---
title: JavaScript语言精粹读书笔记
date: 2017-12-20 18:00
tags: [JavaScript]
categories: 前端技术
---


## 函数的递归调用
* 汉诺塔问题：
    `const hanoi = (disc, src, aux, dst) => {
        if (disc > 0) {
          hanoi(disc-1, src,dst,aux)
          console.log('move disc ' + disc + ' from ' + src + ' to ' + dst)
          hanoi(disc-1,aux,src,dst)
        }
    }
    hanoi(3, 'src','aux','dst')`
  理解：把问题简化为两个盘子，盘子1代表最上层盘子， 盘子2为下面所有的盘子。 对盘子2进行递归调用即可。

