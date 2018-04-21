## 文章索引
1、 <a href="#1webpack-46-hyper-2-and-designing-large-js-applications" >webpack 4.6, Hyper 2, and designing large JS applications</a><br/>
2、 <a href="#2what-you-need-to-know-to-increase-mobile-checkout-conversions" >What You Need To Know To Increase Mobile Checkout Conversions</a><br/>
3、 <a href="#3视频演讲-ucloud-开放-api-体系下的高可用和灰度发布实践" >视频演讲： UCloud 开放 API 体系下的高可用和灰度发布实践</a><br/>
4、 <a href="#4美丽联合集团赵成要让员工看到自己的未来" >美丽联合集团赵成：要让员工看到自己的未来</a><br/>
5、 <a href="#5明略数据杨威公安行业-ai-应用离成熟还有一段距离" >明略数据杨威：公安行业 AI 应用离成熟还有一段距离</a><br/>
6、 <a href="#6tgo-鲲鹏会全球战略开启硅谷分会即将成立" >TGO 鲲鹏会全球战略开启，硅谷分会即将成立</a><br/>
7、 <a href="#7空中金融-cto-朱晔公司初创阶段-cto-需要做什么上篇" >空中金融 CTO 朱晔：公司初创阶段 CTO 需要做什么？（上篇）</a><br/>
8、 <a href="#8微软正在借助区块链技术管理数字化标识" >微软正在借助区块链技术管理数字化标识</a><br/>
9、 <a href="#9迷你书-中国顶尖技术团队访谈录·第十一季" >迷你书： 中国顶尖技术团队访谈录·第十一季</a><br/><h1 id="#title_0" >1、webpack 4.6, Hyper 2, and designing large JS applications</h1>

[https://javascriptweekly.com/issues/382](https://javascriptweekly.com/issues/382)
<table border=0 align="center" border="0">
  <tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   ">

  <div>    
    <table border=0 border=0><tr>
<td align="left" style="padding-left: 4px; font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   "><p>#382 — April 20, 2018</p></td>
<td align="right" style="padding-right: 4px; font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   "><p></p></td>
</tr></table>
    
    <table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0 12px;  "><p>JS Weekly</p></td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;">.</p>
  <p>Malte Ubl </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Enjoy the dev experience of using Vue and webpack, use Vue components in Markdown, and develop custom themes with Vue.</p>
  <p>Evan You </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></p>
  <p>Tobias Koppers </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Learn the techniques you need to write professional, modern JavaScript. This course starts with the basics and takes you to mastering key functional methods like map, reduce and filter ...plus promises and ES6+ asynchronous JavaScript.</p>
  <p>Frontend Masters <span style="text-transform: uppercase; padding: 1px 4px;  margin-left: 4px; font-size: 0.9em;   color: #997 !important;">sponsor</span></p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"> is a framework from Basecamp that <em>augments</em> your HTML using controllers.</p>
  <p>Ilya Bodrov </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — The first release of Node 10 is due next Tuesday (April 24th) and will go LTS in October, but what’s new? HTTP/2 support, organized coded errors, and more.</p>
  <p>Tierney Cyren </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></p>
  <p>ZEIT </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Oracle’s alleged cease and desist order over an iOS app's use of "JavaScript" in its title highlights an issue with the language’s nomenclature.</p>
  <p>James Sanders </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — One to share with anyone you know who’d like a quick, fun way to learn some JavaScript on their phone (Android or iOS) - note that it’s <em>very</em> entry level.</p>
  <p>Area 120 </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Slack <span style="text-transform: uppercase; padding: 1px 4px;  margin-left: 4px; font-size: 0.9em;   color: #997 !important;">sponsor</span></p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Gregg Pollack </p>
</td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  "><p>💻 Jobs</p></td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;">.</p>
  <p>x-team </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Hospitality/tech platform focused on building help into our homes. React, React Native, Node, TypeScript, PostgreSQL.</p>
  <p>Hello Alfred </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Create your discreet profile today and receive opportunities from top US companies who can pay you what you’re worth.</p>
  <p>Woo.io </p>
</td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  "><p>📘 Tutorials</p></td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>William Woodhead </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Leon Revill </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Affecting scrolling with the latest CSS and JS features.</p>
  <p>Anna Selezniova and Andy Barnov </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — DevOps has grown. Here are six patterns that are shifting the scope of software delivery automation.</p>
  <p>CircleCI <span style="text-transform: uppercase; padding: 1px 4px;  margin-left: 4px; font-size: 0.9em;   color: #997 !important;">sponsor</span></p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Per Harald Borgen </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;">▶   often surveys as the most popular editor in the JS space, so this collection of videos may be handy.</p>
  <p>Burke Holland and Sarah Drasner </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Zell Liew </p>
</td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  "><p>🔧 Code and Tools</p></td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — e.g. for phone, date, currency, emails, and similar data types.</p>
  <p>Text Mask </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — e.g. ‘I ♥ Dogs’ becomes ‘i-love-dogs’</p>
  <p>Sindre Sorhus </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — ‘Swizzling’ is a way to quickly rearrange vector elements.</p>
  <p>Popmotion </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Relying on users to report bugs? 500K devs see unminified code right in Sentry’s stack trace with source maps.</p>
  <p>Sentry <span style="text-transform: uppercase; padding: 1px 4px;  margin-left: 4px; font-size: 0.9em;   color: #997 !important;">sponsor</span></p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Here’s a blast from the past, 3 years after its last release.</p>
  
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Melanie Sumner and Kenneth Larsen </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Maximilian Stoiber </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — If you want a self-hosted Mailchimp-esque system, say.</p>
  <p>Mailtrain </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></p>
  <p>tehnokv </p>
</td></tr></table>
<table border=0 border=0><tr><td style=" font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   "></td></tr></table>
</div>

  </td></tr>
</table>





<img src="https://javascriptweekly.com/open/382/rss" width="1" height="1" />
---------------
<h1 id="#title_1" >2、What You Need To Know To Increase Mobile Checkout Conversions</h1>
Suzanna Scacca
[https://www.smashingmagazine.com/2018/04/increasing-mobile-checkout-conversions/](https://www.smashingmagazine.com/2018/04/increasing-mobile-checkout-conversions/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/04/increasing-mobile-checkout-conversions/" />
              <title>What You Need To Know To Increase Mobile Checkout Conversions</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>What You Need To Know To Increase Mobile Checkout Conversions</h1>
                  
                    
                    <address>Suzanna Scacca</address>
                  
                  <time datetime="2018-04-20T13:35:58&#43;02:00" class="op-published">2018-04-20T13:35:58+02:00</time>
                  <time datetime="2018-04-20T15:32:23&#43;00:00" class="op-modified">2018-04-20T15:32:23+00:00</time>
                </header>
                <p> is here. Well, for some websites anyway. For the rest of us, it will be here soon enough, and our websites need to be in tip-top shape if we don’t want search rankings to be adversely affected by the change.</p>

<p>That said, responsive web design is nothing new. We’ve been creating custom mobile user experiences for years now, so most of our websites should be well poised to take this on… right?</p>

<p>Here’s the problem: Research shows that the dominant device through which users access the web, <em>on average</em>, is the smartphone. Granted, this might not be the case for every website, but the data indicates that this is the direction we’re headed in, and so every web designer should be prepared for it.</p>

<p>However, mobile checkout conversions are, to put it bluntly, not good. There are a number of reasons for this, but that doesn’t mean that m-commerce designers should take this lying down.</p>

<p>As more mobile users rely on their smart devices to access the web, websites need to be more adeptly designed to give them the simplified, convenient and secure checkout experience they want. In the following roundup, I’m going to explore some of the impediments to conversion in the mobile checkout and focus on what web designers can do to improve the experience.</p>



  <aside class="product-panel product-panel__tilted product-panel--book" data-audience="non-subscriber">
    <div class="container product-panel--book__container">
      <div class="panel__description panel__description--book">
    <p>Getting the process <em>just</em> right ain't an easy task. That's why we've set up <strong>'this-is-how-I-work'-sessions</strong> — with smart cookies sharing what works really well for them. A part of the , of course.</p>
      <a href="https://www.smashingmagazine.com/membership/" class="btn btn--green btn--large">
        Explore features&nbsp;→
      </a>
      </div>
      <div class="panel__image panel__image--book">
        <a href="https://www.smashingmagazine.com/membership/" class="books__book__image">
        <div class="books__book__img">
          <img src="https://www.smashingmagazine.com/images/smashing-cat/cat-scubadiving-panel.svg" alt="Smashing TV, with live sessions for professional designers and developers." width="310" height="400">
        </div>
      </a>
      </div>
    </div>
  </aside>





<div class="c-garfield-the-cat">


<h3>Why Are Mobile Checkout Conversions Lagging?</h3>

<p>According to the data, prioritizing the mobile experience in our web design strategies is a smart move for everyone involved. With people spending roughly  through mobile devices (as opposed to only 42% on desktop), search engines and websites really do need to align with user trends.</p>

<p>Now, while that statistic paints a positive picture in support of designing websites with a mobile-first approach, other statistics are floating around that might make you wary of it. Here’s why I say that:  issued for Q1 2017 had some really interesting data to show.</p>

<p>In this first table, they break down the percentage of visitors to e-commerce websites using different devices between Q1 2016 and Q1 2017. As you can see, smartphone Internet access has indeed surpassed desktop:</p>

<p><table class="tablesaw break-out" data-tablesaw-mode="swipe" data-tablesaw-minimap>
    <thead>
        <tr>
            <th data-tablesaw-priority="persist">Website Visits by Device</th>
            <th>Q1 2016</th>
            <th>Q2 2016</th>
            <th>Q3 2016</th>
            <th>Q4 2016</th>
            <th>Q1 2017</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Traditional</td>
            <td>49.30%</td>
            <td>47.50%</td>
            <td>44.28%</td>
            <td>42.83%</td>
            <td>42.83%</td>
        </tr>
        <tr>
            <td>Smartphone</td>
            <td>36.46%</td>
            <td>39.00%</td>
            <td>43.07%</td>
            <td>44.89%</td>
            <td>44.89%</td>
        </tr>
        <tr>
            <td>Other</td>
            <td>0.62%</td>
            <td>0.39%</td>
            <td>0.46%</td>
            <td>0.36%</td>
            <td>0.36%</td>
        </tr>
        <tr>
            <td>Tablet</td>
            <td>13.62%</td>
            <td>13.11%</td>
            <td>12.19%</td>
            <td>11.91%</td>
            <td>11.91%</td>
        </tr>
    </tbody>
</table>
<p><em>Monetate’s findings on which devices are used to access in the Internet. ()</em></p></p>

<p>In this next data set, we can see that the average conversion rate for e-commerce websites isn’t great. In fact, the number has gone down significantly since the first quarter of 2016.</p>

<p><table class="tablesaw break-out" data-tablesaw-mode="swipe" data-tablesaw-minimap>
    <thead>
        <tr>
            <th data-tablesaw-priority="persist">Conversion Rates</th>
            <th>Q1 2016</th>
            <th>Q2 2016</th>
            <th>Q3 2016</th>
            <th>Q4 2016</th>
            <th>Q1 2017</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Global</td>
            <td>3.10%</td>
            <td>2.81%</td>
            <td>2.52%</td>
            <td>2.94%</td>
            <td>2.48%</td>
        </tr>
    </tbody>
</table>
<p><em>Monetate’s findings on overall e-commerce global conversion rates (for all devices).  ()</em></figcaption></p>

<p>Even more shocking is the split between device conversion rates:</p>

<p><table class="tablesaw break-out" data-tablesaw-mode="swipe" data-tablesaw-minimap>
    <thead>
        <tr>
            <th data-tablesaw-priority="persist">Conversion Rates by Device</th>
            <th>Q1 2016</th>
            <th>Q2 2016</th>
            <th>Q3 2016</th>
            <th>Q4 2016</th>
            <th>Q1 2017</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Traditional</td>
            <td>4.23%</td>
            <td>3.88%</td>
            <td>3.66%</td>
            <td>4.25%</td>
            <td>3.63%</td>
        </tr>
        <tr>
            <td>Tablet</td>
            <td>1.42%</td>
            <td>1.31%</td>
            <td>1.17%</td>
            <td>1.49%</td>
            <td>1.25%</td>
        </tr>
        <tr>
            <td>Other</td>
            <td>0.69%</td>
            <td>0.35%</td>
            <td>0.50%</td>
            <td>0.35%</td>
            <td>0.27%</td>
        </tr>
        <tr>
            <td>Smartphone</td>
            <td>3.59%</td>
            <td>3.44%</td>
            <td>3.21%</td>
            <td>3.79%</td>
            <td>3.14%</td>
        </tr>
    </tbody>
</table>
<p><em>Monetate’s findings on the average conversion rates, broken down by device. ()</em></p></p>

<p>Smartphones consistently receive fewer conversions than desktop, despite being the predominant device through which users access the web.</p>

<p>What’s the problem here? Why are we able to get people to mobile websites, but we lose them at checkout?</p>

<p>In its report from 2017 named “,” comScore breaks down the top five reasons why mobile checkout conversion rates are so low:</p>











<figure >
	
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d0b029cf-a13b-41b4-bae4-604edceb89b9/comscore-conversion-rates.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d0b029cf-a13b-41b4-bae4-604edceb89b9/comscore-conversion-rates.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d0b029cf-a13b-41b4-bae4-604edceb89b9/comscore-conversion-rates.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d0b029cf-a13b-41b4-bae4-604edceb89b9/comscore-conversion-rates.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d0b029cf-a13b-41b4-bae4-604edceb89b9/comscore-conversion-rates.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d0b029cf-a13b-41b4-bae4-604edceb89b9/comscore-conversion-rates.png"
			sizes="100vw"
			alt="Reasons why m-commerce doesn’t convert"
		/>
	

	
		<figcaption class="op-vertical-bottom">
			The most common reasons why m-commerce shoppers don’t convert. (Image: )
		</figcaption>
	
</figure>


<p>Here is the breakdown for why mobile users don’t convert:</p>

<ul>
<li>20.2% &mdash; security concerns</li>
<li>19.6% &mdash; unclear product details</li>
<li>19.6% &mdash; inability to open multiple browser tabs to compare</li>
<li>19.3% &mdash; difficulty navigating</li>
<li>18.6% &mdash; difficulty inputting information.</li>
</ul>

<p>Those are plausible reasons to move from the smartphone to the desktop to complete a purchase (if they haven’t been completely turned off by the experience by that point, that is).</p>

<p>In sum, we know that consumers want to access the web through their mobile devices. We also know that barriers to conversion are keeping them from staying put. So, how do we deal with this?</p>

<h3>10 Ways to Increase Mobile Checkout Conversions In 2018</h3>

<p>For most of the websites you’ve designed, you’re not likely to see much of a change in search ranking when Google’s mobile-first indexing becomes official.</p>

<p>Your mobile-friendly designs might be “good enough” to keep your websites at the top of search (to start, anyway), but what happens if visitors don’t stick around to convert? Will Google start penalizing you because your website can’t seal the deal with the majority of visitors? In all honesty, that scenario will only occur in extreme cases, where the mobile checkout is so poorly constructed that bounce rates skyrocket and people stop wanting to visit the website at all.</p>

<p>Let’s say that the drop-off in traffic at checkout doesn’t incur penalties from Google. That’s great… for SEO purposes. But what about for business? Your goal is to get visitors to convert without distraction and without friction. Yet, that seems to be what mobile visitors get.</p>

<p>Going forward, your goal needs to be two-fold:</p>

<ul>
<li>to design websites with Google’s mobile-first mission and guidelines in mind,</li>
<li>to keep mobile users on the website until they complete a purchase.</li>
</ul>

<p>Essentially, this means decreasing the amount of work users have to do and improving the visibility of your security measures. Here is what you can do to more effectively design mobile checkouts for conversions.</p>

<h4>1. Keep the Essentials in the Thumb Zone</h4>

<p>Research on  is old hat by now. We know that, whether they use the single- or double-handed approach, certain parts of the mobile screen are just inconvenient for mobile users to reach. And when expediency is expected during checkout, this is something you don’t want to mess around with.</p>

<p>For single-handed users, the middle of the screen is the prime playing field:</p>











<figure >
	
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4a01d1ff-2aa6-42ec-802e-e62b1cef0f7b/single-handed-mobile.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4a01d1ff-2aa6-42ec-802e-e62b1cef0f7b/single-handed-mobile.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4a01d1ff-2aa6-42ec-802e-e62b1cef0f7b/single-handed-mobile.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4a01d1ff-2aa6-42ec-802e-e62b1cef0f7b/single-handed-mobile.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4a01d1ff-2aa6-42ec-802e-e62b1cef0f7b/single-handed-mobile.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4a01d1ff-2aa6-42ec-802e-e62b1cef0f7b/single-handed-mobile.png"
			sizes="100vw"
			alt="The thumb zone for single-handed mobile"
		/>
	

	
		<figcaption class="op-vertical-bottom">
			The good, OK and bad areas for single-handed mobile users. (Image: )
		</figcaption>
	
</figure>


<p>Although users who cradle their phones for greater stability have a couple options for which fingers to use to interact with the screen, only 28% use their index finger. So, let’s focus on the capabilities of thumb users, which, again, means giving the central part of the screen the most prominence:</p>











<figure >
	
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/24d27bb9-f431-49b1-8798-e18559cb10b4/mobile-fingers.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/24d27bb9-f431-49b1-8798-e18559cb10b4/mobile-fingers.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/24d27bb9-f431-49b1-8798-e18559cb10b4/mobile-fingers.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/24d27bb9-f431-49b1-8798-e18559cb10b4/mobile-fingers.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/24d27bb9-f431-49b1-8798-e18559cb10b4/mobile-fingers.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/24d27bb9-f431-49b1-8798-e18559cb10b4/mobile-fingers.png"
			sizes="100vw"
			alt="The thumb and index finger zone for mobile cradling"
		/>
	

	
		<figcaption class="op-vertical-bottom">
			The good, OK and bad areas for mobile users that cradle their phones. (Image: )
		</figcaption>
	
</figure>


<p>Some users hold their phones with two hands. Because the horizontal orientation is more likely to be used for video, this won’t be relevant for mobile checkout. So, pay attention to how much space of that screen is feasibly within reach of the user’s thumb:</p>











<figure >
	
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5c44c210-8e64-4f71-884d-bc993db0554f/vertical-horizontal-mobile.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5c44c210-8e64-4f71-884d-bc993db0554f/vertical-horizontal-mobile.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5c44c210-8e64-4f71-884d-bc993db0554f/vertical-horizontal-mobile.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5c44c210-8e64-4f71-884d-bc993db0554f/vertical-horizontal-mobile.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5c44c210-8e64-4f71-884d-bc993db0554f/vertical-horizontal-mobile.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5c44c210-8e64-4f71-884d-bc993db0554f/vertical-horizontal-mobile.png"
			sizes="100vw"
			alt="The thumb zone for vertical and horizontal"
		/>
	

	
		<figcaption class="op-vertical-bottom">
			The good, OK and bad areas for two-handed mobile users. (Image: )
		</figcaption>
	
</figure>


<p>In sum, we can use  of where to focus content, regardless of left-hand, right-hand or two-handed holding of a smartphone:</p>











<figure >
	
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0732b888-4e74-40b8-aee5-74acbba7fa04/left-right-mobile.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0732b888-4e74-40b8-aee5-74acbba7fa04/left-right-mobile.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0732b888-4e74-40b8-aee5-74acbba7fa04/left-right-mobile.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0732b888-4e74-40b8-aee5-74acbba7fa04/left-right-mobile.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0732b888-4e74-40b8-aee5-74acbba7fa04/left-right-mobile.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0732b888-4e74-40b8-aee5-74acbba7fa04/left-right-mobile.png"
			sizes="100vw"
			alt="Where the ideal thumb zone is on mobile"
		/>
	

	
		<figcaption class="op-vertical-bottom">
			A summary of where the good, OK and bad zones are on mobile devices. (Image: )
		</figcaption>
	
</figure>


<p> is a good example of how to do this:</p>











<figure >
	
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ed5be663-6507-4da0-bdf2-6244b5dc9586/jcpenney-form-placement.PNG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ed5be663-6507-4da0-bdf2-6244b5dc9586/jcpenney-form-placement.PNG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ed5be663-6507-4da0-bdf2-6244b5dc9586/jcpenney-form-placement.PNG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ed5be663-6507-4da0-bdf2-6244b5dc9586/jcpenney-form-placement.PNG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ed5be663-6507-4da0-bdf2-6244b5dc9586/jcpenney-form-placement.PNG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ed5be663-6507-4da0-bdf2-6244b5dc9586/jcpenney-form-placement.PNG"
			sizes="100vw"
			alt="JCPenney’s form is in the thumb zone"
		/>
	

	
		<figcaption class="op-vertical-bottom">
			JCPenney’s contact form starts midway down the page. (Image: )
		</figcaption>
	
</figure>


<p>While information is included at the top of the checkout page, the input fields don’t start until just below the middle of it &mdash; directly in the ideal thumb zone for users of any type. This ensures that visitors holding their phones in any manner and using different fingers to engage with it will have no issue reaching the form fields.</p>

<h4>2. Minimize Content to Maximize Speed</h4>

<p>We’ve been taught over and over again that minimal design is best for websites. This is especially true in mobile checkout, where an already slow or frustrating experience could easily push a customer over the edge, when all they want to do is be done with the purchase.</p>


  <div id="sponsors-article" data-impression="true" class="c-promo-box c-promo-box--ad sponsors hidden" data-audience="non-subscriber" data-remove="true"></div>



<p>To maximize speed during the mobile checkout process, keep the following tips in mind:</p>

<ul>
<li>Only add the essentials to checkout. This is not the time to try to upsell or cross-sell, promote social media or otherwise distract from the action at hand.</li>
<li>Keep the checkout free of all images. The only eye-catching visuals that are really acceptable are trustmarks and calls to action (more on these below).</li>
<li>Any text included on the page should be instructional or descriptive in nature.</li>
<li>Avoid any special stylization of fonts. The less “wow” your checkout page has, the easier it will be for users to get through the process.</li>
</ul>

<p>Look to ’ website as an example of what a highly simple single-page checkout should look like:</p>











<figure >
	
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dfecb586-cb2c-40fc-83fa-3f9eec9e9a1d/staples-simplicity.PNG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dfecb586-cb2c-40fc-83fa-3f9eec9e9a1d/staples-simplicity.PNG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dfecb586-cb2c-40fc-83fa-3f9eec9e9a1d/staples-simplicity.PNG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dfecb586-cb2c-40fc-83fa-3f9eec9e9a1d/staples-simplicity.PNG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dfecb586-cb2c-40fc-83fa-3f9eec9e9a1d/staples-simplicity.PNG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dfecb586-cb2c-40fc-83fa-3f9eec9e9a1d/staples-simplicity.PNG"
			sizes="100vw"
			alt="The single-page checkout for Staples"
		/>
	

	
		<figcaption class="op-vertical-bottom">
			Staples has a single-page checkout with a minimal number of fields to fill out. (Image: )
		</figcaption>
	
</figure>


<p>As you can see, Staples doesn’t bog down the checkout process with product images, branding, navigation, internal links or anything else that might (1) distract from the task at hand, or (2) suck resources from the server while it attempts to process your customers’ requests.</p>

<p>Not only will this checkout page be easy to get through, but it will load quickly and without issue every time &mdash; something customers will remember the next time they need to make a purchase. By keeping your checkout pages light in design, you ensure a speedy experience in all aspects.</p>

<h4>3. Put Them at Ease With Trustmarks</h4>

<p>A trustmark is any indicator on a website that lets customers know, “Hey, there’s absolutely nothing to worry about here. We’re keeping your information safe!”</p>

<p>The one trustmark that every m-commerce website should have? An SSL certificate. Without one, the address bar will not display the lock sign or the green <code>https</code> domain name &mdash; both of which let customers know that the website has extra encryption.</p>

<p>You can use other trustmarks at checkout as well.</p>











<figure >
	
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/85e36c44-714b-4ad7-a5f8-e28762ffcd00/big-chill-trustmark.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/85e36c44-714b-4ad7-a5f8-e28762ffcd00/big-chill-trustmark.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/85e36c44-714b-4ad7-a5f8-e28762ffcd00/big-chill-trustmark.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/85e36c44-714b-4ad7-a5f8-e28762ffcd00/big-chill-trustmark.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/85e36c44-714b-4ad7-a5f8-e28762ffcd00/big-chill-trustmark.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/85e36c44-714b-4ad7-a5f8-e28762ffcd00/big-chill-trustmark.png"
			sizes="100vw"
			alt="Big Chill uses a RapidSSL trust seal"
		/>
	

	
		<figcaption class="op-vertical-bottom">
			Big Chill includes a RapidSSL trust seal to let customers know its data is encrypted. (Image: )
		</figcaption>
	
</figure>


<p>While you can use logos from  and other security software to let customers know your website is protected, users might also be swayed by recognizable and well-trusted names. When you think about it, this isn’t much different than displaying corporate logos beside customer testimonials or in callouts that boast of your big-name connections. If you can leverage a partnership like the ones mentioned below, you can use the inherent trust there to your benefit.</p>

<p>Take , which uses a “Login with Amazon” option at checkout:</p>











<figure >
	
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/35905e35-7425-40b7-8f4d-c03069529c49/6-pm-trustmark.PNG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/35905e35-7425-40b7-8f4d-c03069529c49/6-pm-trustmark.PNG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/35905e35-7425-40b7-8f4d-c03069529c49/6-pm-trustmark.PNG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/35905e35-7425-40b7-8f4d-c03069529c49/6-pm-trustmark.PNG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/35905e35-7425-40b7-8f4d-c03069529c49/6-pm-trustmark.PNG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/35905e35-7425-40b7-8f4d-c03069529c49/6-pm-trustmark.PNG"
			sizes="100vw"
			alt="6pm uses an Amazon trustmark"
		/>
	

	
		<figcaption class="op-vertical-bottom">
			6pm leverages the Amazon name as a trustmark. (Image: )
		</figcaption>
	
</figure>


<p>This is a smart move for a brand that most definitely does not have the brand-name recognition that a company like Amazon has. By giving customers a convenient option to log in with a brand that’s synonymous with speed, reliability and trust, the company might now become known for those same checkout qualities that Amazon is celebrated for.</p>

<p>Then, there are mobile checkout pages like the one on :</p>











<figure >
	
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3b11e5e9-5827-4716-b0a6-064500f38bf8/sephora-trustmark.PNG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3b11e5e9-5827-4716-b0a6-064500f38bf8/sephora-trustmark.PNG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3b11e5e9-5827-4716-b0a6-064500f38bf8/sephora-trustmark.PNG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3b11e5e9-5827-4716-b0a6-064500f38bf8/sephora-trustmark.PNG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3b11e5e9-5827-4716-b0a6-064500f38bf8/sephora-trustmark.PNG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3b11e5e9-5827-4716-b0a6-064500f38bf8/sephora-trustmark.PNG"
			sizes="100vw"
			alt="Sephora’s PayPal trustmark"
		/>
	

	
		<figcaption class="op-vertical-bottom">
			Sephora uses a trusted payment gateway provider as a trustmark. (Image: )
		</figcaption>
	
</figure>


<p>Sephora also uses this technique of leveraging another brand’s good name in order to build trust at checkout time. In this case, however, it presents customers with two clear options: Check out with us right now, or hop over to PayPal, which will take care of you securely. With security being a major concern that keeps mobile customers from converting, this kind of trustmark and payment method is a good move on Sephora’s part.</p>

<h4>4. Provide Easier Editing</h4>

<p>In general, never take a visitor (on any device) away from whatever they’re doing on your website. There are already enough distractions online; the last thing they need is for <em>you</em> to point them in a direction that keeps them from converting.</p>

<p>At checkout, however, your customers might feel compelled to do this very thing if they decide they want a different color, size or quantity of an item in their shopping cart. Rather than let them backtrack through the website, give them an in-checkout editing option to keep them in place.</p>

<p> does this well:</p>











<figure >
	
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/32685fe2-8219-4641-afb4-6811b7d98555/victorias-secret-checkout-edits.PNG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/32685fe2-8219-4641-afb4-6811b7d98555/victorias-secret-checkout-edits.PNG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/32685fe2-8219-4641-afb4-6811b7d98555/victorias-secret-checkout-edits.PNG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/32685fe2-8219-4641-afb4-6811b7d98555/victorias-secret-checkout-edits.PNG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/32685fe2-8219-4641-afb4-6811b7d98555/victorias-secret-checkout-edits.PNG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/32685fe2-8219-4641-afb4-6811b7d98555/victorias-secret-checkout-edits.PNG"
			sizes="100vw"
			alt="Victoria’s Secret edit lightbox in checkout"
		/>
	

	
		<figcaption class="op-vertical-bottom">
			Victoria’s Secret doesn’t force users away from checkout to edit items. (Image: )
		</figcaption>
	
</figure>


<p>When they first get to the checkout screen, customers will see a list of items they’re about to purchase. When the large “Edit” button beside each item is clicked, a lightbox (shown above) opens with the product’s variations. It’s basically the original product page, just superimposed on top of the checkout. Users can adjust their options and save their changes without ever having to leave the checkout page.</p>

<p>If you find, in reviewing your website’s analytics, that users occasionally backtrack after hitting the checkout (you can see this in the sales funnel), add this built-in editing feature. By preventing this unnecessary movement backwards, you could save yourself lost conversions from confused or distracted customers.</p>

<h4>5. Enable Express Checkout Options</h4>

<p>When consumers check out on an e-commerce website through a desktop device, it probably isn’t a big deal if they have to input their user name, email address or payment information each time. Sure, if it can be avoided, they’ll find ways around it (like allowing the website to save their information or using a password manager such as LastPass).</p>

<p>But on mobile, re-entering that information is a pain, especially if contact forms aren’t optimized well (more on that below). So, to ease the log-in and checkout process for mobile users, consider ways in which you can simplify the process:</p>

<ul>
<li>Allow for guest checkout.</li>
<li>Allow for one-click expedited checkout.</li>
<li>Enable one-click sign-in from a trusted source, like Facebook.</li>
<li>Enable payment on a trusted payment provider’s website, like PayPal, Google Wallet or Stripe.</li>
</ul>

<p>One of the nice things about 's already convenient checkout process is that customers can automate the sign-in process going forward with a simple toggle:</p>











<figure >
	
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/16b34d00-8293-4d26-a519-945a7186cd89/sephora-streamlined-signin.PNG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/16b34d00-8293-4d26-a519-945a7186cd89/sephora-streamlined-signin.PNG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/16b34d00-8293-4d26-a519-945a7186cd89/sephora-streamlined-signin.PNG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/16b34d00-8293-4d26-a519-945a7186cd89/sephora-streamlined-signin.PNG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/16b34d00-8293-4d26-a519-945a7186cd89/sephora-streamlined-signin.PNG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/16b34d00-8293-4d26-a519-945a7186cd89/sephora-streamlined-signin.PNG"
			sizes="100vw"
			alt="Sephora lets customers save sign-in information"
		/>
	

	
		<figcaption class="op-vertical-bottom">
			Sephora enables return customers to stay signed in, to avoid this during checkout again. (Image: )
		</figcaption>
	
</figure>


<p>When mobile customers are feeling the rush and want to get to the next stage of checkout, Sephora’s auto-sign-in feature would definitely come in handy and encourage customers to buy more frequently from the mobile website.</p>

<p>Many mobile websites wait until the bottom of the login page to tell customers what kinds of options they have for checking out. But rather than surprise them late,  displays this information in big bold buttons right at the very top:</p>











<figure >
	
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dd39c728-2319-4998-8562-dc47b4d4f30a/victorias-secret-express-checkout.PNG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dd39c728-2319-4998-8562-dc47b4d4f30a/victorias-secret-express-checkout.PNG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dd39c728-2319-4998-8562-dc47b4d4f30a/victorias-secret-express-checkout.PNG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dd39c728-2319-4998-8562-dc47b4d4f30a/victorias-secret-express-checkout.PNG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dd39c728-2319-4998-8562-dc47b4d4f30a/victorias-secret-express-checkout.PNG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dd39c728-2319-4998-8562-dc47b4d4f30a/victorias-secret-express-checkout.PNG"
			sizes="100vw"
			alt="Victoria’s Secret express checkout options"
		/>
	

	
		<figcaption class="op-vertical-bottom">
			Victoria’s Secret simplifies and speeds up checkout by giving three attractive options. (Image: )
		</figcaption>
	
</figure>


<p>Customers have a choice of signing in with their account, checking out as a guest or going directly to PayPal. They are not surprised to discover later on that their preferred checkout or payment method isn’t offered.</p>

<p>I also really love how Victoria’s Secret has chosen to do this. There’s something nice about the brightly colored “Sign In” button sitting beside the more muted “Check Out as a Guest” button. For one, it adds a hint of Victoria’s Secret brand colors to the checkout, which is always a nice touch. But the way it’s colored the buttons also makes clear what it wants the primary action to be (i.e. to create an account and sign in).</p>

<h4>6. Add Breadcrumbs</h4>

<p>When you send mobile customers to checkout, the last thing you want is to give them unnecessary distractions. That’s why the website’s standard navigation bar (or hamburger menu) is typically removed from this page.</p>

<p>Nonetheless, the checkout process can be intimidating if customers don’t know what’s ahead. How many forms will they need to fill out? What sort of information is needed? Will they have a chance to review their order before submitting payment details?</p>

<p>If you’ve designed a multi-page checkout, allay your customers’ fears by defining each step with clearly labeled breadcrumb navigation at the top of the page. In addition, this will give your checkout a cleaner design, reducing the number of clicks and scrolling per page.</p>

<p> has a beautiful example of breadcrumb navigation in action:</p>











<figure >
	
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/224ddaaf-1197-4d33-9982-9c8dd582aae5/hayneedle-breadcrumbs.PNG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/224ddaaf-1197-4d33-9982-9c8dd582aae5/hayneedle-breadcrumbs.PNG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/224ddaaf-1197-4d33-9982-9c8dd582aae5/hayneedle-breadcrumbs.PNG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/224ddaaf-1197-4d33-9982-9c8dd582aae5/hayneedle-breadcrumbs.PNG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/224ddaaf-1197-4d33-9982-9c8dd582aae5/hayneedle-breadcrumbs.PNG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/224ddaaf-1197-4d33-9982-9c8dd582aae5/hayneedle-breadcrumbs.PNG"
			sizes="100vw"
			alt="Hayneedle checkout breadcrumb navigation"
		/>
	

	
		<figcaption class="op-vertical-bottom">
			Hayneedle’s breadcrumbs are cleanly designed and easy to find. (Image: )
		</figcaption>
	
</figure>


<p>You can see that three steps are broken out and clearly labeled. There’s absolutely no question here about what users will encounter in those steps either, which will help put their minds at ease. Three steps seems reasonable enough, and users will have a chance to review the order once more before completing the purchase.</p>

<p> has an alternative style of “breadcrumbs” in its checkout:</p>











<figure >
	
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0849f5a7-04a2-4496-8119-e85b556a40b8/sephora-breadcrumbs.PNG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0849f5a7-04a2-4496-8119-e85b556a40b8/sephora-breadcrumbs.PNG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0849f5a7-04a2-4496-8119-e85b556a40b8/sephora-breadcrumbs.PNG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0849f5a7-04a2-4496-8119-e85b556a40b8/sephora-breadcrumbs.PNG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0849f5a7-04a2-4496-8119-e85b556a40b8/sephora-breadcrumbs.PNG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0849f5a7-04a2-4496-8119-e85b556a40b8/sephora-breadcrumbs.PNG"
			sizes="100vw"
			alt="Sephora’s numbered breadcrumbs navigation"
		/>
	

	
		<figcaption class="op-vertical-bottom">
			Sephora’s numbered breadcrumbs appear as you complete each section. (Image: )
		</figcaption>
	
</figure>


<p>Instead of placing each “breadcrumb” at the top of the checkout page, Sephora’s customers can see what the next step is, as well as how many more are to come as they work their way through the form.</p>

<p>This is a good option to take if you’d rather not make the top navigation or the breadcrumbs sticky. Instead, you can prioritize the call to action (CTA), which you might find better motivates the customer to move down the page and complete their purchase.</p>

<p>I think both of these breadcrumbs designs are valid, though. So, it might be worth A/B testing them if you’re unsure of which would lead to more conversions for your visitors.</p>

<h4>7. Format the Checkout Form Wisely</h4>

<p>Good mobile checkout form design follows a pretty strict formula, which isn’t surprising. While there are ways to bend the rules on desktop in terms of structuring the form, the number of steps per page, the inclusion of images and so on, you really don’t have that kind of flexibility on mobile.</p>

<p>Instead, you will need to be meticulous when building the form:</p>

<ul>
<li>Design each field of the checkout form so that it stretches the full width of the website.</li>
<li>Limit the fields to only what’s essential.</li>
<li>Clearly label each field outside of and above it.</li>
<li>Use at least a 16-point-pixel font.</li>
<li>Format each field so that it’s large enough to tap into without zooming.</li>
<li>Use a recognizable mark to indicate when something is required (like an asterisk).</li>
<li>Always let users know when an error has been made immediately after the information has been inputted in a field.</li>
<li>Place the call to action at the very bottom of the form.</li>
</ul>

<p>Because the checkout form is the most important element that moves customers through the checkout process, you can’t afford to mess around with a tried and true formula. If users can’t seamlessly get from top to bottom, if the fields are too difficult to engage with, or if the functionality of the form itself is riddled with errors, then you might as well kiss your mobile purchases (and maybe your purchases in general) goodbye.</p>

<p> shows how to create form fields that are very user-friendly on mobile:</p>











<figure >
	
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2f3a3e70-c9fb-4254-9e96-ac7f5da840f6/crutchfield-big-buttons.PNG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2f3a3e70-c9fb-4254-9e96-ac7f5da840f6/crutchfield-big-buttons.PNG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2f3a3e70-c9fb-4254-9e96-ac7f5da840f6/crutchfield-big-buttons.PNG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2f3a3e70-c9fb-4254-9e96-ac7f5da840f6/crutchfield-big-buttons.PNG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2f3a3e70-c9fb-4254-9e96-ac7f5da840f6/crutchfield-big-buttons.PNG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2f3a3e70-c9fb-4254-9e96-ac7f5da840f6/crutchfield-big-buttons.PNG"
			sizes="100vw"
			alt="Large-sized form fields on the Crutchfield checkout"
		/>
	

	
		<figcaption class="op-vertical-bottom">
			Form fields on the Crutchfield checkout page are large and difficult to miss. (Image: )
		</figcaption>
	
</figure>


<p>As you can see, each field is large enough to click on (even with fat fingers). The bold outline around the currently selected field is also a nice touch. For a customer who is multitasking and or distracted by something around them, returning to the checkout form would be much easier with this type of format.</p>

<p>, again, handles mobile checkout the right way. In this case, I want to draw your attention to the grayed-out “Place Order” button:</p>











<figure >
	
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/26d09371-5e91-44e8-aa03-ec5b09a46f84/sephora-faded-button.PNG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/26d09371-5e91-44e8-aa03-ec5b09a46f84/sephora-faded-button.PNG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/26d09371-5e91-44e8-aa03-ec5b09a46f84/sephora-faded-button.PNG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/26d09371-5e91-44e8-aa03-ec5b09a46f84/sephora-faded-button.PNG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/26d09371-5e91-44e8-aa03-ec5b09a46f84/sephora-faded-button.PNG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/26d09371-5e91-44e8-aa03-ec5b09a46f84/sephora-faded-button.PNG"
			sizes="100vw"
			alt="Smart use of the Sephora call to action in checkout"
		/>
	

	
		<figcaption class="op-vertical-bottom">
			Sephora uses the call to action as a guide for customers who haven’t finished the form. (Image: )
		</figcaption>
	
</figure>


<p>The button serves as an indicator to customers that they’re not quite ready to submit their purchase information yet, which is great. Even though the form is beautifully designed &mdash; everything is well labeled, the fields are large, and the form is logically organized &mdash; mobile users could accidentally scroll too far past a field and wouldn’t know it until clicking the call-to-action button.</p>

<p>If you can keep users from receiving that dreaded “missing information” error, you’ll do a better job of holding onto their purchases.</p>

<h4>8. Simplify Form Input</h4>

<p>Digging a bit deeper into these contact forms, let’s look at how you can simplify the input of data on mobile:</p>

<ul>
<li>Allow customers to user their browser’s autocomplete functionality to fill in forms.</li>
<li>Include a <code>tabindex</code> HTML directive to enable customers to tap an arrow up and down through the form. This keeps their thumbs within a comfortable range on the smartphone at all times, instead of constantly reaching up to tap into a new field.</li>
<li>Add a checkbox that automatically copies the billing address information over to the shipping fields.</li>
<li>Change the keyboard according to what kind of field is being typed in.</li>
</ul>

<p>One example of this is ’ mobile website:</p>











<figure >
	
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ed735c71-a208-45ba-a259-742c059c36fc/bass-pro-keyboard.PNG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ed735c71-a208-45ba-a259-742c059c36fc/bass-pro-keyboard.PNG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ed735c71-a208-45ba-a259-742c059c36fc/bass-pro-keyboard.PNG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ed735c71-a208-45ba-a259-742c059c36fc/bass-pro-keyboard.PNG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ed735c71-a208-45ba-a259-742c059c36fc/bass-pro-keyboard.PNG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ed735c71-a208-45ba-a259-742c059c36fc/bass-pro-keyboard.PNG"
			sizes="100vw"
			alt="Bass Pro checkout form uses a smart keyboard"
		/>
	

	
		<figcaption class="op-vertical-bottom">
			Each field in the Bass Pro checkout form provides users with the right keyboard type. (Image: )
		</figcaption>
	
</figure>


<p>For starters, the keyboard uses tab functionality (see the up and down arrows just above the keyboard). For customers with short fingers or who are impatient and just want to type away on the keyboard, the tabs help keep their hands in one place, thus speeding up checkout.</p>

<p>Also, when customers tab into a numbers-only field (like for their phone number), the keyboard automatically changes, so they don’t have to switch manually. Again, this is another way to up the convenience of making a purchase on mobile.</p>

<p>’s mobile checkout includes a quick checkbox that streamlines customers’ submission of billing information:</p>











<figure >
	
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e89a4e6a-b065-4ec0-8534-be2bef845f54/amazon-dupe-address.PNG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e89a4e6a-b065-4ec0-8534-be2bef845f54/amazon-dupe-address.PNG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e89a4e6a-b065-4ec0-8534-be2bef845f54/amazon-dupe-address.PNG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e89a4e6a-b065-4ec0-8534-be2bef845f54/amazon-dupe-address.PNG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e89a4e6a-b065-4ec0-8534-be2bef845f54/amazon-dupe-address.PNG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e89a4e6a-b065-4ec0-8534-be2bef845f54/amazon-dupe-address.PNG"
			sizes="100vw"
			alt="Amazon streamlines form input with address duplication"
		/>
	

	
		<figcaption class="op-vertical-bottom">
			Amazon gives customers an easy way to duplicate their shipping address to billing. (Image: )
		</figcaption>
	
</figure>


<p>As we’ve seen with mobile checkout form design, simpler is always better. Obviously, you will always need to collect certain details from customers each time (unless their account has saved that information). Nonetheless, if you can provide a quick toggle or checkbox that enables them to copy data over from one form to another, then do it.</p>

<h4>9. Don’t Skimp on the CTA</h4>

<p>When designing a desktop checkout, your main concerns with the CTA are things like strategic placement of the button and choosing an eye-catching color to draw attention to it.</p>

<p>On mobile, however, you have to think about size, too &mdash; and not just how much space it takes up on the screen. Remember the thumb zone and the various ways in which users hold their phone. Ensure that the button is wide enough so that any user can easily click on it without having to change their hand position.</p>

<p>So, your goal should be to design buttons that (1) sit at the bottom of the mobile checkout page and (2) stretch all the way from left to right, as is the case on ’ mobile website:</p>











<figure >
	
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/64e2fd27-a8d1-4ffc-9c26-3e69971f5366/staples-big-button.PNG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/64e2fd27-a8d1-4ffc-9c26-3e69971f5366/staples-big-button.PNG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/64e2fd27-a8d1-4ffc-9c26-3e69971f5366/staples-big-button.PNG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/64e2fd27-a8d1-4ffc-9c26-3e69971f5366/staples-big-button.PNG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/64e2fd27-a8d1-4ffc-9c26-3e69971f5366/staples-big-button.PNG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/64e2fd27-a8d1-4ffc-9c26-3e69971f5366/staples-big-button.PNG"
			sizes="100vw"
			alt="Staple’s big blue CTA button"
		/>
	

	
		<figcaption class="op-vertical-bottom">
			Staple’s bright blue CTA sticks out in an otherwise plain checkout. (Image: )
		</figcaption>
	
</figure>


<p>No matter who is making the purchase &mdash; a left-handed, a right-handed or a two-handed cradler &mdash; that button will be easy reach.</p>

<p>Of all the mobile checkout enhancements we’ve covered today, the CTA is the easiest one to address. Make it big, give it a distinctive color, place it at the very bottom of the mobile screen, and make it span the full width. In other words, don’t make customers work hard to take the final step in a purchase.</p>

<h4>10. Offer an Alternate Way Out</h4>

<p>Finally, give customers an alternate way out.</p>

<p>Let’s say they’re shopping on a mobile website, adding items to their cart, but something isn’t sitting right with them, and they don’t want to make the purchase. You’ve done everything you can to assure them along the way with a clean, easy and secure checkout experience, but they just aren’t confident in making a payment on their phone.</p>

<p>Rather than merely hoping you don’t lose the purchase entirely, give them a chance to save it for later. That way, if they really are interested in buying your product, they can revisit on desktop and pull the trigger. It’s not ideal, because you do want to keep them in place on mobile, but the option is good for customers who just can’t be saved.</p>

<p>As you can see on ’s mobile website, there is an option at checkout to “Move to Wish List”:</p>











<figure >
	
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b7ce45dd-ca6c-48b4-9d62-dc750804cf5c/llbean-wishlist.PNG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b7ce45dd-ca6c-48b4-9d62-dc750804cf5c/llbean-wishlist.PNG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b7ce45dd-ca6c-48b4-9d62-dc750804cf5c/llbean-wishlist.PNG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b7ce45dd-ca6c-48b4-9d62-dc750804cf5c/llbean-wishlist.PNG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b7ce45dd-ca6c-48b4-9d62-dc750804cf5c/llbean-wishlist.PNG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b7ce45dd-ca6c-48b4-9d62-dc750804cf5c/llbean-wishlist.PNG"
			sizes="100vw"
			alt="L.L. Bean wish list option"
		/>
	

	
		<figcaption class="op-vertical-bottom">
			L.L. Bean gives customers another chance to move items to their wish list during checkout. (Image: )
		</figcaption>
	
</figure>


<p>What’s nice about this is that L.L. Bean clearly doesn’t want browsing of the wish list or the removal of an item to be a primary action. If “Move to Wish List” were shown as a big bold CTA button, more customers might decide to take this seemingly safer alternative. As it’s designed now, it’s more of a, “Hey, we don’t want you to do anything you’re not comfortable with. This is here just in case.”</p>

<p>While fewer options are generally better in web design, this might be something to explore if your checkout has a high cart abandonment rate on mobile.</p>

<h3>Wrapping Up</h3>

<p>As more mobile visitors flock to your website, every step leading to conversion &mdash; including the checkout phase &mdash; needs to be optimized for convenience, speed and security. If your checkout is not adeptly designed to mobile users’ specific needs and expectations, you’re going to find that those conversion rates drop or shift back to desktop &mdash; and that’s not the direction you want things to go in, especially if Google is pushing us all towards a mobile-first world.</p>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(da, ra, yk, al, il)</span>
</div>



  <div id="sponsors-article-end" data-impression="true" class="c-promo-box c-promo-box--ad c-promo-box--wide sponsors hidden" data-audience="non-subscriber" data-remove="true"></div>



</div>



              </article>
            </body>
          </html>
---------------
<h1 id="#title_2" >3、视频演讲： UCloud 开放 API 体系下的高可用和灰度发布实践</h1>
彭兴宇
[http://www.infoq.com/cn/presentations/practice-of-ucloud-open-api-system?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/practice-of-ucloud-open-api-system?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/presentations/practice-of-ucloud-open-api-system/zh/mediumimage/pengxingyu_270-1524137208139.jpg"/><p>UCloud 对用户开放了一系列可自助服务的 API，自身服务与用户业务都同样依赖这些 API 的可用性，从介绍我们微服务体系的变迁和高可用方案开始，再说到灰度发布方面的实践。</p> <i>By 彭兴宇</i>
---------------
<h1 id="#title_3" >4、美丽联合集团赵成：要让员工看到自己的未来</h1>
赵成
[http://www.infoq.com/cn/news/2018/04/beauty-conglomerate-Employee-fut?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/04/beauty-conglomerate-Employee-fut?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>能力是基础，更重要的是要善于思考，敢于表达</p> <i>By 赵成</i>
---------------
<h1 id="#title_4" >5、明略数据杨威：公安行业 AI 应用离成熟还有一段距离</h1>
杨赛
[http://www.infoq.com/cn/news/2018/04/distance-maturity-AI-security-in?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/04/distance-maturity-AI-security-in?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>理想中的人工智能引擎，到底是什么样的？</p> <i>By 杨赛</i>
---------------
<h1 id="#title_5" >6、TGO 鲲鹏会全球战略开启，硅谷分会即将成立</h1>
TGO鲲鹏会
[http://www.infoq.com/cn/news/2018/04/TGO-global-strategy-Silicon-bran?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/04/TGO-global-strategy-Silicon-bran?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>美国西部时间 4 月 21 日，TGO 鲲鹏会硅谷分会将正式举办成立仪式。</p> <i>By TGO鲲鹏会</i>
---------------
<h1 id="#title_6" >7、空中金融 CTO 朱晔：公司初创阶段 CTO 需要做什么？（上篇）</h1>
朱晔
[http://www.infoq.com/cn/news/2018/04/CTO-start-up-phase-company?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/04/CTO-start-up-phase-company?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>只有在正确的阶段做正确的事，才能更好地为公司做出贡献</p> <i>By 朱晔</i>
---------------
<h1 id="#title_7" >8、微软正在借助区块链技术管理数字化标识</h1>
Mix
[http://www.infoq.com/cn/news/2018/04/Microsoft-block-chain-digital?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/04/Microsoft-block-chain-digital?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>目前，用户需要广泛批准各类应用和服务收集并保存自己的个人数据，而这一切已经超出了用户的控制范围。随着数据外泄和标识盗窃事件层出不穷，并且愈加复杂频繁，用户需要通过某种方法重新掌控自己的标识信息。为此微软正在开发一种链下解决方案，这种网络可以在不会造成区块链网络拥堵的情况下处理海量ID数据</p> <i>By Mix</i> <i> Translated by 大愚若智</i>
---------------
<h1 id="#title_8" >9、迷你书： 中国顶尖技术团队访谈录·第十一季</h1>
InfoQ中文站
[http://www.infoq.com/cn/minibooks/toptech11?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/minibooks/toptech11?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/minibooks/toptech11/zh/smallimage/100-1524116232788.jpg"/><p>本次的《中国顶尖技术团队访谈录》·第十一季挑选的17个团队虽然都来自互联网企业，却是风格各异。希望通过这样的记录，能够让一家家品牌背后的技术人员形象更加鲜活，让更多人感受到他们的可爱与坚持。</p> <i>By InfoQ中文站</i>
---------------