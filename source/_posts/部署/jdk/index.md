---
title: jdk(1.8)部署
categories:
  - 部署
  - jdk
tags: jdk
date: 2022-5-30 09:27:52
---

## linux环境

### 安装jdk

1、将下载好的linux版本的jdk通过ftp软件上传到服务器上
![jdk文件](https://raw.githubusercontent.com/XHM923/xbs/main/source/img/202205301026854.png)

2、将上传好的jdk文件夹解压至/usr/local/目录下
```bash
tar -zxvf jdk-8u161-linux-x64.tar.gz -C /usr/local/
```

使用mv命令重命名jdk1.8.0_161文件夹为jdk
```bash
mv jdk1.8.0_161/ jdk/
```
![解压后的文件目录](https://raw.githubusercontent.com/XHM923/xbs/main/source/img/202205301047664.png)

3、然后在/etc/profile文件中添加如下内容：

```bash
export JAVA_HOME=/usr/local/jdk
export JRE_HOME=${JAVA_HOME}/jre
export CLASSPATH=.:${JAVA_HOME}/lib:${JRE_HOME}/lib
export PATH=${JAVA_HOME}/bin:$PATH
```
#### 注意：JAVA_HOME的路径是你实际解压后的JDK的路径

4、输入命令使profile文件生效：

```bash
source /etc/profile
```

5、查看jdk版本

```bash
java -version
```
![](https://raw.githubusercontent.com/XHM923/xbs/main/source/img/202205301049696.png)

