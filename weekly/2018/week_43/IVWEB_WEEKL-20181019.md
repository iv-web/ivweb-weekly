## 文章索引
1、 <a href="#1javascript私有属性要来了但实现方式惹争议" >JavaScript私有属性要来了，但实现方式惹争议</a><br/>
2、 <a href="#2reasons-your-mobile-app-retention-rate-might-be-so-low" >Reasons Your Mobile App Retention Rate Might Be So Low</a><br/>
3、 <a href="#3文章-codefirstui设计的未来" >文章： CodeFirst：UI设计的未来</a><br/>
4、 <a href="#4文章-大数据凉了不流式计算浪潮才刚刚开始" >文章： 大数据凉了？不，流式计算浪潮才刚刚开始</a><br/>
5、 <a href="#5文章-gartner分析师认为区块链幻灭是too-young-too-naive" >文章： Gartner分析师：认为区块链幻灭是too young too naive！</a><br/>
6、 <a href="#6flexbox-布局的最简单表单" >Flexbox 布局的最简单表单</a><br/>
7、 <a href="#7文章-联盟链战国五大巨头横向对比" >文章： 联盟链战国：五大巨头横向对比</a><br/>
8、 <a href="#8cloudflare-workers支持webassembly和键值存储" >Cloudflare Workers支持WebAssembly和键值存储</a><br/>
9、 <a href="#9amazon全新轻量级服务器端swift框架smoke" >Amazon全新轻量级服务器端Swift框架：Smoke</a><br/>
10、 <a href="#10google-cloud-spanner和cloud-bigtable最新更新" >Google Cloud Spanner和Cloud Bigtable最新更新</a><br/>
11、 <a href="#11文章-polylith一款新的软件架构" >文章： Polylith：一款新的软件架构</a><br/><h1 id="#title_0" >1、JavaScript私有属性要来了，但实现方式惹争议</h1>
徐川
[http://www.infoq.com/cn/news/2018/10/js-private-attribute-implement?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/10/js-private-attribute-implement?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>昨天我们介绍了JavaScript的三个新特性，现在，一个广受期待的新特性：私有属性也离我们越来越近了。

昨天，TC39在GitHub上通过了一条EMCAScript语法特性的草案，即类私有属性修饰符“#”，不过，该特性之前在社区的调研中遭遇了大量反对。</p> <i>By 徐川</i>
---------------
<h1 id="#title_1" >2、Reasons Your Mobile App Retention Rate Might Be So Low</h1>
Suzanne Scacca
[https://www.smashingmagazine.com/2018/10/mobile-app-retention-rate/](https://www.smashingmagazine.com/2018/10/mobile-app-retention-rate/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/10/mobile-app-retention-rate/" />
              <title>Reasons Your Mobile App Retention Rate Might Be So Low</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>Reasons Your Mobile App Retention Rate Might Be So Low</h1>
                  
                    
                    <address>Suzanne Scacca</address>
                  
                  <time datetime="2018-10-18T14:00:01&#43;02:00" class="op-published">2018-10-18T14:00:01+02:00</time>
                  <time datetime="2018-10-18T15:22:02&#43;00:00" class="op-modified">2018-10-18T15:22:02+00:00</time>
                </header>
                <p>In business, there’s a lot of talk about generating customer loyalty and retaining the business of good customers. Mobile apps aren’t all that different when you think about it.</p>

<p>While the number of installs may signal that an app is popular with users initially, it doesn’t tell the whole story. In order for an app to be successful, it must have loyal subscribers that make use of the app as it was intended. Which is where the retention rate enters the picture.</p>

<p>In this article, I want to explore what a good retention rate looks like for mobile apps. I’ll dig into the more common reasons why mobile apps have low retention rates and how those issues can be fixed.</p>

<p>Let’s start with the basics.</p>

<h3>Checking The Facts: What Is A Good Mobile App Retention Rate?</h3>

<p>A retention rate is the percentage of users that remain active on your mobile app after a certain period of time. It doesn’t necessarily pertain to how many people have uninstalled the app either. A sustained lack of activity is generally accepted as a sign that a user has lost interest in an app.</p>

<p>To calculate a good retention rate for your mobile app, be sure to take into account the frequency of logins you expect users to make. Some apps realistically should see daily logins, especially for gaming, dating, and social networking. Others, though, may only need weekly logins, like for ride-sharing apps, Google Authenticator or local business apps.</p>

<p>When calculating the retention rate for anticipated daily usage, you should run the calculation for at least a week, if not more. For weekly or monthly usage, adjust your calculation accordingly.</p>

<p><strong>Recommended reading</strong>: <em></em></p>



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




<p>For daily usage, divide the following like so:</p>

<table class="tablesaw break-out" data-tablesaw-mode="swipe" data-tablesaw-minimap>
  <thead>
    <tr>
      <th data-tablesaw-priority="persist">Users Logged into the App on Day 0</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Users Logged into the App on Day 1</td>
    </tr>
    <tr>
      <td>Users Logged into the App on Day 2</td>
    </tr>
    <tr>
      <td>Users Logged into the App on Day 3</td>
    </tr>
    <tr>
      <td>Users Logged into the App on Day 4</td>
    </tr>
    <tr>
      <td>Users Logged into the App on Day 5</td>
    </tr>
    <tr>
      <td>Users Logged into the App on Day 6</td>
    </tr>
    <tr>
      <td>Users Logged into the App on Day 7</td>
    </tr>
  </tbody>
</table>

<p>This will give you a curve that demonstrates how well your mobile app is able to sustain users. Here is an example of how you would calculate this:</p>

<table class="tablesaw break-out" data-tablesaw-mode="swipe" data-tablesaw-minimap>
  <thead>
    <tr>
      <th data-tablesaw-priority="persist">Number of New Users Acquired</th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Day 0</td>
      <td>100</td>
    </tr>
    <tr>
      <td>Day 1</td>
      <td>91 (91% )</td>
    </tr>
    <tr>
      <td>Day 2</td>
      <td>85 (85%)</td>
    </tr>
    <tr>
      <td>Day 3</td>
      <td>70 (70%)</td>
    </tr>
    <tr>
      <td>Day 4</td>
      <td>60 (60%)</td>
    </tr>
    <tr>
      <td>Day 5</td>
      <td>49 (49%)</td>
    </tr>
    <tr>
      <td>Day 6</td>
      <td>32 (32%)</td>
    </tr>
    <tr>
      <td>Day 7</td>
      <td>31 (31%)</td>
    </tr>
  </tbody>
</table>

<p>If you can, add the data into a line graph format. It’ll be much easier to spot trends in downward momentum or plateauing:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b7e6a332-4ab5-453c-8f2f-a1f8834eaef3/retention-rate-example.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b7e6a332-4ab5-453c-8f2f-a1f8834eaef3/retention-rate-example.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b7e6a332-4ab5-453c-8f2f-a1f8834eaef3/retention-rate-example.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b7e6a332-4ab5-453c-8f2f-a1f8834eaef3/retention-rate-example.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b7e6a332-4ab5-453c-8f2f-a1f8834eaef3/retention-rate-example.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b7e6a332-4ab5-453c-8f2f-a1f8834eaef3/retention-rate-example.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b7e6a332-4ab5-453c-8f2f-a1f8834eaef3/retention-rate-example.png"
			sizes="100vw"
			alt="example retention rate"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			An example of how to calculate and chart your app’s retention rate (Image source: )
		</figcaption>
	
</figure>


<p>This is just a basic example of how a retention rate calculation works. Curious to see what the average (Android) mobile app’s retention curve looks like?</p>

<p> (with Andrew Chen) charted the following:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/950eac2b-71d2-48e2-930a-942abe28ace7/quettra-retention-curve.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/950eac2b-71d2-48e2-930a-942abe28ace7/quettra-retention-curve.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/950eac2b-71d2-48e2-930a-942abe28ace7/quettra-retention-curve.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/950eac2b-71d2-48e2-930a-942abe28ace7/quettra-retention-curve.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/950eac2b-71d2-48e2-930a-942abe28ace7/quettra-retention-curve.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/950eac2b-71d2-48e2-930a-942abe28ace7/quettra-retention-curve.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/950eac2b-71d2-48e2-930a-942abe28ace7/quettra-retention-curve.png"
			sizes="100vw"
			alt="average Android app retention rate"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Average retention rates for Android apps (Image source: )
		</figcaption>
	
</figure>


<p>According to this data, <strong>the average app loses 77% of users within just three days</strong>. By the time the first-month wraps, 90% of those original new users are gone.</p>

<p> shows that the average cost per installation of a mobile app (globally) breaks down to the following:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6cada8df-8456-4501-84eb-2a2cc53a04a1/cost-per-install.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6cada8df-8456-4501-84eb-2a2cc53a04a1/cost-per-install.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6cada8df-8456-4501-84eb-2a2cc53a04a1/cost-per-install.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6cada8df-8456-4501-84eb-2a2cc53a04a1/cost-per-install.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6cada8df-8456-4501-84eb-2a2cc53a04a1/cost-per-install.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6cada8df-8456-4501-84eb-2a2cc53a04a1/cost-per-install.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6cada8df-8456-4501-84eb-2a2cc53a04a1/cost-per-install.png"
			sizes="100vw"
			alt="average cost per app install"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Average cost of each mobile app installation (Image source: )
		</figcaption>
	
</figure>


<p>Basically, this is the average cost to build and market an app &mdash; a number you should aim to recuperate per user once the app has been installed. However, if your app loses about 90% of its users within a month’s time, think about what the loss actually translates to for your business.</p>

<p>Ankit Jain of Gradient Ventures summarized the key lesson to take away from these findings:</p>

<blockquote>“Users try out a lot of apps but decide which ones they want to ‘stop using’ within the first 3-7 days. For ‘decent’ apps, the majority of users retained for 7 days stick around much longer. The key to success is to get the users hooked during that critical first 3-7 day period.”</blockquote>

<p>As you can see from the charting of the top Android apps, Jain’s argument holds water:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/70efdcac-49db-4188-8473-d638d94b8dc9/01-reasons-your-mobile-app-retention-rate-might-be-so-low.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/70efdcac-49db-4188-8473-d638d94b8dc9/01-reasons-your-mobile-app-retention-rate-might-be-so-low.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/70efdcac-49db-4188-8473-d638d94b8dc9/01-reasons-your-mobile-app-retention-rate-might-be-so-low.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/70efdcac-49db-4188-8473-d638d94b8dc9/01-reasons-your-mobile-app-retention-rate-might-be-so-low.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/70efdcac-49db-4188-8473-d638d94b8dc9/01-reasons-your-mobile-app-retention-rate-might-be-so-low.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/70efdcac-49db-4188-8473-d638d94b8dc9/01-reasons-your-mobile-app-retention-rate-might-be-so-low.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/70efdcac-49db-4188-8473-d638d94b8dc9/01-reasons-your-mobile-app-retention-rate-might-be-so-low.png"
			sizes="100vw"
			alt="average retention rate for top Android apps"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Average retention rates for top Android apps (Image source: )
		</figcaption>
	
</figure>


<p>Top Android apps still see a sharp decline in active users after about three days, but then the numbers plateau. They also don’t bleed as many new users upfront, which allows them to sustain a larger percentage of users.</p>

<p>This is exactly what you should be aiming for.</p>

<h3>A Retention Recovery Guide For Mobile Apps</h3>

<p>So, we know what makes for a good and bad retention rate. We also understand that it’s not about how many people have uninstalled or deleted the app from their devices. Letting an app sit in isolation, untouched on a mobile device, is just as bad.</p>

<p>As you can imagine, increasing your retention rate will lead to other big wins for your mobile app:</p>

<ul>
<li>More engagement</li>
<li>More <em>meaningful</em> engagement</li>
<li>Greater loyalty</li>
<li>Increased conversions (if your app is monetized, that is)</li>
</ul>

<p>Now you need to ask yourself:</p>

<blockquote>“When are users dropping off? And why?”</blockquote>

<p>You can draw your own hypotheses about this based on the retention rate alone, though it might be helpful to make use of tools like heat maps to spot problem areas in the mobile app. Once you know what’s going on, you can take action to remove the friction from the user experience.</p>

<p>To get you started, I’ve included a number of issues that commonly plague mobile apps with low retention rates. If your app is guilty of any of these, get to work on fixing the design or functionality ASAP!</p>

<div class="sponsors__wide-place"></div>




<h4>1. Difficult Onboarding</h4>

<p>Aside from the app store description and screenshots users encounter, onboarding is the first real experience they have with a mobile app. As you can imagine, a frustrating sign-in or onboarding procedure could easily turn off those who take that as a signal the rest of the app will be as difficult to use.</p>

<p>Let’s use the  dating app as an example. The initial splash screen looks great and is well-designed. It has a clear value proposition, and an easy-to-find call-to-action:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/85f3f915-4f21-4196-ba3a-69fa7b73d48c/okcupid-step1.PNG">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/85f3f915-4f21-4196-ba3a-69fa7b73d48c/okcupid-step1.PNG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/85f3f915-4f21-4196-ba3a-69fa7b73d48c/okcupid-step1.PNG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/85f3f915-4f21-4196-ba3a-69fa7b73d48c/okcupid-step1.PNG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/85f3f915-4f21-4196-ba3a-69fa7b73d48c/okcupid-step1.PNG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/85f3f915-4f21-4196-ba3a-69fa7b73d48c/okcupid-step1.PNG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/85f3f915-4f21-4196-ba3a-69fa7b73d48c/okcupid-step1.PNG"
			sizes="70vw"
			alt="Splash screen for OkCupid app"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The first screen new OkCupid users encounter (Image source: )
		</figcaption>
	
</figure>


<p>On the next page, users are given two options for joining the app. It’s free to use, but still requires users to create an account:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/43e13bfb-cd93-4404-b7fa-f65ad97e8b2d/okcupid-step2.PNG">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/43e13bfb-cd93-4404-b7fa-f65ad97e8b2d/okcupid-step2.PNG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/43e13bfb-cd93-4404-b7fa-f65ad97e8b2d/okcupid-step2.PNG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/43e13bfb-cd93-4404-b7fa-f65ad97e8b2d/okcupid-step2.PNG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/43e13bfb-cd93-4404-b7fa-f65ad97e8b2d/okcupid-step2.PNG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/43e13bfb-cd93-4404-b7fa-f65ad97e8b2d/okcupid-step2.PNG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/43e13bfb-cd93-4404-b7fa-f65ad97e8b2d/okcupid-step2.PNG"
			sizes="70vw"
			alt="OkCupid account creation"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Account creation for OkCupid gives two options (Image source: )
		</figcaption>
	
</figure>


<p>The first option is a Facebook sign-in. The other is to use a personal email address. Since Facebook logins can streamline not just signup, but the setup of dating mobile apps (since users can automatically import details, photos, and connections), this option is probably one many users’ choose.</p>

<p>But there’s a problem with it: After seven clicks to connect to Facebook and confirm one’s identity, here is what the user sees (or, at least, this is what I encountered the last couple of times I tried):</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b9770cf7-0746-480a-a75b-4f330e52c776/okcupid-step7.PNG">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b9770cf7-0746-480a-a75b-4f330e52c776/okcupid-step7.PNG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b9770cf7-0746-480a-a75b-4f330e52c776/okcupid-step7.PNG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b9770cf7-0746-480a-a75b-4f330e52c776/okcupid-step7.PNG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b9770cf7-0746-480a-a75b-4f330e52c776/okcupid-step7.PNG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b9770cf7-0746-480a-a75b-4f330e52c776/okcupid-step7.PNG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b9770cf7-0746-480a-a75b-4f330e52c776/okcupid-step7.PNG"
			sizes="70vw"
			alt="Signup error with OkCupid"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			After connecting to Facebook, users still encounter an error signing in. (Image source: )
		</figcaption>
	
</figure>


<p>One of the main reasons why users choose a Facebook sign-in is because of how quick and easy it’s supposed to be. In these attempts of mine, however, my OkCupid app wouldn’t connect to Facebook. So, after 14 total clicks (7 for each time I tried to sign up), I ended up having to provide an email anyway.</p>

<p>This is obviously not a great first impression OkCupid has left on me (or any of its users). What makes it worse is that we know there’s a lot more work to get onboarded with the app. Unlike competitors like Bumble that have greatly simplified signup, OkCupid forces users into a buggy onboarding experience as well as a more lengthy profile configuration.</p>

<p>Needless to say, this is probably a bit too much for some users.</p>

<div class="sponsors__wide-place"></div>




<h4>2. Slow or Sloppy Navigation</h4>

<p>Here’s another example of a time-waster for mobile app users.</p>

<p>Let’s say getting inside the new app is easy. There’s no real onboarding required. Maybe you just ask if it’s okay to use their location for personalization purposes or if you can send push notifications. Otherwise, users are able to start using the app right away.</p>

<p>That’s great &mdash; until they realize how clunky the experience is.</p>

<p>To start, navigation of a mobile app should be easy and ever-present. It’s not like a browser window where users can hit that “Back” button in order to get out of an unwanted page. On a mobile app, they need a clear and intuitive exit strategy. Also, <strong>navigation of an app should never take more than two or three steps to get to a desired outcome</strong>.</p>

<p>One example of this comes from . Specifically, I want to look at the “Offers” user journey:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9ea36b28-a3c2-45c0-a44a-509444fccf92/wendys-offer1.PNG">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9ea36b28-a3c2-45c0-a44a-509444fccf92/wendys-offer1.PNG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9ea36b28-a3c2-45c0-a44a-509444fccf92/wendys-offer1.PNG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9ea36b28-a3c2-45c0-a44a-509444fccf92/wendys-offer1.PNG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9ea36b28-a3c2-45c0-a44a-509444fccf92/wendys-offer1.PNG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9ea36b28-a3c2-45c0-a44a-509444fccf92/wendys-offer1.PNG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9ea36b28-a3c2-45c0-a44a-509444fccf92/wendys-offer1.PNG"
			sizes="70vw"
			alt="Offers from Wendy’s app"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The home page of the Wendy’s app promises “Offers” (Image source: )
		</figcaption>
	
</figure>


<p>As you can see, the navigation at the bottom of the app is as clear as day. Users have three areas of the app they can explore &mdash; each of which makes sense for a business like Wendy’s. There are three additional navigation options in the top-right corner of the app, too.</p>

<p>When “Offers” is clicked, users are taken to a sort of full-screen pop-up containing all current special deals:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3ec6cbd7-0e18-4461-9d61-9a7b23fedc3a/wendys-offer2.PNG">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3ec6cbd7-0e18-4461-9d61-9a7b23fedc3a/wendys-offer2.PNG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3ec6cbd7-0e18-4461-9d61-9a7b23fedc3a/wendys-offer2.PNG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3ec6cbd7-0e18-4461-9d61-9a7b23fedc3a/wendys-offer2.PNG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3ec6cbd7-0e18-4461-9d61-9a7b23fedc3a/wendys-offer2.PNG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3ec6cbd7-0e18-4461-9d61-9a7b23fedc3a/wendys-offer2.PNG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3ec6cbd7-0e18-4461-9d61-9a7b23fedc3a/wendys-offer2.PNG"
			sizes="70vw"
			alt="Wendy’s Offers pop-up"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The Wendy’s Offers pop-up screen (Image source: )
		</figcaption>
	
</figure>


<p>As you can see, the navigation is no longer there. The “X” for the Offers pop-up also sits in the top-left corner (instead of the right, which is the more intuitive choice). This is already a problem. It also persists throughout the entire Offers redemption experience.</p>

<p>Let’s say that users aren’t turned off by the poor navigational choices and still want to redeem one of these offers. This is what they encounter next:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2e9ca650-d149-4602-a0f9-5211ebbb660e/wendys-offer3.PNG">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2e9ca650-d149-4602-a0f9-5211ebbb660e/wendys-offer3.PNG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2e9ca650-d149-4602-a0f9-5211ebbb660e/wendys-offer3.PNG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2e9ca650-d149-4602-a0f9-5211ebbb660e/wendys-offer3.PNG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2e9ca650-d149-4602-a0f9-5211ebbb660e/wendys-offer3.PNG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2e9ca650-d149-4602-a0f9-5211ebbb660e/wendys-offer3.PNG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2e9ca650-d149-4602-a0f9-5211ebbb660e/wendys-offer3.PNG"
			sizes="70vw"
			alt="Wendy’s in-restaurant offers"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Wendy’s Offers can be used at the restaurant. (Image source: )
		</figcaption>
	
</figure>


<p>Now, this is pretty cool. Users can redeem the offer at that very moment while they’re in a Wendy’s or they can place the order through the app and pick it up. Either way, this is a great way to integrate the mobile app and in-store experiences.</p>

<p>Except…</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bc7002f5-d494-4fdd-8f28-333d1fd9d2e6/wendys-offer4.PNG">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bc7002f5-d494-4fdd-8f28-333d1fd9d2e6/wendys-offer4.PNG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bc7002f5-d494-4fdd-8f28-333d1fd9d2e6/wendys-offer4.PNG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bc7002f5-d494-4fdd-8f28-333d1fd9d2e6/wendys-offer4.PNG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bc7002f5-d494-4fdd-8f28-333d1fd9d2e6/wendys-offer4.PNG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bc7002f5-d494-4fdd-8f28-333d1fd9d2e6/wendys-offer4.PNG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bc7002f5-d494-4fdd-8f28-333d1fd9d2e6/wendys-offer4.PNG"
			sizes="70vw"
			alt="Wendy’s offer code"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The Wendy’s offer code takes a while to populate. (Image source: )
		</figcaption>
	
</figure>


<p>Imagine standing in line at a Wendy’s or going through a drive-thru that isn’t particularly busy. That image above is not one you’d want to see.</p>

<p>They call it “fast food” for a reason and if your app isn’t working or it takes just a few seconds too long to load the offer code, imagine what that will do for everyone else’s experience at Wendy’s. The cashiers will be annoyed that they’ve held up the flow of traffic and everyone waiting in line will be frustrated in having to wait longer.</p>

<p>While mobile apps generally are designed to cater to the single user experience, you do have to consider how something like this could affect the experience of others.</p>

<p><strong>Recommended reading</strong>: <em></em></p>

<h4>3. Overwhelming Navigation</h4>

<p>A poorly constructed or non-visible navigation is one thing. But a navigation that gives way too many options can be just as problematic. While a mega menu on something like an e-commerce website certainly makes sense, an oversized menu in mobile apps doesn’t.</p>

<p>It pains me to do this since I love the , but its news app is guilty of this crime:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d497d98a-526e-4b5b-817f-da5cf1efd875/bbc-navigation1.PNG">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d497d98a-526e-4b5b-817f-da5cf1efd875/bbc-navigation1.PNG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d497d98a-526e-4b5b-817f-da5cf1efd875/bbc-navigation1.PNG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d497d98a-526e-4b5b-817f-da5cf1efd875/bbc-navigation1.PNG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d497d98a-526e-4b5b-817f-da5cf1efd875/bbc-navigation1.PNG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d497d98a-526e-4b5b-817f-da5cf1efd875/bbc-navigation1.PNG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d497d98a-526e-4b5b-817f-da5cf1efd875/bbc-navigation1.PNG"
			sizes="70vw"
			alt="BBC News navigation"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The top of the BBC News navigation (Image source: )
		</figcaption>
	
</figure>


<p>This looks like a standard news navigation at first glance. Top (popular) stories sit at the top; my News (customized) stories below it. But then it appears there’s more, so users are apt to scroll downwards and see what others options there are:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9a02fe54-66f0-4fce-bf7d-16fad4099abf/bbc-navigation2.PNG">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9a02fe54-66f0-4fce-bf7d-16fad4099abf/bbc-navigation2.PNG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9a02fe54-66f0-4fce-bf7d-16fad4099abf/bbc-navigation2.PNG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9a02fe54-66f0-4fce-bf7d-16fad4099abf/bbc-navigation2.PNG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9a02fe54-66f0-4fce-bf7d-16fad4099abf/bbc-navigation2.PNG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9a02fe54-66f0-4fce-bf7d-16fad4099abf/bbc-navigation2.PNG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9a02fe54-66f0-4fce-bf7d-16fad4099abf/bbc-navigation2.PNG"
			sizes="70vw"
			alt="More BBC News pages"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			More of the BBC News navigation bar (Image source: )
		</figcaption>
	
</figure>


<p>The next scroll down gives users a choice of stories by geography, by subject:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/db560adb-a1c3-474a-ba75-3ba73f78ef2a/bbc-navigation3.PNG">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/db560adb-a1c3-474a-ba75-3ba73f78ef2a/bbc-navigation3.PNG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/db560adb-a1c3-474a-ba75-3ba73f78ef2a/bbc-navigation3.PNG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/db560adb-a1c3-474a-ba75-3ba73f78ef2a/bbc-navigation3.PNG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/db560adb-a1c3-474a-ba75-3ba73f78ef2a/bbc-navigation3.PNG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/db560adb-a1c3-474a-ba75-3ba73f78ef2a/bbc-navigation3.PNG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/db560adb-a1c3-474a-ba75-3ba73f78ef2a/bbc-navigation3.PNG"
			sizes="70vw"
			alt="Even more BBC News pages"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Even more BBC News pages to choose from. (Image source: )
		</figcaption>
	
</figure>


<p>And then there are even more options for sports as well as specific BBC News channels. It’s a lot to take in.</p>

<p>If that weren’t bad enough, the personalization choices mirror the depth of the navigation:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d21c0cad-9c2b-4f3f-8bb0-0f77856bd400/bbc-personalization1.PNG">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d21c0cad-9c2b-4f3f-8bb0-0f77856bd400/bbc-personalization1.PNG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d21c0cad-9c2b-4f3f-8bb0-0f77856bd400/bbc-personalization1.PNG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d21c0cad-9c2b-4f3f-8bb0-0f77856bd400/bbc-personalization1.PNG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d21c0cad-9c2b-4f3f-8bb0-0f77856bd400/bbc-personalization1.PNG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d21c0cad-9c2b-4f3f-8bb0-0f77856bd400/bbc-personalization1.PNG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d21c0cad-9c2b-4f3f-8bb0-0f77856bd400/bbc-personalization1.PNG"
			sizes="70vw"
			alt="BBC News personalization"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			BBC News personalization choices (Image source: )
		</figcaption>
	
</figure>


<p>Now, there’s nothing wrong with personalizing the mobile app experience. I think it’s something every app &mdash; especially those that deliver global news &mdash; should allow for. However, BBC News gives an overwhelming amount of options.</p>

<p>What’s worse is that many of the stories overlap categories, which means users could realistically see the same headlines over and over again as they scroll through the personalized categories they’ve chosen.</p>

<p>If BBC News (or any other app that does this) wants to allow for such deep personalization, the app should be programmed to hide stories that have already been seen or scrolled past &mdash; much like how Feedly handles its stream of news. That way, all that personalization really is valuable.</p>

<p><strong>Recommended reading</strong>: <em></em></p>

<h4>4. Outdated or Incomplete Experience</h4>

<p>Anything a mobile app does that makes users unwillingly stop or slow down is bad. And this could be caused by a number of flaws in the experience:</p>

<ul>
<li>Slow-loading pages,</li>
<li>,</li>
<li>Dated design choices,</li>
<li>Broken links or images,</li>
<li>Incomplete information,</li>
<li>And so on.</li>
</ul>

<p>If you expect users to take time to download and at least give your app a try, make sure it’s worth their while.</p>

<p>One such example of this is the  mobile app. It’s supposed to provide the same exact experience to users as the website counterpart. However, the app doesn’t work all that well:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d9593a16-ea7c-4406-9a89-e3d083f67705/ushud1.PNG">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d9593a16-ea7c-4406-9a89-e3d083f67705/ushud1.PNG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d9593a16-ea7c-4406-9a89-e3d083f67705/ushud1.PNG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d9593a16-ea7c-4406-9a89-e3d083f67705/ushud1.PNG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d9593a16-ea7c-4406-9a89-e3d083f67705/ushud1.PNG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d9593a16-ea7c-4406-9a89-e3d083f67705/ushud1.PNG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d9593a16-ea7c-4406-9a89-e3d083f67705/ushud1.PNG"
			sizes="70vw"
			alt="Slow USHD app"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			A slow-loading page on the USHUD app (Image source: )
		</figcaption>
	
</figure>


<p>In the example above, you can see that search results are slow to load. Now, if they were chock full of images and videos, I could see why that might occur (though it’s still not really acceptable).</p>

<p>That said, many of the properties listed on the app don’t have corresponding visual content:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5fcb5b47-5bd0-4192-b3ab-6887e35c8ba7/ushud2.PNG">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5fcb5b47-5bd0-4192-b3ab-6887e35c8ba7/ushud2.PNG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5fcb5b47-5bd0-4192-b3ab-6887e35c8ba7/ushud2.PNG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5fcb5b47-5bd0-4192-b3ab-6887e35c8ba7/ushud2.PNG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5fcb5b47-5bd0-4192-b3ab-6887e35c8ba7/ushud2.PNG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5fcb5b47-5bd0-4192-b3ab-6887e35c8ba7/ushud2.PNG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5fcb5b47-5bd0-4192-b3ab-6887e35c8ba7/ushud2.PNG"
			sizes="70vw"
			alt="USHUD missing images"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			USHUD is missing images in search. (Image source: )
		</figcaption>
	
</figure>


<p>Real estate apps or, really, any apps that deal in the transaction of purchasing or renting of property or products should include images with each listing. It’s the whole reason why consumers are able to rent and buy online (or at least use it in the decisionmaking process).</p>

<p>But this app seems to be missing many images, which can lead to an unhelpful and unpleasant experience for users who hope to get information from the more convenient mobile app option.</p>

<p>If you’re going to build a mobile app that’s supposed to inform and compel users to engage, make sure it’s running in tip-top shape. All information is available. All tabs are accessible. And pages load in a reasonable timeframe.</p>

<h4>5. Complicated or Impossible Gestures</h4>

<p>We’ve already seen what a poorly made navigation can do to the user experience as well as the problem with pages that just don’t load. But sometimes friction can come from intentionally complicated gestures and engagements.</p>

<p>This is something I personally encountered with .</p>

<p>To start, it delayed the sending of cards by a week. When I signed up in May, I was told I would have to wait <em>at least 60 days</em> to receive my card in the mail, even though my subscription had already kicked in. So, there was already a disparity there.</p>

<p>Sinemia’s response to that was to create a “Cardless” feature. This would enable those users who hadn’t yet received their cards to begin using their accounts. As you can see here, the FAQ included a dedicated section to Sinemia Cardless:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d4b23ff2-e541-43e0-807b-e99a7d6e98d7/sinemia-faq.PNG">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d4b23ff2-e541-43e0-807b-e99a7d6e98d7/sinemia-faq.PNG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d4b23ff2-e541-43e0-807b-e99a7d6e98d7/sinemia-faq.PNG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d4b23ff2-e541-43e0-807b-e99a7d6e98d7/sinemia-faq.PNG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d4b23ff2-e541-43e0-807b-e99a7d6e98d7/sinemia-faq.PNG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d4b23ff2-e541-43e0-807b-e99a7d6e98d7/sinemia-faq.PNG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d4b23ff2-e541-43e0-807b-e99a7d6e98d7/sinemia-faq.PNG"
			sizes="70vw"
			alt="Sinemia FAQ"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Questions about Sinemia Cardless (Image source: )
		</figcaption>
	
</figure>


<p>See that point that says “I can confirm I have the latest Sinemia release installed…”? The reason why that point is there is because many Sinemia Cardless users (myself included) couldn’t actually activate the Cardless feature. When attempting to do so, the app would display an error.</p>

<p>The Sinemia FAQ then goes on to provide this answer to the complaint/question:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d8bdee45-5a2d-4841-860c-239ef785ab00/sinemia-cardless.PNG">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d8bdee45-5a2d-4841-860c-239ef785ab00/sinemia-cardless.PNG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d8bdee45-5a2d-4841-860c-239ef785ab00/sinemia-cardless.PNG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d8bdee45-5a2d-4841-860c-239ef785ab00/sinemia-cardless.PNG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d8bdee45-5a2d-4841-860c-239ef785ab00/sinemia-cardless.PNG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d8bdee45-5a2d-4841-860c-239ef785ab00/sinemia-cardless.PNG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d8bdee45-5a2d-4841-860c-239ef785ab00/sinemia-cardless.PNG"
			sizes="70vw"
			alt="Sinemia Cardless issues"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Sinemia Cardless issues with app version (Image source: )
		</figcaption>
	
</figure>


<p>Here’s the problem: there were never any updates available for the mobile app. So, I and many others reached out to Sinemia for support. The answer repeatedly given was that Cardless could not work if your app ran on an old version. Support asked users to delete the app from their devices and reinstall from the app store to ensure they had the correct version &mdash; to no avail.</p>

<p>For me, this was a big problem. <strong>I was paying for a service that I had no way of using</strong>, and I was spending way too much time uninstalling and installing an app that should work straight out the gate.</p>

<p>I gave up after 48 hours of futile attempts. I went to my Profile to delete my account and get a refund on the subscription I had yet to use. But the app told me it was impossible to cancel my account through it. I tried to ask support for help, but no one responded. So, after Googling similar issues with account cancellations, I found that the only channel through which Sinemia would handle these requests was Facebook Messenger.</p>

<p>Needless to say, the whole experience left me quite jaded about apps that can’t do something as simple as activating or deactivating an account. While I recognize an urge to get a better solution on the mobile app market, rushing out an app and functionality that’s not ready to reach the public isn’t the solution.</p>

<p><strong>Recommended reading</strong>: <em></em></p>

<h4>6. Gated Content Keeps App from Being Valuable</h4>

<p>For those of you who notice your retention rate remaining high for the first week or so from installation, the problem may more have to do with the mobile app’s limitations.</p> 

<p> is a coloring book app I discovered in the app store. There’s nothing in the description that would lead me to believe that the app requires payment in order to enjoy the calming benefits of coloring pictures, but that’s indeed what I encountered:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f035b9ef-7157-440c-8cf3-2ccf5a6b5589/recolor-free.PNG">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f035b9ef-7157-440c-8cf3-2ccf5a6b5589/recolor-free.PNG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f035b9ef-7157-440c-8cf3-2ccf5a6b5589/recolor-free.PNG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f035b9ef-7157-440c-8cf3-2ccf5a6b5589/recolor-free.PNG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f035b9ef-7157-440c-8cf3-2ccf5a6b5589/recolor-free.PNG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f035b9ef-7157-440c-8cf3-2ccf5a6b5589/recolor-free.PNG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f035b9ef-7157-440c-8cf3-2ccf5a6b5589/recolor-free.PNG"
			sizes="70vw"
			alt="Free coloring book images"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Free drawings users can color with the Recolor app. (Image source: )
		</figcaption>
	
</figure>


<p>Above, you can see there are a number of free drawings available. Some of the more complex drawings will take some time to fill in, but not as much as a physical coloring book would by hand, which means users are apt to get through this quickly.</p>

<p>Inevitably, mobile app users will go searching for more options and this is what they will encounter:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/62f24267-b2ff-41db-8d42-5ea5b932efe8/recolor-premium1.PNG">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/62f24267-b2ff-41db-8d42-5ea5b932efe8/recolor-premium1.PNG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/62f24267-b2ff-41db-8d42-5ea5b932efe8/recolor-premium1.PNG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/62f24267-b2ff-41db-8d42-5ea5b932efe8/recolor-premium1.PNG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/62f24267-b2ff-41db-8d42-5ea5b932efe8/recolor-premium1.PNG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/62f24267-b2ff-41db-8d42-5ea5b932efe8/recolor-premium1.PNG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/62f24267-b2ff-41db-8d42-5ea5b932efe8/recolor-premium1.PNG"
			sizes="70vw"
			alt="Recolor is pay to play"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Recolor’s more popular options are for Premium users. (Image source: )
		</figcaption>
	
</figure>


<p>When users look into some of the more popular drawings from Recolor, you’d hope they would encounter at least a few free drawings, right? After all, how many users could possibly be paying for a subscription to this app that’s not outrightly advertised as premium?</p>

<p>But it’s not just the Popular choices that require a fee to access (that’s what the yellow symbol in the bottom-right means). So, too, do most of the other categories:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2cf4ba3b-1ad1-4a7e-a6c2-b21554a9f0a8/recolor-premium2.PNG">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2cf4ba3b-1ad1-4a7e-a6c2-b21554a9f0a8/recolor-premium2.PNG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2cf4ba3b-1ad1-4a7e-a6c2-b21554a9f0a8/recolor-premium2.PNG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2cf4ba3b-1ad1-4a7e-a6c2-b21554a9f0a8/recolor-premium2.PNG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2cf4ba3b-1ad1-4a7e-a6c2-b21554a9f0a8/recolor-premium2.PNG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2cf4ba3b-1ad1-4a7e-a6c2-b21554a9f0a8/recolor-premium2.PNG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2cf4ba3b-1ad1-4a7e-a6c2-b21554a9f0a8/recolor-premium2.PNG"
			sizes="70vw"
			alt="Recolor’s premium offerings"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Premium account needed to access more drawings on Recolor. (Image source: )
		</figcaption>
	
</figure>


<p>It’s a shame that so much of the content is gated off.  have proven to be good for managing anxiety and stress, so leaving users with only a few dozen options doesn’t seem right. Plus, the weekly membership to the app is pretty expensive, even if users try to earn coins by watching videos.</p>

<p>A mobile app such as this one should make its intentions clear from the start: “Consider this a free trial. If you want more, you’ll have to pay.”</p>

<p>While I’m sure the developer didn’t intend to deceive with this app model, I can see how the retention rate might suffer and prevent this app from becoming a long-term staple on many users’ devices.</p>

<blockquote class="pull-quote"><p></p></blockquote>

<p>As I noted earlier, those initial signups might make you hopeful of the app’s long-term potential, but a forced pay-to-play scenario could easily disrupt that after just a few weeks.</p>

<h4>7. Impossible to Convert in-App</h4>

<p>Why do we create mobile apps? For many developers, it’s because the mobile web experience is insufficient. And because many users want a more convenient way to connect with your brand. A mobile app sits on the home screen of devices and requires just a single click to get inside.</p>

<p>So, why would someone build an app that forces users to leave it in order to convert? It seems pointless to even go through the trouble of creating the app in the first place (which is usually no easy task).</p>

<p>Here’s the  app:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/18174f2c-af8f-4839-9fb3-76376a39994a/megabus-find-tix.PNG">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/18174f2c-af8f-4839-9fb3-76376a39994a/megabus-find-tix.PNG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/18174f2c-af8f-4839-9fb3-76376a39994a/megabus-find-tix.PNG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/18174f2c-af8f-4839-9fb3-76376a39994a/megabus-find-tix.PNG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/18174f2c-af8f-4839-9fb3-76376a39994a/megabus-find-tix.PNG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/18174f2c-af8f-4839-9fb3-76376a39994a/megabus-find-tix.PNG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/18174f2c-af8f-4839-9fb3-76376a39994a/megabus-find-tix.PNG"
			sizes="70vw"
			alt="Megabus ticket search"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The Megabus mobile app for searching and buying tickets (Image source: )
		</figcaption>
	
</figure>


<p>Megabus is a low-cost transportation service that operates in Canada, the United States and the United Kingdom. There are a number of reasons why users would gravitate to the mobile app counterpart for the website; namely, the convenience of logging in and purchasing tickets while they’re traveling.</p>

<p>The image above shows the search I did for Megabus tickets through the mobile app. I entered all pertinent details, found tickets available for my destination and got ready to “Buy Tickets” right then and there.</p>

<p>However, you can’t actually buy tickets from the mobile app:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/05aa9005-8477-4315-a280-40a46b7cdfd1/megabus-buy-tix.PNG">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/05aa9005-8477-4315-a280-40a46b7cdfd1/megabus-buy-tix.PNG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/05aa9005-8477-4315-a280-40a46b7cdfd1/megabus-buy-tix.PNG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/05aa9005-8477-4315-a280-40a46b7cdfd1/megabus-buy-tix.PNG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/05aa9005-8477-4315-a280-40a46b7cdfd1/megabus-buy-tix.PNG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/05aa9005-8477-4315-a280-40a46b7cdfd1/megabus-buy-tix.PNG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/05aa9005-8477-4315-a280-40a46b7cdfd1/megabus-buy-tix.PNG"
			sizes="70vw"
			alt="Megabus tickets"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Megabus tickets are only available online. (Image source: )
		</figcaption>
	
</figure>


<p>Upon clicking “Buy Tickets”, the app pushes users out and into their browser. They then are asked to reinput all those details from the mobile app to search for open trips and make a purchase.</p>

<p>For a service that’s supposed to make travel over long distances convenient, its mobile app has done anything but reinforce that experience.</p>

<p>For those of you considering building an app (whether on your own accord or because a client asked) solely so you can land a spot in app store search results, don’t waste users’ time. If they can’t have a complete experience within the app, you’re likely to see your retention rate tank fairly quickly.</p>

<h3>Wrapping Up</h3>

<p>Clearly, there are a number of ways in which a mobile app may suffer a misstep in terms of the user experience. And I’m sure that there are times when mobile app developers don’t even realize there’s something off in the experience.</p>

<p>This is why <strong>your mobile app retention rate is such a critical data point to pay attention to</strong>. It’s not enough to just know what that rate is. You should watch for when those major dropoffs occur; not just in terms of the timeline, but also in terms of which pages lead to a stoppage in activity or an uninstall altogether.</p>

<p>With this data in hand, you can refine the in-app experience and make it one that users want to stay inside of for the long run.</p>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(ra, yk, il)</span>
</div>


              </article>
            </body>
          </html>
---------------
<h1 id="#title_2" >3、文章： CodeFirst：UI设计的未来</h1>
Graham Church
[http://www.infoq.com/cn/articles/codefirst-future-ui-design?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/codefirst-future-ui-design?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/codefirst-future-ui-design/zh/smallimage/codefirst-future-ui-design-s-1538375682680-1539278129058.jpeg"/><p>“设计思维”是响应式移动应用和网站设计的核心，这将把产品的艺术家变成产品的战略家。大型图像和类型设计将继续主导UI和UX。物联网在各行业的崛起将加速VUI的增长。AR和VR将导致对3D设计师的需求激增。AI和数据将颠覆并推动UI设计的未来。</p> <i>By Graham Church</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_3" >4、文章： 大数据凉了？不，流式计算浪潮才刚刚开始</h1>
Reuven Lax, Slava Chernyak, Tyler Akidau
[http://www.infoq.com/cn/articles/the-evolution-of-large-scale-data-processing?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/the-evolution-of-large-scale-data-processing?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/the-evolution-of-large-scale-data-processing/zh/smallimage/logo-culture-1511132556049-1539420792341.jpeg"/><p>本文重点讨论了大数据系统发展的历史轨迹，行文轻松活泼，内容通俗易懂，是一篇茶余饭后用来作为大数据谈资的不严肃说明文。本文翻译自《Streaming System》最后一章《The Evolution of Large-Scale Data Processing》，在探讨流式系统方面本书是市面上难得一见的深度书籍，非常值得学习。</p> <i>By Reuven Lax, Slava Chernyak, Tyler Akidau</i> <i> Translated by 巴真</i>
---------------
<h1 id="#title_4" >5、文章： Gartner分析师：认为区块链幻灭是too young too naive！</h1>
Avivah Litan
[http://www.infoq.com/cn/articles/the-shortsightedness-of-blockchain-disillusionment?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/the-shortsightedness-of-blockchain-disillusionment?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/the-shortsightedness-of-blockchain-disillusionment/zh/smallimage/cs8-ranges-and-recursive-patterns-logo-1532385277819-1539427576289.jpeg"/><p>区块链幻灭？那是你too young too naive！</p> <i>By Avivah Litan</i> <i> Translated by 刘志勇</i>
---------------
<h1 id="#title_5" >6、Flexbox 布局的最简单表单</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2018/10/flexbox-form.html](http://www.ruanyifeng.com/blog/2018/10/flexbox-form.html)
<p>弹性布局（Flexbox）逐渐流行，越来越多人使用，因为它写 CSS 布局真是太方便了。</p>

        <p>三年前，我写过 Flexbox 的介绍（，才意识到一个最简单的表单，就可以解释 Flexbox，而且内容还很实用。</p>

<p>下面，你只需要10分钟，就可以学会简单的表单布局。</p>

<h2>一、&lt;form> 元素</h2>

<p>表单使用<code>&lt;form&gt;</code>元素。</p>

<blockquote><pre><code class="language-markup">
&lt;form>&lt;/form>
</code></pre></blockquote>

<p>上面是一个空表单。根据 HTML 标准，它是一个块级元素，默认将占据全部宽度，但是高度为0，因为没有任何内容。</p>

<h2>二、表单控件</h2>

<p>现在，加入两个最常用的表单控件。</p>

<blockquote><pre><code class="language-markup">
&lt;form>
  &lt;input type="email" name="email">
  &lt;button type="submit">Send&lt;/button>
&lt;/form>
</code></pre></blockquote>

<p>上面代码中，表单包含一个输入框（<code>&lt;input&gt;</code>）和一个按钮（<code>&lt;button&gt;</code>）。</p>

<p>根据标准，这两个控件都是行内块级元素（inline-block），也就是说，它们默认并排在一行上。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201810/bg2018101801.png" alt="" title="" /></p>

<p>上图是浏览器对这个表单的默认渲染（颜色除外），可以看到，这两个控件之间有3像素～4像素的间隔，这是浏览器的内置样式指定的。</p>

<h2>三、指定 Flexbox 布局</h2>

<p>接着，指定表单使用 Flexbox 布局。</p>

<blockquote><pre><code class="language-css">
form  {
  display: flex;
}
</code></pre></blockquote>

<p><img src="https://www.wangbase.com/blogimg/asset/201810/bg2018101802.png" alt="" title="" /></p>

<p>可以看到，两个控件之间的间隔消失了，因为弹性布局的项目（item）默认没有间隔。</p>

<h2>四、flex-grow 属性</h2>

<p>两个地方值得注意。</p>

<blockquote>
  <p>（1）两个控件元素的宽度没有发生变化，因为弹性布局默认不改变项目的宽度。</p>

<p>（2）弹性布局默认左对齐，所以两个控件会从行首开始排列。</p>
</blockquote>

<p>如果我们希望，输入框占据当前行的所有剩余宽度，只需要指定输入框的<code>flex-grow</code>属性为<code>1</code>。</p>

<blockquote><pre><code class="language-css">
input  {
  flex-grow: 1;
}
</code></pre></blockquote>

<p><img src="https://www.wangbase.com/blogimg/asset/201810/bg2018101803.png" alt="" title="" /></p>

<p>上图中，按钮的宽度没变，但是输入框变宽了，等于当前行的宽度减去按钮的宽度。</p>

<p><code>flex-grow</code>属性默认等于<code>0</code>，即使用本来的宽度，不拉伸。等于<code>1</code>时，就表示该项目宽度拉伸，占据当前行的所有剩余宽度。</p>

<h2>五、align-self 属性和 align-items 属性</h2>

<p>我们做一点改变，在按钮里面插入一张图片。</p>

<blockquote><pre><code class="language-markup">
&lt;form action="#">
  &lt;input type="email" placeholder="Enter your email">
  &lt;button type="button">&lt;svg>  &lt;!-- a smiley icon -->  &lt;/svg>&lt;/button>
&lt;/form>
</code></pre></blockquote>

<p>按钮插入图片后，它的高度变了，变得更高了。这时，就发生了一件很奇妙的事情。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201810/bg2018101804.png" alt="" title="" /></p>

<p>上图中，按钮变高了，输入框也自动变得一样高了！</p>

<p>前面说过，<strong>弹性布局默认不改变项目的宽度，但是它默认改变项目的高度。如果项目没有显式指定高度，就将占据容器的所有高度。</strong> 本例中，按钮变高了，导致表单元素也变高了，使得输入框的高度自动拉伸了。</p>

<p><code>align-self</code>属性可以改变这种行为。</p>

<blockquote><pre><code class="language-css">
input {
  flex-grow: 1;
  align-self: center;
}
</code></pre></blockquote>

<p><img src="https://www.wangbase.com/blogimg/asset/201810/bg2018101806.png" alt="" title="" /></p>

<p><code>align-self</code>属性可以取四个值。</p>

<blockquote>
  <ul>
<li><code>flex-start</code>：顶边对齐，高度不拉伸</li>
<li><code>flex-end</code>：底边对齐，高度不拉伸</li>
<li><code>center</code>：居中，高度不拉伸</li>
<li><code>stretch</code>：默认值，高度自动拉伸</li>
</ul>
</blockquote>

<p>如果项目很多，一个个地设置<code>align-self</code>属性就很麻烦。这时，可以在容器元素（本例为表单）设置<code>align-items</code>属性，它的值被所有子项目的<code>align-self</code>属性继承。</p>

<blockquote><pre><code class="language-css">
form {
  display: flex;
  align-items: center;
}
</code></pre></blockquote>

<p>上面代码中，<code>&lt;form&gt;</code>元素设置了<code>align-items</code>以后，就不用在控件上设置<code>align-self</code>，除非希望两者的值不一样。</p>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2018-10-18T08:17:18+08:00">2018年10月18日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>文集：</li>
<li>社交媒体：</li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------
<h1 id="#title_6" >7、文章： 联盟链战国：五大巨头横向对比</h1>
付晓岩
[http://www.infoq.com/cn/articles/5-consortium-blockchain-comparison?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/5-consortium-blockchain-comparison?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/5-consortium-blockchain-comparison/zh/smallimage/logo+%286%29-1539898070815.jpg"/><p>本文选择了 Hyperledger Fabric、FISCO BCOS、微软的 Coco、企业以太坊联盟（EEA）及 R3 的 Corda 这五个具有一定影响力的联盟链，拟从设计理念、生态、效率、扩展性、节点管理与权限管理、智能合约、部署与运维友好性、隐私保护、公链结合或演化能力九个方面进行比对，以供各位开发者、爱好者参考。</p> <i>By 付晓岩</i>
---------------
<h1 id="#title_7" >8、Cloudflare Workers支持WebAssembly和键值存储</h1>
Chris Swan
[http://www.infoq.com/cn/news/2018/10/Cloudflare-Workers-WASM-KV?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/10/Cloudflare-Workers-WASM-KV?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Cloudflare最近宣布给他们的“无服务器”服务Workers新增两个附加功能。WebAssembly使Workers可以通过C、C++、Rust和Go等多种编译语言编写。Workers KV提供了最终一致状态存储机制，托管在Cloudflare全球超过150个数据中心的网络中。</p> <i>By Chris Swan</i> <i> Translated by 刘嘉洋</i>
---------------
<h1 id="#title_8" >9、Amazon全新轻量级服务器端Swift框架：Smoke</h1>
Sergio De Simone
[http://www.infoq.com/cn/news/2018/10/amazon-smoke-swift-server-side?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/10/amazon-smoke-swift-server-side?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Amazon Smoke框架是使用Swift语言编写的全新开源轻量级服务器端框架，用于构建类REST或类RPC的服务。它的架构设计强调易于使用，以及请求处理程序偏向纯函数编程的风格。</p> <i>By Sergio De Simone</i> <i> Translated by 刘嘉洋</i>
---------------
<h1 id="#title_9" >10、Google Cloud Spanner和Cloud Bigtable最新更新</h1>
Steef-Jan Wiggers
[http://www.infoq.com/cn/news/2018/10/gcp-cloud-spanner-bigtable?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/10/gcp-cloud-spanner-bigtable?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Google云平台提供了各种云原生数据库服务，最近，Google更新了其中的两项服务。这些更新会影响Cloud Spanner数据库服务（一种的托管关系数据库产品）和Cloud Bigtable（一种托管的NoSQL键值和宽列数据库）。</p> <i>By Steef-Jan Wiggers</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_10" >11、文章： Polylith：一款新的软件架构</h1>
Joakim Tengstrand
[http://www.infoq.com/cn/articles/Polylith-a-new-architecture?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/Polylith-a-new-architecture?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/Polylith-a-new-architecture/zh/smallimage/logo-c-1524212351520-1539423659927.jpeg"/><p>Polylith是一种软件体系结构，利用许多构件来组合系统，所有构件就像工作在一个地方一样。Polylith克服了单体、微服务、无服务架构的一些缺点，本文希望从概念和实现上对这个新架构做一个介绍，以引起开发使用者的兴趣可以去采纳并应用它。</p> <i>By Joakim Tengstrand</i> <i> Translated by 杨雷</i>
---------------