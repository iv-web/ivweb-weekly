## 文章索引
1、 <a href="#1video-playback-on-the-web:-video-delivery-best-practices-part-2" >Video Playback On The Web: Video Delivery Best Practices (Part 2)</a><br/>
2、 <a href="#2page-visibility-api-教程" >Page Visibility API 教程</a><br/>
3、 <a href="#3文章-腾讯十年老兵区块链本质上是一个异地多活的分布式数据库" >文章： 腾讯十年老兵：区块链本质上是一个异地多活的分布式数据库</a><br/>
4、 <a href="#4全栈jvm框架micronaut通向10版本之路" >全栈JVM框架Micronaut通向1.0版本之路</a><br/>
5、 <a href="#5sharding-sphere成长记写在分布式数据库代理端里程碑版本300发布之际" >Sharding-Sphere成长记——写在分布式数据库代理端里程碑版本3.0.0发布之际</a><br/><h1 id="#title_0" >1、Video Playback On The Web: Video Delivery Best Practices (Part 2)</h1>
Doug Sillars
[https://www.smashingmagazine.com/2018/10/video-playback-on-the-web-part-2/](https://www.smashingmagazine.com/2018/10/video-playback-on-the-web-part-2/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/10/video-playback-on-the-web-part-2/" />
              <title>Video Playback On The Web: Video Delivery Best Practices (Part 2)</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>Video Playback On The Web: Video Delivery Best Practices (Part 2)</h1>
                  
                    
                    <address>Doug Sillars</address>
                  
                  <time datetime="2018-10-25T14:40:24&#43;02:00" class="op-published">2018-10-25T14:40:24+02:00</time>
                  <time datetime="2018-10-25T17:59:59&#43;00:00" class="op-modified">2018-10-25T17:59:59+00:00</time>
                </header>
                

<p>In my , I examined video trends on the web today, using data from the HTTP Archive. I found that many websites serve the same video content on mobile <em>and</em> desktop, and that many video streams are being delivered at bitrates that are too high to playback on 3G speed connections. We also discovered that may websites automatically download video to mobile devices &mdash; damaging customer’s data plans, battery life, for videos that might not ever be played.</p>

<p><strong>TL;DR</strong>: <em>In this post, we look at techniques to optimize the speed and delivery of video to your customers, and provide a list of  to help you deliver your video assets.</em></p>

<h3 id="video-playback-metrics">Video Playback Metrics</h3>

<p>There are 3 principal video playback metrics in use today:</p>

<ol>
<li>Video Startup Time</li>
<li>Video Stalling</li>
<li>Video Quality</li>
</ol>

<p>Since video files are large, optimizing the video to be as small as possible will lead to faster video delivery, speeding up video start, lowering the number of stalls, and minimizing the effect of the quality of the video delivered. Of course, we need to balance startup speed and stalling with the third metric of quality (and higher quality videos generally use more data).</p>

<h3 id="video-startup">Video Startup</h3>

<p>When a user presses play on a video, they expect to be able to watch the video quickly. According to  (a leader in video metric analysis), in Q1 of 2018, 14% of videos never started playing (that’s 2.4 Billion video plays) after the user pressed play.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9fdc50ef-4ed5-4a83-bd5b-808c8c420431/video-playback-web-image-17.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9fdc50ef-4ed5-4a83-bd5b-808c8c420431/video-playback-web-image-17.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9fdc50ef-4ed5-4a83-bd5b-808c8c420431/video-playback-web-image-17.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9fdc50ef-4ed5-4a83-bd5b-808c8c420431/video-playback-web-image-17.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9fdc50ef-4ed5-4a83-bd5b-808c8c420431/video-playback-web-image-17.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9fdc50ef-4ed5-4a83-bd5b-808c8c420431/video-playback-web-image-17.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9fdc50ef-4ed5-4a83-bd5b-808c8c420431/video-playback-web-image-17.png"
			sizes="100vw"
			alt="Pie chart showing that nearly 15% of all videos fail to play"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Video Start Breakdown ()
		</figcaption>
	
</figure>


<p>2.3% of videos (400M video requests) failed to play after the user pressed the play button. 11.54% (2B plays) were abandoned by the user after pressing play. Let’s try to break down what might be causing these issues.</p>



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




<h3 id="video-playback-failure">Video Playback Failure</h3>

<p>Video playback failure accounted for 2.3% of all video plays. What could lead to this?  In the HTTP Archive data, we see 0.3% of all video requests resulting in a 4xx or 5xx HTTP response &mdash; so some percentage fail to bad URLs or server misconfigurations. Another potential issue (that is not observed in the HTTP Archive data) are videos that are blocked by Geolocation (blocked based on the location of the viewer and the licensing of the provider to display the video in that locale).</p>

<h3 id="video-playback-abandonment">Video Playback Abandonment</h3>

<p>The Conviva report states that 11.5% of all video plays <em>would</em> play, but that the customer abandoned the playback before the video started playing. The issue here is that the video is not being delivered to the customer fast enough, and they give up. There are many studies on the mobile web where long delays cause abandonment of web pages, and it appears that the same effect occurs with video playback as well.</p>

<p>Research from  shows that viewers will wait for 2 seconds, but for each subsequent second, 5.8% of viewers abandon the video.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/12b96e6e-dff5-4a60-a9b8-640743475780/video-playback-web-image-18a.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/12b96e6e-dff5-4a60-a9b8-640743475780/video-playback-web-image-18a.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/12b96e6e-dff5-4a60-a9b8-640743475780/video-playback-web-image-18a.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/12b96e6e-dff5-4a60-a9b8-640743475780/video-playback-web-image-18a.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/12b96e6e-dff5-4a60-a9b8-640743475780/video-playback-web-image-18a.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/12b96e6e-dff5-4a60-a9b8-640743475780/video-playback-web-image-18a.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/12b96e6e-dff5-4a60-a9b8-640743475780/video-playback-web-image-18a.png"
			sizes="100vw"
			alt="Chart displaying the abandonment rate as startup time is longer."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Rate of abandonment over time ()
		</figcaption>
	
</figure>


<p>So what leads to video playback issues? In general, larger files take longer to download, so will delay playback. Let’s look at a few ways that one can speed up the playback of videos. To reduce the number of videos abandoned at startup, we should ‘slim’ down these files as best as possible, so they download (and begin playback) quickly.</p>

<div class="sponsors__wide-place"></div>




<h3 id="mp4-video-preload">MP4: Video Preload</h3>

<p>To ensure fast playback on the web, one option is to preload the video onto the device in advance. That way, when your customer clicks ‘play’ the video is already downloaded, and playback will be fast. HTML offers a preload attribute with 3 possible options: <code>auto</code>, <code>metadata</code> and <code>none</code>.</p>

<h4 id="preload-auto"><code>preload = auto</code></h4>

<p>When your video is delivered with <code>preload=&quot;auto&quot;</code>, the browser downloads the entire video file and stores it locally. This permits a large performance improvement for video startup, since the video is available locally on the device, and no network interference will slow the startup.</p>

<p>However, <code>preload=&quot;auto&quot;</code> should only be used if there is a high probability that the video will be viewed. If the video is simply resident on your webpage, and it is downloaded each time, this will add a large data penalty to your mobile users, as well as increase your server/CDN costs for delivering the entire video to all of your users.</p>

<p>This website has a section entitled “Video Gallery” with several videos.  Each video in this section has preload set to <code>auto</code>, and we can visualize their download in the WebPageTest waterfall as green horizontal lines:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/48b30762-0835-4fd0-96aa-f15493519e2f/video-playback-web-image-19.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/48b30762-0835-4fd0-96aa-f15493519e2f/video-playback-web-image-19.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/48b30762-0835-4fd0-96aa-f15493519e2f/video-playback-web-image-19.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/48b30762-0835-4fd0-96aa-f15493519e2f/video-playback-web-image-19.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/48b30762-0835-4fd0-96aa-f15493519e2f/video-playback-web-image-19.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/48b30762-0835-4fd0-96aa-f15493519e2f/video-playback-web-image-19.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/48b30762-0835-4fd0-96aa-f15493519e2f/video-playback-web-image-19.png"
			sizes="100vw"
			alt="A WebPageTEst Waterfall chart"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Waterfall of video preload ()
		</figcaption>
	
</figure>


<p>There is a section called “Video Gallery”, and the files for this small section of the website account for 14.6M (83%) of the page download. The odds that one (of many) videos will be played is probably pretty low, and so utilizing <code>preload=&quot;auto&quot;</code> only generates a lot of data traffic for the site.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/13ec5202-483d-4462-8584-815128f13fc9/video-playback-web-image-20.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/13ec5202-483d-4462-8584-815128f13fc9/video-playback-web-image-20.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/13ec5202-483d-4462-8584-815128f13fc9/video-playback-web-image-20.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/13ec5202-483d-4462-8584-815128f13fc9/video-playback-web-image-20.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/13ec5202-483d-4462-8584-815128f13fc9/video-playback-web-image-20.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/13ec5202-483d-4462-8584-815128f13fc9/video-playback-web-image-20.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/13ec5202-483d-4462-8584-815128f13fc9/video-playback-web-image-20.png"
			sizes="100vw"
			alt="Pie Chart showing the high percentage (83%) of video usage."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Webpage data breakdown ()
		</figcaption>
	
</figure>


<p>In this case, it is unlikely that even one of these videos will be viewed, yet all of them are downloaded completely, adding 14.8MB of content to the mobile site (83% of the content on the page).  For videos that are have a high probability of playback (perhaps &gt;90% of page views result in video play) &mdash; preloading the entire video is a very good idea. But for videos that are unlikely to be played, <code>preload=&quot;auto&quot;</code> will only cause extra tonnage of content through your servers and to your customer’s mobile (and desktop) devices.</p>

<h4 id="preload-metadata"><code>preload=&quot;metadata&quot;</code></h4>

<p>When the <code>preload=&quot;metadata&quot;</code> attribute is used, an initial segment of the video is downloaded. This allows the player to know the size of the video window, and to perhaps have a second or 2 of video downloaded for immediate playback. The browser simply makes a 206 (partial request) of the video content. By storing a small bit of video data on the device, video startup time is decreased, without a large impact to the amount of data transferred.</p>

<p>On Chrome, metadata is the default choice if no attribute is chosen.</p>

<p><strong>Note</strong>: <em>This can still lead to a large amount of video to be downloaded, if the video is large.</em></p>

<p>For example, on a mobile website with a video set at <code>preload=&quot;metadata&quot;</code>, we see just one request for video:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/31624d71-4f8a-4f68-a9ac-672d97133910/video-playback-web-metatdata-waterfall.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/31624d71-4f8a-4f68-a9ac-672d97133910/video-playback-web-metatdata-waterfall.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/31624d71-4f8a-4f68-a9ac-672d97133910/video-playback-web-metatdata-waterfall.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/31624d71-4f8a-4f68-a9ac-672d97133910/video-playback-web-metatdata-waterfall.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/31624d71-4f8a-4f68-a9ac-672d97133910/video-playback-web-metatdata-waterfall.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/31624d71-4f8a-4f68-a9ac-672d97133910/video-playback-web-metatdata-waterfall.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/31624d71-4f8a-4f68-a9ac-672d97133910/video-playback-web-metatdata-waterfall.png"
			sizes="100vw"
			alt="Webpage Test Waterfall chart"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<p>And the request is a partial download, but it still results in 2.7 MB of video to be downloaded because the full video is 1080p, 150s long and 97 MB (we’ll talk about optimizing video size in the next sections).</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/13ec5202-483d-4462-8584-815128f13fc9/video-playback-web-image-20.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/13ec5202-483d-4462-8584-815128f13fc9/video-playback-web-image-20.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/13ec5202-483d-4462-8584-815128f13fc9/video-playback-web-image-20.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/13ec5202-483d-4462-8584-815128f13fc9/video-playback-web-image-20.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/13ec5202-483d-4462-8584-815128f13fc9/video-playback-web-image-20.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/13ec5202-483d-4462-8584-815128f13fc9/video-playback-web-image-20.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/13ec5202-483d-4462-8584-815128f13fc9/video-playback-web-image-20.png"
			sizes="100vw"
			alt="Pie chart showing that 2.7 MB or 42% of data is still vide with preload=metadata."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			KB usage with video metadata ()
		</figcaption>
	
</figure>


<p>So, I would recommend that <code>preload=&quot;metadata&quot;</code> still only be used when there is a fairly high probability that the video will be viewed by your users, or if the video is small.</p>

<h4 id="preload-none"><code>preload=&quot;none&quot;</code></h4>

<p>The most economical download option for videos, as no video files are downloaded when the page is loaded. This will potentially add a delay in playback, but will result in faster initial page load For sites with many videos on a single page, it may make sense to add a poster to the video window, and not download any of the video until it is expressly requested by the end user. All YouTube videos that are embedded on websites never download any video content until the play button is pressed, essentially behaving as if <code>preload=&quot;none&quot;</code>.</p>

<p><strong>Preload Best Practice</strong>: <em>Only use</em> <code>preload=&quot;auto&quot;</code> <em>if there is a high probability that the video will be watched. In general, the use of</em> <code>preload=&quot;metadata&quot;</code> <em>provides a good balance in data usage vs. startup time, but should be monitored for excessive data usage.</em></p>

<div class="sponsors__wide-place"></div>




<h3 id="mp4-video-playback-tips">MP4 Video Playback Tips</h3>

<p>Now that the video has started, how can we ensure that the video playback can be optimized to not stall and continue playing. Again, the trick is to make sure the video is as small as possible.</p>

<p>Let’s look at some tricks to optimize the size of video downloads. There are several dimensions of video that can be optimized to reduce the size of the video:</p>

<h3 id="audio">Audio</h3>

<p>Video files are split into different &ldquo;streams&rdquo; &mdash; the most common being the video stream. The second most common stream is the audio track that syncs to the video. In some video playback applications, the audio stream is delivered separately; this allows for different languages to be delivered in s seamless manner.</p>

<p>If your video is played back in a silent manner (like a looping GIF, or a background video), removing the audio stream from the video is a quick and easy way to reduce the file size. In one example of a background video, the full file was 5.3 MB, but the audio track (which is never heard) was nearly 300 KB (5% of the file)  By simple eliminating the audio, the file will be delivered quickly without wasting bytes.</p>

<p>42% of the MP4 files found on the HTTP Archive have no audio stream.</p>

<p><strong>Best Practice</strong>: <em>Remove the audio tracks from videos that are played silently.</em></p>

<h3 id="video-encoding">Video Encoding</h3>

<p>When encoding a video, there are options to reduce the video quality (number of pixels per frame, or the frames per second). Reducing a high-quality video to be suitable for the web is easy to do, and generally does not affect the quality delivered to your end users. This article is not long enough for an in depth discussion of all the various compression techniques available for video. In <code>x264</code> and <code>x265</code> encoders, there is a term called the <strong>C</strong>onstant <strong>R</strong>ate <strong>F</strong>actor (CRF). Using a CRF of 23-28 will generally give a good compression/quality trade off, and is a great first start into the realm of video compression</p>

<h3 id="video-size">Video Size</h3>

<p>Video size can be affected by many dimensions: length, width, and height (you could probably include audio here as well).</p>

<h3 id="video-duration">Video Duration</h3>

<p>The length of the video is generally not a feature that a web developer can adjust. If the video is going to playback for three minutes, it is going to playback for three minutes. In cases in which the video is exceptionally long, tools like <code>preload=&quot;none&quot;</code> or streaming the video can allow for a smaller amount of data to be downloaded initially to reduce page load time.</p>

<h3 id="video-dimensions">Video Dimensions</h3>

<p>18% of all video found in the HTTP Archive is identical on mobile and desktop. Those who have worked with responsive web design know how optimizing images for different viewports can drastically reduce load times since the size of the images is much smaller for smaller screens.</p>

<p>The same holds for video. A website with a 30 MB 2560&times;1226 background video will have a hard time downloading the video on mobile (probably on desktop, too!).  Resizing the video drastically decreases the files size, and might even allow for three or four different background videos to be served:</p>

<table class="tablesaw break-out" data-tablesaw-mode="swipe" data-tablesaw-minimap>
    <thead>
        <tr>
            <th data-tablesaw-priority="persist">Width</th>
            <th>Video (MB)</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>1226</td>
            <td>30</td>
        </tr>
        <tr>
            <td>1080</td>
            <td>8.1</td>
        </tr>
        <tr>
            <td>720</td>
            <td>43</td>
        </tr>
        <tr>
            <td>608</td>
            <td>3.3</td>
        </tr>
        <tr>
            <td>405</td>
            <td>1.76</td>
        </tr>
    </tbody>
</table>

<p>Now, unfortunately, browsers do not support media queries for video in HTML, meaning that this just does not work:</p>

<pre><code class="language-bash">&lt;video preload="auto" autoplay muted controls
    source sizes="(max-width:1400px 100vw, 1400px"
    srcset="small.mp4 200w,
            medium.mp4 800w,
            large.mp4 1400w"
    src="large.mp4"

&lt;/video&gt;
</code></pre>

<p>Therefore, we’ll need to create a small JS wrapper to deliver the videos we want to different screen sizes. But before we go there&hellip;</p>

<h3 id="downloading-video-but-hiding-it-from-view">Downloading Video, But Hiding It From View</h3>

<p>Another throwback to the early responsive web is to download full-size images, but to hide them on mobile devices. Your customers get all the delay for downloading the large images (and hit to mobile data plan, and extra battery drain, etc.), and none of the benefit of actually seeing the image. This occurs quite frequently with video on mobile. So, as we write our script, we can ensure that smaller screens never request the video that will not appear in the first place.</p>

<h3 id="retina-quality-videos">Retina Quality Videos</h3>

<p>You may have different videos for different device screen densities. This can lead to added time to download the videos to your mobile customers. You may wish to prevent retina videos on smaller screen devices, or on devices with a limited network bandwidth, falling to back to standard quality videos for these devices. Tools like the  can provide you with the network throughput, and help you decide which video quality you&rsquo;d like to serve to your customer.</p>

<h4 id="downloading-different-video-types-based-on-device-size-and-network-quality">Downloading Different Video Types Based On Device Size And Network Quality</h4>

<p>We’ve just covered a few ways to optimize the delivery of movies to smaller screens, and also noted the inability of the video tag to choose between video types, so here is a quick JS snippet that will use the screen width to:</p>

<ul>
<li>Not deliver video on screens below 500px;</li>
<li>Deliver small videos for screens 500-1400;</li>
<li>Deliver a larger sized video to all other devices.</li>
</ul>

<pre class="break-out"><code class="language-html">&lt;html&gt;&lt;body&gt;
&lt;div id="video"&gt; &lt;/div&gt;
&lt;div id="text"&gt;&lt;/div&gt;
&lt;script&gt;
    //get screen width and pixel ratio
    var width = screen.width;
    var dpr = window.devicePixelRatio;
//initialise 2 videos &mdash; 
//“small” is 960 pixels wide (2.6 MB), large is 1920 pixels wide (10 MB)
    var smallVideo="http://res.cloudinary.com/dougsillars/video/upload/w_960/v1534228645/30s4kbbb_oblsgc.mp4";
    var bigVideo = "http://res.cloudinary.com/dougsillars/video/upload/w_1920/v1534228645/30s4kbbb_oblsgc.mp4";
    //TODO add logic on adding retina videos    
    if (width&lt;500){
        console.log("this is a very small screen, no video will be requested");
        }
        
    else if (width&lt; 1400){
            console.log("let’s call this mobile sized");
            var videoTag = "\&lt;video preload=\"auto\" width=\"100%\" autoplay muted controls src=\"" +smallVideo +"\"/\&gt;";
            console.log(videoTag);
            document.getElementById('video').innerHTML = videoTag;
            document.getElementById('text').innerHTML = "This is a small video.";
            }
    else{
            var videoTag = "\&lt;video preload=\"auto\" width=\"100%\" autoplay muted controls src=\"" +bigVideo +"\"/\&gt;";
            document.getElementById('video').innerHTML = videoTag;
            document.getElementById('text').innerHTML = "This is a big video.";
            
    }
    
&lt;/script&gt;
&lt;/html&gt;&lt;/body&gt;
</code></pre>

<p>This script divides user’s screens into three options:</p>

<ol>
<li>Under 500 pixels, no video is shown.</li>
<li>Between 500 and 1400, we have a smaller video.</li>
<li>For larger than 1400 pixel wide screens, we have a larger video.</li>
</ol>

<p>Our page has a responsive video with two different sizes: one for mobile, and another for desktop-sized screens. Mobile users get great video quality, but the file is only 2.6 MB, compared to the 10MB video for desktop.</p>

<h3 id="animated-gifs">Animated GIFs</h3>

<p>Animated GIFs are big files. While both aGIFs and video files compress the data through width and height dimensions, only video files have compression (on the often larger) time axis. aGIFs are essentially “flipping through” static GIF images quickly. This lack of compression adds a significant amount of data. Thankfully, it is possible to replace aGIFs with a looping video, potentially saving MBs of data for each request.</p>

<pre><code class="language-html">&lt;video loop autoplay muted playsinline src="pseudoGif.mp4"&gt;
</code></pre>

<p>In Safari, there is an even fancier approach:  You can place a looping mp4 in the picture tag, like so:</p>

<pre class="break-out"><code class="language-html">&lt;picture&gt;
  &lt;source type="video/mp4" loop autoplay srcset="loopingmp4.mp4"&gt;
  &lt;source type="image/webp"  srcset="animated.webp"&gt;
  &lt;src="animated.gif"&gt;
&lt;/picture&gt;
</code></pre>  

<p>In this case, Safari will play the animated GIF, while Chrome (and other browsers that support WebP) will play the animated WebP, with a fallback to the animated GIF. You can read more about this approach in .</p>

<h3 id="third-party-videos">Third-Party Videos</h3>

<p>One of the easiest ways to add video to your website is to simply copy/paste the code from a video sharing service and put it on your site. However, just like adding any third party to your site, you need to be vigilant about what kind of content is added to your page, and how that will affect page load. Many of these &ldquo;simply paste this into your HTML&rdquo; widgets add 100s of KB of JavaScript. Others will download the entire movie (think <code>preload=&quot;auto&quot;</code>), and some will do both.</p>

<p><strong>Third-Party Video Best Practice</strong>: <em>Trust but verify. Examine how much content is added, and how much it affects your page load time. Also, the behavior might change, so track with your analytics regularly.</em></p>

<h3 id="streaming-startup">Streaming Startup</h3>

<p>When a video stream is requested, the server supplies a manifest file to the player, listing every available stream (with dimensions and bitrate information). In HLS streaming, the player generally chooses the first stream in the list to begin playback. Therefore, the stream positioned first in the manifest file should be optimized for video startup on both mobile and desktop (or perhaps alternative manifest files should be delivered to mobile vs. desktop).</p>

<p>In most cases, the startup is optimized by using a lower quality stream to begin playback. Once the player downloads a few segments, it has a better idea of available throughput and can select a higher quality stream for later segments. As a user, you have likely seen this &mdash; where the first few seconds of a video looks very pixelated, but a few seconds into playback the video sharpens.</p>

<p>In examining 1,065 manifest files delivered to mobile devices from the HTTP Archive, we find that  59% of videos have an initial bitrate under 1.2 MBPS &mdash; and are likely to start streaming without any much delay at 1.6 MBPS 3G data rates. 11% use a bitrate between 1.2 and 1.6 MBPS &mdash; which may slow the startup on 3G, and 30% have a bitrate above 1.6 MBPS &mdash; and are unable to playback at this bitrate on a 3G connection. Based on this data, it appears that &#126;41% of all videos will not be able to sustain the initial bitrate on mobile &mdash; adding to startup delay, and possibly increased number of stalls during playback.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2f1c6861-637d-4b1d-9360-061038fd4b92/video-playback-web-image-25.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2f1c6861-637d-4b1d-9360-061038fd4b92/video-playback-web-image-25.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2f1c6861-637d-4b1d-9360-061038fd4b92/video-playback-web-image-25.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2f1c6861-637d-4b1d-9360-061038fd4b92/video-playback-web-image-25.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2f1c6861-637d-4b1d-9360-061038fd4b92/video-playback-web-image-25.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2f1c6861-637d-4b1d-9360-061038fd4b92/video-playback-web-image-25.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2f1c6861-637d-4b1d-9360-061038fd4b92/video-playback-web-image-25.png"
			sizes="100vw"
			alt="Column chart showing initial bitrates in streaming videos. Many videos have too high an initial bitrate to stream on mobile."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Initial bitrate for video streams ()
		</figcaption>
	
</figure>


<p><strong>Streaming Startup Best Practice</strong>: <em>Ensure your initial bitrate in the manifest file is one that will work for most of your customers. If the player has to change streams during startup, playback will be delayed and you will lose video views.</em></p>

<p>So, what happens when the video’s bitrate is near (or above) the available throughput? After a few seconds of download without a completed video segment ready for playback, the player stops the download and chooses a lower quality bitrate video, and begins the process again. The action of downloading a video segment and then abandoning leads to additional startup delay, which will lead to video abandonment.</p>

<p>We can visualize this by building video manifests with different initial bitrates. We test 3 different scenarios: starting with the lowest (215 KBPS), middle (600 KBPS), and highest bitrate (2.6 MBPS).</p>

<p>When beginning with the lowest quality video, playback begins at 11s. After a few seconds, the player begins requesting a higher quality stream, and the picture sharpens.</p>

<p>When starting with the highest bitrate (testing on a 3G connection at 1.6 MBPS), the player quickly realizes that playback cannot occur, and switches to the lowest bitrate video (215 KBPS). The video starts playing at 17s. There is a 6-second delay, and the video quality is the same low quality delivered to in the first test.</p>

<p>Using the middle-quality video allows for a bit of a tradeoff, the video begins playing at 13s (2 seconds slower), but is high quality from the start -and there is no jump from pixelated to higher quality video.</p>

<p><strong>Best Practice for Video Startup</strong>: <em>For fastest playback, start with the lowest quality stream. For longer videos, you might consider using a ‘middle quality’ stream at start to deliver sharp video at startup (with a slightly longer delay).</em></p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7c10f1ef-ec71-4353-8894-80ce5c3cde20/video-playback-web-image-27.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7c10f1ef-ec71-4353-8894-80ce5c3cde20/video-playback-web-image-27.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7c10f1ef-ec71-4353-8894-80ce5c3cde20/video-playback-web-image-27.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7c10f1ef-ec71-4353-8894-80ce5c3cde20/video-playback-web-image-27.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7c10f1ef-ec71-4353-8894-80ce5c3cde20/video-playback-web-image-27.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7c10f1ef-ec71-4353-8894-80ce5c3cde20/video-playback-web-image-27.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7c10f1ef-ec71-4353-8894-80ce5c3cde20/video-playback-web-image-27.png"
			sizes="100vw"
			alt="Thumbnails of 3 pages with video loading."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			WebPage Test Thumbnails ()
		</figcaption>
	
</figure>


<p>WebPageTest results: Initial video stream is low, middle and high (from top to bottom). The video starts the fastest with the lowest quality video. It is important to note that the high quality start video at 17s is the same quality as the low quality start at 11s.</p>

<h3 id="streaming-continuing-playback">Streaming: Continuing Playback</h3>

<p>When the video player can determine the optimal video stream for playback and the stream is lower than the available network speed, the video will playback with no issues. There are tricks that can help ensure that the video will deliver in an optimal manner.  If we examine the following manifest entry:</p>

<pre class="break-out"><code class="language-bash">#EXT-X-STREAM-INF:BANDWIDTH=912912,PROGRAM-ID=1,CODECS="avc1.42c01e,mp4a.40.2",RESOLUTION=640x360,SUBTITLES="subs"
video/600k.m3u8
</code></pre>

<p>The information line reports that this stream has a 913 KBPS bitrate, and 640&times;360 resolution. If we look at the URL that this line points to, we see that it references a 600k video. Examining the video files shows that the video is 600 KBPS, and the manifest is overstating the bitrate.</p>

<h4 id="overstating-the-video-bitrate">Overstating The Video Bitrate</h4>

<ul>
<li><strong>PRO</strong><br />
Overstating the bitrate will ensure that when the player chooses a stream, the video will download faster than expected, and the buffer will fill up faster than expected, reducing the possibility of a stall.</li>
<li><strong>CON</strong><br />
By overstating the bitrate, the video delivered will be a lower quality stream. If we look at the entire list of reported vs. actual bitrates:</li>
</ul>

<table class="tablesaw break-out" data-tablesaw-mode="swipe" data-tablesaw-minimap>
    <thead>
        <tr>
            <th data-tablesaw-priority="persist">Reported (KBS)</th>
            <th>Actual</th>
            <th>Resolution</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>913</td>
            <td>600</td>
            <td>640x360</td>
        </tr>
        <tr>
            <td>142</td>
            <td>64</td>
            <td>320x180</td>
        </tr>
        <tr>
            <td>297</td>
            <td>180</td>
            <td>512x288</td>
        </tr>
        <tr>
            <td>506</td>
            <td>320</td>
            <td>512x288</td>
        </tr>
        <tr>
            <td>689</td>
            <td>450</td>
            <td>412x288</td>
        </tr>
        <tr>
            <td>1410</td>
            <td>950</td>
            <td>853x480</td>
        </tr>
        <tr>
            <td>2090</td>
            <td>1500</td>
            <td>1280x720</td>
        </tr>
    </tbody>
</table>

<p>For users on a 1.6 MBPS connection, the player will choose the 913 KBPS bitrate, serving the customer 600 KBPS video. However, if the bitrates had been reported accurately, the 950 KBPS bitrate would be used, and would likely have streamed with no issues. While the choices here prevent stalls, they also lower the quality of the delivered video to the consumer.</p>

<p><strong>Best Practice</strong>: <em>A small overstatement of video bitrate may be useful to reduce the number of stalls in playback. However, too large a value can lead to reduced quality playback.</em></p>

<p><em>Test the Neilsen video in the browser, and see if you can make it jump back and forth.</em></p>

<h3 id="conclusion">Conclusion</h3>

<p>In this post, we’ve walked through a number of ways to optimize the videos that you present on your websites. By  following the best practices illustrated in this post:</p>

<ol>
<li><code>preload=&quot;auto&quot;</code><br />
Only use if there is a high probability that this video will be watched by your customers.</li>
<li><code>preload=&quot;metadata&quot;</code><br />
Default in Chrome, but can still lead to large video file downloads. Use with caution.</li>
<li><strong>Silent Videos</strong> (looping GIFs or background videos)<br />
Strip out the audio channel</li>
<li><strong>Video Dimensions</strong><br />
Consider delivering differently sized video to mobile over desktop. The videos will be smaller, download faster, and your users are unlikely to see the difference (your server load will go down too!)</li>
<li><strong>Video Compression</strong><br />
Don’t forget to compress the videos to ensure that they are delivered</li>
<li><strong>Don’t ‘hide’ videos</strong><br />
If the video will not be displayed &mdash; don’t download it.</li>
<li><strong>Audit your third-party videos regularly</strong></li>
<li><strong>Streaming</strong><br />
Start with a lower quality stream to ensure fast startup. (For longer play videos, consider a medium bitrate for better quality at startup)</li>
<li><strong>Streaming</strong><br />
It’s OK to be conservative on bitrate to prevent stalling, but go too far, and the streams will deliver a lower quality video.</li>
</ol>

<p>You will find that the video on your page is streamlined for optimal delivery and that your customers will not only delight in the video you present but also enjoy a faster page load time overall.</p>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(dm, ra, il)</span>
</div>


              </article>
            </body>
          </html>
---------------
<h1 id="#title_1" >2、Page Visibility API 教程</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2018/10/page_visibility_api.html](http://www.ruanyifeng.com/blog/2018/10/page_visibility_api.html)
<h2>一、简介</h2>

<p>有时候，开发者需要知道，用户正在离开页面。常用的方法是监听下面三个事件。</p>

        <blockquote>
  <ul>
<li><code>pagehide</code></li>
<li><code>beforeunload</code></li>
<li><code>unload</code></li>
</ul>
</blockquote>

<p>但是，这些事件在手机上可能不会触发，页面就直接关闭了。因为手机系统可以将一个进程直接转入后台，然后杀死。</p>

<blockquote>
  <ul>
<li>用户点击了一条系统通知，切换到另一个 App。</li>
<li>用户进入任务切换窗口，切换到另一个 App。</li>
<li>用户点击了 Home 按钮，切换回主屏幕。</li>
<li>操作系统自动切换到另一个 App（比如，收到一个电话）。</li>
</ul>
</blockquote>

<p>上面这些情况，都会导致手机将浏览器进程切换到后台，然后为了节省资源，可能就会杀死浏览器进程。</p>

<p>以前，页面被系统切换，以及系统清除浏览器进程，是无法监听到的。开发者想要指定，任何一种页面卸载情况下都会执行的代码，也是无法做到的。为了解决这个问题，就诞生了 Page Visibility API。不管手机或桌面电脑，所有情况下，这个 API 都会监听到页面的可见性发生变化。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201810/bg2018082501.png" alt="" title="" /></p>

<p>这个新的 API 的意义在于，通过监听网页的可见性，可以预判网页的卸载，还可以用来节省资源，减缓电能的消耗。比如，一旦用户不看网页，下面这些网页行为都是可以暂停的。</p>

<blockquote>
  <ul>
<li>对服务器的轮询</li>
<li>网页动画</li>
<li>正在播放的音频或视频</li>
</ul>
</blockquote>

<h2>二、document.visibilityState</h2>

<p>这个 API 主要在<code>document</code>对象上，新增了一个<code>document.visibilityState</code>属性。该属性返回一个字符串，表示页面当前的可见性状态，共有三个可能的值。</p>

<blockquote>
  <ul>
<li><code>hidden</code>：页面彻底不可见。</li>
<li><code>visible</code>：页面至少一部分可见。</li>
<li><code>prerender</code>：页面即将或正在渲染，处于不可见状态。</li>
</ul>
</blockquote>

<p>其中，<code>hidden</code>状态和<code>visible</code>状态是所有浏览器都必须支持的。<code>prerender</code>状态只在支持"预渲染"的浏览器上才会出现，比如 Chrome 浏览器就有预渲染功能，可以在用户不可见的状态下，预先把页面渲染出来，等到用户要浏览的时候，直接展示渲染好的网页。</p>

<p>只要页面可见，哪怕只露出一个角，<code>document.visibilityState</code>属性就返回<code>visible</code>。只有以下四种情况，才会返回<code>hidden</code>。</p>

<blockquote>
  <ul>
<li>浏览器最小化。</li>
<li>浏览器没有最小化，但是当前页面切换成了背景页。</li>
<li>浏览器将要卸载（unload）页面。</li>
<li>操作系统触发锁屏屏幕。</li>
</ul>
</blockquote>

<p>可以看到，上面四种场景涵盖了页面可能被卸载的所有情况。也就是说，页面卸载之前，<code>document.visibilityState</code>属性一定会变成<code>hidden</code>。事实上，这也是设计这个 API 的主要目的。</p>

<p>另外，早期版本的 API，这个属性还有第四个值<code>unloaded</code>，表示页面即将卸载，现在已经被废弃了。</p>

<p>注意，<code>document.visibilityState</code>属性只针对顶层窗口，内嵌的<code>&lt;iframe&gt;</code>页面的<code>document.visibilityState</code>属性由顶层窗口决定。使用 CSS 属性隐藏<code>&lt;iframe&gt;</code>页面（比如<code>display: none;</code>），并不会影响内嵌页面的可见性。</p>

<h2>三、document.hidden</h2>

<p>由于历史原因，这个 API 还定义了<code>document.hidden</code>属性。该属性只读，返回一个布尔值，表示当前页面是否可见。</p>

<p>当<code>document.visibilityState</code>属性返回<code>visible</code>时，<code>document.hidden</code>属性返回<code>false</code>；其他情况下，都返回<code>true</code>。</p>

<p>该属性只是出于历史原因而保留的，只要有可能，都应该使用<code>document.visibilityState</code>属性，而不是使用这个属性。</p>

<h2>四、visibilitychange 事件</h2>

<p>只要<code>document.visibilityState</code>属性发生变化，就会触发<code>visibilitychange</code>事件。因此，可以通过监听这个事件（通过<code>document.addEventListener()</code>方法或<code>document.onvisibilitychange</code>属性），跟踪页面可见性的变化。</p>

<blockquote><pre><code class="language-javascript">
document.addEventListener('visibilitychange', function () {
  // 用户离开了当前页面
  if (document.visibilityState === 'hidden') {
    document.title = '页面不可见';
  }

  // 用户打开或回到页面
  if (document.visibilityState === 'visible') {
    document.title = '页面可见';
  }
});
</code></pre></blockquote>

<p>上面代码是 Page Visibility API 的最基本用法，可以监听可见性变化。</p>

<p>下面是另一个例子，一旦页面不可见，就暂停视频播放。</p>

<blockquote><pre><code class="language-javascript">
var vidElem = document.getElementById('video-demo');
document.addEventListener('visibilitychange', startStopVideo);

function startStopVideo() {
  if (document.visibilityState === 'hidden') {
    vidElem.pause();
  } else if (document.visibilityState === 'visible') {
    vidElem.play();
  }
}
</code></pre></blockquote>

<h2>五、页面卸载</h2>

<p>下面专门讨论一下，如何正确监听页面卸载。</p>

<p>页面卸载可以分成三种情况。</p>

<blockquote>
  <ul>
<li>页面可见时，用户关闭 Tab 页或浏览器窗口。</li>
<li>页面可见时，用户在当前窗口前往另一个页面。</li>
<li>页面不可见时，用户或系统关闭浏览器窗口。</li>
</ul>
</blockquote>

<p>这三种情况，都会触发<code>visibilitychange</code>事件。前两种情况，该事件在用户离开页面时触发；最后一种情况，该事件在页面从可见状态变为不可见状态时触发。</p>

<p>由此可见，<code>visibilitychange</code>事件比<code>pagehide</code>、<code>beforeunload</code>、<code>unload</code>事件更可靠，所有情况下都会触发（从<code>visible</code>变为<code>hidden</code>）。因此，可以只监听这个事件，运行页面卸载时需要运行的代码，不用监听后面那三个事件。</p>

<p>甚至可以这样说，<code>unload</code>事件在任何情况下都不必监听，<code>beforeunload</code>事件只有一种适用场景，就是用户修改了表单，没有提交就离开当前页面。另一方面，指定了这两个事件的监听函数，浏览器就不会缓存当前页面。</p>

<h2>六、参考链接</h2>

<ul>
<li>, W3C</li>
<li>, David Walsh</li>
<li>, Joe Marini</li>
<li>, Jatinder Mann</li>
<li>, Ilya Grigorik</li>
</ul>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2018-10-25T08:33:33+08:00">2018年10月25日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>文集：</li>
<li>社交媒体：</li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------
<h1 id="#title_2" >3、文章： 腾讯十年老兵：区块链本质上是一个异地多活的分布式数据库</h1>
腾讯TEG
[http://www.infoq.com/cn/articles/blockchain-is-a-distributed-database?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/blockchain-is-a-distributed-database?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/blockchain-is-a-distributed-database/zh/smallimage/logo-network-1527250511731-1540057433424.jpeg"/><p>讲师介绍：潘安群，腾讯 TEG 计费平台部账户中心总监，专家工程师；中国计算机学会 CCF 区块链专业委员会委员；有近 10 年分布式存储研发经验，目前负责分布式 Cache 系统厚德、分布式数据库 TDSQL，以及腾讯云区块链 TBaaS 平台的技术研发工作。 本文主要有四个部分的内容： 从分布式数据库角度看区块链；腾讯云区块链服务 TBaaS 技术介绍；智能合约开发及示例；快速部署及运营配套</p> <i>By 腾讯TEG</i>
---------------
<h1 id="#title_3" >4、全栈JVM框架Micronaut通向1.0版本之路</h1>
Michael Redlich
[http://www.infoq.com/cn/news/2018/10/the-road-to-micronaut-1.0?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/10/the-road-to-micronaut-1.0?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>经过一年的发展，随着Object Computing（OCI）发布候选版本RC1、RC2和RC3，Micronaut 1.0在过去三周内加速了。Micronaut是一个基于JVM的全栈框架，用于创建可以用Java、Groovy和Kotlin编写的基于微服务的应用程序。OCI的首席软件工程师Graeme Rocher向InfoQ介绍了Micronaut 1.0。</p> <i>By Michael Redlich</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_4" >5、Sharding-Sphere成长记——写在分布式数据库代理端里程碑版本3.0.0发布之际</h1>
张亮
[http://www.infoq.com/cn/news/2018/10/Sharding-Sphere-growth-process?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/10/Sharding-Sphere-growth-process?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>在历经八个月的紧张开发与精心打磨之后，Sharding-Sphere社区为程序员献礼，将Sharding-Sphere 3.0.0正式版于10月24日程序员节发布。在3.0.0发布之际，写下此文，与大家共同回顾这段充满纪念的时光，分享我们的前进历程。</p> <i>By 张亮</i>
---------------