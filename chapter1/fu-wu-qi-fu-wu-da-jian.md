# 服务器搭建（centos6.8）

LNMP代表的就是：Linux系统下Nginx+MySQL+PHP这种网站服务器架构。Nginx是一个高性能的HTTP和反向代理服务器，也是一个IMAP/POP3/SMTP代理服务器。Mysql是一个小型关系型数据库管理系统。PHP是一种在服务器端执行的嵌入HTML文档的脚本语言。这四种软件均为免费开源软件，组合到一起，成为一个免费、高效、扩展性强的网站服务系统。下面是搭建步骤及相关信息。

## nginx

### nginx详情

<table>
  <tr>
    <th>名称</th>
    <th>内容</th>
    <th>路径</th>
  </tr>
  <tr>
    <td>nignx</td>
    <td>版本：nginx/1.7.10</td>
    <td>/usr/local/nginx/</td>
  </tr>
  <tr>
    <td>源码目录</td>
    <td>源码安装包</td>
    <td>/usr/local/src/nginx-1.7.10.tar.gz</td>
  </tr>
  <tr>
    <td>环境变量</td>
    <td>--</td>
    <td>/etc/profile.d/nginx.sh</td>
  </tr>
  <tr>
    <td>启动nginx文件</td>
    <td>nginx启动服务</td>
    <td>/etc/init.d/nginx</td>
  </tr>
  <tr>
    <td>启动方式</td>
    <td>service nginx {start|stop|reload|restart|configtest}</td>
    <td>---</td>
  </tr>
  <tr>
    <td>nginx主配置文件</td>
    <td>nginx.conf</td>
    <td>/usr/local/nginx/conf</td>
  </tr>
  <tr>
    <td>nginx网站配置目录</td>
    <td>配置各个网站的nginx配置</td>
    <td>/usr/local/nginx/vhost</td>
  </tr>
</table>

### 安装步骤

```shell
./configure   --prefix=/usr/local/nginx   --with-pcre --with-http_ssl_module

make && make install
```

### 启动方式

启动命令：

`service nginx start|stop|reload|restart|configtest`

## php

<table>
  <tr>
    <th>名称</th>
    <th>内容</th>
    <th>路径</th>
  </tr>
  <tr>
    <td>php</td>
    <td>版本：PHP 5.6.17</td>
    <td>/usr/local/php/</td>
  </tr>
  <tr>
    <td>源码目录</td>
    <td>源码安装包</td>
    <td>/usr/local/src/php-5.6.17.tar.gz</td>
  </tr>
  <tr>
    <td>环境变量</td>
    <td>--</td>
    <td>/etc/profile.d/php.sh</td>
  </tr>
  <tr>
    <td>启动nginx文件</td>
    <td>nginx启动服务</td>
    <td>/etc/init.d/php-fpm</td>
  </tr>
  <tr>
    <td>启动方式</td>
    <td>service php-fpm {start|stop|force-quit|restart|reload|status}</td>
    <td>---</td>
  </tr>
  <tr>
    <td>php主配置文件</td>
    <td>php-fpm.conf php.ini\(装扩展\)</td>
    <td>/usr/local/php/etc</td>
  </tr>
</table>



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

