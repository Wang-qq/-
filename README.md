HTML学习总结
================
### HTML的概念
HTML全称为Hyper Text Markup Language,译为超文本标记语言。<br/>
超文本有两层含义：一是图片、音频、视频、动画、多媒体等内容，超出了文本的限制，称为超文本；二是它还可以从一个文件跳转到另一个文件，与世界各地主机的文件进行连接，即超级链接文本。<br/>
标记语言的两层含义：一是标记语言是一套标记标签；二是标记语言没有编译过程。<br/>
### 网页的head标签里表示的是页面的配置，有什么配置？
#### html5比较完整的骨架
````
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
	<meta http-equiv="Content-Type" content="text/html;charset=UTF-8">
	<meta name="Author" content="">
    <meta name="Keywords" content="厉害很厉害" />
    <meta name="Description" content="网易是中国领先的互联网技术公司，为用户提供免费邮箱、游戏、搜索
     引擎服务，开设新闻、娱乐、体育等30多个内容频道，及博客、视频、论坛等互动交流，网聚人的力量。" />
    <title>Document</title>
</head>
<body>

</body>
</html>
````
配置包括：字符集、关键词、页面描述、页面标题、IE适配、视口、iphone小图标等等。
#### 头标签内部的常见标签
* `<title>`：指定整个网页的标题，在浏览器最上方显示。
* `<base>`：为网页上的所有链接规定默认地址或默认目标。
* `<meta>`：提供有关网页的基本信息。
* `<body>`：用于定义HTML文档所要显示的内容，也称为主体标签。我们所写的代码必须放在此标签内。
* `<link>`：定义文档与外部资源的关系。
#### 编写XHTML的规范
* 所有标记的元素都要正确的嵌套，不能交叉嵌套。正确写法举例：`<h1><font></font></h1>`
* 所有的标记都必须小写。
* 所有的标签都必须闭合。
	*双标签：`<span></span>`
	*单标签：`<br>`建议写成`<br/>``<hr>`建议写成`<hr/>`，还有`<img src="URL"/>`
* 所有的属性值都必须加引号。`<font color="red"></font>`
* 搜有的属性都必须有值。`<hr noshade="noshade"/>`、`<input type="radio" checked="checked"/>`
* XHTML文档开头必须有DTD文档类型定义。
### HTML排版标签
#### 标题标签
使用`<h1>`到`<h6>`标签进行定义。具有align属性，属性值可以是：left\center\right。
#### HTML注释
`<!-- 我是html注释 -->`
#### 段落标签`<p>`
段落，是英语"paragraph"的缩写。属性`align="属性值"`：对齐方式。属性值包括left center right。
#### HTML标签等级
* **文本级标签**：`p、span、a、b、i、u、em`。文本级标签里只能放**文字、图片、表单元素**。（a标签里不能放a和input）
* **容器级标签**：`div、h系列、li、dt、dd`。容器级标签里可以放任何东西。
#### 水平分割线标签`<hr />`
水平分割线 horizontal rule <br/>
属性介绍：<br/>
* `align="属性值"`：设定线条置放位置。属性值可选择：left center right。
* `size="2"`：设定线条粗细。以像素为单位，内定为2。
* `width="500"`或`width="70%"`：设定线条长度。可以是绝对值（单位是像素）或相对值。如果设置为相对值的话，内定为100%。
* `color="#0000FF"`：设置线条颜色。
* `noshade`：不要阴影，即设定线条为平面显示。若没有这个属性则表明线条具有阴影或立体。（小声逼逼：自己试了一下没看出来有啥差别，可能测试方式不对）
#### 换行标签<br />
#### `<div>`和`<span>`标签
* **div标签**：分割，"division"。可以把标签中的内容分割成独立的区块，必须单独占据一行。div有align属性，用于设置块的位置。
* **span标签**：范围、跨度。和div的作用一致，但是不换行。
#### 内容居中标签`<center>`
此时，center代表一个标签，而不是属性值。只要在这个标签里的内容，都会居于浏览器的中间。<br />
![1](https://user-images.githubusercontent.com/66710812/167578459-0f751a6b-1866-4a2d-acc3-30f4740e0e9e.png){:height="50%" width="50%"}
