title: 搭建Hexo blog总结
date: 2014-10-24 23:22:55
categories: hexo
---
## 搭建环境
安装环境是__*OS X Yosemite*__

## 安装hexo出错
`npm install hexo -g`命令在Mac下需要管理员权限所以就是`sudo npm install hexo -g`
## 使用pacman主题
这个主题还是挺好看的，虽然不如[light](https://github.com/hexojs/hexo-theme-light)主题的简洁，但是那个转动的头像挺有意思的，哈哈。

###使用categories功能
因为是第一次搭建个人博客，所以用了主题之后不知道这个文章是怎么到分类里面去得，按照配置文件的说明是新建`categories`文件夹到`../source`.但是在`pacman`这个文件夹下折腾了半天，崩溃，原来是在博客的根目录下得`source`文件下新建，然后新建`index.md`文件就可以了。
## 添加新浪微博widget(微博秀)
1. 去[新浪微博开放平台](http://app.weibo.com/tool/weiboshow)设置和生成微博秀代码。
2. 在`themes/pacman/layout/_widget`中新建名为`weibo.ejs`的文件，将刚才的代码直接保存到这里。
3. 在`themes/pacman/_config.yml`中，添加如下：
```markdown
widgets:
- weibo
```
刷新就可以看到了.