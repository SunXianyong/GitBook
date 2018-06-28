# Flask 入门

##  简介
Flask 是小而精的框架，如果项目的功能分支不庞大的话，推荐使用falsk。

但是，这并不是说flask只能做小项目。falsk的第三方模块有很多，完全可以通过引用第三方模块打造一个不一样的“Django”。


## 配置文件

在我们配置文件时，可以用app.config 直接配置。但是是我们常用的是写一个配置类，直接导入继承就好，灵活性高。

技术点：
- rsplit
- importlib
- getattr

## 路由系统

1. 路由系统是装饰器，且可以传参。例如：（url, endpoint, methods）
2. 如果想给装饰器再装饰一下的话，一定要加上 wraps（）。因为源码内是通过endpoint调取函数，如果自己不定义endpoint，那装饰器返回的函数名都是inner，会发生重名问题。
3. 路由系统两种编写方式： 装饰器  ，add_url_rule










## 请求和响应


## session
通过加密的cook写在用户的浏览器中
- flash
    数据临时存储

## 蓝图
1. 划分目录结构
2. url 前缀
3. 装饰器区别划分

## 上下文管理

1. 基于threading.local 实现了Local

> - 为每个线程开辟空间，使线程之间进行数据隔离
> - 应用：DBUtils中，开启连接池有两种方法，有一种就是基于它做的。

2. 请求上下文管理

> 代码流程：
> ```python
> # 1   call方法调用 wsgi_app
> # 2   wsgi_app 中，先实例化一个 ctx对象
> ctx = REquestContrxt()
> ```

3. 应用上下文管理
> 代码流程：        
> ```python
> # 1   先实例一个 app_crx 对象
> # 2   通过localStack 放到 local中
> # 3   获取时，通过localproxy + 偏函数
> ```

4. Local 作用
> 类似于threading.local的作用，但是支持了携程

5. LocalStack 作用
> 将线程对应的数据维护成栈

6. app上下文 与请求上下文 
> 用于编写离线脚本，需要的配置文件在app.configli 

7. web 运行时
    stack：[obj,]  只有一个对象



## 外部组件
1. flask-session
2. DBUtils

## wtforms
作用：生成HTML标签 + 用户请求数据进项校验   
使用：

源码：

## 扩展组件
1. flask-session
2. DBUtils
3. wtforms
4. sqlalchemy
5. flask-sqlalchemy

## falsk-sqlalchemyongoing
使用步骤：
1. 

## 多app应用
