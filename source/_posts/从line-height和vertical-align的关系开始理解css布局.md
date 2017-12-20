---
title: 移动端适配方案总结
date: 2017-11-5 18:00
tags: [CSS3,HTML,移动开发]
categories: 前端技术
---
* 布局视口layout viewport：指根元素html的宽度，用document.documentElement.clientWidth获取
* 视觉视口visual viewport: 显示在视觉区域内的css像素宽度，页面缩放会影响其大小,用window.innerWidth获取
* 理想视口：screen.width指设备屏幕宽度，在移动端开发时，把布局视口的宽度设置这个宽度，成为理想视口
* 布局视口就好像一片大小固定的风景，视觉视口就好像相机里的显示屏里看到的画面，焦距越小（页面缩小）画面内容越多（视口越大），焦距越大（页面放大）画面内容越少（视口越小）
> Screen size tests  https://quirksmode.org/m/tests/widthtest_vp380.html
> 本人使用chrome浏览器模拟手机设备，页面缩放后，测试window.innerWidth返回值错误

## 基础知识
* [移动端高清、多屏适配方案](http://div.io/topic/1092)
* [移动端尺寸基础知识](http://www.cnblogs.com/chris-oil/p/5367106.html)
* [PPK剖析viewports](http://www.w3cplus.com/css/viewports.html)

## 进阶
* [移动端应该如何动态设置字体大小](https://segmentfault.com/a/1190000004189237)
* [移动端页面布局及字体大小该如何设置](https://segmentfault.com/a/1190000004344753)
* [移动端适配方案(上)](https://github.com/riskers/blog/issues/17)
* [移动端适配方案(下)](https://github.com/riskers/blog/issues/18)
* [移动端前端适配方案对比](https://github.com/Hancoson/blog/issues/11)
* [手机端页面自适应解决方案—rem布局进阶版（附源码示例](http://www.jianshu.com/p/985d26b40199)
* [一篇真正教会你开发移动端页面的文章(二)](http://hcysun.me/2015/10/19/%E4%B8%80%E7%AF%87%E7%9C%9F%E6%AD%A3%E6%95%99%E4%BC%9A%E4%BD%A0%E5%BC%80%E5%8F%91%E7%A7%BB%E5%8A%A8%E7%AB%AF%E9%A1%B5%E9%9D%A2%E7%9A%84%E6%96%87%E7%AB%A0-%E4%BA%8C/)

## 手淘解决方案
* [使用Flexible实现手淘H5页面的终端适配](http://www.w3cplus.com/mobile/lib-flexible-for-html5-layout.html)
* [再聊移动端页面的适配](https://www.w3cplus.com/css/vw-for-layout.html)
* [从网易与淘宝的font-size思考前端设计稿与工作流](http://www.cnblogs.com/lyzg/p/4877277.html)
* [淘宝弹性布局方案lib-flexible实践](http://www.cnblogs.com/lyzg/p/5058356.html)
* [基于淘宝适配方案flexible + 翻屏h5 适配方案adaptive](https://github.com/chesscai/flexible-adaptive)
* [移动端布局终极解决方案-hotcss](https://github.com/imochen/hotcss)