---
layout: post
title: Omok 2
tags: [test, blog]
image: '/images/java-logo.png'
---
## 오목 만들기
두가지 방법으로 오목을 만들수가 있다.
<img src="/blog/images/omok-1.png">

콘솔창으로는 3가지 클래스를 만들어준다

### 오목 인터페이스 
```
package Omokk;

public interface Omokinterface {
	  public void viewOmok();
	  public int OmokAction(char x, int y, int turn);
}
```

### 오목 Impl
```
import java.util.Scanner;

public class OmokImpl {
	public static void main(String[] args) {
		
		int gameState = 0; 		
    		// 게임의 상태를 알려주는 변수
    
		int turn = 0; 			
    		// 누구턴인지 알려주는 변수
    
		char x = '\u0000'; 		
    		// x축 입력받는 변수
    
		int y = 0; 				
    		// y축 입력받는 변수
		
		Omokview o = new Omokview(); 
		
		Scanner sc = new Scanner(System.in);
		
		// 사용자의 좌표 입력 받는 메소드
		while(gameState == 0) {
			o.viewOmok();		
      			// 오폭판을 출력합니다.
			
			System.out.println("x 좌표를 입력하세요.");
			x = sc.next().charAt(0);
			System.out.println("y 좌표를 입력하세요.");
			y = sc.nextInt();
			
			turn = (turn == 1) ? 2 : 1;
			// 턴제를 바꿔주는 조건문
			
			gameState = o.OmokAction(x, y, turn);
		}
		
		o.viewOmok();			
    		// 최종 오목판을 출력합니다.
		System.out.println("게임이 끝났습니다.");
		sc.close();
	}
}
```

### 오목 뷰
```
import java.util.Scanner;

public class OmokImpl {
	public static void main(String[] args) {
		
		int gameState = 0; 		
    		// 게임의 상태를 알려주는 변수
    
		int turn = 0; 			
    		// 누구턴인지 알려주는 변수
    
		char x = '\u0000'; 		
    		// x축 입력받는 변수
    
		int y = 0; 				
    		// y축 입력받는 변수
		
		Omokview o = new Omokview(); 
		
		Scanner sc = new Scanner(System.in);
		
		// 사용자의 좌표 입력 받는 메소드
		while(gameState == 0) {
			o.viewOmok();		
      			// 오폭판을 출력합니다.
			
			System.out.println("x 좌표를 입력하세요.");
			x = sc.next().charAt(0);
			System.out.println("y 좌표를 입력하세요.");
			y = sc.nextInt();
			
			turn = (turn == 1) ? 2 : 1;
			// 턴제를 바꿔주는 조건문
			
			gameState = o.OmokAction(x, y, turn);
		}
		
		o.viewOmok();			
    		// 최종 오목판을 출력합니다.
		System.out.println("게임이 끝났습니다.");
		sc.close();
	}
}
```

위와 같이 만들어 줬으면 콘솔 창으로 확인할수 있다.

### 콘솔 창으로해서 보기
<img src="/blog/images/omok-2.png">
콘솔 창으로 x값과 y값을 작성해주면서 오목판에 오목을 두는 방법