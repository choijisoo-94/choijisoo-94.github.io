---
title: "[Programmers] N개의 최소공배수"
date: 2020-12-21T18:31:46+09:00
draft: false
description: "[Programmers] N개의 최소공배수"
tags: [Programmers Algorithm]
categories: [Programmers Algorithm]
toc : true
toc_sticky : true
toc_label : 목차
---
## 문제
두 수의 최소공배수(Least Common Multiple)란 입력된 두 수의 배수 중 공통이 되는 가장 작은 숫자를 의미합니다. 예를 들어 2와 7의 최소공배수는 14가 됩니다. 정의를 확장해서, n개의 수의 최소공배수는 n 개의 수들의 배수 중 공통이 되는 가장 작은 숫자가 됩니다. n개의 숫자를 담은 배열 arr이 입력되었을 때 이 수들의 최소공배수를 반환하는 함수, solution을 완성해 주세요.

## 제한 사항
   > ▶ arr은 길이 1이상, 15이하인 배열입니다.
   
   > ▶ arr의 원소는 100 이하인 자연수입니다.

## 소스 코드

<details>
<summary>소스코드</summary>
<div markdown="1">

```java
import java.util.Arrays;

class Solution {
    public int solution(int[] arr){
        Arrays.sort(arr);
        int lcm = arr[0] * arr[1] / gcd(arr[0], arr[1]);
        
        for(int i= 2; i<arr.length; i++){
            lcm = lcm * arr[i] / gcd(lcm, arr[i]);
        }
        return lcm;
    }
    public static int gcd(int small, int big){
        while(small != 0){
            int nmg =big % small;
            big = small;
            small = nmg;
        }
        return big;
    }
}
```
</div>
</details>