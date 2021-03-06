---
title: "[Vanilla JS] Vanilla JS 변수"
date: 2021-05-15T08:31:46+09:00
draft: false
description: "[Vanilla JS] Vanilla JS 변수"
categories: [Vanilla JS]
toc_sticky: true
toc_label: 목차
---
## var let const의 차이점

1. var는 함수 레벨 스코프이고 let, const는 블럭 레벨 스코프입니다.
2. var로 선언한 변수는 선언 전에 사용해도 에러가 나지 않지만 let, const는 에러가 발생합니다.
3. var는 이미 선언되어있는 이름과 같은 이름으로 변수를 또 선언해도 에러가 나지 않지만 let, const는 이미 존재하는 변수와 같은 이름의 변수를 또 선언하면 에러가 납니다.
4. var, let은 변수 선언시 초기 값을 주지 않아도 되지만 const는 반드시 초기값을 할당해야 합니다.
5. var, let은 값을 다시 할당할 수 있지만 const는 한번 할당한 값은 변경할 수 없습니다(단, 객체 안에 프로퍼티가 변경되는 것까지 막지는 못합니다).

## var 예시

```javascript
console.log(num);
var num;  //undefined
```

## let 예시

- let은 변수가 바뀔 수 있지만 const는 변수가 정해진 순간 바뀔 수 없다.

```javascript
console.log(num); // Uncaught ReferenceError: num is not defined
let num = 1;
console.log(num); //1


let num; //undefined
console.log(num); //undefined
num = 1; //1
console.log(num) //1
```

## const 예시

```javascript
const obj = { first: 1 };
// 에러 발생
obj = 1; // Uncaught TypeError: Assignment to constant variable.

// 에러 발생하지 않음.
obj.first = 2;
obj.second = 2;
delete obj.first;
```

