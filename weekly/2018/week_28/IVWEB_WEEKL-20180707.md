## 文章索引
1、 <a href="#1redux-sparse-arrays-and-learning-react-from-basic-code-examples" >Redux, sparse arrays, and learning React from basic code examples</a><br/>
2、 <a href="#2从项目导向转向产品导向中的挑战" >从项目导向转向产品导向中的挑战</a><br/>
3、 <a href="#3开源paas-rainbond-v360提供service-mesh微服务架构开箱即用" >开源PaaS Rainbond v3.6.0：提供service mesh微服务架构开箱即用</a><br/>
4、 <a href="#4将系统分解为微服务的策略" >将系统分解为微服务的策略</a><br/>
5、 <a href="#5微软宣布azure-sql-data-sync服务正式可用" >微软宣布Azure SQL Data Sync服务正式可用</a><br/>
6、 <a href="#6google诠释其它企业在实施sre中的错误" >Google诠释其它企业在实施SRE中的错误</a><br/>
7、 <a href="#7百度新发布的智能小程序是什么" >百度新发布的智能小程序是什么？</a><br/>
8、 <a href="#8android-p将使用更多基于编译器的安全缓解措施" >Android P将使用更多基于编译器的安全缓解措施</a><br/>
9、 <a href="#9文章-ballerina教程一门用于集成的编程语言" >文章： Ballerina教程：一门用于集成的编程语言</a><br/>
10、 <a href="#10文章-日志易aiops实践日志数据大有用途" >文章： 日志易AIOps实践：日志数据大有用途</a><br/>
11、 <a href="#11baidu-create-2018百度大脑论坛聚焦ai生态系统-平等赋能开发者" >Baidu Create 2018百度大脑论坛：聚焦AI生态系统 平等赋能开发者</a><br/>
12、 <a href="#12better-research-better-design-better-results" >Better Research, Better Design, Better Results</a><br/>
13、 <a href="#13每周分享第-12-期" >每周分享第 12 期</a><br/><h1 id="#title_0" >1、Redux, sparse arrays, and learning React from basic code examples</h1>

[https://javascriptweekly.com/issues/393](https://javascriptweekly.com/issues/393)
<table border=0 align="center" border="0">
  <tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   ">

  <div>    
    <table border=0 border=0><tr>
<td align="left" style="padding-left: 4px; font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   "><p>#393 — July  6, 2018</p></td>
<td align="right" style="padding-right: 4px; font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   "><p></p></td>
</tr></table>
    
    <table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0 12px;  "><p>JavaScript Weekly</p></td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   ">
  
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  "><div style="font-size: 10px; color: #999999; ">Illustration by 
</div></td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — A really neat high-level approach to explaining Redux and what it offers <em>beyond</em> state management.</p>
  <p>Linton Ye </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — A quick prod around the idea of ‘sparse’ arrays, how they work in JavaScript, and a few concepts to keep in mind.</p>
  <p>Remy Sharp </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Ahmed Bouchefra offers an in-depth exploration of the features of the Chrome DevTools for measuring performance and debugging your web apps.</p>
  <p>SitePoint </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"> provides a programming model for the cloud. Spend less time on YAML, and more time on JavaScript, because after all… Code is the best Config. Pulumi supports any service on any cloud - from serverless to Kubernetes to storage.</p>
  <p>Pulumi <span style="text-transform: uppercase; padding: 1px 4px;  margin-left: 4px; font-size: 0.9em;   color: #997 !important;">sponsor</span></p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Knowing where to begin optimizing your app’s JavaScript can be daunting — tree shaking might be a good place to start.</p>
  <p>Jeremy Wagner </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Learn how to use Capacitor and cutting-edge web technologies such as Vue.js and Ionic 4 web components to build cross-platform mobile apps for Android and iOS.</p>
  <p>Ahmed Bouchefra </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;">.</p>
  <p>Kay Plößer </p>
</td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0;  "><p>💻 Jobs</p></td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Join our small team building apps and services for customers in over 50 countries worldwide. We learn. We build. We deliver.</p>
  <p>Geist Interactive </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;">.</p>
  <p>x-team </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Vettery matches top tech talent with fast-growing companies. Create your profile to get started.</p>
  <p>Vettery </p>
</td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0;  "><p>📘 Tutorials and Opinions</p></td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Covering <code>Object.entries</code>, <code>Object.values</code>, <code>Object.getOwnPropertyDescriptors</code>, <code>String.padStart</code> and <code>String.padEnd</code>.</p>
  <p>Zsolt Nagy </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Evan Sangaline </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Play adaptive video at the same quality and speed as Netflix and Youtube. Encoding, Player and Analytics - JavaScript API client.</p>
  <p>Bitmovin <span style="text-transform: uppercase; padding: 1px 4px;  margin-left: 4px; font-size: 0.9em;   color: #997 !important;">sponsor</span></p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Gilad Shoham </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Long, but starts from a <em>very</em> simple level.</p>
  <p>Ohans Emmanuel </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — What happens under the hood when you use Angular’s <code>resolveComponentFactory</code>?</p>
  <p>Chidume Nnamdi </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Alexander Zlatkov </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Well written, but quite a theoretical exercise.</p>
  <p>Nathan Leung </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Learn all about data storage, middlewares, routing, &amp; generating views as you build a secure blog with Express.js.</p>
  <p>Okta <span style="text-transform: uppercase; padding: 1px 4px;  margin-left: 4px; font-size: 0.9em;   color: #997 !important;">sponsor</span></p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Gilad Shoham </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — A lot of very different answers here.</p>
  <p>Hacker News </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Robin Wieruch </p>
</td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0;  "><p>🔧 Code and Tools</p></td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   ">
  
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"> on CodePen.</p>
  <p>Vitaliy Stoliarov </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Declaratively compose application state from atomic state machines.</p>
  <p>Taras Mankovski and Charles Lowell </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>ROLLBAR <span style="text-transform: uppercase; padding: 1px 4px;  margin-left: 4px; font-size: 0.9em;   color: #997 !important;">sponsor</span></p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Klaus Sinani </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Handles validation, errors, submission, and getting values in and out. It’s now a year old, too.</p>
  <p>Jared Palmer </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Jamie McCrindle </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Alid Castano </p>
</td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px;  ">
<table border=0 border=0><tr><td style=" font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   "></td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  "><div style="line-height: 1.3em; font-size: 1.4em; color: #555555;">😄 Peter's “They're Not JavaScript But You Might Like 'Em” Bonus Links</div></td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — The most commonly used editor by JavaScript developers gains the ability to lay out multiple editors in the same window in a grid-like manner.</p>
  <p>Microsoft </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — A  quick online way to put together a CSS grid layout and get the code needed.</p>
  <p>Leniolabs </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — An amazingly playable Apple II game from 1984 ported to the Web. You have to program a group of robots to help you escape a sewer. One of the earliest programming-related games, it remains a serious challenge and will suck your time away.</p>
  <p>Micah Elizabeth Scott </p>
</td></tr></table>
</td></tr></table>
<table border=0 border=0><tr><td style=" font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   "></td></tr></table>
</div>

  </td></tr>
</table>





<img src="https://javascriptweekly.com/open/393/rss" width="1" height="1" />
---------------
<h1 id="#title_1" >2、从项目导向转向产品导向中的挑战</h1>
Manuel Pais
[http://www.infoq.com/cn/news/2018/07/challenges-from-projects-to-prod?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/challenges-from-projects-to-prod?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>在DevOps Enterprise伦敦峰会上，Carmen DeArdo和Nicole Bryan做演讲介绍了组织从项目导向转变产品导向的重要性。DeArdo曾任Nationwide Insurance的DevOps技术主管，Bryan是Tasktop的产品管理副总。</p> <i>By Manuel Pais</i> <i> Translated by 盖磊</i>
---------------
<h1 id="#title_2" >3、开源PaaS Rainbond v3.6.0：提供service mesh微服务架构开箱即用</h1>
刘凡
[http://www.infoq.com/cn/news/2018/07/PaaS-Srvice-Rainbond?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/PaaS-Srvice-Rainbond?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Service Mesh自2018年以来，受到了前所未有的关注，这种微服务架构允许我们在开发应用时，只关注业务代码，而不需要关心技术底层逻辑，被认为是企业扩展、保护和监控微服务的最佳方式。</p> <i>By 刘凡</i>
---------------
<h1 id="#title_3" >4、将系统分解为微服务的策略</h1>
Jan Stenberg
[http://www.infoq.com/cn/news/2018/07/decomposing-system-microservices?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/decomposing-system-microservices?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>几年前，Vladik Khononov和他的团队决定开始使用微服务，但是几个月后他们发现自己陷入了巨大的混乱之中。他们专注于采用酷炫的新技术，而不是思考如何将系统分解为微服务，也就是寻找边界并将不同的功能按照边界进行划分。</p> <i>By Jan Stenberg</i> <i> Translated by 张卫滨 </i>
---------------
<h1 id="#title_4" >5、微软宣布Azure SQL Data Sync服务正式可用</h1>
Steef-Jan Wiggers
[http://www.infoq.com/cn/news/2018/07/azure-sql-datasync-ga?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/azure-sql-datasync-ga?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>微软近日宣布，Azure SQL Data Sync 服务正式可用（GA），该服务允许用户在 Azure SQL Database 与其他 SQL 数据源之间进行单向或双向通信。此外，本次发布内容的变更包括新的配置功能、更快的数据库 schema 刷新能力，以及更安全的数据同步过程。</p> <i>By Steef-Jan Wiggers</i> <i> Translated by 邵思华</i>
---------------
<h1 id="#title_5" >6、Google诠释其它企业在实施SRE中的错误</h1>
Manuel Pais
[http://www.infoq.com/cn/news/2018/07/google-explains-sre?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/google-explains-sre?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>在近期的DevOps Enterprise Summit伦敦大会上，Google客户可靠性工程师Stephen Thorne做演讲澄清了SRE的概念，并指出为什么很多企业并不了解SRE的基本前提和优点的原因所在。</p> <i>By Manuel Pais</i> <i> Translated by 盖磊</i>
---------------
<h1 id="#title_6" >7、百度新发布的智能小程序是什么？</h1>
覃云
[http://www.infoq.com/cn/news/2018/07/baidu-small-app?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/baidu-small-app?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>7月5日，在百度AI开发者大会上，百度副总裁沈抖正式对外发布了百度智能小程序。百度称，智能小程序不仅全面接入百度大脑的AI能力，更将在今年12月份全面开源，但是主题演讲上并没有过多地透露智能小程序技术的细节。为此，小编赶赴百度小程序分论坛为大家挖掘了智能小程序在技术和应用上的特点。</p> <i>By 覃云</i>
---------------
<h1 id="#title_7" >8、Android P将使用更多基于编译器的安全缓解措施</h1>
Sergio De Simone
[http://www.infoq.com/cn/news/2018/07/android-p-security-mitigations?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/android-p-security-mitigations?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>谷歌工程师Ivan Lozano写道，即将推出的Android P（最近发布了beta版）将使用更多基于编译器的安全缓解措施，包括控制流完整性和整数溢出检查。</p> <i>By Sergio De Simone</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_8" >9、文章： Ballerina教程：一门用于集成的编程语言</h1>
Tyler Jewell
[http://www.infoq.com/cn/articles/ballerina-integration-tutorial-part-2?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/ballerina-integration-tutorial-part-2?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/ballerina-integration-tutorial-part-2/zh/smallimage/ballerina-part2-logo-small-1527788057440-1530634191419.jpg"/><p>Ballerina是一种新的编程语言和平台，目标是让创建跨分布式端点的弹性服务变得更轻松。Ballerina的设计原则侧重于将集成概念变成一种编程语言，包括网络感知类型系统、时序图语法、并发worker、“DevOps就绪”和环境意识。</p> <i>By Tyler Jewell</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_9" >10、文章： 日志易AIOps实践：日志数据大有用途</h1>
饶琛琳
[http://www.infoq.com/cn/articles/aiops-practice-at-rizhiyi?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/aiops-practice-at-rizhiyi?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/aiops-practice-at-rizhiyi/zh/smallimage/logo (4)-1530634736425.jpg"/><p>AIOps 最大的目的就是缩短运维工作的时间，虽然 AIOps 提出的时间还不长，但目前来看 AIOps 已是明显的趋势。</p> <i>By 饶琛琳</i>
---------------
<h1 id="#title_10" >11、Baidu Create 2018百度大脑论坛：聚焦AI生态系统 平等赋能开发者</h1>
陈思
[http://www.infoq.com/cn/news/2018/07/baidu-create-2018?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/baidu-create-2018?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Baidu Create 2018百度大脑论坛：聚焦AI生态系统 平等赋能开发者。</p> <i>By 陈思</i>
---------------
<h1 id="#title_11" >12、Better Research, Better Design, Better Results</h1>
Sam Wright & James Macnamara
[https://www.smashingmagazine.com/2018/07/better-research-design-results/](https://www.smashingmagazine.com/2018/07/better-research-design-results/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/07/better-research-design-results/" />
              <title>Better Research, Better Design, Better Results</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>Better Research, Better Design, Better Results</h1>
                  
                    
                    <address>Sam Wright &amp; James Macnamara</address>
                  
                  <time datetime="2018-07-06T13:45:41&#43;02:00" class="op-published">2018-07-06T13:45:41+02:00</time>
                  <time datetime="2018-07-06T22:00:31&#43;00:00" class="op-modified">2018-07-06T22:00:31+00:00</time>
                </header>
                

<p>Over the years, one thing we have consistently seen is how little insight from digital marketers is used at the planning stages of a web development project.</p>

<p>Data from Google Analytics and SEMrush to tools like VWO (<strong>V</strong>isual <strong>W</strong>ebsite <strong>O</strong>ptimizer) or Hotjar are all resources that can be used to provide valuable insight ahead of the first line of code being written. Basic SEO elements, such as URL structure and metadata, should also be involved in the decision making of any web design project.</p>

<p>This has been , and it’s a sore point for many SEO and content specialists. However, in this article we’re going to focus on the issue in relation to our own preferred methodology, which is effective content research and creation, and how user intent affects the process at every stage.</p>

<p>We’ll then move on through each aspect of the design process, talking about SEO questions along the way, and ending up with a detailed breakdown of a workflow we feel achieves two things: websites which look great, and are fully-realized assets designed to achieve measurable goals.</p>

<h3 id="intelligent-content-research">Intelligent Content Research</h3>

<p>A website doesn’t just have to be built. It has to populated with material. The way this material is designed will have a large part in determining a website’s success, i.e. what it brings to a client’s business or organization.</p>

<p>This is why we find it strange that a normal web design process misses out at its earliest stages things like . So often a frame is built without enough thought about what it’s going to contain.</p>



  <aside class="product-panel product-panel__tilted product-panel--book" data-audience="non-subscriber" data-remove="true">
    <div class="container product-panel--book__container">
      <div class="panel__description panel__description--book">
        <p>
          Is your pattern library up to date today? <em>Alla Kholmatova</em> has just finished a fully fledged book on <strong>Design Systems</strong> and how to get them right. With common traps, gotchas and the lessons she learned. Hardcover, eBook. <em>Just sayin'.</em>
        </p>
        <a href="http://smashed.by/uxpaneldsbook">
          <button class="btn btn--green btn--large">
            Table of Contents&nbsp;&rarr;
          </button>
        </a>
      </div>
      <div class="panel__image panel__image--book">
        <a href="http://smashed.by/uxpaneldsbook" class="books__book__image">
        <div class="books__book__img">
          <img src="https://www.smashingmagazine.com/images/books/design-systems--large-opt.png">
        </div>
      </a>
      </div>
    </div>
  </aside>








    









<p>All of our projects at some level require keyword research, and this always involves careful attention to . As SmashingMag readers, you’ll most likely understand this concept. For the sake of clarity though, it is worth revisiting this in terms of content strategy and SEO.</p>

<p>Before user intent was a thing, keyword research involved gathering lists of search volumes and “difficulty” numbers and trying to spot what keywords you might rank for, without too much attention paid to whether they were queries actually likely to be used by your ideal users.</p>

<p>While we still have to go through this process, effective research requires more intelligent use of the data we find. We have to focus on discovering target keywords and developing material that satisfies  &mdash; while still looking out for some relevant “good opportunity” keywords (i.e. high volume, low competition) along the way.</p>

<p>This means that keyword research is becoming a way of understanding what users mean by their searches <em>in context</em>, what questions they want answering, and what kind of language they use, all serving the purpose of creating content that has the best chance of helping a website meet its owner’s goals.</p>

<h3 id="user-intent-and-content-creation">User Intent And Content Creation</h3>

<p>User intent informs keyword research, which in time becomes content strategy, and then creation. The content we create always has a purpose, and in the majority of cases it is to satisfy the intent behind a user query.</p>

<p>As a broad example, let’s take the query “coffee”. Here’s how the results look &mdash; notice the different types of content aimed at meeting varying intents:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/362a5872-cdd0-4ddc-b090-fc8d715af8da/2-google-search-results-page.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/362a5872-cdd0-4ddc-b090-fc8d715af8da/2-google-search-results-page.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/362a5872-cdd0-4ddc-b090-fc8d715af8da/2-google-search-results-page.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/362a5872-cdd0-4ddc-b090-fc8d715af8da/2-google-search-results-page.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/362a5872-cdd0-4ddc-b090-fc8d715af8da/2-google-search-results-page.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/362a5872-cdd0-4ddc-b090-fc8d715af8da/2-google-search-results-page.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/362a5872-cdd0-4ddc-b090-fc8d715af8da/2-google-search-results-page.png"
			sizes="100vw"
			alt="Search engine results page for coffee"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<p>The results vary hugely according to the audience they are targeting. Some are aimed at people wanting to find somewhere to grab a coffee nearby, others are sites where you can order your joe online. There are also resources looking at coffee’s history and nutritional information.</p>

<p>While we don’t often have to deal with such broad terms, all of this has to be thought about, unpicked and planned according to a website’s purpose. This means content research, when focused on users, has obvious and enormous implications when it comes to site architecture and even aesthetics &mdash; i.e. the first things to be worked out in any design process.</p>

<h3 id="when-content-isn-t-considered">When Content Isn’t Considered</h3>

<p>One of the most common issues we see with both old and new sites is content that has not designed to fully address user queries, in terms of exact phrases as well as general intent. In some cases, this is easy to fix &mdash; for example, a few tweaks to a page’s metadata and copy can often clarify its query and user targeting almost instantly.</p>

<p>In many others though, the problems are much more serious, and a revised architecture or navigation is required as part of an entirely new content strategy &mdash; a costly process that could have been avoided if the right professionals had been consulted all along.</p>

<p>Here are some scenarios specific to site content we’ve encountered too many times:</p>

<h4 id="scenario-1-shiny-new-website-dull-new-content">Scenario 1: Shiny New Website, Dull New Content</h4>

<p>A client &mdash;  &mdash; is launching a completely new site, with no previous content to refer to.</p>

<p>However, if John isn’t prompted to think about copy, content or SEO until much later down the line &mdash; typically after the back-end development phase &mdash; then poor decisions can be made, while there is also the risk that he will lose some of his motivation, energy, and patience with the project.</p>

<p>A rush to see it completed means the content isn’t researched or executed well enough to be effective in the long term. <em>Eventually it has to be looked at again during a lengthy and costly second-stage SEO and content creation campaign</em>.</p>

<h4 id="scenario-2-same-content-same-problems">Scenario 2: Same Content, Same Problems</h4>

<p>A rebuild of an existing site means there’s existing content to look at and refer to. Sometimes, John is so rushed, or is so intent on keeping costs down at this stage, content is not considered at all.</p>

<p>The same content is used on the old site as on the new site, and John wonders why his site doesn’t shoot immediately to number one for all of his top keywords. <em>Eventually it has to be looked at again during a lengthy and costly second-stage SEO and content creation campaign</em>.</p>

<h4 id="new-content-or-else">New Content, Or Else!</h4>

<p>Sometimes a valuable, authoritative site is rebuilt, as part of a rebrand for example. John insists that everything is new. Without the proper research spelling this out, for example analytics data (explored in more detail below), John isn’t aware of the assets he already has. He gets rid of the old content (or does something even worse like switch to a new domain) that search engines thought was valuable, and rankings mysteriously tank. <em>Eventually it has to be looked at again during a lengthy and costly second-stage SEO and content creation campaign</em>.</p>

<h3 id="workflow-issues-when-seos-are-called-in-after-the-fact">Workflow Issues When SEOs Are Called In After The Fact</h3>

<p>We have to make do with what we get of course, but it is frustrating for SEOs to work on projects well after problems have set it, and we end up having to suggest that a relatively new site needs to be pulled apart if it has any hope of realizing its value.</p>

<p>When SEO isn’t considered from the beginning, the page layout and semantic markup haven’t considered excerpts, H-tags, metadata or how the CMS can aid SEO in the long term. Many clients will then turn to quick fixes such Wordpress plugins like Yoast. There’s a good chance that these will be ineffective or used incorrectly, perpetuating the problems at hand.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2061d5f8-09b5-4666-aa6f-e995ae561b5a/5-downward-results-graph.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2061d5f8-09b5-4666-aa6f-e995ae561b5a/5-downward-results-graph.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2061d5f8-09b5-4666-aa6f-e995ae561b5a/5-downward-results-graph.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2061d5f8-09b5-4666-aa6f-e995ae561b5a/5-downward-results-graph.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2061d5f8-09b5-4666-aa6f-e995ae561b5a/5-downward-results-graph.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2061d5f8-09b5-4666-aa6f-e995ae561b5a/5-downward-results-graph.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2061d5f8-09b5-4666-aa6f-e995ae561b5a/5-downward-results-graph.png"
			sizes="100vw"
			alt="Graph showing negative results"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<p>So, guess what? An SEO specialist is brought in after the site has been launched.</p>

<p>Now the client is unhappy with their existing agency and places a high importance on improving SEO. In turn, the SEO specialist has a difficult job trying not to undermine the web agency but still needs to recommend structural and on-page adjustments.</p>

<p>They will also face problems with client expectations, who will unsurprisingly feel ripped-off and begrudge spending more money on their new shiny website.</p>

<p>Does this all sound familiar? The crux of our argument is that by bringing inline processes such as intent-focused keyword research from the beginning, these situations can be avoided and everyone can get along.</p>

<p>At the same time, an integrated approach will mean better UX and conversions alongside a strong SEO performance. Better focused content can also mean  too, as relevancy is a part of Google’s Adword calculation.</p>

<p>Rather than an expensive design phase followed by a second round of expensive SEO work, the whole process can be streamlined, keeping time and costs down, clients happier, and producing a better final product as a result.</p>

<div class="sponsors__wide-place"></div>




<h3 id="a-new-design-process">A New Design Process</h3>

<p>This is all well and good, but how can we put it into practice? With varying degrees of complexity, for many in the industry the design process will look like this:</p>

<h4 id="a-typical-workflow">A Typical Workflow</h4>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/902d6deb-d240-4b51-96fa-ea2955cdd307/6-different-stages-graph-one.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/902d6deb-d240-4b51-96fa-ea2955cdd307/6-different-stages-graph-one.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/902d6deb-d240-4b51-96fa-ea2955cdd307/6-different-stages-graph-one.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/902d6deb-d240-4b51-96fa-ea2955cdd307/6-different-stages-graph-one.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/902d6deb-d240-4b51-96fa-ea2955cdd307/6-different-stages-graph-one.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/902d6deb-d240-4b51-96fa-ea2955cdd307/6-different-stages-graph-one.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/902d6deb-d240-4b51-96fa-ea2955cdd307/6-different-stages-graph-one.png"
			sizes="100vw"
			alt="Flow graph showing the different processes, project planning, design, and development &amp; launch"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<p>It’s worth stating that good developers will focus on user experience and the visitor journey in their own workflow. Instead, a typical project may move through these stages:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/94781d36-8c47-45dd-b9ba-c783996b4a1f/7-different-stages-graph-two.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/94781d36-8c47-45dd-b9ba-c783996b4a1f/7-different-stages-graph-two.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/94781d36-8c47-45dd-b9ba-c783996b4a1f/7-different-stages-graph-two.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/94781d36-8c47-45dd-b9ba-c783996b4a1f/7-different-stages-graph-two.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/94781d36-8c47-45dd-b9ba-c783996b4a1f/7-different-stages-graph-two.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/94781d36-8c47-45dd-b9ba-c783996b4a1f/7-different-stages-graph-two.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/94781d36-8c47-45dd-b9ba-c783996b4a1f/7-different-stages-graph-two.png"
			sizes="100vw"
			alt="Flow graph showing the different processes, project planning, design, and development &amp; launch"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<h4 id="a-different-approach">A Different Approach</h4>

<p>Over the past year or so, we have put a lot of effort into refining this process in a way that we believe gives the best possible value for our clients. Here it is:</p>

<h5 id="project-planning">Project planning</h5>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3b3133d7-a9fd-4837-abd3-86809319b0ba/8-project-planning.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3b3133d7-a9fd-4837-abd3-86809319b0ba/8-project-planning.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3b3133d7-a9fd-4837-abd3-86809319b0ba/8-project-planning.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3b3133d7-a9fd-4837-abd3-86809319b0ba/8-project-planning.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3b3133d7-a9fd-4837-abd3-86809319b0ba/8-project-planning.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3b3133d7-a9fd-4837-abd3-86809319b0ba/8-project-planning.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3b3133d7-a9fd-4837-abd3-86809319b0ba/8-project-planning.png"
			sizes="100vw"
			alt="Flow graph showing the different processes, specifically project planning and defining budget"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<p>As always, this should be the first step, as it will define the scope of the work ahead. Be realistic and build in room for error, and be very aware that you get what you pay for. Under-budgeting runs the risk of falling short on key areas such as design, functionality, and content. At the same time, if all the project’s budget is swallowed up on design and development, there will be no room for a supporting marketing strategy or ongoing updates and improvements.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/394fdbc7-8ff7-4db0-8732-0a49f3dd936e/9-project-planning-2.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/394fdbc7-8ff7-4db0-8732-0a49f3dd936e/9-project-planning-2.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/394fdbc7-8ff7-4db0-8732-0a49f3dd936e/9-project-planning-2.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/394fdbc7-8ff7-4db0-8732-0a49f3dd936e/9-project-planning-2.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/394fdbc7-8ff7-4db0-8732-0a49f3dd936e/9-project-planning-2.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/394fdbc7-8ff7-4db0-8732-0a49f3dd936e/9-project-planning-2.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/394fdbc7-8ff7-4db0-8732-0a49f3dd936e/9-project-planning-2.png"
			sizes="100vw"
			alt="Flow graph showing the different processes, specifically project planning and defining goals"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<p>Similarly, your goals should be clear from the very start. Are you focused on acquiring email addresses or selling products? What is the one thing that you want your visitors to do above all else? Without clearly understanding this, the chances are that your site will fall short in its aims.</p>

<p>Once this is decided, you can move on to setting broader targets. There are a number of methods here, such as  (or Specific, Measurable, Attainable, Relevant and Time Bound). These will define how a successful project will look on completion. Be realistic here &mdash; if your current site has a few hundred visits per month, don’t expect this to reach 10,000 within a few months without some serious effort and investment.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f6f294e1-9d73-4d66-a19b-2232409448b6/10-sales-website-goals-examples.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f6f294e1-9d73-4d66-a19b-2232409448b6/10-sales-website-goals-examples.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f6f294e1-9d73-4d66-a19b-2232409448b6/10-sales-website-goals-examples.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f6f294e1-9d73-4d66-a19b-2232409448b6/10-sales-website-goals-examples.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f6f294e1-9d73-4d66-a19b-2232409448b6/10-sales-website-goals-examples.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f6f294e1-9d73-4d66-a19b-2232409448b6/10-sales-website-goals-examples.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f6f294e1-9d73-4d66-a19b-2232409448b6/10-sales-website-goals-examples.jpg"
			sizes="100vw"
			alt="Sales website goals examples, including generating more sales, improving sales conversion rate, and improving sales support"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<p>At the same time, we are big fans of the , LinkedIn et al. This technique can work really well for a web project as well a general business strategy.</p>

<p>Here’s a great video that will give you some background on the OKR system.</p>

<figure class="video-container"><iframe data-src="https://www.youtube.com/embed/mJB83EZtAjc" width="600" height="480" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe></figure>

<p>Writing effective OKRs is a bit of an art in itself, but there are some . The main thing to remember though is that your goals are going to define the site’s architecture to some extent.</p>

<p>At its simplest level, people won’t be able to contact you if there is no contact form. Similarly, they will be less likely to get in touch if you remove a bunch of FAQ or blog posts that help explain what it is that your product or service does. This brings us onto our next step.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/193872df-eae5-4775-9542-7699fe40f99c/12-project-planning-3.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/193872df-eae5-4775-9542-7699fe40f99c/12-project-planning-3.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/193872df-eae5-4775-9542-7699fe40f99c/12-project-planning-3.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/193872df-eae5-4775-9542-7699fe40f99c/12-project-planning-3.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/193872df-eae5-4775-9542-7699fe40f99c/12-project-planning-3.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/193872df-eae5-4775-9542-7699fe40f99c/12-project-planning-3.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/193872df-eae5-4775-9542-7699fe40f99c/12-project-planning-3.png"
			sizes="100vw"
			alt="Flow graph showing the different processes, specifically project planning and reviewing existing Google Analytics data, if available"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<p>You may have pages that are already performing well. If that is the case, you’ll need to identify them so you can make sure they are built into your new structure. If you shed pages that bring in traffic at any point of your funnel, this could result in a loss of leads or sales. Along with URL alterations, this can be one of the main causes of drops in traffic after a migration or significant site update. It may seem obvious but it is an issue that we’ve seen time and time again.</p>

<p>The first stage of preventing this is to look in Google Analytics, or whichever analytics platform you use. Find out which pages are bringing in organic visits first of all. These should be built into your new plan as a priority, preferably without changing the URL and keeping a prominent place in your navigation structure.</p>

<p>Another great tool here is  tag that was applied to organic keywords a few years ago.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e38883d8-6da4-426d-b8f6-76ea1332808b/13-not-provided-tag.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e38883d8-6da4-426d-b8f6-76ea1332808b/13-not-provided-tag.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e38883d8-6da4-426d-b8f6-76ea1332808b/13-not-provided-tag.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e38883d8-6da4-426d-b8f6-76ea1332808b/13-not-provided-tag.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e38883d8-6da4-426d-b8f6-76ea1332808b/13-not-provided-tag.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e38883d8-6da4-426d-b8f6-76ea1332808b/13-not-provided-tag.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e38883d8-6da4-426d-b8f6-76ea1332808b/13-not-provided-tag.png"
			sizes="100vw"
			alt="Example of the not provided tag"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<p>This uses , and it means that you’ll be able to see which keywords drive traffic to specific pages on your site. This is extremely useful in terms of planning which pages to keep or remove.</p>

<p>Of course, not all pages are important in terms of organic traffic. As mentioned, some could be crucial pre-conversion or sale, such as an FAQ page, but bring in little of the may of inbound visits to the site. Take a look at page views, and user flow here to make sure you are not missing anything.</p>

<p>At the same time, it’s worth bearing in mind that your data may not be perfect. Checking the validity of Google Analytics data is a pretty big subject in itself, but one of the simplest steps you can take is to check that your tracking code is implemented correctly.</p>

<p>Again, we won’t go into the ins-and-outs here. However, there is one trick that we recommend when carrying out content migrations. The web crawler Screaming Frog has a nifty feature that allows you to check for . More than once, we’ve uncovered valuable pages that are not being tracked, and would have been lost in a redesign.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e899d93b-a929-4fa2-b473-970690889657/14-project-planning-4.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e899d93b-a929-4fa2-b473-970690889657/14-project-planning-4.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e899d93b-a929-4fa2-b473-970690889657/14-project-planning-4.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e899d93b-a929-4fa2-b473-970690889657/14-project-planning-4.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e899d93b-a929-4fa2-b473-970690889657/14-project-planning-4.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e899d93b-a929-4fa2-b473-970690889657/14-project-planning-4.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e899d93b-a929-4fa2-b473-970690889657/14-project-planning-4.png"
			sizes="100vw"
			alt="Flow graph showing the different processes, specifically project planning and reviewing current rankings (keywords and ranking pages), if available"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<p>Next, it’s time to start looking to see which keywords you are visible for. There are a few tools we use here, but the most useful is . This monitors billions of keywords and tracks which sites are ranking for them. By querying its database, you can see which keywords your site is appearing for in Google’s results without manually entering them into a tracker. It’s by no means perfect, so you’ll need to manually check positions for any terms you think it may have missed too.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8e40f258-d6b0-4c80-9fd8-e19d8046d1e0/15-top-organic-keywords.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8e40f258-d6b0-4c80-9fd8-e19d8046d1e0/15-top-organic-keywords.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8e40f258-d6b0-4c80-9fd8-e19d8046d1e0/15-top-organic-keywords.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8e40f258-d6b0-4c80-9fd8-e19d8046d1e0/15-top-organic-keywords.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8e40f258-d6b0-4c80-9fd8-e19d8046d1e0/15-top-organic-keywords.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8e40f258-d6b0-4c80-9fd8-e19d8046d1e0/15-top-organic-keywords.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8e40f258-d6b0-4c80-9fd8-e19d8046d1e0/15-top-organic-keywords.png"
			sizes="100vw"
			alt="Example of top organic keywords from SEMRUSH"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<p>Once you have this information, you can start drawing it together in a spreadsheet. , and you can see the initial findings in the first tab.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1331296b-6295-4387-acc3-7addc8ee8466/16-keyword-document.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1331296b-6295-4387-acc3-7addc8ee8466/16-keyword-document.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1331296b-6295-4387-acc3-7addc8ee8466/16-keyword-document.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1331296b-6295-4387-acc3-7addc8ee8466/16-keyword-document.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1331296b-6295-4387-acc3-7addc8ee8466/16-keyword-document.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1331296b-6295-4387-acc3-7addc8ee8466/16-keyword-document.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1331296b-6295-4387-acc3-7addc8ee8466/16-keyword-document.png"
			sizes="100vw"
			alt="Example of a keyword research document"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>












<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6ca6306f-a843-4843-90ea-1d8f1b9c10be/17-project-planning-5.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6ca6306f-a843-4843-90ea-1d8f1b9c10be/17-project-planning-5.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6ca6306f-a843-4843-90ea-1d8f1b9c10be/17-project-planning-5.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6ca6306f-a843-4843-90ea-1d8f1b9c10be/17-project-planning-5.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6ca6306f-a843-4843-90ea-1d8f1b9c10be/17-project-planning-5.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6ca6306f-a843-4843-90ea-1d8f1b9c10be/17-project-planning-5.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6ca6306f-a843-4843-90ea-1d8f1b9c10be/17-project-planning-5.png"
			sizes="100vw"
			alt="Flow graph showing the different processes, specifically project planning and creating audience profiles"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<p>For both UX and SEO, it is important to understand who you are speaking to. Think about the types of language or phrases your users will know, as well as the tone of voice. Do they respond to images or copy, detail or bullets, flashy designs or more technical pages?</p>

<p>Keyword research is also really useful here, as it defines terms and reveals correct vocabulary &mdash; another example of how keyword research eventually filters down and is important to almost every step.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c84f1a1d-4796-415c-b432-49a9a87e1c95/18-project-planning-6.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c84f1a1d-4796-415c-b432-49a9a87e1c95/18-project-planning-6.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c84f1a1d-4796-415c-b432-49a9a87e1c95/18-project-planning-6.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c84f1a1d-4796-415c-b432-49a9a87e1c95/18-project-planning-6.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c84f1a1d-4796-415c-b432-49a9a87e1c95/18-project-planning-6.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c84f1a1d-4796-415c-b432-49a9a87e1c95/18-project-planning-6.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c84f1a1d-4796-415c-b432-49a9a87e1c95/18-project-planning-6.png"
			sizes="100vw"
			alt="low graph showing the different processes, specifically project planning and carrying out user-intent focused keyword research"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<p>Now that we know who we are talking to, how best can you do it? We have explained the concept behind user-intent focused keyword research earlier in this document, but here’s some insight into how we go about doing it ourselves. Please note, this could be a feature in itself, so for the sake of brevity we’re just focusing on an outline here.</p>

<p>In terms of our toolkit, we tend to use a combination of . We feel that using both, as well as AdWords’ keyword planner, and any others you can get your hands on, is the best way of gathering data, as each tool will have its own strength, and often data for longer-tail keywords will be available in one tool, but not another.</p>

<p>Here are the first steps.</p>

<ul>
<li>Listing all the relevant keywords we can find along with the data we have for them, volume being the most important.</li>
<li>We’ll also include some measure of how competitive they are, as well an indication if the current is already ranking for them. We usually use Moz data here, which corresponds to this key.</li>
</ul>

<h5 id="key">Key</h5>

<table class="tablesaw break-out" data-tablesaw-mode="swipe" data-tablesaw-minimap>
        <tr>
            <td>0 - 15%</td>
            <td>Non-competitive term, top rankings achievable with well optimized on-page keyword use</td>
        </tr>
        <tr>
            <td>16 - 30%</td>
            <td>Low competition, top rankings achievable with well optimized on-page keyword use and light link strength</td>
        </tr>
        <tr>
            <td>31 - 45%</td>
            <td>Slightly competitive, top rankings require well optimized on-page use and moderate link strength</td>
        </tr>
        <tr>
            <td>46 - 60%</td>
            <td>Competitive, top rankings achievable only with highly optimized on-page content and substantial link strength</td>
        </tr>
        <tr>
            <td>61 - 75%</td>
            <td>Highly competitive term, top rankings require on-page optimization, well-established history and robust link strength</td>
        </tr>
        <tr>
            <td>76 - 90%</td>
            <td>Exceptionally competitive term, top rankings only achievable with highly-established site and overwhelming link strength</td>
        </tr>
        <tr>
            <td>91%+</td>
            <td>Among the most competitive terms on the web, only the most powerful & popular sites can achieve rankings</td>
        </tr>
    </tbody>
</table>

<ul>
<li>We gather as much as possible here, so the client can see the research for themselves and so we can see everything at once &mdash; of course, most of it won’t end up being used, but long lists look more thorough than a few simple, if well-researched proposals.</li>
</ul>

<p>It’s what you do with the data you gather that makes the research different and far more valuable than say, five years ago, when user intent wasn’t so important to or understood by search engine algorithms.</p>

<p>From keyword research data the site structure and list of pages needs to emerge, and be thought of as intelligently as possible. To this end:</p>

<ul>
<li><p>We look through everything we find and select keywords based on volume, competition, but most importantly of all, whether the site will be able to effectively meet the user intent behind the query. Sometimes the numbers just click together, but mostly you’ll have to compromise &mdash; with user intent always being the most important consideration.</p></li>

<li><p>We then use the most general or short-tail keywords we select and think of them as intent or topic “nodes” in order to deepen our research and increase our insight into potentially valuable content.</p></li>
</ul>

<p>As well as looking at keywords focused on landing pages, needs and wants keywords and exact phrases (for example questions that are also verbatim search queries) are also crucial.  is a great tool for branching out and seeing what users are wondering about your chosen topics/keywords.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2c1bc240-45e4-4f31-8323-ef9992b7b09d/19-answer-the-public.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2c1bc240-45e4-4f31-8323-ef9992b7b09d/19-answer-the-public.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2c1bc240-45e4-4f31-8323-ef9992b7b09d/19-answer-the-public.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2c1bc240-45e4-4f31-8323-ef9992b7b09d/19-answer-the-public.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2c1bc240-45e4-4f31-8323-ef9992b7b09d/19-answer-the-public.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2c1bc240-45e4-4f31-8323-ef9992b7b09d/19-answer-the-public.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2c1bc240-45e4-4f31-8323-ef9992b7b09d/19-answer-the-public.png"
			sizes="100vw"
			alt="Example of a result from Answer The Public"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<ul>
<li>By branching out, you discover new users with new intent, and think of new content to meet them. The site is built catering to more users as a result, it ranks for more queries, it gets more traffic, its authority grows and you end up with a virtuous circle &mdash; as opposed to the vicious cycle we had before.</li>
</ul>

<p>With well-researched content present when it launches, the site is able to realize its value from day one, so the client ends up with more conversions, more revenue. This way, the extra costs involved during the site build are more than offset.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a16fb733-d945-440a-9698-652602958a80/20-project-planning-7.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a16fb733-d945-440a-9698-652602958a80/20-project-planning-7.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a16fb733-d945-440a-9698-652602958a80/20-project-planning-7.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a16fb733-d945-440a-9698-652602958a80/20-project-planning-7.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a16fb733-d945-440a-9698-652602958a80/20-project-planning-7.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a16fb733-d945-440a-9698-652602958a80/20-project-planning-7.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a16fb733-d945-440a-9698-652602958a80/20-project-planning-7.png"
			sizes="100vw"
			alt="Flow graph showing the different processes, specifically project planning and creating a sitemap and architecture"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<p>With all this information, it’s time to start planning out the site. Define what goes on what page. Understand where the content is going on the website AND WHY. Make it scalable &mdash; adding or removing content should be easy as business goals can rapidly shift.</p>

<p>For this stage, everything needs to make sense. Pages need to be linked because it makes sense semantically. Those that are important for  should be high up in your navigation.</p>

<p>E-commerce sites often do this well. Take the example below &mdash; the category and sub-category structure means that it is clear keywords should be used for the page.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5ff1cce9-60f1-4c8c-88fe-f862736663fd/21-b-and-q.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5ff1cce9-60f1-4c8c-88fe-f862736663fd/21-b-and-q.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5ff1cce9-60f1-4c8c-88fe-f862736663fd/21-b-and-q.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5ff1cce9-60f1-4c8c-88fe-f862736663fd/21-b-and-q.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5ff1cce9-60f1-4c8c-88fe-f862736663fd/21-b-and-q.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5ff1cce9-60f1-4c8c-88fe-f862736663fd/21-b-and-q.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5ff1cce9-60f1-4c8c-88fe-f862736663fd/21-b-and-q.png"
			sizes="100vw"
			alt="Example of a menu from B&amp;Q"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<p>On the other hand, here is an example of a site where the navigation is a wasted opportunity.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/29554e0d-07a1-4229-aeb4-cd048a11fd2b/22-ziggurat.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/29554e0d-07a1-4229-aeb4-cd048a11fd2b/22-ziggurat.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/29554e0d-07a1-4229-aeb4-cd048a11fd2b/22-ziggurat.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/29554e0d-07a1-4229-aeb4-cd048a11fd2b/22-ziggurat.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/29554e0d-07a1-4229-aeb4-cd048a11fd2b/22-ziggurat.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/29554e0d-07a1-4229-aeb4-cd048a11fd2b/22-ziggurat.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/29554e0d-07a1-4229-aeb4-cd048a11fd2b/22-ziggurat.png"
			sizes="100vw"
			alt="Example of a menu from Ziggurat"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<p>There are no services pages that could target keyword groups, and no sub-pages off any of the main categories. While “minivation” may well be a great concept, it’s not one that users will search for. Of course, this may not be a priority in this instance, but we see this kind of layout time and time again.</p>

<p>Overall, the danger here can be that without an awareness of SEO at this stage, the client can want to switch from a navigation like our first example to the second. In this case, there is an enormous risk to traffic and therefore revenue, and as web professionals, it is our duty to state this clearly.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7625b83d-53bd-4c48-a35c-df72def6b725/23-project-planning-8.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7625b83d-53bd-4c48-a35c-df72def6b725/23-project-planning-8.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7625b83d-53bd-4c48-a35c-df72def6b725/23-project-planning-8.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7625b83d-53bd-4c48-a35c-df72def6b725/23-project-planning-8.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7625b83d-53bd-4c48-a35c-df72def6b725/23-project-planning-8.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7625b83d-53bd-4c48-a35c-df72def6b725/23-project-planning-8.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7625b83d-53bd-4c48-a35c-df72def6b725/23-project-planning-8.png"
			sizes="100vw"
			alt="Flow graph showing the different processes, specifically project planning and targeted copywriting/marketing messaging"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<p>While content production usually happens at the end of a project, we feel designing around real content (rather than lorem ipsum) is more cost and time efficient, as it greatly reduces the need for design amendments after a project is complete.</p>

<p>There is also a really strong case here that placeholder text reiterates the idea that content is secondary to design, and that it is something lesser in the hierarchy of the project. This is an idea that again has been , so there is no need for us to tread over the same ground.</p>

<p>At the same time, by this point, your research will give you all the information you need to put together an amazing brief for your writers. Believe us, they’ll appreciate it!</p>

<h5 id="design">Design</h5>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8043a201-d95d-4529-8604-0571d3fa8bc3/24-design.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8043a201-d95d-4529-8604-0571d3fa8bc3/24-design.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8043a201-d95d-4529-8604-0571d3fa8bc3/24-design.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8043a201-d95d-4529-8604-0571d3fa8bc3/24-design.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8043a201-d95d-4529-8604-0571d3fa8bc3/24-design.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8043a201-d95d-4529-8604-0571d3fa8bc3/24-design.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8043a201-d95d-4529-8604-0571d3fa8bc3/24-design.png"
			sizes="100vw"
			alt="Flow graph showing the different processes, specifically design and low fidelity wireframes"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<p>It’s time to start bringing it all together. Initial wireframes should be basic boxes and titles defined by the content development and copy generated up until this point, outlining key sections of the website. Again, wireframe with real content wherever possible. Tools like  are really useful for this.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f928e471-c688-4ad8-93c1-a3b12ebdd09f/25-design-2.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f928e471-c688-4ad8-93c1-a3b12ebdd09f/25-design-2.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f928e471-c688-4ad8-93c1-a3b12ebdd09f/25-design-2.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f928e471-c688-4ad8-93c1-a3b12ebdd09f/25-design-2.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f928e471-c688-4ad8-93c1-a3b12ebdd09f/25-design-2.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f928e471-c688-4ad8-93c1-a3b12ebdd09f/25-design-2.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f928e471-c688-4ad8-93c1-a3b12ebdd09f/25-design-2.png"
			sizes="100vw"
			alt="Flow graph showing the different processes, specifically design and high fidelity wireframes"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<p>Once the wireframes are created the designs can start becoming more realized. Add in some brand identity, such as a color pallet, the actual client logo, corporate typography, and fonts. At this point, you should start to see exactly how the website will look. Any changes should be made at this stage &mdash; it’s much easier to edit a Photoshop file than change code.</p>

<h5 id="development">Development</h5>

<p>By this stage, the actual development phase should be straightforward. Write the HTML and CSS code for the basic design, then focus on any interactive elements. From an SEO point of view, it is worth stating that Javascript is a .</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/aa6ebc7b-cdbd-4339-a46e-6545f18c1225/26-development.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/aa6ebc7b-cdbd-4339-a46e-6545f18c1225/26-development.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/aa6ebc7b-cdbd-4339-a46e-6545f18c1225/26-development.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/aa6ebc7b-cdbd-4339-a46e-6545f18c1225/26-development.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/aa6ebc7b-cdbd-4339-a46e-6545f18c1225/26-development.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/aa6ebc7b-cdbd-4339-a46e-6545f18c1225/26-development.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/aa6ebc7b-cdbd-4339-a46e-6545f18c1225/26-development.png"
			sizes="100vw"
			alt="Flow graph showing the different processes, specifically development and content population"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<p>In our experience, this often is the slowest part of any project. However, with all of the content creation finished early on in the process, this task should just require a copy-and-paste into the CMS, saving considerable time, stress and delays.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b2992e43-6ce5-4aae-9d5a-28b9bde63416/27-design-3.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b2992e43-6ce5-4aae-9d5a-28b9bde63416/27-design-3.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b2992e43-6ce5-4aae-9d5a-28b9bde63416/27-design-3.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b2992e43-6ce5-4aae-9d5a-28b9bde63416/27-design-3.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b2992e43-6ce5-4aae-9d5a-28b9bde63416/27-design-3.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b2992e43-6ce5-4aae-9d5a-28b9bde63416/27-design-3.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b2992e43-6ce5-4aae-9d5a-28b9bde63416/27-design-3.png"
			sizes="100vw"
			alt="Flow graph showing the different processes, specifically design and rounds of testing"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<p>As usual, test, test, and test again. Crawl the site, add all of your tracking codes, add to Search Console, make sure it’s indexed &mdash; the full works!</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c04c7fdd-0ee6-4cce-94d8-ef0f1086ba27/28-development-2.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c04c7fdd-0ee6-4cce-94d8-ef0f1086ba27/28-development-2.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c04c7fdd-0ee6-4cce-94d8-ef0f1086ba27/28-development-2.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c04c7fdd-0ee6-4cce-94d8-ef0f1086ba27/28-development-2.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c04c7fdd-0ee6-4cce-94d8-ef0f1086ba27/28-development-2.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c04c7fdd-0ee6-4cce-94d8-ef0f1086ba27/28-development-2.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c04c7fdd-0ee6-4cce-94d8-ef0f1086ba27/28-development-2.png"
			sizes="100vw"
			alt="Flow graph showing the different processes, specifically development and launch, and post launch review"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<p>Were we right? Have the goals succeeded? <strong>A website is never finished</strong>. Keep tracking and reporting, always remembering the goals set out at the start of the project.</p>

<p>Although it might seem a lot, only a few extra steps have been added to the whole process. With keyword research and a content strategy the focus at the start of the project, the aims of the site are more clearly defined, and its entire structure mapped out and understood, with everything in its right place. Two costly and complex projects, an SEO/content campaign and web design, become one &mdash; and one that is far more manageable, efficient, and ultimately produces a better result.</p>

<p>This is kind of an ideal scenario &mdash; most of the time our work involves working on sites that have been built without SEO in mind, and we come to help afterwards. We see our roles shifting as more people realize the logic behind SEOs, developers, and designers working together on projects, rather than in sequence, undermining each other’s efforts along the way.</p>

<h4 id="further-reading">Further Reading</h4>

<ul>
<li>“,” Search Engine Land</li>
<li>“,” Allie Gray Freeland, Smashing Magazine</li>
<li>“,”</li>
<li>“,” Smashing Magazine</li>
<li>“,” Lyndon Cerejo, Smashing Magazine</li>
<li>“,” SEO Learning Center, Moz.com</li>
<li>“,” Jordan Julien, UXmatters</li>
<li>“,” Paul Boag, Smashing Magazine</li>
<li>“,” Alex Chris, DigitalMarketingPro.net</li>
<li>“,” James George, Design Crawl</li>
<li>“,” Infographic, Keyword Hero</li>
<li>“,” SiteVisibility</li>
<li>“,” Kyle Fiedler, Smashing Magazine</li>
<li>“,” Carla Dawson, TemplateMonster</li>
<li>“,” Xander Marketing</li>
</ul>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(ra, il)</span>
</div>


              </article>
            </body>
          </html>
---------------
<h1 id="#title_12" >13、每周分享第 12 期</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2018/07/weekly-issue-12.html](http://www.ruanyifeng.com/blog/2018/07/weekly-issue-12.html)
<p>这里记录过去一周，我看到的值得分享的东西，每周五发布。</p>

        <p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018070601.jpg" alt="" title="" /></p>

<p>（题图：佘山，上海，2018。）</p>

<p>我看到一篇，美国2016年的社会福利支出，占到政府总支出的73%。这就是说，美国政府的大部分支出，都用在养老金、医疗保险、失业救济这些方面了。现在，大多数的美国穷人和老人，都仰仗政府的这笔支出活着。问题是，美国政府快要承担不起了。</p>

<p>政府的钱从哪里来？主要就是两个途径：债务和税收（包含强制保险）。现在，美国的政府债务已经了 GDP，很难再大规模举债了。而税收本质上是用下一代的钱，养活上一代的人。现在人口老龄化，不工作的老人越来越多，交税的人口比例在下降，因此税收也不够用。总之，美国福利制度快要不行了，需要大大地压缩支出。</p>

<p>全世界的发达国家，几乎都面临同样问题：福利社会太昂贵，政府提供不起全民的社会保险。日本最严重，已经把退休年龄提高到了70岁。你要活到70岁，政府才开始发给你养老金。</p>

<p>对于刚刚就业的年轻人来说，这就是现实，政府很难保障每个人的养老，政府发放的养老金几乎肯定靠不住。你必须靠自己，否则将来的养老一定会成大问题，会出现很多"人还没死，钱却花光"的情况。</p>

<h2>新闻</h2>

<p>1、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018070602.jpg" alt="" title="" /></p>

<p>6月中旬，旧金山举行了一次机器与人的辩论比赛，一方是 IBM 公司的辩论软件 Debator，另一方是人类的专业辩手，包括以色列全国辩论冠军。每位参加者有四分钟的时间阐述观点，然后是四分钟的反驳和两分钟的结论。软件分析人类的发言，然后检索数以亿计的报纸文章和学术论文库，以及一些预先安装的论据，结果并不处于下风，很顺利地完成了一场辩论赛。</p>

<p>2、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018070603.jpg" alt="" title="" /></p>

<p>人类已经发射了几千颗卫星，太空布满了这些卫星的碎片，对未来的飞行安全造成很大威胁。英国的一家卫星制造公司设计了一种太空清洁车，用渔网和叉子捕捉这些碎片带回地球。</p>

<p>3、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018070604.jpg" alt="" title="" /></p>

<p>OpenAI 公司宣布，开发了一种人工智能软件，可以跟人类对战 Dota2 ，已经能够战胜普通选手。7月28日将举办与职业选手的挑战赛，全世界直播。</p>

<p>这个软件的难点在于，Dota2 是组队比赛，采用5x5的模式。软件必须用5个算法实例组队，与5个人类对战。所以，算法需要协同，5个算法实例互相沟通，组成一个队伍共同作战。</p>

<p>4、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018070605.jpg" alt="" title="" /></p>

<p>印度最大城市孟买宣布，禁止一次性塑料用品。凡是使用一次性塑料袋、杯子或瓶子的居民，将被处以高达25,000卢比（276英镑）的罚款或者三个月监禁。主要原因是塑料不会降解，只使用一次就扔掉的塑料，对环境影响太大。</p>

<p>1950年以来，全球约有63亿吨塑料被丢弃到自然环境中，其中大部分在450年内都不会分解。 世界上一半的塑料是在过去13年生产的，其中又有一半是一次性产品（如袋子、杯子或吸管）。印度是全球塑料废物管理不善率最高的国家之一，城市和海滩上，常常布满了塑料垃圾。</p>

<p>5、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018070606.jpg" alt="" title="" /></p>

<p>麻省理工学院正在开发一种可以用脑电波和手势控制的机器人。通过监控脑电波，系统可以实时检测，人类是否在机器人执行任务时发现错误；通过监控肌肉活动，人类可以用手势操作机器人。</p>

<p>这个系统将一系列电极放在用户的头皮和前臂上，用来监控脑电波和肌肉活动。研究团队发现，当人们注意到错误时，脑电波会出现"错误相关电位"。因此，可以使用这个电信号，获得人类对机器人行为的评价，进而用来纠正机器人行为。研究人员希望有一天，这个系统可以用于帮助老年人、有语言障碍或行动不便的人。</p>

<p>6、</p>

<p>6月28日，香港政府宣布，对空置一年及以上的一手住宅征收空置税。它将成为中国首个开征房屋空置税的城市。</p>

<p>征收时，政府会对房屋的租金做一个评估，空置税为年租金的200%。这就是说，如果买来房子空关，政府会对你罚款，最低限度你应该把房子租出去。政府希望这样可以缓解香港的房价上涨。香港的房价是全球最贵、且还在不断上涨。</p>

<p>7、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018070607.jpg" alt="" title="" /></p>

<p>波音公司展示了一款正在开发的概念机型，这种超音速客机可以在二个小时内到底地球的任何地点。就算一切顺利，这种飞机估计最快也要20年以后才能投入使用，而且造价将非常高昂，每架都要几亿甚至十亿美元。</p>

<p>8、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018070608.jpg" alt="" title="" /></p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018070609.jpg" alt="" title="" /></p>

<p>以色列电子烟创业公司 Juul 获得12亿美元投资，估价为150亿美元。这家公司成立于2015年，长方形的电子烟包含电池和装有液体的容器，液体包含尼古丁成分，吸吮会产生类似吸烟的感觉。 </p>

<p>截至上个月，Juul占据了美国电子卷烟市场68％的份额。自2017年1月以来，卷烟的市场份额下降了近4个百分点，而Juul的市场份额在同一时期大幅上升了3.5个百分点。 </p>

<p>由于各国政府对烟草的限制越来越多，而人类的焦虑也在不断增长，所以电子烟有很好的前景。长期来看，电子烟更便宜，而且以后技术发展了，可能可以达到无害且精确的神经刺激作用。</p>

<p>9、</p>

<p>6月29日，比特币发明人中本聪现身，宣布将发布一本书，公布一些事实，并且贴出了。不过，无法确认真实性，因为网站没有给出任何可以验证身份的数字签名。</p>

<h2>教程</h2>

<p>1、（英文）</p>

<p>devops 是 IT 行业的一个新兴领域，这一类工程师的职务应该怎么分类呢？这篇文章认为可以分成三种职务：运维（Operations）、平台工程（Platform Engineering）、发布管理（Release Management）。</p>

<p>2、（英文）</p>

<p>MySQL 的 utf8 字符集不是真正的 UTF-8，只支持最多三个字节的字符。真正的 UTF-8 可能会出现四个字节的字符。MySQL 从来没有修复这个 Bug，而是使用另外的解决方法：真正的 UTF-8字符集改用 utf8mb4 的名字提供。.</p>

<p>3、（英文）</p>

<p>UV、PV、跳出率（bounce rate）这些词到底是什么意思？怎么计算？</p>

<p>4、（英文）</p>

<p>这篇文章写于2014年，回顾了互联网开发技术的历史。客户端的部分看不看无所谓，服务器的部分写得很好。</p>

<p>5、（英文）</p>

<p>socks 是一种服务器的通信代理协议，本文介绍它的一些基本知识。</p>

<p>6、（英文）</p>

<p>Flutter 是谷歌推出的跨平台App开发工具。只要写一次代码，就能同时编译出安卓和iOS两个平台的App。这篇是一个 iOS 开发者的试用报告，他说他对 Flutter 感到非常满意。</p>

<p>7、（英文）</p>

<p>Channel 是 Web Socket 协议的封装，提供服务器、PC端、手机端的库，做到客户端订阅服务器事件，或者服务器订阅客户端事件。</p>

<p>8、（中文）</p>

<p>Rust 是一种静态的编译型语言，实现了<code>C</code> 或 <code>C++</code> 大部分的功能。但是不同于 <code>C</code> 和 <code>C++</code>，Rust 还可以进入 <code>C#</code> 和 Java 长时间统治的领域：自动内存管理。Rust 语言既有低级语言的速度优势，同时又不用手动管理内存，还不存在麻烦的垃圾收集机制。</p>

<p>9、（中文）</p>

<p>WebAssembly 并不是一门编程语言，而是一份字节码标准，需要用高级编程语言编译出字节码放到 WebAssembly 虚拟机中才能运行， 浏览器厂商需要做的就是根据 WebAssembly 规范实现虚拟机。本文重点介绍如何使用 AssemblyScript 来编写 WebAssembly。</p>

<h2>资源</h2>

<p>1、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018070610.jpg" alt="" title="" /></p>

<p>一个美国程序员业余喜欢演奏风琴。他把自己的50多首演奏录音，免费放到网上，我觉得很好听。</p>

<p>2、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018070611.jpg" alt="" title="" /></p>

<p>一款类似塞尔达的 WebGL 游戏，制作非常精美，推荐试玩。</p>

<p>3、（英文）</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018070612.jpg" alt="" title="" /></p>

<p>这本书（Paradigms of Artificial Intelligence Programming）是人工智能领域的名著，Peter Norvig 写于 1992 年，探讨 Lisp 语言在这方面的应用，现在开源了。</p>

<p>4、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018070613.jpg" alt="" title="" /></p>

<p>Mac 的一大烦恼，就是各种软件都要钱。有人整理出了一份 Mac 系统免费软件清单，看看有没有你需要的。</p>

<h2>工具</h2>

<p>1、</p>

<p>Node 语言编写的博客建站工具。</p>

<p>2、</p>

<p>英语单词"词干化"的 Node 库，比如 <span data-type="color" style="color:rgb(0, 0, 0)">am, are, is 都会转成 be，这是自然语言处理必须的。</span> </p>

<p>3、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018070614.jpg" alt="" title="" /></p>

<p>直接将 Markdown 文档转换生成幻灯片。</p>

<p>4、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018070615.jpg" alt="" title="" /></p>

<p>微软正在使用 React 重写 Office365（Office 的在线版），为此专门写了一个 React 的 Office UI 组件库，完全开源。</p>

<p>5、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018070616.jpg" alt="" title="" /></p>

<p>生成本地 HTTPS 加密证书的工具，一个命令就可以生成证书，不需要任何配置。图片是就是它默认为 localhost 生成的加密证书。</p>

<p>6、</p>

<p>一个反向代理服务器，主要特点是进行了各种优化和压缩，号称可以把网站速度提高3到4倍。</p>

<h2>文摘</h2>

<p>1、</p>

<p>2018年1月，我刚刚过完生日，便和伙伴刘怡老师一起踏上了沙特阿拉伯的行程。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018070617.jpg" alt="" title="" /></p>

<p>圣城麦加的禁寺，是我很长时间最向往的地方。我毫不掩饰自己刚刚看到它时的激动！看到无数穆斯林围绕着克尔白天房旋转的时候，这样的人类行为真的是太震撼了。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018070618.jpg" alt="" title="" /></p>

<p>这张照片是周五主麻时，无数来自全世界各地的穆斯林对着克尔白天房跪拜的场景，为了这个场景，我不得不花费3000人民币的高价，在禁寺旁的钟楼酒店的裙楼里开间房，若是钟楼酒店看禁寺的房间，价格得接近一万元，实在是太贵了。</p>

<p>我径直来到禁寺的最高一层，在这里俯瞰克尔白天房，还有围绕着它不断旋转的全世界各地的穆斯林。这个人类行为，已经这样24小时不停歇的旋转了一千多年。禁寺太大了，由于我的镜头是35mm，所以这张照片是用8张照片合成的。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018070619.jpg" alt="" title="" /></p>

<p>当人流量减少之后，禁寺的清理部门便开着这样的清洁车清洁禁寺外的大理石地面。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018070620.jpg" alt="" title="" /></p>

<p>麦加的国际化程度也是超出我想象的，我可以看到手拎着印有H&amp;M购物袋的女性，手拿一杯星巴克，走进禁寺旁商场内的麦当劳。</p>

<p>年轻女性穆斯林，她们手拿智能手机，也喜欢自拍，和全世界各地的女性无任何差别。我还发现一个现象，那就是沙特女性地位真的很高，根本不像外界媒体宣传的那样。而且随着新王储的不断改革，沙特女性在日常生活中扮演的角色会越来越多。</p>

<p>2、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018070621.jpg" alt="" title="" /></p>

<p>史蒂夫·乔布斯创造了 iPhone、iPad 和其他许多东西，让苹果成为全球最有价值的公司。但是，如果年青时代的他来到你的公司，要求一份工作，你会雇佣他吗？</p>

<p>他桀骜不驯，目中无人，大学也没毕业。虽然表现对技术的兴趣，但看起来像一个嬉皮士，穿衣服很随便，身上还有一股味道，员工们都抱怨他很少洗澡。他身上充满了各种消极因素，明显没达到岗位要求的资格。他还喜欢发号施令，操纵别人。</p>

<p>看到这么多缺点，你可能犹豫了，打算拒绝他了。但是你应该看到，他也有长处：不懈地追求完美，毫不妥协地坚持高标准，并且神奇地了解消费者需求和欲望。</p>

<p>管理大师德鲁克说过一句话："没有缺点的员工，只会造出平庸的产品"。你要想办法雇佣到一个人的长处，而不是买到他的缺点。</p>

<h2>本周图片</h2>

<p>1、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018070622.jpg" alt="" title="" /></p>

<p>瑞士数学家欧拉（Leonhard Euler，1707年4月15日－1783年9月18日），被认为是有史以来最伟大的数学家之一。他有很多成就，其中一项就是发明了上图的5个符号。</p>

<p>2、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018070623.jpg" alt="" title="" /></p>

<p>墨西哥的 Sistema Huaulta 是世界最大的洞穴之一，也是西半球最深的洞穴，长达85公里，深达1.5公里，共有25个入口。去年一个美国探险队深入这个洞穴，《国家地理》杂志写了详细的图片报道。</p>

<p>3、（组图）</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018070624.jpg" alt="" title="" /></p>

<p>明尼苏达州圣保罗市，6月13日，有人发现一只浣熊正在爬一幢25层高楼。经过社交媒体转发和直播，这只浣熊成为当天推特的热门话题，电视台也开始滚动报道。</p>

<h2>本周金句</h2>

<p>1、</p>

<p>公司发展到一定阶段，能力强的员工容易离职，因为他们对公司内愚蠢的行为的容忍度不高，他们也容易找到好工作，能力差的员工倾向于留着不走，他们也不太好找工作，年头久了，他们就变中高层了。这种现象叫"死海效应"；好员工像死海的水一样蒸发掉，然后死海盐度就变得很高，正常生物不容易存活。（）</p>

<p>2、</p>

<p>如何生成一个随机字符串？一种方法是让新手使用 vim，但是不告诉他们怎么保存文档和退出。（推特）</p>

<p>3、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018070625.jpg" alt="" title="" /></p>

<p>如果有一天，人们不再使用app，改为使用网站，一定是因为每个app 启动时，都要强迫用户看5秒钟毫无意义的、让你傻等的全屏广告（英语叫 splash screen）。</p>

<h2>欢迎订阅</h2>

<p>这个专栏每周五发布，同步更新在我的。</p>

<p>微信搜索"<strong>阮一峰的网络日志</strong>"或者扫描二维码，即可订阅。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2018/bg2018042311.jpg" alt="image | left" title="" /></p>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2018-07-06T13:51:39+08:00">2018年7月 6日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>文集：</li>
<li>社交媒体：</li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------