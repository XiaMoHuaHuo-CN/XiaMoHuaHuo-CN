---
title: 'Git教程'
date: 2021-04-02 16:26:15
tag: 教程
---
<script type="text/javascript"> 
 !function (e, t, a) {function r() {for (var e = 0; e < s.length; e++) s[e].alpha <= 0 ? (t.body.removeChild(s[e].el), s.splice(e, 1)) : (s[e].y--, s[e].scale += .004, s[e].alpha -= .013, s[e].el.style.cssText = "left:" + s[e].x + "px;top:" + s[e].y + "px;opacity:" + s[e].alpha + ";transform:scale(" + s[e].scale + "," + s[e].scale + ") rotate(45deg);background:" + s[e].color + ";z-index:99999");requestAnimationFrame(r)}function n() {var t = "function" == typeof e.onclick && e.onclick;e.onclick = function (e) {t && t(), o(e)}}function o(e) {var a = t.createElement("div");a.className = "heart", s.push({el: a,x: e.clientX - 5,y: e.clientY - 5,scale: 1,alpha: 1,color: c()}), t.body.appendChild(a)}function i(e) {var a = t.createElement("style");a.type = "text/css";try {a.appendChild(t.createTextNode(e))} catch (t) {a.styleSheet.cssText = e}t.getElementsByTagName("head")[0].appendChild(a)}function c() {return "rgb(" + ~~(255 * Math.random()) + "," + ~~(255 * Math.random()) + "," + ~~(255 * Math.random()) + ")"}var s = [];e.requestAnimationFrame = e.requestAnimationFrame || e.webkitRequestAnimationFrame || e.mozRequestAnimationFrame || e.oRequestAnimationFrame || e.msRequestAnimationFrame || function (e) {setTimeout(e, 1e3 / 60)}, i(".heart{width: 10px;height: 10px;position: fixed;background: #f00;transform: rotate(45deg);-webkit-transform: rotate(45deg);-moz-transform: rotate(45deg);}.heart:after,.heart:before{content: '';width: inherit;height: inherit;background: inherit;border-radius: 50%;-webkit-border-radius: 50%;-moz-border-radius: 50%;position: fixed;}.heart:after{top: -5px;}.heart:before{left: -5px;}"), n(), r()}(window, document);
</script>
<img src="https://z3.ax1x.com/2021/04/02/cmybiF.png" />
<h1>安装</h1>
<p>首先安装Git<br />
Git官网：<a href="http://git-scm.com/">http://git-scm.com/</a><br />
一路Next安装即可。<br />
然后你的右键菜单会多出下面两个按键：<br />
<b>Git GUI Here<br />
Git Bash Here</b></p>
<h1>配置Git</h1>
<p>我们先在电脑里找一块地方存放本地仓库(创建文件夹),然后在文件夹里右键点击<b>Git Bash Here</b>进入Git命令行，如下<br />
<img src="https://z3.ax1x.com/2021/04/02/cm6VsI.png" /><br />
为了保险起见，我们先执行git init命令:<br />
{% codeblock %}$ git init{% endcodeblock %}<br />
<img src="https://z3.ax1x.com/2021/04/02/cm6FRH.png" /><br />
为了把本地的仓库传到github，还需要配置ssh key。<br />
在本地创建ssh key的命令:<br />
{% codeblock %}$ ssh-keygen -t rsa -C "&lt;你注册github的邮箱&gt;"{% endcodeblock %}<br />
直接点回车，说明会在默认文件id_rsa上生成ssh key。 <br />
然后系统要求输入密码，直接按回车表示不设密码,重复密码时也是直接回车，之后提示你ssh key已经生成成功。<br />
<img src="https://z3.ax1x.com/2021/04/02/cm6iJe.png" /><br />
然后我们进入提示的地址下查看ssh key文件。 地址是<b>C:\Users\<电脑用户名>\.ssh</b>,比如<b>C:\Users\Administrator\.ssh</b>(注：部分电脑将&quot;Users&quot;文件夹显示为&quot;用户&quot;文件夹)<br />
用记事本等软件打开<b>id_rsa.pub</b>，复制里面的key。里面的key是一对看不懂的字符数字组合，不用管它，直接复制。<br />
<img src="https://z3.ax1x.com/2021/04/02/cm6kzd.png" /><br />
登录Github后打开<a href="https://github.com/settings/keys">https://github.com/settings/keys</a>，<b>点击New SSH Key</b>，title随便填，粘贴key。<br />
验证是否成功，在Git Bash输入：<br />
{% codeblock %}$ ssh -T git@github.com{% endcodeblock %}<br />
回车就会看到：Hi &lt;Github名&gt;! You’ve successfully authenticated, but GitHub does not provide shell access。这就表示已成功连上github。<br />
<img src="https://z3.ax1x.com/2021/04/02/cm6ZLt.png" /><br />
接下来我们要做的就是把本地仓库传到github上去，在此之前还需要设置username和email，因为github每次commit都会记录他们<br />
{% codeblock %}$ git config --global user.name "&lt;Github名称&gt;"
$ git config --global user.email "&lt;你注册github的邮箱&gt;"{% endcodeblock %}<br />
<img src="https://z3.ax1x.com/2021/04/02/cm6EQA.png" /><br />
进入要上传的仓库，右键git bash，添加远程地址:<br />
{% codeblock %}$ git remote add origin &lt;Github仓库ssh地址&gt;
$ git push origin &lt;Github仓库分支，默认master&gt;{% endcodeblock %}
然后在命令行输入一下命令:<br />
{% codeblock %}$ git add &lt;要上传的文件名称，全部请填*&gt;
$ git ci -m "&lt;上传描述&gt;"
git push命令会将本地仓库推送到远程服务器。
git pull命令则相反。{% endcodeblock %}<br />
注：首次提交，先git pull下，修改完代码后，使用git status可以查看文件的差别，使用git add 添加要commit的文件。</p>
