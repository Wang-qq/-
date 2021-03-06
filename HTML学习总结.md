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
![1](https://user-images.githubusercontent.com/66710812/168278893-67662205-eb5e-492b-9a5a-5fcfcf7ef75e.jpg)
### 字体标签
#### 特殊字符（转义字符）

|特殊字符|描述|字符的代码|
|:------:|:--:|:-------:|
| |空格符|`&nbsp;`|
|<|小于号|`&lt;`|
|>|大于号|`&gt;`|
|&|和号|`&amp;`|
|￥|人民币|`&yen;`|
|©|版权|`copy;`|
|®|注册商标|`&reg;`|
|°|摄氏度|`&deg;`|
|±|正负号|`&plusmn;`|
|x|乘号|`&times;`|
|÷|除号|`&divide;`|
|²|平方|`&sup2;`|
|³|立方|`&sup3;`|

#### 下划线、中划线、斜体
* `<u>`:下划线标记
* `<s>`或`<del>`:中划线标记（删除线）
* `<i>`或`<em>`:斜体标记
#### 粗体标签`<b>`或`<strong>`（已废弃）
#### 上标`<sup>`下标`<sub>`
### 超链接
#### 超链接的三种形式
* 外部链接：链接到外部文件
`<a href="01页面.html">点击进入另一个文件</a>`
a是英文"anchor"，“锚”的意思；href(hypertext reference),“超文本地址”。
* 锚链接
给链接起一个名字，作用是再本页面或者其他页面的不同位置进行跳转。`<a href="name1">回到顶部</a>`
* 邮件链接
代码举例`<a href="mailto:xxx@163.com">点击进入我的邮箱</a>`
#### 超链接的属性
* `href`:目标URL
* `title`:鼠标悬停文本
* `name`:主要用于设置一个锚点的名称
* `target`:告诉浏览器用什么方式来打开浏览器页面。"target"属性有以下几个值：
	* `_self`:在同一个页面中显示（默认值）
	* `_blank`:**在新的窗口中打开**
	* `_parent`:在父窗口中显示
	* `_top`:在顶级窗口中显示
#### 分清楚img和a标签各自的属性
* 区别如下：
	`<img src="1.jpg" />`
	`<a href="1.html"></a>`
* a是一个文本级标签
### img标签简介
#### 插入图片的方式
* 图片的相对路径
两个标记`.`和`..`分别表示当前目录和上一层目录。注意：`..`要么不写，要么写在开头。相对路径的好处：站点不管拷贝到哪里，文件和图片的相对路径关系都是不变的。相对路径使用有一个前提，就是网页文件和图片必须在一个服务器上。
* 图片的绝对路径
	* 以盘符开始的绝对路径
	`<img src="C:\Users\qianguyihao\Desktop\html\images\1.jpg">`
	* 网络路径
	`<img src="http://img.smyhvae.com/20200122_200901.png">`
#### img标签的其他属性
* width、height属性
width和height，在HTML5中的单位是CSS像素，在HTML4中既可以是像素，也可以是百分比。可以只指定width和height中的一个值，浏览器会根据原始图像进行缩放。
* Alt属性
当图片不能正常显示的时候，代替图片显示的内容。alt是alternate“替代”的意思，表示替换资源。
* title属性
提示性文本，鼠标悬停时出现的文本。
* align属性
图片和周围文字的相对位置。属性取值可以是：bottom（默认）、center、top、left、right。默认情况下，文字在图片的底部。
### 列表标签`<ul>、<ol>、<dl>`
* 无序列表`<ul>`，无序列表中的每一项都是`<li>`
	* ul:unordered list,"无序列表"的意思
	* li:list item,"列表项"的意思
	* li不能单独存在，必须包裹在ul里面，但是li里面什么都能放
	* `type="属性值"`。属性值可以选：`disc`（实心圆点，默认），`square`（实心方点),`circle`（空心圆）
	* 列表之间是可以嵌套的
* 有序列表`<ol>`，里面的每一项都是`<li>`
	* ol:ordered list
	* `type="属性值"`。属性值可以是1（阿拉伯数字，默认）、a、A、i、I。结合start属性表示从几开始。
* 定义列表`<dl>`
	* dl:definition list，没有属性，dl的子元素只能是dt和dd。
		* dt:definition title，列表的标题，这个标签是必须的
		* dd:definition description，列表的列表项，如果不需要，可以不加
	* dt、dd只能在dl里面，dl里面只能有dt、dd
	* dd是描述dt的
	* dt、dd都是容器级标签，想放什么都可以
### 表格标签`<table>`
* 一个表格`<table>`是由每行`<tr>`组成的，每行是由每个单元格`<td>`组成的
* `<table>`属性
	* `<border>`：边框。像素为单位
	* `<style="border-collapse:collapse;">`：单元格的线和表格的边框的线合并（表格的两边框合并为一条）
	* `width`：宽度。像素为单位
	* `height`：高度。像素为单位
	* `boedercolor`：表格的边框颜色
	* `align`：表格的水平对齐方式。属性值可以填：left right center。注意：这里不是设置表格里内容的对齐方式，如果想设置表格里内容的对齐方式，要对单元格标签`<td>`进行设置
	* `cellpadding`：单元格内容到边的距离，像素为单位。，默认情况下，文字是紧挨着左边那条线的，即默认情况下的值为0.注意不是单元格内容到四条边的距离，而是到一条边的距离，默认是与左边那条线的距离。如果设置属性`dir="rtl"`，那就是内容到右边那条线的距离
	* `cellspacing`：单元格和单元格之间的距离（外边距），像素为单位。默认情况下的值为0
	* `bgcolor="#99cc66"`：表格的背景颜色
	* `background="路径src/..."`：背景图片。背景图片的优先级大于背景颜色
	* `bordercolorlight`：表格的上、左边框，以及单元格的右、下边框的颜色
	* `bordercolordark`：表格的右、下边框，以及单元格的上、左边框的颜色。这两个属性的目的是为了设置3D效果
	* `dir`：共有属性，单元格内容的排列方式（direction）。可以取值：`ltr`:从左到右（left to right，默认），`rtl`：从右到左（right to left）
* `<tr>`行属性
	* `dir`：共有属性，设置这一行单元格内容的排列方式。可以取值：
		* ltr:从左到右
		* rtl：从右到左
	* `bgcolor`：设置这一行单元格的背景色。没有background属性，无法设置这一行的背景图片，如果非要设置，可以使用css来实现
	* `height`：一行的高度
	* `align="center"`：一行的内容水平居中显示，取值：left center right
	* `valign="center"`：一行的内容垂直居中，取值：top middle bottom，默认就是居中的，我也不知道middle还是center是有用的
* `<td>`单元格属性
	* `align`：内容的横向对齐方式。属性值可以是：left center right。如果想让每个单元格的内容都居中，这个属性太麻烦，可以使用css来解决
	* `valign`：内容的纵向对齐方式。属性值可以是：top middle bottom
	* `width`：绝对值或者相对值（%）
	* `height`：单元格的高度
	* `bgcolor`：设置这个单元格的背景色
	* `background`：设置这个单元格的背景图片
* 单元格的合并
	* `colspan`：横向合并。例如`colspan="2"`表示当前单元格在水平方向上要占据两个单元格的位置
	* `rowspan`：纵向合并。例如`rowspan="2"`表示当前单元格在垂直方向上要占据两个单元格的位置
* `<th>`：加粗的单元格
相当于`<td>`+`<b>`,属性同`<td>`
* `<caption>`：表格的标题
	* 使用时和`<tr>`标签并列
	* 属性：`align`，表示标题相对于表格的位置。属性值可以是：left center right top bottom
* `<thead> <tbody> <tfoot>`标签
	* 如果写了这三个标签，那么这三个部分**代码顺序可以任意**，浏览器显示的时候还是按照thead、tbody、tffot的顺序依次来显示内容。如果不写thead、tbody、tfoot，那么浏览器解析并显示表格内容的时候是按照代码从上到下的顺序来显示
	* 当表格的内容非常大的时候，如果用了这三个标签，那么**数据可以边获取边显示**。如果不写，则必须等表格的全部内容从服务器获取完成才能显示出来。
### 框架标签及内嵌框架`<iframe>`
一个网页中显示多个页面。之前没用到，先不介绍了。
### 表单标签`<form>`
表单标签用于与服务器交互。表单就是收集用户信息的，就是让用户填写、选择的。
* 属性
	* `name`：表单的名称，用于js来操作或控制表单时使用
	* `id`：表单的名称，用于js来操作或控制表单时使用
	* `action`：指定表单数据的处理程序，一般是PHP，如：action="login.php",表单将提交到哪里
	* `method`：表单数据的提交方式，一般取值：get（默认）和post，表示用什么http方法提交，**两种提交方式的区别如下：**
		* GET方式：将表单数据以"name=value"的形式追加到action指定的处理程序后面，两者间用"?"隔开，每一个表单的"name=value"间用'&"隔开。**特点**：只适合提交少量信息，并且不太安全（不要提交敏感数据）、提交的数据类型只限于ASCII字符。
		* POST方式：将表单数据直接发送（隐藏）到action指定的处理程序。POST发送的数据不可见。action指定的处理程序可以获取到表单数据。**特点**：可以提交海量信息，相对来说安全一些，提交的数据格式时多样的(word、excel、rar、img)。
#### `<input>`输入标签（文本框）
用于接收用户输入。
`<input type="text">`
**属性**
* `type="属性值"`:文本类型。属性值可以是：
	* `text`:默认
	* `password`:密码类型
	* `radio`：单选按钮，名字相同的按钮作为一组进行单选，天生不互斥，如果想互斥，必须有相同的name属性。在多个单选框的input标签中，name的属性值可疑相同，但是**id的属性值必须是唯一的**
	* `checkbox`:多选按钮，name属性值相同的按钮作为一组进行选择
	* `checked`：将多选按钮或单选按钮默认处于选中状态。当`<input>`标签设置为`type="radio"`或者`type="checkbox"`属性时，可以使用这个属性。属性值也是checked，可以省略。
	* `hidden`：隐藏框，在表单中包含不希望用户看见的信息
	* `button`：普通按钮，结合js代码一起服用，效果更佳
	* `submit`:提交按钮，传送当前表单的数据给服务器或者其他的程序处理。这个按钮不需要写value就会自动有“提交”文字。真的有提交功能，点击按钮后，表单就会被提交到form标签的action属性中指定的那个页面去
	* `reset`：重置按钮。清空当前表单的内容，并设置为最初的默认值
	* `image`：图片按钮。和提交按钮的功能完全一致，只不过图片按钮可以显示图片
	* `file`：文件选择框。如果要限制上传文件的类型，需要js配合完成。对上传的文件进行安全检查：一是扩展名的检查，二是文件数据内容的检查
* `value="内容"`:文本框中的默认内容（已经被填好了的）
* `size="50"`：文本框内可以显示50个字符。一个英文、一个中文都算一个字符。**size属性值的单位是字符不是像素**
* `readonly`:文本框只读不能编辑。google浏览器，光标点不进去；IE浏览器光标可以点进去，但是文字不能编辑
* `disabled`：文本框只读不能编辑。光标点不进去，属性值可以不写
#### `<select>`下拉列表标签
`<select>`标签里面的每一项用`<option>`表示。select就是“选择”，option就是“选项”。select标签和ul、ol、dl一样，都是组标签
* `<select>`标签的属性
	* `multiple`：对下拉列表中的选项进行多选。可以写成`multiple=""`,也可以写成`multiple="multiple"`
	* `size="3"`:如果属性值大于1，则列表为滚动视图。默认属性值为1，即下拉视图
* `<option> `标签的属性
	* `selected`：预选中。没有属性值。
#### `<textarea>`标签：多行文本输入框
text就是“文本”，area就是“区域”
##### 属性
* `rows="4"`：指定文本区域的行数
* `cols="20"`：指定文本区域的列数
* `readonly`：只读
#### 表单的语义化
````
<form>
        <fieldset>
            <legend>账号信息</legend>
            姓名：<input value="刘亦菲"><br/> 密码：
            <input type="password" value="pwd" size="50"><br/>
        </fieldset>
        <fieldset>
            <legend>其他信息</legend>
            性别：<input type="radio" name="gender" value="male" checked="">男
            <input type="radio" name="gender" value="female">女<br/> 爱好：
            <input type="checkbox" name="love" value="eat">吃饭
            <input type="checkbox" name="love" value="sleep">睡觉
            <input type="checkbox" name="love" value="study">学习
        </fieldset>
</form>
````
![1](https://user-images.githubusercontent.com/66710812/168278178-3e72897a-d642-4e31-9a1f-ac19bfdb233f.jpg)
#### `<label>`标签
````
<input type="radio" name="sex" /> 男
<input type="radio" name="sex" /> 女
````
对于上面这样的单选框，只有点击单选框的小圆圈才可以选中，点击“男”、“女”两个文字时是无法选中的，label标签可以把input和汉字包裹起来作为整体。做法如下：
````
<input type="radio" name="sex" id="nan" /> <label for="nan">男</label>
<input type="radio" name="sex" id="nv"  /> <label for="nv">女</label>
````
上述代码中，让label标签的for属性值和input标签的id属性值相同，那么这个label和input就有绑定关系了，复选框也有label，任何表单元素都有label
### 多媒体标签
#### `<bgsound>`标签：播放背景音乐
##### 属性
* `src="音乐文件的路径"`
* `loop="-1"`：属性值代表播放次数，-1代表循环播放
#### `<embed>`标签：播放多媒体文件（音频、视频等）
* 视频格式支持mp4、wav等，但不是所有视频格式都支持
* 属性
	* `src="多媒体文件的路径"`
	* `loop="-1"`：属性值代表播放次数，-1代表循环播放
	* `autostart="false"`：打开网页时，禁止自动播放。默认值是true
	* `volume="100"`:设置默认的音量大小
	* width:指falsh文件的宽度
	* height：指flash文件的高度
	* quality：指flash的播放质量，质量有高有低hight low
	* pluginspage：如果指定的flash插件不存在，则从pluginspage指定的地方下载
	* type：指定flash的文件格式类型
	* wmode:指flash的背景是否可以透明，取值：transparent是透明的
#### `<object>`标签：播放多媒体文件（音频、视频等）
主要应用于IE浏览器，它是W3C规范
* `classid`:指定flash插件的ID号，一般存在于注册表中
* `codebase`：如果flash插件不存在，则从codebase指定的地址下载
* `<param>`标签的主要作用：设置具体的详细参数
**在网页中插入flash时，为了同时兼容多种浏览器，需要将`<object>`标签和`<embed>`标签一起使用，但使用的顺序是：`<object>`中嵌套`<embed>`标记**
### 滚动字幕标签`<marquee>`
如果在这个标签里设置了内容，打开网页，内容就会像弹幕一样自动移动。包含属性如下所示：
* `direction="right"`：移动的目标方向。属性值可以是：left（从右向左移动，默认值）、right（从左向右移动）、up（从下向上移动）、down（从上向下移动）
* `behavior="slide"`:行为方式。属性值可以是：slide（只移动一次）、scroll（循环移动，默认值）、alternate（循环移动）。后两个都是循环移动，区别在于：假设在`direction="right"`的情况下，`behavior="scroll"`表示从左到右、从左到右、从左到右···`behavior="alternate"`表示从右到左、从右到左、从右到左···
* `scrollamount="30"`：移动的速度
* `loop="3"`：循环多少圈。负值表示无限循环
* `scrolldelay="1000"`：移动一次休息多长时间。单位是毫秒。
### HTML5
#### 什么是HTML5
HTML5是新一代开发web富客户端应用程序整体解决方案。包括：HTML5,CSS3,Javascript API在内的一套技术组合<br/>
**富客户端**：具有很强的**交互性**和体验的客户端程序。比如说，浏览博客，是比较简单的客户端；一个在线听歌的网站、即时聊天网站就是富客户端。
#### HTML5的应用场景
* 极具表现力的网页：内容简约而不简单
* 网页应用程序
	* 代替PC端的软件：iCloud、百度脑图、Office 365等
	* APP端的网页：淘宝、京东、美团等
	* 微信端：公众号、小程序等
* 混合式本地应用
* 简单的游戏
#### HTML5新增的内容
* HTML
	* 标签
		* 更语义化标签
		* 应用程序标签
	* 属性
		* 链接关系描述
		* 结构数据标记
		* ARIA
		* 自定义属性
	* 智能表单
		* 新增的表单类型
		* 虚拟键盘适配
	* 网页多媒体
		* 音频
		* 视频
		* 字幕
	* Canvas
		* 2D
		* 3D(WebGL)
	* SVG
* CSS
	* New Selector
	* Web Fonts
	* Text Styles
	* Opacity
	* HSL Color
	* Rounded Corners
	* Gradients
	* Shadows
	* Background Enhancements
	* Border Image
	* Flexible Box Model
	* Transforms
	* Transitions
	* Animations
	* etc.
* JavaScript API
	* 核心平台提升
		* 新的选择器
		* Element.classList
		* 访问历史API
		* 全屏API
	* 网页存储
		* Application Cache
		* localStorage
		* sessionStorage
		* webSQL
		* IndexedDB
	* 设备信息访问
		* 网络状态
		* 硬件访问
		* 设备方向
		* 地理围栏
	* 拖放操作
		* 网页内拖放
		* 桌面拖放
		* 桌面拖出
	* 文件
		* 文件系统API
		* FileReader
	* 网络访问
		* XMLHttpRequest
		* fetch
		* WebSocket
	* 多线程
	* 桌面通知
#### HTML5新增语义化标签
##### 语义化的作用
* 能够便于开发者阅读和写出更优雅的代码
* 同时能够让浏览器或是网络爬虫可以很好的解析，从而更好分析其中的内容
* 更好的搜索引擎优化
##### H5中新增的语义化标签
* `<section>`：表示区块
* `<article>`：表示文章。如文章、评论、帖子、博客
* `<header>`：表示页眉
* `<footer>`：表示页脚
* `<nav>`：表示导航
* `<aside>`：表示侧边栏。如文章的侧栏
* `<figure>`：表示媒介内容分组
* `<mark>`：表示标记（用的少）
* `<progress>`：表示进度（用的少）
* `<time>`：表示日期
###### 新语义化标签的兼容性处理
IE8及以下版本的浏览器不支持H5和CSS3。解决办法：引入html5shiv.js文件。引入时，需要做if判断，具体代码如下：
````
<!-- 条件注释 只有ie能够识别-->

<!-- [if lte ie 8]>
	<script src="html5shiv.min.js"></script>
<!--[endif]-->
````
上述代码是条件注释，但是ie浏览器可以识别出来。
* l:less 更小
* t:than 比
* e:equal 等于
* g:great 更大
#### H5新增的表单类型
* `email`：只能输入email格式，自动带有验证功能
* `tel`：手机号码
* `url`：只能输入url格式
* `number`：只能输入数字
* `search`：搜索框
* `range`：滑动条
* `color`：拾色器
* `time`：时间
* `date`：日期
* `datetime`：时间日期
* `month`：月份
* `week`：星期
##### 表单元素（标签）
* `<datalist>`数据列表
````
<input type="text" list="myData">
<datalist id="myData">
    <option>本科</option>
    <option>研究生</option>
    <option>不明</option>
</datalist>
````
上述代码将input中的list属性和datalist进行了绑定，数据列表可以自动提示。效果如下：
![687474703a2f2f696d672e736d79687661652e636f6d2f32303138303230365f313834352e676966](https://user-images.githubusercontent.com/66710812/168418022-68ee0689-14f2-4ecc-89d4-620a32859c50.gif)
* `<keygen>`元素
keygen元素的作用是提供一种验证用户的可靠性算法。<br/>
keygen元素是密钥对生成器(key-pair generator)。当提交表单时，会生成两个键：一个公钥，一个私钥。私钥(private key)存储与客户端，公钥(public key)则被发送到服务器。公钥可用于之后验证用户的客户端证书(client certificate)。
* `<meter>`元素：度量器
	* low:低于该值后警告
	* high:高于该值后警告
	* value:当前值
	* max:最大值
	* min:最小值
##### 表单属性
* `placeholder`:占位符（提示文字）
* `autofocus`自动获取焦点
* `multiple`文件上传多选或多个邮箱地址
* `autocomplete`自动完成（填充的）。on开启（默认），off取消。用于表单元素，也用于表单自身
* `form`指定表单项属于哪个form，处理复杂表单时会需要
* `novalidate`关闭默认的验证功能（只能加给form）
* `required`表示必填项
* `pattern`自定义正则，验证表单
##### 表单事件
* `oninput()`：用户输入内容时触发，可用于输入字数统计
* `oninvalid()`：验证不通过时触发。比如，验证不通过，想弹出一段提示文字，就可以用到它
#### H5新增的多媒体
在H5之前，网页上播放音频/视频的通用方法是flash，播放复杂。因此，H5提供了视频和音频的标签
##### 音频
使用举例：
````
<audio src="music/yinyue.mp3" autoplay controls></audio>
````
效果如下：<br/>
![Snipaste_2022-05-14_22-13-48](https://user-images.githubusercontent.com/66710812/168429467-ebb62059-44fb-426c-b701-04000d056f4e.jpg)<br/>
可以通过附加属性，来更友好的控制音频的播放。如：
* `autoplay`自动播放。写成`autoplay`或者`autoplay=""`，都可以
* `controls`控制条。（建议把这个选项写上，不然根本看不到控件在哪里）
* `loop`循环播放
* `preload`预加载。同时设置autoplay时，此属性失效
audio支持三种音频格式，可采取以下措施处理兼容性问题
````
<!--推荐的兼容写法：-->
<audio controls loop>
    <source src="music/yinyue.mp3"/>
    <source src="music/yinyue.ogg"/>
    <source src="music/yinyue.wav"/>
    抱歉，你的浏览器暂不支持此音频格式
</audio>
````
##### 视频
* 使用举例
````
<video src="video/movie.mp4" controls autoplay></video>
````
* 附加属性
	* 具有音频的四条属性
	* `width`设置播放窗口宽度
	* `height`设置播放窗口高度
* 兼容性写法
````
    <!--<video src="video/movie.mp4" controls  autoplay ></video>-->
    <!--  行内块 display:inline-block -->
    <video controls autoplay>
        <source src="video/movie.mp4"/>
        <source src="video/movie.ogg"/>
        <source src="video/movie.webm"/>
        抱歉，不支持此视频
    </video>
````
#### DOM操作
##### 获取元素
* document.querySelector("selector"):通过CSS选择器获取符合条件的第一个元素
* document.querySelectorAll("selector"):通过CSS选择器获取符合条件的所有元素，以类数组形式存在
##### 类名操作
* Node.classList.add("class")：添加class
* Node.classList.remove("class"):移除class
* Node.classList.toggle("class"):切换class，有则移除，无则添加
* Node.classList.contains("class")：检测是否存在class
##### 自定义属性
H5可以直接在标签里添加自定义属性，但必须以`data-`开头。举例：
````
<!DOCTYPE html>
<html>
<head lang="en">
    <meta charset="UTF-8">
    <title></title>
</head>
<body>
<!-- 给标签添加自定义属性 必须以data-开头 -->
<div class="box" title="盒子" data-my-name="smyhvae" data-content="我是一个div">div</div>
<script>
    var box = document.querySelector('.box');

    //自定义的属性 需要通过 dateset[]方式来获取
    console.log(box.dataset["content"]);  //打印结果：我是一个div
    console.log(box.dataset["myName"]);    //打印结果：smyhvae

    //设置自定义属性的值
    var num = 100;
    num.index = 10;
    box.index = 100;
    box.dataset["content"] = "aaaa";

</script>
</body>
</html>
````
#### 拖拽
在H5中，我们可以通过为元素添加`draggable="true"`来设置此元素是否可以进行拖拽操作，其中图片、链接默认是开启拖拽的。
* 拖拽元素<br/>
	* 举例如下：
	```
	<!DOCTYPE html>
	<html>

	<head lang="en">
    	<meta charset="UTF-8">
    	<title></title>
    	<style>
        	.box1 {
            	width: 200px;
            	height: 200px;
            	background-color: green;
        	}
    	</style>
	</head>
	<body>
    	<!-- 给box1添加拖拽的属性-->
    	<div class="box1" draggable="true"></div>
	</body>
	</html>
	```
	* 效果如下：<br/>
	![687474703a2f2f696d672e736d79687661652e636f6d2f32303138303232335f323134302e676966](https://user-images.githubusercontent.com/66710812/168436267-0c50dab8-4a25-4569-a0a8-72ca3e2e8c63.gif)
	* 拖拽元素的事件监听
		* `ondragstart`：当拖拽开始时调用
		* `ondragleave`：当**鼠标离开拖拽元素时**调用
		* `ondragend`：当拖拽结束时调用
		* `ondrag`：整个拖拽过程都会调用
* 目标元素<br/>
想把元素A拖拽到元素B里，那么元素B就是目标元素。页面中任何一个元素都可以成为目标元素。*如果想让拖拽元素在目标元素里做点事情，就必须在ondragover()里加event.preventDefault()这一行代码*
	* 目标元素的事件监听
		* `ondragenter`：当拖拽元素进入目标元素时调用
		* `ondragover`：当拖拽元素停留在目标元素上时，就会连续一直触发（不管拖拽元素此时是移动还是不动的状态）
		* `ondrop`：当在目标元素上松开鼠标时调用
		* `ondragleave`：当鼠标离开目标元素时调用
	* 拖拽练习
```
<!DOCTYPE html>
<html>

<head lang="en">
    <meta charset="UTF-8">
    <title></title>
    <style>
        .one {
            width: 400px;
            height: 400px;
            border: 1px solid #000;
        }
        
        .two {
            width: 400px;
            height: 400px;
            border: 1px solid #000;
            position: absolute;
            left: 600px;
            top: 200px;
        }
        
        .one>div,
        .two>div {
            width: 98px;
            height: 98px;
            border: 1px solid #000;
            border-radius: 50%;
            background-color: red;
            float: left;
            text-align: center;
            line-height: 98px;
        }
    </style>
</head>

<body>
    <div class="one">
        <div draggable="true">1</div>
        <div draggable="true">2</div>
        <div draggable="true">3</div>
        <div draggable="true">4</div>
        <div draggable="true">5</div>
        <div draggable="true">6</div>
        <div draggable="true">7</div>
        <div draggable="true">8</div>
    </div>
    <div class="two"></div>
</body>
<script>
    var boxs = document.querySelectorAll(".one div");
    //临时的盒子，用于存放当前拖拽的元素
    var two = document.querySelector(".two");
    var temp = null;
    //给8个小盒子分别绑定拖拽事件
    for (var i = 0; i < boxs.length; i++) {
        boxs[i].ondragstart = function() {
            //保存当前拖拽的元素
            temp = this;
            console.log(temp);
        }
        boxs[i].ondragend = function() {
            //当拖拽结束，清空temp
            temp = null;
            console.log(temp);
        }
    }
    //目标元素的拖拽事件
    two.ondragover = function(e) {
            //阻止拖拽的默认行为
            e.preventDefault();
        }
        //当在目标元素上松开鼠标时触发
    two.ondrop = function() {
        //将拖拽的元素追加到two上面来
        this.appendChild(temp);
    }
</script>

</html>
```
效果如下：<br/>
![687474703a2f2f696d672e736d79687661652e636f6d2f32303138303232345f323035302e676966](https://user-images.githubusercontent.com/66710812/168454427-19964b08-3911-407f-b842-52fbc67fda88.gif)
#### 历史
界面上的所有JS操作不会被浏览器记住，无法回到之前的状态。在H5中可以通过`window.history`操作访问历史状态，让一个页面可以有多个历史状态，无刷新改变页面内容。
* `window.history.forward()`：前进
* `window.history.back()`：后退
* `window.history.go()`：刷新
* `window.history.go(n)`：n=1表示前进；n=-1表示后退；n=0s表示刷新。如果移动的位置超出了历史的边界，会静默失败，但不会报错。
* 通过Js可以加入一个访问状态
* `history.pushState()`：放入历史中的状态数据，设置title（现在浏览器不支持改变历史状态）
#### 地理定位
*基于位置服务LBS*（Location Base Service)，使得我们可以基于用户位置开发互联网应用。
##### 获取地理信息的方式
* IP地址
* 三维坐标
	* GPS（Global Position System，全球定位系统）
	* Wi-Fi定位：仅限于室内
	* 手机信号定位：通过运营商的信号塔定位
* 用户自定义数据
* 位置获取方式对比（对不同获取方式进行比较，浏览器会自动以最优方式去获取用户地理信息）：<br/>

|数据源|优点|缺点|
|:---:|:---:|:---:|
|IP地址|任何地方都可用在服务器端处理|不精确（经常出错，一般精确到城市级）<br/>运算代价大|
|GPS|很精确|定位时间长，耗量大<br/>室内效果差<br/>需要额外硬件设备支持|
|Wi-Fi|精确<br/>可在室内使用<br/>简单、快捷|在乡村这些Wi-Fi接入点少的地区无法使用|
|手机信号|相当准确<br/>可在室内使用<br/>简单、快捷|需要能够访问手机或其modem设备|
|用户自定义|可获取比程序定位服务更准确的位置数据<br/>用户自行输入可能比自动检测要快|可能很不准确，特别是当用户位置变更后|

##### 隐私
H5 Geolacation（地理位置定位）规范提供了一套保护用户隐私的机制。必须先得到用户的明确许可，才能获取用户的位置信息。
##### API详解
* `navigator.getCurrentPosition(successCallback,errorCallback,options)`:获取当前地理信息
* `navigator.watchPosition(successCallback,errorCallback,options)`:重复获取当前地理信息
	* 成功获取当前地理信息后，会调用successCallback，并返回一个包含位置信息的对象position：（Coords即坐标）
		* `position.coords.latitude`:纬度
		* `position.coords.longitude`:经度
	* 获取地理信息失败后，会调用errorCallback，并返回错误信息error
	* 可选参数options对象可以调整位置信息数据收集方式
#### 全屏
H5规范允许用户自定义网页上*任一元素*全屏展示
* 开启/关闭全屏显示
	* `requestFullscreen()`:让元素开启全屏显示
	* `cancleFullscreen()`：让元素关闭全屏显示
	* 兼容性问题解决方法：添加私有前缀。<br/>
	* ```
	  webkitRequestFullScreen
	  webkitCancleFullScreen

	  mozRequestFullScreen
	  mozCancleFullScreen
	  ```
* 检测当前是否处于全屏状态
	* 方法如下：<br/>
	  ```
	  document.fullScreen
	  ```
	* 不同浏览器添加私有前缀：<br/>
	  ```
	  document.webkitIsFullScreen
	  document.mozFullScreen
	  ```
* 全屏的伪类
	* `:full-screen.box{}`
	* `:-webkit-full-screen{}`
	* `:moz-full-screen{}`
当元素处于全屏状态时，改变它的样式，这时就可以用到伪类。
* 代码举例
```
<!DOCTYPE html>
<html>

<head lang="en">
    <meta charset="UTF-8">
    <title></title>
    <style>
        .box {
            width: 250px;
            height: 250px;
            background-color: green;
            margin: 100px auto;
            border-radius: 50%;
        }
        /*全屏伪类：当元素处于全屏时，改变元素的背景色*/
        
        .box:-webkit-full-screen {
            background-color: red;
        }
    </style>
</head>

<body>
    <div class="box"></div>
</body>
<script>
    var box = document.querySelector('.box');
    // box.requestFullscreen();
    //直接这样写是没有效果的，必须要点一下才可以实现全屏功能。无效的原因可能是浏览器的机制
    document.querySelector('.box').onclick = function() {
        // 开启全屏显示的兼容写法
        if (box.requestFullscreen) { //如果支持全屏，那就让元素全屏
            box.requestFullscreen();
        } else if (box.webkitRequestFullScreen) {
            box.webkitRequestFullScreen();
        } else if (box.mozRequestFullScreen) {
            box.mozRequestFullScreen();
        }
    }
</script>

</html>
```
效果如下：（我自己代码运行不出这样的结果）<br/>
![687474703a2f2f696d672e736d79687661652e636f6d2f32303138303232345f323133302e676966](https://user-images.githubusercontent.com/66710812/168461167-856ae27d-063d-4fe7-ab92-8e3abd621433.gif)
### Web存储
为满足各种各样的需求，会经常性在本地存储大量的数据，传统方式以`document.cookie`来进行存储，但存储大小只有4kb左右。
#### H5的两种存储方式
* `window.sessionStorage`会话存储
	* 保存在内存中
	* 生命周期为关闭浏览器窗口。也就是说，当窗口关闭时数据销毁
	* 在同一个窗口下数据可以共享
* `window.localStorage`本地存储
	* 有可能保存在浏览器内存中，也有可能保存在硬盘中
	* 永久生效，除非手动删除（比如清理垃圾的时候）
	* 可以多窗口共享
#### Web存储的特性
* 设置、读取方便
* 容量较大，sessionStorage约5M、localStorage约20M
* 只能存储字符串，可以将对象JSON。stringify()编码后存储
#### 常用API
* `setItem(key,value)`：设置存储内容。可以新增一个item，也可以更新一个item
* `getItem(key)`：读取存储内容
* `removeItem(key)`：根据建，删除存储内容
* `clear()`：清空所有存储内容
* `key(n)`:根据索引值来获取存储内容
#### 记住用户名和密码案例：
```
<!DOCTYPE html>
<html>

<head lang="en">
    <meta charset="UTF-8">
    <title></title>
    <style>

    </style>
</head>

<body>
    <label for="">
        用户名：<input type="text" class="userName" />
    </label>
    <br/><br/>
    <label for="">
        密码：<input type="password" class="pwd" />
    </label>
    <br/><br/>
    <label for="">
        <input type="checkbox" class="check" id=""/>记住密码
    </label>
    <br/><br/>
    <button>登录</button>
</body>
<script>
    var userName = document.querySelector('.userName');
    var pwd = document.querySelector('.pwd');
    var chk = document.querySelector('.check');
    var btn = document.querySelector('.button');
    //当点击登录时，如果勾选记住密码，就存储密码，否则就清楚密码
    btn.onclick = function() {
            if (chk.checked) {
                //记住数据
                window.localStorage.setItem('userName', userName.value);
                window.localStorage.setItem('pwd', pwd.value);
            } else {
                //清除数据
                window.localStorage.removeItem('userName');
                window.localStorage.removeItem('pwd');
            }
        }
        //下次登录时，如果记录的有数据，就直接填充
    window.onload = function() {
        userName.value = window.localStorage.getItem('userName');
        pwd.value = window.localStorage.getItem('pwd');
    }
</script>

</html>
```
#### 网络状态
我们可以通过`window.online`来检测用户当前的网络状况，返回一个布尔值。
* `window.online`:用户网络连接时被调用
* `window.offline`:用户网络断开时被调用（拔掉网线或者禁用以太网）
#### 应用缓存
H5中我们可以轻松的构建一个离线（无网络状态）应用，只需要创建一个`cache manifest`缓存清单文件
* 优势
	* 可配置需要缓存的资源
	* 网络无连接，应用仍可用
	* 本地读取缓存资源，提升访问速度，增强用户体验
	* 减少请求，缓解服务器负担
* 缓存清单文件里的内容怎样写
*缓存清单文件里列出了浏览器应缓存、以供离线访问的资源。推荐使用`.appcache`作为后缀名，另外还要添加MIME类型*
	* 顶行写CACHE MANIFEST
	* CACHE：换行 指定我们需要缓存的静态资源，如css/image/js等
	* NETWORK：换行 指定需要在线访问的资源，可使用通配符
	* FALLBACK：换行 当被缓存的文件找不到时的备用资源
格式举例：
	```
	CACHE MANIFEST

	#要缓存的文件
	CACHE:
    	images/img1.jpg
    	images/img2.jpg


	#指定必须联网才能访问的文件
	NETWORK:
     	images/img3.jpg
     	images/img4.jpg


	#当前页面无法访问是回退的页面
	FALLBACK:
    	404.html
	```
* 缓存清单文件怎么用
	* 首先我们创建一个名为`demo.appcache`的文件
	```
	CACHE MANIFEST

	# 注释以#开头
	#下面是要缓存的文件
	CACHE:
    	http://img.smyhvae.com/2016040101.jpg
	```
	* 在需要应用缓存在页面的根元素html里，添加属性`manifest="demo.appcache"`。路径要保证正确，例如：
	```
	<!DOCTYPE html>
	<html manifest="demo.appcache">
	<head lang="en">
    	<meta charset="UTF-8">
    	<title></title>
	</head>
	<body>
	<img src="http://img.smyhvae.com/2016040101.jpg" alt=""/>
	</body>
	</html>
	```
