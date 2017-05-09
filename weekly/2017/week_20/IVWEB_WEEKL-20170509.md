## 文章索引
1、 <a href="#1fex-技术周刊---2017/05/08" >FEX 技术周刊 - 2017/05/08</a><br/>
2、 <a href="#2文章-实战大规模敏捷" >文章： 实战大规模敏捷</a><br/>
3、 <a href="#3文章-深入浅出tensorflow四卷积神经网络" >文章： 深入浅出Tensorflow（四）：卷积神经网络</a><br/>
4、 <a href="#4视频演讲-深度学习框架的性能优化及其在医药行业的应用实践" >视频演讲： 深度学习框架的性能优化及其在医药行业的应用实践</a><br/>
5、 <a href="#5android开发周报不使用虚拟机的kotlin发布android方法数杂谈" >Android开发周报：不使用虚拟机的Kotlin发布、Android方法数杂谈</a><br/>
6、 <a href="#6ios-开发周报苹果-2017-q2-财报公布基于-cocoapods-进行-ios-开发" >iOS 开发周报：苹果 2017 Q2 财报公布、基于 CocoaPods 进行 iOS 开发</a><br/>
7、 <a href="#7ibm和red-hat会对java模块系统jigsaw投反对票" >IBM和Red Hat会对Java模块系统（Jigsaw）投反对票</a><br/><h1 id="#title_0" >1、FEX 技术周刊 - 2017/05/08</h1>

[http://fex.baidu.com/blog/2017/05/fex-weekly-08//](http://fex.baidu.com/blog/2017/05/fex-weekly-08//)
作者：zhangtao <br> <p>微信搜索『FEX』关注我们的公众号，及时获得最新资讯。</p>

<h2 id="section">深阅读</h2>

<p><strong>Prepack</strong><br />
https://prepack.io/<br />
Prepack is a tool that optimizes JavaScript source code: Computations that can be done at compile-time instead of run-time get eliminated. Prepack replaces the global code of a JavaScript bundle with equivalent code that is a simple sequence of assignments. This gets rid of most intermediate computations and object allocations. 附：.</p>

<p><strong>Elements of JavaScript Style</strong><br />
https://medium.com/javascript-scene/elements-of-javascript-style-caa8821cb99f<br />
The following are guidelines, not immutable laws. There may be valid reasons to deviate from them if doing so clarifies the meaning of the code, but be vigilant and self-aware. These guidelines have stood the test of time for good reason: They’re usually right.</p>

<p><strong>Glossary of Modern JavaScript Concepts: Part 2</strong><br />
https://auth0.com/blog/glossary-of-modern-javascript-concepts-part-2/<br />
In  series, we learned about functional, reactive, and functional reactive programming. In Part 2, we’ll gain an understanding of concepts like scope, closures, tree shaking, components, and more, as well as JavaScript application topics such as data flow and change detection.</p>

<p><strong>Why I’m Moving on to Web Components and Not Looking Back</strong><br />
https://hackernoon.com/why-im-moving-on-to-web-components-and-not-looking-back-aa8028c99c83<br />
Certainly it will take a few more years before large companies are comfortable taking the plunge and ending support for users that have not updated their web browsers. But a truly wonderful world awaits when they do. I hope I am correct in predicting that the complexity and code proliferation in web development, after increasing for many years, is about to take a nose dive. The features that these libraries and frameworks provide have arrived in the “operating system” itself — the web browser. No pre-processors now. Just code.</p>

<p><strong>Energizing Atom with V8’s custom start-up snapshot</strong><br />
https://v8project.blogspot.com/2017/05/energizing-atom-with-v8s-custom-start.html<br />
Native Electron apps, including Atom, leverage Chromium to display a GUI and Node.js as an execution environment, both of which respectively embed V8 to run JavaScript. This allows Electron apps to take advantage of V8 snapshots to quickly initialize a previously serialized heap for faster startup. Electron developers have even released electron-link, a convenience library for setting up this feature, which Atom heavily relies on for its performance optimizations.</p>

<p><strong>Nest - Node.js framework built on top of TypeScript</strong><br />
https://kamilmysliwiec.com/nest-final-release-is-here-node-js-framework-built-top-of-typescript<br />
Nest is a powerful web framework for Node.js, which helps you effortlessly build efficient, scalable applications. It uses modern JavaScript, is built with TypeScript and combines best concepts of both OOP (Object Oriented Progamming) and FP (Functional Programming). GitHub: https://github.com/kamilmysliwiec/nest</p>

<p><strong>支付宝前端构建工具的发展和未来的选择</strong><br />
https://github.com/pigcan/blog/issues/4<br />
下文说说我理解的支付宝前端构建工具发展史，从 spm 到 ant tool，再到未来我们可能会走的路。</p>

<p><strong>V8 Ignition：JS 引擎与字节码的不解之缘</strong><br />
https://zhuanlan.zhihu.com/p/26669846<br />
很多 JS 引擎都是采用了字节码这一脚本语言实现技术的，而 v8 一枝独秀，走“纯机器码”路线，其实过于激进了：虽然执行性能上可以登峰造极，但却带来了内存占用过大的问题。这次引入字节码实则是做了工程上的恰当取舍，将损失掉的内存找回来，更加符合如今移动和嵌入式设备为主的应用场景；以时间换空间，让 v8 能更好的服务于低内存的设备。如今 V8 也回到了字节码的怀抱，不禁令人感叹 JS 引擎与字节码真是有着不解之缘！这个专栏还有很多 Node 及 V8 相关的资料，感兴趣的可以关注。</p>

<p><strong>月活8.89亿背后：微信工程师细数兼容测试经验</strong><br />
http://wetest.qq.com/lab/view/306.html<br />
微信的自动化测试</p>

<p><strong>大数据浪潮下的前端工程师</strong><br />
https://mp.weixin.qq.com/s?__biz=MzUyOTA1NTkzNw==&amp;mid=2247483719&amp;idx=1&amp;sn=48eca5f7bd71f515e18f7b4aa4325a78<br />
我作为一名前端工程师，在阿里巴巴数据团队工作多年，深入了解数据生产加工链路与产品化。我们这群前端是与界面最近的工程师们，似乎与数据离得很远，对于我们来说与数据有些怎样连接呢。</p>

<p><strong>今日头条Go建千亿级微服务的实践</strong><br />
https://mp.weixin.qq.com/s?__biz=MjM5MDE0Mjc4MA==&amp;mid=2650996069&amp;idx=1&amp;sn=63e7f5d5f91f9d84f1c3278426f6edf6<br />
今日头条当前后端服务超过80%的流量是跑在 Go 构建的服务上。微服务数量超过100个，高峰 QPS 超过700万，日处理请求量超过3000亿，是业内最大规模的 Go 应用。</p>

<p><strong>企业的应用架构到底该怎么演变才能合了CEO的愿</strong><br />
https://mp.weixin.qq.com/s?__biz=MzA5Nzc4OTA1Mw==&amp;mid=2659599230&amp;idx=1&amp;sn=cbf97ea56f956e23b3529ea81551b23c<br />
企业信息化建设已经发展了几十年，传统企业和成熟互联网企业的应用架构并没有本质的区别。本文将通过一个线下小型门店成长为多元化集团的发展历程，逐步向读者展示企业应用架构的演变和设计的理念。</p>

<p><strong>Mastering the Node.js Core Modules - The File System &amp; fs Module</strong><br />
https://blog.risingstack.com/mastering-the-nodejs-core-modules-file-system-fs-module/<br />
In this article, we’ll take a look at the File System core module, File Streams and some fs module alternatives.</p>

<p><strong>Why does Google prepend while(1); to their JSON responses?</strong><br />
http://stackoverflow.com/questions/2669690/why-does-google-prepend-while1-to-their-json-responses<br />
It prevents JSON hijacking.</p>

<p><strong>Redesigning Uber Engineering’s Mobile Content Delivery Ecosystem</strong><br />
https://eng.uber.com/mobile-content-delivery/<br />
In this article, we discuss the technical challenges we encountered—and solutions we developed—while building a new content feed and corresponding backend ecosystem for the app.</p>

<p><strong>Building Express Backbone: Facebook’s new long-haul network</strong><br />
https://code.facebook.com/posts/1782709872057497/building-express-backbone-facebook-s-new-long-haul-network/<br />
As new data centers were being built, we realized the need to split the cross-data center vs Internet-facing traffic into different networks and optimize them individually. In a less than a year, we built the first version of our new cross-data center backbone network, called the Express Backbone (EBB), and we’ve been growing it ever since.</p>

<p><strong>Deploy with haste: the story of rig</strong><br />
https://tech.buzzfeed.com/deploy-with-haste-the-story-of-rig-ca9a58b5719a<br />
This is a tale of infrastructure evolution. In the span of 12 months, we went from large, release-oriented deploys to an architecture and approach that enabled 150+ deploys a day. Getting there wasn’t easy, but we learned a lot along the way…</p>

<p><strong>Augmented camera previews for the Dropbox Android Document Scanner</strong><br />
https://blogs.dropbox.com/tech/2017/05/augmented-camera-previews-for-the-dropbox-android-document-scanner/<br />
With Dropbox’s document scanner, a user can take a photo of a document with their phone and convert it into a clean, rectangular PDF. In our previous blog posts (Part 1, Part 2), we presented an overview of document scanner’s machine learning backend, along with its iOS implementation. This post will describe some of technical challenges associated with implementing the document scanner on Android.</p>

<p><strong>How to Get into VR</strong><br />
https://blog.ycombinator.com/how-to-get-into-vr/<br />
In this post, we’ll explore why it’s an exciting time to get into VR now–both for consumers and developers. Then, we’ll discuss how a wide range of interdisciplinary fields have pushed the technology forward. Lastly, we’ll identify concrete ways in which you can get started.</p>

<p><strong>Designing Voice Experiences</strong><br />
https://www.smashingmagazine.com/2017/05/designing-voice-experiences/<br />
Voice-based interfaces are becoming commonplace. A new interface does not mean that we have to disregard everything we have successfully applied to previous interfaces; we will need to adapt our process for the nuances of voice-driven interfaces, including conversational interactions and the lack of a screen. We will look at how a typical genie in a bottle works, discuss the steps involved in designing voice experiences, and illustrate these steps by designing a voice app for Alexa.</p>

<p><strong>Programming as a Way of Thinking</strong><br />
https://blogs.scientificamerican.com/guest-blog/programming-as-a-way-of-thinking/<br />
Modern programming languages are qualitatively different from their predecessors, but we are only beginning to realize the implications of that difference.  In a , I present more ways to use Python to think, explore, learn, and teach.</p>

<p><strong>SQL is 43 years old - here’s 8 reasons we still use it today</strong><br />
http://blog.sqlizer.io/posts/sql-43/<br />
The simple fact that both arrived early in the life of computing, and that for 90% of the time they just work, means databases have become a ‘solved problem’ you no longer need to think about. But people do use other other email automation software and payment solutions, just like people use NoSQL databases. Yet even with other database technology available, albeit less mature technology, SQL still reigns and reigns well. So, finally, here are 8 reasons we still use SQL 43 years after it was first cooked up.</p>

<h2 id="section-1">新鲜货</h2>

<p><strong>Getting Started with Headless Chrome</strong><br />
https://developers.google.com/web/updates/2017/04/headless-chrome<br />
A headless browser is a great tool for automated testing and server environments where you don’t need a visible UI shell. For example, you may want to run some tests against a real web page, create a PDF of it, or just inspect how the browser renders an URL.</p>

<p><strong>pkg - Package your Node.js project into an executable</strong><br />
https://github.com/zeit/pkg<br />
This command line interface enables you to package your Node.js project into an executable that can be run even on devices without Node.js installed.</p>

<p><strong>YouTube’s redesign is official</strong><br />
https://arstechnica.com/gadgets/2017/05/youtubes-desktop-site-gets-a-material-design-makeover-asks-for-feedback/<br />
YouTube’s new interface is built on Google’s Polymer framework, a JavaScript library for creating Web components with a focus on creating Material Design-style apps on the Web.</p>

<p><strong>Progressive Web Apps Training</strong><br />
https://developers.google.com/web/ilt/pwa/<br />
This course shows you how to convert web pages to PWAs. A PWA is not an API or a technology, but it is a web development approach that uses a combination of tools and technologies already available to create targeted, ideal user experiences. It shows how to use service workers, APIs, and an application shell architecture for meaningful offline experiences, fast first load, and easy user reengagement upon repeat visits.</p>

<p><strong>ECMAScript modules in browsers</strong><br />
https://jakearchibald.com/2017/es-modules-in-browsers/<br />
ES modules are starting to land in browsers! They’re in… Safari 10.1; Chrome Canary 60 – behind the Experimental Web Platform flag in chrome:flags; Firefox 54 – behind the dom.moduleScripts.enabled setting in about:config; Edge 15 – behind the Experimental JavaScript Features setting in about:flags.</p>

<p><strong>Electrino</strong><br />
https://github.com/pojala/electrino<br />
A desktop runtime for apps built on web technologies, using the system’s own web browser engine. Electrino is an experimental featherweight alternative to the popular and powerful Electron. It implements a minuscule portion of the APIs available in Electron, but the output app size is much smaller. A “Hello World” app takes 115 MB using Electron, but only 167 kB using Electrino，详见：.</p>

<p><strong>anime.js</strong><br />
http://anime-js.com/<br />
Anime (/ˈæn.ə.meɪ/) is a lightweight JavaScript animation library. It works with any CSS Properties, individual CSS transforms, SVG or any DOM attributes, and JavaScript Objects.</p>

<p><strong>Create Next App</strong><br />
https://github.com/segmentio/create-next-app<br />
The easiest way to create a React app with server-side rendering thanks to Next.js</p>

<p><strong>node-qrcode</strong><br />
https://github.com/soldair/node-qrcode<br />
QR code/2d barcode generator.</p>

<p><strong>GitHub 项目徽章的添加和设置</strong><br />
https://github.com/EyreFree/GitHubBadgeIntroduction<br />
如何更好滴向他人展示自己的项目，介绍项目相关信息呢？用一些通用的小图标来描述项目相关信息不失为一种很棒的选择，几个好看的徽标能够为自己的项目说明增色不少！</p>

<p><strong>Visual Studio Code 1.12</strong><br />
https://code.visualstudio.com/updates/v1_12<br />
周围越来越多人用了</p>

<p><strong>Jenkins Blue Ocean 1.0</strong><br />
https://jenkins.io/projects/blueocean/<br />
Blue Ocean rethinks the user experience of Jenkins. Designed from the ground up for Jenkins Pipeline, but still compatible with Freestyle jobs, Blue Ocean reduces clutter and increases clarity for every member of the team.</p>

<p><strong>Typefont</strong><br />
https://github.com/Sirvasile/Typefont<br />
This project tries to recognize the font of a text in a photo using a set of algorithms and libraries. The goal is to obtain accurate results with the image as only input avoiding other manual processes. This is the only open source project of its kind.</p>

<p><strong>WebSlides - Create HTML presentations in seconds</strong><br />
https://github.com/webslides/webslides/<br />
WebSlides makes HTML presentations easy. Just the essentials and using lovely CSS.</p>

<p><strong>javascript game</strong><br />
https://javascript-game.firebaseapp.com/<br />
测试一下你认识多少个 JS 库的 logo</p>

<p><strong>OnlineSchemaChange</strong><br />
https://github.com/facebookincubator/OnlineSchemaChange<br />
OnlineSchemaChange is a tool for making schema changes for MySQL tables in a non-blocking way.  另附：</p>

<p><strong>MapSCII - The Whole World In Your Console</strong><br />
https://github.com/rastapasta/mapscii<br />
MapSCII is a Braille &amp; ASCII map renderer for your console - enter =&gt; telnet mapscii.me &lt;= on Mac and Linux, connect with PuTTY if you’re using Windows.</p>

<p><strong>Spring 5 Reactive Web</strong><br />
https://dzone.com/articles/spring-5-reactive-web-services<br />
Interested in learning how to use Spring 5 to do reaction web development? Let this article serve as your one-stop shop on the topic.</p>

<h2 id="section-2">产品及其它</h2>

<p><strong>[译]四五十岁之后，还在编程的程序员都有谁</strong><br />
https://mp.weixin.qq.com/s?__biz=MjM5MDE0Mjc4MA==&amp;mid=2650996096&amp;idx=1&amp;sn=e698467a16d3842c891b477d5e3d846f<br />
关于程序员是不是吃青春饭的讨论由来已久，对于那些步入中年的程序员来说，似乎不转管理岗就会被富有活力的年轻程序员替代。但总有些顶级的软件开发者，不愿意从事管理岗位，仍然活跃在一线写着代码。</p>

<p><strong>什么是好产品？</strong><br />
https://mp.weixin.qq.com/s?__biz=MTEwNTM0ODI0MQ==&amp;mid=2653434095&amp;idx=1&amp;sn=ea892392ec474e87df7acb8320057733<br />
可以恰到好处的满足用户需求，拥有完善的技术实现方式，同时可健康持续的创造商业价值的产品，就是「好产品」。另附：</p>

<p><strong>李明远：现在还是不是做产品最好的时代</strong><br />
https://mp.weixin.qq.com/s?__biz=MzA5ODMzMDkzOA==&amp;mid=2661080887&amp;idx=1&amp;sn=4dda6d53f4ebe937e6a73be3f366d8cb<br />
什么是产品？你必须先把公司里那些描述产品的功能定义、模块素描的文档统统清零。抛开这些表面，跟着李明远好好琢磨琢磨：产品的本质，到底是个什么东西。真正的产品，是去满足用户需求痛点、给用户创造快感，或者成本节约带来的感受。这种感受既可感知，也有可能不可感知。</p>

<p>– THE END –</p>
---------------
<h1 id="#title_1" >2、文章： 实战大规模敏捷</h1>
Yousef Awad
[http://www.infoq.com/cn/articles/agile-scaling-action?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/agile-scaling-action?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/agile-scaling-action/zh/smallimage/GettyImages-516893668.jpg"/><p>人们认为，把几个敏捷团队放在一起根本不可能共同去实施一个项目，但这并非事实。所以当企业需要更高水平的开发和测试能力或应对更大的项目时，可以在企业层面将各自独立的敏捷团队整合到同一敏捷环境中。Yousef分享了一些有益的经验之谈。</p> <i>By Yousef Awad</i> <i> Translated by 王强</i>
---------------
<h1 id="#title_2" >3、文章： 深入浅出Tensorflow（四）：卷积神经网络</h1>
郑泽宇
[http://www.infoq.com/cn/articles/introduction-of-tensorflow-part4?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/introduction-of-tensorflow-part4?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/introduction-of-tensorflow-part4/zh/smallimage/xx_logo (2).jpg"/><p>本文将介绍卷积神经网络，通过与传统算法的对比、卷积神经网络的结构分析等方面来介绍卷积神经网络模型，并给出通过TensorFlow在MNIST数据集上实现卷积神经网络的方法。</p> <i>By 郑泽宇</i>
---------------
<h1 id="#title_3" >4、视频演讲： 深度学习框架的性能优化及其在医药行业的应用实践</h1>
朱智勇
[http://www.infoq.com/cn/presentations/deep-learning-optimization-in-pharmaceutical-industry?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/deep-learning-optimization-in-pharmaceutical-industry?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/deep-learning-optimization-in-pharmaceutical-industry/zh/mediumimage/zhuzhiyong_270.jpg"/><p>开源界大致有 5 个比较流行的机器学习框架，我在本次演讲中会对它们进行简要介绍与对比分析，目前这些框架有一个共同的问题那就是只对 GPGPU 平台有较好的支持，在其它平台上(例如 CPU)性能非常差。我们知道机器学习是个很大的概念里面包含很多不同类型的算法模型，而这些模型在不同的平台上会出现不同的性能瓶颈，如何能让这些框架很好地支持多种主流平台以便为不同算法选择提供最佳的运行平台是业界面临的一个问题。在演讲中我们会探讨针对这个问题的一些解决方案和案例研究。</p> <i>By 朱智勇</i>
---------------
<h1 id="#title_4" >5、Android开发周报：不使用虚拟机的Kotlin发布、Android方法数杂谈</h1>
郭亮
[http://www.infoq.com/cn/news/2017/05/Android-weekly-Kotlin-way?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/05/Android-weekly-Kotlin-way?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>本月Android Nougat的份额可谓突飞猛进，相比上月增加了45%，达到了7.1%，上个月还是4.9%。市场研究公司预测今年Android全球手机市场份额将增长5个百分点至90%。本期周报为大家带来了Android安全、多渠道打包、Android方法数等技术干货，欢迎阅读。</p> <i>By 郭亮</i>
---------------
<h1 id="#title_5" >6、iOS 开发周报：苹果 2017 Q2 财报公布、基于 CocoaPods 进行 iOS 开发</h1>
靛青K
[http://www.infoq.com/cn/news/2017/05/iOS-weekly-2017-Q2?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/05/iOS-weekly-2017-Q2?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>苹果 2017 Q2 财报公布、基于 CocoaPods 进行 iOS 开发</p> <i>By 靛青K</i>
---------------
<h1 id="#title_6" >7、IBM和Red Hat会对Java模块系统（Jigsaw）投反对票</h1>
Charles Humble
[http://www.infoq.com/cn/news/2017/05/no-jigsaw?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/05/no-jigsaw?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>InfoQ之前曾经报道过JSR 376（Java平台模块系统）的开发现状，它通常被称为“Jigsaw项目”。现在，有一件不太寻常事情，IBM和Red Hat都公开表示，将会对Jigsaw目前的状态投反对票。</p> <i>By Charles Humble</i> <i> Translated by 张卫滨</i>
---------------