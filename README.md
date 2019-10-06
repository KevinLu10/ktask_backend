# 班务管理系统-后端
前端是小程序，项目是：

### 一、功能介绍
主要功能有：
* 老师可以新建作业通知和接龙
* 家长阅读通知后，系统会记录已读用户
* 家长可以再接龙下面回复自己的信息
* 家长可以关注老师，这样老师发布的通知或者接龙都会通过微信通知给家长

应用场景
* 发布放假通知
    * 老师发布国庆放假通知
    * 老师转发通知到班群
    * 家长点开通知看通知
    * 老师点开通知查看有哪些家长已阅读通知
* 收集校服号码
    * 老师发布收集校服的接龙
    * 老师转发接龙到班群
    * 家长点开接龙，回复自己小孩的尺码
    * 老师点开接龙，收集家长填的小孩尺码

### 二、架构

项目有前端和后端
前端是微信小程序,[班务管理系统-小程序](https://github.com/KevinLu10/bwtask_wxa)
后端是Python+Flask+Celery+Mysql

### 三、后端代码说明

* 数据库定义在`ktask/model.py`
* 接口定义在`ktask/biz/web/*`
* 接口逻辑在`ktask/biz/clz/*`
* `kclient.py`是测试用的接口单元测试脚本

### 四、后端启动

1. 修改全局配置`ktask/config.py` 和celery配置 `ktask/celery/config.py`
2. 执行`python init_db.py`初始化数据库表结构
3. 执行`python web.py`启动项目