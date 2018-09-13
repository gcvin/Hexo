---
title: CSS实用知识点
tags:
  - Testing
categories: CSS
---
### flex-grow && flex-shrink
https://zhuanlan.zhihu.com/p/24372279

### rgba函数的妙用
http://zcfy.cc/article/the-power-of-the-rgba-color-function-in-css-css-tricks-2001.html
<!-- more -->

### background-position百分数取值原理
> X轴:(容器宽度-背景图片宽度)*X轴百分比
Y轴:(容器高度-背景图片高度)*Y轴百分比

http://www.w3cplus.com/css/background-position-with-percent.html

### margin相邻折叠问题
https://gold.xitu.io/post/58651b0d1b69e675fce5da7e

### 自适应高度塌陷

```css
.box::after {
    content: '';
    display: table;
}
.box::after {
    clear: both;
}
```

### placeholder 改变颜色

```css
::-webkit-input-placeholder { /* WebKit, Blink, Edge */
    color:    #909;
}
:-moz-placeholder { /* Mozilla Firefox 4 to 18 */
    color:    #909;
    opacity:  1;
}
::-moz-placeholder { /* Mozilla Firefox 19+ */
    color:    #909;
    opacity:  1;
}
:-ms-input-placeholder { /* Internet Explorer 10-11 */
    color:    #909;
}
::-ms-input-placeholder { /* Microsoft Edge */
    color:    #909;
}
```

### 左边自适应右边定宽

```css
.left {
    flex-grow: 1
}
.right {
    width: 200px;
    flex-shrink: 0;
}
```

### defer async

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <!--headScripts.js为必须在DOM解析前加载并执行的脚本-->
    <script src="headScripts.js"></script>
    <!--bodyScripts.js加个defer,先加载。等DOM解析好了再执行-->
    <script defer src="bodyScripts.js"></script>
</head>
<body>
    <!--body内容-->
    <h1 id='load-experiment'> hello world </h1>
    <!--独立的组件，不依赖DOM, 锦上添花型的，可用async-->
    <script async src="forumWidget.js"></script>
    <script async src="chatWidget.js"></script>
</body>
</html>
```

### CSS hack区分IE8/IE7/IE6

```css
.ie6_7_8{
    color:blue; /*所有浏览器*/
    color:red\0; /*IE8以及以上版本浏览器*/
    color:red\9; /*IE8以及以下版本浏览器*/
    *color:green; /*IE7及其以下版本浏览器*/
    _color:purple; /*IE6浏览器*/
}
```
