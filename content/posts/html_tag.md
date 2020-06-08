---
title: "html_tag"
date: 2020-06-02T21:56:30+08:00
draft: false
---

# HTML之常用标签


## <a>
1. 什么是a标签
1. 常见单词
1. 属性
1. a的书写规范是什么
1. 代码



<a name="DA8DR"></a>
### 什么是a标签
（或称锚元素）可以创建通向其他网页、文件、同一页面内的位置、电子邮件地址或任何其他 URL 的超链接。<br />

<a name="zRL6b"></a>
### 常见单词
href:hyper reference //超级引用,超链接<br />target //目标
<a name="JWmut"></a>
### 属性
href 包含超链接指向的 URL 或 URL 片段,当值为#xxx.会指定到达IDxxx元素
```html
href="http://google.com" //使用http协议指向URL
href="https://google.com" //使用https协议指向URL
href="//google.com" //无协议指向URL,会依次使用http和https

href="/a/b/index.html" //指向根目录下的a/b/index.html
href="a/b/index.html" //指向a/b/index.html

href="javascript:alert('hello world!')"  //使用伪协议,可以制作无操作的超链接
href="emilto:1234@foxmail.com"  //指向E_mailo

id href="#user"  //跳转到指定id元素
```
target  属性指定在何处显示链接的资源。 取值为标签（tab），窗口（window） 
```html
target=_blank  //新标签页打开
target=_top //在当前页面顶层打开
target=_parent //在父框架下打开
target=_self //在当前标签下打开
```
download 此属性指示浏览器下载 URL 而不是导航到它<br />rel=noopener 该属性指定了目标对象到链接对象的关系。该值是空格分隔的[列表类型值](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Link_types)。
<a name="j5Ha3"></a>
### a的书写规范是什么
属性选择href="//google.com" //无协议网址,会重定向<br />属性为路径时,网页的跟目录是以打开http-server服务的文件夹为根目录
<a name="dnhkP"></a>
### 代码
```html
<!-- 不要双击打开html,使用 http_server . -c-1 -->
<!-- 不要双击打开html,使用 http_server . -c-1 -->
<!-- 不要双击打开html,使用 http_server . -c-1 -->
<!-- 双击打开html,会造成路径从硬盘为根目录.绝对路径会变 -->

<!-- 工具使用, yarn global add http-server 或者 yarn global  add parcel -->
<!-- 不要浪费时间工具,能用就行 -->

<body>
    <a href="http://www.baidu.com">超链接</a>

    <a href="http://www.baidu.com" target="_block">超链接</a>
    <!-- 使用新的标签页打开超链接 -->

    <a href="//baidu.com">无协议超链接</a>
    <!-- 推荐使用无协议超链接 -->

    <a href="/a/a_href.html">本地路径</a>
    <!-- 以当前http服务器为根目录-->

    <a href="a/a_href.html">本地路径</a>
    <!-- 如果使用的是http服务,那么他的路径回是开启服务的目录为根 ,http服务的根目录-->

    <a href="a/a_href.html"></a>
    <!-- 相对路径下，文件夹a -->

    <a href="index.html">链接文档</a>
    <a href="./index.html">跟下链接文档</a>
    <!-- 链接当前目录下的html -->

    <a href="javascript:alert('hello world')">javascript伪协议</a>
    <a href="javascript:;">javascript伪协议</a>
    <!-- 要想使用a标签不起到任何作用，使用空的伪协议 -->
    <a href="">会刷新页面</a>
    <a href="#">会跳到页眉页面</a>
    <a href="#XX">会跳到指定ID</a>
    <a href="mailto::jumpawaltz@foxmail.com ">邮箱</a>
    <a href="tel:24123412">电话</a>
</body>

```


<a name="KOJL0"></a>
## <table>

1. 什么是table
1. 常见单词
1. table 可以干什么
1. table的书写规范是什么
1. table 常见的样式
1. 代码


<br />

<a name="Swzyn"></a>
### 什么是table
table 就是表格
<a name="G0Ac2"></a>
### 常见单词
table //表格<br />thead //表头<br />tbody //表身<br />tfoot //表尾<br />td : table descript //单元格描述<br />th :able head //表头<br />tr :table row 行<br />

<a name="OlfNo"></a>
### table 可以干什么
将数据填写到表格容器里,展示
<a name="bezqi"></a>
### table的书写规范是什么
不用管有几行单元格.都要使用table标签包围,分别使用thead,tbody,tfoot.
<a name="qY8UD"></a>
### table 常见的样式
table-layout :auto //自动分配宽度<br />border-spacing: //表示表格之间的间隙<br />border-collapse:collapse //决定单元格之间是合并<br />

<a name="8fWks"></a>
### 代码
```html
    <table>
        <thead>
            <tr>
                <th>单词</th>
                <th>翻译</th>
            </tr>
            <!-- table row -->
            <!-- table head -->
        </thead>
        <tbody>
            <tr>
                <td>hyper</td>
                <td>超级</td>
              <!-- table descript -->
            </tr>
        </tbody>
        <tfoot></tfoot>
    </table>
```


<a name="1CfKG"></a>
## <img>

1. 什么是img
1. 常见属性
1. 代码



<a name="zfOHu"></a>
### 什么是img
发出get请求,显示图片
<a name="oMpGZ"></a>
### 常见属性
src //指向图片位置,<br />alt //图片描述<br />width //宽度 ;max-width:100% //响应式宽度
<a name="lC1oT"></a>
### 代码


```html
<img class="fit-picture" max-width="100%"
     src="/media/examples/grapefruit-slice-332-332.jpg"
     alt="Grapefruit slice atop a pile of other slices">
```

<br />

<a name="fpkV7"></a>
## 感想
知道了规范的浏览网页,不能使用双击打开,这样会使它的绝对路径发生改变,涨知识,太多我不知道的知识了.其修远兮.<br />

