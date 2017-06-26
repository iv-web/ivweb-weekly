## 文章索引
1、 <a href="#1如何验证-email-地址smtp-协议入门教程" >如何验证 Email 地址：SMTP 协议入门教程</a><br/>
2、 <a href="#2文章-从容器到运维一篇文章看懂技术的变革与未来" >文章： 从容器到运维，一篇文章看懂技术的变革与未来</a><br/>
3、 <a href="#3文章-谈服务发现的背景架构以及落地方案" >文章： 谈服务发现的背景、架构以及落地方案</a><br/>
4、 <a href="#4视频访谈-冯忠旗以用户和业务角度去考虑技术层面的问题才能做好产品" >视频访谈： 冯忠旗：以用户和业务角度去考虑技术层面的问题才能做好产品</a><br/><h1 id="#title_0" >1、如何验证 Email 地址：SMTP 协议入门教程</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2017/06/smtp-protocol.html](http://www.ruanyifeng.com/blog/2017/06/smtp-protocol.html)
<p>Email 是最常用的用户识别手段。</p>

        <p>开发者常常需要验证邮箱的真实性。一般的方法是，注册时向该邮箱发出一封验证邮件，要求用户点击邮件里面的链接。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017062501.png" alt="" title="" /></p>

<p>但是很多时候（比如要搞邮件营销时），拿到的是成千上万现成的 Email 地址，不可能通过回复确认真实性，这时该怎么办呢？</p>

<p>答案就是使用 。本文将介绍如何通过该协议验证邮箱的真假。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017062502.jpg" alt="" title="" /></p>

<p>另外，结尾处还有一则移动端 H5 开发的，欢迎关注。</p>

<h2>一、SMTP 协议简介</h2>

<p>SMTP 是"简单邮件传输协议"（Simple Mail Transfer Protocol）的缩写，基于 TCP 协议，用来发送电子邮件。</p>

<p>只要运行了该协议的服务器端（daemon），当前服务器就变为邮件服务器，可以接收电子邮件。</p>

<p>验证 Email 邮箱的基本思路如下。</p>

<blockquote>
  <ol start='1'>
<li>找到邮箱所在域名的 SMTP 服务器</li>
<li>连接该服务器</li>
<li>询问有没有该邮箱</li>
<li>如果服务器返回 250  或 251 状态码，邮箱就是真的；如果返回 5xx（500～599），就是假的。</li>
</ol>
</blockquote>

<p>注意，即使服务器确认邮箱是真的， 也不代表邮件一定会发送到该邮箱，更不代表用户一定会读到该邮件。</p>

<h2>二、查找域名的 MX 记录</h2>

<p>下面通过一个例子，演示如何验证<code>test@gmail.com</code>这个邮箱。</p>

<p>首先，需要查找<code>gmail.com</code> 的 MX 记录。它指向真正处理邮件的那台服务器。</p>

<blockquote><pre><code class="language-bash">
$ nslookup
> 
</code></pre></blockquote>

<p>输入<code>nslookup</code>命令后，会提示一个大于号，表示等待用户进一步输入。</p>

<blockquote><pre><code class="language-bash">
> set q=mx
> gmail.com
</code></pre></blockquote>

<p>上面代码中，<code>set q=mx</code>设定查询的是 MX 记录，第二行输入要查找的域名，结果返回了5条 MX 记录。</p>

<blockquote><pre><code class="language-bash">
Server:     192.168.1.1
Address:    192.168.1.1#53

Non-authoritative answer:
gmail.com   mail exchanger = 20 alt2.gmail-smtp-in.l.google.com.
gmail.com   mail exchanger = 30 alt3.gmail-smtp-in.l.google.com.
gmail.com   mail exchanger = 10 alt1.gmail-smtp-in.l.google.com.
gmail.com   mail exchanger = 5 gmail-smtp-in.l.google.com.
gmail.com   mail exchanger = 40 alt4.gmail-smtp-in.l.google.com.
</code></pre></blockquote>

<p><code>gmail.com</code>是很大的邮件服务商，所以会有多条记录，一般的域名只有一条。如果这一步查不到 MX 记录，该邮箱肯定是假的。</p>

<p>除了自己执行<code>nslookup</code>，也可以使用线上服务（。</p>

<h2>三、建立 TCP 连接</h2>

<p>知道了邮件服务器的地址，就可以与它建立  连接了。SMTP 协议的默认端口是25。使用 Telnet 或 Netcat 命令，都可以连接该端口。</p>

<blockquote><pre><code class="language-bash">
$ telent gmail-smtp-in.l.google.com 25
# 或者
$ nc gmail-smtp-in.l.google.com 25
</code></pre></blockquote>

<p>服务器返回<code>220</code>状态码，就表示连接成功。</p>

<blockquote><pre><code class="language-bash">
220 mx.google.com ESMTP f14si7006176pln.607 - gsmtp
</code></pre></blockquote>

<p>接下来，就可以使用 SMTP 协议的各种命令与邮件服务器交互了。</p>

<h2>四、HELO 命令和 EHLO 命令</h2>

<p>SMTP 协议规定，连接成功后，必须向邮件服务器提供连接的域名，也就是邮件将从哪台服务器发来。</p>

<p>假定从<code>mail@example.com</code>向<code>test@gmail.com</code>发送邮件，这里要提供的域名就是<code>example.com</code>。</p>

<blockquote><pre><code class="language-bash">
HELO exampl.com
</code></pre></blockquote>

<p>邮件服务器返回状态码<code>250</code>，表示响应成功。</p>

<blockquote><pre><code class="language-bash">
250 mx.google.com at your service
</code></pre></blockquote>

<p>不过，<code>HELO</code>命令现在比较少用，一般都使用<code>EHLO</code>命令。</p>

<blockquote><pre><code class="language-bash">
EHLO example.com
</code></pre></blockquote>

<p>邮件服务器收到<code>EHLO</code>命令以后，不仅会返回<code>250</code>状态码，还会返回自己支持的各种扩展的列表。</p>

<blockquote><pre><code class="language-bash">
250-mx.google.com at your service, [114.84.160.153]
250-SIZE 157286400
250-8BITMIME
250-STARTTLS
250-ENHANCEDSTATUSCODES
250-PIPELINING
250-CHUNKING
250 SMTPUTF8
</code></pre></blockquote>

<h2>五、MAIL FROM 命令</h2>

<p>然后，连接者要使用<code>MAIL FROM</code>命令，向邮件服务器提供邮件的来源邮箱。</p>

<blockquote><pre><code class="language-bash">
MAIL FROM:&lt;mail@example.com>
</code></pre></blockquote>

<p>上面代码表示，连接者将从<code>mail@example.com</code>向邮件服务器发送邮件。邮件服务器返回<code>250</code>状态码，表示响应成功。</p>

<blockquote><pre><code class="language-bash">
250 2.1.0 OK h10si3194349otb.59 - gsmtp
</code></pre></blockquote>

<p>SMTP 是一个很简单的协议，本身没有规定如何验证邮件的来源，也就是说，不验证邮件是否真的从<code>mail@example.com</code>发来，所以导致了后来垃圾邮件泛滥。为了控制垃圾邮件，许多邮件服务器会用自己的方法验证邮件地址，下面就是其中的一些方法。</p>

<blockquote>
  <ul>
<li>example.com 是否有 MX 记录</li>
<li>example.com 是否可以 Ping 通</li>
<li>是否存在 postmaster@example.com 这个邮箱</li>
<li>发起连接的 IP 地址是否在黑名单之中</li>
<li>IP 地址的反向 DNS 解析，是否指向一个邮件服务器</li>
</ul>
</blockquote>

<h2>六、RCPT TO 命令</h2>

<p>最后一步就是使用<code>RCPT TO</code>命令，验证邮件地址是否存在。</p>

<blockquote><pre><code class="language-bash">
RCPT TO:&lt;test@gmail.com>
</code></pre></blockquote>

<p>邮件服务器返回了<code>550</code>状态码，表示该 Email 地址不存在。</p>

<blockquote><pre><code class="language-bash">
550-5.1.1 The email account that you tried to reach does not exist. Please try
550-5.1.1 double-checking the recipient's email address for typos or
550-5.1.1 unnecessary spaces. Learn more at
550 5.1.1  https://support.google.com/mail/?p=NoSuchUser p34si3372771otp.228 - gsmtp
</code></pre></blockquote>

<p>如果查询的是一个真实的 Email 地址，邮件服务器就会返回<code>250</code>状态码。</p>

<blockquote><pre><code class="language-bash">
RCPT TO:&lt;yifeng.ruan@gmail.com>
250 2.1.5 OK p34si3372771otp.228 - gsmtp
</code></pre></blockquote>

<p>一般来说，状态码 250 和 251 都表示邮箱存在，状态码 5xx 表示不存在，其他状态码（主要是 4xx）则代表无法确认。</p>

<blockquote><pre><code class="language-bash">
RCPT TO:&lt;xxx@censored.pl>
451 Temporary local problem - please try later
</code></pre></blockquote>

<p>验证完成后，使用<code>QUIT</code>命令关闭 TCP 连接。</p>

<blockquote><pre><code class="language-bash">
QUIT
221 2.0.0 closing connection p34si3372771otp.228 - gsmtp
</code></pre></blockquote>

<h2>七、参考链接</h2>

<ul>
<li></li>
<li></li>
</ul>

<p>（正文完）</p>

<p>==============================</p>

<p></p>

<p>下面是推广时间。移动端开发的市场广，就业潜力大，现在有一门移动端 H5 开发的课程推荐给大家。</p>

<p>大型公开课，介绍 H5 开发，为期三周。</p>

<p>该课程将带领您一步一步学习移动端页面的开发，手把手教你做出下面的页面。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017062503.png" alt="" title="" /><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017062504.png" alt="" title="" /></p>

<p>完整的课程大纲请参考。</p>

<p>除了技术课程，还会有一次《前端开发流程、求职、职场》的公开课，由海棠学院创始人张小河主讲，帮助你了解前端工程师的就业市场和职业规划。</p>

<blockquote>
  <ul>
<li>前端新手如何进入喜欢的公司？</li>
<li>公司真实的开发流程是怎么样的？</li>
<li>为什么看了 100G 的视频/资料，你也没有学好？</li>
<li>如何成为高年薪的前端工程师？</li>
</ul>
</blockquote>

<p>这堂公开课是免费的，点击了解详情。</p>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2017-06-25T22:08:13+08:00">2017年6月25日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>博客文集：</li>
<li>社交媒体：</li>
<li>Feed订阅： </li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------
<h1 id="#title_1" >2、文章： 从容器到运维，一篇文章看懂技术的变革与未来</h1>
张磊
[http://www.infoq.com/cn/articles/an-article-to-understand-technological-change-and-future?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/an-article-to-understand-technological-change-and-future?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/an-article-to-understand-technological-change-and-future/zh/smallimage/logo11.jpg"/><p>运维，这个传统的技术工种，在容器技术、人工智能的强力加持下，已经从”机械劳动“这样的刻板印象中蜕变出来，成为了任何一家技术公司所必须依赖和大力投入的核心技术能力。</p> <i>By 张磊</i>
---------------
<h1 id="#title_2" >3、文章： 谈服务发现的背景、架构以及落地方案</h1>
宋潇男
[http://www.infoq.com/cn/articles/background-architecture-and-solutions-of-service-discovery?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/background-architecture-and-solutions-of-service-discovery?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/background-architecture-and-solutions-of-service-discovery/zh/smallimage/logo-1 (2).jpg"/><p>在开始之前，我们先来回顾下业内对于微服务架构的定义。简单来说，微服务就是用一组小服务的方式来构建一个应用，服务独立运行在不同的进程中，服务之间通过轻量的通讯机制（如RESTful接口）来交互，并且服务可以通过自动化部署方式独立部署。</p> <i>By 宋潇男</i>
---------------
<h1 id="#title_3" >4、视频访谈： 冯忠旗：以用户和业务角度去考虑技术层面的问题才能做好产品</h1>
冯忠旗
[http://www.infoq.com/cn/interviews/interview-with-fengzhongqi-talk-how-to-take-good-product?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/interviews/interview-with-fengzhongqi-talk-how-to-take-good-product?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/interviews/interview-with-fengzhongqi-talk-how-to-take-good-product/zh/mediumimage/fengzhongqi270.jpg"/><p>付钱拉的冯忠旗老师分享了付钱拉针对金融云行业的痛点在系统架构方面做的设计和实战经验，介绍了他们在改进用户的使用体验方面采取的一些措施以及他们在使用开源项目方面的一些经验，希望给大家带来帮助。</p> <i>By 冯忠旗</i>
---------------