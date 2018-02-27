---
layout: post
title: mongoDB
date: 2018-2-7
tags: 数据库
---

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

* 插入数据
```
db.student.insert({"name":"xiaoming","age":12,"sex":"nan"})
```

* 显示集合
```
show collections
```

* 显示集合中的数据
```
db.student.find()
```

* Mongo Vue安装
[安装教程](http://blog.csdn.net/lupengfei1009/article/details/50832996#mongovue%E5%AE%89%E8%A3%85)

* 导入数据
选择在外部写好数据，然后导入数据,`执行此命令必须重新开启cmd,单独执行此语句`，在mongo执行后继续执行此命令将会报错，无法执行
```
mongoimport --db test --collection restaurants --drop --file primer-dataaset.json
```
	* --db test  想往那个数据库导入
	* --collection restaurants 想往那个集合中导入
	* --drop 把集合清空
	* --file primer-dataset.json 导入哪个文件

* 查找数据，用find。find中没有参数，那么将列出这个集合的所有文档
```
db.restaurants.find()
```

* 精确匹配
```
db.student.find({"scrore.shuxue":70})
```

* 多个条件
```
db.student.find({"score.shuxue":70,"age":12})
```

* 大于某个值
```
db.student.find({"score.yuwen":{$gt:59s}})
```

* or 查询
```
db.student.find({$or:[{"age":9},{"age":11}]})
```

* 排序
查找完毕之后，打点调用sort,表示升降排序,`1`表示升序，`-1`表示降序
```
db.student.find().sort({"borough":1,"address.zipcode":1})
```

* 更新 update
更新数据
```
db.stuent.update({"age":{$lt:20}},{$set:{"age":18}})  更新一条
db.stuent.updateMany({"age":{$lt:20}},{$set:{"age":18}}) 更新所有
```

* 删除 remove
```
db.student.remove({"age":18})  删除所有
db.student.remove({"age":18},{justOne:true}) 仅删除一条
```

* 分页
```
limit()  skip()
```
