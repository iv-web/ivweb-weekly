## 文章索引
1、 <a href="#1文章-musefind编写react组件的最佳实现" >文章： MuseFind：编写React组件的最佳实现</a><br/>
2、 <a href="#2文章-python-深度学习框架回顾" >文章： Python 深度学习框架回顾</a><br/>
3、 <a href="#3视频演讲-携程-redis-多数据中心实践" >视频演讲： 携程 redis 多数据中心实践</a><br/>
4、 <a href="#4视频演讲-大数据场景下应用性能排查的智能根源分析" >视频演讲： 大数据场景下应用性能排查的智能根源分析</a><br/>
5、 <a href="#5文章-对比了解grafana与kibana的关键差异" >文章： 对比了解Grafana与Kibana的关键差异</a><br/>
6、 <a href="#6高级人类的崛起" >高级人类的崛起</a><br/>
7、 <a href="#7using-social-media-for-user-research" >Using Social Media For User Research</a><br/><h1 id="#title_0" >1、文章： MuseFind：编写React组件的最佳实现</h1>
Scott Domes
[http://www.infoq.com/cn/articles/our-best-practices-for-writing-react-components?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/our-best-practices-for-writing-react-components?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/our-best-practices-for-writing-react-components/zh/smallimage/zuzhi_logo.jpg"/><p>React 起源于 Facebook 的内部项目，因为该公司对市场上所有 JavaScript MVC框架，都不满意，就决定自己写一套，用来架设Instagram的网站。做出来以后，发现这套东西很好用，就在2013年5月开源了。 由于React的设计思想极其独特，属于革命性创新，性能出众，代码逻辑却非常简单。所以，越来越多的人开始关注和使用，认为它可能是将来Web开发的主流工具。 来自MuseFind的Scott Domes日前写了一篇文章，阐述了他们编写React组件的最佳实践。Scott Domes是MuseFind的前端移动开发工程师。</p> <i>By Scott Domes</i> <i> Translated by 刘志勇</i>
---------------
<h1 id="#title_1" >2、文章： Python 深度学习框架回顾</h1>
Madison May
[http://www.infoq.com/cn/articles/review-of-python-depth-learning-framework?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/review-of-python-depth-learning-framework?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/review-of-python-depth-learning-framework/zh/smallimage/head_logo.jpg"/><p>本文翻译自 Madison May 发布的 Python Deep Learning Frameworks Reviewed，经原作者授权由InfoQ中文站翻译并分享。本文对于常用的基于 Python 的深度学习框架 Theano、 Lasagne、 Blocks、 TensorFlow、Keras、MXNet、PyTorch 进行了介绍与优劣比较，有助于深度学习入门者对于这些框架形成初步的认识。</p> <i>By Madison May</i> <i> Translated by 王下邀月熊</i>
---------------
<h1 id="#title_2" >3、视频演讲： 携程 redis 多数据中心实践</h1>
孟文超
[http://www.infoq.com/cn/presentations/ctrip-redis-multiple-datacenter-practices?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/ctrip-redis-multiple-datacenter-practices?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/ctrip-redis-multiple-datacenter-practices/zh/mediumimage/mengwenchao270.jpg"/><p>redis 在互联网公司得到了广泛的使用，携程线上业务有 2000 多组 redis 实例，每秒访问量 200 万左右(写入 10 万)；更有很多业务直接将 redis 作为内存数据库使用。内存数据库的使用需求，对 redis 跨数据中心支持能力提出了强烈的需求，高并发的访问，对系统的性能提出了严峻的挑战，然而业界并没有针对 redis 多数据中心的完整可靠解决方案。基于此，携程研发了自己的 redis 跨数据中心解决方案 X-Pipe。本次演讲将分享在整个过程中做出的技术探索以及实践。</p> <i>By  孟文超</i>
---------------
<h1 id="#title_3" >4、视频演讲： 大数据场景下应用性能排查的智能根源分析</h1>
赵宇辰
[http://www.infoq.com/cn/presentations/intelligent-data-analysis-in-big-data-scenarios?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/intelligent-data-analysis-in-big-data-scenarios?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/intelligent-data-analysis-in-big-data-scenarios/zh/mediumimage/zhaoyuchen270.jpg"/><p>随着应用场景的越来越复杂和微服务的兴起，各种软件系统、模块和服务产生的数据越来越多，应用性能正经历着大数据时代的来临，传统应用性能管理技术已经逐渐不能适应数据的增长以及业务需求。应用性能低下和应用出错已经成为困扰软件开发和运维人员最大的挑战之一。排查这类问题往往需要几个小时甚至几天的时间，严重影响了效率和商业业务。在本演讲中，我们将对应用性能中常见的半结构化数据和时间序列进行详细的分析。针对这些数据类型，我们将阐述和展示智能根源分析(RCA)的方法，从而大大降低了应用性能排查的时间至几分钟甚至几秒钟，极大提高了软件开发和运维的效率和成本。</p> <i>By 赵宇辰</i>
---------------
<h1 id="#title_4" >5、文章： 对比了解Grafana与Kibana的关键差异</h1>
Asaf Yigal
[http://www.infoq.com/cn/articles/grafana-vs-kibana-the-key-differences-to-know?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/grafana-vs-kibana-the-key-differences-to-know?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/grafana-vs-kibana-the-key-differences-to-know/zh/smallimage/logo 112 (2).jpg"/><p>我们身处海量数据的包围之中已成众所周知的事实。在此情况下，日志的管理、可视化和度量面临着更多的挑战。Kibana 和 Grafana 是两个开源工具，能可视化和推断大量日志数据内的趋势。本文将向你简单介绍一下每个工具，并主要比较一下它们之间的关键不同。</p> <i>By Asaf Yigal</i> <i> Translated by 冬雨</i>
---------------
<h1 id="#title_5" >6、高级人类的崛起</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2017/03/crispr.html](http://www.ruanyifeng.com/blog/2017/03/crispr.html)
<p>（说明：本文出自我的新书）</p>

        <p>1、</p>

<p>除了人工智能，2016年还有一项技术取得了重大突破，对人类的影响可能更大。</p>

<p>这就是基因编辑技术 。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017022801.jpg" alt="" title="" /></p>

<blockquote>
  <p>2016年4月，《自然》杂志发表，宣布发现了史上最简单方便的编辑基因的方法。</p>

<p>2016年9月，德国科学家该技术修补癌症基因，真正意义上做到预防某些癌症。</p>

<p>2016年10月，成都市华西医科大学开展世界首例，将经过基因编辑的细胞，注射到一名肺癌病人体内，该病人已到癌症末期，其他疗法都无效了。</p>
</blockquote>

<p>基因编辑技术 CRISPR 可以修剪 DNA、替换或修改基因，精确度极高，相比以前的方法，效率大幅提高，成本则大幅降低。现在能做到，像编辑照片像素那样编辑基因。很多人认为，这是近十年来，生物学界最大的科研成果。</p>

<p>2、</p>

<p>为了理解这项技术带给人类的深远影响，我先简单介绍一下什么是基因。</p>

<p>生物细胞里面都有染色体。一个染色体就是一个 DNA 分子，包含了遗传信息。你是老鼠还是人，完全由 DNA 决定。如果有一种技术，可以把老鼠的 DNA 换成人的 DNA，老鼠就可以变成人了。幸好没有这种技术。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017022802.jpg" alt="" title="" /></p>

<p>你可能会问，既然 DNA 决定了人和老鼠的差异，那么人与人的差异是什么决定的呢？</p>

<p>答案是基因。基因是 DNA 片断，决定了一个人的各种生理特征。你的身高、长相、血型、是不是色盲或左撇子，会不会早老性痴呆，都由基因决定。人的 DNA 大约包含5到10万个基因。</p>

<p>自己无法选择基因，那是先天决定的，大部分遗传自父母，还有一小部分来自基因突变。基因并不总是好的，有些基因会导致先天性生理缺陷，或者遗传病。</p>

<p>3、</p>

<p>CRISPR 技术使得人类可以改变基因了，这里擦掉一点，那里加上一笔，让生物更符合人类的需要。下面是一些已知的案例。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017022803.jpg" alt="" title="" /></p>

<blockquote>
  <p>美国科学家培育出一种，产奶性能优良，但是不长牛角，因此不会伤人。</p>

<p>哈佛大学正在从冰冻的猛犸遗体提取基因，与亚洲象的胚胎基因拼接，培养出一只有猛犸特征的大象。据说两三年内就能实现，复活恐龙也不再遥远。</p>

<p>还有一个，要改造雄蚊子的基因，使其失去繁育能力，相当于把它阉了，从而可能使得蚊子灭绝。</p>
</blockquote>

<p>上面这些例子都是"转基因动物"，但是大家心里都清楚，这项技术的主要用途是"转基因人"。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017022804.jpg" alt="" title="" /></p>

<p>美国影星安吉丽娜·朱莉，因为家族遗传，携带乳腺癌基因，母亲就死于这种癌症。她没办法，只能在38岁时切除了整个乳腺。如果有了基因编辑技术，在胚胎时期删掉致病基因，就没有这个问题了。</p>

<p>艾滋病也是如此，如果删除了艾滋病基因，人类就有可能摆脱艾滋病的威胁。</p>

<p>2017年2月15日，美国国家科学院发表："应该允许科学家修改人类胚胎，以消除镰状细胞性贫血等毁灭性遗传疾病"。</p>

<p>4、</p>

<p>问题是除了"治疗性编辑"，还有"增强性编辑"（改造基因让人类变得更完美）：肥胖基因、脱发基因、近视眼基因，这些都可以删除。那些跟感知能力相关的基因，则可以增强，让视力和听觉变得更敏锐，记忆力变得更好。</p>

<p>科学界的主流意见是禁止增强性编辑，反对人为创造出一个更优秀的人种。但是这种反对恐怕难以如愿，如果可以让人变得更好，为什么不做呢？活得更长、老得更慢、病得更少，是人类长久以来的梦想，现在终于有办法实现了，为什么要禁止呢！何况有时也很难分清治疗性编辑和增强性编辑：减少中年男子的脱发，到底是治疗还是增强，或者两者兼有？</p>

<p>就算通过法律，禁止增强性编辑，其实也禁不了。A 国禁止了。可以到 B 国做手术。即使全世界都禁止了，只要能赚钱，也会有疯狂科学家在地下室里做。</p>

<p>增强性编辑的真正问题在于，如果一些人转了基因，另一些人没转，前者就会比后者多了竞争优势。</p>

<p>5、</p>

<p>越早编辑基因，效果越好。先天性的基因缺陷，应该在胚胎或受精卵时期，就接受基因编辑。人类的胚胎将来一定会进行"基因优化"，没人想生下有缺陷的孩子，或者竞争力不如人的孩子。</p>

<p>问题就出在这里，不是每个人都有钱进行基因编辑。大部分人负担不起这笔费用，至少目前是这样。只有那些有钱人才能进行基因编辑。</p>

<p>请想象这样一样情况：上层社会的人们利用基因编辑技术，创造自己的生理优势，删除生理劣势。从胚胎开始，他们就拥有更好的基因，智力更发达、容貌更俊美，体格更健康，再加上后天的悉心培养，良好的营养和教育投入，以及家族在事业上的帮助，很容易就能取得人生成功，控制社会资源，普通人将难以与他们竞争。</p>

<p>他们会形成自己的圈子和阶层。最终，社会分裂成两种人：一种是普通人（基因没有优化过），另一种是高级人类（基因经过优化）。前者智力平平，长相平庸，体格矮小，无论在形体还是能力上，都比后者逊色。</p>

<p>6、</p>

<p>古代的贵族只是在地位、权力、财富上优于其他人，生理上并无不同。资产阶级革命提出人类生而平等的口号，但是这种假设现在不成立了。富裕阶层已经有能力编辑基因，在体能和智能上优于其他人，</p>

<p>一旦人与人在生理上不平等，那么社会就将大变。这跟以前政治经济的不平等，有着本质的区别。人类将是历史上，能够自己在内部创造出生物学意义上更高等的种类。可以想象，经过几代人的基因编辑的累积，底层的人们将全面落后于上层社会，毫无翻身的希望，等待他们的又会是什么命运呢？</p>

<p>有一点是肯定的，那就是上层社会还会进一步分化，其中相对没钱的那部分人，慢慢会变成新的下等阶层。最终，整个社会的金字塔顶端，只有很少的一部分人，他们有着最完美的、编辑得无可挑剔的基因。</p>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2017-03-01T08:23:43+08:00">2017年3月 1日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>博客文集：</li>
<li>社交媒体：</li>
<li>Feed订阅： </li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------
<h1 id="#title_6" >7、Using Social Media For User Research</h1>
Dave Ellender
[https://www.smashingmagazine.com/2017/03/using-social-media-user-research/](https://www.smashingmagazine.com/2017/03/using-social-media-user-research/)
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
</table><p>Social media is one of the dominant forms of interactions on the Internet. Leading platforms such as Facebook and Twitter count hundreds of millions of users each month. In this article, I will show you how <strong>social media is a rich vein of data for user researchers</strong>.</p>

<figure></figure>

<p>I will argue that it would be an oversight for an organization to treat social media as nothing more than an opportunity for customer service enquiries, help requests and brand advocacy.</p><p>The post .</p>
---------------