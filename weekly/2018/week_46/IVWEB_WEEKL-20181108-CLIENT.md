## 文章索引
1、 <a href="#1improve-animated-gif-performance-with-html5-video" >Improve Animated GIF Performance With HTML5 Video</a><br/>
2、 <a href="#2the-value-of-storyboarding-for-product-design" >The Value Of Storyboarding For Product Design</a><br/>
3、 <a href="#3the-101-course-on-crafting-404-pages" >The 101 Course On Crafting 404 Pages</a><br/>
4、 <a href="#4how-to-build-a-virtual-reality-model-with-a-real-time-cross-device-preview" >How To Build A Virtual Reality Model With A Real-Time Cross-Device Preview</a><br/>
5、 <a href="#5awk-入门教程" >awk 入门教程</a><br/><h1 id="#title_0" >1、Improve Animated GIF Performance With HTML5 Video</h1>
Ayo Isaiah
[https://www.smashingmagazine.com/2018/11/gif-to-video/](https://www.smashingmagazine.com/2018/11/gif-to-video/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/11/gif-to-video/" />
              <title>Improve Animated GIF Performance With HTML5 Video</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>Improve Animated GIF Performance With HTML5 Video</h1>
                  
                    
                    <address>Ayo Isaiah</address>
                  
                  <time datetime="2018-11-05T14:30:14&#43;01:00" class="op-published">2018-11-05T14:30:14+01:00</time>
                  <time datetime="2018-11-06T23:07:09&#43;00:00" class="op-modified">2018-11-06T23:07:09+00:00</time>
                </header>
                

<p><em>It has been brought to our attention that this piece is a reworded version of an article published on the Google Web Fundamentals site, written by our friend Jeremy Wagner. The original piece can be found , and we would recommend it to you.</em></p>

<p><em>I’d like to personally apologize to Jeremy for not identifying this as a copy of his work. Recognizing and crediting the work of people in our community is something I &mdash; and the whole team &mdash; care very much about. I’m sorry that we failed to do the right thing this time.</em></p>

<p><em>&mdash; Rachel Andrew, on behalf of the Editorial Team</em></p>

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
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0bd3c4ca-33bf-4df1-b706-45c1217e4575/caniuse-webm.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0bd3c4ca-33bf-4df1-b706-45c1217e4575/caniuse-webm.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0bd3c4ca-33bf-4df1-b706-45c1217e4575/caniuse-webm.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0bd3c4ca-33bf-4df1-b706-45c1217e4575/caniuse-webm.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0bd3c4ca-33bf-4df1-b706-45c1217e4575/caniuse-webm.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0bd3c4ca-33bf-4df1-b706-45c1217e4575/caniuse-webm.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0bd3c4ca-33bf-4df1-b706-45c1217e4575/caniuse-webm.png"
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

<pre class="break-out"><code class="language-html">&lt;video autoplay loop muted playsinline src="video.mp4"&gt;&lt;/video&gt;</code></pre>

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

<h3 id="potential-drawbacks">Potential Drawbacks</h3>

<p>There are a couple of drawbacks you need to consider before adopting HTML5 video as a GIF replacement. It’s clearly not as convenient as simply uploading a GIF to a page and watch it just work everywhere. You need to encode it first, and it may be difficult to implement an automated solution that works well in all scenarios.</p>

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
<h1 id="#title_1" >2、The Value Of Storyboarding For Product Design</h1>
Joshua Bumcrot
[https://www.smashingmagazine.com/2018/11/value-storyboarding-product-design/](https://www.smashingmagazine.com/2018/11/value-storyboarding-product-design/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/11/value-storyboarding-product-design/" />
              <title>The Value Of Storyboarding For Product Design</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>The Value Of Storyboarding For Product Design</h1>
                  
                    
                    <address>Joshua Bumcrot</address>
                  
                  <time datetime="2018-11-06T14:15:20&#43;01:00" class="op-published">2018-11-06T14:15:20+01:00</time>
                  <time datetime="2018-11-06T23:07:09&#43;00:00" class="op-modified">2018-11-06T23:07:09+00:00</time>
                </header>
                <p>When you think of the word “storyboarding,” you probably think about film, media, and video creation. Historically, this is what storyboards have been used for, but who says we can’t use them for product development as well?</p>

<p>Storyboards are an effective communication and product development tool for digital marketers, content creators, user experience specialists, and product managers. In this article, I’ll teach you why storyboarding is valuable to the product development process, as well as why it can reduce interdepartmental miscommunications as well as overhead costs.</p>

<p>Below is a comic of a clear and common situation experienced by most companies. Words can only go so far as to effective explanations and miscommunications are are a common occurrence in the product development world. As you read the article, <strong>keep this image in mind</strong> and notice examples where storyboarding or visual communication may be able to prevent misunderstandings.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6f0514ff-6774-47d0-9727-5119fe3ec15d/1-value-of-storyboarding-for-product-design.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6f0514ff-6774-47d0-9727-5119fe3ec15d/1-value-of-storyboarding-for-product-design.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6f0514ff-6774-47d0-9727-5119fe3ec15d/1-value-of-storyboarding-for-product-design.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6f0514ff-6774-47d0-9727-5119fe3ec15d/1-value-of-storyboarding-for-product-design.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6f0514ff-6774-47d0-9727-5119fe3ec15d/1-value-of-storyboarding-for-product-design.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6f0514ff-6774-47d0-9727-5119fe3ec15d/1-value-of-storyboarding-for-product-design.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6f0514ff-6774-47d0-9727-5119fe3ec15d/1-value-of-storyboarding-for-product-design.png"
			sizes="100vw"
			alt="A classic corporate communication issue"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The ‘Tree Swing’ communication problem ()
		</figcaption>
	
</figure>




<aside class="product-panel product-panel__tilted product-panel--book" data-audience="non-subscriber">
    <div class="container product-panel--book__container">
      <div class="panel__description panel__description--book">
    <p>Web forms are such an important part of the web, but <strong>we design them poorly all the time</strong>. The brand-new “Form Design Patterns” book is our new practical guide for people who <strong>design, prototype</strong> and <strong>build</strong> all sorts of forms for digital services, products and websites. The eBook is <em>free</em> for .</p>
    <a href="https://www.smashingmagazine.com/2018/10/form-design-patterns-release/#toc" class="btn btn--green btn--large">
      Check the table of contents&nbsp;↬
    </a>
      </div>
      <div class="panel__image panel__image--book">
        <a href="https://www.smashingmagazine.com/2018/10/form-design-patterns-release/#toc" class="books__book__image">
        <div class="books__book__img">
          <img src="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/de0c560d-c0e0-4d52-a6b9-02c0028ba10f/form-design-pattners-shop-wo-shadow.png" alt="Form Design Patterns — a practical guide for anyone who needs to design and code web forms" width="310" height="400">
        </div>
      </a>
      </div>
    </div>
  </aside>




<p>I’m going to set a scene that almost all tech companies experience on a regular basis:</p>

<blockquote>Marketer Mary has an idea for a new product. Mary thinks this product will be a huge winner and goes to tech to have them build it.<br /><br />Developer Diane hears Mary’s idea and tells her she will start working on it. As Diane continues to build out functionality, she realizes that the product will actually be much more efficient if she combines some of the parts and cuts out others. Diane finishes building the product and sends it over to Creative Chris.<br /><br />Chris meets with Mary to discuss the product’s UI, where Mary explains her ideas. Chris gets to work. He starts to incorporate Mary’s ideas but quickly realizes that he has a much better and more interesting UI concept in mind, and eventually completes the product that way.<br /><br />Once the project is complete, Mary is upset. The product has neither the functionality she asked for, nor does the UI allow the user to navigate the product properly.<br /><br />All three departments go back to the drawing board to redo the product, and a significant amount of time and money has been wasted.</blockquote>

<p>This common situation is not <em>one</em> person’s fault. Mary should have explained to Diane and Chris her clear end goal of the product and let them create it with the goal in mind. Diane should have understood that Mary was asking for specific functionalities for a reason and even though her product may have been more efficient, <strong>it’s useless if it doesn’t accomplish the desired end goal</strong>. Chris should have understood that even though Mary’s UI concept may not have been the most aesthetically pleasing, she had that UI for a reason. They should have worked together to create a concept that works for everyone.</p>

<p>There are a few ideas out there on how to attack common product development miscommunication problems, however, many have found the most successful solution is to create storyboards throughout the product development process.</p>

<p>A storyboard is a collection of cells, either in a linear progression or mapped out from a central idea that tells a story. Each cell can contain an image, a title, and a description that provides specific information to the reader about certain aspects of the story. <strong>Storyboards are meant to be simple representations of a larger concept</strong>, and force both its creators and readers to break down large complex topics into simple step by step subsections.</p>

<div class="sponsors__wide-place"></div>




<h3>The Journey Of Entrepreneur Erin</h3>

<p><em>The fictional, but based on real events journey of an entrepreneur using storyboards to help her and her team design, build, and iterate a her product.</em></p>

<p>Erin left her job at the big company she worked for and decided to pursue her dreams and start her own company. She already had an idea &mdash; SoLoMoFoo. SoLoMoFoo is an application to alert employees when free food is available in common areas &mdash; like conference rooms, shared office kitchens, or private offices. At her old job, she had noticed far too often that free food goes to waste due to lack of awareness and employees become disgruntled after hearing about free food that they had just missed. She decided that this problem needed a solution and that she was going to build it! First, she needed to figure out who exactly her target users would be.</p>

<p>A useful way to discover potential target users is to create personas. Erin decided she was going to map out a few of her target users and buyers and record some of their unique characteristics.</p>

<h3>Creating Personas</h3>

<blockquote>Creating personas can help you step out of yourself. It can help you to recognize that different people have different needs and expectations, and it can also help you to identify with the user you’re designing for.<br /><br />&mdash; Rikke Dam, Co-Founder of Interaction Design Foundation</blockquote>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4d1ca13c-dc43-4cd4-951c-aa57b8fa86bc/2-value-of-storyboarding-for-product-design.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4d1ca13c-dc43-4cd4-951c-aa57b8fa86bc/2-value-of-storyboarding-for-product-design.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4d1ca13c-dc43-4cd4-951c-aa57b8fa86bc/2-value-of-storyboarding-for-product-design.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4d1ca13c-dc43-4cd4-951c-aa57b8fa86bc/2-value-of-storyboarding-for-product-design.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4d1ca13c-dc43-4cd4-951c-aa57b8fa86bc/2-value-of-storyboarding-for-product-design.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4d1ca13c-dc43-4cd4-951c-aa57b8fa86bc/2-value-of-storyboarding-for-product-design.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4d1ca13c-dc43-4cd4-951c-aa57b8fa86bc/2-value-of-storyboarding-for-product-design.png"
			sizes="100vw"
			alt="Buyer and User Persona Examples"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Personas for SoLoMoFoo ()
		</figcaption>
	
</figure>


<p>Erin knows that SoLoMoFoo will solve a problem that exists (the lack of awareness about free available food) &mdash; but who does this problem exist for? Who will be using her product? Before Erin starts to create storyboards she first has to build her personas. Generally, companies will have to focus on two different types of personas &mdash; user personas and buyer personas.</p>

<h4>1. User Personas</h4>

<p>These are fictional depictions of quintessential users fitting a certain criteria. Most products will try to limit the number of two or a maximum of three <em>key user personas</em>, and then focus the majority of marketing efforts on attracting these users. In SoLoMoFoo’s case, there are two <em>key user personas</em> that Erin has identified:</p>

<ul>
<li><strong>Baking Ben</strong><br />Ben is often bringing free food into the workplace to share with coworkers. He feels a little weird about emailing the entire office every time he brings in cupcakes so he would love an app that alerts his coworkers for him.</li>
<li><strong>Hangry Hank</strong><br />Hank is constantly missing free food and is upset because of it. He feels less productive when he’s hungry and would be very interested in an app that alerts him anytime food is available.</li>
</ul>

<h4>2. Buyer Personas</h4>

<p>Often times the intended user of your product is not the same as the intended buyer. In SoLoMoFoo’s business model, an entire company will purchase the SoLoMoFoo app and have their employees download it. This way everyone in the office will both be able to send alerts when they have free food, and receive alerts when they’re looking for food. Erin has decided that the most likely purchaser of SoLoMoFoo will be the HR department.

<ul>
<li><strong>HR Hailey</strong><br />Hailey is the HR manager and has purchasing power. She is constantly looking for ways to improve employees’ morale and engagement. She is incentivized by her superiors to inspire energy and teamwork amongst the employees and has a budget to spend on applications or tools that will help her do this.</li>
</ul>

<p>Creating these personas will help you step inside the shoes of both your users, and your buyers (if they are different). It helps you take a step back from your product and see it through the eyes of the people you are designing for.</p>

<div class="sponsors__wide-place"></div>




<p>To start creating the personas you need, there are several online resources you can use. For example, you can use a persona worksheet template like one of these:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/68c752ae-a03b-4f48-a76a-a1d158453482/3-value-of-storyboarding-for-product-design.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/68c752ae-a03b-4f48-a76a-a1d158453482/3-value-of-storyboarding-for-product-design.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/68c752ae-a03b-4f48-a76a-a1d158453482/3-value-of-storyboarding-for-product-design.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/68c752ae-a03b-4f48-a76a-a1d158453482/3-value-of-storyboarding-for-product-design.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/68c752ae-a03b-4f48-a76a-a1d158453482/3-value-of-storyboarding-for-product-design.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/68c752ae-a03b-4f48-a76a-a1d158453482/3-value-of-storyboarding-for-product-design.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/68c752ae-a03b-4f48-a76a-a1d158453482/3-value-of-storyboarding-for-product-design.png"
			sizes="100vw"
			alt="HubSpot  Persona Template"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			HubSpot persona template ()
		</figcaption>
	
</figure>












<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2f474fb2-ac71-4a5a-b3b4-9f0976971b50/4-value-of-storyboarding-for-product-design.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2f474fb2-ac71-4a5a-b3b4-9f0976971b50/4-value-of-storyboarding-for-product-design.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2f474fb2-ac71-4a5a-b3b4-9f0976971b50/4-value-of-storyboarding-for-product-design.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2f474fb2-ac71-4a5a-b3b4-9f0976971b50/4-value-of-storyboarding-for-product-design.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2f474fb2-ac71-4a5a-b3b4-9f0976971b50/4-value-of-storyboarding-for-product-design.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2f474fb2-ac71-4a5a-b3b4-9f0976971b50/4-value-of-storyboarding-for-product-design.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2f474fb2-ac71-4a5a-b3b4-9f0976971b50/4-value-of-storyboarding-for-product-design.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Xtensio persona template (Credit to )
		</figcaption>
	
</figure>


<p>Or use a persona creation tool like .</p>

<p>After personas have been created, the next step is to discover how these personas would come in contact with the problem you're solving for, your product as a solution, and how the product would ultimately benefit their lives. A great way to step into your personas’ shoes is to create journey maps.</p>

<h3>Journey Mapping</h3>

<blockquote>Customer journey mapping helps you to visualize your customer’s experience from the customer’s point of view, across all the different touchpoints they have with your brand as they seek to achieve a specific goal or goals.<br /><br />&mdash; Tandem Seven Experts</blockquote>

<p>Now that Erin has identified SoLoMoFoo’s key user and buyer personas it’s time for her to discover how these personas may come across her product, how they would use it, and what potential obstacles they may face throughout the process. A great way to do this is to <strong>create journey maps in the form of storyboards</strong>. Creating these journey mapping storyboards forces the product designer to walk in the user or buyers shoes and experience their product in a step-by-step manner.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bc0e3c4d-4b2f-4732-aefb-79ec1bf329cf/5-value-of-storyboarding-for-product-design.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bc0e3c4d-4b2f-4732-aefb-79ec1bf329cf/5-value-of-storyboarding-for-product-design.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bc0e3c4d-4b2f-4732-aefb-79ec1bf329cf/5-value-of-storyboarding-for-product-design.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bc0e3c4d-4b2f-4732-aefb-79ec1bf329cf/5-value-of-storyboarding-for-product-design.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bc0e3c4d-4b2f-4732-aefb-79ec1bf329cf/5-value-of-storyboarding-for-product-design.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bc0e3c4d-4b2f-4732-aefb-79ec1bf329cf/5-value-of-storyboarding-for-product-design.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bc0e3c4d-4b2f-4732-aefb-79ec1bf329cf/5-value-of-storyboarding-for-product-design.png"
			sizes="100vw"
			alt="User Journey Map"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Customer journey map for SoLoMoFoo ()
		</figcaption>
	
</figure>


<p>A journey map storyboard can generally be broken down in six key components:</p>

<ol>
<li><strong>Problem Experienced</strong><br />You have decided to create your product for a reason. You believe that your target users are experiencing a problem that they want solved. What is the problem that your product solves for?</li>
<li><strong>Solution Search</strong><br />After your persona has experienced the problem, you believe they will go searching for a solution. What methods will they use to search? These can be potential marketing channels to consider for your go-to-market strategy.</li>
<li><strong>Product Discovery</strong><br />During their search, your personas will come across your product and decide to start using it. How will they know this is the product for them? How will they get started? What barriers to entry might they face?</li>
<li><strong>Product Experienced</strong><br />The persona will now use the product and experience the intended objective. How do they use it? Can they use it immediately or are there other steps they need to take?</li>
<li><strong>Problem Alleviated</strong><br />After the intended product objective is attained the users problem is alleviated. Is this the same problem you were attempting to solve for at the beginning of your storyboard? What other potential problems might stem from your solution?</li>
<li><strong>Beneficial Outcome</strong><br />Now that persona’s problem is alleviate, why is their life better? What benefit did solving their problem bring to them and how will this improve their situation?</li>
</ol>

<p>Need an example? Take a look at the illustration below:</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a22310c9-ef21-4aaf-8090-054492a7a61c/6-value-of-storyboarding-for-product-design.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a22310c9-ef21-4aaf-8090-054492a7a61c/6-value-of-storyboarding-for-product-design.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a22310c9-ef21-4aaf-8090-054492a7a61c/6-value-of-storyboarding-for-product-design.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a22310c9-ef21-4aaf-8090-054492a7a61c/6-value-of-storyboarding-for-product-design.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a22310c9-ef21-4aaf-8090-054492a7a61c/6-value-of-storyboarding-for-product-design.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a22310c9-ef21-4aaf-8090-054492a7a61c/6-value-of-storyboarding-for-product-design.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a22310c9-ef21-4aaf-8090-054492a7a61c/6-value-of-storyboarding-for-product-design.png"
			sizes="100vw"
			alt="Blank Stick Figure Template for Journey Mapping"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Customer journey map template ()
		</figcaption>
	
</figure>


<p>In the case of Entrepreneur Erin, she has to consider how the lack of access to free food would affect HR Hailey, how she would research possible solutions, how she would come across SoLoMoFoo, how the SoLoMoFoo platform would be implemented at her place of work, and the potential benefits and timeline for those benefits that the SoLoMoFoo program would bring.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f615395d-bcdb-4a87-a572-bcf80dd6be2a/7-value-of-storyboarding-for-product-design.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f615395d-bcdb-4a87-a572-bcf80dd6be2a/7-value-of-storyboarding-for-product-design.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f615395d-bcdb-4a87-a572-bcf80dd6be2a/7-value-of-storyboarding-for-product-design.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f615395d-bcdb-4a87-a572-bcf80dd6be2a/7-value-of-storyboarding-for-product-design.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f615395d-bcdb-4a87-a572-bcf80dd6be2a/7-value-of-storyboarding-for-product-design.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f615395d-bcdb-4a87-a572-bcf80dd6be2a/7-value-of-storyboarding-for-product-design.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f615395d-bcdb-4a87-a572-bcf80dd6be2a/7-value-of-storyboarding-for-product-design.png"
			sizes="100vw"
			alt="Buyer Journey Mapping"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Buyer journey map for SoLoMoFoo ()
		</figcaption>
	
</figure>


<p>Creating journey maps in the form of storyboards is a useful way to humanize your buyers. It’s essential to remember that your users are not just numbers, but real people. Having a human character and their personal journey map story associated with each persona serves as a constant reminder that <strong>your users are people</strong>, and their needs are constantly changing.</p>

<p>These journey maps are not only a great external product development tool, but also a great way to minimize internal miscommunications.</p>

<p>By developing user personas and a customer journey map storyboard, everyone is able to visualize the steps a persona would take when engaging with your product. Creating journey maps and presenting them to coworkers allows team members to view your vision in a realistic and tangible way. Once every department understands your journey maps, you can all reach consensus on what the final product will be, and the development process can continue with everyone on the same page.</p>

<h3>Storyboarding For UX Design</h3>

<blockquote>Storyboarding in UX is a tool which can help you visually predict and explore a user’s experience with a product.<br /><br />&mdash; Nick Babich, Editor-in-chief of UX Planet</blockquote>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0472f2fe-eae0-4683-9491-20d3331d4560/8-value-of-storyboarding-for-product-design.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0472f2fe-eae0-4683-9491-20d3331d4560/8-value-of-storyboarding-for-product-design.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0472f2fe-eae0-4683-9491-20d3331d4560/8-value-of-storyboarding-for-product-design.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0472f2fe-eae0-4683-9491-20d3331d4560/8-value-of-storyboarding-for-product-design.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0472f2fe-eae0-4683-9491-20d3331d4560/8-value-of-storyboarding-for-product-design.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0472f2fe-eae0-4683-9491-20d3331d4560/8-value-of-storyboarding-for-product-design.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0472f2fe-eae0-4683-9491-20d3331d4560/8-value-of-storyboarding-for-product-design.png"
			sizes="100vw"
			alt="Basic UX Storyboard Mockup"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			User-experience storyboard ()
		</figcaption>
	
</figure>


<p>Entrepreneur Erin has successfully identified who she believes her target users and buyers are and how they will come in contact and use her product. Now it’s time for her to design the SoLoMoFoo user experience.</p>

<p>A useful way to step back and view your product from a user’s point of view is to create UX concepts through storyboarding. <strong>Creating storyboards, cell-by-cell, forces you to walk through every step of your UX process as a user</strong>. You can easily create multiple storyboards and try out different UX approaches to find the most efficient concept.</p>

<p>Erin wants to design SoLoMoFoo as a simple app so she reviews the personas and journey maps with her development and marketing team so they are clear on the product vision and together they start designing a user experience.</p>

<p>Creating these visual, tangible storyboards points out potential flaws in your UX &mdash; maybe you are forcing your users to take a long leap in one step and is not intuitive. Or, perhaps you have a few steps in your UX that could be combined into one thus eliminating superfluous actions.</p>

<p>According to UX Specialist, Luca Morovian:</p>

<blockquote>“The UX storyboard can help visually predict and explore the user experience with a product. It visualizes how people would interact with a service or app. A UX storyboard can also help understand users current motivations and experiences connected to a certain problem.”</blockquote>

<p>The power and value of storyboarding for UX comes in the creation process, letting you experience your product as a user, which allows you to best optimize for effective design and an improved conversion rate.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2d9151c8-31a1-4409-aacd-9fbcc1684d63/9-value-of-storyboarding-for-product-design.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2d9151c8-31a1-4409-aacd-9fbcc1684d63/9-value-of-storyboarding-for-product-design.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2d9151c8-31a1-4409-aacd-9fbcc1684d63/9-value-of-storyboarding-for-product-design.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2d9151c8-31a1-4409-aacd-9fbcc1684d63/9-value-of-storyboarding-for-product-design.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2d9151c8-31a1-4409-aacd-9fbcc1684d63/9-value-of-storyboarding-for-product-design.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2d9151c8-31a1-4409-aacd-9fbcc1684d63/9-value-of-storyboarding-for-product-design.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2d9151c8-31a1-4409-aacd-9fbcc1684d63/9-value-of-storyboarding-for-product-design.png"
			sizes="100vw"
			alt="UX Storyboard with aspect arrows"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			User-experience storyboard with detailed descriptions ()
		</figcaption>
	
</figure>


<p>Finally, Erin has identified her target users and buyers, journey mapped their process, and built a streamlined UX &mdash; but the product development process is never over.</p>

<h3>Storyboarding For Product Iterations And Improvements</h3>

<blockquote>Your people know your products better than anyone else so as long as you ask the right questions and use appealing storyboards, you can solicit reactions from them and start a discussion on whatever it is you need to find out.<br /><br />&mdash; Andre Bourque, Entrepreneur</blockquote>

<p>Erin has now identified who she thinks will use and buy her SoLoMoFoo, how they will come across the product and engage with it, and how the platform user flow will be designed.</p>

<p>As product developers are aware, <strong>a product is never fully complete</strong>. As technology changes, users adapt and so must your product. It’s important to constantly be referring back to your customer journey maps and user personas to make sure they are still accurate to your product. As you learn more about your users and user-case scenarios, your product should adapt accordingly.</p>

<p>When looking into product iterations, most product development teams have a tough time isolating the scope and deciding on which aspect of the current product they want to change. Storyboards can help product designers break their product into individual segments, which then allows them to specifically work on one aspect of a product without involving others.</p>

<p>Here are a few questions you may want to use as a guide:</p>

<ul>
<li>Do you have a homepage conversion rate issue and want to modernize UI?</li>
<li>Are users not responding to your call-to-actions? Maybe your UX is too complicated? Or maybe people just aren’t purchasing your product, so are you really solving your perceived problem?</li>
</ul>

<p>Having a storyboard of your product allows you to clearly see which parts of your product are responsible for which users’ actions. As a result, you can focus your iteration process on one aspect of your product instead of the product as a whole allowing for faster improvements and a cleaner process.</p>

<h3>How To Begin</h3>

<p>Now that you have the knowledge on how to start using storyboards in your product development process, it’s time to get started.</p>

<p>Here are some quick steps to help you make the first step:</p>

<ol>
<li>Identify the problem your product is solving for;</li>
<li>Identify 1-3 user personas and 1-3 buyer personas (if different);</li>
<li>Create journey maps for your personas;</li>
<li>Design UX flows around your target audiences’ needs;</li>
<li>Iterate, repeat, and improve!</li>
</ol>

<p>In conclusion, you now have tools to start incorporating storyboarding into your product development process. From the beginning in identifying your target users all the way to the end in building a UX and iterating your product for improvements.</p>

<p>Using storyboarding through the product design process will help prevent simple miscommunications and allow both you and your team to have a clear concept of what your product will accomplish and look like. Start storyboarding out your new product idea today!</p>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(yk, ra, il)</span>
</div>


              </article>
            </body>
          </html>
---------------
<h1 id="#title_2" >3、The 101 Course On Crafting 404 Pages</h1>
Shelby Rogers
[https://www.smashingmagazine.com/2018/11/the-101-course-on-crafting-404-pages/](https://www.smashingmagazine.com/2018/11/the-101-course-on-crafting-404-pages/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/11/the-101-course-on-crafting-404-pages/" />
              <title>The 101 Course On Crafting 404 Pages</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>The 101 Course On Crafting 404 Pages</h1>
                  
                    
                    <address>Shelby Rogers</address>
                  
                  <time datetime="2018-11-01T09:48:57&#43;00:00" class="op-published">2018-11-01T09:48:57+00:00</time>
                  <time datetime="2018-11-06T23:07:09&#43;00:00" class="op-modified">2018-11-06T23:07:09+00:00</time>
                </header>
                

<p>A lot of people toss around the phrase, “It’s not about the destination. It’s about the journey.” And those people are telling the truth &mdash; until they hit a roadblock.</p>

<p>Missed turns or poorly-given directions can cost someone hours on a trip. When you’re on a mission, those hours spent trying to find what you need could ruin the entire experience.</p>

<p>It doesn’t always have to end in disaster. This more optimal scenario could occur: you take a wrong turn, but after stopping at a nearby gas station, you leave with more than accurate directions to your final destination. You’ve also managed to score a free ice cream cone from the sweet old lady working behind the gas station’s register because she saw you were lost… and wanted to cheer you up.</p>

<p>Often, website visitors can wind up getting turned around. It’s not always their fault. They could’ve typed in the wrong URL (common) or clicked on a broken link (our mistake). Whatever the reasoning, you now have confused people who only wanted to engage with your website in some way and now can’t. You hold the reins on their navigation. You can guide them back to where you wanted them to go all along or you can leave them frustrated and in the dark. Do they need to make a U-turn? Did they get off at the wrong exit? Only you can tell them, and the best way to do so is through a 404 error page.</p>

<p>Your website’s 404 error page can deliver either of these scenarios with regard to getting your visitors back on their buyer’s journey. A lackluster 404 page irritates your visitors and chases them away into the hands of a competing website that better guides them to what they’re looking for. That lackluster 404 page has bland messaging with minimal visual elements. It might include a variation of the same serif text: “This page does not exist.” That’s like your web users asking you for directions and telling them nothing more than “well, what you’re looking for isn’t here. Good luck.” Nothing more.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1e0943a7-226a-4801-9518-4133a342a979/bland-404-page.JPG">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1e0943a7-226a-4801-9518-4133a342a979/bland-404-page.JPG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1e0943a7-226a-4801-9518-4133a342a979/bland-404-page.JPG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1e0943a7-226a-4801-9518-4133a342a979/bland-404-page.JPG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1e0943a7-226a-4801-9518-4133a342a979/bland-404-page.JPG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1e0943a7-226a-4801-9518-4133a342a979/bland-404-page.JPG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1e0943a7-226a-4801-9518-4133a342a979/bland-404-page.JPG"
			sizes="100vw"
			alt="black, boring text about a 404 page on a white background"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Even brands with seemingly clever branding can neglect a 404 page! The owner of this sad excuse for an error page will remain anonymous (but it rhymes with Bards Tragainst Bubanity). ()
		</figcaption>
	
</figure>


<p>Unfortunately, even some of the world’s best brands use these 404 pages. No navigation. No interesting text. Nothing that reflects their brand messaging. Visitors are left even more disappointed in their encounter than before.</p>

<p>However, there are some 404 pages that go above and beyond. Rather than the stark white of a standard 404 error page, these pages take an opportunity to speak to users in a more personal tone. Excellent 404 pages are exactly like getting an unexpected treat from a friendly face. Well-crafted 404 Pages can redirect your pages’ visitors away from being lost and confused and to a much happier mood and onto a more helpful page on your website.</p>



<aside class="product-panel product-panel__tilted product-panel--book" data-audience="non-subscriber">
    <div class="container product-panel--book__container">
      <div class="panel__description panel__description--book">
    <p>Web forms are such an important part of the web, but we design them poorly all the time. The brand new .</p>
    <a href="https://smashed.by/fdppanel/#toc" class="btn btn--green btn--large">
      Check the table of contents&nbsp;↬
    </a>
      </div>
      <div class="panel__image panel__image--book">
        <a href="https://smashed.by/fdppanel/#toc" class="books__book__image">
        <div class="books__book__img">
          <img src="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/de0c560d-c0e0-4d52-a6b9-02c0028ba10f/form-design-pattners-shop-wo-shadow.png" alt="Form Design Patterns — a practical guide for anyone who needs to design and code web forms" width="310" height="400">
        </div>
      </a>
      </div>
    </div>
  </aside>




<p>Take Amazon, for instance. On Amazon Day 2018, Amazon learned firsthand the importance of a decent 404 page. Sure, buyers were still frustrated upon reaching a 404 page &mdash; even if it included a puppy. However, could you imagine how much more irritated buyers would’ve been had the 404 page looked clinical, cold, and not helpful?
</p>

<p>Regardless of what tone you want to take or what visuals you want to use or what copy will best engage your readers, a great 404 page does one thing above all else: Makes website visitors okay with not finding what they need &mdash; if only for a moment &mdash; and directs them to where they need to go.</p>

<p>While 404 pages vary greatly, the best ones all seem to do two things well:</li>

<ol>

<li>Support the company’s overall brand and messaging;</li>

<li>Successfully redirect website visitors elsewhere on the page through clear navigation and support.</li>

</ol>

<p>Thematically, there are a few ways to accomplish the ‘perfect’ 404 page:</p>

<div class="sponsors__wide-place"></div>


<h3 id="1-nail-down-the-overall-tone">1. Nail Down The Overall Tone</h3>

<p>If content isn’t your brand’s strong suit, this could be a struggle. However, if you have a sense of your brand’s voice and messaging, you can quickly identify where you can offer something unexpected. Visitors are already going to be disappointed when they hit your 404 page; they’re not getting what they wanted. Your 404 page is an opportunity to show that your brand has humans behind its marketing rather than robotic, cold, automated messages seen elsewhere. In short, move beyond the “this page is unavailable” and its variants.</p>

<p>Regardless of the tone, good 404 pages work like magicians. The best illusionists often acknowledge they’re magicians; they don’t pretend to be something they’re not. 404 pages own up to being an error page; the copy and visuals often reflect that. And then, like any good magician, 404 pages pull the attention away from the problem and put that attention elsewhere. Typically, that’s done with copy that matches the visual elements.</p>

<p>Here are some themes/moods that successful 404 pages have leveraged in the past used to succeed.</p>

<h4 id="crack-a-joke">Crack A Joke</h4>

<p>A joke (even a corny one) can do wonders for alleviating awkwardness or inconvenience. However, unless your brand is built on crude humor (i.e. Cards Against Humanity which ironically doesn’t have a good 404 page), it’s best to make the jokes either tongue in cheek or punny rather than too crass. This example from Modcloth makes a quick pun but keeps the mood light.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a4142a5f-2f50-4949-a27a-e30bbcc5e457/modcloth-404.JPG">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a4142a5f-2f50-4949-a27a-e30bbcc5e457/modcloth-404.JPG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a4142a5f-2f50-4949-a27a-e30bbcc5e457/modcloth-404.JPG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a4142a5f-2f50-4949-a27a-e30bbcc5e457/modcloth-404.JPG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a4142a5f-2f50-4949-a27a-e30bbcc5e457/modcloth-404.JPG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a4142a5f-2f50-4949-a27a-e30bbcc5e457/modcloth-404.JPG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a4142a5f-2f50-4949-a27a-e30bbcc5e457/modcloth-404.JPG"
			sizes="100vw"
			alt="Light pink background with dark pink text saying Oops! You were lookin&#39; for love on all the wrong pages"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Happy and snappy, this 404 page aligns with the rest of the brand’s fun copy. ()
		</figcaption>
	
</figure>


<h4 id="get-clever">Get Clever</h4>

<p>It might not be outright funny, but it’s something that gets a visitor’s attention shortly after arriving on your page. It can be a little sassy, snarky, even unexpected. This 404 page from Blizzard Entertainment does a great job at flipping the script both with its visual tone and its copy.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b1202578-a3ff-4cb7-a95e-18fda3491b07/blizzard-entertainment-404.JPG">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b1202578-a3ff-4cb7-a95e-18fda3491b07/blizzard-entertainment-404.JPG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b1202578-a3ff-4cb7-a95e-18fda3491b07/blizzard-entertainment-404.JPG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b1202578-a3ff-4cb7-a95e-18fda3491b07/blizzard-entertainment-404.JPG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b1202578-a3ff-4cb7-a95e-18fda3491b07/blizzard-entertainment-404.JPG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b1202578-a3ff-4cb7-a95e-18fda3491b07/blizzard-entertainment-404.JPG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b1202578-a3ff-4cb7-a95e-18fda3491b07/blizzard-entertainment-404.JPG"
			sizes="100vw"
			alt="Broken and cracked screen with copy that says Grats. You broke it."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Sarcasm pays off well for the gaming giant’s 404 page. ()
		</figcaption>
	
</figure>


<h4 id="be-friendly">Be Friendly</h4>

<p class="c-pre-sidenote--left">Prime example would be LEGO Shop’s 404 page with a friendly customer service rep (albeit a LEGO rep). The friendliness can come from an inviting design or warm copy. Ultimately, it’s anything that culminates in a sense of “oh hey, we’re really sorry about that. Let us try to fix it.”</p>

<p class="c-sidenote c-sidenote--right">“If your company’s brand excels in customer service and customer care, maybe taking a tone of genuine friendliness would be most appropriate to carry over brand messaging. If that’s the case, treat your 404 page like an extension of your guest services window.” </a></p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2841eaca-71d3-4c6b-9850-11050374732c/lego-404.JPG">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2841eaca-71d3-4c6b-9850-11050374732c/lego-404.JPG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2841eaca-71d3-4c6b-9850-11050374732c/lego-404.JPG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2841eaca-71d3-4c6b-9850-11050374732c/lego-404.JPG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2841eaca-71d3-4c6b-9850-11050374732c/lego-404.JPG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2841eaca-71d3-4c6b-9850-11050374732c/lego-404.JPG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2841eaca-71d3-4c6b-9850-11050374732c/lego-404.JPG"
			sizes="100vw"
			alt="smiling LEGO figure behind a LEGO block with a computer"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<h4 id="integrate-interactivity">Integrate Interactivity</h4>

<p>People love to click on things, especially if they’re engaging with the 404 page on desktop. And if they’re engaging with your website, all the better! One of the best examples online of interactivity on a 404 page is from Kualo. The site hosting provider gamified its 404 page into a recreation of Space Invaders, complete with the ability to earn extra lives as you level up. Even more impressive is that Kualo actually offers discounts on its hosting for certain thresholds of points that users reach.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d3a155d1-3a39-4bdf-b220-47b462b6a6bc/kualo-404.JPG">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d3a155d1-3a39-4bdf-b220-47b462b6a6bc/kualo-404.JPG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d3a155d1-3a39-4bdf-b220-47b462b6a6bc/kualo-404.JPG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d3a155d1-3a39-4bdf-b220-47b462b6a6bc/kualo-404.JPG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d3a155d1-3a39-4bdf-b220-47b462b6a6bc/kualo-404.JPG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d3a155d1-3a39-4bdf-b220-47b462b6a6bc/kualo-404.JPG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d3a155d1-3a39-4bdf-b220-47b462b6a6bc/kualo-404.JPG"
			sizes="100vw"
			alt="dark background with small ships aligned to spell the word KUALO"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The gamification of Kualo’s 404 keeps users coming back for more chances to win. ()
		</figcaption>
	
</figure>


<h4 id="be-thought-provoking">Be Thought-provoking</h4>

<p>Yes, your 404 pages can even be educational! 404 pages can offer up resources and links to other helpful spots on your website. It’s an unexpected distraction that could easily keep guests entertained by more information. National Public Radio (NPR) does this exceptionally well. The media outlet provides a collection of features with one major similarity: the stories are about things which have also disappeared.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bcbc282b-b508-4136-b01a-860f13b6021b/npr-404.JPG">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bcbc282b-b508-4136-b01a-860f13b6021b/npr-404.JPG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bcbc282b-b508-4136-b01a-860f13b6021b/npr-404.JPG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bcbc282b-b508-4136-b01a-860f13b6021b/npr-404.JPG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bcbc282b-b508-4136-b01a-860f13b6021b/npr-404.JPG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bcbc282b-b508-4136-b01a-860f13b6021b/npr-404.JPG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bcbc282b-b508-4136-b01a-860f13b6021b/npr-404.JPG"
			sizes="100vw"
			alt="White background with pictures of Amelia Earhart, Watergate hotel, and Jimmy Hoffa referencing articles about lost things"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<h4 id="topical-pop-culture-based">Topical/pop-culture Based</h4>

<p>Use this one with caution, as there’s a very good chance you’ll have to change your 404 message if you’re going to be topical. Pop culture references move fast; if you’re not careful, you’ve spent too much time developing a 404 page that will be irrelevant in two weeks. (And this is a cardinal sin for any organization with a target market of Millennials or younger.) The Spotify 404 page above recently underwent a shift to keep up with trends. Prior to doing a quick play on Kanye West’s “808 and Heartbreak,” the 404 page featured lyrics from Justin Bieber’s “Sorry.”</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5bd36a5a-5749-41a2-b097-add0e0328a29/spotify-404.JPG">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5bd36a5a-5749-41a2-b097-add0e0328a29/spotify-404.JPG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5bd36a5a-5749-41a2-b097-add0e0328a29/spotify-404.JPG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5bd36a5a-5749-41a2-b097-add0e0328a29/spotify-404.JPG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5bd36a5a-5749-41a2-b097-add0e0328a29/spotify-404.JPG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5bd36a5a-5749-41a2-b097-add0e0328a29/spotify-404.JPG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5bd36a5a-5749-41a2-b097-add0e0328a29/spotify-404.JPG"
			sizes="100vw"
			alt="pink background with record player spinning"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<h3 id="2-craft-visual-elements-to-match-that-tone">2. Craft Visual Elements To Match That Tone</h3>

<p>Once you have an idea of the proper tone for your 404 page, visuals are an important next step in the process. Visuals are often the first element of a 404 page people will note first &mdash; and thus, it’s the first representation of that page’s desired tone.</p>

<div class="sponsors__wide-place"></div>


<p>Static visuals help emphasize the page copy. Adding in light animation can often collaborate with the text to further a message or tone. For example, Imgur’s 404 page brings its illustrations to life by making the eyes of its characters follow a visitor’s cursor.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/34cdb586-6dde-4b0f-9c9c-becabc6d10c7/imgur-404.JPG">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/34cdb586-6dde-4b0f-9c9c-becabc6d10c7/imgur-404.JPG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/34cdb586-6dde-4b0f-9c9c-becabc6d10c7/imgur-404.JPG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/34cdb586-6dde-4b0f-9c9c-becabc6d10c7/imgur-404.JPG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/34cdb586-6dde-4b0f-9c9c-becabc6d10c7/imgur-404.JPG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/34cdb586-6dde-4b0f-9c9c-becabc6d10c7/imgur-404.JPG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/34cdb586-6dde-4b0f-9c9c-becabc6d10c7/imgur-404.JPG"
			sizes="100vw"
			alt="portraits of animals with googly eyes on a red wall"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<p>Interactivity among the visual elements give people an opportunity to do what frustrated internet users love to do &mdash; click on everything in an attempt at making something useful happen.</p>

<h3 id="3-nail-down-the-navigation-options">3. Nail Down The Navigation Options</h3>

<p class="c-pre-sidenote--left">You know what tone you want your business to strike. You’ve got an idea of the visuals you’ll use to present that tone. Your website visitors will think it’s great and fun &mdash; but only for a moment. Your website still has to get them to what they’re looking for. Clear navigation is the next big step in directing your lost website visitors toward their goals. A 404 page that’s cute but lacks good navigation design is like that sweet old man who is kind but he gives you the world’s worst directions.</p>

<p class="c-sidenote c-sidenote--right">“After making a good first impression with your 404 page, the immediate next step should be getting website visitors off it and to where they want to be. There should always be clear indications on where they should go next.”</a></p>

<p>For example, Shutterstock’s 404 page offers three distinct options. Visitors can either go back to the previous page, which is helpful if they clicked on the wrong link. They can return to the homepage for more of a hard restart in their navigation, or maybe they came in from a search engine and found a broken link, but they’re not quite ready to give up on the website and want to look around. The final option is to report a problem. If someone has been scouring your website for minutes on end and they have an idea of what they’re looking for, they can report that they might have found an issue. At the very least, it gets your web visitors involved with your company and your development team gets feedback about the accessibility of your website.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d93e2ae6-e48c-4ac1-9aa5-ebd6efc449d4/shutterstock-404.JPG">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d93e2ae6-e48c-4ac1-9aa5-ebd6efc449d4/shutterstock-404.JPG 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d93e2ae6-e48c-4ac1-9aa5-ebd6efc449d4/shutterstock-404.JPG 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d93e2ae6-e48c-4ac1-9aa5-ebd6efc449d4/shutterstock-404.JPG 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d93e2ae6-e48c-4ac1-9aa5-ebd6efc449d4/shutterstock-404.JPG 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d93e2ae6-e48c-4ac1-9aa5-ebd6efc449d4/shutterstock-404.JPG 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d93e2ae6-e48c-4ac1-9aa5-ebd6efc449d4/shutterstock-404.JPG"
			sizes="100vw"
			alt="Little girl with mouth open wearing glasses"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<p>In addition to clear navigation, these other navigation-based elements could help your visitors out even more:</p>

<ul>

<li>Chatbots / live chat: Bots are often received one of two ways. Users either find them incredibly annoying or relatively helpful. Bots that pop up within a second of landing on a page often lead visitors to click out of a site entirely as the bot seems intrusive. However, your website can use bots by simply adding a “Click to chat” option. This invites lost visitors who want your help to engage with the bot rather than the bot making a potentially annoying first move.</li>

<li>Search Bars: This element can do wonders for websites with a high volume of pages and information. A search bar could also offer up answers to common questions or redirect to an FAQ.</li>

</ul>

<p>And one final navigation note &mdash; make sure those navigation tactics are just as efficient on mobile as they are on desktop. Treat your 404 page as you would any other. In order for it to succeed, it should be easily navigable to a variety of users, especially in a mobile-first world.</p>

<p>While the look of your 404 page is critical, you ideally never want anyone to find it on your website. Knowing the most common 404 errors on your website could give you insights in how to reduce those issues.</p>

<h3 id="how-to-track-404-events-using-google-analytics">How To Track 404 Events Using Google Analytics</h3>

<h4 id="what-you-need-to-start-tracking">What You Need To Start Tracking</h4>

<p>The code provided will report 404 events within Google Analytics, so you must have an up-and-running account there to take advantage of this tutorial. You also need access to your site’s 404 template and (this is important) the 404 page must preserve the URL structure of the typed/clicked page. This means that your 404 events can’t just redirect to your 404 page. You must serve the 404 template dynamically with the exact URL that is throwing the error. Most web server services (such as Apache) allow you to do this with a variety of rewrite rules.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6fb645c3-0c5d-45cb-8ada-7b9477c79e65/1-404-tracking.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6fb645c3-0c5d-45cb-8ada-7b9477c79e65/1-404-tracking.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6fb645c3-0c5d-45cb-8ada-7b9477c79e65/1-404-tracking.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6fb645c3-0c5d-45cb-8ada-7b9477c79e65/1-404-tracking.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6fb645c3-0c5d-45cb-8ada-7b9477c79e65/1-404-tracking.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6fb645c3-0c5d-45cb-8ada-7b9477c79e65/1-404-tracking.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6fb645c3-0c5d-45cb-8ada-7b9477c79e65/1-404-tracking.jpg"
			sizes="100vw"
			alt="Screenshots of tracking a 404 error"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<h4 id="tracking-404-errors-with-google-analytics">Tracking 404 Errors With Google Analytics</h4>

<p>With Google Analytics, tracking explicit 404 errors is straightforward and simple. Just ensure that your main Google Analytics tracking script is in place and then add the following code to your 404 Error Page/Template:</p>

<pre><code class=“language-javascript">&lt;script&gt;  
   // Create Tracker - Send to GA
 ga('create', 'UA-11111111-11');
   ga('send', {
     hitType: 'event',
     eventCategory: '404 Response',
     eventAction: window.location.href,
     eventLabel: document.referrer
});
&lt;/script&gt;</code></pre>

<p>You will need to swap out the ID of your specific Google Analytics account. After that, the script works by sending an “event” to Google Analytics. The category is “404 Response," the action uses JavaScript to pass the URL that throws the error, and the label uses JavaScript to pass along the previous URL the user was on. Through all of this data, you can then see what URLs cause 404 events and where people are accessing those URLs.</p>

<h4 id="tracking-404-errors-with-google-tag-manager">Tracking 404 Errors With Google Tag Manager</h4>

<p>More and more web managers have decided to move to Google Tag Manager. This tool gives them the capability of embedding a whole host of scripts through a single container. It's especially useful if you have a lot of tracking scripts from several providers. To begin tracking 404s through Tag Manager, first begin by creating a “Variable” called “Page Title Variable.” This variable type is a “JavaScript” variable and the Variable Name is “document.title”:</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3969cacd-3fc2-4237-8a9c-942fe6e826c7/2-404tracking.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3969cacd-3fc2-4237-8a9c-942fe6e826c7/2-404tracking.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3969cacd-3fc2-4237-8a9c-942fe6e826c7/2-404tracking.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3969cacd-3fc2-4237-8a9c-942fe6e826c7/2-404tracking.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3969cacd-3fc2-4237-8a9c-942fe6e826c7/2-404tracking.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3969cacd-3fc2-4237-8a9c-942fe6e826c7/2-404tracking.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3969cacd-3fc2-4237-8a9c-942fe6e826c7/2-404tracking.jpg"
			sizes="100vw"
			alt="Page title variable, screenshots of tracking a 404 error"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<p>Essentially, we’re creating a variable that checks for a page’s given title. This is how we will check if we are on a 404 page.</p>

<p>Then create a “Trigger” called “404 Page Title Trigger.” The type is “Page View” and the trigger fires when the “Page Title Variable” contains “404 &mdash; Page Not Found” or whatever it is your 404 page title displays as within the browser.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ec67986b-4690-4f25-8d75-999d31d0454a/3-404tracking.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ec67986b-4690-4f25-8d75-999d31d0454a/3-404tracking.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ec67986b-4690-4f25-8d75-999d31d0454a/3-404tracking.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ec67986b-4690-4f25-8d75-999d31d0454a/3-404tracking.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ec67986b-4690-4f25-8d75-999d31d0454a/3-404tracking.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ec67986b-4690-4f25-8d75-999d31d0454a/3-404tracking.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ec67986b-4690-4f25-8d75-999d31d0454a/3-404tracking.jpg"
			sizes="100vw"
			alt="Page title trigger, Screenshots of tracking a 404 error"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<p>Lastly, you will need to create a “Tag” called “404 Event Tag.” The tag type is “Universal Analytics” and contains the following components:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a847cd81-126a-40f5-ac76-733ce05812fb/4-404tracking.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a847cd81-126a-40f5-ac76-733ce05812fb/4-404tracking.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a847cd81-126a-40f5-ac76-733ce05812fb/4-404tracking.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a847cd81-126a-40f5-ac76-733ce05812fb/4-404tracking.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a847cd81-126a-40f5-ac76-733ce05812fb/4-404tracking.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a847cd81-126a-40f5-ac76-733ce05812fb/4-404tracking.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a847cd81-126a-40f5-ac76-733ce05812fb/4-404tracking.jpg"
			sizes="100vw"
			alt="404 event tagging, screenshots of tracking a 404 error"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<p>The Variable, Trigger, and Tag all work to pass along the relevant data directly to Google Analytics.</p>

<h3 id="404-event-reporting">404 Event Reporting</h3>

<p>No matter your tracking method (be it through Tag Manager or direct event beacons), your reporting should be the same within Google Analytics. Under “Behavior,” you will see an item called “Events.” Here you will see all reported 404 events. The “Event Action” and “Event Label” dimensions will give you the pertinent data of what URLs are throwing 404 errors and their referring source.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/21bd7b66-4117-4cae-b95f-450ad6a3f748/5-404tracking.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/21bd7b66-4117-4cae-b95f-450ad6a3f748/5-404tracking.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/21bd7b66-4117-4cae-b95f-450ad6a3f748/5-404tracking.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/21bd7b66-4117-4cae-b95f-450ad6a3f748/5-404tracking.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/21bd7b66-4117-4cae-b95f-450ad6a3f748/5-404tracking.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/21bd7b66-4117-4cae-b95f-450ad6a3f748/5-404tracking.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/21bd7b66-4117-4cae-b95f-450ad6a3f748/5-404tracking.jpg"
			sizes="100vw"
			alt="Screenshots of tracking a 404 error"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<p>With this in place, you can now regularly monitor your 404 errors and take the necessary steps to minimize their occurrence. In doing so, you optimize your referral sources and provide the best user experience, keeping conversions and engagement on the right path.</p>

<h3 id="what-to-do-with-your-google-analytics-results">What To Do With Your Google Analytics Results</h3>

<p>Now that you know how to monitor those 404 errors, what’s a developer to do? The key takeaway from tracking 404 occurrences is to look for patterns that result in those errors. The data should help you determine user intent, cluing you into what your users want. Ideally, you’ll see trends in what brings people to your 404 page, and you can apply that knowledge to adjust your website accordingly.</p>

<p>If your website visitors are stumbling while searching for a page, take the opportunity to create content that fills in that hole. That way people get results they hadn’t previously seen from your site.</p>

<p>The 404 events could be avoided with a tweak in your website’s design. Make sure the navigation on your pages are clear and direct users to logical ending points. The fix could even be as simple as changing descriptions on a page to paint a clearer picture for users.</p>

<h3 id="putting-it-all-together">Putting It All Together</h3>

<p>Tone, images, and navigation &mdash; these three elements can transform any 404 page from a ghost town into a pleasant serendipitous stop for your website visitors. And while you don’t want them to stay there forever, you can certainly make sure they stay with you is enjoyable before sending them on their way. By regularly monitoring your 404 errors, you can also alleviate some of the ditches, poorly-marked signage, and potholes that frequently derail users. Being proactive and reactive with 404 errors ultimately improves the journey and the destination for your website visitors.</p>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(yk, ra)</span>
</div>


              </article>
            </body>
          </html>
---------------
<h1 id="#title_3" >4、How To Build A Virtual Reality Model With A Real-Time Cross-Device Preview</h1>
Alvin Wan
[https://www.smashingmagazine.com/2018/11/virtual-reality-model-real-time-cross-device-preview/](https://www.smashingmagazine.com/2018/11/virtual-reality-model-real-time-cross-device-preview/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/11/virtual-reality-model-real-time-cross-device-preview/" />
              <title>How To Build A Virtual Reality Model With A Real-Time Cross-Device Preview</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>How To Build A Virtual Reality Model With A Real-Time Cross-Device Preview</h1>
                  
                    
                    <address>Alvin Wan</address>
                  
                  <time datetime="2018-11-06T23:50:16&#43;01:00" class="op-published">2018-11-06T23:50:16+01:00</time>
                  <time datetime="2018-11-07T20:34:00&#43;00:00" class="op-modified">2018-11-07T20:34:00+00:00</time>
                </header>
                

<p>Virtual reality (VR) is an experience based in a computer-generated environment; a number of different VR products make headlines and its applications range far and wide: for the winter Olympics, the US team utilized virtual reality for athletic training; surgeons are experimenting with virtual reality for medical training; and most commonly, virtual reality is being applied to games.</p>

<p>We will focus on the last category of applications and will specifically focus on <strong>point-and-click adventure games</strong>. Such games are a casual class of games; the goal is to point and click on objects in the scene, to finish a puzzle. In this tutorial, we will build a simple version of such a game but in virtual reality. This serves as an introduction to programming in three dimensions and is a self-contained getting-started guide to deploying a virtual reality model on the web. You will be building with webVR, a framework that gives a dual advantage &mdash; users can play your game in VR and users without a VR headset can still play your game on a phone or desktop.</p>

<div class="c-felix-the-cat">
<h4>Developing For Virtual Reality</h4>
<p>Any developer can create content for VR nowadays. To get a better understanding of VR development, working a demo project can help. </p>
</div>

<p>In the second half of these tutorial, you will then build a &ldquo;mirror&rdquo; for your desktop. This means that all movements the player makes on a mobile device will be mirrored in a desktop preview. This allows you see what the player sees, allowing you to provide guidance, record the game, or simply keep guests entertained.</p>

<h3 id="prerequisites">Prerequisites</h3>

<p>To get started, you will need the following. For the second half of this tutorial, you will need a Mac OSX. Whereas the code can apply to any platform, the dependency installation instructions below are for Mac.</p>

<ul>
<li>Internet access, specifically to ;</li>
<li>A virtual reality headset (optional, recommended). I use Google Cardboard, which is offered at $15 a piece.</li>
</ul>



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




<h3 id="step-1-setting-up-a-virtual-reality-vr-model">Step 1: Setting Up A Virtual Reality (VR) Model</h3>

<p>In this step, we will set up a website with a single static HTML page. This allows us to code from your desktop and automatically deploy to the web. The deployed website can then be loaded on your mobile phone and placed inside a VR headset. Alternatively, the deployed website can be loaded by a standalone VR headset. Get started by navigating to . Then,</p>

<ol>
<li>Click on &ldquo;New Project&rdquo; in the top-right.</li>
<li>Click on &ldquo;hello-express&rdquo; in the drop-down.</li>
</ol>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b74faa49-00f9-4551-aa3a-1d04b02d4fb2/1-glitch-create.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b74faa49-00f9-4551-aa3a-1d04b02d4fb2/1-glitch-create.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b74faa49-00f9-4551-aa3a-1d04b02d4fb2/1-glitch-create.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b74faa49-00f9-4551-aa3a-1d04b02d4fb2/1-glitch-create.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b74faa49-00f9-4551-aa3a-1d04b02d4fb2/1-glitch-create.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b74faa49-00f9-4551-aa3a-1d04b02d4fb2/1-glitch-create.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b74faa49-00f9-4551-aa3a-1d04b02d4fb2/1-glitch-create.png"
			sizes="100vw"
			alt="Get started by navigating to glitch.com"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<p>Next, click on <em>views/index.html</em> in the left sidebar. We will refer to this as your “editor”.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4ac9e4ed-ebdb-48c4-bba4-18e849b7078a/1-glitch-index.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4ac9e4ed-ebdb-48c4-bba4-18e849b7078a/1-glitch-index.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4ac9e4ed-ebdb-48c4-bba4-18e849b7078a/1-glitch-index.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4ac9e4ed-ebdb-48c4-bba4-18e849b7078a/1-glitch-index.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4ac9e4ed-ebdb-48c4-bba4-18e849b7078a/1-glitch-index.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4ac9e4ed-ebdb-48c4-bba4-18e849b7078a/1-glitch-index.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4ac9e4ed-ebdb-48c4-bba4-18e849b7078a/1-glitch-index.png"
			sizes="100vw"
			alt="The next step would be to click on views/index.html in the left sidebar which will be referred to this as your “editor”."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<p>To preview the webpage, click on &ldquo;Preview&rdquo; in the top left. We will refer to this as your <em>preview</em>. Note that any changes in your editor will be automatically reflected in this preview, barring bugs or unsupported browsers.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c59257af-1efa-46cb-8d50-559db30bd228/01-building-a-point-and-click-virtual-reality-game.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c59257af-1efa-46cb-8d50-559db30bd228/01-building-a-point-and-click-virtual-reality-game.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c59257af-1efa-46cb-8d50-559db30bd228/01-building-a-point-and-click-virtual-reality-game.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c59257af-1efa-46cb-8d50-559db30bd228/01-building-a-point-and-click-virtual-reality-game.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c59257af-1efa-46cb-8d50-559db30bd228/01-building-a-point-and-click-virtual-reality-game.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c59257af-1efa-46cb-8d50-559db30bd228/01-building-a-point-and-click-virtual-reality-game.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c59257af-1efa-46cb-8d50-559db30bd228/01-building-a-point-and-click-virtual-reality-game.png"
			sizes="100vw"
			alt="To preview the webpage, click on “Preview” in the top left. We will refer to this as your preview. Note that any changes in your editor will be automatically reflected in this preview, barring bugs or unsupported browsers."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<p>Back in your editor, replace the current HTML with the following boilerplate for a VR model.</p>

<pre class="break-out"><code class="language-html">&lt;!DOCTYPE html>
&lt;html>
  &lt;head>
      &lt;script src="https://aframe.io/releases/0.7.0/aframe.min.js">&lt;/script>
  &lt;/head>
  &lt;body>
    &lt;a-scene>
      
      &lt;!-- blue sky -->
      &lt;a-sky color="#a3d0ed">&lt;/a-sky>
      
      &lt;!-- camera with wasd and panning controls -->
      &lt;a-entity camera look-controls wasd-controls position="0 0.5 2" rotation="0 0 0">&lt;/a-entity>
        
      &lt;!-- brown ground -->
      &lt;a-box shadow id="ground" shadow="receive:true" color="#847452" width="10" height="0.1" depth="10">&lt;/a-box>
        
      &lt;!-- start code here -->
      &lt;!-- end code here -->
    &lt;/a-scene>
  &lt;/body>
&lt;/html>
</code></pre>

<p>Navigate see the following.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e6252192-ff00-48dc-bac2-3759bbd0c8f8/1-preview.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e6252192-ff00-48dc-bac2-3759bbd0c8f8/1-preview.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e6252192-ff00-48dc-bac2-3759bbd0c8f8/1-preview.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e6252192-ff00-48dc-bac2-3759bbd0c8f8/1-preview.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e6252192-ff00-48dc-bac2-3759bbd0c8f8/1-preview.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e6252192-ff00-48dc-bac2-3759bbd0c8f8/1-preview.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e6252192-ff00-48dc-bac2-3759bbd0c8f8/1-preview.png"
			sizes="100vw"
			alt="When navigating back to your preview, you will see the bakground colors blue and brown."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<p>To preview this on your VR headset, use the URL in the omnibar. In the picture above, the URL is <code>https://point-and-click-vr-game.glitch.me/</code>. Your working environment is now set up; feel free to share this URL with family and friends. In the next step, you will create a virtual reality model.</p>

<div class="sponsors__wide-place"></div>




<h3 id="step-2-build-a-tree-model">Step 2: Build A Tree Model</h3>

<p>You will now create a tree, using <em>primitives</em> from . These are standard objects that Aframe has pre-programmed for ease of use. Specifically, Aframe refers to objects as <em>entities</em>. There are three concepts, related to all entities, to organize our discussion around:</p>

<ol>
<li>Geometry and material,</li>
<li>Transformation Axes,</li>
<li>Relative Transformations.</li>
</ol>

<p>First, <strong>geometry</strong> and <strong>material</strong> are two building blocks of all three-dimensional objects in code. The geometry defines the &ldquo;shape&rdquo; &mdash; a cube, a sphere, a pyramid, and so on. The material defines static properties of the shape, such as color, reflectiveness, roughness.</p>

<p>Aframe simplifies this concept for us by defining primitives, such as <code>&lt;a-box&gt;</code>, <code>&lt;a-sphere&gt;</code>, <code>&lt;a-cylinder&gt;</code> and many others to make a specification of a geometry and its material simpler. Start by defining a green sphere. On line 19 in your code, right after <code>&lt;!-- start code here --&gt;</code>, add the following.</p>

<pre class="break-out"><code class="language-css">
      &lt;!-- start code here -->
      &lt;a-sphere color="green" radius="0.5">&lt;/a-sphere>  &lt;!-- new line -->
      &lt;!-- end code here -->
</code></pre>

<p>Second, there are three axes to <strong>transform</strong> our object along. The <code>x</code> axis runs horizontally, where x values increase as we move right. The <code>y</code> axis runs vertically, where y values increase as we move up. The <code>z</code> axis runs out of your screen, where z values increase as we move towards you. We can translate, rotate, or scale entities along these three axes.</p>

<p>For example, to translate an object &ldquo;right,&rdquo; we increase its x value. To spin an object like a top, we rotate it along the y-axis. Modify line 19 to move the sphere &ldquo;up&rdquo; &mdash; this means you need to increase the sphere&rsquo;s y value. Note that all transformations are specified as <code>&lt;x&gt; &lt;y&gt; &lt;z&gt;</code>, meaning to increase its y value, you need to increase the second value. By default, all objects are located at position 0, 0, 0. Add the <code>position</code> specification below.</p>

<pre class="break-out"><code class="language-css">
      &lt;!-- start code here -->
      &lt;a-sphere color="green" radius="0.5" position="0 1 0">&lt;/a-sphere> &lt;!-- edited line -->
      &lt;!-- end code here -->
</code></pre>

<p>Third, all transformations are <strong>relative</strong> to its parent. To add a trunk to your tree, add a cylinder inside of the sphere above. This ensures that the position of your trunk is relative to the sphere&rsquo;s position. In essence, this keeps your tree together as one unit. Add the <code>&lt;a-cylinder&gt;</code> entity between the <code>&lt;a-sphere ...&gt;</code> and <code>&lt;/a-sphere&gt;</code> tags.</p>

<pre class="break-out"><code class="language-css">
      &lt;a-sphere color="green" radius="0.5" position="0 1 0">
        &lt;a-cylinder color="#84651e" position="0 -0.9 0" radius="0.05">&lt;/a-cylinder> &lt;!-- new line -->
      &lt;/a-sphere>
</code></pre>

<p>To make this treeless barebones, add more foliage, in the form of two more green spheres.</p>

<pre class="break-out"><code class="language-css">
      &lt;a-sphere color="green" radius="0.5" position="0 0.75 0">
        &lt;a-cylinder color="#84651e" position="0 -0.9 0" radius="0.05">&lt;/a-cylinder>
        &lt;a-sphere color="green" radius="0.35" position="0 0.5 0">&lt;/a-sphere> &lt;!-- new line -->
        &lt;a-sphere color="green" radius="0.2" position="0 0.8 0">&lt;/a-sphere> &lt;!-- new line -->
      &lt;/a-sphere>
</code></pre>

<p>Navigate back to your preview, and you will see the following tree:</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c3d4c67a-4c16-4c50-9a78-66f7c34c54df/2-tree.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c3d4c67a-4c16-4c50-9a78-66f7c34c54df/2-tree.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c3d4c67a-4c16-4c50-9a78-66f7c34c54df/2-tree.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c3d4c67a-4c16-4c50-9a78-66f7c34c54df/2-tree.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c3d4c67a-4c16-4c50-9a78-66f7c34c54df/2-tree.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c3d4c67a-4c16-4c50-9a78-66f7c34c54df/2-tree.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c3d4c67a-4c16-4c50-9a78-66f7c34c54df/2-tree.png"
			sizes="100vw"
			alt="When navigating back to your preview, you will now be able to see a green tree placed in your background."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<p>Reload the website preview on your VR headset, and check out your new tree. In the next section, we will make this tree interactive.</p>

<div class="sponsors__wide-place"></div>




<h3 id="step-3-add-click-interaction-to-model">Step 3: Add Click Interaction To Model</h3>

<p>To make an entity interactive, you will need to:</p>

<ul>
<li>Add an animation,</li>
<li>Have this animation trigger on click.</li>
</ul>

<p>Since the end user is using a virtual reality headset, clicking is equivalent to staring: in other words, stare at an object to &ldquo;click&rdquo; on it. To effect these changes, you will start with the cursor. Redefine the camera, by replacing line 13 with the following.</p>

<pre class="break-out"><code class="language-html">&lt;a-entity camera look-controls wasd-controls position="0 0.5 2" rotation="0 0 0"&gt;
  &lt;a-entity cursor="fuse: true; fuseTimeout: 250"
            position="0 0 -1"
            geometry="primitive: ring; radiusInner: 0.02; radiusOuter: 0.03"
            material="color: black; shader: flat"
            scale="0.5 0.5 0.5"
            raycaster="far: 20; interval: 1000; objects: .clickable"&gt;
    &lt;!-- add animation here --&gt;
  &lt;/a-entity&gt;
&lt;/a-entity&gt;
</code></pre>

<p>The above adds a cursor that can trigger the clicking action. Note the <code>objects: .clickable</code> property. This means that all objects with the class &ldquo;clickable&rdquo; will trigger the animation and receive a &ldquo;click&rdquo; command where appropriate. You will also add an animation to the click cursor, so that users know when the cursor triggers a click. Here, the cursor will shrink slowly when pointing at a clickable object, snapping after a second to denote an object has been clicked. Replace the comment <code>&lt;!-- add animation here --&gt;</code> with the following code:</p>

<pre class="break-out"><code class="language-html">&lt;a-animation begin="fusing" easing="ease-in" attribute="scale"
  fill="backwards" from="1 1 1" to="0.2 0.2 0.2" dur="250"&gt;&lt;/a-animation&gt;
</code></pre>

<p>Move the tree to the right by 2 units and add class &ldquo;clickable&rdquo; to the tree, by modifying line 29 to match the following.</p>

<pre class="break-out"><code class="language-html">&lt;a-sphere color="green" radius="0.5" position="2 0.75 0" class="clickable"&gt;
</code></pre>

<p>Next, you will:</p>

<ul>
<li>Specify an animation,</li>
<li>Trigger the animation with a click.</li>
</ul>

<p>Due to Aframe&rsquo;s easy-to-use animation entity, both steps can be done in quick succession.</p>

<p>Add an <code>&lt;a-animation&gt;</code> tag on line 33, right after the <code>&lt;a-cylinder&gt;</code> tag but before the end of the <code>&lt;/a-sphere&gt;</code>.</p>

<pre class="break-out"><code class="language-html">&lt;a-animation begin="click" attribute="position" from="2 0.75 0" to="2.2 0.75 0" fill="both" direction="alternate" repeat="1"&gt;&lt;/a-animation&gt;
</code></pre>

<p>The above properties specify a number of configurations for the animation. The animation:</p>

<ul>
<li>Is triggered by the <code>click</code> event</li>
<li>Modifies the tree&rsquo;s <code>position</code></li>
<li>Starts from the original position <code>2 0.75 0</code></li>
<li>Ends in <code>2.2 0.75 0</code> (moving 0.2 units to the right)</li>
<li>Animates when traveling to and from the destination</li>
<li>Alternates animation between traveling to and from the destination</li>
<li>Repeats this animation once. This means the object animates twice in total &mdash; once to the destination and once back to the original position.</li>
</ul>

<p>Finally, navigate to your preview, and drag from the cursor to your tree. Once the black circle rests on the tree, the tree will move to the right and back.</p>

<figure></figcaption></figure>

<p>This concludes the basics needed to build a point-and-click adventure game, in virtual reality. To view and play a more complete version of this game, see the following . The mission is to open the gate and hide the tree behind the gate, by clicking on various objects in the scene.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/81b2a884-a89a-4d14-9189-8c78498f5f51/shift.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/81b2a884-a89a-4d14-9189-8c78498f5f51/shift.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/81b2a884-a89a-4d14-9189-8c78498f5f51/shift.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/81b2a884-a89a-4d14-9189-8c78498f5f51/shift.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/81b2a884-a89a-4d14-9189-8c78498f5f51/shift.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/81b2a884-a89a-4d14-9189-8c78498f5f51/shift.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/81b2a884-a89a-4d14-9189-8c78498f5f51/shift.png"
			sizes="100vw"
			alt="The mission is to open the gate and hide the tree behind the gate, by clicking on various objects in the scene."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<p>Next, we set up a simple nodeJS server to serve our static demo.</p>

<h3 id="step-4-setup-nodejs-server">Step 4: Setup NodeJS Server</h3>

<p>In this step, we will set up a basic, functional nodeJS server that serves your existing VR model. In the left sidebar of your editor, select <code>package.json</code>.</p>

<p>Start by deleting lines 2-4.</p>

<pre class="break-out"><code class="language-javascript">"//1": "describes your app and its dependencies",
"//2": "https://docs.npmjs.com/files/package.json",
"//3": "updating this file will download and update your packages", 
</code></pre>

<p>Change the name to <code>mirrorvr</code>.</p>

<pre><code class="language-javascript">{
  "name": "mirrorvr", // change me
  "version": "0.0.1",
  ...
</code></pre>

<p>Under <code>dependencies</code>, add <code>socket.io</code>.</p>

<pre><code class="language-javascript">"dependencies": {
  "express": "^4.16.3",
  "socketio": "^1.0.0",
},
</code></pre>

<p>Update the repository URL to match your current glitch&rsquo;s. The example glitch project is named <code>point-and-click-vr-game</code>. Replace that with your glitch project&rsquo;s name.</p>

<pre class="break-out"><code class="language-javascript">"repository": {
  "url": "https://glitch.com/edit/#!/point-and-click-vr-game"
},
</code></pre>

<p>Finally, Change the <code>&quot;glitch&quot;</code> tag to <code>&quot;vr&quot;</code>.</p>

<pre><code class="language-javascript">"keywords": [
  "node",
  "vr",  // change me
  "express"
]
</code></pre>

<p>Double check that your <code>package.json</code> now matches the following.</p>

<pre class="break-out"><code class="language-javascript">{
  "name": "mirrorvr",
  "version": "0.0.1",
  "description": "Mirror virtual reality models",
  "main": "server.js",
  "scripts": {
    "start": "node server.js"
  },
  "dependencies": {
    "express": "^4.16.3",
    "socketio": "^1.0.0"
  },
  "engines": {
    "node": "8.x"
  },
  "repository": {
    "url": "https://glitch.com/edit/#!/point-and-click-vr-game"
  },
  "license": "MIT",
  "keywords": [
    "node",
    "vr",
    "express"
  ]
}
</code></pre>

<p>Double check that your code from the previous parts matches the following, in <code>views/index.html</code>.</p>

<pre class="break-out"><code class="language-html">&lt;!DOCTYPE html&gt;
&lt;html&gt;
  &lt;head&gt;
      &lt;script src="https://aframe.io/releases/0.7.0/aframe.min.js"&gt;&lt;/script&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;a-scene&gt;
      
      &lt;!-- blue sky --&gt;
      &lt;a-sky color="#a3d0ed"&gt;&lt;/a-sky&gt;
      
      &lt;!-- camera with wasd and panning controls --&gt;
      &lt;a-entity camera look-controls wasd-controls position="0 0.5 2" rotation="0 0 0"&gt;
        &lt;a-entity cursor="fuse: true; fuseTimeout: 250"
                  position="0 0 -1"
                  geometry="primitive: ring; radiusInner: 0.02; radiusOuter: 0.03"
                  material="color: black; shader: flat"
                  scale="0.5 0.5 0.5"
                  raycaster="far: 20; interval: 1000; objects: .clickable"&gt;
            &lt;a-animation begin="fusing" easing="ease-in" attribute="scale"
               fill="backwards" from="1 1 1" to="0.2 0.2 0.2" dur="250"&gt;&lt;/a-animation&gt;
        &lt;/a-entity&gt;
      &lt;/a-entity&gt;
        
      &lt;!-- brown ground --&gt;
      &lt;a-box shadow id="ground" shadow="receive:true" color="#847452" width="10" height="0.1" depth="10"&gt;&lt;/a-box&gt;
        
      &lt;!-- start code here --&gt;
      &lt;a-sphere color="green" radius="0.5" position="2 0.75 0" class="clickable"&gt;
        &lt;a-cylinder color="#84651e" position="0 -0.9 0" radius="0.05"&gt;&lt;/a-cylinder&gt;
        &lt;a-sphere color="green" radius="0.35" position="0 0.5 0"&gt;&lt;/a-sphere&gt;
        &lt;a-sphere color="green" radius="0.2" position="0 0.8 0"&gt;&lt;/a-sphere&gt;
        &lt;a-animation begin="click" attribute="position" from="2 0.75 0" to="2.2 0.75 0" fill="both" direction="alternate" repeat="1"&gt;&lt;/a-animation&gt;
      &lt;/a-sphere&gt;
      &lt;!-- end code here --&gt;
    &lt;/a-scene&gt;
  &lt;/body&gt;
&lt;/html&gt;
</code></pre>

<p>Modify the existing <code>server.js</code>.</p>

<p>Start by importing several NodeJS utilities.</p>

<ul>
<li><strong>Express</strong><br />
This is the web framework we will use to run the server.</li>
<li><strong>http</strong><br />
This allows us to launch a daemon, listening for activity on various ports.</li>
<li><strong>socket.io</strong><br />
The sockets implementation that allows us to communicate between client-side and server-side in nearly real-time.</li>
</ul>

<p>While importing these utilities, we additionally initialize the ExpressJS application. Note the first two lines are already written for you.</p>

<pre><code class="language-javascript">var express = require('express');
var app = express();

/* start new code */
var http = require('http').Server(app);
var io = require('socket.io')(http);
/* end new code */

// we've started you off with Express, 
</code></pre>

<p>With the utilities loaded, the provided server next instructs the server to return <code>index.html</code> as the homepage. Note there is no new code written below; this is simply an explanation of the existing source code.</p>

<pre><code class="language-javascript">// http://expressjs.com/en/starter/basic-routing.html
app.get('/', function(request, response) {
  response.sendFile(__dirname + '/views/index.html');
});
</code></pre>

<p>Finally, the existing source code instructs the application to bind to and listen to a port, which is 3000 by default unless specified otherwise.</p>

<pre class="break-out"><code class="language-javascript">// listen for requests :)
var listener = app.listen(process.env.PORT, function() {
  console.log('Your app is listening on port ' + listener.address().port);
});
</code></pre>

<p>Once you are finished editing, Glitch automatically reloads the server. Click on &ldquo;Show&rdquo; in the top-left to preview your application.</p>

<p>Your web application is now up and running. Next, we will send messages from the client to the server.</p>

<h3 id="step-5-send-information-from-client-to-server">Step 5: Send Information From Client To Server</h3>

<p>In this step, we will use the client to initialize a connection with the server. The client will additionally inform the server if it is a phone or a desktop. To start, import the soon-to-exist Javascript file in your <code>views/index.html</code>.</p>

<p>After line 4, include a new script.</p>

<pre class="break-out"><code class="language-html">&lt;script src="/client.js" type="text/javascript"&gt;&lt;/script&gt;
</code></pre>

<p>On line 14, add <code>camera-listener</code> to the list of properties for the camera entity.</p>

<pre><code class="language-html">&lt;a-entity camera-listener camera look-controls...&gt;
    ...
&lt;/a-entity&gt;
</code></pre>

<p>Then, navigate to <code>public/client.js</code> in the left sidebar. Delete all Javascript code in this file. Then, define a utility function that checks if the client is a mobile device.</p>

<pre class="break-out"><code class="language-javascript">/**
 * Check if client is on mobile
 */
function mobilecheck() {
  var check = false;
  (function(a){if(/(android|bb\d+|meego).+mobile|avantgo|bada\/|blackberry|blazer|compal|elaine|fennec|hiptop|iemobile|ip(hone|od)|iris|kindle|lge |maemo|midp|mmp|mobile.+firefox|netfront|opera m(ob|in)i|palm( os)?|phone|p(ixi|re)\/|plucker|pocket|psp|series(4|6)0|symbian|treo|up\.(browser|link)|vodafone|wap|windows ce|xda|xiino/i.test(a)||/1207|6310|6590|3gso|4thp|50[1-6]i|770s|802s|a wa|abac|ac(er|oo|s\-)|ai(ko|rn)|al(av|ca|co)|amoi|an(ex|ny|yw)|aptu|ar(ch|go)|as(te|us)|attw|au(di|\-m|r |s )|avan|be(ck|ll|nq)|bi(lb|rd)|bl(ac|az)|br(e|v)w|bumb|bw\-(n|u)|c55\/|capi|ccwa|cdm\-|cell|chtm|cldc|cmd\-|co(mp|nd)|craw|da(it|ll|ng)|dbte|dc\-s|devi|dica|dmob|do(c|p)o|ds(12|\-d)|el(49|ai)|em(l2|ul)|er(ic|k0)|esl8|ez([4-7]0|os|wa|ze)|fetc|fly(\-|_)|g1 u|g560|gene|gf\-5|g\-mo|go(\.w|od)|gr(ad|un)|haie|hcit|hd\-(m|p|t)|hei\-|hi(pt|ta)|hp( i|ip)|hs\-c|ht(c(\-| |_|a|g|p|s|t)|tp)|hu(aw|tc)|i\-(20|go|ma)|i230|iac( |\-|\/)|ibro|idea|ig01|ikom|im1k|inno|ipaq|iris|ja(t|v)a|jbro|jemu|jigs|kddi|keji|kgt( |\/)|klon|kpt |kwc\-|kyo(c|k)|le(no|xi)|lg( g|\/(k|l|u)|50|54|\-[a-w])|libw|lynx|m1\-w|m3ga|m50\/|ma(te|ui|xo)|mc(01|21|ca)|m\-cr|me(rc|ri)|mi(o8|oa|ts)|mmef|mo(01|02|bi|de|do|t(\-| |o|v)|zz)|mt(50|p1|v )|mwbp|mywa|n10[0-2]|n20[2-3]|n30(0|2)|n50(0|2|5)|n7(0(0|1)|10)|ne((c|m)\-|on|tf|wf|wg|wt)|nok(6|i)|nzph|o2im|op(ti|wv)|oran|owg1|p800|pan(a|d|t)|pdxg|pg(13|\-([1-8]|c))|phil|pire|pl(ay|uc)|pn\-2|po(ck|rt|se)|prox|psio|pt\-g|qa\-a|qc(07|12|21|32|60|\-[2-7]|i\-)|qtek|r380|r600|raks|rim9|ro(ve|zo)|s55\/|sa(ge|ma|mm|ms|ny|va)|sc(01|h\-|oo|p\-)|sdk\/|se(c(\-|0|1)|47|mc|nd|ri)|sgh\-|shar|sie(\-|m)|sk\-0|sl(45|id)|sm(al|ar|b3|it|t5)|so(ft|ny)|sp(01|h\-|v\-|v )|sy(01|mb)|t2(18|50)|t6(00|10|18)|ta(gt|lk)|tcl\-|tdg\-|tel(i|m)|tim\-|t\-mo|to(pl|sh)|ts(70|m\-|m3|m5)|tx\-9|up(\.b|g1|si)|utst|v400|v750|veri|vi(rg|te)|vk(40|5[0-3]|\-v)|vm40|voda|vulc|vx(52|53|60|61|70|80|81|83|85|98)|w3c(\-| )|webc|whit|wi(g |nc|nw)|wmlb|wonu|x700|yas\-|your|zeto|zte\-/i.test(a.substr(0,4))) check = true;})(navigator.userAgent||navigator.vendor||window.opera);
  return check;
};
</code></pre>

<p>Next, we will define a series of initial messages to exchange with the server side. Define a new socket.io object to represent the client&rsquo;s connection to the server. Once the socket connects, log a message to the console.</p>

<pre><code class="language-javascript">var socket = io();

socket.on('connect', function() {
  console.log(' * Connection established');
});
</code></pre>

<p>Check if the device is mobile, and send corresponding information to the server, using the function <code>emit</code>.</p>

<pre><code class="language-javascript">if (mobilecheck()) {
  socket.emit('newHost');
} else {
  socket.emit('newMirror');
}
</code></pre>

<p>This concludes the client&rsquo;s message sending. Now, amend the server code to receive this message and react appropriately. Open the server <code>server.js</code> file.</p>

<p>Handle new connections, and immediately listen for the type of client. At the end of the file, add the following.</p>

<pre><code class="language-javascript">/**
 * Handle socket interactions
 */

io.on('connection', function(socket) {

  socket.on('newMirror', function() {
    console.log(" * Participant registered as 'mirror'")
  });

  socket.on('newHost', function() {
    console.log(" * Participant registered as 'host'");
  });
});
</code></pre>

<p>Again, preview the application by clicking on &ldquo;Show&rdquo; in the top left. Load that same URL on your mobile device. In your terminal, you will see the following.</p>

<pre><code class="language-javascript">listening on *: 3000
 * Participant registered as 'host'
 * Participant registered as 'mirror'
</code></pre>

<p>This is the first of simple message-passing, where our client sends information back to the server. Quit the running NodeJS process. For the final part of this step, we will have the client send camera information back to the server. Open <code>public/client.js</code>.</p>

<p>At the very end of the file, include the following.</p>

<pre><code class="language-javascript">var camera;
if (mobilecheck()) {
  AFRAME.registerComponent('camera-listener', {
    tick: function () {
      camera = this.el.sceneEl.camera.el;
      var position = camera.getAttribute('position');
      var rotation = camera.getAttribute('rotation');
      socket.emit('onMove', {
        "position": position,
        "rotation": rotation
      });
    }
  });
}
</code></pre>

<p>Save and close. Open your server file <code>server.js</code> to listen for this <code>onMove</code> event.</p>

<p>Add the following, in the <code>newHost</code> block of your socket code.</p>

<pre><code class="language-javascript">socket.on('newHost', function() {
    console.log(" * Participant registered as 'host'");
    /* start new code */
    socket.on('onMove', function(data) {
      console.log(data);
    });
    /* end new code */
  });
</code></pre>

<p>Once again, load the preview on your desktop and on your mobile device. Once a mobile client is connected, the server will immediately begin logging camera position and rotation information, sent from the client to the server. Next, you will implement the reverse, where you send information from the server back to the client.</p>

<h3 id="step-6-send-information-from-server-to-client">Step 6: Send Information From Server To Client</h3>

<p>In this step, you will send a host&rsquo;s camera information to all mirrors. Open your main server file, <code>server.js</code>.</p>

<p>Change the <code>onMove</code> event handler to the following:</p>

<pre><code class="language-javascript">socket.on('onMove', function(data) {
  console.log(data);  // delete me
  socket.broadcast.emit('move', data)
});
</code></pre>

<p>The <code>broadcast</code> modifier ensures that the server sends this information to all clients connected to the socket, except for the original sender. Once this information is sent to a client, you then need to set the mirror&rsquo;s camera accordingly. Open the client script, <code>public/client.js</code>.</p>

<p>Here, check if the client is a desktop. If so, receive the move data and log accordingly.</p>

<pre><code class="language-javascript">if (!mobilecheck()) {
  socket.on('move', function(data) {
    console.log(data);
  });
}
</code></pre>

<p>Load the preview on your desktop and on your mobile device. In your desktop browser, open the developer console. Then, load the app on your mobile phone. As soon as the mobile phone loads the app, the developer console on your desktop should light up with camera position and rotation.</p>

<p>Open the client script once more, at <code>public/client.js</code>. We finally adjust the client camera depending on the information sent.</p>

<p>Amend the event handler above for the <code>move</code> event.</p>

<pre><code class="language-javascript">socket.on('move', function(data) {
  /* start new code */
  camera.setAttribute('rotation', data["rotation"]);
  camera.setAttribute('position', data["position"]);
  /* end new code */
});
</code></pre>

<p>Load the app on your desktop and your phone. Every movement of your phone is reflected in the corresponding mirror on your desktop! This concludes the mirror portion of your application. As a desktop user, you can now preview what your mobile user sees. The concepts introduced in this section will be crucial for further development of this game, as we transform a single-player to a multiplayer game.</p>

<h3 id="conclusion">Conclusion</h3>

<p>In this tutorial, we programmed three-dimensional objects and added simple interactions to these objects. Additionally, you built a simple message passing system between clients and servers, to effect a desktop preview of what your mobile users see.</p>

<p>These concepts extend beyond even webVR, as the notion of a geometry and material extend to SceneKit on iOS (which is related to ARKit), Three.js (the backbone for Aframe), and other three-dimensional libraries. These simple building blocks put together allow us ample flexibility in creating a fully-fledged point-and-click adventure game. More importantly, they allow us to create any game with a click-based interface.</p>

<p>Here are several resources and examples to further explore:</p>

<ul>
<li><br />
A fully-fledged implementation of the live preview built above. With just a single Javascript link, add a live preview of any virtual reality model on mobile to a desktop.</li>
<li><br />
A gallery of kids’ drawings and each drawing&rsquo;s corresponding virtual reality model.</li>
<li><br />
Examples, developer documentation, and more resources for virtual reality development.</li>
<li><br />
Experiences for the classroom with custom tools for educators.</li>
</ul>

<p>Next time, we will build a complete game, using web sockets to facilitate real-time communication between players in a virtual reality game. Feel free to share your own models in the comments below.</p>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(rb, ra, yk, il)</span>
</div>


              </article>
            </body>
          </html>
---------------
<h1 id="#title_4" >5、awk 入门教程</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2018/11/awk.html](http://www.ruanyifeng.com/blog/2018/11/awk.html)
<p>是处理文本文件的一个应用程序，几乎所有 Linux 系统都自带这个程序。</p>

        <p>它依次处理文件的每一行，并读取里面的每一个字段。对于日志、CSV 那样的每行格式相同的文本文件，<code>awk</code>可能是最方便的工具。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201811/bg2018110702.jpg" alt="" title="" /></p>

<p><code>awk</code>其实不仅仅是工具软件，还是一种编程语言。不过，本文只介绍它的命令行用法，对于大多数场合，应该足够用了。</p>

<h2>一、基本用法</h2>

<p><code>awk</code>的基本用法就是下面的形式。</p>

<blockquote><pre><code class="language-bash">
# 格式
$ awk 动作 文件名

# 示例
$ awk '{print $0}' demo.txt
</code></pre></blockquote>

<p>上面示例中，<code>demo.txt</code>是<code>awk</code>所要处理的文本文件。前面单引号内部有一个大括号，里面就是每一行的处理动作<code>print $0</code>。其中，<code>print</code>是打印命令，<code>$0</code>代表当前行，因此上面命令的执行结果，就是把每一行原样打印出来。</p>

<p><code>awk</code>也可以处理标准输入（stdin）。</p>

<blockquote><pre><code class="language-bash">
$ echo 'this is a test' | awk '{print $0}'
this is a test
</code></pre></blockquote>

<p>上面代码中，<code>print $0</code>就是把标准输入<code>this is a test</code>，重新打印了一遍。</p>

<p><code>awk</code>会根据空格和制表符，将每一行分成若干字段，依次用<code>$1</code>、<code>$2</code>、<code>$3</code>代表第一个字段、第二个字段、第三个字段等等。</p>

<blockquote><pre><code class="language-bash">
$ echo 'this is a test' | awk '{print $3}'
a
</code></pre></blockquote>

<p>上面代码中，<code>$3</code>代表<code>this is a test</code>的第三个字段<code>a</code>。</p>

<p>下面，为了便于举例，我们把<code>/etc/passwd</code>文件保存成<code>demo.txt</code>。</p>

<blockquote><pre><code class="language-bash">
root:x:0:0:root:/root:/usr/bin/zsh
daemon:x:1:1:daemon:/usr/sbin:/usr/sbin/nologin
bin:x:2:2:bin:/bin:/usr/sbin/nologin
sys:x:3:3:sys:/dev:/usr/sbin/nologin
sync:x:4:65534:sync:/bin:/bin/sync
</code></pre></blockquote>

<p>这个文件的字段分隔符是冒号（<code>:</code>），所以要用<code>-F</code>参数指定分隔符为冒号。然后，才能提取到它的第一个字段。</p>

<blockquote><pre><code class="language-bash">
$ awk -F ':' '{ print $1 }' demo.txt
root
daemon
bin
sys
sync
</code></pre></blockquote>

<h2>二、变量</h2>

<p>除了<code>$ + 数字</code>表示某个字段，<code>awk</code>还提供其他一些变量。</p>

<p>变量<code>NF</code>表示当前行有多少个字段，因此<code>$NF</code>就代表最后一个字段。</p>

<blockquote><pre><code class="language-bash">
$ echo 'this is a test' | awk '{print $NF}'
test
</code></pre></blockquote>

<p><code>$(NF-1)</code>代表倒数第二个字段。</p>

<blockquote><pre><code class="language-bash">
$ awk -F ':' '{print $1, $(NF-1)}' demo.txt
root /root
daemon /usr/sbin
bin /bin
sys /dev
sync /bin
</code></pre></blockquote>

<p>上面代码中，<code>print</code>命令里面的逗号，表示输出的时候，两个部分之间使用空格分隔。</p>

<p>变量<code>NR</code>表示当前处理的是第几行。</p>

<blockquote><pre><code class="language-bash">
$ awk -F ':' '{print NR ") " $1}' demo.txt
1) root
2) daemon
3) bin
4) sys
5) sync
</code></pre></blockquote>

<p>上面代码中，<code>print</code>命令里面，如果原样输出字符，要放在双引号里面。</p>

<p><code>awk</code>的其他内置变量如下。</p>

<blockquote>
  <ul>
<li><code>FILENAME</code>：当前文件名</li>
<li><code>FS</code>：字段分隔符，默认是空格和制表符。</li>
<li><code>RS</code>：行分隔符，用于分割每一行，默认是换行符。</li>
<li><code>OFS</code>：输出字段的分隔符，用于打印时分隔字段，默认为空格。</li>
<li><code>ORS</code>：输出记录的分隔符，用于打印时分隔记录，默认为换行符。</li>
<li><code>OFMT</code>：数字输出的格式，默认为<code>％.6g</code>。</li>
</ul>
</blockquote>

<h2>三、函数</h2>

<p><code>awk</code>还提供了一些内置函数，方便对原始数据的处理。</p>

<p>函数<code>toupper()</code>用于将字符转为大写。</p>

<blockquote><pre><code class="language-bash">
$ awk -F ':' '{ print toupper($1) }' demo.txt
ROOT
DAEMON
BIN
SYS
SYNC
</code></pre></blockquote>

<p>上面代码中，第一个字段输出时都变成了大写。</p>

<p>其他常用函数如下。</p>

<blockquote>
  <ul>
<li><code>tolower()</code>：字符转为小写。</li>
<li><code>length()</code>：返回字符串长度。</li>
<li><code>substr()</code>：返回子字符串。</li>
<li><code>sin()</code>：正弦。</li>
<li><code>cos()</code>：余弦。</li>
<li><code>sqrt()</code>：平方根。</li>
<li><code>rand()</code>：随机数。</li>
</ul>
</blockquote>

<p><code>awk</code>内置函数的完整列表，可以查看。</p>

<h2>四、条件</h2>

<p><code>awk</code>允许指定输出条件，只输出符合条件的行。</p>

<p>输出条件要写在动作的前面。</p>

<blockquote><pre><code class="language-bash">
$ awk '条件 动作' 文件名
</code></pre></blockquote>

<p>请看下面的例子。</p>

<blockquote><pre><code class="language-bash">
$ awk -F ':' '/usr/ {print $1}' demo.txt
root
daemon
bin
sys
</code></pre></blockquote>

<p>上面代码中，<code>print</code>命令前面是一个正则表达式，只输出包含<code>usr</code>的行。</p>

<p>下面的例子只输出奇数行，以及输出第三行以后的行。</p>

<blockquote><pre><code class="language-bash">
# 输出奇数行
$ awk -F ':' 'NR % 2 == 1 {print $1}' demo.txt
root
bin
sync

# 输出第三行以后的行
$ awk -F ':' 'NR >3 {print $1}' demo.txt
sys
sync
</code></pre></blockquote>

<p>下面的例子输出第一个字段等于指定值的行。</p>

<blockquote><pre><code class="language-bash">
$ awk -F ':' '$1 == "root" {print $1}' demo.txt
root

$ awk -F ':' '$1 == "root" || $1 == "bin" {print $1}' demo.txt
root
bin
</code></pre></blockquote>

<h2>五、if 语句</h2>

<p><code>awk</code>提供了<code>if</code>结构，用于编写复杂的条件。</p>

<blockquote><pre><code class="language-bash">
$ awk -F ':' '{if ($1 > "m") print $1}' demo.txt
root
sys
sync
</code></pre></blockquote>

<p>上面代码输出第一个字段的第一个字符大于<code>m</code>的行。</p>

<p><code>if</code>结构还可以指定<code>else</code>部分。</p>

<blockquote><pre><code class="language-bash">
$ awk -F ':' '{if ($1 > "m") print $1; else print "---"}' demo.txt
root
---
---
sys
sync
</code></pre></blockquote>

<h2>六、参考链接</h2>

<ul>
<li>, Greg Grothaus</li>
<li>, Mokhtar Ebrahim</li>
</ul>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2018-11-07T21:30:59+08:00">2018年11月 7日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>文集：</li>
<li>社交媒体：</li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------