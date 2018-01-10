---
title: 配置JAVA环境变量
date: 2017-12-14 11:51:36
tags:
  - java
categories: 就会这么点语言
---
# JAVA 环境变量配置
---

## 修改/etc/profile文件
> 计算机下所有的用户都有权限使用这些环境变量

在***profile***文件末尾加入：

```
export JAVA_HOME=/opt/java/jdk1.8.0_131
export PATH=$JAVA_HOME/bin:$PATH
export CLASSPATH=.:$JAVA_HOME/lib/dt.jar:$JAVA_HOME/lib/tools.jar
```
<!-- more -->
修改结束后终端输入：`sudo source /etc/profile `，生效

---

## 修改.bash_profile文件
> 方法更为安全，可以把环境变量的权限控制到用户级别

在***.bash_profile***文件末尾加入:

```
export JAVA_HOME=/opt/java/jdk1.8.0_131
export PATH=$JAVA_HOME/bin:$PATH
export CLASSPATH=.:$JAVA_HOME/lib/dt.jar:$JAVA_HOME/lib/tools.jar
```

---

## 直接在shell下设置变量
> 只限于当前shell

只需在终端执行下列命令

```
export JAVA_HOME=/opt/java/jdk1.8.0_131
export PATH=$JAVA_HOME/bin:$PATH
export CLASSPATH=.:$JAVA_HOME/lib/dt.jar:$JAVA_HOME/lib/tools.jar
```
