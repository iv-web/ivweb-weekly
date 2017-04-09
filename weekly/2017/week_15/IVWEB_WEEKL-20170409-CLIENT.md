## 文章索引
1、 <a href="#1#329:-an-opinionated-comparison-of-react-angular-and-aurelia" >#329: An opinionated comparison of React, Angular and Aurelia</a><br/>
2、 <a href="#2react-v1550" >React v15.5.0</a><br/>
3、 <a href="#3视频演讲-如何从0到1搭建弹性作业云elastic-job-cloud" >视频演讲： 如何从0到1搭建弹性作业云Elastic-Job-Cloud</a><br/>
4、 <a href="#4vibrant-illustrations-to-let-your-mind-wander" >Vibrant Illustrations To Let Your Mind Wander</a><br/><h1 id="#title_0" >1、#329: An opinionated comparison of React, Angular and Aurelia</h1>

[http://javascriptweekly.com/issues/329](http://javascriptweekly.com/issues/329)
<table border="0" width="100%" cellpadding="0" cellspacing="0" bgcolor="#ffffff" style="font-family: 'helvetica neue', helvetica, arial, sans-serif; font-size: 14px; line-height: 20px; color: #333"><tr><td align="center" valign="top">
<table border="0" width="600" cellpadding="0" cellspacing="0" class="container noarchive" style="border-collapse: collapse;"><tr><td style="padding-top: 6px; padding-bottom: 6px; font-size: 11px; text-align: center; color: #555; font-family: verdana, arial, sans-serif">
<span class="nomo">Regexes in a post-ES6 world, and why Glimmer is so fantastic.</span> — 
</td></tr></table>
<table border="0" width="600" cellpadding="0" cellspacing="0" class="container" style="border-collapse: collapse">
<tr><td style="background-color: #f7df1e"><table width="100%" cellspacing="0" cellpadding="0" align="left"><tr><td align="left" class="block" style="padding: 6px 12px;">
<table align="left" width="50%" class="gowide"><tr><td><span style="line-height: 36px; font-size: 23px; color: #f7df1e; font-weight: bold; color: #323330">JavaScript Weekly</span></td></tr></table>
<table align="left" style="text-align: right" width="50%" class="gowide lonmo"><tr><td><span style="font-size: 14px; line-height: 36px; font-weight: normal; color: #323330">
Issue 329 — April 7, 2017
</span></td></tr></table>
</td></tr></table></td></tr>
<tr><td style="padding: 16px 12px 12px 12px" align="left">
<p style="margin-top: 0; font-size: 1.0em; line-height: 1.4em; padding-top: 0; margin-bottom: 20px">We found too many releases were happening on Thursdays so <strong>JavaScript Weekly has moved back to Fridays</strong> :-) We're also working on a redesign and would love if you could anonymously  - all feedback welcomed.<br><em>- Peter Cooper, editor</em></p>
<div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">A look at new regex features introduced in ES6 or later, including the <code>y</code>, <code>u</code> and <code>s</code> flags, named capture groups, and look-behind assertions.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Nicolás Bevacqua
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">A practical, code-led look at how  provides the benefits of Ember’s fast rendering engine and sturdy tools without having to buy into the whole ecosystem.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Tristan Edwards
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">Opinion pieces are a dime-a-dozen but this shows some real insight and technical considerations. It also spawned a 
</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Jeff Schnitzer
</div>
<br clear="all" style="clear: both"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">A free, thorough and open source guide anyone could use to learn about the practice of front-end development. </div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Frontend Masters
  <span style="border: 1px solid #999; border-radius: 2px; color: #999; font-size: 11px; font-weight: normal; padding: 1px 5px 1px 5px; ">Sponsor</span>
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">Facebook merged a huge pull request into React that replaced its build process with one based on Rollup and not Webpack. But why?</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Rich Harris
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">A fast 3KB React alternative with the same API. 8.0 boasts significant performance improvements, smaller size, and fewer edge cases.  is the latest release.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Jason Miller
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">A cross-platform app including a simulator and integrated Node server.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Bita Djaghouri, Jin Choi, Mark Marcelo
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">It's in Chrome Canary only for now, but it shows you which lines were and weren’t used in each JavaScript and CSS file.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
LogRocket
</div>
<br clear="all" style="clear: both"><p style="color: #666666; font-size: 16px; font-weight: bold; margin-top: 8px; margin-bottom: 10px; text-transform: uppercase">Jobs </p>
<ul style="padding-left: 18px; margin-top: 10px; list-style-type: square">
<li style="color: #f7df1e; margin-bottom: 10px; font-size: 15px; line-height: 17px">
<span style="font-size: 12px; color: #666666">Let's help content creators get paid! We're blogfoster: the leading influencer marketing platform in Europe and we would like to hire you. React, Redux, and Node: It's JavaScript all the way down. Let's chat!</span> <span style="color: #999999; font-weight: normal; font-size: 12px; text-transform: uppercase; font-family: verdana, arial, sans-serif">BLOGFOSTER GMBH</span>
</li>
<li style="color: #f7df1e; margin-bottom: 10px; font-size: 15px; line-height: 17px">
<span style="font-size: 12px; color: #666666">Taxfix are looking for an experienced UI Developer who can help build UIs so anyone can file their taxes using our mobile apps.</span> <span style="color: #999999; font-weight: normal; font-size: 12px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Taxfix GmbH</span>
</li>
<li style="color: #f7df1e; margin-bottom: 10px; font-size: 15px; line-height: 17px">
<span style="font-size: 12px; color: #666666">Democracy only works when everyone knows enough to make good decisions. We’re here to make sure that they do, and we need your help.</span> <span style="color: #999999; font-weight: normal; font-size: 12px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Schibsted</span>
</li>
</ul>
<p style="color: #333; font-size: 12px; font-weight: normal; margin-top: 0px; margin-bottom: 10px">Can't find the right job? Want companies to apply to <em>you?</em> </p>
<p style="color: #666666; font-size: 16px; font-weight: bold; margin-top: 24px; margin-bottom: 10px; text-transform: uppercase">In Brief</p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #00aadd; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">news</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">Now 5 years old, a look at both Ember’s history and future.</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Tom Dale, Yehuda Katz, Godfrey Chan</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #00aadd; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">news</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Angular Attack</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> a year ago.</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Twitter</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">You can’t hide from them. GIFs are everywhere. Easily add Giphy GIFs to your app.</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">PubNub  <span style="border: 1px solid #999; border-radius: 2px; color: #999; font-size: 11px; font-weight: normal; padding: 1px 5px 1px 5px;">Sponsor</span></span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Maxim Koretskyi</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">Think of any more? Leave a comment.</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Alexander Myshov</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">How to use the new pipes functionality that replaces filters from Angular 1.</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Burke Holland</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #6ca629; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">node</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Valeri Karpov</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Ashraff Hathibelagal</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> 
<br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Sandbox - API Mocking Software  <span style="border: 1px solid #999; border-radius: 2px; color: #999; font-size: 11px; font-weight: normal; padding: 1px 5px 1px 5px;">Sponsor</span></span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #cc00cc; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">video</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Matt Andrews</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #cc00aa; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">podcast</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">Brendan Eich on his involvement with the WebAssembly specification. <em>1h24m</em>.</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Software Engineering Daily</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #AF7817; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">opinion</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">A personal view of the current state of JavaScript frameworks.</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Matt Burgess</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #bbbbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tools</span> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #6ca629; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">node</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">Helps to identify potential security hotspots.</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">The Node Security Platform</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #bbbbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tools</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">Stream your VR and 360 video with Netflix quality to all major devices using adaptive streaming (DASH and HLS).</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Bitmovin  <span style="border: 1px solid #999; border-radius: 2px; color: #999; font-size: 11px; font-weight: normal; padding: 1px 5px 1px 5px;">Sponsor</span></span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> (featured last week) with theming, effects, &amp; support for complex popovers.</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">atomiks</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #00bbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">code</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">For Facebook, Twitter, Instagram, YouTube and Pinterest content.</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Shobhit Sharma</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #00bbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">code</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif"></span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #00bbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">code</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">Packs booleans into Uint32Arrays for efficiency.</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Brock Whittaker</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #00bbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">code</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">PayPal</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> is an arcane yet still encountered image format.</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Photopea</span></p>
</td></tr>
<tr><td bgcolor="#f4f4f4" style="font-family: verdana, helvetica, arial, sans-serif; text-align: left; padding-top: 12px; padding-left: 12px; padding-right: 12px; padding-bottom: 12px" class="noarchive">
<p style="line-height: 15px; font-size: 11px; margin-top: 0">Curated by .</p>
<p style="line-height: 15px; font-size: 11px; margin-top: 0">Like this? You may also enjoy: </p>
<p style="font-size: 13px"></p>
<p style="font-size: 11px; line-height: 15px">© Cooperpress Ltd. Office 30, Lincoln Way, Louth, LN11 0LS, UK</p>
</td></tr>
</table>
</td></tr></table>
---------------
<h1 id="#title_1" >2、React v15.5.0</h1>

[https://facebook.github.io/react/blog/2017/04/07/react-v15.5.0.html](https://facebook.github.io/react/blog/2017/04/07/react-v15.5.0.html)
<p>It&#39;s been exactly one year since the last breaking change to React. Our next major release, React 16, will include some exciting improvements, including a , and are committed to bringing those improvements to all of our users with minimal effort.</p>

<p>To that end, today we&#39;re releasing React 15.5.0.</p>

<h3>New Deprecation Warnings</h3>

<p>The biggest change is that we&#39;ve extracted <code>React.PropTypes</code> and <code>React.createClass</code> into their own packages. Both are still accessible via the main <code>React</code> object, but using either will log a one-time deprecation warning to the console when in development mode. This will enable future code size optimizations.</p>

<p>These warnings will not affect the behavior of your application. However, we realize they may cause some frustration, particularly if you use a testing framework that treats <code>console.error</code> as a failure.</p>

<p><strong>Adding new warnings is not something we do lightly.</strong> Warnings in React are not mere suggestions — they are integral to our strategy of keeping as many people as possible on the latest version of React. We never add warnings without providing an incremental path forward.</p>

<p>So while the warnings may cause frustration in the short-term, we believe <strong>prodding developers to migrate their codebases now prevents greater frustration in the future</strong>. Proactively fixing warnings ensures you are prepared for the next major release. If your app produces zero warnings in 15.5, it should continue to work in 16 without any changes.</p>

<p>For each of these new deprecations, we&#39;ve provided a codemod to automatically migrate your code. They are available as part of the  project.</p>

<h3>Migrating from React.PropTypes</h3>

<p>Prop types are a feature for runtime validation of props during development. We&#39;ve extracted the built-in prop types to a separate package to reflect the fact that not everybody uses them.</p>

<p>In 15.5, instead of accessing <code>PropTypes</code> from the main <code>React</code> object, install the <code>prop-types</code> package and import them from there:</p>
<div class="highlight"><pre><code class="language-js" data-lang="js"><span class="c1">// Before (15.4 and below)</span>
<span class="kr">import</span> <span class="nx">React</span> <span class="nx">from</span> <span class="s1">&#39;react&#39;</span><span class="p">;</span>

<span class="kr">class</span> <span class="nx">Component</span> <span class="kr">extends</span> <span class="nx">React</span><span class="p">.</span><span class="nx">Component</span> <span class="p">{</span>
  <span class="nx">render</span><span class="p">()</span> <span class="p">{</span>
    <span class="k">return</span> <span class="o">&lt;</span><span class="nx">div</span><span class="o">&gt;</span><span class="p">{</span><span class="k">this</span><span class="p">.</span><span class="nx">props</span><span class="p">.</span><span class="nx">text</span><span class="p">}</span><span class="o">&lt;</span><span class="err">/div&gt;;</span>
  <span class="p">}</span>
<span class="p">}</span>

<span class="nx">Component</span><span class="p">.</span><span class="nx">propTypes</span> <span class="o">=</span> <span class="p">{</span>
<span class="hll">  <span class="nx">text</span><span class="o">:</span> <span class="nx">React</span><span class="p">.</span><span class="nx">PropTypes</span><span class="p">.</span><span class="nx">string</span><span class="p">.</span><span class="nx">isRequired</span><span class="p">,</span>
</span><span class="p">}</span>

<span class="c1">// After (15.5)</span>
<span class="kr">import</span> <span class="nx">React</span> <span class="nx">from</span> <span class="s1">&#39;react&#39;</span><span class="p">;</span>
<span class="hll"><span class="kr">import</span> <span class="nx">PropTypes</span> <span class="nx">from</span> <span class="s1">&#39;prop-types&#39;</span><span class="p">;</span>
</span>
<span class="kr">class</span> <span class="nx">Component</span> <span class="kr">extends</span> <span class="nx">React</span><span class="p">.</span><span class="nx">Component</span> <span class="p">{</span>
  <span class="nx">render</span><span class="p">()</span> <span class="p">{</span>
    <span class="k">return</span> <span class="o">&lt;</span><span class="nx">div</span><span class="o">&gt;</span><span class="p">{</span><span class="k">this</span><span class="p">.</span><span class="nx">props</span><span class="p">.</span><span class="nx">text</span><span class="p">}</span><span class="o">&lt;</span><span class="err">/div&gt;;</span>
  <span class="p">}</span>
<span class="p">}</span>

<span class="nx">Component</span><span class="p">.</span><span class="nx">propTypes</span> <span class="o">=</span> <span class="p">{</span>
<span class="hll">  <span class="nx">text</span><span class="o">:</span> <span class="nx">PropTypes</span><span class="p">.</span><span class="nx">string</span><span class="p">.</span><span class="nx">isRequired</span><span class="p">,</span>
</span><span class="p">};</span>
</code></pre></div>
<p>The  for this change performs this conversion automatically. Basic usage:</p>
<div class="highlight"><pre><code class="language-bash" data-lang="bash">jscodeshift -t react-codemod/transforms/React-PropTypes-to-prop-types.js &lt;path&gt;
</code></pre></div>
<p>The <code>propTypes</code>, <code>contextTypes</code>, and <code>childContextTypes</code> APIs will work exactly as before. The only change is that the built-in validators now live in a separate package.</p>

<p>You may also consider using .</p>

<h3>Migrating from React.createClass</h3>

<p>When React was initially released, there was no idiomatic way to create classes in JavaScript, so we provided our own: <code>React.createClass</code>.</p>

<p>Later, classes were added to the language as part of ES2015, so we added the ability to create React components using JavaScript classes. <strong>Along with functional components, JavaScript classes are now the .</strong></p>

<p>For your existing <code>createClass</code> components, we recommend that you migrate them to JavaScript classes. However, if you have components that rely on mixins, converting to classes may not be immediately feasible. If so, <code>create-react-class</code> is available on npm as a drop-in replacement:</p>
<div class="highlight"><pre><code class="language-js" data-lang="js"><span class="c1">// Before (15.4 and below)</span>
<span class="kd">var</span> <span class="nx">React</span> <span class="o">=</span> <span class="nx">require</span><span class="p">(</span><span class="s1">&#39;react&#39;</span><span class="p">);</span>

<span class="hll"><span class="kd">var</span> <span class="nx">Component</span> <span class="o">=</span> <span class="nx">React</span><span class="p">.</span><span class="nx">createClass</span><span class="p">({</span>
</span>  <span class="nx">mixins</span><span class="o">:</span> <span class="p">[</span><span class="nx">MixinA</span><span class="p">],</span>
  <span class="nx">render</span><span class="p">()</span> <span class="p">{</span>
    <span class="k">return</span> <span class="o">&lt;</span><span class="nx">Child</span> <span class="o">/&gt;</span><span class="p">;</span>
  <span class="p">}</span>
<span class="p">});</span>

<span class="c1">// After (15.5)</span>
<span class="kd">var</span> <span class="nx">React</span> <span class="o">=</span> <span class="nx">require</span><span class="p">(</span><span class="s1">&#39;react&#39;</span><span class="p">);</span>
<span class="hll"><span class="kd">var</span> <span class="nx">createReactClass</span> <span class="o">=</span> <span class="nx">require</span><span class="p">(</span><span class="s1">&#39;create-react-class&#39;</span><span class="p">);</span>
</span>
<span class="hll"><span class="kd">var</span> <span class="nx">Component</span> <span class="o">=</span> <span class="nx">createReactClass</span><span class="p">({</span>
</span>  <span class="nx">mixins</span><span class="o">:</span> <span class="p">[</span><span class="nx">MixinA</span><span class="p">],</span>
  <span class="nx">render</span><span class="p">()</span> <span class="p">{</span>
    <span class="k">return</span> <span class="o">&lt;</span><span class="nx">Child</span> <span class="o">/&gt;</span><span class="p">;</span>
  <span class="p">}</span>
<span class="p">});</span>
</code></pre></div>
<p>Your components will continue to work the same as they did before.</p>

<p>The  for this change attempts to convert a <code>createClass</code> component to a JavaScript class, with a fallback to <code>create-react-class</code> if necessary. It has converted thousands of components internally at Facebook.</p>

<p>Basic usage:</p>
<div class="highlight"><pre><code class="language-bash" data-lang="bash">jscodeshift -t react-codemod/transforms/class.js path/to/components
</code></pre></div>
<h3>Discontinuing support for React Addons</h3>

<p>We&#39;re discontinuing active maintenance of React Addons packages. In truth, most of these packages haven&#39;t been actively maintained in a long time. They will continue to work indefinitely, but we recommend migrating away as soon as you can to prevent future breakages.</p>

<ul>
<li><strong>react-addons-create-fragment</strong> – React 16 will have first-class support for fragments, at which point this package won&#39;t be necessary. We recommend using arrays of keyed elements instead.</li>
<li><strong>react-addons-css-transition-group</strong> - Use  instead. Version 1.1.1 provides a drop-in replacement.</li>
<li><strong>react-addons-linked-state-mixin</strong> - Explicitly set the <code>value</code> and <code>onChange</code> handler instead.</li>
<li><strong>react-addons-pure-render-mixin</strong> - Use  instead.</li>
<li><strong>react-addons-shallow-compare</strong> - Use  instead.</li>
<li><strong>react-addons-transition-group</strong> - Use  instead. Version 1.1.1 provides a drop-in replacement.</li>
<li><strong>react-addons-update</strong> - Use  instead, a drop-in replacement.</li>
<li><strong>react-linked-input</strong> - Explicitly set the <code>value</code> and <code>onChange</code> handler instead.</li>
</ul>

<p>We&#39;re also discontinuing support for the <code>react-with-addons</code> UMD build. It will be removed in React 16.</p>

<h3>React Test Utils</h3>

<p>Currently, the React Test Utils live inside <code>react-addons-test-utils</code>. As of 15.5, we&#39;re deprecating that package and moving them to <code>react-dom/test-utils</code> instead:</p>
<div class="highlight"><pre><code class="language-js" data-lang="js"><span class="c1">// Before (15.4 and below)</span>
<span class="kr">import</span> <span class="nx">TestUtils</span> <span class="nx">from</span> <span class="s1">&#39;react-addons-test-utils&#39;</span><span class="p">;</span>

<span class="c1">// After (15.5)</span>
<span class="kr">import</span> <span class="nx">TestUtils</span> <span class="nx">from</span> <span class="s1">&#39;react-dom/test-utils&#39;</span><span class="p">;</span>
</code></pre></div>
<p>This reflects the fact that what we call the Test Utils are really a set of APIs that wrap the DOM renderer.</p>

<p>The exception is shallow rendering, which is not DOM-specific. The shallow renderer has been moved to <code>react-test-renderer/shallow</code>.</p>
<div class="highlight"><pre><code class="language-js" data-lang="js"><span class="c1">// Before (15.4 and below)</span>
<span class="hll"><span class="kr">import</span> <span class="p">{</span> <span class="nx">createRenderer</span> <span class="p">}</span> <span class="nx">from</span> <span class="s1">&#39;react-addons-test-utils&#39;</span><span class="p">;</span>
</span>
<span class="c1">// After (15.5)</span>
<span class="hll"><span class="kr">import</span> <span class="p">{</span> <span class="nx">createRenderer</span> <span class="p">}</span> <span class="nx">from</span> <span class="s1">&#39;react-test-renderer/shallow&#39;</span><span class="p">;</span>
</span></code></pre></div>
<hr>

<h2>Acknowledgements</h2>

<p>A special thank you to these folks for transferring ownership of npm package names:</p>

<ul>
<li></li>
<li></li>
<li></li>
</ul>

<hr>

<h2>Installation</h2>

<p>We recommend using  is a good place to get started.</p>

<p>To install React with Yarn, run:</p>
<div class="highlight"><pre><code class="language-bash" data-lang="bash">yarn add react@15.5.0 react-dom@15.5.0
</code></pre></div>
<p>To install React with npm, run:</p>
<div class="highlight"><pre><code class="language-bash" data-lang="bash">npm install --save react@15.5.0 react-dom@15.5.0
</code></pre></div>
<p>We recommend using a bundler like  so you can write modular code and bundle it together into small packages to optimize load time.</p>

<p>Remember that by default, React runs extra checks and provides helpful warnings in development mode. When deploying your app, make sure to .</p>

<p>In case you don&#39;t use a bundler, we also provide pre-built bundles in the npm packages which you can  on your page:</p>

<ul>
<li><strong>React</strong><br>
Dev build with warnings: <br>
Minified build for production: <br></li>
<li><strong>React with Add-Ons</strong><br>
Dev build with warnings: <br>
Minified build for production: <br></li>
<li><strong>React DOM</strong> (include React in the page before React DOM)<br>
Dev build with warnings: <br>
Minified build for production: <br></li>
<li><strong>React DOM Server</strong> (include React in the page before React DOM Server)<br>
Dev build with warnings: <br>
Minified build for production: </li>
</ul>

<p>We&#39;ve also published version <code>15.5.0</code> of the <code>react</code>, <code>react-dom</code>, and addons packages on npm and the <code>react</code> package on bower.</p>

<hr>

<h2>Changelog</h2>

<h2>15.5.0 (April 7, 2017)</h2>

<h3>React</h3>

<ul>
<li>Added a deprecation warning for <code>React.createClass</code>. Points users to create-react-class instead. ()</li>
<li>Added a deprecation warning for <code>React.PropTypes</code>. Points users to prop-types instead. ()</li>
<li>Fixed an issue when using <code>ReactDOM</code> together with <code>ReactDOMServer</code>. ()</li>
<li>Fixed issue with Closure Compiler. ()</li>
<li>Another fix for Closure Compiler. ()</li>
<li>Added component stack info to invalid element type warning. ()</li>
</ul>

<h3>React DOM</h3>

<ul>
<li>Fixed Chrome bug when backspacing in number inputs. ()</li>
<li>Added <code>react-dom/test-utils</code>, which exports the React Test Utils. ()</li>
</ul>

<h3>React Test Renderer</h3>

<ul>
<li>Fixed bug where <code>componentWillUnmount</code> was not called for children. ()</li>
<li>Added <code>react-test-renderer/shallow</code>, which exports the shallow renderer. ()</li>
</ul>

<h3>React Addons</h3>

<ul>
<li>Last release for addons; they will no longer be actively maintained.</li>
<li>Removed <code>peerDependencies</code> so that addons continue to work indefinitely. ()</li>
<li>Updated to remove references to <code>React.createClass</code> and <code>React.PropTypes</code> ()</li>
<li><code>react-addons-test-utils</code> is deprecated. Use <code>react-dom/test-utils</code> and <code>react-test-renderer/shallow</code> instead. ()</li>
</ul>
---------------
<h1 id="#title_2" >3、视频演讲： 如何从0到1搭建弹性作业云Elastic-Job-Cloud</h1>
高洪涛
[http://www.infoq.com/cn/presentations/how-to-build-elastic-job-cloud?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/how-to-build-elastic-job-cloud?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/how-to-build-elastic-job-cloud/zh/mediumimage/gaohongtao270.jpg"/><p>Elastic-Job-Cloud是当当开源的第二代弹性作业项目，该项目结合Apache Mesos资源调度器实现了对物理资源的弹性管理，并已经成为Mesos官方认证项目。当当目前正在使用该项目构建新一代作业IPaaS平台，该平台未来将承载当当大部分在线与离线作业的运行。本次分享将为您带来当当是如何从0到1构建大规模作业云平台的。</p> <i>By 高洪涛</i>
---------------
<h1 id="#title_3" >4、Vibrant Illustrations To Let Your Mind Wander</h1>
Veerle Pieters
[https://www.smashingmagazine.com/2017/04/vibrant-illustrations-inspiration/](https://www.smashingmagazine.com/2017/04/vibrant-illustrations-inspiration/)
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
</table><p>On days when things don't seem to go as you'd like them to and inspiration is at its lowest, it's good to take a short break and go outside to try and <strong>empty your mind</strong>. That always seems to be the best remedy for me, especially whenever I jump on my bike and go for a short ride.</p>

<figure></figure>

<p>Now the time has come to enjoy these moments even more as the spring season finally starts to show up in nature. We're starting to see green leaves on the trees again, and every morning I wake up to the sounds of the birds chirping. I really enjoy these small joys of spring &#8212; who doesn't?</p><p>The post .</p>
---------------