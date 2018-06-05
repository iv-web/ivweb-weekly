## 文章索引
1、 <a href="#1making-avengers-id-card-in-html-and-css" >Making Avengers ID Card In HTML And CSS</a><br/>
2、 <a href="#275-亿美金纳德拉宣布微软正式收购-github" >75 亿美金，纳德拉宣布微软正式收购 GitHub</a><br/>
3、 <a href="#3文章-作为一名区块链架构师需要从哪几个纬度去做技术选型" >文章： 作为一名区块链架构师，需要从哪几个纬度去做技术选型？</a><br/>
4、 <a href="#4文章-构建增强现实移动应用程序的六款顶级工具" >文章： 构建增强现实移动应用程序的六款顶级工具</a><br/>
5、 <a href="#5文章-苏宁乔新亮世界上最好的研发管理十条经验" >文章： 苏宁乔新亮：世界上最好的研发管理十条经验</a><br/>
6、 <a href="#6fex-技术周刊---2018/06/04" >FEX 技术周刊 - 2018/06/04</a><br/>
7、 <a href="#7在敏捷中应用即兴游戏" >在敏捷中应用即兴游戏</a><br/>
8、 <a href="#8vpnfilter已经感染了全球50万台以上的路由器" >VPNFilter已经感染了全球50万台以上的路由器</a><br/>
9、 <a href="#9gdpr生效后unrollme和pinterest的instapaper在欧洲无法使用" >GDPR生效后Unroll.me和Pinterest的Instapaper在欧洲无法使用</a><br/>
10、 <a href="#10apicloud以生态之力创造api新经济" >APICloud以生态之力创造API新经济</a><br/>
11、 <a href="#11消息称微软计划收购github估值超50亿美元" >消息称微软计划收购GitHub，估值超50亿美元</a><br/><h1 id="#title_0" >1、Making Avengers ID Card In HTML And CSS</h1>
Kunal Sarkar
[https://www.smashingmagazine.com/2018/06/avengers-id-card-html-css/](https://www.smashingmagazine.com/2018/06/avengers-id-card-html-css/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/06/avengers-id-card-html-css/" />
              <title>Making Avengers ID Card In HTML And CSS</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>Making Avengers ID Card In HTML And CSS</h1>
                  
                    
                    <address>Kunal Sarkar</address>
                  
                  <time datetime="2018-06-04T16:00:01&#43;02:00" class="op-published">2018-06-04T16:00:01+02:00</time>
                  <time datetime="2018-06-04T16:17:31&#43;00:00" class="op-modified">2018-06-04T16:17:31+00:00</time>
                </header>
                

<p>Let’s suppose Tony Stark would like to redesign the ID cards of the Avengers, and he needs our help to create them in HTML and CSS. So, how can we help? In this tutorial, we’ll be using Flexbox to create the desired layout while diving into nested flexboxes for some advanced layouts. We will also be using rounded as well as transparent borders to create sci-fi arcs in CSS, and then animating them by using CSS animations around the picture of the Avenger. Last but not least, we’ll be using the <code>box-shadow</code> and <code>text-shadow</code> properties to give our ID card a final sci-fi touch.</p>

<p>By the end of the tutorial, we will build a sci-fi animated Avengers ID card, and also learn the basics of Flexbox, nested Flexbox, CSS animations, borders, shadows, and many other frequently used CSS properties.</p>

<p>Here’s how our final Avengers ID card will look like:</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="wmNjXm"
   data-user="supersarkar"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<p>Let’s get started!</p>



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





<div class="c-garfield-the-cat">


<h3 id="full-page-background">Full-Page Background</h3>

<p>We need a div that covers the entire screen. We will use this div as the background to place the ID card:</p>

<pre><code class="language-html">&lt;div class="id-card-wrapper"&gt;
&lt;/div&gt;
</code></pre>

<p>Let’s make the div cover the entire page and give a dark background:</p>

<pre><code class="language-css">body {
  margin:0px;
}
.id-card-wrapper {
  height: 100vh;
  width:100%;
  background-color: #122023;
}
</code></pre>

<h4 id="why-use-100vh-and-not-100-for-height">Why use <code>100vh</code> and not <code>100%</code> for height?</h4>

<p>If you look closely, you will notice that we used <code>100%</code> for width, but <code>100vh</code> for height. The <code>vh</code> unit stands for “viewport height”. It is a viewport unit, some other viewport units are: <code>vw</code>, <code>vmin</code>, and <code>vmax</code>.</p>

<p>So, why should we use <code>100vh</code> instead of <code>100%</code> for the height? Well, a <code>%</code> based dimension is relative to its parent element. So, if we set the height of the <code>id-card-wrapper</code> to 100%, that would mean it will make the height of <code>id-card-wrapper</code> cover 100% of the height of its parent element (which is the <code>body</code> element).</p>

<p>The problem is &mdash; by default &mdash; the body element doesn’t cover entire screen’s height. The width of the body element is by default 100% that’s why we can use <code>width: 100%</code> on <code>id-card-wrapper</code>, but since the height is not 100% by default the same won’t work for height.</p>

<p>Since a viewport unit is relative to the viewport, not the parent element, setting the height to <code>100vh</code> will make the element cover entire height of the visible area (viewport), regardless of the parent’s dimensions.</p>

<p><strong>Note</strong>: <em>If you want to dive deeper into the viewport units, checkout this .</em></p>

<h4 id="why-margin-0px-on-body">Why <code>margin: 0px</code> On Body?</h4>

<p>The browsers by default display some margin around the body. If we don’t set this margin to 0, we will get a white gap around the <code>id-card-wrapper</code> div.</p>

<h3 id="centering-using-flexbox">Centering Using Flexbox</h3>

<p>There are many ways to center. Now that our full-page background is ready, let’s create the div that will contain our ID Card. We will put only “Test” as content, and build the layout first:</p>

<pre><code class="language-html">&lt;div class="id-card-wrapper"&gt;
    &lt;div class="id-card"&gt;
        Test
    &lt;/div&gt;
&lt;/div&gt;
</code></pre>

<p>And add some styles to it:</p>

<pre><code class="language-css">.id-card {
  border: 2px solid #0AE0DF;
  max-width: 30em;
  margin: auto;
  color: #fff;
  padding: 1em;
}
</code></pre>

<p>We are using the <code>border</code> property to give a 2px solid border of <code>#0AE0DF</code> color to the <code>id-card</code> element.</p>

<p>Since a “div” is a block element, it will cover the entire width of the parent element by default. But we don’t want it to go beyond <code>30em</code>, so we’ll set the <code>max-width</code> property to <code>30em</code>.</p>

<h4 id="wait-what-is-em-again">Wait, What Is <code>em</code> Again?</h4>

<p>Here’s what  has to say about the &ldquo;em&rdquo; unit:</p>

<blockquote>“The <code>em</code> is simply the font size. In an element with a <code>2in</code> font, <code>1em</code> thus means <code>2in</code>.”</blockquote>

<p>This means that if your browser has a default font size of 14px, then <code>30em</code> will be equal to 30&times;14 = 420px.</p>

<p>But, why use <code>em</code> unit instead of <code>px</code>?</p>

<p>Look, the <code>em</code> unit is relative to the font size. Let’s suppose you are using a browser with 14px default font size. Now if someone views your project from another browser that has 16px as default font size, then guess what would happen?</p>

<p>The content inside will need more space, but your div has a fixed width, i.e. the content will either spill out or break the layout.</p>

<p>It’s always a good idea to have dimensions that scale along with the content, instead of fixing it to arbitrary pixels.</p>

<h4 id="why-doesn-t-margin-auto-center-the-div-vertically">Why Doesn’t <code>margin: auto</code> Center The <code>div</code> Vertically?**</h4>

<p>We already know that we can center a block element horizontally using <code>margin: auto</code>, but it doesn’t work for vertical centering.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f22662a1-508b-4a7f-a10b-e5f3f4ffb690/1-avengers-id-tutorial.JPG">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f22662a1-508b-4a7f-a10b-e5f3f4ffb690/1-avengers-id-tutorial.JPG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f22662a1-508b-4a7f-a10b-e5f3f4ffb690/1-avengers-id-tutorial.JPG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f22662a1-508b-4a7f-a10b-e5f3f4ffb690/1-avengers-id-tutorial.JPG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f22662a1-508b-4a7f-a10b-e5f3f4ffb690/1-avengers-id-tutorial.JPG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f22662a1-508b-4a7f-a10b-e5f3f4ffb690/1-avengers-id-tutorial.JPG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f22662a1-508b-4a7f-a10b-e5f3f4ffb690/1-avengers-id-tutorial.JPG"
			sizes="100vw"
			alt="Screenshot of a horizontally centered element"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Auto margin centers the element horizontally
		</figcaption>
	
</figure>


<p>What if I told you that <code>margin: auto</code> works vertically, too? Actually, in normal layout mode, it doesn’t. But in new layout modes like Flexbox, the <code>margin: auto</code> works for vertical centering, too. Go ahead and make the <code>id-card-wrapper</code> a flexbox to see it yourself:</p>

<pre><code class="language-css">.id-card-wrapper {
  height: 100vh;
  width:100%;
  background-color: #122023;
  display: flex;
}
</code></pre>

<p>Output:</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6b53e4e0-5f85-450d-b031-b92ef53fe2dd/2-avengers-id-tutorial.JPG">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6b53e4e0-5f85-450d-b031-b92ef53fe2dd/2-avengers-id-tutorial.JPG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6b53e4e0-5f85-450d-b031-b92ef53fe2dd/2-avengers-id-tutorial.JPG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6b53e4e0-5f85-450d-b031-b92ef53fe2dd/2-avengers-id-tutorial.JPG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6b53e4e0-5f85-450d-b031-b92ef53fe2dd/2-avengers-id-tutorial.JPG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6b53e4e0-5f85-450d-b031-b92ef53fe2dd/2-avengers-id-tutorial.JPG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6b53e4e0-5f85-450d-b031-b92ef53fe2dd/2-avengers-id-tutorial.JPG"
			sizes="100vw"
			alt="Screenshot of a horizontally and vertically centered element"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Auto margin centers the element horizontally and vertically if the element is a flex-item
		</figcaption>
	
</figure>


<p>As you can see, our <code>id-card</code> div is now centered horizontally and vertically. We simply set <code>display: flex</code> on the <code>id-card-wrapper</code> div. When you set <code>display: flex</code> to an element, that element becomes a <em>flex-container</em> and its child elements become <em>flex-items</em>. Check out “” on MDN.</p>


  <div id="sponsors-article" data-impression="true" class="c-promo-box c-promo-box--ad sponsors hidden" data-audience="non-subscriber" data-remove="true"></div>



<p>Okay, this did center our element, but why did it lose its width? The <code>id-card</code> div is a block element, and since block elements are by default 100% wide, why did the div lose this block level behavior when it became a flex-item?</p>

<p>Actually, it hasn’t lost its block behavior. What’s happening is, as soon as the div comes into the flexbox context, the flexbox algorithm notes that the div doesn’t have any <code>width</code> property set to it (we are giving it only <code>max-width</code>), and then it sets the initial width to 0.</p>

<p>We can change this behavior by explicitly defining the initial width of the element using the <code></code> property, like this:</p>

<pre><code class="language-css">.id-card {
  flex-basis: 100%;
  border: 2px solid #0AE0DF;
  max-width: 30em;
  margin: auto;
  color: #fff;
  padding: 1em;
}
</code></pre>

<p>And now the result looks just as expected:</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/90a617c0-6e5f-489e-9543-4d7f27beb6c1/3-avengers-id-tutorial.JPG">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/90a617c0-6e5f-489e-9543-4d7f27beb6c1/3-avengers-id-tutorial.JPG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/90a617c0-6e5f-489e-9543-4d7f27beb6c1/3-avengers-id-tutorial.JPG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/90a617c0-6e5f-489e-9543-4d7f27beb6c1/3-avengers-id-tutorial.JPG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/90a617c0-6e5f-489e-9543-4d7f27beb6c1/3-avengers-id-tutorial.JPG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/90a617c0-6e5f-489e-9543-4d7f27beb6c1/3-avengers-id-tutorial.JPG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/90a617c0-6e5f-489e-9543-4d7f27beb6c1/3-avengers-id-tutorial.JPG"
			sizes="100vw"
			alt="Screenshot of a flex-item set with flex-basis set to 100%"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The initial width of the flex-item set to 100% using “flex-basis”
		</figcaption>
	
</figure>


<h3 id="nested-flexboxes">Nested Flexboxes</h3>

<p>Now our <code>id-card</code> div is ready for content. Let’s create a <code>profile-row</code> div and two sections in it <code>dp</code> and <code>desc</code>. The <code>dp</code> div will contain the profile photo of the Avenger while the <code>desc</code> div will contain the description of that Avenger:</p>

<pre><code class="language-html">&lt;div class="id-card-wrapper"&gt;
    &lt;div class="id-card"&gt;
        &lt;div class="profile-row"&gt;
            &lt;div class="dp"&gt;
                Test
            &lt;/div&gt;
            &lt;div class="desc"&gt;
                Test desc
            &lt;/div&gt;
        &lt;/div&gt;
    &lt;/div&gt;
&lt;/div&gt;
</code></pre>

<p>We know that the <code>id-card</code> div is a flex-item, but the div we just created inside <code>id-card</code> (the <code>profile-row</code> div) isn’t a flex-item. Yes, only the direct decedents of the flex-containers become flex-items, but not the grandchildren.</p>

<p>Therefore, <code>profile-row</code> is a normal div, and we will make it a flex-container by setting <code>display: flex</code> to it. This will make its child elements, <code>dp</code> and <code>desc</code>, flex-items:</p>

<pre><code class="language-css">.profile-row {
  display: flex;
}
</code></pre>

<p>Now we can use the <code>flex-basis</code> property to make the <code>dp</code> div 33.3% wide and the <code>desc</code> div 66.6% wide:</p>

<pre><code class="language-css">.profile-row .dp {
  flex-basis: 33.3%;
}
.profile-row .desc {
  flex-grow: 66.6%;
}
</code></pre>

<p>Here’s what we get:</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/119fe3ad-8cec-4d58-bc16-40667613d068/4-avengers-id-tutorial.JPG">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/119fe3ad-8cec-4d58-bc16-40667613d068/4-avengers-id-tutorial.JPG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/119fe3ad-8cec-4d58-bc16-40667613d068/4-avengers-id-tutorial.JPG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/119fe3ad-8cec-4d58-bc16-40667613d068/4-avengers-id-tutorial.JPG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/119fe3ad-8cec-4d58-bc16-40667613d068/4-avengers-id-tutorial.JPG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/119fe3ad-8cec-4d58-bc16-40667613d068/4-avengers-id-tutorial.JPG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/119fe3ad-8cec-4d58-bc16-40667613d068/4-avengers-id-tutorial.JPG"
			sizes="100vw"
			alt="Screenshot of two flex-items in a row with 33.3% and 66.6% width"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			We can define how much space the elements would occupy using the “flex-basis” property.
		</figcaption>
	
</figure>


<h3 id="profile-image">Profile Image</h3>

<p>For the profile image, we will use a cute Iron Man picture for Stark’s ID card (). Include the image using <code>img</code> tag inside the <code>dp</code> div:</p>

<pre><code class="language-html">&lt;div class="id-card-wrapper"&gt;
    &lt;div class="id-card"&gt;
        &lt;div class="profile-row"&gt;
            &lt;div class="dp"&gt;
                &lt;img src="img/iron-man-dp.jpg"&gt;
            &lt;/div&gt;
            &lt;div class="desc"&gt;
                Test desc
            &lt;/div&gt;
        &lt;/div&gt;
    &lt;/div&gt;
&lt;/div&gt;
</code></pre>

<p>And give some styles to it:</p>

<pre><code class="language-css">.profile-row .dp img {
  max-width: 100%;
  border-radius: 50%;
}
.profile-row .desc {
  padding: 1em;
}
</code></pre>

<p>We set <code>max-width: 100%</code> for the <code>img</code> element because the <code>img</code> element by default displays the image in its original resolution.</p>

<p>If the image is 500px&times;500px then it will be displayed in that dimension. But we don’t want that. Instead, we want the image to be only as wide as the <code>dp</code> div, that’s why we set its <code>max-width</code> to 100%.</p>

<p>Also, we set the <code>border-radius</code> property to <code>50%</code>. We are doing this to display the image as a circle:</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b33d92c6-a3ef-46c4-9b6c-2c8ddee76470/5-avengers-id-tutorial.JPG">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b33d92c6-a3ef-46c4-9b6c-2c8ddee76470/5-avengers-id-tutorial.JPG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b33d92c6-a3ef-46c4-9b6c-2c8ddee76470/5-avengers-id-tutorial.JPG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b33d92c6-a3ef-46c4-9b6c-2c8ddee76470/5-avengers-id-tutorial.JPG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b33d92c6-a3ef-46c4-9b6c-2c8ddee76470/5-avengers-id-tutorial.JPG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b33d92c6-a3ef-46c4-9b6c-2c8ddee76470/5-avengers-id-tutorial.JPG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b33d92c6-a3ef-46c4-9b6c-2c8ddee76470/5-avengers-id-tutorial.JPG"
			sizes="100vw"
			alt="Screenshot of Iron Man rounded image with demo text"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			We don’t make the img element a flex-item, but rather put it inside a flex-item.
		</figcaption>
	
</figure>


<h3 id="making-arcs-in-css">Making Arcs In CSS</h3>

<p>Eventually, Tony visits us while we’re still working on this ID card, and says that this doesn’t look sci-fi enough. Alright, no problem. Let’s make it more sci-fi. We can make two arcs rotate around the image by inserting the first arc <code>dp-arc-inner</code> inside the <code>dp</code> element:</p>

<pre><code class="language-html">&lt;div class="id-card-wrapper"&gt;
    &lt;div class="id-card"&gt;
        &lt;div class="profile-row"&gt;
            &lt;div class="dp"&gt;
                &lt;div class="dp-arc-inner"&gt;&lt;/div&gt;
                &lt;img src="img/iron-man-dp.jpg"&gt;
            &lt;/div&gt;
            &lt;div class="desc"&gt;
                Test desc
            &lt;/div&gt;
        &lt;/div&gt;
    &lt;/div&gt;
&lt;/div&gt;
</code></pre>

<p>Position it in CSS:</p>

<pre><code class="language-css">.profile-row .dp {
  flex-basis: 33.3%;
  position: relative;
}
.profile-row .dp img {
  max-width: 100%;
  border-radius: 50%;
  display: block;
}
.profile-row .dp .dp-arc-inner {
  position: absolute;
  width: 100%;
  height: 100%;
  border: 6px solid #0AE0DF;
  top: -6px;
  left: -6px;
}
</code></pre>

<p>We want the arc div to overlap on the <code>dp</code> div. The only problem is that elements don’t overlap in HTML. However, if we set the position of an element as <code>absolute</code> then that element is taken out of the normal flow of the document and we can set its position as we desire.</p>

<p>The default positioning of HTML elements is <code>static</code>. We set <code>position: absolute</code> on <code>dp-arc-inner</code> to make it absolutely positioned. Now we can use <code>left</code>, <code>top</code>, <code>bottom</code>, and <code>right</code> properties to set its position.</p>

<p>One caution: The <code>left</code>, <code>top</code>, <code>bottom</code>, and <code>right</code> properties are relative the first parent element in the hierarchy which is “relatively” positioned. That’s why we&rsquo;ve set  <code>position: relative</code> on the <code>dp</code> div. If we don’t do this, the <code>left</code>, <code>top</code>, <code>bottom</code>, and <code>right</code> properties will be set respectively to the screen, not the <code>dp</code> element.</p>

<p>One more thing: we are setting <code>display: block</code> on the <code>img</code> element. Why? Because <code>img</code> elements are <code>inline-block</code> by default, and <code>inline-block</code> elements display a tiny gap on its sides and bottom.</p>

<p>This gap generally doesn’t cause any problem, but a little gap around the image in our case will offset the arc’s position. So we set the <code>img</code> element as block element.</p>

<p>Next, let’s make the <code>dp-arc-inner</code> div look like an arc:</p>

<pre><code class="language-css">.profile-row .dp .dp-arc-inner {
  position: absolute;
  width: 100%;
  height: 100%;
  border: 6px solid transparent;
  border-top-color: #0AE0DF;
  border-radius: 50%;
  top: -6px;
  left: -6px;
}
</code></pre>

<p>What we are doing is, instead of setting the border for all the sides with <code>#0AE0DF</code> color, we are setting all the sides as transparent, and then giving only the top border the color <code>#0AE0DF</code>. Then we set the <code>border-radius: 50%</code> to make it round:</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/978b436f-5e9c-4d6a-a11a-46acb95f6da4/6-avengers-id-tutorial.JPG">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/978b436f-5e9c-4d6a-a11a-46acb95f6da4/6-avengers-id-tutorial.JPG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/978b436f-5e9c-4d6a-a11a-46acb95f6da4/6-avengers-id-tutorial.JPG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/978b436f-5e9c-4d6a-a11a-46acb95f6da4/6-avengers-id-tutorial.JPG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/978b436f-5e9c-4d6a-a11a-46acb95f6da4/6-avengers-id-tutorial.JPG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/978b436f-5e9c-4d6a-a11a-46acb95f6da4/6-avengers-id-tutorial.JPG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/978b436f-5e9c-4d6a-a11a-46acb95f6da4/6-avengers-id-tutorial.JPG"
			sizes="100vw"
			alt="Screenshot of Iron Man’s rounded image surrounded with an arc covering it"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The negative margins offsets the width of the border we gave to the arc
		</figcaption>
	
</figure>


<p>Okay, let’s create one more arc, <code>dp-arc-outer</code>:</p>

<pre><code class="language-html">&lt;div class="id-card-wrapper"&gt;
    &lt;div class="id-card"&gt;
        &lt;div class="profile-row"&gt;
            &lt;div class="dp"&gt;
                &lt;div class="dp-arc-outer"&gt;&lt;/div&gt;
                &lt;div class="dp-arc-inner"&gt;&lt;/div&gt;
                &lt;img src="img/iron-man-dp.jpg"&gt;
            &lt;/div&gt;
            &lt;div class="desc"&gt;
                Test desc
            &lt;/div&gt;
        &lt;/div&gt;
    &lt;/div&gt;
&lt;/div&gt;
</code></pre>

<p>And style it the same way:</p>

<pre><code class="language-css">.profile-row .dp .dp-arc-outer {
  position: absolute;
  width: calc(100% + 12px);
  height: calc(100% + 12px);
  border: 6px solid transparent;
  border-bottom-color: #0AE0DF;
  border-radius: 50%;
  top: -12px;
  left: -12px;
}
</code></pre>

<p>Wow, what’s that <code>calc</code> thing there?</p>

<p> is a CSS function that calculates the mathematical expression given to it. Look, we had the inner arc with width and height of 100% and a border of 6px, right? That makes the inner arc’s total width <code>6px + 100% + 6px</code>.</p>

<p>Now if we want the outer arc to be bigger than the inner arc then we need some way to make it <code>100% + 12px</code> wide. This is where the <code>calc()</code> function comes to the rescue.</p>

<p>Also, notice that we are using <code>border-bottom-color</code> for this arc since we want the arc to display on the bottom.</p>

<p>Output:</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/984bd873-2f11-4733-bdfa-7fbb123f8c16/7-avengers-id-tutorial.JPG">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/984bd873-2f11-4733-bdfa-7fbb123f8c16/7-avengers-id-tutorial.JPG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/984bd873-2f11-4733-bdfa-7fbb123f8c16/7-avengers-id-tutorial.JPG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/984bd873-2f11-4733-bdfa-7fbb123f8c16/7-avengers-id-tutorial.JPG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/984bd873-2f11-4733-bdfa-7fbb123f8c16/7-avengers-id-tutorial.JPG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/984bd873-2f11-4733-bdfa-7fbb123f8c16/7-avengers-id-tutorial.JPG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/984bd873-2f11-4733-bdfa-7fbb123f8c16/7-avengers-id-tutorial.JPG"
			sizes="100vw"
			alt="Screenshot of Iron Man’s rounded image surrounded with two arcs covering it"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The calc function adds 12px to create the 6px gap between the arc and the image
		</figcaption>
	
</figure>


<h3 id="animating-the-arcs">Animating The Arcs</h3>

<p>Now that our arcs are ready, let’s make them rotate around the image. We can do this with the help of CSS animations.</p>

<p>Any animation requires three basic things:</p>

<ol>
<li>The start state of the animation,</li>
<li>The end state of the animation,</li>
<li>How long it should take to go from start to end state (speed of the animation).</li>
</ol>

<p>We can provide these data in CSS like this:</p>

<pre><code class="language-css">.profile-row .dp .dp-arc-inner {
  position: absolute;
  width: 100%;
  height: 100%;
  border: 6px solid transparent;
  border-top-color: #0AE0DF;
  border-radius: 50%;
  top: -6px;
  left: -6px;

  animation-duration: 2s;
  animation-name: rotate-clock;
}
@keyframes rotate-clock {
  from {
    transform: rotate(0deg);
  }
  to {
    transform: rotate(360deg);
  }
}
</code></pre>

<p>We use <code>@keyframes</code> to define the animation. The <code>from</code> and <code>to</code> keywords are used to set the start and end state of the animation.</p>

<p>In the start state, we are rotating the arc 0-degree using <code>transform: rotate(0deg)</code>, and in the end state we are rotating the arc 360-degree using <code>transform: rotate(360deg)</code>.</p>

<p>To use this animation on an element, we need to give the name of the animation (<code>rotate-clock</code> in our case) to the <code>animation-name</code> property of that element. That’s what we are doing with <code>animation-name: rotate-clock</code> .</p>

<p>We also need to know how long it should take the animation to complete. We can do this by setting <code>animation-duration</code> property to <code>2s</code>.</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="aYXJgZ"
   data-user="supersarkar"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<p>You will notice two problems in the output. One, the arc is rotated only one time, we want it to keep rotating, and two, the animation is not linear. The animation is fast at beginning and end, we want it to rotate with same speed throughout the animation.</p>

<p>To solve these problems, we will use the <code>animation-iteration-count</code> property to keep the animation repate itself infinite times, and <code>animation-timing-function</code> property to get a linear animation:</p>

<pre><code class="language-css">.profile-row .dp .dp-arc-inner {
  position: absolute;
  width: 100%;
  height: 100%;
  border: 6px solid transparent;
  border-top-color: #0AE0DF;
  border-radius: 50%;
  top: -6px;
  left: -6px;

  animation-duration: 2s;
  animation-name: rotate-clock;
  animation-iteration-count: infinite;
  animation-timing-function: linear;
}
</code></pre>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="KoJWOL"
   data-user="supersarkar"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<p>Okay, the inner arc is now rotating as expected. Now let’s animate the outer arc in the same way, but in the opposite direction:</p>

<pre><code class="language-css">.profile-row .dp {
  flex-basis: 33.3%;
  position: relative;
  margin: 24px;
}
.profile-row .dp .dp-arc-outer {
  position: absolute;
  width: calc(100% + 12px);
  height: calc(100% + 12px);
  border: 6px solid transparent;
  border-bottom-color: #0AE0DF;
  border-radius: 50%;
  top: -12px;
  left: -12px;

  animation-duration: 2s;
  animation-name: rotate-anticlock;
  animation-iteration-count: infinite;
  animation-timing-function: linear;
}
@keyframes rotate-anticlock {
  from {
    transform: rotate(0deg);
  }
  to {
    transform: rotate(-360deg);
  }
}
</code></pre>

<p>We only changed the <code>to</code> state for the outer arc. Instead of rotating it a positive 360 degree, we rotated it a negative 360 degree, to get an anti-clockwise animation.</p>

<p>Note that we also added 24px margin to the <code>.dp</code> so that it doesn’t get too congested. Here’s what our result looks like now:</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="yKZbyB"
   data-user="supersarkar"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>





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




<h3 id="using-a-sci-fi-google-font">Using A Sci-Fi Google Font</h3>

<p>Tony visits again, and this time he is happy with where we are heading. Only one thing though: he asks to use a sci-fi font.</p>

<p>Not a problem. Let’s use the  font from Google Fonts. Google Fonts gives a wealth of fonts for free and this particular font fits our requirement quite well.</p>

<p>Click on “Select this Font”:</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e129a339-05f9-458f-b699-c1ef976c6e1b/8-avengers-id-tutorial.JPG">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e129a339-05f9-458f-b699-c1ef976c6e1b/8-avengers-id-tutorial.JPG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e129a339-05f9-458f-b699-c1ef976c6e1b/8-avengers-id-tutorial.JPG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e129a339-05f9-458f-b699-c1ef976c6e1b/8-avengers-id-tutorial.JPG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e129a339-05f9-458f-b699-c1ef976c6e1b/8-avengers-id-tutorial.JPG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e129a339-05f9-458f-b699-c1ef976c6e1b/8-avengers-id-tutorial.JPG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e129a339-05f9-458f-b699-c1ef976c6e1b/8-avengers-id-tutorial.JPG"
			sizes="100vw"
			alt="Screenshot of Google Font page of Orbitron font"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			You will see the “Select this font” link once you visit the Google font link
		</figcaption>
	
</figure>


<p>A popover will appear at the bottom. Click on it. You will get two codes: the <code>&lt;link&gt;</code> code to copy into your HTML, and the <code>font-family</code> code to use in your CSS:</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bbcfe9af-7e0d-488f-8a9a-9335ac3ab653/9-avengers-id-tutorial.JPG">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bbcfe9af-7e0d-488f-8a9a-9335ac3ab653/9-avengers-id-tutorial.JPG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bbcfe9af-7e0d-488f-8a9a-9335ac3ab653/9-avengers-id-tutorial.JPG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bbcfe9af-7e0d-488f-8a9a-9335ac3ab653/9-avengers-id-tutorial.JPG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bbcfe9af-7e0d-488f-8a9a-9335ac3ab653/9-avengers-id-tutorial.JPG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bbcfe9af-7e0d-488f-8a9a-9335ac3ab653/9-avengers-id-tutorial.JPG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bbcfe9af-7e0d-488f-8a9a-9335ac3ab653/9-avengers-id-tutorial.JPG"
			sizes="100vw"
			alt="Screenshot of Google Font page of Orbitron font with the font selected"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			When you click the “Select this font” link a pop-up will be displayed with link and “font-family” code of that font
		</figcaption>
	
</figure>


<p>Copy the <code>&lt;link&gt;</code> code into your HTML file just above the line where you are including your stylesheet.</p>

<p>Now let’s add some details of Iron Man inside the <code>desc</code> div:</p>

<pre><code class="language-html">&lt;div class="id-card-wrapper"&gt;
    &lt;div class="id-card"&gt;
        &lt;div class="profile-row"&gt;
            &lt;div class="dp"&gt;
                &lt;div class="dp-arc-outer"&gt;&lt;/div&gt;
                &lt;div class="dp-arc-inner"&gt;&lt;/div&gt;
                &lt;img src="img/iron-man-dp.jpg"&gt;
            &lt;/div&gt;
            &lt;div class="desc"&gt;
                &lt;h1&gt;Tony Stark&lt;/h1&gt;
                &lt;p&gt;Strength: Ironman Suit&lt;/p&gt;
                &lt;p&gt;Weakness: None&lt;/p&gt;
                &lt;p&gt;Known as: Iron Man&lt;/p&gt;
            &lt;/div&gt;
        &lt;/div&gt;
    &lt;/div&gt;
&lt;/div&gt;
</code></pre>

<p>In our CSS, we will use the <code>font-family</code> code from Google Fonts to set the font of <code>desc</code> div:</p>

<pre><code class="language-css">.profile-row .desc {
  font-family: 'Orbitron', sans-serif;
  color: #a4f3f2;
}
.profile-row .desc h1 {
  margin: 0px;
}
</code></pre>

<p>Wait a sec, why are we setting the margin of <code>h1</code> to <code>0</code>?</p>

<p>You see, all the heading elements (<code>h1</code>, <code>h2</code>, <code>h3</code>, <code>h4</code>, and <code>h5</code>) are displayed with some margin around it by the browsers. This is usually not a problem, but we don’t want the top and bottom gaps around the heading elements right now. That’s why we zeroed the margin for <code>h1</code> element.</p>

<p>Let’s have a look at the output:</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="MVLVdX"
   data-user="supersarkar"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<p><em>Uh oh</em>! What happened?</p>

<p>Looks like the height of the <code>dp</code> div is increasing. Normally, if the content in the <code>desc</code> div is of more height than the height of the <code>dp</code> div then nothing happens to the <code>dp</code> div. However, in Flexbox layout, the height of the <code>dp</code> div will also increase along with the height of the <code>desc</code> div.</p>

<p>We don’t want the <code>dp</code> div to increase in height with the <code>desc</code> div, so we can control this by using the <code>[align-self](https://developer.mozilla.org/en-US/docs/Web/CSS/align-self)</code> sub-property of flexbox like this:</p>

<pre><code class="language-css">.profile-row .dp {
  flex-basis: 33.3%;
  align-self: center;
  position: relative;
  margin: 24px;
}
</code></pre>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="zWejOe"
   data-user="supersarkar"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<p>The <code>align-self: center</code> makes the <code>dp</code> div to center keeping its height the same.</p>

<h3 id="adding-glow">Adding Glow</h3>

<p>Now, let’s add some glow.</p>

<p>But wait, CSS doesn’t have any glow property.</p>

<p>No problem, it does have the <code></code> property. If we give a bright color to the shadow, the shadow will look like it’s glowing:</p>

<pre><code class="language-css">.profile-row .desc {
  font-family: 'Orbitron', sans-serif;
  color: #d3f8f7;
  text-shadow: 0px 0px 4px #12a0a0;
  letter-spacing: 1px;
}
</code></pre>

<p>In the <code>text-shadow</code> property, the first value, <code>0px</code>, is the x-offset, how much the shadow is away from text in the x-direction. The second value, <code>0px</code>, is the y-offset, telling us how much the shadow is away from the text in the y-direction. The third value, <code>4px</code>, is the amount of blur you want to give to the shadow. The fourth value, <code>#12a0a0</code>, is the color of the shadow.</p>

<p>Note that we also added a 1px space between the letters of text using the <code></code> property because the text was looking a bit congested.</p>

<p>Next, let’s add some shadow to the ID card and the image:</p>

<pre><code class="language-css">.id-card {
  flex-basis: 100%;
  max-width: 30em;
  border: 1px solid rgb(97, 245, 245);
  margin: auto;
  color: #fff;
  padding: 1em;
  background-color: #0D2C36;
  box-shadow: 0px 0px 3px 1px #12a0a0, inset 0px 0px 3px 1px #12a0a0;
}
.profile-row .dp img {
  max-width: 100%;
  border-radius: 50%;
  display: block;
  box-shadow: 0px 0px 4px 3px #12a0a0;
}
</code></pre>

<p>The <code>text-shadow</code> property gives shadow to the text, and the <code></code> property gives shadow to the elements.</p>

<p>The first three values for <code>box-shadow</code> are the same as <code>text-shadow</code> x-offset, y-offset, and blur. The fourth value is how much you want the shadow to spread, and the fifth value is the color of the shadow.</p>

<p>Notice how we are giving two shadows (outer and inner) to the <code>id-card</code> div in a single line:</p>

<pre><code class="language-css">box-shadow: 0px 0px 3px 1px #12a0a0, inset 0px 0px 3px 1px #12a0a0;
</code></pre>

<p>The first five values create an outer shadow. Then the &ldquo;inset&rdquo; keyword specifies that the next five values are for inside shadow. We separate both with a <code>,</code>.</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="wmNjXm"
   data-user="supersarkar"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<p>The Avengers ID card is ready. Yay!</p>

<h3 id="wrapping-up">Wrapping Up</h3>

<p>In this tutorial, we learned an effective way of making a full-page background, and centering elements with Flexbox and auto margins. We saw the basic usage of Flexbox and nested Flexboxes to make single dimension layouts.</p>

<p>If you want to dive deeper into Flexbox, check out “.</p>

<p>We also used CSS animations and the rotate transform to make animated arcs, however, we used a limited number of CSS properties and values. If you want to explore more about CSS animations then you will love this detailed .</p>

<p>Finally, the glowing elements gave our ID card a unique sci-fi look. We used the <code>box-shadow</code> property to give the glow to our elements. Sometimes manually setting the values of the <code>box-shadow</code> property can be cumbersome, so try using CSSmatic’s  to easily generate box shadows.</p>




<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(rb, ra, il)</span>
</div>


</div>




  <div id="sponsors-article-end" data-impression="true" class="c-promo-box c-promo-box--ad c-promo-box--wide sponsors hidden" data-audience="non-subscriber" data-remove="true"></div>



              </article>
            </body>
          </html>
---------------
<h1 id="#title_1" >2、75 亿美金，纳德拉宣布微软正式收购 GitHub</h1>
郭蕾
[http://www.infoq.com/cn/news/2018/06/github-microsoft?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/06/github-microsoft?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>北京时间6月4日晚，微软官方正式宣布以75亿美元的价格正式收购GitHub，这是微软首席执行官Satya Nadella在两年前以262亿美元收购LinkedIn之后的第二次大手笔收购。

</p> <i>By 郭蕾</i>
---------------
<h1 id="#title_2" >3、文章： 作为一名区块链架构师，需要从哪几个纬度去做技术选型？</h1>
本体, 季宙栋
[http://www.infoq.com/cn/articles/technology-selection-as-blockchain-architector?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/technology-selection-as-blockchain-architector?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/technology-selection-as-blockchain-architector/zh/smallimage/logo-1526022783167-1528019138335.jpeg"/><p> 为了更好地发展区块链技术，防范技术高速发展所孕育的潜在风险，工信部中国电子技术标准化研究院牵头组织中国区块链技术和产业发展论坛主要成员，开展了《信息技术区块链和分布式账本技术参考架构》标准的研制工作。 笔者参加了 4 月 3 日 -5 日的 ISO/IEC TC307 区块链国际标准组第一次会议，下文将对美国提交的区块链参考架构做一个简单分析并思考它的设计理念对我们国内区块链架构设计的借鉴作用。</p> <i>By 本体</i>
---------------
<h1 id="#title_3" >4、文章： 构建增强现实移动应用程序的六款顶级工具</h1>
Andrii Zhuravlov-Galchenko
[http://www.infoq.com/cn/articles/augmented-reality-best-skds?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/augmented-reality-best-skds?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/augmented-reality-best-skds/zh/headerimage/GettyImages-658404920-1526072157984.jpg"/><p>尽管很多人认为增强现实（Augmented Reality，简称AR）只是一种用于娱乐的技术，其实，它在多个行业（如医疗保健、电子商务、建筑等等）有着广泛的应用。本文将帮助您了解我们可以构建什么样的增强现实应用程序、在AR SDK中应该寻求哪些功能，并通过一张表格对比了6种广为人知的AR工具包。</p> <i>By Andrii Zhuravlov-Galchenko</i> <i> Translated by 姚佳灵</i>
---------------
<h1 id="#title_4" >5、文章： 苏宁乔新亮：世界上最好的研发管理十条经验</h1>
乔新亮
[http://www.infoq.com/cn/articles/top-10-experience-on-development-management?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/top-10-experience-on-development-management?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/top-10-experience-on-development-management/zh/smallimage/logo32-1528128953651.jpg"/><p>体系是企业里的核心竞争力</p> <i>By 乔新亮</i>
---------------
<h1 id="#title_5" >6、FEX 技术周刊 - 2018/06/04</h1>

[http://fex.baidu.com/blog/2018/06/fex-weekly-04//](http://fex.baidu.com/blog/2018/06/fex-weekly-04//)
作者：2betop <br> <p>微信搜索『FEX』关注我们的公众号，及时获得最新资讯。</p>

<h2 id="业界会议">业界会议</h2>

<p><strong>JJSConf EU</strong><br />
https://2018.jsconf.eu/<br />
可关注。附：</p>

<h2 id="深阅读">深阅读</h2>

<p><strong>deno</strong><br />
https://github.com/ry/deno<br />
A secure TypeScript runtime on V8. Node 创始人新作，基于 Go 语言. Supports TypeScript 2.8 out of the box. Uses V8 6.8.275.3. That is, it’s very modern JavaScript. No package.json, no npm. Not explicitly compatible with Node. Imports reference source code URLs only.</p>

<p><strong>Why is Front-End Development So Unstable?</strong><br />
https://www.breck-mckye.com/blog/2018/05/why-is-front-end-development-so-unstable/ <br />
Like most natural complainers I am generally better at moaning about problems than, y’know, SOLVING them. But I have a few ideas: Be wary of Medium; Be wary of self-promotion; Consider non-microlib architectures; Don’t over-sweat the employablity thing.</p>

<p><strong>Andrew Clark: React Suspense</strong><br />
https://www.youtube.com/watch?v=z-6JC0_cOns<br />
Async rendering in React gives us a powerful new set of primitives for addressing longstanding problems in UI development. I’ll discuss React’s vision for how async rendering can improve data fetching, code delivery, prefetching, view transitions, and more. 另：</p>

<p><strong>To Yarn and Back (to npm) Again</strong><br />
https://mixmax.com/blog/to-yarn-and-back-again-npm<br />
Last year, we decided to move all of our JavaScript projects from npm to Yarn. Yarn solved the annoying problems we faced using npm, but it came with issues of its own. After a couple of especially painful weeks full of 15-minute Yarn untangling sessions, we decided to take a look at moving back to npm.</p>

<p><strong>Beyond SPAs: alternative architectures for your PWA</strong><br />
https://developers.google.com/web/updates/2018/05/beyond-spa<br />
I’m going to cover an important, but potentially misunderstood topic: The architecture that you use for your web app, and specifically, how your architectural decisions come into play when you’re building a progressive web app.  <br />
另附：</p>

<p><strong>The Cult of the Complex</strong><br />
http://alistapart.com/article/cult-of-the-complex<br />
There’s a lot of complexity to good design. Technical complexity. UX complexity. Challenges of content and microcopy. Performance challenges. This has never been and never will be an easy job. Simplicity is not easy—not for us, anyway. Simplicity means doing the hard work that makes experiences appear seamless—the sweat and torture-testing and failure that eventually, with enough effort, yields experiences that seem to “just work.”</p>

<p><strong>如何用练习快速提升技术</strong><br />
https://mp.weixin.qq.com/s?__biz=MjM5Mjg4NDMwMA==&amp;mid=2652975915&amp;idx=1&amp;sn=1d0c3bb0937e3d9cf1f74b1257c7aacc<br />
有人可以靠中彩票，然后一夜暴富；有人随随便便发几张自拍，就一不小心一夜成名。可技术成长，要一步一个脚印地练习，才能掌握某项特定技术。等到我们掌握了学习的技巧，才能用更短的时间，来掌握某项特定的技术。而练习，也不是一天里写一万行代码，也不是重复写一百行代码，而是在一百天里，每天写下一百行代码。它需要一定的技巧，不懈的坚持，还有一些休息。因此在这篇文章里，我将分享工作几年里的练习技巧。</p>

<p><strong>浅谈 2018 移动端跨平台开发方案</strong><br />
https://juejin.im/post/5b076e3af265da0dce48fe95<br />
介绍目前几个方案的现状。其实在超级 App 流行的当下，跨 App （微信、支付宝、淘宝、百度等）才是一大难题。</p>

<p><strong>头条PC站基于RIOT的组件化开发实践</strong><br />
https://techblog.toutiao.com/2018/05/29/untitled-25/<br />
是一种小而美的js框架，2.2.4稳定版本兼容IE8。采用该框架在头条pc站进行了组件化开发方式的实践，有效地提高了开发效率和扩展能力，并大大降低了维护成本。</p>

<p><strong>Node.js 2018年大前端潮流解析</strong><br />
https://mp.weixin.qq.com/s?__biz=MzAxMTU0NTc4Nw==&amp;mid=2661157679&amp;idx=1&amp;sn=9570b1c8db32eed895e6c06c450771fe<br />
大前端已经是Web前端和客户端开发的趋势，加上Node的横空出世，移动端设备提升、HTML5能力加强，移动和前端的融合也已不可逆转。在如此多变的技术浪潮下，作为一个前端人，该如何辨识清楚技术的发展方向，又该怎么学习呢？</p>

<p><strong>淘宝Web 3D应用与游戏开发</strong><br />
https://mp.weixin.qq.com/s?__biz=MzAxNDEwNjk5OQ==&amp;mid=2650401461&amp;idx=1&amp;sn=695615d75dc2409ac0f461c7fd55710e <br />
详细解释了3D与2D的区别，并阐述了在有限的环境下，淘宝技术虚拟互动团队是如何通过Canvas去实现3D效果。随着Web GL的发展，如何在手机淘宝中实践，以及在项目中如何与Unity结合提升开发效率。而现在，团队希望能够实现一个可视化的编辑器，帮助开发者快速得构建出相关的应用。</p>

<p><strong>移动端本地 H5 秒开方案探索与实现</strong><br />
https://mp.weixin.qq.com/s/0OR4HJQSDq7nEFUAaX1x5A<br />
如何通过本地加载来提升性能</p>

<p><strong>群消息，究竟存1份还是多份？</strong><br />
https://mp.weixin.qq.com/s/1Pd0vhDu8lh9bpvKGQqLVA<br />
为什么存一份是更好的方案</p>

<p><strong>CSS Is So Overpowered It Can Deanonymize Facebook Users</strong><br />
https://www.bleepingcomputer.com/news/security/css-is-so-overpowered-it-can-deanonymize-facebook-users/<br />
Some of the recent additions to the Cascading Style Sheets (CSS) web standard are so powerful that a security researcher has abused them to deanonymize visitors to a demo site and reveal their Facebook usernames, avatars, and if they liked a particular web page of Facebook.</p>

<p><strong>Reconciling GraphQL and Thrift at Airbnb</strong><br />
https://medium.com/airbnb-engineering/reconciling-graphql-and-thrift-at-airbnb-a97e8d290712<br />
Our frontend engineers wanted rapid iteration and flexibility from GraphQL, while our backend engineers wanted stability and specificity from Thrift. This is the story of how we got the two groups talking and built something that works for everyone. <br />
另附：</p>

<p><strong>A cartoon intro to DNS over HTTPS</strong><br />
https://hacks.mozilla.org/2018/05/a-cartoon-intro-to-dns-over-https/<br />
Two more protections we’re adding to that list are: DNS over HTTPS, a new IETF standards effort that we’ve championed; Trusted Recursive Resolver, a new secure way to resolve DNS that we’ve partnered with Cloudflare to provide. With these two initiatives, we’re closing data leaks that have been part of the domain name system since it was created 35 years ago. And we’d like your help in testing them. So let’s look at how DNS over HTTPS and Trusted Recursive Resolver protect our users. But first, let’s look at how web pages move around the Internet.</p>

<p><strong>UTC is Enough for Everyone, Right?</strong><br />
https://zachholman.com/talk/utc-is-enough-for-everyone-right<br />
Programming time, dates, timezones, recurring events, leap seconds… everything is pretty terrible. The common refrain in the industry is Just use UTC! Just use UTC! And that’s correct… sort of. But if you’re stuck building software that deals with time, there’s so much more to consider. It’s time… to talk about time.</p>

<p><strong>Bad Practices in Database Design: Are You Making These Mistakes?</strong><br />
https://www.toptal.com/database/database-design-bad-practices<br />
In this article, you will learn about some of the common database design bad practices, why they are bad, and how you can avoid them.</p>

<p><strong>10 GitHub Security Best Practices</strong><br />
https://snyk.io//blog/ten-git-hub-security-best-practices/<br />
So let’s get started with our list of 10 GitHub security best practices, starting with the classic mistake of people adding their passwords into their GitHub repositories!</p>

<p><strong>How the Go runtime implements maps efficiently (without generics)</strong><br />
https://dave.cheney.net/2018/05/29/how-the-go-runtime-implements-maps-efficiently-without-generics<br />
This post discusses how maps are implemented in Go.</p>

<p><strong>A new fast hash table in response to Google’s new fast hash table</strong><br />
https://probablydance.com/2018/05/28/a-new-fast-hash-table-in-response-to-googles-new-fast-hash-table/<br />
I wrote my new favorite hash table. This came about because last year I wrote the fastest hash table (I still make that claim) and this year one of the organizers of the C++Now conference asked me to give a talk. My problem was that Google had also announced a new fast hash table last year, and I wasn’t sure if mine would compare well against theirs.</p>

<p><strong>How to Create a Team-Health Assessment for Engineering Organizations</strong><br />
https://blog.newrelic.com/2018/05/29/team-health-assessment/<br />
Talking with folks in various leadership roles at New Relic, I heard a lot of stories about the successes and failures of this new model. But it was all anecdotes, it wasn’t real data. We needed something more concrete if we wanted to understand what was going on in these new teams and drive the positive changes we wanted to make. At the same time I was having these conversations, the Agile Fluency Project released an agile practices diagnostic for teams, and the proverbial light bulb appeared: We needed to do team health assessments. This is the story of how we developed and implemented our assessments.</p>

<p><strong>30 years later, QBasic is still the best</strong><br />
http://www.nicolasbize.com/blog/30-years-later-qbasic-is-still-the-best/<br />
My quest has led me to endless forums, through which I have tried countless suggestions: SmallBasic, Pico-8, Smalltalk, Scratch, etc. I have even inquired of the Great Oracles of StackOverflow, to no avail. After 5 months, I ended up with a disappointing conclusion: nothing is even close to what I had back in another era. 30 years later, QBasic is still the best when it comes to discovering programming. <br />
另附：</p>

<h2 id="新鲜货">新鲜货</h2>

<p><strong>MINT</strong><br />
https://www.mint-lang.com/<br />
对现有 JavaScript 不满意，于是造了个语言，自带类似 React+Redux 的框架，自己也是基于一个不参加的语言 Crystal 开发的</p>

<p><strong>Jest 23: Blazing Fast Delightful Testing</strong><br />
https://facebook.github.io/jest/blog/2018/05/29/jest-23-blazing-fast-delightful-testing.html<br />
We would also like to welcome both Babel and Webpack to the Jest community! After converting from Mocha to Jest 23 Beta, Webpack saw their total test suite time reduced 6x from over 13 minutes to 2 minutes 20 seconds.</p>

<p><strong>Announcing TypeScript 2.9</strong><br />
https://blogs.msdn.microsoft.com/typescript/2018/05/31/announcing-typescript-2-9/<br />
TS 党可以关注下新特性</p>

<p><strong>Getting Started with Live Coding in Visual Studio Code w/ Live Share</strong><br />
https://scotch.io/tutorials/getting-started-with-live-coding-in-visual-studio-code-with-live-share<br />
Live Share is an extension for VS Code that enables real-time collaboration between developers. As you’ll see in a second, you’ll have the ability to share a “session” with someone else, allowing them to edit code as well as share a sever and debugging session. I’ve seen real-time collaboration in action with Cloud 9 before, but to have this now be a part of my favorite text editor is extremely exciting! So, let’s go ahead and take a look at how it works.</p>

<p><strong>ServiceWorker Cookbook</strong><br />
https://serviceworke.rs/<br />
The Service Worker Cookbook is a collection of working, practical examples of using service workers in modern web sites.</p>

<p><strong>Chromely</strong><br />
https://github.com/mattkol/Chromely<br />
Chromely is a lightweight alternative to Electron.NET, Electron for .NET/.NET Core developers. Chromely is a .NET/.NET Core HTML5 Chromium desktop framework. It is focused on building apps based on Xilium.CefGlue, CefSharp implementations of embedded Chromium (Cef) without WinForms or WPF. Chromely uses Windows and Linux native GUI API as “thin” chromium hosts. It can be extended to use WinForms or WPF.</p>

<p><strong>ProppyJS - Functional props composition for UI components</strong><br />
https://proppyjs.com/<br />
Functional props composition for components</p>

<p><strong>Smooth UI</strong><br />
https://github.com/smooth-code/smooth-ui<br />
Smooth UI is an open source components library built with React and Styled Components.</p>

<p><strong>Kit</strong><br />
https://compositor.io/kit/<br />
Tools for developing, documenting, and testing React component libraries.</p>

<p><strong>React-Move</strong><br />
https://github.com/react-tools/react-move<br />
Beautiful, data-driven animations for React.</p>

<p><strong>slugify</strong><br />
https://github.com/sindresorhus/slugify<br />
Slugify a string. Useful for URLs, filenames, and IDs.</p>

<p><strong>Reach Router</strong><br />
https://github.com/reach/router<br />
Router manages the focus of your app on route transitions. There’s nothing you have to do about it, it just happens.</p>

<p><strong>Visual Studio 完全AI手册</strong><br />
https://www.cnblogs.com/ms-uap/p/9123033.html<br />
开发环境搭建与离线模型训练</p>

<p><strong>CurrencyFormatter.js</strong><br />
https://osrec.github.io/currencyFormatter.js/<br />
A super simple currency formatting library. 155 currencies, 715 locales &amp; less than 7KB gzipped.</p>

<p><strong>Chatkit - Developer-driven chat done simply</strong><br />
https://pusher.com/chatkit<br />
Adding chat to your app has never been so easy. Integrate Chatkit with your app and engage users via realtime messaging. No more infrastructure hell, no hassle, just add it.</p>

<p><strong>Mastodon</strong><br />
https://github.com/tootsuite/mastodon<br />
Mastodon is a free, open-source social network server based on open web protocols like ActivityPub and OStatus. The social focus of the project is a viable decentralized alternative to commercial social media silos that returns the control of the content distribution channels to the people. The technical focus of the project is a good user interface, a clean REST API for 3rd party apps and robust anti-abuse tools.</p>

<p><strong>High school physics course notes, with JavaScript simulations</strong><br />
https://landgreen.github.io/physics/index.html<br />
This page contains notes for introductory high school physics. It was written for my students, but it might be useful for anyone learning physics. All notes, simulations, and examples were written by Ross Landgreen unless otherwise attributed. Most of the work was done between 2017-2018. The simulations were written in JavaScript, outputting to canvas or SVG.</p>

<p><strong>Join the GitHub Learning Lab Explorer Challenge</strong><br />
https://blog.github.com/2018-05-29-join-the-github-learning-lab-explorer-challenge/<br />
From May 23 to June 26, GitHub is hosting a challenge in the Community Forum where you can be recognized for leveling up your knowledge with GitHub Learning Lab. To participate, visit lab.github.com and sign in with your GitHub account. Complete at least three courses, and head to the challenge page on the Community Forum for details on completing your submission.</p>

<p><strong>GitHub Co-Founder Chris Wanstrath Steps Down From CEO Role</strong><br />
https://www.inc.com/business-insider/github-ceo-chris-wanstrath-steps-down-second-time.html<br />
另附：</p>

<h2 id="设计">设计</h2>

<p><strong>「得到」的猫头鹰Logo 是怎么诞生的</strong><br />
https://www.uisdc.com/iget-owl-logo-birth<br />
来看主创设计师怎么说！</p>

<p><strong>Small Stars of Big Design: Review of Interactive UI Elements</strong><br />
https://uxplanet.org/small-stars-of-big-design-review-of-interactive-ui-elements-fe856eafe0a2<br />
Powerful and user-friendly product designs are based on elaborately crafted details. Web and mobile user interfaces are all packed with small elements of big impact. Today we offer you to revise some of the UI elements found in the vast majority of layouts, consider their functionality and role and check them in various examples by studio designers. So, let’s get started!</p>

<p><strong>A Reference Guide For Typography In Mobile Web Design</strong><br />
https://www.smashingmagazine.com/2018/06/reference-guide-typography-mobile-web-design/<br />
With mobile taking a front seat in search, it’s important that websites are designed in a way that prioritize the best experience possible for their users. While Google has brought attention to elements like pop-ups that might disrupt the mobile experience, what about something as seemingly simple as choice of typography? The answer to the typography question might seem simple enough: what works on desktop should work on mobile so long as it scales well. Right?</p>

<p><strong>9 inspiring redesign concepts for popular websites</strong><br />
https://www.invisionapp.com/blog/popular-website-redesigns/<br />
What if you had free rein to completely redesign one of your favorite websites? As a creative exercise, the designers below did just that for YouTube, LinkedIn, Trello, and more. Here are our nine favorite website redesigns.</p>

<p><strong>How not to write an error message</strong><br />
https://webflow.com/blog/how-not-to-write-an-error-message<br />
Discover all the ways the internet’s most well-meaning messages can go horribly, horribly wrong.</p>

<p><strong>An intro to Machine Learning for designers</strong><br />
https://uxdesign.cc/an-intro-to-machine-learning-for-designers-5c74ba100257<br />
The basics of machine learning and how to apply it to the products you are building right now.</p>

<h2 id="产品及其它">产品及其它</h2>

<p><strong>Security culture, the Dropbox way</strong><br />
https://blogs.dropbox.com/tech/2018/06/security-culture-the-dropbox-way/<br />
The first core company value at Dropbox is “Be Worthy of Trust.” From a security perspective, this means keeping our users’ stuff safe. Our culture of security is built on this foundation of trust and is a fundamental part of our identity. We have a dedicated Security Culture Team whose mission is to cultivate an environment where our employees make consistently secure and informed decisions that protect Dropbox, our users, our employees, and our physical spaces.</p>

<p><strong>Announcing the How to Sell Guide</strong><br />
https://www.entrepidpartners.com/how-to-sell-guide<br />
In our years of coaching dozens of Silicon Valley SaaS startups, we’ve seen a lot of things trip otherwise great teams up. One of the biggest fundamentals? How to sell. With that in mind, we’ve to developed our first-ever guide, How to Sell, designed to give you and your team the tools you need to understand how to build and scale a repeatable sales process.</p>

<p><strong>2018互联网女皇趋势报告</strong><br />
https://36kr.com/p/5136516.html<br />
附：</p>

<p><strong>教育真的可以改变命运和阶层吗</strong><br />
https://mp.weixin.qq.com/s?__biz=MzA4NzQ5MTA2NA==&amp;mid=2653634061&amp;idx=1&amp;sn=cd7a6e35ab9e3a3d80aafa0189d53f90<br />
一方面我们说教育改变命运，但又发现出现了“教育无用论”。有人说教育一定是出了问题。问题是出在学校社会家长，还是出在学生呢？这些原因可能都有，但更重要的可能是我们需要从另外一个角度和眼光来看待这个问题。</p>

<p>– THE END –</p>
---------------
<h1 id="#title_6" >7、在敏捷中应用即兴游戏</h1>
Ben Linders
[http://www.infoq.com/cn/news/2018/06/improv-agile-games?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/06/improv-agile-games?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>即兴为提升积极倾听、协作和相互强化技能提供了简便的方法，而所有这些因素对于敏捷来说都是不可或缺的。整合即兴活动和游戏有助于强化敏捷思维。与其他活动一样，游戏的价值通过汇报的方式得到实现，因为它将游戏体验中的情绪和顿悟时刻与并行工作场景联系在一起。</p> <i>By Ben Linders</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_7" >8、VPNFilter已经感染了全球50万台以上的路由器</h1>
Sergio De Simone
[http://www.infoq.com/cn/news/2018/06/vpnfilter-router-malware?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/06/vpnfilter-router-malware?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>思科公司的安全研究人员发布了一份安全警告，报告中描述了一个复杂的恶意软件系统VPNFilter，该系统已经感染了分布于54个国家的至少50万台网络设备。</p> <i>By Sergio De Simone</i> <i> Translated by 姚佳灵</i>
---------------
<h1 id="#title_8" >9、GDPR生效后Unroll.me和Pinterest的Instapaper在欧洲无法使用</h1>
Charles Humble
[http://www.infoq.com/cn/news/2018/06/gdpr-instapaper-unavailable?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/06/gdpr-instapaper-unavailable?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>虽然企业从2016年4月14日就开始为欧洲的通用数据保护条例（GDPR）做准备，但是，许多企业到最后期限到来时还是没有做好准备，有许多服务在欧洲已经无法使用了。</p> <i>By Charles Humble</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_9" >10、APICloud以生态之力创造API新经济</h1>
覃云
[http://www.infoq.com/cn/news/2018/06/APICloud-API?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/06/APICloud-API?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>5月29日，APICloud新一轮融资暨战略发布会在北京举行，会上披露了APICloud B轮融资金额为1亿元人民币，由复星集团领投。</p> <i>By 覃云</i>
---------------
<h1 id="#title_10" >11、消息称微软计划收购GitHub，估值超50亿美元</h1>
郭蕾
[http://www.infoq.com/cn/news/2018/06/Sources-Microsoft-plans-GitHub-v?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/06/Sources-Microsoft-plans-GitHub-v?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>据知情人士介绍，微软公司最近就收购 GitHub 一事召开相关会议。这意味着双方再次开启多年以来断断续续的对话通道。</p> <i>By 郭蕾</i>
---------------