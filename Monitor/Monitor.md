Tags:
- 服务端 + 前端
- 单页应用
- OS_TOOLS
- MYSQL_TOOLS
- TOMCAT_MONITOR
- NGINX_MONITOR

- - -

### 服务端 + 前端 技术栈

- 服务端：Node.js、MongoDB
- 前端：React + antd

- - -

### OS_TOOLS

数据获取

- CPU: cat /proc/stat
- Disk: df -h
- Memory: free -m
- I/O: iostat -k
- Network: ifconfig
- ProcessCount: cat /proc/sys/fs/file-nr

数据采集：UDP

- - -

### MYSQL_TOOLS

数据获取

- show global status like 'com_select'
- show global status like 'com_insert'
- show global status like 'com_update'
- show global status like 'com_delete'
- show global status like 'connections'

数据采集：UDP

- - -

### TOMCAT_MONITOR

数据获取

- 程序入口：TomcatMonitor.java
- 数据库连接：DBManager.java
- 数据模型：Tomcat.java、TomcatSession.java
- 数据采集：JMXManager.java

数据采集：TCP

- - -

### NGINX_MONITOR

数据获取

- 响应时间
- 请求次数
- 平均响应时间
- ip

数据采集：HTTP

- - -

TODO

- Docker 部署
- PV、UV 监控
- 测试
- 告警