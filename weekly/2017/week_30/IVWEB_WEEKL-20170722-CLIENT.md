## 文章索引
1、 <a href="#1#344:-javascript-factory-functions-with-es6+" >#344: JavaScript Factory Functions with ES6+</a><br/>
2、 <a href="#2salesforce三项新服务让crm具备认知能力" >Salesforce三项新服务让CRM具备认知能力</a><br/>
3、 <a href="#3rider首个发布候选版加入了性能提升特性" >Rider首个发布候选版加入了性能提升特性</a><br/>
4、 <a href="#4从ebay购物车丢失看处理网络i/o" >从eBay购物车丢失看处理网络I/O</a><br/>
5、 <a href="#5迷你书-架构师特刊进击的618" >迷你书： 架构师特刊：进击的618</a><br/>
6、 <a href="#6web-development-reading-list-#190:-images-in-web-notifications-and-angular-code-splitting" >Web Development Reading List #190: Images in Web Notifications and Angular Code Splitting</a><br/><h1 id="#title_0" >1、#344: JavaScript Factory Functions with ES6+</h1>

[http://javascriptweekly.com/issues/344](http://javascriptweekly.com/issues/344)
<table border="0" width="100%" cellpadding="0" cellspacing="0" bgcolor="#ffffff" style="font-family: 'helvetica neue', helvetica, arial, sans-serif; font-size: 14px; line-height: 20px; color: #333"><tr><td align="center" valign="top">
<table border="0" width="600" cellpadding="0" cellspacing="0" class="container noarchive" style="border-collapse: collapse;"><tr><td style="padding-top: 6px; padding-bottom: 6px; font-size: 11px; text-align: center; color: #555; font-family: verdana, arial, sans-serif">
<span class="nomo">This week's JavaScript news</span> — 
</td></tr></table>
<table border="0" width="600" cellpadding="0" cellspacing="0" class="container" style="border-collapse: collapse">
<tr><td style="background-color: #f7df1e"><table width="100%" cellspacing="0" cellpadding="0" align="left"><tr><td align="left" class="block" style="padding: 6px 12px;">
<table align="left" width="50%" class="gowide"><tr><td><span style="line-height: 36px; font-size: 23px; color: #f7df1e; font-weight: bold; color: #323330">JavaScript Weekly</span></td></tr></table>
<table align="left" style="text-align: right" width="50%" class="gowide lonmo"><tr><td><span style="font-size: 14px; line-height: 36px; font-weight: normal; color: #323330">
Issue 344 — July 21, 2017
</span></td></tr></table>
</td></tr></table></td></tr>
<tr><td style="padding: 16px 12px 12px 12px" align="left">
<div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px"><em>“In JavaScript, any function can return an object. When it does so without the new keyword, it’s a factory function.”</em></div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Eric Elliot
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">A fun look at the mechanics behind a seemingly simple snippet of JavaScript that doesn’t do what you’d expect. Beware of hidden Unicode characters.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Stefan Judis
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">This popular survey returns for its second year to see which <em>“buzzwords are here to stay and which ones will soon fall to JavaScript fatigue”</em>.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Sacha Greif
</div>
<br clear="all" style="clear: both"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">This free e-book teaches you about the strengths and weaknesses of JavaScript’s top frameworks and offers a methodology for selecting which framework works best for your team and project. .</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
GrapeCity Wijmo
  <span style="border: 1px solid #999; border-radius: 2px; color: #999; font-size: 11px; font-weight: normal; padding: 1px 5px 1px 5px; ">Sponsor</span>
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">Nirmalya Ghosh shows you how to use Firebase’s real-time database features, coupled with create-react-app, to build a basic Reddit clone with live voting.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
SitePoint
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">Compiles specially written JavaScript functions into shader language (GLSL) and runs them on the GPU via WebGL.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Sapuan, Saw and Cheah
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px"><em>“a good bit has changed in browser land since the last ‘You Might Not Need jQuery’ article you might have stumbled upon”</em></div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Ollie Williams
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">An explanation of a proposed new binary AST format and what benefits it could bring.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Shu-yu Guo
</div>
<br clear="all" style="clear: both"><p style="color: #666666; font-size: 16px; font-weight: bold; margin-top: 8px; margin-bottom: 10px; text-transform: uppercase">Jobs </p>
<ul style="padding-left: 18px; margin-top: 10px; list-style-type: square">
<li style="color: #f7df1e; margin-bottom: 10px; font-size: 15px; line-height: 17px">
<span style="font-size: 12px; color: #666666">Join us to impact how the world's biggest retailers operate by making a web app with great UX and DX using React, Redux and Glamor</span> <span style="color: #999999; font-weight: normal; font-size: 12px; text-transform: uppercase; font-family: verdana, arial, sans-serif">EDITED</span>
</li>
<li style="color: #f7df1e; margin-bottom: 10px; font-size: 15px; line-height: 17px">
<span style="font-size: 12px; color: #666666">We’re a growing realtime platform solving truly complex distributed problems for the developer community. If you enjoy challenging your grey matter and building great web services, apply.</span> <span style="color: #999999; font-weight: normal; font-size: 12px; text-transform: uppercase; font-family: verdana, arial, sans-serif">ABLY<span>.</span>IO</span>
</li>
<li style="color: #f7df1e; margin-bottom: 10px; font-size: 15px; line-height: 17px">
<span style="font-size: 12px; color: #666666">We are looking for a Software Engineer with strong interest and experience in UI engineering who can help take our newest product, New Relic Infrastructure, to the next level. </span> <span style="color: #999999; font-weight: normal; font-size: 12px; text-transform: uppercase; font-family: verdana, arial, sans-serif">New Relic</span>
</li>
</ul>
<p style="color: #333; font-size: 12px; font-weight: normal; margin-top: 0px; margin-bottom: 10px">Can't find the right job? Want companies to apply to <em>you?</em> </p>
<p style="color: #666666; font-size: 16px; font-weight: bold; margin-top: 24px; margin-bottom: 10px; text-transform: uppercase">In Brief</p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px">.</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Stephen Fluin</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #00aadd; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">news</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">Learn new skills faster, find work you love, earn what you're worth. Get it today for $0.99 (limited time).</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Simple Programmer  <span style="border: 1px solid #999; border-radius: 2px; color: #999; font-size: 11px; font-weight: normal; padding: 1px 5px 1px 5px;">Sponsor</span></span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">SitePoint</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Rob Dodson</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Jack Franklin</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Dr. Axel Rauschmayer</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">James Gillmore</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">NoSleep.js is a small Wake Lock API shim to prevent the browser and device from going to sleep.</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">David Walsh</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Gábor Soós</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Anthony Gore</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <br><span style="font-size: 13px; color: #444444; line-height: 19px">Instantly know whats broken and why. Monitoring, alerting &amp; analytics for JavaScript errors. Try it.</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">ROLLBAR  <span style="border: 1px solid #999; border-radius: 2px; color: #999; font-size: 11px; font-weight: normal; padding: 1px 5px 1px 5px;">Sponsor</span></span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #cc00cc; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">video</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Ben Lesh</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #cc00cc; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">video</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Brad Traversy</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #cc00cc; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">video</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Gordon Williams</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #bbbbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tools</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">EclipseSource</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #bbbbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tools</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">A humorous idea if normal minification isn’t your thing.</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Mechazawa</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #bbbbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tools</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">CircleCI  <span style="border: 1px solid #999; border-radius: 2px; color: #999; font-size: 11px; font-weight: normal; padding: 1px 5px 1px 5px;">Sponsor</span></span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #00bbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">code</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Burke Holland</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"></span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Kabir Shah</span></p>
</td></tr>
<tr><td bgcolor="#f4f4f4" style="font-family: verdana, helvetica, arial, sans-serif; text-align: left; padding-top: 12px; padding-left: 12px; padding-right: 12px; padding-bottom: 12px" class="noarchive">
<p style="line-height: 15px; font-size: 11px; margin-top: 0">Curated by .</p>
<p style="line-height: 15px; font-size: 11px; margin-top: 0">Like this? You may also enjoy: </p>
<p style="font-size: 13px"></p>
<p style="font-size: 11px; line-height: 15px">© Cooperpress Ltd. Fairfield Enterprise Centre, Lincoln Way, Louth, LN11 0LS, UK</p>
</td></tr>
</table>
</td></tr></table>
---------------
<h1 id="#title_1" >2、Salesforce三项新服务让CRM具备认知能力</h1>
Kent Weare
[http://www.infoq.com/cn/news/2017/07/Salesforce-Einstein?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/07/Salesforce-Einstein?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Salesforce近期在博客中公布了其爱因斯坦AI平台上的三项认知服务。这三项附加服务包括情感检测、意图检测以及目标检测。Salesforce的用户可以通过这三项服务来自动完成洞察分析，还可以在他们的CRM应用中使用预测模型。
</p> <i>By Kent Weare</i> <i> Translated by 李勇</i>
---------------
<h1 id="#title_2" >3、Rider首个发布候选版加入了性能提升特性</h1>
Jeff Martin
[http://www.infoq.com/cn/news/2017/07/rider-rc1?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/07/rider-rc1?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/news/2017/07/rider-rc1/zh/headerimage/GettyImages-93165688.jpg"/><p>Rider是JetBrains推出的一款多平台IDE产品，聚焦于.NET开发。JetBrains已经给出了Rider的首个发布候选版。该最新预览版扩展了对NuGet的支持，尤其针对Windows系统改进了通用性能，并添加了一些可用性上的改进。</p> <i>By Jeff Martin</i> <i> Translated by Rays</i>
---------------
<h1 id="#title_3" >4、从eBay购物车丢失看处理网络I/O</h1>
麦克周
[http://www.infoq.com/cn/news/2017/07/eBay-shopping-i-o?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/07/eBay-shopping-i-o?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>eBay的员工Venkatesh Ramaswamy于2017年1月发表了一篇文章，文章发表在eBay技术博客上，文章主要讲了针对购物车缓存数据丢失情况，eBay思考的三种解决方案，以及最终采用的解决方案。</p> <i>By 麦克周</i>
---------------
<h1 id="#title_4" >5、迷你书： 架构师特刊：进击的618</h1>
InfoQ中文站
[http://www.infoq.com/cn/minibooks/618-great-advance?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/minibooks/618-great-advance?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/minibooks/618-great-advance/zh/smallimage/100.jpg"/><p>每一次的电商大促，都是外行看热闹（剁手），内行看门道（技术）。在这国人购买力飞速升级的时代，每一轮爆棚流量背后，都有着那改变世界的技术作支撑。今年的 618，京东是怎么玩的？InfoQ 为你揭秘！</p> <i>By InfoQ中文站</i>
---------------
<h1 id="#title_5" >6、Web Development Reading List #190: Images in Web Notifications and Angular Code Splitting</h1>
Anselm Hannemann
[https://www.smashingmagazine.com/2017/07/web-development-reading-list-190-images-web-notifications-angular-code-splitting/](https://www.smashingmagazine.com/2017/07/web-development-reading-list-190-images-web-notifications-angular-code-splitting/)
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
</table><p>New APIs offer great possibilities to <strong>build better web services</strong>. And some people push these new technologies to their limits. For example, we can use JavaScript to generate images that we then can use in Web Notifications. We can use the Storage API to find out if and how much data we can save on a user’s device and can adjust the behavior of our applications accordingly.</p>

<figure><a href="https://www.smashingmagazine.com/2017/07/web-development-reading-list-190-images-web-notifications-angular-code-splitting/"><img
sizes="(max-width: 1600px) 100vw, 1600px"
srcset="
https://www.smashingmagazine.com/wp-content/uploads/2017/07/sustainabnle_sici9n_c_scale_w_200.png 200w,
https://www.smashingmagazine.com/wp-content/uploads/2017/07/sustainabnle_sici9n_c_scale_w_637.png 637w,
https://www.smashingmagazine.com/wp-content/uploads/2017/07/sustainabnle_sici9n_c_scale_w_940.png 940w,
https://www.smashingmagazine.com/wp-content/uploads/2017/07/sustainabnle_sici9n_c_scale_w_1199.png 1199w,
https://www.smashingmagazine.com/wp-content/uploads/2017/07/sustainabnle_sici9n_c_scale_w_1600.png 1600w"
src="https://www.smashingmagazine.com/wp-content/uploads/2017/07/sustainabnle_sici9n_c_scale_w_637.png"
alt="Designing the product for sustainability"></a></figure>

<p>And then we can push our designs further. Constant improvement and development of the navigation is what makes a service like <em>Gitlab</em> easier to use. And by giving advice to users, such as promoting <strong>more sustainable options</strong>, we can show empathy to our users while improving the world. It all starts with us pushing our projects further.</p><p>The post .</p>
---------------