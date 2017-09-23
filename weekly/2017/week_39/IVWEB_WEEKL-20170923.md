## 文章索引
1、 <a href="#1#353:-quantifying-detectable-bugs-in-js" >#353: Quantifying Detectable Bugs in JS</a><br/>
2、 <a href="#2entity-framework中的字符串插值引发担忧" >Entity Framework中的字符串插值引发担忧</a><br/>
3、 <a href="#3我们为什么要选择小众语言rust来实现tikv" >我们为什么要选择小众语言Rust来实现TiKV？</a><br/>
4、 <a href="#4kotlin与java之争" >Kotlin与Java之争</a><br/>
5、 <a href="#5亚马逊cto-werner-vogels谈ai对于企业的价值" >亚马逊CTO Werner Vogels谈AI对于企业的价值</a><br/>
6、 <a href="#6oracle将java-ee移交eclipse基金会" >Oracle将Java EE移交Eclipse基金会</a><br/>
7、 <a href="#7tensorflow-serving-10的技术细节在google-i/o大会上公布" >TensorFlow Serving 1.0的技术细节在Google I/O大会上公布</a><br/>
8、 <a href="#8视频演讲-基于移动的快速工程模式" >视频演讲： 基于移动的快速工程模式</a><br/><h1 id="#title_0" >1、#353: Quantifying Detectable Bugs in JS</h1>

[http://javascriptweekly.com/issues/353](http://javascriptweekly.com/issues/353)
<table border="0" width="100%" cellpadding="0" cellspacing="0" bgcolor="#ffffff" style="font-family: 'helvetica neue', helvetica, arial, sans-serif; font-size: 14px; line-height: 20px; color: #333"><tr><td align="center" valign="top">
<table border="0" width="600" cellpadding="0" cellspacing="0" class="container noarchive" style="border-collapse: collapse;"><tr><td style="padding-top: 6px; padding-bottom: 6px; font-size: 11px; text-align: center; color: #555; font-family: verdana, arial, sans-serif">
<span class="nomo">This week's JavaScript news</span> — 
</td></tr></table>
<table border="0" width="600" cellpadding="0" cellspacing="0" class="container" style="border-collapse: collapse">
<tr><td style="background-color: #f7df1e"><table width="100%" cellspacing="0" cellpadding="0" align="left"><tr><td align="left" class="block" style="padding: 6px 12px;">
<table align="left" width="50%" class="gowide"><tr><td><span style="line-height: 36px; font-size: 23px; color: #f7df1e; font-weight: bold; color: #323330">JavaScript Weekly</span></td></tr></table>
<table align="left" style="text-align: right" width="50%" class="gowide lonmo"><tr><td><span style="font-size: 14px; line-height: 36px; font-weight: normal; color: #323330">
Issue 353 — September 22, 2017
</span></td></tr></table>
</td></tr></table></td></tr>
<tr><td style="padding: 16px 12px 12px 12px" align="left">
<div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">A summary of an academic paper that concludes both Flow and TypeScript are good at preventing bugs that could end up in committed code.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Adrian Colyer
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">Plenty of JS terminology explained, along with code examples, in this thorough guide.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Manuel Beaudru
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">JavaScript telemetry gives a timeline of browser events leading to an error, including interaction events, like clicks, inputs, navigation and console messages + more. Debug better w/ telemetry and know why your app crashed.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
ROLLBAR
  <span style="border: 1px solid #999; border-radius: 2px; color: #999; font-size: 11px; font-weight: normal; padding: 1px 5px 1px 5px; ">Sponsor</span>
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">This new release of the controversial compile-to-JS language preserves its clean syntax but bridges the gap with ES6 and beyond.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
CoffeeScript
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">The CEO of Ionic suggests that incompatibility between component models results in framework churn and that Web Components will provide a resolution.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Max Lynch
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">An example-driven tour of the key features of ES6/ES2015, if you’re not quite there yet.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Łukasz Kyć
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">Using the new `script type=”module”` approach gives us some benefits merely beyond loading ES modules alone - it guarantees ES6/ES2015 support.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Philip Walton
</div>
<br clear="all" style="clear: both"><p style="color: #666666; font-size: 16px; font-weight: bold; margin-top: 8px; margin-bottom: 10px; text-transform: uppercase">Jobs </p>
<ul style="padding-left: 18px; margin-top: 10px; list-style-type: square">
<li style="color: #f7df1e; margin-bottom: 10px; font-size: 15px; line-height: 17px">
<span style="font-size: 12px; color: #666666">If consensus algorithms get your mental juices flowing, come join the team behind a global &amp; fault-tolerant messaging platform.</span> <span style="color: #999999; font-weight: normal; font-size: 12px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Ably realtime</span>
</li>
<li style="color: #f7df1e; margin-bottom: 10px; font-size: 15px; line-height: 17px">
<span style="font-size: 12px; color: #666666">Help us build an online grocery experience that revolutionizes how food is sourced, bought and enjoyed.</span> <span style="color: #999999; font-weight: normal; font-size: 12px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Good Eggs</span>
</li>
</ul>
<p style="color: #333; font-size: 12px; font-weight: normal; margin-top: 0px; margin-bottom: 10px">Can't find the right job? Want companies to apply to <em>you?</em> </p>
<p style="color: #666666; font-size: 16px; font-weight: bold; margin-top: 24px; margin-bottom: 10px; text-transform: uppercase">In Brief</p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #00aadd; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">news</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">It was originally due this week.</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Dor Moshe</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #00aadd; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">news</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Evan You</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">The death of fax has been greatly exaggerated! Twilio Programmable Fax allows you to send and receive fax in the cloud.</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Twilio  <span style="border: 1px solid #999; border-radius: 2px; color: #999; font-size: 11px; font-weight: normal; padding: 1px 5px 1px 5px;">Sponsor</span></span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #6ca629; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">node</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Maga D. Zandaqo</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">David Tang</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Tara Manicsic</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> 
<br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">SitePen  <span style="border: 1px solid #999; border-radius: 2px; color: #999; font-size: 11px; font-weight: normal; padding: 1px 5px 1px 5px;">Sponsor</span></span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #AF7817; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">story</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Justin Duke</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <br><span style="font-size: 13px; color: #444444; line-height: 19px">Part 5 of our Modern Application Stack series - Why ReactJS is driving the development of modern applications.</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">MONGODB  <span style="border: 1px solid #999; border-radius: 2px; color: #999; font-size: 11px; font-weight: normal; padding: 1px 5px 1px 5px;">Sponsor</span></span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"></span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Naver Corp</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #00bbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">code</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif"></span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #00bbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">code</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">Provides a neater API and error handling for the IndexedDB browser database API.</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">David Fahlander</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #00bbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">code</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Christoph Walcher</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px">.</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Andrei Kashcha</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px">.</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Jordan Eldredge</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #00bbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">code</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Andrey Sitnik</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #00bbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">code</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Jerome Etienne</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #00bbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">code</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Julien Elbaz</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #00bbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">code</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Julien Elbaz</span></p>
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
<h1 id="#title_1" >2、Entity Framework中的字符串插值引发担忧</h1>
Jonathan Allen
[http://www.infoq.com/cn/news/2017/09/EF-Core-2.0-4?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/09/EF-Core-2.0-4?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>将内插字符串自动地转化为参数化SQL语句，这是Entity Framework Core 2提供的一个新特性。虽然该特性从设计上是为了避免出现SQL语句编写上的问题，但是有人担心这会导致更多的SQL注入攻击。</p> <i>By Jonathan Allen</i> <i> Translated by 盖磊</i>
---------------
<h1 id="#title_2" >3、我们为什么要选择小众语言Rust来实现TiKV？</h1>
黄东旭
[http://www.infoq.com/cn/news/2017/09/Select-minority-language-Rust-Ti?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/09/Select-minority-language-Rust-Ti?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>编程语言很多，既然存在，就有各自存在的理由。 其实编程语言本身不难，只要学会了一种语言，其它的都是相通的。难的部分，好坏之分，是对语言的理解，记忆，熟悉，和流畅地使用每个语言提供的基础库和扩展库，也就是LIBs，或是APIs，或是SDK，或是Frameworks。 本文是 InfoQ 策划的语言专题其中的 Rust 篇。</p> <i>By 黄东旭</i>
---------------
<h1 id="#title_3" >4、Kotlin与Java之争</h1>
谢丽
[http://www.infoq.com/cn/news/2017/09/Kotlin-Java-debate?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/09/Kotlin-Java-debate?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Kotlin是一门相对比较新的JVM语言，自2011年以来，该语言在Android社区受到的关注度越来越高，Google IO 2017大会宣布，Android正式支持Kotlin。本文将尝试提供一个从Java切换到Kotlin时需要考虑的事项清单。</p> <i>By 谢丽</i>
---------------
<h1 id="#title_4" >5、亚马逊CTO Werner Vogels谈AI对于企业的价值</h1>
麦克周
[http://www.infoq.com/cn/news/2017/09/CTO-Werner-Vogels-AI?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/09/CTO-Werner-Vogels-AI?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Werner Vogels自2005年起担任Amazon的副总兼CTO，他是分布式系统领域专家，对Dynamo、AWS、云计算都有贡献。目前负责Amazon自动驾驶技术研发。在最近一次采访中，Vogels谈到了人工智能和机器学习对于企业的价值。</p> <i>By 麦克周</i>
---------------
<h1 id="#title_5" >6、Oracle将Java EE移交Eclipse基金会</h1>
Tim Hodkinson
[http://www.infoq.com/cn/news/2017/09/JavaEEtoEclipse?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/09/JavaEEtoEclipse?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Oracle宣布将由Eclipse基金会接手Java EE。这一举动受到Red Hat、 IBM和其它社区成员的欢迎。但不确定的是，在此举动之后，该平台是否还会保留其现在Java EE的名称。</p> <i>By Tim Hodkinson</i> <i> Translated by 张斌</i>
---------------
<h1 id="#title_6" >7、TensorFlow Serving 1.0的技术细节在Google I/O大会上公布</h1>
Dylan Raithel
[http://www.infoq.com/cn/news/2017/09/tensor-flow-serving-1-0?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/09/tensor-flow-serving-1-0?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>来自Google的Noah Fiedel在他的演讲中，详细地介绍了TensorFlow Serving稳定版本1.0版的新编程模型。演讲内容涉及改进可移植性、服务能力和可重生性中所面对的主要挑战。</p> <i>By Dylan Raithel</i> <i> Translated by 盖磊</i>
---------------
<h1 id="#title_7" >8、视频演讲： 基于移动的快速工程模式</h1>
许大芮
[http://www.infoq.com/cn/presentations/mobile-based-rapid-engineering-model?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/mobile-based-rapid-engineering-model?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/mobile-based-rapid-engineering-model/zh/mediumimage/xudarui270.jpg"/><p>淘宝是全球范围内用户活跃度顶尖的互联网公司，在移动兴起的浪潮中逐步探索出一套基于前端、客户端及服务端的全新研发模式，利用脚本化和动态化方式为业务快速试错提供了可能，极大的降低了平台创新和营销研发工程成本，整体 3D/VR/AR 等创新技术为快业务发展提供更加广阔的空间。本次演讲我们将分享淘宝在这方面的实践经验。</p> <i>By 许大芮</i>
---------------