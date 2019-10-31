---
title: "[CSS] display:flex"
date: 2019-10-29
categories:
- CSS
tags:
- CSS
- display
- flex
---

## display:flex
- 정렬하고자 하는 엘리먼트의 부모 태그에 적용
- 뒤에 나올 속성 또한 정렬하고자 하는 엘리먼트의 부모 태그에 적용해야 한다.

### flex-direction
###  justify-content
- flex-start: 요소들을 컨테이너의 왼쪽에 정렬
- flex-end: 요소들을 컨테이너의 오른쪽에 정렬
- center: 요소들을 컨테이너의 가운데에 정렬
- space-between: 요소들 사이에 동일한 간격 설정
- space-around: 요소들 양옆에 동일한 간격 설정
- space-evenly: 모든 간격을 동일하게 설정<br>
<img src="https://css-tricks.com/wp-content/uploads/2018/10/justify-content.svg" width="300" height="500">

### align-items
- flex-start: 요소들을 컨테이너의 맨 위에 정렬
- flex-end: 요소들을 컨테이너의 맨 밑에 정렬
- center: 요소들을 컨테이너의 세로선 상의 가운데에 정렬
- baseline: 요소들을 컨테이너의 시작 위치에 정렬
- stretch: 요소들을 컨테이너에 맞도록 늘림<br>
<img src="https://css-tricks.com/wp-content/uploads/2018/10/align-items.svg" width="300" height="400" style="margin-left:0;">

### order
### align-self
### flex-wrap
### flex-flow
align-content

### 예시

### Reference
- <http://flexboxfroggy.com/#ko>