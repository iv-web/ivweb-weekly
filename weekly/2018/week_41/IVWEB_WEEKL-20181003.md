## 文章索引
1、 <a href="#1文章-jshelljava-repl综合指南" >文章： JShell：Java REPL综合指南</a><br/>
2、 <a href="#2create-react-app-20:-babel-7-sass-and-more" >Create React App 2.0: Babel 7, Sass, and More</a><br/>
3、 <a href="#3how-to-build-a-website-with-the-wp-page-builder-plugin" >How To Build A Website With The WP Page Builder Plugin</a><br/>
4、 <a href="#4人工智能白热化运维脱帽背锅侠" >人工智能白热化，运维脱帽“背锅侠”</a><br/>
5、 <a href="#5nuxt-20正式发布支持-webpack-4es-module" >Nuxt 2.0正式发布：支持 Webpack 4、ES module</a><br/><h1 id="#title_0" >1、文章： JShell：Java REPL综合指南</h1>
Dustin Schultz
[http://www.infoq.com/cn/articles/jshell-java-repl?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/jshell-java-repl?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/jshell-java-repl/zh/smallimage/jshell-java-repl-s-1537393177692-1537639774724.jpeg"/><p>JShell提供了一个交互式shell，用于快速原型、调试、学习Java及Java API。本文将对JShell做一个全面的介绍，了解它所有的命令、用法以及它最有效的使用方法。</p> <i>By Dustin Schultz</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_1" >2、Create React App 2.0: Babel 7, Sass, and More</h1>

[https://reactjs.org/blog/2018/10/01/create-react-app-v2.html](https://reactjs.org/blog/2018/10/01/create-react-app-v2.html)
<p>Create React App 2.0 has been released today, and it brings a year’s worth of improvements in a single dependency update.</p>
<p>While React itself  has been to help you focus on what matters the most — your application code — and to handle build and testing setup for you.</p>
<p>Many of the tools it relies on have since released new versions containing new features and performance improvements:  have been busy with for the past few months: <strong>migrating the configuration and dependencies so that you don’t need to do it yourself.</strong></p>
<p>Now that Create React App 2.0 is out of beta, let’s see what’s new and how you can try it!</p>
<blockquote>
<p>Note</p>
<p>Don’t feel pressured to upgrade anything. If you’re satisfied with the current feature set, its performance, and reliability, you can keep using the version you’re currently at! It might also be a good idea to let the 2.0 release stabilize a little bit before switching to it in production.</p>
</blockquote>
<h2 id="whats-new">What’s New</h2>
<p>Here’s a short summary of what’s new in this release:</p>
<ul>
<li>🎉 More styling options: you can use  out of the box.</li>
<li>🐠 We updated to  and many bugfixes.</li>
<li>📦 We updated to , which automatically splits JS bundles more intelligently.</li>
<li>🃏 We updated to  for reviewing snapshots.</li>
<li>💎 You can use  transforms.</li>
<li>🌠 You can now , and use it in JSX.</li>
<li>🐈 You can try the experimental  that removes <code class="gatsby-code-text">node_modules</code>.</li>
<li>🕸 You can now  in development to match your backend API.</li>
<li>🚀 You can now use  without breaking the build.</li>
<li>💄 You can now optionally get a smaller CSS bundle if you only plan to target modern browsers.</li>
<li>👷‍♀️ Service workers are now opt-in and are built using Google’s .</li>
</ul>
<p><strong>All of these features work out of the box</strong> — to enable them, follow the below instructions.</p>
<h2 id="starting-a-project-with-create-react-app-20">Starting a Project with Create React App 2.0</h2>
<p>You don’t need to update anything special. Starting from today, when you run <code class="gatsby-code-text">create-react-app</code> it will use the 2.0 version of the template by default. Have fun!</p>
<p>If you want to <strong>use the old 1.x template</strong> for some reason, you can do that by passing <code class="gatsby-code-text">--scripts-version=react-scripts@1.x</code> as an argument to <code class="gatsby-code-text">create-react-app</code>.</p>
<h2 id="updating-a-project-to-create-react-app-20">Updating a Project to Create React App 2.0</h2>
<p>Upgrading a non-ejected project to Create React App 2.0 should usually be straightforward. Open <code class="gatsby-code-text">package.json</code> in the root of your project and find <code class="gatsby-code-text">react-scripts</code> there.</p>
<p>Then change its version to <code class="gatsby-code-text">2.0.3</code>:</p>
<div class="gatsby-highlight" data-language="jsx"><pre class="gatsby-code-jsx"><code class="gatsby-code-jsx">  <span class="token comment">// ... other dependencies ...</span>
<span class="gatsby-highlight-code-line">  <span class="token string">"react-scripts"</span><span class="token punctuation">:</span> <span class="token string">"2.0.3"</span>
</span></code></pre></div>
<p>Run <code class="gatsby-code-text">npm install</code> (or <code class="gatsby-code-text">yarn</code>, if you use it). <strong>For many projects, this one-line change is sufficient to upgrade!</strong></p>
<blockquote class="twitter-tweet" data-conversation="none" data-dnt="true"><p lang="en" dir="ltr">working here... thanks for all the new functionality 👍</p>&mdash; Stephen Haney (@sdothaney) </blockquote>
<p>Here’s a few more tips to get you started.</p>
<p><strong>When you run <code class="gatsby-code-text">npm start</code> for the first time after the upgrade,</strong> you’ll get a prompt asking about which browsers you’d like to support. Press <code class="gatsby-code-text">y</code> to accept the default ones. They’ll be written to your <code class="gatsby-code-text">package.json</code> and you can edit them any time. Create React App will use this information to produce smaller CSS bundles if you only target modern browsers.</p>
<p><strong>If <code class="gatsby-code-text">npm start</code> still doesn’t quite work for you after the upgrade,</strong>  is now opt-in</strong> to reduce the polyfill size.</p>
<p><strong>If you previously ejected but now want to upgrade,</strong> one common solution is to find the commits where you ejected (and any subsequent commits changing the configuration), revert them, upgrade, and later optionally eject again. It’s also possible that the feature you ejected for (maybe Sass or CSS Modules?) is now supported out of the box.</p>
<blockquote>
<p>Note</p>
<p>Due to a possible bug in npm, you might see warnings about unsatisfied peer dependencies. You should be able to ignore them. As far as we’re aware, this issue isn’t present with Yarn.</p>
</blockquote>
<h2 id="breaking-changes">Breaking Changes</h2>
<p>Here’s a short list of breaking changes in this release:</p>
<ul>
<li>Node 6 is no longer supported.</li>
<li>Support for older browsers (such as IE 9 to IE 11) is now opt-in with a .</li>
<li>Code-splitting with <code class="gatsby-code-text">import()</code> now behaves closer to specification, while <code class="gatsby-code-text">require.ensure()</code> is disabled.</li>
<li>The default Jest environment now includes jsdom.</li>
<li>Support for specifying an object as <code class="gatsby-code-text">proxy</code> setting was replaced with support for a custom proxy module.</li>
<li>Support for <code class="gatsby-code-text">.mjs</code> extension was removed until the ecosystem around it stabilizes.</li>
<li>PropTypes definitions are automatically stripped out of the production builds.</li>
</ul>
<p>If either of these points affects you,  contain more detailed instructions.</p>
<h2 id="learn-more">Learn More</h2>
<p>You can find the full changelog in the  and we’ll try to help.</p>
<blockquote>
<p>Note</p>
<p>If you’ve been using 2.x alpha versions, we provide  for them.</p>
</blockquote>
<h2 id="thanks">Thanks</h2>
<p>This release wouldn’t be possible without our wonderful community of contributors. We’d like to thank , and many others who provided feedback and testing for this release.</p>
---------------
<h1 id="#title_2" >3、How To Build A Website With The WP Page Builder Plugin</h1>
Jakub Mikita
[https://www.smashingmagazine.com/2018/10/wordpress-page-builder-plugin/](https://www.smashingmagazine.com/2018/10/wordpress-page-builder-plugin/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/10/wordpress-page-builder-plugin/" />
              <title>How To Build A Website With The WP Page Builder Plugin</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>How To Build A Website With The WP Page Builder Plugin</h1>
                  
                    
                    <address>Jakub Mikita</address>
                  
                  <time datetime="2018-10-02T13:30:17&#43;02:00" class="op-published">2018-10-02T13:30:17+02:00</time>
                  <time datetime="2018-10-02T18:54:33&#43;00:00" class="op-modified">2018-10-02T18:54:33+00:00</time>
                </header>
                

<p>(This is a sponsored post.) WordPress page builders are the first choice for creating a perfect website without any help from a developer. And a new one is on the market that we are going to test in this article. It’s . We’ll learn how to use this page builder plugin to create a website.</p>

<p>WP Page Builder is a free plugin that integrates with any WordPress theme. You can easily drag and drop elements onto the pages you are building, and you don’t need any coding skills to do so.</p>

<p>At least, that is the developer ’s point of view, which I’ll put to the test in this article. Does the plugin really help us build a website so easily? Are we able to achieve our goals for a website with it? We’re about to find out.</p>

<p>Let’s go through the process of building a real website using the WP Page Builder plugin. We’ll build a website of a few simple pages related to the fictional Rockhedge Park. We’ll learn about the plugin from installation to website launch.</p>

<p>Our goals are to:</p>

<ul>
<li>quickly create the website,</li>
<li>create a home page with the park’s features and highlights,</li>
<li>create a page to help visitors find the park,</li>
<li>create a contact page.</li>
</ul>

<p>Let’s start with a blank WordPress website, with the Twenty Seventeen theme installed.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/836296c3-7e68-4ddc-9418-c0958b7681ec/wppagebuilderplugin-image13.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/836296c3-7e68-4ddc-9418-c0958b7681ec/wppagebuilderplugin-image13.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/836296c3-7e68-4ddc-9418-c0958b7681ec/wppagebuilderplugin-image13.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/836296c3-7e68-4ddc-9418-c0958b7681ec/wppagebuilderplugin-image13.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/836296c3-7e68-4ddc-9418-c0958b7681ec/wppagebuilderplugin-image13.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/836296c3-7e68-4ddc-9418-c0958b7681ec/wppagebuilderplugin-image13.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/836296c3-7e68-4ddc-9418-c0958b7681ec/wppagebuilderplugin-image13.png"
			sizes="100vw"
			alt="a blank WordPress website, with the Twenty Seventeen theme installed"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<h3 id="installing-the-plugin">Installing The Plugin</h3>

<p>WP Page Builder is free, and you can download it from . It’s also easy to install via WordPress’ admin panel, but because the plugin is new, you’ll have to scroll down the list to find it.</p>

<p>Look for the one with the cool blue “P” icon with a square inside.</p>

<figure class="article__image break-out">)</figcaption></figure>

<p>After installation, you will not be bugged with any splash screen, and the only new thing in the admin area you might notice is a new item in the menu. This is the plugin’s general settings page, where you can control a few things such as which post types the plugin should support and who should be able to edit a page with the page builder.</p>

<figure></figure>

<p>I like that the plugin does not take over the whole admin panel. It’s discreet, and you are not even forced to use it to create pages or posts:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c53deb77-007d-4dc4-b4be-b4e12c5adf6d/wppagebuilderplugin-image2.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c53deb77-007d-4dc4-b4be-b4e12c5adf6d/wppagebuilderplugin-image2.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c53deb77-007d-4dc4-b4be-b4e12c5adf6d/wppagebuilderplugin-image2.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c53deb77-007d-4dc4-b4be-b4e12c5adf6d/wppagebuilderplugin-image2.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c53deb77-007d-4dc4-b4be-b4e12c5adf6d/wppagebuilderplugin-image2.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c53deb77-007d-4dc4-b4be-b4e12c5adf6d/wppagebuilderplugin-image2.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c53deb77-007d-4dc4-b4be-b4e12c5adf6d/wppagebuilderplugin-image2.png"
			sizes="100vw"
			alt="the plugin does not take over the whole admin panel"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<p>After clicking the button, you are taken to a new screen where the page builder really makes an appearance.</p>

<figure class="article__image break-out">)</figcaption></figure>

<p>The overall look and feel are very good. I particularly like the way the responsive options work; the whole website shrinks with a nice animation when you click the tablet or mobile icon.</p>

<p>All of the content and options you can tweak are on the left side, which is pretty convenient because the editing panels are not mixed up with the actual page content.</p>

<p>What I find not so great are the row and addon toolbar icons. They are just too small, and you cannot really distinguish them from each other without getting closer to the monitor. Also, I had to think a while about the menu items on the left, because the name “Addons” was a bit confusing to me. In this plugin, addons are the pieces of content you place on your website, not premium addons that you can install to make your website even cooler.</p>

<p>Another thing needed is support. There is none. It would be very nice to have some help text, even though the page builder seems to be very easy to use. For example, the &ldquo;Library&rdquo; tab doesn’t have any content, and I don’t really know what it is or what I can do with it.</p>

<p>Aside from these small things, I like this editor. Let’s proceed to set up our first page!</p>

<h3 id="creating-the-home-page">Creating The Home Page</h3>

<p>By default, you can put the content created with WP Page Builder in one spot, where standard content would appear. While this would be the expected behavior with most themes, it’s not in my case. I don’t want my content to be squished together in the default template:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ab1ab60d-7085-425c-98fc-cad0088076db/wppagebuilderplugin-image10.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ab1ab60d-7085-425c-98fc-cad0088076db/wppagebuilderplugin-image10.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ab1ab60d-7085-425c-98fc-cad0088076db/wppagebuilderplugin-image10.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ab1ab60d-7085-425c-98fc-cad0088076db/wppagebuilderplugin-image10.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ab1ab60d-7085-425c-98fc-cad0088076db/wppagebuilderplugin-image10.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ab1ab60d-7085-425c-98fc-cad0088076db/wppagebuilderplugin-image10.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ab1ab60d-7085-425c-98fc-cad0088076db/wppagebuilderplugin-image10.png"
			sizes="100vw"
			alt="By default, you can put the content created with WP Page Builder in one spot, where standard content would appear."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<p>This is probably why the plugin comes bundled with a page template called WP Page Builder Template. It spreads the content you build across the whole page, and only the header and footer of the theme are used.</p>

<p>The content looks way better now. I think this page builder could fit into any theme using this page template.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/481095fc-ee21-4ea7-9c8d-3e4a33cc5245/wppagebuilderplugin-image6.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/481095fc-ee21-4ea7-9c8d-3e4a33cc5245/wppagebuilderplugin-image6.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/481095fc-ee21-4ea7-9c8d-3e4a33cc5245/wppagebuilderplugin-image6.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/481095fc-ee21-4ea7-9c8d-3e4a33cc5245/wppagebuilderplugin-image6.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/481095fc-ee21-4ea7-9c8d-3e4a33cc5245/wppagebuilderplugin-image6.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/481095fc-ee21-4ea7-9c8d-3e4a33cc5245/wppagebuilderplugin-image6.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/481095fc-ee21-4ea7-9c8d-3e4a33cc5245/wppagebuilderplugin-image6.png"
			sizes="100vw"
			alt="WP Page Builder spreads the content you build across the whole page, and only the header and footer of the theme are used."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<p>OK, the theme is installed, the page builder is installed, and the page is prepared. What do we do next? I’m sure you’ve been in this position when using page builders before; you just don’t know what to do with the page. You don’t even know what you <em>can</em> do with the page. It’s the standard &ldquo;blank canvas&rdquo; problem.</p>

<p>However, I discovered something called &ldquo;Layouts&rdquo; in the plugin’s sidebar. And the way it works impressed me.</p>

<h4 id="page-layouts">Page Layouts</h4>

<p>Page layouts are complete pages, ready to be imported in your WordPress website. Sounds cool, doesn’t it? Watch this:</p>

<figure class="article__image break-out">)</figcaption></figure>

<p>As you can see, there are many templates, and most of them are paid. A few are free, though, and you can use them to get some inspiration.</p>

<p>The best part with this importing is that it doesn’t bloat WordPress. You can wipe out the page content with two clicks, and nothing is left. Even the images are not loaded to WordPress’ library.</p>

<p>You can test many concepts and options, and adjust everything to your needs without ending up with a ton of unused things imported into your WordPress installation. I really like that.</p>

<h4 id="composing-the-home-page">Composing The Home Page</h4>

<p>My initial idea for the home page was a few images of the park and some features highlighted.</p>

<p>After getting inspired by the , I started with a header image, and I created my other pages, as well as the main navigation.</p>

<p>I decided not to use any layouts because the blocks and addons are very simple to use, and they come with default content.</p>

<p>I started with a big image section just beneath the header, with a fixed background and a generic title.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b8b68b80-15b6-48d9-9af7-995eaafaf835/wppagebuilderplugin-image7.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b8b68b80-15b6-48d9-9af7-995eaafaf835/wppagebuilderplugin-image7.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b8b68b80-15b6-48d9-9af7-995eaafaf835/wppagebuilderplugin-image7.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b8b68b80-15b6-48d9-9af7-995eaafaf835/wppagebuilderplugin-image7.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b8b68b80-15b6-48d9-9af7-995eaafaf835/wppagebuilderplugin-image7.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b8b68b80-15b6-48d9-9af7-995eaafaf835/wppagebuilderplugin-image7.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b8b68b80-15b6-48d9-9af7-995eaafaf835/wppagebuilderplugin-image7.png"
			sizes="100vw"
			alt="The template has a big image section just beneath the header, with a fixed background and a generic title"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<p>Configuring this section was very easy, but I had some trouble with the custom font for the headings. I figured out that I have to remove my previous selection, and then I’m able to pick a new font family.</p>

<p>One thing I like is the way you can adjust the addon’s padding live on the screen:</p>

<figure class="article__image break-out">)</figcaption></figure>

<p>For the next section, I decided to use a predefined content block, which looks perfect for me. Adding it to the page is also very simple: Just drop it in the desired spot, and adjust the sample content.</p>

<figure class="article__image break-out">)</figcaption></figure>

<p>Filling in the content was a breeze, and I quickly reached the last section, the call to action. There, I used the call-to-action block with very simple content.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3a9f378c-fcc9-4fb7-8a17-6bfb3893deac/wppagebuilderplugin-image9.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3a9f378c-fcc9-4fb7-8a17-6bfb3893deac/wppagebuilderplugin-image9.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3a9f378c-fcc9-4fb7-8a17-6bfb3893deac/wppagebuilderplugin-image9.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3a9f378c-fcc9-4fb7-8a17-6bfb3893deac/wppagebuilderplugin-image9.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3a9f378c-fcc9-4fb7-8a17-6bfb3893deac/wppagebuilderplugin-image9.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3a9f378c-fcc9-4fb7-8a17-6bfb3893deac/wppagebuilderplugin-image9.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3a9f378c-fcc9-4fb7-8a17-6bfb3893deac/wppagebuilderplugin-image9.png"
			sizes="100vw"
			alt="A call-to-action block with very simple content"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<p>Et voilà! The process of creating the page was very simple, and I enjoyed it.</p>

<h3 id="creating-the-find-us-page">Creating The &ldquo;Find Us&rdquo; Page</h3>

<p>The next page is the one where people can easily find our park. This involved the use of more advanced sections, like a map.</p>

<p>Unfortunately, the map addon isn’t available in the free version of the plugin, so I decided to write that one myself and see how the plugin’s code base looks.</p>

<p>The code is not bad at all. It’s clear and easy to read, despite the fact that there are almost no inline comments. I haven’t found any documentation whatsoever, so I had to dig in to see how I could extend the plugin. And it didn’t look like I needed much — just an addon class and filter.</p>

<h4 id="custom-google-map-addon">Custom Google Map Addon</h4>

<p>When you don’t have any documentation, the best approach is to copy and adjust existing code.</p>

<p>A lot of configuration options seem to be available, some of which really need strong documentation. But for our case, we’ll make a simple Google Map iframe using a Google API key, with a place to query and the iframe’s height.</p>

<p>This is what our class looks like:</p>

<pre class="break-out"><code class="language-javascript">class JakubMikita_Addon_GoogleMap{

    public function get_name(){
        return 'jakubmikita_googlemap_block';
    }
    public function get_title(){
        return 'Google Map';
    }
    public function get_icon() {
        return 'wppb-font-location-map';
    }

    // Google Map block Settings Fields
    public function get_settings() {

        $settings = array(
            'apikey' => array(
                'type' => 'text',
                'title' => __('Google Maps API key','wp-pagebuilder'),
            ),
            'place' => array(
                'type' => 'text',
                'title' => __('Map place','wp-pagebuilder'),
            ),
            'height' => array(
                'type' => 'number',
                'title' => 'Height',
                'unit' => array( 'px','em','%' ),
                'responsive' => true,
                'std' => array(
                    'md' => '500px',
                    'sm' => '500px',
                    'xs' => '500px',
                ),
                'tab' => 'style',
                'selector' => '{{SELECTOR}} iframe { height: {{data.height}}; }',
            ),
        );
        return $settings;
    }

    // Google Map Render HTML
    public function render($data = null){
        $settings       = $data['settings'];
        $apikey         = isset($settings['apikey']) ? $settings['apikey'] : false;
        $place          = isset($settings['place']) ? $settings['place'] : false;

        $output = '<iframe src="https://www.google.com/maps/embed/v1/place?key=' . esc_attr( $apikey ) . '&q=' . esc_attr( $place ) . '" frameborder="0" style="width:100%; margin-bottom: 0; border:0" allowfullscreen></iframe>';
        return $output;
    }

    // Google Map Template
    public function getTemplate(){
        $output = '<iframe src="https://www.google.com/maps/embed/v1/place?key={{data.apikey}}&q={{data.place}}" frameborder="0" style="width:100%; margin-bottom: 0; border:0" allowfullscreen></iframe>';
        return $output;
    }

}
</code></pre>

<p>Looks simple, right? At the top, we have three methods that identify the addon: name, title and icon.</p>

<p>The next method, <code>get_settings()</code>, is where we define all of the user inputs. We define them as an array; I just looked at other addons to figure out the fields I can add. Pretty simple and easy to implement.</p>

<p>I figured out that the next method, <code>render()</code>, is used on the front end. It gets all of the user settings and returns the map iframe.</p>

<p>The last method, <code>getTemplate()</code>, is used on the page builder screen. Having two methods render the same code is not great, but I suppose the reason for it is that the second one has to be parsed with JavaScript.</p>

<p>Another thing that would work better is the method of registering an addon. If this were a more advanced addon, I’d want to include the CSS and JavaScript in separate files. Not very convenient, but also not the end of the world.</p>

<p>The last thing we have to do to register the addon is include it in the array, which we can do with a simple filter:</p>

<pre class="break-out"><code class="language-javascript">add_filter('wppb_available_addons', function( $addons) {
    $addons[] = 'JakubMikita_Addon_GoogleMap';
    return $addons;
} );
</code></pre>

<p>That’s all. The process is quick and simple. Here is our custom addon:</p>

<figure class="article__image break-out"></figure>

<p>We’ve now got an awesome full-page map on this page.</p>

<h3 id="creating-the-contact-us-page">Creating The &ldquo;Contact Us&rdquo; Page</h3>

<p>For the last page, let’s put a contact form. I was about to install one of the popular contact form plugins when I noticed the &ldquo;Form&rdquo; addon. I gave it a try.</p>

<p>Surprisingly, when I dropped the addon onto the page, I saw all of the fields I wanted already configured and aligned nicely.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c9105fde-596f-41e3-a71d-5400bb45f213/wppagebuilderplugin-image1.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c9105fde-596f-41e3-a71d-5400bb45f213/wppagebuilderplugin-image1.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c9105fde-596f-41e3-a71d-5400bb45f213/wppagebuilderplugin-image1.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c9105fde-596f-41e3-a71d-5400bb45f213/wppagebuilderplugin-image1.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c9105fde-596f-41e3-a71d-5400bb45f213/wppagebuilderplugin-image1.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c9105fde-596f-41e3-a71d-5400bb45f213/wppagebuilderplugin-image1.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c9105fde-596f-41e3-a71d-5400bb45f213/wppagebuilderplugin-image1.png"
			sizes="100vw"
			alt="The “Form” addon lets you easily create a Contact Us page"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<p>The most interesting part is that WP Page Builder integrates with the Contact Form 7 and weForms plugins. You can even add a simple CAPTCHA or use Google’s reCAPTCHA after providing the website’s keys.</p>

<p>Very cool addon. Submissions to the form come to my inbox without any problem, including all of the fields, and the user sees a nice confirmation message upon submitting the form.</p>

<h3 id="summary">Summary</h3>

<p>I must say that WP Page Builder is a solid plugin. Obviously, it have some flaws, but it’s still a young product, and I’m sure Themeum will fix all of the bugs and implement the improvements mentioned in this article.</p>

<p>The overall feel of the plugin is great. The plugin does most of the heavy lifting, and you don’t have to think about how to do what you want because it’s mostly already done. The default content does a really good job and speeds up the work.</p>

<p>Themeum is right: Building a page with its plugin is simple, but not because the plugin is basic. The plugin is intuitive, yet packed with cool addons.</p>

<p>I used only a few of the addons, but the plugin comes with a lot more. Blocks you’d normally spend hours trying to figure how to implement are a drag-and-drop away when using the WP Page Builder plugin.</p>

<p>For example, progress bars, social icons, testimonials and flipping content boxes are ready and waiting to be used. It’s hard to convey the experience in writing. You just have to  and see for yourself.</p>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(ms, ra, al, il)</span>
</div>


              </article>
            </body>
          </html>
---------------
<h1 id="#title_3" >4、人工智能白热化，运维脱帽“背锅侠”</h1>
李夏昕
[http://www.infoq.com/cn/news/2018/10/aiops-dev-heated-up?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/10/aiops-dev-heated-up?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>这里有一份运维人的充电计划，请查收。</p> <i>By 李夏昕</i>
---------------
<h1 id="#title_4" >5、Nuxt 2.0正式发布：支持 Webpack 4、ES module</h1>
Nuxt.js
[http://www.infoq.com/cn/news/2018/10/Nuxt2.0-release?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/10/Nuxt2.0-release?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>在Nuxt 1.4.0发布半年之后，Nuxt 2接踵而至。Nuxt 2带来了大量新特性和改进，并专注于稳定性、性能和更好的开发者体验。以下是新版本的主要变化。</p> <i>By Nuxt.js</i>
---------------