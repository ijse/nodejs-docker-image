nodejs-docker-image
==================

本代码演示了基于Docker创建一个简单的Node.js**开发环境**。

## 代码使用方法

```shell

# 下载代码
git clone https://github.com/ijse/nodejs-docker-image.git
cd nodejs-docker-image

# 构建镜像
docker build --force-rm -t ijse/nvm .

# 运行容器
docker run -it -v /nodejs-docker-image:/workspace --name my-project -p 3000:8080 ijse/nvm
npm install && node index.js
```

于是，容器中的程序便运行起来了，访问[http://localhost:3000](http://localhost:3000)查看效果。

>**注意：**
>
> * 如果是在Windows或Mac系统下，由于Docker是运行在虚拟机里的，所以访问时`localhost`要换为虚拟机的ip地址。


## 更多内容

参照博客文章：http://www.ijser.cn/install-nvm-on-docker/


