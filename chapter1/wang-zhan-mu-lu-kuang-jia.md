* 目录框架明细

调度系统和政务用车系统都是采用一样得框架

```shell
./jiaoyun-diaodu/
├── backend     ###后台目录
│   ├── assets
│   ├── config
│   ├── controllers
│   ├── excel
│   ├── filters
│   ├── models
│   ├── runtime
│   ├── views
│   └── web
├── common     ###公共目录（相应的配置文件）
│   ├── config     ##通用的配置，这些配置将作用于前后台和命令行
│   ├── messages   ##前后台和命令行都可能用到的数据模型
│   ├── models
│   ├── pay
│   ├── util
│   └── widgets
├── console
│   ├── config
│   ├── controllers
│   ├── migrations
│   ├── models
│   └── runtime
├── environments ###初始化环境
│   ├── dev
│   └── prod     ##正式环境配置
├── frontend        ###前台的目录
│   ├── assets      ##目录用于存放前端资源包PHP类
│   ├── config      ##用于存放本应用的配置文件，包含主配置文件 main.php 和全局参数配置文件 params.php 
│   ├── controllers ##控制器
│   ├── models      ## 模型类
│   ├── runtime  
│   ├── views       ## 视图文件
│   └── web         ##Web服务器可以访问的目录（里面包含入口文件index.php）
└── vendor      ###公共目录
    ├── 2amigos
    ├── aliyuncs
    ├── behat
    ├── bin
    ├── bower
    ├── callmez
    ├── cebe
    ├── codeception
    ├── composer
    ├── crazydb
    ├── doctrine
    ├── ezyang
    ├── fzaninotto
    ├── guzzlehttp
    ├── imagine
    ├── myclabs
    ├── phpdocumentor
    ├── phpspec
    ├── phpunit
    ├── psr
    ├── sebastian
    ├── symfony
    ├── webmozart
    └── yiisoft
```



