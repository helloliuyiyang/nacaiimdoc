## 1.4 系统启动

im需要安装单机版的redis, mysql.

启动过程

1: 安装单机版的redis并启动

2: 安装msyql并启动

使用im 自带的账号管理服务器,安装mysql后

```bash
create database im;
grant all privileges on *.* to "im"@"localhost" identified by "12345678" with grant option;

use im;

CREATE TABLE `user_id` (
                              `id` INT UNSIGNED NOT NULL AUTO_INCREMENT,
                              `no` VARCHAR(32) UNIQUE NOT NULL,
                              PRIMARY KEY (`id`),
                              UNIQUE INDEX `id_UNIQUE` (`id` ASC) );
```

3:启动账号服务器

```
cd /Users/nacai/gopath/src/nacaiim/bin
./as
```

4: 启动存储服务器

```
cd /Users/nacai/gopath/src/nacaiim/bin
./ss
```

5: 启动路由服务器

```
cd /Users/nacai/gopath/src/nacaiim/bin
./rs
```

6:启动接入汇聚服务器

```
cd /Users/nacai/gopath/src/nacaiim/bin
./s
```

7:启动接入消息变更通知服务器

```
cd /Users/nacai/gopath/src/nacaiim/bin
./syncs
```

8:启动接入消息同步服务器

```
cd /Users/nacai/gopath/src/nacaiim/bin
./chats
```



