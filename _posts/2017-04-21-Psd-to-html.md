---
layout: post
title: "从psd到html实例"
date: 2017-04-21
excerpt: "记录从psd到html开发的过程和总结"
tags: [博文,技术,案例]
comments: true
---

# 从psd到html实例

## 准备工作

#### 建立文件夹

1.css文件夹：根据需要存放三个css文件；

reset.css：用来重置各种标签的默认样式，如把所有标签的margin，padding置为0;去除ul，ol，li的默认样式；清楚左右浮动，清楚伪类after

{% highlight html %}                          
body,dl,dt,li,h1,h2,h3,h4,h5,h6,div,input,form,a,p,textarea{
	margin:0;
	padding: 0;  //可以用通配符，但不是所有的标签都需要去默认样式
	font-family: ;
}

ol,ul,li{
	list-style: none;
}

a{
	text-decoration: none;
	display: block;
}

img{
	display: block;
	border: none;
}

.clearfloat{ //清楚浮动
	zoom: 1;
}
.clearfloat:after{  //清楚伪类浮动
	display: block;
	clear: both;
	content: "";
	visibility: hidden;
	height:0;
}
{% endhighlight %}

common.css：用来存放构建公共头部，尾部的css样式

index.css：存放页面主体内容的样式

2.js文件夹

3.images文件夹：存放psd页面切下来的logo，图片等。切图技巧，用ps打开psd文件，找到要切图像所在的图层，右击转换为智能对象；用框选工具选中图像，Ctrl+C复制加Ctrl+N新建，转换到一个新页面后在Ctrl+V 粘贴，然后保存为相应格式即可。

#### 小技巧

1.制作如图的评分小星星，

<figure class="third">
	<img src="../assets/img/post-img/Psd to html/demon1.jpg">
	<img src="../assets/img/post-img/Psd to html/demon2.jpg">
	<img src="../assets/img/post-img/Psd to html/demon3.jpg">
	<figcaption></figcaption>
</figure>

选中星星，Ctrl+C加Ctrl+N，转换到一个新页面后在Ctrl+V。然后在ps的图像---画布大小，把画布长度拉长一倍，再去原psd图截取灰色星星，粘贴在下面的空间。使用时只要按需设置相关类名即可。

css代码如下：

{% highlight html %}                          
 .star
{
    display: inline-block;

    width: 12px;   //盒子设置为12*12
    height: 12px;
    margin-right: 5px;

    background-image: url(../images/star.png);  //图片尺寸为12*24
    background-repeat: no-repeat;
}
 .nostar
{
    background-position: 0 -12px;  //灰色时只需把背景图上移12px
}
<div class="star-bar">
	<span class="star"></span>
	<span class="star"></span>
	<span class="star nostar"></span>
	<span class="star nostar"></span>
	<span class="star nostar"></span>
</div>
{% endhighlight %}

2.制作如图小按钮

![按钮](../assets/img/post-img/Psd to html/demon4.jpg)

通过css样式即可写出，代码如下：

{% highlight html %}                          
 .btn-group
{
    font-size: 0;

    float: right;
}
.btn
{
    display: inline-block;

    width: 9px;
    height: 9px;
    margin-left: 11px;

    border-radius: 50%;  //边框为圆
    background: #dedede;
}
 .active  //给类设置不同颜色
{
    background: #7a6b6b;
}
<div class="btn-group">
	<a href="" class="btn active"></a>
	<a href="" class="btn"></a>
	<a href="" class="btn"></a>
	<a href="" class="btn"></a>
</div>
{% endhighlight %}

