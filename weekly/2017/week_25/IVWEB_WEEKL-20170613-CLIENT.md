## 文章索引
1、 <a href="#1fex-技术周刊---2017/06/12" >FEX 技术周刊 - 2017/06/12</a><br/>
2、 <a href="#2视频演讲-逢云化雨技术决策论ucloud云汉云计算体系解析" >视频演讲： 逢云化雨技术决策论：UCloud“云汉”云计算体系解析</a><br/>
3、 <a href="#3新技能get如何利用http技术提升网页的加载速度" >新技能Get：如何利用HTTP技术提升网页的加载速度</a><br/>
4、 <a href="#4无我编程的十条戒律" >无我编程的十条戒律</a><br/>
5、 <a href="#5苹果研发专用芯片助力移动ai" >苹果研发专用芯片，助力移动AI</a><br/>
6、 <a href="#6机器学习python和数学学习资料汇总" >机器学习、Python和数学学习资料汇总</a><br/>
7、 <a href="#72017年的-devops-报告新鲜出炉" >2017年的 DevOps 报告新鲜出炉</a><br/>
8、 <a href="#8a-complete-guide-to-switching-from-http-to-https" >A Complete Guide To Switching From HTTP To HTTPS</a><br/><h1 id="#title_0" >1、FEX 技术周刊 - 2017/06/12</h1>

[http://fex.baidu.com/blog/2017/06/fex-weekly-12//](http://fex.baidu.com/blog/2017/06/fex-weekly-12//)
作者：zhangbobell <br> <p>微信搜索『FEX』关注我们的公众号，及时获得最新资讯。</p>

<h2 id="section">业界会议</h2>

<p><strong>WWDC 2017</strong><br />
https://developer.apple.com/wwdc/<br />
亮点并不多，附：</p>

<p><strong>CES Asia 2017</strong><br />
http://ces.zol.com.cn/asia/<br />
可以围观下有啥高科技产品</p>

<h2 id="section-1">深阅读</h2>

<p><strong>V8 Release 6.0</strong><br />
https://v8project.blogspot.jp/2017/06/v8-release-60.html<br />
V8 version 6.0, which will be in beta until it is released in coordination with Chrome 60 Stable in several weeks. V8 6.0 is filled will all sorts of developer-facing goodies. We’d like to give you a preview of some of the highlights in anticipation of the release.</p>

<p><strong>JSC loves ES6</strong><br />
https://webkit.org/blog/7536/jsc-loves-es6/<br />
WebKit’s JavaScript implementation, called JSC (JavaScriptCore), implements all of ES6. ES6 features were implemented to be fast from the start, though we only had microbenchmarks to measure the performance of those features at the time. This post describes the development of our first ES6 benchmark, which we call ARES-6. We used ARES–6 to drive significant optimization efforts in JSC, and this post describes three of them: high throughput generators, a new Map/Set implementation, and phantom spread. The post concludes with an analysis of performance data to show how JSC’s performance compares to other ES6 implementations. 另附 Webkit 的其它更新： 发布.</p>

<p><strong>Node.js + MySQL Example: Handling 100’s of GigaBytes of Data</strong><br />
https://blog.risingstack.com/node-js-mysql-example-handling-hundred-gigabytes-of-data/<br />
Through this Node.js &amp; MySQL example project, we will take a look at how you can efficiently handle billions of rows that take up hundreds of gigabytes of storage space. My secondary goal with this article is to help you decide if Node.js + MySQL is a good fit for your needs, and to provide help with implementing such a solution.</p>

<p><strong>A Guide to Proper Error Handling in JavaScript</strong><br />
https://www.sitepoint.com/proper-error-handling-javascript/<br />
Ah, the perils of error handling in JavaScript. If you believe , anything that can go wrong, will go wrong. In this article, I would like to explore error handling in JavaScript. I will cover pitfalls, good practices, and finish with asynchronous code and Ajax.</p>

<p><strong>Upgrading from Node 6 to Node 8: a real-world performance comparison</strong><br />
https://hackernoon.com/upgrading-from-node-6-to-node-8-a-real-world-performance-comparison-3dfe1fbc92a3<br />
These performance comparisons are for a medium-to-large React site with a single page. On the server, it takes a JSON object with a few thousand properties and returns HTML with 2113 DOM nodes.</p>

<p><strong>Cloud Browser Architecture</strong><br />
https://www.w3.org/TR/2017/NOTE-cloud-browser-arch-20170608/<br />
The Web and TV Interest Group has published a Group Note of Cloud Browser Architecture. A Cloud Browser is a browser running and executing on a server. This document describes the concepts and architecture for the Cloud Browser. The main purpose of this document is to provide the building blocks for a Cloud Browser solution.</p>

<p><strong>The Evolution of Code Deploys at Reddit</strong><br />
https://redditblog.com/2017/06/02/the-evolution-of-code-deploys-at-reddit/<br />
We’re constantly deploying code at Reddit. Every engineer writes code, gets it reviewed, checks it in, and rolls it out to production regularly. This happens as often as 200 times each week and a deploy usually takes fewer than 10 minutes end-to-end. The system that powers all of this has evolved over the years. Let’s take a look at how it’s changed (and how it hasn’t) over all that time.</p>

<p><strong>Google - Spinnaker 1.0: a continuous delivery platform for cloud</strong><br />
http://cloudplatform.googleblog.com/2017/06/spinnaker-10-continuous-delivery.html<br />
We’re happy to announce the release of , an open-source multi-cloud continuous delivery platform used in production at companies like Netflix, Waze, Target, and Cloudera, plus a new open-source command line interface (CLI) tool called halyard that makes it easy to deploy Spinnaker itself.</p>

<p><strong>[译]ES6 modules 即将到来，现在该考虑新的打包方案了嘛</strong><br />
https://zhuanlan.zhihu.com/p/27276672<br />
ES6 modules(以下称ESM)已经定义到了ECMAScript规范里面有段时间了。社区的人们也写了很多文章布道怎么配合Babel来使用以及说明了import和node里的require的区别。但是在浏览器端完整的实现还需要一点时间。 很欣喜的看到Safari第一个在其工程预览版搭载ESM），现在Edge 和 Firefox Nightly也搭载了这个功能。在经历过使用像RequireJs Browserify（还记得AMD和common js之争吗）似乎modules终将到达浏览器领地，那么就让我们来看看未来将会带给我们什么吧。</p>

<p><strong>[译]自包含系统：打开微服务的正确方式</strong><br />
http://www.infoq.com/cn/articles/scs-microservices-done-right <br />
比微服务更进一步，UI 也独立，很多年前的 bigpipe 就是能做到类似的效果了</p>

<p><strong>WebView性能、体验分析与优化</strong><br />
http://tech.meituan.com/WebViewPerf.html<br />
在App开发中，内嵌WebView始终占有着一席之地。它能以较低的成本实现Android、iOS和Web的复用，也可以冠冕堂皇的突破苹果对热更新的封锁。然而便利性的同时，WebView的性能体验却备受质疑，导致很多客户端中需要动态更新等页面时不得不采用其他方案。那么如何克服WebView固有的问题呢？我们将从性能、内存消耗、体验、安全几个维度，来系统的分析客户端默认WebView的问题，以及对应的优化方案。</p>

<p><strong>Web安全之XSS</strong><br />
https://techblog.toutiao.com/2017/06/06/xss/<br />
XSS 科普</p>

<p><strong>那些你不知道的爬虫反爬虫套路</strong><br />
https://zhuanlan.zhihu.com/p/27299841<br />
现在要拼前端了</p>

<p><strong>Reducing our Redux code with React Apollo</strong><br />
https://dev-blog.apollodata.com/reducing-our-redux-code-with-react-apollo-5091b9de9c2a<br />
虽然是软文，但思路可以参考</p>

<p><strong>Learn more about npm’s lockfiles</strong><br />
http://blog.npmjs.org/post/161627993435/learn-more-about-npms-lockfiles<br />
npm5 introduces a lockfile, package-lock.json that keeps a record of every dependency your project uses and what version you have currently installed. Before npm5, this was behavior you could only get from npm shrinkwrap.</p>

<p><strong>Classes, Complexity, and Functional Programming</strong><br />
https://medium.com/@kentcdodds/classes-complexity-and-functional-programming-a8dd86903747<br />
When it comes to applications intended to last, I think we all want to have simple code that’s easier to maintain. Where we often really disagree is how to accomplish that. In this blog post I’m going to talk about how I see functions, objects, and classes fitting into that discussion.</p>

<p><strong>A Brief History of the UUID</strong><br />
https://segment.com/blog/a-brief-history-of-the-uuid/<br />
Today we’re releasing ksuid, a Golang library for unique ID generation. It borrows core ideas from the ubiquitous UUID standard, adding time-based ordering and more friendly representation formats. In doing the research that went into this library, we uncovered a compelling story that we wanted to share with a larger audience. 另附：.</p>

<p><strong>The State Of Advanced Website Builders</strong><br />
https://www.smashingmagazine.com/2017/06/advanced-website-builders/<br />
Advanced website builders — the tools provided by Squarespace, Wix, Weebly, The Grid and more — produce websites that look and feel like they were designed and coded by humans. They’re also software as a service, which is a different business model than traditional, custom-developed websites. So, should companies use them? At some point, will they replace custom development?</p>

<p><strong>How to do it like Google with this powerful checklist</strong><br />
https://uxplanet.org/ux-writing-how-to-do-it-like-google-with-this-powerful-checklist-e263cc37f5f1<br />
These are my notes from a Google I/O 2017 talk by three UX Writers. It’s a great resource to start creating a UX Writing process within your organisation. Useful for anyone involved in putting words on interfaces.</p>

<p><strong>Color Accessibility Workflows</strong><br />
https://alistapart.com/article/color-accessibility-workflows<br />
The Web Content Accessibility Guidelines (WCAG) 2.0 contain recommendations from the World Wide Web Consortium (W3C) for making the web more accessible to users with disabilities, including color blindness and other vision deficiencies.</p>

<p><strong>Creating Yin and Yang Loaders On the Web</strong><br />
https://css-tricks.com/creating-yin-yang-loaders-web/<br />
I came across a couple such animations a while ago and this gave me the idea of creating my own versions with as little code as possible, no external libraries, using various methods, some of which take advantage of more recent features we can use these days, such as CSS variables. This article is going to guide you through the process of building these demos.</p>

<p><strong>digital video introduction</strong><br />
https://github.com/leandromoreira/digital_video_introduction#basic-terminology <br />
A hands-on introduction to video technology: image, video, codec (av1, h264, h265) and more (ffmpeg encoding).</p>

<h2 id="section-2">新鲜货</h2>

<p><strong>WCDB</strong><br />
https://github.com/Tencent/wcdb<br />
微信基于 SQLCipher 封装的移动端数据库，带 ORM 等功能。附介绍：</p>

<p><strong>Lullaby</strong><br />
https://github.com/google/lullaby<br />
Lullaby is a collection of C++ libraries designed to help teams develop virtual and augmented reality experiences.</p>

<p><strong>Introducing Graywater for Android</strong><br />
https://engineering.tumblr.com/post/161546559631/introducing-graywater-for-android<br />
, Tumblr’s framework for decomposing complex items in a RecyclerView list in order to improve scroll performance, reduce memory usage, and lay a foundation for a more composition-oriented approach to building lists. With Graywater, the app now scrolls faster and crashes less often, and it also gives us a solid foundation for building new features faster and better than before.</p>

<p><strong>Node v8.1.0</strong><br />
https://nodejs.org/en/blog/release/v8.1.0/<br />
一些小的修复</p>

<p><strong>Miscrosoft - Fluent Design System</strong><br />
http://fluent.microsoft.com/<br />
Now’s the time for bold, scalable, universal design. This is a transformation. A step into the future of sensory experiences. The world is at our fingertips – join Microsoft in building a design evolution. Design and develop apps using Fluent Design. </p>

<p><strong>The Future of MDN: A Focus on Web Docs</strong><br />
https://developer.mozilla.org/<br />
’s mission today is to provide developers with the information they need to build things on the open Web. MDN is clearly a web documentation reference, and in no way is it a developer network. We want the name to clearly reflect the purpose and mission of MDN, and so we’re going to be updating it to: MDN Web Docs.</p>

<p><strong>JavaScript’s new #private class fields</strong><br />
http://thejameskyle.com/javascripts-new-private-class-fields.html<br />
 are now at Stage 2 in the JavaScript standard process. It’s not finalized yet, but the JavaScript standards committee expects the feature to be developed and eventually included in the standard (although it may still change).</p>

<p><strong>React Log: React for the Console</strong><br />
https://github.com/diegomura/react-log<br />
A component that’s not rendered into the DOM but instead to the console.</p>

<p><strong>billboard.js</strong><br />
https://github.com/naver/billboard.js<br />
billboard.js is a re-usable easy interface JavaScript chart library, based on D3 v4+. 可视化领域还是  更值得信赖.</p>

<p><strong>Mega Project List</strong><br />
https://github.com/karan/Projects<br />
A list of practical projects that anyone can solve in any programming language.</p>

<p><strong>Google’s Environmental Report</strong><br />
https://environment.google/<br />
At Google, our values reflect the fundamental importance of inclusion, openness, science, and commitment to the environment. Operating our business in an environmentally sustainable way has been a core value from the beginning.</p>

<p><strong>npmcharts</strong><br />
http://npmcharts.com/<br />
试试了解目前社区最喜欢哪个库</p>

<p><strong>legoflow</strong><br />
https://github.com/legoflow/legoflow<br />
不了解 node 也能做工程化</p>

<p><strong>High Efficiency Image File Format (HEIF)</strong><br />
https://nokiatech.github.io/heif/ <br />
诺基亚提出的图片格式，比 jpeg 体积小且效果好，但不清楚和 webp 对比如何</p>

<p><strong>Clone in Xcode</strong><br />
https://github.com/blog/2375-clone-in-xcode<br />
It’s easy to explore code in your browser when you visit a GitHub repository, but you often want to pull that code directly into the appropriate editor and try it out. For example, if the repository contains an .xcodeproj or .xcworkspace file, you might want to open that code in Xcode.</p>

<p><strong>ChaosBot</strong><br />
https://github.com/chaosbot/chaos<br />
ChaosBot is a social coding experiment to see what happens when the absolute direction of a software project is turned over to the open source community.</p>

<p><strong>barba.js</strong><br />
https://github.com/luruke/barba.js/<br />
barba.js is a small (4kb minified and gzipped), flexible and dependency free library that helps you creating fluid and smooth transitions between your website’s pages. It helps reducing the delay between your pages, minimizing browser HTTP requests and enhancing your user’s web experience.</p>

<h2 id="section-3">产品及其它</h2>

<p><strong>饿了么 Sofish：前端、移动程序员，如何在大前端浪潮下成长</strong><br />
https://mp.weixin.qq.com/s?__biz=MjM5MDE0Mjc4MA==&amp;mid=2650996438&amp;idx=1&amp;sn=9d3bc76d66030a9d46004260e711cad4<br />
这几个心得很赞：职业不一样，是担起的担子，是对一群人包括自己的一种责任，有些事不喜欢不仅得做，还要做的漂亮；无论选择什么方向，一方面尽力做到最好；另一方面不要给自己设限，去接受更多挑战以提升自己；这样可能是比选择一个方向要更靠谱的方法；比选择更重要的是，成为一个某个产品或团队因为有你而变得更好的人。</p>

<p><strong>凯文凯利：真正的AI时代还未来临</strong><br />
http://newrss.guancha.cn/toutiao/toutiaopost/TMT/2017_06_09_412519.shtml<br />
将会有无数差异化的有别于人类思维的AI迎着我们走来，集合成无比灿烂的交响乐章；随着不断的发展与完善，它们会像电一样在“云”端被人类依赖，作为新经济的引擎，AI帮助人类延展自己的感知领域，也带给创业者们更多的机会。不要恐惧AI及智能机器人时代的到来，因为它只会给人类带来更多更有趣的工作机会；真正的AI时代远还未来临，目前还处于类似于工业革命农业革命一样的AI革命时代，是AI时代开始的开始，好日子还在后头，我们大家要满怀喜悦地迎接这个时代的到来。另附：。</p>

<p><strong>俞永福-看过500家创业公司生死后的产品观</strong><br />
https://mp.weixin.qq.com/s?__biz=MjM5MzkwMzk2MA==&amp;mid=2649939985&amp;idx=2&amp;sn=d0e32680d36703726319eaadbdb3517c<br />
产品经理所需的三大特质：第一，感性与理性；第二，产品哲学；第三，0到1的经历。产品角度的四条线：1、自己的亮点是什么？2、自己的死点是什么？ 3、对手的亮点是什么？ 4、对手的死点是什么。互联网组织形态下：无形和无价的产品。在决策机制上避免两种倾向：一言堂、讲民主。另附：</p>

<p><strong>StackOverflow创始人关于如何高效编程的清单</strong><br />
https://mp.weixin.qq.com/s?__biz=MzA5Nzc4OTA1Mw==&amp;mid=2659599322&amp;idx=1&amp;sn=0f201ceb0d650637384bdd2aea95bb84<br />
无我编程的十条戒律，最早出现在 Gerald Weinberg 于 1971 年出版的经典著作《程序开发心理学》里。Stack Overflow 网站的联合创始人 Jeff Atwood 在博客上再次列出了这十条戒律。要知道，在这本著作出版的时候，Jeff 才一岁。虽然已经过去了几十年，但这些原则并没有被时间侵蚀，仍然值得每一位程序员拜读。另附：<a href="https://mp.weixin.qq.com/s?__biz=MzIyNjE4NjI2Nw==&amp;mid=2652558856&amp;idx=1&amp;sn=bc65b28d3cbe5a1a84bdc5f7e005427  
d">成为专家级程序员的修炼之道</a></p>
---------------
<h1 id="#title_1" >2、视频演讲： 逢云化雨技术决策论：UCloud“云汉”云计算体系解析</h1>
许杨毅
[http://www.infoq.com/cn/presentations/the-analytical-calculation-system-ucloud?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/the-analytical-calculation-system-ucloud?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/the-analytical-calculation-system-ucloud/zh/mediumimage/xuyangyi270.jpg"/><p>据 Cisco 和 Rightscale 分析报告，到 2020 年，77% 的数据和 92% 的计算将会在云端，云计算市场越做越大。作为 IT 技术决策人，在云技术方案选型上，如何合理的进行技术决策、实现自身产品升级和解决方案的最优化？本专场恰恰是这一主题的深入探讨。“云汉”产品解决方案体系，是 3.29 日在 Think in cloud 峰会上推出的全新技术方案体系，从本质上讲，是 UCloud 深挖行业痛点，“应需而为”的成果，也是 UCloud 差异化核心竞争力的重要体现。包括了：视频直播云解决方案——“瑶光”；混合云解决方案——“启明”；金融云解决方案——“玉衡”；全球服解决方案——“开阳”；人工智能解决方案——“文曲”以及 Serverless 计算解决方案——“武曲”。4.16 日的云生态专场上，“云汉”产品体系设计者，UCloud 产品副总裁许杨毅将同您分享这一精彩内容。</p> <i>By 许杨毅</i>
---------------
<h1 id="#title_2" >3、新技能Get：如何利用HTTP技术提升网页的加载速度</h1>
纪永康
[http://www.infoq.com/cn/news/2017/06/HTTP-Akamai-mobile?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/06/HTTP-Akamai-mobile?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>所谓天下武功，唯快不破！想要设计更快的网页优化速度，我们可以借鉴成功的优化经验，全球最大的CDN服务商Akamai（阿卡迈）针对移动体验的问题，提供了一套较为完整的解决方案，感兴趣的读者可以前往注册下载；与此同时，我们也可以采用直接的技术手段，本文从PC端优化经验、HTTP/2优化协议、优化蜂窝网络、以及智能的加载方案设计四个维度，总结了一些提升移动网页加载速度的方法和技巧。</p> <i>By  纪永康</i>
---------------
<h1 id="#title_3" >4、无我编程的十条戒律</h1>
薛命灯
[http://www.infoq.com/cn/news/2017/06/10-Commandments-without-program?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/06/10-Commandments-without-program?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>无我编程的十条戒律，最早出现在Gerald Weinberg于1971年出版的经典著作《程序开发心理学》里。Stack Overflow网站的联合创始人Jeff Atwood在博客上再次列出了这十条戒律。</p> <i>By 薛命灯</i>
---------------
<h1 id="#title_4" >5、苹果研发专用芯片，助力移动AI</h1>
薛命灯
[http://www.infoq.com/cn/news/2017/06/Apple-chip-AI?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/06/Apple-chip-AI?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>苹果在WWDC 2017大会上发布了用于在移动设备上处理AI任务的API框架Core ML。将AI从云端移动到设备上对设备提出了更高的要求，比如CPU和功耗。为了让设备上的AI更强大，苹果开始发力专门为AI设计的芯片。</p> <i>By 薛命灯</i>
---------------
<h1 id="#title_5" >6、机器学习、Python和数学学习资料汇总</h1>
薛命灯
[http://www.infoq.com/cn/news/2017/06/Machine-Python-math-aggregation?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/06/Machine-Python-math-aggregation?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>机器学习保罗万象，在学习这门技术时，最好可以有一些速查手册之类的东西在手边，它们列出了需要了解的关键点。Robbie Allen整理了20多个与机器学习相关的速查资料，并分享出来，或许也可以帮助其他学习这门技术的人。</p> <i>By 薛命灯</i>
---------------
<h1 id="#title_6" >7、2017年的 DevOps 报告新鲜出炉</h1>
Andrew Silver 等
[http://www.infoq.com/cn/news/2017/06/2017-DevOps-baogao?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/06/2017-DevOps-baogao?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>又是一年年中时：由 Puppet 与 DevOps 研究与评估（简称 DORA）协会共同发布的最新《DevOps 现状调查报告（State of DevOps）》再度出炉。作为本轮的核心议题，双方分析了“高效领导者如何影响技术实践与流程改进，从而带来更为理想的 IT 与组织运作成效，同时确认称自动化水平已然成为不同企业之间的核心区别所在。”</p> <i>By Andrew Silver 等</i> <i> Translated by 运和凭</i>
---------------
<h1 id="#title_7" >8、A Complete Guide To Switching From HTTP To HTTPS</h1>
Vladislav Denishev
[https://www.smashingmagazine.com/2017/06/guide-switching-http-https/](https://www.smashingmagazine.com/2017/06/guide-switching-http-https/)
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
</table><p>HTTPS is <strong>a must for every website</strong> nowadays: Users are looking for the padlock when providing their details; Chrome and Firefox explicitly mark websites that provide forms on pages without HTTPS as being non-secure; it is an SEO ranking factor; and it has a serious impact on privacy in general.</p>

<figure></figure>

<p>Additionally, there is now more than one option to get an HTTPS certificate for free, so switching to HTTPS is only a matter of will.</p><p>The post .</p>
---------------