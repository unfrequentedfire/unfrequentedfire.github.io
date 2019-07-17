## 使用手册

[Jekyll搭建个人博客](http://blog.ojx666.xyz/tags/#%E5%8D%9A%E5%AE%A2-ref)  :  我记录下了搭建博客的过程，里面详细描述了我遇到的问题和解决方法，当你遇到问题时希望对你有所帮助

#### 安装Jekyll

在安装jekyll之前，你需要先安装Ruby的开发环境，[下载](https://rubyinstaller.org/downloads/)网站推荐的版本即可（Ruby+devkit的版本，不然后面会出很多问题）

例如，我安装的是**Ruby+Devkit 2.5.X (x64)**

我第一次安装遇到很多问题，如果你也遇到问题请看我的[搭建过程](http://blog.ojx666.xyz/tags/#%E5%8D%9A%E5%AE%A2-ref)，里面有解决的方法，或请在[Issues](https://github.com/sslogan666/sslogan666.github.io/issues)里提问

![mark](http://image.ojx666.xyz/blog/20190714/qngotMW8QEde.png?imageslim)

安装jekyll（你还需要了解一下jekyll，这是[Jekyll中文文档](http://jekyllcn.com/docs/home/)，这是[官方文档](https://jekyllrb.com/docs/)，比中文文档更新及时）

> $ gem install jekyll

#### 获取博客模板

用[Git](https://git-scm.com/)工具

> $ git clone https://github.com/sslogan666/sslogan666.github.io.git

或者直接[下载博客](https://codeload.github.com/sslogan666/sslogan666.github.io/zip/master) 

#### 在本地运行博客

用cmd命令行切换到sslogan666.github.io/ 目录下， 开启本地服务 

> $ jekyll serve

在浏览器输入 [127.0.0.1:4000](127.0.0.1:4000) ， 就可以看到博客效果了。   

#### 个性化

虽然能看到博客，但博客内容都是我的，下面就来打造你自己的博客

`修改个人信息`:打开根目录下_config.yml文件，将**Basic**里的信息改成自己的

`修改头像和背景图片`：将images文件夹下，名为avatar.jpg（头像）和background-cover.jpg（背景图片）替换为你喜欢的图片

`写自己的文章`：_posts文件夹是放文章的地方，你可以先留一篇文章，其他都删除，将这篇文章的内容修改为你自己的，注意，头部信息不要更改

保存之后，再重复步骤【**在本地运行博客**】，就可以看到你自己的博客了

如果你想更多的个性化，务必了解[jekyll](http://jekyllcn.com/docs/home/)，还可以看我的[博客个性化过程](http://blog.ojx666.xyz/2019/07/jekyll%E6%90%AD%E5%BB%BA%E4%B8%AA%E4%BA%BA%E5%8D%9A%E5%AE%A22/)，里面有更多的个性化内容

至此，基本的个性化博客实现了，但博客只在本地运行，下面将其与github pages结合，让你的朋友也可以访问你的博客   

#### 让你的朋友访问你的博客

你可以先按下面步骤来，再了解[GitHub Pages](https://pages.github.com/)

在你的github里创建一个username.github.io的仓库，username指的是你的github的用户名，创建完成后，使用git push,把你本地的仓库push到你的github上username.github.io仓库下

打开浏览器访问`https://username.github.io`，首次访问，可能需要10分钟左右后，才能访问到，喝杯茶，耐心等待:grin:


## 效果预览

#### 首页和头像效果

![mark](http://image.ojx666.xyz/blog/20190714/VRzLRgjdslz0.gif)

#### 正文

![mark](http://image.ojx666.xyz/blog/20190717/BdQxyFyMinma.jpg?imageslim)

#### 关于我

![mark](http://image.ojx666.xyz/blog/20190714/P0svvjQGXHsy.jpg?imageslim)   

#### 感谢   

本博客在[**leopardpan.github.io**](https://github.com/leopardpan/leopardpan.github.io/)基础上修改的  