## 文章索引
1、 <a href="#1getting-started-with-gutenberg-by-creating-your-own-block" >Getting Started With Gutenberg By Creating Your Own Block</a><br/>
2、 <a href="#2文章-道德规范的心理学透视" >文章： 道德规范的心理学透视</a><br/>
3、 <a href="#3文章-2018年夏加密数字化货币现状上" >文章： 2018年夏加密数字化货币现状（上）</a><br/>
4、 <a href="#4文章-mysql是如何做容器测试的" >文章： MySQL是如何做容器测试的？</a><br/>
5、 <a href="#5迷你书-架构师2018年10月" >迷你书： 架构师（2018年10月）</a><br/>
6、 <a href="#6谷歌发布新版本cloud-source-repositories" >谷歌发布新版本Cloud Source Repositories</a><br/><h1 id="#title_0" >1、Getting Started With Gutenberg By Creating Your Own Block</h1>
Muhammad Muhsin
[https://www.smashingmagazine.com/2018/10/gutenberg-testimonials-sliderblock/](https://www.smashingmagazine.com/2018/10/gutenberg-testimonials-sliderblock/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/10/gutenberg-testimonials-sliderblock/" />
              <title>Getting Started With Gutenberg By Creating Your Own Block</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>Getting Started With Gutenberg By Creating Your Own Block</h1>
                  
                    
                    <address>Muhammad Muhsin</address>
                  
                  <time datetime="2018-10-08T13:50:00&#43;02:00" class="op-published">2018-10-08T13:50:00+02:00</time>
                  <time datetime="2018-10-08T17:14:03&#43;00:00" class="op-modified">2018-10-08T17:14:03+00:00</time>
                </header>
                <p>WordPress is the most popular Content Management System (CMS) by far &mdash;powering more than 30% of the web. It has undergone a huge metamorphosis during its 15 years of existence. Its latest addition is Gutenberg which is to be released in version 5.0.</p>

<p>Named after Johannes Gutenberg (the inventor of the printing press), Gutenberg is going to fundamentally change WordPress, further helping reach its goal to democratize publishing.</p>

<p>WordPress usually releases its major features as a plugin to test the waters before baking them into the core. Gutenberg is no exception. In this article, we will learn how to go about building your first Gutenberg block. We will be building a Testimonials Slider Block while dwelling on the basics of Gutenberg.</p>

<p>Here is an outline for this article:</p>

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

<p>This article assumes the following:</p>

<ul>
<li>Some knowledge of WordPress such as how content is saved and basic plugin development;</li>
<li>Basic understanding of React and ES6;</li>
<li>Knowledge of both npm and webpack.</li>
</ul>

<p><strong>Recommended reading</strong>: <em></em></p>



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




<h3 id="installing-the-gutenberg-plugin">Installing The Gutenberg Plugin</h3>

<p>If you are a WordPress user, you will know that installing a plugin is pretty straightforward. Installing  is no exception.</p>

<p>There are two ways to do this:</p>

<ol>
  <li>Click on <strong>Plugins</strong> in your WordPress dashboard and then click <strong>Add New</strong>. Search for “gutenberg” and click on <strong>Install Now</strong>. After installing click on <strong>Activate</strong>.</li>
  <li>Or you can head over to the  and search for “gutenberg”. Click on the first result that appears and download it. Extract the zip file and move the “gutenberg” folder to <code>wp-content/plugins</code>. Go to the <strong>Plugins menu</strong> in the Dashboard and click on <strong>Activate</strong> for the Gutenberg plugin.</li>
</ol>

<p>Now when you go and create a page or a post, you will be able to edit using the Gutenberg Editor.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2cb2844a-8063-49e9-9a74-00deb1a2f538/1-gutenberg-editor-demo.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2cb2844a-8063-49e9-9a74-00deb1a2f538/1-gutenberg-editor-demo.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2cb2844a-8063-49e9-9a74-00deb1a2f538/1-gutenberg-editor-demo.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2cb2844a-8063-49e9-9a74-00deb1a2f538/1-gutenberg-editor-demo.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2cb2844a-8063-49e9-9a74-00deb1a2f538/1-gutenberg-editor-demo.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2cb2844a-8063-49e9-9a74-00deb1a2f538/1-gutenberg-editor-demo.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2cb2844a-8063-49e9-9a74-00deb1a2f538/1-gutenberg-editor-demo.png"
			sizes="100vw"
			alt="Gutenberg Editor Demo"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Gutenberg Editor Demo ()
		</figcaption>
	
</figure>


<p>Since this article is about creating a Gutenberg Block, we will not go into the introduction to the Editor, For a complete understanding of what is Gutenberg and how to use it, please refer to this  on Smashing Magazine.</p>

<h3 id="installing-the-testimonials-slider-block">Installing The Testimonials Slider Block</h3>

<p>The plugin in question &mdash; the one we are going to go through is already published to the WordPress repository.</p>

<p>Please install the  to your local WordPress instance so that you have a feel for how the plugin works.</p>

<p>You can also fork or clone the project from .</p>

<p>After activating the plugin, you can go to your Gutenberg Editor and add a Testimonials Slider to your content:</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3edcd44b-11e2-4456-ab96-100d518fcc4d/2-testimonials-slider-block.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3edcd44b-11e2-4456-ab96-100d518fcc4d/2-testimonials-slider-block.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3edcd44b-11e2-4456-ab96-100d518fcc4d/2-testimonials-slider-block.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3edcd44b-11e2-4456-ab96-100d518fcc4d/2-testimonials-slider-block.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3edcd44b-11e2-4456-ab96-100d518fcc4d/2-testimonials-slider-block.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3edcd44b-11e2-4456-ab96-100d518fcc4d/2-testimonials-slider-block.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3edcd44b-11e2-4456-ab96-100d518fcc4d/2-testimonials-slider-block.png"
			sizes="100vw"
			alt="Testimonials Slider Block"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Selecting the Testimonials Slider Block ()
		</figcaption>
	
</figure>












<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0b98dc03-abe5-4542-bb45-2ac3105af3d9/3-adding-content.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0b98dc03-abe5-4542-bb45-2ac3105af3d9/3-adding-content.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0b98dc03-abe5-4542-bb45-2ac3105af3d9/3-adding-content.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0b98dc03-abe5-4542-bb45-2ac3105af3d9/3-adding-content.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0b98dc03-abe5-4542-bb45-2ac3105af3d9/3-adding-content.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0b98dc03-abe5-4542-bb45-2ac3105af3d9/3-adding-content.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0b98dc03-abe5-4542-bb45-2ac3105af3d9/3-adding-content.jpg"
			sizes="100vw"
			alt="Adding content to the Testimonials Slider Block"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Adding content to the Testimonials Slider Block ()
		</figcaption>
	
</figure>












<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f28c1187-e6d1-422c-9c77-a6e58567d23d/4-front-end.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f28c1187-e6d1-422c-9c77-a6e58567d23d/4-front-end.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f28c1187-e6d1-422c-9c77-a6e58567d23d/4-front-end.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f28c1187-e6d1-422c-9c77-a6e58567d23d/4-front-end.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f28c1187-e6d1-422c-9c77-a6e58567d23d/4-front-end.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f28c1187-e6d1-422c-9c77-a6e58567d23d/4-front-end.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f28c1187-e6d1-422c-9c77-a6e58567d23d/4-front-end.png"
			sizes="100vw"
			alt="Testimonials Slider Block in the frontend"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Testimonials Slider Block in the frontend ()
		</figcaption>
	
</figure>


<p>Now I will go through how I built the plugin and how you too can build a similar one. To keep the article concise, I will not share the entire code in here. However, after reading this you should be able to create your own Gutenberg block.</p>

<h4 id="getting-started-with-the-configuration">Getting Started With The Configuration</h4>

<p>A Gutenberg block is generally created as part of a plugin. Our plugin is not going to be any different.</p>

<p>Navigate to the plugins directory in your local WordPress instance. Move to the <code>testimonials-slider-block</code>. Notice the following files and folders:</p>

<ol>
<li><code>gutenberg-testimonials-slider.php</code> is the main file which has details of the plugin, such as name, description, author details and license. These details will be used in the plugin description in the Plugins menu in the dashboard. You will see that this file calls the init.php file.</li>
<li>The <code>init.php</code> file enqueues the different JavaScript and CSS files. This includes both the external libraries like Bootstrap and Font Awesome and our build files.</li>
<li>The <code>.babelrc</code> file instructs webpack what kind of JavaScript files we are writing.</li>
<li>The <code>package.json</code> file contains all the npm modules that are used in the plugin. You will use the <code>npm install</code> command to install all those packages.</li>
<li><code>webpack.config.js</code> file contains the configuration for webpack to build our JavaScript and CSS. if you did not know,  is a package bundler mainly used for bundling our JavaScript modules and putting them into one file that is then enqueued by WordPress.</li>
</ol>

<p>That was a lot of configuration files. Now we can go about actually building our Gutenberg block.</p>

<div class="sponsors__wide-place"></div>




<h3 id="registering-a-block">Registering A Block</h3>

<p>Within the src folder you will see the <code>index.js</code> file. This is the fle that webpack looks for, to bundle the JavaScript. You can see that this file imports the <code>slider.js</code> file within the block folder.</p>

<p>The block folder has the following styles:</p>

<ul>
<li><code>slider.js</code>: contains the actual code for the block</li>
<li><code>editor.scss</code>: the styles file describing the block within the  Gutenberg Editor</li>
<li><code>style.scss</code>: contains styles pertaining to how the block is displayed in the frontend.</li>
</ul>

<p>Please open the <code>slider.js</code> file in your editor.</p>

<p>This file first imports both the <code>editor</code> and <code>style</code> scss files. Then it imports internationalization component, registerBlockType and the <code>MediaUpload</code> and <code>PlainText</code> components. The last two components will be used to upload the author image and to take in the different text inputs to save in the database.</p>

<p>Next you will see how a block is registered.</p>

<p>It takes in a name as the first parameter. The name must be prefixed with a namespace specific to your plugin in order to avoid any conflicts with another block with the same name.</p>

<p>The second parameter is an array with the following properties and functions:</p>

<ul>
<li><strong>Title</strong><br />The name of the block which will appear when you add a new block in the Gutenberg Editor.</li>
<li><strong>Icon</strong><br />The block’s icon which will be picked up from . You can also specify your own SVG icons if you want to.</li>
<li><strong>Category</strong><br />Under which category of blocks will the block appear. Some of the categories are: common, formatting, layout widgets and embed.</li>
<li><strong>Keywords</strong><br />An array of strings that describe the block, similar to tags.</li>
<li><strong>Attributes</strong><br />A JavaScript object which contains a description of the data that is saved by the block.</li>
<li><strong>Edit</strong><br />The function that provides an interface for the block within the Gutenberg Editor.</li>
<li><strong>Save</strong><br />The function that describes how the block will be rendered in the frontend.</li>
</ul>

<p>To learn more, please refer to this .

<h3 id="introducing-gutenberg-specific-syntax">Introducing Gutenberg Specific Syntax</h3>

<p>Gutenberg is built with React and the blocks that we build for Gutenberg use a similar syntax.</p>

<p>It certainly helps to know a bit of React to build custom Gutenberg blocks though you don’t have to be an expert.</p>

<p>The following things are useful to know before starting the block development:</p>

<ul>
<li>The HTML class is replaced with <code>className</code> like in React.</li>
<li>The edit and save methods return JSX, which stands for JavaScript XML. If you are wondering, JSX is syntax exactly like HTML, except you can use HTML tags and other components like <code>PlainText</code> and <code>RichText</code> within it.</li>
<li>The <code>setAttributes</code> method works similar to React’s <code>setState</code>. What it does is, when you call <code>setAttributes</code> the data in the block is updated and the block within the editor is refreshed.</li>
<li>The block uses <code>props</code> in the edit and <code>save</code> functions, just like React. The <code>props</code> object contains the <code>attributes</code> object, the <code>setAttributes</code> function and a ton of other data.</li>
</ul>

<h3 id="the-attributes-object">The <code>attributes</code> Object</h3>

<p>The attributes object that was mentioned previously define the data within the Gutenberg block. The WordPress Gutenberg Handbook says:</p>

<blockquote>Attribute sources are used to define the strategy by which block attribute values are extracted from saved post content. They provide a mechanism to map from the saved markup to a JavaScript representation of a block.<br /><br />Each source accepts an optional selector as the first argument. If a selector is specified, the source behavior will be run against the corresponding element(s) contained within the block. Otherwise, it will be run against the block’s root node.</blockquote>

<p>For more details on how to use attributes, please refer to .</p>

<p>The following is the attributes object that is used in the Testimonials Slider Block:</p>

<pre><code class="language-css">attributes: {
   id: {
     source: "attribute",
     selector: ".carousel.slide",
     attribute: "id"
   },
   testimonials: {
     source: "query",
     default: [],
     selector: "blockquote.testimonial",
     query: {
       image: {
         source: "attribute",
         selector: "img",
         attribute: "src"
       },
       index: {
         source: "text",
         selector: "span.testimonial-index"
       },
       content: {
         source: "text",
         selector: "span.testimonial-text"
       },
       author: {
         source: "text",
         selector: "span.testimonial-author span"
       },
       link: {
         source: "text",
         selector: ".testimonial-author-link"
       }
     }
   }
 },
</code></pre>

<p>The <code>source</code> tells Gutenberg where to look for data within the markup.</p>

<p>Use <code>attribute</code> to extract the value of an attribute from markup, such as the src from img element. The <code>selector</code> and <code>attribute</code> tell what element to look for and what exact attribute to pick the data from respectively. Notice that the selector string picks up an HTML element from the <code>save</code> function.</p>

<p>Use <code>text</code> to extract the inner text from markup and <code>html</code> to extract the inner HTML from markup.</p>

<p>Use <code>query</code> to extract an array of values from markup. Entries of the array are determined by the <code>selector</code> argument, where each matched element within the block will have an entry structured corresponding to the <code>query</code> argument, an object of <code>attribute</code> and <code>text</code> sources.</p>

<p>You can access the attributes in the <code>edit</code> and <code>save</code> functions through <code>props.attributes</code>.</p>

<p>When you use <code>console.log(props.attributes.testimonials)</code> in the <code>edit</code> function, you get the following result:</p>

<pre class="break-out">
  <code class="language-javascript">▼</code><i><code>(2) [{...}, {...}]</code></i>
  <code class="language-javascript">  ▼0:
      author:"Muhammad"
      content: "This is a testimonial"
      image: "http://localhost/react-gutenberg/wp-content/uploads/2018/08/0.jpg"
      index: 0
      link: "https://twitter.com/muhsinlk"
    ▶__proto__: Object
  ▼1:
    author: "Matt"
    content: "This is another testimonial"
    image: "http://localhost/react-gutenberg/wp-content/uploads/2018/08/767fc115a1b989744c755db47feb60.jpeg"
    index: 1
    link: "https://twitter.com/photomatt"
   ▶__proto__: Object
   length: 2
  ▶__proto__: Array (0)
</code></pre>

<p>Therefore, in the above code, <code>id</code> is a text that uniquely describes each testimonial block whereas testimonials is an array of objects where each object has the properties as shown in the above screenshot.</p>

<div class="sponsors__wide-place"></div>




<h3 id="the edit-and-save-functions">The <code>edit</code> And <code>save</code> Functions</h3>

<p>As mentioned above, these two functions describe how the block is rendered in the editor as well as in the frontend respectively.</p>

<p>Please read the full description .</p>

<h4>The <code>edit</code> Function</h4>

<p>If you look at the <code>edit</code> function, you will notice the following:</p>

<ol>
<li>I first get the <code>props.attributes.testimonials</code> array to a const variable. Notice the ES6 Object Destructuring to set the const value.</li>
<li>Then generate an id for the block which will be used to make each block unique when you add more than one Testimonials Slider Block to your content.</li>
<li>Then the <code>testimonialsList</code> is generated, which is got from sorting then mapping the testimonials array that we got in step 1.</li>
<li>Then, the return function gives out JSX, which we discussed earlier. The <code>testimonialsList</code>, which we constructed in step 3 is rendered. The + button is also rendered, pressing which will create a new testimonial inside the block.</li>
</ol>

<p>If you dig into <code>testimonialsList</code>,  you will see that it contains the <code>PlainText</code> and <code>MediaUpload</code> components. These provide the interface for entering the different texts and uploading the author image respectively.</p>

<p>The <code>PlainText</code> component looks like this:</p>

<pre breakout="true"><code class="language-css">&lt;PlainText
  className="content-plain-text"
  style={{ height: 58 }}
  placeholder="Testimonial Text"
  value={testimonial.content}
  autoFocus
  onChange={content => {
  const newObject = Object.assign({}, testimonial, {
    content: content
  });
  props.setAttributes({
    testimonials: [
      ...testimonials.filter(
        item => item.index != testimonial.index
      ),
      newObject
    ]
    });
  }}
/&gt;
</code></pre>

<p>The attributes I have used for the <code>PlainText</code> component are:</p>

<ul>
<li><code>className</code><br />The CSS class of the component in order to style it.</li>
<li><code>style</code><br />To give a minimum height so that the content does not look like a one-line text. Specifying the height using the class selector did not work.</li>
<li><code>placeholder</code><br />The text that will be displayed when no content is added.</li>
<li><code>value</code><br />The value of the component from the object within the testimonials array.</li>
<li><code>autoFocus</code><br />To tell the browser to focus on this component (input field) as soon as the user adds a new testimonial by clicking the + button.</li>
<li><code>onChange</code><br />What looks like the most complex attribute in this list. This function first gets a copy of the current testimonial and assigns the changed content to newObject. Then it spreads the array of objects, filters out the current object using index and then replaces the newObject within the array. This is set using the the props.setAttributes function to the testimonials array.</li>
</ul>

<h4>The <code>save</code> Function</h4>

<p>This function does the following:</p>

<ol>
<li>I first get the <code>props.attributes.testimonials</code> array and <code>props.attributes.id</code> string to const variables. Again, notice the ES6 Object Destructuring being used to set the values for the two const variables id and testimonials.</li>
<li>Then I create the <code>carouselIndicators</code> variable, which is essentially JSX constructed from the testimonials array.</li>
<li>Then the <code>testimonialsList</code> is created from the testimonials array. The snippet below is from the mapped function callback return.

<pre class="break-out"><code class="language-css">{testimonial.content && (
  &lt;p className="testimonial-text-container"&gt;
    &lt;i className="fa fa-quote-left pull-left" aria-hidden="true" /&gt;
    &lt;span className="testimonial-text">{testimonial.content}&lt;/span&gt;
    &lt;i class="fa fa-quote-right pull-right" aria-hidden="true" /&gt;
  &lt;/p&gt;
)}
</code></pre>

Notice the conditional rendering. The markup will not be rendered for content if the content is not set.</li>
<li>Next, if the testimonials array has objects within it, the HTML is rendered. This is what will be serialized and saved to the database, and this is what will be shown in the frontend (not verbatim).</li>
</ol>

<h3 id="continuing-development">Continuing Development</h3>

<p>I’m sure you want to tinker around this plugin and see what happens. You can continue developing the plugin:</p>

<ol>
<li>Open up the terminal</li>
<li>Navigate to the plugin’s root directory</li>
<li><code>npm install</code></li>
<li><code>npm start</code></li>
</ol>

<p>This will install all the packages, build the files and watch for changes. Every time you make a change to the files, webpack will rebuild the JS and CSS files.</p>

<p><strong>Please note:</strong> Markup changes to the blocks will mess up the block in the Gutenberg Editor if you had added it before. Don’t be alarmed &mdash; you simply have to remove the block and add it again.</p>

<p>If you are done with developing you can <code>npm run build</code> to minify the files to make it ready for production!</p>

<p>Hopefully, you are now convinced Gutenberg block development is more approachable than it sounds.</p>

<p>I have the following plans in mind for this plugin:</p>

<ul>
<li>Allow users to select color of text, background and accent.</li>
<li>Allow users to select the size of slider and font.</li>
<li>Avoid depending on libraries like Bootstrap and Font Awesome.</li>
</ul>

<p>I encourage you  with your improvements and extra features.</p>

<h3 id="conclusion">Conclusion</h3>

<p>We covered the following in today’s article:</p>

<ul>
<li>Installing and using Gutenberg and Testimonials Slider Block plugins</li>
<li>Configuration for a typical Gutenberg block plugin</li>
<li>Registering a Gutenberg block</li>
<li>How to use the attributes object</li>
<li>The <code>edit</code> and <code>save</code> functions and how to use them.</li>
</ul>

<p>I hope this article was useful for you. I can’t wait to see what you will build with and for Gutenberg!</p>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(dm, ra, yk, il)</span>
</div>


              </article>
            </body>
          </html>
---------------
<h1 id="#title_1" >2、文章： 道德规范的心理学透视</h1>
Andrea Dobson
[http://www.infoq.com/cn/articles/ethics-psychological-perspective?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/ethics-psychological-perspective?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/ethics-psychological-perspective/zh/smallimage/ethics-psychological-perspective-s-1537535476773-1538877990742.jpeg"/><p>随着像机器学习这样的新技术的出现，开发人员现在能实现的东西比以往任何时候都多了。但是，这种新力量也有不好的一面。最近，Facebook首席执行官在欧盟议会就未能在虚假新闻、外国干涉选举及开发人员滥用人们的信息中承担起足够的责任而道歉。</p> <i>By Andrea Dobson</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_2" >3、文章： 2018年夏加密数字化货币现状（上）</h1>
Adam Taché
[http://www.infoq.com/cn/articles/state-of-cryptocurrencies-summer-2018-part1?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/state-of-cryptocurrencies-summer-2018-part1?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/state-of-cryptocurrencies-summer-2018-part1/zh/smallimage/how-to-choose-stream-processor-logo-1534706730559-1538879142305.jpeg"/><p>本系列文将全面概述2018年夏季加密货币生态系统的当前状态，主要包括对当前和即将推出的顶级项目的大致介绍和讨论：比特币、比特币现金、Chia、Decred、智能合约平台(以太坊、DFINITY、Cosmos、EOS等)、隐私类数字化货币(Zcash、Monero、Grin/MimbleWimble等)和稳定币(Basis、makerin)。本篇将介绍比特币、比特币现金、Chia、Decred。</p> <i>By Adam Taché</i> <i> Translated by 冬雨</i>
---------------
<h1 id="#title_3" >4、文章： MySQL是如何做容器测试的？</h1>
Robert Neumayer
[http://www.infoq.com/cn/articles/container-testing-for-mysql-server?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/container-testing-for-mysql-server?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/container-testing-for-mysql-server/zh/smallimage/jshell-java-repl-s-1537393177692-1537960835457.jpeg"/><p>在这篇博文中，我们将重点介绍如何使用自动化基础设施测试来验证MySQL Server Docker镜像。我们将比较三个可用于进行容器测试的框架，并给出示例代码。</p> <i>By Robert Neumayer</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_4" >5、迷你书： 架构师（2018年10月）</h1>
InfoQ中文站
[http://www.infoq.com/cn/minibooks/architect-201810?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/minibooks/architect-201810?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/minibooks/architect-201810/zh/smallimage/100-1538279277509.jpg"/><p>本期主要内容：微软开源Sketch2Code，草图秒变代码；Java 11正式发布，新特性解读；秒杀Redis的KVS数据库上云了！伯克利重磅开源Anna 1.0；架构师如何判断技术演进的方向？GitHub：我们为什么会弃用jQuery？</p> <i>By InfoQ中文站</i>
---------------
<h1 id="#title_5" >6、谷歌发布新版本Cloud Source Repositories</h1>
Steef-Jan Wiggers
[http://www.infoq.com/cn/news/2018/10/gcp-cloud-source-repository-beta?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/10/gcp-cloud-source-repository-beta?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>谷歌宣布推出改进过的Cloud Source Repositories和代码搜索功能。经过大幅改进的服务提供了全新的用户界面和语义代码搜索功能。</p> <i>By Steef-Jan Wiggers</i> <i> Translated by 无明</i>
---------------