## 文章索引
1、 <a href="#1#330:-prettier-10-what-is-graphql-and-crockfords-post-javascript-apocalypse" >#330: Prettier 1.0, What is GraphQL, and Crockford's Post JavaScript Apocalypse</a><br/>
2、 <a href="#2数字时代的精益组织" >数字时代的精益组织</a><br/>
3、 <a href="#3依赖类型语言idris发布10版本" >依赖类型语言Idris发布1.0版本</a><br/>
4、 <a href="#4net-framework-47改进了wpf和winforms" >.NET Framework 4.7改进了WPF和WinForms</a><br/>
5、 <a href="#5从ng-conf-2017大会获悉angular将获得长期支持" >从ng-conf 2017大会获悉，Angular将获得长期支持</a><br/>
6、 <a href="#6区块链与cap原理" >区块链与CAP原理</a><br/>
7、 <a href="#7cloudnativecon和kubecon大会摘要kubernetes-16dockercoreos捐赠以及资格认证" >CloudNativeCon和KubeCon大会摘要：Kubernetes 1.6、Docker、CoreOS、捐赠以及资格认证</a><br/>
8、 <a href="#8视频演讲-学而优则仕仕而优则学" >视频演讲： 学而优则仕，仕而优则学</a><br/><h1 id="#title_0" >1、#330: Prettier 1.0, What is GraphQL, and Crockford's Post JavaScript Apocalypse</h1>

[http://javascriptweekly.com/issues/330](http://javascriptweekly.com/issues/330)
<table border="0" width="100%" cellpadding="0" cellspacing="0" bgcolor="#ffffff" style="font-family: 'helvetica neue', helvetica, arial, sans-serif; font-size: 14px; line-height: 20px; color: #333"><tr><td align="center" valign="top">
<table border="0" width="600" cellpadding="0" cellspacing="0" class="container noarchive" style="border-collapse: collapse;"><tr><td style="padding-top: 6px; padding-bottom: 6px; font-size: 11px; text-align: center; color: #555; font-family: verdana, arial, sans-serif">
<span class="nomo">This week's JavaScript news</span> — 
</td></tr></table>
<table border="0" width="600" cellpadding="0" cellspacing="0" class="container" style="border-collapse: collapse">
<tr><td style="background-color: #f7df1e"><table width="100%" cellspacing="0" cellpadding="0" align="left"><tr><td align="left" class="block" style="padding: 6px 12px;">
<table align="left" width="50%" class="gowide"><tr><td><span style="line-height: 36px; font-size: 23px; color: #f7df1e; font-weight: bold; color: #323330">JavaScript Weekly</span></td></tr></table>
<table align="left" style="text-align: right" width="50%" class="gowide lonmo"><tr><td><span style="font-size: 14px; line-height: 36px; font-weight: normal; color: #323330">
Issue 330 — April 14, 2017
</span></td></tr></table>
</td></tr></table></td></tr>
<tr><td style="padding: 16px 12px 12px 12px" align="left">
<div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">A fantastic round-up of concepts, tools, and things to consider when doing one of a developer’s most important tasks: debugging.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Sarah Drasner
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">Just 3 months old, Prettier is already  in the industry for standardizing code style/formatting. With 1.0, the creators are putting their ‘safe for production’ stamp on it.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Christopher Chedeau
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">If GraphQL is yet another buzzword flying past, this is a great introduction to what the declarative data querying approach could be doing for you.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Sacha Greif
</div>
<br clear="all" style="clear: both"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">Lob provides an API that enables developers to send postcards, letters, checks, and more as effortlessly as sending emails. Lob is based in San Francisco, CA and is venture backed with over 6000 customers including Amazon, Square, and Counsyl.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Lob.com
  <span style="border: 1px solid #999; border-radius: 2px; color: #999; font-size: 11px; font-weight: normal; padding: 1px 5px 1px 5px; ">Sponsor</span>
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">Slack recently ported their desktop app over to using TypeScript, here Felix Rieseberg reflects on the experience. Also this week, Ember’s Tom Dale , with examples.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Slack
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">Doug Crockford (author of <em>JavaScript: The Good Parts</em>) has been speculating on what should come <em>after</em> JavaScript while sharing his love and distaste for various languages over the years. <em>(46 minutes)</em>
</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Douglas Crockford
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">
 as the eventually preferred approach.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Vitaly Slobodin
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">Learn to build data-driven apps with Vue 2. Olayinka Omole creates a simple client to pull news stories from the New York Times API with the Axios library.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Sitepoint
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">A release that helps pave the way for React 16. See today’s  for more.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Andrew Clark
</div>
<br clear="all" style="clear: both"><p style="color: #666666; font-size: 16px; font-weight: bold; margin-top: 8px; margin-bottom: 10px; text-transform: uppercase">Jobs </p>
<ul style="padding-left: 18px; margin-top: 10px; list-style-type: square">
<li style="color: #f7df1e; margin-bottom: 10px; font-size: 15px; line-height: 17px">
<span style="font-size: 12px; color: #666666">Do you love JavaScript? We do! React, Redux, and Node: it’s JavaScript all the way down. Join us!</span> <span style="color: #999999; font-weight: normal; font-size: 12px; text-transform: uppercase; font-family: verdana, arial, sans-serif">BLOGFOSTER GMBH</span>
</li>
<li style="color: #f7df1e; margin-bottom: 10px; font-size: 15px; line-height: 17px">
<span style="font-size: 12px; color: #666666">Refactoring our entire frontend, and all the impact around it. Join us building the ultimate online playground for kids of all ages.</span> <span style="color: #999999; font-weight: normal; font-size: 12px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Poki</span>
</li>
<li style="color: #f7df1e; margin-bottom: 10px; font-size: 15px; line-height: 17px">
<span style="font-size: 12px; color: #666666">Econify is a development shop with large media clients. We’re seeking developers with NodeJS experience to solve at scale problems.</span> <span style="color: #999999; font-weight: normal; font-size: 12px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Econify</span>
</li>
</ul>
<p style="color: #333; font-size: 12px; font-weight: normal; margin-top: 0px; margin-bottom: 10px">Can't find the right job? Want companies to apply to <em>you?</em> </p>
<p style="color: #666666; font-size: 16px; font-weight: bold; margin-top: 24px; margin-bottom: 10px; text-transform: uppercase">In Brief</p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #00aadd; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">news</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Seth Thompson</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #00aadd; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">news</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">JSDayES  <span style="border: 1px solid #999; border-radius: 2px; color: #999; font-size: 11px; font-weight: normal; padding: 1px 5px 1px 5px;">Sponsor</span></span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #00aadd; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">news</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Vue.js Conference</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #00aadd; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">news</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">Ignition and TurboFan are now enabled by default.</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Benedikt Meurer</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #00aadd; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">news</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Microsoft</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Matt Rothenberg</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Netanel Basal</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Ulrich-Matthias Schäfer</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Dylan Schiemann</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <br><span style="font-size: 13px; color: #444444; line-height: 19px">A feature to quickly inspect any expression value, even in the middle of a chain of function calls.</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Wallaby.js  <span style="border: 1px solid #999; border-radius: 2px; color: #999; font-size: 11px; font-weight: normal; padding: 1px 5px 1px 5px;">Sponsor</span></span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #cc00cc; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">video</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">ReactCasts</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #cc00cc; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">video</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">LinkedIn</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #bbbbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tools</span> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #6ca629; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">node</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Yohan Lasorsa</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px">.</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Red Gate  <span style="border: 1px solid #999; border-radius: 2px; color: #999; font-size: 11px; font-weight: normal; padding: 1px 5px 1px 5px;">Sponsor</span></span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"></span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Pulusani, Khalkhali, and Wagner</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #00bbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">code</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">Delays, throttled maps, callback/event/successes awaiting.</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Hunter Loftis</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #00bbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">code</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Photopea</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #00bbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">code</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Eric JJ</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #00bbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">code</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Luigi De Rosa</span></p>
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
<h1 id="#title_1" >2、数字时代的精益组织</h1>
Ben Linders
[http://www.infoq.com/cn/news/2017/04/lean-digital-age?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/04/lean-digital-age?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>精益IT应该帮助简化和改善我们为客户创造价值的方式，并提出面向未来的更好的解决方案。未来的组织将专注于同行业的产品或业务流——其他的一切，包括专家和管理者在内，都是为了让一线工作人员可以第一时间就做好，而又不会遇到任何麻烦。</p> <i>By Ben Linders</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_2" >3、依赖类型语言Idris发布1.0版本</h1>
Sergio De Simone
[http://www.infoq.com/cn/news/2017/04/idris-1-released?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/04/idris-1-released?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>英国圣安德鲁大学讲师、Idris创建者Edwin Brady写道，在达到alpha版本几个月之后，Idris 1.0发布。</p> <i>By Sergio De Simone</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_3" >4、.NET Framework 4.7改进了WPF和WinForms</h1>
Jeff Martin
[http://www.infoq.com/cn/news/2017/04/net47?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/04/net47?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>.NET Framework 4.7与Windows 10 Creators Update一起登台亮相，它支持高分辨率的Windows Forms应用，并对运行在Windows 10上的WPF应用提供了触屏和手写笔的支持。</p> <i>By Jeff Martin</i> <i> Translated by Rays</i>
---------------
<h1 id="#title_4" >5、从ng-conf 2017大会获悉，Angular将获得长期支持</h1>
David Iffland
[http://www.infoq.com/cn/news/2017/04/ng-conf-2017-keynote?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/04/ng-conf-2017-keynote?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>在ng-conf 2017大会主题演讲期间，Igor Minarh和Steven Fluin花时间展示了Angular软的一面。在回顾了主要的技术主题后，他们将重点放在了社区和Angular未来的发展上。他们宣布将长期提供Angular v4支持。</p> <i>By David Iffland</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_5" >6、区块链与CAP原理</h1>
Andrew Morgan
[http://www.infoq.com/cn/news/2017/04/blockchain-cap-theorem?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/04/blockchain-cap-theorem?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>微软首席架构师Yaron Goland最近发表了一篇文章，讲述了一个区块链客户端如何可以被实现为AP的或CP的，这取决于它的实现方式。具体是要可以配置在一个事务结束之后必须有多少个区块收到这个事务，才认为它可以被接受了。在事务之后接收到它的区块越多，它就越可能获得系统范围内的共识，即一致性。</p> <i>By Andrew Morgan</i> <i> Translated by 足下</i>
---------------
<h1 id="#title_6" >7、CloudNativeCon和KubeCon大会摘要：Kubernetes 1.6、Docker、CoreOS、捐赠以及资格认证</h1>
Daniel Bryant
[http://www.infoq.com/cn/news/2017/04/cloudnativecon-kubecon-1?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/04/cloudnativecon-kubecon-1?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>在CloudNativeCon和KubeCon Europe联合举办的技术大会上，原生云计算基金会（Cloud Native Computing Foundation，CNCF）通告如下：发布最新版本的容器调度平台，Kubernetes 1.6；CNCF接管Docker的containerd和CoreOS的rkt容器技术项目；发布“Kubernetes管理员资格证考试（Kubernets Certified Administrator Exam）”课程。</p> <i>By Daniel Bryant</i> <i> Translated by 张健欣</i>
---------------
<h1 id="#title_7" >8、视频演讲： 学而优则仕，仕而优则学</h1>
邹光先
[http://www.infoq.com/cn/presentations/the-relation-of-official-and-excellent?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/the-relation-of-official-and-excellent?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/the-relation-of-official-and-excellent/zh/mediumimage/zouguagnxian270.jpg"/><p>听众收益：1、探讨技术路线和管理路线的选择；2、初创企业的人才要求； 3、初创企业如何建立研发和管理体系。</p> <i>By 邹光先 </i>
---------------