第一步：安装依赖

yum -y groupinstall "Development tools"
yum -y install  bzip2-devel openssl-devel ncurses-devel sqlite-devel readline-devel tk-devel gdbm-devel db4-devel libpcap-devel xz-devel zlib*

第二步：下载安装包并解压安装

wget "https://www.python.org/ftp/python/3.6.2/Python-3.6.2.tgz"

tar xvzf Python-3.6.2.tgz

mkdir /usr/local/python3 

cd Python-3.6.2

./configure --prefix=/usr/local/python3  #--enable-optimizations 为最优安装，建议使用这个参数

make && make install

第三步:建立软连接

ln -s /usr/local/python3/bin/python3.6 /usr/bin/python3

ln -s /usr/local/bin/python3/bin/pip3 /usr/bin/pip3

#ln -s /usr/local/python3/bin/python3 /usr/bin/python
