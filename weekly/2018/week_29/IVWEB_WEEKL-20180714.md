## 文章索引
1、 <a href="#1monthly-web-development-update-7/2018:-practical-accessibility-design-mistakes-and-feature-control" >Monthly Web Development Update 7/2018: Practical Accessibility, Design Mistakes, And Feature Control</a><br/>
2、 <a href="#2文章-运满满如何将机器学习应用于车货匹配和公路干线价格预测" >文章： 运满满如何将机器学习应用于车货匹配和公路干线价格预测？</a><br/>
3、 <a href="#3linkedout-失败注入测试框架" >“LinkedOut” 失败注入测试框架</a><br/>
4、 <a href="#4github工程师为mysql高可用性采用了新架构" >Github工程师为MySQL高可用性采用了新架构</a><br/>
5、 <a href="#5android模拟器windows版现在支持amd硬件加速和hyper-v了" >Android模拟器Windows版现在支持AMD硬件加速和Hyper-V了</a><br/>
6、 <a href="#6apache发布groovy-25正式版及30预览版" >Apache发布Groovy 2.5正式版及3.0预览版</a><br/>
7、 <a href="#7文章-我们画了些图并用通俗的语言来解释天才程序员设计的以太坊" >文章： 我们画了些图，并用通俗的语言，来解释天才程序员设计的以太坊</a><br/>
8、 <a href="#8typescript-3-rc-and-an-npm-incident-to-be-aware-of" >TypeScript 3 RC and an npm incident to be aware of</a><br/>
9、 <a href="#9每周分享第-13-期" >每周分享第 13 期</a><br/><h1 id="#title_0" >1、Monthly Web Development Update 7/2018: Practical Accessibility, Design Mistakes, And Feature Control</h1>
Anselm Hannemann
[https://www.smashingmagazine.com/2018/07/monthly-web-development-update-7-2018/](https://www.smashingmagazine.com/2018/07/monthly-web-development-update-7-2018/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/07/monthly-web-development-update-7-2018/" />
              <title>Monthly Web Development Update 7/2018: Practical Accessibility, Design Mistakes, And Feature Control</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>Monthly Web Development Update 7/2018: Practical Accessibility, Design Mistakes, And Feature Control</h1>
                  
                    
                    <address>Anselm Hannemann</address>
                  
                  <time datetime="2018-07-13T14:20:17&#43;02:00" class="op-published">2018-07-13T14:20:17+02:00</time>
                  <time datetime="2018-07-13T12:33:42&#43;00:00" class="op-modified">2018-07-13T12:33:42+00:00</time>
                </header>
                <p>The web continues to amaze me. With all its variety and different changes to the platform, it’s hard to see a straight pattern &mdash; if there even is (just) one. But it’s wonderful to see what is being changed, which features are added to the platform, which ones get deprecated, and how browsers implement more and more technology to protect the user from malicious website attacks. It’s interesting to see that these security features nowadays are getting as much attention as a feature for developers; this shows <strong>the importance of privacy and security</strong> and how unstable and insecure the web was in the past. </p>

<p>But the best thing about all of this is that it shows how important it is to stick to the things that people give us. Instead of implementing our own solutions for everything, it’s often much better to re-use an existing system. Not only is it safer to rely on, but also less work while more inclusive to extend a native DOM element with a custom element (instead of writing our own custom element from scratch). If we think about whether we should build our own version of SSL or use an existing software for this, why would we build a clickable element based on nothing instead of altering the behavior of an <code>a</code> or <code>button</code> element? And why would we check for resource host validation on our own, if the browser already gives us an API for that? This week’s articles are all dedicated to these topics.</p>

<p>Another thing that has been stuck in my head is Andrea Giammarchi’s article, “,” in which he describes how we blindly use Babel as developers when we write JavaScript to be able to write modern ECMAScript. But we usually don’t realize that transpiling all of our modern code in modern browsers isn’t the most efficient way. I’m glad that Andrea offers some ideas on how we can improve that situation and improve our web apps’ performance. Wouldn’t it be amazing to just serve a third of the bundle size by not transpiling the code anymore for each and every browser?</p>

<h3>News</h3>

<ul>
<li>Site Isolation effectively makes it harder for untrusted websites to access or steal information from your accounts on other websites.  and Cross-Origin Read Blocking (CORB) will no longer load, e.g. a JSON file as image. But even further, these changes mean that full-page layout is no longer guaranteed to be synchronous. This new feature affects you if you read out calculated sizes from an element in JavaScript or use <code>unload</code> event listeners.  Ensure that you know about this and check if your sites still work as expected.</li>
<li>By now, we know a bit about Content Security Policies — a feature that lets developers limit the load of certain resources by hostnames. But browser vendors have come up with something new now: Feature Policy. This allows web developers to selectively enable, disable, or modify the behavior of certain APIs and web features in the browser. It’s like CSP but instead of controlling security, it controls features and  explaining everything.</li>
<li>The Brave browser team shows their latest feature to protect their users’ privacy: .</li>
</ul>



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




<h3>Generic</h3>

<ul>
<li>Anton Sten asks if  Analyzing the marketing strategies by Apple, Microsoft, Google, Amazon but also small other companies and how we can do really purposeful work and stick to our values instead of treating them as marketing-material that we don’t need to respect or stick to.</li>
<li>Now that the technology sector of the world is rapidly transforming all of the world’s things into digital things, many have called for more ethics in our field. That is in many instances quite a vague goal, so let’s apply it to one part of digital: front-end development. ? Hidde de Vries wrote an article about that.</li>
</ul>

<h3>Security</h3>

<ul>
<li>Ticketmaster’s customer data has been compromised and as it seems, .</li>
</ul>

<h3>UI/UX</h3>

<ul>
<li>Eugen Eşanu shows  and what we can do instead to make our design more user-friendly.</li>
</ul>











<figure >
	<a href="https://uxplanet.org/10-small-design-mistakes-we-still-make-1cd5f60bc708">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b9c093b8-ed81-46f8-8dfc-758c3a591bb1/what-we-design.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b9c093b8-ed81-46f8-8dfc-758c3a591bb1/what-we-design.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b9c093b8-ed81-46f8-8dfc-758c3a591bb1/what-we-design.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b9c093b8-ed81-46f8-8dfc-758c3a591bb1/what-we-design.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b9c093b8-ed81-46f8-8dfc-758c3a591bb1/what-we-design.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b9c093b8-ed81-46f8-8dfc-758c3a591bb1/what-we-design.png"
			sizes="100vw"
			alt="what we design vs. what a user needs"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Users do not have time to read more than necessary, and yet designers still tend to put a lot of text because they think people need to know that. ()
		</figcaption>
	
</figure>


<h3>Privacy</h3>

<ul>
<li>This is an interesting report about  when they grant permission during app authorization. The issue with that is that there is no way to easily prevent that and it might have quite some impact if you use Gmail for your company as it might affect privacy policies and is under subject of GDPR.</li>
</ul>

<h3>Web Performance</h3>

<ul>
<li>Max Böck on how we can build  using the Network Information API. And despite it’s currently only available in Chrome and Samsung Internet browsers, it’s worth trying it out and maybe already serve it to these users.</li>
<li>From time to time, we can still read articles mentioning the importance of optimizing CSS selectors in order to improve performance. This originates in research done several years ago but Ivan Čurić researched this again .</li>
</ul>

<h3>Accessibility</h3>

<ul>
<li>Microsoft’s developer team shares a , including how to optimize presentations or language for inclusion or how to build a proper “skip navigation” functionality on your website.</li>
<li>Sara Novak shares how she managed to show empathy by  to understand how other people experience the world differently.</li>
<li>The Developer Tools of Firefox now have an <em>Accessibility Inspector</em> mode. .</li>
</ul>











<figure >
	<a href="https://blog.prototypr.io/going-colorblind-an-experiment-in-empathy-and-accessibility-98b7003737ca">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c524a3a0-3a7a-49ef-81b5-5219a7b37b9e/form-with-color-based-indicators.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c524a3a0-3a7a-49ef-81b5-5219a7b37b9e/form-with-color-based-indicators.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c524a3a0-3a7a-49ef-81b5-5219a7b37b9e/form-with-color-based-indicators.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c524a3a0-3a7a-49ef-81b5-5219a7b37b9e/form-with-color-based-indicators.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c524a3a0-3a7a-49ef-81b5-5219a7b37b9e/form-with-color-based-indicators.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c524a3a0-3a7a-49ef-81b5-5219a7b37b9e/form-with-color-based-indicators.jpg"
			sizes="100vw"
			alt="A form with color-based indicators"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			In her article, Sara Novak explains why it's important not to rely on color alone as an indicator. Symbols and error message can be much more helpful to users. (The image above shows a form with color-based indicators. Left: How a person with normal vision sees a form with color-based indicators. Right: How a deuteranomalous person sees the same form.) ()
		</figcaption>
	
</figure>


<h3>JavaScript</h3>

<ul>
<li>Leon Revill show us how we can , but that’s a different story.</li>
<li>Gerardo Rodriguez shows how we can easily fail to optimize websites for performance with Service Workers and the Fetch API and how this can result in a quota exception in browsers. Luckily, he found out the reason of this and by setting the proper CORS headers, Gerardo finally  and tells us how to avoid the issues.</li>
<li>Filepond is a nice open-source JavaScript file uploader. Rik Schennink .</li>
<li>Andrea Giammarchi about . Instead, we should think about how to serve different bundles depending on the browser support to decrease the bundle size and improve performance.</li>
<li>Justin Fuller shares  that will help us write code that is easier to understand, such as operational chaining, nullish coalescing, or the pipeline operator.</li>
<li>Addy Osmani and Mathias Bynens wrote a primer introduction on .</li>
</ul>

<div class="sponsors__wide-place"></div>




<h3>CSS</h3>

<ul>
<li>An article series that covers how we can .</li>
<li>CSS Grid is nice, but I often hear that people can’t use it because IE11 doesn’t support it well. But that’s not exactly true as IE11 has a prior version of CSS Grid available that we can easily transpile with autoprefixer. Daniel Tonon explains the .</li>
<li>For many people, CSS Grid is still very new, and it’s very capable and helps us solve a lot of problems when creating grid-based layouts in CSS. But in the current version, there are a couple of things that are still not possible.  and Rachel Andrew explains what you need that for.</li>
<li>Is CSS-in-JS good? Is it just bad? Why we constantly fall into the trap of arguing when there are no clear winners and  by acknowledging evolution and seeing things in context.</li>
</ul>

<h3>Work & Life</h3>

<ul>
<li>Why . Some thoughts that came into my mind when reading another article and it seems many people like the idea behind this.</li>
<li> and why he thinks it’s important to only choose clients that you can ethically support. But this also shows how difficult this can be sometimes, as recent discussions about Microsoft’s business cooperations with legal entities show.</li>
</ul>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(il)</span>
</div>


              </article>
            </body>
          </html>
---------------
<h1 id="#title_1" >2、文章： 运满满如何将机器学习应用于车货匹配和公路干线价格预测？</h1>
罗竞佳
[http://www.infoq.com/cn/articles/ml-dl-highway-price?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/ml-dl-highway-price?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/ml-dl-highway-price/zh/smallimage/01-1531443906805.jpg"/><p>作为全国最大的公路物流平台，运满满如何在国内庞大的物流市场，应对不同空间和时间的需求？</p> <i>By 罗竞佳</i>
---------------
<h1 id="#title_2" >3、“LinkedOut” 失败注入测试框架</h1>
Daniel Bryant
[http://www.infoq.com/cn/news/2018/07/linkedout-failure-injection?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/linkedout-failure-injection?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>领英工程团队最近更详细地讨论了他们的“LinkedOut”失败注入测试框架。该框架支持围绕应用程序和服务弹性的假设生成数据，并允许通过linkin LiX a/B测试框架或通过cookie中的数据向特定请求注入失败。可以测试的失败场景包括错误、延迟和超时。</p> <i>By Daniel Bryant</i> <i> Translated by 冬雨</i>
---------------
<h1 id="#title_3" >4、Github工程师为MySQL高可用性采用了新架构</h1>
Hrishikesh Barua
[http://www.infoq.com/cn/news/2018/07/github-mysql-high-availability?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/github-mysql-high-availability?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Github.com使用MySQL作为其许多关键服务的主干，如对外API，身份验证和Github.com网站本身。 Github的工程师团队用基于Orchestrator，Consul和Github负载均衡器的设置替换了之前基于DNS和VIP的设置以脑裂和DNS缓存问题。</p> <i>By Hrishikesh Barua</i> <i> Translated by Daniel_Hu</i>
---------------
<h1 id="#title_4" >5、Android模拟器Windows版现在支持AMD硬件加速和Hyper-V了</h1>
Sergio De Simone
[http://www.infoq.com/cn/news/2018/07/android-emulator-amd-hyperv?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/android-emulator-amd-hyperv?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>为了提升在AMD处理器或微软Hyper-V虚拟机上运行时的速度，最新发布的Windows Android模拟器支持以前仅在Intel处理器上才提供的硬件加速增强了。</p> <i>By Sergio De Simone</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_5" >6、Apache发布Groovy 2.5正式版及3.0预览版</h1>
Michael Redlich
[http://www.infoq.com/cn/news/2018/07/apache-releases-groovy-2.5?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/apache-releases-groovy-2.5?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Apache最近发布了Groovy 2.5，对AST转换进行了改进并引入了对宏的支持。Groovy 3.0的开发工作也正在顺利进行中，发布候选项计划于2018年底完成。来自OCI的首席软件工程师兼Groovy提交者Paul King博士向InfoQ介绍了最新版本和即将发布的3.0版本。</p> <i>By Michael Redlich</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_6" >7、文章： 我们画了些图，并用通俗的语言，来解释天才程序员设计的以太坊</h1>
Preethi Kasireddy
[http://www.infoq.com/cn/articles/how-does-ethereum-work-anyway?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/how-does-ethereum-work-anyway?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/how-does-ethereum-work-anyway/zh/smallimage/logo-cloud (2)-1531328527016.jpeg"/><p>我想，只要不是与世隔绝，哪怕只是偶尔看看新闻报道，你就应该听说过区块链、以太坊这些诡异的名词。不过如果没有深入研读过相关介绍，看到这些名词时，怎么都会觉得一头雾水吧。那么，以太坊究竟是什么？</p> <i>By Preethi Kasireddy</i> <i> Translated by 海兴</i>
---------------
<h1 id="#title_7" >8、TypeScript 3 RC and an npm incident to be aware of</h1>

[https://javascriptweekly.com/issues/394](https://javascriptweekly.com/issues/394)
<table border=0 align="center" border="0">
  <tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   ">

  <div>    
    <table border=0 border=0><tr>
<td align="left" style="padding-left: 4px; font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   "><p>#394 — July 13, 2018</p></td>
<td align="right" style="padding-right: 4px; font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   "><p></p></td>
</tr></table>
    
    <table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0 12px;  "><p>JavaScript Weekly</p></td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   ">
  
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></p>
  <p>NHN Entertainment </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"> may also be a good idea.</p>
  <p>The npm Blog </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;">.</em></p>
  <p>Frontend Masters <span style="text-transform: uppercase; padding: 1px 4px;  margin-left: 4px; font-size: 0.9em;   color: #997 !important;">sponsor</span></p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Project references allow TypeScript projects to depend on other TypeScript projects in a way that helps the build tools. Rest parameters can also be inferred as tuple types to make using them easier. There’s also a new <code>unknown</code> type to investigate.</p>
  <p>Daniel Rosenwasser (Microsoft) </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — An interesting proof of concept that takes you away from writing lots of <code>then</code> or <code>await</code> calls. Instead you could write something like <code>value = await proxymise(foo).a().b().c;</code></p>
  <p>Ilya Kozhevnikov </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></p>
  <p>Colin van Eenige </p>
</td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0;  "><p>💻 Jobs</p></td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — We empower video creators to tell exceptional stories and to connect with their audiences &amp; communities. Build the future with us.</p>
  <p>Vimeo </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Vettery matches top tech talent with fast-growing companies. Create your profile to get started.</p>
  <p>Vettery </p>
</td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0;  "><p>📘 Tutorials and Opinions</p></td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Based around a simple counter example.</p>
  <p>Angelos Chalaris </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — There's also a video, if you prefer.</p>
  <p>Tyler McGinnis </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;">▶  </span> — Avoid poor app performance and unnatural UX. Free and open source cross-platform mobile framework.</p>
  <p>NativeScript <span style="text-transform: uppercase; padding: 1px 4px;  margin-left: 4px; font-size: 0.9em;   color: #997 !important;">sponsor</span></p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Oliver Flaggl </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Fatih Kadir Akın </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Uses Auth0 for the authentication.</p>
  <p>Prosper Otemuyiwa </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — You may use it every day, but have you seen what happens after Babel transpiles JSX?</p>
  <p>Kent C. Dodds </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Michael Poirier-Ginter </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;">▶  </span> — An official introduction to using TensorFlow.js for machine learning in the browser.</p>
  <p>Laurence Moroney </p>
</td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0;  "><p>🔧 Code and Tools</p></td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — With summaries and, importantly, live interactive JSFiddle demos for most.</p>
  <p>Anton Shaleynikov </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Fatih Kadir Akın </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Try smart code completion, refactorings, &amp; integrated tools on your React, Angular &amp; Vue projects.</p>
  <p>JetBrains <span style="text-transform: uppercase; padding: 1px 4px;  margin-left: 4px; font-size: 0.9em;   color: #997 !important;">sponsor</span></p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></p>
  <p>Francisco Hodge </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Inspired by Redux and the Elm architecture.</p>
  <p>Reclare </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"> tool.</p>
  <p>Miloš Sutanovac </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>DigitalOcean <span style="text-transform: uppercase; padding: 1px 4px;  margin-left: 4px; font-size: 0.9em;   color: #997 !important;">sponsor</span></p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Including Styletron, Emotion and Styled Components.</p>
  <p>Jonathan Saring </p>
</td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px;  ">
<table border=0 border=0><tr><td style=" font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   "></td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  "><div style="line-height: 1.3em; font-size: 1.4em; color: #555555;">😄 Some Bonus “They're Not JS But You'll Like 'Em” Links</div></td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></p>
  <p>Linda_pp </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></p>
  <p>Khan Academy Engineering </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — If terms like 'load balancer', 'caching', or CDN are gibberish to you, you might appreciate this simple explanation.</p>
  <p>Jonathan Fulton </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"> to try it for yourself.</p>
  <p>Martijn Cuppens on Twitter </p>
</td></tr></table>
</td></tr></table>
<table border=0 border=0><tr><td style=" font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   "></td></tr></table>
</div>

  </td></tr>
</table>





<img src="https://javascriptweekly.com/open/394/rss" width="1" height="1" />
---------------
<h1 id="#title_8" >9、每周分享第 13 期</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2018/07/weekly-issue-13.html](http://www.ruanyifeng.com/blog/2018/07/weekly-issue-13.html)
<p>这里记录过去一周，我看到的值得分享的东西，每周五发布。</p>

        <p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018071301.jpg" alt="" title="" /></p>

<p>（题图：武林门码头，杭州，2017）</p>

<p>自从我，未来二三十年，人类社会将有天翻地覆的大变。我的所有时间，就都投在技术领域了。因为变化是技术引起的，只有了解技术，才可能应对变化。</p>

<p>我相信，未来最大的那些机会，一定是技术带来的机会。底层的年轻人要想翻身，当工程师是比较可能的途径。当然，医生和律师依然可以赚钱，但我觉得前景不如工程师，因为将来一定是机器帮你看病，帮你打官司。</p>

<p>这个《每周分享》系列只谈技术的原因就在这里，因为其他东西没有那么重要。</p>

<h2>新闻</h2>

<p>1、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018071302.jpg" alt="" title="" /></p>

<p>Intel 宣布与 CEO 解除合同，表面理由是他与女员工谈恋爱。但背后原因是这十年来，Intel 的新产品乏善可陈，PC 端止步不前，移动端完全败北，新兴的 AI 计算市场输给了 Nvidia。</p>

<p>2、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018071303.jpg" alt="" title="" /></p>

<p>由于日本人口不断萎缩，劳动力短缺，就业率变得极高。2018年5月，就业人数达到6698万人，是1953年以来的新高。应届大学生的就业率，达到前所未有的98%，进入了大学毕业生几乎人人都能找到工作的"完全就业"时代，学生对企业的招聘会也失去参加热情。另外，女性就业和65岁以上的老人就业也增加非常多。</p>

<p>由于工作太容易找，日本人强调的对企业的忠诚和终身就业都在减少，员工入职后很快就辞职的现象不断增加，企业如何挽留人才成为重要课题。　</p>

<p>另一个相关的新闻是，6月15日，日本政府在2025年以前引进50万外籍劳工，但只限于五个领域：农业、社会护理业、建筑业、酒店业和造船业。估计以后会不断放宽外国人就业，作为日本的主要邻国，中国青年去日本就业必将越来越多。</p>

<p>3、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018071304.jpg" alt="" title="" /></p>

<p>著名的照片网站 500px 宣布，不再允许用户发布照片时，使用创意共享许可证。也就是说，它上面的照片默认无法再免费使用了，必须单独联系作者，获得授权。值得一提的是，该网站不久前刚被北京的视觉中国集团收购。</p>

<p>目前，已经有人声称，将在三天内将该网站原有的共享照片，全部下载下来，大小大约是3TB。</p>

<p>4、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018071305.jpg" alt="" title="" /></p>

<p>意大利历史小说《玫瑰之名》，讲述了一个恐怖故事。中世纪时，有人为了防止异端邪说传播，为某些书籍涂上了毒药，由于那时的僧侣有沾唾液翻书的习惯，读久了就会中毒身亡。</p>

<p>南丹麦大学对图书馆的古书进行 X 光分析，发现真有三本这样的古书，页面涂上了砷，不知道曾经毒死了多少人。</p>

<p>5、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018071306.jpg" alt="" title="" /></p>

<p>Linux 发行版 OpenSUSE 的母公司被收购了，价格是25亿美元。 这家公司所有产品全部开源，只对服务收费，所以不要再认为开源赚不了钱。</p>

<p>6、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018071307.jpg" alt="" title="" /></p>

<p>英国一项研究发现，儿童每天读书时间越长，患上近视的可能性越高。我国城市学生的近视发病率达到90%，十个孩子里面有九个是近视，这说明中国的教育方式有问题，孩子读书时间过长是近视人口超多的主要原因。</p>

<p>7、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018071308.jpg" alt="" title="" /></p>

<p>Python 语言的创始人和最高决策者 Guido van Rossum，由于他主导的提案 PEP572 被社区反对，今天宣布非常疲倦，将不再执行最高决策者的角色。 但是，他没说接下来怎么决策，只说以后你们自己讨论决定。</p>

<p>8、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018071309.jpg" alt="" title="" /></p>

<p>6月底，有人拿到 Linux 发行版 Gentoo 的 GitHub 管理员权限，然后把密码改了，其他管理员都删了，在应用程序的源码里面加入 rm -rf 。虽然，GitHub 官方已经处理这件事情，但是看了也是一身冷汗。万一真的以 root 权限运行，莫名其妙你的系统就全没了。</p>

<p>9、</p>

<p>据统计，今年二季度，中国的创业公司获得的风险投资高于美国。主要原因是，6月份蚂蚁金服完成了C轮融资，获得了140亿美元，是有史以来最大的风险投资。</p>

<p>另外，二季度中国的风险投资笔数是去年同期的395%。这说明，中国已经成为世界上最容易获得风险投资的地方。</p>

<h2>教程</h2>

<p>1、（英文）</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018071310.jpg" alt="" title="" /></p>

<p>现在的跨平台App开发工具分成两类：（1）容器包了Web View，App实际是一个本地网站；（2）原生控件的跨平台抽象。Flutter走了不一样的路：自己开发了一套原生控件，每个平台实现一遍，然后把渲染引擎（这套控件）打包在每个应用里面，因此性能没有问题，平台差异也很小。</p>

<p>2、（英文）</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018071311.jpg" alt="" title="" /></p>

<p>众所周知，Python 是动态类型语言，运行时不需要指定变量类型。这一点是不会改变的，但是2015年9月创始人 Guido van Rossum 在 Python 3.5 引入了一个类型系统，允许开发者指定变量类型。它的主要作用是方便开发，供IDE 和各种开发工具使用，对代码运行不产生影响，运行时会过滤类型信息。</p>

<p>本文回顾了 Python 类型系统的现状，对它的优缺点进行了评价。</p>

<p>3、</p>

<p>原因是1752年英格兰进行了日历改革，由于日历算法的差异，导致丢失了9月3日到9月13日的一共12天。为了避免计算天数的误差，SQL Server 就索性把最小日期定为1753年1月1日，更大的日期范围由 datetime2 类型提供。</p>

<p>4、（中文）</p>

<p>集成开发环境（IDE）作为文件结构、代码编写、代码维护、测试和排错工具于一体的应用程序，对程序员们非常有价值。这个教程展示如何用 Unix 命令行工具完成 IDE 的功能。</p>

<p>5、（英文）</p>

<p>Go 1.11 将支持 Web Assembly，作者尝试用 Go 写了一个 TodoMVC。他的结论是："WebAssembly是 Web 开发的未来。两年后，Go、Swift、Rust 将占到前端代码的三分之一。</p>

<p>这里还有一篇，展示了两个用 Go 语言写的 WebAssebmly demo。</p>

<p>6、（英文）</p>

<p>本地开发时，我们常常使用 localhost 访问本地服务，怎样才能生成证书，让 localhost 提供 https 服务呢？</p>

<p>7、（英文）</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018071312.jpg" alt="" title="" /></p>

<p>Unicode 字符用作 CSS 背景，可以产生一些非常独特的背景。此文还有。</p>

<p>8、（英文）</p>

<p>一篇很有意思的文章，讨论如果不使用 if ... else 语句，应该怎么写代码。他的意思是，某些情况下 if 属于误用，会造成代码冗余或不利于阅读，这时应该减少 if 的使用。</p>

<p>9、（中文）</p>

<p>4月8日，清明节后第一个工作日，腾讯云一个重要的棋牌游戏客户突然遭受大流量 DDoS 攻击，棋牌类游戏遭受攻击习以为常，但是本轮攻击流量峰值竟达到了1.23Tbps，刷新国内DDoS攻击最大流量记录。</p>

<h2>工具</h2>

<p>1、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018071313.jpg" alt="" title="" /></p>

<p>Skia 是一个由C++编写的开源图形库，能在低端设备如手机上呈现高品质的2D图形。截至2017年，它已被应用于 Mozilla Firefox、Google Chrome、Chrome OS、Sublime Text、Android、Flutter 框架，作为底层图形库。</p>

<p>2、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018071329.jpg" alt="" title="" /></p>

<p>这个网站收集各种时钟的代码。</p>

<p>3、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018071314.jpg" alt="" title="" /></p>

<p>这是一个 Chrome 浏览器的插件，可以让任何网站变成"夜晚模式"。</p>

<p>4、</p>

<p>你需要录制命令行操作吗？一般的做法是录制成视频，这个工具让你可以录制成 SVG 动画。</p>

<p>5、</p>

<p>Atlassian 公司推出的 React 拖放操作的库。</p>

<p>6、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018071315.jpg" alt="" title="" /></p>

<p>今年的最有创意发明：自制的"拍立得"照相机，拍出来的不是照片，而是卡通图片！它的内部是摄像头+树莓派+热敏打印机。获得照片以后，自动调用谷歌的服务，处理成卡通图片，然后打印出来。</p>

<p>7、</p>

<p>在线的混淆器工具（obfuscator），将 C/C++ 改成混淆难懂的代码。</p>

<p>8、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018071316.jpg" alt="" title="" /></p>

<p>有人把 Vim 编译成了 WebAssembly，从而可以在浏览器里面使用 Vim 了。网友开玩笑，这样使用 Vim，就不会不知道如何退出了，只要点击浏览器 Tab 页右上角的 x 即可。</p>

<p>9、</p>

<p>谷歌开源的 Java 应用容器生成工具，不用写 Dockerfile，构造过程中自动生成一个 Docker 容器。</p>

<h2>资源</h2>

<p>1、</p>

<p>收集各种 Bash 常用操作的仓库，比如分割字符串、倒转数组等等。</p>

<p>2、</p>

<p>唯品会的 Java 编程规范。</p>

<p>3、</p>

<p>网上有很多免费资源，这份书单是学习大数据的指南。</p>

<h2>文摘</h2>

<p>1、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018071317.jpg" alt="" title="" /></p>

<p>我在15年前，一个人攀登上了富士山顶。日本有一个说法，说"一个人如果一辈子不登一次富士山顶，是混蛋。如果登第二次，也是混蛋。"这句话是说，不登一次富士山顶，是一生的遗憾。如果登二次，那一定是脑子进水了，因为登山的过程实在太艰辛。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018071318.jpg" alt="" title="" /></p>

<p>富士山有多高，标准的高度是3775米。因为它频临太平洋，所以攀登富士山是从海拔1米开始攀登的。古代的时候，人们从山脚下开始攀登，到山顶，一般需要2天2夜的时间。现在大家开始偷懒，因为汽车可以开到半山腰的五合目。所以，攀登富士山顶，变成了从半山腰开始。半山腰的海拔高度，是在2000米左右。</p>

<p>......</p>

<p>经过一天的时间，我终于爬到了山顶，吃惊地发现，那里居然有一家小商店。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018071319.jpg" alt="" title="" /></p>

<p>更吃惊的是，旁边有一个自动售货机。一瓶矿泉水，山下是130日元，到了山顶就是500日元。我都不知道，这个机器、这些饮料是怎么搬运到山顶上来的。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018071320.jpg" alt="" title="" /></p>

<p>下山途中，发现了往山顶搬运货物的登山车，这才明白货物是怎么搬到山顶的。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018071321.jpg" alt="" title="" /></p>

<p>2、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018071322.jpg" alt="" title="" /></p>

<p>亚马逊的 CTO 透露，他们采用"向后工作法"，开发一项产品采用下面的顺序。</p>

<blockquote>
  <p>1、写新闻稿 <br />
2、写 FAQ <br />
3、写用户文档 <br />
4、写代码</p>
</blockquote>

<h2>新奇</h2>

<p>1、</p>

<p>国王对一个犯人说，下周一到周五的某一天，你会被绞死，但我不告诉你到底是哪一天，到时你肯定大吃一惊。</p>

<p>犯人分析后，认为自己不会死。首先不会在周五死，因为周四晚上能推断出次日的绞刑，所以不会大吃一惊。如果已知周五不会执行死刑，那么同理也可以推断出不会在周四死。以此类推，哪一天都不会死。</p>

<p>犯人因此觉得不用担心。但是就在星期三中午，士兵进来把他押到刑场执行死刑。犯人因此大吃一惊："我明明不应该在今天死啊！"由于他认定自己不会死，所以实际上他任何一天都可能死，因为到时肯定大吃一惊。</p>

<p>2、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018071323.jpg" alt="" title="" /></p>

<p>Excel 不仅可以用来制作表格，还可以生成图形和动画。这个网站就收集各种奇特的 Excel 用法。</p>

<p>3、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018071324.jpg" alt="" title="" /></p>

<p>Google Reader 是谷歌的线上 RSS 阅读器，2013年关闭。现在，有人复制了一个一模一样的，让大家体验一下当年的感觉。</p>

<h2>本周图片</h2>

<p>1、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018071325.jpg" alt="" title="" /></p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018071326.jpg" alt="" title="" /></p>

<p>冰坑（Yakhchal）是古代波斯人储藏冰块的仓库，很多都保留了下来。地面的尖顶高达18米，地下的仓库有5000立方米。波斯人冬天把冰块放进去，夏天再拿出来用。沙漠地区能把冰块保存到夏天，是很了不起的。更了不起的是，最早的冰坑建于公元前400年。</p>

<p>2、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018071327.jpg" alt="" title="" /></p>

<p>世界最小的沙漠是加拿大育空地区的 Carcross 沙漠，只有600米宽，几公里长。奇特的是，当地不缺水，植被也比较多。这个沙漠原来是一个湖泊，后来湖泊干涸了，湖底的淤泥就变成了沙漠。</p>

<p>3、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018071328.jpg" alt="" title="" /></p>

<p>这个网站研究哪些面孔会使得面部识别技术失败。</p>

<h2>本周金句</h2>

<p>1、</p>

<p>如果一件事情是手工完成，而不是机器自动化完成，那就是一个 bug。（）</p>

<p>2、</p>

<p>海航集团创始人王健，曾经给员工讲过一堂课，内容是"死去吧"，经南方周末报道后广为流传。课程的中心内容很简单：管我要钱的时候我就让你们"死去吧"。</p>

<p>"不要天天老盯着财务公司那点钱，要看到外面广阔的天地，纽约有上万亿美元，伦敦交易所、香港交易所有那么多钱。给你们发工资，你们永远成不了百万富翁，你们要去拿投资人的钱。"（）</p>

<h2>欢迎订阅</h2>

<p>这个专栏每周五发布，同步更新在我的。</p>

<p>微信搜索"<strong>阮一峰的网络日志</strong>"或者扫描二维码，即可订阅。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2018/bg2018042311.jpg" alt="image | left" title="" /></p>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2018-07-13T12:53:26+08:00">2018年7月13日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>文集：</li>
<li>社交媒体：</li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------