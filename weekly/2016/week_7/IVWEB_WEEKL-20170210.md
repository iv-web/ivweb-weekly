## 文章索引
1、 <a href="#1js-startup-performance-/-webassembly-performance-/-react-native-at-instagram" >JS startup performance / WebAssembly performance / React Native at Instagram</a><br/>
2、 <a href="#2ios-开发周报apple新一季财报成绩喜人reactivecocoa的状态驱动" >iOS 开发周报：Apple新一季财报成绩喜人、ReactiveCocoa的状态驱动</a><br/>
3、 <a href="#3文章-采访wesley-coelhodevops面临的挑战" >文章： 采访Wesley Coelho：DevOps面临的挑战</a><br/>
4、 <a href="#4文章-专访实体建模工具创造者frans-bouma" >文章： 专访实体建模工具创造者Frans Bouma</a><br/>
5、 <a href="#5文章-google的野心为什么google用apache-beam彻底替换掉mapreduce" >文章： Google的野心：为什么google用Apache Beam彻底替换掉MapReduce</a><br/>
6、 <a href="#6twitter的支撑架构扩展网络与存储并提供服务" >Twitter的支撑架构：扩展网络与存储并提供服务</a><br/>
7、 <a href="#7视频演讲-apk-沙箱技术在平台型-app-中的架构实战" >视频演讲： APK 沙箱技术在平台型 App 中的架构实战</a><br/>
8、 <a href="#8chaperone来自uber工程师团队的kafka监控工具" >Chaperone：来自Uber工程师团队的Kafka监控工具</a><br/>
9、 <a href="#9microsoft规划了net的未来发展" >Microsoft规划了.NET的未来发展</a><br/>
10、 <a href="#10snap斥资20亿美元用于购买google的云基础设施服务" >Snap斥资20亿美元，用于购买Google的云基础设施服务</a><br/>
11、 <a href="#11how-to-create-a-realistic-clock-in-sketch" >How To Create A Realistic Clock In Sketch</a><br/>
12、 <a href="#12android开发周报谷歌推出搜即得应用android硬件加速原理解析" >Android开发周报：谷歌推出搜即得应用、Android硬件加速原理解析</a><br/>
13、 <a href="#13ionic-2版本进行了性能提升并提供新的本地插件系统" >Ionic 2版本进行了性能提升并提供新的本地插件系统</a><br/><h1 id="#title_0" >1、JS startup performance / WebAssembly performance / React Native at Instagram</h1>

[http://javascriptweekly.com/issues/321](http://javascriptweekly.com/issues/321)
<table border="0" width="100%" cellpadding="0" cellspacing="0" bgcolor="#ffffff" style="font-family: 'helvetica neue', helvetica, arial, sans-serif; font-size: 14px; line-height: 20px; color: #333"><tr><td align="center" valign="top">
<table border="0" width="620" cellpadding="0" cellspacing="0" class="container noarchive" style="border-collapse: collapse;"><tr><td style="padding-top: 6px; padding-bottom: 6px; font-size: 11px; text-align: center; color: #555; font-family: verdana, arial, sans-serif">
<span class="nomo">This week's JavaScript news</span> — 
</td></tr></table>
<table border="0" width="620" cellpadding="0" cellspacing="0" class="container" style="border-collapse: collapse">
<tr><td style="background-color: #f7df1e"><table width="100%" cellspacing="0" cellpadding="0" align="left"><tr><td align="left" class="block" style="padding: 6px 12px;">
<table align="left" width="50%" class="gowide"><tr><td><span style="line-height: 36px; font-size: 23px; color: #f7df1e; font-weight: bold; color: #323330">JavaScript Weekly</span></td></tr></table>
<table align="left" style="text-align: right" width="50%" class="gowide lonmo"><tr><td><span style="font-size: 14px; line-height: 36px; font-weight: normal; color: #323330">
Issue 321 — February 9, 2017
</span></td></tr></table>
</td></tr></table></td></tr>
<tr><td style="padding: 16px 12px 12px 12px" align="left">
<div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">A look at what’s involved in the process of getting your code running in the first place. What slows it down, how can you measure it, and what can you do to lower parse times?</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Addy Osmani
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">From 
</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Guillaume Plique
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">A trip down memory lane for anyone who was working with JavaScript in the late 00s as MooTools was a popular JS utility library at the time.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Between the Wires
</div>
<br clear="all" style="clear: both"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">Ideal for visualizing hierarchical data, sunburst charts display categorical data “tiers.” Walk through four steps, from preparing the data model to building the chart view, to display the periodic table of elements as a sunburst chart on the web using Wijmo.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Wijmo
  <span style="background-color: #f7df1e; color: #ffffff; font-weight: normal; padding: 1px 5px 0px 5px;">Sponsor</span>
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">React Native has come a long way since it was open-sourced in 2015. Instagram reflects on the successes some of its teams have had with it.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Instagram Engineering
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">
 makes it easy to create vector based graphics easily across browsers as far back as Chrome 1 and IE 6.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Roman Lubushkin
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">Work on  continues to march ahead, but are the promised performance gains coming to light? In Firefox, most definitely.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Stefan Krause
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">A Chrome extension that helps you see how your Vue.js app is running.</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">The first in a 4 part series () walking through the process of building an Angular(2) app with Angular-CLI and Material Design.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Tracy Lee
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">Queries data via your existing REST APIs, stores state and data within Redux reducers automatically, manages caching, and more.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Tony Holdstock-Brown
</div>
<br clear="all" style="clear: both"><p style="color: #666666; font-size: 16px; font-weight: bold; margin-top: 8px; margin-bottom: 10px; text-transform: uppercase">Jobs </p>
<ul style="padding-left: 18px; margin-top: 10px; list-style-type: square">
<li style="color: #f7df1e; margin-bottom: 10px; font-size: 15px; line-height: 17px">
<span style="font-size: 12px; color: #666666">We're looking for a developer with an extensive knowledge of JavaScript and skills in different frameworks and libraries. We are 100% remote and we provide the funding needed to help you achieve your goals and grow.</span> <span style="color: #999999; font-weight: normal; font-size: 12px; text-transform: uppercase; font-family: verdana, arial, sans-serif">X-Team</span>
</li>
<li style="color: #f7df1e; margin-bottom: 10px; font-size: 15px; line-height: 17px">
<span style="font-size: 12px; color: #666666">Civey is seeking an experienced developer with strong JavaScript skills and is familiar with HTTP, REST and Web Applications.</span> <span style="color: #999999; font-weight: normal; font-size: 12px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Civey</span>
</li>
</ul>
<p style="color: #333; font-size: 12px; font-weight: normal; margin-top: 0px; margin-bottom: 10px">Can't find the right job? Want companies to apply to <em>you?</em> </p>
<p style="color: #666666; font-size: 16px; font-weight: bold; margin-top: 24px; margin-bottom: 10px; text-transform: uppercase">In Brief</p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #00aadd; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">news</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">Voting is open for the next two weeks. The logo with the most ‘thumbs up’ will then be deemed the official WebAssembly logo.</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">WebAssembly</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #00aadd; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">news</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">Last chance for Advance tickets to 9 days of JavaScript lectures and workshops by industry experts.</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">ForwardJS &amp; Forward Swift  <span style="background-color: #f7df1e; color: #ffffff; font-weight: normal; padding: 1px 5px 0px 5px;">Sponsor</span></span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px"><em>“a real life use case for destructuring”</em></span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Phil Nash</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Sitepoint</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">The first in an introductory series.</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Sarah Drasner</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Prosper Otemuyiwa</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #AF7817; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">opinion</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif"></span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #AF7817; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">opinion</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Robin Wieruch</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #bbbbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tools</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">FuseBox is a “new generation bundler and module loader”.</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Feras Khoursheed</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #bbbbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tools</span> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #6ca629; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">node</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Cosmo</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #bbbbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tools</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">Unblock collaboration, quit reinventing the wheel, and build amazing things. Unleash the awesomeness, bring npm to work.</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">npm, Inc.  <span style="background-color: #f7df1e; color: #ffffff; font-weight: normal; padding: 1px 5px 0px 5px;">Sponsor</span></span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #00bbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">code</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif"></span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #00bbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">code</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif"></span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #00bbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">code</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">Averages to variance to probabilities to Bayesian classification.</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Tom MacWright</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #00bbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">code</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Luke Edwards</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #00bbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">code</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Ioannis Charalampidis</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #00bbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">code</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">A library developed for creating time-series plots of data measured at water flow sites.</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">United States Geological Survey</span></p>
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
<h1 id="#title_1" >2、iOS 开发周报：Apple新一季财报成绩喜人、ReactiveCocoa的状态驱动</h1>
靛青K
[http://www.infoq.com/cn/news/2017/02/iOS-weekly-ReactiveCocoa?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/02/iOS-weekly-ReactiveCocoa?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>因节假日 iPhone 卖得好，Apple 新一季财报成绩喜人、『状态』驱动的世界：ReactiveCocoa</p> <i>By 靛青K</i>
---------------
<h1 id="#title_2" >3、文章： 采访Wesley Coelho：DevOps面临的挑战</h1>
Shane Hastie
[http://www.infoq.com/cn/articles/agile2016-devops-challenges?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/agile2016-devops-challenges?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/agile2016-devops-challenges/zh/smallimage/logo.jpg"/><p>在敏捷2016大会上，InfoQ采访了Tasktop业务拓展高级总监Wesley Coelho，内容涉及DevOps固有的沟通障碍以及如何克服。DevOps和敏捷暴露出了组织筒仓以及需要自适应和自动化的瀑布式沟通流程。</p> <i>By Shane Hastie</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_3" >4、文章： 专访实体建模工具创造者Frans Bouma</h1>
Jonathan Allen
[http://www.infoq.com/cn/articles/Frans-Bouma-Interview?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/Frans-Bouma-Interview?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/Frans-Bouma-Interview/zh/smallimage/logo-net.jpg"/><p>我们今年的第一次关于.NET的采访对象是LLBLGen Pro的Frans Bouma。这个工具的历史几乎与.NET一样长，但是由于其商业产品的特殊性，它并没有其他一些免费工具那样知名。</p> <i>By Jonathan Allen</i> <i> Translated by 尚剑</i>
---------------
<h1 id="#title_4" >5、文章： Google的野心：为什么google用Apache Beam彻底替换掉MapReduce</h1>
足下
[http://www.infoq.com/cn/articles/why-google-replace-beam-with-apache-mapreduce?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/why-google-replace-beam-with-apache-mapreduce?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/why-google-replace-beam-with-apache-mapreduce/zh/smallimage/logo2 (7).jpg"/><p>1月10日，Apache软件基金会宣布，Apache Beam成功孵化，成为该基金会的一个新的顶级项目。谷歌坚信Apache Beam就是数据批量处理和流式处理的未来。</p> <i>By  足下</i>
---------------
<h1 id="#title_5" >6、Twitter的支撑架构：扩展网络与存储并提供服务</h1>
Daniel Bryant
[http://www.infoq.com/cn/news/2017/02/scaling-twitter-infrastructure?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/02/scaling-twitter-infrastructure?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Twitter工程团队近期提供了Twitter核心技术的演进和扩展的详细资料，这些核心技术支撑了Twitter自营数据中心的系统架构，用于提供社会媒体服务。在介绍核心技术实现细节的同时，他们也分享了很多架构设计实现中的关键经验教训。</p> <i>By Daniel Bryant</i> <i> Translated by Rays</i>
---------------
<h1 id="#title_6" >7、视频演讲： APK 沙箱技术在平台型 App 中的架构实战</h1>
黄明登
[http://www.infoq.com/cn/presentations/apk-sandbox-technology-in-platform-app-architecture?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/apk-sandbox-technology-in-platform-app-architecture?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/apk-sandbox-technology-in-platform-app-architecture/zh/mediumimage/huangmingdeng270.jpg"/><p>随着讯飞输入法的用户规模越来越大，平台效应和优势也越发突出。
如何借助输入法这个平台快速推广子产品，降低用户接触这些 App 的门槛？同时如何解决主、子产品间的架构耦合问题？主、子产品属于不同的业务团队，如何解决多团队协同开发的问题？
APK 沙箱技术是指在 App 内部建立一个隔离的运行环境，在里面直接运行第三方 App，这种技术方案为解决上述问题提供了一条可行之路，本次演讲将分享其技术实现原理以及在讯飞输入法中的实践经验。</p> <i>By 黄明登</i>
---------------
<h1 id="#title_7" >8、Chaperone：来自Uber工程师团队的Kafka监控工具</h1>
Hrishikesh Barua
[http://www.infoq.com/cn/news/2017/02/chaperone-kafka-audit-tool?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/02/chaperone-kafka-audit-tool?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Uber工程师团队发布了开源项目Chaperone，这是一个Kafka监控工具。在Uber，它被用于监控并检测多个数据中心及大容量Kafka集群中数据丢失、延迟以及重复的问题。</p> <i>By Hrishikesh Barua</i> <i> Translated by 周元昊</i>
---------------
<h1 id="#title_8" >9、Microsoft规划了.NET的未来发展</h1>
Jeff Martin
[http://www.infoq.com/cn/news/2017/02/strategic-net?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/02/strategic-net?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/news/2017/02/strategic-net/zh/headerimage/GettyImages-494890850.jpg"/><p>虽然C#、VB.NET和F#的开发是通过GitHub公开进行的，但是Microsoft的长远规划却经常是保密的。近期Microsoft的Mads Torgersen分享了.NET语言家族的更新策略，给出了对Microsoft未来的功能考虑的深刻理解。</p> <i>By Jeff Martin</i> <i> Translated by Rays</i>
---------------
<h1 id="#title_9" >10、Snap斥资20亿美元，用于购买Google的云基础设施服务</h1>
薛命灯
[http://www.infoq.com/cn/news/2017/02/Snap-buy-Google-cloud?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/02/Snap-buy-Google-cloud?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>2月2号，Snap公布了IPO白皮书，准备登陆纽交所，期望估值达到了250亿美元。值得一提的是，Snap在S1文件中披露了在未来5年将总共斥资20亿美元用于购买Google的云基础设施服务。</p> <i>By  薛命灯</i>
---------------
<h1 id="#title_10" >11、How To Create A Realistic Clock In Sketch</h1>
Christian Krammer
[https://www.smashingmagazine.com/2017/02/create-realistic-clock-sketch/](https://www.smashingmagazine.com/2017/02/create-realistic-clock-sketch/)
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
</table><p>Creating a clock in Sketch might not sound exciting at first, but we'll discover how easy it is to recreate real-world objects in a very accurate way. You'll learn how to apply multiple layers of borders and shadows, you'll take a deeper look at gradients and you will see how objects can be rotated and duplicated in special ways. To help you along the way you can also download the Sketch editable file.</p>

<figure></figure>

<p>This is a rather advanced tutorial, so if you are not that savvy with Sketch yet and need some help, I would recommend to first read "Design a Responsive Music Player in Sketch" () that cover a few key aspects in detail when working with Sketch. You can also have a look at my personal project <em>sketchtips.info</em> where I regularly provide tips and tricks about Sketch.</p>


<p>The post .</p>
---------------
<h1 id="#title_11" >12、Android开发周报：谷歌推出搜即得应用、Android硬件加速原理解析</h1>
郭亮
[http://www.infoq.com/cn/news/2017/02/Android-weekly-Android-Instant-A?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/02/Android-weekly-Android-Instant-A?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>谷歌推出四款Android Instant Apps，也就是即搜即得应用。Instant Apps类似于微信的小程序，无需安装，可直接使用。2017开发者大会将于5月17日至19日，在加州山景城的露天剧场举办。本期周报为大家带来了Android Things、Tinker接入、Gradle、逆向等多方面的技术干货，欢迎阅读。</p> <i>By 郭亮</i>
---------------
<h1 id="#title_12" >13、Ionic 2版本进行了性能提升并提供新的本地插件系统</h1>
James Chesters
[http://www.infoq.com/cn/news/2017/02/ionic-2?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/02/ionic-2?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Ionic团队发布了其2.0版本的JavaScript框架，新版本中提供了新的组件、功能和工具，包括新的本地插件系统。Ionic联合创始人Max Lynch介绍了Ionic应用程序大大受益于更快的Angular 2，使Ionic应用程序“固有的性能提升立竿见影”。</p> <i>By James Chesters</i> <i> Translated by 刘嘉洋</i>
---------------