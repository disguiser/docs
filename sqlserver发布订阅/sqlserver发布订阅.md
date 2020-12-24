# 主服务器

防火墙开放1433端口
![image.gif](1.gif)
![image.png](1.png)

![image.png](2.png)

新建文件夹,设置局域网共享

![image.png](3.png)
![image.png](4.png)

启动sqlserver代理,并设置自启动

![image.png](5.png)

建个测试数据库

![image.png](6.png)
![image.png](7.png)

配置分发

![image.png](8.png)

一路下一步到快照文件夹

填写前面设置的共享目录

![image.png](9.png)

继续下一步直至完成

右键本地发布 新建发布

![image.png](10.png)
![image.png](11.png)

选事务发布,快照发布可能相当于全量备份还原,对等发布是多主复制,合并发布不明确

![image.png](12.png)

选取对象,这里只有表,正常还有别的内容,函数,存储过程什么的

![image.png](13.png)

可筛选

![image.png](14.png)

立即创建快照,正式环境还可以定时运行,节省服务器压力

![image.png](15.png)
![image.png](16.png)

设置账号密码

![image.png](17.png)

取个名

![image.png](18.png)

# 从服务器
防火墙开放1433端口,启动sqlserver代理,并设置自启动
本地订阅 右键 新建订阅,下一步

![image.png](19.png)

输入主服务器名称以及登录名密码,据说不能用IP

![image.png](20.png)
![image.png](21.png)

选第一个,第二个未跑通据说跟权限设置相关

![image.png](22.png)

新建订阅数据库

![image.png](23.png)
![image.png](24.png)
![image.png](25.png)

此处可定时获取,未尝试,目测问题不大

![image.png](26.png)

下一步,直到完成,而后可以查看同步状态

![image.png](27.png)
# 测试
![image.gif](2.gif)
