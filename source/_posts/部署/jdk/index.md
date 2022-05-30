---
title: jdk部署
categories:
  - 部署
  - jdk
tags: jdk
date: 2022-5-30 09:27:52
---

## linux环境

### 安装jdk

将下载好的linux版本的jdk通过ftp软件上传到服务器上


将下载好的jdk文件夹解压至/usr/local/jdk/目录下


然后在/etc/profile文件中添加如下内容：

```bash
export JAVA_HOME=/usr/local/jdk
export JRE_HOME=${JAVA_HOME}/jre
export CLASSPATH=.:${JAVA_HOME}/lib:${JRE_HOME}/lib
export PATH=${JAVA_HOME}/bin:$PATH
```
