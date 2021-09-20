---
title: Hexo云构建
date: 2021-09-019 09:26:15
tag: 教程
---
原理是通过Vercel提供的功能进行云构建，所以跟用Vercel部署网站是差不多的
<h1>上传文件至GitHub</h1>
<p>将Hexo的文件上传至GitHub，nodejs的文件不用上传，如果主题文件是用git clone的，要先删除主题文件夹的.git文件夹</p>
<h1>在Vercel创建项目</h2>
<p>在Vercel上新建一个项目，导入刚才上传的储存库，选择Hexo框架，然后部署就可以自动构建了</p>
<br />demo:<iframe height="600" src="https://hexo-cloud-builds-demo.vercel.app/"></iframe>
