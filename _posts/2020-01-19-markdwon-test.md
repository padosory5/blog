---
layout: post
title: 변수
tags: [test, blog]
image: '/images/java-logo.jpg'
---
변수
=============

다음과 같은 a, b를 변수(variable)라고 한다
```
int a;
String b;
```
## 변수명
변수명은 프로그래머가 원하는대로 이름을 지을수가 있다.
단, 몇가지 규칙이 있다
* 변수명은 숫자로 시작할 수 없다.
* _(underscore) 와 $ 문자 이외의 특수문자는 사용할 수 없다.
* 자바의 키워드는 변수명으로 사용할 수 없다. (예: int, class, return 등)
잘못된 사용 예
```
int 1st;
int a#;
int class;
```
## 자료형
변수명 앞의 int, String 등은 변수의 자료형(Type)을 뜻한다.

int 는 정수값만 담을수 있다
String 은 문자열값만 넣을수 있다
그외에도 많은 자료형들이 있다
```
int
long
double
boolean
char
String
StringBuffer
List
Map
```
## 변수에 값을 대입하기
다음과 같이 변수 선언후 값을 대입할수 있다
```
int a;
String b;

a = 3;
b = "hi"
```
변수에 값을 대입할 때는 위의 예에서와 같이 =(assignment) 기호를 사용한다.

이렇게도 변수를 대입할수도 있다
```
int a = 3;
String b = "hi"
```
만약 int 자료형 변수인 a에 문자열을 대입하면 다음과 같은 에러 메세지가 뜬다
```
Type mismatch: cannot convert from String to int
```
### 사용자 정의 자료형
예를 들어 talk 이라는 클래스를 만들면
```
class talk{
}
````
다음과 같은 자료형을 쓸수있다
```
talk a;
```