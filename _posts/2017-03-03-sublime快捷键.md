---
layout: post
title: "sublime text3的安装使用"
date: 2017-03-03
excerpt: "常用功能及快捷键"
tags: [博文,前端]
comments: true
---

## sublime text3的安装

首先通过[www.sublimetext.com](www.sublimetext.com)下载和电脑系统匹配的安装文件，然后下载安装包，因为服务器在国外，所以下载速度非常慢而且可能会下载失败。所以可以百度sublime安装包，网上有下载好的。

## sublime text3 常用插件安装
	
安装方法：在sublime运行界面按快捷键Ctrl+shift+p，弹出命令栏，在命令栏输入install，选择install package。会出现一系列插件表，确保电脑联网之后，点击需要的插件就会自动安装。安装完成后，可以在运行界面的preferences--package settings查看已经安装好的插件，可以自己进行配置。

Emmet：sublime必备插件，减少代码量，可以通过简写自动扩充代码段.Ctrl+E

Emmet语法：

1.使用>运算符用来生成彼此嵌套的元素，如section>div>p
2.使用+运算符用来生成彼此相邻的元素,如section+div+p
3.可以进行嵌套，如ul>(li>a)*3
4.一次生成多个相同的元素，比如列表li，ul>li*5
5.快速生成ID，类名，属性，文本，如div#id,div.classname,div[color:red],p{width:200px;color:blue;}

**ColorPicker**：调色盘。快捷键：Ctrl+shift+c

**sublimelinter**:提示错误语法

**jsformat**：对js代码进行格式化。鼠标右键--jsformat或者Ctrl+alt+F

**SideBarEnhancements**：实用的右键菜单增强插件，实现原来没有的许多其他功能

**csscomb**:为css属性进行格式化和排序，它依赖于node.js环境，即要求计算机安装过node.js环境。Tools->Run CSScomb或者Ctrl+Shift+C



## sublime text3常用功能

### 导航栏功能

* File

New File:创建新的编辑区，Ctrl+N

Open File:打开本地文件，Ctrl+O

界面右下角显示文件的类型，可以点击对文件类型进行切换


* Edit

Unindent:减少缩进，Ctrl+[

Indent:增加缩进，Ctrl+]

Duplicate Line:复制一行，Ctrl+Shift+D

Delete Line:删除一行，Ctrl+Shift+K

Toggle Comment:注释选中的代码，Ctrl+/

Toggle Block Comment:可以显示的注释，Ctrl+Shift+/

Insert Line Before:在光标所在行的上面插入一行，Ctrl+Shift+Enter

Insert Line After:在光标所在行的下面插入一行，Ctrl+Enter


* Selection（选择功能，帮助选择代码）

Expand Selection to Line:选择光标所在行，Ctrl+L

Expand Slection to Word:选择光标所在单词，Ctrl+D

（可重复命令进行多次选择，产生多行光标）

 
* Find（查找替换功能）

Find...:查找输入框，Ctrl+F


* View（对编辑器界面的配置）

Side Bar ->

Show Side Bar:显示侧边栏，Ctrl+K,Ctrl+B


* Goto 

Goto Anything...:可以在文件内或文件之间快速导航，Ctrl+P

（比如输入":20"，即跳转到第20行）


* Tools 

Command Palette...:命令模式，Ctrl+Shift+P


*Preferences（个性化定制）

Setting:可以更改字体大小

Color Scheme：颜色修改


### 常用快捷键

Ctrl+G：快速跳转到相应的行

Ctrl+Z ：撤销

Ctrl+Y ：恢复撤销

Ctrl+H ：替换

Ctrl+W ：关闭当前文件

Ctrl+F2 :设置/取消书签

Ctrl+鼠标左键 :可以同时选择要编辑的多处文本

Shift+鼠标右键 :可以用鼠标进行竖向多行选择

Alt+Shift+1：窗口恢复为默认1屏

Alt+Shift+2：左右分屏-2列

Alt+Shift+3：左右分屏-3列

F6：检测语法错误

F11：全屏模式切换







