---
title: 使用Vercel免费搭建网站
date: 2021-04-30 23:48:30
tags: 教程
---
<script type="text/javascript"> 
 !function (e, t, a) {function r() {for (var e = 0; e < s.length; e++) s[e].alpha <= 0 ? (t.body.removeChild(s[e].el), s.splice(e, 1)) : (s[e].y--, s[e].scale += .004, s[e].alpha -= .013, s[e].el.style.cssText = "left:" + s[e].x + "px;top:" + s[e].y + "px;opacity:" + s[e].alpha + ";transform:scale(" + s[e].scale + "," + s[e].scale + ") rotate(45deg);background:" + s[e].color + ";z-index:99999");requestAnimationFrame(r)}function n() {var t = "function" == typeof e.onclick && e.onclick;e.onclick = function (e) {t && t(), o(e)}}function o(e) {var a = t.createElement("div");a.className = "heart", s.push({el: a,x: e.clientX - 5,y: e.clientY - 5,scale: 1,alpha: 1,color: c()}), t.body.appendChild(a)}function i(e) {var a = t.createElement("style");a.type = "text/css";try {a.appendChild(t.createTextNode(e))} catch (t) {a.styleSheet.cssText = e}t.getElementsByTagName("head")[0].appendChild(a)}function c() {return "rgb(" + ~~(255 * Math.random()) + "," + ~~(255 * Math.random()) + "," + ~~(255 * Math.random()) + ")"}var s = [];e.requestAnimationFrame = e.requestAnimationFrame || e.webkitRequestAnimationFrame || e.mozRequestAnimationFrame || e.oRequestAnimationFrame || e.msRequestAnimationFrame || function (e) {setTimeout(e, 1e3 / 60)}, i(".heart{width: 10px;height: 10px;position: fixed;background: #f00;transform: rotate(45deg);-webkit-transform: rotate(45deg);-moz-transform: rotate(45deg);}.heart:after,.heart:before{content: '';width: inherit;height: inherit;background: inherit;border-radius: 50%;-webkit-border-radius: 50%;-moz-border-radius: 50%;position: fixed;}.heart:after{top: -5px;}.heart:before{left: -5px;}"), n(), r()}(window, document);
</script>
<h1>准备工作</h1>
<p>准备所需要的工具:<br />
<b>GitHub账号<br />
Vercel账号</b></p>
<h1>开始</h1>
<p>访问GitHub官网:<br />
<a href="//github.com">https://github.com</a><br />
点击右上角的"Login&nbsp;in"<br />
<img src="https://z3.ax1x.com/2021/05/08/gGvlYq.png" /><br />
然后输入账户名(一般是你的GitHub名)和密码登录<br />
在主界面左上区域点击"New"(或者访问<a href="//github.com/new">https://github.com/new</a>)创建一个储存库<br />
<img src="https://z3.ax1x.com/2021/05/08/gGvKTs.png" /><br />
储存库名随便填，建议规范命名，然后点击"Create repository"创建(在最下面)<br />
<img src="https://z3.ax1x.com/2021/05/08/gGvESf.png" /><br />
然后访问Vercel官网:<br />
<a href="//vercel.com">https://vercel.com</a><br />
滑到最下面，点击黑色的GitHub按键，注册Vercel<br />
<img src="https://z3.ax1x.com/2021/05/08/gGvZ6S.png"><br />
然后点击"New Project"开始一个新项目<br />
理论上来说，Vercel第一次使用会自动进入新项目界面<br />
<img src="https://z3.ax1x.com/2021/05/08/gGvkfP.png" /><br />
在此界面选择刚才创建的储存库(如果没有请检查你是否授权了Vercel)<br />
<img src="https://z3.ax1x.com/2021/05/08/gGvFYt.png" /><br />
然后会进入部署内容界面。我们直接"Continue"全部选择部署<br />
<img src="https://z3.ax1x.com/2021/05/08/gGveOg.png" /><br />
然后点击"Select"确定后会进入选项卡，我们不用管，直接点"Deploy"开始部署<br />
<img src="https://z3.ax1x.com/2021/05/08/gGvVl8.png" /><br />
<img src="https://z3.ax1x.com/2021/05/08/gGvuwj.png" /><br />
然后我们就会进入部署界面，不久就会自动部署完毕了<br />
<img src="https://z3.ax1x.com/2021/05/08/gGvnmQ.png" />
之后修改文件只需要修改GitHub上的文件，Vercel会自动更新网站</p>
