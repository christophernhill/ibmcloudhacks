# Base AMI
```
CentOS Linux 7 x86_64 HVM EBS ENA 1901_01-b7ee8a69-ee97-4a49-9e68-afaee216db2e-ami-05713873c6794f575.4 (ami-074e2d6769f445be5)
aws-marketplace/CentOS Linux 7 x86_64 HVM EBS ENA 1901_01-b7ee8a69-ee97-4a49-9e68-afaee216db2e-ami-05713873c6794f575.4
```

https://aws.amazon.com/marketplace/pp/Centosorg-CentOS-7-x8664-with-Updates-HVM/B00O7WM7QW

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


