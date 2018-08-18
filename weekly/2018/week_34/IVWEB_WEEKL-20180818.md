## 文章索引
1、 <a href="#1monthly-web-development-update-8/2018:-the-cost-of-javascript-ethics-in-open-source-and-quic" >Monthly Web Development Update 8/2018: The Cost Of JavaScript, Ethics In Open Source, And QUIC</a><br/>
2、 <a href="#2designing-for-micro-moments" >Designing For Micro-Moments</a><br/>
3、 <a href="#3coinbase是如何在其加密货币交易平台上应对扩展性挑战的" >Coinbase是如何在其加密货币交易平台上应对扩展性挑战的</a><br/>
4、 <a href="#4universal-windows-platformuwp应用的窗口特性" >Universal Windows Platform（UWP）应用的窗口特性</a><br/>
5、 <a href="#5软件领域的作家导师兼咨询师杰里·温伯格去世" >软件领域的作家、导师兼咨询师杰里·温伯格去世</a><br/>
6、 <a href="#6新的uwp和win32应用程序分发模型" >新的UWP和Win32应用程序分发模型</a><br/>
7、 <a href="#7kyle-simpson-charting-libraries-and-an-interview-with-dr-axel-rauschmayer" >Kyle Simpson, charting libraries, and an interview with Dr. Axel Rauschmayer</a><br/><h1 id="#title_0" >1、Monthly Web Development Update 8/2018: The Cost Of JavaScript, Ethics In Open Source, And QUIC</h1>
Anselm Hannemann
[https://www.smashingmagazine.com/2018/08/monthly-web-development-update-8-2018/](https://www.smashingmagazine.com/2018/08/monthly-web-development-update-8-2018/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/08/monthly-web-development-update-8-2018/" />
              <title>Monthly Web Development Update 8/2018: The Cost Of JavaScript, Ethics In Open Source, And QUIC</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>Monthly Web Development Update 8/2018: The Cost Of JavaScript, Ethics In Open Source, And QUIC</h1>
                  
                    
                    <address>Anselm Hannemann</address>
                  
                  <time datetime="2018-08-17T11:57:10&#43;02:00" class="op-published">2018-08-17T11:57:10+02:00</time>
                  <time datetime="2018-08-17T12:41:01&#43;00:00" class="op-modified">2018-08-17T12:41:01+00:00</time>
                </header>
                <p>Building technology and software has become a very responsible job. People trust the products we create, and they can have a significant impact on their lives, too. Considering this, we not only need to think about inclusive solutions, but also stand up and advocate for ethics, reliability, and security. It’s a position that gives us power.</p>

<p>Eric Meyer published an article elaborating the problems which an HTTPS-only web is bringing along. In it, ” in which he points out one of the biggest problems we have as developers: We use privileged hardware and infrastructure. We build experiences using the latest iPhones, Macbooks with Gigabit or fast 4G connections but never consider that most people we’re building for use devices and infrastructures that are far from being that well-equipped. Making the web more secure is a great idea, beyond question, but we should also keep in mind the consequences that the latest tech and our design decisions might have for others.</p>

<h3>News</h3>

<ul>
<li> with a couple of convenient language features and fixes.</li>
<li>Implemented in Chrome since quite a while already, Client Hints are an amazing feature. To improve privacy, . Colin Bendell explains the differences and why Client Hints are so useful for performance.</li>
<li>Developers have been asking a lot about Safari’s Intelligent Tracking Prevention (ITP) and how to debug websites with it enabled. Now  which gives you a lot more flexibility and tools to track down issues.</li>
<li>Starting in October,  and, thus, block access to websites which still use them. Please update your certificate if you haven’t already.</li>
<li>The latest version of Chrome (68) brings a new  are the new Page Lifecycle API, a great new API for page events, as well as the Payment Handler API. HTTP cache is now ignored when requesting updates to a service worker, bringing Chrome in line with the spec and other browsers. Apart from that, the <code>cursor</code> values <code>grab</code> and <code>grabbing</code> are now unprefixed in the new version — finally.</li>
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




<h3>General</h3>

<ul>
<li>If you’re building for Open Source, you need to decide which license your project should use. Now there’s a new option, the . It’s for developers who “agree in general with the principles of open source software but are uncomfortable with their software being used as part of efforts to destroy lives, our environment and our future”.</li>
<li>Deep-learning machines are a big topic these days, but some people are exploring even .</li>
<li>Drew DeVault’s “” is a great reminder to set priorities straight in web and software development.</li>
<li>Jonathan Fulton wrote a handy resource called “”, which is a great web architecture 101 and foundation for newcomers in our industry.</li>
</ul>

<h3>UI/UX</h3>

<ul>
<li> is a project where twelve designers and researchers from eight European cities discuss the, sometimes harmful, impact of design on our societies and what designers can do to work for the good of all and not just a few.</li>
</ul>

<h3>Tooling</h3>

<ul>
<li>Prashant Palikhe wrote a long story about , which I can highly recommend as it’s a very complete reference to get to know the developer tools of a browser. If you use another browser, that’s not a big problem as most tools are quite similar.</li>
<li>WebP is an image format with a couple of nice features and likely one of the best-known new formats besides the common JPEG/PNG ones. However, creating WebP images can still be a challenge, so .</li>
<li> which allows you to instruct user agents to collect the same set of information that would appear in your server logs.</li>
<li>Many of us are addicted to communication tools like Slack. The folks from Wildbit decided to  — with a significant effect on how they work. An interesting case study about how we tend to get too comfortable with a useful tool and don’t use it as we should anymore. From time to time, it’s important to reset our minds.</li>
<li>Dennis Reimann published the first stable version of , a workbench for UI-driven development.</li>
</ul>

<h3>Security</h3>

<ul>
<li>A new Observer is around:  lets you know when your site uses a deprecated API or runs into a browser intervention. So far, it’s available in Chrome 69. You could easily use this to send errors that previously were only available in the Console to your backend or error handling service.</li>
</ul>

<h3>Web Performance</h3>

<ul>
<li>Do you remember QUIC (Quick UDP Internet Connections)? The protocol engineered by Google that they use internally and that is shaping up quite well for larger use? While the IETF is currently standardizing the format towards the end of the year, .</li>
</ul>
<figure>)</figcaption></figure>
<h3>HTML &amp; SVG</h3>
<ul>
<li>When you have user-generated content, you often don’t know if you have just one element or a list of elements to output. At Colloq, we wanted to do semantics right and , otherwise a <code>ol</code>/<code>ul</code> list with various list items.</li>
</ul>

<h3>Accessibility</h3>

<ul>
<li>Dave Rupert shares the , a project that attempts to digest and simplify the accessibility expectations when it comes to component authoring.</li>
<li>Skip links are quite common accessibility features. Hampus Sethfors now wrote an article on .</li>
</ul>

<h3>JavaScript</h3>

<ul>
<li>One year after they introduced their Progressive Web App, Zack Argyle from the Pinterest engineering team . It’s important to note why they decided to build a PWA: “Our mobile web experience for people in low-bandwidth environments and limited data plans was not good”. But the results for them are amazing to see.</li>
<li>Philip Walton  which helps us determine page states in the browser more easily via events, such as the page being in the background (not visible), active, frozen or even terminated.</li>
<li>Whoops, you all know <code>eval()</code> in JavaScript is bad, right? That’s why we usually forbid its usage in Content Security Policies. But Remy Sharp reminds us that .</li>
<li>Addy Osmani researched  and now shares evidence that every byte of JavaScript is still the most expensive resource we can send to mobile phones because it can delay interactivity significantly. This is a problem especially for not so capable phones that are widely used outside the tech industry.</li>
<li>Hidde de Vries explains .</li>
</ul>

<figure>)</figcaption></figure>

<h3>CSS</h3>

<ul>
<li>Max Böck explored a few CSS Grid techniques .</li>
<li>Sara Soueidan explains how we can  with modern HTML and CSS.</li>
<li>Jen Simmons shares .</li>
<li>Ethan Marcotte  that we mostly use for CSS Grids.</li>
</ul>

<div class="sponsors__wide-place"></div>




<h3>Work &amp; Life</h3>

<ul>
<li>Paris Marx wrote about why he thinks . He argues that location independence is only possible because of communication infrastructures built with public funds and that it’s not fair to abuse them.</li>
<li>This week I learned how useful it can be to think outside the box and .</li>
<li>It’s not the first time a company . However, it’s great to see how the concept can be established successfully and with benefits for both — the employees <em>and</em> the work done.</li>
</ul>

<h3>Going Beyond…</h3>

<ul>
<li>Tobias van Schneider wrote about why the Sagmeister-Walsh studio is so successful by staying small and .</li>
<li>Ben Werdmüller shares his thoughts on how different it has become to start a business when you’re, for example, in San Francisco. This is  and how this limits ideas.</li>
<li>Jeremy Nagel makes us think about the : As developers we tend to believe that making our code freely available is an amazing move but we forget that we make it available to bad players as well — to coal miners, to pollution-contributing companies, to those who use people to get rich while mistreating them, to those who rip you off indirectly. It’s not that you can’t do anything about it; you have to be aware of these issues and apply a better license or add a dedicated statement to your code.</li>
<li>India has a big plastic waste problem. Since a couple of months, a  but collect all the waste in their nets instead, and bring it back to the shore where it’s used to build roads. A great idea of making use of trash efficiently.</li>
</ul>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(cm)</span>
</div>


              </article>
            </body>
          </html>
---------------
<h1 id="#title_1" >2、Designing For Micro-Moments</h1>
Suzanna Scacca
[https://www.smashingmagazine.com/2018/08/designing-for-micro-moments/](https://www.smashingmagazine.com/2018/08/designing-for-micro-moments/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/08/designing-for-micro-moments/" />
              <title>Designing For Micro-Moments</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>Designing For Micro-Moments</h1>
                  
                    
                    <address>Suzanna Scacca</address>
                  
                  <time datetime="2018-08-17T13:50:09&#43;02:00" class="op-published">2018-08-17T13:50:09+02:00</time>
                  <time datetime="2018-08-17T12:41:01&#43;00:00" class="op-modified">2018-08-17T12:41:01+00:00</time>
                </header>
                <p>A couple of years ago, Google announced a new mobile-first initiative it wanted web designers and marketers to pick up on. This was our introduction to <strong>micro-moments</strong>.</p>

<p>These are not to be confused with micro-interactions, which are miniscule engagements websites have with visitors when they "touch" key points of the interface. A mouse changes its appearance when a user hovers over a clickable element. A display error appears after a field is incorrectly populated. A checkbox briefly enlarges and changes color after it’s been ticked off. These are micro-interactions.</p>

<p>A micro-moment, however, originates with your visitor. In Myriam Jessier’s "", she sums up Google’s four micro-moments:</p>

<ol>
<li>“I want to know.”</li>
<li>“I want to go.”</li>
<li>“I want to do.”</li>
<li>“I want to buy.”</li>
</ol>

<p>Basically, these are four key moments in every consumer’s life when they decide to pick up their mobile device for a specific purpose. As such, it’s your job to know how to specifically design for these micro-moments.</p>

<p><strong>Recommended reading</strong>: <em></em></p>

<h3>How You Should Be Designing For Micro-Moments</h3>

<p>When a visitor arrives at a mobile website (or app), they’ve come with a clear motivation:</p>

<ol>
<li>“I want to know.”</li>
<li>“I want to go.”</li>
<li>“I want to do.”</li>
<li>“I want to buy.”</li>
</ol>

<p>Seems pretty simple, right? However, as Google launched this initiative a couple of years ago, its had time to quietly observe users in these micro-moments as well as the websites that have most aptly responded to them. As you will soon see, consumers have incredibly high expectations for what the mobile web can do for them. Basically, they want you to be a mind reader and anticipate their every need (and even their location) without them having to say a word.</p>



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








    









<p>Is that intimidating? It shouldn’t be. You already have all the information you’d ever need to answer that question.</p>

<p>Here is how you should be designing your mobile website to respond to and draw in consumers as they experience these micro-moments:</p>

<h4>1. Start With The Data</h4>

<p> will help you decipher where they’re spending the most time productively on your website.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/046157f3-d6eb-4deb-b7bb-2c172f4d37ea/google-analytics-pages.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/046157f3-d6eb-4deb-b7bb-2c172f4d37ea/google-analytics-pages.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/046157f3-d6eb-4deb-b7bb-2c172f4d37ea/google-analytics-pages.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/046157f3-d6eb-4deb-b7bb-2c172f4d37ea/google-analytics-pages.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/046157f3-d6eb-4deb-b7bb-2c172f4d37ea/google-analytics-pages.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/046157f3-d6eb-4deb-b7bb-2c172f4d37ea/google-analytics-pages.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/046157f3-d6eb-4deb-b7bb-2c172f4d37ea/google-analytics-pages.png"
			sizes="100vw"
			alt="Google Analytics Behavior breakdowns"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			An example of Google Analytics’ visitor behavior breakdowns. (Source: )
		</figcaption>
	
</figure>


<p> will tell you which keywords are most effective in driving high-quality leads to the site.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/04787bda-ff58-4fc5-bf97-960ba1b25c3e/google-search-console-keywords.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/04787bda-ff58-4fc5-bf97-960ba1b25c3e/google-search-console-keywords.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/04787bda-ff58-4fc5-bf97-960ba1b25c3e/google-search-console-keywords.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/04787bda-ff58-4fc5-bf97-960ba1b25c3e/google-search-console-keywords.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/04787bda-ff58-4fc5-bf97-960ba1b25c3e/google-search-console-keywords.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/04787bda-ff58-4fc5-bf97-960ba1b25c3e/google-search-console-keywords.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/04787bda-ff58-4fc5-bf97-960ba1b25c3e/google-search-console-keywords.png"
			sizes="100vw"
			alt="Google Search Console keywords"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			An example listing of keywords and associated clicks and impressions for a website. (Source: )
		</figcaption>
	
</figure>


<p>Once you know where exactly visitors see the greatest value in your product, you can then turn to third-party tools like  to give you some insights into what relevant questions your users may be asking about you.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dffd4f2f-c199-4a2a-bca4-b7da747cabe3/answer-the-public-answers.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dffd4f2f-c199-4a2a-bca4-b7da747cabe3/answer-the-public-answers.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dffd4f2f-c199-4a2a-bca4-b7da747cabe3/answer-the-public-answers.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dffd4f2f-c199-4a2a-bca4-b7da747cabe3/answer-the-public-answers.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dffd4f2f-c199-4a2a-bca4-b7da747cabe3/answer-the-public-answers.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dffd4f2f-c199-4a2a-bca4-b7da747cabe3/answer-the-public-answers.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dffd4f2f-c199-4a2a-bca4-b7da747cabe3/answer-the-public-answers.png"
			sizes="100vw"
			alt="Answer the Public sample answers"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			An example of how Answer the Public provides micro-moment answers. (Source: )
		</figcaption>
	
</figure>


<p>Ultimately, this data needs to tell you all about your customers’ journey before they ever reach you. What exactly was the question that triggered them to pick up their smartphone and do that search? If you can identify those micro-moments, you can start using various design elements to respond to these questions.</p>

<h4>2. Respond With Immediacy</h4>

<p>:</p>

<blockquote>People are searching at the exact moment they need something and are looking for places that can meet their immediate need. In other words, when making these on-the-spot decisions, they are more loyal to their need than to any particular place.</blockquote>

<p>Although we’ve heard a lot about customer loyalty to brands in the past, it’s interesting to get Google’s take on this matter.</p>

<p>While consumers may indeed still remain loyal to brands that take very good care of them and produce a high-quality product nearly 100% of the time, this opportunity to steal attention from those customers in one of their micro-moments is real. Do that enough times and your brand and website could realistically win that customer over so long as you are there every time they go searching to fill that need.</p>

<p>One of the ways you can do this is by providing users with instant solutions. Is your business open now? Can you mail out that new product same-day? Will there be an open table at your restaurant tonight? Answer that immediately and you could find conversions increase dramatically.</p>

<p>Take the  website, for example.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ee9cf344-55a7-4f61-870f-6dd0e34de511/de-state-fair.PNG">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ee9cf344-55a7-4f61-870f-6dd0e34de511/de-state-fair.PNG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ee9cf344-55a7-4f61-870f-6dd0e34de511/de-state-fair.PNG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ee9cf344-55a7-4f61-870f-6dd0e34de511/de-state-fair.PNG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ee9cf344-55a7-4f61-870f-6dd0e34de511/de-state-fair.PNG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ee9cf344-55a7-4f61-870f-6dd0e34de511/de-state-fair.PNG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ee9cf344-55a7-4f61-870f-6dd0e34de511/de-state-fair.PNG"
			sizes="100vw"
			alt="Delaware State Fair gives users what they need to know"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The top of the Delaware State Fair home page gives users easy access to everything they want to know and do. (Source: )
		</figcaption>
	
</figure>


<p>Look at the top of the homepage. There are the dates of the fair, which probably answer one of the most commonly searched questions. There is a link to the concert lineup as well as calendar, which answers anything people would want to know about special events they might want to go to. And then there’s a button to buy tickets right away. It’s all right there.</p>

<p> is a company that also explicitly addresses immediate needs:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6b3eedd5-0a8a-4a45-b383-0bb396f0610e/office-depot-home.PNG">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6b3eedd5-0a8a-4a45-b383-0bb396f0610e/office-depot-home.PNG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6b3eedd5-0a8a-4a45-b383-0bb396f0610e/office-depot-home.PNG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6b3eedd5-0a8a-4a45-b383-0bb396f0610e/office-depot-home.PNG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6b3eedd5-0a8a-4a45-b383-0bb396f0610e/office-depot-home.PNG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6b3eedd5-0a8a-4a45-b383-0bb396f0610e/office-depot-home.PNG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6b3eedd5-0a8a-4a45-b383-0bb396f0610e/office-depot-home.PNG"
			sizes="100vw"
			alt="Office Depot includes time-driven design elements"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The Office Depot mobile site uses a variety of time-driven design elements to satisfy visitors’ needs. (Source: )
		</figcaption>
	
</figure>


<p>As you can see in the example above, Office Depot uses a number of design tactics and elements to play into this need for immediacy.</p>

<ul>
<li>There is a search bar at the very top. Consumers don’t have to even bother with navigation or scrolling through pages if they don’t want to/have the time to.</li>
<li>You’ll also see that the closest store’s hours are posted and boldly tell me how quickly I can have any products available in store.</li>
<li>Finally, you have the promotional categories for upcoming needs for parents that are about to send kids back to school.</li>
</ul>

<div class="sponsors__wide-place"></div>




<p>Another website is ; it does a great job sparing mobile users the trouble of sifting through irrelevant information and instead gets them to exactly what they need:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/879c59d8-13a2-4ccc-a710-d815954a2eea/universal-studios-home.PNG">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/879c59d8-13a2-4ccc-a710-d815954a2eea/universal-studios-home.PNG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/879c59d8-13a2-4ccc-a710-d815954a2eea/universal-studios-home.PNG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/879c59d8-13a2-4ccc-a710-d815954a2eea/universal-studios-home.PNG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/879c59d8-13a2-4ccc-a710-d815954a2eea/universal-studios-home.PNG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/879c59d8-13a2-4ccc-a710-d815954a2eea/universal-studios-home.PNG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/879c59d8-13a2-4ccc-a710-d815954a2eea/universal-studios-home.PNG"
			sizes="100vw"
			alt="Universal Studios provides immediate research and booking options"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Universal Studios includes immediate options for research and booking on the home page and navigation. (Source: )
		</figcaption>
	
</figure>


<p>Aside from a single banner at the top of the home page, the Universal Studios website design gives visitors exactly what they want right away. The navigation includes only the most pertinent links to information and booking as does this succinct section on the home page. There’s really no time to waste when the options are so clear.</p>

<p>And here is one final example of a website that deals in immediacy, albeit with a more subtle design technique: :</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bb708da0-ed0a-44a9-a537-bc154d5970ba/nordstrom-sale.PNG">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bb708da0-ed0a-44a9-a537-bc154d5970ba/nordstrom-sale.PNG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bb708da0-ed0a-44a9-a537-bc154d5970ba/nordstrom-sale.PNG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bb708da0-ed0a-44a9-a537-bc154d5970ba/nordstrom-sale.PNG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bb708da0-ed0a-44a9-a537-bc154d5970ba/nordstrom-sale.PNG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bb708da0-ed0a-44a9-a537-bc154d5970ba/nordstrom-sale.PNG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bb708da0-ed0a-44a9-a537-bc154d5970ba/nordstrom-sale.PNG"
			sizes="100vw"
			alt="Nordstrom uses color for immediacy"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Nordstrom appeals to immediacy with this one subtle trick. (Source: )
		</figcaption>
	
</figure>


<p>As you can see, this is a pretty typical e-commerce product page. However, there’s one key difference: Nordstrom is subtly calling attention to its Anniversary Sale and the main reason why there is a significant price drop for this purchase. Rather than use  to announce the sale and pester users to shop, it’s made the price change directly on the page and drawn attention to it with the highlighted text.</p>

<h4>3. Respond With Relevant Content</h4>

<p>:</p>

<blockquote>Not only have mobile searches for ‘best’ grown over 80% in the past two years, but searches for ‘best’ have shown higher growth among ‘low-consideration’ products than ‘high-consideration’ products. In other words, we’re all becoming research-obsessed, even about the small stuff.</blockquote>

<p>We understand that the opinions of family, friends, and colleagues matter greatly in the minds of consumers. But as more and more of them to turn the web to make their purchases, it means being open to trusting other opinions online as well &mdash; ones that may be more conveniently expressed from a company’s website, from an influencer’s blog, or from social media.</p>

<p>Wherever those words of wisdom happen to come from, it’s important to take Google’s research to heart. With so many consumers now obsessed with this idea of having the <strong>best</strong> of everything and being able to get it in a pinch, your website needs to be the answer to that question.</p>

<p>But that’s the tricky part. According to Google, it’s not as simple as being a dog food manufacturer and configuring your site to be the answer to:</p>

<h5>“Best Dog Food”</h5>

<p>Consumers experience these micro-moments at a granular level. Sure, there may be some who think, “What is the best dog food?” But isn’t it more likely that question would be more specific in nature? For instance:</p>

<ul>
<li>Best puppy food?</li>
<li>Best grain-free dog food?</li>
<li>Best vegan dog food?</li>
</ul>

<p>Let's take a look at Google, for example. Here’s a variety of searches for a singular “best of” concept:</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d3181ed5-751b-4ac1-a7ec-c8e80878edc2/google-example-best-searches.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d3181ed5-751b-4ac1-a7ec-c8e80878edc2/google-example-best-searches.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d3181ed5-751b-4ac1-a7ec-c8e80878edc2/google-example-best-searches.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d3181ed5-751b-4ac1-a7ec-c8e80878edc2/google-example-best-searches.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d3181ed5-751b-4ac1-a7ec-c8e80878edc2/google-example-best-searches.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d3181ed5-751b-4ac1-a7ec-c8e80878edc2/google-example-best-searches.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d3181ed5-751b-4ac1-a7ec-c8e80878edc2/google-example-best-searches.png"
			sizes="100vw"
			alt="Best searches example from Google"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Example of the variety in “Best” searches in Google. (Source: )
		</figcaption>
	
</figure>


<p>As you can see, it goes beyond the basic questions. Through your design and your content, you must be ready to answer the most relevant questions your users have about your product or service.</p>

<p>With content, you’ll be able to answer many of the “I want to know” questions that are related to the brand with things like:</p>

<ul>
<li>Informational pages regarding services and products.</li>
<li>Whitepapers, ebooks, case studies, reports, and other long-form content that provide heavily researched answers on related matters.</li>
<li>Blog posts, vlogs, podcasts, and other shorter content that can dabble more in appealing to the emotions of consumers.</li>
<li>Tutorials and guides that directly answer questions that consumers are asking.</li>
</ul>

<p>As far as the design piece is concerned, it’s your responsibility to highlight these pages, so visitors don’t have to dig through various parts or layers of the site (like the footer or secondary navigation) to find their answers.</p>

<h5>Google told them it was here, so it’s your job to get them right to it.</h5>

<p>The navigation will play a big part in this, as evidenced by :</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ae20c82a-e1ad-4b50-aa01-9f61df197f75/globus-navigation.PNG">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ae20c82a-e1ad-4b50-aa01-9f61df197f75/globus-navigation.PNG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ae20c82a-e1ad-4b50-aa01-9f61df197f75/globus-navigation.PNG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ae20c82a-e1ad-4b50-aa01-9f61df197f75/globus-navigation.PNG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ae20c82a-e1ad-4b50-aa01-9f61df197f75/globus-navigation.PNG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ae20c82a-e1ad-4b50-aa01-9f61df197f75/globus-navigation.PNG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ae20c82a-e1ad-4b50-aa01-9f61df197f75/globus-navigation.PNG"
			sizes="100vw"
			alt="Globus answers users in the navigation"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Globus Journeys provides answers to micro-moments in the navigation. (Source: )
		</figcaption>
	
</figure>


<p>As you can see in this example, Globus Journeys answers many of those micro-moments right within the navigation: tips on touring (Touring 101), tips on travel best practices (Travel Tips), deals available for travel (Deals & Offers), etc.</p>

<p>Another way to use navigational design to inform visitors on what they’ll learn/know from this experience can take place on the blog.  has an interesting example of this:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3cbdf445-a3c1-4bf6-8eec-312a868b2329/salesforce-blog.PNG">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3cbdf445-a3c1-4bf6-8eec-312a868b2329/salesforce-blog.PNG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3cbdf445-a3c1-4bf6-8eec-312a868b2329/salesforce-blog.PNG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3cbdf445-a3c1-4bf6-8eec-312a868b2329/salesforce-blog.PNG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3cbdf445-a3c1-4bf6-8eec-312a868b2329/salesforce-blog.PNG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3cbdf445-a3c1-4bf6-8eec-312a868b2329/salesforce-blog.PNG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3cbdf445-a3c1-4bf6-8eec-312a868b2329/salesforce-blog.PNG"
			sizes="100vw"
			alt="Salesforce has informative blog navigation"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Salesforce includes a navigation menu for the blog. (Source: )
		</figcaption>
	
</figure>


<p>There is the standard navigation for the Salesforce website, and then there is the navigation that’s specific to the Salesforce blog. This gives you &mdash; as the designer and planner of the site’s layout &mdash; a chance to better and more clearly organize content found within it. So, when visitors show up and want to know tips specific to one of those categories, it doesn’t require random searches or (even worse) endless scrolling through a full blog feed.</p>

<p>Another way you can more quickly and thoroughly inform visitors on topics of interest to them is by using strategically placed sections within blog posts.</p>

<p>While you likely won’t have anything to do with the writing of a website’s blog content, you will have control over its layout and formatting. The first thing you can do to expedite the knowledge acquisition process is by using callouts to detail and link to the various sections covered on the page as  does:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/59d60419-e1e9-4f59-96e0-2defdc16ddcb/bebrainfit-blog.PNG">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/59d60419-e1e9-4f59-96e0-2defdc16ddcb/bebrainfit-blog.PNG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/59d60419-e1e9-4f59-96e0-2defdc16ddcb/bebrainfit-blog.PNG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/59d60419-e1e9-4f59-96e0-2defdc16ddcb/bebrainfit-blog.PNG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/59d60419-e1e9-4f59-96e0-2defdc16ddcb/bebrainfit-blog.PNG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/59d60419-e1e9-4f59-96e0-2defdc16ddcb/bebrainfit-blog.PNG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/59d60419-e1e9-4f59-96e0-2defdc16ddcb/bebrainfit-blog.PNG"
			sizes="100vw"
			alt="Be Brain Fit has an index of topics"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Be Brain Fit calls out a linkable index of topics from the blog post. (Source: )
		</figcaption>
	
</figure>


<p>Of course, the post itself is easy to scan, so readers could guide themselves to the most relevant parts. However, by placing this towards the top of the piece, you’re enabling them to get right to the information they seek.</p>

<p>I’m also going to suggest that pop-ups would be helpful in this matter.</p>

<p>I know, I know.  has done here.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d06cf8f2-02b8-4e5c-8331-cc61417969e1/fit-small-business-blog.PNG">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d06cf8f2-02b8-4e5c-8331-cc61417969e1/fit-small-business-blog.PNG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d06cf8f2-02b8-4e5c-8331-cc61417969e1/fit-small-business-blog.PNG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d06cf8f2-02b8-4e5c-8331-cc61417969e1/fit-small-business-blog.PNG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d06cf8f2-02b8-4e5c-8331-cc61417969e1/fit-small-business-blog.PNG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d06cf8f2-02b8-4e5c-8331-cc61417969e1/fit-small-business-blog.PNG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d06cf8f2-02b8-4e5c-8331-cc61417969e1/fit-small-business-blog.PNG"
			sizes="100vw"
			alt="Fit Small Business uses a helpful pop-up"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Fit Small Business not only provides all the information needed, but also offers an alternative solution to what they seek. (Source: )
		</figcaption>
	
</figure>


<p>I encountered this blog post after doing a search for the best way to create a Facebook page. This was one of the links on the first SERP. I was actually quite pleased with the post as a whole. It broke it up into easy-to-follow steps, attractive and informative visuals, and got me the answer I needed.</p>

<p>However, I was especially pleased to see the bottom banner pop-up after I finished getting through the post. Not only has Fit Small Business attempted to reach its audience by providing helpful content, but it’s also providing an alternative solution to anyone who got here and realized, “Eh, I really don’t want to bother with this on my own."</p>

<h4>4. Respond With Geotargeting</h4>

<p>:</p>

<blockquote>Looking for something nearby &mdash; a coffee shop, noodle restaurant, shoe store &mdash; is one of the most common searches we do. In fact, nearly one-third of all mobile searches are related to location.</blockquote>

<p>Here’s the thing though: users aren’t using “near me” qualifiers as much anymore.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ef5e3ba9-961a-4447-b779-c314cdcab279/think-with-google-near-me-intent.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ef5e3ba9-961a-4447-b779-c314cdcab279/think-with-google-near-me-intent.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ef5e3ba9-961a-4447-b779-c314cdcab279/think-with-google-near-me-intent.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ef5e3ba9-961a-4447-b779-c314cdcab279/think-with-google-near-me-intent.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ef5e3ba9-961a-4447-b779-c314cdcab279/think-with-google-near-me-intent.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ef5e3ba9-961a-4447-b779-c314cdcab279/think-with-google-near-me-intent.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ef5e3ba9-961a-4447-b779-c314cdcab279/think-with-google-near-me-intent.png"
			sizes="100vw"
			alt="Near me qualifiers dropping in use"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Google demonstrates how location qualifiers are decreasing in use. (Source: )
		</figcaption>
	
</figure>


<p>According to Google, this is because many consumers now assume that search engines, websites, and mobile apps are tracking this sort of information already. They expect that if they search for something like “dog food,” Google will automatically serve them the most relevant results &mdash; and that includes taking into account location proximity.</p>

<p>In Google’s research, it found that about two-thirds of mobile consumers are more likely to buy something from a website or app if information is geographically personalized. There are a plethora of ways to communicate this  to visitors &mdash; through the copy, through various design elements, and even photos.</p>

<p> is a pioneer in this space and so I want to give it a special shout-out in this section for what it does with search results:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/40e4bc91-8f31-449b-9029-c69967ba45c4/google-search-example.PNG">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/40e4bc91-8f31-449b-9029-c69967ba45c4/google-search-example.PNG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/40e4bc91-8f31-449b-9029-c69967ba45c4/google-search-example.PNG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/40e4bc91-8f31-449b-9029-c69967ba45c4/google-search-example.PNG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/40e4bc91-8f31-449b-9029-c69967ba45c4/google-search-example.PNG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/40e4bc91-8f31-449b-9029-c69967ba45c4/google-search-example.PNG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/40e4bc91-8f31-449b-9029-c69967ba45c4/google-search-example.PNG"
			sizes="100vw"
			alt="Google auto-populates search questions."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Google’s auto-populated search results aren’t just for Google. (Source: )
		</figcaption>
	
</figure>


<p>The biggest thing to take away from here is the fact that Google provides its users with auto-populated search recommendations. These are based on the users’ geography, behavior, history, as well as what Google knows about the query itself. As you can see here, it expands on Baltimore to provide more specific results based on the area of the city in which the user wants to drink.</p>

<p>With AI-assisted search functionality, any website can offer this same level of smart search for its users.</p>

<p>Of course, you first need to get access to visitors’ geographic data before you can provide them with these kinds of smart and geographically relevant results. One way to do this is to require them to sign in and fill out a profile with these details. Another way, however, is by serving them with this geotargeting request as  has done:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cee6571a-c4f0-4525-8f73-f270b0b17d8c/best-buy-geo.PNG">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cee6571a-c4f0-4525-8f73-f270b0b17d8c/best-buy-geo.PNG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cee6571a-c4f0-4525-8f73-f270b0b17d8c/best-buy-geo.PNG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cee6571a-c4f0-4525-8f73-f270b0b17d8c/best-buy-geo.PNG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cee6571a-c4f0-4525-8f73-f270b0b17d8c/best-buy-geo.PNG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cee6571a-c4f0-4525-8f73-f270b0b17d8c/best-buy-geo.PNG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cee6571a-c4f0-4525-8f73-f270b0b17d8c/best-buy-geo.PNG"
			sizes="100vw"
			alt="Best Buy asks for geo access"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Best Buy requests for access to users’ geographic location. (Source: )
		</figcaption>
	
</figure>


<p>Once you have access to a visitors’ current location, however, you can start providing them with information that helps them with the “I want to go”, “I want to do”, and the “I want to buy” micro-moments that caused them to reach for the phone in the first place.</p>

<p>Here is what the Best Buy website shows me after I granted it permission:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8262d4b9-08a2-4c2d-9dff-888ad7ece3ed/best-buy-local-info.PNG">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8262d4b9-08a2-4c2d-9dff-888ad7ece3ed/best-buy-local-info.PNG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8262d4b9-08a2-4c2d-9dff-888ad7ece3ed/best-buy-local-info.PNG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8262d4b9-08a2-4c2d-9dff-888ad7ece3ed/best-buy-local-info.PNG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8262d4b9-08a2-4c2d-9dff-888ad7ece3ed/best-buy-local-info.PNG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8262d4b9-08a2-4c2d-9dff-888ad7ece3ed/best-buy-local-info.PNG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8262d4b9-08a2-4c2d-9dff-888ad7ece3ed/best-buy-local-info.PNG"
			sizes="100vw"
			alt="Best Buy provides geo-specific details"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Best Buy uses its visitors’ location to provide helpful in-store visit details. (Source: )
		</figcaption>
	
</figure>


<p>The top of the page now displays the nearest location to me as well as opening hours. As I peruse the rest of the site, I will receive relevant information regarding in-store product availability, buy-online-pick-up-in-store options, and so on. This is a really great option for businesses with a sales website and brick-and-mortar location that want to merge the two experiences.</p>

<p>You could also benefit from using this on websites that offer services, appointments, and reservations. Here is an example of what  does with my information:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a7919f2d-f5b5-469b-bb6d-6231e0c99f99/palm-restaurant-reservations.PNG">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a7919f2d-f5b5-469b-bb6d-6231e0c99f99/palm-restaurant-reservations.PNG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a7919f2d-f5b5-469b-bb6d-6231e0c99f99/palm-restaurant-reservations.PNG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a7919f2d-f5b5-469b-bb6d-6231e0c99f99/palm-restaurant-reservations.PNG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a7919f2d-f5b5-469b-bb6d-6231e0c99f99/palm-restaurant-reservations.PNG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a7919f2d-f5b5-469b-bb6d-6231e0c99f99/palm-restaurant-reservations.PNG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a7919f2d-f5b5-469b-bb6d-6231e0c99f99/palm-restaurant-reservations.PNG"
			sizes="100vw"
			alt="The Palm Restaurant geotargeting"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The Palm Restaurant streamlines the reservation process with geotargeting. (Source: )
		</figcaption>
	
</figure>


<p>To start, it uses my information to let me know right away if there even is a location close to me. Philadelphia isn’t too far, but it’s still nice to have the address fully displayed so I can make up my mind about whether I want to dine there. And, if I do, I can choose the “Reservations” button above it.</p>

<p>What’s especially nice about this is that the reservation form is pre-populated:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/68ed4c36-74c8-499f-9f02-d0602ba0c3a4/the-palm-pre-populated.PNG">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/68ed4c36-74c8-499f-9f02-d0602ba0c3a4/the-palm-pre-populated.PNG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/68ed4c36-74c8-499f-9f02-d0602ba0c3a4/the-palm-pre-populated.PNG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/68ed4c36-74c8-499f-9f02-d0602ba0c3a4/the-palm-pre-populated.PNG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/68ed4c36-74c8-499f-9f02-d0602ba0c3a4/the-palm-pre-populated.PNG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/68ed4c36-74c8-499f-9f02-d0602ba0c3a4/the-palm-pre-populated.PNG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/68ed4c36-74c8-499f-9f02-d0602ba0c3a4/the-palm-pre-populated.PNG"
			sizes="100vw"
			alt="The Palm Restaurant streamlines conversion"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The Palm pre-populates its reservation form based on user information. (Source: )
		</figcaption>
	
</figure>


<p>As you can see, it’s used a mixture of my geographic location along with the most popular reservation types (i.e. two people at 7 p.m.) to pre-populate the form. This saves me, as the user, time in filling it out and making my reservation.</p>

<h4>5. Respond With Convenience</h4>

<p>:</p>

<blockquote>Every day, people are becoming more reliant on their smartphones to help make last-minute purchases or spur-of-the-moment decisions. In fact, smartphone users are 50% more likely to expect to purchase something immediately while using their smartphone compared to a year ago.</blockquote>

<p>Recently, I wrote a post about . The underlying message was that mobile consumers have certain expectations that need to be met if you intend on converting them there (as opposed to switching back to desktop).</p>

<ul>
<li>Convenience in getting the information they want is one of them.</li>
<li>Speed in getting to and through checkout is another.</li>
<li>Handling their contact and payment information securely is the final piece.</li>
</ul>

<div class="sponsors__wide-place"></div>




<p>Clearly, web designers are doing something right as over half of smartphone users reach for their phone to buy something and subsequently do. But it can’t stop with the 10 tips offered in that article. You need to be able to predict what they’re going to purchase and what exactly they want to do when you catch them in those exact micro-moments.</p>

<p>Let’s use  as one example.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4bc49d9d-0dee-4c58-abe6-71998b2809ae/upack-quote.PNG">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4bc49d9d-0dee-4c58-abe6-71998b2809ae/upack-quote.PNG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4bc49d9d-0dee-4c58-abe6-71998b2809ae/upack-quote.PNG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4bc49d9d-0dee-4c58-abe6-71998b2809ae/upack-quote.PNG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4bc49d9d-0dee-4c58-abe6-71998b2809ae/upack-quote.PNG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4bc49d9d-0dee-4c58-abe6-71998b2809ae/upack-quote.PNG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4bc49d9d-0dee-4c58-abe6-71998b2809ae/upack-quote.PNG"
			sizes="100vw"
			alt="UPack shows a price quote form first thing"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			UPack includes a price quote form at the very top of the website. (Source: )
		</figcaption>
	
</figure>


<p>At the very top of every page is a short price quote form that asks only the most pertinent details they need in order to provide a quote to interested customers. By anticipating that’s what they’re looking to do when they visit a moving company’s website, UPack likely experiences very high conversion rates.</p>

<p>However, if someone should arrive at this form and wonder, “Should I even bother with a quote from UPack?”, they’ve provided an answer to that on the next step down on the home page:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f3d22fd8-c196-4d94-93db-55aa2f12528e/upack-explainer-graphic.PNG">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f3d22fd8-c196-4d94-93db-55aa2f12528e/upack-explainer-graphic.PNG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f3d22fd8-c196-4d94-93db-55aa2f12528e/upack-explainer-graphic.PNG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f3d22fd8-c196-4d94-93db-55aa2f12528e/upack-explainer-graphic.PNG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f3d22fd8-c196-4d94-93db-55aa2f12528e/upack-explainer-graphic.PNG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f3d22fd8-c196-4d94-93db-55aa2f12528e/upack-explainer-graphic.PNG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f3d22fd8-c196-4d94-93db-55aa2f12528e/upack-explainer-graphic.PNG"
			sizes="100vw"
			alt="UPack’s explainer graphic reaches users on the fence"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			UPack uses an explainer graphic to sell the value of its service right away. (Source: )
		</figcaption>
	
</figure>


<p>This explainer graphic is simple. It includes four points and shows how exactly someone uses the UPack service to move their home from one destination to another. When someone arrives there with the intention of getting help with their move, UPack has already made it all the more simple in just one scroll and two panels of the home page.</p>

<p>Then, you have a company like  that doesn’t waste any time at all:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6f40303e-49cf-41a2-a369-c525f5cea835/hostgator-home-page-purchase.PNG">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6f40303e-49cf-41a2-a369-c525f5cea835/hostgator-home-page-purchase.PNG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6f40303e-49cf-41a2-a369-c525f5cea835/hostgator-home-page-purchase.PNG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6f40303e-49cf-41a2-a369-c525f5cea835/hostgator-home-page-purchase.PNG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6f40303e-49cf-41a2-a369-c525f5cea835/hostgator-home-page-purchase.PNG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6f40303e-49cf-41a2-a369-c525f5cea835/hostgator-home-page-purchase.PNG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6f40303e-49cf-41a2-a369-c525f5cea835/hostgator-home-page-purchase.PNG"
			sizes="100vw"
			alt="HostGator provides shortcut to purchase"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			HostGator’s home page includes smart design callouts that sum up its services. (Source: )
		</figcaption>
	
</figure>


<p>If someone shows up on a web hosting company’s website &mdash; especially one that is well known as they are &mdash; of course they know what they want to do. Now, they could hop into the navigation and dig deeper into the various hosting plans (which some may do). However, HostGator is probably hoping to appeal to two specific audiences with these “Buy Now!” callouts on the home page:</p>

<ul>
<li>The web developer who knows exactly which plan he or she needs, and doesn’t need a full page to explain the benefits to him.</li>
<li>The small business owner who doesn’t know a thing about web hosting, but trusts HostGator’s good name and just wants to get their web hosting purchases ASAP.</li>
</ul>

<p>This is a really good choice of design techniques if you know that a good portion of your audience will be immediately ready to buy upon entering the site. If they don’t have to click through to another site, don’t make them do it.</p>

<p>And, of course, CTAs, in general, are an important element to use when designing for micro-moments. When they’re designed well &mdash; colorful, large, well-labeled &mdash; you’re essentially giving your users a shortcut to conversion.</p>

<p> uses a number of these right on its home page:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3bb8ad79-3517-40fd-bab3-0643843f18ae/barkbox-ctas.PNG">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3bb8ad79-3517-40fd-bab3-0643843f18ae/barkbox-ctas.PNG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3bb8ad79-3517-40fd-bab3-0643843f18ae/barkbox-ctas.PNG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3bb8ad79-3517-40fd-bab3-0643843f18ae/barkbox-ctas.PNG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3bb8ad79-3517-40fd-bab3-0643843f18ae/barkbox-ctas.PNG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3bb8ad79-3517-40fd-bab3-0643843f18ae/barkbox-ctas.PNG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3bb8ad79-3517-40fd-bab3-0643843f18ae/barkbox-ctas.PNG"
			sizes="100vw"
			alt="BarkBox’s CTA shortcuts"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			BarkBox has a number of CTA shortcuts available on its website. (Source: )
		</figcaption>
	
</figure>


<p>Since the brand is particularly well-known among dog owners, this is a good move. While there are some people who enjoy scrolling through the site to see the funny dog pictures and find out more about what’s in this month’s BarkBox, if they’ve arrived here on mobile, they shouldn’t have to wait to subscribe. BarkBox provides those shortcuts in a number of locations, ensuring there’s no friction between its customers and their goals.</p>

<h3>Wrapping Up</h3>

<p>It’s pretty amazing to watch the web change so quickly as consumers become more trusting of their mobile devices. Now, nearly two years after Google first began recommending that we design with micro-moments in mind, it appears that these suggestions have really paid off.</p>

<p>Designing for micro-moments gives us the opportunity to more effectively reach consumers in their moment of need. This, consequently, means reaching consumers who are in a more purchase-intent mindset as opposed to ones casually browsing the web. If you can use your data and design to actively reach consumers in their micro-moments, you can effectively increase your mobile site’s conversion rate in the years to come.</p>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(lf, ra, yk, il)</span>
</div>


              </article>
            </body>
          </html>
---------------
<h1 id="#title_2" >3、Coinbase是如何在其加密货币交易平台上应对扩展性挑战的</h1>
Hrishikesh Barua
[http://www.infoq.com/cn/news/2018/08/coinbase-scaling-challenges?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/08/coinbase-scaling-challenges?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>在2017年的数字货币热潮中，数字货币交易公司Coinbase在他们的平台上遇到了扩展性方面的挑战。工程团队通过升级和优化MongoDB、热点流量隔离解决了这些挑战，并构建了捕获和回放工具以应对未来的流量暴增。</p> <i>By Hrishikesh Barua</i> <i> Translated by 张卫滨 </i>
---------------
<h1 id="#title_3" >4、Universal Windows Platform（UWP）应用的窗口特性</h1>
Jonathan Allen
[http://www.infoq.com/cn/news/2018/08/Windowing-UWP-Applications?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/08/Windowing-UWP-Applications?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>为满足业务线应用的需求，我们将继续推出Universal Windows Platform（UWP）系列文章。下面，我们将注意力转向另一个备受关注的问题，即多窗口支持。Microsoft不仅支持窗口请求响应，而且更进一步提供包括3D支持的多窗口模式。</p> <i>By Jonathan Allen</i> <i> Translated by 盖磊</i>
---------------
<h1 id="#title_4" >5、软件领域的作家、导师兼咨询师杰里·温伯格去世</h1>
Ben Linders
[http://www.infoq.com/cn/news/2018/08/jerry-weinberg-passed-away?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/08/jerry-weinberg-passed-away?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>作家、导师兼顾问杰里·温伯格于2018年8月7日去世，享年84岁。温伯格一生出版了一百多本著作，包括计算机编程、系统思维、领导力、变更、咨询和写作。</p> <i>By Ben Linders</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_5" >6、新的UWP和Win32应用程序分发模型</h1>
Jonathan Allen
[http://www.infoq.com/cn/news/2018/08/UWP-Application-Distribution?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/08/UWP-Application-Distribution?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>自2005年引入ClickOnce技术以来，.NET就支持应用程序自动升级。在ClickOnce模型中，WinForms和WPF应用程序在启动时会从预先配置好的位置查找新版本。很快，私有UWP应用程序分发就将具备同样的功能。</p> <i>By Jonathan Allen</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_6" >7、Kyle Simpson, charting libraries, and an interview with Dr. Axel Rauschmayer</h1>

[https://javascriptweekly.com/issues/399](https://javascriptweekly.com/issues/399)
<table border=0 align="center" border="0">
  <tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   ">

  <div>    
    <table border=0 border=0><tr>
<td align="left" style="padding-left: 4px; font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   "><p>#399 — August 17, 2018</p></td>
<td align="right" style="padding-right: 4px; font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   "><p></p></td>
</tr></table>
    
    <table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0 12px;  "><p>JavaScript Weekly</p></td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
      <p>A blast from the past this week as we take some time out to ask Dr. Axel Rauschmayer, a former editor of <em>JavaScript Weekly</em>, some questions on the release of his new book, <em></em>. You can find that further down in this issue :-)<br>
      <span style="color: #666666;"><em>— Peter Cooper, editor</em></span></p>
    </td></tr></table>
<div style="   margin-top: 14px; margin-bottom: 8px;  "></div>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Having a deeper understanding of how JavaScript engines work can help you reason about the performance characteristics of your code and this diagram-rich post digs into engines optimize around JavaScript’s use of prototype-based inheritance.</p>
  <p>Mathias Bynens </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;">▶  .</p>
  <p>Kyle Simpson </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — The mobile development landscape has changed and we've put together a list of modern options for you. This is a long term decision, you must choose wisely. Download our free ebook to learn more.</p>
  <p>Progress <span style="text-transform: uppercase; padding: 1px 4px;  margin-left: 4px; font-size: 0.9em;   color: #997 !important;">sponsor</span></p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — A rather extensive summary and comparison of charting libraries, comparing key factors such as chart types, commercial vs free, and their open-source status.</p>
  <p>Dan Englishby </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — The V8 JavaScript engine ships with an extensive library of built-in functions and a lot of work has gone into reducing the memory overhead these can represent.</p>
  <p>Jakob Gruber </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Talks through the development lifecycle of creating an extension and lists some of the architectural gotchas.</p>
  <p>Tim Nolet </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"> feature, and better JS/TS error reporting.</p>
  <p>Microsoft </p>
</td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0;  "><p>💻 Jobs</p></td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — We're a SaaS company that creates beautiful data visualizations. Enjoy crafting quality code? We would love to hear from you.</p>
  <p>eBench </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — We're seeking an open minded person who enjoys working in a team and has advanced knowledge in frontend development.</p>
  <p>Football Addicts AB </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Vettery specializes in dev roles and is completely free for job seekers. Create a profile to get started.</p>
  <p>Vettery </p>
</td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0;  "><p>📘 Tutorials and Opinions</p></td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — A collection of common patterns that made working on even the most uncoordinated projects somehow manageable.</p>
  <p>The Cat with a Dragon Tattoo </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Dr. Axel Rauschmayer </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — SDKs for all platforms - Play videos at the same quality and speed as Netflix &amp; YouTube.</p>
  <p>Bitmovin <span style="text-transform: uppercase; padding: 1px 4px;  margin-left: 4px; font-size: 0.9em;   color: #997 !important;">sponsor</span></p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Runs through what Angular application budgets are and what problems they can help surface.</p>
  <p>Tomas Trajan </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"> aims to provide a consistent JS API for client device sensors.</p>
  <p>Ruadhan O'Donoghue </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Chris Nwamba </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;">▶  </span> — Two talks to help you take into account the effect third party scripts may have on your site’s performance.</p>
  <p>SmashingConf </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;">▶  </span></p>
  <p>Amir Rustamzadeh </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>CircleCI <span style="text-transform: uppercase; padding: 1px 4px;  margin-left: 4px; font-size: 0.9em;   color: #997 !important;">sponsor</span></p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;">▶  </span></p>
  <p>JavaScript Jabber <span style="text-transform: uppercase; margin-left: 4px; font-size: 0.9em;  padding: 1px 4px; ">podcast</span></p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Will Ockelmann-Wagner </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Arnaud Lewis </p>
</td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px;  ">
<table border=0 border=0><tr><td style=" font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   "></td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">

<img src="https://res.cloudinary.com/cpress/image/upload/v1534501855/xm6jiym0dfvjwzh2t6hp.png" width="100" style=" margin: 12px 0 16px 16px;      float: right; ">

<p><span style="color: #e40;">💬 A Q&amp;A with…</span><br>Dr. Axel Rauschmayer<br><span style="color: #e40;">JavaScript book author and trainer</span><br><em>Munich, Germany</em></p>

<p>To celebrate the release of his new book, <em> to ask him a couple of questions:</p>

<p>What <em>is</em> an 'impatient' programmer?</p>

<p>I’m assuming that readers of my latest book are 'impatient' in the sense that they want to get started with JavaScript as quickly as possible.</p>

<p>Most chapters are split into two parts. First, the basics, or what is the absolute minimum that you need to know? Then, more advanced stuff, or what should you know once you are more familiar with the language?</p>

<p>This is the only book, that I’m aware of, that covers <em>all </em>of JavaScript, up to and including the very latest version (ES2018). That allowed me to omit old features that were superseded by better features in recent versions (but I do include references that explain the omitted features).</p>

<p>What recent JavaScript features do you think are underused and deserve more attention?</p>

<p>Three stand out for me:</p>

<ul>
<li>In the category “boring, but important”, I count modules and classes, because they provide standardization where we previously had competing and incompatible approaches.</li>
<li>Built-in support for iteration is great, especially if combined with destructuring:
<code>for (const [i, x] of arr.entries()) console.log(i, x);</code>
</li>
<li>Asynchronous functions and asynchronous iteration make asynchronous programming much more pleasant. They are the culmination of a standardization process that started with Promises in ES6.</li>
</ul>

<p>Dr. Axel Rauschmayer is the author of  — out now.</p>

</td></tr></table>
</td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0;  "><p>🔧 Code and Tools</p></td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></p>
  <p>Yotam Mann </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Spencer Kelly </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Notify only the right person based on the commit and see unminified code in the stack trace with source maps.</p>
  <p>Sentry <span style="text-transform: uppercase; padding: 1px 4px;  margin-left: 4px; font-size: 0.9em;   color: #997 !important;">sponsor</span></p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — An interesting and straightforward way to create nested DOM elements.</p>
  <p>m3g4p0p </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></p>
  <p>Adriano Raiano </p>
</td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px;  ">

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
<p>📅 Some forthcoming JavaScript events</p>

<ul>
<li>
 — A one day single track event.</li>

<li>
 — A new 2 day conference focused on all front end frameworks with keynotes from the teams of the most popular ones.</li>

<li>
 — One of the largest JavaScript events. Organized by the Linux Foundation.</li>

<li>
 — An impressive roster of speakers for this event with a focus on mobile and IoT.</li>

</ul>

</td></tr></table>
</td></tr></table>
<table border=0 border=0><tr><td style=" font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   "></td></tr></table>
</div>

  </td></tr>
</table>





<img src="https://javascriptweekly.com/open/399/rss" width="1" height="1" />
---------------