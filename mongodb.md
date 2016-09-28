# mongodb

### 安装
1. brew update
2. brew 下载 mongdob

### 启动
1. mongod --dbpath=./data
2. mongo

## 增加

```js
1. Database:use name

2. collection: db.collection('name')

3. document: - db.collection.insert({name:'asd',age:30})
             - db.collection.sever({})
```

## 删除

```js
1. Database:  db.dropDatabase();

2. collection: db.collection.drop();

3. document: - db.collection.remove({name:'asd',age:30})
             - db.collection.{{name:'asd',age:30},{justone:true}}
```

## 查

```js
1. Database: show dbs

2. collection: show collections

3. document: - db.collection.find({age:1})//1：选择显示 ，0：反向选择显示 .
               db.collection.find({})
             - db.collection.find()
             - db.collection.find().count()// list number
             - db.collection.findOne()...
             - collectoin_name集合名词
             - key字段
             - value值
             - db.worker.find({age: {$gte: 30}}) //查询age 3大于等于30 的数据
            - db.worker.find({age: {$gte: 30}}) //查询age 3大于等于30 的数据
            - db.worker.find({age: {$lt: 30}}) //查询age 小于30的数据
            - db.worker.find({age: {$lte: 30}}) //查询age 小于等于30的数据
            - db.worker.find({age: {$gte: 30, $lte: 50}})
            //查询age 大于等于 30 并且 age 小于等于 50 的数据
            - db.worker.find().limit(3) //查询前3条数据

            - db.worker.find().skip(3) //查询3条以后的数据

            - db.collectoin_name.find().sort({key:1})
            - db.collectoin_name.find().sort({key:-1})
            //sort()方法可以通过参数指定排序的字段，并使用 1 和 -1 来指定排序的方式，其中 1 为升序排列，而-1是用于降序排列


            db.collection.help() //查找更多方式
```

## 改

```js
1. Database: 只能删除 然后复制内部集合

2. collection: db.collection.renamecollection('')

3. document: audata- db.collection.update({name:'asd'},{$set:{name:'asd1'}})
db.collection.update({name:'asd'},{$inc:{age:'1'}})
//nowage= update.inc+age //
db.collection.update({name:'asd1'},{$upsert:{age:'1'}})
//条件不存在则新增。
db.collection.update({name:'asd1'},{$set:{age:'1'}}，{multi:true})
//默认相同条件更新 第一个，如果打开multi那么相同条件全部更新，反之返回默认。
             cover- db.collection.save({_id:'1dsas',name:'asd1'})
```

## 复制

```js
1. Database:

2. collection:

3. document:
```
