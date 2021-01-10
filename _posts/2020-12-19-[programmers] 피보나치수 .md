---
title: "[Programmers] 피보나치수"
date: 2020-12-19T18:31:46+09:00
draft: false
description: "[Programmers] 피보나치수"
tags: [Programmers Algorithm]
categories: [Programmers Algorithm]
toc : true
toc_sticky : true
toc_label : 목차
---
## 문제
피보나치 수는 F(0) = 0, F(1) = 1일 때, 1 이상의 n에 대하여 F(n) = F(n-1) + F(n-2) 가 적용되는 수 입니다.

예를들어

   > ▶ F(2) = F(0) + F(1) = 0 + 1 = 1

   > ▶ F(3) = F(1) + F(2) = 1 + 1 = 2

   > ▶ F(4) = F(2) + F(3) = 1 + 2 = 3

   > ▶ F(5) = F(3) + F(4) = 2 + 3 = 5
   
와 같이 이어집니다.

2 이상의 n이 입력되었을 때, n번째 피보나치 수를 1234567으로 나눈 나머지를 리턴하는 함수, solution을 완성해 주세요.

## 제한 사항
   > ▶ n은 1이상, 100000이하인 자연수입니다.

## 입출력 예 설명
   > ▶ 피보나치수는 0번째부터 0, 1, 1, 2, 3, 5, ... 와 같이 이어집니다.

## 소스 코드

<details>
<summary>소스코드</summary>
<div markdown="1">

```java
#include <stdio.h>
#include <stdbool.h>
#include <stdlib.h>

int solution(int n) {
    int answer = 0;
    int a = 0;
    int b = 1;
    for(int i = 0; i<n; i++){
        int c = (a+b)%1234567;
        a = b%1234567;
        b = c%1234567;
    }
    return a;
}
```
</div>
</details>
