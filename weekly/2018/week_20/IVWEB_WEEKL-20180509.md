## 文章索引
1、 <a href="#1nodejs-100和npm-6发布强化安全性" >Node.js 10.0和NPM 6发布，强化安全性</a><br/>
2、 <a href="#2i-used-the-web-for-a-day-with-javascript-turned-off" >I Used The Web For A Day With JavaScript Turned Off</a><br/>
3、 <a href="#3前端每周清单第61期angular-6发布苹果为统一macos和ios开发声明式api" >前端每周清单第61期：Angular 6发布，苹果为统一macOS和iOS开发声明式API</a><br/>
4、 <a href="#4文章-跟着这五步-从0开始搭建你的第一款小程序" >文章： 跟着这五步 从0开始搭建你的第一款小程序</a><br/>
5、 <a href="#5文章-一种更高效的mn拼图自动还原算法解析" >文章： 一种更高效的M*N拼图自动还原算法解析</a><br/>
6、 <a href="#6专访平安科技cto方国伟云计算十年最需要突破的不仅是技术" >专访平安科技CTO方国伟：云计算十年，最需要突破的不仅是技术</a><br/>
7、 <a href="#7angular-6发布新功能详解" >Angular 6发布，新功能详解</a><br/>
8、 <a href="#8微软azure-sphere提高物联网设备安全性" >微软Azure Sphere提高物联网设备安全性</a><br/>
9、 <a href="#9progress发布nativescript-4" >Progress发布NativeScript 4</a><br/>
10、 <a href="#10文章-一个可供中小团队参考的微服务架构技术栈" >文章： 一个可供中小团队参考的微服务架构技术栈</a><br/><h1 id="#title_0" >1、Node.js 10.0和NPM 6发布，强化安全性</h1>
Kevin Ball
[http://www.infoq.com/cn/news/2018/05/node-10-npm-6-released-security?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/05/node-10-npm-6-released-security?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>4月24日，Node.js项目发布了10.0.0版本的Node.js，同时npm, Inc发布了6.0版本的npm。这两个发布版本都强调了安全性的增强，Node.js升级到了OpenSSL 1.1.0版本，而npm包含了多项聚焦安全的特性，比如对不安全依赖的自动告警。Node.js发布版本还包含了一个新的原生编程API以及对HTTP2的稳定支持。</p> <i>By Kevin Ball</i> <i> Translated by 张卫滨</i>
---------------
<h1 id="#title_1" >2、I Used The Web For A Day With JavaScript Turned Off</h1>
Chris Ashton
[https://www.smashingmagazine.com/2018/05/using-the-web-with-javascript-turned-off/](https://www.smashingmagazine.com/2018/05/using-the-web-with-javascript-turned-off/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/05/using-the-web-with-javascript-turned-off/" />
              <title>I Used The Web For A Day With JavaScript Turned Off</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>I Used The Web For A Day With JavaScript Turned Off</h1>
                  
                    
                    <address>Chris Ashton</address>
                  
                  <time datetime="2018-05-08T14:30:10&#43;02:00" class="op-published">2018-05-08T14:30:10+02:00</time>
                  <time datetime="2018-05-08T21:14:06&#43;00:00" class="op-modified">2018-05-08T21:14:06+00:00</time>
                </header>
                

<p>This article is part of a series in which I attempt to use the web under various constraints, representing a given demographic of user. I hope to raise the profile of difficulties faced by real people, which are avoidable if we design and develop in a way that is sympathetic to their needs. This week, I’m disabling JavaScript.</p>

<h3 id="why-noscript-matters">Why <code>noscript</code> Matters</h3>

<p>Firstly, to clarify, there’s a difference between supporting a <code>noscript</code> experience and using the <code>noscript</code> tag. I don’t generally like the <code>noscript</code> tag, as it fragments your web page into JavaScript and non-JavaScript versions rather than working from the same baseline of content, which is how experiences get messy and things get overlooked.</p>

<p>You may have lots of useful content inside your <code>noscript</code> tags, but if I’m using a JavaScript-enabled browser, I’m not going to see any of that &mdash; I’m going to be stuck waiting for the JS experience to download. When I refer to the ‘noscript’ experience, I generally mean <strong>the experience of using the web page without JavaScript</strong>, rather than the explicit use of the tag.</p>

<div class="c-felix-the-cat">
<h4>Web MIDI API: Getting Started</h4>
<p>Is it possible to use digital musical instruments as browser inputs? With the Web MIDI API, the answer is yes! The best part is, it’s fairly quick and easy to implement and even create a really fun project.  </p>
</div>

<p>So, who cares about users who don’t have JavaScript? Do such <code>noscript</code> users even exist anymore?</p>

<p>Well, they do exist, albeit in small numbers:  have JavaScript disabled. But looking at the numbers of users who have explicitly disabled JavaScript is missing the point.</p>

<p>I’m reminded of this quote by Jake Archibald:</p>

<blockquote>“All your users are non-JS while they’re downloading your JS.”</blockquote>

<p>Think of those users who have JavaScript enabled but who don’t get the JavaScript experience, for any number of reasons, including corporate or local blocking or stripping of JavaScript elements, existing JavaScript errors in the browser from browser add-ons and toolbars, network errors, and so on. BuzzFeed recently revealed that , equating to 13 million failed requests per month.</p>



<aside class="product-panel product-panel__tilted product-panel--book" data-audience="non-subscriber">
    <div class="container product-panel--book__container">
      <div class="panel__description panel__description--book">
    <p>Nope, we can't do any magic tricks, but we have articles,  get a seasoned selection of magic front-end tricks — e.g. <strong>live designing sessions</strong> and perf audits, too. <em>Just sayin'</em>! ;-)</p>

      <a href="https://www.smashingmagazine.com/membership/?utm_medium=panel" class="btn btn--green btn--large">
        Explore Smashing Wizardry&nbsp;→
      </a>
      </div>
      <div class="panel__image panel__image--book">
        <a href="https://www.smashingmagazine.com/membership/?utm_medium=panel" class="books__book__image">
        <div class="books__book__img">
          <img src="https://www.smashingmagazine.com/images/smashing-cat/cat-wizard.svg" alt="Smashing Cat, just preparing to do some magic stuff." width="310" height="400">
        </div>
      </a>
      </div>
    </div>
  </aside>





<div class="c-garfield-the-cat">


<p>Sometimes the issue isn’t with the user but with the CDN delivering the JavaScript. Remember in February 2017 when  in the four-hour outage.</p>

<p>Think also of the emerging global markets; countries still battling to build a network of fast internet, with populations unable to afford fast hardware to run CPU-intensive JavaScript. Or think of the established markets, where even an iPhone X on a 4G connection is not immune to the effects of a partially loaded webpage interrupted by their train going into a tunnel.</p>

<p>The web is a hostile, unpredictable environment, which is why many developers follow the  on top of that. I wanted to see how many sites apply this in practice. What better way than disabling JavaScript altogether?</p>

<h3 id="how-to-disable-javascript">How To Disable JavaScript</h3>

<p>If you’d like to recreate my experiment for yourself, you can disable JavaScript by digging into the settings in Chrome:</p>

<ul>
<li>Open the Developer Tools (Chrome -&gt; View -&gt; Developer Tools, or ⌥⌘I on the keyboard)</li>
<li>Open the developer submenu (the three dots next to the close icon on the Developer Tools)</li>
<li>Choose ‘Settings’ from this submenu</li>
<li>Find the ‘Debugger’ section and check the ‘Disable JavaScript’ box</li>
</ul>

<p>Or, like me, you can use the excellent  which lets you disable JS in one click.</p>

<h3 id="creating-a-wordpress-post-with-javascript-disabled">Creating A WordPress Post With JavaScript Disabled</h3>

<p>After disabling JavaScript, my first port of call was to go to my personal portfolio site &mdash; which runs on WordPress &mdash; with the aim of writing down my experiences in real time.</p>

<p>WordPress is actually very noscript-friendly, so I was able to start writing this post without any difficulty, although it was missing some of the text formatting and media embedding features I’m used to.</p>

<p>Let&rsquo;s compare WordPress’ post screen with and without JavaScript:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e4405d58-16c4-4bd1-8b0c-d39e69248163/web-with-no-js-1.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e4405d58-16c4-4bd1-8b0c-d39e69248163/web-with-no-js-1.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e4405d58-16c4-4bd1-8b0c-d39e69248163/web-with-no-js-1.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e4405d58-16c4-4bd1-8b0c-d39e69248163/web-with-no-js-1.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e4405d58-16c4-4bd1-8b0c-d39e69248163/web-with-no-js-1.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e4405d58-16c4-4bd1-8b0c-d39e69248163/web-with-no-js-1.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e4405d58-16c4-4bd1-8b0c-d39e69248163/web-with-no-js-1.png"
			sizes="100vw"
			alt="The Noscript version of WordPress’ post page, which is made up of two basic text inputs."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The <code>noscript</code> version of WordPress’ post page, which is made up of two basic text inputs.
		</figcaption>
	
</figure>












<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/85d319a0-3b28-4d23-8ad8-8b08cd0bcd76/web-with-no-js-2.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/85d319a0-3b28-4d23-8ad8-8b08cd0bcd76/web-with-no-js-2.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/85d319a0-3b28-4d23-8ad8-8b08cd0bcd76/web-with-no-js-2.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/85d319a0-3b28-4d23-8ad8-8b08cd0bcd76/web-with-no-js-2.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/85d319a0-3b28-4d23-8ad8-8b08cd0bcd76/web-with-no-js-2.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/85d319a0-3b28-4d23-8ad8-8b08cd0bcd76/web-with-no-js-2.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/85d319a0-3b28-4d23-8ad8-8b08cd0bcd76/web-with-no-js-2.png"
			sizes="100vw"
			alt="The JavaScript version contains shortcuts for formatting text, embedding quotes and media, and previewing the content as HTML."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The JavaScript version contains shortcuts for formatting text, embedding quotes and media, and previewing the content as HTML.
		</figcaption>
	
</figure>


<p>I felt quite comfortable without the toolbars until I needed to embed screenshots in my post. Without the ‘Add Media’ button, I had to go to separate screens to upload my files. This makes sense, as ‘background uploading’ content requires Ajax, which requires JavaScript. But I was quite surprised that the separate media screen also required JavaScript!</p>

<p>Luckily, there was a fallback view:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7e9b41da-91f7-419f-bf0a-262d58c97a31/web-with-no-js-3.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7e9b41da-91f7-419f-bf0a-262d58c97a31/web-with-no-js-3.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7e9b41da-91f7-419f-bf0a-262d58c97a31/web-with-no-js-3.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7e9b41da-91f7-419f-bf0a-262d58c97a31/web-with-no-js-3.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7e9b41da-91f7-419f-bf0a-262d58c97a31/web-with-no-js-3.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7e9b41da-91f7-419f-bf0a-262d58c97a31/web-with-no-js-3.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7e9b41da-91f7-419f-bf0a-262d58c97a31/web-with-no-js-3.png"
			sizes="100vw"
			alt="WordPress media grid view (requires JS)"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The <code>noscript</code> version of the Media section in the admin backend. I was warned that the grid view was not supported without JavaScript.
		</figcaption>
	
</figure>












<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4af92eb7-6f35-4e82-a202-7a551bbf05bd/web-with-no-js-4.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4af92eb7-6f35-4e82-a202-7a551bbf05bd/web-with-no-js-4.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4af92eb7-6f35-4e82-a202-7a551bbf05bd/web-with-no-js-4.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4af92eb7-6f35-4e82-a202-7a551bbf05bd/web-with-no-js-4.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4af92eb7-6f35-4e82-a202-7a551bbf05bd/web-with-no-js-4.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4af92eb7-6f35-4e82-a202-7a551bbf05bd/web-with-no-js-4.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4af92eb7-6f35-4e82-a202-7a551bbf05bd/web-with-no-js-4.png"
			sizes="100vw"
			alt="WordPress media list view (fallback)"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Who needs grids anyway? The list view was perfectly fine for my needs.
		</figcaption>
	
</figure>


<p>After uploading the image, I had to manually write an HTML <code>img</code> tag in my post and copy and paste the image URL into it. There was no way of determining the thumbnail URL of the uploaded image, and any captions I wrote also had to be manually copied. I soon got fed up of this approach and planned to come back the next day and re-insert all of the images when I allowed myself to use JavaScript again.</p>

<p>I decided to take a look at how the front-end of my site was doing.</p>

<h3 id="viewing-my-site-without-javascript">Viewing My Site Without JavaScript</h3>

<p>I was pleasantly surprised that my site looked largely the same without JS:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bc39549b-1e1e-4e04-b351-075503b8a745/web-with-no-js-5.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bc39549b-1e1e-4e04-b351-075503b8a745/web-with-no-js-5.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bc39549b-1e1e-4e04-b351-075503b8a745/web-with-no-js-5.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bc39549b-1e1e-4e04-b351-075503b8a745/web-with-no-js-5.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bc39549b-1e1e-4e04-b351-075503b8a745/web-with-no-js-5.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bc39549b-1e1e-4e04-b351-075503b8a745/web-with-no-js-5.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bc39549b-1e1e-4e04-b351-075503b8a745/web-with-no-js-5.png"
			sizes="100vw"
			alt="With JavaScript"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Personal site with JavaScript.
		</figcaption>
	
</figure>












<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0697b178-37ef-4f4b-b2c0-ac892ae9e59c/web-with-no-js-6.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0697b178-37ef-4f4b-b2c0-ac892ae9e59c/web-with-no-js-6.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0697b178-37ef-4f4b-b2c0-ac892ae9e59c/web-with-no-js-6.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0697b178-37ef-4f4b-b2c0-ac892ae9e59c/web-with-no-js-6.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0697b178-37ef-4f4b-b2c0-ac892ae9e59c/web-with-no-js-6.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0697b178-37ef-4f4b-b2c0-ac892ae9e59c/web-with-no-js-6.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0697b178-37ef-4f4b-b2c0-ac892ae9e59c/web-with-no-js-6.png"
			sizes="100vw"
			alt="Without JavaScript"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Personal site without JavaScript. Only the Twitter embed looks any different.
		</figcaption>
	
</figure>


<p>Let’s take a closer look at that Twitter embed:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/50f59b31-87a4-4165-9831-392874d998e4/web-with-no-js-7.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/50f59b31-87a4-4165-9831-392874d998e4/web-with-no-js-7.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/50f59b31-87a4-4165-9831-392874d998e4/web-with-no-js-7.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/50f59b31-87a4-4165-9831-392874d998e4/web-with-no-js-7.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/50f59b31-87a4-4165-9831-392874d998e4/web-with-no-js-7.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/50f59b31-87a4-4165-9831-392874d998e4/web-with-no-js-7.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/50f59b31-87a4-4165-9831-392874d998e4/web-with-no-js-7.png"
			sizes="100vw"
			alt="Tweet with JavaScript"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Note the author information, engagement stats, and information link that we don’t get with the <code>noscript</code> version. The ‘tick’ is an external PNG. ()
		</figcaption>
	
</figure>












<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/eede9681-3fcd-41b8-b370-1e407f8f87c6/web-with-no-js-8.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/eede9681-3fcd-41b8-b370-1e407f8f87c6/web-with-no-js-8.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/eede9681-3fcd-41b8-b370-1e407f8f87c6/web-with-no-js-8.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/eede9681-3fcd-41b8-b370-1e407f8f87c6/web-with-no-js-8.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/eede9681-3fcd-41b8-b370-1e407f8f87c6/web-with-no-js-8.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/eede9681-3fcd-41b8-b370-1e407f8f87c6/web-with-no-js-8.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/eede9681-3fcd-41b8-b370-1e407f8f87c6/web-with-no-js-8.png"
			sizes="100vw"
			alt="Tweet without JavaScript"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Missing styles, but contains all of the content, including hashtag link and link to tweet. The ‘tick’ is an ASCII character: ✔.
		</figcaption>
	
</figure>


<p>Below the fold of my site, I’ve also embedded some Instagram content, which held up well to the <code>noscript</code> experience.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8b97997a-ed53-4622-a749-876d15a2525c/web-with-no-js-9.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8b97997a-ed53-4622-a749-876d15a2525c/web-with-no-js-9.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8b97997a-ed53-4622-a749-876d15a2525c/web-with-no-js-9.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8b97997a-ed53-4622-a749-876d15a2525c/web-with-no-js-9.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8b97997a-ed53-4622-a749-876d15a2525c/web-with-no-js-9.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8b97997a-ed53-4622-a749-876d15a2525c/web-with-no-js-9.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8b97997a-ed53-4622-a749-876d15a2525c/web-with-no-js-9.png"
			sizes="100vw"
			alt="Instagram embed with JavaScript"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Notice the slideshow dots underneath the image, indicating there are more images in the gallery.
		</figcaption>
	
</figure>












<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3ca3b40a-8a79-473d-9f77-59f0ae025aad/web-with-no-js-10.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3ca3b40a-8a79-473d-9f77-59f0ae025aad/web-with-no-js-10.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3ca3b40a-8a79-473d-9f77-59f0ae025aad/web-with-no-js-10.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3ca3b40a-8a79-473d-9f77-59f0ae025aad/web-with-no-js-10.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3ca3b40a-8a79-473d-9f77-59f0ae025aad/web-with-no-js-10.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3ca3b40a-8a79-473d-9f77-59f0ae025aad/web-with-no-js-10.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3ca3b40a-8a79-473d-9f77-59f0ae025aad/web-with-no-js-10.png"
			sizes="100vw"
			alt="Instagram embed without JavaScript"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The noJS version doesn’t have such dots. Other than the missing slideshow functionality, this is indistinguishable from the JS version.
		</figcaption>
	
</figure>


<p>Finally, I have a GitHub embed on my site. GitHub doesn’t offer a native embed, so I use the unofficial .</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/647cfcbb-a5e8-4b3b-b441-3e7eba893ab6/web-with-no-js-11.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/647cfcbb-a5e8-4b3b-b441-3e7eba893ab6/web-with-no-js-11.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/647cfcbb-a5e8-4b3b-b441-3e7eba893ab6/web-with-no-js-11.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/647cfcbb-a5e8-4b3b-b441-3e7eba893ab6/web-with-no-js-11.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/647cfcbb-a5e8-4b3b-b441-3e7eba893ab6/web-with-no-js-11.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/647cfcbb-a5e8-4b3b-b441-3e7eba893ab6/web-with-no-js-11.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/647cfcbb-a5e8-4b3b-b441-3e7eba893ab6/web-with-no-js-11.png"
			sizes="100vw"
			alt="GitHub embed with JavaScript"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The unofficial card gives a nice little snapshot and links to your GitHub profile.
		</figcaption>
	
</figure>












<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a4f54507-41a8-454d-a889-4b70e0a87ff5/web-with-no-js-12.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a4f54507-41a8-454d-a889-4b70e0a87ff5/web-with-no-js-12.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a4f54507-41a8-454d-a889-4b70e0a87ff5/web-with-no-js-12.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a4f54507-41a8-454d-a889-4b70e0a87ff5/web-with-no-js-12.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a4f54507-41a8-454d-a889-4b70e0a87ff5/web-with-no-js-12.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a4f54507-41a8-454d-a889-4b70e0a87ff5/web-with-no-js-12.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a4f54507-41a8-454d-a889-4b70e0a87ff5/web-with-no-js-12.png"
			sizes="100vw"
			alt="GitHub embed without JavaScript"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			I provide a fallback link to GitHub if no JavaScript is available.
		</figcaption>
	
</figure>


<p>I was half hoping to shock you with the before and after stats (<em>megabytes of JS for a small embed! End of the world! Let’s ditch JavaScript!</em>), and half hoping there’d by very little difference (<em>progressive enhancement! Leading by example! I’m a good developer!</em>).</p>

<p>Let’s compare page weights with and without JavaScript. Firstly, with JavaScript:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c9dc35e2-d36d-48ee-b5c6-596207371175/web-with-no-js-13.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c9dc35e2-d36d-48ee-b5c6-596207371175/web-with-no-js-13.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c9dc35e2-d36d-48ee-b5c6-596207371175/web-with-no-js-13.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c9dc35e2-d36d-48ee-b5c6-596207371175/web-with-no-js-13.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c9dc35e2-d36d-48ee-b5c6-596207371175/web-with-no-js-13.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c9dc35e2-d36d-48ee-b5c6-596207371175/web-with-no-js-13.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c9dc35e2-d36d-48ee-b5c6-596207371175/web-with-no-js-13.png"
			sizes="100vw"
			alt="Page weight with JavaScript"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			51 HTTP requests, with 1.9MB transferred.
		</figcaption>
	
</figure>


<p>Now without JavaScript:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/49029a7b-1626-4aca-a420-2841f27b0691/web-with-no-js-14.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/49029a7b-1626-4aca-a420-2841f27b0691/web-with-no-js-14.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/49029a7b-1626-4aca-a420-2841f27b0691/web-with-no-js-14.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/49029a7b-1626-4aca-a420-2841f27b0691/web-with-no-js-14.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/49029a7b-1626-4aca-a420-2841f27b0691/web-with-no-js-14.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/49029a7b-1626-4aca-a420-2841f27b0691/web-with-no-js-14.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/49029a7b-1626-4aca-a420-2841f27b0691/web-with-no-js-14.png"
			sizes="100vw"
			alt="Page weight without JavaScript"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			18 HTTP requests, with 1.3MB transferred.
		</figcaption>
	
</figure>


<p>For the sake of a styled tweet, a GitHub embed and a full-fat Instagram embed, my site grows an extra 600KB. I’ve also got Google analytics tracking and some . All things considered, 600KB doesn’t seem over the top &mdash; though I am a little surprised by the number of additional requests the browser has to make for all that to happen.</p>

<p>All the content is still there without JavaScript, all the menus are still navigable, and with the exception of the Twitter embed, you’d be hard-pressed to realize that JavaScript is turned off. As a result, my site passes the NOSCRIPT-5 level of validation &mdash; the very best non-JavaScript rating possible.</p>

<p><strong>ashton.codes <code>noscript</code> rating: NOSCRIPT-5. ✅</strong></p>

<p>What’s that? You haven’t heard of the <code>noscript</code> classification system? I’d be very surprised if you had because I just made it up. It’s my handy little indicator of a site’s usability without JavaScript, and by extension, it’s a pretty good indicator of how good a site is at progressively enhancing its content.</p>

<h3 id="noscript-classification-system"><code>noscript</code> Classification System</h3>

<p>Websites &mdash; or more accurately, their individual pages &mdash; tend to fall into one of the following categories:</p>

<ul>
<li><strong>NOSCRIPT-5</strong><br />
The site is virtually indistinguishable from the JavaScript-enabled version of the site.</li>
<li><strong>NOSCRIPT-4</strong><br />
The site provides functionality parity for noscript, but links to or redirects to a <em>separate version</em> of the site to achieve that.</li>
<li><strong>NOSCRIPT-3</strong><br />
Site largely works without JavaScript, but some non-key features are unsupported or look broken.</li>
<li><strong>NOSCRIPT-2</strong><br />
The site offers message saying their browser is not supported.</li>
<li><strong>NOSCRIPT-1</strong><br />
The site appears to load, but the user is unable to use key functionality at all.</li>
<li><strong>NOSCRIPT-0</strong><br />
The site does not load at all and offers no feedback to the user.</li>
</ul>

<p>Let’s look at some popular sites and see how they score.</p>

<h3 id="amazon">Amazon</h3>

<p>I’ve had my eye on a little robotic vacuum cleaner for a while. My lease doesn’t allow any pets, and this is the next best thing once you put some googly eyes on it.</p>

<p>At first glance, Amazon does a cracking job with its non-JavaScript solution, although the main product image is missing.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d66e774b-3468-4106-abee-3eda436b87a4/web-with-no-js-16.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d66e774b-3468-4106-abee-3eda436b87a4/web-with-no-js-16.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d66e774b-3468-4106-abee-3eda436b87a4/web-with-no-js-16.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d66e774b-3468-4106-abee-3eda436b87a4/web-with-no-js-16.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d66e774b-3468-4106-abee-3eda436b87a4/web-with-no-js-16.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d66e774b-3468-4106-abee-3eda436b87a4/web-with-no-js-16.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d66e774b-3468-4106-abee-3eda436b87a4/web-with-no-js-16.png"
			sizes="100vw"
			alt="Amazon without JavaScript"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Missing the main image, but unmistakably Amazon.
		</figcaption>
	
</figure>












<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8df16295-6f98-4d34-80b3-b8d192852622/web-with-no-js-15.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8df16295-6f98-4d34-80b3-b8d192852622/web-with-no-js-15.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8df16295-6f98-4d34-80b3-b8d192852622/web-with-no-js-15.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8df16295-6f98-4d34-80b3-b8d192852622/web-with-no-js-15.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8df16295-6f98-4d34-80b3-b8d192852622/web-with-no-js-15.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8df16295-6f98-4d34-80b3-b8d192852622/web-with-no-js-15.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8df16295-6f98-4d34-80b3-b8d192852622/web-with-no-js-15.png"
			sizes="100vw"
			alt="Amazon with JavaScript"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			With JavaScript, we get the main image. Look at this lovely little vacuum.
		</figcaption>
	
</figure>


<p>On closer inspection, quite a few things were a bit broken on the <code>noscript</code> version. I’d like to go through them one by one and suggest a solution for each.</p>

<h3 id="no-gallery-images">No Gallery Images</h3>

<p>I wanted to see some pictures of the products, but clicking on the thumbnails gave me nothing.</p>

<h4 id="issue">Issue</h4>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/96a3beb3-15b7-4346-9692-a4c5a9959756/web-with-no-js-17.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/96a3beb3-15b7-4346-9692-a4c5a9959756/web-with-no-js-17.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/96a3beb3-15b7-4346-9692-a4c5a9959756/web-with-no-js-17.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/96a3beb3-15b7-4346-9692-a4c5a9959756/web-with-no-js-17.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/96a3beb3-15b7-4346-9692-a4c5a9959756/web-with-no-js-17.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/96a3beb3-15b7-4346-9692-a4c5a9959756/web-with-no-js-17.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/96a3beb3-15b7-4346-9692-a4c5a9959756/web-with-no-js-17.png"
			sizes="100vw"
			alt="Issue"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			I clicked on these thumbnails but nothing happened.
		</figcaption>
	
</figure>


<h4 id="potential-solution">Potential Solution</h4>

<p>It would have been nice if these thumbnails were <strong>links to the full image, opening in a new tab. They could then be progressively enhanced</strong> into the image gallery by using JavaScript:</p>

<ul>
<li>Hijack the click event of the thumbnail link;</li>
<li>Grab the <code>href</code> attribute;</li>
<li>Update the <code>src</code> attribute of the main image with the <code>href</code> attribute value.</li>
</ul>

<h4 id="the-report-incorrect-product-information-link-is-javascript-only">The ‘Report Incorrect Product Information’ Link Is JavaScript-Only</h4>

<p>Is this feature really so commonly used that it’s worth downloading extra bytes of JavaScript to all of your users so that it opens as an integrated modal within the page?</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/044fd83b-8826-468f-a420-491695ef71ee/web-with-no-js-19.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/044fd83b-8826-468f-a420-491695ef71ee/web-with-no-js-19.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/044fd83b-8826-468f-a420-491695ef71ee/web-with-no-js-19.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/044fd83b-8826-468f-a420-491695ef71ee/web-with-no-js-19.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/044fd83b-8826-468f-a420-491695ef71ee/web-with-no-js-19.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/044fd83b-8826-468f-a420-491695ef71ee/web-with-no-js-19.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/044fd83b-8826-468f-a420-491695ef71ee/web-with-no-js-19.png"
			sizes="100vw"
			alt="Issue"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Amazon integrated modal window (JavaScript version)
		</figcaption>
	
</figure>


<h4 id="issue-1">Issue</h4>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/33a44264-217e-486e-892b-815e1a3f8fb6/web-with-no-js-18.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/33a44264-217e-486e-892b-815e1a3f8fb6/web-with-no-js-18.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/33a44264-217e-486e-892b-815e1a3f8fb6/web-with-no-js-18.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/33a44264-217e-486e-892b-815e1a3f8fb6/web-with-no-js-18.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/33a44264-217e-486e-892b-815e1a3f8fb6/web-with-no-js-18.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/33a44264-217e-486e-892b-815e1a3f8fb6/web-with-no-js-18.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/33a44264-217e-486e-892b-815e1a3f8fb6/web-with-no-js-18.png"
			sizes="100vw"
			alt="Potential solution"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			It’s a good thing the product information looked accurate to me, because there was no way I could report any issues! The `href` attribute had a value of <code>javascript://</code>, which opens an integrated modal form
		</figcaption>
	
</figure>


<h4 id="potential-solution-1">Potential Solution</h4>

<p>The Amazon integrated modal form requires JavaScript to work. I would <strong>make the ‘report feature’ a standalone form on a separate URL</strong>, e.g. <code>/report-product?product-id=123</code>. This could be progressively enhanced into the integrated modal using Ajax to download the HTML separately.</p>

<h4 id="reviews-are-only-partially-visible-by-default">Reviews Are Only Partially Visible By Default</h4>

<h4 id="issue-2">Issue</h4>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/61925e3b-c200-41ea-84d5-55d3b475a622/web-with-no-js-20.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/61925e3b-c200-41ea-84d5-55d3b475a622/web-with-no-js-20.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/61925e3b-c200-41ea-84d5-55d3b475a622/web-with-no-js-20.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/61925e3b-c200-41ea-84d5-55d3b475a622/web-with-no-js-20.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/61925e3b-c200-41ea-84d5-55d3b475a622/web-with-no-js-20.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/61925e3b-c200-41ea-84d5-55d3b475a622/web-with-no-js-20.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/61925e3b-c200-41ea-84d5-55d3b475a622/web-with-no-js-20.png"
			sizes="100vw"
			alt="Potential solution"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The Read more link does nothing.
		</figcaption>
	
</figure>


<h4 id="potential-solution-2">Potential Solution</h4>

<p>Why not <strong>show the whole review by default and then use JavaScript to truncate</strong> the review text and add the ‘Read more’ link?</p>

<p>It’s worth pointing out that the review title is a link to the review on a standalone page, so it is at least still possible to read the content.</p>

<p>On the whole, I was actually pleasantly surprised just how well the site worked without JavaScript. It could just as easily have been a blank white page. However, the lack of product images means we’re missing out on a really core feature &mdash; I’d argue it’s critical to be able to see what you’re buying! &mdash; so it’s a shame we couldn’t put the icing on the cake and award it a NOSCRIPT-5 rating.</p>

<p><strong>Amazon <code>noscript</code> rating: NOSCRIPT-3. 🤷‍</strong></p>

<p>I still hadn’t decided which product I wanted to buy, so I turned to Camel Camel Camel, the Amazon price tracker.</p>

<h3 id="camel-camel-camel">Camel Camel Camel</h3>

<p>I wanted to decide between the iLife V3s Pro versus the iLife A4s, so headed over to . At first, the site looked indistinguishable from the JavaScript-enabled version.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5f31d9f8-49fe-458e-a37d-4a0fed009379/web-with-no-js-22.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5f31d9f8-49fe-458e-a37d-4a0fed009379/web-with-no-js-22.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5f31d9f8-49fe-458e-a37d-4a0fed009379/web-with-no-js-22.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5f31d9f8-49fe-458e-a37d-4a0fed009379/web-with-no-js-22.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5f31d9f8-49fe-458e-a37d-4a0fed009379/web-with-no-js-22.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5f31d9f8-49fe-458e-a37d-4a0fed009379/web-with-no-js-22.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5f31d9f8-49fe-458e-a37d-4a0fed009379/web-with-no-js-22.png"
			sizes="100vw"
			alt="Potential Solution"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Camel Camel Camel, looking nice and professional &mdash; with no JavaScript.
		</figcaption>
	
</figure>












<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bd43f7bf-540d-44f0-a7fa-c381e4e8785f/web-with-no-js-21.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bd43f7bf-540d-44f0-a7fa-c381e4e8785f/web-with-no-js-21.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bd43f7bf-540d-44f0-a7fa-c381e4e8785f/web-with-no-js-21.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bd43f7bf-540d-44f0-a7fa-c381e4e8785f/web-with-no-js-21.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bd43f7bf-540d-44f0-a7fa-c381e4e8785f/web-with-no-js-21.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bd43f7bf-540d-44f0-a7fa-c381e4e8785f/web-with-no-js-21.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bd43f7bf-540d-44f0-a7fa-c381e4e8785f/web-with-no-js-21.png"
			sizes="100vw"
			alt="no JavaScript issue"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			You could run a git diff on these screenshots and struggle to see the difference!
		</figcaption>
	
</figure>


<p>Unfortunately, the price history chart did not render. It did provide an alt text fallback, but the alt text did not give me any idea of whether or not the price trend has been going up or down.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cd59dc46-3430-4701-8114-c4e86fbcfcd3/web-with-no-js-24.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cd59dc46-3430-4701-8114-c4e86fbcfcd3/web-with-no-js-24.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cd59dc46-3430-4701-8114-c4e86fbcfcd3/web-with-no-js-24.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cd59dc46-3430-4701-8114-c4e86fbcfcd3/web-with-no-js-24.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cd59dc46-3430-4701-8114-c4e86fbcfcd3/web-with-no-js-24.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cd59dc46-3430-4701-8114-c4e86fbcfcd3/web-with-no-js-24.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cd59dc46-3430-4701-8114-c4e86fbcfcd3/web-with-no-js-24.png"
			sizes="100vw"
			alt="Noscript version"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Alt text says “Amazon price history chart” but provides no insight into the data.
		</figcaption>
	
</figure>












<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b018fcef-8bb5-417a-926e-68c9cde8c920/web-with-no-js-23.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b018fcef-8bb5-417a-926e-68c9cde8c920/web-with-no-js-23.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b018fcef-8bb5-417a-926e-68c9cde8c920/web-with-no-js-23.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b018fcef-8bb5-417a-926e-68c9cde8c920/web-with-no-js-23.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b018fcef-8bb5-417a-926e-68c9cde8c920/web-with-no-js-23.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b018fcef-8bb5-417a-926e-68c9cde8c920/web-with-no-js-23.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b018fcef-8bb5-417a-926e-68c9cde8c920/web-with-no-js-23.png"
			sizes="100vw"
			alt="JavaScript version"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Look at this lovely chart you get when JavaScript is enabled.
		</figcaption>
	
</figure>


<p>General suggestion: <strong>provide meaningful alt text at all times</strong>. I don’t necessarily need to see the chart, but I would appreciate a summary of what it contains. Perhaps, in this case, it might be “Amazon price history chart showing that the price of this item has remained largely unchanged since March 2017.” But automatically generating a summary like that is admittedly difficult and prone to anomalies.</p>

<p>Specific suggestion for this use case: <strong>show the image</strong>. The chart on the scripted version of the site is actually a , so there’s no reason why it couldn’t be displayed on the <code>noscript</code> version!</p>

<p>Still, the core content below the chart gave me the information I needed to know.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/12badd3c-bfb6-4a86-979d-6cbea198983f/web-with-no-js-25.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/12badd3c-bfb6-4a86-979d-6cbea198983f/web-with-no-js-25.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/12badd3c-bfb6-4a86-979d-6cbea198983f/web-with-no-js-25.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/12badd3c-bfb6-4a86-979d-6cbea198983f/web-with-no-js-25.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/12badd3c-bfb6-4a86-979d-6cbea198983f/web-with-no-js-25.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/12badd3c-bfb6-4a86-979d-6cbea198983f/web-with-no-js-25.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/12badd3c-bfb6-4a86-979d-6cbea198983f/web-with-no-js-25.png"
			sizes="100vw"
			alt="Who needs a chart? We’ve got a table!"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Who needs a chart? We’ve got a table!
		</figcaption>
	
</figure>


<p>The table provides the feature parity needed to secure a NOSCRIPT-5 rating. I take my hat off to you, Camel Camel Camel!</p>

<p><strong>Camel Camel Camel <code>noscript</code> rating: NOSCRIPT-5 ✅</strong></p>

<h3 id="google-products">Google Products</h3>

<p>At this point in my day, I received a phone call out of the blue: A friend phoned me and asked about meeting up this week. So I went to Google Calendar to check my availability. Google had other ideas!</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/994cdd03-d9c5-422d-a0d2-b9110b1bf023/web-with-no-js-26.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/994cdd03-d9c5-422d-a0d2-b9110b1bf023/web-with-no-js-26.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/994cdd03-d9c5-422d-a0d2-b9110b1bf023/web-with-no-js-26.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/994cdd03-d9c5-422d-a0d2-b9110b1bf023/web-with-no-js-26.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/994cdd03-d9c5-422d-a0d2-b9110b1bf023/web-with-no-js-26.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/994cdd03-d9c5-422d-a0d2-b9110b1bf023/web-with-no-js-26.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/994cdd03-d9c5-422d-a0d2-b9110b1bf023/web-with-no-js-26.png"
			sizes="100vw"
			alt="Issue"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Surprisingly, Google Calendar offers nothing for <code>noscript</code> users.
		</figcaption>
	
</figure>


<p>I was disappointed that there wasn’t a <code>noscript</code> fallback &mdash; Google is usually pretty good at this sort of thing.</p>

<p>I wouldn’t expect to necessarily be able to add/edit/delete entries to my calendar, but it should be possible to <strong>provide a read-only view of my calendar as core content</strong>.</p>

<p><strong>Google calendar <code>noscript</code> rating: NOSCRIPT-0 🔥</strong></p>

<p>Interested in seeing how Google manages other products, I had a quick look at Google Spreadsheets:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ee08d3c1-e5d6-4b79-aeea-9839df0be859/web-with-no-js-27.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ee08d3c1-e5d6-4b79-aeea-9839df0be859/web-with-no-js-27.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ee08d3c1-e5d6-4b79-aeea-9839df0be859/web-with-no-js-27.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ee08d3c1-e5d6-4b79-aeea-9839df0be859/web-with-no-js-27.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ee08d3c1-e5d6-4b79-aeea-9839df0be859/web-with-no-js-27.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ee08d3c1-e5d6-4b79-aeea-9839df0be859/web-with-no-js-27.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ee08d3c1-e5d6-4b79-aeea-9839df0be859/web-with-no-js-27.png"
			sizes="100vw"
			alt="Issue"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Google Spreadsheets shows my spreadsheet but has a big warning message saying “JavaScript isn’t enabled” and won’t let me edit its contents.
		</figcaption>
	
</figure>


<p>In this case, the site fails a lot more gracefully. I can at least read the spreadsheet contents, even if I can’t edit them. Why doesn’t the calendar offer the same fallback solution?</p>

<p>I have no suggestions to improve Google Spreadsheets! It does a good job at <strong>informing the user if core functionality is missing</strong> from the <code>noscript</code> experience.</p>

<p><strong>Google spreadsheets <code>noscript</code> rating: NOSCRIPT-2 😅</strong></p>

<p>This rating isn’t actually that bad! Not all sites are going to be able to offer a <code>noscript</code> experience, but at least if they’re upfront and honest (i.e. they&rsquo;ll say “yeah, we’re not going to try to give you anything”) that prepares you &mdash; the <code>noscript</code> user &mdash; for when it fails. You won’t waste a few precious seconds trying to fill in a form that won’t ever submit, or start reading an article that then has to use Ajax to retrieve the rest of its contents.</p>

<p>Now, back to my potential Amazon purchase. I wanted to look at some third-party reviews before making a purchase.</p>

<p>Google search works really well without JavaScript. It just looks a little dated, like those old desktop-only sites at fixed resolutions.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0da776be-1e75-4ef6-8a6f-55e3275f47b2/web-with-no-js-29.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0da776be-1e75-4ef6-8a6f-55e3275f47b2/web-with-no-js-29.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0da776be-1e75-4ef6-8a6f-55e3275f47b2/web-with-no-js-29.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0da776be-1e75-4ef6-8a6f-55e3275f47b2/web-with-no-js-29.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0da776be-1e75-4ef6-8a6f-55e3275f47b2/web-with-no-js-29.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0da776be-1e75-4ef6-8a6f-55e3275f47b2/web-with-no-js-29.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0da776be-1e75-4ef6-8a6f-55e3275f47b2/web-with-no-js-29.png"
			sizes="100vw"
			alt="Noscript version"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			<code>noscript</code> version has extra search options on the left (otherwise tucked away in settings on the JS version) &mdash; and no privacy banner (perhaps because ‘tracking’ is not relevant to <code>noscript</code> users?)
		</figcaption>
	
</figure>












<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5c6d9e9b-a458-4ac8-9713-c75dbcff78d6/web-with-no-js-28.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5c6d9e9b-a458-4ac8-9713-c75dbcff78d6/web-with-no-js-28.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5c6d9e9b-a458-4ac8-9713-c75dbcff78d6/web-with-no-js-28.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5c6d9e9b-a458-4ac8-9713-c75dbcff78d6/web-with-no-js-28.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5c6d9e9b-a458-4ac8-9713-c75dbcff78d6/web-with-no-js-28.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5c6d9e9b-a458-4ac8-9713-c75dbcff78d6/web-with-no-js-28.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5c6d9e9b-a458-4ac8-9713-c75dbcff78d6/web-with-no-js-28.png"
			sizes="100vw"
			alt="JavaScript version"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			JavaScript version has the ability to search via voice input, and the ‘privacy reminder’ message.
		</figcaption>
	
</figure>


<p>The images view looks even more different, and I actually <em>prefer</em> it in a few ways &mdash; this version loads super quickly and lists the dimensions and image size in kilobytes underneath each thumbnail:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f62ddc7e-d2a4-4438-ac8c-e4b8ba1718bb/web-with-no-js-31.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f62ddc7e-d2a4-4438-ac8c-e4b8ba1718bb/web-with-no-js-31.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f62ddc7e-d2a4-4438-ac8c-e4b8ba1718bb/web-with-no-js-31.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f62ddc7e-d2a4-4438-ac8c-e4b8ba1718bb/web-with-no-js-31.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f62ddc7e-d2a4-4438-ac8c-e4b8ba1718bb/web-with-no-js-31.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f62ddc7e-d2a4-4438-ac8c-e4b8ba1718bb/web-with-no-js-31.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f62ddc7e-d2a4-4438-ac8c-e4b8ba1718bb/web-with-no-js-31.png"
			sizes="100vw"
			alt="Noscript version"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			<code>noscript</code> version: notice the image meta information which is not supplied on the scripted version!
		</figcaption>
	
</figure>












<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2716f197-95f1-48d2-8f9a-a9e57ecf7c06/web-with-no-js-30.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2716f197-95f1-48d2-8f9a-a9e57ecf7c06/web-with-no-js-30.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2716f197-95f1-48d2-8f9a-a9e57ecf7c06/web-with-no-js-30.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2716f197-95f1-48d2-8f9a-a9e57ecf7c06/web-with-no-js-30.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2716f197-95f1-48d2-8f9a-a9e57ecf7c06/web-with-no-js-30.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2716f197-95f1-48d2-8f9a-a9e57ecf7c06/web-with-no-js-30.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2716f197-95f1-48d2-8f9a-a9e57ecf7c06/web-with-no-js-30.png"
			sizes="100vw"
			alt="JavaScript version"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			JavaScript version: notice the ‘related search terms’ area which is not supplied on the <code>noscript</code> version.
		</figcaption>
	
</figure>


<p><strong>Google Search <code>noscript</code> rating: NOSCRIPT-5 ✅</strong></p>

<p>One of the search results took me to a review on YouTube. I clicked, not expecting much. I was right not to get excited:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cb0e52aa-1c51-4811-8fa6-42faf7bacd30/web-with-no-js-32.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cb0e52aa-1c51-4811-8fa6-42faf7bacd30/web-with-no-js-32.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cb0e52aa-1c51-4811-8fa6-42faf7bacd30/web-with-no-js-32.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cb0e52aa-1c51-4811-8fa6-42faf7bacd30/web-with-no-js-32.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cb0e52aa-1c51-4811-8fa6-42faf7bacd30/web-with-no-js-32.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cb0e52aa-1c51-4811-8fa6-42faf7bacd30/web-with-no-js-32.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cb0e52aa-1c51-4811-8fa6-42faf7bacd30/web-with-no-js-32.png"
			sizes="100vw"
			alt="Issue"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			YouTube doesn’t offer much of a <code>noscript</code> experience.
		</figcaption>
	
</figure>


<p>I wouldn’t really expect a site like YouTube to work without JavaScript. YouTube requires advanced streaming capabilities, not to mention that it would open itself up to copy theft if it provided a standalone MP4 download as a fallback. In any case, no site should look broken. I stared at this screen for a few seconds before realizing that nothing else was going to happen.</p>

<p><strong>Suggestion</strong>: <em>If your site is not able to provide a fallback solution for <code>noscript</code> users, at a minimum you should provide a <code>noscript</code> warning message.</em></p>

<p><strong>YouTube <code>noscript</code> rating: NOSCRIPT-0 🔥</strong></p>

<h3 id="which">Which?</h3>

<p>I clicked a couple more review links. The <em>Which?</em> advice site failed me completely.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cbd02077-70f0-43fc-87b8-3a12ca9bf544/web-with-no-js-33.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cbd02077-70f0-43fc-87b8-3a12ca9bf544/web-with-no-js-33.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cbd02077-70f0-43fc-87b8-3a12ca9bf544/web-with-no-js-33.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cbd02077-70f0-43fc-87b8-3a12ca9bf544/web-with-no-js-33.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cbd02077-70f0-43fc-87b8-3a12ca9bf544/web-with-no-js-33.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cbd02077-70f0-43fc-87b8-3a12ca9bf544/web-with-no-js-33.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cbd02077-70f0-43fc-87b8-3a12ca9bf544/web-with-no-js-33.png"
			sizes="100vw"
			alt="Issue"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The site says there are 10 good vacuums to choose from, but the list is clearly populated with Ajax or something as I’m seeing nothing.
		</figcaption>
	
</figure>


<p>This was a page that looked like it loaded fine, but only when you read the content would you realize you must actually be missing some key information. That key information is absolutely core to the purpose of the page, and I can’t get it. Therefore, unfortunately, that’s a NOSCRIPT-1 violation.</p>

<p><strong>Suggestion</strong>: <em>If your site Ajaxes in content, that content exists at another URL. Provide a link to that content for your <code>noscript</code> users. You can always hide the link when you’ve successfully Ajaxed with JavaScript.</em></p>

<p><strong>Which? review site <code>noscript</code> rating: NOSCRIPT-1 😫</strong></p>

<h3 id="facebook">Facebook</h3>

<p>Eventually, I concede that I can’t really afford a vacuum right now. So, I decided to hop onto social media.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/036a04f4-0315-49de-a7c3-f5f2c821d719/web-with-no-js-34.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/036a04f4-0315-49de-a7c3-f5f2c821d719/web-with-no-js-34.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/036a04f4-0315-49de-a7c3-f5f2c821d719/web-with-no-js-34.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/036a04f4-0315-49de-a7c3-f5f2c821d719/web-with-no-js-34.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/036a04f4-0315-49de-a7c3-f5f2c821d719/web-with-no-js-34.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/036a04f4-0315-49de-a7c3-f5f2c821d719/web-with-no-js-34.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/036a04f4-0315-49de-a7c3-f5f2c821d719/web-with-no-js-34.png"
			sizes="100vw"
			alt="Facebook says JavaScript is required to proceed, or we can click the link to the mobile site."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Facebook says JavaScript is required to proceed, or we can click the link to the mobile site.
		</figcaption>
	
</figure>


<p>Facebook flat-out refuses to load without JavaScript, but it does offer a fallback option. Here’s our first example of a NOSCRIPT-4 &mdash; a site which offers a separate version of its content for <code>noscript</code> or feature phone users.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bed1dec2-bb71-4147-85f1-1c608201024f/web-with-no-js-35.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bed1dec2-bb71-4147-85f1-1c608201024f/web-with-no-js-35.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bed1dec2-bb71-4147-85f1-1c608201024f/web-with-no-js-35.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bed1dec2-bb71-4147-85f1-1c608201024f/web-with-no-js-35.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bed1dec2-bb71-4147-85f1-1c608201024f/web-with-no-js-35.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bed1dec2-bb71-4147-85f1-1c608201024f/web-with-no-js-35.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bed1dec2-bb71-4147-85f1-1c608201024f/web-with-no-js-35.png"
			sizes="100vw"
			alt="The mobile site version of Facebook."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The mobile site version of Facebook.
		</figcaption>
	
</figure>


<p>The mobile version loads instantly. It looks ugly, but it seems as though I get the same content as I normally would. Crucially, I have <em>feature parity</em>: I can accomplish the same things here as I can on the main site.</p>

<p><strong>Facebook <code>noscript</code> rating: NOSCRIPT-4 🤔</strong></p>

<p>The page loaded at lightning speed:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/070c291e-65be-4689-8ba9-3548d4fa3d21/web-with-no-js-36.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/070c291e-65be-4689-8ba9-3548d4fa3d21/web-with-no-js-36.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/070c291e-65be-4689-8ba9-3548d4fa3d21/web-with-no-js-36.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/070c291e-65be-4689-8ba9-3548d4fa3d21/web-with-no-js-36.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/070c291e-65be-4689-8ba9-3548d4fa3d21/web-with-no-js-36.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/070c291e-65be-4689-8ba9-3548d4fa3d21/web-with-no-js-36.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/070c291e-65be-4689-8ba9-3548d4fa3d21/web-with-no-js-36.png"
			sizes="100vw"
			alt="50.8KB. Page loaded in 1.39 seconds"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			50.8KB. Page loaded in 1.39 seconds
		</figcaption>
	
</figure>


<p>I could only see 7 items in the news feed at any one time, but I could click to “See More Stories,” which takes me to a new page, using traditional pagination techniques.</p>

<p>I find myself impressed that I have the option to ‘react’ to a Facebook comment, though this is a multi-screen task:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b77c5937-6c7c-4d1e-ac6b-1e21dd4185f2/web-with-no-js-37.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b77c5937-6c7c-4d1e-ac6b-1e21dd4185f2/web-with-no-js-37.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b77c5937-6c7c-4d1e-ac6b-1e21dd4185f2/web-with-no-js-37.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b77c5937-6c7c-4d1e-ac6b-1e21dd4185f2/web-with-no-js-37.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b77c5937-6c7c-4d1e-ac6b-1e21dd4185f2/web-with-no-js-37.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b77c5937-6c7c-4d1e-ac6b-1e21dd4185f2/web-with-no-js-37.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b77c5937-6c7c-4d1e-ac6b-1e21dd4185f2/web-with-no-js-37.png"
			sizes="100vw"
			alt="Reacting first requires you to click ‘React’…"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Reacting first requires you to click ‘React’…
		</figcaption>
	
</figure>












<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4a1c7cf4-d64b-4a3f-8468-1d43cbc51d86/web-with-no-js-38.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4a1c7cf4-d64b-4a3f-8468-1d43cbc51d86/web-with-no-js-38.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4a1c7cf4-d64b-4a3f-8468-1d43cbc51d86/web-with-no-js-38.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4a1c7cf4-d64b-4a3f-8468-1d43cbc51d86/web-with-no-js-38.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4a1c7cf4-d64b-4a3f-8468-1d43cbc51d86/web-with-no-js-38.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4a1c7cf4-d64b-4a3f-8468-1d43cbc51d86/web-with-no-js-38.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4a1c7cf4-d64b-4a3f-8468-1d43cbc51d86/web-with-no-js-38.png"
			sizes="100vw"
			alt="…which then takes you to a separate screen to choose your reaction."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			…which then takes you to a separate screen to choose your reaction.
		</figcaption>
	
</figure>


<p>There’s nothing stopping Facebook building a hover ‘reaction’ menu in non-JavaScript, but to be fair this is aimed at mobile devices that aren’t able to hover.</p>

<p><strong>Suggestion</strong>: <em>Get creative with CSS. You may find that you don’t need JavaScript at all.</em></p>

<p>Before long, a video item came up in my news feed. (At this point, it dawned on me just how much less video content I had seen on the mobile version compared to normal Facebook, meaning I’d actually been seeing peoples’ statuses rather than a random video they ‘liked’ &mdash; a major improvement as far as I’m concerned!)</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0ff33362-a4c7-40df-bfad-a0173fb713c8/web-with-no-js-39.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0ff33362-a4c7-40df-bfad-a0173fb713c8/web-with-no-js-39.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0ff33362-a4c7-40df-bfad-a0173fb713c8/web-with-no-js-39.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0ff33362-a4c7-40df-bfad-a0173fb713c8/web-with-no-js-39.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0ff33362-a4c7-40df-bfad-a0173fb713c8/web-with-no-js-39.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0ff33362-a4c7-40df-bfad-a0173fb713c8/web-with-no-js-39.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0ff33362-a4c7-40df-bfad-a0173fb713c8/web-with-no-js-39.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
</figure>


<p>I fully expected the video not to work when I clicked it, but clicking on the thumbnail opened the video in a new tab:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ae91371b-2b75-4235-9b2b-c127b900d8be/web-with-no-js-40.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ae91371b-2b75-4235-9b2b-c127b900d8be/web-with-no-js-40.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ae91371b-2b75-4235-9b2b-c127b900d8be/web-with-no-js-40.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ae91371b-2b75-4235-9b2b-c127b900d8be/web-with-no-js-40.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ae91371b-2b75-4235-9b2b-c127b900d8be/web-with-no-js-40.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ae91371b-2b75-4235-9b2b-c127b900d8be/web-with-no-js-40.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ae91371b-2b75-4235-9b2b-c127b900d8be/web-with-no-js-40.png"
			sizes="100vw"
			alt="You don’t need JavaScript to play MP4 files"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			You don’t need JavaScript to play MP4 files.
		</figcaption>
	
</figure>


<p>I’m pleasantly surprised that all of the functionality appears to be there on this <code>noscript</code> version of the site. Eventually, however, I found one feature that was just too clunky and cumbersome to see through to the end: album creation.</p>

<p>I wanted to upload a photo album to Facebook, but in <code>noscript</code>-land this is a beast of a task. It involves uploading one photo at a time, going through two or three screens for each upload. I desperately tried and failed to find a bulk-upload option.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1a525cf3-661c-4b44-afd2-499aae40bab0/web-with-no-js-41.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1a525cf3-661c-4b44-afd2-499aae40bab0/web-with-no-js-41.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1a525cf3-661c-4b44-afd2-499aae40bab0/web-with-no-js-41.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1a525cf3-661c-4b44-afd2-499aae40bab0/web-with-no-js-41.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1a525cf3-661c-4b44-afd2-499aae40bab0/web-with-no-js-41.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1a525cf3-661c-4b44-afd2-499aae40bab0/web-with-no-js-41.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1a525cf3-661c-4b44-afd2-499aae40bab0/web-with-no-js-41.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
</figure>


<p>The laboriousness of this got to me after photo number three (my album will contain many more), so I decided to call it a day and come back tomorrow when I’ve got JavaScript.</p>

<h3 id="twitter">Twitter</h3>

<p>Things got weird when I flew over to Twitter.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/11585021-5f76-4c46-827e-408038daffd8/web-with-no-js-42.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/11585021-5f76-4c46-827e-408038daffd8/web-with-no-js-42.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/11585021-5f76-4c46-827e-408038daffd8/web-with-no-js-42.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/11585021-5f76-4c46-827e-408038daffd8/web-with-no-js-42.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/11585021-5f76-4c46-827e-408038daffd8/web-with-no-js-42.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/11585021-5f76-4c46-827e-408038daffd8/web-with-no-js-42.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/11585021-5f76-4c46-827e-408038daffd8/web-with-no-js-42.png"
			sizes="100vw"
			alt="Twitter on first load"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			On first load, I got what looked like the normal desktop site.
		</figcaption>
	
</figure>












<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5ac787ea-ea99-439c-a36a-1b5987234439/web-with-no-js-43.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5ac787ea-ea99-439c-a36a-1b5987234439/web-with-no-js-43.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5ac787ea-ea99-439c-a36a-1b5987234439/web-with-no-js-43.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5ac787ea-ea99-439c-a36a-1b5987234439/web-with-no-js-43.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5ac787ea-ea99-439c-a36a-1b5987234439/web-with-no-js-43.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5ac787ea-ea99-439c-a36a-1b5987234439/web-with-no-js-43.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5ac787ea-ea99-439c-a36a-1b5987234439/web-with-no-js-43.png"
			sizes="100vw"
			alt="Twitter redirect site"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			After a couple of seconds, I was automatically redirected to the mobile site.
		</figcaption>
	
</figure>


<p>I was intrigued by this mechanism, so dug into the source code, which was actually surprisingly simple:</p>

<pre class="break-out"><code class="language-javascript">&lt;noscript&gt;&lt;meta http-equiv="refresh" content="0; URL=https://mobile.twitter.com/i/nojs_router?path=%2F"&gt;&lt;/noscript&gt;</code></pre>

<p>As beautifully simple as this solution is, I found the experience quite clunky because in the flash before I was redirected, I saw that one of the people I follow on Twitter had got engaged. His tweet didn’t appear at the top of the ‘mobile’ version, so I had to go looking for it.</p>

<p><strong>Suggestion</strong>: <em>Build in a grace period into your server-side logic so that redirects and careless refreshes don’t lose interesting tweets before you’ve had a chance to read them.</em></p>

<p>I couldn’t remember my friend’s Twitter handle. Searching was a little tricky &mdash; I started to really miss the autofill suggestions!</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c0488cf8-49f0-4725-bfc3-26685631cad9/web-with-no-js-44.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c0488cf8-49f0-4725-bfc3-26685631cad9/web-with-no-js-44.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c0488cf8-49f0-4725-bfc3-26685631cad9/web-with-no-js-44.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c0488cf8-49f0-4725-bfc3-26685631cad9/web-with-no-js-44.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c0488cf8-49f0-4725-bfc3-26685631cad9/web-with-no-js-44.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c0488cf8-49f0-4725-bfc3-26685631cad9/web-with-no-js-44.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c0488cf8-49f0-4725-bfc3-26685631cad9/web-with-no-js-44.png"
			sizes="100vw"
			alt="A screenshot of me filling in &#39;andy&#39; as a search term, but no autofill suggestions appearing as I type."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			No autofill suggestions appeared as I typed.
		</figcaption>
	
</figure>


<p>Luckily, the search results page brought his account right up, and I was able to find his tweet. I was even able to reply.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4eae7674-8a80-4309-8d42-4ed550d1f66c/web-with-no-js-45.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4eae7674-8a80-4309-8d42-4ed550d1f66c/web-with-no-js-45.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4eae7674-8a80-4309-8d42-4ed550d1f66c/web-with-no-js-45.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4eae7674-8a80-4309-8d42-4ed550d1f66c/web-with-no-js-45.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4eae7674-8a80-4309-8d42-4ed550d1f66c/web-with-no-js-45.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4eae7674-8a80-4309-8d42-4ed550d1f66c/web-with-no-js-45.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4eae7674-8a80-4309-8d42-4ed550d1f66c/web-with-no-js-45.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
</figure>


<p><strong>Twitter <code>noscript</code> rating: NOSCRIPT-4 🤔</strong></p>

<p>This may seem like a generous score, given the clunky feel, but remember that the key thing here is feature parity. It doesn’t have to look beautiful.</p>

<p>I tried out a couple more social media sites, which, unlike Twitter, didn’t reach the dizzy heights of NOSCRIPT-4 compliance.</p>

<h3 id="other-social-networks">Other Social Networks</h3>

<p>LinkedIn has a nice, bespoke loading screen. But it never loads, so all I could do was stare at the logo.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/aa8a0f89-7c5b-41d2-80bb-a852079f70ee/web-with-no-js-46.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/aa8a0f89-7c5b-41d2-80bb-a852079f70ee/web-with-no-js-46.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/aa8a0f89-7c5b-41d2-80bb-a852079f70ee/web-with-no-js-46.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/aa8a0f89-7c5b-41d2-80bb-a852079f70ee/web-with-no-js-46.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/aa8a0f89-7c5b-41d2-80bb-a852079f70ee/web-with-no-js-46.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/aa8a0f89-7c5b-41d2-80bb-a852079f70ee/web-with-no-js-46.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/aa8a0f89-7c5b-41d2-80bb-a852079f70ee/web-with-no-js-46.png"
			sizes="100vw"
			alt="LinkedIn"
		/>
	</a>

	
</figure>


<p><strong>LinkedIn <code>noscript</code> rating: NOSCRIPT-0 🔥</strong></p>

<p>Instagram gave me literally nothing. A blank page. A whole other flavor of NOSCRIPT-0.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0b9acace-ce83-447d-8689-11e724a16081/web-with-no-js-47.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0b9acace-ce83-447d-8689-11e724a16081/web-with-no-js-47.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0b9acace-ce83-447d-8689-11e724a16081/web-with-no-js-47.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0b9acace-ce83-447d-8689-11e724a16081/web-with-no-js-47.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0b9acace-ce83-447d-8689-11e724a16081/web-with-no-js-47.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0b9acace-ce83-447d-8689-11e724a16081/web-with-no-js-47.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0b9acace-ce83-447d-8689-11e724a16081/web-with-no-js-47.png"
			sizes="100vw"
			alt="Instagram"
		/>
	</a>

	
</figure>


<p><strong>Instagram <code>noscript</code> rating: NOSCRIPT-0 🔥🔥🔥</strong></p>

<p>I was surprised Instagram failed so spectacularly here, given that the Instagram embed worked flawlessly on my portfolio site. I guess with an embed you never know what the browser support expectations of the third party are, but as I’m visiting the site directly, Instagram is happy making the call to drop support.</p>

<h3 id="bbc-news">BBC News</h3>

<p>I headed over to the BBC to get my fix of news.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8115d515-fdf6-465d-921e-045d50971ceb/web-with-no-js-49.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8115d515-fdf6-465d-921e-045d50971ceb/web-with-no-js-49.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8115d515-fdf6-465d-921e-045d50971ceb/web-with-no-js-49.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8115d515-fdf6-465d-921e-045d50971ceb/web-with-no-js-49.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8115d515-fdf6-465d-921e-045d50971ceb/web-with-no-js-49.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8115d515-fdf6-465d-921e-045d50971ceb/web-with-no-js-49.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8115d515-fdf6-465d-921e-045d50971ceb/web-with-no-js-49.png"
			sizes="100vw"
			alt="BBC without JavaScript"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			In the <code>noscript</code> version, notice the narrow column and the single story with thumbnail.
		</figcaption>
	
</figure>












<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7e3073d3-504d-4f6f-bfbc-711bba760ff2/web-with-no-js-48.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7e3073d3-504d-4f6f-bfbc-711bba760ff2/web-with-no-js-48.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7e3073d3-504d-4f6f-bfbc-711bba760ff2/web-with-no-js-48.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7e3073d3-504d-4f6f-bfbc-711bba760ff2/web-with-no-js-48.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7e3073d3-504d-4f6f-bfbc-711bba760ff2/web-with-no-js-48.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7e3073d3-504d-4f6f-bfbc-711bba760ff2/web-with-no-js-48.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7e3073d3-504d-4f6f-bfbc-711bba760ff2/web-with-no-js-48.png"
			sizes="100vw"
			alt="BBC with JavaScript"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			JavaScript version: notice the full use of the desktop screen and multiple article thumbnails.
		</figcaption>
	
</figure>


<p>The menu is a little bit off, and the column is quite narrow (definitely a pattern I’m seeing on a lot of sites &mdash; why does “no JavaScript” mean “mobile device”?) but I <em>am</em> able to access the content.</p>




  <aside class="product-panel product-panel__tilted product-panel--book" data-audience="non-subscriber" data-remove="true">
    <div class="container product-panel--book__container">
      <div class="panel__description panel__description--book">
        <p>
          Is your pattern library up to date today? <em>Alla Kholmatova</em> has just finished a fully fledged book on <strong>Design Systems</strong> and how to get them right. With common traps, gotchas and the lessons she learned. Hardcover, eBook. <em>Just sayin'.</em>
        </p>
        <a href="https://www.smashingmagazine.com/printed-books/design-systems/">
          <button class="btn btn--green btn--large">
            Table of Contents&nbsp;&rarr;
          </button>
        </a>
      </div>
      <div class="panel__image panel__image--book">
        <a href="https://www.smashingmagazine.com/printed-books/design-systems/" class="books__book__image">
        <div class="books__book__img">
          <img src="https://www.smashingmagazine.com/images/books/design-systems--large-opt.png">
        </div>
      </a>
      </div>
    </div>
  </aside>




<p>I clicked on the ‘Most Read’ tab, which takes me to another part of the page. With scripting, this anchor link is progressively enhanced to achieve actual tab behavior, which is a lovely example of building up from a solid HTML core.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ae2235a7-10af-40ea-bbd5-609da70f3948/web-with-no-js-50.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ae2235a7-10af-40ea-bbd5-609da70f3948/web-with-no-js-50.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ae2235a7-10af-40ea-bbd5-609da70f3948/web-with-no-js-50.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ae2235a7-10af-40ea-bbd5-609da70f3948/web-with-no-js-50.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ae2235a7-10af-40ea-bbd5-609da70f3948/web-with-no-js-50.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ae2235a7-10af-40ea-bbd5-609da70f3948/web-with-no-js-50.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ae2235a7-10af-40ea-bbd5-609da70f3948/web-with-no-js-50.png"
			sizes="100vw"
			alt="Issue"
		/>
	</a>

	
</figure>


<p>So far, this is the only example of an anchor link I’ve come across in my experiment, which is a shame as it’s a nice technique that saves an additional page load and saves fragmenting the site into lots of micro pages.</p>

<p>It does look a little odd though, the ordered list CSS meaning we have a double numbering glitch here. I click on one of the stories.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0f2e8be9-aefd-4c54-9a3e-79cab5fd1bb2/web-with-no-js-51.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0f2e8be9-aefd-4c54-9a3e-79cab5fd1bb2/web-with-no-js-51.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0f2e8be9-aefd-4c54-9a3e-79cab5fd1bb2/web-with-no-js-51.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0f2e8be9-aefd-4c54-9a3e-79cab5fd1bb2/web-with-no-js-51.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0f2e8be9-aefd-4c54-9a3e-79cab5fd1bb2/web-with-no-js-51.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0f2e8be9-aefd-4c54-9a3e-79cab5fd1bb2/web-with-no-js-51.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0f2e8be9-aefd-4c54-9a3e-79cab5fd1bb2/web-with-no-js-51.png"
			sizes="100vw"
			alt="The article should contain a video, but instead reads “Media playback is unsupported on your device”. There is no transcript."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The article should contain a video, but instead reads “Media playback is unsupported on your device”. There is no transcript.
		</figcaption>
	
</figure>


<p>I can’t access the video content, but due to rights issues, I suspect the BBC cannot provide a separate standalone video as Facebook does. A transcript would be nice though &mdash; and beneficial to more than just <code>noscript</code> users.</p>

<p><strong>Suggestion</strong>: <em>Provide textual fallbacks for audio-visual content.</em></p>

<p>To be fair, the article content basically sums up the content that appears in the video, so I’m not really missing out on information.</p>

<p>The article and index pages load lightning-fast, at about 300KB (mostly images). I do miss the thumbnail images for the other articles on the page, and the ability to make full use of my screen real estate &mdash; but that shouldn’t hamper the rating.</p>

<p><strong>BBC <code>noscript</code> rating: NOSCRIPT-5 ✅</strong></p>

<h3 id="github">GitHub</h3>

<p>GitHub looks almost <em>exactly the same</em> as its JavaScript-enabled counterpart. Wow! But I guess this is a site developed by developers, for developers. 😉</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/997c2444-c963-4c0d-8c7e-80bdda39311e/web-with-no-js-52.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/997c2444-c963-4c0d-8c7e-80bdda39311e/web-with-no-js-52.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/997c2444-c963-4c0d-8c7e-80bdda39311e/web-with-no-js-52.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/997c2444-c963-4c0d-8c7e-80bdda39311e/web-with-no-js-52.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/997c2444-c963-4c0d-8c7e-80bdda39311e/web-with-no-js-52.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/997c2444-c963-4c0d-8c7e-80bdda39311e/web-with-no-js-52.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/997c2444-c963-4c0d-8c7e-80bdda39311e/web-with-no-js-52.png"
			sizes="100vw"
			alt="GitHub with JavaScript"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The one difference I can see is the way GitHub deals with time. With JavaScript enabled, notice how it says ‘2 days ago’...
		</figcaption>
	
</figure>












<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d0b39647-9ea9-4295-8bf7-c5086a5ce2ec/web-with-no-js-53.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d0b39647-9ea9-4295-8bf7-c5086a5ce2ec/web-with-no-js-53.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d0b39647-9ea9-4295-8bf7-c5086a5ce2ec/web-with-no-js-53.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d0b39647-9ea9-4295-8bf7-c5086a5ce2ec/web-with-no-js-53.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d0b39647-9ea9-4295-8bf7-c5086a5ce2ec/web-with-no-js-53.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d0b39647-9ea9-4295-8bf7-c5086a5ce2ec/web-with-no-js-53.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d0b39647-9ea9-4295-8bf7-c5086a5ce2ec/web-with-no-js-53.png"
			sizes="100vw"
			alt="GitHub without JavaScript"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			On the no script version, it instead says “Mar 1, 2018”.
		</figcaption>
	
</figure>


<p>I did a little housekeeping on GitHub, looking around repos and deleting old branches. For a while I genuinely forgot I was on the non-JavaScript version until I came across one little bug:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dd0abd19-2247-4263-9984-e02695f908f6/web-with-no-js-54.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dd0abd19-2247-4263-9984-e02695f908f6/web-with-no-js-54.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dd0abd19-2247-4263-9984-e02695f908f6/web-with-no-js-54.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dd0abd19-2247-4263-9984-e02695f908f6/web-with-no-js-54.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dd0abd19-2247-4263-9984-e02695f908f6/web-with-no-js-54.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dd0abd19-2247-4263-9984-e02695f908f6/web-with-no-js-54.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dd0abd19-2247-4263-9984-e02695f908f6/web-with-no-js-54.png"
			sizes="100vw"
			alt="The “Fetching latest commit…” section will spin forever…"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The “Fetching latest commit…” section will spin forever…
		</figcaption>
	
</figure>


<p>Then I wondered, “How is GitHub going to handle applying labels to issues?” so I gave that a go.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/30efa40d-7ba0-479a-8bfb-41089c4da969/web-with-no-js-55.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/30efa40d-7ba0-479a-8bfb-41089c4da969/web-with-no-js-55.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/30efa40d-7ba0-479a-8bfb-41089c4da969/web-with-no-js-55.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/30efa40d-7ba0-479a-8bfb-41089c4da969/web-with-no-js-55.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/30efa40d-7ba0-479a-8bfb-41089c4da969/web-with-no-js-55.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/30efa40d-7ba0-479a-8bfb-41089c4da969/web-with-no-js-55.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/30efa40d-7ba0-479a-8bfb-41089c4da969/web-with-no-js-55.png"
			sizes="100vw"
			alt="These fields are unresponsive when you click on them."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			These fields are unresponsive when you click on them.
		</figcaption>
	
</figure>


<p>I was unable to create an issue and add labels to it at the same time. In fact, I couldn’t find any way of adding the label even after creating a blank issue. It’s a shame the site fell at the last hurdle because it was very nearly a seamless comparison with the scripted version.</p>

<p><strong>GitHub <code>noscript</code> rating: NOSCRIPT-3 🤗</strong></p>

<p>While GitHub <em>looks</em> incredible &mdash; I would never have known my JavaScript was turned off &mdash; not being able to use the same key functionality as the scripted version is a bummer. Even an ugly looking <code>noscript</code> site would get a higher score because functionality is more important than form.</p>

<h3 id="online-banking">Online Banking</h3>

<p>If there’s one place I expected JavaScript to be required, it was on the NatWest bank website. I was wrong.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5ec4ea19-645e-44bf-8c70-8cb890271aae/web-with-no-js-56.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5ec4ea19-645e-44bf-8c70-8cb890271aae/web-with-no-js-56.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5ec4ea19-645e-44bf-8c70-8cb890271aae/web-with-no-js-56.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5ec4ea19-645e-44bf-8c70-8cb890271aae/web-with-no-js-56.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5ec4ea19-645e-44bf-8c70-8cb890271aae/web-with-no-js-56.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5ec4ea19-645e-44bf-8c70-8cb890271aae/web-with-no-js-56.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5ec4ea19-645e-44bf-8c70-8cb890271aae/web-with-no-js-56.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
</figure>


<p>Not only does it work, but it’s also hard to distinguish from the normal site. The login screen is the same, the only difference being that the focus doesn’t automatically progress through each field as you complete it.</p>

<p><strong>NatWest <code>noscript</code> rating: NOSCRIPT-5 ✅</strong></p>

<h3 id="miscellaneous">Miscellaneous</h3>

<p>I came across a few more sites throughout my day.</p>

<p>FreeAgent &mdash; the tax software site I use for my freelancing &mdash; doesn’t even try a <code>noscript</code> fallback. But hey, that’s better than showing a broken website.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b4d94209-0126-45c2-bf20-bae5936373e0/web-with-no-js-58.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b4d94209-0126-45c2-bf20-bae5936373e0/web-with-no-js-58.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b4d94209-0126-45c2-bf20-bae5936373e0/web-with-no-js-58.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b4d94209-0126-45c2-bf20-bae5936373e0/web-with-no-js-58.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b4d94209-0126-45c2-bf20-bae5936373e0/web-with-no-js-58.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b4d94209-0126-45c2-bf20-bae5936373e0/web-with-no-js-58.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b4d94209-0126-45c2-bf20-bae5936373e0/web-with-no-js-58.png"
			sizes="100vw"
			alt="FreeAgent shows a no-JavaScript message."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			FreeAgent shows a no-JavaScript message.
		</figcaption>
	
</figure>


<p><strong>FreeAgent <code>noscript</code> rating: NOSCRIPT-2 ⛔</strong></p>

<p>And CodePen, somewhat understandably, has to be a NOSCRIPT-2 too.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2ef9a850-b09b-4cfc-913c-451dda3114fc/web-with-no-js-59.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2ef9a850-b09b-4cfc-913c-451dda3114fc/web-with-no-js-59.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2ef9a850-b09b-4cfc-913c-451dda3114fc/web-with-no-js-59.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2ef9a850-b09b-4cfc-913c-451dda3114fc/web-with-no-js-59.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2ef9a850-b09b-4cfc-913c-451dda3114fc/web-with-no-js-59.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2ef9a850-b09b-4cfc-913c-451dda3114fc/web-with-no-js-59.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2ef9a850-b09b-4cfc-913c-451dda3114fc/web-with-no-js-59.png"
			sizes="100vw"
			alt="A CodePen shows a no-JavaScript message, and suggests it would be pretty foolish to expect the site to work without JavaScript!"
		/>
	</a>

	
</figure>


<p><strong>CodePen <code>noscript</code> rating: NOSCRIPT-2 ⛔</strong></p>

<p>Tonik, the energy provider, doesn’t let me log in, but this seems like an oversight rather than a deliberate decision:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0e8b579c-aa22-4f2d-9865-847be95363aa/web-with-no-js-60.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0e8b579c-aa22-4f2d-9865-847be95363aa/web-with-no-js-60.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0e8b579c-aa22-4f2d-9865-847be95363aa/web-with-no-js-60.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0e8b579c-aa22-4f2d-9865-847be95363aa/web-with-no-js-60.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0e8b579c-aa22-4f2d-9865-847be95363aa/web-with-no-js-60.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0e8b579c-aa22-4f2d-9865-847be95363aa/web-with-no-js-60.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0e8b579c-aa22-4f2d-9865-847be95363aa/web-with-no-js-60.png"
			sizes="100vw"
			alt="I see the words “embedded area” where I’m supposed to see a login form."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			I see the words “embedded area” where I’m supposed to see a login form.
		</figcaption>
	
</figure>


<p><strong>Tonik <code>noscript</code> rating: NOSCRIPT-1 ❌</strong></p>

<p>M&amp;S Energy lets me log in &mdash; only to tell me it needs JavaScript to do anything remotely useful.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ea792c8f-de66-4f87-ad63-0cf7348ea4ac/web-with-no-js-61.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ea792c8f-de66-4f87-ad63-0cf7348ea4ac/web-with-no-js-61.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ea792c8f-de66-4f87-ad63-0cf7348ea4ac/web-with-no-js-61.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ea792c8f-de66-4f87-ad63-0cf7348ea4ac/web-with-no-js-61.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ea792c8f-de66-4f87-ad63-0cf7348ea4ac/web-with-no-js-61.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ea792c8f-de66-4f87-ad63-0cf7348ea4ac/web-with-no-js-61.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ea792c8f-de66-4f87-ad63-0cf7348ea4ac/web-with-no-js-61.png"
			sizes="100vw"
			alt="M&amp;S requires JavaScript to work, but you have to put more effort in to get to that point."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			M&S requires JavaScript to work, but you have to put more effort in to get to that point.
		</figcaption>
	
</figure>


<p><strong>M&amp;S <code>noscript</code> rating: NOSCRIPT-1 ❌</strong></p>

<p>Now I come to my favorite screenshot of the day.</p>

<p>One of my colleagues once recommended an , which I bookmarked. I decided to take a look at it today, and laughed at the irony of the alt text:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d15e08b1-78c8-4fd9-aa72-e9bdec7d89cf/web-with-no-js-62.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d15e08b1-78c8-4fd9-aa72-e9bdec7d89cf/web-with-no-js-62.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d15e08b1-78c8-4fd9-aa72-e9bdec7d89cf/web-with-no-js-62.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d15e08b1-78c8-4fd9-aa72-e9bdec7d89cf/web-with-no-js-62.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d15e08b1-78c8-4fd9-aa72-e9bdec7d89cf/web-with-no-js-62.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d15e08b1-78c8-4fd9-aa72-e9bdec7d89cf/web-with-no-js-62.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d15e08b1-78c8-4fd9-aa72-e9bdec7d89cf/web-with-no-js-62.png"
			sizes="100vw"
			alt="Alt text of “Personas: Accessibility for Web Design”. Soooo… what am I missing?"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Alt text of “Personas: Accessibility for Web Design”. Soooo… what am I missing?
		</figcaption>
	
</figure>


<p>With the alt text of “Personas: Accessibility for Web Design,” I’m not too sure what I’m missing here &mdash; is it an image? A video? A PDF? The course itself?</p>

<p><strong>Hint</strong>: <em>It’s actually a video, though you have to be logged in to watch it.</em></p>

<p>The alt text isn’t really supporting its purpose, partly because it’s populated automatically. We as a dev community need to get better at this sort of thing. I don’t think I’ve read any useful alt text today.</p>

<h3 id="summary">Summary</h3>

<p>I started this experiment with the aim of seeing how many sites are implemented using progressive enhancement. I’ve only visited a tiny handful of sites here, most of them big names with big budgets, so it’s interesting to see the wide variation in no-JavaScript support.</p>

<p>It’s interesting to see that relatively simple sites &mdash; Instagram and LinkedIn particularly &mdash; have such poor <code>noscript</code> support. I believe this is partly down to the ever-growing popularity of JavaScript frameworks such as React, Angular, and Vue. Developers are now building “web applications” rather than “websites,” with the aim of recreating the look and feel of native apps, and using JavaScript to manage the DOM is the most manageable way of creating such experiences.</p>

<p>There is a danger that more and more sites will require JavaScript to render any content at all. Luckily, it is usually possible to build your content in the same, developer-friendly way but rendered on the server, for example by using Preact instead of React. Making the conscious decision to care about <code>noscript</code> gives the benefits of a core experience as outlined at the beginning of this article, and can make for a faster perceived loading time, too.</p>

<p>It can be quite daunting to think about an application from the ground up, but a decent core experience is usually possible and actually only involves simple tweaks in a lot of cases. A good core experience is indicative of a well-structured web page, which, in turn, is usually a good sign for SEO and for accessibility. It’s usually a well <em>designed</em> web page, as the designer and developer have spent time and effort thinking about what’s truly core to the experience. Progressive enhancement means more robust experiences, with fewer bugs in production and fewer individual browser quirks, because we’re letting the platform do the job rather than trying to write it all from scratch.</p>

<p>What <code>noscript</code> rating does your site conform to? Let us know in the comments!</p>




<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(rb, ra, il)</span>
</div>


</div>




  <div id="sponsors-article-end" data-impression="true" class="c-promo-box c-promo-box--ad c-promo-box--wide sponsors hidden" data-audience="non-subscriber" data-remove="true"></div>



              </article>
            </body>
          </html>
---------------
<h1 id="#title_2" >3、前端每周清单第61期：Angular 6发布，苹果为统一macOS和iOS开发声明式API</h1>
覃云
[http://www.infoq.com/cn/news/2018/05/arch-weekly-61?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/05/arch-weekly-61?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>前端每周清单第61期：Angular 6发布，苹果为统一macOS和iOS开发声明式API</p> <i>By 覃云</i>
---------------
<h1 id="#title_3" >4、文章： 跟着这五步 从0开始搭建你的第一款小程序</h1>
江柳
[http://www.infoq.com/cn/articles/5-steps-build-your-first-mini-program?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/5-steps-build-your-first-mini-program?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/5-steps-build-your-first-mini-program/zh/smallimage/logo-api-1510092752391-1525715762098.jpeg"/><p>4月28日，腾讯云联合InfoQ举办的云+社区技术沙龙，以小程序开发实战为基准点，围绕小程序云上解决方案，serverless后端架构，小游戏底层设计和直播、电商小程序的开发实战五大主题内容，分享最全面的微信小程序设计开发思路以及解决方案。本文整理了讲师演讲精彩内容。</p> <i>By 江柳</i>
---------------
<h1 id="#title_4" >5、文章： 一种更高效的M*N拼图自动还原算法解析</h1>
魏治涛
[http://www.infoq.com/cn/articles/a-more-efficient-jigsaw-puzzle-auto-restore-algorithm?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/a-more-efficient-jigsaw-puzzle-auto-restore-algorithm?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/a-more-efficient-jigsaw-puzzle-auto-restore-algorithm/zh/smallimage/call-for-articles-small-1511955760204-1525773800648.jpg"/><p>恰巧2016年李世石与阿尔法狗对弈，当时我想既然下围棋能够用算法完成，那自动复原拼图应该是更简单的一件事，一定会有算法。人工智能课上老师也讲过复原拼图的A^*算法,上网查资料拼图的复原也大都用A^*算法。不过对于复原拼图来讲，A^*算法和瞎蒙的差别不大，如果M和N的值较小A^*可以适用，当M和N过大时由于搜索空间变得太大就不可行了。那么有没有一种更明确的算法，可以计算出复原拼图的路径呢？</p> <i>By 魏治涛</i>
---------------
<h1 id="#title_5" >6、专访平安科技CTO方国伟：云计算十年，最需要突破的不仅是技术</h1>
蔡芳芳
[http://www.infoq.com/cn/news/2018/05/cloud-ten-years?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/05/cloud-ten-years?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p> 平安科技 CTO 兼总架构师方国伟讲述云计算产业的发展和平安云的演进历程。 </p> <i>By 蔡芳芳</i>
---------------
<h1 id="#title_6" >7、Angular 6发布，新功能详解</h1>
覃云
[http://www.infoq.com/cn/news/2018/05/Angular-6-release-new-function-d?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/05/Angular-6-release-new-function-d?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>5月4日，Angular 6.0.0正式发布，新版本重点关注工具链以及工具链在Angular中的运行速度问题。这次更新还包括框架包（@angular/core，@angular/common，@angular/compiler等）、Angular CLI、Angular Material + CDK，这主要是为了解决兼容问题，这些项目的补丁版本将根据项目需求发布。</p> <i>By 覃云</i>
---------------
<h1 id="#title_7" >8、微软Azure Sphere提高物联网设备安全性</h1>
Alexis Perrier
[http://www.infoq.com/cn/news/2018/05/iot-security-azure-sphere?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/05/iot-security-azure-sphere?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>为了提高物联网设备的安全性，微软在2018年4月的RSA信息安全会议期间发布了Azure Sphere，一种端到端的联网微控制器（MCU）解决方案。 Azure Sphere以由混合微控制器组成的三层体系结构为基础，该混合微控制器运行为IoT而优化的Linux内核，并使用了基于云的安全服务。第一个Azure Sphere芯片MT3620由联发科公司开发，预计将于2018年第三季度公开发售。</p> <i>By Alexis Perrier</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_8" >9、Progress发布NativeScript 4</h1>
Dylan Schiemann
[http://www.infoq.com/cn/news/2018/05/nativescript-4-release?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/05/nativescript-4-release?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>NativeScript 4.0主要是消除了使用NativeScript开发的限制并提升了灵活性，改进了UI视图的灵活性，优化了创建应用程序的模板，新增了简化原生应用程序开发的工具。</p> <i>By Dylan Schiemann</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_9" >10、文章： 一个可供中小团队参考的微服务架构技术栈</h1>
杨波
[http://www.infoq.com/cn/articles/china-microservice-technique?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/china-microservice-technique?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/china-microservice-technique/zh/smallimage/logo-cloud-1525700972375.jpeg"/><p>所以我在参考Spring Cloud微服务技术栈的基础上，结合自身的实战落地经验，也结合国内外一线互联网公司（例如Netflix，点评，携程，Zalando等）的开源实践，综合提出更贴近国内技术文化特色的轻量级的微服务参考技术栈。希望这个参考技术栈对一线的架构师（或者是初创公司）有一个好的指导，能够少走弯路，快速落地微服务架构。</p> <i>By 杨波</i>
---------------