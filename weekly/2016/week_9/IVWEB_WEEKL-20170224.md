## 文章索引
1、 <a href="#1this-weeks-javascript-news-issue-323" >This week's JavaScript news, issue 323</a><br/>
2、 <a href="#2轻松管理你的-node-版本" >轻松管理你的 Node 版本</a><br/>
3、 <a href="#3stormpath发布了简化移动和前端身份验证的客户端api" >Stormpath发布了简化移动和前端身份验证的客户端API</a><br/>
4、 <a href="#4net-core-工具中的新内容" >.NET Core 工具中的新内容</a><br/>
5、 <a href="#5架构周报|-一个经过优化的微服务架构案例" >架构周报| 一个经过优化的微服务架构案例</a><br/>
6、 <a href="#6google宣布攻破sha-1从此sha-1不再安全" >Google宣布攻破SHA-1，从此SHA-1不再安全！</a><br/>
7、 <a href="#7针对微服务应重新领会功能服务设计来自microxchg大会的报告" >针对微服务应重新领会功能服务设计：来自microXchg大会的报告</a><br/>
8、 <a href="#8深度学习在gilt上的应用" >深度学习在Gilt上的应用</a><br/>
9、 <a href="#9视频演讲-阿里巴巴的数据研发体系是如何建立和管理的" >视频演讲： 阿里巴巴的数据研发体系是如何建立和管理的？</a><br/>
10、 <a href="#10data-geekery发布了java-orm工具jooq的390版用于构建类型安全查询" >Data Geekery发布了Java ORM工具jOOQ的3.9.0版，用于构建类型安全查询</a><br/>
11、 <a href="#11twitter数据中心网络及软件体系建设经验" >Twitter数据中心网络及软件体系建设经验</a><br/>
12、 <a href="#12物联网技术周报第-79-期:-为物联网应用创建-devops-流水线" >物联网技术周报第 79 期: 为物联网应用创建 DevOps 流水线</a><br/>
13、 <a href="#13linus-torvalds:-成功的项目源于99的汗水与1的创新" >Linus Torvalds: 成功的项目源于99%的汗水与1%的创新</a><br/>
14、 <a href="#14文章-以社交活动的方式做计划-乐高公司的规模化敏捷" >文章： 以社交活动的方式做计划-乐高公司的规模化敏捷</a><br/>
15、 <a href="#15视频演讲-kv-存储在-paypal-风控在线服务的使用实践" >视频演讲： KV 存储在 Paypal 风控在线服务的使用实践</a><br/>
16、 <a href="#16designing-with-real-data-in-sketch-using-the-craft-plugin" >Designing With Real Data In Sketch Using The Craft Plugin</a><br/><h1 id="#title_0" >1、This week's JavaScript news, issue 323</h1>

[http://javascriptweekly.com/issues/323](http://javascriptweekly.com/issues/323)
<table border="0" width="100%" cellpadding="0" cellspacing="0" bgcolor="#ffffff" style="font-family: 'helvetica neue', helvetica, arial, sans-serif; font-size: 14px; line-height: 20px; color: #333"><tr><td align="center" valign="top">
<table border="0" width="620" cellpadding="0" cellspacing="0" class="container noarchive" style="border-collapse: collapse;"><tr><td style="padding-top: 6px; padding-bottom: 6px; font-size: 11px; text-align: center; color: #555; font-family: verdana, arial, sans-serif">
<span class="nomo">This week's JavaScript news</span> — 
</td></tr></table>
<table border="0" width="620" cellpadding="0" cellspacing="0" class="container" style="border-collapse: collapse">
<tr><td style="background-color: #f7df1e"><table width="100%" cellspacing="0" cellpadding="0" align="left"><tr><td align="left" class="block" style="padding: 6px 12px;">
<table align="left" width="50%" class="gowide"><tr><td><span style="line-height: 36px; font-size: 23px; color: #f7df1e; font-weight: bold; color: #323330">JavaScript Weekly</span></td></tr></table>
<table align="left" style="text-align: right" width="50%" class="gowide lonmo"><tr><td><span style="font-size: 14px; line-height: 36px; font-weight: normal; color: #323330">
Issue 323 — February 23, 2017
</span></td></tr></table>
</td></tr></table></td></tr>
<tr><td style="padding: 16px 12px 12px 12px" align="left">
<p style="margin-top: 0; font-size: 1.0em; line-height: 1.4em; padding-top: 0; margin-bottom: 20px">Just a brief notice for eagle eyed readers.. we have ) :-)</p>
<div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">A look at recent efforts within the V8 team to bring the performance of newly added JavaScript features on par with their transpiled ES5 counterparts.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Michael Hablich
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">The V8 team is working on a new compiler pipeline that will increase performance. You  in Chrome Canary by enabling an experimental flag.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Michael Hablich
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">Neutrino combines the build and configuration power of Webpack with the capability to build JavaScript-based projects with presets. 
</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Eli Perelman
</div>
<br clear="all" style="clear: both"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">Get real-time crash alerts and collect detailed diagnostics so you can fix errors for your users. See deminified stacktraces with support for sourcemaps. Cut through front-end noise so you can efficiently assess the impact of errors. 
</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Bugsnag
  <span style="background-color: #f7df1e; color: #ffffff; font-weight: normal; padding: 1px 5px 0px 5px;">Sponsor</span>
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">A key release for the testing tool. Tests now re-run instantly after a file change and a typeahead feature has been added to make it easy to select the right tests.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Rogelio Guzman
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">The optionally-typed JavaScript extension adds improved code actions for editors, a new ‘object’ type, better class support for mixins, &amp; more. Sitepen has 
</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Microsoft
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">A fun site where the only messages you post are essentially tiny pieces of JavaScript that render simple demos into canvas elements. See  for example.</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">Late last year we launched a  due to the growth of the React ecosystem. If you use React and haven’t seen it yet, check it out :-)</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Cooperpress
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">A feature-based comparison of five image processing libraries that work within the browser.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
WebKid
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">Async/await won’t free you entirely from having to break out promises every so often.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Daniel Brain
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">Covers the basics of each key stage in a compiler as simply as possible. Note: The posts use  to provide interactive examples.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Yehonathan Sharvit
</div>
<br clear="all" style="clear: both"><p style="color: #666666; font-size: 16px; font-weight: bold; margin-top: 8px; margin-bottom: 10px; text-transform: uppercase">Jobs </p>
<ul style="padding-left: 18px; margin-top: 10px; list-style-type: square">
<li style="color: #f7df1e; margin-bottom: 10px; font-size: 15px; line-height: 17px">
<span style="font-size: 12px; color: #666666">Sticker Mule is looking for passionate engineers to join our remote team. Come help us build the best e-commerce experience using Ruby, Rails, React, Node, Docker and more.</span> <span style="color: #999999; font-weight: normal; font-size: 12px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Sticker Mule</span>
</li>
<li style="color: #f7df1e; margin-bottom: 10px; font-size: 15px; line-height: 17px">
<span style="font-size: 12px; color: #666666">Ready for your next challenge? Join our rapidly expanding team in London and help define the future of a industry-leading Angular (2+) app.</span> <span style="color: #999999; font-weight: normal; font-size: 12px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Avocet<span>.</span>io</span>
</li>
<li style="color: #f7df1e; margin-bottom: 10px; font-size: 15px; line-height: 17px">
<span style="font-size: 12px; color: #666666">We're looking for a developer with an extensive knowledge of Javascript and skills in different frameworks and libraries. We are 100% remote and we provide the funding needed to help you achieve your goals and grow.</span> <span style="color: #999999; font-weight: normal; font-size: 12px; text-transform: uppercase; font-family: verdana, arial, sans-serif">X-Team</span>
</li>
</ul>
<p style="color: #333; font-size: 12px; font-weight: normal; margin-top: 0px; margin-bottom: 10px">Can't find the right job? Want companies to apply to <em>you?</em> </p>
<p style="color: #666666; font-size: 16px; font-weight: bold; margin-top: 24px; margin-bottom: 10px; text-transform: uppercase">In Brief</p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #00aadd; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">news</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">A technical update on the support for the latest JavaScript features in Firefox.</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Mozilla</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #00aadd; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">news</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif"></span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> step-by-step.</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Thinkster  <span style="background-color: #f7df1e; color: #ffffff; font-weight: normal; padding: 1px 5px 0px 5px;">Sponsor</span></span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Jurgen Van de Moere</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">SitePoint</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Just Chris</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Just Chris</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Todd Motto</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Netanel Basal</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #cc00cc; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">video</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Ben Holmes</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #AF7817; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">opinion</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">2017 predictions for the key and rising JavaScript libraries and frameworks and JS’s New Frontiers in this whitepaper</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Progress  <span style="background-color: #f7df1e; color: #ffffff; font-weight: normal; padding: 1px 5px 0px 5px;">Sponsor</span></span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #AF7817; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">opinion</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Jason Dreyzehner</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #AF7817; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">opinion</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Juan Vega</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #bbbbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tools</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">A preset for Babel that lets you specify an environment and it automatically enables the necessary plugins.</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Dr. Axel Rauschmayer</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #bbbbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tools</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">SitePoint</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #00bbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">code</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">A ‘barely polyfill’ that implements a subset of the full Fetch API.</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Jason Miller</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #00bbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">code</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif"></span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #00bbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">code</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Jerome Etienne</span></p>
</td></tr>
<tr><td bgcolor="#f4f4f4" style="font-family: verdana, helvetica, arial, sans-serif; text-align: left; padding-top: 12px; padding-left: 12px; padding-right: 12px; padding-bottom: 12px" class="noarchive">
<p style="line-height: 15px; font-size: 11px; margin-top: 0">Curated by .</p>
<p style="line-height: 15px; font-size: 11px; margin-top: 0">Like this? You may also enjoy: </p>
<p style="font-size: 13px"></p>
<p style="font-size: 11px; line-height: 15px">© Cooperpress Ltd. Office 30, Lincoln Way, Louth, LN11 0LS, UK</p>
</td></tr>
</table>
</td></tr></table>
---------------
<h1 id="#title_1" >2、轻松管理你的 Node 版本</h1>

[https://www.h5jun.com/post/manage_node_with_n.html](https://www.h5jun.com/post/manage_node_with_n.html)
<div class="toc"><ul>
<li></li>
<li></li>
<li></li>
</ul>
</div><p>玩 Node.js 的小伙伴们都知道，现在 Node 的版本更新很快，目前最新稳定版已经更新到 v7.6.0 了，而生产环境一般选择使用 （Long-term Support）版本，目前最新的是 v6.10.0。</p>
<p>新版的 Node 7.x.x 有非常有用的更新，那就是支持了  --harmony-async-await。这样就不用依赖 babel 来使用 async/await 特性了。</p>
<p>但是，如何让 7.x.x 和 LTS 的 6.x.x 并存呢？就需要用 Node 版本管理工具了。</p>
<!--more-->
<p>之前常用的 Node 版本管理工具是 ，这是一个 shell 工具，能够比较方便地切换 Node 版本。</p>
<p>不过今天我要介绍给大家的是另一款更简单好用的 Node 版本管理工具，它本身是一个 Node 模块，叫做  大大开发的，强调简单化的版本管理工具：</p>
<blockquote>
<p>Node.js version management: no subshells, no profile setup, no convoluted API, just simple.</p>
</blockquote>
<h3>安装 n</h3>
<p>要安装 n 非常简单，它本身是一个 NPM 模块，因此：</p>
<pre><code class="hljs lang-undefined">npm -g install n
</code></pre>
<h3>使用和设置</h3>
<p>要使用 n 安装特定版本的 node，只需要如下命令：</p>
<pre><code class="hljs lang-bash">n stable <span class="hljs-comment">#安装最新的稳定版</span>
n lts <span class="hljs-comment">#安装最新的 LTS 版</span>
n 6.9.0 <span class="hljs-comment">#安装特定的 v6.9.0 版本</span>
</code></pre>
<p>安装完成多个版本后，直接输入不带参数的 n 命令，会出现一个已安装版本的列表：</p>
<p><img src="https://p.ssl.qhimg.com/d/inn/b2a93336/2C678E28-C7C0-478E-BD7D-A3D0D2FEC5FB.png" alt="选择版本"></p>
<p>用键盘上下键选择版本，然后回车，就可以切换默认 Node 版本。</p>
<h3>直接启动不同版本的 Node</h3>
<p>假如我们将默认的 Node 版本设置为 6.10.0 了，而我们要使用 7.6.0 启动某个应用，也非常简单，只需要：</p>
<pre><code class="hljs lang-undefined">n use 7.6.0 index.js
</code></pre>
<p>于是，我们可以这么用：</p>
<p><strong>async.js</strong></p>
<pre><code class="hljs lang-js"><span class="hljs-meta">'use strict'</span>

<span class="hljs-keyword">let</span> randomDelay = () =&gt; <span class="hljs-keyword">new</span> <span class="hljs-built_in">Promise</span>(<span class="hljs-function"><span class="hljs-keyword">function</span>(<span class="hljs-params">resolve</span>)</span>{
    <span class="hljs-keyword">var</span> delay = <span class="hljs-built_in">Math</span>.round(<span class="hljs-built_in">Math</span>.random() * <span class="hljs-number">1000</span>);
    setTimeout(<span class="hljs-function"><span class="hljs-keyword">function</span>(<span class="hljs-params"></span>)</span>{
        <span class="hljs-built_in">console</span>.log(<span class="hljs-string">'delay '</span> + delay + <span class="hljs-string">' ms'</span>);
        resolve(delay);
    }, delay);
});

<span class="hljs-keyword">async</span> <span class="hljs-function"><span class="hljs-keyword">function</span> <span class="hljs-title">main</span>(<span class="hljs-params"></span>)</span>{
    <span class="hljs-keyword">await</span> <span class="hljs-built_in">Promise</span>.all([randomDelay(), randomDelay()]);
    <span class="hljs-built_in">console</span>.log(<span class="hljs-string">'pass'</span>);
    <span class="hljs-keyword">await</span> randomDelay();
}

main();
</code></pre>
<pre><code class="hljs lang-undefined">n use 7.6.0 async.js
</code></pre>
<p>你会看到类似下面这样的输出结果，说明我们不需要 babel，直接可以用 Node 7.6.0 支持 async/await 了。</p>
<pre><code class="hljs lang-undefined">delay 252 ms
delay 964 ms
pass
delay 536 ms
</code></pre>
<p>最后，我们可以创建一个快捷的命令：</p>
<pre><code class="hljs lang-bash"><span class="hljs-built_in">echo</span> <span class="hljs-built_in">alias</span> node7=<span class="hljs-string">"\"n use 7.6.0 --harmony-async-await\""</span> &gt;&gt; ~/.bashrc
<span class="hljs-built_in">source</span> ~/.bashrc
</code></pre>
<p>这样我们就可以愉快地使用 node v7.x.x 运行我们的 js 了：</p>
<pre><code class="hljs lang-js">node7 <span class="hljs-keyword">async</span>.js
</code></pre>
---------------
<h1 id="#title_2" >3、Stormpath发布了简化移动和前端身份验证的客户端API</h1>
Benjamin Young
[http://www.infoq.com/cn/news/2017/02/stormpath-client?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/02/stormpath-client?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/news/2017/02/stormpath-client/zh/headerimage/auto.jpg"/><p>身份验证、授权、社交登录，以及其他用户管理相关API服务供应商Stormpath，近日发布了一套意在简化移动和前端身份验证与注册过程的全新客户端API。</p> <i>By Benjamin Young</i> <i> Translated by 大愚若智</i>
---------------
<h1 id="#title_3" >4、.NET Core 工具中的新内容</h1>
Jeff Martin
[http://www.infoq.com/cn/news/2017/02/netcore-rc4?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/02/netcore-rc4?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Visual Studio 2017 RC最近一个版本更新包括一套更新的.NET Core工具箱。这个版本带来了几项改进，包括改变了模版化、dotnet网络命令，以及许多缺陷修复。微软的Rich Lander发表了一份更新说明，陈述了.NET Core开发人员可以预期在.NET Core RC4找到些什么。</p> <i>By Jeff Martin</i> <i> Translated by 冬雨</i>
---------------
<h1 id="#title_4" >5、架构周报| 一个经过优化的微服务架构案例</h1>
ArchSummit峰会
[http://www.infoq.com/cn/news/2017/02/arch-weekly-Micro-service-archit?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/02/arch-weekly-Micro-service-archit?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>一个经过优化的微服务架构案例</p> <i>By ArchSummit峰会</i>
---------------
<h1 id="#title_5" >6、Google宣布攻破SHA-1，从此SHA-1不再安全！</h1>
Marc Stevens
[http://www.infoq.com/cn/news/2017/02/google-first-sha1-collision?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/02/google-first-sha1-collision?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Google昨日正式宣布攻破SHA-1。早在2014年，Chrome小组就宣布将逐渐淘汰对SHA-1的使用。Google希望自己针对SHA-1完成的实际攻击能够进一步巩固这一结论，让更多人意识到其已经不再安全可靠。也建议工业界尽快转向更为安全的替代性方案，例如SHA-256。</p> <i>By Marc Stevens</i>
---------------
<h1 id="#title_6" >7、针对微服务应重新领会功能服务设计：来自microXchg大会的报告</h1>
Daniel Bryant
[http://www.infoq.com/cn/news/2017/02/microxchg-service-design?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/02/microxchg-service-design?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>今年microXchg微服务大会上，Uwe Friedrichsen做了开幕报告。报告中探讨了“弹性功能服务设计”的核心理念，要点包括：微服务开发人员应该了解容错设计模式与缓存，但不能用于改善完全不好（过度耦合）的系统设计；理解DDD和模块化的重要性；组件重在可替换性而非可重用性。报告指出，在实现微服务这样的分布式系统时，开发人员和架构师需要重新领会功能服务设计。</p> <i>By Daniel Bryant</i> <i> Translated by Rayss</i>
---------------
<h1 id="#title_7" >8、深度学习在Gilt上的应用</h1>
Alex Giamas
[http://www.infoq.com/cn/news/2017/02/Deep-Learning-Gilt?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/02/Deep-Learning-Gilt?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/news/2017/02/Deep-Learning-Gilt/zh/headerimage/deep-learning.jpg"/><p>机器学习起源于神经网络，而深度学习是机器学习的一个快速发展的子领域。最近的一些算法的进步和GPU并行计算的使用，使得基于深度学习的算法可以在围棋和其他的一些实际应用里取得很好的成绩。时尚产业是深度学习的目标领域之一。闪购网站Gilt正在实际应用中使用深度学习技术。</p> <i>By Alex Giamas</i> <i> Translated by 尚剑</i>
---------------
<h1 id="#title_8" >9、视频演讲： 阿里巴巴的数据研发体系是如何建立和管理的？</h1>
张磊
[http://www.infoq.com/cn/presentations/how-to-establish-and-manage-the-data-research-and-development-system-of-alibaba?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/how-to-establish-and-manage-the-data-research-and-development-system-of-alibaba?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/how-to-establish-and-manage-the-data-research-and-development-system-of-alibaba/zh/mediumimage/zhanglei270.jpg"/><p>数据研发经常会遇到这些问题：
研发人数较多（超千人），频繁上下线，如何解决开发效率的问题？业务高速发展，数据量爆炸式的增长，如何有效控制存储与计算的线性增长？从数据采集到数据消费的整个链路非常复杂，如何保障整个数据链路的质量与产出时间？大数据建设的标准规范，如何制定并有效的执行？数据浩瀚如烟、纷繁复杂，如何能够迅速的找到自己想要的数据？
经过几年的摸索，我们通过 OneData 研发体系能够比较有效的解决上述问题。OneData 定位是：一个指标一个算法，一个维度属性只有一个名字，模型规范化，从算法定义、数据研发到数据服务，可管理追溯从而规避重复建设。</p> <i>By 张磊</i>
---------------
<h1 id="#title_9" >10、Data Geekery发布了Java ORM工具jOOQ的3.9.0版，用于构建类型安全查询</h1>
Michael Redlich
[http://www.infoq.com/cn/news/2017/02/data-geekery-releases-jooq-3-9?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/02/data-geekery-releases-jooq-3-9?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/news/2017/02/data-geekery-releases-jooq-3-9/zh/headerimage/GettyImages-518002738.jpg"/><p>Data Geekery公司发布了其Java ORM工具包jOOQ的3.9.0版。jOOQ实现从数据库生成代码，用于类型安全查询。本文给出了jOOQ的入门实例，并通过访谈介绍了jOOQ的主要特性及进一步发展。</p> <i>By Michael Redlich</i> <i> Translated by Rayss</i>
---------------
<h1 id="#title_10" >11、Twitter数据中心网络及软件体系建设经验</h1>
麦克周
[http://www.infoq.com/cn/news/2017/02/Twitter-data-center?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/02/Twitter-data-center?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Twitter作为一家互联网通信软件服务提供商，它在建设通信软件服务时遇到的网络问题、软件系统架构问题、软件技术选型等等都值得我们学习。Twitter发表的文章有助于读者从整体理解互联网软件开发、发布、问题解决等整个体系结构相关知识，也帮助读者从侧面完成技术选型。</p> <i>By 麦克周</i>
---------------
<h1 id="#title_11" >12、物联网技术周报第 79 期: 为物联网应用创建 DevOps 流水线</h1>
黄峰达
[http://www.infoq.com/cn/news/2017/02/iot-weekly-79?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/02/iot-weekly-79?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>为物联网应用创建 DevOps 流水线；Arduino 制作 Amazon Dash 物联网按钮；Arduino Due 制作 Altair 8800 仿真器；IBM Watson物联网总部正式投入使用，将专注物联网与人工智能的研究；Android Things给物联网设备带来基于TensorFlow的机器学习和计算机视觉；三星扩大物联网生态系统 实现智能家居和智联汽车的真正融合</p> <i>By 黄峰达</i>
---------------
<h1 id="#title_12" >13、Linus Torvalds: 成功的项目源于99%的汗水与1%的创新</h1>
刘志勇
[http://www.infoq.com/cn/news/2017/02/Linus-Torvalds-success-new?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/02/Linus-Torvalds-success-new?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>2017年2月15日，在加利福尼亚州的开源领袖峰会上，由Linux基金会执行董事Jim Zemlin进行的一次采访中，Torvalds讨论了他如何管理Linux内核的开发以及他对工作的态度。</p> <i>By 刘志勇</i>
---------------
<h1 id="#title_13" >14、文章： 以社交活动的方式做计划-乐高公司的规模化敏捷</h1>
Henrik Kniberg, Eik Thyrsted Brandsgård
[http://www.infoq.com/cn/articles/planning-as-a-social-event-scaling-agile-at-lego?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/planning-as-a-social-event-scaling-agile-at-lego?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/planning-as-a-social-event-scaling-agile-at-lego/zh/smallimage/logo 112 (2).jpg"/><p>乐高数字解决方案部门（DS）由20个左右的团队组成，负责处理孩子和家长手中各种设备- 普通电脑，平板电脑，各种app应用，可穿戴设备，虚拟现实设备等等进行通讯。我们同时也在展望未来的产品开发，如何去拥抱新的技术，如何将传统的玩法与酷炫技术，例如增强现实结合起来，或者找一种能够将一个物理模型“扫描”进游戏的方法。绝大部分的团队在丹麦的比隆，但是我们在印度也有一部分团队。</p> <i>By Henrik Kniberg</i>
---------------
<h1 id="#title_14" >15、视频演讲： KV 存储在 Paypal 风控在线服务的使用实践</h1>
李欣
[http://www.infoq.com/cn/presentations/practice-of-kv-stored-in-paypal-wind-control-online-service?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/practice-of-kv-stored-in-paypal-wind-control-online-service?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/practice-of-kv-stored-in-paypal-wind-control-online-service/zh/mediumimage/lixin270.jpg"/><p>随着Payapl业务的快速发展，对于风控也提出了越来越高的要求：高质量的风险决策需要应对数据量的快速增长，数据结构越来越灵活，数据结构改变趋于频繁，而对于系统稳定性和业务可用性的要求却也越来越高，传统数据库如oracle，已无法很好的跟上快速的业务增长，导致paypal risk需要从新思考并打造下一代的风险数据存储技术。</p> <i>By 李欣</i>
---------------
<h1 id="#title_15" >16、Designing With Real Data In Sketch Using The Craft Plugin</h1>
Christian Krammer
[https://www.smashingmagazine.com/2017/02/design-with-real-data-sketch-using-craft-plugin/](https://www.smashingmagazine.com/2017/02/design-with-real-data-sketch-using-craft-plugin/)
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
</table><p>Besides the user's needs, what's another vital aspect of an app? Your first thought might be its design. That's important, correct, but before you can even think about the design, you need to get something else right: the data.</p>

<figure></figure>

<p>Data should be the cornerstone of everything you create. Not only does it help you to make more informed decisions, but it also makes it easier to account for edge cases, or things you might not have thought of otherwise.</p>

<p>If you want to get even more out of Sketch, feel free to check out our fancy new book, “.</p>
---------------