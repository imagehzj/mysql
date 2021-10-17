# mysql
## usage
### dry run
```bash
docker run -it --rm ttbb/mysql:nake bash
```
### run with port
```bash
docker run -p 3306:3306 -it --rm ttbb/mysql:nake bash
```
## 安装流程
### 以普通用户(sh)安装
```bash
wget https://dev.mysql.com/get/Downloads/MySQL-8.0/mysql-8.0.18-1.el8.x86_64.rpm-bundle.tar
tar -xf mysql-8.0.18-1.el8.x86_64.rpm-bundle.tar -C mysqlrpm

yum localinstall -y /opt/sh/mysql/source/mysqlrpm/*rpm

mysqld --initialize-insecure --user=sh
mysqld --user=sh
```
### 以root安装
```bash
wget https://dev.mysql.com/get/Downloads/MySQL-8.0/mysql-8.0.18-1.el8.x86_64.rpm-bundle.tar
tar -xf mysql-8.0.18-1.el8.x86_64.rpm-bundle.tar -C mysqlrpm

yum localinstall -y /opt/sh/mysql/source/mysqlrpm/*rpm

mysqld --initialize-insecure --user=root
mysqld --user=root
```

### mysql日志路径
/var/log/mysqld.log