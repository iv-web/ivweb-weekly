## 文章索引
1、 <a href="#1一文带你深入拆解java虚拟机" >一文带你深入拆解Java虚拟机</a><br/>
2、 <a href="#2so-you-want-to-persuade-users-make-things-simple!" >So You Want to Persuade Users? Make Things Simple!</a><br/>
3、 <a href="#3文章-腾讯大规模分布式机器学习系统无量是如何进行技术选型的" >文章： 腾讯大规模分布式机器学习系统无量是如何进行技术选型的？</a><br/>
4、 <a href="#4文章-来自buoyant公司的建议如何在生产环境中应用服务网格" >文章： 来自Buoyant公司的建议：如何在生产环境中应用服务网格</a><br/>
5、 <a href="#5视频演讲-基于混合云的应用部署平台构建实践" >视频演讲： 基于混合云的应用部署平台构建实践</a><br/>
6、 <a href="#6视频演讲-基于多项目的离线缓存实现方案" >视频演讲： 基于多项目的离线缓存实现方案</a><br/>
7、 <a href="#7视频演讲-百度aiops实践" >视频演讲： 百度AIOps实践</a><br/>
8、 <a href="#8文章-现代存储系统背后的算法" >文章： 现代存储系统背后的算法</a><br/>
9、 <a href="#9盲目跟风还是无动于衷这篇文章彻底治愈区块链学习焦虑症" >盲目跟风还是无动于衷？这篇文章彻底治愈区块链学习焦虑症！</a><br/>
10、 <a href="#10新ciomark-schwartz认为的领先it" >新CIO：Mark Schwartz认为的领先IT</a><br/>
11、 <a href="#11在首次发布三周之后mlflow迎来了02版本" >在首次发布三周之后，MLflow迎来了0.2版本</a><br/>
12、 <a href="#12eslint的npm账户遭黑客攻击可能窃取用户npm访问令牌" >ESLint的NPM账户遭黑客攻击，可能窃取用户NPM访问令牌</a><br/>
13、 <a href="#13facebook使用机器学习手段来自动优化其系统性能" >Facebook使用机器学习手段来自动优化其系统性能</a><br/>
14、 <a href="#14文章-戳破泡沫人工智能应该这样看" >文章： 戳破泡沫，人工智能应该这样看！</a><br/>
15、 <a href="#15文章-github的mysql高可用性实践" >文章： GitHub的MySQL高可用性实践</a><br/><h1 id="#title_0" >1、一文带你深入拆解Java虚拟机</h1>
郑雨迪
[http://www.infoq.com/cn/news/2018/07/oracle-java-jvm?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/oracle-java-jvm?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>一文带你深入拆解Java虚拟机。</p> <i>By 郑雨迪</i>
---------------
<h1 id="#title_1" >2、So You Want to Persuade Users? Make Things Simple!</h1>
Lyndon Cerejo
[https://www.smashingmagazine.com/2018/07/persuasion-user-experience-design/](https://www.smashingmagazine.com/2018/07/persuasion-user-experience-design/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/07/persuasion-user-experience-design/" />
              <title>So You Want to Persuade Users? Make Things Simple!</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>So You Want to Persuade Users? Make Things Simple!</h1>
                  
                    
                    <address>Lyndon Cerejo</address>
                  
                  <time datetime="2018-07-17T16:15:38&#43;02:00" class="op-published">2018-07-17T16:15:38+02:00</time>
                  <time datetime="2018-07-17T20:48:28&#43;00:00" class="op-modified">2018-07-17T20:48:28+00:00</time>
                </header>
                

<p><p>(<em>This article is kindly sponsored by Adobe</em>.) The persuasive design toolbox is filled with powerful tools based on psychology. These tools range from Cialdini’s set of six principles of persuasion to . Presented with all these methods, it can be tempting to use all of them to cover all possible bases, using a shotgun approach, hoping that one will resonate with your target users.</p>

<p>However, applying persuasion principles and patterns in a haphazard manner just ends up being persuasive design clutter. Like user experience design, designing for everyone is designing for no one. Randomly thrown together persuasive techniques will also make users feel manipulated, not in control, making them abandon the site or experience. The key to persuading your users is to keep it simple: using focused persuasive techniques and tactics that will work for your users.</p>

<h3 id="persuasion-funnel">Persuasion Funnel</h3>

<p> is an acronym used in marketing and advertising to describe the stages that a customer goes through in the purchase process. The stages of <strong>A</strong>ttention, <strong>I</strong>nterest, <strong>D</strong>esire and <strong>A</strong>ction, generically follow a series of cognitive (thinking) and affective (feeling) stages culminating in a behavioral (doing e.g. purchase or trial) stage. This should sound familiar since this is what we do through design, especially persuasive design.</p>

<p>When it comes to persuasive design, users go through a few stages between Awareness and Action, and the design should guide them from one stage to the next. I don’t have a clever acronym for it (yet), but the stages the design has to take the users through are:</p>

<ul>
<li>Awareness</li>
<li>Relevant</li>
<li>Credible</li>
<li>Usable</li>
<li>Desirable</li>
<li>Persuasive</li>
<li>Action</li>
</ul>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5b6a1e88-7419-4c7a-8095-627d7fb667e5/awareness-action-funnel-large.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5b6a1e88-7419-4c7a-8095-627d7fb667e5/awareness-action-funnel-large.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5b6a1e88-7419-4c7a-8095-627d7fb667e5/awareness-action-funnel-large.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5b6a1e88-7419-4c7a-8095-627d7fb667e5/awareness-action-funnel-large.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5b6a1e88-7419-4c7a-8095-627d7fb667e5/awareness-action-funnel-large.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5b6a1e88-7419-4c7a-8095-627d7fb667e5/awareness-action-funnel-large.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5b6a1e88-7419-4c7a-8095-627d7fb667e5/awareness-action-funnel-large.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<p>When users are contemplating an action (like booking a hotel room), they have to be aware of your site, app, or experience. Once they begin their journey on your site, they quickly evaluate the experience and either proceed to the next step or leave and go elsewhere. With fewer users continuing to subsequent stages, the number of users at each stage begins to resemble the shape of a funnel as shown above.</p>

<p>Let’s peek inside what could be going on in hypothetical users’ minds as they go through the experience of booking a hotel room for New Year’s Eve in Times Square, and some of the reasons they may drop off in each stage.</p>

<h4 id="awareness">Awareness</h4>

<blockquote>“Hmmm… Where do I start? Hotel chains promise the lowest rate if we book directly with them, but I won’t be able to see other hotel options around Times Square. Hotel… Maybe I should try an online travel agency like Trivago (looks like the  advertising works!) to find a wider range of hotels. I’m going to also quickly Google it to see if there are other options.”</blockquote>

<p>Users have to be aware of your site, app or experience to use it &mdash; Duh!</p>

<h4 id="relevant">Relevant</h4>

<blockquote>“I found HotelTonight on Google. It looks like a great way to get rooms last minute, but not this far in advance &mdash; it’s not relevant to me.”</blockquote>

<p>If your experience is not relevant to the task they are trying to accomplish, users will leave and try elsewhere. If your products or services are relevant, but not findable by the user, work on your navigation, search, and content layout to ensure your products and services are visible. Everything does not have to be one click away, but if the user gets the , or cues that make them think they are on the right path, they will follow the trail to that information.</p>

<h4 id="credible">Credible</h4>

<blockquote>“This design looks like it hasn’t been updated since the [GeoCities era](http://www.arngren.net/).<br /><br />&mdash; Warning bells go off in head &mdash;<br /><br />I’m out of here.”</blockquote>

<p>Users are aware of many of the risks available online and look for trust indicators including a known brand and domain, secure site, professional design, real-world contact information and third-party certificates or badges. Incorporate these elements to create a comfort level for the user.</p>

<h4 id="usable">Usable</h4>

<blockquote>“I can’t figure out where things are in the navigation, and the search results had hundreds of unhelpful results. The homepage has nice big images, but that meant I had to scroll before I could see any real content.”</blockquote>

<p>Usability is surprisingly still an issue with many sites. Follow User Experience best practices during design, and test with users to validate that the design is usable.</p>

<h4 id="desirable">Desirable</h4>

<blockquote>“This reminds me of Craigslist &mdash; it is usable, but the design does not make me want to stay and use it. I’ll try that other hotel website that provides an immersive, interactive experience as I search for hotels.”</blockquote>

<p>As much as we like to believe it, users’ decisions are not always rational, and very often driven by emotion, and we can address that through design. Usability is about making it work well; this is about making it beautiful as well.</p>

<p>In his book , Don Norman explains: &ldquo;Attractive things do work better &mdash; their attractiveness produces positive emotions, causing mental processes to be more creative, more tolerant of minor difficulties.&rdquo; Don talks about the three different aspects of design: visceral, behavioral, and reflective. Visceral design is about appearance, behavioral about the pleasure and effectiveness of use, and reflective design involves the rationalization and intellectualization of a product.</p>

<h4 id="persuasive">Persuasive</h4>

<blockquote>“Oh, Wow! That’s a long list of hotels, with plenty of availability for New Year’s Eve. There’s no real reason to book now. I’ll just come back to book after Thanksgiving…”</blockquote>

<p>The user was interested, able, and willing, but the design did not motivate him to take intended action. Use relevant persuasion techniques that apply to your user to move them toward the desired action.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dd063f00-f552-4af0-b18d-3bb852053f6e/persuasive-methods-travelocity-example-large.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dd063f00-f552-4af0-b18d-3bb852053f6e/persuasive-methods-travelocity-example-large.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dd063f00-f552-4af0-b18d-3bb852053f6e/persuasive-methods-travelocity-example-large.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dd063f00-f552-4af0-b18d-3bb852053f6e/persuasive-methods-travelocity-example-large.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dd063f00-f552-4af0-b18d-3bb852053f6e/persuasive-methods-travelocity-example-large.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dd063f00-f552-4af0-b18d-3bb852053f6e/persuasive-methods-travelocity-example-large.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dd063f00-f552-4af0-b18d-3bb852053f6e/persuasive-methods-travelocity-example-large.png"
			sizes="100vw"
			alt="Examples of persuasive methods while shopping on Travelocity for a hotel room for New Year’s Eve."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Examples of persuasive methods while shopping on Travelocity for a hotel room for New Year’s Eve. ()
		</figcaption>
	
</figure>


<h4 id="action">Action</h4>

<blockquote>“Oh, Wow! 65% of hotels are already booked in this area for New Year’s Eve. I better make a reservation now. <Scanning the results list, like the screenshot above>. This looks like a nice hotel, and it also offers free cancellation - I’m reserving it now!”</blockquote>

<p>The user who made it to this stage was interested, able, and willing, and the design nudged him to take intended action of making a reservation before leaving the site.</p>

<p>Persuasion is not about applying all available principles and patterns to your designs, but systematically identifying how you can address users’ barriers and motivators during each step of the journey, and guiding your users through the funnel to take the desired action.</p>

<h3 id="the-kiss-approach">The KISS Approach</h3>

<p>Most of us are familiar with the acronym : &ldquo;Keep It Simple, Stupid,&rdquo; a principle advocating simplicity as a key goal in design by avoiding unnecessary complexity. Let’s borrow that acronym for a 4-step approach to persuasive design.</p>

<h4 id="k-now-the-right-behavior-to-target"><strong>K</strong>now The Right Behavior To Target</h4>

<p>The first step is knowing the behavior you would like to target, and identifying the simplest action that can lead to that behavior change. Take the example of term life insurance companies who, to put it very bluntly, stand to benefit if their policyholders are healthy and don’t die while the policy is active. While those companies have a long-term ambitious goal of helping their policyholders lead healthy lives (mutually beneficial), that could be broken down into a simpler target behavior of walking 10,000 steps daily. This behavior is simple to understand, achieve, measure, and contributes to the long-term goal of healthier policyholders.</p>

<p>One such insurance company is offering new policyholders the latest Apple Watch for a low initial down payment ($25). The ongoing monthly payments can be waived each month that the policyholder leads an active lifestyle and exercises regularly (e.g. walks about 10,000 steps a day). About half the people who participated have .</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8eea2ad6-9d3e-4b7c-add7-f5edfdd81bf9/life-insurance-apple-watch-offer-large.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8eea2ad6-9d3e-4b7c-add7-f5edfdd81bf9/life-insurance-apple-watch-offer-large.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8eea2ad6-9d3e-4b7c-add7-f5edfdd81bf9/life-insurance-apple-watch-offer-large.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8eea2ad6-9d3e-4b7c-add7-f5edfdd81bf9/life-insurance-apple-watch-offer-large.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8eea2ad6-9d3e-4b7c-add7-f5edfdd81bf9/life-insurance-apple-watch-offer-large.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8eea2ad6-9d3e-4b7c-add7-f5edfdd81bf9/life-insurance-apple-watch-offer-large.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8eea2ad6-9d3e-4b7c-add7-f5edfdd81bf9/life-insurance-apple-watch-offer-large.png"
			sizes="100vw"
			alt="John Hancock Term Life Insurance Apple Watch offer targets walking about 10,000 steps a day."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			John Hancock Term Life Insurance Apple Watch offer targets walking about 10,000 steps a day. ()
		</figcaption>
	
</figure>


<h4 id="i-dentify-barriers-and-motivators"><strong>I</strong>dentify Barriers And Motivators</h4>

<p>User research for persuasive design digs below the surface thinking level to the feeling level, and moves beyond the rational to the emotional level, as shown below.  will help you use psychology to focus your design to get users to engage in the target behavior identified above. User interviews that focus on users’ feelings and emotions are used to uncover barriers and motivators they consciously or subconsciously face while trying to achieve the target behavior. This helps us identify which blocks we need to weaken, and which motivators we should strengthen, through persuasive design techniques and tactics.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/eb2e9399-310e-497d-a2ff-8e4be0e78854/tip-of-the-iceberg-user-research-large.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/eb2e9399-310e-497d-a2ff-8e4be0e78854/tip-of-the-iceberg-user-research-large.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/eb2e9399-310e-497d-a2ff-8e4be0e78854/tip-of-the-iceberg-user-research-large.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/eb2e9399-310e-497d-a2ff-8e4be0e78854/tip-of-the-iceberg-user-research-large.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/eb2e9399-310e-497d-a2ff-8e4be0e78854/tip-of-the-iceberg-user-research-large.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/eb2e9399-310e-497d-a2ff-8e4be0e78854/tip-of-the-iceberg-user-research-large.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/eb2e9399-310e-497d-a2ff-8e4be0e78854/tip-of-the-iceberg-user-research-large.jpg"
			sizes="100vw"
			alt="Tip of the iceberg user research diagram"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<h4 id="s-implify-the-experience"><strong>S</strong>implify The Experience</h4>

<p>Simplify the design experience of the first stages of the funnel, as users go through the mental verifications of relevancy, credibility, and usability of the experience. This includes making it easy for the user to find what they are looking for, credibility indicators like professional design, contact information, and third-party certificates or badges, as well as addressing usability issues. As Steve Krug put it very succinctly: &ldquo;&rdquo;.</p>

<h4 id="s-elect-appropriate-triggers"><strong>S</strong>elect Appropriate Triggers</h4>

<p>Users who have made it this far in the process are interested in something you have to offer. As a designer, you have to nudge them to take the desired action. A good starting point is Robert Cialdini’s, :</p>

<ol>
<li><strong>Reciprocity</strong><br />
People are obliged to give something back in exchange for receiving something.</li>
<li><strong>Scarcity</strong><br />
People want more of those things they can have less of.</li>
<li><strong>Authority</strong><br />
People follow the lead of credible, knowledgeable experts.</li>
<li><strong>Consistency</strong><br />
People like to be consistent with the things they have previously said or done.</li>
<li><strong>Liking</strong><br />
People prefer to say yes to those that they like.</li>
<li><strong>Consensus (Social Proof)</strong><br />
Especially when they are uncertain, people will look to the actions and behaviors of others to determine their own.</li>
</ol>

<p>These principles can be applied through dozens of different persuasive design patterns and methods, some of which have been previously published on Smashing Magazine (.</p>

<p>Given that there are dozens of patterns and methods (depending on where you look), it is important to selectively use methods that will resonate with your users. Applying all design patterns in the hope of some working will result in persuasion clutter and overwhelm the user, possibly driving them away from your site.</p>

<h3 id="examining-persuasion">Examining Persuasion</h3>

<p>Let’s take a closer look at the earlier example of the term life insurance through the eyes of someone who is motivated (shopping for life insurance) and has the ability (to pay monthly life insurance cost). Like me, let’s assume that this user was made aware of this through a sponsored post on Facebook. During the stages of awareness and relevance, there are a few persuasive triggers as shown below that make the user click &ldquo;Learn More&rdquo;.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3a5f0222-720d-421c-bb7e-2f99c88cd96e/jh-facebook-post-persuasion-large.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3a5f0222-720d-421c-bb7e-2f99c88cd96e/jh-facebook-post-persuasion-large.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3a5f0222-720d-421c-bb7e-2f99c88cd96e/jh-facebook-post-persuasion-large.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3a5f0222-720d-421c-bb7e-2f99c88cd96e/jh-facebook-post-persuasion-large.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3a5f0222-720d-421c-bb7e-2f99c88cd96e/jh-facebook-post-persuasion-large.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3a5f0222-720d-421c-bb7e-2f99c88cd96e/jh-facebook-post-persuasion-large.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3a5f0222-720d-421c-bb7e-2f99c88cd96e/jh-facebook-post-persuasion-large.png"
			sizes="100vw"
			alt="facebook"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<p>Clicking the &ldquo;Learn More&rdquo; button takes the user to a landing page that we will examine in sections for a persuasive flow:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0521424b-45b4-4978-978f-aeba231d4e4b/jh-landing-persuasion-1of2-large.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0521424b-45b4-4978-978f-aeba231d4e4b/jh-landing-persuasion-1of2-large.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0521424b-45b4-4978-978f-aeba231d4e4b/jh-landing-persuasion-1of2-large.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0521424b-45b4-4978-978f-aeba231d4e4b/jh-landing-persuasion-1of2-large.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0521424b-45b4-4978-978f-aeba231d4e4b/jh-landing-persuasion-1of2-large.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0521424b-45b4-4978-978f-aeba231d4e4b/jh-landing-persuasion-1of2-large.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0521424b-45b4-4978-978f-aeba231d4e4b/jh-landing-persuasion-1of2-large.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<p>The user’s primary motivation in shopping for term life insurance is: &ldquo;Protect Family,&rdquo; and a big barrier is “High Cost.”</p>

<ol>
<li><strong>Reputable Name (Credibility)</strong><br />Even if you’ve not heard of this company, John Hancock is a famous person and the term used as a synonym in the United States for one's signature. The company reinforces it’s longevity later on the page.</li>
<li><strong>Toll-free Number (Credibility)</strong><br />Established and legitimate organization.</li>
<li><strong>Message Framing</strong><br />Live healthy, is also reinforced by the image of a family enjoying outdoors.<br /><blockquote>“This life insurance product will help me live longer, lead a happy life like them, and protect my family in case something happens, and won’t cost much.”</blockquote></li>
<li><strong>People Like Me & Association</strong><br />This family looks like mine (or the family next door) &mdash; I can see myself in this wide-open field (visceral and reflective triggers).</li>
<li><strong>Extrinsic Reward</strong><br />An Apple watch for $25 &mdash; that’s a bonus here!</li>
<li><strong>Visual Cueing</strong><br />The person in focus (stereotypical breadwinner) has his gaze directly focused at the form below, leading the user to the next step.</li>
<li><strong>Foot In The Door</strong><br />This quote won’t cost anything &mdash; zip, <em>nada</em>.</li>
<li><strong>Computer As A Social Actor</strong><br />The information takes a conversational tone and format, not the usual form in rows and columns. The information seems reasonable to generate a quote.</li>
<li><strong>Commitment & Consistency</strong><br />By filling this quick, easy, and free form, chances are that the user will act consistently and proceed when it comes to the next step (application), unless there’s another barrier (price, benefits, etc.)











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6dc361e3-b860-4715-a4ac-395cf5961c61/jh-landing-persuasion-2of2-large.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6dc361e3-b860-4715-a4ac-395cf5961c61/jh-landing-persuasion-2of2-large.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6dc361e3-b860-4715-a4ac-395cf5961c61/jh-landing-persuasion-2of2-large.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6dc361e3-b860-4715-a4ac-395cf5961c61/jh-landing-persuasion-2of2-large.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6dc361e3-b860-4715-a4ac-395cf5961c61/jh-landing-persuasion-2of2-large.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6dc361e3-b860-4715-a4ac-395cf5961c61/jh-landing-persuasion-2of2-large.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6dc361e3-b860-4715-a4ac-395cf5961c61/jh-landing-persuasion-2of2-large.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>

</li>
<li><strong>Control</strong><br />The user has a choice of devices.</li>
<li><strong>Extrinsic Rewards</strong><br />More rewards to be earned.</li>
<li><strong>Control</strong><br />The user controls how much they pay (the more active, the less you’ll pay). Also, in case the user does is not active, the cost is framed as just $13 (for a month).</li>
<li><strong>Credibility</strong><br />The company reinforces longevity and protector of America.</li>
<li><strong>Authority</strong><br />Licensed Coverage Coach (not just a sales agent).</li>
<li><strong>Flow</strong><br />One way to keep users in the flow and not get distracted is by disabling the social media links (which could raise the question: why display them?).</li>
</ol>

<p>That took longer to dissect and read than it does in real life, where most of this is processed consciously and subconsciously in a few seconds, often with a glance or two.</p>

<p>Apart from the methods establishing credibility, the persuasive methods are used to strengthen the primary motivator of &ldquo;Protect Family&rdquo; (get insurance, extrinsic reward will help me live longer for my family), and weaken the barrier of “High Cost” (low monthly cost, additional savings, no ongoing watch payments). Note how they work together and don’t conflict or clutter the experience.</p>

<h3 id="conclusion">Conclusion</h3>

<p>Persuasion is all around us, in our everyday lives. As designers, we can use  persuasive design methods to get users to take some action. With plenty of persuasive methods available, we have to be selective about what we use. We can use the KISS approach to keep it simple:</p>

<ul>
<li><strong>K</strong>now the right behavior to target</li>
<li><strong>I</strong>dentify barriers and motivators</li>
<li><strong>S</strong>implify the experience</li>
<li><strong>S</strong>elect appropriate triggers</li>
</ul>

<p>KISS also reminds us to <strong>K</strong>eep <strong>I</strong>t <strong>S</strong>imple &amp; <strong>S</strong>traightforward, by selecting a simple target behavior, simplifying the experience for the user, and by applying persuasive techniques that will lead to the target behavior without overwhelming the user.</p>

<h4 id="further-reading">Further Reading</h4>

<ul>
<li>“,” Susan Weinschenk</li>
<li>“,” Victor S. Yocco</li>
<li>“, by Robert B. Cialdini</li>
<li>“,” B.J. Fogg</li>
<li>“ (scroll down the page),” UI-Patterns</li>
<li>“,” UI-Patterns</li>
</ul>

<p><em>This article is part of the UX design series sponsored by Adobe. Adobe XD tool is made for a  to stay updated and informed on the latest trends and insights for UX/UI design.</em></p>




<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(yk, il)</span>
</div>


              </article>
            </body>
          </html>
---------------
<h1 id="#title_2" >3、文章： 腾讯大规模分布式机器学习系统无量是如何进行技术选型的？</h1>
张红林
[http://www.infoq.com/cn/articles/tencent-distribited-machine-learning?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/tencent-distribited-machine-learning?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/tencent-distribited-machine-learning/zh/smallimage/GettyImages-947661322-1527676268787-1531565863535.jpg"/><p>在互联网场景中，亿级的用户每天产生着百亿规模的用户数据，形成了超大规模的训练样本。如何利用这些数据训练出更好的模型并用这些模型为用户服务，给机器学习平台带来了巨大的挑战。腾讯开发了一个基于参数服务器架构的机器学习计算框架——无量框架，已经能够完成百亿样本/百亿参数模型的小时级训练能力。无量框架提供多种机器学习算法，不但能进行任务式的离线训练，还能支持以流式样本为输入的 7*24 小时的在线训练。</p> <i>By 张红林</i>
---------------
<h1 id="#title_3" >4、文章： 来自Buoyant公司的建议：如何在生产环境中应用服务网格</h1>
Thomas Rampelberg
[http://www.infoq.com/cn/articles/adopting-new-tech-service-mesh?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/adopting-new-tech-service-mesh?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/adopting-new-tech-service-mesh/zh/smallimage/adopting-new-tech-service-mesh-logo-1531154551611-1531635739502.jpg"/><p>在生产环境中采用服务网等新技术将会对你和你的同事产生影响，注意这些影响，可以为利益相关者提供更好的支持。明确你要解决的问题，并确定适当的验收标准。通过实验向各个利益相关者展示服务网格将如何让他们的生活变得更美好。</p> <i>By Thomas Rampelberg</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_4" >5、视频演讲： 基于混合云的应用部署平台构建实践</h1>
赵明、张夏
[http://www.infoq.com/cn/presentations/practice-of-app-deployment-platform-based-on-mixed-cloud?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/practice-of-app-deployment-platform-based-on-mixed-cloud?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/presentations/practice-of-app-deployment-platform-based-on-mixed-cloud/zh/mediumimage/zhaoming270-1531534624847.jpg"/><p>演讲包括项目痛点与用户诉求、基于混合云部署平台概览、混合云部署平台技术架构、基于 Kubernetes 容器云介绍（容器云架构设计、构建Docker镜像最佳实践、基于Helm的应用模板抽象、基于Kubernetes的 CI/CD）、应用在AWS上的EC2部署模块、应用在AWS上的K8s部署模块、基于Consul的混合云服务发现、系统集成自动化测试框架方案、混合云部署应用演示、后续工作计划展望</p> <i>By 赵明、张夏</i>
---------------
<h1 id="#title_5" >6、视频演讲： 基于多项目的离线缓存实现方案</h1>
刘弟新
[http://www.infoq.com/cn/presentations/an-offline-cache-implementation-scheme-based-on-multiple-projects?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/an-offline-cache-implementation-scheme-based-on-multiple-projects?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/presentations/an-offline-cache-implementation-scheme-based-on-multiple-projects/zh/mediumimage/liudixin270-1531482847000.jpg"/><p>海外多个项目因网络环境不乐观，导致离线缓存技术迫切需要应用。针对多项目特点，我们实现了离线缓存打包、更新、应用等方案，本次演讲将分享：

1、为什么需要离线缓存？
2、离线缓存的方案介绍。
3、项目离线缓存方案设计。
4、我们遇到了哪些问题?如何实现解决？   </p> <i>By 刘弟新</i>
---------------
<h1 id="#title_6" >7、视频演讲： 百度AIOps实践</h1>
哈晶晶
[http://www.infoq.com/cn/presentations/baidu-aiops-practice?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/baidu-aiops-practice?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/presentations/baidu-aiops-practice/zh/mediumimage/hajingjing270-1531486701590.jpg"/><p>百度运维经历了脚本&工具、基础运维平台、开放运维平台阶段，在2014年开始智能化运维的探索，并且围绕可用性、成本和效率方向的运维目标，在诸多运维场景落地。本次分享将以百度故障处理场景为例，介绍百度故障发现的异常检测、故障通告的智能报警合并、故障诊断阶段的多维度分析，故障止损阶段的自愈方案等，以及百度AIOps研发框架如何支持诸多运维场景的快速落地。</p> <i>By 哈晶晶</i>
---------------
<h1 id="#title_7" >8、文章： 现代存储系统背后的算法</h1>
Alex Petrov
[http://www.infoq.com/cn/articles/algorithms-behind-modern-storage-systems?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/algorithms-behind-modern-storage-systems?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/algorithms-behind-modern-storage-systems/zh/smallimage/GettyImages-609711710-copy-1508960432386-1531761738982.jpeg"/><p>本文详细剖析了两种被大多数现代数据库使用的存储系统设计方法，即针对读操作优化的B树，以及针对写操作优化的LSM树，并介绍了两种方法的一些用例和权衡考虑。</p> <i>By Alex Petrov</i> <i> Translated by 盖磊</i>
---------------
<h1 id="#title_8" >9、盲目跟风还是无动于衷？这篇文章彻底治愈区块链学习焦虑症！</h1>
陈卢浩
[http://www.infoq.com/cn/news/2018/07/block-chain-learning?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/block-chain-learning?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>针对区块链技术，对当今世界产生的巨大革命性变化，行业从业者应该如何了解、学习这项崭新技术？应该如何针对自身业务，将已掌握的区块链技术知识转化为具备应用价值的解决方案？本文将从行业人才观点和具体技术的角度出发，系统的描述区块链技术的前景、观点及应用。</p> <i>By 陈卢浩</i>
---------------
<h1 id="#title_9" >10、新CIO：Mark Schwartz认为的领先IT</h1>
Helen Beal
[http://www.infoq.com/cn/news/2018/07/new-CIO-leading-Mark-Schwartz?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/new-CIO-leading-Mark-Schwartz?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>美国公民及移民服务局前任CIO，现任AWS企业战略师Mark Schwartz在伦敦举行的DevOps企业峰会上介绍了什么是领先的IT。</p> <i>By Helen Beal</i> <i> Translated by 刘嘉洋</i>
---------------
<h1 id="#title_10" >11、在首次发布三周之后，MLflow迎来了0.2版本</h1>
Matei Zaharia, Mani Parkhe
[http://www.infoq.com/cn/news/2018/07/MLflow-02?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/MLflow-02?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>在今年的Spark+AI峰会上，MLflow团队推出了MLflow，一个开源的用于简化机器学习生命周期的平台。从首次发布到现在的三周时间里，已经有很多数据科学家和工程师对使用MLflow和为MLflow贡献代码感兴趣。MLFlow的GitHub仓库已经有180个分支，其中有十几个贡献者提交了问题和拉取请求。此外，上周参加由该团队举办的第一次MLflow聚会的人数接近100人。

昨天，该团队正式宣布推出MLflow 0.2版本，这一版本包含了由内部客户和开源用户提出的一些最被期待的功能。按照MLflow快速入门指南给出的提示，可以使用pip install mlflow来安装MLflow 0.2。以下内容将介绍该版本的主要新功能。</p> <i>By Matei Zaharia</i> <i> Translated by 悟明</i>
---------------
<h1 id="#title_11" >12、ESLint的NPM账户遭黑客攻击，可能窃取用户NPM访问令牌</h1>
覃云
[http://www.infoq.com/cn/news/2018/07/ESLint-NPMAccount-hacked?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/ESLint-NPMAccount-hacked?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>7月12日，黑客攻击了ESLint维护者的NPM帐户，并将带有病毒的eslint-scope和eslint-config-eslint软件包发布到NPM注册表中。带有恶意病毒的软件包在安装时，计算机会自动下载并执行pastebin.com代码，然后将含有NPM访问令牌的.npmrc文件内容发送给攻击者。</p> <i>By 覃云</i>
---------------
<h1 id="#title_12" >13、Facebook使用机器学习手段来自动优化其系统性能</h1>
VLADIMIR BYCHKOVSKY 等
[http://www.infoq.com/cn/news/2018/07/facebook-opt-machinelearning?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/facebook-opt-machinelearning?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>在 Facebook 数十亿用户眼里，Facebook 的服务看起来就像是一个统一的移动 App 或网站。但从公司内部看，却有着不同的视角。Facebook 提供了数千种服务，功能包罗万象，从均衡互联网流量到转码图像，再到提供可靠的存储。Facebook 的整体效率是各项服务效率的总和，而其中的每项服务通常都有自己的优化方式，这些方式难以进行泛化或适应款速变化的节奏。</p> <i>By VLADIMIR BYCHKOVSKY 等</i> <i> Translated by 悟明</i>
---------------
<h1 id="#title_13" >14、文章： 戳破泡沫，人工智能应该这样看！</h1>
George Krasadakis
[http://www.infoq.com/cn/articles/ai-beyond-the-hype?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/ai-beyond-the-hype?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/ai-beyond-the-hype/zh/smallimage/logo232-1531758824570.jpeg"/><p>穿透迷雾，看清人工智能时代的未来。</p> <i>By George Krasadakis</i> <i> Translated by 刘志勇</i>
---------------
<h1 id="#title_14" >15、文章： GitHub的MySQL高可用性实践</h1>
Shlomi Noach
[http://www.infoq.com/cn/articles/mysql-high-availability-at-github?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/mysql-high-availability-at-github?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/mysql-high-availability-at-github/zh/smallimage/GettyImages-628837052-1518704902676-1531564941674.jpeg"/><p>本文阐述了GitHub的MySQL高可用性和主服务发现解决方案，这个方案使得我们能够可靠地进行跨数据中心运维、克服数据中心隔离的影响并实现故障时的短宕机时间。</p> <i>By Shlomi Noach</i> <i> Translated by 张健欣</i>
---------------