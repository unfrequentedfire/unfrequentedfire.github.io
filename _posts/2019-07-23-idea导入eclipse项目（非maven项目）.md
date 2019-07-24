---
layout: post
title: "idea导入eclipse项目（非maven）"
date: 2019-07-23
tag: 博客
---

### 1.从svn导入项目

首先从svn仓库或者其它类型仓库checkout出eclipse项目。这是一个strust项目

![1563842358320](https://github.com/unfrequentedfire/myblog_image/blob/master/jekyll/1563842358320.png?raw=true)

选择模板，默认1.8

![1563842439021](https://github.com/unfrequentedfire/myblog_image/blob/master/jekyll/1563842439021.png?raw=true)

一路next

![1563842770637](https://github.com/unfrequentedfire/myblog_image/blob/master/jekyll/1563842770637.png?raw=true)

jar包提示

![1563842810750](https://github.com/unfrequentedfire/myblog_image/blob/master/jekyll/1563842810750.png?raw=true)

选择jdk版本

![1563842847508](https://github.com/unfrequentedfire/myblog_image/blob/master/jekyll/1563842847508.png?raw=true)

一直next，直到完成。

本地项目的文件会发现多了2个文件，不影响使用

![1563842961813](https://github.com/unfrequentedfire/myblog_image/blob/master/jekyll/1563842961813.png?raw=true)

### 2.开始设置

File——Project Structure

![1563843065930](https://github.com/unfrequentedfire/myblog_image/raw/master/jekyll/1563843065930.png)

选择**Project**，确认jdk版本

![](https://github.com/unfrequentedfire/myblog_image/raw/master/jekyll/1563843147832.png)

**paths**设置

![](https://github.com/unfrequentedfire/myblog_image/raw/master/jekyll/1563843356139.png?raw=true)

![](https://github.com/unfrequentedfire/myblog_image/blob/master/jekyll/1563843433678.png?raw=true)

**Modules**——**Dependencies**设置

​	选中你的项目名称

![](https://github.com/unfrequentedfire/myblog_image/raw/master/jekyll/1563843530150.png)

删除两个lib包，一般只有一个，然后手动添加项目所有jar包

![](https://github.com/unfrequentedfire/myblog_image/raw/master/jekyll/1563843614165.png)

![](https://github.com/unfrequentedfire/myblog_image/raw/master/jekyll/1563843825142.png)

![](https://github.com/unfrequentedfire/myblog_image/raw/master/jekyll/1563843867715.png)

还是Modules，点击web，这里有个警告，点击它！

![](https://github.com/unfrequentedfire/myblog_image/raw/master/jekyll/1563844001988.png)

发现有jar包错误，点Fix添加所有！

![](https://github.com/unfrequentedfire/myblog_image/raw/master/jekyll/1563844152508.png)

恢复成功

![](https://github.com/unfrequentedfire/myblog_image/raw/master/jekyll/1563844207504.png)

### 3.配置项目启动tomcat

添加配置

![1563844278029](https://github.com/unfrequentedfire/myblog_image/blob/master/jekyll/1563844278029.png?raw=true)

选中Tomcat

![](https://github.com/unfrequentedfire/myblog_image/blob/master/jekyll/1563844325700.png?raw=true)

选中Deployment，选择右边的＋号，添加我们的Artifact

![1563844392007](https://github.com/unfrequentedfire/myblog_image/blob/master/jekyll/1563844392007.png?raw=true)

Application context配好，一般是项目名称（全小写）

![](https://github.com/unfrequentedfire/myblog_image/raw/master/jekyll/1563844505718.png)

### 4.配置完成，启动！！

先不急运行，先把导入的项目重新编译下

![1563844653259](https://github.com/unfrequentedfire/myblog_image/raw/master/jekyll/1563844653259.png)

![1563844712544](https://github.com/unfrequentedfire/myblog_image/blob/master/jekyll/1563844712544.png?raw=true)

有点小尴尬，这里报错，提示javax.servlet.http包不存在，这里是因为没有导入tomcat相关的jar包

依次点击File—Project Structure—Modules—Dependencies—选择小+号

![1563844960392](https://github.com/unfrequentedfire/myblog_image/blob/master/jekyll/1563844960392.png?raw=true)

![1563845018752](https://github.com/unfrequentedfire/myblog_image/raw/master/jekyll/1563845018752.png)

再重新编译下，成功！

![1563845123605](https://github.com/unfrequentedfire/myblog_image/raw/master/jekyll/1563845123605.png)

运行，启动！成功！

![1563845870987](https://github.com/unfrequentedfire/myblog_image/raw/master/jekyll/1563845870987.png)

