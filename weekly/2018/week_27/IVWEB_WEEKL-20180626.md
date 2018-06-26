## 文章索引
1、 <a href="#1fex-技术周刊---2018/06/25" >FEX 技术周刊 - 2018/06/25</a><br/>
2、 <a href="#2what-newsletters-should-designers-and-developers-be-subscribing-to" >What Newsletters Should Designers And Developers Be Subscribing To?</a><br/>
3、 <a href="#3tgo-鲲鹏会台北分会成立继续推动两岸科技交融" >TGO 鲲鹏会台北分会成立，继续推动两岸科技交融</a><br/>
4、 <a href="#4文章-aiops实践思考aiops如何与apm结合" >文章： AIOps实践思考：AIOps如何与APM结合？</a><br/>
5、 <a href="#5firefox重生" >Firefox重生</a><br/>
6、 <a href="#6为高效团队制作游戏" >为高效团队制作游戏</a><br/>
7、 <a href="#7opsramp推出aiops推理引擎" >OpsRamp推出AIOps推理引擎</a><br/>
8、 <a href="#8fake-5提供net-core支持" >Fake 5提供.NET Core支持</a><br/>
9、 <a href="#9opsramp宣布统一服务发现" >OpsRamp宣布统一服务发现</a><br/><h1 id="#title_0" >1、FEX 技术周刊 - 2018/06/25</h1>

[http://fex.baidu.com/blog/2018/06/fex-weekly-25//](http://fex.baidu.com/blog/2018/06/fex-weekly-25//)
作者：zhangtao <br> <h2 id="section">业界会议</h2>

<p><strong>GMTC2018全球大前端技术大会</strong><br />
https://gmtc.geekbang.org/<br />
前端会议越来越高大上了，在会上 
https://www.leiphone.com/news/201806/wLTnCxTerrrMKbxO.html</p>

<h2 id="section-1">深阅读</h2>

<p><strong>V8 release v6.8</strong><br />
https://v8project.blogspot.com/2018/06/v8-release-68.html<br />
his post provides a preview of some of the highlights in anticipation of the release. In parallel we have reduced the memory consumption of SFIs themselves, removing unnecessary fields or compressing them where possible, and decreased their size by ~25%, with further reductions coming in future releases. In V8 v6.8 you can start using trap-based bounds checking on Linux x64 platforms. Performance improvements: Array destructuring, Object.assign, TypedArray.prototype.sort.</p>

<p><strong>The Cost Of JavaScript - Addy Osmani</strong><br />
https://www.youtube.com/watch?v=63I-mEuSvGA<br />
Addy Osmani explains how and why JavaScript is the most expensive resource your site uses today—especially on mobile. Addy also shares tips for fixing JavaScript performance issues so everything loads quicker. A little discipline can help if you want your site to load and be interactive as soon as possible on mobile. As a result, moving forward, we are sunsetting React Native at Airbnb and reinvesting all of our efforts back into native, 见 </p>

<p><strong>Github Stars !== Usage: React is still blowing Vue and Angular Away</strong><br />
https://zendev.com/2018/06/19/react-usage-beating-vue-angular.html<br />
By digging into the NPM download statistics, we find that despite the hype around Vue’s skyrocketing github stars, React is still the 800 pound gorilla in the JavaScript framework space. It is about to cross the mammoth 10 million downloads per month, and has been growing at a torrid rate.</p>

<p><strong>Using JavaScript modules on the web</strong><br />
https://developers.google.com/web/fundamentals/primers/modules<br />
JavaScript modules are now supported in all major browsers! This article explains how to use JS modules, how to deploy them responsibly, and how the Chrome team is working to make modules even better in the future.</p>

<p><strong>Picasso 开启大前端的未来</strong><br />
https://tech.meituan.com/picasso_the_future.html<br />
Picasso是大众点评移动研发团队自研的高性能跨平台动态化框架，经过两年多的孕育和发展，目前在美团多个事业群已经实现了大规模的应用。 Picasso源自我们对大前端实践的重新思考，以简洁高效的架构达成高性能的页面渲染目标。在实践中，甚至可以把Native技术向Picasso技术的迁移当做一种性能优化手段；与此同时，Picasso在跨越小程序端和Web端方面的工作已经取得了突破性进展，有望在四端（Android、iOS、H5、微信小程序）统一大前端实践的基础之上，达成高性能大前端实践，同时配合Picasso布局DSL强表达能力和Picasso代码生成技术，可以进一步提升生产力。</p>

<p><strong>SpriteJS —— Canvas动画从未如此简单</strong><br />
https://www.h5jun.com/post/spritejs.html<br />
奇舞团团长月影亲自操刀，360开源又一力作——spriteJS，实现酷炫的数据可视化，让canvas动画制作变得 so easy 实现你的动画梦。SpriteJS是一款由360奇舞团开源的跨终端canvas绘图库，可以基于canvas快速绘制结构化UI、动画和交互效果，并发布到任何拥有canvas环境的平台上（比如浏览器、小程序和node）。</p>

<p><strong>前端开发-领域驱动设计</strong><br />
https://yuque.com/mayiprototeam/gfyt69/oq14ia<br />
随着我们解决的场景越来越专业化和复杂化，大型SPA应用的流行，前端承担的职责越来越多。代码的质量和系统的完整性越来越难把握。很容易导致迭代着迭代着发现代码改不动了。最后只能新起炉灶，重新开发。归根到底在于复杂度的失控，本文会尝试分析其中的问题以及从前端如何应用领域模型开发的角度给出一些建议。</p>

<p><strong>WWDC2018 - 来自一线开发者的技术笔记</strong><br />
https://techblog.toutiao.com/2018/06/19/untitled-49/<br />
感谢头条的同学的分享。</p>

<p><strong>React Native at Airbnb</strong><br />
https://medium.com/airbnb-engineering/react-native-at-airbnb-f95aa460be1c<br />
In 2016, we took a big bet on React Native. Different teams had a wide range of experiences with React Native. React Native proved to be an incredible tool at times while posing technical and organizational challenges in others. In this series, we provide a detailed account of our experiences with it and what we’re doing next.</p>

<p><strong>How JavaScript works: the internals of Shadow DOM + how to build self-contained components</strong><br />
https://blog.sessionstack.com/how-javascript-works-the-internals-of-shadow-dom-how-to-build-self-contained-components-244331c4de6e<br />
Web Components is a suite of different technologies that allows you to create reusable custom elements.Their functionality is encapsulated away from the rest of your code, and you can utilize them in your web apps. There are 4 Web Component standards: Shadow DOM, HTML Templates, Custom elements, HTML Imports. In this article, we’ll focus on the Shadow DOM.</p>

<p><strong>End-to-end testing Single Page Apps and Node.js APIs with Cucumber.js and Puppeteer</strong><br />
https://medium.com/@anephenix/end-to-end-testing-single-page-apps-and-node-js-apis-with-cucumber-js-and-puppeteer-ad5a519ace0<br />
Single Page Apps are a popular approach to building web applications, but testing them in an end-to-end fashion is not simple; you need to load the backend (potentially a collection of APIs and databases), and make sure that the combination of the SPA and APIs works as expected. The good news is that there is a way to do this, and in this article we will show you how, using a Behaviour-Driven-Development tool called Cucumber.js, and Google’s web browser library Puppeteer. If you develop Node.js web applications and want to use E2E testing for them but don’t know how, then this article is for you.</p>

<p><strong>MySQL High Availability at GitHub</strong><br />
https://githubengineering.com/mysql-high-availability-at-github/<br />
GitHub uses MySQL as its main datastore for all things non-git, and its availability is critical to GitHub’s operation. The site itself, GitHub’s API, authentication and more, all require database access. This post illustrates GitHub’s MySQL high availability and master service discovery solution, which allows us to reliably run a cross-data-center operation, be tolerant of data center isolation, and achieve short outage times on a failure. 另附：</p>

<p><strong>Post Inspector: A Tool to Optimize Content Sharing</strong><br />
https://engineering.linkedin.com/blog/2018/06/post-inspector--a-tool-to-optimize-content-sharing<br />
The Content Ingestion team at LinkedIn primarily focuses on discovering content across the web and ingesting it into the LinkedIn content ecosystem. Not only do we ingest content whenever a member shares a URL, but we also proactively search for interesting content that our members could enjoy. Given the team’s focus, we’ve created a tool—called Post Inspector—for external content providers and internal teams at LinkedIn that provides insight into how we extract metadata so that content providers can easily optimize the sharing experience of their content on the LinkedIn platform.</p>

<p><strong>Growth Engineering at Netflix — Accelerating Innovation</strong><br />
https://medium.com/netflix-techblog/growth-engineering-at-netflix-accelerating-innovation-90eb8e70ce59<br />
The customer experience is remarkably different in each of these cases, but the goal is the same. We seek to offer the best possible signup experience to our prospective members while at the same time, remaining extremely lean, agile and efficient in our implementation of these disparate experiences. Offering an amazing signup experience for thousands of devices in over 190 countries is an incredibly challenging and rewarding task.</p>

<p><strong>Fibonacci Hashing: The Optimization that the World Forgot</strong><br />
https://probablydance.com/2018/06/16/fibonacci-hashing-the-optimization-that-the-world-forgot-or-a-better-alternative-to-integer-modulo/<br />
Hash tables should not be prime number sized and they should not use an integer modulo to map hashes into slots. Fibonacci hashing is just better. Yet somehow nobody is using it and lots of big hash tables (including all the big implementations of std::unordered_map) are much slower than they should be because they don’t use Fibonacci Hashing. So let’s figure this out. 另附：</p>

<h2 id="section-2">新鲜货</h2>

<p><strong>Hello, Pulumi - Get Code to the Cloud. Faster. Together.</strong><br />
http://joeduffyblog.com/2018/06/18/hello-pulumi/<br />
 is multi-language, multi-cloud, and fully extensible. On day one, it supports JavaScript, TypeScript, Python, and Go languages, and AWS, Azure, and GCP clouds, in addition to Kubernetes targeting any public, private, or hybrid cloud. Pulumi delivers a single, consistent programming model and set of tools to program and manage any of these environments, supported by a rich ecosystem of reusable packages. Using real languages changes everything.</p>

<p><strong>GitLab 11.0 released with Auto DevOps and License Management</strong><br />
https://about.gitlab.com/2018/06/22/gitlab-11-0-released/<br />
Auto DevOps is a pre-built, fully featured CI/CD pipeline that automates the entire delivery process. It is Generally Available and ready for prime time in GitLab 11.0. Other key features we have released in GitLab 11.0 include License Management to automatically detect licenses of your project’s dependencies; enhanced Security Testing of your code, containers, and dependencies; further Kubernetes integration features; an enhanced Web IDE; enhanced Epic and Roadmap views; Incremental Rollouts; and much more.</p>

<p><strong>Announcing GitHub for Unity 1.0</strong><br />
https://blog.github.com/2018-06-18-announcing-github-for-unity-1.0/<br />
GitHub for Unity is a Unity editor extension that brings Git into Unity 5.6, 2017.x, and 2018.x with an integrated sign-in experience for GitHub users. It introduces two key features for game development teams: support for large files using Git LFS and file locking. These features allow you to manage large assets and critical scene files using Git in the same way that you manage code files, all within Unity.</p>

<p><strong>Announcing Microsoft Research Open Data</strong><br />
https://www.microsoft.com/en-us/research/blog/announcing-microsoft-research-open-data-datasets-by-microsoft-research-now-available-in-the-cloud/<br />
We are excited to launch  – a new data repository in the cloud dedicated to facilitating collaboration across the global research community. Microsoft Research Open Data, in a single, convenient, cloud-hosted location, offers datasets representing many years of data curation and research efforts by Microsoft that were used in published research studies.</p>

<p><strong>Web Animations in WebKit</strong><br />
https://webkit.org/blog/8343/web-animations-in-webkit/<br />
Over the last 8 months we have been working on adding support for Web Animations, a W3C standard offering Web developers a JavaScript API to create, query and controls animations. While there is work left to do to ship this experimental feature to the Web at large, we feel our implementation has matured enough that, with the release of Safari Technology Preview 59, we can turn Web Animations on by default for our Web developer audience.</p>

<p><strong>W3C Strategic Highlights May 2018</strong><br />
https://www.w3.org/2018/05/w3c-highlights/<br />
This report gives an overview of recent highlights and work of consolidation, optimization, enhancement of the existing landscape, innovation, incubation, research, and the 2018 W3C Road-map for the Web.</p>

<p><strong>GlslEditor</strong><br />
https://github.com/patriciogonzalezvivo/glslEditor<br />
Friendly GLSL Shader editor based on Codemirror compatible with glslViewer (C++/OpenGL ES) and glslCanvas (JS/WebGL). Was originaly develop to work as a embebed editor for . But now have grown as a stand alone Web app. Thanks to their compatibility with other apps of this ecosystems like glslViewer that runs in the RaspberryPi directly from console, GlslEditor interact with other projects like OpenFrame.io allowing the user to export the shaders to frames with only one button.  The Book of Shaders 这本书很棒，教程典范。</p>

<p><strong>Sails 1.0</strong><br />
https://sailsjs.com/<br />
Sails makes it easy to build custom, enterprise-grade Node.js apps. Build practical, production-ready Node.js apps in a matter of weeks, not months. 
Sails is the most popular MVC framework for Node.js, designed to emulate the familiar MVC pattern of frameworks like Ruby on Rails, but with support for the requirements of modern apps: data-driven APIs with a scalable, service-oriented architecture.</p>

<p><strong>billboard.js V1.5</strong><br />
https://github.com/naver/billboard.js<br />
billboard.js is a re-usable, easy interface JavaScript chart library, based on D3 v4+.</p>

<p><strong>Material Dashboard</strong><br />
https://github.com/creativetimofficial/material-dashboard<br />
Material Dashboard - Open Source Bootstrap 4 Material Design Admin. 竟然同时 支持 VUE、React、Angular.</p>

<p><strong>React Lifecycle Visualizer</strong><br />
https://github.com/Oblosys/react-lifecycle-visualizer<br />
An npm package (react-lifecycle-visualizer) for tracing &amp; visualizing lifecycle methods of arbitrary React components.</p>

<p><strong>React Final Form</strong><br />
https://github.com/final-form/react-final-form<br />
High performance subscription-based form state management for React.</p>

<p><strong>Gatsby v2 beta launch</strong><br />
https://www.gatsbyjs.org/blog/2018-06-16-announcing-gatsby-v2-beta-launch/<br />
 : Blazing-fast static site generator for React.</p>

<p><strong>css-doodle</strong><br />
https://css-doodle.com/<br />
A web component for drawing patterns with CSS. 附：</p>

<p><strong>Bitsrc</strong><br />
https://bitsrc.io/<br />
Imagine all your components organized on the cloud, made discoverable for your team and synced in all your projects. That’s Bit.</p>

<p><strong>ActorDB - A distributed SQL database</strong><br />
https://github.com/biokoda/actordb<br />
With the scalability of a KV store, while keeping the query capabilities of a relational database. ActorDB is ideal as a server side database for apps. Think of running a large mail service, dropbox, evernote, etc. They all require server side storage for user data, but the vast majority of queries is within a specific user. With many users, the server side database can get very large. Using ActorDB you can keep a full relational database for every user and not be forced into painful scaling strategies that require you to throw away everything that makes relational databases good.</p>

<p><strong>GraalVM - Run Programs Faster Anywhere</strong><br />
https://www.graalvm.org/<br />
GraalVM is a universal virtual machine for running applications written in JavaScript, Python, Ruby, R, JVM-based languages like Java, Scala, Kotlin, and LLVM-based languages such as C and C++. GraalVM removes the isolation between programming languages and enables interoperability in a shared runtime. It can run either standalone or in the context of OpenJDK, Node.js, Oracle Database, or MySQL.</p>

<p><strong>Gravity</strong><br />
https://marcobambini.github.io/gravity/#/README<br />
Gravity is a powerful, dynamically typed, lightweight, embeddable programming language written in C without any external dependencies (except for stdlib). It is a class-based concurrent scripting language with a modern Swift like syntax. Gravity supports procedural programming, object-oriented programming, functional programming and data-driven programming. Thanks to special built-in methods, it can also be used as a prototype-based programming language. Gravity has been developed from scratch for the Creo project in order to offer an easy way to write portable code for the iOS and Android platforms.</p>

<h2 id="section-3">设计</h2>

<p><strong>Don’t Use The Placeholder Attribute</strong><br />
https://www.smashingmagazine.com/2018/06/placeholder-attribute/<br />
The placeholder attribute contains a surprising amount of issues that prevent it from delivering on what it promises. Let’s clarify why you need to stop using it.</p>

<p><strong>Introducing Inspect: Where the file is the design spec</strong><br />
https://www.goabstract.com/blog/introducing-inspect-where-the-file-is-the-design-spec/<br />
We’re proud to announce Inspect, an easy way for engineers to quickly gather all the information they need to implement any design. Since Inspect is built on top of our versioning system, designers never need to upload the latest version of a file, and engineers no longer have to worry about referencing an outdated design. With Abstract, you always have the latest version at hand—on the web or in the desktop app. 另附：.</p>

<p><strong>How to scale product design with DesignOps</strong><br />
https://www.invisionapp.com/blog/scale-product-design-designops/<br />
The role of design operations, also known as DesignOps, is becoming more and more important as the fields of design and technology become increasingly integrated. It primarily refers to the practice of developing a more efficient design workflow process in organizations. DesignOps can be defined as a collaboration between design, technology, and engineering teams that streamlines and advances the design workflow process in an organization. 另附：</p>

<p><strong>Interface Exploration: Depth and Color</strong><br />
https://blog.marvelapp.com/interface-exploration-depth-color/<br />
Over the last decade, interface design has seen a turn from replication of the physical/material (referred to as skeuomorphism) to a much more flat, abstract aesthetic. While this new visual style appears more appealing, I’ve felt that a sense of intuition and approachability has been lost by discarding some skeuomorphic characteristics. In order to further explore these observations, I endeavored to visualize a future interface that finds a balance between minimalism and physical context, for a future that will further enable people to interact with seamless slabs of glass and simulate tactile buttons.</p>

<p><strong>Using design to make hard life choices</strong><br />
https://blog.prototypr.io/using-design-to-make-hard-life-choices-e660ebedfe3c<br />
When we ask for advice on these tough problems, our friends and family sometimes tell us things like “you’ll just know when things are right” or “find what works for you!” Of course, these just make us feel worse. Eventually we may convince ourselves this is just how things are supposed to be. Life is hard, problems are hard, and others have success because they had the right “blocks” close at hand (which certainly helps, but is rarer than we like to think). Being a little sad about life is normal, right? I think it’s wrong. The biggest parts of your life are not supposed to make you feel bad.</p>

<p><strong>Enhancing Quora’s messaging UX</strong><br />
https://uxdesign.cc/enhancing-quora-messages-ux-2750e5c2a068<br />
Streamlining the process of exchanging messages on world’s largest knowledge sharing platform.</p>

<h2 id="section-4">产品及其它</h2>

<p><strong>GitHub Education</strong><br />
https://blog.github.com/2018-06-19-announcing-github-education/<br />
Turning today’s students into tomorrow’s technologists with , a free program for schools. GitHub Education includes access to GitHub, an ever-growing suite of developer tools in the Student Developer Pack, workflows for teachers in GitHub Classroom, and training through Campus Experts and Campus Advisors.</p>

<p><strong>Reddit - Introducing the News tab</strong><br />
https://redditblog.com/2018/06/20/introducing-the-news-tab/<br />
The News tab offers a home for content that the community surfaces from communities that frequently share and engage with the news. We began the process of identifying them by first looking at the subreddits where news is sourced and engaged with most.</p>

<p><strong>傅盛：“超级复杂时代”来临，思维成长最重要</strong><br />
https://mp.weixin.qq.com/s?__biz=MjM5NjgzMzkwMQ==&amp;mid=2653646952&amp;idx=1&amp;sn=a198408eccd0085c67c3d32c5cf22c1f<br />
移动互联网的格局战争基本结束，正在变成基础产业，新产业将会崛起。后来，我慢慢意识到——跨界融合、新技术、新应用是未来时代最大的机会。今天有一个非常流行的词汇叫“VUCA时代”，表示当今时代显现出“从复杂到超级复杂”的特征。其实VUCA是四个英语单词的对应：易变性、不确定性、复杂性、模糊性。这四个特性，也是这个时代非常鲜明的写照。这个时代，其实已经不是单一面，而是从复杂到超级复杂的时代。人们越来越焦虑，学习心态变得越来越重要。</p>

<p><strong>微软复兴 - 每一个人到达某一个点时，都应点击刷新</strong><br />
https://mp.weixin.qq.com/s?__biz=MzIxNTAzNzU0Ng==&amp;mid=2654601987&amp;idx=1&amp;sn=e0ab6c7feaaa2a428f94c8d381f02ccb<br />
任何企业最后一定会遭遇成熟期，会陷入到非连续性的窘境，会遭遇到阿喀琉斯之踵。这时，原本帮助企业进步、成长的企业文化，反而成为最限制成长的枷锁。我们把它叫做“企业心智枷锁”。大公司转型非常困难，有没有成功的经验？刷新微软。但是这个案例太难了，要费非常大的力气才能做到。正因为它难，一旦形成之后，非常神奇，而且它的改革者本人是内部的职业经理人。</p>

<p>– THE END –</p>
---------------
<h1 id="#title_1" >2、What Newsletters Should Designers And Developers Be Subscribing To?</h1>
Ricky Onsman
[https://www.smashingmagazine.com/2018/06/newsletters-for-designers-and-developers/](https://www.smashingmagazine.com/2018/06/newsletters-for-designers-and-developers/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/06/newsletters-for-designers-and-developers/" />
              <title>What Newsletters Should Designers And Developers Be Subscribing To?</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>What Newsletters Should Designers And Developers Be Subscribing To?</h1>
                  
                    
                    <address>Ricky Onsman</address>
                  
                  <time datetime="2018-06-25T14:00:48&#43;02:00" class="op-published">2018-06-25T14:00:48+02:00</time>
                  <time datetime="2018-06-25T21:44:16&#43;00:00" class="op-modified">2018-06-25T21:44:16+00:00</time>
                </header>
                <p>We put out the call on : “What email newsletters are you following these days?” The task of compiling your (many, many) responses has fallen to me.</p>

<p>I should disclose that I have a vested interest in that I currently edit a bi-weekly email newsletter for a conference organizer, UX Australia. In fact, over the years, I’ve edited dozens of email newsletters &mdash; some more successful than others.</p>

<p>Anyway, for the purpose of this article, we need to make a few things clear.</p>

<p>First, the newsletters that were most namechecked are included here in their own section: “The Favorites.” The eight that made this list comprise a formidable toolkit of newsletters for any web designer or front-end developer.</p>

<p>Second, I found that there are several types of newsletters which I tried to include representatively:</p>

<ul>
<li>Aggregated links</li>
<li>Editorial</li>
<li>Company/product/service/event promotions</li>
<li>Tutorials</li>
<li>Broad industry news</li>
<li>Specific tech news</li>
<li>Combination of any of the above</li>
</ul>

<p>Third, there is a <em>lot</em> of overlap in linked content from one newsletter to the next. That’s to be expected when everyone wants to break news and aggregate link-worthy articles.</p>

<p>Fourth, I focused on great newsletter content. It could be presented as sophisticated HTML with videos and infographics, or it could be no nonsense plain text with minimal descriptions, as long as the content &mdash; including how reliable any links are &mdash; is good.</p>



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




<p>Lastly, I tried to keep the focus to only actual newsletters that arrive in your email inbox, and that focus on what web designers and developers do. That’s not to deny the value of newsletters that give designers and devs a broader <em>context</em> for their work; I just had to draw the line somewhere.</p>

<p>I also excluded newsletters that claim to be bi-weekly but have produced just four issues in the last nine months (even if those four issues were very good) and “occasional updates.”</p>

<p>So, let’s see what we have. Buckle up.</p>

<ul>
<li></li>
<li></li>
<li></li>
<li></li>
<li></li>
<li></li>
<li></li>
<li></li>
<li></li>
<li></li>
<li></li>
<li></li>
<li></li>
</ul> 

<h3 id="#the-favorites">The Favorites</h3>

<h4></h4>

<p>Well, of course a lot of people mentioned our own newsletter, and we’re proud and grateful for our readers’ loyalty. I’ll also point out that ours is a rare example of all of the types of newsletter mentioned above, and one with a strong, clear voice. Just sayin’. Twice a month.</p>

<h4></h4>

<p> CMS. Weekly.</p>

<h4></h4>

<p> and his team regularly pull out new insights and clever styling techniques. Weekly.</p>

<h4><a href="https://css-weekly.com/">CSS Weekly </a></h4>

<p><a href="https://css-weekly.com/"><img style="float: right; padding: 1em;" src="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ceabcdfc-7d50-4aed-b1b0-ecc6d61234a0/roundup-newsletters-cssweekly.jpg" width="180" height="180" alt="CSS Weekly " /></a>Front-end dev ’s hand-picked selection of CSS new, views, tips and techniques from a very wide range of sources, on everything from Unicode patterns to accessibility to security and query feature management. Weekly.</p>

<h4></h4>

<p> of the same name, but the editorial comments are great value in themselves. Monthly. </p>

<h4></h4>

<p>. Highly readable.</p>
 

<h4></h4>

<p>. A clearly defined balance of articles, tools & resources, media, portfolios and news &mdash; all focused on UX design. Has the twin virtues of feeling hand-picked and providing a great range of topics. Weekly.</p>

<h4></h4>

<p> family of publications, this is one of their strongest newsletters, a well chosen round-up of JS news and articles. The first set of article links get a brief and relevant paragraph description, while the rest are divided into Jobs, Tutorials, Opinions, Videos, Code and Tools with one line descriptions. Comprehensive and readable. Weekly.</p>

<h3 id="accessibility">Accessibility</h3>

<h4></h4>

<p>, is an accessibility evangelist, and compiles this very useful dose of links to web accessibility news, resources, tools and tutorials. Weekly.</p>

<h4></h4>

<p>WebAIM has become a major and reliable resource for guidance and discussion relating to web accessibility. The newsletter includes featured articles, technical tips, resources, and questions from WebAIM's discussion forum. The featured articles are both from WebAIM staff and key web accessibility figures around the world. Monthly.</p>

<h3 id="animation">Animation</h3>

<h4></h4>

<p>. Weekly.</p>

<h4></h4>

<p>A hand-picked selection of articles, videos, book reviews, and other goodies pertaining to the wonderful worlds of web animation and motion design (which until last month was called “Web Animation Weekly”). It’s Rachel Nabors’ project, but the hands doing the picking belong to a range of guest editors who can be nominated by readers. Monthly.</p>

<h3 id="email">Email</h3>

<h4></h4>

<p>RGE aims to be “the best showcase of email design and resources on the web”. A 3,300 strong gallery of examples, excellent articles, and links to a lot of resources suggest they really might be “the epicenter of the email earthquake, but in a good and happy-shakey kind of way.” You’d expect this lot to have a good newsletter, and they do. Monthly.</p>

<h4><a href="http://emailweekly.co/">#emailweekly </a></h4>

<p><a href="http://emailweekly.co/"><img style="float: right; padding: 1em;" src="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1bb85ff8-27fd-4403-9140-15ef55abec4c/roundup-newsletters-emailweekly.jpg" width="180" height="180" alt="#emailweekly " /></a>Email design and strategy studio ’s very useful collection of links to articles on design, HTML and creative concepts for email drawn from their own work and other pros in the field. Weekly. </p>

<h3 id="emerging-technology">Emerging Technology</h3>

<h4></h4>

<p>, this is very well organized and aims to keep web developers inspired and in the know, with links to the latest in VR, AR, wearables, the Internet of Things, AI, robotics and all sorts of other new and emerging tech. Weekly.</p>

<h3 id="front-end">Front-End</h3>

<h4><a href="https://zendev.com/friday-frontend.html">Friday Front-end </a></h4>

<p><a href="https://zendev.com/friday-frontend.html"><img style="float: right; padding: 1em;" src="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e1e147cf-3646-4910-b0fa-8bac62136ea3/roundup-newsletters-fridayfront-end.jpg" width="180" height="180" alt="Friday Front-end " /></a> covers CSS-focused developments, industry news, tutorials and dev resources. Each newsletter has an intro from Kball followed by three sections: CSS, JavaScript, and Other Awesomeness (each with five items with handcrafted descriptions). Weekly.</p>

<h4></h4>

<p> tweets a daily link to an interesting front-end article. At the end of the working week, these links are packed with a short description into an email. The selection is a thoughtful mix, so it feels less like a bunch of random links and more like a summary of key stories. Weekly.</p>

<h4><a href="https://frontendfoc.us/">Frontend Focus </a></h4>

<p><a href="https://frontendfoc.us/"><img style="float: right; padding: 1em;" src="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4d152eb1-c3e9-4a53-80bc-12b57d6dc932/roundup-newsletters-frontendfocus.jpg" width="180" height="180" alt="Frontend Focus " /></a>Just one of a suite of targeted publications by . This one focuses on HTML, CSS, WebGL, Canvas and front end-related news updates, articles and tutorials. Others cover JavaScript, Ruby, databases, mobile and more. Weekly.</p>

<h4></h4>

<p>, that will help you to stay on top of all things web design and front end development. Links to tips & tricks, in depth articles, interviews, tools & resources, jobs and the occasional quirky story. Weekly.</p>

<h4></h4>

<p>. Each issue features a brief tip or tutorial, followed by a round-up of apps, scripts, plugins, and other resources to help front-end developers solve problems and be more productive. Weekly.</p>

<h4></h4>

<p>. Site visitors vote up articles linked to from the feed. The newsletter is a list of the top 10 voted most recent articles. Topics are what you’d expect: CSS, JavaScript, HTML, images, performance &mdash; mostly technical, some bigger picture. Definitely some links not seen elsewhere. Weekly.</p>

<h3 id="javascript">JavaScript</h3>

<h4></h4>

<p>. Weekly.</p>

<h3 id="typography">Typography</h3>

<h4></h4>

<p>. Topics include “calligraphy, lettering, display type, micro type, books about fonts, type specimens, neon lights, posters, morse code, stamps, literature, web design, and books about seeds”. The format is that of a proper letter written by Robin to you which is rather lovely when it’s from someone so passionate. Weekly.</p>

<h4></h4>

<p> and featuring the latest free and open-source fonts, the most solid new typefaces by indie foundries and discount codes, this is a concise and well-compiled exploration of (mostly) newly released fonts and how you can get them. Twice a month.</p>

<h4></h4>

<p>. More than just a set of links, Ricardo digs into the articles he’s linking to, whether it’s a new font release or a deeper look into the role of typography on the web. Once or twice a month.</p>

<h3 id="user-experience">User Experience</h3>

<h4></h4>

<p>, this has become a bit of a UX behemoth, publishing a high volume of original articles and aggregated material on a range of UX and design related topics. Impressive output in terms of both quantity and quality. The newsletter reflects that. Weekly.</p>

<h4></h4>

<p> founded this “love letter to user experience design, front-end development, building products, and making the world a better place.” His newsletter collects links to the latest UX articles and resources, as well reminders of older, good resource links. Monthly. </p>

<h4></h4>

<p> has a hard-won global reputation as a consultant, trainer, speaker and writer on usability, UI and UX. It’s not surprising, then, that he realizes the great value of older content. The UIE newsletter is as likely to link to an article from five years ago as yesterday, if it’s still relevant &mdash; and, with user-centric topics, that’s often the case. Smart and useful. Weekly.</p>

<p><h4></h4></p>

<p>, for a readership mostly of beginning-to-intermediate user experience and interaction designers. The newsletter highlights one new inhouse article a week, plus links to three or four external UX articles and the occasional (often remote) job listing. Concise, focused, digestible and reliable. Weekly.</p>

<h4></h4>

<p> in 2005, this provides insights and inspiration to experienced professionals working in every aspect of UX, as well as beginners. The newsletter focuses tightly on new content on the website, but when you publish up to six articles, interviews, panel discussions, and technical pieces a week, that makes for a good newsletter. Weekly.</p>

<h3 id="web-design">Web Design</h3>

<h4></h4>

<p>. The Digest wraps all of this activity up and adds links to other interesting articles, videos and resources. Monthly.</p>

<h4></h4>

<p>Built “to provide web designers and developers with a single location to discover the latest and most significant stories on the Web.” Content includes “quality news, fresh tools and apps, case studies, code demos, inspiration posts, videos and more”. It is extremely comprehensive, and posts links every couple of hours. There is a user voting system, and the most shared items are featured in the newsletter. Daily.</p>

<h4></h4>

<p>In 10 years, WDD has grown from a blog into a genuine online magazine for web designers &mdash; and developers, content authors, specialist and generalists. Drawing on a stable of inhouse writers and external contributors, including some high-profile industry type. The newsletter highlights 10 or so items ranging across news, product info, design, code and WDD’s monthly round-up. Weekly.</p>

<h4></h4>

<p>Since 2012, Sidebar has been collecting links about UI design, typography, CSS, user research, and all other facets of design. It's now a trusted resource for thousands of designers across the world to stay on top of the latest news, trends, and resources. Each newsletter can include from three to a dozen links. Daily. </p>
  

<h4></h4>

<p>The website was launched in 2007 as an inspirational hub for web designers. As web design trends became more advanced and more tools became available it evolved into a web design magazine. Articles are usually published daily, which makes for a satisfyingly full email newsletter. Weekly.</p>

<h4></h4>

<p> has become a go-to site dedicated to providing beginners and advanced users tips, tricks, inspiration and resources for responsive design projects. The newsletter is equally popular and a very convenient way to keep with responsive design news. Weekly.</p>

<h4></h4>

<p>A heady mix of image-heavy product placement, sponsored items, free resources and links to articles, this newsletter regularly comes up with links to articles I don’t see elsewhere. I don’t know who is behind it (the very brief website just says “curated by designers for designers”), but it’s hard to ignore. Weekly.</p>

<h4></h4>

<p>A curated publication full of interesting, relevant links. I would call this an example of an educated, focused and informed newsletter of links to web resources that genuinely advance thinking on design systems. Providing just an article title and link makes it feel robotic and impersonal, but maybe that’s an approach you’ll like. Weekly (more or less).</p>

<h4></h4>

<p>. The Dispatch keeps you up to date. Weekly.</p>

<h4></h4>

<p>. Weekly.</p>

<h3 id="web-and-tech">Web &amp; Tech</h3>

<h4></h4>

<p>. Short, sharp, timely, useful and often linking to items of industry interest that others miss. Daily.</p>

<h4></h4>

<p>’s favorite articles about design, front-end development, technology, startups, productivity and the occasional inspirational life lesson. They pack in a lot of links, which might be why they list only the article title linked to the source. With such a broad remit, there is a lot of overlap with other newsletters, but it’s all in one package. Weekly.</p>

<h4><a href="https://www.hackernewsletter.com/">Hacker Newsletter </a></h4>

<p><a href="https://www.hackernewsletter.com/"><img style="float: right; padding: 1em;" src="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cf62df61-a3fa-472d-b595-e9f6e24f6ce8/roundup-newsletters-hackernewsletter.jpg" width="180" height="180" alt="Hacker Newsletter " /></a>This side project of MailChimp’s . That means this is another list of links, with not much to say where you should direct your attention. Still, those links are pretty good. Weekly.</p>

<h4></h4>

<p>, and now with a team of contributing authors, it also has lots of links to current articles about the web and tech. Weekly.</p>

<h4></h4>

<p> is Kai’s email newsletter offshoot in which he highlights products, news, events and insights for the discerning web worker. Classy and well selected. Weekly.</p>

<h4></h4>

<p> had the bright idea of collecting the moments and stories that make up web history to create an online timeline. Out of that came an email newsletter pointing to one or more of these stories. Highly readable, very informative, and often surprising. Weekly.</p>

<h3 id="wordpress">WordPress</h3>

<h4></h4>

<p> produce this newsletter for WordPress professionals, with editorial and links to apps, tools and resources. It’s not all about WordPress, though &mdash; it’s what WordPress pros need to know, so there’s general small business, lifestyle and industry articles as well as WP-specific items, including technical pieces. Weekly.</p>

<h4></h4>

<p>, this one carries more links to WordPress theme and plugin releases and reviews, tutorials, podcasts and videos &mdash; as well as more business, freelance and industry news and articles of interest to WordPress professionals and enthusiastic amateurs. Weekly.</p>

<h3 id="individuals">Individuals</h3>

<p>While I was compiling this article, I realized I have my own go-to set of people whose email newsletters I really look forward to. It’s not because they’re necessarily “the best” &mdash; it’s more that their choices of content, tone and focus strike a strong chord with me.</p>

<p>I’m sure you have your own, but here &mdash; apart from those who come up in the preceding sections &mdash; are the individuals whose newsletters I look forward to landing in my inbox.</p>

<ul>
<li> (design)</li>
<li> (UX)</li>
<li> (web &amp; tech)</li>
<li> (web &amp; tech)</li>
<li> (UX)</li>
<li> (design &amp; ethics)</li>
<li> (UX research)</li>
</ul>

<p>And that completes our latest round-up of email newsletters for web designers and developers.</p>

<p>Did I say “completes”? Of course, this list is not complete! For one thing, it probably doesn’t have your favorites. Add them &mdash; preferably with a working link &mdash; in the comments below.</p>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(vf, ra, il)</span>
</div>


              </article>
            </body>
          </html>
---------------
<h1 id="#title_2" >3、TGO 鲲鹏会台北分会成立，继续推动两岸科技交融</h1>
杨伟鑫
[http://www.infoq.com/cn/news/2018/06/tgo-taibei?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/06/tgo-taibei?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>6月24日，极客邦科技旗下汇聚全球技术领导者的高端社群 TGO 鲲鹏会台北分会于台北大学集思会议中心正式成立。</p> <i>By 杨伟鑫</i>
---------------
<h1 id="#title_3" >4、文章： AIOps实践思考：AIOps如何与APM结合？</h1>
高驰涛
[http://www.infoq.com/cn/articles/aiops-practice-think?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/aiops-practice-think?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/aiops-practice-think/zh/smallimage/SOA-1529899188338.jpeg"/><p>AIOps如何与APM结合？</p> <i>By 高驰涛</i>
---------------
<h1 id="#title_4" >5、Firefox重生</h1>
Brian Chen
[http://www.infoq.com/cn/news/2018/06/Firefox-new-life?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/06/Firefox-new-life?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Web安全和隐私问题越来越成为人们关注的焦点。Firefox被Chrome“碾压”之后，借助安全和隐私保护特性涅槃重生，这次能否打场漂亮的翻身仗？纽约时报专栏作者Brian Chen对此表达了他的看法。</p> <i>By Brian Chen</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_5" >6、为高效团队制作游戏</h1>
Ben Linders
[http://www.infoq.com/cn/news/2018/06/games-high-performing-teams?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/06/games-high-performing-teams?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>游戏风暴模型介绍了一个创建游戏的流程。它提供了类似游戏空间、边界、规则、工件和目标这样的概念，用于在组织环境里创建有吸引力的学习体验。团队可以使用这样的游戏进行试验，关注成果，尝试颠覆性模型。</p> <i>By Ben Linders</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_6" >7、OpsRamp推出AIOps推理引擎</h1>
Helen Beal
[http://www.infoq.com/cn/news/2018/06/OpsRamp-AI-Inference-Engine?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/06/OpsRamp-AI-Inference-Engine?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>基于SaaS的IT运管平台提供商OpsRamp宣布OpsRamp 5.0发布。新版本的主要特性是在报警和事件关联中使用了AIOps推理引擎，还添加了一种实现云可见性的仪表盘。</p> <i>By Helen Beal</i> <i> Translated by 盖磊</i>
---------------
<h1 id="#title_7" >8、Fake 5提供.NET Core支持</h1>
Pierre-Luc Maheu
[http://www.infoq.com/cn/news/2018/06/fake-dotnet-core?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/06/fake-dotnet-core?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Fake 5在推出预览版的数个月后于近期发布。该新版本的.NET应用构建工具重写了内核，做了一些内部改进，并推出了一些新特性。为更好地了解新版本中的改进和特性，InfoQ采访了Fake的维护者Matthias Dittrich。</p> <i>By Pierre-Luc Maheu</i> <i> Translated by 盖磊</i>
---------------
<h1 id="#title_8" >9、OpsRamp宣布统一服务发现</h1>
Helen Beal
[http://www.infoq.com/cn/news/2018/06/OpsRamp-Unified-Service-Discover?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/06/OpsRamp-Unified-Service-Discover?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>在2018年5月在佛罗里达州奥兰多召开的Gartner IT运营战略与解决方案峰会上，OpsRamp宣布了一项新的解决方案统一服务发现，以及针对混合环境的48小时IT资产可见性挑战。</p> <i>By Helen Beal</i> <i> Translated by 冬雨</i>
---------------