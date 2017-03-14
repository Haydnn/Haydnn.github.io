---
layout: project
title: "JavaScript Dom编程艺术示例"
date: 2017-03-14
excerpt: "典型例子的代码"
tags: [博文]
comments: true
---

// JavaScript Document
/*获取id*/
function $(id){
	return typeof id==='string'? document.getElementById(id):id;
}
/*页面加载*/
window.onload=tab;

function tab(){
	var index=0;
	var timer=null;
	//获取所有的页签和要切换的图片
	var spans=$('numBox').getElementsByTagName('span');
	var divs=$('content-pic').getElementsByTagName('div');
	//鼠标滑过显示图片
	for(var i=0;i<spans.length;i++){
			spans[i].id=i;
			spans[i].onmouseover=function(){
				for(var j=0;j<spans.length;j++){
			        spans[j].className=' ';
			        divs[j].style.display='none';}
				this.className='select';
				divs[this.id].style.display='block';
			}
		}
	
	//添加定时器，改变当前索引
	timer=setInterval(function (){
		index++;
		if(index>=spans.length){
			index=0;
		}
		
		for(var j=0;j<spans.length;j++){
			spans[j].className=' ';
			divs[j].style.display='none';
		}
		//显示当前的页签
		spans[index].className='select';
		divs[index].style.display='block';
		},2000);
}
