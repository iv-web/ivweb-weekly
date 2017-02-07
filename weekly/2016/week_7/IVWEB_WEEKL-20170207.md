## 文章索引
1、 <a href="#1使用teal规范" >使用Teal规范</a><br/>
2、 <a href="#2fex-技术周刊---2017/02/06" >FEX 技术周刊 - 2017/02/06</a><br/>
3、 <a href="#3视频演讲-如何打造大规模互联网企业的监控告警平台以携程-hickwall-为例" >视频演讲： 如何打造大规模互联网企业的监控告警平台——以携程 hickwall 为例</a><br/>
4、 <a href="#4文章-左耳朵耗子我对gitlab误删除数据库事件的几点思考" >文章： 左耳朵耗子：我对GitLab误删除数据库事件的几点思考</a><br/>
5、 <a href="#5文章-反脆弱边缘反脆弱实践访谈" >文章： 《反脆弱边缘：反脆弱实践》访谈</a><br/>
6、 <a href="#6文章-虚拟研讨会net的未来在哪里" >文章： 虚拟研讨会：.NET的未来在哪里？</a><br/>
7、 <a href="#7视频访谈-郑泽宇从学生时代起接触机器学习人工智能尚待技术突破" >视频访谈： 郑泽宇：从学生时代起接触机器学习，人工智能尚待技术突破</a><br/>
8、 <a href="#8谈谈技术选型" >谈谈技术选型</a><br/>
9、 <a href="#9devops能力是落地微服务的前提" >DevOps能力是落地微服务的前提</a><br/>
10、 <a href="#10visual-studio-2017-rc3支持net-core延迟对python的支持" >Visual Studio 2017 RC3支持.NET Core，延迟对Python的支持</a><br/>
11、 <a href="#11java-9进入第一轮问题修复阶段" >Java 9进入第一轮问题修复阶段</a><br/>
12、 <a href="#12oracle收购apiary来加强其api集成云" >Oracle收购Apiary来加强其API集成云</a><br/>
13、 <a href="#13getting-started-with-vr-interface-design" >Getting Started With VR Interface Design</a><br/><h1 id="#title_0" >1、使用Teal规范</h1>
Ben Linders
[http://www.infoq.com/cn/news/2017/02/applying-teal-paradigm?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/02/applying-teal-paradigm?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/news/2017/02/applying-teal-paradigm/zh/headerimage/GettyImages-639263872.jpg"/><p>使用Teal规范可以增进团队成员的参与度，并帮助团队成长。使用Teal规范的组织就好像是“生命体”，他们以人为本，解放员工，发掘员工的智谋，而不是把员工当作劳动力资源。</p> <i>By Ben Linders</i> <i> Translated by 刘嘉洋</i>
---------------
<h1 id="#title_1" >2、FEX 技术周刊 - 2017/02/06</h1>

[http://fex.baidu.com/blog/2017/02/fex-weekly-06//](http://fex.baidu.com/blog/2017/02/fex-weekly-06//)
作者：zhangjunah <br> <p>微信搜索『FEX』关注我们的公众号，及时获得最新资讯。</p>

<h2 id="section">深阅读</h2>

<p><strong>Google Computer Science Education</strong><br />
https://www.google.com/edu/cs/index.html<br />
Computer science (CS) education is a pathway to innovation, to creativity and to exciting career opportunities. We believe that all students deserve these opportunities. That is why Google is committed to developing programs, resources, tools and community partnerships which make CS engaging and accessible for all students.</p>

<p><strong>[译]热闹驱动开发</strong><br />
http://mp.weixin.qq.com/s?__biz=MzA3MDMwOTcwMg==&amp;mid=2650004762&amp;idx=1&amp;sn=b977fae06fdf6f7a39909e956d07085a<br />
软件开发团队关于软件架构或技术栈的决策，很多并不是基于扎实的研究和对期望效果的认真思考，而是不准确的意见、社交媒体的信息，或者就些是“热门”玩意。这种做派的危害我见过不少，称它为“热闹驱动开发（Hype Driven Development，HDD）”。我赞成的是更专业的做法，称之为“脚踏实地的软件工程”。下面一起看看HDD的来龙去脉，想想我们能怎么改进。另附：</p>

<p><strong>Front-End Developer Handbook 2017</strong><br />
https://frontendmasters.gitbooks.io/front-end-handbook-2017/content/<br />
The content of the handbook favors web technologies (HTML, CSS, DOM, and JavaScript) and those solutions that are directly built on top of these open technologies. The materials referenced and discussed in the book are either best in class or the current offering to a problem. The book should not be considered a comprehensive outline of all resources available to a front-end developer. The value of the book is tied up in a terse, focused, and timely curation of just enough categorical information so as not to overwhelm anyone on any one particular subject matter.</p>

<p><strong>Announcing GVFS (Git Virtual File System)</strong><br />
https://blogs.msdn.microsoft.com/visualstudioalm/2017/02/03/announcing-gvfs-git-virtual-file-system/<br />
Today, we’re introducing GVFS (Git Virtual File System), which virtualizes the file system beneath your repo and makes it appear as though all the files in your repo are present, but in reality only downloads a file the first time it is opened. GVFS also actively manages how much of the repo Git has to consider in operations like checkout and status, since any file that has not been hydrated can be safely ignored. And because we do this all at the file system level, your IDEs and build tools don’t need to change at all!</p>

<p><strong>Building Zero protocol for fast, secure mobile connections</strong><br />
https://code.facebook.com/posts/608854979307125/building-zero-protocol-for-fast-secure-mobile-connections/<br />
Over the past year, we’ve built and deployed Zero protocol to our mobile apps and load balancers. We’ve seen performance improvements that include a 41 percent reduction in connection latency and 2 percent reduction in total request time. We’ve learned several practical engineering lessons about the trade-offs associated with 0-RTT protocols, such as API design, security properties, and deployment, and have contributed some of our findings to TLS 1.3, which is now near maturity. We hope the lessons we share here are applicable to apps that will deploy TLS 1.3 in the future.</p>

<p><strong>Why 2016 Was the Best Year Ever for Node.js</strong><br />
https://nodesource.com/blog/why-2016-was-the-best-year-ever-for-node-js-node-by-numbers-2016<br />
Yes, that’s right, I’m going to argue that 2016 was our best year ever, and may go down as the most important period in the history of Node.js, backed by some hard numbers from this year’s </p>

<p><strong>JavaScript Will Finally Get Proper Asynchronous Programming</strong><br />
http://thenewstack.io/async-officially-coming-javascript-year/<br />
The proposal to include async function in ECMAScript has reached stage four; that means it’s on track to be in the 2017 release of the standard. But what does that mean for JavaScript developers?</p>

<p><strong>CQRS Explained - Node.js at Scale</strong><br />
https://blog.risingstack.com/cqrs-explained-node-js-at-scale/<br />
CQRS is an architectural pattern, where the acronym stands for Command Query Responsibility Segregation. We can talk about CQRS when the data read operations are separated from the data write operations, and they happen on a different interface. In most of the CQRS systems, read and write operations use different data models, sometimes even different data stores. This kind of segregation makes it easier to scale, read and write operations and to control security - but adds extra complexity to your system.</p>

<p><strong>Introducing Lottie</strong><br />
https://medium.com/airbnb-engineering/introducing-lottie-4ff4a0afac0e#.n5pgc22dj<br />
 is an iOS, Android, and React Native library that renders After Effects animations in real time, and allows native apps to use animations as easily as they use static assets.</p>

<p><strong>Everything you need to know about HTTP security headers</strong><br />
https://blog.appcanary.com/2017/http-security-headers.html<br />
This article explains what secure headers are and how to implement these headers in Rails, Django, Express.js, Go, Nginx, and Apache.</p>

<p><strong>下一代 Web 应用模型 —— Progressive Web App</strong><br />
http://geek.csdn.net/news/detail/135595<br />
2016年，Google提出了PWA，志在增强Web体验。可显著提高加载速度、可离线工作、可被添加至主屏、全屏执行、推送通知消息……等等这些特性可使Web应用渐进式地变成App，甚至与APP相匹敌。这一系列特性背后有哪些核心关键技术支撑，本文将为您一一分析，解开它的神秘面纱。</p>

<p><strong>(More than) one million requests per second in Node.js</strong><br />
https://github.com/uWebSockets/uWebSockets/wiki/(More-than)-one-million-requests-per-second-in-Node.js<br />
介绍用 uws 实现高性能的 http 服务。另附：</p>

<p><strong>CSS Grid – Table layout is back. Be there and be square</strong><br />
https://developers.google.com/web/updates/2017/01/css-grid<br />
If you are familiar with Flexbox, Grid should feel familiar. Rachel Andrew maintains a great website dedicated to CSS Grid to help you get started. Grid is now available in Google Chrome.  另附：</p>

<p><strong>Why I created junctions.js</strong><br />
http://jamesknelson.com/created-junctions-js/<br />
Junctions is a new, composable alternative to react-router.</p>

<p><strong>What happens when you use RxJS in React?</strong><br />
https://hackernoon.com/what-happens-when-you-use-rxjs-in-react-11ae5163fc0a#.jlru5uko6<br />
The ReactiveX Observable model allows you to treat streams of asynchronous events with the same sort of simple, composable operations that you use for collections of data items like arrays. It frees you from tangled webs of callbacks, and thereby makes your code more readable and less prone to bugs.</p>

<p><strong>Crash Course: UI Design</strong><br />
https://medium.com/hh-design/crash-course-ui-design-25d13ff60962#.75ndc967f<br />
At their most simple forms, UX design is what makes an interface useful, and UI design is what makes an interface beautiful. For UI, this includes a blend of visual hierarchy and interface elements. To understand what separates a great interface from a good interface, one must understand the UI design is merely just one layer of the entire design process. Perhaps this is why people often confuse UX and UI. In the following few paragraphs, however, I hope to help you as the audience or reader understand where the differences lie in the context of the design process.</p>

<p><strong>iOS即时通讯，从入门到“放弃”？</strong><br />
http://www.jianshu.com/p/2dbb360886a8<br />
本文会用实例的方式，将iOS各种IM的方案都简单的实现一遍。并且提供一些选型、实现细节以及优化的建议。这位作者写了一系列即时通讯音视频开发相关的文章，对这个领域有兴趣的同学可以参考。</p>

<p><strong>The most popular Front-End links of 2016</strong><br />
https://medium.com/statuscode/the-most-popular-front-end-links-of-2016-35d3142ac398#.y1pjcaqm5<br />
热门文章精选</p>

<h2 id="section-1">新鲜货</h2>

<p><strong>Open-sourcing Chrome on iOS!</strong><br />
https://blog.chromium.org/2017/01/open-sourcing-chrome-on-ios.html<br />
Historically, the code for Chrome for iOS was kept separate from the rest of the Chromium project due to the additional complexity required for the platform. After years of careful refactoring, all of this code is rejoining Chromium and being moved into the .<br />
Chrome 近期会推出这个功能：</p>

<p><strong>Open-Sourcing Google Earth Enterprise</strong><br />
https://maps-apis.googleblog.com/2017/01/open-sourcing-google-earth-enterprise.html<br />
We are excited to announce that we are open-sourcing Google Earth Enterprise (GEE), the enterprise product that allows developers to build and host their own private maps and 3D globes. With this release, GEE Fusion, GEE Server, and GEE Portable Server source code (all 470,000+ lines!) will be published on GitHub under the Apache2 license in March.</p>

<p><strong>GitLab.com Database Incident</strong><br />
https://about.gitlab.com/2017/02/01/gitlab-dot-com-database-incident/<br />
We had a serious incident with one of our databases. We lost six hours of database data (issues, merge requests, users, comments, snippets, etc.) for GitLab.com. Git/wiki repositories and self-hosted installations were not affected. Losing production data is unacceptable and in a few days we’ll publish a post on why this happened and a list of measures we will implement to prevent it happening again. <br />
另附：</p>

<p><strong>JS1k 2017</strong><br />
http://js1k.com/2017-magic/<br />
Create some JavaScript program with a max size of 1k and make it do something cool. Submit it before March 2017 for fame and a chance of a prize!</p>

<p><strong>Mithril 1.0 Released</strong><br />
http://mithril.js.org/<br />
At 3 years old,  has reached its 1.0 milestone. Mithril is a modern client-side Javascript framework for building Single Page Applications.<br />
It’s small (&lt; 8kb gzip), fast and provides routing and XHR utilities out of the box. Mithril is used by companies like Vimeo and Nike, and open source platforms like Lichess.</p>

<p><strong>hyperapp</strong><br />
https://github.com/hyperapp/hyperapp<br />
HyperApp is a 1kb functional JavaScript library for building modern UI applications.</p>

<p><strong>NativeScript 2.5 is Now Available</strong><br />
https://www.nativescript.org/blog/nativescript-25-is-now-available</p>

<p><strong>Service Mocker - Next generation frontend API mocking framework</strong><br />
https://github.com/service-mocker/service-mocker<br />
Service Mocker is an API mocking framework for frontend developers. With the power of service workers, we can easily set up mocking services without any real servers. It sets developers free from intricate workflows, complex documentations and endless proxies from server to server.</p>

<p><strong>spectacle</strong><br />
https://github.com/FormidableLabs/spectacle<br />
ReactJS based Presentation Library</p>

<p><strong>tectonic - A declerative REST data loader for react + redux</strong><br />
https://github.com/tonyhb/tectonic<br />
Tectonic is a small library that makes loading REST API data a one-liner within your redux apps. You’ll write 80% less data loading code: no more action, reducer, normalizr, reselect boilerplate. Tectonic handles all actions, reducer data management, and prop injection for you &amp;emdash; with one line. Plus you can swap out real data for fake data using a mock driver with one line. Overall, it’s fast to write and maintain, plus it’ll save your sanity.</p>

<p><strong>Nachos UI Kit for React Native</strong><br />
https://avocode.com/nachos-ui/<br />
Nachos UI is a React Native component library.</p>

<p><strong>Jimp - The JavaScript Image Manipulation Program</strong><br />
https://github.com/oliver-moran/jimp<br />
An image processing library written entirely in JavaScript for Node, with zero external or native dependencies.</p>

<p><strong>jsmpeg</strong><br />
http://jsmpeg.com/<br />
用纯 JS 实现的 mpeg 解码</p>

<p><strong>injection-js</strong><br />
https://github.com/mgechev/injection-js<br />
Dependency injection library for JavaScript and TypeScript in 6.6K. It is an extraction of the Angular’s dependency injection which means that it’s feature complete, fast, reliable and well tested.</p>

<p><strong>Breakdance -  a node.js library for converting HTML to markdown</strong><br />
http://breakdance.io/<br />
Breakdance uses cheerio to parse HTML, and snapdragon for rendering, which provides comprehensive coverage of HTML 4 and 5 elements, and granular control over the entire conversion process in a way that is easy to understand, reason about, and customize.</p>

<p><strong>Exploring ES2016 and ES2017</strong><br />
http://exploringjs.com/es2016-es2017/index.html<br />
This book is about ECMAScript 2016 and ECMAScript 2017, new versions of JavaScript. It only covers what’s new in those versions.</p>

<p><strong>Visual Studio Code 1.9</strong><br />
https://code.visualstudio.com/updates/v1_9<br />
依旧是大量看起来很有用的更新</p>

<p><strong>Element</strong><br />
http://element.eleme.io/#/zh-CN<br />
VUE 的 UI 库</p>

<p><strong>mJS: Restricted JavaScript engine</strong><br />
https://github.com/cesanta/mjs<br />
mJS is designed for microcontrollers with limited resources.</p>

<p><strong>vstest</strong><br />
https://github.com/Microsoft/vstest<br />
Visual Studio Test Platform is the runner and engine that powers test explorer and vstest.console.</p>

<h2 id="section-2">产品及其它</h2>

<p><strong>企鹅智库 - 2017必读报告：中国互联网未来5年趋势白皮书</strong><br />
http://tech.qq.com/a/20170111/002574.htm#p=1<br />
了解下行业趋势，好帮助我们去储备面向未来的技术。</p>

<p><strong>新时代的知识演绎者们</strong><br />
https://www.huxiu.com/article/179893.html<br />
并非是不存在能够解决问题的知识，而是这些知识没有被很好的组织起来，形成更加实用、易于理解的形式。如果有一个专业的团队，帮助用户从各种资料中，找到答案，并加工成更易理解和使用的形式呢？可能每个人只需要花费20分钟以内的时间就可以解决自己的问题。所以关于知识类产品的一个机会是，在现在的时代背景下我们似乎缺少知识的“演绎者”。</p>

<p><strong>开源如何影响程序员</strong><br />
http://mp.weixin.qq.com/s?__biz=MjM5MDE0Mjc4MA==&amp;mid=2650995350&amp;idx=1&amp;sn=466a315fd3c87763eb6076845733c1c3<br />
Apple 核心系统高级工程师 Asta 谢（谢孟军）就《开源如何影响程序员》这一主题，结合自身经历、从开源中得到的自我提升，详细阐述了自己对开源的理解，如何在国内做开源，并成为 github 上 Go 语言领域中国排名第一，以及如何同国内外开源者一起参与开源的过程。</p>

<p><strong>职场中脱颖而出的成长秘诀</strong><br />
https://mp.weixin.qq.com/s?__biz=MzA3NTYzODYzMg==&amp;mid=2653578530&amp;idx=1&amp;sn=299b065ccc211d12f0f034744d1037f5<br />
挺实在的经验：自我管理、培养自驱力、建立自己的不可替代性、好善乐施 &amp; 知恩图报。</p>

<p><strong>[译]Uncle Bob：如何成为一名优秀的软件架构师？</strong><br />
http://mp.weixin.qq.com/s?__biz=MzA5Nzc4OTA1Mw==&amp;mid=2659598924&amp;idx=1&amp;sn=5e08adfa73d03b17d3d8e16d790a35ef<br />
关于架构非常生动形象的一篇文章。一名软件架构师真正要做的重要决定都在数据库、Web服务器和框架之外。</p>

<p><strong>年终总结 - 码农篇</strong><br />
http://mp.weixin.qq.com/s?__biz=MzA3MDA2MjE2OQ==&amp;mid=2650096758&amp;idx=1&amp;sn=528fc29907c87f0b01b62b74bd3f433c<br />
这是来自黑夜路人技术微信群里的年终总结，一起体味下码农的冷暖人生。</p>
---------------
<h1 id="#title_2" >3、视频演讲： 如何打造大规模互联网企业的监控告警平台——以携程 hickwall 为例</h1>
唐锐华
[http://www.infoq.com/cn/presentations/how-to-build-a-large-scale-internet-enterprise-monitoring-alarm-platform?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/how-to-build-a-large-scale-internet-enterprise-monitoring-alarm-platform?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/how-to-build-a-large-scale-internet-enterprise-monitoring-alarm-platform/zh/mediumimage/tangruihua270.jpg"/><p>随着公司业务的扩展，新应用不断涌现，基础监控和应用监控的需求迅猛增长，传统的监控告警平台已经不堪重负。在调研了很多开源方案之后发觉或多或少都存在不太满意的地方，所以在借鉴多种方案的基础上，带着对前辈系统的崇敬，以自服务为最终目标，我们重新设计开发了一套监控告警系统(hickwall)，这次演讲主要针对这套系统的各个功能特色进行深入浅出的介绍。</p> <i>By 唐锐华</i>
---------------
<h1 id="#title_3" >4、文章： 左耳朵耗子：我对GitLab误删除数据库事件的几点思考</h1>
陈皓
[http://www.infoq.com/cn/articles/some-thoughts-on-gitlab-accidentally-deleting-database?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/some-thoughts-on-gitlab-accidentally-deleting-database?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/some-thoughts-on-gitlab-accidentally-deleting-database/zh/smallimage/dbushu_logo.jpg"/><p>
太平洋时间2017年1月31日晚上，GitLab通过推特发文承认300GB生产环境数据因为UNIX SA的误操作，已经被彻底删除（后发文补充说明已经挽回部分数据），引起业界一片哗然。知名博主陈皓在其博客中详细回顾了此次事件，并做了思考和总结，InfoQ经原作者授权发布此文。</p> <i>By 陈皓</i>
---------------
<h1 id="#title_4" >5、文章： 《反脆弱边缘：反脆弱实践》访谈</h1>
Ben Linders
[http://www.infoq.com/cn/articles/book-review-antifragility-edge?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/book-review-antifragility-edge?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/book-review-antifragility-edge/zh/smallimage/TAE-AiP-JEG.jpg"/><p>在《反脆弱边缘》一书中，Sinan Si Alhir 介绍了反脆弱已被用来如何帮助组织发展壮大。他举例说明了反脆弱是如何使用在个人、集体（团队和社区）和企业层的敏捷之上的，并探索了企业达成反脆弱的路线图。</p> <i>By Ben Linders</i> <i> Translated by 冬雨</i>
---------------
<h1 id="#title_5" >6、文章： 虚拟研讨会：.NET的未来在哪里？</h1>
Pierre-Luc Maheu
[http://www.infoq.com/cn/articles/virtual-panel-dotnet-future?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/virtual-panel-dotnet-future?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/virtual-panel-dotnet-future/zh/headerimage/GettyImages-523398836.jpg"/><p>.NET生态系统在过去的一年中发生了很多事情。如果要关注细节，那大的景象难以描绘。在每个方面都有新的动作：跨平台、云、移动、Web应用和通用应用。开发人员都想知道这一切会造成什么改变，要实现改变必须要做些什么。</p> <i>By Pierre-Luc Maheu</i> <i> Translated by 刘嘉洋</i>
---------------
<h1 id="#title_6" >7、视频访谈： 郑泽宇：从学生时代起接触机器学习，人工智能尚待技术突破</h1>
郑泽宇
[http://www.infoq.com/cn/interviews/interview-with-zhengzeyu-talk-artificial-intelligence?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/interviews/interview-with-zhengzeyu-talk-artificial-intelligence?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/interviews/interview-with-zhengzeyu-talk-artificial-intelligence/zh/mediumimage/zhengzeyu270.jpg"/><p>来自才云的郑泽宇分享了才云的云平台运维管理系统和大数据的结合点与应用，介绍了他们深度学习模型的选型考量，训练数据的来源和数据清洗相关的经验，分享了他对AI发展，还有对计算机AI与人类智慧博弈的看法，最后谈到了阿里云和Docker官方合作的对才云的影响。
</p> <i>By 郑泽宇</i>
---------------
<h1 id="#title_7" >8、谈谈技术选型</h1>
Marek Kirejczyk
[http://www.infoq.com/cn/news/2017/02/Technology-selection?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/02/Technology-selection?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>本文的主题是技术选型，作者总结了他见过的各种不靠谱的技术选型方式，比如有的团队会根据社交媒体上的讨论来决定选择哪种架构，也有的团队会跟风走，哪个热门就选哪个。但总体来看，这样简单粗暴的方式一定会为未来埋下隐患。那为什么这样说？我们应该如何做正确的选择？且听作者细细道来。</p> <i>By Marek Kirejczyk</i>
---------------
<h1 id="#title_8" >9、DevOps能力是落地微服务的前提</h1>
薛命灯
[http://www.infoq.com/cn/news/2017/02/DevOps-serve-first?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/02/DevOps-serve-first?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>微服务系统比我们想象的要复杂得多。微服务给我们带来了诸多好处，同时也对我们提出了更高的要求。Martin Fowler为我们提出了三点建议，帮助我们分析微服务是否适合我们。</p> <i>By 薛命灯</i>
---------------
<h1 id="#title_9" >10、Visual Studio 2017 RC3支持.NET Core，延迟对Python的支持</h1>
Jeff Martin
[http://www.infoq.com/cn/news/2017/02/VS2017RC3?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/02/VS2017RC3?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Microsoft发布了Visual Studio 2017第三个候选版本。在该版本中值得注意的是对.NET Core和ASP.NET Core的完全支持，但对Python的支持延迟了。由于进行了一些错误修复，预测VS2017将在不久之后发布正式版本。</p> <i>By Jeff Martin</i> <i> Translated by 刘嘉洋</i>
---------------
<h1 id="#title_10" >11、Java 9进入第一轮问题修复阶段</h1>
Abraham Marín Pérez
[http://www.infoq.com/cn/news/2017/02/java9-rampdown-phase-start?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/02/java9-rampdown-phase-start?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Java 9正式完成功能，这意味着第一个问题修复阶段已经开始。HTTP/2客户端没有在截止日期前完成，现已降级为孵化器功能。由于现在的目标是在7月准备好可发布的Java 9，所以目前不太可能添加任何新的JEP。</p> <i>By Abraham Marín Pérez</i> <i> Translated by 尚剑</i>
---------------
<h1 id="#title_11" >12、Oracle收购Apiary来加强其API集成云</h1>
Karthick Viswanathan
[http://www.infoq.com/cn/news/2017/02/oracle-acquires-apiary?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/02/oracle-acquires-apiary?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Oracle宣布计划于1月19日收购Apiary，一家专注于API设计和协作的API管理公司。Apiary最为人所知的是API flow，其API管理平台。</p> <i>By Karthick Viswanathan</i> <i> Translated by 刘嘉洋</i>
---------------
<h1 id="#title_12" >13、Getting Started With VR Interface Design</h1>
Sam Applebee &#38; Alex Deruette
[https://www.smashingmagazine.com/2017/02/getting-started-with-vr-interface-design/](https://www.smashingmagazine.com/2017/02/getting-started-with-vr-interface-design/)
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
</table><p>The virtual realm is uncharted territory for many designers. In the last few years, we've witnessed <strong>an explosion in virtual reality</strong> (VR) hardware and applications. VR experiences range from the mundane to the wondrous, their complexity and utility varying greatly.</p>

<figure></figure>

<p>Taking your first steps into VR as a UX or UI designer can be daunting. We know because we've been there. But fear not! In this article, we'll share a process for designing VR apps that we hope you'll use to start designing for VR yourself. You don't need to be an expert in VR; you just need to be willing to apply your skills to a new domain. Ultimately, as a community working together, we can accelerate VR to reach its full potential faster.</p><p>The post .</p>
---------------