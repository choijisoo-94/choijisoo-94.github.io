---
title: "[linux] 리눅스 IO Redirection - append"
date: 2021-06-14T13:31:46+09:00
draft: false
description: "[linux] 리눅스 IO Redirection - append"
tags: [linux]
categories: [linux]
toc : true
toc_sticky : true
toc_label : 목차
---

# IO Redirection
## - append

> 1번

- firstdir 이라는 디렉토리 안의 항목을 체크함

```linux
websquare@websquare-virtual-machine:~/firstdir$ ls -al
합계 20
drwxrwxr-x  2 websquare websquare 4096  6월 14 14:38 .
drwxr-xr-x 18 websquare websquare 4096  6월 14 14:37 ..
-rw-rw-r--  1 websquare websquare    7  6월 14 14:09 hello.txt
-rw-rw-r--  1 websquare websquare    7  6월 14 14:31 one.txt
-rw-rw-r--  1 websquare websquare  942  6월 14 14:39 result.txt

```

>2번

- firstdir 목록을 result.txt라는 파일을 만들어 저장함

```linux
websquare@websquare-virtual-machine:~/firstdir$ ls -al > result.txt
websquare@websquare-virtual-machine:~/firstdir$ ls -al
합계 20
drwxrwxr-x  2 websquare websquare 4096  6월 14 15:15 .
drwxr-xr-x 18 websquare websquare 4096  6월 14 14:37 ..
-rw-rw-r--  1 websquare websquare    7  6월 14 14:09 hello.txt
-rw-rw-r--  1 websquare websquare    7  6월 14 14:31 one.txt
-rw-rw-r--  1 websquare websquare  314  6월 14 15:15 result.txt

```

>3번

- result.txt 안에 ls -al 을 한번 더, 같은 result.txt 파일에 저장

```linux
websquare@websquare-virtual-machine:~/firstdir$ ls -al >> result.txt
websquare@websquare-virtual-machine:~/firstdir$ cat result.txt
합계 16
drwxrwxr-x  2 websquare websquare 4096  6월 14 15:15 .
drwxr-xr-x 18 websquare websquare 4096  6월 14 14:37 ..
-rw-rw-r--  1 websquare websquare    7  6월 14 14:09 hello.txt
-rw-rw-r--  1 websquare websquare    7  6월 14 14:31 one.txt
-rw-rw-r--  1 websquare websquare    0  6월 14 15:15 result.txt
합계 20
drwxrwxr-x  2 websquare websquare 4096  6월 14 15:15 .
drwxr-xr-x 18 websquare websquare 4096  6월 14 14:37 ..
-rw-rw-r--  1 websquare websquare    7  6월 14 14:09 hello.txt
-rw-rw-r--  1 websquare websquare    7  6월 14 14:31 one.txt
-rw-rw-r--  1 websquare websquare  314  6월 14 15:15 result.txt

```

### 핵심 내용

1) 꺽쇠가 두개 (>>) 이면 기존의 파일에 내용을 더한다.

2) 꺽쇠가 반대로 두개(<<) 이면 입력을 하나로 합친다.