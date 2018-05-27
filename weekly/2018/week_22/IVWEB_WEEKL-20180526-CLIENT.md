## 文章索引
1、 <a href="#1getting-started-with-css-layout" >Getting Started With CSS Layout</a><br/>
2、 <a href="#2google力推的那些前端技术最近有何进展" >Google力推的那些前端技术，最近有何进展？</a><br/>
3、 <a href="#3微众银行张开翔开源联盟链的挑战与应对" >微众银行张开翔：开源联盟链的挑战与应对</a><br/>
4、 <a href="#4创新工场成立ai公司创新奇智融资过亿元" >创新工场成立AI公司创新奇智，融资过亿元</a><br/>
5、 <a href="#5迅雷发布现象级区块链-生态-30-时代来临" >迅雷发布现象级区块链 生态 3.0 时代来临</a><br/>
6、 <a href="#6每周分享第-6-期" >每周分享第 6 期</a><br/>
7、 <a href="#7goodbye-smoosh-arrayprototypeflatten-is-now-flat" >Goodbye 'smoosh', Array.prototype.flatten is now 'flat'</a><br/><h1 id="#title_0" >1、Getting Started With CSS Layout</h1>
Rachel Andrew
[https://www.smashingmagazine.com/2018/05/guide-css-layout/](https://www.smashingmagazine.com/2018/05/guide-css-layout/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/05/guide-css-layout/" />
              <title>Getting Started With CSS Layout</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>Getting Started With CSS Layout</h1>
                  
                    
                    <address>Rachel Andrew</address>
                  
                  <time datetime="2018-05-25T12:00:19&#43;02:00" class="op-published">2018-05-25T12:00:19+02:00</time>
                  <time datetime="2018-05-25T20:06:31&#43;00:00" class="op-modified">2018-05-25T20:06:31+00:00</time>
                </header>
                

<p>Over the past couple of years, CSS Layout has dramatically changed as well as the way we develop the front end of our sites. We now have a real choice in terms of the layout methods we use in CSS to develop our sites, which means we often need to make a choice as to which approach to take. In this article, I will run through the various layout methods that you have available to you by explaining the basics of how they are used and what they are used for.</p>

<p>This guide is for you if you are fairly new to CSS and wondering what the best way to approach layout is, but also if you are an experienced developer from elsewhere in the stack who wants to make sure your understanding of layout today is up to date. I have not tried to fully document each layout method here, as that would have created a book and not an article. Instead, I am giving an overview of what is available to you, with plenty of links to find out more.</p>

<h3 id="normal-flow">Normal Flow</h3>

<p>If you take an HTML webpage which has no CSS applied to change the layout, the elements will display in <strong>normal flow</strong>. In normal flow, boxes are displayed one after another based on the Writing Mode of the document. This means that if you have a horizontal writing mode, one in which sentences run left to right or right to left, normal flow will display the boxes of block level elements one after the other vertically down the page.</p>



<aside class="product-panel product-panel__tilted product-panel--book" data-audience="non-subscriber">
    <div class="container product-panel--book__container">
      <div class="panel__description panel__description--book">
    <p>What if there was a web conference without... slides? Meet <strong>. June <span class="small-caps">26–27</span>. With everything from live designing to live performance audits.</p>
      <a href="http://smashed.by/confpanelspeakers" class="btn btn--green btn--large">
        Check the speakers&nbsp;→
      </a>
      </div>
      <div class="panel__image panel__image--book">
        <a href="http://smashed.by/confpanelspeakers" class="books__book__image">
        <div class="books__book__img">
          <img src="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5a0383cf-197a-49b9-975a-9d1f02c1ace9/dan-hov.png" alt="SmashingConf Toronto 2018, with Dan Mall, Sara Soueidan, Lea Verou and many others." width="310" height="400">
        </div>
      </a>
      </div>
    </div>
  </aside>





<div class="c-garfield-the-cat">


<p>If you are in a vertical writing mode, then sentences run vertically so normal flow would lay the blocks out horizontally.</p>

<figure>
<figcaption>Block and Inline Directions change with Writing Mode</figcaption></figure>

<p>Normal flow is where you begin with any layout: when you create a CSS Layout, you are taking the blocks and causing them to do something other than normal flow.</p>

<h4 id="structure-your-document-to-take-advantage-of-normal-flow">Structure Your Document To Take Advantage Of Normal Flow</h4>

<p>You can take advantage of normal flow by ensuring your document starts out in a well-structured manner. Imagine if &mdash; instead of this concept of normal flow &mdash; the browser piled all your boxes up in the corner on top of each other until you created a layout. That would mean you would have to place every single thing on the page. Instead, the browser displays our content in an immediately readable way.</p>

<p>If your CSS fails to load, the user can still read the content, and users who don’t get CSS at all (e.g. someone using a screen reader) will have the content delivered to them in the order it is in the document. This makes it important from an accessibility point of view that your HTML document starts life in a good order; however, it will also make your life easier as a web developer. If your content is in the order a user would expect to read it, you won’t need to make massive changes to layout to get it into the right place. With newer layout methods you may be surprised how little you have to do.</p>

<p>Therefore, before thinking about layout, think about document structure and the order you would want your content to be read in from the top of the document to the bottom.</p>

<h4 id="moving-away-from-normal-flow">Moving Away From Normal Flow</h4>

<p>Once we have a well-structured document, we need to decide how to take that and turn it into our desired layout. This will involve moving away from normal flow, for parts of our document. We have a whole set of layout methods to use.  The first method we will take a look at is <code>float</code>, as floats are an excellent demonstration of what it is to take an element out of normal flow.</p>

<h3 id="floats">Floats</h3>

<p>Floats are used to shift a box to the left or right, allowing content to display wrapped around it.</p>

<p>In order to float an item, use the CSS property <code>float</code> and a value of left or right. The default value of float is none.</p>

<pre><code class="language-css">.item {
    float: left;
}</code></pre>

<p>It is worth noting that when you float an item and text wraps around it, that what happens is the line boxes of that content are shortened. If you float an item and the following box containing your text has a background color applied, you can see that this background color will then run underneath the floated item.</p>

<figure>
<figcaption>The background color on the content runs under the float</figcaption></figure>

<p>As you are shortening the line boxes in order to make space between the float and the wrapping text, you must set a margin on the floated item. A margin on the text would just move the text in from the edge of the container. For an image floated left, you would add a margin to the right and bottom assuming that you want the image flush with the top and left of the container.</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="BxbgoQ"
   data-user="rachelandrew"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<h4 id="clearing-floats">Clearing Floats</h4>

<p>Once you have floated an element, all of the following elements will wrap around that floated element until they wrap underneath and normal flow continues. If you want to prevent that, you need to clear the float.</p>

<p>On the element that you want to begin displaying after the float, add the property <code>clear</code> with a value of left to indicate clearing an item floated left, right to clear an item floated right, or both to clear any floats.</p>

<pre><code class="language-css">.clear {
    clear: both;
}</code></pre>

<p>The above method works if you want an element to start after a float. It won’t help if you find yourself in a situation where you have a floated item inside a box, with some text alongside. If the text is shorter than the floated item, the box will be drawn underneath the content and ignore the float. As we have already learned, floats shorten the line boxes, the rest of the layout continues in normal flow.</p>

<figure>
<figcaption>The box around the text does not clear the float</figcaption></figure>

<p>To prevent this situation we need to clear something inside the box. We could add an empty element and set that to clear all. This involves sticking empty divs into our document which isn’t ideal and may not be possible if your page is generated by a CMS. So instead, the typical clearing floats method is what is known as a clear fix hack. This method works by adding CSS Generated Content, and setting that to clear both.</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="jxJjje"
   data-user="rachelandrew"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<h5 id="the-block-formatting-context">The Block Formatting Context</h5>

<p>Another way to clear floats inside a box is to invoke a Block Formatting Context (BFC) on the container. A Block Formatting Context contains everything inside it, which would include floated items which can no longer poke out the bottom of the box. There are a few ways to force a BFC, the most common when clearing floats is to set the overflow property to have a value other than the default visible.</p>

<pre><code class="language-css">.container {
    overflow: auto;
}</code></pre>

<p>Using overflow in this way will generally work, however, in certain situations you could end up with clipped shadows or unwanted scrollbars on the item. It also can look a little confusing in your stylesheet: Did you set overflow because you <em>wanted</em> scrollbars or just to gain this clearing ability?</p>

<p>To make intent clearer and prevent the creation of a BFC causing unwanted side effects, you can use <code>flow-root</code> as a value of the <code>display</code> property. The only thing that <code>display: flow-root</code> does is to create a BFC, thus clearing your floats with no other problems caused.</p>

<pre><code class="language-css">.container {
    display: flow-root;
}</code></pre>

<h4 id="legacy-usage-of-floats">Legacy Usage Of Floats</h4>

<p>Until the arrival of newer layout methods floats were used to create column layouts, this technique worked by giving a set of items a width and setting them to float up next to one another. Careful management of the percentage size of these floated boxes could create a grid effect.</p>

<p>I would not suggest starting a new design now and using this method. However, it will remain in existing sites for many years to come. Therefore, if you come across a design where almost everything seems to be floated, this is the technique in use.</p>

<h4 id="resources-and-further-reading-on-floats-and-clearing-floats">Resources And Further Reading On Floats And Clearing Floats</h4>

<ul>
<li>“,” Chris Coyier, CSS-Tricks</li>
<li>“,” CSS: Cascading Style Sheets, MDN web docs</li>
<li>“,” CSS: Cascading Style Sheets, MDN web docs</li>
<li>“,” Rachel Andrew, Smashing Magazine</li>
</ul>

<h3 id="positioning">Positioning</h3>

<p>To remove an element from normal flow or shift it around from its place in normal flow, you can use the <code>position</code> property in CSS. When in normal flow, elements have a <code>position</code> of <code>static</code>. The items display one after the other in the Block dimension and if you scroll the page they scroll with it.</p>

<p>When changing the value of position you will typically be also using offset values to move the box around from a particular reference point. The reference point used depends on the value of position you are using.</p>

<h4 id="relative-positioning">Relative Positioning</h4>

<p>If an item has <code>position: relative</code> then the reference point is the place it would normally be in normal flow. You can then use offset values for the properties <code>top</code>, <code>left</code>, <code>bottom</code> and <code>right</code> to move the box from where it would normally be displayed.</p>

<pre><code class="language-css">.item {
    position: relative;
    bottom: 50px;
}</code></pre>

<p>Note that other items on the page do not respond to the new position of your element. The place it was positioned in normal flow is reserved, therefore you need to manage any overlaps yourself.</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="MGxNwd"
   data-user="rachelandrew"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<h4 id="absolute-positioning">Absolute Positioning</h4>

<p>Set <code>position: absolute</code> on an item and it will be removed completely from normal flow. The space that was left for it will be removed. The item will then be positioned relative to its containing block which, unless it is nested inside another positioned element, will be the viewport.</p>

<p>Therefore, the first thing that will happen if you set <code>position: absolute</code> on an item is that it typically ends up stuck to the top and left of the viewport. You can then use offset values for the properties <code>top</code>, <code>left</code>, <code>bottom</code> and <code>right</code> to move the box from that position to where you want it to be.</p>

<pre><code class="language-css">.item {
    position: absolute;
    top: 20px;
    right: 20px;
}</code></pre>

<p>Often you don’t want the box positioned according to the viewport, but in reference to a containing element, it is inside. In which case you need to give that containing element a position value other than the default static.</p>

<p>As setting <code>position: relative</code> does not remove the item from normal flow, this is the usual choice. Give the parent element that you wish to set your offsets from <code>position: relative</code> and then offset the absolutely positioned block from the boundaries of that element.</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="zjbgvx"
   data-user="rachelandrew"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<h4 id="fixed-positioning">Fixed Positioning</h4>

<p>Something with <code>position: fixed</code> will be positioned in most cases relative to the viewport, and removed from document flow so that no space is reserved for it. When the page is scrolled, the fixed element remains in position relative to the viewport as the rest of the content in normal flow scrolls as usual.</p>

<pre><code class="language-css">.item {
    position: fixed;
    top: 20px;
    left: 100px;
}</code></pre>

<p>This can be helpful to enable a fixed navigation panel which stays on screen, e.g. while the content scrolls. As with other positioning values, you may cause overlaps when doing this so you should take care that all the content can be read and doesn’t end up behind a fixed item.</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="xjBvLE"
   data-user="rachelandrew"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<p>To position a fixed item other than relative to the viewport, you need to have a containing element with one of the <code>transform</code>, <code>perspective</code>, or <code>filter</code> properties set to something other than their default value of <code>none</code>. In this case, that element will become the containing block and your offsets with relate to that block rather than the viewport.</p>

<h4 id="sticky-positioning">Sticky Positioning</h4>

<p>Setting <code>position: sticky</code> on an element will cause the element to scroll with the document just as it would in normal flow, however, once it reaches a certain point in relation to the viewport (using the usual offsets) it “sticks” and starts to act like <code>position: fixed</code>. This is a newer value and is less well supported in browsers than other methods, however, it falls back to just scrolling with the page os is a value nicely used as an enhancement without causing problems if it is not supported.</p>

<pre><code class="language-css">.item {
    position: sticky;
    top: 0;
}</code></pre>

<p>This is how to create the popular effect of a navigation bar scrolling with the content and then stopping at the top of the viewport to stay onscreen as you scroll the content.</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="LmawOy"
   data-user="rachelandrew"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<h4 id="resources-and-further-reading-on-positioning">Resources And Further Reading On Positioning</h4>

<ul>
<li>“,” MDN Learning Area, MDN web docs, Mozilla</li>
<li>“,” Chris Coyier, CSS-Tricks</li>
<li>“,” Browser support information for sticky positioning, caniuse</li>
</ul>

<h3 id="flex-layout">Flex Layout</h3>

<p>Flexible Box Layout (Flexbox) is a layout method designed for one-dimensional layout. One-dimensional means that you wish to lay out your content in a row, or as a column. To turn your element into a flex layout, you use the <code>display</code> property with a value of <code>flex</code>.</p>

<pre><code class="language-css">.container {
    display: flex;
}</code></pre>

<p>The direct children of that element become flex items, they will lay out as a row, aligned to the start edge in the inline direction.</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="RyObov"
   data-user="rachelandrew"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<h4 id="the-axes-of-flexbox">The Axes Of Flexbox</h4>

<p>In the above example, I described out items as being laid out aligned to the start edge of our row in the inline direction, rather than describing them as being aligned to the left. Our items are laid out in a row because the default value of the <code>flex-direction</code> property is <code>row</code>, this creates a row in the inline direction, the direction along which sentences run. As we are working in English, a left-to-right language, the start of a row is on the left and so our items start there. The value of <code>flex-direction</code> thus defines the <strong>main axis</strong> of Flexbox.</p>

<p>The cross axis, therefore, runs across the main axis at right angles. If your flex-direction is <code>row</code> and your items are displayed in the inline direction, your cross axis runs in the Block direction. If your <code>flex-direction</code> is <code>column</code> so the items are running in the Block direction then your cross axis is along the row.</p>

<p>If you get used to thinking in terms of main and cross axis when working with Flexbox, it will make many things easier.</p>

<h4 id="direction-and-order">Direction And Order</h4>

<p>Flexbox gives you the ability to change the direction of items on the main axis by using a <code>flex-direction</code> value of <code>row-reverse</code> or <code>column-reverse</code>.</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="zjXONE"
   data-user="rachelandrew"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<p>You can also change the order of individual flex items with the <code>order</code> property. However, you should take great care when doing so as this can cause a problem for any user who is navigating using the keyboard rather than a mouse or touchscreen as the tab order of the document will follow the order the content is in the source. See the section below on Visual and Document Order for more details.</p>

<h4 id="the-flex-properties">The Flex Properties</h4>

<p>The flex properties are how to control the ratios of flex items along the main axis. The three properties are:</p>

<ul>
<li><code>flex-grow</code></li>
<li><code>flex-shrink</code></li>
<li><code>flex-basis</code></li>
</ul>

<p>These are usually used in their shorthand form of the <code>flex</code> property, the first value being <code>flex-grow</code>, the second <code>flex-shrink</code> and the third <code>flex-basis</code>.</p>

<pre><code class="language-css">.item {
    flex: 1 1 200px;
}</code></pre>

<p>The value of <code>flex-basis</code> gives a size that the item will have before any growing or shrinking takes place. In the above example, that size is 200 pixels, so we would give each item 200 pixels of space. It is unlikely that our container will neatly divide by 200 pixels and so there will be space leftover or not enough space for all of the items if they each have 200 pixels. The <code>flex-grow</code> and <code>flex-shrink</code> properties allow us to control what happens to the items if there is too much or not enough space for them.</p>


  <div id="sponsors-article" data-impression="true" class="c-promo-box c-promo-box--ad sponsors hidden" data-audience="non-subscriber" data-remove="true"></div>



<p>If <code>flex-grow</code> is set to any positive value, then the item is allowed to grow to take up space. Therefore, in our example above, after giving each item 200 pixels, any extra space will be shared out between the items.</p>

<p>If <code>flex-shrink</code> is set to a positive value, then the item can shrink in the situation where an overflow would happen if all of the items were given their <code>flex-basis</code>. If there was not enough space in the container in our example, each item would shrink an equal amount to reduce until all the items fit in the container.</p>

<p>The <code>flex-grow</code> and <code>flex-shrink</code> values can be any positive value. An item with a greater <code>flex-grow</code> value will be given more of the available space in proportion when growing, and with a greater <code>flex-shrink</code> value more will be removed when shrinking.</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="rvbaRM"
   data-user="rachelandrew"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<p>Understanding the way that these flex properties work is really the key to understanding Flexbox, and the resources listed below will give you all of the detail. However, consider using Flexbox when you have a bunch of things that you want to stretch and squish into a container in one dimension. If you find yourself trying to line things up in rows and columns, you want a Grid, and in that case Flexbox probably isn’t the tool for the job.</p>

<h4 id="resources-and-further-reading-for-flex-layout">Resources And Further Reading For Flex Layout</h4>

<ul>
<li>“,” A complete guide to the specification, MDN web docs, Mozilla</li>
<li>“,” Chris Coyier, CSS-Tricks</li>
<li>“,” A game for learning Flexbox</li>
<li>“,” A community curated list of browser bugs relating to Flexbox</li>
</ul>

<h3 id="grid-layout">Grid Layout</h3>

<p>CSS Grid Layout was designed as a two-dimensional layout method. Two-dimensional means that you wish to lay your content out in rows and columns. As with Flexbox, Grid Layout is a value of <code>display</code> and so to start using Grid you should start with <code>display: grid</code> on your container, and then set up some columns and/or rows using the <code>grid-template-columns</code> and <code>grid-template-rows</code> properties.</p>

<pre><code class="language-css">.container {
    display: grid;
    grid-template-columns: 200px 200px 200px;
    grid-template-rows: 200px 200px;
}</code></pre>

<p>The above CSS would create a fixed size grid, with completely fixed column and row tracks. This probably isn’t what you want on the web, and Grid has you well covered. The default for any track is <code>auto</code>, which can generally be thought of as “big enough for the content.” If we didn’t create any row tracks, then rows would be created for us to take any content added, and these would be <code>auto</code> sized. A common pattern is to specify column tracks but allow Grid to create rows as required.</p>

<p>While you can set up your column and row tracks using any length unit or a percentage, you can also use the new <code>fr</code> unit, a unit created for Grid Layout. The <code>fr</code> unit is a flex unit, and denotes a share of the available space in the grid container.</p>

<p>Grid can distribute space for you; you don’t need to calculate percentages to ensure things fit into a container. In the example below, we are creating columns using the <code>fr</code> unit and allowing tracks to create automatically. We are also using <code>grid-gap</code> to space out our tracks (see the section on Box Alignment for more details about gaps and grid layout).</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="erorKm"
   data-user="rachelandrew"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<p>As with Flexbox and <code>flex-grow</code> or <code>flex-shrink</code>, the <code>fr</code> unit deals with sharing out available space. A higher <code>fr</code> value for one track means it gets more of the available space in proportion. You can also mix <code>fr</code> units and absolute lengths. The space needed for the lengths will be subtracted from the available space before working out the <code>fr</code> units.</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="MGRGBW"
   data-user="rachelandrew"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<h4 id="grid-terminology">Grid Terminology</h4>

<p>A Grid always has two axes: the Inline Axis runs in the direction that words are laid out on the page and the Block Axis in the direction that blocks are laid out.</p>

<p>The Grid Container is the element that you have set <code>display: grid</code> on. You then have Grid Lines, created by the column and row <strong>tracks</strong> you have specified when using <code>grid-template-columns</code> and <code>grid-template-rows</code>. The smallest unit on the grid (between four intersecting lines) is known as a Grid Cell, while a collection of Grid Cells that make up a complete rectangle is called a Grid Area.</p>

<figure>
<figcaption>Grid Lines run between each track of the grid.</figcaption></figure>

<figure>
<figcaption>Grid Tracks are between any two lines</figcaption></figure>

<figure>
<figcaption>Grid cells are the smallest unit on the grid, a Grid Area is one or more cells together making a rectangular area</figcaption></figure>

<h4 id="grid-auto-placement">Grid Auto-Placement</h4>

<p>As soon as you create a Grid, the direct children of your grid container begin to lay themselves out, one in each cell of the grid. They do this according to the grid auto-placement rules. These rules ensure that each item is placed in an empty cell avoiding overlapping items.</p>

<p>Any direct child of the grid container which you have not given a position to will be placed according to the auto-placement rules. In the below example, I have caused every third item to span two-row tracks, while still being auto-placed in terms of the start line.</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="ZoZoqY"
   data-user="rachelandrew"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<h4 id="basic-line-based-positioning">Basic Line-Based Positioning</h4>

<p>The simplest way to position items on the Grid is with line-based positioning, giving the item rules to tell it to span from one line of the grid to another. For example, if I have a grid with three column tracks and two-row tracks, I can place an item from column line 1 to column line 3, and row line 1 to row line 3. It will then cover four grid cells in total, spanning two column tracks and two column rows.</p>

<pre><code class="language-css">.item {
    grid-column-start: 1;
    grid-column-end: 3;
    grid-row-start: 1;
    grid-row-end: 3;
}</code></pre>

<p>These properties can be represented as a shorthand, <code>grid-column</code> and <code>grid-row</code> with the first value being <em>start</em> and the second <em>end</em>.</p>

<pre><code class="language-css">.item {
    grid-column: 1 / 3;
    grid-row: 1 / 3;
}</code></pre>

<p>Grid Items can occupy the same cells, enabling the creation of designs with overlapping content. Items stack up in the usual way that content stacks on the web, with items lowering down the source appearing on the top of other items. Still, you can use <code>z-index</code> to control this.</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="mLgLZj"
   data-user="rachelandrew"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<h4 id="positioning-with-named-areas">Positioning With Named Areas</h4>

<p>You can also position items on your grid by using Named Areas. To use this method you give each item a name, and then describe the layout as the value of the <code>grid-template-areas</code> property.</p>

<pre><code class="language-css">.item1 {
    grid-area: a;
}

.item2 {
    grid-area: b;
}

.item3 {
    grid-area: c;
}

.container {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr 1fr;
    grid-template-areas: 
     "a a b b"
     "a a c c";
}</code></pre>

<p>There are a few rules to remember when using this method. If you want an item to span multiple cells then you should repeat the name. Areas need to form a complete rectangle, no L-shaped or Tetris pieces allowed! The grid must be complete &mdash; every cell must be filled. If you want to leave white space then fill that cell with a <code>.</code>. For example, in the below CSS I am leaving the bottom right corner empty.</p>

<pre><code class="language-css">.container {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr 1fr;
    grid-template-areas: 
     "a a b b"
     "a a c .";
}</code></pre>

<p>This is a nice way to work as anyone looking at the CSS can see exactly how the layout will work.</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="bMJKeX"
   data-user="rachelandrew"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<h4 id="resources-and-further-reading-for-grid-layout">Resources And Further Reading For Grid Layout</h4>

<p>There is much more to CSS Grid Layout than this quick overview has shared, and the resources below will help you to learn the specification. Components and your full page layout alike can be grids, choose Grid Layout if you have a two-dimensional layout to create &mdash; no matter how large or small.</p>

<ul>
<li>“,” Web technology for developers, MDN web docs, Mozilla</li>
<li>“,” Everything you need to learn CSS Grid Layout, Rachel Andrew</li>
<li>“,” A fun interactive game to test and improve your CSS skills</li>
<li>“,” Jen Simmons, YouTube</li>
</ul>

<p>I’ve also written a number of articles here on Smashing Magazine that can help you dig into various Grid concepts:</p>

<ul>
<li>“”</li>
<li>“”</li>
<li>“”</li>
<li>“”</li>
<li>“”</li>
</ul>

<h3 id="visual-and-document-order">Visual And Document Order</h3>

<p>At the beginning of this article, I suggested that you start with your document in an order that makes sense read top to bottom, as this would be helpful both for accessibility and in terms of the way that CSS layout works. From our short introduction to Flexbox and CSS Grid, you can see that it would be possible to move things around quite dramatically away from that order. This has the potential to cause a problem.</p>

<p>Browsers will follow the document source for any non-visual use of the document. Therefore, a screen reader will read out the document order and anyone using a keyboard to navigate will tab through the document in the order it is in the source and not the display order. Many screen readers users are not completely blind, and so may be using the screen reader alongside being able to see where they are in the document. For both of these cases, a display which is jumbled up when compared to the source could cause a very confusing situation indeed.</p>

<p>Be very aware when you are moving elements way from the order they are in the source. If you find yourself rearranging the order of items in CSS, should you really be going back and reorganizing your document? Test to see if you can still tab around your document and the visual order make sense.</p>

<h4 id="resources-and-further-reading-for-visual-and-document-order">Resources And Further Reading For Visual And Document Order</h4>

<ul>
<li>“,” Web technology for developers, MDN web docs, Mozilla</li>
<li>“,” Adrian Roselli</li>
<li>“,” Code Things, Tink</li>
<li>“,” Alastair Campbell</li>
</ul>

<h3 id="box-generation">Box Generation</h3>

<p>Everything you put on a web page creates a box, and everything in this article describes how you can use CSS to layout those boxes in your design, however, in certain circumstances you may not want to create a box at all. There are two values of the <code>display</code> property that deal with situations where you do not want boxes.</p>

<h4 id="do-not-generate-the-box-or-contents-display-none">Do Not Generate The Box Or Contents (<code>display: none</code>)</h4>

<p>If you want the element and all of the content of that element, including any child items, to not be generated you can use <code>display: none</code>. The element will now not be displayed, and no space will be reserved for where it would have been.</p>

<pre><code class="language-css">.item {
    display: none;
}
</code></pre>

<h4 id="do-not-generate-this-element-but-generate-any-child-elements-display-contents">Do Not Generate This Element, But Generate Any Child Elements (<code>display: contents</code>)</h4>

<p>A newer value of <code>display</code> is <code>display: contents</code>. Apply <code>display: contents</code> to an element and the box for that element will not be generated but any children will be generated as normal. This can be helpful if you want indirect child elements to become part of a flex or grid layout.</p>

<p>In the example below, the first flex item contains two nested children, yet as it is set to <code>display: contents</code> its box is not rented and the children display as if they were the direct child and become flex items. Remove <code>display: contents</code> from that element to see how the layout changes.</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="GdLBRR"
   data-user="rachelandrew"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<h4 id="resources-and-further-reading-for-box-generation">Resources And Further Reading For Box Generation</h4>

<ul>
<li>“,” Rachel Andrew</li>
<li>,” Ire Aderinokun,</li>
<li>,” Browser support information, caniuse</li>
</ul>

<h3 id="alignment">Alignment</h3>

<p>Alignment has been something of a tricky subject on the web until recently, with very limited ways to properly align items inside boxes. This is changing with the Box Alignment Module, which currently you will use when controlling alignment in Grid and Flex containers. In the future, other layout methods will also implement these alignment properties. The list of alignment properties detailed in the Box Alignment specification is as follows:</p>

<ul>
<li><code>justify-content</code></li>
<li><code>align-content</code></li>
<li><code>place-content</code></li>
<li><code>justify-items</code></li>
<li><code>align-items</code></li>
<li><code>place-items</code></li>
<li><code>justify-self</code></li>
<li><code>align-self</code></li>
<li><code>place-self</code></li>
<li><code>row-gap</code></li>
<li><code>column-gap</code></li>
<li><code>gap</code></li>
</ul>

<p>As layout models have different features, alignment works slightly differently depending on the layout model in use. Let’s take a look at how alignment works with some simple Grid and Flex Layouts.</p>

<p>The <code>align-items</code> and <code>justify-items</code> properties set the <code>align-self</code> and <code>justify-self</code> properties as a group. These properties align the items inside their Grid Area.</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="WJWKgd"
   data-user="rachelandrew"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<p>The <code>align-content</code> and <code>justify-content</code> properties align the grid tracks, where there is more space in the Grid Container than is needed to display the tracks.</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="mLgGym"
   data-user="rachelandrew"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<p>In Flexbox, <code>align-items</code> and <code>align-self</code> deal with alignment on the Cross Axis, while <code>justify-content</code> deals with space distribution on the main axis.</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="ZoZMQZ"
   data-user="rachelandrew"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<p>On the cross axis, you can use <code>align-content</code> where you have wrapped flex lines and additional space in the flex container.</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="QrPVjB"
   data-user="rachelandrew"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<p>See the resources for some links that discuss Box Alignment in detail across layout methods. It really is worth spending some time understanding how alignment works, as it will make working with Flexbox, Grid and future layout methods far easier.</p>

<h4 id="row-and-column-gaps">Row And Column Gaps</h4>

<p>A multiple-column layout has the <code>column-gap</code> property, and the Grid Layout spec had &mdash; until recently &mdash; the properties <code>grid-column-gap</code>, <code>grid-row-gap</code>, and <code>grid-gap</code>. These have now been removed from the Grid specification and added to Box Alignment. At the same time, the <code>grid-</code> prefixed properties were renamed to <code>column-gap</code>, <code>row-gap</code>, and <code>gap</code>. Browsers will alias the prefixed properties to the new renamed ones so you do not need to worry if you are using the better supported old names in your code right now.</p>

<p>The renaming means that these properties can be also applied to other layout methods, the obvious candidate being Flexbox. While no browser supports gaps in Flexbox at the moment, in future we should be able to use <code>column-gap</code> and <code>row-gap</code> to create space between flex items.</p>

<h4 id="resources-and-further-reading-for-alignment">Resources And Further Reading For Alignment</h4>

<ul>
<li>“,” CSS: Cascading Style Sheets, MDN web docs, Mozilla</li>
<li>“,” CSS Flexible Box Layout, MDN web docs, Mozilla</li>
<li>“,” CSS Grid Layout, MDN web docs, Mozilla</li>
<li>“,” Rachel Andrew, Smashing Magazine</li>
<li>“,” Rachel Andrew</li>
</ul>




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




<h3 id="multi-column-layout">Multi-Column Layout</h3>

<p>A multiple-column layout is a layout type that enables the creation of columns, such as you might find in a newspaper. A block is split into columns, and you read down a column in the block direction then return to the top of the next column. While reading content in this way is not always useful in a web context as people don’t want to have to scroll up and down to read, it can be a helpful way to display small amounts of content or to collapse down sets of checkboxes or other small UI elements.</p>

<p>A multiple-column layout can also be used to display sets of cards or products which have differing heights.</p>

<h4 id="setting-a-column-width">Setting A Column Width</h4>

<p>To set an optimal column width, and instruct the browser to display as many columns as possible at that width use the following CSS:</p>

<pre><code class="language-css">.container {
    column-width: 300px;
}</code></pre>

<p>This will create as many as 300 pixel columns as possible, any leftover space is shared between the columns. Therefore, unless your space divides into 300 pixels with no remainder, it is likely that your columns will be slightly wider than 300 pixels.</p>

<h4 id="setting-a-number-of-columns">Setting A Number Of Columns</h4>

<p>Instead of setting the width, you could set a number of columns using <code>column-count</code>. In this case, the browser will share the space between the number of columns you have asked for.</p>

<pre><code class="language-css">.container {
    column-count: 3;
}</code></pre>

<p>If you add both <code>column-width</code> and <code>column-count</code>, then the <code>column-count</code> property acts as a maximum. In the below code, columns will be added until there are three columns, at which point any extra space will be shared between those three columns even if there was enough space for an additional column.</p>

<pre><code class="language-css">.container {
    column-width: 300px;
    column-count: 3;
}</code></pre>

<h4 id="gaps-and-column-rules">Gaps And Column Rules</h4>

<p>You cannot add margins or padding to individual column boxes, to space out columns use the <code>column-gap</code> property. If you do not specify a <code>column-gap</code>, it will default to <code>1em</code> to prevent columns bumping up against each other. This is a different behavior to the way <code>column-gap</code> is specified for other layout methods, where it defaults to 0. You can use any length unit for your gap, including 0 if you want no gap at all.</p>

<p>The <code>column-rule</code> property gives you the ability to add a rule between two columns. It is a shorthand for <code>column-rule-width</code>, <code>column-rule-color</code>, and <code>column-rule-style</code>, and acts in the same way as <code>border</code>. Note that a rule does not take up any space of its own. It lays on top of the gap so to increase or decrease space between the rule and the content you need to increase or decrease the <code>column-gap</code>.</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="ELJdOQ"
   data-user="rachelandrew"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<h4 id="allowing-elements-to-span-columns">Allowing Elements To Span Columns</h4>

<p>You can span an element inside the multicol container across all of the columns using the <code>column-span</code> property on that element.</p>

<pre><code class="language-css">h3 {
    column-span: all;
}</code></pre>

<p>When a <code>column-span</code> happens, the multicol container essentially stops above the spanning element, therefore, the content forms into columns above the element and then remaining content forms a new set of column boxes below the spanning element.</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="gzyBQV"
   data-user="rachelandrew"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<p>You can only use <code>column-span: all</code> or <code>column-span: none</code>; it isn’t possible to span some of the columns. At the time of writing, Firefox does not support the <code>column-span</code> property.</p>

<h4 id="resources-and-further-reading-for-multiple-column-layout">Resources And Further Reading For Multiple-Column Layout</h4>

<ul>
<li>“,” CSS Multi-column Layout, MDN web docs, Mozilla</li>
</ul>

<h3 id="fragmentation">Fragmentation</h3>

<p>Multiple-Column Layout is an example of <em>fragmentation</em>. In this case, the content is broken into columns. It is, however, very similar to the way that content is broken into pages when printing. This process is dealt with by the Fragmentation specification, and this specification contains properties to help control the breaking of content.</p>

<p>For example, if you have laid out a set of cards using multicol and you want to make sure that a card never breaks in half, becoming split between two columns you can use the property <code>break-inside</code> with a value of <code>avoid</code>. Due to browser compatibility reasons, you will also want to use the legacy <code>page-break-inside</code> property as well.</p>

<pre><code class="language-css">.card {
    page-break-inside: avoid;
    break-inside: avoid;
}</code></pre>

<p>If you want to avoid a break directly after a heading, you can use the <code>break-after</code> property.</p>

<pre><code class="language-css">.container h2 {
    page-break-after: avoid;
    break-after: avoid;
}</code></pre>

<p>These properties can be used when preparing a print stylesheet and also in multicol. In the example below, I have three paragraphs in a multicol container that fragments into three columns. I have given <code>break-inside: avoid</code> to the <code>p</code> element meaning that the paragraphs end up one in each column (even if this makes the columns uneven).</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="wjZYOK"
   data-user="rachelandrew"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<h4 id="resources-and-further-reading-for-fragmentation">Resources And Further Reading For Fragmentation</h4>

<ul>
<li>“,” Rachel Andrew, Smashing Magazine</li>
<li>“,” QuirksMode.org</li>
</ul>

<h3 id="selecting-layout-types-how-to-choose">Selecting Layout Types: How To Choose?</h3>

<p>Most web pages will use a mixture of these layout types, and each spec defines exactly how they interact with each other. For example, you might have a Grid Layout in which some Grid Items are also Flex containers. Some of those flex containers might be a containing block for a positioned item or have an image floated inside. The specifications are written with an expectation that we will be mixing layout models, according to what is best for the content that we are laying out. In this guide, I have tried to give an overview of the basic way that each layout type behaves, in order to help you hone in on what is likely to be the best way to achieve a particular effect.</p>

<p>However, don’t be afraid to play around with different ways of creating the design you have in mind. There are fewer places than you might imagine where you should worry about your choices causing any real problem. Start with a good document structure, and take care that you are not disconnecting the visual display from that order. Much of the rest is just a case of testing that things work as you expect in your target browsers.</p>




<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(il)</span>
</div>


</div>




  <div id="sponsors-article-end" data-impression="true" class="c-promo-box c-promo-box--ad c-promo-box--wide sponsors hidden" data-audience="non-subscriber" data-remove="true"></div>



              </article>
            </body>
          </html>
---------------
<h1 id="#title_1" >2、Google力推的那些前端技术，最近有何进展？</h1>
覃云
[http://www.infoq.com/cn/news/2018/05/Google-arch-development?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/05/Google-arch-development?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Google I/O 2018已于上周落下帷幕，普通民众看的是新产品，开发者们关注的是新技术。透过这次大会，我们不难发现，Google已经从mobile first转向AI first，AI之后，就是移动和前端技术了，移动无非是Android P 和Flutter等，前端涵盖的技术从Web框架到Web工具，包括Angular、PWA、polymer、AMP等，下面让我来为大家捋一捋Google力推的这些前端技术最近都有哪些进展。</p> <i>By 覃云</i>
---------------
<h1 id="#title_2" >3、微众银行张开翔：开源联盟链的挑战与应对</h1>
金缕春
[http://www.infoq.com/cn/news/2018/05/challenge-response-open-source-a?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/05/challenge-response-open-source-a?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>“我们在面向区块链这个黑科技时，使命是让它在金融业务领域能发挥更大的作用。所以我们走的是技术研究、应用落地探索、社区运营三位一体互相结合的路线。” 作为微众银行的区块链首席架构师，张开翔在总结他的工作时表示，就是要让区块链这个既引人注目又充满了神秘感的黑科技变得明明白白。 做到这一点并不简单。目前大多数银行业金融机构采取的是将联盟链作为区块链技术运用的发展路径。2016 年 5 月，微众银行联合 20 多家机构发起成立了金融区块链合作联盟（深圳）（简称：金链盟），着力推动区块链技术研发和应用落地。 那么区块链技术将如何推动金融科技发展，联盟链面临哪些机遇和挑战，银行业在区块链技术探索和应用落地方面又有哪些经验？带着这些问题，我们和张开翔进行了一次深度访谈。</p> <i>By 金缕春</i>
---------------
<h1 id="#title_3" >4、创新工场成立AI公司创新奇智，融资过亿元</h1>
陈利鑫
[http://www.infoq.com/cn/news/2018/05/Innova-workshop-AI-innovate-100?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/05/Innova-workshop-AI-innovate-100?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>创新工场董事长兼CEO曾今说过：“未来五年，中国在人工智能领域将超过美国。”不管这一预言能否实现，创新工场对AI的热情一直不减。</p> <i>By 陈利鑫</i>
---------------
<h1 id="#title_4" >5、迅雷发布现象级区块链 生态 3.0 时代来临</h1>
金缕春
[http://www.infoq.com/cn/news/2018/05/xunlei-Block-chain-ecology-3-0?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/05/xunlei-Block-chain-ecology-3-0?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>帮助更多开发者快速接触并应用区块链，推动区块链应用落和帮助众多企业和开发者以更低的成本接入云计算。</p> <i>By 金缕春</i>
---------------
<h1 id="#title_5" >6、每周分享第 6 期</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2018/05/weekly-issue-6.html](http://www.ruanyifeng.com/blog/2018/05/weekly-issue-6.html)
<p>这里记录过去一周，我看到的值得分享的东西，每周五发布。</p>

        <p><img src="https://www.wangbase.com/blogimg/asset/201805/bg2018052501.jpg" alt="" title="" /></p>

<p>最近，我有一个行程，可能要去日本。我还没去过日本呢，听说日本人普遍听不懂英语，我又不会说日语，这可怎么办？</p>

<p>突然想到，"谷歌翻译"这个 APP 也许能解决语言问题。它有一个"对话实时翻译"功能，可以同时监听两种语言，听到中文就自动说出日语，听到日语就说出中文。我试了一下，翻译效果之好令人震惊，完全是真人发音，翻译非常准确。建议大家也装一个玩玩，亲身体验自己说出的话变成流利的日语，肯定能震撼到你。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201805/bg2019052502.jpg" alt="" title="" /></p>

<p>两个人同时对着手机说话，还是比较尴尬的，因此谷歌还推出了 Buds 蓝牙耳机。你说出的话通过耳机的话筒传入手机，让手机播放翻译好的版本给对方听。对方的回应被翻译以后，再通过耳机传给你。这样的话，对话可以始终是面对面。</p>

<p>看着这个玩意，我心想将来还需要苦学外语吗？很多人学了十年，口语还是结结巴巴，词不达意。照我说，那就别学了，大好青春干什么不好，何必用来背单词，反正以后人工智能可以帮你说外语。</p>

<h2>新闻</h2>

<p>1、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201805/bg2018052503.jpg" alt="" title="" /></p>

<p><img src="https://www.wangbase.com/blogimg/asset/201805/bg2018052504.jpg" alt="" title="" /></p>

<p>世界野生动物摄影大赛最近宣布，取消一位摄影师的获奖资格。因为他拍摄的《夜晚的食蚁兽》是假的，是用一只标本摆拍的。</p>

<p>2、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201805/bg2018052505.jpg" alt="" title="" /></p>

<p>4月份，我国首部高中教材《人工智能基础》出版。下个学期就将在首批试点高校投入使用。根据，这本教材包含下面的内容。</p>

<blockquote>
  <ol start='1'>
<li>总论：人工智能概述</li>
<li>经典图像分类（目明）</li>
<li>深度学习（目明）</li>
<li>音乐风格分类（耳聪）</li>
<li>相册聚类</li>
<li>自然语言理解（心灵）</li>
<li>生成模型（手巧）</li>
</ol>
</blockquote>

<p>如果真要学懂上面的内容，是不是意味着高中就必须掌握 Python 语言？</p>

<p>3、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201805/bg2018052506.jpg" alt="" title="" /></p>

<p>Boston Dynamics 公司发布了新的视频，机器人直接在不平整的草地上慢跑了起来，甚至还小小地示范了一下"立定跳"，跳过了一根挡道的圆木。</p>

<p>想想将来，马路上迎面走来的是一个机器人。或者罪犯逃跑，警方放出一个机器人在他后面追......我觉得，最大胆的想象力恐怕都无法想象，未来几十年后的人类社会将变成什么样。</p>

<p>4、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201805/bg2018052507.jpg" alt="" title="" /></p>

<p>这周看到一篇2010年的老文章，提醒了大家一个很容易忽略的问题：数字复印机内部的硬盘会保存复印的文件。</p>

<p>每当你复印了一份文件，文件就保存在硬盘上了。然后，其他人就可以从硬盘还原出你复印的内容。</p>

<p>5、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201805/bg2018052508.jpg" alt="" title="" /></p>

<p>庞培是古罗马被火山喷发毁灭的城市，火山岩浆覆盖了一切。当时有一匹马被岩浆包裹了，久而久之就形成了岩层里面的一个空腔。考古学家将石膏灌入空腔，结果就发现了这里原来有一匹马。</p>

<p>6、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201805/bg2018052509.jpg" alt="" title="" /></p>

<p>买过域名的人都知道，域名注册信息可以在网上查到（你的姓名、电话、地址），这叫 Whois 查询。如果不想被看到，就要花钱让注册商帮你藏起来。</p>

<p>但是，这违反即将在欧洲生效的 GDPR 法律，你凭什么泄露我的个人信息！有文章称，whois会进行重大改革（只有注册商才能看到），甚至废除。</p>

<p>7、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201805/bg2018052510.jpg" alt="" title="" /></p>

<p>一直以来，Windows 系统不内置 SSH 支持，导致登录服务器和其他 Linux 设备非常麻烦，必须安装客户端（比如 Putty）。现在，Windows 10 的最新版已经内置 OpenSSH 支持了，SSH 登录再也不是问题了。</p>

<h2>教程</h2>

<p>1、[文章] （英文）</p>

<p>分布式系统的基本概念和基本知识，这篇文章都谈到了。</p>

<blockquote>
  <p>什么是分布式系统？最简单的定义，分布式系统是一组计算机一起工作，对于最终用户只显示为一台计算机。这些机器具有共享状态，可以处理并发操作，如果其中一台机器发生故障，不会影响整个系统的正常运行。</p>
</blockquote>

<p>2、[教程] （英文）</p>

<p>一张网页的《C 语言的入门教程》，比较注重内存部分的讲解。写得不是很易读，但是还是可以看一下。</p>

<p>3、[教程] （英文）</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201805/bg2018052511.jpg" alt="" title="" /></p>

<p>本文介绍了17个据说改变了世界的数学公式。数了一下，我知道9个。</p>

<p>4、[文章] （英文）</p>

<p>代码还算简单，可以作为编译器的训练。</p>

<p>5、[文章] （英文）</p>

<p>这篇短文讨论了 SOA 架构（服务导向架构）和微服务架构的差异，为什么 SOA 会演变成微服务。</p>

<p>6、[文章] （中文）</p>

<p>我们经常听到 DNS 根域名服务有 13 台，那么是为什么呢？ 今天我们来深入了解下。</p>

<p>7、[PDF] （英文）</p>

<p>这是 Linus Torvalds 的硕士毕业论文，介绍 Linux 系统如何适配不同的硬件架构。这篇论文不涉及代码，只介绍一些概念性的东西，但也不是那么好懂，至少我没有完全看懂。对内核和操作系统感兴趣的朋友，可以读一下。</p>

<p>8、[文章] （英文）</p>

<p>ed 是 Unix 系统里面最古老的命令行编辑器，但是功能并不弱。这篇文章介绍了一个使用 ed 的简单实例。</p>

<p>9、[游戏] （英文）</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201805/bg2018052512.jpg" alt="" title="" /></p>

<p>通过吃豆子（PacMan）游戏学习 Vim 操作的命令行游戏。</p>

<h2>工具</h2>

<p>1、</p>

<p>类似于 GitHub 和 GitLab 的开源项目，用于个人架设 Git 代码托管服务，使用 Go 语言实现。</p>

<p>2、</p>

<p>JavaScript 语言没有类型检查，运行时无法知道函数的参数是否为指定的类型。这个库就用来检查函数参数的类型，如果不符合要求就抛错。</p>

<p>3、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201805/bg2018052513.jpg" alt="" title="" /></p>

<p>一个开源图标库，提供一些 24x24 的常用图标。</p>

<p>4、</p>

<p>Git 的 JavaScript 实现，这意味着你可以在 JS 里进行 Git 操作，比如从抓取/提交 commit，进行 diff 或 merge 等等。</p>

<p>5、</p>

<p>腾讯公司根据 AlphaGo 的论文，实现的开源围棋软件。</p>

<p>6、</p>

<p>收集所有开源的操作系统的网站。</p>

<p>7、</p>

<p>自从苹果采用 Intel 的处理器，OS X 被黑客破解后可以安装在 Intel CPU 与部分 AMD CPU 的机器上。从而出现了一大批非苹果设备而使用苹果操作系统的机器，被称为黑苹果（Hackintosh）。这个仓库收集了各种型号的黑苹果安装方法。</p>

<p>8、</p>

<p>Sci-hub 是最大的免费论文下载网站，几个主要的论文数据库公司都在起诉它。现在，它放出了它的所有论文的 BT 下载种子文件。</p>

<h2>文摘</h2>

<p>1、（英文）</p>

<p>无数文章告诉你，创业需要一个团队，你需要找联合创始人。但是，不一定非如此不可，数据表明没有联合创始人也是可以的。</p>

<blockquote>
  <p>我查了  里面的 7,348家公司，每家公司募集了超过1000万美元。几乎一半的公司只有一个创始人，不到三分之一的公司有两位创始人，只有22％的公司有三位或更多的创始人。创始人的平均数量是 1.85。</p>

<p>我又查了成功退出的公司的数据，这次包括筹集不到1000万美元的公司。这组数据包括6,191家公司，但独立创始人的优势更明显。超过一半的公司是由独立创始人创立的。只有三分之一有两位创始人，约18％有三位或更多的创始人。创始人的平均数量是1.72。</p>
</blockquote>

<p>2、（英文）</p>

<p>人们看一样东西，其实不是看一次，而是会看三次。下面是一张演唱会海报。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201805/bg2018052514.jpg" alt="" title="" /></p>

<p>第一次看，只会注意核心信息，他只看到上面这些东西。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201805/bg2018052515.jpg" alt="" title="" /></p>

<p>如果感兴趣，他会看第二次，寻找更多的信息。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201805/bg2018052516.jpg" alt="" title="" /></p>

<p>如果真正想参与，他会看第三次，寻找所有信息。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201805/bg2018052517.jpg" alt="" title="" /></p>

<p>如果想要吸引用户，其实你只有一次机会。就是在他看第一次的时候，就吸引到他，也就是说，你必须在最显眼的地方，呈现最核心的内容。</p>

<p>3、（英文）</p>

<p>美国佛罗里达州的迪斯尼乐园，停车场距离公园正门足足有1.6公里，中间是一个巨大的人工湖。为什么停车场不设置得近一些，一下车就能进入公园，不是对游客更方便吗？</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201805/bg2018052518.jpg" alt="" title="" /></p>

<p>（上图：红色区域是停车场，绿色区域是乐园，中间是人工湖。）</p>

<p>迪斯尼公司花几百万美元挖一个湖，故意让游客多走将近两公里，这是为什么？</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201805/bg2018052519.jpg" alt="" title="" /></p>

<p>游客从很远的地方来到乐园，他们可能开车了很长时间，途中也许遇到交通事故，也可能遇到交通堵塞，总之还处在真实世界的各种烦躁和焦虑之中。然后，他们下车后就看到了一个大湖，选择登上渡船或乘坐单轨列车前往乐园大门，一路上他们看到的都是湖景。等到了大门口，他们看到了城堡，就会忘记之前发生的一切，完全以崭新的心情，从真实的现实进入了梦幻的现实。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201805/bg2018052520.jpg" alt="" title="" /></p>

<p>（上图：红色区域是真实世界，绿色区域是你的产品，中间是一个隔离地带。）</p>

<p>对于其他产品来说，这也是一个可以借鉴的思路。现实中的用户处于痛苦和失望的状态，你需要为他们设置一个放松和缓冲的区域，与外部世界隔离，让他们以一种兴奋的状态，进入你的产品。</p>

<p>4、（英文）</p>

<blockquote>
  <p>4月9日發表在《自然生態與演化》(Nature Ecology &amp; Evolution)雜誌上的研究結果表明，人類的眉毛主要是一種社交工具，現代人類的前額更平滑，眉毛更具有表現力，也許是為了適應我們日益複雜的人際關係。</p>

<p>「有了更平坦、更豎直的前額，眼睛上方的整個區域就變得靈活了很多，肌肉也能做出一些非常微妙的交流示意，」斯皮金斯說。她表示，那些示意，比如揚起眉毛表示你認出了某人，「更多的是表示友好，而非恐嚇」。</p>
</blockquote>

<p>5、（中文）</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201805/bg2018052521.jpg" alt="" title="" /></p>

<blockquote>
  <p>这是一位叫"倾心2007"的网友发在网上发的一个帖子。2012年春节，她老公被诊断为脊柱肿瘤，初诊时手术概率几乎为零。最后他们决定赴美治疗，这是她写的赴美就医经历。</p>

<p>她在文章的开头说，去美国看病只是人生绝望中孤注一掷的选择。写这个帖子，是想让更多人知道，"绝境还有其他希望"。当然，她写的不全是个励志故事。她还写道，在美国看病里时3个月，这期间没有住过一个月，没有挂过一瓶水，甚至也只吃了几颗药。让人觉得有点不可思议。</p>
</blockquote>

<h2>本周图片</h2>

<p>1、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201805/bg2018052522.jpg" alt="" title="" /></p>

<p>上面这幅作品是纯 CSS 生成，作者还公开了源码。</p>

<p>2、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201805/bg2018052523.jpg" alt="" title="" /></p>

<p>台北市实行垃圾分类，马路上的垃圾箱很少。我在台北时，经常因为找不到垃圾箱，不得不去麦当劳或便利店扔垃圾。</p>

<p>推特网友@riddle_ling根据台北市政府的公开资料，做出了《台北垃圾箱地图》。我觉得，大陆城市应该学习，推广垃圾分类，编号管理每一个公共垃圾箱。</p>

<p>3、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201805/bg2018052524.jpg" alt="" title="" /></p>

<p>打字时多了一个空格，系统就要被删了。</p>

<h2>本周金句</h2>

<p>1、</p>

<p>千万别上瘾只想去解决那些困难的问题。如果那些问题本身就是错的，你会浪费时间；如果你解决不了，也会浪费时间。（）</p>

<p>2、</p>

<p>没用分布式架构之前，你只有一个问题：并发性能不足。用了分布式架构，多出了一堆问题：数据如何同步、主键如何产生、如何熔断、分布式事务如何处理......（）</p>

<h2>欢迎订阅</h2>

<p>这个专栏每周五发布，同步更新在我的。</p>

<p>微信搜索"<strong>阮一峰的网络日志</strong>"或者扫描二维码，即可订阅。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/2018/bg2018042311.jpg" alt="image | left" title="" /></p>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2018-05-25T13:57:27+08:00">2018年5月25日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>文集：</li>
<li>社交媒体：</li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------
<h1 id="#title_6" >7、Goodbye 'smoosh', Array.prototype.flatten is now 'flat'</h1>

[https://javascriptweekly.com/issues/387](https://javascriptweekly.com/issues/387)
<table border=0 align="center" border="0">
  <tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   ">

  <div>    
    <table border=0 border=0><tr>
<td align="left" style="padding-left: 4px; font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   "><p>#387 — May 25, 2018</p></td>
<td align="right" style="padding-right: 4px; font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   "><p></p></td>
</tr></table>
    
    <table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0 12px;  "><p>JavaScript Weekly</p></td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   ">
  
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;">.</p>
  <p>Preet Shihn </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — A wide variety of algorithms (e.g. permutations, Levenshtein distance, binary search) and data structures (e.g. linked lists, trees, stacks) implemented in JavaScript with explanations and links to further reading.</p>
  <p>Oleksii Trekhleb </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — An automated code review tool that allows developers to improve code quality. We check your code against the most popular JS static analysis tools, with specific plugins for Vue, Angular and React. Sign up for free and improve your coding.</p>
  <p>Codacy <span style="text-transform: uppercase; padding: 1px 4px;  margin-left: 4px; font-size: 0.9em;   color: #997 !important;">sponsor</span></p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"> and here’s the full story.</p>
  <p>Mathias Bynens </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"> if you want more React news.</p>
  <p>Andrew Clark </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Keep your network transmission and parse/compile cost for JavaScript low to ensure pages get interactive quickly.</p>
  <p>Addy Osmani </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — <code>npm audit fix</code> uses the results from  <code>npm audit</code> feature to upgrade insecure dependencies for you keeping semver in mind.</p>
  <p>The npm Blog </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Check out the example code for an idea of how you’d use it.</p>
  <p>Node.js Foundation </p>
</td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   ">
  
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — A step closer to native JS than jQuery but with some of the niceties (chainable, short method names).</p>
  <p>Vladimir Carrer </p>
</td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0;  "><p>💻 Jobs</p></td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;">.</p>
  <p>x-team </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — We're looking for frontend developers to join our growing team. We're using technology to reinvent the broken industry that is UK property.</p>
  <p>Nested </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Top companies use Vettery to find the best tech talent. Take a few minutes to join our platform.</p>
  <p>Vettery </p>
</td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0;  "><p>📘 Tutorials</p></td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Uses an ES6 proxy to detect changes to an underlying variable.</p>
  <p>Jack Tarantino </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — The authors and devs you trust offer bite-sized chunks of tutorials, tips and best practices to raise your game.</p>
  <p>The Frontier by Big Nerd Ranch <span style="text-transform: uppercase; padding: 1px 4px;  margin-left: 4px; font-size: 0.9em;   color: #997 !important;">sponsor</span></p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — The conclusion is ‘very’ and if you haven’t played with this ‘zero config’ bundler yet, this is as simple an intro as you’ll get.</p>
  <p>Tom Vance </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Michael Wanyoike </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — A brief guide on how to run end-to-end tests on React apps using the testing framework Cypress.</p>
  <p>Rajat S </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>ROLLBAR <span style="text-transform: uppercase; padding: 1px 4px;  margin-left: 4px; font-size: 0.9em;   color: #997 !important;">sponsor</span></p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;">▶  </span></p>
  <p>Adam Wathan </p>
</td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0;  "><p>🔧 Code and Tools</p></td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Egoist </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Ben Birch </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Very much an early prototype/proof of concept.</p>
  <p>Michal Mecinski </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Wallaby catches errors in your tests and displays the results of expressions right in your editor as you type.</p>
  <p>Wallaby.js <span style="text-transform: uppercase; padding: 1px 4px;  margin-left: 4px; font-size: 0.9em;   color: #997 !important;">sponsor</span></p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Always great to see what Kyle’s thinking.</p>
  <p>Kyle Simpson </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — An interesting use of WebAssembly here too.</p>
  <p>Mathias Nater </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Jeff Smith </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;">.</p>
  <p>Dominik Lubański </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Iskren Slavov </p>
</td></tr></table>
<table border=0 border=0><tr><td style=" font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   "></td></tr></table>
</div>

  </td></tr>
</table>





<img src="https://javascriptweekly.com/open/387/rss" width="1" height="1" />
---------------