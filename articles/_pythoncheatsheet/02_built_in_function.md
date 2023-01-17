---
title: "내장 함수들"
last_modified_at: 2023-01-17
date: 2022-01-17
header:
  teaser: /assets/images/2023/Screenshot_2023-01-17_at_20-55-19_WelcometoPython.org.png
---

파이썬 인터프리터에는 항상 사용할 수 있는 많은 함수와 형이 내장되어 있다. 알파벳 순으로 정리 하였다.

> [파이썬 표준 라이브러리 - 내장 함수](https://docs.python.org/3/library/functions.html?highlight=built)를 참고해서 작성하였다.

# 파이썬 내장 함수들

| Function                                                             | Description                                                                 |
| -------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| [abs(x)](./#absx)                   | 숫자의 절대값을 반환한다.|
| [aiter()]()               | 비동기로 반복 가능한(Iterable)처리가 가능한 경우 비동기 이터레이터를 반환한다.|
| [all()]()                   | 반복 가능한 모든 요소가 참인 경우에 참을 반환한다.|
| [any()]()                   | 반복 가능한 요소들 중에서 참인 경우가 있으면 참을 반환한다.|
| [ascii()]()               | 객체에 대해서 출력가능한 문자열을 반환한다.|
| [bin()]()                   | 정수를 이진 문자열로 변환한다.|
| [bool()]()                 | 이진값을 반환한다.|
| [breakpoint()]()     | 호출한 부분에 디버거를 사용할 수 있도록 한다.|
| [bytearray()]()       | 바이트로 구성된 배열을 반환한다.|
| [bytes()]()               | 새로운 바이트 객체를 반환한다.|
| [callable()]()         | 객체 인자를 호출 할 수 있는 경우에 참을 반환한다.|
| [chr()]()                   | 문자를 표현하는 문자열을 반환한다.|
| [classmethod()]()   | 메소드를 클래스 메소드로 변경한다.|
| [compile()]()           | 소스를 코드나 AST 객체로 컴파일 한다.|
| [complex()]()           | 실수부 + 허수부\*1로 표현되는 복소수를 반환한다.|
| [delattr()]()           | 객체가 명명된 속성을 제거하는것이 가능하면 명명된 속성을 제거 한다.|
| [dict()]()                 | 새로운 사전을 만든다.|
| [dir()]()                   | 현재 로컬 범위의 이름 목록을 반환한다.|
| [divmod()]()             | 몫과 나머지로 구성된 한 쌍의 숫자를 반환한다. |
| [enumerate()]()       | 열거 객체를 반환한다. |
| [eval'>eval()]()                 | 식을 평가하고 실행한다. |
| [exec'>exec()]()                 | 이 함수는 Python 코드의 동적 실행을 지원한다. |
| [filter'>filter()]()             | 반복가능한 경우 반복자를 생성하고 참을 반환한다. |
| [float'>float()]()               | 숫자 또는 문자열에서 부동 소수점 숫자를 반환한다. |
| [format'>format()]()             | 값을 "포맷된" 표현으로 변환한다. |
| [frozenset'>frozenset()]()       | 새로운 frozenset 객체를 반환한다. |
| [getattr'>getattr()]()           | 객체의 명명된 속성 값을 반환한다. |
| [globals'>globals()]()           | 현재 모듈 네임스페이스를 구현하는 사전을 반환한다. |
| [hasattr'>hasattr()]()           | 문자열이 객체 속성 중 하나의 이름이면 참을 반환한다. |
| [hash'>hash()]()                 | 객체의 해시 값을 반환한다. |
| [help'>help()]()                 | 내장 도움말 시스템을 호출한다. |
| [hex'>hex()]()                   | 정수를 소문자 16진수 문자열로 변환한다. |
| [id'>id()]()                     | 객체의 "ID"를 반환한다. |
| [input'>input()]()               | 이 함수는 입력을 받아 문자열로 변환한다. |
| [int'>int()]() | 숫자 또는 문자열로 구성된 정수 객체를 반환한다. |
| [isinstance'>isinstance()]() | 객체 인수가 객체의 인스턴스이면 True를 반환한다. |
| [issubclass'>issubclass()]() | class가 classinfo의 하위 클래스이면 True를 반환한다. |
| [iter'>iter()]() | 반복자 객체를 반환한다. |
| [len'>len()]() | 객체의 길이(항목 수)를 반환한다. |
| [list'>list()]() | 리스트는 함수가 아니라 변경 가능한 시퀀스 유형이다. |
| [locals'>locals()]() | 현재 로컬 심볼 테이블로 사전을 업데이트하고 반환한다. |
| [map'>map()]() | iterable의 모든 항목에 함수를 적용하는 반복자를 반환한다. |
| [max'>max()]() | iterable에서 가장 큰 항목을 반환한다. |
| [min'>min()]() | iterable에서 가장 작은 항목을 반환한다. |
| [next'>next()]() | 반복자에서 다음 항목을 검색한다. |
| [object'>object()]() | 특징이 없는 새로운 객체를 반환한다. |
| [oct'>oct()]() | 정수를 8진수 문자열로 변환한다. |
| [open'>open()]() | 파일을 열고 해당 파일 객체를 반환한다. |
| [ord'>ord()]() | 문자의 유니코드 코드 포인트를 나타내는 정수를 반환한다. |
| [pow'>pow()]() | 제곱근을 계산하여 반환한다. |
| [print'>print()]() | 개체를 텍스트 스트림 파일로 출력한다. |
| [property'>property()]() | property 속성을 반환한다. |
| [repr'>repr()]() | 객체의 출력 가능한 표현을 포함하는 문자열을 반환한다. |
| [reversed'>reversed()]() | 역 반복자를 반환한다. |
| [round'>round()]() | 소수점 이하 ndigits 정밀도로 반올림된 숫자를 반환한다. |
| [set'>set()]() | 새로운 집합 객체를 반환한다. |
| [setattr'>setattr()]() | 이것은 getattr()의 대응물이다. |
| [slice'>slice()]() | 인덱스 세트를 나타내는 슬라이스 객체를 반환한다. |
| [sorted'>sorted()]() | 반복 가능한 항목들을 새로 정렬된 목록으로 반환한다. |
| [staticmethod'>staticmethod()]() | 메서드를 정적 메서드로 변환한다. |
| [str'>str()]() | 객체의 str 버전을 반환한다. |
| [sum'>sum()]() | 합계가 시작되고 iterable의 항목이 시작된다. |
| [super'>슈퍼()]() | 메서드 호출을 부모 또는 형제에게 위임하는 프록시 개체를 반환한다. |
| [tuple'>tuple()]() | 함수가 아니라 실제로 불변 시퀀스 유형이다. |
| [type'>type()]() | 객체의 유형을 반환한다. |
| [vars'>vars()]() | dict 속성이 있는 다른 객체의 dict 속성을 반환한다. |
| [zip'>zip()]() | 여러 iterable을 병렬로 반복한다. |
|[import()]() | 이 함수는 import 문에 의해 호출된다. |

# A

## abs(x)

숫자의 절댓값을 돌려줍니다. 인자는 정수, 실수 또는 __abs__()를 구현하는 객체입니다. 인자가 복소수면 그 크기가 반환됩니다.

## aiter(async_iterable)

비동기적으로 반복가능한 객체의 이터레이터를 반환한다. x.__aiter__()를 호출하는것과 같다.

> Note: Unlike iter(), aiter() has no 2-argument variant.
> 버전 3.10에서 추가됨.

## all(iterable)
iterable 의 모든 요소가 참이면 (또는 iterable 이 비어있으면) True 를 반환한다.. 아래의 코드와 동일한 동작을 한다.

```python
def all(iterable):
    for element in iterable:
        if not element:
            return False
    return True
```

## awaitable anext(async_iterator), awaitable anext(async_iterator, default)

    When awaited, return the next item from the given asynchronous iterator, or default if given and the iterator is exhausted.

    This is the async variant of the next() builtin, and behaves similarly.

    This calls the __anext__() method of async_iterator, returning an awaitable. Awaiting this returns the next value of the iterator. If default is given, it is returned if the iterator is exhausted, otherwise StopAsyncIteration is raised.

> 버전 3.10에 추가.

## any(iterable)

iterable 의 요소 중 어느 하나라도 참이면 True를 돌려줍니다. iterable이 비어 있으면 False 를 돌려줍니다. 다음과 동등합니다:

```python
def any(iterable):
    for element in iterable:
        if element:
            return True
    return False
```

## ascii(object)
As repr(), return a string containing a printable representation of an object, but escape the non-ASCII characters in the string returned by repr() using \x, \u, or \U escapes. This generates a string similar to that returned by repr() in Python 2.

# B


영문으로 표현된 내용이 더 편한경우에는 아래의 표를 참고 하면 된다.

The Python interpreter has a number of functions and types built into it that are always available.

## Python built-in Functions

| Function                                                             | Description                                                                 |
| -------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| [abs'>abs()]()                   | Return the absolute value of a number.                                      |
| [aiter'>aiter()]()               | Return an asynchronous iterator for an asynchronous iterable.               |
| [all'>all()]()                   | Return True if all elements of the iterable are true.                       |
| [any'>any()]()                   | Return True if any element of the iterable is true.                         |
| [ascii'>ascii()]()               | Return a string with a printable representation of an object.               |
| [bin'>bin()]()                   | Convert an integer number to a binary string.                               |
| [bool'>bool()]()                 | Return a Boolean value.                                                     |
| [breakpoint'>breakpoint()]()     | Drops you into the debugger at the call site.                               |
| [bytearray'>bytearray()]()       | <new-badge /> Return a new array of bytes.                                  |
| [bytes'>bytes()]()               | <new-badge /> Return a new “bytes” object.                                  |
| [callable'>callable()]()         | <new-badge /> Return True if the object argument is callable, False if not. |
| [chr'>chr()]()                   | <new-badge /> Return the string representing a character.                   |
| [classmethod'>classmethod()]()   | Transform a method into a class method.                                     |
| [compile'>compile()]()           | Compile the source into a code or AST object.                               |
| [complex'>complex()]()           | Return a complex number with the value real + imag\*1j.                     |
| [delattr'>delattr()]()           | Deletes the named attribute, provided the object allows it.                 |
| [dict'>dict()]()                 | Create a new dictionary.                                                    |
| [dir'>dir()]()                   | Return the list of names in the current local scope.                        |
| [divmod'>divmod()]()             | Return a pair of numbers consisting of their quotient and remainder.        |
| [enumerate'>enumerate()]()       | Return an enumerate object.                                                 |
| [eval'>eval()]()                 | Evaluates and executes an expression.                                       |
| [exec'>exec()]()                 | This function supports dynamic execution of Python code.                    |
| [filter'>filter()]()             | Construct an iterator from an iterable and returns true.                    |
| [float'>float()]()               | Return a floating point number from a number or string.                     |
| [format'>format()]()             | Convert a value to a “formatted” representation.                            |
| [frozenset'>frozenset()]()       | Return a new frozenset object.                                              |
| [getattr'>getattr()]()           | Return the value of the named attribute of object.                          |
| [globals'>globals()]()           | Return the dictionary implementing the current module namespace.            |
| [hasattr'>hasattr()]()           | True if the string is the name of one of the object’s attributes.           |
| [hash'>hash()]()                 | Return the hash value of the object.                                        |
| [help'>help()]()                 | Invoke the built-in help system.                                            |
| [hex'>hex()]()                   | Convert an integer number to a lowercase hexadecimal string.                |
| [id'>id()]()                     | Return the “identity” of an object.                                         |
| [input'>input()]()               | This function takes an input and converts it into a string.                 |
| [int'>int()]()                   | Return an integer object constructed from a number or string.               |
| [isinstance'>isinstance()]()     | Return True if the object argument is an instance of an object.             |
| [issubclass'>issubclass()]()     | Return True if class is a subclass of classinfo.                            |
| [iter'>iter()]()                 | Return an iterator object.                                                  |
| [len'>len()]()                   | Return the length (the number of items) of an object.                       |
| [list'>list()]()                 | Rather than being a function, list is a mutable sequence type.              |
| [locals'>locals()]()             | Update and return a dictionary with the current local symbol table.         |
| [map'>map()]()                   | Return an iterator that applies function to every item of iterable.         |
| [max'>max()]()                   | Return the largest item in an iterable.                                     |
| [min'>min()]()                   | Return the smallest item in an iterable.                                    |
| [next'>next()]()                 | Retrieve the next item from the iterator.                                   |
| [object'>object()]()             | Return a new featureless object.                                            |
| [oct'>oct()]()                   | Convert an integer number to an octal string.                               |
| [open'>open()]()                 | Open file and return a corresponding file object.                           |
| [ord'>ord()]()                   | Return an integer representing the Unicode code point of a character.       |
| [pow'>pow()]()                   | Return base to the power exp.                                               |
| [print'>print()]()               | Print objects to the text stream file.                                      |
| [property'>property()]()         | Return a property attribute.                                                |
| [repr'>repr()]()                 | Return a string containing a printable representation of an object.         |
| [reversed'>reversed()]()         | Return a reverse iterator.                                                  |
| [round'>round()]()               | Return number rounded to ndigits precision after the decimal point.         |
| [set'>set()]()                   | Return a new set object.                                                    |
| [setattr'>setattr()]()           | This is the counterpart of getattr().                                       |
| [slice'>slice()]()               | Return a sliced object representing a set of indices.                       |
| [sorted'>sorted()]()             | Return a new sorted list from the items in iterable.                        |
| [staticmethod'>staticmethod()]() | Transform a method into a static method.                                    |
| [str'>str()]()                   | Return a str version of object.                                             |
| [sum'>sum()]()                   | Sums start and the items of an iterable.                                    |
| [super'>super()]()               | Return a proxy object that delegates method calls to a parent or sibling.   |
| [tuple'>tuple()]()               | Rather than being a function, is actually an immutable sequence type.       |
| [type'>type()]()                 | Return the type of an object.                                               |
| [vars'>vars()]()                 | Return the dict attribute for any other object with a dict attribute.       |
| [zip'>zip()]()                   | Iterate over several iterables in parallel.                                 |
| [import'>import()]()         | This function is invoked by the import statement.                           |
