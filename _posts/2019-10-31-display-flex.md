---
title: "[CSS] display : flex"
date: 2019-10-31
categories:
- CSS
tags:
- CSS
- display
- flex
---

# display : flex
- 정렬하고자 하는 엘리먼트의 부모 태그에 적용
- 뒤에 나올 속성 또한 정렬하고자 하는 엘리먼트의 부모 태그에 적용해야 한다.

## 정렬하고자 하는 엘리먼트의 부모 태그에 적용해야 하는 속성

### flex-direction
- row : 요소들을 가로로 정렬
- row-reverse : 요소들을 가로로 역순 정렬
- column : 요소들을 세로로 정렬
- column-reverse : 요소들을 세로로 역순 정렬

###  justify-content ( 하나의 줄 내부에서 요소 정렬, 요소들의 간격 지정 )
- flex-start : 요소들을 컨테이너의 왼쪽에 정렬
- flex-end : 요소들을 컨테이너의 오른쪽에 정렬
- center : 요소들을 컨테이너의 가운데에 정렬
- space-between : 요소들 사이에 동일한 간격 설정
- space-around : 요소들 양옆에 동일한 간격 설정
- space-evenly : 모든 간격을 동일하게 설정<br><br>
<img src="https://css-tricks.com/wp-content/uploads/2018/10/justify-content.svg" width="350" height="auto" style="margin-left:0;">

### align-items ( 컨테이너에서 줄의 위치 설정 )
- flex-start : 요소들을 컨테이너의 맨 위에 배치
- flex-end : 요소들을 컨테이너의 맨 밑에 배치
- center : 요소들을 컨테이너의 세로선 상의 가운데에 배치
- baseline : 요소들을 컨테이너의 기준선에 배치
- stretch : 요소들을 컨테이너에 맞도록 늘림<br><br>
<img src="https://css-tricks.com/wp-content/uploads/2018/10/align-items.svg" width="350" height="auto" style="margin-left:0;">

### align-content ( 각 줄을 정렬, 각 줄의 간격 지정 )
- **한 줄만 있는 경우, align-content는 적용되지 않는다.**<br><br>
- flex-start : 여러 줄들을 컨테이너의 맨 위에 정렬
  - `align-items: flex-start`보다 좁은 간격으로 배치된다.
- flex-end : 여러 줄들을 컨테이너의 맨 밑에 정렬
  - `align-items: flex-end`보다 좁은 간격으로 배치된다.
- center : 여러 줄들을 세로선 상의 가운데에 정렬
  - `align-items: center`보다 좁은 간격으로 배치된다.
- space-between : 각 줄 사이에 동일한 간격 설정
- space-around : 각 줄 양옆에 동일한 간격 설정
- stretch : 각 줄을 컨테이너에 맞도록 늘림<br><br>
<img src="https://css-tricks.com/wp-content/uploads/2018/10/align-content.svg" width="350" height="auto" style="margin-left:0;">

### flex-wrap
- nowrap : 모든 요소들을 한 줄에 정렬
- wrap : 요소들이 넘칠 경우 여러 줄로 나누어 정렬
- wrap-reverse : 요소들이 넘칠 경우 여러 줄로 나누어 정렬하되 각 줄을 역순으로 정렬
<p class="codepen" data-height="500" data-theme-id="light" data-default-tab="result" data-user="jiyeonjyn" data-slug-hash="eYYeePR" style="height: 500px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="[CSS] flex-wrap">
  <span>See the Pen <a href="https://codepen.io/jiyeonjyn/pen/eYYeePR">
  [CSS] flex-wrap</a> by 이지연 (<a href="https://codepen.io/jiyeonjyn">@jiyeonjyn</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

### flex-flow
- flex-direction과 flex-wrap을 간략히 적용하는 속성
- `flex-flow : <flex-direction> <flex-wrap>;`
  - ex) flex-flow : row wrap;


## 정렬하고자 하는 엘리먼트에 직접 적용해야 하는 속성

### order
- 자식 요소에 order 속성을 적용하여 정렬 순서를 바꿀 수 있다.
- 기본값은 0이며 정수의 값을 가진다.
  - ex) ..., -2, -1, 0, 1, 2, ...
- order 숫자가 작은 것부터 오름차순으로 정렬된다. (정렬 방향은 flex-direction에 의해 결정됨)

### align-self
- 그 줄의 다른 엘리먼트와 별개로 해당 엘리먼트만  align-items를 따로 적용할 수 있다.
  - 해당 엘리먼트가 빠진 자리를 그 다음 엘리먼트가 대체하지 않고 빈 공간으로 놔둔다.
- 속성값으로 align-items가 사용하는 값들을 가진다.

## display:flex 활용
- margin, position 등 다른 속성을 사용하지 않고 간단하게 가운데 정렬할 수 있다.
```css
div.wrap {
    display:flex;
    width:100%;
    justify-content:center;
}
```

## Reference
- <http://flexboxfroggy.com/#ko>