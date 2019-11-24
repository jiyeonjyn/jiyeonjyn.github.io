---
title: "[JavaScript] 기초 2"
date: 2019-10-29
categories:
    - JavaScript
tags:
    - JavaScript
---

## 자바스크립트(JavaScript)

-   함수로 값을 넘겨주는 방식
    -   call by value : 값을 복사해서 전달하는 방식, 원래 변수의 값은 변하지 않음
    -   call by reference : 주소값을 전달하는 방식, 함수 안에서 값이 변하면 원래 변수의 값도 변함
        -   ex) var a = {key='value1'}일 때,
        -   함수 내에서 a.key = value2로 바꿨을 때 객체의 key 값도 value2로 바뀐다.
        -   var b = a 일 때, b.key = value3로 바꿨을 때 a의 key 값도 value3로 바뀐다.<br><br>
-   전역변수/지역변수 -> 함수의 매개변수는 지역변수이다.<br><br>
-   var a = function() {}; vs. function a() {}
    -   function a() {}는 hoisting(끌어올리기)이 가능 -> 함수 정의하기 전 실행 가능
    -   var a = function() {}; -> 이 형식은 예외적으로 뒤에 세미콜론을 붙인다.<br><br>
-   연산자 == vs. ===(데이터 형도 같음)
    -   1=="1" -> true
    -   1==="1" -> false<br><br>
-   if

```javascript
if (조건1) {
    결과;
} else if (조건2) {
    결과;
} else {
    결과;
}
```

-   switch

```javascript
switch (변수) {
    case 값1:
    case 값2:
        결과;
        break;
    case 값3:
        결과;
        break;
    case 값4:
    case 값5:
    case 값6:
        결과;
}
```

-   while

```javascript
1.초기화식
while (2.조건식) {
    실행문;
    3.증감식;
}
```

-   for

```javascript
for (1.초기화식; 2.조건식; 3.증감식) {
    실행문;
}
```

-   do while

```javascript
1.초기화식
do {
    실행문; //적어도 한 번 실행됨
    3.증감식;
} while (2.조건식)
```

-   조건식을 쓸 때는 == or === 사용!!!
-   반복문 안에 `if (조건) { continue; }`를 넣으면 그 조건에 해당할 때는 건너뛰고 실행된다.
-   반복문 안에 `if (조건) { break; }`를 넣으면 그 조건에 해당할 때 반복문을 탈출한다.
