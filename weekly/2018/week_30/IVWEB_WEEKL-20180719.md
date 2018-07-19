## 文章索引
1、 <a href="#1视频演讲-去哪儿网-nodejs-实践及性能监控方案" >视频演讲： 去哪儿网 Node.js 实践及性能监控方案</a><br/>
2、 <a href="#2前端周报第69期udacity弃用react-native微信小程序将支持npm分包和可视化编程" >前端周报第69期：Udacity弃用React Native，微信小程序将支持npm、分包和可视化编程</a><br/>
3、 <a href="#3视频演讲-大规模数据中心变更风险应对之道" >视频演讲： 大规模数据中心变更风险应对之道</a><br/>
4、 <a href="#4文章-为什么能有上百万个goroutines却只能有上千个java线程" >文章： 为什么能有上百万个Goroutines，却只能有上千个Java线程？</a><br/>
5、 <a href="#5文章-猫量子位和远距传动令人匪夷所思的量子计算世界第二部分" >文章： 猫、量子位和远距传动：令人匪夷所思的量子计算世界（第二部分）</a><br/>
6、 <a href="#6视频演讲-新一代分布式数据库架构设计" >视频演讲： 新一代分布式数据库架构设计</a><br/>
7、 <a href="#7文章-现代网络负载均衡与代理上" >文章： 现代网络负载均衡与代理（上）</a><br/>
8、 <a href="#8文章-vta一个开放高度可定制化的深度学习加速器平台" >文章： VTA：一个开放、高度可定制化的深度学习加速器平台</a><br/>
9、 <a href="#9文章-观察之道带你走进可观察性" >文章： 观察之道：带你走进可观察性</a><br/>
10、 <a href="#10amazon-lambda支持以简单队列服务作为事件源了" >Amazon Lambda支持以简单队列服务作为事件源了</a><br/>
11、 <a href="#11mongodb数据库工具dbkoda-10版本提供了更好的用户体验和性能实验室" >MongoDB数据库工具dbKoda 1.0版本提供了更好的用户体验和性能实验室</a><br/>
12、 <a href="#12物联网技术周报第-143-期:-unity-3d-和-arduino-打造虚拟现实飞行器" >物联网技术周报第 143 期: Unity 3D 和 Arduino 打造虚拟现实飞行器</a><br/>
13、 <a href="#13linkbuilding:-the-citizens-field-guide" >Linkbuilding: The Citizen’s Field Guide</a><br/><h1 id="#title_0" >1、视频演讲： 去哪儿网 Node.js 实践及性能监控方案</h1>
兴百放
[http://www.infoq.com/cn/presentations/qunar-node-js-practice-and-performance-monitoring-scheme?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/qunar-node-js-practice-and-performance-monitoring-scheme?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/presentations/qunar-node-js-practice-and-performance-monitoring-scheme/zh/mediumimage/xingbaifang270-1531482856835.jpg"/><p>去哪网很早就开始在前后端分离方面做了很多不同的尝试，包括从前端（Javascript）到后端（Java）完全项目分离，到前端写部分页面逻辑（Java），然后同步到后端（Java），再到前端使用 Node.js ，后端完全提供数据的生产等一系列方案。现在内部正在尝试使用 eggjs 作为项目框架，结合 React SSR 做页面同构渲染，首屏直出。

同时，在应用发布、应用部署、机器监控、应用监控、性能监控等方面也做了一些实践，从而建立一套完整的健全的生态体系。</p> <i>By 兴百放</i>
---------------
<h1 id="#title_1" >2、前端周报第69期：Udacity弃用React Native，微信小程序将支持npm、分包和可视化编程</h1>
覃云
[http://www.infoq.com/cn/news/2018/07/arch-weekly-69?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/arch-weekly-69?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>前端周报专注大前端领域内容，帮助开发者了解一周前端热点；分为新闻热点、开发教程、工程实践、深度阅读、开源项目等栏 目。欢迎关注【前端之巅】微信公众号（ID: Frontshow），及时获取前端周报。</p> <i>By 覃云</i>
---------------
<h1 id="#title_2" >3、视频演讲： 大规模数据中心变更风险应对之道</h1>
杨涛
[http://www.infoq.com/cn/presentations/the-way-to-deal-with-the-change-of-risk-in-large-scale-data-center?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/the-way-to-deal-with-the-change-of-risk-in-large-scale-data-center?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/presentations/the-way-to-deal-with-the-change-of-risk-in-large-scale-data-center/zh/mediumimage/yangtao270-1531486746733.jpg"/><p>在大规模数据中心中，对生产环境的变更来自于各个方面，有机器类操作（重装、重启、初始化等）、机器环境变更（BIOS、内核、内核参数、基础库等）、服务变更（程序、配置、数据发布）、服务容量变更、服务操作等等。这些变更无论是自动化的还是手动的，任何一次变更都会带来服务稳定性风险。本次演讲会从具体的案例出发，介绍百度应对变更风险的防御机制演变及最佳实践。</p> <i>By 杨涛</i>
---------------
<h1 id="#title_3" >4、文章： 为什么能有上百万个Goroutines，却只能有上千个Java线程？</h1>
Russell Cohen
[http://www.infoq.com/cn/articles/a-million-go-routines-but-only-1000-java-threads?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/a-million-go-routines-but-only-1000-java-threads?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/a-million-go-routines-but-only-1000-java-threads/zh/smallimage/726272-1531566866707.jpeg"/><p>本文通过Java和Golang在底层原理上的差异，分析了Java为什么只能创建数千个线程，而Golang可以有数百万的Goroutines，并在上下文切换、栈大小方面对两者的实现原理进行了剖析。</p> <i>By Russell Cohen</i> <i> Translated by 张卫滨 </i>
---------------
<h1 id="#title_4" >5、文章： 猫、量子位和远距传动：令人匪夷所思的量子计算世界（第二部分）</h1>
Holly Cummins
[http://www.infoq.com/cn/articles/quantum-computing-algoritms-two?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/quantum-computing-algoritms-two?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/quantum-computing-algoritms-two/zh/smallimage/logo-quantum-computing-algoritms-1530726495601-1531823565526.jpg"/><p>一旦人们注意到量子系统的计算复杂性实际上是一种计算能力，量子信息理论就真正起飞了，它可以被应用于其他问题上，例如在公钥密码学中使用的因子分解。 本文探讨了量子算法及其适用性。</p> <i>By Holly Cummins</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_5" >6、视频演讲： 新一代分布式数据库架构设计</h1>
张雁飞
[http://www.infoq.com/cn/presentations/architecture-design-of-a-new-generation-of-distributed-database?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/architecture-design-of-a-new-generation-of-distributed-database?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/presentations/architecture-design-of-a-new-generation-of-distributed-database/zh/mediumimage/zhangyanfei270-1531534738203.jpg"/><p>随着数据规模越来越大，存储和运维成本逐渐增加，有人认为MySQL架构的分布式数据库已经过时，现在是NewSQL的天下，本次分享把分布式一致性协议Raft与MySQL高可用集群相结合，打造一款新式分布式数据库架构（MyNewSQL）。</p> <i>By 张雁飞</i>
---------------
<h1 id="#title_6" >7、文章： 现代网络负载均衡与代理（上）</h1>
mattklein123
[http://www.infoq.com/cn/articles/modern-network-load-balancing-and-proxying-1?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/modern-network-load-balancing-and-proxying-1?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/modern-network-load-balancing-and-proxying-1/zh/smallimage/logo-1518043435207-1531930835068.jpeg"/><p>在现代分布式系统中，负载均衡器是非常关键的组件。但是关于当代网络负载均衡的入门教材非常匮乏。为此，本文将从概念、功能、拓扑结构、现状和前景等方面，对现代网络负载均衡进行详细介绍。这里是本文的上半卷，主要介绍负载均衡的概念、功能和拓扑结构。</p> <i>By mattklein123</i> <i> Translated by 张健欣</i>
---------------
<h1 id="#title_7" >8、文章： VTA：一个开放、高度可定制化的深度学习加速器平台</h1>
VTA团队
[http://www.infoq.com/cn/articles/vta-release-announcement?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/vta-release-announcement?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/vta-release-announcement/zh/smallimage/logo-1511261592598-1531825984184.jpg"/><p>Versatile Tensor Accelerator（VTA，发音为vita）是一种开放、通用、可定制的深度学习加速器。VTA是一种可编程加速器，提供了RISC风格的编程抽象来描述张量级的操作。VTA的设计体现了主流深度学习加速器最突出和最常见的一些特征，比如张量操作、DMA加载/存储和显式的计算/内存调节。</p> <i>By VTA团队</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_8" >9、文章： 观察之道：带你走进可观察性</h1>
高洪涛
[http://www.infoq.com/cn/articles/observability-enhance?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/observability-enhance?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/observability-enhance/zh/smallimage/state-of-testing-1531883658611.jpg"/><p></p> <i>By 高洪涛</i>
---------------
<h1 id="#title_9" >10、Amazon Lambda支持以简单队列服务作为事件源了</h1>
Steef-Jan Wiggers
[http://www.infoq.com/cn/news/2018/07/aws-sqs-lambda-event-source?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/aws-sqs-lambda-event-source?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Amazon发布更新其简单队列服务（SQS）——开发人员现在可以使用SQS触发AWS Lambda函数了。而且，开发人员不再需要运行轮询服务或创建SQS到SNS的映射。</p> <i>By Steef-Jan Wiggers</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_10" >11、MongoDB数据库工具dbKoda 1.0版本提供了更好的用户体验和性能实验室</h1>
Michael Redlich
[http://www.infoq.com/cn/news/2018/07/southbank-releases-dbkoda-1.0?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/southbank-releases-dbkoda-1.0?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>在最初发布后不到一年，Southbank Software就于近日发布了其旗舰产品dbKoda的1.0版本。dbKoda是一个开源的MongoDB数据库开发工具。用户界面根据用户反馈进行了重新设计，包括了多个新特性。Southbank Software首席技术官Guy Harrison就这个最新版本接受了InfoQ的采访。</p> <i>By Michael Redlich</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_11" >12、物联网技术周报第 143 期: Unity 3D 和 Arduino 打造虚拟现实飞行器</h1>
黄峰达
[http://www.infoq.com/cn/news/2018/07/iot-weekly-143?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/iot-weekly-143?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>西门子、阿里云签约助力中国工业物联网发展；[云米发布「21Face」智能冰箱，未来的互联网家居或许就是这样了；全球智能音箱总量要破亿了，但这次的领先者从苹果换成了亚马逊；外国分析机构：中国本土语音助手崛起，亚马逊和谷歌渗透失败；4 种用于构建嵌入式 Linux 系统的工具；边缘计算实验平台的思考；Unity 3D 和 Arduino 打造虚拟现实飞行器</p> <i>By 黄峰达</i>
---------------
<h1 id="#title_12" >13、Linkbuilding: The Citizen’s Field Guide</h1>
Myriam Jessier & Stéphanie Walter
[https://www.smashingmagazine.com/2018/07/linkbuilding-the-citizens-field-guide/](https://www.smashingmagazine.com/2018/07/linkbuilding-the-citizens-field-guide/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/07/linkbuilding-the-citizens-field-guide/" />
              <title>Linkbuilding: The Citizen’s Field Guide</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>Linkbuilding: The Citizen’s Field Guide</h1>
                  
                    
                    <address>Myriam Jessier &amp; Stéphanie Walter</address>
                  
                  <time datetime="2018-07-18T14:00:07&#43;02:00" class="op-published">2018-07-18T14:00:07+02:00</time>
                  <time datetime="2018-07-18T19:42:53&#43;00:00" class="op-modified">2018-07-18T19:42:53+00:00</time>
                </header>
                <p>Before buying followers on Instagram was a common practice, before Russian trolls made fake news an Olympic sport, we had linkbuilding. Today, we <em>still</em> have linkbuilding, its just that you haven't noticed it &mdash; or have you?</p>

<p>Welcome, to the Twilight Zone, dear folks. You are about to go through a linkbuilding crash course. This will help you preserve your website, detect potential problems in content or consider why you keep receiving strange emails from strangers wanting to get their links all over your content.</p>

<figure><figcaption>Rod Sterling in the Twilight Zone TV series.</figcaption></figure>

<p><strong>Note</strong>: <em>If you are a website owner, a marketer, a blogger, a social media specialist or a regular user of the internet (and everything else in between)...you should take the time to read this!</em></p>

<h3>What Is Linkbuilding?</h3>

<blockquote>Links are basically a popularity contest. Linkbuilding is the process of gaining links to your online content in order to boost your visibility in search engines.</blockquote>

<p>Through links, search engines can analyze popularity but also other vital metrics such as authority, spam, trust. Google uses links to establish which websites are popular with users, are trusted by users or are seen as spam by users.</p>



  <aside class="product-panel product-panel__tilted product-panel--book" data-audience="non-subscriber">
    <div class="container product-panel--book__container">
      <div class="panel__description panel__description--book">
    <p>Getting the process <em>just</em> right ain't an easy task. That's why we've set up <strong>'this-is-how-I-work'-sessions</strong> — with smart cookies sharing what works really well for them. A part of the , of course.</p>
      <a href="http://smashed.by/casestudypanelmembership" class="btn btn--green btn--large">
        Explore features&nbsp;→
      </a>
      </div>
      <div class="panel__image panel__image--book">
        <a href="http://smashed.by/casestudypanelmembership" class="books__book__image">
        <div class="books__book__img">
          <img src="https://www.smashingmagazine.com/images/smashing-cat/cat-scubadiving-panel.svg" alt="Smashing TV, with live sessions for professional designers and developers." width="310" height="400">
        </div>
      </a>
      </div>
    </div>
  </aside>




<h3>Key Signals That Influence The Value Of a Link</h3>

<p>You have the stock exchange, and then you have the link exchange. All links are not created equal. Some of you may get flooded with spammy requests while others are reading this article wondering why they've never heard of linkbuilding. Some websites are more valuable and thus more targeted than others by linkbuilding attempts. Here are some key metrics that help establish the value of a link:</p>

<h4>Global Popularity</h4>

<p>The more popular a website is, the more a link from that site will have value. Wikipedia or Huffington Post have a lot of websites pointing to them which is a signal for search engines that these websites are probably important or at least very popular. Here is an example of linkbuilders trying to sell links on well-known publications that may not be aware their platform is used to peddle paid links.</p>











<figure class="article__image break-out">
	
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fd0739a7-68d2-4127-9771-6fc809966160/03-linkbuilding-the-citizen-s-field-guide.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fd0739a7-68d2-4127-9771-6fc809966160/03-linkbuilding-the-citizen-s-field-guide.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fd0739a7-68d2-4127-9771-6fc809966160/03-linkbuilding-the-citizen-s-field-guide.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fd0739a7-68d2-4127-9771-6fc809966160/03-linkbuilding-the-citizen-s-field-guide.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fd0739a7-68d2-4127-9771-6fc809966160/03-linkbuilding-the-citizen-s-field-guide.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fd0739a7-68d2-4127-9771-6fc809966160/03-linkbuilding-the-citizen-s-field-guide.png"
			sizes="100vw"
			alt=""
		/>
	

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<h4>Topical Or Local Popularity</h4>

<p>Links that are topic-specific and highly related to your subject matter are worth more than links from general or off-topic sites. A link from a dog training business pointing to an SEO training website (like the one I run) will have less value than if Smashing Magazine (a website recognized for its topical authority on the web) will. Which means that placing a link on "SEO training website" would have been an amazing opportunity for me.</p>

<h4>Placement In The Page</h4>

<p class="c-pre-sidenote--left">If a link is "editorially placed", meaning that it looks like something the author placed in the content naturally, then Google will give it more credibility. If the link is something someone with a shady profile shared in the comments, the impact won't be the same. The position of a link within a page is important. Most linkbuilders will always negotiate for a link at the beginning or in the middle of your main content. Links in footers and sidebars do not have the same value.<sup>1</sup</p><p class="c-sidenote c-sidenote--right"><sup>1</sup> “,” Link Building For SEO: The Definitive Guide (2018 Update), Backlinko</p>

<h4>Types Of Links Matter</h4>

<p>A text link tends to have more weight than an image link. Furthermore, most people forget to provide an ALT attribute for their images, which means that Google will have a hard time getting context regarding the link placed on the image. Links can also be placed in iframes.</p>

<h4>Anchor Text</h4>

<p>You know what would be an even better anchor than "SEO training website" for me? I would love to also push a local signal on top of a topical one with "SEO training in Montreal" Why is that better than placing a link on a random word like "platypus"? Well, because one of the strongest signals used by search engines is anchor text. What is anchor text? Anchor Text is the visible, clickable text in a hyperlink. For most of us, it's the blue text that's underlined, like the ones you see below. As you can see, Smashing Magazine has made it a mission to explain .</p>











<figure class="article__image break-out">
	
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0f0306bf-f6da-4383-82b5-960f32d55dee/04-linkbuilding-the-citizen-s-field-guide.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0f0306bf-f6da-4383-82b5-960f32d55dee/04-linkbuilding-the-citizen-s-field-guide.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0f0306bf-f6da-4383-82b5-960f32d55dee/04-linkbuilding-the-citizen-s-field-guide.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0f0306bf-f6da-4383-82b5-960f32d55dee/04-linkbuilding-the-citizen-s-field-guide.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0f0306bf-f6da-4383-82b5-960f32d55dee/04-linkbuilding-the-citizen-s-field-guide.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0f0306bf-f6da-4383-82b5-960f32d55dee/04-linkbuilding-the-citizen-s-field-guide.jpg"
			sizes="100vw"
			alt=""
		/>
	

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<h4>Trust Score</h4>

<p>The internet is made up of a lot of spam. In order to stay relevant to users, search engines use systems that analyze link profiles and provide a trust score. Earning links from websites with a high Trust metric can boost your own scoring metric and impact your organic visibility. That's why most SEO experts will favor non-profit organizations, universities or government websites. Those websites benefit from great Trust Score normally. I call the trust factor a trust score because each SEO tool has its own nomenclature (TrustRank, TrustFlow, etc.). This is the Trust Score of Smashing Magazine:</p>











<figure class="article__image break-out">
	
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e509d4c2-889e-444a-a21d-9892289467aa/majestic-seo-trust-flow-of-smashing-magazine.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e509d4c2-889e-444a-a21d-9892289467aa/majestic-seo-trust-flow-of-smashing-magazine.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e509d4c2-889e-444a-a21d-9892289467aa/majestic-seo-trust-flow-of-smashing-magazine.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e509d4c2-889e-444a-a21d-9892289467aa/majestic-seo-trust-flow-of-smashing-magazine.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e509d4c2-889e-444a-a21d-9892289467aa/majestic-seo-trust-flow-of-smashing-magazine.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e509d4c2-889e-444a-a21d-9892289467aa/majestic-seo-trust-flow-of-smashing-magazine.png"
			sizes="100vw"
			alt=""
		/>
	

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>So of course, you can imagine that this makes Smashing Magazine a very desirable website to have a link on. This leads to hilarious situations like this comical email by a link builder trying to buy a link from me:</p>











<figure class="article__image break-out">
	
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/56dc6b81-4b75-4213-a8fe-abd4286fd9d9/05-linkbuilding-the-citizen-s-field-guide.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/56dc6b81-4b75-4213-a8fe-abd4286fd9d9/05-linkbuilding-the-citizen-s-field-guide.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/56dc6b81-4b75-4213-a8fe-abd4286fd9d9/05-linkbuilding-the-citizen-s-field-guide.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/56dc6b81-4b75-4213-a8fe-abd4286fd9d9/05-linkbuilding-the-citizen-s-field-guide.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/56dc6b81-4b75-4213-a8fe-abd4286fd9d9/05-linkbuilding-the-citizen-s-field-guide.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/56dc6b81-4b75-4213-a8fe-abd4286fd9d9/05-linkbuilding-the-citizen-s-field-guide.png"
			sizes="100vw"
			alt=""
		/>
	

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<h4>Link Neighborhood</h4>

<p>The notion of a "link neighborhood" means that if a website is spammy and links to another website, Google will be suspicious that the other website is spammy as well. This is important because sometimes, websites are targeted by negative SEO attacks. One of the quickest ways to sabotage a competitor's organic visibility is to have a lot of spammy websites pointing to its website. This is where the notion of link neighborhood becomes incredibly important.</p>

<h4>Freshness And Pertinence</h4>

<p>Link signals tend to decay over time. That's why it's important to keep earning new links over time. This helps establish the pertinence of a website. But you have to be careful: If you keep earning links from hype websites that aren't necessarily trustworthy, your website could be seen as pertinent but not trustworthy. It's a fine balance between authority and pertinence.</p>

<h4>Social Sharing</h4>

<p>Search engines treat socially shared links differently than any other type of link. The SEO community is still debating how strong of a signal social links are.</p>

<h4>The Importance Of A Link</h4>

<p>Getting a link from a website that is considered a reputable and expert source of information is a highly valuable asset. Let's use this article to do some good and give a link to someone in Web that deserves it. Meet Nicolas Steenhout, a  doing great work. Bonjour Monsieur! I hope this link helps give your work more visibility!</p>

<h3>Common Linkbuilding Tactics</h3>

<p>Here is a quick recap of what happens to some of us on a daily basis:</p>

<ul>
<li>We receive some type of communication trying to get us to put things on our websites for strange reasons we don't understand.</li>
<li>Someone requests or demands, depending on how combative their writing style is, that we guest blog for free on platforms that we do not know, trust or like.</li>
<li>We get folks peddling SEO services. They use scare tactics to push you to pay them for their services.</li>
<li>Websites get hacked for links...or worse.</li>
</ul>

<p>Here are some of common linkbuilding tactics you should be aware of:</p>

<ul>
<li><strong>Broken linkbuilding</strong><br />If you notice a broken link in a quality website, you can email the owner and say what page the link is on and what could be a solid resource to replace the current webpage that's no longer available. Of course, the replacement you offer just so happens to be from your own website that you want to rank in search engines.</li>
<li><strong>Comment spam linkbuilding</strong><br />There is a reason why strange spammy comments keep trying to peddle certain products or websites - it's called linkbuilding.</li>
<li><strong>Negative SEO</strong><br />If you can't be first because you are the best, then buy a bunch of links to make your competitors go down in Google. That's basically what negative SEO is. Here is a  if you want to see how this can happen to any type of website owner, not just big startups or famous people.</li>
<li><strong>Sponsored content linkbuilding</strong><br />I have had many bloggers complain to me because they had been duped by agencies "buying" a sponsored article for a year on their blog. They discovered later on that what the company actually bought was a link that they could control.</li>
<li><strong>Hacking websites</strong><br />Oftentimes, websites will get hacked for SEO purposes. Because if you can't rank honestly, then parasite good websites to rank no matter what! That's the philosophy of some ruthless search engine optimization specialists. If you gain access to a website, you can place any link where you want, for as long as you want. As a website owner, it's important that you <strong>secure your website</strong> and make sure nothing strange is going on in your content. Want to see what a hacked website can look like? I recently had a case where a very legitimate website in the IT sector was hacked to host and promote a discount NBA jersey store. This is the what the website looks like:











<figure class="article__image break-out">
	
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/91028a3f-141f-443f-8d87-702e6f0e2e25/ma-carriere-techno-home.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/91028a3f-141f-443f-8d87-702e6f0e2e25/ma-carriere-techno-home.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/91028a3f-141f-443f-8d87-702e6f0e2e25/ma-carriere-techno-home.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/91028a3f-141f-443f-8d87-702e6f0e2e25/ma-carriere-techno-home.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/91028a3f-141f-443f-8d87-702e6f0e2e25/ma-carriere-techno-home.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/91028a3f-141f-443f-8d87-702e6f0e2e25/ma-carriere-techno-home.png"
			sizes="100vw"
			alt=""
		/>
	

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


However, what they were not aware of was that the website had been hacked. Upon analyzing their incoming links, it was clear that this IT focused website was known for "cheap NBA jerseys" and "wholesale NBA jerseys" than anything else. I wondered why, and found a lot of pages were receiving links:











<figure class="article__image break-out">
	
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d90a4329-026d-4bd1-b62d-31194f67e770/jerseys.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d90a4329-026d-4bd1-b62d-31194f67e770/jerseys.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d90a4329-026d-4bd1-b62d-31194f67e770/jerseys.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d90a4329-026d-4bd1-b62d-31194f67e770/jerseys.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d90a4329-026d-4bd1-b62d-31194f67e770/jerseys.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d90a4329-026d-4bd1-b62d-31194f67e770/jerseys.png"
			sizes="100vw"
			alt=""
		/>
	

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


The wonderful developer team cleaned up the damage and made sure to patch any security breach they found. However, this specific hacker thrives in websites that have been hacked and are full of malware such as this one:











<figure class="article__image break-out">
	
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3dfdc8c0-d8b3-4db0-91be-48aa0cfa87ff/ecommerce-nba-jersey-hack.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3dfdc8c0-d8b3-4db0-91be-48aa0cfa87ff/ecommerce-nba-jersey-hack.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3dfdc8c0-d8b3-4db0-91be-48aa0cfa87ff/ecommerce-nba-jersey-hack.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3dfdc8c0-d8b3-4db0-91be-48aa0cfa87ff/ecommerce-nba-jersey-hack.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3dfdc8c0-d8b3-4db0-91be-48aa0cfa87ff/ecommerce-nba-jersey-hack.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3dfdc8c0-d8b3-4db0-91be-48aa0cfa87ff/ecommerce-nba-jersey-hack.png"
			sizes="100vw"
			alt=""
		/>
	

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>
</li>
<li><strong>Link outreach</strong><br />If you get bombarded with emails asking you to review a product or add a link in your blog article, chances are that you have been targeted during a link outreach campaign. You can always decline or simply not answer this unsolicited email. On the flipside of the coin, if you get offers to place your links in some highly regarded publications, know that this is an offer the person is making you to place your links on certain website.</li>
<li><strong>Guest blogging</strong><br />If someone asks you to create an article on their platform, the often want free quality content with your notoriety to promote it in order to garner links. If on the other hand, someone offers you free content for your website, chances are that it is for linkbuilding purposes.</li>
<li><strong>PBN</strong><br />A <strong>P</strong>rivate <strong>B</strong>log <strong>N</strong>etwork is a network of websites with great SEO metrics used to build links to a main website in order to help it rank higher in search engines. It means that someone usually ranks multiple websites high in Google in order to use them to place links that will boost the visibility of a chosen site. Google does not appreciate PBN efforts or link exchange efforts and routinely penalizes networks of websites.</li>
<li><strong>Creating awesome content</strong><br />There are many linkbuilding tactics that push for the creation of tools, content or other types of media that is so good, so useful and so relevant that they will naturally garner links from other website owners. We won't detail them here but they usually work well because they provide something <strong>useful that deserves to be shared with others!</strong></li>
</ul>

<div class="sponsors__wide-place"></div>




<h3>The Hidden Survival Guide To Linkbuilding</h3>

<p>Read this part if you are a website owner, a UX, a customer, a visitor, a blogger, my friend Igor (hi Igor, please read this!) or anyone else using search engines regularly to find information. Let's get started by giving you access to the  on the matter. Website guidelines vary from search engine to search engine. You can check each search engine's guidelines but oftentimes, the broader concepts of what qualifies as a good website in terms of SEO are the same.</p>

<h4>The Ugly Truth: Not All Linkbuilding Is Bad</h4>

<p>Google clearly disagrees with paying for links or selling links. However, keep this in mind: not all linkbuilding efforts are bad. Earlier in this article, I gave a shout out to a friend of mine because I know that it will help give his website some visibility in search engines. Offering a link is a way to show your support for a product, an article, a tool, a website, a person. It is a vote of confidence in their favor. If you go out of your way to do it, technically, that counts as linkbuilding. Linkbuilding is also a way to make money. Some website owners may leverage linkbuilding to earn money despite legal regulations and Google's guidelines.</p>

<h4>If You See Something, Say Something!</h4>

<p>You can signal bad links and anything strange going on that may be related to a hack, malware or even paid links to Google. You can .</p>

<h4>Make It Clear If You Accept Or Refuse Linkbuilding Offers</h4>

<p>If you are a blogger, make sure you are aware of your rights and responsibilities when it comes to linkbuilding efforts. Make sure to update your key pages to reflect your linkbuilding policy. This could be done in the about page, the services page if you offer services or the contact page.</p>

<p>Take the time to specify if you accept of refuse commercial or affiliate links in the content of a guest blog post for example. This will also help avoid nasty linkbuilding surprises in the future.</p>

<h4>Nofollow: You Can Have Sponsored Content And Still Respect The Guidelines!</h4>

<p>So what do you do if you realize that someone is using your website to place a link? Well, if this is something that was done legally, you can fix the situation by placing an attribute on your link that will signal to search engine bots not to follow the link. A nofollow link is a way to make sure that links from sponsored posts are not going against Google's guidelines. This type of link cancels the linkbuilding benefits as Google gives them no love because the nofollow tag in the code signals "do not take this link into account." Website owners and administrators should  into a nofollow link as it can be done quickly and easily.</p>

<p>This is what a nofollow link looks like in the code:</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7786efc2-2498-4310-98e0-49bdbc7bfa5d/nofollow-link-in-wikipedia.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7786efc2-2498-4310-98e0-49bdbc7bfa5d/nofollow-link-in-wikipedia.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7786efc2-2498-4310-98e0-49bdbc7bfa5d/nofollow-link-in-wikipedia.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7786efc2-2498-4310-98e0-49bdbc7bfa5d/nofollow-link-in-wikipedia.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7786efc2-2498-4310-98e0-49bdbc7bfa5d/nofollow-link-in-wikipedia.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7786efc2-2498-4310-98e0-49bdbc7bfa5d/nofollow-link-in-wikipedia.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7786efc2-2498-4310-98e0-49bdbc7bfa5d/nofollow-link-in-wikipedia.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>So, what do you do if you are asked for a link in exchange for a review?</p>

<p>This is the most common way most bloggers are approached in order to get links placed on their websites. Here are some guidelines for bloggers that .</p>

<p>If you think your website is hacked for links, you must first secure your website and do a security audit. The second step would entail cleaning up the links and the third step includes submitting a  to Google that signals any shady domains that may be pointing to you because of hacker activity.</p>

<h4>Red Flag #1 : You Start Seeing Your Organic Traffic Go Down</h4>

<p>If you haven't changed anything and you see your organic traffic go down, make sure it's not a link issue. You could have suffered an attack. We recommend you use the Google Search Console tool available to all website owners and administrators. You must validate that you own the website and then, you will be able to receive an alert if Google detects something is very wrong with your website. Careful, if something is wrong with your website, it could mean a penalty and cause a substantial organic traffic drop. To know more about the types of penalties and alerts Google Search Console provides, you can  or check the official documentation.</p>

<h4>Red Flag #2: Downloading A Premium Theme Or Plugin For Free</h4>

<p>This is a very underhanded technique to obtain links. Some individuals will pay for a premium theme or plugin or software and offer it for free on torrent websites or forums where free or hacked versions of premium products are made available. When someone downloads the theme and uses it on a website, the doctored version of theme is used to place links in the website. Oftentimes, the owners never notice that their website is hosting parasite links.</p>

<h4>Red Flag #3: You Start Getting Strange Feedback About Your Website Or See Strange Content Appear</h4>

<p>If your readers, customers, visitors or even Google Search Console start telling you about strange content or links showing up on your website, this means that it's time for an SEO audit and a security audit to assess the damage done to your website. Something tells me that Schneiters Gold did not plan on ever offering the BEST Online Viagra OFFERS...</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f3d5bb5b-f20f-4c68-b4de-379ab6fa2121/viagra-phama-hack.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f3d5bb5b-f20f-4c68-b4de-379ab6fa2121/viagra-phama-hack.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f3d5bb5b-f20f-4c68-b4de-379ab6fa2121/viagra-phama-hack.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f3d5bb5b-f20f-4c68-b4de-379ab6fa2121/viagra-phama-hack.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f3d5bb5b-f20f-4c68-b4de-379ab6fa2121/viagra-phama-hack.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f3d5bb5b-f20f-4c68-b4de-379ab6fa2121/viagra-phama-hack.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f3d5bb5b-f20f-4c68-b4de-379ab6fa2121/viagra-phama-hack.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<h4>Red Flag #4: You Get A Google Search Console Warning</h4>

<p>If you get an email from the Google Search Console team telling you about some spam issues or other problems that cause you to break their guidelines, you should investigate immediately the source of the problem and fix the issue fast or you could risk a penalty.</p>

<h4>Red Flag #5: The Link Looks Like It Could Be A Hidden Affiliate Link Or A Redirect</h4>

<p>Always check the links before placing them. Click the links and see where they lead. You could be provided a link that looks like a high-quality content but instead, it points to a spammy page.</p>

<p>Make sure to ask if a link is an affiliate link. Affiliate links are links that contain information that helps track a sale back to the person who promoted the product. These affiliate partners get a cut each sale that is attributed to them. Companies like Amazon and Forever21 among others have affiliate programs. You do not want someone promoting a product purely for money and you do not want to lose the trust of search engines and human visitors.</p>

<div class="sponsors__wide-place"></div>




<h3>Advice For Linkbuilders, Growth Hackers And Anyone Looking to Gain More Visibility In Search Engines</h3>

<h5>Vet a website before getting in touch</h5>

<p>Go ahead, click on the link and check out the website before you do anything else. Otherwise, you will end up contacting your competitors, unrelated blogs, spammy websites, etc.</p>

<h5>Read the advertising page</h5>

<p>Most websites have a page, it can be the contact, advertise or about page, that lists the specs and guidelines to collaborate with the websites. Respect what's written on there! Do not bother folks that clearly said they do not want to be contacted for links. <strong>No, you are not the one that will make them change their minds. Yes, we're sure.</strong></p>

<h5>Avoid metric blindness</h5>

<p>My very good friend Igor, proud owner of Igor.io, gets contacted all the time by linkbuilding companies. Why? Because their website was once upon a time (before they removed their incredible archive of technical articles) had incredible metrics. For reference, Igor has a fully responsive, accessible website and it looks like this:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ea85d880-49ae-44a3-aafd-f97f1692d8ed/06-linkbuilding-igors-weblog.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ea85d880-49ae-44a3-aafd-f97f1692d8ed/06-linkbuilding-igors-weblog.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ea85d880-49ae-44a3-aafd-f97f1692d8ed/06-linkbuilding-igors-weblog.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ea85d880-49ae-44a3-aafd-f97f1692d8ed/06-linkbuilding-igors-weblog.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ea85d880-49ae-44a3-aafd-f97f1692d8ed/06-linkbuilding-igors-weblog.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ea85d880-49ae-44a3-aafd-f97f1692d8ed/06-linkbuilding-igors-weblog.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ea85d880-49ae-44a3-aafd-f97f1692d8ed/06-linkbuilding-igors-weblog.png"
			sizes="100vw"
			alt="igor.io"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>But Igor's weblog's metrics look like this (and they looked even more enticing to SEOs the last time I checked):</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0f325993-4f1a-4187-b64e-6bcd789ff04f/07-linkbuilding-the-citizen-s-field-guide.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0f325993-4f1a-4187-b64e-6bcd789ff04f/07-linkbuilding-the-citizen-s-field-guide.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0f325993-4f1a-4187-b64e-6bcd789ff04f/07-linkbuilding-the-citizen-s-field-guide.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0f325993-4f1a-4187-b64e-6bcd789ff04f/07-linkbuilding-the-citizen-s-field-guide.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0f325993-4f1a-4187-b64e-6bcd789ff04f/07-linkbuilding-the-citizen-s-field-guide.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0f325993-4f1a-4187-b64e-6bcd789ff04f/07-linkbuilding-the-citizen-s-field-guide.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0f325993-4f1a-4187-b64e-6bcd789ff04f/07-linkbuilding-the-citizen-s-field-guide.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>This meant that a lot of companies wanted to contact the owner of a website that had more than 1000 high-quality websites referring to it. But if they had bothered to check out Igor's website, they would have seen that nothing was on there. Back in the days, this website just read: <em>igor's weblog</em> and the archive was hidden in the code. You had to know where to look for it... or you would find it very easily if you happened to be a bot. That's why the metrics were the so high: only a bot and those in the know would discover and share Igor's content.</p>

<h5>Know who you are talking to</h5>

<p>I get emails telling me to ask my boss if the company can place a link on my website. Now, quick reminder, if you go on myriamjessier.com and contact me, the person with an email that contains the words myriam + jessier, chances are that you are talking to the owner herself, right? Which leads me to another point: write my name correctly please and do not address me as sir, or dear, or dear sir. This is a common issue that Stéphanie Walter has as half of the Internet doesn't seem to know .</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9fab39de-e602-4a32-a646-177ac33c6957/08-linkbuilding-the-citizen-s-field-guide.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9fab39de-e602-4a32-a646-177ac33c6957/08-linkbuilding-the-citizen-s-field-guide.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9fab39de-e602-4a32-a646-177ac33c6957/08-linkbuilding-the-citizen-s-field-guide.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9fab39de-e602-4a32-a646-177ac33c6957/08-linkbuilding-the-citizen-s-field-guide.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9fab39de-e602-4a32-a646-177ac33c6957/08-linkbuilding-the-citizen-s-field-guide.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9fab39de-e602-4a32-a646-177ac33c6957/08-linkbuilding-the-citizen-s-field-guide.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9fab39de-e602-4a32-a646-177ac33c6957/08-linkbuilding-the-citizen-s-field-guide.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<h5>Not knowing or ignoring legal guidelines and Google's guidelines</h5>

<p>If you do not disclose why you are asking for a link and that there could be a risk to a website selling you a link, then you are not being transparent.</p>

<h5>Bonus Tip</h5>

<p>Don't reach out to experts who do what you do for a living. I receive linkbuilding offers (buying and selling) from other search engine optimization "specialists" all the time. If you found me on the web and are offering to sell me links because my website <em>isn't visible enough</em>, then maybe, just maybe, my SEO efforts are working no?</p>

<h3>Conclusion</h3>

<p>We hope that you learned a few things about linkbuilding. Here is a quick recap:</p>

<ul>
<li>There's money in the  and in linkbuilding.</li>
<li>Not all links are equal, key metrics are : authority, freshness, placement, relevancy.</li>
<li>People will go to extremes to get links so if a “great deal” is offered to you, look for the hidden link in there!</li>
<li>Secure your website to avoid SEO problems. If you make it hard work for hackers, they will often give up and move on to an easier prey.</li>
<li>If you want to help someone out, make sure you give them a link with a good anchor! It really helps!</li>
</ul>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(ra, yk, il)</span>
</div>


              </article>
            </body>
          </html>
---------------