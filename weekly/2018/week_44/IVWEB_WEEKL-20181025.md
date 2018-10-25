## 文章索引
1、 <a href="#1react-v1660:-lazy-memo-and-contexttype" >React v16.6.0: lazy, memo and contextType</a><br/>
2、 <a href="#2video-playback-on-the-web:-the-current-state-of-video-part-1" >Video Playback On The Web: The Current State Of Video (Part 1)</a><br/>
3、 <a href="#3文章-银行业中的弹性系统" >文章： 银行业中的弹性系统</a><br/>
4、 <a href="#4文章-一文看懂智能合约的现状与未来" >文章： 一文看懂智能合约的现状与未来</a><br/>
5、 <a href="#5文章-olap引擎这么多麻袋财富为什么选择用kylin做自助分析" >文章： OLAP引擎这么多，麻袋财富为什么选择用Kylin做自助分析？</a><br/>
6、 <a href="#6微服务开源项目servicecomb-毕业成为apache顶级项目" >微服务开源项目ServiceComb 毕业成为Apache顶级项目</a><br/>
7、 <a href="#7postgresql中的大容量空间探索时间序列数据存储" >PostgreSQL中的大容量空间探索时间序列数据存储</a><br/>
8、 <a href="#8freewheel业务系统微服务化过程经验分享" >FreeWheel业务系统微服务化过程经验分享</a><br/>
9、 <a href="#9旷视联合idc发布ai+手机行业白皮书cv将成手机行业关键" >旷视联合IDC发布AI+手机行业白皮书：CV将成手机行业关键</a><br/>
10、 <a href="#10intel图形库mesa的持续集成" >Intel图形库Mesa的持续集成</a><br/><h1 id="#title_0" >1、React v16.6.0: lazy, memo and contextType</h1>

[https://reactjs.org/blog/2018/10/23/react-v-16-6.html](https://reactjs.org/blog/2018/10/23/react-v-16-6.html)
<p>Today we’re releasing React 16.6 with a few new convenient features. A form of PureComponent/shouldComponentUpdate for function components, a way to do code splitting using Suspense and an easier way to consume Context from class components.</p>
<p>Check out the full  below.</p>
<h2 id="reactmemo"></h2>
<p>Class components can bail out from rendering when their input props are the same using .</p>
<div class="gatsby-highlight" data-language="jsx"><pre class="gatsby-code-jsx"><code class="gatsby-code-jsx"><span class="token keyword">const</span> MyComponent <span class="token operator">=</span> React<span class="token punctuation">.</span><span class="token function">memo</span><span class="token punctuation">(</span><span class="token keyword">function</span> <span class="token function">MyComponent</span><span class="token punctuation">(</span>props<span class="token punctuation">)</span> <span class="token punctuation">{</span>
  <span class="token comment">/* only rerenders if props change */</span>
<span class="token punctuation">}</span><span class="token punctuation">)</span><span class="token punctuation">;</span></code></pre></div>
<h2 id="reactlazy-code-splitting-with-suspense">: Code-Splitting with <code class="gatsby-code-text">Suspense</code></h2>
<p>You may have seen  by wrapping a dynamic import in a call to <code class="gatsby-code-text">React.lazy()</code>.</p>
<div class="gatsby-highlight" data-language="jsx"><pre class="gatsby-code-jsx"><code class="gatsby-code-jsx"><span class="token keyword">import</span> React<span class="token punctuation">,</span> <span class="token punctuation">{</span>lazy<span class="token punctuation">,</span> Suspense<span class="token punctuation">}</span> <span class="token keyword">from</span> <span class="token string">'react'</span><span class="token punctuation">;</span>
<span class="token keyword">const</span> OtherComponent <span class="token operator">=</span> <span class="token function">lazy</span><span class="token punctuation">(</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">=></span> <span class="token keyword">import</span><span class="token punctuation">(</span><span class="token string">'./OtherComponent'</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

<span class="token keyword">function</span> <span class="token function">MyComponent</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
  <span class="token keyword">return</span> <span class="token punctuation">(</span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>Suspense</span> <span class="token attr-name">fallback</span><span class="token script language-javascript"><span class="token script-punctuation punctuation">=</span><span class="token punctuation">{</span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span><span class="token punctuation">></span></span><span class="token plain-text">Loading...</span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">></span></span><span class="token punctuation">}</span></span><span class="token punctuation">></span></span><span class="token plain-text">
      </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>OtherComponent</span> <span class="token punctuation">/></span></span><span class="token plain-text">
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>Suspense</span><span class="token punctuation">></span></span>
  <span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span></code></pre></div>
<p>The Suspense component will also allow library authors to start building data fetching with Suspense support in the future.</p>
<blockquote>
<p>Note: This feature is not yet available for server-side rendering. Suspense support will be added in a later release.</p>
</blockquote>
<h2 id="static-contexttype"></h2>
<p>In  API.</p>
<div class="gatsby-highlight" data-language="jsx"><pre class="gatsby-code-jsx"><code class="gatsby-code-jsx"><span class="token keyword">const</span> MyContext <span class="token operator">=</span> React<span class="token punctuation">.</span><span class="token function">createContext</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span></code></pre></div>
<p>We’ve heard feedback that adopting the new render prop API can be difficult in class components. So we’ve add a convenience API to .</p>
<div class="gatsby-highlight" data-language="jsx"><pre class="gatsby-code-jsx"><code class="gatsby-code-jsx"><span class="token keyword">class</span> <span class="token class-name">MyClass</span> <span class="token keyword">extends</span> <span class="token class-name">React<span class="token punctuation">.</span>Component</span> <span class="token punctuation">{</span>
  <span class="token keyword">static</span> contextType <span class="token operator">=</span> MyContext<span class="token punctuation">;</span>
  <span class="token function">componentDidMount</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token keyword">let</span> value <span class="token operator">=</span> <span class="token keyword">this</span><span class="token punctuation">.</span>context<span class="token punctuation">;</span>
    <span class="token comment">/* perform a side-effect at mount using the value of MyContext */</span>
  <span class="token punctuation">}</span>
  <span class="token function">componentDidUpdate</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token keyword">let</span> value <span class="token operator">=</span> <span class="token keyword">this</span><span class="token punctuation">.</span>context<span class="token punctuation">;</span>
    <span class="token comment">/* ... */</span>
  <span class="token punctuation">}</span>
  <span class="token function">componentWillUnmount</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token keyword">let</span> value <span class="token operator">=</span> <span class="token keyword">this</span><span class="token punctuation">.</span>context<span class="token punctuation">;</span>
    <span class="token comment">/* ... */</span>
  <span class="token punctuation">}</span>
  <span class="token function">render</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token keyword">let</span> value <span class="token operator">=</span> <span class="token keyword">this</span><span class="token punctuation">.</span>context<span class="token punctuation">;</span>
    <span class="token comment">/* render something based on the value of MyContext */</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span></code></pre></div>
<h2 id="static-getderivedstatefromerror"></h2>
<p>React 16 introduced  for handling errors thrown in React renders. We already had the <code class="gatsby-code-text">componentDidCatch</code> lifecycle method which gets fired after an error has already happened. It’s great for logging errors to the server. It also lets you show a different UI to the user by calling <code class="gatsby-code-text">setState</code>.</p>
<p>Before that is fired, we render <code class="gatsby-code-text">null</code> in place of the tree that threw an error. This sometimes breaks parent components that don’t expect their refs to be empty. It also doesn’t work to recover from errors on the server since the <code class="gatsby-code-text">Did</code> lifecycle methods don’t fire during server-side rendering.</p>
<p>We’re adding another error method that lets you render the fallback UI before the render completes. See the docs for .</p>
<blockquote>
<p>Note: <code class="gatsby-code-text">getDerivedStateFromError()</code> is not yet available for server-side rendering. It is designed to work with server-side rendering in a future release. We’re releasing it early so that you can start preparing to use it.</p>
</blockquote>
<h2 id="deprecations-in-strictmode">Deprecations in StrictMode</h2>
<p>In  component. It lets you opt-in to early warnings for patterns that might cause problems in the future.</p>
<p>We’ve added two more APIs to the list of deprecated APIs in <code class="gatsby-code-text">StrictMode</code>. If you don’t use <code class="gatsby-code-text">StrictMode</code> you don’t have to worry; these warning won’t fire for you.</p>
<ul>
<li><strong>ReactDOM.findDOMNode()</strong> - This API is often misunderstood and most uses of it are unnecessary. It can also be surprisingly slow in React 16.  for possible upgrade paths.</li>
<li><strong>Legacy Context</strong> using contextTypes and getChildContext - Legacy context makes React slightly slower and bigger than it needs to be. That’s why we strongly want to encourage upgrading to the  API makes this a bit easier.</li>
</ul>
<p>If you’re having trouble upgrading, we’d like to hear your feedback.</p>
<h2 id="installation">Installation</h2>
<p>React v16.6.0 is available on the npm registry.</p>
<p>To install React 16 with Yarn, run:</p>
<div class="gatsby-highlight" data-language="bash"><pre class="gatsby-code-bash"><code class="gatsby-code-bash">yarn add react@^16.6.0 react-dom@^16.6.0</code></pre></div>
<p>To install React 16 with npm, run:</p>
<div class="gatsby-highlight" data-language="bash"><pre class="gatsby-code-bash"><code class="gatsby-code-bash"><span class="token function">npm</span> <span class="token function">install</span> --save react@^16.6.0 react-dom@^16.6.0</code></pre></div>
<p>We also provide UMD builds of React via a CDN:</p>
<div class="gatsby-highlight" data-language="html"><pre class="gatsby-code-html"><code class="gatsby-code-html"><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span> <span class="token attr-name">crossorigin</span> <span class="token attr-name">src</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>https://unpkg.com/react@16/umd/react.production.min.js<span class="token punctuation">"</span></span><span class="token punctuation">></span></span><span class="token script language-javascript"></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">></span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span> <span class="token attr-name">crossorigin</span> <span class="token attr-name">src</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>https://unpkg.com/react-dom@16/umd/react-dom.production.min.js<span class="token punctuation">"</span></span><span class="token punctuation">></span></span><span class="token script language-javascript"></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">></span></span></code></pre></div>
<p>Refer to the documentation for .</p>
<h2 id="changelog">Changelog</h2>
<h3 id="react">React</h3>
<ul>
<li>Add <code class="gatsby-code-text">React.memo()</code> as an alternative to <code class="gatsby-code-text">PureComponent</code> for functions. ()</li>
<li>Add <code class="gatsby-code-text">React.lazy()</code> for code splitting components. ()</li>
<li><code class="gatsby-code-text">React.StrictMode</code> now warns about legacy context API. ()</li>
<li><code class="gatsby-code-text">React.StrictMode</code> now warns about <code class="gatsby-code-text">findDOMNode</code>. ()</li>
<li>Rename <code class="gatsby-code-text">unstable_AsyncMode</code> to <code class="gatsby-code-text">unstable_ConcurrentMode</code>. ()</li>
<li>Rename <code class="gatsby-code-text">unstable_Placeholder</code> to <code class="gatsby-code-text">Suspense</code>, and <code class="gatsby-code-text">delayMs</code> to <code class="gatsby-code-text">maxDuration</code>. ()</li>
</ul>
<h3 id="react-dom">React DOM</h3>
<ul>
<li>Add <code class="gatsby-code-text">contextType</code> as a more ergonomic way to subscribe to context from a class. ()</li>
<li>Add <code class="gatsby-code-text">getDerivedStateFromError</code> lifecycle method for catching errors in a future asynchronous server-side renderer. ()</li>
<li>Warn when <code class="gatsby-code-text">&lt;Context&gt;</code> is used instead of <code class="gatsby-code-text">&lt;Context.Consumer&gt;</code>. ()</li>
<li>Fix gray overlay on iOS Safari. ()</li>
<li>Fix a bug caused by overwriting <code class="gatsby-code-text">window.event</code> in development. ()</li>
</ul>
<h3 id="react-dom-server">React DOM Server</h3>
<ul>
<li>Add support for <code class="gatsby-code-text">React.memo()</code>. ()</li>
<li>Add support for <code class="gatsby-code-text">contextType</code>. ()</li>
</ul>
<h3 id="scheduler-experimental">Scheduler (Experimental)</h3>
<ul>
<li>Rename the package to <code class="gatsby-code-text">scheduler</code>. ()</li>
<li>Support priority levels, continuations, and wrapped callbacks. ()</li>
<li>Improve the fallback mechanism in non-DOM environments. ()</li>
<li>Schedule <code class="gatsby-code-text">requestAnimationFrame</code> earlier. ()</li>
<li>Fix the DOM detection to be more thorough. ()</li>
<li>Fix bugs with interaction tracing. ()</li>
<li>Add the <code class="gatsby-code-text">envify</code> transform to the package. ()</li>
</ul>
---------------
<h1 id="#title_1" >2、Video Playback On The Web: The Current State Of Video (Part 1)</h1>
Doug Sillars
[https://www.smashingmagazine.com/2018/10/video-playback-on-the-web-part-1/](https://www.smashingmagazine.com/2018/10/video-playback-on-the-web-part-1/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/10/video-playback-on-the-web-part-1/" />
              <title>Video Playback On The Web: The Current State Of Video (Part 1)</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>Video Playback On The Web: The Current State Of Video (Part 1)</h1>
                  
                    
                    <address>Doug Sillars</address>
                  
                  <time datetime="2018-10-24T13:30:24&#43;02:00" class="op-published">2018-10-24T13:30:24+02:00</time>
                  <time datetime="2018-10-24T22:53:50&#43;00:00" class="op-modified">2018-10-24T22:53:50+00:00</time>
                </header>
                

<p>Usage of video on the web is increasing as devices and networks become faster and more capable of handling video content. Research shows that sites with video increase engagement by 80%. E-Commerce sites with video have higher conversions than sites without video.</p>

<p>But adding video can come at a cost. Videos (being larger files) add to the page load time, and performance research shows that slower pages have the opposite effect of lower customer engagement and conversions. In this aticle, I’ll examine the important metrics to balance performance and video playback on the web, look at how video is being used today, and provide best practices on delivering video on the web.</p>

<p>One of the first steps to improve customer satisfaction is to <strong>speed up the load time of a page</strong>. Google has shown that mobile pages that take over three seconds to load lose 53% of their audience to abandonment. Other studies find that on improving site performance, usage and sales increase.</p>

<p>Adding video to a website will increase engagement, but it can also dramatically slow down the load time, so it is clear that a balance must be found between adding videos to your site and not impacting the load time too greatly.</p>

<p><strong>Recommended reading</strong>: <em></em></p>

<h3 id="video-on-the-web-today">Video On The Web Today</h3>

<p>To examine the state of video on the web today, I’ll use data from the HTTP Archive. The HTTP Archive uses WebPageTest to scan the performance of 1.2 million mobile and desktop websites every two weeks, and then stores the data in Google BigQuery.</p>

<p>Typically just the main page of each domain is checked (meaning <code>www.cnn.com</code> is run, but <code>www.cnn.com/politics</code> is not). This data can help us understand how the usage of video on the web affects the performance of websites. Mobile tests are run on an emulated Motorola G4 with a 3G internet connection (1.6 MBPS down, 768 KBPS up, 300 ms RTT), and desktop tests run Chrome on a cable connection (5 MBPS down, 1 MBPS up, 28ms RTT). I’ll be using the data set from 1 August 2018.</p>



<aside class="product-panel product-panel__tilted product-panel--book" data-audience="non-subscriber">
    <div class="container product-panel--book__container">
      <div class="panel__description panel__description--book">
    <p>Front-end is messy and complicated these days. That's why we publish  with a growing selection of <strong>front-end&nbsp;&amp;&nbsp;UX goodies</strong>. So you get your work done, better and faster.</p>

      <a href="https://smashed.by/perfpanelmembership" class="btn btn--green btn--large">
        Explore Smashing Membership&nbsp;↬
      </a>
      </div>
      <div class="panel__image panel__image--book">
        <a href="https://smashed.by/perfpanelmembership" class="books__book__image">
        <div class="books__book__img">
          <img src="https://www.smashingmagazine.com/images/smashing-cat/cat-rollerderby.svg" alt="Smashing Cat, just preparing to do some magic stuff." width="310" height="400">
        </div>
      </a>
      </div>
    </div>
  </aside>




<h4 id="sites-that-download-video">Sites That Download Video</h4>

<p>As a first step to study sites with video, we should look at sites that download video files when the page loads. There are 35k mobile sites and 55k desktop sites with video file downloads in the HTTP Archive data set (that’s 3% of all mobile sites and 4.5% of all desktop sites). Comparing desktop to mobile, we find that 30k of these sites have video on both mobile and desktop (leaving &#126;5,800 sites on mobile with no video on the desktop).</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bc7e76c6-16ae-494e-8c44-5e70eb0f2bce/video-playback-web-image-0.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bc7e76c6-16ae-494e-8c44-5e70eb0f2bce/video-playback-web-image-0.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bc7e76c6-16ae-494e-8c44-5e70eb0f2bce/video-playback-web-image-0.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bc7e76c6-16ae-494e-8c44-5e70eb0f2bce/video-playback-web-image-0.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bc7e76c6-16ae-494e-8c44-5e70eb0f2bce/video-playback-web-image-0.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bc7e76c6-16ae-494e-8c44-5e70eb0f2bce/video-playback-web-image-0.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bc7e76c6-16ae-494e-8c44-5e70eb0f2bce/video-playback-web-image-0.png"
			sizes="100vw"
			alt="Pi chart showing overlap of mobile and desktop video sites"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Mobile and Desktop Sites with Video ()
		</figcaption>
	
</figure>


<p>The median mobile page with video weighs in at a hefty 7 MB (583% larger than 1.2 MB found for the median mobile site). This increase is not fully accounted for by video alone (2.5 MB).  As sites with video tend to be more feature rich and visually engaging, they also use more images (the median site has over 1 MB more), CSS, and Javascript. The table below also shows that the median SpeedIndex (a measurement of how quickly content appears on the screen) for sites with video is 3.7s slower than a typical mobile site, taking a whopping 11.5 seconds to load.</p>

<table class="tablesaw break-out" data-tablesaw-mode="swipe" data-tablesaw-minimap>
    <thead>
        <tr>
            <th data-tablesaw-priority="persist"></th>
            <th>SpeedIndex</th>
            <th>Bytes Total</th>
            <th>Bytes Video</th>
            <th>Bytes CSS</th>
            <th>Bytes Images</th>
            <th>Bytes JS</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Video</td>
            <td>11544</td>
            <td>6,963,579</td>
            <td>2,526,098</td>
            <td>80,327</td>
            <td>1,596,062</td>
            <td>708,978</td>
        </tr>
        <tr>
            <td>all sites</td>
            <td>7780</td>
            <td>1,201,802</td>
            <td>0</td>
            <td>40,648</td>
            <td>449,585</td>
            <td>336,973</td>
        </tr>
    </tbody>
</table>

<p>This clearly shows that sites that are more interactive and have video content take (on average) longer to load that sites without video. But can we speed up video delivery?  What else can we learn from the data at hand?</p>

<h3 id="video-hosting">Video Hosting</h3>

<p>When examining video delivery, are the files being served from a CDN or video provider, or are developers hosting the videos on their own servers?  By examining the domain of the videos delivered on mobile, we find that 12,163 domains are used to deliver video, indicating that &#126;49% of sites are serving their own video files. If we stack rank the domains by frequency, we are able to determine the most common video hosting solutions:</p>

<table class="tablesaw break-out" data-tablesaw-mode="swipe" data-tablesaw-minimap>
    <thead>
        <tr>
            <th data-tablesaw-priority="persist">Video Doman</th>
            <th>cnt</th>
            <th>%</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>fbcdn.net</td>
            <td>116788</td>
            <td>67%</td>
        </tr>
        <tr>
            <td>akamaihd.net</td>
            <td>11170</td>
            <td>6%</td>
        </tr>
        <tr>
            <td>googlevideo.com</td>
            <td>10394</td>
            <td>6%</td>
        </tr>
        <tr>
            <td>cloudinary.com</td>
            <td>3170</td>
            <td>2%</td>
        </tr>
        <tr>
            <td>amazonaws.com</td>
            <td>1939</td>
            <td>1%</td>
        </tr>
        <tr>
            <td>cloudfront.net</td>
            <td>1896</td>
            <td>1%</td>
        </tr>
        <tr>
            <td>pixfs.net</td>
            <td>1853</td>
            <td>1%</td>
        </tr>
        <tr>
            <td>akamaized.net</td>
            <td>1573</td>
            <td>1%</td>
        </tr>
        <tr>
            <td>tedcdn.com</td>
            <td>1507</td>
            <td>1%</td>
        </tr>
        <tr>
            <td>contentabc.com</td>
            <td>1507</td>
            <td>1%</td>
        </tr>
        <tr>
            <td>vimeocdn.ccom</td>
            <td>1373</td>
            <td>1%</td>
        </tr>
        <tr>
            <td>dailymotion.com</td>
            <td>1337</td>
            <td>1%</td>
        </tr>
        <tr>
            <td>teads.tv</td>
            <td>1022</td>
            <td>1%</td>
        </tr>
        <tr>
            <td>youtube.com</td>
            <td>1007</td>
            <td>1%</td>
        </tr>
        <tr>
            <td>adstatic.com</td>
            <td>998</td>
            <td>1%</td>
        </tr>
    </tbody>
</table>

<p>Top CDNs and domains Facebook, Akamai, Google, Cloudinary, AWS, and Cloudfront lead the way, which is not surprising. However, it is interesting to see YouTube and Vimeo so far down in the list, as they are two of the most popular video sharing sites.</p>

<div class="sponsors__wide-place"></div>




<p>Let’s look into YouTube, Vimeo and Facebook video delivery:</p>

<h4 id="youtube-video-counts">YouTube Video Counts</h4>

<p>By default, pages with a YouTube video embedded do not actually download any video files &mdash; just scripts and a placeholder image, so they do not show up in a querly looking for sites with video downloads. One of the Javascript downloads for the YouTube Video player is <code>www-embed-player.js</code>. Searching for this file, we find 69k instances on 66,647 mobile sites. These sites have a median SpeedIndex of 10,700, and data usage of 3.31MB &mdash; better than sites with video downloaded, but still slower than sites with no video at all. The increase in data is directly associated with more images and Javascript (as shown below).</p>

<table class="tablesaw break-out" data-tablesaw-mode="swipe" data-tablesaw-minimap>
    <thead>
        <tr>
            <th data-tablesaw-priority="persist"></th>
            <th>Speedindex</th>
            <th>Bytes Total</th>
            <th>Bytes Video</th>
            <th>Bytes CSS</th>
            <th>Bytes Images</th>
            <th>Bytes JS</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Video</td>
            <td>11544</td>
            <td>6,963,579</td>
            <td>2,526,098</td>
            <td>80,327</td>
            <td>1,596,062</td>
            <td>708,978</td>
        </tr>
        <tr>
            <td>All sites</td>
            <td>7780</td>
            <td>1,201,802</td>
            <td>0</td>
            <td>40,648</td>
            <td>449,585</td>
            <td>336,973</td>
        </tr>
        <tr>
            <td>YouTube script</td>
            <td>10700</td>
            <td>3,310,000</td>
            <td>0</td>
            <td>126,314</td>
            <td>1,733,473</td>
            <td>1,005,758</td>
        </tr>
    </tbody>
</table>

<h4 id="vimeo-video-counts">Vimeo Video Counts</h4>

<p>There are 14,148  requests for Vimeo videos in HTTP Archive for Video playback. I see only 5,848 requests for the <em>player.js</em> file (in the format <code>https://f.vimeocdn.com/p/3.2.0/js/player.js</code> &mdash; implying that perhaps there are many videos on one page, or perhaps another location for the video player file. There are 17 different versions of the player present into HTTP Archive, with the most popular being 3.1.5 and 3.1.4:</p>

<table class="tablesaw break-out" data-tablesaw-mode="swipe" data-tablesaw-minimap>
    <thead>
        <tr>
            <th data-tablesaw-priority="persist">URL</th>
            <th>cnt</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><code>https://f.vimeocdn.com/p/3.1.5/js/player.js</code></td>
            <td>1832</td>
        </tr>
        <tr>
            <td><code>https://f.vimeocdn.com/p/3.1.4/js/player.js</code></td>
            <td>1057</td>
        </tr>
        <tr>
            <td><code>https://f.vimeocdn.com/p/3.1.17/js/player.js</code></td>
            <td>730</td>
        </tr>
        <tr>
            <td><code>https://f.vimeocdn.com/p/3.1.8/js/player.js</code></td>
            <td>507</td>
        </tr>
        <tr>
            <td><code>https://f.vimeocdn.com/p/3.1.10/js/player.js</code></td>
            <td>432</td>
        </tr>
        <tr>
            <td><code>https://f.vimeocdn.com/p/3.1.15/js/player.js</code></td>
            <td>352</td>
        </tr>
        <tr>
            <td><code>https://f.vimeocdn.com/p/3.1.19/js/player.js</code></td>
            <td>153</td>
        </tr>
        <tr>
            <td><code>https://f.vimeocdn.com/p/3.1.2/js/player.js</code></td>
            <td>117</td>
        </tr>
        <tr>
            <td><code>https://f.vimeocdn.com/p/3.1.13/js/player.js</code></td>
            <td>105</td>
        </tr>
    </tbody>
</table>

<p>There does not appear to be any performance gain for any Vimeo Library &mdash; all of the pages have similar load times.</p>

<p><strong>Note</strong>: <em>Using</em> <code>www-embed-player.js</code> <em>for YouTube or</em> <code>https://f.vimeocdn.com/p/*/js/player.js</code> <em>for Vimeo are good fingerprints for browsers with a clean cache, but if the customer has previously browsed a site with an embedded video, this file might already be in the browser cache, and thus will not be re-requested. But, as Andy Davies recently , this is not a safe assumption to make.</em></p>

<h4 id="facebook-video-counts">Facebook Video Counts</h4>

<p>It is surprising that in the HTTP Archive data, 67% of all video requests are from Facebook’s CDN. It turns out that on Chrome, 3rd party Facebook widgets  posted inside the widget (This effect does not occur in Safari or in Firefox.). It turns out that a 3rd party widget added with just a few lines of code is responsible for 57% of all the video seen in the HTTP Archive.</p>

<h3 id="video-file-types">Video File Types</h3>

<p>The majority of videos on pages tested are Mp4s. If we look at all the videos downloaded (excluding those from Facebook), we get the following view:</p>

<table class="tablesaw break-out" data-tablesaw-mode="swipe" data-tablesaw-minimap>
    <thead>
        <tr>
            <th data-tablesaw-priority="persist">File extension</th>
            <th>Video count</th>
            <th>%</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>.mp4</td>
            <td>48,448</td>
            <td>53%</td>
        </tr>
        <tr>
            <td>.ts</td>
            <td>18,026</td>
            <td>20%</td>
        </tr>
        <tr>
            <td>.webm</td>
            <td>3,946</td>
            <td>4%</td>
        </tr>
        <tr>
            <td></td>
            <td>14,926</td>
            <td>16%</td>
        </tr>
        <tr>
            <td>.m4s</td>
            <td>2,017</td>
            <td>2%</td>
        </tr>
        <tr>
            <td>.mpg</td>
            <td>1,431</td>
            <td>2%</td>
        </tr>
        <tr>
            <td>.mov</td>
            <td>441</td>
            <td>0%</td>
        </tr>
        <tr>
            <td>.m4v</td>
            <td>407</td>
            <td>0%</td>
        </tr>
        <tr>
            <td>.swf</td>
            <td>251</td>
            <td>0%</td>
        </tr>
    </tbody>
</table>

<p>Of the files with no extension &mdash; 10k are <code>googlevideo.com</code> files.</p>

<p>What can we learn about these files?  Let’s look each file type to learn more about the content being delivered.</p>

<p>I used FFPROBE to query the 34k unique MP4 files, and obtained data for 14,700 videos (many of the videos had changed or been removed in the 3 weeks from HTTP Archive capture to analysis).</p>

<h3 id="mp4-video-data">MP4 Video Data</h3>

<p>Of the 14.7k videos in the dataset, 8,564 have audio tracks (58%). Shorter videos that autoplay or videos that play in the background do not require audio, so stripping the audio track is a great way to reduce the file size (and speed the delivery) of your videos.</p>

<p>The next most important aspect to quickly downloading a video are the dimensions. The larger the dimensions (and in the case of video, there are three dimensions to consider: <code>width</code> &times; <code>height</code> &times; <code>time</code>), the larger the video file will be.</p>

<h4 id="mp4-video-duration">MP4 Video Duration</h4>

<p>Most of the 14k videos studied are short: the median (50th percentile) duration is 21s. However, 10% of the videos surveyed are over 2 minutes in duration. Use cases here will, of course, be divided, but for short video loops, or background videos &mdash; shorter videos will use less data, and download faster.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c33e264c-0275-45ae-a7a8-e0da51f4908a/video-playback-web-image-6.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c33e264c-0275-45ae-a7a8-e0da51f4908a/video-playback-web-image-6.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c33e264c-0275-45ae-a7a8-e0da51f4908a/video-playback-web-image-6.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c33e264c-0275-45ae-a7a8-e0da51f4908a/video-playback-web-image-6.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c33e264c-0275-45ae-a7a8-e0da51f4908a/video-playback-web-image-6.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c33e264c-0275-45ae-a7a8-e0da51f4908a/video-playback-web-image-6.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c33e264c-0275-45ae-a7a8-e0da51f4908a/video-playback-web-image-6.png"
			sizes="100vw"
			alt="Column Chart breaking down video length in 10 second segments"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Distribution of Video Duration ()
		</figcaption>
	
</figure>


<h4 id="mp4-video-width-and-height">MP4 Video Width And Height</h4>

<p>The dimensions of the video on the screen decide how many pixels each frame will have to use. The chart below shows the various video widths that are being served to the mobile device. (As a note, the Moto G4 has a screen size of 1080&times;1920, and the pages are all viewed in portrait mode).</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d5c3e491-aa9d-42c2-984e-28209ab17eb9/video-playback-web-image-7.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d5c3e491-aa9d-42c2-984e-28209ab17eb9/video-playback-web-image-7.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d5c3e491-aa9d-42c2-984e-28209ab17eb9/video-playback-web-image-7.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d5c3e491-aa9d-42c2-984e-28209ab17eb9/video-playback-web-image-7.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d5c3e491-aa9d-42c2-984e-28209ab17eb9/video-playback-web-image-7.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d5c3e491-aa9d-42c2-984e-28209ab17eb9/video-playback-web-image-7.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d5c3e491-aa9d-42c2-984e-28209ab17eb9/video-playback-web-image-7.png"
			sizes="100vw"
			alt="A column chart displaying the count of each video width observed in the data set"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Video Counts by Width ()
		</figcaption>
	
</figure>


<p>As the data shows, the two most utilized video widths are significantly larger than the G4 screen (when held in portrait mode). A full 49% of all videos are served with a width greater than 1080 pixels wide. The Alcatel 1x, a new Android Go device, has a 480&times;960-pixel screen. 77% of the videos delivered in the sample set are larger than 480 pixels wide.</p>

<p>As dimensions of videos decrease, so does the files size (and thus time to deliver the video). This is the primary reason to resize videos.</p>

<p>Why are these videos so large? If we correlate the videos served on mobile and desktop, we find that 18% of videos served on mobile are the same videos served on the desktop. This is a ‘problem’ solved for images years ago with responsive images. By serving differently sized videos to different sized devices, we can ensure that beautiful videos are served, but at a size and dimension that makes sense for the device.</p>

<div class="sponsors__wide-place"></div>




<h4 id="mp4-video-bitrate">MP4 Video Bitrate</h4>

<p>The bitrate of the video delivered to the device plays a large effect on how well the video will play back. The HTTP Archive tests are run on a 3G connection at 1.6 MBPS download speed. To playback (without stalling) the download has to be faster than playback. Let’s provide 80% of the available bitrate to video files (1.3 MBPS). 47% of the videos in the sample set have a bitrate over 1.3 MBPS, meaning that when these videos are played on a 3G connection, they are more likely to stall &mdash; leading to unhappy customers. 27% of videos have a bitrate higher than 2.5 MBPS, 10% are higher than 5 MBPS, and 35 of videos served to mobile devices have a bitrate &gt; 10 MBPS. These larger videos are unlikely to play without stalling on many connections &mdash; fixed or mobile.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5f724a0b-23d1-47bd-a786-7f4e0036b130/video-playback-web-image-8.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5f724a0b-23d1-47bd-a786-7f4e0036b130/video-playback-web-image-8.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5f724a0b-23d1-47bd-a786-7f4e0036b130/video-playback-web-image-8.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5f724a0b-23d1-47bd-a786-7f4e0036b130/video-playback-web-image-8.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5f724a0b-23d1-47bd-a786-7f4e0036b130/video-playback-web-image-8.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5f724a0b-23d1-47bd-a786-7f4e0036b130/video-playback-web-image-8.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5f724a0b-23d1-47bd-a786-7f4e0036b130/video-playback-web-image-8.png"
			sizes="100vw"
			alt="Column chart listing video bitrates in 500 KBPS buckets."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Observed Video Bitrates ()
		</figcaption>
	
</figure>


<h4 id="what-leads-to-higher-bitrates">What Leads To Higher Bitrates</h4>

<p>Larger videos tend to carry a larger bitrate, as larger dimensioned videos require a lot more data to populate the additional pixels on the device. Cross referencing the bitrate of each video to the width confirms this:  videos with width 1280 (orange) and 1920 (gray) have a much broader distribution of bitrates (more data points to the right in the chart). The column marked in yellow denotes the 136 videos with width 1920, and a bitrate between 10-11 MBPS.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fdbf8c36-ca16-43e3-924b-b0b7e86b404b/video-playback-web-image-9.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fdbf8c36-ca16-43e3-924b-b0b7e86b404b/video-playback-web-image-9.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fdbf8c36-ca16-43e3-924b-b0b7e86b404b/video-playback-web-image-9.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fdbf8c36-ca16-43e3-924b-b0b7e86b404b/video-playback-web-image-9.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fdbf8c36-ca16-43e3-924b-b0b7e86b404b/video-playback-web-image-9.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fdbf8c36-ca16-43e3-924b-b0b7e86b404b/video-playback-web-image-9.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fdbf8c36-ca16-43e3-924b-b0b7e86b404b/video-playback-web-image-9.png"
			sizes="100vw"
			alt="3D Column chart showing how bitrate and video size are related"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Bitrate Vs. Video Width ()
		</figcaption>
	
</figure>


<p>If we visualize only the videos over 1.6 MBPS, it becomes clear that the higher screen resolutions (1280 and 1920) are responsible for the higher bitrate videos.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/47a8dacf-73e1-422d-bfdc-d6d9fcff5bbb/video-playback-web-image-10.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/47a8dacf-73e1-422d-bfdc-d6d9fcff5bbb/video-playback-web-image-10.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/47a8dacf-73e1-422d-bfdc-d6d9fcff5bbb/video-playback-web-image-10.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/47a8dacf-73e1-422d-bfdc-d6d9fcff5bbb/video-playback-web-image-10.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/47a8dacf-73e1-422d-bfdc-d6d9fcff5bbb/video-playback-web-image-10.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/47a8dacf-73e1-422d-bfdc-d6d9fcff5bbb/video-playback-web-image-10.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/47a8dacf-73e1-422d-bfdc-d6d9fcff5bbb/video-playback-web-image-10.png"
			sizes="100vw"
			alt="3D chart showing that larger width videos generally have higher bitrate"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			High Bitrate and Video Width ()
		</figcaption>
	
</figure>


<h4 id="mp4-http-vs-https">MP4: HTTP vs. HTTPS</h4>

<p>HTTP2 has redefined content delivery with multiplexed connections &mdash; where just one connection per server is required. For large files like video, does HTTP2 provide a meaningful improvement to content delivery?  If we look at the stats from the HTTP Archive:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0c8c11b8-5fed-4323-89ff-2c08089827d0/11-video-playback-web.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0c8c11b8-5fed-4323-89ff-2c08089827d0/11-video-playback-web.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0c8c11b8-5fed-4323-89ff-2c08089827d0/11-video-playback-web.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0c8c11b8-5fed-4323-89ff-2c08089827d0/11-video-playback-web.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0c8c11b8-5fed-4323-89ff-2c08089827d0/11-video-playback-web.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0c8c11b8-5fed-4323-89ff-2c08089827d0/11-video-playback-web.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0c8c11b8-5fed-4323-89ff-2c08089827d0/11-video-playback-web.png"
			sizes="100vw"
			alt="Pie Chart of HTTP1 vs. HTTP2 for video delivery"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			HTTP1 vs HTTTP2 ()
		</figcaption>
	
</figure>


<p>Omitting the 116k Facebook videos (all sent via HTTP2), we see that it is about a 50:50 split between HTTP 1.1 and HTTP2. However, HTTP1.1 can utilize HTTPS, and when we filter for HTTPS usage, we find that 81% of video streams are sent via HTTPS, with HTTP2 being used slightly more than HTTPS1.1 (41%:36%)</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d2b2249d-5d9c-49fa-a833-889e7f42c3b7/12-video-playback-web.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d2b2249d-5d9c-49fa-a833-889e7f42c3b7/12-video-playback-web.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d2b2249d-5d9c-49fa-a833-889e7f42c3b7/12-video-playback-web.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d2b2249d-5d9c-49fa-a833-889e7f42c3b7/12-video-playback-web.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d2b2249d-5d9c-49fa-a833-889e7f42c3b7/12-video-playback-web.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d2b2249d-5d9c-49fa-a833-889e7f42c3b7/12-video-playback-web.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d2b2249d-5d9c-49fa-a833-889e7f42c3b7/12-video-playback-web.png"
			sizes="100vw"
			alt="Pie Chart further showing HTTP1 nonsecure and secure breakdown"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			HTTP vs. HTTP2 and secure ()
		</figcaption>
	
</figure>


<p>As you can see, comparing the speed of HTTP and HTTP2 video delivery is a work in progress.</p>

<h3 id="hls-video-streaming">HLS Video Streaming</h3>

<p>Video streaming using adaptive bitrate is an ideal way to deliver video to the end user. Multiple versions of each video are built with different dimensions and bitrates. The list of available streams is presented to the playback device, and the video player on the device can choose the most appropriate stream based on the size of the device screen and the available network conditions. There are 1,065 manifest files (and 14k video stream files) in the HTTP Archive data set that I examined.</p>

<h4 id="video-stream-playback">Video Stream Playback</h4>

<p>One key metric in video streaming is to have the video start as quickly as possible. While the manifest file has a list of available streams, the player has no idea the available bandwidth of the network at the beginning of playback. To begin streaming, and because the player has to pick a stream, it typically chooses the first one in the list. In order to facilitate a fast video startup, it is important to place the correct stream at the top of your manifest file.</p>

<p><strong>Note</strong>: <em>Utilizing the Chrome Network Info API to generate manifest files on the fly might be a good way to quickly optimize video content at startup.</em></p>

<p>One way to ensure that the video starts quickly is to start with the lowest quality video segment, as the download will be the fastest. The initial video quality may be pixelated, but as the player better understands the network quality, it can quickly adjust to a more appropriate (hopefully higher quality) video stream. With that in mind, let’s look at the initial stream bitrates in the HTTP Archive.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dcbd9944-9261-4a63-b87a-9f9cc7003223/video-playback-web-image-13.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dcbd9944-9261-4a63-b87a-9f9cc7003223/video-playback-web-image-13.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dcbd9944-9261-4a63-b87a-9f9cc7003223/video-playback-web-image-13.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dcbd9944-9261-4a63-b87a-9f9cc7003223/video-playback-web-image-13.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dcbd9944-9261-4a63-b87a-9f9cc7003223/video-playback-web-image-13.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dcbd9944-9261-4a63-b87a-9f9cc7003223/video-playback-web-image-13.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dcbd9944-9261-4a63-b87a-9f9cc7003223/video-playback-web-image-13.png"
			sizes="100vw"
			alt="Column chart showing initial bitrates in streaming videos. Many videos have too high an initial bitrate to stream on mobile."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Initial Bitrate for video streams ()
		</figcaption>
	
</figure>


<p>The red line in the above chart denotes 1.5 MBPS (recall that mobile tests are run at 1.6 MBPS, and not only video content is being downloaded). We see 30.5% of all of the streams (everything to the left of the line) start with an initial bitrate higher than 1.5 MBPS (and are thus unlikely to playback on a 3G connection)  17% start above 2 MBPS.</p>

<p>So what happens when video download is slower than the actual playback of the video? Initially, the player will attempt to download the (too) large bitrate files, but based on the download speed, will realise the problem. The player will then switch to downloading a lower bitrate video, so that download is faster than playback. The problem is that the initial download attempt takes time, and adding a delay to video playback start leads to customer abandonment.</p>

<p>We can also look at the most common bitrates of <code>.ts</code> files (the files that have the video content), to see what bitrates end up being downloaded on mobile. This data includes the initial bitrates, and any subsequent file downloaded during the WebPageTest run:</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dfbb01a0-6f17-4db2-818b-1e50991e5499/video-playback-web-image-14.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dfbb01a0-6f17-4db2-818b-1e50991e5499/video-playback-web-image-14.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dfbb01a0-6f17-4db2-818b-1e50991e5499/video-playback-web-image-14.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dfbb01a0-6f17-4db2-818b-1e50991e5499/video-playback-web-image-14.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dfbb01a0-6f17-4db2-818b-1e50991e5499/video-playback-web-image-14.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dfbb01a0-6f17-4db2-818b-1e50991e5499/video-playback-web-image-14.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dfbb01a0-6f17-4db2-818b-1e50991e5499/video-playback-web-image-14.png"
			sizes="100vw"
			alt="Column chart of observed bitrates once streaming begins"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Observed Mobile Bitrates ()
		</figcaption>
	
</figure>


<p>We can see two major groupings of video streaming bitrates (100-300 KBPS, and a broader peak from 300-1,000 MBPS). This is where we would expect streams to appear, given that the network speed is capped at 1.6 MBPS.</p>

<p>Comparing the data to the desktop, Mobile clearly is higher at the lower bitrates, and desktop streams have high peaks in the 500-600 and 800-900 KBPS ranges, that are not seen in mobile.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/faef7695-db2e-4073-acf2-1a083292f890/15-video-playback-web.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/faef7695-db2e-4073-acf2-1a083292f890/15-video-playback-web.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/faef7695-db2e-4073-acf2-1a083292f890/15-video-playback-web.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/faef7695-db2e-4073-acf2-1a083292f890/15-video-playback-web.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/faef7695-db2e-4073-acf2-1a083292f890/15-video-playback-web.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/faef7695-db2e-4073-acf2-1a083292f890/15-video-playback-web.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/faef7695-db2e-4073-acf2-1a083292f890/15-video-playback-web.png"
			sizes="100vw"
			alt="Column chart comparing observed bitrates on mobile and desktop"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Observed mobile and Desktop streaming bitrates ()
		</figcaption>
	
</figure>












<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/aaf045ea-5945-4016-b0c2-ca5de3e8ed4a/16-video-playback-web.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/aaf045ea-5945-4016-b0c2-ca5de3e8ed4a/16-video-playback-web.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/aaf045ea-5945-4016-b0c2-ca5de3e8ed4a/16-video-playback-web.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/aaf045ea-5945-4016-b0c2-ca5de3e8ed4a/16-video-playback-web.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/aaf045ea-5945-4016-b0c2-ca5de3e8ed4a/16-video-playback-web.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/aaf045ea-5945-4016-b0c2-ca5de3e8ed4a/16-video-playback-web.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/aaf045ea-5945-4016-b0c2-ca5de3e8ed4a/16-video-playback-web.png"
			sizes="100vw"
			alt="Column chart comparing initial bitrates with the observed bitrates for mobile and desktop."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Observed bitrates, mobile, desktop compared to initial bitrate ()
		</figcaption>
	
</figure>


<p>When we compare the initial bitrates observed (blue) with the actual files downloaded, it is very clear that for mobile the bitrate generally decreases during stream playback, indicating that lowering the initial bitrate for video streams might improve the performance of video startup and prevent stalls in early playback of the video. Desktop video also appears to decrease, but it is also possible that some video move to higher playback speeds.</p>

<h3 id="conclusion">Conclusion</h3>

<p>Video content on the web increases customer engagement and satisfaction. Pages that load quickly have the same effect. The addition of video to your website will slow down the page rendering time, necessitating a balance between overall page load and video content. To reduce the size of your video content, ensure that you have versions appropriately sized for mobile device dimensions, and use shorter videos when possible.</p>

<p>If playback of your videos is not essential, follow the path of YouTube and Vimeo &mdash; download all the required pieces to be ready for playback, but don’t actually download any video segments until the user presses play. Finally &mdash; if you are streaming video &mdash; start with the lowest quality setting to ensure a fast video playback.</p>

<p>In my next post on video, I will take these general findings, and dig deeper into how to resolve potential issues with examples. Stay tuned!</p>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(dm, ra, il)</span>
</div>


              </article>
            </body>
          </html>
---------------
<h1 id="#title_2" >3、文章： 银行业中的弹性系统</h1>
Greg Hawkins
[http://www.infoq.com/cn/articles/resilient-banking-systems?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/resilient-banking-systems?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/resilient-banking-systems/zh/smallimage/resilient-banking-systems-s-1538688547991-1539965445461.jpg"/><p>弹性是容忍失败，而不是消除它。要建立一个有弹性的系统，你必须建立一个能够吸收冲击并继续或恢复的系统。遵循弹性架构的最佳实践，包括已建立的云模式，“斯塔林银行（Starling Bank）”在一年之内从零开始创建了一家银行，这是在现有银行公共服务大量中断的背景下实现的。</p> <i>By Greg Hawkins</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_3" >4、文章： 一文看懂智能合约的现状与未来</h1>
Harry Papacharissiou
[http://www.infoq.com/cn/articles/smart-contracts-the-path-to-mainstream-adoption?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/smart-contracts-the-path-to-mainstream-adoption?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/smart-contracts-the-path-to-mainstream-adoption/zh/smallimage/agil-series-1508534878617-1540054952226.jpeg"/><p>智能合约的未来可期。</p> <i>By Harry Papacharissiou</i> <i> Translated by 刘志勇</i>
---------------
<h1 id="#title_4" >5、文章： OLAP引擎这么多，麻袋财富为什么选择用Kylin做自助分析？</h1>
麻袋财富大数据平台部门
[http://www.infoq.com/cn/articles/why-madailicai-choose-kylin?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/why-madailicai-choose-kylin?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/why-madailicai-choose-kylin/zh/smallimage/analyzing-and-preventing-unconscious-bias-in-machine-learning-s-1534197829508-1540056258763.jpeg"/><p>借贷信息中介平台麻袋财富现在已成为行业头部平台，庞大的业务量带来了数据量指数级增长，原有的数据分析处理方式已远远不能满足业务的需求。面对复杂的数据分析处理要求，麻袋财富选择了 Kylin。 为什么它会选择 Kylin 而不是其他解决方案呢？</p> <i>By 麻袋财富大数据平台部门</i>
---------------
<h1 id="#title_5" >6、微服务开源项目ServiceComb 毕业成为Apache顶级项目</h1>
Sally Khudairi
[http://www.infoq.com/cn/news/2018/10/servicecomb-Apache-TLP?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/10/servicecomb-Apache-TLP?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>全球最大的开源软件基金会Apache软件基金会（以下简称Apache）于北京时间10月24日宣布Apache ServiceComb 毕业成为Apache 顶级项目。</p> <i>By Sally Khudairi</i>
---------------
<h1 id="#title_6" >7、PostgreSQL中的大容量空间探索时间序列数据存储</h1>
Hrishikesh Barua
[http://www.infoq.com/cn/news/2018/10/space-time-series-data?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/10/space-time-series-data?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>欧洲航天局科学数据中心（the European Space Agency Science Data Center，简称ESDC）利用TimescaleDB扩展切换到用PostgreSQL来存储他们的数据。ESDC的各种数据，包括结构化的、非结构化的和时间序列指标在内接近数百TB，还有使用开源工具查询跨数据集的需求。</p> <i>By Hrishikesh Barua</i> <i> Translated by 姚佳灵</i>
---------------
<h1 id="#title_7" >8、FreeWheel业务系统微服务化过程经验分享</h1>
张晗, 杨谕黔, 罗昕
[http://www.infoq.com/cn/news/2018/10/FreeWheel-experience-share?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/10/FreeWheel-experience-share?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>2016 年下半年开始，FreeWheel 开始将其业务系统从 Rails 单体应用逐步迁移到微服务，同时技术栈从 Rails 改为 Golang，两年之后，整个迁移接近尾声，FreeWheel 业务系统技术团队对外分享了它们在微服务化过程中的经验。</p> <i>By 张晗, 杨谕黔, 罗昕</i>
---------------
<h1 id="#title_8" >9、旷视联合IDC发布AI+手机行业白皮书：CV将成手机行业关键</h1>
陈利鑫
[http://www.infoq.com/cn/news/2018/10/cv-key-factor-mobile-industry?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/10/cv-key-factor-mobile-industry?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>近日，IDC联合旷视科技发布行业首个“AI+手机”行业白皮书——《IDC手机行业白皮书:“视”界革命》，从应用层、算法层、解决方案层和硬件层详细展示了AI赋能手机的现状。 报告显示，目前手机端人工智能的应用主要集中在“视觉”上，如拍照、摄像、人像解锁等功能，而计算机视觉技术封装将成为手机产业链的关键环节，基于计算机视觉的算法、技术等在手机和其他领域的应用前景广阔。</p> <i>By 陈利鑫</i>
---------------
<h1 id="#title_9" >10、Intel图形库Mesa的持续集成</h1>
Hrishikesh Barua
[http://www.infoq.com/cn/news/2018/10/continuous-integration-mesa?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/10/continuous-integration-mesa?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Mesa CI是Intel的一个持续集成系统，用于运行Mesa图形库的构建和一致性测试套件。它运行在200多个系统中，每天运行数千万次测试。</p> <i>By Hrishikesh Barua</i> <i> Translated by 谢丽</i>
---------------