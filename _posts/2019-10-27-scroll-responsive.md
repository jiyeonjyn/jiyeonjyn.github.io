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
    background:#555;
    width:100%;
    height:130px;
    transition: top 0.5s;
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