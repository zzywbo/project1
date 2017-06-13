
## 1.Boostrap第二部分：全局CSS样式——辅助类
  .pull-left
  .pull-right	
  .caret
  .close
  .center-block

## 2.Boostrap第二部分：全局CSS样式——排版&代码


## 3.Boostrap第二部分：全局CSS样式——表格
  .table								
  .table-bordered		带边框的表格
  .table-striped		隔行变色的表格
  .table-hover			鼠标悬停变色的表格
  .table-responsive		响应式表格，用于TABEL父元素DIV
Bootlint：官方提供的一个用于检查HTML/CSS使用方面错误的工具。

## 4.Boostrap第二部分：全局CSS样式——栅格布局系统——重点
  页面内容布局的三种方式：
  (1)TABLE布局
	好处：简单容易控制
 	问题：语义错误，渲染效率低
  (2)DIV+CSS布局
	好处：语义正确，渲染效率高
	问题：不容易控制
  (3)Bootstrap栅格布局系统
	好处：语义正确，渲染效率高，简单容易控制，实现了响应式
	不足：没有！

### 栅格布局系统的使用方法：
**(1)栅格系统的父元素必须是：**
	div.container	- 定宽容器  
		LG:1170px MD:970px SM: 750px XS:100%
	div.container-fluid - 变宽容器
		width:100%
**(2)在容器中声明“行”**
	div.container > div.row
**(3)在“行”中声明“列”**
	div.container > div.row > div.col-*-*
**(4)列根据不同的屏幕尺寸分为四组：**
	.col-lg-*
	.col-md-*
	.col-sm-*
	.col-xs-*
**(5)一行均分为12等份，每个列必须指定自己的占比：**
	.col-lg-1
	.col-lg-2
	.col-lg-3
	.col-lg-...
	.col-lg-12**
**(6)列可以向后“偏移”指定的宽度**
	.col-lg-offset-1
	.col-lg-offset-2
	.col-lg-offset-....
	.col-lg-offset-12
	
**(7)不同屏幕宽度下的列宽度占比适用于指定屏幕以及更大屏幕**
	.col-xs-*		适用于xs/sm/md/lg屏幕
	.col-sm-*		适用于sm/md/lg屏幕
	.col-md-*		适用于md/lg屏幕
	.col-lg-*		适用于lg屏幕
**(8)一个列可以指定不同屏幕下的不同宽度占比**
	<div class="col-xs-12  col-sm-9  col-md-6">
	<div class="col-xs-12  col-md-6">
**(9)可以指定列在特定的屏幕下实现隐藏**
	.hidden-lg
	.hidden-md
	.hidden-sm
	.hidden-xs
	.hidden
	注意：隐藏只对指定屏幕有效！
**(10)栅格系统可以嵌套使用**
	<div class="row">
		<div class="col-xs-1">
			<div class="row">
				<div class="col-xs-6"></div>
			</div>
		</div>
	</div>

  

## 5.Boostrap第二部分：全局CSS样式——表单——难点
  难点：(1)相关class较多  (2)HTML结构复杂——HTML5规范
  Bootstrap提供了三种形式的表单：
  **(1)默认表单**
	
	<form>
		<div class="form-group">
			<label class="control-label"></label>
			<input class="form-control">
			<span class="help-block"></span>
		</div>
	</form>
  **(2)行内表单**
	
	<form class="form-inline">
		<div class="form-group">
			<label class="sr-only"></label>
			<input class="form-control">
		</div>
	</form>
  **(3)水平表单**
 	提示：水平表单指在一行中放置label、input、span，需要整合栅格布局系统(变种) 和 表单相关内容。
	标准栅格系统	水平表单中栅格
外层容器	div.container  或
div.container-fluid	form.form-horizontal
行	div.row	div.form-group
列	div.col-*-*	div.col-*-*
	
	<form class="form-horizontal ">	  <!--.container-->
		<div class="form-group">	  <!--.row-->
		  <div class="col-*-*>		  <!--.col-*-*-->
			<label class="sr-only"></label>
		  </div>
		  <div class="col-*-*">
			<input class="form-control">
		  </div>
		</div>
	</form>


## 8.Bootstrap第三部分：组件 —— 下拉菜单
  下拉菜单必需的三级结构：
  <div class="dropdown">
	<a data-toggle="dropdown">触发元素</a>
	<ul class="dropdown-menu">隐藏的菜单</ul>
  </div>
  提示：后面必需引入bootstrap.js，其中会查找data-toggle="dropdown"元素，为其绑定事件监听函数。

## 9. Bootstrap第三部分：组件 —— 警告框
	  <div class="alert alert-四种颜色 alert-dismissible">
		<span class="close" data-dismiss="alert">&times;</span>
		任意文本内容
	  </div>







