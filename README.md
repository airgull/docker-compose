## Jumpserver Docker-Compose

```
$ git clone https://github.com/wojiushixiaobai/docker-compose.git
$ cd docker-compose
$ cat .env
$ docker-compose up
```

build
```
$ cd docker-compose
$ cat .env
$ docker-compose -f docker-compose-build up
```
## 说明

- 默认的 config.yml 不再调用, 如果有特殊需求, 可以自己编译后挂载到容器里面即可
- .env 的变量 用在 docker-compose 里面, 可以自己看下

还有很多问题, 尽量自己调试一遍后再使用

> 如果自己编译, 可以在 docker-compose 的 environment: 处加入 Version: $Version , 取代 Dockerfile 的 ARG

## airgull 修改

- 注意创建数据库时，设置字符集， CREATE DATABASE db_name DEFAULT CHARACTER SET utf8;
- 注意配置 nginx 容器的配置文件，如果使用 configmap 配置 nginx.conf ，注意映射的路径
