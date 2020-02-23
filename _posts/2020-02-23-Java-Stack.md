---
layout: post
title: Java Stack
tags: [test, blog]
image: '/images/java-logo.png'
---
## 스택(stack)
* 데이터를 집어넣을 수 있는 선형(linear) 자료형이다
* 나중에 집어 넣은 데이터가 먼저 나온다.이 특징을 줄여서 LIFO(Last In First Out) 라고 부른다
* 데이터를 집어넣는 push, 데이터를 추출하는 pop, 맨 나중에 집어넣은 데이터를 확인하는 peek등의 작업을 할수 있다

### Java 스택 클래스
자바에서는 Stack 클래스를 따로 지원해줘 이 클래스를 사용해서도 쓸수있다
구현하는 방법은 밑과 같다
```
Stack<Element> stack = new Stack<>();
```
그리고 5가지의함수를 지원해준다 (밑과 같이)
```
public Element push(Element item); // 데이터 추가
public Element pop(); // 최근에 추가된(Top) 데이터 삭제
public Element peek(); // 최근에 추가된(Top) 데이터 조회
public boolean empty(); // stack의 값이 비었는지 확인, 비었으면 true, 아니면 false
public int seach(Object o); // 인자값으로 받은 데이터의 위치 반환, 그림으로 설명하겠음
```
사용 예
```
Stack<Integer> stack = new Stack<>();
        for (int i = 0; i < 5; i++) {
            stack.push(i + 1);
            System.out.println(stack.peek());
        } // 1, 2, 3, 4, 5 가 현재 들어가 있음
        stack.pop(); // 1, 2, 3, 4
        System.out.println(stack.peek()); // 4
        System.out.println(stack.search(1)); // 4
        System.out.println(stack.empty()); // false
```
search는 인덱스를 반환 하는 것이 아니라 순번을 반환 하는 것이다. 즉 search의 인자 값으로 받은 값이 스택구조에서 몇번째에 있는지를 반환하는 것이다

### 사용자 정의 stack 구현
현재 구현해야하는 것은 Top, push, pop, peek 이다. 이것을 배열을 활용해 구현하는 방법이 있다.
```
public class UserArrayStack {

    int top;
    int [] stack;
    int size;

    public UserArrayStack(int size) {
        this.size = size; //
        stack = new int[size];
        top = -1; // top 의 값 초기화
    }

    private void push(int item) {
        stack[++top] = item;
        System.out.println(stack[top] + " push!");
    }

    private void peek() {
        System.out.println(stack[top] + " peek!");
    }

    private void pop() {
        System.out.println(stack[top] + " pop!");
        stack[top--] = 0;
    }

    private int search(int item) {
        for (int i = 0; i <= top; i++) { // for 문은 top 만큼
            if (stack[i] == item)
                return (top - i) + 1; // top - 탐색한 배열의 인덱스, 배열 이므로 +1 추가
        }
        return -1;
    }

    private boolean empty() {
        return size == 0;
    }
}
```
### 배열 구현의 장단점
장점은 구현이 쉽다는것과 데이터 접근 속도가 빠르다는것이다. 하지만 단점은 항상 최대 개수를 정해놔야한다.
