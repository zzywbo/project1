
## 1.什么是响应式网页？  
				
  响应式网页、自适应式网页，一个页面，可以根据浏览设备的不同、或使用环境的不同，自动的修改布局、图片尺寸、文字大小，从而可以保证所有的设备下都正常的浏览体验。
  好处：各种设备下都正常浏览
  不足：页面代码结构需要考虑到多种设备，编写难度更大，一般只适用于内容量不太多的页面。


## 2.如何测试响应式网页？
(1)使用真实物理设备测试——测试效果最好但最麻烦  
(2)使用第三方模拟器软件测试——测试效果有待进一步验证  
(3)使用浏览器提供的设备模拟器测试——最简单但有时测试效果与真实物理设备有所不同，需要进一步验证


行业小知识：Viewport，视口，屏幕中浏览网页的窗口
早期的手机浏览PC网页时只能把页面进行缩小，影响浏览体验：

iOS系统提出了viewport的概念——承载网页的窗口，可以随意指定宽和高，但不能小于手机物理屏幕，可以让任意大小的网页不经缩放，直接显示：

Android后来也引入了该概念 —— 只有移动浏览器才有该概念

## 如何编写响应式网页？
  **(1)必须声明viewport元标签**
   	<meta name="viewport" content="width=device-width,initial-scale=1.0,user-scalable=no">
  **(2)容器尽量使用相对尺寸**
	尽量避免绝对尺寸：  div.container {  width: 500px;  }
	使用相对尺寸代替：  div.container {  width: 80%;  }
  **(3)文字大小尽量使用相对尺寸**
	尽量避免绝对尺寸：  .text { font-size: 12px; }
	使用相对尺寸代替：  .text { font-size: 0.8rem; }
  **(4)图片尽量使用相对尺寸**
	尽量避免绝对尺寸：  img { width: 200px; }
	使用相对尺寸代替：	 img { width: 50%; }  指定在父容器中的宽度占比，可以随着父容器无限变大
					 img { max-width: 50%; } 指定在父容器中的宽度占比，同时还不能超过自己的原始大小
  **(5)页面布局尽量采用流式布局(Fluid)**
	float:left;   或  display:inline-block;	
  **(6)响应式网页必须CSS3 Media Query技术！**


## 4.CSS3 Media Query
  Media：指浏览网页的设备，如screen(phone/pc/pad)、tv、projection、print、tty、braille  
  Query：使用CSS自动查询出浏览设备的特性，如位深、解析度、宽高、水平/竖直方向....
  CSS3 Media Query：根据浏览网页的设备类型不同，或者特性不同，而有选择的执行某些CSS，放弃执行另外的。
  媒体查询具体有两种使用方法：
  **(1)有选择性的执行符合条件的外部CSS文件**
	`<link media="screen and (min-width:768px) and (max-width:991px)" rel="stylesheet" href="css/pad.css">`
	缺陷：即使不满足当前浏览器条件的CSS文件，也会被浏览器请求。
 ** (2)有选择性的执行CSS片段中的部分内容**
	@media screen and (min-width: 768px) and (max-width: 991px) {
  		h3 {
			display：none
  		}
	}

bootstrap：起步，引导程序，入口程序

## 5.Twitter Bootstrap概述			
  官网：http://getbootstrap.com/
  中文网：http://www.bootcss.com/
  Bootstrap is the most popular HTML, CSS, and JS framework for developing responsive, mobile first projects on the web.
  内容分为五部分：
  (1)起步
  (2)全局CSS样式
  (3)组件
  (4)JS插件
  (5)定制


## 6.Bootstrap第一部分：起步
  下载
  基本模板
<html lang="zh-cn">
<html lang="en-us">
HTML标签的lang属性(language)指定当前页面所使用的自然语言，如zh、zh-cn、zh-tw、zh-hk、en、en-uk、ja、de、fr....
作用1：指定当前页面的基础语言，为浏览器的翻译做准备
作用2：为盲人的屏幕阅读器指明基础发音

<meta http-equiv="X-UA-Compatible" content="IE=6">
<meta http-equiv="X-UA-Compatible" content="IE=edge">
Cross-UserAgent-Compatible，跨（IE）浏览器兼容性
IE 6： 非常多的专有对象
IE 7： 6/7
IE 8 :  6/7/8
IE 9 :  6/7/8/9
IE 10 : 6/7/8/9/10
IE 11 : 6/7/8/9/10/11
   edge：使用可用的最新版本的IE内核

html5shiv.js：第三方的JS文件，自调函数，让老IE支持HTML5语义标签。
respond.js：第三方的JS文件，自调函数，让老IE支持响应式网页——CSS3媒体查询技术


7.Bootstrap第二部分——全局CSS样式
  与按钮相关样式：
	.btn
	.btn-default		白底黑字按钮
	.btn-danger		红色
	.btn-warning		黄色
	.btn-success		绿色
	.btn-info			浅蓝色
	.btn-primary		深蓝色
	.btn-lg			大号
	.btn-sm			小号
	.btn-xs			超小号
	.btn-block		块级按钮			
  与图片相关的样式：
	.img-rounded		圆角图片
	.img-circle		圆形图片
	.img-thumbnail	缩略图片
	.img-responsive	响应式图片
   与列表相关的样式：
	.list-unstyled		没有提示符的列表
	.list-inline			行内列表
   与文本相关的样式：
	.text-danger
	.text-success
	.text-warning
	.text-info
	.text-primary
	.bg-danger
	.bg-success
	.bg-warning
	.bg-info
	.bg-primary
	.text-left
	.text-right
	.text-center
	.text-justify
	.text-uppercase
	.text-lowercase
	.text-capitalize





