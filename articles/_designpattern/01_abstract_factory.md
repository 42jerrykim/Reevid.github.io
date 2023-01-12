---
title: "Abstract Factory"
last_modified_at: 2023-01-12
date: 2022-01-01
header:
  teaser: /assets/images/undefined/design-pattern-nedir-2021-12-18-143754.jpg
---

추상 팩토리 패턴은 개별적인 팩토리들의 그룹을 캡슐화하는 방법을 제공한다. 개별 팩토리는 구체적인 구현 클래스 없이 공통적인 특징을 가지고 있다. 보통의 경우에는 클라이언트 프로그램에서 추상 팩토리에 대한 구현체를 생성하고 인터페이스를 사용하여 구현체를 사용한다. 클라이언트는 결과물(Product)의 제너릭 인터페이스(Generic Interfaces)만 사용하기 때문에 팩토리 내부에서 어떤 구현 객체(Concrete Objects)가 반환되는지 모른다. 팩토리에서 객체를 생성하는 메소드를 인터페이스로 노출 하기 때문에 추상 팩토리 패턴은 객체가 어떻게 구현되어 있는지와 객체를 사용하는 일반적인 방법을 분리 할 수 있다. 그리고 추상 팩토리 패턴은 객체 합성(Object Composition, *Composition 의 경우 구성으로 번역할지, 합성으로 번역할지 애매하다.*)에 의존한다.

# 참고

* [https://en.wikipedia.org/wiki/Abstract_factory_pattern](https://en.wikipedia.org/wiki/Abstract_factory_pattern)
* [객체지향 프로그래밍(OOP) – 2 : Composition and Inheritance](https://actruce.com/copy-object-oriented-programming-2/)
