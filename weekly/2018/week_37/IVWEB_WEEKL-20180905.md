## 文章索引
1、 <a href="#1take-a-new-look-at-css-shapes" >Take A New Look At CSS Shapes</a><br/>
2、 <a href="#2文章-构建一个运行在azure虚拟机上的mysql-spring-boot应用程序" >文章： 构建一个运行在Azure虚拟机上的MySQL Spring Boot应用程序</a><br/>
3、 <a href="#3文章-别用大批量mini-batch训练神经网络用局部sgd" >文章： 别用大批量mini-batch训练神经网络，用局部SGD！</a><br/>
4、 <a href="#4文章-聊聊工程师的影响力" >文章： 聊聊工程师的影响力</a><br/>
5、 <a href="#5google发布app-engine第二代运行时提供python-37和php-72支持" >Google发布App Engine第二代运行时，提供Python 3.7和PHP 7.2支持</a><br/>
6、 <a href="#6如何定义敏捷教练的能力" >如何定义敏捷教练的能力</a><br/>
7、 <a href="#7加州颁布消费者隐私法" >加州颁布消费者隐私法</a><br/>
8、 <a href="#8vaughn-vernon谈云原生和反应式现状" >Vaughn Vernon谈云原生和反应式现状</a><br/><h1 id="#title_0" >1、Take A New Look At CSS Shapes</h1>
Rachel Andrew
[https://www.smashingmagazine.com/2018/09/css-shapes/](https://www.smashingmagazine.com/2018/09/css-shapes/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/09/css-shapes/" />
              <title>Take A New Look At CSS Shapes</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>Take A New Look At CSS Shapes</h1>
                  
                    
                    <address>Rachel Andrew</address>
                  
                  <time datetime="2018-09-04T13:30:57&#43;02:00" class="op-published">2018-09-04T13:30:57+02:00</time>
                  <time datetime="2018-09-04T17:39:40&#43;00:00" class="op-modified">2018-09-04T17:39:40+00:00</time>
                </header>
                

<p>CSS Shapes Level 1 has been available in Chrome and Safari for a number of years, however, this week it ships in a production version of Firefox with the release of Firefox 62 &mdash; along with a very nice addition to the Firefox DevTools to help us work with Shapes. In this article, I&rsquo;ll take a look at some of the things you can do with CSS Shapes. Perhaps it&rsquo;s time to consider adding some curves to your designs?</p>

<h3 id="what-are-css-shapes">What Are CSS Shapes?</h3>

<p>The CSS Shapes specification Level 1 defines three new properties:</p>

<ul>
<li><code>shape-outside</code></li>
<li><code>shape-image-threshold</code></li>
<li><code>shape-margin</code></li>
</ul>

<p>The purpose of this specification is to allow content to flow around a non-rectangular shape, something which is quite unusual on our boxy web. There are a few different ways to create shapes, which we will have a look at in this tutorial. We will also have a look at the Shape Path Editor, available in Firefox, as it can help you to easily understand the shapes on your page and work with them.</p>

<p>In the current specification, shapes can only be applied to a float, so any shapes example needs to start with a floated element. In the example below, I have a PNG image with a transparent background in which I have floated the image left. The text that follows the image now flows around the right and bottom of my image.</p>

<p>What I would like to happen is for my content to follow the shape of the opaque part of the image, rather than follow the line of the physical image file. To do this, I use the <code>shape-outside</code> property, with the value being the URL of my image. I&rsquo;m using the actual image file to create a path for the content to flow around.</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="KxaZXw"
   data-user="rachelandrew"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<p>Note that your image needs to be CORS compatible, so hosted on the same server as the rest of your content or sending the correct headers if hosted on a CDN. Browser DevTools will usually tell you if your image is being blocked due to CORS.</p>

<p>This method of creating shapes uses the alpha channel of the image to create the shape, as we have a shape with a fully transparent area, then all we need do is pass the URL of the image to <code>shape-outside</code> and the shape path follows the line of the fully opaque area.</p>



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




<h3 id="creating-a-margin">Creating A Margin</h3>

<p>To push the line of the text away from the image we can use the <code>shape-margin</code> property. This creates a margin between the line of the shape and the content running alongside it.</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="vzgdXw"
   data-user="rachelandrew"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<h3 id="using-generated-content-for-our-shape">Using Generated Content For Our Shape</h3>

<p>In the case above, we have the image displayed on the page and then the text curved around it. However, you could also use an image as the path for the shape in order to create a curved text effect without also including the image on the page. You still need something to float, however, and so for this, we can use Generated Content.</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="bxgLBp"
   data-user="rachelandrew"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<p>In this example, we have inserted some generated content, floated it left, given it a width and a height and then used <code>shape-outside</code> with our image just as before. We then get a curved line against the whitespace, but no visible image.</p>

<h3 id="using-a-gradient-for-our-shape">Using A Gradient For Our Shape</h3>

<p>A CSS gradient is just like an image, which means we can use a gradient to create a shape, which can make for some interesting effects. In this next example, I have created a gradient which goes from blue to transparent; your gradient will need to have a transparent or semi-transparent area in order to use shapes. Once again, I have used generated content to add the gradient and am then using the gradient in the value for <code>shape-outside</code>.</p>

<p>Once the gradient becomes fully transparent, then the shape comes into play, and the content runs along the edge of the gradient.</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="zJNRpL"
   data-user="rachelandrew"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<h3 id="using-shape-image-threshold-to-position-text-over-a-semi-opaque-image">Using <code>shape-image-threshold</code> To Position Text Over A Semi-Opaque Image</h3>

<p>So far we have looked at using a completely transparent part of an image or of a gradient in order to create our shape, however, the third property defined in the CSS Shapes specification means that we can use images or gradients with semi-opaque areas by setting a threshold. A value for <code>shape-image-threshold</code> of <code>1</code> means fully opaque while <code>0</code> means fully transparent.</p>

<p>A gradient like our example above is a great way to see this in action as we can change the <code>shape-image-threshold</code> value and move the line along which the text falls to more opaque areas or more transparent areas. This property works in exactly the same way with an image that has an alpha channel yet is not fully transparent.</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="JaEpMw"
   data-user="rachelandrew"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<p>This method of creating shapes from images and gradients is &mdash; I think &mdash; the most straightforward way of creating a shape. You can create a shape as complex as you need it to be, in the comfort of a graphics application and then use that to define the shape on your page. That said, there is another way to create our shapes, and that&rsquo;s by using <em>Basic Shapes</em>.</p>

<div class="sponsors__wide-place"></div>




<h3 id="css-shapes-with-basic-shapes">CSS Shapes With Basic Shapes</h3>

<p>The Basic Shapes are a set of predefined shapes which cover a lot of different types of shapes you might want to create. To use a basic shape, you use the basic shape <em>type</em> as a value for <code>shape-outside</code>. This type uses functional notation, so we have the name of the shape followed by brackets (inside which are some values for our shape).</p>

<p>The options that you have are the following:</p>

<ul>
<li><code>inset()</code></li>
<li><code>circle()</code></li>
<li><code>ellipse()</code></li>
<li><code>polygon()</code></li>
</ul>

<p>We will take a look at the <code>circle()</code> type first as we can use this to understand some useful things which apply to all shapes which use the basic shape type. We will also have a look at the new tools in Firefox for inspecting these shapes.</p>

<p>In the example below, I am creating the most simple of shapes: a circle using <code>shape-outside: circle(50%)</code>. I&rsquo;m using generated content again, and I have given the box a background color, and also added a margin, border, and padding to help highlight some of the concepts of using CSS Shapes. You can see in the example that the circle is created centered on the box; this is because I have given the circle a value of 50%. That value is the <code>&lt;shape-radius&gt;</code> which can be a length or a percentage. I&rsquo;ve used a percentage so that the radius is half of the size of my box.</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="dqNmvM"
   data-user="rachelandrew"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<p>This is a really good to time have a look at the shape that has been created using the Firefox Shape Path Editor. You can inspect the shape by clicking on the generated content and then clicking the little shape icon next to the property <code>shape-outside</code>; your shape will now highlight.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4ada6850-25be-4c76-b403-4a0c7e367bc4/circle.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4ada6850-25be-4c76-b403-4a0c7e367bc4/circle.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4ada6850-25be-4c76-b403-4a0c7e367bc4/circle.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4ada6850-25be-4c76-b403-4a0c7e367bc4/circle.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4ada6850-25be-4c76-b403-4a0c7e367bc4/circle.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4ada6850-25be-4c76-b403-4a0c7e367bc4/circle.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4ada6850-25be-4c76-b403-4a0c7e367bc4/circle.png"
			sizes="100vw"
			alt="The shape highlighted with a line"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The Shape Path Editor highlights the circle shape ()
		</figcaption>
	
</figure>


<p>You can see how the circle extends to the edge of the margin on our box. This is because the initial <em>reference box</em> used by our shape is <code>margin-box</code>. You already know something of reference boxes if you have ever added <code>box-sizing: border-box</code> to your CSS. When you do this, you are asking CSS to use the <code>border-box</code> and not the default <code>content-box</code> as the size of elements. In Shapes, we can also change which reference box is used. After any basic shape, add <code>border-box</code> to use the border to define the shape or <code>content-box</code> to use the edge of the content (inside the padding). For example:</p>

<pre class="break-out"><code class="language-css">.content::before {
    content: "";
    width: 150px;
    height: 150px;
    margin: 20px;
    padding: 20px;
    border: 10px solid #FC466B;
    background: linear-gradient(90deg, #FC466B 0%, #3F5EFB 100%);
    float: left;
    circle(50%) content-box;
}
</code></pre>

<p>You will see the circle appear to become much smaller. It is now using the width of the content &mdash; in this case the width of the box at 150px &mdash; rather than the margin box which includes the padding, border, and margin.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3cd0eefa-4cc2-4721-873b-6933a9643770/content-box.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3cd0eefa-4cc2-4721-873b-6933a9643770/content-box.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3cd0eefa-4cc2-4721-873b-6933a9643770/content-box.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3cd0eefa-4cc2-4721-873b-6933a9643770/content-box.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3cd0eefa-4cc2-4721-873b-6933a9643770/content-box.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3cd0eefa-4cc2-4721-873b-6933a9643770/content-box.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3cd0eefa-4cc2-4721-873b-6933a9643770/content-box.png"
			sizes="100vw"
			alt="A smaller circle is highlighted"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The content-box is the edge of the content of the square we created with our generated content ()
		</figcaption>
	
</figure>


<p>Inspecting your element in Firefox DevTools will also show you the reference boxes so you can choose which might give you the best result with your particular shape.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/89137819-2571-4164-8133-48e42f55f153/reference-boxes.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/89137819-2571-4164-8133-48e42f55f153/reference-boxes.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/89137819-2571-4164-8133-48e42f55f153/reference-boxes.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/89137819-2571-4164-8133-48e42f55f153/reference-boxes.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/89137819-2571-4164-8133-48e42f55f153/reference-boxes.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/89137819-2571-4164-8133-48e42f55f153/reference-boxes.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/89137819-2571-4164-8133-48e42f55f153/reference-boxes.png"
			sizes="100vw"
			alt="Highlights showing the margin, border and padding"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Reference boxes highlighted in Firefox ()
		</figcaption>
	
</figure>


<h5 id="the-position-value">The Position Value</h5>

<p>A second value can be passed to <code>circle()</code> which is a position; if you do not pass this value, it defaults to <code>center</code>. However, you can use this value to pull your circle around. In the next example, I have positioned the circle by using <code>shape-outside(50% at 30%)</code>; this changes where the center of the circle is positioned.</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="rZjvJW"
   data-user="rachelandrew"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<h5 id="clip-path"><code>clip-path</code></h5>

<p>Something useful to know is that the same <code>&lt;basic-shape&gt;</code> values can be used as a value for <code>clip-path</code>. This means that after creating a shape, you can clip away the image or background color that extends outside of the shape. In the example below, I am going to do this with our example gradient background, so that we end up with a circle that has text curved around from our square box.</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="dqNeJm"
   data-user="rachelandrew"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<p>All of the above concepts can be applied to our other basic shapes. Now let&rsquo;s have a quick look at how they work.</p>

<div class="sponsors__wide-place"></div>




<h4 id="inset">inset()</h4>

<p>The <code>inset()</code> value defines a rectangle. This might not seem very useful as a float is a rectangle, however, this value means that you can inset the content wrapping your shape. It takes four values for top, right, bottom, and left plus a final value which defines a border radius.</p>

<p>In the example below, I am using the values to inset the content on the right and bottom of the floated image, plus adding a border radius around which my content will wrap using <code>shape-outside: inset(0 30px 100px 0 round 40px)</code>. You can see how the content is now over the background color of the box:</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="PdWaPY"
   data-user="rachelandrew"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<h4 id="ellipse">ellipse()</h4>

<p>An ellipse is a squashed circle and as such needs two radii for x and y (in that order). You can then push the ellipse around just as with circle using the position value. In the example below, I am creating an ellipse and then using clip-path with the same values to remove the content outside of my shape.</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="bxgKwE"
   data-user="rachelandrew"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<p>In the above example, I also used <code>shape-margin</code> to demonstrate how we can use this property as with our image generated shapes to push the content away.</p>

<h4 id="polygon">polygon()</h4>

<p>Creating polygon shapes gives us the most flexibility, as our shapes can be created with three or more points. The value passed to the polygon needs to be three or more pairs of values which represent coordinates.</p>

<p>It is here where the Firefox tools become really useful as we can use them to help create our polygon. In the below example, I have created a polygon with four points. In the Firefox DevTools, you can double-click on any line to create a new point, and double-click again to remove it. Once you have created a polygon that you are happy with, you can then copy the value out of DevTools for your CSS.</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="BOpVVL"
   data-user="rachelandrew"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<h4 id="fallbacks">Fallbacks</h4>

<p>As CSS Shapes are applied to a float, in many cases the fallback is that instead of seeing the content wrap around a shape, the content will wrap around a floated element (in the way that content has always wrapped around floats). Browsers ignore properties they do not understand, so if they don&rsquo;t understand Shapes, it doesn&rsquo;t matter that the <code>shape-outside</code> property is there.</p>

<p>Where you should take care would be in any situation where not having shapes could mean that content overlaid an area which made it difficult to read. Perhaps you are using Shapes to push content away from a busy area of a background image, for example. In that case, you should first make sure that your content is usable for the non-Shapes people, then use Feature Queries to check for support of <code>shape-outside</code> and overwrite that CSS and apply the shape. For example, you could use a margin to push the content away for non-Shapes visitors and remove the margin inside your feature query.</p>

<pre><code class="language-css">.content {
    margin-left: 120px;
}

@supports (shape-outside: circle()) {
    .content {
        margin-left: 0;
        /* add the rest of your shapes CSS here */
    }

}
</code></pre>

<p>With Firefox releasing their support we now only have one main browser without support for Shapes &mdash; Edge. If you want to see Shapes support across the board you could go and , and see if we can encourage the implementation of the feature in Edge.</p>

<h4 id="find-out-more-about-css-shapes">Find Out More About CSS Shapes</h4>

<p>In this article, I&rsquo;ve tried to give a quick overview of some of the interesting things that are possible with CSS Shapes. For a more in-depth look at each feature, check out the .</p>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(il)</span>
</div>


              </article>
            </body>
          </html>
---------------
<h1 id="#title_1" >2、文章： 构建一个运行在Azure虚拟机上的MySQL Spring Boot应用程序</h1>
Brian Benz
[http://www.infoq.com/cn/articles/azure-wildfly-spring-boot-app?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/azure-wildfly-spring-boot-app?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/azure-wildfly-spring-boot-app/zh/smallimage/azure-wildfly-spring-boot-app-s-1535114484093-1535703231661.jpeg"/><p>最近，我被要求构建一个在WildFly应用程序平台上运行的演示网站，并连接到微软Azure上的MySQL数据库。前提看起来似乎很简单，但实现起来可能很棘手，而且关于如何设置这样的东西的文档也很有限。我花了很多时间来研究实现这一目标需要做些什么，我将把步骤分享给大家。</p> <i>By Brian Benz</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_2" >3、文章： 别用大批量mini-batch训练神经网络，用局部SGD！</h1>
马卓奇
[http://www.infoq.com/cn/articles/dont-use-large-mini-batch-use-local-SGD?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/dont-use-large-mini-batch-use-local-SGD?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/dont-use-large-mini-batch-use-local-SGD/zh/smallimage/logo32-1535818939624.jpg"/><p>小批量随机梯度下降是目前最常用的训练大型神经网络和其它机器学习模型的方法。但它不能自适应的调整系统通信和计算之间的权衡。此外，梯度交换的通信带宽的固定要求严重限制了多节点训练的可扩展性。而局部随机梯度方法在与其他节点通信之前能够在局部的模型上进行迭代更新，提升了整体性能和通信效率，及对系统资源的自适应性。这篇论文对局部SGD进行了层次化扩展，使其可以在异质分布式系统中有效自适应不同级别的计算消耗。</p> <i>By 马卓奇</i>
---------------
<h1 id="#title_3" >4、文章： 聊聊工程师的影响力</h1>
CHARITY.WTF
[http://www.infoq.com/cn/articles/engineers-and-influence?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/engineers-and-influence?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/engineers-and-influence/zh/smallimage/logo-small-1535706853563.jpg"/><p>作为一名工程师，你是如何获得影响力的？什么是影响力，它的根源是什么，你该如何运用它或者怎样会失去它？它与管理者的权力和影响力有什么不同？</p> <i>By CHARITY.WTF</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_4" >5、Google发布App Engine第二代运行时，提供Python 3.7和PHP 7.2支持</h1>
Steef-Jan Wiggers
[http://www.infoq.com/cn/news/2018/09/gcp-app-engine-python-php?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/09/gcp-app-engine-python-php?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>最近，Google Cloud宣布第二代App Engine标准运行时发布。第二代运行时升级了用于构建应用的Web框架和云计算平台，支持用户使用最新版本的常用语言、框架和软件库运行Web应用，其中包括了Python 3.7和PHP 7.2软件库。</p> <i>By Steef-Jan Wiggers</i> <i> Translated by 盖磊</i>
---------------
<h1 id="#title_5" >6、如何定义敏捷教练的能力</h1>
Angela Wick
[http://www.infoq.com/cn/news/2018/09/competencies-agile-coaching?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/09/competencies-agile-coaching?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>在2018年8月7日于美国圣地亚哥召开的Agile2018大会期间，国际敏捷联盟（ICAgile）针对敏捷教练这一专业而主持召开了一场专家研讨会。研讨会探讨了如何定义敏捷教练、敏捷教练应具备的能力、职业的定位及未来发展方向等问题</p> <i>By Angela Wick</i> <i> Translated by 盖磊</i>
---------------
<h1 id="#title_6" >7、加州颁布消费者隐私法</h1>
Michael Stiefel
[http://www.infoq.com/cn/news/2018/09/California-Consumer-Privacy-Act?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/09/California-Consumer-Privacy-Act?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>美国加州颁布了2018年加州消费者隐私法（CCPA，California Consumer Privacy Act），并将自2020年1月1日起生效。该法案将企业收集、储存、销售和分享消费者信息的若干权利授予消费者本身。其中，消费者指的是居住在加州的“自然人”。这是美国首个此类立法。</p> <i>By Michael Stiefel</i> <i> Translated by 盖磊</i>
---------------
<h1 id="#title_7" >8、Vaughn Vernon谈云原生和反应式现状</h1>
Jan Stenberg
[http://www.infoq.com/cn/news/2018/09/cloud-native-reactive-reality?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/09/cloud-native-reactive-reality?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>反应式、流和NoSQL是现如今的重要概念，它们非常有用，有时候，对于云原生应用程序而言，可以认为是必须的，但是，Vaughn Vernon在一篇博文中强调，并不是公司里的所有系统都必须使用所有这些概念才能从云中充分获益。</p> <i>By Jan Stenberg</i> <i> Translated by 谢丽</i>
---------------