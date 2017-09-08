FROM waitlee/ubuntu:14.04

MAINTAINER <waitlee> liduabc2012@gmail.com

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update \
    && apt-get install -y mysql-server mysql-client\
    && rm -rf /var/lib/apt/lists/*

RUN sed -i "/max_allowed_packet/c max_allowed_packet = 1024M" /etc/mysql/my.cnf
RUN sed -i "s/bind-address/#bind-address/g" /etc/mysql/my.cnf

ADD init.sh /usr/local/bin/init.sh
RUN chmod +x /usr/local/bin/init.sh

EXPOSE 3306
CMD ["/usr/local/bin/init.sh"]