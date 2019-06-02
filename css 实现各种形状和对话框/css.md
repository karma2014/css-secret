##CSS实现梯形
CSS实现三角形和梯形主要是依靠border是梯形的特性来做的，有点像相框的那种感觉。

首先我们先给一个正方形设置比较宽的边框。如下。
<div id="test1"></div>
<style>
	#test1{
    	width: 50px;
    	height: 50px;
    	background: purple;
    	border-top: 50px solid red;
    	border-bottom: 50px solid green;
    	border-left: 50px solid blue;
    	border-right: 50px solid yellow;
    	margin:0 auto;
	}
</style>

代码如下：
	
	<div id="test1"></div>

    <style>
		#test1{
    		width: 50px;
    		height: 50px;
    		background: purple;
    		border-top: 50px solid red;
    		border-bottom: 50px solid green;
    		border-left: 50px solid blue;
    		border-right: 50px solid yellow;
    		margin:0 auto;
		}
	</style>

然后把其他颜色设置成看不见的颜色，我们就得到了梯形
<div id="test2"></div>
<style>
    #test2{
        width: 50px;
        height: 50px;
        background: transparent;
        border-top: 50px solid transparent;
        border-bottom: 50px solid #d71345;
        border-left: 50px solid transparent;
        border-right: 50px solid transparent;
    }
</style>
代码如下：
	
    <div id="test2"></div>

	<style>
    	#test2{
        	width: 50px;
        	height: 50px;
        	background: transparent;
        	border-top: 50px solid transparent;
        	border-bottom: 50px solid #d71345;
        	border-left: 50px solid transparent;
        	border-right: 50px solid transparent;		
    	}
		</style>

##CSS实现三角形
只要把中间的正方形的宽高设为0就行
<div id="test3"></div>
<style>
    #test3{
        width: 0;
        height: 0;
        display: inline-block;
        background: transparent;
        border-top: 50px solid transparent;
        border-bottom: 50px solid #fcaf17;
        border-left: 50px solid transparent;
        border-right: 50px solid transparent;
		margin:0 auto;
    }
</style>
代码如下

	<div id="test3"></div>
	<style>
    	#test3{
        	width: 0;
        	height: 0;
        	display: inline-block;
        	background: transparent;
        	border-top: 50px solid transparent;
        	border-bottom: 50px solid #fcaf17;
        	border-left: 50px solid transparent;
        	border-right: 50px solid transparent;
			margin:0 auto;
    	}
	</style>

##CSS实现平行四边形
首先，先来两个三角形，如下

<div id="triangle1"></div>
<div id="triangle2"></div>
<style>
    	#triangle1{
        	width: 0;
        	height: 0;
        	background: transparent;
        	border-top: 50px solid transparent;
        	border-bottom: 50px solid #00ae9d;
        	border-left: 50px solid transparent;
        	border-right: 50px solid transparent;
    	}
		#triangle2{
        	width: 0;
        	height: 0;
        	background: transparent;
        	border-top: 50px solid #009ad6;
        	border-bottom: 50px solid transparent;
        	border-left: 50px solid transparent;
        	border-right: 50px solid transparent;
    	}
</style>
代码如下：

	<div id="triangle1"></div>
	<div id="triangle2"></div>
	<style>
    	#triangle1{
        	width: 0;
        	height: 0;
        	background: transparent;
        	border-top: 50px solid transparent;
        	border-bottom: 50px solid #00ae9d;
        	border-left: 50px solid transparent;
        	border-right: 50px solid transparent;
    	}
		#triangle2{
        	width: 0;
        	height: 0;
        	background: transparent;
        	border-top: 50px solid #009ad6;
        	border-bottom: 50px solid transparent;
        	border-left: 50px solid transparent;
        	border-right: 50px solid transparent;
    	}
	</style>
再通过CSS3中的transform属性将两个三角形移动下位置，就可以实现自己的要求啦。当然你也可以用绝对定位来移动。
 
 
##CSS实现圆形
使用CSS3属性border-radius可以实现一个圆形。
<div id="circle"></div>
<style>
    #circle{
        width: 100px;
        height: 100px;
        background: #f05b72;
        border-radius: 50px;
    }
</style>

代码如下：

	<div id="circle"></div>
	<style>
    	#circle{
        	width: 100px;
       		height: 100px;
        	background: #f05b72;
        	border-radius: 50px;
    	}
	</style>

##CSS实现椭圆形
border-radius有一个水平半径和一个垂直半径。
border-radius: 水平半径 / 垂直半径;//当然也可以单独设置某个角的水平半径和垂直半径。
border-radius: 左上角水平半径、 右上角水平半径、 右下角水平半径、 左下角水平半径 / 左上角垂直半径、 右上角垂直半径、 右下角垂直半径、 左下角垂直半径。

实现一个椭圆形
<div id="ellipse"></div>

<style>
	#ellipse{
    	width: 100px;
    	height: 50px;
    	background: #f47920;
    	border-radius: 50px / 25px;
	}
</style>

代码如下：

	<div id="oval"></div>
	<style>
    #oval{
        width: 100px;
        height: 50px;
        background: #f47920;
        border-radius: 50px / 25px;
    }
	</style>

等价于

	<div id="oval"></div>
	<style>
	    #oval{
        width: 100px;
        height: 50px;
        background: blue;
        border-top-left-radius: 50px 25px;
        border-top-right-radius: 50px 25px;
        border-bottom-left-radius: 50px 25px;
        border-bottom-right-radius: 50px 25px;
    	}
	</style>

##CSS实现对话框

主要实现原理就是通过两个三角形的“叠加覆盖”，来形成对话框的尖角

样例1：
<div class="test1">
    <div class="bot">&nbsp;</div>
    <div class="top">&nbsp;</div>
    CSS实现对话框效果一
</div>
<style>
.test1{width:300px;height: 30px; padding:30px 20px; margin-left:100px; background: #ffe600; position:relative;}
.test1 div{ width:0; height:0; position:absolute;}
.test1 .bot{
    border-width:20px;
    border-style:solid;
    border-color:#ffffff #ffe600 #ffe600 #ffffff;
    left:-40px;
    top:40px;
}
.test1 .top{
    border-width:10px 20px;
    border-style:solid;
    border-color: transparent  #ffffff #ffffff transparent ;
    left:-40px;
    top:60px;
}
</style>
代码如下：

	<div class="test1">
    	<div class="bot">&nbsp;</div>
    	<div class="top">&nbsp;</div>
    	CSS实现对话框效果一
	</div>
	<style>
		.test1{width:300px;height: 30px; padding:30px 20px; margin-left:100px; background: #eb7956; position:relative;}
		.test1 div{ width:0; height:0; position:absolute;}
		.test1 .bot{
    		border-width:20px;
    		border-style:solid;
    		border-color:#ffffff #eb7956 #eb7956 #ffffff;
    		left:-40px;
    		top:40px;
		}
		.test1 .top{
    		border-width:10px 20px;
    		border-style:solid;
   			border-color: transparent  #ffffff #ffffff transparent ;
    		left:-40px;
    		top:60px;
		}
	</style>

 样例2：
<div class="test2">
    <div class="bot"></div>
    <div class="top"></div>
    CSS实现对话框效果e二
</div>
<style>
    .test2{width:300px; padding:30px 20px; border:5px solid #beceeb; position:relative;}
    .test2 div{width:0; height:0; font-size:0; overflow:hidden; position:absolute;}
    .test2 div.bot{
        border-width:20px;
        border-style:solid dashed dashed;
        border-color:#beceeb transparent transparent;
        left:80px;
        bottom:-40px;
    }
    .test2 div.top{
        border-width:20px;
        border-style:solid dashed dashed;
        border-color:#ffffff transparent transparent;
        left:80px;
        bottom:-33px;
    }
</style>
代码如下：

	<div class="test2">
    	<div class="bot"></div>
    	<div class="top"></div>
    	CSS实现对话框效果e二
	</div>
	<style>
    	.test2{width:300px; padding:30px 20px; border:5px solid #beceeb; position:relative;}
    	.test2 div{width:0; height:0; font-size:0; overflow:hidden; position:absolute;}
    	.test2 div.bot{
        	border-width:20px;
        	border-style:solid dashed dashed;
        	border-color:#beceeb transparent transparent;
        	left:80px;
        	bottom:-40px;
    	}
    	.test2 div.top{
        	border-width:20px;
        	border-style:solid dashed dashed;
        	border-color:#ffffff transparent transparent;
        	left:80px;
        	bottom:-33px;
    	}
	</style>



 样例3
<div class="test3">
    <div class="bot">&nbsp;</div>
    <div class="top">&nbsp;</div>
    CSS实现对话框效果三
</div>
<style>
.test3{
    width:300px;
    height: 30px;
    border-radius: 160px/45px;
    padding:30px 20px;
    margin-left:100px;
    background: #eb7956;
    position:relative;
}
.test3 div{ width:0; height:0; position:absolute;}
.test3 .bot{
    border-width:20px;
    border-style:solid;
    border-color:transparent #eb7956 #eb7956 transparent;
    left:-30px;
    top:40px;
}
.test3 .top{
    border-width:10px 20px;
    border-style:solid;
    border-color: transparent  #ffffff #ffffff transparent ;
    left:-30px;
    top:60px;
}
</style>

代码如下：

	<div class="test3">
    	<div class="bot">&nbsp;</div>
    	<div class="top">&nbsp;</div>
    	CSS实现对话框效果三
	</div>
	<style>
	.test3{
    	width:300px;
    	height: 30px;
    	border-radius: 160px/45px;
    	padding:30px 20px;
    	margin-left:100px;
    	background: #eb7956;
    	position:relative;
	}
	.test3 div{ width:0; height:0; position:absolute;}
	.test3 .bot{
    	border-width:20px;
    	border-style:solid;
    	border-color:transparent #eb7956 #eb7956 transparent;
    	left:-30px;
    	top:40px;
	}
	.test3 .top{
    	border-width:10px 20px;
    	border-style:solid;
    	border-color: transparent  #ffffff #ffffff transparent ;
    	left:-30px;
    	top:60px;
	}
	</style>

###补充：css中的单位
px：绝对单位，页面按精确像素展示
em：相对单位，基准点为父节点字体的大小，如果自身定义了font-size按自身来计算（浏览器默认字体是16px），整个页面内1em不是一个固定的值。
rem：相对单位，可理解为”root em”, 相对根节点html的字体大小来计算，CSS3新加属性，chrome/firefox/IE9+支持
vw：viewpoint width，视窗宽度，1vw等于视窗宽度的1%。
vh：viewpoint height，视窗高度，1vh等于视窗高度的1%。
vmin：vw和vh中较小的那个。
vmax：vw和vh中较大的那个。
vw, vh, vmin, vmax：IE9+局部支持，chrome/firefox/safari/opera支持，ios safari 8+支持，android browser4.4+支持，chrome for android39支持
%:百分比
in:寸
cm:厘米
mm:毫米
pt:point，大约1/72寸
pc:pica，大约6pt，1/6寸
ex：取当前作用效果的字体的x的高度，在无法确定x高度的情况下以0.5em计算(IE11及以下均不支持，firefox/chrome/safari/opera/ios safari/android browser4.4+等均需属性加么有前缀)
ch:以节点所使用字体中的“0”字符为基准，找不到时为0.5em(ie10+,chrome31+,safair7.1+,opera26+,ios safari 7.1+,android browser4.4+支持)