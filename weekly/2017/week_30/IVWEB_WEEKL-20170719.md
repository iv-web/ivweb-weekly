## 文章索引
1、 <a href="#1文章-分布式数据库和-hadoop-都不够好于是我们设计了分布式-sql-计算系统" >文章： 分布式数据库和 Hadoop 都不够好，于是我们设计了分布式 SQL 计算系统</a><br/>
2、 <a href="#2pull-request-的命令行管理" >Pull Request 的命令行管理</a><br/>
3、 <a href="#3视频演讲-精益创新组合决策更科学地决策你的投资" >视频演讲： 精益创新组合决策——更科学地决策你的投资</a><br/>
4、 <a href="#4文章-gitlab首席执行官sid-sijbrandij畅谈当前开发实践" >文章： GitLab首席执行官Sid Sijbrandij畅谈当前开发实践</a><br/>
5、 <a href="#5文章-专访frances-perry关注apache-beam" >文章： 专访Frances Perry：关注Apache Beam</a><br/>
6、 <a href="#6fex-技术周刊---2017/07/17" >FEX 技术周刊 - 2017/07/17</a><br/>
7、 <a href="#7迷你书-放手去做管理-30-实战手册" >迷你书： 放手去做：管理 3.0 实战手册</a><br/>
8、 <a href="#8物联网技术周报第-98-期:-使用-linuxpython-和-raspberry-pi-酿造啤酒" >物联网技术周报第 98 期: 使用 Linux、Python 和 Raspberry Pi 酿造啤酒</a><br/>
9、 <a href="#9百度开源其nlp主题模型工具包文本分类等场景可直接使用" >百度开源其NLP主题模型工具包，文本分类等场景可直接使用</a><br/>
10、 <a href="#10integrate-2017回顾将智能融入集成" >Integrate 2017回顾：将智能融入集成</a><br/>
11、 <a href="#11以ebay机器人购物助手为例阐述聊天机器人的可扩展架构" >以eBay机器人购物助手为例阐述聊天机器人的可扩展架构</a><br/><h1 id="#title_0" >1、文章： 分布式数据库和 Hadoop 都不够好，于是我们设计了分布式 SQL 计算系统</h1>
江和慧
[http://www.infoq.com/cn/articles/distributed-database-hadoop-distributed-sql-computing-system?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/distributed-database-hadoop-distributed-sql-computing-system?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/distributed-database-hadoop-distributed-sql-computing-system/zh/smallimage/logo2 (9).jpg"/><p>为了解决分布式数据库下，复杂的 SQL（如全局性的排序、分组、join、子查询，特别是非均衡字段的这些逻辑操作）难以实现的问题；在有了一些分布式数据库和 Hadoop 实际应用经验的基础上，对比两者的优点和不足，加上自己的一些提炼和思考, 设计了一套综合两者的系统，利用两者的优点， 补充两者的不足。具体的说， 使用数据库水平分割的思想实现数据存储，使用 MapReduce的思想实现 SQL 计算。</p> <i>By 江和慧</i>
---------------
<h1 id="#title_1" >2、Pull Request 的命令行管理</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2017/07/pull_request.html](http://www.ruanyifeng.com/blog/2017/07/pull_request.html)
<p>Github 的一大特色就是  功能（简写为 PR）。</p>

        <p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017071801.png" alt="" title="" /></p>

<p>对于多人合作的项目，该功能简直必不可少。大部分人都是使用 Web 界面（如上图），本文介绍如何在命令行下处理 PR，翻译自 Cédric Beust 的。</p>

<h2>一、Pull Request 是什么？</h2>

<p>Github 官方文档的如下。</p>

<blockquote>
  <p>"Pull Request 是一种通知机制。你修改了他人的代码，将你的修改通知原来的作者，希望他合并你的修改，这就是 Pull Request。"</p>
</blockquote>

<p>Pull Request 本质上是一种软件的合作方式，是将涉及不同功能的代码，纳入主干的一种流程。这个过程中，还可以进行讨论、审核和修改代码。</p>

<h2>二、Pull Request 的流程</h2>

<p>第一步，你需要把别人的代码，克隆到你自己的仓库，Github 的术语叫做 。</p>

<p>第二步，在你仓库的修改后的分支上，按下"New pull request"按钮。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017071802.png" alt="" title="" /></p>

<p>这时，会进入一个新页面，有Base 和 Head 两个选项。Base 是你希望提交变更的目标，Head  是目前包含你的变更的那个分支或仓库。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017071806.png" alt="" title="" /></p>

<p>第三步，填写说明，帮助别人理解你的提交，然后按下"create pull request"按钮即可。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017071805.png" alt="" title="" /></p>

<p>PR 创建后，管理者就要决定是否接受该 PR。对于非代码变更（比如文档），单单使用 Web 界面就足够了。但是，对于代码变更，Web 界面可能不够用，需要命令行验证是否可以运行。</p>

<h2>三、git am</h2>

<p><code>git am</code>命令用于将一个 patch 文件，合并进入当前代码。</p>

<p>Github 对每个 PR 会自动生成一个 patch 文件。我们下载该文件，合并进本地代码，就可以在本地查看效果了。</p>

<blockquote><pre><code class="language-bash">
$ curl -L http://github.com/cbeust/testng/pull/17.patch | git am
</code></pre></blockquote>

<p>上面代码中，<code>curl</code>的<code>-L</code>参数表示，如果有302跳转，<code>curl</code>会自动跟进。后面网址里面的<code>/cbeust/testng</code>是目标仓库，<code>pull/17</code>表示该仓库收到的第17个 PR。</p>

<p>如果 PR 只包含一个 commit，那么也可以直接下载这个 commit 的 patch 文件。</p>

<blockquote><pre><code class="language-bash">
$ curl https://github.com/sclasen/jcommander/commit/bd770141029f49bcfa2e0d6e6e6282b531e69179.patch | git am
</code></pre></blockquote>

<p>上面代码中，网址里面的<code>/sclasen/jcommander</code>是代码变更所在的那个仓库。</p>

<h2>四、创建远程仓库</h2>

<p>另一种方法是为 PR 创建一个远程分支，追踪提交者的仓库。</p>

<blockquote><pre><code class="language-bash">
# 创建远程仓库，指向 PR 提交者的仓库
$ git remote add nullin git://github.com/nullin/testng.git

# 从该远程仓库拉取代码
$ git fetch nullin

# 将该仓库的某个分支合并到当前分支
$ git merge kneath/error-page

# 推送到自己的仓库
$ git push origin master
</code></pre></blockquote>

<h2>五、cherry-pick</h2>

<p>有时，PR 里面包含好几个 commit，但是你只想合并其中的一个或几个。</p>

<p>这时可以使用<code>cherry-pick</code>命令，挑出你感兴趣的 commit。</p>

<blockquote><pre><code class="language-bash">
# 建立远程分支，追踪提交者的仓库
$ git remote add nullin git://github.com/nullin/testng.git

# 从该远程仓库拉取代码
$ git fetch nullin

# 只将感兴趣的 commit 加入当前代码
$ git cherry-pick commit1
$ git cherry-pick commit2

# 推送到自己的仓库
$ git push origin master
</code></pre></blockquote>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2017-07-18T18:06:14+08:00">2017年7月18日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>博客文集：</li>
<li>社交媒体：</li>
<li>Feed订阅： </li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------
<h1 id="#title_2" >3、视频演讲： 精益创新组合决策——更科学地决策你的投资</h1>
姚安峰
[http://www.infoq.com/cn/presentations/lean-innovation-portfolio-decision-making-your-investment-more-scientifically?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/lean-innovation-portfolio-decision-making-your-investment-more-scientifically?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/lean-innovation-portfolio-decision-making-your-investment-more-scientifically/zh/mediumimage/yaoanfeng270.jpg"/><p>面对科技创新机会层出不穷的时代，传统的投资组合管理似乎不再有效，应该做什么不做什么，先做什么后做什么，产品和研发团队面对不确定性有些无所适从，领导拍脑袋产品功能越来越多，用户抱怨越来越多。精益创新组合决策，融合了精益画布、精益 A3、延迟成本、精益创业、滚动规划的思想给你一套立刻可落地的方法，从容不迫地进行产品创新的投资分析、决策和验证，更加科学、更加透明，助你实现业务敏捷。该方法已在多个国内企业实践，深受欢迎。</p> <i>By 姚安峰</i>
---------------
<h1 id="#title_3" >4、文章： GitLab首席执行官Sid Sijbrandij畅谈当前开发实践</h1>
Sergio De Simone
[http://www.infoq.com/cn/articles/gitlab-sid-interview-sw-development?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/gitlab-sid-interview-sw-development?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/gitlab-sid-interview-sw-development/zh/headerimage/article-logo-big.jpg"/><p>在整个采访过程中，GitLab首席执行官Sid Sijbrandij谈到了GitLab是如何创立的、GitLab与竞争对手的不同之处、成为“开放”的公司的重要性、GitLab工程师如何使用持续集成以及成为一家采用远程工作方式的公司意味着什么等诸多话题。</p> <i>By Sergio De Simone</i> <i> Translated by 蔡芳芳</i>
---------------
<h1 id="#title_4" >5、文章： 专访Frances Perry：关注Apache Beam</h1>
Dylan Raithel
[http://www.infoq.com/cn/articles/beam-perry?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/beam-perry?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/beam-perry/zh/headerimage/apachebeam-large.jpg"/><p>InfoQ采访了Apache Beam项目管理委员会的Frances Perry，内容涉及企业采用Beam的动力所在，以及该Apache顶级项目的未来发展。</p> <i>By Dylan Raithel</i> <i> Translated by Rays</i>
---------------
<h1 id="#title_5" >6、FEX 技术周刊 - 2017/07/17</h1>

[http://fex.baidu.com/blog/2017/07/fex-weekly-17//](http://fex.baidu.com/blog/2017/07/fex-weekly-17//)
作者：duhongbin01 <br> <p>微信搜索『FEX』关注我们的公众号，及时获得最新资讯。</p>

<h2 id="section">业界会议</h2>

<p><strong>2017 JavaScript中国开发者大会</strong><br />
http://2017.jsconf.cn/<br />
附：</p>

<h2 id="section-1">深阅读</h2>

<p><strong>Let’s Dev: A Package Manager</strong><br />
https://yarnpkg.com/blog/2017/07/11/lets-dev-a-package-manager/<br />
Hello everyone! Today, we’re gonna write a new package manager, even better than Yarn! Ok, maybe not, but at least we’re gonna have some fun, learn how package managers work, and think about what could come next on Yarn.</p>

<p><strong>ES8 was Released and here are its Main New Features</strong><br />
https://hackernoon.com/es8-was-released-and-here-are-its-main-new-features-ee9c394adf66<br />
EcmaScript 8 or EcmaScript 2017 was officially released at the end of June by TC39. It seems that we are talking a lot about EcmaScript in the last year. It’s not for nothing. Currently the standard is to publish a new ES specification version once a year. ES6 was published in 2015 and ES7 was published in 2016, but did someone remembered when ES5 was released? It happened in 2009, before the magical rise of JavaScript. 另附：</p>

<p><strong>Security updates for all active release lines</strong><br />
https://nodejs.org/en/blog/vulnerability/july-2017-security-releases/<br />
Updates are now available for all active Node.js release lines as well as the 7.x line. These include the fix for the high severity vulnerability identified in the initial announcement, one additional lower priority Node.js vulnerability in the 4.x release line, as well as some lower priority fixes for Node.js dependencies across the current release lines.</p>

<p><strong>Introducing npx: an npm package runner</strong><br />
https://medium.com/@maybekatz/introducing-npx-an-npm-package-runner-55f7d4bd282b<br />
</p>

<p><strong>Upcoming RegExp Features</strong><br />
https://v8project.blogspot.jp/2017/07/upcoming-regexp-features.html<br />
ES2015 introduced many new features to the JavaScript language, including significant improvements to the regular expression syntax with the Unicode (/u) and sticky (/y) flags. In this blog post we want to give you a preview of this exciting future. If you’d like to follow along with the upcoming examples, enable experimental JavaScript features at chrome://flags/#enable-javascript-harmony.</p>

<p><strong>Introducing sphinx-js, a better way to document large JavaScript projects</strong><br />
https://hacks.mozilla.org/2017/07/introducing-sphinx-js-a-better-way-to-document-large-javascript-projects/<br />
sphinx-js consumes standard JSDoc comments and tags—you don’t have to do anything weird to your source code. You just have Sphinx initialize a docs folder in the root of your project, activate sphinx-js as a plugin, and then write docs to your heart’s content using simple reStructuredText. When it comes time to call in some extracted documentation, you use one of sphinx-js’s special directives, modeled after the Python-centric autodoc’s mature example.</p>

<p><strong>A look inside React Fiber - how work will get done.</strong><br />
http://makersden.io/blog/look-inside-fiber/<br />
Fiber 是如何实现的</p>

<p><strong>The MVC Design Pattern in Vanilla JavaScript</strong><br />
https://www.sitepoint.com/mvc-design-pattern-javascript/<br />
The MVC pattern is good for client-side frameworks, but modern frameworks change. What is modern today is subject to the passing of time and withers away. In this take, I’d like to explore alternatives and see where a little discipline takes us.</p>

<p><strong>Event Delegation: Pattern or Anti-Pattern</strong><br />
https://www.sitepen.com/blog/2017/07/11/event-delegation-pattern-or-anti-pattern/<br />
Event delegation is one of the defacto ways of doing event handling. But is it the right methodology for all projects? In fact, the better question might be whether the assumptions each toolkit has made are right for your project. Knowing whether an API is right for your project depends on knowing what assumptions these tools are built on and understanding how each toolkit has interpreted them.</p>

<p><strong>架构开发技术百科全书</strong><br />
https://mp.weixin.qq.com/s?__biz=MzIyNjE4NjI2Nw==&amp;mid=2652559046&amp;idx=1&amp;sn=209b4499f3884cf02514f38e75b24d39<br />
本文是笔者多年来积累和收集的知识技能图谱，有的是笔者原创总结的最佳实践，有的是小伙伴们的分享，其中每个秘籍图谱里面的内容都是互联网高并发架构师应该了解和掌握的知识，笔者索性把这些图谱收集在一起，并且归类便于查找和学习，希望能够帮助到每一位想成为架构师或者已经是架构师的小伙伴。</p>

<p><strong>百度转型AI，Web大有可为</strong><br />
http://www.infoq.com/cn/news/2017/07/Web-baidu-AI-HTTPS<br />
HTTPS、MIP、AR 等相关的技术分享</p>

<p><strong>单向数据流动的函数式 View Controller</strong><br />
https://onevcat.com/2017/07/state-based-viewcontroller/<br />
在这篇文章里，我会先实现一个很常见的 MVC 架构，然后对状态和状态改变的部分进行抽象及重构，最终得到一个纯函数式的易于测试的 View Controller 类。希望通过这个例子，能够给你在日常维护 View Controller 的工作中带来一些启示或者帮助。</p>

<p><strong>ios10 vs ios11 :完整UI比较分析</strong><br />
https://mp.weixin.qq.com/s/E8TQZAX5riS-xjVzI-x_wA<br />
很详细的 UI 对比及说明</p>

<p><strong>Developer Experience Lessons Operating a Serverless-like Platform At Netflix</strong><br />
https://medium.com/netflix-techblog/developer-experience-lessons-operating-a-serverless-like-platform-at-netflix-a8bbd5b899a0<br />
This is the first in a series of posts where we draw from our learnings to outline various aspects that we are addressing in the next generation of our platform. We believe these aspects are applicable to general purpose serverless solutions too. Here we will look at application development, delivery and code composition. Future posts will delve into topics such as deployments, insights, performance, scalability and other operational concerns.</p>

<p><strong>How Uber Uses JavaScript and Node.js</strong><br />
https://www.youtube.com/watch?v=JWFyH13_I3o<br />
Talk recording from AmsterdamJS Conference 2017.</p>

<p><strong>Reverse Engineering One Line of JavaScript</strong><br />
https://www.alexkras.com/reverse-engineering-one-line-of-javascript/<br />
如何分析一个高度混淆的代码，能学到不少知识</p>

<p><strong>What 10 Things Should a Serious Javascript Developer Know Right Now</strong><br />
https://www.reddit.com/r/javascript/comments/6mlc9d/what_10_things_should_a_serious_javascript/<br />
Scope, Architecture, DOM, Node.js…</p>

<p><strong>How Rust is tested</strong><br />
https://brson.github.io/2017/07/10/how-rust-is-tested<br />
I’ve always admired well-tested software projects, like SQLite, and aim to place Rust among the pantheon of the best. This document then, is a catalog of all the ways we test Rust. I hope it provides insight into what it takes to deliver a production-quality programming language, a hint at the wide variety of techniques employed in software validation, and that it reinforces your confidence in Rust’s reliability. 另附：</p>

<p><strong>Mock system APIs</strong><br />
https://glebbahmutov.com/blog/mock-system-apis/<br />
When you write your module (let’s say a Node JavaScript one), you often expose public API, but internally your code accesses the outside world via own code. Testing the public API is the best, but often it is hard, since your code interacts with the file system, user or network. How do you test the exposed API when you need to mock the rest of the system? I think it is preferable to NOT mock your own code modules, but to mock the interface to the external world.</p>

<p><strong>Don’t write an SPA* Unless it makes sense to</strong><br />
https://blog.semanticscholar.org/dont-write-an-spa-57aaa40e0314<br />
SPAs are a good choice if: The interface you’re building is highly interactive and needs to be fast / responsive — and you want an architecture and abstractions that supports this out the gate; You’re not worried about each and every bit of content being indexed by search engines correctly. On the other hand, an SPA might not be worth the complexity if: Your application is simple (there’s not a lot of interactive content); SEO is of pivotal importance.</p>

<p><strong>What is “modern” programming</strong><br />
http://lemire.me/blog/2017/07/15/what-is-modern-programming/<br />
I submit to you that modern programming has little to do with the look of your desktop. Graphical user interfaces are only skin deep. Modern programming techniques are all about processes and actual tools, not the skin on top of them. I don’t care whether you are using Eclipse or Emacs… this tells me nothing about how modern you are. So what is “modern”?</p>

<p><strong>A Complete List Of UX Deliverables</strong><br />
https://uxplanet.org/a-complete-list-of-ux-deliverables-d62ccf1de434<br />
The list below contains most common deliverables produced by UX Designers as they craft great experiences for users. For better readability, I’ve combined the deliverables according to UX activities: User Research, Market Research, Design, Testing. For each item in the list you’ll find additional links or video with detailed explanation or best practices.</p>

<p><strong>URLs are UI</strong><br />
https://www.hanselman.com/blog/URLsAreUI.aspx<br />
So many folks spend time on their CSS and their UX/UI but still come up with URLs that are at best, comically long, and at worst, user hostile.</p>

<h2 id="section-2">新鲜货</h2>

<p><strong>Angular 4.3 Now Available</strong><br />
http://angularjs.blogspot.jp/2017/07/angular-43-now-available.html<br />
Angular version 4.3 has been released. This is a minor release following our announced adoption of Semantic Versioning, meaning that it contains no breaking changes and that it is a drop-in replacement for 4.x.x.</p>

<p><strong>Babylon.js 3.0</strong><br />
https://blogs.windows.com/buildingapps/2017/07/12/announcing-babylon-js-3-0/<br />
Babylon.js is an open source framework that allows you to create stunning 3D experiences in your browser. Built with simplicity and performance in mind, it is the engine that fuels the Remix3D site or the Xbox Design Lab.</p>

<p><strong>Tim Berners-Lee approves Web DRM</strong><br />
http://defectivebydesign.org/blog/tim_bernerslee_approves_web_drm_w3c_member_organizations_have_two_weeks_appeal<br />
Tim Berners-Lee, the chief arbiter of Web standards, approved the controversial proposed Digital Restrictions Management (DRM) standard for the Web, Encrypted Media Extensions (EME).</p>

<p><strong>Introducing Channels: Private Q&amp;A for Your Team</strong><br />
https://stackoverflow.blog/2017/07/11/introducing-channels-private-qa-team/<br />
We’re announcing Stack Overflow Channels for teams that need a dedicated, private space to share knowledge. We’re working hard on an early beta, and we want your active involvement in the product as we build it.</p>

<p><strong>Building open source tools for Adobe Creative Cloud updates</strong><br />
https://code.facebook.com/posts/1555751614499319/building-open-source-tools-for-adobe-creative-cloud-updates/<br />
Our Enterprise Engineering team recently developed a software management script that could save teams hundreds of hours in building application packages for Mac users. The new system makes it easier for people to access Adobe apps with centrally-managed Creative Cloud licensing, while saving time and improving reporting and accounting accuracy.</p>

<p><strong>emotion - The Next Generation of CSS-in-JS</strong><br />
https://github.com/tkh44/emotion<br />
emotion is a high performance, lightweight css-in-js library. The core idea comes from Sunil Pai’s glam library and its philosophy is laid out here. The basic idea is simple. You shouldn’t have to sacrifice runtime performance for good developer experience when writing CSS. emotion minimizes the runtime cost of css-in-js dramatically by parsing your styles with PostCSS during compilation instead of at runtime. 详见。</p>

<p><strong>WeSketch</strong><br />
https://github.com/weixin/WeSketch<br />
微信开源的 Sketch 辅助插件</p>

<p><strong>Pell: A Simple, Small (5kB) WYSIWYG Web Text Editor</strong><br />
https://github.com/jaredreich/pell<br />
pell is the simplest and smallest WYSIWYG text editor for web, with no dependencies</p>

<p><strong>gpu.js</strong><br />
https://github.com/gpujs/gpu.js<br />
gpu.js is a single-file JavaScript library for GPGPU (General purpose computing on GPUs) in the browser. gpu.js will automatically compile specially written JavaScript functions into shader language and run them on the GPU using the WebGL API. In case WebGL is not available, the functions will still run in regular JavaScript.</p>

<p><strong>p5.js</strong><br />
https://p5js.org/<br />
p5.js is a JavaScript library that starts with the original goal of Processing, to make coding accessible for artists, designers, edcators, and beginners, and reinterprets this for today’s web.</p>

<p><strong>BotUI</strong><br />
https://github.com/moinism/botui<br />
A JavaScript framework to create conversational UIs.</p>

<p><strong>TagUI</strong><br />
https://github.com/tebelorg/TagUI<br />
TagUI is a general purpose tool for automating web interactions</p>

<p><strong>CSS Database</strong><br />
https://jonathantneal.github.io/css-db/<br />
CSS Database is a comprehensive list of CSS features and their positions in the process of becoming implemented web standards.</p>

<p><strong>create sea animals using pure CSS</strong><br />
https://codepen.io/ChhaviKhandelwal/pen/pwdeRO/<br />
用纯CSS来制作几个海洋生物的样子，值得学习</p>

<p><strong>PHP7 to ES7 syntax translator</strong><br />
https://gitlab.com/kornelski/babel-preset-php<br />
最近我们有同事正好用过别的类似工具，语法和函数都好说，字符编码不一致的问题比较麻烦。另附：</p>

<p><strong>Real World React</strong><br />
https://github.com/jeromedalbert/real-world-react<br />
收集了大量 React 项目，方便通过查找代码的方式学习</p>

<p><strong>Microcosm</strong><br />
http://code.viget.com/microcosm/<br />
Microcosm is Flux with actions at center stage. Write optimistic updates, cancel requests, and track changes with ease。附：</p>

<p><strong>3 New Tools to Speed Up Your Apps</strong><br />
https://medium.freecodecamp.org/make-react-fast-again-tools-and-techniques-for-speeding-up-your-react-app-7ad39d3c1b82<br />
In this post I’ll highlight tools and techniques for making React apps fast. Each section also has an interactive, and (hopefully) fun demo. Tools: The Performance Timeline, why-did-you-update, React Developer Tools.</p>

<p><strong>Web Tools &amp; Services Highly Rated By Experts</strong><br />
http://codecondo.com/web-tools-services-highly-rated-by-experts/<br />
Welcome to this great showcase of 21 web tools &amp; services that are highly rated by experts. The used methods to find out the most popular solutions were to search the internet, test the web tools and discuss with different experts from several domains.</p>

<p><strong>6 Free Material Design CSS Frameworks for 2017 Compared</strong><br />
https://www.sitepoint.com/free-material-design-css-frameworks-compared/<br />
对6个比较火热的 Material Design 的CSS框架进行对比，用户可以根据自己的需求场景以及各个框架的生态情况选择适合自己的那一款</p>

<p><strong>PouchDB 6.3.0</strong><br />
https://pouchdb.com/2017/07/13/pouchdb-6.3.0.html<br />
PouchDB is an open-source JavaScript database inspired by Apache CouchDB that is designed to run well within the browser. PouchDB was created to help web developers build applications that work as well offline as they do online.</p>

<p><strong>API Security Checklist</strong><br />
https://github.com/shieldfy/API-Security-Checklist<br />
Checklist of the most important security countermeasures when designing, testing, and releasing your API.</p>

<p><strong>Redis 4.0 GA is out!</strong><br />
https://groups.google.com/forum/#!msg/redis-db/5Kh3viziYGQ/58TKLwX0AAAJ<br />
Redis 4.0.0 is out. I’m very happy about 4.0, because this release finally overcomes several very important limits of Redis. There are many things in the 4.2 plan, so Redis with 4.0 is not magically perfect. Yet it is a very important, measurable, step forward, because of the following features.</p>

<p><strong>Go Makes It Into TIOBE’s Top 10 Languages</strong><br />
https://www.tiobe.com/tiobe-index/<br />
This is an important landmark for the Go programming language, but it also makes you wonder what’s next. Is Go really able to join the big stars in the programming language world and leave languages such as JavaScript and Python behind? We will see.</p>

<h2 id="section-3">产品及其它</h2>

<p><strong>Seeing AI: Talking Camera for the Blind</strong><br />
https://www.microsoft.com/en-us/seeing-ai/<br />
A free app that narrates the world around you. Designed for the low vision community, this research project harnesses the power of AI to describe people, text and objects. 另附：</p>

<p><strong>Dashboard设计思考</strong><br />
https://mp.weixin.qq.com/s?__biz=MTEwNTM0ODI0MQ==&amp;mid=2653434474&amp;idx=1&amp;sn=8cfd25c46f5634b3f4da989dddd33549<br />
在企业类应用服务（SaaS）、检测工具（手机安全助手）、量化自我工具（智能手环）等后台管理系统中，使用Dashboard可以帮助用户监控和分析数据，快速获取重要信息。但如果对Dashboard设计缺乏认知，就很可能会造成Dashboard呈现的信息杂乱，充斥着无关紧要的指标、文本信息及各种半成品的图表等，让用户抓不到重点。那么，设计师该如何设计内容精确、体验友好的Dashboard以满足用户需求呢？</p>

<p><strong>蚂蚁金服CTO程立 - 昨天最好的表现是今天最低的要求</strong><br />
https://mp.weixin.qq.com/s?__biz=MjM5MDE0Mjc4MA==&amp;mid=2650996875&amp;idx=1&amp;sn=02e6d7c94a29a0d220a814790999b37e<br />
技术连接了两个端，一端是需求、目的，另一端是一个已有的技术，将两者结合一起，商业贡献与技术贡献的有效结合形成化学反应，出现了一个新技术，而这个新技术再去满足新的技术，再出来一个新的技术，形成一个化学反应过程。如果团队成员每个人想法背景多元化，但梦想又相同时，会出现很多创新的结果，技术本身是化学反应不是物理反应。比团队认同自己更重要的是，认同共同的目标。最顺利的时候总是最危险的时候。今天很残酷，明天更残酷，但是后天很美好。</p>

<p><strong>陆奇-如何成为一个优秀的工程师</strong><br />
https://mp.weixin.qq.com/s?__biz=MzA3OTQyNzcwNw==&amp;mid=2650387426&amp;idx=1&amp;sn=8f47c85367575a4d65608d8d6e4fdcae<br />
我们一定要有一个坚定不移的深刻的理念，相信整个世界终究是为技术所驱动的；有没有其他人已经解决这个问题？然后你可以把你的时间放在更好的创新上；做什么事情一定要做最好，一定要是做业界最强的；我把自己想象是一个软件、一个代码，今天的版本一定要比昨天版本好，明天的版本肯定会比今天好；看到问题也不要去问别人，就把它Fix。</p>
---------------
<h1 id="#title_6" >7、迷你书： 放手去做：管理 3.0 实战手册</h1>
Ralph van Roosmalen
[http://www.infoq.com/cn/minibooks/doing-it?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/minibooks/doing-it?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/minibooks/doing-it/zh/smallimage/100.jpg"/><p>愿所有人都能从这本实战手册里面掌握一些好玩且有效的工具，提升团队的管理，让每个人都能对工作乐在其中。</p> <i>By Ralph van Roosmalen</i> <i> Translated by 侯伯薇</i>
---------------
<h1 id="#title_7" >8、物联网技术周报第 98 期: 使用 Linux、Python 和 Raspberry Pi 酿造啤酒</h1>
黄峰达
[http://www.infoq.com/cn/news/2017/07/iot-weekly-98?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/07/iot-weekly-98?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>使用 Ansible 和 Raspberry Pi 3 构建 Kubernetes 群集；使用 Linux、Python 和 Raspberry Pi 酿造啤酒；借助平台互操作性打造物联网生态；ofo宣布全面使用“物联网智能锁”，与中国电信、华为共同宣布NB-IoT启动商用；BAT为何都看中智能音箱？这篇文章说清楚了；英特尔物联网业务发展受挫 裁员约140人</p> <i>By 黄峰达</i>
---------------
<h1 id="#title_8" >9、百度开源其NLP主题模型工具包，文本分类等场景可直接使用</h1>
姜迪
[http://www.infoq.com/cn/news/2017/07/Baidu-open-NLP-Toolkit?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/07/Baidu-open-NLP-Toolkit?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>百度开源了一款NLP主题模型工具包，包含文档主题推断工具、语义匹配计算工具以及基于工业级语料训练的三种主题模型。同时支持使用者以“拿来即用”的方式进行文本分类、文本聚类、个性化推荐等多种场景的调研和应用。</p> <i>By 姜迪</i>
---------------
<h1 id="#title_9" >10、Integrate 2017回顾：将智能融入集成</h1>
Kent Weare
[http://www.infoq.com/cn/news/2017/07/Microsoft-Integrate2017?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/07/Microsoft-Integrate2017?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>一年一度的专注于微软集成技术大会Integrate 2017于今年6月26-28日在伦敦召开。本次大会的核心主题有认知计算在集成中的作用、API编排、SaaS连接、云原生集成、无服务器对集成的影响和大规模的云消息传递。</p> <i>By Kent Weare</i> <i> Translated by 李梦</i>
---------------
<h1 id="#title_10" >11、以eBay机器人购物助手为例阐述聊天机器人的可扩展架构</h1>
Srini Penchikala
[http://www.infoq.com/cn/news/2017/07/ebay-shopbot?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/07/ebay-shopbot?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/news/2017/07/ebay-shopbot/zh/headerimage/GettyImages-458574425.jpg"/><p>来自eBay的软件工程师Robet Enyedi在QCon纽约2017会议上谈了个人购物助手这款购物机器人应用背后的架构设计。这款购物机器人助手于2016年发布，是基于Facebook Messenger打造的，集成了AI组件和ebay的用户数据，通过对话的形式来为用户提供购物选择。</p> <i>By Srini Penchikala</i> <i> Translated by 李勇</i>
---------------