---
title: '网站的部分文件作用以及文件夹结构'
date: 2026-09-17
authors: ['ljq']
image:
    preview_only: ture
weight: 2
---
这篇文章旨在介绍该网站的部分文件作用以及文章文件夹的结构，具体文件参数如何写问ai

### 首页导航栏
![daohanglan](daohanglan.png)

上图就是网站首页的导航栏<br>
导航栏的名称、顺序和作用通过这个文件调整"/config/_default/menus.yaml"<br>
也可以写多级导航栏，但是比较复杂，此处不做具体介绍

### 网站首页
网站首页和导航栏有非常强的关联性！<br>
网站首页的结构通过这个文件调整"/content/_index.md"

### 文章底部作者栏
作者的信息存放在"/data/authors"中，每一个作者需要单独写一个yaml<br>
作者的照片存放在"/asset/media/authors"中，使用png或jpg格式

### 其他需要微调的文件
"/config/_default"中的文件很重要，如何调整问ai即可

### 文章结构
&emsp;&emsp;首先先介绍文档和文章的区别（个人定义😁），文档就是在vscode（其他编译器）中写的.md文件，文章就是经过编译后的.md文档，在网页上能够点开来看的就称作文章。<br>
&emsp;&emsp;所有的文档以及有关的文件都在content文件夹内部，首先需要区分“分支包”和“叶子包”，网站就像树一样，可以有很多分支，分支之上还能继续有分支，分到最末端就是叶子也就是文章，那么这就引出了“分支包”和“叶子包”的概念，每一个文件夹都是一个包，每一个“分支包”文件夹中都需要有一个_index.md文档，hugo会根据该文档决定如何渲染该网页，每一个“叶子包”中都包含有每一篇文章所需要的所有素材（包括但不限于文档文件index.md和图片文件）。说简单点就是content文件夹内部需要进行大类区分，也就是分支，所以在content中需要有_index.md，此时大类中还可以进行小类区分，所以大类文件夹中需要有_index.md，可以重复该操作，直到最后不再进行分类开始制作文章时便不再需要_index.md，此时需要的是文档文件index.md。一般来说大类就是一级导航栏，之后的分支就可以写成多级导航栏，不做多级导航栏也可以单独访问小类网页，但是访问方式比较特殊，不做具体介绍。

```
此处使用代码块来演示文件夹结构
content
    _index.md # <---渲染网站首页的文件
    major_category1 # <---分支包
        _index.md # <---用来渲染分支网页的文件
        sub_category1 # <---分支包
            _index.md # <---用来渲染分支网页的文件
            260910 # <---叶子包，单独存放一篇文章的所有素材
                index.md # <---注意，这是你的文档文件，他和_index不一样，前面没有下划线
                cover.png
                featured.png
                picture1.png
                picture2.png
            260915
                index.md
                cover.png
                featured.png
                picture1.png
                picture2.png
        sub_category2 # <---分支包
            _index.md# <---用来渲染分支网页的文件
            260910
                index.md
                cover.png
                featured.png
                picture1.png
                picture2.png
            260915
                index.md
                cover.png
                featured.png
                picture1.png
                picture2.png
    major_category2
        _index.md
        sub_category1
        sub_category2
    major_category3
    ...
```
