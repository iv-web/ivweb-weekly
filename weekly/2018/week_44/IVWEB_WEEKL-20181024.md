## 文章索引
1、 <a href="#1splicing-htmls-dna-with-css-attribute-selectors" >Splicing HTML’s DNA With CSS Attribute Selectors</a><br/>
2、 <a href="#2文章-micronaut教程如何使用基于jvm的框架构建微服务" >文章： Micronaut教程：如何使用基于JVM的框架构建微服务</a><br/>
3、 <a href="#3官宣警告月活431亿的新浪微博如何应对流量激增" >官宣警告！月活4.31亿的新浪微博，如何应对流量激增？</a><br/>
4、 <a href="#4十周后62的php网站将运行在一个不受支持的php版本上" >十周后，62%的PHP网站将运行在一个不受支持的PHP版本上</a><br/><h1 id="#title_0" >1、Splicing HTML’s DNA With CSS Attribute Selectors</h1>
John Rhea
[https://www.smashingmagazine.com/2018/10/attribute-selectors-splicing-html-dna-css/](https://www.smashingmagazine.com/2018/10/attribute-selectors-splicing-html-dna-css/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/10/attribute-selectors-splicing-html-dna-css/" />
              <title>Splicing HTML’s DNA With CSS Attribute Selectors</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>Splicing HTML’s DNA With CSS Attribute Selectors</h1>
                  
                    
                    <address>John Rhea</address>
                  
                  <time datetime="2018-10-23T14:00:11&#43;02:00" class="op-published">2018-10-23T14:00:11+02:00</time>
                  <time datetime="2018-10-23T12:09:02&#43;00:00" class="op-modified">2018-10-23T12:09:02+00:00</time>
                </header>
                <p>For most of my career, attribute selectors have been more magic than science. I’d stare, gobsmacked, at the CSS for outputting a link in a print style sheet, understanding nothing. I’d dutifully copy, and paste it into my print stylesheet then run off to put out whatever project was the largest burning trash heap.</p>

<p>But you don’t have to stare slack-jawed at CSS attribute selectors anymore. By the end of this article, you’ll use them to run diagnostics on your site, fix otherwise unsolvable problems, and generate technologic experiences so advanced they feel like magic. You may think I’m promising too much and you’re right, but once you understand the power of attribute selectors, you might feel like exaggerating yourself.</p>

<p>On the most basic level, you put an HTML attribute in square brackets and call it an attribute selector like so:</p>

<pre><code class="language-bash">[href] {
   color: chartreuse;
}
</code></pre>

<p>The text of any element that has an <code>href</code> and doesn’t have a more specific selector will now magically turn chartreuse. Attribute selector specificity is the same as classes.</p>

<p><strong>Note</strong>: <em>For more on the cage match that is CSS specificity, you can read “”.</em></p>

<p>But you can do far more with attribute selectors. Just like your DNA, they have built-in logic to help you choose all kinds of attribute combinations and values. Instead of only exact matching the way a tag, class, or id selector would, they can match any attribute and even string values within attributes.</p>



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




<h3>Attribute Selection</h3>

<p>Attribute selectors can live on their own or be more specific, i.e. if you need to select all <code>div</code> tags that had a <code>title</code> attribute.</p>

<pre><code class="language-bash">div[title]
</code></pre>

<p>But you could also select the children of divs that have a title by doing the following:</p>

<pre><code class="language-bash">div [title]
</code></pre>

<p>To be clear, no space between them means the attribute is on the same element (just like an element and class without a space), and a space between them means a descendant selector, i.e. selecting the element’s children who have the attribute.</p>

<p>You can get far more granular in how you select attributes including the values of attributes.</p>

<pre><code class="language-bash">div[title="dna"]
</code></pre>

<p>The above selects all divs with an exact title of “dna”. A title of “dna is awesome” or “dnamutation” wouldn’t be selected, though there are selector algorithms that handle each of those cases (and more). We’ll get to those soon.</p>

<p><strong>Note</strong>: <em>Quotation marks are not required in attribute selectors in most cases, but I will use them because I believe it increases clarity and ensures edge cases work appropriately.</em></p>

<p>If you wanted to select “dna” out of a space separated list like “my beautiful dna” or “mutating dna is fun!” you can add a tilde or “squiggly,” as I like to call it, in front of the equal sign.</p>

<pre><code class="language-bash">div[title~="dna"]
</code></pre>

<p>You can select titles such as “dontblamemeblamemydna” or “his-stupidity-is-from-upbringing-not-dna” then you can use the dollar sign $ to match the end of a title.</p>

<pre><code class="language-bash">[title$="dna"]
</code></pre>

<p>To match the front of an attribute value such as titles of “dnamutants” or “dna-splicing-for-all” use a caret.</p>

<pre><code class="language-bash">[title^="dna"]
</code></pre>

<p>While having an exact match is helpful it might be too tight of a selection, and the caret front match might be too wide for your needs. For instance, you might not want to select a title of “genealogy”, but still select both “gene” and “gene-data”. The exclamation point or “bang,” as I like to call it, is just that, it does an exact match, but includes when the exact match is followed by a dash.</p>

<pre><code class="language-bash">[title!="gene"]
</code></pre>

<p>To be clear, though this construction often means “not equal” in many programming languages, in CSS attribute selectors it is an exact match plus an exact match at the beginning of the value followed by a dash.</p>

<p>Lastly, there’s a full search attribute operator that will match any substring.</p>

<pre><code class="language-bash">[title*="dna"]
</code></pre>

<p>But use it wisely as the above will match “I-like-my-dna-like-my-meat-rare” as well as “edna”, “kidnapping”, and “echidnas” (something Edna really shouldn’t do.)</p>

<div class="sponsors__wide-place"></div>




<p>What makes these attribute selectors even more powerful is that they’re stackable &mdash; allowing you to select elements with multiple matching factors.</p>

<p>But you need to find the <code>a</code> tag that has a title and has a class ending in “genes”? Here’s how:</p>

<pre><code class="language-bash">a[title][class$="genes"]
</code></pre>

<p>Not only can you select the attributes of an HTML element you can also print their mutated genes using pseudo-“science” (meaning pseudo-elements and the content declaration).</p>

<pre class="break-out"><code class="language-bash">&lt;span class="joke" title="Gene Editing!"&gt;What’s the first thing a biotech journalist does after finishing the first draft of an article?&lt;/span&gt;
</code></pre>

<pre><code class="language-css">.joke:hover:after {
   content: "Answer:" attr(title);
   display: block;
}
</code></pre>

<p>The code above will show the answer to one of the worst jokes ever written on hover (yes, I wrote it myself, and, yes, calling it a “joke” is being generous).</p>

<p>The last thing to know is that you can add a flag to make the attribute searches case insensitive. You add an <code>i</code> before the closing square bracket.</p>

<pre><code class="language-bash">[title*="DNA" i]
</code></pre>

<p>And thus it would match “dna”, “DNA”, “dnA”, and any other variation.</p>

<p>The only downside to this is that the <code>i</code> only works in Firefox, Chrome, Safari, Opera and a smattering of mobile browsers.</p>

<p>Now that we’ve seen how to select with attribute selectors, let’s look at some use cases. I’ve divided them into two categories: <em>General Uses</em> and <em>Diagnostics</em>.</p>

<h3>General Uses</h3>

<h4>Style By Input Type</h4>

<p>You can style input types differently, e.g. email vs. phone.</p>

<pre><code class="language-bash">input[type="email"] {
   color: papayawhip;
}
input[type="tel"] {
   color: thistle;
}
</code></pre>

<h4>Display Telephone Links</h4>

<p>You can hide a phone number at certain sizes and display a phone link instead to make calling easier on a phone.</p>

<pre><code class="language-bash">span.phone {
   display: none;
}
a[href^="tel"] {
   display: block;
}
</code></pre>

<h4>Internal vs. External Links, Secure vs. Insecure</h4>

<p>You can treat internal and external links differently and style secure links differently from insecure links.</p>

<pre><code class="language-bash">a[href^="http"]{
   color: bisque;
}
a:not([href^="http"]) {
  color: darksalmon;
}
 
a[href^="http://"]:after {
   content: url(unlock-icon.svg);
}
a[href^="https://"]:after {
   content: url(lock-icon.svg);
}
</code></pre>

<div class="sponsors__wide-place"></div>




<h4>Download Icons</h4>

<p>One attribute HTML5 gave us was “download” which tells the browser to, you guessed it, download that file rather than trying to open it. This is useful for PDFs and DOCs you want people to access but don&rsquo;t want them to open right now. It also makes the workflow for downloading lots of files in a row easier. The downside to the <code>download</code> attribute is that there’s no default visual that distinguishes it from a more traditional link. Often this is what you want, but when it’s not, you can do something like the below.</p>

<pre><code class="language-bash">a[download]:after { 
   content: url(download-arrow.svg);
}
</code></pre>

<p>You could also communicate file types with different icons like PDF vs. DOCX vs. ODF, and so on.</p>

<pre><code class="language-bash">a[href$="pdf"]:after {
   content: url(pdf-icon.svg);
}
a[href$="docx"]:after {
   content: url(docx-icon.svg);
}
a[href$="odf"]:after {
   content: url(open-office-icon.svg);
}
</code></pre>

<p>You could also make sure that those icons were only on downloadable links by stacking the attribute selector.</p>

<pre><code class="language-bash">a[download][href$="pdf"]:after {
   content: url(pdf-icon.svg);
}
</code></pre>

<h4>Override Or Reapply Obsolete/Deprecated Code</h4>

<p>We’ve all come across old sites that have outdated code, but sometimes updating the code isn’t worth the time it’d take to do it on six thousand pages. You might need to override or even reapply a style implemented as an attribute before HTML5.</p>

<pre class="break-out"><code class="language-bash">&lt;div bgcolor="#000000" color="#FFFFFF"&gt;Old, holey genes&lt;/div&gt;
 
div[bgcolor="#000000"] { /*override*/
   background-color: #222222 !important;
}
div[color="#FFFFFF"] { /*reapply*/
   color: #FFFFFF;
}
</code></pre>

<h4>Override Specific Inline Styles</h4>

<p>Sometimes you’ll come across inline styles that are gumming up the works, but they’re coming from code outside your control. It should be said if you can change them that would be ideal, but if you can’t, here’s a workaround.</p>

<p><strong>Note</strong>: <em>This works best if you know the exact property and value you want to override, and if you want it overridden wherever it appears.</em></p>

<p>For this example, the element’s margin is set in pixels, but it needs to be expanded and set in <code>em</code>s so that the element can re-adjust properly if the user changes the default font size.</p>

<pre class="break-out"><code class="language-bash">&lt;div style="color: #222222; margin: 8px; background-color: #EFEFEF;"Teenage Mutant Ninja Myrtle&lt;/div&gt;
 
div[style*="margin: 8px"] {
   margin: 1em !important;
}
</code></pre>

<p><strong>Note</strong>: <em>This approach should be used with extreme caution as if you ever need to override this style you’ll fall into an</em> <code>!important</code> <em>war and kittens will die.</em></p>

<h4>Showing File Types</h4>

<p>The list of acceptable files for a file input is invisible by default. Typically, we’d use a pseudo element for exposing them and, though you can’t do pseudo elements on most <code>input</code> tags (or at all in Firefox or Edge), you can use them on file inputs.</p>

<pre><code class="language-bash">&lt;input type="file" accept="pdf,doc,docx"&gt;
 
[accept] {
   content: "Acceptable file types: " attr(accept);
}
</code></pre>

<h4>HTML Accordion Menu</h4>

<p>The not-well-publicized <code>details</code> and <code>summary</code> tag duo are a way to do expandable/accordion menus with just HTML. Details wrap both the <code>summary</code> tag and the content you want to display when the accordion is open. Clicking on the summary expands the <code>detail</code> tag and adds an open attribute. The open attribute makes it easy to style an open <code>details</code> tag differently from a closed <code>details</code> tag.</p>

<pre><code class="language-bash">&lt;details&gt;
  &lt;summary&gt;List of Genes&lt;/summary&gt;
    Roddenberry
    Hackman
    Wilder
    Kelly
    Luen Yang
    Simmons
&lt;/details&gt;
</code></pre>

<pre><code class="language-css">details[open] {
   background-color: hotpink;
}
</code></pre>

<h4>Printing Links</h4>

<p>Showing URLs in print styles led me down this road to understanding attribute selectors. You should know how to construct it yourself now. You simply select all <code>a</code> tags with an <code>href</code>, add a pseudo-element, and print them using <code>attr()</code> and <code>content</code>.</p>

<pre><code class="language-bash">a[href]:after {
   content: " (" attr(href) ") ";
}
</code></pre>

<h4>Custom Tooltips</h4>

<p>Creating custom tooltips is fun and easy with attribute selectors (okay, fun if you’re a nerd like me, but easy either way).</p>

<p><strong>Note</strong>: <em>This code should get you in the general vicinity, but may need some tweaks to the spacing, padding, and color scheme depending on your site&rsquo;s environment and whether you have better taste than me or not.</em></p>

<pre><code class="language-css">[title] {
  position: relative;
  display: block;
}
[title]:hover:after {
  content: attr(title);
  color: hotpink;
  background-color: slateblue;
  display: block;
  padding: .225em .35em;
  position: absolute;
  right: -5px;
  bottom: -5px;
}
</code></pre>

<h4>AccessKeys</h4>

<p>One of the great things about the web is that it provides many different options for accessing information. One rarely used attribute is the ability to set an <code>accesskey</code> so that that item can be accessed directly through a key combination and the letter set by <code>accesskey</code> (the exact key combination depends on the browser). But there’s no easy way to know what keys have been set on a website.</p>

<p>The following code will show those keys on <code>:focus</code>. I don’t use on <code>hover</code> because most of the time people who need the <code>accesskey</code> are those who have trouble using a mouse. You can add that as a second option, but be sure it isn’t the only option.</p>

<pre><code class="language-css">a[accesskey]:focus:after {
   content: " AccessKey: " attr(accesskey);
}
</code></pre>

<h3>Diagnostics</h3>

<p>These options are for helping you identify issues either during the build process or locally while trying to fix issues. Putting these on your production site will make errors stick out to your users.</p>

<h4>Audio Without Controls</h4>

<p>I don’t use the <code>audio</code> tag too often, but when I do use it, I often forget to include the <code>controls</code> attribute. The result: nothing is shown. If you’re working in Firefox, this code can help you suss out if you’ve got an audio element hiding or if syntax or some other issue is preventing it from appearing (it only works in Firefox).</p>

<pre><code class="language-css">audio:not([controls]) {
  width: 100px;
  height: 20px;
  background-color: chartreuse;
  display: block;
}
</code></pre>

<h4>No Alt Text</h4>

<p>Images without alt text are a logistics and accessibility nightmare. They’re hard to find by just looking at the page, but if you add this they’ll pop right out.</p>

<p><strong>Note</strong>: <em>I use</em> <code>outline</code> <em>instead of</em> <code>border</code> <em>because borders could add to the element’s width and mess up the layout.</em> <code>outline</code> <em>does not add width.</em></p>

<pre><code class="language-bash">img:not([alt]) { /* no alt attribute */ 
  outline: 2em solid chartreuse; 
}
img[alt=""] { /* alt attribute is blank */ 
  outline: 2em solid cadetblue; 
}
</code></pre>

<h4>Asynchronous Javascript Files</h4>

<p>Web pages can be a conglomerate of content management systems and plugins and frameworks and code that Ted (sitting three cubicles over) wrote on vacation because the site was down and he fears your boss. Figuring out what JavaScript loads asynchronously and what doesn’t can help you focus on where to enhance page performance.</p>

<pre><code class="language-javascript">script[src]:not([async]) {
  display: block;
  width: 100%;
  height: 1em;
  background-color: red;
}
script:after {
  content: attr(src);
}
</code></pre>

<h4>Javascript Event Elements</h4>

<p>You can also highlight elements that have a JavaScript event attribute to refactor them into your JavaScript file. I’ve focused on the <code>OnMouseOver</code> attribute here, but it works for any of the JavaScript event attributes.</p>

<pre><code class="language-javascript">[OnMouseOver] {
   color: burlywood;
}
[OnMouseOver]:after {
   content: "JS: " attr(OnMouseOver);
}
</code></pre>

<h4>Hidden Items</h4>

<p>If you need to see where your hidden elements or hidden inputs live you can show them with:</p>

<pre><code class="language-bash">[hidden], [type="hidden"] {
  display: block;
}
</code></pre>

<p>But with all these amazing capabilities you think there must be a catch. Surely attribute selectors must only work while flagged in Chrome or in the nightly builds of Fiery Foxes on the Edge of a Safari. This is just too good to be true. And, unfortunately, there is a catch.</p>

<p>If you want to work with attribute selectors in that most beloved of browsers &mdash; that is, IE6 &mdash; you won’t be able to. (It’s okay; let the tears fall. No judgments.) Pretty much everywhere else you’re good to go. Attribute selectors are part of the CSS 2.1 spec and thus have been in browsers for the better part of a decade.</p>

<p>And so these selectors should no longer be magical to you but revealed as a sufficiently advanced technology. They are more science than magic, and now that you know their deepest secrets, it’s up to you. Go forth and work mystifying wonders of science upon the web.</p>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(dm, ra, yk, il)</span>
</div>


              </article>
            </body>
          </html>
---------------
<h1 id="#title_1" >2、文章： Micronaut教程：如何使用基于JVM的框架构建微服务</h1>
Sergio del Amo Caballero
[http://www.infoq.com/cn/articles/micronaut-tutorial-microservices-jvm?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/micronaut-tutorial-microservices-jvm?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/micronaut-tutorial-microservices-jvm/zh/smallimage/micronaut-tutorial-microservices-jvm-s-1538571826519-1539964752783.jpeg"/><p>Micronaut是一种基于jvm的现代化全栈框架，用于构建模块化且易于测试的微服务应用程序。在本教程中，你将使用该框架创建三个使用Java、Kotlin和Groovy编写的微服务。</p> <i>By Sergio del Amo Caballero</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_2" >3、官宣警告！月活4.31亿的新浪微博，如何应对流量激增？</h1>
刘然
[http://www.infoq.com/cn/news/2018/10/sina-weibo-manage-vast-traffic?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/10/sina-weibo-manage-vast-traffic?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>提升运维自动化的自研占比是非常重要的，它决定了后续自动化所能达到的高度。我们建设自动化运维平台的目标是：更快的响应、更省的方案、更高的效率！要通过人工智能技术，解放运维的双手，拥抱美好未来！</p> <i>By 刘然</i>
---------------
<h1 id="#title_3" >4、十周后，62%的PHP网站将运行在一个不受支持的PHP版本上</h1>
Catalin Cimpanu
[http://www.infoq.com/cn/news/2018/10/PHP-site-run-unsupported-version?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/10/PHP-site-run-unsupported-version?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>根据W3Techs的统计数据，目前约有78.9％的网站使用PHP开发。但是，PHP 5.6.x的安全支持将在2018年12月31日正式停止，这标志着对古老的PHP 5.x分支版本的支持都将结束。</p> <i>By Catalin Cimpanu</i> <i> Translated by 无明</i>
---------------