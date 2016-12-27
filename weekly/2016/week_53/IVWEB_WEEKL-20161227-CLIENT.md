## 文章索引
1、 <a href="#1文章-我们正处在一个激进的后开源时代开源的过去和未来" >文章： 我们正处在一个激进的后开源时代：开源的过去和未来</a><br/>
2、 <a href="#2视频演讲-构建-react-同构应用及优化" >视频演讲： 构建 React 同构应用及优化</a><br/>
3、 <a href="#3视频演讲-又拍云-企业容器私有云架构分享" >视频演讲： 又拍云-企业容器私有云架构分享</a><br/>
4、 <a href="#4文章-跨越篱笆蘑菇街每秒订单数25倍提升历程" >文章： 跨越篱笆：蘑菇街每秒订单数25倍提升历程</a><br/>
5、 <a href="#5文章-增进编程技能的万全之计" >文章： 增进编程技能的万全之计</a><br/>
6、 <a href="#6文章-腾讯亿级排行榜系统实践及挑战" >文章： 腾讯亿级排行榜系统实践及挑战</a><br/>
7、 <a href="#7fex-技术周刊---2016/12/26" >FEX 技术周刊 - 2016/12/26</a><br/>
8、 <a href="#8文章-腾讯游戏运维服务体系演变史" >文章： 腾讯游戏运维服务体系演变史</a><br/>
9、 <a href="#9区块链云计算大数据人工智能fintech带来的挑战与机遇中国技术开放日上海站精彩回顾" >区块链、云计算、大数据、人工智能、FinTech带来的挑战与机遇，中国技术开放日上海站精彩回顾</a><br/>
10、 <a href="#10netflix-conductor一个微服务编制引擎" >Netflix Conductor：一个微服务编制引擎</a><br/>
11、 <a href="#11dropbox是如何安全地存储用户密码的" >Dropbox是如何安全地存储用户密码的</a><br/>
12、 <a href="#122016年deepmind给人类带来了什么" >2016年：DeepMind给人类带来了什么？</a><br/>
13、 <a href="#13人工智能周报第五期" >人工智能周报（第五期）</a><br/>
14、 <a href="#14用深度神经网络生成以假乱真的照片" >用深度神经网络生成以假乱真的“照片”</a><br/><h1 id="#title_0" >1、文章： 我们正处在一个激进的后开源时代：开源的过去和未来</h1>
Nadia Eghbal
[http://www.infoq.com/cn/articles/we-live-in-open-radical-source-era?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/we-live-in-open-radical-source-era?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/we-live-in-open-radical-source-era/zh/smallimage/bigdataaquan_logo.jpg"/><p>开源改变了初创公司，而初创公司也反过来改变了开源。LAMP技术栈、GitHub和Stack Overflow为开源的流行做了很大贡献。这是开源的伟大胜利。不过与此同时，开源也面临着新的挑战。或许我们还未感受到肩上的重担，但是冬天真的来了。在后开源时代，我们必须去面对这些问题。</p> <i>By Nadia Eghbal</i> <i> Translated by 薛命灯</i>
---------------
<h1 id="#title_1" >2、视频演讲： 构建 React 同构应用及优化</h1>
蒋吉麟
[http://www.infoq.com/cn/presentations/application-and-optimization-of-constructing-react-isomorphism?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/application-and-optimization-of-constructing-react-isomorphism?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/application-and-optimization-of-constructing-react-isomorphism/zh/mediumimage/jiangjilin270.jpg"/><p>React 作为当下最热门的的 Web 框架以及在 FaceBook 的支持下，React 社区获得了茁长成长。今天，我们来讨论基于 React 官方组件 react router 构建同构应用的实践经验（Webpack+ES6+React+Babel）。享受一次代码同构渲染带来的便捷，也同时需要考虑同构应用带来的数据安全性的问题。以及在实际开发过程中，遇到的性能问题以及优化步奏。当然了，也同时需要思考是否每个人都需要同构应用呢？</p> <i>By 蒋吉麟</i>
---------------
<h1 id="#title_2" >3、视频演讲： 又拍云-企业容器私有云架构分享</h1>
莫红波
[http://www.infoq.com/cn/presentations/sharing-of-architecture-of-ypyun-container-private-cloud?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/sharing-of-architecture-of-ypyun-container-private-cloud?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/sharing-of-architecture-of-ypyun-container-private-cloud/zh/mediumimage/mohonbo270.jpg"/><p>又拍云拥有一个大规模的处理集群，主要用来进行图片以及音视频处理，但是，在实际使用过程中，我们发现很多物理资源没有很好的利用起来。另一方面，客户反馈上来的小需求越来越多，如果每一个项目都交给运维发布的话，会极大增加运维同学的工作量，而且物理主机上的环境隔离也是一件十分头疼事情。
本次分享主要介绍又拍云私有云架构中的几个主要组件，基于 OpenResty 的动态服务路由 Slardar (已开源) 、基于 GitLab-CI 的容器交付、基于 ElasticSearch/Kibana/Slack 的容器监控告警、基于 Mozilla Heka 的容器日志搜集。</p> <i>By 莫红波</i>
---------------
<h1 id="#title_3" >4、文章： 跨越篱笆：蘑菇街每秒订单数25倍提升历程</h1>
七公
[http://www.infoq.com/cn/articles/mogujie-orders-per-second-25-times-enhance?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/mogujie-orders-per-second-25-times-enhance?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/mogujie-orders-per-second-25-times-enhance/zh/smallimage/logo4 (2).jpg"/><p>本文根据白辉在2016ArchSummit全球架构师（深圳）峰会上的演讲整理而成。</p> <i>By 七公</i>
---------------
<h1 id="#title_4" >5、文章： 增进编程技能的万全之计</h1>
Jerod Santo
[http://www.infoq.com/cn/articles/one-sure-fire-way-to-improve-your-coding?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/one-sure-fire-way-to-improve-your-coding?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/one-sure-fire-way-to-improve-your-coding/zh/smallimage/logo (23).jpg"/><p>增进编程能力最明显的方式就是尽可能编写更多代码，然而还有另一种完全“背道而驰”的方式：阅读别人写的代码。</p> <i>By Jerod Santo</i> <i> Translated by 大愚若智</i>
---------------
<h1 id="#title_5" >6、文章： 腾讯亿级排行榜系统实践及挑战</h1>
唐聪
[http://www.infoq.com/cn/articles/tencent-ranking-system-practice-and-challenges?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/tencent-ranking-system-practice-and-challenges?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/tencent-ranking-system-practice-and-challenges/zh/smallimage/heinz-kabutz-article-icon.jpg"/><p>腾讯排行榜系统从无到有，接入排行榜数实现了从几个到数万的突破，单个排行榜用户数最大9000万, 存储集群活跃用户量数亿 1. 排行榜系统基本架构； 2. 如何支撑数万乃至百万级排行榜自动化申请？ 3. 如何降低机器成本？选择合适存储引擎？</p> <i>By 唐聪</i>
---------------
<h1 id="#title_6" >7、FEX 技术周刊 - 2016/12/26</h1>

[http://fex.baidu.com/blog/2016/12/fex-weekly-26//](http://fex.baidu.com/blog/2016/12/fex-weekly-26//)
作者：duhongbin01 <br> <p>微信搜索『FEX』关注我们的公众号，及时获得最新资讯。</p>

<h2 id="section">深阅读</h2>

<p><strong>Building Jarvis</strong><br />
https://www.facebook.com/notes/mark-zuckerberg/building-jarvis/10154361492931634<br />
http://www.leiphone.com/news/201612/09HecjzLRdGX3r81.html<br />
My personal challenge for 2016 was to build a simple AI to run my home – like Jarvis in Iron Man.
My goal was to learn about the state of artificial intelligence – where we’re further along than people realize and where we’re still a long ways off. These challenges always lead me to learn more than I expected, and this one also gave me a better sense of all the internal technology Facebook engineers get to use, as well as a thorough overview of home automation.  作为 Facebook 的 CEO，Zuckerberg 却依然保持写代码的习惯，而且同时用多种语言，这种对 coding 的热爱值得广大码农学习，这应该是 Facebook 工程师文化的最好体现。</p>

<p><strong>Front-End Performance Checklist 2017</strong><br />
https://www.smashingmagazine.com/2016/12/front-end-performance-checklist-2017-pdf-pages/<br />
Performance isn’t just a technical concern: It matters, and when baking it into the workflow, design decisions have to be informed by their performance implications. Below you’ll find a (hopefully unbiased and objective) front-end performance checklist for 2017 — an overview of the issues you might need to consider to ensure that your response times are fast and your website smooth.</p>

<p><strong>10 things I learned making the fastest site in the world</strong><br />
https://hackernoon.com/10-things-i-learned-making-the-fastest-site-in-the-world-18a0e1cdf4a7#.jcfny4tqc<br />
Writing a fast website is like raising a puppy, it requires constancy and consistency (both over time and from everyone involved). You can do a great job keeping everything lean and mean, but if you get sloppy and use an 11 KB library to format a date and let the puppy shit in the bed just one time, you’ve undone a lot of hard work and have some cleaning up to do. 另附：</p>

<p><strong>13 things you need to know about React</strong><br />
https://hackernoon.com/13-things-you-need-to-know-about-react-d2e6a6422552#.iuf1zr20x<br />
I’ve been using React for over a year now. I’m also conducting training to help people learn it from scratch. I noticed that on every training session I’m explaining the same set of concepts over and over. I think those concepts are essential if you want to “speak React”. If you are in a middle of learning it right know, you might be interested in reading this post.</p>

<p><strong>Weekly 2016 年终回顾</strong><br />
http://javascriptweekly.com/issues/315<br />
http://react.statuscode.com/issues/17<br />
http://frontendfocus.co/issues/270<br />
http://nodeweekly.com/issues/168<br />
精选了今年值得关注的一些技术文章，如果你平时没太多时间关注技术，这期汇总绝对不能错过。另附：。</p>

<p><strong>TypeScript: the missing introduction</strong><br />
https://medium.com/@lavrton/optimizing-react-redux-store-for-high-performance-updates-3ae6f7f1e4c1<br />
The purpose of this article is to offer an introduction to how we can think about TypeScript, and its role in supercharging our JavaScript development. We will also try and come up with our own reasonable definitions for a lot of the buzzwords surrounding types and compilation.</p>

<p><strong>Front-End Developers Are Information Architects Too</strong><br />
https://24ways.org/2016/front-end-developers-are-information-architects-too/<br />
This is about a realisation I had a couple of years ago when I started to run an increasing amount of usability-testing sessions with people who have disabilities: that the structure, labelling, and connections that can be made in front-end code is information architecture. People’s ability to be successful online is unequivocally connected to the quality of the code that is written.</p>

<p><strong>One Sure-Fire Way to Improve Your Coding</strong><br />
https://changelog.com/posts/one-sure-fire-way-to-improve-your-coding<br />
The most obvious way to improve your coding is to write more code. Everybody knows that. However, another activity which I guarantee will improve your coding is the complete opposite of writing. I will state this as plainly as I possibly can: If you want to dramatically increase your programming skills you need to be reading other people’s code. In this article I will help you choose what to read and give you practical advice on how to go about reading it.</p>

<p><strong>Modern garbage collection</strong><br />
https://medium.com/@octskyward/modern-garbage-collection-911ef4f8bd8e#.pxuzlud1h<br />
The point of this article is not to convince you to use a different programming language or tool. But if you take one thing away, let it be this: garbage collection is a hard problem, really hard, one that has been studied by an army of computer scientists for decades. So be very suspicious of supposed breakthroughs that everyone else missed. They are more likely to just be strange or unusual tradeoffs in disguise, avoided by others for reasons that may only become apparent later.</p>

<p><strong>架构随聊</strong><br />
http://www.cnblogs.com/Zachary-Fan/p/ArchitectureChat.html<br />
“架构”是我们这行业种一个很常见的词，表明其必然也是经历了很长的岁月打磨所形成的一个词。架构的这个词出现的意义是什么？为了解决什么问题？只有把这2个问题想明白了，才能设计出一个良好的项目架构。程序设计和架构设计是互通的，每个人都可以从设计好一个程序往设计好一个系统架构前进。如果现在还无从下手的，我推荐大家可以从领域驱动设计这个概念入手，这是由业务为导向的设计方式，可以对培养设计出落地的架构有很大的帮助。</p>

<p><strong>[译]您的公司能从渐进式网页应用中受益吗</strong><br />
http://www.infoq.com/cn/articles/progressive-web-app-benefits<br />
文章从6个方面介绍了渐进式网页应用的优点，同时也列举了其面临的一些难题例如缺乏通用支持等。相关文章：</p>

<p><strong>webpack 构建性能优化策略小结</strong><br />
https://segmentfault.com/a/1190000007891318<br />
本文通过CommonsChunk、externals、DllPlugin、Happypack、uglify-parallel这五个点分别介绍了webpack在构建中可以进行性能优化的一些手段</p>

<p><strong>[译]构建稳固的、可升缩的CSS框架的八大原则</strong><br />
http://www.zcfy.cc/article/8-simple-rules-for-a-robust-scalable-css-architecture-2082.html<br />
这些原则都是我从这些年工作中所含盖的各个大型、复杂的web项目中总结出来的。而这些事情也都是我这些年被多次问到的，所以觉得将其用文档的形式叙述出来会是个不错的想法。</p>

<p><strong>redux applyMiddleware 原理剖析</strong><br />
http://www.jianshu.com/p/47887299cabb<br />
从源码更透彻解读 redux 中间件原理</p>

<p><strong>三十分钟学会SED和AWK</strong><br />
https://github.com/mylxsw/growing-up/blob/master/doc/%E4%B8%89%E5%8D%81%E5%88%86%E9%92%9F%E5%AD%A6%E4%BC%9ASED.md<br />
https://github.com/mylxsw/growing-up/blob/master/doc/%E4%B8%89%E5%8D%81%E5%88%86%E9%92%9F%E5%AD%A6%E4%BC%9AAWK.md<br />
随着 Node 的大范围使用，前端跟日志打交道的场景越来越多了，这时候 awk 和 sed 这两个命令就派上大用场了，这两篇教程值得认真学习下。</p>

<p><strong>Comparing MobX with NX observe</strong><br />
http://www.nx-framework.com/blog/public/mobx-vs-nx/<br />
主要介绍了NX observe 和MobX相比在特性、方法、性能等方面上的优点。</p>

<p><strong>Animating 2048 SVG nodes in React, Preact, Inferno, Vue, Angular 2, and CycleJS – a side-by-side comparison</strong><br />
https://swizec.com/blog/animating-svg-nodes-react-preact-inferno-vue/swizec/7311<br />
文中给出了一个由2048个svg节点组成的动画分别由React, Preact, Inferno, Vue, Angular2 以及 CycleJS 来实现的demo以及源码，看起来像是Inferno和Vue的性能更好，但Preact支持异步渲染，也受作者推崇</p>

<h2 id="section-1">新鲜货</h2>

<p><strong>What’s New In Python 3.6</strong><br />
https://docs.python.org/3.6/whatsnew/3.6.html<br />
喜欢 python 的同学可以关注下 3.6 版的新特性，另附：</p>

<p><strong>Weex Conf - 2017.1.12 - 报名</strong><br />
https://atf.alibaba.com/weex<br />
这次WeexConf我们将和业界分享以下亮点：
Weex最新的技术特性、技术工具、技术能力、技术趋势发布； Weex两次历经双11大考的实战经验及阿里生态系的业务经验； Weex团队更将首次集体亮相，畅谈从开源到加入Apache的心路历程。</p>

<p><strong>WePayUI</strong><br />
https://github.com/wepayui/wepayui<br />
WePayUI 由微信支付为服务商和商户量身打造，用于快速制作符合微信支付规范的Web页面，提升开发效率。WePayUI 基于 WeUI 拓展，包含基础组件和行业场景。</p>

<p><strong>腾讯大数据宣布开源第三代高性能计算平台Angel</strong><br />
http://www.leiphone.com/news/201612/H8mIdFZLUI6uWiG9.html<br />
Angel是腾讯完全自主的大数据平台，按照腾讯的说法无论是在性能还是实用性，Angel比其它平台都有很大的优势，但让业界为之震惊的还是腾讯将其开源，而且开源的力度也是腾讯过去2代计算平台无法比拟的。</p>

<p><strong>DynamicCocoa：滴滴 iOS 动态化方案</strong><br />
http://mp.weixin.qq.com/s/qRW_akbU3TSd0SxpF3iQmQ<br />
DynamicCocoa 可以让现有的 Objective-C 代码转换生成中间代码（JS），下发后动态执行，相比其他动态化方案，优势在于：使用原生技术栈：使用者完全不用接触到 JS 或任何中间代码，保持原生的 Objective-C 开发、调试方式不变；无需重写已有代码：已有 native 模块能很方便的变成动态化插件；语法支持完备性高：支持绝大多数日常开发中用到的语法，不用担心这不支持那不支持；支持 HotPatch：改完 bug 后直接从源码打出 patch，一站式解决动态化和热修复需求。另附：</p>

<p><strong>提升效率的利器</strong><br />
https://dbarobin.com/2016/12/21/liqi-of-robinwen/<br />
提升效率的利器，应该在经济承受范围以内毫不犹豫地拥有。工作以来，一贯的宗旨就是为美好的事物花费。这份清单，于己于人，或多或少有所帮助。倘若读者因此受益，实在是荣幸不已。</p>

<p><strong>FuseBox</strong><br />
https://github.com/fuse-box/fuse-box<br />
号称比 Webpack 快得多的打包工具</p>

<p><strong>用React、Redux、Immutable做俄罗斯方块</strong><br />
https://github.com/chvin/react-tetris/<br />
用react写的一款俄罗斯方块的游戏，玩一玩之余，也是一款不错的react练手项目</p>

<p><strong>Bootstrap 4 drops IE9 support and goes full flexbox</strong><br />
https://github.com/twbs/bootstrap/pull/21389<br />
Flexbox becomes the default layout option for Bootstrap 4.</p>

<p><strong>Writing web applications using only the Go Standard Library</strong><br />
https://golang.org/doc/articles/wiki/<br />
用 Go 语言写 Web 应用的新手入门文档</p>

<p><strong>2016年度最受欢迎中国开源软件评选</strong><br />
http://www.oschina.net/project/top_cn_2016<br />
看看今年有哪些好用的开源软件。</p>

<p><strong>Draft.js</strong><br />
https://github.com/facebook/draft-js<br />
Draft.js is a JavaScript rich text editor framework, built for React and backed by an immutable model.</p>

<p><strong>viewerjs</strong><br />
https://github.com/fengyuanchen/viewerjs<br />
一款图片浏览器的js库</p>

<p><strong>anypixel</strong><br />
https://github.com/googlecreativelab/anypixel<br />
AnyPixel.js is an open-source software and hardware library that makes it possible to use the web to create big, unusual, interactive displays.</p>

<p><strong>lightgallery.js</strong><br />
https://github.com/sachinchoolur/lightgallery.js<br />
Full featured JavaScript lightbox gallery.Fully responsive、Animated thumbnails、Mouse drag supports for desktops、Touch support for mobile devices…</p>

<p><strong>optimize-js</strong><br />
https://github.com/nolanlawson/optimize-js<br />
通过将立即执行的函数或者可能要被执行的函数包上括号，来保证这些代码在被js引擎解析时跳过pre-parse阶段，从而达到解析性能大幅提升的效果</p>

<p><strong>Flexbox Patterns</strong><br />
https://github.com/cjcenizal/flexbox-patterns<br />
Build awesome user interfaces with CSS flexbox. Examples and source code included.</p>

<p><strong>rxdb</strong><br />
https://github.com/pubkey/rxdb<br />
Reactive Offline-first Database with Sync, Schema, Mongo-Query, Encryption, LevelDown</p>

<h2 id="section-2">产品及其它</h2>

<p><strong>移动、前端融合新趋势：属于前端的时代即将来临</strong><br />
http://mp.weixin.qq.com/s?__biz=MjM5MDE0Mjc4MA==&amp;mid=2650995106&amp;idx=1&amp;sn=3fb607651f92e793e95f5a2a2e65c31b<br />
不管是 Web 前端、iOS，还是 Android，对大前端工程师来说，这是最好的时代。放在几年前 1/3 是大前端，2/3 是后端。而现在则是一半以上是大前端的人，这充分说明大前端的重要性。跨端技术，只是大前端开始。端与端技术之间相互学习和借鉴，这将成为未来前端技术最重要的创新来源。</p>

<p><strong>[译]我会这么多编码套路，你说我不是好开发？那怎样才是？</strong><br />
http://mp.weixin.qq.com/s?__biz=MjM5MDE0Mjc4MA==&amp;mid=2650995084&amp;idx=1&amp;sn=07271a4af7227290b5afb588e47f8951<br />
软件开发者使用编码套路学习新的软件开发技能确实有效。但当工作面对燃眉之急时，例如要达成最后期限、赶上发布日期、在遗留代码中解决故障等却往往力不从心。本文给出了成为一名好的开发者所应具备的技能，重点强调了转变训练方法的重要性，这些训练方法可完善我们在高强度和具有挑战性环境中工作的技能。</p>

<p><strong>[译] 小心负产出的开发者</strong><br />
https://segmentfault.com/a/1190000007864801<br />
人们很容易高估提前一个月上线的收益，而低估了这之后擦一年屁股的成本。生活中或许很少会遇到类似文中这样的负产出开发者，但类似的例子确实存在，说个最近发生的例子，有些新人开发者遇到问题后不做任何debug尝试就将问题抛向他的导师或者他所使用的产品的管理员，其实都是一些稍微看下文档或者分析下报错就能知道问题所在的小问题，对整个企业的研发效率来讲这就是负产出。也希望所有的开发者能培养自我解决问题的习惯而非做一名不爱思考的伸手党。</p>

<p><strong>复盘投资bilibili的过程，谈谈我对社区的看法</strong><br />
http://mp.weixin.qq.com/s/K0OGB0EfglcnYYR-eODOyg<br />
你会发现越是大的社区，其实越不会轻易定义自己的产品。越是拥有大规模用户的产品，表现就越简洁、越稳定，所谓大道至简。反观那些面面俱到，一个列表恨不得包含十几个功能的复杂产品，一定做不大。一个好的社区是建立在两种基本要素之上的——关系链和内容，只要创业者在这两条线中，能抓好一条就能生存。最终，这两种要素也会演变出不同类型的社区。</p>
---------------
<h1 id="#title_7" >8、文章： 腾讯游戏运维服务体系演变史</h1>
洪楷
[http://www.infoq.com/cn/articles/tencentgame-opsarchitect-history?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/tencentgame-opsarchitect-history?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/tencentgame-opsarchitect-history/zh/smallimage/logo (27).jpg"/><p>在面临高速发展的移动互联网游戏行业，对运维能力的要求变得越来越高，传统运维已经无法适应当下的节奏，如何随着时代演变而进步，如何能在危机中给自己创造机会，抓住要领才能坦然面对万变。这篇文章讲述了腾讯游戏运维服务体系演变史。</p> <i>By 洪楷</i>
---------------
<h1 id="#title_8" >9、区块链、云计算、大数据、人工智能、FinTech带来的挑战与机遇，中国技术开放日上海站精彩回顾</h1>
韩婷
[http://www.infoq.com/cn/news/2016/12/china-tech-day-shanghai?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2016/12/china-tech-day-shanghai?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>12月17日，中国技术开放日上海站成功举办，来自万达、维优区块链、京东云、恒生电子、平安科技、德国智能投顾Ginmon、众安科技的FinTech相关技术专家分享了他们对FinTech的看法和一线的工程实践。以下是分享内容的要点整理。</p> <i>By 韩婷</i>
---------------
<h1 id="#title_9" >10、Netflix Conductor：一个微服务编制引擎</h1>
Abel Avram
[http://www.infoq.com/cn/news/2016/12/netflix-conductor?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2016/12/netflix-conductor?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/news/2016/12/netflix-conductor/zh/headerimage/GettyImages-617775558.jpg"/><p>近日，Netflix宣布开源其微服务编制引擎Conductor，本文介绍了这个引擎的主要特性、架构图、以及任务类型。</p> <i>By Abel Avram</i> <i> Translated by 杨雷</i>
---------------
<h1 id="#title_10" >11、Dropbox是如何安全地存储用户密码的</h1>
薛命灯
[http://www.infoq.com/cn/news/2016/12/How-Dropbox-securely-passwords?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2016/12/How-Dropbox-securely-passwords?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>加密和破解是一场你追我赶的长期斗争。Dropbox作为一个应用范围很广的云存储解决方案，他们是如何保证用户的密码安全的呢？</p> <i>By 薛命灯</i>
---------------
<h1 id="#title_11" >12、2016年：DeepMind给人类带来了什么？</h1>
刘志勇
[http://www.infoq.com/cn/news/2016/12/2016-DeepMind-people?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2016/12/2016-DeepMind-people?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>自从DeepMind以4:1战胜围棋世界顶尖选手的李世石之后，就声名鹊起，经常登上各大媒体的头条。从那以后，人们就经常猜测人工智能的各种可能性。 DeepMind是一家位于英国的尖端科技公司，曾让Facebook、Google等巨头争相收购，最后Google在2014年1月以4亿英镑（6.66亿美元）击败Facebook成功收购了DeepMind。Google已经在机器学习和AI领域处于前沿地位，那为什么还要不惜代价斥巨资来收购DeepMind呢？究竟DeepMind能为Google带来怎样的价值？</p> <i>By 刘志勇</i>
---------------
<h1 id="#title_12" >13、人工智能周报（第五期）</h1>
戴民@TalkingData
[http://www.infoq.com/cn/news/2016/12/Artificial-Intelligence-Weekly-7?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2016/12/Artificial-Intelligence-Weekly-7?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>人工智能周报，为大家带来全球大数据产业及周边行业最新的咨询动态以及领袖观点。期待和大家一起不断找到海外数据技术和方案在国内落地的灵感，让每个大数据人同步在人工智能领域的世界前沿。</p> <i>By 戴民@TalkingData</i>
---------------
<h1 id="#title_13" >14、用深度神经网络生成以假乱真的“照片”</h1>
杨赛
[http://www.infoq.com/cn/news/2016/12/depth-neural-network-fake-photos?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2016/12/depth-neural-network-fake-photos?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>AI，人类再也无法阻挡的P图大师。</p> <i>By 杨赛</i>
---------------