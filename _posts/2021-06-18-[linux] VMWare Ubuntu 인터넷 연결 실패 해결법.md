---
title: "[linux] VMWare Ubuntu 인터넷 연결 실패 해결법"
date: 2021-06-14T13:31:46+09:00
draft: false
description: "[linux] VMWare Ubuntu 인터넷 연결 실패 해결법"
tags: [linux]
categories: [linux]
toc : true
toc_sticky : true
toc_label : 목차
---

## 가상머신(Ubuntu) 인터넷 연결 실패 해결법

1. 가상 머신을 실행한다.

2. 상단 메뉴바의 [VM] -> setting 를 클릭한다.

3. Network 설정을 NET 으로 설정해준다.

4. 터미널을 켜서 하단의 명령어를 입력한다.
```linux
sudo dhclient
```

5. ip 주소를 받아오는지 확인한다.
```linux
ifconfig
```

> **주의!!** 여러 방법을 동원해봐도 인터넷 연결이 되지 않을 때 사용하는 하나의 해결책입니다.