## 文章索引
1、 <a href="#1继爆款超级账本后ibm再次推出新产品" >继爆款超级账本后，IBM再次推出新产品</a><br/>
2、 <a href="#2everything-you-need-to-know-about-alignment-in-flexbox" >Everything You Need To Know About Alignment In Flexbox</a><br/>
3、 <a href="#3文章-使用契约测试提高分布式系统的质量" >文章： 使用契约测试提高分布式系统的质量</a><br/>
4、 <a href="#4文章-人工智能与区块链初探交集与前瞻" >文章： 人工智能与区块链初探：交集与前瞻</a><br/>
5、 <a href="#5文章-实时音频混音技术在视频直播场景中的实践" >文章： 实时音频混音技术在视频直播场景中的实践</a><br/>
6、 <a href="#6文章-苏宁金融app全链路灰度实践" >文章： 苏宁金融App全链路灰度实践</a><br/>
7、 <a href="#7聪明的头脑+有趣的灵魂揭秘腾讯云最暖智能酒店解决方案" >聪明的头脑+有趣的灵魂，揭秘腾讯云最暖智能酒店解决方案</a><br/>
8、 <a href="#8fex-技术周刊---2018/08/13" >FEX 技术周刊 - 2018/08/13</a><br/>
9、 <a href="#9git实用技巧和命令" >Git实用技巧和命令</a><br/>
10、 <a href="#10microsoft-quantum-katas帮助开发人员探索使用q#实现量子计算" >Microsoft Quantum Katas帮助开发人员探索使用Q#实现量子计算</a><br/>
11、 <a href="#11ebay通过事件溯源实现持续交付" >eBay通过事件溯源实现持续交付</a><br/>
12、 <a href="#12微软把uwp定位成业务线应用程序开发平台" >微软把UWP定位成业务线应用程序开发平台</a><br/>
13、 <a href="#13我是如何用2个unix命令给sql提速的" >我是如何用2个Unix命令给SQL提速的</a><br/>
14、 <a href="#14汇聚40+机器学习最佳落地案例第二届aicon来了" >汇聚40+机器学习最佳落地案例，第二届AICon来了！</a><br/><h1 id="#title_0" >1、继爆款超级账本后，IBM再次推出新产品</h1>
Ian Allison
[http://www.infoq.com/cn/news/2018/08/ibm-blockchain-LedgerConnect?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/08/ibm-blockchain-LedgerConnect?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>IBM推出了用于金融服务区块链平台LedgerConnect，继续扩大其区块链技术产品生态。</p> <i>By Ian Allison</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_1" >2、Everything You Need To Know About Alignment In Flexbox</h1>
Rachel Andrew
[https://www.smashingmagazine.com/2018/08/flexbox-alignment/](https://www.smashingmagazine.com/2018/08/flexbox-alignment/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/08/flexbox-alignment/" />
              <title>Everything You Need To Know About Alignment In Flexbox</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>Everything You Need To Know About Alignment In Flexbox</h1>
                  
                    
                    <address>Rachel Andrew</address>
                  
                  <time datetime="2018-08-13T14:00:57&#43;02:00" class="op-published">2018-08-13T14:00:57+02:00</time>
                  <time datetime="2018-08-13T14:00:50&#43;00:00" class="op-modified">2018-08-13T14:00:50+00:00</time>
                </header>
                

<p>, I explained what happens when you declare <code>display: flex</code> on an element. This time we will take a look at the alignment properties, and how these work with Flexbox. If you have ever been confused about when to align and when to justify, I hope this article will make things clearer!</p>

<h3 id="history-of-flexbox-alignment">History Of Flexbox Alignment</h3>

<p>For the entire history of CSS Layout, being able to properly align things on both axes seemed like it might truly be the hardest problem in web design. So the ability to properly align items and groups of items was for many of us the most exciting thing about Flexbox when it first started to show up in browsers. Alignment became as simple as two lines of CSS:</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="WKLYEX"
   data-user="rachelandrew"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<p>The alignment properties that you might think of as the flexbox alignment properties are now fully defined in the . This specification details how alignment works across the various layout contexts. This means that we can use the same alignment properties in CSS Grid as we use in Flexbox &mdash; and in future in other layout contexts, too. Therefore, any new alignment capability for flexbox will be detailed in the Box Alignment specification and not in a future level of Flexbox.</p>



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




<h3 id="the-properties">The Properties</h3>

<p>Many people tell me that they struggle to remember whether to use properties which start with <code>align-</code> or those which start with <code>justify-</code> in flexbox. The thing to remember is that:</p>

<ul>
<li><code>justify-</code> performs main axis alignment. Alignment in the same direction as your <code>flex-direction</code></li>
<li><code>align-</code> performs cross-axis alignment. Alignment across the direction defined by <code>flex-direction</code>.</li>
</ul>

<p>Thinking in terms of main axis and cross axis, rather than horizontal and vertical really helps here. It doesn’t matter which way the axis is physically.</p>

<h4 id="main-axis-alignment-with-justify-content">Main Axis Alignment With <code>justify-content</code></h4>

<p>We will start with the main axis alignment. On the main axis, we align using the <code>justify-content</code> property. This property deals with all of our flex items as a group, and controls how space is distributed between them.</p>

<p>The initial value of <code>justify-content</code> is <code>flex-start</code>. This is why, when you declare <code>display: flex</code> all your flex items line up against the start of the flex line. If you have a <code>flex-direction</code> of <code>row</code> and are in a left to right language such as English, then the items will start on the left.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/67648629-b445-429f-9fd4-0fb47b7875ef/justify-content-flex-start.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/67648629-b445-429f-9fd4-0fb47b7875ef/justify-content-flex-start.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/67648629-b445-429f-9fd4-0fb47b7875ef/justify-content-flex-start.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/67648629-b445-429f-9fd4-0fb47b7875ef/justify-content-flex-start.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/67648629-b445-429f-9fd4-0fb47b7875ef/justify-content-flex-start.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/67648629-b445-429f-9fd4-0fb47b7875ef/justify-content-flex-start.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/67648629-b445-429f-9fd4-0fb47b7875ef/justify-content-flex-start.png"
			sizes="100vw"
			alt="The items are all lined up in a row starting on the left"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The items line up to the start ()
		</figcaption>
	
</figure>


<p>Note that the <code>justify-content</code> property can only do something <strong>if there is spare space to distribute</strong>. Therefore if you have a set of flex items which take up all of the space on the main axis, using <code>justify-content</code> will not change anything.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/064418da-c45c-4fbf-9b4e-65c481c05c00/justify-content-no-space.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/064418da-c45c-4fbf-9b4e-65c481c05c00/justify-content-no-space.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/064418da-c45c-4fbf-9b4e-65c481c05c00/justify-content-no-space.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/064418da-c45c-4fbf-9b4e-65c481c05c00/justify-content-no-space.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/064418da-c45c-4fbf-9b4e-65c481c05c00/justify-content-no-space.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/064418da-c45c-4fbf-9b4e-65c481c05c00/justify-content-no-space.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/064418da-c45c-4fbf-9b4e-65c481c05c00/justify-content-no-space.png"
			sizes="100vw"
			alt="The container is filled with the items"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			There is no space to distribute ()
		</figcaption>
	
</figure>


<p>If we give <code>justify-content</code> a value of <code>flex-end</code> then all of the items will move to the end of the line. The spare space is now placed at the beginning.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/262c2132-a9bf-4c6c-90cd-4ec445c9f3e1/justify-content-flex-end.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/262c2132-a9bf-4c6c-90cd-4ec445c9f3e1/justify-content-flex-end.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/262c2132-a9bf-4c6c-90cd-4ec445c9f3e1/justify-content-flex-end.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/262c2132-a9bf-4c6c-90cd-4ec445c9f3e1/justify-content-flex-end.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/262c2132-a9bf-4c6c-90cd-4ec445c9f3e1/justify-content-flex-end.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/262c2132-a9bf-4c6c-90cd-4ec445c9f3e1/justify-content-flex-end.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/262c2132-a9bf-4c6c-90cd-4ec445c9f3e1/justify-content-flex-end.png"
			sizes="100vw"
			alt="The items are displayed in a row starting at the end of the container — on the right"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The items line up at the end ()
		</figcaption>
	
</figure>


<p>We can do other things with that space. We could ask for it to be distributed <em>between</em> our flex items, by using <code>justify-content: space-between</code>. In this case, the first and last item will be flush with the ends of the container and all of the space shared equally between the items.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e0df6bac-5250-47d2-82ed-da66306e7c95/justify-content-space-between.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e0df6bac-5250-47d2-82ed-da66306e7c95/justify-content-space-between.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e0df6bac-5250-47d2-82ed-da66306e7c95/justify-content-space-between.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e0df6bac-5250-47d2-82ed-da66306e7c95/justify-content-space-between.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e0df6bac-5250-47d2-82ed-da66306e7c95/justify-content-space-between.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e0df6bac-5250-47d2-82ed-da66306e7c95/justify-content-space-between.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e0df6bac-5250-47d2-82ed-da66306e7c95/justify-content-space-between.png"
			sizes="100vw"
			alt="Items lined up left and right with equal space between them"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The spare space is shared out between the items ()
		</figcaption>
	
</figure>


<p>We can ask that the space to be distributed around our flex items, using <code>justify-content: space-around</code>. In this case, the available space is shared out and placed on each side of the item.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/acab1663-6d66-4d98-9d1c-2f2b98911bbe/justify-content-space-around.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/acab1663-6d66-4d98-9d1c-2f2b98911bbe/justify-content-space-around.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/acab1663-6d66-4d98-9d1c-2f2b98911bbe/justify-content-space-around.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/acab1663-6d66-4d98-9d1c-2f2b98911bbe/justify-content-space-around.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/acab1663-6d66-4d98-9d1c-2f2b98911bbe/justify-content-space-around.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/acab1663-6d66-4d98-9d1c-2f2b98911bbe/justify-content-space-around.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/acab1663-6d66-4d98-9d1c-2f2b98911bbe/justify-content-space-around.png"
			sizes="100vw"
			alt="Items spaced out with even amounts of space on each side"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The items have space either side of them ()
		</figcaption>
	
</figure>


<p>A newer value of <code>justify-content</code> can be found in the Box Alignment specification; it doesn’t appear in the Flexbox spec. This value is <code>space-evenly</code>. In this case, the items will be evenly distributed in the container, and the extra space will be shared out between and either side of the items.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b8960c00-dd71-4147-bd7a-7a32bc98f08a/justify-content-space-evenly.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b8960c00-dd71-4147-bd7a-7a32bc98f08a/justify-content-space-evenly.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b8960c00-dd71-4147-bd7a-7a32bc98f08a/justify-content-space-evenly.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b8960c00-dd71-4147-bd7a-7a32bc98f08a/justify-content-space-evenly.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b8960c00-dd71-4147-bd7a-7a32bc98f08a/justify-content-space-evenly.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b8960c00-dd71-4147-bd7a-7a32bc98f08a/justify-content-space-evenly.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b8960c00-dd71-4147-bd7a-7a32bc98f08a/justify-content-space-evenly.png"
			sizes="100vw"
			alt="Items with equal amounts of space between and on each end"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The items are spaced evenly ()
		</figcaption>
	
</figure>


<p>You can play with all of the values in the demo:</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="Owraaj"
   data-user="rachelandrew"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<p>These values work in the same way if your <code>flex-direction</code> is <code>column</code>. You may not have extra space to distribute in a column however unless you add a height or block-size to the flex container as in this next demo.</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="zLyMyV"
   data-user="rachelandrew"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<h4 id="cross-axis-alignment-with-align-content">Cross Axis Alignment with <code>align-content</code></h4>

<p>If you have added <code>flex-wrap: wrap</code> to your flex container, and have multiple flex lines then you can use <code>align-content</code> to align your flex lines on the cross axis. However, this will require that you have additional space on the cross axis. In the below demo, my cross axis is running in the block direction as a column, and I have set the height of the flex container to <code>60vh</code>. As this is more than is needed to display my flex items I have spare space vertically in the container.</p>

<p>I can then use <code>align-content</code> with any of the values:</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="pZqqMJ"
   data-user="rachelandrew"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<p>If my <code>flex-direction</code> were <code>column</code> then <code>align-content</code> would work as in the following example.</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="MBZZNy"
   data-user="rachelandrew"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<p>As with <code>justify-content</code>, we are working with the lines as a group and distributing the spare space.</p>

<div class="sponsors__wide-place"></div>




<h3 id="the-place-content-shorthand">The <code>place-content</code> Shorthand</h3>

<p>In the Box Alignment, we find the shorthand <code>place-content</code>; using this property means you can set <code>justify-content</code> and <code>align-content</code> at once. The first value is for <code>align-content</code>, the second for <code>justify-content</code>. If you only set one value then both values are set to that value, therefore:</p>

<pre><code class="language-css">.container {
    place-content: space-between stretch;
}</code></pre>

<p>Is the same as:</p>

<pre><code class="language-css">.container {
    align-content: space-between; 
    justify-content: stretch;
}</code></pre>

<p>If we used:</p>

<pre><code class="language-css">.container {
    place-content: space-between;
}</code></pre>

<p>This would be the same as:</p>

<pre><code class="language-css">.container {
    align-content: space-between; 
    justify-content: space-between;
}</code></pre>

<h4 id="cross-axis-alignment-with-align-items">Cross Axis Alignment With <code>align-items</code></h4>

<p>We now know that we can align our set of flex items or our flex lines as a group. However, there is another way we might wish to align our items and that is to align items in relationship to each other on the cross axis. Your flex container has a height. That height might be defined by the height of the tallest item as in this image.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dabd13bf-bf9c-411f-86c0-d43cdfb935fe/container-height-of-item.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dabd13bf-bf9c-411f-86c0-d43cdfb935fe/container-height-of-item.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dabd13bf-bf9c-411f-86c0-d43cdfb935fe/container-height-of-item.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dabd13bf-bf9c-411f-86c0-d43cdfb935fe/container-height-of-item.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dabd13bf-bf9c-411f-86c0-d43cdfb935fe/container-height-of-item.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dabd13bf-bf9c-411f-86c0-d43cdfb935fe/container-height-of-item.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dabd13bf-bf9c-411f-86c0-d43cdfb935fe/container-height-of-item.png"
			sizes="100vw"
			alt="The container height is tall enough to contain the items, the third item has more content"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The container height is defined by the third item ()
		</figcaption>
	
</figure>


<p>It might instead be defined by adding a height to the flex container:</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c477a442-ea29-48cf-bed9-94b75593a1b2/container-added-height.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c477a442-ea29-48cf-bed9-94b75593a1b2/container-added-height.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c477a442-ea29-48cf-bed9-94b75593a1b2/container-added-height.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c477a442-ea29-48cf-bed9-94b75593a1b2/container-added-height.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c477a442-ea29-48cf-bed9-94b75593a1b2/container-added-height.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c477a442-ea29-48cf-bed9-94b75593a1b2/container-added-height.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c477a442-ea29-48cf-bed9-94b75593a1b2/container-added-height.png"
			sizes="100vw"
			alt="The container height is taller than needed to display the items"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			THe height is defined by a size on the flex container ()
		</figcaption>
	
</figure>


<p>The reason that flex items appear to stretch to the size of the tallest item is that the initial value of <code>align-items</code> is <code>stretch</code>. The items stretch on the cross access to become the size of the flex container in that direction.</p>

<p>Note that where <code>align-items</code> is concerned, if you have a multi-line flex container, each line acts like a new flex container. The tallest item in that line would define the size of all items in that line.</p>

<p>In addition to the initial value of stretch, you can give <code>align-items</code> a value of <code>flex-start</code>, in which case they align to the start of the container and no longer stretch to the height.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7da24e8b-8d18-4ada-9f0e-e417e0293607/align-items-flex-start.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7da24e8b-8d18-4ada-9f0e-e417e0293607/align-items-flex-start.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7da24e8b-8d18-4ada-9f0e-e417e0293607/align-items-flex-start.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7da24e8b-8d18-4ada-9f0e-e417e0293607/align-items-flex-start.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7da24e8b-8d18-4ada-9f0e-e417e0293607/align-items-flex-start.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7da24e8b-8d18-4ada-9f0e-e417e0293607/align-items-flex-start.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7da24e8b-8d18-4ada-9f0e-e417e0293607/align-items-flex-start.png"
			sizes="100vw"
			alt="The items are aligned to the start"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The items aligned to the start of the cross axis ()
		</figcaption>
	
</figure>


<p>The value <code>flex-end</code> moves them to the end of the container on the cross axis.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/52d4c377-8c60-4336-be64-f01cb9a20833/align-items-flex-end.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/52d4c377-8c60-4336-be64-f01cb9a20833/align-items-flex-end.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/52d4c377-8c60-4336-be64-f01cb9a20833/align-items-flex-end.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/52d4c377-8c60-4336-be64-f01cb9a20833/align-items-flex-end.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/52d4c377-8c60-4336-be64-f01cb9a20833/align-items-flex-end.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/52d4c377-8c60-4336-be64-f01cb9a20833/align-items-flex-end.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/52d4c377-8c60-4336-be64-f01cb9a20833/align-items-flex-end.png"
			sizes="100vw"
			alt="Items aligned to the end of the cross axis"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The items aligned to the end of the cross axis ()
		</figcaption>
	
</figure>


<p>If you use a value of <code>center</code> the items all centre against each other:</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8ccb2aba-b692-4ba5-8827-1043674fc1d4/align-items-center.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8ccb2aba-b692-4ba5-8827-1043674fc1d4/align-items-center.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8ccb2aba-b692-4ba5-8827-1043674fc1d4/align-items-center.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8ccb2aba-b692-4ba5-8827-1043674fc1d4/align-items-center.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8ccb2aba-b692-4ba5-8827-1043674fc1d4/align-items-center.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8ccb2aba-b692-4ba5-8827-1043674fc1d4/align-items-center.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8ccb2aba-b692-4ba5-8827-1043674fc1d4/align-items-center.png"
			sizes="100vw"
			alt="The items are centered"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Centering the items on the cross axis ()
		</figcaption>
	
</figure>


<p>We can also do baseline alignment. This ensures that the baselines of text line up, as opposed to aligning the boxes around the content.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6607e8bc-9f6b-43a6-9b13-24bff76068f1/align-items-baseline.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6607e8bc-9f6b-43a6-9b13-24bff76068f1/align-items-baseline.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6607e8bc-9f6b-43a6-9b13-24bff76068f1/align-items-baseline.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6607e8bc-9f6b-43a6-9b13-24bff76068f1/align-items-baseline.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6607e8bc-9f6b-43a6-9b13-24bff76068f1/align-items-baseline.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6607e8bc-9f6b-43a6-9b13-24bff76068f1/align-items-baseline.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6607e8bc-9f6b-43a6-9b13-24bff76068f1/align-items-baseline.png"
			sizes="100vw"
			alt="The items are aligned so their baselines match"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Aligning the baselines ()
		</figcaption>
	
</figure>


<p>You can try these values out in the demo:</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="WKLBpv"
   data-user="rachelandrew"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<h4 id="individual-alignment-with-align-self">Individual Alignment With <code>align-self</code></h4>

<p>The <code>align-items</code> property means that you can set the alignment of all of the items at once. What this really does is set all of the <code>align-self</code> values on the individual flex items as a group. You can also use the <code>align-self</code> property on any individual flex item to align it inside the flex line and against the other flex items.</p>

<p>In the following example, I have used <code>align-items</code> on the container to set the alignment for the group to <code>center</code>, but also used <code>align-self</code> on the first and last items to change their alignment value.</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="KBbLmz"
   data-user="rachelandrew"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<h3 id="why-is-there-no-justify-self">Why Is There No <code>justify-self</code>?</h3>

<p>A common question is why it is not possible to align one item or a group of the items on the main axis. Why is there no <code>-self</code> property for main axis alignment in Flexbox? If you think about <code>justify-content</code> and <code>align-content</code> as being about space distribution, the reason for their being no self-alignment becomes more obvious. We are dealing with the flex items as a group, and distributing available space in some way &mdash; either at the start or end of the group or between the items.</p>

<p>If might be also helpful to think about how <code>justify-content</code> and <code>align-content</code> work in CSS Grid Layout. In Grid, these properties are used to distribute spare space in the grid container <em>between grid tracks</em>. Once again, we take the tracks as a group, and these properties give us a way to distribute any extra space between them. As we are acting on a group in both Grid and Flexbox, we can’t target an item on its own and do something different with it. However, there is a way to achieve the kind of layout that you are asking for when you ask for a <code>self</code> property on the main axis, and that is to use auto margins.</p>

<div class="sponsors__wide-place"></div>




<h4 id="using-auto-margins-on-the-main-axis">Using Auto Margins On The Main Axis</h4>

<p>If you have ever centered a block in CSS (such as the wrapper for your main page content by setting a margin left and right of <code>auto</code>), then you already have some experience of how auto margins behave. A margin set to auto will try to become as big as it can in the direction it has been set in. In the case of using margins to center a block, we set the left and right both to auto; they each try and take up as much space as possible and so push our block into the center.</p>

<p>Auto margins work very nicely in Flexbox to align single items or groups of items on the main axis. In the next example, I am achieving a common design pattern. I have a navigation bar using Flexbox, the items are displayed as a row and are using the initial value of <code>justify-content: start</code>. I would like the final item to be displayed separated from the others at the end of the flex line &mdash; assuming there is enough space on the line to do so.</p>

<p>I target that item and give it a margin-left of auto. This then means that the margin tries to get as much space as possible to the left of the item, which means the item gets pushed all the way over to the right.</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="oMJROm"
   data-user="rachelandrew"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<p>If you use auto margins on the main axis then <code>justify-content</code> will cease to have any effect, as the auto margins will have taken up all of the space that would otherwise be assigned using <code>justify-content</code>.</p>

<h3 id="fallback-alignment">Fallback Alignment</h3>

<p>Each alignment method details a fallback alignment, this is what will happen if the alignment you have requested can’t be achieved. For example, if you only have one item in a flex container and ask for <code>justify-content: space-between</code>, what should happen? The answer is that the fallback alignment of <code>flex-start</code> is used and your single item will align to the start of the flex container. In the case of <code>justify-content: space-around</code>, a fallback alignment of <code>center</code> is used.</p>

<p>In the current specification you can’t change what the fallback alignment is, so if you would prefer that the fallback for <code>space-between</code> was <code>center</code> rather than <code>flex-start</code>, there isn’t a way to do that. There is  which says that future levels may enable this.</p>

<h3 id="safe-and-unsafe-alignment">Safe And Unsafe Alignment</h3>

<p>A more recent addition to the Box Alignment specification is the concept of safe and unsafe alignment using the <em>safe</em> and <em>unsafe</em> keywords.</p>

<p>With the following code, the final item is too wide for the container and with unsafe alignment and the flex container on the left-hand side of the page, the item becomes cut off as the overflow is outside the page boundary.</p>

<pre><code class="language-css">.container {  
    display: flex;
    flex-direction: column;
    width: 100px;
    align-items: unsafe center;
}

.item:last-child {
    width: 200px;
}</code></pre>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/54359e1a-e4e4-445a-8fcc-e4ef59591bad/unsafe-alignment.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/54359e1a-e4e4-445a-8fcc-e4ef59591bad/unsafe-alignment.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/54359e1a-e4e4-445a-8fcc-e4ef59591bad/unsafe-alignment.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/54359e1a-e4e4-445a-8fcc-e4ef59591bad/unsafe-alignment.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/54359e1a-e4e4-445a-8fcc-e4ef59591bad/unsafe-alignment.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/54359e1a-e4e4-445a-8fcc-e4ef59591bad/unsafe-alignment.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/54359e1a-e4e4-445a-8fcc-e4ef59591bad/unsafe-alignment.png"
			sizes="100vw"
			alt="The overflowing item is centered and partly cut off"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Unsafe alignment will give you the alignment you asked for but may cause data loss ()
		</figcaption>
	
</figure>


<p>A safe alignment would prevent the data loss occurring, by relocating the overflow to the other side.</p>

<pre><code class="language-css">.container {  
    display: flex;
    flex-direction: column;
    width: 100px;
    align-items: safe center;
}

.item:last-child {
    width: 200px;
}</code></pre>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7e31128f-cc18-430d-aa06-9a5307021d0c/safe-alignment.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7e31128f-cc18-430d-aa06-9a5307021d0c/safe-alignment.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7e31128f-cc18-430d-aa06-9a5307021d0c/safe-alignment.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7e31128f-cc18-430d-aa06-9a5307021d0c/safe-alignment.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7e31128f-cc18-430d-aa06-9a5307021d0c/safe-alignment.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7e31128f-cc18-430d-aa06-9a5307021d0c/safe-alignment.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7e31128f-cc18-430d-aa06-9a5307021d0c/safe-alignment.png"
			sizes="100vw"
			alt="The overflowing item overflows to the right"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Safe alignment tries to prevent data loss ()
		</figcaption>
	
</figure>


<p>These keywords have limited browser support right now, however, they demonstrate the additional control being brought to Flexbox via the Box Alignment specification.</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="zLyVmQ"
   data-user="rachelandrew"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<h3 id="in-summary">In Summary</h3>

<p>The alignment properties started as a list in Flexbox, but are now in their own specification and apply to other layout contexts. A few key facts will help you to remember how to use them in Flexbox:</p>

<ul>
<li><code>justify-</code> the main axis and <code>align-</code> the cross axis;</li>
<li>To use <code>align-content</code> and <code>justify-content</code> you need spare space to play with;</li>
<li>The <code>align-content</code> and <code>justify-content</code> properties deal with the items as a group, sharing out space. Therefore, you can’t target an individual item and so there is no <code>-self</code> alignment for these properties;</li>
<li>If you do want to align one item, or split a group on the main axis, use auto margins to do so;</li>
<li>The <code>align-items</code> property sets all of the <code>align-self</code> values as a group. Use <code>align-self</code> on the flex child to set the value for an individual item.</li>
</ul>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(il)</span>
</div>


              </article>
            </body>
          </html>
---------------
<h1 id="#title_2" >3、文章： 使用契约测试提高分布式系统的质量</h1>
Marcin Grzejszczak
[http://www.infoq.com/cn/articles/contract-testing-spring-cloud-contract?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/contract-testing-spring-cloud-contract?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/contract-testing-spring-cloud-contract/zh/smallimage/logo-cloud-1527438712853-1534007382863.jpeg"/><p>在开发后期捕获软件缺陷的代价巨大。我们应该如何逐步测试一个复杂的分布式系统？在本文中，Marcin Grzejszczak分析了组件间通信的集成测试方法，并给出了一种使用契约测试和Spring Cloud Contract的解决方案。</p> <i>By Marcin Grzejszczak</i> <i> Translated by 盖磊</i>
---------------
<h1 id="#title_3" >4、文章： 人工智能与区块链初探：交集与前瞻</h1>
Matt Turck
[http://www.infoq.com/cn/articles/ai-blockchain?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/ai-blockchain?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/ai-blockchain/zh/smallimage/logo32-1534056750671.jpg"/><p>作者从VC风投的视角谈论了人工智能与区块链的联系及未来可能的交集。尽管很多人认为泡沫存在，但新技术的影响在短期确实往往被高估，而在长期却是被低估的。本文还展示了一些有趣的使用场景及实验项目，它们对未来的影响值得我们期待。</p> <i>By Matt Turck</i> <i> Translated by 王强</i>
---------------
<h1 id="#title_4" >5、文章： 实时音频混音技术在视频直播场景中的实践</h1>
冼牛
[http://www.infoq.com/cn/articles/remix-in-live-video?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/remix-in-live-video?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/remix-in-live-video/zh/smallimage/GettyImages-628837052-1518704902676-1534056150706.jpeg"/><p>最近半年，视频直播领域中产生不少创新玩法，其中包括K歌直播和合唱直播。这些创新玩法都用到实时音频混音技术。今天我们来聊一下混音技术的实现，及其在创新玩法中的应用。</p> <i>By 冼牛</i>
---------------
<h1 id="#title_5" >6、文章： 苏宁金融App全链路灰度实践</h1>
戴治波, 吴晨捷
[http://www.infoq.com/cn/articles/suing-jinrong-full-stack-grey-practice?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/suing-jinrong-full-stack-grey-practice?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/suing-jinrong-full-stack-grey-practice/zh/smallimage/java-logo-1516663617190-1534060596133.jpeg"/><p>打造快捷和可控的生产验证，对于移动端来讲需要一个完整的灰度解决方案。相比其他移动端的灰度方案，苏宁金融的方案既包括移动APP环节的灰度，也包括移动网关到整个APP后端服务环节的灰度，实现了在真实生产环境下，苏宁金融APP全链路的灰度。</p> <i>By 戴治波</i>
---------------
<h1 id="#title_6" >7、聪明的头脑+有趣的灵魂，揭秘腾讯云最暖智能酒店解决方案</h1>
孙春鹭
[http://www.infoq.com/cn/news/2018/08/Tencent-cloud-Smart-Hotel?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/08/Tencent-cloud-Smart-Hotel?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>什么是酒店真正的智能化？智能酒店如何成为未来酒店的发展方向……InfoQ记者采访了腾讯云技术总监曹涛和腾讯云资深产品经理李俊林，共同探秘腾讯云智能酒店解决方案以及智能酒店产业未来发展趋势。</p> <i>By 孙春鹭</i>
---------------
<h1 id="#title_7" >8、FEX 技术周刊 - 2018/08/13</h1>

[http://fex.baidu.com/blog/2018/08/fex-weekly-13//](http://fex.baidu.com/blog/2018/08/fex-weekly-13//)
作者：exialym <br> <h2 id="section">深阅读</h2>

<p><strong>V8 release v6.9</strong><br />
https://v8project.blogspot.com/2018/08/v8-release-69.html<br />
This post provides a preview of some of the highlights in anticipation of the release: Memory savings through embedded built-ins; Liftoff, WebAssembly’s new first-tier compiler; Faster DataView operations; Faster processing of WeakMaps during garbage collection;</p>

<p><strong>Announcing Dart 2 Stable and the Dart Web Platform</strong><br />
https://medium.com/dartlang/dart-2-stable-and-the-dart-web-platform-3775d5f8eac7<br />
We’re announcing the immediate availability of the stable release of Dart 2, including a rewrite of the Dart web platform that offers a unique combination of productivity, performance and scalability. With the release of Dart 2, web developers can now leverage the same language, libraries and tools along with a number of web-specific enhancements. 附：.</p>

<p><strong>New version of the Roadmap of Web Applications on Mobile</strong><br />
https://www.w3.org/blog/news/archives/7227<br />
W3C has published a new version of its , an overview of the various technologies developed in W3C that increase the capabilities of Web applications, and how they apply more specifically to the mobile context. The contents of the roadmap have been updated to follow the evolution of the Web platform since April 2018.</p>

<p><strong>Community questions following the eslint security incident</strong><br />
https://blog.npmjs.org/post/176488970320/community-questions-following-the-eslint-security<br />
Following the eslint incident on July 12, 2018, the community reached out to us with a few follow-up questions. This post will answer those questions as well as provide some additional technical insight into the eslint-scope malware that we haven’t seen discussed elsewhere.</p>

<p><strong>从前端技术进化到体验科技</strong><br />
https://mp.weixin.qq.com/s/IYddaaw2ps1wR2VT1dZWPg<br />
玉伯分享了他从前端一路进阶升级到体验科技的个人思考，并详细介绍了体验科技的历史及未来发展，以及本次体验科技开放的愿景。前端的本质是什么？随着移动和物联网的发展，前端技术又会有哪些变化？希望通过本文内容大家能对这些问题以及体验科技有更进一步的了解。</p>

<p><strong>聊聊CSS中的层叠相关概念</strong><br />
https://www.w3cplus.com/css/understand-css-stacking-context-order-z-index.html<br />
对于众多CSSer来说，阅读CSS的规范和理解相关的概念都是枯燥无味的。而且很多同学理解一些概念都比较吃力。比如这篇文章中提到的相关概念： 文档流（Normal Flow）、格式化上下文（Formatting Context）、层叠上下文（Stacking Context）、层叠水平（Stacking Level） 和 层叠顺序（Stacking Order）。虽然这些概念是CSS的基础，但很多同学都一直不愿去触碰，因为它们看起来简单，事实上还是较为复杂的。如查我们花一定的时间理解了这些概念，能帮助我们更好的理解CSS中其他相关的概念和知识点，特别是z-index的运用。</p>

<p><strong>美团扫码付的前端可用性保障实践</strong><br />
https://tech.meituan.com/qrcode_web_availability_guarantee.html<br />
2017年，美团金融前端遇到了很多通用性问题，特别是在保障前端可用性的过程中，我们团队也踩了不少“坑”，在梳理完这些问题以后，我们还专门做了一期线下沙龙给大家进行了分享。不管是在面试过程中与候选人讨论，还是在团队内的和我们前端小伙伴讨论，都能发现很多同学有一个共同点，对所做的工作缺乏判断，包括如何评判工作交付的质量，如何评判产品与客户之间的触达率等等，这些问题其实比“埋头敲代码”重要很多。今天抛砖引玉，分享一下我们团队的思考，希望能帮助更多的同学对前端可用性的保障工作，有一个更全面的认识。</p>

<p><strong>为什么现在的前端开发工程师都只在提技术和造轮子，并不怎么关注UI和UX相关的东西</strong><br />
https://www.zhihu.com/question/288641999<br />
这是一个值得思考的问题。其实 UI 是可以成为产品核心竞争力的，比如 Apple。</p>

<p><strong>精读 The Cost of JavaScript</strong><br />
https://zhuanlan.zhihu.com/p/41292532<br />
作者首先将全文的内容压缩成几条观点总结出来，之后从用户体验为 Web 带来的变化开始说起，到 JavaScript 的成本有哪些、它们为何如此高昂、如何降低开销以及持续集成，全文形成一个非常完整的优化流程。</p>

<p><strong>Pseudo Localization @ Netflix</strong><br />
https://medium.com/netflix-techblog/pseudo-localization-netflix-12fff76fbcbe<br />
In the past 8 years Netflix has transformed from an English-only product, to now supporting 26 languages and growing. As we add language support for our members residing in 190 different countries, scaling globalization at Netflix has never been more important. Along the way we’ve built out countless solutions to help us achieve globalization at scale. In this article we’ll focus on one my team has been working on, Pseudo Localization.</p>

<p><strong>A Breath of Life: Welcome the Brand New Mobile Web Dashboard</strong><br />
https://engineering.tumblr.com/post/176808165864/javascript-a-breath-of-life-welcome-the-brand<br />
We rebuilt another piece of the site with React. And the rewrite turned out really well. Even with more features like pull-to-refresh, a new activity popover, and modern audio and video players, we sped up our DOM content loaded time by 35%! The new page has a lot of modern web standards in it too like srcsets, flexbox, asynchronous bundle loading, and a web app manifest.</p>

<p><strong>Webhint.io – hinting at a better web</strong><br />
https://christianheilmann.com/2018/08/07/webhint-io-hinting-at-a-better-web/<br />
we released a new, rebranded version of the tool. It is now called  and you can find it on GitHub, use it at webhint.io or use it as a node module using npm, yarn or whatever other package installer you want to use. By default webhint tests for these features of great web products: Performance, Accessibility, Browser Interoperability, Security, Sensible configuration of build tools and PWA Readiness.</p>

<p><strong>How to deal with dirty side effects in your pure functional JavaScript</strong><br />
https://jrsinclair.com/articles/2018/how-to-deal-with-dirty-side-effects-in-your-pure-functional-javascript/<br />
ow, when I say they cheat, they technically follow the rules. But they find loopholes in those rules and stretch them big enough to drive a herd of elephants through. There’s two main ways they do this: Dependency injection, or as I call it, chucking the problem over the fence; and Using an Effect functor, which I think of as extreme procrastination.</p>

<p><strong>GLB: GitHub’s open source load balancer</strong><br />
https://githubengineering.com/glb-director-open-source-load-balancer/<br />
GLB Director is a Layer 4 load balancer which scales a single IP address across a large number of physical machines while attempting to minimise connection disruption during any change in servers. GLB Director does not replace services like haproxy and nginx, but rather is a layer in front of these services (or any TCP service) that allows them to scale across multiple physical machines without requiring each machine to have unique IP addresses.</p>

<p><strong>GraphQL on the server</strong><br />
https://www.joyent.com/blog/graphql-on-the-server<br />
In the following post we’ll quickly explain what GraphQL is and why you might want to consider it. GraphQL is a querying language for APIs, and we have been using it as an alternative to REST. 另附：.</p>

<p><strong>Two Years Later: APIs are the Destination</strong><br />
https://www.ebayinc.com/stories/blogs/tech/two-years-later-apis-are-destination/<br />
eBay speaks API! Two years ago, we started a journey to deliver a new, modern family of APIs to expose marketplace capabilities to sellers and buyers. The APIs evolved and grew with the business and enabled expansion to new experiences. They are built by developers for developers and treated as first-class products at eBay. We delivered a simple, consistent, and well-documented API portfolio rather than an API maze where it is challenging to discover capabilities.</p>

<p><strong>Why Status Codes Matter in Data Delivery</strong><br />
https://segment.com/blog/why-status-codes-matter-in-data-delivery/<br />
Segment engineering has taken lengths to operate reliably in this environment. Our latest efforts have been around visibility into the HTTP response codes from destinations. We spent the last few months adding hooks to measure everything from the volume of events, how quickly they are sent to destinations, and what HTTP status code and error response body, if any, occurred for every request. This instrumentation is ultimately for Segment users to see into the black box to answer one question: how do delivery challenges affect my data? To this end, we built .</p>

<p><strong>Use Cloudflare Stream to build secure, reliable video apps</strong><br />
https://blog.cloudflare.com/why-use-stream/<br />
If I had to summarize what we’ve learned as we’ve built Stream it would be: Video streaming is hard, but building a successful video streaming business is even harder. This is why our goal has been to take away the complexity of encoding, storage, and smooth delivery so you can focus on all the other critical parts of your business.</p>

<p><strong>If You’re Not Monitoring Your Resource Pools, You’re Doing It Wrong</strong><br />
https://blog.newrelic.com/engineering/monitor-resource-pools/<br />
In my four years at New Relic I’ve been responsible for the health of dozens of different services. Something they all had in common was that when they failed you could always see something going on in their resource pools.</p>

<p><strong>Prometheus - transforming monitoring over the years</strong><br />
https://coreos.com/blog/prometheus-transforming-monitoring-over-years<br />
Prometheus is easy to set up as a single, statically linked binary that can be downloaded and started with a single command. In tandem with this simplicity, it scales to hundreds of thousands of samples per second ingested on modern commodity hardware. Prometheus’ architecture is well suited for dynamic environments in which containers start and stop frequently, instead of requiring manual re-configuration. .</p>

<p><strong>Writing Good Documentation for Your Open-Source Library</strong><br />
https://brainhub.eu/blog/writing-good-documentation-open-source-library/<br />
There are many parts to a documentation, among others: Readme, Reference, Guide, Cookbook, Blog post. Each of these fulfills different purposes, and the boundary between kinds of docs is sometimes blurred. 另附：.</p>

<h2 id="section-1">新鲜货</h2>

<p><strong>Julia 1.0</strong><br />
https://julialang.org/blog/2018/08/one-point-zero<br />
Scientific computing has traditionally required the highest performance, yet domain experts have largely moved to slower dynamic languages for daily work. We believe there are many good reasons to prefer dynamic languages for these applications, and we do not expect their use to diminish. Fortunately, modern language design and compiler techniques make it possible to mostly eliminate the performance trade-off and provide a single environment productive enough for prototyping and efficient enough for deploying performance-intensive applications. The Julia programming language fills this role: it is a flexible dynamic language, appropriate for scientific and numerical computing, with performance comparable to traditional statically-typed languages.</p>

<p><strong>Vue CLI 3.0 is here!</strong><br />
https://medium.com/the-vue-point/vue-cli-3-0-is-here-c42bebe28fbb<br />
Over the past few months, we’ve been working really hard on the next generation of Vue CLI, the standard build toolchain for Vue applications. Today we are thrilled to announce the release of Vue CLI 3.0 and all the exciting features that come with it. 另附：.</p>

<p><strong>First Babel 7.0 Release Candidates</strong><br />
https://github.com/babel/babel/releases/tag/v7.0.0-rc.1<br />
附：</p>

<p><strong>Ultralight - HTML UI Engine</strong><br />
https://ultralig.ht/<br />
Ultralight is the lighter, faster option to integrate HTML UI in your C++ app.</p>

<p><strong>WebReplay</strong><br />
https://developer.mozilla.org/en-US/docs/Mozilla/Projects/WebReplay<br />
介绍 firefox 新版重放功能的实现，可以支持 JS、DOM、图形的重放，看起来很厉害</p>

<p><strong>The Transport Layer Security (TLS) Protocol Version 1.3</strong><br />
https://tools.ietf.org/html/rfc8446<br />
This document specifies version 1.3 of the Transport Layer Security (TLS) protocol.  TLS allows client/server applications to communicate over the Internet in a way that is designed to prevent eavesdropping, tampering, and message forgery.  附：.</p>

<p><strong>Internet Archive, decentralized</strong><br />
https://dweb.archive.org/<br />
A goal in creating a Decentralized Web is to reduce or eliminate such centralized points of control. That way, too, if any player drops out, the system still works. Such a system could better help protect user privacy, ensure reliable access, and even make it possible for users to buy and sell directly, without having to go through websites that now serve as middlemen, and collect user data in the process. 另附：.</p>

<p><strong>Mavo - A new, approachable way to create Web applications</strong><br />
http://mavo.io/<br />
Create complex, reactive, persistent web applications by just writing HTML &amp; CSS, without a single line of JavaScript and no server backend. 另附：， Retool makes building internal software faster by pre-building common components.</p>

<p><strong>Introducing Android 9 Pie</strong><br />
https://android-developers.googleblog.com/2018/08/introducing-android-9-pie.html<br />
Android 9 harnesses the power of machine learning to make your phone smarter, simpler, and tailored to you. Read all about the new consumer features here. For developers, Android 9 includes many new ways to enhance your apps and build new experiences to drive engagement.</p>

<p><strong>Introducing Electron Fiddle</strong><br />
https://medium.com/@felixrieseberg/introducing-electron-fiddle-1de2be1ba6e7<br />
We’re releasing a first version of , an attempt to bring the same playfulness to cross-platform desktop development with Electron.  Electron Fiddle lets you create, share, and play with small Electron experiments. It greets you with a quick-start template after opening — change a few things, choose the version of Electron you want to run it with, and play around.</p>

<p><strong>Pts</strong><br />
https://github.com/williamngan/pts<br />
Pts is a typescript/javascript library for visualization and creative-coding.</p>

<p><strong>Angular Console — The UI for the Angular CLI</strong><br />
https://blog.nrwl.io/angular-console-the-ui-for-the-angular-cli-a5d0924240b7<br />
We realized that most developers don’t need more sophisticated commands — they need a more approachable way to use what the Angular CLI already does. And that’s what  is.</p>

<p><strong>react-day-picker</strong><br />
https://github.com/gpbl/react-day-picker<br />
Flexible date picker component for React. Highly customizable, localizable, with ARIA support, no external dependencies, 9KB gzipped. 另附：</p>

<p><strong>Dumper.js</strong><br />
https://github.com/zeeshanu/dumper.js<br />
dumper.js is a better and pretty variable inspector for your Node.js applications.</p>

<p><strong>franc - Detect the language of text</strong><br />
https://github.com/wooorm/franc<br />
What’s so cool about franc? franc can support more languages(†) than any other library; franc is packaged; with support for 82, 188, or 402 languages; franc has a CLI.</p>

<p><strong>camaro</strong><br />
https://github.com/tuananh/camaro<br />
camaro is an utility to transform XML to JSON, using Node.js binding to native XML parser pugixml, one of the fastest XML parser around.</p>

<p><strong>Got - Simplified HTTP requests</strong><br />
https://github.com/sindresorhus/got<br />
Got is a human-friendly and powerful HTTP request library. It was created because the popular request package is bloated.</p>

<p><strong>Teutonic CSS</strong><br />
https://teutonic.co/<br />
A modern CSS framework — versatile, well documented.</p>

<p><strong>Bash Infinity</strong><br />
https://github.com/niieani/bash-oo-framework<br />
Bash Infinity is a standard library and a boilerplate framework for writing tools using bash. It’s modular and lightweight, while managing to implement some concepts from C#, Java or JavaScript into bash. The Infinity Framework is also plug &amp; play: include it at the beginning of your existing script to import any of the individual features such as error handling, and start using other features gradually. The aim of Bash Infinity is to maximize readability of bash scripts, minimize the amount of code repeat and create a central repository for well-written, and a well-tested standard library for bash. Bash Infinity transforms the often obfuscated “bash syntax” to a cleaner, more modern syntax.</p>

<h2 id="section-2">设计</h2>

<p><strong>Building a Design Culture of Inclusion</strong><br />
https://medium.com/google-design/building-a-design-culture-of-inclusion-6cb0bf7a927f<br />
Design=Empathy, Empathy=Understanding, Understanding=Exposure, Exposure=Meaning, Meaning=Inclusion, Inclusion=Design. And so you can see that a truly inclusive environment does not come together without thought or deliberate effort, and really takes an exercise in design thinking to bring a great team together.</p>

<p><strong>Introducing Supernova V4</strong><br />
https://medium.com/sketch-app-sources/introducing-supernova-v4-d21cd8c7a7e<br />
Forget what you’ve been told. Design to code is finally possible.
Ever since the first beta of Supernova, we’ve dreamed about the day when it would be possible to blend the world of design and code just so that people can work better, together. Today, we are unveiling Supernova V4, the most advanced design to code tool, available now! 另附：.</p>

<p><strong>Flow 1.0.0 – All the Polish</strong><br />
https://blog.prototypr.io/flow-1-0-0-all-the-polish-6ff708d788ea<br />
Flow is a production tool that lets you animate static designs in seconds, then export those animations to either HTML5 / CSS or Swift / iOS code.</p>

<p><strong>Utilizing Micro-interactions to Enhance Your UX Design</strong><br />
http://www.uxbooth.com/articles/utilizing-micro-interactions-to-enhance-your-ux-design/<br />
A website that works across all devices is also key to having a high conversion rate and building loyalty. For those striving for success, effectively enhancing UX micro-interactions—which are often overlooked—can make the difference between a customer that stays and a customer that hits the X button on their browser.</p>

<p><strong>Whatever The Approach, It’s The 4I’s!</strong><br />
http://moha.studio/labs/whatever-the-approach-its-the-4is.html<br />
Okay, if you did not read “” Read it and back again. As a reminder, you are reading this article as a part of the 4I’s serious: Whatever The Approach, It’s a 4I’s!. The 4I’s – Introduction to Inspiration. The 4I’s – Introduction to Ideation. The 4I’s – Introduction to Implementation. The 4I’s – Introduction to Iteration.</p>

<p><strong>How System Thinking Will Improve Your Product Design</strong><br />
http://sherif-amin.com/system-thinking-improve-product-design/<br />
I recognized it was a very complex challenge and unless I change my way of thinking about products and treat them as systems, I will never be able to solve these complexities.</p>

<p><strong>What is Typesetting?</strong><br />
https://alistapart.com/article/flexible-typesetting<br />
Typesetting is the most important part of typography, because most text is meant to be read, and typesetting involves preparing text for reading. 另附：.</p>

<h2 id="section-3">产品及其它</h2>

<p><strong>OpenAI Five Benchmark: Results</strong><br />
https://blog.openai.com/openai-five-benchmark-results/<br />
OpenAI Five won a best-of-three against a team of 99.95th percentile Dota players: Blitz, Cap, Fogged, Merlini, and MoonMeander — four of whom have played Dota professionally — in front of a live audience and 100,000 concurrent livestream viewers. 另附：.</p>

<p><strong>Where Vim Came From</strong><br />
https://twobithistory.org/2018/08/05/where-vim-came-from.html<br />
Vim is everywhere. It is used by so many people that something like HEX file support shouldn’t be a surprise. Vim comes pre-installed on Mac OS and has a large constituency in the Linux world. It is familiar even to people that hate it, because enough popular command line tools will throw users into Vim by default that the uninitiated getting trapped in Vim has become a meme. There are major websites, including Facebook, that will scroll down when you press the j key and up when you press the k key—the unlikely high-water mark of Vim’s spread through digital culture.</p>

<p><strong>7 open web champions on the greatest web challenges</strong><br />
https://webfoundation.org/2018/08/7-open-web-champions-on-the-greatest-web-challenges/<br />
Along with other digital rights organisations, our team attended the Internet Freedom Forum in Abuja in April. We took this opportunity to speak to our peers about the biggest issues we all face online today. Here’s what they said. 另附：</p>

<p><strong>Get to Know Our New Code of Conduct</strong><br />
https://stackoverflow.blog/2018/08/07/get-to-know-our-new-code-of-conduct/<br />
Stack Overflow began with a community of folks that were avid readers and pundits of Joel On Software and Coding Horror. As the initial community had some experience interacting with one another, “Be nice” was sufficient as a beacon to pull people back from over-enthusiastically critiquing other user’s contributions.</p>

<p><strong>拼多多为什么崛起</strong><br />
https://mp.weixin.qq.com/s/8C4aCqFhXjw9yMjUlWGKzQ<br />
拼多多为什么崛起？拼多多的用户体验有何不同？对拼多多用户有怎样的洞察？8 月 2 日，《产品经理 30 讲》作者梁宁在得到 APP 上，就最近最火的拼多多展开了一系列分析。经梁宁授权，首席品牌官把直播内容整理后，分享给大家。可以说，这绝对是目前市场上面对于拼多多的解读和研究最深刻的一次。拼多多包括低端供应链也好，怎么着也好，大家在这个过程中叫做过程的机会，或者叫过程的原罪。但最终的终局一定是体验的平等。另附：.</p>

<p><strong>知乎的「好恶」</strong><br />
http://www.geekpark.net/news/231818<br />
在目前互联网社区运营中，普遍被认可的做法是不断扩展用户边界，做大流量，拿到好看的日活、月活数据。知乎却反常地用一些可量化的指标来肯定符合其所认可价值观的用户，这种做法既让人意外，又好像很「知乎」。</p>

<p>— THE END –</p>
---------------
<h1 id="#title_8" >9、Git实用技巧和命令</h1>
viktor
[http://www.infoq.com/cn/news/2018/08/git-techinique-commands-trick?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/08/git-techinique-commands-trick?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Git是一个非常强大的工具，它包含丰富的工具用以维护项目。本文我们将会看见一些Git日常使用过程中的实用技巧和命令。希望其中的一些内容能够对读者有所帮助。</p> <i>By viktor</i> <i> Translated by 金灵杰</i>
---------------
<h1 id="#title_9" >10、Microsoft Quantum Katas帮助开发人员探索使用Q#实现量子计算</h1>
Sergio De Simone
[http://www.infoq.com/cn/news/2018/08/microsoft-quantum-katas?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/08/microsoft-quantum-katas?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Microsoft根据“软件招式”（Code Katas）这一理念，开源了一个称为“Quantum Katas”的项目。该项目意在帮助开发人员迈出使用Q#语言实现量子计算的第一步。它提供了一组复杂度递增的编程练习，并可向学习者提供即刻反馈。</p> <i>By Sergio De Simone</i> <i> Translated by 盖磊</i>
---------------
<h1 id="#title_10" >11、eBay通过事件溯源实现持续交付</h1>
Jan Stenberg
[http://www.infoq.com/cn/news/2018/08/event-sourcing-ebay?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/08/event-sourcing-ebay?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>eBay的持续交付团队通过使用以事件为中心的方法构建了一个可以持续交付的编配器，具备故障弹性和伸缩性，以便处理eBay构建管道中不断增加的负载。John Long和Nataraj Sundar在两篇博文中描述了事件溯源的好处以及在实际应用程序开发当中所具备的优势。</p> <i>By Jan Stenberg</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_11" >12、微软把UWP定位成业务线应用程序开发平台</h1>
Jonathan Allen
[http://www.infoq.com/cn/news/2018/08/UWP-LOB-Win10?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/08/UWP-LOB-Win10?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>微软把UWP定位成传统业务线（LOB）应用程序开发平台，以使用Windows Template Studio实现快速应用程序开发为重点。但是，为了把LOB开发人员吸引到UWP平台，他们在做的事情不止这些。</p> <i>By Jonathan Allen</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_12" >13、我是如何用2个Unix命令给SQL提速的</h1>
spinellis
[http://www.infoq.com/cn/news/2018/08/unix-commands-slash-sql?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/08/unix-commands-slash-sql?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>我试图在MariaDB（MySQL）上运行一个简单的连接查询，但性能简直糟糕透了。这篇文字将介绍我是如何通过两个简单的Unix命令，将查询时间从380小时降到12小时以下的。</p> <i>By spinellis</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_13" >14、汇聚40+机器学习最佳落地案例，第二届AICon来了！</h1>
孟夕
[http://www.infoq.com/cn/news/2018/08/AICon-machine-learning?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/08/AICon-machine-learning?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>由极客邦科技旗下 InfoQ 中国主办的第二届AICon全球人工智能与机器学习技术大会，将于12月份在北京举行，我们将为参会者全方位介绍AI&机器学习技术趋势和最佳实践案例。</p> <i>By 孟夕</i>
---------------