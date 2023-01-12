---
title: "Abstract Factory"
last_modified_at: 2023-01-12
date: 2022-01-01
header:
  teaser: /assets/images/undefined/design-pattern-nedir-2021-12-18-143754.jpg
---

추상 팩토리 패턴은 여러개의 개별적인 팩토리를 캡슐화하는 방법을 제공한다. 각각의 팩토리는 구현 클래스(Concrete Class) 없이 공통의 기능을 가지고 있어야 한다. 보통의 경우에는 클라이언트 프로그램에서 추상 팩토리에 대한 구현체(Concrete Implementation)를 생성하고 팩토리의 제너릭 인터페이스를 사용하여 구현체를 사용한다. 클라이언트는 결과물(Product)의 제너릭 인터페이스(Generic Interfaces)만 사용하기 때문에 팩토리 내부에서 어떤 객체(Concrete Objects)가 반환되는지 모른다. 팩토리에서 객체를 생성하는 메소드를 인터페이스로 노출하기 때문에 추상 팩토리 패턴은 객체가 어떻게 구현되어 있는지와 객체를 사용하는 일반적인 방법을 분리 할 수 있다. 그리고 추상 팩토리 패턴은 객체 합성(Object Composition)에 의존한다.

# 개요

추상 팩토리 패턴은 잘 알려진 23개의 패턴중에서 아래와 같은 상황에서 사용할 수 있는 패턴이다.

* 어플리케이션과 객체를 어떤식으로 생성하는지 독립적으로 처리해야 할때
* 클래스와 객체를 생성할때 필요한것들과 분리 시키고 싶을때
* 관련되거나 의존하는 객체를 한번에 생성하고 싶을때

# 정의

추상 팩토리 패턴은 객체에 대한 구현 클래스 없이, 관련되거나 의존성이 있는 객체들을 생성하는 인터페이스다.

# 사용법

# 구조

# 예시

# 구체적인 구현클래스가 없는 팩토리 예시

아래의 코드에서 WinFactory는 IButton을 반환하는 메소드만 가지고 있기 때문에 구현 클래스(Concrete Classes)가 없다고 말할 수 있다.

```csharp
interface IButton
{
    void Paint();
}

interface IGUIFactory
{
    IButton CreateButton();
}

class WinFactory : IGUIFactory
{
    public IButton CreateButton()
    {
        return new WinButton();
    }
}
```

# 영문 단어 번역 사전

|영문|한글|
|:---|:---|
|Concrete Implementation|구현체|
|Concrete Objects|구현 객체|
|Concrete Classes|구현 클래스|
|Object Composition|객체 합성 (Composition 의 경우 구성으로 번역할지, 합성으로 번역할지 애매하다.)|

# 참고

* [https://en.wikipedia.org/wiki/Abstract_factory_pattern](https://en.wikipedia.org/wiki/Abstract_factory_pattern)
* [객체지향 프로그래밍(OOP) – 2 : Composition and Inheritance](https://actruce.com/copy-object-oriented-programming-2/)
