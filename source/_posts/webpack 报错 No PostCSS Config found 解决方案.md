---
title: webpack 报错 No PostCSS Config found 解决方案
date: 2017-9-20
tags: webpack
categories: 前端技术
---

ebpack 报错 No PostCSS Config found  这个问题我在百度上找了好久，也没有找到解决方案，最后没有办法只能自己去啃官方文档，本案例在本人的webpack 学习感悟中已经写过，但是发现很多人还是没有找到答案，所以就将本问题整理为独立版本。本着互联网分享精神，现将本篇文件分享给大家。
<!--more-->
本案例经过本人实测绝对好使。 


安装：
>npm install postcss-import autoprefixer cssnano style-loader postcss-loader --save-dev

webpackconfig.js配置
```javascript
var htmlWebpackPlugin = require('html-webpack-plugin');
var path = require('path');
module.exports = {
    entry: './src/app.js',
    output: {
        path: path.resolve(__dirname, './dist/js'),
        filename: 'js/[name].bundle.js'
    },
    module: {
        loaders: [
            {
                test: /\.css$/,
                use: [
                    'style-loader',
                    {
                        loader: 'css-loader',
                        options: {importLoaders: 1} //这里可以简单理解为，如果css文件中有import 进来的文件也进行处理
                    },
                    {
                        loader: 'postcss-loader',
                        options: {           // 如果没有options这个选项将会报错 No PostCSS Config found
                            plugins: (loader) => [
                                require('postcss-import')({root: loader.resourcePath}),
                                require('autoprefixer')(), //CSS浏览器兼容
                                require('cssnano')()  //压缩css
                            ]
                        }
                    }
                ]
            }
        ]
    },
    plugins: [
        new htmlWebpackPlugin({
            filename: 'index.html',
            template: 'index.html',
            inject: 'body'     //将js文件插入body文件内
        }),
    ]
};
```

入口文件app.js内容
```javascript
import  './css/common.css';
const App = function () {
};
new App();
```

原文地址；http://www.cnblogs.com/waitforyou/p/6872066.html