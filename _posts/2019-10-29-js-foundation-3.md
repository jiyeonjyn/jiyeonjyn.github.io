---
title: "[JavaScript] 기초 3"
date: 2019-10-29
categories:
- JavaScript
tags:
- JavaScript
---

## 자바스크립트(JavaScript)
- 자바스크립트로 css 적용하기
```
var a = document.getElementsByTagName('TagName');
var a = document.getElementsByClassName('ClassName');
var a = document.getElementsById('Id');

for ( var i = 0; i < a.length; i++ ) {
    a[i].style.color='red';
}
```
- 제이쿼리로 css 적용하기
```javascript
$('선택자').css('color','red');
```
<br>

- 배열 관련 methods
    - .sort() : 배열을 순서대로 정렬한다.
    - .join() : 배열을 하나의 문자열로 만들어 준다.
    - .slice() : 배열의 일부분의 값을 추출한다.
    - .reverse() : 배열을 역순으로 재정렬한다.
    - .concat() : 두 개의 배열을 하나로 합친다.
    - .split() : 문자열을 배열로 만들어 준다.<br><br>
- .sort()
```javascript
var array = new Array( "ghi", "abc", "def" );
array.sort() = [ "abs", "def", "ghi" ]; -> 배열이 a~z 순서로 정렬됨

var score = [ 4, 11, 2, 10, 3, 1 ];
score.sort() = [ 1, 10, 11, 2, 3, 4 ]; -> 숫자의 크기대로 나오지 않음

score.sort(function(a, b) { 
    return a - b; // 오름차순
}) = [ 1, 2, 3, 4, 10, 11 ];

score.sort(function(a, b) { 
    return b - a; // 내림차순
}) = [ 11, 10, 4, 3, 2, 1 ];
```
- .join()
```javascript
var array = new Array( "ghi", "abc", "def" );

array.join(',') = "ghi,abc,def";
array.join("&") = "ghi&abc&def";
```
- .slice()
```javascript
var array = new Array( "ghi", "abc", "def" );

array.slice(1,3) = [ "abc", "def" ];
```
- .reverse()
```javascript
var array = new Array( "ghi", "abc", "def" );

array.reverse() = [ "def", "abc", "ghi" ];
```
- .concat()
```javascript
var array = new Array( "ghi", "abc", "def" );
var array2 = [ "사과", "배", "감" ];

array.concat(array2) = [ "ghi", "abc", "def", "사과", "배", "감" ];
```
- .split()
```javascript
var str = "안녕하세요";
str.split('') = [ "안", "녕", "하", "세", "요" ];

var str2 = "가, 나, 다";
str2.split(', ') = [ "가", "나", "다" ];

var str3 = "서울-대전-부산";
str3.split('-') = [ "서울", "대전", "부산" ];
```
