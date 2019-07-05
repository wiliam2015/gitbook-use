# 生成电子书

GitBook不仅可以生成静态网站，也可以将内容输出为电子书(ePub，Mobi，PDF)格式。

```
＃生成PDF文件
$ gitbook pdf ./ ./mybook.pdf

＃生成ePub文件
$ gitbook epub ./ ./mybook.epub

＃生成Mobi文件
$ gitbook mobi ./ ./mybook.mobi
```

## 安装ebook-convert

`ebook-convert`是生成电子书所必需的(epub，mobi，pdf)插件。

**Linux系统**

安装[Caliber应用程序](https://calibre-ebook.com/download)。

```
sudo aptitude install calibre
```
在某些Linux发行版中安装nodejs，您还需要手动创建一个nodejs软链接：

```
sudo ln -s /usr/bin/nodejs /usr/bin/node
```

**苹果OS X系统**

下载[Caliber应用程序](https://calibre-ebook.com/download)应用程序。将`calibre.app`移动到您的应用程序文件夹后，创建一个指向`ebook-convert`工具的软件链接：
```
sudo ln -s /Applications/calibre.app/Contents/MacOS/ebook-convert /usr/local/bin
```

这样就可以在任何目录下执行目录执行ebook-convert命令。



最后测试一下`ebook-convert`指令是否能正常被调用：

```
$ ebook-convert --version
ebook-convert (calibre 2.81.0)
Created by: Kovid Goyal <kovid@kovidgoyal.net>
```

大功告成！下面就可以使用`gitbook pdf ./ ./mybook.pdf` 命令把你的项目生成pdf文档了！

# 封面

所有格式电子书都可以创建封面。在安装完可以自己提供一个，或使用[autocover](https://plugins.gitbook.com/plugin/autocover)插件生成一个。

要创建封面，请在您的书的根目录下放置一个 `cover.jpg` 文件。还可以添加 `cover_small.jpg` 指定一个较小版本的封面。封面图片格式必须是 **JPEG** 文件。

一个合格的封面应遵守以下准则：
* `cover.jpg`的大小为1800x2360像素，`cover_small.jpg`为200x262像素
* 无边框
* 清晰可见的书名
* 任何重要的文本应该在小版本中可见

# 生成PDF

进入文档项目目录，输入`gitbook pdf ./ ./gitbook.pdf`

```
$ cd ~/gitbook-cn

$ gitbook pdf ./ ./gitbook.pdf
```

* pdf： 表示生成pdf格式，还有epub、mobi可选
*./ ： 表示需要生成书籍的项目根目录
*./gitbook.pdf : 表示生成书籍的名称
*如果你的书籍有多种语言，就会生成多本书籍，书籍的名称会以语言结尾
