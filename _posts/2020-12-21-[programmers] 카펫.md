---
title: "[Programmers] 카펫"
date: 2020-12-25T18:31:46+09:00
draft: false
description: "[Programmers] 카펫"
tags: [알고리즘]
categories: [알고리즘]
toc : true
toc_sticky : true
toc_label : 목차
---
## 문제
Leo는 카펫을 사러 갔다가 아래 그림과 같이 중앙에는 노란색으로 칠해져 있고 테두리 1줄은 갈색으로 칠해져 있는 격자 모양 카펫을 봤습니다.

## 카펫 그림 예시
![carpet](https://user-images.githubusercontent.com/73863771/103135860-e276b500-46fe-11eb-8830-b555644cd3be.png)

Leo는 집으로 돌아와서 아까 본 카펫의 노란색과 갈색으로 색칠된 격자의 개수는 기억했지만, 전체 카펫의 크기는 기억하지 못했습니다.

Leo가 본 카펫에서 갈색 격자의 수 brown, 노란색 격자의 수 yellow가 매개변수로 주어질 때 카펫의 가로, 세로 크기를 순서대로 배열에 담아 return 하도록 solution 함수를 작성해주세요.

## 제한사항
    ▶ 갈색 격자의 수 brown은 8 이상 5,000 이하인 자연수입니다.
    ▶ 노란색 격자의 수 yellow는 1 이상 2,000,000 이하인 자연수입니다.
    ▶ 카펫의 가로 길이는 세로 길이와 같거나, 세로 길이보다 깁니다.

```java
import java.util.*;
 
class Solution {
    public int[] solution(int brown, int yellow) {
        int[] answer = new int[2];
        int sum = (brown + 4) / 2; // 가로와 세로의 합.
        int m = 3; // 세로
        int n = sum - m; // 가로
        
        // 노란색 칸이 최소 1개이기때문에 n은 3이상이어야 함.
        // 문제에서 가로 길이는 세로 길이보다 크거나 같다고 명시되어 있음.
        while(n >= 3 && n >= m) {
            // (가로 - 2) * (세로 - 2)는 노란색 칸의 개수와 같음.
            if((n - 2) * (m - 2) == yellow){
                answer[0] = n;
                answer[1] = m;
                break;
            }
            
            n--; m++;
        }
        
        return answer;
    }
}
```