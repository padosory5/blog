---
layout: post
title: 리눅스 명령어
tags: [test, blog]
image: '/images/linux-logo.png'
---
# 리눅스에서 자주 사용하는 명령어
## 모든 명령어는 명령어 뒤에 –help 옵션을 주면 자세한 사용 방법이 나온다.
* * *
## pwd
현재 작업중인 디렉토리 정보 출력
```
/Users/youngjune/Projects/blog
```
* * *
## cd
경로 이동 (change directory)
```
Youngjunes-MacBook-Pro:~ youngjune$
```
## ls
디렉토리 목록 확인
```
2Dgame
Adlm
Ai project
Applications
Creative Cloud Files
Desktop
Documents
Downloads
Library
```
## cp (copy)
파일 혹은 디렉토리를 복사 디렉토리를 복사할때는 -r 옵션을 주어야함
```
$ ls
testdir/  testfile


$ cp testfile1 testfile_cp
$ ls
testdir/  testfile  testfile_cp
```
```
$ ls
testdir/  testfile  testfile_cp


$ cp -r testdir testdir_cp
$ ls
testdir/  testdir_cp/  testfile  testfile_cp
```
## mv (move)
파일 혹은 디렉토리 이동 실제로 원하는 위치로 이동할때도 사용하지만, 이름을 변경하는 용도로도 사용한다.
```
$ mv testfile testfile_mv
```
## mkdir (make directory)
디렉토리 생성 -p 옵션을 주면 하위 디렉토리까지 한 번에 생성 가능
```
$ mkdir testdir
```
```
$ mkdir -p a/b/c/d/e/
```
rm (remove) 파일이나 디렉토리를 삭제 디렉토리를 삭제할때는 r 옵션을 주어야 한다. -f 옵션을 주면 사용자에게 삭제 여부를 묻지 않고 바로 삭제한다.
```
$ rm -f testfile1
```
```
$ rm -rf testdir/
```
출처 : https://taein0910.github.io/blog/2020-01-05/linux-note/



