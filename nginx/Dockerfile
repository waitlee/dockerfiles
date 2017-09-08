FROM waitlee/ubuntu:14.04

MAINTAINER <waitlee> liduabc2012@gmail.com

ENV DEBIAN_FRONTEND noninteractive

RUN apt-get update \
    && apt-get install -y nginx
    && rm -rf /var/lib/apt/lists/*
RUN mkdir /data \
    && mkdir /data/www \
    && chown -R www-data:www-data /data

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]
