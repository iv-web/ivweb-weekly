## 文章索引
1、 <a href="#1web-development-reading-list-#185:-safari-11-new-edge-build-chrome-59-and-css-optimization-insights" >Web Development Reading List #185: Safari 11, New Edge Build, Chrome 59, And CSS Optimization Insights</a><br/>
2、 <a href="#2tcp-协议简介" >TCP 协议简介</a><br/>
3、 <a href="#3#338:-a-comparison-between-adopting-flow-or-typescript" >#338: A Comparison Between Adopting Flow or TypeScript</a><br/>
4、 <a href="#4when-large-isnt-large-enough:-designing-with-hero-images" >When Large Isn’t Large Enough: Designing With Hero Images</a><br/><h1 id="#title_0" >1、Web Development Reading List #185: Safari 11, New Edge Build, Chrome 59, And CSS Optimization Insights</h1>
Anselm Hannemann
[https://www.smashingmagazine.com/2017/06/web-development-reading-list-185/](https://www.smashingmagazine.com/2017/06/web-development-reading-list-185/)
<table width="650">
	<tr>
		<td width="650">
			<div style="width:650px;">
				<img src="http://statisches.auslieferung.commindo-media-ressourcen.de/advertisement.gif" alt="" border="0"/>
				<br/>
				<a href="http://auslieferung.commindo-media-ressourcen.de/random.php?mode=target&collection=smashing-rss&position=1" target="_blank">
					<img src="http://auslieferung.commindo-media-ressourcen.de/random.php?mode=image&collection=smashing-rss&position=1" border="0" alt=""/>
				</a>
				&nbsp;
				<a href="http://auslieferung.commindo-media-ressourcen.de/random.php?mode=target&collection=smashing-rss&position=2" target="_blank">
					<img src="http://auslieferung.commindo-media-ressourcen.de/random.php?mode=image&collection=smashing-rss&position=2" border="0" alt=""/>
				</a>
				&nbsp;
				<a href="http://auslieferung.commindo-media-ressourcen.de/random.php?mode=target&collection=smashing-rss&position=3" target="_blank">
					<img src="http://auslieferung.commindo-media-ressourcen.de/random.php?mode=image&collection=smashing-rss&position=3" border="0" alt=""/>
				</a>
			</div>
		</td>
	</tr>
</table><p>This week was full of <strong>great browser vendor news</strong>: Safari 11 was announced with long-awaited features such as WebRTC and tracking protection, and a new Edge build with new CSS features is now available, too.</p>
<figure></figure>
<p>But the past few days also had some valuable articles up their sleeves: about implementing HTTP/2 push, using <code>datetime-local</code>, and slimming down your CSS, for example. I collected everything in this reading list for you, so you don’t miss out on anything. Enjoy!</p><p>The post .</p>
---------------
<h1 id="#title_1" >2、TCP 协议简介</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2017/06/tcp-protocol.html](http://www.ruanyifeng.com/blog/2017/06/tcp-protocol.html)
<p>TCP 是互联网核心协议之一，本文介绍它的基础知识。</p>

        <p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017060801.png" alt="" title="" /></p>

<h2>一、TCP 协议的作用</h2>

<p>互联网由构成。TCP 只是其中的一层，有着自己的分工。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017060804.png" alt="" title="" /></p>

<p>（图片说明：TCP 是以太网协议和 IP 协议的上层协议，也是应用层协议的下层协议。）</p>

<p>最底层的以太网协议（Ethernet）规定了电子信号如何组成数据包（packet），解决了子网内部的点对点通信。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017060802.jpg" alt="" title="" /></p>

<p>（图片说明：以太网协议解决了局域网的点对点通信。）</p>

<p>但是，以太网协议不能解决多个局域网如何互通，这由 IP 协议解决。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017060803.png" alt="" title="" /></p>

<p>（图片说明：IP 协议可以连接多个局域网。）</p>

<p>IP 协议定义了一套自己的地址规则，称为 IP 地址。它实现了路由功能，允许某个局域网的 A 主机，向另一个局域网的 B 主机发送消息。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017060805.jpg" alt="" title="" /></p>

<p>（图片说明：路由器就是基于 IP 协议。局域网之间要靠路由器连接。）</p>

<p>路由的原理很简单。市场上所有的路由器，背后都有很多网口，要接入多根网线。路由器内部有一张路由表，规定了 A 段 IP 地址走出口一，B 段地址走出口二，......通过这套"指路牌"，实现了数据包的转发。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017060806.jpg" alt="" title="" /></p>

<p>（图片说明：本机的路由表注明了不同 IP 目的地的数据包，要发送到哪一个网口（interface）。）</p>

<p>IP 协议只是一个地址协议，并不保证数据包的完整。如果路由器丢包（比如缓存满了，新进来的数据包就会丢失），就需要发现丢了哪一个包，以及如何重新发送这个包。这就要依靠 TCP 协议。</p>

<p>简单说，TCP 协议的作用是，保证数据通信的完整性和可靠性，防止丢包。</p>

<h2>二、TCP 数据包的大小</h2>

<p>以太网数据包（packet）的大小是固定的，最初是1518字节，后来增加到1522字节。其中， 1500 字节是负载（payload），22字节是头信息（head）。</p>

<p>IP 数据包在以太网数据包的负载里面，它也有自己的头信息，最少需要20字节，所以 IP 数据包的负载最多为1480字节。</p>

<p><img src="http://image.beekka.com/blog/201205/bg2012052913.png" alt="" title="" /></p>

<p>（图片说明：IP 数据包在以太网数据包里面，TCP 数据包在 IP 数据包里面。）</p>

<p>TCP 数据包在 IP 数据包的负载里面。它的头信息最少也需要20字节，因此 TCP 数据包的最大负载是 1480 - 20 = 1460 字节。由于 IP 和 TCP 协议往往有额外的头信息，所以 TCP 负载实际为1400字节左右。</p>

<p>因此，一条1500字节的信息需要两个 TCP 数据包。HTTP/2 协议的一大改进， 就是压缩 HTTP 协议的头信息，使得一个 HTTP 请求可以放在一个 TCP 数据包里面，而不是分成多个，这样就提高了速度。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg20170060810.png" alt="" title="" /></p>

<p>（图片说明：以太网数据包的负载是1500字节，TCP 数据包的负载在1400字节左右。）</p>

<h2>三、TCP 数据包的编号（SEQ）</h2>

<p>一个包1400字节，那么一次性发送大量数据，就必须分成多个包。比如，一个 10MB 的文件，需要发送7100多个包。</p>

<p>发送的时候，TCP 协议为每个包编号（sequence number，简称 SEQ），以便接收的一方按照顺序还原。万一发生丢包，也可以知道丢失的是哪一个包。</p>

<p>第一个包的编号是一个随机数。为了便于理解，这里就把它称为1号包。假定这个包的负载长度是100字节，那么可以推算出下一个包的编号应该是101。这就是说，每个数据包都可以得到两个编号：自身的编号，以及下一个包的编号。接收方由此知道，应该按照什么顺序将它们还原成原始文件。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017060807.png" alt="" title="" /></p>

<p>（图片说明：当前包的编号是45943，下一个数据包的编号是46183，由此可知，这个包的负载是240字节。）</p>

<h2>四、TCP 数据包的组装</h2>

<p>收到 TCP 数据包以后，组装还原是操作系统完成的。应用程序不会直接处理 TCP 数据包。</p>

<p>对于应用程序来说，不用关心数据通信的细节。除非线路异常，收到的总是完整的数据。应用程序需要的数据放在 TCP 数据包里面，有自己的格式（比如 HTTP 协议）。</p>

<p>TCP 并没有提供任何机制，表示原始文件的大小，这由应用层的协议来规定。比如，HTTP 协议就有一个头信息<code>Content-Length</code>，表示信息体的大小。对于操作系统来说，就是持续地接收 TCP 数据包，将它们按照顺序组装好，一个包都不少。</p>

<p>操作系统不会去处理 TCP 数据包里面的数据。一旦组装好 TCP 数据包，就把它们转交给应用程序。TCP 数据包里面有一个端口（port）参数，就是用来指定转交给监听该端口的应用程序。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017060808.jpg" alt="" title="" /></p>

<p>（图片说明：系统根据 TCP 数据包里面的端口，将组装好的数据转交给相应的应用程序。上图中，21端口是 FTP 服务器，25端口是 SMTP 服务，80端口是 Web 服务器。）</p>

<p>应用程序收到组装好的原始数据，以浏览器为例，就会根据 HTTP 协议的<code>Content-Length</code>字段正确读出一段段的数据。这也意味着，一次 TCP 通信可以包括多个 HTTP 通信。</p>

<h2>五、慢启动和 ACK</h2>

<p>服务器发送数据包，当然越快越好，最好一次性全发出去。但是，发得太快，就有可能丢包。带宽小、路由器过热、缓存溢出等许多因素都会导致丢包。线路不好的话，发得越快，丢得越多。</p>

<p>最理想的状态是，在线路允许的情况下，达到最高速率。但是我们怎么知道，对方线路的理想速率是多少呢？答案就是慢慢试。</p>

<p>TCP 协议为了做到效率与可靠性的统一，设计了一个慢启动（slow start）机制。开始的时候，发送得较慢，然后根据丢包的情况，调整速率：如果不丢包，就加快发送速度；如果丢包，就降低发送速度。</p>

<p>Linux 内核里面了（常量<code>TCP_INIT_CWND</code>），刚开始通信的时候，发送方一次性发送10个数据包，即"发送窗口"的大小为10。然后停下来，等待接收方的确认，再继续发送。</p>

<p>默认情况下，接收方每收到一个确认消息。"确认"的英语是 acknowledgement，所以这个确认消息就简称 ACK。</p>

<p>ACK 携带两个信息。</p>

<blockquote>
  <ul>
<li>期待要收到下一个数据包的编号</li>
<li>接收方的接收窗口的剩余容量</li>
</ul>
</blockquote>

<p>发送方有了这两个信息，再加上自己已经发出的数据包的最新编号，就会推测出接收方大概的接收速度，从而降低或增加发送速率。这被称为"发送窗口"，这个窗口的大小是可变的。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017060809.png" alt="" title="" /></p>

<p>（图片说明：每个 ACK 都带有下一个数据包的编号，以及接收窗口的剩余容量。双方都会发送 ACK。）</p>

<p>注意，由于 TCP 通信是双向的，所以双方都需要发送 ACK。两方的窗口大小，很可能是不一样的。而且 ACK 只是很简单的几个字段，通常与数据合并在一个数据包里面发送。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017060812.jpg" alt="" title="" /></p>

<p>（图片说明：上图一共4次通信。第一次通信，A 主机发给B 主机的数据包编号是1，长度是100字节，因此第二次通信 B 主机的 ACK 编号是 1 + 100 = 101，第三次通信 A 主机的数据包编号也是 101。同理，第二次通信 B 主机发给 A 主机的数据包编号是1，长度是200字节，因此第三次通信 A 主机的 ACK 是201，第四次通信 B 主机的数据包编号也是201。）</p>

<p>即使对于带宽很大、线路很好的连接，TCP 也总是从10个数据包开始慢慢试，过了一段时间以后，才达到最高的传输速率。这就是 TCP 的慢启动。</p>

<h2>六、数据包的遗失处理</h2>

<p>TCP 协议可以保证数据通信的完整性，这是怎么做到的？</p>

<p>前面说过，每一个数据包都带有下一个数据包的编号。如果下一个数据包没有收到，那么 ACK 的编号就不会发生变化。</p>

<p>举例来说，现在收到了4号包，但是没有收到5号包。ACK 就会记录，期待收到5号包。过了一段时间，5号包收到了，那么下一轮 ACK 会更新编号。如果5号包还是没收到，但是收到了6号包或7号包，那么 ACK 里面的编号不会变化，总是显示5号包。这会导致大量重复内容的 ACK。</p>

<p>如果发送方发现收到连续的重复 ACK，或者超时了还没有收到任何 ACK，就会确认丢包，即5号包遗失了，从而再次发送这个包。通过这种机制，TCP 保证了不会有数据包丢失。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017060811.png" alt="" title="" /></p>

<p>（图片说明：Host B 没有收到100号数据包，会连续发出相同的 ACK，触发 Host A 重发100号数据包。）</p>

<h2>七、参考链接</h2>

<ul>
<li></li>
</ul>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2017-06-08T16:26:18+08:00">2017年6月 8日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>博客文集：</li>
<li>社交媒体：</li>
<li>Feed订阅： </li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------
<h1 id="#title_2" >3、#338: A Comparison Between Adopting Flow or TypeScript</h1>

[http://javascriptweekly.com/issues/338](http://javascriptweekly.com/issues/338)
<table border="0" width="100%" cellpadding="0" cellspacing="0" bgcolor="#ffffff" style="font-family: 'helvetica neue', helvetica, arial, sans-serif; font-size: 14px; line-height: 20px; color: #333"><tr><td align="center" valign="top">
<table border="0" width="600" cellpadding="0" cellspacing="0" class="container noarchive" style="border-collapse: collapse;"><tr><td style="padding-top: 6px; padding-bottom: 6px; font-size: 11px; text-align: center; color: #555; font-family: verdana, arial, sans-serif">
<span class="nomo">This week's JavaScript news</span> — 
</td></tr></table>
<table border="0" width="600" cellpadding="0" cellspacing="0" class="container" style="border-collapse: collapse">
<tr><td style="background-color: #f7df1e"><table width="100%" cellspacing="0" cellpadding="0" align="left"><tr><td align="left" class="block" style="padding: 6px 12px;">
<table align="left" width="50%" class="gowide"><tr><td><span style="line-height: 36px; font-size: 23px; color: #f7df1e; font-weight: bold; color: #323330">JavaScript Weekly</span></td></tr></table>
<table align="left" style="text-align: right" width="50%" class="gowide lonmo"><tr><td><span style="font-size: 14px; line-height: 36px; font-weight: normal; color: #323330">
Issue 338 — June  9, 2017
</span></td></tr></table>
</td></tr></table></td></tr>
<tr><td style="padding: 16px 12px 12px 12px" align="left">
<div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">Both Flow and TypeScript can bring type checking to your code. This post falls in favor of Flow, a TypeScript PM posted 
</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
James Kyle
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">Where do functions, classes, and objects fit into the big picture of writing simpler code that’s easy to maintain?</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Kent C. Dodds
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">An exercise in porting a JavaScript library to WebAssembly (wasm) - perfect for those wanting more than a Hello World introduction.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Maxime Rouyrre
</div>
<br clear="all" style="clear: both"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">Learn from Todd Gardner (Co-founder of TrackJS) on Debugging and Fixing Common JavaScript Errors. In this course, you’ll be armed to find and squash JS bugs faster, and for good. — Free until June 26.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Frontend Masters
  <span style="border: 1px solid #999; border-radius: 2px; color: #999; font-size: 11px; font-weight: normal; padding: 1px 5px 1px 5px; ">Sponsor</span>
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">
 (denoted as such: <code>this.#x</code>) are now at stage 2 in TC39’s standard process. Here’s a look at why they’re important and what they could mean for JavaScript.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
James Kyle
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">A .</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Naver Corp
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">Jurgen Van de Moere takes an existing Angular 2+ app and adds a REST API service. Learn about RxJS observables and how to mock HTTP services for testing.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
SitePoint
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">ARES-6 measures the execution time of JavaScript’s newest features. This post digs deep on it and is very much for the more technical reader.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
WebKit
</div>
<br clear="all" style="clear: both"><p style="color: #666666; font-size: 16px; font-weight: bold; margin-top: 8px; margin-bottom: 10px; text-transform: uppercase">Jobs </p>
<ul style="padding-left: 18px; margin-top: 10px; list-style-type: square">
<li style="color: #f7df1e; margin-bottom: 10px; font-size: 15px; line-height: 17px">
.</span> <span style="color: #999999; font-weight: normal; font-size: 12px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Workday</span>
</li>
<li style="color: #f7df1e; margin-bottom: 10px; font-size: 15px; line-height: 17px">
<span style="font-size: 12px; color: #666666">Join us to impact how the world's biggest retailers operate by making a web app with great UX and DX using React, Redux and Glamor</span> <span style="color: #999999; font-weight: normal; font-size: 12px; text-transform: uppercase; font-family: verdana, arial, sans-serif">EDITED</span>
</li>
<li style="color: #f7df1e; margin-bottom: 10px; font-size: 15px; line-height: 17px">
<span style="font-size: 12px; color: #666666">LIQID is seeking a JavaScript Architect. The ideal candidate will drive the architectural innovation of LIQID's web platform.</span> <span style="color: #999999; font-weight: normal; font-size: 12px; text-transform: uppercase; font-family: verdana, arial, sans-serif">LIQID Investments GmbH</span>
</li>
</ul>
<p style="color: #333; font-size: 12px; font-weight: normal; margin-top: 0px; margin-bottom: 10px">Can't find the right job? Want companies to apply to <em>you?</em> </p>
<p style="color: #666666; font-size: 16px; font-weight: bold; margin-top: 24px; margin-bottom: 10px; text-transform: uppercase">In Brief</p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">SitePoint</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">A fast, tiny alternative to React with the same ES6 API.</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Bilal Budhani</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">The latest in Eric Elliott’s popular functional programming series.</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Eric Elliott</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">A good opportunity to show, simply, how React works.</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Samer Buna</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">An introduction for absolute beginners.</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Monica Dinculescu</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px"><code>util.promisify</code> converts a callback-based function to a Promise-based one.</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Dr. Axel Rauschmayer</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Matt Hink</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">Updated for npm 5.0’s recent release.</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Michael Wanyoike and Peter Dierx</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #AF7817; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">opinion</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Hacker Noon</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #AF7817; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">opinion</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Hacker News</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #bbbbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tools</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">PubNub gets your data anywhere in &lt;0.25 seconds. It’s so easy with PubNub’s Angular library.</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">PubNub  <span style="border: 1px solid #999; border-radius: 2px; color: #999; font-size: 11px; font-weight: normal; padding: 1px 5px 1px 5px;">Sponsor</span></span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #bbbbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tools</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px"><code>npm i -g npmc</code> gets you a canary release as a separate <code>npmc</code> binary.</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">The npm Blog</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #bbbbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tools</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Brent Lintner</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #bbbbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tools</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">Connect your database to your version control system with SQL Source Control and keep track of every change.
</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Red Gate  <span style="border: 1px solid #999; border-radius: 2px; color: #999; font-size: 11px; font-weight: normal; padding: 1px 5px 1px 5px;">Sponsor</span></span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #00bbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">code</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Jon Abrams</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #00bbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">code</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Jiayi Hu</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #00bbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">code</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Vitaliy Potapov</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #00bbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">code</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Synacor</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Mongo DB  <span style="border: 1px solid #999; border-radius: 2px; color: #999; font-size: 11px; font-weight: normal; padding: 1px 5px 1px 5px;">Sponsor</span></span></p>
</td></tr>
<tr><td bgcolor="#f4f4f4" style="font-family: verdana, helvetica, arial, sans-serif; text-align: left; padding-top: 12px; padding-left: 12px; padding-right: 12px; padding-bottom: 12px" class="noarchive">
<p style="line-height: 15px; font-size: 11px; margin-top: 0">Curated by .</p>
<p style="line-height: 15px; font-size: 11px; margin-top: 0">Like this? You may also enjoy: </p>
<p style="font-size: 13px"></p>
<p style="font-size: 11px; line-height: 15px">© Cooperpress Ltd. Office 30, Lincoln Way, Louth, LN11 0LS, UK</p>
</td></tr>
</table>
</td></tr></table>
---------------
<h1 id="#title_3" >4、When Large Isn’t Large Enough: Designing With Hero Images</h1>
Nick Babich
[https://www.smashingmagazine.com/2017/06/designing-hero-images/](https://www.smashingmagazine.com/2017/06/designing-hero-images/)
<table width="650">
	<tr>
		<td width="650">
			<div style="width:650px;">
				<img src="http://statisches.auslieferung.commindo-media-ressourcen.de/advertisement.gif" alt="" border="0"/>
				<br/>
				<a href="http://auslieferung.commindo-media-ressourcen.de/random.php?mode=target&collection=smashing-rss&position=1" target="_blank">
					<img src="http://auslieferung.commindo-media-ressourcen.de/random.php?mode=image&collection=smashing-rss&position=1" border="0" alt=""/>
				</a>
				&nbsp;
				<a href="http://auslieferung.commindo-media-ressourcen.de/random.php?mode=target&collection=smashing-rss&position=2" target="_blank">
					<img src="http://auslieferung.commindo-media-ressourcen.de/random.php?mode=image&collection=smashing-rss&position=2" border="0" alt=""/>
				</a>
				&nbsp;
				<a href="http://auslieferung.commindo-media-ressourcen.de/random.php?mode=target&collection=smashing-rss&position=3" target="_blank">
					<img src="http://auslieferung.commindo-media-ressourcen.de/random.php?mode=image&collection=smashing-rss&position=3" border="0" alt=""/>
				</a>
			</div>
		</td>
	</tr>
</table><p>When users come to your page, they’ll feel some kind of reaction. Whether it’s positive or negative, that reaction is determined in large part by what they see. Because <strong>vision is perhaps the strongest human sense</strong>, a hero image is one of the fastest ways to grab the user’s attention. Bold, graphic and intentional imagery engages the user. It draws the user in immediately and makes a perfect centerpiece for a minimalist app or website.</p>

<figure></figure>

<p>A hero image is more than just a pretty picture. It’s a powerful communication tool. In this article, I’ll give you a few tips on using hero images. Also, if you’d like to get started and take a go at prototyping and wireframing your own designs a bit more differently, you can download and test <em>Adobe XD</em> for free.</p><p>The post .</p>
---------------