## 文章索引
1、 <a href="#1saving-grandmas-recipes-with-xamarinforms" >Saving Grandma’s Recipes With Xamarin.Forms</a><br/>
2、 <a href="#2文章-java-10-var关键字详解和示例教程" >文章： Java 10 var关键字详解和示例教程</a><br/>
3、 <a href="#3文章-fair重磅发布大规模语料库xnli支持15种语言解决跨语言理解难题" >文章： FAIR重磅发布大规模语料库XNLI：支持15种语言，解决跨语言理解难题</a><br/>
4、 <a href="#4文章-日志的5个级别" >文章： 日志的5个级别</a><br/>
5、 <a href="#5持续交付会如何影响测试" >持续交付会如何影响测试</a><br/>
6、 <a href="#6typescript-31增加可映射元组和数组类型" >TypeScript 3.1增加可映射元组和数组类型</a><br/>
7、 <a href="#7谷歌发布任务队列服务cloud-tasks" >谷歌发布任务队列服务Cloud Tasks</a><br/>
8、 <a href="#8可读性代码为什么怎样以及什么时候" >可读性代码：为什么、怎样以及什么时候</a><br/>
9、 <a href="#9机器人操作系统来到windows" >机器人操作系统来到Windows</a><br/><h1 id="#title_0" >1、Saving Grandma’s Recipes With Xamarin.Forms</h1>
Matthew Soucoup
[https://www.smashingmagazine.com/2018/10/android-ios-mobile-apps-xamarin-forms/](https://www.smashingmagazine.com/2018/10/android-ios-mobile-apps-xamarin-forms/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/10/android-ios-mobile-apps-xamarin-forms/" />
              <title>Saving Grandma’s Recipes With Xamarin.Forms</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>Saving Grandma’s Recipes With Xamarin.Forms</h1>
                  
                    
                    <address>Matthew Soucoup</address>
                  
                  <time datetime="2018-10-11T14:10:38&#43;02:00" class="op-published">2018-10-11T14:10:38+02:00</time>
                  <time datetime="2018-10-11T12:19:46&#43;00:00" class="op-modified">2018-10-11T12:19:46+00:00</time>
                </header>
                

<p>My grandma makes the best, most fluffiest, go weak-in-your-knees buns that anybody has ever tasted. The problem is, there’s a ton of secret ingredients (and I’m not just talking love) that go into those buns, and those ingredients and directions are all stored in my grandma’s head.</p>

<p>We all have family recipes like that, and instead of possibly forgetting them, in this article we’re going to create a mobile app for iOS and Android using  that will save them for myself and future generations of my family!</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/753f8c56-98b2-4494-a6b8-4a61a8769785/1-buns.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/753f8c56-98b2-4494-a6b8-4a61a8769785/1-buns.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/753f8c56-98b2-4494-a6b8-4a61a8769785/1-buns.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/753f8c56-98b2-4494-a6b8-4a61a8769785/1-buns.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/753f8c56-98b2-4494-a6b8-4a61a8769785/1-buns.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/753f8c56-98b2-4494-a6b8-4a61a8769785/1-buns.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/753f8c56-98b2-4494-a6b8-4a61a8769785/1-buns.png"
			sizes="100vw"
			alt="Drawing of buns with steam rising"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Delicious warm buns ()
		</figcaption>
	
</figure>


<p>So if you’re interested in writing mobile applications, but don’t have the time to write the same app over and over again for each platform, this article is for you! Don’t worry if you don’t know C# from a Strawberry Pretzel Salad; I’ve been writing Xamarin apps for over 8 years, and this article is a tour through Xamarin.Forms that intends to give you enough information to start learning on your own.</p>

<h3 id="what-is-this-xamarin-stuff">What Is This Xamarin Stuff?</h3>

<p>More than just a fun word to say,  applications using the exact same SDKs and UI controls available as in Swift and XCode for iOS or Java and Android Studio for Android.</p>



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














<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d00d2cf5-fcc2-45dc-8a63-710ee4403ed5/2-deciding.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d00d2cf5-fcc2-45dc-8a63-710ee4403ed5/2-deciding.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d00d2cf5-fcc2-45dc-8a63-710ee4403ed5/2-deciding.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d00d2cf5-fcc2-45dc-8a63-710ee4403ed5/2-deciding.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d00d2cf5-fcc2-45dc-8a63-710ee4403ed5/2-deciding.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d00d2cf5-fcc2-45dc-8a63-710ee4403ed5/2-deciding.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d00d2cf5-fcc2-45dc-8a63-710ee4403ed5/2-deciding.png"
			sizes="100vw"
			alt="Drawing of stick figure wondering if they should develop for iOS or Android"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Which platform should I develop for? ()
		</figcaption>
	
</figure>


<p>The difference is that the apps are developed with . The apps that result, however, are exactly the same. They look, feel, and behave just like native apps written in Objective-C, Swift, or Java.</p>

<p>Xamarin shines when it comes to . A developer can create and tailor their UI for each platform using native controls and SDKs, but then write a library of shared app logic that’s shared across platforms.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/63ab6fc8-d345-4950-a1bc-21d45c8aee2f/3-xamarin-idea.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/63ab6fc8-d345-4950-a1bc-21d45c8aee2f/3-xamarin-idea.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/63ab6fc8-d345-4950-a1bc-21d45c8aee2f/3-xamarin-idea.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/63ab6fc8-d345-4950-a1bc-21d45c8aee2f/3-xamarin-idea.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/63ab6fc8-d345-4950-a1bc-21d45c8aee2f/3-xamarin-idea.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/63ab6fc8-d345-4950-a1bc-21d45c8aee2f/3-xamarin-idea.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/63ab6fc8-d345-4950-a1bc-21d45c8aee2f/3-xamarin-idea.png"
			sizes="70vw"
			alt="Drawing of stick figure with the idea to develop for both platforms at once using Xamarin"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Aha! I’ll pick Xamarin! ()
		</figcaption>
	
</figure>


<p>It’s this code sharing where tremendous time savings can be realized.</p>

<p>And like the delicious buns my grandma bakes, once given the taste of sharing code &mdash; it’s hard not to crave more &mdash; and that’s where Xamarin.Forms comes in.</p>

<h3 id="xamarin-forms">Xamarin.Forms</h3>

<p> development and adds a layer of abstraction to it.</p>

<p>Instead of developing the user interface for iOS and Android separately, Xamarin.Forms introduces a UI toolkit that enables you to write native mobile apps from a single code base.</p>

<p>Think of it this way: You have an app that needs a button. Each platform has the concept of a button. Why should you have to write the user interface a bunch of different times when you know all the user of your app needs to do is tap a button?</p>

<p>That’s one of the problems Xamarin.Forms solves.</p>

<p>It provides a toolkit of the most commonly used  within a Xamarin.Forms app. Also, we can share the application logic between platforms as before.</p>

<p>The code sharing stats for apps developed with Xamarin.Forms can be off the charts. A conference organizing app has 93% of its code shared on iOS and 91% on Android. The app is open sourced. .</p>

<p>Xamarin.Forms provides more than UI controls. It also contains a , plus others.</p>

<p>But today, we’re going to focus on the UI capabilities for building our recipe manager app.</p>

<h3 id="the-app-we-ll-build">The App We’ll Build</h3>

<p>The recipe manager app will have a straightforward user interface. We will be working in the kitchen, so it needs to be easy to use!</p>

<p><strong>It will consist of 3 screens</strong>. The first will show a list of all the recipes currently loaded in the app.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/70642fb2-30dc-48bd-9003-48677e85e711/recipe-list-ios-large.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/70642fb2-30dc-48bd-9003-48677e85e711/recipe-list-ios-large.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/70642fb2-30dc-48bd-9003-48677e85e711/recipe-list-ios-large.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/70642fb2-30dc-48bd-9003-48677e85e711/recipe-list-ios-large.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/70642fb2-30dc-48bd-9003-48677e85e711/recipe-list-ios-large.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/70642fb2-30dc-48bd-9003-48677e85e711/recipe-list-ios-large.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/70642fb2-30dc-48bd-9003-48677e85e711/recipe-list-ios-large.png"
			sizes="70vw"
			alt="Screenshot of the recipe list screen on iOS"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			 ()
		</figcaption>
	
</figure>


<p>Then, by tapping on one of those recipes, you’ll be able to see its details on a second screen:</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/79ab7e3c-9dde-42ce-8c5b-b7840ad7120c/recipe-detail-ios-large.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/79ab7e3c-9dde-42ce-8c5b-b7840ad7120c/recipe-detail-ios-large.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/79ab7e3c-9dde-42ce-8c5b-b7840ad7120c/recipe-detail-ios-large.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/79ab7e3c-9dde-42ce-8c5b-b7840ad7120c/recipe-detail-ios-large.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/79ab7e3c-9dde-42ce-8c5b-b7840ad7120c/recipe-detail-ios-large.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/79ab7e3c-9dde-42ce-8c5b-b7840ad7120c/recipe-detail-ios-large.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/79ab7e3c-9dde-42ce-8c5b-b7840ad7120c/recipe-detail-ios-large.png"
			sizes="70vw"
			alt="Screenshot of the recipe detail screen on iOS"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The recipe detail screen on iOS ()
		</figcaption>
	
</figure>


<p>From there you can tap an edit button to make changes to the recipe on the third screen:</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2c28639a-1f12-415c-8d0e-cc1c77f6b636/recipe-edit-ios-large.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2c28639a-1f12-415c-8d0e-cc1c77f6b636/recipe-edit-ios-large.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2c28639a-1f12-415c-8d0e-cc1c77f6b636/recipe-edit-ios-large.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2c28639a-1f12-415c-8d0e-cc1c77f6b636/recipe-edit-ios-large.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2c28639a-1f12-415c-8d0e-cc1c77f6b636/recipe-edit-ios-large.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2c28639a-1f12-415c-8d0e-cc1c77f6b636/recipe-edit-ios-large.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2c28639a-1f12-415c-8d0e-cc1c77f6b636/recipe-edit-ios-large.png"
			sizes="70vw"
			alt="Screenshot of the recipe edit screen on iOS"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The recipe edit screen on iOS ()
		</figcaption>
	
</figure>


<p>You can also get to this screen by tapping the add button from the recipe list screen.</p>

<h3 id="the-development-environment">The Development Environment</h3>

<p>Xamarin apps are built with C# and .NET, using Visual Studio on Windows or Visual Studio for Mac on the Mac, but you need to have the  SDKs and tooling installed, too. Getting everything installed, in the correct order could be a bit of an issue, however, the Visual Studio installers will take care of note only getting the IDE installed, but also the platform tooling.</p>

<p>Although a Mac is always required to build iOS apps, with Xamarin you can still develop and debug those apps from ! So if Windows is your jam, there’s no need to change your environments altogether.</p>

<p>Now let’s see how Xamarin.Forms can help us save some family recipes from one code base!</p>

<div class="sponsors__wide-place"></div>




<h3 id="recipe-list-page-laying-out-the-ui">Recipe List Page: Laying Out the UI</h3>

<p>Let’s start with talking about how we’re going to layout the UI for our recipe saving app!</p>

<p>Overall each screen in Xamarin.Forms is comprised of 3 elements. A <code>Page</code>. At least one element called a <code>Layout</code>. And at least one <code>Control</code>.</p>

<p><strong>The Page</strong></p>

<p>The  is the thing that hosts everything displayed on the screen at one time. The <code>Page</code> is also central in navigation within an app.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a756873c-09ef-4613-9eaf-aaf72b77173c/7-page.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a756873c-09ef-4613-9eaf-aaf72b77173c/7-page.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a756873c-09ef-4613-9eaf-aaf72b77173c/7-page.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a756873c-09ef-4613-9eaf-aaf72b77173c/7-page.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a756873c-09ef-4613-9eaf-aaf72b77173c/7-page.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a756873c-09ef-4613-9eaf-aaf72b77173c/7-page.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a756873c-09ef-4613-9eaf-aaf72b77173c/7-page.png"
			sizes="100vw"
			alt="Drawing representing a Page in Xamarin.Forms"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The page ()
		</figcaption>
	
</figure>


<p>We tell Xamarin.Forms which <code>Page</code> to display via a . That service then will take care of displaying whatever page in a way that’s appropriate and native for the operating system.</p>

<p>In other words, the code to navigate between screens has been abstracted too!</p>

<p>Finally, although not the only way to do it, I code the UI of my <code>Page</code>’s in . (The other way would be to use C#.) XAML is a markup language that describes how a page looks. And for now, suffice it to say, it’s kinda sorta similar to HTML.</p>

<p><strong>The Layout</strong></p>

<p>All the controls on a page are arranged by something called a .</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3e5cc3b2-c16e-4e32-bafb-49cabd80e8d4/8-layouts.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3e5cc3b2-c16e-4e32-bafb-49cabd80e8d4/8-layouts.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3e5cc3b2-c16e-4e32-bafb-49cabd80e8d4/8-layouts.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3e5cc3b2-c16e-4e32-bafb-49cabd80e8d4/8-layouts.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3e5cc3b2-c16e-4e32-bafb-49cabd80e8d4/8-layouts.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3e5cc3b2-c16e-4e32-bafb-49cabd80e8d4/8-layouts.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3e5cc3b2-c16e-4e32-bafb-49cabd80e8d4/8-layouts.png"
			sizes="100vw"
			alt="Drawing representing some layouts in Xamarin.Forms"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The layouts ()
		</figcaption>
	
</figure>


<p>One or more layouts can be added to a page.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f506231c-1bb1-4797-9710-1f3bc03d0e23/9-layouts-on-board.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f506231c-1bb1-4797-9710-1f3bc03d0e23/9-layouts-on-board.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f506231c-1bb1-4797-9710-1f3bc03d0e23/9-layouts-on-board.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f506231c-1bb1-4797-9710-1f3bc03d0e23/9-layouts-on-board.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f506231c-1bb1-4797-9710-1f3bc03d0e23/9-layouts-on-board.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f506231c-1bb1-4797-9710-1f3bc03d0e23/9-layouts-on-board.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f506231c-1bb1-4797-9710-1f3bc03d0e23/9-layouts-on-board.png"
			sizes="100vw"
			alt="Drawing of how the layouts interact with the page"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Layouts on the page ()
		</figcaption>
	
</figure>


<p>There are several different types of Layouts in Forms. Some of the most common ones include Stack, Absolute, Relative, Grid, Scroll, and Flex layouts.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/96baf003-56ff-4947-9d3d-744e427a7eda/10-all-layouts.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/96baf003-56ff-4947-9d3d-744e427a7eda/10-all-layouts.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/96baf003-56ff-4947-9d3d-744e427a7eda/10-all-layouts.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/96baf003-56ff-4947-9d3d-744e427a7eda/10-all-layouts.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/96baf003-56ff-4947-9d3d-744e427a7eda/10-all-layouts.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/96baf003-56ff-4947-9d3d-744e427a7eda/10-all-layouts.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/96baf003-56ff-4947-9d3d-744e427a7eda/10-all-layouts.png"
			sizes="100vw"
			alt="Drawing of several Xamarin.Forms layouts and how they arrange their child elements."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Common Xamarin.Forms layouts ()
		</figcaption>
	
</figure>


<p><strong>The Controls</strong></p>

<p>Then finally there are the . These are the widgets of your app that the user interacts with.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ce45880a-f33f-41fd-b137-a0e8d9eedf8a/11-controls.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ce45880a-f33f-41fd-b137-a0e8d9eedf8a/11-controls.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ce45880a-f33f-41fd-b137-a0e8d9eedf8a/11-controls.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ce45880a-f33f-41fd-b137-a0e8d9eedf8a/11-controls.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ce45880a-f33f-41fd-b137-a0e8d9eedf8a/11-controls.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ce45880a-f33f-41fd-b137-a0e8d9eedf8a/11-controls.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ce45880a-f33f-41fd-b137-a0e8d9eedf8a/11-controls.png"
			sizes="100vw"
			alt="Drawing of a couple of Xamarin.Forms controls, each drawn as a box"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Some of the controls ()
		</figcaption>
	
</figure>


<p>Forms come with many controls that will be used no matter what type of app you’re building. Things like labels, buttons, entry boxes, images, and of course, list views.</p>

<p>When adding a control to a screen, you add it to a layout. It’s the layout that takes care of figuring where exactly on the screen the control should appear.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7cd6221f-ce4b-4e2d-b8ef-f3b044b81801/12-all-done.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7cd6221f-ce4b-4e2d-b8ef-f3b044b81801/12-all-done.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7cd6221f-ce4b-4e2d-b8ef-f3b044b81801/12-all-done.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7cd6221f-ce4b-4e2d-b8ef-f3b044b81801/12-all-done.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7cd6221f-ce4b-4e2d-b8ef-f3b044b81801/12-all-done.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7cd6221f-ce4b-4e2d-b8ef-f3b044b81801/12-all-done.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7cd6221f-ce4b-4e2d-b8ef-f3b044b81801/12-all-done.png"
			sizes="100vw"
			alt="Drawing of a page holding 2 layouts, and those layouts arranging the controls according to the layout type."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Everything fits together! ()
		</figcaption>
	
</figure>


<p>So to generate the following screens on iOS and Android respectively:</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/38733a99-1dd4-46b6-ad25-edfdccb41d8c/example-recipe-list-ios-android.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/38733a99-1dd4-46b6-ad25-edfdccb41d8c/example-recipe-list-ios-android.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/38733a99-1dd4-46b6-ad25-edfdccb41d8c/example-recipe-list-ios-android.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/38733a99-1dd4-46b6-ad25-edfdccb41d8c/example-recipe-list-ios-android.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/38733a99-1dd4-46b6-ad25-edfdccb41d8c/example-recipe-list-ios-android.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/38733a99-1dd4-46b6-ad25-edfdccb41d8c/example-recipe-list-ios-android.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/38733a99-1dd4-46b6-ad25-edfdccb41d8c/example-recipe-list-ios-android.png"
			sizes="100vw"
			alt="Screenshot of recipe list screen on iOS and Android"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Recipe lists on iOS (left) and Android (right) ()
		</figcaption>
	
</figure>


<p>I used this XAML:</p>

<pre class="break-out"><code class="language-xml">&lt;?xml version="1.0" encoding="UTF-8"?&gt;
&lt;ContentPage xmlns="http://xamarin.com/schemas/2014/forms" 
             xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml" 
             x:Class="SmashingRecipe.RecipeListPage"
             Title="Recipes"&gt;
    &lt;ContentPage.Content&gt;
        &lt;StackLayout&gt;
            &lt;ListView x:Name="recipesList"&gt;
                &lt;ListView.ItemTemplate&gt;
                    &lt;DataTemplate&gt;
                        &lt;TextCell Text="{Binding Name}"/&gt;
                    &lt;/DataTemplate&gt;
                &lt;/ListView.ItemTemplate&gt;
            &lt;/ListView&gt;
        &lt;/StackLayout&gt;
    &lt;/ContentPage.Content&gt;
    &lt;ContentPage.ToolbarItems&gt;
        &lt;ToolbarItem Text="Add" /&gt;
    &lt;/ContentPage.ToolbarItems&gt;
&lt;/ContentPage&gt;
</code></pre>

<p>There’s a couple of important things going on here.</p>

<p>The first is the <code>&lt;StackLayout&gt;</code>. This is telling Forms to arrange all the controls that follow in a stack.</p>

<p>There happens to only be a single control in the layout, and that’s a <code>&lt;ListView&gt;</code>, and we’re going to give it a name so we can reference it later.</p>

<p>Then there’s a little bit of boilerplate ceremony to the <code>ListView</code> before we get to what we’re after: the <code>&lt;TextCell&gt;</code>. This is telling Forms to display simple text in each cell of the list.</p>

<p>We tell the <code>&lt;TextCell&gt;</code> the text we want it to display through a technique called <strong>Data Binding</strong>. The syntax looks like <code>Text=&quot;{Binding Name}&quot;</code>. Where <code>Name</code> is a property of a <code>Recipe</code> class that models… well, Recipes.</p>

<p>So how do the recipes get added to the list?</p>

<p>Along with every XAML file, there is a “code-behind” file. This code-behind allows us to do things like handle user interaction events, or perform setup, or do other app logic.</p>

<p>There’s a function that can be overridden in every <code>Page</code> called <code>OnAppearing</code> &mdash; which as I’m sure you guessed &mdash; gets called when the <code>Page</code> appears.</p>

<pre><code class="language-css">protected override void OnAppearing()
{
    base.OnAppearing();

    recipesList.ItemsSource = null;
    recipesList.ItemsSource = App.AllRecipes;    
}
</code></pre>

<p>Notice the <code>recipesList.ItemsSource = AllRecipes;</code></p>

<p>This is telling the <code>ListView</code> &mdash; “Hey! All of your data is found in the enumerable <code>App.AllRecipes</code> (an application-wide variable) and you can use any of its child object’s properties to bind off of!”.</p>

<p>A list of recipes is all well and fine &mdash; but you can’t bake anything without first seeing the recipe’s details &mdash; and we’re going to take care of that next.</p>

<div class="sponsors__wide-place"></div>




<h3 id="event-handling">Event Handling</h3>

<p>Without responding to user touches our app is nothing more than a list of delicious sounding recipes. They sound good, but without knowing how to cook them, it’s not of much use!</p>

<p>Let’s make each cell in the  <code>ListView</code> respond to taps so we can see how to make the recipe!</p>

<p>In the <code>RecipeListPage</code> code-behind file, we can add <em>event handlers</em> to controls to listen and react to user interaction events.</p>

<p>Handling tap events on the list view then:</p>

<pre class="break-out"><code class="language-css">recipesList.ItemSelected += async (sender, eventArgs) =>
{
    if (eventArgs.SelectedItem != null)
    {
        var detailPage = new RecipeDetailPage(eventArgs.SelectedItem as Recipe);

        await Navigation.PushAsync(detailPage);

        recipesList.SelectedItem = null;
    }
};
</code></pre>

<p>There’s some neat stuff going on there.</p>

<p>Whenever somebody selects a row, <code>ItemSelected</code> is fired on the <code>ListView</code>.</p>

<p>Of the arguments that get passed into the handler, the <code>eventArgs</code> object has a <code>SelectedItem</code> property that happens to be whatever is bound to the <code>ListView</code> from before.</p>

<p>In our case, that’s the <code>Recipe</code> class.  (So we don’t have to search for the object in the master source - it gets passed to us.)</p>

<h3 id="recipe-detail-page">Recipe Detail Page</h3>

<p>Of course, there’s a page that shows us the secret ingredients and directions of how to make each recipe, but how does that page get displayed?</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4b81b004-6262-49e3-95c3-441f1d393d21/14-baker.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4b81b004-6262-49e3-95c3-441f1d393d21/14-baker.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4b81b004-6262-49e3-95c3-441f1d393d21/14-baker.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4b81b004-6262-49e3-95c3-441f1d393d21/14-baker.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4b81b004-6262-49e3-95c3-441f1d393d21/14-baker.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4b81b004-6262-49e3-95c3-441f1d393d21/14-baker.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4b81b004-6262-49e3-95c3-441f1d393d21/14-baker.png"
			sizes="100vw"
			alt="Drawing of a stick figure dressed as a chef who is ready to start baking."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Let’s get cooking! ()
		</figcaption>
	
</figure>


<p>Notice the <code>await Navigation.PushAsync(detailPage);</code> line from above. The <code>Navigation</code> object is a platform-independent object that handles page transitions in a native fashion for each platform.</p>

<p>Now let’s take a peek at the recipe details page:</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/11a9684d-1ea7-4ce2-927c-94fdac68f18f/15a-example-recipe-detail-ios-android.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/11a9684d-1ea7-4ce2-927c-94fdac68f18f/15a-example-recipe-detail-ios-android.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/11a9684d-1ea7-4ce2-927c-94fdac68f18f/15a-example-recipe-detail-ios-android.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/11a9684d-1ea7-4ce2-927c-94fdac68f18f/15a-example-recipe-detail-ios-android.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/11a9684d-1ea7-4ce2-927c-94fdac68f18f/15a-example-recipe-detail-ios-android.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/11a9684d-1ea7-4ce2-927c-94fdac68f18f/15a-example-recipe-detail-ios-android.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/11a9684d-1ea7-4ce2-927c-94fdac68f18f/15a-example-recipe-detail-ios-android.png"
			sizes="100vw"
			alt="Screenshot of recipe detail screen on iOS and Android"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Recipe detail screens on iOS (left) and Android (right) ()
		</figcaption>
	
</figure>


<p>This page is built with XAML as well. However, the <code>Layout</code> used () is quite cool as it’s inspired by the CSS Flexbox.</p>

<pre class="break-out"><code class="language-xml">&lt;ContentPage.Content&gt;
    &lt;ScrollView&gt;
        &lt;FlexLayout
            AlignItems="Start"
            AlignContent="Start"
            Wrap="Wrap"&gt;

            &lt;Image Source="buns.png" FlexLayout.Basis="100%" /&gt;

            &lt;Label Text="{Binding Name}" HorizontalTextAlignment="Center" TextColor="#01487E"
                   FontAttributes="Bold" FontSize="Large" Margin="10, 10" /&gt;
                   
            &lt;BoxView FlexLayout.Basis="100%" HeightRequest="0" /&gt;

            &lt;Label Text="Ingredients" FontAttributes="Bold" FontSize="Medium" TextColor="#EE3F60"
                   Margin="10,10" HorizontalOptions="FillAndExpand" /&gt;
            &lt;BoxView FlexLayout.Basis="100%" HeightRequest="0" /&gt;
            &lt;Label Text="{Binding Ingredients}" Margin="10,10" FontSize="Small" /&gt;

            &lt;BoxView FlexLayout.Basis="100%" HeightRequest="0" /&gt;
            
            &lt;Label Text="Directions" FontAttributes="Bold" FontSize="Medium" TextColor="#EE3F60" 
                   Margin="10,10" HorizontalOptions="FillAndExpand" /&gt;
            &lt;BoxView FlexLayout.Basis="100%" HeightRequest="0" /&gt;
            &lt;Label Text="{Binding Directions}" Margin="10,10" FontSize="Small" /&gt;

        &lt;/FlexLayout&gt;
    &lt;/ScrollView&gt;
&lt;/ContentPage.Content&gt;
</code></pre>

<p>The <code>FlexLayout</code> will arrange its controls in either rows or columns. The big benefit comes though with the fact that it can automatically detect how much room there is left on the screen to place a control, and if there’s not enough, then it can automatically create a new row or column to accommodate it!</p>

<p>This helps greatly when dealing with various screen sizes, which there are plenty of in mobile development.</p>

<p>Well, with the <code>FlexLayout</code> helping us keep the details screen looking good, we still need to edit those recipes, right?</p>

<p>You probably noticed this:</p>

<pre><code class="language-xml">&lt;ToolbarItem Text="Edit" Clicked="Edit_Clicked" /></code></pre>

<p>That line is responsible for putting a button in the app’s toolbar. The <code>Clicked=&quot;Edit_Clicked&quot;</code> tells the button that when it’s clicked, look in the code behind for a function of that name, and then execute its code.</p>

<p>Which in this case, would be instantiating the Recipe Edit Page, and pushing that onto our navigation stack using the <code>Navigation</code> object mentioned previously.</p>

<h3 id="recipe-edit-page">Recipe Edit Page</h3>

<p>A page with a list of recipes: check! A page with all the details to make the recipes: check! All that’s now left is to create the page that we use to enter or change a recipe while we watch grandma work her magic!</p>

<p>First, check out the screens:</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a2640997-c5e0-4f92-973b-66f122f7a7d9/example-recipe-edit-ios-android.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a2640997-c5e0-4f92-973b-66f122f7a7d9/example-recipe-edit-ios-android.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a2640997-c5e0-4f92-973b-66f122f7a7d9/example-recipe-edit-ios-android.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a2640997-c5e0-4f92-973b-66f122f7a7d9/example-recipe-edit-ios-android.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a2640997-c5e0-4f92-973b-66f122f7a7d9/example-recipe-edit-ios-android.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a2640997-c5e0-4f92-973b-66f122f7a7d9/example-recipe-edit-ios-android.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a2640997-c5e0-4f92-973b-66f122f7a7d9/example-recipe-edit-ios-android.png"
			sizes="100vw"
			alt="Screenshot of recipe edit screen on iOS and Android"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Recipe edit screens on iOS (left) and Android (right) ()
		</figcaption>
	
</figure>


<p>And now the code:</p>

<pre class="break-out"><code class="language-xml">&lt;ContentPage.Content&gt;
    &lt;Grid&gt;
        &lt;Grid.RowDefinitions&gt;
            &lt;RowDefinition Height="*" /&gt;
            &lt;RowDefinition Height="Auto" /&gt;
        &lt;/Grid.RowDefinitions&gt;
        &lt;Grid.ColumnDefinitions&gt;
            &lt;ColumnDefinition Width="*" /&gt;
            &lt;ColumnDefinition Width="*" /&gt;
        &lt;/Grid.ColumnDefinitions&gt;

        &lt;TableView Grid.Row="0" Grid.Column="0" Grid.ColumnSpan="2" 
                   Intent="Form" HasUnevenRows="true"&gt;
            &lt;TableSection Title="General"&gt;
                &lt;EntryCell x:Name="recipeNameCell" Label="Name" /&gt; 
            &lt;/TableSection&gt;
            
            &lt;TableSection Title="Ingredients"&gt;
                &lt;ViewCell&gt;
                    &lt;StackLayout Padding="15"&gt;
                        &lt;Editor x:Name="ingredientsCell" /&gt;
                    &lt;/StackLayout&gt;
                &lt;/ViewCell&gt;
            &lt;/TableSection&gt;
            
            &lt;TableSection Title="Directions"&gt;
                &lt;ViewCell&gt;
                    &lt;StackLayout Padding="15"&gt;
                        &lt;Editor x:Name="directionsCell" /&gt;
                    &lt;/StackLayout&gt;
                &lt;/ViewCell&gt;
            &lt;/TableSection&gt;
        &lt;/TableView&gt;

        &lt;Button Text="Save" Grid.Row="1" Grid.Column="0" BackgroundColor="#EE3F60" TextColor="White" x:Name="saveButton" /&gt;
        &lt;Button Text="Cancel" Grid.Row="1" Grid.Column="1" BackgroundColor="#4CC7F2" TextColor="White" x:Name="cancelButton" /&gt;
    &lt;/Grid&gt;
&lt;/ContentPage.Content&gt;
</code></pre>

<p>There’s a little more code here, and that’s because I’m using the <code>Grid</code> layout to specify how everything should lay out in a 2-Dimensional pattern.</p>

<p>And also notice no data binding here. Because I wanted to give an example of how one would populate the controls purely from the code behind file:</p>

<pre><code class="language-css">void InitializePage()
{
    Title = TheRecipe.Name ?? "New Recipe";

    recipeNameCell.Text = TheRecipe.Name;
    ingredientsCell.Text = TheRecipe.Ingredients;
    directionsCell.Text = TheRecipe.Directions;

    saveButton.Clicked += async (sender, args) =>
    {
        SaveRecipe();
        await CloseWindow();
    };

    cancelButton.Clicked += async (sender, args) =>
    {
        await CloseWindow();
    };
}
</code></pre>

<p>See that <code>TheRecipe</code> property? It’s page level, holds all the data for a particular recipe, and gets set in the constructor of the page.</p>

<p>Secondly, the <code>Clicked</code> event handlers for the <code>saveButton</code> and <code>cancelButton</code> are totally .NET-ified (and yes, I do make my own words up quite often.)</p>

<p>I say they’re .NET-ified because the syntax to handle that event is not native to Java nor Objective-C. When the app runs on Android or iOS, the behavior will be exactly like an Android Click or an iOS TouchUpInside.</p>

<p>And as you can see, each of those click event handlers are invoking appropriate functions that either save the recipe and dismiss the page, or only dismiss the page.</p>

<p>There it is &mdash; we have the UI down to save the recipes from now until the end of time!</p>

<h3 id="css-wha-or-making-the-app-pretty">CSS Wha?!? Or Making The App Pretty</h3>

<p>Saving the best for last: Xamarin.Forms 3.0 gives us &mdash; among other things &mdash; the ability to style controls using !</p>

<p>The Xamarin.Forms CSS isn’t 100% what you may be used to from web development. But it’s close enough that anyone familiar with CSS will feel right at home. Just like me at grandma’s!</p>

<p>So let’s take the Recipe Details page and refactor it, so it uses Cascading Style Sheets to set the visual elements instead of setting everything directly inline in the XAML.</p>

<p>First step is to create the CSS doc! In this case it will look like the following:</p>

<pre><code class="language-css">.flexContent {
    align-items: flex-start;
    align-content: flex-start;
    flex-wrap: wrap;
}

image {
    flex-basis: 100%;
}

.spacer {
    flex-basis: 100%;
    height: 0;
}

.foodHeader {
    font-size: large;
    font-weight: bold;
    color: #01487E;
    margin: 10 10;
}

.dataLabel {
    font-size: medium;
    font-weight: bold;
    color: #EE3F60;
    margin: 10 10;
}

.data {
    font-size: small;
    margin: 10 10;
}
</code></pre>

<p>For the most part, it looks like CSS. There are classes in there. There is a single selector for a class type, <code>Image</code>. And then a bunch of property setters.</p>

<p>Some of those property setters, such as <code>flex-wrap</code> or <code>flex-basis</code> are specific to Xamarin.Forms. Going forward, the team will prefix those with <code>xf-</code> to follow standard practices.</p>

<p>Next up will be to apply it to XAML controls.</p>

<pre class="break-out"><code class="language-xml">&lt;ContentPage.Resources&gt;
    &lt;StyleSheet Source="../Styles/RecipeDetailStyle.css" /&gt;
&lt;/ContentPage.Resources&gt;

&lt;ContentPage.Content&gt;
    &lt;ScrollView&gt;
        &lt;FlexLayout StyleClass="flexContent"&gt;

            &lt;Image Source="buns.png" /&gt;

            &lt;Label Text="{Binding Name}" StyleClass="foodHeader" /&gt;
                   
            &lt;BoxView StyleClass="spacer" /&gt;

            &lt;Label Text="Ingredients" StyleClass="dataLabel" HorizontalOptions="FillAndExpand" /&gt;
            &lt;BoxView StyleClass="spacer" /&gt;
            &lt;Label Text="{Binding Ingredients}" StyleClass="data" /&gt;

            &lt;BoxView StyleClass="spacer" /&gt;
            
            &lt;Label Text="Directions" StyleClass="dataLabel" HorizontalOptions="FillAndExpand" /&gt;
            &lt;BoxView StyleClass="spacer" /&gt;
            &lt;Label Text="{Binding Directions}" StyleClass="data" /&gt;

        &lt;/FlexLayout&gt;
    &lt;/ScrollView&gt;
&lt;/ContentPage.Content&gt;
</code></pre>

<p>Here’s what it .</p>

<p>In Xamarin.Forms, to reference the CSS document, add a <code>&lt;StyleSheet Source=&quot;YOUR DOC PATH&quot; /&gt;</code>. Then you can reference the classes in each control via the <code>StyleClass</code> property.</p>

<p>It definitely cleans up the XAML, and it makes the intention of the control clearer too. For example, now it’s pretty obvious what those <code>&lt;BoxView StyleClass=&quot;spacer&quot; /&gt;</code> are up to!</p>

<p>And the <code>Image</code> gets itself styled all because it’s an <code>Image</code> and the way we defined the selector in the CSS.</p>

<p>To be sure, CSS in Xamarin.Forms isn’t as fully implemented as its web cousin, but it’s still pretty cool. You have selectors, classes, can set properties and, of course, that whole cascading thing going on!</p>

<h3 id="summary">Summary</h3>

<p>Three screens, two platforms, one article, and endless recipes saved! And you know what else? You can build apps with Xamarin.Forms for more than Android and iOS. You can build UWP, macOS, and even Samsung Tizen platforms!</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bb497595-adae-465f-978c-42c55520871b/17-buns.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bb497595-adae-465f-978c-42c55520871b/17-buns.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bb497595-adae-465f-978c-42c55520871b/17-buns.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bb497595-adae-465f-978c-42c55520871b/17-buns.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bb497595-adae-465f-978c-42c55520871b/17-buns.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bb497595-adae-465f-978c-42c55520871b/17-buns.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bb497595-adae-465f-978c-42c55520871b/17-buns.png"
			sizes="100vw"
			alt="Drawing of buns with steam rising"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Delicious! ()
		</figcaption>
	
</figure>


<p>Xamarin.Forms is a UI toolkit that allows you to create apps by writing the user interface once and having the UI rendered natively across the major platforms.</p>

<p>It does this by providing an SDK that’s an abstraction to the most commonly used controls across the platforms. In addition to the UI goodness, Xamarin.Forms also provides a full-featured MVVM framework, a pub/sub messaging service, an animation API, and a dependency service.</p>

<p>Xamarin.Forms also gives you all the same code benefits that traditional Xamarin development does. Any application logic is shared across all the platforms. And you get to develop all your apps with a single IDE using a single language &mdash; that’s pretty cool!</p>

<p>Where to next? !</p>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(dm, ra, yk, il)</span>
</div>


              </article>
            </body>
          </html>
---------------
<h1 id="#title_1" >2、文章： Java 10 var关键字详解和示例教程</h1>
Mohamed Taman
[http://www.infoq.com/cn/articles/java-10-var-type?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/java-10-var-type?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/java-10-var-type/zh/smallimage/GettyImages-499691816-copy-1539274818281.jpeg"/><p>在本文中，我将通过示例介绍新的Java SE 10特性——“var”类型。你将学习如何在代码中正确使用它，以及在什么情况下不能使用它。</p> <i>By Mohamed Taman</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_2" >3、文章： FAIR重磅发布大规模语料库XNLI：支持15种语言，解决跨语言理解难题</h1>
盖磊
[http://www.infoq.com/cn/articles/XNLI-evaluating-cross-lingual-sentence-representations?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/XNLI-evaluating-cross-lingual-sentence-representations?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/XNLI-evaluating-cross-lingual-sentence-representations/zh/smallimage/logo-ai-1538909099831.jpeg"/><p>自然语言处理系统依赖于使用基于标注数据的有监督学习提高模型的处理能力。目前，许多模型是使用单一语言训练的，并不能直接应用于其他语言。鉴于收集每种语言的语料数据是不现实的，因此如何实现跨语言句子理解和低资源的跨语言迁移得到了越来越多的关注。XNLI论文进一步将多类型自然语言推理语料库的开发和测试集扩展到15种语言，其中甚至包括斯瓦希里语和乌尔都语等低资源语言，构建了一种用于XLU的基准测试数据集。</p> <i>By 盖磊</i>
---------------
<h1 id="#title_3" >4、文章： 日志的5个级别</h1>
Orhan Kavrakoğlu
[http://www.infoq.com/cn/articles/five-levels-of-logging?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/five-levels-of-logging?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/five-levels-of-logging/zh/smallimage/image_fences-1538911781682.jpg"/><p>作者介绍了重要的几个日志级别。</p> <i>By Orhan Kavrakoğlu</i> <i> Translated by 刘嘉洋</i>
---------------
<h1 id="#title_4" >5、持续交付会如何影响测试</h1>
Ben Linders
[http://www.infoq.com/cn/news/2018/10/continuous-delivery-testing?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/10/continuous-delivery-testing?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>如果要做持续交付，那我们必须关注我们写的代码的质量。不是所有团队都配备专门的测试人员，但如果有测试人员的话，他们会和开发人员紧密合作，编写在单元测试中无法覆盖的少数测试的自动化代码，并帮助开发人员搭建单元测试。</p> <i>By Ben Linders</i> <i> Translated by 刘嘉洋</i>
---------------
<h1 id="#title_5" >6、TypeScript 3.1增加可映射元组和数组类型</h1>
Dylan Schiemann
[http://www.infoq.com/cn/news/2018/10/typescript-mappable-tuple-array?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/10/typescript-mappable-tuple-array?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>TypeScript团队最近发布了TypeScript版本3.1，继3.0版本之后添加了可映射元组和数组类型以及其他一些改进。</p> <i>By Dylan Schiemann</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_6" >7、谷歌发布任务队列服务Cloud Tasks</h1>
Eldert Grootenboer
[http://www.infoq.com/cn/news/2018/10/google-cloud-tasks?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/10/google-cloud-tasks?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>谷歌发布了Cloud Tasks，这是一项针对谷歌云平台App Engine服务的任务队列服务。Cloud Tasks允许从应用程序中异步执行任务，解耦服务并支持长期运行和在后台运行的活动。</p> <i>By Eldert Grootenboer</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_7" >8、可读性代码：为什么、怎样以及什么时候</h1>
Thomas Betts
[http://www.infoq.com/cn/news/2018/10/readable-code?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/10/readable-code?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>大多数人会说“我们想要可读性高的代码”。你甚至发现有些人认为可读性比功能更重要。但是，当要求人们对可读性做出定义时，他们的意见就会出现分歧。Laura Savino在Explore DDD 2018大会上的演讲就是以这个作为前提。她阐述了为什么我们想要可读性高的代码、可读性究竟意味着什么，以及什么时候必须优先考虑可读性。</p> <i>By Thomas Betts</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_8" >9、机器人操作系统来到Windows</h1>
Sergio De Simone
[http://www.infoq.com/cn/news/2018/10/robot-os-coming-to-windows?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/10/robot-os-coming-to-windows?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>机器人操作系统（ROS）是一种用于机器人开发的元操作系统，目前可在Windows 10上使用。微软最初的实验性构建名为ROS1，集成在Visual Studio中，包括ROS Core的完全移植和若干模块。根据微软的说法，ROS on Windows将逐步发展，以至于完全集成基于GPU的机器学习和Azure IoT Hub。</p> <i>By Sergio De Simone</i> <i> Translated by 谢丽</i>
---------------