---
title: "[C,C++] define 문을 namespace안에 선언하는건 의미가 없다."
categories:
  - Language
tags:
  - Language
  - C,C++
  - define
  - namespace
  - Preprocessor
---

# define 문을 namespace안에 선언하는건 의미가 없다.
```
namespace MyNamespace
{
  #define SOME_VALUE 0xDEADBABE
}
```
을 아래처럼 사용하도록 가이드
```
namespace MyNamespace
{
  const unsigned int SOME_VALUE = 0xDEADBABE;
}
```
[Preprocessor](https://en.wikipedia.org/wiki/C_preprocessor)인 define은 namespace로 경계가 나누어 지지 않기 때문에 namespace로 경계를 나누기 위해서는 const를 사용해야 한다.
