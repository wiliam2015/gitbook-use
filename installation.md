# GitBook安装
下面介绍在本地如何安装 GitBook，如果不需要本地调试 & 不需要获得生成的 html 文件，可以直接使用 [官网](https://www.gitbook.com/) 提供的服务。
<!-- toc -->

## 环境要求

* NodeJS(v4.0.0及以上)

## 通过NPM安装
运行下面的命令进行安装
```bash
npm install gitbook-cli -g
```
其中`gitbook-cli`是gitbook的一个命令行工具, 通过它可以在电脑上安装和管理gitbook的多个版本.

## 创建一本书
GitBook通过以下命令在当前目录创建一本书：

```nodejs
gitbook init
```
如果你想用现有的目录来创建一本书，你可以通过运行 `gitbook init ./directory`来实现




## 编辑书籍
gitbook 官方已经提供了一个本地的编辑器-[Windows版本](https://www.gitbook.com/editor/windows),[Mac版本](https://www.gitbook.com/editor/osx),[Linux版本](https://www.gitbook.com/editor/linux), 使用它可以方便的编写书籍(不需要手动的写SUMMARY.md), 并且支持windows、mac、linux 三种平台, 所以强烈建议使用编辑器编写书籍.

## 预览书籍
使用下列命令会运行一个服务器, 通过`http://localhost:4000/`可以预览书籍
```bash
gitbook serve
```
运行该命令后会在书籍的文件夹中生成一个 `_book` 文件夹, 里面的内容即为生成的 html 文件.
我们可以使用下面命令来生成网页而不开启服务器
```bash
gitbook build
```

## 打开原有书籍
例如你从github或者其他网站下载了书籍信息，需要自己手动编译书籍才可以。有的书籍有插件，所以需要在执行`gitbook build`命令之前需要执行`gitbook install`将gitbook需要的插件自动安装到书籍目录，成功后再次执行`gitbook build`就可以了