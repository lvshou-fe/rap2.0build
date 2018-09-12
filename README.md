# 前言

```
rap 2.0 是nodejs + react 前后端分离项目

前端架构(rap2-dolores)
React / Redux / Saga / Router
Mock.js
SASS / Bootstrap 4 beta
server: nginx

后端架构(rap2-delos)
Koa
Sequelize
MySQL
Server
server: node
```

# 官网线上demo

[demo](http://rap2.taobao.org/)


# 前端

[前端github地址](https://github.com/thx/rap2-dolores)

```
git clone https://github.com/thx/rap2-dolores.git

development 开发模式
# initialize 初始化
npm install

# config development mode server API path in /src/config/config.dev.js
# 配置开发模式后端服务器的地址。 /src/config/config.dev.js

# test cases 测试用例
npm run test

# will watch & serve automatically 会自动监视改变后重新编译
npm run dev
```

# 后端

[后端github地址](https://github.com/thx/rap2-delos)

```
git clone https://github.com/thx/rap2-delos.git

部署流程太繁琐直接看
https://github.com/thx/rap2-delos
```

# 常见问题

```
先创建创建数据库
npm run create-db 失败
修改mysql数据库账号密码 src/config dev 开发环境
```

### npm run create-db
错误消息:

mysql Client does not support authentication protocol requested by server; consider upgrading MySQL



先登录:

```
sudo mysql -u root -p
```

解决:

```
ALTER USER 'root'@'%' IDENTIFIED WITH mysql_native_password BY '你的密码';
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY '你的密码';
SELECT plugin FROM mysql.user WHERE User = 'root';
```

参考地址:

[解决地址](https://blog.csdn.net/qq_19707521/article/details/80226321)
