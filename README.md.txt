# pwn环境配置

## 1.Ubuntun安装

 本机环境配置：windowss10+vmware+ubuntu16.04

​      [ubuntu-16.04.6-desktop-amd64.iso](C:\Users\86151\Desktop\ubuntu-16.04.6-desktop-amd64.iso) （已有最新版）



![img](https://img-blog.csdn.net/20180906101935719?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2xlZV9oYW0=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

1.如果vmware设置了安装过程中自动将vmware tools安装到虚拟机中，那么安装好的虚拟机中可以使用vmware tools相关功能；而通过后一种install方式，好像是需要自己手动安装vmware tools。

2.第一种安装之后，”安装vmware tools/重新安装vmware tools”这个选项是无法点击的。第二种可以。

## 2.换源

### 1.备份原来的源

​    sudo cp /etc/apt/sources.list /etc/apt/sources_init.list2

### 2.更换源

sudo gedit /etc/apt/sources.list

#### 阿里源

deb http://mirrors.aliyun.com/ubuntu/ xenial main multiverse restricted universe
deb http://mirrors.aliyun.com/ubuntu/ xenial-backports main multiverse restricted universe
deb http://mirrors.aliyun.com/ubuntu/ xenial-proposed main multiverse restricted universe
deb http://mirrors.aliyun.com/ubuntu/ xenial-security main multiverse restricted universe
deb http://mirrors.aliyun.com/ubuntu/ xenial-updates main multiverse restricted universe
deb-src http://mirrors.aliyun.com/ubuntu/ xenial main multiverse restricted universe
deb-src http://mirrors.aliyun.com/ubuntu/ xenial-backports main multiverse restricted universe
deb-src http://mirrors.aliyun.com/ubuntu/ xenial-proposed main multiverse restricted universe
deb-src http://mirrors.aliyun.com/ubuntu/ xenial-security main multiverse restricted universe
deb-src http://mirrors.aliyun.com/ubuntu/ xenial-updates main multiverse restricted universe

## 3.安装<!--pip-->

pip 是 Python 包管理工具，该工具提供了对Python 包的查找、下载、安装、卸载的功能。

sudo apt-get install python-pip

sudo apt-get install python3-pip

## 4.pip换源

 vim ~/.pip/pip.conf（没有自建）

[global] 

index-url = https://pypi.tuna.tsinghua.edu.cn

## 5.安装pwntols

```
pip install pwntools
```



