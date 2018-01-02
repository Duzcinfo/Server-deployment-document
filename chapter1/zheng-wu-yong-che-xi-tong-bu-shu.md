
- 克隆项目  

```shell
[root@******]# git clone https://2763393126@code.aliyun.com/phpgrp/jiaoyu-zhengwu.git
Initialized empty Git repository in /mnt/jiaoyun/jiaoyu-zhengwu/.git
Password: # 输入密码


## 成功克隆代码
remote: Counting objects: 16533, done.
remote: Total 16533 (delta 3169), reused 16533 (delta 3169)
Receiving objects: 100% (16533/16533), 34.52 MiB | 14.27 MiB/s, done.
Resolving deltas: 100% (3169/3169), done.
```


* 初始化代码
进入到`jiaoyu-zhengwu`这个项目里。

```shell
# 代码初始化，就是将程序设置好的一些配置，新建的目录，以及相关的权限会重新完成，不用手动更改配置
[root@******]# php init 
Yii Application Initialization Tool v1.0

Which environment do you want the application to be initialized in?

  [0] Development
  [1] Production

  Your choice [0-1, or "q" to quit]
  
  # [0]是开发模式
  # [1]是生产模式
  这里选取1，进入生产模式。
  
  
   Your choice [0-1, or "q" to quit] 1

  Initialize the application under 'Production' environment? [yes|no] yes

  Start initialization ...

   generate frontend/web/index.php
   generate frontend/web/robots.txt
   generate frontend/config/main-local.php
   generate frontend/config/params-local.php
   generate demand/web/index-test.php
   generate demand/web/index.php
   generate demand/web/robots.txt
   generate demand/config/main-local.php
   generate demand/config/test-local.php
   generate demand/config/params-local.php
   generate yii
   generate backend/web/index.php
   generate backend/web/robots.txt
   generate backend/config/main-local.php
   generate backend/config/params-local.php
   generate console/config/main-local.php
   generate console/config/params-local.php
   generate common/config/main-local.php
   generate common/config/params-local.php
   generate cookie validation key in demand/config/main-local.php
   generate cookie validation key in backend/config/main-local.php
   generate cookie validation key in frontend/config/main-local.php
      chmod 0777 demand/runtime
      chmod 0777 demand/web/assets
      chmod 0777 backend/runtime
      chmod 0777 backend/web/assets
      chmod 0777 frontend/runtime
      chmod 0777 frontend/web/assets
      chmod 0755 yii

  ... initialization completed.
  
  ## 初始化成功
  
```
  以后代码有更新，有优化，执行`git pull `命令，输入相关密码即可。
