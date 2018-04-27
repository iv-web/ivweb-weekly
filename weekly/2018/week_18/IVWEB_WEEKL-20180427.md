## 文章索引
1、 <a href="#1measuring-websites-with-mobile-first-optimization-tools" >Measuring Websites With Mobile-First Optimization Tools</a><br/>
2、 <a href="#2文章-敏捷开发&远程团队你应该知道的六条生产力秘诀" >文章： 敏捷开发&远程团队——你应该知道的六条生产力秘诀</a><br/>
3、 <a href="#3文章-区块链创新之卡尔达诺cardano" >文章： 区块链创新之卡尔达诺（Cardano）</a><br/>
4、 <a href="#4文章-实时音视频的架构设计" >文章： 实时音视频的架构设计</a><br/>
5、 <a href="#5百度深度学习公开课首场爆满开发者收获最强进阶宝典" >百度“深度学习公开课”首场爆满，开发者收获最强进阶“宝典”</a><br/>
6、 <a href="#6英孚教育全面上云与serverless构建之路" >英孚教育全面上云与Serverless构建之路</a><br/>
7、 <a href="#7sauce-labs将分析和扩展调试添加到其持续测试云中" >Sauce Labs将分析和扩展调试添加到其持续测试云中</a><br/>
8、 <a href="#8spring-cloud-stream-20发布专注于性能灵活性和一致性" >Spring Cloud Stream 2.0发布，专注于性能、灵活性和一致性</a><br/>
9、 <a href="#9精益敏捷采购的外包" >精益敏捷采购的外包</a><br/>
10、 <a href="#10gcp发布kaniko在非特权容器和kubernetes中构建容器镜像的工具" >GCP发布Kaniko：在非特权容器和Kubernetes中构建容器镜像的工具</a><br/><h1 id="#title_0" >1、Measuring Websites With Mobile-First Optimization Tools</h1>
Jon Raasch
[https://www.smashingmagazine.com/2018/04/mobile-first-optimization-tools/](https://www.smashingmagazine.com/2018/04/mobile-first-optimization-tools/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/04/mobile-first-optimization-tools/" />
              <title>Measuring Websites With Mobile-First Optimization Tools</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>Measuring Websites With Mobile-First Optimization Tools</h1>
                  
                    
                    <address>Jon Raasch</address>
                  
                  <time datetime="2018-04-26T13:40:03&#43;02:00" class="op-published">2018-04-26T13:40:03+02:00</time>
                  <time datetime="2018-04-26T14:11:08&#43;00:00" class="op-modified">2018-04-26T14:11:08+00:00</time>
                </header>
                <p>Performance on mobile can be particularly challenging: underpowered devices, slow networks, and poor connections are some of those challenges. With more and more users migrating to mobile, the rewards for mobile optimization are great. Most workflows have already adopted mobile-first design and development strategies, and it’s time to apply a similar mindset to performance.</p>

<p>In this article, we’ll take a look at studies linking page speed to real-world metrics, and discuss the specific ways mobile performance impacts your site. Then we’ll explore benchmarking tools you can use to measure your website’s mobile performance. Finally, we’ll work with tools to help identify and remove the code debt that bloats and weighs down your site.</p>

<div class="c-felix-the-cat">
<h4>Responsive Configurators</h4>
<p>How would you design a responsive car configurator? How would you deal with accessibility, navigation, real-time previews, interaction and performance? Let’s figure it out. </p>
</div>

<h3>Why Performance Matters</h3>

<p>The benefits of performance optimization are well-documented. In short, performance matters because users prefer faster websites. But it’s more than a qualitative assumption about user experience. There are a variety of studies that directly link reduced load times to increased conversion and revenue, such as the now decade-old  that showed each 100ms of latency led to a 1% drop in sales.</p>

<h4>Page Speed, Bounce Rate & Conversion</h4>

<p>In the data world, poor performance leads to an increased bounce rate. And in the mobile world that bounce rate may occur sooner than you think. A  shows that 53% of mobile users abandon a site that takes more than 3 seconds to load.</p>

<p>That means if your site loads in 3.5 seconds, over half of your potential users are leaving (and most likely visiting a competitor). That may be tough to swallow, but it is as much a problem as it is an opportunity. If you can get your site to load more quickly, you are potentially doubling your conversion. And if your conversion is even indirectly linked to profits, you’re doubling your revenue.</p>



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


<h4>SEO And Social Media</h4>

<p>Beyond reduced conversion, slow load times create secondary effects that diminish your inbound traffic. Search engines already use  for mobile searches as of July 2018.</p>

<p>Social media outlets have begun factoring page speed in their algorithms as well. In August 2017,  that it would roll out specific changes to the newsfeed algorithm for mobile devices. These changes include page speed as a factor, which means that slow websites will see a decline in Facebook impressions, and in turn a decline in visitors from that source.</p>

<p>Search engines and social media companies aren’t punishing slow websites on a whim, they’ve made a calculated decision to improve the experience for their users. If two websites have effectively the same content, wouldn’t you rather visit one that loads faster?</p>

<p>Many websites depend on search engines and social media for a large portion of their traffic. The slowest of these will have an exacerbated problem, with a reduced number of visitors coming to their site, and over half of those visitors subsequently abandoning.</p>

<p>If the prognosis sounds alarming, that’s because it is! But the good news is that there are a few concrete steps you can take to improve your page speeds. Even the slowest sites can get “sub three seconds” with a good strategy and some work.</p>

<h3>Profiling And Benchmarking Tools</h3>

<p>Before you begin optimizing, it’s a good idea to take a snapshot of your website’s performance. With profiling, you can determine how much progress you will need to make. Later, you can compare against this benchmark to quantify the speed improvements you make.</p>

<p>There are a number of tools that assess a website’s performance. But before you get started, it’s important to understand that no tool provides a perfect measurement of client-side performance. Devices, connection speeds, and web browsers all impact performance, and it is impossible to analyze all combinations. Additionally, any tool that runs on your personal device can only approximate the experience on a different device or connection.</p>

<p>In one sense, whichever tool you use can provide meaningful insights. As long as you use the same tool before and after, the comparison of each should provide a decent snapshot of performance changes. But certain tools are better than others.</p>

<p>In this section, we’ll walk through two tools that provide a profile of how well your website performs in a mobile environment.</p>

<p><strong>Note</strong>: <em>If can be difficult to benchmark an entire site, so I recommend that you choose one or two of your most important pages for benchmarking.</em></p>

<h4>Lighthouse</h4>

<p>One of the more useful tools for profiling mobile performance is Google’s . It’s a nice starting point for optimization since it not only analyzes page performance but also provides insights into specific performance issues. Additionally, Lighthouse provides high-level suggestions for speed improvements.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c8ef44c0-c9f5-41da-9560-82259a44ff23/mobile-first-optimization-img-1.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c8ef44c0-c9f5-41da-9560-82259a44ff23/mobile-first-optimization-img-1.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c8ef44c0-c9f5-41da-9560-82259a44ff23/mobile-first-optimization-img-1.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c8ef44c0-c9f5-41da-9560-82259a44ff23/mobile-first-optimization-img-1.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c8ef44c0-c9f5-41da-9560-82259a44ff23/mobile-first-optimization-img-1.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c8ef44c0-c9f5-41da-9560-82259a44ff23/mobile-first-optimization-img-1.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c8ef44c0-c9f5-41da-9560-82259a44ff23/mobile-first-optimization-img-1.png"
			sizes="100vw"
			alt="Lighthouse audit tab"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Lighthouse in the Google’s Web Developer Tools. ()
		</figcaption>
	
</figure>


<p>Lighthouse is available in the Audits tab of the Chrome Developer Tools. To get started, open the page you want to optimize in Chrome Dev Tools and perform an audit. I typically perform all the audits, but for our purposes, you only need to check the ‘Performance’ checkbox:</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e937c7ed-9970-4480-8847-4b1a009b6943/mobile-first-optimization-img-2.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e937c7ed-9970-4480-8847-4b1a009b6943/mobile-first-optimization-img-2.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e937c7ed-9970-4480-8847-4b1a009b6943/mobile-first-optimization-img-2.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e937c7ed-9970-4480-8847-4b1a009b6943/mobile-first-optimization-img-2.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e937c7ed-9970-4480-8847-4b1a009b6943/mobile-first-optimization-img-2.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e937c7ed-9970-4480-8847-4b1a009b6943/mobile-first-optimization-img-2.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e937c7ed-9970-4480-8847-4b1a009b6943/mobile-first-optimization-img-2.png"
			sizes="100vw"
			alt="Lighthouse audit selection"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			All the audits are useful, but we’ll only need the Performance audit. ()
		</figcaption>
	
</figure>


<p>Lighthouse focuses on mobile, so when you run the audit, Lighthouse will pop your page into the inspector’s responsive viewer and throttle the connection to simulate a mobile experience.</p>

<h5>Lighthouse Reports</h5>

<p>When the audit finishes, you’ll see an overall performance score, a timeline view of how the page rendered over time, as well as a variety of metrics:</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/45f9e814-2293-43e7-8204-8f74105fb9f9/mobile-first-optimization-img-3.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/45f9e814-2293-43e7-8204-8f74105fb9f9/mobile-first-optimization-img-3.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/45f9e814-2293-43e7-8204-8f74105fb9f9/mobile-first-optimization-img-3.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/45f9e814-2293-43e7-8204-8f74105fb9f9/mobile-first-optimization-img-3.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/45f9e814-2293-43e7-8204-8f74105fb9f9/mobile-first-optimization-img-3.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/45f9e814-2293-43e7-8204-8f74105fb9f9/mobile-first-optimization-img-3.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/45f9e814-2293-43e7-8204-8f74105fb9f9/mobile-first-optimization-img-3.png"
			sizes="100vw"
			alt="Lighthouse performance audit results"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			In the performance audit, pay attention to the first meaningful paint. ()
		</figcaption>
	
</figure>


<p>It’s a lot of information, but one report to emphasize is the <em>first meaningful paint</em>, since that directly influences user bounce rates. You may notice that the tool doesn’t even list the total load time, and that’s because it rarely matters for user experience.</p>


  <div id="sponsors-article" data-impression="true" class="c-promo-box c-promo-box--ad sponsors hidden" data-audience="non-subscriber" data-remove="true"></div>



<p>Mobile users expect a first view of the page very quickly, and it may be some time before they scroll to the lower content. In the timeline above, the first paint occurs quickly at 1.3 seconds, then a full above-the-fold content paint occurs at 3.9 seconds. The user can now engage with the above-the-fold content, and anything below-the-fold can take a few seconds longer to load.</p>

<p>Lighthouse’s first meaningful paint is a great metric for benchmarking, but also take a look at the opportunities section. This list helps to identify the key problem areas of your site. Keep these recommendations on your radar, since they may provide your biggest improvements.</p>

<h5>Lighthouse Caveats</h5>

<p>While Lighthouse provides great insights, it is important to bear in mind that it only simulates a mobile experience. The device is simulated in Chrome, and a mobile connection is simulated with throttling. Actual experiences will vary.</p>

<p>Additionally, you may notice that if you run the audit multiple times, you will get different reports. That’s again because it is simulating the experience, and variances in your device, connection, and the server will impact the results. That said, you can still use Lighthouse for benchmarking, but it is important that you run it several times. It is more relevant as a range of values than a single report.</p>

<h4>WebPageTest</h4>

<p>In order to get an idea of how quickly your page loads in an actual mobile device, use WebPageTest. One of the nice things about WebPageTest is that it tests on a variety of <em>real</em> devices. Additionally, it will perform the test a number of times and take the average to provide a more accurate benchmark.</p>

<p>To get started, navigate to , enter the URL for the page you want to test and then select the mobile device you’d like to use for testing. Also, open up the advanced settings and change the connection speed. I like testing at Fast 3G, because even when users are connected to LTE the connection speed is rarely LTE (#sad):</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/50eeebae-ac59-4b43-8f5a-5ba8eaae9043/mobile-first-optimization-img-4.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/50eeebae-ac59-4b43-8f5a-5ba8eaae9043/mobile-first-optimization-img-4.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/50eeebae-ac59-4b43-8f5a-5ba8eaae9043/mobile-first-optimization-img-4.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/50eeebae-ac59-4b43-8f5a-5ba8eaae9043/mobile-first-optimization-img-4.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/50eeebae-ac59-4b43-8f5a-5ba8eaae9043/mobile-first-optimization-img-4.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/50eeebae-ac59-4b43-8f5a-5ba8eaae9043/mobile-first-optimization-img-4.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/50eeebae-ac59-4b43-8f5a-5ba8eaae9043/mobile-first-optimization-img-4.png"
			sizes="100vw"
			alt="WebPageTest advanced settings form"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			WebPageTest provides actual mobile devices for profiling. ()
		</figcaption>
	
</figure>


<p>After submitting the test (and waiting for any queue), you’ll get a report on the speed of the page:</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7a75f382-afc6-4fce-9e7d-e53d0541e133/mobile-first-optimization-img-5.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7a75f382-afc6-4fce-9e7d-e53d0541e133/mobile-first-optimization-img-5.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7a75f382-afc6-4fce-9e7d-e53d0541e133/mobile-first-optimization-img-5.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7a75f382-afc6-4fce-9e7d-e53d0541e133/mobile-first-optimization-img-5.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7a75f382-afc6-4fce-9e7d-e53d0541e133/mobile-first-optimization-img-5.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7a75f382-afc6-4fce-9e7d-e53d0541e133/mobile-first-optimization-img-5.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7a75f382-afc6-4fce-9e7d-e53d0541e133/mobile-first-optimization-img-5.png"
			sizes="100vw"
			alt="WebPageTest profiling results"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			In WebPageTest’s results, pay attention to the start render and first byte. ()
		</figcaption>
	
</figure>


<p>The summary view consists of a short list of metrics and links to timelines. Again, the value of the start render is more important than the load time. The first byte is useful for analyzing the server response speed. You can also dig into the more in-depth reports for additional insights.</p>

<h4>Benchmarking</h4>

<p>Now that you’ve profiled your page in Lighthouse and WebPageTest, it’s time to record the values. These benchmarks will provide a useful comparison as you optimize your page. If the metrics improve, your changes are worthwhile. If they stay static (or worse decline), you’ll need to rethink your strategy.</p>

<p>Lighthouse results are simulated which makes it less useful for benchmarking and more useful for in-depth reports and optimization suggestions. However, Lighthouse’s performance score and first meaningful paint are nice benchmarks so run it a few times and take the median for each.</p>

<p>WebPageTest’s values are more reliable for benchmarking since it tests on real devices, so these will be your primary benchmarks. Record the value for the first byte, start to render, and overall load time.</p>

<h3>Bloat Reduction</h3>

<p>Now that you’ve assessed the performance of your site, let’s take a look at a tool that can help reduce the size of your files. This tool can identify extra, unnecessary pieces of code that bloat your files and cause resources to be larger than they should.</p>

<p>In a perfect world, users would only download the code that they actually need. But the production and maintenance process can lead to unused artifacts in the codebase. Even the most diligent developers can forget to remove pieces of old CSS and JavaScript while making changes. Over time these bits of dead code accumulate and become unnecessary bloat.</p>

<p>Additionally, certain resources are intended to be cached and then used throughout multiple pages, such as a site-wide stylesheet. Site-wide resources often make sense, but how can you tell when a stylesheet is mostly underused?</p>

<h4>The Coverage Tab</h4>

<p>Fortunately, Chrome Developer Tools has a tool that helps assess the bloat in files: . The Coverage tab analyzes code coverage as you navigate your site. It provides an interface that shows how much code in a given CSS or JS file is actually being used.</p>

<p>To access the Coverage tab, open up Chrome Developer Tools, and click on the three dots in the top right. Navigate to ‘More Tools’&nbsp;&rarr;&nbsp;‘Coverage’.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/30adac8e-db4c-4d43-a96e-3dc2a5433fa6/mobile-first-optimization-img-6.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/30adac8e-db4c-4d43-a96e-3dc2a5433fa6/mobile-first-optimization-img-6.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/30adac8e-db4c-4d43-a96e-3dc2a5433fa6/mobile-first-optimization-img-6.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/30adac8e-db4c-4d43-a96e-3dc2a5433fa6/mobile-first-optimization-img-6.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/30adac8e-db4c-4d43-a96e-3dc2a5433fa6/mobile-first-optimization-img-6.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/30adac8e-db4c-4d43-a96e-3dc2a5433fa6/mobile-first-optimization-img-6.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/30adac8e-db4c-4d43-a96e-3dc2a5433fa6/mobile-first-optimization-img-6.png"
			sizes="100vw"
			alt="Access the Coverage tab by clicking on More tools and then Coverage"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The Coverage tab is a bit hidden in the web developer tools console. ()
		</figcaption>
	
</figure>


<p>Next, start instrumenting coverage by clicking the reload button on the right. That will reload the page and begin the code coverage analysis. It brings up a report similar to this:</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5a34d25f-e984-45a9-be6f-d99286f7858b/mobile-first-optimization-img-7.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5a34d25f-e984-45a9-be6f-d99286f7858b/mobile-first-optimization-img-7.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5a34d25f-e984-45a9-be6f-d99286f7858b/mobile-first-optimization-img-7.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5a34d25f-e984-45a9-be6f-d99286f7858b/mobile-first-optimization-img-7.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5a34d25f-e984-45a9-be6f-d99286f7858b/mobile-first-optimization-img-7.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5a34d25f-e984-45a9-be6f-d99286f7858b/mobile-first-optimization-img-7.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5a34d25f-e984-45a9-be6f-d99286f7858b/mobile-first-optimization-img-7.png"
			sizes="100vw"
			alt="The Coverage report identifies unused code"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			An example of a Coverage report. ()
		</figcaption>
	
</figure>


<p>Here, pay attention to the unused bytes:</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/346c8878-a66a-4a82-ba19-112b08eef3e5/mobile-first-optimization-img-8.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/346c8878-a66a-4a82-ba19-112b08eef3e5/mobile-first-optimization-img-8.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/346c8878-a66a-4a82-ba19-112b08eef3e5/mobile-first-optimization-img-8.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/346c8878-a66a-4a82-ba19-112b08eef3e5/mobile-first-optimization-img-8.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/346c8878-a66a-4a82-ba19-112b08eef3e5/mobile-first-optimization-img-8.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/346c8878-a66a-4a82-ba19-112b08eef3e5/mobile-first-optimization-img-8.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/346c8878-a66a-4a82-ba19-112b08eef3e5/mobile-first-optimization-img-8.png"
			sizes="100vw"
			alt="The coverage report UI shows a breakdown of used and unused bytes"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The unused bytes are represented by red lines. ()
		</figcaption>
	
</figure>


<p>This UI shows the amount of code that is currently unused, colored red. In this particular page, the first file shown is 73% bloat. You may see significant bloat at first, but it only represents the <em>current</em> render. Change your screen size and you should see the CSS coverage go up as media queries get applied. Open any interactive elements like modals and toggles, and it should go up further.</p>

<p>Once you’ve activated every view, you will have an idea of how much code you are actually using. Next, you can dig into the report further to find out just which pieces of code are unused, simply click on one of the resources and look in the main window:</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3ae55233-9752-410d-8efc-6787f1287755/mobile-first-optimization-img-9.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3ae55233-9752-410d-8efc-6787f1287755/mobile-first-optimization-img-9.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3ae55233-9752-410d-8efc-6787f1287755/mobile-first-optimization-img-9.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3ae55233-9752-410d-8efc-6787f1287755/mobile-first-optimization-img-9.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3ae55233-9752-410d-8efc-6787f1287755/mobile-first-optimization-img-9.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3ae55233-9752-410d-8efc-6787f1287755/mobile-first-optimization-img-9.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3ae55233-9752-410d-8efc-6787f1287755/mobile-first-optimization-img-9.png"
			sizes="100vw"
			alt="Detail view of a file in the Coverage report, showing which pieces of code aren’t being used"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Click on a file in the Coverage report to see the specific portions of unused code. ()
		</figcaption>
	
</figure>


<p>In this CSS file, look at the highlights to the left of each ruleset; <em>green</em> indicates used code and <em>red</em> indicates bloat. If you are building a single page app or using specialized resources for this particular page, you may be inclined to go in and remove this garbage. But don’t be too hasty. You should definitely remove dead code, but be careful to make sure that you haven’t missed a breakpoint or interactive element.</p>

<h3>Next Steps</h3>

<p>In this article, we’ve shown the quantitative benefits of optimizing page speed. I hope you’re convinced, and that you have the tools you need to convince others. We’ve also set a minimum goal for mobile page speed: sub three seconds.</p>

<p>To hit this goal, it’s important that you prioritize the highest impact optimizations first. There are a lot of resources online that can help define this roadmap, such as . Lighthouse can also be a great tool for identifying specific issues in your codebase, so I encourage you to tackle those bottlenecks first. Sometimes the smallest optimizations can have the biggest impact.</p>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(da, lf, ra, yk, il)</span>
</div>



  <div id="sponsors-article-end" data-impression="true" class="c-promo-box c-promo-box--ad c-promo-box--wide sponsors hidden" data-audience="non-subscriber" data-remove="true"></div>



</div>



              </article>
            </body>
          </html>
---------------
<h1 id="#title_1" >2、文章： 敏捷开发&远程团队——你应该知道的六条生产力秘诀</h1>
Tanya Kumari
[http://www.infoq.com/cn/articles/remote-team-productivity-hacks?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/remote-team-productivity-hacks?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/remote-team-productivity-hacks/zh/headerimage/GettyImages-590608096-1523273751601.jpg"/><p>随着世界各地的组织都在尝试精益转型，现如今的分布式敏捷工作环境肯定在增加。本文将提供一些建议，克服这种组合的固有挑战。这种方法可以帮助远程团队分清事情的优先级并变得更有生产力，而不会引入其他的矛盾。</p> <i>By Tanya Kumari</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_2" >3、文章： 区块链创新之卡尔达诺（Cardano）</h1>
自游
[http://www.infoq.com/cn/articles/blockchain-innovation-cardano?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/blockchain-innovation-cardano?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/blockchain-innovation-cardano/zh/smallimage/logo-1512943402650-1524678384643.jpeg"/><p>我们之前介绍了以太坊的直接竞争对手EOS，今天这篇文章我们要介绍的卡尔达诺（Cardano）的目标就更加远大了，他要同时锁定比特币和以太坊。但大家去网上搜索卡尔达诺相关资料时就会发现基本没有吐槽点，一致的信任与好评。到底是什么样的项目得到大家这么高的认可度呢？</p> <i>By 自游</i>
---------------
<h1 id="#title_3" >4、文章： 实时音视频的架构设计</h1>
关旭
[http://www.infoq.com/cn/articles/realtime-video-audio-architecture?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/realtime-video-audio-architecture?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/realtime-video-audio-architecture/zh/smallimage/mobile-logo-1510931101833-1524678803043.jpg"/><p>从直播在线上抓娃娃，不断变化的是玩法的创新，始终不变的是对超低延迟的苛求。实时架构是超低延迟的基石，如何在信源编码、信道编码和实时传输整个链条来构建实时架构？在实时架构的基础之上，如果通过优化采集、编码、传输、解码和渲染中的关键环节来降低延迟？本文将会介绍即构在这方面的思考与实践。</p> <i>By 关旭</i>
---------------
<h1 id="#title_4" >5、百度“深度学习公开课”首场爆满，开发者收获最强进阶“宝典”</h1>
李珂
[http://www.infoq.com/cn/news/2018/04/Baidu-deep-learning?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/04/Baidu-deep-learning?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p></p> <i>By 李珂</i>
---------------
<h1 id="#title_5" >6、英孚教育全面上云与Serverless构建之路</h1>
曹倩芸
[http://www.infoq.com/cn/news/2018/04/ef-serverless?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/04/ef-serverless?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>在英孚教育的云迁移之路中，许多值得借鉴的架构设计经验和部署战略的发展理念可以作为典型案例用来分析。因而，InfoQ也借此机会对英孚青少儿CTO Andrew Tsui进行了专访，与他探讨应用、数据迁移上云以及在Serverless架构实践中的相关思考。</p> <i>By 曹倩芸</i>
---------------
<h1 id="#title_6" >7、Sauce Labs将分析和扩展调试添加到其持续测试云中</h1>
Helen Beal
[http://www.infoq.com/cn/news/2018/04/sauce-labs-analytics-testing?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/04/sauce-labs-analytics-testing?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>在最近的用户会议SauceCon上，Sauce Labs为其持续测试云加入了一些新的功能，包括测试分析，其中还包含了一个仪表板，用于分析测试结果并显示浏览器和操作系统（包括安卓和iOS）常见的故障。</p> <i>By Helen Beal</i> <i> Translated by 张兰月</i>
---------------
<h1 id="#title_7" >8、Spring Cloud Stream 2.0发布，专注于性能、灵活性和一致性</h1>
Daniel Bryant
[http://www.infoq.com/cn/news/2018/04/spring-cloud-stream-2.0?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/04/spring-cloud-stream-2.0?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Pivotal正式发布Spring Cloud Stream 2.0，用于构建高度可扩展的基于事件驱动的微服务。此版本包含对content-type协商功能（允许用户定义消息转换器）的全面改进，减小资源占用，支持轮询式的消费者，支持Micrometer度量指标，增强对Apache Kafka Streams的支持等。</p> <i>By Daniel Bryant</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_8" >9、精益敏捷采购的外包</h1>
Shane Hastie
[http://www.infoq.com/cn/news/2018/04/lean-agile-procurement?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/04/lean-agile-procurement?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>采购流程是组织在运营中变敏捷的最后一道障碍。在最近的Agilia会议上, Mirko Kleiner就精益敏捷采购提出了一种服务合同谈判的方法，该方法涉及采购专家、IT团队和供应商，它能够大幅缩短合同谈判的时间，并将你争我夺的态度转变为协作的方式，以满足客户的需求。</p> <i>By Shane Hastie</i> <i> Translated by 张兰月</i>
---------------
<h1 id="#title_9" >10、GCP发布Kaniko：在非特权容器和Kubernetes中构建容器镜像的工具</h1>
Daniel Bryant
[http://www.infoq.com/cn/news/2018/04/kaniko-container-image-builder?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/04/kaniko-container-image-builder?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Google发布了“Kaniko”，一种用于在未授权容器或Kubernetes集群中构建容器镜像的开源工具。虽然Kaniko也是根据用户给定的Dockerfile构建镜像，但是并不依赖于Docker守护进程，而是在用户空间中完全执行每个命令，并对所导致的文件系统更改做快照。Kaniko支持在Kubernetes集群等不方便甚至是不能安全地暴露Docker守护进程的环境中构建容器镜像。</p> <i>By Daniel Bryant</i> <i> Translated by 盖磊</i>
---------------