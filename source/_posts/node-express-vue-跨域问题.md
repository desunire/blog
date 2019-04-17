---
title: node-express vue 跨域问题
date: 2019-04-17 14:27:39
tags:
---


部分总结：
1:跨域问题的出现是浏览器的一种安全策略，服务器与服务器之间是不存在的
2: vue 前端post请求 在服务端被解析成options请求的原因 是报文变成了OPTION包，而不是POST请求报文。
这是跨域访问的一种安全检查机制，需要在前端设置下请求的header，常见的是 
{
'Content-Type':'application/x-www-form-urlencoded'
},

3:node-express 框架下允许跨域的方案 
a: 在每个请求的res下设置header信息
res.header('Access-Control-Allow-Origin', '*');
res.header('Access-Control-Allow-Methods', 'POST, GET, PUT, PATCH, OPTIONS, DELETE');
res.header('Access-Control-Allow-Headers', 'origin, content-type');
b:整体在app中设置app.all  这个方案经测试，没起效果
c:使用cors
var cors = require('cors');
app.use(cors());


4:跨域问题 还是需要服务端配合解决的，前端需要注意你request中header的部分属性设置

