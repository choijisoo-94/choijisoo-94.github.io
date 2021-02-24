---
title: "[Python class] 기초문법 Review"
date: 2021-01-28T21:31:46+09:00
draft: false
description:  "[Python class] 기초문법 Review"
tags: [Python class]
categories: [Python class]
toc : true
toc_sticky : true
toc_label : 목차
---
## Review

### 1. 창작 문제
**창작**

- 플레이데이터에서 수업을 듣는 정민, 지수, 희성, 준형, 아정, 종욱은 수업이 끝난 후 저녁을 먹으러 가려고 한다.

- 정민이 피자를 좋아해 다들 피자 가게로 향했다. 

- 피자는 1인당 11000원이다.

- 각자가 가진 금액은 모두 다르다. 아래의 금액은 모두 지출해야 한다. 

- 각자 낸 금액은 아래에 명시되어 있다.

<details>
<summary>각자 낸 금액과 이름</summary>
<div markdown="1">
```python
ourmoney = [('정민', 13000), ('지수', 11000), ('희성', 20000), ('준형', 2000), ('아정', 6000), ('종욱', 18000)]
```
</div>
</details>

#### 문제 1

- 각자가 가진 돈을 모두 합한 금액은?

<details>
<summary>문제 1 코드</summary>
<div markdown="1">
```python
from functools import reduce
data = reduce(lambda x, y: x+y, [13000, 11000, 20000, 2000, 6000, 18000])
print(data)
```
</div>
</details>

#### 답
70000


#### 문제 2

- 피자를 6명이 모두 먹었을 때 나올 금액은?

<details>
<summary>문제 2 코드</summary>
<div markdown="1">
```python
eval('11000 * 6')
```
</div>
</details>

#### 답
66000


#### 문제 3

- 피자를 다 먹고 난 후 6명에게 남은 금액은?

<details>
<summary>문제 3 코드</summary>
<div markdown="1">
```python
from functools import reduce
data = reduce(lambda x, y : x - y, [70000, 66000])
print(data)
```
</div>
</details>

#### 답
4000

#### 문제 4

- 돈을 많이 낸 순으로 리스트 정렬하기

<details>
<summary>문제4 코드</summary>
<div markdown="1">

```python
ourmoney = [('정민', 13000), ('지수', 11000), ('희성', 20000), ('준형', 2000), ('아정', 6000), ('종욱', 18000)]

ourmoney.sort(key = lambda x : x[1], reverse=True)
print('돈을 많이 낸 순서', '\n')

for i, v in enumerate(ourmoney):
    print(i+1, '번째로 많이 낸 사람 :', v[0])
    print('가격 :', v[1], '\n')
```
</div>
</details>

#### 답 
돈을 많이 낸 순서 

1 번째로 많이 낸 사람 : 희성
가격 : 20000 

2 번째로 많이 낸 사람 : 종욱
가격 : 18000 

3 번째로 많이 낸 사람 : 정민
가격 : 13000 

4 번째로 많이 낸 사람 : 지수
가격 : 11000 

5 번째로 많이 낸 사람 : 아정
가격 : 6000 

6 번째로 많이 낸 사람 : 준형
가격 : 2000 

#### 문제 5

- 돈을 11000원 이상 낸 사람 뽑아내기

<details>
<summary>문제 5 코드</summary>
<div markdown="1">

```python
ourmoney = [('정민', 13000), ('지수', 11000), ('희성', 20000), ('준형', 2000), ('아정', 6000), ('종욱', 18000)]

list(filter(lambda x : x[1] >= 11000, ourmoney))
```
</div>
</details>

#### 답
[('정민', 13000), ('지수', 11000), ('희성', 20000), ('종욱', 18000)]