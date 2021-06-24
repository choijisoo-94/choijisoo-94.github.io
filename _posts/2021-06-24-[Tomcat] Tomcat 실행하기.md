---
title: "[Tomcat] TOMCAT9 실행하기(1)"
date: 2021-06-24T13:31:46+09:00
draft: false
description: "[Tomcat] TOMCAT9 실행하기(1)"
tags: [Tomcat]
categories: [Tomcat]
toc : true
toc_sticky : true
toc_label : 목차
---

## Tomcat9 실행하기(1)

1. 우선 tomcat 사이트에 접속합니다.

[tomcat](http://tomcat.apache.org)

2. 좌측에 사이드바에 Download 란을 확인합니다.

![제목 없음](https://user-images.githubusercontent.com/73863771/123202552-bee6c880-d4ef-11eb-9246-a15eced29cf5.png)


3. 원하는 tomcat 버전을 선택하고 Binary Distributions 를 확인합니다.

![제목 없음1](https://user-images.githubusercontent.com/73863771/123202723-18e78e00-d4f0-11eb-94ef-5aa0e5fe38a8.png)

4. 자신의 컴퓨터 OS에 따라 자유롭게 선택합니다.

- WINDOW 버전은 편하게 **32-bit/64-bit Windows Service Installer (pgp, sha512)** 를 선택해줍니다.

- LINUX 버전은 **tar.gz (pgp, sha512)** 를 선택해줍니다.

5. 다운이 끝나면 압축 풀기 도구를 통하여 압축을 풀어줍니다.

6. 설치 시 아래와 같은 화면이 뜰 때까지 Next 눌러줍니다.

![26473749586E66E81A](https://user-images.githubusercontent.com/73863771/123202898-754aad80-d4f0-11eb-8bd8-5f32229978fc.png)

7. http 포트는 서버에 접속할 때에 필요한 포트 번호입니다. 본인 pc 에서 사용할 번호이니 편한 번호로 사용자 지정해줍니다.

8. jdk 파일이 필요합니다. jdk를 설치합니다.

(※경로는 한글이 들어가지 않게 해주세요.)

9. 설치(install) 버튼을 눌러 설치해 줍니다.

![223FB249586E67B527](https://user-images.githubusercontent.com/73863771/123203219-f86c0380-d4f0-11eb-9c31-beb30b2344cd.png)

10. 설치가 완료되면 아래 화면이 뜨고 finish 버튼 눌러 줍니다.

![223FB249586E67B527](https://user-images.githubusercontent.com/73863771/123203327-24878480-d4f1-11eb-98ba-4246d6795588.png)