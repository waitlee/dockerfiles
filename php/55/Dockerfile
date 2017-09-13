FROM waitlee/ubuntu:14.04

MAINTAINER waitlee <liduabc2012@gmail.com>

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update \
    && apt-get install -y curl \
    php5-fpm \
    php5-cli \
    php5-mysql \
    php5-curl \
    php5-mcrypt \
    php5-memcache \
    php5-memcached \
    php5-sqlite \
    php5-redis \
    php5-mongo \
    php5-json


RUN rm -rf /var/lib/apt/lists/*
RUN sed -i '/daemonize /c daemonize = no' /etc/php5/fpm/php-fpm.conf
RUN sed -i "/^listen /c listen = 0.0.0.0:9000" /etc/php5/fpm/pool.d/www.conf
RUN sed -i 's/^listen.allowed_clients/;listen.allowed_clients/' /etc/php5/fpm/pool.d/www.conf

RUN mkdir /data \
    && mkdir /data/www \
    && chown -R www-data:www-data /data

EXPOSE 9000

CMD ["php5-fpm"]