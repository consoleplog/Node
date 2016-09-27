### 部署项目 deploy project

1. 上传代码：ssh   git   github

    scp -r express-api(文件夹) username.com（服务器）

2. 登录到服务器上

    ssh + ip/域名（ssh的远程登录)

3. 安装服务器（此处为软件Server)

    sudo apt-get install nginx (nginx 当下最流行的软件Server)

    - sudo:使用管理员权限

    - apt-get install：安装软件

    - nginx : 被安装的软件
4. 配置 ***nginx*** Server

    修改配置文件，进入： cd /etc/nginx 文件夹下（nginx配置区域）

    查看可用的网站： cd sites-enabled

    创建配置文件：sudo touch express.conf

    修改配置文件：sudo vim express.conf
```js
附录：express.conf
server {
    listen  80 default;
    server_name username.express.com;
    root /home/username//express-api/;
}
```
5.  重新加载配置文件

    sodu service nginx reload

    fail (配置文件写的有错误)

    sudo nginx -t 查看错误信息

### 局域网内模拟部署过程

第一步: 安装 ssh server

  - sudo apt-get install openssh-server  开放自己的机器给对方登录

第二步：访问对方ip(ifconfig查看ip)

  - ping 对方ip 查看是否连通
  - 访问方式：用户名@ip 输入对方密码

第三步：上传自己文件到对方电脑上
  - scp -r username-express someone@192.168.1.158:

  在:之后不加路径的话，会把上传的文件放到对方的用户主目录下（后面的：是必须添加的）
  - scp -r  xiaoxiao@192.168.1.115:20160926.pdf .    这个直接是从别人电脑上拷贝文件到本地的当前目录下，最后的.是本地当前目录的意思
  前提得知道对方的密码

  - 回到自己机器上，再配置 nginx Server下的.config文件。修改配置文件，进入： cd /etc/nginx 文件夹下（nginx配置区域）
  ```js
  附录：express.conf
  server {
      listen  80 default;  
      server_name username.express.com;
      root /home/username/express-api/;
  }
  ```
  重新加载 sodu service nginx reload

  default 只能有一个

### Vim 教程

1. 打开文件： vim filename(打开文件，若不存在则创建并打开)

1. 进入插入模式：i

3. 保存并退出界面：先按ESC 再按大写Z再次。

4. 不保存强制退出：先按ESC 然后输入 :q!

request  请求

response 响应

writer:liyuexi
