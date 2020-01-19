---
layout: post
title: Git 명령어
tags: [test, blog]
image: '/images/git_logo.png'
---
## 새로운 저장소 만들기
폴더를 하나 만들고 그아래 다음과 같은 명령어를 실행시켜주면 된다
```
git init
```
## 추가와 확정(commit)
변경된 파일은 아래 명령어로 (인덱스에) 추가할 수 있다.
```
git add <파일 이름>
```
```
git add .
```
변경 내용을 확정하려면 아래 명령을 내려야 한다.
```
git commit -m "이번 확정본에 대한 설명"
```
이렇게만 변경해주면 파일은 HEAD 에 반영된다
## 변경 내용 발행(push)하기
현재 변경 내용은 아직 HEAD 에 있다
이제 변경 내용을 서버에 올리려면 다음과 같은 명령어를 실행 시켜줘야한다
```
git push origin master
```
만약 기존에 있던 원격 저장소를 복제한 것이 아니라면, 원격 서버의 주소를 git에게 알려줘야 한다.
```
git remote add origin <원격 서버 주소>
```
이제 변경 내용을 원격 서버로 발행할 수 있다.
