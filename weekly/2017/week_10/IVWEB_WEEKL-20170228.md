## 文章索引
1、 <a href="#1为iot应用搭建devops管道" >为IoT应用搭建DevOps管道</a><br/>
2、 <a href="#2fex-技术周刊---2017/02/27" >FEX 技术周刊 - 2017/02/27</a><br/>
3、 <a href="#3文章-荷兰国际集团ing的it组织数字化升级之路" >文章： 荷兰国际集团ING的IT组织数字化升级之路</a><br/>
4、 <a href="#4文章-jvm为什么需要gc" >文章： JVM为什么需要GC</a><br/>
5、 <a href="#5beam晋升apache顶级项目" >Beam晋升Apache顶级项目</a><br/>
6、 <a href="#6文章-rxjava2实例解析" >文章： RxJava2实例解析</a><br/>
7、 <a href="#7eric-evansddd不是为完美主义者而生" >Eric Evans：DDD不是为完美主义者而生</a><br/>
8、 <a href="#8google云计算平台推出支持云端gpu加速服务的公开测试版" >Google云计算平台推出支持云端GPU加速服务的公开测试版</a><br/>
9、 <a href="#9高io型本地盘存储实例双十一中阿里如何将数据库性能提升100响应时间减少80" >高IO型本地盘存储实例：双十一中，阿里如何将数据库性能提升100%、响应时间减少80%？</a><br/>
10、 <a href="#10视频演讲-weex-极致性能优化" >视频演讲： Weex 极致性能优化</a><br/>
11、 <a href="#11the-art-of-calligraphy:-getting-started-and-lessons-learned" >The Art Of Calligraphy: Getting Started And Lessons Learned</a><br/><h1 id="#title_0" >1、为IoT应用搭建DevOps管道</h1>
Hrishikesh Barua
[http://www.infoq.com/cn/news/2017/02/setting-up-devops-iot?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/02/setting-up-devops-iot?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/news/2017/02/setting-up-devops-iot/zh/headerimage/GettyImages-2.jpg"/><p>在MSDN站点最近的一篇文章中，Daniel Meixler探讨了一个针对物联网（Internet of Things，IoT）应用的完整DevOps生命周期，用到了微软的框架和组件。这个理念稍作改动就可以泛化应用到其他IoT平台上。</p> <i>By Hrishikesh Barua</i> <i> Translated by 张卫滨</i>
---------------
<h1 id="#title_1" >2、FEX 技术周刊 - 2017/02/27</h1>

[http://fex.baidu.com/blog/2017/02/fex-weekly-27//](http://fex.baidu.com/blog/2017/02/fex-weekly-27//)
作者：nwind <br> <p>微信搜索『FEX』关注我们的公众号，及时获得最新资讯。</p>

<h2 id="section">深阅读</h2>

<p><strong>API Design Guide</strong><br />
https://cloud.google.com/apis/design/<br />
This is a general design guide for networked APIs. It has been used inside Google since 2014 and is the guide we follow when designing Cloud APIs and other Google APIs. It is shared here to inform outside developers and to make it easier for us all to work together. 另附：</p>

<p><strong>V8 is going to switch to a new compiler architecture after 5.8 branch cut</strong><br />
https://groups.google.com/forum/?#!msg/v8-dev/YXpjhVeHlbI/iiYlrF8vCgAJ<br />
The V8 team is currently working on a new compiler pipeline that will help us bring future speedups to real-world JavaScript. In the next few weeks we will replace our current compiler architecture based on a non-optimizing (FullCodeGen) and optimizing compiler (Crankshaft) pair with the combination of an interpreter (Ignition) and a new optimizing compiler ().</p>

<p><strong>Image Processing in Javascript</strong><br />
http://blog.webkid.io/image-processing-in-javascript/<br />
对各种 JS 图片处理库进行分析</p>

<p><strong>Node 6 at Wikimedia: Stability and substantial memory savings</strong><br />
https://blog.wikimedia.org/2017/02/17/node-6-wikimedia/<br />
Over the last years, Wikimedia engineers have built significant Node.js services to complement the venerable MediaWiki wiki platform implemented in PHP.  Over 10 such services are deployed in our production environment, powering features like VisualEditor, scientific formulae rendering, rich maps display and the REST content API. Individual services are built and owned by specific teams on top of the overall Node.js platform, which is maintained by the Wikimedia Services team. Recently, we upgraded our infrastructure to Node.js v6. This blog post describes how we did it, and what we learned in the process.</p>

<p><strong>The Future of Serverless Compute</strong><br />
https://www.infoq.com/articles/future-serverless<br />
As we approach the end of the early-adopter period, it’s an interesting exercise to put on our prediction goggles and contemplate where this movement is going next, how it’s getting there, and most importantly what changes we need from our organizations to support it. So, join me as we look at one possible future of Serverless compute.</p>

<p><strong>Cross-Site Request Forgery is dead!</strong><br />
https://scotthelme.co.uk/csrf-is-dead/<br />
After toiling with Cross-Site Request Forgery on the web for, well forever really, we finally have a proper solution. No technical burden on the site owner, no difficult implementation, it’s trivially simple to deploy, it’s Same-Site Cookies.</p>

<p><strong>使用Node.js实现文件流转存服务</strong><br />
https://zhuanlan.zhihu.com/p/25367269<br />
深入讲解如何使用Stream和Promise来实现一些复杂的功能</p>

<p><strong>Web 持续集成工作实践</strong><br />
http://div.io/topic/1929<br />
2015年10月我加入一家已盈利的创业公司，负责 Web 技术方向。创业过程中为了生存，都是拼快拼狠，难免选用猛糙快的工作方法。随着业务和团队不断扩大，面对的问题也越来越具挑战性。我逐步将一些自动化工具和方法引入到日常工作中，使团队获得一些收益。本文总结我这一年来做持续集成的获得经验教训。持续集成，项目之大事，研发团队负责人不可不察也。持续集成是通过平台串联各个开发环节，实现和沉淀工作自动化的方法。</p>

<p><strong>RxJS 入门指引和初步应用</strong><br />
https://zhuanlan.zhihu.com/p/25383159<br />
听徐叔给大家科普 RxJS，另附：</p>

<p><strong>Front-End Developer Handbook 2017</strong><br />
https://www.gitbook.com/book/frontendmasters/front-end-handbook-2017/details<br />
This is a guide that anyone could use to learn about the practice of front-end development. It broadly outlines and discusses the practice of front-end engineering: how to learn it and what tools are used when practicing it in 2017.The content of the handbook favors web technologies (HTML, CSS, DOM, and JavaScript) and those solutions that are directly built on top of these open technologies. The materials referenced and discussed in the book are either best in class or the current offering to a problem.</p>

<p><strong>Announcing the first SHA1 collision</strong><br />
https://security.googleblog.com/2017/02/announcing-first-sha1-collision.html<br />
Today, more than 20 years after of SHA-1 was first introduced, we are announcing the first practical technique for generating a collision. This represents the culmination of two years of research that sprung from a collaboration between the CWI Institute in Amsterdam and Google. We’ve summarized how we went about generating a collision below. As a proof of the attack, we are releasing two PDFs that have identical SHA-1 hashes but different content. 附：、
</p>

<p><strong>Code review checklist</strong><br />
https://ana-balica.github.io/2017/02/21/code-review-checklist/<br />
Over the last couple of months, I’ve developed my own internal code review checklist. I use it both for reviewing for own finished code and my teammates code complete tickets. It’s split up into 3 sections: code, automated testing and manual testing.</p>

<p><strong>A Detailed Introduction To Webpack</strong><br />
https://www.smashingmagazine.com/2017/02/a-detailed-introduction-to-webpack/<br />
JavaScript module bundling has been around for a while. RequireJS had its first commits in 2009, then Browserify made its debut, and since then several other bundlers have spawned across the Internet. Among that group, webpack has jumped out as one of the best. If you’re not familiar with it, I hope this article will get you started with this powerful tool.</p>

<p><strong>Node.js - Quality with Speed</strong><br />
https://nodejs.org/en/blog/community/quality-with-speed/<br />
One of the key tenets of the Node.js community is to allow change at a rapid pace in order to foster innovation and to allow Node.js to be used in a growing number of use cases. At the same time the community values quality. Newer versions of the runtime must be as good or better than earlier versions and must not un-intentionally break existing applications. Instead of trading off one for the other, the community looks for the path that allows us to maintain our rate of change while ensuring the required level of quality. Many of the activities undertaken by the community over the last year are in support of this goal. This is our take on how these activities fit together.</p>

<p><strong>A Functional Programmer’s Introduction to JavaScript (Composing Software)</strong><br />
https://medium.com/javascript-scene/a-functional-programmers-introduction-to-javascript-composing-software-d670d14ede30#.qzzkkd4py<br />
This is part of the “Composing Software” series on learning functional programming and compositional software techniques in JavaScript ES6+ from the ground up. 另附，阮一峰老师的：</p>

<p><strong>Deep dive CSS: font metrics, line-height and vertical-align</strong><br />
http://iamvdo.me/en/blog/css-font-metrics-line-height-and-vertical-align<br />
Line-height and vertical-align are simple CSS properties. So simple that most of us are convinced to fully understand how they work and how to use them. But it’s not. They really are complex, maybe the hardest ones, as they have a major role in the creation of one of the less-known feature of CSS: inline formatting context.</p>

<p><strong>Big Data Visualization with Meaning</strong><br />
https://alistapart.com/article/big-data-visualization-with-meaning<br />
As with all design, the approach we take when creating a user-minded visualization is based on the context and the constraints we have to work with. Good data visualizations—those with meaning—need to be accessible and human even though data is rarely described with those words.</p>

<p><strong>8 Best Practices for Mobile Form Design</strong><br />
http://www.uxmatters.com/mt/archives/2017/02/8-best-practices-for-mobile-form-design.php<br />
Designers have now been building mobile forms for a decade. But, as technology continues to go through metamorphoses and our understanding of users’ needs becomes more refined, good mobile form design is constantly evolving. In this article, I’ll provide eight best practices for mobile form design circa 2017.</p>

<p><strong>3 Key Uses for Animation in Mobile UI Design</strong><br />
https://uxplanet.org/3-key-uses-for-animation-in-mobile-ui-design-4d7c482dd84b#.q4mobfh1y<br />
With the quick development of technology, animation is less of a visual luxury and more of a functional requirement that users expect. Animation solves a lot of functional problems within interfaces and makes interfaces feel alive and truly responsive to the user. Let’s explore the key animation tactics that improve the functionality and emotional power of your mobile interface.</p>

<p><strong>What Does Being a Fullstack Developer Mean in 2017?</strong><br />
https://blog.qmo.io/what-does-being-a-fullstack-developer-mean-in-2017/<br />
What does fullstack mean? Everyone has their own definition. The problem is the breadth and depth of technologies have expanded so rapidly, fullstack developers are trying to play catch-up when everything is already red‑shifted by the time you’re looking at it. This problem is what makes “fullstack” a contested and controversial title.</p>

<p><strong>教你如何从0到1实现组件化架构</strong><br />
http://www.jianshu.com/p/7b4667cde80b<br />
iOS 组件化一种实现方法</p>

<p><strong>从技术角度谈一谈，我参与设计开发的手Q春节红包项目</strong><br />
http://mp.weixin.qq.com/s?__biz=MzA5Nzc4OTA1Mw==&amp;mid=2659599011&amp;idx=1&amp;sn=77dcd934fcff0f7688c999cb65b8a310<br />
本文将会详细介绍手Q春节红包项目的设计、容灾、运维、架构以及总结。</p>

<p><strong>关于技术选型的那些事儿</strong><br />
http://mp.weixin.qq.com/s?__biz=MjM5MDE0Mjc4MA==&amp;mid=2650995506&amp;idx=1&amp;sn=4dbec250c8e24f895ca6ce4833f9444e<br />
滴滴小巴业务技术负责人的经验之谈，技术选型关键需要思考三个角度：技术、业务和人。</p>

<h2 id="section-1">新鲜货</h2>

<p><strong>Safari Technology Preview 24</strong><br />
https://webkit.org/blog/7423/release-notes-for-safari-technology-preview-24/<br />
挺多值得关注的新特性的，比如：Added <link preload="" /> as an experimental feature、Implemented dynamic import operator. 另附：</p>

<p><strong>Announcing TypeScript 2.2</strong><br />
https://blogs.msdn.microsoft.com/typescript/2017/02/22/announcing-typescript-2-2/<br />
用 TS 的同学可以关注下新特性</p>

<p><strong>Incident report on memory leak caused by Cloudflare parser bug</strong><br />
https://blog.cloudflare.com/incident-report-on-memory-leak-caused-by-cloudflare-parser-bug/<br />
Cloudflare to report a security problem with our edge servers. He was seeing corrupted web pages being returned by some HTTP requests run through Cloudflare. 附：</p>

<p><strong>Introducing Netflix Stethoscope</strong><br />
http://techblog.netflix.com/2017/02/introducing-netflix-stethoscope.html<br />
Netflix is pleased to announce the open source release of Stethoscope, our first project following a User Focused Security approach. Stethoscope is a web application that collects information for a given user’s devices and gives them clear and specific recommendations for securing their systems.</p>

<p><strong>Boundless</strong><br />
https://github.com/enigma-io/boundless<br />
Boundless is a UI toolkit that was conceived to abstract away difficult interface patterns. It follows three main guidelines: Performance is mandatory, not a nice-to-have; Components should be as customizable as possible; Components should be as accessible as possible (falling back to WAI-ARIA attributes when necessary.)</p>

<p><strong>AR.js - Efficient Augmented Reality for the Web using ARToolKit</strong><br />
https://github.com/jeromeetienne/AR.js<br />
Efficient Augmented Reality for the Web using ARToolKit - 60fps on mobile!</p>

<p><strong>axios</strong><br />
https://github.com/mzabriskie/axios<br />
Promise based HTTP client for the browser and node.js</p>

<p><strong>unfetch</strong><br />
https://github.com/developit/unfetch<br />
Bare minimum fetch polyfill in 500 bytes.</p>

<p><strong>slim.js</strong><br />
https://github.com/eavichay/slim.js<br />
Slim.js is a lightning fast library for development of native web-components. No black magic. It uses javascript’s inheritance mechanism to boost up HTML elements with superpowers.</p>

<p><strong>各个编程语言都有哪些「黑点」</strong><br />
https://www.zhihu.com/question/53584423<br />
一个顾客走进一家牛排店，要一块牛排：C：服务员牵来一头牛，给了顾客一把大刀，笑道，请享用…</p>

<p><strong>Hero Patterns</strong><br />
http://www.heropatterns.com/<br />
A collection of repeatable SVG background patterns for you to use on your web projects.</p>

<p><strong>Upspin - A framework for naming everyone’s everything</strong><br />
https://github.com/upspin/upspin<br />
Upspin is an experimental project to build a framework for naming and sharing files and other data securely, uniformly, and globally: a global name system of sorts. It is not a file system, but a set of protocols and reference implementations that can be used to join things like file systems and other storage services to the name space.</p>

<h2 id="section-2">产品及其它</h2>

<p><strong>微软首款小程序「微软小蜜」</strong><br />
http://mp.weixin.qq.com/s?__biz=MzIwOTQ4NTkwOA==&amp;mid=2247483700&amp;idx=1&amp;sn=524d4102f38e934bee232e544706ca68<br />
微软中国在微信上发布了一款小程序 -「微软小蜜」预览版，它利用微软亚洲研究院的图片认知服务。通过识别并深度学习，小程序提取图片中的文字形状等元素，一键生成可编辑的PPT文件。简单的说，手机上的截图，街边的广告，会议上的幻灯片，只要通过微软小秘，都能快速保存为“可编辑“的PPT文档。</p>

<p><strong>从京东11万快递小哥与1万白领，看到的真实互联网世界</strong><br />
http://mp.weixin.qq.com/s?__biz=MzA3Mjc3OTk5Nw==&amp;mid=2653651124&amp;idx=1&amp;sn=0d842a266e0d7f388fc4b6c87babe9ba<br />
互联网时代的中国，城市与乡村，白领与蓝领，二元对立又相互依赖。面对这样一个复杂而庞大的市场，该如何做产品推广？知名创业者、前腾讯资深产品经理梁宁在读完《创京东》之后，给出了自己的看法——当你要推一个产品的时候，是不是可以更直率地想，目标是京东的1万白领，还是11万蓝领？</p>

<p><strong>为什么网易系擅长做产品</strong><br />
http://tech.qq.com/a/20170223/026608.htm<br />
由谙熟业务，比高层更年轻，更懂用户市场的中层来掌握做产品的实权。几乎没有KPI文化，产品做得好与坏，主要靠产品经理的内心热情来驱动，不靠金钱驱动，更不会为了完成数字而打乱节奏。没有产品大战略，不参与刚正面的烧钱竞争，网易的产品策略只能以中小投入为主，不去赤裸裸地拼资源，便格外注重创新与体验。</p>

<p><strong>当我在排版时，我在思考什么</strong><br />
http://mp.weixin.qq.com/s?__biz=MjM5ODQwMjA4MA==&amp;mid=2649293721&amp;idx=1&amp;sn=d42f1227ea0ebbc0216a492478edccb7<br />
你可能见过很多关于微信公众号排版的教程，告诉你应该用多少字号、用什么颜色、行距应该设置为多少，大部分教程或许对想速成或直接找一个 todolist 做工作交差的人来说，是有效的。然而，真正要做好排版，并不只是需要获得别人给的 todolist，而是理解排版背后的原理。</p>

<p><strong>Microsoft’s new AI can code by stealing bits of code from other software</strong><br />
http://www.businessinsider.com/microsoft-cambridge-ai-deepcoder-programs-software-combining-stolen-code-2017-2<br />
微软和剑桥大学正开发具有人工智能的编程软件 DeepCoder，它可以从把其他应用的代码拿过来给自己用。微软首先训练一个神经网络来检测程序的性质，然后将该神经网络的预测输出代入到编程社区的高级搜索工具中。之后运用这种神经网络的 DeepCoder 可以通过现有软件获取的代码拼接在一起写出新程序。此外，DeepCoder 使用机器学习来清理源代码数据库，并对它们按照有用性进行排序。</p>
---------------
<h1 id="#title_2" >3、文章： 荷兰国际集团ING的IT组织数字化升级之路</h1>
Mary Poppendieck
[http://www.infoq.com/cn/articles/path-of-ing-it-organization-digital-upgrade?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/path-of-ing-it-organization-digital-upgrade?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/path-of-ing-it-organization-digital-upgrade/zh/smallimage/logo-2 (1).jpg"/><p>2010年的初试实验后，ING的IT部门开始用敏捷开发团队替代瀑布团队。短期之内，这种方式显然并不可能对银行的发展带来根本性影响，但它一定会在某种程度上提升持续交付的反馈效率和DevOps团队稳定性。</p> <i>By Mary Poppendieck</i> <i> Translated by 曹倩芸</i>
---------------
<h1 id="#title_3" >4、文章： JVM为什么需要GC</h1>
麦克周
[http://www.infoq.com/cn/articles/why-jvm-need-gc?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/why-jvm-need-gc?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/why-jvm-need-gc/zh/smallimage/logo 112.jpg"/><p>社区内有人发起了一个讨论，认为JVM是否一定需要GC？他们认为应用程序的回收目标是构建一个仅用来处理内存分配，而不执行任何真正的内存回收操作的 GC，即仅当可用的 Java 堆耗尽的时候，才进行顺序的 JVM 停顿操作。 首先需要理解为什么需要GC。应用程序所应对的业务越来越庞大、复杂，用户越来越多，没有GC就不能保证应用程序正常进行，而经常造成STW的GC又跟不上实际的需求，所以才会不断地尝试对GC进行优化。 社区的需求是尽量减少对应用程序的正常执行干扰，这也是业界目标。Oracle在JDK7时发布G1 GC的目的是为了减少应用程序停顿发生的可能性，让我们通过本文来了解G1 GC所做的工作。</p> <i>By  麦克周</i>
---------------
<h1 id="#title_4" >5、Beam晋升Apache顶级项目</h1>
Dylan Raithel
[http://www.infoq.com/cn/news/2017/02/apache-beam-top-level?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/02/apache-beam-top-level?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Beam渡过了孵化期并成功地晋升Apache顶级项目，Google支持并贡献给开源社区整合更多的数据处理框架。</p> <i>By Dylan Raithel</i> <i> Translated by 麦克周</i>
---------------
<h1 id="#title_5" >6、文章： RxJava2实例解析</h1>
Victor Grazi
[http://www.infoq.com/cn/articles/rxjava2-by-example?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/rxjava2-by-example?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/rxjava2-by-example/zh/headerimage/5.jpg"/><p> 在高并发编程范式的发展过程中，响应式编程最为抢眼。它是处理异步数据流的一种规范，为数据流的转换和聚合以及数据流的控制管理提供了工具支持，让考量程序整体设计的工作变得简单。本文中，我们将根据例子循序渐进地学习RxJava2。</p> <i>By Victor Grazi</i> <i> Translated by 薛命灯 Rays</i>
---------------
<h1 id="#title_6" >7、Eric Evans：DDD不是为完美主义者而生</h1>
Jan Stenberg
[http://www.infoq.com/cn/news/2017/02/ddd-perfectionists?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/02/ddd-perfectionists?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/news/2017/02/ddd-perfectionists/zh/headerimage/GettyImages-518958102-copy.jpg"/><p>追寻完美设计是从一开始就伴随着领域驱动设计（DDD）的常见问题，但DDD不是为完美主义者而生的。最近在阿姆斯特丹的DDD欧洲会议上，Eric Evans在其演讲中指出，为了停止这种追求，你需要对如何创建设计良好但并不完美的软件有一些概念。</p> <i>By Jan Stenberg</i> <i> Translated by 汪欣</i>
---------------
<h1 id="#title_7" >8、Google云计算平台推出支持云端GPU加速服务的公开测试版</h1>
刘志勇
[http://www.infoq.com/cn/news/2017/02/Google-cloud-GPU?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/02/Google-cloud-GPU?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Google曾在2016年11月16日宣布，将于2017年初通过其云端（Google Cloud Platform）的公共云发布图形处理器（GPU）支持的虚拟机（VM）实例。</p> <i>By 刘志勇</i>
---------------
<h1 id="#title_8" >9、高IO型本地盘存储实例：双十一中，阿里如何将数据库性能提升100%、响应时间减少80%？</h1>
木环
[http://www.infoq.com/cn/news/2017/02/IO-ali-data-warehouse?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/02/IO-ali-data-warehouse?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>随着硬件技术的发展，硬件自身性能越来越高，存储软件的瓶颈也就越发明显。为了解决I/O性能上的痛点，阿里云开始基于NVMe 协议和英特尔开源项目SPDK研发高IO存储实例。</p> <i>By  木环</i>
---------------
<h1 id="#title_9" >10、视频演讲： Weex 极致性能优化</h1>
冯成晓
[http://www.infoq.com/cn/presentations/weex-ultimate-performance-optimization?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/weex-ultimate-performance-optimization?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/weex-ultimate-performance-optimization/zh/mediumimage/fengchengxiao270.jpg"/><p>作为新一代移动动态化解决方案，Weex 不仅仅希望通过一套代码多端运行和低成本的前端接入来提升开发者体验，同时也一直致力于通过提高加载和渲染性能来提升用户体验。
本次分享将主要介绍 Weex 在性能优化体系上的独特之处，介绍优化过程中遇到的困难、踩过的坑以及对应的解决方案。
主要会从以下几个方面进行深入的剖析:
渲染流程优化：node & tree 流式渲染、分段渲染、异步渲染；
组件设计优化：list、text 等组件在设计上如何保证低内存、高帧率的性能表现；
JS 下载优化：利用预加载及网络优化，抹平 JS 下载时间；
性能最佳实践：遵循一些最佳实践， 让 Weex 开发的 App 拥有丝般顺滑的用户体验；
性能现状与未来： Weex 的性能现状、与 React Native 的对比以及未来的优化方向。</p> <i>By 冯成晓</i>
---------------
<h1 id="#title_10" >11、The Art Of Calligraphy: Getting Started And Lessons Learned</h1>
Anastasia Shevchuk
[https://www.smashingmagazine.com/2017/02/art-calligraphy-getting-started-lessons-learned/](https://www.smashingmagazine.com/2017/02/art-calligraphy-getting-started-lessons-learned/)
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
</table><p>Typography is a primary element of composition. Being a designer, I pay a lot of attention to its quality. Operating Photoshop is easy for me; however, to level up my skills, I am always learning to work with letters, using my hands, without any computer programs.</p>

<figure><</figure>

<p>The first time I took a calligraphy course was about a year ago, and the decision was quite hard. I was sure that it would be painstaking and that I would need excellent handwriting to learn this art. How mistaken I was!</p><p>The post .</p>
---------------