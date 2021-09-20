---
title: 'Hexo Blog安装'
date: 2021-03-21 11:29:32
tag: 教程
---
<script type="text/javascript"> 
 !function (e, t, a) {function r() {for (var e = 0; e < s.length; e++) s[e].alpha <= 0 ? (t.body.removeChild(s[e].el), s.splice(e, 1)) : (s[e].y--, s[e].scale += .004, s[e].alpha -= .013, s[e].el.style.cssText = "left:" + s[e].x + "px;top:" + s[e].y + "px;opacity:" + s[e].alpha + ";transform:scale(" + s[e].scale + "," + s[e].scale + ") rotate(45deg);background:" + s[e].color + ";z-index:99999");requestAnimationFrame(r)}function n() {var t = "function" == typeof e.onclick && e.onclick;e.onclick = function (e) {t && t(), o(e)}}function o(e) {var a = t.createElement("div");a.className = "heart", s.push({el: a,x: e.clientX - 5,y: e.clientY - 5,scale: 1,alpha: 1,color: c()}), t.body.appendChild(a)}function i(e) {var a = t.createElement("style");a.type = "text/css";try {a.appendChild(t.createTextNode(e))} catch (t) {a.styleSheet.cssText = e}t.getElementsByTagName("head")[0].appendChild(a)}function c() {return "rgb(" + ~~(255 * Math.random()) + "," + ~~(255 * Math.random()) + "," + ~~(255 * Math.random()) + ")"}var s = [];e.requestAnimationFrame = e.requestAnimationFrame || e.webkitRequestAnimationFrame || e.mozRequestAnimationFrame || e.oRequestAnimationFrame || e.msRequestAnimationFrame || function (e) {setTimeout(e, 1e3 / 60)}, i(".heart{width: 10px;height: 10px;position: fixed;background: #f00;transform: rotate(45deg);-webkit-transform: rotate(45deg);-moz-transform: rotate(45deg);}.heart:after,.heart:before{content: '';width: inherit;height: inherit;background: inherit;border-radius: 50%;-webkit-border-radius: 50%;-moz-border-radius: 50%;position: fixed;}.heart:after{top: -5px;}.heart:before{left: -5px;}"), n(), r()}(window, document);
</script>
<h2>安装Git&Node.js</h2>
<span>Git:<a href="https://git-scm.com/">https://git-scm.com/</a></span>
<span>Node.js:<a href="https://nodejs.org/en/">https://nodejs.org/en/</a></span>
<h2>安装Hexo</h2>
<span>安装完上面的Git和Node.js后，输入下面的命令安装Hexo</span>
<p>{% codeblock %}$ npm install -g hexo-cli{% endcodeblock %}</p>
<span>输入下面的命令创建Hexo目录</span>
<p>{% codeblock %}$ hexo init
或$ hexo init &lt;想要用于存放hexo的目录&gt;{% endcodeblock %}</p>
<span>使用cd命令打开文件夹位置</span>
<p>{% codeblock %}$ cd &lt;存放hexo的目录&gt;{% endcodeblock %}
<span>然后输入<span>
<p>{% codeblock %}$ npm install{% endcodeblock %}</p>
<h2>命令</h2>
<span>新建一篇文章。如果没有设置 layout 的话，默认使用 _config.yml 中的 default_layout 参数代替。如果标题包含空格的话，请使用引号括起来。</span>
<p>{% codeblock %}$ hexo new [layout] &lt;文章标题&gt;{% endcodeblock %}</p>
<span>生成静态文件</span>
<p>{% codeblock %}$ hexo generate
缩写：$ hexo g{% endcodeblock %}</p>
<span>启动服务器。默认情况下，访问网址为： <a href="http://localhost:4000">http://localhost:4000</a></span>
<p>{% codeblock %}$ hexo server{% endcodeblock %}<br />
缩写：{% codeblock %}$ hexo s{% endcodeblock %}</p>
<span>部署网站</span>
<p>{% codeblock %}$ hexo deploy
缩写：$ hexo d{% endcodeblock %}</p>
<span>清理hexo的缓存</span>
<p>{% codeblock %}$ hexo clean{% endcodeblock %}</p>
