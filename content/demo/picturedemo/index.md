---
title: '图片演示文档'
date: 2026-09-17
authors: ['ljq']
image:
    preview_only: ture
weight: 3
---

首先需要将所有要用到的图片与文章放到同一个文件夹，图片格式为jpg或png

### 文件结构
```
picturedemo #文件夹
  index.md #文档文件
  cover.png #顶部背景图
  featured.png #精选图片
  picture1.png #文章中可选插入的图片
  picture2.png
  ...
```

### 封面缩略图和文章顶部背景图
featured.png只要和文档文件处于同一级文件夹中就会被自动当作文章的封面并且被自动插入到文章最开头

cover.png只要和文档文件处于同一级文件夹中就会被自动当作文章顶部的背景图（将该页往上拉到最高，此时顶部的图片就是文章顶部背景图）

如果不需要封面和文章顶部背景图只需要删除这两张图片即可

如果只需要featured.png生成文章封面但是不想该图被插入到文章开头的话需要在md文档中加入一个参数
```
title: '图片演示文档'
date: 2026-09-17
authors: ['ljq']
#上面是普通的md文档开头
#此时feature.png会自动生成为封面并且自动插入到文章开头

title: '图片演示文档'
date: 2026-09-17
authors: ['ljq']
image:
    preview_only: ture
#增加preview_only参数即可使得featured.png不插入到文章开头
#从参数字面意思也很好理解仅生成封面缩略图
```

### 文章中插入图片
![古桥](featured.jpg)
需要在md文档中插入一条代码
```
![图片描述](picture.png)
#[]中是对图片的描述，虽然我也不知道有什么用
#()中是图片的路径，若将图片放在与文档同一级的文件夹中则只需要输入名称即可
#如果将图片放在其他文件夹中需要输入具体路径，怎么输入问ai
```