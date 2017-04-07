## 监控系统设计

- - -

主要涉及三个层面的监控：
- 硬件层面：CPU 利用率、磁盘、I/O、网卡、内存、线程数
- 平台层面：Tomcat、Nginx、MySQL
- 软件层面：PV、UV、其他业务需求

- - -

整体结构：

![](http://cdn1.showjoy.com/images/01/01601498610b439f8cc2562830f41b0b.png)

- - -

硬件信息采集结构：

![](http://cdn1.showjoy.com/images/bf/bf515ebc5dba44bd9ff88d8b221ae8fd.png)

- - -

Tomcat 信息采集结构：

![](http://cdn1.showjoy.com/images/63/63ba118df61e47fdb5254548b9bb990b.png)

- - -

Nginx 信息采集结构：

![](http://cdn1.showjoy.com/images/14/142970c28e2a4b0ab17d5e2803dbae10.png)

- - -

TODO

- Docker 部署
- PV、UV 监控
- MySQL 监控
- 权限控制
- 测试
- 告警