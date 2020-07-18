# Markdown_Toolkit
Markdown 编译工具 / Simple toolkit for Markdown

## 简介

基于`Pandoc`和`LaTeX`的快速markdown编译脚本工具

### Preview

|                md2art                 |             md2slide              |
| :-----------------------------------: | :-------------------------------: |
| [![article](example/article/article.png)](example/article/article.png) | [![slide](example/slide/slide.png)](example/slide/slide.png) |

## 特点

- 方便快捷：只需要在tool命令后输入源文件名和输出文件名，即可快速生成PDF文件
- 自动备份：每次编译前，都会将markdown源文件备份至`./md_backup`文件夹中，起到checkpoint的作用
- 自定义模板：可在md_template中加入自定义模板使用
- 自定义Meta信息：可在markdown文件顶部的block区域添加标题、作者、日期等信息（使用范例请参考 [example\article\article.md](example\article\article.md) 和 [example\slide\slide.md](example\slide\slide.md)）
- 自定义LaTeX命令：可在markdown文件顶部的block区域添加你想使用的LaTeX命令，如`\usepackage{}`（使用范例请参考 [example\article\article.md](example\article\article.md) 和 [example\slide\slide.md](example\slide\slide.md)）

## 安装

首先需要安装好下列软件：

- `pandoc`: [https://pandoc.org/installing.html](https://pandoc.org/installing.html)
- `texlive`: [https://www.tug.org/texlive/](https://www.tug.org/texlive/)

安装好后，请按照软件说明添加路径到`PATH`中，确保能在终端中直接执行命令`pandoc`和`xelatex`。

之后，请将本项目clone至你本地任意目录，并添加至`PATH`

```shell
git clone https://github.com/zawnpn/Markdown_Toolkit.git
echo 'export PATH=/path/to/Markdown_Toolkit:$PATH' >> ~/.bashrc 
source ~/.bashrc
```

## 使用

**1. Markdown → Article PDF**

```shell
md2art md_filename.md output.pdf
```

**2. Markdown → Slide PDF**

```shell
md2slide md_filename.md output.pdf
```

