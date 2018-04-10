＃docker-wordpress-nginx

Dockerfile，安装最新的wordpress，nginx，php-apc和php-fpm。

注意：非常感谢[jbfink]（https://github.com/jbfink/docker-wordpress）谁在wordpress部分做了大部分努力！

你可以查看他的[Apache版本]（https://github.com/jbfink/docker-wordpress）。

##安装

获取这个码头镜像最简单的方法是获取最新版本
来自Docker注册表：

```bash
$ docker pull eugeneware / docker-wordpress-nginx
```

如果你想自己构建图像，那么：

```bash
$ git clone https://github.com/eugeneware/docker-wordpress-nginx.git
$ cd docker-wordpress-nginx
$ sudo docker build -t =“eugeneware / docker-wordpress-nginx”。
```

##用法

在端口80上产生一个新的wordpress实例。-p 80:80将内部码头端口80映射到主机的外部端口80。

```bash
$ sudo docker run -p 80:80 --name docker-wordpress-nginx -d eugeneware / docker-wordpress-nginx
```

开始你新创建的码头。

```
$ sudo docker start docker-wordpress-nginx
```

启动docker-wordpress-nginx检查后，看看它是否启动，端口映射是否正确。这也将报告码头集装箱和主机之间的端口映射。

```
$ sudo docker ps

0.0.0.0:80 - > 80 / tcp docker-wordpress-nginx
```

您可以在主机上的浏览器中访问以下URL以开始使用：

```
http://127.0.0.1:80
```
