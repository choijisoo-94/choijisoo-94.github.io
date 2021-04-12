---
title: "[project] datetimepicker 기본값으로 만들어주기"
date: 2021-03-31T21:31:46+09:00
draft: false
description: "[project] datetimepicker 기본값으로 만들어주기"
tags: [project]
categories: [project]
toc: true
toc_sticky: true
toc_label: 목차
---

## Educare 프로젝트

### datetimepicker

- datetime 을 넣는 vue.js 의 views 화면단의 addTest.vue 안에서 데이터가 none으로 들어갔다.

- 데이터 형식이 맞지 않아서 이것을 고치기 위해서 여러 시도를 했다.

- 2021-03-31T21:31:46 -> 이러한 형식을 갖추어야 mysql 의 저장소에 들어갈 수 있었다.

- buefy의 datetimepicker 들은 대부분 분 단위까지만 나왔고, 형식과 맞지 않았다.

- 구글링을 통해 로컬 표준시간대의 날짜 시간 형식으로 저장시켜주는 하이브리드 npm 패키지를 발견하였다.

- vscode 의 현재 협업하는 경로로 설정한다.(bash로 하는 것을 추천!)

- 그 후 npm i local-iso-dt 를 친다.

- 설치가 진행되어 완료되면 사용하고자 하는 addTest.vue 안에 import 해 준다.

- import { localISOdt } from 'local-iso-dt'

- 그 후에 vue.js의 문법에 따라 return 값 안에 localISOdt 을 추가해준다.

- 사용하고자 하는 datetimepicker에 localISOdt: "localISOdt"을 추가해준다.

- 정상적으로 mysql DB에 저장되는 것을 확인할 수 있다.
