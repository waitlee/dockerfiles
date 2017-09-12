FROM waitlee/ubuntu:14.04

MAINTAINER <waitlee> liduabc2012@gmail.com

ENV DEBIAN_FRONTEND noninteractive

RUN apt-get update

RUN apt-get install -y mongodb

RUN sed -i "/^bind_ip /c bind_id = 0.0.0.0" /etc/mongodb.conf \
&& sed -i "/^#port /c port = 27017" /etc/mongodb.conf

RUN mkdir -p /data/db \
&& chmod 755 /data/*

RUN rm -rf /var/lib/apt/lists/*

EXPOSE 27017

CMD ["/usr/bin/mongod"]