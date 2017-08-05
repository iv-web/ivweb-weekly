## 文章索引
1、 <a href="#1#346:-js-oddities-v8-61-and-an-online-vs-code-ide-for-javascript" >#346: JS oddities, V8 6.1, and an online VS Code IDE for JavaScript</a><br/>
2、 <a href="#2netflix开源神经网络库针对千亿级别维度稀疏数据" >Netflix开源神经网络库，针对千亿级别维度稀疏数据</a><br/>
3、 <a href="#3ai技术兴起令谷歌及微软成为芯片制造商" >AI技术兴起令谷歌及微软成为芯片制造商</a><br/>
4、 <a href="#411m-ios-app给你的瘦身建议" >11M iOS App给你的瘦身建议</a><br/>
5、 <a href="#5netflix微服务架构中的应用程序-ddos-防护" >Netflix：微服务架构中的应用程序 DDoS 防护</a><br/>
6、 <a href="#6google使用3亿张图片大幅度改进图像识别算法" >Google使用3亿张图片大幅度改进图像识别算法</a><br/>
7、 <a href="#7amazon-cloudwatch-events新增跨账户事件传递特性" >Amazon CloudWatch Events新增跨账户事件传递特性</a><br/>
8、 <a href="#8learn-from-what-you-see:-it-all-starts-with-inspiration" >Learn From What You See: It All Starts With Inspiration</a><br/><h1 id="#title_0" >1、#346: JS oddities, V8 6.1, and an online VS Code IDE for JavaScript</h1>

[http://javascriptweekly.com/issues/346](http://javascriptweekly.com/issues/346)
<table border="0" width="100%" cellpadding="0" cellspacing="0" bgcolor="#ffffff" style="font-family: 'helvetica neue', helvetica, arial, sans-serif; font-size: 14px; line-height: 20px; color: #333"><tr><td align="center" valign="top">
<table border="0" width="600" cellpadding="0" cellspacing="0" class="container noarchive" style="border-collapse: collapse;"><tr><td style="padding-top: 6px; padding-bottom: 6px; font-size: 11px; text-align: center; color: #555; font-family: verdana, arial, sans-serif">
<span class="nomo">This week's JavaScript news</span> — 
</td></tr></table>
<table border="0" width="600" cellpadding="0" cellspacing="0" class="container" style="border-collapse: collapse">
<tr><td style="background-color: #f7df1e"><table width="100%" cellspacing="0" cellpadding="0" align="left"><tr><td align="left" class="block" style="padding: 6px 12px;">
<table align="left" width="50%" class="gowide"><tr><td><span style="line-height: 36px; font-size: 23px; color: #f7df1e; font-weight: bold; color: #323330">JavaScript Weekly</span></td></tr></table>
<table align="left" style="text-align: right" width="50%" class="gowide lonmo"><tr><td><span style="font-size: 14px; line-height: 36px; font-weight: normal; color: #323330">
Issue 346 — August  4, 2017
</span></td></tr></table>
</td></tr></table></td></tr>
<tr><td style="padding: 16px 12px 12px 12px" align="left">
<div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">Around 40 examples of ‘quirky’ JavaScript code with unexpected results or outcomes. Mostly interesting to learn about odd edge cases.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Denys Dovhan
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">Get the VS Code experience in your browser. 
</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Eric Simons
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">In beta until the release of Chrome 61, 6.1 has a smaller binary, includes some <em>significant</em> performance improvements when iterating over maps and sets, and asm.js code is now transpiled to WebAssembly.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Mathias Bynens
</div>
<br clear="all" style="clear: both"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">Multi-directional scrolling with a fixed header, paging, grouping and editing data in cells are just a few of the capabilities of the ExtReact grid. Try ExtReact for free to see how easy it is to add the grid and many other components into your apps.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Sencha, Inc
  <span style="border: 1px solid #999; border-radius: 2px; color: #999; font-size: 11px; font-weight: normal; padding: 1px 5px 1px 5px; ">Sponsor</span>
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">Nuxt.js is a framework for bringing server-side rendering (SSR) to your Vue.js apps, similar to how Next.js does with React.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Olayinka Omole
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">Adopting a more functional approach let the author stop using bits of JavaScript he didn’t like.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Joel Thoms
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">A practical introduction to  (scripts that run in the background separate from a Web page context) and how to easily create one using Ember.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Adnan Chowdhury
</div>
<br clear="all" style="clear: both"><p style="color: #666666; font-size: 16px; font-weight: bold; margin-top: 8px; margin-bottom: 10px; text-transform: uppercase">Jobs </p>
<ul style="padding-left: 18px; margin-top: 10px; list-style-type: square">
<li style="color: #f7df1e; margin-bottom: 10px; font-size: 15px; line-height: 17px">
<span style="font-size: 12px; color: #666666">Be a cornerstone in the development of an innovative project management tool using cutting edge technology, React.js.</span> <span style="color: #999999; font-weight: normal; font-size: 12px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Mosaic Manages Teamwork</span>
</li>
<li style="color: #f7df1e; margin-bottom: 10px; font-size: 15px; line-height: 17px">
<span style="font-size: 12px; color: #666666">Join us to impact how the world's biggest retailers operate by making a web app with great UX and DX using React, Redux and Glamor</span> <span style="color: #999999; font-weight: normal; font-size: 12px; text-transform: uppercase; font-family: verdana, arial, sans-serif">EDITED</span>
</li>
<li style="color: #f7df1e; margin-bottom: 10px; font-size: 15px; line-height: 17px">
.</span> <span style="color: #999999; font-weight: normal; font-size: 12px; text-transform: uppercase; font-family: verdana, arial, sans-serif">X-Team</span>
</li>
</ul>
<p style="color: #333; font-size: 12px; font-weight: normal; margin-top: 0px; margin-bottom: 10px">Can't find the right job? Want companies to apply to <em>you?</em> </p>
<p style="color: #666666; font-size: 16px; font-weight: bold; margin-top: 24px; margin-bottom: 10px; text-transform: uppercase">In Brief</p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #00aadd; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">news</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Henning Dieterichs</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #00aadd; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">news</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">To implement first-class support for WebAssembly.</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Sean T. Larkin</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #00aadd; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">news</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">Learn more about the talks and workshops at this year's Polymer Summit, and see who our amazing speakers are.</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Google, Inc.  <span style="border: 1px solid #999; border-radius: 2px; color: #999; font-size: 11px; font-weight: normal; padding: 1px 5px 1px 5px;">Sponsor</span></span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #00aadd; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">news</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Bradley Nelson</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #00aadd; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">news</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">With a new JS library that runs Google’s TensorFlow in the browser.</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">InfoWorld</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">Provides an alternative to endless null checks.</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Nicolás Bevacqua</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">Understand how <code>v-model</code> works on native inputs and custom components.</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Joseph Zimmerman</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Zell Liew</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">Get started with the beta release of MongoDB's backend-as-a-service with step-by-step tutorials and sample apps.</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">MONGODB  <span style="border: 1px solid #999; border-radius: 2px; color: #999; font-size: 11px; font-weight: normal; padding: 1px 5px 1px 5px;">Sponsor</span></span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Dr. Axel Rauschmayer</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Peter Cook</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #cc00cc; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">video</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">Poses a series of ever more challenging JavaScript riddles and brain-teasers.</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Dan Shappir</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #AF7817; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">opinion</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Vince Campanale</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #AF7817; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">story</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">CircleCI  <span style="border: 1px solid #999; border-radius: 2px; color: #999; font-size: 11px; font-weight: normal; padding: 1px 5px 1px 5px;">Sponsor</span></span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"></span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Epicmax</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #00bbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">code</span> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #6ca629; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">node</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif"></span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #00bbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">code</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Morgan Herlocker</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #00bbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">code</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Kent C. Dodds</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #00bbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">code</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Marijn Haverbeke</span></p>
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
<h1 id="#title_1" >2、Netflix开源神经网络库，针对千亿级别维度稀疏数据</h1>
Benoît Rostykus
[http://www.infoq.com/cn/news/2017/08/Netflix-open-Neural-network-libr?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/08/Netflix-open-Neural-network-libr?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Netflix，中文名“网飞”，是一家在世界多国提供网络视频点播的公司，不少人是因为热门美剧《纸牌屋》知道的这家公司。事实上，Netflix 在发展中十分重视技术的应用，尤其是近年来人工智能技术的应用，Netflix 甚至拥有自己的深度学习研究室。本文的作者就是来自 Netflix 深度学习研究室的研究员，将要向我们介绍 Netflix 开源的一款面向稀疏数据的轻量化神经网络库：Vectorflow。</p> <i>By Benoît Rostykus</i>
---------------
<h1 id="#title_2" >3、AI技术兴起令谷歌及微软成为芯片制造商</h1>
Tom Simonite Business
[http://www.infoq.com/cn/news/2017/08/AI-Google-Microsoft-chip-mak?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/08/AI-Google-Microsoft-chip-mak?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>软件厂商谷歌与微软已经投入大量资源以构建自己的芯片方案。而在双方身后，则是一大批兜售以AI为中心的自有芯片产品的初创企业——甚至也包括苹果公司。除了利用智能机器改变我们的生活之外，这场竞逐可能也会给已然成熟的芯片行业带来深远变革甚至是一轮大洗牌。</p> <i>By Tom Simonite Business</i> <i> Translated by 运和凭</i>
---------------
<h1 id="#title_3" >4、11M iOS App给你的瘦身建议</h1>
Ben Sandofsky
[http://www.infoq.com/cn/news/2017/08/11M-iOS-App-weight-loss-advice?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/08/11M-iOS-App-weight-loss-advice?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>如果聚焦于客户体验，App瘦身是很重要的工作。不同于很多大型App，一个小型的App无疑会更受用户青睐。本文给出了一些iOS App瘦身的技巧，并介绍了作者的App设计理念。</p> <i>By Ben Sandofsky</i> <i> Translated by Rays</i>
---------------
<h1 id="#title_4" >5、Netflix：微服务架构中的应用程序 DDoS 防护</h1>
Andrew Morgan
[http://www.infoq.com/cn/news/2017/08/application-ddos-microservices?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/08/application-ddos-microservices?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>日前，Netflix 发布了一篇博文，阐述了在微服务架构中缓解应用程序 DDoS 攻击的策略。该博文概要阐述了如何识别触发这种攻击的请求，如何使用开源的 Repulsive Grizzly 和 Cloud Kraken 框架进行测试，最后，还提供了保护系统的一些最佳实践。</p> <i>By Andrew Morgan</i> <i> Translated by 刘志勇</i>
---------------
<h1 id="#title_5" >6、Google使用3亿张图片大幅度改进图像识别算法</h1>
Roland Meertens
[http://www.infoq.com/cn/news/2017/08/image-recognition-big-data?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/08/image-recognition-big-data?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Google和CMU的研究员使用高达3亿张图片，在图像识别算法上取得了长足改进。</p> <i>By Roland Meertens</i> <i> Translated by Beining</i>
---------------
<h1 id="#title_6" >7、Amazon CloudWatch Events新增跨账户事件传递特性</h1>
Steffen Opel
[http://www.infoq.com/cn/news/2017/08/cloudwatch-events-cross-account?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/08/cloudwatch-events-cross-account?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>近日，Amazon Web Services（AWS）在Amazon CloudWatch Events中引入了跨账户事件传递特性，可以为跟踪组织事件、在单独的账户中处理事件实现高级安全策略等场景提供支持。</p> <i>By Steffen Opel</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_7" >8、Learn From What You See: It All Starts With Inspiration</h1>
Veerle Pieters
[https://www.smashingmagazine.com/2017/08/it-all-starts-with-inspiration/](https://www.smashingmagazine.com/2017/08/it-all-starts-with-inspiration/)
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
</table><p>The world around us is full of little things and experiences that shape us, our way of thinking, but also how we tackle our work. Influenced by these encounters, <strong>every designer develops their unique style and workflow</strong>, and studying their artwork — the compositions, geometry of lines and shapes, light and shadows, the  — can all inspire us to look beyond our own horizon and try something new.</p>

<figure></figure>

<p>It doesn't really take much to let your mind wander. Always remember to take a closer look at things around you; you'll be sure to .</p>
---------------