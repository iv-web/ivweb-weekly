## 文章索引
1、 <a href="#1office-365-being-rewritten-in-javascript" >Office 365 being rewritten in JavaScript</a><br/>
2、 <a href="#2迷你书-2018进击的大前端" >迷你书： 2018，进击的大前端</a><br/>
3、 <a href="#3monthly-web-development-update-6/2018:-complexity-dns-over-https-and-push-notifications" >Monthly Web Development Update 6/2018: Complexity, DNS Over HTTPS, And Push Notifications</a><br/>
4、 <a href="#4文章-坚硬的区块链" >文章： 坚硬的区块链</a><br/>
5、 <a href="#5文章-netflix开源新作大数据发现服务框架metacat" >文章： Netflix开源新作：大数据发现服务框架Metacat</a><br/>
6、 <a href="#6如何防止密码被硬编码到代码中yelp开源了自己的解决方案" >如何防止密码被硬编码到代码中？Yelp开源了自己的解决方案</a><br/>
7、 <a href="#7关于visual-studio-2019的前期详情" >关于Visual Studio 2019的前期详情</a><br/>
8、 <a href="#8让敏捷领导随机应变的素质" >让敏捷领导随机应变的素质</a><br/>
9、 <a href="#9studio-3tmongodb-sql探究" >Studio 3T：MongoDB SQL探究</a><br/>
10、 <a href="#10dockly创建者访谈基于控制台的docker容器管理ui" >Dockly创建者访谈：基于控制台的Docker容器管理UI</a><br/><h1 id="#title_0" >1、Office 365 being rewritten in JavaScript</h1>

[https://javascriptweekly.com/issues/390](https://javascriptweekly.com/issues/390)
<table border=0 align="center" border="0">
  <tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   ">

  <div>    
    <table border=0 border=0><tr>
<td align="left" style="padding-left: 4px; font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   "><p>#390 — June 15, 2018</p></td>
<td align="right" style="padding-right: 4px; font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   "><p></p></td>
</tr></table>
    
    <table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0 12px;"><p>JavaScript Weekly</p></td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   ">
  
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;">, if preferred) looking at the key parts of major JavaScript VMs/engines and how they interact with the code you write.</p>
  <p>Mathias Bynens </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></p>
  <p>Netflix </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Bored by the academic approach of most data structures and algorithms courses? This is for you. Solve algorithms and analyze space and time complexity in both an interview setting and in your day-to-day development.</p>
  <p>Frontend Masters <span style="text-transform: uppercase; padding: 1px 4px;  margin-left: 4px; font-size: 0.9em;   color: #997 !important;">sponsor</span></p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"> is the approach used, making it possible to build seamless Windows 10 and Xbox One apps with React.</p>
  <p>Sean Thomas Larkin on Twitter </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></p>
  <p>GeekyAnts </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — ‘Marking’ is a key step in V8 6.4’s garbage collection process and now this process takes place on separate worker threads meaning more time for <em>your</em> code on Chrome 64+ and Node 10+.</p>
  <p>Mathias Bynens </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — John Resig, the creator of jQuery, has co-written a book aiming to show you why GraphQL APIs are <em>“the true successor to REST APIs”</em>.</p>
  <p>John Resig and Loren Sands-Ramshaw </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — A vanity metric for sure, but an interesting one nonetheless. React still has significantly more downloads each day but Vue’s community is particularly vibrant and eager.</p>
  <p>Dan Abramov on Twitter </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>The Lead Developer London <span style="text-transform: uppercase; padding: 1px 4px;  margin-left: 4px; font-size: 0.9em;   color: #997 !important;">sponsor</span></p>
</td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0;"><p>💻 Jobs</p></td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Join our small, distributed team as we build the world’s largest open library of freely usable visuals. Open to all, regardless of experience and background.</p>
  <p>Unsplash </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Vettery matches top tech talent with fast-growing companies. Take a few minutes to join our platform.</p>
  <p>Vettery </p>
</td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0;"><p>📘 Tutorials</p></td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — A beginner-friendly walkthrough of using JavaScript’s <code>reduce</code> method.</p>
  <p>Sarah Drasner </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Including async iteration, <code>Promise.finally()</code>, and rest/spread properties.</p>
  <p>Craig Buckler </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;">▶  </span> — Fun with thought processed interactions using a brain sensor with JavaScript.</p>
  <p>Charlie Gerard </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;">▶  </span> — A demo of Slack’s new developer features, with an introduction to Actions, showing what it enables for developers, and some possible use cases.</p>
  <p>Slack <span style="text-transform: uppercase; padding: 1px 4px;  margin-left: 4px; font-size: 0.9em;   color: #997 !important;">sponsor</span></p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Ogundipe Samuel </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — A Rails-esque MVC framework for Node webapps.</p>
  <p>Ahmed Bouchefra </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;">▶  </span> — This isn’t JS specific but we’re always hearing of developers trying out Windows lately so this could be helpful.</p>
  <p>Sarah Cooley and Tara Raj </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;">▶  </span></p>
  <p>Dapper Dino </p>
</td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0;"><p>🔧 Code and Tools</p></td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — If you want a fast, easy, zero-config bundler.</p>
  <p>Devon Govett </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Wallaby catches errors in your tests and displays the results of expressions right in your editor as you type.</p>
  <p>Wallaby.js <span style="text-transform: uppercase; padding: 1px 4px;  margin-left: 4px; font-size: 0.9em;   color: #997 !important;">sponsor</span></p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Mihir Chaturvedi </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — A similar API to Laravel Collections: chunk, flatten, shuffle, firstWhere, etc.</p>
  <p>Daniel Eckermann </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"> It’s nice.</p>
  <p>Simon Wep </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;">, if that’s your bag.</p>
  <p>Jos de Jong </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Bourry Xavier </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;">.</p>
  <p>Lv Yang </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Lusaxweb </p>
</td></tr></table>
<table border=0 border=0><tr><td style=" font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   "></td></tr></table>
</div>

  </td></tr>
</table>





<img src="https://javascriptweekly.com/open/390/rss" width="1" height="1" />
---------------
<h1 id="#title_1" >2、迷你书： 2018，进击的大前端</h1>
InfoQ中文站
[http://www.infoq.com/cn/minibooks/gmtc-mini-book?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/minibooks/gmtc-mini-book?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/minibooks/gmtc-mini-book/zh/smallimage/100-1528874853560.jpg"/><p>本期主要内容：全栈与大前端，前端工程师进阶该如何抉择？狼叔：Node全栈为前端带来更多可能；2018年，前端开发者需要学习哪些东西？为什么说Flutter让移动开发变得更好？</p> <i>By InfoQ中文站</i>
---------------
<h1 id="#title_2" >3、Monthly Web Development Update 6/2018: Complexity, DNS Over HTTPS, And Push Notifications</h1>
Anselm Hannemann
[https://www.smashingmagazine.com/2018/06/monthly-web-development-update-6-2018/](https://www.smashingmagazine.com/2018/06/monthly-web-development-update-6-2018/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/06/monthly-web-development-update-6-2018/" />
              <title>Monthly Web Development Update 6/2018: Complexity, DNS Over HTTPS, And Push Notifications</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>Monthly Web Development Update 6/2018: Complexity, DNS Over HTTPS, And Push Notifications</h1>
                  
                    
                    <address>Anselm Hannemann</address>
                  
                  <time datetime="2018-06-15T12:32:58&#43;02:00" class="op-published">2018-06-15T12:32:58+02:00</time>
                  <time datetime="2018-06-15T23:49:44&#43;00:00" class="op-modified">2018-06-15T23:49:44+00:00</time>
                </header>
                <p>We see complexity in every corner of a web project these days. We’ve read quite a bunch of articles about how complex a specific technology has become, and we discuss this over and over again. Coming from a time where we uploaded websites via FTP and had no git or anything comparable, now living in a time where we have a build system, transpilers, frameworks, tests, and a CI even for the smallest projects, this is easy to understand. But on the other hand, web development has grown up so much in the past 15 years that <strong>we can’t really compare today to the past anymore</strong>. And while it might seem that some things were easier in the past, we neglect the advantages and countless possibilities we have today. When we didn’t write tests back then, well, we simply had no test — meaning no reliable way to test for success. When we had no deployment process, it was easy to upload a new version but just as easy to break something — and it happened a lot more than today when a Continuous Integration system is in place.</p>
<p>Jeffrey Zeldman wrote an interesting article on the matter: “” outlines how we lose ourselves in unnecessary details and often try to <strong>overthink problems</strong>. I like the challenge of building systems that are not too complex but show a decent amount of responsibility (when it comes to ethics, privacy, security, a great user experience, and performance) and are working reliably (tests, deployments, availability, and performance again). I guess the problem of finding the right balance won’t go away anytime soon. Complexity is everywhere — we just need to decide if it’s useful complexity or if it was added simply because it was easier or because we were over-engineering the original problem.</p>

<p><h3>News</h3>
<ul>
<li>The upcoming Safari version 12 was unveiled at Apple’s WWDC. Here’s what’s new: icons in tabs, strong passwords, as well as a password generator control via HTML attributes including two-factor authentication control, a 3D and AR model viewer, the Fullscreen API on iPads, <code>font-display</code>, and, very important,  which is more restrictive than ever and might have a significant impact on the functionality of existing websites.</li>
<li>The headless Chrome automation library  is now out in version 1.5. It brings along Browser contexts to isolate cookies and other data usually shared between pages, and Workers can now be used to interact with Web Workers, too.</li>
<li>Google released , the third major version of their performance analyzation tool which features a new report interface, some scoring changes, a CSV export, and First Contentful Paint measurement.</li>
<li>, bringing Progressive Web Apps to the Desktop, as well as support for the Generic Sensor API, and extending the Credential Management API to support U2F authenticators via USB.</li>
<li>We’ve seen quite some changes in the browsers’ security interfaces over the past months. First, they emphasized sites that offer a secured connection (HTTPS). Then they decided to indicate insecure sites, and now Chrome announced new changes coming in fall that will make HTTPS the default by .</li>
</ul></p>

<figure>)</figcaption></figure>

<p><h3>General</h3>
<ul>
<li>In “.</li>
<li>Heydon Pickering shared a new, very interesting article that teaches us to build a web component properly: This time he explains .</li>
</ul></p>

<p><h3>UI/UX</h3>
<ul>
<li> is a cool side project by Moe Amaya. It’s an online generator for polygonal backgrounds with gradients that can generate a lot of variants and shapes. Simply beautiful.</li>
</ul></p>

<p><h3>Tooling</h3>
<ul>
<li>Ben Frain shares some useful  that are available in almost all modern code editors.</li>
</ul></p>

<p><h3>Security</h3>
<ul>
<li>As security attacks via DNS gain popularity, DNS over HTTPS gets more and more important. Lin Clark  to make it easier to understand.</li>
<li>Windows Edge is now . The attribute to lock down cookies even more is already available in Firefox and Chrome, so Safari is the only major browser that still needs to implement it, but I guess it’ll land in their Tech Preview builds very soon as well.</li>
</ul></p>

<figure>)</figcaption></figure>

<p><h3>Privacy</h3>
<ul>
<li>The ACLU discovered that  and provides a mass-face recognition technology that is already used in cities around the world.</li>
</ul></p>

<p><h3>Web Performance</h3>
<ul>
<li>KeyCDN asked 15 people who know a lot about web performance to share their best advice with readers. Now they shared this article containing a lot of , including a few words by myself.</li>
<li>Stefan Judis discovered that we can already  by adding an HTML header tag <code>link rel=&ldquo;modulepreload&rdquo;</code>.</li>
</ul></p>

<p><h3>Accessibility</h3>
<ul>
<li>It’s relatively easy to build a loading spinner — for a Single Page Application during load, for example —, but we rarely think about making them accessible. Stuart Nelson now explains .</li>
<li>Paul Stanton shares  to get the best results.</li>
</ul></p>

<p><h3>JavaScript</h3>
<ul>
<li>JavaScript has lately been bullied by people who favor Elm, Rust, TypeScript, Babel or Dart. But , as Andrea Giammarchi explains with great examples. This article is also a great read for everyone who uses one of these other languages as it shows a couple of pitfalls that we should be aware of.</li>
<li>For a lot of projects, we want to use analytics or other scripts that collect personal information. With GDPR in effect, this got a lot harder.  is a nice JavaScript tool that lets you block the execution of such resources until a user agrees to it.</li>
<li>Ryan Miller created a new publication called “The Frontendian”, and it features  I’ve come across so far.</li>
<li>The folks at Microsoft created a nice interactive demo page to show . If you haven’t gotten to grips with the technology yet, it’s a great primer to how it all works and how to build an interface that doesn’t disturb users.</li>
<li> is a JavaScript library for uploading files. It looks great and comes with a lot of adapters for React, Vue, Angular, and jQuery.</li>
<li> and brings quite a feature to the library: Pointer Events. They’ll make it easier to deal with user interactions and have been requested for a long time already.</li>
</ul></p>

<figure>)</figcaption></figure>

<p><h3>CSS</h3>
<ul>
<li>Oliver Schöndorfer shares  and how we can style them with CSS. A pretty complete summary of things you need to consider as well as possible pitfalls.</li>
<li>With the upcoming macOS Mojave supporting a ‘dark mode’,  if no <code>background-color</code> is explicitly set. This is a great reminder that browsers can set and alter their default styles and that we need to set our site defaults carefully. I’m still hoping that the ‘dark mode’ will be exposed to a CSS Media Query so we can officially add support for it.</li>
<li>Rafaela Ferro shares how to . This article has the answers to many questions I regularly get when talking about Grid layout.</li>
<li>Marcin Wichary explains how .</li>
</ul></p>

<p><h3>Work &amp; Life</h3>
<ul>
<li>Anton Sten wrote about . A meaningful explanation why the times of “move fast and break things” are definitely over as we’re dealing with Artificial Intelligence, social networks that affect peoples’ lives, and privacy matters enforced by GDPR.</li>
<li>Basecamp now has a new chart type to display a project’s status: the so-called “” adds a better context than a simple progress bar could ever do it.</li>
<li> and how they always fail to reflect who you are, what you do, and why you should be hired.</li>
</ul></p>

<p>I hope you enjoyed this monthly update. The next one is scheduled for July 13th, so stay tuned. In the meantime, if you like what I do, .</p>

<p>Have a great day!</em></p>

<p><em>&mdash; Anselm</em></p>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(cm)</span>
</div>


              </article>
            </body>
          </html>
---------------
<h1 id="#title_3" >4、文章： 坚硬的区块链</h1>
Jimmy Song
[http://www.infoq.com/cn/articles/why-blockchain-is-hard?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/why-blockchain-is-hard?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/why-blockchain-is-hard/zh/smallimage/logo-1526022783167-1528994830888.jpeg"/><p>现在区块链的风这么大，很多猪都挤过来等着上天。那些喜欢炒作的人把区块链说的天花乱坠。我想用这篇文章解释一下区块链是什么，以及它不是什么（从目前的情况来看，这一点更重要），从而给出这些问题的答案。</p> <i>By Jimmy Song</i> <i> Translated by 海兴</i>
---------------
<h1 id="#title_4" >5、文章： Netflix开源新作：大数据发现服务框架Metacat</h1>
蔡芳芳
[http://www.infoq.com/cn/articles/bigdata-netflix-metacat?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/bigdata-netflix-metacat?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/bigdata-netflix-metacat/zh/smallimage/ballerina-part2-logo-small-1527788057440-1529052687967.jpg"/><p>Netflix开源新作：大数据发现服务框架Metacat</p> <i>By 蔡芳芳</i>
---------------
<h1 id="#title_5" >6、如何防止密码被硬编码到代码中？Yelp开源了自己的解决方案</h1>
无明
[http://www.infoq.com/cn/news/2018/06/preventing-secrets-coded-yelp?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/06/preventing-secrets-coded-yelp?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>近日，Yelp 宣布正式开源其密码检测框架，该框架用于防止代码中的密码等相关敏感信息被提交到代码库中，它号称可以在保证安全性的同时不会给开发者的生产力带来任何影响。</p> <i>By 无明</i>
---------------
<h1 id="#title_6" >7、关于Visual Studio 2019的前期详情</h1>
Jeff Martin
[http://www.infoq.com/cn/news/2018/06/vs2019-announced?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/06/vs2019-announced?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>近日，来自微软公司的 John Montgomery 正式宣布，VS2017 的下一代产品 Visual Studio 2019 已进入开发阶段。InfoQ 对于目前已知的部分内容进行了相关报道 。</p> <i>By Jeff Martin</i> <i> Translated by 邵思华</i>
---------------
<h1 id="#title_7" >8、让敏捷领导随机应变的素质</h1>
Shane Hastie
[http://www.infoq.com/cn/news/2018/06/remain-adaptive-leader?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/06/remain-adaptive-leader?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>组织中的每个层面、每个岗位都离不开领导力。最近有很多文章在讨论履行领导职责时的随机应变能力。按照Brent Gleeson在Inc上那篇文章的说法，如今这个年代，不管在哪个领域，要想取得真正的成果，必须靠随机应变，而且只能靠随机应变。在福布斯教练协会看来，在思想和领导行为上保持敏捷对成功履行领导职责至关重要。

</p> <i>By Shane Hastie</i> <i> Translated by 海兴</i>
---------------
<h1 id="#title_8" >9、Studio 3T：MongoDB SQL探究</h1>
Jonathan Allen
[http://www.infoq.com/cn/news/2018/06/Studio-3T-SQL-MongoDB?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/06/Studio-3T-SQL-MongoDB?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Studio 3T为MongoDB提供了一个基于SQL的用户界面，其中包括就地数据编辑、查询性能信息和SQL代码到JavaScript（node.JS）、Java、Python和C#的转换器。</p> <i>By Jonathan Allen</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_9" >10、Dockly创建者访谈：基于控制台的Docker容器管理UI</h1>
Matt Campbell
[http://www.infoq.com/cn/news/2018/06/dockly-console-based-docker-mgmt?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/06/dockly-console-based-docker-mgmt?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Dockly是Docker CLI的开源替代方案，它可以帮助你从命令行管理和监控所有的Docker容器。为了更好地了解Dockly如何改进了与Docker的协同，InfoQ采访了Dockly开发者Liran Tal，了解他构建Dockly及创建终端应用程序的经验。</p> <i>By Matt Campbell</i> <i> Translated by 谢丽</i>
---------------