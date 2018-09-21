## 文章索引
1、 <a href="#1网易云信周梁伟专访亿级架构im平台的技术难点解析" >网易云信周梁伟专访：亿级架构IM平台的技术难点解析</a><br/>
2、 <a href="#2命令行通配符教程" >命令行通配符教程</a><br/>
3、 <a href="#3文章-使用apache-kafka和ksql实现流处理普及化第二部分" >文章： 使用Apache Kafka和KSQL实现流处理普及化——第二部分</a><br/>
4、 <a href="#4文章-丁磊命名的这款翻译机凭什么成为有道的战略产品" >文章： 丁磊命名的这款翻译机，凭什么成为有道的战略产品？</a><br/>
5、 <a href="#5文章-aws上的计算抽象一个视觉故事" >文章： AWS上的计算抽象：一个视觉故事</a><br/>
6、 <a href="#6building-a-pwa-using-angular-6" >Building A PWA Using Angular 6</a><br/>
7、 <a href="#7性能比cpu高40倍英伟达发布推理专用gpu-tesla-t4" >性能比CPU高40倍！英伟达发布推理专用GPU Tesla T4</a><br/>
8、 <a href="#8ebay把平台更新为kubernetesenvoy和kafka计划开源硬件和软件" >eBay把平台更新为Kubernetes、Envoy和Kafka：计划开源硬件和软件</a><br/>
9、 <a href="#9eric-evans说ddd还未结束" >Eric Evans说DDD还未结束</a><br/>
10、 <a href="#10区块链在健康保险行业的落地探索" >区块链在健康保险行业的落地探索</a><br/>
11、 <a href="#11人工智能加医真云每年让5700万人告别误诊" >人工智能加“医真云”，每年让5700万人告别误诊</a><br/><h1 id="#title_0" >1、网易云信周梁伟专访：亿级架构IM平台的技术难点解析</h1>
徐川
[http://www.infoq.com/cn/news/2018/09/netease-IM-techpoint-annalysis?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/09/netease-IM-techpoint-annalysis?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>自从8月20号子弹短信在锤子发布会露面之后，关于它的讨论不绝于耳，7天融资1.5亿的传闻更是将它推到了风口浪尖。同时很多技术人开始分析它的代码，挖出了它的IM系统其实不是自研，而是使用网易云信提供的第三方服务。有人质疑说，第三方的SDK做一个demo跑跑还可以，能拿来开发正式产品吗？本文就想来谈谈IM开发的难点以及目前第三方IM服务的现状。</p> <i>By 徐川</i>
---------------
<h1 id="#title_1" >2、命令行通配符教程</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2018/09/bash-wildcards.html](http://www.ruanyifeng.com/blog/2018/09/bash-wildcards.html)
<p>一次性操作多个文件时，命令行提供通配符（wildcards），用一种很短的文本模式（通常只有一个字符），简洁地代表一组路径。</p>

        <p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018092001.jpg" alt="" title="" /></p>

<p>通配符又叫做 globbing patterns。因为 Unix 早期有一个<code>/etc/glob</code>文件保存通配符模板，后来 Bash 内置了这个功能，但是这个名字被保留了下来。</p>

<p>通配符早于正则表达式出现，可以看作是原始的正则表达式。它的功能没有正则那么强大灵活，但是胜在简单和方便。</p>

<p>本文介绍 Bash 的各种通配符。</p>

<h2>一、? 字符</h2>

<p><code>?</code>字符代表单个字符。</p>

<blockquote><pre><code class="language-bash">
# 存在文件 a.txt 和 b.txt
$ ls ?.txt
a.txt b.txt
</code></pre></blockquote>

<p>上面命令中，<code>?</code>表示单个字符，所以会同时匹配<code>a.txt</code>和<code>b.txt</code>。</p>

<p>如果匹配多个字符，就需要多个<code>?</code>连用。</p>

<blockquote><pre><code class="language-bash">
# 存在文件 a.txt、b.txt 和 ab.txt
$ ls ??.txt
ab.txt
</code></pre></blockquote>

<p>上面命令中，<code>??</code>匹配了两个字符。</p>

<p>注意，<code>?</code>不能匹配空字符。也就是说，它占据的位置必须有字符存在。</p>

<h2>二、* 字符</h2>

<p><code>*</code>代表任意数量的字符。</p>

<blockquote><pre><code class="language-bash">
# 存在文件 a.txt、b.txt 和 ab.txt
$ ls *.txt
a.txt b.txt ab.txt

# 输出所有文件
$ ls *
</code></pre></blockquote>

<p>上面代码中，<code>*</code>匹配任意长度的字符。</p>

<p><code>*</code>可以匹配空字符。</p>

<blockquote><pre><code class="language-bash">
# 存在文件 a.txt、b.txt 和 ab.txt
$ ls a*.txt
a.txt ab.txt
</code></pre></blockquote>

<h2>三、[...] 模式</h2>

<p><code>[...]</code>匹配方括号之中的任意一个字符，比如<code>[aeiou]</code>可以匹配五个元音字母。</p>

<blockquote><pre><code class="language-bash">
# 存在文件 a.txt 和 b.txt
$ ls [ab].txt
a.txt b.txt

$ ls *[ab].txt
ab.txt a.txt b.txt
</code></pre></blockquote>

<p><code>[start-end]</code>表示一个连续的范围。</p>

<blockquote><pre><code class="language-bash">
# 存在文件 a.txt、b.txt 和 c.txt
$ ls [a-c].txt
a.txt b.txt c.txt

# 存在文件 report1.txt、report2.txt 和 report3.txt
$ ls report[0-9].txt
report1.txt report2.txt report3.txt
</code></pre></blockquote>

<h2>四、<code>[^...]</code> 和 <code>[!...]</code></h2>

<p><code>[^...]</code>和<code>[!...]</code>表示匹配不在方括号里面的字符（不包括空字符）。这两种写法是等价的。</p>

<blockquote><pre><code class="language-bash">
# 存在文件 a.txt、b.txt 和 c.txt
$ ls [^a].txt
b.txt c.txt
</code></pre></blockquote>

<p>这种模式下也可以使用连续范围的写法<code>[!start-end]</code>。</p>

<blockquote><pre><code class="language-bash">
$ echo report[!1-3].txt
report4.txt report5.txt
</code></pre></blockquote>

<p>上面代码中，<code>[!1-3]</code>表示排除1、2和3。</p>

<h2>五、{...} 模式</h2>

<p><code>{...}</code> 表示匹配大括号里面的所有模式，模式之间使用逗号分隔。</p>

<blockquote><pre><code class="language-bash">
$ echo d{a,e,i,u,o}g
dag deg dig dug dog
</code></pre></blockquote>

<p>它可以用于多字符的模式。</p>

<blockquote><pre><code class="language-bash">
$ echo {cat,dog}
cat dog
</code></pre></blockquote>

<p><code>{...}</code>与<code>[...]</code>有一个很重要的区别。如果匹配的文件不存在，<code>[...]</code>会失去模式的功能，变成一个单纯的字符串，而<code>{...}</code>依然可以展开。</p>

<blockquote><pre><code class="language-bash">
# 不存在 a.txt 和 b.txt
$ ls [ab].txt
ls: [ab].txt: No such file or directory

$ ls {a,b}.txt
ls: a.txt: No such file or directory
ls: b.txt: No such file or directory
</code></pre></blockquote>

<p>上面代码中，如果不存在<code>a.txt</code>和<code>b.txt</code>，那么<code>[ab].txt</code>就会变成一个普通的文件名，而<code>{a,b}.txt</code>可以照样展开。</p>

<p>大括号可以嵌套。</p>

<blockquote><pre><code class="language-bash">
$ echo {j{p,pe}g,png}
jpg jpeg png
</code></pre></blockquote>

<p>大括号也可以与其他模式联用。</p>

<blockquote><pre><code class="language-bash">
$ echo {cat,d*}
cat dawg dg dig dog doug dug
</code></pre></blockquote>

<p>上面代码中，会先进行大括号扩展，然后进行<code>*</code>扩展。</p>

<h2>六、{start..end} 模式</h2>

<p><code>{start..end}</code>会匹配连续范围的字符。</p>

<blockquote><pre><code class="language-bash">
$ echo d{a..d}g
dag dbg dcg ddg

$ echo {11..15}
11 12 13 14 15
</code></pre></blockquote>

<p>如果遇到无法解释的扩展，模式会原样输出。</p>

<blockquote><pre><code class="language-bash">
$ echo {a1..3c}
{a1..3c}
</code></pre></blockquote>

<p>这种模式与逗号联用，可以写出复杂的模式。</p>

<blockquote><pre><code class="language-bash">
$ echo .{mp{3..4},m4{a,b,p,v}}
.mp3 .mp4 .m4a .m4b .m4p .m4v
</code></pre></blockquote>

<h2>七、注意点</h2>

<p>通配符有一些使用注意点，不可不知。</p>

<p><strong>（1）通配符是先解释，再执行。</strong></p>

<p>Bash 接收到命令以后，发现里面有通配符，会进行通配符扩展，然后再执行命令。</p>

<blockquote><pre><code class="language-bash">
$ ls a*.txt
ab.txt
</code></pre></blockquote>

<p>上面命令的执行过程是，Bash 先将<code>a*.txt</code>扩展成<code>ab.txt</code>，然后再执行<code>ls ab.txt</code>。</p>

<p><strong>（2）通配符不匹配，会原样输出。</strong></p>

<p>Bash 扩展通配符的时候，发现不存在匹配的文件，会将通配符原样输出。</p>

<blockquote><pre><code class="language-bash">
# 不存在 r 开头的文件名
$ echo r*
r*
</code></pre></blockquote>

<p>上面代码中，由于不存在<code>r</code>开头的文件名，<code>r*</code>会原样输出。</p>

<p>下面是另一个例子。</p>

<blockquote><pre><code class="language-bash">
$ ls *.csv
ls: *.csv: No such file or directory
</code></pre></blockquote> 

<p>另外，前面已经说过，这条规则对<code>{...}</code>不适用</p>

<p><strong>（3）只适用于单层路径。</strong></p>

<p>上面所有通配符只匹配单层路径，不能跨目录匹配，即无法匹配子目录里面的文件。或者说，<code>?</code>或<code>*</code>这样的通配符，不能匹配路径分隔符（<code>/</code>）。</p>

<p>如果要匹配子目录里面的文件，可以写成下面这样。</p>

<blockquote><pre><code class="language-bash">
$ ls */*.txt
</code></pre></blockquote>

<p><strong>（4）可用于文件名。</strong></p>

<p>Bash 允许文件名使用通配符。这时，引用文件名的时候，需要把文件名放在单引号里面。</p>

<blockquote><pre><code class="language-bash">
$ touch 'fo*'
$ ls
fo*
</code></pre></blockquote>

<p>上面代码创建了一个<code>fo*</code>文件，这时<code>*</code>就是文件名的一部分。</p>

<h2>八、参考链接</h2>

<ul>
<li></li>
<li></li>
</ul>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2018-09-20T17:41:34+08:00">2018年9月20日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>文集：</li>
<li>社交媒体：</li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------
<h1 id="#title_2" >3、文章： 使用Apache Kafka和KSQL实现流处理普及化——第二部分</h1>
Robin Moffatt
[http://www.infoq.com/cn/articles/democratizing-stream-processing-kafka-ksql-part2?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/democratizing-stream-processing-kafka-ksql-part2?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/democratizing-stream-processing-kafka-ksql-part2/zh/smallimage/Democratizing-Stream-Processing-Apache-Kafka-KSQL-Part-2-logo-small-1536080637584-1536941484783.jpg"/><p>在本文中，作者Robin Moffatt展示了如何借助一个电商实例应用程序使用Apache Kafka和KSQL构建数据集成和处理应用程序。本文讨论了三个应用场景：客户操作、操作仪表板、在线分析。</p> <i>By Robin Moffatt</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_3" >4、文章： 丁磊命名的这款翻译机，凭什么成为有道的战略产品？</h1>
陈思
[http://www.infoq.com/cn/articles/youdao-fanyiwang-2.0-pro?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/youdao-fanyiwang-2.0-pro?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/youdao-fanyiwang-2.0-pro/zh/smallimage/9-1537015668738.jpg"/><p>9月6日，网易有道AI开放日，专注翻译机研发的有道推出了新款产品：有道翻译王 2.0 pro。比起上一代产品，这次发布的新品功能更加强大，除了支持多语种翻译外，还可以作为智能语音助手使用。当然，更加强大的功能背后，更需要更加强大的售价来买单，这款新品将以1688元人民币的定价面世。InfoQ记者在发布会后对网易有道CEO周枫、网易有道副总裁刘韧磊以及有道首席科学家段亦涛进行了专访。</p> <i>By 陈思</i>
---------------
<h1 id="#title_4" >5、文章： AWS上的计算抽象：一个视觉故事</h1>
Massimo Re Ferre
[http://www.infoq.com/cn/articles/compute-abstractions-on-aws-a-visual-story?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/compute-abstractions-on-aws-a-visual-story?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/compute-abstractions-on-aws-a-visual-story/zh/smallimage/cloud-logo-1509665409121-1537014320985.jpg"/><p>围绕业界在过去的20年间所见证的不同级别的计算抽象的介绍。</p> <i>By Massimo Re Ferre</i> <i> Translated by 姚佳灵</i>
---------------
<h1 id="#title_5" >6、Building A PWA Using Angular 6</h1>
Ahmed Bouchefra
[https://www.smashingmagazine.com/2018/09/pwa-angular-6/](https://www.smashingmagazine.com/2018/09/pwa-angular-6/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/09/pwa-angular-6/" />
              <title>Building A PWA Using Angular 6</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>Building A PWA Using Angular 6</h1>
                  
                    
                    <address>Ahmed Bouchefra</address>
                  
                  <time datetime="2018-09-20T13:35:23&#43;02:00" class="op-published">2018-09-20T13:35:23+02:00</time>
                  <time datetime="2018-09-20T11:42:41&#43;00:00" class="op-modified">2018-09-20T11:42:41+00:00</time>
                </header>
                

<p>In this tutorial, we’ll be using the latest Angular 6 to build a PWA by implementing the core tenets that make a PWA. We’ll start by creating a front-end web application that consumes a JSON API. For this matter, we’ll be using the Angular <code>HttpClient</code> module to send HTTP requests to a statically JSON API generated from the  GitHub repository. We’ll also use Material Design for building the UI via the Angular Material package.</p>

<p>Next, we’ll use the “Audits” panel (Lighthouse)  from Chrome DevTools to analyze our web application against the core tenets of PWAs. Finally, we’ll explain and add the PWA features to our web application according to the “Progressive Web App” section in the Lighthouse report.</p>

<p>Before we start implementing our PWA, let’s first introduce PWAs and Lighthouse.</p>

<p><strong>Recommended reading</strong>: <em></em></p>

<h3 id="what-s-a-pwa">What’s A PWA?</h3>

<p>A Progressive Web App or PWA is a web application that has a set of capabilities (similar to native apps) which provide an app-like experience to users. PWAs need to meet a set of essential requirements that we’ll see next. PWAs are similar to native apps but are deployed and accessible from web servers via URLs, so we don’t need to go through app stores.</p>

<p>:</p>

<ul>
<li><strong>Progressive</strong><br />
Work for every user, regardless of browser choice, because they are built with progressive enhancement as a core tenet.</li>
<li><strong>Responsive</strong><br />
Fit any form factor, desktop, mobile, tablet, or whatever is next.</li>
<li><strong>Connectivity independent</strong><br />
Enhanced with service workers to work offline or on low-quality networks.</li>
<li><strong>App-like</strong><br />
Use the app-shell model to provide app-style navigation and interactions.</li>
<li><strong>Fresh</strong><br />
Always up-to-date thanks to the service worker update process.</li>
<li><strong>Safe</strong><br />
Served via HTTPS to prevent snooping and ensure content has not been tampered with.</li>
<li><strong>Discoverable</strong><br />
Are identifiable as “applications” thanks to W3C manifests and service worker registration scope allowing search engines to find them.</li>
<li><strong>Re-engageable</strong><br />
Make re-engagement easy through features like push notifications.</li>
<li><strong>Installable</strong><br />
Allow users to “keep” apps they find most useful on their home screen without the hassle of an app store.</li>
<li><strong>Linkable</strong><br />
Easily share via URL and not require complex installation.</li>
</ul>



<aside class="product-panel product-panel__tilted product-panel--book" data-audience="non-subscriber">
    <div class="container product-panel--book__container">
      <div class="panel__description panel__description--book">
    <p>Getting workflow <em>just</em> right ain’t an easy task. So are proper estimates. Or alignment among different departments. That’s why we’ve set up <strong>“this-is-how-I-work”-sessions</strong> — with smart cookies sharing what works well for them. A part of the , of course.</p>
      <a href="https://smashed.by/workflowpanelmembership" class="btn btn--green btn--large">
        Explore Smashing Membership&nbsp;↬
      </a>
      </div>
      <div class="panel__image panel__image--book">
        <a href="https://smashed.by/workflowpanelmembership" class="books__book__image">
        <div class="books__book__img">
          <img src="https://www.smashingmagazine.com/images/smashing-cat/smashing-tv-box-cat.svg" alt="Smashing TV, with live sessions for professional designers and developers." width="310" height="400">
        </div>
      </a>
      </div>
    </div>
  </aside>




<h3 id="introducing-lighthouse">Introducing Lighthouse</h3>

<p> is an open-source auditing tool created by Google which can be used to audit websites and applications for accessibility performance, SEO, best practices and PWA features.</p>

<p>You can access Lighthouse from the <em>Audit</em> tab in Chrome DevTools as a module in Node.js or as a CLI tool. You can use Lighthouse by providing an URL and then running the audits which will provide you with a report containing the auditing results which are basically suggestions on how you can improve your web application.</p>

<h3 id="installing-angular-cli-v6-and-generating-a-project">Installing Angular CLI v6 And Generating A Project</h3>

<p>In this section, we’ll install the latest version of Angular CLI then we’ll use it to create a new Angular 6 project.</p>

<p>Angular CLI requires <strong>Node.js &gt;= 8.9+</strong> so first make sure you have the required version installed by running the following command:</p>

<pre><code class="language-bash">$ node -v
</code></pre>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d48330c2-ac5e-40ae-b030-c100b58b1d71/node-version.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d48330c2-ac5e-40ae-b030-c100b58b1d71/node-version.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d48330c2-ac5e-40ae-b030-c100b58b1d71/node-version.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d48330c2-ac5e-40ae-b030-c100b58b1d71/node-version.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d48330c2-ac5e-40ae-b030-c100b58b1d71/node-version.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d48330c2-ac5e-40ae-b030-c100b58b1d71/node-version.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d48330c2-ac5e-40ae-b030-c100b58b1d71/node-version.png"
			sizes="100vw"
			alt="Node.js version"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Checking Node version. ()
		</figcaption>
	
</figure>


<p>In case you don’t have Node.js installed, you can simply head on to  and grab the Node binaries for your system.</p>

<p>Now, you can go ahead and install the latest version of Angular CLI by running:</p>

<pre><code class="language-bash">$ npm install -g @angular/cli 
</code></pre>

<p><strong>Note</strong>: <em>Depending on your npm configuration, you may need to add <code>_sudo_</code> to install packages globally.</em></p>

<p>You can generate your Angular 6 project by running the following command in your terminal:</p>

<pre><code class="language-bash">$ ng new pwademo
</code></pre>

<p>This will create a project with a structure that looks like:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d7426a30-d5e9-476f-b741-fd12e02a0053/project-structure.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d7426a30-d5e9-476f-b741-fd12e02a0053/project-structure.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d7426a30-d5e9-476f-b741-fd12e02a0053/project-structure.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d7426a30-d5e9-476f-b741-fd12e02a0053/project-structure.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d7426a30-d5e9-476f-b741-fd12e02a0053/project-structure.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d7426a30-d5e9-476f-b741-fd12e02a0053/project-structure.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d7426a30-d5e9-476f-b741-fd12e02a0053/project-structure.png"
			sizes="100vw"
			alt="Angular project structure"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Angular project structure. ()
		</figcaption>
	
</figure>


<p>Most work that’s done will be inside the <code>src/</code> folder that contains the source code of the application.</p>

<div class="sponsors__wide-place"></div>




<h3 id="creating-the-angular-application">Creating The Angular Application</h3>

<p>After generating a project, we’ll build a web application that consumes a JSON API and displays the items on the home page. We’ll use the <em>HttpClient</em> service for sending HTTP requests and Angular Material for building the UI.</p>

<h4 id="adding-angular-material">Adding Angular Material</h4>

<p>Thanks to Angular CLI v6 and the new <em>ng add</em> command, adding Angular Material to your project is only one command away. You just need to run the following command from your terminal:</p>

<pre><code class="language-bash">$ cd pwademo
$ ng add @angular/material
</code></pre>  











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4a4c58ed-c750-4bf8-ab8a-716665b8c4b9/adding-angular-material.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4a4c58ed-c750-4bf8-ab8a-716665b8c4b9/adding-angular-material.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4a4c58ed-c750-4bf8-ab8a-716665b8c4b9/adding-angular-material.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4a4c58ed-c750-4bf8-ab8a-716665b8c4b9/adding-angular-material.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4a4c58ed-c750-4bf8-ab8a-716665b8c4b9/adding-angular-material.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4a4c58ed-c750-4bf8-ab8a-716665b8c4b9/adding-angular-material.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4a4c58ed-c750-4bf8-ab8a-716665b8c4b9/adding-angular-material.png"
			sizes="100vw"
			alt="Adding Angular Material"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Adding Angular Material. ()
		</figcaption>
	
</figure>


<p>You can see from the screenshot that the command installs the required package from npm and update a bunch of files for setting up Angular Material in your project which previously needed manual updates.</p>

<h4 id="setting-up-httpclient-and-consuming-the-json-api">Setting Up <code>HttpClient</code> And Consuming The JSON API</h4>

<p>Now, let’s setup the Angular project to use <code>HttpClient</code> for sending HTTP requests. First, you need to import the <code>HttpClientModule</code> module in the main application module in the <code>src/app/app.module.ts</code> file:</p>

<pre class="break-out"><code class="language-javascript">/*...*/
import { HttpClientModule } from  '@angular/common/http';
@NgModule({
declarations: [
AppComponent
],
imports: [
/*...*/
HttpClientModule
],
providers: [],
bootstrap: [AppComponent]
})
export  class  AppModule { }
</code></pre>

<p>That’s it. We can now inject and use <code>HttpClient</code> in any component or service that belongs to the main module.</p>

<p>For demo purposes, we’ll consume a statically generated  . If you are consuming any other resource, make sure you have CORS enabled so the browser doesn’t disallow reading the remote resource due to the <strong>Same Origin Policy</strong>.</p>

<p>Let’s create a service that interfaces with the API. Inside your project folder, run:</p>

<pre><code class="language-bash">$ ng g service api
</code></pre>

<p>This will create a service called <code>ApiService</code> in the <code>src/app/api.service.ts</code> file.</p>

<p>Now open the <code>src/app/api.service.ts</code> file and update it to reflect the following changes:</p>

<pre class="break-out"><code class="language-javascript">import { Injectable } from  '@angular/core';
import { HttpClient } from  '@angular/common/http';
import { Observable } from  'rxjs';

export  interface  Item{
name:  string;
description:  string;
url:  string;
html:  string;
markdown:  string;
}

@Injectable({
providedIn:  'root'
})

export  class  ApiService {
private  dataURL:  string  =  "https://www.techiediaries.com/api/data.json";
constructor(private  httpClient:  HttpClient) {}
fetch():  Observable&lt;Item[]&gt;{
return &lt;Observable&lt;Item[]&gt;this.httpClient.get(this.dataURL);
}
}
</code></pre>

<p>We first imported the <code>HttpClient</code> and <code>Observable</code> classes then injected the <code>HttpClient</code> in the constructor as <code>httpClient</code> and added a <code>fetch()</code> method which calls the <code>get()</code> method of <code>HttpClient</code> (for sending an HTTP GET request to our JSON endpoint) and returns an Observable that we can subscribe to later.</p>

<p>We also declared an <code>Item</code> interface which represents a single item of the returned JSON data.</p>

<p>Next import this service from the application component. Open the <code>src/app/app.component.ts</code> file and add:</p>

<pre class="break-out"><code class="language-javascript">import { Component, OnInit } from  '@angular/core';
import { ApiService } from  './api.service';
import { Item } from  './api.service';

@Component({
selector:  'app-root',
templateUrl:  './app.component.html',
styleUrls: ['./app.component.css']
})
export  class  AppComponent  implements  OnInit{
title  =  'pwademo';
items:  Array&lt;Item&gt;;
constructor(private  apiService:  ApiService){
}
ngOnInit(){
this.fetchData();
}
fetchData(){
this.apiService.fetch().subscribe((data:  Array&lt;Item&gt;)=&gt;{
console.log(data);
this.items  =  data;
}, (err)=&gt;{
console.log(err);
});
}
}
</code></pre> 

<p>We import the <code>ApiService</code> that we created before and we inject it as <code>apiService</code>, we also import the <code>Item</code> class which represents a single item of our JSON data and we declare the <code>items</code> variable of type <code>Array&lt;Item&gt;</code> which will hold the fetched items.</p>

<p>Next, we add a <code>fetchData()</code> method which calls our <code>fetch()</code> method that we defined in the <code>ApiService</code> which returns an Observable. We simply subscribe to this observable in order to send a GET request to our JSON endpoint and get the response data that we finally assign to the <code>items</code> array.</p>

<p>We call the <code>fetchData()</code> method in the <code>ngOnInit()</code> life-cycle event so it will be called once the <code>AppComponent</code> component is initialized.</p>

<h4 id="adding-the-application-ui">Adding The Application UI</h4>

<p>Our application UI will consist of a navigation bar and the skeleton of the page which will be created with Angular Material.</p>

<p>Before using an Angular Material component, you’ll need to import its module. Each Material component belongs to its own module.</p>

<p>Open the <code>src/app/app.module.ts</code> file and add the following imports:</p>

<pre class="break-out"><code class="language-javascript">/*...*/
import { MatToolbarModule } from  '&#64;angular/material/toolbar';
import { MatCardModule } from  '&#64;angular/material/card';
import { MatButtonModule } from  '&#64;angular/material/button';

&#64;NgModule({
declarations: [
AppComponent
],
imports: [
/*...*/
MatToolbarModule,
MatCardModule,
MatButtonModule
],
providers: [],
bootstrap: [AppComponent]
})
export  class  AppModule { }
</code></pre>

<p>We import modules for toolbar, card and button components and we add them to the <em>imports</em> array of the <code>AppModule</code>.</p>

<p>Next, open the <code>src/app/app.component.html</code> file, delete what’s in there and add:</p>

<pre><code class="language-html">&lt;mat-toolbar  color="primary"&gt;
&lt;mat-toolbar-row&gt;
&lt;span&gt;JS-jargon&lt;/span&gt;
&lt;/mat-toolbar-row&gt;
&lt;/mat-toolbar&gt;
&lt;main&gt;
&lt;mat-card *ngFor="let item of items"&gt;
&lt;mat-card-header&gt;
&lt;mat-card-title&gt;{{item.name}}&lt;/mat-card-title&gt;
&lt;/mat-card-header&gt;
&lt;mat-card-content&gt;
{{item.description}}
&lt;/mat-card-content&gt;
&lt;mat-card-actions&gt;
&lt;a  mat-raised-button  href="{{item.url}}"  color="primary"&gt;More&lt;/a&gt;
&lt;/mat-card-actions&gt;
&lt;/mat-card&gt;
&lt;/main&gt;
</code></pre>

<p>We use Material components to create the UI. The  <code>&lt;mat-toolbar&gt;</code> component is used to create a Material toolbar and the <code>&lt;mat-card&gt;</code> component is used to create a Material card etc.</p>

<p>We iterate over the <code>items</code> array which gets populated by the <code>fetchData()</code> method when the component is initialized, and display items as Material cards. Each card contains the name, description and a link for more information (The link is styled as a Material button using the <code>mat-raised-button</code> directive).</p>

<p>This is a screenshot of the application:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2b8b0954-71fc-48f5-af57-01d7b98ac335/pwa-demo.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2b8b0954-71fc-48f5-af57-01d7b98ac335/pwa-demo.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2b8b0954-71fc-48f5-af57-01d7b98ac335/pwa-demo.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2b8b0954-71fc-48f5-af57-01d7b98ac335/pwa-demo.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2b8b0954-71fc-48f5-af57-01d7b98ac335/pwa-demo.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2b8b0954-71fc-48f5-af57-01d7b98ac335/pwa-demo.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2b8b0954-71fc-48f5-af57-01d7b98ac335/pwa-demo.png"
			sizes="100vw"
			alt="Demo Application"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Demo Application. ()
		</figcaption>
	
</figure>


<h3 id="building-the-application-for-production">Building The Application For Production</h3>

<p>Typically, when checking your application for PWA features you should first build it for production because most PWA features are not added in development. For example, you don’t want to have service workers and caching enabled in development since you will periodically need to update the files.</p>

<p>Let’s build the application for production using the following command:</p>

<pre><code class="language-bash">$ ng build --prod
</code></pre>

<p>The production build will be available from the <code>dist/pwademo</code> folder. We can use a tool like <code>http-server</code> to serve it.</p>

<p>First, install <code>http-server</code> using the following command:</p>

<pre><code class="language-bash">$ npm i -g http-server
</code></pre>

<p>You can then run it using the following command:</p>

<pre><code class="language-bash">$ cd dist/pwademo
$ http-server -o
</code></pre>

<p>The <code>-o</code> option will automatically open the default browser in your system and navigate to the <code>http://127.0.0.1:8080/</code> address where our web application is available.</p>

<h3 id="analyzing-the-application-using-lighthouse">Analyzing The Application Using Lighthouse</h3>

<p>Let’s now analyze our application using Lighthouse. First, launch Chrome and visit our application address <code>http://127.0.0.1:8080/</code>.</p>

<p>Next, open <em>Developer Tools</em> or press <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>I</kbd> and click on the <em>Audit</em> panel.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d19e6cf0-3f3a-4bcd-9a05-57263e7cf991/perform-audit.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d19e6cf0-3f3a-4bcd-9a05-57263e7cf991/perform-audit.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d19e6cf0-3f3a-4bcd-9a05-57263e7cf991/perform-audit.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d19e6cf0-3f3a-4bcd-9a05-57263e7cf991/perform-audit.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d19e6cf0-3f3a-4bcd-9a05-57263e7cf991/perform-audit.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d19e6cf0-3f3a-4bcd-9a05-57263e7cf991/perform-audit.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d19e6cf0-3f3a-4bcd-9a05-57263e7cf991/perform-audit.png"
			sizes="100vw"
			alt="Perform an audit"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Perform an audit. ()
		</figcaption>
	
</figure>


<p>You preferably need to set the <em>Emulation</em> to <em>Mobile</em> instead of <em>Desktop</em> to emulate a mobile environment. Next, click on <em>Perform an audit&hellip;</em> blue button. You’ll have a dialog opened in which you need to choose the types of the audits you want to perform against your web application. Un-check all types but <em>Progressive Web App</em> and click the <em>Run audit</em> button.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3bcbd012-5aa5-41b1-8a75-ec082f02ecb6/progressive-web-app.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3bcbd012-5aa5-41b1-8a75-ec082f02ecb6/progressive-web-app.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3bcbd012-5aa5-41b1-8a75-ec082f02ecb6/progressive-web-app.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3bcbd012-5aa5-41b1-8a75-ec082f02ecb6/progressive-web-app.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3bcbd012-5aa5-41b1-8a75-ec082f02ecb6/progressive-web-app.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3bcbd012-5aa5-41b1-8a75-ec082f02ecb6/progressive-web-app.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3bcbd012-5aa5-41b1-8a75-ec082f02ecb6/progressive-web-app.png"
			sizes="100vw"
			alt="Progressive Web App Audits"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Progressive Web App Audits. ()
		</figcaption>
	
</figure>


<p>Wait for the Lighthouse to generate the report. This is a screenshot of the result at this stage:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/91c1eb56-c6a5-45ec-84bf-ff7e4b85b60b/pwa-initial-report.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/91c1eb56-c6a5-45ec-84bf-ff7e4b85b60b/pwa-initial-report.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/91c1eb56-c6a5-45ec-84bf-ff7e4b85b60b/pwa-initial-report.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/91c1eb56-c6a5-45ec-84bf-ff7e4b85b60b/pwa-initial-report.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/91c1eb56-c6a5-45ec-84bf-ff7e4b85b60b/pwa-initial-report.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/91c1eb56-c6a5-45ec-84bf-ff7e4b85b60b/pwa-initial-report.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/91c1eb56-c6a5-45ec-84bf-ff7e4b85b60b/pwa-initial-report.png"
			sizes="100vw"
			alt="Initial PWA Report"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Initial Report. ()
		</figcaption>
	
</figure>


<p>Lighthouse performs a series of checks which validate the aspects of a Progressive Web App specified by the .
We get an initial score of <em><sup>36</sup>&frasl;<sub>100</sub></em> that’s because we have some audits passed.</p>

<p>Our application has <em>7</em> failed audits mainly related to <strong>Service Workers</strong>, <strong>Progressive Enhancement</strong>, <strong>HTTPS</strong> and <strong>Web App Manifest</strong> which are the core aspects of a PWA.</p>

<h4 id="registering-a-service-worker">Registering A Service Worker</h4>

<p>The first two failed audits (“Does not register a service worker” and “Does not respond with a 200 when offline”) are related to <strong>Service Workers</strong> and caching. So what’s a service worker?</p>

<p>A service worker is a feature that’s available on modern browsers which can be used as a network proxy that lets your application intercept network requests to cache assets and data. This could be used for implementing PWA features such as offline support and Push notifications etc.</p>

<p>To pass these audits we simply need to register a service worker and use it to cache files locally. When offline, the SW should return the locally cached version of the file. We’ll see a bit later how to add that with one CLI command.</p>

<p><strong>Recommended reading</strong>: <em></em></p>

<h4 id="progressive-enhancement">Progressive Enhancement</h4>

<p>The third failed audit (“Does not provide fallback content when JavaScript is not available”) is related to <strong>Progressive Enhancement</strong> which is an essential aspect of a PWA  and It simply refers to the capability of PWAs to run on different browsers but provide advanced features if they’re available. One simple example of PE is the use of the <code>&lt;noscript&gt;</code> HTML tag that informs users of the need to enable JavaScript to run the application in case It’s not enabled:</p>

<pre><code class="language-html">&lt;noscript&gt;
Please enable JavaScript to run this application.
&lt;/noscript&gt;
</code></pre>

<h4 id="https">HTTPS</h4>

<p>The fourth failed audit (“Does not redirect HTTP traffic to HTTPS”) is related to HTTPS which is also a core aspect of PWAs (service workers can be only served from secure origins, except for localhost). The “Uses HTTPS” audit itself is considered as passed by Lighthouse since we’re auditing localhost but once you use an actual host you need a SSL certificate.  You can get a free SSL certificate from different services such as Let’s Encrypt, Cloudflare, Firebase or Netlify etc.</p>

<h4 id="the-web-app-manifest">The Web App Manifest</h4>

<p>The three failed audits (“User will not be prompted to Install the Web App”, “Is not configured for a custom Splash Screen” and “Address bar does not match brand colors”) are related to a missing <strong>Web App Manifest</strong> which is a file in JSON format that provides the name, description, icons and other information required by a PWA. It lets users install the web app on the home screen just like native apps without going through an app store.</p>

<p>You need to provide a web app manifest and reference it from the <code>index.html</code> file using a <code>&lt;link&gt;</code> tag with <code>rel</code> property set to <code>manifest</code>. We’ll see next how we can do that automatically with one CLI command.</p>

<div class="sponsors__wide-place"></div>




<h3 id="implementing-pwa-features">Implementing PWA Features</h3>

<p>Angular CLI v6 allows you to quickly add PWA features to an existing Angular application. You can turn your application into a PWA by simply running the following command in your terminal from the root of the project:</p>

<pre><code class="language-bash">$ ng add @angular/pwa
</code></pre>

<p>The command automatically adds PWA features to our Angular application, such as:</p>

<ul>
<li>A <code>manifest.json</code> file,</li>
<li>Different sizes of icons in the <code>src/assets/icons</code> folder,</li>
<li>The <code>ngsw-worker.js</code> service worker.</li>
</ul>

<p>Open the <code>dist/</code> folder which contains the production build. You’ll find various files but let’s concentrate on the files related to PWA features that we mentioned above:</p>

<p>A <code>manifest.json</code> file was added with the following content:</p>

<pre><code class="language-javascript">{
    "name": "pwademo",
    "short_name": "pwademo",
    "theme_color": "#1976d2",
    "background_color": "#fafafa",
    "display": "standalone",
    "scope": "/",
    "start_url": "/",
    "icons": [
        {
        "src": "assets/icons/icon-72x72.png",
        "sizes": "72x72",
        "type": "image/png"
    },
    {
        "src": "assets/icons/icon-96x96.png",
        "sizes": "96x96",
        "type": "image/png"
    },
    {
        "src": "assets/icons/icon-128x128.png",
        "sizes": "128x128",
        "type": "image/png"
    },
    {
        "src": "assets/icons/icon-144x144.png",
        "sizes": "144x144",
        "type": "image/png"
    },
    {
        "src": "assets/icons/icon-152x152.png",
        "sizes": "152x152",
        "type": "image/png"
    },
    {
        "src": "assets/icons/icon-192x192.png",
        "sizes": "192x192",
        "type": "image/png"
    },
    {
        "src": "assets/icons/icon-384x384.png",
        "sizes": "384x384",
        "type": "image/png"
    },
    {
        "src": "assets/icons/icon-512x512.png",
        "sizes": "512x512",
        "type": "image/png"
    }
    ]
}
</code></pre>

<p>As you can see, the added <code>manifest.json</code> file has all the information required by a PWA such as the name, description and <code>start_url</code> etc.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/71ee25b8-7d4d-4377-bb5e-8edfb0cf6670/project-structure2.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/71ee25b8-7d4d-4377-bb5e-8edfb0cf6670/project-structure2.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/71ee25b8-7d4d-4377-bb5e-8edfb0cf6670/project-structure2.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/71ee25b8-7d4d-4377-bb5e-8edfb0cf6670/project-structure2.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/71ee25b8-7d4d-4377-bb5e-8edfb0cf6670/project-structure2.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/71ee25b8-7d4d-4377-bb5e-8edfb0cf6670/project-structure2.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/71ee25b8-7d4d-4377-bb5e-8edfb0cf6670/project-structure2.png"
			sizes="100vw"
			alt="Angular project structure"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Angular project structure. ()
		</figcaption>
	
</figure>


<p>The <code>manifest.json</code> file, links to icons with different sizes, that were also added automatically in the <code>assets/icons</code> folder. You will, of course, need to change those icons with your own once you are ready to build the final version of your PWA.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5b617a4e-c850-4b3c-a5d2-2badda38d3e5/project-structure3.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5b617a4e-c850-4b3c-a5d2-2badda38d3e5/project-structure3.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5b617a4e-c850-4b3c-a5d2-2badda38d3e5/project-structure3.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5b617a4e-c850-4b3c-a5d2-2badda38d3e5/project-structure3.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5b617a4e-c850-4b3c-a5d2-2badda38d3e5/project-structure3.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5b617a4e-c850-4b3c-a5d2-2badda38d3e5/project-structure3.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5b617a4e-c850-4b3c-a5d2-2badda38d3e5/project-structure3.png"
			sizes="100vw"
			alt="Angular project structure"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Angular project structure. ()
		</figcaption>
	
</figure>


<p>In the <code>index.html</code> file, the <code>manifest.json</code> file is referenced using:</p>

<pre><code class="language-html">&lt;link  rel="manifest"  href="manifest.json"&gt;
</code></pre>

<p>The <code>ngsw-worker.js</code> file, was also automatically added, which contains the service worker. The code to install this service worker is automatically inserted in the <code>src/app/app.module.ts</code> file:</p>

<pre class="break-out"><code class="language-javascript">...
import { ServiceWorkerModule } from  '@angular/service-worker';

@NgModule({
declarations: [
AppComponent
],

imports: [
...
ServiceWorkerModule.register('/ngsw-worker.js', { enabled:  environment.production })
],
</code></pre>

<p>The <code>@angular/service-worker</code> is installed by the <code>ng add</code> command and added as a dependency to <code>pwademo/package.json</code>:</p>

<pre><code class="language-javascript">"dependencies": {
...
"@angular/service-worker": "^6.1.0"
}
</code></pre>

<p>The service worker build support is also enabled in the CLI. In the <code>angular.json</code> file a <code>&quot;serviceWorker&quot;: true</code> configuration option is added.</p>

<p>In the <code>index.html</code> file a meta tag for  <code>theme-color</code>  with a value of <code>#1976d2</code> is added (It also corresponds to the <code>theme_color</code> value in the <code>manifest.json</code> file):</p>

<pre><code class="language-html">&lt;meta  name="theme-color"  content="#1976d2"&gt;
</code></pre>

<p>The theme color tells the browser what color to tint .</p>

<p>Adding the theme color to both the <code>index.html</code> and <code>manifest.json</code> files fixes the .</p>

<h4 id="the-service-worker-configuration-file">The Service Worker Configuration File</h4>

<p>Another file <code>src/ngsw-config.json</code> is added to the project but It’s not a required file for PWAs. It’s a configuration file which allows you to specify which files and data URLs the Angular service worker should cache and how it should update the cached files and data. You can find all details about this file from the official .</p>

<p><strong>Note</strong>: <em>As of this writing, with the latest <strong>6.1.3</strong> previous <code>ng add @angular/pwa</code> command : <code>Path “/ngsw-config.json” already exists</code> so for now the solution is to downgrade <code>@angular/cli</code> and <code>@angular/pwa</code> to version <strong>6.0.8</strong>.</em></p>

<p>Simply run the following commands in your project:</p>

<pre><code class="language-bash">$ npm i @angular/cli@6.0.8
$ ng i @angular/pwa@6.0.8
$ ng add @angular/pwa
</code></pre>

<p>Now let’s re-run the audits against our local PWA hosted locally. This is the new PWA score:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ae7aca32-0544-4bdb-862b-fe994459ef4a/pwa-report.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ae7aca32-0544-4bdb-862b-fe994459ef4a/pwa-report.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ae7aca32-0544-4bdb-862b-fe994459ef4a/pwa-report.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ae7aca32-0544-4bdb-862b-fe994459ef4a/pwa-report.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ae7aca32-0544-4bdb-862b-fe994459ef4a/pwa-report.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ae7aca32-0544-4bdb-862b-fe994459ef4a/pwa-report.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ae7aca32-0544-4bdb-862b-fe994459ef4a/pwa-report.png"
			sizes="100vw"
			alt="Initial PWA Report"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			PWA Report. ()
		</figcaption>
	
</figure>


<p>The Angular CLI doesn’t automatically add the JavaScript fallback code we mentioned in the Progressive Enhancement section so open the <code>src/index.html</code> file and add it:</p>

<pre><code class="language-html">&lt;noscript&gt;
Please enable JavaScript to run this application.
&lt;/noscript&gt;
</code></pre>

<p>Next, rebuild your application and re-run the audits. This is the result now:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3e6b8ed1-ce04-440b-9869-24c9ef2080e3/pwa-report-91.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3e6b8ed1-ce04-440b-9869-24c9ef2080e3/pwa-report-91.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3e6b8ed1-ce04-440b-9869-24c9ef2080e3/pwa-report-91.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3e6b8ed1-ce04-440b-9869-24c9ef2080e3/pwa-report-91.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3e6b8ed1-ce04-440b-9869-24c9ef2080e3/pwa-report-91.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3e6b8ed1-ce04-440b-9869-24c9ef2080e3/pwa-report-91.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3e6b8ed1-ce04-440b-9869-24c9ef2080e3/pwa-report-91.png"
			sizes="100vw"
			alt="Initial PWA Report"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			PWA Report. ()
		</figcaption>
	
</figure>


<p>We have only one failed audit which is related to HTTPS redirect. We need to host the application and .</p>

<p>Let’s now run the audits against a hosted and secured .</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6e619b7b-acaf-4699-ac1f-354d23e992f8/pwa-final-report.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6e619b7b-acaf-4699-ac1f-354d23e992f8/pwa-final-report.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6e619b7b-acaf-4699-ac1f-354d23e992f8/pwa-final-report.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6e619b7b-acaf-4699-ac1f-354d23e992f8/pwa-final-report.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6e619b7b-acaf-4699-ac1f-354d23e992f8/pwa-final-report.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6e619b7b-acaf-4699-ac1f-354d23e992f8/pwa-final-report.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6e619b7b-acaf-4699-ac1f-354d23e992f8/pwa-final-report.png"
			sizes="100vw"
			alt="PWA Final Report"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			PWA Final Report. ()
		</figcaption>
	
</figure>


<p>We get a score of <em><sup>100</sup>&frasl;<sub>100</sub></em> which means we’ve successfully implemented all core tenets of PWAs.</p>

<p>You can get the final code of this demo PWA from this .</p>

<h3 id="conclusion">Conclusion</h3>

<p>In this tutorial, we’ve built a simple Angular application and have turned it into a PWA using Angular CLI. We used Google’s Lighthouse to audit our application for PWA features and explained various core tenets of PWAs such as <strong>Service Workers</strong> for adding offline support and push notifications. The <strong>Web Manifest</strong> file for enabling add-to-home-screen and splash screen features, <strong>Progressive Enhancement</strong> as well as <strong>HTTPS</strong> .</p>

<p>You may also need to manually check for other items highlighted (under the “Additional items to manually check” section) but not automatically checked by Lighthouse. These checks are required by the baseline  which is important for the purpose of shareability on social media.</p>

<p>Since PWAs are also about other aspects such as better perceived performance and accessibility, you can also use Lighthouse for auditing your PWA (or any general website) for these aspects and improve it as needed.</p>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(rb, ra, yk, il)</span>
</div>


              </article>
            </body>
          </html>
---------------
<h1 id="#title_6" >7、性能比CPU高40倍！英伟达发布推理专用GPU Tesla T4</h1>
The Next Platform
[http://www.infoq.com/cn/news/2018/09/nvidia-turinggpu-teslaT4?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/09/nvidia-turinggpu-teslaT4?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>在刚刚结束的日本GTC大会上，英伟达终于发布了推理专用GPU Tesla T4加速器。Tesla T4基于“图灵”GPU架构，该架构于今年夏天早些时候推出，用于GeForce RTX和Quadro RTX卡，可通过机器学习算法增强动态射线跟踪。Tesla T4上的芯片包含了2560个CUDA内核，具有32位单精度和16位半精度浮点数学单元（FP32和FP16）以及8位和4位整数数学单元（INT8和INT4）。性能达到了单精度8.1teraflops，而使用新的INT8八位整数格式可达到130teraops，相比上一代P4效率得到了很大的提升。</p> <i>By The Next Platform</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_7" >8、eBay把平台更新为Kubernetes、Envoy和Kafka：计划开源硬件和软件</h1>
Daniel Bryant
[http://www.infoq.com/cn/news/2018/09/ebay-replatform-open-source?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/09/ebay-replatform-open-source?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>eBay已经探讨了如何对整个技术栈执行平台更新，包括把硬件和软件都作为开源项目构建和开源。借助像Kubernetes、Envoy、MongoDB、Docker和Apache Kafka这样的云原生技术，开源推动了eBay基础设施软件的转型。</p> <i>By Daniel Bryant</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_8" >9、Eric Evans说DDD还未结束</h1>
Thomas Betts
[http://www.infoq.com/cn/news/2018/09/ddd-not-done?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/09/ddd-not-done?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>在Explore DDD 2018大会上，Eric Evans做了“怀疑、乐观和实用主义”的主题演讲，他在演讲中表示，“DDD还没有结束”。他还表示，要保持DDD不断发展，还有很多工作要做。</p> <i>By Thomas Betts</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_9" >10、区块链在健康保险行业的落地探索</h1>
徐川
[http://www.infoq.com/cn/news/2018/09/blockchain-in-health-insurance?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/09/blockchain-in-health-insurance?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>截止到2018年9月，区块链技术的落地应用主要以联盟链为主。各大互联网公司和传统企业都在联盟链方面进行了探索，在刚刚过去的万向区块链全球峰会上，民生保险健康险事业部总经理、万向区块链分布式商业创新咨询合伙人程羽分享了民生健康在区块链落地上的探索。</p> <i>By 徐川</i>
---------------
<h1 id="#title_10" >11、人工智能加“医真云”，每年让5700万人告别误诊</h1>
Sharon
[http://www.infoq.com/cn/news/2018/09/AI-in-medical-image-analysis?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/09/AI-in-medical-image-analysis?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>西安盈谷的三记组合拳，让人工智能走进医院。</p> <i>By Sharon</i>
---------------