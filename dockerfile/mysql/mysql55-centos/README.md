# ִ��

* �������ݾ����

```
docker run --name=dbdata -v /var/lib/mysql mysql:1.0 true
```

* ������ʼ��������mysql��ʼ���룩

```
docker run --rm=true -e MYSQL_ROOT_PASSWORD=root --volumes-from=dbdata mysql:1.0
```

* �����ػ���������

```
docker run -d --volumes-from=dbdata mysql:1.0
```