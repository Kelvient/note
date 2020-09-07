# Docker架构

开源的应用容器引擎

操作系统级虚拟化

使用C/S架构->分为服务端和客户端

使用Go语言进行开发->是目前Go语言的重量级应用




## 三个基本、核心概念

1. 镜像（image），相当于用于安装虚拟机的ISO文件
2. 容器（Container），是镜像运行时的实体，相当于虚拟机
3. 仓库（Repository），保存镜像的地方


Docker-compose定义和运行多个容器组成的系统

Swarm是Docker官方的集群管理工具

Dockerfile是镜像描述文件，每条指令构建一层


## Docker三剑客

1. Docker
2. Docker-compose
3. Swarm


## 容器的7种状态

1. created（已创建）
2. restarting（重启中）
3. running（运行中）
4. removing（迁移中）
5. paused（暂停）
6. exited（停止）
7. dead（死亡）


## 镜像的状态

1. Used（有容器实例关联）
2. Unused（无容器实例关联）
3. Dangling（被tag标记，悬空镜像）


## 零散要点

### 让普通用户使用docker

**默认情况下，Unix socket属于root用户，需要root权限才能访问。**


解决方法1:使用sudo获取管理员权限，运行docker命令

解决方法2:创建docker用户组，并将当前用户加入到docker用户组中

```
sudo groupadd docker          #添加docker用户组
sudo gpasswd -a $USER docker  #将登陆用户加入到docker用户组中
newgrp docker                 #更新用户组
docker ps                     #测试docker命令是否可以使用sudo正常使用

```

### 关于Docker stop

docker stop让容器停止运行后，没有执行docker rm命令删除容器

执行docker system df查看资源信息，RECLAIMABLE是可回收比例

docker system df -v





