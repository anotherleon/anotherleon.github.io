---
title: 解决vuex中的数据在页面刷新以后消失问题
date: 2017-11-7 12:00
tags: [vuex,localStorage]
categories: 前端技术
---

## 背景 
* 技术栈vue + vue-router + vuex
* 项目有个页面微信自定义分享功能，从首页一步一步点进去可以正常分享，但是一旦刷新页面或者直接进去发现'undefined XXXX....'
* 原因分析：因为页面刷新后vuex的state重新清空了（vuex数据保存在内存中）
* 解决办法：持久化vuex的数据,或者vuex-persist持久化插件

 > [使用 Web Storage API](https://developer.mozilla.org/zh-CN/docs/Web/API/Web_Storage_API/Using_the_Web_Storage_API#相关链接)
 
 > [使用localStorage解决vuex在页面刷新后数据被清除的问题](http://www.cnblogs.com/limengyi/p/6534435.html) 
 
 > [vuex中的数据在页面刷新以后消失怎么办？](https://www.zhihu.com/question/54164220)