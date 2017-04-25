## 文章索引
1、 <a href="#1fex-技术周刊---2017/04/24" >FEX 技术周刊 - 2017/04/24</a><br/>
2、 <a href="#2文章-transcrypt剖析python转javascript编译器" >文章： Transcrypt：剖析Python转JavaScript编译器</a><br/>
3、 <a href="#3微软宣布azure-service-fabric-sdk开源" >微软宣布Azure Service Fabric SDK开源</a><br/>
4、 <a href="#4文章-如何从业务和平台两方面入手设计更具可靠性的微服务" >文章： 如何从业务和平台两方面入手，设计更具可靠性的微服务</a><br/>
5、 <a href="#5谷歌的fuchsia一个新的操作系统" >谷歌的Fuchsia：一个新的操作系统</a><br/>
6、 <a href="#6与michael-nir谈论使团队高效的执行目标" >与Michael Nir谈论使团队高效的执行目标</a><br/>
7、 <a href="#7slack从javascript切换至typescript" >Slack从JavaScript切换至TypeScript</a><br/>
8、 <a href="#8亚马逊增加了对aurora的跨区域和加密复制支持" >亚马逊增加了对Aurora的跨区域和加密复制支持</a><br/>
9、 <a href="#9谷歌的招聘工具和启示" >谷歌的招聘工具和启示</a><br/>
10、 <a href="#10视频演讲-以创业的思维经营开源项目" >视频演讲： 以创业的思维经营开源项目</a><br/>
11、 <a href="#11文章-三位专家谈大数据工程" >文章： 三位专家谈大数据工程</a><br/>
12、 <a href="#12applications-of-machine-learning-for-designers" >Applications Of Machine Learning For Designers</a><br/><h1 id="#title_0" >1、FEX 技术周刊 - 2017/04/24</h1>

[http://fex.baidu.com/blog/2017/04/fex-weekly-24//](http://fex.baidu.com/blog/2017/04/fex-weekly-24//)
作者：zhangbobell <br> <p>微信搜索『FEX』关注我们的公众号，及时获得最新资讯。</p>

<p><strong>F8 2017</strong><br />
https://www.fbf8.com/<br />
附：<br />
<br />
<br />
<br />
。<br />
值得前端关注的：<br />
<br />
<br />
</p>

<p><strong>[报名]2017 JavaScript中国开发者大会</strong><br />
http://2017.jsconf.cn/
7月15至16日在上海举行，赶紧抢票吧。</p>

<h2 id="section">深阅读</h2>

<p><strong>LinuxKit: A Toolkit for Building Secure, Lean and Portable Linux Subsystems</strong><br />
https://blog.docker.com/2017/04/introducing-linuxkit-container-os-toolkit/<br />
LinuxKit includes the tooling to allow building custom Linux subsystems that only include exactly the components the runtime platform requires. All system services are containers that can be replaced, and everything that is not required can be removed. All components can be substituted with ones that match specific needs. It is a kit, very much in the Docker philosophy of batteries included but swappable.</p>

<p><strong>Hard-won lessons: Five years with Node.js</strong><br />
https://blog.scottnonnenberg.com/hard-won-lessons-five-years-with-node-js/<br />
After five years working with Node.js, I’ve learned a lot. I’ve already shared a few stories, but this time I wanted to focus on the ones I learned the hard way. Bugs, challenges, surprises, and the lessons you can apply to your own projects!</p>

<p><strong>Improving Startup Time</strong><br />
http://blog.atom.io/2017/04/18/improving-startup-time.html<br />
Over the last months, the Atom team has been working hard on improving one of the aspects of the editor our users care about the most: startup time. We will first provide the reader with some background about why reducing startup time is a non-trivial task, then illustrate the optimizations we have shipped in Atom 1.17 (currently in beta) and, finally, describe what other improvements to expect in the future.</p>

<p><strong> To Start Using CSS Custom Properties</strong><br />
https://www.smashingmagazine.com/2017/04/start-using-css-custom-properties/<br />
Today, CSS preprocessors are a standard for web development. One of the main advantages of preprocessors is that they enable you to use variables. As a silver bullet for these and other problems, the community invented CSS custom properties. Essentially, these look and work like CSS variables, and the way they work is reflected in their name. Custom properties are opening new horizons for web development.</p>

<p><strong>When Does a Project Need React</strong><br />
https://css-tricks.com/project-need-react/<br />
I’m just going to use React as a placeholder here for kinda large JavaScript framework thingies. Vue, Ember, Svelte… whatever. I understand they aren’t all the same, but when to reach for them I find equally nebulous. Here’s my take.<br />
另附：</p>

<p><strong>The Benefits of Server Side Rendering Over Client Side Rendering</strong><br />
https://medium.com/walmartlabs/the-benefits-of-server-side-rendering-over-client-side-rendering-5d07ff2cefe8<br />
Most of our pages on walmart.com are using server side rendering (henceforth SSR) with only a few unique exceptions.
We are using server side rendering for two reasons: Performance benefit for our customers; Consistent SEO performance.</p>

<p><strong>Modernizing the DOM tree in Microsoft Edge</strong><br />
https://blogs.windows.com/msedgedev/2017/04/19/modernizing-dom-tree-microsoft-edge/#rJS15V2JDdrG8i26.97  <br />
The DOM is the foundation of the web platform programming model, and its design and performance impacts the rest of the browser pipeline. However, its history and evolution is far from a simple story. <br />
另附：</p>

<p><strong>单页应用的数据流方案探索</strong><br />
https://zhuanlan.zhihu.com/p/26426054<br />
民工叔叔在 Qcon 的分享：过去的3年里，前端开发领域可谓风起云涌，革故鼎新。除了开发语言的语法增强和工具体系的提升之外，大部分人开始习惯几件事：组件化、MDV（Model Driven View）。所谓组件化，很容易理解，把视图按照功能，切分为若干基本单元，所得的东西就可以称为组件，而组件又可以一级一级组合而成复合组件，从而在整个应用的规模上，形成一棵倒置的组件树。这种方法论历史久远，其实现方式或有瑜亮，理念则大同小异。而MDV，则是对很多低级DOM操作的简化，把对DOM的手动修改屏蔽了，通过从数据到视图的一个映射关系，达到了只要操作数据，就能改变视图的效果。</p>

<p><strong>一种几乎无法被检测到的Punycode钓鱼攻击，Chrome、Firefox和Opera等浏览器都中招</strong><br />
http://www.freebuf.com/news/132240.html  <br />
使用肉眼没法区分的 unicode 域名</p>

<p><strong>CSS Grid布局这样玩</strong><br />
https://www.w3cplus.com/css3/playing-with-css-grid-layout.html<br />
自从去年下半年开始，CSS Grid布局的相关教程在互联网上就铺天盖地，可谓是声势浩大。就针对于Web布局而言，个人认为Grid布局将是Web布局的神器，它改变了以往任何一种布局方式或者方法。不管以前的采用什么布局方法都可以说是一维的布局方式，而Grid最大的特色，采用了二维布局。@Rachel Andrew也一直致力于完善Grid的规范。就我个人而言，我也一直在不断的关注这个布局利器的相关更新，自从最初规范的出来，到目前规范的完善。在站上也不断的在更新CSS Grid布局的使用。虽然这方向的教程已经很多了，但各有千秋，我追求以最简单，最直接的方式来阐述它的使用方式方法。让初学者能尽快的掌握其使用规则。</p>

<p><strong>Node CTC Votes to Delay Node 8.x To May 30th</strong><br />
https://github.com/nodejs/CTC/issues/99<br />
Following a [discussion] on how Node will deal with key changes to the V8 JavaScript engine, the CTC voted to delay Node v8 until the end of May.</p>

<p><strong>Announcing Free Node.js Monitoring &amp; Debugging with Trace</strong><br />
https://blog.risingstack.com/announcing-free-node-js-monitoring-and-debugging/<br />
We launched  a year ago with the intention of helping developers looking for a Node.js specific APM which is easy to use and helps with the most difficult aspects of building Node projects, like: finding memory leaks in a production environment, profiling CPU usage to find bottlenecks, tracing distributed call-chains, avoiding security leaks &amp; bad npm packages.</p>

<p><strong>The Definitive Guide to Object Streams in Node.js</strong><br />
https://community.risingstack.com/the-definitive-guide-to-object-streams-in-node-js/<br />
Node.js Streams come with a great power: You have an asynchronous way of dealing with input and output, and you can transform data in independent steps. In this tutorial, I’ll walk you through the theory, and teach you how to use object stream transformables, just like Gulp does.</p>

<p><strong>Me and SVG</strong><br />
http://codepen.io/AmeliaBR/post/me-and-svg<br />
For the past three-and-a-half years of my life, I have devoted a large portion of my time and creativity to the creature known as SVG. Whether that was a good choice or not, I do not know. But here I am. However, I’m not really sure where I’m going to go next. And I’m even less sure where SVG is going next. So I sat down to write out my thoughts about the future of SVG, and instead wrote about how I came to be so tangled up with it.</p>

<p><strong>PhotoScan: Taking Glare-Free Pictures of Pictures</strong><br />
https://research.googleblog.com/2017/04/photoscan-taking-glare-free-pictures-of.html<br />
One of the key features of PhotoScan is the ability to remove glare from prints, which are often glossy and reflective, as are the plastic album pages or glass-covered picture frames that host them. To create this feature, we developed a unique blend of computer vision and image processing techniques that can carefully align and combine several slightly different pictures of a print to separate the glare from the image underneath.</p>

<p><strong>PHP 7 Virtual Machine</strong><br />
http://nikic.github.io/2017/04/14/PHP-7-Virtual-machine.html  <br />
深入解读 PHP 7 虚拟机的实现原理</p>

<h2 id="section-1">新鲜货</h2>

<p><strong>Welcome home to the new Google Earth</strong><br />
https://blog.google/products/earth/welcome-home-new-google-earth/<br />
Today we’re introducing a brand-new version of Google Earth—on the web and Android—two years in the making. With the new Earth, we want to open up different lenses for you to see the world and learn a bit about how it all fits together; to open your mind with new stories while giving you a new perspective on the locations and experiences you cherish. 体验 Web 版 https://earth.google.com/web/</p>

<p><strong>Firefox faster and more stable with the first big bytes of Project Quantum</strong><br />
https://blog.mozilla.org/blog/2017/04/19/first-big-bytes-project-quantum/<br />
In case you missed our .</p>

<p><strong>Google - WebVR Experiments</strong><br />
https://www.webvrexperiments.com/<br />
To explore what’s possible with WebVR, we’re launching WebVR Experiments, a showcase of the amazing experiences developers are already building.</p>

<p><strong>Litho</strong><br />
http://fblitho.com/docs/getting-started  <br />
Facebook 新推出的 Android UI 框架</p>

<p><strong>React Move</strong><br />
https://github.com/tannerlinsley/react-move<br />
Beautifully and deterministically animate anything in react.</p>

<p><strong>Recycle V2 - A functional and reactive library for React</strong><br />
https://github.com/recyclejs/recycle/<br />
Convert functional/reactive object description into React component. You don’t need another UI framework if you want to use RxJS.</p>

<p><strong>Chroma.js</strong><br />
https://github.com/gka/chroma.js<br />
Chroma.js is a tiny JavaScript library (14kB) for all kinds of color conversions and color scales.</p>

<p><strong>Web魔幻线条 - curvejs</strong><br />
https://github.com/AlloyTeam/curvejs<br />
curvejs 中文读[“克js”]，是腾讯AlloyTeam打造的一款魔幻线条框架，让线条成为一名优秀的舞者，让线条们成为优秀的舞团，HTML5 Canvas就是舞台。</p>

<p><strong>pwmetrics</strong><br />
https://github.com/paulirish/pwmetrics<br />
Progressive web metrics at your fingertipz. CLI tool and lib to gather performance metrics via Lighthouse. IN BETA.</p>

<p><strong>Tamper Chrome</strong><br />
https://github.com/google/tamperchrome<br />
Tamper Chrome is a Chrome extension that allows you to modify HTTP requests on the fly and aid on web security testing. Tamper Chrome works across all operating systems (including Chrome OS).</p>

<p><strong>68 Resources To Help You To Create Programming Languages</strong><br />
https://tomassetti.me/resources-create-programming-languages/<br />
Creating a programming language is one of the most fascinating challenge you can dream of as a developer. We organized the resources around the three stages in the creation of a programming language: design, parsing, and execution.</p>

<p><strong>tiny-care-terminal</strong><br />
https://github.com/notwaldorf/tiny-care-terminal<br />
This is a little dashboard that tries to take care of you when you’re using your terminal. It tells you cute, self care things, and tries not to stress you out.</p>

<p><strong>Java 微服务框架新选择：Spring 5</strong><br />
https://mp.weixin.qq.com/s?__biz=MzAwMDU1MTE1OQ==&amp;mid=2653548625&amp;idx=1&amp;sn=04467345d35dcf057d4bfe8f483c4bdb<br />
Spring 5 引入了新的编程范式用来开发小型的、轻量级的、微服务式 Web应用程序。 我们显式得定义请求路由器和请求处理函数，在完全不需要应用上下文的情况下快速运行并部署。</p>

<p><strong>那些让人惊艳的Python库</strong><br />
https://mp.weixin.qq.com/s?__biz=MzI3NTAxNjE0Ng==&amp;mid=2650007219&amp;idx=1&amp;sn=de4f7fc20a12499cceecf95abb44b757<br />
每一门技艺都是入门容易熟悉难，越是了解，越是感觉到自己的欠缺，在python博大精深的世界里，这些蔚为壮观的python库，也只能算是沧海一粟。</p>

<h2 id="section-2">产品及其它</h2>

<p><strong>为什么说顺丰错过了成为更伟大企业的机会</strong><br />
https://mp.weixin.qq.com/s?__biz=MjM5OTM5OTAyMQ==&amp;mid=2654431175&amp;idx=2&amp;sn=18ef9ca322b4cf6e068aababda54b9fc<br />
今天的顺丰尽管高享两千多亿的估值。光鲜亮丽的财报难掩隐忧：B2B 商务件收入和利润增长滞后；在最热闹的电商市场被边缘化。这影响顺丰长远增长，也将决定顺丰行业地位。</p>

<p><strong>聊聊【折腾】的重要性</strong><br />
https://program-think.blogspot.com/2017/04/The-Importance-of-Zheteng.html<br />
“折腾”指的是：在你【不熟悉】的领域中干某些事情（如果是你【熟悉】的领域，那属于“轻车熟路”，不能算“折腾”）；这些事情通常带有某种“探索/钻研”的性质（通常颇费周折）；这些事情通常要耗费一定的时间和精力（能很快搞定的，就不能算“折腾”）；这些事情通常具有不确定的结果（你不清楚是否能得到期望的结果）。</p>

<p><strong>这一波知识付费：一个机会，两种能力，三个要点</strong><br />
https://mp.weixin.qq.com/s?__biz=MjM5NDUyOTAwOA==&amp;mid=2652915461&amp;idx=1&amp;sn=ff6f41377960bfe2f6585f3bb8c5b1fa<br />
“知识付费”其实可以算作是“内容付费”的一个最重要的分支，在这一波浪潮中，表现最抢眼的，也是“知识付费”，包括三节课在做的事，也与“知识付费”更近，因此，今日此文，我会更侧重于“知识付费”产品的角度来谈一些我自己的思考和见解，当中也会有一些观点和逻辑可以广泛适用于更为广阔的“内容付费”范畴。</p>

<p><strong>Ptmind铂金智慧：像Excel一样，做一款人人都能用的数据产品</strong><br />
https://mp.weixin.qq.com/s?__biz=MzI3MDUyNjM2Ng==&amp;mid=2247484685&amp;idx=1&amp;sn=10d90a64609cec343014a3548df3373d<br />
在企业业务体系中，对数据分析有越来越多需求的销售人员、市场人员。所谓的普适性就是大家能够普遍的使用，实际上，目前世界上唯一普适性的数据工具只有一个，那就是excel，Ptmind要做的就是互联网数据分析领域的Excel。没有任何事情能够阻挡大家对数据价值的认可和利用，数据已经成为每个人都触手可及的，像空气和水一般的存在。</p>

<p><strong>The Art of Writing One-Sentence Product Descriptions</strong><br />
https://medium.dave-bailey.com/the-magic-formula-to-describe-a-product-in-one-sentence-175ce38619c7<br />
A look back at early interviews with Facebook and Uber CEOs illustrates an ingenious way to communicate hard-to-describe products. Your product will only come up in conversations when it’s perceived as being relevant to that conversation. Viral products tend to have a “lead feature”.</p>
---------------
<h1 id="#title_1" >2、文章： Transcrypt：剖析Python转JavaScript编译器</h1>
Jacques de Hooge
[http://www.infoq.com/cn/articles/transcrypt-python-javascript-compiler?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/transcrypt-python-javascript-compiler?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/transcrypt-python-javascript-compiler/zh/headerimage/GettyImages-499691816.jpg"/><p>在Web前端，开发千篇一律地使用了JavaScript。Transcrypt的Python转JavaScript编译器是一个相对较新的开源项目，意在使用大小近似的文件以JavaScript的速度执行Python 3.6。本文中，Jacques de Hooge介绍了构建源码到源码的编译器（transpiler）中的需求，以及Transcrypt是如何构建满足这些需求的。</p> <i>By Jacques de Hooge</i> <i> Translated by Rays</i>
---------------
<h1 id="#title_2" >3、微软宣布Azure Service Fabric SDK开源</h1>
Pierre-Luc Maheu
[http://www.infoq.com/cn/news/2017/04/service-fabric-sdk-open-source?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/04/service-fabric-sdk-open-source?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>微软最近宣布Azure Service Fabric SDK的源代码已经开源。Azure Service Fabric是一个分布式平台，用于微服务的打包、部署和管理。SDK暴露了Service Fabric平台中与.NET应用集成的Service Fabric API。</p> <i>By Pierre-Luc Maheu</i> <i> Translated by 张卫滨</i>
---------------
<h1 id="#title_3" >4、文章： 如何从业务和平台两方面入手，设计更具可靠性的微服务</h1>
李林锋
[http://www.infoq.com/cn/articles/design-a-more-reliable-micro-service?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/design-a-more-reliable-micro-service?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/design-a-more-reliable-micro-service/zh/smallimage/heinz-kabutz-article-icon.jpg"/><p>微服务在带来众多好处的同时，也让系统发生故障的概率提高了很多。如何从业务和平台两方面入手，提升微服务的可靠性，作者给出了非常翔实的建议。</p> <i>By 李林锋</i>
---------------
<h1 id="#title_4" >5、谷歌的Fuchsia：一个新的操作系统</h1>
Nur Hussein
[http://www.infoq.com/cn/news/2017/04/Fuchsia-Google-OS?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/04/Fuchsia-Google-OS?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>本文介绍了谷歌正在开发的新开源操作系统Fuchsia。</p> <i>By Nur Hussein</i> <i> Translated by 孙薇</i>
---------------
<h1 id="#title_5" >6、与Michael Nir谈论使团队高效的执行目标</h1>
Stéphane Wojewoda, Shane Hastie
[http://www.infoq.com/cn/news/2017/04/nir-high-team-performance?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/04/nir-high-team-performance?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Michael Nir在敏捷游戏大会上发表了演讲“为Scrum Master带来一剂良方：使团队高效的执行目标”。InfoQ对Michael进行了访谈，讨论了关于执行目标的目的、衡量行为的方式、个性欣赏的常见问题、团队章程（Team Charter）的使用方式以及与核心协议（Core Protocols）的联系等一系列话题。</p> <i>By Stéphane Wojewoda</i> <i> Translated by 王婷婷</i>
---------------
<h1 id="#title_6" >7、Slack从JavaScript切换至TypeScript</h1>
Sergio De Simone
[http://www.infoq.com/cn/news/2017/04/going-typescript-slack?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/04/going-typescript-slack?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/news/2017/04/going-typescript-slack/zh/headerimage/GettyImages-456074601.jpg"/><p>Slack桌面端工程师Felix Rieseberg撰文介绍了Slack从JavaScript切换至TypeScript充满挑战，但也获得了巨大收益的过程。InfoQ采访了他。</p> <i>By Sergio De Simone</i> <i> Translated by 大愚若智</i>
---------------
<h1 id="#title_7" >8、亚马逊增加了对Aurora的跨区域和加密复制支持</h1>
Kent Weare
[http://www.infoq.com/cn/news/2017/04/Amazon-Aurora-Update?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/04/Amazon-Aurora-Update?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>在一篇最近的博客文章上，亚马逊最近公布了对她的兼容MySQL的数据库引擎Aurora的更新。在这次更新中亚马逊发布了许多项新功能，包括跨区域镜像拷贝、加密数据库的跨区域数据复制、不同账号之间的加密快照分享、增加了一个新的名为T2.Small的可以部署Aurora的区域等。</p> <i>By Kent Weare</i> <i> Translated by 足下</i>
---------------
<h1 id="#title_8" >9、谷歌的招聘工具和启示</h1>
Abel Avram
[http://www.infoq.com/cn/news/2017/04/hiring-tools-tips-Google?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/04/hiring-tools-tips-Google?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>谷歌发布了几个有助于招聘流程的工具，包括对创建一份招聘需求的建议、面试官的准备、面试过程中的最佳实践等。</p> <i>By Abel Avram</i> <i> Translated by 足下</i>
---------------
<h1 id="#title_9" >10、视频演讲： 以创业的思维经营开源项目</h1>
韩卿
[http://www.infoq.com/cn/presentations/operating-an-open-source-project-with-entrepreneurial-thinking?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/operating-an-open-source-project-with-entrepreneurial-thinking?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/operating-an-open-source-project-with-entrepreneurial-thinking/zh/mediumimage/hanqing270.jpg"/><p>几乎每一个成功的开源项目背后都有一家创业公司来提供商业运作，几乎每一个成功的开源项目的团队最终都会走上创业的路，开源而优则创业。那么如何开始开源项目？如何定位开源项目的商业价值？如何平衡商业与开源？如何说服投资者？如何真正建立一家基于开源的商业公司？
本主题将由国内唯一一个Apache 顶级项目创立者，首家在国内由 Apache 顶级项目核心贡献者团队组建的创业公司的联合创始人兼 CEO，分享 Apache Kylin 是怎么从无到有，从内部用到贡献给开源社区，并加入 Apache 孵化器项目以及如何管理和运作整个开源项目等的过程，运营项目不断扩大影响力和使用率，到接触投资机构并最终顺利融资并建立公司的历程与经验，为有志于技术创业的朋友分享技术之外的更多思考和教训等。</p> <i>By 韩卿</i>
---------------
<h1 id="#title_10" >11、文章： 三位专家谈大数据工程</h1>
Clemens Szyperski, Martin Petitclerc, Roger Barga
[http://www.infoq.com/cn/articles/big-data-engineering?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/big-data-engineering?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/big-data-engineering/zh/headerimage/GettyImages-519470268-2.jpg"/><p>来自微软、IBM、亚马逊网络服务的三位专家Clemens Szyperski、Martin Petitclerc和Roger Barga回答了三个大数据系统中的问题：在创建可伸缩的大数据系统时主要面对哪些挑战？如何解决这些挑战？社区研发过程中应该专注于哪些方面来开发工具及方法用于创建高可靠、可伸缩的大数据系统？</p> <i>By Clemens Szyperski</i> <i> Translated by 周元昊</i>
---------------
<h1 id="#title_11" >12、Applications Of Machine Learning For Designers</h1>
Lassi Liikkanen
[https://www.smashingmagazine.com/2017/04/applications-machine-learning-designers/](https://www.smashingmagazine.com/2017/04/applications-machine-learning-designers/)
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
</table><p>As a designer, you will be facing more demands and opportunities to work with digital systems that embody machine learning. To have your say about how best to use it, you need a good understanding about its applications and related design patterns.</p>

<figure></figure>

<p>This article illustrates the power of machine learning through the applications of detection, prediction and generation. It gives six reasons <strong>why machine learning makes products and services better</strong> and introduces four design patterns relevant to such applications. To help you get started, I have included two non-technical questions that will help with assessing whether your task is ready to be learned by a machine.</p><p>The post .</p>
---------------