## 文章索引
1、 <a href="#1前端每周清单第63期polymer-30ios爆出新漏洞2018前端工具调查结果" >前端每周清单第63期：Polymer 3.0，iOS爆出新漏洞，2018前端工具调查结果</a><br/>
2、 <a href="#2react-v1640:-pointer-events" >React v16.4.0: Pointer Events</a><br/>
3、 <a href="#3lessons-learned-while-developing-wordpress-plugins" >Lessons Learned While Developing WordPress Plugins</a><br/>
4、 <a href="#4文章-贝壳金控赵文乐基于-spring-cloud-的服务治理实践" >文章： 贝壳金控赵文乐：基于 Spring Cloud 的服务治理实践</a><br/>
5、 <a href="#5视频访谈-迟连义青云-open-pitrix多云平台的前世今生" >视频访谈： 迟连义：青云 Open  Pitrix多云平台的前世今生</a><br/>
6、 <a href="#6netflix正式开源其api网关zuul-2" >Netflix正式开源其API网关Zuul 2</a><br/>
7、 <a href="#7c#-73新特性一览" >C# 7.3新特性一览</a><br/>
8、 <a href="#8物联网技术周报第-137-期:-使用-amazon-freertos-和-esp32-将设备连接到云端" >物联网技术周报第 137 期: 使用 Amazon FreeRTOS 和 ESP32 将设备连接到云端</a><br/>
9、 <a href="#9文章-性能是net-core的一个关键特性" >文章： 性能是.NET Core的一个关键特性</a><br/><h1 id="#title_0" >1、前端每周清单第63期：Polymer 3.0，iOS爆出新漏洞，2018前端工具调查结果</h1>
覃云
[http://www.infoq.com/cn/news/2018/05/arch-weekly-63?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/05/arch-weekly-63?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>前端每周清单专注大前端领域内容，以对外文资料的搜集为主，帮助开发者了解一周前端热点；分为新闻热点、开发教程、工程实践、深度阅读、开源项目、巅峰人生等栏 目。欢迎关注【前端之巅】微信公众号（ID: frontshow），及时获取前端每周清单。</p> <i>By 覃云</i>
---------------
<h1 id="#title_1" >2、React v16.4.0: Pointer Events</h1>

[https://reactjs.org/blog/2018/05/23/react-v-16-4.html](https://reactjs.org/blog/2018/05/23/react-v-16-4.html)
<p>The latest minor release adds support for an oft-requested feature: pointer events!</p>
<p>It also includes a bugfix for <code>getDerivedStateFromProps</code>. Check out the full  below.</p>
<h2 id="pointer-events">Pointer Events</h2>
<p>The following event types are now available in React DOM:</p>
<ul>
<li><code>onPointerDown</code></li>
<li><code>onPointerMove</code></li>
<li><code>onPointerUp</code></li>
<li><code>onPointerCancel</code></li>
<li><code>onGotPointerCapture</code></li>
<li><code>onLostPointerCapture</code></li>
<li><code>onPointerEnter</code></li>
<li><code>onPointerLeave</code></li>
<li><code>onPointerOver</code></li>
<li><code>onPointerOut</code></li>
</ul>
<p>Please note that these events will only work in browsers that support the  specification. (At the time of this writing, this includes the latest versions of Chrome, Firefox, Edge, and Internet Explorer.) If your application depends on pointer events, we recommend using a third-party pointer events polyfill. We have opted not to include such a polyfill in React DOM, to avoid an increase in bundle size.</p>
<p></p>
<p>Huge thanks to  for contributing this change!</p>
<h2 id="bugfix-for-getderivedstatefromprops">Bugfix for <code>getDerivedStateFromProps</code></h2>
<p><code>getDerivedStateFromProps</code> is now called every time a component is rendered, regardless of the cause of the update. Previously, it was only called if the component was re-rendered by its parent, and would not fire as the result of a local <code>setState</code>. This was an oversight in the initial implementation that has now been corrected. The previous behavior was more similar to <code>componentWillReceiveProps</code>, but the improved behavior ensures compatibility with React’s upcoming asynchronous rendering mode.</p>
<p><strong>This bug fix will not affect most apps</strong>, but it may cause issues with a small fraction of components. The rare cases where it does matter fall into one of two categories:</p>
<h3 id="1-avoid-side-effects-in-getderivedstatefromprops">1. Avoid Side Effects in <code>getDerivedStateFromProps</code></h3>
<p>Like the render method, <code>getDerivedStateFromProps</code> should be a pure function of props and state. Side effects in <code>getDerivedStateFromProps</code> were never supported, but since it now fires more often than it used to, the recent change may expose previously undiscovered bugs.</p>
<p>Side effectful code should be moved to other methods: for example, Flux dispatches typically belong inside the originating event handler, and manual DOM mutations belong inside componentDidMount or componentDidUpdate. You can read more about this in our recent post about .</p>
<h3 id="2-compare-incoming-props-to-previous-props-when-computing-controlled-values">2. Compare Incoming Props to Previous Props When Computing Controlled Values</h3>
<p>The following code assumes <code>getDerivedStateFromProps</code> only fires on prop changes:</p>
<div class="gatsby-highlight">
      <pre class="gatsby-code-jsx"><code><span class="token keyword">static</span> <span class="token function">getDerivedStateFromProps</span><span class="token punctuation">(</span>props<span class="token punctuation">,</span> state<span class="token punctuation">)</span> <span class="token punctuation">{</span>
  <span class="token keyword">if</span> <span class="token punctuation">(</span>props<span class="token punctuation">.</span>value <span class="token operator">!==</span> state<span class="token punctuation">.</span>controlledValue<span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token keyword">return</span> <span class="token punctuation">{</span>
      <span class="token comment">// Since this method fires on both props and state changes, local updates</span>
      <span class="token comment">// to the controlled value will be ignored, because the props version</span>
      <span class="token comment">// always overrides it. Oops!</span>
      controlledValue<span class="token punctuation">:</span> props<span class="token punctuation">.</span>value<span class="token punctuation">,</span>
    <span class="token punctuation">}</span><span class="token punctuation">;</span>
  <span class="token punctuation">}</span>
  <span class="token keyword">return</span> <span class="token keyword">null</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span>
</code></pre>
      </div>
<p>One possible way to fix this is to compare the incoming value to the previous value by storing the previous props in state:</p>
<div class="gatsby-highlight">
      <pre class="gatsby-code-jsx"><code><span class="token keyword">static</span> <span class="token function">getDerivedStateFromProps</span><span class="token punctuation">(</span>props<span class="token punctuation">,</span> state<span class="token punctuation">)</span> <span class="token punctuation">{</span>
  <span class="token keyword">const</span> prevProps <span class="token operator">=</span> state<span class="token punctuation">.</span>prevProps<span class="token punctuation">;</span>
  <span class="token comment">// Compare the incoming prop to previous prop</span>
  <span class="token keyword">const</span> controlledValue <span class="token operator">=</span>
    prevProps<span class="token punctuation">.</span>value <span class="token operator">!==</span> props<span class="token punctuation">.</span>value
      <span class="token operator">?</span> props<span class="token punctuation">.</span>value
      <span class="token punctuation">:</span> state<span class="token punctuation">.</span>controlledValue<span class="token punctuation">;</span>
  <span class="token keyword">return</span> <span class="token punctuation">{</span>
    <span class="token comment">// Store the previous props in state</span>
    prevProps<span class="token punctuation">:</span> props<span class="token punctuation">,</span>
    controlledValue<span class="token punctuation">,</span>
  <span class="token punctuation">}</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span>
</code></pre>
      </div>
<p>However, try to avoid mixing props and state in this way — it’s rare that state needs to duplicate a value that exists in props and doing so can lead to subtle bugs. Prefer to have one source of truth for any value, and  if necessary to share it between multiple components. Most uses of <code>getDerivedStateFromProps</code> (and its predecessor <code>componentWillReceiveProps</code>) can be fixed by moving the state management to a parent component.</p>
<p>Please remember that <strong>most components do not need <code>getDerivedStateFromProps</code></strong>. It’s not meant to serve as a one-to-one replacement for <code>componentWillReceiveProps</code>. We’ll publish a follow-up post in the coming weeks with more recommendations on how to use (and not use) <code>getDerivedStateFromProps</code>.</p>
<h2 id="installation">Installation</h2>
<p>React v16.4.0 is available on the npm registry.</p>
<p>To install React 16 with Yarn, run:</p>
<div class="gatsby-highlight">
      <pre class="gatsby-code-bash"><code>yarn add react@^16.4.0 react-dom@^16.4.0
</code></pre>
      </div>
<p>To install React 16 with npm, run:</p>
<div class="gatsby-highlight">
      <pre class="gatsby-code-bash"><code><span class="token function">npm</span> <span class="token function">install</span> --save react@^16.4.0 react-dom@^16.4.0
</code></pre>
      </div>
<p>We also provide UMD builds of React via a CDN:</p>
<div class="gatsby-highlight">
      <pre class="gatsby-code-html"><code><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span> <span class="token attr-name">crossorigin</span> <span class="token attr-name">src</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>https://unpkg.com/react@16/umd/react.production.min.js<span class="token punctuation">"</span></span><span class="token punctuation">></span></span><span class="token script language-javascript"></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">></span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span> <span class="token attr-name">crossorigin</span> <span class="token attr-name">src</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>https://unpkg.com/react-dom@16/umd/react-dom.production.min.js<span class="token punctuation">"</span></span><span class="token punctuation">></span></span><span class="token script language-javascript"></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">></span></span>
</code></pre>
      </div>
<p>Refer to the documentation for .</p>
<h2 id="changelog">Changelog</h2>
<h3 id="react">React</h3>
<ul>
<li>Add a new )</li>
</ul>
<h3 id="react-dom">React DOM</h3>
<ul>
<li>Add support for the Pointer Events specification. ()</li>
<li>Properly call <code>getDerivedStateFromProps()</code> regardless of the reason for re-rendering. ()</li>
<li>Fix a bug that prevented context propagation in some cases. ()</li>
<li>Fix re-rendering of components using <code>forwardRef()</code> on a deeper <code>setState()</code>. ()</li>
<li>Fix some attributes incorrectly getting removed from custom element nodes. ()</li>
<li>Fix context providers to not bail out on children if there’s a legacy context provider above. ()</li>
<li>Add the ability to specify <code>propTypes</code> on a context provider component. ()</li>
<li>Fix a false positive warning when using <code>react-lifecycles-compat</code> in <code>&#x3C;StrictMode></code>. ()</li>
<li>Warn when the <code>forwardRef()</code> render function has <code>propTypes</code> or <code>defaultProps</code>. ()</li>
<li>Improve how <code>forwardRef()</code> and context consumers are displayed in the component stack. ()</li>
<li>Change internal event names. This can break third-party packages that rely on React internals in unsupported ways. ()</li>
</ul>
<h3 id="react-test-renderer">React Test Renderer</h3>
<ul>
<li>Fix the <code>getDerivedStateFromProps()</code> support to match the new React DOM behavior. ()</li>
<li>Fix a <code>testInstance.parent</code> crash when the parent is a fragment or another special node. ()</li>
<li><code>forwardRef()</code> components are now discoverable by the test renderer traversal methods. ()</li>
<li>Shallow renderer now ignores <code>setState()</code> updaters that return <code>null</code> or <code>undefined</code>. ()</li>
</ul>
<h3 id="react-art">React ART</h3>
<ul>
<li>Fix reading context provided from the tree managed by React DOM. ()</li>
</ul>
<h3 id="react-call-return-experimental">React Call Return (Experimental)</h3>
<ul>
<li>This experiment was deleted because it was affecting the bundle size and the API wasn’t good enough. It’s likely to come back in the future in some other form. ()</li>
</ul>
<h3 id="react-reconciler-experimental">React Reconciler (Experimental)</h3>
<ul>
<li>The )</li>
</ul>
---------------
<h1 id="#title_2" >3、Lessons Learned While Developing WordPress Plugins</h1>
Jakub Mikita
[https://www.smashingmagazine.com/2018/05/developing-wordpress-plugins/](https://www.smashingmagazine.com/2018/05/developing-wordpress-plugins/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/05/developing-wordpress-plugins/" />
              <title>Lessons Learned While Developing WordPress Plugins</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>Lessons Learned While Developing WordPress Plugins</h1>
                  
                    
                    <address>Jakub Mikita</address>
                  
                  <time datetime="2018-05-24T13:30:28&#43;02:00" class="op-published">2018-05-24T13:30:28+02:00</time>
                  <time datetime="2018-05-24T16:58:31&#43;00:00" class="op-modified">2018-05-24T16:58:31+00:00</time>
                </header>
                <p>Every WordPress plugin developer struggles with tough problems and code that’s difficult to maintain. We spend late nights supporting our users and tear out our hair when an upgrade breaks our plugin. Let me show you how to make it easier.</p>

<p>In this article, I’ll share my five years of experience developing WordPress plugins. The first plugin I wrote was a simple marketing plugin. It displayed a call to action (CTA) button with Google’s search phrase. Since then, I’ve written , and I maintain almost all of them. I’ve written around 40 plugins for my clients, from really small ones to one that have been maintained for over a year now.</p>

<div class="c-felix-the-cat">
<h4>Measuring Performance With Heatmaps</h4>
<p>Heatmaps can show you the exact spots that receive the most engagement on a given page. Find out why they’re so efficient for your marketing goals and how they can be integrated with your WordPress site. </p>
</div>

<p>Good development and support lead to more downloads. More downloads mean more money and a better reputation. This article will show you the lessons I’ve learned and the mistakes I’ve made, so that you can improve your plugin development.</p>



<aside class="product-panel product-panel__tilted product-panel--book" data-audience="non-subscriber">
    <div class="container product-panel--book__container">
      <div class="panel__description panel__description--book">
    <p>Getting workflow <em>just</em> right ain't an easy task. So are proper estimates. Or alignment among different departments. That's why we've set up <strong>'this-is-how-I-work'-sessions</strong> — with smart cookies sharing what works well for them. A part of the , of course.</p>
      <a href="https://www.smashingmagazine.com/membership/" class="btn btn--green btn--large">
        Explore features&nbsp;→
      </a>
      </div>
      <div class="panel__image panel__image--book">
        <a href="https://www.smashingmagazine.com/membership/" class="books__book__image">
        <div class="books__book__img">
          <img src="https://www.smashingmagazine.com/images/smashing-cat/smashing-tv-box-cat.svg" alt="Smashing TV, with live sessions for professional designers and developers." width="310" height="400">
        </div>
      </a>
      </div>
    </div>
  </aside>





<div class="c-garfield-the-cat">


<h3>1. Solve A Problem</h3>

<p>If your plugin doesn’t solve a problem, it won’t get downloaded. It’s as simple as that.</p>

<p>Take the  plugin (8,000+ active installations). It helps WordPress users who are having a hard time debugging their cron. The plugin was written out of a need &mdash; I needed something to help myself. I didn’t need to market this one, because people already needed it. It scratched their itch.</p>

<p>On the other hand, there’s the  plugin (70+ active installations). It randomly simulates a fly on the screen. It doesn’t really solve a problem, so it’s not going to have a huge audience. It was a fun plugin to develop, though.</p>

<p>Focus on a problem. When people don’t see their SEO performing well, they install an SEO plugin. When people want to speed up their website, they install a caching plugin. When people can’t find a solution to their problem, then they find a developer who writes a solution for them.</p>

<p>As David Hehenberger attests in his , need is a key factor in the WordPress user’s decision of whether to install a particular plugin.</p>

<p>If you have an opportunity to solve someone’s problem, take a chance.</p>

<h3>2. Support Your Product</h3>

<blockquote>“3 out of 5 Americans would try a new brand or company for a better service experience. 7 out of 10 said they were willing to spend more with companies they believe provide excellent service.”<br /><br />&mdash; Nykki Yeager</blockquote>

<p>Don’t neglect your support. Don’t treat it like a must, but more like an opportunity.</p>

<p>Good-quality support is critical in order for your plugin to grow. Even a plugin with the best code will get some support tickets. The more people who use your plugin, the more tickets you’ll get. A better user experience will get you fewer tickets, but you will never reach inbox 0.</p>

<p>Every time someone posts a message in a support forum, I get an email notification immediately, and I respond as soon as I can. It pays off. The vast majority of my good reviews were earned because of the support. This is a side effect: Good support often translates to 5-star reviews.</p>

<p>When you provide excellent support, people start to trust you and your product. And a plugin is a product, even if it’s completely free and open-source.</p>

<p>Good support is more complex than about writing a short answer once a day. When your plugin gains traction, you’ll get several tickets per day. It’s a lot easier to manage if you’re proactive and answer customers’ questions before they even ask.</p>

<p>Here’s a list of some actions you can take:</p>

<ul>

<li>Create an FAQ section in your repository.</li>

<li>Pin the “Before you ask” thread at the top of your support forum, highlighting the troubleshooting tips and FAQ.</li>

<li>Make sure your plugin is simple to use and that users know what they should do after they install it. UX is important.</li>

<li>Analyze the support questions and fix the pain points. Set up a board where people can vote for the features they want.</li>

<li>Create a video showing how the plugin works, and add it to your plugin’s main page in the WordPress.org repository.</li>

</ul>

<p>It doesn’t really matter what software you use to support your product. The WordPress.org’s official support forum works just as well as email or your own support system. I use WordPress.org’s forum for the free plugins and my own system for the premium plugins.</p>

<h3>3. Don’t Use Composer</h3>

<p>Composer is package-manager software. A repository of packages is hosted on packagist.org, and you can easily download them to your project. It’s like NPM or Bower for PHP. Managing your third-party packages the way Composer does is a good practice, but don’t use it in your WordPress project.</p>

<p>I know, I dropped a bomb. Let me explain.</p>

<p>Composer is great software. I use it myself, but not in public WordPress projects. The problem lies in conflicts. WordPress doesn’t have any global package manager, so each and every plugin has to load dependencies of their own. When two plugins load the same dependency, it causes a fatal error.</p>

<p>There isn’t really an ideal solution to this problem, but Composer makes it worse. You can bundle the dependency in your source manually and always check whether you are safe to load it.</p>

<p>Composer’s issue with WordPress plugins is still not solved, and there won’t be any viable solution to this problem in the near future. The problem was raised many years ago, and, as you can read in , many developers are trying to solve it, without any luck.</p>

<p>The best you can do is to make sure that the conditions and environment are good to run your code.</p>

<h3>4. Reasonably Support Old PHP Versions</h3>

<p>Don’t support very old versions of PHP, like 5.2. The security issues and maintenance aren’t worth it, and you’re not going to earn more installations from those older versions.</p>











<figure >
	
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b13115d5-6c5c-4c46-8b32-8458b9f6ad5f/lessons-learned-while-developing-wordpress-plugins.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b13115d5-6c5c-4c46-8b32-8458b9f6ad5f/lessons-learned-while-developing-wordpress-plugins.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b13115d5-6c5c-4c46-8b32-8458b9f6ad5f/lessons-learned-while-developing-wordpress-plugins.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b13115d5-6c5c-4c46-8b32-8458b9f6ad5f/lessons-learned-while-developing-wordpress-plugins.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b13115d5-6c5c-4c46-8b32-8458b9f6ad5f/lessons-learned-while-developing-wordpress-plugins.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b13115d5-6c5c-4c46-8b32-8458b9f6ad5f/lessons-learned-while-developing-wordpress-plugins.png"
			sizes="100vw"
			alt=""
		/>
	

	
		<figcaption class="op-vertical-bottom">
			The )
		</figcaption>
	
</figure>


<p>Go with PHP 5.6 as a minimal requirement, even though official support will be </p>

<p>There’s a movement that , which you can include in your plugin and which displays to your users important information about their PHP version and why they should upgrade.</p>

<p>Tell your users which versions you do support, and make sure their website doesn’t break after your plugin is installed on too low a version.</p>

<h3>5. Focus On Quality Code</h3>

<p>Writing good code is tough in the beginning. It takes time to learn the “SOLID” principles and design patterns and to change old coding habits.</p>

<p>It once took me three days to display a simple string in WordPress, when I decided to rewrite one of my plugins using better coding practices. It was frustrating knowing that it should have taken 30 minutes. Switching my mindset was painful but worth it.</p>


  <div id="sponsors-article" data-impression="true" class="c-promo-box c-promo-box--ad sponsors hidden" data-audience="non-subscriber" data-remove="true"></div>



<p>Why was it so hard? Because you start writing code that seems at first to be overkill and not very intuitive. I kept asking myself, “Is this really needed?” For example, you have to separate the logic into different classes and make sure each is responsible for a single thing. You also have to separate classes for the translation, custom post type registration, assets management, form handlers, etc. Then, you compose the bigger structures out of the simple small objects. That’s called . That’s very different from having “front end” and “admin” classes, where you cram all your code.</p>

<p>The other counterintuitive practice was to keep all actions and filters outside of the constructor method. This way, you’re not invoking any actions while creating the objects, which is very helpful for unit testing. You also have better control over which methods are executed and when. I wish I knew this before I wrote a project with an infinite loop caused by the actions in the constructor methods. Those kinds of bugs are hard to trace and hard to fix. The project had to be refactored.</p>

<p>The above are but a few examples, but you should get to know the . These are valid for any system and any coding language.</p>

<p>When you follow all of the best practices, you reach the point where every new feature just fits in. You don’t have to tweak anything or make any exceptions to the existing code. It’s amazing. Instead of getting more complex, your code just gets more advanced, without losing flexibility.</p>

<p>Also, format your code properly, and make sure every member of your team follows a standard. Standards will make your code predictable and easier to read and test. , which you can implement in your projects.</p>

<h3>6. Test Your Plugin Ahead Of Time</h3>

<p>I learned this lesson the hard way. Lack of testing led me to release a new version of a plugin with a fatal error. Twice. Both times, I got a 1-star rating, which I couldn’t turn into a positive review.</p>

<p>You can test manually or automatically. Travis CI is a continuous testing product that integrates with GitHub. I’ve built a  for my Notification plugin that just checks whether the plugin can boot properly on every PHP version. This way, I can be sure the plugin is error-free, and I don’t have to pay much attention to testing it in every environment.</p>

<p>Each automated test takes a fraction of a second. 100 automated tests will take about 10 minutes to complete, whereas manual testing needs about 2 minutes for each case.</p>

<p>The more time you invest in testing your plugin up front, the more it will save you in the long run.</p>

<p>To get started with automated testing, you can use the WP-CLI \\`wp scaffold plugin-test\\` command, which  you need.</p>

<h3>7. Document Your Work</h3>

<p>It’s a cliche that developers don’t like to write documentation. It’s the most boring part of the development process, but a little goes a long way.</p>

<p>Write self-documenting code. Pay attention to variable, function and class names. Don’t make any complicated structures, like cascades that can’t be read easily.</p>

<p>Another way to document code is to use the “doc block”, which is a comment for every file, function and class. If you write how the function works and what it does, it will be so much easier to understand when you need to debug it six months from now. WordPress Coding Standards covers this part by forcing you to write the doc blocks.</p>

<p>Using both techniques will save you the time of writing the documentation, but the code documentation is not going to be read by everyone.</p>

<p>For the end user, you have to write high-quality, short and easy-to-read articles explaining how the system works and how to use it. Videos are even better; many people prefer to watch a short tutorial than read an article. They are not going to look at the code, so make their lives easier. Good documentation also reduces support tickets.</p>

<h3>Conclusion</h3>

<p>These seven rules have helped me develop good-quality products, which are starting to be a core business at . I hope they’ll help you in your journey with WordPress plugins as well.</p>

<p>Let me know in the comments what your golden development rule is or whether you’ve found any of the above particularly helpful.</p>




<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(il, ra, yk)</span>
</div>


</div>




  <div id="sponsors-article-end" data-impression="true" class="c-promo-box c-promo-box--ad c-promo-box--wide sponsors hidden" data-audience="non-subscriber" data-remove="true"></div>



              </article>
            </body>
          </html>
---------------
<h1 id="#title_3" >4、文章： 贝壳金控赵文乐：基于 Spring Cloud 的服务治理实践</h1>
赵文乐
[http://www.infoq.com/cn/articles/spring-cloud-based-service-governance?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/spring-cloud-based-service-governance?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/spring-cloud-based-service-governance/zh/smallimage/cloud-logo-1508587932376-1526403146206.jpeg"/><p>4 月 23 日，TGO 鲲鹏会上海分会会员，贝壳金控高级架构总监赵文乐作为 TGO 鲲鹏会线上分享第六季的嘉宾，以直播的形式分享了服务治理的范围及原因、服务拆分和治理的原则，以及 Spring Cloud 的服务治理等内容。本文根据当天直播内容整理。</p> <i>By 赵文乐</i>
---------------
<h1 id="#title_4" >5、视频访谈： 迟连义：青云 Open  Pitrix多云平台的前世今生</h1>
迟连义
[http://www.infoq.com/cn/interviews/interview-with-chilianyi-talk-qing-cloud-open-pitrix?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/interviews/interview-with-chilianyi-talk-qing-cloud-open-pitrix?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/interviews/interview-with-chilianyi-talk-qing-cloud-open-pitrix/zh/mediumimage/chilianyi270-1527093102948.jpg"/><p>我们在QCon 全球软件开发大会，2018北京站的现场，很荣幸地采访到了来自青云QingCloud的应用平台顾问研发工程师，Open  Pitrix项目负责人迟连义先生，请他来谈谈青云开源项目Open  Pitrix的现状与发展。</p> <i>By 迟连义</i>
---------------
<h1 id="#title_5" >6、Netflix正式开源其API网关Zuul 2</h1>
Arthur Gonigberg 等
[http://www.infoq.com/cn/news/2018/05/netflix-zuul2?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/05/netflix-zuul2?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>本文将概述Zuul 2，详细介绍我们今天发布的一些有趣特性，并讨论我们正在使用Zuul 2构建的其他一些项目。</p> <i>By Arthur Gonigberg 等</i>
---------------
<h1 id="#title_6" >7、C# 7.3新特性一览</h1>
Jonathan Allen
[http://www.infoq.com/cn/news/2018/05/CSharp-7.3?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/05/CSharp-7.3?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>通过一个相对较小的版本，C# 7.3解决了一些自C# 1和2以来长期悬而未决的问题，如重载解析以及使用枚举和委托时的泛型约束。</p> <i>By Jonathan Allen</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_7" >8、物联网技术周报第 137 期: 使用 Amazon FreeRTOS 和 ESP32 将设备连接到云端</h1>
黄峰达
[http://www.infoq.com/cn/news/2018/05/iot-weekly-137?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/05/iot-weekly-137?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>使用 Amazon FreeRTOS 和 ESP32 将设备连接到云端；基于阿里云 HiTSDB 搭建工业物联网平台实践；将 Raspberry Pi 联机模拟器连接到 Azure IoT 中心；云知声推出首款物联网 AI 芯片， 将对部分客户开源；物联网风口下，Arduino 已不再是业余爱好者的“玩具”；英特尔发布 OpenVINO：让开发者在物联网上轻松布局 AI 模型；AWS IoT Analytics 服务正式发布</p> <i>By 黄峰达</i>
---------------
<h1 id="#title_8" >9、文章： 性能是.NET Core的一个关键特性</h1>
Maarten Balliauw
[http://www.infoq.com/cn/articles/performance-net-core?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/performance-net-core?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/performance-net-core/zh/headerimage/GettyImages-514210781-1525413367464.jpg"/><p>.NET Core核心带来了许多性能方面的优化，无论是在执行速度方面还是内存分配方面。示例是集合和LINQ扩展方法、文本处理、网络的优化，还有一些新的类型和概念，比如可以用Span做些有趣的事情。在本文中，我们将讨论如何使用这些新概念。</p> <i>By Maarten Balliauw</i> <i> Translated by 冬雨</i>
---------------