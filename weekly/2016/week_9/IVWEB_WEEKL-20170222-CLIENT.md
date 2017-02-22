## 文章索引
1、 <a href="#1前端开发周报pwa-将与安卓原生平起平坐v8-团队致力于提高-es2015-特性性能" >前端开发周报：PWA 将与安卓原生平起平坐、V8 团队致力于提高 ES2015 特性性能</a><br/>
2、 <a href="#2文章-将持久数据从redis中迁出" >文章： 将持久数据从Redis中迁出</a><br/>
3、 <a href="#3视频演讲-京东大促之大规模分布式监控系统实践" >视频演讲： 京东大促之大规模分布式监控系统实践</a><br/>
4、 <a href="#4视频演讲-当互联网金融遇到区块链" >视频演讲： 当互联网金融遇到区块链</a><br/>
5、 <a href="#5文章-万亿级日志与行为数据存储查询技术剖析" >文章： 万亿级日志与行为数据存储查询技术剖析</a><br/>
6、 <a href="#6文章-遗留系统流水线的改进" >文章： 遗留系统流水线的改进</a><br/>
7、 <a href="#7专访rocketmq联合创始人项目思路技术细节和未来规划" >专访RocketMQ联合创始人：项目思路、技术细节和未来规划</a><br/>
8、 <a href="#8谷歌新发布的分布式数据库服务是要打破cap定理了吗" >谷歌新发布的分布式数据库服务，是要打破CAP定理了吗？</a><br/>
9、 <a href="#9谷歌宣布pwa将获得与安卓原生应用同等的待遇与权限" >谷歌宣布，PWA将获得与安卓原生应用同等的待遇与权限</a><br/>
10、 <a href="#10a-detailed-introduction-to-webpack" >A Detailed Introduction To Webpack</a><br/><h1 id="#title_0" >1、前端开发周报：PWA 将与安卓原生平起平坐、V8 团队致力于提高 ES2015 特性性能</h1>
王下邀月熊
[http://www.infoq.com/cn/news/2017/02/Front-end-PWA-V8-ES2015?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/02/Front-end-PWA-V8-ES2015?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>前端之巅周报，遵循中立报道原则，描述清楚事件，或提取大纲，不夹杂个人情感和观点。可以提供别人相关的观点链接。</p> <i>By 王下邀月熊</i>
---------------
<h1 id="#title_1" >2、文章： 将持久数据从Redis中迁出</h1>
刘志勇
[http://www.infoq.com/cn/articles/github-moves-persistent-data-out-of-redis?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/github-moves-persistent-data-out-of-redis?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/github-moves-persistent-data-out-of-redis/zh/smallimage/logo-java.jpg"/><p>但是，Redis的两种持久化方式也有明显的缺点： RDB需要定时持久化，风险是可能会丢两次持久之间的数据，量可能很大。 AOF每秒fsync一次指令硬盘，如果硬盘IO慢，会阻塞父进程；风险是会丢失1秒多的数据；在Rewrite过程中，主进程把指令存到mem-buffer中，最后写盘时会阻塞主进程。 这两个缺点是个很大的痛点。为了解决这些痛点，GitHub的两位工程师Bryana Knight和Miguel Fernández日前写了一篇文章，讲述了将持久数据从Redis迁出的经验， 经Bryana Knight和Miguel Fernández的独家授权，InfoQ翻译并整理了他们合著的文章，以飨广大读者，以下是正文。</p> <i>By 刘志勇</i>
---------------
<h1 id="#title_2" >3、视频演讲： 京东大促之大规模分布式监控系统实践</h1>
鲍永成
[http://www.infoq.com/cn/presentations/large-scale-distributed-monitoring-system-of-Jingdong?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/large-scale-distributed-monitoring-system-of-Jingdong?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/large-scale-distributed-monitoring-system-of-Jingdong/zh/mediumimage/baoyongcheng270.jpg"/><p>京东业务壮大，特别是大规模容器落地后，对基础监控带来挑战。在此背景下，带领团队自研 light 监控平台（内部名称 mjdos 系统），帮助运维和研发同事更好的监控运维业务系统。
light 分布式监控平台特点：
支持容器类型监控数据采集；
全容器化部署，弹性伸缩；
支持跨 IDC 部署和感知；
海量监控采集点；
监控能力平台化 & 开放 API。</p> <i>By 鲍永成</i>
---------------
<h1 id="#title_3" >4、视频演讲： 当互联网金融遇到区块链</h1>
邓明
[http://www.infoq.com/cn/presentations/when-the-internet-financial-encounter-block-chain?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/when-the-internet-financial-encounter-block-chain?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/when-the-internet-financial-encounter-block-chain/zh/mediumimage/dengming270.jpg"/><p>区块链是2016年最受关注的技术之一。由于其出自于比特币，大家对于其在金融领域，尤其是互联网金融领域的应用充满了兴趣。国付宝作为第三方支付公司，凭借多年的互联网金融行业经验，已经开始了区块链应用的尝试。本主题试图通过区块链技术介绍，应用案例介绍，以及对未来愿景的探讨，向大家展示区块链技术可能为互联网金融业务带来的革新和促进。</p> <i>By 邓明</i>
---------------
<h1 id="#title_4" >5、文章： 万亿级日志与行为数据存储查询技术剖析</h1>
王劲
[http://www.infoq.com/cn/articles/trillion-log-and-data-storage-query-techniques?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/trillion-log-and-data-storage-query-techniques?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/trillion-log-and-data-storage-query-techniques/zh/smallimage/logo2 (10).jpg"/><p>近些年，大数据背后的价值也开始得到关注和重视，越来越多的企业开始保存和分析数据，希望从中挖掘大数据的价值。大数据产生的根本还是增量数据，单纯的用户数据不足以构成大数据，然而用户的行为或行为相关的日志的数据量，加之随着物联网的发力，产生的增量数据将不可预估，存储和查询增量数据尤为关键。</p> <i>By 王劲</i>
---------------
<h1 id="#title_5" >6、文章： 遗留系统流水线的改进</h1>
杨政权
[http://www.infoq.com/cn/articles/improvement-of-legacy-system-pipeline?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/improvement-of-legacy-system-pipeline?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/improvement-of-legacy-system-pipeline/zh/smallimage/java-logo2.jpg"/><p>持续集成（Continuous Integration）是一种软件开发实践，它倡导开发团队频繁地进行系统集成，每一次的集成都可以通过流水线（Pipeline）快速验证。和传统的集成方式相比，持续集成可以有效地缩短反馈周期、提高软件质量、降低开发成本。这种开发实践也越来越为更多的开发者所接受。对于一个有七年历史的项目，非常幸运的是我们在项目刚开始就使用了持续集成，这也是我们可以长期、稳定地给客户交付高质量软件的保障之一。</p> <i>By 杨政权</i>
---------------
<h1 id="#title_6" >7、专访RocketMQ联合创始人：项目思路、技术细节和未来规划</h1>
木环
[http://www.infoq.com/cn/news/2017/02/RocketMQ-future-idea?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/02/RocketMQ-future-idea?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>最早的代码对外开放可以追溯到1953年 UNVAC A-2系统，然而线上社区氛围则开始于九十年代:Usenet一个全球性的文件交换网络提供了基础条件，随后陆续出现了GNU和BSD项目，接下来Linux问世、红帽基金会成立、MySQL诞生。Apache HTTP网络服务器于1996年的受到开源社区和市场的热捧，而Apache软件基金会在1999年正式成立。 这些年开源氛围越来越好，各大IT公司都纷纷将一些自研项目开源出来，其中不乏中国技术企业的身影。不过项目代码开源与项目被纳入开源软件基金会是两回事，如果想加入到开源软件基金则需要经过评审方的考核与观察。坦率而言，业界还对中国的技术开源参与保持着旧有的刻板印象。 那么RocketMQ项目，究竟用怎样的技术内涵，缘何赢得了基金会的初步认可呢？InfoQ带着这样的疑问对两位项目联合创始人进行了专访，内容整理如下。</p> <i>By  木环</i>
---------------
<h1 id="#title_7" >8、谷歌新发布的分布式数据库服务，是要打破CAP定理了吗？</h1>
登州知府
[http://www.infoq.com/cn/news/2017/02/Google-Cloud-Spanner-hit-CAP?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/02/Google-Cloud-Spanner-hit-CAP?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>2月14日，Google 宣布推出 Cloud Spanner 云端数据库服务的 Beta 版。Cloud Spanner 是构建在 Google Cloud Platform（GCP）平台上的全球级分布式关系型数据库服务，主要为 OLTP 场景的核心业务应用提供服务。不同于 Bigtable、Cloud SQL 和 Cloud Datastore，此次 Google 发布的 Cloud Spanner 打破了传统关系型数据库与 NoSQL 数据库之间的壁垒，让开发者可以使用到兼具二者优点的新型数据库：支持 ACID 事务及 SQL 语义，同时具备水平扩展和跨数据中心高可用。</p> <i>By  登州知府</i>
---------------
<h1 id="#title_8" >9、谷歌宣布，PWA将获得与安卓原生应用同等的待遇与权限</h1>
周元昊
[http://www.infoq.com/cn/news/2017/02/PWA-Chrome?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/02/PWA-Chrome?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>自从谷歌提出PWA概念之后，它就持续受到移动开发界的关注。由于其可靠、快速、融入的特性，大大提升了网络应用的用户友好性。近日官方博客更进一步宣布将使PWA应用获得和原生应用同等的待遇与权限。</p> <i>By 周元昊</i>
---------------
<h1 id="#title_9" >10、A Detailed Introduction To Webpack</h1>
Joseph Zimmerman
[https://www.smashingmagazine.com/2017/02/a-detailed-introduction-to-webpack/](https://www.smashingmagazine.com/2017/02/a-detailed-introduction-to-webpack/)
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
</table><p>JavaScript module bundling has been around for a while. RequireJS had its first commits in 2009, then Browserify made its debut, and since then several other bundlers have spawned across the Internet.</p>

<figure></figure>

<p>Among that group, <em>webpack</em> has jumped out as one of the best. If you’re not familiar with it, I hope this article will get you started with this powerful tool.</p><p>The post .</p>
---------------