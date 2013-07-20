# DOCTYPE

文档类型（DOCument TYPE, DOCTYPE），一个DOCTYPE是一种标准通用标记语言的文档类型声明，它的目的是要告诉标准通用标记语言解析器，它应该使用什么样的文档类型定义（DTD）来解析文档。

[W3C：DOCTYPE说明和标准写法](http://www.w3.org/TR/html/syntax.html#syntax-doctype)

---

## 定义和用法

`<!DOCTYPE>`声明位于文档中的最前面的位置，处于`<html>`标签之前。


### 历史遗留字符串

    <!DOCTYPE html SYSTEM "about:legacy-compat">


### HTML 4.01

该标签可声明三种 DTD 类型，分别表示严格版本（Strict）、过渡版本（Transitional）以及基于框架（Frameset）的 HTML 文档。

以下面这个`<!DOCTYPE>`标签为例：

    <!DOCTYPE html
    PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" 
    "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">

该`<!DOCTYPE>`由三部分组成，分别是：根元素，公共标识符，系统标识符

在上面的声明中，声明了文档的根元素是 html，它在公共标识符被定义为 "-//W3C//DTD XHTML 1.0 Strict//EN" 的 DTD 中进行了定义。<br>
浏览器将明白如何寻找匹配此公共标识符的 DTD。如果找不到，浏览器将使用公共标识符后面的系统标识符（URL）作为寻找 DTD 的位置。

__公共标识符格式：__

    前缀//所有者 //类型 标签描述            //语言//显示版本
    -  //W3C   //DTD XHTML 1.0 Strict   //EN //...

__公共标识符前缀类型：__

1. ISO：是"国际标准化组织"的标准
2. +：组织名称已注册
3. -：组织名称未注册


### HTML 5

HTML 4.01 中的 doctype 需要对 DTD 进行引用，因为 HTML 4.01 基于 SGML。<br>
而 HTML 5 不基于 SGML，因此不需要对 DTD 进行引用，但是需要 doctype 来规范浏览器的行为（让浏览器按照它们应该的方式来运行。）

在 HTML 4.01 中有 3 个不同的文档类型，在 HTML 5 中只有一个：`<!DOCTYPE HTML>`

