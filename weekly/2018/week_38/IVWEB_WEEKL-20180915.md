## 文章索引
1、 <a href="#1celebrating-10-years-of-the-v8-javascript-engine" >Celebrating 10 Years of the V8 JavaScript engine</a><br/>
2、 <a href="#2monthly-web-development-update-9/2018:-native-lazy-loading-and-imaginary-work" >Monthly Web Development Update 9/2018: Native Lazy Loading And Imaginary Work</a><br/>
3、 <a href="#3每周分享第-22-期" >每周分享第 22 期</a><br/>
4、 <a href="#4聊天机器人已死为什么腾讯还要打造自己的智能客服" >聊天机器人已死，为什么腾讯还要打造自己的智能客服？</a><br/>
5、 <a href="#5go-2将添加错误处理和泛型" >Go 2将添加错误处理和泛型</a><br/>
6、 <a href="#6gitopsweaveworks通过开发者工具实现ci/cd" >GitOps：Weaveworks通过开发者工具实现CI/CD</a><br/>
7、 <a href="#7microsoft正式发布azure-iot-hub与event-grid的集成" >Microsoft正式发布Azure IoT Hub与Event Grid的集成</a><br/>
8、 <a href="#8azure编配器简化有状态无服务器工作流的创建" >Azure编配器简化有状态无服务器工作流的创建</a><br/>
9、 <a href="#9jenkins将致力于提升稳定性易用性和云原生兼容性" >Jenkins将致力于提升稳定性、易用性和云原生兼容性</a><br/><h1 id="#title_0" >1、Celebrating 10 Years of the V8 JavaScript engine</h1>

[https://javascriptweekly.com/issues/403](https://javascriptweekly.com/issues/403)
<table border=0 align="center" border="0">
  <tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   ">

  <div>    
    <table border=0 border=0><tr>
<td align="left" style="padding-left: 4px; font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   "><p>#403 — September 14, 2018</p></td>
<td align="right" style="padding-right: 4px; font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   "><p></p></td>
</tr></table>
    
    <table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0 12px;  "><p>JavaScript Weekly</p></td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   ">
  
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — The V8 JavaScript engine has had a <em>huge</em> impact on the growth of JavaScript, taking it from being a relatively slow scripting language to something surpassing many other languages on performance. This post celebrates V8’s tenth anniversary with some details about its history and development.</p>
  <p>Mathias Bynens </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — How do you know if a new technology, tool, or library is worth investing time into? Sacha Greif considers 12 factors to consider including features, stability, community and momentum.</p>
  <p>Sacha Greif </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Take your JavaScript to the next level to find out what it is fully capable of with this comprehensive learning path.</p>
  <p>Frontend Masters <span style="text-transform: uppercase; padding: 1px 4px;  margin-left: 4px; font-size: 0.9em;   color: #997 !important;">sponsor</span></p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"> (formerly ‘crux’) is a new, experimental JavaScript package manager from the folks at npm, Inc, that aims to provoke new thoughts on how package management should be handled.</p>
  <p>The npm Blog </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"> is a popular date and time manipulation library but with some downsides around tree-shaking and mutability. But do you even need it? This repo shows off the alternatives, including many native functions that do similar things.</p>
  <p>Various Contributors </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — 3.1 two main additions are mappable tuple and array types plus properties on function declarations.</p>
  <p>Microsoft </p>
</td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0;  "><p>💻 Jobs</p></td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — The Digital Concert Hall team is looking for a passionate developer with strong focus on Javascript
</p>
  <p>Berliner Philharmoniker </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Build native apps for the world’s largest social network for expatriates in JavaScript. International team. </p>
  <p>InterNations </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Create a profile to connect with inspiring companies seeking JavaScript devs.</p>
  <p>Vettery </p>
</td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0;  "><p>📘 Articles &amp; Tutorials</p></td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Know what file-splitting strategy will work best for your site and your users.</p>
  <p>David Gilbertson </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — This cheat sheet could be useful to you in both directions, whether coming from Python or wanting to learn some.</p>
  <p>Saya </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Jez covers DevOps and its culture, cynicism on teams, and how to drive change slowly through organizations.</p>
  <p>CircleCI <span style="text-transform: uppercase; padding: 1px 4px;  margin-left: 4px; font-size: 0.9em;   color: #997 !important;">sponsor</span></p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — A complete, straightforward walkthrough, with code.</p>
  <p>Francis Cote </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></p>
  <p>Sashko Stubailo </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Watch us build Angular web, native iOS and Android apps connected to Cloud Data with 70% shared code.</p>
  <p>Progress <span style="text-transform: uppercase; padding: 1px 4px;  margin-left: 4px; font-size: 0.9em;   color: #997 !important;">sponsor</span></p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Web Workers are scripts that run in the background in separate threads and if you’ve not worked with them yet, this is a good primer.</p>
  <p>Dan Arias </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;">▶  .</p>
  <p>JavaScript Jabber <span style="text-transform: uppercase; margin-left: 4px; font-size: 0.9em;  padding: 1px 4px; ">podcast</span></p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Chris Coyier </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Test your JavaScript <code>==</code> equality knowledge with this quirky Minesweeper-esque game.</p>
  <p>slikts </p>
</td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0;  "><p>🔧 Code and Tools</p></td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Review and manage GitHub PRs directly from within VS Code.</p>
  <p>Kenneth Auchenberg (Microsoft) </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></p>
  <p>neonious GmbH </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Bitmovin <span style="text-transform: uppercase; padding: 1px 4px;  margin-left: 4px; font-size: 0.9em;   color: #997 !important;">sponsor</span></p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Matteo Basso </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Guess the language of a text, stemming/tokenization, sentiment analysis, etc.</p>
  <p>AXA </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Offers a new way to handle user data in React apps in a lazy-loading fashion.</p>
  <p>Nozbe </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Erik Brinkman </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Dogstudio </p>
</td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px;  ">

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
<p>🗓 <strong>Upcoming JavaScript Events</strong></p>

<ul>

<li>
 — Two day, four-track frontend developer event.</li>

<li>
 — A new two day conference focused on all front end frameworks with keynotes from the teams of the most popular ones.</li>

<li>
 — One of the largest JavaScript events. Organized by the Linux Foundation.</li>

<li>
 — A two-day, two-track, developer event focused on mobility and the cutting-edge JavaScript ecosystem.</li>

<li></li>

</ul>

</td></tr></table>
</td></tr></table>
<table border=0 border=0><tr><td style=" font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   "></td></tr></table>
</div>

  </td></tr>
</table>





<img src="https://javascriptweekly.com/open/403/rss" width="1" height="1" />
---------------
<h1 id="#title_1" >2、Monthly Web Development Update 9/2018: Native Lazy Loading And Imaginary Work</h1>
Anselm Hannemann
[https://www.smashingmagazine.com/2018/09/monthly-web-development-update-9-2018/](https://www.smashingmagazine.com/2018/09/monthly-web-development-update-9-2018/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/09/monthly-web-development-update-9-2018/" />
              <title>Monthly Web Development Update 9/2018: Native Lazy Loading And Imaginary Work</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>Monthly Web Development Update 9/2018: Native Lazy Loading And Imaginary Work</h1>
                  
                    
                    <address>Anselm Hannemann</address>
                  
                  <time datetime="2018-09-14T14:50:19&#43;02:00" class="op-published">2018-09-14T14:50:19+02:00</time>
                  <time datetime="2018-09-14T13:06:51&#43;00:00" class="op-modified">2018-09-14T13:06:51+00:00</time>
                </header>
                <p><p>It&#8217;s an interesting concept to <strong>compare JavaScript with CO2</strong> and yet a very valid one. Alex Russel who works for the Chrome team and has a lot of insights into the current state of the web says that using too much JavaScript or using it exclusively (without progressive enhancement/graceful degradation) will have the same effect as too much CO2 for the ecosystem on planet Earth &mdash; the ecosystem will fall apart. And just like we need a certain amount of CO2 to live, we need JavaScript on the web. It&#8217;s that fine line that makes the difference &mdash; the line between not too much and none at all.</p>
<p>I feel that with the native browser APIs that we have these days we have a fantastic opportunity to <strong>build great web services without bloating</strong> them too much and without relying only on JavaScript. We can enhance native elements with the Custom Elements API easily via ES6 Classes, with so little code that it seems ridiculous to build all that on your own in a third-party framework. Coincidentally, the Github engineering team published an article about  and what they now use instead: native JavaScript and small, lean code that is progressively enhancing their platform. Less code, better maintainability, and more stability.</p>
<h3>News</h3>
<ul>
<li>, bringing shape detection as an origin trial that allows us to perform QR code reading, face detection, and text recognition in images. The Web Authentication API got some updates, too, and <code>referrerpolicy</code> support was added to <code>&lt;script&gt;</code> elements. This version will also deprecate Custom Elements v0, HTML Imports, and Shadow DOM v0.</li>
<li>Finally, , Mozilla ships <code>::selection</code> instead of <code>:-moz-selection</code>. They also implemented <code>flat()</code>, and <code>flatMap()</code> for JavaScript arrays and developers get a new Shape Path Editor.</li>
<li>. Let&#8217;s see how that will evolve.</li>
<li>With , we finally have support in all major browsers and can use it widely now to improve performance, be more creative with typography, and reduce data traffic drastically.</li>
<li>Manuel Rego Casasnovas wrote about  in the Chrome browser.</li>
<li>Anyone who isn&#8217;t an expert would be hard-pressed to explain how tracking on the internet actually works. That&#8217;s why Firefox now changes their default settings and  .</li>
<li> with new Heredoc and Nowdoc syntax, trailing commas in function calls, <code>is_countable()</code>, <code>array_key_first()</code>, <code>array_key_last()</code>, and Argon2 password hash enhancements.</li>
</ul>


  <aside class="product-panel product-panel__tilted product-panel--book" data-audience="non-subscriber">
    <div class="container product-panel--book__container">
      <div class="panel__description panel__description--book">
    <p>Getting the process <em>just</em> right ain't an easy task. That's why we've set up <strong>'this-is-how-I-work'-sessions</strong> — with smart cookies sharing what works really well for them. A part of the , of course.</p>
      <a href="https://smashed.by/casestudypanelmembership" class="btn btn--green btn--large">
        Explore features&nbsp;→
      </a>
      </div>
      <div class="panel__image panel__image--book">
        <a href="https://smashed.by/casestudypanelmembership" class="books__book__image">
        <div class="books__book__img">
          <img src="https://www.smashingmagazine.com/images/smashing-cat/cat-scubadiving-panel.svg" alt="Smashing TV, with live sessions for professional designers and developers." width="310" height="400">
        </div>
      </a>
      </div>
    </div>
  </aside>



<h3>General</h3>
<ul>
<li>Alex Russell&#8217;s &#8220;&#8221; is a great piece that explains the toxic environments we currently build for the web and why JavaScript can be compared to CO2 &mdash; both are needed in small portions, but if there&#8217;s too much of it, it&#8217;ll put the entire ecosystem (the web) at risk. A thoughtful article that I recommend everyone here to read, share, and remember.</li>
<li>As Alexa, Cortana, Siri, and even customer support chat bots become the norm we have to start considering not only how our content looks but . We can &mdash; and should &mdash; use HTML and ARIA to make our content structured, sensible, and most importantly, meaningful.</li>
</ul>
<h3>Web Performance</h3>
<ul>
<li>The upcoming PostgreSQL 11 has some interesting performance improvements. Dimitri Fontaine .</li>
<li>Ben Schwarz shares new approaches to  that could become a reality soon.</li>
</ul>
<h3>Security</h3>
<ul>
<li>Nightwatch Cybersecurity published a  that exposes information about the user&#8217;s device to all applications running on it. This seems to include the WiFi network name, BSSID, local IP addresses, DNS server information, and the MAC address &mdash; all in all quite a lot of private information that allows people to track individual Android devices. Unfortunately, all Android OS versions including forks (except for Android P/9 where a fix was provided) seem to be affected with no plan to fix older versions.</li>
</ul>
<div class="sponsors__wide-place"></div>



<h3>CSS</h3>
<ul>
<li>Chen Hui Jing explains  without compromising their accessibility.</li>
<li>CSS Shapes have quite some history already. Brought to the web early by an initiative of the Adobe Web team, browser vendors removed the implementations soon again, and are now slowly coming back with iterated, improved specifications and implementations. .</li>
<li>Sara Soueidan wrote down the reasons she  and what the benefits are.</li>
<li>With the web&#8217;s growth come new features to better accommodate its new form factors and use cases. One feature I&#8217;m excited about is the , proposed in CSS Color Module Level 4. It is an acknowledgment that the web will continue to show up on devices that have less-than-stellar displays.</li>
</ul>
<figure>)</figcaption></figure>
<h3>HTML &amp; SVG</h3>
<ul>
<li>Stefan Judis read what the Mozilla documentation has to say about <code>input</code> elements and  that could be very useful for your next project.</li>
</ul>
<h3>JavaScript</h3>
<ul>
<li>Nolan Lawson  and when to use which.</li>
<li> is a tiny and elegant HTTP client based on the browser Fetch API.</li>
<li>Ankur Anand wrote an article about .</li>
<li>Adrian Roselli shares how we can .</li>
<li> is out. It&#8217;s faster, has more options, and supports JSX Fragments and TypeScript.</li>
<li>Auto-resizing <code>&lt;textarea&gt;</code>s is a very useful way to improve the user experience for people writing content for your site or service. I wrote a blog post about how to .</li>
</ul>
<h3>Accessibility</h3>
<ul>
<li>Ethan Marcotte  and realizes that it&#8217;s not about making a website compatible with some assistive technology or software but about making it usable for everyone who wants to access it, regardless of the technology. This is a huge difference because his approach includes people who have difficulties reading a website even though they use the same browser and the same laptop as you. Maybe they are in bright sunlight, have difficulties with small text, or get distracted by bright colors or animated elements.</li>
<li>Eric Bailey emphasizes .</li>
<li>Scott O&#8217;Hara shares a  to provide an accessible name and <code>aria-current</code> to indicate the currently active link.</li>
</ul>
<div class="sponsors__wide-place"></div>



<h3>Work &amp; Life</h3>
<ul>
<li>Ryan Singer contemplates  and why it&#8217;s so important to test first how hard something will be to integrate before planning it on the roadmap.</li>
</ul>
<figure>)</figcaption></figure>
<h3>Going Beyond&hellip;</h3>
<ul>
<li>I love the concept of doodling, and even though I don&#8217;t do it regularly, it always fascinates me.  is a platform that collects doodles from people all around the world. A nice gallery to get inspiration from.</li>
<li>Jonny Brooks-Bartlett wrote an interesting article on . The job might sound quite interesting and like a good bet these days, but often expectations don&#8217;t match reality and politics and ethical decisions are extremely difficult.</li>
<li>Marco Lambertini explains , but more than anything we need to learn to value nature and its resources.</li>
<li>An interesting discussion was raised this week by a very well-known Open Source contributor ) shows that more and more people think about the impact of their work. They don&#8217;t want it to be used for bad, but for good. And while the idea of open, non-restricted source is desirable, it&#8217;s only if people use it to support human rights and for improving lives. I&#8217;m curious about new solutions that could ensure this; maybe we&#8217;ll see more terms of service for open-source projects soon (which would then be legally binding but may prevent free open-source projects from using them).</li>
</ul>
<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(cm)</span>
</div>
</p>

              </article>
            </body>
          </html>
---------------
<h1 id="#title_2" >3、每周分享第 22 期</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2018/09/weekly-issue-22.html](http://www.ruanyifeng.com/blog/2018/09/weekly-issue-22.html)
<p>这里记录过去一周，我看到的值得分享的东西，每周五发布。</p>

        <p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018091401.jpg" alt="" title="" /></p>

<p>2008年，英国摄影师大卫·斯莱特（David Slater）来到印度尼西亚，拍摄一种珍贵的猕猴。他把照相机固定在三脚架上，放在丛林中，然后躲在远处偷偷观察猕猴。猴子很快发现了照相机，拿起来玩，居然真的按下了快门，留下了几张。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018091402.jpg" alt="" title="" /></p>

<p>2011年，大卫·斯莱特把这些照片发表在英国的《每日邮报》。几天以后，有人把它们上传到维基百科，版权归属设定为"公共领域"。理由很简单，照片的版权属于拍摄者，现在拍摄者是一只猴子，所以不存在版权。大卫·斯莱特抗议，认为他才是版权所有者，但是维基百科坚持不改。</p>

<p>事情到这里还没结束，大卫·斯莱特继续出售这些照片。2015年，美国的一个动物保护组织将他告上了法庭，称这些照片的版权属于那只猴子，不属于他。动物保护组织要求大卫·斯莱特停止侵权，并希望法院同意由他们代理版权收入，所有收入将用来保护这种猕猴和印度尼西亚的热带丛林。2016年，美国联邦法院裁决，猴子不拥有照片的版权。动物保护组织继续上诉，2018年，美国上诉法院维持原判。</p>

<p>注意，法院并没有认定，大卫·斯莱特拥有照片的版权，只是认为猴子没有版权。那么，非人类拍摄的照片或视频，是否属于公共领域，依然没有结论。维基百科上，这些照片的版权标注是公共领域，直到今天还是如此。</p>

<p>如果只有人类拍摄的照片才拥有版权，那么机器人拍摄的照片，版权属于谁呢？进一步说，那些马路边的探头，24小时自动拍摄，也不能算是人类的作品，那么监控视频的版权是否也属于公共领域呢？</p>

<h2>新闻</h2>

<p>1、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018091403.jpg" alt="" title="" /></p>

<p>输血需要识别血型，O 型血是全能血，可以给其他血型输血，别的血型都不行。现在，加拿大科学家发现一种特殊类型的肠道细菌可以去除人体血液中的抗原，使任何血型都变成O型血。也就是说，解决了输血血型不匹配的问题。</p>

<p>2、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018091404.jpg" alt="" title="" /></p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018091405.jpg" alt="" title="" /></p>

<p>过滤装置都是让较小的颗粒通过，拦截较大的颗粒。现在，科学家做出了反向过滤的膜，让较大的颗粒通过，拦截较小的颗粒。</p>

<p>它是一种十二烷基硫酸钠和水制成的透明液体膜，利用了液体的表面张力。较大的物体有较大的动能，能够突破表面张力，较小的物体就做不到。这种膜可以用来拦截小分子，比如用作手术膜，防止灰尘落入伤口，或者用作马桶膜捕获异味。</p>

<p>3、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018091406.jpg" alt="" title="" /></p>

<p>挪威正在建造的 YARA Birkeland 货轮，是世界第一艘无人驾驶、自主航行的货轮。由于国际航运法规定，远洋船舶必须有船员，因此无人驾驶船舶不得进入国际水域。所以，这艘货轮只能在挪威国内开展业务。不过，联合国国际海事组织可能改变目前的规定。</p>

<p>2016年欧洲海事安全局统计发现，全球（2011-2015）发生的880起事故有62％是由"人为错误"引起的。因此，无人货轮不仅可以节省成本，还有利于减少事故。</p>

<p>4、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018091407.jpg" alt="" title="" /></p>

<p>巴西里约热内卢博物馆是美洲最大的博物馆之一，9月2日晚上发生大火。由于火灾发生在闭馆后，目前没有发现人员伤亡。</p>

<p>这家博物馆有2000多万件藏品，最珍贵的是一个1.2万年前的人类化石，那是美洲发现最早的人类。火灾损失还无法估计，知情人士透露，博物馆被彻底摧毁了，大部分藏品都烧掉了。该博物馆建于1818年，1892年改为博物馆。</p>

<p>一个巴西人网上：</p>

<blockquote>
  <p>"我在2013年参观了这家博物馆。博物馆距离马拉卡纳体育场大约半英里，一年后就要举办巴西世界杯，体育场正在花费3亿美元更新，而博物馆的经费来自里约热内卢大学的拨款，大约是15万美元。"</p>
</blockquote>

<p>5、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018091408.jpg" alt="" title="" /></p>

<p>每年冬天，候鸟都会沿着相同的路线迁移。它们为什么知道路线，不会迷失方向？很多科学家猜测，候鸟能够感知地球的磁场，最近的研究证实了这个猜测。</p>

<p>科学家发现，鸟类眼中有一种蛋白质Cry4，这种蛋白质可以感受蓝光。地球磁场的电磁波，会导致某些波长的光被鸟类看见，也就是说，鸟类可以看见磁场。</p>

<p>6、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018091409.jpg" alt="" title="" /></p>

<p>无人飞行器的一个缺点就是太耗电，一块电池只能支持不到30分钟。美国军方正在研制一种无限飞行的无人机，解决方法就是激光充电。激光打中无人机，无人机里面的光伏设备再将激光转换为电能，储存在电池里面。</p>

<p>7、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018091410.jpg" alt="" title="" /></p>

<p>有些狗主人遛狗的时候，不清除狗屎，影响环境。意大利一个小镇忍无可忍，对本地2,156只狗的 DNA 全部登记。一旦发现没清理的狗屎，就追查DNA，对主人罚款58美元。</p>

<p>8、</p>

<p>《纽约时报》发表了一封匿名来信，作者是特朗普总统身边的高官。来信说，他为了美国的利益，潜伏在总统身边，让总统的很多错误决定无法执行。</p>

<p>有个程序员在 GitHub 公布了一个脚本，将这封来信与每个内阁成员的推特进行对比，求出相关系数，运行结果是副总统的相关系数最高。</p>

<p>9、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018091411.jpg" alt="" title="" /></p>

<p>Windows 10 最新的内部测试版，会拦截 Chrome 和 Firefox 的安装，提醒你已经安装了 Edge，不需要别的浏览器了。用户坚持的话，还是可以继续安装。</p>

<p>10、<strong>一句话新闻</strong></p>

<ul>
<li>发现一种方法，利用酶和一些化学品的混合物，只用阳光就将水分解为氢气和氧气。这为生产和储存能量带来了新的方法。</li>
<li>11个科研管理机构和基金会联合宣布了"S计划"，凡是接受这些机构资助的科研项目，所产生的论文必须让公众免费获取，不得收费。一些科研杂志说，这会导致这些杂志关门。</li>
<li>将在明年上半年发售电动轿车，挑战特斯拉在高端电动车市场的独占地位。</li>
</ul>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018091412.jpg" alt="" title="" /></p>

<h2>教程</h2>

<p>1、（英文）</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018091413.jpg" alt="" title="" /></p>

<p>本文介绍大型网站架构的基本知识。</p>

<p>2、（英文）</p>

<p>Go v1.11 引入了模块（module）的概念，主要为了使用语义版本，解决依赖升级的兼容性问题。</p>

<p>3、（英文）</p>

<p>"about: "开头的网址，返回与浏览器本身相关的内容，最常用就是空网址 <code>about: blank</code> ，以及 <code>about:history</code> 。</p>

<p>4、（英文）</p>

<p>.ipynb 文件是一种在网页上运行的代码运行时，可以实时看到运行结果，支持40多种语言的运行，包括 Python，R，Julia 和 Scala。它是由 Jupyter  Notebook 生成的，本文介绍5种支持 Jupyter 的云服务。</p>

<p>5、（英文）</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018091414.jpg" alt="" title="" /></p>

<p>跨平台桌面应用一般用 Electron 开发，打包体积很大。对于纯静态应用，其实有另一种轻量级选择。</p>

<p>操作系统都有自己的 Webview，Mac 是 webview，Windows 是 MSHTML，Linux 是 gtk-webkit2。这篇文章教你怎么用 Webview，开发一个跨平台的桌面打飞机游戏。</p>

<p>6、（英文）</p>

<p>大部分情况下，我们使用市场上现有的 CDN 服务。但是，你也可以自己搭一个，这篇文章教你怎么做。</p>

<p>7、（英文）</p>

<p>作者原来是一个 Java 开发者，后来转为使用 Node。他比较了这两种语言。</p>

<p>8、（英文）</p>

<p>WordPress 是常用的博客软件，虽然方便易用，但是容易产生安全问题。作者提供了一个脚本，可以将 WordPress 网站的 HTML 页面，部署到 Gitlab Pages 服务，做成一个静态网站。 </p>

<p>9、（英文）</p>

<p>WireGuard 内部实现原理的一些介绍，以及与现有方案的比较。</p>

<p>10、（英文）</p>

<p>Serverless 作为服务导向架构的一种形式，有很多优点。本文介绍了使用这种架构时，应该注意的问题。</p>

<h2>资源</h2>

<p>1、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018091415.jpg" alt="" title="" /></p>

<p>Windows 2000 通过 WebAssembly，可以在浏览器里运行了。</p>

<p>2、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018091416.jpg" alt="" title="" /></p>

<p>《数据挖掘》（第二版）这本书本身没有全部开源，这个网页提供了所有章节的 PPT 教辅材料和实验代码。</p>

<p>3、</p>

<p>开源教材，以 Julia 语言的教学，讲解计算机科学的基本概念和原理。</p>

<p>4、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018091417.jpg" alt="" title="" /></p>

<p>Windows 95 被做成了一个 Electron App，可以用来玩 DOS 游戏，底层是 x86 的JS虚拟机。</p>

<p>5、</p>

<p>开源电子书，介绍 App 发布到应用商店，怎样才能取到满意的结果。</p>

<h2>工具</h2>

<p>1、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018091418.jpg" alt="" title="" /></p>

<p>Slack 是目前最流行的团队协同通信工具。这篇文章列出了25种 Slack 的替代品。</p>

<p>2、</p>

<p>Wireguard 的自动化安装脚本。</p>

<p>3、</p>

<p>网页上的 Python 运行环境。</p>

<p>4、</p>

<p>Chrome 插件，可以将用户在浏览器里面的操作，自动生成对应的 Puppeteer 脚本。</p>

<p>5、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018091419.jpg" alt="" title="" /></p>

<p>有人用 JS 写了一个 C++ 的解释器，可以在 Node 或浏览器直接运行 C++ 代码。</p>

<p>6、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018091420.jpg" alt="" title="" /></p>

<p>cron 是设置 Linux 系统定时任务的工具，只能在命令行下使用。现在，这个软件为它提供了图形界面。</p>

<p>7、</p>

<p>一个 webassembly 的 GIF 图片解析库，性能较好。另外还有一个 JS 的 GIF 解析库 ，用法较友好。</p>

<p>8、</p>

<p>bat 是 cat 命令的加强版，同样在命令行输出文件内容，但是带有高亮和分页，并且与 Git 集成。</p>

<p>9、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018091421.jpg" alt="" title="" /></p>

<p>Picular 会抓取谷歌的图片搜索结果，提取并显示每张图片的主要颜色。上图是搜索"夏天"的颜色</p>

<h2>文摘</h2>

<p>1、</p>

<p>1988年的夏天，一位名叫 Wes Cherry 的大学生在微软担任实习生。为了搞懂 Windows，他决定改写 Macintosh 电脑的一个纸牌游戏，写出一个 Windows 版本。根据 Cherry 本人的说法，他写的游戏代码"没有什么特别之处"，并不比其他纸牌游戏更好。对他来说，这个软件最特别之处仅仅在于，纸牌背面的图案由他的女友 Leslie Kooy 绘制。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018091422.jpg" alt="" title="" /></p>

<p>被问到开发这个游戏最困难的是什么，他说是游戏胜利后纸牌不断弹跳的场景。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018091423.jpg" alt="" title="" /></p>

<p>暑期实习结束时，他将自己的纸牌游戏放在一个微软内部的服务器上，然后又回到了大学。</p>

<p>几个月后，微软的一位产品经理发现了这个游戏。当时，微软已经开始寻找即将推出的 Windows 3.0 的内置游戏，他们决定把这个纸牌游戏放进去。对这个游戏进行了测试之后，他们让 Wes Cherry 解决发现的各种错误，报酬是一台全新的计算机。</p>

<p>1990年5月，Windows 3.0发布时，纸牌游戏包括在内。这个游戏很快就风靡全球，成为人们最常玩的电脑游戏，直到今天还是如此。微软很快就宣布，它是"最常用"的 Windows 应用程序。全世界办公室的咖啡时间和休息时间，都有人在玩这个游戏。1994年，华盛顿邮报的一篇文章半开玩笑地说，这个游戏正在播下"美国资本主义崩溃"的种子。2007年芬兰的一项研究发现，它是36％的女性和13％的男性最喜欢的游戏，没有其他任何游戏接近这些数字。</p>

<p>Wes Cherry 是上班时间在微软办公室开发这个游戏，因此知识产权属于微软。他创造了历史上最受欢迎的电脑游戏，但是除了一台免费电脑之外，他从来没有得到任何报酬。他说他不介意。他早已离开计算机行业，现在西雅图附近的 Vashon 岛拥有并经营一家。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018091424.jpg" alt="" title="" /></p>

<p>2、</p>

<p>用户阅读网页内容的热力图是下面这样。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018091425.jpg" alt="" title="" /></p>

<p>这就是说，用户以 F 状的方式阅读网页，先看前三行，然后垂直向下阅读，只看每一行的前几个字。</p>

<p>所以，写作的时候，应该注意下面几点。</p>

<blockquote>
  <ul>
<li>第一段和第二段必须给出最重要的信息，而且第一句话最重要。</li>
<li>标题、段落、列表的开头，都应该立即给出信息。</li>
<li>通过字型的变化（大小、黑体、链接），把用户的注意力吸引到重点句子。</li>
</ul>
</blockquote>

<h2>本周图片</h2>

<p>1、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018091426.jpg" alt="" title="" /></p>

<p>动画片《辛普森一家》的主角荷马，被人做成现实生活里的样子。</p>

<p>2、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018091427.jpg" alt="" title="" /></p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018091428.jpg" alt="" title="" /></p>

<p>上个世纪70年代，美国家居用品零售商 Best Products 店铺都采用废弃式的设计，看上去建筑物未完工或已经废弃了，但实际上是正常使用的。</p>

<p>3、</p>

<p>1956年，英国通过《清洁空气法案》，要求减少空气污染。在此之前，曼彻斯特很多建筑物都被煤烟熏黑了。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018091429.jpg" alt="" title="" /></p>

<p>《曼彻斯特晚报》将一些建筑物的历史照片与今天的照片做了对比。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018091430.jpg" alt="" title="" /></p>

<h2>新奇</h2>

<p>1、</p>

<p>联想新发布的10.8寸笔记本 Yoga Book C930 ，键盘是一块 E-ink 电子墨水屏，可以当作第二块屏幕。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018091431.jpg" alt="" title="" /></p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018091432.jpg" alt="" title="" /></p>

<p>使用手写笔的时候，副屏就是一个手写输入板；当作键盘使用的时候，则会有触觉反应。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018091433.jpg" alt="" title="" /></p>

<h2>本周金句</h2>

<p>1、</p>

<p>我把许可证授予 IBM、它的顾客、合作者和下属公司，允许他们使用 JSLint 做坏事。</p>

<p>-- 写着："这个软件只能用于善事，不得用于邪恶"。由于善和恶的含义很难准确定义，IBM 公司的律师要求找到开发者 Douglas Crockford 要求给予 IBM 特别许可，Douglas Crockford 就在许可证里面加了上面一行。</p>

<p>2、</p>

<p>我们购买任何商品时，支付价格不包括商品的全部成本。我们没有支付商品回收处理的成本，也没有支付修复环境的成本，更没有支付应对生产过程中排放的二氧化碳的成本。换句话说，每一件商品里面都包含后代支付给我们的大量补贴。</p>

<p>-- 对各国政府没有有效控制温室气体的评论</p>

<p>3、</p>

<p>沟通不是一件好事。</p>

<p>---- 亚马逊内部会议上，有人提议改善各个小组之间的沟通，贝佐斯做了上面的回答。他认为，随着人数的增加，点对点沟通的成本巨大，而且会导致混乱。他希望每个小组都尽量小，保证内部沟通有效。小组对外提供定义良好的接口，可以从接口上拿到所有信息，尽量消除直接沟通的必要。</p>

<h2>欢迎订阅</h2>

<p>这个专栏每周五发布，同步更新在我的。</p>

<p>微信搜索"<strong>阮一峰的网络日志</strong>"或者扫描二维码，即可订阅。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2018/bg2018042311.jpg" alt="" title="" /></p>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2018-09-14T08:42:26+08:00">2018年9月14日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>文集：</li>
<li>社交媒体：</li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------
<h1 id="#title_3" >4、聊天机器人已死，为什么腾讯还要打造自己的智能客服？</h1>
Natalie
[http://www.infoq.com/cn/news/2018/09/Chat-robot-dead-Why-Tencent-cust?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/09/Chat-robot-dead-Why-Tencent-cust?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>都说聊天机器人已死，他却认为市场潜力仍未被开发</p> <i>By Natalie</i>
---------------
<h1 id="#title_4" >5、Go 2将添加错误处理和泛型</h1>
Sergio De Simone
[http://www.infoq.com/cn/news/2018/09/go-2-draft-designs?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/09/go-2-draft-designs?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>在Gophercon 2018大会上，Russ Cox介绍了将添加到Go 2的特性，包括错误处理和泛型，并透露了当前一些新特性提案的内容。</p> <i>By Sergio De Simone</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_5" >6、GitOps：Weaveworks通过开发者工具实现CI/CD</h1>
Daniel Bryant
[http://www.infoq.com/cn/news/2018/09/gitops-weaveworks?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/09/gitops-weaveworks?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>在过去的一年中，Weaveworks团队逐步改进了有关“GitOps”实践的想法。“GitOps”是指他们通过开发者工具来推动运营和实现持续交付。</p> <i>By Daniel Bryant</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_6" >7、Microsoft正式发布Azure IoT Hub与Event Grid的集成</h1>
Steef-Jan Wiggers
[http://www.infoq.com/cn/news/2018/09/azure-iothub-eventgrid-ga?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/09/azure-iothub-eventgrid-ga?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>在经历为期六个月的公开预览后，微软宣布正式发布IoT Hub与Azure Event Grid的集成。组合使用两者可以提高对客户设备事件的支持，实现数据库更新、工单（ticket）创建和定价管理等操作的自动化。</p> <i>By Steef-Jan Wiggers</i> <i> Translated by 盖磊</i>
---------------
<h1 id="#title_7" >8、Azure编配器简化有状态无服务器工作流的创建</h1>
Sergio De Simone
[http://www.infoq.com/cn/news/2018/09/azure-durable-function-intro?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/09/azure-durable-function-intro?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Azure Durable Functions旨在通过引入编排器function概念来定义更复杂的工作流，以此来扩展无服务器计算范式。如果你曾经想过要使用它们，微软刚刚发布了一个示例，帮助开发人员开始他们的无服务器计算和编排器function之旅。</p> <i>By Sergio De Simone</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_8" >9、Jenkins将致力于提升稳定性、易用性和云原生兼容性</h1>
Hrishikesh Barua
[http://www.infoq.com/cn/news/2018/09/jenkins-stability-cloud-native?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/09/jenkins-stability-cloud-native?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Jenkins项目团队决定在稳定性和为Kubernetes等平台提供更好的支持方面分配一些工作量。前者可能会发生一些向后不兼容的变更，将影响发布模型并提供具有更多预置选项的版本，而后者将在与现有Jenkins X项目齐头并进。</p> <i>By Hrishikesh Barua</i> <i> Translated by 无明</i>
---------------