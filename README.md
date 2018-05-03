# gozh_all
> build all gozh , such as backend, web client, http server, database

## 获取项目

>git clone https://github.com/gozh-io/gozh_all.git

``` bash
这里通过docker-compose,搭建整个gozh中文社区服务
目录说明:
	mongo   --- mongo配置,数据,日志
	myapp   --- 后端接口的日志
	nginx   --- nginx配置,日志,web静态内容
其中
	只有nginx目录下conf,html,需要在make up前配置好
	mongo,myapp目录都不需要配置
```
	
## Build Setup 
在gozh_all目录下操作

``` bash
1.搭建环境
	make

2.运行gozh社区服务
    make up

3.停止gozh社区服务
	make down
```

## 获取前端项目

>在gozh_all目录下make up执行成功后,需要单独生成web前端的静态资源,复制到nginx/html,才能看到页面

``` bash
cd gozh_all目录同级目录
git clone https://github.com/gozh-io/gozh_web.git
cd gozh_web
npm install
npm run build
生成dist目录
mv dist  ../gozh_all/nginx/html/gozh
```
