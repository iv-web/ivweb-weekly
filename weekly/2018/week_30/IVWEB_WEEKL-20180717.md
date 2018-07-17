## 文章索引
1、 <a href="#1视频演讲-高可用性系统的架构与运维实践" >视频演讲： 高可用性系统的架构与运维实践</a><br/>
2、 <a href="#2fex-技术周刊---2018/07/16" >FEX 技术周刊 - 2018/07/16</a><br/>
3、 <a href="#3cap-定理的含义" >CAP 定理的含义</a><br/>
4、 <a href="#4文章-组织变革中的恐慌成本" >文章： 组织变革中的恐慌成本</a><br/>
5、 <a href="#5视频演讲-互联网文本内容安全一种对抗式ai设计实践" >视频演讲： 互联网文本内容安全：一种对抗式AI设计实践</a><br/>
6、 <a href="#6视频演讲-cloud-studio-beta-20-发布" >视频演讲： Cloud Studio Beta 2.0 发布</a><br/>
7、 <a href="#7the-holy-grail-of-reusable-components:-custom-elements-shadow-dom-and-npm" >The Holy Grail Of Reusable Components: Custom Elements, Shadow DOM, And NPM</a><br/>
8、 <a href="#830个案例告诉你企业到底是怎么用区块链的" >30个案例告诉你，企业到底是怎么用区块链的</a><br/>
9、 <a href="#9无代码方法和低代码方法如何为业务用户和专业开发人员提供支持" >无代码方法和低代码方法如何为业务用户和专业开发人员提供支持</a><br/>
10、 <a href="#10实体服务增加了系统复杂性" >实体服务增加了系统复杂性</a><br/>
11、 <a href="#11nginx-controller现已普遍可用" >NGINX Controller现已普遍可用</a><br/>
12、 <a href="#12微信小程序的下一步支持npm小程序云可视化编程支持分包" >微信小程序的下一步：支持NPM、小程序云、可视化编程、支持分包</a><br/><h1 id="#title_0" >1、视频演讲： 高可用性系统的架构与运维实践</h1>
王栋
[http://www.infoq.com/cn/presentations/architecture-and-operation-practice-of-high-availability-system?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/architecture-and-operation-practice-of-high-availability-system?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/presentations/architecture-and-operation-practice-of-high-availability-system/zh/mediumimage/wangdong270-1531486667003.jpg"/><p>确保大型分布式复杂软件系统的可用性历来是一个严峻的技术挑战，具体而言，这种挑战一方面来自于系统的体系架构设计，另一方面来自于线上系统的高效运维，二者相辅相成。本次分享将从百度运维的技术演进切入，介绍百度如何从最初的手工操作为主发展到如今领先业界的AIOps实际落地；然后以变更管理作为一个典型的例子，阐述百度在实践DevOps方面的一些体会；最后，以百度统一前端接入（Baidu Front End, BFE）、数据库以及Redis为例，介绍保证线上系统高可用的实战经验。</p> <i>By 王栋</i>
---------------
<h1 id="#title_1" >2、FEX 技术周刊 - 2018/07/16</h1>

[http://fex.baidu.com/blog/2018/07/fex-weekly-16//](http://fex.baidu.com/blog/2018/07/fex-weekly-16//)
作者：wuyiping <br> <h2 id="section">业界会议</h2>

<p><strong>ICML International Conference on Machine Learning</strong><br />
https://icml.cc/Conferences/2018<br />
附：</p>

<h2 id="section-1">深阅读</h2>

<p><strong>Postmortem for Malicious Packages Published</strong><br />
https://eslint.org/blog/2018/07/postmortem-for-malicious-package-publishes<br />
On July 12th, 2018, an attacker compromised the npm account of an ESLint maintainer and published malicious versions of the eslint-scope and eslint-config-eslint packages to the npm registry. On installation, the malicious packages downloaded and executed code from pastebin.com which sent the contents of the user’s .npmrc file to the attacker. An .npmrc file typically contains access tokens for publishing to npm. 附：.</p>

<p><strong>Goodbye Microservices: From 100s of problem children to 1 superstar</strong><br />
https://segment.com/blog/goodbye-microservices/<br />
In early 2017 we reached a tipping point with a core piece of Segment’s product. It seemed as if we were falling from the microservices tree, hitting every branch on the way down. Instead of enabling us to move faster, the small team found themselves mired in exploding complexity. Essential benefits of this architecture became burdens. As our velocity plummeted, our defect rate exploded. Eventually, the team found themselves unable to make headway, with 3 full-time engineers spending most of their time just keeping the system alive. Something had to change. This post is the story of how we took a step back and embraced an approach that aligned well with our product requirements and needs of the team.  另附：.</p>

<p><strong>Service Mesh and the Promise of Istio</strong><br />
https://thenewstack.io/service-mesh-and-the-promise-of-istio/<br />
In a microservices environment, neither of these options is ideal. The application overlay approach is application aware and can perform sophisticated content-based routing, but it will lead to a large amount of redundant code in each service and potentially a lower performance. Conversely, relying on traditional L3 or L4 networking means that it has neither the concept nor the visibility of service requests, which are critical to making optimal routing decisions. This is why service mesh is so appealing for the microservice environment — it operates at the L7 level, but is separate from the application code and can enforce L3/L4 policies with app-level insight. To understand this point, we must first dig into the architecture of service mesh.</p>

<p><strong>Thank You for Your Help NoSQL, but We Got It from Here</strong><br />
http://blog.memsql.com/nosql/<br />
It’s time for us to admit what we have all known is true for a long time; NoSQL is the wrong tool for many of the modern application use cases, and it’s time that we move on.</p>

<p><strong>洞察 video 超能力系列——玩转 mp4</strong>. 
https://techblog.toutiao.com/2018/07/09/untitled-51/<br />
只要在 HTML5 中使用过视频播放的同学对 video 标签一定不会陌生，不过很多同学只使用了 video 的基础功能，实际上 video 拥有强大潜能的，只要姿势正确就能让其拥有超能力。不妨从下面几个场景来逐渐了解下video 未曾被发掘的神秘空间： * 清晰度无缝切换 * 节省视频流量。另附：。</p>

<p><strong>移动持续集成在大众点评的实践</strong><br />
https://tech.meituan.com/mci.html<br />
MCI（Mobile continuous integration）是大众点评移动端团队多年来实践总结出来的一套行之有效的架构体系。它能实际解决移动项目中依赖复杂、研发流程琐碎、构建速度慢的问题，同时接入MCI架构体系的移动项目能真正有效实现App质量的提升。</p>

<p><strong>编程人生：毕业到迈入工作的第五年</strong><br />
https://mp.weixin.qq.com/s?__biz=MjM5Mjg4NDMwMA==&amp;mid=2652975960&amp;idx=1&amp;sn=9539d222eae7a50ddb5ca7d42a24a28f<br />
每年，在这个时候，充满了悲欢离合，也总能看到各种活蹦乱跳的小鲜肉。我们毕业了，我们开始赚钱了，我们踏上了一条不归路……。结束一段旅程，开始填新的坑，或者挖一个坑。我总习惯性的会做一些“反省”、总结的文章，它可以帮助我重新回到 “正轨” 上，指出到下一阶段我所需要的内容。另附：</p>

<p><strong>微信小程序的下一步：支持NPM、小程序云、可视化编程、支持分包</strong>
https://mp.weixin.qq.com/s?__biz=MzUxMzcxMzE5Ng==&amp;mid=2247489190&amp;idx=1&amp;sn=f10a16e2ac08c07c43cbdad76a1f2ec9<br />
微信公开课微信小程序技术专场在上海举行，会上，微信公布了面向开发者的技术规划，内容主要包括小程序技术能力与规划、小程序生态体系、小程序性能优化三个方面。</p>

<p><strong>Javascript Framework Comparison with Examples (React, Vue &amp; Hyperapp)</strong><br />
https://hackernoon.com/javascript-framework-comparison-with-examples-react-vue-hyperapp-97f064fb468d<br />
In my , I tried to explain why I think Hyperapp is a viable alternative to React or Vue and the reasons I found it easier to get started with it. Lots of people criticized that piece, as it was opinionated and didn’t give the other frameworks a proper chance to shine. So, in this article, I’m going to try to compare these three frameworks as objectively as possible, by providing some minimal examples to showcase their capabilities.</p>

<p><strong>Out of Depth with Flutter</strong><br />
https://medium.com/flutter-io/out-of-depth-with-flutter-f683c29305a8<br />
In my experience using Flutter (as a member of the Flutter team), development speed is achieved primarily through the following: Stateful hot reload; Reactive programming; Composition; UI as code.</p>

<p><strong>LinkedIn Lite: A Server-Side Rendered PWA</strong><br />
https://engineering.linkedin.com/blog/2018/07/linkedin-lite–a-server-side-rendered-pwa<br />
A couple of months ago, we shared details about LinkedIn Lite’s architecture, its evolution as a light-weight mobile web experience, and how it became a huge success in emerging markets. As a pure server-side rendered web app, it was fast, but it wasn’t providing a good user experience.</p>

<p><strong>Evolving the MediaWiki platform: Why we replaced Tidy with a HTML5 parser</strong><br />
https://blog.wikimedia.org/2018/07/09/tidy-html5-replacement/<br />
Three years ago, the Wikimedia Foundation’s Parsing Team decided to replace Tidy, a tool to fix HTML errors, with an HTML5-based tool. Here’s what we did in that time period, and what kind of complexities we faced in changing pieces of the technical infrastructure powering Wikimedia wikis.</p>

<p><strong>Building a real-time user action counting system for ads</strong><br />
https://medium.com/@Pinterest_Engineering/building-a-real-time-user-action-counting-system-for-ads-88a60d9c9a<br />
The Pinterest ads team’s mission is to provide the best experience for both Pinners and advertisers. Our ads system is a real-time bidding system that delivers targeted ads based on a variety of attributes. One of the major behavioral attributes is user action counts, the count for a Pinner’s past clicks, impressions and other actions on ads. An important part of user action counts is frequency control, which sets a maximum number of times an ad is shown to a Pinner (impression counts over a period of time enforce this limit).</p>

<p><strong>XARs: An efficient system for self-contained executables</strong><br />
https://code.fb.com/data-infrastructure/xars-a-more-efficient-open-source-system-for-self-contained-executables/<br />
XARs can be used to deploy Python virtual environments, bundle Node.js applications, and even Lua tools. This can result in efficiency wins from lowered overhead for many types of Python tools, reduced size of the binaries deployed, and offer a more reliable production environment for Python tooling. 另附：.</p>

<p><strong>Event Sourcing in Action with eBay’s Continuous Delivery Team</strong><br />
https://www.ebayinc.com/stories/blogs/tech/event-sourcing-connecting-the-dots-for-a-better-future/<br />
https://www.ebayinc.com/stories/blogs/tech/event-sourcing-in-action-with-ebays-continuous-delivery-team/<br />
Using an Event-centric approach has enabled our team at eBay to scale to handle millions of events with the resiliency to recover from failures as quickly and reliably as possible. Though similar approaches have been widely adopted to augment large-scale data applications, for eBay’s Continuous Delivery team, Event Sourcing is at the heart of decision-making and application development. To that end, we’ve built a system that continuously scales and tests our ability to handle an increasing volume of events and an ever growing list of external data sources and partner integrations.</p>

<p><strong>Simple, correct, fast: in that order</strong><br />
https://drewdevault.com/2018/07/09/Simple-correct-fast.html<br />
The single most important quality in a piece of software is simplicity. It’s more important than doing the task you set out to achieve. It’s more important than performance. The reason is straightforward: if your solution is not simple, it will not be correct or fast.</p>

<p><strong>Learning To Code By Writing Code Poems</strong><br />
https://www.smashingmagazine.com/2018/07/writing-code-poems/<br />
Learning to code can be tough. In this article, Murat shares his advice on how writing code differently and poetically has helped him overcome his initial struggles and insecurities.</p>

<p><strong>Google Cloud Platform - The Good, Bad, and Ugly (It’s Mostly Good)</strong><br />
https://www.deps.co/blog/google-cloud-platform-good-bad-ugly/<br />
A note up front, these are solely my experiences, and it’s quite possible that I’ve misunderstood or misrepresented things here. If I’ve made any mistakes, let me know so I can correct them. I only talk about services that I have experience using. There are a bunch of really good looking services like Google Kubernetes Engine, Google App Engine, and BigQuery, but I haven’t used them enough (or at all) to be able to give a review on them.</p>

<h2 id="section-2">新鲜货</h2>

<p><strong>Introducing Jib — build Java Docker images better</strong><br />
https://cloudplatform.googleblog.com/2018/07/introducing-jib-build-java-docker-images-better.html<br />
To address this challenge, we’re excited to announce .</p>

<p><strong>npm Joins ECMA International and TC39</strong><br />
https://blog.npmjs.org/post/175722319045/npm-joins-ecma-international-and-tc39<br />
We’re excited to announce that npm has joined ECMA International and is participating in TC39, the working group of ECMA International that defines the standard for the JavaScript programming language.</p>

<p><strong>Bringing GraphQL to Octokit.NET</strong><br />
https://blog.github.com/2018-07-13-graphql-for-octokit/<br />
If you’ve built apps that connect with GitHub, you are no doubt familiar with Octokit. GitHub offers three official flavors of the easy-to-use Octokit library—one for Ruby, .NET, and Node.js—that work with the GitHub REST API v3. Back in September of 2016, we announced that we would move to GraphQL, the query language developed by Facebook, in part due to the ability to fetch all of the data we wanted in a single request. As a result, the GitHub API v4 is built on GraphQL instead of REST. 另附:.</p>

<p><strong>Announcing TypeScript 3.0 RC</strong><br />
https://blogs.msdn.microsoft.com/typescript/2018/07/12/announcing-typescript-3-0-rc/<br />
We’ll be discussing a few major items going into TypeScript 3.0: Project references, Extracting and spreading parameter lists with tuples, Richer tuple types, The unknown type, Support for React’s defaultProps.</p>

<p><strong>State of Kotlin 2018</strong><br />
https://pusher.com/state-of-kotlin<br />
From Google announcing Kotlin support in Android a year ago, to over 100k respondents of the StackOverflow survey voting it the second most loved language, JetBrains’ baby is thriving. At Pusher, we wanted to learn what’s so special about Kotlin so we decided to dig deeper. We surveyed 2,744 people from January to March 2018 and took the pulse of the ecosystem. 另附：.</p>

<p><strong>NGINX Unit 1.3 Available Now</strong><br />
https://www.nginx.com/blog/nginx-unit-1-3-available-now/<br />
NGINX Unit 1.3 includes these new features: New settings object in the configuration API; Configuration of HTTP timeouts; Configuration of request body size limit; Automatic use of Bundler for Ruby applications; Ansible integration. These new features make your applications more configurable. All parameters can be defined dynamically, without any disruption to running services or loss of connectivity.</p>

<p><strong>Bootstrap 4.1.2</strong><br />
http://blog.getbootstrap.com/2018/07/12/bootstrap-4-1-2/<br />
Beyond the file structure changes, here are the highlights for v4.1.2: Fixed an XSS vulnerability in tooltip, collapse, and scrollspy plugins; Improved how we query elements in our JavaScript plugins; Inline SVGs now have the same vertical alignment as images; Fixed issues with double transitions on carousels…</p>

<p><strong>The Ultimate Guide to Learning CSS</strong><br />
https://zendev.com/ultimate-guide-to-learning-css.html<br />
If you have particular areas of CSS you want to brush up on, you can use the table of contents to jump to them. If you’re looking for comprehensive “learn everything from a single source” resources, you should jump down to comprehensive resources and courses. And finally, if you’re looking for ways to stay up to date, the newsletters portion at the very end will give you a number of options for continuing to hear about the latest and greatest. 另附：.</p>

<p><strong>React/Redux Style Guide</strong><br />
https://github.com/iraycd/React-Redux-Styleguide<br />
This is a working set of guidelines for developing React applications. We say “guideline” because there are no hard-and-fast rules; best practices, patterns and technology change over time, so we consider this a living set of style guides.</p>

<p><strong>Toast UI ImageEditor</strong><br />
https://github.com/nhnent/tui.image-editor<br />
Full featured image editor using HTML5 Canvas. It’s easy to use and provides powerful filters.</p>

<p><strong>ReaKit</strong><br />
https://reakit.io/<br />
Toolkit for building interactive UIs with React</p>

<p><strong>React Fiber renderer for PIXI</strong><br />
https://reactpixi.org/#/<br />
A custom React 16+ (Fiber) renderer. Write PIXI applications using React declarative style.</p>

<p><strong>Kleur</strong><br />
https://github.com/lukeed/kleur<br />
The fastest Node.js library for formatting terminal text with ANSI colors~!</p>

<p><strong>Phenomenon</strong><br />
https://github.com/vaneenige/phenomenon<br />
Phenomenon is a very small, low-level WebGL library that provides the essentials to deliver a high performance experience. Its core functionality is built around the idea of moving millions of particles around using the power of the GPU.</p>

<p><strong>PuzzleScript</strong><br />
https://www.puzzlescript.net/<br />
PuzzleScript is an open-source HTML5 puzzle game engine.</p>

<p><strong>Browsh</strong><br />
https://www.brow.sh/<br />
Browsh is a fully-modern text-based browser. It renders anything that a modern browser can; HTML5, CSS3, JS, video and even WebGL. Its main purpose is to be run on a remote server and accessed via SSH/Mosh or the in-browser HTML service in order to significantly reduce bandwidth and thus both increase browsing speeds and decrease bandwidth costs.</p>

<p><strong>Fathom - simple website analytics</strong><br />
https://github.com/usefathom/fathom<br />
Fathom Analytics is a simpler and more privacy-focused alternative to Google Analytics. Collecting information on the internet is important, but it’s broken. We’ve become complacent in trading information for free access to web services, and then complaining when those web services do crappy things with that data. The problem is this: if we aren’t paying for the product, we are the product.</p>

<p><strong>LocustDB</strong><br />
https://github.com/cswinter/LocustDB<br />
An experimental analytics database aiming to set a new standard for query performance on commodity hardware. See  per Second on a Single Desktop PC for an overview of current capabilities.</p>

<h2 id="section-3">设计</h2>

<p><strong>Design Systems at GitHub</strong><br />
https://medium.com/@broccolini/design-systems-at-github-c8e5378d2542<br />
Design systems have become core to the way we design and build at GitHub. Since 2011 GitHub designers have documented UI patterns and shared common styles. In 2012, CSS and other assets were packaged up into a Ruby Gem for use in GitHub websites — this package was named Primer. Primer continued to be used internally for years before eventually having its CSS and accompanying documentation open-sourced as Primer CSS. In 2016 the design systems team was formed with its first full-time employees. This post shares a brief history of how the team grew, what we’ve been working on, and what’s next.</p>

<p><strong>Dark Side of the Mac: Appearance &amp; Materials</strong><br />
https://mackuba.eu/2018/07/04/dark-side-mac-1/<br />
This eventually grew into the longest article on this blog, so instead of deleting some sections, I’ve decided to split it into two parts. This first part will be a bit more theoretical about some underlying features and APIs that make the dark mode work or that are especially relevant now, and the second part will be about the things you need to think about while updating the app (and in the future).</p>

<p><strong>What every product designer should take away from Lyft’s new UI</strong><br />
https://uxdesign.cc/what-every-product-designer-should-take-away-from-lyfts-new-ui-742c9668b067<br />
Lyft took a different approach with their search bar. Instead of a floating field up top, they added it to an overlay towards the bottom-mid section of the screen. This simple change made it more accessible for almost 100% of users.</p>

<p><strong>7 Basic Design Principles We Forget About</strong><br />
https://uxplanet.org/7-basic-design-principles-we-forget-about-8f5c15d4b527<br />
There are of course a lot more principles that we should use, but the problem is that a lot of us still don’t use these. And it mainly happens because we prioritise tasks and goals that are not important to our customers. We should always strive to find the right balance that works for our product and users. 另附：<a href="https://uxplanet.org/15-simple-habits-that-will-help-you-become-a-better-ux-designer-d5ecb4aed281">15 Simple Habits That Will Help You Become a Better UX Designer
</a></p>

<p><strong>A quick guide to choosing a color palette</strong><br />
https://www.invisionapp.com/blog/quick-guide-color-palette/<br />
It doesn’t have to be overwhelming. With a few well-placed tips and hints, you can take most of the work out of picking fonts and choosing colors. We’ve already covered the former, so here’s some approaches to the latter that should up your design game and make it easier to pick a palette that’s pleasing to the eye and easy to understand.</p>

<h2 id="section-4">产品及其它</h2>

<p><strong>Welcome Wagon: Classifying Comments on Stack Overflow</strong> 
 https://stackoverflow.blog/2018/07/10/welcome-wagon-classifying-comments-on-stack-overflow/<br />
Last month, Joe wrote about the Welcome Wagon work that we are doing to make Stack Overflow more welcoming and inclusive. Our current work involves projects across domains from asking questions to framing community standards and more; one project we have been working on is understanding how comments are used and misused on Stack Overflow.</p>

<p><strong>2018知识付费和在线教育从业者生存状况报告</strong><br />
https://mp.weixin.qq.com/s?__biz=MzI2NTY4MDg1NA==&amp;mid=2247492803&amp;idx=1&amp;sn=40c00b35884db60ebb6c30b5a15ae8dd<br />
知识付费和在线教育行业已经火了几年，期间虽然经历了一些起起伏伏，但整体的态势来看，可以称作是野蛮生长的几年。但行业发展到今天，却很少有人真正了解它的发展状况以及从业者的生存现状。基于此，三节课联合了新榜、多知网和荔枝微课，发起了《知识付费和在线教育从业者生存状况》的调查，一是希望帮助从业者了解整个行业的基本状况，了解自己的同行在做什么，想什么，同时也希望收集到的数据和一些结论能够对从业者的思考和决策有切实的帮助。</p>

<p>— THE END –</p>
---------------
<h1 id="#title_2" >3、CAP 定理的含义</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2018/07/cap.html](http://www.ruanyifeng.com/blog/2018/07/cap.html)
<p>分布式系统（distributed system）正变得越来越重要，大型网站几乎都是分布式的。</p>

        <p>分布式系统的最大难点，就是各个节点的状态如何同步。CAP 定理是这方面的基本定理，也是理解分布式系统的起点。</p>

<p>本文介绍该定理。它其实很好懂，而且是显而易见的。下面的内容主要参考了 Michael Whittaker 的。</p>

<h2>一、分布式系统的三个指标</h2>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018071607.jpg" alt="" title="" /></p>

<p>1998年，加州大学的计算机科学家 Eric Brewer 提出，分布式系统有三个指标。</p>

<blockquote>
  <ul>
<li>Consistency</li>
<li>Availability</li>
<li>Partition tolerance</li>
</ul>
</blockquote>

<p>它们的第一个字母分别是 C、A、P。</p>

<p>Eric Brewer 说，这三个指标不可能同时做到。这个结论就叫做 CAP 定理。</p>

<h2>二、Partition tolerance</h2>

<p>先看 Partition tolerance，中文叫做"分区容错"。</p>

<p>大多数分布式系统都分布在多个子网络。每个子网络就叫做一个区（partition）。分区容错的意思是，区间通信可能失败。比如，一台服务器放在中国，另一台服务器放在美国，这就是两个区，它们之间可能无法通信。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018071601.png" alt="" title="" /></p>

<p>上图中，G1 和 G2 是两台跨区的服务器。G1 向 G2 发送一条消息，G2 可能无法收到。系统设计的时候，必须考虑到这种情况。</p>

<p>一般来说，分区容错无法避免，因此可以认为 CAP 的 P 总是成立。CAP 定理告诉我们，剩下的 C 和 A 无法同时做到。</p>

<h2>三、Consistency</h2>

<p>Consistency 中文叫做"一致性"。意思是，写操作之后的读操作，必须返回该值。举例来说，某条记录是 v0，用户向 G1 发起一个写操作，将其改为 v1。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018071602.png" alt="" title="" /></p>

<p>接下来，用户的读操作就会得到 v1。这就叫一致性。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018071603.png" alt="" title="" /></p>

<p>问题是，用户有可能向 G2 发起读操作，由于 G2 的值没有发生变化，因此返回的是 v0。G1 和 G2 读操作的结果不一致，这就不满足一致性了。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018071604.png" alt="" title="" /></p>

<p>为了让 G2 也能变为 v1，就要在 G1 写操作的时候，让 G1 向 G2 发送一条消息，要求 G2 也改成 v1。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018071605.png" alt="" title="" /></p>

<p>这样的话，用户向 G2 发起读操作，也能得到 v1。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018071606.png" alt="" title="" /></p>

<h2>四、Availability</h2>

<p>Availability 中文叫做"可用性"，意思是只要收到用户的请求，服务器就必须给出回应。</p>

<p>用户可以选择向 G1 或 G2 发起读操作。不管是哪台服务器，只要收到请求，就必须告诉用户，到底是 v0 还是 v1，否则就不满足可用性。</p>

<h2>五、Consistency 和 Availability 的矛盾</h2>

<p>一致性和可用性，为什么不可能同时成立？答案很简单，因为可能通信失败（即出现分区容错）。</p>

<p>如果保证 G2 的一致性，那么 G1 必须在写操作时，锁定 G2 的读操作和写操作。只有数据同步后，才能重新开放读写。锁定期间，G2 不能读写，没有可用性不。</p>

<p>如果保证 G2 的可用性，那么势必不能锁定 G2，所以一致性不成立。</p>

<p>综上所述，G2 无法同时做到一致性和可用性。系统设计时只能选择一个目标。如果追求一致性，那么无法保证所有节点的可用性；如果追求所有节点的可用性，那就没法做到一致性。</p>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2018-07-16T08:48:47+08:00">2018年7月16日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>文集：</li>
<li>社交媒体：</li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------
<h1 id="#title_3" >4、文章： 组织变革中的恐慌成本</h1>
Oana Juncu
[http://www.infoq.com/cn/articles/cost-fear-change?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/cost-fear-change?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/cost-fear-change/zh/smallimage/cost-fear-organisational-change-logo-small2-1528803311161-1531634358002.jpg"/><p>在本文中，Oana 将对导致企业变革过程中恐慌心态的出现的因素进行分析，并指出这种恐慌所带来的成本，以及如何对现状进行挑战，最后为如何克服这些因素提出了针对性的建议。Oana 指出了四种常见的实践，表面上，这些实践能够降低风险。但实际上，他们反而加重了组织机构所页面的挑战。在这个不断发展和变化的时代，对于变革的适应能力是至关重要的。</p> <i>By Oana Juncu</i> <i> Translated by 邵思华</i>
---------------
<h1 id="#title_4" >5、视频演讲： 互联网文本内容安全：一种对抗式AI设计实践</h1>
王国印
[http://www.infoq.com/cn/presentations/an-adversarial-ai-design-practice?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/an-adversarial-ai-design-practice?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/presentations/an-adversarial-ai-design-practice/zh/mediumimage/wangguoyin270-1531534376164.jpg"/><p>涉黄、涉政、垃圾广告、违规违法交易等UGC评论严重制约业务健康发展，部分UGC评论屡屡触及监管红线。UGC垃圾评论随对抗而升级，变种不断涌现。腾讯云天御分别从降低人工审核量、构建数据闭环使得模型随对抗而自动升级从而降低研发投入、模型分布式按行存储使得GB级模型秒级更新等、三大维度搭建内容安全完整解决方案。本次分享将介绍互联网内容安全现状，腾讯云在大流量、强对抗场景下的算法设计思路和成功经验。
</p> <i>By 王国印</i>
---------------
<h1 id="#title_5" >6、视频演讲： Cloud Studio Beta 2.0 发布</h1>
张海龙
[http://www.infoq.com/cn/presentations/cloud-studio-beta-2-release?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/cloud-studio-beta-2-release?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/presentations/cloud-studio-beta-2-release/zh/mediumimage/zhanghailong270-1531482839660.jpg"/><p>现场将发布 Cloud Studio Beta 2.0 版本。Cloud Studio 将打造开发环境的生态系统，开发者在 Cloud Studio 里编辑好的环境可以保存上传到市场，其他开发者可以使用你配置的环境进行开发，并为此付费。现场演示下一代的研发工具，展现 Cloud Studio 带来未来的想象空间。</p> <i>By 张海龙</i>
---------------
<h1 id="#title_6" >7、The Holy Grail Of Reusable Components: Custom Elements, Shadow DOM, And NPM</h1>
Oliver Williams
[https://www.smashingmagazine.com/2018/07/reusable-components-custom-elements-shadow-dom-npm/](https://www.smashingmagazine.com/2018/07/reusable-components-custom-elements-shadow-dom-npm/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/07/reusable-components-custom-elements-shadow-dom-npm/" />
              <title>The Holy Grail Of Reusable Components: Custom Elements, Shadow DOM, And NPM</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>The Holy Grail Of Reusable Components: Custom Elements, Shadow DOM, And NPM</h1>
                  
                    
                    <address>Oliver Williams</address>
                  
                  <time datetime="2018-07-16T13:30:58&#43;02:00" class="op-published">2018-07-16T13:30:58+02:00</time>
                  <time datetime="2018-07-16T17:29:08&#43;00:00" class="op-modified">2018-07-16T17:29:08+00:00</time>
                </header>
                <p>For even the simplest of components, the cost in human-labour may have been significant. UX teams do usability testing. An array of stakeholders have to sign off on the design.</p>

<p>Developers conduct AB tests, accessibility audits, unit tests and cross-browser checks. Once you’ve solved a problem, <em>you don’t want to repeat that effort</em>. By building a reusable component library (rather than building everything from scratch), we can continuously utilize past efforts and avoid revisiting already solved design and development challenges.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fd61c2a7-6c87-42c0-864c-624bc0e0403f/materialcomponents.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fd61c2a7-6c87-42c0-864c-624bc0e0403f/materialcomponents.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fd61c2a7-6c87-42c0-864c-624bc0e0403f/materialcomponents.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fd61c2a7-6c87-42c0-864c-624bc0e0403f/materialcomponents.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fd61c2a7-6c87-42c0-864c-624bc0e0403f/materialcomponents.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fd61c2a7-6c87-42c0-864c-624bc0e0403f/materialcomponents.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fd61c2a7-6c87-42c0-864c-624bc0e0403f/materialcomponents.png"
			sizes="100vw"
			alt="A screenshot of Google’s material components website – showing various components."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>Building an arsenal of components is particularly useful for companies such as Google that own a considerable portfolio of websites all sharing a common brand. By codifying their UI into composable widgets, larger companies can both speed up development time and achieve consistency of both visual and user-interaction design across projects. There’s been a rise in interest in style guides and pattern libraries over the last several years. Given multiple developers and designers spread over multiple teams, large companies seek to attain consistency. We can do better than simple color swatches. <strong>What we need is easily distributable code</strong>.</p>

<h4>Sharing And Reusing Code</h4>

<p>Manually copy-and-pasting code is effortless. Keeping that code up-to-date, however, is a maintenance nightmare. Many developers, therefore, rely on a package manager to reuse code across projects. Despite its name, the Node Package Manager has become the unrivalled platform for <em>front-end</em> package management. There are currently over 700,000 packages in the NPM registry and <em>billions</em> of packages are downloaded every month. Any folder with a package.json file can be uploaded to NPM as a shareable package. While NPM is primarily associated with JavaScript, a package can include CSS and markup. NPM makes it easy to reuse and, importantly, <em>update</em> code. Rather than needing to amend code in myriad places, you change the code only in the package.</p>



<aside class="product-panel product-panel__tilted product-panel--book" data-audience="non-subscriber">
    <div class="container product-panel--book__container">
      <div class="panel__description panel__description--book">
    <p>Getting workflow <em>just</em> right ain’t an easy task. So are proper estimates. Or alignment among different departments. That’s why we’ve set up <strong>“this-is-how-I-work”-sessions</strong> — with smart cookies sharing what works well for them. A part of the , of course.</p>
      <a href="http://smashed.by/workflowpanelmembership" class="btn btn--green btn--large">
        Explore features&nbsp;→
      </a>
      </div>
      <div class="panel__image panel__image--book">
        <a href="http://smashed.by/workflowpanelmembership" class="books__book__image">
        <div class="books__book__img">
          <img src="https://www.smashingmagazine.com/images/smashing-cat/smashing-tv-box-cat.svg" alt="Smashing TV, with live sessions for professional designers and developers." width="310" height="400">
        </div>
      </a>
      </div>
    </div>
  </aside>




<h4>The Markup Problem</h4>

<p>Sass and Javascript are easily portable with the use of import statements. Templating languages give HTML the same ability &mdash; templates can import other fragments of HTML in the form of partials. You can write the markup for your footer, for example, just once, then include it in other templates. To say there exists a multiplicity of templating languages would be an understatement. Tying yourself to <em>just one</em> severely limits the potential reusability of your code. The alternative is to copy-and-paste markup and to use NPM only for styles and javascript.</p>

<p>This is the approach taken by the Financial Times with their </p>

<blockquote>“Once they copy that code they are essentially cutting a version which needs to be maintained indefinitely. When they copied the markup for a working component it had an implicit link to a snapshot of the CSS at that point. If you then update the template or refactor the CSS, you need to update all versions of the template scattered around your site.”</blockquote>

<h4>A Solution: Web Components</h4>

<p>Web components solve this problem by defining markup in JavaScript. The author of a component is free to alter markup, CSS, and Javascript. The consumer of the component can benefit from these upgrades without needing to trawl through a project altering code by hand. Syncing with the latest changes project-wide can be achieved with a terse <code>npm update</code> via terminal. Only the name of the component and its API need to stay consistent.</p>

<p>Installing a web component is as simple as typing <code>npm install component-name</code> into a terminal. The Javascript can be included with an import statement:</p>

<pre><code class="language-css">&lt;script type="module"&gt;
import './node_modules/component-name/index.js';
&lt;/script&gt;
</code></pre>

<p>Then you can use the component anywhere in your markup. Here is a simple example component that copies text to the clipboard.</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="KemvbM"
   data-user="cssgrid"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<p>A component-centric approach to front-end development has become ubiquitous, ushered in by Facebook’s React framework. Inevitably, given the pervasiveness of frameworks in modern front-end workflows, a number of companies have built component libraries using their framework of choice. Those components are reusable only within that particular framework.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d5cdd3ce-b918-405b-b709-0b6a9a60f5eb/reactonly.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d5cdd3ce-b918-405b-b709-0b6a9a60f5eb/reactonly.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d5cdd3ce-b918-405b-b709-0b6a9a60f5eb/reactonly.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d5cdd3ce-b918-405b-b709-0b6a9a60f5eb/reactonly.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d5cdd3ce-b918-405b-b709-0b6a9a60f5eb/reactonly.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d5cdd3ce-b918-405b-b709-0b6a9a60f5eb/reactonly.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d5cdd3ce-b918-405b-b709-0b6a9a60f5eb/reactonly.png"
			sizes="100vw"
			alt="A component from IBM’s Carbon Design System"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			A component from IBM’s Carbon Design System. For use in React applications only. Other significant examples of component libraries built in React include )
		</figcaption>
	
</figure>


<p>It’s rare for a sizeable company to have a uniform front-end and replatorming from one framework to another isn’t uncommon. Frameworks come and go. To enable the maximum amount of potential reuse across projects, we need components that are <em>framework agnostic</em>.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3cb17761-cd4a-4de8-aa1c-518eef1a6281/fragmented.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3cb17761-cd4a-4de8-aa1c-518eef1a6281/fragmented.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3cb17761-cd4a-4de8-aa1c-518eef1a6281/fragmented.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3cb17761-cd4a-4de8-aa1c-518eef1a6281/fragmented.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3cb17761-cd4a-4de8-aa1c-518eef1a6281/fragmented.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3cb17761-cd4a-4de8-aa1c-518eef1a6281/fragmented.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3cb17761-cd4a-4de8-aa1c-518eef1a6281/fragmented.png"
			sizes="100vw"
			alt="A screenshot from npmjs.com showing components that do that same thing built exclusively for particular javascript frameworks."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Searching for components via )
		</figcaption>
	
</figure>












<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f9d9a4a9-4ee2-4982-ac18-e3f3257bbe16/frameworkgraph.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f9d9a4a9-4ee2-4982-ac18-e3f3257bbe16/frameworkgraph.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f9d9a4a9-4ee2-4982-ac18-e3f3257bbe16/frameworkgraph.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f9d9a4a9-4ee2-4982-ac18-e3f3257bbe16/frameworkgraph.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f9d9a4a9-4ee2-4982-ac18-e3f3257bbe16/frameworkgraph.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f9d9a4a9-4ee2-4982-ac18-e3f3257bbe16/frameworkgraph.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f9d9a4a9-4ee2-4982-ac18-e3f3257bbe16/frameworkgraph.png"
			sizes="100vw"
			alt="A graph charting the popularity of frameworks over time. Ember, Knockout and Backbone have plunged in popularity, replaced by newer offerings."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The ever-changing popularity of frameworks over time. ()
		</figcaption>
	
</figure>


<blockquote>“I have built web applications using: Dojo, Mootools, Prototype, jQuery, Backbone, Thorax, and React over the years...I would love to have been able to bring that killer Dojo component that I slaved over with me to my React app of today.”<br /><br />&mdash; , Director of Engineering, Google</blockquote>

<p>When we talk about a web component, we are talking about the combination of a custom element with shadow DOM. Custom Elements and shadow DOM are part of both the W3C DOM specification and the WHATWG DOM Standard &mdash; <em>meaning web components are a web standard</em>. Custom elements and shadow DOM are <em>finally</em> set to achieve cross-browser support this year. By using a standard part of the native web platform, we ensure that our components can survive the fast-moving cycle of front-end restructuring and architectural rethinks. Web components can be used with any templating language and any front-end framework &mdash; they’re truly cross-compatible and interoperable. They can be used everywhere from a Wordpress blog to a single page application.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8727121e-eefc-44b8-8ef4-1b64f3bbb432/frameworkcompat.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8727121e-eefc-44b8-8ef4-1b64f3bbb432/frameworkcompat.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8727121e-eefc-44b8-8ef4-1b64f3bbb432/frameworkcompat.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8727121e-eefc-44b8-8ef4-1b64f3bbb432/frameworkcompat.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8727121e-eefc-44b8-8ef4-1b64f3bbb432/frameworkcompat.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8727121e-eefc-44b8-8ef4-1b64f3bbb432/frameworkcompat.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8727121e-eefc-44b8-8ef4-1b64f3bbb432/frameworkcompat.png"
			sizes="100vw"
			alt="The Custom Elements Everywhere project by Rob Dodson documents the interoperability of web components with various client-side Javascript frameworks."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The )
		</figcaption>
	
</figure>


<h3>Making A Web Component</h3>

<h4>Defining A Custom Element</h4>

<p>It's always been possible to make up tag-names and have their content appear on the page.</p>

<pre><code class="language-html">&lt;made-up-tag&gt;Hello World!&lt;/made-up-tag&gt;</code></pre>

<p>HTML is designed to be fault tolerant. The above will render, even though it’s not a valid HTML element. There’s never been a good reason to do this &mdash; deviating from standardized tags has traditionally been a bad practice. By defining a new tag using the custom element API, however, we can augment HTML with reusable elements that have built-in functionality. Creating a custom element is much like creating a component in React &mdash; but here were extending <code>HTMLElement</code>.</p>

<pre><code class="language-css">class ExpandableBox extends HTMLElement {
      constructor() {
        super()
      }
    }
</code></pre>

<p>A parameter-less call to <code>super()</code> must be the first statement in the constructor. The constructor should be used to set up initial state and default values and to set up any event listeners.  A new custom element needs to be defined with a name for its HTML tag and the elements corresponding class:</p>

<pre><code class="language-css">customElements.define('expandable-box', ExpandableBox)</code></pre>

<p>It’s a convention to capitalize class names. The syntax of the HTML tag is, however, more than a convention. What if browsers wanted to implement a new HTML element and they wanted to call it expandable-box? To prevent naming collisions, no new standardized HTML tags will include a dash. By contrast, the names of custom elements <em>have to</em> include a dash.</p>

<pre><code class="language-css">customElements.define('whatever', Whatever) // invalid
customElements.define('what-ever', Whatever) // valid
</code></pre>

<div class="sponsors__wide-place"></div>




<h4>Custom Element Lifecycle</h4>

<p>The API offers four custom element <em>reactions</em> &mdash; functions that can be defined within the class that will automatically be called in response to certain events in the lifecycle of a custom element.</p>

<p><strong>connectedCallback</strong> is run when the custom element is added to the DOM.</p>

<pre><code class="language-css">connectedCallback() {
    console.log("custom element is on the page!")
}
</code></pre>

<p>This includes adding an element with Javascript:</p>

<pre><code class="language-javascript">document.body.appendChild(document.createElement("expandable-box")) //“custom element is on the page”</code></pre>

<p>as well as simply including the element within the page with a HTML tag:</p>

<pre><code class="language-html">&lt;expandable-box&gt;&lt;/expandable-box&gt; // "custom element is on the page"</code></pre>

<p>Any work that involves fetching resources or rendering should be in here.</p>

<p><strong>disconnectedCallback</strong> is run when the custom element is removed from the DOM.</p>

<pre><code class="language-javascript">disconnectedCallback() {
    console.log("element has been removed")
}
document.querySelector("expandable-box").remove() //"element has been removed"
</code></pre>

<p><code>adoptedCallback</code> is run when the custom element is adopted into a new document. You probably don’t need to worry about this one too often.</p>

<p><code>attributeChangedCallback</code> is run when an attribute is added, changed, or removed. It can be used to listen for changes to both standardized native attributes like <em>disabled</em> or <em>src</em>, as well as any custom ones we make up. This is one of the most powerful aspects of custom elements as it enables the creation of a user-friendly API.</p>

<h4>Custom Element Attributes</h4>

<p>There are a great many HTML attributes. So that the browser doesn’t waste time calling our <code>attributeChangedCallback</code> when <em>any</em> attribute is changed, we need to provide a list of the attribute changes we want to listen for. For this example, we’re only interested in one.</p>

<pre><code class="language-javascript">static get observedAttributes() {
            return ['expanded']
        }
</code></pre>

<p>So now our <code>attributeChangedCallback</code> will only be called when we change the value of the expanded attribute on the custom element, as it’s the only attribute we’ve listed.</p>

<p>HTML attributes can have corresponding values (think <em>href, src, alt, value</em> etc) while others are either true or false (e.g. <em>disabled, selected, required</em>). For an attribute with a corresponding value, we would include the following within the custom element’s class definition.</p>

<pre><code class="language-javascript">get yourCustomAttributeName() {
  return this.getAttribute('yourCustomAttributeName');
}
set yourCustomAttributeName(newValue) {
  this.setAttribute('yourCustomAttributeName', newValue);
}
</code></pre>

<p>For our example element, the attribute will either be true or false, so defining the getter and setter is a little different.</p>

<pre><code class="language-javascript">get expanded() {
  return this.hasAttribute('expanded')
}
        
// the second argument for setAttribute is mandatory, so we’ll use an empty string
set expanded(val) {
  if (val) {
    this.setAttribute('expanded', '');
  }
  else {
    this.removeAttribute('expanded')
  }
}
</code></pre>

<p>Now that the boilerplate has been dealt with, we can make use of <code>attributeChangedCallback</code>.</p>

<pre><code class="language-javascript">attributeChangedCallback(name, oldval, newval) {
  console.log(`the ${name} attribute has changed from ${oldval} to ${newval}!!`);
  // do something every time the attribute changes
}
</code></pre>

<p>Traditionally, configuring a Javascript component would have involved passing arguments to an <code>init</code> function. By utilising the <code>attributeChangedCallback</code>, its possible to make a custom element that’s configurable just with markup.</p>

<p>Shadow DOM and custom elements can be used separately, and you may find custom elements useful all by themselves. Unlike shadow DOM, they <em>can</em> be polyfilled. However, the two specs work well in conjunction.</p>

<div class="sponsors__wide-place"></div>




<h4>Attaching Markup And Styles With Shadow DOM</h4>

<p>So far, we’ve handled the <em>behavior</em> of a custom element. In regard to markup and styles, however, our custom element is equivalent to an empty unstyled <code>&lt;span></code>. To encapsulate HTML and CSS as part of the component, we need to attach a shadow DOM. It’s best to do this within the constructor function.</p>

<pre class="break-out"><code class="language-javascript">class FancyComponent extends HTMLElement {
        constructor() {
            super()
            var shadowRoot = this.attachShadow({mode: 'open'})
            shadowRoot.innerHTML = `&lt;h2>hello world!&lt;/h2>`
            }
</code></pre>

<p>Don’t worry about understanding what the mode means &mdash; its boilerplate you have to include, but you’ll pretty much <em>always</em> want <code>open</code>. This simple example component will just render the text “hello world”. Like most other HTML elements, a custom element can have children &mdash; but not by default. So far the above custom element we’ve defined won’t render any children to the screen. To display any content between the tags, we need to make use of a <code>slot</code> element.</p>

<pre><code class="language-html">shadowRoot.innerHTML = `
&lt;h2&gt;hello world!&lt;/h2&gt;
&lt;slot&gt;&lt;/slot&gt;
`
</code></pre>

<p>We can use a style tag to apply some CSS to the component.</p>

<pre><code class="language-css">shadowRoot.innerHTML = 
`&lt;style&gt;
p {
color: red;
}
&lt;/style&gt;
&lt;h2&gt;hello world!&lt;/h2&gt;
&lt;slot&gt;some default content&lt;/slot&gt;`
</code></pre>

<p>These styles will only apply to the component, so we are free to make use of element selectors without the styles affecting anything else of the page. This simplifies writing CSS, making naming conventions like BEM unnecessary.</p>

<h4>Publishing A Component On NPM</h4>

<p>NPM packages are published via the command line. Open a terminal window and move into a directory that you would like to turn into a reusable package. Then type the following commands into the terminal:</p>

<ol>
<li>If your project doesn’t already have a , <code>npm init</code> will walk you through generating one.</li>
<li><code>npm adduser</code> links your machine to your NPM account. If you don’t have a preexisting account, it will create a new one for you.</li>
<li><code>npm publish</code></li>
</ol>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b594f06b-c102-49bd-9463-3caf5d742be7/terminal.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b594f06b-c102-49bd-9463-3caf5d742be7/terminal.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b594f06b-c102-49bd-9463-3caf5d742be7/terminal.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b594f06b-c102-49bd-9463-3caf5d742be7/terminal.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b594f06b-c102-49bd-9463-3caf5d742be7/terminal.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b594f06b-c102-49bd-9463-3caf5d742be7/terminal.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b594f06b-c102-49bd-9463-3caf5d742be7/terminal.png"
			sizes="100vw"
			alt="NPM packages are published via the command line"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>If all’s gone well, you now have a component in the NPM registry, ready to be installed and used in your own projects &mdash; and shared with the world.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ff9b48c4-72c9-49ae-829e-28e3611f322a/npm.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ff9b48c4-72c9-49ae-829e-28e3611f322a/npm.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ff9b48c4-72c9-49ae-829e-28e3611f322a/npm.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ff9b48c4-72c9-49ae-829e-28e3611f322a/npm.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ff9b48c4-72c9-49ae-829e-28e3611f322a/npm.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ff9b48c4-72c9-49ae-829e-28e3611f322a/npm.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ff9b48c4-72c9-49ae-829e-28e3611f322a/npm.png"
			sizes="100vw"
			alt="An example of a component in the NPM registry, ready to be installed and used in your own projects."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>The web components API isn’t perfect. Custom elements are currently unable to .</p>

<p>Although originally announced in 2011, browser support still isn’t universal. Firefox support is due later this year. Nevertheless, some high-profile websites (like Youtube) are already making use of them. Despite their current shortcomings, for <em>universally</em> shareable components they’re the singular option and in the future we can expect  to what they have to offer.</p>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(il, ra, yk)</span>
</div>


              </article>
            </body>
          </html>
---------------
<h1 id="#title_7" >8、30个案例告诉你，企业到底是怎么用区块链的</h1>
田宁宁
[http://www.infoq.com/cn/news/2018/07/bccon-30-solutions?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/bccon-30-solutions?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>这里有 30 个案例，或许会对你的业务决策有所帮助。</p> <i>By 田宁宁</i>
---------------
<h1 id="#title_8" >9、无代码方法和低代码方法如何为业务用户和专业开发人员提供支持</h1>
Ben Linders
[http://www.infoq.com/cn/news/2018/07/no-code-low-code?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/no-code-low-code?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>无代码方法旨在为业务人员开发和维护自己的应用程序提供支持，而低代码则是简化开发人员的工作，提高他们的生产力。两种方法都能以更低的成本实现更快速的开发。由于这些方法之间的差别越来越小，所以业务人员和开发人员可以合作，把它们结合在一起使用。</p> <i>By Ben Linders</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_9" >10、实体服务增加了系统复杂性</h1>
Andrew Morgan
[http://www.infoq.com/cn/news/2018/07/entity-services-complexity?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/entity-services-complexity?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>独立软件顾问Tareq Abedrabbo认为，实体服务是一种微服务反模式。主要是因为实体服务形成了浅模块，接口和功能之间的关系比较复杂。</p> <i>By Andrew Morgan</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_10" >11、NGINX Controller现已普遍可用</h1>
Andrew Morgan
[http://www.infoq.com/cn/news/2018/07/nginx-controllr?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/nginx-controllr?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>NGINX Controller是NGINX Plus实例的集中式监控和管理平台，现已普遍可用。它是NGINX应用平台的一部分，来自NGINX的一套企业产品。</p> <i>By Andrew Morgan</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_11" >12、微信小程序的下一步：支持NPM、小程序云、可视化编程、支持分包</h1>
覃云
[http://www.infoq.com/cn/news/2018/07/wchat-miniprog-support?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/wchat-miniprog-support?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>微信最新的数据显示，目前已发布小程序数量为100万+，小程序开发者已达150万+，小程序日均打开次数4次，主动访问的用户量为54%，从这些数据可以看出，小程序俨然已经成为微信生态体系中最重要的组成部分。 7月11日下午，微信公开课微信小程序技术专场在上海举行，会上，微信公布了面向开发者的技术规划，内容主要包括小程序技术能力与规划、小程序生态体系、小程序性能优化三个方面。</p> <i>By 覃云</i>
---------------