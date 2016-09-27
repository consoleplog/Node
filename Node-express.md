request  请求

response 响应


### DNS  绑定

ip    和    域名


sudo vim /etc/hosts  本地可访问ip 绑定假域名

1. ip  ========= 域名
2.  server 下的 指向文件
```js
server_name domain
root /home/fuwuqi/ 指向文件
```


公钥 id_rsa.pub
私钥  id_rsa

commamd:ssh-keygen  生成钥匙

复制公钥

$ sudo vim authorized_keys  服务器端 创建编辑公钥

# Express

react  前端框架

express 是后台框架

服务器 数据

1. html css js

    express js 后台框架  作用：查询数据和插入数据到html

2. database  基础数据  数据库



### http 请求

http  request =  verb + path

(http  request = get /post/... +path)

服务器接受请求

1. get请求

读取请求参数

request =verb +path

req:
参数（parameters）作为path 来传给后台，这样可以实现前台数据传入后台代码中。

#### CURL 教程

服务器模拟请求

1. install curl  

2. curl --request GET localhost:3000/some one

3. curl --request POST localhost:3000/some one


2. post请求

### router




express 框架 建立

1. npm init

2. npm i express --save

3.  build index.js

4.  node index.js
