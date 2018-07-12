## Django 

### Django 是什么？

> Django是有个大而全的web开发框架，拥有强大的模块库，帮助我们快捷开发。

### Django 的生命周期

> 先通过WSGI，WSGI先对请求体数据进行处理；然后又封装出了request。   
> 然后到中间件，diango自带的中间件有Session , scrf , 用户验证等。如果我们自己写中间件的话，一定要注意中间件的执行顺序。     
> 到视图没什么说的，都是自己的逻辑。有数据就去数据库 or redis 取出数据，渲染后发给回前端。  
> 回去的时候还是要再次通过中间件的。

### Django rest framework 提供了那些功能：
1. 路由   通过as_view 传参数进行路由分发。支持.jason渲染方式
2. 试图   给我们封装好了类，根据method配合url分发，重新封装了request
3. 版本   版本设置有三种方式，一般写在url中，直接request.version 调用 
4. 认证   写一个类，注册到认证类中。在authticate中写认证逻辑。返回元组，抛错，None
5. 权限   写一个类，注册到权限类。 在has_permission写权限逻辑。 返回 true false
6. 频率   注册到频率类。allow_request/wait 中写认证逻辑
7. 解析器 就是根据 contenType 解析请求体的数据。
8. 序列化 对数据库序列化，和校验 
9. 分页   三种方式；页码、索引、加密
10. 渲染   自带的渲染rander

### 什么是接口：


### restful 规范： 
> 就是一个规范么，遵循规范可以让我们的api 方便维护，更简洁。        
>最主要的比如说：method：就是根据get，post 什么的来进行路由分发。            
还有一些响应数据的一些格式：    
> 1. url中 要求有版本信息    
> 2. url中 要求有请求接口信息    
> 3. url    支持https    
> 4. url    遵循面向资源    
> 5.    
> 6.    

### WSGI 是什么
是一种web服务的网关接口，本质是一种
### 中间件是什么
1. 中间件本质就是在 试图执行前 OR 响应发出前 进行操作的一些类，可自定义。
2. 中间件 有5个方法  
哪五个？


### FBV 与 CBV

### rest framework框架
> 帮助我们快速开发，提供一些可直接继承的类。搭建基于restful 规范的接口。
1. 使用rest时，继承过哪些类。--都干了什么？
    - APIview
	- GenericAPIview
	- Genericviewset
	- ModelViewSet


### 序列化

### orm 提升性能的操作
- 联查
- 预先 查询

### orm 高级特性
    F Q
    偏原生sq语句
            -raw
            -extra
            -

### 断言
restfremok 里用过的断言