# docker-学习命令
docker 


### 1. 生成镜像
> -t 指定 镜像 名字
```bash
$ docker image build -t docker-demo .
```

### 2. 生成容器
> -p 本地端口 : 镜像端口  -it 映射当前 shell

```bash
$ docker container run -p 8080:3000 -it docker-demo /bin/bash
```

### 3. 查看容器

```bash
$ docker container ls
```

### 4. 构建

```bash
$ docker build -t <login-name>/cheers2019 .
```

### 5. 跑起来

```bash
$ docker run -it --rm <login-name>/cheers2019
```

### 6. 推到 Docker Hub上

```bash
$ docker login
$ docker push <login-name>/cheers2019
```