---
title: 'Hexo Blog安装'
date: 2021-03-21 11:29:32
tag: 教程
---
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
