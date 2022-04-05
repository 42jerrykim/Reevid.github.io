---
title: "[C#] Source Generators"
category: DotNET
tag:
- C#
- .NET
- DotNET
- Convert
- long
- int
header:
  teaser: https://media.vlpt.us/images/jinuku/post/e62f8f63-4001-46f9-b811-dc6f62f0828e/40cc3e52-745d-48b8-8a09-02c21efc36e5.png
---

# 일반적인 적용 방법

* 런타임 리플렉션
* Juggling MSBuild tasks.
* Intermediate Language (IL) weaving (본 글에서는 다루지 않는다).

## Runtime reflection

런타임 리플렉션은 오래 전에 .NET에 추가된 강력한 기술입니다. 이를 사용하는 수많은 시나리오가 있습니다. 일반적인 시나리오는 앱이 시작될 때 사용자 코드의 일부 분석을 수행하고 해당 데이터를 사용하여 작업을 생성하는 것입니다.

예를 들어 ASP.NET Core 웹 서비스가 처음 실행되면 리플렉션을 사용하여 정의한 구문을 검색하여 컨트롤러 및 razor 페이지와 같은 것을 **연결**할 수 있습니다. 이렇게 하면 강력한 추상화로 간단한 코드를 작성할 수 있지만 런타임에 성능 저하가 발생합니다. 웹 서비스 또는 앱이 처음 시작될 때 코드에 대한 정보를 검색하는 모든 런타임 리플렉션 코드 실행이 완료될 때까지 요청을 수락할 수 없습니다. 이 성능 저하는 크지는 않지만 자체 앱에서 개선할 수 없는 고정 비용입니다.

Source Generator를 사용하면 시작의 컨트롤러 검색 단계가 대신 컴파일 시간에 발생할 수 있습니다. 생성기는 소스 코드를 분석하고 앱을 **연결**하는 데 필요한 코드를 내보낼 수 있습니다. Source Generator를 사용하면 오늘 런타임에 발생하는 작업이 컴파일 시간으로 푸시될 수 있으므로 시작 시간이 더 빨라질 수 있습니다.

## MSBuild 작업 저글링

원본 생성기는 런타임 시 리플렉션에 제한되지 않도록 성능을 개선하여 형식도 검색할 수 있습니다. 일부 시나리오에서는 컴파일에서 데이터를 검사할 수 있도록 MSBuild C# 작업(CSC라고 함)을 여러 번 호출합니다. 짐작하시겠지만, 컴파일러를 두 번 이상 호출하면 앱을 구축하는 데 걸리는 총 시간이 영향을 받습니다. 원본 생성기는 일부 성능 혜택을 제공할 뿐만 아니라 도구가 올바른 추상화 수준에서 작동할 수 있도록 해주므로, 이와 같이 MSBuild 작업을 저글링할 필요가 없도록 원본 생성기를 사용할 방법을 조사하고 있습니다.

원본 생성기가 제공할 수 있는 또 다른 기능은 컨트롤러와 razor 페이지 간의 ASP.NET Core 라우팅 작동 방식과 같은 일부 "문자열 형식" API의 사용을 방해합니다. 원본 생성기를 사용하면 컴파일 시간 세부 정보로 생성되는 데 필요한 문자열로 라우팅을 강력하게 입력할 수 있습니다. 이렇게 하면 잘못 입력된 문자열 리터럴이 올바른 컨트롤러에 도달하지 않는 요청으로 이어지는 횟수가 줄어듭니다.

# 참고
* [Introducing C# Source Generators](https://devblogs.microsoft.com/dotnet/introducing-c-source-generators/)
* [Source Generators](https://docs.microsoft.com/en-us/dotnet/csharp/roslyn-sdk/source-generators-overview)
