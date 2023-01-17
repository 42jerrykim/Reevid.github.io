---
title: "Basic"
last_modified_at: 2023-01-17
date: 2022-01-17
header:
  teaser: 
---

우리는 어디에선가 시작할 필요가 있다. 바로 여기서 그 시작점이다.

> [The Python Tutorial](https://docs.python.org/3/tutorial/index.html)에서 내용을 가지고 왔다.
> 
> Python is an easy to learn, powerful programming language [...] Python’s elegant syntax and dynamic typing, together with its interpreted nature, make it an ideal language for scripting and rapid application development. 파이썬은 배우기 쉬운 언어이면서 강력한 언어이다. 파이썬은 우아한 문법과 다이나믹 파입을 지원한다. 이것들은 자연스럽게 어우러져 스크립팅과 빠른 어플리케이션 개발하는데 있어서 이상적인 언어로 만든다.

# 수학 함수

우선 순위가 높은 순서로 나열 하였다.

|Operators|Operation|Example|
|:---|:---|:---|
|**|Exponent|2 ** 3 = 8|
|%|Modulus/Remainder|22 % 8 = 6|
|//|Integer division|22 // 8 = 2|
|/|Division|22 / 8 = 2.75|
|*|Multiplication|3 * 3 = 9|
|-|Subtraction|5 - 2 = 3|
|+|Addition|2 + 2 = 4|

## 수학 함수 예시

```python
>>> 2 + 3 * 6
# 20

>>> (2 + 3) * 6
# 30

>>> 2 ** 8
#256

>>> 23 // 7
# 3

>>> 23 % 7
# 2

>>> (5 - 1) * ((7 + 1) / (3 - 1))
# 16.0
```

# 증강 연산자

|Operator|Equivalent|
|:---|:---|
|var += 1|var = var + 1|
|var -= 1|var = var - 1|
|var *= 1|var = var * 1|
|var /= 1|var = var / 1|
|var %= 1|var = var % 1|

## 예시

```python
>>> greeting = 'Hello'
>>> greeting += ' world!'
>>> greeting
# 'Hello world!'

>>> number = 1
>>> number += 1
>>> number
# 2

>>> my_list = ['item']
>>> my_list *= 3
>>> my_list
# ['item', 'item', 'item']
```

# 자료형

|Data Type|Examples
|:---|:---|
|Integers|-2, -1, 0, 1, 2, 3, 4, 5|
|Floating-point numbers|-1.25, -1.0, --0.5, 0.0, 0.5, 1.0, 1.25|
|Strings|'a', 'aa', 'aaa', 'Hello!', '11 cats'|

# 결합(Concatenation)과 복사

## 스트링 결합

```python
>>> 'Alice' 'Bob'
# 'AliceBob'
```

## 문자열 복사

```python
>>> 'Alice' * 5
# 'AliceAliceAliceAliceAlice'
```

# 변수
1. 한 단어로 변수를 지정할 수 있다.
    ```python
    >>> # bad
    >>> my variable = 'Hello'

    >>> # good
    >>> var = 'Hello'
    ```
1. 문자, 숫자, `_`만 사용 할 수 있다.
    ```python
    >>> # bad
    >>> %$@variable = 'Hello'

    >>> # good
    >>> my_var = 'Hello'

    >>> # good
    >>> my_var_2 = 'Hello'
    ```
1. 숫자로 시작 할 수 없다.
    ```python
    >>> # this wont work
    >>> 23_var = 'hello'
    ```
1. 이름의 처음에 `_`를 사용하는것은 별로 유용하지 않다고 생각할 수 있다.
    ```python
    >>> # _spam should not be used again in the code
    >>> _spam = 'Hello'
    ```