---
title: "[Regex] C#에서 Regex로 검색한 결과를 재사용하는 방법"
categories:
  - Regex
tags:
  - Regex
  - C#
  - match
  - Lamda
---

문자열에서 내가 원하는것을 검색하고 변경하고 삭제하는 작업을 하는데 있어서 Regex는 매우 좋은 방법이다. 본 글에서는 Regex에서 검색된 결과를 재사용하는 방법에 대해서 알아 본다.

``` { id:'Outsider', sex:"23" } ```가 있을때 쌍따옴표로 감싸진 "23"을 23으로 변경하는 방법을 예시를 들어서 살펴 보자.

# match와 람다 사용

``` Regex.Replace() ```를 사용해서 정규식을 이용해서 "23"을 검색하면 검색의 결과가 ``` match ```로 전달된다 
이때 람다를 사용해서 ```match```를 재사용하여 변경을 할 수 있다.

## Sample code

``` csharp
string str = "{ id:'Outsider', sex:\"23\" }";
Console.WriteLine(str);
str = Regex.Replace(str, "\"[0-9]+\"", match => match.Value.Replace("\"", "")); // 
Console.WriteLine(str);
```

## Sample code의 출력 결과

``` json
{ id:'Outsider', sex:"23" }
{ id:'Outsider', sex:23 }
```