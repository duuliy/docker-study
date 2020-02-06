# docker-学习命令

docker

### 1. 生成镜像

> -t 指定 镜像 名字

```bash
$ docker image build -t docker-demo .
```

### 2. 生成容器

> -p 本地端口 : 镜像端口 -it 映射当前 shell

```bash
$ docker container run -p 8080:3000 -it docker-demo /bin/bash
```

### 3. 查看容器

```bash
$ docker container ls
$ docker container ls --all
```

### 4. 构建

```bash
$ docker build -t <login-name>/cheers2019 .
```

### 5. 跑起来

```bash
$ docker run -it --rm <login-name>/cheers2019
```

### 6. 推到 Docker Hub 上

```bash
$ docker login
$ docker push <login-name>/cheers2019
```

### 7. 列出本机的所有 image 文件

```bash
$ docker image ls
```

### 8. 删除 image 文件

```bash
$ docker image rm [imageName]
```

### 9. 从仓库抓取 image 文件

```bash
$ docker image pull hello-world
```

### 10. 运行这个 image 文件

```bash
$ docker container run hello-world
```

### 11. 终止那些不会自动终止的容器

```bash
$ docker container kill [containID]
```

### 12. 删除容器

```bash
$ docker container rm [containerID]
```

### 13. 进入 koa-demo 容器

```bash
$ docker container run -p 8000:3000 -it koa-demo /bin/bash
```

### 14. 退出容器

```bash
$ exit
```

### 15. 登陆

```bash
$ docker login
```

### 16. 打标签

```bash
$ docker image tag [imageName] [username]/[repository]:[tag]
```

### 16. 发布 image

```bash
$ docker image push [username]/[repository]:[tag]
```

### 16. 启动,停止容器

```bash
$ docker container start [containerID]
$ docker container stop
```

### 16. 看日志

```bash
$ docker container logs
```

### 16. 进入正在运行的 docker 容器

```bash
$ docker container exec -it [containerID] /bin/bash
```

### 16. 拷贝正在运行容器 docker 里的代码到本地

```bash
$ docker container cp [containID]:[/path/to/file] .
```
