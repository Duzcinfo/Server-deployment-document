> web服务器这里是包含用的最多得`nginx`,`apache`

# nginx
* 配置`/usr/local/nginx/conf/nginx.conf/`,使得nginx支持读取vhost里面得虚拟机得配置信息。
```shell
# 在nginx.conf 最后加一下代码。
include vhost/*.conf;
```
*配置虚拟目录

`vhost` 目录是自己创建的。

```shell
ls  `/usr/local/nginx/conf/vhost/` 
api_jy_dd.conf   # 调度接口
api_jy_zhengwu.conf # 政务用车系统接口
admin_jiaoyun_zhengwu.conf # 政务用车系统后台
admin_jiaoyun_diaodu.conf # 调度用车后台
```

#apcahe（略）


