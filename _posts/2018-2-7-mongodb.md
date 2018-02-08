---
layout: post
title: mongoDB
date: 2018-2-7
tags: 数据库
---
	学习mongoDB中的知识点
### 补丁
[下载补丁](http://hotfixv4.microsoft.com/Windows%207/Windows%20Server2008%20R2%20SP1/sp2/Fix405791/7600/free/451413_intl_x64_zip.exe)

### mongoDB
[下载mongoDB](https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.2-signed.msi)
### mongoDB命令
* 开机
```
mongod --dbpath F:\mongo
--dbpath 就是选择数据库文档所在的文件夹
```
* 使用数据库
```
mongo
```
* 导入数据
```
mongoimport
```
* 重新开启cmd，使用mongo
```
mongo
```
* 显示数据库
```
show dbs
```
* 使用某个数据库
```
use 数据库名
```
如果想新建数据库，也是use，use一个不存在的 ，就是新建

