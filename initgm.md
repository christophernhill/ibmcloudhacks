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
