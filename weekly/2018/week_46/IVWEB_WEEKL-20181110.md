## 文章索引
1、 <a href="#1css-frameworks-or-css-grid:-what-should-i-use-for-my-project" >CSS Frameworks Or CSS Grid: What Should I Use For My Project?</a><br/>
2、 <a href="#2每周分享第-30-期" >每周分享第 30 期</a><br/>
3、 <a href="#3going-beyond-consolelog" >Going beyond console.log()</a><br/><h1 id="#title_0" >1、CSS Frameworks Or CSS Grid: What Should I Use For My Project?</h1>
Rachel Andrew
[https://www.smashingmagazine.com/2018/11/css-frameworks-css-grid/](https://www.smashingmagazine.com/2018/11/css-frameworks-css-grid/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/11/css-frameworks-css-grid/" />
              <title>CSS Frameworks Or CSS Grid: What Should I Use For My Project?</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>CSS Frameworks Or CSS Grid: What Should I Use For My Project?</h1>
                  
                    
                    <address>Rachel Andrew</address>
                  
                  <time datetime="2018-11-09T12:30:30&#43;02:00" class="op-published">2018-11-09T12:30:30+02:00</time>
                  <time datetime="2018-11-09T17:55:33&#43;00:00" class="op-modified">2018-11-09T17:55:33+00:00</time>
                </header>
                

<p>Among the questions I am most frequently asked is some variety of the question, &ldquo;Should I use CSS Grid or Bootstrap?&rdquo; In this article, I will take a look at that question. You will discover that the reasons for using frameworks are varied, and not simply centered around use of the grid system contained in that framework. I hope that by unpacking these reasons, I can help you to make your own decision, in terms of what is best for the sites and applications that you are working on, and also for the team you work with.</p>

<p>In this article when I talk about <strong>a framework</strong>, I’m describing a third party CSS framework such as Bootstrap or Foundation. You might argue these are really component libraries, but many people (including their own docs) would describe them as a framework so that is what we will use here. The important factor is that these are something developed externally to you, without reference to your specific issues. The alternative to using a third party framework is to write your own CSS &mdash; that might involve developing your own internal framework, using a bunch of common files as a starting point, or creating every project as a new thing. All these things are done in reference to your own specific needs rather than very generic ones.</p>

<h3 id="why-choose-a-css-framework">Why Choose A CSS Framework?</h3>

<p>The question of whether to use Grid or a framework is flawed, as CSS Grid is not a drop-in replacement for the things that a CSS framework does. Any exploration of the subject needs to consider what of our framework CSS Grid is going to replace. I wanted to start by finding out why people had chosen to use a CSS framework at all. So I turned to Twitter and posted this tweet.</p>

<p><blockquote class="twitter-tweet" data-lang="en"><p lang="en" dir="ltr">A question: if you have chosen to use a CSS framework (Bootstrap, Foundation etc.) for your project, what were the main reasons for doing so?</p>&mdash; Rachel Andrew (@rachelandrew) </blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script></p>

<p>There were <em>a lot</em> of responses. As I expected, there are far more reasons to use a framework than simply the grid system that it contains.</p>



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




<h4 id="a-framework-gives-your-team-ready-made-documentation">A Framework Gives Your Team Ready Made Documentation</h4>

<p>If you are working on a project with a number of other developers then any internal system you create will need to also include documentation to help your team members use it effectively. Creating useful documentation is time-consuming, skilled work in itself, and something that the big frameworks do very well.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b850a48a-e888-4a42-a6a6-c4a021558941/bootstraps-docs.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b850a48a-e888-4a42-a6a6-c4a021558941/bootstraps-docs.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b850a48a-e888-4a42-a6a6-c4a021558941/bootstraps-docs.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b850a48a-e888-4a42-a6a6-c4a021558941/bootstraps-docs.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b850a48a-e888-4a42-a6a6-c4a021558941/bootstraps-docs.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b850a48a-e888-4a42-a6a6-c4a021558941/bootstraps-docs.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b850a48a-e888-4a42-a6a6-c4a021558941/bootstraps-docs.png"
			sizes="100vw"
			alt="Screenshot of the Bootstrap documentation homepage"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The Bootstrap Documentation. ()
		</figcaption>
	
</figure>


<p>Framework documentation came up again and again, with many experienced front-end developers chipping in and explaining this is why they would recommend and use a CSS framework. I sometimes hear the opinion that people are using frameworks because they don’t really know CSS, many of the people replying, however, are well known to me as expert CSS developers. I’m sure that they are sometimes frustrated by the choices made by the framework, however, the positive aspects of that choice outweigh that.</p>

<h4 id="online-communities-easy-access-to-help">Online Communities: Easy Access To Help</h4>

<p>When you decide to use a particular tool, you also gain a community of users to ask for help. Unless you have a very clear CSS issue, and can produce a reduced use case to demonstrate it, asking for help with CSS can be difficult. It is especially so if you want to ask how to approach building a certain component. Using a framework can give you a starting point for your question; in general, you will be asking how to modify or style a particular component rather than starting from scratch. This is an easier thing to ask, as well as an easier thing to answer.</p>

<div class="sponsors__wide-place"></div>




<h4 id="the-grid-system">The Grid System</h4>

<p>Despite the fact that we have CSS Grid, many people replied that the main reason they decided to use a framework was for the grid system. Of course, many of these projects may have been started a long time before CSS Grid was available. Even today, however, concerns about backwards compatibility or team understanding of newer layout methods might cause people to decide to use a framework rather than adopting native CSS.</p>

<h4 id="speed-of-project-delivery">Speed Of Project Delivery</h4>

<p><blockquote class="twitter-tweet" data-conversation="none" data-lang="en"><p lang="en" dir="ltr">when having a unique design and efficient css were a much lower priority than the due date</p>&mdash; CodingBlocks.net (@CodingBlocks) </blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script></p>

<p>Opting for a framework will, in general, make it far quicker to deliver your project, in particular if that project fits very well with the way the framework does things and doesn’t need a lot of customization.</p>

<p>In the case of developing an MVP for a new idea, a framework may well be an excellent choice. You will have many things to spend time on, and be still testing assumptions in terms of what the project needs. Being able to develop that first version using a framework can help you get the product in front of users more quickly, and save burning up a lot of time developing things you then decide not to use.</p>

<p><blockquote class="twitter-tweet" data-conversation="none" data-lang="en"><p lang="en" dir="ltr">I go with a framework on anything that’s an MVP &mdash; minimal dev effort on tooling and frameworks to optimise for time working on the actual concept.<br><br>I make my own CSS “framework” on anything that’s a redo of an existing large-scale site/app.</p>&mdash; Ben Bodien (@bbodien) </blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script></p>

<p>Another place where speed and a bunch of ready built components can be very useful is when developing the backend admin system for a site or application. In the case where you simply need to create a few admin screens, a framework can save a lot of time styling form fields and other components! There are even dashboard themes for Bootstrap and Foundation that can give a helpful starting point.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b33cdffb-5792-4db7-a543-370154e97a00/foundation-dashboard.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b33cdffb-5792-4db7-a543-370154e97a00/foundation-dashboard.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b33cdffb-5792-4db7-a543-370154e97a00/foundation-dashboard.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b33cdffb-5792-4db7-a543-370154e97a00/foundation-dashboard.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b33cdffb-5792-4db7-a543-370154e97a00/foundation-dashboard.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b33cdffb-5792-4db7-a543-370154e97a00/foundation-dashboard.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b33cdffb-5792-4db7-a543-370154e97a00/foundation-dashboard.png"
			sizes="100vw"
			alt="Screenshot of a dashboard kit for Foundation"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Collections of dasboard components make it quicker to build out the admin for an app. ()
		</figcaption>
	
</figure>


<h4 id="i-m-not-a-designer">I’m Not A Designer!</h4>

<p>This point is the reason I’ve opted for a CSS framework in the past. I’m not a designer, and if I have to both design and build something, I’ll spend a long time trying to make design decisions I am entirely unqualified to make. It would be lovely to have the funds to hire a designer for every side project, however, I don’t, and so a framework might mean the difference between shipping the thing and not.</p>

<div class="sponsors__wide-place"></div>




<h4 id="dealing-with-css-bugs-and-browser-compatibility-issues">Dealing With CSS Bugs And Browser Compatibility Issues</h4>

<p>Mentioned less than I thought it might be was the fact that the framework authors would already have dealt with browser issues, be that due to actual bugs or lack of support for certain features. However, this was still a factor in the decision-making for many people.</p>

<h4 id="to-help-with-responsive-design">To Help With Responsive Design</h4>

<p><blockquote class="twitter-tweet" data-conversation="none" data-lang="en"><p lang="en" dir="ltr">Responsiveness of web pages . I found it difficult for me to decide breakpoints for web pages.</p>&mdash; Faisal Ali (@f_a_akhtar) </blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script></p>

<p>This came up a few times; people were opting for a framework specifically due to the fact it was responsive, or that I made decisions about breakpoints for them. I thought it interesting that this specifically was something called out as a factor in choosing to use a framework.</p>

<h3 id="why-not-use-a-framework">Why Not Use A Framework?</h3>

<p>Among positive reasons why frameworks had been selected were some of the issues that people have had with that choice.</p>

<h4 id="difficulty-of-overriding-framework-code">Difficulty Of Overriding Framework Code</h4>

<p>Many people commented on the fact that it could become difficult to override the code used in the framework, and that frameworks were a good choice if they didn’t need a lot of overriding. The benefits of ease of use, and everyone on the team understanding how to use the framework can be lost if there are then a huge number of customizations in place.</p>

<h4 id="all-websites-end-up-looking-the-same">All Websites End Up Looking The Same</h4>

<p>The blame for all websites starting to look the same has been placed squarely at the door of the well known CSS frameworks. I have seen sites where I am sure a certain framework has been used, then discover they are custom CSS, so prevalent are the design choices made in these frameworks.</p>

<p>The difficulty in overriding framework styles already mentioned is a large part of why sites developed using a particular framework will tend to look similar. This isn’t just a creative issue, it can be very odd as a user of a few websites which have all opted for the same framework to feel that they are all the same thing. In terms of conveying your brand, and making good user experience part of that, perhaps you lose something when opting for the generic choices of a framework.</p>

<h4 id="inheriting-the-css-problems-of-the-entire-world">Inheriting The CSS Problems Of The Entire World</h4>

<p>Whether front or back-end, any tool or framework that seeks to hit the mainstream has to solve as many problems as possible. Unless the tool is tightly coupled to solving one particular use-case it is going to contain a lot of very generic code, and code which solves problems that you do not have, and will never have.</p>

<p>You may be in the fortunate position of only needing your full experience to be viewed in the most current browsers, allowing for a more limited experience in Internet Explorer, or older versions of Chrome. Using a framework with lots of built-in support going back to IE9 would result in lots of additional code &mdash; especially given the improvements in CSS layout recently. It might also prevent you from being creative, as everything in the framework is assuming this requirement for support. Things which are possible using CSS may well be limited by the framework.</p>

<p>As an example, the grid systems in popular frameworks do not have an ability to span rows, as there isn’t any concept or rows in layout systems prior to Grid Layout. CSS Grid Layout easily allows for this. If you are tied to the Bootstrap Grid and your designer comes up with a design that includes elements which span rows, you are left unable to implement it &mdash; despite the fact that Grid might be supported by your target browsers.</p>

<h4 id="performance-issues">Performance Issues</h4>

<p>Related to the above are performance issues inherent in using fairly generic code, rather than something optimized for the exact use cases that you have. When trying to improve performance you will find yourself hitting up against the decisions of the framework.</p>

<h4 id="increased-technical-debt">Increased Technical Debt</h4>

<p><blockquote class="twitter-tweet" data-conversation="none" data-lang="en"><p lang="en" dir="ltr">Speed, mainly, though we quickly found out it was a bit of a false economy because it created substantial technical debt in the long run.</p>&mdash; Tim Cthulhuegdon (@nefarioustim) </blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script></p>

<p>While a framework might be a great way to get your startup quickly off the ground, and at the time of making that decision you are sure that you will replace it, is there a plan to make that happen?</p>

<h4 id="learning-a-framework-rather-than-learning-css">Learning A Framework Rather Than Learning CSS</h4>

<p>When talking to conference and workshop attendees, I have discovered that many people have only ever used a framework to write CSS. There is nothing wrong with coming into web development via one of these tools, given the complexity of the web platform today I imagine that will be the route in for many people. However, it can become a career-limiting choice, especially if the framework you based your skills around falls out of favor.</p>

<p>Having front-end developers without CSS knowledge should worry a company. It makes it incredibly hard to move away from that framework if your team doesn’t actually understand how to do CSS without it. While this isn’t really a reason not to use a framework, it is something to bear in mind when using one. When the day comes to move away you would hope that the team will be ready to take on something new, not needing to remember (or learn for the first time) how to write CSS!</p>

<h4 id="the-choice-doesn-t-consider-end-users">The Choice Doesn’t Consider End Users</h4>

<p>Nicole Sullivan asked . This was also the case with the responses to my question.</p>

<p>In our race to get our site built quickly, our desire to make things as good as possible for ourselves as the designers and developers of the site, do we forget who we are doing this for? Do the decisions made by the framework developer match up with the needs of the users of the site you are building?</p>

<div class="sponsors__wide-place"></div>




<h3 id="can-we-replace-frameworks-with-vanilla-css">Can We Replace Frameworks With “Vanilla” CSS?</h3>

<p>If you are considering replacing your framework or starting a new project without one, what are some of the things that you could consider in order to make that process easier?</p>

<h4 id="understand-which-parts-of-the-framework-you-need">Understand Which Parts Of The Framework You Need</h4>

<p>If you are replacing the use of a framework with your own CSS, a good place to start would be to audit your use of the current framework. Work out what you are using and why. Consider how you will replace those things in the new design.</p>

<p>You could follow a similar process when thinking about whether to select a framework or write your own. What parts of this could you reasonably expect to need? How well does it fit with your requirements? Will there be a lot of code that you import, potentially ask visitors to download, but never make use of?</p>

<h4 id="create-a-documented-pattern-library-or-style-guide">Create A Documented Pattern Library Or Style Guide</h4>

<p>I am a huge fan of working with pattern libraries and you can read my post here on Smashing Magazine about . A pattern library or a style guide enables the creation of documentation along with all of your components. I start all of my projects by working on the CSS in the pattern library.</p>

<p>You are still going to need to write the documentation, as someone who writes documentation, however, I know that often the hardest thing is knowing where to start and how to structure the docs. A pattern library helps with this by keeping the docs along with the CSS for the component itself. This approach can also help prevent the docs becoming out of date as they are tightly linked to the component they refer to.</p>

<h4 id="develop-your-own-css-code-guidelines">Develop Your Own CSS Code Guidelines</h4>

<p>Consistency across the team is incredibly useful, and without a framework, there may be nothing dictating that. With newer layout methods, in particular, there are often several ways in which a pattern could be built, if everyone picks a different one then inconsistencies are likely to creep in.</p>

<h4 id="better-places-to-ask-for-help">Better Places To Ask For Help</h4>

<p>Other than sending people in the direction of Stack Overflow, it seems that there are very few places to ask for help on CSS. In particular there seem to be few places which are approachable for beginners. If we are to encourage people away from third-party tools then we need to fill that need for friendly, helpful support which comes from the communities around those tools.</p>

<p>Within a company, it is possible that more experienced developers can become the CSS support for newer team members. If moving away from a framework to your own solution, it would be wise to consider what training might be needed to help bridge the gap, especially if people are used to using the help provided around the third party tool when they needed help in the past.</p>

<h4 id="style-guides-or-starting-points-for-non-designers">Style Guides Or Starting Points For Non-Designers</h4>

<p>I tie myself in knots with questions such as, &ldquo;Which fonts should I use?&rdquo;, &ldquo;How big should the headings be in relationship to the body text?&rdquo;, &ldquo;Is it OK to use a drop shadow?&rdquo; I can easily write the CSS &mdash; if I know what I’m trying to do! What I really need are some rules for making a not-terrible design, some kind of typography starting point, or a set of basic guidelines would replace being able to use the defaults of a framework in a lot of cases.</p>

<h4 id="educating-people-about-the-state-of-modern-browser-interoperability">Educating People About The State Of Modern Browser Interoperability</h4>

<p>I have discovered that people who have been immersed in framework-based development for a number of years, often have a view of browser interoperability which is several years out of date. We have never been in a better situation in terms of CSS working cross-browser. It may be that some browsers don’t support one new shiny bit of CSS, but in general, CSS (when supported) won’t be full of strange bugs. For example, in almost all cases if you use CSS Grid in one browser your CSS will work in exactly the same way in another.</p>

<p>If trying to make a case for not using a framework to team members who believe that the framework saves them from browser bugs, this point may be a useful one to raise. Are the browser compatibility problems real, or based on the concerns of the past?</p>

<h3 id="will-we-see-a-new-breed-of-frameworks">Will We See A New Breed Of Frameworks?</h3>

<p>Something that interests me is whether our new layout methods will help usher in a new breed of tools and frameworks. Will we see tools which take advantage of new layout methods, allow for more creativity but still give teams and individuals some of the undeniable advantages that came out of the responses to my tweet.</p>

<p>Perhaps by relying on new layout methods, rather than an inbuilt grid system, a new-style framework could be much lighter, becoming a collection of useful components. It might be able to then get away from some of the performance issues inherent in very generic code.</p>

<p>An area a framework could help with would be in helping to create solid fallbacks for browsers which don’t support newer layout methods, or by having really solid accessibility baked into the components. This could help provide guidance into a way of working that considers interoperability and accessibility, even for those people who don’t have these things in the forefront of their minds.</p>

<p>I don’t think that simply switching the Bootstrap Grid for CSS Grid Layout will achieve this. Instead, authors coming up with new frameworks, should perhaps look at some of the reasons outlined here, and try to solve them in new ways, using the new functionality we have in CSS to do that.</p>

<h3 id="should-you-use-a-framework">Should <em>You</em> Use A Framework?</h3>

<p>You and your team will need to answer that question yourself. And, despite what people might try to have you believe, there is no universal right or wrong answer. There is only what is right or wrong for your project. I hope that this article and the many responses to my original question might give you some things to discuss as you ponder that question.</p>

<p>Remember that the answer will change over time. It might be a useful thought experiment to not only consider what you need right now, in terms of initially doing the development for the site, but consider the lifespan of the site. Do you expect this still to be around in five years? Will your choice be a positive or negative one then?</p>

<p>Document your decisions, don’t be afraid to revisit them, and do ensure that you and your team maintain your skills outside of any framework that you decide to use. That way, you will be in a good place to move on in future and to make the best decisions for the next phases of your project.</p>

<p>I’d love the conversation started in that tweet to continue. Let us know your stories in the comments &mdash; they may well help other folks trying to work out what is best for their projects right now.</p>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(il)</span>
</div>


              </article>
            </body>
          </html>
---------------
<h1 id="#title_1" >2、每周分享第 30 期</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2018/11/weekly-issue-30.html](http://www.ruanyifeng.com/blog/2018/11/weekly-issue-30.html)
<p>这里记录过去一周，我看到的值得分享的东西，每周五发布。</p>

        <p>欢迎投稿，请前往 GitHub 的  提交 issue。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201811/bg2018110901.jpg" alt="" title="" /></p>

<p>上个月谷歌，社交应用 G+ 将在10个月后关闭。</p>

<p>主要原因有两个。一是缺乏用户，90%的用户会话短于5秒；二是有安全漏洞，近50万用户资料存在泄露风险，虽然没有证据表明黑客发现了这个漏洞。</p>

<p>谷歌是世界最大的互联网公司，资金和技术都不是问题，所有底层产品几乎都是业内最强：人工智能、搜索、邮件、地图、照片、云盘、在线办公......按理说，G+ 没有理由失败，谷歌只要把底层产品组合一下，就没人打得过。可是，G+ 就是做不起来。谷歌做过四个社交产品，全部失败了，这是为什么？</p>

<p>几年前，一度有传言，Gmail 要并入 G+，提升后者的访问量，结果也没有实施。这多少反映了 G+ 不是谷歌的核心业务，公司并没有不惜一切代价投入。谷歌这家公司的兴趣，从来不在应用软件，而是在基础服务、底层算法、操作系统上面。我猜想，谷歌内部多多少少把 G+ 看作玩具，"发动态，加好友，这种玩意有多少难度？"，工程师和科学家更愿意去研究高难度的产品。这才是 G+ 失败的根本原因，谷歌从高管到基层，对社交产品都缺乏足够兴趣。不信你去看，谷歌没有一个高管，喜欢玩社交媒体。甚至谷歌工程师里面，很少有特别喜欢写博客的，Steve Yegge 算一个，但是他觉得谷歌不合适自己，辞职了。</p>

<p>这件事情告诉我们，公司跟人一样，也有自己的兴趣爱好。倘若硬要去做那些没兴趣的事情，不仅内心煎熬，而且投入大量时间和金钱之后，最终还是难逃认赔离场的结局。</p>

<h2>新闻</h2>

<p>1、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201811/bg2018110902.jpg" alt="" title="" /></p>

<p>目前，太阳能发电主要是指光伏发电，将太阳光直接转化为电流。它的问题是，太阳光有间歇性，导致电能储存成了巨大问题。</p>

<p>但是，太阳能发电还有另一种方式，我们知道，聚焦太阳光会产生巨大的热量。这意味着，我们可以建立工厂，将太阳能转化为热能，然后通过热能发电。相比储存电能，热能的储存容易得多，这样就可以实现全天候发电。这在技术上已经可行，但是现阶段，太阳能的热能发电还是比光伏发电贵得多。上图为位于以色列内盖夫沙漠的110兆瓦太阳能发电厂。</p>

<p>2、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201811/bg2018110903.jpg" alt="" title="" /></p>

<p>视频播放器 Bitmovin 加入了观众感知功能。播放视频的时候，它会打开摄像头，观察正在看视频的观众。如果发现观众距离比较远，就降低了一些比特率（画面质量），反之则提高比特率；如果发现观众起身走开了，自动暂定播放，等到发现观众回来，再恢复播放。</p>

<p>3、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201811/bg2018110904.jpg" alt="" title="" /></p>

<p>交通控制都通过红绿灯。但是，如果车辆之间可以互相通信，我们是否还需要红绿灯？</p>

<p>卡内基梅隆大学开发的一种算法，允许汽车使用车载通信功能进行协商，彼此约定谁先通过路口、谁后通过，而无需使用任何红绿灯。通过模拟计算，这种算法比起红绿灯，可以将通勤时间减少三分之一。长远来看，它如果与自动驾驶汽车相结合，就可以精确控制整个行程的时间。</p>

<p>4、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201811/bg2018110905.jpg" alt="" title="" /></p>

<p>很多软件采用 GPL 许可证。这种许可证规定，如果你修改了代码再进行"分发"，就必须开放源码。但是，如果某家公司使用 GPL 软件提供线上服务，不分发软件本身，就可以不提供修改后的源码。很多人认为，这是 GPL 许可证的一个漏洞。</p>

<p>现在，MongoDB 宣布，许可证从 GPL 改为 SSPL，明确要求使用 Mongo 提供线上服务的公司，也必须开放源码。举例来说，如果亚马逊公司在 AWS 里面有一个 MongoDB 服务，那么现在它就必须开源它的 MongoDB 源码修改。</p>

<p>5、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201811/bg2018110906.jpg" alt="" title="" /></p>

<p>一家意大利3D打印公司，发明用泥浆和稻草打印小屋。每间的成本只要1000欧元。上图中，外墙的水平纹路就是一圈圈打印出来的。点击标题链接，就可以观看小屋打印过程的视频。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201811/bg2018110907.jpg" alt="" title="" /></p>

<p>6、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201811/bg2018110908.jpg" alt="" title="" /></p>

<p>伊斯坦布尔在地铁站新增了饮料瓶回收机，乘客提交饮料瓶，可以折算成地铁票积分。一个1.5升塑料瓶可以换6美分，一个易拉罐9美分，而单程地铁票是40美分。</p>

<p>7、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201811/bg2018110909.jpg" alt="" title="" /></p>

<p>美国科学家估算了，全世界生物体内的碳元素一共是550千兆吨（Gt C），其中植物占了450GTC，细菌70GTC，真菌12GtC，原核生物7GtC，单细胞生物4GtC，所有动物只有2GtC。</p>

<p>动物之中，一半是节肢动物（昆虫）占1GtC，鱼类0.7Gtc，人类0.06GtC，牲畜（以牛和猪为主）0.1GtC，野生哺乳动物0.007GtC。</p>

<p>8、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201811/bg2018110910.jpg" alt="" title="" /></p>

<p><img src="https://www.wangbase.com/blogimg/asset/201811/bg2018110911.jpg" alt="" title="" /></p>

<p>考古学家在黑海底部发现一艘世界最古老的沉船，据称这艘船有2700年的历史，可以追溯到古希腊。这艘船长23米，桅杆、方向舵和划艇长凳都存在，沉没在水下一英里的地方。考古学家说，那个深度缺氧，所以把它保留了下来。</p>

<p>以前人们只在大英博物馆收藏的古希腊陶器上，见过那个时代的船只。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201811/bg2018110912.jpg" alt="" title="" /></p>

<p>9、</p>

<p>欧洲议会支持禁止使用一次性塑料，以解决海洋，田野和水道的污染问题。根据拟通过的法令，塑料吸管、棉签、一次性塑料板、餐具等物品，都将在2021年禁止。</p>

<p>现在，大量的塑料废物冲入海洋，在那里可能需要几个世纪才能完全降解。那些轻质的一次性塑料物品是最大的麻烦，它们可以轻松地在海洋里长途漂流，破坏海洋动植物。</p>

<p>10、<strong>一句话新闻</strong></p>

<ul>
<li> 是世界第二大搜索引擎，它的每月搜索次数比 Bing + Yahoo 加起来都多。<br><br></li>
<li>开发出艾滋病口服预防片，可以预防艾滋病。<br><br></li>
</ul>

<p><img src="https://www.wangbase.com/blogimg/asset/201811/bg2018110913.jpg" alt="" title="" /></p>

<h2>教程</h2>

<p>1、（英文）</p>

<p>压缩是最常用的功能之一，压缩算法一般分成两大类：基于熵的压缩和基于字典的压缩。本文简单解释这两类算法的原理，以及将它们合在一起的 deflate 算法。</p>

<p>2、（英文）</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201811/bg2018110914.jpg" alt="" title="" /></p>

<p>Manjaro 是一个新的 Linux 发行版，内核采用 Arch Linux，UI 采用 Deepin，集灵活性和易用的 UI 于一体。</p>

<p>3、（英文）</p>

<p>本文回顾了加密发展的几个阶段，每个阶段都给出了 Python 的小例子。</p>

<p>4、（英文）</p>

<p>本文提出网页的无限滚动并不是一个好的设计，应该限制使用或者停止使用。</p>

<p>5、（英文）</p>

<p>WebAssembly 目前只是 MVP（最小可行产品）阶段，本文介绍了这种编译语言未来可能具有的功能。</p>

<p>6、（英文）</p>

<p>YAML 格式虽然比 JSON 格式易读易写，但也有很多问题。这种格式其实很复杂，并不是配置文件的理想格式。</p>

<p>7、（英文）</p>

<p>Pokemon GO 是一个在地图上捕捉口袋妖怪的游戏，初看起来相当无聊，不需要任何游戏技能。但是该游戏取得了惊人的成功，这是为什么？</p>

<p>8、（英文）</p>

<p>本文对三个层次的（初级、中级、高级）用户，介绍最合适的 Linux 发行版，用于桌面系统。对新手有一定的参考价值。</p>

<p>9、（英文）</p>

<p>网页性能的基础知识，针对初学者，内容比较全。</p>

<h2>资源</h2>

<p>1、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201811/bg2018110915.jpg" alt="" title="" /></p>

<p>谷歌有一个公开网页，展示使用 IPv6 访问谷歌的比例。最近，这个比率来到历史最高的25%。</p>

<p>2、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201811/bg2018110916.jpg" alt="" title="" /></p>

<p>一本英文的纯数学教材，免费下载，从简单的自然数讲起，包括代数、数论、集合运算、概率和微积分等章节。我觉得，至少对于了解数学的符号体系很有好处。</p>

<p>3、</p>

<p>按照主题，收集 JS 学习资源的仓库。</p>

<p>4、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201811/bg2018110917.jpg" alt="" title="" /></p>

<p>收集纸飞机折纸方法的网站，目前有40种纸飞机。</p>

<p>5、（Calculus made easy）</p>

<p>有名的微积分教材，版权已经过期。虽然年代比较久了，但是内容很经典。</p>

<p>6、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201811/bg2018110918.jpg" alt="" title="" /></p>

<p>该网站收集科幻影视作品里面出现的计算机界面设计。</p>

<p>7、</p>

<p>国人开发的前端题库，可以用作评测系统，带有讨论区。（@ 投稿）</p>

<h2>工具</h2>

<p>1、</p>

<p>通过把 Perl 5 解释器编译成 WebAssembly，从而在网页上运行 Perl 代码。</p>

<p>2、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201811/bg2018110919.jpg" alt="" title="" /></p>

<p>一个针对初学者的 Python IDE（集成编程环境），界面清爽简单，可用于儿童的编程教育。</p>

<p>3、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201811/bg2018110920.jpg" alt="" title="" /></p>

<p>这个 JS 库可以将网页上的外联 SVG 图像，变为内嵌的 SVG 图像，从而使得全局的 CSS 样式文件可以对这个图像生效。</p>

<p>4、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201811/bg2018110921.jpg" alt="" title="" /></p>

<p>一个质量不错的科幻风格 React UI 组件库。（@ 投稿）</p>

<p>5、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201811/bg2018110922.jpg" alt="" title="" /></p>

<p>一个类似 Disqus 的网站评论服务。</p>

<p>6、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201811/bg2018110923.jpg" alt="" title="" /></p>

<p>gRPC-Web 是一个JavaScript客户端库，使 Web 应用程序能够直接与后端gRPC服务通信，不需要 HTTP 服务器充当中介。这意味着可以构建真正的端到端 gRPC 应用程序体系结构。</p>

<p>7、</p>

<p>irondb  是一个浏览器 key-value 储存的封装库，把 Cookies、IndexedDB、LocalStorage、SessionStorage 统一成一个接口。它的最大特色就是数据冗余机制，即使某种底层储存机制失效，它可以从其他机制恢复数据。</p>

<p>8、</p>

<p>一个可以录制 GIF 图片的开源工具，同时还具备编辑帧、调用摄像头录制、录制画板等功能。（@ 投稿）</p>

<p>9、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201811/bg2018110924.jpg" alt="" title="" /></p>

<p>微软的在线工具，将手绘草图转成 HTML 代码。（ 投稿）</p>

<p>10、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201811/bg2018110925.jpg" alt="" title="" /></p>

<p>免费在线作图，可以实时协作。ProcessOn 支持流程图、思维导图、原型图、UML、网络拓扑图、组织结构图等。（@<em>_ _</em>投稿）</p>

<h2>文摘</h2>

<p>1、</p>

<p>美国国家航天局 NASA 正在讨论金星移民的可能。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201811/bg2018110926.jpg" alt="" title="" /></p>

<p>上图左侧是金星，右侧是地球。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201811/bg2018110927.jpg" alt="" title="" /></p>

<p>金星地面的照片。</p>

<p>初听起来，金星根本不是一个可能的目标，它的表面温度有460度，高于许多金属的熔点。下雪的时候，金星落下的实际上是金属滴。金星的大气压高达93个大气压，人类根本无法承受。金星大气由97％的二氧化碳，3％的氮气和微量的其他气体组成，还有大量硫酸形成的致密云层，因此它的空气具有腐蚀性。</p>

<p>NASA 讨论的并不是地面移民，而是派出一艘飞艇，飞行在金星地面上方50公里~60公里的高空中，人类就生活在飞艇里面。那个区域的大气压相当于地球海平面大气压的一半，跟乞力马扎罗山顶差不多，温度介于20°C和30°C之间。人类在那里甚至不需要宇航服与外界隔离，只需要携带氧气装置，因为那里的空气绝大部分是二氧化碳。</p>

<p>高于此高度的大气层也足够密集，可以保护人员免受来自太空的电离辐射。太阳辐射提供了比地球更大的能量，可用于发电（是地球太阳能发电效率的大约1.4倍）。</p>

<p>飞艇漂浮在空中，使用正常的地球空气填充就可获得浮力，因为氧气和氮气的比重低于二氧化碳，所以飞艇可以飞起来。目前的技术完全可以实现这个方案。</p>

<p>2、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201811/bg2018110928.jpg" alt="" title="" /></p>

<p>Martin Fowler 提出，大多数软件项目存在三类代码所有权。</p>

<p>（1）强代码所有权。</p>

<p>每个模块指定一个负责人。开发者只能更改自己拥有的模块，如果需要更改其他人的模块，就必须与模块所有者联系，让后者更改。你可以为其他模块写补丁，将其发送给模块所有者来加速此过程。</p>

<p>（2）弱代码所有权。</p>

<p>每个模块指定一个负责人，但是开发者可以更改其他人的模块。模块所有者应对其拥有的模块负责，密切关注其他人所做的更改。礼貌的做法是，更改其他人的模块之前，首先与模块所有者进行讨论。</p>

<p>（3）集体代码所有权。</p>

<p>模块不指定负责人，代码库由整个团队拥有，任何人都可以在任何地方进行更改。这种做法可以视为代码没有个人所有权，只有团队所有权。</p>

<p>现在大多数公司都要求所有人都可以修改源代码，也就是集体代码所有权的模式。这样的政策，很可能导致软件质量和员工敬业度的下降。如果你的目标是工程师既高效又以工作为荣的企业文化，那么强代码所有权模式是最佳选择。</p>

<p>3、</p>

<p>加州的国内生产总值超过2.7万亿美元，约占美国的13.9％。它的经济规模超过英国，是世界第五大经济体。该州极其富有，但令人难以置信的是，加州也是美国最贫穷的州之一。</p>

<p>贫困线以下的美国人口平均是13%，但是加利福尼亚州为19％，远高于阿拉巴马州的14％。加州穷人多的部分原因是房价快速上涨，这对富人有利，而对中产阶级来说，生活成本过高，于是成群结队地离开。随着中产阶级的离开，加利福尼亚的社会主要由富豪和穷人组成。</p>

<p>加州租房者每月平均支付1,447美元，而全国平均水平为1,012美元。29％的人将超过一半的收入用于住房。房屋中位数价值为529,000美元，是全国中位数239,800美元的两倍多。</p>

<p>加州的流浪者多得惊人。2016年到2017年，该州无家可归者人数增加了近14％，超过130,000人。2016 年，132名流浪者死在街头。旧金山有几百亿美元的富豪，但也遍地是流浪汉的粪便。</p>

<h2>本周图片</h2>

<p>1、</p>

<p>前苏联建造了大量令人叹为观止的雄伟纪念碑，大部分都是为了纪念战胜纳粹。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201811/bg2018110929.jpg" alt="" title="" /></p>

<p>四只巨手拿着四把枪，Novorossiysk，1978。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201811/bg2018110930.jpg" alt="" title="" /></p>

<p>苏联-波兰友谊纪念碑，1983。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201811/bg2018110931.jpg" alt="" title="" /></p>

<p>烈士纪念碑，摩尔多瓦，1972。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201811/bg2018110932.jpg" alt="" title="" /></p>

<p>北极士兵纪念碑，摩尔曼斯克，1974。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201811/bg2018110933.jpg" alt="" title="" /></p>

<p>空间征服者纪念碑，莫斯科,1972。</p>

<p>2、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201811/bg2018110934.jpg" alt="" title="" /></p>

<p>日本铁路公司 JR 有一个事故展览馆，专门展示该公司发生的事故。"我们希望我们的员工永远不会忘记过去的事故。"不过，该展览馆只允许员工参观，不对公众开放。</p>

<h2>新奇</h2>

<p>1、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201811/bg2018110935.jpg" alt="" title="" /></p>

<p>一家创业公司正在开发 AI 音乐引擎。该引擎学习了无数旋律以后，已经能够自己生成音乐，主要用来为电影和游戏生成音轨。</p>

<p>大家可以去该公司的网站，收听机器生成的音乐，那些音乐非常动听。</p>

<h2>本周金句</h2>

<p>1、</p>

<p>由于重力只有地球的六分之一，月球很合适人类养老。在本世纪末之前，我们将在月球上为老年人设立医院，使他们能够长寿。他们的心脏在六分之一的重力下，可以跳得更轻快；他们脆弱的骨头，也将承担轻得多的负荷。</p>

<p>-- 在1969年7月20日（阿波罗11号登月日）接受采访，谈登月对人类的影响</p>

<p>2、</p>

<p>JavaScript 的优点是可以写任何东西，缺点是你真的会用它去写这些东西。</p>

<p>-- </p>

<p>3、</p>

<p>据估计，2009年全球有500万 PHP 开发人员。</p>

<p>-- </p>

<p>4、</p>

<p>房价不断上涨的前提是不断有新人加入，他们愿意并且能够支付越来越高的房价。房价上涨的本质是，年轻人愿意把自己的财富转移给老年人，当这些年轻人变老时，再有新的年轻人愿意给他们更多的钱。</p>

<p>-- </p>

<h2>欢迎订阅</h2>

<p>这个专栏每周五发布，同步更新在我的。</p>

<p>微信搜索"<strong>阮一峰的网络日志</strong>"或者扫描二维码，即可订阅。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2018/bg2018042311.jpg" alt="" title="" /></p>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2018-11-09T08:21:13+08:00">2018年11月 9日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>文集：</li>
<li>社交媒体：</li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------
<h1 id="#title_2" >3、Going beyond console.log()</h1>

[https://javascriptweekly.com/issues/411](https://javascriptweekly.com/issues/411)
<table border=0 align="center" border="0">
  <tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   ">

  <div>    
    <table border=0 border=0><tr>
<td align="left" style="padding-left: 4px; font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   "><p>#411 — November  9, 2018</p></td>
<td align="right" style="padding-right: 4px; font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   "><p></p></td>
</tr></table>
    
    <table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0 12px;"><p>JavaScript Weekly</p></td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   ">
  
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"> is a new site that shows up to date level of support and information on how different JavaScript engines support various language features based on the results of more than 68000 tests.</p>
  <p>Rick Waldron and Boaz Sender </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — While <code>console.log()</code> may form the basis of many people’s debugging strategies, the console object has a <em>lot</em> more to offer, as covered here. If you don’t know about <code>console.assert</code> or <code>console.count</code>, step in.</p>
  <p>Matt Burgess </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Resourcing problems and changing requirements impact your cost and speed of app delivery. Newer techniques drastically reduce costs and time. Learn more about how enterprises are accelerating development, cutting expenses, and reducing IT app backlog.</p>
  <p>Progress Kinvey <span style="text-transform: uppercase; padding: 1px 4px;  margin-left: 4px; font-size: 0.9em;   color: #997 !important;">sponsor</span></p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Netflix boosted performance on their frontend by switching from React and other client-side libraries to vanilla JS.</p>
  <p>Addy Osmani </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"> proposal (essentially arbitrary-precision integers) is due to become an official part of ECMAScript in the near future - this lets you play with it now.</p>
  <p>Google Chrome Labs </p>
</td></tr></table>
<table border=0 border=0><tr><td style=" font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   "></td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   ">
  
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Small and sweet, mobile friendly, and the homepage has lots of good demos. Plus, I just noticed it mentions this newsletter 😆.</p>
  <p>Nick Piscitelli </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Aurelia is a modern front-end framework and it has gained many enhancements recently including a new single-file build you can pull into a page with a single <code>script</code> tag which makes it even easier to try out.</p>
  <p>Rob Eisenberg </p>
</td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0;"><p>💻 Jobs</p></td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;">.</p>
  <p>x-team </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Sticker Mule is looking for passionate developers to join our remote team. Come help us become the Internet’s best place to shop and work.</p>
  <p>Sticker Mule </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Through Hired, software engineers have transparency into salary offers, competing opportunities, and job details.</p>
  <p>Hired </p>
</td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0;"><p>📘 Tutorials and Opinions</p></td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — A look at a pattern for implementing static properties in ES6.</p>
  <p>Valeri Karpov </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Pete Corey </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;">) have been one of the last ES6 features to see widespread support in browsers.</p>
  <p>Can I Use </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — A guide to the Canvas API, one of the best ways to draw graphics dynamically in the browser.</p>
  <p>Flavio Copes </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;">▶  .</p>
  <p>Azure <span style="text-transform: uppercase; padding: 1px 4px;  margin-left: 4px; font-size: 0.9em;   color: #997 !important;">sponsor</span></p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;">▶  </span></p>
  <p>Daniel Persson </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Rob Ferguson </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Salomone Baquis </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Your first question might well be, why would it be necessary to interfere with the Virtual DOM? Well…</p>
  <p>Michael Gallagher </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — A list of handy Git aliases inspired by the oh-my-zsh suite.</p>
  <p>Michal Konarski </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Bitmovin <span style="text-transform: uppercase; padding: 1px 4px;  margin-left: 4px; font-size: 0.9em;   color: #997 !important;">sponsor</span></p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Blanca Mendizábal Perelló </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>SitePoint </p>
</td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0;"><p>🔧 Code and Tools</p></td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — This online tool will analyze your bundle and give you actionable suggestions on how to reduce its size.</p>
  <p>Jakob Lind </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Very much an experiment/POC but interesting nonetheless.</p>
  <p>Tobias Koppers </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Practice proactive error monitoring: stop outsourcing bug discovery to users, or using logs for debugging.</p>
  <p>Rollbar <span style="text-transform: uppercase; padding: 1px 4px;  margin-left: 4px; font-size: 0.9em;   color: #997 !important;">sponsor</span></p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Supports most color spaces and formats defined in the CSS Colors Level 4 spec and can parse, convert, mix, create color differences, and more.</p>
  <p>Moqups </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>EGOIST </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — A minimalist library that parses, validates, manipulates, and displays dates and times for modern browsers with a largely Moment.js-compatible API.</p>
  <p>iamkun </p>
</td></tr></table>
<table border=0 border=0><tr><td style=" font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   "></td></tr></table>
</div>

  </td></tr>
</table>





<img src="https://javascriptweekly.com/open/411/rss" width="1" height="1" />
---------------