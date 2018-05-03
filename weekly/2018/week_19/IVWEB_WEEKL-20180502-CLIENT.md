## 文章索引
1、 <a href="#1a-guide-to-the-state-of-print-stylesheets-in-2018" >A Guide To The State Of Print Stylesheets In 2018</a><br/>
2、 <a href="#2文章-数字化转型指南第一部分" >文章： 数字化转型指南（第一部分）</a><br/>
3、 <a href="#3文章-paas将吞噬云计算kubernetes的市场冲击波" >文章： PaaS将吞噬云计算？Kubernetes的市场冲击波</a><br/>
4、 <a href="#4文章-如何用游戏引擎改造hybrid-app" >文章： 如何用游戏引擎改造Hybrid App？</a><br/>
5、 <a href="#5揭秘applegoogle等千亿市值企业的架构设计" >揭秘Apple、Google等千亿市值企业的架构设计</a><br/><h1 id="#title_0" >1、A Guide To The State Of Print Stylesheets In 2018</h1>
Rachel Andrew
[https://www.smashingmagazine.com/2018/05/print-stylesheets-in-2018/](https://www.smashingmagazine.com/2018/05/print-stylesheets-in-2018/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/05/print-stylesheets-in-2018/" />
              <title>A Guide To The State Of Print Stylesheets In 2018</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>A Guide To The State Of Print Stylesheets In 2018</h1>
                  
                    
                    <address>Rachel Andrew</address>
                  
                  <time datetime="2018-05-01T14:00:19&#43;02:00" class="op-published">2018-05-01T14:00:19+02:00</time>
                  <time datetime="2018-05-01T15:51:08&#43;00:00" class="op-modified">2018-05-01T15:51:08+00:00</time>
                </header>
                

<p>Today, I’d like to return to a subject that has already been covered in Smashing Magazine in the past &mdash; the topic of the print stylesheet. In this case, I am talking about printing pages directly from the browser. It’s an experience that can lead to frustration with enormous images (and even advertising) being printed out. Just sometimes, however, it adds a little bit of delight when a nicely optimized page comes out of the printer using a minimum of ink and paper and ensuring that everything is easy to read.</p>

<p>This article will explore how we can best create that second experience. We will take a look at how we should include print styles in our web pages, and look at the specifications that really come into their own once printing. We’ll find out about the state of browser support, and how to best test our print styles. I’ll then give you some pointers as to what to do when a print stylesheet isn’t enough for your printing needs.</p>

<h3 id="key-places-for-print-support">Key Places For Print Support</h3>

<p>If you still have not implemented any print styles on your site, there are a few key places where a solid print experience will be helpful to your users. For example, many users will want to print a transaction confirmation page after making a purchase or booking even if you will send details via email.</p>

<p>Any information that your visitor might want to use when away from their computer is also a good candidate for a print stylesheet. The most common thing that I print are recipes. I could load them up on my iPad but it is often more convenient to simply print the recipe to pop onto the fridge door while I cook. Other such examples might be directions or travel information. When traveling abroad and not always having access to data these printouts can be invaluable.</p>



<aside class="product-panel product-panel__tilted product-panel--book" data-audience="non-subscriber">
    <div class="container product-panel--book__container">
      <div class="panel__description panel__description--book">
    <p>Nope, we can't do any magic tricks, but we have articles,  get a seasoned selection of magic front-end tricks — e.g. <strong>live designing sessions</strong> and perf audits, too. <em>Just sayin'</em>! ;-)</p>

      <a href="https://www.smashingmagazine.com/membership/?utm_medium=panel" class="btn btn--green btn--large">
        Explore Smashing Wizardry&nbsp;→
      </a>
      </div>
      <div class="panel__image panel__image--book">
        <a href="https://www.smashingmagazine.com/membership/?utm_medium=panel" class="books__book__image">
        <div class="books__book__img">
          <img src="https://www.smashingmagazine.com/images/smashing-cat/cat-wizard.svg" alt="Smashing Cat, just preparing to do some magic stuff." width="310" height="400">
        </div>
      </a>
      </div>
    </div>
  </aside>





<div class="c-garfield-the-cat">


<p>Reference materials of any sort are also often printed. For many people, being able to make notes on paper copies is the way they best learn. Again, it means the information is accessible in an offline format. It is easy for us to wonder why people want to print web pages, however, our job is often to make content accessible &mdash; in the best format for our visitors. If that best format is printed to paper, then who are we to argue?</p>

<h4 id="why-would-this-page-be-printed">Why Would This Page Be Printed?</h4>

<p>A good question to ask when deciding on the content to include or hide in the print stylesheet is, “Why is the user printing this page?” Well, maybe there&rsquo;s a recipe they&rsquo;d like to follow while cooking in the kitchen or take along with them when shopping to buy ingredients. Or they&rsquo;d like to print out a confirmation page after purchasing a ticket as proof of booking. Or perhaps they&rsquo;d like a receipt or invoice to be printed (or printed to PDF) in order to store it in the accounts either as paper or electronically.</p>

<p>Considering the use of the printed document can help you to produce a print version of your content that is most useful in the context in which the user is in when referring to that print-out.</p>

<h3 id="workflow">Workflow</h3>

<p>Once we have decided to include print styles in our CSS, we need to add them to our workflow to ensure that when we make changes to the layout we also include those changes in the print version.</p>

<h4 id="adding-print-styles-to-a-page">Adding Print Styles To A Page</h4>

<p>To enable a “print stylesheet” what we are doing is telling the browser what these CSS rules are for when the document is printed. One method of doing this is to link an additional stylesheet by using the <code>&lt;link&gt;</code> element.</p>

<pre><code class="language-markup">&lt;link media="print" href="print.css"&gt;
</code></pre>
 

<p>This method does keep your print styles separate from everything else which you might consider to be tidier, however, that has downsides.</p>

<p>The linked stylesheet creates an additional request to the server. In addition, that nice, neat separation of print styles from other styles can have a downside. While you may take care to update the separate styles before going live, the stylesheet may find itself suffering due to being out of sight and therefore out of mind &mdash; ultimately becoming useless as features are added to the site but not reflected in the print styles.</p>

<p>The alternate method for including print styles is to use <code>@media</code> in the same way that you includes CSS for certain breakpoints in your responsive design. This method keeps all of the CSS together for a feature. Styles for narrow to wide breakpoints, and styles for print. Alongside Feature Queries with <code>@supports</code>, this encourages a way of development that ensures that all of the CSS for a design feature is kept and maintained together.</p>

<pre><code class="language-css">@media print {
    
}</code></pre>

<h4 id="overwriting-screen-css-or-creating-separate-rules">Overwriting Screen CSS Or Creating Separate Rules</h4>

<p>Much of the time you are likely to find that the CSS you use for the screen display works for print with a few small adjustments. Therefore you only need to write CSS for print, for changes to that basic CSS. You might overwrite a font size, or family, yet leave other elements in the CSS alone.</p>

<p>If you really want to have completely separate styles for print and start with a blank slate then you will need to wrap the rest of your site styles in a Media Query with the screen keyword.</p>

<pre><code class="language-css">@media screen {
    
}</code></pre>

<p>On that note, if you are using Media Queries for your Responsive Design, then you may have written them for screen.</p>

<pre><code class="language-css">@media screen and (min-width: 500px) {
    
}</code></pre>

<p>If you want these styles to be used when printing, then you should remove the <code>screen</code> keyword. In practice, however, I often find that if I work “mobile first” the single column mobile layout is a really good starting point for my print layout. By having the media queries that bring in the more complex layouts for screen only, I have far less overwriting of styles to do for print.</p>

<h4 id="add-your-print-styles-to-your-pattern-libraries-and-style-guides">Add Your Print Styles To Your Pattern Libraries And Style Guides</h4>

<p>To help ensure that your print styles are seen as an integral part of the site design, add them to your style guide or pattern library for the site if you have one. That way there is always a reminder that the print styles exist, and that any new pattern created will need to have an equivalent print version. In this way, you are giving the print styles visibility as a first-class citizen of your design system.</p>

<h3 id="basics-of-css-for-print">Basics Of CSS For Print</h3>

<p>When it comes to creating the CSS for print, there are three things you are likely to find yourself doing. You will want to hide, and not display content which is irrelevant when printed. You may also want to add content to make a print version more useful. You might also want to adjust fonts or other elements of your page to optimize them for print. Let’s take a look at these techniques.</p>

<h4 id="hiding-content">Hiding Content</h4>

<p>In CSS the method to hide content and also prevent generation of boxes is to use the display property with a value of <code>none</code>.</p>

<pre><code class="language-css">.box {
  display: none;
}</code></pre>

<p>Using <code>display: none</code> will collapse the element and all of its child elements. Therefore, if you have an image gallery marked up as a list, all you would need to do to hide this when printed is to set <code>display: none</code> on the <code>ul</code>.</p>

<p>Things that you might want to hide are images which would be unnecessary when printed, navigation, advertising panels and areas of the page which display links to related content and so on. Referring back to why a user might print the page can help you to decide what to remove.</p>

<h4 id="inserting-content">Inserting Content</h4>


  <div id="sponsors-article" data-impression="true" class="c-promo-box c-promo-box--ad sponsors hidden" data-audience="non-subscriber" data-remove="true"></div>



<p>There might be some content that makes sense to display when the page is printed. You could have some content set to <code>display: none</code> in a screen stylesheet and show it in your print stylesheet. Additionally, however, you can use CSS to expose content not normally output to the screen. A good example of this would be the URL of a link in the document. In your screen document, a link would normally show the link text which can then be clicked to visit that new page or external website. When printed links cannot be followed, however, it might be useful if the reader could see the URL in case they wished to visit the link at a later time.</p>

<p>We achieve this by using CSS Generated Content. Generated Content gives you a way to insert content into your document via CSS. When printing, this becomes very useful.</p>

<p>You can insert a simple text string into your document. The next example targets the element with a class of <code>wrapper</code> and inserts before it the string, “Please see www.mysite.com for the latest version of this information.”</p>

<pre><code class="language-css">.wrapper::after {
  content: "Please see www.mysite.com for the latest version of this information.";
}</code></pre>

<p>You can insert things that already exist in the document however, an example would be the content of the link <code>href</code>. We add Generated Content after each instance of <code>a</code> with an attribute of <code>href</code> and the content we insert is the value of the <code>href</code> attribute - which will be the link.</p>

<pre><code class="language-css">a[href]:after {
  content: " (" attr(href) ")";
}</code></pre>

<p>You could use the newer CSS <code>:not</code> selector to exclude internal links if you wished.</p>

<pre><code class="language-css">a[href^="http"]:not([href*="example.com"]):after {
  content: " (" attr(href) ")";
}</code></pre>

<p>There are some other useful tips like this in the article, “”, written by Manuel Matuzovic.</p>

<h3 id="advanced-print-styling">Advanced Print Styling</h3>

<p>If your printed version fits neatly onto one page then you should be able to create a print stylesheet relatively simply by using the techniques of the last section. However, once you have something which prints onto multiple pages (and particularly if it contains elements such as tables or figures), you may find that items break onto new pages in a suboptimal manner. You may also want to control things about the page itself, e.g. changing the margin size.</p>

<p>CSS does have a way to do these things, however, as we will see, browser support is patchy.</p>

<h4 id="paged-media">Paged Media</h4>

<p>The CSS Paged Media Specification opens with the following description of its role.</p>

<blockquote>“This CSS module specifies how pages are generated and laid out to hold fragmented content in a paged presentation. It adds functionality for controlling page margins, page size and orientation, and headers and footers, and extends generated content to enable page numbering and running headers/footers.”</blockquote>

<p>The screen is <em>continuous media</em>; if there is more content, we scroll to see it. There is no concept of it being broken up into individual pages. As soon as we are printing we output to a fixed size page, described in the specification as <em>paged media</em>. The Paged Media specification doesn’t deal with how content is fragmented between pages, we will get to that later. Instead, it looks at the features of the pages themselves.</p>

<p>We need a way to target an individual page, and we do this by using the <code>@page</code> rule. This is used much like a regular selector, in that we target <code>@page</code> and then write CSS to be used by the page. A simple example would be to change the margin on all of the pages created when you print your document.</p>

<pre><code class="language-css">@page {
  margin: 20px;
}</code></pre>

<p>You can target specific pages with <code>:left</code> and <code>:right</code> spread pseudo-class selectors. The first page can be targeted with the <code>:first</code> pseudo-class selector and blank pages caused by page breaks can be selected with <code>:blank</code>. For example, to set a top margin only on the first page:</p>

<pre><code class="language-css">@page :first {
  margin-top: 250pt;
}</code></pre>

<p>To set a larger margin on the right side of a left-hand page and the left side of a right-hand page:</p>

<pre><code class="language-css">@page :left {
  margin-right: 200pt;
}
    
@page :right {
  margin-left: 200pt;
}</code></pre>

<p>The specification defines being able to insert content into the margins created, however, no browser appears to support this feature. I describe this in my article about creating stylesheets for use with print-specific user agents, .</p>




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




<h3 id="css-fragmentation">CSS Fragmentation</h3>

<p>Where the Paged Media module deals with the page boxes themselves, the  details how content breaks between <em>fragmentainers</em>. A fragmentainer (or <em>fragment container</em>) is a container which contains a portion of a fragmented flow. This is a flow which, when it gets to a point where it would overflow, breaks into a new container.</p>

<p>The contexts in which you will encounter fragmentation currently are in paged media, therefore when printing, and also when using Multiple-column layout and your content breaks between column boxes. The Fragmentation specification defines various rules for breaking, CSS properties that give you some control over how content breaks into new fragments, in these contexts. It also defines how content breaks in the CSS Regions specification, although this isn’t something usable cross-browser right now.</p>

<p>And, speaking of browsers, fragmentation is a bit of a mess in terms of support at the moment. The  for each property on MDN seem to be accurate as to support, however testing use of these properties carefully will be required.</p>

<h4 id="older-properties-from-css2">Older Properties From CSS2</h4>

<p>In addition to the <code>break-*</code> properties from CSS Fragmentation Level 3, we have <code>page-break-*</code> properties which came from CSS2. In spec terms, these have been superseded by the newer <code>break-*</code> properties, as these are more generic and can be used in the different contexts breaking happens. There isn’t much difference between a page and a multicol break. However, in terms of browser support, there is better browser support for the older properties. This means you may well need to use those at the current time to control breaking. Browsers that implement the newer properties are to alias the older ones rather than drop them.</p>

<p>In the examples that follow, I shall show both the new property and the old one where it exists.</p>

<h4 id="break-before-amp-break-after"><code>break-before</code> &amp; <code>break-after</code></h4>

<p>These properties deal with breaks between boxes, and accept the following values, with the initial value being auto. The final four values do not apply to paged media, instead being for multicol and regions.</p>

<ul>
<li><code>auto</code></li>
<li><code>avoid</code></li>
<li><code>avoid-page</code></li>
<li><code>page</code></li>
<li><code>left</code></li>
<li><code>right</code></li>
<li><code>recto</code></li>
<li><code>verso</code></li>
<li><code>avoid-column</code></li>
<li><code>column</code></li>
<li><code>avoid-region</code></li>
<li><code>region</code></li>
</ul>

<p>The older properties of <code>page-break-before</code> and <code>page-break-after</code> accept a smaller range of values.</p>

<ul>
<li><code>auto</code></li>
<li><code>always</code></li>
<li><code>avoid</code></li>
<li><code>left</code></li>
<li><code>right</code></li>
<li><code>inherit</code></li>
</ul>

<p>To always cause a page break before an <code>h2</code> element, you would use the following:</p>

<pre><code class="language-css">h2 {
  break-before: page;
}</code></pre>

<p>To avoid a paragraph being detached from the heading immediately preceding it:</p>

<pre><code class="language-css">h2, h3 {
  break-after: avoid-page;
}</code></pre>

<p>The older <code>page-break-*</code> property to always cause a page break before an <code>h2</code>:</p>

<pre><code class="language-css">h2 {
  page-break-before: always;
}</code></pre>

<p>To avoid a paragraph being detached from the heading immediately preceding it:</p>

<pre><code class="language-css">h2, h3{
  page-break-after: avoid;
}</code></pre>

<p>On MDN find information and usage examples for the properties:</p>

<ul>
<li></li>
<li></li>
<li></li>
<li></li>
</ul>

<h4 id="break-inside"><code>break-inside</code></h4>

<p>This property controls breaks inside boxes and accepts the values:</p>

<ul>
<li><code>auto</code></li>
<li><code>avoid</code></li>
<li><code>avoid-page</code></li>
<li><code>avoid-column</code></li>
<li><code>avoid-region</code></li>
</ul>

<p>As with the previous two properties, there is an aliased <code>page-break-inside</code> from CSS2, which accepts the values:</p>

<ul>
<li><code>auto</code></li>
<li><code>avoid</code></li>
<li><code>inherit</code></li>
</ul>

<p>For example, perhaps you have a <code>figure</code> or a <code>table</code> and you don’t want a half of it to end up on one page and the other half on another page.</p>

<pre><code class="language-css">figure {
  break-inside: avoid;
}</code></pre>

<p>And when using the older property:</p>

<pre><code class="language-css">figure {
  page-break-inside: avoid;
}</code></pre>

<p>On MDN:</p>

<ul>
<li></li>
<li></li>
</ul>

<h4 id="orphans-and-widows">Orphans And Widows</h4>

<p>The Fragmentation specification also defines the properties <code>orphans</code> and <code>widows</code>. The <code>orphans</code> property defines how many lines can be left at the bottom of the first page when content such as a paragraph is broken between two pages. The <code>widows</code> property defines how many lines may be left at the top of the second page.</p>

<p>Therefore, in order to prevent ending up with a single line at the end of a page and a single line at the top the next page, you can use the following:</p>

<pre><code class="language-css">p {
  orphans: 2;
  widows: 2;
}</code></pre>

<p>The <code>widows</code> and <code>orphans</code> properties are well supported (the missing browser implementation being Firefox).</p>

<p>On MDN:</p>

<ul>
<li></li>
<li></li>
</ul>

<h4 id="box-decoration-break"><code>box-decoration-break</code></h4>

<p>The final property defined in the Fragmentation module is <code>box-decoration-break</code>. This property deals with whether borders, margins, and padding break or wrap the content. The values it accepts are:</p>

<ul>
<li><code>slice</code></li>
<li><code>clone</code></li>
</ul>

<p>For example, if my content area has a 10-pixel grey border and I print the content, then the default way that this will print is that the border will continue onto each page, however, it will only wrap at the end of the content. So we get a break before going to the next page and continuing.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/46c6f4fb-6ee2-4325-8cd1-1145ec034ff8/box-decoration-break-no-support.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/46c6f4fb-6ee2-4325-8cd1-1145ec034ff8/box-decoration-break-no-support.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/46c6f4fb-6ee2-4325-8cd1-1145ec034ff8/box-decoration-break-no-support.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/46c6f4fb-6ee2-4325-8cd1-1145ec034ff8/box-decoration-break-no-support.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/46c6f4fb-6ee2-4325-8cd1-1145ec034ff8/box-decoration-break-no-support.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/46c6f4fb-6ee2-4325-8cd1-1145ec034ff8/box-decoration-break-no-support.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/46c6f4fb-6ee2-4325-8cd1-1145ec034ff8/box-decoration-break-no-support.png"
			sizes="100vw"
			alt="The border does not wrap each page and so breaks between pages"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The border does not wrap each page and so breaks between pages
		</figcaption>
	
</figure>


<p>If I use <code>box-decoration-break: clone</code>, the border and any padding and margin will complete on each page, thus giving each page a grey border.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a17e21f8-41a9-43e1-9b32-692e0930f3dc/box-decoration-break-support.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a17e21f8-41a9-43e1-9b32-692e0930f3dc/box-decoration-break-support.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a17e21f8-41a9-43e1-9b32-692e0930f3dc/box-decoration-break-support.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a17e21f8-41a9-43e1-9b32-692e0930f3dc/box-decoration-break-support.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a17e21f8-41a9-43e1-9b32-692e0930f3dc/box-decoration-break-support.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a17e21f8-41a9-43e1-9b32-692e0930f3dc/box-decoration-break-support.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a17e21f8-41a9-43e1-9b32-692e0930f3dc/box-decoration-break-support.png"
			sizes="100vw"
			alt="The border wraps each individual page"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The border wraps each individual page
		</figcaption>
	
</figure>


<p>Currently, this only works for Paged Media in Firefox, and you can find out more about .</p>

<h3 id="browser-support">Browser Support</h3>

<p>As already mentioned, browser support is patchy for Paged Media and Fragmentation. Where Fragmentation is concerned, an additional issue is that breaking has to be specified and implemented for each layout method. If you were hoping to use Flexbox or CSS Grid in print stylesheets, you will probably be disappointed. You can check out the Chrome bugs for .</p>

<p>The best suggestion I can give right now is to keep your print stylesheets reasonably simple. Add fragmentation properties &mdash; including both the old <code>page-break-*</code> properties as well as the new properties. However, accept that these may well not work in all browsers. And, if you find lack of browser support frustrating, raise these issues with browsers or vote for already raised issues. Fragmentation, in particular, should be treated as a suggestion rather than a command, even where it is supported. It would be possible to be so specific about where and when you want things to break that it is almost impossible to lay out the pages. You should assume that sometimes you may get suboptimal breaking.</p>

<h3 id="testing-print-stylesheets">Testing Print Stylesheets</h3>

<p>Testing print stylesheets can be something of a bore, typically requiring using print preview or printing to a PDF repeatedly. However, browser DevTools have made this a little easier for us. Both Chrome and Firefox have a way to view the print styles only.</p>

<h4 id="firefox">Firefox</h4>

<p>Open the Developer Toolbar then type <code>media emulate print</code> at the prompt.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8a3828ba-4c66-437f-936c-ae7fcec857fc/print-styles-firefox.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8a3828ba-4c66-437f-936c-ae7fcec857fc/print-styles-firefox.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8a3828ba-4c66-437f-936c-ae7fcec857fc/print-styles-firefox.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8a3828ba-4c66-437f-936c-ae7fcec857fc/print-styles-firefox.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8a3828ba-4c66-437f-936c-ae7fcec857fc/print-styles-firefox.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8a3828ba-4c66-437f-936c-ae7fcec857fc/print-styles-firefox.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8a3828ba-4c66-437f-936c-ae7fcec857fc/print-styles-firefox.png"
			sizes="100vw"
			alt="Typing media emulate print"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Emulating print styles in Firefox
		</figcaption>
	
</figure>


<h4 id="chrome">Chrome</h4>

<p>Open DevTools, click on the three dots icon and then select “More Tools” and “Rendering”. You can then select print under Emulate CSS Media.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fa670aab-ce26-4b4d-af38-bcde0ee32534/print-styles-chrome.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fa670aab-ce26-4b4d-af38-bcde0ee32534/print-styles-chrome.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fa670aab-ce26-4b4d-af38-bcde0ee32534/print-styles-chrome.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fa670aab-ce26-4b4d-af38-bcde0ee32534/print-styles-chrome.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fa670aab-ce26-4b4d-af38-bcde0ee32534/print-styles-chrome.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fa670aab-ce26-4b4d-af38-bcde0ee32534/print-styles-chrome.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fa670aab-ce26-4b4d-af38-bcde0ee32534/print-styles-chrome.png"
			sizes="100vw"
			alt="Chrome DevTools emulate print media"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Emulating print styles in Chrome
		</figcaption>
	
</figure>


<p>This will only be helpful in testing changes to the CSS layout, hidden or generated content. It can’t help you with fragmentation &mdash; you will need to print or print to PDF for that. However, it will save you a few round trips to the printer and can help you check as you develop new parts of the site that you are still hiding and showing the correct things.</p>

<h3 id="what-to-do-when-a-print-stylesheet-isn-t-enough">What To Do When A Print Stylesheet Isn’t Enough</h3>

<p>In an ideal world, browsers would have implemented more of the Paged Media specification when printing direct from the browser, and fragmentation would be more thoroughly implemented in a consistent way. It is certainly worth raising the bugs that you find when printing from the browser with the browsers concerned. If we don’t request these things are fixed, they will remain low priority to be fixed.</p>

<p>If you do need to have a high level of print support and want to use CSS, then currently you would need to use a print-specific User Agent, such as .”</p>

<p>Prince is also available to install on your server in order to generate nicely printed documents using CSS on the web, however, it comes at a high price. An alternative is a server like  who offer an API on top of the Prince rendering engine.</p>

<p>There are open-source HTML- and CSS-to-PDF generators such as  which seems to have its own implementation and supports slightly different features, although is not in any way as full-featured as something like Prince.</p>

<p>You will find more information about user agents for print on the  site.</p>

<h4 id="other-resources">Other Resources</h4>

<p>Due to the fact that printing from CSS has really moved on very little in the past few years, many older resources on Smashing Magazine and elsewhere are still valid. Some additional tips and tricks can be found in the following resources. If you have discovered a useful print workflow or technical tip, then add it to the comments below.</p>

<ul>
<li>“,” Manuel Matuzovic, UX Collective</li>
<li>“,” Chris Coyier, CSS-Tricks</li>
<li>“,” Andreas Hecht, Noupe</li>
<li>“,” Christian Krammer, Smashing Magazine</li>
<li>“,” Dudley Storey, Smashing Magazine</li>
</ul>




<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(il)</span>
</div>


</div>



              </article>
            </body>
          </html>
---------------
<h1 id="#title_1" >2、文章： 数字化转型指南（第一部分）</h1>
Philippe Assouline
[http://www.infoq.com/cn/articles/Digital-Transformation-Guide-1?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/Digital-Transformation-Guide-1?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/Digital-Transformation-Guide-1/zh/smallimage/BOLTS-1524751812192-1525173295320.jpg"/><p>从传统来看，实现伟大的数字化商业愿景需要在运营、技术和人力方面进行艰苦卓绝的努力。 本文介绍了一种框架，可轻松将数字化业务目标转化为数字化策略，然后可以对其进行定价和建模，以便进行影响分析和创造经济价值。
</p> <i>By Philippe Assouline</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_2" >3、文章： PaaS将吞噬云计算？Kubernetes的市场冲击波</h1>
徐川
[http://www.infoq.com/cn/articles/kubernetes-and-pass?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/kubernetes-and-pass?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/kubernetes-and-pass/zh/smallimage/book-cover-leadership-agility-1516406885241-1525178124580.jpg"/><p>2017年是Kubernetes的胜利之年，很多人还不明白这意味着什么。但如果看一下云计算业界的动向，你会发现，Kubernetes的影响正在扩散。在本文中我将分享我们的发现，并试图说服你：基于容器+Kubernetes的新型PaaS将会成为云计算的主流。</p> <i>By 徐川</i>
---------------
<h1 id="#title_3" >4、文章： 如何用游戏引擎改造Hybrid App？</h1>
胡骁杰
[http://www.infoq.com/cn/articles/how-to-reform-hybrid-app-using-game-engine?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/how-to-reform-hybrid-app-using-game-engine?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/how-to-reform-hybrid-app-using-game-engine/zh/smallimage/LOGO-1511697970292-1525173742880.jpeg"/><p>在移动设备上，Hybrid 混合开发的性能问题一直为人诟病，对它的各种优化、hack 层出不穷，但你听说过用游戏引擎来优化 Hybrid 性能的吗？这次我们的 GMTC 邀请到了腾讯高级工程师潘伟洲分享《基于 Cocos 的高性能跨平台应用开发方案》，我们提前对他进行了采访，了解了一些技术细节，分享给大家。</p> <i>By 胡骁杰</i>
---------------
<h1 id="#title_4" >5、揭秘Apple、Google等千亿市值企业的架构设计</h1>
David
[http://www.infoq.com/cn/news/2018/05/trillion-architecture?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/05/trillion-architecture?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>毫无疑问，中国互联网企业技术水平与硅谷的整体差距越来越小，某些方面甚至有赶超之处。但在大数据&人工智能风口下，无论国内还是国外，都可以看出大企业的技术实践难度都在加大，于是大量失败和教训默默重复和隐藏在各企业内，国内外成功的经验难以传播、借鉴和参考。

</p> <i>By David</i>
---------------