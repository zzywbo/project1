

## 1.补充知识点：Bootstrap全局CSS样式——栅格系统
  列偏移(offset)：  

	控制某列向右错位，并影响后续所有的列
	.col-lg/md/sm/xs-offset-*
	作用：列左右留白、列右对齐、列居中
  列排序：  

	控制某列向右/左移动，并不影响其他列
	
	.col-lg-push-1/2/.../12
	.col-lg-pull-1/2/.../12
	作用：在特定屏幕下临时调整列的出现位置


## 2.Bootstrap第三部分：组件——下拉菜单

## 3.Bootstrap第三部分：组件——警告框

## 4.Bootstrap第三部分：组件——图标字体  

  图标字体：本质是文字，不是图片，可以随意变大、添加下划线、变斜体、改颜色。  

  Web应用中常用图标字体： FontAwesome、Glyphicons
  因为客户端都没有上述字体文件，必须应用服务器端字体：  

	 ···
 @font-face {
		font-family: 'Glyphicon';			/*声明服务器端字体*/
		src: url(../fonts/glyphicons....ttf)	/*服务器端字体下载位置*/
	  }
	  .glyphicon {
		font-family: 'Glyphicon';		/*使用服务器端字体*/
	  }
	  .glyphicon-alert:before {
		content: '\9fc3';
	  }
···
Bootstrap提供了200+个Glyphicons图标，使用方法：
<span class="glyphicon glyphicon-*"></span>
提示：使用图标字体的HTML标签中不能有任何子元素或内容！


## 5.Bootstrap第三部分：组件——按钮组
  把多个按钮放在一起组成小组
  .btn-group > .btn*n
  .btn-group.btn-group-justified > .btn*n
  .btn-group-vertical > .btn*n

## 6.Bootstrap第三部分：组件——导航(nav)
  Boostrap提供了三种形式的导航组件：  

**(1)标签页式导航（页签组件）**
···
	<ul class="nav nav-tabs">
		<li class="active"><a data-toggle="tab"></a></li>
	</ul>
···
**(2)胶囊式导航**
	<ul class="nav nav-pills">
		<li class="active"><a data-toggle="tab"></a></li>
	</ul>
**(3)导航条专用导航**

## 7.Bootstrap第三部分：组件——缩略图
  可以用于A元素或者DIV元素，用于展示一系列条目中的一个。
 练习：使用栅格系统+缩略图实现“商城中的商品列表”
 

## 8.Bootstrap第三部分：组件——媒体对象
  媒体对象常用于商品列表：
	<div class="media">
		<div class="media-left">图片</div>
		<div class="media-body">主体</div>
		<div class="media-right">图片</div>
	</div>


## 9.Bootstrap第三部分：组件——列表组
  用法1：无鼠标悬停效果
	<ul class="list-group">
		<li class="list-group-item"></li>
	</ul>
  用法2：有鼠标悬停效果
	<div class="list-group">
		<a class="list-group-item"></div >
	</div>

## 10.Bootstrap第三部分：组件 —— 面板组件 —— 小难点
  面板：在Bootstrap中是一种呈现“头部-主体-尾部”三层结构的组件。
	<div class="panel">
		<div class="panel-heading"></div>
		<div class="panel-body"></div>
		<div class="panel-footer"></div>
	</div>
  提示：面板组件中尤其适合放置 <table class="table">



## 11.Bootstrap第四部分：JS插件 —— Collapse
  折叠效果，本身使用很简单：
	<a data-toggle="collapse" href="cid">触发元素</a>
	<div id="cid" class="collapse in">
		内容
	</div>
  折叠效果有两个使用场景：
  (1)手风琴： 折叠效果插件 + 面板组
  (2)响应式导航条： 

## 12.Bootstrap第三部分：组件 —— 响应式导航条 —— 最难点
  注意：响应式导航条的结构——只有从手机屏幕才能看出来！
  
  代码结构：
	<div class="navbar">
		<div class="container">
			<div class="navbar-header">
				商标和汉堡包按钮
			</div>
			<div class="navbar-collapse collapse">
				能够折叠隐藏的内容，如导航、表单、链接...
			</div>
		</div>
	</div>
  导航条的种类：按颜色：
	浅色底深色字：.navbar.navbar-default
	深色底浅色字：.navbar.navbar-inverse
  导航条的种类：按定位：
	相对定位(占空间)：.navbar
	固定定位(不占空间)：.navbar.navbar-fixed-*
  导航条的种类：按位置：
	固定在顶部：.navbar.navbar-fixed-top
	固定在底部：.navbar.navbar-fixed-bottom



## 前端实现动画可用的技术：  

(1)CSS3 Transition技术  

(2)CSS3 Keyframes技术  

(3)JS定时器 —— jQuery1/2动画函数都是定时器动画  

(4)requestAnimationFrame技术 —— jQuery3