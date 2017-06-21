## 文章索引
1、 <a href="#1如何利用云计算为ai推力-这些专家都有自己的看法" >如何利用云计算为AI推力 这些专家都有自己的看法</a><br/>
2、 <a href="#2视频演讲-电商广告计费系统的容灾设计" >视频演讲： 电商广告计费系统的容灾设计</a><br/>
3、 <a href="#3文章-基于postgresql的内存计算引擎来自lenovo的设计开发经验" >文章： 基于PostgreSQL的内存计算引擎，来自Lenovo的设计开发经验</a><br/>
4、 <a href="#4揭秘腾讯数据中心十八年建设及运营实践" >揭秘腾讯数据中心十八年建设及运营实践</a><br/>
5、 <a href="#5专访高性能计算领军人物刘文志并行计算的未来是让人工智能无处不在" >专访高性能计算领军人物刘文志：并行计算的未来，是让人工智能无处不在</a><br/>
6、 <a href="#6如何组建开源社区" >如何组建开源社区</a><br/>
7、 <a href="#7infoq在新兴技术企业大会上对lightbend企业架构师kiki-carter的访谈" >InfoQ在新兴技术企业大会上对Lightbend企业架构师Kiki Carter的访谈</a><br/>
8、 <a href="#8文章-解决问题方法论技术人都应该学习的troubleshooting" >文章： 解决问题方法论，技术人都应该学习的troubleshooting</a><br/>
9、 <a href="#9易宝支付cto陈斌如何做一个好的cto" >易宝支付CTO陈斌：如何做一个好的CTO</a><br/>
10、 <a href="#10再谈10x程序员" >再谈10x程序员</a><br/>
11、 <a href="#11wwdc-2017-技术盘点" >WWDC 2017 技术盘点</a><br/>
12、 <a href="#12来自datadog的docker全球使用调查报告" >来自Datadog的Docker全球使用调查报告</a><br/>
13、 <a href="#13视频演讲-构建基于富媒体大数据的弹性深度学习计算平台" >视频演讲： 构建基于富媒体大数据的弹性深度学习计算平台</a><br/>
14、 <a href="#14connecting-with-users:-incorporating-humor-in-web-design" >Connecting With Users: Incorporating Humor In Web Design</a><br/>
15、 <a href="#15reaching-the-millennials:-mobile-marketing-trends-and-techniques" >Reaching The Millennials: Mobile Marketing Trends And Techniques</a><br/><h1 id="#title_0" >1、如何利用云计算为AI推力 这些专家都有自己的看法</h1>
江柳
[http://www.infoq.com/cn/news/2017/06/tengxun-Cloud-AI?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/06/tengxun-Cloud-AI?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>随着亚马逊、微软、谷歌以及腾讯、阿里等一众企业相继进入云计算市场并发布对应的产品，基础云服务的同质化愈发的明显。而人工智能在云计算领域应用的展开，让大数据、人工智能和云计算有望真正走向融合重新定义“效率”，亚马逊、微软、谷歌，包括国内的腾讯、阿里、百度都已开始在人工智能领域的探索，这个趋势也将云计算的竞争推入一个人工智能应用的新“战场”。</p> <i>By 江柳</i>
---------------
<h1 id="#title_1" >2、视频演讲： 电商广告计费系统的容灾设计</h1>
子文
[http://www.infoq.com/cn/presentations/disaster-tolerance-design-of-lectricity-supplier-advertising-billing-system?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/disaster-tolerance-design-of-lectricity-supplier-advertising-billing-system?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/disaster-tolerance-design-of-lectricity-supplier-advertising-billing-system/zh/mediumimage/ziwen270.jpg"/><p>互联网广告系统本身是一个对稳定性和可靠性要求极高的系统，每天面对数十亿级别的请求，广告投放主多样的投放方式变化与用户关注点及兴趣频繁的更新，同时对时效性要求严格，而作为电商广告的计费系统，则要求更加严格，从打点到计费任何一环节出现问题，都会带来巨大的经济损失和平台信任度危机，涉及到商家账户资金，系统实时反作弊和防刷，亿级别点击（曝光）等高效稳定账务扣费，数据的强一致性和最终一致性的保证及全链路高效可靠的监控。在蘑菇街广告计费系统的持续优化改进之路中，对整个蘑菇街广告计费系统容灾方面，积累了一些经验，本次分享主要分享电商广告计费系统的容灾设计。</p> <i>By 子文</i>
---------------
<h1 id="#title_2" >3、文章： 基于PostgreSQL的内存计算引擎，来自Lenovo的设计开发经验</h1>
联想数据库团队
[http://www.infoq.com/cn/articles/lenovo-postgresql-based-memory-computing-engine?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/lenovo-postgresql-based-memory-computing-engine?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/lenovo-postgresql-based-memory-computing-engine/zh/smallimage/logo4 (2).jpg"/><p>身处大数据时代，在数据库领域，我们要分析处理的数据越来越多，我们分析处理数据的速度也要越来越快，但是传统数据库基于磁盘的计算模型，已经难以满足我们的需求。幸运的是随着硬件的发展，内存设备的性能在不断提高，而价格却在不断下降。内存计算技术将带着我们“飞”起来！ 内存计算（In-Memory Computing），实质上是 CPU 直接从内存而非硬盘上读取数据，并对数据进行计算、分析。在数据库上引入内存计算技术，意味着去除磁盘 IO 的消耗，利用内存随机访问的特性可以制定更高效的算法等等。这都极大的提高数据的处理速度。 目前很多商业数据库已经拥有了内存计算功能，如 SAP HANA、DB2 BLU、Oracle 12C、SQL Server 2014。但是商业数据库的价格毕竟不菲，在开源产品飞速发展的今天，利用开源的内存计算产品是一个好主意。</p> <i>By 联想数据库团队</i>
---------------
<h1 id="#title_3" >4、揭秘腾讯数据中心十八年建设及运营实践</h1>
曹倩芸
[http://www.infoq.com/cn/news/2017/06/tencent-idc-operation-and-build?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/06/tencent-idc-operation-and-build?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>2000年，腾讯第一个IDC在深圳东门建立，2012年9月，第一个微模块数据中心在宝安落地。这中间，腾讯又相继建立了异地IDC、海外IDC、还包括自建数据中心和超大规模数据中心的上线和交付。十七年，腾讯在数据中心建设和运营上积累了一系列的实践经验，也在自主设计、自主建设领域已经取得了丰硕的成果。</p> <i>By 曹倩芸</i>
---------------
<h1 id="#title_4" >5、专访高性能计算领军人物刘文志：并行计算的未来，是让人工智能无处不在</h1>
杨旸
[http://www.infoq.com/cn/news/2017/06/parallel-compu-artificial-intell?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/06/parallel-compu-artificial-intell?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>大数据、算法和计算能力决定了人工智能的发展。在计算领域上，主要依靠的硬件就是GPU、CPU，以及最近刚推出的TPU，背后是英伟达、英特尔和谷歌的角力。伴随着这些公司的股价一路上涨的趋势，从此也能看出并行计算的再次崛起。InfoQ一直很关注并行计算领域，联系了业界领军人物刘文志老师，并拜托杨旸进行了一次较深入的访谈，以下是访谈实录。 刘文志（花名风辰），商汤科技高性能计算总监，毕业于中国科学院研究生院，闻名于并行计算江湖，尤善异构并行计算（X86、ARM、GPU、APU及PHI）和大规模集群计算，有7年相关经验，涉及图像处理、计算机视觉、数据挖掘和石油勘探。曾任英伟达并行计算工程师（协助建立英伟达北京CUDA团队）、百度在线高级研发工程师（协助建立百度深度学习实验室异构计算团队）。</p> <i>By 杨旸</i>
---------------
<h1 id="#title_5" >6、如何组建开源社区</h1>
Ben Linders
[http://www.infoq.com/cn/news/2017/06/build-open-source-communities?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/06/build-open-source-communities?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/news/2017/06/build-open-source-communities/zh/headerimage/GettyImages-612491256.jpg"/><p>将编程看作是一种社交活动，这将改变我们围绕编程而构建社区的方式。我们应聚焦于如何去构建一个社区，而不是如何去构建一块代码。以上是Ash Furrow在Craft大会上提出的观点。他的建议还包括：应采用一种行为准则；对持续时间长的或很激烈的讨论，应使用Skype电话或Google Hangout开展；避免亲历亲为去解决一些简单的问题；将权利和责任分发下去。</p> <i>By Ben Linders</i> <i> Translated by Rays</i>
---------------
<h1 id="#title_6" >7、InfoQ在新兴技术企业大会上对Lightbend企业架构师Kiki Carter的访谈</h1>
Michael Redlich
[http://www.infoq.com/cn/news/2017/06/kiki-carter-speaks-to-infoq?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/06/kiki-carter-speaks-to-infoq?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>InfoQ在新兴技术企业大会上对Lightbend企业架构师Kiki Carter进行了采访，Carter向我们分享了她对于微服务、响应式系统、Scala与Java的对比、以及SMACK（Spark, Mesos, Akka, Cassandra, Kafka）技术栈的观点。</p> <i>By Michael Redlich</i> <i> Translated by 马卓奇</i>
---------------
<h1 id="#title_7" >8、文章： 解决问题方法论，技术人都应该学习的troubleshooting</h1>
滕传永
[http://www.infoq.com/cn/articles/technical-people-should-learn-troubleshooting?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/technical-people-should-learn-troubleshooting?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/technical-people-should-learn-troubleshooting/zh/smallimage/budong.jpg"/><p>troubleshooting 是找到问题发生的根源并将其解决更正的过程，troubleshooting 的目标就是使设备 / 系统回到正常的工作状态。 因为很多系统，特别是 IT 系统或者一些电力系统、通讯系统，都是 7×24 小时不间断运行的。如果一旦发生故障，就要求我们运维人员很快的发现故障，然后用快速和经济的办法去把这个故障解决掉。比如医院有些支撑手术的系统，一旦故障如果不能很快解决的话，甚至会威胁到病人的生命安全。所以 troubleshooting 对我们运维人员来说是一项非常重要的技能和技术要求。</p> <i>By 滕传永</i>
---------------
<h1 id="#title_8" >9、易宝支付CTO陈斌：如何做一个好的CTO</h1>
陈园园
[http://www.infoq.com/cn/news/2017/06/Yeepay-CTO-how-great?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/06/Yeepay-CTO-how-great?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>易宝支付CTO陈斌将作为GTLC峰会的重磅嘉宾，与现场技术Leader们一起分享他关于打造优秀技术团队的实践与经验。</p> <i>By 陈园园</i>
---------------
<h1 id="#title_9" >10、再谈10x程序员</h1>
Rudy Rigot
[http://www.infoq.com/cn/news/2017/06/Talk-10x-programmers?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/06/Talk-10x-programmers?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>在之前的一篇文章中，Redis之父Salvatore Sanfilippo列出了10x程序员应该具备的9个素质。Salesforce的首席工程师Rudy Rigot从另一个角度解读10x程序员。</p> <i>By Rudy Rigot</i> <i> Translated by 薛命灯</i>
---------------
<h1 id="#title_10" >11、WWDC 2017 技术盘点</h1>
臧成威
[http://www.infoq.com/cn/news/2017/06/WWDC-2017-technology-inventory?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/06/WWDC-2017-technology-inventory?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>上周很荣幸的参加了 San Jose 举办的 WWDC 2017，本届 WWDC 可以说是近 3 年最为精彩的一届 WWDC。在各个平台上都有很多新技术和新变化涌现，也意外的让大家看到了新的硬件产品 HomePod 的发布。下面就为大家简单盘点一下 WWDC 2017 中值得一提的技术</p> <i>By 臧成威</i>
---------------
<h1 id="#title_11" >12、来自Datadog的Docker全球使用调查报告</h1>
Datadog
[http://www.infoq.com/cn/news/2017/06/Docker-global-survey-Datadog?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/06/Docker-global-survey-Datadog?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>2017年4月，美国云应用监控服务提供商Datadog发布了一份全新的全球Docker使用调查报告。Docker或许是过去几年被谈论最多的基础设施技术。这份报告对Docker在生产环境的使用情况和采用速度进行了调查。</p> <i>By Datadog</i> <i> Translated by 薛命灯</i>
---------------
<h1 id="#title_12" >13、视频演讲： 构建基于富媒体大数据的弹性深度学习计算平台</h1>
彭垚
[http://www.infoq.com/cn/presentations/elastic-depth-based-on-large-data-rich-media-learning-computing-platform?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/elastic-depth-based-on-large-data-rich-media-learning-computing-platform?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/elastic-depth-based-on-large-data-rich-media-learning-computing-platform/zh/mediumimage/pengyao270.jpg"/><p>我们离真正的智能还远吗？移动互联网带来了富媒体大数据的爆发式增长，而深度学习计算和大数据处理能力的发展，让富媒体的智能认知应用得到了高速的发展。本次演讲主要结合七牛人工智能实验室在海量富媒体数据的应用于实践，讲述如何结合容器云技术，构建富媒体大数据时代的深度学习计算平台，并探讨深度学习在视频，图像领域的一些突破和应用。</p> <i>By  彭垚</i>
---------------
<h1 id="#title_13" >14、Connecting With Users: Incorporating Humor In Web Design</h1>
Victor Yocco
[https://www.smashingmagazine.com/2017/06/connecting-users-humor-web-design/](https://www.smashingmagazine.com/2017/06/connecting-users-humor-web-design/)
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
</table><p>Joan is applying for a small loan on all-online-loanzzz.com. She's becoming frustrated with the number of financial-disclosure forms she has to fill out. She's thinking about visiting her local bank to ask for a loan instead.</p>

<figure></figure>

<p>While waiting for a page to load, the application presents a cartoon image of a person wearing a business suit sitting in a jail cell. The image caption says, "Hey, everyone hates disclosures. We know you do, too. We're doing our best to keep everyone out of jail. Please bear with us for a few more clicks. You won't regret it, and our loan officers will stay out of jail." Joan smirks at the image. She might not appreciate the number of forms she has to complete, but she understands the serious nature of applying for a loan.</p><p>The post .</p>
---------------
<h1 id="#title_14" >15、Reaching The Millennials: Mobile Marketing Trends And Techniques</h1>
Anya Pratskevich
[https://www.smashingmagazine.com/2017/06/mobile-marketing-experiences-millennial/](https://www.smashingmagazine.com/2017/06/mobile-marketing-experiences-millennial/)
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
</table><p>The average American spends at least five hours per day on their smartphone. So, why is it so hard to make mobile ads work? Marketers toil over clicks and conversions on highly targeted ads, but users, tired of intrusive banners, keep installing ad blockers.</p>

<figure></figure>

<p>With $100 billion in annual mobile ad spend at stake, someone has to figure out a way to fix this disconnect.</p>
<p>The post .</p>
---------------