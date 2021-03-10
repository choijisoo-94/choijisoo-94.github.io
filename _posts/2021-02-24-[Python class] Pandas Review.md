---
title: "[Python class] Pandas Review"
date: 2021-03-10T12:31:46+09:00
draft: false
description:  "[Python class] Pandas Review"
tags: [Python class]
categories: [Python class]
toc : true
toc_sticky : true
toc_label : 목차
---
## Review

### 1. Pandas 학습

1. 데이터 분석을 위한 모듈
2. excel과 가장 큰 차이점 : Pandas는 대용량 데이터 처리가 가능
3. 데이터 분석 및 데이터 가공에 절대적으로 사용되는 library
4. 주요 학습 내용
> 1. DataFrame - excel의 다수의 컬럼들을 보유한 table과 동일하다 간주
> 2. series - DataFrame을 구성하는 column 간주

<details>
<summary>import문</summary>
<div markdown="1">
```python
import numpy as np
import pandas as pd
```
</div>
</details>


<details>
<summary>pandas 버전 확인</summary>
<div markdown="1">
```python
pd.__version__
```
</div>
</details>


<details>
<summary>s 선언하기</summary>
<div markdown="1">
```python
s = pd.Series([1, 2, 3])
print(s)
print(type(s))
print(data)
```
</div>
</details>



<details>
<summary>s 출력하기</summary>
<div markdown="1">
```python
print(s.values)  # series  데이터들만 list
print("-"*10)
print(s.index)   # series의 index 정보 확인 
print("-"*10)
print(s.value_counts) 
```
</div>
</details>


<details>
<summary>nn/nan 사용</summary>
<div markdown="1">
```python
# python에서 np/nan등은 결측치 의미 
s = pd.Series([3, 1, 2, 3, 4, np.nan])
print(s)
print("-"*10)
s.value_counts(normalize=True)
s = pd.Series(['a', 'b', 'a', np.nan])
s.value_counts()
```
</div>
</details>


<details>
<summary>정수 데이터 - int64</summary>
<div markdown="1">
```python
s = pd.Series([1, 2])   # 정수 데이터 - int64
print(s)
```
</div>
</details>

