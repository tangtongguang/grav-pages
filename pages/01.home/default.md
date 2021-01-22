---
title: 'CSS 绝对定位'
taxonomy:
    category:
        - css
    tag:
        - position
body_classes: 'title-center title-h1h2'
---

为了链接悬停状态下只是文字下显示边框，不让#下有边框可以采用绝对定位

```html
<a><span>#</span>link</a>
```

```css
a {
    position:relative;
    border-bottom: 1px solid transparent;
}
a span {
    positon: absolute;
    padding-right: 0.6em;
    right: 100%;
}
a:hover {
    border-bottom-color: #666
}
```
