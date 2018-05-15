## 文章索引
1、 <a href="#1a-strategy-guide-to-css-custom-properties" >A Strategy Guide To CSS Custom Properties</a><br/>
2、 <a href="#2文章-使用政府开放数据和低代码方案构建应用" >文章： 使用政府开放数据和低代码方案构建应用</a><br/>
3、 <a href="#3罗辑思维首席架构师go微服务改造实践" >罗辑思维首席架构师：Go微服务改造实践</a><br/>
4、 <a href="#4技术团队如何化剑为犁完成市场迅速扩张" >技术团队如何化剑为犁完成市场迅速扩张</a><br/>
5、 <a href="#5vr已糊facebook不服" >VR已糊？Facebook不服！</a><br/>
6、 <a href="#6细思极恐后门代码被隐藏在npm模块中差点就得逞" >细思极恐：后门代码被隐藏在npm模块中，差点就得逞</a><br/>
7、 <a href="#7得标准者得天下中国已着手建立区块链国家标准" >得标准者得天下，中国已着手建立区块链国家标准</a><br/>
8、 <a href="#8oracle正在推出其区块链产品" >Oracle正在推出其区块链产品</a><br/>
9、 <a href="#9极客时间首个订阅破万专栏诞生背后快时代中的内容匠人" >极客时间首个订阅破万专栏诞生背后：快时代中的内容匠人</a><br/><h1 id="#title_0" >1、A Strategy Guide To CSS Custom Properties</h1>
Michael Riethmuller
[https://www.smashingmagazine.com/2018/05/css-custom-properties-strategy-guide/](https://www.smashingmagazine.com/2018/05/css-custom-properties-strategy-guide/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/05/css-custom-properties-strategy-guide/" />
              <title>A Strategy Guide To CSS Custom Properties</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>A Strategy Guide To CSS Custom Properties</h1>
                  
                    
                    <address>Michael Riethmuller</address>
                  
                  <time datetime="2018-05-14T13:30:38&#43;02:00" class="op-published">2018-05-14T13:30:38+02:00</time>
                  <time datetime="2018-05-14T13:47:25&#43;00:00" class="op-modified">2018-05-14T13:47:25+00:00</time>
                </header>
                

<p>CSS Custom Properties (sometimes known as ‘CSS variables’) are now supported in all modern browsers, and people are starting to use them in production. This is great, but they’re different from variables in preprocessors, and I’ve already seen many examples of people using them without considering what advantages they offer.</p>

<p>Custom properties have a huge potential to change how we write and structure CSS and to a lesser extent, how we use JavaScript to interact with UI components. I’m not going to focus on the syntax and how they work (for that I recommend you read “”). Instead, I want to take a deeper look at strategies for getting the most out of CSS Custom Properties.</p>

<h3 id="how-are-they-similar-to-variables-in-preprocessors">How Are They Similar To Variables In Preprocessors?</h3>

<p>Custom Properties are a little bit like variables in preprocessors but have very some important differences. The first and most obvious difference is the syntax.</p>

<p>With <code>SCSS</code> we use a dollar symbol to denote a variable:</p>

<pre><code class="language-css">$smashing-red: #d33a2c;</code></pre>

<p>In Less we use an <code>@</code> symbol:</p>

<pre><code class="language-css">@smashing-red: #d33a2c;</code></pre>

<p>Custom properties follow a similar conventions and use a <code>--</code> prefix:</p>

<pre><code class="language-css">:root { --smashing-red: #d33a2c; }
.smashing-text { 
  color: var(--smashing-red);
}
</code></pre>

<p>One important difference between custom properties and variables in preprocessors is that custom properties have a different syntax for assigning a value and retrieving that value. When retrieving the value of a custom property we use the <code>var()</code> function.</p>



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


<p>The next most obvious difference is in the name. They are called ‘custom properties’ because they really are CSS properties. In preprocessors, you can declare and use variables almost anywhere, including outside declaration blocks, in media rules, or even as part of a selector.</p>

<pre><code class="language-css">$breakpoint: 800px;
$smashing-red: #d33a2c;
$smashing-things: ".smashing-text, .cats";

@media screen and (min-width: $breakpoint) {
  #{$smashing-things} {
    color: $smashing-red;
  }
}
</code></pre>

<p>Most of the examples above would be invalid using custom properties.</p>

<p>Custom properties have the same rules about where they can be used as normal CSS properties. It’s far better to think of them as dynamic properties than variables. That means they can only be used inside a declaration block, or in other words, custom properties are tied to a selector. This can be the <code>:root</code> selector, or any other valid selector.</p>

<pre><code class="language-css">:root { --smashing-red: #d33a2c; }

@media screen and (min-width: 800px) {
  .smashing-text, .cats {
    --margin-left:  1em;
  }
}
</code></pre>

<p>You can retrieve the value of a custom property anywhere you would otherwise use a value in a property declaration. This means they can be used as a single value, as part of a shorthand statement or even inside <code>calc()</code> equations.</p>

<pre><code class="language-css">.smashing-text, .cats {
  color: var(--smashing-red);
  margin: 0 var(--margin-horizontal);
  padding: calc(var(--margin-horizontal) / 2)
}
</code></pre>

<p>However, they cannot be used in media rules, or selectors including <code>:nth-child()</code>.</p>

<p>There is probably a lot more you want to know about the syntax and how custom properties work, such as how to use fallback values and can you assign variables to other variables (yes), but this basic introduction should be enough to understand the rest of the concepts in this article. For more information on the specifics of how custom properties work, you can read “” written by Serg Hospodarets.</p>

<h3 id="dynamic-vs-static">Dynamic vs. Static</h3>

<p>Cosmetic differences aside, the most significant difference between variables in preprocessors and custom properties is how they are scoped. We can refer to variables as either statically or dynamically scoped. Variables in preprocessors are static whereas custom properties are dynamic.</p>

<p>Where CSS is concerned static means that you can update the value of a variable at different points in the compilation process, but this cannot change the value of the code that came before it.</p>

<pre><code class="language-css">$background: blue;
.blue {
  background: $background;
}
$background: red;
.red {
  background: $background;
}
</code></pre>

<p>results in:</p>

<pre><code class="language-css">.blue {
  background: blue;
}
.red {
  background: red;
}
</code></pre>

<p>Once this is rendered to CSS, the variables are gone. This means that we could potentially read an <code>.scss</code> file and determine it’s output without knowing anything about the HTML, browser or other inputs. This is not the case with custom properties.</p>

<p>Preprocessors do have a kind of “block scope” where variables can be temporarily changed inside a selector, function or mixin. This changes the value of a variable inside the block, but it’s still static. This is tied to the block, not the selector.  In the example below, the variable <code>$background</code> is changed inside the <code>.example</code> block. It changes back to the initial value outside the block, even if we use the same selector.</p>

<pre><code class="language-css">$background: red;
.example {
  $background: blue;
  background: $background;
}

.example {
  background: $background;
}
</code></pre>

<p>This will result in:</p>

<pre><code class="language-css">.example {
  background: blue;
}
.example {
  background: red;
}
</code></pre>

<p>Custom properties work differently. Where custom properties are concerned, dynamically scoped means they are subject to inheritance and the cascade. The property is tied to a selector and if the value changes, this affects all matching DOM elements just like any other CSS property.</p>

<p>This is great because you can change the value of a custom property inside a media query, with a pseudo selector such as hover, or even with JavaScript.</p>

<pre><code class="language-css">a {
  --link-color: black;
}
a:hover,
a:focus {
  --link-color: tomato;
}
@media screen and (min-width: 600px) {
  a {
    --link-color: blue;
  }
}

a {
  color: var(--link-color);
}
</code></pre>

<p>We don’t have to change where the custom property is used &mdash; we change the value of the custom property with CSS. This means using the same custom property, we can have different values in different places or context on the same page.</p>

<h3 id="global-vs-local">Global vs. Local</h3>

<p>In addition to being static or dynamic, variables can also be either global or local. If you write JavaScript, you will be familiar with this. Variables can either be applied to everything inside an application, or their scope can be limited to specific functions or blocks of code.</p>

<p>CSS is similar. We have some things that are applied globally and some things that are more local. Brand colors, vertical spacing, and typography are all examples of things you might want to be applied globally and consistently across your website or application. We also have local things. For example, a button component might have a small and large variant. You wouldn’t want the sizes from these buttons to be applied to all input elements or even every element on the page.</p>


  <div id="sponsors-article" data-impression="true" class="c-promo-box c-promo-box--ad sponsors hidden" data-audience="non-subscriber" data-remove="true"></div>



<p>This is something we are familiar with in CSS. We’ve developed design systems, naming conventions and JavaScript libraries, all to help with isolating local components and global design elements. Custom properties provide new options for dealing with this old problem.</p>

<p>CSS Custom Properties are by default locally scoped to the specific selectors we apply them to. So they are kinda like local variables. However, custom properties are also inherited, so in many situations they behave like global variables &mdash; especially when applied to the <code>:root</code> selector. This means that we need to be thoughtful about how to use them.</p>

<p>So many examples show custom properties being applied to the <code>:root</code> element and although, this fine for a demo, it can result in a messy global scope and unintended issues with inheritance. Luckily, we’ve already learned these lessons.</p>

<h4 id="global-variables-tend-to-be-static">Global Variables Tend To Be Static</h4>

<p>There are a few small exceptions, but generally speaking, most global things in CSS are also static.</p>

<p>Global variables like brand colors, typography and spacing don&rsquo;t tend to change much from one component to the next. When they do change this tends to be a global rebranding or some other significant change that rarely happens on a mature product. It still makes sense for these things to be variables, they are used in many places, and variables help with consistency. But it doesn’t make sense for them to be dynamic. The value of these variables does not change in any dynamic way.</p>

<p>For this reason, <strong>I strongly recommend using preprocessors for global (static) variables.</strong> This not only ensures that they are always static, but it visually denotes them within the code. This can make CSS a whole lot more readable and easier to maintain.</p>

<h4 id="local-static-variables-are-ok-sometimes">Local Static Variables Are OK (Sometimes)</h4>

<p>You might think given the strong stance on global variables being static, that by reflection, all local variables might need to be dynamic. While it’s true that local variables do tend to be dynamic, this is nowhere near as strong as the tendency for a global variable to be static.</p>

<p>Locally static variables are perfectly  OK in many situations. I use preprocessors variables in component files mostly as a developer convenience.</p>

<p>Consider the classic example of a button component with multiple size variations.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b8f668c2-7b33-4fe9-a410-210138e711d6/buttons-small-medium-large.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b8f668c2-7b33-4fe9-a410-210138e711d6/buttons-small-medium-large.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b8f668c2-7b33-4fe9-a410-210138e711d6/buttons-small-medium-large.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b8f668c2-7b33-4fe9-a410-210138e711d6/buttons-small-medium-large.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b8f668c2-7b33-4fe9-a410-210138e711d6/buttons-small-medium-large.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b8f668c2-7b33-4fe9-a410-210138e711d6/buttons-small-medium-large.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b8f668c2-7b33-4fe9-a410-210138e711d6/buttons-small-medium-large.png"
			sizes="100vw"
			alt="buttons"
		/>
	</a>

	
</figure>


<p>My <code>scss</code> might look something like this:</p>

<pre><code class="language-css">$button-sml: 1em;
$button-med: 1.5em;
$button-lrg: 2em;

.btn {
  // Visual styles
}

.btn-sml {
  font-size: $button-sml;
}

.btn-med {
  font-size: $button-med;
}

.btn-lrg {
  font-size: $button-lrg;
}
</code></pre>

<p>Obviously, this example would make more sense if I was using the variables multiple times or deriving margin and padding values from the size variables. However, the ability to quickly prototype different sizes might be a sufficient reason.</p>

<p>Because most static variables are global, I like to differentiate static variables that are used only inside a component. To do this, you can prefix these variables with the component name, or you could use another prefix such as <code>c-variable-name</code> for component or <code>l-variable-name</code> for local. You can use whatever prefix you want, or you can prefix global variables. Whatever you choose, it’s helpful to differentiate especially if converting an existing codebase to use custom properties.</p>

<h3 id="when-to-use-custom-properties">When To Use Custom Properties</h3>

<p>If it is alright to use static variables inside components, when should we use custom properties? Converting existing preprocessor variables to custom properties usually makes little sense. After all, the reason for custom properties is completely different. Custom properties make sense when we have CSS properties that change relative to a condition in the DOM &mdash; especially a dynamic condition such as <code>:focus</code>, <code>:hover</code>, media queries or with JavaScript.</p>

<p>I suspect we will always use some form of static variables, although we might need fewer in future, as custom properties offer new ways to organise logic and code. Until then, I think in most situations we are going to be working with a combination of preprocessor variables and custom properties.</p>

<p>It&rsquo;s helpful to know that we can assign static variables to custom properties. Whether they are global or local, it makes sense in many situations to convert static variables, to locally dynamic custom properties.</p>

<p><strong>Note</strong>: <em>Did you know that <code>$var</code> is valid value for a custom property? Recent versions of Sass recognize this, and therefore we need to interpolate variables assigned to custom properties, like this: <code>#{$var}</code>. This tells Sass you want to output the value of the variable, rather than just $var in the stylesheet. This is only needed for situations like custom properties, where a variable names can also be a valid CSS.</em></p>

<p>If we take the button example above and decide all buttons should use the small variation on mobile devices, regardless of the class applied in the HTML, this is now a more dynamic situation. For this, we should use custom properties.</p>

<pre><code class="language-css">$button-sml: 1em;
$button-med: 1.5em;
$button-lrg: 2em;

.btn {
  --button-size: #{$button-sml};
}

@media screen and (min-width: 600px) {
  .btn-med {
    --button-size: #{$button-med};
  }
  .btn-lrg {
    --button-size: #{$button-lrg};
  }
}

.btn {
  font-size: var(--button-size);
}
</code></pre>

<p>Here I create a single custom property: <code>--button-size</code>. This custom property is initially scoped to all button elements using the <code>btn</code> class. I then change the value of <code>--button-size</code> above 600px for the classes <code>btn-med</code> and <code>btn-lrg</code>. Finally, I apply this custom property to all button elements in one place.</p>

<h3 id="don-t-be-too-clever">Don&rsquo;t Be Too Clever</h3>

<p>The dynamic nature of custom properties allows us to create some clever and complicated components.</p>

<p>With the introduction of preprocessors, many of us created libraries with clever abstractions using mixins and custom functions. In limited cases, examples like this are still useful today, but for the most part, the longer I work with preprocessors the fewer features I use. Today, I use preprocessors almost exclusively for static variables.</p>

<p>Custom properties will not (and should not) be immune from this type of experimentation, and I look forward to seeing many clever examples. But in the long run, readable and maintainable code will always win over clever abstractions (at least in production).</p>

<p>I read an excellent article on this topic on the Free Code Camp Medium recently. It was written by Bill Sourour and is called “.” Rather than paraphrasing his arguments, I&rsquo;ll let you read it.</p>

<p>One key difference between preprocessor variables and custom properties is that custom properties work at runtime. This means things that might have been borderline acceptable, in terms of complexity, with preprocessors might not be a good idea with custom properties.</p>

<p>One example that illustrated this for me recently was this:</p>

<pre class="break-out"><code class="language-css">:root {
  --font-scale: 1.2;
  --font-size-1: calc(var(--font-scale) * var(--font-size-2));
  --font-size-2: calc(var(--font-scale) * var(--font-size-3)); 
  --font-size-3: calc(var(--font-scale) * var(--font-size-4));   
  --font-size-4: 1rem;     
}
</code></pre>

<p>This generates a modular scale. A modular scale is a series of numbers that relate to each other using a ratio. They are often used in web design and development to set font-sizes or spacing.</p>

<p>In this example, each custom property is determined using <code>calc()</code>, by taking the value of the previous custom property and multiplying this by the ratio. Doing this, we can get the next number in the scale.</p>

<p>This means the ratios are calculated at run-time and you can change them by updating only the value of the <code>--font-scale</code> property. For example:</p>

<pre><code class="language-css">@media screen and (min-width: 800px) {
  :root {
    --font-scale: 1.33;
  }
}
</code></pre>

<p>This is clever, concise and much quicker than calculating all the values again should you want to change the scale. It’s also something I would <em>not</em> do in production code.</p>

<p>Although the above example is useful for prototyping, in production, I&rsquo;d much prefer to see something like this:</p>

<pre><code class="language-css">:root {
  --font-size-1: 1.728rem;
  --font-size-2: 1.44rem;
  --font-size-3: 1.2em;
  --font-size-4: 1em;
}

@media screen and (min-width: 800px) {
  :root {
    --font-size-1: 2.369rem; 
    --font-size-2: 1.777rem;     
    --font-size-3: 1.333rem; 
    --font-size-4: 1rem;     
  }
}
</code></pre>

<p>Similar to the example in Bill&rsquo;s article, I find it helpful to see what the actual values are. We read code many more times than we write it and global values such as font scales change infrequently in production.</p>

<p>The above example is still not perfect. It violates the rule from earlier that <strong>global values should be static</strong>. I&rsquo;d much prefer to use preprocessor variables and convert them to locally dynamic custom properties using the techniques demonstrated earlier.</p>

<p>It is also important to avoid situations where we go from using one custom property to a different custom property. This can happen when we name properties like this.</p>

<h3 id="change-the-value-not-the-variable">Change The Value Not The Variable</h3>

<p>Change the value not the variable is one of the most important strategies for using custom properties effectively.</p>

<p>As a general rule, you should never change which custom property is used for any single purpose.
It&rsquo;s easy to do because this is exactly how we do things with preprocessors, but it makes little sense with custom properties.</p>

<p>In this example, we have two custom properties that are used on an example component. I switch from using the value of <code>--font-size-small</code> to <code>--font-size-large</code> depending on the screen size.</p>

<pre><code class="language-css">:root {
  --font-size-small: 1.2em;
  --font-size-large: 2em;            
}
.example {
  font-size: var(--font-size-small);
}
@media screen and (min-width: 800px) {
  .example {
    font-size: var(--font-size-large);
  }
}
</code></pre>

<p>A better way to do this would be to define a single custom property scoped to the component. Then using a media query, or any other selector, change its value.</p>

<pre><code class="language-css">.example {
  --example-font-size: 1.2em;
}
@media screen and (min-width: 800px) {                             
  .example {
    --example-font-size: 2em;            
  }
}
</code></pre>

<p>Finally, in a single place, I use the value of this custom property:</p>

<pre><code class="language-css">.example {
  font-size: var(--example-font-size);
}
</code></pre>
  

<p>In this example and others before it, media queries have only been used to change the value of custom properties. You might also notice there is only one place where the <code>var()</code> statement is used, and regular CSS properties are updated.</p>

<p>This separation between variable declarations and property declarations is intentional. There are many reasons for this, but the benefits are most obvious when thinking about responsive design.</p>

<h3 id="responsive-design-with-custom-properties">Responsive Design With Custom Properties</h3>

<p>One of the difficulties with responsive design when it relies heavily on media queries is that the no matter how you organize your CSS, styles relating to a particular component become fragmented across the stylesheet.</p>

<p>It can be very difficult to know what CSS properties are going to change. Still, CSS Custom Properties can help us organize some of the logic related to responsive design and make working with media queries a lot easier.</p>

<h4 id="if-it-changes-it-s-a-variable">If It Changes It&rsquo;s A Variable</h4>

<p>Properties that change using media queries are inherently dynamic and custom properties provide the means to express dynamic values in CSS. This means that if you are using a media query to change any CSS property, you should place this value in a custom property.</p>

<p>You can then move this, along with all the media rules, hover states or any dynamic selectors that define how the value changes, to the top of the document.</p>

<h4 id="separate-logic-from-design">Separate Logic From Design</h4>

<p>When done correctly, separation of logic and design means that <strong>media queries are only be used to change the value of custom properties</strong>. It means all the logic related to responsive design should be at the top of the document, and wherever we see a <code>var()</code> statement in our CSS, we immediately know that this property that changes. With traditional methods of writing CSS, there was no way of knowing this at a glance.</p>

<p>Many of us got very good at reading and interpreting CSS at a glance while tracking in our head which properties changed in different situations. I’m tired of this, and I don&rsquo;t want to do this anymore! Custom properties now provide a link between logic and its implementation, so we don’t need to track this, and that is incredibly useful!</p>

<h4 id="the-logic-fold">The Logic Fold</h4>

<p>The idea of declaring variables at the top of a document or function is not a new idea. It&rsquo;s something we do in most languages, and it&rsquo;s now something we can do in CSS as well. Writing CSS in this way creates a clear visual distinction between CSS at the top of the document and below. I need a way to differentiate these sections when I talk about them and the idea of a &ldquo;logic fold&rdquo; is a metaphor I’ve started using.<br />
Above the fold contains all preprocessor variables and custom properties. This includes all the different values a custom property can have. It should be easy to trace how a custom property changes.</p>

<p>CSS below the fold is straightforward and highly declarative and easy to read. It feels like CSS before media queries and other necessary complexities of modern CSS.</p>

<p>Take a look at a really simple example of a six column flexbox grid system:</p>

<pre><code class="language-css">.row {
  --row-display: block;
}
@media screen and (min-width: 600px) {
  .row {
    --row-display: flex;
  }
}
</code></pre>

<p>The <code>--row-display</code> custom property is initially set to block. Above 800px the display mode is set to flex.</p>

<p>Below the fold might look like this:</p>

<pre><code class="language-css">.row {
  display: var(--row-display);
  flex-direction: row;
  flex-wrap: nowrap;
}
.col-1, .col-2, .col-3,
.col-4, .col-5, .col-6 {
  flex-grow: 0;
  flex-shrink: 0;
}
.col-1 { flex-basis: 16.66%; }
.col-2 { flex-basis: 33.33%; }
.col-3 { flex-basis: 50%; }
.col-4 { flex-basis: 66.66%; }
.col-5 { flex-basis: 83.33%; }
.col-6 { flex-basis: 100%; }
</code></pre>

<p>We immediately know <code>--row-display</code> is a value that changes. Initially, it will be <code>block</code>, so the flex values will be ignored.</p>

<p>This example is fairly simple, but if we expanded it to include a flexible width column that fills the remaining space, it&rsquo;s likely <code>flex-grow</code>, <code>flex-shrink</code> and <code>flex-basis</code> values would need to be converted to custom properties. You can try this or take a .</p>

<h3 id="custom-properties-for-theming">Custom Properties For Theming</h3>

<p>I&rsquo;ve mostly argued against using custom properties for global dynamic variables and hopefully implied that attaching custom properties to the <code>:root</code> selector is in many cases considered harmful. But every rule has an exception, and for custom properties, it&rsquo;s theming.</p>

<p>Limited use of global custom properties can make theming a whole lot easier.</p>

<p>Theming generally refers to letting users customize the UI in some way. This could be something like changing colors on a profile page. Or it might be something more localized. For example, you can choose the color of a note in the Google Keep application.</p>











<figure class="article__image break-out">
	<a href="https://play.google.com/store/apps/details?id=com.google.android.keep">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a0d1f2dd-b44b-45e5-ad01-29418cbe0fd7/google-keep-app.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a0d1f2dd-b44b-45e5-ad01-29418cbe0fd7/google-keep-app.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a0d1f2dd-b44b-45e5-ad01-29418cbe0fd7/google-keep-app.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a0d1f2dd-b44b-45e5-ad01-29418cbe0fd7/google-keep-app.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a0d1f2dd-b44b-45e5-ad01-29418cbe0fd7/google-keep-app.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a0d1f2dd-b44b-45e5-ad01-29418cbe0fd7/google-keep-app.png"
			sizes="100vw"
			alt="Google Keep App"
		/>
	</a>

	
</figure>


<p>Theming usually involves compiling a separate stylesheet to override a default value with user preferences, or compiling a different stylesheet for each user. Both of these can be difficult and have an impact on performance.</p>

<p>With custom properties, we don&rsquo;t need to compile a different stylesheet; we only need to update the value of properties according to the user&rsquo;s preferences. Since they are inherited values, if we do this on the root element they can be used anywhere in our application.</p>

<h4 id="capitalize-global-dynamic-properties">Capitalize Global Dynamic Properties</h4>

<p>Custom properties are case sensitive and since most custom properties will be local, if you are using global dynamic properties, it can make sense to capitalize them.</p>

<pre class="break-out"><code class="language-css">:root {
  --THEME-COLOR: var(--user-theme-color, #d33a2c);            
}
</code></pre>

<p>Capitalization of variables often signifies global constants. For us, this is going to signify that the property is set elsewhere in the application and that we should probably not change it locally.</p>

<h4 id="avoid-directly-setting-global-dynamic-properties">Avoid Directly Setting Global Dynamic Properties</h4>

<p>Custom properties accept a fallback value. It can be a useful to avoid directly overwriting the value of a global custom properties and keep user values separate. We can use the fallback value to do this.</p>

<p>The example above sets the value of <code>--THEME-COLOR</code> to the value of <code>--user-theme-color</code> if it exists. If <code>--user-theme-color</code> is not set, the value of <code>#d33a2c</code> will be used. This way, we don’t need to provide a fallback every time we use <code>--THEME-COLOR</code>.</p>

<p>You might expect in the example below that the <code>background</code> will be set to green. However, the value of <code>--user-theme-color</code> has not been set on the root element, so the value of <code>--THEME-COLOR</code> has not changed.</p>

<pre class="break-out"><code class="language-css">:root {
  --THEME-COLOR: var(--user-theme-color, #d33a2c);            
}
body {
  --user-theme-color: green;
  background: var(--THEME-COLOR);
}
</code></pre>

<p>Indirectly setting global dynamic properties like this protects them from being overwritten locally and ensures user settings are always inherited from the root element. This is a useful convention to safeguard your theme values and avoid unintended inheritance.</p>

<p>If we do want to expose specific properties to inheritance, we can replace the <code>:root</code> selector with a <code>*</code> selector:</p>

<pre class="break-out"><code class="language-css">:root {
  --THEME-COLOR: var(--user-theme-color, #d33a2c);            
}
body {
  --user-theme-color: green;
  background: var(--THEME-COLOR);
}
</code></pre>

<p>Now the value of <code>--THEME-COLOR</code> is recalculated for every element and therefore the local value of <code>--user-theme-color</code> can be used. In other words, the background color in this example will be green.</p>

<p>You can see some more detailed examples of this pattern in the section on .</p>

<h4 id="updating-custom-properties-with-javascript">Updating Custom Properties With JavaScript</h4>

<p>If you want to set custom properties using JavaScript there is a fairly simple API and it looks like this:</p>

<pre><code class="language-javascript">const elm = document.documentElement;
elm.style.setProperty('--USER-THEME-COLOR', 'tomato');
</code></pre>

<p>Here I’m setting the value of <code>--USER-THEME-COLOR</code> on the document element, or in other words, the <code>:root</code> element where it will be inherited by all elements.</p>

<p>This is not a new API; it&rsquo;s the same JavaScript method for updating styles on an element. These are inline styles so they will have a higher specificity than regular CSS.</p>

<p>This means it&rsquo;s easy to apply local customizations:</p>

<pre><code class="language-css">.note {
  --note-color: #eaeaea;
}
.note {
  background: var(--note-color);
}
</code></pre>

<p>Here I set a default value for <code>--note-color</code> and scope this to the <code>.note</code> component. I keep the variable declaration separate from the property declaration, even in this simple example.</p>

<pre><code class="language-css">const elm = document.querySelector('#note-uid');
elm.style.setProperty('--note-color', 'yellow');
</code></pre>

<p>I then target a specific instance of a <code>.note</code> element and change the value of the <code>--note-color</code> custom property for that element only. This will now have higher specificity than the default value.</p>

<p>You can see how this works with this . These user preferences could be saved in local storage or in the case of a larger application perhaps in a database.</p>

<h4 id="manipulating-color-with-custom-properties">Manipulating Color With Custom Properties</h4>

<p>In addition to hex values and named colors, CSS has colors function such as <code>rgb()</code> and  <code>hsl()</code>. These allow us to specify individual components of a color such as the hue or lightness. Custom properties can be used in conjunction with color functions.</p>

<pre><code class="language-css">:root {
  --hue: 25;
}
body {
  background: hsl(var(--hue), 80%, 50%);
}
</code></pre>

<p>This is useful, but some of the most widely used features of preprocessors are advanced color functions that allow us to manipulate color using functions like lighten, darken or desaturate:</p>

<pre><code class="language-css">darken($base-color, 10%);
lighten($base-color, 10%);
desaturate($base-color, 20%);
</code></pre>

<p>It would be useful to have some of these features in browsers. , but until we have native color modification functions in CSS, custom properties could fill some of that gap.</p>

<p>We’ve seen that custom properties can be used inside existing color functions like <code>rgb()</code> and <code>hsl()</code> but they can also be used in <code>calc()</code>. This means that we can convert a real number to a percentage by multiplying it, e.g. <code>calc(50 * 1%)</code>  = <code>50%</code>.</p>

<pre><code class="language-css">:root {
  --lightness: 50;
}
body {
  background: hsl(25, 80%, calc(var(--lightness) * 1%));
}
</code></pre>

<p>The reason we want to store the lightness value as a real number is so that we can manipulate it with calc before converting it to a percentage. For example, if I want to darken a color by <code>20%</code>,  I can multiply its lightness by <code>0.8</code>. We can make this a little easier to read by separating the lightness calculation into a locally scoped custom property:</p>

<pre><code class="language-css">:root {
  --lightness: 50;
}
body {
  --lightness: calc(var(--lightness * 0.8));
  background: hsl(25, 80%, calc(var(--lightness) * 1%));
}
</code></pre>

<p>We <em>could</em> even abstract away more of the calculations and create something like . This example is likely too complex for most practical cases of theming, but it demonstrates the full power of dynamic custom properties.</p>

<h4 id="simplify-theming">Simplify Theming</h4>

<p>One of the advantages of using custom properties is the ability to simplify theming. The application doesn’t need to be aware of how custom properties are used. Instead, we use JavaScript or server-side code to set the value of custom properties. How these values are used is determined by the stylesheets.</p>

<p>This means once again that we are able to separate logic from design. If you have a technical design team, authors can update stylesheets and decide how to apply custom properties without changing a single line of JavaScript or backend code.</p>

<p>Custom properties also allow as to move some of the complexity of theming into the CSS and this complexity can have a negative impact on the maintainability of your CSS, so remember to keep it simple wherever possible.</p>




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




<h3 id="using-custom-properties-today">Using Custom Properties Today</h3>

<p>Even if you&rsquo;re supporting IE10 and 11, you can start using custom properties today. Most of the examples in this article have to do with how we write and structure CSS. The benefits are significant in terms of maintainability, however, most of the examples only reduce what could otherwise be done with more complex code.</p>

<p>I use a tool called  to convert most of the features of custom properties into a static representation of the same code. Other similar tools ignore custom properties inside media queries or complex selectors treating custom properties much like preprocessor variables.</p>

<p>What these tools cannot do is emulate the runtime features of custom properties. This means no dynamic features like theming or changing properties with JavaScript. This might be OK in many situations. Depending on the situation, UI customization might be considered a progressive enhancement and the default theme could be perfectly acceptable for older browsers.</p>

<h4 id="loading-the-correct-stylesheet">Loading The Correct Stylesheet</h4>

<p>There are many ways you can use postCSS. I use a  process to compile separate stylesheets for newer and older browsers. A simplified version of my <code>gulp</code> task looks like this:</p>

<pre><code class="language-javascript">import gulp from "gulp";
import sass from "gulp-sass";
import postcss from "gulp-postcss";
import rename from "gulp-rename";
import cssvariables from "postcss-css-variables";
import autoprefixer from "autoprefixer";
import cssnano from "cssnano";

gulp.task("css-no-vars", () =>
  gulp
    .src("./src/css/*.scss")
    .pipe(sass().on("error", sass.logError))
    .pipe(postcss([cssvariables(), cssnano()]))
    .pipe(rename({ extname: ".no-vars.css" }))
    .pipe(gulp.dest("./dist/css"))
);

gulp.task("css", () =>
  gulp
    .src("./src/css/*.scss")
    .pipe(sass().on("error", sass.logError))
    .pipe(postcss([cssnano()]))
    .pipe(rename({ extname: ".css" }))
    .pipe(gulp.dest("./dist/css"))
);
</code></pre>

<p>This results in two CSS files: a regular one with custom properties (<code>styles.css</code>) and one for older browsers (<code>styles.no-vars.css</code>). I want IE10 and 11 to be served <code>styles.no-vars.css</code> and other browsers to get the regular CSS file.</p>

<p>Normally, I’d advocate using feature queries but  and we’ve used custom properties so extensively that serving a different stylesheet makes sense in this case.</p>

<p>Intelligently serving a different stylesheet and avoiding a flash of unstyled content is not a simple task. If you don’t need the dynamic features of custom properties, you could consider serving all browser <code>styles.no-vars.css</code> and using custom properties simply as a development tool.</p>

<p>If you want to take full advantage of all the dynamic features of custom properties, I suggest using a . Following these techniques, the main stylesheet is loaded asynchronously while the critical CSS is rendered inline. Your page header might look something like this:</p>

<pre><code class="language-html">&lt;head&gt;
  &lt;style&gt; /* inlined critical CSS */ &lt;/style&gt;
  &lt;script&gt; loadCSS('non-critical.css'); &lt;/script&gt;
&lt;/head&gt;
</code></pre>

<p>We can extend this to load either <code>styles.css</code> or <code>styles.no-vars.css</code> depending on whether the browser supports custom properties. We can detect support like this:</p>

<pre><code class="language-javascript">if ( window.CSS && CSS.supports('color', 'var(--test)') ) {
  loadCSS('styles.css');
} else {
  loadCSS('styles.no-vars.css');
}
</code></pre>

<h3 id="conclusion">Conclusion</h3>

<p>If you’ve been struggling to organize CSS efficiently, have difficulty with responsive components, want to implement client-side theming, or just want to start off on the right foot with custom properties, this guide should tell you everything you need to know.</p>

<p>It comes down to understanding the difference between dynamic and static variables in CSS as well as a few simple rules:</p>

<ol>
<li>Separate logic from design;</li>
<li>If a CSS property changes, consider using a custom property;</li>
<li>Change the value of custom properties, not which custom property is used;</li>
<li>Global variables are usually static.</li>
</ol>

<p>If you follow these conventions, you will find that working with custom properties is a whole lot easier than you think. This might even change how you approach CSS in general.</p>

<h4 id="further-reading">Further Reading</h4>

<ul>
<li>“,” Serg Hospodarets<br />
<em>A general introduction to the syntax and the features of custom properties.</em></li>
<li>“,” Harry Roberts<br />
<em>More useful information on theming.</em></li>
<li>, Mike Riethmuller on CodePen<br />
<em>A number of different examples you can experiment with.</em></li>
</ul>




<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(ra, yk, il)</span>
</div>


</div>




  <div id="sponsors-article-end" data-impression="true" class="c-promo-box c-promo-box--ad c-promo-box--wide sponsors hidden" data-audience="non-subscriber" data-remove="true"></div>



              </article>
            </body>
          </html>
---------------
<h1 id="#title_1" >2、文章： 使用政府开放数据和低代码方案构建应用</h1>
Marc Sewtz
[http://www.infoq.com/cn/articles/open-data-oracle-apex?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/open-data-oracle-apex?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/open-data-oracle-apex/zh/headerimage/GettyImages-836447336-1525205057427.jpg"/><p>市政府每天生成并发布大量的数据和信息。本文演示了如何使用Oracle Application Express（APEX），一种基于云计算的低代码开发工具，以及Socrata Open Data API（SODA），构建一个提供纽约市NYC 311服务请求公开数据报告和图表的Web应用。</p> <i>By Marc Sewtz</i> <i> Translated by 盖磊</i>
---------------
<h1 id="#title_2" >3、罗辑思维首席架构师：Go微服务改造实践</h1>
方圆
[http://www.infoq.com/cn/news/2018/05/luojisiwei?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/05/luojisiwei?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>得到最早的 APP 就是一个单体的 PHP 的应用，就是图中最大的黄色块，中间蓝色块代表不同模块。下面的黄色部分代表 passport 和支付系统，这个是在做得到之前就存在的系统，因为公司早期有微信里的电商业务。</p> <i>By 方圆</i>
---------------
<h1 id="#title_3" >4、技术团队如何化剑为犁完成市场迅速扩张</h1>
Jackson
[http://www.infoq.com/cn/news/2018/05/SHAREits?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/05/SHAREits?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p></p> <i>By Jackson</i>
---------------
<h1 id="#title_4" >5、VR已糊？Facebook不服！</h1>
覃云
[http://www.infoq.com/cn/news/2018/05/VR-Facebook?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/05/VR-Facebook?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>这几年，VR、AR、AI、比特币和区块链接连大火，身处互联网时代的我们，认知在不断地被刷新。而当某种技术既不再刷屏，也没有实现落地，我们基本就判定它flop了。</p> <i>By 覃云</i>
---------------
<h1 id="#title_5" >6、细思极恐：后门代码被隐藏在npm模块中，差点就得逞</h1>
覃云
[http://www.infoq.com/cn/news/2018/05/back-door-code-hidden-NPM?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/05/back-door-code-hidden-NPM?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>据 npm 博客报道，5 月 2 日，npm 安全小组收到了一份关于软件包伪装成 cookie 解析库并包含恶意后门程序（ backdoor）的报告，npm 官方在 2 个小时内迅速做出了响应。调查之后，他们决定撤掉 npm Registry 中的三个包和第四个包的三个版本。</p> <i>By 覃云</i>
---------------
<h1 id="#title_6" >7、得标准者得天下，中国已着手建立区块链国家标准</h1>
金缕春
[http://www.infoq.com/cn/news/2018/05/China-national-standard-block-ch?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/05/China-national-standard-block-ch?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>5月10日，据《经济参考报》报道，工信部电子工业标准化研究院区块链研究室主任李鸣表示，中国已着手建立区块链国家标准，以从顶层设计推动区块链标准体系建设，预计最快将于2019年底完成。</p> <i>By 金缕春</i>
---------------
<h1 id="#title_7" >8、Oracle正在推出其区块链产品</h1>
Nico Grant
[http://www.infoq.com/cn/news/2018/05/Oracle-launch-block-chain-produc?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/05/Oracle-launch-block-chain-produc?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>据彭博社报道，从本月开始，Oracle正着手推出其区块链软件产品。越来越多的企业正使用这种支撑比特币的数字账本技术，Oracle也将加入其中。</p> <i>By Nico Grant</i> <i> Translated by 盖磊</i>
---------------
<h1 id="#title_8" >9、极客时间首个订阅破万专栏诞生背后：快时代中的内容匠人</h1>
师海君
[http://www.infoq.com/cn/news/2018/05/content-craftsman-fast-age?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/05/content-craftsman-fast-age?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>这世上本就没有无缘无故的成功，当然也没有无缘无故的失败。</p> <i>By 师海君</i>
---------------