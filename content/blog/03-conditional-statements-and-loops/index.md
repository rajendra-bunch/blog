---
title: "[파이썬 기초] 03. 조건문 및 루프"
date: "2023-01-31T00:20:32.000Z"
description: "Conditional Statements and Loops"
---

## 조건문

Python의 조건문을 사용하면 코드에서 결정을 내릴 수 있습니다. 예를 들어, 숫자가 짝수인지 홀수인지 확인하고 결과에 따라 다른 작업을 수행할 수 있습니다. 추가적으로 들여쓰기(indent)에 주의해주세요. 파이썬에서 들여쓰기는 코드블록의 구분에 중요한 역할을 하므로, 정확히 이루어져야 합니다.


```python
if number % 2 == 0:
    print("The number is even")
else:
    print("The number is odd")
```

특정 조건이 충족되는지 여부에 따라 코드에서 결정을 내릴 수 있습니다. Python에서 `if`, `elif` 및 `else` 문을 사용하여 이러한 조건을 정의할 수 있습니다.

여기에 또 다른 예가 있습니다:

```python
fruit = 'apple'
if fruit == 'apple':
    print("이것은 사과입니다")
elif fruit == 'banana':
    print("이것은 바나나입니다")
else:
    print("이것은 사과도 바나나도 아닙니다")
```

이 코드에서 첫 번째 `if` 문은 `fruit`의 값이 `apple`과 같은지 확인합니다. 만약 그렇다면, `if` 블록 내부의 코드가 실행되고 "이것은 사과입니다"라는 메시지가 인쇄됩니다. 그렇지 않은 경우, 코드는 과일의 값이 `banana`와 같은지 확인하는 `elif` 문으로 이동합니다. 그렇다면 `elif` 블록 내부의 코드가 실행되고 "이것은 바나나입니다"라는 메시지가 인쇄됩니다. `if` 조건과 `elif` 조건이 모두 충족되지 않으면 `else` 블록 내부의 코드가 실행되고 "이것은 사과도 바나나도 아닙니다"라는 메시지가 인쇄됩니다.

여러 개의 `elif` 문을 사용할 수 있으며 필요하지 않은 경우 사용하지 않아도 됩니다.

```python
fruit = 'cherry'
if fruit == 'apple':
    print("This is an apple")
elif fruit == 'banana':
    print("This is a banana")
elif fruit == 'cherry':
    print("This is a cherry")
```

이 코드에서 `if`와 `elif`문은 과일의 다른 값을 확인하고, 과일의 값에 따라 적절한 블록 내의 코드가 실행됩니다.


## 반복문 (Loops)

루프를 사용하면 코드 블록을 여러 번 반복할 수 있습니다. 파이썬의 루프에는 크게 `for` 루프와 `while` 루프 두 가지 유형이 있습니다.

### for 루프

`for` 루프는 리스트(`list`) 또는 문자열과 같은 시퀀스에서 반복하는 것에 사용됩니다. 리스트에 대한 설명은 다음 강의에서 자세히 설명드리겠습니다. 다음은 간단한 예입니다:

```python
fruits = ['apple', 'banana', 'cherry']
for fruit in fruits:
    print(fruit)

```

이 코드에서 `for` 루프는 `fruits` 리스트에 대해 반복되며 각 반복에 대해 `fruit`의 값은 `fruits` 리스트의 현재 항목으로 설정됩니다. 그런 다음 루프 내부의 코드가 실행되고 `fruit`의 값이 출력됩니다.

### while 루프

반면 `while` 루프는 특정 조건이 충족되는 한 코드 블록을 반복하는 데 사용됩니다. 다음은 간단한 예입니다:


```python
count = 0
while count < 5:
    print(count)
    count += 1
```

이 코드에서 `while` 루프는 `count` 값이 5보다 작으면 루프 내부에서 코드를 반복합니다. 각 반복에서 `count` 값이 출력된 다음 1씩 증가합니다. 카운트 값이 5 이상이면 루프가 중지됩니다.

루프 중에 사용할 때 주의해야 합니다. 조건이 충족되지 않으면 무한 루프가 발생할 수 있습니다.

### break

`break` 문은 루프를 조기에 해제하는 데 사용됩니다. 예를 들어 목록에서 특정 항목을 검색하는 `for` 루프가 있는 경우 `break` 문을 사용하여 항목이 발견되는 즉시 루프를 종료할 수 있습니다.

다음은 예입니다:

```python
fruits = ['apple', 'banana', 'cherry']
search_fruit = 'banana'
for fruit in fruits:
    if fruit == search_fruit:
        print(f'{search_fruit} found')
        break
```

이 코드에서 `for` 루프는 `fruits` 리스트에 대해 반복되며 각 반복에 대해 `fruit`의 값은 리스트의 현재 항목으로 설정됩니다. 루프 내부의 코드는 `fruit`의 값이 `search_fruit`과 같은지 확인합니다. 그렇다면 'banana found' 메시지가 인쇄되고 브레이크 문이 실행되어 루프에서 벗어납니다.

## Python에서 들여쓰기(Indentation)

파이썬에서 들여쓰기(indent)는 함께 속한 코드 블록을 나타내기 위해 사용된다. 코드 블록은 `if`, `for`, `while` 문과 해당 `end` 문(예: `elif`, `else` 또는 `break`) 사이의 코드입니다.

예시:

```python
fruits = ['apple', 'banana', 'cherry']
for fruit in fruits:
    if fruit == 'banana':
        print("Found banana!")
        break
    print(fruit)
else:
    print("All fruits have been checked")
```

이 코드에서 `if` 문과 `for` 루프 안에 있는 두 개의 프린트 함수는 들여씁니다. 이는 `for` 루프에 속하며 루프가 실행될 때마다 실행된다는 것을 나타냅니다. 들여쓰기되지 않은 다른 문도 `for` 루프에 속하지만 루프가 정상적으로 종료될 때(즉, 브레이크 문에 의해 중단되지 않을 때)에만 실행됩니다.

들여쓰기는 파이썬 구문의 핵심 요소이며 함께 속한 코드 블록을 표시하는 데 사용합니다. 들여쓰기를 일관되게 사용하고 코드를 명확하게 구성하는 데 사용하는 것이 중요합니다.

## 중첩 루프(Nested Loops)

루프 내에서 작업을 여러 번 반복하기 위해 다른 루프를 넣을 수 있습니다. 예를 들어 중첩 루프를 사용하여 구구단을 출력할 수 있습니다.

```python
for i in range(1, 11):
    for j in range(1, 11):
        print(i * j, end="\t")
    print()
```

조건문과 루프를 사용하면 많은 문제를 해결할 수 있는 복잡한 프로그램을 만들 수 있습니다.

