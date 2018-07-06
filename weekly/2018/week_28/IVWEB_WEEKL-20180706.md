## 文章索引
1、 <a href="#1what-is-redux:-a-designers-guide" >What Is Redux: A Designer’s Guide</a><br/>
2、 <a href="#2视频演讲-有赞在电商小程序上的技术积累与实践" >视频演讲： 有赞在电商小程序上的技术积累与实践</a><br/>
3、 <a href="#3miki-szikszai谈snapper如何培养技术人才" >Miki Szikszai谈Snapper如何培养技术人才</a><br/>
4、 <a href="#4云原生持续交付的模式和实践" >云原生持续交付的模式和实践</a><br/>
5、 <a href="#5区块链将如何重塑bpm" >区块链将如何重塑BPM</a><br/>
6、 <a href="#6pivotal发布spring-cloud-data-flow-15版本" >Pivotal发布Spring Cloud Data Flow 1.5版本</a><br/><h1 id="#title_0" >1、What Is Redux: A Designer’s Guide</h1>
Linton Ye
[https://www.smashingmagazine.com/2018/07/redux-designers-guide/](https://www.smashingmagazine.com/2018/07/redux-designers-guide/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/07/redux-designers-guide/" />
              <title>What Is Redux: A Designer’s Guide</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>What Is Redux: A Designer’s Guide</h1>
                  
                    
                    <address>Linton Ye</address>
                  
                  <time datetime="2018-07-05T15:30:46&#43;02:00" class="op-published">2018-07-05T15:30:46+02:00</time>
                  <time datetime="2018-07-05T18:35:54&#43;00:00" class="op-modified">2018-07-05T18:35:54+00:00</time>
                </header>
                

<p>Have you heard of Redux? What is it? No googling, please!</p>

<ul>
<li>“Fancy backend stuff.”</li>
<li>“I have heard of it, but I’m not aware of what it is. It’s a React framework perhaps?”</li>
<li>“A better way to store and manage states in a React application.”</li>
</ul>

<p>I’ve asked this question to over 40 designers. The above are their typical answers. Many of them are aware that Redux works with React and its job is “state management.”</p>

<p>But do you know what this “state management” really means? Do you know Redux’s real power is beyond managing the state? Do you know that <strong>Redux doesn’t necessarily require React to work</strong>? Do you want to join your team’s discussion (or at least lunch chats) about whether to use Redux? Do you want to design with an understanding of how Redux works in mind?</p>

<p>With the help of this article, <strong>I’d like to show you a full picture of Redux</strong>: what it can do, why it does its things, what the downsides are, when to use it, and how it relates to design.</p>

<p>My goal is to help designers like you. Even if you haven’t written a single line of code before, I think it’s still possible and beneficial (and fun) to understand Redux. Expect plain English and doodles &mdash; no code or abstract talks.</p>

<p>Ready for the ride?</p>



<aside class="product-panel product-panel__tilted product-panel--book" data-audience="non-subscriber">
    <div class="container product-panel--book__container">
      <div class="panel__description panel__description--book">
    <p>With so much happening on the web, what should we really pay attention to? At . Oct <span class="small-caps">23–24</span>.</p>
      <a href="http://smashed.by/confpanelspeakers" class="btn btn--green btn--large">
        Check the speakers&nbsp;→
      </a>
      </div>
      <div class="panel__image panel__image--book">
        <a href="http://smashed.by/confpanelspeakers" class="books__book__image">
        <div class="books__book__img">
          <img src="https://res.cloudinary.com/indysigner/image/upload/v1529498640/sarah-drasner-opt_kaxhos.png" alt="SmashingConf New York 2018, with Dan Mall, Sara Soueidan, Sarah Drasner and many others." width="310" height="400">
        </div>
      </a>
      </div>
    </div>
  </aside>




<h3 id="what-is-redux">What Is Redux?</h3>

<p>At a super-high level, Redux is a tool that developers use to make their lives easier. As many of you might have heard, its job is &ldquo;state management.&rdquo; I’ll explain what state management means a few sections later. At this point, I’ll leave you with this picture:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/abf88135-c431-43f2-b70d-720318ba2255/redux-state-manage-power.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/abf88135-c431-43f2-b70d-720318ba2255/redux-state-manage-power.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/abf88135-c431-43f2-b70d-720318ba2255/redux-state-manage-power.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/abf88135-c431-43f2-b70d-720318ba2255/redux-state-manage-power.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/abf88135-c431-43f2-b70d-720318ba2255/redux-state-manage-power.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/abf88135-c431-43f2-b70d-720318ba2255/redux-state-manage-power.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/abf88135-c431-43f2-b70d-720318ba2255/redux-state-manage-power.png"
			sizes="100vw"
			alt="Redux the state manager."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Redux manages state, but in the background, there are a few hidden powers. (Illustration by )
		</figcaption>
	
</figure>


<h3 id="why-should-you-care">Why Should You Care?</h3>

<p>Redux is more about the inner workings of an app than its look-and-feel. It’s a somewhat complex tool with a steep learning curve. Does that mean we, as designers, should stay far away from it?</p>

<p>No. I think we should embrace it. A car designer should understand what the engine is for, right? To successfully design app interfaces, <strong>designers should also have solid knowledge about things under the hood</strong>. We should learn about what it can do, understand why developers use it, and be aware of its advantages and implications.</p>

<blockquote>“Design is not just what it looks like and feels like. Design is how it works.”<br /><br />&mdash; Steve Jobs</blockquote>

<h3 id="what-can-redux-do">What Can Redux Do?</h3>

<p>Many people use Redux to manage the state in React apps. It’s the most common use case in the wild and Redux improves the aspects where React doesn’t do well (yet).</p>

<p>However, you’ll soon see that the real power of Redux goes way beyond that. Let’s get started by learning what state management really means.</p>

<h4 id="state-management">State Management</h4>

<p>If you are not sure what this “state” means, let’s replace it with a more generic term: “data.” <strong>State is data that change from time to time</strong>. State determines what’s displayed on the user interface.</p>

<p>What does state management mean? In general, there are three aspects of data that we’d need to manage in an app:</p>

<ol>
    <li></li>
    <li></li>
    <li></li>
</ol>

<p>Let’s say we are building a Dribbble shot page. What is the data we want to display on the page? They include the author’s profile photo, name, the animated GIF, the number of hearts, the comments, and so on.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f44a20de-4eef-4124-a6a1-19f9366eaf4a/redux-dribbble-page-data.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f44a20de-4eef-4124-a6a1-19f9366eaf4a/redux-dribbble-page-data.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f44a20de-4eef-4124-a6a1-19f9366eaf4a/redux-dribbble-page-data.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f44a20de-4eef-4124-a6a1-19f9366eaf4a/redux-dribbble-page-data.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f44a20de-4eef-4124-a6a1-19f9366eaf4a/redux-dribbble-page-data.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f44a20de-4eef-4124-a6a1-19f9366eaf4a/redux-dribbble-page-data.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f44a20de-4eef-4124-a6a1-19f9366eaf4a/redux-dribbble-page-data.png"
			sizes="100vw"
			alt="Data on a Dribbble shot page"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Data on a Dribbble shot page ()
		</figcaption>
	
</figure>


<p>First, we need to fetch all these data from a server in the cloud and put it somewhere. Next, we need to actually display the data. We need to assign pieces of this data to corresponding UI elements that represent what we actually see in the browser. For example, we assign the URL of the profile photo to the <code>src</code> attribute of an HTML <code>img</code> tag:</p>

<pre><code class="language-html">&lt;img src='https://url/to/profile_photo'&gt;
</code></pre>

<p>Finally, we need to handle changes to the data. For example, if a user adds a new comment to a Dribbble shot, or adds a star, we need to update the HTML accordingly.</p>

<p>Coordinating these three aspects of state is a big part in front-end development, and <strong>React has various degree of support</strong> for this task. Sometimes the built-in facility in React works well enough. But as the app grows more complex, its state may become harder to manage with React alone. That’s why many people start using Redux as an alternative.</p>

<h5 id="fetching-and-storing-data">Fetching And Storing Data</h5>

<p>In React, we break down a UI into components. Each of these components can be broken down into smaller components (see “”).</p>

<figure>)</figcaption></figure>

<p>If our UI is structured this way, when do we fetch the data and where to store it before populating the UI?</p>

<p><strong>Imagine there’s a chef living in each component</strong>. Fetching data from servers is like sourcing all the ingredients needed to prepare dishes.</p>

<p>A naive way is to fetch and store the data where and when it’s needed. This is like each chef going out to buy vegetables and meats directly from far-away farms.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1cbde4e9-cc6a-4eeb-9bea-04826fecd773/redux-each-chef-buy.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1cbde4e9-cc6a-4eeb-9bea-04826fecd773/redux-each-chef-buy.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1cbde4e9-cc6a-4eeb-9bea-04826fecd773/redux-each-chef-buy.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1cbde4e9-cc6a-4eeb-9bea-04826fecd773/redux-each-chef-buy.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1cbde4e9-cc6a-4eeb-9bea-04826fecd773/redux-each-chef-buy.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1cbde4e9-cc6a-4eeb-9bea-04826fecd773/redux-each-chef-buy.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1cbde4e9-cc6a-4eeb-9bea-04826fecd773/redux-each-chef-buy.png"
			sizes="100vw"
			alt="The naive way: fetch data from each component."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The naive way: fetch data from each component. (Illustration by )
		</figcaption>
	
</figure>


<p>This approach is wasteful. We’d need to call the server many times from many components &mdash; even for the same data. The chefs would waste a lot of gas and time traveling back and forth.</p>

<p>With Redux, we fetch data once and store it in a central place, conveniently called “store.” The data is then ready for use anytime by any component. This is not unlike having a superstore nearby where our chefs can buy all the ingredients. The superstore sends trucks to carry back vegetables and meats in bulk from farms. It’s a lot more efficient than asking individual chefs to go to the farms themselves!</p>

<p>The store also serves as the single source of truth. Components always retrieve data from the store, not from anywhere else. This keeps all the UI content consistent.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/03b718c6-e9c7-4ce7-8f02-c64dab1f3ea3/redux-redux-store.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/03b718c6-e9c7-4ce7-8f02-c64dab1f3ea3/redux-redux-store.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/03b718c6-e9c7-4ce7-8f02-c64dab1f3ea3/redux-redux-store.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/03b718c6-e9c7-4ce7-8f02-c64dab1f3ea3/redux-redux-store.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/03b718c6-e9c7-4ce7-8f02-c64dab1f3ea3/redux-redux-store.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/03b718c6-e9c7-4ce7-8f02-c64dab1f3ea3/redux-redux-store.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/03b718c6-e9c7-4ce7-8f02-c64dab1f3ea3/redux-redux-store.png"
			sizes="100vw"
			alt="Redux as a central store of data."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Redux as a central store of data. (Illustration by )
		</figcaption>
	
</figure>


<h5 id="assigning-data-to-ui-elements">Assigning Data To UI Elements</h5>

<p>With only React, there’s actually a better way to fetch and store data. We can ask our very kind chef Shotwell to do the shopping for all his chef friends. He would drive a truck to the farms and carry back the goodies. We could fetch data from a container component, for example, the &ldquo;Shot&rdquo; component in the Dribbble example, and use that as the single source of truth.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dd954175-93ce-4d28-adba-86c03d3fadc0/redux-driver-shotwell.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dd954175-93ce-4d28-adba-86c03d3fadc0/redux-driver-shotwell.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dd954175-93ce-4d28-adba-86c03d3fadc0/redux-driver-shotwell.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dd954175-93ce-4d28-adba-86c03d3fadc0/redux-driver-shotwell.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dd954175-93ce-4d28-adba-86c03d3fadc0/redux-driver-shotwell.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dd954175-93ce-4d28-adba-86c03d3fadc0/redux-driver-shotwell.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dd954175-93ce-4d28-adba-86c03d3fadc0/redux-driver-shotwell.png"
			sizes="100vw"
			alt="Fetch data from the root component."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Fetch data from the root component. (Illustration by )
		</figcaption>
	
</figure>


<p>This approach is more efficient than the naive way of fetching data from every component. But how does Shotwell pass the ingredients to other chefs? How to pass the data to the components that actually render HTML elements? We pass data from outer components to inner components like the baton in a relay, all the way until the data reach the destination.</p>

<p>For example, the URL of the author avatar needs to be passed from “Shot”, to “ShotDetail”, to “Title” and finally to the <code>&lt;img&gt;</code> tag. If our chefs live in an apartment, it really looks like this:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a4b8e9be-2a65-4099-b003-da559bf8318b/redux-floor-without-redux.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a4b8e9be-2a65-4099-b003-da559bf8318b/redux-floor-without-redux.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a4b8e9be-2a65-4099-b003-da559bf8318b/redux-floor-without-redux.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a4b8e9be-2a65-4099-b003-da559bf8318b/redux-floor-without-redux.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a4b8e9be-2a65-4099-b003-da559bf8318b/redux-floor-without-redux.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a4b8e9be-2a65-4099-b003-da559bf8318b/redux-floor-without-redux.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a4b8e9be-2a65-4099-b003-da559bf8318b/redux-floor-without-redux.png"
			sizes="100vw"
			alt="Pass data to components via props."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Pass data to components via props. (Illustration by )
		</figcaption>
	
</figure>


<p>To deliver data to the destination, we’d have to engage all the components on the path, even if they don’t need the data at all. It’d be really annoying if there are many floors!</p>

<p class="c-pre-sidenote--left">What if the superstore does door-to-door delivery?
With Redux<sup>1</sup>, we can plug in any data into any component, without affecting other components at all, like so:</p><p class="c-sidenote c-sidenote--right"><sup>1</sup> To be absolutely accurate, it’s another library called <code>react-redux</code> that hands data to React components, not Redux itself. But since react-redux just does the plumbing and people almost always use Redux and react-redux together, I think it’s fine to include this as one of the benefits of Redux.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a739f7a0-1349-4f6c-b2ba-274e0a7896b3/redux-floor-with-redux.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a739f7a0-1349-4f6c-b2ba-274e0a7896b3/redux-floor-with-redux.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a739f7a0-1349-4f6c-b2ba-274e0a7896b3/redux-floor-with-redux.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a739f7a0-1349-4f6c-b2ba-274e0a7896b3/redux-floor-with-redux.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a739f7a0-1349-4f6c-b2ba-274e0a7896b3/redux-floor-with-redux.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a739f7a0-1349-4f6c-b2ba-274e0a7896b3/redux-floor-with-redux.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a739f7a0-1349-4f6c-b2ba-274e0a7896b3/redux-floor-with-redux.png"
			sizes="100vw"
			alt="Plug data into components with Redux."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Plug data into components with Redux. (Illustration by )
		</figcaption>
	
</figure>


<p><strong>Note</strong>: <em>In the latest version of React (16.3), there’s a new “context” API that does almost the same job in terms of plugging data into components. So if this is the only reason your team is using Redux, seriously consider upgrading to React 16.3! Check out the  for more information (warning: lots of code ahead).</em></p>

<h5 id="changing-data">Changing Data</h5>

<p>Sometimes the logic of updating data in an app can be fairly complex. It might involve multiple steps that depend on one another. We may need to wait for the responses from multiple servers before updating the application state. We might need to update many places in the state at different times under different conditions.</p>

<p>It can be overwhelming if we don’t have a good structure for all this logic. The code would be difficult to understand and maintain.</p>

<p><strong>Redux allows us to divide and conquer</strong>. It provides a standard way to break data updating logic into small &ldquo;reducers&rdquo;. Those reducers work harmoniously together to complete a complex action.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7901f3b2-6048-4c8d-9599-e4ed33a8ef27/redux-from-spaghetti-to-reducer.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7901f3b2-6048-4c8d-9599-e4ed33a8ef27/redux-from-spaghetti-to-reducer.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7901f3b2-6048-4c8d-9599-e4ed33a8ef27/redux-from-spaghetti-to-reducer.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7901f3b2-6048-4c8d-9599-e4ed33a8ef27/redux-from-spaghetti-to-reducer.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7901f3b2-6048-4c8d-9599-e4ed33a8ef27/redux-from-spaghetti-to-reducer.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7901f3b2-6048-4c8d-9599-e4ed33a8ef27/redux-from-spaghetti-to-reducer.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7901f3b2-6048-4c8d-9599-e4ed33a8ef27/redux-from-spaghetti-to-reducer.png"
			sizes="100vw"
			alt="Divide complex logic into reducers."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Divide complex logic into reducers. (Illustration by )
		</figcaption>
	
</figure>


<p>Keep an eye on the recent development of React, though. As with the “context” API, there might be a new “setState” API in a future version of React. It’d make it easier to break up complex update logic into smaller parts. Once this new API becomes available, it’s possible that you won’t be needing Redux anymore to manage this aspect of state management.</p>

<div class="sponsors__wide-place"></div>




<h4 id="the-real-power-of-redux">The Real Power Of Redux</h4>

<p>So far, it seems Redux is just a band-aid for React. People use Redux to improve aspects that React doesn’t do well (yet). But React is catching up quickly! In fact, Dan Abramov, the creator of Redux, joined the React core team at Facebook a couple of years ago. They have been busy working on the aforementioned improvements to React: context API (released in 16.3), better data fetching API ( in Feb 2018), a better setState API and so on.</p>

<p>Will it make Redux obsolete?</p>

<p>Guess what? <strong>I haven’t shown you the real power of Redux yet!</strong></p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/317dc4b5-d0cf-4bdc-a9dd-3fe5f2efa723/redux-other-powers.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/317dc4b5-d0cf-4bdc-a9dd-3fe5f2efa723/redux-other-powers.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/317dc4b5-d0cf-4bdc-a9dd-3fe5f2efa723/redux-other-powers.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/317dc4b5-d0cf-4bdc-a9dd-3fe5f2efa723/redux-other-powers.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/317dc4b5-d0cf-4bdc-a9dd-3fe5f2efa723/redux-other-powers.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/317dc4b5-d0cf-4bdc-a9dd-3fe5f2efa723/redux-other-powers.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/317dc4b5-d0cf-4bdc-a9dd-3fe5f2efa723/redux-other-powers.png"
			sizes="100vw"
			alt="Redux power is way beyond state management."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Redux' power is way beyond state management. (Illustration by )
		</figcaption>
	
</figure>


<p>Redux forces developers to follow a few strict rules, which bring Redux a lot of power (yup, the power of discipline!):</p>

<ol>
<li>All the data (application state) has to be described in clear text. You should be able to write down all the data with a pen on paper.</li>
<li>Every action (change of data) has to be described in clear text. You must write down what you’ll do before changing anything. You can’t change data without leaving a mark. This process is called &ldquo;dispatching an action&rdquo; in Redux slang.</li>
<li>Your code that changes data must behave like a math formula. It must return the same result given the same input. The square of 4 is always 16 no matter how many times you run it.</li>
</ol>

<p class="c-pre-sidenote--left">When you follow these rules to build apps, magic happens. It enables a lot of cool features that are otherwise difficult or expensive to implement. Here are some examples.<sup>2</sup></p><p class="c-sidenote c-sidenote--right"><sup>2</sup> I collected these examples from Dan Abramov’s post “.”</p>

<h4 id="undo-redo">Undo, Redo</h4>

<p>The popular undo/redo feature requires system-level planning. Because undo/redo needs to record and replay every single change of data in the app, you must take it into account in the architecture from the very beginning. If it’s done as an afterthought, it’d require changing a lot of files which is a recipe for countless bugs.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/adbcb1c7-e32a-41cc-a0b4-b110af3ee017/redux-redo-undo.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/adbcb1c7-e32a-41cc-a0b4-b110af3ee017/redux-redo-undo.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/adbcb1c7-e32a-41cc-a0b4-b110af3ee017/redux-redo-undo.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/adbcb1c7-e32a-41cc-a0b4-b110af3ee017/redux-redo-undo.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/adbcb1c7-e32a-41cc-a0b4-b110af3ee017/redux-redo-undo.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/adbcb1c7-e32a-41cc-a0b4-b110af3ee017/redux-redo-undo.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/adbcb1c7-e32a-41cc-a0b4-b110af3ee017/redux-redo-undo.png"
			sizes="100vw"
			alt="Undo, redo."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Undo, redo. (Illustration by )
		</figcaption>
	
</figure>


<p>Because Redux requires every action to be described in clear text, the support for undo/redo almost comes for free. The instructions of how to implement undo/redo with Redux fit in a .</p>

<h4 id="collaborative-environment">Collaborative Environment</h4>

<p>If you are building an app similar to Google Docs where multiple users work together on a complex task, consider using Redux. It will likely do a lot of weightlifting for you.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8d4a626d-5f76-4634-b5e3-036dd5c3ddc1/redux-google-docs.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8d4a626d-5f76-4634-b5e3-036dd5c3ddc1/redux-google-docs.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8d4a626d-5f76-4634-b5e3-036dd5c3ddc1/redux-google-docs.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8d4a626d-5f76-4634-b5e3-036dd5c3ddc1/redux-google-docs.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8d4a626d-5f76-4634-b5e3-036dd5c3ddc1/redux-google-docs.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8d4a626d-5f76-4634-b5e3-036dd5c3ddc1/redux-google-docs.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8d4a626d-5f76-4634-b5e3-036dd5c3ddc1/redux-google-docs.png"
			sizes="100vw"
			alt="google docs"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Google Docs (Illustration by )
		</figcaption>
	
</figure>


<p>Redux makes it very easy to send what is happening over the network. It’s straightforward to receive actions another user performs on another machine, replay the changes and merge with what’s happening locally.</p>

<h4 id="optimistic-ui">Optimistic UI</h4>

<p>Optimistic UI is a way to improve the user experience of an app. It makes the app appear to respond faster over a slow network. It’s a popular strategy in apps that require real-time responses, for example, a first-person shooter game.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/49d3f673-1917-48cb-9b50-9f8150e62988/redux-optimisticui.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/49d3f673-1917-48cb-9b50-9f8150e62988/redux-optimisticui.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/49d3f673-1917-48cb-9b50-9f8150e62988/redux-optimisticui.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/49d3f673-1917-48cb-9b50-9f8150e62988/redux-optimisticui.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/49d3f673-1917-48cb-9b50-9f8150e62988/redux-optimisticui.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/49d3f673-1917-48cb-9b50-9f8150e62988/redux-optimisticui.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/49d3f673-1917-48cb-9b50-9f8150e62988/redux-optimisticui.png"
			sizes="100vw"
			alt="optimistic UI"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Optimistic UI (Illustration by )
		</figcaption>
	
</figure>


<p>As a simple example, in the Twitter app, when you click the heart on a tweet, it needs to request the server to do a few checkups, for example, whether that tweet still exists. Instead of waiting many seconds for the result, the app chooses to cheat! It assumes everything is OK and shows a filled heart right away.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2eab28ae-687b-41a4-bc75-2c137f1e6a0a/redux-twitter-heart.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2eab28ae-687b-41a4-bc75-2c137f1e6a0a/redux-twitter-heart.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2eab28ae-687b-41a4-bc75-2c137f1e6a0a/redux-twitter-heart.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2eab28ae-687b-41a4-bc75-2c137f1e6a0a/redux-twitter-heart.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2eab28ae-687b-41a4-bc75-2c137f1e6a0a/redux-twitter-heart.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2eab28ae-687b-41a4-bc75-2c137f1e6a0a/redux-twitter-heart.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2eab28ae-687b-41a4-bc75-2c137f1e6a0a/redux-twitter-heart.png"
			sizes="100vw"
			alt="Twitter heart"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Twitter heart (Illustration by )
		</figcaption>
	
</figure>


<p>This approach works because most of the time everything is OK. When things are not OK, the app will revert the previous UI updates and apply the actual result from the server, for example, show an error message.</p>

<p>Redux supports optimistic UI in the same fashion as what it does for undo and redo. It makes it easy to record, replay and revert changes of data when receiving a negative result from the server.</p>

<h4 id="persisting-and-booting-up-from-state">Persisting And Booting Up From State</h4>

<p>Redux makes it easy to save what’s happening in an app in the storage. Later on, even if the computer restarts, the app can load all the data and continue from exactly the same spot, as if it’s never been interrupted.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5b355529-4363-4ade-8ade-cb683f4129a1/redux-game-save-load.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5b355529-4363-4ade-8ade-cb683f4129a1/redux-game-save-load.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5b355529-4363-4ade-8ade-cb683f4129a1/redux-game-save-load.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5b355529-4363-4ade-8ade-cb683f4129a1/redux-game-save-load.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5b355529-4363-4ade-8ade-cb683f4129a1/redux-game-save-load.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5b355529-4363-4ade-8ade-cb683f4129a1/redux-game-save-load.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5b355529-4363-4ade-8ade-cb683f4129a1/redux-game-save-load.png"
			sizes="100vw"
			alt="Save/load game progress"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Save/load game progress (Illustration by )
		</figcaption>
	
</figure>


<p>If you build a game with Redux, you’d just need a couple more lines of code to save/load the game progress, without changing the rest of the code.</p>

<h4 id="really-extensible-systems">Really Extensible Systems</h4>

<p>With Redux, you must &ldquo;dispatch&rdquo; an action to update any data in an app. This restriction makes it possible to hook into almost every aspect of what’s happening in an app.</p>

<p>You can build really extensible apps where every function can be customized by the user. For example, check out , a terminal app built with Redux. The “hyperpower” extension adds sprinkles to the cursor and shakes up the window. How do you like this &ldquo;wow&rdquo; mode? (Perhaps not terribly useful but enough to impress users)</p>

<figure>)</figcaption></figure>

<h4 id="time-travel-debugging">Time-Travel Debugging</h4>

<p>How about being able to travel in time when debugging an app? You run the app, rewind or forward a few times to find the exact place when the bug occurs, fix the bug and re-play to confirm.</p>

<p>Redux makes this dream of developers come true.  allows you to manipulate the progress of a running app as a YouTube video &mdash; by dragging a slider!</p>

<p>How does it work? Remember the three strict rules that Redux enforces? That’s the secret sauce of the magic.</p>

<figure></figcaption></figure>

<h4 id="automated-bug-reports">Automated Bug Reports</h4>

<p>Imagine this: A user finds something wrong in your app and wants to report the bug. She painstakingly recalls and describes what she has done. A developer then tries to follow the steps manually to see if the bug occurs again. The bug report may be vague or inaccurate. The developer is having a hard time finding where the bug is.</p>

<p>Now, how about this. The user clicks the “Report bug” button. The system automatically sends what she has done to the developer. The developer clicks the “Replay bug” button and watches how that bug exactly happens. The bug is squashed on the spot, everybody is happy!</p>

<p>This is exactly what would happen if you use . How does it work? The Redux restrictions make wonders.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/85d8f237-d2b5-4230-a5af-cd9b0258ec5c/redux-bug-reports.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/85d8f237-d2b5-4230-a5af-cd9b0258ec5c/redux-bug-reports.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/85d8f237-d2b5-4230-a5af-cd9b0258ec5c/redux-bug-reports.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/85d8f237-d2b5-4230-a5af-cd9b0258ec5c/redux-bug-reports.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/85d8f237-d2b5-4230-a5af-cd9b0258ec5c/redux-bug-reports.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/85d8f237-d2b5-4230-a5af-cd9b0258ec5c/redux-bug-reports.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/85d8f237-d2b5-4230-a5af-cd9b0258ec5c/redux-bug-reports.png"
			sizes="100vw"
			alt="Automated bug reports"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Automated bug reports (Illustration by )
		</figcaption>
	
</figure>


<h3 id="downsides-of-redux">Downsides Of Redux</h3>

<p>The three major rules that Redux enforces are a double-edged sword. They enable powerful features, but at the same time cause inevitable downsides.</p>

<h4 id="steep-learning-curve">Steep Learning Curve</h4>

<p>Redux has a relatively steep learning curve. It takes time to understand, remember and get used to its patterns. It’s not recommended to learn Redux and React at the same time if they are both new to you.</p>

<h4 id="boilerplate-code">“Boilerplate” Code</h4>

<p>In many cases, using Redux means writing more code. It’s often required to touch multiple files to get a simple feature working. People have been complaining about the “boilerplate” code they’d have to write with Redux.</p>

<p>I know, this sounds contradictory. Didn’t I say <strong>Redux makes it possible to implement features with minimal code</strong>? This is a bit like using a dishwasher. First, you’d have to spend the time carefully arranging the dishes in rows. Not until then you will see the benefits of the dishwasher: saving time on actually cleaning the dishes, sanitizing the dishes etc. You have to decide whether the preparation time is worth it!</p>

<h4 id="performance-penalty">Performance Penalty</h4>

<p>Redux could also have an impact on performance due to the restrictions it enforces. It adds a little overhead whenever the data changes. In most cases, it’s not a big deal, and the slowdown is not noticeable. Still, when there’s a large amount of data in the store and when the data changes frequently (e.g. when the user is typing rapidly on a mobile device), the UI may become sluggish as a result.</p>

<h3 id="bonus-redux-is-not-just-for-react">Bonus: Redux Is Not Just For React</h3>

<p>A common misconception is that Redux is <em>for</em> React only. It sounds like Redux can’t do anything without React. Indeed, Redux complements React in a few important ways, as we have discussed earlier. It’s the most common use case.</p>

<p>However, in fact, Redux can work with any front-end frameworks, such as Angular, Ember.js or even jQuery, or even vanilla JavaScript. Try googling it, you’ll find . The general ideas of Redux apply anywhere!</p>

<p>As long as you use Redux wisely, you can get its benefits in many situations &mdash; not just in a React app.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/eee8e984-8bc6-4633-b514-e13862c40e47/redux-work-well-with-other.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/eee8e984-8bc6-4633-b514-e13862c40e47/redux-work-well-with-other.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/eee8e984-8bc6-4633-b514-e13862c40e47/redux-work-well-with-other.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/eee8e984-8bc6-4633-b514-e13862c40e47/redux-work-well-with-other.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/eee8e984-8bc6-4633-b514-e13862c40e47/redux-work-well-with-other.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/eee8e984-8bc6-4633-b514-e13862c40e47/redux-work-well-with-other.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/eee8e984-8bc6-4633-b514-e13862c40e47/redux-work-well-with-other.png"
			sizes="100vw"
			alt="Redux works well with other front-end libraries"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Redux works well with other front-end libraries. (Illustration by )
		</figcaption>
	
</figure>


<h3 id="conclusion">Conclusion</h3>

<p>As any tool, Redux offers a tradeoff. It enables powerful features but also has inevitable drawbacks. The job of a development team is to evaluate whether the tradeoff is worth it and make a conscious decision.</p>

<p>As designers, if we understand the advantages and downsides of Redux, we’ll be able to contribute to this decision making from the perspective of design. For example, perhaps we could design the UI to mitigate the potential performance impact? Perhaps we could advocate the inclusion of undo/redo features to remove a boatload of confirmation dialogs? Perhaps we could suggest optimistic UI since it improves user experience with a relatively low cost?</p>

<p>Understand the benefits and limitations of a technology, and design accordingly. I think that’s what Steve Jobs meant by “design is how it works.”</p>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(rb, ra, il)</span>
</div>


              </article>
            </body>
          </html>
---------------
<h1 id="#title_1" >2、视频演讲： 有赞在电商小程序上的技术积累与实践</h1>
施德来
[http://www.infoq.com/cn/presentations/technology-accumulation-and-practice-of-youzan?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/technology-accumulation-and-practice-of-youzan?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/presentations/technology-accumulation-and-practice-of-youzan/zh/mediumimage/shidelai270-1530460846807.jpg"/><p>黎贝卡小程序店铺“首次上新7分钟破百万”、“二次上新59秒破百万”，这些傲人的成绩背后离不开技术团队的幕后支持，沙龙现场会主要介绍有赞在小程序技术上的积累，如小程序组件库的开源、在微页面里如何将H5与小程序合二为一等，并分享有赞在小程序开发过程中遇到的一些问题，以及如何利用官方解决方案进行最优处理。</p> <i>By 施德来</i>
---------------
<h1 id="#title_2" >3、Miki Szikszai谈Snapper如何培养技术人才</h1>
Shane Hastie
[http://www.infoq.com/cn/news/2018/07/snapper-technical-graduates?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/snapper-technical-graduates?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>在JAFAC大会上，Snapper首席执行官Miki Szikszai谈论了该公司如何克服在技能短缺的环境中培养技术团队的一些挑战。 他们聘用毕业生团队，并让他们从事面对真实客户的工作，而不是将他们安插到现有团队中，这样可以产生更好的结果并实现快速增长。</p> <i>By Shane Hastie</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_3" >4、云原生持续交付的模式和实践</h1>
Manuel Pais
[http://www.infoq.com/cn/news/2018/07/cloud-native-continuous-delivery?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/cloud-native-continuous-delivery?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>RIO（大众汽车公司的一个品牌）首席架构师Christian Deger最近在伦敦Continuous Lifecycle大会上分享了一系列实现云原生持续交付的模式和实践。</p> <i>By Manuel Pais</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_4" >5、区块链将如何重塑BPM</h1>
Kent Weare
[http://www.infoq.com/cn/news/2018/07/blockchain-BPM?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/blockchain-BPM?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>在最近的一篇Hyperledger博文中，MonetaGo首席执行官Jesse Chenard讨论了区块链如何准备重塑传统业务流程管理平台（BPM）。当前的BPM平台面临的一个挑战是数据通常存储在孤岛中，而相应的交易中心也存在挑战。区块链解决方案可跨越边界提供审计，而不会将敏感信息泄露给其他方。</p> <i>By Kent Weare</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_5" >6、Pivotal发布Spring Cloud Data Flow 1.5版本</h1>
Michael Redlich
[http://www.infoq.com/cn/news/2018/07/pivotal-releases-data-flow-1.5?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/pivotal-releases-data-flow-1.5?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Pivotal发布了Spring Cloud Data Flow 1.5版本，这是一款用于构建实时数据服务的项目。新功能包括对用户界面、指标和Kubernetes的改进，以及更新的Spring Cloud Stream应用启动器。</p> <i>By Michael Redlich</i> <i> Translated by 刘嘉洋</i>
---------------