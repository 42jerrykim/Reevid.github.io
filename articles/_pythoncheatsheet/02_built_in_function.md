---
title: "내장 함수들"
last_modified_at: 2023-01-17
date: 2022-01-17
header:
  teaser: /assets/images/2023/Screenshot_2023-01-17_at_20-55-19_WelcometoPython.org.png
---

파이썬 인터프리터는 다양한 함수와 타입을 내장하고 있어서 언제든지 사용가능하다.

# 파이썬 내장 함수들

| Function                                                             | Description                                                                 |
| -------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| <router-link to='/builtin/abs'>abs()</router-link>                   | 숫자의 절대값을 반환한다.|
| <router-link to='/builtin/aiter'>aiter()</router-link>               | 비동기로 반복 가능한(Iterable)처리가 가능한 경우 비동기 이터레이터를 반환한다.|
| <router-link to='/builtin/all'>all()</router-link>                   | 반복 가능한 모든 요소가 참인 경우에 참을 반환한다.|
| <router-link to='/builtin/any'>any()</router-link>                   | 반복 가능한 요소들 중에서 참인 경우가 있으면 참을 반환한다.|
| <router-link to='/builtin/ascii'>ascii()</router-link>               | 객체에 대해서 출력가능한 문자열을 반환한다.|
| <router-link to='/builtin/bin'>bin()</router-link>                   | 정수를 이진 문자열로 변환한다.|
| <router-link to='/builtin/bool'>bool()</router-link>                 | 이진값을 반환한다.|
| <router-link to='/builtin/breakpoint'>breakpoint()</router-link>     | 호출한 부분에 디버거를 사용할 수 있도록 한다.|
| <router-link to='/builtin/bytearray'>bytearray()</router-link>       | 바이트로 구성된 배열을 반환한다.|
| <router-link to='/builtin/bytes'>bytes()</router-link>               | 새로운 바이트 객체를 반환한다.|
| <router-link to='/builtin/callable'>callable()</router-link>         | 객체 인자를 호출 할 수 있는 경우에 참을 반환한다.|
| <router-link to='/builtin/chr'>chr()</router-link>                   | 문자를 표현하는 문자열을 반환한다.|
| <router-link to='/builtin/classmethod'>classmethod()</router-link>   | 메소드를 클래스 메소드로 변경한다.|
| <router-link to='/builtin/compile'>compile()</router-link>           | 소스를 코드나 AST 객체로 컴파일 한다.|
| <router-link to='/builtin/complex'>complex()</router-link>           | 실수부 + 허수부\*1로 표현되는 복소수를 반환한다.|
| <router-link to='/builtin/delattr'>delattr()</router-link>           | 객체가 명명된 속성을 제거하는것이 가능하면 명명된 속성을 제거 한다.|
| <router-link to='/builtin/dict'>dict()</router-link>                 | 새로운 사전을 만든다.|
| <router-link to='/builtin/dir'>dir()</router-link>                   | 현재 로컬 범위의 이름 목록을 반환한다.|
| <router-link to='/builtin/divmod'>divmod()</router-link>             | 몫과 나머지로 구성된 한 쌍의 숫자를 반환한다. |
| <router-link to='/builtin/enumerate'>enumerate()</router-link>       | 열거 객체를 반환한다. |
| <router-link to='/builtin/eval'>eval()</router-link>                 | 식을 평가하고 실행한다. |
| <router-link to='/builtin/exec'>exec()</router-link>                 | 이 함수는 Python 코드의 동적 실행을 지원한다. |
| <router-link to='/builtin/filter'>filter()</router-link>             | 반복가능한 경우 반복자를 생성하고 참을 반환한다. |
| <router-link to='/builtin/float'>float()</router-link>               | 숫자 또는 문자열에서 부동 소수점 숫자를 반환한다. |
| <router-link to='/builtin/format'>format()</router-link>             | 값을 "포맷된" 표현으로 변환한다. |
| <router-link to='/builtin/frozenset'>frozenset()</router-link>       | 새로운 frozenset 객체를 반환한다. |
| <router-link to='/builtin/getattr'>getattr()</router-link>           | 객체의 명명된 속성 값을 반환한다. |
| <router-link to='/builtin/globals'>globals()</router-link>           | 현재 모듈 네임스페이스를 구현하는 사전을 반환한다. |
| <router-link to='/builtin/hasattr'>hasattr()</router-link>           | 문자열이 객체 속성 중 하나의 이름이면 참을 반환한다. |
| <router-link to='/builtin/hash'>hash()</router-link>                 | 객체의 해시 값을 반환한다. |
| <router-link to='/builtin/help'>help()</router-link>                 | 내장 도움말 시스템을 호출한다. |
| <router-link to='/builtin/hex'>hex()</router-link>                   | 정수를 소문자 16진수 문자열로 변환한다. |
| <router-link to='/builtin/id'>id()</router-link>                     | 객체의 "ID"를 반환한다. |
| <router-link to='/builtin/input'>input()</router-link>               | 이 함수는 입력을 받아 문자열로 변환한다. |
| <router-link to='/builtin/int'>int()</router-link> | 숫자 또는 문자열로 구성된 정수 객체를 반환한다. |
| <router-link to='/builtin/isinstance'>isinstance()</router-link> | 객체 인수가 객체의 인스턴스이면 True를 반환한다. |
| <router-link to='/builtin/issubclass'>issubclass()</router-link> | class가 classinfo의 하위 클래스이면 True를 반환한다. |
| <router-link to='/builtin/iter'>iter()</router-link> | 반복자 객체를 반환한다. |
| <router-link to='/builtin/len'>len()</router-link> | 객체의 길이(항목 수)를 반환한다. |
| <router-link to='/builtin/list'>list()</router-link> | 리스트는 함수가 아니라 변경 가능한 시퀀스 유형이다. |
| <router-link to='/builtin/locals'>locals()</router-link> | 현재 로컬 심볼 테이블로 사전을 업데이트하고 반환한다. |
| <router-link to='/builtin/map'>map()</router-link> | iterable의 모든 항목에 함수를 적용하는 반복자를 반환한다. |
| <router-link to='/builtin/max'>max()</router-link> | iterable에서 가장 큰 항목을 반환한다. |
| <router-link to='/builtin/min'>min()</router-link> | iterable에서 가장 작은 항목을 반환한다. |
| <router-link to='/builtin/next'>next()</router-link> | 반복자에서 다음 항목을 검색한다. |
| <router-link to='/builtin/object'>object()</router-link> | 특징이 없는 새로운 객체를 반환한다. |
| <router-link to='/builtin/oct'>oct()</router-link> | 정수를 8진수 문자열로 변환한다. |
| <router-link to='/builtin/open'>open()</router-link> | 파일을 열고 해당 파일 객체를 반환한다. |
| <router-link to='/builtin/ord'>ord()</router-link> | 문자의 유니코드 코드 포인트를 나타내는 정수를 반환한다. |
| <router-link to='/builtin/pow'>pow()</router-link> | 제곱근을 계산하여 반환한다. |
| <router-link to='/builtin/print'>print()</router-link> | 개체를 텍스트 스트림 파일로 출력한다. |
| <router-link to='/builtin/property'>property()</router-link> | property 속성을 반환한다. |
| <router-link to='/builtin/repr'>repr()</router-link> | 객체의 출력 가능한 표현을 포함하는 문자열을 반환한다. |
| <router-link to='/builtin/reversed'>reversed()</router-link> | 역 반복자를 반환한다. |
| <router-link to='/builtin/round'>round()</router-link> | 소수점 이하 ndigits 정밀도로 반올림된 숫자를 반환한다. |
| <router-link to='/builtin/set'>set()</router-link> | 새로운 집합 객체를 반환한다. |
| <router-link to='/builtin/setattr'>setattr()</router-link> | 이것은 getattr()의 대응물이다. |
| <router-link to='/builtin/slice'>slice()</router-link> | 인덱스 세트를 나타내는 슬라이스 객체를 반환한다. |
| <router-link to='/builtin/sorted'>sorted()</router-link> | 반복 가능한 항목들을 새로 정렬된 목록으로 반환한다. |
| <router-link to='/builtin/staticmethod'>staticmethod()</router-link> | 메서드를 정적 메서드로 변환한다. |
| <router-link to='/builtin/str'>str()</router-link> | 객체의 str 버전을 반환한다. |
| <router-link to='/builtin/sum'>sum()</router-link> | 합계가 시작되고 iterable의 항목이 시작된다. |
| <router-link to='/builtin/super'>슈퍼()</router-link> | 메서드 호출을 부모 또는 형제에게 위임하는 프록시 개체를 반환한다. |
| <router-link to='/builtin/tuple'>tuple()</router-link> | 함수가 아니라 실제로 불변 시퀀스 유형이다. |
| <router-link to='/builtin/type'>type()</router-link> | 객체의 유형을 반환한다. |
| <router-link to='/builtin/vars'>vars()</router-link> | dict 속성이 있는 다른 객체의 dict 속성을 반환한다. |
| <router-link to='/builtin/zip'>zip()</router-link> | 여러 iterable을 병렬로 반복한다. |
| <router-link to='/builtin/import'>**import**()</router-link> | 이 함수는 import 문에 의해 호출된다. |

영문으로 표현된 내용이 더 편한경우에는 아래의 표를 참고 하면 된다.

The Python interpreter has a number of functions and types built into it that are always available.

## Python built-in Functions

| Function                                                             | Description                                                                 |
| -------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| <router-link to='/builtin/abs'>abs()</router-link>                   | Return the absolute value of a number.                                      |
| <router-link to='/builtin/aiter'>aiter()</router-link>               | Return an asynchronous iterator for an asynchronous iterable.               |
| <router-link to='/builtin/all'>all()</router-link>                   | Return True if all elements of the iterable are true.                       |
| <router-link to='/builtin/any'>any()</router-link>                   | Return True if any element of the iterable is true.                         |
| <router-link to='/builtin/ascii'>ascii()</router-link>               | Return a string with a printable representation of an object.               |
| <router-link to='/builtin/bin'>bin()</router-link>                   | Convert an integer number to a binary string.                               |
| <router-link to='/builtin/bool'>bool()</router-link>                 | Return a Boolean value.                                                     |
| <router-link to='/builtin/breakpoint'>breakpoint()</router-link>     | Drops you into the debugger at the call site.                               |
| <router-link to='/builtin/bytearray'>bytearray()</router-link>       | <new-badge /> Return a new array of bytes.                                  |
| <router-link to='/builtin/bytes'>bytes()</router-link>               | <new-badge /> Return a new “bytes” object.                                  |
| <router-link to='/builtin/callable'>callable()</router-link>         | <new-badge /> Return True if the object argument is callable, False if not. |
| <router-link to='/builtin/chr'>chr()</router-link>                   | <new-badge /> Return the string representing a character.                   |
| <router-link to='/builtin/classmethod'>classmethod()</router-link>   | Transform a method into a class method.                                     |
| <router-link to='/builtin/compile'>compile()</router-link>           | Compile the source into a code or AST object.                               |
| <router-link to='/builtin/complex'>complex()</router-link>           | Return a complex number with the value real + imag\*1j.                     |
| <router-link to='/builtin/delattr'>delattr()</router-link>           | Deletes the named attribute, provided the object allows it.                 |
| <router-link to='/builtin/dict'>dict()</router-link>                 | Create a new dictionary.                                                    |
| <router-link to='/builtin/dir'>dir()</router-link>                   | Return the list of names in the current local scope.                        |
| <router-link to='/builtin/divmod'>divmod()</router-link>             | Return a pair of numbers consisting of their quotient and remainder.        |
| <router-link to='/builtin/enumerate'>enumerate()</router-link>       | Return an enumerate object.                                                 |
| <router-link to='/builtin/eval'>eval()</router-link>                 | Evaluates and executes an expression.                                       |
| <router-link to='/builtin/exec'>exec()</router-link>                 | This function supports dynamic execution of Python code.                    |
| <router-link to='/builtin/filter'>filter()</router-link>             | Construct an iterator from an iterable and returns true.                    |
| <router-link to='/builtin/float'>float()</router-link>               | Return a floating point number from a number or string.                     |
| <router-link to='/builtin/format'>format()</router-link>             | Convert a value to a “formatted” representation.                            |
| <router-link to='/builtin/frozenset'>frozenset()</router-link>       | Return a new frozenset object.                                              |
| <router-link to='/builtin/getattr'>getattr()</router-link>           | Return the value of the named attribute of object.                          |
| <router-link to='/builtin/globals'>globals()</router-link>           | Return the dictionary implementing the current module namespace.            |
| <router-link to='/builtin/hasattr'>hasattr()</router-link>           | True if the string is the name of one of the object’s attributes.           |
| <router-link to='/builtin/hash'>hash()</router-link>                 | Return the hash value of the object.                                        |
| <router-link to='/builtin/help'>help()</router-link>                 | Invoke the built-in help system.                                            |
| <router-link to='/builtin/hex'>hex()</router-link>                   | Convert an integer number to a lowercase hexadecimal string.                |
| <router-link to='/builtin/id'>id()</router-link>                     | Return the “identity” of an object.                                         |
| <router-link to='/builtin/input'>input()</router-link>               | This function takes an input and converts it into a string.                 |
| <router-link to='/builtin/int'>int()</router-link>                   | Return an integer object constructed from a number or string.               |
| <router-link to='/builtin/isinstance'>isinstance()</router-link>     | Return True if the object argument is an instance of an object.             |
| <router-link to='/builtin/issubclass'>issubclass()</router-link>     | Return True if class is a subclass of classinfo.                            |
| <router-link to='/builtin/iter'>iter()</router-link>                 | Return an iterator object.                                                  |
| <router-link to='/builtin/len'>len()</router-link>                   | Return the length (the number of items) of an object.                       |
| <router-link to='/builtin/list'>list()</router-link>                 | Rather than being a function, list is a mutable sequence type.              |
| <router-link to='/builtin/locals'>locals()</router-link>             | Update and return a dictionary with the current local symbol table.         |
| <router-link to='/builtin/map'>map()</router-link>                   | Return an iterator that applies function to every item of iterable.         |
| <router-link to='/builtin/max'>max()</router-link>                   | Return the largest item in an iterable.                                     |
| <router-link to='/builtin/min'>min()</router-link>                   | Return the smallest item in an iterable.                                    |
| <router-link to='/builtin/next'>next()</router-link>                 | Retrieve the next item from the iterator.                                   |
| <router-link to='/builtin/object'>object()</router-link>             | Return a new featureless object.                                            |
| <router-link to='/builtin/oct'>oct()</router-link>                   | Convert an integer number to an octal string.                               |
| <router-link to='/builtin/open'>open()</router-link>                 | Open file and return a corresponding file object.                           |
| <router-link to='/builtin/ord'>ord()</router-link>                   | Return an integer representing the Unicode code point of a character.       |
| <router-link to='/builtin/pow'>pow()</router-link>                   | Return base to the power exp.                                               |
| <router-link to='/builtin/print'>print()</router-link>               | Print objects to the text stream file.                                      |
| <router-link to='/builtin/property'>property()</router-link>         | Return a property attribute.                                                |
| <router-link to='/builtin/repr'>repr()</router-link>                 | Return a string containing a printable representation of an object.         |
| <router-link to='/builtin/reversed'>reversed()</router-link>         | Return a reverse iterator.                                                  |
| <router-link to='/builtin/round'>round()</router-link>               | Return number rounded to ndigits precision after the decimal point.         |
| <router-link to='/builtin/set'>set()</router-link>                   | Return a new set object.                                                    |
| <router-link to='/builtin/setattr'>setattr()</router-link>           | This is the counterpart of getattr().                                       |
| <router-link to='/builtin/slice'>slice()</router-link>               | Return a sliced object representing a set of indices.                       |
| <router-link to='/builtin/sorted'>sorted()</router-link>             | Return a new sorted list from the items in iterable.                        |
| <router-link to='/builtin/staticmethod'>staticmethod()</router-link> | Transform a method into a static method.                                    |
| <router-link to='/builtin/str'>str()</router-link>                   | Return a str version of object.                                             |
| <router-link to='/builtin/sum'>sum()</router-link>                   | Sums start and the items of an iterable.                                    |
| <router-link to='/builtin/super'>super()</router-link>               | Return a proxy object that delegates method calls to a parent or sibling.   |
| <router-link to='/builtin/tuple'>tuple()</router-link>               | Rather than being a function, is actually an immutable sequence type.       |
| <router-link to='/builtin/type'>type()</router-link>                 | Return the type of an object.                                               |
| <router-link to='/builtin/vars'>vars()</router-link>                 | Return the dict attribute for any other object with a dict attribute.       |
| <router-link to='/builtin/zip'>zip()</router-link>                   | Iterate over several iterables in parallel.                                 |
| <router-link to='/builtin/import'>**import**()</router-link>         | This function is invoked by the import statement.                           |
