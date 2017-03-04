## 文章索引
1、 <a href="#1node-76默认支持async/await" >Node 7.6默认支持Async/Await</a><br/>
2、 <a href="#2技术的热门度曲线" >技术的热门度曲线</a><br/>
3、 <a href="#3辅助visual-studio-2017部署的devops新工具" >辅助Visual Studio 2017部署的DevOps新工具</a><br/>
4、 <a href="#4shopify的闪购限流解决方案" >Shopify的闪购限流解决方案</a><br/>
5、 <a href="#5视频演讲-携程的推荐及智能化算法及架构体系实践" >视频演讲： 携程的推荐及智能化算法及架构体系实践</a><br/>
6、 <a href="#6inspiring-illustrations-with-plenty-of-bright-colors-and-cool-patterns" >Inspiring Illustrations With Plenty Of Bright Colors And Cool Patterns</a><br/>
7、 <a href="#7web-development-reading-list-#172:-on-reporting-bugs-dns-subdomain-takeovers-and-sustainable-ux" >Web Development Reading List #172: On Reporting Bugs, DNS Subdomain Takeovers, And Sustainable UX</a><br/><h1 id="#title_0" >1、Node 7.6默认支持Async/Await</h1>
Sergio De Simone
[http://www.infoq.com/cn/news/2017/03/node-76-async-await?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/03/node-76-async-await?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Node.js 7.6正式默认支持async/await功能，并能够使低内存设备获得更出色的性能。</p> <i>By Sergio De Simone</i> <i> Translated by 谢旭</i>
---------------
<h1 id="#title_1" >2、技术的热门度曲线</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2017/03/gartner-hype-cycle.html](http://www.ruanyifeng.com/blog/2017/03/gartner-hype-cycle.html)
<p>全球最大的 IT 咨询公司模型（Gartner Hype Cycle）。</p>

        <p>该模型认为，一门技术的发展要经历五个阶段。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017030301.png" alt="" title="" /></p>

<blockquote>
  <p><strong>（1）启动期（Innovation Trigger）</strong></p>

<p>该技术刚刚诞生，还只是一个概念，不具有可用性，无法评估商业潜力。媒体有所报道，引起了外界的兴趣。</p>

<p><strong>（2）泡沫期（Peak of Inflated Expectations）</strong></p>

<p>该技术逐步成型，出现了个别成功的案例，一些激进的公司开始跟进。媒体开始大肆报导，伴有各种非理性的渲染，产品的知名度达到高峰。</p>

<p><strong>（3）低谷期（Trough of Disillusionment）</strong></p>

<p>该技术的局限和缺点逐步暴露，对它的兴趣开始减弱。基于它的产品，大部分被市场淘汰或者失败，只有那些找到早期用户的公司艰难地活了下来。媒体对它的报道逐步冷却，前景不明。</p>

<p><strong>（4）爬升期（Slope of Enlightenment）</strong></p>

<p>该技术的优缺点越来越明显，细节逐渐清晰，越来越多的人开始理解它。基于它的第二代和第三代产品出现，更多的企业开始尝试，可复制的成功使用模式出现。媒体重新认识它，业界这一次给予了高度的理性的关注。</p>

<p><strong>（5）高原期（Plateau of Productivity）</strong></p>

<p>经过不断发展，该技术慢慢成为了主流。技术标准得到了清晰定义，使用起来越发方便好用，市场占有率越来越高，进入稳定应用阶段。配合它的工具和最佳实践，经过数代的演进，也变得非常成熟了。业界对它有了公认的一致的评价。</p>
</blockquote>

<p>该模型的细节可以查看维基百科的。</p>

<p>高德纳公司每年都会公布，当年的热门技术图。下面就是去年七月的图。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017030302.png" alt="" title="" /></p>

<p>上图中，4D打印处于"启动期"，区块链处于"泡沫期"，增强现实处于"低谷期"，虚拟现实处于爬升期。</p>

<p>本周，有人进行数据分析后，建立了一个名叫  的网站，提供各种技术的热门程度图。</p>

<p>下图是编程语言。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017030303.png" alt="" title="" /></p>

<p>上图中，Rust 语言处于启动期，Go 语言处于泡沫期，Ruby 语言处于低谷期，Object-C 处于爬升期，PHP 和 Java 处于高原期。</p>

<p>下图是 Web 技术。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017030305.png" alt="" title="" /></p>

<p>上图中，WebAssembly 处于启动期，WebRTC 处于低谷期，HTTPS 处于高原期。</p>

<p>一门技术到底前景如何，很难预测，但是它的热门程度却是可以衡量的（比如在社交媒体提及次数的增长幅度）。风险投资跟热门程度高度正相关，越热门的技术越容易拿到投资。</p>

<p>用户可以采用这张图，判断技术处在哪一个阶段，确定它的热门程度。简单的使用规则如下。</p>

<blockquote>
  <p>"<strong>争取风险投资，要选择热门的技术；解决实际问题， 要选择可靠的技术。</strong>"</p>
</blockquote>

<p>简单说，处于启动期的技术，风险很大，不确定性极高，但是一旦成功，回报可能也很高，适合创业公司；处于高原期的技术，非常可靠，风险低，有成熟的解决方案和配套工具，适合大公司和企业的内部应用。</p>

<p>反过来说，如果一门技术处于高原期了，就代表它非常成熟了，人们对它能干什么和不能干什么，都已经很了解了，也没有新的期待了，技术本身的潜力已经不大了，所以用它拿不到投资，只能用来干活。</p>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2017-03-03T15:07:05+08:00">2017年3月 3日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>博客文集：</li>
<li>社交媒体：</li>
<li>Feed订阅： </li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------
<h1 id="#title_2" >3、辅助Visual Studio 2017部署的DevOps新工具</h1>
Jeff Martin
[http://www.infoq.com/cn/news/2017/03/vs2017-devops?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/03/vs2017-devops?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p> Visual Studio 2017对安装程序做了改进，这意味着在确定构建环境时不能再使用查询系统注册表的传统方法。新发布的新API、PowerShell模块和独立工具集为开发人员和构建工程师提供了更好的自动化构建环境工具。</p> <i>By Jeff Martin</i> <i> Translated by Rays</i>
---------------
<h1 id="#title_3" >4、Shopify的闪购限流解决方案</h1>
薛命灯
[http://www.infoq.com/cn/news/2017/03/Shopify-solve-idea?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/03/Shopify-solve-idea?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Shopify是加拿大著名的电子商务软件解决方案提供商，来自Shopify性能工程团队的Emil Stolarsky分享了Shopify的闪购限流解决方案。</p> <i>By  薛命灯</i>
---------------
<h1 id="#title_4" >5、视频演讲： 携程的推荐及智能化算法及架构体系实践</h1>
于磊
[http://www.infoq.com/cn/presentations/ctrip-recommended-and-intelligent-algorithms-and-architecture-system-practice?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/ctrip-recommended-and-intelligent-algorithms-and-architecture-system-practice?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/ctrip-recommended-and-intelligent-algorithms-and-architecture-system-practice/zh/mediumimage/yulei270.jpg"/><p>区别于一般电商公司，OTA(Online Travel Agent)公司的业务线繁多，各业务线的线上流程、商品数据、用户行为、用户需求和订单逻辑差异性极大，不同业务线，近似于完全不同的行业。但是同一般大型电商公司一样，OTA 的大数据营销平台也同时面对着公司跨繁多业务线的个性化推荐、进阶销售（up-selling）和交叉销售（cross-selling）的业务诉求。本次分享将介绍携程通用实时个性化推荐架构和算法体系设计方面的最新进展。</p> <i>By 于磊</i>
---------------
<h1 id="#title_5" >6、Inspiring Illustrations With Plenty Of Bright Colors And Cool Patterns</h1>
Veerle Pieters
[https://www.smashingmagazine.com/2017/03/inspiring-illustrations-bright-colors-cool-patterns/](https://www.smashingmagazine.com/2017/03/inspiring-illustrations-bright-colors-cool-patterns/)
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
</table><p>It's almost time to leave winter behind us here in the Northern Hemisphere. Most of the time, the weather can't quite make up its mind, and so the days pass by with half of the sky sunny while the other half gray. Nature usually tends to have a strong impact on my mood, and so these days I feel like I'm literally in a gray zone — between winter and spring.</p>

<figure></figure>

<p>I'm not sure about you, but with springtime lurking around the corner, my need for extra inspiration is even bigger. So, I hope that this month's set will give you just that spark you need to cheer you up and boost your creativity.</p>

<p>The post .</p>
---------------
<h1 id="#title_6" >7、Web Development Reading List #172: On Reporting Bugs, DNS Subdomain Takeovers, And Sustainable UX</h1>
Anselm Hannemann
[https://www.smashingmagazine.com/2017/03/web-development-reading-list-172/](https://www.smashingmagazine.com/2017/03/web-development-reading-list-172/)
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
</table><p>As web developers, we all approach our work very differently. And even when you take a look at yourself, you’ll notice that <strong>the way you do your work does vary all the time</strong>. I, for example, have not reported a single bug to a browser vendor in the past year, despite having stumbled over a couple. I was just too lazy to write them up, report them, write a test case and care about follow-up comments.</p>
<figure></figure>
<p>This week, however, when integrating the Internationalization API for dates and times, I noticed a couple of inconsistencies and specification violations in several browsers, and I reported them. It took me one hour, but now browser vendors can at least fix these bugs. Today, I filed two new issues, because I’ve become more aware again of things that work in one browser but not in others. I think it’s important to change the way we work from time to time. It’s as easy as caring more about the issues we face and reporting them back.</p><p>The post .</p>
---------------