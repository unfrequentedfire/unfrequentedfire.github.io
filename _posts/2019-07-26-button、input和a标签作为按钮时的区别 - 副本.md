---
layout: post
title: "button、input和a标签作为按钮时的区别"
date: 2019-07-26
tag: 前端
---

首先要知道，button、a、input三个标签在加上相应的样式之后，在外观上是没有什么区别的。

那么，这三个在什么样的场景下用作按钮使用比较好呢？

### 1.button标签

通过`onclick`绑定`javascript`事件。

```css
<button>提交</button>
```



### 2.a标签

通过添加链接访问到页面中的某一个位置或另一个页面，不向后台提交数据。

```css
<a class='btn' href='#'>提交</a>
```



### 3.input标签

将表单内用户设置或选择的所有数据一并提交到后台。

```css
<input type='submit' value='提交' />
```

