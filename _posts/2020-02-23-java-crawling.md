---
layout: post
title: Java Crawling
tags: [test, blog]
image: '/images/java-logo.png'
---
## Crawling
웹 사이트에 출력되어 있는 데이터들을 가져오는 것이다.
### 준비 방법
밑에 있는 사이트 에서 가장 첫번째 jsoup-1.12.2.jar core library 를 다운해준다
https://jsoup.org/download

그다음 자신의 프로젝트를 우클릭을 해 properties 로 들어간다

그렇게 하면 libraries 가 뜨는데 거기로 들어가 add externals JAR 를 눌러 파일을 가져온다
그런 다음 apply and close 를 눌러 apply 를 해준다

그렇게 해준다음 밑에 있는 코드를 작성해준다

```
package Lecture20200223;

import java.io.IOException;

import org.jsoup.Jsoup;
import org.jsoup.nodes.Document;
import org.jsoup.nodes.Element;
import org.jsoup.select.Elements;

public class CrawlingTest {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		String url = "https://news.naver.com/main/list.nhn?mode=LSD&mid=sec&sid1=001";
		Document doc = null;
		
		try {
			doc = Jsoup.connect(url).get();
		}catch(IOException e) {
			e.printStackTrace();
		}
		
		Elements element = doc.select("div.list_body");
		//1. 필요한부분 텍스트를 가져온다.
		String title = element.select("a").text();
		System.out.println("====================================");
		System.out.println(title);
		System.out.println("====================================");
		
		for(Element el : element.select("li")) { // 하위 웹툰 제목들을 for 문을 통해 가져온
			System.out.println(el.text());
		}
	}

}
```
코드에서 string url 에는 현재 웹 주소를 붙여준다
Elements element = doc.select("class"); class 에는 class 를 찾아 써준다
String title = element.select("a").text(); text type 을 알아내서 써줘야한다