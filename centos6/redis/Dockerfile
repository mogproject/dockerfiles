# Dockerfile for redis server
#
# using EPEL repository

FROM centos:centos6

RUN yum history new
RUN yum install -y --nogpgcheck http://ftp.riken.jp/Linux/fedora/epel/6/x86_64/epel-release-6-8.noarch.rpm
RUN yum install -y --nogpgcheck redis

EXPOSE 6379
CMD ["/usr/sbin/redis-server"]

