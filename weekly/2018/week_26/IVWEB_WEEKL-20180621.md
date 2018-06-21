## 文章索引
1、 <a href="#1为什么要从众多的前端框架中选择react" >为什么要从众多的前端框架中选择React?</a><br/>
2、 <a href="#2fb正在大规模重构react-native预计今年发布" >FB正在大规模重构React Native，预计今年发布</a><br/>
3、 <a href="#3oracle弃用nashorn-javascript引擎" >Oracle弃用Nashorn JavaScript引擎</a><br/>
4、 <a href="#4dont-use-the-placeholder-attribute" >Don’t Use The Placeholder Attribute</a><br/>
5、 <a href="#5文章-apache-kylin在4399大数据平台的应用" >文章： Apache Kylin在4399大数据平台的应用</a><br/>
6、 <a href="#6文章-你的产品路线图是否仍然贴合用户的需求" >文章： 你的产品路线图是否仍然贴合用户的需求？</a><br/>
7、 <a href="#7aws发布elastic-container-service-for-kuberneteseks" >AWS发布Elastic Container Service for Kubernetes（EKS）</a><br/>
8、 <a href="#8通过devops考古学了解生产环境" >通过DevOps考古学了解生产环境</a><br/><h1 id="#title_0" >1、为什么要从众多的前端框架中选择React?</h1>
王沛
[http://www.infoq.com/cn/news/2018/06/why-choose-React?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/06/why-choose-React?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>React 从入门到精通，帮你快速掌握当下最热门的前端框架。</p> <i>By 王沛</i>
---------------
<h1 id="#title_1" >2、FB正在大规模重构React Native，预计今年发布</h1>
Sophie Alpert
[http://www.infoq.com/cn/news/2018/06/facebook-refactor-react-native?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/06/facebook-refactor-react-native?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>几日前，Facebook刚刚发布了React Native 0.56，随后，React工程经理Sophie Alpert在其官方博客上宣布他们将要重构React Native，使其更轻量，更适应JavaScript生态圈的发展。</p> <i>By Sophie Alpert</i> <i> Translated by 覃云</i>
---------------
<h1 id="#title_2" >3、Oracle弃用Nashorn JavaScript引擎</h1>
Kesha Williams
[http://www.infoq.com/cn/news/2018/06/deprecate-nashorn?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/06/deprecate-nashorn?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Oracle通过JDK增强提案（JEP）355宣布弃用Nashorn JavaScript引擎，最终将从未来所有的JDK中删除。ECMAScript的语言结构变化太快，Oracle发现，维护Nashorn JavaScript引擎变得非常困难。</p> <i>By Kesha Williams</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_3" >4、Don’t Use The Placeholder Attribute</h1>
Eric Bailey
[https://www.smashingmagazine.com/2018/06/placeholder-attribute/](https://www.smashingmagazine.com/2018/06/placeholder-attribute/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/06/placeholder-attribute/" />
              <title>Don’t Use The Placeholder Attribute</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>Don’t Use The Placeholder Attribute</h1>
                  
                    
                    <address>Eric Bailey</address>
                  
                  <time datetime="2018-06-20T13:45:26&#43;02:00" class="op-published">2018-06-20T13:45:26+02:00</time>
                  <time datetime="2018-06-20T20:43:46&#43;00:00" class="op-modified">2018-06-20T20:43:46+00:00</time>
                </header>
                

<p>Introduced as part of the HTML5 specification,  “represents a short hint (a word or short phrase) intended to aid the user with data entry when the control has no value. A hint could be a sample value or a brief description of the expected format.”</p>

<p>This seemingly straightforward attribute contains a surprising amount of issues that prevent it from delivering on what it promises. Hopefully, I can convince you to stop using it.</p>

<h3 id="technically-correct">Technically Correct</h3>

<p>Inputs are the gates through which nearly all e-commerce has to pass. Regardless of your feelings on , unusable inputs leave money on the table.</p>

<p>The presence of a placeholder attribute won’t be flagged by automated accessibility checking software. However, this doesn’t necessarily mean it’s usable. Ultimately, , so it is important to think about your interface in terms beyond running through a checklist.</p>

<p>Call it remediation, inclusive design, universal access, whatever. The spirit of all these philosophies boils down to making things that people—all people—can use. Viewed through this lens, <code>placeholder</code> simply doesn’t hold up.</p>

<h3 id="the-problems">The Problems</h3>

<h4 id="translation">Translation</h4>

<p>Browsers with auto-translation features such as Chrome skip over attributes when a request to translate the current page is initiated. For many attributes, this is desired behavior, as .</p>

<p>One of the attributes skipped over by browsers is <code>placeholder</code>. Because of this, <code>placeholder</code> content won’t be translated and will remain as the originally authored language.</p>



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




<p>If a person is requesting a page to be translated, the expectation is that all visible page content will be updated. Placeholders are frequently used to provide important input formatting instructions or are used in place of a more appropriate <code>label</code> element (more on that in a bit). If this content is not updated along with the rest of the translated page, there is a high possibility that a person unfamiliar with the language will not be able to successfully understand and operate the input.</p>

<p>This should be reason enough to not use the attribute.</p>

<p>While we’re on the subject of translation, it’s also worth pointing out that location isn’t the same as language preference. Many people set their devices to use a language that isn’t the official language of the country reported by their browser’s IP address (to say nothing of —your neighbors will thank you!</p>

<h4 id="interoperability">Interoperability</h4>

<p>Interoperability is the practice of making different systems exchange and understand information. It is a foundational part of both the Internet and assistive technology.</p>

<p>Semantically describing your content makes it interoperable. An interoperable <code>input</code> is created by programmatically associating a <code>label</code> element with it. Labels describe the purpose of an input field, providing the person filling out the form with a prompt that they can take action on. One way to associate a <code>label</code> with an <code>input</code>, is to use  with a value that matches the input’s <code>id</code>.</p>

<p>Without this <code>for</code>/<code>id</code> pairing, assistive technology will be unable to determine what the input is for. The programmatic association provides  can utilize. Without it, people who rely on this specialized software will not be able to read or operate inputs.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/06626f97-abe7-4ed1-a215-df14a3aaefea/computed-properties-landscape-new.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/06626f97-abe7-4ed1-a215-df14a3aaefea/computed-properties-landscape-new.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/06626f97-abe7-4ed1-a215-df14a3aaefea/computed-properties-landscape-new.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/06626f97-abe7-4ed1-a215-df14a3aaefea/computed-properties-landscape-new.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/06626f97-abe7-4ed1-a215-df14a3aaefea/computed-properties-landscape-new.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/06626f97-abe7-4ed1-a215-df14a3aaefea/computed-properties-landscape-new.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/06626f97-abe7-4ed1-a215-df14a3aaefea/computed-properties-landscape-new.png"
			sizes="100vw"
			alt="A diagram demonstrating how code gets converted into a rendered input, and how the code’s computed properties get read by assistive technology. The code is a text input with a label that reads Your Name. The listed computed properties are the accessible name, which is Your Name, and a role of textbox."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			How semantic markup is used for both visual presentation and accessible content. ()
		</figcaption>
	
</figure>


<p>The reason I am mentioning this is that <code>placeholder</code> is oftentimes used in place of a <code>label</code> element. Although I’m personally baffled by the practice, it seems to have gained traction in the design community. My best guess for its popularity is the geometrically precise grid effect it creates when placed next to other label-less input fields acts like designer catnip.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bbba30fe-95e5-43c1-b1ef-be5037a0eae2/facebook-signup.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bbba30fe-95e5-43c1-b1ef-be5037a0eae2/facebook-signup.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bbba30fe-95e5-43c1-b1ef-be5037a0eae2/facebook-signup.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bbba30fe-95e5-43c1-b1ef-be5037a0eae2/facebook-signup.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bbba30fe-95e5-43c1-b1ef-be5037a0eae2/facebook-signup.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bbba30fe-95e5-43c1-b1ef-be5037a0eae2/facebook-signup.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bbba30fe-95e5-43c1-b1ef-be5037a0eae2/facebook-signup.png"
			sizes="100vw"
			alt="Facebook’s signup form. A heading reads, “Sign Up. It’s free and always will be.” Placeholders are being used as labels, asking for your first name, last name, mobile number or email, and to create a new password for your account Screenshot."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			An example of input grid fetishization from a certain infamous blue website. ()
		</figcaption>
	
</figure>


<p>The , a close cousin to this phenomenon, oftentimes utilizes the placeholder attribute in place of a <code>label</code>, as well.</p>

<p>A neat thing worth pointing out is that if a label is programmatically associated with an input, clicking or tapping on the label text will place focus on the input. This little trick provides an extra area for interacting with the input, which can be beneficial to . Placeholders acting as labels, as well as floating labels, cannot do that.</p>

<h4 id="cognition">Cognition</h4>

<p> lists nearly 15 million people who report having cognitive difficulty &mdash; and that’s only counting individuals who choose to self-report. Extrapolating from this, we can assume that cognitive accessibility concerns affect a significant amount of the world’s population.</p>

<p>Self-reporting is worth calling out, in that a person may not know, or feel comfortable sharing that they have a cognitive accessibility condition. Unfortunately, there are still a lot of  attached to disclosing this kind of information, as it oftentimes affects things like job and housing prospects.</p>

<p>Cognition can be inhibited situationally, meaning it can very well happen to you. It can be affected by things like multitasking, sleep deprivation, stress, substance abuse, and depression. I might be a bit jaded here, but that sounds a lot like conditions you’ll find at most office jobs.</p>

<h5 id="recall">Recall</h5>

<p>The umbrella of cognitive concerns covers conditions such as short-term memory loss, traumatic brain injury, and Attention Deficit Hyperactivity Disorder. They can all affect a person’s ability to recall information.</p>

<p>When a person enters information into an input, its placeholder content will disappear. The only way to restore it is to remove the information entered. This creates an experience where guiding language is removed as soon as the person attempting to fill out the input interacts with it. Not great!</p>

<figure>)</figcaption></figure>

<p>When your ability to recall information is inhibited, it makes following these disappearing rules annoying. For inputs with complicated requirements to satisfy—say creating a new password—it transcends annoyance and becomes a difficult barrier to overcome.</p>

<figure>)</figcaption></figure>

<p>While more technologically-sophisticated people may have learned clever tricks such as cutting entered information, reviewing the placeholder content to refresh their memory, then re-pasting it back in to edit, people who are less technologically literate may not understand why the help content is disappearing or how to bring it back.</p>

<h4 id="digital-literacy">Digital Literacy</h4>

<p>Considering that more and more of the world’s population is coming online, the onus falls on us as responsible designers and developers to make these people feel welcomed. Your little corner of the Internet (or intranet!) could very well be one of their first experiences online &mdash; assuming that the end user “will just know” is simple arrogance.</p>


  <div id="sponsors-article" data-impression="true" class="c-promo-box c-promo-box--ad sponsors hidden" data-audience="non-subscriber" data-remove="true"></div>



<p>For US-based readers, a gentle reminder that new may not mean foreign. .</p>

<p>For someone who has never encountered it before, placeholder text may look like entered content, causing them to skip over the input. If it’s a required field, form submission will create a frustrating experience where they may not understand what the error is, or how to fix it. If it’s not a required field, your form still runs the unnecessary risk of failing to collect potentially valuable secondary information.</p>

<h4 id="utility">Utility</h4>

<p>Placeholder help content is limited to just a string of static text, and that may not always be sufficient to communicate the message. It may need to have additional styling applied to it, or contain descriptive markup, attributes, images, and iconography.</p>

<p>This is especially handy in mature design systems. The additional styling options created by moving the string of text out of the input element means it can take advantage of the system’s , and all the benefits that come with using them.</p>

<p>Placeholder text’s length is also limited to the width of the input it is contained in. In our responsive, mobile-first world, there stands a very good chance that important information could be truncated:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6b964bd2-5cb9-487b-9f91-a05208665b44/truncation.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6b964bd2-5cb9-487b-9f91-a05208665b44/truncation.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6b964bd2-5cb9-487b-9f91-a05208665b44/truncation.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6b964bd2-5cb9-487b-9f91-a05208665b44/truncation.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6b964bd2-5cb9-487b-9f91-a05208665b44/truncation.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6b964bd2-5cb9-487b-9f91-a05208665b44/truncation.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6b964bd2-5cb9-487b-9f91-a05208665b44/truncation.png"
			sizes="100vw"
			alt="An input called Your YAMA Code, with a truncated placeholder that reads, You can find this code on the ba-"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			I guess I’ll never know where that code is. ()
		</figcaption>
	
</figure>


<h4 id="vision">Vision</h4>

<h5 id="color-contrast">Color Contrast</h5>

<p>The  for placeholder content use a light gray color to visually communicate that it is a suggestion. Many custom input designs follow this convention by taking the color of input content and lightening it.</p>

<p>Unfortunately, this technique is likely to run afoul of color contrast issues. Color contrast is a ratio determined by comparing the luminosity of the text and background color values; in this case, it’s the color of the placeholder text over the input’s background.</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="dKbbEV"
   data-user="ericwbailey"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<p>If the placeholder content has a contrast ratio that is too low to be perceived, it means that information critical to filling out a form successfully may not be able to be seen by people experiencing low vision conditions. For most common input font sizing, .</p>

<p>Like all accessibility concerns, low vision conditions can be permanent or temporary, biological or environmental, or a combination. Biological disabilities include conditions like farsightedness, color blindness, dilated pupils, and cataracts. Environmental conditions include circumstances such as the glare of the mid-day sun, a battery-saving low brightness setting, privacy screens, grease and makeup left on your screen by your last phone call, and so on.</p>

<p>This ratio isn’t some personal aesthetic preference that I’m trying to force onto others arbitrarily. It’s part of a set of  that help ensure that the largest possible swath of people can operate digital technology, regardless of their ability or circumstance. Consciously ignoring these rules is to be complicit in practicing exclusion.</p>

<p>And here’s the rub: In trying to make placeholder attributes inclusive, the updated higher contrast placeholder content color may become dark enough to be interpreted as entered input, even by more digitally literate people. This swings the issue back into cognitive concerns land.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f4b57a44-567d-4c47-8c56-aa2b3cf6509d/gofundme-password-reset.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f4b57a44-567d-4c47-8c56-aa2b3cf6509d/gofundme-password-reset.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f4b57a44-567d-4c47-8c56-aa2b3cf6509d/gofundme-password-reset.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f4b57a44-567d-4c47-8c56-aa2b3cf6509d/gofundme-password-reset.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f4b57a44-567d-4c47-8c56-aa2b3cf6509d/gofundme-password-reset.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f4b57a44-567d-4c47-8c56-aa2b3cf6509d/gofundme-password-reset.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f4b57a44-567d-4c47-8c56-aa2b3cf6509d/gofundme-password-reset.png"
			sizes="100vw"
			alt="The email address field on GoFundMe’s password reset page has a placeholder that reads email@address.com and is set to a dark black color that makes it look like entered input. Screenshot."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The placeholder text color on GoFundMe’s password reset page makes it appear like entered input. Additionally, the checkmark icon on the Request New Password button makes it seem like the request has already been processed. ()
		</figcaption>
	
</figure>


<h5 id="high-contrast-mode">High Contrast Mode</h5>

<p>The Windows operating system contains a feature called . When activated, it assigns new colors to interface elements from a special high contrast palette that uses a limited number of color options. Here’s an example of what it may look like:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4047600d-d20b-4555-ba34-d2c474cb24c8/high-contrast-mode.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4047600d-d20b-4555-ba34-d2c474cb24c8/high-contrast-mode.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4047600d-d20b-4555-ba34-d2c474cb24c8/high-contrast-mode.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4047600d-d20b-4555-ba34-d2c474cb24c8/high-contrast-mode.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4047600d-d20b-4555-ba34-d2c474cb24c8/high-contrast-mode.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4047600d-d20b-4555-ba34-d2c474cb24c8/high-contrast-mode.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4047600d-d20b-4555-ba34-d2c474cb24c8/high-contrast-mode.png"
			sizes="100vw"
			alt="An input field with a label that reads “Donation amount” and a placeholder that reads “$25.00.” The screenshot is taken with Windows High Contrast mode active, so the placeholder element looks like entered text content. Screenshot."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Windows 10 set to use the High Contrast Mode 1 theme running Internet Explorer 11. ()
		</figcaption>
	
</figure>


<p>In High Contrast Mode, <code>placeholder</code> content is assigned one of those high contrast colors, making it look like pre-filled information. As discussed earlier, this could prevent people from understanding that the input may need information entered into it.</p>

<p>You may be wondering if it’s possible to update the styling in High Contrast Mode to make a placeholder more understandable. While it is possible to target High Contrast Mode in a media query, I implore you not to do so. Front-end developer :</p>

<blockquote>“High contrast mode is not about design anymore but strict usability. You should aim for highest readability, not color aesthetics.”</blockquote>

<p>The people that rely on High Contrast Mode use it because of how  it is. Unduly altering how it presents content may interfere with the only way they can reliably use a computer. In the case of lightening the color of placeholder content to make it appear like its non-High Contrast Mode treatment, you run a very real risk of making it impossible for them to perceive.</p>

<h3 id="a-solution">A Solution</h3>

<p>To recap, the placeholder attribute:</p>

<ul>
<li>Can’t be automatically translated;</li>
<li>Is oftentimes used in place of a label, locking out assistive technology;</li>
<li>Can hide important information when content is entered;</li>
<li>Can be too light-colored to be legible;</li>
<li>Has limited styling options;</li>
<li>May look like pre-filled information and be skipped over.</li>
</ul>

<p>Eesh. That’s not great. So what can we do about it?</p>

<h4 id="design">Design</h4>

<p>Move the placeholder content above the input, but below the label:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e08cd2c9-4f50-4fb9-b480-d0f843733beb/solution.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e08cd2c9-4f50-4fb9-b480-d0f843733beb/solution.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e08cd2c9-4f50-4fb9-b480-d0f843733beb/solution.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e08cd2c9-4f50-4fb9-b480-d0f843733beb/solution.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e08cd2c9-4f50-4fb9-b480-d0f843733beb/solution.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e08cd2c9-4f50-4fb9-b480-d0f843733beb/solution.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e08cd2c9-4f50-4fb9-b480-d0f843733beb/solution.png"
			sizes="100vw"
			alt="An input with a label that reads, Your employee ID number, and help content below the label that reads, Can be found on your employee intranet profile. Example: a1234567-89. The example ID has been styled using a monospaced font."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>This approach:</p>

<ul>
<li>Communicates a visual and structural hierarchy:

<ul>
<li>What this input is for,</li>
<li>Things you need to know to use the input successfully, and</li>
<li>the input itself.</li>
</ul></li>
<li>Can be translated.</li>
<li>Won’t look like pre-filled information.</li>
<li>Can be seen in low vision circumstances.</li>
<li>Won’t disappear when content is entered into the input.</li>
<li>Can include semantic markup and be styled via CSS.</li>
</ul>

<p>Additionally, the help content will be kept in view when the input is activated on a device with a software keyboard. If placed below the input, the content may be obscured when an on-screen keyboard appears at the bottom of the device viewport:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cf3c2b8a-8b00-475e-b365-11961a2e99d6/ios-obscured-input-1200px.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cf3c2b8a-8b00-475e-b365-11961a2e99d6/ios-obscured-input-1200px.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cf3c2b8a-8b00-475e-b365-11961a2e99d6/ios-obscured-input-1200px.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cf3c2b8a-8b00-475e-b365-11961a2e99d6/ios-obscured-input-1200px.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cf3c2b8a-8b00-475e-b365-11961a2e99d6/ios-obscured-input-1200px.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cf3c2b8a-8b00-475e-b365-11961a2e99d6/ios-obscured-input-1200px.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cf3c2b8a-8b00-475e-b365-11961a2e99d6/ios-obscured-input-1200px.png"
			sizes="70vw"
			alt="iOS’ on-screen keyboard is obscuring information about password requirements on a “Set a password” input. Screenshot."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Content hidden by an on-screen keyboard. 3rd party keyboards with larger heights may have a greater risk of blocking important content. ()
		</figcaption>
	
</figure>


<h4 id="development">Development</h4>

<p>Here’s how to translate our designed example to code:</p>

<pre><code class="language-html">&lt;div class="input-wrapper">
  &lt;label for="employee-id">
    Your employee ID number
  &lt;/label>
  &lt;p
    id="employee-id-hint"
    class="input-hint">
    Can be found on your employee intranet profile. Example: &lt;samp>a1234567-89&lt;/samp>.
  &lt;/p>
  &lt;input
    id="employee-id"
    aria-describedby="employee-id-hint"
    name="id-number"
    type="text" />
&lt;/div>
</code></pre>

<p>This isn’t too much of a departure from a traditional accessible <code>for</code>/<code>id</code> attribute pairing: The <code>label</code> element is programmatically associated with the <code>input</code> via its <code>id</code> declaration of “employee-id”. The <code>p</code> element placed between the <code>label</code>  and <code>input</code> elements acts as a replacement for a <code>placeholder</code> attribute.</p>

<p>“So,” you may be wondering. “Why don’t we just put all that placeholder replacement content in the <code>label</code> element? It seems like it’d be a lot less work!” The answer is that developer convenience shouldn’t take priority over user experience.</p>

<p>By using  with what a person browsing without a screen reader would experience. <code>aria-describedby</code> ensures that the <code>p</code> content will be described last, after the <code>label</code>’s content and the kind of input it is associated with.</p>

<p>In other words, it’s what content the input is asking for, what type of input it is, then additional help if you need it &mdash; exactly what someone would experience if they look at form input.</p>

<p>User experience encompasses all users, including those who navigate with the aid of screen readers. The help content is self-contained and easy to navigate to and from, should the person using a screen reader need to re-reference it. As it is a self-contained node, it can also be silenced (typically with the Control key) without risking muting other important information.</p>

<p>Including the help content as part of the <code>label</code> makes it unnecessarily verbose. <code>label</code>s should be .</p>

<h4 id="example">Example</h4>

<p>Here is the solution implemented in live code:</p>

<p><p data-height="265" data-theme-id="0" data-slug-hash="ea10dcdde2520c561bd588a2e1f50ce8" data-default-tab="html,result" data-user="ericwbailey" data-embed-version="2" data-pen-title="Don't use the placeholder attribute" data-editable="true" class="codepen">See the Pen .</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script></p>

<p>And here’s a video demonstrating how popular screen readers handle it:</p>

<figure class="video-container"><iframe data-src="https://www.youtube.com/embed/MHGJna9GcTM?rel=0" width="600" height="480" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe></figure>

<h3 id="a-better-solution">A Better Solution</h3>

<blockquote>“The less an interface requires of its users, the more accessible it is.”<br /><br />&mdash; </blockquote>

<p>A final thought: Do you even need that additional placeholder information?</p>

<p>Good front-end solutions take advantage of  to prevent offloading the extra work onto the person who simply just wants to use your site or app with as little complication as possible.</p>

<p>Good copywriting creates labels that clearly and succinctly describe the input’s purpose. Do a good enough job here and the label cuts through the ambiguity, especially if you .</p>

<p>Good user experience is all about creating intelligent flows that preempt people’s needs, wants, and desires by capitalizing on existing information to remove as many unnecessary questions as possible.</p>

<p>Accommodating the people who use your website or web app means taking a critical eye at what you take for granted when you browse the Internet. By not making assumptions about other people’s circumstances &mdash; including the technology they use &mdash; you can do your part to help prevent exclusion.</p>

<p>Take some time to review your design and code and see what doesn’t stand up to scrutiny &mdash; checking to see if you use the placeholder attribute might be a good place to start.</p>

<p><em>Standing on the shoulders of giants. Thanks to  for their writing on the subject.</em></p>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(rb, ra, yk, il)</span>
</div>


              </article>
            </body>
          </html>
---------------
<h1 id="#title_4" >5、文章： Apache Kylin在4399大数据平台的应用</h1>
林兴财
[http://www.infoq.com/cn/articles/apache-kylin-at-4399-big-data-platform?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/apache-kylin-at-4399-big-data-platform?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/apache-kylin-at-4399-big-data-platform/zh/smallimage/GettyImages-489084228-1529509621151.jpg"/><p>本文介绍了 4399 大数据团队在公司大数据平台上应用 Kylin 的实践经验，并基于应用中遇到的问题给出了对应的优化建议。</p> <i>By 林兴财</i>
---------------
<h1 id="#title_5" >6、文章： 你的产品路线图是否仍然贴合用户的需求？</h1>
Justin Zalewski
[http://www.infoq.com/cn/articles/product-roadmap-meeting-needs?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/product-roadmap-meeting-needs?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/product-roadmap-meeting-needs/zh/smallimage/map-1528700845386-1529510646600.jpeg"/><p>一款产品需要有一个坚定的愿景，这一点的重要性无论怎样强调都不过份。不过，愿景必须频繁地、定期地与用户的需求保持一致性。在本文中，Justin 将与你探讨如何确定你的产品路线图是否仍然贴合用户的需求。</p> <i>By Justin Zalewski</i> <i> Translated by 邵思华</i>
---------------
<h1 id="#title_6" >7、AWS发布Elastic Container Service for Kubernetes（EKS）</h1>
Richard Seroter
[http://www.infoq.com/cn/news/2018/06/kubernetes-amazon-eks?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/06/kubernetes-amazon-eks?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>在re:Invent 2017大会上，AWS预览了基于Kubernetes的容器服务。现在，六个月之后，Elastic Container Service for Kubernetes（EKS）正式发布。它加入了托管Kubernetes云服务的激烈竞争，每种服务提供不同的功能和部署地区。</p> <i>By Richard Seroter</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_7" >8、通过DevOps考古学了解生产环境</h1>
Manuel Pais
[http://www.infoq.com/cn/news/2018/06/devOps-archeology?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/06/devOps-archeology?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Infor云架构师Lee Fox在上个月举行的Continuous Lifecycle伦敦大会上发表了演讲，介绍了有助于理解当今复杂的系统和基础设施的工具和方法。与软件考古学领域类似，Fox把这个称为“DevOps考古学”。</p> <i>By Manuel Pais</i> <i> Translated by 无明</i>
---------------