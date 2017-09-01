# 菜单与页面
---

## 菜单
GitBook使用一个`SUMMARY.md`文件来定义文档的菜单。

`SUMMARY.md`中`[]`内的内容是标题，`()`内是文档的路径，章节和子章节用四个空格或者tab键来分级。

**简单示例**

```
# 概述
### 第一部分

* [第一部分](part1/README.md)
    * [Writing很牛](part1/README.md#writing)
    * [GitBook很牛](part1/README.md#gitbook)
* [第二部分](part2/README.md)
    * [我们喜欢社交网络](part2/README.md#feedback)
    * [更好的写作工具](part2/README.md#tools)
```

每一个章节都有一个专用的页面（part1/README.md#），并被分割成子章节。

## 区域导航

文章可以使用区域导航定位到文件的特定部分。 在md文件结尾使用`#`号加上文章内容中章节的标题就能实现区域导航

```
# 概述

### 第一部分

* [第一部分](part1/README.md)
    * [Writing很牛](part1/README.md#writing)
    * [GitBook很牛](part1/README.md#gitbook)
* [第二部分](part2/README.md)
    * [我们喜欢社交网络](part2/README.md#feedback)
    * [更好的写作工具](part2/README.md#tools)
```

## 部分

内容表可以分为由标题或水平线分隔的部分：
```
# 章节标题

这里是一些简单的介绍。

## 第一节

Markdown will dictates _most_ of your **book's structure**

## 第二节

```
# 章节标题

这里是一些简单的介绍。

## 第一节

Markdown will dictates _most_ of your **book's structure**

## 第二节
...
```

部分只是章节组，没有对应的页面，但根据不同主题，它会显示在导航中。

---

# 页面

## Markdown语法
GitBook默认使用Markdown语法编写页面。也可以选择AsciiDoc语法。

**章节文件的示例**

```
＃本章标题

这里是介绍。

## 第1节

Markdown将决定 **书的结构**

## 第2节
...

```