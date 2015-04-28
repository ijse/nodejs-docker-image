nodejs-docker-image
==================

本代码演示了基于Docker创建一个简单的Node.js**开发环境**。

## 代码使用方法

```shell

# 下载代码
git clone https://github.com/ijse/nodejs-docker-image.git
cd nodejs-docker-image

# 开发环境
## 构建镜像
docker build --force-rm -t ijse/nvm-dev -f ./Dockerfile_dev .

## 运行容器
docker run -it -v /nodejs-docker-image:/workspace --name my-project -p 3000:8080 ijse/nvm
## 此时会启动进入容器内的bash提示符，在这里可以安装程序依赖（对于容器平台），及启动调试程序
npm install && node index.js

# 生产环境
## 构建镜像
docker build --force-rm -t ijse/nvm -f ./Dockerfile .

## 运行容器
docker run --name my-project ijse/nvm
```

于是，容器中的程序便运行起来了

>**注意：**
>
> * 如果是在Windows或Mac系统下，由于Docker是运行在虚拟机里的，所以访问时`localhost`要换为虚拟机的ip地址。
> * 可以通过`docker inspect <container_id>`来获取运行的container的ip和端口信息


## 更多内容

参照博客文章：http://www.ijser.cn/install-nvm-on-docker/


