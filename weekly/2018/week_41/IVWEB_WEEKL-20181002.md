## 文章索引
1、 <a href="#1the-new-framer-x:-initial-impressions" >The New Framer X: Initial Impressions</a><br/>
2、 <a href="#2october-magic-for-your-desktop-2018-edition" >October Magic For Your Desktop (2018 Edition)</a><br/>
3、 <a href="#3文章-ddd返工" >文章： DDD返工</a><br/>
4、 <a href="#4不畏智能调度的核心是对业务数据的价值挖掘和有效利用" >不畏：智能调度的核心是对业务数据的价值挖掘和有效利用</a><br/>
5、 <a href="#5百度智能小程序月活破亿正式开放申请" >百度智能小程序月活破亿，正式开放申请</a><br/><h1 id="#title_0" >1、The New Framer X: Initial Impressions</h1>
Lachezar Petkov
[https://www.smashingmagazine.com/2018/10/new-framer-x-initial-impressions/](https://www.smashingmagazine.com/2018/10/new-framer-x-initial-impressions/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/10/new-framer-x-initial-impressions/" />
              <title>The New Framer X: Initial Impressions</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>The New Framer X: Initial Impressions</h1>
                  
                    
                    <address>Lachezar Petkov</address>
                  
                  <time datetime="2018-10-01T13:30:03&#43;02:00" class="op-published">2018-10-01T13:30:03+02:00</time>
                  <time datetime="2018-10-01T11:38:55&#43;00:00" class="op-modified">2018-10-01T11:38:55+00:00</time>
                </header>
                <p>The Framer team recently released a new prototyping tool, , and I was lucky enough to be able to test it during the beta phase. In this article, I’d like to share my thoughts about this new tool and its features. I’ll make a comparison with the “legacy” Framer app as well as other tools, and I’ll discuss its brand new features such as <em>Stacks</em> and <em>Scroll</em>, and its new <em>Code</em> and <em>Design</em> components.</p>

<p>This article is intended for UI and UX designers who would like to learn more about Framer X’s prototyping abilities. Since it is (in many ways) a brand new product, you don’t need to be familiar with the  are beneficial.</p>

<p>For the purpose of this tutorial, I have also created a prototype which is a ’s app for Android.</p>

<p><strong>Note</strong>: <em>I’m in no way affiliated with Khan Academy; I just thought this would make a cool experiment &mdash; I hope you’ll agree.</em></p>

<h3>Intro To Framer X</h3>

<p>Framer X goes a few steps further than its predecessor in trying to bridge the gap between interface design and software development. Here’s how:</p>

<h4>Dear Designers, Meet React</h4>

<p>The key difference between the old and the new applications in this regard is the introduction of , as opposed to using CoffeeScript for programming microinteractions and animations, loading data, and so on.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b1964809-2686-43ff-b0a9-496ec03b6009/framerx-react-logos.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b1964809-2686-43ff-b0a9-496ec03b6009/framerx-react-logos.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b1964809-2686-43ff-b0a9-496ec03b6009/framerx-react-logos.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b1964809-2686-43ff-b0a9-496ec03b6009/framerx-react-logos.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b1964809-2686-43ff-b0a9-496ec03b6009/framerx-react-logos.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b1964809-2686-43ff-b0a9-496ec03b6009/framerx-react-logos.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b1964809-2686-43ff-b0a9-496ec03b6009/framerx-react-logos.jpg"
			sizes="100vw"
			alt="Framer X and React logos"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Framer X’s most important feature: It integrates tightly with ReactJS. ()
		</figcaption>
	
</figure>


<p>During the beta phase, people wrote some React components that I think show us the potential of how far the tool can take us. For example, you can embed actual media players (that actually stream and play music and video) within your prototypes. Or, you can  into other languages. And that’s not all: Things are just getting started.</p>



  <aside class="product-panel product-panel__tilted product-panel--book" data-audience="non-subscriber">
    <div class="container product-panel--book__container">
      <div class="panel__description panel__description--book">

    <p>Meet .</p>
    <a href="https://smashed.by/confpanelspeakers" class="btn btn--green btn--large">
      Check all topics&nbsp;and&nbsp;speakers&nbsp;↬
    </a>
      </div>
      <div class="panel__image panel__image--book">

  <a href="https://www.smashingconf.com/ny-2018/" class="books__book__image">
  <div class="books__book__img">
          <img src="https://www.smashingmagazine.com/images/smashing-cat/cat-scubadiving-panel.svg" alt="Smashing TV, with live sessions for professional designers and developers." width="310" height="400">
        </div>
      </a>
      </div>
    </div>
  </aside>




<p>The same React code you write for a Framer X prototype could &mdash; at least hypothetically &mdash; be used in a production environment after the design phase. This can be especially useful for teams that do a lot of web development in React (and perhaps for teams who write mobile apps in React Native). Personally, I shudder at the thought of me, <em>a designer</em>, writing any code that goes into production, but that might work for others.</p>

<blockquote>“Framer X is more like Unity than like Photoshop. An IDE for design, if you will.”<br /><br />&mdash;The Framer X documentation</blockquote>

<h4>The Framer X Interface</h4>

<p>If you are already a Framer user, the first thing you’d notice is that the integrated code editor is gone. Instead, if you want to write any code, you can use an editor of your choice. Most people (including myself) seem to go with .</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/69f945d8-23cc-4746-b5b8-96635a80202b/framerx-screenshot.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/69f945d8-23cc-4746-b5b8-96635a80202b/framerx-screenshot.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/69f945d8-23cc-4746-b5b8-96635a80202b/framerx-screenshot.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/69f945d8-23cc-4746-b5b8-96635a80202b/framerx-screenshot.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/69f945d8-23cc-4746-b5b8-96635a80202b/framerx-screenshot.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/69f945d8-23cc-4746-b5b8-96635a80202b/framerx-screenshot.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/69f945d8-23cc-4746-b5b8-96635a80202b/framerx-screenshot.png"
			sizes="100vw"
			alt="Framer X screenshot"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Framer X ()
		</figcaption>
	
</figure>


<p>There are four tabs in the sidebar:</p>

<ul>
<li><strong>Tools</strong><br />
Opens all the layout and drawing tools everyone’s familiar with (shapes, path, text, ) as well as three new toys we’ll discuss a little later: Stacks, Link, and Scroll.</li>
<li><strong>Layers</strong><br />
Contains, well, the layers of the selected frame, as well as its properties (color, position, border, shadow and so on). This bit is essentially the same as in the old Framer, and very similar to Sketch and Figma.</li>
</ul>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/19a4751f-b6ca-46fb-ae35-5e3bba22bc30/framerx-layers.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/19a4751f-b6ca-46fb-ae35-5e3bba22bc30/framerx-layers.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/19a4751f-b6ca-46fb-ae35-5e3bba22bc30/framerx-layers.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/19a4751f-b6ca-46fb-ae35-5e3bba22bc30/framerx-layers.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/19a4751f-b6ca-46fb-ae35-5e3bba22bc30/framerx-layers.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/19a4751f-b6ca-46fb-ae35-5e3bba22bc30/framerx-layers.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/19a4751f-b6ca-46fb-ae35-5e3bba22bc30/framerx-layers.jpg"
			sizes="100vw"
			alt="The Framer X layers panel"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The Framer X Layers panel. ()
		</figcaption>
	
</figure>


<ul>
<li><strong>Components</strong><br />
This is for any Design or Code components you may have in the file you’ve opened.</li>
<li><strong>Store</strong><br />
A new, huge feature in Framer X. It allows users to publish their creations &mdash; be it icons and illustrations or interactive code components for others to use. Currently, all components are free of charge, but I’d imagine people will be able to sell their stuff at the store in the future.</li>
</ul>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b23a6c15-9283-4bce-9677-54d3a9eb08cb/framerx-store.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b23a6c15-9283-4bce-9677-54d3a9eb08cb/framerx-store.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b23a6c15-9283-4bce-9677-54d3a9eb08cb/framerx-store.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b23a6c15-9283-4bce-9677-54d3a9eb08cb/framerx-store.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b23a6c15-9283-4bce-9677-54d3a9eb08cb/framerx-store.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b23a6c15-9283-4bce-9677-54d3a9eb08cb/framerx-store.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b23a6c15-9283-4bce-9677-54d3a9eb08cb/framerx-store.png"
			sizes="100vw"
			alt="The Framer X Store"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The Framer X Store ()
		</figcaption>
	
</figure>


<p>The <strong>Preview</strong> and <strong>Live Preview</strong> buttons are up at the top right corner. As with legacy Framer, you can preview your prototypes within a device picture for more realism, or preview them directly on an actual device, or in a browser.</p>

<p><strong>Recommended reading</strong>: <em></em></p>

<h3>Prototyping With Framer X</h3>

<h4>A Few Thoughts On The Prototype We’ll Create</h4>

<p>The Khan Academy Android app isn’t a , so let’s explore how it might look and behave if it was. I want to think of this as if it were a real-world project, so here are a couple of considerations that we’ll see how to handle in Framer X:</p>

<ol>
<li>The product’s goal is to provide free education for everyone, thus it must be able to run on old and cheap devices. What this means for the design of the prototype is, it has to work on <code>320dp</code> wide screens.</li>
<li>The design must adapt well when the app is translated into a language more verbose than English.</li>
</ol>

<p>The first thing I’m going to do is mock up the <em>Home</em> screen. There are four things I want to be prominent:</p>

<ul>
<li>A search input;</li>
<li>Something that will show me my most recent activity;</li>
<li>Something that will show me my Missions;</li>
<li>Something to notify me if there’s a new Mastery Challenge.</li>
</ul>

<p>Let’s begin.</p>

<h4>Installing Components From The Store</h4>

<p>The first two elements I want to have here are the Android status bar and navigation bar. Instead of drawing them myself, I’ll quickly install a component bundle from the store called “”. It contains all sorts of (static, not programmed in this case) elements like buttons, cards, switches, bars, keyboards and so on. I got my status bar and my nav bar in seconds:</p>

<figure><figcaption>Adding a component from the Store</figcaption></figure>

<p><strong>Note</strong>: <em>Each component is installed per-project.</em></p>

<h4>The Interactive Scroll Tool</h4>

<p>Now, if I were doing this in Sketch, I’d continue mocking up the rest of the elements on the same artboard, and if it can’t fit all elements, I’d make it taller. In Framer X, however, things work a little differently. I’ll have the <em>content</em> of the Home screen within a separate frame (screen/artboard) and <em>link</em> that frame so it scrolls beneath the navigation and status bars of the home screen:</p>

<figure><figcaption>Using the Scroll tool</figcaption></figure>

<p>Now when I run a preview, my content is scrollable:</p>

<figure><figcaption>The Scroll tool in action</figcaption></figure>

<p>Awesome! With the underlying work out of the way, I’m ready to increase the fidelity a little bit. First, I want the general style of the app to be soft and welcoming, so I’ll use <code>4dp</code> (display points) border-radius for my cards and buttons, and the .</p>

<p>Since having an actual search input is super important for this screen, I don’t want the regular Android  and search icon experience. I’ll go for an actual input with a CTA message along with a hamburger icon ala Google Maps.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ce79cd74-8e85-4d82-886d-e0457cb91521/proto-appbar.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ce79cd74-8e85-4d82-886d-e0457cb91521/proto-appbar.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ce79cd74-8e85-4d82-886d-e0457cb91521/proto-appbar.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ce79cd74-8e85-4d82-886d-e0457cb91521/proto-appbar.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ce79cd74-8e85-4d82-886d-e0457cb91521/proto-appbar.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ce79cd74-8e85-4d82-886d-e0457cb91521/proto-appbar.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ce79cd74-8e85-4d82-886d-e0457cb91521/proto-appbar.jpg"
			sizes="100vw"
			alt="The app bar and search input for this prototype"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The app bar and search input for this prototype ()
		</figcaption>
	
</figure>


<p>If I were to go deeper here, I’d make this bar a code component and write it so it expands to full width on scroll, like this:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/af3f157b-1686-4dc6-92ee-ef55cda9a81e/proto-appbar-expanded.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/af3f157b-1686-4dc6-92ee-ef55cda9a81e/proto-appbar-expanded.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/af3f157b-1686-4dc6-92ee-ef55cda9a81e/proto-appbar-expanded.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/af3f157b-1686-4dc6-92ee-ef55cda9a81e/proto-appbar-expanded.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/af3f157b-1686-4dc6-92ee-ef55cda9a81e/proto-appbar-expanded.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/af3f157b-1686-4dc6-92ee-ef55cda9a81e/proto-appbar-expanded.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/af3f157b-1686-4dc6-92ee-ef55cda9a81e/proto-appbar-expanded.jpg"
			sizes="100vw"
			alt="The app bar, expanded on scroll"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The app bar, expanded on scroll ()
		</figcaption>
	
</figure>


<p>I won’t do that for the purpose of this article, but I have to say I think something as simple would be easier to do in legacy Framer compared to Framer X &mdash; at least in this first version.</p>

<h4>Linking</h4>

<p>Let’s add some basic interactivity to this thing! When I tap on the search input, I want it to pull out a keyboard from the bottom. When I tap on the menu icon, however, I want to pull out a  from the left side.</p>

<p>Whereas in legacy Framer I’d have to write a  for this type of thing, it’s now super easy in Framer X and with its new Link tool! It’s similar to other prototyping applications in which I’d select a UI element, link it to a frame, and choose the type of transition I want. I imported the keyboard from the Android Kit component and linked to it from the search input. I set the transition to <strong>Overlay</strong> and the direction to <em>bottom</em>.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b9788340-9055-4097-8f4f-0f5a86b6b390/linking.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b9788340-9055-4097-8f4f-0f5a86b6b390/linking.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b9788340-9055-4097-8f4f-0f5a86b6b390/linking.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b9788340-9055-4097-8f4f-0f5a86b6b390/linking.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b9788340-9055-4097-8f4f-0f5a86b6b390/linking.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b9788340-9055-4097-8f4f-0f5a86b6b390/linking.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b9788340-9055-4097-8f4f-0f5a86b6b390/linking.jpg"
			sizes="100vw"
			alt="The Links panel"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Once you link two frames, you can configure the link through the Links panel. ()
		</figcaption>
	
</figure>


<p>Because I have too many items in the navigation drawer to fit on a screen, I had to split it into two frames just like the <em>Home</em> screen: one container with a scroll layer linked to a frame with the actual content inside. Here’s how that looks:</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/87bbf38f-16dc-4e18-9afb-f264339655b9/linked-frames.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/87bbf38f-16dc-4e18-9afb-f264339655b9/linked-frames.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/87bbf38f-16dc-4e18-9afb-f264339655b9/linked-frames.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/87bbf38f-16dc-4e18-9afb-f264339655b9/linked-frames.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/87bbf38f-16dc-4e18-9afb-f264339655b9/linked-frames.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/87bbf38f-16dc-4e18-9afb-f264339655b9/linked-frames.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/87bbf38f-16dc-4e18-9afb-f264339655b9/linked-frames.jpg"
			sizes="100vw"
			alt="Linked frames"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The 'Birdseye' view of all linked frames in the prototype so far ()
		</figcaption>
	
</figure>


<figure class="video-container"><iframe data-src="https://player.vimeo.com/video/291475598" width="600" height="480" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe></figure>

<p><em>Interacting with the prototype</em></p>

<p>Neat! There is a problem with this approach, though, that the Framer team will hopefully fix. When the transition of a frame is set to <strong>Overlay</strong>, it covers and dims <em>everything</em> beneath it. This isn’t quite what we want when we prototype for Android: The nav bar and status bar have to be <em>above all</em> other screen elements &mdash; including the overlays.</p>

<p>Same goes for the Search interface: I don’t want any screen dimming if I want to have filtering options and/or a list of recent queries when the keyboard is pulled out. Hopefully, we’ll see some fixes for these issues in future Framer X versions.</p>

<div class="sponsors__wide-place"></div>




<h4>Pinning, Positioning, And Responsiveness</h4>

<p>Back to the <em>Home</em> screen of the prototype. Below the search input, I want a list with my recent activity. Just as in legacy Framer and other design tools, you can pin elements within frames so they move and scale exactly as you want them to. Framer X also shows you distances and gaps between elements, snaps them together for you, and so on. Have a look:</p>

<figure><figcaption>Once my frames are pinned appropriately, designing responsively is very easy.</figcaption></figure>

<h4>Design Components</h4>

<p>I want to add a few more things to the prototype home screen: A <em>Mastery Challenge</em> prompt, a streak counter, list of missions, bookmarks and some UI that allows the user to explore content they might find cool or useful.</p>

<p>Since the recent missions and the bookmarks are going to be cards with very similar content, the best solution Framer X has for me is to use <strong>design components</strong>. I already mentioned them above (the Material Kit component bundle). Framer X’s design components work similarly to Sketch’s symbols and Figma’s components.</p>

<p>To convert a frame to a component, simply press <kbd>Cmd</kbd> + <kbd>K</kbd>. This creates a Master from which you can create as many instances as you want:</p>

<figure><figcaption>A Master component and its instance: Any changes applied to the Master are applied to the Instance, but not the other way around.</figcaption></figure>

<p>Anything you do to a Master component will affect its instances, but whatever you do to the instances won’t affect the Master. You can also nest Master components and go as crazy as you like.</p>

<p>So, here are my <em>Recent</em> missions and <em>Explore</em> sections:</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/df7737a3-e6be-456c-b807-e71711f963dc/horizontal-scroll.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/df7737a3-e6be-456c-b807-e71711f963dc/horizontal-scroll.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/df7737a3-e6be-456c-b807-e71711f963dc/horizontal-scroll.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/df7737a3-e6be-456c-b807-e71711f963dc/horizontal-scroll.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/df7737a3-e6be-456c-b807-e71711f963dc/horizontal-scroll.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/df7737a3-e6be-456c-b807-e71711f963dc/horizontal-scroll.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/df7737a3-e6be-456c-b807-e71711f963dc/horizontal-scroll.jpg"
			sizes="100vw"
			alt="Horizontally scrollable frames"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Recent missions and Explore sections as horizontally scrollable frames. ()
		</figcaption>
	
</figure>


<p>Each section is a frame, connected to its own scroll component, and populated with components. The text strings (as well as the bitmap images in the instances) are overrides.</p>

<h4>Stacks</h4>

<p>Now, what if I’m not sure how to position and distribute all these cards? Well, Framer X’s Stacks feature comes into play here:</p>

<figure class="video-container"><iframe data-src="https://player.vimeo.com/video/291477573" width="600" height="480" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe></figure>

<p>I only had to make sure that all items I wanted into a Stack are organized into frames. It works surprisingly well, and you can have components within a stack, as well as a stack within another stack, and so on. It’s huge for anyone mocking up and prototyping lists often!</p>

<h4>Drawing Icons And Illustrations</h4>

<p>The drawing tools in Framer X are pretty much the same as in legacy Framer. They’re good enough to do a lot, but still somewhat lagging behind Sketch’s: There are no rulers; you can’t convert strokes to outlines; you can’t flatten shapes; there’s no scissors tool.</p>

<figure class="video-container"><iframe data-src="https://player.vimeo.com/video/291477961" width="600" height="480" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe></figure>

<figure class="video-container"><iframe data-src="https://player.vimeo.com/video/291478285" width="600" height="480" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe></figure>

<h4>Code Components</h4>

<h5>Creating A Simple Code Component</h5>

<p>Finally, let’s take a closer look at the code components. Again, these are regular React components (both Stateless and Class) that can be written in either JavaScript or TypeScript (up to you). You can also install third-party libraries to use within your components in Framer.</p>

<p>Let’s try and use the popular  library. This will allow us to style our component using actual CSS syntax within the <em>.tsx</em> file.</p>

<p>First, go to the <strong>Components</strong> tab&nbsp;&rarr;&nbsp;<strong>New Component</strong>&nbsp;&rarr;&nbsp;<strong>from Code</strong>. After you name your component and confirm, your default system editor (in my case, VS Code) will open an example Framer X component file.</p>

<p>Now go to <strong>File</strong>&nbsp;&rarr;&nbsp;<strong>Show project folder</strong>,  if you haven’t already and add <code>styled-components</code> to your Framer project:

<pre><code class="language-javascript">$>yarn add styled-components
</code></pre>

<p>The library and its dependencies will be added to your <em>package.json</em> and you’re ready to go.</p>

<p>Here’s the source for my <code>styled-components</code> button, after I replaced the default code in my component’s <em>.tsx</em> file:</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4f94a6a9-72b6-430f-afe2-cbaeb3f6cd09/code-component.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4f94a6a9-72b6-430f-afe2-cbaeb3f6cd09/code-component.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4f94a6a9-72b6-430f-afe2-cbaeb3f6cd09/code-component.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4f94a6a9-72b6-430f-afe2-cbaeb3f6cd09/code-component.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4f94a6a9-72b6-430f-afe2-cbaeb3f6cd09/code-component.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4f94a6a9-72b6-430f-afe2-cbaeb3f6cd09/code-component.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4f94a6a9-72b6-430f-afe2-cbaeb3f6cd09/code-component.jpg"
			sizes="100vw"
			alt="The Go button code component and its source"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The Go button as a code component and its source ()
		</figcaption>
	
</figure>


<p>Note that the button label is customizable directly through the Framer X interface (because of the Framer library’s <code>PropertyControls</code> feature). Having my button written in code obviously has many advantages. It is customizable, responsive, and interactive. Along with the responsive paddings, it’s super easy to test if the design breaks in other languages.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/823ca42a-ca80-4864-bae0-8ff4a660ef51/code-component-lang.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/823ca42a-ca80-4864-bae0-8ff4a660ef51/code-component-lang.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/823ca42a-ca80-4864-bae0-8ff4a660ef51/code-component-lang.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/823ca42a-ca80-4864-bae0-8ff4a660ef51/code-component-lang.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/823ca42a-ca80-4864-bae0-8ff4a660ef51/code-component-lang.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/823ca42a-ca80-4864-bae0-8ff4a660ef51/code-component-lang.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/823ca42a-ca80-4864-bae0-8ff4a660ef51/code-component-lang.jpg"
			sizes="100vw"
			alt="The responsive Go button, translated quickly by changing the Text property directly in the Framer X UI."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The responsive Go button, translated quickly by changing the Text property directly in the Framer X UI. ()
		</figcaption>
	
</figure>


<h5>Importing A Code Component From The Store</h5>

<p>There’s a lot of video content on Khan Academy, so for my prototype, I want to open a video lesson. Instead of mocking up a ‘fake’ video player, I can directly embed an actual YouTube player in my prototype. There’s already a component in the Store for this purpose:</p>

<figure><figcaption>Playing a Khan Academy video in a Khan Academy prototype</figcaption></figure>

<p>You can fork the code of any Store component and edit it as you like. For now, the only way to do this is to right-click on it in the sidebar, copy its code and paste it in a newly created components’ file.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/55afd9c9-e6e3-4b06-a07e-d7bd78604d46/component-copy-code.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/55afd9c9-e6e3-4b06-a07e-d7bd78604d46/component-copy-code.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/55afd9c9-e6e3-4b06-a07e-d7bd78604d46/component-copy-code.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/55afd9c9-e6e3-4b06-a07e-d7bd78604d46/component-copy-code.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/55afd9c9-e6e3-4b06-a07e-d7bd78604d46/component-copy-code.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/55afd9c9-e6e3-4b06-a07e-d7bd78604d46/component-copy-code.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/55afd9c9-e6e3-4b06-a07e-d7bd78604d46/component-copy-code.jpg"
			sizes="100vw"
			alt="Copying a Store component’s code."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			You can copy every Store component’s code and play with it. ()
		</figcaption>
	
</figure>


<h4>Code Overrides And The Framer library</h4>

<p><strong>The Framer JavaScript library</strong> has now been ported to work with Framer X and React. As with the legacy Framer library, it provides us with tools (helper functions) to animate our designs and to listen to events (simple things like onClick and onMove, but also advanced events like pinch, whether the device has been rotated or whether an animation has ended, and more).</p>

<p><strong>Code Overrides</strong> are bits of code (JS functions) that allow you to change any frame’s or component’s properties. Static changes such as color are applied before you run the preview, directly within the Framer app, and the animations/interactions can be seen in the Preview window or on your preview device.</p>

<p>Let’s have a quick look at one of the simplest and default examples. I drew this simple champions cup illustration for one of the prototype cards, and I decided to animate it:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d7072f1f-80b4-4ed9-b0e9-b9352c8d5290/mastery-challenge.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d7072f1f-80b4-4ed9-b0e9-b9352c8d5290/mastery-challenge.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d7072f1f-80b4-4ed9-b0e9-b9352c8d5290/mastery-challenge.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d7072f1f-80b4-4ed9-b0e9-b9352c8d5290/mastery-challenge.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d7072f1f-80b4-4ed9-b0e9-b9352c8d5290/mastery-challenge.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d7072f1f-80b4-4ed9-b0e9-b9352c8d5290/mastery-challenge.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d7072f1f-80b4-4ed9-b0e9-b9352c8d5290/mastery-challenge.jpg"
			sizes="100vw"
			alt="The static Mastery Challenge card"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The static Mastery Challenge card ()
		</figcaption>
	
</figure>


<p>To add an override, I have to select my target frame (in this case the illustration) and click on the <em>Code</em> menu item in the right sidebar. Now I need to select the override I want from Exampels (selected by default in the drop down):</p>

<figure><figcaption>The Scale code override will provide me with a fun scale animation. I can edit it’s code and adjust as I like.</figcaption></figure>

<p>Remember, overrides are just blocks of code, therefore, they can live in any file within your project. What I just selected was the <em>Examples.tsx</em> file which contains multiple functions for Scale, Rotation, Fade, and so on. I can create my own file and write my own <code>Override</code> functions, or include them in my code components source code &mdash; just as long as I keep in mind to use the <code>Override</code>  when I <code>export</code> them.</p>

<div class="sponsors__wide-place"></div>




<p>Here’s the source code for the Scale override I chose:</p>

<pre class="break-out"><code class="language-javascript">export const Scale: Override = () => {
    return {
        scale: data.scale,
        onTap() {
            data.scale.set(0.6)
            animate.spring(data.scale, 1)
        },
    }
}
</code></pre>

<p>In plain English: Set the initial scale value of the frame down to 0.6, then animate the scale to 1 with spring curve. Finally, export it with name Scale and specify that it is an Override.</p>

<p>Once applied, this is the result:</p>

<figure><figcaption>The Mastery Challenge card with some animation</figcaption></figure>

<h4>Design Responsiveness</h4>

<p>As I mentioned in the beginning, it is essential for this particular prototype to work on small device screens (<code>320dp</code>). This is very easy to test in Framer X (considering you’ve pinned your UI elements properly, as described above). Simply set the Preview mode to <strong>Canvas - Responsive</strong>:</p>

<figure class="video-container"><iframe data-src="https://player.vimeo.com/video/291482276" width="600" height="480" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe></figure>

<p><em>Framer X makes it easy to test my designs for different screens.</em></p>

<p>This is super helpful &mdash; I am now aware of what problems my designs have on smaller screens, and I’m ready to come up with fixes for the next iteration!</p>

<h4>Day And Night Modes</h4>

<p>Finally, in Framer you have two themes: Light, called “Day” mode:</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3bda502f-cd59-4c33-bb15-3dc7d70a9e21/day-mode.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3bda502f-cd59-4c33-bb15-3dc7d70a9e21/day-mode.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3bda502f-cd59-4c33-bb15-3dc7d70a9e21/day-mode.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3bda502f-cd59-4c33-bb15-3dc7d70a9e21/day-mode.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3bda502f-cd59-4c33-bb15-3dc7d70a9e21/day-mode.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3bda502f-cd59-4c33-bb15-3dc7d70a9e21/day-mode.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3bda502f-cd59-4c33-bb15-3dc7d70a9e21/day-mode.jpg"
			sizes="100vw"
			alt=" Framer X  day (light) mode"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Framer X during the day ()
		</figcaption>
	
</figure>


<p>And dark, called “Night” mode:</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/14a5b801-3452-4033-8dc8-6e6fc057fcb7/night-mode.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/14a5b801-3452-4033-8dc8-6e6fc057fcb7/night-mode.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/14a5b801-3452-4033-8dc8-6e6fc057fcb7/night-mode.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/14a5b801-3452-4033-8dc8-6e6fc057fcb7/night-mode.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/14a5b801-3452-4033-8dc8-6e6fc057fcb7/night-mode.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/14a5b801-3452-4033-8dc8-6e6fc057fcb7/night-mode.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/14a5b801-3452-4033-8dc8-6e6fc057fcb7/night-mode.jpg"
			sizes="100vw"
			alt="Framer X  dark (night) mode"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Framer X at night ()
		</figcaption>
	
</figure>


<p>You can switch the two from the <em>Window</em> menu.</p>

<h3>Protoype: Final Result</h3>

<p>Here are all my frames linked together:</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9b03a52b-eadd-4111-89e2-065ded1bb6b1/prototype-all-links.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9b03a52b-eadd-4111-89e2-065ded1bb6b1/prototype-all-links.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9b03a52b-eadd-4111-89e2-065ded1bb6b1/prototype-all-links.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9b03a52b-eadd-4111-89e2-065ded1bb6b1/prototype-all-links.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9b03a52b-eadd-4111-89e2-065ded1bb6b1/prototype-all-links.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9b03a52b-eadd-4111-89e2-065ded1bb6b1/prototype-all-links.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9b03a52b-eadd-4111-89e2-065ded1bb6b1/prototype-all-links.jpg"
			sizes="100vw"
			alt="All my frames linked together"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			All my frames linked together ()
		</figcaption>
	
</figure>


<p>And here’s the prototype in action:</p>

<figure class="video-container"><iframe data-src="https://player.vimeo.com/video/291486609" width="600" height="480" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe></figure>

<h3>What I Like About Framer X</h3>

<p>The application performs fast (though the beta choked a little with large project files) and <strong>it feels well designed</strong>. It’s a new tool, yet at the same time, it feels familiar. It also does give me that sense of it being a ‘design IDE’ and I think the Framer team is taking things in a very interesting direction.</p>

<p>Framer X makes mundane things like linking screens and scrolling fast and easy, as they should be. Though I hope to see even more of that type of thing in the future: <strong>prototyping is supposed to be a quick and dirty process</strong>, after all. To spend too many hours on a prototype is to miss the point of prototyping.</p>

<p>Having a Components Store is a great idea, and will certainly speed up my design process. <strong>I no longer have to spend time hunting down the plugins I need</strong>. I can imagine a couple of years from now there will be thousands of components with basically everything I need to put something relatively advanced together &mdash; relatively quickly. It may need some moderation in the future, though. I can see people uploading too many simple buttons, each a fork of the other, just because they can.</p>

<p>I like the focus on design systems through the components and the <em>Private Store</em> features. We all know, <strong>many teams struggle to collaborate meaningfully</strong> and tools like these are an immense help.</p>

<h3>What I’m Not Sure I Like About Framer X</h3>

<p>What worries me a little is that part of the “super easy playground for experimentation” experience of the original Framer tool is somewhat gone. The new features in X make it very easy to quickly prototype any “standard” feature or screen: you have all you need in the Store. But it is arguably <strong>more difficult to explore crazy and weird ideas for custom interactions</strong> &mdash; at least with this initial product release.</p>

<p>Learning React will be more intimidating to a lot of us, math and logic-impaired designers. For me personally, code reuse is not an option, since none of the projects I’m currently working on are built using web technologies. But even if it was an option, I’m thinking about programming in terms of it being a tool to express my design ideas. I’m not an engineer; <strong>using my code for anything but a prototype</strong> is not exactly a terrific idea.</p>

<p>Having said that, there’s <em>a lot</em> more documentation on JavaScript and React than on CoffeeScript. There’re also more people to help out, and the React community seems . I’m very curious to see how Framer X will help designers and engineers collaborate more &mdash; if at all.</p>

<h3>Framer X In My Toolset</h3>

<p>I’ll definitely be using Framer X in production, but I can’t see it completely replacing Sketch for me just yet. In my organization, each designer is allowed to use their favorite tool, as long as it integrates with , and Framer X doesn’t. Other things it lacks compared to Sketch (for now) are the pages, the crazy amount of plugins, and the more powerful drawing tools.</p>

<p>I will continue to use the original Framer for custom interactions &mdash; at least for the foreseeable future. When prototyping, things need to be done fast, and I also still have much to learn about React.</p>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(mb, ra, yk, il)</span>
</div>


              </article>
            </body>
          </html>
---------------
<h1 id="#title_1" >2、October Magic For Your Desktop (2018 Edition)</h1>
Cosima Mielke
[https://www.smashingmagazine.com/2018/09/desktop-wallpaper-calendars-october-2018/](https://www.smashingmagazine.com/2018/09/desktop-wallpaper-calendars-october-2018/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/09/desktop-wallpaper-calendars-october-2018/" />
              <title>October Magic For Your Desktop (2018 Edition)</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>October Magic For Your Desktop (2018 Edition)</h1>
                  
                    
                    <address>Cosima Mielke</address>
                  
                  <time datetime="2018-09-30T09:00:00&#43;02:00" class="op-published">2018-09-30T09:00:00+02:00</time>
                  <time datetime="2018-10-01T11:38:55&#43;00:00" class="op-modified">2018-10-01T11:38:55+00:00</time>
                </header>
                

<p>The leaves are shining in the most beautiful colors and pumpkins are taking over the front porches. Time to <strong>welcome the spookiest of all months</strong>: October! To get your desktop ready for fall and the upcoming Halloween season, artists and designers from across the globe once again challenged their creative skills and designed inspiring desktop wallpapers for you to indulge in.</p>

<p>As usual, the wallpapers come in versions with and without a calendar for <strong>October 2018</strong> and can be downloaded for free. And since so many inspiring, beautiful, and unique artworks evolve around our  every month, we once again dived into our archives to find some timeless October <strong>classics from past years</strong> to add to this collection. Because, well, some things are just too good to be forgotten, right? Enjoy!</p>

<p>Please note that: </p>

<ul>
<li>All <strong>images can be clicked on</strong> and lead to the preview of the wallpaper,</li>
<li>You can  by taking part in our Desktop Wallpaper Calendar series. We are regularly looking for creative designers and artists to be featured on Smashing Magazine. Are you one of them?</li>
</ul>

<h4><span class="rh">Further Reading</span> on SmashingMag:</h4>
<ul>
<li></li>
<li></li>
<li></li>
<li></li>
</ul>



  <aside class="product-panel product-panel__tilted product-panel--book" data-audience="non-subscriber" data-remove="true">
    <div class="container product-panel--book__container">
      <div class="panel__description panel__description--book">
        <p>Meet <strong>.</p>
        <a href="https://smashed.by/sb6panel">
          <button class="btn btn--green btn--large">
            Table of Contents&nbsp;&rarr;
          </button>
        </a>
      </div>
      <div class="panel__image panel__image--book">
        <a href="https://smashed.by/sb6panel" class="books__book__image">
        <div class="books__book__img">
          <img src="https://res.cloudinary.com/indysigner/image/upload/v1528877747/smashing-book-6-opt-wo-shadow_kbbopt.png">
        </div>
      </a>
      </div>
    </div>
  </aside>




<h3 id="shades-of-gold-10-2018">Shades Of Gold</h3>
<p>&#147;We are about to experience the magical imagery of nature, with all the yellows, ochers, oranges, and reds coming our way this fall. With all the subtle sunrises and the burning sunsets before us, we feel so joyful that we are going to shout it out to the world from the top of the mountains.&#148; &mdash; Designed by  from Serbia.</p>
<figure></figure>
<ul>
<li></li>
<li>with calendar: </li>
<li>without calendar: </li>
</ul>

<h3 id="flying-home-for-halloween-10-2018">Flying Home For Halloween</h3>
<p>&#147;You can only fully master the sky wearing an aviator hat and goggles. Like this little bat, flying home to celebrate Halloween with his family and friends.&#148; &mdash; Designed by  from the Netherlands.</p>
<figure></figure>
<ul>
<li></li>
<li>with calendar: </li>
<li>without calendar: </li>
</ul>

<h3 id="strange-october-journey-10-2018">Strange October Journey</h3>
<p>&#147;October makes the leaves fall to cover the land with lovely auburn colors and brings out all types of weird with them.&#148; &mdash; Designed by  from Serbia.</p>
<figure></figure>
<ul>
<li></li>
<li>with calendar: </li>
<li>without calendar: </li>
</ul>

<h3 id="ghostbusters-10-2018">Ghostbusters</h3>
<p>Designed by  from Sweden.</p>
<figure></figure>
<ul>
<li></li>
<li>with calendar: </li>
<li>without calendar: </li>
</ul>

<h3 id="trick-or-treat-10-2018">Trick Or Treat</h3>
<p>Designed by  from the USA.</p>
<figure></figure>
<ul>
<li></li>
<li>with calendar: </li>
<li>without calendar: </li>
</ul>

<h3 id="hello-fall-10-2018">Hello Fall</h3>
<p>&#147;Leaves are falling from the trees in all kinds of beautiful colors.&#148; &mdash; Designed by  from Belgium.</p>
<figure></figure>
<ul>
<li></li>
<li>with calendar: </li>
<li>without calendar: </li>
</ul>

<h3 id="halloween-candy-10-2018">Halloween Candy</h3>
<p>Designed by  from the Netherlands.</p>
<figure></figure>
<ul>
<li></li>
<li>with calendar: </li>
<li>without calendar: </li>
</ul>

<h3 id="the-pleasure-in-travelling-10-2018">The Pleasure In Travelling</h3>
<p>&#147;Travel makes you humble by letting you see the tiny place you occupy in the world. An individual with ordinary talent will always be ordinary, whether he or she travels or not; but a person with superior talent will go to pieces if they remain forever in the same place.&#148; &mdash; Designed by  from India.</p>
<figure></figure>
<ul>
<li></li>
<li>with calendar: </li>
<li>without calendar: </li>
</ul>

<h3 id="love-and-life-10-2018">Love And Life</h3>
<p>&#147;Mahatma Gandhi is remembered for all his great deeds and words of wisdom. Though he never lived his life peacefully, he always remained proactive in removing the social evils of our society. So let’s devote this month in the memory of this great man and recall all his good deeds as well as learning which he left behind for the world to follow.&#148; &mdash; Designed by  from India.</p>
<figure></figure>
<ul>
<li></li>
<li>with calendar: </li>
<li>without calendar: </li>
</ul>

<h3 id="that-new-car-smell-11-2018">That New Car Smell</h3>
<p>Designed by  from the United Kingdom.</p>
<figure></figure>
<ul>
<li></li>
<li>with calendar: </li>
<li>without calendar: </li>
</ul>

<h3 id="experience-the-magical-mirage-11-2018">Experience The Magical Mirage</h3>
<p>Designed by  from London.</p>
<figure></figure>
<ul>
<li></li>
<li>with calendar: </li>
<li>without calendar: </li>
</ul>

<h3 id="exclusively-fall-10-2018">Exclusively Fall</h3>
<p>&#147;When I think of October the real beginning of the fall season comes to mind. It was difficult to narrow down what symbols I wanted to use to represent the season and how to sort out which ones would work into a collective theme. I decided using textures and objects found in nature itself would make the most sense for my theme. By ‘carving’ symbols into the natural texture of wood and showing the change of season with the coloured leaves I hope I was able to capture the essence of fall.&#148; &mdash; Designed by  from Canada.</p>
<figure></figure>
<ul>
<li></li>
<li>with calendar: </li>
<li>without calendar: </li>
</ul>

<div class="sponsors__wide-place"></div>




<h3>Oldies But Goodies</h3>

<p>Creepy Halloween fellows, a nice cup of tea on a rainy day, and the magic of the fall forest — October has its very own charm. And, well, the treasures we rediscovered in our Wallpapers archives pay tribute to all those big and small October moments. Please note that these wallpapers <strong>don’t come with a calendar</strong>.</p>

<h4>Haunted House</h4>

<p>“Love all the Halloween costumes and decorations!” — Designed by  from Australia.</p>

<figure></figure>

<ul>
<li></li>
<li>without calendar: </li>
</ul>

<h4>A Very Pug-o-ween</h4>

<p>“The best part of October is undoubtedly Halloween. And the best part of Halloween is dog owners who never pass up an o-paw-tunity to dress up their pups as something a-dog-able. Why design pugs specifically in costumes? Because no matter how you look at it, pugs are cute in whatever costume you put them in for trick or treating. There’s something about their wrinkly snorting snoots that makes us giggle, and we hope our backgrounds make you smile all month. Happy Pug-o-ween from the punsters at Trillion!” — Designed by  from Summit, NJ.</p>

<figure></figure>

<ul>
<li></li>
<li>without calendar: </li>
</ul>

<h4 id="tea-and-cookies">Tea And Cookies</h4>

<p>“As it gets colder outside, all I want to do is stay inside with a big pot of tea, eat cookies and read or watch a movie, wrapped in a blanket. Is it just me?” — Designed by  from Romania.</p>

<figure></figure>

<ul>
<li></li>
<li>without calendar: </li>
</ul>

<h4 id="hello-autumn-i-m-glad-to-see-you-again">Hello, Autumn, I’m Glad to See You Again</h4>

<p>Designed by  from Hungary.</p>

<figure></figure>

<ul>
<li></li>
<li>without calendar: </li>
</ul>

<h4 id="omnomnomtober">Omnomnomtober</h4>

<p>“I’m just a sucker for Halloween, candy, tiny witches and giant kittens. And you can’t tell me that October is not Halloween, because I’ve waited the whole year for this. I thought that I would make illustration central to this calendar so I started with the idea of a tiny witch who’s stolen a ton of candy along with her cat — who’s gotten herself in trouble and can’t unstick the bubble gum from her giant teeth. A typical Halloween scene, right?” — Designed by  from Spain.</p>

<figure></figure>

<ul>
<li></li>
<li>without calendar: </li>
</ul>

<h4 id="dope-code">Dope Code</h4>

<p>“October is the month, when the weather in Poland starts to get colder, and it gets very rainy, too. You can&rsquo;t always spend your free time outside, so it&rsquo;s the perfect opportunity to get some hot coffee and work on your next cool web project!” — Designed by  from Poland.</p>

<figure></figure>

<ul>
<li></li>
<li>without calendar: </li>
</ul>

<h4 id="summer-don-t-go">Summer, Don&rsquo;t Go!</h4>

<p>“It would be nice if we could bring summer back, wouldn&rsquo;t it?” — Designed by  from Serbia.</p>

<figure></figure>

<ul>
<li></li>
<li>without calendar: </li>
</ul>

<h4 id="boodoni">Boodoni</h4>

<p>“This wallpaper was inspired by the creepy crawlies of Halloween, animation concept art, and hand-drawn type.” — Designed by  from the United States.</p>

<figure></figure>

<ul>
<li></li>
<li>without calendar: </li>
</ul>

<h4 id="my-spooky-love">My Spooky Love</h4>

<p>“Halloween can be a season of love too. This undead bunny is a combination of different inspiration from sugar skulls, cute characters and patterns that I have been drawing in my &ldquo;Year of Creative Habit&rdquo; project.” — Designed by  from Brunei.</p>

<figure></figure>

<ul>
<li></li>
<li>without calendar: </li>
</ul>

<h4 id="a-positive-fall">A Positive Fall</h4>

<p>“October is the month when fall truly begins, and many people feel tired and depressed in this season. The jumping fox wants you to be happy! Also, foxes always have reminded me of fall because of their beautiful fur colors.” — Designed by Elena Sanchez from Spain.</p>

<figure></figure>

<ul>
<li></li>
<li>without calendar: </li>
</ul>

<h4 id="autumn-in-the-forest">Autumn In The Forest</h4>

<p>“Autumn is a wonderful time to go for walks in the forest!” — Designed by  from Sweden.</p>

<figure></figure>

<ul>
<li></li>
<li>without calendar: </li>
</ul>

<h4 id="october-gifts">October Gifts</h4>

<p>“I was inspired by autumn and those gifts it presents to us in the form of beautiful colors, unusual shapes and mysterious weather. So enjoy October!” — Designed by  from Ukraine.</p>

<figure></figure>

<ul>
<li></li>
<li>without calendar: </li>
</ul>

<h4 id="autumn-is-the-new-spring">Autumn Is The New Spring</h4>

<p>&ldquo;Who says Autumn isn&rsquo;t fun? It&rsquo;s the new Spring, after all!&rdquo; Designed by  from the USA.</p>

<figure></figure>

<ul>
<li></li>
<li>without calendar: </li>
</ul>

<div class="sponsors__wide-place"></div>




<h4 id="watercolor-autumn">Watercolor Autumn</h4>

<p>&ldquo;There is nothing like being surrounded by beautiful, fiery, natural art for 2.5 months every year. This piece was inspired by the Falls I remember back in my New England hometown.&rdquo; Designed by Rachel Ladew from the USA.</p>

<figure></figure>

<ul>
<li></li>
<li>without calendar: </li>
</ul>

<h4 id="autumn-deer">Autumn Deer</h4>

<p>Designed by  from Canada.
<figure></figure></p>

<ul>
<li></li>
<li>without calendar: </li>
</ul>

<h4 id="roger-that-rogue-rover">Roger That Rogue Rover</h4>

<p>“The story is a mash-up of retro science fiction and zombie infection. What would happen if a Mars rover came into contact with an unknown Martian material and got infected with a virus? What if it reversed its intended purpose of research and exploration? Instead choosing a life of chaos and evil. What if they all ran rogue on Mars? Would humans ever dare to voyage to the red planet?” Designed by  from the USA.</p>

<figure></figure>

<ul>
<li></li>
<li>without calendar: </li>
</ul>

<h4 id="limbostyle">Limbostyle</h4>

<p>“This is my tribute to the awesome and beautifully designed videogame ‘Limbo’. Enjoy and share if you like this drawing.” Designed by Jonas Duri.</p>

<figure></figure>

<ul>
<li></li>
<li>without calendar: </li>
</ul>

<h4 id="spooky-town">Spooky Town</h4>
<p>Designed by  from Germany.</p>

<figure></figure>

<ul>
<li></li>
<li></li>
</ul>

<h4 id="halloween-cat">Halloween Cat</h4>

<p>Designed by Mohamad Khatib from Lebanon.</p>

<figure></figure>

<ul>
<li></li>
<li></li>
</ul>

<h4 id="skull-wallpaper">Crow</h4>

<p>Designed by Rumake Web Agency from Russia.</p>

<figure></figure>

<ul>
<li></li>
<li></li>
</ul>

<h4 id="ghostober">Ghostober</h4>

<p>Designed by  from México City.</p>
<figure></figure>

<ul>
<li></li>
<li></li>
</ul>

<h3>Join In Next Month!</h3>

<p>Please note that we respect and carefully consider the ideas and motivation behind each and every artist’s work. This is why we give all artists the <strong>full freedom to explore their creativity</strong> and express emotions and experience throughout their works. This is also why the themes of the wallpapers weren’t anyhow influenced by us, but rather designed from scratch by the artists themselves.</p>

<p>Thank you to all designers for their participation.  next month!</p>

              </article>
            </body>
          </html>
---------------
<h1 id="#title_2" >3、文章： DDD返工</h1>
Thomas Betts
[http://www.infoq.com/cn/articles/ddd-do-over?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/ddd-do-over?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/ddd-do-over/zh/smallimage/ddd-do-over-s-1536958878552-1537638167206.jpeg"/><p>Jimmy Bogard获得了一个少有的机会，做许多开发人员在完成一个艰难的项目之后希望做的事情——返工。他的团队参与了两个类似的项目，两个项目都使用了DDD。他探讨了从第一个项目中获得的经验教训，团队如何避免同样的陷阱并在稍后的项目中取得更大的成功。</p> <i>By Thomas Betts</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_3" >4、不畏：智能调度的核心是对业务数据的价值挖掘和有效利用</h1>
李夏昕
[http://www.infoq.com/cn/news/2018/10/alibaba-intelligent-dispatching?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/10/alibaba-intelligent-dispatching?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>InfoqQ有幸请到了阿里视频云运维专家不畏，来聊一聊在业务请求量高峰阶段，调度策略如何进行分配优化，调度系统有哪些智能化运维的思考和实践。</p> <i>By 李夏昕</i>
---------------
<h1 id="#title_4" >5、百度智能小程序月活破亿，正式开放申请</h1>
覃云
[http://www.infoq.com/cn/news/2018/10/Baidu-smart-program-open-apply?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/10/Baidu-smart-program-open-apply?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>9月25日，百度宣布智能小程序正式开放申请：即日起开发者只要通过搜索“百度智能小程序”或百度App语音搜索“智能小程序学院”就可以找到申请入口，申请成功便可以开发自己的智能小程序。</p> <i>By 覃云</i>
---------------