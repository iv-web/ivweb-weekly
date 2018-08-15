## 文章索引
1、 <a href="#1uber开源fusionjs一个基于插件架构的通用web框架" >Uber开源Fusion.js：一个基于插件架构的通用Web框架</a><br/>
2、 <a href="#2the-complete-anatomy-of-the-gutenberg-wordpress-editor" >The Complete Anatomy Of The Gutenberg WordPress Editor</a><br/>
3、 <a href="#3文章-想要高效上传下载试试去中心化的docker镜像仓库设计" >文章： 想要高效上传下载？试试去中心化的Docker镜像仓库设计</a><br/>
4、 <a href="#4文章-敏捷反思的实践和应用" >文章： 敏捷：反思的实践和应用</a><br/>
5、 <a href="#5文章-都去炒ai和大数据了落地的事儿谁来做" >文章： 都去炒AI和大数据了，落地的事儿谁来做？</a><br/>
6、 <a href="#6全球区块链生态技术大会日程揭底" >全球区块链生态技术大会日程揭底</a><br/>
7、 <a href="#7vmware的云管理之道" >VMware的云管理之道</a><br/>
8、 <a href="#8不挡脸放肆看b站黑科技蒙版弹幕揭秘" >不挡脸，放肆看！B站黑科技蒙版弹幕揭秘</a><br/>
9、 <a href="#9专访王连诚让新技术在银行领域落地打造经典区块链产业案例" >专访王连诚：让新技术在银行领域落地，打造经典区块链产业案例</a><br/><h1 id="#title_0" >1、Uber开源Fusion.js：一个基于插件架构的通用Web框架</h1>
Uber
[http://www.infoq.com/cn/news/2018/08/uber-Web-open-fusion-js?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/08/uber-Web-open-fusion-js?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Uber的Web平台团队开发了Fusion.js，一个开源的Web框架，用于简化Web开发，并构建出高性能的轻量级Web应用程序。</p> <i>By Uber</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_1" >2、The Complete Anatomy Of The Gutenberg WordPress Editor</h1>
Manish Dudharejia
[https://www.smashingmagazine.com/2018/08/complete-anatomy-gutenberg-wordpress-editor/](https://www.smashingmagazine.com/2018/08/complete-anatomy-gutenberg-wordpress-editor/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/08/complete-anatomy-gutenberg-wordpress-editor/" />
              <title>The Complete Anatomy Of The Gutenberg WordPress Editor</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>The Complete Anatomy Of The Gutenberg WordPress Editor</h1>
                  
                    
                    <address>Manish Dudharejia</address>
                  
                  <time datetime="2018-08-14T14:00:22&#43;02:00" class="op-published">2018-08-14T14:00:22+02:00</time>
                  <time datetime="2018-08-14T18:39:34&#43;00:00" class="op-modified">2018-08-14T18:39:34+00:00</time>
                </header>
                

<p>It seems that Gutenberg has been a term of controversy in the world of WordPress lately. Hailed as the most significant change to  this year, the Gutenberg editor has received a mixed response from web developers and regular folk alike. All of this chaos is making it difficult to see Gutenberg for what it really is. So, I’ll try to put some of the confusion to rest once and for all.</p>

<p>In this article, I will cover the following:</p>

<ol>
<li></li>
<li></li>
<li></li>
<li></li>
<li></li>
<li></li>
<li></li>
<li></li>
<li></li>
</ol>

<h3 id="1-what-is-gutenberg-a-name-what-is-gutenberg-a">1. What Is Gutenberg? </h3>

<p>Named after Johannes Gutenberg, who invented the mechanical printing press, Gutenberg was introduced to the world by Matt Mullenweg at . In essence, Gutenberg is a new WordPress editor, with dozens of cutting-edge features. It simplifies website creation and editing for the average non-technical user.</p>

<p>It has earned several accolades, from &ldquo;WordPress’s new publishing experience&rdquo; to “the future of website creation”. Some skeptics think it is the nail in the coffin for WordPress. All this babble aside, Gutenberg is going to be way more than just an editor for WordPress (which I will discuss next).</p>

<p>It allows website creators to build a website using blocks, which are small drag-and-drop units. Thus, it replaces the current inconsistent and distracting customization process. It also enables HTML tags such as <code>section</code> and <code>figure</code>, outputting solid HTML. At the time of writing, Gutenberg is still a plugin. However, the community is planning to merge it with WordPress 5.0 this year.</p>



<aside class="product-panel product-panel__tilted product-panel--book" data-audience="non-subscriber">
    <div class="container product-panel--book__container">
      <div class="panel__description panel__description--book">
    <p>Getting workflow <em>just</em> right ain’t an easy task. So are proper estimates. Or alignment among different departments. That’s why we’ve set up <strong>“this-is-how-I-work”-sessions</strong> — with smart cookies sharing what works well for them. A part of the , of course.</p>
      <a href="http://smashed.by/workflowpanelmembership" class="btn btn--green btn--large">
        Explore features&nbsp;→
      </a>
      </div>
      <div class="panel__image panel__image--book">
        <a href="http://smashed.by/workflowpanelmembership" class="books__book__image">
        <div class="books__book__img">
          <img src="https://www.smashingmagazine.com/images/smashing-cat/smashing-tv-box-cat.svg" alt="Smashing TV, with live sessions for professional designers and developers." width="310" height="400">
        </div>
      </a>
      </div>
    </div>
  </aside>




<h3 id="2-more-than-just-an-editor-a-name-more-than-just-an-editor-a">2. More Than Just An Editor </h3>

<p>Gutenberg is more than just an editor because it allows you to handle website content in customizable chunks or blocks. You don’t need to be fluent in HTML or write shortcodes. You can control a website’s entire layout (both back end and front end) from a single console.</p>

<p>This new editor attempts to combine the best features from both page-builder plugins such as , as well as do-it-yourself platforms such as Medium, Wix and Squarespace. So, just like those page-builder plugins, you can handle multi-column layouts through a single interface.</p>

<p>Does this spell the end of plugins such as Divi and Beaver Builder? That’s a topic for another post, but the short answer is no. Gutenberg is unlikely to replace those plugins completely. You can continue to use them even once Gutenberg becomes the default editor.</p>

<h3 id="3-what-does-gutenberg-change-in-wordpress-a-name-what-does-gutenberg-change-in-wordpress-a">3. What Does Gutenberg Change In WordPress? </h3>

<p>The sole purpose of the Gutenberg editor is to provide an alternative to the current open text editor, not to mention the difficult-to-remember shortcodes, with an agile and visual user interface (UI). So, unlike the current WordPress editor, you don’t have to:</p>

<ul>
<li>import images, multimedia and approved files from the media library or add HTML shortcodes;</li>
<li>copy and paste links for embeds;</li>
<li>write shortcodes for specialized assets of different plugins;</li>
<li>create featured images to be added at the top of a post or page;</li>
<li>add excerpts for subheads;</li>
<li>add widgets for content on the side of a page.</li>
</ul>

<p>In short, Gutenberg doesn’t change how WordPress functions. It does, however, change the way website owners (or creators) interact with it. Instead of a whole lot of shortcodes and meta boxes, you will be using simple blocks.</p>

<h5 id="what-are-blocks">What Are Blocks?</h5>

<p>Consider a block as the most basic (therefore, smallest) unit of the new editor. They will be the building blocks of WordPress 5.0. In other words, everything—including content, images, quotes, galleries, cover images, audio, video, headings, embeds, custom codes, paragraphs, separators and buttons—will turn into distinct blocks. Because you can drag and drop each block, identifying these items and placing them on the page becomes a lot easier.</p>

<h3 id="4-installing-gutenberg-a-name-installing-gutenberg-a">4. Installing Gutenberg </h3>

<p>You can download the latest version of Gutenberg directly from the  or later) to install the Gutenberg editor.</p>

<ol>
<li>Sign into your WordPress admin dashboard.</li>
<li>Go to the Plugins menu on the left side of the dashboard.</li>
<li>Click &ldquo;Plugins&rdquo; to open the “Add New” menu.</li>
<li>Type &ldquo;Gutenberg&rdquo; in the search box, located in the top-left corner.</li>
<li>You will see the Gutenberg plugin in the results.</li>
<li>Click the &ldquo;Install Now&rdquo; button.</li>
<li>Click the &ldquo;Activate&rdquo; button to initiate the plugin.</li>
</ol>

<figure>)</figcaption></figure>

<h3 id="5-exploring-gutenberg-at-length-a-name-exploring-gutenberg-at-length-a">5. Exploring Gutenberg At Length </h3>

<p>Once installed and activated, Gutenberg will show an icon in the left menu bar. When you launch it for the first time, you will see a new sample post, titled &ldquo;Gutenberg Demo.&rdquo; You can practice on the demo post before creating your own.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/92f1463c-c6b8-4e1e-82b2-12f49d0c9631/gutenberg-editor-gutenberg-demo.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/92f1463c-c6b8-4e1e-82b2-12f49d0c9631/gutenberg-editor-gutenberg-demo.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/92f1463c-c6b8-4e1e-82b2-12f49d0c9631/gutenberg-editor-gutenberg-demo.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/92f1463c-c6b8-4e1e-82b2-12f49d0c9631/gutenberg-editor-gutenberg-demo.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/92f1463c-c6b8-4e1e-82b2-12f49d0c9631/gutenberg-editor-gutenberg-demo.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/92f1463c-c6b8-4e1e-82b2-12f49d0c9631/gutenberg-editor-gutenberg-demo.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/92f1463c-c6b8-4e1e-82b2-12f49d0c9631/gutenberg-editor-gutenberg-demo.jpg"
			sizes="100vw"
			alt="Gutenberg Demo"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Gutenberg Sample Post ()
		</figcaption>
	
</figure>


<h4 id="a-add-new">A. Add New</h4>

<p>Go to &ldquo;Posts&rdquo; in the left menu bar of your WordPress dashboard. The new post will launch in Gutenberg first. You can later edit it in both the classic editor and Gutenberg.</p>

<figure>)</figcaption></figure>

<h4 id="b-edit">B. Edit</h4>

<p>Go to the &ldquo;Posts&rdquo; menu, and hover the mouse over a saved post to see the option to choose between the two editors. Although the classic editor option is available for the time being, it will most likely be removed with the launch of WordPress 5.0.</p>

<figure>)</figcaption></figure>

<h4 id="c-switch-between-editors">C. Switch Between Editors</h4>

<p>You can also switch between the two editors when editing a post. Click on the dropdown menu in the upper-right corner to toggle between the visual editor mode and the text editor (i.e. code). Alternatively, you can also use the shortcut <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>Alt</kbd> + <kbd>M</kbd> to switch between editors.</p>

<p>Text editor:</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/242af93b-0b8e-4acd-bbbd-b4bdf8cbaf24/gutenberg-editor-code-editor.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/242af93b-0b8e-4acd-bbbd-b4bdf8cbaf24/gutenberg-editor-code-editor.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/242af93b-0b8e-4acd-bbbd-b4bdf8cbaf24/gutenberg-editor-code-editor.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/242af93b-0b8e-4acd-bbbd-b4bdf8cbaf24/gutenberg-editor-code-editor.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/242af93b-0b8e-4acd-bbbd-b4bdf8cbaf24/gutenberg-editor-code-editor.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/242af93b-0b8e-4acd-bbbd-b4bdf8cbaf24/gutenberg-editor-code-editor.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/242af93b-0b8e-4acd-bbbd-b4bdf8cbaf24/gutenberg-editor-code-editor.jpg"
			sizes="100vw"
			alt="The text editor in Gutenberg"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The text editor in Gutenberg ()
		</figcaption>
	
</figure>


<p>Visual editor:</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/abd80a2a-d19b-42bb-9569-b5cf7121df5f/gutenberg-editor-visual-editor.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/abd80a2a-d19b-42bb-9569-b5cf7121df5f/gutenberg-editor-visual-editor.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/abd80a2a-d19b-42bb-9569-b5cf7121df5f/gutenberg-editor-visual-editor.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/abd80a2a-d19b-42bb-9569-b5cf7121df5f/gutenberg-editor-visual-editor.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/abd80a2a-d19b-42bb-9569-b5cf7121df5f/gutenberg-editor-visual-editor.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/abd80a2a-d19b-42bb-9569-b5cf7121df5f/gutenberg-editor-visual-editor.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/abd80a2a-d19b-42bb-9569-b5cf7121df5f/gutenberg-editor-visual-editor.jpg"
			sizes="100vw"
			alt="The visual editor in Gutenberg"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The visual editor in Gutenberg ()
		</figcaption>
	
</figure>


<h4 id="d-copy-all-content">D. Copy All Content</h4>

<p>This feature allows you to copy all content in the HTML version with just one click. You can open this feature in both editors by clicking on the dropdown menu in the upper-right corner of the dashboard.</p>

<figure>)</figcaption></figure>

<h4 id="e-content-structures">E. Content Structures</h4>

<p>This feature allows you to count the number of words in an entire post. You can also see the number of headings, paragraphs and blocks with just a click. Click the information icon (i) in the upper-left area.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/64b9fe7a-6b6f-4be0-a57e-d6792ad1dd5d/gutenberg-editor-content-structures.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/64b9fe7a-6b6f-4be0-a57e-d6792ad1dd5d/gutenberg-editor-content-structures.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/64b9fe7a-6b6f-4be0-a57e-d6792ad1dd5d/gutenberg-editor-content-structures.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/64b9fe7a-6b6f-4be0-a57e-d6792ad1dd5d/gutenberg-editor-content-structures.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/64b9fe7a-6b6f-4be0-a57e-d6792ad1dd5d/gutenberg-editor-content-structures.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/64b9fe7a-6b6f-4be0-a57e-d6792ad1dd5d/gutenberg-editor-content-structures.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/64b9fe7a-6b6f-4be0-a57e-d6792ad1dd5d/gutenberg-editor-content-structures.jpg"
			sizes="100vw"
			alt="Content Structures"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Content information in Gutenberg ()
		</figcaption>
	
</figure>


<h4 id="f-redo-and-undo">F. Redo and Undo</h4>

<p>You can find these options next to the information icon (i). They allow you to undo or redo the last command.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/978348a9-0ba3-489d-bbd3-3f9820230d29/gutenberg-editor-undo-redo.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/978348a9-0ba3-489d-bbd3-3f9820230d29/gutenberg-editor-undo-redo.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/978348a9-0ba3-489d-bbd3-3f9820230d29/gutenberg-editor-undo-redo.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/978348a9-0ba3-489d-bbd3-3f9820230d29/gutenberg-editor-undo-redo.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/978348a9-0ba3-489d-bbd3-3f9820230d29/gutenberg-editor-undo-redo.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/978348a9-0ba3-489d-bbd3-3f9820230d29/gutenberg-editor-undo-redo.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/978348a9-0ba3-489d-bbd3-3f9820230d29/gutenberg-editor-undo-redo.jpg"
			sizes="100vw"
			alt="Undo and Redo command"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Undo&#47;Redo Command ()
		</figcaption>
	
</figure>


<h4 id="g-page-and-document-settings">G. Page and Document Settings</h4>

<p>This allows you to change various page and document settings. You can find it in the right menu bar. You can make the following adjustments:</p>

<ul>
<li>Make a post public or private.</li>
<li>Change the publishing date.</li>
<li>Select a post’s format.</li>
<li>Add or edit categories and tags.</li>
<li>Upload featured images.</li>
<li>Write an excerpt.</li>
<li>Enable and disable comments, pingbacks and trackbacks.</li>
</ul>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e17825da-447e-4209-827e-f6e3c6374baf/gutenberg-editor-page-document-settings.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e17825da-447e-4209-827e-f6e3c6374baf/gutenberg-editor-page-document-settings.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e17825da-447e-4209-827e-f6e3c6374baf/gutenberg-editor-page-document-settings.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e17825da-447e-4209-827e-f6e3c6374baf/gutenberg-editor-page-document-settings.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e17825da-447e-4209-827e-f6e3c6374baf/gutenberg-editor-page-document-settings.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e17825da-447e-4209-827e-f6e3c6374baf/gutenberg-editor-page-document-settings.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e17825da-447e-4209-827e-f6e3c6374baf/gutenberg-editor-page-document-settings.jpg"
			sizes="100vw"
			alt="Page and Document Settings"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Page&#47;Document Settings ()
		</figcaption>
	
</figure>


<h4 id="h-stick-to-front-page">H. Stick to Front Page</h4>

<p>This feature will come handy if you’re running a blog. When you turn this on in the document settings, that particular post will always appear on the front page of your blog. And just turn it off to remove it from the front page.</p>

<figure>)</figcaption></figure>

<h4 id="i-using-blocks">I. Using Blocks</h4>

<p>As mentioned, blocks are the fundamental unit of the new Gutenberg editor. To use Gutenberg efficiently, you need to understand how to use these blocks. I will cover the main blocks one by one. Click the plus (+) button next to the redo/undo option to open the blocks menu.</p>

<h5 id="common-blocks">Common Blocks</h5>

<p>Common blocks allow you to add the elements required to create a rich UI.</p>

<ul>
<li><strong>Paragraph</strong><br />
The paragraph block comes with a few excellent features, such as custom font sizes, drop caps, background colors and text colors, among others. You are also able to add more CSS classes here.</li>
</ul>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c818f2ac-170e-433f-89cf-485ca20dc311/gutenberg-text-editor-options.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c818f2ac-170e-433f-89cf-485ca20dc311/gutenberg-text-editor-options.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c818f2ac-170e-433f-89cf-485ca20dc311/gutenberg-text-editor-options.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c818f2ac-170e-433f-89cf-485ca20dc311/gutenberg-text-editor-options.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c818f2ac-170e-433f-89cf-485ca20dc311/gutenberg-text-editor-options.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c818f2ac-170e-433f-89cf-485ca20dc311/gutenberg-text-editor-options.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c818f2ac-170e-433f-89cf-485ca20dc311/gutenberg-text-editor-options.jpg"
			sizes="100vw"
			alt="Gutenberg Text Editor Options"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Gutenberg Text Editor Options ()
		</figcaption>
	
</figure>


<ul>
<li><strong>Image</strong><br />
This element comes with a new feature that allows you to toggle between gallery and image layouts. You also get more control over images because you can set particular size dimensions, percentage size ratios, and an alternative text description for each image.</li>
</ul>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6c7f3656-81e9-4f5b-8465-b8e1823663de/gutenberg-editor-image-settings.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6c7f3656-81e9-4f5b-8465-b8e1823663de/gutenberg-editor-image-settings.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6c7f3656-81e9-4f5b-8465-b8e1823663de/gutenberg-editor-image-settings.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6c7f3656-81e9-4f5b-8465-b8e1823663de/gutenberg-editor-image-settings.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6c7f3656-81e9-4f5b-8465-b8e1823663de/gutenberg-editor-image-settings.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6c7f3656-81e9-4f5b-8465-b8e1823663de/gutenberg-editor-image-settings.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6c7f3656-81e9-4f5b-8465-b8e1823663de/gutenberg-editor-image-settings.jpg"
			sizes="100vw"
			alt="Image Settings in Gutenberg"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Image Settings in Gutenberg ()
		</figcaption>
	
</figure>


<ul>
<li><strong>Other elements include</strong>:

<ul>
<li>quotes,</li>
<li>galleries,</li>
<li>cover images,</li>
<li>headings,</li>
<li>lists,</li>
<li>audio,</li>
<li>files,</li>
<li>subheadings,</li>
<li>video.</li>
</ul></li>
</ul>

<div class="sponsors__wide-place"></div>




<h5 id="formatting">Formatting</h5>

<p>As the name suggests, these blocks comprise all of the formatting tools.</p>

<ul>
<li><strong>Table</strong><br />
Adding a table using custom HTML code was a tedious job. With the table block, however, the task is a lot easier. You are able to add and remove rows and columns of a table without coding.</li>
</ul>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4c962ec4-f25c-413b-a93f-a0021db19fef/gutenberg-editor-table-format.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4c962ec4-f25c-413b-a93f-a0021db19fef/gutenberg-editor-table-format.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4c962ec4-f25c-413b-a93f-a0021db19fef/gutenberg-editor-table-format.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4c962ec4-f25c-413b-a93f-a0021db19fef/gutenberg-editor-table-format.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4c962ec4-f25c-413b-a93f-a0021db19fef/gutenberg-editor-table-format.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4c962ec4-f25c-413b-a93f-a0021db19fef/gutenberg-editor-table-format.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4c962ec4-f25c-413b-a93f-a0021db19fef/gutenberg-editor-table-format.jpg"
			sizes="100vw"
			alt="Table Block in Gutenberg"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Table Block in Gutenberg ()
		</figcaption>
	
</figure>


<ul>
<li><strong>Custom HTML</strong><br />
You can use a custom HTML code in Gutenberg. And the nice part is that you can insert your code and see a preview in the block itself.</li>
</ul>

<figure>)</figcaption></figure>

<ul>
<li><strong>Other elements include</strong>:<br />

<ul>
<li>code,</li>
<li>classic,</li>
<li>preformatted,</li>
<li>pull quote,</li>
<li>verse.</li>
</ul></li>
</ul>

<h5 id="layout">Layout</h5>

<p>Use your imagination to create a stunning layout using this block. Each element in this block comes with excellent features.</p>

<ul>
<li><strong>Button</strong><br />
You can add buttons such as &ldquo;Subscribe now&rdquo; and “Buy now” using this block. It has different options, including alignment and font styles. You can also set the background color and shape of the button.</li>
</ul>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/38e979be-78e0-4fea-829f-ce3c9ac9da3f/gutenberg-editor-button-layout.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/38e979be-78e0-4fea-829f-ce3c9ac9da3f/gutenberg-editor-button-layout.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/38e979be-78e0-4fea-829f-ce3c9ac9da3f/gutenberg-editor-button-layout.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/38e979be-78e0-4fea-829f-ce3c9ac9da3f/gutenberg-editor-button-layout.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/38e979be-78e0-4fea-829f-ce3c9ac9da3f/gutenberg-editor-button-layout.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/38e979be-78e0-4fea-829f-ce3c9ac9da3f/gutenberg-editor-button-layout.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/38e979be-78e0-4fea-829f-ce3c9ac9da3f/gutenberg-editor-button-layout.jpg"
			sizes="100vw"
			alt="Button Layout in Gutenberg"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Button Layout in Gutenberg ()
		</figcaption>
	
</figure>


<ul>
<li><strong>Columns (beta)</strong><br />
Creating columns in the code-based editor is time-consuming and laborious. This block allows you to add text columns. You are able to add one to six columns in a single row.</li>
</ul>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/86072526-97af-4f7e-9e12-6f0209b27657/gutenberg-editor-column-layout.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/86072526-97af-4f7e-9e12-6f0209b27657/gutenberg-editor-column-layout.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/86072526-97af-4f7e-9e12-6f0209b27657/gutenberg-editor-column-layout.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/86072526-97af-4f7e-9e12-6f0209b27657/gutenberg-editor-column-layout.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/86072526-97af-4f7e-9e12-6f0209b27657/gutenberg-editor-column-layout.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/86072526-97af-4f7e-9e12-6f0209b27657/gutenberg-editor-column-layout.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/86072526-97af-4f7e-9e12-6f0209b27657/gutenberg-editor-column-layout.jpg"
			sizes="100vw"
			alt="Column Layout in Gutenberg"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Column Layout in Gutenberg ()
		</figcaption>
	
</figure>


<ul>
<li><strong>Other elements include</strong>:<br />

<ul>
<li>read more,</li>
<li>page break,</li>
<li>separator,</li>
<li>spacer.</li>
</ul></li>
</ul>

<h5 id="widgets">Widgets</h5>

<p>These blocks allow you to add an archive, categories, the latest posts and the latest comments with just a click anywhere on the page. You are also able to adjust these elements without any coding.</p>

<ul>
<li><strong>Latest Post</strong><br />
With this block element, you can show posts in a grid view or list view, organize them in categories, and order them alphabetically or according to publication date. You can also choose to display the publication date.</li>
</ul>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5180c984-286b-428b-8a59-a21a585e091c/gutenberg-editor-latest-posts.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5180c984-286b-428b-8a59-a21a585e091c/gutenberg-editor-latest-posts.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5180c984-286b-428b-8a59-a21a585e091c/gutenberg-editor-latest-posts.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5180c984-286b-428b-8a59-a21a585e091c/gutenberg-editor-latest-posts.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5180c984-286b-428b-8a59-a21a585e091c/gutenberg-editor-latest-posts.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5180c984-286b-428b-8a59-a21a585e091c/gutenberg-editor-latest-posts.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5180c984-286b-428b-8a59-a21a585e091c/gutenberg-editor-latest-posts.jpg"
			sizes="100vw"
			alt="Latest Posts Setting in Gutenberg"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Latest Posts Setting in Gutenberg ()
		</figcaption>
	
</figure>


<h5 id="embeds">Embeds</h5>

<p>You can easily access any embeds using these blocks. Whether you want to add a YouTube or Twitter link, it’s super-easy and quick. All you need to do is paste the URL in the given blank space, and Gutenberg will embed the code for you. Here is an example of inserting a YouTube link:</p>

<figure>)</figcaption></figure>

<h5 id="reusable-blocks">Reusable Blocks</h5>

<p>Reusable blocks give developers improved usability. You can convert any block into a reusable block so that you can use it in a different location. You can edit the same and save it as a new reusable block again.</p>

<p>You can also see a preview of a reusable block. All reusable blocks are available under the &ldquo;Shared Block&rdquo; options. Most importantly, you can turn one back into a regular block anytime.</p>

<figure>)</figcaption></figure>

<h5 id="most-used">Most Used</h5>

<p>Under this option, you will see the most used blocks, for quick access. Alternatively, you can use the search box to find a block by name.</p>

<h5 id="j-edit-block">J. Edit Block</h5>

<p>To edit any block, open the dropdown menu by clicking in the upper-right corner of the block. You will see different options, including to edit as HTML, duplicate and add to the reusable blocks.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c4eec69a-a4dc-4302-80fb-cdea8f738685/gutenberg-editor-edit-block.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c4eec69a-a4dc-4302-80fb-cdea8f738685/gutenberg-editor-edit-block.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c4eec69a-a4dc-4302-80fb-cdea8f738685/gutenberg-editor-edit-block.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c4eec69a-a4dc-4302-80fb-cdea8f738685/gutenberg-editor-edit-block.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c4eec69a-a4dc-4302-80fb-cdea8f738685/gutenberg-editor-edit-block.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c4eec69a-a4dc-4302-80fb-cdea8f738685/gutenberg-editor-edit-block.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c4eec69a-a4dc-4302-80fb-cdea8f738685/gutenberg-editor-edit-block.jpg"
			sizes="100vw"
			alt="Edit Block in Gutenberg"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Edit Block in Gutenberg ()
		</figcaption>
	
</figure>


<h5 id="k-insert-blocks">K. Insert Blocks</h5>

<p>Using this feature, you can insert a new block anytime. When you bring your mouse over a block, you will see a plus icon (+). Click it to insert a new block.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/57bc414e-1993-47e5-96c5-bcd6374f3e1f/gutenberg-editor-insert-block.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/57bc414e-1993-47e5-96c5-bcd6374f3e1f/gutenberg-editor-insert-block.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/57bc414e-1993-47e5-96c5-bcd6374f3e1f/gutenberg-editor-insert-block.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/57bc414e-1993-47e5-96c5-bcd6374f3e1f/gutenberg-editor-insert-block.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/57bc414e-1993-47e5-96c5-bcd6374f3e1f/gutenberg-editor-insert-block.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/57bc414e-1993-47e5-96c5-bcd6374f3e1f/gutenberg-editor-insert-block.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/57bc414e-1993-47e5-96c5-bcd6374f3e1f/gutenberg-editor-insert-block.jpg"
			sizes="100vw"
			alt="Insert Block in Gutenberg"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Inserting a block in Gutenberg ()
		</figcaption>
	
</figure>


<h5 id="l-slash-autocomplete">L. Slash Autocomplete</h5>

<p>The Slash Autocomplete feature is available in Gutenberg 1.1.0 and later versions. Chances are you are already familiar with the similar feature in Slack. It was added to reduce the amount of pointing and clicking required to create new blocks.</p>

<p>When you open a new block, just press <kbd>/</kbd> (slash key) on your keyboard to select any of the autocomplete options. It works in the default paragraph block only, but it might become a part of other types of blocks in the future.</p>

<figure>)</figcaption></figure>

<h5 id="m-move-blocks">M. Move Blocks</h5>

<p>Gutenberg enables you to move each block up and down. You can use the arrows (on the left side of each block) to move them vertically.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/571acb8a-0066-4214-aa10-fc156108bd24/gutenberg-editor-move-block.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/571acb8a-0066-4214-aa10-fc156108bd24/gutenberg-editor-move-block.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/571acb8a-0066-4214-aa10-fc156108bd24/gutenberg-editor-move-block.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/571acb8a-0066-4214-aa10-fc156108bd24/gutenberg-editor-move-block.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/571acb8a-0066-4214-aa10-fc156108bd24/gutenberg-editor-move-block.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/571acb8a-0066-4214-aa10-fc156108bd24/gutenberg-editor-move-block.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/571acb8a-0066-4214-aa10-fc156108bd24/gutenberg-editor-move-block.jpg"
			sizes="100vw"
			alt="Move Block in Gutenberg"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Moving a block in Gutenberg ()
		</figcaption>
	
</figure>


<h3 id="6-gutenberg-pros-and-cons-a-name-pros-and-cons-a">6. Gutenberg Pros And Cons </h3>

<h4 id="pros">Pros</h4>

<ul>
<li>No technical skill is required to make a custom layout for a blog post or website. It works like , so people looking for that kind of style and user-friendly editing experience will love it.</li>
<li>It allows you to create a consistent and advanced design without relying much on .</li>
<li>Furthermore, blocks are an excellent concept. They allow non-developers to intuitively craft complex layouts. If you are new to WordPress or have no knowledge of it whatsoever, you are still going to love it.</li>
<li>The Gutenberg editor itself works well on mobile (it’s responsive). Unlike its predecessor, it allows you to make quick edits on the go. In fact, mobile-savvy developers can manage to do more than just a few quick edits.</li>
<li>The increased screen space is proving to be a less distracting user experience for many developers.</li>
<li>Hardcore developers can still create customized reusable blocks using HTML5. So, it seems like a win-win for both geeks and non-technical users.</li>
</ul>

<h4 id="cons">Cons</h4>

<ul>
<li>For the time being, there is no Markdown support in the beta version of the WordPress editor.</li>
<li>It still doesn’t support responsive columns. You will need to do some custom coding to make this feature responsive. So, using this feature on mobile isn’t an option right now.</li>
<li>The design layout options are inadequate at the moment.</li>
<li>Compatibility issues could be a significant concern for some WordPress users.</li>
<li>You get only partial support for meta boxes. For now, it only supports Yoast SEO. So, using most custom plugins in Gutenberg is not possible. However, developers are working hard to extend meta box support.</li>
<li> is going to be a primary concern for most developers. It will destroy current plugins and themes, especially ones that require integration with TinyMCE.</li>
</ul>

<div class="sponsors__wide-place"></div>




<h3 id="7-understanding-compatibility-issues-a-name-understanding-compatibility-issues-a">7. Understanding Compatibility Issues </h3>

<p>Despite its simplicity and agility, Gutenberg might not be everyone’s cup of tea. Most WordPress developers might find it difficult to work with, especially in the beginning. They will need to retrain their reflexes to get used to the new UX.</p>

<ul>
<li>Owing to the backward-compatibility issue, you will need to update many plugins and themes to ensure they are fully compatible with the new editor.</li>
<li>For the time being, blocks are more focused on content. As a result, Gutenberg lacks precision and control over the layout of custom websites.</li>
<li>Shortcodes are replaced by shortcode blocks. However, you will still be able to add shortcodes from the widget block.</li>
<li>Meta boxes will be available under a new name and a new UI. Conflicting meta boxes are likely to lead to the classic editor, instead of Gutenberg, with an alert. While this system might prove helpful, some meta boxes will not be supported in Gutenberg.</li>
<li>Custom post types are supported and remain backward-compatible in Gutenberg.</li>
<li>You won’t be able to turn off Gutenberg once it is integrated in WordPress core. However, you can disable it using the  anytime.</li>
</ul>

<h3 id="8-gutenberg-is-the-future-a-name-gutenberg-is-the-future-a">8. Gutenberg Is The Future </h3>

<p>Contrary to popular opinion, Gutenberg is not a replacement for the current text editor. It is a new way to build websites. I like to think of it as Facebook for WordPress.</p>

<p>You don’t need to be a computer geek to publish things on Facebook or any other social media platform. Gutenberg is just a way to bring this simplicity and flexibility to WordPress, so that people don’t need to code in order to create and publish websites. That’s why I think it is going to be the future, not only for WordPress, but for the web in general.</p>

<p>Granted, Gutenberg has a long way to go. People (including me) have had issues with its implementation, but soon we will have Gutenberg-ready themes, plugins and tools surfacing everywhere. Nevertheless, you have to start somewhere. So, you might as well be a part of this change from the beginning.</p>

<h3 id="9-latest-news-and-further-resources-a-name-latest-news-and-further-resources-a">9. Latest News And Further Resources </h3>

<p>If you are interested in riding the Gutenberg train from the beginning, here are a few links to find the latest buzz. Keep in mind that none of these websites are officially endorsed by WordPress.</p>

<ul>
<li></li>
<li></li>
<li></li>
</ul>

<p>For official updates and news, you can try the following:</p>

<ul>
<li>“,” Matías Ventura Bausero</li>
<li>“,” Matías Ventura Bausero, WordPress.org</li>
<li>“,” WordPress.org</li>
<li>“,” Dennis Snell</li>
<li>“,” Jeffrey Paul</li>
<li>“,” WordPress.org</li>
</ul>

<h3 id="wrapping-up">Wrapping Up</h3>

<p>Whether you like it or not, Gutenberg is coming to WordPress 5.0. Do try to be a part of the ongoing discussion about it on the web. It will certainly help. In fact, while you’re at it, try to speed up the development process with your skills. Meanwhile, let me know if this post has shed some light on the topic. Drop your queries and suggestions in the comments section. I would love to keep the conversation going.</p>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(ra, il)</span>
</div>


              </article>
            </body>
          </html>
---------------
<h1 id="#title_2" >3、文章： 想要高效上传下载？试试去中心化的Docker镜像仓库设计</h1>
yangjunsss
[http://www.infoq.com/cn/articles/decentralized-docker-image-registry?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/decentralized-docker-image-registry?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/decentralized-docker-image-registry/zh/smallimage/logo-1526022783167-1534063196099.jpeg"/><p>Docker作为轻量级容器技术解决应用容器化已经为广大用户使用，涵盖了应用的编译、打包、部署、测试等整个周期。镜像为运行Docker容器提供了基础和重要的前提，Docker Registry提供了一个存储、分发、管理Docker镜像的仓库服务，在某些场景下，如跨国部署场景，要求镜像仓库服务提供更高效的上传下载，同时降低复杂度和具备服务高可用。本文设计了一种镜像仓库服务的去中心化的新思路。</p> <i>By yangjunsss</i>
---------------
<h1 id="#title_3" >4、文章： 敏捷：反思的实践和应用</h1>
John Yorke
[http://www.infoq.com/cn/articles/agile-reflective-practice?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/agile-reflective-practice?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/agile-reflective-practice/zh/smallimage/agile-reflective-practice-logo-1533075201973-1534008560260.jpeg"/><p>我们将探讨成功的软件开发是如何基于以下三个相互交织的思维过程：系统思考、群体和反思实践。大多数不成功的敏捷转型是由于团队成员未能意识到，他们是在为更大的系统做贡献，或者不愿意学习如何改进，或者意识不到软件开发其实是一项团队活动。</p> <i>By John Yorke</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_4" >5、文章： 都去炒AI和大数据了，落地的事儿谁来做？</h1>
杨雷
[http://www.infoq.com/cn/articles/how-do-we-fail-data-product?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/how-do-we-fail-data-product?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/how-do-we-fail-data-product/zh/smallimage/GettyImages-518897996-copy-1534062533838.jpeg"/><p>几乎每个企业都期望建立自己的完善的合体的数据体系，但成功的例子并不多。本文希望用一些实践阐述以下几个观点： - 数据产品应该朴实无华 - 浮躁的认知会有大麻烦 - 如何正确认识自己，如何敏捷</p> <i>By 杨雷</i>
---------------
<h1 id="#title_5" >6、全球区块链生态技术大会日程揭底</h1>
田宁宁
[http://www.infoq.com/cn/news/2018/08/bccon-schedule?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/08/bccon-schedule?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>InfoQ主办的BCCon2018全球区块链生态技术大会将于8月18日在北京国际会议中心开幕，大会集结了BAT、华为、京东、小米、360、迅雷等大厂的区块链实践经验，受到业内广泛关注。究竟内容是怎样设置的呢？今天小编带大家一探究竟。</p> <i>By 田宁宁</i>
---------------
<h1 id="#title_6" >7、VMware的云管理之道</h1>
张蝉
[http://www.infoq.com/cn/news/2018/08/vmware-cloud-dev?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/08/vmware-cloud-dev?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>本文介绍VMware的云管理之道。</p> <i>By 张蝉</i>
---------------
<h1 id="#title_7" >8、不挡脸，放肆看！B站黑科技蒙版弹幕揭秘</h1>
陈思
[http://www.infoq.com/cn/news/2018/08/bili-bili-mask-barrage?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/08/bili-bili-mask-barrage?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>不久前，B 站发布一条官方消息，为了更好的提升用户体验，B 站推出一种“不挡脸”的黑科技弹幕，名曰：弹幕蒙版。虽然目前只在几个分区内试用，但是在体验之后，小编表示：真的很好用啊！于是，我们专门采访到了 B 站负责黑科技弹幕的产品小哥，请他来为我们揭秘这神奇弹幕背后的故事。</p> <i>By 陈思</i>
---------------
<h1 id="#title_8" >9、专访王连诚：让新技术在银行领域落地，打造经典区块链产业案例</h1>
前哨小兵甲
[http://www.infoq.com/cn/news/2018/08/exclusive-interview-blockchain?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/08/exclusive-interview-blockchain?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>区块链分布式账本具有去中心化的可信机制，和信息透明和不可篡改的特点，被金融业寄予厚望。 长期以来银行间的国内信用证业务都是采用传统的信开和邮寄交单方式，并需要同时发送SWIFT加押电进行确认，客户也无法了解银行处理进度。同时银行也缺乏足够的手段来核实业务的贸易背景真实性。通过区块链技术可以将信息安全可靠地整合在一个平台，能够使所有交易参与者实现互赢。 2016年开始，民生银行总行信息科技部区块链实验室主管王连诚带领团队，开始在区块链领域进行金融场景的探索，基于Fabric架构进行深度定制开发出面向商业银行联盟的Baas平台，并在其上构建出首个贸易金融领域产品：国内信用证信息传输系(Blockchain based Letter of Credit System , 简称BCLC)。</p> <i>By 前哨小兵甲</i>
---------------