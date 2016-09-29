# js mongo    ｛mongoose｝

 mongoDB 本身命令行命令操作 。

^
     适配层

|
    mongoose    [传送门]http://mongoosejs.com

         **数据模型对象话**

        - 把数据转化js对象

        - 用js代码来控制mongdb的数据
v

 express 后台框架框架

使用说明：

1. npm install mongoose 作为模块导入

  - js 代码中链接 mongondb
```js
// index.js
var mongoose = require('mongoose');

mongoose.connect('mongodb://localhost:27017/forwebdb');
//链接数据库
```
每个项目只需要一个数据库就可以

2.
```js
var db = mongoose.connection
//数据库链接 赋予给db变量   相当于api

```


3. 测试
```js
db.on('error', console.error.bind(console, 'connection error:'));
db.once('open', function() {
  console.log('ok')
});
```
4.
建立数据 Schema

Schema 概要

 描述数据结构

描述记录（文档）结构

规定

这个记录中有几个字段（field）

每个字段名字（name）

以及字段类型（string）

 ```js

 ```

 5.
  Model
  模型的概念

  model  MVC 中的m ｛模型视图控制器｝Model View Controller

  模型是 代码数据库的中间

  视图   是人和模型的中间人

  控制器是

  model通常会写成一个类

  存放所有和数据直接相关的代码

  构建一条数据记录

  数据结构 ＋ 数据模型 ＋ 实例化
  ```js
  var personSchema = mongoose.Schema({
    name: String
  })// make base type
  var person = mongoose.model('', personSchema)；//一条记录的名字和数据类型   //collection name   and  basetype
  var frank = new person({ name: 'frank' },{password:'123456'},{age:'100'});//实例化
    console.log(frank.name);

  ```

## 用 nodejs 增 删 改 查

```js
collection.save()  //

collection.find().exec(function(err,collections){
  console.log(collections)
  // 异步执行代码 （提高效率）
})

updata
person.findById({_id:'57ecc8eb8d52f60559de08a6'},function(err,user){
  user.name= 'oooopopo'
  user.save(function(err){
    console.log('delete')
    person.find().exec(function(err, persons) {
     // 异步执行
     console.log(persons);
   });
  })
})

remove//delete
person.findById({_id:'57ecc8eb8d52f60559de08a6'},function(err,user){
  // user.name= 'oooopopo'
  user.remove(function(err){
    console.log('delete')
    person.find().exec(function(err, persons) {
     // 异步执行
     console.log(persons);
   });
  })
})
```
