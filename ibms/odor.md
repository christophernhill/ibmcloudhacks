# Set up base with Docker
```
yum -y update
/sbin/shutdown -r now
yum install -y yum-utils device-mapper-persistent-data lvm2
yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo
yum install docker-ce
systemctl start docker.service
systemctl enable docker.service
```


# Docker file
```
# Create image
#  docker build -t oodond -f centosood.Dockerfile .
#
# Run image
#  docker run -i -t --rm -p 80:80 -p 443:443 --cap-add SYS_ADMIN -e "contianer=docker" -v /sys/fs/cgroup:/sys/fs/cgroup:ro --tmpfs /run --tmpfs /run/lock oodond /usr/sbin/init

FROM centos:centos7

RUN yum -y install centos-release-scl
RUN yum -y install https://yum.osc.edu/ondemand/1.6/ondemand-release-web-1.6-1.el7.noarch.rpm
RUN yum -y install openssh-server

COPY COPY/etc/yum.repos.d/CentOS-SCLo-sclo.repo /etc/yum.repos.d/CentOS-SCLo-sclo.repo

RUN yum -y install ondemand

RUN systemctl enable httpd24-httpd
RUN systemctl enable sshd

EXPOSE 80
EXPOSE 443

RUN adduser -p '$6$ccQO/iLq$0lleoURX7HuJYbBkq.QX/UhuNaThu8V2J0XdYiJaB8Vzo.ypr1tKlWvhNzp3TWOfjVN8eM1IkjVt.llICQo/f1' user

RUN scl enable ondemand -- htpasswd -b -c /opt/rh/httpd24/root/etc/httpd/.htpasswd user password

RUN mkdir -p /etc/ood/config/apps/shell
RUN ( echo "DEFAULT_SSHHOST=127.0.0.1" > /etc/ood/config/apps/shell/env )
```


