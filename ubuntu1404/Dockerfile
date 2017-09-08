FROM ubuntu:14.04

MAINTAINER <waitlee> liduabc2012@gmail.com

# edit contents of /usr/sbin/policy-rc.d, to replace exit 101 by exit 0.
RUN sed -i "s/101/0/g" /usr/sbin/policy-rc.d

RUN mv /etc/apt/sources.list /etc/apt/sources.list_bak
ADD sources.list /etc/apt/sources.list

CMD ["/bin/bash"]
