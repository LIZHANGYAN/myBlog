---
title: '[原]JSP在Eclipse中调用.class'
tags:
  - java
  - servlet
categories: 我怎么会这些杂七杂八的东西
date: 2014-11-01 21:17:47
---

这两天在学习Jsp，在调用.class的时候总是报错，最后才发现再写.Java时必须要用包名，然后再用
<!-- more -->
```
<%@ page import=test.TestBean%>调用
```
