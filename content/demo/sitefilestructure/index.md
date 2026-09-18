---
title: '网站的部分文件作用以及文件夹结构'
date: 2026-09-17
authors: ['ljq']
image:
    preview_only: ture
---
这篇文章旨在介绍该网站的部分文件作用以及文章文件夹的结构，具体文件参数如何写问ai

### 网页顶部导航栏
![daohanglan](daohanglan.png)

上图就是网页的导航栏<br>
导航栏的名称、顺序和作用通过这个文件调整"/config/_default/menus.yaml"

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
&emsp;&emsp;所有的文档以及有关的文件都在content文件夹内部，先进行大类区分，大类一般来就对应着导航栏中的块，当然也可以有一些私密文章不想展示出来，此时不需要将大类放置在导航栏和网站首页，同样可以通过网页访问，但是访问方式特殊，具体不做介绍。其次，大类文件夹中需要有一个_index.md文档，然后大类中就可以进行小类区分。最后，你的某一篇文章中的所需要的文档和图片最好是存放在同一个文件夹，这样子用起来比较方便。
```
此处使用代码块来演示文件夹结构
content
    _index.md #这个文件非常重要，这就是调整网站首页的文件
    major_category1
        _index.md #这个文件很重要，虽然我也不知道有什么用，但是很重要
        sub_category1 #小类之后并不再进行区分，所以小类文件夹中可以不需要_index.md
            260910
                index.md #注意，这是你的文档文件，他和_index不一样，前面没有下划线
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
        sub_category2
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
