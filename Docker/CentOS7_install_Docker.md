
```
sudo yum install -y yum-utils \
device-mapper-persistent-data \
lvm2

# 使用Docker官方软件源安装Docker
sudo yum-config-manager \
--add-repo \
https://download.docker.com/linux/centos/docker-ce.repo


# 使用阿里云镜像站安装Docker
# 如果要使用阿里云容器镜像服务，则还需要添加相应的配置文件，否则默认从Dockerhub下载容器

# sudo yum-config-manager \
# --add-repo \
# http://mirrors.aliyun.com/docker-ce/linux/centos/docker-ce.repo


sudo yum install docker-ce docker-ce-cli containerd.io -y
sudo systemctl start docker
sudo systemctl enable docker
sudo docker run hello-world
docker pull ubuntu:latest
```
