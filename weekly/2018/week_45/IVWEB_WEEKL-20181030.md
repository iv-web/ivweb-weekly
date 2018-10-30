## 文章索引
1、 <a href="#1the-css-working-group-at-tpac:-whats-new-in-css" >The CSS Working Group At TPAC: What’s New In CSS?</a><br/>
2、 <a href="#2fex-技术周刊---2018/10/29" >FEX 技术周刊 - 2018/10/29</a><br/>
3、 <a href="#3fex-技术周刊---2018/08/20" >FEX 技术周刊 - 2018/08/20</a><br/>
4、 <a href="#4文章-helm三思而后用" >文章： Helm：三思而后用</a><br/>
5、 <a href="#5william-mcknight关于数据平台和创建现代数据架构的见解" >William McKnight关于数据平台和创建现代数据架构的见解</a><br/>
6、 <a href="#6oboe安卓上的低延迟音频应用开发库" >Oboe，安卓上的低延迟音频应用开发库</a><br/>
7、 <a href="#7grpc-web发布rest又要被干掉了" >gRPC-Web发布，REST又要被干掉了？</a><br/>
8、 <a href="#8数据建模nosql数据库的概念和对象建模符号" >数据建模NoSQL数据库的概念和对象建模符号</a><br/><h1 id="#title_0" >1、The CSS Working Group At TPAC: What’s New In CSS?</h1>
Rachel Andrew
[https://www.smashingmagazine.com/2018/10/tpac-css-working-group-new/](https://www.smashingmagazine.com/2018/10/tpac-css-working-group-new/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/10/tpac-css-working-group-new/" />
              <title>The CSS Working Group At TPAC: What’s New In CSS?</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>The CSS Working Group At TPAC: What’s New In CSS?</h1>
                  
                    
                    <address>Rachel Andrew</address>
                  
                  <time datetime="2018-10-26T22:30:30&#43;02:00" class="op-published">2018-10-26T22:30:30+02:00</time>
                  <time datetime="2018-10-29T16:03:22&#43;00:00" class="op-modified">2018-10-29T16:03:22+00:00</time>
                </header>
                

<p>Last week, I attended W3C TPAC as well as the CSS Working Group meeting there. Various changes were made to specifications, and discussions had which I feel are of interest to web designers and developers. In this article, I&rsquo;ll explain a little bit about what happens at TPAC, and show some examples and demos of the things we discussed at TPAC for CSS in particular.</p>

<h3 id="what-is-tpac">What Is TPAC?</h3>

<p>TPAC is the Technical Plenary / Advisory Committee Meetings Week of the W3C. A chance for all of the various working groups that are part of the W3C to get together under one roof. The event is in a different part of the world each year, this year it was held in Lyon, France. At TPAC, Working Groups such as the CSS Working Group have their own meetings, just as we do at other times of the year. However, because we are all in one building, it means that people from other groups can more easily come as observers, and cross-working group interests can be discussed.</p>

<p>Attendees of TPAC are typically members of one or more of the Working Groups, working on W3C technologies. They will either be representatives of a member organization or Invited Experts. As with any other meetings of W3C Working Groups, the minutes of all of the discussions held at TPAC will be openly available, usually as IRC logs scribed during the meetings.</p>

<h3 id="the-css-working-group">The CSS Working Group</h3>

<p>The CSS Working Group meet face-to-face at TPAC and on at least two other occasions during the year; this is in addition to our weekly phone calls. At all of our meetings, the various issues raised on the specifications are discussed, and decisions made. Some issues are kept for face-to-face discussions due to the benefits of being able to have them with the whole group, or just being able to all get around a whiteboard or see a demo on screen.</p>

<p>When an issue is discussed in any meeting (whether face-to-face or teleconference), the relevant GitHub issue is updated with the minutes of the discussion. This means if you have an issue you want to keep track of, you can star it and see when it is updated. The full IRC minutes are also posted to the  mailing list.</p>

<p>Here is a selection of the things we discussed that I think will be of most interest to you.</p>



<aside class="product-panel product-panel__tilted product-panel--book" data-audience="non-subscriber">
    <div class="container product-panel--book__container">
      <div class="panel__description panel__description--book">
    <p>Web forms are such an important part of the web, but we design them poorly all the time. The brand new .</p>
    <a href="https://smashed.by/fdppanel/#toc" class="btn btn--green btn--large">
      Check the table of contents&nbsp;↬
    </a>
      </div>
      <div class="panel__image panel__image--book">
        <a href="https://smashed.by/fdppanel/#toc" class="books__book__image">
        <div class="books__book__img">
          <img src="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/de0c560d-c0e0-4d52-a6b9-02c0028ba10f/form-design-pattners-shop-wo-shadow.png" alt="Form Design Patterns — a practical guide for anyone who needs to design and code web forms" width="310" height="400">
        </div>
      </a>
      </div>
    </div>
  </aside>




<h4 id="css-scrollbars">CSS Scrollbars</h4>

<p>The CSS Scrollbars specification seeks to give a standard way of styling the size and color of scrollbars. If you have Firefox Nightly, you can test it out. To see the examples below, use Firefox Nightly and enable the flags <code>layout.css.scrollbar-width.enabled</code> and <code>layout.css.scrollbar-color.enabled</code> by visiting <code>http://about:config</code> in Firefox Nightly.</p>

<p>The specification gives us two new properties: <code>scrollbar-width</code> and <code>scrollbar-color</code>. The <code>scrollbar-width</code> property can take a value of <code>auto</code>, <code>thin</code>, <code>none</code>, or <code>length</code> (such as <code>1em</code>). It looks as if the <code>length</code> value may be removed from the specification. As you can imagine, it would be possible for a web developer to make a very unusable scrollbar by playing with the width, so it may be better to allow the browser to decide the exact width that makes sense but instead to either show thin or thick scrollbars. Firefox has not implemented the length option.</p>

<p>If you use <code>auto</code> as the value, then the browser will use the default scrollbars: <code>thin</code> will give you a thin scrollbar, and <code>none</code> will show no visible scrollbar (but the element will still be scrollable).</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/da6370d7-bc30-4554-9b32-cee8961a5bf0/scrollbar-width.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/da6370d7-bc30-4554-9b32-cee8961a5bf0/scrollbar-width.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/da6370d7-bc30-4554-9b32-cee8961a5bf0/scrollbar-width.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/da6370d7-bc30-4554-9b32-cee8961a5bf0/scrollbar-width.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/da6370d7-bc30-4554-9b32-cee8961a5bf0/scrollbar-width.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/da6370d7-bc30-4554-9b32-cee8961a5bf0/scrollbar-width.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/da6370d7-bc30-4554-9b32-cee8961a5bf0/scrollbar-width.png"
			sizes="100vw"
			alt="A scrolling element with a thin scrollbar"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			In this example I have set <code>scrollbar-width: thin</code>.()
		</figcaption>
	
</figure>


<p>In a browser with support for CSS Scrollbars, you can see this in action in the demo:</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="MqVgXX"
   data-user="rachelandrew"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<p>The <code>scrollbar-color</code> property deals with &mdash; as you would expect &mdash; scrollbar colors. A scrollbar has two parts which you may wish to color independently:</p>

<ul>
<li><strong>thumb</strong><br />
The slider that moves up and down as you scroll.</li>
<li><strong>track</strong><br />
The scrollbar background.</li>
</ul>

<p>The values for the <code>scrollbar-color</code> property are <code>auto</code>, <code>dark</code>, <code>light</code> and <code>&lt;color&gt; &lt;color&gt;</code>.</p>

<p>Using <code>auto</code> as a keyword value will give you the default scrollbar colors for that browser, <code>dark</code> will provide a dark scrollbar, either in the dark mode of that platform or a custom dark mode, <code>light</code> the light mode of the platform or a custom light mode.</p>

<p>To set your own colors, you add two colors as the value that are separated by a space. The first color will be used for the <em>thumb</em> and the second one for the <em>track</em>. You should take care that there is enough contrast between the colors, as otherwise the scrollbar may be difficult to use for some people.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/06023d41-9eec-4c5d-aff6-b32c7434f995/scrollbar-color.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/06023d41-9eec-4c5d-aff6-b32c7434f995/scrollbar-color.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/06023d41-9eec-4c5d-aff6-b32c7434f995/scrollbar-color.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/06023d41-9eec-4c5d-aff6-b32c7434f995/scrollbar-color.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/06023d41-9eec-4c5d-aff6-b32c7434f995/scrollbar-color.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/06023d41-9eec-4c5d-aff6-b32c7434f995/scrollbar-color.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/06023d41-9eec-4c5d-aff6-b32c7434f995/scrollbar-color.png"
			sizes="100vw"
			alt="A scrolling element with a purple and white scrollbar"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			In this example, I have set custom colors for the scrollbar elements. ()
		</figcaption>
	
</figure>


<p>In a browser with support for CSS Scrollbars, you can see this in the demo:</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="VEgzPw"
   data-user="rachelandrew"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<h4 id="aspect-ratio-units">Aspect Ratio Units</h4>

<p>We&rsquo;ve been using the  in CSS to achieve aspect ratio boxes for some time, however, with the advent of Grid Layout and better ways of sizing content, having a real way to do aspect ratios in CSS has become a more pressing need.</p>

<p>There are two issues raised on GitHub which relate to this requirement:</p>

<ul>
<li></li>
<li>.</li>
</ul>

<p>There is now  was that this needed further discussion on GitHub before any decisions can be made. So, if you are interested in this, or have additional use cases, the CSS Working Group would be interested in your comments on those issues.</p>

<div class="sponsors__wide-place"></div>




<h4 id="the-where-functional-pseudo-class">The <code>:where()</code> Functional Pseudo-Class</h4>

<p>, the CSSWG resolved to add a pseudo-class which acted like <code>:matches()</code> but with zero specificity, thus making it easy to override without needing to artificially inflate the specificity of later elements to override something in a default stylesheet.</p>

<p>The <code>:matches()</code> pseudo-class might be new to you as it is a Level 4 Selector, however, it allows you to specify a group of selectors to apply some CSS, too. For example, you could write:</p>

<pre><code class="language-css">.foo a:hover,
p a:hover {
  color: green;
}
</code></pre>

<p>Or with <code>:matches()</code></p>

<pre><code class="language-css">:matches(.foo, p) a:hover {
  color: green;
}
</code></pre>

<p>If you have ever had a big stack of selectors just in order to set the same couple of rules, you will see how useful this will be. The following CodePen uses the prefixed names of <code>webkit-any</code> and <code>-moz-any</code> to demonstrate the <code>matches()</code> functionality. You can also .</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="rqPyQb"
   data-user="rachelandrew"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<p>Where we often do this kind of stacking of selectors, and thus where <code>:matches()</code> will be most useful is in some kind of initial, default stylesheet. However, we then need to be careful when overwriting those defaults that any overwriting is done in a way that will ensure it is more specific than the defaults. It is for this reason that a zero specificity version was proposed.</p>

<p>The issue that was discussed in the meeting was in regard to naming this pseudo-class, you can . Naming things in CSS is very hard — because we are all going to have to live with it forever! After a lot of debate, the group voted and decided to call this selector <code>:where()</code>.</p>

<p>Since the meeting, and while I was writing up this post, a suggestion has been raised to rename <code>matches()</code> to <code>is()</code>.  and comment if you have any strong feelings either way!</p>

<h4 id="logical-shorthands-for-margins-and-padding">Logical Shorthands For Margins And Padding</h4>

<p>On the subject of naming things, I&rsquo;ve written about Logical Properties and Values here on Smashing Magazine in the past, take a look at “”. These properties and values provide flow relative mappings. This means that if you are using Writing Modes other than a horizontal top to bottom writing mode, such as English, things like margins and padding, widths and height follow the text direction and are not linked to the physical screen dimensions.</p>

<p>For example, for physical margins we have:</p>

<ul>
<li><code>margin-top</code></li>
<li><code>margin-right</code></li>
<li><code>margin-bottom</code></li>
<li><code>margin-left</code></li>
</ul>

<p>The logical mappings for these (assuming horizontal-tb) are:</p>

<ul>
<li><code>margin-block-start</code></li>
<li><code>margin-inline-end</code></li>
<li><code>margin-block-end</code></li>
<li><code>margin-inline-start</code></li>
</ul>

<p>We can have two value shorthands. For example, to set both <code>margin-block-start</code> and <code>margin-block-end</code> as a shorthand, we can use <code>margin-block: 20px 1em</code>. The first value representing the start edge in the block dimension, the second value the end edge in the block dimension.</p>

<div class="sponsors__wide-place"></div>




<p>We hit a problem, however, when we come to the four-value shorthand <code>margin</code>. That property name is used for physical margins &mdash; how do we denote the logical four-value version? Various things have been suggested, including a switch at the top of the file:</p>

<pre><code class="language-css">@mode "logical";
</code></pre>

<p>Or, to use a block that looks a little like a media query:</p>

<pre><code class="language-css">@mode (flow-mode: relative) {

}
</code></pre>

<p>Then various suggestions for keyword modifiers, using some punctuation character, or creating a brand new property name:</p>

<pre><code class="language-css">margin: relative 1em 2em 3em 4em;
margin: 1em 2em 3em 4em !relative;
margin-relative: 1em 2em 3em 4em;
~margin: 1em 2em 3em 4em;
</code></pre>

<p> to see the various things that are being considered. Issues discussed were that while the logical version may well end up being generally the default, sometimes you will want things to relate to the screen geometry; we need to be able to have both options in one stylesheet. Having a <code>@mode</code> setting at the top of the CSS could be confusing; it would fail if someone were to copy and paste a chunk of the stylesheet.</p>

<p>My preference is to have some sort of keyword value. That way, if you look at the rule, you can see exactly which mode is being used, even if it does seem slightly inelegant. It is the sort of thing that a preprocessor could deal with for you; if you did indeed want all of your properties and values to use the logical versions.</p>

<p>We didn&rsquo;t manage to resolve on the issue, so if you do have thoughts on which of these might be best, or can see problems with them that we haven&rsquo;t described, please comment on the issue on GitHub.</p>

<h3 id="web-platform-tests-discussion">Web Platform Tests Discussion</h3>

<p>At the CSS Working Group meeting and then during the unconference style Technical Plenary Day, I was involved in discussing how to get more people involved in writing tests for CSS specifications. The  project aims to provide tests for all of the web platform. These tests then help browser vendors check whether their browser is correct as to the spec. In the CSS Working Group, the aim is that any normative change to a specification which has reached Candidate Recommendation (CR) status, should be accompanied by a test. This makes sense as once a spec is in CR, we are asking browsers to implement that spec and provide feedback. They need to know if anything in the spec changes so they can update their code.</p>

<p>The problem is that we have very few people writing specs, so for spec writers to have to write all the tests will slow the progress of CSS down. We would love to see other people writing tests, as it is a way to contribute to the web platform and to gain deep knowledge of how specifications work. So we met to think about how we could encourage people to participate in the effort. I&rsquo;ve written on this subject in the past; if the idea of writing tests for the platform interests you, take a look at my 24 Ways article on “”.</p>

<h3 id="on-with-the-work">On With The Work!</h3>

<p>TPAC has added to my personal to-do list considerably. However, I&rsquo;ve been able to pick up tips about specification editing, test writing, and to come up with a plan to get the Multi-Column Layout specification — of which I&rsquo;m the co-editor — back to CR status. As someone who is not a fan of meetings, I&rsquo;ve come to see how valuable these face-to-face meetings are for the web platform, giving those of us contributing to it a chance to share the knowledge we individually are developing. I feel it is important though to then take that knowledge and share it outside of the group in order to help more people get involved with developing as well as using the platform.</p>

<p>If you are interested in how the CSS Working Group functions, and how new CSS is invented and ends up in browsers, check out my 2017 CSSConf.eu presentation “”.</p>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(il)</span>
</div>


              </article>
            </body>
          </html>
---------------
<h1 id="#title_1" >2、FEX 技术周刊 - 2018/10/29</h1>

[http://fex.baidu.com/blog/2018/10/fex-weekly-29//](http://fex.baidu.com/blog/2018/10/fex-weekly-29//)
作者：dafrok <br> <h2 id="section">深阅读</h2>

<p><strong>React v16.6.0: lazy, memo and contextType</strong><br />
https://reactjs.org/blog/2018/10/23/react-v-16-6.html<br />
加了几个方便的方法。<br />
另附：.</p>

<p><strong>Qt Design Studio 1.0 Released</strong><br />
https://blog.qt.io/blog/2018/10/25/qt-design-studio-1-0-released/<br />
We believe that collaboration between designers and developers in an effective workflow fosters and boosts product innovation and ultimately leads to a  better user experience. That’s why I’m extremely happy to announce that Qt Design Studio 1.0 released today! Qt Design Studio is a UI design and development environment that enables designers and developers to rapidly prototype and develop complex and scalable UIs.</p>

<p><strong>The best WYSIWYG editor for Angular and React is here</strong><br />
https://ckeditor.com/blog/best-wysiwyg-editor-for-angular-react/<br />
We are happy to announce the first two integrations of CKEditor 5 with popular JavaScript frameworks: CKEditor 5 WYSIWYG editor component for React. CKEditor 5 WYSIWYG editor component for Angular 2+. We want to make installing and integrating CKEditor 5 as simple and intuitive as possible.</p>

<p><strong>Is WebAssembly faster than JavaScript?</strong><br />
https://lemire.me/blog/2018/10/23/is-webassembly-faster-than-javascript/<br />
Most programs running on web sites are written in JavaScript. There are still a few Java applets and other plugins hanging around, but they are considered obsolete at this point. It is far easier to find JavaScript front-end developers in almost any industry, except maybe gaming. I think it is almost surely going to be more labor intensive to program web applications using WebAssembly. <br />
另附：.</p>

<p><strong>灵活文档：通过上下文可视化链接文本和表格数据来帮助文档阅读</strong><br />
http://vis.pku.edu.cn/blog/elastic/<br />
数据丰富的文档本身就是复杂的数据集，它们由不同格式的信息组成，如文本，图形和数据表。这些额外的信息形式更有利于我们对文档中的文本叙述的理解。但是，传统的打印文档的静态布局通常会妨碍对其内容的深入理解，因为这些信息往往分散各个部分。在本文中[1]，我们寻求通过将文本内容与文档中包含的数据表格相结合的上下文可视化技术来促进对这些文档的更好理解。我们解析文本内容和数据表格，使用基于关键字的匹配算法来链接这两部分，并根据读者在文档中的当前关注点来生成可视化。<br />
另附：.</p>

<p><strong>Finally, a React Refactoring Tool - Introducing Glean</strong><br />
https://www.wix.engineering/blog/finally-a-react-refactoring-tool-introducing-glean<br />
React is the predominant framework today for web and mobile UI development, and it’s no surprise it is widely used by Wix Engineering. However, when it came to large-scale refactoring projects, there were no proper tools that could help with the process, and developers got used to a lot of keyboard activity with loads of ctrl+C and ctrl+V. Manual refactoring of React code was, therefore, quite time consuming and somewhat tedious, as well as error-prone when done on a massive scale. As JS is dynamic, refactoring automation could be quite a challenge to implement and that could explain the little support it has in common IDEs.</p>

<p><strong>Let the Framework do its job</strong><br />
https://blog.ionicframework.com/let-framework-do-its-job/<br />
One of the core changes Ionic is making is moving from custom build tooling to using the official tooling for each Framework we support.</p>

<p><strong>Applying Customer Feedback: How NLP &amp; Deep Learning Improve Uber’s Maps</strong><br />
https://eng.uber.com/nlp-deep-learning-uber-maps/<br />
To address the problem of large-scale ticket analysis, we built a natural language processing (NLP) platform that looks for map data-related issues in the text of tickets. This platform can then specify which specific type of map data triggered the ticket, so that the appropriate team within our maps organization can assess the issue and determine a solution. <br />
另附：.</p>

<p><strong>Why Netflix Rolled Its Own Node.js Functions-as-a-Service Runtime</strong><br />
https://thenewstack.io/why-netflix-rolled-its-own-node-js-functions-as-a-service-runtime/<br />
Engineers love the “no-ops” aspect of FaaS, which makes it possible to simply upload modular chunks of functionality onto the cloud provider of your choice and then execute them as isolated, reliable, and low latency production services. Enterprises love that their devs can deploy code to production faster than ever before. Netflix, a company respected for being an early and extremely effective adopter of cloud native tech, happily embraced FaaS to keep the films flowing smoothly to their 130 million customers streaming 140 million hours of video each day.</p>

<p><strong>Playing Mortal Kombat with TensorFlow.js. Transfer learning and data augmentation</strong><br />
https://blog.mgechev.com/2018/10/20/transfer-learning-tensorflow-js-data-augmentation-mobile-net/<br />
In this blog post, I’ll share my experience of building a posture classification algorithm using TensorFlow.js and MobileNet.</p>

<p><strong>How architecture evolves into strategy</strong><br />
https://www.oreilly.com/ideas/how-architecture-evolves-into-strategy<br />
A look at the roles of architect and strategist, and how they help develop successful technology strategies for business.</p>

<p><strong>The Past, Present, and Future of Go 2</strong><br />
https://dave.cheney.net/paste/the-past-present-and-future-of-go2.pdf<br />
Where Go came from? How Go has evolved since it was launched? What’s happening in Go 2? <br />
另附：</p>

<p><strong>How to write narrative documentation</strong><br />
http://esr.ibiblio.org/?p=8175<br />
In fact, writing good documentation is an excellent way to ensure that you really understand the problem space you’re in, and to throw light into corners of your software where defects might lurk. Do not underestimate the power of this effect! Often enough to matter, it will save you from serious embarrassment.</p>

<h2 id="section-1">新鲜货</h2>

<p><strong>gRPC-Web is going GA</strong><br />
https://www.cncf.io/blog/2018/10/24/grpc-web-is-going-ga/<br />
gRPC-Web enables you to define the service “contract” between client web applications and backend gRPC servers using .proto definitions and auto-generate client JavaScript (you can choose between Closure compiler JavaScript or the more widely used CommonJS). What you get to leave out of the development process: creating custom JSON serialization and deserialization logic, wrangling HTTP status codes (which can vary across REST APIs), content type negotiation, etc.</p>

<p><strong>Node v11.0.0 (Current)</strong><br />
https://nodejs.org/en/blog/release/v11.0.0/<br />
Node.js 11.0.0 is here! This is the newest Node.js Current Release line with a focus primarily on improving internals, performance, and an update to V8 7.0.<br />
另附：.</p>

<p><strong>Redis 5.0 is here!</strong><br />
https://redislabs.com/blog/redis-5-0-is-here/<br />
Redis reached a major milestone with the release of 5.0, which includes a variety of advancements and improvements. The big story here is the introduction of Streams as part of the release. Streams is the first entirely new data structure in Redis since HyperLogLog was introduced as part of 2.8.9 back in April 2014 (over four years ago)! <br />
另附：.</p>

<p><strong>30 Seconds of CSS</strong><br />
https://30-seconds.github.io/30-seconds-of-css/<br />
A curated collection of useful CSS snippets you can understand in 30 seconds or less.</p>

<p><strong>Introducing Squirrelly: a fast, lightweight, and simple JS template engine</strong><br />
https://hackernoon.com/introducing-squirrelly-a-fast-lightweight-and-simple-js-template-engine-70a873d765c9<br />
 is a template engine written in JavaScript. With Squirrelly, you can write templates that are blazing fast and can be rendered in milliseconds, server-side or client-side. Squirrelly doesn’t just limit you to HTML–you can use it with any language, and custom delimeters make it so there aren’t parsing errors. It’s also tiny (~2.5 KB gzipped), has 0 dependencies, and is blazing fast.</p>

<p><strong>IronDB</strong><br />
https://github.com/gruns/irondb<br />
A relentless key-value store for the browser.</p>

<p><strong>face-api.js</strong><br />
https://github.com/justadudewhohacks/face-api.js<br />
JavaScript API for face detection and face recognition in the browser with tensorflow.js</p>

<p><strong>percollate</strong><br />
https://github.com/danburzo/percollate<br />
Percollate is a command-line tool to turn web pages into beautifully formatted PDFs.</p>

<p><strong>A Web-Based Random Dummy Data Generation Tool</strong><br />
https://www.onlinedatagenerator.com/<br />
Here you can find up to 100 combinations of data formats and information. Build up your test dataset and export your data in CSV, Excel, Json, or even Sql script to create your table.<br />
It’s very easy - Add new fields, select a field category, and a field type, establish ranges if required and preview you data. You can generate up to 10 000 rows with random names, random address or fake email address.</p>

<p><strong>Announcing the GNU Kind Communication Guidelines</strong><br />
http://lists.gnu.org/archive/html/info-gnu/2018-10/msg00001.html<br />
The GNU Kind Communication Guidelines, initial version, have been published in https://gnu.org/philosophy/kind-communication.html. On behalf of the GNU Project, I ask all GNU contributors to make their best efforts to follow these guidelines in GNU Project discuaaions.</p>

<h2 id="section-2">设计</h2>

<p><strong>设计师的职责：重在参与</strong><br />
https://www.huxiu.com/article/268881.html<br />
严格来说，复杂适应性系统的设计师所设计的并非系统本身，他们是把一系列现有的互相关联的系统引导至他们所期望的成果。对于这些会与其他力量、想法、事件和设计师产生交互的系统，它们的设计师没有把自己置于系统的中心，而是将自己理解为塑造这些系统的“参与者”。本文的主旨是探索“参与”在这里的意义。<br />
另附：.</p>

<p><strong>Introducing CodeX</strong><br />
https://blog.prototypr.io/introducing-codex-5cdaf7140090<br />
Welcome CodeX, fully automated, real-time platform for automated design/development handoff and advanced prototyping.<br />
另附：.</p>

<p><strong>User flow is the new wireframe</strong><br />
https://uxdesign.cc/when-to-use-user-flows-guide-8b26ca9aa36a<br />
An illustrated guide on the different ‘resolutions’ of user flows, and when to use them.<br />
另附：.</p>

<p><strong>Augmented Reality vs. Virtual Reality vs. Mixed Reality – An Introductory Guide</strong><br />
https://www.toptal.com/designers/ui/augmented-reality-vs-virtual-reality-vs-mixed-reality<br />
In this article, we start by highlighting the nuances between VR, AR, and MR, and then take a quick trip back in time to see how VR/AR evolved. Finally, we evaluate how they fit in today’s reality, and how they may affect tomorrow’s.</p>

<p><strong>深入了解柳冠中的设计观</strong><br />
https://www.uisdc.com/learn-liuguanzhong-design-concept<br />
柳冠中老师是中国最早的工业设计创始人之一，其「设计事理学」出发点和落脚点都源自于辩证唯物主义哲学观，事理学的设计观点也给人以醍醐灌顶的启发。柳教授的事理学观点无论是从自然建构的基础学科思考问题还是从研究复杂体系的综合学科层面思考，事理学中都可以找到相关的论点和论据。</p>

<h2 id="section-3">产品及其它</h2>

<p><strong>保罗·艾伦的故事</strong><br />
http://www.ruanyifeng.com/blog/2018/10/paul-allen.html<br />
如果你现在去西雅图，到处可以看到保罗的痕迹。他建立了流行文件博物馆、计算机博物馆，创办画廊和音乐节。现在他不在了，但是他支持的这些事业还会长久地存在。正如盖茨在悼念文章中所说：”保罗应当活得更久一些，他一定会充分利用那些多出来的时间。我将非常地怀念他。”</p>

<p><strong>如何高效把书读「薄」-专访 MarginNote</strong><br />
https://sspai.com/post/47547<br />
说起 iPad 上的学习工具，MarginNote 一定会是许多人第一个想到的选择。除了最基础的阅读和批注功能，MarginNote 还支持大纲、脑图、学习卡等高阶并且复杂的功能。为什么 MarginNote 在默默「耕耘」了几年之后才走进大家的视野并且变得热门起来？相比于同类产品，MarginNote 到底有着怎样的优势和特点，让它能够成为许多人心目中独一无二的学习工具？本期幕后一起听 MarginNote 的开发者 Min 聊一聊背后的故事。另附：</p>

<p><strong>大胆减少你的工作</strong><br />
https://mp.weixin.qq.com/s?__biz=MzIxNTAzNzU0Ng==&amp;mid=2654611005&amp;idx=2&amp;sn=d4ed61b97c814b12530d4743cc357a2b<br />
关于知识工作者任务的讨论，一般都从如何做计划说起。这样看来很合乎逻辑。可惜的是，知识工作者的工作计划很少有能够真正发生作用的。计划通常只是纸上谈兵，或只是良好的意愿而已，很少能够真正实现。有效的知识工作者并不是一开始就着手工作，他们往往会从时间安排上着手。他们并不以计划为起点，认识清楚自己的时间用在什么地方才是起点。然后，他们管理自己的时间，减少非生产性工作所占用的时间。最后，再将“可自由运用的时间”，由零星的集中成大块连续性的时段。</p>

<p><strong>What does Stack Overflow want to be when it grows up?</strong><br />
https://blog.codinghorror.com/what-does-stack-overflow-want-to-be-when-it-grows-up/<br />
I sometimes get asked by regular people in the actual real world what it is that I do for a living, and here’s my 15 second answer: We built a sort of Wikipedia website for computer programmers to post questions and answers. It’s called Stack Overflow. As of last month, it’s been 10 years since Joel Spolsky and I started Stack Overflow. I currently do other stuff now, and I have since 2012, but if I will be known for anything when I’m dead, clearly it is going to be good old Stack Overflow. Thus, what I’d like to do right now is peer into that glorious abyss for a bit and introspect about the challenges I see facing Stack Overflow for the next 10 years.</p>

<p>– THE END –</p>
---------------
<h1 id="#title_2" >3、FEX 技术周刊 - 2018/08/20</h1>

[http://fex.baidu.com/blog/2018/08/fex-weekly-20//](http://fex.baidu.com/blog/2018/08/fex-weekly-20//)
作者：Dafrok <br> <p>微信搜索『FEX』关注我们的公众号，及时获得最新资讯。</p>

<h2 id="section">业界会议</h2>

<p><strong>中国首届React DEV Conf &amp; FEDAY 2018</strong><br />
https://fequan.com/2018/ <br />
https://react.w3ctech.com/<br />
可围观，期待会议资料。</p>

<h2 id="section-1">深阅读</h2>

<p><strong>Who Left Open The Cookie Jar?</strong><br />
https://wholeftopenthecookiejar.eu/<br />
As browsers have become enormously complex, certain edge-cases may have been overlooked or the interplay of specific features may have unwanted side-effects. In our research, we created a framework to verify whether all imposed cookie- and request-policies are correctly applied (will be made available soon). Worryingly, we found that most mechanisms could be circumvented: for instance for all ad-blocking and anti-tracking browser extensions we discovered at least one technique that could bypass the policies. For the technical details of these findings, we invite you to .</p>

<p><strong>Embedded builtins</strong><br />
https://v8project.blogspot.com/2018/08/embedded-builtins.html<br />
V8 built-in functions (builtins) consume memory in every instance of V8. The builtin count, average size, and the number of V8 instances per Chrome browser tab have been growing significantly. This blog post describes how we reduced the median V8 heap size per website by 19% over the past year.</p>

<p><strong>JavaScript engine fundamentals: optimizing prototypes</strong><br />
https://mathiasbynens.be/notes/prototypes<br />
This article describes some key fundamentals that are common to all JavaScript engines — and not just V8, the engine the authors (Benedikt and Mathias) work on. As a JavaScript developer, having a deeper understanding of how JavaScript engines work helps you reason about the performance characteristics of your code.</p>

<p><strong>Keep Betting on JavaScript by Kyle Simpson</strong><br />
https://www.youtube.com/watch?v=lDLQA6lQSFg<br />
“Always bet on JavaScript”, revels in JS’s history of naysayers predicting that we’d eventually reach a point where JS couldn’t grow to meet the demands of modern development; it turns out those have always been bad bets. It’s safe to say JS is no longer trying to prove itself. It has arrived.</p>

<p><strong>Principles of Modern Application Development</strong><br />
https://www.nginx.com/blog/principles-of-modern-application-development/<br />
These principles can be summarized as keep it small, design for the developer, and make it networked. With these three principles, you can design a robust, complex application that can be delivered quickly and securely, scaled easily, and extended simply.</p>

<p><strong>The 10:1 rule of writing and programming</strong><br />
https://www.ybrikman.com/writing/2018/08/12/the-10-to-1-rule-of-writing-and-programming/<br />
Give that my data set is limited, I can only draw a few preliminary conclusions: The ratio of “raw materials” to “finished product” in a book is roughly 10:1. Keep this in mind the next time an editor asks you for a timeline! If you want to write a 300 page book, you’ll probably have to write around 3,000 pages. Similarly, the ratio of “code churn” to “lines of code” in mature and non-trivial software is also at least 10:1. Keep this in mind the next time a manager or customer asks you for a time estimate! To build a 10,000 line app, expect to write roughly 100,000 lines. These can be summarized as what I shall dub the 10:1 rule of writing and programming: Good software and good writing requires that every line has been rewritten, on average, at least 10 times.</p>

<p><strong>前端下半场：构建跨框架的 UI 库</strong><br />
https://www.phodal.com/blog/build-cross-framework-ui-library/<br />
跨框架的 UI 库，即前端 UI 库可以不经任何修改，直接能运行在 React、Angular、Vue 等框架上。</p>

<p><strong>微前端的设计理念与实践初探</strong><br />
https://zhuanlan.zhihu.com/p/41879781<br />
微服务与微前端，都是希望将某个单一的单体应用，转化为多个可以独立运行、独立开发、独立部署、独立维护的服务或者应用的聚合，从而满足业务快速变化及分布式多团队并行开发的需求。如康威定律(Conway’s Law)所言，设计系统的组织，其产生的设计和架构等价于组织间的沟通结构；微服务与微前端不仅仅是技术架构的变化，还包含了组织方式、沟通方式的变化。</p>

<p><strong>聊聊Web中的度数单位</strong><br />
https://www.w3cplus.com/css/understanding-degrees-on-the-web.html<br />
在现实世界中，度数几乎是测量角度的单位。它在Web中同样是一个受欢迎的角色，也适用于我们将遇到的各种场景。幸运的是，在现实世界中的度数和虚拟世界中的度数有很多相似之处，所以在这篇文章中将来学习一些有关于度数相关的知识，然后深入了解一些细节。</p>

<p><strong>漫谈前端性能 突破 React 应用瓶颈</strong><br />
https://zhuanlan.zhihu.com/p/42032897<br />
性能一直以来是前端开发中非常重要的话题。随着前端能做的事情越来越多，浏览器能力被无限放大和利用：从 web 游戏到复杂单页面应用，从 NodeJS 服务到 web VR/AR、数据可视化，前端工程师总是在突破极限。随之而来的性能问题有的被迎刃而解，有的成为难以逾越的盾墙。那么，当我们在谈论性能时，到底在说什么？基于 React 框架开发的应用，在性能上又有哪些特点？这篇文章我们从浏览器和 JavaScript 引擎角度来剖析前端性能，同时创新 React，充分利用浏览器能力突破局限。</p>

<p><strong>洞察 video 超能力系列——玩转 flv</strong><br />
https://techblog.toutiao.com/2018/08/13/untitled-52/<br />
flv的全程是 Flash Video，顾名思义，就是专门给flash播放器提供的播放格式，这种格式具有结构简单、清晰的优点，最早出现是为了解决flash导出的swf文件体积过大，不适合在web中播放的问题。随着flash的逐渐淘汰，新的video标签自然是不支持flv格式的，人们开始把web视频的重点放在mp4或者hls上，但是随着直播这种视频形式的火热兴起，flv迎来了新一轮的生机。</p>

<p><strong>Simple internationalization of React apps</strong><br />
https://itnext.io/simple-internationalization-of-react-apps-34b3bda95725<br />
react-intl is still a standard when it comes to i18n of React apps. Even though it haven’t been maintained for about a year, the community is so strong that it’s gaining on popularity and new independent tools are constantly being published. I would like to introduce you to alternative i18n solution I’ve been working on for the last year and a half — . The low-level API is very similar to react-intl to make migration of my projects easier, but on top of that there’s a completely different developer experience.</p>

<p><strong>Creating a Chrome extension in 2018: The good, the bad and the meh</strong><br />
https://checklyhq.com/blog/2018/08/creating-a-chrome-extension-in-2018-the-good-the-bad-and-the-meh/<br />
We shipped an initial version of , a Google Chrome extension that records your browser interactions and generates a Puppeteer script. It turns out Chrome extension development is almost like real web development, but with a weird dash of quasi embedded development mixed in. This post talks you through the development lifecycle when creating an extension and lists some of the architectural gotcha’s. Source code for the extension in question is on github.</p>

<p><strong>Browser painting and considerations for web performance</strong><br />
https://css-tricks.com/browser-painting-and-considerations-for-web-performance/<br />
In this article, I’d like to focus on the last part: painting. All of those steps combined is a lot of work for a browser to do on load… and actually, not just on load, but any time the DOM (or CSSOM) is changed. That’s why many web developers tend to partially solve this by using some sort of frontend framework, such as React which, apart from many other advantages, can help to highly optimize changes in the DOM to avoid unnecessary recalculating or rendering.</p>

<p><strong>Creating the “Perfect” CSS System</strong><br />
https://medium.com/gusto-design/creating-the-perfect-css-system-fa38f5bcdd9e<br />
A high level guide for designers and developers who write CSS, but want to be more strategic about building moderate to large scale CSS systems.<br />
另附：.</p>

<p><strong>Cross-tab Synchronization with the Web Locks API</strong><br />
https://www.sitepen.com/blog/2018/08/14/cross-tab-synchronization-with-the-web-locks-api/<br />
The Web Locks API is a new addition to the Web Platform which allows you to execute JavaScript in a lock, a resource which can potentially get shared with other browser tabs. Use cases which are suitable for the Web Locks API are the managing, coordinating, and syncing of multi-tab interactions. Currently, some or all of the Shared Web Worker, Broadcast Channel, Local Storage, Session Storage, Post Message &amp; unload handler APIs can be used to manage tab communication and synchronization, however, they each have their drawbacks and require workarounds which decrease code maintainability.</p>

<p><strong>Shadow DOM in Ionic (and Why it’s Awesome)</strong><br />
https://blog.ionicframework.com/shadow-dom-in-ionic-and-why-its-awesome/<br />
I’d like to think we here at Ionic know a thing or two about Shadow DOM, as we recently made the move to using it in Ionic 4, and with that, received a lot of questions from the community on just what the heck it is. There’s a lot of information (and misinformation) floating around about Shadow DOM, so let’s go through the API and see what it actually does.</p>

<p><strong>WebAssembly: How and why</strong><br />
https://blog.logrocket.com/webassembly-how-and-why-559b7f96cd71<br />
How to run native code in the browser, why would you do that, and what does it all mean for JavaScript and the future of web development</p>

<p><strong>Dweb: Building a Resilient Web with WebTorrent</strong><br />
https://hacks.mozilla.org/2018/08/dweb-building-a-resilient-web-with-webtorrent/<br />
The web is healthy when the financial cost of self-expression isn’t a barrier. In this installment of the Dweb series we’ll learn about WebTorrent – an implementation of the BitTorrent protocol that runs in web browsers. This approach to serving files means that websites can scale with as many users as are simultaneously viewing the website – removing the cost of running centralized servers at data centers.</p>

<p><strong>Introducing headless Chrome support in Cloud Functions and App Engine</strong><br />
https://cloud.google.com/blog/products/gcp/introducing-headless-chrome-support-in-cloud-functions-and-app-engine<br />
We’re pleased to announce that the Google Cloud Functions and Cloud Functions for Firebase Node.js 8 runtimes have also been upgraded with the OS packages required to run headless Chrome. This means that you can now author Cloud Functions that use headless Chrome—and utilize all the features of a web browser in a fully serverless environment. Headless Chrome lets you take advantage of the modern web platform features from Chromium and the Blink rendering engine too.<br />
另附：.</p>

<p><strong>Beyond Web and Worker: Evolution of the Modern Web App on Heroku</strong><br />
https://blog.heroku.com/modern-web-app-architecture<br />
This is the first in a series of blog posts examining the evolution of web app architecture over the past 10 years. This post examines the forces that have driven the architectural changes and a high-level view of a new architecture. In future posts, we’ll zoom in to details of specific parts of the system.</p>

<p><strong>How to Debug a Node.js app in a Docker Container</strong><br />
https://blog.risingstack.com/how-to-debug-a-node-js-app-in-a-docker-container/<br />
While containerization, in general, is a very powerful tool - and here at RisingStack we always start new projects by spinning up the needed infrastructure in a docker-compose.yaml - it can be tricky to reach the enveloped Node process if you don’t know how to do it.</p>

<p><strong>Serverless Docker Beta</strong><br />
https://zeit.co/blog/serverless-docker<br />
The focus of our ZEIT Day Keynote this year was on the new capabilities of the Now cloud platform. In particular, we emphasized our focus on Serverless Docker Deployments. Today, we are announcing their availability as a public beta, which features: A 10x-20x improvement in cold boot performance, based on data from 1.5M+ deployments…<br />
另附：.</p>

<p><strong>Beyond Interactive: Notebook Innovation at Netflix</strong><br />
https://medium.com/netflix-techblog/notebook-innovation-591ee3221233<br />
Notebooks have rapidly grown in popularity among data scientists to become the de facto standard for quick prototyping and exploratory analysis. At Netflix, we’re pushing the boundaries even further, reimagining what a notebook can be, who can use it, and what they can do with it. And we’re making big investments to help make this vision a reality. In this post, we’ll share our motivations and why we find Jupyter notebooks so compelling. We’ll also introduce components of our notebook infrastructure and explore some of the novel ways we’re using notebooks at Netflix.</p>

<p><strong>Maximizing Process Performance with Maze, Uber’s Funnel Visualization Platform</strong><br />
https://eng.uber.com/maze/<br />
By applying Maze to the logs captured during driver sign-up, we can visualize the actual paths drivers take when signing up with Uber, and identify bottlenecks that occur in the process. Maze’s application at Uber has since expanded beyond the sign-up use case, and it is now used to visualize many processes—from rider pick-up and drop-off to user interactions with our website. Read on to learn how the Uber Visualization team developed Maze and why this new solution offers unparalleled insight into the Uber user experience.</p>

<p><strong>Capturing Data Evolution in a Service-Oriented Architecture</strong><br />
https://medium.com/airbnb-engineering/capturing-data-evolution-in-a-service-oriented-architecture-72f7c643ee6f<br />
Building Airbnb’s Change Data Capture system (SpinalTap), to enable propagating &amp; reacting to data mutations in real time.</p>

<p><strong>E-Commerce at Scale: Inside Shopify’s Tech Stack</strong><br />
https://shopifyengineering.myshopify.com/blogs/engineering/e-commerce-at-scale-inside-shopifys-tech-stack<br />
Shopify is a multi-channel commerce platform for small and medium businesses that lets you create a shop and sell products wherever you want: online via web store or social media and offline with a POS card reader. Shopify powers 600K merchants and serves 80K requests per second at peak. While helping aspiring entrepreneurs to launch their stores, Shopify also holds some of the world’s largest sales for the Super Bowl, Kylie Cosmetics, and celebrities like Justin Bieber and Kanye West. These “flash sales” are tricky from an engineering point of view because of their unpredictably large volumes of traffic.</p>

<p><strong>Cost of a Join</strong><br />
https://www.brianlikespostgres.com/<br />
It depends! It depends what the join criteria is, what indexes are present, how big the tables are, whether the relations are cached, what hardware is being used, what configuration parameters are set, whether statistics are up-to-date, what other activity is happening on the system, to name a few things.</p>

<p><strong>Universal Method to Sort Complex Information Found</strong><br />
https://www.quantamagazine.org/universal-method-to-sort-complex-information-found-20180813/<br />
The nearest neighbor problem asks where a new point fits into an existing data set. A few researchers set out to prove that there was no universal way to solve it. Instead, they found such a way.</p>

<p><strong>Dijkstra’s in Disguise</strong><br />
https://blog.evjang.com/2018/08/dijkstras.html<br />
Dijkstra’s, Bellman-Ford, Johnson’s, Floyd-Warshall are good algorithms for solving the shortest paths problem. This blog post is a gentle tutorial on how all these varied CS topics are connected. No prior knowledge of finance, reinforcement learning, or computer graphics is needed. The reader should be familiar with undergraduate probability theory, introductory calculus, and be willing to look at some math equations. I’ve also sprinkled in some insights and questions that might be interesting to the AI research audience, so hopefully there’s something for everybody here.<br />
另附：.</p>

<h2 id="section-2">新鲜货</h2>

<p><strong>GiuHub - Release Radar · July 2018</strong><br />
https://blog.github.com/2018-08-17-release-radar-july-2018/<br />
July has come and gone, leaving a lot of exciting releases in its wake! It’s been an especially big month for people learning to program—we’re highlighting two releases that will help new programmers—but there’s something for everyone in this month’s Release Radar.</p>

<p><strong>Front-End Performance Checklist</strong><br />
https://github.com/thedaviddias/Front-End-Performance-Checklist/<br />
The only Front-End Performance Checklist that runs faster than the others. One simple rule: “Design and code with performance in mind”</p>

<p><strong>JavaScript for impatient programmers</strong><br />
http://exploringjs.com/impatient-js/<br />
Goal of this book: make JavaScript less challenging to learn for newcomers, by offering a modern view that is as consistent as possible. Highlights: Get started quickly, by initially focusing on modern features; Test-driven exercises and quizzes for most chapters; Covers all essential features of JavaScript, up to and including ES2018; Advanced sections occasionally let you dig deeper (if you want to); No prior knowledge of JavaScript is required, but you should know how to program.<br />
另附：.</p>

<p><strong>Preventing downloading images or objects until they are visible in the viewport</strong><br />
https://github.com/whatwg/html/issues/2806<br />
One solution to this is to have an attribute for declaring which images or objects should not be downloaded and decoded until they are visible in the viewport. For example,  <code class="highlighter-rouge">&lt;img lazyload&gt;.*.</code> Alternatively, a meta element could be placed in the head to globally set all images and objects to only download once they are visible in the viewport.</p>

<p><strong>bbx</strong><br />
https://bbxjs.github.io/<br />
bbx 是一个极其简单高效的 React 状态管理方式。你可以很方便的使用 bbx 进行状态管理而不用太多的困扰，也就是说，要是你会 React，那就已经会使用 bbx 了。</p>

<p><strong>Popmotion</strong><br />
https://popmotion.io/<br />
Simple libraries for delightful interfaces.</p>

<p><strong>Nano ID</strong><br />
https://github.com/ai/nanoid<br />
A tiny, secure, URL-friendly, unique string ID generator for JavaScript. Safe: It uses cryptographically strong random APIs and tests distribution of symbols. Small: 145 bytes (minified and gzipped). No dependencies. It uses Size Limit to control size. Compact: It uses a larger alphabet than UUID (A-Za-z0-9_~). As result it could reduce ID size from 36 to 21 symbols.</p>

<p><strong>Tone.js</strong><br />
https://github.com/Tonejs/Tone.js<br />
A Web Audio framework for making interactive music in the browser.</p>

<p><strong>Spacetime</strong><br />
https://github.com/spencermountain/spacetime<br />
A lightweight javascript timezone library.</p>

<p><strong>The Best JavaScript Data Visualization &amp; Charting Libraries</strong><br />
https://www.codewall.co.uk/the-best-javascript-data-visualization-charting-libraries/<br />
There are quite a few charting libraries around now, but which one’s are the best to use? This can depend on many things like business needs, type of data, purpose of the chart itself and many more. In this article, each JavaScript charting library will be compared with some key factors including chart types, commercial or free and open-source status. These beautiful libraries been analysed thoroughly with hands-on experience to maximize the very best comparison.<br />
另附： .</p>

<p><strong>OpenPGPjs, has passed an independent security audit</strong><br />
https://protonmail.com/blog/openpgpjs-protonmail-security-audit/<br />
As part of our commitment to open source, we maintain the  encryption library. After some recent code enhancements, OpenPGPjs underwent an independent security audit, the results of which are discussed below.</p>

<p><strong>Termgraph</strong><br />
https://github.com/mkaz/termgraph<br />
A python command-line tool which draws basic graphs in the terminal.</p>

<p><strong>Python Fire</strong><br />
https://github.com/google/python-fire<br />
Python Fire is a library for automatically generating command line interfaces (CLIs) from absolutely any Python object.</p>

<p><strong>git-bug</strong><br />
https://github.com/MichaelMure/git-bug<br />
Distributed bug tracker embedded in Git.</p>

<h2 id="section-3">设计</h2>

<p><strong>The easiest way to keep your web apps accessible: Just use text</strong><br />
https://blog.logrocket.com/the-easiest-way-to-keep-your-web-apps-accessible-c2b57506cc2a<br />
Keeping increasingly complex web apps accessible is a necessity. Fortunately, there is one thing you can do to keep any web app accessible to as many users as possible, and lessen the burden of development and maintenance for yourself, too. Just use text.</p>

<p><strong>Framer X — Initial Impressions</strong><br />
https://blog.prototypr.io/framer-x-initial-impressions-3402c20257e8<br />
The power of code meets the power of design. Framer X, currently in invite only Beta, is the future of Framer(RIP). AND IT IS EXCITING!!! Apologies for the caps but it is indeed exciting and here’s why…</p>

<p><strong>Living in Information, Responsible Design for Digital Places: a Book Excerpt</strong><br />
http://uxmag.com/articles/living-in-information-responsible-design-for-digital-places-a-book-excerpt<br />
We are in the midst of a major social transformation — moving many of our day-to-day activities from physical places to information-based places that we experience on our phones and computers. The central question of this book is: How can we design these information environments so they serve our social needs in the long term?</p>

<p><strong>How to design for (and with) developers</strong><br />
https://about.gitlab.com/2018/08/17/designing-for-developers/<br />
Designers have a challenging task: Solve problems to empower users to do their best work. To understand how designers balance the demands of their roles as problem solvers with the evolving needs of an audience, I chatted with UX Manager Sarrah Vesselov about the considerations that go into designing for developers.</p>

<h2 id="section-4">产品及其它</h2>

<p><strong>写给工程师的十条精进原则</strong><br />
https://tech.meituan.com/10_principles_for_engineers.html<br />
“追求卓越”是美团的价值观。作为一名技术人员，我们应该如何践行呢？本文总结了十条精进原则，希望能够给大家带来一些启发，更好地指导我们的行动。</p>

<p><strong>Make Something Great: Become an Open Source Contributor</strong><br />
https://alistapart.com/article/make-something-great-become-an-open-source-contributor<br />
You may think that open source is not for you. After all, it has always been a developer-dominant ecosystem. But code is by no means the only thing a piece of software is made of. Open source is first and foremost about community. Whether you’re a designer, developer, writer, doctor, or lawyer, there are many paths to the open source world. Learn what you need to know to set out on your journey, from first steps to becoming a core contributor. It might change your career.</p>

<p><strong>他把自己估值上万亿美元的项目免费化了</strong><br />
https://mp.weixin.qq.com/s?__biz=MzIyMTM5ODU4Nw==&amp;mid=2247487419&amp;idx=1&amp;sn=9e9509c5b33d7e7eb893a67c161f6d7c<br />
这个不起眼的小伙子叫萨尔曼·可汗（Salman Khan），今年39岁。他颠覆了美国教育，成为了数学教父，让数学老师不再讲课，比尔盖茨都捧着他。他成功登上了《福布斯》杂志封面，但是他却拒绝了10亿美元！</p>

<p><strong>全面反思腾讯的战略</strong><br />
https://36kr.com/p/5148266.html<br />
看待腾讯，有很多视角，今天我用的是数据与算法这个视角。数据与算法，以我对两者重要性的理解，我觉得是对一家互联网公司运营最高维度的抽象，这个视角过滤掉了许多喧嚣的表面因素和大量无关紧要的细枝末节，因而有可能是最接近本质的。我认为，从数据与算法的角度看，一个公司从小到大的进化过程，无非是在做两件事情，一是升级算法处理数据，二是获取更多的数据，而在这两方面，腾讯都做得不够好，它未来的进化之路就会困难重重。</p>
---------------
<h1 id="#title_3" >4、文章： Helm：三思而后用</h1>
Bartłomiej Antoniak
[http://www.infoq.com/cn/articles/think-twice-before-using-helm?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/think-twice-before-using-helm?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/think-twice-before-using-helm/zh/smallimage/cs8-ranges-and-recursive-patterns-logo-1532385277819-1540056810292.jpeg"/><p>Helm是Kubernetes的包管理器。它可以大幅简化发布过程，但有时候也会带来问题。近日，Helm已经提升为正式的顶级@CloudNativeFdn项目，并且在社区得到了广泛的应用。那可以说明一些问题，但我将和你分享我对于Helm的一些思考。本文将说明我不相信那些大肆宣传的原因。</p> <i>By Bartłomiej Antoniak</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_4" >5、William McKnight关于数据平台和创建现代数据架构的见解</h1>
Srini Penchikala
[http://www.infoq.com/cn/news/2018/10/das-modern-data-architecture?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/10/das-modern-data-architecture?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>在上周举行的数据架构2018年峰会上，William McKnight就使用不同的数据平台创建现代数据架构做了主旨演讲。</p> <i>By Srini Penchikala</i> <i> Translated by  姚佳灵</i>
---------------
<h1 id="#title_5" >6、Oboe，安卓上的低延迟音频应用开发库</h1>
Diogo Carleto
[http://www.infoq.com/cn/news/2018/10/android-oboe?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/10/android-oboe?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>谷歌已经发布了第一个生产就绪的Oboe版本。Oboe是一个C++库，它用来构建在99%的安卓设备上都有着最低可能延迟的高性能音频应用。</p> <i>By Diogo Carleto</i> <i> Translated by Key先森</i>
---------------
<h1 id="#title_6" >7、gRPC-Web发布，REST又要被干掉了？</h1>
Luc Perkins
[http://www.infoq.com/cn/news/2018/10/published-gRPC-Web?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/10/published-gRPC-Web?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>云原生计算基金会（CNCF）正式发布GA版本的gRPC-Web，这是一个JavaScript客户端库，使Web应用程序能够直接与后端gRPC服务通信，不需要HTTP服务器充当中介。这意味着你现在可以通过.proto文件来定义客户端和服务器端数据类型和服务接口，轻松构建真正的端到端gRPC应用程序架构。gRPC-Web为Web开发提供了REST之外的另一个选择。</p> <i>By Luc Perkins</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_7" >8、数据建模NoSQL数据库的概念和对象建模符号</h1>
Srini Penchikala
[http://www.infoq.com/cn/news/2018/10/hills-data-modeling-nosql-comn?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/10/hills-data-modeling-nosql-comn?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>在最近的2018数据架构峰会上，Ted Hills主持了一个研讨会，该研讨会的主题是关系数据库和NoSQL数据库的数据建模。</p> <i>By Srini Penchikala</i> <i> Translated by 姚佳灵</i>
---------------