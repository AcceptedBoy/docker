#FROM centos:base
FROM docker.io/centos:6.7
MAINTAINER acceptedboy <972192420@qq.com>
RUN yum install -y wget tar gcc
RUN wget http://download.redis.io/releases/redis-2.8.3.tar.gz
RUN tar xzf redis-2.8.3.tar.gz
WORKDIR /redis-2.8.3/
RUN make
RUN yum remove -y wget tar
RUN rm -f redis-2.8.3.tar.gz
EXPOSE 6379
ENTRYPOINT ["src/redis-server"]