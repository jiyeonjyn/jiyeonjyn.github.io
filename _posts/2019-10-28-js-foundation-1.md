---
title: [JavaScript] 기초 1
date: 2019-10-28
categories:
- JavaScript
tags:
- JavaScript
---

## 자바스크립트(JavaScript)
- 구성요소: 변수, 함수, 조건문, 반복문
- 변수와 함수는 window의 속성을 정의하는 것과 같다.<br><br>
- 배열
    - var array = [];
        - ex) var arr = [1, 2, 3];
    - var array = new Array();
        - ex) var arr = new Array(1, 2, 3);
    - a.push(1); a.push(2);로 값 넣음 or a[0]=1, a[1]=2로 넣는 것도 가능
    - 넣은 순서대로 0부터 index 지정됨(0,1,2,3,~)
    - arr[index]로 추출 가능<br><br>
- 객체
    - var object = {};
        - ex) var obj = {a:1, b:2, c:3};
    - object.key = value;로 값 넣음
    - key는 자유롭게 설정 가능, 따옴표 안 써도 됨, 숫자가 먼저 오면 안 됨
    - a.key vs. a['key']
    - a.변수 vs. a['변수'] : a.변수는 '변수'라는 문자열을 가진 속성의 속성값을 찾음, a.['변수']는 변수의 값으로 변환되어 var 변수 = c 라면 a.[c]값을 찾음<br><br>
- 속성 판별 함수
  - typeof() = number(숫자), string(문자), boolean(논리)<br><br>
- 문자열 자르기
    - substring(처음index,끝index)
    - substr(처음index,문자개수)
        - ex)뒤에서 두 글자: substr(-2,2)<br><br>
- parseInt() : 정수화(괄호 안 값보다 작은 정수 중 가장 가까운 정수 값)
- parseFloat() : 실수화<br><br>
- 문자열 숫자로 변환하기 : parseInt(), parseFloat(), Number()<br><br>
-  Escape Character 
   - `\'` : 작은따옴표, `\"` : 큰따옴표
   - \n : 줄바꿈
   - " '' " 가능, ' "" ' 가능
   - `\\` : 역슬래쉬 표현<br><br>
- 연산자 a++은 우선순위 낮음, 가장 나중에 실행됨<br><br>
- Math Methods
  - Math.pow(밑,지수)
  - Math.sqrt(cc) : cc의 (2)제곱근 (루트 cc)
  - Math.random() : 0~1사이의 임의의 수
  - Math.random(100) : 0~100사이의 임의의 수
  - Math.abs(숫자) : 절댓값
      - ex) Math.abs(-5) = 5