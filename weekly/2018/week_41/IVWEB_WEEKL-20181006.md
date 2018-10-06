## 文章索引
1、 <a href="#1create-react-app-20-the-next-vuejs-and-lots-of-vs-code-goodies" >Create React App 2.0, the next Vue.js, and lots of VS Code goodies</a><br/>
2、 <a href="#2taming-this-in-javascript-with-bind-operator" >Taming this In JavaScript With Bind Operator</a><br/>
3、 <a href="#3每周分享第-25-期" >每周分享第 25 期</a><br/>
4、 <a href="#4smashingconf-toronto-videos" >SmashingConf Toronto Videos</a><br/>
5、 <a href="#5文章-为什么在以太坊上构建项目注定会失败" >文章： 为什么在以太坊上构建项目注定会失败</a><br/>
6、 <a href="#6cqrs和事件源框架axon的基本概念和未来" >CQRS和事件源框架Axon的基本概念和未来</a><br/><h1 id="#title_0" >1、Create React App 2.0, the next Vue.js, and lots of VS Code goodies</h1>

[https://javascriptweekly.com/issues/406](https://javascriptweekly.com/issues/406)
<table border=0 align="center" border="0">
  <tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   ">

  <div>    
    <table border=0 border=0><tr>
<td align="left" style="padding-left: 4px; font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   "><p>#406 — October 5, 2018</p></td>
<td align="right" style="padding-right: 4px; font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   "><p></p></td>
</tr></table>
    
    <table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0 12px;"><p>JavaScript Weekly</p></td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
      <p>This past week . Over the past eight years it's been a pleasure to share projects, advice, and news with you, and see how JavaScript continues to grow and grow. We don't do it often, but sometimes its nice to mark such a milestone — if you're reading this I just wanted to say thanks. :-)<br>
      <span style="color: #666666;"><em>— Peter Cooper, editor</em></span></p>
    </td></tr></table>
<div style="   margin-top: 14px; margin-bottom: 8px;  "></div>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   ">
  
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — It’s aimed at beginners <em>but</em> this guide is really extensive and packed with examples, so it’s worth a skim unless you’re Kyle Simpson or something :-)</p>
  <p>Tyler McGinnis </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;">, a popular alternative to things like React and Angular, gives a ‘brief sneak peek’ at what’s coming in the next major version of Vue, Vue 3.0.</p>
  <p>Evan You </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Use our fast IP Geolocation API to reliably locate users, personalize content, analyze traffic, enrich forms, target ads, enforce GDPR compliance, perform redirections, prevent trial abuse, block certain countries and more. Get started with a free API key.</p>
  <p>ipdata <span style="text-transform: uppercase; padding: 1px 4px;  margin-left: 4px; font-size: 0.9em;   color: #997 !important;">sponsor</span></p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"> too.</em></p>
  <p>Joe Haddad and Dan Abramov </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"> was renamed from <em>JS Interactive</em> recently :-)</p>
  <p>The Linux Foundation </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — It’s not been pushed to its full potential yet, but WebAssembly (a binary instruction format that compilers can target to run code fast in the browser) opens up a lot of potential for the Web, though, as Ed notes, JavaScript continues to have a role to play.</p>
  <p>Ed Charbeneau </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — We always love a good Smashing Magazine walkthrough - this time out, it’s about building a basic news app (for both desktop and mobile) using Angular and Google’s Material Design principles.</p>
  <p>Rachid Sakara </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Yep, it’s one of <em>those</em> ‘awesome’ lists - this time it’s a list packed with over a hundred links to themes and extensions, both language specific and general productivity ones.</p>
  <p>Valerii Iatsko </p>
</td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0;"><p>💻 Jobs</p></td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;">.</p>
  <p>x-team </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Our small dynamic team is looking for an experienced frontend developer to help build and iterate features for an open online community for creative collaboration.
</p>
  <p>Hitrecord </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Through Hired, software engineers have transparency into salary offers, competing opportunities, and job details.</p>
  <p>Hired </p>
</td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0;"><p>📘 Tutorials and Opinions</p></td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Reproducing the sort of graph you might see on Yahoo Finance, say.</p>
  <p>Colin Eberhardt </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Using React function components to render your website’s skeleton <code>index.html</code></p>
  <p>Kent C. Dodds </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"> is a library that makes WebWorkers more transparent to work with.</p>
  <p>Paul Kinlan </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Twilio <span style="text-transform: uppercase; padding: 1px 4px;  margin-left: 4px; font-size: 0.9em;   color: #997 !important;">sponsor</span></p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>David Tang </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Goes through setting up a project with Webpack and Babel 7, highlighting the basics of Babel plus some cool features of what it can do with your code.</p>
  <p>Jan D'Hollander </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — If you’ve got some spare time at the weekend and want to get into some FP with JS, this is a good read.</p>
  <p>Lonsdorf, Benkort, Takle, et al. </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"> if that’s your kinda thing.</p>
  <p>Nader Dabit </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>James Robb </p>
</td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0;"><p>🔧 Code and Tools</p></td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Prevent bad commits, pushes, etc. by running tests or more automatically. 1.0, now just out, is a complete rewrite in TypeScript.</p>
  <p>Typicode </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Wallaby catches errors in your tests and displays the results of expressions in your editor, in real-time.</p>
  <p>Wallaby.js <span style="text-transform: uppercase; padding: 1px 4px;  margin-left: 4px; font-size: 0.9em;   color: #997 !important;">sponsor</span></p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;">.</p>
  <p>Mirosław Ciastek </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Highground is currently in beta and presents an alternative fast and easy way to test ES6 apps.</p>
  <p>Daniel Stern </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Could be useful in development as well.</p>
  <p>René Hansen </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Replace time-consuming manual QA to catch visual UI bugs automatically and start deploying faster.</p>
  <p>Percy <span style="text-transform: uppercase; padding: 1px 4px;  margin-left: 4px; font-size: 0.9em;   color: #997 !important;">sponsor</span></p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — An interesting idea that brings a JSX-style approach for managing audio nodes.</p>
  <p>James Wright </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Runs in the browser, too.</p>
  <p>Victor Ribeiro </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Runs on .NET Core 2.1 and SQL Server.</p>
  <p>Ray Fan </p>
</td></tr></table>
<table border=0 border=0><tr><td style=" font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   "></td></tr></table>
</div>

  </td></tr>
</table>





<img src="https://javascriptweekly.com/open/406/rss" width="1" height="1" />
---------------
<h1 id="#title_1" >2、Taming this In JavaScript With Bind Operator</h1>
Willian Martins
[https://www.smashingmagazine.com/2018/10/taming-this-javascript-bind-operator/](https://www.smashingmagazine.com/2018/10/taming-this-javascript-bind-operator/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/10/taming-this-javascript-bind-operator/" />
              <title>Taming &lt;code&gt;this&lt;/code&gt; In JavaScript With Bind Operator</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>Taming &lt;code&gt;this&lt;/code&gt; In JavaScript With Bind Operator</h1>
                  
                    
                    <address>Willian Martins</address>
                  
                  <time datetime="2018-10-05T14:20:22&#43;02:00" class="op-published">2018-10-05T14:20:22+02:00</time>
                  <time datetime="2018-10-05T18:29:59&#43;00:00" class="op-modified">2018-10-05T18:29:59+00:00</time>
                </header>
                <p>Do you want to discover the next exciting JavaScript features that you didn’t even know you needed? In this article, I will introduce one of these proposals that if accepted may change the way you write code the same way the  did.</p>

<p>However, here’s a small disclaimer: <strong>This feature is under development and discussion</strong>. The goal here is to add some hype around it and create awareness of the hard work that TC39 is doing to find consensus, fix all the syntax and semantics issues and have it shipped with the next releases of ECMAScript. If you have any concerns, comments or desire to express your support, please go to the , add a star to this feature to show your support, open an issue to voice your concerns and get involved.</p>

<p>But before, I want to ask a simple (but tricky) question:</p>

<p>What <em>is</em> <code>this</code>?</p>

<p>In ECMAScript, <code>this</code> has a different semantic than <code>this</code> in many other programming languages, where <code>this</code> often refers to the lexical scope. In general, this behaves differently in the global scope, within a function, in non-strict mode and strict mode. Let’s break this behavior down into small examples.</p>



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




<h3><code>this</code> In The Global Scope</h3>

<p>What is the value of <code>this</code> in this example?</p>

<pre><code class="language-javascript">console.info(this);</code></pre>

<p>At the global scope, <code>this</code> refers to the global object, like the <strong>window</strong> in the browser, <strong>self</strong> on web workers and the <strong>module.exports</strong> object in NodeJS.</p>

<h3><code>this</code> In The Function Scope</h3>

<p>At the function scope, <code>this</code> behaves depending on how the function is called, and this aspect makes it tricky to predict its value. We can understand it better by checking the following examples:</p>

<h4>What Is The Value Of <code>this</code> Here?</h4>

<pre><code class="language-javascript">function foo() {
  return this;
}

console.info(this);
</code></pre>

<p>Inside a function, <code>this</code> starts to have an interesting behavior since its value depends on how the function is called. In the example above, <code>this</code> still refers to the global scope, with one difference. In NodeJs, this will point to the global object instead of <code>module.exports</code>.</p>

<h4>Setting A Value Into <code>this</code>:</h4>

<pre><code class="language-javascript">function foo() {
  this.bar = 'baz';
  return this;
}

console.info(foo());
console.info(new foo());
</code></pre>

<p>Setting a value into <code>this</code> sets the value into the current context. The example above logs the global scope with the property <code>bar</code> with the value <code>baz</code> in the first <code>console.info</code>, but it logs only <code>{ bar: ‘baz’ }</code> in the second <code>console.info</code>. It happens because the <code>new</code> operator among other things bounds the value of <code>this</code> to the newly created object.</p>

<h3>This Keyword In The Strict Mode</h3>

<p>In strict mode, the <code>this</code> variable doesn’t carry the value of the context implicitly, this means if its context isn’t set, the value of this is default to <code>undefined</code> as shown in the following snippet.</p>

<pre><code class="language-javascript">function foo() {
  "use strict";
  return this;
}

console.info(foo()); //undefined
</code></pre>

<p>To set the context of <code>this</code> in strict mode you can set the function as member of an object, use <code>new</code> operator, <code>Function.prototype.call()</code>, <code>Function.prototype.apply()</code> or <code>Function.prototype.bind()</code> methods for example.</p>

<pre><code class="language-javascript">function foo() {
  "use strict";
  return this;
}

var a = { foo };

foo(); // undefined
a.foo(); // { foo: ƒunction }
new foo(); // Object foo {}
foo.call(this); // Window / Global Object
foo.apply(this); // Window / Global Object
foo.bind(this)(); // Window / Global Object
</code></pre>

<h3>Making <code>this</code> Variable Predictable</h3>

<p>At this point, you may realize that the value of <code>this</code> in ECMAScript is quite tricky to predict. To demonstrate the available techniques to make it predictable, I’d like to present the following example that mimics a common use case of <code>this</code>.</p>

<pre><code class="language-javascript">&lt;button id="button">🐱 🐾&lt;/button>
&lt;script>
  class MeowctComponent {
    constructor() {
      this.paw = document.getElementById('button');
    }

    meow() {
      console.info('🐱 on this: ', this.paw);
    }
  }

  const cat = new MeowctComponent();
  cat.paw.addEventListener('click', cat.meow);
&lt;/script>
</code></pre>

<p>In the example above, I created a <code>MeowctComponent</code>, which has only one property <code>paw</code> that points to the button element and one method called <code>meow</code> that should print the paw instance property into the console.</p>

<p>The tricky part is that the meow method is executed only when the button is clicked, and because of that, <code>this</code> has the button tag as context, and since the button tag does not have any paw property, it logs the <strong>undefined</strong> value into the console. Tricky, isn’t it?</p>

<p>To fix this specific behavior we can leverage on the <code>Function.prototype.bind()</code> method to explicitly bind this to the cat instance, like in the following example:</p>

<pre><code class="language-javascript">&lt;button id="button">Meow&lt;/button>
&lt;script>
  class MeowctComponent {
    constructor() {
      this.paw = document.getElementById('button');
    }

    meow() {
      console.info('🐱 on this: ', this.paw);
    }
  }

  const cat = new MeowctComponent();
  cat.paw.addEventListener('click', cat.meow.bind(cat));
&lt;/script>
</code></pre>

<p>The method <code>.bind()</code> returns a new permanently bound function to the first given parameter, which is the context. Now, because we bound the <code>cat.meow</code> method to the <code>cat</code> instance, <code>this.paw</code> inside the meow method correctly points to the <em>button element</em>.</p>

<p>As an alternative to the <code>Function.prototype.bind()</code> method, we can use the arrow function to achieve the same result. It keeps the value of the lexical <code>this</code> of the surrounding context and dispenses the need to bind the context explicitly, like in the next example:</p>

<pre><code class="language-javascript">&lt;button id="button">🐱 Meow&lt;/button>
&lt;script>
  class MeowctComponent {
    constructor() {
      this.paw = document.getElementById('button');
    }

    meow() {
      console.info('🐱 on this: ', this.paw);
    }
  }

  const cat = new MeowctComponent();
  cat.paw.addEventListener('click', () => cat.meow());
&lt;/script>
</code></pre>

<p>Although arrow functions solve the majority of use cases where we need to bind the lexical <code>this</code> explicitly, we still have two use cases for which the use of the explicit bind is needed.</p>

<h4>Calling A Known Function Using <code>this</code> To Provide Context:</h4>

<pre><code class="language-javascript">let hasOwnProp = Object.prototype.hasOwnProperty;
let obj = Object.create(null);

obj.hasOwnProperty('x') // Type Error...

hasOwnProp.call(obj, "x"); //false

obj.x = 100;

hasOwnProp.call(obj, "x"); // true
</code></pre>

<p>Let's suppose for any reason we have this <code>obj</code> object that doesn't extend <code>Object.prototype</code> but we need to check if <code>obj</code> has an <code>x</code> property by using the <code>hasOwnProperty</code> method from <code>Object.prototype</code>. To achieve that, we have to use the call method and explicitly pass <code>obj</code> as the first parameter to make it work as expected, which appears not to be so idiomatic.</p>

<div class="sponsors__wide-place"></div>




<h4>Extracting A Method</h4>

<p>The second case can be spotted when we need to extract a method from an object like in our <code>MeowctComponent</code> example:</p>

<pre><code class="language-javascript">&lt;button id="button">🐱 🐾&lt;/button>
&lt;script>
  class MeowctComponent {
    constructor() {
      this.paw = document.getElementById('button');
    }

    meow() {
      console.info('🐱 on this: ', this.paw);
    }
  }

  const cat = new MeowctComponent();
  cat.paw.addEventListener('click', cat.meow.bind(cat));
&lt;/script>
</code></pre>

<p>These use cases are the baseline problem that the bind operator tries to solve.</p>

<h3>The Bind Operator <code>::</code></h3>

<p>The <strong>Bind operator</strong> consists of an introduction of a new operator <code>::</code> (double colon), which acts as syntax sugar for the previous two use cases. It comes in two formats: <strong>binary</strong> and <strong>unary</strong>.</p>

<p>In its binary form, the bind operator creates a function with its left side is bound to <code>this</code> of the right side, like in the following example:</p>

<pre><code class="language-javascript">let hasOwnProp = Object.prototype.hasOwnProperty;
let obj = Object.create(null);

obj.hasOwnProperty('x') // Type Error...

obj::hasOwnProp("x"); //false

obj.x = 100;

obj::hasOwnProp("x"); // true
</code></pre>

<p>That looks more natural, doesn’t it?</p>

<p>In its unary form, the operator creates a function bound to the base of the provided reference as a value for <code>this</code> variable, like in the following example:</p>

<pre><code class="language-javascript">...
cat.paw.addEventListener('click', ::cat.meow);
// which desugars to
cat.paw.addEventListener('click', cat.meow.bind(cat));
...
</code></pre>

<p>What’s so cool about the bind operator is the fact that it opens up new opportunities for creating virtual methods, as in this example of lib for iterable.</p>

<pre><code class="language-javascript">import { map, takeWhile, forEach } from "iterlib";

getPlayers()
  ::map(x => x.character())
  ::takeWhile(x => x.strength > 100)
  ::forEach(x => console.log(x));
</code></pre>

<p>It’s super useful because the developer doesn’t need to download the whole lib to do small stuff, which reduces the amount of imported JavaScript. Besides, it makes those kinds of libs easier to extend.</p>

<h3>How To Develop Using Bind Operator</h3>

<p>To keep the example simple, let’s suppose we need to create a math module which the developer can chain the operations to form an math expression that, given a number as an entry it could make all calculations into a pipeline. The code to achieve this is simple and could be written as the following.</p>

<pre><code class="language-javascript">function plus(x) {
  return this + x;
}

function minus(x) {
  return this - x;
}

function times(x) {
  return this * x;
}

function div(x) {
  return this / x;
}
</code></pre>

<p>As you can spot in the example above, we expect to have the value as a context and we use this to make the calculation, so then using the bind operator, we could make an expression like the following:</p>

<pre><code class="language-javascript">1::plus(2)::times(4)::div(3)::minus(1); // returns 3
</code></pre>

<p>Which is equivalent to:</p>

<pre><code class="language-javascript">minus.call(div.call(times.call(plus.call(1, 2), 4), 3), 1);
</code></pre>

<p>The first snippet looks more idiomatic, isn’t?</p>

<p>Going a little further, we can use it to convert a temperature from Celsius to Fahrenheit, this can be accomplished by the following function expression:</p>

<pre><code class="language-javascript">const toFahrenheit = x => x::times(9)::div(5)::plus(32);
console.info(toFahrenheit(20)); // 68
</code></pre>

<p>So far, we demonstrate how create functions to interact with the values, but what about extending the object with virtual methods? We can do new stream compositions mixing built-in methods with custom ones. To demonstrate it, we can compose string methods with custom ones. First, let's check the module with the custom methods with its implementation.</p>

<pre><code class="language-javascript">function capitalize() {
  return this.replace(/(?:^|\s)\S/g, a => a.toUpperCase());
}

function doubleSay() {
  return `${this} ${this}`;
}

function exclamation() {
  return `${this}!`;
}
</code></pre>

<p>With this module in place we can do cool things like the following:</p>

<pre><code class="language-javascript">const { trim, padEnd } = String.prototype;

console.info(
  '   hello world   '
    ::trim()
    ::capitalize()
    ::doubleSay()
    ::exclamation()
    ::padEnd(30)
);

// "Hello World Hello World!      "
</code></pre>

<p>In the example above, you can spot that I extracted two methods from the <code>String.prototype</code>, <code>trim()</code> and <code>padEnd()</code>. Since these methods are extracted, I can use them to compose my stream of methods alongside with my virtual methods <code>capitalize()</code>, <code>doubleSay()</code> and <code>exclamation()</code>. This aspect is what makes bind operator so exciting and promising.</p>

<div class="sponsors__wide-place"></div>




<h3>Advantages And Disadvantages Of Bind Operator</h3>

<p>As you may realize at this point, there are some aspects that Bind Operator shines. Those are the following:</p>

<ul>
<li>It covers the only two missing use cases that explicit bind is necessary;</li>
<li>It makes easy to make <code>this</code> variable to be predictable;</li>
<li>It adds a new way to extend functionality by using virtual methods;</li>
<li>It helps to extend built-in objects without extending the prototype chain. Do you remember ?</li>
</ul>

<p>In the other side, to compose functions with bind operator you need to rely on this to be bound, that can lead to some issues like in this example:</p>

<pre><code class="language-javascript">const plus = (x) => this + x;

console.info(1::plus(1));
// "[object Window]1"
</code></pre>

<p>As it becomes clear in the example above, it’s not possible to compose arrow function with bind operator, since it’s not possible to bind <code>this</code> to an arrow function. Sometimes users don’t want to rely on <code>this</code> to be bound to compose their behavior through a function chain, which could be a problem if you only use bind operator to achieve this.</p>

<p>Another issue that is often said is the possible syntax overload that the bind operator can bring which can be a problem to onboard newcomers to the language. Realizing that a specific operator works in binary and unary form is tricky as well. One possible solution for this is to introduce the binary form to the language separately of the unary form. So once the binary form is integrated to the language, the committee can reassess if the unary form is still necessary. Meanwhile, users can get used to the binary form, and the syntax overload could potentially be mitigated.</p>

<h3>Conclusion</h3>

<p>Predict the value of <code>this</code> in JavaScript is trick. The language has some rules to explain how the context is assigned to this, but in the daily basis we want to make this value predictable. The <code>Function.prototype.bind()</code> method and arrow functions help us to make the value of <code>this</code> predictable. The <strong>bind operator</strong> comes to play to cover the two use cases that we still need to explicitly bind <code>this</code>.</p>

<p>The advent of bind operator opens an opportunity to create a new set of function composition via virtual methods, but it can add a syntax overload making difficult to onboard newcomers to the language.</p>

<p>The author of the bind operator is Kevin Smith, and . The TC39 is open to feedback. If you like this feature and think that it’s useful, please add a star in the repository, if you have an Idea to solve the issues presented here, if you have another way to shape the syntax or semantics of this features or if you spot another issue with it, please open an issue in the repo and share your thoughts/ideas with the committee.</p>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(dm, ra, yk, il)</span>
</div>


              </article>
            </body>
          </html>
---------------
<h1 id="#title_2" >3、每周分享第 25 期</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2018/10/weekly-issue-25.html](http://www.ruanyifeng.com/blog/2018/10/weekly-issue-25.html)
<p>这里记录过去一周，我看到的值得分享的东西，每周五发布。</p>

        <p><img src="https://www.wangbase.com/blogimg/asset/201810/bg2018100501.jpg" alt="" title="" /></p>

<p>上周我看到一个，9月23日是安卓手机的十周年纪念日。</p>

<p>十年前的2008年9月23日，HTC 发布了世界上第一台安卓手机 G1，3.2英寸屏幕，320x480分辨率，256MB内存， 1150mAh电池，并带有一个实体的全键盘。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201810/bg2018100502.jpg" alt="" title="" /></p>

<p>真不敢相信，智能手机真正开始普及，仅仅只有十年。</p>

<p>这十年，人类的生活完全改变。十年前，每个人都以与现在完全不同的方式生活着。2008年，没人用手机付款，大家在地铁读书看报，或者听着 iPod，想要给别人发消息，只能用短信。那些只凭一个 App 就成为独角兽的公司，一家都不存在。许多人还没有意识到，只需要做出一个受欢迎的 App，你就能创业，如果成功还能发财。</p>

<p>我敢预言，接下来的十年会有更大的变化，因为现在有了人工智能。2028年，我们的生活将是什么样？完全无法想象。我写过一本书叫做，预言大多数人在未来世界很难有出路，因为没法跟机器竞争。你要么会造机器，要么比机器强，否则怎么办呢。</p>

<p>这个《每周分享》专栏其实是那本书的延续，主题就是关注未来，关注那些将要流行的新技术和新趋势。有人说过，未来已经到来，只是还未流行。我们需要在未来变得流行之前，做好准备。假如2008年这个专栏就存在，那么我希望，安卓刚出来的时候，我们就知道这个东西会改变世界，带来无数机会，应该去学习如何开发 App。</p>

<h2>新闻</h2>

<p>1、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201810/bg2018100503.jpg" alt="" title="" /></p>

<p>亚马逊推出"零件搜索"（part search）。用户只要拍摄一个零件（比如螺丝），亚马逊就会给出提示，让用户选择相关参数，以便确定到底是哪一种零件。</p>

<p>2、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201810/bg2018100504.jpg" alt="" title="" /></p>

<p>据美国媒体报道，黑人姑娘 Lyndsey Scott 是"维多利亚的秘密"的内衣模特，同时也是程序员，懂得五种编程语言。还是 StackOverflow 的 ，为 code.org 录制过课程。</p>

<p>3、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201810/bg2018100505.jpg" alt="" title="" /></p>

<p>一个开发者使用 ARKit 2 为 iOS 手表增加了 AR 界面（现实增强界面）。当用户带着 AR 眼镜操作手表的时候，会看到辅助信息。比如打开"天气"的时候，就会看到上图。</p>

<p>这种 AR 界面的意义在于，未来的 UI 不必局限于设备之中，三维空间都可以是 UI。</p>

<p>4、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201810/bg2018100506.jpg" alt="" title="" /></p>

<p>加拿大在北方的冻土区，发现了一个冰河时期的狼的木乃伊。据检测，距今已有5万年。这头狼的保存情况好得惊人，皮毛、皮肤和肌肉组织都保存下来了，头部、尾部、爪子、皮肤和头发的细节都很好。</p>

<p>5、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201810/bg2018100507.jpg" alt="" title="" /></p>

<p>9月7日，美国最后一个小儿麻痹症患者 David Salamone 去世，享年28岁。他的特别之处在于，他不是自然感染，而是由于使用小儿麻痹症疫苗，而得了小儿麻痹症。</p>

<p>我们知道，疫苗的本质是灭活的病毒，即丧失活性的病毒。美国原来采用是口服小儿麻痹症疫苗，优点是服用方便，成本较低，但是有可能使得极少数的儿童（每年个位数）由于无力抵抗灭活的病毒而得病。David Salamone 就是这样得病了，由于这个案例，美国政府决定疫苗从口服改为注射，灭活病毒含量大大下降，从此再也没有发生过由于疫苗而得病的案例。他就成了美国最后一个小儿麻痹症患者。</p>

<p>6、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201810/bg2018100508.jpg" alt="" title="" /></p>

<p>畜牧业是人类蛋白质供给的主要来源之一，也是温室气体的主要来源之一。每一吨红肉的背后，都是大量的二氧化碳释放。</p>

<p>为了减少温室气体，科学家提出，我们也可以食用细菌产生的蛋白质。有些细菌可以食用糖或氨，随着它们的生长，可以被干燥，碾成粉末，用作蛋白质供人类或牲畜食用。计算后发现，如果大规模应用，到2050年，细菌每年可替代175至3.07亿吨的饲料，减少土地使用量6％，温室气体排放减少7％。 </p>

<p>7、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201810/bg2018100509.jpg" alt="" title="" /></p>

<p>索尼会在12月3日发售 PlayStation Classic 游戏主机，用来玩早期的 PS 游戏。主机大小跟一本书差不多，价格99美元。但是，多少人愿意买个新机器玩老游戏，让人怀疑，尤其是老游戏的分辨率最高只能到720P。</p>

<p>8、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201810/bg2018100510.jpg" alt="" title="" /></p>

<p>四十多万年前，北京猿人生活的周口店遗址，最近在山上修了一个保护棚，把猿人洞的露天洞口遮蔽起来。保护棚长77.5米，宽54.5米，高35.7米。</p>

<p>保护棚分为内外两层叶片，外层叶片不仅可以遮风挡雨，而且设有种植槽，植物可以生长在棚顶。内层叶片尽量与洞内岩壁融为一体。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201810/bg2018100511.jpg" alt="" title="" /></p>

<p>9、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201810/bg2018100512.jpg" alt="" title="" /></p>

<p>美国电视剧《海军罪案调查处.》（NCIS）最近播出的第十六季第一集，讲述一家公司使用熔岩灯作为随机数生成器，结果被插入木马，导致核反应堆被渗透。</p>

<p>这个装置其实不是虚构的，而是 Cloudflare 公司的。他们旧金山总部就有一个熔岩灯墙，对面是一个摄像头，每秒拍一一张照片。熔岩灯里面是一团蜡滴，会不断变换形状、颜色和位置，所以拍出来的照片都不一样，可以当作随机数。Cloudflare 公司已经发布了澄清声明，表示该发明并没有用于生产环境，因此不存在插入木马的可能。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201810/bg2018100513.jpg" alt="" title="" /></p>

<p>10、<strong>一句话新闻</strong></p>

<ul>
<li> 在 Windows 10 上面默认开启了 WebRender，使用 GPU 渲染网页，而不是传统的 CPU。这将大大改善网页的渲染性能，页面滚动和动画都会有更好的表现。 <br><br></li>
<li>都被互联网公司挖走了，美国高校的 AI 教育现在缺乏师资。<br><br></li>
<li> 称，该公司的目标是10年后人们不再拥有个人汽车，想要出门的时候，平台已经为你安排好了车。<br><br></li>
<li>在伦敦用电动卡车，取代普通卡车送货。</li>
</ul>

<p><img src="https://www.wangbase.com/blogimg/asset/201810/bg2018100514.jpg" alt="" title="" /></p>

<h2>教程</h2>

<p>1、 （英文）</p>

<p>PyPy 是用 Python 编写的 Python 解释器，这也是它名字的来源。该项目的创始人回顾了走过的十五年。</p>

<p>2、（英文）</p>

<p>Linux 内核与 Mac 内核虽然都源于 Unix，但是差别较大。Mac 内核继承 BSD Unix，有一些很老的代码，并且做了大量的定制。</p>

<p>3、（英文）</p>

<p>一些虚拟私有网络的相关知识。</p>

<p>4、（英文）</p>

<p>本文列举如何用 date-fns 或者原生方法，取代 moment.js。</p>

<p>5、（英文）</p>

<p>决定使用 Severless 架构之前，你应该读一下这篇文章，了解这种架构的一些问题。目前，最大的问题是，一旦用了它，就很难再摆脱对服务提供商的依赖。</p>

<p>6、（英文）</p>

<p>IPFS 是一个具有 web 接口的分布式数据库，一旦写入，你的内容就将永远存在，且无法修改。本文是一篇很不错的介绍文章， Cloudflare 在文中宣布开通 IPFS 网关服务。如果你有自己的 IPFS 节点，就可以让 Cloudflare 的 CDN 网络分发你的内容。</p>

<p>7、 （英文）</p>

<p>ActivePub 是一种分布式的通信协议，本文以 Mastodon 为例，介绍为什么它可以改变互联网。</p>

<p>8、（英文）</p>

<p>Github 正在测试语义搜索，匹配的依据不再是关键字，而是搜索的语义。比如，搜索"连接两个字符串"，就会跳出相关的代码。本文介绍实现细节。</p>

<p>9、（英文）</p>

<p>Facebook 在开发 React 的同时，还发明了一种新语言 Reason，它是 OCaml 语言的变种。Reason 和 React 的创始人是相同的，这篇文章解释了为什么 Reason 语言天生适合写 React 应用。</p>

<p>10、（英文）</p>

<p>简单的歌词通常有重复的内容。这篇文章使用压缩算法，比较现在的歌词与过去的歌词，看看哪个压缩得更小，内容更简单。</p>

<h2>资源</h2>

<p>1、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201810/bg2018100515.jpg" alt="" title="" /></p>

<p>免费电子书，如何通过数据进行预测。</p>

<p>2、</p>

<p>通过网页上的互动实例，教授 Python 语法。</p>

<p>3、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201810/bg2018100516.jpg" alt="" title="" /></p>

<p>一个 13KB 的网页小游戏。</p>

<p>4、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201810/bg2018100517.jpg" alt="" title="" /></p>

<p>各大公司的 UI 组件库的 Storybook 展示。Storybook 是一种 React 组件的展示工具。</p>

<p>5、</p>

<p>v8 引擎新的官方网站。为了体现 v8 高效快速的特点，这个网站故意做得很简单，能够快速加载。</p>

<h2>工具</h2>

<p>1、</p>

<p>有时候，系统通过鼠标判断用户是否走开了。这个工具可以让鼠标保持运行。</p>

<p>2、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201810/bg2018100518.jpg" alt="" title="" /></p>

<p>一个有点玩笑性质的项目。它可以将 Windows 画板程序制作的程序图片，编译执行。</p>

<p>3、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201810/bg2018100519.jpg" alt="" title="" /></p>

<p>将代码保存成图片的开源服务，可以用来上传到社交媒体。</p>

<p>4、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201810/bg2018100520.jpg" alt="" title="" /></p>

<p>Airdroid 是一个手机 App，可以将安卓手机与桌面电脑相连，用来传递文件。只需在手机上安装，然后桌面电脑访问一个局域网网址即可。</p>

<p>5、</p>

<p>一个代码协同的网站。你新建一个代码片段，然后把网址分享给其他人，就可以看到他们的实时编辑。</p>

<p>6、</p>

<p>一个基于 Python 的 Shell，最大特点就是跨平台。</p>

<p>7、</p>

<p>一个可以在网页运行的 BASIC 语言实现。</p>

<p>8、</p>

<p>perkeep 是一个开源工具，可以将你的文件同步储存到多个节点，保证不会丢失。它可以用作个人的储存系统，可以看作是亚马逊 S3 服务的本地实现。</p>

<p>9、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201810/bg2018100521.jpg" alt="" title="" /></p>

<p>搭建 Web 服务下载 Youtube 视频的工具。</p>

<h2>文摘</h2>

<p>1、</p>

<p>第二次世界大战以后，德国分裂成东德和西德，两边处于敌对状态。28岁的工程师 Bernd Boettge 想逃离东德，到西方去。</p>

<p>陆地边界都是封锁的，只有从海上偷渡。最初，他尝试游泳，但是很快体力耗尽，被抓住了。由于他是东德需要的工程师，所以没被关进监狱。</p>

<p>Bernd Boettge 不死心，决心第二次偷渡。为了能在水下呼吸，他让西德的阿姨寄来了一套潜水服。然后，自己改装了一台二冲程汽油发动机。这种发动机的体积很小，一般用于动力自动车，可以在水下作为动力装置，拉着他前进。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201810/bg2018100522.jpg" alt="" title="" /></p>

<p>发送机需要空气，因此他添加了一个橡胶的呼吸管，排气管则位于上方的圆柱形容器中。这个容器也起到浮子的作用。发动机带动螺旋桨，后面会拖着一个架子，他自己就挂在这个架子上。整个装置重约22磅（大约10公斤），足够轻，可以手里拿着穿过海滩，总成本大约50美元。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201810/bg2018100523.jpg" alt="" title="" /></p>

<p>他没办法测试，只能寄希望第一次下水就成功。如果再被抓住，肯定就完了。</p>

<p>1968年9月8日，在黑暗的掩护下，他在格拉尔 - 米里茨（Graal-Müritz）的海面下水，慢慢穿过探照灯和巡逻船。在海里前进了25公里之后，成功到达了丹麦。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201810/bg2018100524.jpg" alt="" title="" /></p>

<p>上图为他到达丹麦时的照片。</p>

<p>后来，他为这个装置申请了专利，并由其他公司投入了生产：大海里面拖动潜水员的汽油动力拖动器。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201810/bg2018100525.jpg" alt="" title="" /></p>

<p>1974年，Bernd Boettge 死于西班牙的一次潜水事故。至今不知道，这是真的事故，还是东德策划的暗杀。</p>

<p>2、</p>

<p>2018年9月5日，美国国会召开听证会。推特 CEO 和 Facebook 总裁都出席了，但是45岁的谷歌创始人拉里佩奇却没去。他的座位空着。Alphabet （谷歌的母公司）在一份声明中说，谷歌全球事务负责人参加了听证会，而"拉里佩奇正专注于其他项目和长期技术问题。"</p>

<p>问题是，拉里佩奇已经将近5年没有亮相，没有任何新闻报道，他消失了。2013年以来，他没有参与任何产品发布会或对外的电话会议。2015年以来，他没有接受过任何新闻采访。公司的日常管理交给了 Sundar Pichai，外界不知道他在干嘛。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201810/bg2018100526.jpg" alt="" title="" /></p>

<p>2011年，他接替埃里克施密特，担任谷歌的 CEO。他每周工作80小时，大量阅读商业管理书籍，很快他就对管理和运营厌倦了，想把更多时间用于研发。一个前谷歌高管说，一次开会时，他对正在汇报的员工说"你做的事情很无聊"。另一次，有人请示他解决公司内部两个团队之间的矛盾，他回答说"你们不能自己解决吗？"</p>

<p>2015年谷歌重组，Sundar Pichai 成为谷歌的 CEO，佩奇担任母公司 Alphabet 的 CEO。从此，他更专注于那些疯狂的未来项目，比如自动驾驶飞行器、机器人、谷歌光纤等等，不再出现在公众场合，甚至谷歌内部员工也极少看见他。</p>

<p>拉里佩奇的隐居，让人感觉他像一个身体虚弱和衰老的名人，但实际上他比 Sundar Pichai 年轻。他的最后一次公开露面，是2014年的一次，谈论谷歌的未来。此后，他就不再出现了，也不知道未来是否还会出现。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201810/bg2018100527.jpg" alt="" title="" /></p>

<h2>本周图片</h2>

<p>1、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201810/bg2018100528.jpg" alt="" title="" /></p>

<p>很多手机应用，就是上面这张漫画，说是整个社会的写照也可以：以安全名义把用户信息都留住，同时把用户隐私剥个精光。（via 推特）</p>

<p>2、</p>

<p>巧克力是全世界最流行的食品之一，它的主要原料是可可豆。可可豆长在一种红色的豆荚里面。每个豆荚包裹额20～25个可可豆。好几个非洲国家的经济，就依赖这种树。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201810/bg2018100529.jpg" alt="" title="" /></p>

<p><img src="https://www.wangbase.com/blogimg/asset/201810/bg2018100530.jpg" alt="" title="" /></p>

<p>3、</p>

<p>日本名古屋东山动物园有一只喜欢歪着头、吐舌头的小河马。现在成了动物园推特账户 的明星。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201810/bg2018100531.jpg" alt="" title="" /></p>

<p><img src="https://www.wangbase.com/blogimg/asset/201810/bg2018100532.jpg" alt="" title="" /></p>

<h2>新奇</h2>

<p>1、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201810/bg2018100533.jpg" alt="" title="" /></p>

<p><img src="https://www.wangbase.com/blogimg/asset/201810/bg2018100534.jpg" alt="" title="" /></p>

<p>日本开发出了自动旋转的魔方。里面安装了电机和芯片，会自动复原。</p>

<h2>本周金句</h2>

<p>1、</p>

<p>我在想这个火箭有两万个零件，每一个都是由最低价的投标者制造的。</p>

<p>-- ，第一个进入地球轨道的美国宇航员。有人问，坐在火箭里面等待发射时，他在想什么？他说了上面的回答。</p>

<p>2、</p>

<p>我已经投入了2,600多个小时，编写了62,176行代码（主要是C ++）。该游戏的收入为27.92美元，每小时收入约0.01美元。</p>

<p>-- 。他用了三年，独自一人开发游戏，放到 Steam 平台销售后，只有四个人购买。现在，他不得不考虑放弃这个游戏，这意味这三年时间都白费了。</p>

<h2>欢迎订阅</h2>

<p>这个专栏每周五发布，同步更新在我的。</p>

<p>微信搜索"<strong>阮一峰的网络日志</strong>"或者扫描二维码，即可订阅。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2018/bg2018042311.jpg" alt="" title="" /></p>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2018-10-05T14:15:10+08:00">2018年10月 5日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>文集：</li>
<li>社交媒体：</li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------
<h1 id="#title_3" >4、SmashingConf Toronto Videos</h1>
The Smashing Editorial
[https://www.smashingmagazine.com/2018/10/smashingconf-toronto-videos/](https://www.smashingmagazine.com/2018/10/smashingconf-toronto-videos/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/10/smashingconf-toronto-videos/" />
              <title>SmashingConf Toronto Videos</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>SmashingConf Toronto Videos</h1>
                  
                    
                    <address>The Smashing Editorial</address>
                  
                  <time datetime="2018-10-05T18:00:35&#43;02:00" class="op-published">2018-10-05T18:00:35+02:00</time>
                  <time datetime="2018-10-05T18:29:59&#43;00:00" class="op-modified">2018-10-05T18:29:59+00:00</time>
                </header>
                

<p>This year, many of your favorite speakers were featured at our conference in Toronto, however, things were quite different this time. The speakers had been asked to present without slides. Yep, and it was brilliant!</p>

<p>In this pairing of videos from  anytime.</p>

<h3 id="how-i-think-when-i-think-visually-eva-lotta-lamm">How I Think When I Think Visually: Eva-Lotta Lamm</h3>

<p>Sketching is something which lends itself perfectly to the no-slides format. In this talk, Eva-Lotta demonstrates her process for visual thinking. A method which helps her order her thoughts, create sketchnotes, and visualize processes such as user journeys.</p>

<figure class="video-container"><iframe data-src="https://player.vimeo.com/video/292461456" width="600" height="480" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe></figure>

<h3 id="svg-and-vue-together-from-start-to-finish-sarah-drasner">SVG And Vue Together From Start To Finish: Sarah Drasner</h3>

<p>In this talk, Sarah starts with only an Illustrator document and by the end, makes it move! In this talk, which has an included GitHub repository to help you follow along, Sarah uses animation and Vue.js to create the final piece.</p>

<figure class="video-container"><iframe data-src="https://player.vimeo.com/video/292473138" width="600" height="480" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe></figure>

<p>Enjoyed watching these talks? There are many  &mdash; see you there? ;-)</p>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(ra, il)</span>
</div>





              </article>
            </body>
          </html>
---------------
<h1 id="#title_4" >5、文章： 为什么在以太坊上构建项目注定会失败</h1>
Cameron Wall
[http://www.infoq.com/cn/articles/why-building-projects-on-ethereum-are-destent-fail?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/why-building-projects-on-ethereum-are-destent-fail?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/why-building-projects-on-ethereum-are-destent-fail/zh/smallimage/DNUN-logo-small-1537696087142.jpg"/><p>解释几乎所有由以太坊区块链支持的项目都会失败的原因。</p> <i>By Cameron Wall</i> <i> Translated by 姚佳灵</i>
---------------
<h1 id="#title_5" >6、CQRS和事件源框架Axon的基本概念和未来</h1>
Jan Stenberg
[http://www.infoq.com/cn/news/2018/10/concepts-future-axon-cqrs?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/10/concepts-future-axon-cqrs?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>在最近的阿姆斯特丹事件驱动微服务大会上，Allard Buijze在演讲中介绍了Axon的基本概念、历史和未来。该框架面向以DDD、事件源和CQRS为基础的系统。Axon Framework的应用正在迅速增加，最近达到了100万的下载量。</p> <i>By Jan Stenberg</i> <i> Translated by 谢丽</i>
---------------