## 文章索引
1、 <a href="#1android-android-面试经验" >[Android] Android 面试经验</a><br/>
2、 <a href="#2android-android-中热修复框架-robust-原理解析-+-并将框架代码从-闭源-变成-开源上篇" >[Android]  Android 中热修复框架 Robust 原理解析 + 并将框架代码从 "闭源" 变成 "开源"(上篇)</a><br/>
3、 <a href="#3android-小-demo-大知识---控制-button-移动来学-android-坐标" >[Android] 小 Demo 大知识 - 控制 Button 移动来学 Android 坐标</a><br/>
4、 <a href="#4android-coordinatorlayout-子-view-之间的依赖管理机制-有向无环图" >[Android] CoordinatorLayout 子 View 之间的依赖管理机制 —— 有向无环图</a><br/>
5、 <a href="#5android-eventbus-30-源码分析" >[Android] EventBus 3.0 源码分析</a><br/>
6、 <a href="#6视频演讲-饿了么异构服务平台数据访问层的演进" >视频演讲： 饿了么异构服务平台数据访问层的演进</a><br/>
7、 <a href="#7前端-vuetify---vuejs-20-组建库" >[前端] Vuetify - Vue.js 2.0 组建库</a><br/>
8、 <a href="#8前端-web-storage-实用指南" >[前端] Web Storage 实用指南</a><br/>
9、 <a href="#9fex-技术周刊---2016/12/19" >FEX 技术周刊 - 2016/12/19</a><br/>
10、 <a href="#10设计-以微信为例谈谈产品设计的四大基本原则十大可用性原则情感化设计" >[设计] 以微信为例，谈谈产品设计的四大基本原则、十大可用性原则、情感化设计</a><br/>
11、 <a href="#11后端-张大胖改-bug" >[后端] 张大胖改 Bug</a><br/>
12、 <a href="#12后端-php-完整实战-23-种设计模式" >[后端] PHP 完整实战 23 种设计模式</a><br/>
13、 <a href="#13前端-230-行实现一个简单的-mvvm" >[前端] 230 行实现一个简单的 MVVM</a><br/>
14、 <a href="#14文章-解读2016之容器篇已死和永生" >文章： 解读2016之容器篇：“已死”和“永生”</a><br/>
15、 <a href="#15文章-net异常设计原则" >文章： .NET异常设计原则</a><br/>
16、 <a href="#16文章-学会用spark实现朴素贝叶斯算法" >文章： 学会用Spark实现朴素贝叶斯算法</a><br/>
17、 <a href="#17视频演讲-百亿级通用推荐系统实践" >视频演讲： 百亿级通用推荐系统实践</a><br/>
18、 <a href="#1858集团cto邢宏宇58的技术演进之路" >58集团CTO邢宏宇：58的技术演进之路</a><br/>
19、 <a href="#19一个实践如何提升云主机稳定性及防御能力" >一个实践：如何提升云主机稳定性及防御能力</a><br/>
20、 <a href="#20人工智能周报第四期" >人工智能周报（第四期）</a><br/>
21、 <a href="#21facebook针对图数据处理对apache-giraph-和-spark-graphx的比较" >Facebook针对图数据处理对Apache Giraph 和 Spark GraphX的比较</a><br/>
22、 <a href="#22infoq采访http/2的早期采用者lawyercom" >InfoQ采访HTTP/2的早期采用者Lawyer.com</a><br/>
23、 <a href="#23微软宣布cortana小娜对第三方开放" >微软宣布Cortana小娜对第三方开放</a><br/>
24、 <a href="#24老牌巨头公司的持续创新探寻网易杭研的三重职能" >老牌巨头公司的持续创新，探寻网易杭研的三重职能</a><br/>
25、 <a href="#25the-not-so-secret-powers-of-the-mobile-browser" >The (Not So) Secret Powers Of The Mobile Browser</a><br/><h1 id="#title_0" >1、[Android] Android 面试经验</h1>
Jomeslu
[https://gold.xitu.io/entry/5858730e8d6d810065bf06f2](https://gold.xitu.io/entry/5858730e8d6d810065bf06f2)
<p>一个小伙伴单位面试经验。</p><p></p>
---------------
<h1 id="#title_1" >2、[Android]  Android 中热修复框架 Robust 原理解析 + 并将框架代码从 "闭源" 变成 "开源"(上篇)</h1>
peter2016
[https://gold.xitu.io/entry/5857bb2a128fe1006b7e01e2](https://gold.xitu.io/entry/5857bb2a128fe1006b7e01e2)
<p>Android 中热修复框架比较多，每家公司都有对应的方案和框架，比如阿里的 AndFix 框架，关于这个框架在之前的文章已经详细讲解了，不了解的同学可以点击这里：AndFix 热修复框架原理分析 。本文继续来看另外一个热修复框架，也就是美团团队开发的 Robust 框架。关于这个框架网上已经有详细解释了，具体用法也有。不过他没有开源，所以本文就先简单介绍他的原理，用一个案例来演示这个框架的作用，但是重点是咋们自己编码将其框架机制实现，让其 "闭源" 变成 "开源"。</p><p></p>
---------------
<h1 id="#title_2" >3、[Android] 小 Demo 大知识 - 控制 Button 移动来学 Android 坐标</h1>
青蛙ing
[https://gold.xitu.io/entry/5857fd1c128fe1006dc483bd](https://gold.xitu.io/entry/5857fd1c128fe1006dc483bd)
<img src="https://dn-mhke0kuv.qbox.me/f2864e7c16286b38ce18.jpg?imageView/2/w/800/h/600/q/80/format/png"/><p>发表在简书写的小 Demo 解说。控制 Button 移动来学 Android 坐标，其中特别是涉及到状态栏高度及标题栏高度。从而熟悉不同坐标系。</p><p></p>
---------------
<h1 id="#title_3" >4、[Android] CoordinatorLayout 子 View 之间的依赖管理机制 —— 有向无环图</h1>
梁山boy
[https://gold.xitu.io/entry/5858126961ff4b006cb1bac4](https://gold.xitu.io/entry/5858126961ff4b006cb1bac4)
<img src="https://dn-mhke0kuv.qbox.me/38e5d311091034511d3d.jpg?imageView/2/w/800/h/600/q/80/format/png"/><p>这几天接触了 CoordinatorLayout 和所谓 layout_behavior，然后进一步理了一遍源码。有两点惊艳到了我，一个是嵌套滑动机制，再一个便是依赖管理机制。

对于嵌套滑动 NestedScroll 的分析，网上有挺多博客。那本文打算从依赖管理的角度来讲一些东西。</p><p></p>
---------------
<h1 id="#title_4" >5、[Android] EventBus 3.0 源码分析</h1>
maimingliang
[https://gold.xitu.io/entry/5857d31b61ff4b00686cb307](https://gold.xitu.io/entry/5857d31b61ff4b00686cb307)
<img src="https://dn-mhke0kuv.qbox.me/4b959f1d9627f9c89a94.png?imageView/2/w/800/h/600/q/80/format/png"/><p>EventBus 3.0 源码分析</p><p></p>
---------------
<h1 id="#title_5" >6、视频演讲： 饿了么异构服务平台数据访问层的演进</h1>
徐东焱
[http://www.infoq.com/cn/presentations/eleme-heterogeneous-service-platform-data-access-layer?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/eleme-heterogeneous-service-platform-data-access-layer?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/eleme-heterogeneous-service-platform-data-access-layer/zh/mediumimage/xudongyan1_270.jpg"/><p>饿了么数据访问层（DAL）基于 IO.Netty 实现的高并发、高吞吐量的 Java 服务，不同于通常前段异步，后端同步的模式，饿了么数据访问层（DAL）在客户端连接和 DB 连接都使用了异步 IO 处理 SQL 请求和结果集。目前集群峰值 SQL 请求量约 10 万/s。除了作为数据库代理的基本功能，本次主题主要介绍 DAL 在大型综合网站中以最小侵入代价对产研开发的支持、为数据库提供主动防护的特性、对网站线上排障的支持，以及在实际应用中所遇到的问题和应对措施。</p> <i>By 徐东焱</i>
---------------
<h1 id="#title_6" >7、[前端] Vuetify - Vue.js 2.0 组建库</h1>
kalasoo
[https://gold.xitu.io/entry/5858052a128fe1006b805e07](https://gold.xitu.io/entry/5858052a128fe1006b805e07)
<img src="https://dn-mhke0kuv.qbox.me/82c10d4ee984bfa46a5f.png?imageView/2/w/800/h/600/q/80/format/png"/><p>Material Design 的前端组建库，基于 Vue.js 2.0</p><p></p>
---------------
<h1 id="#title_7" >8、[前端] Web Storage 实用指南</h1>
阿希Mario
[https://gold.xitu.io/entry/5857c03a8e450a006c75e932](https://gold.xitu.io/entry/5857c03a8e450a006c75e932)
<img src="https://dn-mhke0kuv.qbox.me/f2ee0868b7784002afd1.jpg?imageView/2/w/800/h/600/q/80/format/png"/><p>关于 Web Storage 使用的那些事</p><p></p>
---------------
<h1 id="#title_8" >9、FEX 技术周刊 - 2016/12/19</h1>

[http://fex.baidu.com/blog/2016/12/fex-weekly-19//](http://fex.baidu.com/blog/2016/12/fex-weekly-19//)
作者：2betop <br> <p>微信搜索『FEX』关注我们的公众号，及时获得最新资讯。</p>

<h2 id="section">业界会议</h2>

<p><strong>第11届D2前端技术论坛 - 12.17</strong><br />
http://d2forum.alibaba-inc.com/#/index?_k=fclt5x<br />
D2为国内前端领域的开发者和设计者，以及所有对前端技术感兴趣的人提供一个交流的机会，以技术会友，一起分享技术的乐趣，探讨行业的发展。十届是一次轮回，十一届的主题定为“初心”，近10年来，前端领域风云涌动，移动终端领域突飞猛进，web全栈势不可挡，作为距离用户最近的工程师，我们回望“初心”，不惧未来。</p>

<p><strong>中国第三届CSS开发者大会 - 12.17</strong><br />
https://css.w3ctech.com/<br />
围绕 CSS Grid Layout、Sass &amp; CSS Design<br />
Pattern、SVG工程化、SVG动画、微信网页重构实践、WebGL 等话题展开。</p>

<p><strong>GOPS2016全球运维大会北京站- 12.16-17</strong><br />
http://gops2016-beijing-tcwechatshare.eventdove.com/<br />
主题是：DevOps 2.0，node.js 及全栈的推进使得运维也逐渐成为前端需要关注的内容，可以关注下业界的最新成果。附：</p>

<h2 id="section-1">深阅读</h2>

<p><strong>20 Years of CSS</strong><br />
https://www.w3.org/Style/CSS20/<br />
On December 17, 1996, W3C published the first standard for CSS. And thus from December 17, 2016 until one year later, CSS is 20 years old. Read more about .</p>

<p><strong>V8 ❤️ Node.js</strong></p>

<p>http://v8project.blogspot.com/2016/12/v8-nodejs.html<br />
Node’s popularity has been growing steadily over the last few years, and we have been working to make Node better. This blog post highlights some of the recent efforts in V8 and DevTools.</p>

<p><strong>npm@5, specifications, and our RFC process</strong><br />
http://blog.npmjs.org/post/154473364440/npm5-specifications-and-our-rfc-process<br />
Before the release of Node.js 8, we intend to ship npm@5: a faster client, as measured by benchmarking and profiling tools available to everyone; a much improved version of npm-shrinkwrap.json, npm’s lockfile. In particular, shrinkwrap was originally intended to be a finalizing tool used prior to deployment, but we intend the new shrinkwrap to be used for the entire lifecycle of your JavaScript applications; new tools intended for use with upcoming registry features.</p>

<p><strong>it’s going to be Angular 4.0, or just Angular</strong><br />
http://angularjs.blogspot.com/2016/12/ok-let-me-explain-its-going-to-be.html<br />
Why Angular 4?? Why even Angular 3?? What is going on?</p>

<p><strong>Prefer DEFER Over ASYNC - by Steve Souders</strong><br />
http://calendar.perfplanet.com/2016/prefer-defer-over-async/<br />
In this article, I make the argument that DEFER should be the default choice over ASYNC. To set the stage, I’m going to review how browsers evolved to make scripts faster with preloaders and the motivation for the ASYNC and DEFER attributes.</p>

<p><strong>How Creating A Design Language Can Streamline Your UX Design Process</strong><br />
https://www.smashingmagazine.com/2016/12/how-creating-a-design-language-can-streamline-your-ux-design-process/<br />
Around a year ago, while working at a digital agency, I was given the objective of streamlining our UX design process. Twelve months later, this article shares my thoughts and experiences on how lean thinking helped to instill efficiencies within our UX design process.</p>

<p><strong>The Inner Workings Of Virtual DOM</strong><br />
https://medium.com/@rajaraodv/the-inner-workings-of-virtual-dom-666ee7ad47cf#.lvgg5l8mj<br />
Virtual DOM (VDOM aka VNode) is magical ✨ but is also complex and hard to understand. React, Preact and similar JS libraries use them in their core. Unfortunately I couldn’t find any good article or doc that explains it in a detailed-yet-simple-to-understand fashion. So I thought of writing one myself.</p>

<p><strong>The JS Community has a Bullying Problem</strong><br />
https://medium.com/javascript-scene/the-js-community-has-a-bullying-problem-96c10f11c85d#.bly6zilv1<br />
JavaScript has grown up. It’s time for the community to grow up with it. We need a lot less negativity and a lot more positivity in our community. The last thing we need to do is drive our most positive, selfless, helpful voices away.</p>

<p><strong>Linux Kernel 4.9 中的 BBR 算法与之前的 TCP 拥塞控制相比有什么优势</strong><br />
https://www.zhihu.com/question/53559433/answer/135903103<br />
中国科大的同学在 LUG HTTP 代理服务器上部署了 Linux 4.9 的 TCP BBR 拥塞控制算法。从科大的移动出口到新加坡 DigitalOcean 的实测下载速度从 647 KB/s 提高到了 22.1 MB/s，附：。</p>

<p><strong>JavaScript Clean Coding Best Practices - Node.js at Scale</strong><br />
https://blog.risingstack.com/javascript-clean-coding-best-practices-node-js-at-scale/<br />
Writing clean code is what you must know and do in order to call yourself a professional developer. There is no reasonable excuse for doing anything less than your best. In this blog post, we will cover general clean coding principles for naming and using variables &amp; functions, as well as some JavaScript specific clean coding best practices.</p>

<p><strong>When everything’s important, nothing is</strong><br />
https://aerotwist.com/blog/when-everything-is-important-nothing-is/<br />
关于性能优化的实践，重点讨论了 Server-Side-Rendering 和 Client-Side-Rendering 的对 First Meaningful Paint (‘FMP’) 和 Time to Interactive (‘TTI’) 的影响。</p>

<p><strong>2016年前端技术观察</strong><br />
http://geek.csdn.net/news/detail/128912<br />
https://www.zhihu.com/question/53625757<br />
阿当老师的一篇文章又引发业界轩然大波，抛开文章对主流前端技术的一些主观判断，这几个观点还是不错的：技术选型要考虑个人开发还是团队合作；技术方案不会只有优点而没缺点，做任何的技术选型都是在对优点和缺点做权衡；任何一个领域的开发，要掌握的知识都是多方位的，语言只是其中之一而已；不要迷信任何权威；基础很重要。他的另一篇后续文：。</p>

<p><strong>[译]2017 年你应该学习的编程语言、框架和工具</strong><br />
https://zhuanlan.zhihu.com/p/24369470<br />
回顾 2016 年，我们看到了更多新兴的流行语言、框架和工具，它们改变着我们的工作方式，让我们看到更多的可能。但在这个行业，紧随潮流是很难的。所以在每年年底，我们都会给你提供一些建议，它涉及什么是最重要的，以及你在未来一年中应该学习什么。另附：</p>

<p><strong>双11的极限挑战——5个极致目标教你玩转前端栈</strong><br />
https://yq.aliyun.com/articles/66106<br />
双11中的前端的极限挑战，包括前端栈，5个极致目标（从后到前的100%可用、秒开体验、AR和3D体验、可视的体验监控、人性化的无障碍端体验）的实现过程和方法，以及前端未来的发展。</p>

<p><strong>初识 Dva</strong><br />
https://github.com/pigcan/blog/issues/2<br />
https://github.com/dvajs/dva<br />
近期，我们在内部做了一个类似 IDE 性质的应用，基于 electron 和 dva，由于之前一直只关注 node 相关的开发者工具，并未太多接触 React 等内容，所以这段时间过的有点煎熬同时也很兴奋，煎熬来源于非舒适区，而兴奋来源于发现基于 dva + electron 给开发者工具带来了更多的可能性。</p>

<p><strong>vue-cli#2.0 webpack 配置分析</strong><br />
https://github.com/DDFE/DDFE-blog/issues/10<br />
滴滴的同学似乎在大规模使用 vue，近期给出了多个源码解析文章，对学习和了解 vue 挺有帮助的。</p>

<p><strong>一个拼写错误引来的讨论</strong></p>

<p>https://github.com/visionmedia/debug/issues/347#issuecomment-266959055<br />
npm 上的新版 debug 由于拼写问题导致报错，影响了无数依赖的项目，也引发了大量讨论，很多人吐槽没有静态检查和持续集成，后来连 tj 大神也现身了，吐槽开源项目难做。。。其实吧，比尔盖茨在文革结束那年早就预测到了</p>

<p><strong>Why we chose Vue.js over React</strong><br />
http://pixeljets.com/blog/why-we-chose-vuejs-over-react<br />
We have pretty big codebase, mostly PHP&amp;JS. We decided to use Vue.js after we’ve completed evaluation of modern frameworks: we’ve built our customer calculator on React, Vue.js and Angular2. 另外，还有从  。</p>

<p><strong>跨平台 ListView 性能优化</strong><br />
https://mp.weixin.qq.com/s/FbiSLPxFdGqJ00WgpJ94yw<br />
详细分析了 RN、Weex 下 ListView 的性能问题及优化</p>

<p><strong>Saving the internet 2000 terabytes a day: fixing Font Awesome’s fonts</strong><br />
https://pixelambacht.nl/2016/font-awesome-fixed/<br />
优化 Font Awesome 的体积</p>

<p><strong>浅析渲染引擎与前端优化</strong><br />
http://jdc.jd.com/archives/2806<br />
根据渲染原理来介绍如何优化性能</p>

<p><strong>使用 Enzyme 测试 React（Native）组件</strong><br />
https://blog.jimmylv.info/2016-12-07-react-testing-with-enzyme/<br />
React 测试框架的介绍</p>

<p><strong>微信读书 iOS 质量保证及性能监控</strong><br />
http://wereadteam.github.io/2016/12/12/Monitor/</p>

<p>在使用微信读书的过程中，我们也碰到过app随机丢失动画、用户反馈app卡死、用户投诉看不了书籍等等的问题，这些问题都严重影响使用，也会降低产品口碑，因此我们开发了一些监控工具来解决这些问题，在这里总结和分享一下。</p>

<p><strong>解读2016之Golang篇：极速提升，逐步超越</strong></p>

<p>http://www.infoq.com/cn/articles/2016-review-go?winzoom=1<br />
Go语言从原先的第50多位经过多次上窜已经跃到了第13位，跻入绝对主流的编程语言的行列！下面就带领大家一起回顾一下Go语言在2016年做出的那些大动作。</p>

<h2 id="section-2">新鲜货</h2>

<p><strong>TypeORM</strong><br />
https://github.com/typeorm/typeorm<br />
TypeORM is an Object Relational Mapper (ORM) for node.js written in TypeScript that can be used with TypeScript or JavaScript (ES5, ES6, ES7). Its goal to always support latest JavaScript features and provide features that help you to develop any kind of applications that use database - from small applications with a few tables to large scale enterprise applications.</p>

<p><strong>react-redux v5.0.0</strong><br />
https://github.com/reactjs/react-redux/releases/tag/v5.0.0<br />
Backwards compatible API; Major internal changes; Significant performance improvements in common usage patterns; Additional features added to connect(); New connectAdvanced() API;</p>

<p><strong>RxJS 5</strong></p>

<p>https://github.com/ReactiveX/rxjs<br />
This is a rewrite of Reactive-Extensions/RxJS and is intended to supersede it once this is ready. This rewrite is meant to have better performance, better modularity, better debuggable call stacks, while staying mostly backwards compatible, with some breaking changes that reduce the API surface.</p>

<p><strong>webpack 2.2: The Release Candidate</strong><br />
https://medium.com/webpack/webpack-2-2-the-release-candidate-2e614d05d75f#.sv5w97osa<br />
webpack 2.2.0-rc.0 is available to download right now: npm install webpack@beta –save-dev</p>

<p><strong>Voca - The ultimate JavaScript string library</strong><br />
https://vocajs.com/</p>

<p>The Voca library offers helpful functions to make string manipulations comfortable: change case, trim, pad, slugifly, latinise, sprintf’y, truncate, escape and much more. The modular design allows to load the entire library, or individual functions to minimize the application builds. The library is fully tested, well documented and long-term supported.</p>

<p><strong>Visual Studio Code</strong><br />
https://code.visualstudio.com/updates/v1_8<br />
细节改进非常多</p>

<p><strong>Chrome 56 Beta Ships With WebGL 2.0 Enabled By Default &amp; Much More</strong><br />
https://blog.chromium.org/2016/12/chrome-56-beta-not-secure-warning-web.html<br />
WebGL 2.0 终于来了</p>

<p><strong>Weex 进入 Apache 基金会孵化阶段</strong><br />
http://mp.weixin.qq.com/s/00ccnbbIaf2JksqaesICSQ<br />
12月15日，阿里巴巴宣布将 Weex 捐赠给Apache基金会开始孵化，Weex有望成为中国移动领域的首个Apache顶级项目。</p>

<p><strong>Polymer is the whole package</strong><br />
https://wearenorthern.com/blog/2016/polymer-is-the-whole-package/<br />
可以了解下 ployer 生态</p>

<p><strong>2016 in Jest</strong><br />
https://facebook.github.io/jest/blog/2016/12/15/2016-in-jest.html<br />
2016 was a big year for JavaScript testing with Jest. In the first six months of the year we rewrote Jest and built a solid foundation to significantly improve performance and the developer experience of testing JavaScript code.</p>

<p><strong>roadhog —— 让 create-react-app 可配的命令行工具</strong><br />
https://github.com/sorrycc/blog/issues/15<br />
roadhog 是一个 cli 工具，提供 server 和 build 两个命令，分别用于本地调试和构建。命令行体验和 create-react-app 一致，配置略有不同，比如默认开启 css modules，然后还提供了 JSON 格式的配置方式。</p>

<p><strong>BROWSIX - UNIX IN YOUR BROWSER TAB</strong><br />
https://browsix.org/<br />
Run C, C++, Go and Node.js programs as processes in browsers, including LaTeX, GNU Make, Go HTTP servers, and POSIX shell scripts.</p>

<p><strong>Hyper™ 1.0.0 发布</strong><br />
https://www.oschina.net/news/79981/hyper-1-0-0<br />
Hyper™ 1.0.0 发布了，Hyper™ 是一款 JS / HTML/ CSS 终端工具。该项目旨在为用户创建一个美观的、易于扩展的命令行接口工具，并且构建一个开放式 Web 标准。</p>

<p><strong>gitql - A git query language</strong><br />
https://github.com/cloudson/gitql<br />
Gitql doesn’t want kill git log. It was created just for science!!<br />
It’s read-only. Nothing about delete, insert or update commits.</p>

<p><strong>redux-orm</strong><br />
https://github.com/tommikaikkonen/redux-orm<br />
A small, simple and immutable ORM to manage relational data in your Redux store.</p>

<h2 id="section-3">产品及其它</h2>

<p><strong>谷歌拿什么PK后发制人的巨头亚马逊</strong><br />
http://mp.weixin.qq.com/s?__biz=MjM5MTM5ODQyMA==&amp;mid=2651194595&amp;idx=1&amp;sn=6f5223c6ccaa0cebce5889e49a402764<br />
文中云计算的一些理念挺不错的，比如：AWS 本身是一套可持续演进的系统。它能够在不停机、不瘫痪的情况下就完成大幅度升级和大规模客户转移等任务，让企业级客户安享 7x24 小时不间断的服务，无需担心自己会受到影响；AWS 提供给用户的，不是框架（frameworks）而是“基元”（primitives），利用这些“基元”，客户自己也可按照具体需要，构建出种种可持续演进、可持续扩展的（scalable）后端系统；当分配成本（distribution cost）或转换成本（switching cost）下降时，用户体验的重要性就会上升，利用 Kubernetes，谷歌希望能创建一个完全不受控于云基础设施的浏览器，然后降低转换成本。</p>

<p><strong>知乎在移动端的艰难与它错过的一个时代</strong><br />
http://mp.weixin.qq.com/s?__biz=MjM5NDUyOTAwOA==&amp;mid=2652914245&amp;idx=1&amp;sn=72e4ec6a763703da60f7c77407817291<br />
以2016年为时间维度的话，毫无疑问，知乎的商业化是2016年中国互联网圈内不容忽视的一个产品大事件。<br />
但，如果我们退后一步，将知乎上线的6年作为一个整体来看待，我们将会发现，知乎的6年，也正恰好是移动互联网最狂飙突进的6年。那么，知乎在移动化这件事情上，又做得怎么样呢？</p>

<p><strong>在技术概念的大爆发中何以自处</strong><br />
http://mp.weixin.qq.com/s?__biz=MjM5MDE0Mjc4MA==&amp;mid=2650995079&amp;idx=1&amp;sn=b7f5bd64614c1ef487766ffc5af56aed<br />
腾讯Web前端技术级别最高的程序员黄希彤结合他10多年的经历分享了对技术的看法：</p>

<ul>
  <li>工程师的天职是「解决问题」，我们要关心的是新的技术是否赋予另了我们新的解决问题的能力，让我们能够解决以前不能解决的问题，在掌握了基础的编程能力的基础上，更加专注于有哪些问题是前人没解决的；</li>
  <li>基于云去思考和架构系统的方式，现在我们也常常称为「云原生」，这样的思考方式会极大提升我们前端工程师和全栈工程师解决问题的能力；</li>
  <li>我们使用的很多技术将来都会被淘汰，我们做的很多产品将来都会过时，真正能让我们牛的，应该是那些可以经得起时间考验的技术实践；</li>
</ul>
---------------
<h1 id="#title_9" >10、[设计] 以微信为例，谈谈产品设计的四大基本原则、十大可用性原则、情感化设计</h1>
AleCC
[https://gold.xitu.io/entry/5858015a61ff4b006cb11fd4](https://gold.xitu.io/entry/5858015a61ff4b006cb11fd4)
<img src="https://dn-mhke0kuv.qbox.me/22ea2800c4562e4b324e.jpg?imageView/2/w/800/h/600/q/80/format/png"/><p>文章以微信为案例，谈谈产品设计的四大基本原则、十大可用性原则、情感化设计。</p><p></p>
---------------
<h1 id="#title_10" >11、[后端] 张大胖改 Bug</h1>
刘欣
[https://gold.xitu.io/entry/5857cd6b8e450a006cb10450](https://gold.xitu.io/entry/5857cd6b8e450a006cb10450)
<img src="https://dn-mhke0kuv.qbox.me/5b2d41e286fef7c3aa5a.jpg?imageView/2/w/800/h/600/q/80/format/png"/><p>表面光鲜，内部腐烂，面对这样的代码，张大胖该怎么办？</p><p></p>
---------------
<h1 id="#title_11" >12、[后端] PHP 完整实战 23 种设计模式</h1>
TIGERB
[https://gold.xitu.io/entry/5857b81b1b69e60056ec2f55](https://gold.xitu.io/entry/5857b81b1b69e60056ec2f55)
<img src="https://dn-mhke0kuv.qbox.me/381347a09921c3a71756.jpg?imageView/2/w/800/h/600/q/80/format/png"/><p>设计模式是面向对象的最佳实践</p><p></p>
---------------
<h1 id="#title_12" >13、[前端] 230 行实现一个简单的 MVVM</h1>
mirone
[https://gold.xitu.io/entry/5857e419128fe1006b7f5952](https://gold.xitu.io/entry/5857e419128fe1006b7f5952)
<p>MVVM 这两年在前端届掀起了一股热潮，火热的 Vue 和 Angular 带给了开发者无数的便利，本文将实现一个简单的 MVVM，用 200 多行代码探索 MVVM 的秘密。</p><p></p>
---------------
<h1 id="#title_13" >14、文章： 解读2016之容器篇：“已死”和“永生”</h1>
张磊
[http://www.infoq.com/cn/articles/interpretation-of-2016-container?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/interpretation-of-2016-container?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/interpretation-of-2016-container/zh/smallimage/logo.jpg"/><p>2016年，容器技术圈子依然热闹非凡，容器社区里的弄潮儿们在“is dead”和“long live”的悖论里不断地自我否定和进化已成为这个社区所独有的常态。Docker公司“萌萌哒”的鲸鱼背后，一只野心勃勃的海洋霸主正蓄势待发；而作为容器编排管理领域的领导者，纵使有Google、Redhat等巨头的撑腰，Kubernetes恐怕也不会放慢脚步，通过CRI联合CNCF、OCI两大开源社区举措也在情理之中。容器技术的圈子里容不得懈怠，Mesos生态已经开始励精图治，意在凭借独有的能力拿回昔日的地位。我们不难发现，在Docker公司向平台领域发展的同时，Kubernetes、Mesos也同样渗透进了容器运行时的范畴。实际上，正如同那些支付宝与微信之争，几个大佬原生的核心能力恐怕才是它们取得今天成绩的关键所在。作为终端用户，理清自身真实需求之后，做出适合自己的选择其实并不太难。</p> <i>By 张磊</i>
---------------
<h1 id="#title_14" >15、文章： .NET异常设计原则</h1>
Jonathan Allen
[http://www.infoq.com/cn/articles/Exceptions-API-Design?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/Exceptions-API-Design?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/Exceptions-API-Design/zh/smallimage/logo.jpg"/><p>异常是使用.NET时必然会遇到的问题，但是，有太多的开发人员没有从API设计的角度考虑这个问题。在大部分工作中，他们自始至终都知道需要捕获什么异常以及哪些异常需要写入全局日志。如果你设计了可以让你正确使用异常的API，则可以显著减少修复缺陷的时间。</p> <i>By Jonathan Allen</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_15" >16、文章： 学会用Spark实现朴素贝叶斯算法</h1>
汪榕
[http://www.infoq.com/cn/articles/use-spark-to-achieve-naive-bayesian-algorithm?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/use-spark-to-achieve-naive-bayesian-algorithm?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/use-spark-to-achieve-naive-bayesian-algorithm/zh/smallimage/logo 112 (1).jpg"/><p>本文作者汪榕曾写过一篇文章：《以什么姿势进入数据挖掘会少走弯路》，是对想入行大数据的读者的肺腑之言，其中也表达了作者的一些想法，希望大家不要随便去上没有结合业务的收费培训班课程；而后，他有了结合他本人的工作经验，写一系列帮助大家进行实践学习课程文章的想法，InfoQ也觉得这是件非常有意义的事情，特别是对于大数据行业1-3年工作经验的人士，或者是没有相关工作经验但是想入行大数据行业的人。课程的名称是“数据挖掘与数据产品的那些事”。这系列文章会在InfoQ上形成一个专栏，本文是专栏的第二篇。</p> <i>By 汪榕</i>
---------------
<h1 id="#title_16" >17、视频演讲： 百亿级通用推荐系统实践</h1>
吕慧伟
[http://www.infoq.com/cn/presentations/practice-of-universal-recommendation-system?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/practice-of-universal-recommendation-system?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/practice-of-universal-recommendation-system/zh/mediumimage/lvhuiwei270.jpg"/><p>神盾通用推荐系统的设计和架构。
日均百亿推荐请求的挑战及如何重构实时计算系统来应对。
神盾推荐在腾讯 SNG 社交网络运营部的应用和实践。
腾讯云推荐引擎的架构和解决方案。</p> <i>By 吕慧伟</i>
---------------
<h1 id="#title_17" >18、58集团CTO邢宏宇：58的技术演进之路</h1>
曹倩芸
[http://www.infoq.com/cn/news/2016/12/58-technology-evolution?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2016/12/58-technology-evolution?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>2015年到2016年，58集团在整个业务和战略层面面临了几项大的挑战：一是各平台间整合后如何发挥协同优势，如何搭建适应各个业务线发展的大平台+垂直的业务模型；二是经过十年的高速发展，如何在产品、技术体系和架构仍存在诸多问题的情况下让业务跑的更快；三是怎样从此前的分类信息服务过渡到垂直化业务模式。</p> <i>By 曹倩芸</i>
---------------
<h1 id="#title_18" >19、一个实践：如何提升云主机稳定性及防御能力</h1>
曹倩芸
[http://www.infoq.com/cn/news/2016/12/cloud-host-iops-defense?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2016/12/cloud-host-iops-defense?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>云计算时代到来，IDC行业的服务商和用户也开始成批转向IaaS服务。从国内IaaS服务目前的应用形式来看，云主机、云存储用户采用率最高，使用比例达70%以上。</p> <i>By 曹倩芸</i>
---------------
<h1 id="#title_19" >20、人工智能周报（第四期）</h1>
戴民@TalkingData
[http://www.infoq.com/cn/news/2016/12/Artificial-Intelligence-Weekly-4?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2016/12/Artificial-Intelligence-Weekly-4?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>人工智能周报，为大家带来全球大数据产业及周边行业最新的咨询动态以及领袖观点。期待和大家一起不断找到海外数据技术和方案在国内落地的灵感，让每个大数据人同步在人工智能领域的世界前沿。</p> <i>By 戴民@TalkingData</i>
---------------
<h1 id="#title_20" >21、Facebook针对图数据处理对Apache Giraph 和 Spark GraphX的比较</h1>
Srini Penchikala
[http://www.infoq.com/cn/news/2016/12/graph-processing-facebook?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2016/12/graph-processing-facebook?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>大规模图处理是Facebook数据基础设施的重要组成部分，针对于图数据分析会涉及到Apache Giraph 和 Spark GraphX。这个团队比较了这两个框架针对大规模图处理的性能。</p> <i>By Srini Penchikala</i> <i> Translated by 冬雨</i>
---------------
<h1 id="#title_21" >22、InfoQ采访HTTP/2的早期采用者Lawyer.com</h1>
Michael Redlich
[http://www.infoq.com/cn/news/2016/12/lawyer-com-adopts-http-2?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2016/12/lawyer-com-adopts-http-2?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Lawyer.com，一个为客户和律师提供匹配服务的网站，最近宣布他们已开始采用HTTP/2协议。这一举措可以让Lawyer.com关注页面交付速度，并为客户提供最佳匹配。根据数据分析网站Alexa所提供的数据，Lawyer.com被评为页面交付最快的律师网站。Lawyer.com还声称自己是第一个接受比特币支付的律师匹配网站。</p> <i>By Michael Redlich</i> <i> Translated by 孙镜涛</i>
---------------
<h1 id="#title_22" >23、微软宣布Cortana小娜对第三方开放</h1>
刘志勇
[http://www.infoq.com/cn/news/2016/12/Microsoft-Cortana-open?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2016/12/Microsoft-Cortana-open?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>在移动互联网和物联网时代，人工智能语音助手角逐的好戏在频频上演。语音助手对外开放，已经成为行业性趋势。</p> <i>By 刘志勇</i>
---------------
<h1 id="#title_23" >24、老牌巨头公司的持续创新，探寻网易杭研的三重职能</h1>
木环
[http://www.infoq.com/cn/news/2016/12/netease-research-academy-for19ye?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2016/12/netease-research-academy-for19ye?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>自997年成立以来，网易的产品线一直不断地发展。在网易人的“稳健务实，厚积薄发”理念之外，究竟是什么使得网易不断保持着创新力？作为一个巨头公司，它怎样进行产品布局和技术研发？网易背后的杭州研究院扮演着怎样的角色？带着这些问题，InfoQ对网易杭州研究院执行院长汪源进行了采访，本文是对采访内容的整理。</p> <i>By 木环</i>
---------------
<h1 id="#title_24" >25、The (Not So) Secret Powers Of The Mobile Browser</h1>
Stéphanie Walter
[https://www.smashingmagazine.com/2016/12/the-not-so-secret-powers-of-the-mobile-browser/](https://www.smashingmagazine.com/2016/12/the-not-so-secret-powers-of-the-mobile-browser/)
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
</table><p>Apple taught us, "There's an app for that." And we believed it. Why wouldn't we? But time has passed since 2009. Our mobile users have gotten more mature and are starting to weigh having space for new photos against installing your big fat e-commerce app. Meanwhile, mobile browsers have also improved. <strong>New APIs are being supported</strong>, and they will bring native app-like functionality to the mobile browser.</p>

<figure></figure>

<p>We can now access video and audio and use WebRTC to build a live video-chat web apps directly in the browser, no native app or plugin required. We can build progressive web apps that bring users an almost native app experience, with a launch icon, notifications, offline support and more. Using geolocation, battery status, ambient light detection, Bluetooth and the physical web, we can even go beyond responsive web design and build websites that will automagically adapt to users' needs and context.</p><p>The post .</p>
---------------