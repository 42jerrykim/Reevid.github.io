---
title: "[Shell] 리눅스 zip, tar, tar.gz 파일 압축 & 풀기"
categories:
  - Shell
tags:
  - Shell
  - zip
  - unzip
  - tar
  - tar.gz
---

# zip 압축하기

## 명령어

```bash
zip {압축 파일명}.zip {압축할 파일 혹은 디렉토리1} {압축할 파일 혹은 디렉토리2}...
```

## 파일 압축하기

특정 디렉토리에 모든 파일(./*)를 test.zip으로 압축한다.

```bash
zip test.zip ./*
```
## 파일 및 디렉토리 압축하기

현재 폴더에 여러 하위 폴더가 있는데, 그것도 다 같이 압축하기 위해서는 -r 이라는 옵션을 추가한다.
특정 디렉토리에 모든 파일 및 디렉토리(./*)를 test.zip으로 압축한다.

```
zip -r test.zip ./*
```

# zip 압축풀기

zip파일을 압축을 푸는 명령어는 아래와 같다.

## 명령어

```bash
unzip {압축 파일명}.zip
```

## 파일 압축풀기

test.zip 파일의 압축을 푸는 명령어는 아래와 같다.

```bash
unzip test.zip
```

## 특정 디렉토리에 파일 압축풀기

test.zip 파일을 /home/devkuma 디렉토리에 압축을 푸는 명령어는 아래와 같다.

```bash
unzip test.zip -d /home/temp 
```

# tar 압축 하기

## 명령어

# tar 압축 풀기
# tar.gz 압축 하기
# tar.gz 압축 풀기

