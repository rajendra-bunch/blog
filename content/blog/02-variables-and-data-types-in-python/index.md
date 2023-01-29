---
title: "02. 파이썬 변수와 데이터타입"
date: "2023-01-29T23:10:41.182Z"
description: "Variables and Data Types in Python"
---

![카페 테이블 위에 오렌지 주스와 IDE가 켜져있는 노트북 사진](./banner.jpg)

<small>사진: <a href="https://unsplash.com/ko/%EC%82%AC%EC%A7%84/HvYy5SEefC8?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Unsplash</a>의<a href="https://unsplash.com/@jantined?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Jantine Doornbos</a>
  </small>

## 변수

변수는 프로그램 내에서 사용되고 조작될 수 있는 데이터를 저장하는 데 사용되기 때문에 모든 프로그래밍 언어에서 중요한 역할을 한다. 파이썬에서 할당 연산자 `=`를 사용하여 변수에 값을 할당할 수 있습니다.

예를 들어: 

```python
name = "John Doe"
age = 30
weight = 68.5
is_student = True
student = None
```

파이썬에서는 다른 프로그래밍 언어와 달리 변수에 값을 할당하기 전에 변수의 데이터 유형을 선언할 필요가 없습니다. Python에서 변수의 데이터 유형은 사용자가 할당한 값에 따라 동적으로 결정됩니다. 이 기능을 "동적 타이핑"이라고 합니다

파이썬의 기본 데이터 유형은 다음과 같습니다:

- **String**: 문자열은 문자, 숫자 및 기호와 같은 문자의 시퀀스입니다. 작은따옴표(`'`) 또는 큰따옴표(`"`)를 사용하여 파이썬에서 문자열을 정의할 수 있습니다. 문자열은 `+` 연산자를 사용하여 연결할 수 있습니다.  
  예: `name = "John Doe"`
- **Integer**: 정수(`Integer`)는 분수 성분이 없는 정수입니다. 정수는 파이썬에서 10진수 시스템으로 표현됩니다.  
  예: `age = 30`
- **Float**: 플로트(`Float`)는 분수 성분이 있는 숫자입니다. 부동소수점 숫자는 파이썬에서 소수점으로 표현됩니다.
  예: `weight = 68.5`
- **Boolean**: 부울(`Boolean`) 값은 참(`True`) 또는 거짓(`False`)입니다. 입니다. `Boolean`은 프로그램에서 이진 조건 또는 결정을 나타내는데 사용됩니다.  
  예: `is_student = True`
- **None**: 값 없음(`None`)은 Python에서 값이 없음을 나타냅니다. 일반적으로 아직 값이 할당되지 않은 개체 또는 변수의 자리 표시자로 사용됩니다.  
  예: `student = None`

Python의 데이터 유형은 프로그램에서 데이터를 사용하고 조작하는 방법에 영향을 미치기 때문에 이해하는 것이 중요합니다. 예를 들어 문자열에 대해 수학적 연산을 수행하거나 문자열과 정수를 비교할 수 없습니다.

Python의 `type()` 함수를 사용하여 변수의 데이터 유형을 확인할 수 있습니다.

예시: 
```python
name = "John Doe"
print(type(name)) # Output: <class 'str'>

age = 30
print(type(age)) # Output: <class 'int'>

weight = 68.5
print(type(weight)) # Output: <class 'float'>
```

Python에서 변수에 대한 설명적이고 의미 있는 이름을 선택하는 것은 코드를 읽고 이해하기 쉽게 하기 때문에 좋은 관행입니다.


## Python에서의 타입 변환

경우에 따라 Python에서 한 데이터 유형을 다른 데이터 유형으로 변환해야 할 수도 있습니다. 이 작업은 `int()`, `float()`, `str()`과 같은 빌트인 타입 변환 함수를 이용하여 수행할 수 있습니다.

예를 들어:

```python
# Converting from float to int
weight = 68.5
weight = int(weight)
print(weight) # Output: 68

# Converting from int to float
age = 30
age = float(age)
print(age) # Output: 30.0

# Converting from int to string
age = 30
age = str(age)
print(age) # Output: "30"

# Converting from string to int
weight = "68.5"
weight = float(weight)
print(weight) # Output: 68.5
```

모든 변환이 가능한 것은 아닙니다. 예를 들어, `int()` 함수를 사용하여 숫자가 아닌 문자를 포함하는 문자열을 정수로 변환할 수 없습니다. 그러면 `ValueError`가 발생합니다.

또한 문자열을 부울 값으로 변환하려는 경우와 같이 값을 호환되지 않는 데이터 형식으로 변환하려고 하면 `TypeError`가 발생할 수 있습니다.

```python
# This will result in a ValueError
age = "thirty"
age = int(age)
print(age) # Output: ValueError: invalid literal for int() with base 10: 'thirty'

# This will result in a TypeError
is_student = "True"
is_student = bool(is_student)
print(is_student) # Output: TypeError: Cannot convert 'True' to bool
```

오류를 방지하려면 이러한 제한 사항을 인식하고 코드에서 적절하게 처리해야 합니다.
