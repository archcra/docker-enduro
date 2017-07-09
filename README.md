# docker-enduro
Dockerfile for enduro (http://www.endurojs.com/, https://github.com/Gottwik/Enduro)

Based on Node.js Dockerfile.

在这个文件所在的目录下，创建Docker Image：
$ docker build -t enduro:0.2 .

然后，使用这个Image:

$ docker run --rm enduro:0.2 node -v
v6.11.0

使用示例，假设当前目录下有做好的enduro工程内容：
$ docker run --rm -v `pwd`:/cms -p 6800:3000 -p 6900:5000 enduro:0.2 enduro dev

以下无效：

或者，建立一个theme:

docker run --rm -v `pwd`:/cms enduro:0.2 enduro theme  (目前这个命令不支持)
