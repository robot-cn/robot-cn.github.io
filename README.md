# 这是测速文档

<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
    "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml" id="sixapart-standard">
<head>
    <meta http-equiv="Content-Type" content="text/html; charset=UTF-8" />
<meta name="generator" content="Movable Type  5.2.2" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<!--link rel="stylesheet" href="http://www.ruanyifeng.com/blog/styles.css" type="text/css" /-->
<link rel="start" href="http://www.ruanyifeng.com/blog/" title="Home" />
<link rel="alternate" type="application/atom+xml" title="Recent Entries" href="http://feeds.feedburner.com/ruanyifeng" />
<script type="text/javascript" src="http://www.ruanyifeng.com/blog/mt.js"></script>
<!--
<rdf:RDF xmlns="http://web.resource.org/cc/"
         xmlns:dc="http://purl.org/dc/elements/1.1/"
         xmlns:rdf="http://www.w3.org/1999/02/22-rdf-syntax-ns#">
<Work rdf:about="http://www.ruanyifeng.com/blog/2014/10/real-leadership-lessons-of-steve-jobs.html">
<dc:title>乔布斯的管理课</dc:title>
<dc:description>2011年11月出版的《乔布斯传》很畅销，也写得很好，我还写过一篇读后感。...</dc:description>
<dc:creator>阮一峰</dc:creator>
<dc:date>2014-10-02T12:13:53+08:00</dc:date>
<license rdf:resource="http://creativecommons.org/licenses/by-nc-nd/3.0/" />
</Work>
<License rdf:about="http://creativecommons.org/licenses/by-nc-nd/3.0/">
</License>
</rdf:RDF>
-->

<style>
body {
  background-color: #f5f5d5;
}

#container::before {
  display: block;
  width: 100%;
  padding: 10px;
  background: rgba(0,0,0,0.1);
  text-align: center;
  content: "本站显示不正常，可能因为您使用了广告拦截器。";
}

</style>
<script>
function loadjscssfile(filename, filetype){
    if (filetype=="js"){ //if filename is a external JavaScript file
        var fileref=document.createElement('script')
        fileref.setAttribute("type","text/javascript")
        fileref.setAttribute("src", filename)
    }
    else if (filetype=="css"){ //if filename is an external CSS file
        var fileref=document.createElement("link")
        fileref.setAttribute("rel", "stylesheet")
        fileref.setAttribute("type", "text/css")
        fileref.setAttribute("href", filename)
    }
    if (typeof fileref!="undefined")
        document.getElementsByTagName("head")[0].appendChild(fileref)
}
//loadjscssfile("http://www.ruanyifeng.com/blog/styles.css", "css");
loadjscssfile('/static/themes/theme_scrapbook/theme_scrapbook.min.css', "css");


function checker() {
// var img = document.querySelector('img[src^="http://www.ruanyifeng.com/blog/images"]');
var img = document.querySelector('a > img[src*="wangbase.com/blogimg/asset/"]');
  if (img && window.getComputedStyle(img).display === 'none'){
    var sponsor = document.querySelector('.entry-sponsor');
    var prompt = document.createElement('div');
    prompt.style = 'border: 1px solid #c6c6c6;border-radius: 4px;background-color: #f5f2f0;padding: 15px; font-size: 14px;';
  prompt.innerHTML = '<p>您使用了广告拦截器，导致本站内容无法显示。</p><p>请将 www.ruanyifeng.com 加入白名单，解除广告屏蔽后，刷新页面。谢谢。</p>';
    sponsor.parentNode.replaceChild(prompt, sponsor);
    document.querySelector('#main-content').innerHTML = '';
  }
}

setTimeout(checker, 1000);
</script>

    
    <link rel="prev" href="http://www.ruanyifeng.com/blog/2012/08/diary_of_wildlife_conservation.html" title="斑头雁守护日记（转载）" />
    <link rel="next" href="http://www.ruanyifeng.com/blog/2012/08/how_to_read_diff.html" title="读懂diff" />
    
    <title>搭建一个免费的，无限流量的Blog----github Pages和Jekyll入门 - 阮一峰的网络日志</title>
</head>
<body id="scrapbook" class="mt-entry-archive one-column">
<script>
if (/mobile/i.test(navigator.userAgent) || /android/i.test(navigator.userAgent)) document.body.classList.add('mobile');

/*
window.addEventListener('load', function(event) {
  setTimeout(function () {
    hab('#sup-post-2');
    hab('#cre-inner');
  }, 1000);
});
*/
</script>
    <div id="container">
        <div id="container-inner">

            <div id="header">
    <div id="header-inner">
        <div id="header-content">


            <div id="header-name">阮一峰的网络日志 <span id="site_location"> » <a href="http://www.ruanyifeng.com/blog/" accesskey="1">首页</a></span><span id="site_archive"> » <a href="http://www.ruanyifeng.com/blog/archives.html">档案</a></span>
</div>

<div id="google_search">
<!-- SiteSearch Google -->
<form action="https://www.baidu.com/s" target="_blank" method="get" id="cse-search-box">
  <div>
  <input type="text" size="20" name="origin" class="searchbox" id="sbi" value="" />
  <input type="hidden" name="wd" value="" />
  <!--input type="image" src="/static/themes/theme_scrapbook/images/top_search_submit.gif" class="searchbox_submit" value="" alt="搜索" name="sa" onclick="this.form.wd.value = this.form.origin.value + ' inurl:www.ruanyifeng.com/blog'" /-->
  <input type="image" src="/static/themes/theme_scrapbook/images/top_search_submit.gif" class="searchbox_submit" value="" alt="搜索" name="sa" onclick="this.form.wd.value = this.form.origin.value + ' 阮一峰'" />
</div>
</form>

<!-- SiteSearch Google -->
</div>
<div id="feed_icon">
<a href="/feed.html" title="订阅Feed">
<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACAAAAAgCAYAAABzenr0AAAABGdBTUEAAK/INwWK6QAAABl0RVh0U29mdHdhcmUAQWRvYmUgSW1hZ2VSZWFkeXHJZTwAAAUzSURBVHjavFdbbFRVFF3nPjoz7dTWTittaW0jUDRAUqaNojyqREnEQKgfUj9MqqAmhqRt/OCD4CuY+Kckoh+aiGKC+gMJbdHoRysJ8dkhhmJLNdDKtJU+6GMK87j3Hs85d2Z6HzNtMYWb3Dn3NWftvfba+5xNYDl+e6Fkj6yqb/oDRbWq14vlPBLRKCITkxf0ROLt+hNjp1PPSRK4kA3vF1dXNRcWlyA2OQU9eos9opAkAiKxD+XkKO6t15aRWO7J/MgmAZU8MEgexgZHMX518Dh72sYMmVKShnxWuWHdHtxKIDIYTgMuDzgfmSOIQkYMpdUF8OY92Hytt4/jvkg47czzU16iQovM3QFwmNck+Yyduu7D6NA0Z6JR4THntFs9V4tWQg6Ui3s6MwKDncsFTnXKLJhDSeUK3AgPtyhccDzmVs999buRt/1Vm4i0od+hX7+MRG87jPGB/w1u8FPj9xEw7McVrnYuOCvtpjTth3J/nTg99c8LRhKhr6D3dTB5R24bXFwbMXBsyZzeoXaycEpJ95TB09AGX/NpqLVNtw8urnVzLvHjFNxiFqRy2OOHuqUVnue+ACkoWzo4O6lGzTmuHq6nPvY2m9rVqjrIK2rMEKxqyG5NPAKt+wjo0LklgfNxJkZMA3KJvqRUk3z5UFY3QH14P0h+WUY79HPvgv7VuSg4ZRGY1YgZgqXmORccF17sy2ehnf9AeO085K2HQFbtXBScj0LcpgF2cN+WV+DZ/LJQu6gD4R7oV7pBJwbSgtMvfiPoVp56DySwxm7EtkMs1WdAB7qzggsDJKQYsHucSkOudrkiCPWR/fA2nYCn8SNIK4NptSMyAu3sAdDRkIsJdfth0LzSrODUoPNZ4KI9SxJI5UHk7D4GdQfz2us31c7CoHMjRkKuDPHseCMrONVhNcDJwMJpKFVvg9L4OaTiNWm1x789KCqkrXhVBiEz0WYCT2nAzQAD1/vaETv1GrRfP4Vx5cfMNcDPwvP0h0DhanPym7OIf/+O67vcJ1/PCJ4KgdzaUP6Wz+dU+5yIL6fV+PsHGAOdwlPpvvUOyeeAVGyCdqkDNB6DPjsBSrnndfOGevOh3RhGItxvA+fX1CtbGFhgYUFkFMZPR6F1HnClHq8HyubWtJexX06CRmdt33hrd7nA7SFY4qoGpnYuOKcRykPPgDCBcsHx9Iv+fNL2PueBehCWUfYQIIMGLOCcOmXDXsh1+yCt35tUPfvzGFuSvzvoinXOxqa02qOhM6733nVP2MAdaej2XN11DPKjLZCD+yBvahGCo7JfTKAN9UD7s8Oe9zUNIhz8fWI8DG2k38WCFdxugANcXrvTVd1IEbuv3Jour7Hzn7jLMBNfKs7R3i67gRVrbeCOEDhinmWhAatsqdquM2XzHZINhK2cqTjHr/XZdVJUbgN3MWAVXKbSyg9jesRW2xP9di+lwrL5ojM3m2H/kG9hwcIA37c71W6wJdW2J2S5nrjYbq/t1AHAhJsKQeyfPvf6IMJgghPJhFZ4x0KlfLFvt22du45Au/A1SOlGc0P672XXwhLtOcM0kTTEMMd0qkVmMNXxMd/tsedUjInr4SQDgOfeXMSiN0FCL5WHah4L1qqYXPJOJlttd+a5M+YpcG5poLYKQ5f+6JJ4r8bbJYP47hq4r7QAs9PjYNhHJd4o8l5taiwuOpa7AS4XKqI/5NjJbTnaWK92nLdLuhQAJayRNMiygXPBeQN+Qbvu0zDc3y+aUzhbkGR73sI7ljvUnndx2q3t+X8CDAD66FtrIL864AAAAABJRU5ErkJggg==" alt="" style="border: 0pt none;" />
</a></div>

        </div>
    </div>
</div>



            <div id="content">
                <div id="content-inner">


                    <div id="alpha">
                        <div id="alpha-inner">


                            <div id="entry-1737" class="entry-asset asset hentry">
                                <div class="asset-header">
<div class="asset-nav entry-nav">

<div class="entry-location">
<ul>
<li>上一篇：<a href="http://www.ruanyifeng.com/blog/2012/08/diary_of_wildlife_conservation.html" title="斑头雁守护日记（转载）">斑头雁守护日记（转载）</a></li>
<li>下一篇：<a href="http://www.ruanyifeng.com/blog/2012/08/how_to_read_diff.html" title="读懂diff">读懂diff&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</a></li>
</ul>
</div>


    
                                    <div class="entry-categories">
                                        <p>分类<span class="delimiter">：</span></p>
                                        <ul>
                                            <li><a href="http://www.ruanyifeng.com/blog/developer/" rel="tag">开发者手册</a></li>
                                        </ul>
                                    </div>
    


                                            
<div class="entry-location-mobile" style="float: right;">
<ul>
<li><a href="http://www.ruanyifeng.com/blog/2012/08/diary_of_wildlife_conservation.html" title="斑头雁守护日记（转载）">⇐&nbsp;</a></li>
<li><a href="http://www.ruanyifeng.com/blog/2012/08/how_to_read_diff.html" title="读懂diff">&nbsp;⇒</a></li>
</ul>
</div>

</div>
</div>

                          
<article class="hentry">
                                    <h1 id="page-title" class="asset-name entry-title">搭建一个免费的，无限流量的Blog----github Pages和Jekyll入门</h1>
                                            <div id="share_button" class="social-share" style="float:right;padding-right:2em;padding-top:1em;"></div>

<div class="asset-meta">
                                        

                                            <p class="vcard author">作者： <a class="fn url" href="http://www.ruanyifeng.com">阮一峰</a></p>
                                    <p>日期： <a href="http://www.ruanyifeng.com/blog/2012/08/"><abbr class="published" title="2012-08-25T18:32:38+08:00">2012年8月25日</abbr></a></p>


</div>








                                
                                <div class="asset-content entry-content" id="main-content">

                                    <!-- div class="asset-body" -->
                                        <p>喜欢写Blog的人，会经历三个阶段。</p>
                                    <!-- /div -->


                                    <!-- div id="more" class="asset-more" -->
                                        <blockquote>

<p>　　第一阶段，刚接触Blog，觉得很新鲜，试着选择一个免费空间来写。</p>

<p>　　第二阶段，发现免费空间限制太多，就自己购买域名和空间，搭建独立博客。</p>

<p>　　第三阶段，觉得独立博客的管理太麻烦，最好在保留控制权的前提下，让别人来管，自己只负责写文章。</p>

</blockquote>

<p>大多数Blog作者，都停留在第一和第二阶段，因为第三阶段不太容易到达：你很难找到俯首听命、愿意为你管理服务器的人。</p>

<p><img src="/blogimg/asset/201208/bg2012082501.jpg" /></p>

<p>但是两年前，情况出现变化，一些程序员开始在<a href="https://github.com/">ｇithub</a>网站上搭建blog。他们既拥有绝对管理权，又享受github带来的便利----不管何时何地，只要向主机提交commit，就能发布新文章。更妙的是，这一切还是免费的，github提供无限流量，世界各地都有理想的访问速度。</p>

<p>今天，我就来示范如何在github上搭建Blog，你可以从中掌握github的Pages功能，以及Jekyll软件的基本用法。更重要的是，你会体会到一种建立网站的全新思路。</p>

<p><img src="/blogimg/asset/201208/bg2012082502.jpg" /></p>

<p><strong>一、Github Pages 是什么？</strong></p>

<p>如果你对编程有所了解，就一定听说过<a href="https://github.com/">github</a>。它号称程序员的Facebook，有着极高的人气，许多重要的项目都托管在上面。</p>

<p>简单说，它是一个具有版本管理功能的代码仓库，每个项目都有一个主页，列出项目的源文件。</p>

<p><img src="/blogimg/asset/201208/bg2012082503.jpg" /></p>

<p>但是对于一个新手来说，看到一大堆源码，只会让人头晕脑涨，不知何处入手。他希望看到的是，一个简明易懂的网页，说明每一步应该怎么做。因此，github就设计了<a href="http://pages.github.com/">Pages功能</a>，允许用户自定义项目首页，用来替代默认的源码列表。<strong>所以，github Pages可以被认为是用户编写的、托管在github上的静态网页。</strong></p>

<p><img src="/blogimg/asset/201208/bg2012082504.jpg" /></p>

<p>github提供模板，允许<a href="https://help.github.com/articles/creating-pages-with-the-automatic-generator">站内生成</a>网页，但也允许用户自己编写网页，然后上传。有意思的是，这种上传并不是单纯的上传，而是会经过Jekyll程序的再处理。</p>

<p><strong>二、Jekyll是什么？</strong></p>

<p><strong><a href="http://jekyllrb.com/">Jekyll</a>（发音/'dʒiːk əl/，"杰克尔"）是一个静态站点生成器，它会根据网页源码生成静态文件。</strong>它提供了模板、变量、插件等功能，所以实际上可以用来编写整个网站。</p>

<p><img src="/blogimg/asset/201208/bg2012082505.jpg" /></p>

<p><strong>整个思路到这里就很明显了。你先在本地编写符合Jekyll规范的网站源码，然后上传到github，由github生成并托管整个网站。</strong></p>

<p>这种做法的好处是：</p>

<blockquote>

<p>　　* 免费，无限流量。</p>

<p>　　* 享受git的版本管理功能，不用担心文章遗失。</p>

<p>　　* 你只要用自己喜欢的编辑器写文章就可以了，其他事情一概不用操心，都由github处理。</p>

</blockquote>

<p>它的缺点是：</p>

<blockquote>

<p>　　* 有一定技术门槛，你必须要懂一点git和网页开发。</p>

<p>　　* 它生成的是静态网页，添加动态功能必须使用外部服务，比如评论功能就只能用<a href="http://disqus.com/">disqus</a>。</p>

<p>　　* 它不适合大型网站，因为没有用到数据库，每运行一次都必须遍历全部的文本文件，网站越大，生成时间越长。</p>

</blockquote>

<p>但是，综合来看，它不失为搭建中小型Blog或项目主页的最佳选项之一。</p>

<p><strong>三、一个实例</strong></p>

<p>下面，我举一个实例，演示如何在github上搭建blog，你可以跟着一步步做。为了便于理解，这个blog只有最基本的功能。</p>

<p>在搭建之前，你必须已经安装了<a href="http://git-scm.com/book/en/Getting-Started-Installing-Git">git</a>，并且有<a href="https://github.com/">github</a>账户。</p>

<p><strong>第一步，创建项目。</strong></p>

<p>在你的电脑上，建立一个目录，作为项目的主目录。我们假定，它的名称为jekyll_demo。</p>

<blockquote>

<p>　　$ mkdir jekyll_demo</p>

</blockquote>

<p>对该目录进行git初始化。</p>

<blockquote>

<p>　　$ cd jekyll_demo</p>

<p>　　$ git init</p>

</blockquote>

<p>然后，创建一个没有父节点的分支gh-pages。因为github规定，只有该分支中的页面，才会生成网页文件。</p>

<blockquote>

<p>　　$ git checkout --orphan gh-pages</p>

</blockquote>

<p>以下所有动作，都在该分支下完成。</p>

<p><strong>第二步，创建设置文件。</strong></p>

<p>在项目根目录下，建立一个名为_config.yml的文本文件。它是jekyll的设置文件，我们在里面填入如下内容，其他设置都可以用默认选项，具体解释参见<a href="https://github.com/mojombo/jekyll/wiki/Configuration">官方网页</a>。</p>

<blockquote>

<p>　　baseurl:  /jekyll_demo</p>

</blockquote>

<p>目录结构变成：</p>

<blockquote>

<p>　　/jekyll_demo<br />
　　　　|--　_config.yml</p>

</blockquote>

<p><strong>第三步，创建模板文件。</strong></p>

<p>在项目根目录下，创建一个_layouts目录，用于存放模板文件。</p>

<blockquote>

<p>　　$ mkdir _layouts</p>

</blockquote>

<p>进入该目录，创建一个default.html文件，作为Blog的默认模板。并在该文件中填入以下内容。</p>

<blockquote>

<p>　　&lt;!DOCTYPE html&gt;</p>

<p>　　&lt;html&gt;</p>

<p>　　&lt;head&gt;</p>

<p>　　　　&lt;meta http-equiv="content-type" content="text/html; charset=utf-8" /&gt;</p>

<p>　　　　&lt;title&gt;{{ page.title }}&lt;/title&gt;</p>

<p>　　&lt;/head&gt;</p>

<p>　　&lt;body&gt;<br />
 <br />
　　　　{{ content }}<br />
  <br />
　　&lt;/body&gt;</p>

<p>　　&lt;/html&gt;</p>

</blockquote>

<p>Jekyll使用<a href="https://github.com/shopify/liquid/wiki/liquid-for-designers">Liquid模板语言</a>，{{ page.title }}表示文章标题，{{ content }}表示文章内容，更多模板变量请参考<a href="https://github.com/mojombo/jekyll/wiki/Template-Data">官方文档</a>。</p>

<p>目录结构变成：</p>

<blockquote>

<p>　　/jekyll_demo<br />
　　　　|--　_config.yml<br />
　　　　|--　_layouts<br />
　　　　|　　　|--　default.html </p>

</blockquote>

<p><strong>第四步，创建文章。</strong></p>

<p>回到项目根目录，创建一个_posts目录，用于存放blog文章。</p>

<blockquote>

<p>　　$ mkdir _posts</p>

</blockquote>

<p>进入该目录，创建第一篇文章。文章就是普通的文本文件，文件名假定为2012-08-25-hello-world.html。(注意，文件名必须为"年-月-日-文章标题.后缀名"的格式。如果网页代码采用html格式，后缀名为html；如果采用<a href="http://daringfireball.net/projects/markdown/">markdown</a>格式，后缀名为md。）</p>

<p>在该文件中，填入以下内容：（注意，行首不能有空格）</p>

<blockquote>

<p>　　---<br />
　　layout: default<br />
　　title: 你好，世界<br />
　　---</p>

<p>　　&lt;h2&gt;{{ page.title }}&lt;/h2&gt;</p>

<p>　　&lt;p&gt;我的第一篇文章&lt;/p&gt;</p>

<p>　　&lt;p&gt;{{ page.date | date_to_string }}&lt;/p&gt;</p>

</blockquote>

<p>每篇文章的头部，必须有一个<a href="https://github.com/mojombo/jekyll/wiki/YAML-Front-Matter">yaml文件头</a>，用来设置一些元数据。它用三根短划线"---"，标记开始和结束，里面每一行设置一种元数据。"layout:default"，表示该文章的模板使用_layouts目录下的default.html文件；"title: 你好，世界"，表示该文章的标题是"你好，世界"，如果不设置这个值，默认使用嵌入文件名的标题，即"hello world"。</p>

<p>在yaml文件头后面，就是文章的正式内容，里面可以使用模板变量。{{ page.title }}就是文件头中设置的"你好，世界"，{{ page.date   }}则是嵌入文件名的日期（也可以在文件头重新定义date变量），"| date_to_string"表示将page.date变量转化成人类可读的格式。</p>

<p>目录结构变成：</p>

<blockquote>

<p>　　/jekyll_demo<br />
　　　　|--　_config.yml<br />
　　　　|--　_layouts<br />
　　　　|　　　|--　default.html <br />
　　　　|--　_posts<br />
　　　　|　　　|--　2012-08-25-hello-world.html</p>

</blockquote>

<p><strong>第五步，创建首页。</strong></p>

<p>有了文章以后，还需要有一个首页。</p>

<p>回到根目录，创建一个index.html文件，填入以下内容。</p>

<blockquote>

<p>　　---<br />
　　layout: default<br />
　　title: 我的Blog<br />
　　---</p>

<p>　　&lt;h2&gt;{{ page.title }}&lt;/h2&gt;</p>

<p>　　&lt;p&gt;最新文章&lt;/p&gt;</p>

<p>　　&lt;ul&gt;</p>

<p>　　　　{% for post in site.posts %}  </p>

<p>　　　　　　&lt;li&gt;{{ post.date | date_to_string }} &lt;a href="{{ site.baseurl }}{{ post.url }}"&gt;{{ post.title }}&lt;/a&gt;&lt;/li&gt;</p>

<p>　　　　{% endfor %}</p>

<p>　　&lt;/ul&gt;</p>

</blockquote>

<p>它的Yaml文件头表示，首页使用default模板，标题为"我的Blog"。然后，首页使用了{% for post in site.posts %}，表示对所有帖子进行一个遍历。这里要注意的是，Liquid模板语言规定，输出内容使用两层大括号，单纯的命令使用一层大括号。至于{{site.baseurl}}就是_config.yml中设置的baseurl变量。</p>

<p>目录结构变成：</p>

<blockquote>

<p>　　/jekyll_demo<br />
　　　　|--　_config.yml<br />
　　　　|--　_layouts<br />
　　　　|　　　|--　default.html <br />
　　　　|--　_posts<br />
　　　　|　　　|--　2012-08-25-hello-world.html<br />
　　　　|--　index.html</p>

</blockquote>

<p><strong>第六步，发布内容。</strong></p>

<p>现在，这个简单的Blog就可以发布了。先把所有内容加入本地git库。</p>

<blockquote>

<p>　　$ git add .</p>

<p>　　$ git commit -m "first post"</p>

</blockquote>

<p>然后，前往github的网站，在网站上创建一个名为jekyll_demo的库。接着，再将本地内容推送到github上你刚创建的库。注意，下面命令中的username，要替换成你的username。</p>

<blockquote>

<p>　　$ git remote add origin https://github.com/<strong>username</strong>/jekyll_demo.git</p>

<p>　　$ git push origin gh-pages</p>

</blockquote>

<p>上传成功之后，等10分钟左右，访问<strong>http://username.github.com/jekyll_demo/</strong>就可以看到Blog已经生成了（将username换成你的用户名）。</p>

<p>首页：</p>

<p><img src="/blogimg/asset/201208/bg2012082506.jpg" /></p>

<p>文章页面：</p>

<p><img src="/blogimg/asset/201208/bg2012082507.jpg" /></p>

<p><strong>第七步，绑定域名。</strong></p>

<p>如果你不想用<strong>http://username.github.com/jekyll_demo/</strong>这个域名，可以换成自己的域名。</p>

<p>具体方法是在repo的根目录下面，新建一个名为CNAME的文本文件，里面写入你要绑定的域名，比如example.com或者xxx.example.com。</p>

<p>如果绑定的是顶级域名，则DNS要新建一条A记录，指向204.232.175.78。如果绑定的是二级域名，则DNS要新建一条CNAME记录，指向username.github.com（请将username换成你的用户名）。此外，别忘了将_config.yml文件中的baseurl改成根目录"/"。</p>

<p>至此，最简单的Blog就算搭建完成了。进一步的完善，请参考Jekyll创始人的<a href="https://github.com/mojombo/tpw">示例库</a>，以及其他用Jekyll搭建的<a href="https://github.com/mojombo/jekyll/wiki/Sites">blog</a>。</p>

<p>（完）</p>
                                    <!-- /div -->

                                </div>
    <script type="text/javascript" src="/newwindow.js"></script>
                                <div class="asset-footer">

<h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（<a href="http://creativecommons.org/licenses/by-nc-nd/3.0/deed.zh">创意共享3.0许可证</a>）</li>
<li>发表日期： <abbr class="published" title="2012-08-25T18:32:38+08:00">2012年8月25日</abbr></li>

</ul>
                                </div>
</article>
                            </div>

  <div style="display: inline-block ! important;width: 100%;">

  </div>

<div id="related_entries">
<h2>相关文章</h2>
<ul>

<li><strong>2020.04.27: <a href="http://www.ruanyifeng.com/blog/2020/04/git-cherry-pick.html">git cherry-pick 教程</a></strong>

                           <div class="entry-body">
                              对于多分支的代码库，将代码从一个分支转移到另一个分支是常见需求。

                           </div>

</li>

 
<li><strong>2020.04.16: <a href="http://www.ruanyifeng.com/blog/2020/04/bash-tutorial.html">《Bash 脚本教程》发布了</a></strong>

                           <div class="entry-body">
                              过去三个月，我一直在写《Bash 脚本教程》，现在终于写完了。

                           </div>

</li>

 
<li><strong>2020.02.23: <a href="http://www.ruanyifeng.com/blog/2020/02/sparql.html">RDF 和 SPARQL 初探：以维基数据为例</a></strong>

                           <div class="entry-body">
                              维基百科有一个姐妹项目，叫做"维基数据"（Wikidata）。你可以从维基百科左侧边栏点进去。

                           </div>

</li>

 
<li><strong>2020.01.14: <a href="http://www.ruanyifeng.com/blog/2020/01/ffmpeg.html">FFmpeg 视频处理入门教程</a></strong>

                           <div class="entry-body">
                              FFmpeg 是视频处理最常用的开源软件。

                           </div>

</li>

 
</ul>
</div>



                    

                    <div id="comments" class="comments">


    
    
        
    <h2 class="comments-header">留言（188条）</h2>

    <div id="comments-content" class="comments-content" style="clear: left;">
        
        <div id="comment-262008" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://wonderflow.info" href="http://wonderflow.info" target="_blank" rel="nofollow">wonderflow</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262008">
            <p>请我博主的博客是按照这个方法构建的吗？</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 25, 2012  8:15 PM">2012年8月25日 20:15</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262008">#</a>
 | <a href="#comment-text" title="引用wonderflow的这条留言" onclick="return CommentQuote('comment-quote-262008','wonderflow');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262009" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://fangpeishi.tk" href="http://fangpeishi.tk" target="_blank" rel="nofollow">fps</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262009">
            <p>个人的小blog是这样的<br />
用的是基于jekyll的octopress</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 25, 2012  8:24 PM">2012年8月25日 20:24</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262009">#</a>
 | <a href="#comment-text" title="引用fps的这条留言" onclick="return CommentQuote('comment-quote-262009','fps');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262010" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">wonderflow</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262010">
            <p>嗯，受教了，以后有机会也学着搭一个~谢谢O(∩_∩)O~！。</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 25, 2012  8:29 PM">2012年8月25日 20:29</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262010">#</a>
 | <a href="#comment-text" title="引用wonderflow的这条留言" onclick="return CommentQuote('comment-quote-262010','wonderflow');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262011" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://www.icesoft.net/" href="http://www.icesoft.net/" target="_blank" rel="nofollow">王河豚</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262011">
            <p>我现在使用wodrpress 搭建在openshift上，也是免费的哦，也挺方便的。</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 25, 2012  8:51 PM">2012年8月25日 20:51</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262011">#</a>
 | <a href="#comment-text" title="引用王河豚的这条留言" onclick="return CommentQuote('comment-quote-262011','王河豚');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262012" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://reverland.github.com" href="http://reverland.github.com" target="_blank" rel="nofollow">reverland</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262012">
            <p>比较喜欢本地用vim来写东西，然后push上去，省心省力。还有就是觉得静态博客速度比较快，</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 25, 2012  9:26 PM">2012年8月25日 21:26</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262012">#</a>
 | <a href="#comment-text" title="引用reverland的这条留言" onclick="return CommentQuote('comment-quote-262012','reverland');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262013" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://dourok.info" href="http://dourok.info" target="_blank" rel="nofollow">DouO</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262013">
            <p>評論功能並不是只能用disqus，所有社會化評論服務都是可以整合進去的。disqus也因爲它不是開源的，在黑客社區受到一些批評。如果想玩 Static Blog Generators 的話，我推薦試一下 ruhoh.com 。是jekyll-bootstrap的作者，作了jekyll-bootstrap後重新思考出來的作品。</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 25, 2012  9:34 PM">2012年8月25日 21:34</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262013">#</a>
 | <a href="#comment-text" title="引用DouO的这条留言" onclick="return CommentQuote('comment-quote-262013','DouO');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262015" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://t.qq.com/michalliu" href="http://t.qq.com/michalliu" target="_blank" rel="nofollow">自由国度</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262015">
            <p>说中国人是蝗虫还真是不错，github被屏蔽了你就开心了？就像蝗虫，有好东西一拥而上，生怕自己抢不到，吃光了或不抢不过了就换下一个地方，继续搞。</p>

<p>这种东西需要写篇文章来宣传么，不知道宣传了以后的后果么，本来是个挺好的社区博客，有可能会因为你这一篇文章，搞的大家以后都用不了了，麻烦作者以后发文章前先考虑对社会的影响，对社区的影响，顾全大局...</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 25, 2012 10:09 PM">2012年8月25日 22:09</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262015">#</a>
 | <a href="#comment-text" title="引用自由国度的这条留言" onclick="return CommentQuote('comment-quote-262015','自由国度');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262017" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://maxellar.diandian.com/" href="http://maxellar.diandian.com/" target="_blank" rel="nofollow">杜顺帆</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262017">
            <p>我应该是按步骤做了，但为什么输入网址后仍是404？</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 25, 2012 10:13 PM">2012年8月25日 22:13</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262017">#</a>
 | <a href="#comment-text" title="引用杜顺帆的这条留言" onclick="return CommentQuote('comment-quote-262017','杜顺帆');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262018" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">屁民</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262018">
            <blockquote>
<pre>引用自由国度的发言：</pre>

<p>说中国人是蝗虫还真是不错，github被屏蔽了你就开心了？就像蝗虫，有好东西一拥而上，生怕自己抢不到，吃光了或不抢不过了就换下一个地方，继续搞。</p>

<p>这种东西需要写篇文章来宣传么，不知道宣传了以后的后果么，本来是个挺好的社区博客，有可能会因为你这一篇文章，搞的大家以后都用不了了，麻烦作者以后发文章前先考虑对社会的影响，对社区的影响，顾全大局...</p>

</blockquote>

<p>同意，早晚会像sourceforge一样把中国ip屏蔽的。。。。<br />
总想白占别人便宜。。。。自愿低别人一等。。。。 </p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 25, 2012 10:22 PM">2012年8月25日 22:22</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262018">#</a>
 | <a href="#comment-text" title="引用屁民的这条留言" onclick="return CommentQuote('comment-quote-262018','屁民');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262019" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://coursegarden.com" href="http://coursegarden.com" target="_blank" rel="nofollow">xvfeng</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262019">
            <p>输入”$ git checkout --orphan gh-pages“后，页面提示<br />
"You are on a branch yet to be born" 请问这个是怎么原因，如何解决？</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 25, 2012 10:36 PM">2012年8月25日 22:36</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262019">#</a>
 | <a href="#comment-text" title="引用xvfeng的这条留言" onclick="return CommentQuote('comment-quote-262019','xvfeng');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262022" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://maxellar.diandian.com/" href="http://maxellar.diandian.com/" target="_blank" rel="nofollow">杜顺帆</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262022">
            <p>为何网页仍是代码</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 25, 2012 11:04 PM">2012年8月25日 23:04</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262022">#</a>
 | <a href="#comment-text" title="引用杜顺帆的这条留言" onclick="return CommentQuote('comment-quote-262022','杜顺帆');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262024" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">weedge</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262024">
            <p>感谢博主分享，尝试着搭建一个。@自由国度的话很反感，好东西当然需要分享；不知道他说的话所表达的是啥意思。</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 25, 2012 11:12 PM">2012年8月25日 23:12</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262024">#</a>
 | <a href="#comment-text" title="引用weedge的这条留言" onclick="return CommentQuote('comment-quote-262024','weedge');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262025" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">Probe</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262025">
            <blockquote>
<pre>引用自由国度的发言：</pre>

<p>说中国人是蝗虫还真是不错，github被屏蔽了你就开心了？就像蝗虫，有好东西一拥而上，生怕自己抢不到，吃光了或不抢不过了就换下一个地方，继续搞。</p>

<p>这种东西需要写篇文章来宣传么，不知道宣传了以后的后果么，本来是个挺好的社区博客，有可能会因为你这一篇文章，搞的大家以后都用不了了，麻烦作者以后发文章前先考虑对社会的影响，对社区的影响，顾全大局...</p>

</blockquote>

<p>就算 github 真的被墙了，错的也是弄出墙的这些人，跟博主有半毛钱关系？</p>

<p>看到好的东西不分享出来，自己偷摸留着，这算什么心态？</p>

<p>见到出色的产品，我觉得最好的做法就是像博主一样毫无保留的介绍给别人，方便的话也捎带介绍一下墙是什么。人都有自己的判断力的，能通过对比分出好坏，能想明白他在网上受到了多大限制，为什么一些国外网站不被允许访问。</p>

<p>github 是好东西，但藏着不让大伙知道就可以不被墙了？我不这么看，反倒是当每个网民都知道事实的时候，就离墙消失的一天不远了，那时候大家安心的去用 github 不是更好吗？<br />
</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 25, 2012 11:13 PM">2012年8月25日 23:13</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262025">#</a>
 | <a href="#comment-text" title="引用Probe的这条留言" onclick="return CommentQuote('comment-quote-262025','Probe');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262028" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">阮一峰</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262028">
            <blockquote>
<pre>引用xvfeng的发言：</pre>

<p>输入”$ git checkout --orphan gh-pages“后，页面提示<br />
"You are on a branch yet to be born" 请问这个是怎么原因，如何解决？</p>

</blockquote>

<p>奇怪，我的git没报错……怀疑是不是你的版本没更新。</p>

<p>出现这个错误的原因可能是，必须先有master分支，然后才能创建其他分支。</p>

<p>你可以在git init之后，随便做一次git commit，然后再git checkout --orphan gh-pages，应该就不会报错了。</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 25, 2012 11:25 PM">2012年8月25日 23:25</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262028">#</a>
 | <a href="#comment-text" title="引用阮一峰的这条留言" onclick="return CommentQuote('comment-quote-262028','阮一峰');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262029" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">阮一峰</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262029">
            <blockquote>
<pre>引用杜顺帆的发言：</pre>

<p>为何网页仍是代码</p>

</blockquote>

<p>请确认yaml头是否书写正确。三根短划线前面，是不能有空格的！</p>

<p>如果你用windows，必须确认保存文件的时候不带BOM。<br />
</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 25, 2012 11:28 PM">2012年8月25日 23:28</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262029">#</a>
 | <a href="#comment-text" title="引用阮一峰的这条留言" onclick="return CommentQuote('comment-quote-262029','阮一峰');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262031" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://maxellar.diandian.com/" href="http://maxellar.diandian.com/" target="_blank" rel="nofollow">杜顺帆</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262031">
            <blockquote>
<pre>引用阮一峰的发言：</pre>

<p></p>

<p>请确认yaml头是否书写正确。三根短划线前面，是不能有空格的！</p>

<p>如果你用windows，必须确认保存文件的时候不带BOM。</p>

<p><br />
</p></blockquote>

<p>已经确认前面没空格，mac编辑的，可以帮忙看一下吗：https://github.com/Perrydu/maxellar</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 25, 2012 11:43 PM">2012年8月25日 23:43</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262031">#</a>
 | <a href="#comment-text" title="引用杜顺帆的这条留言" onclick="return CommentQuote('comment-quote-262031','杜顺帆');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262038" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://gbspacing.com" href="http://gbspacing.com" target="_blank" rel="nofollow">gb_2312</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262038">
            <p>昨天刚尝试这搭好，用的 octopress</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 26, 2012 12:40 AM">2012年8月26日 00:40</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262038">#</a>
 | <a href="#comment-text" title="引用gb_2312的这条留言" onclick="return CommentQuote('comment-quote-262038','gb_2312');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262041" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://t.qq.com/michalliu" href="http://t.qq.com/michalliu" target="_blank" rel="nofollow">自由国度</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262041">
            <blockquote>
<pre>引用Probe的发言：</pre>

<p>看到好的东西不分享出来，自己偷摸留着，这算什么心态？</p>

</blockquote>

<p>树大招风，凡木秀于林而风必摧之</p>

<p>github确实能让你打起免费的博客，但是请别盯着 免费 两个字去宣传它，这样做的结果是到最后大家谁也不用了，github本身并没有博客功能，github pages的初衷只是方便开发者为自己的项目做一个介绍的页面，展示文档之类的功能，你非要把他当成免费的博客去用，现在也没人限制你，我只是说大家要有点儿自觉性，一点儿公德心。不要像蝗虫一样，有免费生怕自己用不上，抢不到，相信关注这个博客的人也不至于连100块一年的空间都买不起</p>

<p>我不希望以后连github都要翻墙才能用，相信你也不愿意，你说是吧</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 26, 2012  1:23 AM">2012年8月26日 01:23</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262041">#</a>
 | <a href="#comment-text" title="引用自由国度的这条留言" onclick="return CommentQuote('comment-quote-262041','自由国度');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262045" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">Dem</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262045">
            <p>把口碑式传播说成蝗虫的是什么心态。。。要是真的"生怕自己抢不到"的话就不会分享了<br />
</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 26, 2012  2:06 AM">2012年8月26日 02:06</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262045">#</a>
 | <a href="#comment-text" title="引用Dem的这条留言" onclick="return CommentQuote('comment-quote-262045','Dem');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262055" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://www.galaxyyao.com" href="http://www.galaxyyao.com" target="_blank" rel="nofollow">Dem</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262055">
            <blockquote>
<pre>引用自由国度的发言：</pre>

<p>我不希望以后连github都要翻墙才能用，相信你也不愿意，你说是吧</p>

</blockquote>

<p>虽然标题里有“免费，无限流量的字眼”，但博主在文章一开始着重突出的是“觉得独立博客的管理太麻烦，最好在保留控制权的前提下，让别人来管，自己只负责写文章。”<br />
jekyll的开发者（GitHub员工，https://github.com/mojombo）也很开心地看到很多人实际使用这个技术（https://github.com/mojombo/jekyll/wiki/Sites，“It’s interesting to see what designs and features others have come up with.”）。列表里的站点很多是Host在GitHub上（随机挑了几个来ping）</p>

<p>从使用上来说，在当前，就算有编辑器辅助写HTML页面，还是比有现成后台管理系统的WordPress动态网站麻烦很多。连最基本的功能之一：搜索只能靠Google Custom Search还很难继续优化。短期内，想推广到让程序员之外的人使用基本没戏的。现在就考虑屏蔽什么的真是想太多了。单纯当成jekyll技术介绍就行。</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 26, 2012  2:38 AM">2012年8月26日 02:38</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262055">#</a>
 | <a href="#comment-text" title="引用Dem的这条留言" onclick="return CommentQuote('comment-quote-262055','Dem');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262070" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">中学同学</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262070">
            <p>非常感谢!!!</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 26, 2012  4:17 AM">2012年8月26日 04:17</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262070">#</a>
 | <a href="#comment-text" title="引用中学同学的这条留言" onclick="return CommentQuote('comment-quote-262070','中学同学');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262079" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">阮一峰</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262079">
            <blockquote>
<pre>引用杜顺帆的发言：</pre>

<p>已经确认前面没空格，mac编辑的，可以帮忙看一下吗：https://github.com/Perrydu/maxellar</p>

</blockquote>

<p>我不知道为什么，你上传到github的，已经是生成好的网页了。</p>

<p>建议仔细研究Jekyll的示例库：https://github.com/mojombo/tpw</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 26, 2012  6:25 AM">2012年8月26日 06:25</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262079">#</a>
 | <a href="#comment-text" title="引用阮一峰的这条留言" onclick="return CommentQuote('comment-quote-262079','阮一峰');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262083" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://onetipperday.blogspot.com/" href="http://onetipperday.blogspot.com/" target="_blank" rel="nofollow">sterding</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262083">
            <p>阮兄，一直订阅你的blog，受益匪浅，多谢！</p>

<p>我按照你的steps，上传等都没有错误，但是网页显示404错误，帮我看一下好吗？<br />
地址：https://github.com/sterding/myhome/</p>

<p>btw，我是在mac下做的。<br />
</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 26, 2012  7:34 AM">2012年8月26日 07:34</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262083">#</a>
 | <a href="#comment-text" title="引用sterding的这条留言" onclick="return CommentQuote('comment-quote-262083','sterding');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262086" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">阮一峰</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262086">
            <p>@sterding：</p>

<p>2012-08-25-my-first-blog-in-git.html的Yaml文件头不正确，其他我看不出问题。</p>

<p>你可以点击项目主页左上角Admin按钮，看看pages部分怎么提示。</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 26, 2012  8:02 AM">2012年8月26日 08:02</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262086">#</a>
 | <a href="#comment-text" title="引用阮一峰的这条留言" onclick="return CommentQuote('comment-quote-262086','阮一峰');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262088" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://blog.zhaojie.me/" href="http://blog.zhaojie.me/" target="_blank" rel="nofollow">老赵</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262088">
            <p>项目页和个人页不同吧？项目页也可以加自定义域名吗？</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 26, 2012 12:05 PM">2012年8月26日 12:05</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262088">#</a>
 | <a href="#comment-text" title="引用老赵的这条留言" onclick="return CommentQuote('comment-quote-262088','老赵');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262089" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">木鸟</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262089">
            <p>sourceforg.net就是被国内大量建网站给封了大陆IP，希望博主不要发这样的教程了，好东西都是这样被大陆人给毁了的。</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 26, 2012 12:17 PM">2012年8月26日 12:17</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262089">#</a>
 | <a href="#comment-text" title="引用木鸟的这条留言" onclick="return CommentQuote('comment-quote-262089','木鸟');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262095" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://wiki.moegirl.org" href="http://wiki.moegirl.org" target="_blank" rel="nofollow">晒太阳的冰</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262095">
            <blockquote>
<pre>引用Probe的发言：</pre>

<p>github 是好东西，但藏着不让大伙知道就可以不被墙了？我不这么看，反倒是当每个网民都知道事实的时候，就离墙消失的一天不远了，那时候大家安心的去用 github 不是更好吗？</p>

</blockquote>

<p>你搞清楚是谁墙谁。蝗虫一般贪小便宜的大陆人涌入，光耗资源不贡献代码。任谁是运营商都会屏蔽所有大陆IP的。</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 26, 2012  2:14 PM">2012年8月26日 14:14</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262095">#</a>
 | <a href="#comment-text" title="引用晒太阳的冰的这条留言" onclick="return CommentQuote('comment-quote-262095','晒太阳的冰');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262096" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">东鱼</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262096">
            <p>实话说我也立刻想到sourceforge屏蔽中国地区IP的事情，原因就是这部分网民“占用了大量的免费资源却没有做出贡献“之类的。如果很多人也开始用同样思路利用github的免费空间的话，结果应该是可以预见的。</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 26, 2012  4:33 PM">2012年8月26日 16:33</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262096">#</a>
 | <a href="#comment-text" title="引用东鱼的这条留言" onclick="return CommentQuote('comment-quote-262096','东鱼');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262099" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">阮一峰</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262099">
            <blockquote>
<pre>引用老赵的发言：</pre>

<p>项目页和个人页不同吧？项目页也可以加自定义域名吗？</p>

</blockquote>

<p>项目页可以自定义域名的。</p>

<p>个人觉得，除非想要username.github.com这个域名，否则个人页用处不大。</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 26, 2012  5:41 PM">2012年8月26日 17:41</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262099">#</a>
 | <a href="#comment-text" title="引用阮一峰的这条留言" onclick="return CommentQuote('comment-quote-262099','阮一峰');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262101" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://blog.zhaojie.me/" href="http://blog.zhaojie.me/" target="_blank" rel="nofollow">老赵</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262101">
            <blockquote>
<pre>引用阮一峰的发言：</pre>

<p></p>

<p>项目页可以自定义域名的。</p>

<p>个人觉得，除非想要username.github.com这个域名，否则个人页用处不大。</p>

</blockquote>

<p>啊，这也可以？我去看看，我为了自定义域名还额外搞了个账号呢……</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 26, 2012  8:58 PM">2012年8月26日 20:58</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262101">#</a>
 | <a href="#comment-text" title="引用老赵的这条留言" onclick="return CommentQuote('comment-quote-262101','老赵');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262103" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://www.chiram.com" href="http://www.chiram.com" target="_blank" rel="nofollow">stanton</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262103">
            <p><a href="http://hzmook.github.com/2012/07/01/use-jekyll-build-blog-on-github.html" rel="nofollow">http://hzmook.github.com/2012/07/01/use-jekyll-build-blog-on-github.html</a></p>

<p>这篇讲得也不错</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 26, 2012 10:21 PM">2012年8月26日 22:21</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262103">#</a>
 | <a href="#comment-text" title="引用stanton的这条留言" onclick="return CommentQuote('comment-quote-262103','stanton');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262104" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://www.vipinit.com" href="http://www.vipinit.com" target="_blank" rel="nofollow">vipinchan</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262104">
            <p>国内SAE个人觉得挺好用的，对于开发者，可以申请下开发者认证就可以免费使用SAE空间了。。那可是全能免费空间哦，也能绑定独立域名。。</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 27, 2012  9:48 AM">2012年8月27日 09:48</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262104">#</a>
 | <a href="#comment-text" title="引用vipinchan的这条留言" onclick="return CommentQuote('comment-quote-262104','vipinchan');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262106" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">呆驴</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262106">
            <p>@自由国度，人家只是单纯的介绍，国人依然喜欢藏着掖着，一点分享精神都没有，从你的言论来看，你有什么资格说博主乱宣传了。</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 27, 2012 12:04 PM">2012年8月27日 12:04</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262106">#</a>
 | <a href="#comment-text" title="引用呆驴的这条留言" onclick="return CommentQuote('comment-quote-262106','呆驴');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262107" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">ipoly</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262107">
            <p>看起来正好可以用来托管前端切片代码～省得在本地搭建各种开发环境以实现文件的引用和包含～不错～</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 27, 2012 12:20 PM">2012年8月27日 12:20</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262107">#</a>
 | <a href="#comment-text" title="引用ipoly的这条留言" onclick="return CommentQuote('comment-quote-262107','ipoly');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262108" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">恶魔吹着笛子来</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262108">
            <blockquote>
<pre>引用自由国度的发言：</pre>

<p>github确实能让你打起免费的博客，但是请别盯着 免费 两个字去宣传它，这样做的结果是到最后大家谁也不用了，github本身并没有博客功能，github pages的初衷只是方便开发者为自己的项目做一个介绍的页面，展示文档之类的功能，你非要把他当成免费的博客去用，现在也没人限制你，我只是说大家要有点儿自觉性，一点儿公德心。不要像蝗虫一样，有免费生怕自己用不上，抢不到，相信关注这个博客的人也不至于连100块一年的空间都买不起</p>

<p>我不希望以后连github都要翻墙才能用，相信你也不愿意，你说是吧</p>

</blockquote>

<p>同意，我觉得大家应该看一下这偏博文http://www.williamlong.info/archives/3182.html</p>

<p>希望不要为了免费去在github上建博客，免得最后像sourceforge一样，最终害的是自己，</p>

<p>一直很喜欢阮先生的文章，但是这篇博客我也觉得确实不应该宣传</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 27, 2012  1:18 PM">2012年8月27日 13:18</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262108">#</a>
 | <a href="#comment-text" title="引用恶魔吹着笛子来的这条留言" onclick="return CommentQuote('comment-quote-262108','恶魔吹着笛子来');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262109" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://about:blank" href="http://about:blank" target="_blank" rel="nofollow">CK</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262109">
            <blockquote>

<p>　$ git push origin gh-pages</p>

</blockquote>

<p>执行这最后一步时，提示：</p>

<blockquote>

<p>fatal: <a href="https://github.com/%username%/jekyll_demo.git/info/refs" rel="nofollow">https://github.com/%username%/jekyll_demo.git/info/refs</a> not found: did you run git update-server-info on the server?</p>

</blockquote>

        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 27, 2012  2:12 PM">2012年8月27日 14:12</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262109">#</a>
 | <a href="#comment-text" title="引用CK的这条留言" onclick="return CommentQuote('comment-quote-262109','CK');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262111" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">CC</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262111">
            <p>看了觉得编程无能，还是不去凑热闹好了~~囧orz..</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 27, 2012  3:00 PM">2012年8月27日 15:00</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262111">#</a>
 | <a href="#comment-text" title="引用CC的这条留言" onclick="return CommentQuote('comment-quote-262111','CC');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262113" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://www.xuanmingyi.com" href="http://www.xuanmingyi.com" target="_blank" rel="nofollow">你怎么这样</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262113">
            <blockquote>
<pre>引用自由国度的发言：</pre>

<p>说中国人是蝗虫还真是不错，github被屏蔽了你就开心了？就像蝗虫，有好东西一拥而上，生怕自己抢不到，吃光了或不抢不过了就换下一个地方，继续搞。</p>

<p>这种东西需要写篇文章来宣传么，不知道宣传了以后的后果么，本来是个挺好的社区博客，有可能会因为你这一篇文章，搞的大家以后都用不了了，麻烦作者以后发文章前先考虑对社会的影响，对社区的影响，顾全大局...</p>

</blockquote>

<p>不知道什么意思，完全不明白为什么就说github会被屏蔽，就好像我受害了你还在说 谁让你长着一张被害的脸呢……</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 27, 2012  3:34 PM">2012年8月27日 15:34</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262113">#</a>
 | <a href="#comment-text" title="引用你怎么这样的这条留言" onclick="return CommentQuote('comment-quote-262113','你怎么这样');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262114" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://sokoban.ws" href="http://sokoban.ws" target="_blank" rel="nofollow">sokoban</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262114">
            <p>sourceforge.net 屏蔽了吗？能连上啊。</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 27, 2012  3:53 PM">2012年8月27日 15:53</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262114">#</a>
 | <a href="#comment-text" title="引用sokoban的这条留言" onclick="return CommentQuote('comment-quote-262114','sokoban');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262118" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">阮一峰</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262118">
            <p>@CK：</p>

<p>你要先在github.com上建立jekyll_demo的库，然后才在本地执行git push命令。</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 27, 2012  4:44 PM">2012年8月27日 16:44</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262118">#</a>
 | <a href="#comment-text" title="引用阮一峰的这条留言" onclick="return CommentQuote('comment-quote-262118','阮一峰');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262119" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://t.qq.com/michalliu" href="http://t.qq.com/michalliu" target="_blank" rel="nofollow">自由国度</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262119">
            <blockquote>
<pre>引用你怎么这样的发言：</pre>

<p></p>

<p>不知道什么意思，完全不明白为什么就说github会被屏蔽，就好像我受害了你还在说 谁让你长着一张被害的脸呢……</p>

</blockquote>

<p>按照国内的法律，博客建站是需要备案的，至于我为什么说github会被屏蔽，参考blogspot，我求某些人不要来祸害github了，这是一块净土...<br />
</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 27, 2012  4:52 PM">2012年8月27日 16:52</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262119">#</a>
 | <a href="#comment-text" title="引用自由国度的这条留言" onclick="return CommentQuote('comment-quote-262119','自由国度');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262120" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">hourglass</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262120">
            <p>我国的政策已造成巨大数量的国际网络难民，他们应当具有在别国避难的权利...而那些声称守卫着自家“净土”的原住民也持有自然的道义，但这个道义真的大于接受难民的道义吗？</p>

<p>这是个见仁见智的问题。</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 27, 2012  5:16 PM">2012年8月27日 17:16</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262120">#</a>
 | <a href="#comment-text" title="引用hourglass的这条留言" onclick="return CommentQuote('comment-quote-262120','hourglass');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262123" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">dirtyac</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262123">
            <p>看了后第一感觉是github也许很快会被墙了，不管是谁的错</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 27, 2012  6:27 PM">2012年8月27日 18:27</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262123">#</a>
 | <a href="#comment-text" title="引用dirtyac的这条留言" onclick="return CommentQuote('comment-quote-262123','dirtyac');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262125" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">小p</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262125">
            <p>sourceforge就是因为这样被国外封了中国的ip的。哎、、、</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 27, 2012  6:57 PM">2012年8月27日 18:57</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262125">#</a>
 | <a href="#comment-text" title="引用小p的这条留言" onclick="return CommentQuote('comment-quote-262125','小p');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262129" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://sokoban.ws" href="http://sokoban.ws" target="_blank" rel="nofollow">sokoban</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262129">
            <blockquote>
<pre>引用自由国度的发言：</pre>

<p></p>

<p>按照国内的法律，博客建站是需要备案的，至于我为什么说github会被屏蔽，参考blogspot，我求某些人不要来祸害github了，这是一块净土...</p>

<p><br />
</p></blockquote>

<p>这跟我国法律没有任何关系。在外国服务器建网站不受中国法律约束。阮兄的博客不也没备案么，也没见被屏蔽。</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 27, 2012  7:26 PM">2012年8月27日 19:26</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262129">#</a>
 | <a href="#comment-text" title="引用sokoban的这条留言" onclick="return CommentQuote('comment-quote-262129','sokoban');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262130" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">sai</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262130">
            <blockquote>
<pre>引用sokoban的发言：</pre>

<p></p>

<p>这跟我国法律没有任何关系。在外国服务器建网站不受中国法律约束。阮兄的博客不也没备案么，也没见被屏蔽。</p>

</blockquote>

<p>千里之行，始于hello world...</p>

<p>p.s.为何在google reader中订阅阮先生的博客，总是会触发在google搜敏感词一般的错误？</p>

<p>p.s.</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 27, 2012  8:26 PM">2012年8月27日 20:26</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262130">#</a>
 | <a href="#comment-text" title="引用sai的这条留言" onclick="return CommentQuote('comment-quote-262130','sai');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262134" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://github.com" href="http://github.com" target="_blank" rel="nofollow">github</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262134">
            <blockquote>
<pre>引用自由国度的发言：</pre>

<p>github确实能让你打起免费的博客，但是请别盯着 免费 两个字去宣传它，这样做的结果是到最后大家谁也不用了</p>

</blockquote>

<p><br />
强烈支持！占茅坑不拉屎者都滚！！！lz前两天下载jboss才发现sourceforge不能访问了，都是因为</p>

<p>这群损人利己的屎货！</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 27, 2012  9:04 PM">2012年8月27日 21:04</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262134">#</a>
 | <a href="#comment-text" title="引用github的这条留言" onclick="return CommentQuote('comment-quote-262134','github');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262139" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">阮一峰</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262139">
            <blockquote>
<pre>引用sai的发言：</pre>

<p>为何在google reader中订阅阮先生的博客，总是会触发在google搜敏感词一般的错误？</p>

</blockquote>

<p>我的Feed托管在Feedburner上面，而Feedburner被屏蔽了，所以……</p>

<p>你可以改成订阅备用Feed：http://www.ruanyifeng.com/blog/atom.xml<br />
</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 28, 2012 12:33 AM">2012年8月28日 00:33</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262139">#</a>
 | <a href="#comment-text" title="引用阮一峰的这条留言" onclick="return CommentQuote('comment-quote-262139','阮一峰');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262143" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">j.w</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262143">
            <blockquote>
<pre>引用github的发言：</pre>

<p></p>

<p><br />
强烈支持！占茅坑不拉屎者都滚！！！lz前两天下载jboss才发现sourceforge不能访问了，都是因为</p>

<p>这群损人利己的屎货！</p>

</blockquote>

<p>问题好像并不是因为他们使用了这些免费资源，按你的论断，twitter,facebook还有很多google的免费服务被封，都是因为国人喜欢免费的服务，占用服务者太多资源？<br />
</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 28, 2012  9:59 AM">2012年8月28日 09:59</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262143">#</a>
 | <a href="#comment-text" title="引用j.w的这条留言" onclick="return CommentQuote('comment-quote-262143','j.w');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262144" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://ziji.cc" href="http://ziji.cc" target="_blank" rel="nofollow">小年</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262144">
            <p>这个。。第三阶段过段牛气了！！</p>

<p>这个方法只适合做小站了~~如果是和我一样的个人博客，倒还是蛮合适的。呵呵！</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 28, 2012 10:17 AM">2012年8月28日 10:17</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262144">#</a>
 | <a href="#comment-text" title="引用小年的这条留言" onclick="return CommentQuote('comment-quote-262144','小年');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262145" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">hourglass</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262145">
            <p>技术，本来就是用来满足人的愿望，而不是用来压抑。</p>

<p>如果说满足人的愿望是邪恶的，那么技术本身即是邪恶的。从事技术的人，一方面践行这种邪恶，一方面又想要维护技术带来的表面上的“纯洁性”，妄图带来一种道德乃至沿用原初社会中的道德规律，是怎么也说不过去的。</p>

<p>这就是和现实的难民问题的差别。土地是先于人存在的，因此土耳其可以说已经接纳不下叙利亚的难民了，风俗是历史的也是久远的，因此土耳其可以说这些难民破坏了本地居民的生活。网络就大不一样，它是人创造的，本身的目的即是提供现实中没有的空间，承载量问题也会有相应的规律，但决不是现实中的规律只要这种创造一直延续下去（一些邪恶的组织想要使网络屈服现实规律不过是另外的话题）。另一点就是网络的“习俗”只有短短的20年时间，本身就不该作为定则甚至是值得挑战的成分。</p>

<p>总之，我的观点是网络的一切还处于创造之中，在任何方面都不应紧盯于日趋僵死的现实（或者被它扼杀，或最终拯救它，就看接下来了）。因此，需要鼓励的依然是探险家而不是道德说教者，是创造规则（哪怕是恐怖的规则，不过我相信持续的创造会带来好的结果）的人而不是照本宣科的人，是极大的混乱而不是极大的秩序。</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 28, 2012 10:20 AM">2012年8月28日 10:20</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262145">#</a>
 | <a href="#comment-text" title="引用hourglass的这条留言" onclick="return CommentQuote('comment-quote-262145','hourglass');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262147" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">hourglass</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262147">
            <p>不过这就带来了一个困境，也是一部分坚持之所在，那就是在技术（愿望的延伸）的无限发展下怎样寻找和留下美（心灵的延伸）。</p>

<p>在博物馆里可以看到饰有美丽花纹的刀剑，这种工艺的发展随着冷兵器时代的终止而消亡了。武器是技术，它不会为美而等待停滞。更为残酷的例子是大量拆除的北京老街和四合院，一种最初的建筑技术和美的产物被新的技术所取代了。人们找到了技术发展的指数形式，但美拒绝服从这种（简单又粗暴）的生产形式。于是，我们常说的“城市越来越丑陋”就产生了。</p>

<p>在一个风暴吹袭的下午，或许你会发现一朵天空中美丽的云。它是诞生在这场风暴之中，最终也将为它所毁灭。这短暂的美丽时刻我们或许在网络上也感受过，我们为之痛苦，但这是全人类的困境。</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 28, 2012 10:43 AM">2012年8月28日 10:43</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262147">#</a>
 | <a href="#comment-text" title="引用hourglass的这条留言" onclick="return CommentQuote('comment-quote-262147','hourglass');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262150" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">nikolai</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262150">
            <blockquote>
<pre>引用CK的发言：</pre>

<p>fatal: <a href="https://github.com/%username%/jekyll_demo.git/info/refs" rel="nofollow">https://github.com/%username%/jekyll_demo.git/info/refs</a> not found: did you run git update-server-info on the server?</p>

</blockquote>

<p>我也是出现这个错误，请问如何解决。</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 28, 2012 11:32 AM">2012年8月28日 11:32</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262150">#</a>
 | <a href="#comment-text" title="引用nikolai的这条留言" onclick="return CommentQuote('comment-quote-262150','nikolai');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262153" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">nikolai</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262153">
            <blockquote>
<pre>引用nikolai的发言：</pre>

<p></p>

<p>我也是出现这个错误，请问如何解决。</p>

</blockquote>

<p>忘了看到博主在上面已解答，问题已解决。打扰抱歉。:P<br />
</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 28, 2012 12:41 PM">2012年8月28日 12:41</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262153">#</a>
 | <a href="#comment-text" title="引用nikolai的这条留言" onclick="return CommentQuote('comment-quote-262153','nikolai');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262172" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">FreeSpirit</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262172">
            <blockquote>
<pre>引用Probe的发言：</pre>

<p>github 是好东西，但藏着不让大伙知道就可以不被墙了？我不这么看，反倒是当每个网民都知道事实的时候，就离墙消失的一天不远了，那时候大家安心的去用 github 不是更好吗？</p>

</blockquote>

<p>说的很对。<br />
</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 28, 2012  4:54 PM">2012年8月28日 16:54</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262172">#</a>
 | <a href="#comment-text" title="引用FreeSpirit的这条留言" onclick="return CommentQuote('comment-quote-262172','FreeSpirit');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262174" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://正在建立" href="http://正在建立" target="_blank" rel="nofollow">闵曙辉</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262174">
            <blockquote>
<pre>引用阮一峰的发言：</pre>

<p>建议仔细研究Jekyll的示例库：https://github.com/mojombo/tpw</p>

</blockquote>

<p>想问一下这个实例是否提交了的，我访问http://mojombo.github.com/tpw</p>

<p>也是404错，页面未提交还是github的BLOG已经被墙了？有哪些比较知名的GITHUB网站推荐么？</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 28, 2012  4:58 PM">2012年8月28日 16:58</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262174">#</a>
 | <a href="#comment-text" title="引用闵曙辉的这条留言" onclick="return CommentQuote('comment-quote-262174','闵曙辉');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262192" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">Leo</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262192">
            <p>你好，我试着建了两个，为什么都是404的错误呢？<br />
<a href="http://shuiyue.github.com/jekyll_demo/" rel="nofollow">http://shuiyue.github.com/jekyll_demo/</a><br />
<a href="https://github.com/shuiyue/jekyll_demo.git" rel="nofollow">https://github.com/shuiyue/jekyll_demo.git</a></p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 28, 2012  7:25 PM">2012年8月28日 19:25</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262192">#</a>
 | <a href="#comment-text" title="引用Leo的这条留言" onclick="return CommentQuote('comment-quote-262192','Leo');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262201" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://www.douban.com/people/chenist/" href="http://www.douban.com/people/chenist/" target="_blank" rel="nofollow">阿肯</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262201">
            <p>和点点网比起来,优点在哪?</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 28, 2012  8:37 PM">2012年8月28日 20:37</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262201">#</a>
 | <a href="#comment-text" title="引用阿肯的这条留言" onclick="return CommentQuote('comment-quote-262201','阿肯');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262202" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">Homeway</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262202">
            <p>如何更新已经也写好的blog呢?<br />
可定不能再用下面的方法了吧?<br />
$ git add .<br />
$ git commit -m "first post"<br />
$ git remote add origin <a href="https://github.com/username/jekyll_demo.git" rel="nofollow">https://github.com/username/jekyll_demo.git</a><br />
$ git push origin gh-pages</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 28, 2012  8:37 PM">2012年8月28日 20:37</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262202">#</a>
 | <a href="#comment-text" title="引用Homeway的这条留言" onclick="return CommentQuote('comment-quote-262202','Homeway');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262208" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">唉唉唉</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262208">
            <p>真没必要，找个稳定的空间，买个域名，少喝一次酒这钱就出来了。wordpress不比这些玩法好多了吗。还嫌贵用点点也可以啊，点点可以绑域名的。</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 28, 2012  9:06 PM">2012年8月28日 21:06</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262208">#</a>
 | <a href="#comment-text" title="引用唉唉唉的这条留言" onclick="return CommentQuote('comment-quote-262208','唉唉唉');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262210" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">唉唉唉</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262210">
            <blockquote>
<pre>引用j.w的发言：</pre>

<p></p>

<p>问题好像并不是因为他们使用了这些免费资源，按你的论断，twitter,facebook还有很多google的免费服务被封，都是因为国人喜欢免费的服务，占用服务者太多资源？</p>

<p><br />
</p></blockquote>

<p>你没弄清楚情况，一个是gfw封你出口，一个是别人网站封你ip，这是两回事</p>

<p>github本意不是让你搭免费博客的地方。</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 28, 2012  9:10 PM">2012年8月28日 21:10</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262210">#</a>
 | <a href="#comment-text" title="引用唉唉唉的这条留言" onclick="return CommentQuote('comment-quote-262210','唉唉唉');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262219" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">阮一峰</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262219">
            <blockquote>
<pre>引用Leo的发言：</pre>

<p>你好，我试着建了两个，为什么都是404的错误呢？</p>

</blockquote>

<p>页面必须放在gh-pages分支中</p>

<blockquote>
<pre>引用闵曙辉的发言：</pre>

<p>我访问http://mojombo.github.com/tpw</p>

<p>也是404错，页面未提交还是github的BLOG已经被墙了？</p>

</blockquote>

<p>他自定义域名了，你可以访问http://tom.preston-werner.com/</p>

<p><br />
</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 28, 2012 10:31 PM">2012年8月28日 22:31</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262219">#</a>
 | <a href="#comment-text" title="引用阮一峰的这条留言" onclick="return CommentQuote('comment-quote-262219','阮一峰');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262226" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">小周</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262226">
            <p>您好，现在买域名和空间，在国内您有什么注册商推荐么？万网好吗？</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 29, 2012  9:43 AM">2012年8月29日 09:43</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262226">#</a>
 | <a href="#comment-text" title="引用小周的这条留言" onclick="return CommentQuote('comment-quote-262226','小周');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262239" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://hellokuku.com" href="http://hellokuku.com" target="_blank" rel="nofollow">jianwei</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262239">
            <p>ruanyifeng,您好，我是一名大二学生，是从暑假快结束的时候，才无意间关注到您的blog的，一下子就喜欢上了这个地方。于是用ipad离线1K+您的博文，打算用空闲的时间仔细看，自己也打算好好写blog。同时也感受到了资讯和经验的可贵，目前用greader订阅了几个blog，但是还是觉得挺空的。能否推荐几个呢？（我喜欢IT、实事、经济、文化、电影。我的专业是计算机科学与技术） 或者您要是愿意分享，能否把订阅类表导出，发送给我，然后由我自己筛选。谢谢啦～</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 29, 2012  4:52 PM">2012年8月29日 16:52</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262239">#</a>
 | <a href="#comment-text" title="引用jianwei的这条留言" onclick="return CommentQuote('comment-quote-262239','jianwei');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262248" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">张奇</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262248">
            <p>你好，请问博主电脑的操作系统是什么？</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 29, 2012  7:25 PM">2012年8月29日 19:25</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262248">#</a>
 | <a href="#comment-text" title="引用张奇的这条留言" onclick="return CommentQuote('comment-quote-262248','张奇');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262315" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://www.qianxingzhem.com" href="http://www.qianxingzhem.com" target="_blank" rel="nofollow">潜行者m</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262315">
            <blockquote>
<pre>引用weedge的发言：</pre>

<p>感谢博主分享，尝试着搭建一个。@自由国度的话很反感，好东西当然需要分享；不知道他说的话所表达的是啥意思。</p>

</blockquote>

<p>如果有某个国外的免费产品被推荐给中国人,很多素质比较低的国人,会拿那些来做垃圾网站或者其他的使用.就像有些国外免费主机,就有屏蔽中国的.因为那些素质比较低的,会一拥而上,然后做垃圾站,发垃圾内容.<br />
他们这样,只有垃圾,没有利益,当然屏蔽了.<br />
就是这个意思.我说的是部分素质比较低的国人.</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 30, 2012 12:43 PM">2012年8月30日 12:43</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262315">#</a>
 | <a href="#comment-text" title="引用潜行者m的这条留言" onclick="return CommentQuote('comment-quote-262315','潜行者m');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262322" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">小豆</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262322">
            <p>看了很久阮老师的博客，大约是由于《黑客与画家》这本书，要找下蛋的母鸡才发现阮老师的。<br />
真心谢谢您的分享。</p>

<p>互联网因为您这样的独立博客的存在才变得有价值！</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 30, 2012  2:38 PM">2012年8月30日 14:38</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262322">#</a>
 | <a href="#comment-text" title="引用小豆的这条留言" onclick="return CommentQuote('comment-quote-262322','小豆');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262329" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">chris</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262329">
            <p>下面是我的首页，<br />
<a href="http://asiachrispy.github.com/achris/" rel="nofollow">http://asiachrispy.github.com/achris/</a></p>

<p>点击这个页面中的文章链接到<br />
<a href="http://asiachrispy.github.com/2012/08/25/hello-world.html" rel="nofollow">http://asiachrispy.github.com/2012/08/25/hello-world.html</a></p>

<p>大家发现什么没有，少了我的项目名 achris,加上项目名访问就正常了<br />
<a href="http://asiachrispy.github.com/achris/2012/08/25/hello-world.html" rel="nofollow">http://asiachrispy.github.com/achris/2012/08/25/hello-world.html</a></p>

<p><br />
</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 30, 2012  5:43 PM">2012年8月30日 17:43</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262329">#</a>
 | <a href="#comment-text" title="引用chris的这条留言" onclick="return CommentQuote('comment-quote-262329','chris');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262365" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://tumutanzi.com" href="http://tumutanzi.com" target="_blank" rel="nofollow">土木坛子</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262365">
            <p>我很早以前就听说并见到有资深博客主，比如谢益辉同学，转向GIT创建博客，但我试过以后，还是坚持使用WP, 不易上手，也不够自由。</p>

<p>对于国内用户，访问速度未必会快，而且，用的人多了以后可能面临被GFW的问题。倒是独立主机创建的话还有较大的空间来变化，所以，至少对于中国的大部分独立博客主，GIT恐怕难以适用。</p>

<p>事实上，对于国外用户有很多选择来不考虑主机空间和流量的问题，比如wordpress.com, blogger.com, tumblr.com等博客，都可以挂上自己的域名，相当于自己的独立博客了。可惜，这一切都是墙外的服务。</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 31, 2012  4:39 AM">2012年8月31日 04:39</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262365">#</a>
 | <a href="#comment-text" title="引用土木坛子的这条留言" onclick="return CommentQuote('comment-quote-262365','土木坛子');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262373" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">jazzi</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262373">
            <p>@阮先生<br />
如何只显示一篇博文的前一百个字呢？</p>

<p>I read Liquid document and just found how to show limited posts ({% for post in site.posts limit:1 %}) {% endfor %}</p>

<p>Thanks</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 31, 2012  9:20 AM">2012年8月31日 09:20</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262373">#</a>
 | <a href="#comment-text" title="引用jazzi的这条留言" onclick="return CommentQuote('comment-quote-262373','jazzi');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262376" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://zx1986.github.com" href="http://zx1986.github.com" target="_blank" rel="nofollow">張旭</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262376">
            <p>Octopress 跟 ruhoh.com 也都很好用喲，原理是一樣的 :-)</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 31, 2012 10:13 AM">2012年8月31日 10:13</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262376">#</a>
 | <a href="#comment-text" title="引用張旭的这条留言" onclick="return CommentQuote('comment-quote-262376','張旭');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262378" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://maxellar.diandian.com/" href="http://maxellar.diandian.com/" target="_blank" rel="nofollow">杜顺帆</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262378">
            <p>请问我使用了atom.xml来处理RSS，但仍然无法使用，我看了很多中文jekyll网站貌似都没有RSS，难道atom.xml不支持中文？</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 31, 2012 10:43 AM">2012年8月31日 10:43</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262378">#</a>
 | <a href="#comment-text" title="引用杜顺帆的这条留言" onclick="return CommentQuote('comment-quote-262378','杜顺帆');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262382" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">tttyu</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262382">
            <p>我认为博主分享是对的,不过看到这篇章心中就有一份预期,github很快就会屏蔽大陆....<br />
很多做法都是对的,不过是不是真的要去做?是不是真的不需要理会旁人看法,旁人对这件事的处理方式,还有不久将来这位"旁人"会为其它人带来啥负面问题,我认应博主应三思而后行,否则简直就是祸害github</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 31, 2012 12:17 PM">2012年8月31日 12:17</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262382">#</a>
 | <a href="#comment-text" title="引用tttyu的这条留言" onclick="return CommentQuote('comment-quote-262382','tttyu');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262431" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">M</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262431">
            <p>不是有很多用wordpress的 免费托管站吗</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 31, 2012  7:22 PM">2012年8月31日 19:22</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262431">#</a>
 | <a href="#comment-text" title="引用M的这条留言" onclick="return CommentQuote('comment-quote-262431','M');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262440" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://twokg.com" href="http://twokg.com" target="_blank" rel="nofollow">两公斤</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262440">
            <p>说真的，在中国的话，免费、可绑定域名、最简单的博客托管应该是点点吧？我的一个博客就是放在点点上的。稳定性还可以</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 31, 2012 10:11 PM">2012年8月31日 22:11</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262440">#</a>
 | <a href="#comment-text" title="引用两公斤的这条留言" onclick="return CommentQuote('comment-quote-262440','两公斤');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262455" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">momo5269</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262455">
            <p>个人感觉说会封的真心D疼......网上那么多比github良好的免费空间呢 比如上面说到的openshift 管理也挺简单...</p>

<p>而且Jekyll有效杜绝低端用户的涌入..</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="September  1, 2012  3:59 AM">2012年9月 1日 03:59</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262455">#</a>
 | <a href="#comment-text" title="引用momo5269的这条留言" onclick="return CommentQuote('comment-quote-262455','momo5269');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262461" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">wang</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262461">
            <p>发现了，网页的主机域名是 <a href="http://用户名.github.com/repo名，这是" rel="nofollow">http://用户名.github.com/repo名，这是</a> github 的硬性规定。网页中生成链接时用的就是 baseurl，为了能正确访问，所以 baseurl 必须和 repo名 一致。</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="September  1, 2012  6:49 AM">2012年9月 1日 06:49</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262461">#</a>
 | <a href="#comment-text" title="引用wang的这条留言" onclick="return CommentQuote('comment-quote-262461','wang');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262505" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://netwjx.github.com" href="http://netwjx.github.com" target="_blank" rel="nofollow">netwjx</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262505">
            <p>第三种应该叫 自动化工具生成静态网站的Blog, 我在用Octopress, 基于Jekyll</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="September  2, 2012  4:19 PM">2012年9月 2日 16:19</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262505">#</a>
 | <a href="#comment-text" title="引用netwjx的这条留言" onclick="return CommentQuote('comment-quote-262505','netwjx');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262565" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://verynix.com" href="http://verynix.com" target="_blank" rel="nofollow">自由的角马</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262565">
            <p>挺担心github和openshift这两个号东西被河蟹了。</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="September  3, 2012  1:16 PM">2012年9月 3日 13:16</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262565">#</a>
 | <a href="#comment-text" title="引用自由的角马的这条留言" onclick="return CommentQuote('comment-quote-262565','自由的角马');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262599" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://www.yadli.net" href="http://www.yadli.net" target="_blank" rel="nofollow">v-yadli</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262599">
            <blockquote>
<pre>引用潜行者m的发言：</pre>

<p></p>

<p>如果有某个国外的免费产品被推荐给中国人,很多素质比较低的国人,会拿那些来做垃圾网站或者其他的使用.就像有些国外免费主机,就有屏蔽中国的.因为那些素质比较低的,会一拥而上,然后做垃圾站,发垃圾内容.<br />
他们这样,只有垃圾,没有利益,当然屏蔽了.<br />
就是这个意思.我说的是部分素质比较低的国人.</p>

</blockquote>

<p>别的不说，<br />
“某些素质低下的人”可以“一拥而上地使用git以及手动的模板生成器”？<br />
我不这么认为……他们想要的大概是可以运行一些CGI然后点点网页直接就能用的那种吧。</p>

<p>我认为这篇文章点到为止，是为有念力追求新知识的人准备的。<br />
在这样的人群中推广github建站，会给github带来很多有冒险精神的新人。<br />
（另外vimwiki+dropbox+github也是很和谐的方法）</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="September  3, 2012  8:48 PM">2012年9月 3日 20:48</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262599">#</a>
 | <a href="#comment-text" title="引用v-yadli的这条留言" onclick="return CommentQuote('comment-quote-262599','v-yadli');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262637" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">liang456</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262637">
            <p><a href="http://liang456.github.com/gitpage/" rel="nofollow">http://liang456.github.com/gitpage/</a><br />
各位大神，我通过gh-pages分支上传了，上传以后出来一些乱码，能帮我看看是什么问题么？<br />
</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="September  4, 2012  2:35 AM">2012年9月 4日 02:35</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262637">#</a>
 | <a href="#comment-text" title="引用liang456的这条留言" onclick="return CommentQuote('comment-quote-262637','liang456');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262648" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">阮一峰</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262648">
            <p>@liang456：</p>

<p>將每一行行首的空格去除。</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="September  4, 2012  8:15 AM">2012年9月 4日 08:15</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262648">#</a>
 | <a href="#comment-text" title="引用阮一峰的这条留言" onclick="return CommentQuote('comment-quote-262648','阮一峰');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262685" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">Jerry Lee</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262685">
            <p>正想要倒腾的东西。Mark比Wordpress来写好多了。</p>

<p>PS：<br />
如何让文章可以被评论？</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="September  4, 2012  5:37 PM">2012年9月 4日 17:37</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262685">#</a>
 | <a href="#comment-text" title="引用Jerry Lee的这条留言" onclick="return CommentQuote('comment-quote-262685','Jerry Lee');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262774" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://yahaizi.com" href="http://yahaizi.com" target="_blank" rel="nofollow">z</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262774">
            <p>这种分享文章很好呀。还有那个分享Linus自传的。</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="September  5, 2012  9:52 AM">2012年9月 5日 09:52</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262774">#</a>
 | <a href="#comment-text" title="引用z的这条留言" onclick="return CommentQuote('comment-quote-262774','z');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262840" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://maxellar.diandian.com/" href="http://maxellar.diandian.com/" target="_blank" rel="nofollow">杜顺帆</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262840">
            <p>发现配合http://prose.io/ 写文章很方便</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="September  5, 2012 10:23 PM">2012年9月 5日 22:23</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262840">#</a>
 | <a href="#comment-text" title="引用杜顺帆的这条留言" onclick="return CommentQuote('comment-quote-262840','杜顺帆');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-262971" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://yahaizi.com" href="http://yahaizi.com" target="_blank" rel="nofollow">z</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-262971">
            <blockquote>
<pre>引用自由的角马的发言：</pre>

<p>挺担心github和openshift这两个号东西被河蟹了。</p>

</blockquote>

<p>不要担心啦。和谐的目的就是要让你担心，你一担心，就小心谨慎，鼠目寸光，正中河蟹下怀。<br />
该干嘛干嘛。和谐了再找别的。<br />
blogger和wordpress都和谐啦。怎样？有了github和openshift。还有很多其他的。<br />
如果就发表点文章什么的，你只要有个域名，空间随便找，花钱买个也很便宜，比电话月租便宜多了。如果你搞编程的，翻墙应该是所有搞技术必备的工具吧。</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="September  7, 2012 12:48 PM">2012年9月 7日 12:48</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-262971">#</a>
 | <a href="#comment-text" title="引用z的这条留言" onclick="return CommentQuote('comment-quote-262971','z');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-263005" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">vampire</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-263005">
            <p>请教一下，绑定域名是怎么操作的，没看明白，多谢。</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="September  8, 2012  6:54 PM">2012年9月 8日 18:54</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-263005">#</a>
 | <a href="#comment-text" title="引用vampire的这条留言" onclick="return CommentQuote('comment-quote-263005','vampire');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-263112" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://pmper.me" href="http://pmper.me" target="_blank" rel="nofollow">BreeStealth</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-263112">
            <p>如果为了图省事，我还是建议octopress，很多手动的东西，它都可以帮你自动化处理了。</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="September 10, 2012  2:06 PM">2012年9月10日 14:06</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-263112">#</a>
 | <a href="#comment-text" title="引用BreeStealth的这条留言" onclick="return CommentQuote('comment-quote-263112','BreeStealth');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-263115" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://pmper.me" href="http://pmper.me" target="_blank" rel="nofollow">BreeStealth</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-263115">
            <blockquote>
<pre>引用两公斤的发言：</pre>

<p>说真的，在中国的话，免费、可绑定域名、最简单的博客托管应该是点点吧？我的一个博客就是放在点点上的。稳定性还可以</p>

</blockquote>

<p>国内这些东西，能不用就尽量别用了吧。</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="September 10, 2012  2:07 PM">2012年9月10日 14:07</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-263115">#</a>
 | <a href="#comment-text" title="引用BreeStealth的这条留言" onclick="return CommentQuote('comment-quote-263115','BreeStealth');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-263148" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://chchwy.github.com" href="http://chchwy.github.com" target="_blank" rel="nofollow">chchwy</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-263148">
            <p>剛剛照著博主的步驟折騰了一下，發覺jekyll可以直接放在master下，不一定要放在gh-pages分支裡。</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="September 11, 2012  2:41 PM">2012年9月11日 14:41</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-263148">#</a>
 | <a href="#comment-text" title="引用chchwy的这条留言" onclick="return CommentQuote('comment-quote-263148','chchwy');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-263252" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://no-propergation.net" href="http://no-propergation.net" target="_blank" rel="nofollow">no-propergation</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-263252">
            <p>无语了。。。。<br />
某些人支持 利用github满足私欲的人，你们搞清楚逻辑好吧。</p>

<p>是github或者说国外的站 封掉 国内的IP，而不是你们屎脑壳里面的相反逻辑。</p>

<p>国内gfw封锁国外，是按照敏感性问题（至少是一个原则）来封锁目标站的（不论国内外），而不是这里说的 “占用资源不贡献”而导致（国内IP）被封锁。</p>

<p>都是搞it的，居然连这两个简单，但意义截然相反的逻辑都没看明白。<br />
即使是没看懂，你屎脑壳难道一点常识判断都没有？（而且好的东西到了国人这里都会被糟蹋掉，就像很多国外空间，不论付费还是免费的，一旦国人多了就导致同一个host上的其他网站，在国内都连不上他们了。一窝蜂占坑，又少见人为社区出力。）</p>

<p><br />
</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="September 13, 2012 10:57 AM">2012年9月13日 10:57</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-263252">#</a>
 | <a href="#comment-text" title="引用no-propergation的这条留言" onclick="return CommentQuote('comment-quote-263252','no-propergation');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-263488" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">ruibofeng</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-263488">
            <blockquote>
<pre>引用杜顺帆的发言：</pre>

<p></p>

<p>已经确认前面没空格，mac编辑的，可以帮忙看一下吗：https://github.com/Perrydu/maxellar</p>

</blockquote>

<p>碰到类似问题，把https换成http试试。</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="September 17, 2012 12:15 PM">2012年9月17日 12:15</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-263488">#</a>
 | <a href="#comment-text" title="引用ruibofeng的这条留言" onclick="return CommentQuote('comment-quote-263488','ruibofeng');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-263514" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://www.cloudaice.com" href="http://www.cloudaice.com" target="_blank" rel="nofollow">cloudaice</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-263514">
            <p>已经用了有一段时间了，自己也早就想写一篇文章来介绍了。</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="September 17, 2012  5:30 PM">2012年9月17日 17:30</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-263514">#</a>
 | <a href="#comment-text" title="引用cloudaice的这条留言" onclick="return CommentQuote('comment-quote-263514','cloudaice');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-263521" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://microcai.is-programmer.com/" href="http://microcai.is-programmer.com/" target="_blank" rel="nofollow">microcai</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-263521">
            <blockquote>
<pre>引用no-propergation的发言：</pre>

<p>是github或者说国外的站 封掉 国内的IP，而不是你们屎脑壳里面的相反逻辑。</p>

</blockquote>

<p>你觉得会使用 git 的有几个人？别太高估网民的技术水平。</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="September 17, 2012  6:56 PM">2012年9月17日 18:56</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-263521">#</a>
 | <a href="#comment-text" title="引用microcai的这条留言" onclick="return CommentQuote('comment-quote-263521','microcai');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-263649" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">zz</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-263649">
            <blockquote>
<pre>引用土木坛子的发言：</pre>

<p>我很早以前就听说并见到有资深博客主，比如谢益辉同学，转向GIT创建博客，但我试过以后，还是坚持使用WP, 不易上手，也不够自由。</p>

<p>对于国内用户，访问速度未必会快，而且，用的人多了以后可能面临被GFW的问题。倒是独立主机创建的话还有较大的空间来变化，所以，至少对于中国的大部分独立博客主，GIT恐怕难以适用。</p>

<p>事实上，对于国外用户有很多选择来不考虑主机空间和流量的问题，比如wordpress.com, blogger.com, tumblr.com等博客，都可以挂上自己的域名，相当于自己的独立博客了。可惜，这一切都是墙外的服务。</p>

</blockquote>
你这个回复太典型了，所以拿来挑个刺，不是针对你哦。

<p>开源的，没什么不够自由，只有技术不够。<br />
访问速度，下载 github 资源时，都有 200kb 以上，很难跟“慢”关联起来。<br />
你也说他不易上手，那么国内用户就不会太多，不太多就不容易墙。这个空间只有 300mb ，也做不了什么大的坏事。<br />
不过，我并不觉得他难用，不会用的人基本上不是太懒，就是英文太烂，前者居多。我们是用户，不是开发者，难不到哪里去，只要肯折腾。<br />
你提到“独立主机创建的话还有较大的空间来变化”，可是静态网站搬家才最轻松简便，对空间没要求的吧？免费稳定空间还会少吗？光免费的 git hosting 就有十几个，甚至还可以用 dropbox 。<br />
wordpress.com 这些，绑定域名不是免费的。有个没墙的东西叫 dreamapp 。不过，一旦 jekyll/octopress/ruhoh 上手，看到这些东西，也兴趣缺缺了。</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="September 20, 2012  5:39 PM">2012年9月20日 17:39</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-263649">#</a>
 | <a href="#comment-text" title="引用zz的这条留言" onclick="return CommentQuote('comment-quote-263649','zz');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-263669" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://mindon.github.com" href="http://mindon.github.com" target="_blank" rel="nofollow">麦盾</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-263669">
            <p>用的是 Jekyll 的一个实现：octopress，感觉还是很不错的。</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="September 21, 2012 10:01 AM">2012年9月21日 10:01</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-263669">#</a>
 | <a href="#comment-text" title="引用麦盾的这条留言" onclick="return CommentQuote('comment-quote-263669','麦盾');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-263731" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://dfd.com" href="http://dfd.com" target="_blank" rel="nofollow">大</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-263731">
            <blockquote>
<pre>引用潜行者m的发言：</pre>

<p></p>

<p>如果有某个国外的免费产品被推荐给中国人,很多素质比较低的国人,会拿那些来做垃圾网站或者其他的使用.就像有些国外免费主机,就有屏蔽中国的.因为那些素质比较低的,会一拥而上,然后做垃圾站,发垃圾内容.<br />
他们这样,只有垃圾,没有利益,当然屏蔽了.<br />
就是这个意思.我说的是部分素质比较低的国人.</p>

</blockquote>

<p>你是没看到国外的情况，那什么来着？好像叫垃圾工场，就是用机器产生无意义的一大堆文章，然后google收录了，而且Google认为他原创很高，搜索很多关键字都被转到这些垃圾的文章上去了。我想说的是这跟素质没啥关系，这是利益驱使，这是游戏规则，也是技术手段，你没看过发垃圾邮件的每天信息量有多少？</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="September 21, 2012 10:23 PM">2012年9月21日 22:23</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-263731">#</a>
 | <a href="#comment-text" title="引用大的这条留言" onclick="return CommentQuote('comment-quote-263731','大');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-263765" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">wj</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-263765">
            <p>请问出现这个问题是什么原因呢？</p>

<p>wj@wj:~/jekyll_demo$ git checkout --orphan gh-pages<br />
error: unknown option `orphan'<br />
</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="September 22, 2012 11:00 AM">2012年9月22日 11:00</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-263765">#</a>
 | <a href="#comment-text" title="引用wj的这条留言" onclick="return CommentQuote('comment-quote-263765','wj');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-263791" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://reverland.org" href="http://reverland.org" target="_blank" rel="nofollow">reverland</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-263791">
            <blockquote>
<pre>引用chchwy的发言：</pre>

<p>剛剛照著博主的步驟折騰了一下，發覺jekyll可以直接放在master下，不一定要放在gh-pages分支裡。</p>

</blockquote>

<p>是的，直接新建一个username.github.com的项目还更方便一些。</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="September 23, 2012 12:37 PM">2012年9月23日 12:37</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-263791">#</a>
 | <a href="#comment-text" title="引用reverland的这条留言" onclick="return CommentQuote('comment-quote-263791','reverland');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-264067" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">alexbian</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-264067">
            <p>作者应该看清楚gitihub说明，此文会误导大家，创建主页可以有2种，一种是个人或者组织类的，另一种才是这种“项目主页”<br />
详见<br />
<a href="https://help.github.com/articles/user-organization-and-project-pages" rel="nofollow">https://help.github.com/articles/user-organization-and-project-pages</a></p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="September 29, 2012  8:56 PM">2012年9月29日 20:56</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-264067">#</a>
 | <a href="#comment-text" title="引用alexbian的这条留言" onclick="return CommentQuote('comment-quote-264067','alexbian');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-266064" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">storm</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-266064">
            <p>好东西，马上试试。</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="November 16, 2012 10:16 PM">2012年11月16日 22:16</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-266064">#</a>
 | <a href="#comment-text" title="引用storm的这条留言" onclick="return CommentQuote('comment-quote-266064','storm');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-266221" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">DolphinBoy</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-266221">
            <p>我觉得只是说博主的过错就有点儿蛋疼了，我相信没有博主的文章也一样会有人在Github上建站，至于博主是否应该发布这篇文章，我认为，为什么不可以呢，至少博主的初衷是好的。当然如果大家担心的是因为一部分所谓的“低素质”的中国人在Github建垃圾网站而导致Github封掉中国的IP，那我觉得大家是闲操心了，难道Github没有想过这个问题吗，难道Github是脑子一热就决定这样做的吗？Github的初衷可能只是让大家方便的建立项目主页，但是他们和肯定会想的有一部分人有恶意行为，至于怎么对待这中恶意行为，我觉得如果Github采取像“所有安装360安全卫士的电脑将不能安装QQ软件”的做法的话，那Github也不值得去追捧，什么是以人为主，如果网站因为一部分人的恶意行为而去停止对大部分人的服务，那叫什么网站，那就干脆别做了呗。当然我们是建议大家尽量能够让Github做它应该做的事情，不过你总要考虑一些苦逼程序员的资金情况吧。</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="November 21, 2012  3:45 PM">2012年11月21日 15:45</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-266221">#</a>
 | <a href="#comment-text" title="引用DolphinBoy的这条留言" onclick="return CommentQuote('comment-quote-266221','DolphinBoy');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-266355" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">pengtao</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-266355">
            <p>博主您好:按照你的方法试了下,麻烦你看下这个是怎么回事吗?http://peng-tao.github.com/jekyll_demo/谢谢!</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="November 26, 2012  1:50 AM">2012年11月26日 01:50</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-266355">#</a>
 | <a href="#comment-text" title="引用pengtao的这条留言" onclick="return CommentQuote('comment-quote-266355','pengtao');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-266364" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">阮一峰</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-266364">
            <p>@pengtao，</p>

<p>每一行都要顶行写，不能直接拷贝我的代码，因为为了排版，我在行首加了两个空格。</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="November 26, 2012  8:15 AM">2012年11月26日 08:15</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-266364">#</a>
 | <a href="#comment-text" title="引用阮一峰的这条留言" onclick="return CommentQuote('comment-quote-266364','阮一峰');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-266375" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">CJ</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-266375">
            <p>人家Github pages官方网站上都推荐使用Jekyll了。不就搭个静态页面作为技术博客。你脑袋被洗过啦。Github也是免费hosting开源项目的。那我们蝗虫不用去用好啦</p>

<p>PS：请勿回复，哈哈，因为我懒得没劲再回复你。<br />
</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="November 26, 2012  7:28 PM">2012年11月26日 19:28</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-266375">#</a>
 | <a href="#comment-text" title="引用CJ的这条留言" onclick="return CommentQuote('comment-quote-266375','CJ');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-266587" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">chinaxing</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-266587">
            <blockquote>
<pre>引用阮一峰的发言：</pre>

<p></p>

<p>奇怪，我的git没报错……怀疑是不是你的版本没更新。</p>

<p>出现这个错误的原因可能是，必须先有master分支，然后才能创建其他分支。</p>

<p>你可以在git init之后，随便做一次git commit，然后再git checkout --orphan gh-pages，应该就不会报错了。</p>

</blockquote>

<p>按照你说的做，还是不行，请帮忙看看哦<br />
</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="December  2, 2012  9:33 PM">2012年12月 2日 21:33</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-266587">#</a>
 | <a href="#comment-text" title="引用chinaxing的这条留言" onclick="return CommentQuote('comment-quote-266587','chinaxing');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-266754" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">xing</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-266754">
            <blockquote>
<pre>引用自由国度的发言：</pre>

<p>说中国人是蝗虫还真是不错，github被屏蔽了你就开心了？就像蝗虫，有好东西一拥而上，生怕自己抢不到，吃光了或不抢不过了就换下一个地方，继续搞。</p>

<p>这种东西需要写篇文章来宣传么，不知道宣传了以后的后果么，本来是个挺好的社区博客，有可能会因为你这一篇文章，搞的大家以后都用不了了，麻烦作者以后发文章前先考虑对社会的影响，对社区的影响，顾全大局...</p>

</blockquote>

<p>真的很可笑。试问如果没有任何人推荐，没有任何新闻报道，你又凭什么知道github？如果互联网不能传播有用的信息，存在还有何价值？<br />
有用的优秀的东西共享有什么错？难道非要每个人都藏着掖着？<br />
如果某D要墙某些东西，不能成为我们沉默缄口的借口！！！<br />
你把中国人比作蝗虫，我只能说你连蝗虫都不如。如此自私而又怯懦的你，恐怕世界上没有哪个字眼可以真的配得上你。</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="December  7, 2012  7:14 PM">2012年12月 7日 19:14</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-266754">#</a>
 | <a href="#comment-text" title="引用xing的这条留言" onclick="return CommentQuote('comment-quote-266754','xing');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-266990" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">freeMe</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-266990">
            <blockquote>
<pre>引用xing的发言：</pre>

<p>真的很可笑。试问如果没有任何人推荐，没有任何新闻报道，你又凭什么知道github？如果互联网不能传播有用的信息，存在还有何价值？<br />
有用的优秀的东西共享有什么错？难道非要每个人都藏着掖着？</p>

</blockquote>

<p>麻烦你可笑别人的时候反思一下无知的自己。</p>

<p>我的确是通过别人推荐才知道Github的。但Github是一个代码托管网站，而不是“免费”的博客托管平台。我在使用它们的服务的同时也贡献和分享了很多代码，这才是促进这个社区良性发展的做法。否则，当Github降格为“免费”博客托管平台，当它充斥着各种垃圾内容时，整个社区的影响力也就被拉低了。</p>

<p>至于你到现在还不清楚谁封锁的谁，我就不嘲讽你了。因为很明显你不是一个经常使用国外服务的网民，否则当国外巨多的服务提供商拒绝中国IP的访问，当国外巨多服务提供商屏蔽中国邮件提供商时，你才能深刻体会中国的蝗虫的力量。</p>

<p>分享经验本没有错，质疑它可能造成一些不好的后果也很合理。但你这么无知还嘲笑别人就很有问题了。我也充分相信假如你使用Github，也不会产出什么高质量内容。<br />
</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="December 15, 2012 12:41 PM">2012年12月15日 12:41</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-266990">#</a>
 | <a href="#comment-text" title="引用freeMe的这条留言" onclick="return CommentQuote('comment-quote-266990','freeMe');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-267010" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">jerry</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-267010">
            <p>睡不着，折腾了一下，为啥不成功呢？GitHub发的邮件太奇怪了，等于啥也没说：</p>

<p>The page build failed with the following error:<br />
page build failed</p>

<p>请大神帮忙看看： <a href="https://github.com/JerryBian/jekyll_demo" rel="nofollow"><a href="https://github.com/JerryBian/jekyll_demo" rel="nofollow">https://github.com/JerryBian/jekyll_demo</a></a></p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="December 16, 2012  6:54 AM">2012年12月16日 06:54</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-267010">#</a>
 | <a href="#comment-text" title="引用jerry的这条留言" onclick="return CommentQuote('comment-quote-267010','jerry');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-267015" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">阮一峰</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-267015">
            <p>@jerry：</p>

<p>yaml头写得不对，冒号之后必须有一个空格。</p>

<p>layout:default要写成 layout: default</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="December 16, 2012 10:39 AM">2012年12月16日 10:39</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-267015">#</a>
 | <a href="#comment-text" title="引用阮一峰的这条留言" onclick="return CommentQuote('comment-quote-267015','阮一峰');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-267040" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">think</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-267040">
            <p>大神帮我看看,为什么我的显示出来是这个样子!数据展示不出来!<br />
<a href="http://wuhuanhost.github.com/blog/" rel="nofollow">http://wuhuanhost.github.com/blog/</a></p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="December 17, 2012  2:14 PM">2012年12月17日 14:14</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-267040">#</a>
 | <a href="#comment-text" title="引用think的这条留言" onclick="return CommentQuote('comment-quote-267040','think');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-267045" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">coanor</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-267045">
            <p>如果有 Dropbox 账号, <a href="http://calepin.co/" rel="nofollow">http://calepin.co/</a> 也是搭建blog的一个不错选择。</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="December 17, 2012  5:47 PM">2012年12月17日 17:47</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-267045">#</a>
 | <a href="#comment-text" title="引用coanor的这条留言" onclick="return CommentQuote('comment-quote-267045','coanor');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-267096" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://www.playhtml.com/" href="http://www.playhtml.com/" target="_blank" rel="nofollow">solar</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-267096">
            <p>这个碉堡啦，太好用了，很方便，也很Geek，就是开始创建那些东西对有些人来说可能有点难度。但是过了这关就万事大吉了。我在Windows上，使用TortoiseGit 提交，推送很方便。只是对普通用户来说估计就不好弄了，这需要会css和html。</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="December 19, 2012 11:09 AM">2012年12月19日 11:09</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-267096">#</a>
 | <a href="#comment-text" title="引用solar的这条留言" onclick="return CommentQuote('comment-quote-267096','solar');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-267189" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">fengxiaolong</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-267189">
            <p>终于可以找到一个靠谱的中文教程了</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="December 22, 2012  4:15 PM">2012年12月22日 16:15</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-267189">#</a>
 | <a href="#comment-text" title="引用fengxiaolong的这条留言" onclick="return CommentQuote('comment-quote-267189','fengxiaolong');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-267256" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">NaixSpirit</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-267256">
            <p>已经按照楼主的方式搭建完毕，谢谢楼主。<br />
另外，个人感觉不是每个人都会用git命令的，楼主的文章是需要一定的git命令基础的。</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="December 24, 2012 11:12 PM">2012年12月24日 23:12</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-267256">#</a>
 | <a href="#comment-text" title="引用NaixSpirit的这条留言" onclick="return CommentQuote('comment-quote-267256','NaixSpirit');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-267338" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://amoblin.github.com" href="http://amoblin.github.com" target="_blank" rel="nofollow">amoblin</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-267338">
            <p>不知道博主用mac吗？用mac的话可以用MarkBook来管理markdown文件，无缝发布到jekyll博客。这是我刚发布的一个软件，希望能够帮到大家：https://code.google.com/p/markbook/</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="December 27, 2012 11:52 AM">2012年12月27日 11:52</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-267338">#</a>
 | <a href="#comment-text" title="引用amoblin的这条留言" onclick="return CommentQuote('comment-quote-267338','amoblin');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-267351" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">dazzi</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-267351">
            <blockquote>
<pre>引用屁民的发言：</pre>

<p></p>

<p>同意，早晚会像sourceforge一样把中国ip屏蔽的。。。。<br />
总想白占别人便宜。。。。自愿低别人一等。。。。 </p>

</blockquote>

<p>不同意。就算博主不写也会有其他地方传播出去的。只要博主是现在中立的角度写无可厚非。博主并没有错反倒让人觉得你们看扁了自己。</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="December 27, 2012  9:30 PM">2012年12月27日 21:30</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-267351">#</a>
 | <a href="#comment-text" title="引用dazzi的这条留言" onclick="return CommentQuote('comment-quote-267351','dazzi');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-267626" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">ray</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-267626">
            <p>github却有被墙的危险，我已经发现了一些利用github发布和技术无关的一些敏感信息</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="January  7, 2013 10:17 AM">2013年1月 7日 10:17</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-267626">#</a>
 | <a href="#comment-text" title="引用ray的这条留言" onclick="return CommentQuote('comment-quote-267626','ray');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-268018" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://perry.asia/" href="http://perry.asia/" target="_blank" rel="nofollow">杜顺帆</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-268018">
            <p>Github Pages已经被墙了、</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="January 18, 2013  7:04 PM">2013年1月18日 19:04</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-268018">#</a>
 | <a href="#comment-text" title="引用杜顺帆的这条留言" onclick="return CommentQuote('comment-quote-268018','杜顺帆');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-268028" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">自由国度</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-268028">
            <p>好吧，我又来了，Github Pages全线被墙，起因不一定是这篇文章。</p>

<p>却一定是因为github好心，做了免费的cdn服务器，被某些人利用了，不为社区贡献任何代码，却把它当成了内容服务器。</p>

<p>请问连70块每年都舍不得花的所谓博主们，不知道这些天你们得到了什么，省了多少钱！</p>

<p>但是我知道一大帮人从此上github都要翻墙了，请原谅我说脏话，操！</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="January 18, 2013 11:55 PM">2013年1月18日 23:55</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-268028">#</a>
 | <a href="#comment-text" title="引用自由国度的这条留言" onclick="return CommentQuote('comment-quote-268028','自由国度');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-268074" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://demi-panda.com" href="http://demi-panda.com" target="_blank" rel="nofollow">熊猫家族</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-268074">
            <p>请教一个问题：就是在使用jekyll中，sort方式除了默认的排序外可以使用自定义的字段排序吗？</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="January 19, 2013  5:54 PM">2013年1月19日 17:54</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-268074">#</a>
 | <a href="#comment-text" title="引用熊猫家族的这条留言" onclick="return CommentQuote('comment-quote-268074','熊猫家族');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-268089" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">hyp</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-268089">
            <p>我上传了，但是github总是返回page build failed。你遇到过这种么?</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="January 20, 2013  4:11 PM">2013年1月20日 16:11</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-268089">#</a>
 | <a href="#comment-text" title="引用hyp的这条留言" onclick="return CommentQuote('comment-quote-268089','hyp');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-268091" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">lemon_shenzhen</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-268091">
            <p>跟着别人的帖子，用GitHub的GUI工具，建仓库Username.github.com, master分支，尝试了一天都没成功。<br />
可以访问http://Username.github.com, 但是index.html修改后没有生效。<br />
不知道为什么。</p>

<p>照着楼主的方法搭建blog一次通过。<br />
非常感谢，很严谨，代码没有任何错误。</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="January 20, 2013  5:48 PM">2013年1月20日 17:48</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-268091">#</a>
 | <a href="#comment-text" title="引用lemon_shenzhen的这条留言" onclick="return CommentQuote('comment-quote-268091','lemon_shenzhen');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-268093" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://wangyingang.github.com" href="http://wangyingang.github.com" target="_blank" rel="nofollow">wangyingang</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-268093">
            <p>唉，别问了，就在前几天，page.github.com被墙。</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="January 20, 2013  7:10 PM">2013年1月20日 19:10</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-268093">#</a>
 | <a href="#comment-text" title="引用wangyingang的这条留言" onclick="return CommentQuote('comment-quote-268093','wangyingang');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-268157" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">github被墙</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-268157">
            <p>大家不用争了，已经被封大陆IP了。</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="January 22, 2013 11:19 AM">2013年1月22日 11:19</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-268157">#</a>
 | <a href="#comment-text" title="引用github被墙的这条留言" onclick="return CommentQuote('comment-quote-268157','github被墙');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-268176" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">William</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-268176">
            <blockquote>
<pre>引用Dem的发言：</pre>

<p>把口碑式传播说成蝗虫的是什么心态。。。要是真的"生怕自己抢不到"的话就不会分享了</p>

</blockquote>

<p>现在你们满意了吗？</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="January 23, 2013 11:38 AM">2013年1月23日 11:38</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-268176">#</a>
 | <a href="#comment-text" title="引用William的这条留言" onclick="return CommentQuote('comment-quote-268176','William');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-268245" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://hechaocheng.cn/" href="http://hechaocheng.cn/" target="_blank" rel="nofollow">阿城守候</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-268245">
            <blockquote>
<pre>引用vampire的发言：</pre>

<p>请教一下，绑定域名是怎么操作的，没看明白，多谢。</p>

</blockquote>

<p>在您的项目根目录下新建个文件CNAME(不要扩展名,最简单"新建个文本文档.txt" 然后改成<b>CNAME</b>保存)内容就是您要绑定的域名www.abc.com(我要绑定的是<a href="http://detail.hechaocheng.cn" rel="nofollow">detail.hechaocheng.cn</a>里面的内容就填detail.hechaocheng.cn 然后做个cname解析到username.github.com(我的解析http://acity-waiting.github.com)不绑定的原始地址是http://acity-waiting.github.com/hechaocheng 绑定的是http://detail.hechaocheng.cn  <br />
希望对您有用....如果有不明白可以继续跟帖或者联系acity@hechaocheng.cn</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="January 25, 2013  8:13 PM">2013年1月25日 20:13</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-268245">#</a>
 | <a href="#comment-text" title="引用阿城守候的这条留言" onclick="return CommentQuote('comment-quote-268245','阿城守候');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-268246" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">superman</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-268246">
            <p>这篇文章写得很好，github pages上https://github.com/blog/272-github-pages就写了可以用github pages来写Blog，github创始人之一也写了一篇文章Blogging Like a Hacker。之前 github被封与用pages写博客无关，github也不可能封大陆IP，如果github真想封大陆IP的话，现在也不会解禁。而愚民只会把责任自以为是的推卸到无关的事物上。</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="January 25, 2013  8:41 PM">2013年1月25日 20:41</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-268246">#</a>
 | <a href="#comment-text" title="引用superman的这条留言" onclick="return CommentQuote('comment-quote-268246','superman');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-268327" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">kris</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-268327">
            <blockquote>
<pre>引用superman的发言：</pre>

<p>这篇文章写得很好，github pages上https://github.com/blog/272-github-pages就写了可以用github pages来写Blog，github创始人之一也写了一篇文章Blogging Like a Hacker。之前 github被封与用pages写博客无关，github也不可能封大陆IP，如果github真想封大陆IP的话，现在也不会解禁。而愚民只会把责任自以为是的推卸到无关的事物上。</p>

</blockquote>

<p>打脸打的漂亮！<br />
某些人的话真是难听，那浓郁的优越感不知道是怎么建立起来的。</p>

<p>以前研究git时搜到过博主的文章，今天又搜到这里了，对博主表示感谢！</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="January 29, 2013  7:50 PM">2013年1月29日 19:50</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-268327">#</a>
 | <a href="#comment-text" title="引用kris的这条留言" onclick="return CommentQuote('comment-quote-268327','kris');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-268358" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">Shawn</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-268358">
            <p>我在进行 git push origin gh-pages 操作后得到的提示是“<br />
fatal: Unable to find remote helper for 'https' ”。按照博主的步骤一步步，在google并尝试了在cent os上的解决方案后仍未解决。求助！<br />
</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="January 30, 2013  1:30 PM">2013年1月30日 13:30</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-268358">#</a>
 | <a href="#comment-text" title="引用Shawn的这条留言" onclick="return CommentQuote('comment-quote-268358','Shawn');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-268386" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://toolchainx.github.com/" href="http://toolchainx.github.com/" target="_blank" rel="nofollow">toolchainX</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-268386">
            <p>你好，博主这篇文章写得很好！我想问是如何添加baseurl的？ 我这里添加的baseurl为何不起作用，我现在的主页(index.html)显示了,但是我的第一篇文章为何显示不了。我的主页地址(http://toolchainx.github.com/)<br />
我的主页repo<br />
(https://github.com/toolchainX/toolchainx.github.com)<br />
希望博主能指教一二。</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="January 31, 2013  2:33 PM">2013年1月31日 14:33</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-268386">#</a>
 | <a href="#comment-text" title="引用toolchainX的这条留言" onclick="return CommentQuote('comment-quote-268386','toolchainX');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-268432" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://www.gudoor.com" href="http://www.gudoor.com" target="_blank" rel="nofollow">大熊</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-268432">
            <p>请教，博主的评论功能是用的什么？应该不是disqus。</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="February  1, 2013 12:26 PM">2013年2月 1日 12:26</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-268432">#</a>
 | <a href="#comment-text" title="引用大熊的这条留言" onclick="return CommentQuote('comment-quote-268432','大熊');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-268773" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://pinggit.github.com" href="http://pinggit.github.com" target="_blank" rel="nofollow">try</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-268773">
            <p>非常喜欢你blog的风格，思想，内容，形式。。。<br />
受教了，非常感谢！</p>

<p>正在研读这篇：<br />
<a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html" rel="nofollow">http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html</a></p>

<p>我严格按照顺序做，一切都好，但最后无法访问那个hello-world博客页面。</p>

<p>我是在本地启动jekyll server做的本地测试。你博客的例子是推到服务器上。这 是唯一的差别。<br />
难道在本地测试的话，博客hello-world写法需要改变？</p>

<pre>

<p>ping@640g-laptop:~/jekyll-demo/_posts$ cat 2012-08-25-hello-world.html<br />
---<br />
layout: default<br />
title: 你好，世界<br />
---</p>

{{ page.title }}

<p>我的第一篇文章</p>

<p>{{ page.date | date_to_string }}</p>

</pre>

        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="February 16, 2013 10:07 PM">2013年2月16日 22:07</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-268773">#</a>
 | <a href="#comment-text" title="引用try的这条留言" onclick="return CommentQuote('comment-quote-268773','try');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-268977" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">小兵</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-268977">
            <p>编码问题怎么破?<br />
我本地是win7的系统,刚开始用的是ANSI的编码,传上去是乱码.改成了UTF-8编码,过了一会儿看看,还是乱码</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="February 21, 2013  9:08 PM">2013年2月21日 21:08</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-268977">#</a>
 | <a href="#comment-text" title="引用小兵的这条留言" onclick="return CommentQuote('comment-quote-268977','小兵');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-268978" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">小兵</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-268978">
            <blockquote>
<pre>引用小兵的发言：</pre>

<p>编码问题怎么破?<br />
我本地是win7的系统,刚开始用的是ANSI的编码,传上去是乱码.改成了UTF-8编码,过了一会儿看看,还是乱码</p>

</blockquote>

<p>搞定了,还是对git不熟悉,只在本地commit了.没有push</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="February 21, 2013  9:22 PM">2013年2月21日 21:22</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-268978">#</a>
 | <a href="#comment-text" title="引用小兵的这条留言" onclick="return CommentQuote('comment-quote-268978','小兵');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-269084" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://detail.hechaocheng.cn/" href="http://detail.hechaocheng.cn/" target="_blank" rel="nofollow">阿城守候</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-269084">
            <p>@阮先生,你好！<br />
    我按照你提供的步驟，剛開始的時候能正常解析，但亂碼？我重新改了(utf-8)後，就一直正确解析了，你看下有時間幫幫我解決下可以嗎？我也發了一封郵件給你了,不知道你有沒有收到</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="February 24, 2013  9:21 AM">2013年2月24日 09:21</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-269084">#</a>
 | <a href="#comment-text" title="引用阿城守候的这条留言" onclick="return CommentQuote('comment-quote-269084','阿城守候');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-269194" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://www.AppleXsoft.com" href="http://www.AppleXsoft.com" target="_blank" rel="nofollow">蓝熙之</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-269194">
            <p>大家讨论了这么多，我就想知道，建立一个目录这些是不是就是用 html单独写的网页，还是说不同的文件夹，然后再有html网页？表示纠结，求指点！</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="February 27, 2013  3:51 PM">2013年2月27日 15:51</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-269194">#</a>
 | <a href="#comment-text" title="引用蓝熙之的这条留言" onclick="return CommentQuote('comment-quote-269194','蓝熙之');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-269331" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">fantouch</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-269331">
            <p>筑墙之人就是喜欢看着底下的p民这样内耗</p>

<blockquote>
<pre>引用github的发言：</pre>

<p></p>

<p><br />
强烈支持！占茅坑不拉屎者都滚！！！lz前两天下载jboss才发现sourceforge不能访问了，都是因为</p>

<p>这群损人利己的屎货！</p>

</blockquote>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="March  4, 2013 10:59 AM">2013年3月 4日 10:59</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-269331">#</a>
 | <a href="#comment-text" title="引用fantouch的这条留言" onclick="return CommentQuote('comment-quote-269331','fantouch');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-269422" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">自由</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-269422">
            <p>@自由国度，一类的人，自认为你自己很厉害。</p>

<p>你们说的这话，让我想起了，我刚上初中那会，说网吧不好，大家别去，但是还是有很多人去网吧学习，查资料；有的人适合放松，适合娱乐，只是很少的人，中了网瘾。</p>

<p>本来是用github的人，基本上都是为了学习，虽然我们写不出好的源码供大家分享，但是我们也在努力分享自己的一些成果，尽管没什么fork，没人watch，但请不要打击我们这部分人的积极性。</p>

<p>也许有一些人是为了免费而来，但是买域名，弄空间，不是我喜欢的方式，嫌麻烦，不是为了那小几百元！</p>

<p>你担心的问题，难道阮大师就没想过吗，他喜欢你们这样的人在他的博客上，天天骂人吗？</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="March  6, 2013  2:50 PM">2013年3月 6日 14:50</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-269422">#</a>
 | <a href="#comment-text" title="引用自由的这条留言" onclick="return CommentQuote('comment-quote-269422','自由');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-269538" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://jwhsir.tk" href="http://jwhsir.tk" target="_blank" rel="nofollow">JwhSir</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-269538">
            <p>为什么每次到最后一步的时候都会提示错误？就是git push origin master这一步 以前都是这样</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="March  9, 2013  8:28 PM">2013年3月 9日 20:28</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-269538">#</a>
 | <a href="#comment-text" title="引用JwhSir的这条留言" onclick="return CommentQuote('comment-quote-269538','JwhSir');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-270099" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">pizzabad</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-270099">
            <p>本生想用来当自己兄弟购物网店页面的，可是看到上面的评论，觉得占这个免费的便宜实在是有点不明智，开源本身就很不容易盈利。所以决定去购买git的空间，然后架设。顺便折腾折腾代码。当然楼主没有错，指出这个问题的人也没有错，主要的还是看使用这些方法的人。。。</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="March 23, 2013 10:35 PM">2013年3月23日 22:35</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-270099">#</a>
 | <a href="#comment-text" title="引用pizzabad的这条留言" onclick="return CommentQuote('comment-quote-270099','pizzabad');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-270163" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">wjx</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-270163">
            <p>阮老师，请教个问题，在您最后提到的使用Jekyll的站点列表里，发现了<a href="https://github.com/gitready/gitready" rel="nofollow">这个repo</a>, 从它的branch名和repo的命名来看，它不属于User/Organization Pages或Project Page，但<a href="http://uptime.netcraft.com/up/graph?site=http%3A%2F%2Fgitready.com" rel="nofollow">测试它的独立域名http://gitready.com</a>显示它似乎又是host在github上的，请问这是怎么回事？</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="March 26, 2013 11:20 AM">2013年3月26日 11:20</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-270163">#</a>
 | <a href="#comment-text" title="引用wjx的这条留言" onclick="return CommentQuote('comment-quote-270163','wjx');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-270269" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">C</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-270269">
            <p>非常感谢博主</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="March 31, 2013  9:45 AM">2013年3月31日 09:45</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-270269">#</a>
 | <a href="#comment-text" title="引用C的这条留言" onclick="return CommentQuote('comment-quote-270269','C');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-270831" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">lgx</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-270831">
            <p>按照博主的步骤一步一步的做了，可是还是有错误，最后一步把数据push了以后还是没有生成博客，找了好久也没找出解决的方法，可以帮我看下哪出错了么？ <a href="https://github.com/lexishenjingzhi/jekyll_demo" rel="nofollow">https://github.com/lexishenjingzhi/jekyll_demo</a></p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="April 17, 2013  8:48 PM">2013年4月17日 20:48</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-270831">#</a>
 | <a href="#comment-text" title="引用lgx的这条留言" onclick="return CommentQuote('comment-quote-270831','lgx');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-270855" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">Lumint</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-270855">
            <blockquote>
<pre>引用杜顺帆的发言：</pre>

<p>我应该是按步骤做了，但为什么输入网址后仍是404？</p>

</blockquote>

<p>我的也是404 啊  都部署成功了 就是显示404</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="April 18, 2013 12:42 PM">2013年4月18日 12:42</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-270855">#</a>
 | <a href="#comment-text" title="引用Lumint的这条留言" onclick="return CommentQuote('comment-quote-270855','Lumint');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-270876" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">Joe</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-270876">
            <p>非常感谢！this post is GREAT!!</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="April 19, 2013  8:44 PM">2013年4月19日 20:44</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-270876">#</a>
 | <a href="#comment-text" title="引用Joe的这条留言" onclick="return CommentQuote('comment-quote-270876','Joe');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-270892" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">wenfei-qi</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-270892">
            <p>thanks ! Helps a lot!</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="April 20, 2013  9:10 PM">2013年4月20日 21:10</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-270892">#</a>
 | <a href="#comment-text" title="引用wenfei-qi的这条留言" onclick="return CommentQuote('comment-quote-270892','wenfei-qi');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-271065" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">CrazyEgg</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-271065">
            <blockquote>
<pre>引用晒太阳的冰的发言：</pre>

<p></p>

<p>你搞清楚是谁墙谁。蝗虫一般贪小便宜的大陆人涌入，光耗资源不贡献代码。任谁是运营商都会屏蔽所有大陆IP的。</p>

</blockquote>
我不清楚你是怎么得出“光耗资源不贡献代码”的结论的，是不是你经常这么干？
你一点肚量都没有！
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="April 26, 2013 11:38 AM">2013年4月26日 11:38</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-271065">#</a>
 | <a href="#comment-text" title="引用CrazyEgg的这条留言" onclick="return CommentQuote('comment-quote-271065','CrazyEgg');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-271235" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">凡士林</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-271235">
            <p>很感兴趣，但是还摸不到门道。你这个博客是用什么搭建的呢？</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="May  3, 2013  1:05 PM">2013年5月 3日 13:05</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-271235">#</a>
 | <a href="#comment-text" title="引用凡士林的这条留言" onclick="return CommentQuote('comment-quote-271235','凡士林');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-271344" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">chyy</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-271344">
            <p>你好，按照您的说法初步搭建好了，请问后续的修改和发新文章应该怎样做呢，有什么参考书吗，谢谢</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="May  7, 2013 12:44 AM">2013年5月 7日 00:44</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-271344">#</a>
 | <a href="#comment-text" title="引用chyy的这条留言" onclick="return CommentQuote('comment-quote-271344','chyy');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-271387" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">小明</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-271387">
            <p>我了个去，太感激楼主啦。<br />
正想搞个博客练练手呢，还好咱用git托管代码着。</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="May  9, 2013  3:10 PM">2013年5月 9日 15:10</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-271387">#</a>
 | <a href="#comment-text" title="引用小明的这条留言" onclick="return CommentQuote('comment-quote-271387','小明');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-271409" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://abbshr.github.io/abbshrblog" href="http://abbshr.github.io/abbshrblog" target="_blank" rel="nofollow">ran</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-271409">
            <p>前来膜拜，测试博客建成，谢谢阮老师的分享。<br />
</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="May 10, 2013  5:16 PM">2013年5月10日 17:16</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-271409">#</a>
 | <a href="#comment-text" title="引用ran的这条留言" onclick="return CommentQuote('comment-quote-271409','ran');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-272157" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">fdx</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-272157">
            <blockquote>
<pre>引用liang456的发言：</pre>

<p><a href="http://liang456.github.com/gitpage/" rel="nofollow">http://liang456.github.com/gitpage/</a><br />
各位大神，我通过gh-pages分支上传了，上传以后出来一些乱码，能帮我看看是什么问题么？</p>

</blockquote>

<p>呵呵，千万不要用记事本做。会有个BOM头，然后就这种悲剧。我花了一天弄这个，从乱码到BOM头。搞得头晕，终于行了 <a href="http://fan123199.github.io/jekyll_demo/" rel="nofollow">http://fan123199.github.io/jekyll_demo/</a></p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="June 16, 2013  5:23 PM">2013年6月16日 17:23</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-272157">#</a>
 | <a href="#comment-text" title="引用fdx的这条留言" onclick="return CommentQuote('comment-quote-272157','fdx');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-272270" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://pigerla.com/" href="http://pigerla.com/" target="_blank" rel="nofollow">Spy</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-272270">
            <p>我的一篇文章出现很“与众不同”的问题，但找了很久都木有找到，阮一峰老师，您好，可以帮我看看吗，链接http://pigerla.com/2013/06/21/Web%E5%89%8D%E7%AB%AF%E6%80%A7%E8%83%BD%E4%BC%98%E5%8C%9631%E9%A1%B9/<br />
在首页也出现一些问题了，链接http://pigerla.com/<br />
真的奇怪啊，老师帮帮忙~~谢谢</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="June 22, 2013  8:32 PM">2013年6月22日 20:32</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-272270">#</a>
 | <a href="#comment-text" title="引用Spy的这条留言" onclick="return CommentQuote('comment-quote-272270','Spy');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-272271" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://pigerla.com/" href="http://pigerla.com/" target="_blank" rel="nofollow">Spy</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-272271">
            <p>我还有已经写好的博文文章，但是push上去以后就提示"page build fail"<br />
怀疑是文件编码的问题，究竟什么样的编码格式是才是正确的？</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="June 22, 2013  8:36 PM">2013年6月22日 20:36</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-272271">#</a>
 | <a href="#comment-text" title="引用Spy的这条留言" onclick="return CommentQuote('comment-quote-272271','Spy');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-272418" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">ledz</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-272418">
            <p>可笑啊有些的观点，github建站就是为了让世界上所有的人都用的，提供了免费的服务，世界合法公民就能享受，真心不知道这些人哪里来的优越感，敢问你们都为Kernel贡献了多少行代码？不还是用着linux，免费的服务收费的服务肯定是有区别的。我的需求之内用不到收费level的服务我还要给GitHub塞钱？请问你们给很多独立开发者资助了多少？你们用stardict你们为那个哥们捐了多少？你们用vim，你们为乌干达捐了多少？真可笑的“精英”嘴脸。博主这种善意科普的文章你们这种人才不会有这样的胸襟。分享就是收获！</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="June 30, 2013  3:43 PM">2013年6月30日 15:43</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-272418">#</a>
 | <a href="#comment-text" title="引用ledz的这条留言" onclick="return CommentQuote('comment-quote-272418','ledz');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-272952" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">linuxess</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-272952">
            <p>高手写的博文就是这么通俗易懂</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August  5, 2013  6:30 PM">2013年8月 5日 18:30</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-272952">#</a>
 | <a href="#comment-text" title="引用linuxess的这条留言" onclick="return CommentQuote('comment-quote-272952','linuxess');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-273079" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">victorwoo</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-273079">
            <p>现在是不是都得翻墙访问了？还有没有什么办法？域名指向之类的？</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 15, 2013  7:59 PM">2013年8月15日 19:59</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-273079">#</a>
 | <a href="#comment-text" title="引用victorwoo的这条留言" onclick="return CommentQuote('comment-quote-273079','victorwoo');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-273091" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">victorwoo</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-273091">
            <blockquote>
<pre>引用DouO的发言：</pre>

<p>評論功能並不是只能用disqus，所有社會化評論服務都是可以整合進去的。disqus也因爲它不是開源的，在黑客社區受到一些批評。如果想玩 Static Blog Generators 的話，我推薦試一下 ruhoh.com 。是jekyll-bootstrap的作者，作了jekyll-bootstrap後重新思考出來的作品。</p>

</blockquote>

<p>ruhoh.com 2.x能不能像jekyll那样，提交*.md上去，由github帮我们生成html？</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 16, 2013  6:03 PM">2013年8月16日 18:03</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-273091">#</a>
 | <a href="#comment-text" title="引用victorwoo的这条留言" onclick="return CommentQuote('comment-quote-273091','victorwoo');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-273175" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">someone</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-273175">
            <p>前面回复的人不一一引用了。</p>

<p>借用知乎的一句话，自我审查。</p>

<p>这最可怕了。</p>

<p>不多说了。</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 21, 2013  9:20 AM">2013年8月21日 09:20</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-273175">#</a>
 | <a href="#comment-text" title="引用someone的这条留言" onclick="return CommentQuote('comment-quote-273175','someone');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-273313" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://f2es.net/" href="http://f2es.net/" target="_blank" rel="nofollow">xiaoxiehang</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-273313">
            <p>阮哥  问一下文章列表页  如何显示摘要呢</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="August 28, 2013  4:00 PM">2013年8月28日 16:00</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-273313">#</a>
 | <a href="#comment-text" title="引用xiaoxiehang的这条留言" onclick="return CommentQuote('comment-quote-273313','xiaoxiehang');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-274159" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://home.ustc.edu.cn/~yinhuang/" href="http://home.ustc.edu.cn/~yinhuang/" target="_blank" rel="nofollow">GrahamLe</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-274159">
            <p>{{ page.date | date_to_string }}<br />
这个如果写上date_to_string时，jekyll build都是通不过的~~可否赐教~~或是po个链学习下？</p>

<p>谢谢阮老师~~</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="September 12, 2013  5:24 PM">2013年9月12日 17:24</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-274159">#</a>
 | <a href="#comment-text" title="引用GrahamLe的这条留言" onclick="return CommentQuote('comment-quote-274159','GrahamLe');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-274214" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://home.ustc.edu.cn/~yinhuang/" href="http://home.ustc.edu.cn/~yinhuang/" target="_blank" rel="nofollow">GrahamLe</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-274214">
            <p>无论怎么尝试，都没有像阮老师说的这样，push一下，10分钟后就可以通过那个访问了。怎么访问都是404~~所以好心酸~~阮老师快出现吧~~是不是有遗漏的步骤呢？？？</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="September 13, 2013  2:46 PM">2013年9月13日 14:46</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-274214">#</a>
 | <a href="#comment-text" title="引用GrahamLe的这条留言" onclick="return CommentQuote('comment-quote-274214','GrahamLe');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-274340" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">lee</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-274340">
            <blockquote>
<pre>引用reverland的发言：</pre>

<p>比较喜欢本地用vim来写东西，然后push上去，省心省力。还有就是觉得静态博客速度比较快，</p>

</blockquote>

<p>这个方法可以在windows下使用吗？</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="September 14, 2013  9:59 PM">2013年9月14日 21:59</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-274340">#</a>
 | <a href="#comment-text" title="引用lee的这条留言" onclick="return CommentQuote('comment-quote-274340','lee');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-274654" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">Lisa</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-274654">
            <p>现在不管哪个行业都往国人素质上扯了，虽然不知道各位在说什么，不过以偏概全，一竿子打死一船人这样的人笔笔皆是。</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="September 18, 2013  9:10 AM">2013年9月18日 09:10</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-274654">#</a>
 | <a href="#comment-text" title="引用Lisa的这条留言" onclick="return CommentQuote('comment-quote-274654','Lisa');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-275439" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://hypergroups.github.com" href="http://hypergroups.github.com" target="_blank" rel="nofollow">HyperGroups</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-275439">
            <p>LZ你好，是否有关于Jekyll编译中文文件名的问题的设置，我用中文的文件名无法编译成功还。</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="September 23, 2013  9:30 PM">2013年9月23日 21:30</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-275439">#</a>
 | <a href="#comment-text" title="引用HyperGroups的这条留言" onclick="return CommentQuote('comment-quote-275439','HyperGroups');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-275440" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://hypergroups.github.com" href="http://hypergroups.github.com" target="_blank" rel="nofollow">HyperGroups</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-275440">
            <p>LZ你好，是否有关于Jekyll编译中文文件名的问题的设置，我用中文的文件名无法编译成功还。</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="September 23, 2013  9:31 PM">2013年9月23日 21:31</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-275440">#</a>
 | <a href="#comment-text" title="引用HyperGroups的这条留言" onclick="return CommentQuote('comment-quote-275440','HyperGroups');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-277348" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">油焖大黄瓜</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-277348">
            <p>@CK：<br />
在git上没有建repo</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="October  6, 2013  3:47 PM">2013年10月 6日 15:47</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-277348">#</a>
 | <a href="#comment-text" title="引用油焖大黄瓜的这条留言" onclick="return CommentQuote('comment-quote-277348','油焖大黄瓜');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-277386" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://zz-mars.github.io/" href="http://zz-mars.github.io/" target="_blank" rel="nofollow">zz</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-277386">
            <p>为什么我的首页里面能看到文章，但是就是没有链接啊。。就是 你好，世界 的这个链接</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="October  6, 2013 10:38 PM">2013年10月 6日 22:38</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-277386">#</a>
 | <a href="#comment-text" title="引用zz的这条留言" onclick="return CommentQuote('comment-quote-277386','zz');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-277930" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">open</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-277930">
            <blockquote>
<pre>引用ledz的发言：</pre>

<p>可笑啊有些的观点，github建站就是为了让世界上所有的人都用的，提供了免费的服务，世界合法公民就能享受！</p>

</blockquote>

<p>赞同！总有些人觉得或者希望自己高人一等，故作嘴脸。互联网的精神是自由，开放，平等。</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="October 10, 2013 10:17 AM">2013年10月10日 10:17</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-277930">#</a>
 | <a href="#comment-text" title="引用open的这条留言" onclick="return CommentQuote('comment-quote-277930','open');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-278654" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">enzo123</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-278654">
            <p>很好哇，被墙的担心还是有的，想当年用GOOLEDOC费了好大劲写了一批文档，后来被墙了</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="October 15, 2013  2:13 PM">2013年10月15日 14:13</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-278654">#</a>
 | <a href="#comment-text" title="引用enzo123的这条留言" onclick="return CommentQuote('comment-quote-278654','enzo123');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-279545" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://blog.mo2g.com" href="http://blog.mo2g.com" target="_blank" rel="nofollow">磨途歌</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-279545">
            <p>感谢博主分享经验，等有时间了再尝试全静态博客</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="October 21, 2013  5:26 PM">2013年10月21日 17:26</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-279545">#</a>
 | <a href="#comment-text" title="引用磨途歌的这条留言" onclick="return CommentQuote('comment-quote-279545','磨途歌');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-280159" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">Robter</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-280159">
            <p>好文章……看了文章之后发现滚动条才到一半，后来发现评论里喷素质的占一半……然后无语之。<br />
谢谢博主给我带来新思想……<br />
我已经有想法用这种方式去建立自己的blog了。当然，不会使用github的资源。准备挂到我的DO-VPS。我觉得用文本来建立静态博客一定能带来速度上的提升。去trytry了~</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="October 25, 2013  9:32 AM">2013年10月25日 09:32</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-280159">#</a>
 | <a href="#comment-text" title="引用Robter的这条留言" onclick="return CommentQuote('comment-quote-280159','Robter');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-280993" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">kuma</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-280993">
            <p>yoho，成功了。</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="October 29, 2013 10:30 AM">2013年10月29日 10:30</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-280993">#</a>
 | <a href="#comment-text" title="引用kuma的这条留言" onclick="return CommentQuote('comment-quote-280993','kuma');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-283594" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">MXMR</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-283594">
            <p>博主<br />
我在测试时，将index.html内，文章标题链接中的<br />
{{ site.baseurl }}<br />
去掉才成功，否则主页能打开，文章打不开，不知为何。</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="November  5, 2013  5:59 PM">2013年11月 5日 17:59</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-283594">#</a>
 | <a href="#comment-text" title="引用MXMR的这条留言" onclick="return CommentQuote('comment-quote-283594','MXMR');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-285635" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">wilesduan</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-285635">
            <blockquote>
<pre>引用自由国度的发言：</pre>

<p>我不希望以后连github都要翻墙才能用，相信你也不愿意，你说是吧</p>

</blockquote>

<p>你觉得你说的这段话对的起你的名字？</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="November 12, 2013  3:15 PM">2013年11月12日 15:15</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-285635">#</a>
 | <a href="#comment-text" title="引用wilesduan的这条留言" onclick="return CommentQuote('comment-quote-285635','wilesduan');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-288924" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">lonzty</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-288924">
            <p>楼上那个自由国度，绝对是善于自我阉割、自我审查的可怜虫，<br />
github都还没表示，就预先幻想了<br />
一厢情愿认为github只是个托管代码的，<br />
一厢情愿的认为github会不欢迎用户来免费建站，<br />
可是github的态度不是摆在那吗，人家在首页推荐这个小工具！</p>

<p>至于GFW的疑虑，github将来有一天可能会访问不了，<br />
这个结果多数人或多或少都会有心理准备，<br />
你不将炮火指向真正的作恶者真理部，却来指责普通用户的使用导致它被屏蔽！<br />
所以你要求大家悄悄的使用，限于小圈子的使用，不要分享这些知识！<br />
以免你的使用被影响到！何其自私，何其可耻！</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="November 25, 2013  2:30 PM">2013年11月25日 14:30</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-288924">#</a>
 | <a href="#comment-text" title="引用lonzty的这条留言" onclick="return CommentQuote('comment-quote-288924','lonzty');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-290017" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://boa-d-luffy.github.io/blog/" href="http://boa-d-luffy.github.io/blog/" target="_blank" rel="nofollow">Norland</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-290017">
            <p>真的成功了，讲解很详细，太感谢了~</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="November 29, 2013  1:04 PM">2013年11月29日 13:04</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-290017">#</a>
 | <a href="#comment-text" title="引用Norland的这条留言" onclick="return CommentQuote('comment-quote-290017','Norland');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-292024" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://www.a.com" href="http://www.a.com" target="_blank" rel="nofollow">asdf</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-292024">
            <blockquote>
<pre>引用屁民的发言：</pre>

<p></p>

<p>同意，早晚会像sourceforge一样把中国ip屏蔽的。。。。<br />
总想白占别人便宜。。。。自愿低别人一等。。。。 </p>

</blockquote>

<p>别人就是免费提供让你用的，怎么成白占便宜低人一定呢，如果别人觉得亏就不提供这服务了，真是小人之心妒君子之腹，把github的好意也给扭曲了，还把用的人说的不堪。</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="December  9, 2013 11:13 AM">2013年12月 9日 11:13</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-292024">#</a>
 | <a href="#comment-text" title="引用asdf的这条留言" onclick="return CommentQuote('comment-quote-292024','asdf');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-292511" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">Jimmiry</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-292511">
            <p>搜到此文，发现有半数在讨论这样做好不好，呃，感觉用了它会有负罪感，于是给GitHub写信询问，答复如下（省略客服姓名）：</p>

<p>Hi there,</p>

<p>Please check out GitHub Pages – this allows you to create and host static sites including blogs on GitHub infrastructure:</p>

<p><a href="http://pages.github.com/" rel="nofollow">http://pages.github.com/</a></p>

<p>Cheers,</p>

<p>不管怎么说，官方是允许的。至于会不会有人把它用烂，还是看使用者吧。</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="December 11, 2013 11:41 PM">2013年12月11日 23:41</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-292511">#</a>
 | <a href="#comment-text" title="引用Jimmiry的这条留言" onclick="return CommentQuote('comment-quote-292511','Jimmiry');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-293347" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">jone</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-293347">
            <p>请教楼主，我按照你的教程来着，但是为什么提示建立失败呢？我都是一步步按照你的教程来的啊？写之前要做什么准备吗？</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="December 16, 2013 10:49 PM">2013年12月16日 22:49</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-293347">#</a>
 | <a href="#comment-text" title="引用jone的这条留言" onclick="return CommentQuote('comment-quote-293347','jone');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-293649" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://ueshell.com" href="http://ueshell.com" target="_blank" rel="nofollow">大鱼</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-293649">
            <p>不错的方法。<br />
没有必要争吵。</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="December 18, 2013 11:44 PM">2013年12月18日 23:44</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-293649">#</a>
 | <a href="#comment-text" title="引用大鱼的这条留言" onclick="return CommentQuote('comment-quote-293649','大鱼');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-293989" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">呵呵</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-293989">
            <p>Jekyll 音标标错误导许多人</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="December 21, 2013  3:45 PM">2013年12月21日 15:45</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-293989">#</a>
 | <a href="#comment-text" title="引用呵呵的这条留言" onclick="return CommentQuote('comment-quote-293989','呵呵');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-295037" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">woyaowenzi</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-295037">
            <blockquote>
<pre>引用HyperGroups的发言：</pre>

<p>LZ你好，是否有关于Jekyll编译中文文件名的问题的设置，我用中文的文件名无法编译成功还。</p>

</blockquote>

<p>在_config.yml文件中添加：encoding: utf-8</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="December 28, 2013 11:28 PM">2013年12月28日 23:28</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-295037">#</a>
 | <a href="#comment-text" title="引用woyaowenzi的这条留言" onclick="return CommentQuote('comment-quote-295037','woyaowenzi');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-295625" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">过客</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-295625">
            <p>求教 <br />
创建分支$ git checkout --orphan gh-pages 时显示错误<br />
error: did you mean `--orphan` (with two dashes ?)<br />
跪求指导。。。</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="January  2, 2014 10:34 AM">2014年1月 2日 10:34</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-295625">#</a>
 | <a href="#comment-text" title="引用过客的这条留言" onclick="return CommentQuote('comment-quote-295625','过客');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-296043" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author"><a title="http://bonkebo.github.io/Blog/" href="http://bonkebo.github.io/Blog/" target="_blank" rel="nofollow">Bonkebo</a></span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-296043">
            <p>这里面样式表按照什么路径来？</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="January  4, 2014  2:11 PM">2014年1月 4日 14:11</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-296043">#</a>
 | <a href="#comment-text" title="引用Bonkebo的这条留言" onclick="return CommentQuote('comment-quote-296043','Bonkebo');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-296240" class="comment">
    <div  class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">过客</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-296240">
            <p>又试了一遍<br />
又在最后一步出错了 说是连不到github.com 真心跪求指导。。。</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="January  5, 2014 10:42 AM">2014年1月 5日 10:42</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-296240">#</a>
 | <a href="#comment-text" title="引用过客的这条留言" onclick="return CommentQuote('comment-quote-296240','过客');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    
        
        <div id="comment-298376" class="comment">
    <div id="comment-last" class="inner">
        <div class="comment-header">
            <div class="asset-meta">
<p>
                <span class="byline">
                    

                    <span class="vcard author">阮一峰</span>

 说：
                </span>
</p>
            </div>
        </div>
        <div class="comment-content" id="comment-quote-298376">
            <p>本文关闭留言功能。</p>

<p>遇到问题的网友，可以参考以下网址。</p>

<p>- 我的实例库: <a href="https://github.com/ruanyf/jekyll_demo" rel="nofollow">https://github.com/ruanyf/jekyll_demo</a></p>

<p>- 发明者mojombo的实例库：<a href="https://github.com/mojombo/mojombo.github.io" rel="nofollow"><a href="https://github.com/mojombo/mojombo.github.io" rel="nofollow">https://github.com/mojombo/mojombo.github.io</a></a></p>

<p>- 官方网站：<a href="http://jekyllrb.com/" rel="nofollow"><a href="http://jekyllrb.com/" rel="nofollow">http://jekyllrb.com/</a></a><br />
</p>
        </div>
<div class="comment-footer">
<div class="comment-footer-inner">
<p>
                   <abbr class="published" title="January 19, 2014 11:34 PM">2014年1月19日 23:34</abbr>
 | <a href="http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html#comment-298376">#</a>
 | <a href="#comment-text" title="引用阮一峰的这条留言" onclick="return CommentQuote('comment-quote-298376','阮一峰');">引用</a>
</p>
</div>
</div>
    </div>
</div>
        
    </div>
        
    


    
    


</div>




                        </div>
                    </div>

                </div>
            </div>
        <script type="text/javascript" src="http://www.ruanyifeng.com/blog/js/prism.js"></script>
        <script type="text/javascript" src="/blog/checker.js"></script> 
            <div id="footer">
<div id="footer-inner">
  <div id="footer-content">

      
<!--
      <section> 
     </section>
  <p><a title="Instagram" target="_blank" href="http://instagram.com/ruanyf">Instagram</a></p>
       <p><a title="订阅" href="https://app.feedblitz.com/f/f.fbz?Sub=348868" target="_blank">邮件订阅</a></p>
  
       <h2>Feed</h2>
       <p><a title="FeedBurner" href="http://feeds.feedburner.com/ruanyifeng" target="_blank">FeedBurner</a></p>
       <p><a title="atom.xml" href="http://www.ruanyifeng.com/blog/atom.xml" target="_blank">atom.xml</a></p>
     
      <p>支付宝：<a title="支付宝" href="alipays://platformapi/startapp?appId=20000067&url=http%3A%2F%2Fwww.ruanyifeng.com%2Fblog" target="_blank">yifeng.ruan@gmail.com</a></p>
-->

     <section>
<!--
       <h2>授权方式</h2>
       <p><a title="许可证" href="http://creativecommons.org/licenses/by-nc-nd/3.0/deed.zh" target="_blank">自由转载-非商用-非衍生-保持署名</a></p>
       <h2>微信公号</h2>
       <h2>社交帐号</h2>
       <h2>联系方式</h2>
     -->
       <p><img src="https://www.wangbase.com/blogimg/asset/202001/bg2020013101.jpg" alt="微信扫描"></p>
       <p>
         <a title="微博" href="http://weibo.com/ruanyf" target="_blank">Weibo</a> | 
         <a title="Twitter" target="_blank" href="https://twitter.com/ruanyf">Twitter</a> |
         <a title="GitHub" target="_blank" href="https://github.com/ruanyf">GitHub</a>
       </p>
     
     <p>Email: <a title="电子邮件" href="mailto:yifeng.ruan@gmail.com" target="_blank">yifeng.ruan@gmail.com</a></p>
     </section>
  
  


  </div>
</div>
</div>

<script>
  (function(i,s,o,g,r,a,m){i['GoogleAnalyticsObject']=r;i[r]=i[r]||function(){
  (i[r].q=i[r].q||[]).push(arguments)},i[r].l=1*new Date();a=s.createElement(o),
  m=s.getElementsByTagName(o)[0];a.async=1;a.src=g;m.parentNode.insertBefore(a,m)
  })(window,document,'script','//www.google-analytics.com/analytics.js','ga');

  ga('create', 'UA-46829782-1', 'ruanyifeng.com');
  ga('send', 'pageview');

</script>

<script type="text/javascript" src="/blog/stats.js"></script>
<script>
var supportImg = document.querySelector('#support-img');

if (supportImg && _hmt) {
  _hmt.push(['_trackEvent', 'banner', 'load']);
  supportImg.addEventListener('click', function () {
    _hmt.push(['_trackEvent', 'banner', 'click']);
  }, false);
}

var homepageImg = document.querySelector('#homepage_sponsor');
if (homepageImg && _hmt) {
  _hmt.push(['_trackEvent', 'homepage-banner', 'load']);
  homepageImg.addEventListener('click', function () {
    _hmt.push(['_trackEvent', 'homepage-banner', 'click']);
  }, false);
}
</script>


<div id="share_button_proto" style="display:none;">
<a class="bshareDiv" href="http://www.bshare.cn/share">分享按钮</a>



<script type="text/javascript" charset="utf-8" src="http://static.bshare.cn/b/buttonLite.js#uuid=15e016b4-0028-44f1-a40d-a3c9d9c13c28&style=10&bgcolor=#fff&bp=weixin,qqim,qzone,qqmb,sinaminiblog,fanfou,xueqiu,douban,facebook,twitter,gplus,instapaper&ssc=false"></script>
<script type="text/javascript" charset="utf-8">
bShare.addEntry({
    title: document.getElementById("page-title").innerHTML,
url:window.location.href
});
</script>
</div>

<script>
document.getElementById("share_button").innerHTML=document.getElementById("share_button_proto").innerHTML;
</script>





        </div>
    </div>
</body>
</html>
