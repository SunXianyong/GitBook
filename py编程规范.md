## 撸代码好习惯
1. 命名：
    > 类 - 可以用驼峰命名   
其他 - 用小写与下划线（包括文件名，项目名）

2. url：
    > 空行分类  
    $结尾符号必须加     
    结尾加一个^$ 

3. 注释：
    > py文件开头要有注释    
    类有注释

4. view函数 
    > 试图内的操作要加 try 

5. BaseResponse   
    > 自定义一个返回dict的类，方便操作

6. 数据库操作：
    > 只要是原子性操作必须要加上 事物

7. 其他规则
    > 简单逻辑往上放

8. 模块导入顺序注意
    > 内置-----框架-----自定义