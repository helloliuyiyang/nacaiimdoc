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

本机配置数据

    /*
     Navicat Premium Data Transfer

     Source Server         : 127.0.0.1
     Source Server Type    : MySQL
     Source Server Version : 80015
     Source Host           : localhost:3306
     Source Schema         : im

     Target Server Type    : MySQL
     Target Server Version : 80015
     File Encoding         : 65001

     Date: 08/02/2020 11:08:54
    */

    SET NAMES utf8mb4;
    SET FOREIGN_KEY_CHECKS = 0;

    -- ----------------------------
    -- Table structure for node_list
    -- ----------------------------
    DROP TABLE IF EXISTS `node_list`;
    CREATE TABLE `node_list` (
      `id` int(11) NOT NULL AUTO_INCREMENT,
      `tcp_port` int(4) NOT NULL,
      `udp_port` int(4) NOT NULL,
      `weight` int(4) NOT NULL,
      `server_type` int(4) NOT NULL,
      `tcp_protocol` varchar(255) DEFAULT NULL,
      `address` varchar(512) NOT NULL,
      `disabled` int(4) NOT NULL DEFAULT '0',
      PRIMARY KEY (`id`)
    ) ENGINE=InnoDB AUTO_INCREMENT=3 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci;

    -- ----------------------------
    -- Records of node_list
    -- ----------------------------
    BEGIN;
    INSERT INTO `node_list` VALUES (1, 21983, 21985, 100, 1, '\"\"', '127.0.0.1', 0);
    INSERT INTO `node_list` VALUES (2, 31983, 31985, 100, 2, '\"\"', '127.0.0.1', 0);
    COMMIT;

    SET FOREIGN_KEY_CHECKS = 1;


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



