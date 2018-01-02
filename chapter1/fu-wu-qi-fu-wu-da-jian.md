# 服务器搭建（centos6.8）

LNMP代表的就是：Linux系统下Nginx+MySQL+PHP这种网站服务器架构。Nginx是一个高性能的HTTP和反向代理服务器，也是一个IMAP/POP3/SMTP代理服务器。Mysql是一个小型关系型数据库管理系统。PHP是一种在服务器端执行的嵌入HTML文档的脚本语言。这四种软件均为免费开源软件，组合到一起，成为一个免费、高效、扩展性强的网站服务系统。下面是搭建步骤及相关信息。

## nginx

### nginx详情

| 名称 | 内容 | 路径 |
| --- | --- | --- |
| nignx | 版本：nginx/1.7.10 | /usr/local/nginx/ |
| 源码目录 | 源码安装包 | /usr/local/src/nginx-1.7.10.tar.gz |
| 环境变量 | -- | /etc/profile.d/nginx.sh |
| 启动nginx文件 | nginx启动服务 | /etc/init.d/nginx |
| 启动方式 | service nginx {start\|stop\|reload\|restart\|configtest} | 无 |
| nginx主配置文件 | nginx.conf | /usr/local/nginx/conf |
| nginx网站配置目录 | 配置各个网站的nginx配置 | /usr/local/nginx/vhost |

### 安装步骤

```shell
./configure   --prefix=/usr/local/nginx   --with-pcre --with-http_ssl_module

make && make install
```

### 启动方式

启动命令：

`service nginx start|stop|reload|restart|configtest`

## php

| 名称 | 内容 | 路径 |
| --- | --- | --- |
| php | 版本：PHP 5.6.17 | /usr/local/php/ |
| 源码目录 | 源码安装包 | /usr/local/src/php-5.6.17.tar.gz |
| 环境变量 | -- | /etc/profile.d/php.sh |
| 启动nginx文件 | nginx启动服务 | /etc/init.d/php-fpm |
| 启动方式 | service php-fpm  {start\|stop\|force-quit\|restart\|reload\|status} | 无 |
| php主配置文件 | php-fpm.conf  php.ini\(装扩展\) | /usr/local/php/etc |

### 源文件位置

`/usr/local/src/php-5.6.17.tar.gz`

### 安装步骤

```shell
 ./configure  --prefix=/usr/local/php --with-config-file-path=/usr/local/php/etc --with-mysql=mysqlnd --with-mysqli=mysqlnd --with-pdo-mysql=mysqlnd --enable-inline-optimization --disable-debug --disable-rpath --enable-shared --enable-opcache --enable-fpm --with-fpm-user=www --with-fpm-group=www --with-gettext --enable-mbstring --with-iconv --with-mcrypt --with-mhash --with-openssl --enable-bcmath --enable-soap --with-libxml-dir --enable-pcntl --enable-shmop nable-sysvmsg --enable-sysvsem --enable-sysvshm --enable-sockets --with-curl --with-zlib --enable-zip --with-bz2 --with-readline --with-freetype-dir --with-jpeg-dir --with-png-dir --enable-xml --enable-mbregex --with-pcre-regex --with-gd --enable-gd-native-ttf --with-ldap --with-ldap-sasl --with-xmlrpc --disable-ipv6 --enable-intl


 make && make install
```

### 启动方式

启动命令：



`service php-fpm  {start\|stop\|force-quit\|restart\|reload\|status}\`

## mysql



mysql这里没有采用自己搭建的方式，而是直接购买了阿里云的RDS服务。

