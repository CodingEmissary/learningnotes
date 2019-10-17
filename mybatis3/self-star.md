# Mybatis3-star 学习笔记

# 环境配置

安装docker

```
brew cask install docker
```

安装mysql

- 拉取mysql镜像：docker pull mysql:5.7 
- 运行mysql-docker：docker run --name mysql -e MYSQL_ROOT_PASSWORD=123456 -d -i -p 3306:3306 --restart=always mysql:5.7 
- 进入mysql bash命令行：docker exec -ti mysql bash mysql
- 客户端连接mysql：mysql -hlocalhost -P3306 -uroot -p123456

建表建库

```mysql
create database investment;
use investment;
CREATE TABLE IF NOT EXISTS `time_deposit` (
	`id` bigint NOT NULL AUTO_INCREMENT,
	`platform` int NOT NULL DEFAULT 1 COMMENT '平台。1:支付宝2:同花顺',
	`prod_code` varchar(64) NOT NULL COMMENT '理财产品代码',
	`prod_name` varchar(128) NOT NULL COMMENT '理财产品名称',
	PRIMARY KEY (`id`)
) ENGINE=InnoDB CHARSET=utf8;
```

测试代码

[Java code](https://github.com/vmstar/mybatis.git)

## 事务

行为定义：

- commit：提交事务
- rollback：回滚事务
- close：关闭事务内部的sql链接
- getConnection：获取内部的链接

