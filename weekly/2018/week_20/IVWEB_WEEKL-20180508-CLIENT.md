## 文章索引
1、 <a href="#1fex-技术周刊---2018/05/07" >FEX 技术周刊 - 2018/05/07</a><br/>
2、 <a href="#2前端每周清单第60期nodejs-10npm-6提速17倍如何设计大型javascript项目" >前端每周清单第60期：Node.js 10，npm 6提速17倍，如何设计大型JavaScript项目？</a><br/>
3、 <a href="#3经典java面试题解析谈谈你对java平台的理解" >经典Java面试题解析——谈谈你对Java平台的理解？</a><br/>
4、 <a href="#4文章-kubernetes-状态管理与扩展" >文章： Kubernetes 状态管理与扩展</a><br/>
5、 <a href="#5迷你书-架构师2018年5月" >迷你书： 架构师（2018年5月）</a><br/>
6、 <a href="#6文章-阿里巴巴提出rnn多比特量化方法推断提速3倍并减少105倍内存消耗" >文章： 阿里巴巴提出RNN多比特量化方法，推断提速3倍并减少10.5倍内存消耗</a><br/>
7、 <a href="#7new-css-features-that-are-changing-web-design" >New CSS Features That Are Changing Web Design</a><br/>
8、 <a href="#8shareit-cto陈少为技术出海如何克服水土不服" >SHAREit CTO陈少为：技术出海如何克服水土不服</a><br/>
9、 <a href="#9区块链从新手到精通看这个公众号就够了" >区块链从新手到精通，看这个公众号就够了</a><br/>
10、 <a href="#10fast-ux-research:-an-easier-way-to-engage-stakeholders-and-speed-up-the-research-process" >Fast UX Research: An Easier Way To Engage Stakeholders And Speed Up The Research Process</a><br/>
11、 <a href="#11oracle发布多语种虚拟机平台graalvm-10" >Oracle发布多语种虚拟机平台GraalVM 1.0</a><br/>
12、 <a href="#12vueconfus大会第二天会议内容概述" >VueConf.US大会第二天会议内容概述</a><br/><h1 id="#title_0" >1、FEX 技术周刊 - 2018/05/07</h1>

[http://fex.baidu.com/blog/2018/05/fex-weekly-07//](http://fex.baidu.com/blog/2018/05/fex-weekly-07//)
作者：zhangzhao <br> <p>微信搜索『FEX』关注我们的公众号，及时获得最新资讯。</p>

<h2 id="section">业界大会</h2>

<p><strong>F8-2018</strong><br />
https://www.f8.com/<br />
.</p>

<h2 id="section-1">深阅读</h2>

<p><strong>NodeJS 10: The New, The Changed, and the Deprecated</strong><br />
https://auth0.com/blog/nodejs-10-new-changes-deprecations/<br />
Node.js 10 comes packed with significant performance improvements through V8 v6.6 and new experimental features such the fs promise API and time traveling. 另附：</p>

<p><strong>Adding BigInts to V8</strong><br />
https://v8project.blogspot.com/2018/05/bigint.html<br />
Over the past couple of months, we have implemented support for BigInts in V8, as currently specified by this proposal, to be included in a future version of ECMAScript. The following post tells the story of our adventures. 另附：.</p>

<p><strong>Version 6 of Angular Now Available</strong><br />
https://blog.angular.io/version-6-of-angular-now-available-cc56b0efa7a4<br />
This is a major release focused less on the underlying framework, and more on the toolchain and on making it easier to move quickly with Angular in the future. </p>

<p><strong>Rethinking Web Performance with Service Workers</strong><br />
https://medium.baqend.com/the-technology-behind-fast-websites-2638196fa60a<br />
This article surveys the current state of the art in page speed optimization through Service Worker technology. It contains the gist of more than 30 man-years of research that went into Speed Kit, an easy-to-use web performance plugin to accelerate websites.</p>

<p><strong>You Don’t Need Redux, MobX, RxJS, Cerebral</strong><br />
https://medium.com/@foxdonut00/you-dont-need-redux-mobx-rxjs-cerebral-6a735b150a02<br />
For state management, try this simple pattern instead of a library
Don’t get me wrong. Those libraries are great. But I’m suggesting a different, unique approach. I know what you’re thinking: Redux alternatives are a dime a dozen. But this isn’t yet another library. In fact, it’s not a library at all. It’s just a simple pattern: Meiosis.</p>

<p><strong>React Suite v3.0 正式版发布</strong><br />
http://div.io/topic/2200<br />
RSUITE（React Suite 的简写）是 一套 React 组件库，为后台产品而生。由 HYPERS 前端团队与 UX 团队打造，主要服务于公司大数据产品线。经历了三次大的版本更新后，累积了大量的组件和丰富的功能。我们的目标：让所有的企业都可以定制化一套属于自己产品风格的组件。</p>

<p><strong>全栈虚拟机GraalVM初体验</strong><br />
https://juejin.im/post/5ad7372f6fb9a045e511b0a4<br />
可以一个文件中同时写 node、ruby、java 等语言</p>

<p><strong>Reported malicious module: getcookies</strong><br />
https://blog.npmjs.org/post/173526807575/reported-malicious-module-getcookies<br />
Early May 2nd, the npm security team received and responded to reports of a package that masqueraded as a cookie parsing library but contained a malicious backdoor. The result of the investigation concluded with three packages and three versions of a fourth package being unpublished from the npm Registry.</p>

<p><strong>A Guide To The State Of Print Stylesheets In 2018</strong><br />
https://www.smashingmagazine.com/2018/05/print-stylesheets-in-2018/<br />
This article will explore how we can best create that second experience. We will take a look at how we should include print styles in our web pages, and look at the specifications that really come into their own once printing. We’ll find out about the state of browser support, and how to best test our print styles. I’ll then give you some pointers as to what to do when a print stylesheet isn’t enough for your printing needs.</p>

<p><strong>Evolution of Couchbase at LinkedIn</strong><br />
https://engineering.linkedin.com/blog/2018/05/evolution-of-couchbase-at-linkedin<br />
This blog post aims to: Tell the story of how our use of Couchbase and our support model evolved over the years; Describe the challenges with scaling and operating Couchbase at our scale and what we’re doing do solve it; Get a glimpse of where we want to take Couchbase into the future.</p>

<p><strong>How fast can you parse JSON?</strong><br />
https://lemire.me/blog/2018/05/03/how-fast-can-you-parse-json/<br />
n a recent paper by Microsoft (), the researchers report parsing JSON document at 0.1 or 0.2 GB/s with common libraries such as RapidJSON. It is hard to tell the exact number as you need to read a tiny plot, but I have the right ballpark. They use a 3.5 GHz processor, so that’s 8 to 16 cycles per input byte of data.</p>

<p><strong>Previewing Elasticsearch 6.3 SQL Feature</strong><br />
https://medium.com/@mustafaakin/previewing-elasticsearch-6-3-sql-feature-2d3a1d60cab4<br />
Elasticsearch 6.3 is announced to contain basic X-Pack features in the repo by default. X-Pack contains APM, Canvas, and most importantly (to me at least) the SQL support. 另附：.</p>

<p><strong>Learning from Source Code</strong><br />
https://www.microsoft.com/en-us/research/blog/learning-source-code/<br />
Program analysis in the past has largely focused on either the formal, machine-interpretable semantics of programs or it has viewed programs as a (somewhat odd) instance of natural language. Approaches from the former are rooted in mathematical logic and require extensive engineering effort for every new case that needs to be handled. On the other hand, natural language approaches involve applications of natural language processing tools that work well on purely syntactic tasks but so far have not been able to learn semantics of programs. In a new paper presented at ICLR 2018, researchers from Microsoft Research and from Simon Fraser University Vancouver present a new way to combine these two worlds and show how to find bugs in released software.</p>

<p><strong>Open-sourcing gVisor, a sandboxed container runtime</strong><br />
https://cloudplatform.googleblog.com/2018/05/Open-sourcing-gVisor-a-sandboxed-container-runtime.html<br />
We’d like to introduce .</p>

<h2 id="section-2">新鲜货</h2>

<p><strong>Proton Native - React Native for the desktop</strong><br />
https://proton-native.js.org/#/<br />
Proton Native does the same to desktop that React Native did to mobile. Build cross-platform apps for the desktop, all while never leaving the React eco-system. Popular React packages such as Redux still work. Same syntax as React Native , Works with existing React libraries such as Redux, Cross platform, Native components. No more Electron, Compatible with all normal Node.js packages. 另附：</p>

<p><strong>New version of the Roadmap of Web Applications on Mobile</strong><br />
https://www.w3.org/blog/news/archives/7006<br />
W3C has published a new version of its Roadmap of Web Applications on Mobile, an overview of the various technologies developed in W3C that increase the capabilities of Web applications, and how they apply more specifically to the mobile context.</p>

<p><strong>Dojo 2.0</strong><br />
https://dojo.io/blog/2018/05/02/2018-05-02-Dojo2-0-0-release/<br />
竟然还健在…看看有几个人还认识这个</p>

<p><strong>Announcing Babylon.js v3.2</strong><br />
https://blogs.windows.com/buildingapps/2018/05/01/announcing-babylon-js-v3-2/#kxuTEvI556G1cmJq.97<br />
支持更多 WebGL2 的功能</p>

<p><strong>Ember’s 2018 Roadmap: A Call for Blog Posts</strong><br />
https://www.emberjs.com/blog/2018/05/02/ember-2018-roadmap-call-for-posts.html<br />
The Ember team would like you to write a blog post to propose goals and direction for Ember in the remainder of 2018. The content of these posts will help us to draft our first Roadmap RFC.</p>

<p><strong>Is ServiceWorker Ready? (Yes.)</strong><br />
https://jakearchibald.github.io/isserviceworkerready/<br />
IE 也支持了：</p>

<p><strong>layerJS - UI composition &amp; animation in pure HTML</strong><br />
https://layerjs.org/<br />
UX patterns like menus, sliders, layers &amp; lightboxes, parallax effects, page-swipes, zoom effects, etc. are really just interactive animated layers. layerJS is a simple open source library that provides one simple universal concept to create such patterns in pure HTML.</p>

<p><strong>React Lifecycle Visualizer</strong><br />
https://github.com/Oblosys/react-lifecycle-visualizer<br />
An npm package for tracing &amp; visualizing lifecycle methods of arbitrary React components.</p>

<p><strong>GitLab Web IDE</strong><br />
https://docs.gitlab.com/ee/user/project/web_ide/<br />
基于 monaco 的 Web IDE</p>

<p><strong>OPENRECORD</strong><br />
https://github.com/PhilWaldmann/openrecord<br />
又一款 node ORM</p>

<p><strong>ow - Function argument validation for humans</strong><br />
https://github.com/sindresorhus/ow</p>

<p><strong>Impact - HTML5 Canvas &amp; JavaScript Game Engine</strong><br />
http://impactjs.com/<br />
Impact is a JavaScript Game Engine that allows you to develop stunning HTML5 Games for desktop and mobile browsers.</p>

<p><strong>Pure CSS Francine</strong><br />
https://github.com/cyanharlow/purecss-francine<br />
An ongoing series in which I create art using only CSS and HTML.</p>

<p><strong>Introducing Elmstatic: an Elm-to-HTML static site generator</strong><br />
https://korban.net/posts/elm/2018-05-03-introducing-elmstatic-elm-static-site-generator/<br />
I’ve been using Elm to generate this site for a few months. It’s still highly experimental and incomplete but I hope that other Elm enthusiasts may find it useful. At the moment, it works for my needs and allows me to generate this site with a single command, but it requires manual intervention if I’m doing things like deleting pages or adding new Elm dependencies, and I’m sure there are many use cases it doesn’t address. I think I have something barebones but useful so I published it on NPM under the name of Elmstatic.</p>

<p><strong>HTML5 Boilerplate 6.1.0 Released</strong><br />
http://htmlcssjavascript.com/web/html5-boilerplate-6-1-0-released/<br />
The biggest change was moving to eslint for JavaScript linting. That was a lingering change we were unable to get into 6.0 and that change ended up being my biggest personal contribution to this release.</p>

<p><strong>8 Top Web Development Trends in 2018</strong><br />
http://merehead.com/blog/web-development-trends-2018/<br />
Web technologies are developing at high-speed. What was popular yesterday doesn’t mean to be the same tomorrow, you should keep this in your mind… 另附：</p>

<p><strong>QCGPU-Rust</strong><br />
https://github.com/QCGPU/qcgpu-rust<br />
Open Source, High Performance &amp; Hardware Accelerated, Quantum Computer Simulation in Rust</p>

<p><strong>ReLaXed - Create PDF documents using web technologies</strong><br />
https://github.com/RelaxedJS/ReLaXed<br />
ReLaXed creates PDF documents interactively using HTML or Pug (a shorthand for HTML). It allows complex layouts to be defined with CSS and JavaScript, while writing the content in a friendly, minimal syntax close to Markdown or LaTeX.</p>

<p><strong>Salsify — A New Architecture for Real-time Internet Video</strong><br />
https://snr.stanford.edu/salsify/<br />
Salsify is a new design for real-time Internet video that jointly controls a video codec and a network transport protocol. Current systems (Skype, Facetime, WebRTC) run these components independently, which produces more glitches and stalls when the network is unpredictable.</p>

<p><strong>Lobe - Deep Learning Made Simple</strong><br />
https://lobe.ai/<br />
Lobe is an easy-to-use visual tool that lets you build custom deep learning models, quickly train them, and ship them directly in your app without writing any code. Start by dragging in a folder of training examples from your desktop. Lobe automatically builds you a custom deep learning model and begins training. When you’re done, you can export a trained model and ship it directly in your app.</p>

<p><strong>TextQL</strong><br />
https://github.com/dinedal/textql<br />
Allows you to easily execute SQL against structured text like CSV or TSV.</p>

<p><strong>Stack Overflow for Teams is Now Available</strong><br />
https://stackoverflow.blog/2018/05/03/stack-overflow-for-teams-is-now-available/<br />
It’s here. After months of designing, building, testing, and beta-ing, we’re happy to announce that as of today, Stack Overflow for Teams has launched and is available to everyone!</p>

<p><strong>Custom domains on GitHub Pages gain support for HTTPS</strong><br />
https://blog.github.com/2018-05-01-github-pages-custom-domains-https/<br />
We have partnered with the certificate authority Let’s Encrypt on this project. As supporters of Let’s Encrypt’s mission to make the web more secure for everyone, we’ve officially become Silver-level sponsors of the initiative. 另附：</p>

<h2 id="section-3">设计</h2>

<p><strong>The Ultimate Guide to Font Sizes in UI Design</strong><br />
https://learnui.design/blog/ultimate-guide-font-sizes-ui-design.html<br />
One of the most common questions I receive from beginning UI designers is: what font size should I use for my project? Sometimes they’re asking about a website, sometimes an Android app, sometimes iPhone/iPad. And you know? I empathize. Material Design has nice guidelines, but they’re like 50 pages long. iOS… well, they don’t even have nice guidelines! And the web is (still) the wild west. Maybe some article pops up – whoa, new sheriff in town – and tells you what font sizes to use based on some dark magic involving the golden ratio, but come on people.</p>

<p><strong>Using Sketch’s Symbols as Links for Big Projects</strong><br />
https://medium.com/sketch-app-sources/sketch-symbol-links-ea4c32f63a16<br />
A simple hack to navigate huge Sketch projects faster.</p>

<p><strong>Building a UI Component Design System</strong><br />
https://blog.bitsrc.io/building-a-consistent-ui-design-system-4481fb37470f<br />
Learn how Uber, Pinterest, Shopify and Airbnb are leveraging components to build a consistent UI/UX design system.</p>

<p><strong>Previewing Material Design 2.0</strong><br />
https://uxdesign.cc/previewing-material-design-2-0-ec0215f0588f<br />
I could (and probably should), wait a couple of weeks until Google I/O before publishing this post where I anticipate we’ll be hearing a lot about MD 2.0. However, that wouldn’t be fun, would it?</p>

<p><strong>Great Questions Lead to Great Design - A Guide to the Design Thinking Process</strong><br />
https://www.toptal.com/designers/product-design/design-thinking-great-questions<br />
Great designers help teams and stakeholders make better decisions by using questions to identify opportunities, reveal underlying needs, and understand user context.</p>

<p><strong>Priority Guides: A Content-First Alternative to Wireframes</strong><br />
http://alistapart.com/article/priority-guides-a-content-first-alternative-to-wireframes<br />
No matter your role, if you’ve ever been involved in a digital design project, chances are you’re familiar with wireframes. After all, they’re among the most popular and widely used tools when designing websites, apps, dashboards, and other digital user interfaces.</p>

<h2 id="section-4">产品及其它</h2>

<p><strong>Jupyter receives the ACM Software System Award</strong><br />
https://blog.jupyter.org/jupyter-receives-the-acm-software-system-award-d433b0dfe3a2<br />
It is our pleasure to announce that Project Jupyter has been awarded the 2017 ACM Software System Award, a significant honor for the project. We are humbled to join an illustrious list of projects that contains major highlights of computing history, including Unix, TeX, S (R’s predecessor), the Web, Mosaic, Java, INGRES (modern databases) and more.</p>

<p><strong>当程序员突然想画画，AI+机器人就该登场了</strong><br />
http://new.qq.com/omn/20180501/20180501A0MI4U.html<br />
澳大利亚人Jeremy Kraybill活了40多岁，突然对绘画产生了兴趣。横亘在他面前的就是那两个问题：既没有艺术灵感，也没有绘画基础。但，他有技术。为了完成一副幅画，他动用了人工智能（神经网络）来产生创意，然后又动用了机械臂，把创意画了出来，最终入围了2018年度 。</p>

<p><strong>北大理科一号楼芯片往事</strong><br />
https://mp.weixin.qq.com/s?__biz=MzU5OTI0NTc3Mg==&amp;mid=2247484759&amp;idx=1&amp;sn=06897e87a26cdc854954fc87a6482365<br />
「甲子光年」采访了近20年以来，多位深入参与MPRC和众志创业历程的芯片从业者。他们的机会、突围、困局、兴奋、迷茫和无奈展示了CPU难题的更多侧面，是自主CPU探索中的一个难得样本。探寻答案的过程中，历史仿佛一个黑箱中复杂缠绕的线团。每当我们理清一个线头，总有下一个更大的线团在等着我们。事件盘根错节，追问抽丝剥茧，这场芯片往事，暗含着宏大的历史难题，也蕴藏着通往明天的答案。</p>

<p><strong>腾讯没有梦想</strong><br />
https://mp.weixin.qq.com/s?__biz=MjM5MDczODM3Mw==&amp;mid=2653028142&amp;idx=1&amp;sn=0dd174c676138016803af3d9ac77e919<br />
腾讯正在丧失产品能力和创业精神，变成一家投资公司。这家快20岁的公司正在变得功利和短视，他的强项不再是产品业务，而是投资财技 。3Q大战过后这8年，腾讯刀枪入库马放南山，以流量和资本为核心动能，走上了开放投资道路。但与此同时，公司逐步失去了内部的产品和创新能力，在搜索/微博/电商/信息流/短视频/云等核心战场不断溃败。另附：</p>

<p><strong>小米是谁，小米为什么而奋斗</strong><br />
https://mp.weixin.qq.com/s?__biz=MjM5NjgzMzkwMQ==&amp;mid=2653646691&amp;idx=1&amp;sn=008521a8648190bcd47c1669d3a7942a<br />
这是每个做产品、开公司的人都需要持续思考的问题，不妨先看看小米的。</p>

<p>– THE END –</p>
---------------
<h1 id="#title_1" >2、前端每周清单第60期：Node.js 10，npm 6提速17倍，如何设计大型JavaScript项目？</h1>
覃云
[http://www.infoq.com/cn/news/2018/05/arch-weekly-60?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/05/arch-weekly-60?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>前端每周清单：Node.js 10，npm 6提速17倍，如何设计大型JavaScript项目？</p> <i>By 覃云</i>
---------------
<h1 id="#title_2" >3、经典Java面试题解析——谈谈你对Java平台的理解？</h1>
杨晓峰
[http://www.infoq.com/cn/news/2018/05/understand-java-platform?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/05/understand-java-platform?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>从你接触Java开发到现在，你对Java最直观的印象是什么呢？是它宣传的 “Compile once, run anywhere”，还是目前看已经有些过于形式主义的语法呢？你对于Java平台到底了解到什么程度？请你先停下来总结思考一下。今天我要问你的问题是，谈谈你对Java平台的理解？“Java是解释执行”，这句话正确吗？</p> <i>By 杨晓峰</i>
---------------
<h1 id="#title_3" >4、文章： Kubernetes 状态管理与扩展</h1>
杨谕黔
[http://www.infoq.com/cn/articles/kubernetes-status-management-and-extension?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/kubernetes-status-management-and-extension?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/kubernetes-status-management-and-extension/zh/smallimage/logo-java-1525624874524.jpeg"/><p>本文通过一个具体实例介绍Kubernetes 扩展开发，分析了API Server的兼容性设计；基于部分源码介绍了Kubernetes API聚合层原理和实现；最后还分析了Kubernetes提供的工具链和客户端抽象，希望为Kubernetes扩展开发提供一些启发 。</p> <i>By 杨谕黔</i>
---------------
<h1 id="#title_4" >5、迷你书： 架构师（2018年5月）</h1>
InfoQ中文站
[http://www.infoq.com/cn/minibooks/architect-201805?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/minibooks/architect-201805?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/minibooks/architect-201805/zh/smallimage/100-1525426276079.jpg"/><p>本期主要内容：Stream：我们为何要从Python转到Go语言？Jeff Dean在SystemML会议上的论文解读：学习索引结构的一些案例；谷歌开源针对iOS的可访问性测试框架；Node.js 10带着npm 6来了！</p> <i>By InfoQ中文站</i>
---------------
<h1 id="#title_5" >6、文章： 阿里巴巴提出RNN多比特量化方法，推断提速3倍并减少10.5倍内存消耗</h1>
许晨等
[http://www.infoq.com/cn/articles/alibaba-rnn-multi-bit-quantization?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/alibaba-rnn-multi-bit-quantization?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/alibaba-rnn-multi-bit-quantization/zh/smallimage/GettyImages-544982936 copy-1525707979588.jpg"/><p>在这个工作中，我们主要考虑神经网络的多比特量化压缩加速问题。我们发现，如果编码的实系数固定，那么离散的二值编码{-1,+1}可以通过二叉搜索树高效的求解。基于这个发现，我们相应地提出交替方向法。</p> <i>By 许晨等</i>
---------------
<h1 id="#title_6" >7、New CSS Features That Are Changing Web Design</h1>
Zell Liew
[https://www.smashingmagazine.com/2018/05/future-of-web-design/](https://www.smashingmagazine.com/2018/05/future-of-web-design/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/05/future-of-web-design/" />
              <title>New CSS Features That Are Changing Web Design</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>New CSS Features That Are Changing Web Design</h1>
                  
                    
                    <address>Zell Liew</address>
                  
                  <time datetime="2018-05-07T12:30:10&#43;02:00" class="op-published">2018-05-07T12:30:10+02:00</time>
                  <time datetime="2018-05-07T20:03:31&#43;00:00" class="op-modified">2018-05-07T20:03:31+00:00</time>
                </header>
                

<p>There was a time when web design got monotonous. Designers and developers built the same kinds of websites over and over again, so much so that we were mocked by people in our own industry for creating only two kinds of websites:</p>

<figure><img src="https://res.cloudinary.com/indysigner/image/upload/v1525708189/which-one-of-the-two-possible-websites-are-you-currently-designing_hxjfnc.png" alt="A tweet by Jon Gold asking: “which one of the two possible websites are you currently designing?”" /><figcaption>: “which one of the two possible websites are you currently designing?”</figcaption></figure>

<p>Is this the limit of what our “creative” minds can achieve? This thought sent an incontrollable pang of sadness into my heart.</p>

<p>I don&rsquo;t want to admit it, but maybe that was the best we could accomplish back then. Maybe we didn&rsquo;t have suitable tools to make creative designs. The demands of the web were evolving quickly, but we were stuck with ancient techniques like floats and tables.</p>

<p>Today, the design landscape has changed completely. We&rsquo;re equipped with new and powerful tools &mdash; CSS Grid, CSS custom properties, CSS shapes and CSS <code>writing-mode</code>, to name a few &mdash; that we can use to exercise our creativity.</p>



<aside class="product-panel product-panel__tilted product-panel--book" data-audience="non-subscriber">
    <div class="container product-panel--book__container">
      <div class="panel__description panel__description--book">
    <p>What if there was a web conference without... slides? Meet <strong>. June <span class="small-caps">26–27</span>. With everything from live designing to live performance audits.</p>
      <a href="https://www.smashingmagazine.com/events/toronto-2018/#speakers" class="btn btn--green btn--large">
        Check the speakers&nbsp;→
      </a>
      </div>
      <div class="panel__image panel__image--book">
        <a href="https://www.smashingmagazine.com/events/toronto-2018/#speakers" class="books__book__image">
        <div class="books__book__img">
          <img src="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5a0383cf-197a-49b9-975a-9d1f02c1ace9/dan-hov.png" alt="SmashingConf Toronto 2018, with Dan Mall, Sara Soueidan, Lea Verou and many others." width="310" height="400">
        </div>
      </a>
      </div>
    </div>
  </aside>





<div class="c-garfield-the-cat">


<h3 id="how-css-grid-changed-everything">How CSS Grid Changed Everything</h3>

<p>Grids are essential for web design; you already knew that. But have you stopped to asked yourself how you designed the grid you mainly use?</p>

<p>Most of us haven&rsquo;t. We use the 12-column grid that has became a standard in our industry.</p>

<ul>
<li>But why do we use the same grid?</li>
<li>Why are grids made of 12 columns?</li>
<li>Why are our grids sized equally?</li>
</ul>

<p>Here&rsquo;s one possible answer to why we use the same grid: <strong>We don&rsquo;t want to do the math</strong>.</p>

<p>In the past, with float-based grids, to create a three-column grid, you needed to calculate the width of each column, the size of each gutter, and how to position each grid item. Then, you needed to create classes in the HTML to style them appropriately. It was .</p>

<p>To make things easier, we adopted grid frameworks. In the beginning, frameworks such as  allowed us to choose between 8-, 9-, 12- and even 16-column grids. Later, Bootstrap won the frameworks war. Because Bootstrap allowed only 12 columns, and changing that was a pain, we eventually settled on 12 columns as the standard.</p>

<p>But we shouldn&rsquo;t blame Bootstrap. It was the best approach back then. Who wouldn&rsquo;t want a good solution that works with minimal effort? With the grid problem settled, we turned our attention to other aspects of design, such as typography, color and accessibility.</p>

<p>Now, with the <strong>advent of CSS Grid, grids have become much simpler</strong>. We no longer have to fear grid math. It’s become so simple that I would argue that creating a grid is easier with CSS than in a design tool such as Sketch!</p>

<p>Why?</p>

<p>Let&rsquo;s say you want to make a 4-column grid, each column sized at 100 pixels. With CSS Grid, you can write <code>100px</code> four times in the <code>grid-template-columns</code> declaration, and a 4-column grid will be created.</p>

<pre><code class="language-css">.grid {
  display: grid;
  grid-template-columns: 100px 100px 100px 100px;
  grid-column-gap: 20px;
}
</code></pre>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9287f25c-75f8-456b-9f22-b3190802d543/future-web-design-grid-four.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9287f25c-75f8-456b-9f22-b3190802d543/future-web-design-grid-four.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9287f25c-75f8-456b-9f22-b3190802d543/future-web-design-grid-four.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9287f25c-75f8-456b-9f22-b3190802d543/future-web-design-grid-four.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9287f25c-75f8-456b-9f22-b3190802d543/future-web-design-grid-four.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9287f25c-75f8-456b-9f22-b3190802d543/future-web-design-grid-four.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9287f25c-75f8-456b-9f22-b3190802d543/future-web-design-grid-four.png"
			sizes="100vw"
			alt="Screenshot of Firefox&#39;s grid inspector that shows four columns."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			You can create four grid columns by specifying a column-width four times in <code>grid-template-columns</code>
		</figcaption>
	
</figure>


<p>If you want a 12-column grid, you just have to repeat <code>100px</code> 12 times.</p>

<pre class="break-out"><code class="language-css">.grid {
  display: grid;
  grid-template-columns: 100px 100px 100px 100px 100px 100px 100px 100px 100px 100px 100px 100px;
  grid-column-gap: 20px;
}
</code></pre>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/61ab598a-9c0d-4d81-a624-3fbca4dfb6b2/future-web-design-grid-twelve.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/61ab598a-9c0d-4d81-a624-3fbca4dfb6b2/future-web-design-grid-twelve.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/61ab598a-9c0d-4d81-a624-3fbca4dfb6b2/future-web-design-grid-twelve.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/61ab598a-9c0d-4d81-a624-3fbca4dfb6b2/future-web-design-grid-twelve.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/61ab598a-9c0d-4d81-a624-3fbca4dfb6b2/future-web-design-grid-twelve.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/61ab598a-9c0d-4d81-a624-3fbca4dfb6b2/future-web-design-grid-twelve.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/61ab598a-9c0d-4d81-a624-3fbca4dfb6b2/future-web-design-grid-twelve.png"
			sizes="100vw"
			alt="Screenshot of Firefox&#39;s grid inspector that shows twelve columns."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Creating 12 columns with CSS Grid
		</figcaption>
	
</figure>


<p>Yes, the code isn&rsquo;t beautiful, but we&rsquo;re not concerned with optimizing for code quality (yet) &mdash; we&rsquo;re still thinking about design. CSS Grid makes it so easy for anyone &mdash; even a designer without coding knowledge &mdash; to create a grid on the web.</p>

<p>If you want to create grid columns with different widths, you just have to specify the desired width in your <code>grid-template-columns</code> declaration, and you&rsquo;re set.</p>

<pre><code class="language-css">.grid {
  display: grid;
  grid-template-columns: 100px 162px 262px;
  grid-column-gap: 20px;
}
</code></pre>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6be83c78-9646-4c17-8d74-a3ffa55c13e1/future-web-design-grid-asym.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6be83c78-9646-4c17-8d74-a3ffa55c13e1/future-web-design-grid-asym.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6be83c78-9646-4c17-8d74-a3ffa55c13e1/future-web-design-grid-asym.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6be83c78-9646-4c17-8d74-a3ffa55c13e1/future-web-design-grid-asym.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6be83c78-9646-4c17-8d74-a3ffa55c13e1/future-web-design-grid-asym.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6be83c78-9646-4c17-8d74-a3ffa55c13e1/future-web-design-grid-asym.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6be83c78-9646-4c17-8d74-a3ffa55c13e1/future-web-design-grid-asym.png"
			sizes="100vw"
			alt="Screenshot of Firefox&#39;s grid inspector that shows three colums of different width."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Creating columns of different widths is easy as pie.
		</figcaption>
	
</figure>


<h4 id="making-grids-responsive">Making Grids Responsive</h4>

<p>No discussion about CSS Grid is complete without talking about the responsive aspect. There are several ways to make CSS Grid responsive. One way (probably the most popular way) is to use the <code>fr</code> unit. Another way is to change the number of columns with media queries.</p>

<p><code>fr</code> is a flexible length that represents a fraction. When you use the <code>fr</code> unit, browsers divide up the open space and allocate the areas to columns based on the <code>fr</code> multiple. This means that to create four columns of equal size, you would write <code>1fr</code> four times.</p>

<pre><code class="language-css">.grid {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr 1fr;
  grid-column-gap: 20px;
}
</code></pre>

<figure>)</figcaption></figure>

<p><strong>Let&rsquo;s do some calculations to understand why four equal-sized columns are created</strong>.</p>

<p>First, let&rsquo;s assume the total space available for the grid is <code>1260px</code>.</p>

<p>Before allocating width to each column, CSS Grid needs to know how much space is available (or leftover). Here, it subtracts <code>grip-gap</code> declarations from <code>1260px</code>. Since each gap <code>20px</code>, we&rsquo;re left with <code>1200px</code> for the available space. <code>(1260 - (20 * 3) = 1200)</code>.</p>

<p>Next, it adds up the <code>fr</code> multiples. In this case, we have four <code>1fr</code> multiples, so browsers divide <code>1200px</code> by four. Each column is thus <code>300px</code>. This is why we get four equal columns.</p>

<p><strong>However, grids created with the <code>fr</code> unit aren&rsquo;t always equal</strong>!</p>

<p>When you use <code>fr</code>, you need to be aware that each <code>fr</code> unit is a fraction of the available (or leftover) space.</p>

<p>If you have an element that is wider than any of the columns created with the <code>fr</code> unit, the calculation needs to be done differently.</p>

<p>For example, the grid below has one large column and three small (but equal) columns even though it&rsquo;s created with <code>grid-template-columns: 1fr 1fr 1fr 1fr</code>.</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="vjWQep"
   data-user="smashingmag"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<p>After splitting <code>1200px</code> into four and allocating <code>300px</code> to each of the <code>1fr</code> columns, browsers realize that the first grid item contains an image that is <code>1000px</code>. Since <code>1000px</code> is larger than <code>300px</code>, browsers choose to allocate <code>1000px</code> to the first column instead.</p>


  <div id="sponsors-article" data-impression="true" class="c-promo-box c-promo-box--ad sponsors hidden" data-audience="non-subscriber" data-remove="true"></div>



<p>That means, we need to recalculate leftover space.</p>

<p>The new leftover space is <code>1260px - 1000px - 20px * 3 = 200px</code>; this <code>200px</code> is then divided by three according to the amount of leftover fractions. Each fraction is then <code>66px</code>. Hopefully that explains why <code>fr</code> units do not always create equal-width columns.</p>

<p>If you want the <code>fr</code> unit to create equal-width columns everytime, you need to force it with <code>minmax(0, 1fr)</code>. For this specific example, you’ll also want to set the image’s <code>max-width</code> property to 100%.</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="NMwEvo"
   data-user="smashingmag"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<p><strong>Note</strong>: <em>Rachel Andrew has written an amazing  on how different CSS values (min-content, max-content, fr, etc.) affect content sizes. It’s worth a read!</em></p>

<h4 id="unequal-width-grids">Unequal-Width Grids</h4>

<p>To create grids with unequal widths, you simply vary the fr multiple. Below is a grid that follows the golden ratio, where the second column is 1.618 times of the first column, and the third column is 1.618 times of the second column.</p>

<pre><code class="language-css">.grid {
  display: grid;
  grid-template-columns: 1fr 1.618fr 2.618fr;
  grid-column-gap: 1em;
}
</code></pre>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/18f3c1ee-74f1-4bdc-b747-1019285f671b/future-web-design-grid-fr-asym.gif">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/18f3c1ee-74f1-4bdc-b747-1019285f671b/future-web-design-grid-fr-asym.gif 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/18f3c1ee-74f1-4bdc-b747-1019285f671b/future-web-design-grid-fr-asym.gif 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/18f3c1ee-74f1-4bdc-b747-1019285f671b/future-web-design-grid-fr-asym.gif 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/18f3c1ee-74f1-4bdc-b747-1019285f671b/future-web-design-grid-fr-asym.gif 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/18f3c1ee-74f1-4bdc-b747-1019285f671b/future-web-design-grid-fr-asym.gif 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/18f3c1ee-74f1-4bdc-b747-1019285f671b/future-web-design-grid-fr-asym.gif"
			sizes="100vw"
			alt="GIF shows a three-column grid created with the golden ratio. When the browser is resized, the columns resize accordingly."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			A three-column grid created with the golden ratio
		</figcaption>
	
</figure>


<h4 id="changing-grids-at-different-breakpoints">Changing Grids At Different Breakpoints</h4>

<p>If you want to change the grid at different breakpoints, you can declare a new grid within a media query.</p>

<pre><code class="language-css">.grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-column-gap: 1em;
}

@media (min-width: 30em) {
  .grid {
    grid-template-columns: 1fr 1fr 1fr 1fr;
  }
}
</code></pre>

<p>Isn&rsquo;t it easy to create grids with CSS Grid? Earlier designers and developers would have killed for such a possibility.</p>

<h4 id="height-based-grids">Height-Based Grids</h4>

<p>It was impossible to make grids based on the height of a website previously because there wasn&rsquo;t a way for us to tell how tall the viewport was. Now, with viewport units, CSS Calc, and CSS Grid, we can even make grids based on viewport height.</p>

<p>In the demo below, I created grid squares based on the height of the browser.</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="qoEYaL"
   data-user="zellwk"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<p>Jen Simmons has a great video that talks about  &mdash; with CSS Grid. I highly recommend you watch it.</p>

<h4 id="grid-item-placement">Grid Item Placement</h4>

<p>Positioning grid items was a big pain in the past because you had to calculate the <code>margin-left</code> property.</p>

<p>Now, with CSS Grid, you can place grid items directly with CSS without the extra calculations.</p>

<pre><code class="language-css">.grid-item {
  grid-column: 2; /* Put on the second column */
}
</code></pre>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bf790516-2d0d-4078-aac0-6a1d9357a74b/future-web-design-grid-placement.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bf790516-2d0d-4078-aac0-6a1d9357a74b/future-web-design-grid-placement.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bf790516-2d0d-4078-aac0-6a1d9357a74b/future-web-design-grid-placement.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bf790516-2d0d-4078-aac0-6a1d9357a74b/future-web-design-grid-placement.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bf790516-2d0d-4078-aac0-6a1d9357a74b/future-web-design-grid-placement.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bf790516-2d0d-4078-aac0-6a1d9357a74b/future-web-design-grid-placement.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bf790516-2d0d-4078-aac0-6a1d9357a74b/future-web-design-grid-placement.png"
			sizes="100vw"
			alt="Screenshot of a grid item placed on the second column"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Placing an item on the second column.
		</figcaption>
	
</figure>


<p>You can even tell a grid item how many columns it should take up with the <code>span</code> keyword.</p>

<pre><code class="language-css">.grid-item {
  /* Put in the second column, span 2 columns */
  grid-column: 2 / span 2;
}
</code></pre>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a66e3449-3bd9-40ff-8fe2-6116c0939d77/future-web-design-grid-placement-span.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a66e3449-3bd9-40ff-8fe2-6116c0939d77/future-web-design-grid-placement-span.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a66e3449-3bd9-40ff-8fe2-6116c0939d77/future-web-design-grid-placement-span.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a66e3449-3bd9-40ff-8fe2-6116c0939d77/future-web-design-grid-placement-span.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a66e3449-3bd9-40ff-8fe2-6116c0939d77/future-web-design-grid-placement-span.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a66e3449-3bd9-40ff-8fe2-6116c0939d77/future-web-design-grid-placement-span.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a66e3449-3bd9-40ff-8fe2-6116c0939d77/future-web-design-grid-placement-span.png"
			sizes="100vw"
			alt="Screenshot of a grid item that&#39;s placed on the second column. It spans two columns"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			You can tell grid items the number of columns (or even rows) they should occupy with the <code>span</code> keyword
		</figcaption>
	
</figure>


<h4 id="inspirations">Inspirations</h4>

<p>CSS Grid enables you to lay things out so easily that you can create a lot of variations of the same website quickly. One prime example is .</p>

<figure class="video-container"><iframe data-src="https://player.vimeo.com/video/267241410" width="600" height="480" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe></figure>

<p>If you&rsquo;d like to find out more about what CSS Grid can do, check out , where she explores how to create different kinds of layouts with CSS Grid and other tools.</p>

<p>To learn more about CSS Grid, check out the following resources:</p>

<ul>
<li>, Rachel Andrew and Jen Simmons<br />
Video tutorials</li>
<li>, Jen Simmons<br />
A series of videos about layout</li>
<li>, Rachel Andrew<br />
A CSS layout course</li>
<li>, Jonathan Suh<br />
A free course on CSS Grid.</li>
<li>, Dave Geddes<br />
A fun way to learn CSS Grid</li>
</ul>




  <aside class="product-panel product-panel__tilted product-panel--book" data-audience="non-subscriber" data-remove="true">
    <div class="container product-panel--book__container">
      <div class="panel__description panel__description--book">
        <p>
          Is your pattern library up to date today? <em>Alla Kholmatova</em> has just finished a fully fledged book on <strong>Design Systems</strong> and how to get them right. With common traps, gotchas and the lessons she learned. Hardcover, eBook. <em>Just sayin'.</em>
        </p>
        <a href="https://www.smashingmagazine.com/printed-books/design-systems/">
          <button class="btn btn--green btn--large">
            Table of Contents&nbsp;&rarr;
          </button>
        </a>
      </div>
      <div class="panel__image panel__image--book">
        <a href="https://www.smashingmagazine.com/printed-books/design-systems/" class="books__book__image">
        <div class="books__book__img">
          <img src="https://www.smashingmagazine.com/images/books/design-systems--large-opt.png">
        </div>
      </a>
      </div>
    </div>
  </aside>




<h3 id="designing-with-irregular-shapes">Designing With Irregular Shapes</h3>

<p>We are used to creating rectangular layouts on the web because the CSS box model is a rectangle. Besides rectangles, we’ve also found ways to create simple shapes, such as triangles and circles.</p>

<p>Today, we don&rsquo;t need to stop there. With CSS shapes and <code>clip-path</code> at our disposal, we can create irregular shapes without much effort.</p>

<p>For example,  experimented with a comic-strip-inspired layout with CSS Grid and <code>clip path</code>.</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="LzLXYJ"
   data-user="rrenula"
   data-default-tab="result"
   class='codepen'>See the Pen . </p>


<p> along the Beyoncé curve.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e2b60894-b7dd-41ac-94dd-b87a6bdf3cbc/future-web-design-beyonce.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e2b60894-b7dd-41ac-94dd-b87a6bdf3cbc/future-web-design-beyonce.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e2b60894-b7dd-41ac-94dd-b87a6bdf3cbc/future-web-design-beyonce.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e2b60894-b7dd-41ac-94dd-b87a6bdf3cbc/future-web-design-beyonce.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e2b60894-b7dd-41ac-94dd-b87a6bdf3cbc/future-web-design-beyonce.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e2b60894-b7dd-41ac-94dd-b87a6bdf3cbc/future-web-design-beyonce.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e2b60894-b7dd-41ac-94dd-b87a6bdf3cbc/future-web-design-beyonce.png"
			sizes="100vw"
			alt="An image of Huijing&#39;s article, where text flows around Beyoncé."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Text can flow around Beyoncé if you wanted it to!
		</figcaption>
	
</figure>


<p>If you&rsquo;d like to dig deeper, .</p>

<p>CSS shapes and <code>clip-path</code> give you infinite possibilities to create custom shapes unique to your designs. Unfortunately, syntax-wise, CSS shapes and <code>clip-path</code> aren&rsquo;t as intuitive as CSS Grid. Luckily, we have tools such as  to help us create the shapes we want.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1c101607-4aac-4fa9-a968-62a33133331c/future-web-design-clippy.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1c101607-4aac-4fa9-a968-62a33133331c/future-web-design-clippy.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1c101607-4aac-4fa9-a968-62a33133331c/future-web-design-clippy.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1c101607-4aac-4fa9-a968-62a33133331c/future-web-design-clippy.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1c101607-4aac-4fa9-a968-62a33133331c/future-web-design-clippy.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1c101607-4aac-4fa9-a968-62a33133331c/future-web-design-clippy.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1c101607-4aac-4fa9-a968-62a33133331c/future-web-design-clippy.png"
			sizes="100vw"
			alt="Image of Clippy, a tool to help you create custom CSS shapes"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Clippy helps you create custom shapes easily with <code>clip-path</code>.
		</figcaption>
	
</figure>


<h3 id="switching-text-flow-with-css-writing-mode">Switching Text Flow With CSS’ <code>writing-mode</code></h3>

<p>We&rsquo;re used to seeing words flow from left to right on the web because the web is predominantly made for English-speaking folks (at least that&rsquo;s how it started).</p>

<p>But some languages don&rsquo;t flow in that direction. For example, Chinese words can read top down and right to left.</p>

<p>CSS’ <code>writing-mode</code> makes text flow in the direction native to each language. Hui Jing experimented with a Chinese-based layout that flows top down and right to left on a website called ”.</p>

<p>Besides articles, Hui Jing has a great talk on typography and <code>writing-mode</code>, “”. I highly encourage you to watch it.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2f69df2b-18d2-4da4-8e44-22226ef0becd/future-web-design-penang-hokkien.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2f69df2b-18d2-4da4-8e44-22226ef0becd/future-web-design-penang-hokkien.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2f69df2b-18d2-4da4-8e44-22226ef0becd/future-web-design-penang-hokkien.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2f69df2b-18d2-4da4-8e44-22226ef0becd/future-web-design-penang-hokkien.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2f69df2b-18d2-4da4-8e44-22226ef0becd/future-web-design-penang-hokkien.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2f69df2b-18d2-4da4-8e44-22226ef0becd/future-web-design-penang-hokkien.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2f69df2b-18d2-4da4-8e44-22226ef0becd/future-web-design-penang-hokkien.png"
			sizes="100vw"
			alt="An image of the Penang Hokken, showcasing text that reads from top to bottom and right to left."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Penang Hokkien shows that Chinese text can be written from top to bottom, right to left.
		</figcaption>
	
</figure>


<p>Even if you don&rsquo;t design for languages like Chinese, it doesn&rsquo;t mean you can&rsquo;t apply CSS’ <code>writing-mode</code> to English. Back in 2016, when I created , I flexed a small creative muscle and opted to rotate text with <code>writing-mode</code>.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/70acafa4-5454-4257-bbdd-3f5fe18d3696/future-web-design-devfest.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/70acafa4-5454-4257-bbdd-3f5fe18d3696/future-web-design-devfest.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/70acafa4-5454-4257-bbdd-3f5fe18d3696/future-web-design-devfest.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/70acafa4-5454-4257-bbdd-3f5fe18d3696/future-web-design-devfest.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/70acafa4-5454-4257-bbdd-3f5fe18d3696/future-web-design-devfest.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/70acafa4-5454-4257-bbdd-3f5fe18d3696/future-web-design-devfest.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/70acafa4-5454-4257-bbdd-3f5fe18d3696/future-web-design-devfest.png"
			sizes="100vw"
			alt="An image that shows how I rotated text in a design I created for Devfest.asia"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Tags were created by using writing mode and transforms.
		</figcaption>
	
</figure>


<p> contains many experiments with <code>writing-mode</code>, too. I highly recommend checking it out, too.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4f024681-c86e-4009-89aa-1ff379e71e8a/future-web-design-lab.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4f024681-c86e-4009-89aa-1ff379e71e8a/future-web-design-lab.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4f024681-c86e-4009-89aa-1ff379e71e8a/future-web-design-lab.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4f024681-c86e-4009-89aa-1ff379e71e8a/future-web-design-lab.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4f024681-c86e-4009-89aa-1ff379e71e8a/future-web-design-lab.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4f024681-c86e-4009-89aa-1ff379e71e8a/future-web-design-lab.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4f024681-c86e-4009-89aa-1ff379e71e8a/future-web-design-lab.png"
			sizes="100vw"
			alt="An image from Jen Simmon&#39;s lab that shows a design from Jan Tschichold."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			An image from Jen Simmon's lab that shows Jan Tschichold
		</figcaption>
	
</figure>


<h3 id="effort-and-ingenuity-go-a-long-way">Effort And Ingenuity Go A Long Way</h3>

<p>Even though the new CSS tools are helpful, you don&rsquo;t need any of them to create unique websites. A little ingenuity and some effort go a long way.</p>

<p>For example, in  rotates the entire website by -15 degrees and makes you look silly when reading the website.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e308a830-ba6a-431c-8e5d-c4128cad965a/future-web-design-supersilly.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e308a830-ba6a-431c-8e5d-c4128cad965a/future-web-design-supersilly.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e308a830-ba6a-431c-8e5d-c4128cad965a/future-web-design-supersilly.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e308a830-ba6a-431c-8e5d-c4128cad965a/future-web-design-supersilly.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e308a830-ba6a-431c-8e5d-c4128cad965a/future-web-design-supersilly.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e308a830-ba6a-431c-8e5d-c4128cad965a/future-web-design-supersilly.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e308a830-ba6a-431c-8e5d-c4128cad965a/future-web-design-supersilly.png"
			sizes="100vw"
			alt="A screenshot from Super Silly Hackthon, with text slightly rotated to the left"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Cheeaun makes sure you look silly if you want to enter Super Silly Hackathon.
		</figcaption>
	
</figure>


<p> with some trigonometry and GSAP. Look at how cute the ape is and how it covers its eyes when you focus on the password field. Lovely!</p>

<figure class="video-container"><iframe data-src="https://player.vimeo.com/video/267239924" width="600" height="480" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe></figure>

<p>When I created the sales page for my course, , I added elements that make the JavaScript learner feel at home.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6b66f918-dc6f-4da1-870e-aa6b5ea8029c/future-web-design-learnjavascript.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6b66f918-dc6f-4da1-870e-aa6b5ea8029c/future-web-design-learnjavascript.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6b66f918-dc6f-4da1-870e-aa6b5ea8029c/future-web-design-learnjavascript.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6b66f918-dc6f-4da1-870e-aa6b5ea8029c/future-web-design-learnjavascript.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6b66f918-dc6f-4da1-870e-aa6b5ea8029c/future-web-design-learnjavascript.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6b66f918-dc6f-4da1-870e-aa6b5ea8029c/future-web-design-learnjavascript.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6b66f918-dc6f-4da1-870e-aa6b5ea8029c/future-web-design-learnjavascript.png"
			sizes="100vw"
			alt="Image where I used JavaScript elements in the design for Learn JavaScript."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			I used the <code>function</code> syntax to create course packages instead of writing about course packages
		</figcaption>
	
</figure>


<h3 id="wrapping-up">Wrapping Up</h3>

<p>A unique web design isn&rsquo;t just about layout. It&rsquo;s about how the design integrates with the content. With a little effort and ingenuity, all of us can create unique designs that speak to our audiences. The tools at our disposal today make our jobs easier.</p>

<p>The question is, do you care enough to make a unique design? I hope you do.</p>




<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(ra, il, al)</span>
</div>


</div>




  <div id="sponsors-article-end" data-impression="true" class="c-promo-box c-promo-box--ad c-promo-box--wide sponsors hidden" data-audience="non-subscriber" data-remove="true"></div>



              </article>
            </body>
          </html>
---------------
<h1 id="#title_7" >8、SHAREit CTO陈少为：技术出海如何克服水土不服</h1>
贾凯强
[http://www.infoq.com/cn/news/2018/05/SHAREit-CTO?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/05/SHAREit-CTO?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p></p> <i>By 贾凯强</i>
---------------
<h1 id="#title_8" >9、区块链从新手到精通，看这个公众号就够了</h1>
Tina
[http://www.infoq.com/cn/news/2018/05/Block-chain-novice-proficient?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/05/Block-chain-novice-proficient?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>2018年开始，InfoQ为千万互联网人打造了一个区块链技术公众号：区块链前哨。这个公众号，旨在帮你掌握最前沿区块链资讯，并会深度分析区块链技术，致力于区块链技术普及。同时我们还有千人交流社群，不定期会举办线上技术分享。我们希望，从新手到精通的过程中，你只需要关注这一个专业助手。</p> <i>By Tina</i>
---------------
<h1 id="#title_9" >10、Fast UX Research: An Easier Way To Engage Stakeholders And Speed Up The Research Process</h1>
Zoe Dimov
[https://www.smashingmagazine.com/2018/05/fast-ux-research/](https://www.smashingmagazine.com/2018/05/fast-ux-research/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/05/fast-ux-research/" />
              <title>Fast UX Research: An Easier Way To Engage Stakeholders And Speed Up The Research Process</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>Fast UX Research: An Easier Way To Engage Stakeholders And Speed Up The Research Process</h1>
                  
                    
                    <address>Zoe Dimov</address>
                  
                  <time datetime="2018-05-04T14:00:27&#43;02:00" class="op-published">2018-05-04T14:00:27+02:00</time>
                  <time datetime="2018-05-07T20:03:31&#43;00:00" class="op-modified">2018-05-07T20:03:31+00:00</time>
                </header>
                

<p>Today, UX research has earned wide recognition as an essential part of product and service design. However, UX professionals still seem to be facing two big problems when it comes to UX research: A lack of engagement from the team and stakeholders as well as the pressure to constantly reduce the time for research.</p>

<p>In this article, I’ll take a closer look at each of these challenges and propose a new approach known as ‘FAST UX’ in order to solve them. This is a simple but <strong>powerful tool that you can use to speed up UX research</strong> and turn stakeholders into active champions of the process.</p>

<p>Contrary to what you might think, speeding up the research process (in both the short and long term) requires effective collaboration, rather than you going away and soldiering on by yourself.</p>

<p>The acronym FAST (<strong>F</strong>ocus, <strong>A</strong>ttend, <strong>S</strong>ummarise, <strong>T</strong>ranslate) wraps up a number of techniques and ideas that make the UX process more transparent, fun, and collaborative. I also describe a 5-day project with a central UK government department that shows you how the model can be put into practice.</p>

<p>The article is relevant for UX professionals and the people who work with them, including product owners, engineers, business analysts, scrum masters, marketing and sales professionals.</p>

<h4 id="1-lack-of-engagement-of-the-team-and-stakeholders">1. Lack Of Engagement Of The Team And Stakeholders</h4>

<blockquote>“Stakeholders have the capacity for being your worst nightmare and your best collaborator.”<br /><br />&mdash;  (2017)</blockquote>

<p>As UX researchers, : from the design of the study (objectives, research questions), to recruitment, set up, fieldwork, analysis and the final presentation.</p>



  <aside class="product-panel product-panel__tilted product-panel--book" data-audience="non-subscriber" data-remove="true">
    <div class="container product-panel--book__container">
      <div class="panel__description panel__description--book">
        <p>
          Is your pattern library up to date today? <em>Alla Kholmatova</em> has just finished a fully fledged book on <strong>Design Systems</strong> and how to get them right. With common traps, gotchas and the lessons she learned. Hardcover, eBook. <em>Just sayin'.</em>
        </p>
        <a href="https://www.smashingmagazine.com/printed-books/design-systems/">
          <button class="btn btn--green btn--large">
            Table of Contents&nbsp;&rarr;
          </button>
        </a>
      </div>
      <div class="panel__image panel__image--book">
        <a href="https://www.smashingmagazine.com/printed-books/design-systems/" class="books__book__image">
        <div class="books__book__img">
          <img src="https://www.smashingmagazine.com/images/books/design-systems--large-opt.png">
        </div>
      </a>
      </div>
    </div>
  </aside>








    










<div class="c-garfield-the-cat">


<p>Anyone who has tried to do this knows that it can be extremely difficult to organize and get stakeholders to participate in research. There are two main reasons for this:</p>

<ol>
    <li><strong>Research is somebody else’s job</strong>.<br />In my experience, UX professionals are often hired to “do the UX” for a company or organization. Even though the title of “Lead UX Researcher” sounds great and very important in my head, it often leads to misconceptions during kick-off meetings. Everyone automatically assumes that research is solely MY responsibility. It’s no wonder that stakeholders don’t want to get involved in the project. They assume research is my and nobody else’s job.</li>
    <li><strong>UX process frameworks are incomplete</strong>.<br />The problem is that even when stakeholders want to engage and participate in UX, they still do not know *how* they should get involved and *what* they should do. We spend a lot of time selling a UX process and research frameworks that are useful but ultimately incomplete &mdash; they do not explain how non-researchers can get involved in the research process.</li>
</ol>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e55428b7-ec3c-4bf9-908d-2ad08259bbf4/fig1-stakeholder-challenges.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e55428b7-ec3c-4bf9-908d-2ad08259bbf4/fig1-stakeholder-challenges.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e55428b7-ec3c-4bf9-908d-2ad08259bbf4/fig1-stakeholder-challenges.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e55428b7-ec3c-4bf9-908d-2ad08259bbf4/fig1-stakeholder-challenges.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e55428b7-ec3c-4bf9-908d-2ad08259bbf4/fig1-stakeholder-challenges.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e55428b7-ec3c-4bf9-908d-2ad08259bbf4/fig1-stakeholder-challenges.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e55428b7-ec3c-4bf9-908d-2ad08259bbf4/fig1-stakeholder-challenges.jpg"
			sizes="100vw"
			alt="Problems associated with stakeholders involvement in UX Research."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Fig. 1. Despite our enthusiasm as researchers, stakeholders often don’t understand how to get involved with the research process.
		</figcaption>
	
</figure>


<p>Further, a lot of stakeholders can find words such as ‘design,’ ‘analysis’ or ‘fieldwork’ intimidating or irrelevant to what they do. In fact, “ that can be off-putting to people from other fields.” In some situations, terms are familiar but mean something completely different, e.g., research in UX versus marketing research.</p>

<h4 id="2-pressure-to-constantly-reduce-the-time-for-research">2. Pressure To Constantly Reduce The Time For Research</h4>

<p>Another issue is that there is a constantly growing pressure to speed up the UX process and reduce the time spent on research. I cannot count the number of times when a project manager asked me to shorten a study even further by skipping the analysis stage or the kick-off sessions.</p>

<p>While previously you could spend weeks on research, a 5-day research cycle is increasingly becoming the norm. In fact, the book  describes how research can dwindle to just a day (from an overall 5-day cycle).</p>

<p>Considering this, there is a LOT of pressure on UX researchers to deliver fast, without compromising the quality of the study. <strong>The difficulty increases when there are multiple stakeholders</strong>, each with their own opinions, demands, views, assumptions, and priorities.</p>

<h3 id="the-fast-ux-approach">The Fast UX Approach</h3>

<p>Contrary to what you might think, reducing the time it takes to do UX research does not mean that you need to soldier on by yourself. I have done this and it only works in the short term. It does not matter how amazing the findings are &mdash; there is not enough PowerPoint slides in the world to convince a team of the urgency to take action if they have not been on the research journey themselves.</p>

<p>In the long term, the more actively engaged your team and stakeholders are in the research, the more empowered they will feel and the more willing they will be to take action. <strong>Productive collaboration also means that you can move together at a quicker pace</strong> and speed up the whole research process.</p>

<p>The FAST UX Research framework (see Fig. 2 below) is a tool to truly engage team members and stakeholders in a way that turns them into active advocates and champions of the research process. It shows non-researchers <strong>when and how</strong> they should get involved in UX Research.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7063afcb-c5aa-4f91-af94-e9213e37623f/fig2-fast-ux-research-process.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7063afcb-c5aa-4f91-af94-e9213e37623f/fig2-fast-ux-research-process.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7063afcb-c5aa-4f91-af94-e9213e37623f/fig2-fast-ux-research-process.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7063afcb-c5aa-4f91-af94-e9213e37623f/fig2-fast-ux-research-process.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7063afcb-c5aa-4f91-af94-e9213e37623f/fig2-fast-ux-research-process.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7063afcb-c5aa-4f91-af94-e9213e37623f/fig2-fast-ux-research-process.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7063afcb-c5aa-4f91-af94-e9213e37623f/fig2-fast-ux-research-process.jpg"
			sizes="100vw"
			alt="The FAST UX Research approach; FAST UX Research methodology."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Fig. 2. The FAST User Experience Research framework
		</figcaption>
	
</figure>


<p>In essence, stakeholders take ownership of each of the UX research stages by carrying out the four activities, each corresponding to its research stage.</p>

<p>Working together reduces the time it takes for UX Research. The true benefit of the approach, however, is that, in the long term, it takes less and less time for the business to take action based on research findings as people become true advocates of user-centricity and the research process.</p>

<p><strong>This approach can be applied to any qualitative research method and with any team</strong>. For example, you can carry out FAST usability testing, FAST interviews, FAST ethnography, and so on. In order to be effective, you will need to explain this approach to your stakeholders from the start. Talk them through the framework, explaining each stage. Emphasize that this is what EVERYONE does, that it’s their work as much as the UX researcher’s job, and that it’s only successful if everyone is involved throughout the process.</p>

<h3 id="stage-1-focus-define-a-common-goal">Stage 1: Focus (Define A Common Goal)</h3>

<p>There is a uniform consensus within UX that a research project should start by : why is this research done and how will the results be acted upon?</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bb2c9555-294f-4c1e-b35c-b96c0639eecc/fig3-focus-in-fast.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bb2c9555-294f-4c1e-b35c-b96c0639eecc/fig3-focus-in-fast.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bb2c9555-294f-4c1e-b35c-b96c0639eecc/fig3-focus-in-fast.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bb2c9555-294f-4c1e-b35c-b96c0639eecc/fig3-focus-in-fast.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bb2c9555-294f-4c1e-b35c-b96c0639eecc/fig3-focus-in-fast.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bb2c9555-294f-4c1e-b35c-b96c0639eecc/fig3-focus-in-fast.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bb2c9555-294f-4c1e-b35c-b96c0639eecc/fig3-focus-in-fast.jpg"
			sizes="100vw"
			alt="Focus in FAST UX Research; first stage in the FAST UX Research process."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Fig. 3. Focus is about defining clear objectives and goals for the research and it’s ultimately the team’s and all stakeholders’ shared responsibility to do this.
		</figcaption>
	
</figure>


<p>Generally, this is expressed within the research goals, objectives, research questions and/or hypotheses. Most projects start with a kick-off meeting where those are either discussed (based on an available brief) or are defined during the meeting.</p>

<p>The most regular problem with kick-off sessions like these is that stakeholders come up with too many things they want to learn from a study. The way to turn the situation around is to <strong>assign a specific task to your immediate team</strong> (other UX professionals you work with) and stakeholders (key decision makers): they will help focus the study from the beginning.</p>

<p>The way they will do that is by working together through the following steps:</p>

<ol>
<li><strong>Identify as a group the current challenges and problems</strong>.<br />
Ask someone to take notes on a shared document; alternatively, ask everyone to participate and write on sticky notes which are then displayed on a “project wall” for everyone to see.</li>
<li><strong>Identify the potential objectives and questions for a research study</strong>.<br />
Do this the same way you did the previous step. You don’t need to commit to anything yet.</li>
<li><strong>Prioritize</strong>.<br />
Ask the team to order the objectives and questions, starting with the most important ones.<br /></li>
<li><strong>Reword and rephrase</strong>.<br />
Look at the top 3 questions and objectives. Are they too broad or narrow? Could they be reworded so it’s clearer what is the focus of the study? Are they feasible? Do you need to split or merge objectives and questions?</li>
<li><strong>Commit to be flexible</strong>.<br />
Agree on the top 1-2 objectives and ensure that you have agreement from everyone that this is what you will focus on.<br /></li>
</ol>

<p>Here are some questions you can ask to help your stakeholders and team to get to the focus of the study faster:</p>

<ul>
<li>From the objectives we have recognized, what is most important?</li>
<li>What does success look like?</li>
<li>If we only learn one thing, which one would be the most important one?</li>
</ul>

<p>Your role during the process is to provide expertise to determine if:</p>

<ul>
<li>The identified objectives and questions are feasible for a single study;</li>
<li>Help with the wording of objectives and questions;</li>
<li>Design the study (including selecting a methodology) after the focus has been identified.</li>
</ul>

<p>At first sight, the <em>Focus</em> and <em>Attend</em> (next stages) activities might be familiar as you are already carrying out a kick-off meeting and inviting stakeholders to attend research sessions.</p>

<p>However, adopting a FAST approach means that your stakeholders have as much ownership as you do during the research process because work is shared and co-owned.  Reiterate that the process is collaborative and at the end of the session, emphasize that <strong>agreeing on clear research objectives is not easy</strong>. Remind everybody that having a shared focus is already better than what many teams start with.</p>

<p>Finally, remind the team and your stakeholders what they need to do during the rest of the process.</p>




  <aside class="product-panel product-panel__tilted product-panel--book" data-audience="non-subscriber" data-remove="true">
    <div class="container product-panel--book__container">
      <div class="panel__description panel__description--book">
        <p>
          Is your pattern library up to date today? <em>Alla Kholmatova</em> has just finished a fully fledged book on <strong>Design Systems</strong> and how to get them right. With common traps, gotchas and the lessons she learned. Hardcover, eBook. <em>Just sayin'.</em>
        </p>
        <a href="https://www.smashingmagazine.com/printed-books/design-systems/">
          <button class="btn btn--green btn--large">
            Table of Contents&nbsp;&rarr;
          </button>
        </a>
      </div>
      <div class="panel__image panel__image--book">
        <a href="https://www.smashingmagazine.com/printed-books/design-systems/" class="books__book__image">
        <div class="books__book__img">
          <img src="https://www.smashingmagazine.com/images/books/design-systems--large-opt.png">
        </div>
      </a>
      </div>
    </div>
  </aside>




<h3 id="stage-2-attend-immerse-the-team-deeply-in-the-research-process">Stage 2: Attend (Immerse The Team Deeply In The Research Process)</h3>

<p>Seeing first hand the experience of someone using a product or service is so rich that there is  to engage the team.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9c79d889-959b-4fee-b2c3-42ad764b3f0e/fig4-attend-in-fast.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9c79d889-959b-4fee-b2c3-42ad764b3f0e/fig4-attend-in-fast.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9c79d889-959b-4fee-b2c3-42ad764b3f0e/fig4-attend-in-fast.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9c79d889-959b-4fee-b2c3-42ad764b3f0e/fig4-attend-in-fast.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9c79d889-959b-4fee-b2c3-42ad764b3f0e/fig4-attend-in-fast.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9c79d889-959b-4fee-b2c3-42ad764b3f0e/fig4-attend-in-fast.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9c79d889-959b-4fee-b2c3-42ad764b3f0e/fig4-attend-in-fast.jpg"
			sizes="100vw"
			alt="Attend in FAST UX Research; second stage in FAST UX Research."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Fig. 4. Attend in FAST UX Research is about encouraging the team and stakeholders to be present at all research sessions, but also to be actively engaged with the research.
		</figcaption>
	
</figure>


<p>What often happens is that observers join in on the day of the research study and then they spend the time plastered to their laptops and mobile phones. What is worse, some stakeholders often talk to the note-taker and distract the rest of the design team who need to observe the sessions.</p>

<p>This is why it is just as important that you <strong>get the team to interact with the research</strong>. The following activities allow the team to immerse themselves in the research session. You can ask stakeholders to:</p>

<ul>
<li>Ask questions during the session through a dedicated live chat (e.g. Slack, Google Hangouts, Skype);</li>
<li>Take notes on sticky notes;</li>
<li>Summarize observations for everyone (see next stage).</li>
</ul>

<p>Assign one person per session for each of these activities. Have one “live chat manager,” one “note-taker,” and one “observer” who will sum up the session afterwards.</p>

<p>Rotate people for the next session.</p>

<p>Before the session, it’s useful to walk observers through the ‘ground rules’ very briefly. You can have a poster similar to the one  that will help you do this and remind the team of their role during the study (see Fig. 3 above).</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ba8af57b-ccb5-4356-85df-bb732385a211/fig5-observation-poster.jpeg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ba8af57b-ccb5-4356-85df-bb732385a211/fig5-observation-poster.jpeg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ba8af57b-ccb5-4356-85df-bb732385a211/fig5-observation-poster.jpeg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ba8af57b-ccb5-4356-85df-bb732385a211/fig5-observation-poster.jpeg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ba8af57b-ccb5-4356-85df-bb732385a211/fig5-observation-poster.jpeg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ba8af57b-ccb5-4356-85df-bb732385a211/fig5-observation-poster.jpeg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ba8af57b-ccb5-4356-85df-bb732385a211/fig5-observation-poster.jpeg"
			sizes="100vw"
			alt="An observation poster; user research poster."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Fig. 5. A poster can be hanged in the observation room and used to remind the team and stakeholders what their responsibilities are and the ground rules during observation.
		</figcaption>
	
</figure>


<p> to an observation room.</p>

<h3 id="stage-3-summarize-analysis-for-non-researchers">Stage 3: Summarize (Analysis For Non-Researchers)</h3>

<p>I am a strong supporter of the idea that <strong>analysis starts the moment fieldwork begins</strong>. During the very first research session, you start looking for patterns and interpretation of what the data you have means.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d8b315ca-e99a-42f6-bf08-ded098979b52/fig6-summarize-in-fast.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d8b315ca-e99a-42f6-bf08-ded098979b52/fig6-summarize-in-fast.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d8b315ca-e99a-42f6-bf08-ded098979b52/fig6-summarize-in-fast.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d8b315ca-e99a-42f6-bf08-ded098979b52/fig6-summarize-in-fast.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d8b315ca-e99a-42f6-bf08-ded098979b52/fig6-summarize-in-fast.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d8b315ca-e99a-42f6-bf08-ded098979b52/fig6-summarize-in-fast.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d8b315ca-e99a-42f6-bf08-ded098979b52/fig6-summarize-in-fast.jpg"
			sizes="100vw"
			alt="Summarize in FAST UX Research; the third stage in FAST UX Research."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Fig. 6. Summarize in FAST UX Research is about asking the team and your stakeholders to tell you about what they thought were the most interesting aspects of user research.
		</figcaption>
	
</figure>


<p>Even after the first session (but typically towards the end of fieldwork) you can carry out collaborative analysis:  in one of the most important stages of research.</p>

<p>The collaborative analysis session is an activity where you provide an opportunity for everyone to be heard and create a shared understanding of the research.</p>

<p>Since you&rsquo;re including other experts’ perspectives, you’re increasing the chances to <strong>identify more objective and relevant insights</strong>, and also <strong>for stakeholders to act upon the results of the study</strong>.</p>

<p>Even though ‘analysis’ is an essential part of any research project, a lot of stakeholders get scared by the word. The activity sounds very academic and complex. This is why at the end of each research session, research day, or the study as a whole, the role of your stakeholders and immediate team is to <em>summarize</em> their observations. Summarizing may sound superfluous but is an important part of the analysis stage; this is essentially what we do during “” sessions.</p>

<p>Listening to someone’s summary provides you with an opportunity to understand:</p>

<ul>
<li>What they paid attention to;</li>
<li>What is important for them;</li>
<li>Their interpretation of the event.</li>
</ul>

<h4 id="summary-at-the-end-of-each-session">Summary At The End Of Each Session</h4>

<p>You do this by reminding everyone at the beginning of the session that at the end you will enter the room and ask them to summarize their observations and recommendations.</p>

<p>You then end the session by asking each stakeholder the following:</p>

<ul>
    <li>What were their key observations (see also Fig. 3)?</li>
    <ul>
        <li>What happened during the session?</li>
        <li>Were there any major difficulties for the participant?</li>
        <li>What were the things that worked well?</li>
    </ul>
<li>Was there anything that surprised them?</li>
</ul>

<p>This will make the team more attentive during the session, as they know that they will need to sum it up at the end. It will also help them to internalize the observations (and later, transition more easily to findings).</p>

<p>This is also the time to <strong>consistently share with your team what you think stands out</strong> from the study so far. Avoid the temptation to do a ‘’ at the end. It’s better if outcomes are told to stakeholders many times.</p>

<p>On multiple occasions, research has given me great outcomes. Instead of sharing them regularly, I keep them to myself until the final report. It doesn’t work well. A big reveal at the end leads to bewildered stakeholders who often cannot jump from observations to insights as quickly. As a result, there is either stubborn pushback or indifferent shrugs.</p>

<h4 id="summary-at-the-end-of-the-day">Summary At The End Of The Day</h4>


  <div id="sponsors-article" data-impression="true" class="c-promo-box c-promo-box--ad sponsors hidden" data-audience="non-subscriber" data-remove="true"></div>



<p>A summary of the event or the day can then naturally transition into a collaborative analysis session. Your job is to moderate the session.</p>

<p>The job of your stakeholders is to summarize the events of the day and the final results. Ask a volunteer to talk the group through what happened during the day. Other stakeholders can then add to these observations.</p>

<h4 id="summary-at-the-end-of-the-study">Summary At The End Of The Study</h4>

<p>After the analysis is done, ask one or two stakeholders to summarize the study. Make sure they cover why we did research, what happened during the study and what are the primary findings.  They can also do this by walking through the project wall (if you have one).</p>

<p>It’s very difficult <em>not</em> to talk about your research and leave someone else to do it. But it’s worth it. No matter how much you’re itching to do this yourself &mdash; don’t! It’s a great opportunity for people to internalize research and become comfortable with the process. This is one of the key moments to turn stakeholders into active advocates of user research.</p>

<p>At the end of this stage, you should have 5-7 findings that capture the study.</p>

<h3 id="stage-4-translate-make-stakeholders-active-champions-of-the-solution">Stage 4: Translate (Make Stakeholders Active Champions Of The Solution)</h3>

<blockquote>“Research doesn’t have a value unless it results in decisions and actions.”<br /><br />&mdash;Lang and Howell (2017).</blockquote>

<p>Even when you agree with the findings, stakeholders might still disagree about what the research means or lack commitment to take further action. This is why after summarizing, ask your stakeholders to work with you and identify the “Now what?” or what it all means for the organization, product, service, team and/or individually for each one of them.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f542777a-a4bb-4673-afaa-05b3ca2bc656/fig7-translate-in-fast.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f542777a-a4bb-4673-afaa-05b3ca2bc656/fig7-translate-in-fast.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f542777a-a4bb-4673-afaa-05b3ca2bc656/fig7-translate-in-fast.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f542777a-a4bb-4673-afaa-05b3ca2bc656/fig7-translate-in-fast.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f542777a-a4bb-4673-afaa-05b3ca2bc656/fig7-translate-in-fast.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f542777a-a4bb-4673-afaa-05b3ca2bc656/fig7-translate-in-fast.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f542777a-a4bb-4673-afaa-05b3ca2bc656/fig7-translate-in-fast.jpg"
			sizes="100vw"
			alt="Translate in FAST UX Research; the fourth stage in FAST UX Research."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Fig. 7. Translate in FAST UX Research is about asking the team or individual stakeholders to discuss each of the findings and articulate how it will impact the business, the service, and product or their work.
		</figcaption>
	
</figure>


<p>Traditionally,  to write clear, precise, descriptive findings, and actionable recommendations. However, if the team and stakeholders are not part of identifying actionable recommendations, they might be resistant towards change in future.</p>

<p>To prevent later pushback, ask stakeholders to identify the “” (also referred to as ‘actionable recommendations’). Together, you’ll be able to identify how the insights and findings will:</p>

<ul>
<li>Affect the business and what needs to be done now;</li>
<li>Affect the product/service and what changes do we need to make;</li>
<li>Affect people individually and the actions they need to take;</li>
<li>Lead to potential problems and challenges and their solutions;</li>
<li>Help solve problems or identify potential solutions.</li>
</ul>

<p>Stakeholders and the team can translate the findings at the end of a collaborative analysis session.</p>

<p>If you decide to separate the activities and conduct a meeting in which the only focus is on actionable recommendations, then consider the following format:</p>

<ol>
<li>Briefly talk through the 5-7 main findings from the study (as a refresher if this stage is done separately from the analysis session or with other stakeholders).</li>
<li>Split the group into teams and ask them to work on one finding/problem at a time.</li>
<li>Ask them to list as many ways they see the finding affecting them.</li>
<li>Ask one person from each group to present the findings back to the team.</li>
<li>Ask one/two final stakeholders to summarize the whole study, together with the methods, findings, and recommendations.</li>
</ol>

<p>Later, you can have multiple similar workshops; this is how you get to engage different departments from the organization.</p>

<h3 id="fast-ux-in-practice">Fast UX In Practice</h3>

<p>An excellent example of a FAST UX Research approach in practice is a project I was hired to carry out for a central UK government department. The ultimate goal of the project was to identify user requirements for a very complex internal system.</p>

<p>At first sight, this was a very challenging project because:</p>

<ul>
<li><strong>There was no time to get to know the department or the client</strong>.<br />
Usually, I would have at least a week or two to get to know the client, their needs, opinions, internal pressures, and challenges. For this project, I had to start work on Monday with a team I had never met; in a building I had never worked, in a domain I knew little about, and finish on Friday the same week.</li>
<li><strong>The system was very complex and required intense research</strong>.<br />
The internal system and the nature of work were very complex; this required gathering data with at least a few research methods (for triangulation).</li>
<li><strong>This was the first time the team had worked with a UX Researcher</strong>.<br />
The stakeholders were primarily IT specialists. However, I was lucky that they were very keen and enthusiastic to be involved in the project and get their hands dirty.</li>
<li><strong>Stakeholder availability</strong>.<br />
As is the case on many other projects, all stakeholders were extremely busy as they had their own work on top of the project. Nonetheless, we made it work, even if it meant meeting over lunch, or for a 15-minute wrap up before we went home.</li>
<li><strong>There were internal pressures and challenges</strong>.<br />
As with any department and huge organization, there were a number of internal pressures and challenges. Some of them I expected (e.g. legacy systems, slow pace of change) but some I had no clue about when I started.</li>
<li><strong>We had to coordinate work with external teams</strong>.<br />
An additional challenge was the need to work with and coordinate efforts with external teams at another UK department.</li>
</ul>

<p>Despite all of these challenges, this was one of the most enjoyable projects I have worked on because of the tight collaboration initiated by the FAST approach.</p>

<p>The project consisted of:</p>

<ul>
<li>1 day of kick-off sessions and getting to know the team</li>
<li>2,5 days of contextual inquiries and shadowing of internal team members,</li>
<li>Half a day for a co-creation workshop, and</li>
<li>1 day for analysis and results reporting.</li>
</ul>

<p>In the process, I gathered data from 20+ employees, had 16+ hours of observations, 300+ photos and about 100 pages of notes. Here is a great example of cramming in 3 weeks’ worth of work into a mere 5-day research cycle. More importantly, people in the department were really excited about the process.</p>

<p>Here is how we did it using a FAST UX Research approach:</p>

<ul>
    <li><strong>Focus</strong><br />At the beginning of the project, the two key stakeholders identified what the focus of research would be while my role was mainly to help with prioritizing the objectives, tweak the research questions and check for feasibility. In this sense, I listened and mainly asked questions, interjecting occasionally with examples from previous projects or options that helped to adjust our approach.<br /><br />While I wrote the main discussion guide for the contextual inquiries and shadowing sessions, we sat together with the primary team to discuss and design the co-creation workshop with internal users of the system.</li>
    <li><strong>Attend</strong><br />During the workshop one of the stakeholders moderated half of the session, while the other took notes and observed closely the participants. It was a huge success internally, as stakeholders felt there was better visibility for their efforts to modernize the department, while employees felt listened to and involved in the research.</li>
    <li><strong>Summarize</strong><br />Immediately after the workshop, we sat together with the stakeholders for a 30-minute meeting where I had them summarize their observations.<br /><br />As a result of the shadowing, contextual inquiries and co-creation workshop, we were able to identify 60+ issues and problems with the internal system (with regards to integration, functionality, and usability), all captured in six high-level findings. </li>
    <li><strong>Translate</strong><br />Later, we discussed with the team how each of the six major findings translated to a change or implication for the department, the internal system, as well as collaboration with other departments.</li>
</ul>

<p>We were so perfectly aligned with the team that when we had to talk about our work in front of another UK government department, I could let the stakeholders talk about the process and our progress.</p>

<p>My final task (over two additional days) was to document all of the findings in a research report. This was necessary as a knowledge repository because I had to move onto other projects.</p>

<p>With a more traditional approach, the project could have easily spanned 3 weeks. More importantly, <strong>quickly understanding individual and team pressures and challenges were the keys to the success</strong> of the new system. This could not have happened within the allocated time without a collaborative approach.</p>

<p>A FAST UX approach resulted in tight collaboration, strong co-ownership and a shared sense of progress; all of those allowed to shorten the time of the project, but also to instill a feeling of excitement about the UX research process.</p>

<h3 id="have-you-tried-it-out-already">Have You Tried It Out Already?</h3>

<p>While UX research becomes ever more popular, gone are the days when we could soldier on by ourselves and only consult stakeholders at the end.</p>

<p>Mastering our craft as UX researchers means engaging others within the process and being articulate, clear, and transparent about our work. The FAST approach is a simple model that shows how to engage non-researchers with the research process. Reducing the time it takes to do research, both in the short (i.e. the study itself) and long term (i.e. using the research results), is a strategic advantage for the researcher, team, and the business as a whole.</p>

<p>Would you like to improve your efficiency and turn stakeholders into user research advocates? Go and try it out. You can then share your stories and advice here.</p>

<p>I would love to hear your comments, suggestion and any feedback you care to share! If you have tried it out already, do you have success stories you want to share? Be as open as you can &mdash; what worked well, and what didn’t? As with all other things UX, it’s most fun if we learn together as a team.</p>




<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(cc, ra, il)</span>
</div>



  <div id="sponsors-article-end" data-impression="true" class="c-promo-box c-promo-box--ad c-promo-box--wide sponsors hidden" data-audience="non-subscriber" data-remove="true"></div>



</div>



              </article>
            </body>
          </html>
---------------
<h1 id="#title_10" >11、Oracle发布多语种虚拟机平台GraalVM 1.0</h1>
Ben Evans
[http://www.infoq.com/cn/news/2018/05/oracle-graalvm-v1?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/05/oracle-graalvm-v1?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Oracle发布了多语种虚拟机平台GraalVM的1.0版本。初始发布版包括运行Java和JVM语言（通过字节码）的能力，对JavaScript和Node.JS的全面支持，以及对Ruby、Python和R语言的测试性支持。</p> <i>By Ben Evans</i> <i> Translated by 金灵杰</i>
---------------
<h1 id="#title_11" >12、VueConf.US大会第二天会议内容概述</h1>
Kevin Ball
[http://www.infoq.com/cn/news/2018/05/sessions-from-day-2-vueconf-us?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/05/sessions-from-day-2-vueconf-us?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>第一届VueConf.US大会于3月26日到28日在新奥尔良市举行，VueJS核心团队和来自世界各地的数百名Vue开发者齐聚一堂。28日的会议包括高级Vue模型、使用Vue设计系统、TypeScript与Vue搭配使用、Vue与React比较、使用Vue进行服务器端渲染、Vue Storybook以及使用Vue单文件组件的快速原型。</p> <i>By Kevin Ball</i> <i> Translated by 谢丽</i>
---------------