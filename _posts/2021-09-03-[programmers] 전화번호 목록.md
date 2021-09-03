---
title: "[Programmers] 전화번호 목록"
date: 2021-09-03T18:31:46+09:00
draft: false
description: "[Programmers] 전화번호 목록"
tags: [Programmers Algorithm]
categories: [Programmers Algorithm]
toc : true
toc_sticky : true
toc_label : 목차
---
## 문제
전화번호부에 적힌 전화번호 중, 한 번호가 다른 번호의 접두어인 경우가 있는지 확인하려 합니다.
전화번호가 다음과 같을 경우, 구조대 전화번호는 영석이의 전화번호의 접두사입니다.

    구조대 : 119
    박준영 : 97 674 223
    지영석 : 11 9552 4421

전화번호부에 적힌 전화번호를 담은 배열 phone_book 이 solution 함수의 매개변수로 주어질 때, 어떤 번호가 다른 번호의 접두어인 경우가 있으면 false를 그렇지 않으면 true를 return 하도록 solution 함수를 작성해주세요.


## 제한 사항

  * ▶ phone_book의 길이는 1 이상 1,000,000 이하입니다. 

        * ▶  각 전화번호의 길이는 1 이상 20 이하입니다.

        * ▶  같은 전화번호가 중복해서 들어있지 않습니다.



## 입출력 예

|phone_book|return|
|:-----------:|:-----------:|
|["119", "97674223", "1195524421"]|false|
|["123","456","789"]|true|
|["12","123","1235","567","88"]|false|

## 입출력 예 설명

### 입출력 예 #1
앞에서 설명한 예와 같습니다.

### 입출력 예 #2
한 번호가 다른 번호의 접두사인 경우가 없으므로, 답은 true입니다.

### 입출력 예 #3
첫 번째 전화번호, “12”가 두 번째 전화번호 “123”의 접두사입니다. 따라서 답은 false입니다.

## 소스 코드

<details>
<summary>소스코드</summary>
<div markdown="1">

```python
def solution(phone_book):
    answer = True
    phone_book_hash = {}
    for numbers in phone_book:
        phone_book_hash[numbers] = 1
    for numbers in phone_book:
        check = ''
        for number in numbers:
            check += number
            if check in phone_book_hash and check != numbers:
                answer = False
    return answer
```
</div>
</details>