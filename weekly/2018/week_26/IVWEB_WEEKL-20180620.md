## 文章索引
1、 <a href="#1fex-技术周刊---2018/06/19" >FEX 技术周刊 - 2018/06/19</a><br/>
2、 <a href="#2how-to-speed-up-the-wireframing-process-with-photoshop-and-adobe-xd" >How To Speed Up The Wireframing Process With Photoshop And Adobe XD</a><br/>
3、 <a href="#3文章-如何解决区块链的硬伤对时间的感知" >文章： 如何解决区块链的硬伤：对时间的感知</a><br/>
4、 <a href="#4文章-针对aspnet-core-web-api的先进架构" >文章： 针对ASP.NET Core Web API的先进架构</a><br/>
5、 <a href="#5文章-以太坊dapp入门实战一" >文章： 以太坊Dapp入门实战(一)</a><br/>
6、 <a href="#6aspnet-core-21带来signalrrazor类库" >ASP.NET Core 2.1带来SignalR、Razor类库</a><br/>
7、 <a href="#7全新的图形数据库云服务amazon-neptune正式发布" >全新的图形数据库云服务Amazon Neptune正式发布</a><br/>
8、 <a href="#8facebook-sonar一款可视化及交互式移动应用调试工具" >Facebook Sonar：一款可视化及交互式移动应用调试工具</a><br/>
9、 <a href="#9谷歌发布android-p-beta-2" >谷歌发布Android P Beta 2</a><br/><h1 id="#title_0" >1、FEX 技术周刊 - 2018/06/19</h1>

[http://fex.baidu.com/blog/2018/06/fex-weekly-19//](http://fex.baidu.com/blog/2018/06/fex-weekly-19//)
作者：Dafrok <br> <p>微信搜索『FEX』关注我们的公众号，及时获得最新资讯。</p>

<h2 id="section">深阅读</h2>

<p><strong>Concurrent marking in V8</strong><br />
https://v8project.blogspot.com/2018/06/concurrent-marking.html<br />
This post describes the garbage collection technique called concurrent marking. The optimization allows a JavaScript application to continue execution while the garbage collector scans the heap to find and mark live objects. Our benchmarks show that concurrent marking reduces the time spent marking on the main thread by 60%–70%. Concurrent marking is the last puzzle piece of the Orinoco project — the project to incrementally replace the old garbage collector with the new mostly concurrent and parallel garbage collector. Concurrent marking is enabled by default in Chrome 64 and Node.js v10.<br />
另附：</p>

<p><strong>Jsonnet - The Data Templating Language</strong><br />
https://jsonnet.org/<br />
A data templating language for app and tool developers: Generate config data; Side-effect free; Organize, simplify, unify; Manage sprawling config.</p>

<p><strong>State of React Native 2018</strong><br />
https://facebook.github.io/react-native/blog/2018/06/14/state-of-react-native-2018<br />
Alongside the community inside Facebook, we’re happy to have a thriving population of React Native users and collaborators outside Facebook. We’d like to support the React Native community more, both by serving React Native users better and by making the project easier to contribute to. Just as our architecture changes will help React Native interoperate more cleanly with other native infrastructure, React Native should be slimmer on the JavaScript side to fit better with the JavaScript ecosystem, which includes making the VM and bundler swappable.<br />
另附：、</p>

<p><strong>Introducing the GraphQL Guide</strong><br />
https://blog.graphql.guide/introducing-the-graphql-guide-11a5ae48628a<br />
jQuery 作者新书。The Guide shows you why GraphQL APIs are the true successor to REST APIs. We’ll be looking at the core fundamentals of GraphQL along with strategies for how to implement it (client-side with Apollo and server-side in Node.js). Additionally, we’ll be exploring different situations in which GraphQL can be used (on mobile with React Native or Java/Swift, and on the web with either React or Vue).<br />
另附：</p>

<p><strong>From Node.js to Go: There, and back again</strong><br />
https://www.thenativeweb.io/blog/2018-06-12-15-47-from-node-to-go-there-and-back-again/<br />
A few years ago, we chose Go over Node.js for writing the wolkenkit CLI. A few months ago we rewrote everything from scratch, this time using Node.js again. We’ve learned that you can’t dance at two weddings.</p>

<p><strong>Building A Pub/Sub Service In-House Using Node.js And Redis</strong><br />
https://www.smashingmagazine.com/2018/06/pub-sub-service-in-house-node-js-redis/<br />
As the size of data for each message in our system differs from a few bytes to up to 100MB, we needed a scalable solution that could support a multitude of scenarios. In this article, Dhimil Gosalia explains why you should consider building an in-house Pub/Sub service, too.</p>

<p><strong>Eggjs 和 SOFA 的跨语言互调</strong><br />
https://zhuanlan.zhihu.com/p/38004479<br />
本文通过 Step by Step 的形式介绍了 Eggjs 和 SOFA（Java）是如何进行互联互通的，涵盖了 RPC 的服务发现、接口定义、本地代理生成、服务端实现等各方面，期望展现给你一个相对完整的 Nodejs RPC 解决方案。考虑到社区的接受度、多语言友好性等因素，接下来的示例采用 protobuf 作为 RPC 的序列化方式。</p>

<p><strong>结合源码分析 Node.js 模块加载与运行原理</strong><br />
http://efe.baidu.com/blog/nodejs-module-analyze/<br />
在 Node.js 中使用模块非常简单，我们日常开发中几乎都有过这样的经历：写一段 JavaScript 代码，require 一些想要的包，然后将代码产物 exports 导出。但是，对于 Node.js 模块化背后的加载与运行原理，我们是否清楚呢。首先抛出以下几个问题：Node.js 中的模块支持哪些文件类型？核心模块和第三方模块的加载运行流程有什么不同？除了 JavaScript 模块以外，怎样去写一个 C/C++ 扩展模块？本篇文章，就会结合 Node.js 源码，探究一下以上这些问题背后的答案。</p>

<p><strong>是时候好好安利下LuLu UI框架了</strong><br />
https://l-ui.com/<br />
LuLu UI是阅文前端荣誉出品的UI框架，基于jQuery，针对PC网站，兼容IE8+，包含20+静态或动态UI组件，非常适合面向外部用户的网站开发。其实 jQuery 如果有一个像 AntD 这么漂亮的 UI 库的话，应该还是有不少人会用的。
另附：</p>

<p><strong>如何提高代码的可读性</strong><br />
https://zhuanlan.zhihu.com/p/34982747<br />
编程语言的文本形式决定了它只能提高一个方面的信噪比而放弃其他方面的信噪比。但是文本不是唯一的信息获取方式。IDE 或者 PaaS 完全可以用各种不同的方式重组信息。</p>

<p><strong>The new (and old) CSS units you’ve never heard about</strong><br />
https://dev.to/maxart2501/the-new-and-old-css-units-youve-never-heard-about-1mn1<br />
Talking about CSS that you might - but more probably might not! - have heard, and even less used, about the units described in this article. And no, not like the “old” vw and vh (which I happen to still have to explain to those less proficient in CSS).</p>

<p><strong>Image Inconsistencies: How and When Browsers Download Images</strong><br />
https://csswizardry.com/2018/06/image-inconsistencies-how-and-when-browsers-download-images/<br />
Firefox and Safari seem to have the most preferred behaviour here: they won’t download background-images that they know they won’t need. Chrome, Opera, and Edge will all download background-images that are applied to invisible elements.</p>

<p><strong>The Trouble with D3</strong><br />
https://medium.com/dailyjs/the-trouble-with-d3-4a84f7de011f<br />
Recently there were a couple of threads on Twitter discussing the difficulties associated with learning d3.js. I’ve also seen this come up in many similar conversations I’ve had at meetups, conferences, workshops, mailing list threads and slack chats. While I agree that many of the difficulties are real, the threads highlight a common misconception that needs to be cleared up if we want to help people getting into data visualization.</p>

<p><strong>Your Brain on Front-End Development</strong><br />
https://css-tricks.com/your-brain-on-front-end-development/<br />
Part of the job of being a front-end developer is applying different techniques and technologies to pull off the desired UI and UX. Perhaps you work with a design team and implement their designs. I know when I look at a design (heck, even if I know I’m not going to be building it), my front-end brain starts triggering all sorts of things I know will be related to the task. Let’s take a look at what I mean.</p>

<p><strong>Reverse Engineering Instruments’ File Format</strong><br />
http://jamie-wong.com/post/reverse-engineering-instruments-file-format/<br />
At Figma, I work in a C++ codebase that cross-compiles to asm.js and WebAssembly to run in the browser. Occasionally, however, it’s helpful to be able to profile the native build we use for development and debugging. The tool of choice to do that on OS X is Instruments. If we can extract the right information from the files Instruments outputs, then we can construct flamecharts to help us build intuition for what’s happening while our code is executing.</p>

<p><strong>How Developers Power eBay’s Product-Based Shopping Experience</strong><br />
https://www.ebayinc.com/stories/blogs/tech/powering-ebays-product-based-shopping-experience/<br />
As eBay evolves and adapts to stay ahead of commerce trends and user preferences, eBay’s public API portfolio continues to expand and improve to enable third-party developers the means to easily integrate with eBay and to create innovative and valuable experiences for their customers and ours.</p>

<p><strong>Open-sourcing Sonar, a new extensible debugging tool</strong><br />
https://code.facebook.com/posts/1461914677288302/open-sourcing-sonar-a-new-extensible-debugging-tool/<br />
Sonar has enabled Facebook engineers to more easily inspect the behavior of our applications. It has been used in many projects, but sample use cases include: Providing our engineers with access to a view hierarchy that more accurately resembles the features and functionality they are working with, by showing Litho and ComponentKit components; Surfacing a stream of GraphQL requests, as opposed to raw network events; Tracking performance markers in real time, allowing developers to more easily investigate performance problems.<br />
另附：</p>

<p><strong>Metacat: Making Big Data Discoverable and Meaningful at Netflix</strong><br />
https://medium.com/netflix-techblog/metacat-making-big-data-discoverable-and-meaningful-at-netflix-56fb36a53520<br />
At Netflix, our data warehouse consists of a large number of data sets stored in Amazon S3 (via Hive), Druid, Elasticsearch, Redshift, Snowflake and MySql. Our platform supports Spark, Presto, Pig, and Hive for consuming, processing and producing data sets. Given the diverse set of data sources, and to make sure our data platform can interoperate across these data sets as one “single” data warehouse, we built Metacat. In this blog, we will discuss our motivations in building Metacat, a metadata service to make data easy to discover, process and manage.</p>

<p><strong>Twitter meets TensorFlow</strong><br />
https://blog.twitter.com/engineering/en_us/topics/insights/2018/twittertensorflow.html<br />
In this blog post, we will discuss the history, evolution, and future of our modeling/testing/serving framework, internally referred to as Deepbird, applying ML to Twitter data, and the challenges of serving ML in production settings. Indeed, Twitter handles large amounts of data and custom data formats. Twitter has a specific infrastructure stack, latency constraints, and a large request volume.</p>

<p><strong>Open Source Database HA Resources From Severalnines</strong><br />
http://highscalability.com/blog/2018/6/8/open-source-database-ha-resources-from-severalnines.html<br />
Severalnines has spent the last several years writing blogs and crafting content to help make your open source database solutions highly available. We are fans of highscalability.com and wanted to post some links to our top resources to help readers learn more how to make MySQL, MongoDB, MariaDB, Percona and PostgreSQL databases scalable.</p>

<h2 id="section-1">新鲜货</h2>

<p><strong>React &amp; VUE Star 过 10W</strong><br />
https://seven.ooo/hubble-congrats-react-and-vue-100k-stars/#Hubble<br />
.</p>

<p><strong>Office 365 Is Being Rewritten with JS and React</strong><br />
https://twitter.com/TheLarkInn/status/1006746626617008128</p>

<p><strong>GitHub Release Radar · May 2018</strong><br />
https://blog.github.com/2018-06-12-release-radar-may-2018/<br />
You may have noticed there were a lot of great open source releases this past month. Here are a few of our favorites.</p>

<p><strong>Meet the GitLab Web IDE</strong><br />
https://about.gitlab.com/2018/06/15/introducing-gitlab-s-integrated-development-environment/<br />
Here’s how we went from a proof of concept to a new feature that makes it even easier for everyone to edit inside of GitLab.</p>

<p><strong>Parcel v1.9.0 — Tree Shaking, 2x faster watcher, and more</strong><br />
https://medium.com/@devongovett/parcel-v1-9-0-tree-shaking-2x-faster-watcher-and-more-87f2e1a70f79<br />
The highlights of this release include: Tree Shaking for both ES6 and CommonJS modules — Parcel now removes unused code from your production bundles by completely compiling away the module system, reducing the file sizes and initialization times of bundles considerably; Up to 2x faster file watcher — Parcel’s file watcher now runs in a background worker for performance and stability. This speeds up compilation times during development by up to 2x! Resolved filenames are now cached…</p>

<p><strong>Now, you can deploy your Node.js app to App Engine standard environment</strong><br />
https://cloudplatform.googleblog.com/2018/06/Now-you-can-deploy-your-Node-js-app-to-App-Engine-standard-environment.html<br />
App Engine is ready and waiting to host your Node.js apps, with very minimal changes.<br />
另附：</p>

<p><strong>Open Source Serverless Frameworks on Docker EE</strong><br />
https://blog.docker.com/2018/06/open-source-serverless-frameworks-docker-ee/<br />
The maturation of container platforms such as Docker EE has made this process even easier, resulting in a number of competing frameworks in this space. We have identified at least 9 different frameworks*. In this study, we start with the following six: OpenFaaS, nuclio, Gestalt, Riff, Fn and OpenWhisk.</p>

<p><strong>Announcing winston@3.0.0!</strong><br />
https://godaddy.github.io/2018/06/12/announcing-winston-3/<br />
winston is the most popular logging solution for Node.js. In fact, when measured in public npm downloads winston is so popular that it has more usage than the top four comparable logging solutions combined.</p>

<p><strong>Record, replay, and stub HTTP interactions.</strong><br />
https://medium.com/dailyjs/the-trouble-with-d3-4a84f7de011f<br />
Polly.JS is a standalone, framework-agnostic JavaScript library that enables recording, replaying, and stubbing HTTP interactions. Polly taps into native browser APIs to mock requests and responses with little to no configuration while giving you the ability to take full control of each request with a simple, powerful, and intuitive API.</p>

<p><strong>React-Select</strong><br />
https://github.com/JedWatson/react-select<br />
A Select control built with and for React. Initially built for use in KeystoneJS.</p>

<p><strong>Math.js</strong><br />
http://mathjs.org<br />
Math.js is an extensive math library for JavaScript and Node.js. It features a flexible expression parser with support for symbolic computation, comes with a large set of built-in functions and constants, and offers an integrated solution to work with different data types like numbers, big numbers, complex numbers, fractions, units, and matrices. Powerful and easy to use.</p>

<p><strong>SVG Icons Library - Vivid.js</strong><br />
https://webkul.github.io/vivid/<br />
A JavaScript library which is built to easily customize and use the SVG Icons with a blaze.</p>

<p><strong>node-android</strong><br />
https://github.com/getICO/node-android<br />
Run Node.js on Android by rewrite Node.js in Java with the compatible API. 挺能折腾的。</p>

<p><strong>PulltoRefresh.js</strong><br />
https://www.boxfactura.com/pulltorefresh.js/<br />
A small, but powerful Javascript library crafted to power your webapp’s pull to refresh feature. No markup needed, highly customizable and dependency-free!</p>

<p><strong>style guide guide, gatsby edition</strong><br />
http://bradfrost.com/blog/post/style-guide-guide-gatsby-edition/<br />
Style Guide Guide is a boilerplate for creating a custom style guide for your organization’s design system. It provides just enough IA and hooks to get you going. As a bonus, I’ve provided links to helpful resources and inspiration to help you as you create your own custom style guide.</p>

<p><strong>Hoyjar - All-in-one Analytics &amp; Feedback</strong><br />
https://www.hotjar.com/<br />
Hotjar is a new and easy way to truly understand your web and mobile site visitors. Find your hottest opportunities for growth today.</p>

<p><strong>The 50 Best Free Datasets for Machine Learning</strong><br />
https://gengo.ai/articles/the-50-best-free-datasets-for-machine-learning/<br />
What are some open datasets for machine learning? We at Gengo decided to create the ultimate cheat sheet for high quality datasets. These range from the vast (looking at you, Kaggle) or the highly specific (data for self-driving cars).</p>

<p><strong>The Second Edition of “Refactoring”</strong><br />
https://martinfowler.com/articles/refactoring-2nd-ed.html#new-cover<br />
For the past two years, I’ve been working on a second edition of my book “Refactoring”. Here I have details about the new edition and some memos describing my thoughts in the last months of this project. The book is in production: we hope that it will be on the shelves early in the fall.</p>

<h2 id="section-2">设计</h2>

<p><strong>The Problem with Patterns</strong><br />
http://alistapart.com/article/problem-with-patterns<br />
A design pattern library can range from being thorough, trying to cover all the bases, to politely broad, so as to not step on the toes of a design team. But patterns should never sacrifice user context for efficiency and consistency. They should reinforce the importance of the design process while helping an organization think more broadly about its users’ needs and its own goals. Real-world problems rarely are solved with out-of-the-box solutions. Even in service design.</p>

<p><strong>Smashing Book 6 Excerpt - Bringing Personality Back To The Web</strong><br />
https://www.smashingmagazine.com/2018/06/bringing-personality-back-to-the-web/<br />
We’re pleased to announce that the brand new Smashing Book 6 is now available for pre-order. To give you a taste of what the book offers, here’s a sneak peek of a chapter written by Vitaly Friedman. Let’s explore a strategic guide for bringing back personality to the web, in regular real-life projects.<br />
另附：</p>

<p><strong>The new design tools on the block</strong><br />
https://uxdesign.cc/the-new-design-tools-on-the-block-1adcba8a293d<br />
While Sketch, Adobe XD, Figma and Invision Studio are all building the same product with slight differences in their focus areas and execution, some new cool kids just arrived to ease painful parts of our workflow.<br />
另附：</p>

<p><strong>Emotional Design for data heavy apps</strong><br />
https://blog.prototypr.io/emotional-design-to-make-people-fall-in-love-with-data-heavy-apps-fde2bd5db500<br />
It is boring to see the data/statistics in the form of plain graphs or tables or pie charts. But, to represent the data in a way that is more scannable and logical we have to use these forms or representations. Specially in an environment where the customers have to look at the data daily and repeatedly to track status of their audience it is tough to get rid of these representations. In such situation, how can we improve the user experience? From my experience and from inspiration looking at online trends in UX, I wanted share few tips to improve the UI for a possible better UX.</p>

<p><strong>How to Build an Effective Design Framework</strong><br />
https://www.toptal.com/designers/ui/design-framework<br />
Let’s outline the main issues a design framework solves, why you need one, and the components you will need to create when building one. You will find a free downloadable Sketch UI framework later in the article that allows you to create your own design framework.</p>

<h2 id="section-3">产品及其它</h2>

<p><strong>Blot</strong><br />
https://blot.im/<br />
Blot is a blogging platform with no interface. It creates a special folder in your Dropbox and publishes files you put inside. The point of all this — the reason Blot exists — is so you can use your favorite tools to create whatever you publish.</p>

<p><strong>Speak with Confidence</strong><br />
https://adamdrake.com/speak-with-confidence.html<br />
The good news is that speaking with confidence is a skill that can be learned. It requires practice, but there are a few things you can do in order to dramatically improve the confidence you project when speaking.</p>

<p><strong>游戏是不是洪水猛兽</strong><br />
https://mp.weixin.qq.com/s?__biz=MzA3MDMwOTcwMg==&amp;mid=2650005309&amp;idx=1&amp;sn=e47a34de9bd2420cbf2b2d054e8f2b42<br />
关于游戏的讨论又多了起来。有叫好的，也有叫骂的，还有扼腕叹息的。游戏究竟是不是洪水猛兽？这个问题值得探讨，答案没那么简单。<br />
另附：</p>

<p><strong>增长教科书Netflix：进取到让自己毛骨悚然</strong><br />
https://mp.weixin.qq.com/s?__biz=MzUyMDQ5NzI5Mg==&amp;mid=2247496448&amp;idx=1&amp;sn=40a37dd2df0fd66f39eb482a2a0eac73<br />
我们太沉迷于一种想法：不要成为下一个柯达或者美国在线，不要成为一家死守本业，而错过大趋势的公司。我们当时说，如果别人对此存有偏见，我们反而必须更加进取，我们必须进取到让自己毛骨悚然的程度。</p>

<p><strong>死于 25 岁，葬于 75 岁，这是改变上百万人的短片</strong><br />
https://mp.weixin.qq.com/s?__biz=MjM5NDg2NjA4MQ==&amp;mid=2650943601&amp;idx=1&amp;sn=87017e27b33db6d3a4d8009af0d8687c<br />
富兰克林这句名言是一剂猛药…你生来与众不同。现在你所拥有的思想,灵魂,精神是任何时刻、任何地点的其他人都不曾拥有的。每个人从零开始到成为一个领域的专家需要大约7年的时间。我们需要做的是秉持信念,期盼未来。许下你最真诚的梦想,一旦机会来临,就为之拼搏。上帝多次赋予我们梦想的天资,去点亮不曾确信的世界。如果你能活到88岁，在11岁之后，你将有11次机会成为某个领域的专家。<br />
另附：</p>

<p><strong>在美国模式之外，来见识下不甘平庸的「英伦式」科技创新</strong><br />
http://www.geekpark.net/news/230229<br />
如果硅谷为人们描绘出的未来图景是乐观至上、充满冒险意味，那么当我们来到「前沿之前」，就能发现英国创新者对于时间哲学的理解无形中渗透到了各个层面。无论是剑桥大学卡文迪许实验室、帝国理工大学哈姆林中心里正在攻克的课题方向，还是老牌跑车公司捷豹设计的一款新能源汽车，都在执着地平衡着前沿和人文、大胆创新和实际应用之间的关系。在这里，你几乎不会看到「风口」和「概念」，「能否解决实际问题，给人类带来更好的未来」是最重要的风向标。这也是几个世纪以来，英国推动技术社会进步的一贯思维体现。它看似少了锋芒，但如果我们必将要回答人类社会如何与技术共存的终极问题，这种典型的英式思考或许又是更先进和超前的，它值得被关注和重视。</p>
---------------
<h1 id="#title_1" >2、How To Speed Up The Wireframing Process With Photoshop And Adobe XD</h1>
Manuela Langella
[https://www.smashingmagazine.com/2018/06/wireframing-process-photoshop-xd/](https://www.smashingmagazine.com/2018/06/wireframing-process-photoshop-xd/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/06/wireframing-process-photoshop-xd/" />
              <title>How To Speed Up The Wireframing Process With Photoshop And Adobe XD</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>How To Speed Up The Wireframing Process With Photoshop And Adobe XD</h1>
                  
                    
                    <address>Manuela Langella</address>
                  
                  <time datetime="2018-06-19T15:45:38&#43;02:00" class="op-published">2018-06-19T15:45:38+02:00</time>
                  <time datetime="2018-06-19T14:36:53&#43;00:00" class="op-modified">2018-06-19T14:36:53+00:00</time>
                </header>
                

<p>Before starting any design project, there is one word that is sure follow you from the very beginning: <strong>wireframing</strong>. Today, we will learn how to create a wireframe in  and how to implement some graphics from Photoshop just by using libraries.</p>

<p>But first, what exactly is a wireframe?</p>

<p>A wireframe is a visual representation of your project’s structure. It defines the bones, the elements that will work in your layout, and the placement of the content for your prototype.</p>

<p>The great thing about wireframing is that it’s a combination of simple elements that make you concentrate on your project’s functionality. In this stage, you can draw without thinking too much about the style and design.</p>

<p>You just have to figure out what your project targets are and how to develop them through wireframing by using simple elements. As you move further through wireframing, you develop the best solutions as team component make comments and suggestions about your sketch.</p>

<p>The first step is to create a project and name it “sections”, then make a list of “elements” you need to complete the different steps, up to the creation of the final “architecture.”</p>

<p>Creating a wireframe “by hand” first makes a lot of sense. It helps you develop the entire idea on paper (without digital limits), and also lets your concepts flow easily. For those of you who work in a team, working with paper doesn’t seem the best approach if you want to share your notions with everyone involved in the project &mdash; especially if you work with your team online.</p>

<p>In this tutorial, we will cover the following steps:</p>

<ol>
<li>Create a wireframe, select, and insert PS assets through libraries;</li>
<li>Update PS files and see the results in Adobe XD.</li>
</ol>

<p>We will create a set of objects to use in our wireframe. We will put them aside in our assets as we had an extra panel from where we can take our tools.</p>

<p>Once you’ve done with it, you can save it and re-use for future projects, by using the same elements again and adding some more objects as well.</p>

<p>You will need these Photoshop elements I prepared to use in our wireframe.</p>

<p>Here’s what we will create:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/878e0c7b-4457-4f72-a346-ceef5358d36f/wireframing-process-photoshop-xd-image-0.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/878e0c7b-4457-4f72-a346-ceef5358d36f/wireframing-process-photoshop-xd-image-0.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/878e0c7b-4457-4f72-a346-ceef5358d36f/wireframing-process-photoshop-xd-image-0.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/878e0c7b-4457-4f72-a346-ceef5358d36f/wireframing-process-photoshop-xd-image-0.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/878e0c7b-4457-4f72-a346-ceef5358d36f/wireframing-process-photoshop-xd-image-0.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/878e0c7b-4457-4f72-a346-ceef5358d36f/wireframing-process-photoshop-xd-image-0.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/878e0c7b-4457-4f72-a346-ceef5358d36f/wireframing-process-photoshop-xd-image-0.jpg"
			sizes="100vw"
			alt="wireframe"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Wireframe (
		</figcaption>
	
</figure>












<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6f7dfb81-bdba-4f02-aa57-71dce9428e6c/wireframing-process-photoshop-xd-image-1.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6f7dfb81-bdba-4f02-aa57-71dce9428e6c/wireframing-process-photoshop-xd-image-1.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6f7dfb81-bdba-4f02-aa57-71dce9428e6c/wireframing-process-photoshop-xd-image-1.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6f7dfb81-bdba-4f02-aa57-71dce9428e6c/wireframing-process-photoshop-xd-image-1.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6f7dfb81-bdba-4f02-aa57-71dce9428e6c/wireframing-process-photoshop-xd-image-1.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6f7dfb81-bdba-4f02-aa57-71dce9428e6c/wireframing-process-photoshop-xd-image-1.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6f7dfb81-bdba-4f02-aa57-71dce9428e6c/wireframing-process-photoshop-xd-image-1.jpg"
			sizes="100vw"
			alt="complete layout"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Complete layout (
		</figcaption>
	
</figure>


<h4 id="1-create-a-wireframe-and-select-and-insert-ps-assets-through-libraries">1 . Create A Wireframe And Select And Insert PS Assets Through Libraries</h4>

<p>The best place to begin developing a wireframe from scratch is to draw it by hand first.</p>

<p>In this project, I want to create a landing page for an online course site. I know I need to communicate essential information in it. It doesn’t have to be perfect the first time out, but in the end, its effectiveness is very much dependent on how I organized the wireframe and how closely it aligns with the initial purpose.</p>

<p><strong>First Step</strong>: Here are my own hand-drawn wireframes.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/62cb6318-ad27-484a-8899-0c77039b29bb/wireframing-process-photoshop-xd-image-2.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/62cb6318-ad27-484a-8899-0c77039b29bb/wireframing-process-photoshop-xd-image-2.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/62cb6318-ad27-484a-8899-0c77039b29bb/wireframing-process-photoshop-xd-image-2.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/62cb6318-ad27-484a-8899-0c77039b29bb/wireframing-process-photoshop-xd-image-2.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/62cb6318-ad27-484a-8899-0c77039b29bb/wireframing-process-photoshop-xd-image-2.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/62cb6318-ad27-484a-8899-0c77039b29bb/wireframing-process-photoshop-xd-image-2.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/62cb6318-ad27-484a-8899-0c77039b29bb/wireframing-process-photoshop-xd-image-2.jpg"
			sizes="100vw"
			alt="wireframe"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>












<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ec9d3f8a-183b-4a92-872f-ecdd443fe600/wireframing-process-photoshop-xd-image-3.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ec9d3f8a-183b-4a92-872f-ecdd443fe600/wireframing-process-photoshop-xd-image-3.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ec9d3f8a-183b-4a92-872f-ecdd443fe600/wireframing-process-photoshop-xd-image-3.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ec9d3f8a-183b-4a92-872f-ecdd443fe600/wireframing-process-photoshop-xd-image-3.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ec9d3f8a-183b-4a92-872f-ecdd443fe600/wireframing-process-photoshop-xd-image-3.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ec9d3f8a-183b-4a92-872f-ecdd443fe600/wireframing-process-photoshop-xd-image-3.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ec9d3f8a-183b-4a92-872f-ecdd443fe600/wireframing-process-photoshop-xd-image-3.jpg"
			sizes="100vw"
			alt="wireframe"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>As you can see, there is not much information on them. The first intention is just to show how the layout will be composed and which elements are to be considered. Clean and simple.</p>

<p><strong>Second Step</strong>: Re-submit the wireframe in a smaller size and with some margin notes which I use to explain the elements and their use:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a9349c1b-6916-4d6d-921f-4be9f7401b2e/wireframing-process-photoshop-xd-image-4.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a9349c1b-6916-4d6d-921f-4be9f7401b2e/wireframing-process-photoshop-xd-image-4.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a9349c1b-6916-4d6d-921f-4be9f7401b2e/wireframing-process-photoshop-xd-image-4.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a9349c1b-6916-4d6d-921f-4be9f7401b2e/wireframing-process-photoshop-xd-image-4.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a9349c1b-6916-4d6d-921f-4be9f7401b2e/wireframing-process-photoshop-xd-image-4.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a9349c1b-6916-4d6d-921f-4be9f7401b2e/wireframing-process-photoshop-xd-image-4.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a9349c1b-6916-4d6d-921f-4be9f7401b2e/wireframing-process-photoshop-xd-image-4.jpg"
			sizes="100vw"
			alt="explaining elements on wireframe"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p><strong>Third Step</strong>: Let’s begin to create our digital wireframe with Adobe XD.</p>

<p>Open Adobe XD and choose &ldquo;Web 1920&rdquo; from the open window.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1b8b7d72-cd56-43b4-a4db-b24ce4a82014/wireframing-process-photoshop-xd-image-5.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1b8b7d72-cd56-43b4-a4db-b24ce4a82014/wireframing-process-photoshop-xd-image-5.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1b8b7d72-cd56-43b4-a4db-b24ce4a82014/wireframing-process-photoshop-xd-image-5.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1b8b7d72-cd56-43b4-a4db-b24ce4a82014/wireframing-process-photoshop-xd-image-5.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1b8b7d72-cd56-43b4-a4db-b24ce4a82014/wireframing-process-photoshop-xd-image-5.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1b8b7d72-cd56-43b4-a4db-b24ce4a82014/wireframing-process-photoshop-xd-image-5.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1b8b7d72-cd56-43b4-a4db-b24ce4a82014/wireframing-process-photoshop-xd-image-5.png"
			sizes="100vw"
			alt="chose web 1920 in adobe xd"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>Save your project as “Wireframe” by selecting <strong>File</strong>&nbsp;&rarr;&nbsp;<strong>Save as</strong>.</p>

<p>Once your file is saved, create another artboard for iPhone <sup>6</sup>&frasl;<sub>7</sub> Plus as well.</p>

<p>Click on the <kbd>A</kbd> (Artboard) button on the left side, and choose “iPhone 6/7/8” in the right sidebar.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d8262700-9b40-472a-8794-d05d33ab3075/wireframing-process-photoshop-xd-image-6.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d8262700-9b40-472a-8794-d05d33ab3075/wireframing-process-photoshop-xd-image-6.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d8262700-9b40-472a-8794-d05d33ab3075/wireframing-process-photoshop-xd-image-6.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d8262700-9b40-472a-8794-d05d33ab3075/wireframing-process-photoshop-xd-image-6.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d8262700-9b40-472a-8794-d05d33ab3075/wireframing-process-photoshop-xd-image-6.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d8262700-9b40-472a-8794-d05d33ab3075/wireframing-process-photoshop-xd-image-6.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d8262700-9b40-472a-8794-d05d33ab3075/wireframing-process-photoshop-xd-image-6.jpg"
			sizes="100vw"
			alt="creating artboard for iPhone formats"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>












<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/85699614-3eaa-44ce-8e7b-d35c98d67e68/wireframing-process-photoshop-xd-image-7.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/85699614-3eaa-44ce-8e7b-d35c98d67e68/wireframing-process-photoshop-xd-image-7.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/85699614-3eaa-44ce-8e7b-d35c98d67e68/wireframing-process-photoshop-xd-image-7.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/85699614-3eaa-44ce-8e7b-d35c98d67e68/wireframing-process-photoshop-xd-image-7.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/85699614-3eaa-44ce-8e7b-d35c98d67e68/wireframing-process-photoshop-xd-image-7.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/85699614-3eaa-44ce-8e7b-d35c98d67e68/wireframing-process-photoshop-xd-image-7.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/85699614-3eaa-44ce-8e7b-d35c98d67e68/wireframing-process-photoshop-xd-image-7.jpg"
			sizes="100vw"
			alt="creating artboard for iPhone formats"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>And here are our two artboards: one for desktop and one for mobile.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/80b2326f-899f-424a-bb4c-2db731dac9c0/wireframing-process-photoshop-xd-image-8.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/80b2326f-899f-424a-bb4c-2db731dac9c0/wireframing-process-photoshop-xd-image-8.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/80b2326f-899f-424a-bb4c-2db731dac9c0/wireframing-process-photoshop-xd-image-8.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/80b2326f-899f-424a-bb4c-2db731dac9c0/wireframing-process-photoshop-xd-image-8.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/80b2326f-899f-424a-bb4c-2db731dac9c0/wireframing-process-photoshop-xd-image-8.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/80b2326f-899f-424a-bb4c-2db731dac9c0/wireframing-process-photoshop-xd-image-8.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/80b2326f-899f-424a-bb4c-2db731dac9c0/wireframing-process-photoshop-xd-image-8.png"
			sizes="100vw"
			alt="creating two artboards, one for desktop and one for mobile"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>Now we can begin to create our wireframe objects. Following our hand-drawn sketches, we will now create the same objects in XD.</p>

<p><strong>Hero Image</strong><br />
Select the Rectangle Tool (<kbd>R</kbd>) and draw a shape where your hero image should be. Then grab the Line Tool (<kbd>L</kbd>) and draw two lines joining the vertices. This kind of shape represents our image placeholder.</p>

<p>Group the shape and lines and call the group “Hero”:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6943a20b-4fa8-497b-aba2-9181e85354da/wireframing-process-photoshop-xd-image-9.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6943a20b-4fa8-497b-aba2-9181e85354da/wireframing-process-photoshop-xd-image-9.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6943a20b-4fa8-497b-aba2-9181e85354da/wireframing-process-photoshop-xd-image-9.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6943a20b-4fa8-497b-aba2-9181e85354da/wireframing-process-photoshop-xd-image-9.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6943a20b-4fa8-497b-aba2-9181e85354da/wireframing-process-photoshop-xd-image-9.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6943a20b-4fa8-497b-aba2-9181e85354da/wireframing-process-photoshop-xd-image-9.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6943a20b-4fa8-497b-aba2-9181e85354da/wireframing-process-photoshop-xd-image-9.png"
			sizes="100vw"
			alt="grouping shapes and lines"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>Now let’s continue with the “Icons” section. I put some text before my icons, and I’m going to represent that visually with some lines. Grab the Line Tool (<kbd>L</kbd>) again and draw a single horizontal line. Click on Repeat Grid Tool (<kbd>⌘</kbd> + <kbd>R</kbd> on Mac or <kbd>CTRL</kbd> + <kbd>R</kbd> on Windows), and drag your line until you have three of them.</p>

<figure></figure>

<p>We need three symbols for our icons, so click on Ellipse Tool /<kbd>E</kbd>) and draw a circle. Click again on Repeat Grid Tool (<kbd>⌘</kbd> + <kbd>R</kbd> on Mac or <kbd>CTRL</kbd> + <kbd>R</kbd> on Windows) and create three circles. Then select the space between the circles and drag to make it wider.</p>

<figure></figure>

<p><strong>Feature Section</strong><br />
Create a light grey background (<code>#F8F8F8</code>) by using the Rectangle Tool (<kbd>R</kbd>). Repeat the steps from the previous Hero Image section above to create an image placeholder, then repeat the steps from the Icons Section (also above) to create a line for text. Finally, create a simple button with the help of the Rectangle Tool (<kbd>R</kbd>) tool.</p>

<p>This is the final result:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/195b4181-261f-4b00-8a4f-6b2816a5f1a0/wireframing-process-photoshop-xd-image-12.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/195b4181-261f-4b00-8a4f-6b2816a5f1a0/wireframing-process-photoshop-xd-image-12.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/195b4181-261f-4b00-8a4f-6b2816a5f1a0/wireframing-process-photoshop-xd-image-12.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/195b4181-261f-4b00-8a4f-6b2816a5f1a0/wireframing-process-photoshop-xd-image-12.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/195b4181-261f-4b00-8a4f-6b2816a5f1a0/wireframing-process-photoshop-xd-image-12.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/195b4181-261f-4b00-8a4f-6b2816a5f1a0/wireframing-process-photoshop-xd-image-12.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/195b4181-261f-4b00-8a4f-6b2816a5f1a0/wireframing-process-photoshop-xd-image-12.png"
			sizes="100vw"
			alt="Final result"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>For the Testimonial Section, repeat the same steps as before in order to create an image placeholder and some text lines. As you can see from the complete wireframe image, there’s a quotation-mark symbol that we have to insert.</p>

<p>We’re going to do it using Photoshop.</p>

<p>Open the Photoshop file I provided by clicking .</p>

<p>I want to insert this image as a symbol by using Libraries CC.</p>

<p>In Photoshop, be sure to see Libraries panel by going on <strong>Window</strong>&nbsp;&rarr;&nbsp;<strong>Libraries</strong>. Create a new library by clicking on the little icon top right (see image):</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cdc10d39-ffa7-4b31-a002-06186c0fd47c/wireframing-process-photoshop-xd-image-13.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cdc10d39-ffa7-4b31-a002-06186c0fd47c/wireframing-process-photoshop-xd-image-13.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cdc10d39-ffa7-4b31-a002-06186c0fd47c/wireframing-process-photoshop-xd-image-13.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cdc10d39-ffa7-4b31-a002-06186c0fd47c/wireframing-process-photoshop-xd-image-13.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cdc10d39-ffa7-4b31-a002-06186c0fd47c/wireframing-process-photoshop-xd-image-13.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cdc10d39-ffa7-4b31-a002-06186c0fd47c/wireframing-process-photoshop-xd-image-13.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cdc10d39-ffa7-4b31-a002-06186c0fd47c/wireframing-process-photoshop-xd-image-13.png"
			sizes="100vw"
			alt="creating a new library"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>I named my library &ldquo;Wireframe&rdquo;. Feel free to give your library the name you desire.</p>

<p>Now click and drag on the symbol you want to have in your library:</p>

<figure></figure>

<p>Switch back to XD, and go to <strong>File</strong>&nbsp;&rarr;&nbsp;<strong>Open CC Libraries</strong> and you will see the last symbol you just uploaded through Photoshop and the library you created.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2a46ff66-3211-44c8-aaaa-8056c9815e27/wireframing-process-photoshop-xd-image-15.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2a46ff66-3211-44c8-aaaa-8056c9815e27/wireframing-process-photoshop-xd-image-15.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2a46ff66-3211-44c8-aaaa-8056c9815e27/wireframing-process-photoshop-xd-image-15.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2a46ff66-3211-44c8-aaaa-8056c9815e27/wireframing-process-photoshop-xd-image-15.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2a46ff66-3211-44c8-aaaa-8056c9815e27/wireframing-process-photoshop-xd-image-15.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2a46ff66-3211-44c8-aaaa-8056c9815e27/wireframing-process-photoshop-xd-image-15.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2a46ff66-3211-44c8-aaaa-8056c9815e27/wireframing-process-photoshop-xd-image-15.png"
			sizes="100vw"
			alt="symbols created in photoshop and moved to adobe xd"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>Drag the quotation symbol into your wireframe in XD and position it wherever you need it to be.</p>

<figure></figure>

<p>For the “Prices, Subscribe and Footer” sections, we will represent them by using additional boxes and lines like the ones you see in the image below.</p>

<p><strong>Note</strong>: <em>You can find the  email icon in the Photoshop file which I’ve provided </em>.)</p>

<p>Follow the steps described in the <strong>Feature</strong> section to insert the symbol in the library through Photoshop, open it in XD, and drag it into your wireframe artboard.</p>

<p>This is the result:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c3a2b7a5-3623-40bc-a9d6-cbcd7a8b4754/wireframing-process-photoshop-xd-image-17.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c3a2b7a5-3623-40bc-a9d6-cbcd7a8b4754/wireframing-process-photoshop-xd-image-17.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c3a2b7a5-3623-40bc-a9d6-cbcd7a8b4754/wireframing-process-photoshop-xd-image-17.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c3a2b7a5-3623-40bc-a9d6-cbcd7a8b4754/wireframing-process-photoshop-xd-image-17.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c3a2b7a5-3623-40bc-a9d6-cbcd7a8b4754/wireframing-process-photoshop-xd-image-17.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c3a2b7a5-3623-40bc-a9d6-cbcd7a8b4754/wireframing-process-photoshop-xd-image-17.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c3a2b7a5-3623-40bc-a9d6-cbcd7a8b4754/wireframing-process-photoshop-xd-image-17.png"
			sizes="100vw"
			alt="result"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>One last thing we need to do before going ahead is to order our layers. Be sure your layers are activated by clicking on the Layer Icon (<kbd>⌘</kbd> + <kbd>Y</kbd> for Mac or <kbd>CTRL</kbd> + <kbd>Y</kbd> for Windows).</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/820167d5-417c-429f-aabe-cc20de01139b/wireframing-process-photoshop-xd-image-18.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/820167d5-417c-429f-aabe-cc20de01139b/wireframing-process-photoshop-xd-image-18.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/820167d5-417c-429f-aabe-cc20de01139b/wireframing-process-photoshop-xd-image-18.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/820167d5-417c-429f-aabe-cc20de01139b/wireframing-process-photoshop-xd-image-18.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/820167d5-417c-429f-aabe-cc20de01139b/wireframing-process-photoshop-xd-image-18.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/820167d5-417c-429f-aabe-cc20de01139b/wireframing-process-photoshop-xd-image-18.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/820167d5-417c-429f-aabe-cc20de01139b/wireframing-process-photoshop-xd-image-18.png"
			sizes="100vw"
			alt="ordering layers in adobe xd"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>Group all of the section elements into folders (I assigned them the same name of the section they represent). This way, you will have all of your elements placed in order and won’t have any difficulty in finding them quickly (see image).</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/503bde6b-f54c-4bdf-b362-4889a81a25c5/wireframing-process-photoshop-xd-image-19.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/503bde6b-f54c-4bdf-b362-4889a81a25c5/wireframing-process-photoshop-xd-image-19.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/503bde6b-f54c-4bdf-b362-4889a81a25c5/wireframing-process-photoshop-xd-image-19.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/503bde6b-f54c-4bdf-b362-4889a81a25c5/wireframing-process-photoshop-xd-image-19.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/503bde6b-f54c-4bdf-b362-4889a81a25c5/wireframing-process-photoshop-xd-image-19.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/503bde6b-f54c-4bdf-b362-4889a81a25c5/wireframing-process-photoshop-xd-image-19.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/503bde6b-f54c-4bdf-b362-4889a81a25c5/wireframing-process-photoshop-xd-image-19.png"
			sizes="100vw"
			alt="grouping section elements into folders"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>












<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/724ed16f-5fd1-456b-aa09-c90c0ea6b48e/wireframing-process-photoshop-xd-image-20.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/724ed16f-5fd1-456b-aa09-c90c0ea6b48e/wireframing-process-photoshop-xd-image-20.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/724ed16f-5fd1-456b-aa09-c90c0ea6b48e/wireframing-process-photoshop-xd-image-20.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/724ed16f-5fd1-456b-aa09-c90c0ea6b48e/wireframing-process-photoshop-xd-image-20.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/724ed16f-5fd1-456b-aa09-c90c0ea6b48e/wireframing-process-photoshop-xd-image-20.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/724ed16f-5fd1-456b-aa09-c90c0ea6b48e/wireframing-process-photoshop-xd-image-20.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/724ed16f-5fd1-456b-aa09-c90c0ea6b48e/wireframing-process-photoshop-xd-image-20.png"
			sizes="100vw"
			alt="grouping section elements into folders"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>We are now done with our wireframe!</p>

<p>In the next step, we will build our design by using our wireframe and discovering how to modify Libraries’ elements instantly.</p>

<h4 id="2-adding-a-layer-of-fidelity-to-your-wireframe">2. Adding A Layer Of Fidelity To Your Wireframe</h4>

<p>We have just finished our wireframe and, at this point, we can double-check it to see if we have missed something. Once we are sure that we have all of the necessary information included in the wireframe, we can then share it with the project’s team.</p>

<p>We are ready to move on and update our wireframe to make it &ldquo;live&rdquo; with images, color, and placeholder copy.</p>

<p>Go ahead and create your design. Duplicate your wireframe by saving it with another name (e.g. “Wireframe-Layout”).</p>

<p>First, we’ll need an image for our Hero section (I went ahead and used .)</p>

<p>Open the image in Photoshop, and reduce the image size by clicking on <strong>Image</strong>&nbsp;&rarr;&nbsp;<strong>Image size</strong> and set the width at 3000px:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1e2dface-885a-4449-bdd5-d46621b535a0/wireframing-process-photoshop-xd-image-21.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1e2dface-885a-4449-bdd5-d46621b535a0/wireframing-process-photoshop-xd-image-21.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1e2dface-885a-4449-bdd5-d46621b535a0/wireframing-process-photoshop-xd-image-21.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1e2dface-885a-4449-bdd5-d46621b535a0/wireframing-process-photoshop-xd-image-21.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1e2dface-885a-4449-bdd5-d46621b535a0/wireframing-process-photoshop-xd-image-21.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1e2dface-885a-4449-bdd5-d46621b535a0/wireframing-process-photoshop-xd-image-21.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1e2dface-885a-4449-bdd5-d46621b535a0/wireframing-process-photoshop-xd-image-21.png"
			sizes="100vw"
			alt="reducing image size"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>Save your image and then drag it into your Libraries.</p>

<p>In XD, drag the image from Libraries to your Artboard. Let it fit with the shape we just created as the image placeholder.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2ebb0c31-28e1-44c4-a753-e3d836a11754/wireframing-process-photoshop-xd-image-22.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2ebb0c31-28e1-44c4-a753-e3d836a11754/wireframing-process-photoshop-xd-image-22.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2ebb0c31-28e1-44c4-a753-e3d836a11754/wireframing-process-photoshop-xd-image-22.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2ebb0c31-28e1-44c4-a753-e3d836a11754/wireframing-process-photoshop-xd-image-22.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2ebb0c31-28e1-44c4-a753-e3d836a11754/wireframing-process-photoshop-xd-image-22.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2ebb0c31-28e1-44c4-a753-e3d836a11754/wireframing-process-photoshop-xd-image-22.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2ebb0c31-28e1-44c4-a753-e3d836a11754/wireframing-process-photoshop-xd-image-22.png"
			sizes="100vw"
			alt="dragging the image from Libraries to your Artboard"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>I’m going to add a logo and some text to this image; I  need the image to be a little darker so that the information is easy to read. Go back into Photoshop Libraries and double click on the image in the panel. Once the image is open, go on the Layer panel, select the image layer and click on <strong>Add a layer style</strong> at the bottom of the panel. Set a <strong>Color Overlay</strong> with the settings as shown below:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/85bfa3fe-7a86-4df9-a478-5fef388429ed/wireframing-process-photoshop-xd-image-23.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/85bfa3fe-7a86-4df9-a478-5fef388429ed/wireframing-process-photoshop-xd-image-23.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/85bfa3fe-7a86-4df9-a478-5fef388429ed/wireframing-process-photoshop-xd-image-23.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/85bfa3fe-7a86-4df9-a478-5fef388429ed/wireframing-process-photoshop-xd-image-23.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/85bfa3fe-7a86-4df9-a478-5fef388429ed/wireframing-process-photoshop-xd-image-23.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/85bfa3fe-7a86-4df9-a478-5fef388429ed/wireframing-process-photoshop-xd-image-23.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/85bfa3fe-7a86-4df9-a478-5fef388429ed/wireframing-process-photoshop-xd-image-23.png"
			sizes="100vw"
			alt="adding a logo and some text to the image"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>Save it, and it will be automatically be saved in all of your libraries. Switch back to XD and you will see the image in your artboard updated (no need to drag it back from the library again).</p>

<p><strong>Note</strong>: <em>Depending on the image size, it could take a little more time for the libraries to update themselves.</em></p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/57556868-e283-456e-9d81-c669f8b9c8d8/wireframing-process-photoshop-xd-image-24.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/57556868-e283-456e-9d81-c669f8b9c8d8/wireframing-process-photoshop-xd-image-24.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/57556868-e283-456e-9d81-c669f8b9c8d8/wireframing-process-photoshop-xd-image-24.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/57556868-e283-456e-9d81-c669f8b9c8d8/wireframing-process-photoshop-xd-image-24.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/57556868-e283-456e-9d81-c669f8b9c8d8/wireframing-process-photoshop-xd-image-24.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/57556868-e283-456e-9d81-c669f8b9c8d8/wireframing-process-photoshop-xd-image-24.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/57556868-e283-456e-9d81-c669f8b9c8d8/wireframing-process-photoshop-xd-image-24.png"
			sizes="100vw"
			alt="updating images in libraries"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>Now let’s insert our logo. .</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/df4c1798-e3b7-45ad-b3da-e0aa15331cc1/wireframing-process-photoshop-xd-image-25.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/df4c1798-e3b7-45ad-b3da-e0aa15331cc1/wireframing-process-photoshop-xd-image-25.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/df4c1798-e3b7-45ad-b3da-e0aa15331cc1/wireframing-process-photoshop-xd-image-25.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/df4c1798-e3b7-45ad-b3da-e0aa15331cc1/wireframing-process-photoshop-xd-image-25.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/df4c1798-e3b7-45ad-b3da-e0aa15331cc1/wireframing-process-photoshop-xd-image-25.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/df4c1798-e3b7-45ad-b3da-e0aa15331cc1/wireframing-process-photoshop-xd-image-25.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/df4c1798-e3b7-45ad-b3da-e0aa15331cc1/wireframing-process-photoshop-xd-image-25.png"
			sizes="100vw"
			alt="inserting the logo in photoshop"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>Since our background is dark, we will need a white logo. Switch back to Photoshop and double click on the logo from Libraries.</p>

<p>Grab the Type Tool, highlight the logo text, and make it white. Save it, and it will automatically be saved in your XD artboard as well.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fc2c8279-6d5a-4a0a-9e18-a80eab71296d/wireframing-process-photoshop-xd-image-26.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fc2c8279-6d5a-4a0a-9e18-a80eab71296d/wireframing-process-photoshop-xd-image-26.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fc2c8279-6d5a-4a0a-9e18-a80eab71296d/wireframing-process-photoshop-xd-image-26.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fc2c8279-6d5a-4a0a-9e18-a80eab71296d/wireframing-process-photoshop-xd-image-26.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fc2c8279-6d5a-4a0a-9e18-a80eab71296d/wireframing-process-photoshop-xd-image-26.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fc2c8279-6d5a-4a0a-9e18-a80eab71296d/wireframing-process-photoshop-xd-image-26.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fc2c8279-6d5a-4a0a-9e18-a80eab71296d/wireframing-process-photoshop-xd-image-26.png"
			sizes="100vw"
			alt="creating a while logo on a dark background"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>












<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fc353ca5-7017-48a1-a82b-60623951fb0f/wireframing-process-photoshop-xd-image-27.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fc353ca5-7017-48a1-a82b-60623951fb0f/wireframing-process-photoshop-xd-image-27.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fc353ca5-7017-48a1-a82b-60623951fb0f/wireframing-process-photoshop-xd-image-27.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fc353ca5-7017-48a1-a82b-60623951fb0f/wireframing-process-photoshop-xd-image-27.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fc353ca5-7017-48a1-a82b-60623951fb0f/wireframing-process-photoshop-xd-image-27.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fc353ca5-7017-48a1-a82b-60623951fb0f/wireframing-process-photoshop-xd-image-27.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fc353ca5-7017-48a1-a82b-60623951fb0f/wireframing-process-photoshop-xd-image-27.png"
			sizes="100vw"
			alt="creating a while logo on a dark background"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>Insert some text and a button to complete the Hero section.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e759f8a3-8d68-4674-8553-7e15757a2fad/wireframing-process-photoshop-xd-image-28.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e759f8a3-8d68-4674-8553-7e15757a2fad/wireframing-process-photoshop-xd-image-28.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e759f8a3-8d68-4674-8553-7e15757a2fad/wireframing-process-photoshop-xd-image-28.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e759f8a3-8d68-4674-8553-7e15757a2fad/wireframing-process-photoshop-xd-image-28.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e759f8a3-8d68-4674-8553-7e15757a2fad/wireframing-process-photoshop-xd-image-28.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e759f8a3-8d68-4674-8553-7e15757a2fad/wireframing-process-photoshop-xd-image-28.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e759f8a3-8d68-4674-8553-7e15757a2fad/wireframing-process-photoshop-xd-image-28.png"
			sizes="100vw"
			alt="inserting some text and a button to complete the Hero section"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>Next, I’m going fill out the next section by adding text and icons. The ones I used are from a free pack I created for Smashing Magazine that .</p>

<p>As previously done, open up the icons and add them to your libraries in Photoshop, then switch back to XD to place them in your wireframe. Here is the result:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/534c8b00-4716-4d7d-a16e-d727731c37c4/wireframing-process-photoshop-xd-image-29.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/534c8b00-4716-4d7d-a16e-d727731c37c4/wireframing-process-photoshop-xd-image-29.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/534c8b00-4716-4d7d-a16e-d727731c37c4/wireframing-process-photoshop-xd-image-29.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/534c8b00-4716-4d7d-a16e-d727731c37c4/wireframing-process-photoshop-xd-image-29.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/534c8b00-4716-4d7d-a16e-d727731c37c4/wireframing-process-photoshop-xd-image-29.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/534c8b00-4716-4d7d-a16e-d727731c37c4/wireframing-process-photoshop-xd-image-29.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/534c8b00-4716-4d7d-a16e-d727731c37c4/wireframing-process-photoshop-xd-image-29.png"
			sizes="100vw"
			alt="adding text and icons, result"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>Now we’ll move on to the <strong>Feature</strong> section. As before, we’ll drag an image onto the image placeholder (I used ). Add in some text and a button as I have shown you in the previous steps above.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0a6895af-4454-44b9-bfd8-a142f9ba31ef/wireframing-process-photoshop-xd-image-30.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0a6895af-4454-44b9-bfd8-a142f9ba31ef/wireframing-process-photoshop-xd-image-30.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0a6895af-4454-44b9-bfd8-a142f9ba31ef/wireframing-process-photoshop-xd-image-30.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0a6895af-4454-44b9-bfd8-a142f9ba31ef/wireframing-process-photoshop-xd-image-30.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0a6895af-4454-44b9-bfd8-a142f9ba31ef/wireframing-process-photoshop-xd-image-30.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0a6895af-4454-44b9-bfd8-a142f9ba31ef/wireframing-process-photoshop-xd-image-30.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0a6895af-4454-44b9-bfd8-a142f9ba31ef/wireframing-process-photoshop-xd-image-30.png"
			sizes="100vw"
			alt="feature section"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>Open  and add the check symbol into your Libraries. Open Libraries in XD and put the icon near the text. Use the Repeat Grid to make three copies of it:</p>

<figure></figure>

<p>Now let’s change the color of the check symbol. Go back to Photoshop, open it from the Libraries and give it a Color Overlay as shown below:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5b49fec8-e77d-4a37-ae02-e32b23c69070/wireframing-process-photoshop-xd-image-32.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5b49fec8-e77d-4a37-ae02-e32b23c69070/wireframing-process-photoshop-xd-image-32.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5b49fec8-e77d-4a37-ae02-e32b23c69070/wireframing-process-photoshop-xd-image-32.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5b49fec8-e77d-4a37-ae02-e32b23c69070/wireframing-process-photoshop-xd-image-32.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5b49fec8-e77d-4a37-ae02-e32b23c69070/wireframing-process-photoshop-xd-image-32.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5b49fec8-e77d-4a37-ae02-e32b23c69070/wireframing-process-photoshop-xd-image-32.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5b49fec8-e77d-4a37-ae02-e32b23c69070/wireframing-process-photoshop-xd-image-32.png"
			sizes="100vw"
			alt="changing the color of the check symbol"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>Save it, and see your icons in XD directly updated.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6a77b457-38d0-431e-9704-d267df0e48ef/wireframing-process-photoshop-xd-image-33.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6a77b457-38d0-431e-9704-d267df0e48ef/wireframing-process-photoshop-xd-image-33.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6a77b457-38d0-431e-9704-d267df0e48ef/wireframing-process-photoshop-xd-image-33.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6a77b457-38d0-431e-9704-d267df0e48ef/wireframing-process-photoshop-xd-image-33.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6a77b457-38d0-431e-9704-d267df0e48ef/wireframing-process-photoshop-xd-image-33.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6a77b457-38d0-431e-9704-d267df0e48ef/wireframing-process-photoshop-xd-image-33.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6a77b457-38d0-431e-9704-d267df0e48ef/wireframing-process-photoshop-xd-image-33.png"
			sizes="100vw"
			alt="changing the color of the check symbol"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>Now let’s finish our layout.</p>

<p>For the <strong>Testimonial</strong> section, add in text and an image for the testimonial (I took mine ).</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/70721198-debb-4758-8520-7d7d90d5db0a/wireframing-process-photoshop-xd-image-34.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/70721198-debb-4758-8520-7d7d90d5db0a/wireframing-process-photoshop-xd-image-34.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/70721198-debb-4758-8520-7d7d90d5db0a/wireframing-process-photoshop-xd-image-34.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/70721198-debb-4758-8520-7d7d90d5db0a/wireframing-process-photoshop-xd-image-34.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/70721198-debb-4758-8520-7d7d90d5db0a/wireframing-process-photoshop-xd-image-34.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/70721198-debb-4758-8520-7d7d90d5db0a/wireframing-process-photoshop-xd-image-34.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/70721198-debb-4758-8520-7d7d90d5db0a/wireframing-process-photoshop-xd-image-34.png"
			sizes="100vw"
			alt="adding in text and an image for the testimonial"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>Finally, we’ll add information for the <strong>Price</strong> section, the <strong>Subscribe</strong> section, and the footer. You can find Price tables in the . Drag them into your Libraries in Photoshop, then open Libraries in XD and drag them into your artboard. Feel free to modify them as you want.</p>

<p>And&hellip; we’re done!</p>

<h3 id="conclusion">Conclusion</h3>

<p>In this tutorial, we have learned how to work with Photoshop and  which you can use to practice and follow along to this tutorial. Follow the steps as we did for the desktop version to add text and images.</p>

<p>Let me see your result in the comments!</p>

<p><em>This article is part of the UX design series sponsored by Adobe. Adobe XD tool is made for a  to stay updated and informed on the latest trends and insights for UX/UI design.</em></p>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(il)</span>
</div>


              </article>
            </body>
          </html>
---------------
<h1 id="#title_2" >3、文章： 如何解决区块链的硬伤：对时间的感知</h1>
Daniel Kmak
[http://www.infoq.com/cn/articles/blockchain-doesnt-know-time?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/blockchain-doesnt-know-time?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/blockchain-doesnt-know-time/zh/smallimage/book-cover-leadership-agility-1516406885241-1529426164673.jpg"/><p>加密数字货币希望能最终撼动银行，为了让其变为现实，加密钱包的功能就不能被银行系统比下去。银行最基本的功能之一是交易调度。但不幸的是，区块链不知道时间的概念，而我们需要改变这个现状。</p> <i>By Daniel Kmak</i> <i> Translated by 周小璐</i>
---------------
<h1 id="#title_3" >4、文章： 针对ASP.NET Core Web API的先进架构</h1>
Chris Woodruff
[http://www.infoq.com/cn/articles/advanced-architecture-aspnet-core?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/advanced-architecture-aspnet-core?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/advanced-architecture-aspnet-core/zh/smallimage/GettyImages-947661322-1527676268787-1529422958506.jpg"/><p>本文将探讨ASP.NET Core是如何使现代web API的构建变得更加容易的。它使实现易于设计、测试和维护。通过使用端口和适配器模式，业务逻辑可以从API框架和数据访问中分离出来。</p> <i>By Chris Woodruff</i> <i> Translated by 冬雨</i>
---------------
<h1 id="#title_4" >5、文章： 以太坊Dapp入门实战(一)</h1>
Mahesh Murthy
[http://www.infoq.com/cn/articles/full-stack-ethereum-dapp-tutorial-part-1?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/full-stack-ethereum-dapp-tutorial-part-1?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/full-stack-ethereum-dapp-tutorial-part-1/zh/smallimage/BOLTS-1524870463316-1529424521081.jpg"/><p>俗话说，实践出真知！对于开发人员来说，最好的学习办法就是亲自动手做一个小项目。所以，接下来我们将会以一个投票程序为例，带着你在以太坊平台上搭建一个dapp。</p> <i>By Mahesh Murthy</i> <i> Translated by 海兴</i>
---------------
<h1 id="#title_5" >6、ASP.NET Core 2.1带来SignalR、Razor类库</h1>
Jeff Martin
[http://www.infoq.com/cn/news/2018/06/aspnetcore21-released?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/06/aspnetcore21-released?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>随着.NET Core 2.1的发布，微软推出了 ASP.NET Core 2.1。这是一个强大的版本，包括实时通信库SignalR，更新的模板使GDPR更容易遵守，并且针对Angular、React，以及React + Redux更新了SPA模板。</p> <i>By Jeff Martin</i> <i> Translated by 冬雨</i>
---------------
<h1 id="#title_6" >7、全新的图形数据库云服务Amazon Neptune正式发布</h1>
Steef-Jan Wiggers
[http://www.infoq.com/cn/news/2018/06/aws-neptune-graph-ga?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/06/aws-neptune-graph-ga?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Amazon Neptune 是一个全新的托管在云端的图形数据库，在经过去年的非公开预览版本之后，终于在近期正式发布。使用者可以通过 Amazon Neptune，以图形模型（这是一种语义化的数据结构，以节点、边缘与属性的形式表示）的方式对数据进行管理。</p> <i>By Steef-Jan Wiggers</i> <i> Translated by 邵思华</i>
---------------
<h1 id="#title_7" >8、Facebook Sonar：一款可视化及交互式移动应用调试工具</h1>
Sergio De Simone
[http://www.infoq.com/cn/news/2018/06/facebook-sonar-mobile-app-debug?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/06/facebook-sonar-mobile-app-debug?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Facebook Sonar是一个开源工具集，旨在帮助开发人员以交互式和可扩展的方式检查和理解iOS及Android应用程序的结构和行为。</p> <i>By Sergio De Simone</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_8" >9、谷歌发布Android P Beta 2</h1>
Diogo Carleto
[http://www.infoq.com/cn/news/2018/06/android-p-beta-2?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/06/android-p-beta-2?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>谷歌发布了Android P Beta 2，包含最终的Android P API（API Level 28）、最新的系统镜像、显示剪切支持等。</p> <i>By Diogo Carleto</i> <i> Translated by 无明</i>
---------------