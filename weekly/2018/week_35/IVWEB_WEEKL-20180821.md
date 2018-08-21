## 文章索引
1、 <a href="#1ux-and-html5:-lets-help-users-fill-in-your-mobile-form-part-1" >UX And HTML5: Let’s Help Users Fill In Your Mobile Form (Part 1)</a><br/>
2、 <a href="#2文章-我用vue和react构建了相同的应用程序这是他们的差异" >文章： 我用Vue和React构建了相同的应用程序，这是他们的差异</a><br/>
3、 <a href="#3通过xaml-islands使windows桌面应用程序现代化" >通过XAML Islands使Windows桌面应用程序现代化</a><br/>
4、 <a href="#4文章-将web站点改造为渐进式web应用" >文章： 将Web站点改造为渐进式Web应用</a><br/>
5、 <a href="#5文章-苏宁mock测试桩服务建设实践" >文章： 苏宁MOCK测试桩服务建设实践</a><br/>
6、 <a href="#6微信的历史" >微信的历史</a><br/>
7、 <a href="#7最新版byte-buddy完全支持java-11" >最新版Byte Buddy完全支持Java 11</a><br/>
8、 <a href="#8rust-2018临近设法从rust-2015过渡" >Rust 2018临近：设法从Rust 2015过渡</a><br/>
9、 <a href="#9谷歌云平台发布edge-tpu和cloud-iot-edge" >谷歌云平台发布Edge TPU和Cloud IoT Edge</a><br/>
10、 <a href="#10保持分布式团队同步" >保持分布式团队同步</a><br/>
11、 <a href="#11文章-无服务器仍然离不开基础设施管理" >文章： 无服务器仍然离不开基础设施管理</a><br/><h1 id="#title_0" >1、UX And HTML5: Let’s Help Users Fill In Your Mobile Form (Part 1)</h1>
Stéphanie Walter
[https://www.smashingmagazine.com/2018/08/ux-html5-mobile-form-part-1/](https://www.smashingmagazine.com/2018/08/ux-html5-mobile-form-part-1/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/08/ux-html5-mobile-form-part-1/" />
              <title>UX And HTML5: Let’s Help Users Fill In Your Mobile Form (Part 1)</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>UX And HTML5: Let’s Help Users Fill In Your Mobile Form (Part 1)</h1>
                  
                    
                    <address>Stéphanie Walter</address>
                  
                  <time datetime="2018-08-20T13:45:31&#43;02:00" class="op-published">2018-08-20T13:45:31+02:00</time>
                  <time datetime="2018-08-20T18:56:09&#43;00:00" class="op-modified">2018-08-20T18:56:09+00:00</time>
                </header>
                

<p>Forms are one of the most basic primary interactions users will have with your websites (and mobile apps). They link people together and let them communicate. They let them comment on articles and explain to the author how they strongly disagree with what they’ve written. They let people chat directly on a dating app to meet &ldquo;the one&rdquo;. Whether for forums, product orders, online communities, account creation or online payment, forms are a big part of users’ online life.</p>

<p>It’s 2018, and <strong>we have more mobile than desktop users around the globe</strong>. Yet, we still treat those users as second-class citizens of the web. Everybody writes and speaks about user experience all the time. So, why, why, why are so many websites and products still doing it wrong. Why is their mobile user experience damaged for half of the world? Why is it still a pain, why is it still super-hard to book a flight and register an account in a mobile form today? Users expect better!</p>

<p><strong>Recommended reading</strong>: <em></em></p>

<p>This is the first part of a series of two articles. In this one, I will sum up some essential best practices to improve your mobile forms, including scannability and readability. I will guide you through label and input placement, size and optimization. We will see how to choose the right form element to reduce interaction costs. Finally, you will learn how to prevent and deal with errors on mobile forms.</p>

<p>In the second part, I will take a closer look at specific mobile capabilities and HTML5 form elements, and we will go beyond classic form elements to make unique and enjoyable web applications and websites.</p>

<p><strong>Note</strong>: <em>While most of the code enhancement in this article are web-related (because I don’t know Swift or Java), the usability best practices hold true for mobile applications</em>.</p>



<aside class="product-panel product-panel__tilted product-panel--book" data-audience="non-subscriber">
    <div class="container product-panel--book__container">
      <div class="panel__description panel__description--book">
    <p>Nope, we can't do any magic tricks, but we have articles,  get a seasoned selection of magic front-end tricks — e.g. <strong>live designing sessions</strong> and perf audits, too. <em>Just sayin'</em>! ;-)</p>

      <a href="http://smashed.by/perfpanelmembership" class="btn btn--green btn--large">
        Explore Smashing Wizardry&nbsp;→
      </a>
      </div>
      <div class="panel__image panel__image--book">
        <a href="http://smashed.by/perfpanelmembership" class="books__book__image">
        <div class="books__book__img">
          <img src="https://www.smashingmagazine.com/images/smashing-cat/cat-wizard.svg" alt="Smashing Cat, just preparing to do some magic stuff." width="310" height="400">
        </div>
      </a>
      </div>
    </div>
  </aside>




<h3 id="form-design-101-prioritizing-scannability-and-readability">Form Design 101: Prioritizing Scannability And Readability</h3>

<p>“A form is the name, value, pairs, in a structure for storing data on a computer barfed out as labels and input fields to human being.” This is a direct quote from  at a conference. Like him, I believe that most form usability issues come from this tendency to serve the structure of the database to users.</p>

<h4 id="strong-information-architecture">Strong Information Architecture</h4>

<p>To build better forms, you first need to take a few steps away from your database’s structure. Try to understand how users want to fill in forms. This is where doing some usability testing and user research on your forms becomes handy.  is a UX concept that can help you with that. Nielsen Norman Group describes it as &ldquo;what the user believes about the system at hand&rdquo;. Ask your tester to think aloud and tell you how they would fill the form. Which steps do they expect? What come first? What comes next? This will give you a better idea of how to structure your form in a more user-friendly way.</p>

<p>Visually grouping fields that belong together will also help users fill a form. In the code, use the  to group them programmatically. It will also help screen readers understand the hierarchy.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8b0867fa-770f-4a3c-aa76-43d5358fa278/making-mobile-form-experience-better-00-visually-group.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8b0867fa-770f-4a3c-aa76-43d5358fa278/making-mobile-form-experience-better-00-visually-group.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8b0867fa-770f-4a3c-aa76-43d5358fa278/making-mobile-form-experience-better-00-visually-group.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8b0867fa-770f-4a3c-aa76-43d5358fa278/making-mobile-form-experience-better-00-visually-group.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8b0867fa-770f-4a3c-aa76-43d5358fa278/making-mobile-form-experience-better-00-visually-group.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8b0867fa-770f-4a3c-aa76-43d5358fa278/making-mobile-form-experience-better-00-visually-group.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8b0867fa-770f-4a3c-aa76-43d5358fa278/making-mobile-form-experience-better-00-visually-group.jpg"
			sizes="100vw"
			alt="example of visually grouped forms"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Chunking information and grouping related pieces of information helps the human brain process this information in an easy, more readable way ()
		</figcaption>
	
</figure>


<p>If the form is long, <strong>don’t expose everything by default</strong>. Be smart about what you display. Use branching wisely to display only the fields that people need. In a checkout form, for example, don’t display all of the detailed fields for all of the shipment options. This will overwhelm the user. Display enough information to help them choose the right shipment option. Then, display only the details and fields related to that choice.</p>

<p>User attention spans get shorter with time: <strong>Ask for optional things at the end</strong> of the form. For instance, if your form is a customer-satisfaction survey, ask for demographic information at the end. Better yet, auto-fill them, if possible. Ask users only for what’s necessary.</p>

<p>Finally, plan ahead for localization: What will happen when your form gets translated? What will happen, say, for German? Will your design still work?</p>

<h4 id="label-placement-and-input-optimization">Label Placement And Input Optimization</h4>

<h5 id="single-column-layout-works-best">Single-Column Layout Works Best</h5>

<p>Due to the lack of space, you don’t get endless options for placing labels and fields on mobile screens:</p>

<ul>
<li>Present fields in a <strong>single-column layout</strong>. There’s no room on mobile for multiple columns. Multi-columns forms are not a great idea on desktop either anyway.</li>
<li>In portrait mode, it’s better to place the <strong>label on top of the field</strong> so that users can see what’s in the field when they type.</li>
</ul>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fce1568a-073d-44eb-b974-6704664e1beb/making-mobile-form-experience-better-01-label-top.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fce1568a-073d-44eb-b974-6704664e1beb/making-mobile-form-experience-better-01-label-top.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fce1568a-073d-44eb-b974-6704664e1beb/making-mobile-form-experience-better-01-label-top.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fce1568a-073d-44eb-b974-6704664e1beb/making-mobile-form-experience-better-01-label-top.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fce1568a-073d-44eb-b974-6704664e1beb/making-mobile-form-experience-better-01-label-top.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fce1568a-073d-44eb-b974-6704664e1beb/making-mobile-form-experience-better-01-label-top.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fce1568a-073d-44eb-b974-6704664e1beb/making-mobile-form-experience-better-01-label-top.jpg"
			sizes="100vw"
			alt="portrait mode"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			In portrait mode, it’s better to put the label on top of the field. ()
		</figcaption>
	
</figure>


<ul>
<li>In landscape mode, the screen’s height is reduced. You might want to put <strong>labels on the left and inputs on the right</strong>. But test it to make sure it works.</li>
</ul>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/380a603f-8790-4d77-8071-66fb56c11258/making-mobile-form-experience-better-02-label-landascape.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/380a603f-8790-4d77-8071-66fb56c11258/making-mobile-form-experience-better-02-label-landascape.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/380a603f-8790-4d77-8071-66fb56c11258/making-mobile-form-experience-better-02-label-landascape.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/380a603f-8790-4d77-8071-66fb56c11258/making-mobile-form-experience-better-02-label-landascape.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/380a603f-8790-4d77-8071-66fb56c11258/making-mobile-form-experience-better-02-label-landascape.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/380a603f-8790-4d77-8071-66fb56c11258/making-mobile-form-experience-better-02-label-landascape.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/380a603f-8790-4d77-8071-66fb56c11258/making-mobile-form-experience-better-02-label-landascape.jpg"
			sizes="100vw"
			alt="landscape mode"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			In landscape mode, you want to put labels on the left and inputs on the right. ()
		</figcaption>
	
</figure>


<p>For more on label placement, see Baymard Institute’s &ldquo;&rdquo;.</p>

<h5 id="labels-should-be-clear-and-visible-and-work-without-context">Labels Should Be Clear And Visible And Work Without Context</h5>

<p>Remember that as soon as a field gets focus, the keyboard opens and will take at least one third of the screen’s area. On small mobile screens, users will also have to scroll to fill the form. This means that they will lose part of the context while filling the form. Plan accordingly:</p>

<ul>
<li>Your labels should be clear, visible text that can be read and understood without context. User should be able to complete each label and field pair as a separate task, even if they lose context.</li>
</ul>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/357da31e-fbc7-45c2-b509-0450230a75bf/making-mobile-form-experience-better-03-label-contexte.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/357da31e-fbc7-45c2-b509-0450230a75bf/making-mobile-form-experience-better-03-label-contexte.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/357da31e-fbc7-45c2-b509-0450230a75bf/making-mobile-form-experience-better-03-label-contexte.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/357da31e-fbc7-45c2-b509-0450230a75bf/making-mobile-form-experience-better-03-label-contexte.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/357da31e-fbc7-45c2-b509-0450230a75bf/making-mobile-form-experience-better-03-label-contexte.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/357da31e-fbc7-45c2-b509-0450230a75bf/making-mobile-form-experience-better-03-label-contexte.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/357da31e-fbc7-45c2-b509-0450230a75bf/making-mobile-form-experience-better-03-label-contexte.jpg"
			sizes="100vw"
			alt="labels should be clear"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Just “Address” without context is more complicated to process that “Shipping Address”. ()
		</figcaption>
	
</figure>


<ul>
<li>Avoid jargon, abbreviations and industry-specific language whenever you can.</li>
<li>Be consistent. If you use “customer” in a label once, stick with that word. Avoid using “clients” later because it might confuse users.</li>
<li>The font size should be big enough. Test your form on real devices as soon as possible, and adjust the size accordingly.</li>
<li>All-caps text can be hard to read for some users. You might want to avoid using all-caps text on labels.</li>
<li>The label copy should be short and scannable. If a field needs clarification, don’t put it in the label. Use a field description instead.</li>
</ul>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f3affa7d-f5ec-4ef6-aa41-10dbf14f2b07/04-making-mobile-form-experience-better-label-avoid.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f3affa7d-f5ec-4ef6-aa41-10dbf14f2b07/04-making-mobile-form-experience-better-label-avoid.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f3affa7d-f5ec-4ef6-aa41-10dbf14f2b07/04-making-mobile-form-experience-better-label-avoid.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f3affa7d-f5ec-4ef6-aa41-10dbf14f2b07/04-making-mobile-form-experience-better-label-avoid.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f3affa7d-f5ec-4ef6-aa41-10dbf14f2b07/04-making-mobile-form-experience-better-label-avoid.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f3affa7d-f5ec-4ef6-aa41-10dbf14f2b07/04-making-mobile-form-experience-better-label-avoid.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f3affa7d-f5ec-4ef6-aa41-10dbf14f2b07/04-making-mobile-form-experience-better-label-avoid.jpg"
			sizes="100vw"
			alt="Avoid full caps, jargon and very long labels."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Avoid full caps, jargon and very long labels. ()
		</figcaption>
	
</figure>


<h5 id="input-size-best-practice">Input Size Best Practice</h5>

<p>If possible, the <strong>size of the input element should match the size of the expected content</strong>. This will help users quickly fill in the form and understand what’s expected.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/58cbd16b-ab52-4a6d-9b3f-cd641b1ab92a/making-mobile-form-experience-better-05-size.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/58cbd16b-ab52-4a6d-9b3f-cd641b1ab92a/making-mobile-form-experience-better-05-size.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/58cbd16b-ab52-4a6d-9b3f-cd641b1ab92a/making-mobile-form-experience-better-05-size.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/58cbd16b-ab52-4a6d-9b3f-cd641b1ab92a/making-mobile-form-experience-better-05-size.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/58cbd16b-ab52-4a6d-9b3f-cd641b1ab92a/making-mobile-form-experience-better-05-size.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/58cbd16b-ab52-4a6d-9b3f-cd641b1ab92a/making-mobile-form-experience-better-05-size.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/58cbd16b-ab52-4a6d-9b3f-cd641b1ab92a/making-mobile-form-experience-better-05-size.jpg"
			sizes="100vw"
			alt="Properly sized inputs help the user scan the form and understand what is expected in the fields."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Properly sized inputs help the user scan the form and understand what is expected in the fields. ()
		</figcaption>
	
</figure>


<h4 id="using-masks-to-avoid-splitting-inputs-on-mobile">Using Masks To Avoid Splitting Inputs On Mobile</h4>

<p><strong>Don’t split inputs just for the sake of formatting</strong>. It’s especially annoying on mobile, where users can’t use the keyboard to navigate between fields. It requires extra taps just to go to the next field to fill in the form. You might be thinking, &ldquo;But I’ll automagically put the focus on the next field when I get the required number of characters in that field&rdquo;. That could work. But you will have taken control of the UI, which becomes unpredictable for the user. Also, it would be a pain if you automagically sent them to the next field and they needed to correct something in the last field. Finally, it’s more complicated to guess what’s mandatory with split inputs. So, let’s stop playing the “But what if” game and simply .</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b47c2cd8-509e-4dac-92b0-f67f09589892/making-mobile-form-experience-better-06-field-cut.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b47c2cd8-509e-4dac-92b0-f67f09589892/making-mobile-form-experience-better-06-field-cut.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b47c2cd8-509e-4dac-92b0-f67f09589892/making-mobile-form-experience-better-06-field-cut.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b47c2cd8-509e-4dac-92b0-f67f09589892/making-mobile-form-experience-better-06-field-cut.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b47c2cd8-509e-4dac-92b0-f67f09589892/making-mobile-form-experience-better-06-field-cut.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b47c2cd8-509e-4dac-92b0-f67f09589892/making-mobile-form-experience-better-06-field-cut.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b47c2cd8-509e-4dac-92b0-f67f09589892/making-mobile-form-experience-better-06-field-cut.jpg"
			sizes="100vw"
			alt="Don’t split the phone number into many little inputs."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Don’t split the phone number into many little inputs. ()
		</figcaption>
	
</figure>


<p>I get it: You still want to be able to format your user’s data in small pieces to help them fill in your fields. And you are perfectly right about that. To do so, you could <strong>use masks</strong>. Instead of splitting an input, just put a mask on top of it, to visually help the user fill it. Here is a video example of what a mask would look like to help users fill in a credit-card field:</p>

<figure class="video-container"><iframe data-src="https://player.vimeo.com/video/285089997" width="600" height="480" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe></figure>

<p>Masks help to <strong>prevent errors by guiding users</strong> to the correct format. Avoid gradually revealing them &mdash; show the format directly. Also, <strong>avoid putting fake values in the mask</strong>. Users might think it’s already filled. That’s why I’ve replaced the numbers with a little “X” in my demo. Find what works best for your type of input.</p>

<p>Finally, remember that some data can vary between countries, and sometimes the format changes, too (phone numbers, for example). Plan accordingly.</p>

<h4 id="efficient-fields-descriptions">Efficient Fields Descriptions</h4>

<p>Displaying efficient field descriptions can make the difference between a seamless and a painful form experience.</p>

<h5 id="what-can-descriptions-be-used-for">What Can Descriptions Be Used For?</h5>

<p>Descriptions can help users in so many ways. Here are a few examples.</p>

<ul>
    <li><strong>What Exactly Are You Asking For?</strong><br /><p>For whatever database-related reason, some shipment companies ask for "Address 1" and “Address 2” fields. This is highly confusing for users, but you might not have a choice here. Add description fields to help users understand what they need to put in each field.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0757a18b-94f8-4b02-9d1d-3f6bb5c49a74/07-making-mobile-form-experience-better-description-inline.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0757a18b-94f8-4b02-9d1d-3f6bb5c49a74/07-making-mobile-form-experience-better-description-inline.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0757a18b-94f8-4b02-9d1d-3f6bb5c49a74/07-making-mobile-form-experience-better-description-inline.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0757a18b-94f8-4b02-9d1d-3f6bb5c49a74/07-making-mobile-form-experience-better-description-inline.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0757a18b-94f8-4b02-9d1d-3f6bb5c49a74/07-making-mobile-form-experience-better-description-inline.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0757a18b-94f8-4b02-9d1d-3f6bb5c49a74/07-making-mobile-form-experience-better-description-inline.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0757a18b-94f8-4b02-9d1d-3f6bb5c49a74/07-making-mobile-form-experience-better-description-inline.jpg"
			sizes="100vw"
			alt="Inline descriptions help users understand why you need this information."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Inline descriptions help users understand why you need this information. ()
		</figcaption>
	
</figure>


<p>The same goes for acronyms and abbreviations. I know I said that you should avoid them, but sometimes you can’t. If you work on complex forms for a particular industry, for instance, they might have their own set of abbreviations. Any new user who needs to fill in the form might not be familiar (yet) with those abbreviations. Having a description available somewhere will help them.</p></li>
<li><strong>Why Do You Need This Information?</strong><br />Users might be reluctant to give you personal information if they don’t understand <strong>why you need it</strong> and <strong>what you will do with it</strong>. But sometimes you still need to ask for such information for legal reasons (like date of birth for a website that sells alcohol). Using field descriptions here will help users understand why this kind of information is needed.<br /><br /><p>On e-commerce websites, you might want to ask for the user’s phone number in case the delivery person needs to contact them. This is a legitimate reason. So, again, use descriptions to explain to e-commerce users why you need their phone number.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a4d2a9ab-7a22-4959-bbbd-29d230606659/making-mobile-form-experience-better-08-description-age-phone.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a4d2a9ab-7a22-4959-bbbd-29d230606659/making-mobile-form-experience-better-08-description-age-phone.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a4d2a9ab-7a22-4959-bbbd-29d230606659/making-mobile-form-experience-better-08-description-age-phone.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a4d2a9ab-7a22-4959-bbbd-29d230606659/making-mobile-form-experience-better-08-description-age-phone.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a4d2a9ab-7a22-4959-bbbd-29d230606659/making-mobile-form-experience-better-08-description-age-phone.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a4d2a9ab-7a22-4959-bbbd-29d230606659/making-mobile-form-experience-better-08-description-age-phone.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a4d2a9ab-7a22-4959-bbbd-29d230606659/making-mobile-form-experience-better-08-description-age-phone.jpg"
			sizes="100vw"
			alt="Sometimes you need information for legal or practical reasons. Again, tell the user why."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Sometimes you need information for legal or practical reasons. Again, tell the user why. ()
		</figcaption>
	
</figure>

</li>
<lo><strong>“Where Do I Find the Information?”</strong><br />If your users need to find certain information somewhere else in order to fill a form, tell them where to find it. I worked on a mobile app that lets user track their house. Users needed to pair the app to the monitoring device using a serial number. It’s not very easy to find this serial number on the device; it requires some instruction. We added a little <kbd>?</kbd> button next to the serial number field. The button opens a modal that shows a picture and some indication to help the user understand where to find the serial number on the monitoring device.  
E-commerce websites do the same with promo codes: They give indicators that tell users where to find the codes.











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ce030b6d-1481-4443-aa1b-d51e1e05f7bc/making-mobile-form-experience-better-09-description-find-info.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ce030b6d-1481-4443-aa1b-d51e1e05f7bc/making-mobile-form-experience-better-09-description-find-info.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ce030b6d-1481-4443-aa1b-d51e1e05f7bc/making-mobile-form-experience-better-09-description-find-info.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ce030b6d-1481-4443-aa1b-d51e1e05f7bc/making-mobile-form-experience-better-09-description-find-info.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ce030b6d-1481-4443-aa1b-d51e1e05f7bc/making-mobile-form-experience-better-09-description-find-info.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ce030b6d-1481-4443-aa1b-d51e1e05f7bc/making-mobile-form-experience-better-09-description-find-info.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ce030b6d-1481-4443-aa1b-d51e1e05f7bc/making-mobile-form-experience-better-09-description-find-info.jpg"
			sizes="100vw"
			alt="Users can tap to open a pop-up in which they can find extra information to help them fill in the field"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Users can tap on the link (left) or the question mark (right) to open a popup where they can find extra information to help them fill in the field. ()
		</figcaption>
	
</figure>

</lo>
<li><strong>“How Should I Format The Information?”</strong><br />Some fields need a <strong>particular format</strong>. In this case, use descriptions to let users know the formatting rules up front. Here are a few examples:
    <ul>
        <li>Phone number: do I need to put the international dialing code (+xx) in front of the field?</li>
        <li>Is there a maximum length? Twitter on mobile does a good job with that one.</li>
        <li>When dealing with monetary amounts, is the format with comma (like 10,000) or a space (like 10 000)?</li>
        <li>What format do you expect for dates? I’ll let you . The difference between DD MM YY and MM DD YY can cause a *lot* of trouble to users when booking online.</li>
    </ul>
Note that a lot of those formatting issues can be solved by input masks. We will come to that later in the article (or you can jump right in if you are impatient).











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c2a623db-3bfa-4511-9d8d-ca6324f5bff4/making-mobile-form-experience-better-10-description-format.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c2a623db-3bfa-4511-9d8d-ca6324f5bff4/making-mobile-form-experience-better-10-description-format.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c2a623db-3bfa-4511-9d8d-ca6324f5bff4/making-mobile-form-experience-better-10-description-format.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c2a623db-3bfa-4511-9d8d-ca6324f5bff4/making-mobile-form-experience-better-10-description-format.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c2a623db-3bfa-4511-9d8d-ca6324f5bff4/making-mobile-form-experience-better-10-description-format.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c2a623db-3bfa-4511-9d8d-ca6324f5bff4/making-mobile-form-experience-better-10-description-format.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c2a623db-3bfa-4511-9d8d-ca6324f5bff4/making-mobile-form-experience-better-10-description-format.jpg"
			sizes="100vw"
			alt="In the old 180-character days, Twitter used to tell you exactly how many characters you had left. Also, the date format varies from one country to another, so you might want to explain what to expect."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			In the old 180-character days, Twitter used to tell you exactly how many characters you had left. Also, the date format varies from one country to another, so you might want to explain what to expect. ()
		</figcaption>
	
</figure>

</li>
</ul>

<h5 id="how-to-display-descriptions">How To Display Descriptions</h5>

<p>In the examples, above, we saw a few ways to display field descriptions. Here is a summary of what to do:</p>

<ul>
<li>Inline descriptions should be directly visible and displayed next to the field.</li>
<li>If you need more in-depth descriptions with heavy content, you can use <strong>tooltips or modals</strong>. Tooltips are generally triggered on hover on desktop and on tap on mobile. The same goes for the modals: Open it when the user taps the help icon or &ldquo;see more&rdquo; link, for instance.</li>
</ul>

<div class="sponsors__wide-place"></div>




<h4 id="be-careful-with-placeholders">Be Careful With Placeholders</h4>

<p>I get it: it’s tempting to remove fields on mobile to gain space and use placeholders instead. We’ve all gone down that road. But please don’t. The HML5 specification is clear about this: &ldquo;&rdquo;. And here is why:</p>

<ul>
<li>The placeholder disappears when the user starts typing. The user must then <strong>rely on short-term memory to remember what they are supposed to put in the field</strong>. If they can’t, they will need to empty the field to see the indication.</li>
<li>It’s <strong>hard for users to double-check fields before submitting</strong> because the fields no longer have any label indications.</li>
<li>It’s <strong>hard to recover from errors</strong> once a field has been submitted because, again, there’s no label to help the user.</li>
</ul>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4d7c0ed2-6428-47a6-98ec-f38f62a7cc6a/making-mobile-form-experience-better-11-placeholder-all.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4d7c0ed2-6428-47a6-98ec-f38f62a7cc6a/making-mobile-form-experience-better-11-placeholder-all.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4d7c0ed2-6428-47a6-98ec-f38f62a7cc6a/making-mobile-form-experience-better-11-placeholder-all.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4d7c0ed2-6428-47a6-98ec-f38f62a7cc6a/making-mobile-form-experience-better-11-placeholder-all.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4d7c0ed2-6428-47a6-98ec-f38f62a7cc6a/making-mobile-form-experience-better-11-placeholder-all.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4d7c0ed2-6428-47a6-98ec-f38f62a7cc6a/making-mobile-form-experience-better-11-placeholder-all.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4d7c0ed2-6428-47a6-98ec-f38f62a7cc6a/making-mobile-form-experience-better-11-placeholder-all.jpg"
			sizes="100vw"
			alt="Placeholders rely on short-term memory"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Placeholders rely on short-term memory. They make forms hard to check before submission. And recovering from errors is hard, especially when error messages don’t help much. ()
		</figcaption>
	
</figure>


<p>Even if you use placeholders with labels, you might still have some issues. It’s <strong>hard to tell the difference between a filled field and a field with a placeholder</strong>. I’m a UX designer who writes about mobile form design and even I got tricked last week by one of those. If it happens to me, it will happen to your users &mdash; trust me on that one. Finally, most placeholders have light-gray text, so you might have some contrast issues as well.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/201528ba-b016-4682-aa84-52ebc482e2a6/making-mobile-form-experience-better-12-placeholders.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/201528ba-b016-4682-aa84-52ebc482e2a6/making-mobile-form-experience-better-12-placeholders.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/201528ba-b016-4682-aa84-52ebc482e2a6/making-mobile-form-experience-better-12-placeholders.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/201528ba-b016-4682-aa84-52ebc482e2a6/making-mobile-form-experience-better-12-placeholders.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/201528ba-b016-4682-aa84-52ebc482e2a6/making-mobile-form-experience-better-12-placeholders.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/201528ba-b016-4682-aa84-52ebc482e2a6/making-mobile-form-experience-better-12-placeholders.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/201528ba-b016-4682-aa84-52ebc482e2a6/making-mobile-form-experience-better-12-placeholders.jpg"
			sizes="100vw"
			alt="It’s easy to mistake some form fields for being filled in"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			It’s easy to mistake some of these fields for being filled in. The right screenshot is something I’ve seen online. I’ll let you guess what is filled in and what is not. ()
		</figcaption>
	
</figure>


<p>If you want to go deeper in this topic, there’s a great article named &ldquo;.”</p>

<p><strong>Placeholders are not mandatory in HTML5</strong>. From a usability point of view, you most certainly don’t need a placeholder in every field of your form. But with the massive adoption of Bootstrap and other frameworks, it looks like a lot of people just copy and paste components. Those components have placeholders, so I guess people feel kind of obligated to add something to the placeholder in the code? If your form’s placeholders look like “Please fill your &mdash; label &mdash; here”, you’re doing it wrong.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a7b4ae24-471f-4308-85b5-cc58a3c85b0c/making-mobile-form-experience-better-13-placeholders-bootstrap.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a7b4ae24-471f-4308-85b5-cc58a3c85b0c/making-mobile-form-experience-better-13-placeholders-bootstrap.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a7b4ae24-471f-4308-85b5-cc58a3c85b0c/making-mobile-form-experience-better-13-placeholders-bootstrap.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a7b4ae24-471f-4308-85b5-cc58a3c85b0c/making-mobile-form-experience-better-13-placeholders-bootstrap.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a7b4ae24-471f-4308-85b5-cc58a3c85b0c/making-mobile-form-experience-better-13-placeholders-bootstrap.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a7b4ae24-471f-4308-85b5-cc58a3c85b0c/making-mobile-form-experience-better-13-placeholders-bootstrap.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a7b4ae24-471f-4308-85b5-cc58a3c85b0c/making-mobile-form-experience-better-13-placeholders-bootstrap.jpg"
			sizes="100vw"
			alt="form example"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			I’m not joking: I’ve actually seen forms with 12 fields, with each placeholder less useful than the last. ()
		</figcaption>
	
</figure>


<p>Labels inside fields could, nevertheless, <strong>work well for short forms in which fields are predictable</strong>. Login forms are a good candidate for this. But please don’t use the HTML5 placeholder to code this. Use a real label in the code and move it around with CSS and JavaScript.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/71ad7733-80b6-4920-99fc-538eb2c2d7c0/making-mobile-form-experience-better-14-placeholders-label-short.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/71ad7733-80b6-4920-99fc-538eb2c2d7c0/making-mobile-form-experience-better-14-placeholders-label-short.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/71ad7733-80b6-4920-99fc-538eb2c2d7c0/making-mobile-form-experience-better-14-placeholders-label-short.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/71ad7733-80b6-4920-99fc-538eb2c2d7c0/making-mobile-form-experience-better-14-placeholders-label-short.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/71ad7733-80b6-4920-99fc-538eb2c2d7c0/making-mobile-form-experience-better-14-placeholders-label-short.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/71ad7733-80b6-4920-99fc-538eb2c2d7c0/making-mobile-form-experience-better-14-placeholders-label-short.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/71ad7733-80b6-4920-99fc-538eb2c2d7c0/making-mobile-form-experience-better-14-placeholders-label-short.jpg"
			sizes="100vw"
			alt="Labels inside fields can work on really short forms, like login forms, where users don’t have a lot of information to remember."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Labels inside fields can work on really short forms, like login forms, where users don’t have a lot of information to remember. ()
		</figcaption>
	
</figure>


<p>Since the success of Android’s material design, a pattern has started to emerge: . This label is inside the field when the field is not filled in, so it takes a bit less vertical space on mobile. When users start interacting with the field, the label moves above the field.</p>

<p>This looks like an interesting way to gain some space, without running into the “placeholders in place of labels” issues cited above. Nevertheless, it does not solve the problem of users possibly mistaking a placeholder for filled-in content.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c40c8a8f-9036-421a-9a0d-67d4bf23028d/making-mobile-form-experience-better-15-floatinglabel.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c40c8a8f-9036-421a-9a0d-67d4bf23028d/making-mobile-form-experience-better-15-floatinglabel.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c40c8a8f-9036-421a-9a0d-67d4bf23028d/making-mobile-form-experience-better-15-floatinglabel.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c40c8a8f-9036-421a-9a0d-67d4bf23028d/making-mobile-form-experience-better-15-floatinglabel.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c40c8a8f-9036-421a-9a0d-67d4bf23028d/making-mobile-form-experience-better-15-floatinglabel.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c40c8a8f-9036-421a-9a0d-67d4bf23028d/making-mobile-form-experience-better-15-floatinglabel.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c40c8a8f-9036-421a-9a0d-67d4bf23028d/making-mobile-form-experience-better-15-floatinglabel.jpg"
			sizes="100vw"
			alt="The floating label, even if not perfect, is an interesting alternative to gaining vertical space on the screen."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The floating label, even if not perfect, is an interesting alternative to gaining vertical space on the screen. ()
		</figcaption>
	
</figure>


<h3 id="interaction-cost-reduction-for-successful-forms">Interaction Cost Reduction For Successful Forms</h3>

<p>Reducing the interaction cost (i.e. the number of taps, swipes, etc.) of users achieving their task will help you build a seamless form experience. There are different techniques to achieve that. Let’s look at a few of them in detail.</p>

<h4 id="a-magic-study-on-the-internet-told-me-to-reduce-the-number-of-fields">A Magic Study On The Internet Told Me To Reduce The Number Of Fields</h4>

<p>More fields mean fewer conversions, right? You might have encountered the “” study. It’s a classic. And if you look at their contact form, it kind of makes sense. Why would users want to fill in 11 fields just to contact the company? You can’t ask such a big commitment of people who barely know you, right?</p>

<p>Start by asking only for useful information. Why do you need a person’s gender to create an account for them? Why do you have two lines for the address if your subscription form is for an online service?</p>

<p>Ask only for the information you need. And then ask for the information in context. If you have an e-commerce website, users might be more inclined to give you their address in the shipping section of the checkout process than when they register. It will make your e-commerce registration form so much easier to fill on mobile!</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/393b3a79-251b-45bf-b57e-ab3017f5f71d/making-mobile-form-experience-better-16-context-info.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/393b3a79-251b-45bf-b57e-ab3017f5f71d/making-mobile-form-experience-better-16-context-info.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/393b3a79-251b-45bf-b57e-ab3017f5f71d/making-mobile-form-experience-better-16-context-info.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/393b3a79-251b-45bf-b57e-ab3017f5f71d/making-mobile-form-experience-better-16-context-info.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/393b3a79-251b-45bf-b57e-ab3017f5f71d/making-mobile-form-experience-better-16-context-info.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/393b3a79-251b-45bf-b57e-ab3017f5f71d/making-mobile-form-experience-better-16-context-info.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/393b3a79-251b-45bf-b57e-ab3017f5f71d/making-mobile-form-experience-better-16-context-info.jpg"
			sizes="100vw"
			alt="Ask only for the information you need"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Ask for the user’s address in the shipping section of the checkout, not when they register. ()
		</figcaption>
	
</figure>


<p>Also, don’t blindly trust every statistic and study you find on the Internet. Remember the 11-fields-to-4 study? Well another more recent study showed that by . Shocking, isn’t it? Why? Well, they removed the most engaging fields. Long story short, they then went back to 9 fields, put the most important on the top, and voilà, conversions increased by 19.21%.</p>

<p>The bottom line is that while these studies are interesting, those websites are not your website. Don’t blindly trust the first study you find on the Internet.</p>

<p>So, what can you do? Test. Test. And test!</p>

<ul>
<li>Do some user testing to see the time to completion of your mobile form.</li>
<li>Measure drop outs.</li>
<li>Measure problems with certain fields.</li>
<li>Measure the frustration associated with certain fields. How willing are users to give that information? How personal is that information?</li>
</ul>

<div class="sponsors__wide-place"></div>




<h4 id="optimizing-touch-interactions">Optimizing Touch Interactions</h4>

<h5 id="making-controls-touch-friendly">Making Controls Touch-Friendly</h5>

<p>If your fields are too small or hard to reach, users will make errors and will need extra interactions to achieve their goals. Remember ? You could apply it to mobile design as well: Make your labels, fields and form controls easy to tap by <strong>increasing the touch target size</strong>. For labels on the web, a little more padding can increase the touchable area. Sometimes you will also need to add some margins between elements to avoid missed taps.</p>

<p>Also, don’t forget to link labels with their components by pairing <code>for</code> and ID values. That way, if the user misses a tap on the label, the corresponding field will still get focus.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a43e638c-4580-4967-9fcc-7fca4d6026cf/making-mobile-form-experience-better-17-padding-margin.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a43e638c-4580-4967-9fcc-7fca4d6026cf/making-mobile-form-experience-better-17-padding-margin.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a43e638c-4580-4967-9fcc-7fca4d6026cf/making-mobile-form-experience-better-17-padding-margin.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a43e638c-4580-4967-9fcc-7fca4d6026cf/making-mobile-form-experience-better-17-padding-margin.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a43e638c-4580-4967-9fcc-7fca4d6026cf/making-mobile-form-experience-better-17-padding-margin.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a43e638c-4580-4967-9fcc-7fca4d6026cf/making-mobile-form-experience-better-17-padding-margin.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a43e638c-4580-4967-9fcc-7fca4d6026cf/making-mobile-form-experience-better-17-padding-margin.jpg"
			sizes="100vw"
			alt="On mobile, respect mobile touch-optimized best practices, and make sure inputs are big enough to be easily tappable."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			On mobile, respect mobile touch-optimized best practices, and make sure inputs are big enough to be easily tappable. ()
		</figcaption>
	
</figure>


<p>Steven Hoober conducted some user research on touch areas. You’ll find a summary in &ldquo;. The tool could help you make sure your touch areas are big enough for mobile forms and more generally for mobile design.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cac71a58-605b-43aa-8069-0a312e54a3f3/making-mobile-form-experience-better-18-touchtemplate.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cac71a58-605b-43aa-8069-0a312e54a3f3/making-mobile-form-experience-better-18-touchtemplate.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cac71a58-605b-43aa-8069-0a312e54a3f3/making-mobile-form-experience-better-18-touchtemplate.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cac71a58-605b-43aa-8069-0a312e54a3f3/making-mobile-form-experience-better-18-touchtemplate.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cac71a58-605b-43aa-8069-0a312e54a3f3/making-mobile-form-experience-better-18-touchtemplate.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cac71a58-605b-43aa-8069-0a312e54a3f3/making-mobile-form-experience-better-18-touchtemplate.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cac71a58-605b-43aa-8069-0a312e54a3f3/making-mobile-form-experience-better-18-touchtemplate.jpg"
			sizes="100vw"
			alt="Image from Steven Hoober"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Image from Steven Hoober’s )
		</figcaption>
	
</figure>


<p>To learn more about designing for touch you can read the following:</p>

<ul>
<li>“”</li>
<li>“”</li>
</ul>

<h5 id="providing-feedback">Providing Feedback</h5>

<p>Mobile users don’t have a mouse (no kidding), so they don’t get the &ldquo;click&rdquo; feedback that desktop users get when hitting a button. Mobile form users need clear feedback when interacting with elements:</p>

<ul>
<li><strong>Provide a focus state</strong> for the form field that the user is interacting with.</li>
<li>Provide <strong>visual feedback when the user interacts with a button</strong>.</li>
</ul>

<p>I’m not a big fan of material design’s ripple effect on buttons. But I must admit that  on Android provide clear feedback when the user interacts with a button.</p>

<figure class="video-container"><iframe data-src="https://player.vimeo.com/video/285090837" width="600" height="480" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe></figure>

<h5 id="honor-the-next-and-previous-button-order">Honor The Next And Previous Button Order</h5>

<p>Finally, honor the next and previous buttons on mobile keyboards. Users can use them to quickly navigate fields. The <code>tabindex</code> order should match the visual order of fields and components.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/92647327-ec00-4110-8f53-6e86dc5838ee/making-mobile-form-experience-better-19-ios-ordre.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/92647327-ec00-4110-8f53-6e86dc5838ee/making-mobile-form-experience-better-19-ios-ordre.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/92647327-ec00-4110-8f53-6e86dc5838ee/making-mobile-form-experience-better-19-ios-ordre.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/92647327-ec00-4110-8f53-6e86dc5838ee/making-mobile-form-experience-better-19-ios-ordre.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/92647327-ec00-4110-8f53-6e86dc5838ee/making-mobile-form-experience-better-19-ios-ordre.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/92647327-ec00-4110-8f53-6e86dc5838ee/making-mobile-form-experience-better-19-ios-ordre.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/92647327-ec00-4110-8f53-6e86dc5838ee/making-mobile-form-experience-better-19-ios-ordre.jpg"
			sizes="100vw"
			alt="iOS has small arrows on the keyboard to go from one field to another."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			iOS has small arrows on the keyboard to go from one field to another. ()
		</figcaption>
	
</figure>


<h4 id="avoid-dropdowns-on-mobile-if-possible">Avoid Dropdowns On Mobile If Possible</h4>

<p>Dropdowns (the HTML select element) on the web require a lot of tabs and interactions. Therefore, as Luke Wroblewski said, . Many other UI components work better than dropdowns in many situations.</p>

<p><strong>Segment controls and radio buttons</strong> are good alternatives to dropdowns if you have between two and four options. Why hide the options under a dropdown when you can show them all directly on one screen? Note that, like radio buttons, segment controls are mutually exclusive.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/29cc7fed-c6e5-4378-8e73-ea0b9286f2ae/making-mobile-form-experience-better-20-segment-control.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/29cc7fed-c6e5-4378-8e73-ea0b9286f2ae/making-mobile-form-experience-better-20-segment-control.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/29cc7fed-c6e5-4378-8e73-ea0b9286f2ae/making-mobile-form-experience-better-20-segment-control.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/29cc7fed-c6e5-4378-8e73-ea0b9286f2ae/making-mobile-form-experience-better-20-segment-control.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/29cc7fed-c6e5-4378-8e73-ea0b9286f2ae/making-mobile-form-experience-better-20-segment-control.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/29cc7fed-c6e5-4378-8e73-ea0b9286f2ae/making-mobile-form-experience-better-20-segment-control.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/29cc7fed-c6e5-4378-8e73-ea0b9286f2ae/making-mobile-form-experience-better-20-segment-control.png"
			sizes="100vw"
			alt="Example of segment controls in the iOnic library."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Example of segment controls in the iOnic library. ()
		</figcaption>
	
</figure>


<p>A <strong>country list</strong> is a good candidate for a component. A dropdown of over a hundred countries is an interaction nightmare on mobile. It’s OK if you are looking for Afghanistan (at the beginning of the list) or Zimbabwe (the end of the list). If you’re looking for Luxembourg, you will end up in a game of scrolling to reach the middle of the list, going too far to the letter M, trying to come back to L, and so on.</p>

<p><strong>Long dropdowns can be replaced by predictive text input fields</strong>. When the user starts typing L, the interface would propose nine countries. If they add a U &mdash; <em>voilà!</em> &mdash; Luxembourg it is. Four interactions instead of two, versus as many as six or seven scrolling interactions with the dropdown.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2db338a4-5349-4f2f-bdb5-df6f01d1a8ba/making-mobile-form-experience-better-21-dropdowns-countries.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2db338a4-5349-4f2f-bdb5-df6f01d1a8ba/making-mobile-form-experience-better-21-dropdowns-countries.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2db338a4-5349-4f2f-bdb5-df6f01d1a8ba/making-mobile-form-experience-better-21-dropdowns-countries.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2db338a4-5349-4f2f-bdb5-df6f01d1a8ba/making-mobile-form-experience-better-21-dropdowns-countries.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2db338a4-5349-4f2f-bdb5-df6f01d1a8ba/making-mobile-form-experience-better-21-dropdowns-countries.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2db338a4-5349-4f2f-bdb5-df6f01d1a8ba/making-mobile-form-experience-better-21-dropdowns-countries.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2db338a4-5349-4f2f-bdb5-df6f01d1a8ba/making-mobile-form-experience-better-21-dropdowns-countries.jpg"
			sizes="100vw"
			alt="Long dropdowns are a nightmare when you’re searching for France. Predictive fields work better."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Long dropdowns are a nightmare when you’re searching for France. Predictive fields work better. ()
		</figcaption>
	
</figure>


<p>If you need users to <strong>pick a date, forget about splitting it into a day, month and year dropdown</strong> like people are used to doing on paper forms. <strong>Replace multiple date dropdowns with a date picker</strong>. The HTML5 input <code>type=date</code> works in most cases. But you might have some special needs and end up building your own date picker in JavaScript, especially if you are in the booking business (hotels, cars, flights).</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ee52d37a-bbe6-4e5b-b7e8-106a17ac803e/22-making-mobile-form-experience-better-dropdown-date.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ee52d37a-bbe6-4e5b-b7e8-106a17ac803e/22-making-mobile-form-experience-better-dropdown-date.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ee52d37a-bbe6-4e5b-b7e8-106a17ac803e/22-making-mobile-form-experience-better-dropdown-date.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ee52d37a-bbe6-4e5b-b7e8-106a17ac803e/22-making-mobile-form-experience-better-dropdown-date.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ee52d37a-bbe6-4e5b-b7e8-106a17ac803e/22-making-mobile-form-experience-better-dropdown-date.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ee52d37a-bbe6-4e5b-b7e8-106a17ac803e/22-making-mobile-form-experience-better-dropdown-date.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ee52d37a-bbe6-4e5b-b7e8-106a17ac803e/22-making-mobile-form-experience-better-dropdown-date.jpg"
			sizes="100vw"
			alt="A double date-picker built in JavaScript makes it easy to pick arrival and departure dates with a minimum of interaction"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			A double date-picker built in JavaScript makes it easy to pick arrival and departure dates with a minimum of interaction ()
		</figcaption>
	
</figure>


<p>In his article “”, Klaus Schaefers explains how using a date-picker for arrival and departure dates made interactions 60% faster.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a41754a5-36a4-40f4-9188-2ba1f1b50258/making-mobile-form-experience-better-23-dropdowns-revisited.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a41754a5-36a4-40f4-9188-2ba1f1b50258/making-mobile-form-experience-better-23-dropdowns-revisited.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a41754a5-36a4-40f4-9188-2ba1f1b50258/making-mobile-form-experience-better-23-dropdowns-revisited.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a41754a5-36a4-40f4-9188-2ba1f1b50258/making-mobile-form-experience-better-23-dropdowns-revisited.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a41754a5-36a4-40f4-9188-2ba1f1b50258/making-mobile-form-experience-better-23-dropdowns-revisited.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a41754a5-36a4-40f4-9188-2ba1f1b50258/making-mobile-form-experience-better-23-dropdowns-revisited.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a41754a5-36a4-40f4-9188-2ba1f1b50258/making-mobile-form-experience-better-23-dropdowns-revisited.jpg"
			sizes="100vw"
			alt="A date-picker, using HTML5 or JavaScript, instead of dropdowns, via Mobile DropDowns Revisited"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			A date-picker, using HTML5 or JavaScript, instead of dropdowns, via )
		</figcaption>
	
</figure>


<p>Let’s stick with the booking business. Suppose the user needs to add multiple travellers to their itinerary. You can **replace the dropdown *<strong><em>with a</em></strong>* stepper** to select the number of passengers. A stepper is a control that allows the user to increase and decrease values simply by tapping on <kbd>+</kbd> and <kbd>-</kbd> buttons. That tends to be faster when fewer than six persons have to be added. It’s also more intuitive. Below is an example of a stepper used in the Android-native Airbnb app to select guests, and on the mobile-optimized website of Kayak to add passengers.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a8ddd2d6-ccfa-4c21-9473-75aebe266228/making-mobile-form-experience-better-24-steppers.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a8ddd2d6-ccfa-4c21-9473-75aebe266228/making-mobile-form-experience-better-24-steppers.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a8ddd2d6-ccfa-4c21-9473-75aebe266228/making-mobile-form-experience-better-24-steppers.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a8ddd2d6-ccfa-4c21-9473-75aebe266228/making-mobile-form-experience-better-24-steppers.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a8ddd2d6-ccfa-4c21-9473-75aebe266228/making-mobile-form-experience-better-24-steppers.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a8ddd2d6-ccfa-4c21-9473-75aebe266228/making-mobile-form-experience-better-24-steppers.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a8ddd2d6-ccfa-4c21-9473-75aebe266228/making-mobile-form-experience-better-24-steppers.jpg"
			sizes="100vw"
			alt="A stepper is used in the Android-native Airbnb app to select guests and on the mobile-optimized website of Kayak to add passengers."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			A stepper is used in the Android-native Airbnb app to select guests and on the mobile-optimized website of Kayak to add passengers. ()
		</figcaption>
	
</figure>


<p>A final alternative to dropdowns is the list view. <strong>The options would be listed in a specific subview, as radio buttons</strong>, for instance. This is mostly how Android settings work.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cbab6d24-f3c8-4a04-9e80-b182d44f5c04/making-mobile-form-experience-better-25-dropdownlist-view.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cbab6d24-f3c8-4a04-9e80-b182d44f5c04/making-mobile-form-experience-better-25-dropdownlist-view.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cbab6d24-f3c8-4a04-9e80-b182d44f5c04/making-mobile-form-experience-better-25-dropdownlist-view.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cbab6d24-f3c8-4a04-9e80-b182d44f5c04/making-mobile-form-experience-better-25-dropdownlist-view.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cbab6d24-f3c8-4a04-9e80-b182d44f5c04/making-mobile-form-experience-better-25-dropdownlist-view.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cbab6d24-f3c8-4a04-9e80-b182d44f5c04/making-mobile-form-experience-better-25-dropdownlist-view.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cbab6d24-f3c8-4a04-9e80-b182d44f5c04/making-mobile-form-experience-better-25-dropdownlist-view.jpg"
			sizes="100vw"
			alt="In our monitoring app, when the user clicks on “notification type 1”, it opens a list view with the options."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			In our monitoring app, when the user clicks on “notification type 1”, it opens a list view with the options. ()
		</figcaption>
	
</figure>


<h4 id="getting-smart-with-auto-completion">Getting Smart With Auto-Completion</h4>

<p>If you want to decrease the interaction cost of your form, be smart. Don’t ask for information that you can auto-detect or guess based on other information users have given you. Autocomplete and prefill as much as you can.</p>

<h5 id="places-and-addresses">Places and Addresses</h5>

<p>If the user searches for a place or needs to enter an address, you can offer auto-completion to help them. As they type, an API would fill in the rest of the address for them. This also reduces errors.</p>

<p>You could use:</p>

<ul>
<li></li>
<li></li>
</ul>

<figure class="video-container"><iframe data-src="https://player.vimeo.com/video/285090864" width="600" height="480" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe><nr /><em>In the , as the user types, it offers suggestions and can autocomplete the field.</em></figure>

<p>In France and many other countries, you can guess the city based on the area code. So, if a French user enters an area code, you could automatically auto-complete or at least propose the city. My country, Luxembourg, is small (don’t make fun of me). My area code is linked to my street. So, if I enter my area code, the form should even be able to suggest my street.</p>

<h5 id="credit-cards">Credit Cards</h5>

<p>Another area where auto-detection is easy is credit cards. You don’t need to ask the user what type of credit card they have. You can auto-detect this based on the initial numbers they enter. There’s even a  that can do the job for you.</p>

<figure class="video-container"><iframe data-src="https://player.vimeo.com/video/285090878" width="600" height="480" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe><br /><em>A demo of the payment script that detects credit card type.</em></figure>

<h5 id="using-html5-autocompletion-autofill">Using HTML5 Autocompletion (Autofill)</h5>

<p>The .</p>

<p>Chrome and other mobile browsers already . This means that users can prefill forms with their name and credit card data that they use on other websites.</p>

<figure>)</figcaption></figure>

<p>In short, when you must choose between different systems, count the number of interactions each is going to require.</p>

<h3 id="mistakes-happen-handling-errors-in-mobile-forms">Mistakes Happen: Handling Errors In Mobile Forms</h3>

<p>The last step on our journey towards better mobile forms is handling errors and mistakes. We can try to reduce mistakes to ease the user’s cognitive load. We can also help them recover from errors, because no matter how great your form design is, mistakes happen.</p>

<h4 id="avoiding-errors-while-filling-the-forms">Avoiding Errors While Filling The Forms</h4>

<p>“Prevention is better than a cure,” my mother used to say. That’s also true of form design: Preventing errors will improve your mobile form’s experience.</p>

<h5 id="explicit-format-limitation">Explicit Format Limitation</h5>

<p>“Be conservative in what you do. Be liberal in what you accept from others.” This  can be applied to form fields as well. If possible, let the user enter data in any format.</p>

<p>If you think you need to limit what a user can enter in the field, start by asking yourself &ldquo;why&rdquo;. In the user experience field, we have a technique called “the three whys”. If the answer is “because blah blah database”, maybe it’s time to change things. For instance, why do you refuse special characters like é, à and ö in the user name field? . I’m still trying to figure out a good reason for that (apart from database reasons).</p>

<p>If you have a good reason to <strong>require a specific format from users, state this up front</strong>. You can use HTML5 <strong>placeholder</strong>s to give users a hint about what the data should look like, but again, be careful with those. You could also use all of the <strong>field description techniques</strong> explained at the beginning of this article. Finally, input masks can <strong>guide users towards</strong> the right format.</p>

<h5 id="marking-mandatory-fields-and-optional-ones">Marking Mandatory Fields (And Optional Ones)</h5>

<p>Don’t wait for users to submit a half-completed form to tell them about required fields. If a <strong>field is mandatory, users should know about it</strong>. Marking mandatory fields with an asterix (<code>*</code>) and a legend has become a standard pattern for forms. The good part is that it does not take much space. The problem is that it has no semantic value, so it can cause accessibility issues if poorly coded and if you rely on people’s habits with form interaction.</p>

<p>You could instead <strong>explicitly mark both mandatory and optional fields with the words</strong> “required” (or “mandatory”) and “optional”. Both  agree on that. This avoids ambiguity with long forms on mobile, such as when using a scroller, proceeding with something else, then coming back and not remembering if mandatory fields were marked with an asterisk or something else.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/09470d89-4a0d-43cb-959e-0af5e28cac37/making-mobile-form-experience-better-26-mandatory.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/09470d89-4a0d-43cb-959e-0af5e28cac37/making-mobile-form-experience-better-26-mandatory.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/09470d89-4a0d-43cb-959e-0af5e28cac37/making-mobile-form-experience-better-26-mandatory.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/09470d89-4a0d-43cb-959e-0af5e28cac37/making-mobile-form-experience-better-26-mandatory.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/09470d89-4a0d-43cb-959e-0af5e28cac37/making-mobile-form-experience-better-26-mandatory.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/09470d89-4a0d-43cb-959e-0af5e28cac37/making-mobile-form-experience-better-26-mandatory.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/09470d89-4a0d-43cb-959e-0af5e28cac37/making-mobile-form-experience-better-26-mandatory.jpg"
			sizes="100vw"
			alt="A form with both mandatory and optional fields marked."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			A form with both mandatory and optional fields marked. ()
		</figcaption>
	
</figure>


<p>Eventually, the decision on how to mark those fields will depend on the design and length of the field and on the context. The best way to know whether you’ve made the right decision is, again, to test the form.</p>

<h5 id="sensible-defaults">Sensible Defaults</h5>

<p><strong>Be careful about default selected options in forms</strong>. When I applied for my previous job, there was an information form. The marital status was optional. They made the first element in the dropdown, “divorced”, the default field. So, I could either not answer (because it was an optional field) and let the system believe that I was divorced, or correct this and disclose my actual marital status even if I did not want to.</p>

<p>Also, be careful about gender. Again, have an option for people who don’t want to disclose it; make clear why you’re asking for their gender; better yet, ask for pronouns, or don’t ask if you don’t really need to. If you are interested in this topic, I recommend “.” And if the gender is optional, again, don’t auto-check the first choice, otherwise people won’t be able to uncheck that radio button and choose not to answer.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3b5acd51-0cda-4935-bb35-74f852be83e0/making-mobile-form-experience-better-27-defaults.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3b5acd51-0cda-4935-bb35-74f852be83e0/making-mobile-form-experience-better-27-defaults.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3b5acd51-0cda-4935-bb35-74f852be83e0/making-mobile-form-experience-better-27-defaults.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3b5acd51-0cda-4935-bb35-74f852be83e0/making-mobile-form-experience-better-27-defaults.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3b5acd51-0cda-4935-bb35-74f852be83e0/making-mobile-form-experience-better-27-defaults.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3b5acd51-0cda-4935-bb35-74f852be83e0/making-mobile-form-experience-better-27-defaults.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3b5acd51-0cda-4935-bb35-74f852be83e0/making-mobile-form-experience-better-27-defaults.jpg"
			sizes="100vw"
			alt="Should I leave the default and lie, or put the right information even I don’t want to?"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Should I leave the default and lie, or put the right information even I don’t want to? ()
		</figcaption>
	
</figure>


<p><strong>Smart defaults, on the other hand, can help users avoid mistakes</strong> when filling a form. Unless you’re in a Dr. Who episode, you’re not supposed to book a hotel in the past. Booking.com understands that. When you open the date-picker on the website, the default date is set to the current date and you can’t select a date in the past. When you select a return date, the default is the day after the departure date.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8da2085f-22fb-41a7-a073-9133c6f87ee3/making-mobile-form-experience-better-28-booking-defaults.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8da2085f-22fb-41a7-a073-9133c6f87ee3/making-mobile-form-experience-better-28-booking-defaults.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8da2085f-22fb-41a7-a073-9133c6f87ee3/making-mobile-form-experience-better-28-booking-defaults.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8da2085f-22fb-41a7-a073-9133c6f87ee3/making-mobile-form-experience-better-28-booking-defaults.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8da2085f-22fb-41a7-a073-9133c6f87ee3/making-mobile-form-experience-better-28-booking-defaults.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8da2085f-22fb-41a7-a073-9133c6f87ee3/making-mobile-form-experience-better-28-booking-defaults.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8da2085f-22fb-41a7-a073-9133c6f87ee3/making-mobile-form-experience-better-28-booking-defaults.jpg"
			sizes="100vw"
			alt="Booking.com’s smart defaults help users avoid mistakes. You can’t search in the past or before your arrival date."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Booking.com’s smart defaults help users avoid mistakes. You can’t search in the past or before your arrival date. ()
		</figcaption>
	
</figure>


<h5 id="less-painful-password-experience">Less Painful Password Experience</h5>

<p>I’ve written about password-less authentication, but you can’t always use those techniques. Users will eventually have to create a password and enter it in a mobile form. And most of the time, that experience sucks. Here are a few ideas on how to make it better and help users avoid mistakes.</p>

<ul>
    <li><strong>When Creating An Account</strong><br />I won’t get into the details of what kind of passwords you should require and how many characters they should be composed of &mdash; plenty of articles on that topic are on the web &mdash; just make up your mind about your password criteria. When users create an account, be proactive, not reactive. For the love of Cthulhu, don’t let people guess. <strong>Tell users your password criteria up front</strong>.<br /><br />A lot of websites now show you <strong>a gauge for password strength telling you in real time what is missing</strong>. This is an interesting and excellent pattern. KLM uses it in its sign-in form:











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/065a64ce-9323-4fa6-b272-8d8427bb5ccc/making-mobile-form-experience-better-29-klm-passwords.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/065a64ce-9323-4fa6-b272-8d8427bb5ccc/making-mobile-form-experience-better-29-klm-passwords.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/065a64ce-9323-4fa6-b272-8d8427bb5ccc/making-mobile-form-experience-better-29-klm-passwords.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/065a64ce-9323-4fa6-b272-8d8427bb5ccc/making-mobile-form-experience-better-29-klm-passwords.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/065a64ce-9323-4fa6-b272-8d8427bb5ccc/making-mobile-form-experience-better-29-klm-passwords.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/065a64ce-9323-4fa6-b272-8d8427bb5ccc/making-mobile-form-experience-better-29-klm-passwords.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/065a64ce-9323-4fa6-b272-8d8427bb5ccc/making-mobile-form-experience-better-29-klm-passwords.jpg"
			sizes="100vw"
			alt="KLM sign-in form example"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			KLM sign-in form example ()
		</figcaption>
	
</figure>


But there are still some big problems with this design.</li></ul>

<ol>
    <li>They don’t tell users their password criteria up front. Users who want to generate a password (using a password manager, for instance) must first guess that they need to first interact with the field in other to see the password criteria.</li>
    <li>They limit the password’s length to 12 characters, but they never tell users how many characters are left. Sure, let’s add "counting the dots" to the cognitive load of building a password with so many criteria. After 12 characters, you can keep on typing on the keyboard, and nothing will happen.</li>
    <li>What happens if, like me, you reached the 12-character limit but haven’t met all of the criteria? Well, you would just have to delete the entire password and start over again.</li>
    <li>Finally, you must enter the password twice. How is a user supposed to remember and retype the password that they just created based on those criteria while counting the dots?</li>
    <li>Back to 1, generating a password with a password manager.</li>
</ol>

<p>If KLM wanted to make this form better, it could <strong>provide a mask/unmask option</strong> for the password. Doing so, it would not need to ask for the same password twice. Users could visually check that the password they typed is the one they want.</p>

<figure class="video-container"><iframe data-src="https://player.vimeo.com/video/285097738" width="600" height="480" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe><br /><em>TransferWise doesn’t solve my first problem in the list, but at least I can unmask while typing.</em></figure>
</li>

<ul>
<li><strong>When Logging In</strong><br />In a login form, a <strong>mask/unmask password option</strong> would tremendously improve the user experience.

<figure class="video-container"><iframe data-src="https://player.vimeo.com/video/285090892" width="600" height="480" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe><br /><em>A button to show and hide the password in a form.</em></figure>

<p>Amazon has an interesting history of iterating on passwords in its login form. It used to have a version in which you could not see the password. The next iteration allowed users to reveal it. Then, the password was revealed by default, and you could hide it. This is what is looked like in 2015:</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f5d81f26-f0a4-4eb6-af61-b8960ea10069/making-mobile-form-experience-better-30-amazonpwd.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f5d81f26-f0a4-4eb6-af61-b8960ea10069/making-mobile-form-experience-better-30-amazonpwd.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f5d81f26-f0a4-4eb6-af61-b8960ea10069/making-mobile-form-experience-better-30-amazonpwd.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f5d81f26-f0a4-4eb6-af61-b8960ea10069/making-mobile-form-experience-better-30-amazonpwd.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f5d81f26-f0a4-4eb6-af61-b8960ea10069/making-mobile-form-experience-better-30-amazonpwd.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f5d81f26-f0a4-4eb6-af61-b8960ea10069/making-mobile-form-experience-better-30-amazonpwd.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f5d81f26-f0a4-4eb6-af61-b8960ea10069/making-mobile-form-experience-better-30-amazonpwd.png"
			sizes="100vw"
			alt="Showing Passwords on Log-In Screens by Luke Wroblewski (2015)"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			)
		</figcaption>
	
</figure>


<p>Amazon tested the last version, and 60% people got suspicious. So, they replaced the &ldquo;hide password&rdquo; unchecked checkbox with a “show password” checked box. This would show the password in smaller characters, under the field, while the user typed. This is what it looks like at the time of writing this article:</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e5d1937d-cd03-4b09-844c-cce54a509850/making-mobile-form-experience-better-31-amazon-current-passwords.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e5d1937d-cd03-4b09-844c-cce54a509850/making-mobile-form-experience-better-31-amazon-current-passwords.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e5d1937d-cd03-4b09-844c-cce54a509850/making-mobile-form-experience-better-31-amazon-current-passwords.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e5d1937d-cd03-4b09-844c-cce54a509850/making-mobile-form-experience-better-31-amazon-current-passwords.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e5d1937d-cd03-4b09-844c-cce54a509850/making-mobile-form-experience-better-31-amazon-current-passwords.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e5d1937d-cd03-4b09-844c-cce54a509850/making-mobile-form-experience-better-31-amazon-current-passwords.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e5d1937d-cd03-4b09-844c-cce54a509850/making-mobile-form-experience-better-31-amazon-current-passwords.jpg"
			sizes="100vw"
			alt="Amazon’s show and hide password functionality"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Amazon’s show and hide password functionality ()
		</figcaption>
	
</figure>


<p>As you can see, there’s always room for improvement.</li>
</ul></p>

<h5 id="inline-validation">Inline Validation</h5>

<p>If you are familiar with usability principles, you might know the Gestalt law of proximity. On mobile, avoid the summary of errors at the top of the page, with no contextual information, after the user has tapped the submit button.</p>

<p>Instead, <strong>error messages should be located close to the errors themselves</strong>.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/173b4ef2-b61f-4af4-8869-57ca43c3b165/making-mobile-form-experience-better-32-erreurs-inline.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/173b4ef2-b61f-4af4-8869-57ca43c3b165/making-mobile-form-experience-better-32-erreurs-inline.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/173b4ef2-b61f-4af4-8869-57ca43c3b165/making-mobile-form-experience-better-32-erreurs-inline.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/173b4ef2-b61f-4af4-8869-57ca43c3b165/making-mobile-form-experience-better-32-erreurs-inline.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/173b4ef2-b61f-4af4-8869-57ca43c3b165/making-mobile-form-experience-better-32-erreurs-inline.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/173b4ef2-b61f-4af4-8869-57ca43c3b165/making-mobile-form-experience-better-32-erreurs-inline.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/173b4ef2-b61f-4af4-8869-57ca43c3b165/making-mobile-form-experience-better-32-erreurs-inline.jpg"
			sizes="100vw"
			alt="An example of inline validation"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			An example of inline validation ()
		</figcaption>
	
</figure>


<h5 id="real-time-validation">Real-Time Validation</h5>

<p>You also don’t need to wait until users hit the submit button. You can <strong>validate fields and display feedback while the user is filling them in</strong>.</p>

<p>A few tips:</p>

<ul>
<li>As mentioned earlier, password fields would benefit from real-time validation and feedback on each keystroke.</li>
<li>You might also want to validate user names in real time when accounts are being created, to make sure they’re available. Twitter does a good job of that.</li>
<li>Don’t validate every keystroke. Wait until the user has finished typing. (Use JavaScript <code>blur</code> for web forms, or just wait a few seconds to detect inactivity.)</li>
</ul>

<p><strong>Note</strong>: *Mihael Konjević has written a nice article on “.” He explains the concept of “<strong>reward early, punish late</strong>.”*</p>

<blockquote>“If the user is entering the data in the field that was in a <strong>valid</strong> state, perform the validation after the data entry.”</blockquote>

<blockquote>“If the user is entering the data in the field that was in an <strong>invalid</strong> state, perform the validation during the data entry.”</blockquote>

<figure class="video-container"><iframe data-src="https://player.vimeo.com/video/285090905" width="600" height="480" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe><br /><em>Example from  based on the article.</em></figure>

<h4 id="color-matters">Color Matters</h4>

<p>I’m not saying that color matters just because of my current ginger, pink and purple hair color. Color really matters in form design.</p>

<p>There are some conventions on the web that you don’t want to break. Non-colorblind users know that red is for errors, yellow is for warnings, and green is almost always for confirmation or success. It’s best to stick with these three colors. , though. The user might think they’ve made a really serious mistake. Using orange or yellow for error messages could cause less panic. The problem with yellow and orange is that it’s hard to find colorblind-friendly hues of them.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d31017a8-ce0d-42f8-a1b0-4d5afebfdab7/making-mobile-form-experience-better-33-colors.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d31017a8-ce0d-42f8-a1b0-4d5afebfdab7/making-mobile-form-experience-better-33-colors.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d31017a8-ce0d-42f8-a1b0-4d5afebfdab7/making-mobile-form-experience-better-33-colors.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d31017a8-ce0d-42f8-a1b0-4d5afebfdab7/making-mobile-form-experience-better-33-colors.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d31017a8-ce0d-42f8-a1b0-4d5afebfdab7/making-mobile-form-experience-better-33-colors.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d31017a8-ce0d-42f8-a1b0-4d5afebfdab7/making-mobile-form-experience-better-33-colors.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d31017a8-ce0d-42f8-a1b0-4d5afebfdab7/making-mobile-form-experience-better-33-colors.jpg"
			sizes="100vw"
			alt="Colors have different connotations across countries and cultures. Be careful with them."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Colors have different connotations across countries and cultures. Be careful with them. ()
		</figcaption>
	
</figure>


<p>Speaking of colorblindness: <strong>Color should not be the only way to convey an error message</strong>. This is an accessibility criterion.</p>

<p>In the example below on the left, the field with an error is in orange, and the field that has been corrected has turned green. I used a colorblind testing tool to take the screenshot in the middle: You can’t distinguish between the default gray border and the green one anymore. Adding some icons in the last screenshot ensures that the error messages are conveyed to colorblind people.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/694142d3-e538-4499-be08-063fa55a8d74/making-mobile-form-experience-better-33-erreur-accessibilite.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/694142d3-e538-4499-be08-063fa55a8d74/making-mobile-form-experience-better-33-erreur-accessibilite.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/694142d3-e538-4499-be08-063fa55a8d74/making-mobile-form-experience-better-33-erreur-accessibilite.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/694142d3-e538-4499-be08-063fa55a8d74/making-mobile-form-experience-better-33-erreur-accessibilite.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/694142d3-e538-4499-be08-063fa55a8d74/making-mobile-form-experience-better-33-erreur-accessibilite.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/694142d3-e538-4499-be08-063fa55a8d74/making-mobile-form-experience-better-33-erreur-accessibilite.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/694142d3-e538-4499-be08-063fa55a8d74/making-mobile-form-experience-better-33-erreur-accessibilite.jpg"
			sizes="100vw"
			alt="Color should not be the only way to convey error messages. The colorblind simulation in the middle shows that the green border cannot be seen by a colorblind person."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Color should not be the only way to convey error messages. The colorblind simulation in the middle shows that the green border cannot be seen by a colorblind person. ()
		</figcaption>
	
</figure>


<h4 id="recovering-from-errors-writing-user-friendly-error-messages">Recovering From Errors: Writing User-Friendly Error Messages</h4>

<p>At this point, we’ve done everything we can to help users fill our forms and avoid errors. But sometimes, despite our best effort, mistakes happen. It’s time to figure out how to help users recover from those mistakes.</p>

<p>First, remember: Don’t hijack control of the system. If a problem isn’t critical, the user should be able to continue interacting with as much of the rest of the interface as possible. Avoid those JavaScript alert error message and modals that blocks users whenever possible. Also, if your form needs some permission, request it in the flow of use. If permission is not granted, do not consider this an error because it is not. Be careful about the copy you use here.</p>

<h5 id="you-re-not-a-robot-and-neither-are-your-users">You’re Not A Robot, And Neither Are Your Users</h5>

<p>Robots are cool, I know. But you’re not a robot, and neither are your users. Yet so many error messages are still so poorly written. Here are a few tips when it comes to human-friendly error messages:</p>

<ul>
<li>Never show a raw error message, like “An error of type 2393 has occurred. Server could not complete the operation.” Instead, <strong>explain what happened in human language and why it happened</strong>.</li>
<li>Never show a dead-end error message, like &ldquo;An error has occurred.&rdquo; Instead <strong>suggest ways to recover from the error</strong>. Write actionable copy.</li>
<li>Never show a vague error message, like “A server with the specified hostname could not be found”, with a “Try again” button. Instead, <strong>make error messages informative and consistent</strong>. Please don’t sound like a robot.</li>
<li>Don’t assume that people know the context of a message. Your users are not tech-savvy geeks. Instead, <strong>explain to them in plain language, without technical jargon, how to recover from this error</strong>.</li>
</ul>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1466199f-9b74-4ca6-8a13-76d2914c389f/making-mobile-form-experience-better-34-erreur-messages.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1466199f-9b74-4ca6-8a13-76d2914c389f/making-mobile-form-experience-better-34-erreur-messages.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1466199f-9b74-4ca6-8a13-76d2914c389f/making-mobile-form-experience-better-34-erreur-messages.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1466199f-9b74-4ca6-8a13-76d2914c389f/making-mobile-form-experience-better-34-erreur-messages.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1466199f-9b74-4ca6-8a13-76d2914c389f/making-mobile-form-experience-better-34-erreur-messages.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1466199f-9b74-4ca6-8a13-76d2914c389f/making-mobile-form-experience-better-34-erreur-messages.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1466199f-9b74-4ca6-8a13-76d2914c389f/making-mobile-form-experience-better-34-erreur-messages.jpg"
			sizes="100vw"
			alt="Examples of non-human-friendly error messages. Eek!"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Examples of non-human-friendly error messages. Eek! ()
		</figcaption>
	
</figure>


<h5 id="beware-the-language-you-use-in-messages">Beware The Language You Use In Messages</h5>

<p>Whatever you write, <strong>avoid making people feel stupid</strong> about a mistake. If possible, <strong>leave out negative words</strong>; they tend to scare people and make them even more anxious. Use a courteous, positive, affirming tone instead.</p>

<p><strong>Don’t blame users for mistakes</strong>; blame the system instead. The system won’t hold a grudge, I promise. Shift the user’s attention to how the system could not process the action, and explain to them <strong>how to find a solution</strong>.</p>

<p>A little trick is to <strong>read your own message out loud.</strong> It will help you hear whether it works or is too harsh or too casual, etc.</p>

<p>You could also get creative with error messages and <strong>incorporate imagery and humour</strong> to make them less threatening. This will really depend on your brand’s identity and tone, though.</p>

<p>To help you write better error message, I suggest you read the following:</p>

<ul>
<li>“”</li>
<li>“”</li>
</ul>

<h3 id="time-to-submit-the-form">Time To Submit The Form</h3>

<p>The user has filled in the form, there are no more errors, and everything looks good. Finally, it’s time to submit the form!</p>

<p>The first rule is, don’t <strong>mask the submit button</strong>. Seriously! I wonder what twisted mind came up with this idea, but I’ve seen it in some forms. The submit button would be displayed only once all required fields were filled in without any errors. It’s disturbing for the user to wonder whether something is wrong or the form’s button has not loaded or the website is broken and so on.</p>

<p>If you don’t want users to be able to hit the submit button if there’s missing mandatory fields or there are validation errors, use <strong>the <code>disabled</code> HTML attribute on the <code>submit</code> input</strong>. You will need to re-enable the button using JavaScript once the form is valid and ready for submission.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/13670ab0-534c-4285-a215-173098f8bab5/making-mobile-form-experience-better-35-info-en-contexte.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/13670ab0-534c-4285-a215-173098f8bab5/making-mobile-form-experience-better-35-info-en-contexte.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/13670ab0-534c-4285-a215-173098f8bab5/making-mobile-form-experience-better-35-info-en-contexte.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/13670ab0-534c-4285-a215-173098f8bab5/making-mobile-form-experience-better-35-info-en-contexte.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/13670ab0-534c-4285-a215-173098f8bab5/making-mobile-form-experience-better-35-info-en-contexte.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/13670ab0-534c-4285-a215-173098f8bab5/making-mobile-form-experience-better-35-info-en-contexte.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/13670ab0-534c-4285-a215-173098f8bab5/making-mobile-form-experience-better-35-info-en-contexte.jpg"
			sizes="100vw"
			alt="Do not hide the submit button. Instead, deactivate it until users have filled in the required information."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Do not hide the submit button. Instead, deactivate it until users have filled in the required information. ()
		</figcaption>
	
</figure>


<p>If you have a <strong>primary and secondary call to action, use color, size and styling to show the hierarchy</strong>.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a3ebae2a-8573-436a-94cf-0e98e2268e9a/making-mobile-form-experience-better-36-call-to-action-priorisation.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a3ebae2a-8573-436a-94cf-0e98e2268e9a/making-mobile-form-experience-better-36-call-to-action-priorisation.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a3ebae2a-8573-436a-94cf-0e98e2268e9a/making-mobile-form-experience-better-36-call-to-action-priorisation.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a3ebae2a-8573-436a-94cf-0e98e2268e9a/making-mobile-form-experience-better-36-call-to-action-priorisation.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a3ebae2a-8573-436a-94cf-0e98e2268e9a/making-mobile-form-experience-better-36-call-to-action-priorisation.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a3ebae2a-8573-436a-94cf-0e98e2268e9a/making-mobile-form-experience-better-36-call-to-action-priorisation.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a3ebae2a-8573-436a-94cf-0e98e2268e9a/making-mobile-form-experience-better-36-call-to-action-priorisation.jpg"
			sizes="100vw"
			alt="Example of primary and secondary actions"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Example of primary and secondary actions ()
		</figcaption>
	
</figure>


<p>If are wondering whether the confirmation button should come before or after the cancellation button, so am I (and a lot of other people). If you are building a native app, . It’s become particularly fun since Android changed the button positions in its fourth version. On the web, it’s more complicated because there are no real guidelines. Regardless of the OS, here are some general guidelines for mobile-optimized submit buttons:</p>

<ul>
<li>Give the <strong>call to action descriptive, actionable verbs.</strong></li>
<li>Provide <strong>visual feedback when the user taps it.</strong></li>
<li>If you have two buttons, <strong>make the primary action stand out</strong>.</li>
<li>Unless you’re working on a very specific back-office enterprise form (in which case, you’ll have a lot of challenges optimizing for mobile), <strong>avoid a reset button</strong>. Users might confuse it with the submit button and will lose all of their data by accident.</li>
</ul>

<h3 id="conclusion">Conclusion</h3>

<p>In this first part, I’ve discussed a lot of little techniques to take your form to the next level and help users fill it in. Some of these general guidelines and mobile best practices might not work 100% of the time — that’s the catch with best practices. So, <strong>always test your forms on real users and real devices, and adapt the guidelines to your users’ specific needs and experience.</strong></p>

<p>Also, do some regression and automated functional testing — again, on real devices. Chrome’s mobile emulator won’t be enough to test touch-optimized forms. I say this because I had launched an e-commerce website with a search form that didn’t work on mobile. We only did automated testing using an emulator. Here is what happened. The search form was hidden under a search icon. You could tap on the button, which opened a box with the search field. It worked by emulating a mouse hover as a touch event. We tested tapping on the button, and it opened the box. Nobody tried to launch a search. So, nobody (not even the client) saw that the search field disappeared as soon as users tried to interact with it. What happened? When the input element got focus, the button lost the hover state, so it closed the box with the field. Automated testing was not able to catch this because the input was not losing focus. So, we launched an e-commerce website without search functionality on mobile. Not a super experience.</p>

<p>In the second part of this series, we will see more advanced mobile-specific techniques. We will see how to use cool HTML5 features to format fields and how to use mobile capabilities to take the mobile user experience to the next level.</p>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(lf, ra, al, il)</span>
</div>


              </article>
            </body>
          </html>
---------------
<h1 id="#title_1" >2、文章： 我用Vue和React构建了相同的应用程序，这是他们的差异</h1>
Sunil Sandhu
[http://www.infoq.com/cn/articles/differences-between-react-and-vue?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/differences-between-react-and-vue?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/differences-between-react-and-vue/zh/smallimage/LOGOpair-1534610279205.jpg"/><p>在工作中使用了Vue之后，我已经对它有了相当深入的了解。同时，我也对React感到好奇。我阅读了React的文档，也看了一些教程视频，虽然它们很棒，但我真正想知道的是React与Vue有哪些区别。这里所说的区别，并不是指它们是否都具有虚拟DOM或者它们如何渲染页面。我真正想要做的是对它们的代码进行并排比较，并搞清楚在使用这两个框架开发应用时究竟有哪些差别。</p> <i>By Sunil Sandhu</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_2" >3、通过XAML Islands使Windows桌面应用程序现代化</h1>
Jonathan Allen
[http://www.infoq.com/cn/news/2018/08/Modern-Desktop-Applications?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/08/Modern-Desktop-Applications?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>你可能会觉得，Windows桌面开发已经彻底完蛋了，但根据Visual Studio中的遥测数据，每个月有大约240万开发人员在积极地开发桌面应用程序，比20个月前增长了50%。有一个如此大的社区支持，微软正在寻找方法，帮助开发人员把那些资产整合进Windows 10。</p> <i>By Jonathan Allen</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_3" >4、文章： 将Web站点改造为渐进式Web应用</h1>
Craig Buckler
[http://www.infoq.com/cn/articles/retrofit-your-website-as-a-progressive-web-app?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/retrofit-your-website-as-a-progressive-web-app?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/retrofit-your-website-as-a-progressive-web-app/zh/smallimage/images+%282%29-1534608263033.jpg"/><p>最近围绕渐进式Web应用（PWA）有很多的讨论，很多人在怀疑它是不是代表了（移动）Web的未来。在本文中，作者以实际的样例阐述了如何将一个已有的Web站点改造为PWA，改造后的站点在行为上与原生Web应用相同，它能够离线运行并且具有自己的主页屏幕图标。</p> <i>By Craig Buckler</i> <i> Translated by 张卫滨 </i>
---------------
<h1 id="#title_4" >5、文章： 苏宁MOCK测试桩服务建设实践</h1>
程派峰
[http://www.infoq.com/cn/articles/suning-mock-test?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/suning-mock-test?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/suning-mock-test/zh/smallimage/GettyImages-628837052-1518704902676-1534611961866.jpeg"/><p>2018 年苏宁易购提出了智慧零售大开发战略，快速的发展速度对苏宁的 IT 技术提出了更高的要求，其中一个重要的环节就是加快软件版本的上线步伐，伴随着软件的上线必然存在巨大的测试压力。</p> <i>By 程派峰</i>
---------------
<h1 id="#title_5" >6、微信的历史</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2018/08/weixin.html](http://www.ruanyifeng.com/blog/2018/08/weixin.html)
<p>上周，香港的《南华早报》有一个，介绍了微信如何变成中国用户最多的手机 App。</p>

        <p>我读了很有收获，就结合和其他公开的资料，总结了一份微信的发展史。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201808/bg2018082001.png" alt="" title="" /></p>

<p><strong>2010年6月</strong>，苹果发布 iPhone 4。当年中国的智能手机销量是3610万部，2011年就猛增到9060万部，2012年更是飙升到2.142亿部。很显然，手机软件（尤其是即时通信软件）即将爆发。</p>

<p><strong>2010年10月</strong>，腾讯广州研发中心开始开发微信。研发负责人是张小龙，当时是 QQ 邮件移动版的负责人。2005年，他的前一个产品 Foxmail 被腾讯收购，他因此加入腾讯。他带领一支不到10人的团队，不到70天的时间内开发出了第一版微信，击败了另外两个内部同类项目。腾讯公司总裁马化腾确定这款产品的名称叫做"微信"。</p>

<p><strong>2011年1月21日</strong>，微信正式发布，第一版只允许用户发送文本和照片，不能发送短信。一位用户在苹果公司的 App 商店留言："不能像飞信那样，给其它手机发免费短信，我不知道这种产品有什么意义。"但是，飞信（feixin）当时不愿意向非中国移动的用户开放它的短信功能，导致没有能进一步占领市场。</p>

<p><strong>2011年5月</strong>，微信推出了"语音消息"这个关键功能，让用户的手机变成对讲机那样工作，每条语音消息不能超过60秒。马化腾后来说："语音消息将不习惯在智能手机上打字的商人转变为微信用户。"微信的每日用户增长从 10000 增加到了 60000。</p>

<p><strong>2011年7月</strong>，微信增加了基于位置的服务"附近的人"、"漂流瓶"和"摇一摇"，允许用户与附近的陌生人联系。每日用户增长跳升到了100,000。</p>

<p><strong>2012年3月</strong>，微信达到1亿注册用户，这时距离产品推出433天。</p>

<p><strong>2012年4月</strong>，微信开始国际化，英文名称定为"WeChat"，并推出了多语言版本。</p>

<p><strong>2012年5月</strong>，微信推出"朋友圈"，允许用户分享自己的生活。这使得微信从一个即时通信软件，向社交网络发展。</p>

<p><strong>2012年8月</strong>，微信增加"视频通话"功能，并且提供了网页版。</p>

<p><strong>2012年9月17日</strong>，微信达到2亿注册用户。</p>

<p><strong>2013年1月15日</strong>，达到3亿注册用户，成为全球用户最多的通信软件。</p>

<p><strong>2013年8月</strong>，微信添加了公众号、微信支付、表情商店和游戏中心等大量功能。公众号使得微信变成内容平台，游戏中心使得微信具备娱乐功能，游戏中心的第一个游戏是"飞机大战"。微信支付最早只限于游戏内的支付，后来才演变成通用的支付工具。</p>

<p><strong>2013年8月</strong>，中国以外的注册用户达到1亿。</p>

<p><strong>2014年1月</strong>，腾讯联合创始人张志东希望改变传统的向腾讯员工发红包的形式，就委托微信团队的一个工程师开发了微信的红包功能。这个功能在春节前夕向公众开放，结果一炮而红，那年春节超过800万中国人收到超过4000万个红包。为了发红包，用户开始将他们的银行账户，绑定到微信手机钱包，这使得微信有能力与支付宝竞争。阿里巴巴创始人马云称这件事是"袭击珍珠港"。</p>

<p><strong>2014年10月</strong>，朋友圈允许发布短视频。</p>

<p><strong>2015年5月</strong>，增加微信运动功能，可以记录用户每天走了多少步，并给出排名。</p>

<p><strong>2016年1月</strong>，张小龙宣布正在研发小程序，这个功能允许商家和第三方开发者在微信里面运行自己的应用程序，完成一些特殊功能，比如点餐和购物，用户不用额外安装。对于微信来说，小程序可以提供用户粘性，并且增加线下服务的能力。</p>

<p><strong>2017年1月</strong>，小程序的开发指南和 API 正式发布。</p>

<p><strong>2017年12月</strong>，微信正式推出小游戏，它属于小程序的一个类别。同时发布了一个小游戏"跳一跳"作为演示，这个游戏的日活跃用户达到1亿。</p>

<p><strong>2018年2月</strong>，除夕夜共有6.88亿用户使用了微信红包。当月，微信的全球活跃用户达到了10亿。</p>

<p><strong>2018年6月</strong>，微信小程序数量超过100万，用户超过6亿。小程序将最终使得微信成为一个生态体系，其中可以进行各种各样的业务，为腾讯创造出无数的商业可能。</p>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2018-08-20T14:00:54+08:00">2018年8月20日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>文集：</li>
<li>社交媒体：</li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------
<h1 id="#title_6" >7、最新版Byte Buddy完全支持Java 11</h1>
Ben Evans
[http://www.infoq.com/cn/news/2018/08/byte-buddy-java11?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/08/byte-buddy-java11?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Java字节码工程库Byte Buddy最新版本完全支持Java 11以及自Java 8以来引入的所有类文件和字节码新特性。</p> <i>By Ben Evans</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_7" >8、Rust 2018临近：设法从Rust 2015过渡</h1>
Sergio De Simone
[http://www.infoq.com/cn/news/2018/08/handling-rust-2018-transition?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/08/handling-rust-2018-transition?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>据Rust核心团队报道，Rust 2018（对应Rust 1.31）的第一个版本将于2018年12月6日准备就绪。从Rust 2015首次发布以来，大量新特性合并到一个新的标签下，大大丰富了这门语言。</p> <i>By Sergio De Simone</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_8" >9、谷歌云平台发布Edge TPU和Cloud IoT Edge</h1>
Steef-Jan Wiggers
[http://www.infoq.com/cn/news/2018/08/google-iot-edge-tpu-ai?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/08/google-iot-edge-tpu-ai?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>谷歌宣布将在他们的云平台上推出两款新产品，帮助客户在他们的网络“边缘”开发和部署离最终用户最近的设备。这些产品分别是Edge TPU（一种新的硬件芯片）和Cloud IoT Edge（针对网关和连接设备的谷歌云AI功能的扩展）。</p> <i>By Steef-Jan Wiggers</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_9" >10、保持分布式团队同步</h1>
Ben Linders
[http://www.infoq.com/cn/news/2018/08/distributed-teams?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/08/distributed-teams?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>分布式团队最大的挑战是沟通，这对建立协作的基本原则必不可少。调整工作时间，互相适应，而团队联络员有助于沟通和同步工作。以信任、尊重和开明为基础的团队会鼓励组织中的人们互相帮助，培养一种使团队保持同步的文化。</p> <i>By Ben Linders</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_10" >11、文章： 无服务器仍然离不开基础设施管理</h1>
Rafal Gancarz
[http://www.infoq.com/cn/articles/serverless-infrastructure-management?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/serverless-infrastructure-management?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/serverless-infrastructure-management/zh/smallimage/serverless-infrastructure-management-logo-1533656754512-1534673365249.jpg"/><p>为了在无服务器时代有效地管理云基础设施，相关的理念、实践和工具必须不断发展。</p> <i>By Rafal Gancarz</i> <i> Translated by 无明</i>
---------------