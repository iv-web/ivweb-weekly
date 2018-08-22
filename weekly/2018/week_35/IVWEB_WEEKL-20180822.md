## 文章索引
1、 <a href="#1文章-前端性能之javascript成本2018版" >文章： 前端性能之JavaScript成本2018版</a><br/>
2、 <a href="#2onboarding-users-of-your-product:-from-trial-to-payment" >Onboarding Users Of Your Product: From Trial To Payment</a><br/>
3、 <a href="#3文章-通俗易懂图解kubernetes" >文章： 通俗易懂图解Kubernetes</a><br/>
4、 <a href="#4文章-协作是持续测试的关键推动力" >文章： 协作是持续测试的关键推动力</a><br/>
5、 <a href="#5文章-kafka实践到底该不该把不同类型的消息放在同一个主题中" >文章： Kafka实践：到底该不该把不同类型的消息放在同一个主题中</a><br/>
6、 <a href="#6专访网易云陈谔用微服务体系满足数字化转型需求" >专访网易云陈谔：用微服务体系满足数字化转型需求</a><br/>
7、 <a href="#7netbeans在apache基金会取得的进展" >NetBeans在Apache基金会取得的进展</a><br/>
8、 <a href="#8android-pie提供了自适应供电神经网络api-11等新特性" >Android Pie提供了自适应供电、神经网络API 1.1等新特性</a><br/>
9、 <a href="#9microsoft宣布正式发布linux-on-ase" >Microsoft宣布正式发布Linux on ASE</a><br/>
10、 <a href="#10微服务通信策略" >微服务通信策略</a><br/><h1 id="#title_0" >1、文章： 前端性能之JavaScript成本2018版</h1>
Addy Osmani
[http://www.infoq.com/cn/articles/the-cost-of-javascript-in-2018?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/the-cost-of-javascript-in-2018?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/the-cost-of-javascript-in-2018/zh/smallimage/agile-reflective-practice-logo-1533075201973-1534613554799.jpeg"/><p>构建交互式网站通常涉及向用户发送大量的JavaScript代码。JavaScript是我们向手机端发送的最昂贵的资源，因为在很大程度上，它们会增加交互延迟。在这篇文章中，我们将介绍一些策略，用于在保持良好用户体验的前提下更高效地发送JavaScript。</p> <i>By Addy Osmani</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_1" >2、Onboarding Users Of Your Product: From Trial To Payment</h1>
Joe Leech
[https://www.smashingmagazine.com/2018/08/ux-lifecycle-activating-users/](https://www.smashingmagazine.com/2018/08/ux-lifecycle-activating-users/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/08/ux-lifecycle-activating-users/" />
              <title>Onboarding Users Of Your Product: From Trial To Payment</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>Onboarding Users Of Your Product: From Trial To Payment</h1>
                  
                    
                    <address>Joe Leech</address>
                  
                  <time datetime="2018-08-21T14:20:21&#43;02:00" class="op-published">2018-08-21T14:20:21+02:00</time>
                  <time datetime="2018-08-21T13:33:03&#43;00:00" class="op-modified">2018-08-21T13:33:03+00:00</time>
                </header>
                <p>(<em>This is a sponsored article</em>.) In  of this series, we looked at the <em>Attraction</em> phase of the customer lifecycle. This three-part series outlines the three phases of the product lifecycle, the future for UX, and the skills and approach you’ll need to design modern digital products.</p>

<ul>
<li><strong>Part 1: Attraction</strong><br />Going out there to get users to evaluate your product.</li>
<li><strong>Part 2: Activation</strong><br />Signing up, onboarding users, asking for payment.</li>
<li><strong>Part 3: Retention</strong><br />Encouraging users to come back and keep using and paying for your product.</li>
</ul>

<h3>Part Two: Activation</h3>

<h4>Plotting Out The Journey</h4>

<p>When we talk about the <em>Attraction</em> phase, we’re talking about users discovering they have a need, discovering our product and visiting our website to see if our product meets their needs.</p>

<p>Within the lifecycle, we can split the larger three phases into smaller phases to help us plan our approach. In this case, we can use Philip Kotler's model (expanded to 6 steps by Bryony Thomas).</p>

<ul>
<li><strong>Awareness</strong><br />Realizing they have a need.</li>
<li><strong>Interest</strong><br />Looking for something to help with that need.</li>
<li><strong>Evaluation</strong><br />Looking at products that help with their need.</li>
<li><strong>Trial</strong><br />Trying the product to see if it meets their need.</li>
<li><strong>Adoption</strong><br />Choosing a product and using it for a while.</li>
<li><strong>Loyalty</strong><br />Deciding to stay using the product or switch to a different one.</li>
</ul>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d3e866bb-dd69-4a87-9c9a-b71374025cc4/the-ux-lifecycle-activating-users-4.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d3e866bb-dd69-4a87-9c9a-b71374025cc4/the-ux-lifecycle-activating-users-4.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d3e866bb-dd69-4a87-9c9a-b71374025cc4/the-ux-lifecycle-activating-users-4.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d3e866bb-dd69-4a87-9c9a-b71374025cc4/the-ux-lifecycle-activating-users-4.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d3e866bb-dd69-4a87-9c9a-b71374025cc4/the-ux-lifecycle-activating-users-4.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d3e866bb-dd69-4a87-9c9a-b71374025cc4/the-ux-lifecycle-activating-users-4.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d3e866bb-dd69-4a87-9c9a-b71374025cc4/the-ux-lifecycle-activating-users-4.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<p>We’re interested in the middle two parts that fall under the <em>Acquisition</em> phase.</p>

<p>In , we looked at the <em>Evaluation</em> phase. The user is now ready to sign up and get going with our product; we used the example of the money management app:</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/41910c07-4640-4b2d-8e94-107748ec98b6/the-ux-lifecycle-activating-users-3.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/41910c07-4640-4b2d-8e94-107748ec98b6/the-ux-lifecycle-activating-users-3.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/41910c07-4640-4b2d-8e94-107748ec98b6/the-ux-lifecycle-activating-users-3.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/41910c07-4640-4b2d-8e94-107748ec98b6/the-ux-lifecycle-activating-users-3.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/41910c07-4640-4b2d-8e94-107748ec98b6/the-ux-lifecycle-activating-users-3.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/41910c07-4640-4b2d-8e94-107748ec98b6/the-ux-lifecycle-activating-users-3.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/41910c07-4640-4b2d-8e94-107748ec98b6/the-ux-lifecycle-activating-users-3.png"
			sizes="100vw"
			alt="Homepage showing what our app does."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Homepage showing what our app does. ()
		</figcaption>
	
</figure>


<p>Let’s take that app forward into the <em>Acquisition</em> phase of the lifecycle.</p>

<h3>A. Trial/Onboarding</h3>

<p>In the <em>Trial</em> phase, our user is going to sign up and see if it is the product for them.</p>

<p>The first challenge is to onboard the user. Onboarding is a real challenge as it can be complex, involving the user entering personal information as well as getting to grips with what the product does. There is a huge potential for users to drop out and leave.</p>

<p>Joshua Porter sums it up:</p>

<blockquote>“Onboarding should not be a separate function/consideration/afterthought. It should be an initial (and primary) focus of design.”<br /><br />&mdash; </blockquote>

<p>So with that in mind, let’s take a look at onboarding.</p>

<h4>Onboarding: Steady Progress Showing Value</h4>

<p>For our money management app to work well we need for our user we need to accomplish three goals:</p>

<ol>
<li><strong>Collect some personal data from our users.</strong><br />Who they are (including email, mobile phone number, etc.).</li>
<li><strong>Bank account access, to auto pull in transactions.</strong><br />As we’re in the EU,  mean that all banks have to provide API access to transaction data.</li>
<li><strong>Familiarize them with the product.</strong></li>
</ol>

<p>That’s a big ask. Let’s think about how we can soften that. We need a simple hook to get started. We use a concept in psychology called ‘.’ We ask for a low commitment to the product and then when the user gets something in return was ask for more.</p>

<p>We ask the simple question, “How much do you think you spend on coffee a month?”</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d83dcc21-8afc-4eba-95ee-793dde57e243/the-ux-lifecycle-activating-users-6.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d83dcc21-8afc-4eba-95ee-793dde57e243/the-ux-lifecycle-activating-users-6.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d83dcc21-8afc-4eba-95ee-793dde57e243/the-ux-lifecycle-activating-users-6.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d83dcc21-8afc-4eba-95ee-793dde57e243/the-ux-lifecycle-activating-users-6.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d83dcc21-8afc-4eba-95ee-793dde57e243/the-ux-lifecycle-activating-users-6.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d83dcc21-8afc-4eba-95ee-793dde57e243/the-ux-lifecycle-activating-users-6.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d83dcc21-8afc-4eba-95ee-793dde57e243/the-ux-lifecycle-activating-users-6.png"
			sizes="100vw"
			alt="A simple question to get started"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			A simple question to get started. ()
		</figcaption>
	
</figure>


<p>This can be done along with a hook to encourage people to compare their spend to others. There’s now a quick, easy win for the user.</p>

<p>We give something back, in this case comparing to the average. Then, we ask the next question.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8ba99bf8-59c4-4976-8c49-65844fde52fb/the-ux-lifecycle-activating-users-5.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8ba99bf8-59c4-4976-8c49-65844fde52fb/the-ux-lifecycle-activating-users-5.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8ba99bf8-59c4-4976-8c49-65844fde52fb/the-ux-lifecycle-activating-users-5.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8ba99bf8-59c4-4976-8c49-65844fde52fb/the-ux-lifecycle-activating-users-5.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8ba99bf8-59c4-4976-8c49-65844fde52fb/the-ux-lifecycle-activating-users-5.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8ba99bf8-59c4-4976-8c49-65844fde52fb/the-ux-lifecycle-activating-users-5.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8ba99bf8-59c4-4976-8c49-65844fde52fb/the-ux-lifecycle-activating-users-5.png"
			sizes="100vw"
			alt="incremental commitment in action. We ask a follow-up."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Incremental commitment in action. We ask a follow-up. ()
		</figcaption>
	
</figure>


<p>It allows us to build trust, and for the user to get value from our product early.</p>

<p>Next, the big ask. We want bank account access. If we’d asked for this early, we’d see a larger dropout. But we now have built some trust, and our user is invested in the product.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9dc72281-0aa1-450c-8fbd-0d5c68edda63/the-ux-lifecycle-activating-users-7.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9dc72281-0aa1-450c-8fbd-0d5c68edda63/the-ux-lifecycle-activating-users-7.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9dc72281-0aa1-450c-8fbd-0d5c68edda63/the-ux-lifecycle-activating-users-7.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9dc72281-0aa1-450c-8fbd-0d5c68edda63/the-ux-lifecycle-activating-users-7.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9dc72281-0aa1-450c-8fbd-0d5c68edda63/the-ux-lifecycle-activating-users-7.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9dc72281-0aa1-450c-8fbd-0d5c68edda63/the-ux-lifecycle-activating-users-7.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9dc72281-0aa1-450c-8fbd-0d5c68edda63/the-ux-lifecycle-activating-users-7.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<p>We then go for the big ask, granting bank access. As you can see, we are gently guiding our user through the onboarding, showing useful content at each step, trying to make it feel natural.</p>

<p>Asking for what could be challenging data like the mobile phone number is much easier if we offer context and say what benefit there is to the user. We could include the following on the sign-up page asking for the mobile number.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/46906782-4d35-4176-a4c9-88a2ef961c30/the-ux-lifecycle-activating-users-1.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/46906782-4d35-4176-a4c9-88a2ef961c30/the-ux-lifecycle-activating-users-1.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/46906782-4d35-4176-a4c9-88a2ef961c30/the-ux-lifecycle-activating-users-1.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/46906782-4d35-4176-a4c9-88a2ef961c30/the-ux-lifecycle-activating-users-1.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/46906782-4d35-4176-a4c9-88a2ef961c30/the-ux-lifecycle-activating-users-1.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/46906782-4d35-4176-a4c9-88a2ef961c30/the-ux-lifecycle-activating-users-1.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/46906782-4d35-4176-a4c9-88a2ef961c30/the-ux-lifecycle-activating-users-1.png"
			sizes="100vw"
			alt="showing how giving us your mobile number adds value "
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Showing how giving us your mobile number adds value. ()
		</figcaption>
	
</figure>


<p>We can then ask further questions, like email and for a password which will have less impact being asked later after we’ve shown value.</p>

<p>Interaction by interaction we’re asking a question, gathering some data and showing how the product works.</p>

<h4>Things To Avoid During Onboarding</h4>

<p>There are other pitfalls to designing a product onboarding flow.</p>

<ul>
    <li>, Registration is a meaningless concept, offer a reason for why you are asking for a pieces of information.</li>
    <li>Similarly don’t ask too many questions, that might sound obvious, but the more you ask the more likely it is for users to drop out.</li>
    <li>Answer these three simple questions when it comes to form fields:</li>
    <ul>
        <li>Why are you asking the question?</li>
        <li>What will you use the data for?</li>
        <li>What value does the user get from giving us this data?</li>
    </ul>
    <li>. Plus, they aren’t very friendly.</li>
    <li>And, of course, if your users are located in the EU, you need to .</li>
</ul>

<h3>B. Adoption</h3>

<p>Onboarding doesn’t end when the user has signed up. This is a common mistake made by organizations big and small. “Great, our new registrations are up month on month. But our retention rate is really poor” is a common problem.</p>

<p>We need to support our users through the first few weeks and months of using our app. We need to give them a reason to come back to us.</p>

<p>In , we talked about SEO and Marketing skills and tools we can use to improve the experience.</p>

<p>We’ll be expanding our skill set to look at email, and how we can improve the email experience. To encourage product adoption, we need to understand and map the email user journey.</p>

<p>Any modern UX or product designer needs to know how to design multi-channel experiences, and after the product itself email is the most important.</p>

<h4>Planning And Encouraging The Second Visit</h4>

<p>For our money management app we have access to the users' bank transaction data. Rather than hoping they return to our app, we need to reach out and give them a reason to come back.</p>

<h4>The pull: using email to get users to come back to our app</h4>

<p>Let’s look at an email we can send them the next day. But before we do that, let’s look back at one question we asked users:</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d83dcc21-8afc-4eba-95ee-793dde57e243/the-ux-lifecycle-activating-users-6.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d83dcc21-8afc-4eba-95ee-793dde57e243/the-ux-lifecycle-activating-users-6.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d83dcc21-8afc-4eba-95ee-793dde57e243/the-ux-lifecycle-activating-users-6.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d83dcc21-8afc-4eba-95ee-793dde57e243/the-ux-lifecycle-activating-users-6.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d83dcc21-8afc-4eba-95ee-793dde57e243/the-ux-lifecycle-activating-users-6.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d83dcc21-8afc-4eba-95ee-793dde57e243/the-ux-lifecycle-activating-users-6.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d83dcc21-8afc-4eba-95ee-793dde57e243/the-ux-lifecycle-activating-users-6.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Notice that the ‘on coffee’ can be changed for other spending items. ()
		</figcaption>
	
</figure>


<p>The user could have changed ‘on coffee’ to be ‘at Restaurants’ or ‘at Amazon’ or another discretionary purchase option.</p>

<p>This is a tiny piece of personalization, and the best follow-up emails are personalized.</p>

<p>When designing an email the most important element is the subject line. A good subject line encourages the user to open it.</p>

<p>Let’s look at the most common email provider of them all, Gmail. Like we did in  when designing Facebook ads, we’ll design in context, in this case the crowded inbox. Actually, the promotions inbox on Gmail.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5835f8d6-4b40-40ff-aebc-70ed831511d1/the-ux-lifecycle-activating-users-8.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5835f8d6-4b40-40ff-aebc-70ed831511d1/the-ux-lifecycle-activating-users-8.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5835f8d6-4b40-40ff-aebc-70ed831511d1/the-ux-lifecycle-activating-users-8.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5835f8d6-4b40-40ff-aebc-70ed831511d1/the-ux-lifecycle-activating-users-8.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5835f8d6-4b40-40ff-aebc-70ed831511d1/the-ux-lifecycle-activating-users-8.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5835f8d6-4b40-40ff-aebc-70ed831511d1/the-ux-lifecycle-activating-users-8.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5835f8d6-4b40-40ff-aebc-70ed831511d1/the-ux-lifecycle-activating-users-8.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			There’s one email in there that stands out, yes it’s us! ()
		</figcaption>
	
</figure>


<p>By referencing the Frotos we identified in  (Frotos: are the current bad state the user has and their wish for a new state. The From and the To, Froto) we should get a better open rate.</p>

<p>And yes, that is an emoji you see. Two in fact. 😜</p>

<p>This article is great at helping you decide if emojis are right for you:  as it has a lot of data.</p>

<p>TLDR, emojis can help boost open rates, and well...</p>

<p>What an emoji (in a subject line) does is one of two things:</p>

<ol>
<li>It makes a bad subject line worse;</li>
<li>Or it makes a good subject line better.</li>
</ol>

<p>We also need to think about other email design considerations:</p>

<ul>
<li>Preview text called ‘preheader’ (shown in grey) we need to design this content: .</li>
<li>Short emails work better. A short paragraph of text and one call to action: .</li>
<li>More great tips and advice for UX and optimizing email in this article: .</li>
</ul>

<p>Don’t forget to test your emails to make sure they look as designed &mdash;  is great at this.</p>

<h4>User Research And Email</h4>

<p>It’s a good idea to user research your emails, you’ll be surprised at what useful ideas you’ll get back. Using the emails as prompt material will encourage users to answer the question “What could you offer me that would make me come back to the app?”</p>

<h4>Drip, Drip, Drip That Email</h4>

<p>That’s email one done, great job! But now we need to think about an ongoing programme of emails. It takes a while to form a habit, and that’s what we’re after. Getting our users to keep coming back. It can take from  so we need to keep sending those emails.</p>

<p>These emails should offer value to our users. The key insights our product offers should be easy to deliver by email, SMS, or indeed any digital channel.</p>

<p>Our product promises a “Personalised Savings Plan” that’s what we need to deliver.</p> 

<p>The best performing products work seamlessly across digital channels.</p>

<p>To encourage product adoption and to help our user save we could offer SMS messages.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7042cd77-ef81-49f3-a52c-d7dce6f5a134/the-ux-lifecycle-activating-users-10.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7042cd77-ef81-49f3-a52c-d7dce6f5a134/the-ux-lifecycle-activating-users-10.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7042cd77-ef81-49f3-a52c-d7dce6f5a134/the-ux-lifecycle-activating-users-10.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7042cd77-ef81-49f3-a52c-d7dce6f5a134/the-ux-lifecycle-activating-users-10.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7042cd77-ef81-49f3-a52c-d7dce6f5a134/the-ux-lifecycle-activating-users-10.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7042cd77-ef81-49f3-a52c-d7dce6f5a134/the-ux-lifecycle-activating-users-10.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7042cd77-ef81-49f3-a52c-d7dce6f5a134/the-ux-lifecycle-activating-users-10.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<p>SMS is a neglected message format. Yes, it can be annoying if done badly, but it can equally be effective for our users.</p>

<p>Some :</p>

<ul>
<li>98% of text messages are read within 2 minutes;</li>
<li>Open rates are around 99% for text messages compared to 20% for email;</li>
<li>Click through rates are around 30% for SMS and less than 5% for email.</li>
</ul>

<p>That makes a compelling case for the effectiveness of SMS. Look at the success of startup  and learn more about how they use SMS.</p>

<p>We can encourage our user to save money by using SMS, sending an email once a day. A daily, personalized, money coach is a huge benefit to our user.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/46906782-4d35-4176-a4c9-88a2ef961c30/the-ux-lifecycle-activating-users-1.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/46906782-4d35-4176-a4c9-88a2ef961c30/the-ux-lifecycle-activating-users-1.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/46906782-4d35-4176-a4c9-88a2ef961c30/the-ux-lifecycle-activating-users-1.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/46906782-4d35-4176-a4c9-88a2ef961c30/the-ux-lifecycle-activating-users-1.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/46906782-4d35-4176-a4c9-88a2ef961c30/the-ux-lifecycle-activating-users-1.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/46906782-4d35-4176-a4c9-88a2ef961c30/the-ux-lifecycle-activating-users-1.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/46906782-4d35-4176-a4c9-88a2ef961c30/the-ux-lifecycle-activating-users-1.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<p>This article is a great for planning your messaging approach: .</p>

<p>Here’s some more great advice on planning email drip programmes:</p>

<ul>
<li></li>
<li></li>
</ul>

<h4>User Research And Email/SMS</h4>

<p>Researching the effectiveness of email and SMS is best done through AB testing. Testing different variants to see which performs better.</p>

<p>User research can help understand what content users will find useful and by what channel.</p>

<h4>The Secret To Onboarding And Adoption: It Takes Time</h4>

<p>Onboarding should be done gently, in short chunks offering value immediately. When it comes to asking for precious information like mobile phone number, bank account or email we need to demonstrate how we will deliver value.</p>

<p>To get a user to adopt our service takes time. We need to be able to deliver useful content over a long period of time to encourage them to keep using the product.</p>

<h4>Next Up, Retention</h4>

<p>In the  we talked about the beginnings of the customer journey how to attract or users.</p>

<p>Coming up next, we’ll talk about how to retain users and get them to pay for our product &mdash; that holy grail of our user taking out a monthly subscription. Stay tuned!</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dd5c7edb-485b-4384-99b5-a39d1b2a703a/the-ux-lifecycle-activating-users-2.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dd5c7edb-485b-4384-99b5-a39d1b2a703a/the-ux-lifecycle-activating-users-2.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dd5c7edb-485b-4384-99b5-a39d1b2a703a/the-ux-lifecycle-activating-users-2.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dd5c7edb-485b-4384-99b5-a39d1b2a703a/the-ux-lifecycle-activating-users-2.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dd5c7edb-485b-4384-99b5-a39d1b2a703a/the-ux-lifecycle-activating-users-2.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dd5c7edb-485b-4384-99b5-a39d1b2a703a/the-ux-lifecycle-activating-users-2.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dd5c7edb-485b-4384-99b5-a39d1b2a703a/the-ux-lifecycle-activating-users-2.png"
			sizes="100vw"
			alt="The parts of the user journey"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The parts of the user journey. ()
		</figcaption>
	
</figure>


<p><em>This article is part of the UX design series sponsored by Adobe. Adobe XD tool is made for a , and also sign up for the Adobe experience design newsletter to stay updated and informed on the latest trends and insights for UX/UI design.</em></p>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(ra, yk, il)</span>
</div>


              </article>
            </body>
          </html>
---------------
<h1 id="#title_2" >3、文章： 通俗易懂图解Kubernetes</h1>
Daniel Lebrero
[http://www.infoq.com/cn/articles/kubernetes-explained-in-pictures-the-theme-park-analogy?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/kubernetes-explained-in-pictures-the-theme-park-analogy?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/kubernetes-explained-in-pictures-the-theme-park-analogy/zh/smallimage/GettyImages-845809800-1524208773636-1534615233039.jpg"/><p>Kubernetes有自己的各种模型和术语，导致很多初学者在刚刚接触Kubernetes时，理解起来有很多的困难和障碍。本文将其类比为主题公园，配合生动形象的图片，通俗易懂地阐述了Kubernetes的基础理念和各个组成部分。</p> <i>By Daniel Lebrero</i> <i> Translated by 张卫滨 </i>
---------------
<h1 id="#title_3" >4、文章： 协作是持续测试的关键推动力</h1>
Alexander Mohr
[http://www.infoq.com/cn/articles/collaboration-continuous-testing?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/collaboration-continuous-testing?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/collaboration-continuous-testing/zh/smallimage/collaboration-continuous-testing-l-1533843564763-1534825500066.jpeg"/><p>成功的数字化转型的梦想往往会破坏有限的、以团队为中心的持续测试策略。本文描述了如何在敏捷团队层面以及整个企业层面应用测试、为什么协作是关键的推动因素，以及不同的测试技术如何协同工作以实现整体的成功。</p> <i>By Alexander Mohr</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_4" >5、文章： Kafka实践：到底该不该把不同类型的消息放在同一个主题中</h1>
Martin Kleppmann
[http://www.infoq.com/cn/articles/event-types-in-kafka-topic?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/event-types-in-kafka-topic?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/event-types-in-kafka-topic/zh/smallimage/image_fences-1534614905077.jpg"/><p>如果你使用了像Kafka这样的流式处理平台，就要搞清楚一件事情：你需要用到哪些主题？特别是如果你要将一堆不同的事件作为消息发布到Kafka，你是要将它们放在同一个主题中，还是将它们拆分到不同的主题中？</p> <i>By Martin Kleppmann</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_5" >6、专访网易云陈谔：用微服务体系满足数字化转型需求</h1>
张婵
[http://www.infoq.com/cn/news/2018/08/microservice-digital-transformat?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/08/microservice-digital-transformat?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>现在的公有云市场，国外有AWS，Google Cloud和微软的Azure三足鼎立，国内则是阿里云一家独大，即便如此，在数字化浪潮下，云计算市场依然有很多玩家进场，各家竞争也相当激烈。在这样的环境下，网易云作为入场较晚的选手（2016年“网易云”作为整体品牌正式推出），通过独特的玩法在这场角逐中占据了一定的席位。在7月31日的中国杭州云创大会上，InfoQ记者专访了网易云基础服务总经理陈谔，了解了网易云计算服务如何服务企业。</p> <i>By 张婵</i>
---------------
<h1 id="#title_6" >7、NetBeans在Apache基金会取得的进展</h1>
Ben Evans
[http://www.infoq.com/cn/news/2018/08/netbeans-apache-update-aug18?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/08/netbeans-apache-update-aug18?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>NetBeans在Apache基金会取得进展，包括发布了一个新的主要版本</p> <i>By Ben Evans</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_7" >8、Android Pie提供了自适应供电、神经网络API 1.1等新特性</h1>
Diogo Carleto
[http://www.infoq.com/cn/news/2018/08/android-pie?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/08/android-pie?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Google发布了Android Oreo的后继版本Android Pie。Android Pie提供了“刘海”屏显示支持（Display cutout）、神经网络API 1.1、放大镜组件、自适应供电（Adaptive Battery）、Slices、基于Wi-FI RTT的室内定位等一系列功能。</p> <i>By Diogo Carleto</i> <i> Translated by 盖磊</i>
---------------
<h1 id="#title_8" >9、Microsoft宣布正式发布Linux on ASE</h1>
Steef-Jan Wiggers
[http://www.infoq.com/cn/news/2018/08/ase-linux-azure?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/08/ase-linux-azure?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Microsoft宣布正式发布（GA）用于ASE（应用服务环境，App Service Environment）的Linux。该服务使客户可结合使用Linux上的应用服务（App Service）特性与ASE。在正式发布版之前，Microsoft曾于今年五月发布了支持客户在ASE中部署Linux和容器化应用的公开预览版。</p> <i>By Steef-Jan Wiggers</i> <i> Translated by 盖磊</i>
---------------
<h1 id="#title_9" >10、微服务通信策略</h1>
Jan Stenberg
[http://www.infoq.com/cn/news/2018/08/microservices-communication?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/08/microservices-communication?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>在GeeCON 2018大会上，Michael Plöd在一场介绍微服务之间不同的通信策略的演讲中解释说，在从单体架构迁移到微服务架构时，暗含在单体架构中的复杂性会明确显露出来，通信挑战将呈指数级增长。</p> <i>By Jan Stenberg</i> <i> Translated by 谢丽</i>
---------------