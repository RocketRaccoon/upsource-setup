# Upsource setup

```bash
sudo vim /etc/security/limits.conf
#* - memlock unlimited
#* - nofile 100000
#* - nproc 32768
#* - as unlimited
sudo mkdir –p /usr/local/java
mkdir /home/user
mkdir /home/user/downloads
wget --no-cookies --no-check-certificate --header "Cookie: gpw_e24=http%3A%2F%2Fwww.oracle.com%2F; oraclelicense=accept-securebackup-cookie" http://download.oracle.com/otn-pub/java/jdk/8u91-b14/jre-8u91-linux-x64.rpm
sudo cp -r jre-8u91-linux-x64.rpm /usr/local/java
cd /usr/local/java
rpm -ivh jre-8u91-linux-x64.rpm
export JRE_HOME=/usr/local/java/jre1.8.0_91 
export PATH=$PATH:$JRE_HOME/bin 

mkdir /usr/local/mercurial
cd /usr/local/mercurial
wget --no-check-certificate https://www.mercurial-scm.org/release/centos7/RPMS/x86_64/mercurial-3.7.3-1.x86_64.rpm
rpm -ivh mercurial-3.7.3-1.x86_64.rpm

wget https://download.jetbrains.com/upsource/upsource-3.0.4346.zip
yum install unzipunzip 
sudo chmod a+x upsource-3.0.4346.zip
sudo unzip upsource-3.0.4346.zip
```
## Issues

https://youtrack.jetbrains.com/issue/UP-5686

http://askubuntu.com/questions/311438/how-to-make-tmp-executable

https://upsource-support.jetbrains.com/hc/en-us/articles/207634655-OutOfMemory-exception-How-to-increase-JVM-heap-size-for-Upsource-services-
