## 文章索引
1、 <a href="#1文章-从sun离职后我抛弃了java拥抱javascript和node" >文章： 从Sun离职后，我“抛弃”了Java，拥抱JavaScript和Node</a><br/>
2、 <a href="#2designing-a-textbox-unabridged" >Designing A Textbox, Unabridged</a><br/>
3、 <a href="#3文章-波士顿儿童医院如何利用开放云创新" >文章： 波士顿儿童医院如何利用开放云创新</a><br/>
4、 <a href="#4文章-如何实现靠谱的分布式锁" >文章： 如何实现靠谱的分布式锁？</a><br/>
5、 <a href="#5eclipse发布microprofile-14和20" >Eclipse发布MicroProfile 1.4和2.0</a><br/>
6、 <a href="#6新西兰一家公司试验四天工作周" >新西兰一家公司试验四天工作周</a><br/>
7、 <a href="#7客户并非始终正确你也不是永远正确的" >客户并非始终正确，你也不是永远正确的</a><br/>
8、 <a href="#8都说是下一个十年dapp为什么还如此冷清" >都说是下一个十年，DApp为什么还如此冷清？</a><br/>
9、 <a href="#9联盟链华山论剑开启fisco-bcos上的底层与场景之战" >联盟链“华山论剑”，开启FISCO BCOS上的底层与场景之战</a><br/><h1 id="#title_0" >1、文章： 从Sun离职后，我“抛弃”了Java，拥抱JavaScript和Node</h1>
David Herron
[http://www.infoq.com/cn/articles/why-is-a-java-guy-so-excited-about-node-js-and-javascript?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/why-is-a-java-guy-so-excited-about-node-js-and-javascript?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/why-is-a-java-guy-so-excited-about-node-js-and-javascript/zh/smallimage/logo-data-1513200536971-1535711553109.jpeg"/><p>在这篇文章中，我将会解释我这个Java死忠是如何变成一个Node.js和JavaScript死忠的。</p> <i>By David Herron</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_1" >2、Designing A Textbox, Unabridged</h1>
Shane Hudson
[https://www.smashingmagazine.com/2018/09/designing-a-textbox-unabridged/](https://www.smashingmagazine.com/2018/09/designing-a-textbox-unabridged/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/09/designing-a-textbox-unabridged/" />
              <title>Designing A Textbox, Unabridged</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>Designing A Textbox, Unabridged</h1>
                  
                    
                    <address>Shane Hudson</address>
                  
                  <time datetime="2018-09-06T13:30:16&#43;02:00" class="op-published">2018-09-06T13:30:16+02:00</time>
                  <time datetime="2018-09-06T11:42:22&#43;00:00" class="op-modified">2018-09-06T11:42:22+00:00</time>
                </header>
                

<p>Ever spent an hour (or even a day) working on something just to throw the whole lot away and redo it in five minutes? That isn&rsquo;t just a beginner’s code mistake; it is a real-world situation that you can easily find yourself in especially if the problem you&rsquo;re trying to solve isn&rsquo;t well understood to begin with.</p>

<p>This is why I’m such a big proponent of upfront design, user research, and creating often multiple prototypes &mdash; also known as the old adage of “You don&rsquo;t know what you don&rsquo;t know.” At the same time, it is very easy to look at something someone else has made, which may have taken them quite a lot of time, and think it is extremely easy because you have the benefit of hindsight by seeing a finished product.</p>

<p>This idea that simple is easy was summed up nicely by  while speaking about CSS Grid and Piet Mondrian’s paintings:</p>

<blockquote>“I feel like these paintings, you know, if you look at them with the sense of like ‘Why’s that important? I could have done that.’ It's like, well yeah, you could paint that today because we’re so used to this kind of thinking, but would you have painted this when everything around you was Victorian &mdash; when everything around you was this other style?”</blockquote>

<p>I feel this sums up the feeling I have about seeing websites and design systems that make complete sense; it’s almost as if the fact they make sense means they were easy to make. Of course, it is usually the opposite; writing the code is the simple bit, but it’s the thinking and process that goes into it that takes the most effort.</p>

<p>With that in mind, I’m going to explore building a text box, in an exaggeration of situations many of us often find ourselves in. Hopefully, by the end of this article, we can all feel more emphatic to how the journey from start to finish is rarely linear.</p>

<div class="c-felix-the-cat">
<h4>A Comprehensive Guide To User Testing</h4>
<p>So you think you’ve designed something that’s perfect, but your test tells you otherwise. Let’s explore the importance of user testing.  </p>
</div>



<aside class="product-panel product-panel__tilted product-panel--book" data-audience="non-subscriber">
    <div class="container product-panel--book__container">
      <div class="panel__description panel__description--book">
    <p>Getting workflow <em>just</em> right ain’t an easy task. So are proper estimates. Or alignment among different departments. That’s why we’ve set up <strong>“this-is-how-I-work”-sessions</strong> — with smart cookies sharing what works well for them. A part of the , of course.</p>
      <a href="https://smashed.by/workflowpanelmembership" class="btn btn--green btn--large">
        Explore features&nbsp;→
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




<h3 id="brief">Brief</h3>

<p>We all know that careful planning and understanding of the user need is important to a successful project of any size. We also all know that all too often we feel to need to rush to quickly design and develop new features. That can often mean our common sense and best practices are forgotten as we slog away to quickly get onto the next task on the everlasting to-do list. Rinse and repeat.</p>

<p>Today our task is to build a text box. Simple enough, it needs to allow a user to type in some text. In fact, it is so simple that we leave the task to last because there is so much other important stuff to do. Then, just before we pack up to go home, we smirk and write:</p>

<pre><code class="language-html">&lt;input type="text"&gt;
</code></pre>

<p>There we go!</p>

<p>Oh wait, we probably need to hook that up to send data to the backend when the form is submitted, like so:</p>

<pre><code class="language-html">&lt;input type="text" name="our_textbox"&gt;
</code></pre>

<p>That’s better. Done. Time to go home.</p>

<h3 id="how-do-you-add-a-new-line">How Do You Add A New Line?</h3>

<p>The issue with using a simple text box is it is pretty useless if you want to type a lot of text. For a name or title it works fine, but quite often a user will type more text than you expect. Trust me when I say if you leave a textbox for long enough without strict validation, someone will paste the entire of War and Peace. In many cases, this can be prevented by having a maximum amount of characters.</p>

<p>In this situation though, we have found out that our laziness (or bad prioritization) of leaving it to the last minute meant we didn’t consider the real requirements. We just wanted to do another task on that everlasting to-do list and get home. This text box needs to be reusable; examples of its usage include as a content entry box, a Twitter-style note box, and a user feedback box. In all of those cases, the user is likely to type a lot of text, and a basic text box would just scroll sideways. Sometimes that may be okay, but generally, that’s an awful experience.</p>

<p>Thankfully for us, that simple mistake doesn’t take long to fix:</p>

<pre><code class="language-html">&lt;textarea name="our_textbox"&gt;&lt;/textarea&gt;
</code></pre>

<p>Now, let’s take a moment to consider that line. A <code>&lt;textarea&gt;</code>: as simple as it can get without removing the name. Isn’t it interesting, or is it just my pedantic mind that we need to use a completely different element to add a new line? It isn’t a type of input, or an attribute used to add multi-line to an input. Also, the <code>&lt;textarea&gt;</code> element is not self-closing but an input is? Strange.</p>

<p>This “moment to consider” sent me time traveling back to October 1993, trawling through the depths of the  said:</p>

<blockquote>“Well, it's far-fetched I suppose, but you might use HTML forms as part of a game playing interface.”</blockquote>

<p>This really does show that the web wasn’t just intended to be about documents as is widely believed. Marc Andreessen )</p>

<blockquote>“Makes the browser code cleaner &mdash; they have to be handled differently internally.”</blockquote>

<p>That’s a fair reason to have <code>&lt;textarea&gt;</code> separate to text, but that’s still not what we ended up with. So why is <code>&lt;textarea&gt;</code> its own element?</p>

<p>I didn’t find any decision in the mailing list archives, but by the following month, the  had the <code>&lt;textarea&gt;</code> element and a note saying:</p>

<blockquote>“In the initial design for forms, multi-line text fields were supported by the INPUT element with TYPE=TEXT. Unfortunately, this causes problems for fields with long text values as SGML limits the length of attributea literals. The HTML+ DTD allows for up to 1024 characters (the SGML default is only 240 characters!)”</blockquote>

<p>Ah, so that’s why the text goes within the element and cannot be self-closing; they were not able to use an attribute for long text. In 1994, the <code>&lt;textarea&gt;</code> element was included, along with many others from HTML+ such as <code>&lt;option&gt;</code> in the HTML 2 spec.</p>

<p>Okay, that’s enough. I could easily explore the archives further but back to the task.</p>

<h3 id="styling-a-textarea">Styling A <code>&lt;textarea&gt;</code></h3>

<p>So we’ve got a default <code>&lt;textarea&gt;</code>. If you rarely use them or haven’t seen the browser defaults in a long time, then you may be surprised. A <code>&lt;textarea&gt;</code> (made almost purely for multi-line text) looks very similar to a normal text input except most browser defaults style the border darker, the box slightly larger, and there are lines in the bottom right. Those lines are the resize handle; they aren’t actually part of the spec so browsers all handle (pun absolutely intended) it in their own way. That generally means that the resize handle cannot be restyled, though you can disable resizing by setting <code>resize: none</code> to the <code>&lt;textarea&gt;</code>. It is possible to create a custom handle or use browser specific pseudo elements such as <code>::-webkit-resizer</code>.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6f354a41-76e5-457e-8a08-41e4a201d7ad/textbox-unabridged-default-textarea.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6f354a41-76e5-457e-8a08-41e4a201d7ad/textbox-unabridged-default-textarea.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6f354a41-76e5-457e-8a08-41e4a201d7ad/textbox-unabridged-default-textarea.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6f354a41-76e5-457e-8a08-41e4a201d7ad/textbox-unabridged-default-textarea.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6f354a41-76e5-457e-8a08-41e4a201d7ad/textbox-unabridged-default-textarea.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6f354a41-76e5-457e-8a08-41e4a201d7ad/textbox-unabridged-default-textarea.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6f354a41-76e5-457e-8a08-41e4a201d7ad/textbox-unabridged-default-textarea.png"
			sizes="100vw"
			alt="The default &lt;code&gt;&amp;lt;textarea&amp;gt;&lt;/code&gt; looks very small with a grey border and three lines as a resize handle."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			A default textarea with no styling ()
		</figcaption>
	
</figure>


<p>It’s important to understand the defaults, especially because of the resizing ability. It’s a very unique behavior; the user is able to drag to change the size of the element by default. If you don’t override the minimum and maximum sizes then the size could be as small as 9px&nbsp;&times;&nbsp;9px (when I checked Chrome) or as large as they have patience to drag it. That’s something that could cause mayhem with the rest of the site’s layout if it’s not considered. Imagine a grid where <code>&lt;textarea&gt;</code> is in one column and a blue box is in another; the size of the blue box is purely decided by the size of the <code>&lt;textarea&gt;</code>.</p>

<p>Other than that, we can approach styling a <code>&lt;textarea&gt;</code> much the same as any other input. Want to change the grey around the edge into thick green dashes? Sure here you go: <code>border: 5px dashed green;</code>. Want to restyle the focus in which a lot of browsers have a slightly blurred box shadow? Change the outline &mdash; responsibly though, you know, that’s important for accessibility. You can even add a background image to your <code>&lt;textarea&gt;</code> if that interests you (I can think of a few ideas that would have been popular when skeuomorphic design was more celebrated).</p>

<div class="sponsors__wide-place"></div>




<h3 id="scope-creep">Scope Creep</h3>

<p>We’ve all experienced scope creep in our work, whether it is a client that doesn’t think the final version matches their idea or you just try to squeeze in a tiny tweak and end up taking forever to finish it. So I ( enjoying creating the persona of an exaggerated project manager telling us what we need to build) have decided that our <code>&lt;textarea&gt;</code> just is not good enough. Yes, it is now multi-line, and that’s great, and yes it even ‘pops’ a bit more with its new styling. Yet, it just doesn’t fit the very vague user need that I’ve pretty much just thought of now after we thought we were almost done.</p>

<p>What happens if the user puts in thousands of words? Or drags the resize handle so far it breaks the layout? It needs to be reusable, as we have already mentioned, but in some of the situations (such as a ‘Twittereqsue’ note taking box), we will need a limit. So the next task is to add a character limit. The user needs to be able to see how many characters they have left.</p>

<p>In the same way we started with <code>&lt;input&gt;</code> instead of <code>&lt;textarea&gt;</code>, it is very easy to think that adding the <code>maxlength</code> attribute would solve our issue. That is one way to limit the amount of characters the user types, it uses the browser’s built-in validation, but it is not able to display how many characters are left.</p>

<p>We started with the HTML, then added the CSS, now it is time for some JavaScript. As we’ve seen, charging along like a bull in a china shop without stopping to consider the right approaches can really slow us down in the long run. Especially in situations where there is a large refactor required to change it. So let’s think about this counter; it needs to update as the user types, so we need to trigger an event when the user types. It then needs to check if the amount of text is already at the maximum length.</p>

<p>So which event handler should we choose?</p>

<ul>
<li><strong><code>change</code></strong><br />
Intuitively, it may make sense to choose the change event. It works on <code>&lt;textarea&gt;</code> and does what it says on the tin. Except, it only triggers when the element loses focus so it wouldn’t update while typing.</li>
<li><strong><code>keypress</code></strong><br />
The keypress event is triggered when typing any character, which is a good start. But it does not trigger when characters are deleted, so the counter wouldn’t update after pressing backspace. It also doesn’t trigger after a copy/paste.</li>
<li><strong><code>keyup</code></strong><br />
This one gets quite close, it is triggered whenever a key has been pressed (including the backspace button). So it does trigger when deleting characters, but still not after a copy/paste.</li>
<li><strong><code>input</code></strong><br />
This is the one we want. This triggers whenever a character is added, deleted or pasted.</li>
</ul>

<p>This is another good example of how using our intuition just isn’t enough sometimes. There are so many quirks (especially in JavaScript!) that are all important to consider before getting started. So the code to add a counter that updates needs to update a counter (which we’ve done with a span that has a class called <code>counter</code>) by adding an <code>input</code> event handler to the <code>&lt;textarea&gt;</code>. The maximum amount of characters is set in a variable called <code>maxLength</code> and added to the HTML, so if the value is changed it is changed in only one place.</p>

<pre><code class="language-javascript">var textEl = document.querySelector('textarea')
var counterEl = document.querySelector('.counter')
var maxLength = 200
    
textEl.setAttribute('maxlength', maxLength)
textEl.addEventListener('input', (val) => {
var count = textEl.value.length
counterEl.innerHTML = ${count}/${maxLength}
})
</code></pre>

<h3 id="browser-compatibility-and-progressive-enhancement">Browser Compatibility And Progressive Enhancement</h3>

<p>Progressive enhancement is a mindset in which we understand that we have no control over what the user exactly sees on their screen, and instead, we try to guide the browser. Responsive Web Design is a good example, where we build a website that adjusts to suit the content on the particular size viewport without manually setting what each size would look like. It means that on the one hand, we strongly care that a website works across all browsers and devices, but on the other hand, we don’t care that they look exactly the same.</p>

<p>Currently, we are missing a trick. We haven’t set a sensible default for the counter. The default is currently “0/200” if 200 were the maximum length; this kind of makes sense but has two downsides. The first, it doesn’t really make sense at first glance. You need to start typing before it is obvious the 0 updates as you type. The other downside is that the 0 updates as you type, meaning if the JavaScript event doesn’t trigger properly (maybe the script did not download correctly or uses JavaScript that an old browser doesn’t support such as the double arrow in the code above) then it won’t do anything. A better way would be to think carefully beforehand. How would we go about making it useful when it is both working and when it isn’t?</p>

<p>In this case, we could make the default text be “200 character limit.” This would mean that without any JavaScript at all, the user would always see the character limit but it just wouldn’t feedback about how close they are to the limit. However, when the JavaScript is working, it would update as they type and could say “200 characters remaining” instead. It is a very subtle change but means that although two users could get different experiences, neither are getting an experience that feels broken.</p>

<p>Another default that we could set is the <code>maxlength</code> on the element itself rather than afterwards with JavaScript. Without doing this, the baseline version (the one without JS) would be able to type past the limit.</p>

<h3 id="user-testing">User Testing</h3>

<p>It’s all very well testing on various browsers and thinking about the various permutations of how devices could serve the website in a different way, but are users able to use it?</p>

<p>Generally speaking, no. I’m consistently shocked by user testing; <strong>people never use a site how you expect them to</strong>. This means that user testing is crucial.</p>

<p>It’s quite hard to simulate a user test session in an article, so for the purposes of this article, I’m going to just focus on one point that I’ve seen users struggle with on various projects.</p>

<p>The user is happily writing away, gets to 0 characters remaining, and then gets stuck. They forget what they were writing, or they don’t notice that it had stopped typing.</p>

<p>This happens because there is nothing telling the user that something has changed; if they are typing away without paying much attention, then they can hit the maximum length without noticing. This is a frustrating experience.</p>

<p>One way to solve this issue is to allow overtyping, so the maximum length still counts for it to be valid when submitted but it allows the user to type as much as they want and then edit it before submission. This is a good solution as it gives the control back to the user.</p>

<p>Okay, so how do we implement overtyping? Instead of jumping into the code, let’s step through in theory. <code>maxlength</code> doesn’t allow overtyping, it just stops allowing input once it hits the limit. So we need to remove <code>maxlength</code> and write a JS equivalent. We can use the input event handler as we did before, as we know that works on paste, etc. So in that event, the handler would check if the user has typed more than the limit, and if so, the counter text could change to say “10 characters too many.” The baseline version (without the JS) would no longer have a limit at all, so a useful middle ground could be to add the <code>maxlength</code> to the element in the HTML and remove the attribute using JavaScript.</p>

<p>That way, the user would see that they are over the limit without being cut off while typing. There would still need to be validation to make sure it isn’t submitted, but that is worth the extra small bit of work to make the user experience far better.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9bd74a36-054c-4c61-8c1f-01bfde7ebb3e/textbox-unabridged-overtype.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9bd74a36-054c-4c61-8c1f-01bfde7ebb3e/textbox-unabridged-overtype.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9bd74a36-054c-4c61-8c1f-01bfde7ebb3e/textbox-unabridged-overtype.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9bd74a36-054c-4c61-8c1f-01bfde7ebb3e/textbox-unabridged-overtype.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9bd74a36-054c-4c61-8c1f-01bfde7ebb3e/textbox-unabridged-overtype.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9bd74a36-054c-4c61-8c1f-01bfde7ebb3e/textbox-unabridged-overtype.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9bd74a36-054c-4c61-8c1f-01bfde7ebb3e/textbox-unabridged-overtype.png"
			sizes="100vw"
			alt="An example showing “17 characters too many” in red text next to a &lt;code&gt;&amp;lt;textarea&amp;gt;&lt;/code&gt;."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Allowing the user to overtype ()
		</figcaption>
	
</figure>


<h3 id="designing-the-overtype">Designing The Overtype</h3>

<p>This gets us to quite a solid position: the user is now able to use any device and get a decent experience. If they type too much it is not going to cut them off; instead, it will just allow it and encourage them to edit it down.</p>

<p>There’s a variety of ways this could be designed differently, so let’s look at how Twitter handles it:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/35a0665c-7809-492a-b90d-a8b975d02680/textbox-unabridged-twitter-overtype.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/35a0665c-7809-492a-b90d-a8b975d02680/textbox-unabridged-twitter-overtype.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/35a0665c-7809-492a-b90d-a8b975d02680/textbox-unabridged-twitter-overtype.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/35a0665c-7809-492a-b90d-a8b975d02680/textbox-unabridged-twitter-overtype.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/35a0665c-7809-492a-b90d-a8b975d02680/textbox-unabridged-twitter-overtype.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/35a0665c-7809-492a-b90d-a8b975d02680/textbox-unabridged-twitter-overtype.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/35a0665c-7809-492a-b90d-a8b975d02680/textbox-unabridged-twitter-overtype.png"
			sizes="100vw"
			alt="A screenshot from Twitter showing their textarea with overtyped text with a red background."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Twitter's <code>&lt;textarea&gt;</code> ()
		</figcaption>
	
</figure>


<p>Twitter has been iterating its main tweet <code>&lt;textarea&gt;</code> since they started the company. The current version uses a lot of techniques that we could consider using.</p>

<p>As you type on Twitter, there is a circle that completes once you get to the character limit of 280. Interestingly, it doesn’t say how many characters are available until you are 20 characters away from the limit. At that point, the incomplete circle turns orange. Once you have 0 characters remaining, it turns red. After the 0 characters, the countdown goes negative; it doesn’t appear to have a limit on how far you can overtype (I tried as far as 4,000 characters remaining) but the tweet button is disabled while overtyping.</p>

<p>So this works the same way as our <code>&lt;textarea&gt;</code> does, with the main difference being the characters represented by a circle that updates and shows the number of characters remaining after 260 characters. We could implement this by removing the text and replacing it with an SVG circle.</p>

<p>The other thing that Twitter does is add a red background behind the overtyped text. This makes it completely obvious that the user is going to need to edit or remove some of the text to publish the tweet. It is a really nice part of the design. So how would we implement that? We would start again from the beginning.</p>

<div class="sponsors__wide-place"></div>




<p>You remember the part where we realized that a basic input text box would not give us multiline? And that a <code>maxlength</code> attribute would not give us the ability to overtype? This is one of those cases. As far as I know, there is nothing in CSS that gives us the ability to style parts of the text inside a <code>&lt;textarea&gt;</code>. This is the point where some people would suggest web components, as what we would need is a pretend <code>&lt;textarea&gt;</code>. We would need some kind of element &mdash; probably a div &mdash; with <code>contenteditable</code> on it and in JS we would need to wrap the overtyped text in a span that is styled with CSS.</p>

<p>What would the baseline non-JS version look like then? Well, it wouldn’t work at all because while <code>contenteditable</code> will work without JS, we would have no way to actually do anything with it. So we would need to have a <code>&lt;textarea&gt;</code> by default and remove that if JS is available. We would also need to do a lot of accessibility testing because while we can trust a <code>&lt;textarea&gt;</code> to be accessible relying on browser features is a much safer bet than building your own components. How does Twitter handle it? You may have seen it; if you are on a train and your JavaScript doesn’t load while going into a tunnel then you get chucked into a decade-old legacy version of Twitter where there is no character limit at all.</p>

<p>What happens then if you tweet over the character limit? Twitter reloads the page with an error message saying “Your Tweet was over the character limit. You&rsquo;ll have to be more clever.” No, Twitter. <em>You</em> need to be more clever.</p>

<h3 id="retro">Retro</h3>

<p>The only way to conclude this dramatization is a retrospective. What went well? What did we learn? What would we do differently next time or what would we change completely?</p>

<p>We started very simple with a basic textbox; in some ways, this is good because it can be all too easy to overcomplicate things from the beginning and an MVP approach is good. However, as time went on, we realized how important it is to have some critical thinking and to consider what we are doing. We should have known a basic textbox wouldn’t be enough and that a way of setting a maximum length would be useful. It is even possible that if we have conducted or sat in on user research sessions in the past that we could have anticipated the need to allow overtyping. As for the browser compatibility and user experiences across devices, considering progressive enhancement from the beginning would have caught most of those potential issues.</p>

<p>So one change we could make is to be much more proactive about the thinking process instead of jumping straight into the task, thinking that the code is easy when actually the code is the least important part.</p>

<p>On a similar vein to that, we had the “scope creep” of <code>maxlength</code>, and while we could possibly have anticipated that, we would rather not have any scope creep at all. So everybody involved from the beginning would be very useful, as a diverse multidisciplinary approach to even small tasks like this can seriously reduce the time it takes to figure out and fix all the unexpected tweaks.</p>

<h3 id="back-to-the-real-world">Back To The Real World</h3>

<p>Okay, so I can get quite deep into this made-up project, but I think it demonstrates well how complicated the most seemingly simple tasks can be. Being user-focussed, having a progressive enhancement mindset, and thinking things through from the beginning can have a real impact on both the speed and quality of delivery. And I didn’t even mention testing!</p>

<p>I went into some detail about the history of the <code>&lt;textarea&gt;</code> and which event listeners to use, some of this can seem overkill, but I find it fascinating to gain a real understanding of the subtleties of the web, and it can often help demystify issues we will face in the future.</p>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(ra, il)</span>
</div>


              </article>
            </body>
          </html>
---------------
<h1 id="#title_2" >3、文章： 波士顿儿童医院如何利用开放云创新</h1>
Jennifer Riggins
[http://www.infoq.com/cn/articles/open-private-cloud?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/open-private-cloud?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/open-private-cloud/zh/smallimage/how-the-boston-childrens-hospital-is-innovating-on-top-of-open-cloud-logo-1534417456244-1536060403658.jpeg"/><p>混合开放云正在上升为像AWS这样的巨头的替代方案。本文介绍了波士顿儿童医院如何使用这项技术加速诊断和数据处理。</p> <i>By Jennifer Riggins</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_3" >4、文章： 如何实现靠谱的分布式锁？</h1>
鞠明业
[http://www.infoq.com/cn/articles/how-to-implement-distributed-lock?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/how-to-implement-distributed-lock?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/how-to-implement-distributed-lock/zh/smallimage/net-logo-1526676504145-1535710921617.jpeg"/><p>分布式锁，是用来控制分布式系统中互斥访问共享资源的一种手段，从而避免并行导致的结果不可控。基本的实现原理和单进程锁是一致的，通过一个共享标识来确定唯一性，对共享标识进行修改时能够保证原子性和和对锁服务调用方的可见性。由于分布式环境需要考虑各种异常因素，为实现一个靠谱的分布式锁服务引入了一定的复杂度。</p> <i>By 鞠明业</i>
---------------
<h1 id="#title_4" >5、Eclipse发布MicroProfile 1.4和2.0</h1>
Michael Redlich
[http://www.infoq.com/cn/news/2018/09/microprofile-1.4-and-2.0?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/09/microprofile-1.4-and-2.0?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Eclipse基金会最近发布了MicroProfile 1.4和2.0，对API进行了更新，包括全面测试兼容性套件（Test Compatibility Kits，简称TCKs）、Maven坐标、Javadocs和Git标签。这些版本和Java EE 7及Java EE 8是完全一致的。MicroProfile和Jakarta EE的协同效应引发了一些猜测，认为这两个平台有可能合并。</p> <i>By Michael Redlich</i> <i> Translated by 姚佳灵</i>
---------------
<h1 id="#title_5" >6、新西兰一家公司试验四天工作周</h1>
Rui Miguel Ferreira
[http://www.infoq.com/cn/news/2018/09/four-day-work-week?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/09/four-day-work-week?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Perpetual Guardian是新西兰的一家管理信托、遗嘱和遗产的公司。今年早些时候，公司邀请它的240名员工参加为期8周的试验。试验期间，他们每周只工作4天，享受额外的休闲日，但薪资不变。</p> <i>By Rui Miguel Ferreira</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_6" >7、客户并非始终正确，你也不是永远正确的</h1>
Angela Wick
[http://www.infoq.com/cn/news/2018/09/customer-not-always-right?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/09/customer-not-always-right?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>在最近举行的Agile 2018大会上，Natalie Warnert给出了题为“客户并非始终正确，你也不是永远正确的！”的演说，她抛出了一些发人深思的观点，让观众思考如何保证我们自己做的产品是正确的。她给出了三个团队容易陷入的困境，以及避免陷入误区的建议：错误的客户带来的困境，不成熟的解决方案带来的困境以及淹没在数据中带来的困境。</p> <i>By Angela Wick</i> <i> Translated by 刘嘉洋</i>
---------------
<h1 id="#title_7" >8、都说是下一个十年，DApp为什么还如此冷清？</h1>
前哨小兵甲
[http://www.infoq.com/cn/news/2018/09/DApp-depression?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/09/DApp-depression?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>技术发展的浪潮几乎都以十年为一个节点，Web 持续了十年，App 持续了十年，未来的十年则被认为是 DApp 的十年。但是目前还没有一个为大众所用的DApp是因为什么？ 我总结了几点原因：1. 底层链扩展性不高。2. 智能合约开发更类似于硬件开发。3. 高昂的DApp费用，以太坊年均支出大约为 90 以太币 /27000 美元，EOS部署成本加上前期运行成本约为 10628 EOS/55000 美元。开发表示：“我好穷”.....</p> <i>By 前哨小兵甲</i>
---------------
<h1 id="#title_8" >9、联盟链“华山论剑”，开启FISCO BCOS上的底层与场景之战</h1>
田宁宁
[http://www.infoq.com/cn/news/2018/09/consortium-blockchain-FISCO-BCOS?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/09/consortium-blockchain-FISCO-BCOS?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>近年来，以多方参与、智能协同与价值分享等为主要特征的分布式商业逐渐兴起，区块链和分布式账本等技术实现了分布式商业中的对等、共享与透明规则，逐渐获得认可，并成为了前沿金融科技的核心代表。</p> <i>By 田宁宁</i>
---------------