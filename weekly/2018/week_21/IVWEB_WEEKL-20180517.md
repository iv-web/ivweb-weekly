## 文章索引
1、 <a href="#1managing-svg-interaction-with-the-pointer-events-property" >Managing SVG Interaction With The Pointer Events Property</a><br/>
2、 <a href="#2文章-优秀架构师必须掌握的架构思维" >文章： 优秀架构师必须掌握的架构思维</a><br/>
3、 <a href="#3视频访谈-邓光耕架构演进是一门平衡的艺术" >视频访谈： 邓光耕：架构演进是一门平衡的艺术</a><br/>
4、 <a href="#4快讯阿里巴巴加入jcp执行委员会" >快讯：阿里巴巴加入JCP执行委员会</a><br/>
5、 <a href="#5docker企业版20更易于kubernetes集成" >Docker企业版2.0更易于Kubernetes集成</a><br/>
6、 <a href="#6net-core-3将支持windows桌面应用" >.NET Core 3将支持Windows桌面应用</a><br/>
7、 <a href="#7aws-appsync的ga版添加了新的graphql特性" >AWS AppSync的GA版添加了新的GraphQL特性</a><br/>
8、 <a href="#8从把事做对到做对的事" >从把事做对到做对的事</a><br/>
9、 <a href="#9现在所有主流浏览器都支持service-workers了" >现在所有主流浏览器都支持Service Workers了</a><br/><h1 id="#title_0" >1、Managing SVG Interaction With The Pointer Events Property</h1>
Tiffany Brown
[https://www.smashingmagazine.com/2018/05/svg-interaction-pointer-events-property/](https://www.smashingmagazine.com/2018/05/svg-interaction-pointer-events-property/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/05/svg-interaction-pointer-events-property/" />
              <title>Managing SVG Interaction With The Pointer Events Property</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>Managing SVG Interaction With The Pointer Events Property</h1>
                  
                    
                    <address>Tiffany Brown</address>
                  
                  <time datetime="2018-05-16T14:15:25&#43;02:00" class="op-published">2018-05-16T14:15:25+02:00</time>
                  <time datetime="2018-05-16T14:40:31&#43;00:00" class="op-modified">2018-05-16T14:40:31+00:00</time>
                </header>
                

<p>Try clicking or tapping the SVG image below. If you put your pointer in the right place (the shaded path) then you should have Smashing Magazine’s homepage open in a new browser tab. If you tried to click on some white space, you might be really confused instead.</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="XEeMKd"
   data-user="Yakudoo"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<p>This is the dilemma I faced during a recent project that included links within SVG images. Sometimes when I clicked the image, the link worked. Other times it didn&rsquo;t. Confusing, right?</p>

<p>I turned to the SVG  to learn more about what might be happening and whether SVG offers a fix. The answer: <code>pointer-events</code>.</p>



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


<p>Not to be confused with DOM (<strong>D</strong>ocument <strong>O</strong>bject <strong>M</strong>odel) , <code>pointer-events</code> is both a CSS property and an SVG element attribute. With it, we can manage which parts of an SVG document or element can receive events from a pointing device such as a mouse, trackpad, or finger.</p>

<p>A note about terminology: "pointer events" is also the name of a , web platform feature for user input. However, in this article &mdash; and for the purposes of the <code>pointer-events</code> property  &mdash; the phrase "pointer events" also includes mouse and touch events.</p>

<h3>Outside Of The Box: SVG’s "Shape Model"</h3>

<p>Using CSS with HTML imposes a  on HTML. In the box layout model, every element generates a rectangle around its contents. That rectangle may be inline, inline-level, atomic inline-level, or block, but it’s still a rectangle with four right angles and four edges. When we add a link or an event listener to an element, the interactive area matches the  dimensions of the rectangle.</p>

<p><strong>Note</strong>: <em>Adding a <code>clip-path</code> to an interactive element alters its interactive bounds. In other words, if you add a hexagonal <code>clip-path</code> path to an <code>a</code> element, only the points within the clipping path will be clickable. Similarly, adding a skew transformation will turn rectangles into rhomboids.</em></p>

<p>SVG does not have a box layout model. You see, when an SVG document is contained by an HTML document, within a CSS layout, the root SVG element adheres to the box layout model. Its child elements do not. As a result, most CSS layout-related properties don’t apply to SVG.</p>

<p>So instead, SVG has what I’ll call a ‘shape model’. When we add a link or an event listener to an SVG document or element, the interactive area will not necessarily be a rectangle. SVG elements <em>do</em> have a . The bounding box is defined as: <q>the tightest fitting rectangle aligned with the axes of that element’s user coordinate system that entirely encloses it and its descendants.</q> But initially, which parts of an SVG document are interactive depends on which parts are <em>visible</em> and/or <em>painted</em>.</p>

<h3 id="painted-vs-visible-elements">Painted vs. Visible Elements</h3>

<p>SVG elements can be “filled” but they can also be “stroked”. <em>Fill</em> refers to the interior of a shape. <em>Stroke</em> refers to its outline.</p>

<p>Together, “fill” and “stroke” are <em>painting operations</em> that render elements to the screen or page (also known as the <em>canvas</em>). When we talk about <em>painted elements</em>, we mean that the element has a fill and/or a stroke. Usually, this means the element is also visible.</p>

<p>However, an SVG element can be painted without being visible. This can happen if the <code>visible</code> attribute value or CSS property is <code>hidden</code> or when <code>display</code> is <code>none</code>. The element is there and occupies theoretical space. We just can’t see it (and assistive technology may not detect it).</p>

<p>Perhaps more confusingly, an element can also be visible &mdash; that is, have a computed <code>visibility</code> value of <code>visible</code> &mdash; without being painted. This happens when elements lack both a stroke and a fill.</p>

<p><strong>Note</strong>: <em>Color values with alpha transparency (e.g. <code>rgba(0,0,0,0)</code>) do not affect whether an element is painted or visible. In other words, if an element has an alpha transparent fill or stroke, it’s painted even if it can’t be seen.</em></p>

<p>Knowing when an element is painted, visible, or neither is crucial to understanding the impact of each <code>pointer-events</code> value.</p>


  <div id="sponsors-article" data-impression="true" class="c-promo-box c-promo-box--ad sponsors hidden" data-audience="non-subscriber" data-remove="true"></div>



<h3 id="all-or-none-or-something-in-between-the-values">All Or None Or Something In Between: The Values</h3>

<p><code>pointer-events</code> is both a CSS property and an SVG element attribute. Its initial value is <code>auto</code>, which means that only the painted and visible portions will receive pointer events. Most other values can be split into two groups:</p>

<ol>
<li>Values that require an element to be visible; and</li>
<li>Values that do not.</li>
</ol>

<p><code>painted</code>, <code>fill</code>, <code>stroke</code>, and <code>all</code> fall into the latter category. Their visibility-dependent counterparts &mdash; <code>visiblePainted</code>, <code>visibleFill</code>, <code>visibleStroke</code> and <code>visible</code> &mdash; fall into the former.</p>

<p>The  also defines a <code>bounding-box</code> value. When the value of <code>pointer-events</code> is <code>bounding-box</code>, the rectangular area around the element can also receive pointer events. As of this writing, only Chrome 65+ supports the <code>bounding-box</code> value.</p>

<p><code>none</code> is also a valid value. It prevents the element and its children from receiving any pointer events. The <code>pointer-events</code> CSS property can be used with HTML elements too. But when used with HTML, only <code>auto</code> and <code>none</code> are valid values.</p>

<p>Since <code>pointer-events</code> values are better demonstrated than explained, let’s look at some demos.</p>

<p>Here we have a circle with a fill and a stroke applied. It’s both <em>painted</em> and <em>visible</em>. The entire circle can receive pointer events, but the area outside of the circle cannot.</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="xWXqrd"
   data-user="webinista"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<p>Disable the fill, so that its value is <code>none</code>. Now if you try to hover, click, or tap the interior of the circle, nothing happens. But if you do the same for the stroke area, pointer events are still dispatched. Changing the <code>fill</code> value to <code>none</code> means that this area <em>visible</em>, but not <em>painted</em>.</p>

<p>Let’s make a small change to our markup. We&rsquo;ll add <code>pointer-events=&quot;visible&quot;</code> to our <code>circle</code> element, while keeping <code>fill=none</code>.</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="dmVWoQ"
   data-user="webinista"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<p>Now the unpainted area encircled by the stroke can receive pointer events.</p>

<h3 id="augmenting-the-clickable-area-of-an-svg-image">Augmenting The Clickable Area Of An SVG Image</h3>

<p>Let’s return to the image from the beginning of this article. Our &ldquo;amethyst&rdquo;  is a <code>path</code> element, as opposed to a group of polygons each with a <code>stroke</code> and <code>fill</code>. That means we can’t just add <code>pointer-events=&quot;all&quot;</code> and call it a day.</p>

<p>Instead, we need to augment the click area. Let’s use what we know about painted and visible elements. In the example below, I’ve added a rectangle to our image markup.</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="BrwWQv"
   data-user="webinista"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<p>Even though this rectangle is unseen, it’s still <em>technically</em> visible (i.e. <code>visibility: visible</code>).  Its lack of a fill, however, means that it is not <em>painted</em>. Our image looks the same. Indeed it still works the same &mdash; clicking white space still doesn’t trigger a navigation operation. We still need to add a <code>pointer-events</code> attribute to our <code>a</code> element. Using the <code>visible</code> or <code>all</code> values will work here.</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="RMLpGy"
   data-user="webinista"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<p>Now the entire image can receive pointer events.</p>

<p>Using <code>bounding-box</code> would eliminate the need for a phantom element. All points within the bounding box would receive pointer events, including the white space enclosed by the path. But again: <code>pointer-events=&quot;bounding-box&quot;</code> isn’t widely supported. Until it is, we can use unpainted elements.</p>

<h3 id="using-pointer-events-when-mixing-svg-and-html">Using <code>pointer-events</code> When Mixing SVG And HTML</h3>

<p>Another case where <code>pointer-events</code> may be helpful: using SVG inside of an HTML button.</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="Ovxmmy"
   data-user="webinista"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<p>In most browsers &mdash; Firefox and Internet Explorer 11 are exceptions here &mdash; the value of <code>event.target</code> will be an SVG element instead of our HTML button. Let’s add <code>pointer-events=&quot;none&quot;</code> to our opening SVG tag.</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="KoXmqm"
   data-user="webinista"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<p>Now when users click or tap our button, the <code>event.target</code>  will refer to our <code>button</code>.</p>

<p>Those well-versed in the DOM and JavaScript will note that using the <code>function</code> keyword instead of an arrow function and <code>this</code> instead of <code>event.target</code> fixes this problem. Using <code>pointer-events=&quot;none&quot;</code> (or <code>pointer-events: none;</code> in your CSS), however, means that you don’t have to commit that particular JavaScript quirk to memory.</p>

<h3 id="conclusion">Conclusion</h3>

<p>SVG supports the same kind of interactivity we&rsquo;re used to with HTML. We can use it to create charts that respond to clicks or taps. We can create linked areas that don’t adhere to the CSS and HTML box model. And with the addition of <code>pointer-events</code>, we can improve the way our SVG documents behave in response to user interaction.</p>

<p>Browser support for SVG <code>pointer-events</code> is robust. Every browser that supports SVG supports the property for SVG documents and elements. When used with , support is slightly less robust.  It isn’t available in Internet Explorer 10 or its predecessors, or any version of Opera Mini.</p>

<p>We’ve just scratched the surface of <code>pointer-events</code> in this piece. For a more in-depth,  technical treatment, read through the , complete with examples.</p>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(rb, ra, yk, il)</span>
</div>


</div>




  <div id="sponsors-article-end" data-impression="true" class="c-promo-box c-promo-box--ad c-promo-box--wide sponsors hidden" data-audience="non-subscriber" data-remove="true"></div>



              </article>
            </body>
          </html>
---------------
<h1 id="#title_1" >2、文章： 优秀架构师必须掌握的架构思维</h1>
杨波
[http://www.infoq.com/cn/articles/architecture-thought?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/architecture-thought?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/architecture-thought/zh/smallimage/GettyImages-671039130-1512649078720-1526460276922.jpg"/><p>最近团队来了一些新人，有些有一定工作经验，是以高级工程师/架构师身份进来的，但我发现他们大部分人思维偏应用和细节，抽象能力弱。所以作为团队技术培训的一部分，我整理了这篇文章，希望对他们树立正确的架构设计思维有帮助。我认为，对思维习惯和思考能力的培养，其重要性远远大于对实际技术工具的掌握。</p> <i>By 杨波</i>
---------------
<h1 id="#title_2" >3、视频访谈： 邓光耕：架构演进是一门平衡的艺术</h1>
邓光耕
[http://www.infoq.com/cn/interviews/interview-with-dengguangeng-talk-architecture-evolution?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/interviews/interview-with-dengguangeng-talk-architecture-evolution?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/interviews/interview-with-dengguangeng-talk-architecture-evolution/zh/mediumimage/dengguangdeng270-1526498490645.jpg"/><p>我们在QCon 全球软件开发大会，2018北京站的现场，很荣幸地采访到了来自付钱拉的高级技术经理邓光耕先生，请他来谈谈有关付钱拉架构演进的发展情况与技术难点。</p> <i>By 邓光耕</i>
---------------
<h1 id="#title_3" >4、快讯：阿里巴巴加入JCP执行委员会</h1>
徐川
[http://www.infoq.com/cn/news/2018/05/alibaba-elected-JCP-EC?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/05/alibaba-elected-JCP-EC?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>今日，InfoQ获得消息，阿里巴巴通过了JCP-EC的投票，入选成为执行委员会的一员，该席位将于5月24日生效。</p> <i>By 徐川</i>
---------------
<h1 id="#title_4" >5、Docker企业版2.0更易于Kubernetes集成</h1>
Sergio De Simone
[http://www.infoq.com/cn/news/2018/05/docker-ee-2.0-kubernetes?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/05/docker-ee-2.0-kubernetes?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>最新版的Docker企业版（Docker Enterprise Edition，Docker EE）可以管理和保护运行在异构环境中运行在Kubernetes之上的应用程序，并且提供简化Kubernetes环境日常管理的工作流。</p> <i>By Sergio De Simone</i> <i> Translated by 金灵杰</i>
---------------
<h1 id="#title_5" >6、.NET Core 3将支持Windows桌面应用</h1>
Jeff Martin
[http://www.infoq.com/cn/news/2018/05/net-core3-announced?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/05/net-core3-announced?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>微软在Build开发者大会上宣布，.NET Core 3将包含对Windows桌面应用的支持。这意味着开发人员可以在.NET Core中使用WinForms、WPF或UWP编写Windows平台应用了。</p> <i>By Jeff Martin</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_6" >7、AWS AppSync的GA版添加了新的GraphQL特性</h1>
Steef-Jan Wiggers
[http://www.infoq.com/cn/news/2018/05/aws-appsync-graphql?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/05/aws-appsync-graphql?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>2018年4月，Amazon发布了AWS AppSync的一般可用版（GA）。AWS AppSync是一种提供实时数据处理和离线编程能力的GraphQL服务，是Amazon先前于去年的AWS re:Inventd大会上推出的。当前发布的GA版中，提供了多种可加速开发的新特性，其中包括一种测试和调试流程、与Amazon CloudWatch的集成，以及对Amazon CloudFormation的支持。</p> <i>By Steef-Jan Wiggers</i> <i> Translated by 盖磊</i>
---------------
<h1 id="#title_7" >8、从把事做对到做对的事</h1>
Rui Miguel Ferreira
[http://www.infoq.com/cn/news/2018/05/doing-the-right-things-right?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/05/doing-the-right-things-right?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>ING Netherlands首席信息官Peter Jacobs在Agile 2018印度大会上作了一场演讲。他在演讲中说明了如何提倡并践行敏捷方法，帮助组织把事做对，以便应对他们目前面临的挑战，保证他们真正做对的事。</p> <i>By Rui Miguel Ferreira</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_8" >9、现在所有主流浏览器都支持Service Workers了</h1>
Kevin Ball
[http://www.infoq.com/cn/news/2018/05/service-workers-supported-across?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/05/service-workers-supported-across?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>随着4月30日Windows 10 2018年4月10日更新补丁的发布，以及3月29日Safari 11.1版本的发布，Edge和Safari以及Firefox和Chrome都默认支持Service Workers了。开发人员现在可以开发提供离线功能的渐进式Web应用（Progressive Web Apps），并期望它们在除Internet Explorer和Opera Mini之外的所有浏览器上运行。</p> <i>By Kevin Ball</i> <i> Translated by 冬雨</i>
---------------