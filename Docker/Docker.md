## 什么是 Docker ？

- - -

- 开源的应用容器引擎: 开发者可以打包他们的应用以及依赖包到一个可移植的容器中，然后发布到任何流行的 Linux 机器上
- 容器是完全使用沙箱机制: 相互之间不会有任何接口
- 轻量级的操作系统虚拟化解决方案

- - -

## 传统虚拟机

![](http://cdn1.showjoy.com/images/25/25b8a602188044b2a901c829c50c6c27.png)

- - -

## Docker

![](http://cdn1.showjoy.com/images/27/279880dd31134e78bdfbe8c2373bfde7.png)

- - -

- Docker 在操作系统层面上实现虚拟化，复用本地操作系统
- 虚拟机在硬件层面实现虚拟化

- - -

## 为什么要使用 Docker ？

- - -

### 更快的交付和部署
- 一次创建或配置，可以在任意地方运行
- 开发人员通过标准镜像构建开发容器
- 运维人员直接使用该容器部署代码

- - -

### 更高效的虚拟化
- 无需额外的 hypervisor 支持
注: 虚拟机利用 hypervisor 虚拟化CPU, 内存等硬件资源，运行在 Docker 容器上的程序直接使用的是实际物理机的资源

- - -

### 更轻松的迁移和扩展
Docker 容器几乎可以运行在任意 Linux 平台上，使得应用程序迁移更方便

- - -

## 对比传统虚拟机总结：

![](http://cdn1.showjoy.com/images/54/54a392f37bd04b70848287b78545a82e.png)

- - -

## Docker 基本要素
- Docker Container
- Docker Image
- DockerFile

- - -

### Docker Image
- 只读的静态模板
- 保存容器需要的环境和应用的执行代码

- - -

### Docker Container
- 镜像的运行状态

- - -

### DockerFile
- 文件指令集，用来说明如何自动创建 Docker 镜像

- - -

### 一些指令
- docker build -t="feedit" .
- docker images
- docker run -d -P feedit
- docker ps
- docker rmi IMAGE_ID

