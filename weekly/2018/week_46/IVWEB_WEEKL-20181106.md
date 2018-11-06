## 文章索引
1、 <a href="#1improve-animated-gif-performance-with-html5-video" >Improve Animated GIF Performance With HTML5 video</a><br/>
2、 <a href="#2react-native重构路线图发布" >React Native重构路线图发布！</a><br/>
3、 <a href="#3用云但不依赖云-英特尔与腾讯优图祭出新杀器" >用云但不依赖云 英特尔与腾讯优图祭出新杀器</a><br/>
4、 <a href="#4剖析腾讯知文智能问答机器人路在何方" >剖析腾讯知文，智能问答机器人路在何方？</a><br/>
5、 <a href="#5codeone主题演讲java未来已来" >CodeOne主题演讲：Java，未来已来</a><br/>
6、 <a href="#6mango的组织重构" >Mango的组织重构</a><br/>
7、 <a href="#7腾讯we2018现场报道用ai救命向宇宙发问全球顶尖科学家同台论道" >腾讯WE2018现场报道：用AI救命、向宇宙发问，全球顶尖科学家同台论道</a><br/>
8、 <a href="#8page-lifecycle-api-教程" >Page Lifecycle API 教程</a><br/>
9、 <a href="#9迷你书-paas凶猛" >迷你书： PaaS凶猛</a><br/>
10、 <a href="#10nosql数据库敏捷数据模型" >NoSQL数据库敏捷数据模型</a><br/>
11、 <a href="#11fex-技术周刊---2018/11/05" >FEX 技术周刊 - 2018/11/05</a><br/>
12、 <a href="#12google发布fluid-annotation数据标注速度提高三倍" >Google发布Fluid Annotation，数据标注速度提高三倍！</a><br/>
13、 <a href="#13文章-苏宁蛙测&sat在自动化测试方面的应用" >文章： 苏宁蛙测&SAT在自动化测试方面的应用</a><br/>
14、 <a href="#14微软正式发布azure-iot-central" >微软正式发布Azure IoT Central</a><br/>
15、 <a href="#15文章-苏宁大数据离线任务开发调度平台实践" >文章： 苏宁大数据离线任务开发调度平台实践</a><br/><h1 id="#title_0" >1、Improve Animated GIF Performance With HTML5 video</h1>
Ayo Isaiah
[https://www.smashingmagazine.com/2018/11/gif-to-video/](https://www.smashingmagazine.com/2018/11/gif-to-video/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/11/gif-to-video/" />
              <title>Improve Animated GIF Performance With HTML5 video</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>Improve Animated GIF Performance With HTML5 video</h1>
                  
                    
                    <address>Ayo Isaiah</address>
                  
                  <time datetime="2018-11-05T14:30:14&#43;01:00" class="op-published">2018-11-05T14:30:14+01:00</time>
                  <time datetime="2018-11-05T21:23:43&#43;00:00" class="op-modified">2018-11-05T21:23:43+00:00</time>
                </header>
                

<p>Animated GIFs have a lot going for them; they’re easy to make and work well enough in literally all browsers. But the GIF format was not originally intended for animation. The original design of the GIF format was to provide a way to compress multiple images inside a single file using a lossless compression algorithm (called LZW compression) which meant they could be downloaded in a reasonably short space of time, even on slow connections.</p>

<p>Later, basic animation capabilities were added which allowed the various images (frames) in the file to be painted with time delays. By default, the series of frames that constitute the animation was displayed only once, stopping after the last frame was shown. Netscape Navigator 2.0 was the first browser to added the ability for animated GIFs to loop, which lead to the rise of animated GIFs as we know them today.</p>

<p>As an animation platform, the GIF format is incredibly limited. Each frame in the animation is restricted to a palette of just 256 colors, and over the years, advances in compression technology has made leading to several improvements the way animations and video files are compressed and used. Unlike proper video formats, the GIF format does not take advantage of any of the new technology meaning that even a few seconds of content can lead to tremendously large file sizes since a lot of repetitive information is stored.</p>

<p>Even if you try to tweak the quality and length of a GIF with a tool like , converting animated GIFs to video can decrease load times and improve playback smoothness leading to a more pleasant user experience.</p>

<p>Hence, we’re going to look at  some techniques that enable us use HTML5 video as a drop in replacement for animated GIFs. We’ll learn how to convert animated GIFs to video files and examine how to properly embed these video files on the web so that they act just like a GIF would. Finally, we’ll consider a few potential drawbacks that you need to ponder before using this solution.</p>

<h3 id="convert-animated-gifs-to-video">Convert Animated GIFs To Video</h3>

<p>The first step is to convert GIF files to a video format. MP4 is the most widely supported format in browsers with almost 94% of all browsers enjoying support, so that’s a safe default.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e3895577-cd44-4905-93fa-ad0cd844cfd0/caniuse-mp4.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e3895577-cd44-4905-93fa-ad0cd844cfd0/caniuse-mp4.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e3895577-cd44-4905-93fa-ad0cd844cfd0/caniuse-mp4.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e3895577-cd44-4905-93fa-ad0cd844cfd0/caniuse-mp4.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e3895577-cd44-4905-93fa-ad0cd844cfd0/caniuse-mp4.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e3895577-cd44-4905-93fa-ad0cd844cfd0/caniuse-mp4.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e3895577-cd44-4905-93fa-ad0cd844cfd0/caniuse-mp4.png"
			sizes="100vw"
			alt="Support table on caniuse.com showing browser support for the MP4 video format"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			94% of all browsers support the MP4 format ()
		</figcaption>
	
</figure>


<p>Another option is the WebM format which offers high quality videos, often comparable to an MP4, but usually at a reduced file size. However, at this time, browser support is not as widespread so you can’t just go replacing MP4 files with their WebM equivalents.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e3895577-cd44-4905-93fa-ad0cd844cfd0/caniuse-mp4.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e3895577-cd44-4905-93fa-ad0cd844cfd0/caniuse-mp4.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e3895577-cd44-4905-93fa-ad0cd844cfd0/caniuse-mp4.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e3895577-cd44-4905-93fa-ad0cd844cfd0/caniuse-mp4.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e3895577-cd44-4905-93fa-ad0cd844cfd0/caniuse-mp4.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e3895577-cd44-4905-93fa-ad0cd844cfd0/caniuse-mp4.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e3895577-cd44-4905-93fa-ad0cd844cfd0/caniuse-mp4.png"
			sizes="100vw"
			alt="Support table on caniuse.com showing browser support for the WebM video format"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Internet Explorer and Safari are notable browsers without WebM support ()
		</figcaption>
	
</figure>


<p>However, because the <code>&lt;video&gt;</code>  tag supports multiple <code>&lt;source&gt;</code> files, we can serve WebM videos to browsers that support them while falling back to MP4 everywhere else.</p>

<p>Let’s go ahead and convert an animated GIF to both MP4 and WebM. There are several online tools that can help you do this, but many of them use  under the hood so we’ll skip the middle man and just use that instead. <code>ffmpeg</code> is a free and open source command line tool that is designed for the processing of video and audio files. It can also be used to convert an animated GIF to video formats.</p>

<p>To find out if you have <code>ffmpeg</code> on your machine, fire up a terminal and run the <code>ffmpeg</code> command. This should display some diagnostic information, otherwise, you’ll need to install it. Installation instructions for Windows, macOS and Linux can be found on .</p>



<aside class="product-panel product-panel__tilted product-panel--book" data-audience="non-subscriber">
    <div class="container product-panel--book__container">
      <div class="panel__description panel__description--book">
    <p>Getting workflow <em>just</em> right ain’t an easy task. So are proper estimates. Or alignment among different departments. That’s why we’ve set up <strong>“this-is-how-I-work”-sessions</strong> — with smart cookies sharing what works well for them. A part of the , of course.</p>
      <a href="https://smashed.by/workflowpanelmembership" class="btn btn--green btn--large">
        Explore Smashing Membership&nbsp;↬
      </a>
      </div>
      <div class="panel__image panel__image--book">
        <a href="https://smashed.by/workflowpanelmembership" class="books__book__image">
        <div class="books__book__img">
          <img src="https://www.smashingmagazine.com/images/smashing-cat/smashing-tv-box-cat.svg" alt="Smashing TV, with live sessions for professional designers and developers." width="310" height="400">
        </div>
      </a>
      </div>
    </div>
  </aside>




<p>To follow along with the commands that are included in this article, you can use any animated GIF file lying around on your computer or  which is just over 28MB. Let’s begin by converting a GIF to MP4 in the next section.</p>

<h4 id="convert-gif-to-mp4">Convert GIF To MP4</h4>

<p>Open up a terminal instance and navigate to the directory where the test gif is located then run the command below to convert it to an MP4 video file:</p>

<pre><code>ffmpeg -i animated.gif video.mp4</code></pre>

<p>This should output a new video file in the current directory after a few seconds depending on the size of the GIF file you’re converting. The <code>-i</code>  flag specifies the path to the input GIF file and the output file is specified afterwards (video.mp4 in this instance). Running this command on my 28MB GIF produces an MP4 file that is just 536KB in size, <strong>a 98% reduction</strong> in file size with roughly the same visual quality.</p>

<p>But we can go even further than that. <code>ffmpeg</code> has so many options that you can use to regulate the video output even further. One way is to employ an encoding method known as Constant Rate Factor (CRF) to trim the size of the MP4 output even further. Here’s the command you need to run:</p>

<pre><code>ffmpeg -i animated.gif -b:v 0 -crf 25 video.mp4</code></pre>

<p>As you can see, there are a couple of new flags in above command compared to the previous one. <code>-b:v</code> is normally used to limit the output bitrate, but when using CRF mode, it must be set to 0. The <code>-crf</code> flag controls the quality of the video output. It accepts a value between 0 and 51; the lower the value, the higher the video quality and file size.</p>

<p>Running the above command on the test GIF, trims down the video output to just 386KB with no discernable difference in quality. If you want to trim the size even further, you could increase the CRF value. Just keep in mind that higher values will lower the quality of the video file.</p>

<div class="sponsors__wide-place"></div>




<h4 id="convert-gif-to-webm">Convert GIF To WebM</h4>

<p>You can convert your GIF file to WebM by running the command below in the terminal:</p>

<pre><code>ffmpeg -i animated.gif -c vp9 -b:v 0 -crf 41 video.webm</code></pre>

<p>This command is almost the same as the previous one, with the exception of a new <code>-c</code> flag which is used to specify the codec that should be used for this conversion. We are using the <code>vp9</code> codec which succeeds the <code>vp8</code> codec.</p>

<p>In addition, I’ve adjusted the CRF value to 41 in this case since CRF values don’t necessarily yield the same quality across video formats. This particular value results in a WebM file that is 16KB smaller than the MP4 with roughly the same visual quality.</p>

<p>Now that we know how to convert animated GIFs to video files, let’s look at how we can imitate their behavior in the browser with the HTML5 <code>&lt;video&gt;</code> tag.</p>

<h3 id="replace-animated-gifs-with-video-in-the-browser">Replace Animated GIFs With Video In The Browser</h3>

<p>Making a video act like a GIF on a webpage is not as easy as dropping the file in an <code>&lt;img&gt;</code> tag, but it’s not so difficult either. The major qualities of animated GIFs to keep in mind are as follows:</p>

<ul>
<li>They play automatically</li>
<li>They loop continuously</li>
<li>They are silent</li>
</ul>

<p>While you get these qualities by default with GIF files, we can cause a video file to act the exact same way using a handful of attributes. Here’s how you’ll embed a video file to behave like a GIF:</p>

<pre><code class="language-html">&lt;video autoplay loop muted playsinline src="video.mp4"&gt;&lt;/video&gt;</code></pre>

<p>This markup instructs the browser to automatically start the video, loop it continuously, play no sound, and play inline without displaying any video controls. This gives the same experience as an animated GIF but with better performance.</p>

<p>To specify more that once source for a video, you can use the <code>&lt;source&gt;</code> element within the <code>&lt;video&gt;</code> tag like this:</p>

<pre><code class="language-html">&lt;video autoplay loop muted playsinline&gt;
    &lt;source src="video.webm" type="video/webm"&gt;
    &lt;source src="video.mp4" type="video/mp4"&gt;
&lt;/video&gt;</code></pre>

<p>This tells the browser to choose from the provided video files depending on format support. In this case, the WebM video will be downloaded and played if it’s supported, otherwise the MP4 file is used instead.</p>

<p>To make this more robust for older browsers which do not support HTML5 video, you could add some HTML content linking to the original GIF file as a fallback.</p>

<pre><code class="language-html">&lt;video autoplay loop muted playsinline&gt;
    &lt;source src="video.webm" type="video/webm"&gt;
    &lt;source src="video.mp4" type="video/mp4"&gt;
      
    Your browser does not support HTML5 video.       
    &lt;a href="/animated.gif"&gt;Click here to view original GIF&lt;/a&gt;
&lt;/video&gt;</code></pre>

<p>Or you could just add the GIF file directly in an <code>&lt;img&gt;</code> tag:</p>

<pre><code class="language-html">&lt;video autoplay loop muted playsinline&gt;
    &lt;source src="video.webm" type="video/webm"&gt;
    &lt;source src="video.mp4" type="video/mp4"&gt;
    &lt;img src="animated.gif"&gt;
&lt;/video&gt;</code></pre>

<p>Now that we’ve examined how to emulate animated GIFs in the browser with HTML5 video, let’s consider a few potential drawbacks to doing so in the next section.</p>

<h2 id="potential-drawbacks">Potential Drawbacks</h2>

<p>There are a couple of drawbacks you need to consider before adopting HTML5 video as a GIF replacement. It’s clearly not as convenient as simply uploading a GIF to a page and watch is just work everywhere. You need to encode it first, and it may be difficult to implement an automated solution that works well in all scenarios.</p>

<p>The safest thing would be to convert each GIF manually and check the result of the output to ensure a good balance between visual quality and file size. But on large projects, this may not be practical. In that case, it may be better to look to a service like  to do the heavy lifting for you.</p>

<p>Another problem is that unlike images, browsers do not preload video content. Because video files can be of any length, they’re often skipped until the main thread is ready to parse their content. This could delay the loading of a video file by several hundreds of milliseconds.</p>

<p>Additionally, there are quite a few restrictions on autoplaying videos especially on mobile. The  <code>muted</code> attribute is actually required for videos to autoplay in  even if the video does not contain an audio track, and where autoplay is disallowed, the user will only see a blank space where the video should have been. An example is Data Saver mode in Chrome for Android where autoplaying videos will not work even if you set up everything correctly.</p>

<p>To account for any of these scenarios, you should consider setting a placeholder image for the video using the <code>poster</code> attribute so that the video area is still populated with meaningful content if the video does not autoplay for some reason. Also consider using the  which allows the user to initiate playback even if video autoplay is disallowed.</p>

<h3 id="wrap-up">Wrap Up</h3>

<p>By replacing animated GIFs with HTML5 video, we can provide awesome GIF-like experiences without the performance and quality drawbacks associated with GIF files. Doing away with animated GIFs is worth serious consideration especially if your site is GIF-heavy.</p>

<p>There are websites already doing this:</p>

<ul>
<li></li>
<li></li>
<li></li>
</ul>

<p>Taking the time to convert the GIF files on your site to video can lead to a massive improvement in page load times. Provided your website is not too complex, it is fairly easy to implement and you can be up and running within a very short amount of time.</p>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(ra,dm)</span>
</div>


              </article>
            </body>
          </html>
---------------
<h1 id="#title_1" >2、React Native重构路线图发布！</h1>
覃云
[http://www.infoq.com/cn/news/2018/11/react-native-roadmap?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/11/react-native-roadmap?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Facebook正式公开了React Native重构计划的一些细节。</p> <i>By 覃云</i>
---------------
<h1 id="#title_2" >3、用云但不依赖云 英特尔与腾讯优图祭出新杀器</h1>
Jackson
[http://www.infoq.com/cn/news/2018/11/MovidiusAtTencent?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/11/MovidiusAtTencent?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p></p> <i>By Jackson</i>
---------------
<h1 id="#title_3" >4、剖析腾讯知文，智能问答机器人路在何方？</h1>
陈利鑫
[http://www.infoq.com/cn/news/2018/11/tencent-NLP-road?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/11/tencent-NLP-road?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>如今，NLP和语音技术在商业化应用上遇到了哪些瓶颈？为何迟迟没有大的进步？解决问题的关键在于哪里？或许我们可以通过智能对话机器人的典型代表——腾讯知文问答系统，发掘当前智能对话机器人破解行业应用难题的答案。</p> <i>By 陈利鑫</i>
---------------
<h1 id="#title_4" >5、CodeOne主题演讲：Java，未来已来</h1>
Daniel Bryant
[http://www.infoq.com/cn/news/2018/11/codeone-java-keynote?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/11/codeone-java-keynote?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>在上一次JavaOne大会之后，首届Oracle CodeOne大会最近于美国旧金山举行。周一晚上主旨演讲的头条是“Java：未来已来”，其中包括：新的Java/JDK的发布节奏正在按计划进行；Oracle和许多其他组织将继续支持Java并为之做出贡献，等等。</p> <i>By Daniel Bryant</i> <i> Translated by 姚佳灵</i>
---------------
<h1 id="#title_5" >6、Mango的组织重构</h1>
Ben Linders
[http://www.infoq.com/cn/news/2018/11/organizational-refactoring-mango?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/11/organizational-refactoring-mango?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>为了提高敏捷性，企业应将自己划分为一些负责业务战略计划价值中心，，承担端到端的责任，并完全获取有关客户需求的信息。企业需要为员工营造可交叉协作和学习的空间，使用自组织等方式改进工作圈、实践社群（CoP，Communities of Practice）或内部开源模型。</p> <i>By Ben Linders</i> <i> Translated by 盖磊</i>
---------------
<h1 id="#title_6" >7、腾讯WE2018现场报道：用AI救命、向宇宙发问，全球顶尖科学家同台论道</h1>
陈思
[http://www.infoq.com/cn/news/2018/11/tencent-we-2018?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/11/tencent-we-2018?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>11月4日，2018腾讯WE大会在北京举行。七位来自全球的顶尖科学家，在会上揭晓了天文、物理、生命科学等多个领域的重大科学进展。腾讯与自然集团联合创立的“自然科研全球影响力大奖”正式发布，奖项设立第一年将表彰为“脑科学”做出重大贡献的青年科学家。本届WE大会还聚焦通过前沿科技解决全球性难题，腾讯首席探索官网大为介绍了腾讯打造的“救命的AI”，并展望了人工智能在星球管理中的应用前景。</p> <i>By 陈思</i>
---------------
<h1 id="#title_7" >8、Page Lifecycle API 教程</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2018/11/page_lifecycle_api.html](http://www.ruanyifeng.com/blog/2018/11/page_lifecycle_api.html)
<p>两周前，我介绍了 。有了它，就可以监听各种情况的网页卸载。</p>

        <p>但是，它没有解决一个问题。Android、iOS 和最新的 Windows 系统可以随时自主地停止后台进程，及时释放系统资源。也就是说，网页可能随时被系统丢弃掉。Page Visibility API 只在网页对用户不可见时触发，至于网页会不会被系统丢弃掉，它就无能为力了。</p>

<p>为了解决这个问题，W3C 新制定了一个 ，统一了网页从诞生到卸载的行为模式，并且定义了新的事件，允许开发者响应网页状态的各种转换。</p>

<p>有了这个 API，开发者就可以预测网页下一步的状态，从而进行各种针对性的处理。Chrome 68 支持这个 API，对于老式浏览器可以使用谷歌开发的兼容库 。</p>

<h2>一、生命周期阶段</h2>

<p>网页的生命周期分成六个阶段，每个时刻只可能处于其中一个阶段。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201811/bg2018110401.png" alt="" title="" /></p>

<p><strong>（1）Active 阶段</strong></p>

<p>在 Active 阶段，网页处于可见状态，且拥有输入焦点。</p>

<p><strong>（2）Passive 阶段</strong></p>

<p>在 Passive 阶段，网页可见，但没有输入焦点，无法接受输入。UI 更新（比如动画）仍然在执行。该阶段只可能发生在桌面同时有多个窗口的情况。</p>

<p><strong>（3）Hidden 阶段</strong></p>

<p>在 Hidden 阶段，用户的桌面被其他窗口占据，网页不可见，但尚未冻结。UI 更新不再执行。</p>

<p><strong>（4）Terminated 阶段</strong></p>

<p>在 Terminated 阶段，由于用户主动关闭窗口，或者在同一个窗口前往其他页面，导致当前页面开始被浏览器卸载并从内存中清除。注意，这个阶段总是在 Hidden 阶段之后发生，也就是说，用户主动离开当前页面，总是先进入 Hidden 阶段，再进入 Terminated 阶段。</p>

<p>这个阶段会导致网页卸载，任何新任务都不会在这个阶段启动，并且如果运行时间太长，正在进行的任务可能会被终止。</p>

<p><strong>（5）Frozen 阶段</strong></p>

<p>如果网页处于 Hidden 阶段的时间过久，用户又不关闭网页，浏览器就有可能冻结网页，使其进入 Frozen 阶段。不过，也有可能，处于可见状态的页面长时间没有操作，也会进入 Frozen 阶段。</p>

<p>这个阶段的特征是，网页不会再被分配 CPU 计算资源。定时器、回调函数、网络请求、DOM 操作都不会执行，不过正在运行的任务会执行完。浏览器可能会允许 Frozen 阶段的页面，周期性复苏一小段时间，短暂变回 Hidden 状态，允许一小部分任务执行。</p>

<p><strong>（6）Discarded 阶段</strong></p>

<p>如果网页长时间处于 Frozen 阶段，用户又不唤醒页面，那么就会进入 Discarded 阶段，即浏览器自动卸载网页，清除该网页的内存占用。不过，Passive 阶段的网页如果长时间没有互动，也可能直接进入 Discarded 阶段。</p>

<p>这一般是在用户没有介入的情况下，由系统强制执行。任何类型的新任务或 JavaScript 代码，都不能在此阶段执行，因为这时通常处在资源限制的状况下。</p>

<p>网页被浏览器自动 Discarded 以后，它的 Tab 窗口还是在的。如果用户重新访问这个 Tab 页，浏览器将会重新向服务器发出请求，再一次重新加载网页，回到 Active 阶段。</p>

<h2>二、常见场景</h2>

<p>以下是几个常见场景的网页生命周期变化。</p>

<p>（1）用户打开网页后，又切换到其他 App，但只过了一会又回到网页。</p>

<p>网页由 Active 变成 Hidden，又变回 Active。</p>

<p>（2）用户打开网页后，又切换到其他 App，并且长时候使用后者，导致系统自动丢弃网页。</p>

<p>网页由 Active 变成 Hidden，再变成 Frozen，最后 Discarded。</p>

<p>（3）用户打开网页后，又切换到其他 App，然后从任务管理器里面将浏览器进程清除。</p>

<p>网页由 Active 变成 Hidden，然后 Terminated。</p>

<p>（4）系统丢弃了某个 Tab 里面的页面后，用户重新打开这个 Tab。</p>

<p>网页由 Discarded 变成 Active。</p>

<h2>三、事件</h2>

<p>生命周期的各个阶段都有自己的事件，以供开发者指定监听函数。这些事件里面，只有两个是新定义的（<code>freeze</code>事件和<code>resume</code>事件），其它都是现有的。</p>

<p>注意，网页的生命周期事件是在所有帧（frame）触发，不管是底层的帧，还是内嵌的帧。也就是说，内嵌的<code>&lt;iframe&gt;</code>网页跟顶层网页一样，都会同时监听到下面的事件。</p>

<h3>3.1 focus 事件</h3>

<p><code>focus</code>事件在页面获得输入焦点时触发，比如网页从 Passive 阶段变为 Active 阶段。</p>

<h3>3.2 blur 事件</h3>

<p><code>blur</code>事件在页面失去输入焦点时触发，比如网页从 Active 阶段变为 Passive 阶段。</p>

<h3>3.3 visibilitychange 事件</h3>

<p><code>visibilitychange</code>事件在网页可见状态发生变化时触发，一般发生在以下几种场景。</p>

<blockquote>
  <ul>
<li>用户隐藏页面（切换 Tab、最小化浏览器），页面由 Active 阶段变成 Hidden 阶段。</li>
<li>用户重新访问隐藏的页面，页面由 Hidden 阶段变成 Active 阶段。</li>
<li>用户关闭页面，页面会先进入 Hidden 阶段，然后进入 Terminated 阶段。</li>
</ul>
</blockquote>

<p>可以通过<code>document.onvisibilitychange</code>属性指定这个事件的回调函数。</p>

<h3>3.4 freeze 事件</h3>

<p><code>freeze</code>事件在网页进入 Frozen 阶段时触发。</p>

<p>可以通过<code>document.onfreeze</code>属性指定在进入 Frozen 阶段时调用的回调函数。</p>

<blockquote><pre><code class="language-javascript">
function handleFreeze(e) {
  // Handle transition to FROZEN
}
document.addEventListener('freeze', handleFreeze);

# 或者
document.onfreeze = function() { ... }
</code></pre></blockquote>

<p>这个事件的监听函数，最长只能运行500毫秒。并且只能复用已经打开的网络连接，不能发起新的网络请求。</p>

<p>注意，从 Frozen 阶段进入 Discarded 阶段，不会触发任何事件，无法指定回调函数，只能在进入 Frozen 阶段时指定回调函数。</p>

<h3>3.5 resume 事件</h3>

<p><code>resume</code>事件在网页离开 Frozen 阶段，变为 Active / Passive / Hidden 阶段时触发。</p>

<p><code>document.onresume</code>属性指定用户重新访问页面，是的页面离开 Frozen 阶段、进入可用阶段时调用的回调函数。</p>

<blockquote><pre><code class="language-javascript">
function handleResume(e) {
  // handle state transition FROZEN -> ACTIVE
}
document.addEventListener("resume", handleResume);

# 或者
document.onresume = function() { ... }
</code></pre></blockquote>

<h3>3.6 pageshow 事件</h3>

<p><code>pageshow</code>事件在用户加载网页时触发。这时，有可能是全新的页面加载，也可能是从缓存中获取的页面。如果是从缓存中获取，则该事件对象的<code>event.persisted</code>属性为<code>true</code>，否则为<code>false</code>。</p>

<p>这个事件的名字有点误导，它跟页面的可见性其实毫无关系，只跟浏览器的 History 记录的变化有关。</p>

<h3>3.7 pagehide 事件</h3>

<p><code>pagehide</code>事件在用户离开当前网页、进入另一个网页时触发。它的前提是浏览器的 History 记录必须发生变化，跟网页是否可见无关。</p>

<p>如果浏览器能够将当前页面添加到缓存以供稍后重用，则事件对象的<code>event.persisted</code>属性为<code>true</code>。 如果为<code>true</code>。如果页面添加到了缓存，则页面进入 Frozen 状态，否则进入 Terminatied 状态。</p>

<h3>3.8 beforeunload 事件</h3>

<p><code>beforeunload</code>事件在窗口或文档即将卸载时触发。该事件发生时，文档仍然可见，此时卸载仍可取消。经过这个事件，网页进入 Terminated 状态。</p>

<h3>3.9 unload 事件</h3>

<p><code>unload</code>事件在页面正在卸载时触发。经过这个事件，网页进入 Terminated 状态。</p>

<h2>四、获取当前阶段</h2>

<p>如果网页处于 Active、Passive 或 Hidden 阶段，可以通过下面的代码，获得网页当前的状态。</p>

<blockquote><pre><code class="language-javascript">
const getState = () => {
  if (document.visibilityState === 'hidden') {
    return 'hidden';
  }
  if (document.hasFocus()) {
    return 'active';
  }
  return 'passive';
};
</code></pre></blockquote>

<p>如果网页处于 Frozen 和 Terminated 状态，由于定时器代码不会执行，只能通过事件监听判断状态。进入 Frozen 阶段，可以监听<code>freeze</code>事件；进入 Terminated 阶段，可以监听<code>pagehide</code>事件。</p>

<h2>五、document.wasDiscarded</h2>

<p>如果某个选项卡处于 Frozen 阶段，就随时有可能被系统丢弃，进入 Discarded 阶段。如果后来用户再次点击该选项卡，浏览器会重新加载该页面。</p>

<p>这时，开发者可以通过判断<code>document.wasDiscarded</code>属性，了解先前的网页是否被丢弃了。</p>

<blockquote><pre><code class="language-javascript">
if (document.wasDiscarded) {
  // 该网页已经不是原来的状态了，曾经被浏览器丢弃过
  // 恢复以前的状态
  getPersistedState(self.discardedClientId);
}
</code></pre></blockquote>

<p>同时，<code>window</code>对象上会新增<code>window.clientId</code>和<code>window.discardedClientId</code>两个属性，用来恢复丢弃前的状态。</p>

<h2>六、参考链接</h2>

<ul>
<li>, Philip Walton</li>
<li>, W3C</li>
<li>, W3C</li>
</ul>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2018-11-05T17:13:14+08:00">2018年11月 5日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>文集：</li>
<li>社交媒体：</li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------
<h1 id="#title_8" >9、迷你书： PaaS凶猛</h1>
InfoQ&BoCloud 博云
[http://www.infoq.com/cn/minibooks/boyun-minibook-paas?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/minibooks/boyun-minibook-paas?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/minibooks/boyun-minibook-paas/zh/smallimage/100-1541403257780.jpg"/><p>BoCloud技术特刊。</p> <i>By InfoQ&BoCloud 博云</i>
---------------
<h1 id="#title_9" >10、NoSQL数据库敏捷数据模型</h1>
Srini Penchikala
[http://www.infoq.com/cn/news/2018/11/agile-data-modeling-nosql?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/11/agile-data-modeling-nosql?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>在近日举行的2018年数据架构峰会上，Pascal Desmarets谈了NoSQL数据库的敏捷建模和最佳实践。</p> <i>By Srini Penchikala</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_10" >11、FEX 技术周刊 - 2018/11/05</h1>

[http://fex.baidu.com/blog/2018/11/fex-weekly-05//](http://fex.baidu.com/blog/2018/11/fex-weekly-05//)
作者：nwind <br> <h2 id="业界会议">业界会议</h2>

<p><strong>React Conf 2018</strong><br />
https://conf.reactjs.org/<br />
附：.</p>

<h2 id="深阅读">深阅读</h2>

<p><strong>V8 release v7.1</strong><br />
https://v8.dev/blog/v8-release-71<br />
V8 v7.1 is filled with all sorts of developer-facing goodies. This post provides a preview of some of the highlights in anticipation of the release.</p>

<p><strong>React Native - Open Source Roadmap</strong><br />
http://facebook.github.io/react-native/blog/2018/11/01/oss-roadmap<br />
This year, the React Native team has focused on a large scale re-architecture of React Native. As Sophie mentioned in her State of React Native post, we’ve sketched out a plan to better support the thriving population of React Native users and collaborators outside of Facebook. It’s now time to share more details about what we’ve been working on. Before I do so, I’d like to lay out our long-term vision for React Native in open source. 附：.</p>

<p><strong>Making Sense of React Hooks</strong><br />
https://medium.com/@dan_abramov/making-sense-of-react-hooks-fdbde8803889<br />
Hooks are an experimental proposal to React. You don’t need to learn about them right now. Also, note that this post contains my personal opinions and doesn’t necessarily reflect the positions of the React team. 另附：.</p>

<p><strong>An Annotated webpack 4 Config for Frontend Web Development</strong><br />
https://nystudio107.com/blog/an-annotated-webpack-4-config-for-frontend-web-development<br />
As web devel­op­ment becomes more com­plex, we need tool­ing to help us build mod­ern web­sites. Here’s a com­plete real-world pro­duc­tion exam­ple of a sophis­ti­cat­ed web­pack 4 config. Build­ing a mod­ern web­site has become cus­tom appli­ca­tion devel­op­ment. Web­sites are expect­ed to do more than just be mar­ket­ing sites as they take on the func­tion­al­i­ty of tra­di­tion­al apps. Any time a process becomes com­pli­cat­ed, we break it down into man­age­able com­po­nents, and auto­mate the build process with tool­ing. This is the case in whether we are man­u­fac­tur­ing cars, draft­ing legal doc­u­ments, or build­ing websites.</p>

<p><strong>The Definitive TypeScript Guide</strong><br />
https://www.sitepen.com/blog/2018/10/29/update-the-definitive-typescript-guide/<br />
This article describes the features and functionality of TypeScript 3.1.</p>

<p><strong>Splicing HTML’s DNA With CSS Attribute Selectors</strong><br />
https://www.smashingmagazine.com/2018/10/attribute-selectors-splicing-html-dna-css/<br />
Attribute selectors are magical. They can get you out of sticky problems, help you avoid adding classes and point out some problems in your code. But don’t worry, while attribute selectors are complex and powerful, they’re easy to learn and easy to utilize. In this article, we’ll discuss how they operate and give you some ideas about how to use them.</p>

<p><strong>克军：如何成为一位优秀的前端工程师</strong><br />
https://www.weibo.com/ttarticle/p/show?id=2309404300456787613157<br />
有很多关于成长的建议，值得拜读和实践。</p>

<p><strong>富文本编辑器的技术演进之路</strong><br />
https://mp.weixin.qq.com/s?__biz=MzU0Nzk1MTg5OA==&amp;mid=2247484137&amp;idx=1&amp;sn=8dc25f8de7d359549520c9f198721408 <br />
浏览器提供了两个原生特性：contenteditable、document.execCommand()，contenteditable 特性，可以指定某一容器变成可编辑器区域，即用户可以在容器内直接输入内容，或者删减内容。execCommand API，可以对选中的某一段结构体，执行一个命令，譬如赋予黑体格式。基于以上，可以做出最简单的富文本编辑器。原来富文本编辑器是这么简单？当然不止如此简单！另附：.</p>

<p><strong>Atag - Web Components 最佳实践</strong><br />
http://taobaofed.org/blog/2018/10/31/a-tag/<br />
过去一段时间，我一直在使用 Web Components 构建淘宝小程序的 基础组件 Atag。这篇文章的目的，是希望总结在 Atag 开发阶段中使用 Web Components 的经验，避免大家踩坑。另附：.</p>

<p><strong>蚂蚁金服移动开发平台mPaaS</strong><br />
https://juejin.im/post/5bd81cf2f265da0ab674096c<br />
Android 拆分项目的方案</p>

<p><strong>Web Performance 101</strong><br />
https://3perf.com/talks/web-perf-101/<br />
This is an introduction to the modern web loading performance. Learn why performance is important, what performance optimizations exist and what tools help to understand if your app is doing well.</p>

<p><strong>You Might Not Need JavaScript</strong><br />
http://youmightnotneedjs.com/<br />
JavaScript is great, and by all means use it, while also being aware that you can build so many functional UI components without the additional dependancy. Maybe you can include a few lines of utility code, or a mixin, and forgo the requirement. If you’re only targeting more modern browsers, you might not need anything more than what the browser ships with. We take a look at the power of modern native HTML and CSS as well as some of the syntactic sugar of Sass. Because, you might not need scripts for that task at all!</p>

<p><strong>Creating a QR Code step by step</strong><br />
https://www.nayuki.io/page/creating-a-qr-code-step-by-step<br />
This JavaScript demo application visualizes in detailed steps, how a text string is encoded into a QR Code barcode symbol. The content of this page essentially explains and justifies how my  works internally.</p>

<p><strong>GraphQL - The Good and the Bad</strong><br />
https://scotch.io/tutorials/graphql-the-good-and-the-bad<br />
GraphQL is a query language for APIs and a runtime for fulfilling those queries with your existing data. GraphQL provides a complete and understandable description of the data in your API as well as gives clients the power to ask for exactly what they need and nothing more. It makes it easier to evolve APIs over time and enables powerful developer tools. At least that’s what we all know it to be. In this post, we’ll look at all the wonderful things about GraphQL and also look at the unpopular “not so good” things about it. 另附：.</p>

<p><strong>Best Practices for Setting SLOs and SLIs For Modern, Complex Systems</strong><br />
https://blog.newrelic.com/engineering/best-practices-for-setting-slos-and-slis-for-modern-complex-systems/ <br />
At New Relic, defining and setting Service Level Indicators (SLIs) and Service Level Objectives (SLOs) is an increasingly important aspect of our site reliability engineering (SRE) practice. It’s not news that SLIs and SLOs are an important part of high-functioning reliability practices, but planning how to apply them within the context of a real-world, complex modern software architecture can be challenging, especially figuring out what to measure and how to measure it. In this post, we’ll use a highly simplified version of New Relic’s architecture to walk you through some concrete, practical examples of how we define and measure SLIs and SLOs for our own modern software platform.</p>

<p><strong>API Profiling at Pinterest</strong><br />
https://medium.com/@Pinterest_Engineering/api-profiling-at-pinterest-6fa9333b4961<br />
When I walked into Pinterest on the first day of my internship and learned I’d be focusing on profiling the API Gateway service — the core backend service of the Pinterest product — my only thought was “What is profiling?”. Profiling is often shoved aside as a side project or as a lower priority concern, and not one typically taught in my college CS courses. Essentially, the services come first, and profiling of is a far second.</p>

<p><strong>Node.js Everywhere with Environment Variables!</strong><br />
https://medium.com/the-node-js-collection/making-your-node-js-work-everywhere-with-environment-variables-2da8cdf6e786 <br />
This post walks you through creating and using environment variables, leading to a Node.js app you can run anywhere.</p>

<p><strong>NGINX Unit Now Supports TLS and JavaScript Apps with Node.js</strong><br />
https://www.nginx.com/blog/nginx-unit-1-5-available-now/<br />
In this post we cover the configuration of TLS certificates and Node.js applications in detail.</p>

<p><strong>October 21 post-incident analysis</strong><br />
https://blog.github.com/2018-10-30-oct21-post-incident-analysis/<br />
GitHub experienced an incident that resulted in degraded service for 24 hours and 11 minutes. While portions of our platform were not affected by this incident, multiple internal systems were affected which resulted in our displaying of information that was out of date and inconsistent. Ultimately, no user data was lost; however manual reconciliation for a few seconds of database writes is still in progress. For the majority of the incident, GitHub was also unable to serve webhook events or build and publish GitHub Pages sites. 另附：.</p>

<p><strong>Why we use Ruby on Rails to build GitLab</strong><br />
https://about.gitlab.com/2018/10/29/why-we-use-rails-to-build-gitlab/<br />
Here’s our CEO on GitLab’s inception using Rails, and how challenges are being handled along the way. 另附：.</p>

<p><strong>Why Jupyter is data scientists’ computational notebook of choice</strong><br />
https://www.nature.com/articles/d41586-018-07196-1<br />
For data scientists, Jupyter has emerged as a de facto standard, says Lorena Barba, a mechanical and aeronautical engineer at George Washington University in Washington DC. Mario Jurić, an astronomer at the University of Washington in Seattle who coordinates the LSST’s data-management team, says: “I’ve never seen any migration this fast. It’s just amazing.”</p>

<p><strong>The differing definitions of “serverless”</strong><br />
https://winterwindsoftware.com/serverless-definitions/<br />
A serverless solution is one where developers are freed up to focus more on application development without needing to worry about provisioning, scaling or maintaining servers (or containers), and whose running costs are proportional to the system’s usage levels.</p>

<p><strong>A Look at the Design of Lua</strong><br />
https://cacm.acm.org/magazines/2018/11/232214-a-look-at-the-design-of-lua/fulltext<br />
Though mainly a procedural language, Lua lends itself to several other paradigms, including object-oriented programming, functional programming, and data-driven programming.5 It also offers good support for data description, in the style of JavaScript and JSON. Data description was indeed one of our main motivations for creating Lua, some years before the appearance of XML and JavaScript. 另附：.</p>

<h2 id="新鲜货">新鲜货</h2>

<p><strong>Carlo: Web rendering surface for Node applications by Google Chrome</strong><br />
https://github.com/GoogleChromeLabs/carlo<br />
Carlo provides Node applications with the rich rendering capabilities powered by the Google Chrome browser. It uses Puppeteer project to communicate with the locally installed browser instance, provides remote call infrastructure for communication between Node and the browser.</p>

<p><strong>Facebook open-sources new suite of Linux kernel components and tools</strong><br />
https://code.fb.com/open-source/linux/<br />
We are announcing a suite of open source Linux kernel components and related tools that address critical fleet management issues. These include resource control, resource utilization, workload isolation, load balancing, measuring, monitoring, and much more.</p>

<p><strong>Storybook 4.0 is here!</strong><br />
https://medium.com/storybookjs/storybook-4-0-is-here-10b9857fc7de<br />
Storybook 4.0 (SB4) supports six new view layers and introduces improvements at every level: View layers: Ember, MarkoJS, Mithril, HTML, Svelte, Riot; Build: Webpack 4, Babel 7; Mobile: React Native, Mobile device view; UI: Theming; Core: Story parameters.</p>

<p><strong>The CSS Working Group At TPAC: What’s New In CSS?</strong><br />
https://www.smashingmagazine.com/2018/10/tpac-css-working-group-new/<br />
Last week, Rachel Andrew attended the CSS Working Group meeting at W3C TPAC, and rounds up some of the discussions in this post — including those things where you can help make a decision.</p>

<p><strong>Foundation 6.5.0 Released</strong><br />
https://medium.com/@ncoden/foundation-6-5-0-released-f405d8561ed7<br />
Foundation 6.5 in a few words: Over 100 bugs fixed, more customization, more accessible and better supported!</p>

<p><strong>Google 万圣节小游戏</strong><br />
https://www.google.com/doodles/halloween-2018<br />
Today’s annual Halloween Doodle marks a wickedly exciting milestone: our first-ever multiplayer interactive game Doodle, powered by Google Cloud! Join in as ghosts around the world gather to play their own version of Trick-or-Treat: The Great Ghoul Duel! Ghosts team up and compete to see who can collect the most wandering spirit flames before the moon is gone….but not without some unexpected twists along the way.</p>

<p><strong>JavaScript Visualizer</strong><br />
https://tylermcginnis.com/javascript-visualizer/<br />
A tool for visualizing Execution Context, Hoisting, Closures, and Scopes in JavaScript.</p>

<p><strong>libreact</strong><br />
https://github.com/streamich/libreact<br />
React 工具类库.</p>

<p><strong>Create React App 2.1</strong><br />
https://github.com/facebook/create-react-app/releases/tag/v2.1.0<br />
Create React App 2.1 adds support for TypeScript! New applications can be created using TypeScript by running: <code class="highlighter-rouge">$ npx create-react-app my-app --typescript</code></p>

<p><strong>React Material Web Components</strong><br />
https://jamesmfriedman.github.io/rmwc/<br />
A React wrapper for Google’s official Material Components for the Web.</p>

<p><strong>React SimpleMDE Markdown Editor</strong><br />
https://github.com/RIP21/react-simplemde-editor<br />
React wrapper for simplemde markdown editor: https://github.com/sparksuite/simplemde-markdown-editor.</p>

<p><strong>howler.js - JavaScript audio library for the modern web</strong><br />
https://howlerjs.com/<br />
howler.js makes working with audio in JavaScript easy and reliable across all platforms.</p>

<p><strong>Ervy - Bring charts to terminal</strong><br />
https://www.chunqiuyiyu.com/ervy/#started<br />
Why build this: There is no special reason, just because I love terminal and ASCII art. It’s very cool! Hope you enjoy Ervy and make your terminal more beautiful.</p>

<p><strong>simple-keyboard</strong><br />
https://virtual-keyboard.js.org/<br />
Meet the slick virtual keyboard for Javascript. Compatible with your ES6, React, Vue, Angular or jQuery projects.</p>

<p><strong>SimpleBar</strong><br />
https://github.com/Grsmto/simplebar<br />
Custom scrollbars vanilla javascript library with native scroll, done simple, lightweight, easy to use and cross-browser.</p>

<p><strong>Introducing AloeStackView for iOS</strong><br />
https://medium.com/airbnb-engineering/introducing-aloestackview-for-ios-a676d253c6ba<br />
A simple, open source class for laying out a collection of views with a convenient API.</p>

<p><strong>DeepCreamPy</strong><br />
https://github.com/deeppomf/DeepCreamPy<br />
Decensoring Hentai with Deep Neural Networks. Formerly named DeepMindBreak. A deep learning-based tool to automatically replace censored artwork in hentai with plausible reconstructions. The user specifies the censored regions in each image by coloring those regions green in a separate image editing program like GIMP or Photoshop. A neural network handles the hard part of filling in the censored regions.</p>

<p><strong>Algojammer</strong><br />
https://github.com/ChrisKnott/Algojammer<br />
Algojammer is an experimental, proof-of-concept code editor for writing algorithms in Python. It was mainly written to assist with solving the kind of algorithm problems that feature in competitions like Google Code Jam, Topcoder and HackerRank.</p>

<p><strong>谷歌最强NLP模型BERT开源</strong><br />
https://mp.weixin.qq.com/s/xch7eJoqa9BUCEG-mgxQDA<br />
https://github.com/google-research/bert#fine-tuning-with-bert<br />
BERT全称Bidirectional Encoder Representations from Transformers，是预训练语言表示的方法，可以在大型文本语料库（如维基百科）上训练通用的“语言理解”模型，然后将该模型用于下游NLP任务，比如机器翻译、问答。BERT是第一个无监督的用于预训练NLP的深度双向系统。无监督意味着BERT仅使用文本语料库进行训练，也就是说网络上有大量多种语言文本数据可供使用。另附：.</p>

<p><strong>Introducing reCAPTCHA v3: the new way to stop bots</strong><br />
https://webmasters.googleblog.com/2018/10/introducing-recaptcha-v3-new-way-to.html<br />
In reCAPTCHA v3, we are introducing a new concept called “Action”—a tag that you can use to define the key steps of your user journey and enable reCAPTCHA to run its risk analysis in context.</p>

<p><strong>NixOS - The Purely Functional Linux Distribution</strong><br />
https://nixos.org/<br />
NixOS is a Linux distribution with a unique approach to package and configuration management. Built on top of the Nix package manager, it is completely declarative, makes upgrading systems reliable, and has many other advantages.</p>

<h2 id="设计">设计</h2>

<p><strong>Your Face Here - Creating illustration guidelines for a more inclusive visual identity</strong><br />
https://medium.com/dropbox-design/4-ways-to-show-the-value-of-ux-writing-4369d84a6afd<br />
One of my career goals is to elevate the quality of illustration in tech. Airbnb’s design brand is a harmony of many disciplines—a chorus of experience and motion design, photography, writing, data visualization, and illustration. When I joined the team in October of 2017, I was given the opportunity to redesign Airbnb’s illustration style as a key component of our core identity system. Here’s how my journey unfolded.</p>

<p><strong>From URL to Interactive</strong><br />
https://alistapart.com/article/from-url-to-interactive<br />
Imagine, if you will, that you’re behind the wheel of a gorgeous 1957 Chevy Bel Air convertible, making your way across the desert on a wide open highway. The sun is setting, so you’ve got the top down, naturally. The breeze caresses your cheek like a warm hand as your nose catches a faint whiff of … What was that?</p>

<p><strong>Why you should stop being a UI designer</strong><br />
https://uxdesign.cc/why-you-should-stop-being-a-ui-designer-and-become-a-ui-redesigner-instead-9a08b8ec0186<br />
Designers need to stop viewing themselves as “creators” and wear the “rebuilders” hat, in order to have a better understanding of their product.</p>

<p><strong>Designing an Enterprise Application</strong><br />
https://www.lollypop.design/blog/2018/october/designing-an-enterprise-application/<br />
Designing an enterprise app is complex and requires stitching hundreds of separate requirements together to produce a product that is functional, assistive and delightful, all at the same time. Though it sounds really easy, in practice it is an extremely gruesome process and every designer that opts to be part of an enterprise app designing process should understand in entirety the commitment, patience, and endless hours it requires.</p>

<h2 id="产品及其它">产品及其它</h2>

<p><strong>Father of Web says tech giants may have to be split up</strong><br />
https://www.reuters.com/article/us-technology-www/father-of-web-says-tech-giants-may-have-to-be-split-up-idUSKCN1N63MV<br />
Tim Berners-Lee, a London-born computer scientist who invented the Web in 1989, said he was disappointed with the current state of the internet, following scandals over the abuse of personal data and the use of social media to spread hate. “What naturally happens is you end up with one company dominating the field so through history there is no alternative to really coming in and breaking things up,” Berners-Lee, 63, said in an interview. “There is a danger of concentration.”</p>

<p><strong>专访 Bear - Markdown 笔记应用</strong><br />
https://sspai.com/post/47756<br />
说起 Markdown 写作工具，Bear 可能并不如它的前辈像 Ulysses 等那么有名，但是凭借足够简洁的设计和足够优秀的写作体验，Bear 依然在一经推出就收获了大量的好评和忠实用户，并在去年获得了Apple Design Awards 年度设计大奖。另附：.</p>

<p><strong>互联网考古地图</strong><br />
https://www.huxiu.com/article/269319.html<br />
在关于互联网的早期历史方面，我最近看到一份资料，集合了过去二十多年关于互联网的所有较为知名的创意。它所提及的 100 个网站，曾经在全球范围内获得广泛的影响力，很有群众基础，相当值得研究。这种“考古”工作有价值的一点大概在于，当年互联网还非常稚嫩的时候，是活生生的、各式各样有趣的人创造了经典，他们尝试过、努力过、也遗憾过，是他们塑造了今天的互联网。</p>

<p><strong>曾鸣新作出版 - 智能商业</strong><br />
https://mp.weixin.qq.com/s?__biz=MzI0NzY3Mjc0Mw==&amp;mid=2247484764&amp;idx=1&amp;sn=81480a112e07c6c064a3bff5c60ffd54<br />
曾鸣教授在本书中做出对未来的预判：未来的商业必然是智能商业。让更多对未来的思考关照到当下的商业世界。附：。</p>

<p><strong>你可能没读懂的金庸文学伟业</strong><br />
https://mp.weixin.qq.com/s?__biz=MzA4NDEzNTMyMA==&amp;mid=2650318284&amp;idx=1&amp;sn=b1cd2fb2b21c2169be7bd96d8ec0d0a1<br />
金庸在文学上的最高成就，我认为是他不但塑造了一大批一流的文学人物，而且居然用武侠小说这种超级不严肃的东西，进行了最庄严的文学探讨，开展了触及人类灵魂的叩问。而在这种叩问之中，竟然还穿插着神奇瑰丽的想象世界，风光旖旎的爱情，热血激昂的侠义精神。另附：.</p>

<p>– THE END –</p>
---------------
<h1 id="#title_11" >12、Google发布Fluid Annotation，数据标注速度提高三倍！</h1>
Jasper Uijlings
[http://www.infoq.com/cn/news/2018/11/google-fluid-annotation?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/11/google-fluid-annotation?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>我们能不能让机器解放数据标注员呢？Google AI 就推出了 Fluid Annotation ，旨在提高数据标注的能力。</p> <i>By Jasper Uijlings</i> <i> Translated by 刘志勇</i>
---------------
<h1 id="#title_12" >13、文章： 苏宁蛙测&SAT在自动化测试方面的应用</h1>
卢烨
[http://www.infoq.com/cn/articles/suning-test-sat?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/suning-test-sat?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/suning-test-sat/zh/smallimage/02-1541245808278.jpeg"/><p>2018 年苏宁易购提出了智慧零售大开发战略，业务快速发展对苏宁的 IT 技术提出了更高的要求，其中一个重要的环节就是加快软件版本的上线步伐，伴随着软件的频繁快速上线迭代必然存在巨大的测试压力。</p> <i>By 卢烨</i>
---------------
<h1 id="#title_13" >14、微软正式发布Azure IoT Central</h1>
Eldert Grootenboer
[http://www.infoq.com/cn/news/2018/11/microsoft-azure-iot-central?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/11/microsoft-azure-iot-central?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>微软正式发布Azure IoT Central，这是一个面向物联网的软件即服务解决方案。借助该服务，微软旨在提供一种设计、开发、配置和管理IoT设备的低代码方式，同时提供开箱即用的安全性、可伸缩性以及与流程&应用程序集成。</p> <i>By Eldert Grootenboer</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_14" >15、文章： 苏宁大数据离线任务开发调度平台实践</h1>
桑强
[http://www.infoq.com/cn/articles/suning-big-data?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/suning-big-data?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/suning-big-data/zh/smallimage/logo2-1541244309631.jpeg"/><p>本文主要讲述的是作业调度系统。不过，IDE除了完成了大数据的任务各种复杂调度外，还包含了任务开发、依赖组织、状态维护、任务监控、任务治理、服务监控、动态扩缩容等诸多内容。</p> <i>By 桑强</i>
---------------