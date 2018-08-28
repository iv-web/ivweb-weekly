## 文章索引
1、 <a href="#1ux-and-html5:-lets-help-users-fill-in-your-mobile-form-part-2" >UX And HTML5: Let’s Help Users Fill In Your Mobile Form (Part 2)</a><br/>
2、 <a href="#2视频演讲-基于-serverless-架构的小程序开发实践" >视频演讲： 基于 Serverless 架构的小程序开发实践</a><br/>
3、 <a href="#3文章-flink关系型api解读table-api-与sql" >文章： Flink关系型API解读：Table API 与SQL</a><br/>
4、 <a href="#4文章-深入理解junit-5的扩展模型" >文章： 深入理解JUnit 5的扩展模型</a><br/>
5、 <a href="#5文章-serverless架构开发与scf部署实践" >文章： Serverless架构开发与SCF部署实践</a><br/>
6、 <a href="#6文章-v神推荐99容错共识新算法" >文章： V神推荐99%容错共识新算法</a><br/>
7、 <a href="#7fex-技术周刊---2018/08/27" >FEX 技术周刊 - 2018/08/27</a><br/>
8、 <a href="#8amazon-aurora-serverless-mysql已正式可用" >Amazon Aurora Serverless MySQL已正式可用</a><br/>
9、 <a href="#9docker-desktop添加对kubernetes的支持" >Docker Desktop添加对Kubernetes的支持</a><br/>
10、 <a href="#10uber开源其大规模指标平台m3" >Uber开源其大规模指标平台M3</a><br/>
11、 <a href="#11产品思维而不是项目思维" >产品思维而不是项目思维</a><br/>
12、 <a href="#12币圈凉了链圈一切刚刚好" >币圈凉了，链圈一切刚刚好</a><br/><h1 id="#title_0" >1、UX And HTML5: Let’s Help Users Fill In Your Mobile Form (Part 2)</h1>
Stéphanie Walter
[https://www.smashingmagazine.com/2018/08/ux-html5-mobile-form-part-2/](https://www.smashingmagazine.com/2018/08/ux-html5-mobile-form-part-2/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/08/ux-html5-mobile-form-part-2/" />
              <title>UX And HTML5: Let’s Help Users Fill In Your Mobile Form (Part 2)</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>UX And HTML5: Let’s Help Users Fill In Your Mobile Form (Part 2)</h1>
                  
                    
                    <address>Stéphanie Walter</address>
                  
                  <time datetime="2018-08-27T14:00:31&#43;02:00" class="op-published">2018-08-27T14:00:31+02:00</time>
                  <time datetime="2018-08-27T20:14:44&#43;00:00" class="op-modified">2018-08-27T20:14:44+00:00</time>
                </header>
                

<p>In this second part, I want to focus more on mobile-specific capabilities. HTML5, for instance, has brought us a lot of really cool <strong>features to help users fill in mobile forms and format their data. We will see in detail how HTML5 attributes can help</strong> you with that. Then, we will go beyond “classic” form elements and see how to use mobile capabilities such as the camera, geolocation and fingerprint scanners to really take your mobile form experience to the next level on websites and in native applications.</p>

<h3 id="helping-the-user-format-content-with-html5">Helping The User Format Content With HTML5</h3>

<p>In the first part of this series, we saw some general advice on how to display fields. Now it’s time to go a bit deeper and look at how a few well-crafted lines of HTML5 code can improve your mobile forms.</p>

<h4 id="html5-mobile-optimized-goodness">HTML5 Mobile-Optimized Goodness</h4>

<p>HTML5 opens a whole world of possibilities for optimizing forms for mobile and touch devices. A lot of interesting new input types can trigger different keyboards to help users. We can also do some interesting things with capturing media directly in the browser.</p>

<h5 id="entering-numerical-data">Entering Numerical Data</h5>

<p><strong><code>input type= number</code></strong></p>

<p>The HTML5  attribute restricts an input field to numbers. It has a built-in validation system that rejects anything that is not a number.</p>

<p>In some desktop browsers, this input is presented with little arrows on the right that the user can click to increment the number. On mobile, it <strong>opens a keyboard with numbers</strong>, which decreases typos and form-validation errors. The input’s look and feel depend on the operating system.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5a9d0c6e-ce67-4e14-8c55-0cfcf8d8b880/making-mobile-form-experience-better-37-input-number.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5a9d0c6e-ce67-4e14-8c55-0cfcf8d8b880/making-mobile-form-experience-better-37-input-number.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5a9d0c6e-ce67-4e14-8c55-0cfcf8d8b880/making-mobile-form-experience-better-37-input-number.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5a9d0c6e-ce67-4e14-8c55-0cfcf8d8b880/making-mobile-form-experience-better-37-input-number.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5a9d0c6e-ce67-4e14-8c55-0cfcf8d8b880/making-mobile-form-experience-better-37-input-number.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5a9d0c6e-ce67-4e14-8c55-0cfcf8d8b880/making-mobile-form-experience-better-37-input-number.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5a9d0c6e-ce67-4e14-8c55-0cfcf8d8b880/making-mobile-form-experience-better-37-input-number.png"
			sizes="100vw"
			alt="On the left, Android’s keyboard, and on the right, the iOS keyboard with numbers."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			On the left, Android’s keyboard, and on the right, the iOS keyboard with numbers. ()
		</figcaption>
	
</figure>


<p>The input should allow for decimals and negative numbers (but few keyboards respect that). As explained in , &ldquo;a simple way of determining whether to use type=number is to consider whether it would make sense for the input control to have a spinbox interface (e.g. with ‘up’ and ‘down’ arrows)&rdquo;. This means that the input is not supposed to be used for credit cards or area codes.</p>



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




<p><strong>The <code>pattern</code> And <code>inputmode</code> Attributes</strong></p>

<p>To add some restrictions to your number inputs, you could use the <code>pattern</code> attribute to specify a regular expression against which you want to control values.</p>

<p>This is what it looks like:</p>

<pre class="break-out"><code class="language-html">&lt;input type="number" id="quantity" name="quantity" pattern="[0-9]*" inputmode="numeric" /&gt;</code></pre>

<p>You can use this pattern to bring up the big-button numeric keyboard on the iPhone (but not the iPad). This keyboard does not have the minus sign or comma, so users lose the ability to use negative numbers and decimals. Also, they can’t switch back to another keyboard here, so be careful when using this.</p>

<p>Also, note that patterns can be applied to any other type of inputs.</p>

<p>Using only this pattern won’t work on most Android phones. You’ll still need a combination of <code>input type=number</code> and the attribute to make this work.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/aab3d5e8-dbb3-42b4-b1e4-8e9c81077231/making-mobile-form-experience-better-38-input-numeric.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/aab3d5e8-dbb3-42b4-b1e4-8e9c81077231/making-mobile-form-experience-better-38-input-numeric.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/aab3d5e8-dbb3-42b4-b1e4-8e9c81077231/making-mobile-form-experience-better-38-input-numeric.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/aab3d5e8-dbb3-42b4-b1e4-8e9c81077231/making-mobile-form-experience-better-38-input-numeric.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/aab3d5e8-dbb3-42b4-b1e4-8e9c81077231/making-mobile-form-experience-better-38-input-numeric.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/aab3d5e8-dbb3-42b4-b1e4-8e9c81077231/making-mobile-form-experience-better-38-input-numeric.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/aab3d5e8-dbb3-42b4-b1e4-8e9c81077231/making-mobile-form-experience-better-38-input-numeric.png"
			sizes="100vw"
			alt="Android and iOS demo with input type=number, pattern and inputmode."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Android and iOS demo with <code>input type=number</code>, <code>pattern</code> and <code>inputmode</code>. ()
		</figcaption>
	
</figure>


<p><strong><code>inputmode</code></strong></p>

<p>If you only want to trigger the mobile numeric keyboard but don’t want to deal with the <code>type=number</code> and <code>pattern</code> mess, you could use a text input and apply the attribute. It would look like this:</p>

<pre class="break-out"><code class="language-html">&lt;input type="text" id="quantity" name="quantity" inputmode="numeric" /&gt;</code></pre>

<p>Unfortunately (at the time of writing), , but it should be arriving in Chrome desktop 66 without a flag.</p>

<p>To learn more about how to enter numbers in a form, read &ldquo;&rdquo;.</p>

<p><strong><code>input type=tel</code></strong></p>

<p>If you want users to enter a phone number, you can use the . As you can see in the screenshot below, it triggers the same digits on iOS’ keyboard as the pattern attribute described above. Due to the complexity of phone numbers across the world, there is no automatic validation with this input type.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b924751d-56d3-42c1-97f7-8a00a788e1e2/making-mobile-form-experience-better-39-input-tel.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b924751d-56d3-42c1-97f7-8a00a788e1e2/making-mobile-form-experience-better-39-input-tel.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b924751d-56d3-42c1-97f7-8a00a788e1e2/making-mobile-form-experience-better-39-input-tel.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b924751d-56d3-42c1-97f7-8a00a788e1e2/making-mobile-form-experience-better-39-input-tel.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b924751d-56d3-42c1-97f7-8a00a788e1e2/making-mobile-form-experience-better-39-input-tel.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b924751d-56d3-42c1-97f7-8a00a788e1e2/making-mobile-form-experience-better-39-input-tel.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b924751d-56d3-42c1-97f7-8a00a788e1e2/making-mobile-form-experience-better-39-input-tel.png"
			sizes="100vw"
			alt="input type=tel on Android and iOS"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			<code>input type=tel</code> on Android and iOS ()
		</figcaption>
	
</figure>


<h5 id="entering-dates">Entering Dates</h5>

<p>Even if they are technically numerical data, dates deserve their own section. There are a few HTML5 input types for entering dates. The most used is .&rdquo;</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/13460a5d-8a6a-4a62-b187-b6c643f8f5d5/making-mobile-form-experience-better-40-input-date.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/13460a5d-8a6a-4a62-b187-b6c643f8f5d5/making-mobile-form-experience-better-40-input-date.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/13460a5d-8a6a-4a62-b187-b6c643f8f5d5/making-mobile-form-experience-better-40-input-date.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/13460a5d-8a6a-4a62-b187-b6c643f8f5d5/making-mobile-form-experience-better-40-input-date.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/13460a5d-8a6a-4a62-b187-b6c643f8f5d5/making-mobile-form-experience-better-40-input-date.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/13460a5d-8a6a-4a62-b187-b6c643f8f5d5/making-mobile-form-experience-better-40-input-date.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/13460a5d-8a6a-4a62-b187-b6c643f8f5d5/making-mobile-form-experience-better-40-input-date.png"
			sizes="100vw"
			alt="A date-picker based on input type=date on Android and iOS"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			A date-picker based on <code>input type=date</code> on Android and iOS ()
		</figcaption>
	
</figure>


<p>There’s also  to pick a date <em>and</em> a time (using the user’s local time). So many choices!</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b14867d8-1d6e-4887-b692-487a52e1d1a7/making-mobile-form-experience-better-41-timeweek.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b14867d8-1d6e-4887-b692-487a52e1d1a7/making-mobile-form-experience-better-41-timeweek.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b14867d8-1d6e-4887-b692-487a52e1d1a7/making-mobile-form-experience-better-41-timeweek.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b14867d8-1d6e-4887-b692-487a52e1d1a7/making-mobile-form-experience-better-41-timeweek.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b14867d8-1d6e-4887-b692-487a52e1d1a7/making-mobile-form-experience-better-41-timeweek.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b14867d8-1d6e-4887-b692-487a52e1d1a7/making-mobile-form-experience-better-41-timeweek.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b14867d8-1d6e-4887-b692-487a52e1d1a7/making-mobile-form-experience-better-41-timeweek.jpg"
			sizes="100vw"
			alt="Example of date-picker with more options on Android"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Example of date-picker with more options on Android (week, date and time, etc.) ()
		</figcaption>
	
</figure>


<p><code>input type=date</code> works well for booking interfaces, for example. You might have some needs that require you to build your own date-picker, though (). But <code>input type=date</code> is always a nice option if you need a date-picker and don’t want to bring a whole JavaScript library into the website for the job.</p>

<div class="sponsors__wide-place"></div>




<p>Yet, sometimes not using <code>type=date</code> for dates is better. Let’s take the example of a birth date. If I was born in 1960 (I’m not &mdash; this is just an example), it would take me many taps to pick my birth date if I was starting from 2018. On Android, I discovered recently that if I press on the year in the picker, I get a sort of dropdown wheel with all of the years. A bit better, but it still requires a fair amount of scrolling.</p>

<p>A :</p>

<blockquote>"I’m born in 1977 and can confirm the annoyance. The more time it takes to scroll, the older you feel :-("</blockquote>

<p>So, maybe birth dates are not the best candidate for date-pickers.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1508c7f2-9e28-4f14-8925-523fa11534f3/making-mobile-form-experience-better-42-date-picker.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1508c7f2-9e28-4f14-8925-523fa11534f3/making-mobile-form-experience-better-42-date-picker.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1508c7f2-9e28-4f14-8925-523fa11534f3/making-mobile-form-experience-better-42-date-picker.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1508c7f2-9e28-4f14-8925-523fa11534f3/making-mobile-form-experience-better-42-date-picker.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1508c7f2-9e28-4f14-8925-523fa11534f3/making-mobile-form-experience-better-42-date-picker.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1508c7f2-9e28-4f14-8925-523fa11534f3/making-mobile-form-experience-better-42-date-picker.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1508c7f2-9e28-4f14-8925-523fa11534f3/making-mobile-form-experience-better-42-date-picker.jpg"
			sizes="100vw"
			alt="With Android’s date-picker, even though you can press and hold the year to get a year-picker, picking a birth date is still tedious."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			With Android’s date-picker, even though you can press and hold the year to get a year-picker, picking a birth date is still tedious. ()
		</figcaption>
	
</figure>


<h5 id="url-email-tel-and-search">URL, Email, Tel And Search</h5>

<p>Mobile phones hide some other keyboard and input-optimization goodness that enhance the user’s experience when filling in a form. The devil is in the details, as they say.</p>

<p>Using the  field will bring up an optimized keyboard on mobile, with <kbd>/</kbd> (the slash key) directly accessible. Depending on the OS, you can also give quick access to commons top-level domains, like the <code>.fr</code> in the screenshot below. If you long-press this button, shortcuts to other top-level domains will appear. This also comes with automatic browser validation that checks that the URL’s format is valid.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3b638893-8768-4c94-9174-20d255e9035e/making-mobile-form-experience-better-43-input-url.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3b638893-8768-4c94-9174-20d255e9035e/making-mobile-form-experience-better-43-input-url.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3b638893-8768-4c94-9174-20d255e9035e/making-mobile-form-experience-better-43-input-url.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3b638893-8768-4c94-9174-20d255e9035e/making-mobile-form-experience-better-43-input-url.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3b638893-8768-4c94-9174-20d255e9035e/making-mobile-form-experience-better-43-input-url.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3b638893-8768-4c94-9174-20d255e9035e/making-mobile-form-experience-better-43-input-url.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3b638893-8768-4c94-9174-20d255e9035e/making-mobile-form-experience-better-43-input-url.png"
			sizes="100vw"
			alt="input type=url keyboard on Android and iOS"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			<code>input type=url</code> keyboard on Android and iOS ()
		</figcaption>
	
</figure>


<p>The field brings up an email-optimized keyboard giving quick access to the <code>@</code> symbol. This input requires the presence of <code>@</code> somewhere in the field in order to be valid. That’s the only verification it does.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/13fe0a6f-b8bc-4541-b624-30dfb6fbf85b/making-mobile-form-experience-better-44-input-email.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/13fe0a6f-b8bc-4541-b624-30dfb6fbf85b/making-mobile-form-experience-better-44-input-email.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/13fe0a6f-b8bc-4541-b624-30dfb6fbf85b/making-mobile-form-experience-better-44-input-email.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/13fe0a6f-b8bc-4541-b624-30dfb6fbf85b/making-mobile-form-experience-better-44-input-email.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/13fe0a6f-b8bc-4541-b624-30dfb6fbf85b/making-mobile-form-experience-better-44-input-email.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/13fe0a6f-b8bc-4541-b624-30dfb6fbf85b/making-mobile-form-experience-better-44-input-email.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/13fe0a6f-b8bc-4541-b624-30dfb6fbf85b/making-mobile-form-experience-better-44-input-email.png"
			sizes="100vw"
			alt="input type=email keyboard on Android and iOS"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			<code>input type=email</code> keyboard on Android and iOS ()
		</figcaption>
	
</figure>


<p>The  field brings up a search-optimized keyboard. The user can directly launch the search from a button on the keyboard. There’s also a little cross to clear the field and type a new query.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8e56b3fb-4d44-47ed-bc21-c26461a8a182/making-mobile-form-experience-better-45-input-search.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8e56b3fb-4d44-47ed-bc21-c26461a8a182/making-mobile-form-experience-better-45-input-search.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8e56b3fb-4d44-47ed-bc21-c26461a8a182/making-mobile-form-experience-better-45-input-search.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8e56b3fb-4d44-47ed-bc21-c26461a8a182/making-mobile-form-experience-better-45-input-search.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8e56b3fb-4d44-47ed-bc21-c26461a8a182/making-mobile-form-experience-better-45-input-search.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8e56b3fb-4d44-47ed-bc21-c26461a8a182/making-mobile-form-experience-better-45-input-search.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8e56b3fb-4d44-47ed-bc21-c26461a8a182/making-mobile-form-experience-better-45-input-search.png"
			sizes="100vw"
			alt="input type=search keyboard on Android and iOS"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			<code>input type=search</code> keyboard on Android and iOS ()
		</figcaption>
	
</figure>


<h5 id="range-and-color">Range And Color</h5>

<p>The last two input types we looked at are not particularly optimized for mobile, but by using them, we can avoid having to load heavy custom JavaScript libraries, which is a good idea for mobile users.</p>

<p> provides a visual UI slider to input a number. The UI for this control is browser-dependent.</p>

<p> provides an easy way for the user to enter a color value. In many browser implementations, this comes with a color-picker.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/feae3167-10e4-4508-b499-59c6931f8691/making-mobile-form-experience-better-46-input-c-range.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/feae3167-10e4-4508-b499-59c6931f8691/making-mobile-form-experience-better-46-input-c-range.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/feae3167-10e4-4508-b499-59c6931f8691/making-mobile-form-experience-better-46-input-c-range.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/feae3167-10e4-4508-b499-59c6931f8691/making-mobile-form-experience-better-46-input-c-range.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/feae3167-10e4-4508-b499-59c6931f8691/making-mobile-form-experience-better-46-input-c-range.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/feae3167-10e4-4508-b499-59c6931f8691/making-mobile-form-experience-better-46-input-c-range.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/feae3167-10e4-4508-b499-59c6931f8691/making-mobile-form-experience-better-46-input-c-range.png"
			sizes="100vw"
			alt="input type=range and input type=color on Android and iOS"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			<code>input type=range</code> and <code>input type=color</code> on Android and iOS ()
		</figcaption>
	
</figure>


<h5 id="html-media-capture-taking-and-uploading-pictures-and-recording-sound">HTML Media Capture: Taking And Uploading Pictures And Recording Sound</h5>

<p>I remember the time of the iPhone 3, when Apple would not even allow a simple <code>input type=file</code> to be used on a website, for security reasons. Those times are long gone. With the , it’s now possible to access different sensors of a device. We can capture photos and videos, and we can even record voice directly in the browser.</p>

<p>The  lets you specify what kind of media to accept in the input: audio, image, video. The user can give the browser direct access to their camera, for example.</p>

<p>The code looks like this:</p>

<pre class="break-out"><code class="language-html">&lt;input type="file" id="take-picture" accept="image/*"&gt;</code></pre>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8dff911a-9299-4951-95e3-03f90ecc0e7e/making-mobile-form-experience-better-48-capture.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8dff911a-9299-4951-95e3-03f90ecc0e7e/making-mobile-form-experience-better-48-capture.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8dff911a-9299-4951-95e3-03f90ecc0e7e/making-mobile-form-experience-better-48-capture.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8dff911a-9299-4951-95e3-03f90ecc0e7e/making-mobile-form-experience-better-48-capture.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8dff911a-9299-4951-95e3-03f90ecc0e7e/making-mobile-form-experience-better-48-capture.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8dff911a-9299-4951-95e3-03f90ecc0e7e/making-mobile-form-experience-better-48-capture.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8dff911a-9299-4951-95e3-03f90ecc0e7e/making-mobile-form-experience-better-48-capture.jpg"
			sizes="100vw"
			alt="The accept attribute is set to image. The browser asks whether I want to access the camera directly or the files on the device."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The <code>accept</code> attribute is set to <code>image</code>. The browser asks whether I want to access the camera directly or the files on the device. ()
		</figcaption>
	
</figure>


<p>The  lets you specify the preferred mode of capture. If you add the <code>capture</code> attribute on top of the <code>accept</code> attribute, you can make the browser open the camera or voice recorder directly.</p>

<pre class="break-out"><code class="language-html">&lt;input type="file" accept="image/*" capture&gt; // opens the camera&gt;
</code></pre>

<pre class="break-out"><code class="language-html">&lt;input type="file" accept="video/*" capture&gt; // opens the camera in video mode
</code></pre>

<pre class="break-out"><code class="language-html">&lt;input type="file" accept="audio/*" capture&gt; // opens the voice recorder
</code></pre>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b1ee8822-cb93-43f3-9016-947566308416/making-mobile-form-experience-better-49-opening.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b1ee8822-cb93-43f3-9016-947566308416/making-mobile-form-experience-better-49-opening.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b1ee8822-cb93-43f3-9016-947566308416/making-mobile-form-experience-better-49-opening.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b1ee8822-cb93-43f3-9016-947566308416/making-mobile-form-experience-better-49-opening.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b1ee8822-cb93-43f3-9016-947566308416/making-mobile-form-experience-better-49-opening.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b1ee8822-cb93-43f3-9016-947566308416/making-mobile-form-experience-better-49-opening.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b1ee8822-cb93-43f3-9016-947566308416/making-mobile-form-experience-better-49-opening.jpg"
			sizes="100vw"
			alt="The mobile browser directly opens the capture mechanism: on the left, the camera, on the right, the video recorder."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The mobile browser directly opens the capture mechanism: on the left, the camera, on the right, the video recorder. ()
		</figcaption>
	
</figure>


<p>For more details on how to use media directly in the browser, read the section &ldquo;&rdquo; in my article on the secret powers of mobile browsers.</p>

<h5 id="html5-autos-autocorrect-autocomplete-autofill-autocapitalize-and-autofocus">HTML5 Autos: Autocorrect, Autocomplete, Autofill, Autocapitalize And Autofocus</h5>

<p>HTML5 comes with a slew of automatic attributes. To enhance the mobile experience, you will want to be smart about what can be automated and what can’t. Here are some general rules of thumb:</p>

<ul>
<li><strong>Disable autocorrect on things for which the dictionary is weak</strong>: email addresses, numbers, names, addresses, cities, regions, area codes, credit card numbers.</li>
<li><strong>Disable autocapitalize for email</strong> fields and other fields where appropriate (for example, website URLs). Note that <code>type=email</code> does the job for you in recents version of iOS and Android, but disable it anyway for older versions or if <code>type=email</code> is not supported.</li>
<li>You can set the autocapitalize attribute to <code>words</code> to automatically <strong>uppercase the first letter of each word</strong> the user types. This can be useful for names, places and the like, but, again, be careful with it, and test it.</li>
</ul>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/067eeb52-d66f-4f28-b859-e7269a7b50f4/making-mobile-form-experience-better-50-autos.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/067eeb52-d66f-4f28-b859-e7269a7b50f4/making-mobile-form-experience-better-50-autos.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/067eeb52-d66f-4f28-b859-e7269a7b50f4/making-mobile-form-experience-better-50-autos.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/067eeb52-d66f-4f28-b859-e7269a7b50f4/making-mobile-form-experience-better-50-autos.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/067eeb52-d66f-4f28-b859-e7269a7b50f4/making-mobile-form-experience-better-50-autos.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/067eeb52-d66f-4f28-b859-e7269a7b50f4/making-mobile-form-experience-better-50-autos.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/067eeb52-d66f-4f28-b859-e7269a7b50f4/making-mobile-form-experience-better-50-autos.jpg"
			sizes="100vw"
			alt="Use input type=email for email addresses. If you don’t, at least deactivate auto-capitalization. No email address starts with a capital letter."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Use <code>input type=email</code> for email addresses. If you don’t, at least deactivate auto-capitalization. No email address starts with a capital letter. ()
		</figcaption>
	
</figure>


<ul>
<li>For <code>input type=tel</code>, set <code>autocomplete=&quot;tel&quot;</code>.</li>
<li>You could use <code>autofocus</code> to give the focus to a control element when the user loads the page. But just because the user opens the &ldquo;contact&rdquo; page, it does not mean they are ready to jump right to the first field of your form. So, again, use it wisely.</li>
</ul>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f4d2154a-9fed-47e5-bb5b-d1cece87128c/making-mobile-form-experience-better-51-focus-loading.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f4d2154a-9fed-47e5-bb5b-d1cece87128c/making-mobile-form-experience-better-51-focus-loading.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f4d2154a-9fed-47e5-bb5b-d1cece87128c/making-mobile-form-experience-better-51-focus-loading.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f4d2154a-9fed-47e5-bb5b-d1cece87128c/making-mobile-form-experience-better-51-focus-loading.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f4d2154a-9fed-47e5-bb5b-d1cece87128c/making-mobile-form-experience-better-51-focus-loading.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f4d2154a-9fed-47e5-bb5b-d1cece87128c/making-mobile-form-experience-better-51-focus-loading.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f4d2154a-9fed-47e5-bb5b-d1cece87128c/making-mobile-form-experience-better-51-focus-loading.jpg"
			sizes="100vw"
			alt="In this example, we could use autofocus to take the user directly to the first field once they’ve clicked on the button."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			In this example, we could use <code>autofocus</code> to take the user directly to the first field once they’ve clicked on the button. ()
		</figcaption>
	
</figure>


<p>If you want . Just make sure you use the right ones. Implement, test, and test again.</p>

<h5 id="html5-form-validation">HTML5 Form Validation</h5>

<p>I won’t get into the technical details here, but you should know that . It’s nice if you don’t want to use a JavaScript library to display inline validation messages. Here are the main things you need to know as a UX designer about HTML5 form validation:</p>

<ul>
<li>The validation message is a browser control. You can’t style it in CSS, and it’s different for every browser.</li>
<li>You can change the text of the message in JavaScript using <code>setCustomValidity</code>.</li>
<li>. These get triggered on blur, so are pretty much useless for now.</li>
</ul>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/934a1c5f-deac-4988-bdd9-5d471e57b561/making-mobile-form-experience-better-52-validation.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/934a1c5f-deac-4988-bdd9-5d471e57b561/making-mobile-form-experience-better-52-validation.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/934a1c5f-deac-4988-bdd9-5d471e57b561/making-mobile-form-experience-better-52-validation.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/934a1c5f-deac-4988-bdd9-5d471e57b561/making-mobile-form-experience-better-52-validation.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/934a1c5f-deac-4988-bdd9-5d471e57b561/making-mobile-form-experience-better-52-validation.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/934a1c5f-deac-4988-bdd9-5d471e57b561/making-mobile-form-experience-better-52-validation.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/934a1c5f-deac-4988-bdd9-5d471e57b561/making-mobile-form-experience-better-52-validation.jpg"
			sizes="100vw"
			alt="HTML native form validation in an Android browser"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			HTML native form validation in an Android browser ()
		</figcaption>
	
</figure>


<p>In “,” Peter-Paul Koch goes into detail on why HTML and CSS form validation doesn’t really make forms better at this time.</p>

<h5 id="offline-support-to-save-user-data">Offline Support To Save User Data</h5>

<p>A lot of things can go wrong, especially on mobile. Mistakes happen. A user could mistap the back button in the browser and lose all of their data.</p>

<p><strong>If the user comes back to the page, it would be nice to display their data again</strong>. The same goes for if the browser crashes or the user closes the tab. You can <strong>store the user’s data in local or session storage</strong> to ensure nothing gets lost if something goes wrong. Geoffrey Crofte has .</p>

<p>If the connection is lost as the user is submitting the form, they might also lose the data. To avoid this, you could use a combination of the** HTML5 offline API** and the <strong>Service Workers API</strong> to:</p>

<ul>
<li>store the data in the cache,</li>
<li>try to automatically send it again when the connection comes back.</li>
</ul>

<p>To learn how to code this, check out the article on &ldquo;&rdquo;.</p>

<h3 id="mobile-device-capabilities-can-take-the-experience-to-the-next-level">Mobile Device Capabilities Can Take the Experience To The Next Level</h3>

<p>In , we stuck to the basic common HTML form elements and attributes for enhancing mobile forms. But mobile devices capabilities now go far beyond displaying HTML, CSS and JavaScript web pages. Those little devices come <strong>equipped with a lot of sensors</strong>. And we will be able to <strong>use many of those in native apps and on the web</strong> to make our users’ lives so much easier.</p>

<h4 id="detecting-the-user-s-location">Detecting The User’s Location</h4>

<p>In the previous section, I wrote about pre-filling information for places and addresses. That’s a good start. We can go one step further. <strong>Instead of asking users to type a location, we can detect it</strong>. Meet the  for the web. There are also native iOS, Android and Windows Phone geolocation APIs.</p>

<p>Citymapper is a website and an app that helps users plan their travels. When the user goes into the first field, they see the &ldquo;Use current location&rdquo; option. If they select it, they are asked to allow the browser to access their geolocation data. This is the geolocation API. The browser then autocompletes the location it found and, the user can proceed to the destination field. The native app works pretty much the same way.</p>

<figure class="video-container"><iframe data-src="https://player.vimeo.com/video/285090916" width="600" height="480" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe><br /><em>Citymapper proposes the user’s current location as the starting point for the journey.</em></figure>

<h4 id="be-smart-when-asking-for-the-user-s-permission">Be Smart When Asking For The User’s Permission</h4>

<p>You might have noticed in the previous video that I had to agree to give access to my position to the Citymapper website. In the browser, the user handles permissions website by website, API by API.</p>

<p>You also <strong>need to be careful how you ask for permission</strong>. The user might refuse access to the geolocation, notification or other API if you ask too soon. They also might refuse if they don’t understand why you need the permission. <strong>You get one chance; use it wisely</strong>. After that, it will be almost impossible to recover. I’m an Android power user, and even I have to search around for the options in my browser when I want to reset the permissions I’ve given to a website. Imagine the trouble your users will have.</p>

<p>Here is some general advice on asking for permissions on the web:</p>

<ul>
<li>Don’t be the creepy geolocation or notification stalker: <strong>Don’t ask for permission as soon as the user arrives on your website</strong>. They might not know about you or your service yet.</li>
<li>Let the user discover your website and service. Then, <strong>ask for permission in context</strong>. If you want to access their location, ask them only when you need it (Citymapper is a good example).</li>
<li>Explain <strong>why you need permission and what you will do with it</strong>.</li>
</ul>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6ed9222f-d200-4b5f-8b0a-f73fa24ba884/making-mobile-form-experience-better-53-permissions.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6ed9222f-d200-4b5f-8b0a-f73fa24ba884/making-mobile-form-experience-better-53-permissions.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6ed9222f-d200-4b5f-8b0a-f73fa24ba884/making-mobile-form-experience-better-53-permissions.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6ed9222f-d200-4b5f-8b0a-f73fa24ba884/making-mobile-form-experience-better-53-permissions.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6ed9222f-d200-4b5f-8b0a-f73fa24ba884/making-mobile-form-experience-better-53-permissions.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6ed9222f-d200-4b5f-8b0a-f73fa24ba884/making-mobile-form-experience-better-53-permissions.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6ed9222f-d200-4b5f-8b0a-f73fa24ba884/making-mobile-form-experience-better-53-permissions.jpg"
			sizes="100vw"
			alt="Citymapper asks for access to the user’s location only when it needs it. Clearing permissions after the user refuses it can get really complicated because the user will need to search through their settings for that website."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Citymapper asks for access to the user’s location only when it needs it. Clearing permissions after the user refuses it can get really complicated because the user will need to search through their settings for that website. ()
		</figcaption>
	
</figure>


<p>If you want to go further, Luke Wroblewski (yes, him again) has created a .</p>

<h4 id="a-better-checkout-experience">A Better Checkout Experience</h4>

<p>A big area of improvement for forms is the whole checkout payment experience. Here again, sensors on the device can make this an almost painless experience. The only pain will be the amount of money the user spends.</p>

<h5 id="ios-credit-card-scanner">iOS Credit Card Scanner</h5>

<p>In the previous section, I wrote about autodetection of credit cards and autocompletion features based on the user’s previous input. This still means that the user has to type their credit card data at least once.</p>

<p>Apple has taken this to the next level with its <strong>credit card scanner</strong>. Since iOS 8 in Safari, <strong>users can use their camera to scan and autocomplete</strong> their credit card information. To perform this magic, you will need to add the autocomplete <code>cc-number</code> attribute and some name to identify this as a credit card field. Apple doesn’t have much official information on it, but .</p>

<p>Safari also has , allowing them reuse it on multiple websites.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e4139e02-1864-47e1-abb0-910ad1aeff01/making-mobile-form-experience-better-54-ios-creditcard-scan.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e4139e02-1864-47e1-abb0-910ad1aeff01/making-mobile-form-experience-better-54-ios-creditcard-scan.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e4139e02-1864-47e1-abb0-910ad1aeff01/making-mobile-form-experience-better-54-ios-creditcard-scan.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e4139e02-1864-47e1-abb0-910ad1aeff01/making-mobile-form-experience-better-54-ios-creditcard-scan.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e4139e02-1864-47e1-abb0-910ad1aeff01/making-mobile-form-experience-better-54-ios-creditcard-scan.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e4139e02-1864-47e1-abb0-910ad1aeff01/making-mobile-form-experience-better-54-ios-creditcard-scan.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e4139e02-1864-47e1-abb0-910ad1aeff01/making-mobile-form-experience-better-54-ios-creditcard-scan.jpg"
			sizes="100vw"
			alt="The credit card scanning option appears when Safari detects a field that matches the credit card format. If the user already has a card registered on the phone, they can use the autofill option."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The credit card scanning option appears when Safari detects a field that matches the credit card format. If the user already has a card registered on the phone, they can use the autofill option. ()
		</figcaption>
	
</figure>


<h5 id="take-checkout-one-step-further-with-google-pay-api">Take Checkout One Step Further With Google Pay API</h5>

<p>Google launched something similar: the . When implemented on a website, the API <strong>eliminates the need to manually enter payment information</strong>. It goes one step further: It can store billing and shipping addresses as well.</p>

<p>The user gets a dialog in Chrome that displays the various payment information they’ve stored. They can choose which one to use and can <strong>pay directly through the dialog</strong>.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ef94d52f-9476-49a7-a5f4-08983b057d01/making-mobile-form-experience-better-55-android-fast-checkout.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ef94d52f-9476-49a7-a5f4-08983b057d01/making-mobile-form-experience-better-55-android-fast-checkout.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ef94d52f-9476-49a7-a5f4-08983b057d01/making-mobile-form-experience-better-55-android-fast-checkout.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ef94d52f-9476-49a7-a5f4-08983b057d01/making-mobile-form-experience-better-55-android-fast-checkout.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ef94d52f-9476-49a7-a5f4-08983b057d01/making-mobile-form-experience-better-55-android-fast-checkout.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ef94d52f-9476-49a7-a5f4-08983b057d01/making-mobile-form-experience-better-55-android-fast-checkout.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ef94d52f-9476-49a7-a5f4-08983b057d01/making-mobile-form-experience-better-55-android-fast-checkout.jpg"
			sizes="100vw"
			alt="The Google Pay API pop-up triggered on an e-commerce website"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The Google Pay API pop-up triggered on an e-commerce website ()
		</figcaption>
	
</figure>


<p>A . If this gets implemented in browsers, it would allow users to check out with a single button, which would request the API. Every step thereafter would be handled by native browser dialogs.</p>

<h4 id="making-authentication-easier">Making Authentication Easier</h4>

<p>Mobile phones are, in most cases, personal devices that people don’t usually share with others. This opens up some interesting opportunities for authentication.</p>

<h5 id="magic-link">Magic Link</h5>

<p>I use a password manager. I don’t know 99% of my passwords. They are all randomly generated. In order to log into a new Slack workspace, I must:</p>

<ol>
<li>open my password manager,</li>
<li>enter my master password,</li>
<li>search for the workspace,</li>
<li>copy and paste the password into the Slack app.</li>
</ol>

<p>It’s a tedious process, but Slack was smart enough to provide a better option.</p>

<div class="sponsors__wide-place"></div>




<p>Many users have they mail synchronized on their phone. Slack understood that. When you add a new Slack workspace in the app, you can either log in using the password or ask for the &ldquo;magic link&rdquo; option. If you opt for the latter, <strong>Slack sends a magic link to your mailbox</strong>. Open the mail, click on the big green button, and &mdash; <em>ta-da!</em> &mdash; you’re logged in.</p>

<p>Behind the scenes, this magic link contains an authentication token. The Slack app catches this and authenticates you without requiring the password.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ee1eecc3-74a2-4375-8609-981e29c3db0e/55a-making-mobile-form-experience-better-slack.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ee1eecc3-74a2-4375-8609-981e29c3db0e/55a-making-mobile-form-experience-better-slack.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ee1eecc3-74a2-4375-8609-981e29c3db0e/55a-making-mobile-form-experience-better-slack.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ee1eecc3-74a2-4375-8609-981e29c3db0e/55a-making-mobile-form-experience-better-slack.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ee1eecc3-74a2-4375-8609-981e29c3db0e/55a-making-mobile-form-experience-better-slack.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ee1eecc3-74a2-4375-8609-981e29c3db0e/55a-making-mobile-form-experience-better-slack.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ee1eecc3-74a2-4375-8609-981e29c3db0e/55a-making-mobile-form-experience-better-slack.jpg"
			sizes="100vw"
			alt="When using the magic link option, Slack sends you an email with a link that lets you connect to your slack without having to enter your password."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			When using the magic link option, Slack sends you an email with a link that lets you connect to your slack without having to enter your password. ()
		</figcaption>
	
</figure>


<h5 id="fingerprint-for-smart-identification">Fingerprint For Smart Identification</h5>

<p>I do almost all of my banking on my mobile device. And when it comes to logging into my bank accounts, there’s a world of difference between my French Societe General bank app and the German N26 app.</p>

<p>With Société Générale, I have a login string and a passphrase. I can ask the app to remember the login string, which is 10 random digits. I’m not able to remember that one; I use a password manager for it. I must still remember and enter the six-digit passphrase on a custom-built keypad. Of course, the numbers’ positions change every time I log in. Security &mdash; yeah, I know. Also, I must change this passphrase every three months. The last time I was forced to change the passphrase, I did what most people do: choose almost the same passphrase, because I don’t want to have to remember yet another six-digit number. And of course, I was damn sure I would remember it, so I did not enter it in my password manager. Rookie mistake. Two weeks later, I tried to log in. Of course, I forgot it. I made three failed attempts, and then my account was blocked. Fortunately, I only use this account for savings. In the app, you can ask for a new passcode. It took almost one week for the bank to send me a new six-digit passphrase by paper mail to my home address in Luxembourg. Yeah.</p>

<p>N26, on the other hand, uses my email address as the login string. I can remember that without a password manager. When I want to log in, I put my finger on the start button of my Xperia phone, and that’s it. In the background, my phone scans my fingerprint and authenticates me. If that does not work, I can fall back to a password.</p>

<p>Same device, two apps, two totally different experiences.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0653d65d-f41c-40bf-8c3a-c44b8150b08c/making-mobile-form-experience-better-56-password-fingerprint.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0653d65d-f41c-40bf-8c3a-c44b8150b08c/making-mobile-form-experience-better-56-password-fingerprint.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0653d65d-f41c-40bf-8c3a-c44b8150b08c/making-mobile-form-experience-better-56-password-fingerprint.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0653d65d-f41c-40bf-8c3a-c44b8150b08c/making-mobile-form-experience-better-56-password-fingerprint.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0653d65d-f41c-40bf-8c3a-c44b8150b08c/making-mobile-form-experience-better-56-password-fingerprint.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0653d65d-f41c-40bf-8c3a-c44b8150b08c/making-mobile-form-experience-better-56-password-fingerprint.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0653d65d-f41c-40bf-8c3a-c44b8150b08c/making-mobile-form-experience-better-56-password-fingerprint.jpg"
			sizes="100vw"
			alt="Dropbox has another example of fingerprint authentication."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Dropbox has another example of fingerprint authentication. ()
		</figcaption>
	
</figure>


<p>More and more apps on both Android and iOS now offer user the possibility to <strong>authenticate with a fingerprint</strong>. No more passwords &mdash; it’s an interesting and elegant solution.</p>

<p>Of course, people have expressed some security concerns about this. For the National Institute of Standards and Technology (NIST), . It advises combining biometrics with a second factor of authentication.</p>

<p>Fingerprint sensors can also be tricked &mdash; yes, like in spy movies. Did you hear about the plane that was forced to land because a woman learned of her husband’s infidelity after  while he was sleeping?</p>

<h5 id="facial-recognition-and-face-id">Facial Recognition And Face ID</h5>

<p>In 2018, Apple launched the iPhone X with the brand new . Users can <strong>unlock their iPhone X using their face</strong>. Of course, some other Android phones and Windows tablets and computers had proposed this feature earlier. But when Apple launches something, it tends to become &ldquo;a thing&rdquo;. For the moment, this technology is mostly used as authentication to unlock phones and computer.</p>

<p>There are some pretty big challenges with facial-recognition technology. First, some algorithms can be fooled by a picture of the person, which is easily hackable. Another bigger concern is diversity. Facial-recognition algorithms tend to have difficulty recognizing people of color. For instance, a  about the issue.</p>

<p>Some facial-recognition software is also used by some customs services to speed up border processing. It is used in New Zealand and will be used in Canada.</p>

<p>Most of us have seen enough science fiction to see the potential problems and consequences of systems that use facial recognition at scale. This kind of technology used outside of the private space of unlocking phones can get controversial and scary.</p>

<h5 id="google-one-tap-sign-up">Google: One-Tap Sign-Up</h5>

<p>If a user has a Google account, they can benefit from , they get automatically signed in on other devices as well.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/62f2d217-919c-47dc-ab6e-15d14641f0d7/making-mobile-form-experience-better-57-google-signin.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/62f2d217-919c-47dc-ab6e-15d14641f0d7/making-mobile-form-experience-better-57-google-signin.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/62f2d217-919c-47dc-ab6e-15d14641f0d7/making-mobile-form-experience-better-57-google-signin.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/62f2d217-919c-47dc-ab6e-15d14641f0d7/making-mobile-form-experience-better-57-google-signin.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/62f2d217-919c-47dc-ab6e-15d14641f0d7/making-mobile-form-experience-better-57-google-signin.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/62f2d217-919c-47dc-ab6e-15d14641f0d7/making-mobile-form-experience-better-57-google-signin.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/62f2d217-919c-47dc-ab6e-15d14641f0d7/making-mobile-form-experience-better-57-google-signin.jpg"
			sizes="100vw"
			alt="Google’s one-tap sign-up dialog"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Google’s one-tap sign-up dialog ()
		</figcaption>
	
</figure>


<p><strong>Note</strong>: <em>This is an interesting password-less solution. Of course, by using it, users are linked to Google, which not everyone will feel comfortable with</em>.</p>

<h3 id="conclusion">Conclusion</h3>

<p>You can do a lot of really cool things when you start using mobile capabilities to help users fill in forms. We need a <strong>mobile-first mindset when building forms</strong>; otherwise, we’ll get stuck on the desktop capabilities we are familiar with.</p>

<p>Again, be careful with the device&rsquo;s capabilities: <strong>always have a fallback solution</strong> in case a sensor fails or the user refuses access. Avoid making those capabilities the only options for those functions (unless you are building a map app that relies on geolocation).</p>

<p>This is the end of a series of two really long articles in which I’ve given you some general UX and usability advice and best practices. In the end, <strong>what matter are your form and your users</strong>. Some things described here might not even work specifically for your users &mdash; who knows? So, whatever you do, don’t take my (or Luke’s) word for it. Test it, with real users, on real devices. Measure it. And test again. <strong>Do some user research and usability testing</strong>. User experience is not only about best practices and magic recipes that you copy and paste. You need to adapt the recipe to make it work for you.</p>

<p>So, in short: Test it. Test it on real devices. Test it with real users.</p>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(lf, ra, al, il)</span>
</div>


              </article>
            </body>
          </html>
---------------
<h1 id="#title_1" >2、视频演讲： 基于 Serverless 架构的小程序开发实践</h1>
张吉
[http://www.infoq.com/cn/presentations/small-program-development-based-on-serverless-architecture?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/small-program-development-based-on-serverless-architecture?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/presentations/small-program-development-based-on-serverless-architecture/zh/mediumimage/zhangji270-1535294425218.jpg"/><p>为了帮助小程序开发者实现业务快速上线，我们利用腾讯云上的资源做了一些探索和尝试。基于 Serverless 架构，我们彻底屏蔽了底层资源，和云函数结合使用，实现了云能力的快速拓展应用。</p> <i>By 张吉</i>
---------------
<h1 id="#title_2" >3、文章： Flink关系型API解读：Table API 与SQL</h1>
王剑
[http://www.infoq.com/cn/articles/flink-api-table-api-and-sql?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/flink-api-table-api-and-sql?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/flink-api-table-api-and-sql/zh/smallimage/image_code-1535217548241.jpg"/><p>本篇文章主要介绍Flink的关系型API。</p> <i>By 王剑</i>
---------------
<h1 id="#title_3" >4、文章： 深入理解JUnit 5的扩展模型</h1>
Uday Tatiraju
[http://www.infoq.com/cn/articles/deep-dive-junit5-extensions?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/deep-dive-junit5-extensions?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/deep-dive-junit5-extensions/zh/smallimage/deep-dive-junit5-extensions-l-1534517379579-1535210036613.jpeg"/><p>JUnit 5是一个模块化和可扩展的测试框架，支持Java 8及更高版本。JUnit 5 Jupiter的扩展模型可用于向JUnit中添加自定义功能。</p> <i>By Uday Tatiraju</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_4" >5、文章： Serverless架构开发与SCF部署实践</h1>
贾凯强
[http://www.infoq.com/cn/articles/Serverless-framework-and-scf-deployment?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/Serverless-framework-and-scf-deployment?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/Serverless-framework-and-scf-deployment/zh/smallimage/cloud-logo-1508587932376-1535363456271.jpeg"/><p>8月18日，腾讯云联合InfoQ举办的云+社区技术沙龙聚焦在了Serverless架构之上。此次沙龙从Serverless架构场景化应用、基于 Serverless 架构的小程序开发、API网关与SCF深度结合应用、对象存储与SCF深度结合应用、享受纯粹的编程乐趣等五大主题内容，探索Serverless技术的应用难点，带领开发者实现无招胜有招。本文整理了讲师演讲精彩内容。</p> <i>By 贾凯强</i>
---------------
<h1 id="#title_5" >6、文章： V神推荐99%容错共识新算法</h1>
Vitalik Buterin
[http://www.infoq.com/cn/articles/vitalik-buterin-proposes-consensus-algorithm?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/vitalik-buterin-proposes-consensus-algorithm?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/vitalik-buterin-proposes-consensus-algorithm/zh/smallimage/software-system-ml-1532598838952-1535217008710.jpeg"/><p>Vitalik最近在他的博客上发布了一篇名为《99%容错共识算法指南》，并表示该算法由计算机科学家Leslie Lamport发明。Vitalik对该共识进行了解释，并对其调整以适用于区块链环境中。</p> <i>By Vitalik Buterin</i> <i> Translated by 姚佳灵</i>
---------------
<h1 id="#title_6" >7、FEX 技术周刊 - 2018/08/27</h1>

[http://fex.baidu.com/blog/2018/08/fex-weekly-27//](http://fex.baidu.com/blog/2018/08/fex-weekly-27//)
作者：zhangtao <br> <h2 id="section">深阅读</h2>

<p><strong>Liftoff: a new baseline compiler for WebAssembly in V8</strong><br />
https://v8project.blogspot.com/2018/08/liftoff.html<br />
V8 v6.9 includes Liftoff, a new baseline compiler for WebAssembly. Liftoff is now enabled by default on desktop systems. This article details the motivation to add another compilation tier and describes the implementation and performance of Liftoff.</p>

<p><strong>Web Performance Made Easy: Google I/O 2018 edition</strong><br />
https://developers.google.com/web/updates/2018/08/web-performance-made-easy<br />
We’ve been pretty busy over the past year trying to figure out how to make the Web faster and more performant. This led to new tools, approaches and libraries that we’d like share with you in this article. In the first part, we’ll show you some optimization techniques we used in practice when developing The Oodles Theater app. In the second part, we’ll talk about our experiments with predictive loading and the new .</p>

<p><strong>Internet Native Applications</strong><br />
https://blog.cloudflare.com/internet-native-applications/<br />
No single technology defines Internet Native Applications. However, I believe the combination of: A rapidly increasing percentage of requests serviced directly from the Edge under 10ms; Near-native speed code on the browser, powered by WebAssembly; Improved Internet protocols like QUIC and HTTP/2. 另附：</p>

<p><strong>Implementing single file Web Components</strong><br />
https://medium.com/content-uneditable/implementing-single-file-web-components-22adeaa0cd17<br />
Probably everyone who knows the Vue framework also heard about its single file components. This super simple idea allows web developers to define the entire code of a component in one file. It’s such a useful solution that an initiative to include this mechanism in browsers has already appeared. However, it seems quite dead as, unfortunately, no progress has been made since August 2017. Nevertheless, looking into this topic and trying to make single file components work in the browsers using the technologies already available was interesting enough to write an article about it!</p>

<p><strong>Apps That Work Natively on the Web and Mobile</strong><br />
https://blog.angular.io/apps-that-work-natively-on-the-web-and-mobile-9b26852495e7<br />
We’re happy to announce an exciting new way to build web and mobile apps with Angular and NativeScript. First, some background: since the beginning of Angular, you could use NativeScript with Angular to build mobile apps.</p>

<p><strong>从红芯事件聊聊浏览器内核（一）</strong><br />
https://juejin.im/post/5b798b0ff265da432e75bd88<br />
通过泄漏的 IE2 和 IE 5.5 源码了解</p>

<p><strong>深入理解JSCore</strong><br />
https://tech.meituan.com/deep_understanding_of_jscore.html<br />
动态化作为移动客户端技术的一个重要分支，一直是业界积极探索的方向。目前业界流行的动态化方案，如Facebook的React Native，阿里巴巴的Weex都采用了前端系的DSL方案，而它们在iOS系统上能够顺利的运行，都离不开一个背后的功臣：JavaScriptCore（以下简称JSCore），它建立起了Objective-C（以下简称OC）和JavaScript（以下简称JS）两门语言之间沟通的桥梁。无论是这些流行的动态化方案，还是WebView Hybrid方案，亦或是之前广泛流行的JSPatch，JSCore都在其中发挥了举足轻重的作用。作为一名iOS开发工程师，了解JSCore已经逐渐成为了必备技能之一。另附：</p>

<p><strong>唯品会的Service Mesh三年进化史</strong><br />
http://calvin1978.blogcn.com/?p=1779<br />
唯品会的服务化体系OSP(Open Service Platform) 在三年前就走上了ServiceMesh的路，每种架构风格，由于各司不同的历史因果，现实状况，以及对采纳新架构的诉求和希望，都会有不同的实现路线。我们的SM在实战中一点点演化而来，与 Istio由谷歌IBM的超级架构师们画出来的架构也有不同之处。希望通过分享我们的演进过程，能给各司里同样在往SM演进中的架构师们一个参考。</p>

<p><strong>WebAssembly vs. the world. Should you use WebAssembly?</strong><br />
https://blog.sqreen.io/webassembly-performance/<br />
WebAssembly is known for its speed capabilities and this article will put it to the test to better understand what are the best applications to start using WebAssembly today. We will compare the performance of WebAssembly with C/C++, Rust, and TypeScript. Will WebAssembly kill JavaScript? Maybe not just yet. 另附：.</p>

<p><strong>Advanced effects with CSS background blend modes</strong><br />
https://blog.logrocket.com/advanced-effects-with-css-background-blend-modes-4b750198522a<br />
This article will focus on background-blend-mode, the property with the most widespread support, and how you can use it today to create eye-catching backgrounds and photo effects for your website that once were only possible in Photoshop.</p>

<p><strong>Async data loading in React</strong><br />
https://medium.com/@ghengeveld/async-data-loading-in-react-94661e23cd3d<br />
The common place to perform data fetching in a React component is in the componentDidMount lifecycle method. Just run fetch and use setState to store the result. This is simple enough (and very effective) but leaves a lot to be desired. What about showing some sort of loading indicator? What about error handling? In practice you’ll want to enhance your fetch with a bunch of metadata. You should also consider promise cancellation on unmount, as well as deal with race conditions between consecutive fetches (FiFo).</p>

<p><strong>Behind the scenes of my latest book on JavaScript</strong><br />
http://2ality.com/2018/08/impatient-js.html<br />
This blog post takes you behind the scenes of my latest book, “JavaScript for impatient programmers” (which I’ll henceforth abbreviate as “Impatient JS”). It describes: How I chose what to write about; My techniques for explaining topics; Tools I used for creating ebooks and other artifacts; How I unit-tested the code shown in the book and in its quizzes.</p>

<p><strong>Web Reading Mode: The non-standard rendering mode</strong><br />
https://www.ctrl.blog/entry/browser-reading-mode-parsers<br />
All the leading web browsers, except for Google Chrome, include a separate “reading mode” that extracts the main content from pages, reformats it to be more readable, and hides distractions like advertisements, comments, and even page navigation. This separate rendering mode isn’t governed by any standards and as such it behave differently from web browser to web browser. So what is a web developer to do to properly support this distinctly separate and non-standard rendering mode? This article is part one in a series on web reading mode and reading mode parsers. The article is broken up into multiple parts as each part is written for a slightly different audience.</p>

<p><strong>Small Assets without the Headache</strong><br />
https://elm-lang.org/blog/small-assets-without-the-headache<br />
If you want faster page loads, you want smaller assets. But it feels quite complicated to get small assets with JavaScript. Should I switch from React to Preact? Do I have tree shaking set up properly? Will my dependencies even work with tree shaking? Do I need to do something special with my dependencies now? And will code splitting help as well? How does that work? It feels overwhelming even talking about it! Elm 0.19 makes our assets really small without the headache. A bunch of projects have implemented this “RealWorld App” that is a decent size application.</p>

<p><strong>GraphQL Server Tutorial with Apollo Server and Express</strong><br />
https://www.robinwieruch.de/graphql-apollo-server-tutorial/<br />
In the following, you are going to implement the server-side of such architecture by using GraphQL and Apollo Server. Whereas GraphQL is only the query language which got implemented as reference implementation in JavaScript by Facebook, Apollo Server builds up on top of it to simplify building GraphQL servers in JavaScript. 另附：</p>

<p><strong>First steps with TensorFlow.js</strong><br />
https://aralroca.com/2018/08/24/first-steps-with-tensorflow-js/<br />
Nevertheless, we don’t need a deep knowledge about machine learning to use some existing models. We can use some libraries like Keras, Tensorflow or TensorFlow.js. We are going to see here how to create basic AI models and use more sophisticated models with TensorFlow.js. Although it’s not required a deep knowledge, we are going to explain few concepts.</p>

<p><strong>Serverless Best Practices</strong><br />
https://medium.com/@PaulDJohnston/serverless-best-practices-b3c97d551535<br />
And remember that best practices are not “the only practices”. Best practices rely on a set of underlying assumptions. If those assumptions don’t fit your use case, then those best practices may not fit. 另附：.</p>

<p><strong>How to extract a data-rich service from a monolith</strong><br />
https://martinfowler.com/articles/extract-data-rich-service.html<br />
When breaking monoliths into smaller services, the hardest part is actually breaking up the data that lives in the database of the monolith. In this article, I will be talking about a pattern, which is a series of steps, for extracting a data-rich service from a monolith while causing minimum disruption to the service consumers.</p>

<p><strong>Coding with Clarity: Part II</strong><br />
https://alistapart.com/article/coding-with-clarity-part-ii<br />
As any developer who works with other developers can attest, if code is unclear, problems occur. In  of this series, I went over some principles to improve clarity in our code to prevent problems that can arise from unclear code. As our apps get larger, clarity becomes even more important, and we need to take extra care to ensure that our code is easy to read, understand, and modify or extend. This article discusses some more-advanced principles related to object-oriented programming (OOP) to improve clarity in larger apps.</p>

<p><strong>Don’t Do This in Production</strong><br />
https://stephenmann.io/post/dont-do-this-in-production/<br />
This blog is about building production ready applications. It will do this from every aspect: from infrastructure automation, to testing, to design, to debugging, to documentation, to development process, to security. Every post will stand on its own feet, ready to use in the real world – ready to use in production.</p>

<p><strong>The Future of Notebooks: Lessons from JupyterCon</strong><br />
http://willcrichton.net/notes/lessons-from-jupytercon/<br />
Over the last two days at .</p>

<h2 id="section-1">新鲜货</h2>

<p><strong>中国首届React开发者大会 &amp; 第四届 FEDAY 会议资料</strong><br />
https://react.w3ctech.com/?from=timeline#schedule<br />
https://mp.weixin.qq.com/s?__biz=MzA5NTM2MTEzNw==&amp;mid=2736712821&amp;idx=1&amp;sn=8bb2eb1ec0b9da6349fadd27b1aabd23<br />
另附：</p>

<p><strong>More Than A Billion Downloads of Node.js</strong><br />
https://medium.com/@nodejs/more-than-a-billion-downloads-of-node-js-952a8a98eb42<br />
The application platform known as Node.js surpassed one billion downloads and is now officially a part of the three comma club. 另附：.</p>

<p><strong>GitLab 11.2 released with live preview in the Web IDE and Android project import</strong><br />
https://about.gitlab.com/2018/08/22/gitlab-11-2-released/<br />
We are super excited to deliver new features with 11.2 that will help you get started and iterate faster. Today we deliver enhancements to the Web IDE, support for manifest files to import Android projects, and enable custom project templates.</p>

<p><strong>Introducing Ghost 2.0</strong><br />
https://blog.ghost.org/2-0/<br />
A powerful new editor, multi-language support, custom homepages, dynamic routes, custom structures and much more. 另附：.</p>

<p><strong>The Book “Computer Networks: A Systems Approach” is now open source</strong><br />
https://github.com/SystemsApproach/book<br />
This site contains source text for Computer Networks: A Systems Approach, now available under terms of the Creative Commons (CC BY 4.0) license. The community is invited to contribute corrections, improvements, updates, and new material under the same terms. Like many open source software projects, this one has been seeded with once restricted content: the 5th edition of Peterson and Davie, copyrighted by Elsevier. Our hope is that open sourcing this material will both make it widely available and serve as an attractor for new content: updating what’s already there, expanding it to cover new topics, and augmenting the text with additional teaching collateral.</p>

<p><strong>Bing.com runs on .NET Core 2.1</strong><br />
https://blogs.msdn.microsoft.com/dotnet/2018/08/20/bing-com-runs-on-net-core-2-1/<br />
Our production data resonates with the significant performance improvements in .NET Core 2.1 (as compared to both .NET Core 2.0 and .NET Framework 4.7.2). The graph below tracks our internal server latency over the last few months. The Y axis is the latency (actual values omitted), and the final precipitous drop (on June 2) is the deployment of .NET Core 2.1! That is a 34% improvement, all thanks to the hard work of the .NET community!</p>

<p><strong>FASTER: A Fast Key-Value Store From Microsoft Research</strong><br />
https://github.com/Microsoft/FASTER<br />
Available in both C# and C++ versions, FASTER uses a unique ‘hybrid record log’ design that combines a traditional persistent log with in-place updates, to shape the memory working set and retain performance. 附：.</p>

<p><strong>WorkerDOM</strong><br />
https://github.com/ampproject/worker-dom<br />
可以在 worker 里使用 DOM 的 api</p>

<p><strong>Layui</strong><br />
https://github.com/sentsin/layui/<br />
返璞归真：身处在前端社区的繁荣之下，我们都在有意或无意地追逐。而 layui 偏偏回望当初，奔赴在返璞归真的漫漫征途，自信并勇敢着，追寻于原生态的书写指令，试图以最简单的方式诠释高效。双面体验：拥有双面的不仅是人生，还有 layui。一面极简，一面丰盈。极简是视觉所见的外在，是开发所念的简易。丰盈是倾情雕琢的内在，是信手拈来的承诺。一切本应如此，简而全，双重体验。</p>

<p><strong>svg-3d-builder</strong><br />
https://github.com/captainwz/svg-3d-builder<br />
This framework aims at creating 3d models with SVG and to provide a concise API. It is purely developed with concepts of two-dimensions. One of its essential implementations is Bezier in both curve and surface. It is one thing to describe them with mathematic equations, but another thing to illustrate them with computer graphics.</p>

<p><strong>Fitty, Snugly text resizing</strong><br />
https://github.com/rikschennink/fitty<br />
Scales up (or down) text so it fits perfectly to its parent container. Ideal for flexible and responsive websites. 另附：.</p>

<p><strong>Immer</strong><br />
https://github.com/mweststrate/immer<br />
Create the next immutable state tree by simply modifying the current tree.</p>

<p><strong>Johnny-Five v1.0</strong><br />
http://johnny-five.io/news/v1_0/<br />
Johnny-Five is the JavaScript Robotics &amp; IoT Platform. Released by Bocoup in 2012, Johnny-Five is maintained by a community of passionate software developers and hardware engineers. Over 75 developers have made contributions towards building a robust, extensible and composable ecosystem.</p>

<p><strong>Ajax</strong><br />
https://github.com/fdaciuk/ajax<br />
Ajax module in Vanilla JS.  You can use this module with AMD, CommonJS or just like a method of window object!</p>

<p><strong>Stimulus 1.1 Released</strong><br />
https://github.com/stimulusjs/stimulus/releases/tag/v1.1.0<br />
Stimulus is a JavaScript framework with modest ambitions. It doesn’t seek to take over your entire front-end—in fact, it’s not concerned with rendering HTML at all. Instead, it’s designed to augment your HTML with just enough behavior to make it shine.</p>

<p><strong>NeutralinoJs</strong><br />
https://github.com/neutralinojs/neutralinojs<br />
NeutralinoJs is a portable and lightweight framework which lets you to develop apps with native functions that can run inside web browsers. In electron and NWjs you have to install NodeJs and hundreds of dependency libraries. Embedded Chromium and Node creates large overhead and makes even simple apps like “hello world” considerable in size. Neutralino offers a solution for this issue.</p>

<p><strong>webview</strong><br />
https://github.com/zserge/webview<br />
A tiny cross-platform webview library for C/C++/Golang to build modern cross-platform GUIs. Also, there are Rust bindings, Python bindings, Nim bindings, Haskell and C# bindings available. 附一个基于它的作品：.</p>

<p><strong>Home Assistant</strong><br />
https://www.home-assistant.io/<br />
Open source home automation that puts local control and privacy first. Powered by a worldwide community of tinkerers and DIY enthusiasts. Perfect to run on a Raspberry Pi or a local server.</p>

<p><strong>Pyodide</strong><br />
https://github.com/iodide-project/pyodide<br />
The Python scientific stack, compiled to WebAssembly. It provides transparent conversion of objects between Javascript and Python. When inside a browser, this means Python has full access to the Web APIs.</p>

<p><strong>PyPy.js</strong><br />
https://pypyjs.org/<br />
PyPy.js is an experiment in building a fast and compliant python environment for the web. It uses the PyPy python interpreter, compiled for the web via emscripten, with a custom JIT backend that emits asm.js code at runtime.</p>

<p><strong>Redis will remain BSD licensed</strong><br />
http://antirez.com/news/120<br />
Today a page about the new .</p>

<h2 id="section-2">设计</h2>

<p><strong>前馈：让功能找到用户；让用户体验美好「自然交互 1」</strong><br />
https://zhuanlan.zhihu.com/p/41952711<br />
在人机交互过程中，如何促使人和机/系统在合适场景、合适时间和合适用户上发生交互，是非常重要的课题。但当下数字设备的人机交互中，却存在很大的矛盾，主要来源于以下两点：在物理世界中，一个设备所拥有的功能是存在一定物理极限的，像瑞士军刀一样具备几十种功能的产品已是特例；在数字世界中，功能增长却没有明确的天花板，再加上能无缝访问互联网的设备，基本提供无限多的功能，例如：打开支付宝，享受成千上万种服务；与 50 年前相比，在如今信息爆炸的时代，人们每天接触的信息量早已跃升好几个量级，然而我们的认知能力却与 50 年前无异，甚至和几百年前的人类没有本质差异。
所以，人类认知进化的龟速，远远跟不上信息爆炸的光速。前馈：以设计的方式解决这对日益严重的矛盾，通过自然的人机交互，改变以往「让用户找到功能」的老路，我们探索「让功能找到用户」的新路。</p>

<p><strong>Experience Is Everything – The Ultimate UX Guide</strong><br />
https://www.toptal.com/designers/ux/the-ultimate-ux-guide<br />
User experience (UX) design experts have a deep understanding of design, technology, and human psychology. What makes a product great? What keeps people coming back? What drives them away? A well-thought-out UX design process, spearheaded by a seasoned UX professional, will help you strike the right balance and keep users coming back for more.</p>

<p><strong>Design is not Science, Art or Engineering</strong><br />
https://uxdesign.cc/design-is-not-science-art-or-engineering-5e8d2f499494<br />
What the hell is design? The following is a list of summary from some books I read, with my understanding. Bibliography is at the end.</p>

<p><strong>Here’s everything I’ve learned from designing 10,000+ UI screens as a lead product designer</strong><br />
https://medium.com/ux-power-tools/heres-everything-i-ve-learned-from-designing-10-000-ui-screens-as-a-lead-product-designer-7d2810bee810<br />
I learned all of this from amazing designers like you, fantastic mentors, and lots of trial and error. If you learn something from this article, share it with another designer. 另附：.</p>

<p><strong>UX Design Trends For 2018</strong><br />
https://www.lollypop.design/blog/2018/august/ux-design-trends-for-2018/<br />
With all that said, we can’t be more thrilled to announce that this year gave birth to UX 2.0! It’s brand new and is a better version of yesteryear’s UX. UX 2.0 comes with a number of new trends that can provide a frictionless experience, smarter personalization, and technology such as augmented reality, virtual reality, and voice assistance.</p>

<p><strong>Mindful Design • Part 1</strong><br />
https://blog.prototypr.io/mindful-design-part-1-b0f6282c455a<br />
In these Mindful Design series (yes, there will be more than one article) I will be exploring how mindfulness principles can be applied in a designer’s workflow.</p>

<h2 id="section-3">产品及其它</h2>

<p><strong>This AI is bad at drawing but will try anyways</strong><br />
http://aiweirdness.com/post/177091486527/this-ai-is-bad-at-drawing-but-will-try-anyways<br />
There was a  recently where a research team trained a machine learning algorithm (a GAN they called AttnGAN) to generate pictures based on written descriptions. It’s like Visual Chatbot in reverse. When it was just trained to generate pictures of birds, it did pretty well, actually.</p>

<p><strong>Intro to Augur</strong><br />
https://litepaper.com/resources/intro-to-augur<br />
Augur is a predictions market built on  ETHEREUM. Its entire premise is to create a decentralized hub where users can collectively bet on what the future might look like. Currently, prediction industries - like the stock market or weather forecasting - rely on small groups of experts. In Augur’s vision, it wants to let anyone have a go at guessing what tomorrow brings. 另附： </p>

<p><strong>巨头布局下的编程教育生态</strong><br />
http://www.geekpark.net/news/232238<br />
8 月 17 日，由教育部主办，Google、清华大学等承办中美青年创客大赛落下帷幕，参赛的大学生们「各显神通」，获奖的诸多作品都以人工智能为底色，有能识别水质，有的能监测糖尿病患者状态。无独有偶，8 月 12 日索尼中国发布了与索尼可编程教育机器人 KOOV 配合使用的教材及教育者资源包，并已在 11 所小学试讲。索尼中国把编程教育的下一步布局瞄准了小学生。目前，除了颇受资本青睐的编程猫、小码王等创业型教育公司在这个新赛道上开疆拓土外，索尼、谷歌等行业巨头们也开始纷纷布局。</p>

<p><strong>创业、艺术家和量子物理</strong><br />
https://mp.weixin.qq.com/s?__biz=MzUyMDQ5NzI5Mg==&amp;mid=2247498476&amp;idx=1&amp;sn=d16c77c1e91bea434bd781ec5166648b<br />
“科学和艺术在山脚下分开行走，最后在美学的山顶相遇。”这该是怎样一种奇景？作者综述了创业、艺术家、与量子物理，提炼出了一些通达各个领域的，关于“美”的底层规律，很是新颖奇特。</p>

<p>– THE END –</p>
---------------
<h1 id="#title_7" >8、Amazon Aurora Serverless MySQL已正式可用</h1>
Steef-Jan Wiggers
[http://www.infoq.com/cn/news/2018/08/aurora-mysql-serverless-ga?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/08/aurora-mysql-serverless-ga?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Amazon Aurora是AWS定制的MySQL和PostgreSQL兼容数据库，最近提供了新的功能——Aurora Serverless MySQL。亚马逊去年首次在AWS re:Invent上展示了这种无服务器功能的预览版。</p> <i>By Steef-Jan Wiggers</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_8" >9、Docker Desktop添加对Kubernetes的支持</h1>
Matt Campbell
[http://www.infoq.com/cn/news/2018/08/docker-desktop-kubernetes?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/08/docker-desktop-kubernetes?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Docker在其stable频道发布了Windows和Mac平台下Docker Desktop对Kubernetes的支持。Kubernetes也得到了Docker Enterprise的支持，允许我们将相同的镜像部署到两个系统中。它还包括对Docker Compose的支持，允许我们使用compose文件部署到Kubernetes，可以将其作为kubeconfig文件的替代方案。</p> <i>By Matt Campbell</i> <i> Translated by 张卫滨 </i>
---------------
<h1 id="#title_9" >10、Uber开源其大规模指标平台M3</h1>
Hrishikesh Barua
[http://www.infoq.com/cn/news/2018/08/uber-metrics-m3?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/08/uber-metrics-m3?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Uber的工程团队发布了其开源指标平台M3，该平台已经在Uber内部使用多年。构建这个平台是为了取代基于Graphite的系统，M3提供了集群管理、聚合、收集、存储管理、分布式时序数据库（TSDB）以及带有其查询语言M3QL的查询引擎。</p> <i>By Hrishikesh Barua</i> <i> Translated by 张卫滨 </i>
---------------
<h1 id="#title_10" >11、产品思维而不是项目思维</h1>
Ben Linders
[http://www.infoq.com/cn/news/2018/08/think-products?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/08/think-products?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>组织结构围绕产品来构建，负责整个工作过程。反转康威定律，围绕产品建立长期团队，保证稳定性，简化管理和工作优先级制定。回顾是一个强大的产品管理工具；它们可以提供继续工作的信心，并能帮助你在组织可能面临风险或损失的情况下快速调整方向。</p> <i>By Ben Linders</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_11" >12、币圈凉了，链圈一切刚刚好</h1>
前哨小兵甲
[http://www.infoq.com/cn/news/2018/08/block-chain-community-well?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/08/block-chain-community-well?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>其实无论币圈热闹还是冷清，总还有一批怀有理想的技术人一直在默默的钻研试验区块链技术，希望形成普罗大众需要的完整的、可用的产品，能解决实际生活中的问题。 金融行业长期在区块链技术的研发与投资方面占据主导地位，区块链活动早在几年前就已经开始，且一直通过概念验证、试点以及测试项目的形式持续推进。金融服务行业也似乎最接近生产就绪阶段。 区块链作为一项基础技术，与人工智能、大数据一样，潜力不容被忽视。放眼整个全球的区块链赛道，各大企业都希望能抢占到区块链市场的先发优势，挖掘到区块链这片新大陆上最大的红利和财富。我们整理了一份清单，囊括一部分主要的创新领域的领导者</p> <i>By 前哨小兵甲</i>
---------------