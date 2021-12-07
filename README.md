# ThinkPHP-5.0.x-LTS

ThinkPHP 5.0.x 长期支持版

目前5.0.x官方已经停止支持，为持续支持上层应用（如fastadmin还是采用5.0版本），特发起相关项目（与官方采用一致的开源协议）；

类似的项目还有 3.x 的长期支持版：https://github.com/ThinkPHP-LTS/ThinkPHP-3-LTS 

另外，暂无计划对 5.1.x 版本做长期支持，未有接触到大量使用 5.1.x 版本的上层应用。

关于5.0.x版本官方生命周期的博客：https://blog.thinkphp.cn/810718 

## 关于代码起点

官方的最后发布版为 5.0.24 （ 最后下载版页面：https://www.thinkphp.cn/down/framework.html ）

目前官方git在5.0.24版本发布后，还修正了几处，主要是是针对 Redis::Set()方法强制进行了 bool类型转换。

此修正，本长期版本决定引入，原因是此处修正的原因是因为 上游的插件phpRedis变更了其API

~~~
     * This function took a single argument and returned TRUE or FALSE in phpredis versions < 4.0.0.
     *
     * @since >= 4.0 Returned int, if < 4.0 returned bool
~~~

目前新版的 redis插件会返回 int，为了跟原有的程序兼容，因此对返回值强制转换为 bool类型。

即：本发行版的起点为： https://github.com/top-think/framework/commit/a33d8847f58a978f1b19c373ca4ee796e8809ccb  

以此为起点，本支持版发行   4.0.25-0 版本

请注意：本发行版所有的代码位于 src 目录下

-----------------------------------

## ThinkPHP 5.0.x 官方手册

完全开发手册  https://www.kancloud.cn/manual/thinkphp5

快速入门  https://www.kancloud.cn/thinkphp/thinkphp5_quickstart

路由完全指南 https://www.kancloud.cn/thinkphp/route-master

控制器从入门到精通  https://www.kancloud.cn/thinkphp/controller-in-detail

掌握数据库和模型  https://www.kancloud.cn/thinkphp/master-database-and-model 

## 官方原始版本

https://www.thinkphp.cn/down/framework.html

应用项目：https://github.com/top-think/think

核心框架：https://github.com/top-think/framework/tree/master

Composer
> composer create-project topthink/think=5.0.* tp5  --prefer-dist



