#BFSpider
BFSpider = **Breadth-first search Spider**

**不是**boy friend spider

##程序概述：
爬虫采用广度优先策略，以**线程池**的方式实现。

TreadPoolSlot类是一个具体的线程实现，TreadPool类负责管理创建的线程，
Spider类则是一个具体的爬虫。Spider.start方法向TreadPool中添加任务，而TreadPoolSlot不停的从TreadPool的任务队列中取出任务执行


##注意事项
程序运行后会在当前目录创建一个Resource.txt文件，用于记录爬取到的资源链接，每次运行会将上一次的结果覆盖，
程序未结束前打开Resource.txt有可能还没有写入
同时也会在当前目录创建一个sys_run.log的系统运行日志文件，下次的运行结果不会覆盖之前的，会以追加的方式写入
如果设置的爬取深度不够，即使没有达到资源上限爬虫也会结束



