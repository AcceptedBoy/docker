FROM docker.io/centos:6.7
MAINTAINER acceptedboy <972192420@qq.com>
RUN yum install -y mysql-server mysql
RUN rpm -qi mysql-server
RUN service mysqld start &&\
 mysql -h localhost -u root &&\
 mysql -e "GRANT ALL PRIVILEGES ON *.* TO 'root'@'%' IDENTIFIED BY 'root' WITH GRANT OPTION;" &&\
 mysql -e "FLUSH PRIVILEGES;" &&\
 mysqladmin -u root password 'root'
CMD ["/usr/bin/mysqld_safe"]
EXPOSE 3306