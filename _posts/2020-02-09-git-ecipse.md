---
layout: post
title: Git Eclipse 연동
tags: [test, blog]
image: '/images/Webp.net-resizeimage.jpg'
---

## 첫번째
위에 window 를 누른 다음에 Perspective -> open perspective -> other...
Other 에 들어가면 Git 을 찾아서 누르면 된다

<img src="/images/git1.jpg">

## 두번째
Git 에 들어가면 3가지 항목이 뜨는데 그중에서 Clone a Git repository 을 누르면 된다
Clone a Git repository 를 누르면 2가지 항목이 뜨는데 그중에서 Clone URI 를 누르면 된다
## 세번째
개인의 git URI 를 입력해 준 다음에 자신의 아이디랑 비밀번호를 입력후 Next 를 누르면 된다
그후 기본 brnach 인 master 를 눌러주고 Next 를 눌러준다.
## 네번째
깃이 연동될 디렉토리를 입력해준 다음 commit 을 하고 git 에 push 하여 다시 한번 업데이트를 해준다
다 됬으면 finish 를 눌러준다
## 다섯번째
깃세팅이 다 되었으니 자신이 업로드 할 프로젝트를 오른쪽 클릭 하여 team -> share project 를 해준다.
local 저장소를 선택하고 간단히 finish 를 누르면 동기화가 된다
하지만, 실제로 git에 올라간것이 아니기 때문에 commit 을 해주고 update 를 해줘야한다
## 여섯번째
프로젝트를 오른쪽 클릭하고 team -> Add to index 를 눌러준다음 똑같이 team -> commit 을 해준다
commit을 할때 메세지도 같이 달아줘야한다. commit 을 해준후 commit and push 를 해주면 Github에 올라가게 된다. 