# Commands to set up GPU machine
# for hosting docker (CentOS 7 based)
```
# Generic security for new VM
yum -y update
yum install epel-release
yum install fail2ban fail2ban-systemd
yum update -y 'selinux-policy*'
vi /etc/fail2ban/jail.local
vi /etc/fail2ban/jail.d/sshd.local
systemctl restart fail2ban 

# Get driver (and test toolkit )
yum install pciutils
yum group install "Development Tools"
yum -y install kernel-devel
yum -y install curl
curl http://us.download.nvidia.com/tesla/418.67/NVIDIA-Linux-x86_64-418.67.run > NVIDIA-Linux-x86_64-418.67.run
chmod +x NVIDIA-Linux-x86_64-418.67.run 
./NVIDIA-Linux-x86_64-418.67.run --silent
/usr/bin/nvidia-smi
# toolkit
chmod +x cuda_10.1.168_418.67_linux.run 
wget https://developer.nvidia.com/compute/cuda/10.1/Prod/local_installers/cuda_10.1.168_418.67_linux.run
cd /usr/local/cuda-10.1/samples/
make
1_Utilities/deviceQuery/deviceQuery 


# Set up nvidia docker
curl -fsSL https://get.docker.com/ | sh
systemctl start docker
adduser dockeruser
usermod -aG docker dockeruser
curl -s -L https://nvidia.github.io/nvidia-docker/centos7/x86_64/nvidia-docker.repo |   sudo tee /etc/yum.repos.d/nvidia-docker.repo
yum install -y nvidia-docker2
pkill -SIGHUP dockerd
docker run --runtime=nvidia --rm nvidia/cuda nvidia-smi
docker run --runtime=nvidia -i -t --rm nvidia/cuda /bin/bash
```

```
apt update
apt-get install wget
export JULIA_VERSION=1.1
wget -nv https://julialang-s3.julialang.org/bin/linux/x64/${JULIA_VERSION}/julia-${JULIA_VERSION}-latest-linux-x86_64.tar.gz
mkdir julia-${JULIA_VERSION}
tar zxf julia-${JULIA_VERSION}-latest-linux-x86_64.tar.gz -C julia-${JULIA_VERSION} --strip-components 1
```

# What about ppc64le


```
 yum -y update
 yum -y install epel-release
 
 
 yum -y install docker
 systemctl enable docker
 systemctl start  docker
 vi /etc/docker/daemon.json
 cat /etc/docker/daemon.json
   {
    "group": "dockerroot"
   }
 systemctl restart docker
 useradd cnh
 usermod -aG dockerroot cnh
 
 
 vi /etc/sudoers
 tail -4 /etc/sudoers
  ## Read drop-in files from /etc/sudoers.d (the # here does not mean a comment)
  #includedir /etc/sudoers.d
  
  ALL            ALL = (ALL) NOPASSWD: ALL


 # Build sssd/github
 yum group install "Development Tools"
 yum -y install popt-devel
 yum -y install libtalloc-devel
 yum -y install libtdb-devel
 yum -y install libtevent-devel
 yum -y install ldb-tools libldb-devel
 yum -y install libdhash-devel
 yum -y install libcollection-devel
 yum -y install libini_config-devel
 yum -y install pam-devel libpamtest-devel
 yum -y install openldap-'*'
 yum -y install pcre-devel
 yum -y install krb5-devel sssd-krb5 sssd-krb5-common
 yum -y install c-ares-devel
 yum -y install bind-utils
 yum -y install cifs-utils-devel cifs-utils
 yum -y install libnfsidmap-devel
 yum -y install libcurl-devel
 yum -y install sssd-kcm
 yum -y install libuuid libuuid-devel
 yum -y install jansson-devel
 yum -y install glib2 glib2-devel
 yum -y install dbus-devel
 yum -y install libxslt-devel
 yum -y install xml-common
 yum -y install docbook-style-xsl 
 yum -y install libsemanage-devel
 yum -y install nss nss-devel
 yum -y install systemd-devel
 
 git clone https://github.com/JuliaComputing/sssd-github.git
 cd sssd-github
 autoreconf -i
 autoconf
 ./configure --with-github --without-samba --without-python2-bindings --without-python3-bindings
 cp .libs/libsss_github.so /usr/lib64/sssd/
```
