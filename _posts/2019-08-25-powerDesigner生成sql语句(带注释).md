---
layout: post
title: "powerDesigner生成sql语句(带注释)"
date: 2019-08-25
tag: powerDesigner
---

### 1 设置ColumnComment

选择database->edit current dbms-->Column-->ColumnComment将value改成

```sql
[%OWNER%?[.O:[execute ][exec ]]sp_addextendedproperty [%R%?[N]]'MS_Description', 
   [%R%?[N]]%.q:COMMENT%,
   [%R%?[N]]'user', [%R%?[N]]%.q:OWNER%, [%R%?[N]]'table', [%R%?[N]]%.q:TABLE%, [%R%?[N]]'column', [%R%?[N]]%.q:COLUMN%
:declare @CurrentUser sysname
select @CurrentUser = user_name()
[.O:[execute ][exec ]]sp_addextendedproperty [%R%?[N]]'MS_Description', 
   [%R%?[N]]%.q:COMMENT%,
   [%R%?[N]]'user', [%R%?[N]]@CurrentUser, [%R%?[N]]'table', [%R%?[N]]%.q:TABLE%, [%R%?[N]]'column', [%R%?[N]]%.q:COLUMN%
]
```

![](https://raw.githubusercontent.com/unfrequentedfire/myblog_image/master/jekyll/20190822084653.png)

### 2 解决comment为空时不能生成注释

![](https://raw.githubusercontent.com/unfrequentedfire/myblog_image/master/jekyll/1566435092004.png)

![](https://raw.githubusercontent.com/unfrequentedfire/myblog_image/master/jekyll/20190822085412.png)

勾上Generate name in empty comment

### 3 测试

表结构如下：

![](https://raw.githubusercontent.com/unfrequentedfire/myblog_image/master/jekyll/20190821175219.png)

生成sql加注释

![](https://raw.githubusercontent.com/unfrequentedfire/myblog_image/master/jekyll/20190822141953.png)

