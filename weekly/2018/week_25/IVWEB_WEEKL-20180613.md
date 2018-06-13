## 文章索引
1、 <a href="#1building-a-pub/sub-service-in-house-using-nodejs-and-redis" >Building A Pub/Sub Service In-House Using Node.js And Redis</a><br/>
2、 <a href="#2how-to-turn-your-users-into-advocates" >How To Turn Your Users Into Advocates</a><br/>
3、 <a href="#3因为aiblued成为垂直社交产品里不一样的烟火" >因为ai，Blued成为垂直社交产品里“不一样的烟火”</a><br/>
4、 <a href="#4物联网技术周报第-140-期:-使用流引擎-apache-nifi-和-mqtt-构建一个工业物联网系统" >物联网技术周报第 140 期: 使用流引擎 Apache NiFi 和 MQTT 构建一个工业物联网系统</a><br/>
5、 <a href="#5专访martijn-verburg关于adoptopenjdk与nestmates" >专访Martijn Verburg，关于AdoptOpenJDK与Nestmates</a><br/>
6、 <a href="#6苹果发布core-ml-2" >苹果发布Core ML 2</a><br/>
7、 <a href="#7github的未来可期" >GitHub的未来，可期</a><br/><h1 id="#title_0" >1、Building A Pub/Sub Service In-House Using Node.js And Redis</h1>
Dhimil Gosalia
[https://www.smashingmagazine.com/2018/06/pub-sub-service-in-house-node-js-redis/](https://www.smashingmagazine.com/2018/06/pub-sub-service-in-house-node-js-redis/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/06/pub-sub-service-in-house-node-js-redis/" />
              <title>Building A Pub/Sub Service In-House Using Node.js And Redis</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>Building A Pub/Sub Service In-House Using Node.js And Redis</h1>
                  
                    
                    <address>Dhimil Gosalia</address>
                  
                  <time datetime="2018-06-12T15:30:58&#43;02:00" class="op-published">2018-06-12T15:30:58+02:00</time>
                  <time datetime="2018-06-12T20:27:20&#43;00:00" class="op-modified">2018-06-12T20:27:20+00:00</time>
                </header>
                

<p>Today’s world operates in real time. Whether it’s trading stock or ordering food, consumers today expect immediate results. Likewise, we all expect to know things immediately &mdash; whether it’s in news or sports. Zero, in other words, is the new hero.</p>

<p>This applies to software developers as well &mdash; arguably some of the most impatient people! Before diving into BrowserStack’s story, it would be remiss of me not to provide some background about Pub/Sub. For those of you who are familiar with the basics, feel free to skip the next two paragraphs.</p>

<p>Many applications today rely on real-time data transfer. Let’s look closer at an example: social networks. <strong>The likes of Facebook and Twitter generate relevant feeds</strong>, and you (via their app) consume it and spy on your friends. They accomplish this with a messaging feature, wherein if a user generates data, it will be posted for others to consume in nothing short of a blink. Any significant delays and users will complain, usage will drop, and if it persists, churn out. The stakes are high, and so are user expectations. So how do services like WhatsApp, Facebook, TD Ameritrade, Wall Street Journal and GrubHub support high volumes of real-time data transfers?</p>



<aside class="product-panel product-panel__tilted product-panel--book" data-audience="non-subscriber">
    <div class="container product-panel--book__container">
      <div class="panel__description panel__description--book">
    <p>Nope, we can't do any magic tricks, but we have articles,  get a seasoned selection of magic front-end tricks — e.g. <strong>live designing sessions</strong> and perf audits, too. <em>Just sayin'</em>! ;-)</p>

      <a href="http://smashed.by/perfpanelmembership" class="btn btn--green btn--large">
        Explore Smashing Wizardry&nbsp;→
      </a>
      </div>
      <div class="panel__image panel__image--book">
        <a href="http://smashed.by/perfpanelmembership" class="books__book__image">
        <div class="books__book__img">
          <img src="https://www.smashingmagazine.com/images/smashing-cat/cat-wizard.svg" alt="Smashing Cat, just preparing to do some magic stuff." width="310" height="400">
        </div>
      </a>
      </div>
    </div>
  </aside>





<div class="c-garfield-the-cat">


<p>All of them use a similar software architecture at a high level called a “Publish-Subscribe” model, commonly referred to as Pub/Sub.</p>

<blockquote>“In </blockquote>

<p>Bored by the definition? Back to our story.</p>

<p>At BrowserStack, all of our products support (in one way or another) software with a substantial real-time dependency component &mdash; whether its automate tests logs, freshly baked browser screenshots, or 15fps mobile streaming.</p>

<p>In such cases, if a single message drops, <strong>a customer can lose information vital for preventing a bug</strong>. Therefore, we needed to scale for varied data size requirements. For example, with device logger services at a given point of time, there may be 50MB of data generated under a single message. Sizes like this could crash the browser. Not to mention that BrowserStack’s system would need to scale for additional products in the future.</p>

<p>As the size of data for each message differs from a few bytes to up to 100MB, we needed a scalable solution that could support a multitude of scenarios. In other words, we sought a sword that could cut all cakes. In this article, I will discuss the why, how, and results of building our Pub/Sub service in-house.</p>

<p>Through the lens of BrowserStack’s real-world problem, you will get <strong>a deeper understanding of the requirements and process of building your very own Pub/Sub</strong>.</p>

<h3 id="our-need-for-a-pub-sub-service">Our Need For A Pub/Sub Service</h3>

<p>BrowserStack has around 100M+ messages, each of which is somewhere between approximately 2 bytes and 100+ MB. These are passed around the world at any moment, all at different Internet speeds.</p>

<p>The largest generators of these messages, by message size, are our BrowserStack Automate products. Both have real-time dashboards displaying all requests and responses for each command of a user test. So, if someone runs a test with 100 requests where the average request-response size is 10 bytes, this transmits 1&times;100&times;10 = 1000 bytes.</p>

<p>Now let’s consider the larger picture as &mdash; of course &mdash; we don’t run just one test a day. More than approximately 850,000 BrowserStack  tests are run with BrowserStack each and every day. And yes, we average around 235 request-response per test. Since users can take screenshots or ask for page sources in Selenium, our average request-response size is approximately 220 bytes.</p>

<p>So, going back to our calculator:</p>

<blockquote>850,000&times;235&times;220 = 43,945,000,000 bytes (approx.) or only 43.945GB per day</blockquote>

<p>Now let’s talk about . Surely we have Automate as our winner in form of size of data. However, Live products take the lead when it comes to the number of messages passed. For every live test, about 20 messages are passed each minute it turns. We run around 100,000 live tests, which each test averaging around 12 mins meaning:</p>

<blockquote>100,000&times;12&times;20 = 24,000,000 messages per day</blockquote>

<p>Now for the awesome and remarkable bit: We build, run, and maintain the application for this called pusher with 6 t1.micro instances of ec2. The cost of running the service? About $70 <strong>per month</strong>.</p>

<h3 id="choosing-to-build-vs-buying">Choosing To Build vs. Buying</h3>

<p>First things first: As a startup, like most others, we were always excited to build things in-house. But we still evaluated a few services out there. The primary requirements we had were:</p>

<ol>
<li>Reliability and stability,</li>
<li>High performance, and</li>
<li>Cost-effectiveness.</li>
</ol>

<p>Let’s leave the cost-effectiveness criteria out, as I can’t think of any external services that cost under $70 a month (tweet me if know you one that does!). So our answer there is obvious.</p>

<p>In terms of reliability and stability, we found companies that provided Pub/Sub as a service with 99.9+ percent uptime SLA, but there were many T&amp;C’s attached. The problem is not as simple as you think, especially when you consider the vast lands of the open Internet that lie between the system and client. Anyone familiar with Internet infrastructure knows stable connectivity is the biggest challenge. Additionally, the amount of data sent depends on traffic. For example, a data pipe that’s at zero for one minute may burst during the next. Services providing adequate reliability during such burst moments are rare (Google and Amazon).</p>


  <div id="sponsors-article" data-impression="true" class="c-promo-box c-promo-box--ad sponsors hidden" data-audience="non-subscriber" data-remove="true"></div>



<p>Performance for our project means <strong>obtaining and sending data to all listening nodes at near zero latency</strong>. At BrowserStack, we utilize cloud services (AWS) along with co-location hosting. However, our publishers and/or subscribers could be placed anywhere. For example, it may involve an AWS application server generating much-needed log data, or terminals (machines where users can securely connect for testing). Coming back to the open Internet issue again, if we were to reduce our risk we would have to ensure our Pub/Sub leveraged the best host services and AWS.</p>

<p>Another essential requirement was the ability to transmit all types of data (Bytes, text, weird media data, etc.). With all considered, it did not make sense to rely on a third-party solution to support our products. In turn, we decided to revive our startup spirit, rolling up our sleeves to code our own solution.</p>

<h3 id="building-our-solution">Building Our Solution</h3>

<p>Pub/Sub by design means there will be a publisher, generating and sending data, and a Subscriber accepting and processing it. This is similar to a radio: A radio channel broadcasts (publishes) content everywhere within a range. As a subscriber, you can decide whether to tune into that channel and listen (or turn off your radio altogether). </p>

<p>Unlike the radio analogy where data is free for all and anyone can decide to tune in, in our digital scenario we need authentication which means data generated by the publisher could only be for a single particular client or subscriber.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0f270e19-40d6-4a72-b5fe-91383f49c94b/pubsub.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0f270e19-40d6-4a72-b5fe-91383f49c94b/pubsub.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0f270e19-40d6-4a72-b5fe-91383f49c94b/pubsub.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0f270e19-40d6-4a72-b5fe-91383f49c94b/pubsub.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0f270e19-40d6-4a72-b5fe-91383f49c94b/pubsub.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0f270e19-40d6-4a72-b5fe-91383f49c94b/pubsub.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0f270e19-40d6-4a72-b5fe-91383f49c94b/pubsub.jpg"
			sizes="100vw"
			alt="Basic working of Pub/Sub"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Basic working of Pub/Sub ()
		</figcaption>
	
</figure>


<p>Above is a diagram providing an example of a good Pub/Sub with:</p>

<ul>
<li><strong>Publishers</strong><br />
Here we have two publishers generating messages based on pre-defined logic. In our radio analogy, these are our radio jockeys creating the content.</li>
<li><strong>Topics</strong><br />
There are two here, meaning there are two types of data. We can say these are our radio channels 1 and 2.</li>
<li><strong>Subscribers</strong><br />
We have three that each read data on a particular topic. One thing to notice is that Subscriber 2 is reading from multiple topics. In our radio analogy, these are the people who are tuned into a radio channel. </li>
</ul>

<p>Let’s start understanding the necessary requirements for the service.</p>

<ol>
<li><strong>An evented component</strong><br />
This kicks in only when there is something to kick in.</li>
<li><strong>Transient storage</strong><br />
This keeps data persisted for a short duration so if the subscriber is slow, it still has a window to consume it.</li>
<li><strong>Reducing the latency</strong><br />
Connecting two entities over a network with minimum hops and distance.</li>
</ol>

<p>We picked a technology stack that fulfilled the above requirements:</p>

<ol>
<li><strong>Node.js</strong><br />
Because why not? Evented, we wouldn’t need heavy data processing, plus it’s easy to onboard.</li>
<li><strong>Redis</strong><br />
Supports perfectly short-lived data. It has all the capabilities to initiate, update and auto-expire. It also puts less load on the application.</li>
</ol>

<h4 id="node-js-for-business-logic-connectivity">Node.js For Business Logic Connectivity</h4>

<p>Node.js is a nearly perfect language when it comes to writing code incorporating IO and events. Our particular given problem had both, making this option the most practical for our needs.</p>

<p>Surely other languages such as Java could be more optimized, or a language like Python offers scalability. However, the cost of starting with these languages is so high that a developer could finish writing code in Node in the same duration. </p>

<p>To be honest, if the service had a chance of adding more complicated features, we could have looked at other languages or a completed stack. But here it is a marriage made in heaven. Here is our <em>package.json</em>:</p>

<pre class="break-out"><code class="language-javascript">{
  "name": "Pusher",
  "version": "1.0.0",
  "dependencies": {
    "bstack-analytics": "*****", // Hidden for BrowserStack reasons. :)
    "ioredis": "^2.5.0",
    "socket.io": "^1.4.4"
  },
  "devDependencies": {},
  "scripts": {
    "start": "node server.js"
  }
}
</code></pre>

<p>Very simply put, we believe in minimalism especially when it comes to writing code. On the other hand, we could have used libraries like Express to write extensible code for this project. However, our startup instincts decided to pass on this and to save it for the next project. Additional tools we used:</p>

<ul>
<li><strong>ioredis</strong><br />
This is one of the most supported libraries for Redis connectivity with Node.js used by companies including Alibaba.</li>
<li><strong>socket.io</strong><br />
The best library for graceful connectivity and fallback with WebSocket and HTTP.</li>
</ul>

<h4 id="redis-for-transient-storage">Redis For Transient Storage</h4>

<p>Redis as a service scales is heavily reliable and configurable. Plus there are many reliable managed service providers for Redis, including AWS. Even if you don’t want to use a provider, Redis is easy to get started with.</p>

<p>Let’s break down the configurable part. We started off with the usual master-slave configuration, but Redis also comes with cluster or sentinel modes. Every mode has its own advantages.</p>

<p>If we could share the data in some way, a Redis cluster would be the best choice. But if we shared the data by any heuristics, <strong>we have less flexibility as the heuristic has to be followed across</strong>. Fewer rules, more control is good for life!</p>

<p>Redis Sentinel works best for us as data lookup is done in just one node, connecting at a given point in time while data is not sharded. This also means that even if multiple nodes are lost, the data is still distributed and present in other nodes. So you have more  HA and less chances of loss. Of course, this removed the pros from having a cluster, but our use case is different.</p>




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




<h3 id="architecture-at-30000-feet">Architecture At 30000 Feet</h3>

<p>The diagram below provides a very high-level picture of how our  dashboards work. Remember the real-time system that we had from the earlier section?</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a6d293f2-45c9-46e4-961c-ee9ba2de088e/automate-dashboard.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a6d293f2-45c9-46e4-961c-ee9ba2de088e/automate-dashboard.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a6d293f2-45c9-46e4-961c-ee9ba2de088e/automate-dashboard.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a6d293f2-45c9-46e4-961c-ee9ba2de088e/automate-dashboard.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a6d293f2-45c9-46e4-961c-ee9ba2de088e/automate-dashboard.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a6d293f2-45c9-46e4-961c-ee9ba2de088e/automate-dashboard.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a6d293f2-45c9-46e4-961c-ee9ba2de088e/automate-dashboard.jpg"
			sizes="100vw"
			alt="BrowserStack’s real-time Automate and App Automate dashboards."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			BrowserStack’s real-time Automate and App Automate dashboards ()
		</figcaption>
	
</figure>


<p>In our diagram, our main workflow is highlighted with thicker borders. The “automate” section consists of:</p>

<ol>
<li><strong>Terminals</strong><br />
Comprised of the pristine versions of Windows, OSX, Android or iOS that you get while testing on BrowserStack.</li>
<li><strong>Hub</strong><br />
The point of contact for all your Selenium and Appium tests with BrowserStack.</li>
</ol>

<p>The “user service” section here is our gatekeeper, ensuring data is sent to and saved for the right individual. It is also our security keeper. The “pusher” section incorporates the heart of what we discussed in this article. It consists of the usual suspects including:</p>

<ol>
<li><strong>Redis</strong><br />
Our transient storage for messages, where in our case automate logs are temporarily stored.</li>
<li><strong>Publisher</strong><br />
This is basically the entity that obtains data from the hub. All your request responses are captured by this component which writes to Redis with <code>session_id</code> as the channel.</li>
<li><strong>Subscriber</strong><br />
This reads data from Redis generated for the <code>session_id</code>. It is also the web server for clients to connect via WebSocket (or HTTP) to get data and then sends it to authenticated clients.</li>
</ol>

<p>Finally, we have the user’s browser section, representing an authenticated WebSocket connection to ensure <code>session_id</code> logs are sent. This enables the front-end JS to parse and beautify it for users.</p>

<p>Similar to the logs service, we have pusher here that is being used for other product integrations. Instead of <code>session_id</code>, we use another form of ID to represent that channel. This all works out of pusher!</p>

<h3 id="conclusion-tldr">Conclusion (TLDR)</h3>

<p>We’ve had considerable success in building out Pub/Sub. To sum up why we built it in-house:</p>

<ol>
<li>Scales better for our needs;</li>
<li>Cheaper than outsourced services;</li>
<li>Full control over the overall architecture.</li>
</ol>

<p>Not to mention that JS is the perfect fit for this kind of scenario. Event loop and massive amount of IO is what the problem needs! JavaScript is magic of single pseudo thread. </p>

<p>Events and Redis as a system keep things simple for developers, as you can obtain data from one source and push it to another via Redis. So we built it.</p>

<p>If the usage fits into your system, I recommend doing the same!</p>




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
<h1 id="#title_1" >2、How To Turn Your Users Into Advocates</h1>
Nick Babich
[https://www.smashingmagazine.com/2018/06/how-to-turn-your-users-into-advocates/](https://www.smashingmagazine.com/2018/06/how-to-turn-your-users-into-advocates/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/06/how-to-turn-your-users-into-advocates/" />
              <title>How To Turn Your Users Into Advocates</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>How To Turn Your Users Into Advocates</h1>
                  
                    
                    <address>Nick Babich</address>
                  
                  <time datetime="2018-06-12T12:15:44&#43;02:00" class="op-published">2018-06-12T12:15:44+02:00</time>
                  <time datetime="2018-06-12T20:27:20&#43;00:00" class="op-modified">2018-06-12T20:27:20+00:00</time>
                </header>
                

<p>(<em>This article is kindly sponsored by Adobe</em>.) As businesses become more consumer-oriented, competition grows fiercer. Thousands of companies worldwide are struggling each day to gain more market share and to win over new consumers. A significant number of companies concentrate only on acquiring new customers — they allocate enormous marketing budgets trying to strengthen their customer base. But acquiring new customers only becomes harder and more expensive. According to the  by Adobe, ad costs are seeing growth five times faster than US inflation rates.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/196be0bd-58df-4a0e-9aa2-7d7c3cdddf37/image-0-user-advocates.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/196be0bd-58df-4a0e-9aa2-7d7c3cdddf37/image-0-user-advocates.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/196be0bd-58df-4a0e-9aa2-7d7c3cdddf37/image-0-user-advocates.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/196be0bd-58df-4a0e-9aa2-7d7c3cdddf37/image-0-user-advocates.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/196be0bd-58df-4a0e-9aa2-7d7c3cdddf37/image-0-user-advocates.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/196be0bd-58df-4a0e-9aa2-7d7c3cdddf37/image-0-user-advocates.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/196be0bd-58df-4a0e-9aa2-7d7c3cdddf37/image-0-user-advocates.png"
			sizes="100vw"
			alt="Cost of advertising increase from 2014 to 2016 in the US."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Cost of advertising increase from 2014 to 2016 in the US. ()
		</figcaption>
	
</figure>


<p>In an attempt to find new customers, companies often forget to think of ways to engage with existing users. However, acquiring a new customer is anywhere from  than retaining an existing one.</p>

<p>To succeed in the modern market, companies need to do more than produce an excellent product or provide reliable service: They need to <strong>turn their faithful users into advocates</strong>.</p>

<p>In this article, I’m going to discuss:</p>

<ul>
<li>who are product advocates,</li>
<li>actionable ways to turn your customers into brand advocates,</li>
<li>what to consider when creating a strategy for advocacy.</li>
</ul>


<div class="c-garfield-the-cat">


<h3 id="who-are-product-advocates">Who Are Product Advocates?</h3>

<p>Brand advocates are people who feel so positively about a brand that they want to recommend it to others. They’re often called volunteer marketers because they pass on positive word-of-mouth messages about the brand to other people (both offline and online). Advocates do it organically — money is not the primary reason why they promote a brand or product; they promote it because they truly believe in the brand.</p>

<h4 id="why-advocacy-is-great">Why Advocacy Is Great</h4>

<p>Who sells your products or services? You might think it the sole responsibility of the sales and marketing team. Yes, for a long time, sales and marketing was the team responsible for product growth, but the situation has changed. Your customers have quickly become the most critical people to sell what you’re offering. More specifically, your customers have become keen advocates for your product or service. Advocates can be a key part of growing your customer base:</p>

<ul>
<li><strong>Organic promotion</strong><br />
Brand advocacy is the modern form of traditional word-of-mouth marketing. And word of mouth about a product or service is one of the most powerful forms of advertising; when regular people recommend a product, their message carries more weight than a paid advertisement. According to a , word of mouth can generate more than double the sales of paid advertising.</li>
<li><strong>Authentic reviews and testimonials</strong><br />
Social proof plays a vital part in the process of product selection. Reading reviews and testimonials is the first step potential users make when researching a product; reviews and testimonials play a role in the wisdom of the crowd. And advocates can be excellent sources of reviews and testimonials. According to , 19% of brand advocates share their experiences online in their networks — twice as many as non-brand advocates.</li>
<li><strong>Brand awareness</strong><br />
Advocates use the power of social channels to amplify a brand’s exposure. As a result, they can reach out to people you might not have considered.</li>
<li><strong>Valuable customer feedback loops</strong><br />
Advocates can provide valuable customer insights. Their insights can help you formulate more focused, customer-centric product road maps.</li>
</ul>

<h4 id="loyalty-and-advocacy-are-not-the-same-thing">Loyalty And Advocacy Are Not The Same Thing</h4>

<p>Many people confuse loyalists and brand advocates. Brand loyalists and advocates aren’t the same groups of customers. Loyal customers are people who stay with your brand. For example, if you run an e-commerce store, loyal customers will be your return buyers. But they might not actively promote your brand to others (i.e. they might not be comfortable with sharing information about your brand publicly).</p>

<p>Advocates, on the other hand, are people who not only are loyal to your brand, but also <strong>proactively</strong> talk up and advocate for your company to their own networks. The word &ldquo;proactive&rdquo; is key here. Advocates invest in the success of your brand heavily. The goal is to turn brand loyalists into brand advocates.</p>

<h4 id="who-has-the-potential-to-become-a-brand-advocate">Who Has The Potential To Become A Brand Advocate?</h4>

<p>Your existing customers are the most apparent advocates for your brand. Let’s define the groups of existing users who likely to be interested in a brand advocacy program:</p>

<ul>
<li><strong>Promoters</strong><br />
Promoters are people who participate in an NPS survey, a single-question survey that sounds like, &ldquo;On a scale of 0 to 10, how likely are you to recommend us to your friends, family, or colleagues?&rdquo;, and who answers 9 or 10.</li>
<li><strong>Referrers</strong><br />
These are existing customers who refer new users to your product.</li>
<li><strong>Repeat visitors</strong><br />
Repeat visitors are highly engaged and interested in the content you provide.</li>
<li><strong>Social sharers</strong><br />
These are people who share your content on social media on a regular basis.</li>
<li><strong>Critics</strong><br />
Critics leave feedback about your product or service.</li>
</ul>

<p>However, your customers are not your only advocates. The best brand advocates are people who work with you: your employees. Communications marketing firm Edelman found that  view employees as very credible sources of information about a brand.</p>

<h3 id="how-to-encourage-advocacy">How To Encourage Advocacy</h3>

<p>Getting customers to advocate for a brand is a lot different from getting them to buy products or services. Users don’t become advocates without reason. To acquire a brand ambassador, companies need to create the conditions that generate not only happy customers, but true customer advocates.</p>

<h4 id="don-t-try-to-force-it">Don’t Try To Force It</h4>

<p>Pushing people towards a particular type of action typically results in them doing the opposite. Don’t try to force advocacy; it should be completely natural.</p>

<h4 id="create-a-delightful-ux">Create A Delightful UX</h4>

<p>Designing for the user experience has a lot more to it than making a product usable. It’s also important to generate a certain positive emotional effect while people are using a product. After all, user experience is about how users <em>feel</em> when they interact with a product. As humans, we establish some sort of an emotional connection with all of the products we use. It’s possible to establish a deeper connection with a product by adding elements that generate positive emotions at multiple points along that journey.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/432c3365-23f2-476f-ac8e-82557003c46a/image-1-user-advocates.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/432c3365-23f2-476f-ac8e-82557003c46a/image-1-user-advocates.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/432c3365-23f2-476f-ac8e-82557003c46a/image-1-user-advocates.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/432c3365-23f2-476f-ac8e-82557003c46a/image-1-user-advocates.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/432c3365-23f2-476f-ac8e-82557003c46a/image-1-user-advocates.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/432c3365-23f2-476f-ac8e-82557003c46a/image-1-user-advocates.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/432c3365-23f2-476f-ac8e-82557003c46a/image-1-user-advocates.png"
			sizes="100vw"
			alt="Pleasure is at the top of Aaron Walter’s pyramid of emotional design. Designers should have a goal to please their users and make them feel happy when they use the product."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Pleasure is at the top of . Designers should have a goal to please their users and make them feel happy when they use the product.
		</figcaption>
	
</figure>


<p>The reward for brands that connect with customers’ emotions in a positive way can be substantial. People love to talk about products that make them happy.</p>

<p>Duolingo is an excellent example of incorporating delight in UX. What makes Duolingo thrive is its smooth functionality wrapped in a friendly design with elements of gamification. Each lesson is presented as a challenge to the user. When users accomplish a task, Duolingo celebrates this progress with the users by rewarding them with a badge. By presenting the learning process as a challenge, the service creates a sense of development and accomplishment. The latter has a significant impact on delight.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/081622b9-674a-4625-ad9d-6463248e7766/image-2-user-advocates.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/081622b9-674a-4625-ad9d-6463248e7766/image-2-user-advocates.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/081622b9-674a-4625-ad9d-6463248e7766/image-2-user-advocates.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/081622b9-674a-4625-ad9d-6463248e7766/image-2-user-advocates.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/081622b9-674a-4625-ad9d-6463248e7766/image-2-user-advocates.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/081622b9-674a-4625-ad9d-6463248e7766/image-2-user-advocates.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/081622b9-674a-4625-ad9d-6463248e7766/image-2-user-advocates.png"
			sizes="100vw"
			alt="Evoking a positive emotional response in users is key to creating a delightful UX. Duolingo transforms the task of learning a new language into an inviting experience. This motivates users to level up and achieve mastery in the discipline."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Evoking a positive emotional response in users is key to creating a delightful UX. Duolingo transforms the task of learning a new language into an inviting experience. This motivates users to level up and achieve mastery in the discipline.
		</figcaption>
	
</figure>


<h4 id="focus-on-building-trust">Focus On Building Trust</h4>

<p>Advocacy is always a risky business. When discussing a company, advocates are putting their reputation on the line. They know that if something goes wrong, people will blame them for it. But one thing can alleviate those fears: trust. The more they trust you, the more easily they will recommend your product.</p>

<p>Below are a few things that play a significant role in building trust.</p>

<h5 id="stand-by-what-you-offer">Stand By What You Offer</h5>

<p>Deliver what you promise, and promptly solve problems when something goes wrong. That’s the obvious starting point, but you’d be surprised at how many fail to execute well on this simple principle.</p>

<p>) and an incredibly lenient return policy. By making returns as simple as possible, Casper makes the process of ordering a mattress as comfortable as possible. Casper not only stands by its products, but also trusts its customers to be honest when requesting a refund.</p>

<h5 id="make-it-easy-to-reach-you">Make It Easy To Reach You</h5>

<p>When customers interact with a brand, they expect to have a dialog, not a monologue. They want you to listen to them and demonstrate that you care about them as individuals. This is especially important when users face problems. Users should be able to reach a company through whichever channel is most convenient to them at the time. Whether they prefer face-to-face communication, email, a phone call or a message in a social network, make sure you’re available by all those means.</p>

<h5 id="ask-for-feedback">Ask For Feedback</h5>

<p>Asking users for feedback not only is one of the best ways to gain insight into your business, but is also a great way to build relationships. When you ask users for feedback, they understand that you actually care about them and want to make their experience better.</p>

<p>However, the way you ask for feedback plays a vital role in how users react to it. Generic surveys with questions like, &ldquo;Are you happy with our service? Answer yes or no&rdquo; won’t deliver many insights. You need to research users problems first, get to know what is bothering them, and only after that ask questions that your users will be happy to answer.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ef4f49b2-7894-49e9-9ffc-0cfe699e1483/image-3-user-advocates.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ef4f49b2-7894-49e9-9ffc-0cfe699e1483/image-3-user-advocates.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ef4f49b2-7894-49e9-9ffc-0cfe699e1483/image-3-user-advocates.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ef4f49b2-7894-49e9-9ffc-0cfe699e1483/image-3-user-advocates.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ef4f49b2-7894-49e9-9ffc-0cfe699e1483/image-3-user-advocates.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ef4f49b2-7894-49e9-9ffc-0cfe699e1483/image-3-user-advocates.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ef4f49b2-7894-49e9-9ffc-0cfe699e1483/image-3-user-advocates.png"
			sizes="100vw"
			alt="DigitalOcean makes users feel that their opinions carry weight."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			DigitalOcean makes users feel that their opinions carry weight.
		</figcaption>
	
</figure>


<h5 id="encourage-your-customers-to-talk-about-you">Encourage Your Customers To Talk About You</h5>

<p>Despite the digital world constantly changing, one trend remains the same: When it comes to evaluating a new product or service, potential clients trust the advice and expertise of existing clients. To build trust, you need to encourage users to talk about you. Here are a few things to remember when asking users for a review:</p>

<ul>
<li>Find the right time to ask for a review. The request for a review should be a natural part of the customer journey.</li>
</ul>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8dd94b00-a6bf-4f8b-badb-febaeb3421e7/image-4-user-advocates.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8dd94b00-a6bf-4f8b-badb-febaeb3421e7/image-4-user-advocates.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8dd94b00-a6bf-4f8b-badb-febaeb3421e7/image-4-user-advocates.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8dd94b00-a6bf-4f8b-badb-febaeb3421e7/image-4-user-advocates.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8dd94b00-a6bf-4f8b-badb-febaeb3421e7/image-4-user-advocates.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8dd94b00-a6bf-4f8b-badb-febaeb3421e7/image-4-user-advocates.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8dd94b00-a6bf-4f8b-badb-febaeb3421e7/image-4-user-advocates.png"
			sizes="100vw"
			alt="Booking.com makes asking for feedback a natural part of the user journey. When Booking.com users check out at a hotel, the service asks them to review their stay."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Booking.com makes asking for feedback a natural part of the user journey. When Booking.com users check out at a hotel, the service asks them to review their stay.
		</figcaption>
	
</figure>


<ul>
<li>Focus on quality, not quantity. Stay away from reviews and testimonials that praise the product. &ldquo;Amazing product, highly recommended&rdquo; doesn’t say much to potential customers. Prioritize testimonials that have context and that tell a story. This testimonial from Amazon illustrates exactly what I mean:</li>
</ul>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8925c6db-94c4-41e8-a97a-26a51678aaf8/image-5-user-advocates.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8925c6db-94c4-41e8-a97a-26a51678aaf8/image-5-user-advocates.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8925c6db-94c4-41e8-a97a-26a51678aaf8/image-5-user-advocates.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8925c6db-94c4-41e8-a97a-26a51678aaf8/image-5-user-advocates.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8925c6db-94c4-41e8-a97a-26a51678aaf8/image-5-user-advocates.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8925c6db-94c4-41e8-a97a-26a51678aaf8/image-5-user-advocates.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8925c6db-94c4-41e8-a97a-26a51678aaf8/image-5-user-advocates.png"
			sizes="100vw"
			alt="Product reviews can act as social proof and encourage prospects to convert. The best reviews not only describe the pros and cons of a product, but tell a story of how the product benefits the user."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Product reviews can act as social proof and encourage prospects to convert. The best reviews not only describe the pros and cons of a product, but tell a story of how the product benefits the user.
		</figcaption>
	
</figure>


<h4 id="offer-a-loyalty-program">Offer A Loyalty Program</h4>

<p>A loyalty program is a tried-and-true technique to show users your gratitude. As mentioned above, loyalty and advocacy aren’t the same thing. Still, a loyalty program can be used to increase the number of brand advocates:</p>

<ul>
<li><strong>Beat negative experience.</strong><br />
A loyalty program might come in handy when users face a problem and complain about it. Of course, it’s essential to respond to the user request and provide a solution to the problem as fast as you can. But once the issue has been resolved, you can offer the customer loyalty points as an apology. This might help you to win back frustrated users, and maybe they can even advocate for your brand.</li>
<li><strong>Encourage social activity.</strong><br />
Motivate users to participate in social activities. For example, reward users by awarding loyalty points every time they tweet or post to Facebook, write a review, or refer their friends.</li>
</ul>

<h4 id="offer-a-referral-program">Offer A Referral Program</h4>

<p>Running a referral program is a great way to encourage existing users to share information about your business. A successful referral program can help you achieve two key goals:</p>

<ul>
<li>acquire new customers,</li>
<li>turn existing customers into brand advocates.</li>
</ul>

<p>Moreover, studies confirm that ), resulting in an overall higher customer lifetime value.</p>

<p>The critical point with a referral strategy is to find out the right incentive to make users spread the word about your product. Dropbox’s referral program is possibly one of the most famous cases of referral marketing done right. The service grew. When existing Dropbox users referred Dropbox to someone and the person signed up, both got extra free space. Apparently, Dropbox’s tremendous rise is not all due to the referral program; the service provides an excellent user experience, and the team continually improves its product. But the referral program was a great accelerator of the process of promotion.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bcdd82be-718c-4afc-8e9a-afbfd1212896/image-6-user-advocates.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bcdd82be-718c-4afc-8e9a-afbfd1212896/image-6-user-advocates.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bcdd82be-718c-4afc-8e9a-afbfd1212896/image-6-user-advocates.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bcdd82be-718c-4afc-8e9a-afbfd1212896/image-6-user-advocates.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bcdd82be-718c-4afc-8e9a-afbfd1212896/image-6-user-advocates.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bcdd82be-718c-4afc-8e9a-afbfd1212896/image-6-user-advocates.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bcdd82be-718c-4afc-8e9a-afbfd1212896/image-6-user-advocates.png"
			sizes="100vw"
			alt="Dropbox offered a two-sides referral program. Both advocate and referrer are rewarded for completing the desired task."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Dropbox offered a two-sides referral program. Both advocate and referrer are rewarded for completing the desired task.
		</figcaption>
	
</figure>


<p>Uber is an excellent example of how a referral program baked into the service from day one can boost adoption. When Uber launched, it was quite a revolutionary service that brought the sharing economy to the transportation industry. People had to adapt to this new format of ridesharing — many potential users had doubts that stopped them from trying the new experience. The referral program was an excellent tool to alleviate fears. The incentive for participation in the program is straightforward: The service offers a free ride to both the referrer and the new rider upon a successful referral. A free ride is an excellent opportunity to get to know the service. This way, Uber gives new customers the perfect introduction to the service.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/be6c2b6b-a9bd-4bfd-b0ca-d549b6e762e0/image-7-user-advocates.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/be6c2b6b-a9bd-4bfd-b0ca-d549b6e762e0/image-7-user-advocates.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/be6c2b6b-a9bd-4bfd-b0ca-d549b6e762e0/image-7-user-advocates.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/be6c2b6b-a9bd-4bfd-b0ca-d549b6e762e0/image-7-user-advocates.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/be6c2b6b-a9bd-4bfd-b0ca-d549b6e762e0/image-7-user-advocates.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/be6c2b6b-a9bd-4bfd-b0ca-d549b6e762e0/image-7-user-advocates.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/be6c2b6b-a9bd-4bfd-b0ca-d549b6e762e0/image-7-user-advocates.png"
			sizes="100vw"
			alt="Uber’s referral program"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Uber’s referral program
		</figcaption>
	
</figure>


<p>Both Dropbox and Uber integrated the referral program very naturally into the product experience. For Dropbox users, the referral program is presented as the final step of the onboarding process — at the point when users already know what benefits the product brings to them and when they’ll be most likely to participate in the program. As for Uber, the referral program has its own option in app’s main menu.</p>

<h4 id="personalize-customer-experiences">Personalize Customer Experiences</h4>

<p>Personalization allows brands to build deeper connections with their customers. It feels great when a product offers an experience that feels tailored especially to us. A personalized experience is what often drives a customer to say, &ldquo;This is the brand for me.&rdquo;</p>

<p>It’s possible to make the experience more personal by gathering information on customers and using it to deliver more relevant content. For example, you could have an intuitive interface that adjusts exactly the way the user expects. Netflix is an excellent example of earning loyalty based on providing a personalized experience. The service offers content suggestions based on the user’s viewing history. Netflix also notifies users when new seasons of their favorite TV shows are released.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2fd6dd61-c1e7-4bb8-a06a-c2c3551e7229/image-8-user-advocates.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2fd6dd61-c1e7-4bb8-a06a-c2c3551e7229/image-8-user-advocates.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2fd6dd61-c1e7-4bb8-a06a-c2c3551e7229/image-8-user-advocates.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2fd6dd61-c1e7-4bb8-a06a-c2c3551e7229/image-8-user-advocates.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2fd6dd61-c1e7-4bb8-a06a-c2c3551e7229/image-8-user-advocates.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2fd6dd61-c1e7-4bb8-a06a-c2c3551e7229/image-8-user-advocates.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2fd6dd61-c1e7-4bb8-a06a-c2c3551e7229/image-8-user-advocates.png"
			sizes="100vw"
			alt="Netflix does a great job of personalizing its mobile push notifications."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Netflix does a great job of personalizing its mobile push notifications.
		</figcaption>
	
</figure>


<h4 id="leverage-the-power-of-social-media">Leverage The Power Of Social Media</h4>

<p>The power of word of mouth created by brand advocates is amplified through social media. In fact, if there’s one place your company should look for brand advocates, it’s on your social media channels. Today,  use social media channels to engage with friends, family and the people they know. Thus, it’s essential to practice social listening — listen to what your current customers and advocates are saying about your brand — and respond to their comments accordingly.</p>

<h5 id="choose-the-social-networks-most-effective-to-your-business">Choose The Social Networks Most Effective To Your Business</h5>

<p>It’s extremely important to know where your audience lives on social media and where potential advocates could have the most influence.</p>

<h5 id="carefully-choose-content-to-publish">Carefully Choose Content To Publish</h5>

<p>Before posting anything on social media, ask yourself two simple questions, &ldquo;Does it benefit our company?&rdquo; and “Does it meet our audience’s needs?” Ideally, you should post content that both reflects your business’ goals and satisfies the needs of your target audience.</p>

<h5 id="respond-to-user-feedback">Respond To User Feedback</h5>

<p>Recognizing and responding to positive feedback is particularly important over social media. Reward the people who stand out in your community. If you have a customer who wants to engage with you, engage with them. Give them as much love as they’re giving you.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/645edeb9-a9c6-4ed0-8cde-7fb9ea59e419/image-9-user-advocates.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/645edeb9-a9c6-4ed0-8cde-7fb9ea59e419/image-9-user-advocates.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/645edeb9-a9c6-4ed0-8cde-7fb9ea59e419/image-9-user-advocates.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/645edeb9-a9c6-4ed0-8cde-7fb9ea59e419/image-9-user-advocates.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/645edeb9-a9c6-4ed0-8cde-7fb9ea59e419/image-9-user-advocates.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/645edeb9-a9c6-4ed0-8cde-7fb9ea59e419/image-9-user-advocates.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/645edeb9-a9c6-4ed0-8cde-7fb9ea59e419/image-9-user-advocates.png"
			sizes="100vw"
			alt="Users giving positive feedback about your brand is by far the best brand promotion. MailChimp responds to positive customer feedback on Twitter."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Users giving positive feedback about your brand is by far the best brand promotion. MailChimp responds to positive customer feedback on Twitter.
		</figcaption>
	
</figure>


<h5 id="share-user-generated-content">Share User-Generated Content</h5>

<p>One of the best ways to push customer advocacy is through user-generated content.</p>

<p>It’s great for brands because one piece of user-generated content can reach thousands of people within hours. And it’s great for users: Being mentioned or having content shared by a brand is really exciting for many consumers.</p>

<p>Airbnb is an excellent example of how user-generated content can be a vital part of a brand’s content. In the  account, Airbnb shares stunning photos captured by its customers. The photos include exotic locations, and this kind of content is highly attractive to prospective customers.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ac19ae51-1caa-48c6-b754-544869f2cb91/image-10-user-advocates.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ac19ae51-1caa-48c6-b754-544869f2cb91/image-10-user-advocates.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ac19ae51-1caa-48c6-b754-544869f2cb91/image-10-user-advocates.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ac19ae51-1caa-48c6-b754-544869f2cb91/image-10-user-advocates.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ac19ae51-1caa-48c6-b754-544869f2cb91/image-10-user-advocates.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ac19ae51-1caa-48c6-b754-544869f2cb91/image-10-user-advocates.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ac19ae51-1caa-48c6-b754-544869f2cb91/image-10-user-advocates.png"
			sizes="100vw"
			alt="Sharing user content helps you get to that user’s audience. Airbnb uses such content to show off its users’ talents behind the camera."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Sharing user content helps you get to that user’s audience. Airbnb uses such content to show off its users’ talents behind the camera.
		</figcaption>
	
</figure>


<h5 id="solve-user-problems">Solve User Problems</h5>

<p>When users have a problem with a product, they often post questions or complaints on social networks in the hope of getting a quick response. It’s tremendously important to address every concern users have about your brand. By solving their problems, you clearly demonstrate that your brand is genuinely addressing customer concerns. Just imagine the effect when you resolve an issue on Twitter, Facebook or Instagram, and the happy user shares the whole conversation with their friends and family. The benefits will be priceless. Thus, the more you interact with people and solve their issues on social media, the more value you will provide to them, and the more they will like you.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/091fdc61-b2bc-432e-ac42-235271ce279b/image-11-user-advocates.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/091fdc61-b2bc-432e-ac42-235271ce279b/image-11-user-advocates.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/091fdc61-b2bc-432e-ac42-235271ce279b/image-11-user-advocates.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/091fdc61-b2bc-432e-ac42-235271ce279b/image-11-user-advocates.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/091fdc61-b2bc-432e-ac42-235271ce279b/image-11-user-advocates.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/091fdc61-b2bc-432e-ac42-235271ce279b/image-11-user-advocates.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/091fdc61-b2bc-432e-ac42-235271ce279b/image-11-user-advocates.png"
			sizes="100vw"
			alt="MailChimp deals with user problems on Twitter."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			MailChimp deals with user problems on Twitter.
		</figcaption>
	
</figure>


<h5 id="encourage-your-followers-to-share-content">Encourage Your Followers To Share Content</h5>

<p>Social media are great places to run promotional campaigns. Next time you run a promotion, ask your followers to share special moments using the hash tag assigned to the campaign. Track the hash tag, and choose the most inspiring contributions. This type of sharing has three significant benefits:</p>

<ul>
<li>It builds brand loyalty.</li>
<li>It brings a community together.</li>
<li>It helps you create great content relevant to your brand.</li>
</ul>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6558287f-0f2d-4309-a1ed-06de7624cc0e/image-12-user-advocates.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6558287f-0f2d-4309-a1ed-06de7624cc0e/image-12-user-advocates.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6558287f-0f2d-4309-a1ed-06de7624cc0e/image-12-user-advocates.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6558287f-0f2d-4309-a1ed-06de7624cc0e/image-12-user-advocates.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6558287f-0f2d-4309-a1ed-06de7624cc0e/image-12-user-advocates.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6558287f-0f2d-4309-a1ed-06de7624cc0e/image-12-user-advocates.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6558287f-0f2d-4309-a1ed-06de7624cc0e/image-12-user-advocates.png"
			sizes="100vw"
			alt="In Adobe XD’s promotional campaign on Twitter, designers share their work with Adobe XD using the hash tag #AdobeXDUIKit."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			In ’s promotional campaign on Twitter, designers share their work with Adobe XD using the hash tag #AdobeXDUIKit.
		</figcaption>
	
</figure>


<h5 id="provide-social-reward">Provide Social Reward</h5>

<p>Monitor your social media channels to identify people who are frequently mentioning your brand, and reward them with personal messages or gifts.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d5aa49ae-5779-49fc-b9d1-c5f5b4f2dfc9/image-13-user-advocates.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d5aa49ae-5779-49fc-b9d1-c5f5b4f2dfc9/image-13-user-advocates.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d5aa49ae-5779-49fc-b9d1-c5f5b4f2dfc9/image-13-user-advocates.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d5aa49ae-5779-49fc-b9d1-c5f5b4f2dfc9/image-13-user-advocates.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d5aa49ae-5779-49fc-b9d1-c5f5b4f2dfc9/image-13-user-advocates.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d5aa49ae-5779-49fc-b9d1-c5f5b4f2dfc9/image-13-user-advocates.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d5aa49ae-5779-49fc-b9d1-c5f5b4f2dfc9/image-13-user-advocates.png"
			sizes="100vw"
			alt="Reward users for connecting and interacting with your brand on social media. Starbucks sent a personalized, reusable Starbucks cup to one of its loyal customers to thank her for promoting Starbucks’ products in her Instagram posts."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Reward users for connecting and interacting with your brand on social media. Starbucks sent a personalized, reusable Starbucks cup to one of its loyal customers to thank her for promoting Starbucks’ products in her Instagram posts.
		</figcaption>
	
</figure>


<h5 id="make-social-engagement-a-natural-part-of-the-user-journey">Make Social Engagement A Natural Part Of The User Journey</h5>

<p>Encourage your users to share their achievements in the app on social media. Every once in a while, give users a shout out by sharing their posts on your page as well. Such encouragement can play a key role in making other people do the same. Just make sure the spotlight is on their accomplishments, not your product.</p>

<p>Runtastic (an app that tracks the number of kilometers a user runs every day) is a great example. The app encourages users to share their run with friends on social networks. Users love to share their progress with their network because it makes them look good.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bd72cf67-eee1-403e-9e39-723730e39c72/image-14-user-advocates.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bd72cf67-eee1-403e-9e39-723730e39c72/image-14-user-advocates.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bd72cf67-eee1-403e-9e39-723730e39c72/image-14-user-advocates.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bd72cf67-eee1-403e-9e39-723730e39c72/image-14-user-advocates.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bd72cf67-eee1-403e-9e39-723730e39c72/image-14-user-advocates.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bd72cf67-eee1-403e-9e39-723730e39c72/image-14-user-advocates.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bd72cf67-eee1-403e-9e39-723730e39c72/image-14-user-advocates.png"
			sizes="100vw"
			alt="Encourage your followers to share special moments. Runtastic encourages its users to share their accomplishments on social media."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Encourage your followers to share special moments. Runtastic encourages its users to share their accomplishments on social media.
		</figcaption>
	
</figure>


<h5 id="boost-employee-advocacy">Boost Employee Advocacy</h5>

<p>Your employees can help you amplify the brand’s message. According to .</p>

<p>Your employees know the product inside out; they are capable of providing support and answering detailed questions about the product. It’s possible to boost employee advocacy by following a few simple rules:</p>

<ul>
<li>Train your employees on social sharing activities. Organize seminars to educate your employees on the importance of social sharing and how they can participate in this activity.</li>
<li>Incentivize participation in social activities. Provide benefits to frequent sharers and referrers, and acknowledge them in company events.</li>
<li>Practice co-creating content with your employees. Give your employees more opportunities to be involved with your brand by sharing their own messages that reinforce business goals.</li>
<li>Help them build their personal brand. When your employees gain enough credibility to market your company, the impact of promotion will be much higher.</li>
</ul>

<h4 id="help-customers-reach-their-professional-goals">Help Customers Reach Their Professional Goals</h4>

<p>Every brand should help customers to become more experienced in what they do. One way to help your customers with their professional advancement is to provide educational opportunities. Today, many big companies are focused on creating content that will help their users. For example, Adobe offers a magnificent suite of products for designers, but it isn&rsquo;t only the products that make the company recognizable; it&rsquo;s the content it publishes. Adobe runs a that offers free in-depth educational content that helps thousands of designers create better products.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f88027a0-757c-4ce9-9a23-5e9d618255ec/image-15-user-advocates.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f88027a0-757c-4ce9-9a23-5e9d618255ec/image-15-user-advocates.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f88027a0-757c-4ce9-9a23-5e9d618255ec/image-15-user-advocates.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f88027a0-757c-4ce9-9a23-5e9d618255ec/image-15-user-advocates.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f88027a0-757c-4ce9-9a23-5e9d618255ec/image-15-user-advocates.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f88027a0-757c-4ce9-9a23-5e9d618255ec/image-15-user-advocates.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f88027a0-757c-4ce9-9a23-5e9d618255ec/image-15-user-advocates.png"
			sizes="100vw"
			alt="Hundreds of thousands of designers return to Adobe’s blog every month to learn more about design. Readers recognize and love the brand because the blog posts help them in what they do."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Hundreds of thousands of designers return to  every month to learn more about design. Readers recognize and love the brand because the blog posts help them in what they do.
		</figcaption>
	
</figure>


<h4 id="create-wow-moments-for-your-users">Create &ldquo;Wow&rdquo; Moments For Your Users</h4>

<p>One of the most effective ways to make your users happy (and turn them into brand advocates) is to surprise them — for example, with an unexpected gift. A gift doesn’t mean something expensive. It could be as simple as a handwritten note. Most users would be delighted to receive such a gift because they understand that it takes time to write a personal message. Give your customers such a surprise and they’ll want to talk about it and about, more importantly, its sender.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a9c22e4f-7a7d-4ebf-aec0-cceec2e0cbb7/image-16-user-advocates.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a9c22e4f-7a7d-4ebf-aec0-cceec2e0cbb7/image-16-user-advocates.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a9c22e4f-7a7d-4ebf-aec0-cceec2e0cbb7/image-16-user-advocates.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a9c22e4f-7a7d-4ebf-aec0-cceec2e0cbb7/image-16-user-advocates.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a9c22e4f-7a7d-4ebf-aec0-cceec2e0cbb7/image-16-user-advocates.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a9c22e4f-7a7d-4ebf-aec0-cceec2e0cbb7/image-16-user-advocates.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a9c22e4f-7a7d-4ebf-aec0-cceec2e0cbb7/image-16-user-advocates.jpg"
			sizes="100vw"
			alt="In today’s world of digital communication, a handwritten note stands out. Sending thank-you notes is a fantastic, and very personal, way to surprise your customers."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			In today’s world of digital communication, a handwritten note stands out. Sending thank-you notes is a fantastic, and very personal, way to surprise your customers. ()
		</figcaption>
	
</figure>


<h3 id="things-to-remember-when-creating-a-brand-advocacy-program">Things To Remember When Creating A Brand Advocacy Program</h3>

<p>We’ve just reviewed a great list of methods to boost brand advocacy. But which methods should be applied in your case? Unfortunately, when it comes to creating a brand advocacy program, there’s no silver bullet that turns customers into enthusiastic advocates. Each company has its own unique set of requirements, and it’s impossible to provide a one-size-fits-all solution. But it is still possible to provide a few general recommendations on how to create an advocacy program.</p>

<h4 id="set-a-goal">Set A Goal</h4>

<p>Without clear goals, your chances to engage advocates decrease significantly. Before you get started, know what you want to achieve from your advocate marketing program. What do you want advocates to do?</p>

<p>Choose advocacy goals that align with your overall business objectives. For example, if your top business goal is to increase conversions, then one of your top advocacy goals could be to get more high-quality referrals.</p>

<p>Here are a few common goals:</p>

<ul>
<li><strong>Higher brand engagement</strong><br />
The number of comments, likes and mentions on your channels is a signifier of success.</li>
<li><strong>Higher conversion rates</strong><br />
Get more high-quality referrals that result in increased sales.</li>
<li><strong>Better brand awareness</strong><br />
By tracking keywords associated with your brand, you’ll know how often people mention your brand and in what context.</li>
</ul>

<p><strong>Quick tip:</strong> <em>Use the S.M.A.R.T. goal-setting program to set the most effective goals possible. The goals you define should be specific, measurable, attainable, relevant and timely.</em></p>

<h4 id="measure-the-outcome">Measure The Outcome</h4>

<p>When it comes to measuring the outcome of an advocacy program, many teams use NPS (Net Promoter Score) as a key metric. NPS is computed by asking users to answer, &ldquo;How likely are you to recommend this product to a friend or relative? Rate it on a scale from 0 to 10.&rdquo; The answers are then grouped into three categories:</p>

<ul>
<li>Detractors: responses of 0 to 6, which indicate dissatisfaction.</li>
<li>Passives: responses of 7 or 8, which indicate moderate satisfaction.</li>
<li>Promoters: responses of 9 or 10, which indicate high satisfaction and a strong likelihood of recommendation.</li>
</ul>

<p>The NPS is then calculated by subtracting the percentage of detractors from the percentage of promoters. The NPS can range from -100% (only detractors) to +100% (only promoters).</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c6980d56-cf6d-4f74-9f8f-ae0093efe295/image-17-user-advocates.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c6980d56-cf6d-4f74-9f8f-ae0093efe295/image-17-user-advocates.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c6980d56-cf6d-4f74-9f8f-ae0093efe295/image-17-user-advocates.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c6980d56-cf6d-4f74-9f8f-ae0093efe295/image-17-user-advocates.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c6980d56-cf6d-4f74-9f8f-ae0093efe295/image-17-user-advocates.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c6980d56-cf6d-4f74-9f8f-ae0093efe295/image-17-user-advocates.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c6980d56-cf6d-4f74-9f8f-ae0093efe295/image-17-user-advocates.png"
			sizes="100vw"
			alt="The Net Promoter Score (NPS) is an index ranging from -100 to 100 that measures the willingness of customers to recommend a company’s products to others."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The Net Promoter Score (NPS) is an index ranging from -100 to 100 that measures the willingness of customers to recommend a company’s products to others.
		</figcaption>
	
</figure>


<p>While NPS is an excellent base level for measuring customer satisfaction and loyalty, don’t use NPS as a key performance indicator. Jared Spool provides a few valid arguments on why NPS can be considered  to business. Figure out the more reliable and actionable ways to measure how customers feel about your brand and its offerings.</p>

<p>Also, when it comes to evaluating your advocacy program, focus on measuring retention, not conversion. Customer retention refers to a business’ ability to keep a customer over a specified period of time. Your retention rate can tell you a lot about your user base.</p>

<p>Here are three metrics that can help you measure it:</p>

<ul>
<li><strong>Customer retention rate</strong><br />
The customer retention rate indicates what percentage of customers have stayed with you over a given period of time. While there’s no standard formula for calculating a customer retention rate, Jeff Haden shares a . Customer retention rate = ((CE – CN) / CS)) x 100, where CE is the number of customers at the end of a period, CN is the number of new customers acquired during a period of time, and CS is the number of customers at the start of a period of time. A business with a low customer retention rate is like a bucket of water with holes in it.</li>
<li><strong>Customer lifetime value</strong><br />
The customer lifetime value is a projection of revenue a business can expect from a customer relationship. Knowing the lifetime value of a customer will help you determine how much money you can spend on customer acquisition; it also enables you to calculate your return on investment (ROI). A customer’s acquisition costs being higher than their lifetime value will often cause problems.</li>
</ul>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/96c4b8a0-6593-46d9-80ba-dc887a31dc67/image-18-user-advocates.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/96c4b8a0-6593-46d9-80ba-dc887a31dc67/image-18-user-advocates.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/96c4b8a0-6593-46d9-80ba-dc887a31dc67/image-18-user-advocates.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/96c4b8a0-6593-46d9-80ba-dc887a31dc67/image-18-user-advocates.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/96c4b8a0-6593-46d9-80ba-dc887a31dc67/image-18-user-advocates.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/96c4b8a0-6593-46d9-80ba-dc887a31dc67/image-18-user-advocates.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/96c4b8a0-6593-46d9-80ba-dc887a31dc67/image-18-user-advocates.png"
			sizes="100vw"
			alt="Customer lifetime value"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Customer lifetime value ()
		</figcaption>
	
</figure>


<ul>
<li><strong>Referral rate</strong><br />
If a business runs a referral program, customer referrals are the ultimate proof of your advocacy program. Referral rate = number of coupons redeemed / number of coupons issued. If any user has a personal coupon they can share with friends and family, the formula can be even more straightforward: referral rate = number of coupons redeemed / total number of users.</li>
</ul>

<h3 id="conclusion">Conclusion</h3>

<p>Think of brand advocates as your new sales team. They have tremendous brand value, they drive awareness, and they are capable of persuading people to consider your product. By focusing your efforts on developing brand advocates, you will see an increase in your company’s growth.</p>

<p><em>This article is part of the UX design series sponsored by Adobe. Adobe XD tool is made for a  to stay updated and informed on the latest trends and insights for UX/UI design.</em></p>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(ms, al, il)</span>
</div>


</div>



              </article>
            </body>
          </html>
---------------
<h1 id="#title_2" >3、因为ai，Blued成为垂直社交产品里“不一样的烟火”</h1>
王英杰
[http://www.infoq.com/cn/news/2018/06/ai-blued?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/06/ai-blued?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>而男同社交应用Blued的成功，让这个群体有了某种程度上的归属感，并证明了这个市场巨大的潜力。很少有人知道，它的成功和人工智能的进步有着密不可分的关系。</p> <i>By 王英杰</i>
---------------
<h1 id="#title_3" >4、物联网技术周报第 140 期: 使用流引擎 Apache NiFi 和 MQTT 构建一个工业物联网系统</h1>
黄峰达
[http://www.infoq.com/cn/news/2018/06/iot-weekly-140?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/06/iot-weekly-140?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>使用 Amazon FreeRTOS 和 ESP32 连接设备到云端；使用流引擎 Apache NiFi 和 MQTT 构建一个工业物联网系统；如何使用 Arduino 制作一个绘图仪；亚马逊推 Echo Look 摄像头：教你如何穿衣搭配；Sonos 和宜家展示 Symfonisk 智能扬声器；从 10 万台到 1 万台：百度兵败智能音箱市场揭密；微软发布 Windows 10 IoT Core Services 付费提供 10 年长期支持</p> <i>By 黄峰达</i>
---------------
<h1 id="#title_4" >5、专访Martijn Verburg，关于AdoptOpenJDK与Nestmates</h1>
Kesha Williams
[http://www.infoq.com/cn/news/2018/06/adoptopenjdk-nestmates?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/06/adoptopenjdk-nestmates?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>InfoQ 近期对 Martijn Verburg 进行了一次专访，他是伦敦 Java 社区的领导人、AdoptOpenJDK 项目的联合创始人、同时也是 jClarity 的 CEO。谈论了 AdoptOpenJDK 构建平台的整体目标、他对于 Nestmates 和 Java 11的看法、AdoptOpenJDK 在2018年的发展计划，以及开发者如何参与这一项目的方式。</p> <i>By Kesha Williams</i> <i> Translated by 邵思华</i>
---------------
<h1 id="#title_5" >6、苹果发布Core ML 2</h1>
Roland Meertens
[http://www.infoq.com/cn/news/2018/06/apple-released-core-ml-2?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/06/apple-released-core-ml-2?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>在WWDC大会上，苹果发布了Core ML 2：iOS设备的新版机器学习SDK。新版本Core ML 2将带来30％的推理速度提升。Core ML SDK的一个重要新功能是Create ML。开发者可以在Mac上使用Swift创建和训练自定义机器学习模型。</p> <i>By Roland Meertens</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_6" >7、GitHub的未来，可期</h1>
Reddit
[http://www.infoq.com/cn/news/2018/06/github-future-expected?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/06/github-future-expected?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>6 月 7 日，微软公司副总裁，Xamarin 创始人，也就是 GitHub 新的 CEO Nat Friedman 在 Reddit 上开了帖子，第一时间回答了用户心中的一些疑问。以下内容根据 Reddit 上的分数排列选出，涵盖 Atom、GitHub 未来发展、业务模式、文化等方面的问题。</p> <i>By Reddit</i> <i> Translated by 无明</i>
---------------