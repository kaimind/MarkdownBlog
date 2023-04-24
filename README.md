# MarkdownBlog

## 目标

本项目的功能类似Hugo，用于在GitHub page上写博客。目标是更简单，更灵活。

### 简单

内容只需要写markdown就可以了，不需要本地环境，不需要命令行。

### 灵活

前端使用了semantic ui和jquery，只需要修改一个index.html就可以把博客改成想要的样子。

## 原理

相当于一个单页应用。使用semantic ui在html文件里面写博客的标题，菜单，注脚等不变的框架部分。变化的内容部分，由ajax获取markdown文件，在前端使用markd.js渲染而来。所有可变内容部分都由markdown文件来编辑。

## 本地预览

本来最理想的状态是，只需要用浏览器打开本地的index.html文件就能预览。但是，ajax在获取本地的markdown文件的时候会触发跨域问题，所以，还是需要使用一个静态服务器。建议在vscode里面使用插件live server来实现。好在markdown也是在vscode里面编辑的，这就很方便。

## 写文章

博客文章的markdown文件放在static\article目录下。在该目录下新建一个xxx.md文件，然后在home.md里面添加这个文件的标题和链接，就可以了，非常简单。

如果要给文章添加分类和标签，就编辑category.md和tag.md两个文件。

## 修改外观

要修改博客的外观，就编辑index.html文件。

## 使用到的开源项目

- [Semantic UI](https://semantic-ui.com/)
- [Marked js](https://marked.js.org/)