# scrapy

### 执行流程
1. 引擎根据名字找到要执行的爬虫；通过 settings里的配置找到

2. 执行 start——requests方法那起始url 封装requests对象

3. 把req对象放到调度器中，待下载器取出使用

4. 下载器下载完后，调用回调函数


### 分布式