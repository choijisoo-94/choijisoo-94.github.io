---
title: "[Tomcat] TOMCAT9 실행하기(2)"
date: 2021-06-24T13:31:46+09:00
draft: false
description: "[Tomcat] TOMCAT9 실행하기(2)"
tags: [Tomcat]
categories: [Tomcat]
toc : true
toc_sticky : true
toc_label : 목차
---

## TOMCAT9 실행하기(2)

1. 설치한 경로에 위치한 Tomcat 9.0 폴더로 들어가 보면 아래 화면과 같은 구조가 나옵니다.


![화면 캡처 2021-06-24 134408](https://user-images.githubusercontent.com/73863771/123204074-50573a00-d4f2-11eb-8c08-ca963201f907.png)


2. ./bin 폴더에 들어가서 Tomcat9.exe 혹은 Tomcat9w.exe 실행

	- Tomcat9w.exe는 네트워크 차단을 자동적으로 함


3. ./bin 폴더에 들어가서 startup.bat 파일로 들어가도 됩니다.


![화면 캡처 2021-06-24 134408](https://user-images.githubusercontent.com/73863771/123205146-53ebc080-d4f4-11eb-822c-1b0365a2299e.png)


4. 브라우저로 들어가서 지정한 포트번호로 http://localhost:포트번호 접속하시면 됩니다.


5. 추가적으로 webapp 하단이 배포되는 경로이므로 이 경로 아래로 새 폴더들을 만드시면 됩니다.