# MAC Docker 配置文件

启动4个Docker：`nginx`, `php`, `mysql`,  `memcached`。`nginx`连接 `php`，`php` 连接 `mysql`, `memcached`。

四个服务都可定制。

每个服务都有独立的文件夹存储其相关内容。

 - `nginx`： 存储 nginx 的默认站点配置文件：`default.conf`；
 - `mysql`： 存储 mysql 的配置文件 `mysql.cnf`；
 - `php`： 存储定制 php image 的 `Dockerfile`，以及`php.conf`；

  官方的 php 是不带 mysql 和 memcached 插件的，因此需要使用 Dockerfile 进行定制。

## 启动

```
docker-compose up -d
```

## 访问服务

通过`docker-machine ip dev` 查看虚拟机 ip 直接访问 site 站点


## 停止服务

```
docker-compose stop
```
