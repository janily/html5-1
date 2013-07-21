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

