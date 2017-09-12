FROM waitlee/ubuntu:14.04

MAINTAINER waitlee <liduabc2012@gmail.com>

ENV DEBIAN_FRONTEND noninteractive

RUN apt-get update \
&& apt-get install -y memcached \
&& rm -rf /var/lib/apt/lists/* \
&& sed -i "/^-l /c -l 0.0.0.0" /etc/memcached.conf

USER memcache
EXPOSE 11211

CMD ["memcached"]
