---
title: "[JavaScript] 스크롤 반응형 메뉴바"
date: 2019-10-27
categories:
- JavaScript
tags:
- JavaScript
- JQuery
---

### HTML
```html
<div id="header"></div>
```

### CSS
```css
body {
    height:2000px;
}
#header {
    position: fixed;
    top:0;
    left:50%;
    transform:translateX(-50%);
    background:salmon;
    width:100%;
    height:100px;
    transition: top 0.7s ease-in-out;
}
#header.hide {
    top:-100%;
}
```

### JavaScript
```javascript
var lastScrollTop = 0;
var headerHeight = $("#header").outerHeight();

$(window).scroll(function() {
    var scrollTop = $(this).scrollTop();

    if ( scrollTop > lastScrollTop && scrollTop > headerHeight ) {
        $("#header").addClass("hide");
    } else {
        $("#header").removeClass("hide");
    }

    lastScrollTop = scrollTop;
});
```

### 결과확인
<p class="codepen" data-height="500" data-theme-id="light" data-default-tab="result" data-user="jiyeonjyn" data-slug-hash="ExxbKJN" style="height: 500px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="스크롤 반응형 메뉴바">
  <span>See the Pen <a href="https://codepen.io/jiyeonjyn/pen/ExxbKJN">
  스크롤 반응형 메뉴바</a> by 이지연 (<a href="https://codepen.io/jiyeonjyn">@jiyeonjyn</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>