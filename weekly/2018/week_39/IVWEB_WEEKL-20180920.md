## 文章索引
1、 <a href="#1git-219-对diffbranch和grep等做了改进" >Git 2.19 对Diff、Branch和Grep等做了改进</a><br/>
2、 <a href="#2visual-studio-live-share-can-do-that" >Visual Studio Live Share Can Do That?</a><br/>
3、 <a href="#3文章-c#-8中的async-streams" >文章： C# 8中的Async Streams</a><br/>
4、 <a href="#4文章-sparkflinkcarbondata技术实践最佳案例解析" >文章： Spark、Flink、CarbonData技术实践最佳案例解析</a><br/>
5、 <a href="#5文章-github我们为什么会弃用jquery" >文章： GitHub：我们为什么会弃用jQuery？</a><br/>
6、 <a href="#6从iphone-xs看手机业下一个十年要走芯了" >从iPhone XS看手机业下一个十年，要“走芯”了</a><br/>
7、 <a href="#7如何实现弹性架构" >如何实现弹性架构</a><br/>
8、 <a href="#8腾讯开源ml-images超越谷歌成业内最大多标签图像数据集" >腾讯开源ML-Images，超越谷歌成业内最大多标签图像数据集</a><br/>
9、 <a href="#9microsoft向高性能计算市场推出了新的azure产品" >Microsoft向高性能计算市场推出了新的Azure产品</a><br/>
10、 <a href="#10敏捷世界中的合规性" >敏捷世界中的合规性</a><br/>
11、 <a href="#11stack-overflow最新薪资计算器出炉devops和go语言开发者是大赢家" >Stack Overflow最新薪资计算器出炉：DevOps和Go语言开发者是大赢家</a><br/><h1 id="#title_0" >1、Git 2.19 对Diff、Branch和Grep等做了改进</h1>
Sergio De Simone
[http://www.infoq.com/cn/news/2018/09/git-2.19-released?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/09/git-2.19-released?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Git的最新版带来了丰富的新功能以及内部更新，包括改进的diff、branch和grep，更好的命令行补全，新的range-diff命令等。</p> <i>By Sergio De Simone</i> <i> Translated by 姚佳灵</i>
---------------
<h1 id="#title_1" >2、Visual Studio Live Share Can Do That?</h1>
Burke Holland
[https://www.smashingmagazine.com/2018/09/visual-studio-live/](https://www.smashingmagazine.com/2018/09/visual-studio-live/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/09/visual-studio-live/" />
              <title>Visual Studio Live Share Can Do That?</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>Visual Studio Live Share Can Do That?</h1>
                  
                    
                    <address>Burke Holland</address>
                  
                  <time datetime="2018-09-19T13:30:17&#43;02:00" class="op-published">2018-09-19T13:30:17+02:00</time>
                  <time datetime="2018-09-19T16:36:17&#43;00:00" class="op-modified">2018-09-19T16:36:17+00:00</time>
                </header>
                

<p>A few months ago, Microsoft released its free . VS Live Share is Google Docs level collaboration for code. Multiple developers can collaborate on the same file at the same time without ever leaving their own editor.</p>

<p>After the release of Live Share, I realized that many of us have resigned ourselves to being isolated in our code and we’re not even aware that there are better ways to work with a service like VS Live Share. This is partly because we are stuck in old habits and partly because we just aren’t aware of what all VS Live Share can do. That last part I can help with!</p>

<p>In this article, we’ll go over the features and best practices for VS Live Share that make developer collaboration as easy as being an “Anonymous Hippo.”</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cc379e44-11f8-4138-a4fe-5ab9523c3a1c/visual-studio-live-anonymous-hippo.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cc379e44-11f8-4138-a4fe-5ab9523c3a1c/visual-studio-live-anonymous-hippo.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cc379e44-11f8-4138-a4fe-5ab9523c3a1c/visual-studio-live-anonymous-hippo.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cc379e44-11f8-4138-a4fe-5ab9523c3a1c/visual-studio-live-anonymous-hippo.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cc379e44-11f8-4138-a4fe-5ab9523c3a1c/visual-studio-live-anonymous-hippo.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cc379e44-11f8-4138-a4fe-5ab9523c3a1c/visual-studio-live-anonymous-hippo.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cc379e44-11f8-4138-a4fe-5ab9523c3a1c/visual-studio-live-anonymous-hippo.png"
			sizes="100vw"
			alt="list of anonymous animals in Google Docs"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Google Docs has an interesting way of handling anonymous participants ()
		</figcaption>
	
</figure>


<h3 id="share-your-code">Share Your Code</h3>

<p>Live Share comes as . In this article, we’re going to focus on VS Code.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/43df4203-df06-485f-9211-1ce5eb5c3fc3/visual-studio-live-liveshare-readme.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/43df4203-df06-485f-9211-1ce5eb5c3fc3/visual-studio-live-liveshare-readme.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/43df4203-df06-485f-9211-1ce5eb5c3fc3/visual-studio-live-liveshare-readme.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/43df4203-df06-485f-9211-1ce5eb5c3fc3/visual-studio-live-liveshare-readme.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/43df4203-df06-485f-9211-1ce5eb5c3fc3/visual-studio-live-liveshare-readme.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/43df4203-df06-485f-9211-1ce5eb5c3fc3/visual-studio-live-liveshare-readme.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/43df4203-df06-485f-9211-1ce5eb5c3fc3/visual-studio-live-liveshare-readme.png"
			sizes="100vw"
			alt="vs code live share extension readme page"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<p>You can also install it via the , which includes the following extensions, all of which we are going to cover in this article&hellip;</p>

<ul>
<li>VS Live Share</li>
<li>VS Live Share Audio</li>
<li>Slack Chat extension</li>
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




<p>Once the extension is installed, you will need to log in to the VS Live Share service. You can do that by opening the Command Palette <kbd>Ctrl/Cmd</kbd> + <kbd>Shift</kbd> + <kbd>P</kbd> and select “Sign In With Browser”. If you don’t log in and you try and start a new sharing session, you will be prompted to log in at that time.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1d7e53bc-d504-425d-b771-e590087827ad/visual-studio-live-sign-in-with-browser.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1d7e53bc-d504-425d-b771-e590087827ad/visual-studio-live-sign-in-with-browser.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1d7e53bc-d504-425d-b771-e590087827ad/visual-studio-live-sign-in-with-browser.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1d7e53bc-d504-425d-b771-e590087827ad/visual-studio-live-sign-in-with-browser.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1d7e53bc-d504-425d-b771-e590087827ad/visual-studio-live-sign-in-with-browser.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1d7e53bc-d504-425d-b771-e590087827ad/visual-studio-live-sign-in-with-browser.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1d7e53bc-d504-425d-b771-e590087827ad/visual-studio-live-sign-in-with-browser.png"
			sizes="100vw"
			alt="vs code command palette showing option to sign in with browser"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Use the VS Code Command Palette to start a new Live Share session ()
		</figcaption>
	
</figure>


<p>There are several ways to kick off a VS Live Share session. You can do it from the Command Palette, you can click that “Share” button in the bottom toolbar, or you can use the VS Live Share explorer view in the Sidebar.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d8643506-c61d-4d87-945b-45ae4ca283fa/visual-studio-live-new-live-share.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d8643506-c61d-4d87-945b-45ae4ca283fa/visual-studio-live-new-live-share.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d8643506-c61d-4d87-945b-45ae4ca283fa/visual-studio-live-new-live-share.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d8643506-c61d-4d87-945b-45ae4ca283fa/visual-studio-live-new-live-share.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d8643506-c61d-4d87-945b-45ae4ca283fa/visual-studio-live-new-live-share.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d8643506-c61d-4d87-945b-45ae4ca283fa/visual-studio-live-new-live-share.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d8643506-c61d-4d87-945b-45ae4ca283fa/visual-studio-live-new-live-share.png"
			sizes="100vw"
			alt="vs code with boxes drawn around the different parts of the UI that can be used to start a live share session"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			There are a myriad of ways to start a new VS Live Share session ()
		</figcaption>
	
</figure>


<p>A link is copied to your clipboard. You can then send that link to others, and they can join your Live Share session &mdash; provided they are using VS Code as well. Which, aren’t we all?</p>

<p>Now you can collaborate just like you were working on a regular old Word document:</p>

<figure class="video-container"><iframe data-src="https://www.youtube.com/embed/3J4ZNnaX0jw" width="600" height="480" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe></figure>

<p>The other person can not only see your code, but they can edit it, save it, execute it and even debug it. For you, they show up as a cursor with a name on it. You show up in their editor the same way.</p>

<h3 id="the-vs-live-share-explorer">The VS Live Share Explorer</h3>

<p>The  shows up as a new icon in the Action Bar &mdash; which is that bar of icons on the far right of my screen (the far left of yours for default Action Bar placement). This is a sort of “ground zero” for everything VS Live Share. From here, you can start sessions, end them, share terminals, servers, and see who is connected.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/44eec113-fb05-4681-89a8-1df6cdcb8f64/visual-studio-live-live-share-explorer.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/44eec113-fb05-4681-89a8-1df6cdcb8f64/visual-studio-live-live-share-explorer.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/44eec113-fb05-4681-89a8-1df6cdcb8f64/visual-studio-live-live-share-explorer.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/44eec113-fb05-4681-89a8-1df6cdcb8f64/visual-studio-live-live-share-explorer.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/44eec113-fb05-4681-89a8-1df6cdcb8f64/visual-studio-live-live-share-explorer.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/44eec113-fb05-4681-89a8-1df6cdcb8f64/visual-studio-live-live-share-explorer.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/44eec113-fb05-4681-89a8-1df6cdcb8f64/visual-studio-live-live-share-explorer.png"
			sizes="100vw"
			alt="vs live share viewlet"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The VS Live Share Explorer is a heads-up view of all things Live Share ()
		</figcaption>
	
</figure>


<p>It’s a good idea to bind a keyboard shortcut to this VS Live Share Explorer view so that you can quickly toggle between that and your files. You can do this by pressing <kbd>Ctrl/Cmd</kbd> + <kbd>K</kbd> (or <kbd>Ctrl/Cmd</kbd> + <kbd>S</kbd>) and then searching for “Show Live Share”. I bound mine to <kbd>Ctrl/Cmd</kbd> + <kbd>L</kbd>, which doesn’t seem to be bound to anything else. I find this shortcut to be intuitive (<kbd>L</kbd> for Live Share) and easy to hit on the keyboard.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/eea40c0e-c413-4f15-87c4-82da59a75565/visual-studio-live-keyboard-shortcut-binding.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/eea40c0e-c413-4f15-87c4-82da59a75565/visual-studio-live-keyboard-shortcut-binding.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/eea40c0e-c413-4f15-87c4-82da59a75565/visual-studio-live-keyboard-shortcut-binding.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/eea40c0e-c413-4f15-87c4-82da59a75565/visual-studio-live-keyboard-shortcut-binding.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/eea40c0e-c413-4f15-87c4-82da59a75565/visual-studio-live-keyboard-shortcut-binding.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/eea40c0e-c413-4f15-87c4-82da59a75565/visual-studio-live-keyboard-shortcut-binding.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/eea40c0e-c413-4f15-87c4-82da59a75565/visual-studio-live-keyboard-shortcut-binding.png"
			sizes="100vw"
			alt="the keyboard binding screen in vs code with a binding created for the vs live share viewlet"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			You can create a binding for the VS Live Share Explorer viewlet ()
		</figcaption>
	
</figure>


<h3 id="share-code-read-only">Share Code Read-Only</h3>

<p>When you start a new sharing session, you will be notified thusly and asked if you would like to share your workspace read-only. If you select read-only, people will be able to see your code and follow your movements, but they will not be able to interact.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/123a8b5d-c0ca-43a6-9513-01d77b932509/visual-studio-live-read-only-code.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/123a8b5d-c0ca-43a6-9513-01d77b932509/visual-studio-live-read-only-code.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/123a8b5d-c0ca-43a6-9513-01d77b932509/visual-studio-live-read-only-code.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/123a8b5d-c0ca-43a6-9513-01d77b932509/visual-studio-live-read-only-code.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/123a8b5d-c0ca-43a6-9513-01d77b932509/visual-studio-live-read-only-code.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/123a8b5d-c0ca-43a6-9513-01d77b932509/visual-studio-live-read-only-code.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/123a8b5d-c0ca-43a6-9513-01d77b932509/visual-studio-live-read-only-code.png"
			sizes="100vw"
			alt="vs code notification prompting user to choose read-only sharing"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Sharing sessions are read-write by default, but you can make them read-only ()
		</figcaption>
	
</figure>


<p>This mode is useful when you are sharing with someone that you don’t necessarily trust &mdash; maybe a vendor, partner or an estranged ex.</p>

<p>It’s also particularly useful for instructors. Note that at the time of this writing, VS Live Share is locked to 5 concurrent users. Since you probably are going to want more than that in read-only mode, especially if you’re teaching a group, you can up the limit to 30 by adding the following line to your User Settings file: <kbd>Ctrl/Cmd</kbd> + <kbd>,</kbd>.</p>

<pre><code class="language-javascript">"liveshare.features": "experimental"
</code></pre>

<div class="sponsors__wide-place"></div>




<h3 id="change-the-default-join-behavior">Change The Default Join Behavior</h3>

<p>Anyone with the link can join your Live Share session. When they join, you’ll see a pop-up letting you know. Likewise, when they disconnect, you get notified. This is the default behavior for VS Live Share.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b35cd855-5e50-4d90-a33a-e554ae374268/visual-studio-live-join-notification.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b35cd855-5e50-4d90-a33a-e554ae374268/visual-studio-live-join-notification.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b35cd855-5e50-4d90-a33a-e554ae374268/visual-studio-live-join-notification.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b35cd855-5e50-4d90-a33a-e554ae374268/visual-studio-live-join-notification.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b35cd855-5e50-4d90-a33a-e554ae374268/visual-studio-live-join-notification.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b35cd855-5e50-4d90-a33a-e554ae374268/visual-studio-live-join-notification.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b35cd855-5e50-4d90-a33a-e554ae374268/visual-studio-live-join-notification.png"
			sizes="100vw"
			alt="vs code notification with the name of the person who has joined the live share session"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			VS Code will alert you whenever someone joins your session ()
		</figcaption>
	
</figure>


<p>It’s a good idea to change this so that you have to manually approve someone before they can join your session. This is to protect you in the case where you go to lunch and forget to disconnect your session. Your co-workers can’t log back in, change one letter in your database connection string and then laugh while you spend the next four hours trying to figure out how your life has gone so horribly wrong.</p>

<p>To enable this, add the following line to your User Settings file <kbd>Ctrl/Cmd</kbd> + <kbd>,</kbd>.</p>

<pre><code class="language-javascript">"liveshare.guestApprovalRequired": true
</code></pre>

<p>Now you’ll be prompted when someone wants to join. If you block someone, they are blocked for the duration of the session. If they try to join again, you won’t be notified and they will be unceremoniously rejected by VS Live Share.</p>

<figure class="video-container"><iframe data-src="https://www.youtube.com/embed/RwO3QnzpOF8" width="600" height="480" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe></figure>

<p>Go and enjoy your lunch. Your computer is safe.</p>

<h3 id="focus-followers">Focus Followers</h3>

<p>By default, anyone who joins your Live Share session is  you. That means that their editor will load up whatever file you are in and scroll whenever you scroll. Even if you switch files, participants will see exactly what you see.</p>

<p>The second that a person makes changes to a file, they are no longer following you. So if you are both working on a file together, and then you go to a different file, they won’t automatically go with you. That can lead to a lot of confusion with you talking about code in the file you’re in while the other person is looking at something entirely different.</p>

<p>Besides just telling each other where you are (which works, btw), there is a handy command called “Focus Participants” that is in the Command Palette <kbd>Ctrl/Cmd</kbd> + <kbd>Shift</kbd> + <kbd>P</kbd>.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/62e07f51-0221-4b2b-8762-74060ddf587b/visual-studio-live-command-palette-focus.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/62e07f51-0221-4b2b-8762-74060ddf587b/visual-studio-live-command-palette-focus.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/62e07f51-0221-4b2b-8762-74060ddf587b/visual-studio-live-command-palette-focus.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/62e07f51-0221-4b2b-8762-74060ddf587b/visual-studio-live-command-palette-focus.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/62e07f51-0221-4b2b-8762-74060ddf587b/visual-studio-live-command-palette-focus.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/62e07f51-0221-4b2b-8762-74060ddf587b/visual-studio-live-command-palette-focus.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/62e07f51-0221-4b2b-8762-74060ddf587b/visual-studio-live-command-palette-focus.png"
			sizes="100vw"
			alt="vs code command palette showing live share focus command"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Access the “focus” command from the VS Code Command Palette ()
		</figcaption>
	
</figure>


<p>You can also access it as an icon in the VS Live Share Explorer view.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6e50d868-9766-41a5-a13c-8f872270a6d7/visual-studio-live-explorer-focus-icon.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6e50d868-9766-41a5-a13c-8f872270a6d7/visual-studio-live-explorer-focus-icon.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6e50d868-9766-41a5-a13c-8f872270a6d7/visual-studio-live-explorer-focus-icon.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6e50d868-9766-41a5-a13c-8f872270a6d7/visual-studio-live-explorer-focus-icon.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6e50d868-9766-41a5-a13c-8f872270a6d7/visual-studio-live-explorer-focus-icon.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6e50d868-9766-41a5-a13c-8f872270a6d7/visual-studio-live-explorer-focus-icon.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6e50d868-9766-41a5-a13c-8f872270a6d7/visual-studio-live-explorer-focus-icon.png"
			sizes="100vw"
			alt="vs code live share explorer focus icon"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Send a follow request by clicking the follow icon in the VS Live Share Explorer viewlet ()
		</figcaption>
	
</figure>


<p>This will focus your participants on the next thing you click on or scroll to. By default, VS Live Share focus requests are accepted implicitly. If you don’t want people to be able to focus you, you can add the following line to your User Settings file.</p>

<pre><code class="language-javascript">"liveshare.focusBehavior": "prompt"
</code></pre>

<figure class="video-container"><iframe data-src="https://www.youtube.com/embed/IMy-Q6I8AvI" width="600" height="480" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe></figure>

<p>Also note that you can follow participants. If you click on their name in the VS Live Share Explorer view, you will begin to follow them.</p>

<p>Because following is turned off as soon as the other person begins editing code, it can be tough to know exactly when people are following you and when they aren’t. One place you can look is in the VS Live Share Explorer view. It will tell you the file that a person is in, but not whether or not they are following you.</p>

<p>A good practice is to just remember that focus is always changing so people may or may not see what you see at any given time.</p>

<h3 id="debug-as-a-team">Debug As A Team</h3>

<p>Participants can share any debug sessions that you run. If you start a debug session, they will get the exact same experience that you do. If it breaks on your side, it breaks on theirs, and they get the full debug view into all of your code.</p>

<figure class="video-container"><iframe data-src="https://www.youtube.com/embed/S3q6maLUxVo" width="600" height="480" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe></figure>

<p>They can step in, out, over, add watches, evaluate in the Debug Console; any debugging that you can do, they can do too, and they can control it.</p>

<p>Debugging can also be launched by participants. Be default, though, VS Code does not allow your debugger to be started remotely. To enable this, add the following line to your User Settings file <kbd>Ctrl/Cmd</kbd> + <kbd>,</kbd>:</p>

<pre><code class="language-javascript">"liveshare.allowGuestDebugControl": true
</code></pre>

<h3 id="share-your-terminal">Share Your Terminal</h3>

<p>A lot of the work we do as developers isn’t in our code; it’s in the terminal. Some days it seems like I spend about as much time on my terminal as I do in my editor. This means that if you have an error on your terminal or need to type some command, it would be nice if your participants in VS Live Share can see your terminal in addition to your code.</p>

<p>VS Code has an .</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b8734f4d-2281-4e75-92aa-954ff1096dab/visual-studio-live-command-palette-share-terminal.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b8734f4d-2281-4e75-92aa-954ff1096dab/visual-studio-live-command-palette-share-terminal.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b8734f4d-2281-4e75-92aa-954ff1096dab/visual-studio-live-command-palette-share-terminal.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b8734f4d-2281-4e75-92aa-954ff1096dab/visual-studio-live-command-palette-share-terminal.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b8734f4d-2281-4e75-92aa-954ff1096dab/visual-studio-live-command-palette-share-terminal.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b8734f4d-2281-4e75-92aa-954ff1096dab/visual-studio-live-command-palette-share-terminal.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b8734f4d-2281-4e75-92aa-954ff1096dab/visual-studio-live-command-palette-share-terminal.png"
			sizes="100vw"
			alt="vs code command palette with share terminal selected"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Access the “Share Terminal” command from the VS Code Command Palette ()
		</figcaption>
	
</figure>


<p>When you do this, you have the opportunity to share your terminal as read-only, or as read-write.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9b11f241-4c53-44de-8b1f-acb0e8218cc6/visual-studio-live-share-terminal-read-write.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9b11f241-4c53-44de-8b1f-acb0e8218cc6/visual-studio-live-share-terminal-read-write.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9b11f241-4c53-44de-8b1f-acb0e8218cc6/visual-studio-live-share-terminal-read-write.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9b11f241-4c53-44de-8b1f-acb0e8218cc6/visual-studio-live-share-terminal-read-write.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9b11f241-4c53-44de-8b1f-acb0e8218cc6/visual-studio-live-share-terminal-read-write.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9b11f241-4c53-44de-8b1f-acb0e8218cc6/visual-studio-live-share-terminal-read-write.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9b11f241-4c53-44de-8b1f-acb0e8218cc6/visual-studio-live-share-terminal-read-write.png"
			sizes="100vw"
			alt="vs code prompting to share terminal as read-only or read-write"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Always share your terminal read-only unless you absolutely have to share it with write access ()
		</figcaption>
	
</figure>


<p>By default, you should be sharing your terminal as read-only. When you share your terminal read-write, the user can execute arbitrary commands directly on your terminal. Let that sink in for a moment. That’s heavy.</p>

<p>It goes without saying that having remote write access to someone’s terminal comes with a lot of trust and responsibility. You should only ever share your terminal read-write with people that you trust implicitly. Estranged ex’s are probably off the table.</p>

<p>Sharing your terminal read-only safely allows the person on the other end of the line to see what you are typing and your terminal output in real time, but restricts them from typing anything into that terminal.</p>

<figure class="video-container"><iframe data-src="https://www.youtube.com/embed/jucRYRXEkGU" width="600" height="480" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe></figure>

<p>Should you find yourself in a scenario where it would be quicker for the other person to just get at your terminal instead of trying to walk you through some wacky command with a ton of flags, you can share your terminal read-write. In this mode, the other person has full remote access to your terminal. Choose your friends wisely.</p>

<div class="sponsors__wide-place"></div>




<h3 id="share-your-localhost">Share Your localhost</h3>

<p>In the video above, the terminal command ends with a link to a site running on . With VS Live Share, you can share that localhost so that the other person can access it just like it was their own localhost.</p>

<figure class="video-container"><iframe data-src="https://www.youtube.com/embed/UovIFgwfF-M" width="600" height="480" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe></figure>

<p>If you are running a shared debug session, when the participant hits that localhost URL on their end, it will break for both of you if a breakpoint is hit. Even better, you can share any TCP process. That means that you can share something like a database or a Redis cache. For instance, you could share your local Mongo DB server. Seriously! This means no more changing config files or trying to get a shared database up. Just share the port for your local Mongo DB instance.</p>

<figure class="video-container"><iframe data-src="https://www.youtube.com/embed/oK6L0nZU8_E" width="600" height="480" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe></figure>

<h3 id="share-the-right-files-the-right-way">Share The Right Files The Right Way</h3>

<p>Sometimes you don’t want collaborators to see certain files. There are likely private keys and passwords in your project that are not checked into source control and not suitable for public viewing. In this case, you would want to hide those files from anyone participating in your Live Share session.</p>

<p>By default, VS Live Share will hide any file that is specified in your <code>.gitignore</code>. If there is a file that you want to hide, just add it to your <code>.gitignore</code>. Note though, that this only hides the file in the project view. If you are in a shared debugging session and you step into a file that is in the <code>.gitignore</code>, it is still loaded up in the editor and your collaborators will be able to see it.</p>

<p>You can get more fine-grained control over how you share files by creating a <code>.vsls.json</code> file.</p>

<p>For instance, if you wanted to make sure that any files that are in the <code>.gitignore</code> are never visible, even during debugging, you can set the <code>gitignore</code> property to <code>exclude</code>.</p>

<pre><code class="language-javascript">{
    "$schema": "http://json.schemastore.org/vsls",
    "gitignore":"exclude"
}
</code></pre>

<p>Likewise, you could show everything in your <code>.gitignore</code> and control file visibilty directly from the <code>.vsls.json</code> file. To do that, set the <code>gitignore</code> to <code>none</code> and then use the <code>excludeFiles</code> and <code>hideFiles</code> properties. Remember &mdash; exclude means never visible, and hide means “not visible in the file explorer.”</p>

<pre><code class="language-javascript">{
    "$schema": "http://json.schemastore.org/vsls",
    "gitignore":"none",
    "excludeFiles":[
        "*.env"
    ],
    "hideFiles": [
        "dist"
    ]
}
</code></pre>

<h3 id="sharing-and-extensions">Sharing And Extensions</h3>

<p>Part of the appeal of VS Code to a lot of developers is the massive . Most people will have more than a few installed. It’s important to understand how extensions will work, or not work, in the context of VS Live Share.</p>

<p>VS Live Share will synchronize anything that is specific to the context of the project you are sharing. For instance, if you have the Vetur extension installed because you are working with a Vue project, it will be shared across to any participants &mdash; regardless of whether or not they have it installed as well. The same is true for other context-specific things, like linters, formatters, debuggers, and language services.</p>

<p>VS Live Share does not synchronize extensions that are user specific. These would be things like themes, icons, keyboard bindings, and so on. As a general rule of thumb, VS Live Share shares your context, not your screen. You can consult  for a more in-depth explanation of what extensions you can expect to be shared.</p>

<h3 id="communicate-while-you-collaborate">Communicate While You Collaborate</h3>

<p>One of the first things people do on their inaugural VS Live Share experience is to try to communicate by typing in code comments. This seems like the write (get it?) thing to do, but not really how VS Live Share was designed to be used.</p>

<p>VS Live Share is not meant to replace your chat client of choice. You likely already have a preferred chat mechanism, and VS Live Share assumes that you will continue to use that.</p>

<p>If you’re already using Slack, there is a VS Code extension called . This extension is still a tad early in its development, but it looks quite promising. It puts VS Code in split mode and embeds Slack on the right-hand side. Even better, you can start a Live Share session directly from the Slack chat.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/78f5e1f3-e182-4ee9-92b1-3e398cc10f2a/visual-studio-live-slack-chat.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/78f5e1f3-e182-4ee9-92b1-3e398cc10f2a/visual-studio-live-slack-chat.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/78f5e1f3-e182-4ee9-92b1-3e398cc10f2a/visual-studio-live-slack-chat.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/78f5e1f3-e182-4ee9-92b1-3e398cc10f2a/visual-studio-live-slack-chat.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/78f5e1f3-e182-4ee9-92b1-3e398cc10f2a/visual-studio-live-slack-chat.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/78f5e1f3-e182-4ee9-92b1-3e398cc10f2a/visual-studio-live-slack-chat.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/78f5e1f3-e182-4ee9-92b1-3e398cc10f2a/visual-studio-live-slack-chat.png"
			sizes="100vw"
			alt="vs code slack chat extension"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The Slack Chat extension puts Slack inside of your editor ()
		</figcaption>
	
</figure>


<p>Another tool that looks quite interesting is called CodeStream.</p>

<h4 id="codestream">CodeStream</h4>

<p>While VS Live Share looks to improve collaboration from the editor, CodeStream is aiming to solve that same problem from a chat perspective.</p>

<p> allows you to chat directly within VS Code and those chats become part of your code history. You can highlight a chunk of code to discuss and it goes directly into the chat so there is context for your comments. These comments are then saved as part of your Git repo. They also show up in your code as little comment icons, and these comments will show up no matter which branch you are on.</p>

<p>When it comes to VS Live Share, CodeStream offers a complimentary set of features. You can start new sessions directly from the chat pane, as well as by clicking on an avatar. New sessions automatically create a corresponding chat channel that you can persist with the code, or dispose of when you are done.</p>

<figure class="video-container"><iframe data-src="https://www.youtube.com/embed/ObClZLJb8dU" width="600" height="480" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe></figure>

<p>If chatting isn’t enough to get the job done, and you need to collaborate like it’s 1999, help is just a phone call away.</p>

<h3 id="vs-live-share-audio">VS Live Share Audio</h3>

<p>While VS Live Share isn’t trying to reinvent chat, it does re-invent your telephone. Kind of.</p>

<p>With the , you can call someone directly and do voice chat from within VS Code.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c5efc268-b99f-4595-b4da-d647dde3d0d3/visual-studio-live-start-audio.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c5efc268-b99f-4595-b4da-d647dde3d0d3/visual-studio-live-start-audio.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c5efc268-b99f-4595-b4da-d647dde3d0d3/visual-studio-live-start-audio.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c5efc268-b99f-4595-b4da-d647dde3d0d3/visual-studio-live-start-audio.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c5efc268-b99f-4595-b4da-d647dde3d0d3/visual-studio-live-start-audio.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c5efc268-b99f-4595-b4da-d647dde3d0d3/visual-studio-live-start-audio.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c5efc268-b99f-4595-b4da-d647dde3d0d3/visual-studio-live-start-audio.png"
			sizes="100vw"
			alt="vs code command palette showing start audio call option"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Make audio calls from VS Code using the VS Live Share Audio extension ()
		</figcaption>
	
</figure>


<p>The other person will then get a prompt to join your call.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bd39473f-755c-4a9f-9237-e27de71d2324/visual-studio-live-accept-audio-call.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bd39473f-755c-4a9f-9237-e27de71d2324/visual-studio-live-accept-audio-call.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bd39473f-755c-4a9f-9237-e27de71d2324/visual-studio-live-accept-audio-call.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bd39473f-755c-4a9f-9237-e27de71d2324/visual-studio-live-accept-audio-call.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bd39473f-755c-4a9f-9237-e27de71d2324/visual-studio-live-accept-audio-call.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bd39473f-755c-4a9f-9237-e27de71d2324/visual-studio-live-accept-audio-call.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bd39473f-755c-4a9f-9237-e27de71d2324/visual-studio-live-accept-audio-call.png"
			sizes="100vw"
			alt="vs code notification asking if you would like to join the audio call"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			VS Code will ask you if you want to join an audio call that is in process ()
		</figcaption>
	
</figure>


<p>You will see a speaker icon in the bottom status bar when you are connected to a call. You can click on that speaker to change your audio device, mute yourself, or disconnect from the call.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/33fbc411-10ec-4814-aca2-ee60092adf53/visual-studio-live-audio-options.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/33fbc411-10ec-4814-aca2-ee60092adf53/visual-studio-live-audio-options.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/33fbc411-10ec-4814-aca2-ee60092adf53/visual-studio-live-audio-options.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/33fbc411-10ec-4814-aca2-ee60092adf53/visual-studio-live-audio-options.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/33fbc411-10ec-4814-aca2-ee60092adf53/visual-studio-live-audio-options.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/33fbc411-10ec-4814-aca2-ee60092adf53/visual-studio-live-audio-options.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/33fbc411-10ec-4814-aca2-ee60092adf53/visual-studio-live-audio-options.png"
			sizes="100vw"
			alt="vs code options showing options like mute and disconnect for live share audio extension"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			You have full control over audio settings when in a VS Live Share Audio call ()
		</figcaption>
	
</figure>


<p>The last tip I’ll give you is probably the most important, and it’s not a fancy feature or obscure setting you didn’t know existed.</p>

<h3 id="change-your-muscle-memory">Change Your Muscle Memory</h3>

<p>We’ve got years of learned behavior when it comes to getting help or sharing our code. The state of developer collaboration tools has been so bad for so long that we are conditioned to paste code into Slack, start an awkward Skype calls that consist mostly of &ldquo;tell me when you can see my screen&rdquo;, or crowd around a monitor and point excessively, i.e. stock photo style.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/89ba1ae0-3ea0-4774-b68f-b6f63cc11b93/visual-studio-live-stock-photo.jpeg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/89ba1ae0-3ea0-4774-b68f-b6f63cc11b93/visual-studio-live-stock-photo.jpeg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/89ba1ae0-3ea0-4774-b68f-b6f63cc11b93/visual-studio-live-stock-photo.jpeg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/89ba1ae0-3ea0-4774-b68f-b6f63cc11b93/visual-studio-live-stock-photo.jpeg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/89ba1ae0-3ea0-4774-b68f-b6f63cc11b93/visual-studio-live-stock-photo.jpeg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/89ba1ae0-3ea0-4774-b68f-b6f63cc11b93/visual-studio-live-stock-photo.jpeg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/89ba1ae0-3ea0-4774-b68f-b6f63cc11b93/visual-studio-live-stock-photo.jpeg"
			sizes="100vw"
			alt="a group of people pointing at a computer screen"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<p>The most important thing you can do to get the most out of VS Live Share is to actually use VS Live Share. And it will have to be a “conscious” effort.</p>

<p>Your brain is good at patterns. You are constantly recognizing and classifying the world around you based on patterns you have identified, and you are so good at it, you don’t even realize you are doing it. You then develop default responses to these patterns. You form instincts. This is why you will default to the old ways of collaboration without even thinking about what you are doing. Before you know it you will be on a Skype call with someone sharing your screen &mdash; even if you have Live Share installed.</p>

<p>I’ve written a lot about VS Code and people will ask me from time to time how they can get more productive with their editor. I always say the same thing: the next time you reach for the mouse to do something, stop. Can you do that something with the keyboard instead? You probably can. Look up the shortcut and then make yourself use it. At first it’s going to be slower, but if you are willing to deliberately adopt a different behavior, you will be astonished at how fast your brain will default to the more productive way of doing something.</p>

<p>The same goes for Live Share. You will be on a call sharing your screen when it occurs to you that you could be using Live Share. At that moment, stop; click that “Share” button in the bottom of VS Code.</p>

<p>Yes, the person on the other end may not have the extension installed. Yes, it may take a moment to set it up. But if you work on establishing this behavior now, the next time you go to do this, it will “just work” and it won’t be long before you don’t even have to think about it, and at that point, you will finally have achieved that “Anonymous Hippo” level of collaboration.</p>

<h4 id="more-resources">More Resources</h4>

<ul>
<li></li>
<li></li>
<li></li>
<li></li>
</ul>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(rb, ra, il)</span>
</div>


              </article>
            </body>
          </html>
---------------
<h1 id="#title_2" >3、文章： C# 8中的Async Streams</h1>
Bassam Alugili
[http://www.infoq.com/cn/articles/Async-Streams?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/Async-Streams?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/Async-Streams/zh/smallimage/csharp-8-async-streams-logo-small-1535719363027-1536939295437.jpg"/><p>C# 8中新增了异步流（Async Streams），允许异步方法返回多个值。Bassam Alugili将在这篇文章中详细介绍这一特性。</p> <i>By Bassam Alugili</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_3" >4、文章： Spark、Flink、CarbonData技术实践最佳案例解析</h1>
杨雷
[http://www.infoq.com/cn/articles/spark-flink-carbondata-best-practice?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/spark-flink-carbondata-best-practice?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/spark-flink-carbondata-best-practice/zh/smallimage/logo1-1537374373052.jpg"/><p>为帮助开发者更深入的了解这三个大数据开源技术及其实际应用场景，9月8日，InfoQ联合华为云举办了一场实时大数据Meetup，集结了来自Databricks、华为及美团点评的大咖级嘉宾前来分享。本文整理了其中的部分精彩内容，同时，作为本次活动的承办方，InfoQ整理上传了所有讲师的演讲PPT，感兴趣的同学可以下载讲师PPT获取完整资料 。</p> <i>By 杨雷</i>
---------------
<h1 id="#title_4" >5、文章： GitHub：我们为什么会弃用jQuery？</h1>
GitHub前端工程团队
[http://www.infoq.com/cn/articles/removing-jquery-from-github-frontend?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/removing-jquery-from-github-frontend?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/removing-jquery-from-github-frontend/zh/smallimage/envoy-service-mesh-cascading-failure-logo-1533332002940-1537009369311.jpeg"/><p>我们最近完成了一个里程碑，将jQuery完全从GitHub.com的前端代码中移除。这标志着我们数年来逐步移除jQuery这个渐进式的过程终于结束了，我们现在已经完全移除了这个库。这篇文章将介绍我们是如何依赖上jQuery的，以及后来我们意识到不再需要它，到最后我们并没有使用另一个库或框架取代它，而是使用标准的浏览器API实现了我们所需要的一切。</p> <i>By GitHub前端工程团队</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_5" >6、从iPhone XS看手机业下一个十年，要“走芯”了</h1>
胡骁杰
[http://www.infoq.com/cn/news/2018/09/iphonexs-chip?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/09/iphonexs-chip?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>作为行业从业者，我们必须把对于AI芯片的关注度提到足够高。</p> <i>By 胡骁杰</i>
---------------
<h1 id="#title_6" >7、如何实现弹性架构</h1>
Jan Stenberg
[http://www.infoq.com/cn/news/2018/09/resilient-architectures-patterns?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/09/resilient-architectures-patterns?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>为了管理大规模的系统，你必须把系统推向强度极限，但仍然有能力在故障中恢复，并且拥抱失败，Adrian Hornsby 写了两篇博客，分享了自己在大规模系统工作中十多年的经验，以及他发现的有用的模式。</p> <i>By Jan Stenberg</i> <i> Translated by 冬雨</i>
---------------
<h1 id="#title_7" >8、腾讯开源ML-Images，超越谷歌成业内最大多标签图像数据集</h1>
腾讯AI Lab
[http://www.infoq.com/cn/news/2018/09/Tecent-open-source-ML-Image?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/09/Tecent-open-source-ML-Image?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>2018 年 9 月 10 日，腾讯 AI Lab 宣布将于 9 月底开源“Tencent ML-Images”项目，该项目由多标签图像数据集 ML-Images，以及业内目前同类深度学习模型中精度最高的深度残差网络 ResNet-101 构成。AI 前线记者专门采访了腾讯 AI Lab ML-Images 团队，为各位读者带来该项目的第一手深度解读。</p> <i>By 腾讯AI Lab</i>
---------------
<h1 id="#title_8" >9、Microsoft向高性能计算市场推出了新的Azure产品</h1>
Steef-Jan Wiggers
[http://www.infoq.com/cn/news/2018/09/azure-hpc-nvidia-gpu-cyclecloud?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/09/azure-hpc-nvidia-gpu-cyclecloud?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>微软宣布Azure CycleCloud正式可用，这标志着微软进入了高性能计算（HPC）市场。Azure CycleCloud是一种用于创建、管理、运维和优化Azure中任何规模HPC集群的工具，它适用于作为IT企业的Azure用户，支持他们为自身的客户创建安全且灵活的云高性能计算和大型计算（Big Compute）环境。此外，微软还宣布了对NGC（NVIDIA GPU Cloud）的支持。</p> <i>By Steef-Jan Wiggers</i> <i> Translated by 盖磊</i>
---------------
<h1 id="#title_9" >10、敏捷世界中的合规性</h1>
Ben Linders
[http://www.infoq.com/cn/news/2018/09/compliance-agile?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/09/compliance-agile?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>合规性（Compliance）是指确保人们正确地做事，并能够证明做事的正确性。在实施敏捷和频繁交付的情况下，人们需要为交付过程建立合规性。融入了合规性义务（Compliance Obligation）的DevOps团队将更有可能取得成功。</p> <i>By Ben Linders</i> <i> Translated by 盖磊</i>
---------------
<h1 id="#title_10" >11、Stack Overflow最新薪资计算器出炉：DevOps和Go语言开发者是大赢家</h1>
Sarah Schlothauer
[http://www.infoq.com/cn/news/2018/09/survey-top-paying-technologies?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/09/survey-top-paying-technologies?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Stack Overflow 2018年最新的薪资计算器正式出炉。最新的计算器除了增加新的国家和地区之外，还更新了数字数据。为了让薪资更上一层楼，你应该关注哪些技术？这取决于你是愿意冒一些风险还是只想待在安全区域。</p> <i>By Sarah Schlothauer</i> <i> Translated by 无明</i>
---------------