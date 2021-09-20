---
title: Jetbrains系列无限重置
date: 2021-08-04 21:25:00
tags: 教程
---
<script type="text/javascript"> 
 !function (e, t, a) {function r() {for (var e = 0; e < s.length; e++) s[e].alpha <= 0 ? (t.body.removeChild(s[e].el), s.splice(e, 1)) : (s[e].y--, s[e].scale += .004, s[e].alpha -= .013, s[e].el.style.cssText = "left:" + s[e].x + "px;top:" + s[e].y + "px;opacity:" + s[e].alpha + ";transform:scale(" + s[e].scale + "," + s[e].scale + ") rotate(45deg);background:" + s[e].color + ";z-index:99999");requestAnimationFrame(r)}function n() {var t = "function" == typeof e.onclick && e.onclick;e.onclick = function (e) {t && t(), o(e)}}function o(e) {var a = t.createElement("div");a.className = "heart", s.push({el: a,x: e.clientX - 5,y: e.clientY - 5,scale: 1,alpha: 1,color: c()}), t.body.appendChild(a)}function i(e) {var a = t.createElement("style");a.type = "text/css";try {a.appendChild(t.createTextNode(e))} catch (t) {a.styleSheet.cssText = e}t.getElementsByTagName("head")[0].appendChild(a)}function c() {return "rgb(" + ~~(255 * Math.random()) + "," + ~~(255 * Math.random()) + "," + ~~(255 * Math.random()) + ")"}var s = [];e.requestAnimationFrame = e.requestAnimationFrame || e.webkitRequestAnimationFrame || e.mozRequestAnimationFrame || e.oRequestAnimationFrame || e.msRequestAnimationFrame || function (e) {setTimeout(e, 1e3 / 60)}, i(".heart{width: 10px;height: 10px;position: fixed;background: #f00;transform: rotate(45deg);-webkit-transform: rotate(45deg);-moz-transform: rotate(45deg);}.heart:after,.heart:before{content: '';width: inherit;height: inherit;background: inherit;border-radius: 50%;-webkit-border-radius: 50%;-moz-border-radius: 50%;position: fixed;}.heart:after{top: -5px;}.heart:before{left: -5px;}"), n(), r()}(window, document);
</script>
<h1>声明</h1>
<p>不要将其用于非法用途和无休止地滥用</p>
<h2>支持的Jetbrains系列</h2>
<p><b>IntelliJ IDEA<br />
AppCode<br />
CLion<br />
DataGrip<br />
GoLand<br />
PhpStorm<br />
PyCharm<br />
Rider<br />
RubyMine<br />
WebStorm</b></p>
<h1>安装</h1>
<p>首先是一套操作选择试用30天，进到主界面点击Plugins,然后添加第三方插件仓库<br />
地址:https://plugins.zhile.io<br />
<img src="https://i.huahuo-cn.tk/Jetbrains-A.png"/><br />
<img src="https://i.huahuo-cn.tk/Jetbrains-B.png"/><br />
搜索插件<b>IDE Eval Reset</b>,然后安装,安装完成重启即可<br />
<img src="https://i.huahuo-cn.tk/Jetbrains-C.png"/></p>
