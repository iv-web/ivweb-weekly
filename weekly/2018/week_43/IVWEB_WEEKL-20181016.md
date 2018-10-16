## 文章索引
1、 <a href="#1360开源又一力作kafkabridge让操作kafka更简单" >360开源又一力作——KafkaBridge：让操作kafka更简单！</a><br/>
2、 <a href="#2fex-技术周刊---2018/10/15" >FEX 技术周刊 - 2018/10/15</a><br/>
3、 <a href="#3文章-使用反应式领域驱动设计来解决不确定性" >文章： 使用反应式领域驱动设计来解决不确定性</a><br/>
4、 <a href="#4文章-以chef和ansible为例快速入门服务器配置" >文章： 以Chef和Ansible为例快速入门服务器配置</a><br/>
5、 <a href="#5文章-v神应用zcash技术以太坊能扩展到500tx/s" >文章： V神：应用Zcash技术，以太坊能扩展到500tx/s</a><br/>
6、 <a href="#6文章-为什么devops和sre职位这么难招人" >文章： 为什么DevOps和SRE职位这么难招人？</a><br/>
7、 <a href="#7smart-bundling:-how-to-serve-legacy-code-only-to-legacy-browsers" >Smart Bundling: How To Serve Legacy Code Only To Legacy Browsers</a><br/>
8、 <a href="#8chaosconf-2018混沌实验的演变" >ChaosConf 2018：混沌实验的演变</a><br/>
9、 <a href="#9微软宣布针对azure-cosmos-db的多个更新" >微软宣布针对Azure Cosmos DB的多个更新</a><br/>
10、 <a href="#10visual-studio-2017-159预览版3支持arm64-for-uwp" >Visual Studio 2017 15.9预览版3支持ARM64 for UWP</a><br/>
11、 <a href="#11oracle推出轻量级java微服务框架helidon" >Oracle推出轻量级Java微服务框架Helidon</a><br/>
12、 <a href="#12kafka落选infoworld最佳开源数据平台奖公布" >Kafka落选！InfoWorld最佳开源数据平台奖公布</a><br/><h1 id="#title_0" >1、360开源又一力作——KafkaBridge：让操作kafka更简单！</h1>
张婵
[http://www.infoq.com/cn/news/2018/10/360-kafka-bridge?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/10/360-kafka-bridge?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>KafkaBridge 封装了对Kafka集群的读写操作，接口极少，简单易用，稳定可靠，支持c++/c、php、python、golang等多种语言，并特别针对php-fpm场景中作了长连接复用的优化，已在360公司内部广泛使用。</p> <i>By 张婵</i>
---------------
<h1 id="#title_1" >2、FEX 技术周刊 - 2018/10/15</h1>

[http://fex.baidu.com/blog/2018/10/fex-weekly-15//](http://fex.baidu.com/blog/2018/10/fex-weekly-15//)
作者：2betop <br> <h2 id="section">深阅读</h2>

<p><strong>Rethinking Unit Test Assertions</strong><br />
https://medium.com/javascript-scene/rethinking-unit-test-assertions-55f59358253f<br />
The problem with most test frameworks is that they’re so busy making it easy for you to take shortcuts with their “convenient” assertions that they forget that the biggest value of a test is realized when the test fails. At the failure stage, the convenience of writing the test matters a lot less than how easy it is to figure out what went wrong when we read the test.</p>

<p><strong>12 Factor CLI Apps</strong><br />
https://medium.com/@jdxcode/12-factor-cli-apps-dd3c227a0e46<br />
At Heroku, we’ve come up with a methodology called the 12 factor app. It’s a set of principles designed to make great web applications that are easy to maintain. In that spirit, here are 12 CLI factors to keep in mind when building your next CLI application. Following these principles will offer CLI UX that users will love.</p>

<p><strong>Death by a thousand cuts - a checklist for eliminating common React performance issues</strong><br />
https://logrocket-blog.ghost.io/death-by-a-thousand-cuts-a-checklist-for-eliminating-common-react-performance-issues/<br />
A pragmatic step-by-step guide to eliminating common react performance issues.</p>

<p><strong>Start Performance Budgeting</strong><br />
https://addyosmani.com/blog/performance-budgets/<br />
If you’re building a web experience and want to stay fast, a performance budget can be critical. For success, embrace performance budgets and learn to live within them. Network &amp; CPU limits on mobile can require asking hard questions like, “what is really important to my users?”</p>

<p><strong>The Suspense is Killing Redux</strong><br />
https://medium.com/@ryanflorence/the-suspense-is-killing-redux-e888f9692430<br />
At my latest workshops I’ve been getting this question: So does Suspense kill Redux? First, that’s a rude way to put it. But I get it, the suspense is killing you — or maybe Redux.</p>

<p><strong>[译]再见，面向对象编程</strong><br />
https://mp.weixin.qq.com/s?__biz=MzU0Nzk1MTg5OA==&amp;mid=2247483877&amp;idx=1&amp;sn=39cc95efadec791b8ca572e27d94ef92<br />
几十年来，我一直都在使用面向对象语言编程。 我使用的第一个面向对象语言是C ++，接着是Smalltalk，最后是.NET和Java。我曾经是面向对象三大范式：继承，封装和多态，狂热的拥趸者，为他们的所带来的遍历疯狂。我渴望得到它（面向对象）所承诺的重用性，并期待自己能站在前人的肩膀上，进入这块全新、美好的土地。一想到只要将现实世界的物体映射到他们对应的类中，他们就能整齐的找到自己的位置，我就无法抑制自己的兴奋。但“我不能错的更多”。</p>

<p><strong>前端安全系列之二：如何防止CSRF攻击</strong><br />
https://tech.meituan.com/fe_security_csrf.html<br />
相比XSS，CSRF的名气似乎并不是那么大，很多人都认为“CSRF不具备那么大的破坏性”。真的是这样吗？接下来，我们还是有请小明同学再次“闪亮”登场。</p>

<p><strong>精致化的微前端开发之旅</strong><br />
https://zhuanlan.zhihu.com/p/46284079<br />
微前端（Micro-Frontend），是将微服务（Micro-Services）理念应用于前端技术后的相关实践，使得一个前端项目能够经由多个团队独立开发以及独立部署。本文中将会以此为目标，从零构建一套微前端的开发方案的最佳实践*，并用于完成 Micro Frontends 网站中的示例应用。</p>

<p><strong>深拷贝的终极探索</strong><br />
https://yanhaijing.com/javascript/2018/10/10/clone-deep/<br />
本文我将给大家破解深拷贝的谜题，由浅入深，环环相扣，总共涉及4种深拷贝方式，每种方式都有自己的特点和个性。</p>

<p><strong>Why We Decided to Rewrite Uber’s Driver App</strong><br />
https://eng.uber.com/rewrite-uber-carbon-app/<br />
This article is the first in a series covering how Uber’s mobile engineering team developed the newest version of our driver app, codenamed Carbon, a core component of our ridesharing business. Among other new features, the app lets our population of over three million driver-partners find fares, get directions, and track their earnings. We began designing the new app in conjunction with feedback from our driver-partners in 2017, and began rolling it out for production in September 2018.</p>

<p><strong>Understanding the difference between grid-template and grid-auto</strong><br />
https://bitsofco.de/understanding-the-difference-between-grid-template-and-grid-auto/<br />
To summarize, the grid-template-* properties are used to create, place, and size cells for the explicit grid. Any cell that exists in the grid that is not explicitly created by this property forms part of the implicit grid, which can be sized by the grid-auto-* properties.</p>

<p><strong>Building Enterprise Software on LinkedIn’s Consumer Stack: Behind the Scenes of LinkedIn Talent Hub</strong><br />
https://engineering.linkedin.com/blog/2018/10/building-linkedin-talent-hub<br />
In this blog post, we will discuss the foundational building blocks that were either built from scratch, or created by modifying existing platforms, to power LinkedIn’s new Talent Hub product.</p>

<p><strong>Why we need the distributed web</strong><br />
https://www.ctrl.blog/entry/the-dweb<br />
The distributed web seeks to make peer-to-peer content distribution the new default. This should help make the web topology more democratic and resilient to nature and political whims.</p>

<p><strong>Infrastructure as Code - Getting Started with Terraform</strong><br />
https://blog.scottlogic.com/2018/10/08/infrastructure-as-code-getting-started-with-terraform.html<br />
This blog post serves as a brief introduction to what Infrastructure as Code is, as well as how to get started using it with Terraform. Although Terraform can be used with many cloud providers, the post focuses particularly on deploying resources to AWS.</p>

<p><strong>Dropbox traffic infrastructure: Edge network</strong><br />
https://blogs.dropbox.com/tech/2018/10/dropbox-traffic-infrastructure-edge-network/<br />
Dropbox has more than half a billion registered users who trust us with exabytes of data and petabytes of corresponding metadata. For the Traffic team this means millions of HTTP requests and terabits of traffic. To support all of that we’ve built an extensive network of points of presence (PoPs) around the world that we call Edge. 另附 Dropbox 的 </p>

<p><strong>Applying machine intelligence to GitHub security alerts</strong><br />
https://blog.github.com/2018-10-09-applying-machine-intelligence-to-security-alerts/<br />
We created a machine learning model that scans text associated with public commits (the commit message and linked issues or pull requests) to filter out those related to possible security upgrades. With this smaller batch of commits, the model uses the diff to understand how required version ranges have changed.</p>

<p><strong>Writing system software: code comments</strong><br />
http://antirez.com/news/124<br />
In this post I analyze Redis comments, trying to categorize them.  Along the way I try to show why, in my opinion, writing comments is of paramount importance in order to produce good code, that is maintainable in the long run and understandable by others and by the authors during modifications and debugging activities.</p>

<h2 id="section-1">新鲜货</h2>

<p><strong>CKEditor 5 v11.1.0 released</strong><br />
https://ckeditor.com/blog/CKEditor-5-v11.1.0-released/<br />
This editor version brings the long-awaited media embed feature, support for block content in tables, tables available in real-time collaborative editing and many smaller features and improvements. We also streamlined our Operational Transformation engine to improve its support for already implemented collaboration features as well as those planned in the near future (like “suggestion mode”).</p>

<p><strong>Ionic 4 Beta: What’s New and Building a Sample App</strong><br />
https://auth0.com/blog/ionic-4-beta-whats-new-and-building-a-sample-app/<br />
In this article, you will learn about what’s new in Ionic 4, changes in the existing features, how to migrate your Ionic 3 app to Ionic 4 app, and about using Ionic with Stencil and Capacitor. Finally, you will create a simple application using Ionic 4 to see the new version of this framework in action.</p>

<p><strong>Custom Elements Now ‘In Development’ on Microsoft Edge</strong><br />
https://developer.microsoft.com/en-us/microsoft-edge/platform/status/customelements/<br />
Edge is the last major browser to get on board with custom elements. Shadow DOM is being worked on, too. 另附：</p>

<p><strong>Microsoft Joins the Open Invention Network Community</strong><br />
https://globenewswire.com/news-release/2018/10/10/1619375/0/en/Microsoft-Joins-the-Open-Invention-Network-Community.html<br />
Microsoft’s participation in OIN will drive additional innovation and enhance patent non-aggression in Linux and adjacent OSS technologies. 另附：</p>

<p><strong>Calls between JavaScript and WebAssembly are finally fast</strong><br />
https://hacks.mozilla.org/2018/10/calls-between-javascript-and-webassembly-are-finally-fast-%F0%9F%8E%89/<br />
In the latest version of Firefox Beta, calls between JS and WebAssembly are faster than non-inlined JS to JS function calls. 另附：.</p>

<p><strong>WorkerDOM</strong><br />
https://github.com/ampproject/worker-dom<br />
An in-progress (as in very-alpha) implementation of the DOM API intended to run within a Web Worker. Purpose: Move complexity of intermediate work related to DOM mutations to a background thread, sending only the necessary manipulations to a foreground thread.</p>

<p><strong>baffle.js</strong><br />
https://github.com/camwiegert/baffle<br />
A tiny javascript library for obfuscating and revealing text in DOM elements.</p>

<p><strong>Hover</strong><br />
https://github.com/IanLunn/Hover<br />
A collection of CSS3 powered hover effects to be applied to links, buttons, logos, SVG, featured images and so on. Easily apply to your own elements, modify or just use for inspiration. Available in CSS, Sass, and LESS.</p>

<p><strong>Bloom Filter</strong><br />
https://github.com/jasondavies/bloomfilter.js<br />
This JavaScript bloom filter implementation uses the non-cryptographic  for speed.</p>

<p><strong>awesome-mongodb</strong><br />
https://github.com/ramnes/awesome-mongodb<br />
A curated list of awesome MongoDB resources, libraries, tools and applications. 另附：.</p>

<p><strong>Muze - Composable data visualisation library for web with a data-first approach</strong><br />
https://github.com/chartshq/muze<br />
Compose data-driven layers to create interactive visualizations in JavaScript with relational algebra supported data model.</p>

<p><strong>Flatbush</strong><br />
https://github.com/mourner/flatbush<br />
A really fast static spatial index for 2D points and rectangles in JavaScript. An efficient implementation of the packed Hilbert R-tree algorithm. Enables fast spatial queries on a very large number of objects (e.g. millions), which is very useful in maps, data visualizations and computational geometry algorithms.</p>

<p><strong>Ferret</strong><br />
https://github.com/MontFerret/ferret<br />
ferret is a web scraping system aiming to simplify data extraction from the web for such things like UI testing, machine learning and analytics. Having its own declarative language, ferret abstracts away technical details and complexity of the underlying technologies, helping to focus on the data itself. It’s extremely portable, extensible and fast.</p>

<p><strong>Boltons</strong><br />
https://github.com/mahmoud/boltons<br />
Boltons is a set of over 220 BSD-licensed, pure-Python utilities in the same spirit as — and yet conspicuously missing from — the standard library. 另附：.</p>

<p><strong>Turn the web into a database: An alternative to web crawling/scraping</strong><br />
https://www.mixnode.com/blog/posts/turn-the-web-into-a-database-an-alternative-to-web-crawling-scraping<br />
Mixnode turns the web into a giant database! In other words, Mixnode allows you to think of all the web pages, images, videos, PDF files, and other resources on the web as rows in a database table; a giant database table with trillions of rows that you can query using the standard Structured Query Language (SQL).</p>

<p><strong>NVIDIA and Open-Source Ecosystem Come Together to Accelerate Data Science</strong><br />
https://blogs.nvidia.com/blog/2018/10/10/rapids-data-science-open-source-community/<br />
While the world’s data doubles each year, CPU computing has hit a brick wall with the end of Moore’s law. For this reason, scientific computing and deep learning have turned to NVIDIA GPU acceleration. Data analytics and machine learning haven’t yet tapped into the GPU as systematically. That’s changing.</p>

<h2 id="section-2">设计</h2>

<p><strong>Designing Experiences To Improve Mental Health</strong><br />
https://www.smashingmagazine.com/2018/10/designing-experiences-improving-mental-health/<br />
Designing apps for mental health is one area where UX designers can have a huge impact. In this article, we’ll look at the issues with current apps, and guidelines to ensure UX practitioners are using clinically proven methods for improving mental health treatment.</p>

<p><strong>Here’s What You Need to Know About Color Accessibility in Product Design</strong><br />
https://uxplanet.org/heres-what-you-need-to-know-about-color-accessibility-in-product-design-aecbd0c30628<br />
As a Product Designer at Handsome, I recently worked with a client to create the most complex implementation of an accessible color system that I’ve had a chance to work on, and thought I’d pass along some of my learnings.</p>

<p><strong>Designing a Styleguide: Elements That Go Into Building Compelling Products</strong><br />
https://blog.marvelapp.com/designing-styleguide-elements-building-compelling-products/<br />
The goal of this article is to introduce you to some well-thought-out styleguides and branding guidelines. It also details some of the most important elements every styleguide should have.</p>

<h2 id="section-3">产品及其它</h2>

<p><strong>InVision has no physical headquarters and all 700 employees work remotely</strong><br />
https://www.businessinsider.com/invision-startup-all-employees-work-remotely-2018-9<br />
All 700 employees at this startup work remotely. Here’s why one of its top execs says it’s given them a major edge over the competition.</p>

<p><strong>任正非：告别”完人”预设，拥抱巨大无穷性</strong><br />
https://mp.weixin.qq.com/s/rB4V5RpvgDnksmQJEKR2OA<br />
世间人生百态，许多意见会误导你的人生，经历一次次的吃亏是福，终于到一个节点上你意识到，水往低处流，能量向居下的人聚集。甘居后者反而领先，甘居下者反而为上，谦卑，敬畏，居下，开放，包容，是成就点事最重要的品质。当然世界需要你独一无二的价值！这时，你就走上了回归的道路，回归你真正的天赋天性，回归你为人类创造价值的初心。另附：.</p>

<p><strong>为什么是黄峥？</strong><br />
https://mp.weixin.qq.com/s?__biz=MzUyMDQ5NzI5Mg==&amp;mid=2247499454&amp;idx=1&amp;sn=8685ee7536854a3861a61f9212175181<br />
人的思想很容易被染污的，当人对一件事情做判断的时候，往往要了解背景和事实，之后需要的不是睿智，而是面对事实时是否有勇气依然用理性、用常识来判断。</p>

<p><strong>It doesn’t have to be crazy at work</strong><br />
https://basecamp.com/books/calm<br />
.</p>

<p>– THE END –</p>
---------------
<h1 id="#title_2" >3、文章： 使用反应式领域驱动设计来解决不确定性</h1>
Vaughn Vernon
[http://www.infoq.com/cn/articles/modeling-uncertainty-reactive-ddd?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/modeling-uncertainty-reactive-ddd?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/modeling-uncertainty-reactive-ddd/zh/smallimage/modeling-uncertainty-reactive-ddd-s-1538047373293-1539275383302.jpeg"/><p>Vaughn Vernon撰写了几本关于DDD和反应式消息传递模式的书，并发现分布式系统的本质意味着你必须处理不确定性。如何响应丢失的消息或重复收到的消息应该是一种业务决策，因此必须是领域模型的一部分。</p> <i>By Vaughn Vernon</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_3" >4、文章： 以Chef和Ansible为例快速入门服务器配置</h1>
Stephen Mann
[http://www.infoq.com/cn/articles/a-brief-introduction-to-provisioning?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/a-brief-introduction-to-provisioning?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/a-brief-introduction-to-provisioning/zh/smallimage/LOGO-1511697970292-1539412670095.jpeg"/><p>这篇文章讨论了如何在我们的环境中安装和配置软件，这个任务通常被称为服务器配置（Server Provisioning）。</p> <i>By Stephen Mann</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_4" >5、文章： V神：应用Zcash技术，以太坊能扩展到500tx/s</h1>
CNN
[http://www.infoq.com/cn/articles/ethereum-can-scale-to-500-txs-using-zcash-technology?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/ethereum-can-scale-to-500-txs-using-zcash-technology?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/ethereum-can-scale-to-500-txs-using-zcash-technology/zh/smallimage/apachebeam-small-1539413477914.jpg"/><p>Zcash加持，放飞以太坊不是梦。</p> <i>By CNN</i> <i> Translated by 刘志勇</i>
---------------
<h1 id="#title_5" >6、文章： 为什么DevOps和SRE职位这么难招人？</h1>
张婵
[http://www.infoq.com/cn/articles/why-it-is-hard-to-hire-devops-sre?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/why-it-is-hard-to-hire-devops-sre?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/why-it-is-hard-to-hire-devops-sre/zh/smallimage/14-things-mongoDB-logo-small-1536657216288-1539414120594.jpg"/><p>你的团队的DevOps／SRE职位招聘困难吗？作为DevOps／SRE工程师你在求职过程中感觉也是如此吗？</p> <i>By 张婵</i>
---------------
<h1 id="#title_6" >7、Smart Bundling: How To Serve Legacy Code Only To Legacy Browsers</h1>
Shubham Kanodia
[https://www.smashingmagazine.com/2018/10/smart-bundling-legacy-code-browsers/](https://www.smashingmagazine.com/2018/10/smart-bundling-legacy-code-browsers/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/10/smart-bundling-legacy-code-browsers/" />
              <title>Smart Bundling: How To Serve Legacy Code Only To Legacy Browsers</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>Smart Bundling: How To Serve Legacy Code Only To Legacy Browsers</h1>
                  
                    
                    <address>Shubham Kanodia</address>
                  
                  <time datetime="2018-10-15T14:30:13&#43;02:00" class="op-published">2018-10-15T14:30:13+02:00</time>
                  <time datetime="2018-10-15T22:18:02&#43;00:00" class="op-modified">2018-10-15T22:18:02+00:00</time>
                </header>
                

<p>A website today receives a large chunk of its traffic from evergreen browsers &mdash; most of which have good support for ES6+, new JavaScript standards, new web platform APIs and CSS attributes. However, legacy browsers still need to be supported for the near future &mdash; their usage share is large enough not to be ignored, depending on your user base.</p>

<p>A quick look at ’s usage table reveals that evergreen browsers occupy a lion’s share of the browser market &mdash; more than 75%. In spite of this, the norm is to prefix CSS, transpile all of our JavaScript to ES5, and include polyfills to support every user we care about.</p>

<p>While this is understandable from a historical context &mdash; the web has always been about progressive enhancement &mdash; the question remains: Are we slowing down the web for the majority of our users in order to support a diminishing set of legacy browsers?</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7cd8cff3-2517-4109-9bf4-cae93f62bb9b/01-shipping-a-modern-frontend.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7cd8cff3-2517-4109-9bf4-cae93f62bb9b/01-shipping-a-modern-frontend.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7cd8cff3-2517-4109-9bf4-cae93f62bb9b/01-shipping-a-modern-frontend.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7cd8cff3-2517-4109-9bf4-cae93f62bb9b/01-shipping-a-modern-frontend.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7cd8cff3-2517-4109-9bf4-cae93f62bb9b/01-shipping-a-modern-frontend.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7cd8cff3-2517-4109-9bf4-cae93f62bb9b/01-shipping-a-modern-frontend.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7cd8cff3-2517-4109-9bf4-cae93f62bb9b/01-shipping-a-modern-frontend.png"
			sizes="100vw"
			alt="Transpilation to ES5, web platform polyfills, ES6&#43; polyfills, CSS prefixing"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The different compatibility layers of a web app. ()
		</figcaption>
	
</figure>


<h3 id="the-cost-of-supporting-legacy-browsers">The Cost Of Supporting Legacy Browsers</h3>

<p>Let’s try to understand how different steps in a typical build pipeline can add weight to our front-end resources:</p>

<h4 id="transpiling-to-es5">Transpiling To ES5</h4>

<p>To estimate how much weight transpiling can add to a JavaScript bundle, I took a few popular JavaScript libraries originally written in ES6+ and compared their bundle sizes before and after transpilation:</p>

<p><table class="tablesaw break-out" data-tablesaw-mode="swipe" data-tablesaw-minimap>
  <thead>
<tr>
<th data-tablesaw-priority="persist">Library</th>
<th>Size<br />(minified ES6)</th>
<th>Size<br />(minified ES5)</th>
<th>Difference</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>TodoMVC</strong></td>
<td>8.4 KB</td>
<td>11 KB</td>
<td>24.5%</td>
</tr>
<tr>
<td><strong>Draggable</strong></td>
<td>77.9 KB</td>
<td>53.5 KB</td>
<td>31.3%</td>
</tr>
<tr>
<td><strong>Luxon</strong></td>
<td>75.4 KB</td>
<td>100.3 KB</td>
<td>24.8%</td>
</tr>
<tr>
<td><strong>Video.js</strong></td>
<td>237.2 KB</td>
<td>335.8 KB</td>
<td>29.4%</td>
</tr>
<tr>
<td><strong>PixiJS</strong></td>
<td>370.8 KB</td>
<td>452 KB</td>
<td>18%</td>
</tr>
</tbody>
</table><p></p></p>

<p>On average, untranspiled bundles are about 25% smaller than those that have been transpiled down to ES5. This isn’t surprising given that ES6+ provides a more compact and expressive way to represent the equivalent logic and that transpilation of some of these features to ES5 can require a lot of code.</p>

<h4 id="es6-polyfills">ES6+ Polyfills</h4>

<p>While Babel does a good job of applying syntactical transforms to our ES6+ code,  built-in features introduced in ES6+ &mdash; such as <code>Promise</code>, <code>Map</code> and <code>Set</code>, and new array and string methods &mdash; still need to be polyfilled. Dropping in <code>babel-polyfill</code> as is can add close to 90 KB to your minified bundle.</p>



<aside class="product-panel product-panel__tilted product-panel--book" data-audience="non-subscriber">
    <div class="container product-panel--book__container">
      <div class="panel__description panel__description--book">
    <p>Front-end is messy and complicated these days. That's why we publish  with a growing selection of <strong>front-end&nbsp;&amp;&nbsp;UX goodies</strong>. So you get your work done, better and faster.</p>

      <a href="https://smashed.by/perfpanelmembership" class="btn btn--green btn--large">
        Explore Smashing Membership&nbsp;↬
      </a>
      </div>
      <div class="panel__image panel__image--book">
        <a href="https://smashed.by/perfpanelmembership" class="books__book__image">
        <div class="books__book__img">
          <img src="https://www.smashingmagazine.com/images/smashing-cat/cat-rollerderby.svg" alt="Smashing Cat, just preparing to do some magic stuff." width="310" height="400">
        </div>
      </a>
      </div>
    </div>
  </aside>




<h4 id="web-platform-polyfills">Web Platform Polyfills</h4>

<p>Modern web application development has been simplified due to the availability of a plethora of new browser APIs. Commonly used ones are <code>fetch</code>, for requesting for resources, <code>IntersectionObserver</code>, for efficiently observing the visibility of elements, and the <code>URL</code> specification, which makes reading and manipulation of URLs on the web easier.</p>

<p>Adding a spec-compliant polyfill for each of these features can have a noticeable impact on bundle size.</p>

<h4 id="css-prefixing">CSS Prefixing</h4>

<p>Lastly, let’s look at the impact of CSS prefixing. While prefixes aren’t going to add as much dead weight to bundles as other build transforms do &mdash; especially because they compress well when Gzip’d &mdash; there are still some savings to be achieved here.</p>

<p><table class="tablesaw break-out" data-tablesaw-mode="swipe" data-tablesaw-minimap>
<thead>
<tr>
<th data-tablesaw-priority="persist">Library</th>
<th>Size<br />(minified, prefixed for last 5 browser versions)</th>
<th>Size<br />(minified, prefixed for last browser version)</th>
<th>Difference</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Bootstrap</strong></td>
<td>159 KB</td>
<td>132 KB</td>
<td>17%</td>
</tr>
<tr>
<td><strong>Bulma</strong></td>
<td>184 KB</td>
<td>164 KB</td>
<td>10.9%</td>
</tr>
<tr>
<td><strong>Foundation</strong></td>
<td>139 KB</td>
<td>118 KB</td>
<td>15.1%</td>
</tr>
<tr>
<td><strong>Semantic UI</strong></td>
<td>622 KB</td>
<td>569 KB</td>
<td>8.5%</td>
</tr>
</tbody>
</table><p></p></p>

<h3 id="a-practical-guide-to-shipping-efficient-code">A Practical Guide To Shipping Efficient Code</h3>

<p>It’s probably evident where I’m going with this. If we leverage existing build pipelines to ship these compatibility layers only to browsers that require it, we can deliver a lighter experience to the rest of our users &mdash; those who form a rising majority &mdash; while maintaining compatibility for older browsers.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/73ab53df-3320-4556-bf20-440530dec8a1/modern-vs-legacy.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/73ab53df-3320-4556-bf20-440530dec8a1/modern-vs-legacy.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/73ab53df-3320-4556-bf20-440530dec8a1/modern-vs-legacy.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/73ab53df-3320-4556-bf20-440530dec8a1/modern-vs-legacy.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/73ab53df-3320-4556-bf20-440530dec8a1/modern-vs-legacy.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/73ab53df-3320-4556-bf20-440530dec8a1/modern-vs-legacy.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/73ab53df-3320-4556-bf20-440530dec8a1/modern-vs-legacy.png"
			sizes="100vw"
			alt="The modern bundle is smaller than the legacy bundle because it forgoes some compatibility layers."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Forking our bundles. ()
		</figcaption>
	
</figure>


<p>This idea isn’t entirely new. Services such as  are attempts to dynamically polyfill browser environments at runtime. But approaches such as this suffer from a few shortcomings:</p>

<ul>
<li>The selection of polyfills is limited to those listed by the service &mdash; unless you host and maintain the service yourself.</li>
<li>Because the polyfilling happens at runtime and is a blocking operation, page-loading time can be significantly higher for users on old browsers.</li>
<li>Serving a custom-made polyfill file to every user introduces entropy to the system, which makes troubleshooting harder when things go wrong.</li>
</ul>

<p>Also, this doesn’t solve the problem of weight added by transpilation of the application code, which at times can be larger than the polyfills themselves.</p>

<p>Let see how we can solve for all of the sources of bloat we’ve identified till now.</p>

<div class="sponsors__wide-place"></div>




<h3 id="tools-we-ll-need">Tools We&rsquo;ll Need</h3>

<ul>
<li><strong>Webpack</strong><br />
This will be our build tool, although the process will remain similar to that of other build tools, like Parcel and Rollup.</li>
<li><strong>Browserslist</strong><br />
With this, we’ll manage and define the browsers we&rsquo;d like to support.</li>
<li>And we’ll use some <strong>Browserslist support plugins</strong>.</li>
</ul>

<h3 id="1-defining-modern-and-legacy-browsers">1. Defining Modern And Legacy Browsers</h3>

<p>First, we’ll want to make clear what we mean by “modern” and “legacy” browsers. For ease of maintenance and testing, it helps to divide browsers into two discrete groups: adding browsers that require little to no polyfilling or transpilation to our modern list, and putting the rest on our legacy list.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/97c66848-0e54-4756-ba67-b6fcdee3ef26/modern-browsers.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/97c66848-0e54-4756-ba67-b6fcdee3ef26/modern-browsers.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/97c66848-0e54-4756-ba67-b6fcdee3ef26/modern-browsers.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/97c66848-0e54-4756-ba67-b6fcdee3ef26/modern-browsers.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/97c66848-0e54-4756-ba67-b6fcdee3ef26/modern-browsers.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/97c66848-0e54-4756-ba67-b6fcdee3ef26/modern-browsers.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/97c66848-0e54-4756-ba67-b6fcdee3ef26/modern-browsers.png"
			sizes="100vw"
			alt="Firefox &gt;= 53; Edge &gt;= 15; Chrome &gt;= 58; iOS &gt;= 10.1"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Browsers that support ES6+, new CSS attributes, and browser APIs like Promises and Fetch. ()
		</figcaption>
	
</figure>


<p>A Browserslist configuration at the root of your project can store this information. “Environment” subsections can be used to document the two browser groups, like so:</p>

<pre><code class="language-javascript">[modern]
Firefox >= 53
Edge >= 15
Chrome >= 58
iOS >= 10.1

[legacy]
> 1%
</code></pre>

<p>The list given here is only an example and can be customized and updated based on your website’s requirements and the time available. This configuration will act as the source of truth for the two sets of front-end bundles that we will create next: one for the modern browsers and one for all other users.</p>

<h3 id="2-es6-transpiling-and-polyfilling">2. ES6+ Transpiling And Polyfilling</h3>

<p>To transpile our JavaScript in an environment-aware manner, we’re going to use <code>babel-preset-env</code>.</p>

<p>Let&rsquo;s initialize a <code>.babelrc</code> file at our project’s root with this:</p>

<pre><code class="language-javascript">{
  "presets": [
    ["env", { "useBuiltIns": "entry"}]
  ]
}
</code></pre>

<p>Enabling the <code>useBuiltIns</code> flag allows Babel to selectively polyfill built-in features that were introduced as part of ES6+. Because it filters polyfills to include only the ones required by the environment, we mitigate the cost of shipping with <code>babel-polyfill</code> in its entirety.</p>

<p>For this flag to work, we will also need to import <code>babel-polyfill</code> in our entry point.</p>

<pre><code class="language-css">// In
import "babel-polyfill";
</code></pre>

<p>Doing so will replace the large <code>babel-polyfill</code> import with granular imports, filtered by the browser environment that we’re targeting.</p>

<pre><code class="language-javascript">// Transformed output
import "core-js/modules/es7.string.pad-start";
import "core-js/modules/es7.string.pad-end";
import "core-js/modules/web.timers";
…
</code></pre>

<h3 id="3-polyfilling-web-platform-features">3. Polyfilling Web Platform Features</h3>

<p>To ship polyfills for web platform features to our users, we will need to create two entry points for both environments:</p>

<pre><code class="language-javascript">require('whatwg-fetch');
require('es6-promise').polyfill();
// … other polyfills
</code></pre>  

<p>And this:</p>

<pre><code class="language-javascript">// polyfills for modern browsers (if any)
require('intersection-observer');
</code></pre>

<p>This is the only step in our flow that requires some degree of manual maintenance. We can make this process less error-prone by adding  to the project. This plugin warns us when we use a browser feature that hasn’t been polyfilled yet.</p>

<div class="sponsors__wide-place"></div>




<h3 id="4-css-prefixing">4. CSS Prefixing</h3>

<p>Finally, let’s see how we can cut down on CSS prefixes for browsers that don’t require it. Because <code>autoprefixer</code> was one of the first tools in the ecosystem to support reading from a <code>browserslist</code> configuration file, we don’t have much to do here.</p>

<p>Creating a simple PostCSS configuration file at the project’s root should suffice:</p>

<pre><code class="language-javascript">module.exports = {
  plugins: [ require('autoprefixer') ],
}
</code></pre>

<h3 id="putting-it-all-together">Putting It All Together</h3>

<p>Now that we’ve defined all of the required plugin configurations, we can put together a webpack configuration that reads these and outputs two separate builds in <code>dist/modern</code> and <code>dist/legacy</code> folders.</p>

<pre class="break-out"><code class="language-javascript">const MiniCssExtractPlugin = require('mini-css-extract-plugin')
const isModern = process.env.BROWSERSLIST_ENV === 'modern'
const buildRoot = path.resolve(__dirname, "dist")

module.exports = {
  entry: [
    isModern ? './polyfills.modern.js' : './polyfills.legacy.js',
    "./main.js"
  ],
  output: {
    path: path.join(buildRoot, isModern ? 'modern' : 'legacy'),
    filename: 'bundle.[hash].js',
  },
  module: {
    rules: [
      { test: /\.jsx?$/, use: "babel-loader" },
      {
        test: /\.css$/,
        use: [MiniCssExtractPlugin.loader, 'css-loader', 'postcss-loader']
      }
    ]},
    plugins: {
      new MiniCssExtractPlugin(),
      new HtmlWebpackPlugin({
      template: 'index.hbs',
      filename: 'index.html',
    }),
  },
};
</code></pre>

<p>To finish up, we’ll create a few build commands in our <code>package.json</code> file:</p>

<pre class="break-out"><code class="language-javascript">"scripts": {
  "build": "yarn build:legacy && yarn build:modern",
  "build:legacy": "BROWSERSLIST_ENV=legacy webpack -p --config webpack.config.js",
  "build:modern": "BROWSERSLIST_ENV=modern webpack -p --config webpack.config.js"
}
</code></pre>

<p>That’s it. Running <code>yarn build</code> should now give us two builds, which are equivalent in functionality.</p>

<h3 id="serving-the-right-bundle-to-users">Serving The Right Bundle To Users</h3>

<p>Creating separate builds helps us achieve only the first half of our goal. We still need to identify and serve the right bundle to users.</p>

<p>Remember the Browserslist configuration we defined earlier? Wouldn’t it be nice if we could use the same configuration to determine which category the user falls into?</p>

<p>Enter . As the name suggests, <code>browserslist-useragent</code> can read our <code>browserslist</code> configuration and then match a user agent to the relevant environment. The following example demonstrates this with a Koa server:</p>

<pre class="break-out"><code class="language-javascript">const Koa = require('koa')
const app = new Koa()
const send = require('koa-send')
const { matchesUA } = require('browserslist-useragent')
var router = new Router()

app.use(router.routes())

router.get('/', async (ctx, next) => {
  const useragent = ctx.get('User-Agent')  
  const isModernUser = matchesUA(useragent, {
      env: 'modern',
      allowHigherVersions: true,
   })
   const index = isModernUser ? 'dist/modern/index.html', 'dist/legacy/index.html'
   await send(ctx, index);
});
</code></pre>

<p>Here, setting the <code>allowHigherVersions</code> flag ensures that if newer versions of a browser are released &mdash; ones that are not yet a part of Can I Use’s database &mdash; they will still report as truthy for modern browsers.</p>

<p>One of <code>browserslist-useragent</code>&rsquo;s functions is to ensure that platform quirks are taken into account while matching user agents. For example, all browsers on iOS (including Chrome) use WebKit as the underlying engine and will be matched to the respective Safari-specific Browserslist query.</p>

<p>It might not be prudent to rely solely on the correctness of user-agent parsing in production. By falling back to the legacy bundle for browsers that aren’t defined in the modern list or that have unknown or unparseable user-agent strings, we ensure that our website still works.</p>

<h3 id="conclusion-is-it-worth-it">Conclusion: Is It Worth It?</h3>

<p>We have managed to cover an end-to-end flow for shipping bloat-free bundles to our clients. But it’s only reasonable to wonder whether the maintenance overhead this adds to a project is worth its benefits. Let’s evaluate the pros and cons of this approach:</p>

<h4 id="1-maintenance-and-testing">1. Maintenance And Testing</h4>

<p>One is required to maintain only a single Browserslist configuration that powers all of the tools in this pipeline. Updating the definitions of modern and legacy browsers can be done anytime in the future without having to refactor supporting configurations or code. I’d argue that this makes the maintenance overhead almost negligible.</p>

<p>There is, however, a small theoretical risk associated with relying on Babel to produce two different code bundles, each of which needs to work fine in its respective environment.</p>

<p>While errors due to differences in bundles might be rare, monitoring these variants for errors should help to identify and effectively mitigate any issues.</p>

<h4 id="2-build-time-vs-runtime">2. Build Time vs. Runtime</h4>

<p>Unlike other techniques prevalent today, all of these optimizations occur at build time and are invisible to the client.</p>

<h4 id="3-progressively-enhanced-speed">3. Progressively Enhanced Speed</h4>

<p>The experience of users on modern browsers becomes significantly faster, while users on legacy browsers continue to get served the same bundle as before, without any negative consequences.</p>

<h4 id="4-using-modern-browser-features-with-ease">4. Using Modern Browser Features With Ease</h4>

<p>We often avoid using new browser features due to the size of polyfills required to use them. At times, we even choose smaller non-spec-compliant polyfills to save on size. This new approach allows us to use spec-compliant polyfills without worrying much about affecting all users.</p>

<h3 id="differential-bundle-serving-in-production">Differential Bundle Serving In Production</h3>

<p>Given the significant advantages, we adopted this build pipeline when creating a new mobile checkout experience for customers of Urban Ladder, one of India’s largest furniture and decor retailers.</p>

<p>In our already optimized bundle, we were able to squeeze savings of approximately 20% on the Gzip’d CSS and JavaScript resources sent down the wire to modern mobile users. Because more than 80% of our daily visitors were on these evergreen browsers, the effort put in was well worth the impact.</p>

<h4 id="further-resources">Further Resources</h4>

<ul>
<li>“”, Philip Walton</li>
<li><br />
A smart Babel preset</li>
<li><br />
Ecosystem of plugins built for Browserslist</li>
<li><br />
Current browser marketshare table</li>
</ul>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(dm, ra, yk, il, al)</span>
</div>


              </article>
            </body>
          </html>
---------------
<h1 id="#title_7" >8、ChaosConf 2018：混沌实验的演变</h1>
Daniel Bryant
[http://www.infoq.com/cn/news/2018/10/chaosconf-evolution?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/10/chaosconf-evolution?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>在美国旧金山举行的首届ChaosConf大会上，Kolton Andrus做了一个有关混沌实验在过去八年中如何演变的演讲。他认为，与处理故障有关的人力和组织方面的内容不应该被忽略，并建议工具应该支持应用程序和请求级别的故障注入测试，以便最小化潜在的故障影响范围。</p> <i>By Daniel Bryant</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_8" >9、微软宣布针对Azure Cosmos DB的多个更新</h1>
Eldert Grootenboer
[http://www.infoq.com/cn/news/2018/10/updates-azure-cosmos-db?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/10/updates-azure-cosmos-db?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>微软宣布了针对Azure Cosmos DB的多个更新。Azure Cosmos DB微软的分布式、可大规模扩展的多模型数据库服务。发布公告中包含了支持全球规模多主节点的特性、新增Cassandra支持API以及可降低成本的预留容量模型。</p> <i>By Eldert Grootenboer</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_9" >10、Visual Studio 2017 15.9预览版3支持ARM64 for UWP</h1>
Jeff Martin
[http://www.infoq.com/cn/news/2018/10/vs2017-159-preview3?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/10/vs2017-159-preview3?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>微软针对Visual Studio 2017 15.9的更新工作还在继续。在15.9的第三个预览版中，微软宣布支持ARM64平台上的UWP应用程序，并扩展了TypeScript开发人员可以使用的功能。和通常的情况一样，该版本还包含了大量的修复程序。</p> <i>By Jeff Martin</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_10" >11、Oracle推出轻量级Java微服务框架Helidon</h1>
Michael Redlich
[http://www.infoq.com/cn/news/2018/10/oracle-introduces-helidon?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/10/oracle-introduces-helidon?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>近日，Oracle推出了一个新的开源框架Helidon，该项目是一个用于创建基于微服务的应用程序的Java库集合。Helidon加入了MicroProfile家族，并实现了MicroProfile 1.1规范。Oracle的高级软件开发经理Dmitry Kornilov向infoQ介绍了这个新项目。</p> <i>By Michael Redlich</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_11" >12、Kafka落选！InfoWorld最佳开源数据平台奖公布</h1>
InfoWorld
[http://www.infoq.com/cn/news/2018/10/the-best-open-source-database?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/10/the-best-open-source-database?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>在现如今，没有比数据更大的东西存在了！我们有比以前多很多的数据，我们有更多方式来存储和分析数据：SQL数据库、NoSQL数据库、分布式OLTP数据库，分部署OLAP平台、分布式混OLTP/OLAP平台。2018年Bossie奖数据库和数据分析平台获得者包括在流处理运算方面的创新者。</p> <i>By InfoWorld</i> <i> Translated by 刘嘉洋</i>
---------------