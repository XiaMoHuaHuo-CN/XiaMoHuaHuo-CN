---
title: '[原创][MCBBS]从零编写自己的开服批处理--轻松开服'
date: 2021-03-27 17:35:36
tag: MineCraft
---
<img src="https://z3.ax1x.com/2021/04/02/cmyqG4.png" /><br />
<h1>前言</h1>
<p>由于批处理文件的命令非常奇怪，而搜索的用法却总是不尽人意，于是，本人决定着手写一篇基础开服批处理编写教程，方便各位新人轻松开服。<br />
<font color="red">注意：编辑bat时请使用<i><u>ANSI</u></i>编码，否则部分内容将出现报错、乱码等问题，甚至无法启动</font></p>
<h1>第一章 基础知识</h1>
<p>在开始之前，我们要了解用得到的内容。<br />
<font color="blue"><b>@echo</b></font><br />
这是一个回执的命令，它用来控制控制台的回执。<br />
<font color="blue"><b>echo</b></font><br />
这是一个回执的命令。它能在控制台中添加一个回执。<br />
<font color="blue"><b>set</b></font><br />
这是一个设置变量的命令。这个命令可以用来优化Java参数。<br />
<font color="blue"><b>goto</b></font><br />
跳转命令。多用于崩溃自重启。<br />
<font color="blue"><b>Java</b></font><br />
调起Java进程。开服必备命令。<br />
<font color="blue"><b>title</b></font><br />
这是一个标题命令。设置控制台的窗口标题。<br />
<font color="blue"><b>color</b></font><br />
这是一个颜色命令。用于设置控制台背景与文字的颜色。<br />
<font color="blue"><b>timeout</b></font><br />
这是一个等待命令。以秒为单位。这个命令用于自重启等待。<br />
<font color="blue"><b>choice</b></font><br />
同上,这是一个等待命令。以秒为单位。这个命令用于自重启等待。</p>

<h1>第二章 初步启航</h1>
<p>本章开始正式教学。如果还有不懂，建议先消化第一章的内容。<br />
开服最简单的方式就是添加Java参数。如下所示：<br />
{% codeblock %}java -Xms&lt;最小内存&gt; -Xmx&lt;最大内存&gt; -jar &lt;开服核心名&gt;{% endcodeblock %}<br />
但是这样似乎过于简陋。对于我们，一定想进行优化和个性化。<br />
在“java -Xms&lt;最小内存&gt; -Xmx&lt;最大内存&gt; -jar &lt;开服核心名&gt;”中，如果使用高级Java参数，就会导致修改不方便，或者导致误删等问题。那么，我们用set命令来解决。<br />
set命令可以设置变量，那么我们只要设置+调用变量，即可轻松解决问题。如下所示：<br />
{% codeblock %}set Xms=&lt;最小内存&gt;
set Xmx=&lt;最大内存&gt;
set jar=&lt;开服核心名，无需后缀&gt;{% endcodeblock %}<br />
有了变量，那么我们就要调用变量。我们把变量调用至Java参数中。如下所示：<br />
{% codeblock %}java -Xms%Xms% -Xmx%Xmx% -jar %jar%.jar{% endcodeblock %}<br />
现在，你已经学会了最基础的内容，本章到此完结。</p>

<h1>第三章 小有学识</h1>
<p><img src="https://www.mcmod.cn/pages/tools/achievements/images/achievements/201504_ndqqLSUf.png" /><br />
服务器重启总是要手动？试试goto指令吧。如下所示:<br />
{% codeblock %}:1
goto 1{% endcodeblock %}<br />
这样就可以不断跳回1处。goto命令用:&lt;标记名&gt;来做标记，牢记此点可完善服务器。<br />
我们把参数加到中间，如下所示:<br />
{% codeblock %}:1
set Xms=&lt;最小内存&gt;
set Xmx=&lt;最大内存&gt;
set jar=&lt;开服核心名，无需后缀&gt;
java -Xms%Xms% -Xmx%Xmx% -jar %jar%.jar
goto 1{% endcodeblock %}<br />
重启是解决了，可是关服好像也会重启？试试timeout或者choice吧。如下所示:<br />
<span>timeout:</span><br />
{% codeblock %}set goto_time=&lt;自重启等待秒数&gt;
timeout /t %goto_time%{% endcodeblock %}<br />
<span>choice:</span><br />
{% codeblock %}set goto_time=&lt;自重启等待秒数&gt;
choice /c a /t %goto_time% /d a /n&gt;nul{% endcodeblock %}<br />
这样不就解决了吗。我们把它加到参数中，如下所示:<br />
<span>timeout:</span><br />
{% codeblock %}:1
set goto_time=&lt;自重启等待秒数&gt;
(略)
timeout /t %goto_time%
goto 1{% endcodeblock %}<br />
<span>choice:</span><br />
{% codeblock %}:1
set goto_time=&lt;自重启等待秒数&gt;
(略)
choice /c a /t %goto_time% /d a /n&gt;nul
goto 1{% endcodeblock %}<br />
这样就有了一个高级的批处理了。但是回执似乎很烦？把@echo加进去试试吧。如下所示：<br />
{% codeblock %}@echo off
(略){% endcodeblock %}<br />
现在，烦人的回执就被关掉了。<br />
你学会了这些内容，那么本章到此完结。</p>

<h1>第四章 扩展内容</h1>
<p><img src="https://www.mcmod.cn/pages/tools/achievements/images/achievements/0_qDrGhCsG.png" /><br />
这里是第四章，扩展内容。你可以在这里学到一些扩展内容。<br />
在这里，你将学到<font color="blue"><b>color、echo、title</b></font>三种代码的用法。<br />
背景和文字颜色好像太单调？还是黑底白字？我们来用<font color="blue"><b>color</b></font>设置颜色吧。如下所示：<br />
{% codeblock %}color &lt;文字颜色&gt;&lt;背景颜色&gt;{% endcodeblock %}<br />
颜色表:<br />
<img src="https://z3.ax1x.com/2021/04/02/cmy7IU.jpg" /><br />
听说你想增加回执？<font color="blue"><b>echo</b></font>满足你。如下所示：<br />
{% codeblock %}echo &lt;内容&gt;{% endcodeblock %}<br />
想自定义窗口标题？这个不难，<font color="blue"><b>title</b></font>可以做到。如下所示：<br />
{% codeblock %}title &lt;标题&gt;{% endcodeblock %}<br />
现在在你的批处理中加入他们做一个更高级的批处理来开服吧。<br />
本章到此完结。</p>
<h1>扩展教程</h1>
<div class="sample-form">
<form id="hcaptcha-demo-form" method="POST">
<div class="">
<div id="hcaptcha-demo" class="h-captcha" data-sitekey="3d162544-450b-4223-b895-dfcf219a416d" data-callback="onSuccess" data-expired-callback="onExpire"></div>
<script>
                      var onSuccess = function(response) {
                        var errorDivs = document.getElementsByClassName("hcaptcha-error");
                        if (errorDivs.length) {
                          errorDivs[0].className = "";
                        }
                        var errorMsgs = document.getElementsByClassName("hcaptcha-error-message");
                        if (errorMsgs.length) {
                          errorMsgs[0].parentNode.removeChild(errorMsgs[0]);
                        }
  var logEl = document.querySelector(".hcaptcha-success");
  logEl.innerHTML = '<p><b>扩展1：使用Notepad++编辑</b><br/>Windows自带的记事本的编码方式难改，而使用<b>Notepad++</b>可以轻松调节编码方式，而且其填充功能可以轻松填入代码，无需频繁输入。</p><p><b>扩展2：使用记事本排列图案</b><br/>想用回执排列符号图案？记事本是个好东西。记事本的显示比例与bat窗口完全一致，是个排列图案的好东西。注意，排列完后记得把内容复制到编辑器里。</p>'
                      };
                      var onExpire = function(response) {
                        var logEl = document.querySelector(".hcaptcha-success");
                        logEl.innerHTML = '人机验证token已过期'
              };
</script>
</div>
</form>
<div class="hcaptcha-success smsg" aria-live="polite"></div>
</div>
<h1>白嫖区！！！</h1>
<p>白嫖bat↓↓↓纯手打<br />
<a href="http://repo.huahuo-cn.tk/Start.bat">http://repo.huahuo-cn.tk/Start.bat</a><br />
<br/>
开服高级参数：<br/>
{% codeblock %}-Xms&lt;最大内存&gt; -Xmx&lt;最小内存&gt; -XX:+UseG1GC -server -XX:+UseFastAccessorMethods -XX:+OptimizeStringConcat -XX:+AggressiveOpts -XX:MaxGCPauseMillis=10 -XX:+UseStringDeduplication -jar &lt;核心名&gt;.jar{% endcodeblock %}</p>
