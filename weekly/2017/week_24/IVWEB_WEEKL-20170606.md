## 文章索引
1、 <a href="#1从责任界定和问题预警角度-解读全栈溯源对devops的价值" >从责任界定和问题预警角度 解读全栈溯源对DevOps的价值</a><br/>
2、 <a href="#2fex-技术周刊---2017/06/05" >FEX 技术周刊 - 2017/06/05</a><br/>
3、 <a href="#3文章-nginscript系列通过tcp负载均衡和galera集群来扩展mysql" >文章： nginScript系列：通过TCP负载均衡和Galera集群来扩展MySQL</a><br/>
4、 <a href="#4视频演讲-aws-数据中心与-vpc-揭秘" >视频演讲： AWS 数据中心与 VPC 揭秘</a><br/>
5、 <a href="#5文章-共享行业的分布式mqtt设计" >文章： 共享行业的分布式MQTT设计</a><br/>
6、 <a href="#6文章-可编程世界的发展之路" >文章： 可编程世界的发展之路</a><br/>
7、 <a href="#7java-9正式版有可能被推迟到9月21号发布" >Java 9正式版有可能被推迟到9月21号发布</a><br/>
8、 <a href="#8damon-edwards访谈自助运维是否意味着更好更快更省钱" >Damon Edwards访谈：自助运维是否意味着更好、更快、更省钱？</a><br/>
9、 <a href="#9nicole-forsgren访谈devops和提升绩效的关键因素" >Nicole Forsgren访谈：DevOps和提升绩效的关键因素</a><br/>
10、 <a href="#10在twitter信息流中大规模应用深度学习" >在Twitter信息流中大规模应用深度学习</a><br/>
11、 <a href="#11the-state-of-advanced-website-builders" >The State Of Advanced Website Builders</a><br/><h1 id="#title_0" >1、从责任界定和问题预警角度 解读全栈溯源对DevOps的价值</h1>
江柳
[http://www.infoq.com/cn/news/2017/06/APM-tingyun-DevOps?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/06/APM-tingyun-DevOps?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>在2000年及更早的时候，应用大都是简单的3层架构，即界面层、业务逻辑层和数据访问层。而随着云技术和移动互联网的发展，时代对IT技术提出了更高的要求，它需要适应更迅捷的变化。同时，产品的迭代速度和效率变得更快，应用的复杂性也发生了爆炸式的增长，新时代的应用也变得更加难于管理。</p> <i>By 江柳</i>
---------------
<h1 id="#title_1" >2、FEX 技术周刊 - 2017/06/05</h1>

[http://fex.baidu.com/blog/2017/06/fex-weekly-05//](http://fex.baidu.com/blog/2017/06/fex-weekly-05//)
作者：2betop <br> <p>微信搜索『FEX』关注我们的公众号，及时获得最新资讯。</p>

<h2 id="section">深阅读</h2>

<p><strong>Node v8.0.0</strong><br />
https://nodejs.org/en/blog/release/v8.0.0/<br />
.</p>

<p><strong>WebAssembly: Mozilla Won</strong><br />
http://robert.ocallahan.org/2017/06/webassembly-mozilla-won.html<br />
Mozilla staff are being very diplomatic and restrained by allowing WebAssembly to be portrayed as a compromise between the approaches of asm.js and PNaCl. They have good reasons for being so, but I can be a bit less restrained. asm.js and PNaCl represented quite different visions for how C/C++ code should be supported on the Web, and I think WebAssembly is a big victory for asm.js and Mozilla’s vision. 另附：</p>

<p><strong>Yarn determinism</strong><br />
https://yarnpkg.com/blog/2017/05/31/determinism/<br />
One of the claims that Yarn makes is that it makes your package management “deterministic”. But what exactly does this mean? This blog post highlights how both Yarn and npm 5 are deterministic, but differ in the exact guarantees they provide and the tradeoffs they have chosen. Determinism in the context of JavaScript package management is defined as always getting the exact same node_modules folder given a package.json and companion lock file.</p>

<p><strong>Key Abstractions for IoT-Oriented Software Engineering</strong><br />
https://www.infoq.com/articles/iot-key-abstractions<br />
The current design of IoT systems sports a number of common features such as the “things” they want to connect, the software infrastructure that connects them, and the services and applications that allow to regulate and configure the system.The first abstraction that is useful in the defintion of an IoT system is that of system stakeholders, including local and global managers, and users.</p>

<p><strong>Into the Great Unknown — Migrating from Mocha to Jest</strong><br />
https://ebaytech.berlin/into-the-great-unknown-migrating-from-mocha-to-jest-3baced083c7e<br />
How to migrate an existing code base to Jest? Let’s put on our sun helmets, zip up our sturdy boots and prepare to venture into the great unknown!</p>

<p><strong>[译]HTTP/2推送技术之难，真的远超我们想象</strong><br />
https://mp.weixin.qq.com/s?__biz=MzA5Nzc4OTA1Mw==&amp;mid=2659599304&amp;idx=1&amp;sn=12d2da3dc46c50e829f6f959237c41ff<br />
HTTP/2 推送远比我最初想象中更复杂，也更底层，但最让我措手不及的地方在于，这种技术在不同浏览器上的表现竟然有这么大的差别，本来我还觉得这技术已经足够成熟，可以在生产环境中使用了。本文并不是那种认为“HTTP/2 推送一无是处”的吐槽文。我觉得 HTTP/2 推送真的很强大，以后还会更加完善，但并不算能解决所有问题的万灵药。</p>

<p><strong>回顾我的600篇技术笔记</strong><br />
https://mp.weixin.qq.com/s?__biz=MzU5OTAxOTE4MA==&amp;mid=2247483673&amp;idx=1&amp;sn=2668eee091d3ebe040f199d417c08a30<br />
一位码农的心得体会，挺实在的，赞：“节制无穷尽的求知欲，从实践出发求知；不要闭门造车，好东西要分享”。</p>

<p><strong>我对知乎前端相关问题的十问十答</strong><br />
http://www.zhangxinxu.com/wordpress/2017/06/ten-question-about-frontend-zhihu/<br />
CSS 专家张鑫旭对前端的理解。</p>

<p><strong>Instagram 在 PyCon 2017 的演讲摘要</strong><br />
http://www.zlovezl.cn/articles/instagram-pycon-2017/<br />
Instagram 的总注册用户达到 30 亿，月活用户超过 7 亿。而令人吃惊的是，这么高的访问量背后，竟完全是由以速度慢著称的 Python + Django 支撑。在  上，Instagram 的工程师们带来了一个有关 Python 在 Instagram 的主题演讲，同时还分享了 Instagram 如何将整个项目运行环境升级到 Python 3 的故事。</p>

<p><strong>DNS Infrastructure at GitHub</strong><br />
https://githubengineering.com/dns-infrastructure-at-github/<br />
At GitHub we recently revamped how we do DNS from the ground up. This included both how we interact with external DNS providers and how we serve records internally to our hosts. To do this, we had to design and build a new DNS infrastructure that could scale with GitHub’s growth and across many data centers.</p>

<p><strong>Flannel: An Application-Level Edge Cache to Make Slack Scale</strong><br />
https://slack.engineering/flannel-an-application-level-edge-cache-to-make-slack-scale-b8a6400e2f6b<br />
Slack was architected around the goal of keeping teams of hundreds of people connected, and as teams have gotten larger, our initial techniques for loading and maintaining data have not scaled. To address that, we created a system that lazily loads data on demand and answers queries as you go.</p>

<p><strong>Animating Single Div Art</strong><br />
https://css-tricks.com/animating-single-div-art/<br />
When you dig deep with your tools, it is amazing what you can create out of the most basic of HTML. I have been constantly impressed with “Single Div Art” by Lynn Fisher and others where you take a single generic <code class="highlighter-rouge">&lt;div&gt;</code> to create a beautiful cactus, Alamo, or panda.</p>

<p><strong>11 things I learned reading the flexbox spec</strong><br />
https://hackernoon.com/11-things-i-learned-reading-the-flexbox-spec-5f0c799c776b<br />
A run through some of the ‘good bits’ of the CSS Flexible Box Layout specification.</p>

<p><strong>A Love Letter to CSS</strong><br />
http://developer.telerik.com/topics/web-development/love-letter-css/<br />
Today I’m going to try to convince you that not only is CSS one of the best technologies you use on a day-to-day basis, not only is CSS incredibly well designed, but that you should be thankful—thankful!—each and every time you open a .css file. My argument is relatively simple: creating a comprehensive styling mechanism for building complex user interfaces is startlingly hard, and every alternative to CSS is much worse. Like, it’s not even close.</p>

<h2 id="section-1">新鲜货</h2>

<p><strong>Announcing an open data set on the open source community</strong><br />
https://github.com/blog/2372-announcing-an-open-data-set-on-the-open-source-community<br />
We just released  for the open source community, researchers, and curious data wonks to study. The data includes responses from 5,500 open source participants randomly sampled from over 3,800 projects on GitHub.com and over 500 sourced from communities that work on other platforms. Altogether, the data represents some of the most comprehensive and high-quality data on the open source community to date.</p>

<p><strong>Best JavaScript Frameworks, Libraries and Tools to use in 2017</strong><br />
https://www.sitepoint.com/top-javascript-frameworks-libraries-tools-use/<br />
This article endeavors to explain the basics and rudimentary differences between the most popular client-side JavaScript frameworks, libraries, and tools. Whether they are “best” for you is another question. Choose something and stick with it for a while. Just be aware your favorite option will be superseded by something “better” no matter what you select!</p>

<p><strong>npm Pride 2017 Shirts</strong><br />
http://blog.npmjs.org/post/161303607370/npm-pride-2017<br />
不知国内能不能买。</p>

<p><strong>2017互联网女皇报告中文完整版</strong><br />
http://tech.qq.com/a/20170601/009038.htm#p=1<br />
有“互联网女皇”之称的玛丽·米克尔在美国Code大会上发布了2017年的互联网趋势报告，可关注下行业发展趋势。</p>

<p><strong>TypeScript support in Electron</strong><br />
https://electron.atom.io/blog/2017/06/01/typescript<br />
The electron npm package now includes a TypeScript definition file that provides detailed annotations of the entire Electron API. These annotation can improve your Electron development experience even if you’re writing vanilla JavaScript. Just npm install electron to get up-to-date Electron typings in your project.</p>

<p><strong>Visualize data instantly with machine learning in Google Sheets</strong><br />
https://www.blog.google/products/g-suite/visualize-data-instantly-machine-learning-google-sheets/<br />
Explore in Sheets, powered by machine learning, helps teams gain insights from data, instantly. Simply ask questions—in words, not formulas—to quickly analyze your data.</p>

<p><strong>What’s New In DevTools (Chrome 60)</strong><br />
https://developers.google.com/web/updates/2017/05/devtools-release-notes<br />
Here’s what’s new in DevTools in Chrome 60. You can check what version of Chrome you’re running at chrome://version.</p>

<p><strong>vis.js</strong><br />
http://visjs.org/<br />
A dynamic, browser based visualization library. The library is designed to be easy to use, to handle large amounts of dynamic data, and to enable manipulation of and interaction with the data. The library consists of the components DataSet, Timeline, Network, Graph2d and Graph3d.</p>

<p><strong>Storybook 3.0</strong><br />
https://medium.com/storybookjs/announcing-storybook-3-0-329748b8f4cd<br />
 is a development environment for UI components. It allows you to browse a component library, view the different states of each component, and interactively develop and test components. 3.0 brings long-anticipated webpack2 support, create-react-native-app support, flexible snapshot testing, and a host of bugfixes and enhancements.</p>

<p><strong>Meteor 1.5</strong><br />
https://blog.meteor.com/announcing-meteor-1-5-b82be66571bb<br />
Dynamic import(…), exact code splitting, immutable module caching, and bundle analysis tools</p>

<p><strong>Muuri</strong><br />
https://haltu.github.io/muuri/<br />
Responsive, sortable, filterable and draggable grid layouts</p>

<p><strong>Awesome CSS in JS</strong><br />
https://github.com/tuchk4/awesome-css-in-js<br />
A collection of awesome things regarding to CSS in JS approach</p>

<p><strong>Popper.js</strong><br />
https://popper.js.org/<br />
A kickass library to manage your poppers. A popper is an element on the screen which “pops out” from the natural flow of your application.</p>

<p><strong>Picodom</strong><br />
https://github.com/picodom/picodom<br />
Picodom is a 1kb Virtual DOM builder and patch algorithm.</p>

<p><strong>Browse faster and safer with Brave</strong><br />
https://brave.com/<br />
The new Brave browser automatically blocks ads and trackers, making it faster and safer than your current browser.</p>

<p><strong>W3C Performance Specifications</strong><br />
http://www.standardista.com/w3c-performance-specifications/<br />
Here are some of the W3C’s web performance specifications.</p>

<p><strong>Web Design Museum</strong><br />
https://www.webdesignmuseum.org/<br />
The museum exhibits over 800 carefully selected and sorted web sites that show web design trends between the years 1996 and 2005.</p>

<p><strong>Data GIF Maker - 一款数据 GIF 制作工具</strong><br />
http://www.geekpark.net/topics/219627<br />
News Lab 推出了一款数据 GIF 制作工具——Data GIF Maker。该工具可以使某些动态性的数据更加直观地进行对比，例如，你可以使用这款工具在不同的时间节点上，查看两支球队的夺冠支持率，但是它仅能用于两种不同主题对比的数据统计。</p>

<p><strong>Game Programming Patterns</strong><br />
http://gameprogrammingpatterns.com/<br />
I’m here to help! Game Programming Patterns is a collection of patterns I found in games that make code cleaner, easier to understand, and faster. This is the book I wish I had when I started making games, and now I want you to have it.</p>

<h2 id="section-2">产品及其它</h2>

<p><strong>腾讯社交办公产品 TIM</strong><br />
http://36kr.com/p/5078074.html<br />
TIM没有一般企业内部交流软件的标配——企业组织架构。它似乎只是在QQ的基础上，做了一些定制化的功能，并没有革命性的改变。这似乎是腾讯进军办公场景的一条尝试路径。另附：。</p>

<p><strong>傅盛创业方法论之CEO系列全集</strong><br />
https://mp.weixin.qq.com/s?__biz=MjM5NjgzMzkwMQ==&amp;mid=2653646337&amp;idx=1&amp;sn=548060db00705b85e236f18545d0ea8b<br />
创业要解决的，就是开放性的环境下，找到方向。CEO的核心是树立一个简单可行的目标，树立一个越简单越聚焦的目标越好。尽管这个目标，可能在过程中，不断变化。创业过程中，开放式变成封闭式问题的转换能力，是我们真正最需要的能力的核心。当目标足够简单，就会足够狭窄，足够狭窄会带来什么？就是你如此投入以后，别人没有机会赶超，因为已经没办法再超越了。管理的本质就是树立一个核心的业务，让这个业务带着所有的员工和组织构架往前走，而不是去构建一个四平八稳的组织，让所有的业务井井有条。</p>

<p><strong>从顺丰大战阿里，看巨头的“舒服恶”和“舒服死”</strong><br />
https://mp.weixin.qq.com/s?__biz=MjM5NzYxMzk4MQ==&amp;mid=2649331114&amp;idx=1&amp;sn=a07400fe7db5e2f396916e039b2d6428<br />
能力越大，责任越大，要求越高。曾经，腾讯在那个“艰难的决定”之后，痛改前非，拥抱开放，重建生态，获得了行业的尊重。阿里呢？</p>

<p><strong>技术人转型怎样转变思路与处事之道</strong><br />
https://mp.weixin.qq.com/s?__biz=MjM5MDE0Mjc4MA==&amp;mid=2650996346&amp;idx=1&amp;sn=e0998b024f852f966d3d59be7969f2dd<br />
本文作者将从自己的工作经历出发，从工程师择业的角度，与观众产生共鸣，从大公司到创业公司，需要转变的思路与做事情的方法，有原则性的东西，也有真实案例与身边的故事，还会穿插一些工程师的软技能。</p>

<p><strong>互联网世界的「阿甘正传」 - Meduim 创始人 Ev Williams</strong><br />
https://mp.weixin.qq.com/s/UMujS8y-d2MfwKH_ZB8jAw<br />
网络，是指页面由HTML或者CSS编写。而自由，是指所有人都可以访问，没有特权页面，没有付费要求，没有用户账号。最重要的是，这个开放网络是自由的——就像语言和意识一样自由。自由并不是一项权利，更像是一种技术上不可分割的事实。这种自由的终极意义：是创造一个最好、最酷的，以往媒体从来没能创造的，由全人类共同编写的图书所组成的图书馆。这个网络将包含着小说、报纸、科学期刊，和其它全部的东西。每个人都能为它写作，每个人都能来阅读它。它是待办事项清单、日记本、文学作品，也是力量强大到甚至能够阻止战争的沟通工具。</p>
---------------
<h1 id="#title_2" >3、文章： nginScript系列：通过TCP负载均衡和Galera集群来扩展MySQL</h1>
Nginx
[http://www.infoq.com/cn/articles/introduction-to-nginscript-part03?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/introduction-to-nginscript-part03?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/introduction-to-nginscript-part03/zh/smallimage/zhihui_logo.jpg"/><p>这是nginScript系列文章的第三篇，将介绍如何使用nginScript将客户端循序渐进地重定向到新的服务器。</p> <i>By Nginx</i> <i> Translated by 薛命灯</i>
---------------
<h1 id="#title_3" >4、视频演讲： AWS 数据中心与 VPC 揭秘</h1>
余骏
[http://www.infoq.com/cn/presentations/aws-data-center-and-vpc-secret?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/aws-data-center-and-vpc-secret?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/aws-data-center-and-vpc-secret/zh/mediumimage/yujun270.jpg"/><p>地球人都知道的 AWS 数据中心是如何建成的？AWS VPC 又是如何在 AWS 数据中心物理网络中实现逻辑隔离的虚拟网络？本次分享我们会深入剖析 AWS 数据中心和 VPC 背后的秘密，带你走进 AWS 全球 16 个地理区域、42个 可用区所组成的庞大数字帝国。</p> <i>By 余骏</i>
---------------
<h1 id="#title_4" >5、文章： 共享行业的分布式MQTT设计</h1>
百度云
[http://www.infoq.com/cn/articles/distributed-mqtt-design-for-shared-industries?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/distributed-mqtt-design-for-shared-industries?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/distributed-mqtt-design-for-shared-industries/zh/smallimage/xx_logo (3).jpg"/><p>随着移动互联网慢慢进入后半场，越来越多的公司将注意力转移到物联网，希望通过早期布局来起到占领这个行业的制高点，比如目前流行的摩拜单车，OFO 单车都是典型的物联网应用。物联网本身并不是什么新概念，随着大数据，AI 等技术的发展，大家意识到传统的物联网通过一定改造，借助大数据以及 AI 技术可以获得很多额外的价值。 这里主要介绍物联网的接入服务，物联网主流接入协议分为 MQTT，CoaP，Http，XMPP 等几种，本文主要是介绍 MQTT 协议的优缺点以及如何实现 MQTT 的分布式框架。</p> <i>By  百度云</i>
---------------
<h1 id="#title_5" >6、文章： 可编程世界的发展之路</h1>
Antero Taivalsaari, Tommi Mikkonen
[http://www.infoq.com/cn/articles/iot-programmable-world-roadmap?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/iot-programmable-world-roadmap?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/iot-programmable-world-roadmap/zh/headerimage/headerlogo_480.jpg"/><p>我们周围陆续涌现出数以百万计可远程操作、可编程的设备，这对软件开发者造成了巨大的挑战。本文为当今以云为中心，以数据为中心的物联网系统向着可编程世界的发展提出了一种路线图，并着重介绍了一些尚未引起足够重视的挑战。</p> <i>By Antero Taivalsaari</i> <i> Translated by 大愚若智</i>
---------------
<h1 id="#title_6" >7、Java 9正式版有可能被推迟到9月21号发布</h1>
薛命灯
[http://www.infoq.com/cn/news/2017/06/Java-9-delayed-September-21st?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/06/Java-9-delayed-September-21st?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Oracle Java Platform Group首席架构师Mark Reinhold在五月份的一系列专家组电话会议中建议将Java 9的正式发布日期向后延期8周，也就是在9月21号发布。</p> <i>By 薛命灯</i>
---------------
<h1 id="#title_7" >8、Damon Edwards访谈：自助运维是否意味着更好、更快、更省钱？</h1>
Daniel Bryant
[http://www.infoq.com/cn/news/2017/06/self-service-operations?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/06/self-service-operations?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>为迎接6月5日召开的伦敦DevOps企业峰会，InfoQ采访了Rundeck公司的联合创始人Damon Edwards，讨论了“自助运维（Self-Service Operations）”的优势与实现。</p> <i>By Daniel Bryant</i> <i> Translated by 王强</i>
---------------
<h1 id="#title_8" >9、Nicole Forsgren访谈：DevOps和提升绩效的关键因素</h1>
Daniel Bryant
[http://www.infoq.com/cn/news/2017/06/forsgren-devops-performance?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/06/forsgren-devops-performance?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>在为即将举行的伦敦DevOps企业峰会做准备工作的过程中，InfoQ采访了DORA的CEO兼首席科学家Nicole Forsgren博士，与他探讨了DevOps基础、在制定业务目标方面所面临的挑战，以及如何衡量企业的绩效等问题。</p> <i>By Daniel Bryant</i> <i> Translated by 薛命灯</i>
---------------
<h1 id="#title_9" >10、在Twitter信息流中大规模应用深度学习</h1>
Nicolas Koumchatzky 等
[http://www.infoq.com/cn/news/2017/06/Twitter-new-deep-study?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/06/Twitter-new-deep-study?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>来自Twitter的Nicolas Koumchatzky和Anton Andryeyev在这篇文章里介绍了Twitter基于深度神经网络的信息流排序算法，以及由Twitter内部AI团队Cortex构建的AI平台和它提供的建模功能。</p> <i>By Nicolas Koumchatzky 等</i> <i> Translated by 薛命灯</i>
---------------
<h1 id="#title_10" >11、The State Of Advanced Website Builders</h1>
Drew Thomas
[https://www.smashingmagazine.com/2017/06/advanced-website-builders/](https://www.smashingmagazine.com/2017/06/advanced-website-builders/)
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
</table><p>Advanced website builders — the tools provided by <em>Squarespace</em>, <em>Wix</em>, <em>Weebly</em>, <em>The Grid</em> and more — produce websites that look and feel like they were designed and coded by humans. They’re also software as a service, which is a different business model than traditional, custom-developed websites.</p>

<figure></figure>

<p>So, should companies use them? At some point, will they replace custom development? In short, yes.</p><p>The post .</p>
---------------