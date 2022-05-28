---
title: "[Pytorch] pytorch 기초 _1"
date: 2022-05-29T02:31:46+09:00
draft: false
description: "[Pytorch] pytorch 기초 _1"
tags: [Pytorch]
categories: [Pytorch]
toc : true
toc_sticky : true
toc_label : 목차
---

## [Pytorch] pytorch 기초 _1

### 텐서(TENSOR)?
텐서(tensor)는 배열(array)이나 행렬(matrix)과 매우 유사한 특수한 자료구조입니다. PyTorch에서는 텐서를 사용하여 모델의 입력(input)과 출력(output), 그리고 모델의 매개변수들을 부호화(encode)합니다.

텐서는 GPU나 다른 하드웨어 가속기에서 실행할 수 있다는 점만 제외하면 NumPy 의 ndarray와 유사합니다. 실제로 텐서와 NumPy 배열(array)은 종종 동일한 내부(underly) 메모리를 공유할 수 있어 데이터를 복수할 필요가 없습니다.
텐서는 또한 자동 미분(automatic differentiation)에 최적화되어 있습니다.

## import 방법

<details>
<summary>import 방법</summary>
<div markdown="1">

```python
import torch
import numpy as np
```
</div>
</details>

### 텐서(tensor) 초기화
텐서는 여러가지 방법으로 초기화할 수 있습니다.

#### 데이터로부터 직접(directly) 생성하기

데이터로부터 직접 텐서를 생성할 수 있습니다. 데이터의 자료형(data type)은 자동으로 유추합니다.

<details>
<div markdown="1">

```python
data = [[1, 2],[3, 4]]
x_data = torch.tensor(data)

```
</div>
</details>


#### NumPy 배열로부터 생성하기

텐서는 NumPy 배열로 생성할 수 있습니다.

<details>
<div markdown="1">

```python
np_array = np.array(data)
x_np = torch.from_numpy(np_array)
```

</div>
</details>


#### 다른 텐서로부터 생성하기

명시적으로 재정의(override)하지 않는다면, 인자로 주어진 텐서의 속성(모양(shape), 자료형(datatype))을 유지합니다.

<details>
<div markdown="1">

```python
x_ones = torch.ones_like(x_data) # x_data의 속성을 유지합니다.
print(f"Ones Tensor: \n {x_ones} \n")

x_rand = torch.rand_like(x_data, dtype=torch.float) # x_data의 속성을 덮어씁니다.
print(f"Random Tensor: \n {x_rand} \n")
```

#### Out:
```python

Ones Tensor:
 tensor([[1, 1],
        [1, 1]])

Random Tensor:
 tensor([[0.0965, 0.2738],
        [0.9675, 0.2934]])
```
</div>
</details>

#### 무작위(random) 또는 상수(constant) 값을 사용하기

shape 은 텐서의 차원(dimension)을 나타내는 튜플(tuple)로, 아래 함수들에서는 출력 텐서의 차원을 결정합니다.

<details>
<div>

```python
shape = (2,3,)
rand_tensor = torch.rand(shape)
ones_tensor = torch.ones(shape)
zeros_tensor = torch.zeros(shape)

print(f"Random Tensor: \n {rand_tensor} \n")
print(f"Ones Tensor: \n {ones_tensor} \n")
print(f"Zeros Tensor: \n {zeros_tensor}")
```

#### Out:
```python
Random Tensor:
 tensor([[0.8398, 0.8787, 0.4099],
        [0.6517, 0.2316, 0.1294]])

Ones Tensor:
 tensor([[1., 1., 1.],
        [1., 1., 1.]])

Zeros Tensor:
 tensor([[0., 0., 0.],
        [0., 0., 0.]])
```
</div>
</details>