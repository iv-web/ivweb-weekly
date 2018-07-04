## 文章索引
1、 <a href="#1css-grid-level-2:-here-comes-subgrid" >CSS Grid Level 2: Here Comes Subgrid</a><br/>
2、 <a href="#2谷歌发布适用于android-things的cloud-iot-core客户端库" >谷歌发布适用于Android Things的Cloud IoT Core客户端库</a><br/>
3、 <a href="#3文章-用于软件架构的c4模型" >文章： 用于软件架构的C4模型</a><br/>
4、 <a href="#4视频演讲-小程序在直播产品中的技术应用" >视频演讲： 小程序在直播产品中的技术应用</a><br/>
5、 <a href="#5文章-百度智能运维的技术演进之路" >文章： 百度智能运维的技术演进之路</a><br/>
6、 <a href="#6文章-独家揭秘腾讯千亿级参数分布式机器学习系统无量" >文章： 独家揭秘腾讯千亿级参数分布式机器学习系统无量</a><br/>
7、 <a href="#7采访微软项目经理gabe-monroy探讨build-2018大会上发布的azure-kubernetes-service" >采访微软项目经理Gabe Monroy，探讨Build 2018大会上发布的Azure Kubernetes Service</a><br/>
8、 <a href="#8oracle宣布提供新的java支持价格体系" >Oracle宣布提供新的Java支持价格体系</a><br/>
9、 <a href="#9microprofile社区对jakarta-ee的影响" >MicroProfile社区对Jakarta EE的影响</a><br/>
10、 <a href="#10ibm扩展可用区域和全球云能力" >IBM扩展可用区域和全球云能力</a><br/>
11、 <a href="#11腾讯谈开源通过自身拥抱开源更好地促进中国的开源生态" >腾讯谈开源：通过自身拥抱开源更好地促进中国的开源生态</a><br/><h1 id="#title_0" >1、CSS Grid Level 2: Here Comes Subgrid</h1>
Rachel Andrew
[https://www.smashingmagazine.com/2018/07/css-grid-2/](https://www.smashingmagazine.com/2018/07/css-grid-2/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/07/css-grid-2/" />
              <title>CSS Grid Level 2: Here Comes Subgrid</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>CSS Grid Level 2: Here Comes Subgrid</h1>
                  
                    
                    <address>Rachel Andrew</address>
                  
                  <time datetime="2018-07-03T13:00:47&#43;02:00" class="op-published">2018-07-03T13:00:47+02:00</time>
                  <time datetime="2018-07-03T18:48:11&#43;00:00" class="op-modified">2018-07-03T18:48:11+00:00</time>
                </header>
                

<p>We are now over a year on from CSS Grid Layout landing in the majority of our browsers, and the CSS Working Group are already working on Level 2 of the specification. In this article, I’m going to explain what is currently part of the Working and Editor’s Draft of that spec. Note that everything here is subject to change, and none of it currently works in browsers. Take this as a peek into the process, I’m sure I’ll be writing more practical pieces as we start to see implementations take shape.</p>

<h3 id="css-specification-levels">CSS Specification Levels</h3>

<p>The CSS Grid features we can currently use in browsers are those from . The various parts of CSS are broken up into modules; this modularisation happened when CSS moved on from CSS 2.1, which is why you sometimes hear people talking about CSS3. In reality, there is no CSS3. Instead, there were a set of modules which included all of the things that were already part of the CSS2.1 specification. Any CSS that existed in CSS2.1 became part of a Level 3 module, therefore, we have CSS Selectors Level 3, as selectors existed in CSS2.1.</p>

<p>New CSS features which were not part of CSS2.1, such as CSS Grid Layout, start out at Level 1. The CSS Grid Level 1 specification is essentially the first version of Grid. Once a specification Level gets to Candidate Recommendation status, major new features are not added. This means that browsers and other user agents can implement the spec and it can become a W3C Recommendation. If new features are to be designed, they will happen in a new Level of the specification. We are at this point with CSS Grid Layout. The Level 1 specification is at CR, and a Level 2 specification has been created in order for new features to be worked on. I would suggest looking at the  if you want to follow along with specification discussions, as this will contain all of the latest edits.</p>



<aside class="product-panel product-panel__tilted product-panel--book" data-audience="non-subscriber">
    <div class="container product-panel--book__container">
      <div class="panel__description panel__description--book">
    <p>Nope, we can't do any magic tricks, but we have articles,  get a seasoned selection of magic front-end tricks — e.g. <strong>live designing sessions</strong> and perf audits, too. <em>Just sayin'</em>! ;-)</p>

      <a href="http://smashed.by/perfpanelmembership" class="btn btn--green btn--large">
        Explore Smashing Wizardry&nbsp;→
      </a>
      </div>
      <div class="panel__image panel__image--book">
        <a href="http://smashed.by/perfpanelmembership" class="books__book__image">
        <div class="books__book__img">
          <img src="https://www.smashingmagazine.com/images/smashing-cat/cat-wizard.svg" alt="Smashing Cat, just preparing to do some magic stuff." width="310" height="400">
        </div>
      </a>
      </div>
    </div>
  </aside>




<h3 id="what-will-level-2-of-css-grid-contain">What Will Level 2 Of CSS Grid Contain?</h3>

<p>Ultimately, the level 2 specification will contain everything that is already in Level 1 plus some new features. If you take a look at the specification at the time of writing, there is a note explaining that all of Level 1 should be copied over once Level 2 reaches CR.</p>

<p>We can then expect to find some new features, and Level 2 of the Grid Specification is all about working out the <strong>subgrid</strong> feature of CSS Grid. This feature was dropped from the Level 1 specification in order to allow time to properly understand the use cases for subgrid, and give more time to work on it without holding up the rest of Level 1. In the rest of this article, I’ll be taking a look at the subgrid feature as it is currently detailed in the Editor’s Draft. We are at a very early stage with the feature, however, this is the perfect time to follow along, and to actually help shape how the specification is developed. My aim with writing this article is to explain some of the things being discussed, in order that you can understand and bring your input to discussions.</p>

<h3 id="what-is-a-subgrid">What Is A Subgrid?</h3>

<p>When using CSS Grid Layout, you can already nest grids. In the example below, I have a parent grid with six column tracks and three-row tracks. I have positioned an item on this grid from column line 2 to line 6 and from row line 1 to 3. I have then made that item a grid container and defined column tracks.</p>

<pre><code class="language-css">.grid {
    display: grid;
    grid-template-columns: 1fr 2fr 1fr 2fr 1fr 2fr;
    grid-template-rows: auto auto auto;
}

.item {
    grid-column: 2 / 6;
    grid-row: 1 / 3;
    display: grid;
    grid-template-columns: 2fr 1fr 2fr 1fr;
}
</code></pre>

<p>The tracks of our nested grid have no relationship to tracks on the parent. This means that if we want to be able to line the tracks of our nested grid up with the lines on the outer grid, we have to do the work and use methods of calculating track sizes that ensure all tracks remain equal. In the example above, the tracks will look lined up, until an item with a larger size is added to one cell of the grid (making it use more space).</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/19e90227-ec85-4b49-9275-00fbf37da8de/nested-grid-small-item.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/19e90227-ec85-4b49-9275-00fbf37da8de/nested-grid-small-item.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/19e90227-ec85-4b49-9275-00fbf37da8de/nested-grid-small-item.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/19e90227-ec85-4b49-9275-00fbf37da8de/nested-grid-small-item.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/19e90227-ec85-4b49-9275-00fbf37da8de/nested-grid-small-item.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/19e90227-ec85-4b49-9275-00fbf37da8de/nested-grid-small-item.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/19e90227-ec85-4b49-9275-00fbf37da8de/nested-grid-small-item.png"
			sizes="100vw"
			alt="A grid with the Firefox grid inspector showing the lines"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			A small item means the tracks look as if they line up. ()
		</figcaption>
	
</figure>












<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/80979ef6-3f02-41c8-b012-e7277d2b085a/nested-grid-large-item.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/80979ef6-3f02-41c8-b012-e7277d2b085a/nested-grid-large-item.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/80979ef6-3f02-41c8-b012-e7277d2b085a/nested-grid-large-item.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/80979ef6-3f02-41c8-b012-e7277d2b085a/nested-grid-large-item.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/80979ef6-3f02-41c8-b012-e7277d2b085a/nested-grid-large-item.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/80979ef6-3f02-41c8-b012-e7277d2b085a/nested-grid-large-item.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/80979ef6-3f02-41c8-b012-e7277d2b085a/nested-grid-large-item.png"
			sizes="100vw"
			alt="As with the first example, except the nested grid now does not align with the outer."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			With a large item, we can see the tracks do not align. ()
		</figcaption>
	
</figure>


<p>For columns, it is often possible to get around the above scenario, essentially by restricting the flexibility of grid. You could make your <code>fr</code> unit columns <code>minmax(0,1fr)</code> in order that they ignore item size when doing space distribution, or you could go back to using percentages. However, this removes some of the benefits of using grid and, when it comes to lining up rows in a nested grid these methods will not work.</p>

<p>Let’s say we want a card layout in which the individual cards have a header, body, and footer. We also want the header and footer to line up across the cards.</p>

<pre><code class="language-css">.cards {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    grid-gap: 20px;
}
    
.card {
    display: grid;
    grid-template-rows: auto 1fr auto;
}</code></pre>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0a2100e3-0db0-4773-bc98-78985b106625/cards-line-up.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0a2100e3-0db0-4773-bc98-78985b106625/cards-line-up.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0a2100e3-0db0-4773-bc98-78985b106625/cards-line-up.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0a2100e3-0db0-4773-bc98-78985b106625/cards-line-up.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0a2100e3-0db0-4773-bc98-78985b106625/cards-line-up.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0a2100e3-0db0-4773-bc98-78985b106625/cards-line-up.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0a2100e3-0db0-4773-bc98-78985b106625/cards-line-up.png"
			sizes="100vw"
			alt="Three cards in a container"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			A set of cards ()
		</figcaption>
	
</figure>


<p>This works as long as the content is the same height in each header and footer. If we have extra content then the illusion is broken and the headers and footers no longer line up across the row.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/484895b2-6f38-432a-837b-c6d251f1be53/cards-no-line-up.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/484895b2-6f38-432a-837b-c6d251f1be53/cards-no-line-up.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/484895b2-6f38-432a-837b-c6d251f1be53/cards-no-line-up.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/484895b2-6f38-432a-837b-c6d251f1be53/cards-no-line-up.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/484895b2-6f38-432a-837b-c6d251f1be53/cards-no-line-up.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/484895b2-6f38-432a-837b-c6d251f1be53/cards-no-line-up.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/484895b2-6f38-432a-837b-c6d251f1be53/cards-no-line-up.png"
			sizes="100vw"
			alt="Three cards in a container, one header taller than the others"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			We can’t get the headers to line up across the cards. ()
		</figcaption>
	
</figure>


<h3 id="creating-a-subgrid">Creating A Subgrid</h3>

<p>We can now take a look at how the subgrid feature is currently specified, and how it might solve the problems I’ve shown above.</p>

<p><strong>Note</strong>: <em>At the time of writing, none of the code below works in browsers. The aim here is to explain the syntax and concepts. The final specification is also likely to change from these details. For reference, I have written this article based on the Editor’s Draft available on June 23rd, 2018.</em></p>

<p>To create a subgrid, we will have a new value for <code>grid-template-rows</code> and <code>grid-template-columns</code>. These properties are normally used with a track listing, which defines the number and size of the row and column tracks. When creating a subgrid, however, you do not want to specify these tracks. Instead, you use the <code>subgrid</code> value to tell grid that this nested grid should use the number of tracks and track sizing that the grid area it covers spans.</p>

<p>In the below code, I have a parent grid with 6-column tracks and 3-row tracks. The nested grid is a grid item on that parent grid and spans from column line 2 to column line 6 and from row line 1 to row line 4. This is just like our initial example, however, we can now take a look at it using subgrid. The nested grid has a value of <code>subgrid</code> for both <code>grid-template-columns</code> and <code>grid-template-rows</code>. This means that the nested grid now has 4- column tracks and 2-row tracks, using the same sizing as the tracks defined on the parent.</p>

<pre><code class="language-css">.grid {
    display: grid;
    grid-template-columns: 1fr 2fr 1fr 2fr 1fr 2fr;
    grid-template-rows: auto auto auto;
}

.item {
    grid-column: 2 / 6;
    grid-row: 1 / 3;
    display: grid;
    grid-template-columns: subgrid;
    grid-template-rows: subgrid;
}</code></pre>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cd2a9063-382e-4c11-b521-fda5cbc217dc/subgrid.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cd2a9063-382e-4c11-b521-fda5cbc217dc/subgrid.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cd2a9063-382e-4c11-b521-fda5cbc217dc/subgrid.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cd2a9063-382e-4c11-b521-fda5cbc217dc/subgrid.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cd2a9063-382e-4c11-b521-fda5cbc217dc/subgrid.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cd2a9063-382e-4c11-b521-fda5cbc217dc/subgrid.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cd2a9063-382e-4c11-b521-fda5cbc217dc/subgrid.png"
			sizes="100vw"
			alt="Diagram of a grid"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The nested grid is using the tracks defined on the parent. ()
		</figcaption>
	
</figure>


<p>This would mean that any change to the track sizing on the parent would be followed by the nested grid. A longer word making one of the tracks in the parent grid wider would result in that track in the nested grid also becoming wider, so things would continue to line up. This would also work the other way: the tracks of the parent grid could become wider based on the content in the subgrid.</p>

<h3 id="one-dimensional-subgrids">One-Dimensional Subgrids</h3>

<p>You can have a subgrid in one dimension and specify track sizing in another. In this next example, the subgrid is only specified on <code>grid-template-columns</code>. The <code>grid-template-rows</code> property has a track listing specified. The column tracks will therefore remain as the four tracks we saw above, but the row tracks can be defined separately to the tracks of the parent.</p>

<pre><code class="language-css">
.grid {
    display: grid;
    grid-template-columns: 1fr 2fr 1fr 2fr 1fr 2fr;
    grid-template-rows: auto auto auto;
}

.item {
    grid-column: 2 / 6;
    grid-row: 1 / 3;
    display: grid;
    grid-template-columns: subgrid;
    grid-template-rows: 10em 5em 200px 200px;
}</code></pre>

<p>This means that the rows of the subgrid will be nested inside the parent grid, just as when creating a nested grid today. As our nested grid spans two rows of the parent, one or both of these rows will need to expand to contain the content of the subgrid so as not to cause overflows.</p>

<p>You could also have a subgrid in one dimension and the other dimension use implicit tracks. In the below example, I have not specified any row tracks, and gave a value for <code>grid-auto-rows</code>. Rows will be created in the implicit grid at the size I specified and, as with the previous example, the parent will need to have room for these rows or to expand to contain them.</p>

<pre><code class="language-css">.grid {
    display: grid;
    grid-template-columns: 1fr 2fr 1fr 2fr 1fr 2fr;
    grid-template-rows: auto auto auto;
}

.item {
    grid-column: 2 / 6;
    grid-row: 1 / 3;
    display: grid;
    grid-template-columns: subgrid;
    grid-auto-rows: minmax(200px, auto);
}</code></pre>

<h3 id="line-numbering-and-subgrid">Line Numbering And Subgrid</h3>

<p>If we take a look at our first example again, the track sizing of our subgrid is dictated by the parent in both dimensions. The line numbers, however, act as normal in the subgrid. The first column line in the inline direction is line 1, and the line at the far end of the inline direction is line -1. You do not refer to the lines of the subgrid with the line number of the parent.</p>

<pre><code class="language-css">.grid {
    display: grid;
    grid-template-columns: 1fr 2fr 1fr 2fr 1fr 2fr;
    grid-template-rows: auto auto auto;
}

.item {
    grid-column: 2 / 6;
    grid-row: 1 / 3;
    display: grid;
    grid-template-columns: subgrid;
    grid-template-rows: subgrid;
}

.subitem {
    grid-column: 2 / 4;
    grid-row: 2;
}</code></pre>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e6803c87-c092-4df8-91ee-b36dc723f4af/subgrid-numbers.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e6803c87-c092-4df8-91ee-b36dc723f4af/subgrid-numbers.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e6803c87-c092-4df8-91ee-b36dc723f4af/subgrid-numbers.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e6803c87-c092-4df8-91ee-b36dc723f4af/subgrid-numbers.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e6803c87-c092-4df8-91ee-b36dc723f4af/subgrid-numbers.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e6803c87-c092-4df8-91ee-b36dc723f4af/subgrid-numbers.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e6803c87-c092-4df8-91ee-b36dc723f4af/subgrid-numbers.png"
			sizes="100vw"
			alt="Diagram of a grid with another nested inside"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The nested grid starts numbering at line 1. ()
		</figcaption>
	
</figure>


<div id="sponsors-leaderboard-place"></div>


<h3 id="gaps-and-subgrids">Gaps And Subgrids</h3>

<p>The subgrid will inherit any column or row gap set on the parent grid, however, this can be overruled by column and row gaps specified on the subgrid. If, for example the parent grid had a <code>column-gap</code> set to 20px, but the subgrid then had <code>column-gap</code> set to 0, the grid cells of the subgrid would gain 10px on each side in order to reduce the gap to 0, with the grid line essentially running down the middle of the gap.</p>

<p>We can now see how subgrid would help us to solve the second use case from the beginning of this article, that of having cards with headers and footers that line up across the cards.</p>

<pre><code class="language-css">.grid {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    grid-auto-rows: auto 1fr auto;
    grid-gap: 20px;
}
    
.card {
    grid-row: auto / span 3; /* use three rows of the parent grid */
    display: grid;
    grid-template-rows: subgrid;
    grid-gap: 0; /* set the gap to 0 on the subgrid so our cards don’t have gaps */
}</code></pre>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/82740499-c614-4477-8f51-0d2df9751cf4/cards-subgrid-fix.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/82740499-c614-4477-8f51-0d2df9751cf4/cards-subgrid-fix.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/82740499-c614-4477-8f51-0d2df9751cf4/cards-subgrid-fix.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/82740499-c614-4477-8f51-0d2df9751cf4/cards-subgrid-fix.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/82740499-c614-4477-8f51-0d2df9751cf4/cards-subgrid-fix.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/82740499-c614-4477-8f51-0d2df9751cf4/cards-subgrid-fix.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/82740499-c614-4477-8f51-0d2df9751cf4/cards-subgrid-fix.png"
			sizes="100vw"
			alt="Three cards with headers and footers aligned"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The Card Internals Now Line Up ()
		</figcaption>
	
</figure>


<h3 id="line-names-and-subgrid">Line Names And Subgrid</h3>

<p>Any line names on your parent grid will be passed down to the subgrid. Therefore, if we named the lines on our parent grid, we could position the item according to those line names.</p>

<pre><code class="language-css">.grid {
    display: grid;
    grid-template-columns: [a] 1fr [b] 2fr [c] 1fr [d] 2fr [e] 1fr [f] 2fr [g];
    grid-template-rows: auto auto auto;
}

.item {
    grid-column: 2 / 6;
    grid-row: 1 / 3;
    display: grid;
    grid-template-columns: subgrid;
    grid-template-rows: 10em 5em 200px 200px;
}

.subitem {
    grid-column: c / e;
}</code></pre>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/df5fb087-5d66-4293-bff8-b788044c0b76/subgrid-names.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/df5fb087-5d66-4293-bff8-b788044c0b76/subgrid-names.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/df5fb087-5d66-4293-bff8-b788044c0b76/subgrid-names.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/df5fb087-5d66-4293-bff8-b788044c0b76/subgrid-names.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/df5fb087-5d66-4293-bff8-b788044c0b76/subgrid-names.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/df5fb087-5d66-4293-bff8-b788044c0b76/subgrid-names.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/df5fb087-5d66-4293-bff8-b788044c0b76/subgrid-names.png"
			sizes="100vw"
			alt="Diagram showing that line names apply to the grid and subgrid"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The line names on the parent apply to the subgrid. ()
		</figcaption>
	
</figure>


<p>You can also add line names to your subgrid, grid lines can have multiple line names so these names would be added to the lines. To specify line names, add a listing of these names after the <code>subgrid</code> value of <code>grid-template-columns</code> and <code>grid-template-rows</code>. If we take our above example and also add names to the subgrid lines we will end up with two line names for any line in the subgrid.</p>

<pre><code class="language-css">.grid {
    display: grid;
    grid-template-columns: [a] 1fr [b] 2fr [c] 1fr [d] 2fr [e] 1fr [f] 2fr [g];
    grid-template-rows: auto auto auto;
}

.item {
    grid-column: 2 / 6;
    grid-row: 1 / 3;
    display: grid;
    grid-template-columns: subgrid [sub-a] [sub-b] [sub-c] [sub-d] [sub-e];
    grid-template-rows: 10em 5em 200px 200px;
}

.subitem {
    grid-column: c / e;
}</code></pre>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/64e83c36-d077-4bc6-85e4-eb63e2fae204/subgrid-names2.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/64e83c36-d077-4bc6-85e4-eb63e2fae204/subgrid-names2.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/64e83c36-d077-4bc6-85e4-eb63e2fae204/subgrid-names2.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/64e83c36-d077-4bc6-85e4-eb63e2fae204/subgrid-names2.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/64e83c36-d077-4bc6-85e4-eb63e2fae204/subgrid-names2.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/64e83c36-d077-4bc6-85e4-eb63e2fae204/subgrid-names2.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/64e83c36-d077-4bc6-85e4-eb63e2fae204/subgrid-names2.png"
			sizes="100vw"
			alt="Diagram showing line names on the subgrid are added to those of the parent"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The Line Names Specified on the subgrid are added to those of the parent. ()
		</figcaption>
	
</figure>


<h3 id="implicit-tracks-and-subgrid">Implicit Tracks And Subgrid</h3>

<p>Once you have decided that a dimension of your grid is a subgrid, this removes the ability to have any additional implicit tracks in that dimension. If you add more items that can fit, the additional items will be placed in the last available track of the subgrid in the same way that items are dealt with in overly large grids. A Grid Area created in the subgrid that spans more tracks than are available, will have its last line set to the last line of the subgrid.</p>

<p>As explained above, however, you can have one dimension of your subgrid behave in exactly the same way as a normal nested grid, including implicit tracks.</p>

<h3 id="getting-involved-with-the-process">Getting Involved With The Process</h3>

<p>The work of the CSS Working Group happens in public, on GitHub just like any other open-source project. This makes it somewhat easier to follow along with the work that it was the everything happened in a mailing list. You can take a look at the issues raised against Level 2 of the CSS Grid specification by searching for issues tagged as  in the CSS Working Group GitHub repository. If you can contribute thoughts or a use case to any of those issues, it would be welcomed.</p>

<p>There are other features that people have requested for CSS Grid Layout, and the fact that they haven’t been included in Level 2 does not mean they are not being considered. You can see the levels as a feature release might be in a product, just because some feature isn’t part of the current sprint, doesn’t mean it will never happen. Work on new web platform features tends to take a little longer than the average product release, but it is a similar process.</p>

<h3 id="how-long-does-this-all-take">How Long Does This All Take?</h3>

<p>Specification development and browser implementation is a somewhat circular, iterative process. It is not the case that the specification needs to be “finished” before we will see some browser implementations. The initial implementations are likely to be behind feature flags &mdash; just as the original grid specification was. Keep an eye out for these appearing, as once there is code to play with it makes thinking about these features far easier!</p>

<p>I hope this tour of what might be coming soon has been interesting. I’m excited that the subgrid feature is underway, as I have always believed it vital for a full grid layout system for the web, watch this space for more news on how the feature is progressing and of emerging browser implementations.</p>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(il)</span>
</div>


              </article>
            </body>
          </html>
---------------
<h1 id="#title_1" >2、谷歌发布适用于Android Things的Cloud IoT Core客户端库</h1>
Diogo Carleto
[http://www.infoq.com/cn/news/2018/07/cloud-iot-core-client-library?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/cloud-iot-core-client-library?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>谷歌发布了一个客户端库，让开发人员更容易在Android Things设备上使用Google Cloud IoT Core。开发人员可以连接到IoT Core MQTT桥，认证设备，发布设备遥测数据，订阅配置变更，处理错误及网络中断。</p> <i>By Diogo Carleto</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_2" >3、文章： 用于软件架构的C4模型</h1>
Simon Brown
[http://www.infoq.com/cn/articles/C4-architecture-model?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/C4-architecture-model?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/C4-architecture-model/zh/smallimage/c4Model_Icon_sm-1529798065695-1530373371903.jpg"/><p>软件架构图可能是一个非常有用的沟通工具，但很多团队减少了图表的创建，即使有创建图表，也往往模糊不清。C4模型由用于上下文、容器、组件和代码的分层软件架构图组成。</p> <i>By Simon Brown</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_3" >4、视频演讲： 小程序在直播产品中的技术应用</h1>
杨春文
[http://www.infoq.com/cn/presentations/technical-application-of-small-program-in-live-product?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/technical-application-of-small-program-in-live-product?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/presentations/technical-application-of-small-program-in-live-product/zh/mediumimage/yangchunlei270-1530460894502.jpg"/><p>现场将以NOW直播为例，介绍腾讯小程序在直播领域的一些尝试，包括登录能力建设、基于腾讯云基础音视频能力的直播流性能对比和选择、动画开发、直播间元素布局开发、官方支持的一些实用基础能力等，并分享在做开发过程中遇到的一些问题及解决方案。</p> <i>By 杨春文</i>
---------------
<h1 id="#title_4" >5、文章： 百度智能运维的技术演进之路</h1>
孙春鹭
[http://www.infoq.com/cn/articles/Baidu-AIOps-Redis?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/Baidu-AIOps-Redis?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/Baidu-AIOps-Redis/zh/smallimage/timg (1)-1530613297497.jpg"/><p></p> <i>By 孙春鹭</i>
---------------
<h1 id="#title_5" >6、文章： 独家揭秘腾讯千亿级参数分布式机器学习系统无量</h1>
袁镱
[http://www.infoq.com/cn/articles/tencent-distributed-machine-learninng-system?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/tencent-distributed-machine-learninng-system?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/tencent-distributed-machine-learninng-system/zh/smallimage/GettyImages-947661322-1527676268787-1530380066494.jpg"/><p>千亿参数规模的模型已经被业界证明能够有效提高业务效果。如何高效训练出这样的模型？百 GB 级别的模型如何在线上实现毫秒级的响应？这些能力在各个大厂都被视为核心技术竞争力和机器学习能力的技术壁垒。要具备这样的能力，对相关系统有什么样的挑战？本文将从系统的角度去详细分析这些问题，并给出腾讯公司的无量系统对这些问题的解答。</p> <i>By 袁镱</i>
---------------
<h1 id="#title_6" >7、采访微软项目经理Gabe Monroy，探讨Build 2018大会上发布的Azure Kubernetes Service</h1>
Rags Srinivas
[http://www.infoq.com/cn/news/2018/07/build-2018-gabe-monroy?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/build-2018-gabe-monroy?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>InfoQ 与 Azure 平台容器服务的项目经理主管 Gabe Monroy 进行了一次访谈，探讨了在微软 //build 大会上宣布正式可用的 Azure Kubernetes Service（AKS）服务。Gabe 为读者介绍了微软与社区的合作，同时也致力于让 AKS 带来与众不同的功能，例如与 Azure Active Directory（AAD）的集成。</p> <i>By Rags Srinivas</i> <i> Translated by 邵思华</i>
---------------
<h1 id="#title_7" >8、Oracle宣布提供新的Java支持价格体系</h1>
Ben Evans
[http://www.infoq.com/cn/news/2018/07/new-support-pricing-java?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/new-support-pricing-java?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Oracle发布了一套新的Java商业支持价格体系。由于价格体系变得简单许多，企业部署会更加受益于此。</p> <i>By Ben Evans</i> <i> Translated by 刘嘉洋</i>
---------------
<h1 id="#title_8" >9、MicroProfile社区对Jakarta EE的影响</h1>
Michael Redlich
[http://www.infoq.com/cn/news/2018/07/microprofile-influence-jakartaee?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/microprofile-influence-jakartaee?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>近期，James Roper荣升为Eclipse MicroProfile的提交者（Committer），他也因此成为Jakarta EE参与成员Lightbend的首位提交者。Roper是Lightbend的高级开发人员，也是Lagom微服务框架的创立者之一。Roper近期撰写博文分享了他成为提交者的经历，并介绍了MicroProfile社区对Jakarta EE项目的影响。InfoQ就此采访了Roger，并接触了一些供职于其它企业的MicroProfile提交者。</p> <i>By Michael Redlich</i> <i> Translated by 盖磊</i>
---------------
<h1 id="#title_9" >10、IBM扩展可用区域和全球云能力</h1>
Steef-Jan Wiggers
[http://www.infoq.com/cn/news/2018/07/ibm-availability-zones?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/ibm-availability-zones?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>6月10日，IBM宣布大规模扩展其云能力及全球可用区域。该公告显示，为了在云服务市场和Amazon、微软、谷歌展开竞争，IBM做了大量的投资。</p> <i>By Steef-Jan Wiggers</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_10" >11、腾讯谈开源：通过自身拥抱开源更好地促进中国的开源生态</h1>
张婵
[http://www.infoq.com/cn/news/2018/07/tencent-open-source?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/tencent-open-source?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>6月25日-6月27日，LC3（LinuxCon + ContainerCon + CloudOpen）中国 2018 大会在北京举行。该会议由 Linux 基金会主办，是集 Linux、容器、云技术、网络、微服务等多种前沿开源议题于一身的科技盛会，吸引超过 2000 名开源专家共聚一堂。在本届大会上，腾讯正式成为 Linux 基金会白金会员，并将其两大自研开源项目——高性能 RPC 开发框架 TARS和轻量化名字服务方案 TSeer 贡献给了 Linux 基金会。</p> <i>By 张婵</i>
---------------