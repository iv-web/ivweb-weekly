## 文章索引
1、 <a href="#1pattern-library-first:-an-approach-for-managing-css" >Pattern Library First: An Approach For Managing CSS</a><br/>
2、 <a href="#2fex-技术周刊---2018/07/09" >FEX 技术周刊 - 2018/07/09</a><br/>
3、 <a href="#3文章-华为快应用引擎技术架构详解" >文章： 华为快应用引擎技术架构详解</a><br/>
4、 <a href="#4文章-猫量子位和远距传动令人匪夷所思的量子计算世界第一部分" >文章： 猫、量子位和远距传动：令人匪夷所思的量子计算世界（第一部分）</a><br/>
5、 <a href="#5视频演讲-如何在小程序上增加音视频功能" >视频演讲： 如何在小程序上增加音视频功能</a><br/>
6、 <a href="#6spark-the-change大会闪亮颠覆" >Spark the Change大会：闪亮颠覆</a><br/>
7、 <a href="#7electric-cloud推出用于devops的预测分析平台" >Electric Cloud推出用于DevOps的预测分析平台</a><br/>
8、 <a href="#8在瑞士最大银行驱动创新" >在瑞士最大银行驱动创新</a><br/>
9、 <a href="#9专访wyre聂尔区块链在工业界的应用是病态的" >专访Wyre聂尔：区块链在工业界的应用是“病态”的！</a><br/><h1 id="#title_0" >1、Pattern Library First: An Approach For Managing CSS</h1>
Rachel Andrew
[https://www.smashingmagazine.com/2018/07/pattern-library-first-css/](https://www.smashingmagazine.com/2018/07/pattern-library-first-css/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/07/pattern-library-first-css/" />
              <title>Pattern Library First: An Approach For Managing CSS</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>Pattern Library First: An Approach For Managing CSS</h1>
                  
                    
                    <address>Rachel Andrew</address>
                  
                  <time datetime="2018-07-09T14:00:35&#43;02:00" class="op-published">2018-07-09T14:00:35+02:00</time>
                  <time datetime="2018-07-09T16:08:32&#43;00:00" class="op-modified">2018-07-09T16:08:32+00:00</time>
                </header>
                <p>In this article, based on the talk that I gave at Smashing Conference in Toronto, I’m going to describe a method of working that I’ve adopted over the past two years that helps me to manage CSS across my projects.</p>

<p>I’ll be showing you how to use the pattern library tool , to manage your CSS on a component by component basis, while allowing you to use the tools you are already familiar with. While this serves as an introduction to Fractal, and why we have selected this particular pattern library, it is likely this way of working would transfer to other solutions. </p>

<h4>Our Projects</h4>

<p>My company has a couple of products &mdash; Perch and Perch Runway CMS and Notist, a software as a service application for public speakers. These products are quite different, especially given that Perch is a self-hosted system and Notist is SaaS, however, they both have a lot of user interface to develop. We also have all of the associated websites and documentation for these products, plus other things that we work on such as the 24 Ways website. After discovering Fractal two years ago, we have moved every new project &mdash; large and small &mdash; into Fractal.</p>

<h4>Problems we wanted to solve</h4>

<p>I began investigating pattern library solutions two years ago when I started work rebuilding the Perch UI for version 3. A feature of Perch is that the templates you create for the output of content on your website become the schema of the admin UI. This means that any fieldtype used in a template needs to be able to exist alongside any other fieldtype. We don’t know how our customers might combine these, and there are a huge number of possible combinations. It's also not a "website", and I didn't want to try and force the pattern library into something designed for organizing website patterns.</p>

<p>As Perch is self-hosted &mdash; people download it and host it on their own servers &mdash; we need to use the simplest tech stack possible in order to not place any additional barriers to entry in front of people, many of who are new to using a CMS. To add an extra level of fun, we support back to Internet Explorer 9, yet I intended to use a lot of Flexbox &mdash; as this was before Grid Layout shipped.</p>



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




<p>I was also keen to avoid using tools which came with a lot of relearning how we worked, and completely changing our process. Any additional tool or change to the way that you work on your projects brings with it new friction. You can solve one problem, but bring in a whole new set of problems if you make large changes to the way that you work. In our case, we were using Sass in a fairly limited way, and processing that using Gulp. None of our projects use a Javascript framework, we’re just writing HTML, CSS and JavaScript.</p>

<p>Fractal fit our needs perfectly. It is agnostic as to the way you develop or the tools you want to use. Importantly for our purposes, it didn’t assume we were building a website. The experiment was so successful that we found ourselves using Fractal for every project large or small, as it makes the process of working on CSS far more straightforward. Even small sites I create on my own often start life in Fractal, because there are more benefits than you might think in terms of working with a pattern library, and many of those benefits make as much sense for a team of one as a large team.</p>

<p>Before we think about how to develop using Fractal and why I think it makes sense for small projects as well as large ones, let’s take a look at how to get the environment set up.</p>

<h4>Getting Started With Fractal</h4>

<p>The most straightforward approach for working with Fractal is to go to the Fractal website and take a look at the . You will first need to install Fractal globally, you can then follow the steps listed here to create a new Fractal project.</p>

<p>With your new project installed, at the command line change into the folder you have just created and run the command:</p>

<pre><code class="language-bash">fractal start --sync</code></code></pre>

<p>This will start up a little server at port 3000, so you should be able to go to <code>http://localhost:3000</code> in a web browser and see your project.</p>

<p>Now that your project is up and running, open up the project folder in your favorite text editor and find the example component under <code>components/example</code>. You will find a config file and a file named <em>example.hbs</em>. The <em>example.hbs</em> template is the HTML of your component, you can add some more HTML to that and Fractal will automatically reload and display it. Change the file to:</p>

<pre><code class="language-html">&#x3C;h1&#x3E;This is my heading&#x3C;/h1&#x3E;
&#x3C;p&#x3E;{{ text }}&#x3C;/p&#x3E;</code></pre>

<p>You should see the heading appear in the browser. The config file can be used to add content and otherwise configure your component. If you want to read your heading text out of that file then edit that file to look like the following example:</p>

<pre><code class="language-html">title: Example component
context:
    text: This is an example component!
    heading: My heading</code></pre>

<p>Now change your <em>example.hbs</em> file to read in that text.</p>

<pre><code class="language-html">&#x3C;h1&#x3E;{{ heading }}&#x3C;/h1&#x3E;
&#x3C;p&#x3E;{{ text }}&#x3C;/p&#x3E;</code></pre>

<h5>Adding Additional Components</h5>

<p>You can follow the pattern of the example component to add your own. At a minimum, you need a folder (the name of the component) and a <em>.hbs</em> file using the same name. You can add the config file if you want to set configuration options.</p>

<p>Components can be nested into folders to make it easier to locate particular components, and how you structure the folders is completely up to you.</p>

<p><strong>Note</strong>: <em>It is really easy to find yourself spending a lot of time worrying about how to name your components. In Fractal at least, renaming and also reorganizing components into folders is straightforward. You can rename or move them and Fractal will update to show the new structure. I find that often the ideal structure only becomes apparent as I’m developing so I don’t worry too much at the outset and then firm it up later.</em></p>

<h4>Adding a CSS Workflow</h4>

<p>So far, we are able to create HTML components as handlebars templates, and a config file to insert data, however, we haven’t added any CSS. Ideally, we want to add the CSS for each component into the same folder as the rest of the component files and then combine it all together.</p>

<p>I mentioned that Fractal makes very few assumptions about your workflow; due to this, it does far less out of the box than it might if it were forcing you down a particular way of working. However, we can fairly easily get Fractal working with a Gulp setup.</p>

<h5>Combining Fractal, Sass, And Gulp</h5>

<p>The following describes a minimal setup using Gulp and Sass to create a single output CSS file. Hopefully, you can follow this process to do anything else that you would normally do in Gulp. The key thing to note is that most of this is not Fractal specific, so once you get the Fractal part working you can add in anything else following the same patterns. If you are familiar with another build tool then it is likely that you could create a similar process; if you do, and are happy to share, let us know in the comments.</p>

<p>First some setup, the following will enable you to follow along with the code listed in this tutorial, the locations of your Sass files and output CSS might ultimately be different to mine. The key thing is that the output CSS file needs to be somewhere in the public folder.</p>

<ol>
    <li>Inside the <em>public</em> folder in your Fractal install, add a folder named <em>css</em>.</li>
    <li>In the root folder of your Fractal, install add a folder <em>assets</em> inside which is a folder <em>scss</em>. Create a Sass file named <em>global.scss</em> inside that folder. Inside that file add the following line:<br/>
    <pre><code class="language-html">@import &quot;../../components/**/*.scss&quot;;</code></pre>
  </li>
    <li>Create a file named <em>example.scss</em> in your <code>example</code> component directory.</li>
    <li>Create <em>gulpfile.js</em> in the root of your Fractal project and add the below code.</li>
</ol>

<pre><code class="language-javascript">'use strict';

const gulp         = require('gulp');
const fractal      = require('./fractal.js');
const logger       = fractal.cli.console;
const sass         = require('gulp-sass');
const sassGlob     = require('gulp-sass-glob');
const plumber      = require('gulp-plumber');
const notify       = require('gulp-notify');
const path         = require('path');

gulp.task('sass',function() {
    return gulp.src('assets/scss/**/*.scss')
    .pipe(customPlumber('Error running Sass'))
    .pipe(sassGlob())
    .pipe(sass())
    .pipe(gulp.dest('public/css'))
});

gulp.task('watch', ['sass'], function() {
   gulp.watch([
        'components/**/*.scss',
        'assets/scss/**/*.scss'
        ], ['sass']);
});

function customPlumber(errTitle) {
    return plumber({
        errorHandler: notify.onError({
            title: errTitle || "Error running Gulp",
            message: "Error: <%= error.message %>",
        })
    });
}

gulp.task('fractal:start', function(){
    const server = fractal.web.server({
        sync: true
    });
    server.on('error', err => logger.error(err.message));
    return server.start().then(() => {
        logger.success(`Fractal server is now running at ${server.url}`);
    });
});

gulp.task('default', ['fractal:start', 'sass', 'watch']);</code></pre>

<p>I then install the dependencies listed at the top of the file. If you were to install those at the command line you would run:</p>

<p><code>npm install gulp gulp-sass gulp-sass-glob gulp-plumber gulp-notify</code></p>

<p>The <code>sass</code> function compiles the Sass from assets into a single file, and outputs it into the folder in <code>public</code>.</p>

<pre><code class="language-javascript">gulp.task(&#39;sass&#39;,function() {
return gulp.src(&#39;src/assets/scss/**/*.scss&#39;)
.pipe(customPlumber(&#39;Error running Sass&#39;))
.pipe(sassGlob())
.pipe(sass())
.pipe(gulp.dest(&#39;public/css&#39;))
});
</code></pre>

<p>I then create a <code>watch</code> function that will watch my Sass in <code>assets</code> and also that in individual components and compile it into the folder in public.</p>

<pre><code class="language-javascript">gulp.task(&#39;watch&#39;, [&#39;sass&#39;], function() {
   gulp.watch([
&#39;components/**/*.scss&#39;,
&#39;assets/scss/**/*.scss&#39;
], [&#39;sass&#39;]);
});
</code></pre>

<p>That’s my CSS building. I now want to make it so that I can run gulp and it will kick off the watching of the CSS file as well as starting fractal. I do this by creating a gulp task to run the fractal start command.</p>

<pre><code class="language-javascript">gulp.task(&#39;fractal:start&#39;, function(){
const server = fractal.web.server({
sync: true
});
server.on(&#39;error&#39;, err =&gt; logger.error(err.message));
return server.start().then(() =&gt; {
logger.success(Fractal server is now running at ${server.url});
});
});</code></pre>

<p>Finally, I need to ensure that the Sass building and Fractal start run when I run gulp and the command line:</p>

<p><code class="language-javascript">gulp.task(&#39;default&#39;, &#39;fractal:start&#39;, &#39;sass&#39;, &#39;watch&#39;);</code></p>

<p>That’s my completed <em>gulpfile.js</em>. If you add this into your default Fractal project, make sure the folders are in place for the paths mentioned. You should be able to go to the command line, run <code>gulp</code>, and Fractal will start.</p>











<figure class="article__image break-out">
	
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/30f5f567-218a-4813-9ccd-dfffbadbcfb7/cli.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/30f5f567-218a-4813-9ccd-dfffbadbcfb7/cli.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/30f5f567-218a-4813-9ccd-dfffbadbcfb7/cli.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/30f5f567-218a-4813-9ccd-dfffbadbcfb7/cli.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/30f5f567-218a-4813-9ccd-dfffbadbcfb7/cli.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/30f5f567-218a-4813-9ccd-dfffbadbcfb7/cli.png"
			sizes="100vw"
			alt="Commandline output"
		/>
	

	
		<figcaption class="op-vertical-bottom">
			Starting Fractal with gulp ()
		</figcaption>
	
</figure>


<p>We can test out our Sass by adding a variable in the <em>global.scss</em> file; you will need to add this above the line that includes the components so that the variable is available for those components.</p>

<pre><code class="language-css">$color1: rebeccapurple;</code></pre>

<p>Then in <code>example.scss</code> add a rule for the level 1 heading we added earlier:</p>

<pre><code class="language-css">h1 {
  color: $color1;
}</code></pre>

<p>If everything is set up correctly, you should find you have a <em>.css</em> file in public/css which contains the rule:</p>

<pre><code class="language-css">h1 {
  color: rebeccapurple;
}</code></pre>

<p>We need to do one more thing so that we can preview our components using the CSS we are building. We need to create a preview file, which will link in the stylesheet from the public folder. </p>

<p>Inside your components folder, create a file named <em>_preview.hbs</em>.</p>

<p>The preview file is essentially an HTML document, linking in our CSS and anything else you need to include. In the body is a tag <code>{{ yield }}</code>, and this is where a component will be placed.</p>

<pre><code class="language-html">&#x3C;!doctype html&#x3E;
&#x3C;html lang=&#x22;en&#x22;&#x3E;
&#x3C;head&#x3E;
&#x9;&#x3C;meta charset=&#x22;utf-8&#x22; /&#x3E;
&#x9;&#x3C;title&#x3E;Preview Layout&#x3C;/title&#x3E;
&#x9;&#x3C;meta name=&#x22;viewport&#x22; content=&#x22;width=device-width, initial-scale=1, shrink-to-fit=no&#x22;&#x3E;
&#x9;&#x3C;link rel=&#x22;stylesheet&#x22; href=&#x22;{{ path &#x27;/css/global.css&#x27; }}&#x22;&#x3E;
&#x3C;/head&#x3E;
&#x3C;body&#x3E;
&#x9;{{{ yield }}}
&#x3C;/body&#x3E;
&#x3C;/html&#x3E;</code></pre>

<p><strong>Note</strong>: <em>The public folder can also house any other assets that you need to display in components such as images, fonts and so on.</em></p>

<h5>The Pattern Library As Source Of Truth</h5>

<p>As we have seen, Fractal can build our CSS. In our projects, we make it so that Fractal is the <em>only</em> place we build and process CSS and other assets for the site. What this means is that our pattern library and site or application do not drift. Drift happens after you deploy the site if people start editing the CSS of the site and not bringing those changes back to the pattern library. If you can make the pattern library the place where CSS is processed then changes have to start there &mdash; which prevents drift between the live site and library.</p>

<p>We build everything in Fractal and then copy those public assets over to the live sites to be deployed. In addition to preventing drift between the systems, it also makes managing CSS in source control much easier. When multiple people work on one CSS file, merge conflicts can be reasonably hard to deal with. With people working on individual components in the pattern library, you can usually avoid two people committing changes to the same file at once, and if they do it is only a small file to sort out and not all of your CSS.</p>

<div class="sponsors__wide-place"></div>




<h3>Using A Pattern Library First Approach For Managing Fallbacks</h3>

<p>I have found that working pattern library first makes dealing with fallbacks in your code far more straightforward and less overwhelming than attempting to fix up a complete site or application at once. It also allows us to concentrate on the best possible case, and be creative with new techniques, rather than limit what we do due to being worried about how we will get it to work well in non-supporting browsers.</p>

<p>We can look at a simple case of a media object component to see how that might work. To follow along, create a <em>media</em> folder inside components in Fractal, and add the files <em>media.hbs</em> and <em>media.scss</em>.</p>

<h5>Start With Good Markup</h5>

<p>Your starting point should always be well-structured markup. In the pattern library, it may be that you will use this component with a range of markup, for example, you could use a component with content marked up as a figure in one place and just with divs in another. Your content should, however, be structured in a way that makes sense and can be read from top to bottom.</p>

<p>This ensures that your content is accessible at a very basic level, but it also means you can take advantage of normal flow. Normal Flow is how browsers display your content by default, with block elements progressing one after the other in the block dimension and inline elements &mdash; such as words in a sentence &mdash; running along the inline axis. For a lot of content that is exactly what you want, and by taking advantage of normal flow rather than fighting against it you make your job far easier as you create your layout.</p>

<p>Therefore, my component has the following markup which I add to <em>media.hbs</em>.</p>

<pre><code class="language-html">&#x3C;div class=&#x22;media&#x22;&#x3E;

  &#x3C;div class=&#x22;img&#x22;&#x3E;
    &#x3C;img src=&#x22;/img/placeholder.jpg&#x22; alt=&#x22;Placeholder&#x22;&#x3E;
  &#x3C;/div&#x3E;
  &#x3C;h2 class=&#x22;title&#x22;&#x3E;This is my title&#x3C;/h2&#x3E;
  &#x3C;div class=&#x22;content&#x22;&#x3E;
      &#x3C;p&#x3E;Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis vehicula vitae ligula sit amet maximus. Nunc auctor neque ipsum, ac porttitor elit lobortis ac. Vivamus ultrices sodales tellus et aliquam. Pellentesque porta sit amet nulla vitae luctus. Praesent quis risus id dolor venenatis condimentum.&#x3C;/p&#x3E;
  &#x3C;/div&#x3E;
  &#x3C;div class=&#x22;footer&#x22;&#x3E;
    An optional footer goes here.
  &#x3C;/div&#x3E;
&#x3C;/div&#x3E;</code></pre>

<p>You can see how this then displays inside Fractal.</p>











<figure class="article__image break-out">
	
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bb40e309-8190-48c4-ab26-83d7bb641ca8/component-markedup.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bb40e309-8190-48c4-ab26-83d7bb641ca8/component-markedup.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bb40e309-8190-48c4-ab26-83d7bb641ca8/component-markedup.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bb40e309-8190-48c4-ab26-83d7bb641ca8/component-markedup.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bb40e309-8190-48c4-ab26-83d7bb641ca8/component-markedup.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bb40e309-8190-48c4-ab26-83d7bb641ca8/component-markedup.png"
			sizes="100vw"
			alt="The fractal UI with the added component"
		/>
	

	
		<figcaption class="op-vertical-bottom">
			My component after adding the markup. ()
		</figcaption>
	
</figure>


<p>Once I’ve got the markup that I want, I am going to work on the desktop display that I have in mind. I’m going to use CSS Grid Layout and the <code>grid-template-areas</code> method of doing so. Add the following to <em>media.scss</em>.</p>

<pre><code class="language-css">img { max-width: 100%; }

.media &gt; .title { 
  grid-area: title; 
}

.media &gt; .img { 
  grid-area: img; 
}

.media &gt; .content { 
  grid-area: bd; 
}

.media &gt; .footer { 
  grid-area: ft; 
}

.media {
  margin-bottom: 2em;
  display: grid;
  grid-column-gap: 20px;
  grid-template-columns: 200px 3fr;
  grid-template-areas:
    &quot;img title&quot;
    &quot;img bd&quot;
    &quot;img ft&quot;;
  }</code></pre>

<p>We now have a simple media object layout:</p>











<figure class="article__image break-out">
	
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/40d6ffb9-61a3-4715-ac63-7a65a466e926/component-layout.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/40d6ffb9-61a3-4715-ac63-7a65a466e926/component-layout.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/40d6ffb9-61a3-4715-ac63-7a65a466e926/component-layout.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/40d6ffb9-61a3-4715-ac63-7a65a466e926/component-layout.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/40d6ffb9-61a3-4715-ac63-7a65a466e926/component-layout.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/40d6ffb9-61a3-4715-ac63-7a65a466e926/component-layout.png"
			sizes="100vw"
			alt="A two column layout, image on the left text on the right"
		/>
	

	
		<figcaption class="op-vertical-bottom">
			The Media Object layout. ()
		</figcaption>
	
</figure>


<p>Something you can do in Fractal is to add variations of a component. You might want to flip the media object so that the image is on the right.</p>

<p>Now add the CSS to <em>media.scss</em> in order to flip the layout:</p>

<pre><code class="language-css">.media.media-flip {
grid-template-columns: 3fr 200px ;
grid-template-areas:
  &quot;title img&quot;
  &quot;bd img&quot;
  &quot;ft img&quot;;
  }
</code></pre>

<p>There are two ways to create variants: file-based and configuration based. File-based is simplest and is also useful if your variant has different markup. To create a file-based variant, make a copy of your component in the media folder with the name media <em>--flip.hbs</em> (that’s two dashes in the filename).</p>

<p>This component should have identical markup with the class <code>media-flip</code> added to the first line, and you will then be able to see both versions.</p>

<pre><code>&lt;div class=&quot;media media-flip&quot;&gt;</code></pre>











<figure class="article__image break-out">
	
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4498b4db-aec4-4fa9-ae93-d8f3d8253729/component-flipped.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4498b4db-aec4-4fa9-ae93-d8f3d8253729/component-flipped.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4498b4db-aec4-4fa9-ae93-d8f3d8253729/component-flipped.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4498b4db-aec4-4fa9-ae93-d8f3d8253729/component-flipped.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4498b4db-aec4-4fa9-ae93-d8f3d8253729/component-flipped.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4498b4db-aec4-4fa9-ae93-d8f3d8253729/component-flipped.png"
			sizes="100vw"
			alt="A two column layout, image on the right text on the left"
		/>
	

	
		<figcaption class="op-vertical-bottom">
			The flipped version. ()
		</figcaption>
	
</figure>


<p>Alternately, as in this case all we need to do is add a class, you can create a variant using a config file.</p>

<p>If you want to do this, remove your variant file, and instead add a config file named <em>media.config.json</em> containing the following code:</p>

<pre><code class="language-javascript">{
    &quot;title&quot;: &quot;Media Object&quot;,
    &quot;context&quot;: {
        &quot;modifier&quot;: &quot;default&quot;
    },
    &quot;variants&quot;: [
        {
            &quot;name&quot;: &quot;Flipped&quot;,
            &quot;context&quot;: {
                &quot;modifier&quot;: &quot;flip&quot;
            }
        }
    ]
}
</code></pre>

<p>Then modify the first line of <em>media.hbs</em> as follows:</p>

<p><code class="language-html">&lt;div class=&quot;media media-{{ modifier }}&quot;&gt;</code></p>

<p><strong>Note</strong>: <em>You can add as many variants as you like (take a look at the  to read more).</em></p>

<p>We might now think about adding some CSS to change the layout based on screen size. Wrapping the layout we have created in a media query and above that creating a single column layout for smaller devices.</p>

<pre><code class="language-css">img {
  max-width: 100%;
}

.media &gt; .title { 
  grid-area: title; 
}

.media &gt; .img { 
  grid-area: img; 
}

.media &gt; .content { 
  grid-area: bd; 
}

.media &gt; .footer { 
  grid-area: ft; 
}

.media {
  display: grid;
  grid-column-gap: 20px;
  grid-template-areas:
    &quot;title&quot;
    &quot;img&quot;
    &quot;bd&quot;
    &quot;ft&quot;;
  }
  
  @media (min-width: 600px) {
    .media {
      margin-bottom: 2em;
      display: grid;
      grid-column-gap: 20px;
      grid-template-columns: 200px 3fr;
      grid-template-areas:
        &quot;img title&quot;
        &quot;img bd&quot;
        &quot;img ft&quot;;
    }

    .media.media-flip {
      grid-template-columns: 3fr 200px ;
      grid-template-areas:
        &quot;title img&quot;
        &quot;bd img&quot;
        &quot;ft img&quot;;
    }
}</code></pre>











<figure class="article__image break-out">
	
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1d1eb900-b706-448f-bf69-5ebd5e3ae81b/component-narrow.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1d1eb900-b706-448f-bf69-5ebd5e3ae81b/component-narrow.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1d1eb900-b706-448f-bf69-5ebd5e3ae81b/component-narrow.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1d1eb900-b706-448f-bf69-5ebd5e3ae81b/component-narrow.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1d1eb900-b706-448f-bf69-5ebd5e3ae81b/component-narrow.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1d1eb900-b706-448f-bf69-5ebd5e3ae81b/component-narrow.png"
			sizes="100vw"
			alt="A single column layout"
		/>
	

	
		<figcaption class="op-vertical-bottom">
			The object for mobile devices. ()
		</figcaption>
	
</figure>


<p>Then, just as we manage the view for smaller devices within our component, we can manage the layout for older browsers which do not support grid.</p>

<p>In this case, I’m going to build a float-based fallback (this will work for pretty much any legacy browser). I’m only going to worry about it for wider screen sizes and leave the component displaying in normal flow for older mobile devices.</p>

<p>Just inside the media query, add the following CSS:</p>

<pre><code class="language-css">.media:after {
  content: &quot;&quot;;
  display: table;
  clear: both;
}

.media &gt; .media {
  margin-left: 160px;
  clear: both;
}

.media .img {
  float: left;
  margin: 0 10px 0 0;
  width: 150px;
}

.media.media-flip .img {
  float: right;
  margin: 0 0 0 10px;
}

.media &gt; * {
  margin: 0 0 0 160px;
}

.media.media-flip &gt; * {
  margin: 0 160px 0 0;
}</code></pre>

<p>This should sort out the display in non-grid browsers. For browsers that do support grid, you don’t need to worry about floats, i.e. when the floated item becomes a grid item, the float is removed. What will be a problem are any margins. The layout in grid supporting browsers will now be all spaced out due to the extra margins.</p>











<figure class="article__image break-out">
	
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6c5b1cbe-b879-4c6e-bace-839efd3a7a29/component-gaps.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6c5b1cbe-b879-4c6e-bace-839efd3a7a29/component-gaps.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6c5b1cbe-b879-4c6e-bace-839efd3a7a29/component-gaps.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6c5b1cbe-b879-4c6e-bace-839efd3a7a29/component-gaps.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6c5b1cbe-b879-4c6e-bace-839efd3a7a29/component-gaps.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6c5b1cbe-b879-4c6e-bace-839efd3a7a29/component-gaps.png"
			sizes="100vw"
			alt="Two column layout with big gaps"
		/>
	

	
		<figcaption class="op-vertical-bottom">
			The layout is spaced out due to the extra margins. ()
		</figcaption>
	
</figure>


<p>This is where we can add a feature query, removing the margins if we know that our browser supports grid.</p>

<pre><code class="language-css">@supports(display: grid) {
  .media &gt; *,
  .media.media-flip &gt; * {
    margin: 0;
  }

  .media .img,
  .media.media-flip .img {
    width: auto;
    margin: 0;
  }
  
  .media:after {
    content: none;
  }
}</code></pre>

<p>That’s our small component finished. While a simple example &mdash; and it might be argued that it’s one which doesn’t really need grid at all if you <em>need</em> to have a fallback &mdash; it demonstrates the approach I’m taking across all of my projects, large and small.</p>

<p>To get my CSS file into production, we can take the CSS file from the public folder and add that to our production site. You could even script this process to copy it over to your site folder as it builds.</p>

<h5>Reduced Test Case First Development</h5>

<p>Something I have discovered as a key benefit in working this way, is that it really does make the browser support piece of the puzzle easier. Not only is it easier to see what fallback CSS is being included with this component, but also if we are having problems with a browser, it makes it far easier to debug them.</p>

<p>When you are battling with a browser issue then the thing you will generally be told to do is create a . Reduce the problem down to the smallest thing that exhibits the issue. A component in a pattern library is often very close to that reduced test case already. Certainly far closer than if you are trying to debug a problem while looking at your entire website.</p>

<p>In addition to making browser debugging easier, having your fallbacks included alongside the rest of the CSS makes it easier to remove the fallback code once it is no longer needed, it’s obvious this fallback code is for this component. I know that removing it won’t change the way anything else displays.</p>

<p>This ease of organizing our code is really why Fractal makes sense even in small projects. Given that we tend to use Gulp and Sass anyway (even on smaller projects), adding Fractal to the mix isn't a big overhead. We don't need to see it as only for our bigger projects, as even a small site might have a reasonable amount of CSS.</p>

<h3>See The Code</h3>

<p>I've created a  which has all of the code mentioned in the article. I would suggest setting up Fractal as described in the article and then grabbing any bits - such as the gulpfile or preview layout, from my repository.</p>

<p>As an additional reference and to see some published Fractal projects, we have the published version of the ), which you can take a look at. These are good examples of a non-website pattern library, and a more traditional one used for a site.</p>

<h3>How Do <em>You</em> Manage CSS?</h3>

<p>I really like this way of working; it allows me to write CSS in a straightforward, progressively enhanced way. Depending on the project, we may include far more tooling and processing of files. Or, I may be building a simple site in which case the setup will be pretty much as we have seen in this article &mdash; with some light processing of Sass. The fact that Fractal means we can have the same process for sites big and small, for web applications or websites. It means we can always work in a familiar way. </p>

<p>This works for us, and I hope this article might give you some things to experiment with. However, I would love to know the ways in which you and your team have approached managing CSS in your projects and the strengths and weaknesses of the approaches you have tried. I’d be especially interested in hearing from anyone who has developed a similar process using another pattern library solution. Add your experiences in the comments.</p>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(il)</span>
</div>


              </article>
            </body>
          </html>
---------------
<h1 id="#title_1" >2、FEX 技术周刊 - 2018/07/09</h1>

[http://fex.baidu.com/blog/2018/07/fex-weekly-09//](http://fex.baidu.com/blog/2018/07/fex-weekly-09//)
作者：zhangzhao <br> <h2 id="section">业界会议</h2>

<p><strong>2018百度AI开发者大会</strong><br />
http://create.baidu.com/<br />
人类历史上有太多里程碑式的创新，源起于微不足道的梦想，最终成长为改变世界的力量。而在这个AI时代，每一个梦想都更有机会成为现实，每一位开发者的创新与现实仅有一步之遥。2018年夏天，百度诚邀全球开发者，发现改变世界的力量，让我们一起 Create More。</p>

<p><strong>ArchSummit2018-深圳站</strong><br />
https://sz2018.archsummit.com/<br />
ArchSummit聚焦业界强大的技术成果，秉承“实践第一、案例为主”的原则，展示先进技术在行业中的最佳实践，以及技术在企业转型、发展中的推动作用。旨在帮助技术管理者、CTO、架构师做好技术选型、技术团队组建与管理，并确立技术对于产品和业务的关键作用。</p>

<h2 id="section-1">深阅读</h2>

<p><strong>Web Components in 2018</strong><br />
https://www.sitepen.com/blog/2018/07/06/web-components-in-2018/<br />
Adoption and hype around Web Components have been extended and undulating. That said, as the Web Component specifications gain better adoption, the need for polyfills should gradually dissolve, keeping them leaner and faster for users. The Shadow DOM allows developers to write simple, scoped CSS which is arguably easier to manage and generally better for performance. Custom Elements give a unified methodology for defining components that can (in theory) get used across codebases and teams.</p>

<p><strong>Vue.js: the good, the meh, and the ugly</strong><br />
https://medium.com/@Pier/vue-js-the-good-the-meh-and-the-ugly-82800bbe6684<br />
Moving from React to Vue, two years later. Picking up new frameworks and libraries is exciting but also stressful. Even after some evaluation you never really know what skeletons you’re going to find out down the road. My honeymoon period is long over. After about 2 years of using Vue almost daily I can finally write about it with some perspective. 另附：.</p>

<p><strong>What Is Redux: A Designer’s Guide</strong><br />
https://www.smashingmagazine.com/2018/07/redux-designers-guide/<br />
Do you know Redux’s real power is beyond managing the state? Do you want to design with an understanding of how Redux works in mind? Let’s dig deeper into what Redux can do, why it does its things, what the downsides are, and how it relates to design.</p>

<p><strong>React Native: A retrospective from the mobile-engineering team at Udacity</strong><br />
https://engineering.udacity.com/react-native-a-retrospective-from-the-mobile-engineering-team-at-udacity-89975d6a8102<br />
The mobile team here at Udacity recently removed the last features in our apps that were written with React Native. We’ve received numerous questions regarding our usage or React Native and why we’ve stopped investing in it. In this post, I hope to answer the majority of the questions we’ve received and give insight into: What is the size &amp; makeup of our particular team? Why did we try React Native in the first place? What was the reason for removing it? What worked? What didn’t? 另附：.</p>

<p><strong>前端遇上Go: 静态资源增量更新的新实践</strong><br />
https://tech.meituan.com/fe-and-golang.html<br />
美团金融的业务在过去的一段时间里发展非常快速。在业务增长的同时，我们也注意到，很多用户的支付环境，其实是在弱网环境中的。大家知道，前端能够服务用户的前提是 JavaScript 和 CSS 等静态资源能够正确加载。如果网络环境恶劣，那么我们的静态资源尺寸越大，用户下载失败的概率就越高。根据我们的数据统计，我们的业务中有2%的用户流失与资源加载有关。因此每次更新的代价越小、加载成功率越高，用户流失率也就会越低，从而就能够变相提高订单的转化率。</p>

<p><strong>实施前端微服务化的六七种方式</strong><br />
https://mp.weixin.qq.com/s?__biz=MjM5Mjg4NDMwMA==&amp;mid=2652975949&amp;idx=1&amp;sn=c36387188283dd4fae52257357541729<br />
是一种类似于微服务的架构，它将微服务的理念应用于浏览器端，即将 Web 应用由单一的单体应用转变为多个小型前端应用聚合为一的应用。由此带来的变化是，这些前端应 用可以独立运行、独立开发、独立部署。以及，它们应该可以在共享组件的同时进行并行开发——这些组件可以通过 NPM 或者 Git Tag、Git Submodule 来管理。</p>

<p><strong>科普文：服务器上如何 Node 多版本共存</strong><br />
https://yuque.com/egg/nodejs/node-multi-versioning<br />
很多公司的服务器环境没有做隔离，就是全局安装一个 Node.js Runtime，一般很少升级。nvs / nvm 等可以用来切换版本，但无法同时共存。而且一般服务器不允许你随意升级。因此很多同学都会很痛苦：「都 8012 年了，还是 Node 4.x 甚至 0.x 简直想死！」时至今天，最好的办法就是 Docker。但奈何很多小公司还处于水深火热之中。本文将介绍下我们很早前就使用的一套方案，可以完美解决非 Docker 情况下 Node 多版本共存问题。</p>

<p><strong>W3C重点报告发布，综述2018年发展路线图</strong><br />
https://mp.weixin.qq.com/s/o0EnLmcCX1FvjIe3NbutJA<br />
这份报告整合了W3C近期工作亮点，综述了W3C对现有工作的优化、改进、创新、孵化、研究，以及2018年的发展路线图。W3C在实现对技术和功能的再次核心创新的同时，不断对Web进行扩展以迎接新的机遇和挑战。诸多领域的重大进展都展现着W3C与Web社区的巨大活力。我们可以看到Web新技术的不断成熟和进一步发展。</p>

<p><strong>华为快应用引擎技术架构详解</strong><br />
https://mp.weixin.qq.com/s/JdNJifhpkGzd0VpLZhN6Eg<br />
快应用是一种基于手机硬件平台的新型应用形态，无需安装，即点即用，又兼具原生应用体验（性能、系统整合、交互等）。同时，快应用在诞生之初就在开发规范、能力接入、开发者服务等层面实现了手机厂商间的标准化统一，极大地降低开发者的适配成本。</p>

<p><strong>Get Better Type Checking in JavaScript with the Maybe Type</strong><br />
https://blog.bitsrc.io/get-better-type-checking-in-javascript-with-the-maybe-type-e7f70b23b505<br />
Maybe type is a popular abstraction for defining values that may or may not exist. It encapsulates the type checking and guards our code against any error or bugs caused by the missing values. In this post, I will show how to use Maybe and keep your app readable and maintainable. Let’s dive in.</p>

<p><strong>Pointer events with React — The why, how, what?</strong><br />
https://medium.com/@wesharehoodies/pointer-events-with-react-the-why-how-what-617a5b51dbb2<br />
Back in the good old days we only had a mouse and listening for events was simple. The web content assumed the user’s pointing device will be a mouse. Nowadays we have many devices which don’t correlate to having a mouse, like phones with touch surface or pens. How can we listen for events if the user doesn’t have a mouse?</p>

<p><strong>Resilient, Declarative, Contextual</strong><br />
https://keithjgrant.com/posts/2018/06/resilient-declarative-contextual/<br />
Today I want to take a different tack. I want to look at three key characteristics of CSS that set it apart from conventional programming languages: it’s resilient; it’s declarative; and it’s contextual. Understanding these aspects of the language, I think, is key to becoming proficient in CSS.</p>

<p><strong>Clearfix: A Lesson in Web Development Evolution</strong><br />
https://css-tricks.com/clearfix-a-lesson-in-web-development-evolution/<br />
The web community has, for the most part, been a spectacularly open place. As such, a lot of the best development techniques happen right out in the open, on blogs and in forums, evolving as they’re passed around and improved. I thought it might be fun (and fascinating) to actually follow this creative exchange all the way through. To take a look at a popular CSS trick, the clearfix, and find out exactly how a web design technique comes to be.</p>

<p><strong>Building a Snipping Tool with Electron, React and Node.js</strong><br />
https://quantizd.com/building-a-snipping-tool-with-electron-react-and-node-js/<br />
In this tutorial, I’ll show how to build a snipping tool using  desktopCapturer module. We’ll use React for building our application’s user interface and Nodejs as a backend server for uploading snipped images.</p>

<p><strong>A Real-World WebAssembly Benchmark</strong><br />
https://pspdfkit.com/blog/2018/a-real-world-webassembly-benchmark/<br />
Rendering PDF documents is a complex task: The format is 25 years old and has many edge cases. It wouldn’t be feasible for us to rewrite the equivalent of 500,000 lines of C++ code to JavaScript, but technologies such as WebAssembly and asm.js allow us to use the same codebase in a browser, delivering a consistent level of high-fidelity rendering and parsing of PDF documents everywhere. Performance of the WebAssembly code has been a focus for us since day one, and it’s amazing to see the entire industry move toward a shared goal: making WebAssembly fast. This starts with optimizing WebAssembly startup time, compiler improvements, and continuous browser upgrades.</p>

<p><strong>How to drop 10 million packets per second</strong><br />
https://blog.cloudflare.com/how-to-drop-10-million-packets/<br />
Internally our DDoS mitigation team is sometimes called “the packet droppers”. When other teams build exciting products to do smart things with the traffic that passes through our network, we take joy in discovering novel ways of discarding it. Being able to quickly discard packets is very important to withstand DDoS attacks. Dropping packets hitting our servers, as simple as it sounds, can be done on multiple layers. Each technique has its advantages and limitations. In this blog post we’ll review all the techniques we tried thus far.</p>

<p><strong>A one size fits all database doesn’t fit anyone</strong><br />
https://www.allthingsdistributed.com/2018/06/purpose-built-databases-in-aws.html<br />
A common question that I get is why do we offer so many database products? The answer for me is simple: Developers want their applications to be well architected and scale effectively. To do this, they need to be able to use multiple databases and data models within the same application.</p>

<p><strong>The Not-So-Dark Art Of Designing Database Indexes: Reflections From An Average Software Engineer</strong><br />
https://www.bennadel.com/blog/3467-the-not-so-dark-art-of-designing-database-indexes-reflections-from-an-average-software-engineer.htm<br />
What I eventually came to realize, after years of impostor syndrome, was that database index design is simply not that mysterious: If you need to access data quickly, you index it. If the performance of data access isn’t a concern, you don’t index it. That’s 90-percent of what you need to know about database indexing</p>

<p><strong>Rules of optimization</strong><br />
http://www.humus.name/index.php?page=News&amp;ID=383<br />
Basically Programming Wisdom (which btw often is a great sources for actual programming wisdom) posted a quote that basically suggested more or less that there’s never a good time to think about performance. Even experts should defer it until later! This is way worse advice than your usual “premature optimization is the root of all evil” tirade. The premature optimization at least addresses something that can be a bit of a problem, i.e. that programmers go ahead and obfuscate code in order to make it faster, without even looking at whether the code had any performance problem to begin with or verifying that the new code actually is any faster, and in the process of doing this introducing bugs and reducing readability.</p>

<p><strong>Timsort — the fastest sorting algorithm you’ve never heard of</strong><br />
https://hackernoon.com/timsort-the-fastest-sorting-algorithm-youve-never-heard-of-36b28417f399<br />
Timsort: A very fast , O(n log n), stable sorting algorithm built for the real world — not constructed in academia.</p>

<p><strong>Kubernetes 1.11: a look from inside Google</strong><br />
https://cloudplatform.googleblog.com/2018/07/kubernetes-1-11-a-look-from-inside-Google.html<br />
With the release of 1.11, let’s take a look at the core Kubernetes work that Google is driving, as well as some of the innovation we’ve built on Kubernetes’ foundations in the last three months.</p>

<p><strong>Democratizing APIs with Natural Language Interfaces</strong><br />
https://www.microsoft.com/en-us/research/blog/democratizing-apis-with-natural-language-interfaces/<br />
We have been studying natural language interfaces to APIs (NL2APIs). Different from general-purpose NLIs like virtual assistants, we examined how to build NLIs for individual web APIs, for example, the API to a calendar service. Such NL2APIs have the potential to democratize APIs by helping users communicate with software systems. They can also address the scalability issue of general-purpose virtual assistants by allowing for distributed development.</p>

<h2 id="section-2">新鲜货</h2>

<p><strong>Announcing npm.community</strong><br />
https://blog.npmjs.org/post/175587538995/announcing-npmcommunity<br />
I am pleased to announce that npm is transitioning its public issue trackers from GitHub to a Discourse site at npm.community. This will allow us to give the community a single place to report bugs that impact npm, regardless if they’re on the website, in the command line tool or in the registry itself.</p>

<p><strong>Let’s celebrate Hugo’s 5th birthday</strong><br />
https://gohugo.io/news/lets-celebrate-hugos-5th-birthday/<br />
How a side project became one of the most popular frameworks for building websites.</p>

<p><strong>Office UI Fabric</strong><br />
https://developer.microsoft.com/en-us/fabric<br />
The official front-end framework for building experiences that fit seamlessly into Office and Office 365.</p>

<p><strong>Rogue</strong><br />
https://github.com/alidcastano/rogue<br />
SSR for React that’s invisible (zero configuration!) and quick (no Webpack!)</p>

<p><strong>React From Zero</strong><br />
https://github.com/kay-is/react-from-zero<br />
A simple (99% ES2015 less) tutorial for React. Everything runs in the browser without a manual pre-compilation. 另附：.</p>

<p><strong>Rete.js</strong><br />
https://github.com/retejs/rete<br />
Rete is a modular framework for visual programming. Rete allows you to create node-based editor directly in the browser. You can define nodes and workers that allow users to create instructions for processing data in your editor without a single line of code.</p>

<p><strong>pdfshift</strong><br />
https://pdfshift.io/?tab=javascript<br />
Convert HTML to PDF online with PDFShift’s lightning-fast and powerful API</p>

<p><strong>LayoutIt!</strong><br />
https://www.layoutit.com/grid<br />
CSS Grid Layout Interface Builder</p>

<p><strong>WebSub</strong><br />
https://www.w3.org/TR/websub/#abstract<br />
WebSub provides a common mechanism for communication between publishers of any kind of Web content and their subscribers, based on HTTP web hooks. Subscription requests are relayed through hubs, which validate and verify the request. Hubs then distribute new and updated content to subscribers when it becomes available. WebSub was previously known as PubSubHubbub.</p>

<p><strong>GoAccess - Visual Web Log Analyzer</strong><br />
https://goaccess.io/<br />
GoAccess is an open source real-time web log analyzer and interactive viewer that runs in a terminal in *nix systems or through your browser. It provides fast and valuable HTTP statistics for system administrators that require a visual server report on the fly.</p>

<p><strong>youtube-dl</strong><br />
https://github.com/rg3/youtube-dl<br />
Command-line program to download videos from YouTube.com and other video sites.</p>

<p><strong>GCFS - A FUSE file system based on Google Drive</strong><br />
https://github.com/harababurel/gcsf<br />
GCSF is a virtual filesystem that allows users to mount their Google Drive account locally and interact with it as a regular disk partition. You can find out more in this paper.</p>

<p><strong>Language Graph</strong><br />
https://akr.am/languages/<br />
A graph of programming languages connected through compilers. This project shows a graph where the nodes are programming languages and the edges are compilers. The graph is drawn using Cytoscape.js, particularly the CoSE layout module.The data for the list of compilers is sourced from the compilers.js module.</p>

<p><strong>termtosvg</strong><br />
https://github.com/nbedos/termtosvg<br />
A Linux terminal recorder written in Python that renders your command line sessions as standalone SVG animations.</p>

<h2 id="section-3">设计</h2>

<p><strong>Timeline 2.0 — Interaction Design for Sketch</strong><br />
https://medium.com/sketch-app-sources/timeline-2-0-interaction-design-for-sketch-f6fc0a852c8a<br />
Design Interactions and Export Code, Directly in Sketch.</p>

<p><strong>“MVP vs. MDP” and the winner is…</strong><br />
https://uxdesign.cc/mvp-vs-mdp-and-the-winner-is-a754ba0ce55f<br />
MDP - Stands for Minimum Desirable Product or someone even says Minimum Delightful Product.MVP - Stands for Minimum Viable Product.</p>

<p><strong>Order Out of Chaos: Patterns of Organization for Writing on the Job</strong><br />
http://alistapart.com/article/order-out-of-chaos-patterns-of-organization-for-writing-on-the-job<br />
Given the endless variety of writing situations, there is no such thing as a single organization solution. But saying that “advice varies widely depending on the situation” doesn’t tell the whole story. There are flexible patterns and principles that can guide you in finding, customizing, and creating structures for your goals. The key thing to remember is that structure affects meaning. The sequence of information, the categories you use, the emphasis you imply through your hierarchy—all of these decisions impact how well your audience understands what you write. Your ideal structure should therefore reinforce what you mean to say.</p>

<p><strong>Design Principles That Help You Shape The Best User Experience</strong><br />
https://blog.marvelapp.com/design-principles-help-shape-best-user-experience/<br />
Every product has an ultimate goal — to help people solve certain problems. When designing a product, you need to keep user experience in mind, you don’t want to create a product that is more complicated than the actual problem the users have. There are some principles to follow when designing a product. It could be an app, a website or a physical product. These principles would help you shape better user experience.</p>

<p><strong>Better Research, Better Design, Better Results</strong><br />
https://www.smashingmagazine.com/2018/07/better-research-design-results/<br />
Most web professionals like to see their influence felt in web design projects as early as possible, in order to make sure what they have to say gets heard. Yet often SEOs and content marketers are asked to step in post-launch when the design work is more or less complete. However, there are very real benefits, ranging from better UX to lower costs to using SEO-focused data such as keyword research as a springboard for design and development, rather than having to turn to it further down the line.</p>

<p><strong>Mobile App Design Best Practices and Mistakes</strong><br />
https://www.toptal.com/designers/mobile/mobile-app-design-mistakes<br />
The most common mistakes span from failing to maintain consistency throughout the lifespan of an app to difficulty attracting users in the first place. It’s challenging to design an app with intuitive simplicity without it becoming repetitive and boring. An app has to offer pleasing design and UX details without losing sight of a greater purpose. Most apps live and die in the first few days, so following some basic mobile app design best practices and avoiding the most common mistakes will help designers create apps that live past that 90-day mark.</p>

<p><strong>Dribbble’s Sarah Kuehnle - Community is everything</strong><br />
https://www.invisionapp.com/blog/dribbble-design-chat/<br />
In case you haven’t noticed, we at InVision are huge Dribbble fans. The invite-only social platform for designers launched in 2009 and has since become the best place to share illustrations, animations, wireframes, photography, and other creative work.</p>

<h2 id="section-4">产品及其它</h2>

<p><strong>EU copyright law</strong><br />
https://juliareda.eu/eu-copyright-reform/<br />
</p>

<p><strong>Tim Berners-Lee’s Solid is a platform designed to re-decentralize the web</strong><br />
https://www.vanityfair.com/news/2018/07/the-man-who-created-the-world-wide-web-has-some-regrets<br />
The idea is simple: re-decentralize the Web. Working with a small team of developers, he spends most of his time now on , a platform designed to give individuals, rather than corporations, control of their own data. “There are people working in the lab trying to imagine how the Web could be different. How society on the Web could look different. What could happen if we give people privacy and we give people control of their data,” Berners-Lee told me. “We are building a whole eco-system.”</p>

<p><strong>Founder to CEO</strong><br />
https://docs.google.com/document/d/1ZJZbv4J6FZ8Dnb0JuMhJxTnwl-dwqx5xl0s65DE3wO8/edit#<br />
I coach tech startup CEOs (and tech investors) in Silicon Valley,  most of whom are young technical founders. They include the CEOs of Coinbase, ClearBit, AngelList, CoinList, TrustToken, Bolt, Shogun, Speechify, etc.  In my coaching, I found several things: Becoming a great CEO requires training;  For a founding CEO, there is precious little time to get that training, especially if her company is succeeding; While there are many books out there with excellent and relevant knowledge for the founding CEO, there is no single book that is a compendium of all the things she needs to learn; My mentees and I repeatedly solve the same core issues together. In this book, I have simply written down the solutions that we came up with. And hopefully it will serve as a compendium so that you can become a great CEO in the very little time you have to do so.</p>

<p><strong>知乎：成则得到，败则贴吧</strong><br />
https://mp.weixin.qq.com/s?__biz=MzI2NTY4MDg1NA==&amp;mid=2247492644&amp;idx=1&amp;sn=06cc0eaf762f4faed07e876eb667af66<br />
作为中国最大的知识分享社区，知乎从10年创业以来，一直受到大家的关注。但是，虽然有良好的社区氛围，知乎的商业化之路却一直十分坎坷，无论是知乎live，还是读书会，包括最近的超级会员，似乎都没有达到预期效果，反而频频受到用户的质疑。知乎的商业化之路为何如此困难，它的前路又在哪里？今天，我想站在一个旁观者的角度，来试着聊这样几个问题：为什么知乎要积极的探索商业化？知乎的商业化变现的难点在哪里？超级会员究竟应该会走向何方？</p>

<p>– THE END –</p>
---------------
<h1 id="#title_2" >3、文章： 华为快应用引擎技术架构详解</h1>
华为快应用引擎技术架构详解
[http://www.infoq.com/cn/articles/huawei-quickapp-engine-architecture?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/huawei-quickapp-engine-architecture?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/huawei-quickapp-engine-architecture/zh/smallimage/Istio-Future-of-Service-Meshes-1529065924373-1530985692015.jpeg"/><p>2018年3月华为与小米，Oppo，Vivo等9家手机厂商，联合发布快应用联盟标准。快应用是一种基于手机硬件平台的新型应用形态，无需安装，即点即用，又兼具原生应用体验（性能、系统整合、交互等）。同时，快应用在诞生之初就在开发规范、能力接入、开发者服务等层面实现了手机厂商间的标准化统一，极大的降低开发者的适配成本。</p> <i>By 华为快应用引擎技术架构详解</i>
---------------
<h1 id="#title_3" >4、文章： 猫、量子位和远距传动：令人匪夷所思的量子计算世界（第一部分）</h1>
Holly Cummins
[http://www.infoq.com/cn/articles/quantum-computing-intro-one?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/quantum-computing-intro-one?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/quantum-computing-intro-one/zh/smallimage/logo-cats-1530093171385-1530982363443.jpg"/><p>当我们大多数人进入成年时，都知道一些基本事实。猫不能同时既是活的又是死的。宇宙两级的物体不能互相影响。计算机基于0和1运行，这是最基本的信息单位。然后，量子计算却是以这些真理有一部分是错误的作为前提。</p> <i>By Holly Cummins</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_4" >5、视频演讲： 如何在小程序上增加音视频功能</h1>
常青
[http://www.infoq.com/cn/presentations/how-to-add-audio-and-video-functions-for-small-program?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/how-to-add-audio-and-video-functions-for-small-program?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/presentations/how-to-add-audio-and-video-functions-for-small-program/zh/mediumimage/changqing270-1531063305496.jpg"/><p>这段时间小程序的热度可谓如日中天，由于获客成本的优势和轻量级体验来带的便利，很多公司都在纷纷将自己主战场从APP转向小程序。但是音视频能力一直以来都是小程序上的一个短板，2017年 Q4, 腾讯视频云终端团队与微信团队通力合作，将腾讯视频云的技术积累以SDK的形式落地到了微信版本上，从而为小程序增加了直播和实时音视频能力。本次演讲的主要提纲如下：小程序音视频的应用前景，同 WebRTC 的区别和互通，内部原理解析，如何在小程序上快速增加音视频功能，未来走向。</p> <i>By 常青</i>
---------------
<h1 id="#title_5" >6、Spark the Change大会：闪亮颠覆</h1>
Ben Linders
[http://www.infoq.com/cn/news/2018/07/spark-paris-sparkling-disruption?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/spark-paris-sparkling-disruption?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>让人们可以在任何地方生活和工作的新交通系统，让人们可以通过App分享故事获得改变企业的思路的人脉关系，让这个世界上每个地方的人都可以联系起来的不受空间限制的高速互联网，这些就是Spark the Change大会上谈及的闪亮颠覆。</p> <i>By Ben Linders</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_6" >7、Electric Cloud推出用于DevOps的预测分析平台</h1>
Helen Beal
[http://www.infoq.com/cn/news/2018/07/electric-cloud-predictive-devops?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/electric-cloud-predictive-devops?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>ElectricFlow DevOps Foresight使用深度学习来识别发布管道中的模式，评估软件发布成功的可能性，并提出建议以逐步提高管道性能和应用程序质量。</p> <i>By Helen Beal</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_7" >8、在瑞士最大银行驱动创新</h1>
Manuel Pais
[http://www.infoq.com/cn/news/2018/07/innovation-largest-swiss-bank?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/innovation-largest-swiss-bank?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>瑞银集团（UBS）资产管理SWAT（软件操作团队）负责人Jelena Laketic在伦敦DevOps企业峰会上分享了她在瑞士最大银行驱动创新的一些心得体会。InfoQ采访了Laketic，了解了她在SWAT遇到的挑战以及取得的成果，以及对于UBS来说，创新代表着什么。</p> <i>By Manuel Pais</i> <i> Translated by 刘嘉洋</i>
---------------
<h1 id="#title_8" >9、专访Wyre聂尔：区块链在工业界的应用是“病态”的！</h1>
前哨小兵甲
[http://www.infoq.com/cn/news/2018/07/blockchain-industry-disease?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/blockchain-industry-disease?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>2013 年之前，我们在网上看到的只是一些比特币的信息。现在，关于比特币的讨论已经被撕裂成两面，一边是以收割为目的的币圈乱象，一边是世界范围内的一些大型企业在积极地探索区块链技术。 而在区块链行业摸爬滚打数年的英国人聂尔说了句话：“区块链在工业界的应用，整体来看就是一种病态！并且这种疾病还在蔓延！”</p> <i>By 前哨小兵甲</i>
---------------