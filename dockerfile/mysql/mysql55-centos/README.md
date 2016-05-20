# 执行

* 镜像数据卷加载

```
docker run --name=dbdata -v /var/lib/mysql mysql:1.0 true
```

* 容器初始化（设置mysql初始密码）

```
docker run --rm=true -e MYSQL_ROOT_PASSWORD=root --volumes-from=dbdata mysql:1.0
```

* 容器守护进程启动

```
docker run -d --volumes-from=dbdata mysql:1.0
```