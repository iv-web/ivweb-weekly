## 文章索引
1、 <a href="#1react-v160" >React v16.0</a><br/>
2、 <a href="#2react-v1562" >React v15.6.2</a><br/>
3、 <a href="#3css-grid-gotchas-and-stumbling-blocks" >CSS Grid Gotchas And Stumbling Blocks</a><br/>
4、 <a href="#4视频演讲-ui-model更纯粹的前端" >视频演讲： ui-model，更纯粹的前端</a><br/>
5、 <a href="#5文章-微服务架构同程旅游让你少踩坑" >文章： 微服务架构，同程旅游让你少踩坑</a><br/>
6、 <a href="#6文章-且谈apache-spark的api三剑客rdddataframe和dataset" >文章： 且谈Apache Spark的API三剑客：RDD、DataFrame和Dataset</a><br/>
7、 <a href="#7文章-关于老程序员招聘和应聘的那点事" >文章： 关于老程序员招聘和应聘的那点事</a><br/>
8、 <a href="#8intellij-idea宣布对java-9的支持情况" >IntelliJ IDEA宣布对Java 9的支持情况</a><br/>
9、 <a href="#9阿里巴巴java开发手册背后的故事" >《阿里巴巴Java开发手册》背后的故事</a><br/><h1 id="#title_0" >1、React v16.0</h1>

[https://facebook.github.io/react/blog/2017/09/26/react-v16.0.html](https://facebook.github.io/react/blog/2017/09/26/react-v16.0.html)
<p>We&#39;re excited to announce the release of React v16.0! Among the changes are some long-standing feature requests, including .</p>

<h3>New render return types: fragments and strings</h3>

<p>You can now return an array of elements from a component&#39;s <code>render</code> method. Like with other arrays, you&#39;ll need to add a key to each element to avoid the key warning:</p>
<div class="highlight"><pre><code class="language-js" data-lang="js"><span class="nx">render</span><span class="p">()</span> <span class="p">{</span>
  <span class="c1">// No need to wrap list items in an extra element!</span>
  <span class="k">return</span> <span class="p">[</span>
    <span class="c1">// Don&#39;t forget the keys :)</span>
    <span class="o">&lt;</span><span class="nx">li</span> <span class="nx">key</span><span class="o">=</span><span class="s2">&quot;A&quot;</span><span class="o">&gt;</span><span class="nx">First</span> <span class="nx">item</span><span class="o">&lt;</span><span class="err">/li&gt;,</span>
    <span class="o">&lt;</span><span class="nx">li</span> <span class="nx">key</span><span class="o">=</span><span class="s2">&quot;B&quot;</span><span class="o">&gt;</span><span class="nx">Second</span> <span class="nx">item</span><span class="o">&lt;</span><span class="err">/li&gt;,</span>
    <span class="o">&lt;</span><span class="nx">li</span> <span class="nx">key</span><span class="o">=</span><span class="s2">&quot;C&quot;</span><span class="o">&gt;</span><span class="nx">Third</span> <span class="nx">item</span><span class="o">&lt;</span><span class="err">/li&gt;,</span>
  <span class="p">];</span>
<span class="p">}</span>
</code></pre></div>
<p>In the future, we&#39;ll likely add a special fragment syntax to JSX that doesn&#39;t require keys.</p>

<p>We&#39;ve added support for returning strings, too:</p>
<div class="highlight"><pre><code class="language-js" data-lang="js"><span class="nx">render</span><span class="p">()</span> <span class="p">{</span>
  <span class="k">return</span> <span class="s1">&#39;Look ma, no spans!&#39;</span><span class="p">;</span>
<span class="p">}</span>
</code></pre></div>
<p>.</p>

<h3>Better error handling</h3>

<p>Previously, runtime errors during rendering could put React in a broken state, producing cryptic error messages and requiring a page refresh to recover. To address this problem, React 16 uses a more resilient error-handling strategy. By default, if an error is thrown inside a component&#39;s render or lifecycle methods, the whole component tree is unmounted from the root. This prevents the display of corrupted data. However, it&#39;s probably not the ideal user experience.</p>

<p>Instead of unmounting the whole app every time there&#39;s an error, you can use error boundaries. Error boundaries are special components that capture errors inside their subtree and display a fallback UI in its place. Think of error boundaries like try-catch statements, but for React components.</p>

<p>For more details, check out our .</p>

<h3>Portals</h3>

<p>Portals provide a first-class way to render children into a DOM node that exists outside the DOM hierarchy of the parent component.</p>
<div class="highlight"><pre><code class="language-js" data-lang="js"><span class="nx">render</span><span class="p">()</span> <span class="p">{</span>
  <span class="c1">// React does *not* create a new div. It renders the children into `domNode`.</span>
  <span class="c1">// `domNode` is any valid DOM node, regardless of its location in the DOM.</span>
  <span class="k">return</span> <span class="nx">ReactDOM</span><span class="p">.</span><span class="nx">createPortal</span><span class="p">(</span>
    <span class="k">this</span><span class="p">.</span><span class="nx">props</span><span class="p">.</span><span class="nx">children</span><span class="p">,</span>
    <span class="nx">domNode</span><span class="p">,</span>
  <span class="p">);</span>
<span class="p">}</span>
</code></pre></div>
<p>See a full example in the .</p>

<h3>Better server-side rendering</h3>

<p>React 16 includes a completely rewritten server renderer. It&#39;s really fast. It supports <strong>streaming</strong>, so you can start sending bytes to the client faster. And thanks to a  that compiles away <code>process.env</code> checks (Believe it or not, reading <code>process.env</code> in Node is really slow!), you no longer need to bundle React to get good server-rendering performance.</p>

<p>Core team member Sasha Aickin wrote a . According to Sasha&#39;s synthetic benchmarks, server rendering in React 16 is roughly <strong>three times faster</strong> than React 15. &quot;When comparing against React 15 with <code>process.env</code> compiled out, there’s about a 2.4x improvement in Node 4, about a 3x performance improvement in Node 6, and a full 3.8x improvement in the new Node 8.4 release. And if you compare against React 15 without compilation, React 16 has a full order of magnitude gain in SSR in the latest version of Node!&quot; (As Sasha points out, please be aware that these numbers are based on synthetic benchmarks and may not reflect real-world performance.)</p>

<p>In addition, React 16 is better at hydrating server-rendered HTML once it reaches the client. It no longer requires the initial render to exactly match the result from the server. Instead, it will attempt to reuse as much of the existing DOM as possible. No more checksums! In general, we don&#39;t recommend that you render different content on the client versus the server, but it can be useful in some cases (e.g. timestamps).</p>

<p>See the  for more details.</p>

<h3>Support for custom DOM attributes</h3>

<p>Instead of ignoring unrecognized HTML and SVG attributes, React will now . This has the added benefit of allowing us to get rid of most of React&#39;s attribute whitelist, resulting in reduced file sizes.</p>

<h3>Reduced file size</h3>

<p>Despite all these additions, React 16 is actually <strong>smaller</strong> compared to 15.6.1!</p>

<ul>
<li><code>react</code> is 5.3 kb (2.2 kb gzipped), down from 20.7 kb (6.9 kb gzipped).</li>
<li><code>react-dom</code> is 103.7 kb (32.6 kb gzipped), down from 141 kb (42.9 kb gzipped).</li>
<li><code>react</code> + <code>react-dom</code> is 109 kb (34.8 kb gzipped), down from 161.7 kb (49.8 kb gzipped).</li>
</ul>

<p>That amounts to a combined <strong>32% size decrease compared to the previous version (30% post-gzip)</strong>.</p>

<p>The size difference is partly attributable to a change in packaging. React now uses  to create flat bundles for each of its different target formats, resulting in both size and runtime performance wins. The flat bundle format also means that React&#39;s impact on bundle size is roughly consistent regardless of how you ship your app, whether it&#39;s with Webpack, Browserify, the pre-built UMD bundles, or any other system.</p>

<h3>MIT licensed</h3>

<p>, React 16 is available under the MIT license. We&#39;ve also published React 15.6.2 under MIT, for those who are unable to upgrade immediately.</p>

<h3>New core architecture</h3>

<p>React 16 is the first version of React built on top of a new core architecture, codenamed &quot;Fiber.&quot; You can read all about this project over on . (Spoiler: we rewrote React!)</p>

<p>Fiber is responsible for most of the new features in React 16, like error boundaries and fragments. Over the next few releases, you can expect more new features as we begin to unlock the full potential of React.</p>

<p>Perhaps the most exciting area we&#39;re working on is <strong>async rendering</strong>—a strategy for cooperatively scheduling rendering work by periodically yielding execution to the browser. The upshot is that, with async rendering, apps are more responsive because React avoids blocking the main thread.</p>

<p>This demo provides an early peek at the types of problems async rendering can solve:</p>

<blockquote class="twitter-tweet" data-lang="en"><p lang="en" dir="ltr">Ever wonder what &quot;async rendering&quot; means? Here&#39;s a demo of how to coordinate an async React tree with non-React work </blockquote>

<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

<p><em>Tip: Pay attention to the spinning black square.</em></p>

<p>We think async rendering is a big deal, and represents the future of React. To make migration to v16.0 as smooth as possible, we&#39;re not enabling any async features yet, but we&#39;re excited to start rolling them out in the coming months. Stay tuned!</p>

<h2>Installation</h2>

<p>React v16.0.0 is available on the npm registry.</p>

<p>To install React 16 with Yarn, run:</p>
<div class="highlight"><pre><code class="language-bash" data-lang="bash">yarn add react@^16.0.0 react-dom@^16.0.0
</code></pre></div>
<p>To install React 16 with npm, run:</p>
<div class="highlight"><pre><code class="language-bash" data-lang="bash">npm install --save react@^16.0.0 react-dom@^16.0.0
</code></pre></div>
<p>We also provide UMD builds of React via a CDN:</p>
<div class="highlight"><pre><code class="language-html" data-lang="html"><span class="nt">&lt;script </span><span class="na">crossorigin</span> <span class="na">src=</span><span class="s">&quot;https://unpkg.com/react@16/umd/react.production.min.js&quot;</span><span class="nt">&gt;&lt;/script&gt;</span>
<span class="nt">&lt;script </span><span class="na">crossorigin</span> <span class="na">src=</span><span class="s">&quot;https://unpkg.com/react-dom@16/umd/react-dom.production.min.js&quot;</span><span class="nt">&gt;&lt;/script&gt;</span>
</code></pre></div>
<p>Refer to the documentation for .</p>

<h2>Upgrading</h2>

<p>Although React 16 includes significant internal changes, in terms of upgrading, you can think of this like any other major React release. We&#39;ve been serving React 16 to Facebook and Messenger.com users since earlier this year, and we released several beta and release candidate versions to flush out additional issues. With minor exceptions, <strong>if your app runs in 15.6 without any warnings, it should work in 16.</strong></p>

<h3>New deprecations</h3>

<p>Hydrating a server-rendered container now has an explicit API. If you&#39;re reviving server-rendered HTML, use  instead of <code>ReactDOM.render</code>. Keep using <code>ReactDOM.render</code> if you&#39;re just doing client-side rendering.</p>

<h3>React Addons</h3>

<p>As previously announced, we&#39;ve . We expect the latest version of each addon (except <code>react-addons-perf</code>; see below) to work for the foreseeable future, but we won&#39;t publish additional updates.</p>

<p>Refer to the previous announcement for .</p>

<p><code>react-addons-perf</code> no longer works at all in React 16. It&#39;s likely that we&#39;ll release a new version of this tool in the future. In the meantime, you can .</p>

<h3>Breaking changes</h3>

<p>React 16 includes a number of small breaking changes. These only affect uncommon use cases and we don&#39;t expect them to break most apps.</p>

<ul>
<li>React 15 had limited, undocumented support for error boundaries using <code>unstable_handleError</code>. This method has been renamed to <code>componentDidCatch</code>. You can use a codemod to .</li>
<li><code>ReactDOM.render</code> and <code>ReactDOM.unstable_renderIntoContainer</code> now return null if called from inside a lifecycle method. To work around this, you can use .</li>
<li><code>setState</code>:

<ul>
<li>Calling <code>setState</code> with null no longer triggers an update. This allows you to decide in an updater function if you want to re-render.</li>
<li>Calling <code>setState</code> directly in render always causes an update. This was not previously the case. Regardless, you should not be calling setState from render.</li>
<li><code>setState</code> callbacks (second argument) now fire immediately after <code>componentDidMount</code> / <code>componentDidUpdate</code> instead of after all components have rendered.</li>
</ul></li>
<li>When replacing <code>&lt;A /&gt;</code> with <code>&lt;B /&gt;</code>,  <code>B.componentWillMount</code> now always happens before  <code>A.componentWillUnmount</code>. Previously, <code>A.componentWillUnmount</code> could fire first in some cases.</li>
<li>Previously, changing the ref to a component would always detach the ref before that component&#39;s render is called. Now, we change the ref later, when applying the changes to the DOM.</li>
<li>It is not safe to re-render into a container that was modified by something other than React. This worked previously in some cases but was never supported. We now emit a warning in this case. Instead you should clean up your component trees using <code>ReactDOM.unmountComponentAtNode</code>. </li>
<li><code>componentDidUpdate</code> lifecycle no longer receives <code>prevContext</code> param. (See )</li>
<li>Shallow renderer no longer calls <code>componentDidUpdate</code> because DOM refs are not available. This also makes it consistent with <code>componentDidMount</code> (which does not get called in previous versions either).</li>
<li>Shallow renderer does not implement <code>unstable_batchedUpdates</code> anymore.</li>
</ul>

<h3>Packaging</h3>

<ul>
<li>There is no <code>react/lib/*</code> and <code>react-dom/lib/*</code> anymore. Even in CommonJS environments, React and ReactDOM are precompiled to single files (“flat bundles”). If you previously relied on undocumented React internals, and they don’t work anymore, let us know about your specific case in a new issue, and we’ll try to figure out a migration strategy for you.</li>
<li>There is no <code>react-with-addons.js</code> build anymore. All compatible addons are published separately on npm, and have single-file browser versions if you need them.</li>
<li>The deprecations introduced in 15.x have been removed from the core package. <code>React.createClass</code> is now available as <code>create-react-class</code>, <code>React.PropTypes</code> as <code>prop-types</code>, <code>React.DOM</code> as <code>react-dom-factories</code>, <code>react-addons-test-utils</code> as <code>react-dom/test-utils</code>, and shallow renderer as <code>react-test-renderer/shallow</code>. See  blog posts for instructions on migrating code and automated codemods.</li>
<li>The names and paths to the single-file browser builds have changed to emphasize the difference between development and production builds. For example:

<ul>
<li><code>react/dist/react.js</code> → <code>react/umd/react.development.js</code></li>
<li><code>react/dist/react.min.js</code> → <code>react/umd/react.production.min.js</code></li>
<li><code>react-dom/dist/react-dom.js</code> → <code>react-dom/umd/react-dom.development.js</code></li>
<li><code>react-dom/dist/react-dom.min</code>.js → <code>react-dom/umd/react-dom.production.min.js</code></li>
</ul></li>
</ul>

<h2>JavaScript Environment Requirements</h2>

<p>React 16 depends on the collection types .</p>

<p>A polyfilled environment for React 16 using core-js to support older browsers might look like:</p>
<div class="highlight"><pre><code class="language-js" data-lang="js"><span class="kr">import</span> <span class="s1">&#39;core-js/es6/map&#39;</span><span class="p">;</span>
<span class="kr">import</span> <span class="s1">&#39;core-js/es6/set&#39;</span><span class="p">;</span>

<span class="kr">import</span> <span class="nx">React</span> <span class="nx">from</span> <span class="s1">&#39;react&#39;</span><span class="p">;</span>
<span class="kr">import</span> <span class="nx">ReactDOM</span> <span class="nx">from</span> <span class="s1">&#39;react-dom&#39;</span><span class="p">;</span>

<span class="nx">ReactDOM</span><span class="p">.</span><span class="nx">render</span><span class="p">(</span>
  <span class="o">&lt;</span><span class="nx">h1</span><span class="o">&gt;</span><span class="nx">Hello</span><span class="p">,</span> <span class="nx">world</span><span class="o">!&lt;</span><span class="err">/h1&gt;,</span>
  <span class="nb">document</span><span class="p">.</span><span class="nx">getElementById</span><span class="p">(</span><span class="s1">&#39;root&#39;</span><span class="p">)</span>
<span class="p">);</span>
</code></pre></div>
<p>React also depends on <code>requestAnimationFrame</code> (even in test environments). A simple shim for test environments would be:</p>
<div class="highlight"><pre><code class="language-js" data-lang="js"><span class="nx">global</span><span class="p">.</span><span class="nx">requestAnimationFrame</span> <span class="o">=</span> <span class="kd">function</span><span class="p">(</span><span class="nx">callback</span><span class="p">)</span> <span class="p">{</span>
  <span class="nx">setTimeout</span><span class="p">(</span><span class="nx">callback</span><span class="p">,</span> <span class="mi">0</span><span class="p">);</span>
<span class="p">};</span>
</code></pre></div>
<h2>Acknowledgments</h2>

<p>As always, this release would not have been possible without our open source contributors. Thanks to everyone who filed bugs, opened PRs, responded to issues, wrote documentation, and more!</p>

<p>Special thanks to our core contributors, especially for their heroic efforts over the past few weeks during the prerelease cycle: .</p>
---------------
<h1 id="#title_1" >2、React v15.6.2</h1>

[https://facebook.github.io/react/blog/2017/09/25/react-v15.6.2.html](https://facebook.github.io/react/blog/2017/09/25/react-v15.6.2.html)
<p>Today we&#39;re sending out React 15.6.2. In 15.6.1, we shipped a few fixes for change events and inputs that had some unintended consequences. Those regressions have been ironed out, and we&#39;ve also included a few more fixes to improve the stability of React across all browsers.</p>

<p>Additionally, 15.6.2 adds support for the  attribute, and CSS columns are no longer appended with a <code>px</code> suffix.</p>

<h2>Installation</h2>

<p>We recommend using  is a good place to get started.</p>

<p>To install React with Yarn, run:</p>
<div class="highlight"><pre><code class="language-bash" data-lang="bash">yarn add react@^15.6.2 react-dom@^15.6.2
</code></pre></div>
<p>To install React with npm, run:</p>
<div class="highlight"><pre><code class="language-bash" data-lang="bash">npm install --save react@^15.6.2 react-dom@^15.6.2
</code></pre></div>
<p>We recommend using a bundler like  so you can write modular code and bundle it together into small packages to optimize load time.</p>

<p>Remember that by default, React runs extra checks and provides helpful warnings in development mode. When deploying your app, make sure to .</p>

<p>In case you don&#39;t use a bundler, we also provide pre-built bundles in the npm packages which you can  on your page:</p>

<ul>
<li><strong>React</strong><br/>
Dev build with warnings: <br/>
Minified build for production: <br/></li>
<li><strong>React with Add-Ons</strong><br/>
Dev build with warnings: <br/>
Minified build for production: <br/></li>
<li><strong>React DOM</strong> (include React in the page before React DOM)<br/>
Dev build with warnings: <br/>
Minified build for production: <br/></li>
<li><strong>React DOM Server</strong> (include React in the page before React DOM Server)<br/>
Dev build with warnings: <br/>
Minified build for production: <br/></li>
</ul>

<p>We&#39;ve also published version <code>15.6.2</code> of <code>react</code> and <code>react-dom</code> on npm, and the <code>react</code> package on bower.</p>

<hr>

<h2>Changelog</h2>

<h2>15.6.2 (September 25, 2017)</h2>

<h3>All Packages</h3>

<ul>
<li>Switch from BSD + Patents to MIT license</li>
</ul>

<h3>React DOM</h3>

<ul>
<li>Fix a bug where modifying <code>document.documentMode</code> would trigger IE detection in other browsers, breaking change events. ()</li>
<li>CSS Columns are treated as unitless numbers. ()</li>
<li>Fix bug in QtWebKit when wrapping synthetic events in proxies. ()</li>
<li>Prevent event handlers from receiving extra argument in development. ()</li>
<li>Fix cases where <code>onChange</code> would not fire with <code>defaultChecked</code> on radio inputs. ()</li>
<li>Add support for <code>controlList</code> attribute to DOM property whitelist ()</li>
<li>Fix a bug where creating an element with a ref in a constructor did not throw an error in development. ()</li>
</ul>
---------------
<h1 id="#title_2" >3、CSS Grid Gotchas And Stumbling Blocks</h1>
Rachel Andrew
[https://www.smashingmagazine.com/2017/09/css-grid-gotchas-stumbling-blocks/](https://www.smashingmagazine.com/2017/09/css-grid-gotchas-stumbling-blocks/)
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
</table><p>In March this year, CSS Grid shipped into production versions of Chrome, Firefox and Safari within weeks of each other. It has been great to see how excited people are about finally being able to use it to solve real problems.</p>

<figure></figure>

<p><strong>CSS Grid is such a different way of approaching layout</strong> that there are a number of common questions I am asked as people start to use the specification. This article aims to answer some of those, and will be one in a series of articles on Smashing Magazine about layouts.</p><p>The post .</p>
---------------
<h1 id="#title_3" >4、视频演讲： ui-model，更纯粹的前端</h1>
汪志成
[http://www.infoq.com/cn/presentations/ui-model-a-more-pure-front-end?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/ui-model-a-more-pure-front-end?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://cdn3.infoqstatic.com/statics_s1_20170927-0419/resource/presentations/ui-model-a-more-pure-front-end/zh/mediumimage/wangzhicheng270.jpg"/><p>当前，各种功能相似而又互不兼容的前端框架层出不穷，你是否为此感到困惑？你的应用系统是否常在维持现状和用新技术重写之间摇摆？你是否觉得自己做了越来越多低价值的重复劳动？这时候，你需要一种框架中立的技术方案。它能让你保护现有投资，在多种框架之间进退自如。是的，你需要 ui-model。ui-model 是一种设计思想，它的核心是把 SoC 发挥到极致，通过深入思考“什么是界面”，来剥离所有非核心的关注点，抽取出纯粹的交互逻辑。这让它得以中立于 JS 框架，也中立于 CSS 框架。我将带大家一步步走入 ui-model 的世界，你会发现，在 ui-model 的支持下，应用代码会得到大幅简化，可读性也显著提升。</p> <i>By 汪志成</i>
---------------
<h1 id="#title_4" >5、文章： 微服务架构，同程旅游让你少踩坑</h1>
谢康
[http://www.infoq.com/cn/articles/micro-service-architecture-of-tongcheng?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/micro-service-architecture-of-tongcheng?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://cdn3.infoqstatic.com/statics_s1_20170927-0419/resource/articles/micro-service-architecture-of-tongcheng/zh/smallimage/whole_logo.jpg"/><p>文章从开发者角度对微服务如何拆分、版本管理和单体到微服务过渡等方面给出了一些建议。</p> <i>By 谢康</i>
---------------
<h1 id="#title_5" >6、文章： 且谈Apache Spark的API三剑客：RDD、DataFrame和Dataset</h1>
Jules S. Damji
[http://www.infoq.com/cn/articles/three-apache-spark-apis-rdds-dataframes-and-datasets?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/three-apache-spark-apis-rdds-dataframes-and-datasets?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://cdn2.infoqstatic.com/statics_s1_20170927-0419/resource/articles/three-apache-spark-apis-rdds-dataframes-and-datasets/zh/smallimage/logo-mobile.jpg"/><p>本文将深入讲解Apache Spark 2.0的三种API——RDD、DataFrame和Dataset，在什么情况下该选用哪一种以及为什么，并概述它们的性能和优化点，列举那些应该使用DataFrame和Dataset而不是RDD的场景。</p> <i>By Jules S. Damji</i> <i> Translated by 足下</i>
---------------
<h1 id="#title_6" >7、文章： 关于老程序员招聘和应聘的那点事</h1>
Don Denoncourt
[http://www.infoq.com/cn/articles/tech-oldies-hiring?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/tech-oldies-hiring?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://cdn2.infoqstatic.com/statics_s1_20170927-0419/resource/articles/tech-oldies-hiring/zh/headerimage/article1-logo-big.jpg"/><p>Don给老程序员提了一些建议，比如如何写好求职信和简历，如何应对面试，如何回答刁钻的问题，如何为代码考察做好准备。招聘者将因此改变他们对应聘者的看法，他们将会从招聘聪明、热爱学习且追求卓越的老程序员中获益良多。</p> <i>By Don Denoncourt</i> <i> Translated by 薛命灯</i>
---------------
<h1 id="#title_7" >8、IntelliJ IDEA宣布对Java 9的支持情况</h1>
张卫滨
[http://www.infoq.com/cn/news/2017/09/IntelliJ-IDEA-Java-9?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/09/IntelliJ-IDEA-Java-9?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Java 9于本月21日正式发布，广受开发者欢迎的IDE产品IntelliJ IDEA随即在官方博客介绍了对Java 9的支持情况以及即将发布的IntelliJ IDEA 2017.3所包含的新特性。</p> <i>By 张卫滨</i>
---------------
<h1 id="#title_8" >9、《阿里巴巴Java开发手册》背后的故事</h1>
谢然
[http://www.infoq.com/cn/news/2017/09/short-being-good-programmer?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/09/short-being-good-programmer?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>互联网的世界，风云变幻，经历着雷厉风行的洗牌，在这个快速迭代升级的风口上，创新成了几乎所有互联网企业的核心理念。而规范是需要一定的匠心去打造的，迁就规范，似乎就碍了创新，在技术日新月异、业务风口变换的今天，如何才能权衡好创新和匠心呢？</p> <i>By 谢然</i>
---------------