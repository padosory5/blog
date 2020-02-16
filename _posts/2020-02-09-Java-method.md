---
layout: post
title: Java Method
tags: [test, blog]
image: '/images/java-logo.png'
---
## 단일 파라미터 메소드
### 무엇?
입력 변수가 하나만 있는 메소드를, 단일 파라미터 메소드라 합니다. 여기서 파라미터란 입력 변수의 또 다른 표현입니다
```
// 단일 파라미터 메소드 호출 예
int x = square(4); // 입력값: 4 -> 반환값: 16
```

### 파라미터로의 입력 값 대입
메소드 호출 시 입력한 값은 입력 변수 즉, 파라미터로 대입됩니다.
```
//단일 파라미터 메소드 정의 예
publich static int square(int n) {
    int result = n * n; //변수 생성 밑 제곱 값 대입
    return result; // 값 변환
}
```
### 문제
입력값의 세제곱을 반확하는 cube() 메소드를 완성하여, 출력 예와 같은 결과를 얻으시오.

출력 예
```
3의 세제곱 -> 27
```
정답 
```
public class Problem009 {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		int a = 3;
		int x = cube(a);
		System.out.println(a + "의 세제곱 -> " + x);
	}
	public static int cube(int a) {
		int result = a * a * a;
		return result;
	}
}
```

## 다중 파라미터 메소드
### 무엇?
입력 변수가 2개 이상인 경우, 이를 자둥 파라미터 메소드라 합니다.
```
//다중 파라미터 메소드 호출 예
int a = times(3, 4); //12
int b = times(5, 6); //30

파라미터로 입력 값 전달
메소드 호출 시 입력한 값은 차례로 파라미터(입력 변수)에 대입됩니다.
```
//다중 파라미터 메소드 정의 예
public static int times(int a, int b){
    return a * b;
}
