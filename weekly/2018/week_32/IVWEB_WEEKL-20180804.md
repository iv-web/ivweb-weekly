## 文章索引
1、 <a href="#1the-cost-of-javascript-typescript-30-and-a-new-framework-from-uber" >The 'cost' of JavaScript, TypeScript 3.0, and a new framework from Uber</a><br/>
2、 <a href="#2迷你书-前端面试指南" >迷你书： 前端面试指南</a><br/>
3、 <a href="#3视频演讲-华为容器在kubernetes上的技术实践之路" >视频演讲： 华为容器在Kubernetes上的技术实践之路</a><br/>
4、 <a href="#4视频访谈-七牛云宫静研发组织实施cicd-需要注意些什么" >视频访谈： 七牛云宫静：研发组织实施CICD 需要注意些什么？</a><br/>
5、 <a href="#5we-are-just-getting-started:-1000-smashing-members" >We Are Just Getting Started: 1,000 Smashing Members</a><br/>
6、 <a href="#6甲骨文中国数据库中心将落地与微软数据库市场两家独大" >甲骨文中国数据库中心将落地，与微软数据库市场两家独大</a><br/>
7、 <a href="#7每周分享第-16-期" >每周分享第 16 期</a><br/>
8、 <a href="#8从无人问津到占主导脸书如何从python-2迁移到python-3" >从无人问津到占主导，脸书如何从Python 2迁移到Python 3</a><br/>
9、 <a href="#9百度超级链首个应用图腾落地跨界公链＋ai+大数据" >百度超级链首个应用图腾落地，跨界公链＋AI+大数据</a><br/>
10、 <a href="#10用于google-cloud开发人员的区块链工具包发布" >用于Google Cloud开发人员的区块链工具包发布</a><br/>
11、 <a href="#11istio-v10服务网格发布各特性已生产就绪" >Istio v1.0服务网格发布，各特性已生产就绪</a><br/>
12、 <a href="#12pymetrics开源公平性感知机器学习算法audit-ai" >Pymetrics开源公平性感知机器学习算法Audit AI</a><br/>
13、 <a href="#13物联网技术周报第-145-期:-esp8266-和-ifttt-自制-wifi-智能秤" >物联网技术周报第 145 期: ESP8266 和 IFTTT 自制 WiFi 智能秤</a><br/><h1 id="#title_0" >1、The 'cost' of JavaScript, TypeScript 3.0, and a new framework from Uber</h1>

[https://javascriptweekly.com/issues/397](https://javascriptweekly.com/issues/397)
<table border=0 align="center" border="0">
  <tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   ">

  <div>    
    <table border=0 border=0><tr>
<td align="left" style="padding-left: 4px; font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   "><p>#397 — August  3, 2018</p></td>
<td align="right" style="padding-right: 4px; font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   "><p></p></td>
</tr></table>
    
    <table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0 12px;  "><p>JavaScript Weekly</p></td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   ">
  
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"> of Addy’s talk a month ago, but now here’s the detailed write-up of Addy’s thoughts and findings on how much effect JavaScript has on page sizes and performance and some ways to improve matters.</p>
  <p>Addy Osmani </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — 3.0 has few breaking changes (meaning it should be very easy to upgrade) and introduces a new flexible, scalable way to structure your projects, powerful new support for operating on parameter lists, better JSX support, an overall better error UX, and more.</p>
  <p>Microsoft </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;">.</p>
  <p>Bugsnag <span style="text-transform: uppercase; padding: 1px 4px;  margin-left: 4px; font-size: 0.9em;   color: #997 !important;">sponsor</span></p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Uber builds and maintains hundreds of Web apps, both internal and public, and Fusion.js is their answer to the challenges this presents. It comes with hot module reloading, data-aware server-side rendering, and bundle splitting out of the box.</p>
  <p>Leo Horie </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — <em>“Moving forward with v7, we’ve decided it’s best to stop publishing the Stage presets in Babel (e.g. <code>@babel/preset-stage-0</code>).”</em> If you’re a Babel user, you’ll appreciate this the explanation for this change.</p>
  <p>Henry Zhu (Babel) </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Always a fun contest with some interesting results. You’re limited to 13KB for all code and assets. It runs August 13-September 13.</p>
  <p>Andrzej Mazur </p>
</td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0;  "><p>💻 Jobs</p></td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — As a Web Platform engineer at Uber, you'll be building the foundation for all web applications at Uber and beyond.</p>
  <p>Uber </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;">.</p>
  <p>x-team </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Create a profile to connect with 4,000+ companies seeking top tech talent.</p>
  <p>Vettery </p>
</td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0;  "><p>📘 Tutorials and Opinions</p></td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — If you fancy a direct comparison between Vue and React, fill your boots here.</p>
  <p>Sunil Sandhu </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — How to build a Slack-like chat application using Vue.js and ChatEngine - global &amp; private chat, and chatbots.</p>
  <p>PubNub <span style="text-transform: uppercase; padding: 1px 4px;  margin-left: 4px; font-size: 0.9em;   color: #997 !important;">sponsor</span></p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Hassan Djirdeh </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Máté Huszárik </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — The latest ASP.NET Core includes a template to build an Angular <em>4</em> application, but what about Angular 6? Here’s how to do it.</p>
  <p>Lee Brandt </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;">.</p>
  <p>Yoni Goldberg, Kyle Martin and Bruno Scheufler </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Building web apps? Read this whitepaper to learn top considerations for choosing your technology stack.</p>
  <p>Sencha, Inc <span style="text-transform: uppercase; padding: 1px 4px;  margin-left: 4px; font-size: 0.9em;   color: #997 !important;">sponsor</span></p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Lots of deep cloning with <code>JSON.parse</code> and <code>JSON.stringify</code>.</p>
  <p>Arjun Gadhia </p>
</td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0;  "><p>🔧 Code and Tools</p></td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   ">
  
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"> about <em>why</em> we need yet another chart library. It does sparklines, gauges, and heatmaps too.</p>
  <p>Juned Chhipa </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></p>
  <p>Alexander Buzin </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>MONGODB <span style="text-transform: uppercase; padding: 1px 4px;  margin-left: 4px; font-size: 0.9em;   color: #997 !important;">sponsor</span></p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Not something you often associate with JavaScript, but yes, you can explore brain signals from JS.</p>
  <p>Gilad Shoham </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Netlify </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Jon Abrams </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Only a minor point release, but the first in a few months.</p>
  
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Manage lists and tasks right from the terminal.</p>
  <p>Klaus Sinani </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>steelydylan </p>
</td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px;  ">
<table border=0 border=0><tr><td style=" font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   "></td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  "><div style="line-height: 1.3em; font-size: 1.4em; color: #555555;">📅 Some Forthcoming JavaScript Events</div></td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — A one day single track JS event taking place soon.</p>
  <p>JSCamp Chicago </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — One of the largest JavaScript events. Organized by The Linux Foundation.</p>
  <p>The Linux Foundation </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Already an impressive roster of speakers for this event with a focus on mobile, app, and IoT uses for JavaScript.</p>
  <p>Progress </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>JSConf </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  "><p>We're thinking of adding a permanent events section to JavaScript Weekly in future, so if you have an event you want to have listed, hit reply and let us know.</p></td></tr></table>
</td></tr></table>
<table border=0 border=0><tr><td style=" font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   "></td></tr></table>
</div>

  </td></tr>
</table>





<img src="https://javascriptweekly.com/open/397/rss" width="1" height="1" />
---------------
<h1 id="#title_1" >2、迷你书： 前端面试指南</h1>
InfoQ中文站
[http://www.infoq.com/cn/minibooks/interview-map?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/minibooks/interview-map?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/minibooks/interview-map/zh/smallimage/100-1533179148861.jpg"/><p>希望这个面试指南能够帮助到大家更好的准备面试。</p> <i>By InfoQ中文站</i>
---------------
<h1 id="#title_2" >3、视频演讲： 华为容器在Kubernetes上的技术实践之路</h1>
黄毽
[http://www.infoq.com/cn/presentations/the-technical-practice-of-huawei-container-on-kubernetes?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/the-technical-practice-of-huawei-container-on-kubernetes?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/presentations/the-technical-practice-of-huawei-container-on-kubernetes/zh/mediumimage/huangtan270-1532435967486.jpg"/><p>Kubernetes 拥有一套非常坚实的技术基础，站在了 Google 内部久经考验的容器管理系统 Borg 的肩膀上，同时也吸取了旨在替代 Borg 但是没有成功的 Omega 项目的失败经验。而在容器编排领域早期群雄混战的时代，华为是最早坚定支持K8s的企业，经过数年的深耕挖掘，已积累非常深厚的实践经验。本主题就将分享与大家分享华为在多年K8s深耕挖掘的实践经验和产品结晶。</p> <i>By 黄毽</i>
---------------
<h1 id="#title_3" >4、视频访谈： 七牛云宫静：研发组织实施CICD 需要注意些什么？</h1>
宫静
[http://www.infoq.com/cn/interviews/interview-with-gongjing-talk-implementing-cicd?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/interviews/interview-with-gongjing-talk-implementing-cicd?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/interviews/interview-with-gongjing-talk-implementing-cicd/zh/mediumimage/gongjing270-1533180041407.jpg"/><p>我们现在正在ArchSummit全球架构师峰会2018深圳站的现场，InfoQ很荣幸地邀请到了七牛云工程效率部技术专家 宫静老师来接受我们的采访，谈谈七牛云在实施CICD过程中的经验和教训。</p> <i>By 宫静</i>
---------------
<h1 id="#title_4" >5、We Are Just Getting Started: 1,000 Smashing Members</h1>
Vitaly Friedman
[https://www.smashingmagazine.com/2018/08/1000-smashing-members/](https://www.smashingmagazine.com/2018/08/1000-smashing-members/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/08/1000-smashing-members/" />
              <title>We Are Just Getting Started: 1,000 Smashing Members</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>We Are Just Getting Started: 1,000 Smashing Members</h1>
                  
                    
                    <address>Vitaly Friedman</address>
                  
                  <time datetime="2018-08-03T13:50:31&#43;02:00" class="op-published">2018-08-03T13:50:31+02:00</time>
                  <time datetime="2018-08-03T19:47:06&#43;00:00" class="op-modified">2018-08-03T19:47:06+00:00</time>
                </header>
                <p>We’ve all been there: bringing a new product to the market is a tough nut to crack. It requires patience, commitment, and a bit of healthy stubbornness. That's the exact attitude we started off with when we launched our shiny new  last October — a friendly and respectful community that keeps this website alive, along with books, webinars, discounts, networking, and a seasoned selection of fancy cats.</p>

<p>Thanks to the generous support of Smashing Members, we're incredibly honored to have crossed the <span class="small-caps">1,000</span> members mark today. This is a very important day for us, and frankly, it's quite flattering to see <span class="small-caps">1,000</span> people actively supporting our little site and sharing our goals. In fact, with Membership, sometimes it feels like walking around a small town in which <strong>everyone knows each other</strong> and their friends, and so we know many members by name, and we've also met some of them at Smashing Conferences. It's a wonderful <em>family</em> that shares similar values and wants to get better at their work. But it's also a family that wants to bring along a shift in the industry.</p>

<h3>The People Behind The Scenes</h3>

<p>When looking at obscure avatars and nicknames appearing in remote corners of the web, it's easy to forget that there are actually <em>real</em> people behind them. That's why it was important for us that the Membership experience is focused around <strong>real names and real faces</strong> of the community members &mdash; both on the new Smashing Magazine website and in our Membership Slack channel. It's the people who shape the community and make it feel like <em>home</em>, and so Membership should become a <em>humane</em> product, with approachable and friendly authors, contributors and attendees.</p>

<p>We reached out to a few members to ask them why out of all the wonderful resources on the web, they chose to support the red, cat-friendly, and quirky Smashing Magazine, and what they found useful or remarkably painful during their Membership so far.</p>

<figure class="author author--full">
  <a href="https://twitter.com/llexan">
    <div class="author__image-wrapper tilt">
      <div class="author__image">
        
<img src="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/84f56276-35e1-4e45-aa80-927debf4f973/allen-brady-180w.jpeg" alt="Allen Brady" width="180" height="180">
      </div>
    </div>
  </a>
  <figcaption class="author__desc" id="author__desc">
    <h3 class="author__desc__title">Allen Brady</h3>
    <p>
       is based in Knoxville, TN. He is passionate about building great experiences on the web for companies and their audiences. Currently he is learning to make the web more accessible with great HTML, CSS and inclusive design.
    </p>
  </figcaption>
</figure>

<blockquote style="clear: both;"><p>“I wanted to support Smashing Magazine as soon as they launched their membership program because not only have they been an excellent resource over the years with all the fantastic articles, books and conferences, but also because they’re so great at amplifying the voices in this industry, which is really important. I know that with my membership I’m getting a diverse range of perspectives that’s really helped shape me into a better developer.</p>
<p>The best part about this membership is the community. There’s a fantastic Slack group where you can talk about your projects, ask for help or just chat about whatever. The webinars have also been great. My favorite part is that we get to chat with the hosts and each other during the live recording. Involving the community in everything they can seems to be a theme with Smashing Magazine. It sets them apart from other resources out there and I love it.”</p></blockquote>
<br />

<figure class="author author--full">
  <a href="https://twitter.com/V__Verena">
    <div class="author__image-wrapper tilt">
      <div class="author__image">
        
<img src="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/534a9d96-2738-4705-afd8-4b826b9385e0/verena-vertonghen-180w.jpg" alt="Verena Vertonghen" width="180" height="180">
      </div>
    </div>
  </a>
  <figcaption class="author__desc" id="author__desc">
    <h3 class="author__desc__title">Verena Vertonghen</h3>
    <p>
      's journey in the development world started 6 years ago. She studied Multimedia Technology with a specialisation in Web&UX in Antwerp.
    </p>
  </figcaption>
</figure>

<blockquote style="clear: both;">“Now I'm a front-end developer who also picks up some design challenges from time to time. I love creating all sorts of things and going on walks with my dogs. Because Smashing Magazine has been an invaluable learning resource for me throughout my studies and my career. I decided on membership to support the continuation of all the great work that Smashing Magazine already offers. But also because you get even more goodies when you do.</p>
<p>Some of the things I really like about it are the eBooks, previews to articles, webinars and the Slack channel that gives me the opportunity to connect with people that have a similar profile. The user experience is overall really great, and SmashingMag cat mascot gives a very playful and personal vibe!”</blockquote>
<br />

<figure class="author author--full">
  <a href="https://twitter.com/EmilyEServen">
    <div class="author__image-wrapper tilt">
      <div class="author__image">
        
<img src="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ad0f56be-fd68-4bc3-b870-bb0cd92f6230/emily-serven-180w.png" alt="Emily Serven" width="180" height="180">
      </div>
    </div>
  </a>
  <figcaption class="author__desc" id="author__desc">
    <h3 class="author__desc__title">Emily Serven</h3>
    <p>
       is a recent college graduate and new member of the workforce. In her spare time, she like practicing photography, listening to foreign music, and occasionally playing Overwatch.
    </p>
  </figcaption>
</figure>

<blockquote style="clear: both;"><p>“I remember checking SmashingMag regularly as far back as middle school and have always loved the quality and steady quantity of content. I know I can trust the quality of writing on Smashing (especially considering there’s so much content and noise from other places to sift through nowadays)!</p>

<p>I’m also a cat person, for sure. I’ve found the available resources to be really useful (eBook library and book discounts), and I can’t wait for the printed magazine to come out. That’s the other thing about Smashing; even though the medium in which I express my work as a web dev is primarily digital, Smashing still recognizes the value of well-produced and attractive physical media. I love getting the physical books for that reason.</p>

<p>Oh, another thing. I used to freelance more back in middle school until I got my full-time position recently. When I found Smashing for the first time, I really loved how it really ‘got’ me and my job. There was coding, but also design (Photoshop, UX, etc.) and freelance articles specifically. It all felt very well balanced. I think that helped me develop my dev skills and the other auxiliary talents in a way that led to my holistic view of dev nowadays, too.</p></blockquote>
<br />

<figure class="author author--full">
  <a href="https://www.behance.net/user/?username=arthurleonov">
    <div class="author__image-wrapper tilt">
      <div class="author__image">
        
<img src="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d95b896c-bd51-4206-a317-f63cbf0cdf04/arthur-leonov-180w.png" alt="Arthur Leonov" width="180" height="180">
      </div>
    </div>
  </a>
  <figcaption class="author__desc" id="author__desc">
    <h3 class="author__desc__title">Arthur Leonov</h3>
    <p>
     is a product designer that also codes front-end.  He is a firm believer that merging design and technology can solve even the most difficult problems.
    </p>
  </figcaption>
</figure>

<blockquote style="clear: both;"><p>“I’m a designer that codes front-end. What a combo, right? I also believe that merging design and technology can solve even the most difficult problems in this world. The Smashing community keeps me inspired and informed day in and day out.</p>

<p>I catch up on SmashingMag every morning because it is one of the few online magazines in this industry who puts a lot of emphasis on good quality, relevant, and practical content.”</p></blockquote>

<p>It might sound like an overstatement, but these people have already made a difference. They’ve helped us initiate projects that we wouldn't be able to support otherwise. Now, don't get me wrong: with dwindling ad revenues facing us, of course our aim was to earn <em>enough</em> with the help of the Membership to keep the magazine independent and self-funded. But that’s just one side of the story. Our aim was also to <strong>support design education and new voices in the industry</strong>; reward great people doing great work; foster open, diverse, inclusive and accessible initiatives. Last but not least, we wanted to help community events and projects, and the people behind them.</p>

<p>Did we achieve <em>any</em> of these goals with the money we've earned? I'm glad you asked.</p>

<h3>So How Much Money Did We Earn? Total: <span class="small-caps">$33,128</span></h3>

<p>Initially, we were hoping to provide a larger financial support for new design/tech education initiatives and open-source projects, but with limited resources we had to be more realistic and pragmatic. We reached <strong><span class="small-caps">1,013</span> Smashing Members</strong> in <span class="small-caps">257</span> days, with <span class="small-caps">30</span> supporters, <span class="small-caps">562</span> members, and <span class="small-caps">421</span> smashers. That makes a current total of <strong><span class="small-caps">$6,689</span></strong> gross per month for August 2019.</p>

<p>Since the launch of the Membership, Smashing Members contributed a total of <span class="small-caps">$33,128</span> net over the course of <span class="small-caps">10</span> months (including current month):</p>

<table class="tablesaw break-out" data-tablesaw-mode="swipe" data-tablesaw-minimap>
<thead>
<tr>
<th>Month</th>
<th>Net revenue</th>
</tr>
</thead>
<tfoot>
<tr>
<th>Total</th>
<th><span class="small-caps">$33,128</span></th>
</tfoot>
<tr>
<td>November <span class="small-caps">2017</span></td>
<td><span class="small-caps">$1,104</span></td>
</tr>

<tr>
<td>December <span class="small-caps">2017</span></td>
<td><span class="small-caps">$1,530</span></td>
</tr>

<tr>
<td>January <span class="small-caps">2018</span></td>
<td><span class="small-caps">$2,130</span></td>
</tr>

<tr>
<td>February <span class="small-caps">2018</span></td>
<td><span class="small-caps">$2,181</span></td>
</tr>

<tr>
<td>March <span class="small-caps">2018</span></td>
<td><span class="small-caps">$2,748</span></td>
</tr>

<tr>
<td>April <span class="small-caps">2018</span></td>
<td><span class="small-caps">$4,015</span></td>
</tr>

<tr>
<td>May <span class="small-caps">2018</span></td>
<td><span class="small-caps">$4,440</span></td>
</tr>

<tr>
<td>June <span class="small-caps">2018</span></td>
<td><span class="small-caps">$4,750</span></td>
</tr>

<tr>
<td>July <span class="small-caps">2018</span></td>
<td><span class="small-caps">$4,990</span></td>
</tr>

<tr>
<td>August <span class="small-caps">2018</span></td>
<td><span class="small-caps">$5,240</span></td>
</tr>
</table>

<p>It goes without saying that these kind contributions massively helped us <strong>cover monthly costs</strong>, from maintenance to honorarium for authors, in particular:</p>

<ul>
  <li>Honorarium for authors contributing articles and chapters for Smashing Magazine, our eBooks and printed books,</li>
  <li>Honorarium for ,</li>
  <li>Honorarium for all ,</li>
  <li>All design education initiatives and community support is enabled by Smashing Membership,</li>
  <li>All money was reinvested in the Magazine and Membership projects.</li>
</ul>

<p>From day one, we kept things fully transparent; we've been sharing monthly reports on how much money we've earned and how we spent it. So <strong>here's what happened</strong> since the launch of Membership last year.</p>

<h3>Smashing TV: 24 Live Sessions</h3>

<p>Each month, we are proud to host <span class="small-caps">2</span> curated webinars for Smashing Members. We've teamed up with active members of the community to run <strong>1:1 interactive sessions</strong> with Smashing Members. Overall, we ran  on front-end, UX, ethics, performance, accessibility and design workflow. With Marcy Sutton, Val Head, Dan Rose, Ada Rose Cannon, Martin Splitt, Michael Riethmueller, Sara Soueidan, dina Amin, Rachel Andrew and Dan Mall, among others.</p>

<p>The goal of every session is to be highly practical and provide <strong>actionable insights and learnings</strong> &mdash; be it in front-end or in user experience. Everyone can also suggest topics for upcoming webinars in the Membership Slack channel, and we'll invite speakers to cover the topic. Of course, <strong>live recordings</strong> of these sessions are available as well, and are later released publicly for free for everybody.</p>

<figure class="video-container"><iframe data-src="https://player.vimeo.com/video/244888085" width="600" height="480" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe><figcaption>Smashing TV: &ldquo;Smashing Big Bang Redesign&rdquo; with Vitaly Friedman</figcaption></figcaption></figure>

<h3>Design/Tech Courses And Trainings</h3>

<p>These days there is always something to do, learn, or wrap your head around these days, and because all of us tend to get lost in small details, video tutorials and courses can be quite helpful. There are of course huge video course platforms which are wonderful, but there are also many fantastic <em>one-man-show</em>-teachers out there in the community who produce courses and tutorials for everybody to learn from.</p>

<p>That's why we've teamed up with some of these teachers to provide <strong>community discounts for training and video courses</strong>. For example, for a  by Wes Bos &mdash; with many more courses coming up over the next months.</p>

<h3>Supporting Community Initiatives</h3>

<p>It's not easy to maintain and grow a community, and we are proud to <strong>help community initiatives</strong> around the world to connect like-minded designers and developers.</p>

<p>Here are the projects we've supported so far:</p>

<ul>
  <li> (<em>Kiev, Ukraine</em>),</li>
  <li> (<em>Minsk, Belarus</em>),</li>
  <li> (<em>Tel-Aviv, Israel</em>),</li>
  <li> (<em>London, UK</em>),</li>
  <li> (<em>Osijek, Croatia</em>),</li>
  <li> (<em>Porto, Portugal</em>),</li>
  <li> (<em>Berlin, Germany</em>),</li>
  <li> (<em>Amsterdam, Netherlands</em>),</li>
  <li> (<em>Bratislava, Slovakia</em>),</li>
  <li> (<em>Kyiv, Ukraine</em>),</li>
  <li> (<em>Amsterdam, Netherlands</em>),</li>
  <li> (<em>Moscow, Russia</em>),</li>
  <li> (<em>Toronto, Canada</em>),</li>
  <li>Local communities in <em>Kairo, Egypt</em>.</li>
</ul>

<p>If you are running a meet-up or a community in your city, we'd be happy to support you as well. Just  and tell us a bit about your community, and we'll make it happen!</p>

<h3>Smashing Book 6: New Frontiers In Web Design</h3>

<p>It took us a while, but we are almost there. The brand new  is coming out early September, with contributions by Laura Elizabeth, Marcy Sutton, Rachel Andrew, Mike Riethmuller, Harry Roberts, Lyza Gardner, Yoav Weiss, Adrian Zumbrunnen, Greg Nudelman, Ada Rose Cannon, and yours truly.</p>

<p>It explores <strong>common pain points and solutions from real-world</strong> projects: be it accessibility in times of single-page apps, performance loading patterns, making design systems work in real-life, AR/VR, responsive art-direction, building an advanced service worker and designing for next-gen interfaces. A book packed with practical advice for designers and developers alike, designed and illustrated by .</p>











<figure class="article__image break-out">
	<a href="https://www.smashingmagazine.com/printed-books/smashing-book-6-new-frontiers-in-web-design/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a951b2e1-f8a3-4200-b709-b065a021a729/smashing-book-6-wooden-floor-800.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a951b2e1-f8a3-4200-b709-b065a021a729/smashing-book-6-wooden-floor-800.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a951b2e1-f8a3-4200-b709-b065a021a729/smashing-book-6-wooden-floor-800.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a951b2e1-f8a3-4200-b709-b065a021a729/smashing-book-6-wooden-floor-800.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a951b2e1-f8a3-4200-b709-b065a021a729/smashing-book-6-wooden-floor-800.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a951b2e1-f8a3-4200-b709-b065a021a729/smashing-book-6-wooden-floor-800.jpg"
			sizes="100vw"
			alt="The cover of the Smashing Book 6, with geometric objects shaping the letter S."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			)
		</figcaption>
	
</figure>


<p>The book is being finished as we speak, but we've been slowly releasing chapters, so <strong>Members can actually start reading the book already</strong> before its official release. All new books and eBooks &mdash; as well as upcoming <strong>Smashing Print magazine</strong> (currently in the works) &mdash; is made available for Members free of charge. But that goes without saying, doesn't it?</p>

<h3>Smashing Diversity Program</h3>

<p>There is a huge amount of discrimination out there, and not everybody is getting a fair chance even though they deserve one. That's why we've launched a  program, providing conference and workshop tickets for students, non-profits, and people who might not be able to afford a conference ticket or attend a workshop. We also make sure that our conference volunteers can attend the sessions they'd love to see.</p>

<p>Beyond that, please  to provide mentorship, training, and opportunities to up-and-coming speakers from all over the world.</p>

<h3>Support New Wave Of Digital Education</h3>

<p>Tiego Pedras and Sara Ramos run the  last year. Their goal is to provide students with better front-end and design education to be ready for real-life world.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6302faf7-81eb-478a-80c8-6a409d0071f7/1-new-digital-school.JPG">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6302faf7-81eb-478a-80c8-6a409d0071f7/1-new-digital-school.JPG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6302faf7-81eb-478a-80c8-6a409d0071f7/1-new-digital-school.JPG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6302faf7-81eb-478a-80c8-6a409d0071f7/1-new-digital-school.JPG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6302faf7-81eb-478a-80c8-6a409d0071f7/1-new-digital-school.JPG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6302faf7-81eb-478a-80c8-6a409d0071f7/1-new-digital-school.JPG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6302faf7-81eb-478a-80c8-6a409d0071f7/1-new-digital-school.JPG"
			sizes="100vw"
			alt="Each group of students had their own project to work on at The New Digital School."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Each group of students had their own project to work on at )
		</figcaption>
	
</figure>












<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/608ecf33-181e-4c0b-82df-8f47c11486cd/2-new-digital-school.JPG">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/608ecf33-181e-4c0b-82df-8f47c11486cd/2-new-digital-school.JPG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/608ecf33-181e-4c0b-82df-8f47c11486cd/2-new-digital-school.JPG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/608ecf33-181e-4c0b-82df-8f47c11486cd/2-new-digital-school.JPG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/608ecf33-181e-4c0b-82df-8f47c11486cd/2-new-digital-school.JPG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/608ecf33-181e-4c0b-82df-8f47c11486cd/2-new-digital-school.JPG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/608ecf33-181e-4c0b-82df-8f47c11486cd/2-new-digital-school.JPG"
			sizes="100vw"
			alt="Students presented their projects and shared their results with the group."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Students presented their projects and shared their results with the group. (Image source: )
		</figcaption>
	
</figure>


<p>For two years in a row now, I was honored to be able to explore the current state of front-end, interface design, and responsive art-direction with students from all over the world. In February this year, I headed to Porto to spend a week with students from India, Malaysia, Portugal, France and USA for an entire week. Each group of students was working on their own project, ranging from <strong>interactive VR storytelling</strong> to (<em>hello, Miguel and Sarthak!</em>) to Olympics leaderboards (<em>and hello to you, Prashant and Marissa!</em>).</p>

<p>It might not sound like a big deal, but it was so rewarding to see the sparkle in the eyes of the students as they were working on their projects. Being able to provide an experience that hopefully many students will remember was a huge privilege and a remarkable moment in the entire experience. And it was all possible thanks to the contributions of our Smashing Members. I couldn't be more proud of this effort.</p>

<h3>Berlin Design Campus</h3>

<p>Late June is usually quite slow, with most projects slowly fading into sleep mode. Well, it was quite the opposite for us. For June, we teamed up with  — a week-long trip to Berlin to explore digital design agencies and studios with students from Ukraine. It was <strong>our first initiative to improve design education</strong> by setting up a project of our own.</p>

<p>We visited the offices of  (previously <em>EdenSpiekermann</em>, <em>Thoughtworks</em>) with hands-on workshops in those companies throughout the week.</p>











<figure class="article__image break-out">
	<a href="https://twitter.com/smashingmag/status/1020197461858676736">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f4188193-6e2c-4515-affa-9b528ba34758/berlin-design-campus-2018.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f4188193-6e2c-4515-affa-9b528ba34758/berlin-design-campus-2018.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f4188193-6e2c-4515-affa-9b528ba34758/berlin-design-campus-2018.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f4188193-6e2c-4515-affa-9b528ba34758/berlin-design-campus-2018.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f4188193-6e2c-4515-affa-9b528ba34758/berlin-design-campus-2018.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f4188193-6e2c-4515-affa-9b528ba34758/berlin-design-campus-2018.jpg"
			sizes="100vw"
			alt="Branding and visuals for Berlin Design Campus, designed by Prjctr Design School in Kiev, Ukraine."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			We couldn't be more proud to team up with )
		</figcaption>
	
</figure>


<p>We visited both <strong>design agencies and larger consultancy firms</strong>, spoke with local freelancers, artists and entrepreneurs. We've set up <strong>informal evening meetings</strong> in which students could ask questions, and we organized visits to offices so students could see how other professionals work. It was a fascinating week with practical insights you would never get otherwise; a look behind the scenes in actual real-life projects with early prototypes that failed and hands-on exercises to work on.</p>











<figure class="article__image break-out">
	<a href="https://twitter.com/smashingmag/status/1020197782332891136">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6e61139f-2b10-4b19-b948-b4ac9f5f26af/students-visiting-consultancy-firms.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6e61139f-2b10-4b19-b948-b4ac9f5f26af/students-visiting-consultancy-firms.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6e61139f-2b10-4b19-b948-b4ac9f5f26af/students-visiting-consultancy-firms.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6e61139f-2b10-4b19-b948-b4ac9f5f26af/students-visiting-consultancy-firms.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6e61139f-2b10-4b19-b948-b4ac9f5f26af/students-visiting-consultancy-firms.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6e61139f-2b10-4b19-b948-b4ac9f5f26af/students-visiting-consultancy-firms.jpg"
			sizes="100vw"
			alt="Ukrainian students visiting design agencies in Berlin."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			During Berlin Design Campus, we visited a number of offices in Berlin. One of them was Mozilla's office, with a hands-on workshop by )
		</figcaption>
	
</figure>


<p>You never get to visit or see how designers in those respected companies work, and what their processes look like. So happy and honored to be a part of this little initiative, and looking forward to more adventures in the future. Again, made possible through contributions of wonderful Smashing Members.</p>

<h3>New SmashingConf Experience</h3>

<p>With a few more resources available to us, we were able to focus on exploring new formats for Smashing Conferences. Being inspired by our Italian friends from the , we tested a brand new format in Toronto earlier this year: <strong>interactive live sessions</strong> in which speakers were not allowed to use slides (be it Powerpoint, Keynote or Reveal.js). Instead, we encouraged speakers to show how they work, how they design and build, what their setup looks like, and give audience insights into how they <em>think</em> as they make progress in their work.</p>











<figure class="article__image break-out">
	<a href="https://www.flickr.com/photos/marcthiele/sets/72157670813337918/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a4470aa5-fd4a-4589-b51f-3e335839257c/gemma-o-brien-smashingconf-toronto-18.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a4470aa5-fd4a-4589-b51f-3e335839257c/gemma-o-brien-smashingconf-toronto-18.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a4470aa5-fd4a-4589-b51f-3e335839257c/gemma-o-brien-smashingconf-toronto-18.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a4470aa5-fd4a-4589-b51f-3e335839257c/gemma-o-brien-smashingconf-toronto-18.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a4470aa5-fd4a-4589-b51f-3e335839257c/gemma-o-brien-smashingconf-toronto-18.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a4470aa5-fd4a-4589-b51f-3e335839257c/gemma-o-brien-smashingconf-toronto-18.jpg"
			sizes="100vw"
			alt="Gemma O’Brien presenting with no slides at SmashingConf Toronto 2018"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			One of those unforgettable moments. When Gemma O’Brien brought her entire studio to SmashingConf Toronto, a conference where speakers weren’t allowed to use slides. We’ll be rolling out this format at all Smashing events in 2019. (Image credit: )
		</figcaption>
	
</figure>


<p>Instead of speaking in front of a podium, we set up a <strong>coffee shop-alike setting</strong> with speakers sitting at the desk and literally walking the audience through their thought process. It was a quite special event. Some speakers felt , along with lightning talks, design nights, and a book exchange board. It goes without saying: all Smashing Members are getting a heavy discount on all Smashing Conferences.</p>

<h3>Giving Back To The Community</h3>

<p>Of course, Smashing Magazine has always been free, but with  — all thoroughly reviewed and edited by the Smashing Editorial team. We refocus back on the heart of it all — yours truly Smashing Magazine.</p>

<p>We are committed to make the content we get out there accessible to as many people as possible. That goes for our eBooks as well. That's why we also publicly released ), a wonderful book on inclusive design patterns &mdash; for free. Why? Because accessibility matters.</p>

<h3>We Are Just Getting Started</h3>

<p><span class="small-caps">1,000</span> is a first major milestone for us. Not many people know it, but the entire Smashing team is actually quite small, with just <span class="small-caps">13</span> of us floating from one project to another. Frankly, we might be a bit slow at times, but we are trying our best to bring along a positive change to our industry.</p>

<p><strong>We need less craziness and narrow-mindedness around us</strong>, and we need more respect, care, and constructive help. That's the goal we are aiming to provide with the Smashing Membership, with our next projects, and with <em>your</em> help. . We are in it for a long game. We are, after all, just getting started.</p>

<p><em>Huge thank you to  for his kind support and work on the Smashing Membership. You are truly smashing!</em></p>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(cm, sw, il)</span>
</div>




<aside class="product-panel product-panel__tilted product-panel--book" data-audience="non-subscriber">
    <div class="container product-panel--book__container">
      <div class="panel__description panel__description--book">
    <p>With so much happening on the web, what should we really pay attention to? At . Oct <span class="small-caps">23–24</span>.</p>
      <a href="http://smashed.by/confpanelspeakers" class="btn btn--green btn--large">
        Check the speakers&nbsp;→
      </a>
      </div>
      <div class="panel__image panel__image--book">
        <a href="http://smashed.by/confpanelspeakers" class="books__book__image">
        <div class="books__book__img">
          <img src="https://res.cloudinary.com/indysigner/image/upload/v1529498640/sarah-drasner-opt_kaxhos.png" alt="SmashingConf New York 2018, with Dan Mall, Sara Soueidan, Sarah Drasner and many others." width="310" height="400">
        </div>
      </a>
      </div>
    </div>
  </aside>




              </article>
            </body>
          </html>
---------------
<h1 id="#title_5" >6、甲骨文中国数据库中心将落地，与微软数据库市场两家独大</h1>
陈利鑫
[http://www.infoq.com/cn/news/2018/08/Oracle-database-center?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/08/Oracle-database-center?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>甲骨文筹谋已久的中国数据库中心也将在本周落地，并计划推出自治事务处理服务。</p> <i>By 陈利鑫</i>
---------------
<h1 id="#title_6" >7、每周分享第 16 期</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2018/08/weekly-issue-16.html](http://www.ruanyifeng.com/blog/2018/08/weekly-issue-16.html)
<p>这里记录过去一周，我看到的值得分享的东西，每周五发布。</p>

        <p><img src="https://www.wangbase.com/blogimg/asset/201808/bg2018080301.jpg" alt="" title="" /></p>

<p>影视作品经常出现，病人的心脏停止跳动，医生使用两块电极板对心脏电击。它叫除颤器（defibrillator），通过放电刺激心脏恢复跳动。</p>

<p>除颤器必须在心跳停止以后立刻使用，拖延越久，希望越渺茫。可想而知，大部分心脏停止的病人是死定的。据统计，美国每年心脏骤停有35万人，其中90%以上都没有抢救的机会。医生们于是想到了，能不能把除颤器放在体内呢？</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201808/bg2018080302.jpg" alt="" title="" /></p>

<p>体内除颤器就是这样发明的。这个装置放在心脏衰弱的病人体内，自动检查心脏骤停，一旦发现立刻电击。它救了很多人，但带来了另一个问题。那些心脏衰弱的病人，即使抢救回来，心脏还是衰弱的，而且由于经受了一次电击，会变得比以前更衰弱。病人很可能不久就会发生另一次心脏骤停，或者心脏越来越弱，无法满足身体新陈代谢的需要，导致其他器官慢性衰竭。也就是说，除颤器只是推迟了死亡的时间和方式，病人从死于心脏骤停变成死于慢性衰竭。</p>

<p>安装"体内除颤器"需要病人的同意，毕竟是一个大手术。《纽约时报》就有一篇心脏医生的，他认为这迫使病人选择自己的死亡方式：你要死得快而无痛，还是慢而痛苦？他举例，一个心脏病人虽然抢救回来了，但是肺部逐渐衰竭，严重积液，导致每一口呼吸都非常困难，最终在窒息的痛苦中慢慢死去。</p>

<p>我觉得，这种问题是技术带来的，也只有靠技术解决。如果技术可以让病人免于骤死，那么可能也能免于慢性衰竭。心脏衰竭了，就换人工心脏；肺衰竭了，就装人工肺。到了那时，人类好像就不那么容易死亡了，只是一刻都离不开机器了，一旦停电或机器故障，立马就没命了。</p>

<h2>新闻</h2>

<p>1、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201808/bg2018080303.jpg" alt="" title="" /></p>

<p>1912年，科学家发现，地球每天都在遭受高能粒子的撞击。这些粒子的能量非常大，因此必定有一个地方在源源不断地射出它们，然后地球正好在这些粒子的喷射轨道上。但是，一百多年来，科学家都没有答案，到底什么地方在喷射高能粒子？</p>

<p>上个月终于发现了，宇宙射线的来源之一是一个叫做 blazar 的星系。它的中心有超大质量的黑洞，将吸入的物质撕成粒子，然后像激光炮一样将这些粒子抛向太空。</p>

<p>2、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201808/bg2018080304.jpg" alt="" title="" /></p>

<p>亚马逊公司的股票不断上涨，创始人贝佐斯成为世界首富，还成为现代历史上最有钱的人。</p>

<p>他的财富估计为1500亿美元。第二位的比尔·盖茨大概拥有953亿美元。不过，盖茨捐掉了近7亿股微软股票和29亿美元现金。如果算上这些钱，那么他的净资产将超过1500亿美元。</p>

<p>3、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201808/bg2018080305.jpg" alt="" title="" /></p>

<p>美国科学家公布了一种消除图片噪点的 AI 算法。这种算法可以从有噪点的图片推断出原图。上面第一张图是原图，第二张是算法处理的结果，第三张是没有噪点的实际图像。</p>

<p>4、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201808/bg2018080306.jpg" alt="" title="" /></p>

<p>很多公司都在开发可以飞行的汽车，不少已经做出了成品。BlackFly 是最接近完成的一个产品。</p>

<p>它可以用100公里/小时的速度，飞行40公里。能量来自电池，一次充电需要30分钟。下图后面的架子是它的充电器。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201808/bg2018080307.jpg" alt="" title="" /></p>

<p>它是垂直起降的，带有八个推进器，分布在两个机翼上，只能载一个人。出品公司宣称，已经进行了多年1400多次的测试，飞行距离超过12,000多英里。</p>

<p>5、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201808/bg2018080308.jpg" alt="" title="" /></p>

<p>美国一家媒体根据员工体验，对财富500强的工作环境进行了排名。员工心目中的最佳工作场所前三名依次是 Facebook、西南航空和 Salesforce。下面是对它们的评语。</p>

<blockquote>
  <ul>
<li>Facebook：工作场所充满活力。人员都经验丰富，能力极强。管理层坚定但乐于助人。团队合作至关重要。</li>
<li>西南航空：精彩的管理，令人敬畏的同事，鼓励个性和进步。</li>
<li>Salseforce： 快节奏，具有挑战性的项目和聪明的人以及酷炫有趣的文化相结合。无论头衔或职级如何，你都可以发表自己的声音和意见，尽管有疯狂的工作安排，但有趣的氛围可以平衡。</li>
</ul>
</blockquote>

<p>6、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201808/bg2018080309.jpg" alt="" title="" /></p>

<p>目前，互联网视频大部分采用 H.264 编码方案。这个方案是有专利的，使用必须付费。即使你可以在 Youtube 这样的视频网站免费观看视频，但是 Youtube 必须为使用 H.264 每年支付几百万美元。</p>

<p>为了有一个彻底开放的视频编码方案，也为了更好的性能，2015年多家软件和硬件厂商成立了 AOMedia 联盟。现在，新的视频编解码器  终于问世了。AV1 主要基于谷歌的 VP9 编码方案，并加入了其他代码。AV1是无版权的，任何人都可以免费使用。它比 H.264 提供更高效的压缩，大约高出30％。</p>

<p>7、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201808/bg2018080310.jpg" alt="" title="" /></p>

<p>特斯拉老板马斯克旗下的 Boring Company，不久前中标芝加哥市地下快运系统，挖一条隧道，连接市中心到机场。</p>

<p>Boring Company 披露了这个系统的细节。它依靠电动轨道车承运旅客，单车载客8~16人，时速最高240公里，每30秒一班，单程12分钟，比现有的客运系统节约70%的时间。施工时间最短18个月，最长可能要3年。</p>

<p>8、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201808/bg2018080311.jpg" alt="" title="" /></p>

<p>Nvidia 公司宣布了一种 Super Slomo 技术，可以用人工智能生成慢镜头。</p>

<p>常规的做法是，摄像机每秒拍摄240帧，然后以每秒30帧的速度播放，从而达到放慢8倍的效果。这种新技术可以基于普通视频，自动生成多余的帧，从而达到超级慢镜头的效果。</p>

<p>9、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201808/bg2018080312.jpg" alt="" title="" /></p>

<p>美国一所大学发明了智能绷带，上面有传感器和药物。传感器监控伤口的 pH 值，实现智能给药。这对于慢性伤口非常有效。</p>

<p>10、</p>

<p>历史上，从来没有一家美国公司达到 10000 亿美元的市值。现在，五家公司正在接近这个金额。</p>

<blockquote>
  <ul>
<li>Apple：9240亿美元</li>
<li>亚马逊：8480亿美元</li>
<li>Alphabet：8140亿美元</li>
<li>微软：7820亿美元</li>
<li>Facebook：5870亿美元</li>
</ul>
</blockquote>

<p>这五家公司合计占标准普尔500指数总市值的16.5％。这个比例虽然不是历史最高，但这五家公司都是同一个行业的，这是历史上从来没有的。</p>

<p>最新消息是，苹果公司已经达到了1万亿美元市值。但是，媒体发现2007年有一家也曾有一万亿美元市值，因此苹果公司只能排在历史第二。2007年，中国石油在上交所上市，第一天的开盘价是48元，市值超过1万亿美元，成为全球最大公司。但是，它只在那个位置待了一天，然后不断下跌，再也没有涨回去过。</p>

<p>11、<strong>一句话新闻</strong></p>

<ul>
<li> 的最新 PR，把编译后端从 Node 改成了LLVM，使得 JS 可以编译成 webAssembly 甚至汇编语言了。</li>
<li>GitHub ，改用标准 JS 操作 DOM。jQuery 的历史使命已经完成，正在退出前端开发的工具箱。</li>
<li>发布 Linux 版本。</li>
</ul>

<p><img src="https://www.wangbase.com/blogimg/asset/201808/bg2018080313.jpg" alt="" title="" /></p>

<h2>教程</h2>

<p>1、（英文）</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201808/bg2018080314.jpg" alt="" title="" /></p>

<p>图（graph）是一种数据结构，由点（vertex）和边（edge）组成。本文介绍图结构的算法基本知识。</p>

<p>2、（英文）</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201808/bg2018080315.jpg" alt="" title="" /></p>

<p>上面这幅欧洲油画是什么时候画的，15世纪还是17世纪？</p>

<p>这种问题恐怕要熟悉欧洲艺术的专家才能回答。现在，有人写了一个神经网络教程，介绍如何用算法判断油画的年代。</p>

<p>3、（英文）</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201808/bg2018080316.jpg" alt="" title="" /></p>

<p>这篇文章教你如何手写一个 SVG 文件，作为网页的背景图案。</p>

<p>4、（英文）</p>

<p>全球气候正在变暖，这到底是怎么一回事，原因是什么。本文是我读过最好的这方面的入门读物。</p>

<p>5、（中文）</p>

<p>大型 Web 应用最关键的就是架构，最难的也是架构。这份教程整理了这方面需要知道的知识。</p>

<p>6、（英文）</p>

<p>Webpack 是 JS 代码的打包器，现在前端开发的主流工具。Webpack 4 是它的最新版本。</p>

<p>7、（英文）</p>

<p>SSH 的作者回忆， ftp 端口是21，telnet 的端口是23，他就挑了中间剩下的22。 </p>

<p>8、（英文）</p>

<p>作者认为应该避免使用 PDF 格式。一般情况下，HTML 格式是更好的选择。如果要求保证精确的打印效果，可以使用压缩的 Postscript 格式。</p>

<p>9、（英文）</p>

<p>这篇文章解释，为什么以后发布应用的时候，不是直接发布在服务器上，而是通过 Kubernetes 发布。</p>

<h2>工具</h2>

<p>1、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201808/bg2018080317.jpg" alt="" title="" /></p>

<p>微软推出了一个团队协作工具，可以让用户在多种设备上，远程实时分享电子白板。目前，它只有 Windows 10 的客户端，但马上就会推出 iOS 客户端和 Web 版本。</p>

<p>2、</p>

<p>有的图片 CDN 可以对图片进行实时处理，允许指定图片的大小和方向。thumbor 就是这样一种图片服务器。</p>

<p>3、</p>

<p>Go 语言写的自然语言处理工具，目前只能处理英语。</p>

<p>4、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201808/bg2018080318.jpg" alt="" title="" /></p>

<p>一个网页游戏，玩家通过组合虚拟电路，组装出一台计算机。</p>

<p>5、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201808/bg2018080319.jpg" alt="" title="" /></p>

<p>一个管理本地视频的免费桌面软件，可以预览、搜索、分类各类视频文件。</p>

<p>6、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201808/bg2018080320.jpg" alt="" title="" /></p>

<p>一个基于 WebRTC 技术的实时通讯平台，可以实现 P2P 的文字聊天、语音和视频对话。</p>

<p>7、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201808/bg2018080321.jpg" alt="" title="" /></p>

<p>一个使用系统原生组件开发桌面应用的框架，相比 Electron，好处就是打包出来的体积比较小。</p>

<p>8、</p>

<p>一个开源的多端笔记本工具，兼容 Evernote。</p>

<p>9、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201808/bg2018080322.jpg" alt="" title="" /></p>

<p>Browsh 是一个基于 Firefox 的命令行脚本，可以在命令行打开网页，并且渲染出大致的样子。它也可以用作移动端网页浏览的处理方案。</p>

<h2>资源</h2>

<p>1、（PDF）</p>

<p>开源电子书，从零开始介绍汇编语言，读者必须懂一点 C 语言。内容很全，也非常厚。</p>

<p>2、</p>

<p>这个培训课程帮助学员深入理解机器学习的概念，技术和数学框架。一共30个讲座，包括一整套课后作业。</p>

<p>3、</p>

<p>麻省理工学院开发的一个类似 Unix 的教学操作系统。</p>

<p>4、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201808/bg2018080323.jpg" alt="" title="" /></p>

<p>中国开发者写的英语专著，介绍前端测试。书放在 Leanpub，付不付费、付多少钱都是自愿的。</p>

<p>5、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201808/bg2018080324.jpg" alt="" title="" /></p>

<p>《网站可靠性工作手册》一书现在免费下载，谷歌官网提供，为期一个月。</p>

<h2>文摘</h2>

<p>1、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201808/bg2018080325.jpg" alt="" title="" /></p>

<p>郭台铭创业初期，好不容易有了进一步投资的钱，当时有两个选择：一是买地自己盖厂房，然后买人家的模具；二是租别人的厂房，自己买机床开发模具，加强研发能力。</p>

<p>他选择了后者。结果几年后，地价一口气涨了10倍，房东大幅上涨房租，而模具还没开发出来，还在摸索中，因此苦不堪言，经济很窘迫。但是，郭台铭后来说，幸好选择了后者，因为房价到一定程度就不再快速上涨了，靠房地产只能赚一次的钱，但是一旦掌握了核心技术，可以赚无数次钱。</p>

<p>2、</p>

<p>1483年，31岁的达芬奇离开故乡，来到米兰。他没钱，需要找工作，就给米兰公爵写了一封求职信。</p>

<p>这封信写得极好，公爵一看就认定达芬奇是一个人才，从而给他资助。即使在今天，这样的信依然能帮你找到工作。</p>

<blockquote>
  <p>尊敬的，显贵的公爵阁下：</p>

<p>我是来自佛罗伦萨的作战机械发明者达·芬奇，希望可以成为阁下您的军事工程师，同时求见阁下，以便面陈机密：</p>

<p>一、我能建造坚固、轻便又耐用的桥梁，可用来野外行军。这种桥梁的装卸非常方便。我也能破坏敌军的桥梁。</p>

<p>二、我能制造出围攻城池的云梯和其他类似设备。</p>

<p>三、我能制造一种易于搬运的大炮，可用来投射小石块，犹如下冰雹一般，可以给敌军造成重大损失和混乱。</p>

<p>四、我能制造出装有大炮的铁甲车，可用来冲破敌军密集的队伍，为我军的进攻开辟道路。</p>

<p>五、我能设计出各种地道，无论是直的还是弯的，必要时还可以设计出在河流下面挖地道的方法。</p>

<p>六、倘若您要在海上作战，我能设计出多种适宜进攻的兵船，这些兵船的防护力很好，能够抵御敌军的炮火攻击。......</p>

<p>九、如果战斗发生在海上，我打算建造能够抵抗最猛烈炮火和烟尘的船只。</p>

<p>十、和平时期，我相信在建筑上，以及从一地到另一地的引水工程上，我一样可以像其他人那样令您完全满意。......</p>

<p>此外，我还擅长建造其他民用设施，同时擅长绘画和雕塑。</p>

<p>如果有人认为上述任何一项我办不到的话，我愿在您的花园，或您指定的其他任何地点进行试验。</p>

<p>谨此无限谦恭之忱，向阁下问安!</p>

<p>列奥纳多·迪·皮耶罗·达·芬奇</p>
</blockquote>

<p>3、</p>

<p>1931年，西澳大利亚州的阿里德角半岛，一些自然爱好者在灌木丛生的荒原上，发现了一种没人见过的昆虫。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201808/bg2018080326.jpg" alt="" title="" /></p>

<p>它看上去隐约有点蚂蚁的模样，可却是一种不寻常的淡黄色，还有一双奇怪的眼睛，很惹眼，显得异常局促不安。人们收集了一些标本，送到墨尔本维多利亚国家博物馆某位专家的桌上，专家立马就认定这种昆虫是巨响蚁。这一发现使人们极为兴奋，因为据人类所知，类似的东西不存于地球已经1亿年之久了。巨响蚁是一种原始蚂蚁，是蚂蚁自黄蜂开始的进化过程中某一时段的活化石。在昆虫学领域，这非凡卓越得就仿佛有人发现一群三角龙在某个遥远的草原上啃草一样。</p>

<p>考察队立刻组织起来，可是，虽然进行了最为一丝不苟的搜寻，但没人找得到阿里德角蚁群。之后的寻找也同样空手而回。</p>

<p>差不多过了半个世纪，当传闻一队美国科学家正计划寻找这种蚂蚁，而且几乎肯定会带上那种让澳大利亚人显得业余且组织不力的高科技精巧装置的时候，堪培拉的官方科学家们决定先发制人，为找到这种蚂蚁的活体做最后一次努力。于是，他们组织了一队人马出发横穿整个国家。</p>

<p>野外的第二天，正开车经过南澳大利亚州荒漠的时候，一辆车冒烟了，开起来啪啪啪地乱响，他们被迫打破日程，在公路上的一处偏僻驿站普彻拉停留一晚。晚间，科学家鲍勃·泰勒踱步出来透透气，无所事事之间把玩着手电筒，光柱扫向周围的地面。你可以想象出他的惊诧莫名啦，他发现，在他们营地附近一棵桉树树干上爬过的那队人丁兴旺的蚁群不是巨响蚁又是什么。</p>

<p>现在，我们来考虑一下可能性的问题。泰勒和他的同事距他们预定搜寻地有800英里之遥。在澳大利亚约摸3百万平方英里的旷野中，一小撮能够识别地球上最稀有、最吃香的虫子的人中的一个找到了这种虫子----它的活体只被人看见过一趟，还是差不多半个世纪之前----而这统统是因为他们的车子在此处抛锚了。其附带结果便是，巨响蚁至今仍旧没有在其原发现地被找到。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201808/bg2018080327.jpg" alt="" title="" /></p>

<h2>本周图片</h2>

<p>1、</p>

<p>有一个数学难题，怎样的多边形可以铺满一个平面？数学家已经证明，任意三角形和四边形都可以，五边形不确定，六边形只有三种可以，其他都不行。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201808/bg2018080328.jpg" alt="" title="" /></p>

<p>上图是目前找到的所有15种五边形，可以平铺平面。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201808/bg2018080329.jpg" alt="" title="" /></p>

<p>其中的第15种五边形，2015年发现的。</p>

<p>2、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201808/bg2018080330.jpg" alt="" title="" /></p>

<p>根据谷歌搜索指数，Python 语言过去10年一直在上升，现在已经是最热门的编程语言。（图片来源《经济学家》杂志）</p>

<p>3、（组图）</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201808/bg2018080331.jpg" alt="" title="" /></p>

<p>圣赫勒拿岛最著名的景点，当然是拿破仑故居和空的拿破仑墓。1815年，拿破仑被流放到这里，1821年去世安葬在岛上的墓地。1840年法国政府将灵柩移回巴黎，买下岛上三块拿破仑有关土地，并入法国领土，成为"在英国海外领地上的法国海外领土"。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201808/bg2018080332.jpg" alt="" title="" /></p>

<p>拿破仑故居门口立着牌子，禁止拍照，不过没有监控，靠自觉。我是2018年这个别墅的第一个参观游客，在别墅里忍不住，拍了一些内部照片。里面的所有家具和设施完全是原物原样，没有任何变化，让你觉得好像拿破仑昨天才在这里去世。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201808/bg2018080333.jpg" alt="" title="" /></p>

<p>往山下开一段路，就是另一块法国领土，拿破仑墓。当然，是空的，灵柩已经移回巴黎。这块墓地占的区域很大，由松木屑铺成防滑的山路一直走下去。没人看管，任何时候都可以来。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201808/bg2018080334.jpg" alt="" title="" /></p>

<p>我住的旅馆，由英国遗民Hazel老太太经营。其中一部分是2008年从所罗门家族买来的，包括书房，大部分都保持原样几百年。临走前一天，Hazel告诉我，她接到一个叫信天翁的旅游agent订单，有11个北京来的中国团第二天到。然后她有点担心地问我，他们会不会在房间 cooking?</p>

<p>以前有一个中国人住的时候，在房间煮面方便面，弄得房间都是味道。我想了一下，觉得非常有可能。于是我帮她写了5页纸的中文 tips，希望他们不要在房间煮面，另外也尽可能告知了一些岛上的吃喝玩乐地方，不晓得最后这11位中国同胞看到没有。</p>

<h2>本周金句</h2>

<p>1、</p>

<p>圆明园的兽头，原本是喷水池的水龙头。它们不太可能是八国联军抢走的，因为圆明园珍宝如山，八国联军会抢这种仿制西方的喷头吗？它们十有八九是圆明园废弃后，中国人自己弄下来卖掉的。（）</p>

<p>2、</p>

<p>你存心做一个与世无争的老实人吧，人家就利用你欺侮你。你稍有才德品貌，人家就嫉妒你排挤你。 你大度退让，人家就侵犯你损害你。你要不与人争，就得与世无求，同时还要维持实力准备斗争。你要和别人和平共处，就先得和他们周旋，还得准备随时吃亏。 （）</p>

<p>3、</p>

<p>摩尔定理有一个后果，每隔几年，我们就要学习一个新的希腊语前缀：mega-、giga-、tera-、peta-、exa-、......（推特 ）</p>

<h2>欢迎订阅</h2>

<p>这个专栏每周五发布，同步更新在我的。</p>

<p>微信搜索"<strong>阮一峰的网络日志</strong>"或者扫描二维码，即可订阅。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2018/bg2018042311.jpg" alt="image | left" title="" /></p>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2018-08-03T11:03:33+08:00">2018年8月 3日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>文集：</li>
<li>社交媒体：</li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------
<h1 id="#title_7" >8、从无人问津到占主导，脸书如何从Python 2迁移到Python 3</h1>
陈利鑫
[http://www.infoq.com/cn/news/2018/08/facebook-python2-to-3?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/08/facebook-python2-to-3?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>过去几年，Python 3的采用量明显增加，但它仍有很长的路要走。采用Python的大型公司倾向于在其基础架构上运行大量的Python 2.7代码，Facebook也不例外。</p> <i>By 陈利鑫</i>
---------------
<h1 id="#title_8" >9、百度超级链首个应用图腾落地，跨界公链＋AI+大数据</h1>
拜占庭教主
[http://www.infoq.com/cn/news/2018/08/baidu-pic-chain-bigdata-implemen?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/08/baidu-pic-chain-bigdata-implemen?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>7 月 18 日，百度正式宣布推出基于区块链技术的原创图片服务平台“图腾”，这也是基于百度超级链开发的首个区块链的应用。 百度称，图腾产品是在 4 月公测后正式上线，测试中超级链单链性能可达数万 TPS，多链性能理论可达百万至千万 TPS。 超级链核心技术包括超级节点技术、链内并行技术和立体网络技术。百度图腾基于超级链系统初始生成 40 亿图腾积分。 更多干货内容请关注微信公众号“区块链前哨”，（ID：blockchain-666）</p> <i>By 拜占庭教主</i>
---------------
<h1 id="#title_9" >10、用于Google Cloud开发人员的区块链工具包发布</h1>
Josiah Wilmoth
[http://www.infoq.com/cn/news/2018/08/blockchain-and-thecloud-service?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/08/blockchain-and-thecloud-service?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Google Cloud用户开发企业区块链解决方案不再是难事。Google与一家DLT初创企业Digital Asset合作，于本周一（即7月23日）发布了支持Google Cloud开发人员测试和构建区块链应用的SDK，使开发人员免于亲自编码搭建整个平台。</p> <i>By Josiah Wilmoth</i> <i> Translated by 盖磊</i>
---------------
<h1 id="#title_10" >11、Istio v1.0服务网格发布，各特性已生产就绪</h1>
Daniel Bryant
[http://www.infoq.com/cn/news/2018/08/istio-1.0-service-mesh?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/08/istio-1.0-service-mesh?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>在谷歌Cloud Next 2018大会上，Istio 1.0服务发布，其中，主要的新特性包括跨集群mesh支持、细粒度流量控制以及在一个mesh中增量推出mutual TLS的能力。</p> <i>By Daniel Bryant</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_11" >12、Pymetrics开源公平性感知机器学习算法Audit AI</h1>
Kent Weare
[http://www.infoq.com/cn/news/2018/08/Pymetrics-Fair-Machine-Learning?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/08/Pymetrics-Fair-Machine-Learning?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Pymetrics是一件专注于向企业提供招聘服务的初创企业。最近，Pymetrics在Github上开源了企业使用的偏差检测算法，称为“Audit AI”。Audit AI用于降低存在于训练数据集中的判别模式。这些判别模式会改进或影响机器学习算法在选取总体上的概率。</p> <i>By Kent Weare</i> <i> Translated by 盖磊</i>
---------------
<h1 id="#title_12" >13、物联网技术周报第 145 期: ESP8266 和 IFTTT 自制 WiFi 智能秤</h1>
黄峰达
[http://www.infoq.com/cn/news/2018/08/iot-weekly-145?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/08/iot-weekly-145?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>从我的第一个 DIY IoT 项目中吸取的经验；ESP8266 和 IFTTT 自制 WiFi 智能秤；如何在 Raspberry Pi 上使用深度学习轻松检测对象；阿里云 IoT 发布视频服务 Link Vision，全面助力安防行业数字化转型；Google 推出 AI 芯片 Edge TPU，可在边缘运行 TensorFlow Lite 机器学习模型；云知声开源全栈语音交互方案 全面布局 IoT 市场。</p> <i>By 黄峰达</i>
---------------