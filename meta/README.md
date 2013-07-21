# meta元素

[W3C说明与标准](http://www.w3.org/TR/html/document-metadata.html#the-meta-element) ([中文](http://www.w3.org/html/ig/zh/wiki/HTML5/semantics#the-meta-element))

__所属分类：__
- 元数据式内容

__使用场景：__
- 如果有charset属性出现，或者如果元素的http-equiv属性在编码声明状态：在一个head元素里。
- 如果元素具有http-equiv属性并且不在在编码声明状态：在一个head元素里。
- 如果元素具有http-equiv属性并且不在在编码声明状态：在一个做为head元素子节点的noscript元素里。
- 如果name属性出现：任何期望出现元数据式内容的位置

__内容模型：__
- 空

__允许的属性：__
- 全局属性
- name
- http-equiv
- content
- charset

__简介：__

meta元素用来表示那些不能被title, base, link, style和script这些元素描述的各种元数据。<br>
meta元素可以用name属性表示文档级元数据，以http-equiv属性表示编程指示，以及charset属性用来表示HTML文档序列化为字符串而成的文件的字符编码声明。（比如为了在网络上传输或者磁盘存储）

__注：__
- name, http-equiv 和 charset三属性其一必须被声明。
- 如果name或者http-equiv被指定了，那么content属性一定要被指定，否则它必不能出现。
- 一个文档内只能指定一条含有charset属性的meta。

## 属性 name

如果meta元素的含有name属性，则标示设置文件的元数据。<br>
文件元数据表达式为：key-value。<br>
meta元素上的name属性表示key，content属性表示对应的value。<br>
如果meta元素没有content属性，那么元数据kay-value的value部分对应是空字符串。

### 属性 name

约定：注意描述内所说的“_对应该值_”是指name属性对应的value，也就是content属性的属性值

1. application-name
    * _对应该值_必须是一个简短的自由形式的字符串表示页面所代表的Web应用程序的名称。
    * 如果页面是不是一个Web应用程序，则不要使用此属性值。
    * 用户代理（浏览器）可以在用户界面中使用该属性，优先页面的title元素，因为title元素可能包括状态信息和相关页面的状态在一个特定的时刻，而不是仅仅是应用程序的名称。
    * 页面上不得有超过一个的mata元素name属性值为application-name。
2. author
    * _对应该值_必须是一个自由形式的字符串给页面的作者之一的名称。
3. description
    * _对应该值_必须是一个自由形式的字符串，它用于描述的当前页面。
    * 页面上不得有超过一个的mata元素name属性值为description。
4. generator
    * _对应该值_必须是一个自由形式的字符串，它用于标识一个用来生成文档的软件包。
5. keywords
     * _对应该值_是一组采用逗号(,)分割的单词，用来定义当前页面的关键字。


## 属性 http-equiv

当http-equiv属性在meta元素被指定，则该元素代表一种程序指令。

### content-type	

### default-style	

### refresh



