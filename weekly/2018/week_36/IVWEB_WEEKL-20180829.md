## 文章索引
1、 <a href="#1best-practices-for-mobile-form-design" >Best Practices For Mobile Form Design</a><br/>
2、 <a href="#2文章-一年回顾测试可编程基础设施" >文章： 一年回顾：测试可编程基础设施</a><br/>
3、 <a href="#3文章-电商平台shopify的技术架构演进思路" >文章： 电商平台Shopify的技术架构演进思路</a><br/>
4、 <a href="#4文章-看苏宁易购的运营保障体系如何hold住818大促" >文章： 看苏宁易购的运营保障体系如何hold住818大促</a><br/>
5、 <a href="#5视频演讲-敏捷开发api网关与scf深度结合应用" >视频演讲： 敏捷开发：API网关与SCF深度结合应用</a><br/>
6、 <a href="#6bitbucket支持git-v2并改进了搜索功能" >BitBucket支持Git V2，并改进了搜索功能</a><br/>
7、 <a href="#7auth0转向基于aws的单云架构" >Auth0转向基于AWS的单云架构</a><br/>
8、 <a href="#8专访美图林添毅用-dpos-共识改造以太坊工程型人才转型区块链开发中的探索" >专访美图林添毅：用 DPos 共识改造以太坊，工程型人才转型区块链开发中的探索</a><br/>
9、 <a href="#9你真了解实时大数据高手们如何玩转开源流计算" >你真了解实时大数据？高手们如何玩转开源流计算？</a><br/>
10、 <a href="#10kubernetes原来可以如此简单" >Kubernetes，原来可以如此简单</a><br/><h1 id="#title_0" >1、Best Practices For Mobile Form Design</h1>
Nick Babich
[https://www.smashingmagazine.com/2018/08/best-practices-for-mobile-form-design/](https://www.smashingmagazine.com/2018/08/best-practices-for-mobile-form-design/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/08/best-practices-for-mobile-form-design/" />
              <title>Best Practices For Mobile Form Design</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>Best Practices For Mobile Form Design</h1>
                  
                    
                    <address>Nick Babich</address>
                  
                  <time datetime="2018-08-28T16:00:09&#43;02:00" class="op-published">2018-08-28T16:00:09+02:00</time>
                  <time datetime="2018-08-28T21:57:21&#43;00:00" class="op-modified">2018-08-28T21:57:21+00:00</time>
                </header>
                <p>(This article is kindly sponsored by Adobe.) Forms are the linchpin of all mobile interactions; it stands between the person and what they're looking for. Every day, we use forms for essential online activities. Recall the last time you bought a ticket, booked a hotel room or made a purchase online &mdash; most probably those interactions contained a step with filling out a form.</p>

<p>Forms are just a means to an end. Users should be able to complete them quickly and without confusion. In this article, you’ll learn practical techniques that will help you design an effective form.</p>

<h3>What Makes For An Effective Form</h3>

<p>The primary goal with every form is completion. Two factors have a major impact on completion rate:</p>

<ul>
<li><strong>Perception of complexity</strong><br />The first thing users do when they see a new form is estimate how much time is required to complete it. Users do this by scanning the form. Perception plays a crucial role in the process of estimation. The more complex a form looks, the more likely users will abandon the process.</li>
<li><strong>Interaction cost</strong><br />Interaction cost is the sum of efforts &mdash; both cognitive and physical &mdash; that the users put into interacting with an interface in order to reach their goal. Interaction cost has a direct connection with form usability. The more effort users have to make to complete a form, the less usable the form is. A high interaction cost could be the result of data that is difficult to input, an inability to understand the meaning of some questions, or confusion about error messages.</li>
</ul>

<h3>The Components Of Forms</h3>

<p>A typical form has the following five components:</p>

<ul>
<li><strong>Input fields</strong><br />These include text fields, password fields, checkboxes, radio buttons, sliders and any other fields designed for user input.</li>
<li><strong>Field labels</strong><br />These tell users what the corresponding input fields mean.</li>
<li><strong>Structure</strong><br />This includes the order of fields, the form’s appearance on the page, and the logical connections between different fields.</li>
<li><strong>Action buttons</strong><br />The form will have at least one call to action (the button that triggers data submission).</li>
<li><strong>Feedback</strong><br />Feedback notifies the user about the result of an operation. Feedback can be positive (for example, indicating that the form was submitted successfully) or negative (saying something like, “The number you’ve provided is incorrect”).</li>
</ul>

<p>This article covers many aspects related to structure, input fields, labels, action buttons and validation. Most points mentioned in this article have visual do and don’t examples; all such examples were created using .</p>

<h3>Input Fields</h3>

<p>When it comes to form design, the most important thing a designer can do is to minimize the need for typing. Reducing input effort is essential. Designers can achieve this goal by focusing on form field design.</p>

<h4>Minimize The Total Number Of Fields</h4>

<p>Every field you ask users to fill out requires some effort. The more effort is needed to fill out a form, the less likely users will complete the form. That’s why the foundational rule of form design is <strong>shorter is better</strong> &mdash; get rid of all inessential fields.</p>

<p>Baymard Institute analyzed checkout forms and found that a too  is one of the top reasons for abandonment during checkout. The study found that the average checkout contains almost 15 form fields. Most online services could reduce the number of fields displayed by default by 20 to 60%.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e582680c-98c9-4a88-8c5c-38ea030077b0/1-best-practices-for-mobile-form-design.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e582680c-98c9-4a88-8c5c-38ea030077b0/1-best-practices-for-mobile-form-design.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e582680c-98c9-4a88-8c5c-38ea030077b0/1-best-practices-for-mobile-form-design.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e582680c-98c9-4a88-8c5c-38ea030077b0/1-best-practices-for-mobile-form-design.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e582680c-98c9-4a88-8c5c-38ea030077b0/1-best-practices-for-mobile-form-design.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e582680c-98c9-4a88-8c5c-38ea030077b0/1-best-practices-for-mobile-form-design.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e582680c-98c9-4a88-8c5c-38ea030077b0/1-best-practices-for-mobile-form-design.jpg"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Top reasons for abandonment during checkout. (Image: )
		</figcaption>
	
</figure>


<p>Many designers are familiar with the “less is more” rule; still, they ask additional questions in an attempt to gather more data about their users. It might be tempting to collect more data about your users during the initial signup, but resist that temptation. Think about it this way: With every additional field you add to your form, you increase the chance of losing a prospective user. Is the information you gain from a field worth losing new users? Remember that, as long as you’ve collected a user’s contact information, you can always follow up with a request for more data.</p>

<h4>Clearly Distinguish All Optional Fields</h4>

<p>Before optimizing optional fields, ask yourself whether you really need to include them in your form. Think about what information you really need, not what you want. Ideally, the number of optional fields in your form should be zero.</p>

<p>If after a brainstorming session, you still want to include a few optional questions in your form, make it clear for users that those fields are optional:</p>

<ul>
<li><strong>Mark optional fields instead of mandatory ones.</strong><br />If you ask as little as possible, then the vast majority of fields in your form will be mandatory. Therefore, mark only those fields in the minority. For instance, if five out of six fields are mandatory, then it makes sense to mark only one field as optional.</li>
<li><strong>Use the “Optional” label to denote optional fields.</strong><br />Avoid using the asterisk (<code>*</code>) to mean “optional.” Not all users will associate the asterisk with optional information, and some users will be confused by the meaning (an asterisk is often used to denote mandatory fields).</li>
</ul>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/328909f7-3c19-4b0c-99a1-7d20e2a339b4/2-best-practices-for-mobile-form-design.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/328909f7-3c19-4b0c-99a1-7d20e2a339b4/2-best-practices-for-mobile-form-design.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/328909f7-3c19-4b0c-99a1-7d20e2a339b4/2-best-practices-for-mobile-form-design.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/328909f7-3c19-4b0c-99a1-7d20e2a339b4/2-best-practices-for-mobile-form-design.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/328909f7-3c19-4b0c-99a1-7d20e2a339b4/2-best-practices-for-mobile-form-design.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/328909f7-3c19-4b0c-99a1-7d20e2a339b4/2-best-practices-for-mobile-form-design.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/328909f7-3c19-4b0c-99a1-7d20e2a339b4/2-best-practices-for-mobile-form-design.png"
			sizes="100vw"
			alt="Clearly distinguish all optional fields."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Clearly distinguish all optional fields. ()
		</figcaption>
	
</figure>


<h4>Size Fields Accordingly</h4>

<p>When possible, use field length as an affordance. The length of an input field should be in proportion to the amount of information expected in the field. The size of the field will act as a visual constraint &mdash; the user will know how much text is expected to be entered just by looking at the field. Generally, fields such as ones for area codes and house numbers should be shorter than ones for street addresses.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/16b52630-9da6-4376-a4bb-b8725eb8be5d/3-best-practices-for-mobile-form-design.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/16b52630-9da6-4376-a4bb-b8725eb8be5d/3-best-practices-for-mobile-form-design.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/16b52630-9da6-4376-a4bb-b8725eb8be5d/3-best-practices-for-mobile-form-design.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/16b52630-9da6-4376-a4bb-b8725eb8be5d/3-best-practices-for-mobile-form-design.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/16b52630-9da6-4376-a4bb-b8725eb8be5d/3-best-practices-for-mobile-form-design.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/16b52630-9da6-4376-a4bb-b8725eb8be5d/3-best-practices-for-mobile-form-design.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/16b52630-9da6-4376-a4bb-b8725eb8be5d/3-best-practices-for-mobile-form-design.png"
			sizes="100vw"
			alt="The size of a field is used as a visual constraint."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The size of a field is used as a visual constraint. ()
		</figcaption>
	
</figure>


<h4>Offer Field Focus</h4>

<p>Auto-focus the first input field in your form. Auto-focusing a field gives the user an indication and a starting point, so that they are able to quickly start filling out the form. By doing that, you reduce the interaction cost &mdash; saving the user one unnecessary tap.</p>

<p>Make the active input field prominent and focused. The field focus itself should be crystal clear &mdash; users should be able to understand at a glance where the focus is. It could be an accented border color or a fade-in of the box.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8acc2fd0-713c-4595-adc3-4d4cdfc44843/4-best-practices-for-mobile-form-design.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8acc2fd0-713c-4595-adc3-4d4cdfc44843/4-best-practices-for-mobile-form-design.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8acc2fd0-713c-4595-adc3-4d4cdfc44843/4-best-practices-for-mobile-form-design.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8acc2fd0-713c-4595-adc3-4d4cdfc44843/4-best-practices-for-mobile-form-design.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8acc2fd0-713c-4595-adc3-4d4cdfc44843/4-best-practices-for-mobile-form-design.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8acc2fd0-713c-4595-adc3-4d4cdfc44843/4-best-practices-for-mobile-form-design.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8acc2fd0-713c-4595-adc3-4d4cdfc44843/4-best-practices-for-mobile-form-design.png"
			sizes="100vw"
			alt="Amazon puts strong visual focus on the input field."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Amazon puts strong visual focus on the input field. ()
		</figcaption>
	
</figure>


<h4>Don’t Ask Users To Repeat Their Email Address</h4>

<p>The reason why an extra field for the email address is so popular among product developers is apparent: Every company wants to minimize the risk of hard bounces (non-deliverables caused by invalid email addresses). Unfortunately, following this approach doesn’t guarantee that you’ll get a valid address. Users often copy and paste their address from one field to another.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bb8d8c0c-0168-4a89-805f-23fb808c0b71/5-best-practices-for-mobile-form-design.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bb8d8c0c-0168-4a89-805f-23fb808c0b71/5-best-practices-for-mobile-form-design.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bb8d8c0c-0168-4a89-805f-23fb808c0b71/5-best-practices-for-mobile-form-design.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bb8d8c0c-0168-4a89-805f-23fb808c0b71/5-best-practices-for-mobile-form-design.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bb8d8c0c-0168-4a89-805f-23fb808c0b71/5-best-practices-for-mobile-form-design.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bb8d8c0c-0168-4a89-805f-23fb808c0b71/5-best-practices-for-mobile-form-design.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bb8d8c0c-0168-4a89-805f-23fb808c0b71/5-best-practices-for-mobile-form-design.png"
			sizes="100vw"
			alt="Avoid asking users to retype their email address."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Avoid asking users to retype their email address. ()
		</figcaption>
	
</figure>


<h4>Provide “Show Password” Option</h4>

<p>Duplicating the password input field is another common mistake among product designers. Designers follow this approach because they believe it will prevent users from mistyping a password. In reality, a second field for a password not only increases interaction cost, but also doesn't guarantee that users will proceed without mistakes. Because users don’t see what they’ve entered in the field, they can make the same mistake twice (in both fields) and will face a problem when they try to log in using a password. As </p>

<blockquote>Usability suffers when users type in passwords and the only feedback they get is a row of bullets. Typically, masking passwords doesn’t even increase security, but it does cost you business due to login failures.</blockquote>

<p>Instead of duplicating the password field, provide an option that allows users to view the password they have chosen to create. Have an icon or checkbox that unmasks the password when clicked. A password preview can be an opportunity for users to check their data before sending.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/97655e3a-3767-4472-a941-9dc10e3ad003/6-best-practices-for-mobile-form-design.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/97655e3a-3767-4472-a941-9dc10e3ad003/6-best-practices-for-mobile-form-design.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/97655e3a-3767-4472-a941-9dc10e3ad003/6-best-practices-for-mobile-form-design.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/97655e3a-3767-4472-a941-9dc10e3ad003/6-best-practices-for-mobile-form-design.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/97655e3a-3767-4472-a941-9dc10e3ad003/6-best-practices-for-mobile-form-design.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/97655e3a-3767-4472-a941-9dc10e3ad003/6-best-practices-for-mobile-form-design.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/97655e3a-3767-4472-a941-9dc10e3ad003/6-best-practices-for-mobile-form-design.png"
			sizes="100vw"
			alt="Show password&#39; option"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Not being able to see what you're typing is a huge issue. Providing a 'Show password' option next to the password field will help to solve this problem. ()
		</figcaption>
	
</figure>


<h4>Don’t Slice Data Fields</h4>

<p>Do not slice fields when asking for a full name, phone number or date of birth. Sliced fields force the user to make additional taps to move to the next field. For fields that require some formatting (such as phone numbers or a date of birth), it’s also better to have a single field paired with clear formatting rules as its placeholder.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/080ce741-ea2c-4b49-91be-5253bc5cf9aa/7-best-practices-for-mobile-form-design.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/080ce741-ea2c-4b49-91be-5253bc5cf9aa/7-best-practices-for-mobile-form-design.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/080ce741-ea2c-4b49-91be-5253bc5cf9aa/7-best-practices-for-mobile-form-design.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/080ce741-ea2c-4b49-91be-5253bc5cf9aa/7-best-practices-for-mobile-form-design.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/080ce741-ea2c-4b49-91be-5253bc5cf9aa/7-best-practices-for-mobile-form-design.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/080ce741-ea2c-4b49-91be-5253bc5cf9aa/7-best-practices-for-mobile-form-design.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/080ce741-ea2c-4b49-91be-5253bc5cf9aa/7-best-practices-for-mobile-form-design.png"
			sizes="100vw"
			alt="“Full name” field"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Avoid splitting input fields; don’t make people jump between fields. Instead of asking for a first name and last name in two separate fields, have a single 'Full name' field. ()
		</figcaption>
	
</figure>


<h4>Avoid Dropdown Menus</h4>

<p>Luke Wroblewski famously said that . Dropdowns are especially bad for mobile because collapsed elements make the process of data input harder on a small screen: Placing options in a dropdown requires two taps and hides the options.</p>

<p>If you’re using a dropdown for selection of options, consider replacing it with radio buttons. They will make all options glanceable and also reduce the interaction cost &mdash; users can tap on the item and select at once.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e80b0e47-d91d-48f5-bf9e-52a6aeb8ab71/8-best-practices-for-mobile-form-design.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e80b0e47-d91d-48f5-bf9e-52a6aeb8ab71/8-best-practices-for-mobile-form-design.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e80b0e47-d91d-48f5-bf9e-52a6aeb8ab71/8-best-practices-for-mobile-form-design.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e80b0e47-d91d-48f5-bf9e-52a6aeb8ab71/8-best-practices-for-mobile-form-design.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e80b0e47-d91d-48f5-bf9e-52a6aeb8ab71/8-best-practices-for-mobile-form-design.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e80b0e47-d91d-48f5-bf9e-52a6aeb8ab71/8-best-practices-for-mobile-form-design.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e80b0e47-d91d-48f5-bf9e-52a6aeb8ab71/8-best-practices-for-mobile-form-design.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<h4>Use Placeholders And Masked Input</h4>

<p>Formatting uncertainty is one of the most significant problems of form design. This problem has a direct connection with form abandonment &mdash; when users are uncertain of the format in which they should provide data, they can quickly abandon the form. There are a few things you can do to make the format clear.</p>

<h5>Placeholder Text</h5>

<p>The text in an input field can tell users what content is expected. Placeholder text is not required for simple fields such as “Full name”, but it can be extremely valuable for fields that require data in a specific format. For example, if you design search functionality for tracking a parcel, it would be good to provide a sample tracking number as a placeholder for the tracking-number field.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5c1adc2d-f4f5-4bad-95b9-fe13f3d44953/9-best-practices-for-mobile-form-design.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5c1adc2d-f4f5-4bad-95b9-fe13f3d44953/9-best-practices-for-mobile-form-design.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5c1adc2d-f4f5-4bad-95b9-fe13f3d44953/9-best-practices-for-mobile-form-design.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5c1adc2d-f4f5-4bad-95b9-fe13f3d44953/9-best-practices-for-mobile-form-design.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5c1adc2d-f4f5-4bad-95b9-fe13f3d44953/9-best-practices-for-mobile-form-design.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5c1adc2d-f4f5-4bad-95b9-fe13f3d44953/9-best-practices-for-mobile-form-design.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5c1adc2d-f4f5-4bad-95b9-fe13f3d44953/9-best-practices-for-mobile-form-design.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<p>It’s vital that your form should have a clear visual distinction between the placeholder text and the actual value entered by the user. In other words, placeholder text shouldn’t look like a preset value. Without clear visual distinction, users might think that the fields with placeholders already have values.</p>

<h5>Masked Input</h5>

<p>Field masking is a technique that helps users format inputted text. Many designers confuse field masking with placeholder text &mdash; they are not the same thing. Unlike placeholders, which are basically static text, masks automatically format the data provided by the user. In the example below, the parentheses, spaces and dashes appear on the screen automatically as a phone number is entered.</p>

<p>Masked input also makes it easy for users to validate information. When a phone number is displayed in chunks, it makes it easier to find and correct a typo.</p>

<figure>)</figcaption></figure>

<h4>Provide Matching Keyboard</h4>

<p>Mobile users appreciate apps and websites that provide an appropriate keyboard for the field. This feature prevents them from doing additional actions. For example, when users need to enter a credit card number, your app should only display the dialpad. It’s essential to implement keyboard matching consistently throughout the app (all forms in your app should have this feature).</p>

<p>Set HTML input types to show the correct keypad. Seven input types are relevant to form design:</p>

<ul>
<li><code>input type="text"</code> displays the mobile device’s normal keyboard.</li>
<li><code>input type="email"</code> displays the normal keyboard and '@' and '.com'.</li>
<li><code>input type="tel"</code> displays the numeric 0 to 9 keypad.</li>
<li><code>input type="number"</code> displays a keyboard with numbers and symbols.</li>
<li><code>input type="date"</code> displays the mobile device’s date selector.</li>
<li><code>input type="datetime"</code> displays the mobile device’s date and time selector.</li>
<li><code>input type="month"</code> displays the mobile device’s month and year selector.</li>
</ul>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/71c053d5-9037-4357-9b65-59e7a9aaa39f/11-best-practices-for-mobile-form-design.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/71c053d5-9037-4357-9b65-59e7a9aaa39f/11-best-practices-for-mobile-form-design.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/71c053d5-9037-4357-9b65-59e7a9aaa39f/11-best-practices-for-mobile-form-design.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/71c053d5-9037-4357-9b65-59e7a9aaa39f/11-best-practices-for-mobile-form-design.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/71c053d5-9037-4357-9b65-59e7a9aaa39f/11-best-practices-for-mobile-form-design.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/71c053d5-9037-4357-9b65-59e7a9aaa39f/11-best-practices-for-mobile-form-design.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/71c053d5-9037-4357-9b65-59e7a9aaa39f/11-best-practices-for-mobile-form-design.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			When users tap into a field with credit card number, they should see a numerical dialpad &mdash; all numbers, no letters. ()
		</figcaption>
	
</figure>


<h4>Use A Slider When Asking For A Specific Range</h4>

<p>Many forms ask users to provide a range of values (for example, a price range, distance range, etc.). Instead of using two separate fields, “from” and “to”, for that purpose, use a slider to allow users to specify the range with a thumb interaction.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cfc67b22-bd99-423a-8af1-3a709d2e737d/12-best-practices-for-mobile-form-design.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cfc67b22-bd99-423a-8af1-3a709d2e737d/12-best-practices-for-mobile-form-design.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cfc67b22-bd99-423a-8af1-3a709d2e737d/12-best-practices-for-mobile-form-design.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cfc67b22-bd99-423a-8af1-3a709d2e737d/12-best-practices-for-mobile-form-design.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cfc67b22-bd99-423a-8af1-3a709d2e737d/12-best-practices-for-mobile-form-design.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cfc67b22-bd99-423a-8af1-3a709d2e737d/12-best-practices-for-mobile-form-design.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cfc67b22-bd99-423a-8af1-3a709d2e737d/12-best-practices-for-mobile-form-design.png"
			sizes="100vw"
			alt="Sliders are good for touch interfaces because they allow users to specify a range without typing."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Sliders are good for touch interfaces because they allow users to specify a range without typing. ()
		</figcaption>
	
</figure>


<h4>Clearly Explain Why You’re Asking For Sensitive Information</h4>

<p>People are increasingly concerned about privacy and information security. When users see a request for information they consider as private, they might think, “Hm, why do they need this?” If your form asks users for sensitive information, make sure to explain why you need it. You can do that by adding support text below relevant fields. As a rule of thumb, the explanation text shouldn’t exceed 100 characters.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/074980c9-0960-4044-81c0-3df357fdd341/13-best-practices-for-mobile-form-design.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/074980c9-0960-4044-81c0-3df357fdd341/13-best-practices-for-mobile-form-design.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/074980c9-0960-4044-81c0-3df357fdd341/13-best-practices-for-mobile-form-design.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/074980c9-0960-4044-81c0-3df357fdd341/13-best-practices-for-mobile-form-design.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/074980c9-0960-4044-81c0-3df357fdd341/13-best-practices-for-mobile-form-design.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/074980c9-0960-4044-81c0-3df357fdd341/13-best-practices-for-mobile-form-design.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/074980c9-0960-4044-81c0-3df357fdd341/13-best-practices-for-mobile-form-design.png"
			sizes="100vw"
			alt="A request for a phone number in a booking form might confuse users. Explain why you are asking for it."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			A request for a phone number in a booking form might confuse users. Explain why you are asking for it. ()
		</figcaption>
	
</figure>


<h4>Be Careful With Static Defaults</h4>

<p>Unlike smart defaults, which are calculated by the system based on the information the system has about users, static defaults are preset values in forms that are the same for all users. Avoid static defaults unless you believe a significant portion of your users (say, 95%) would select those values &mdash; particularly for required fields. Why? Because you’re likely to introduce errors &mdash; people scan forms quickly, and they won’t spend extra time parsing all of the questions; instead, they’ll simply skip the field, assuming it already has a value.</p>

<h4>Protect User Data</h4>

<p>Jef Raskin once said, “The system should treat all user input as sacred.” This is absolutely true for forms. It’s great when you start filling in a web form and then accidentally refresh the page but the data remains in the fields. Tools such as  help you to persist a form’s values locally until the form is submitted. This way, users won’t lose any precious data if they accidentally close the tab or browser.</p>

<h4>Automate Actions</h4>

<p>If you want to make the process of data input as smooth as possible, it's not enough to minimize the number of input fields &mdash; you should also pay attention to the user effort required for the data input. Typing has a high interaction cost &mdash; it’s error-prone and time-consuming, even with a physical keyboard. But when it comes to mobile screens, it becomes even more critical. More typing increases the user’s chance of making errors. Strive to prevent unnecessary typing, because it will improve user satisfaction and decrease error rates.</p>

<p>Here are a few things you can do to achieve this goal:</p>

<h5>Autocomplete</h5>

<p>Most users experience autocompletion when typing a question in Google’s search box. Google provides users with a list of suggestions related to what the user has typed in the field. The same mechanism can be applied to form design. For example, a form could autocomplete an email address.</p>

<figure>)</figcaption></figure>

<h5>Autocapitalize</h5>

<p>Autocapitalizing makes the first letter a capital automatically. This feature is excellent for fields like names and street addresses, but avoid it for password fields.</p>

<h5>Autocorrect</h5>

<p>Autocorrection modifies words that appear to be misspelled. Turn this feature off for unique fields, such as names, addresses, etc.</p>

<h5>Auto-filling of personal details</h5>

<p>Typing an address is often the most cumbersome part of any online signup form. Make this task easier by using the browser function to fill the field based on previously entered values. According to , auto-filling helps people fill out forms 30% faster.</p>

<figure></figcaption></figure>

<h4>Use The Mobile Device’s Native Features To Simplify Data Input</h4>

<p>Modern mobile devices are sophisticated devices that have a ton of amazing capabilities. Designers can use a device’s native features (such as camera or geolocation) to streamline the task of inputting data.</p>

<p>Below are just a few tips on how to make use of sensors and device hardware.</p>

<h5>Location Services</h5>

<p>It’s possible to preselect the user’s country based on their geolocation data. But sometimes prefilling a full address can be problematic due to accuracy issues.  can help solve this problem. It uses both geolocation and address prefilling to provide accurate suggestions based on the user’s exact location.</p>

<figure>)</figcaption></figure>

<p>Using location services, it’s also possible to provide smart defaults. For example, for a “Find a flight” form, it’s possible to prefill the “From” field with the nearest airport to the user based on the user’s geolocation.</p>

<h5>Biometric Authorization</h5>

<p>The biggest problem of using a text password today is that most people forget passwords.  if they had to attempt to recover their password while checking out.</p>

<p>The future of passwords is no passwords. Even today, mobile developers can take advantage of biometric technologies. Users shouldn’t need to type a password; they should be able to use biometric readers for authentication &mdash; signing in using a fingerprint or face scanning.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dd8f2b47-0177-410f-a5b5-ffb77be89f14/17-best-practices-for-mobile-form-design.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dd8f2b47-0177-410f-a5b5-ffb77be89f14/17-best-practices-for-mobile-form-design.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dd8f2b47-0177-410f-a5b5-ffb77be89f14/17-best-practices-for-mobile-form-design.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dd8f2b47-0177-410f-a5b5-ffb77be89f14/17-best-practices-for-mobile-form-design.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dd8f2b47-0177-410f-a5b5-ffb77be89f14/17-best-practices-for-mobile-form-design.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dd8f2b47-0177-410f-a5b5-ffb77be89f14/17-best-practices-for-mobile-form-design.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dd8f2b47-0177-410f-a5b5-ffb77be89f14/17-best-practices-for-mobile-form-design.png"
			sizes="100vw"
			alt="eBay took advantage of the biometrics functionality on smartphones. Users can use their thumbprint to login into their eBay account."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			eBay took advantage of the biometrics functionality on smartphones. Users can use their thumbprint to login into their eBay account. ()
		</figcaption>
	
</figure>


<h5>Camera</h5>

<p>If your form asks users to provide credit card details or information from their driver’s license, it’s possible to simplify the process of data input by using the camera as a scanner. Provide an option to take a photo of the card and fill out all details automatically.</p>

<figure>)</figcaption></figure>

<p>But remember that no matter how good your app fills out the fields, it’s essential to leave them available for editing. Users should be able to modify the fields whenever they want.</p>

<h5>Voice</h5>

<p>Voice-controlled devices, such as Apple HomePod, Google Home and Amazon Echo, are actively encroaching on the market. The number of people who prefer to use voice for common operations has grown significantly. According to ComScore, .</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/873d6fc2-dbff-4e23-844d-3944963c58f6/19-best-practices-for-mobile-form-design.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/873d6fc2-dbff-4e23-844d-3944963c58f6/19-best-practices-for-mobile-form-design.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/873d6fc2-dbff-4e23-844d-3944963c58f6/19-best-practices-for-mobile-form-design.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/873d6fc2-dbff-4e23-844d-3944963c58f6/19-best-practices-for-mobile-form-design.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/873d6fc2-dbff-4e23-844d-3944963c58f6/19-best-practices-for-mobile-form-design.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/873d6fc2-dbff-4e23-844d-3944963c58f6/19-best-practices-for-mobile-form-design.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/873d6fc2-dbff-4e23-844d-3944963c58f6/19-best-practices-for-mobile-form-design.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			How people in the US use smart speakers (according to )
		</figcaption>
	
</figure>


<p>As users get more comfortable and confident using voice commands, they will become an expected feature of mobile interactions. Voice input provides a lot of advantages for mobile users &mdash; it’s especially valuable in situations when users can’t focus on a screen, for example, while driving a car.</p>

<p>When designing a form, you can provide voice input as an alternative method of data input.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/32fd22df-6c88-472f-af88-60314af7cc81/20-best-practices-for-mobile-form-design.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/32fd22df-6c88-472f-af88-60314af7cc81/20-best-practices-for-mobile-form-design.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/32fd22df-6c88-472f-af88-60314af7cc81/20-best-practices-for-mobile-form-design.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/32fd22df-6c88-472f-af88-60314af7cc81/20-best-practices-for-mobile-form-design.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/32fd22df-6c88-472f-af88-60314af7cc81/20-best-practices-for-mobile-form-design.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/32fd22df-6c88-472f-af88-60314af7cc81/20-best-practices-for-mobile-form-design.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/32fd22df-6c88-472f-af88-60314af7cc81/20-best-practices-for-mobile-form-design.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Google Translate provides an option to enter the text for translation using voice. ()
		</figcaption>
	
</figure>


<h3>Field Labels</h3>

<h4>Write Clear And Concise Labels</h4>

<p>The label is the text that tells users what data is expected from them in a particular input field. Writing clear labels is one of the best ways to make a form more accessible. Labels should help the user understand what information is required at a glance.</p>

<p>Avoid using complete sentences to explain. A label is not help text. Write succinct and crisp labels (a word or two), so that users can quickly scan your form.</p>

<h4>Place The Label And Input Close Together</h4>

<p>Put each label close to the input field, because the eye will visually know they’re tied together.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e4966559-5928-4aab-b6e5-fb34ae0e4691/21-best-practices-for-mobile-form-design.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e4966559-5928-4aab-b6e5-fb34ae0e4691/21-best-practices-for-mobile-form-design.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e4966559-5928-4aab-b6e5-fb34ae0e4691/21-best-practices-for-mobile-form-design.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e4966559-5928-4aab-b6e5-fb34ae0e4691/21-best-practices-for-mobile-form-design.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e4966559-5928-4aab-b6e5-fb34ae0e4691/21-best-practices-for-mobile-form-design.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e4966559-5928-4aab-b6e5-fb34ae0e4691/21-best-practices-for-mobile-form-design.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e4966559-5928-4aab-b6e5-fb34ae0e4691/21-best-practices-for-mobile-form-design.png"
			sizes="100vw"
			alt="A label and its field should be visually grouped, so that users can understand which label belongs to which field."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			A label and its field should be visually grouped, so that users can understand which label belongs to which field. ()
		</figcaption>
	
</figure>


<h4>Don’t Use Disappearing Placeholder Text As Labels</h4>

<p>While inline labels look good and save valuable screen estate, these benefits are far outweighed by the significant usability drawbacks, the most critical of which is the loss of context. When users start entering text in a field, the placeholder text disappears and forces people to recall this information. While it might not be a problem for simple two-field forms, it could be a big deal for forms that have a lot of fields (say, 7 to 10). It would be tough for users to recall all field labels after inputting data. Not surprisingly, user testing continually shows that  more than help.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/83382f56-8b99-4e7c-b992-1470df20bc03/22-best-practices-for-mobile-form-design.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/83382f56-8b99-4e7c-b992-1470df20bc03/22-best-practices-for-mobile-form-design.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/83382f56-8b99-4e7c-b992-1470df20bc03/22-best-practices-for-mobile-form-design.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/83382f56-8b99-4e7c-b992-1470df20bc03/22-best-practices-for-mobile-form-design.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/83382f56-8b99-4e7c-b992-1470df20bc03/22-best-practices-for-mobile-form-design.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/83382f56-8b99-4e7c-b992-1470df20bc03/22-best-practices-for-mobile-form-design.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/83382f56-8b99-4e7c-b992-1470df20bc03/22-best-practices-for-mobile-form-design.png"
			sizes="100vw"
			alt="Don’t use placeholder text that disappears when the user interacts with the field."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Don’t use placeholder text that disappears when the user interacts with the field. ()
		</figcaption>
	
</figure>


<p>There’s a simple solution to the problem of disappearing placeholders: the floating (or adaptive) label. After the user taps on the field with the label placeholder, the label doesn’t disappear, it moves up to the top of the field and makes room for the user to enter their data.</p>

<figure>)</figcaption></figure>

<h4>Top-Align Labels</h4>

<p>Putting field labels above the fields in a form improves the way users scan the form. Using eye-tracking technology for this, Google showed that users need , less fixation time and fewer saccades before submitting a form.</p>

<p>Another important advantage of top-aligned labels is that they provide more space for labels. Long labels and localized versions will fit more easily in the layout. The latter is especially suitable for small mobile screens. You can have form fields extend the full width of the screen, making them large enough to display the user’s entire input.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c5d00e59-ec24-439d-abfa-c8523f74e09d/24-best-practices-for-mobile-form-design.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c5d00e59-ec24-439d-abfa-c8523f74e09d/24-best-practices-for-mobile-form-design.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c5d00e59-ec24-439d-abfa-c8523f74e09d/24-best-practices-for-mobile-form-design.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c5d00e59-ec24-439d-abfa-c8523f74e09d/24-best-practices-for-mobile-form-design.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c5d00e59-ec24-439d-abfa-c8523f74e09d/24-best-practices-for-mobile-form-design.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c5d00e59-ec24-439d-abfa-c8523f74e09d/24-best-practices-for-mobile-form-design.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c5d00e59-ec24-439d-abfa-c8523f74e09d/24-best-practices-for-mobile-form-design.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<h4>Sentence Case Vs. Title Case</h4>

<p>There are two general ways to capitalize words:</p>

<ul>
<li>Title case: Capitalize every word. “This Is Title Case.”</li>
<li>Sentence case: Capitalize the first word. “This is sentence case.”</li>
</ul>

<p>Using sentence case for labels has one advantage over title case: It is slightly easier (and, thus, faster) to read. While the difference for short labels is negligible (there’s not much difference between “Full Name” and “Full name”), for longer labels, sentence case is better. Now You Know How Difficult It Is to Read Long Text in Title Case.</p>

<h4>Avoid Using Caps For Labels</h4>

<p>All-caps text  &mdash;  meaning text with all of the letters cap­i­tal­ized  &mdash;  is OK in contexts that don’t involve substantive reading (such as acronyms and logos), but avoid all caps otherwise. As mentioned by  in his work <em>Legibility of Print</em>, all-capital print dramatically slows the speed of scanning and reading compared to lowercase type.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4db9e926-8318-4a23-a2d9-2243e49c8fbe/25-best-practices-for-mobile-form-design.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4db9e926-8318-4a23-a2d9-2243e49c8fbe/25-best-practices-for-mobile-form-design.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4db9e926-8318-4a23-a2d9-2243e49c8fbe/25-best-practices-for-mobile-form-design.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4db9e926-8318-4a23-a2d9-2243e49c8fbe/25-best-practices-for-mobile-form-design.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4db9e926-8318-4a23-a2d9-2243e49c8fbe/25-best-practices-for-mobile-form-design.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4db9e926-8318-4a23-a2d9-2243e49c8fbe/25-best-practices-for-mobile-form-design.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4db9e926-8318-4a23-a2d9-2243e49c8fbe/25-best-practices-for-mobile-form-design.png"
			sizes="100vw"
			alt="All-capitalized letters"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			All-capitalized letters are hard to scan and read. ()
		</figcaption>
	
</figure>


<h3>Layout</h3>

<p>You know by now that . The same goes for filling out forms. That’s why designers should design a form that is easy to scan. Allowing for efficient, effective scanning is crucial to making the process of the filling out a form as quick as possible.</p>

<h4>Use A Single-Column Layout</h4>

<p>A  found that single-column forms are faster to complete than multi-column forms. In that study, test participants were able to complete a single-column form an average of 15.4 seconds faster than a multi-column form.</p>

<p>Multiple columns disrupt a user’s vertical momentum; with multiple columns, the eyes start zigzagging. This dramatically increases the number of eye fixations and, as a result, the completion time. Moreover, multiple-column forms might raise unnecessary questions in the user, like “Where should I begin?” and “Are questions in the right column equal in importance to questions in the left one?”</p>

<p>In a one-column design, the eyes move in a natural direction, from top to bottom, one line at a time. This helps to set a clear path for the user. One column is excellent for mobile because the screens are longer vertically, and vertical scrolling is .</p>

<p>There are some exceptions to this rule. It’s possible to place short and logically related fields on the same row (such as for the city and area code).</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b46639c6-09c3-467f-a5da-8add29ff8661/26-best-practices-for-mobile-form-design.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b46639c6-09c3-467f-a5da-8add29ff8661/26-best-practices-for-mobile-form-design.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b46639c6-09c3-467f-a5da-8add29ff8661/26-best-practices-for-mobile-form-design.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b46639c6-09c3-467f-a5da-8add29ff8661/26-best-practices-for-mobile-form-design.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b46639c6-09c3-467f-a5da-8add29ff8661/26-best-practices-for-mobile-form-design.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b46639c6-09c3-467f-a5da-8add29ff8661/26-best-practices-for-mobile-form-design.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b46639c6-09c3-467f-a5da-8add29ff8661/26-best-practices-for-mobile-form-design.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			If a form has horizontally adjacent fields, the user has to scan the form following a Z pattern. When the eyes start zigzagging, it slows the speed of comprehension and increases completion time. ()
		</figcaption>
	
</figure>












<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e0c5b631-be70-45f6-9569-f6cef8a3ef53/27-best-practices-for-mobile-form-design.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e0c5b631-be70-45f6-9569-f6cef8a3ef53/27-best-practices-for-mobile-form-design.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e0c5b631-be70-45f6-9569-f6cef8a3ef53/27-best-practices-for-mobile-form-design.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e0c5b631-be70-45f6-9569-f6cef8a3ef53/27-best-practices-for-mobile-form-design.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e0c5b631-be70-45f6-9569-f6cef8a3ef53/27-best-practices-for-mobile-form-design.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e0c5b631-be70-45f6-9569-f6cef8a3ef53/27-best-practices-for-mobile-form-design.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e0c5b631-be70-45f6-9569-f6cef8a3ef53/27-best-practices-for-mobile-form-design.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<h4>Create A Flow With Your Questions</h4>

<p>The way you ask questions also matters. Questions should be asked logically from the user’s perspective, not according to the application or database’s logic, because it will help to create a sense of conversation with the user. For example, if you design a checkout form and asks for details such as full name, phone number and credit card, the first question should be for the full name. Changing the order (for example, starting with a phone number instead of a name) leads to discomfort. In real-world conversations, it would be unusual to ask for someone’s phone number before asking their name.</p>

<h4>Defer In-Depth Questions To The End</h4>

<p>When it comes to designing a flow for questions you want to ask, think about prioritization. Follow the rule “easy before difficult” and place in-depth or personal questions last. This eases users into the process; they will be more likely to answer complex and more intrusive questions once they’ve established a rapport. This has a scientific basis:  stipulates that when someone takes a small action or step towards something, they feel more compelled to finish.</p>

<h4>Group Related Fields Together</h4>

<p>One of the principles of Gestalt psychology, the principle of proximity, states that related elements should be near each other. This principle can be applied to the order of questions in a form. The more related questions are, the closer they should be to each other.</p>

<p>Designers can group related fields into sections. If your form has more than six questions, group related questions into logical sections. Don’t forget to provide a good amount of white space between sections to distinguish them visually.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cf242705-2501-48ca-99c5-0c363b297923/28-best-practices-for-mobile-form-design.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cf242705-2501-48ca-99c5-0c363b297923/28-best-practices-for-mobile-form-design.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cf242705-2501-48ca-99c5-0c363b297923/28-best-practices-for-mobile-form-design.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cf242705-2501-48ca-99c5-0c363b297923/28-best-practices-for-mobile-form-design.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cf242705-2501-48ca-99c5-0c363b297923/28-best-practices-for-mobile-form-design.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cf242705-2501-48ca-99c5-0c363b297923/28-best-practices-for-mobile-form-design.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cf242705-2501-48ca-99c5-0c363b297923/28-best-practices-for-mobile-form-design.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Generally, if your form has more than six questions, it’s better to group related questions into logical sections. Put things together that make sense together. ()
		</figcaption>
	
</figure>


<h4>Make A Long Form Look Simpler</h4>

<p>How do you design a form that asks users a lot of questions? Of course, you could put all of the questions on one screen. But this hinder your completion rate. If users don’t have enough motivation to complete a form, the form’s complexity could scare them away. The first impression plays a vital role. Generally, the longer or more complicated a form seems, the less likely users will be to start filling in the blanks.</p>

<p>Minimize the number of fields visible at one time. This creates the perception that the form is shorter than it really is.</p>

<p>There are two techniques to do this.</p>

<h5>Progressive Disclosure</h5>

<p>Progressive disclosure is all about giving users the right thing at the right time. The goal is to find the right stuff to put on the small screen at the right time:</p>

<ul>
<li>Initially, show users only a few of the most important options.</li>
<li>Reveal parts of your form as the user interacts with it.</li>
</ul>

<figure>)</figcaption></figure>

<h5>Chunking</h5>

<p>Chunking entails breaking a long form into steps. It’s possible to increase the completion rate by splitting a form into a few steps. Chunking can also help users . When designing multi-step forms, always inform users of their progress with a completeness meter.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f7019860-b160-4a24-a198-5d0723009259/30-best-practices-for-mobile-form-design.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f7019860-b160-4a24-a198-5d0723009259/30-best-practices-for-mobile-form-design.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f7019860-b160-4a24-a198-5d0723009259/30-best-practices-for-mobile-form-design.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f7019860-b160-4a24-a198-5d0723009259/30-best-practices-for-mobile-form-design.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f7019860-b160-4a24-a198-5d0723009259/30-best-practices-for-mobile-form-design.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f7019860-b160-4a24-a198-5d0723009259/30-best-practices-for-mobile-form-design.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f7019860-b160-4a24-a198-5d0723009259/30-best-practices-for-mobile-form-design.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Progress tracker for e-commerce form. (Image: )
		</figcaption>
	
</figure>


<p>Designers can use either a progress tracker (as shown in the example above) or a “Step # out of #” indicator both to tell how many steps there are total and to show how far along the user is at the moment. The latter approach could be great for mobile forms because step indication doesn’t take up much space.</p>

<h3>Action Buttons</h3>

<p>A button is an interactive element that direct users to take an action.</p>

<h4>Make Action Buttons Descriptive</h4>

<p>A button’s label should explain what the button does; users should be able to understand what happens after a tap just by looking at the button. Avoid generic labels such as “Submit” and “Send”, using instead labels that describe the action.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/100aa67d-954a-4b63-ae18-aab02054b243/31-best-practices-for-mobile-form-design.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/100aa67d-954a-4b63-ae18-aab02054b243/31-best-practices-for-mobile-form-design.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/100aa67d-954a-4b63-ae18-aab02054b243/31-best-practices-for-mobile-form-design.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/100aa67d-954a-4b63-ae18-aab02054b243/31-best-practices-for-mobile-form-design.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/100aa67d-954a-4b63-ae18-aab02054b243/31-best-practices-for-mobile-form-design.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/100aa67d-954a-4b63-ae18-aab02054b243/31-best-practices-for-mobile-form-design.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/100aa67d-954a-4b63-ae18-aab02054b243/31-best-practices-for-mobile-form-design.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Label should help users finish the sentence, 'I want to…' For example, if it’s a form to create an account, the call to action could be 'Create an account'. ()
		</figcaption>
	
</figure>


<h4>Don’t Use Clear Or Reset Buttons</h4>

<p>Clear or reset buttons allow users to erase their data in a form. These buttons almost never help users and often hurt them. The risk of deleting all of the information a user has entered outweighs the small benefit of having to start again. If a user fills in a form and accidentally hits the wrong button, there’s a good chance they won’t start over.</p>

<h4>Use Different Styles For Primary And Secondary Buttons</h4>

<p>Avoid secondary actions if possible. But if your form has two calls to action (for example, an e-commerce form that has “Apply discount” and “Submit order”) buttons, ensure a clear visual distinction between the primary and secondary actions. Visually prioritize the primary action by adding more visual weight to the button. This will prevent users from tapping on the wrong button.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/84a5c33c-8be5-4f8b-8fc2-fa0ccfa77d42/32-best-practices-for-mobile-form-design.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/84a5c33c-8be5-4f8b-8fc2-fa0ccfa77d42/32-best-practices-for-mobile-form-design.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/84a5c33c-8be5-4f8b-8fc2-fa0ccfa77d42/32-best-practices-for-mobile-form-design.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/84a5c33c-8be5-4f8b-8fc2-fa0ccfa77d42/32-best-practices-for-mobile-form-design.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/84a5c33c-8be5-4f8b-8fc2-fa0ccfa77d42/32-best-practices-for-mobile-form-design.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/84a5c33c-8be5-4f8b-8fc2-fa0ccfa77d42/32-best-practices-for-mobile-form-design.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/84a5c33c-8be5-4f8b-8fc2-fa0ccfa77d42/32-best-practices-for-mobile-form-design.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Ensure a clear visual distinction between primary and secondary buttons. ()
		</figcaption>
	
</figure>


<h4>Design Finger-Friendly Touch Targets</h4>

<p>Tiny touch targets create a horrible user experience because they make it challenging for users to interact with interactive objects. It’s vital to design finger-friendly touch targets: bigger input fields and buttons.</p>

<p>The image below shows that the width of the average adult finger is about 11 mm.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f347d699-dc38-480d-af4f-a9c489fb08ac/33-best-practices-for-mobile-form-design.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f347d699-dc38-480d-af4f-a9c489fb08ac/33-best-practices-for-mobile-form-design.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f347d699-dc38-480d-af4f-a9c489fb08ac/33-best-practices-for-mobile-form-design.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f347d699-dc38-480d-af4f-a9c489fb08ac/33-best-practices-for-mobile-form-design.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f347d699-dc38-480d-af4f-a9c489fb08ac/33-best-practices-for-mobile-form-design.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f347d699-dc38-480d-af4f-a9c489fb08ac/33-best-practices-for-mobile-form-design.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f347d699-dc38-480d-af4f-a9c489fb08ac/33-best-practices-for-mobile-form-design.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			People often blame themselves for having “fat fingers”. But even baby fingers are wider than most touch targets. (Image: )
		</figcaption>
	
</figure>


<p>According to , touch targets should be at least 48 &#215; 48 DP. A touch target of this size results in a physical size of about 9 mm, regardless of screen size. It might be appropriate to use larger touch targets to accommodate a wider spectrum of users.</p>

<p>Not only is target size important, but sufficient space between touch targets matters, too. The main reason to maintain a safe distance between touch targets is to prevent users from touching the wrong button and invoking the wrong action. The distance between buttons becomes extremely important when binary choices such as “Agree” and “Disagree” are located right next to each other. Material design guidelines recommend separating touch targets with 8 DP of space or more, which will create balanced information density and usability.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/00ca89fa-e66f-41bf-9b06-0f6c9232f265/34-best-practices-for-mobile-form-design.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/00ca89fa-e66f-41bf-9b06-0f6c9232f265/34-best-practices-for-mobile-form-design.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/00ca89fa-e66f-41bf-9b06-0f6c9232f265/34-best-practices-for-mobile-form-design.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/00ca89fa-e66f-41bf-9b06-0f6c9232f265/34-best-practices-for-mobile-form-design.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/00ca89fa-e66f-41bf-9b06-0f6c9232f265/34-best-practices-for-mobile-form-design.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/00ca89fa-e66f-41bf-9b06-0f6c9232f265/34-best-practices-for-mobile-form-design.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/00ca89fa-e66f-41bf-9b06-0f6c9232f265/34-best-practices-for-mobile-form-design.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<h4>Disable Buttons After Tap</h4>

<p>Forms actions commonly require some time to be processed. For example, data calculation might be required after a submission. It’s essential not only to provide feedback when an action is in progress, but also to disable the submit button to prevent users from accidentally tapping the button again. This is especially important for e-commerce websites and apps. By disabling the button, you not only prevent duplicate submissions, which can happen by accident, but you also provide a valuable acknowledgment to users (users will know that the system has received their submission).</p>

<figure>)</figcaption></figure>

<h3>Assistance And Support</h3>

<h4>Provide Success State</h4>

<p>Upon successful completion of a form, it’s critical to notify users about that. It’s possible to provide this information in the context of an existing form (for example, showing a green checkmark above the refreshed form) or to direct users to a new page that communicates that their submission has been successful.</p>

<figure>)</figcaption></figure>

<h4>Errors And Validation</h4>

<p>Users will make mistakes. It’s inevitable. It’s essential to design a user interface that supports users in those moments of failures.</p>

<p>While the topic of errors and validation deserves its own article, it’s still worth mentioning a few things that should be done to improve the user experience of mobile forms.</p>

<h5>Use Input Constraints for Each Field</h5>

<p>Prevention is better than a cure. If you’re a seasoned designer, you should be familiar with the most common cases that can lead to an error state (error-prone conditions). For example, it’s usually hard to correctly fill out a form on the first attempt, or to properly sync data when the mobile device has a poor network connection. Take these cases into account to minimize the possibility of errors. In other words, it’s better to prevent users from making errors in the first place by utilizing constraints and offering suggestions.</p>

<p>For instance, if you design a form that allows people to search for a hotel reservation, you should prevent users from selecting check-in dates that are in the past. As shown in the Booking.com example below, you can simply use a date selector that allows users only to choose today’s date or a date in the future. Such a selector would force users to pick a date range that fits.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/91815aac-3175-42ad-9f0b-9747647c579b/38-best-practices-for-mobile-form-design.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/91815aac-3175-42ad-9f0b-9747647c579b/38-best-practices-for-mobile-form-design.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/91815aac-3175-42ad-9f0b-9747647c579b/38-best-practices-for-mobile-form-design.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/91815aac-3175-42ad-9f0b-9747647c579b/38-best-practices-for-mobile-form-design.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/91815aac-3175-42ad-9f0b-9747647c579b/38-best-practices-for-mobile-form-design.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/91815aac-3175-42ad-9f0b-9747647c579b/38-best-practices-for-mobile-form-design.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/91815aac-3175-42ad-9f0b-9747647c579b/38-best-practices-for-mobile-form-design.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			You can significantly decrease the number of mistakes or incorrectly inputted data by putting constraints on what can be inputted in the field. The date picker in Booking.com’s app displays a full monthly calendar but makes past dates unavailable for selection. ()
		</figcaption>
	
</figure>


<h5>Don’t Make Data Validation Rules Too Strict</h5>

<p>While there might be cases where it’s essential to use strict validation rules, in most cases, strict validation is a sign of lazy programming. Showing errors on the screen when the user provides data in a slightly different format than expected creates unnecessary friction. And this would have a negative impact on conversions.</p>

<p>It’s very common for a few variations of an answer to a question to be possible; for example, when a form asks users to provide information about their state, and a user responds by typing their state’s abbreviation instead of the full name (for example, CA instead of California). The form should accept both formats, and it’s the developer job to convert the data into a consistent format.</p>

<h5>Clear Error Message</h5>

<p>When you write error messages, focus on minimizing the frustration users feel when they face a problem in interacting with a form. Here are a few rules on writing effective error messages:</p>

<ul>
<li><strong>Never blame the user.</strong><br />The way you deliver an error message can have a tremendous impact on how users perceive it. An error message like, “You’ve entered a wrong number” puts all of the blame on the user; as a result, the user might get frustrated and abandon the app. Write copy that sounds neutral or positive. A neutral message sounds like, “That number is incorrect.”</li>
<li><strong>Avoid vague or general error messages.</strong><br />Messages like “Something went wrong. Please, try again later” don’t say much to users. Users will wonder what <em>exactly</em> went wrong. Always try to explain the root cause of a problem. Make sure users know how to fix errors.</li>
<li><strong>Make error messages human-readable.</strong><br />Error messages like “User input error: 0x100999” are cryptic and scary. Write like a human, not like a robot. Use human language, and explain what exactly the user or system did wrong, and what exactly the user should do to fix the problem.</li>
</ul>

<h5>Display Errors Inline</h5>

<p>When it comes to displaying error messages, designers opt for one of two locations: at the top of the form or inline. The first option can make for a bad experience. Javier Bargas-Avila and Glenn Oberholzer conducted research on online form validation and  that displaying all error messages at the top of the form puts a high cognitive load on user memory. Users need to spend extra time matching error messages with the fields that require attention.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/284b9888-ce82-4eba-a91e-0abfc2fbcfff/39-best-practices-for-mobile-form-design.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/284b9888-ce82-4eba-a91e-0abfc2fbcfff/39-best-practices-for-mobile-form-design.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/284b9888-ce82-4eba-a91e-0abfc2fbcfff/39-best-practices-for-mobile-form-design.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/284b9888-ce82-4eba-a91e-0abfc2fbcfff/39-best-practices-for-mobile-form-design.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/284b9888-ce82-4eba-a91e-0abfc2fbcfff/39-best-practices-for-mobile-form-design.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/284b9888-ce82-4eba-a91e-0abfc2fbcfff/39-best-practices-for-mobile-form-design.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/284b9888-ce82-4eba-a91e-0abfc2fbcfff/39-best-practices-for-mobile-form-design.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Avoid displaying errors at the top of the form. (Image: )
		</figcaption>
	
</figure>


<p>It’s much better to position error messages inline. First, this placement corresponds with the user’s natural top-to-bottom reading flow. Secondly, the errors will appear in the context of the user’s input.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c12b046d-468b-4556-9ac8-4122321e61b9/40-best-practices-for-mobile-form-design.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c12b046d-468b-4556-9ac8-4122321e61b9/40-best-practices-for-mobile-form-design.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c12b046d-468b-4556-9ac8-4122321e61b9/40-best-practices-for-mobile-form-design.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c12b046d-468b-4556-9ac8-4122321e61b9/40-best-practices-for-mobile-form-design.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c12b046d-468b-4556-9ac8-4122321e61b9/40-best-practices-for-mobile-form-design.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c12b046d-468b-4556-9ac8-4122321e61b9/40-best-practices-for-mobile-form-design.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c12b046d-468b-4556-9ac8-4122321e61b9/40-best-practices-for-mobile-form-design.png"
			sizes="100vw"
			alt="eBay uses inline validation."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			eBay uses inline validation. ()
		</figcaption>
	
</figure>


<h5>Use Dynamic Validation</h5>

<p>The time at which you choose to display an error message is vital. Seeing an error message only after pressing the submit button might frustrate users. Don’t wait until users finish the form; provide feedback as data is being entered.</p>

<p>Use inline validation with real-time feedback. This validation instantly tells people whether the information they’ve typed is compatible with the form’s requirements. In 2009,  against post-submission validation and found the following results for the inline version:</p>

<ul>
<li>22% increase in success rate,</li>
<li>22% decrease in errors made,</li>
<li>31% increase in satisfaction rating,</li>
<li>42% decrease in completion times,</li>
<li>47% decrease in the number of eye fixations.</li>
</ul>

<p>But inline validation should be implemented carefully:</p>

<ul>
<li><strong>Avoid showing inline validation on focus.</strong><br />In this case, as soon as the user taps a field, they see an error message. The error appears even when the field is completely empty. When an error message is shown on focus, it might look like the form is yelling at the user before they’ve even started filling it out.</li>
<li><strong>Don’t validate after each character typed.</strong><br />This approach not only increases the number of unnecessary validation attempts, but it also frustrates users (because users will likely see error messages before they have completed the field). Ideally, inline validation messages should appear around  or after they’ve moved to the next field. This rule has a few exceptions: It’s helpful to validate inline as the user is typing when creating a password (to check whether the password meets complexity requirements), when creating a user name (to check whether a name is available) and when typing a message with a character limit.</li>
</ul>

<figure>)</figcaption></figure>

<h3>Accessibility</h3>

<p>Users of all abilities should be able to access and enjoy digital products. Designers should strive to incorporate accessibility needs as much as they can when building a product. Here are a few things you can do to make your forms more accessible.</p>

<h4>Ensure The Form Has Proper Contrast</h4>

<p>Your users will likely interact with your form outdoors. Ensure that it is easy to use both in sun glare and in low-light environments. Check the contrast ratio of fields and labels in your form. The  for body text:</p>

<ul>
<li>Small text should have a contrast ratio of at least 4.5:1 against its background.</li>
<li>Large text (at 14-point bold, 18-point regular and up) should have a contrast ratio of at least 3:1 against its background.</li>
</ul>

<p>Measuring color contrast can seem overwhelming. Fortunately, some tools make the process simple. One of them is , which helps designers to measure contrast levels.</p>

<h4>Do Not Rely On Color Alone To Communicate Status</h4>

<p>Color blindness (or color vision deficiency) affects approximately 1 in 12 men (8%) and  state, color shouldn’t be used as the only visual means of conveying information, indicating an action, prompting a response or distinguishing a visual element. Designers should use color to highlight or complement what is already visible. Support colorblind people by providing additional visual cues that help them understand the user interface.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fc399215-910e-48e7-87c9-0e87c5e13a64/42-best-practices-for-mobile-form-design.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fc399215-910e-48e7-87c9-0e87c5e13a64/42-best-practices-for-mobile-form-design.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fc399215-910e-48e7-87c9-0e87c5e13a64/42-best-practices-for-mobile-form-design.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fc399215-910e-48e7-87c9-0e87c5e13a64/42-best-practices-for-mobile-form-design.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fc399215-910e-48e7-87c9-0e87c5e13a64/42-best-practices-for-mobile-form-design.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fc399215-910e-48e7-87c9-0e87c5e13a64/42-best-practices-for-mobile-form-design.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fc399215-910e-48e7-87c9-0e87c5e13a64/42-best-practices-for-mobile-form-design.png"
			sizes="100vw"
			alt="Use icons and supportive text to show which fields are invalid. This will help colorblind people fix the problems."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Use icons and supportive text to show which fields are invalid. This will help colorblind people fix the problems. ()
		</figcaption>
	
</figure>


<h4>Allow Users To Control Font Size</h4>

<p>Allow users to increase font size to improve readability. Mobile devices and browsers include features to enable users to adjust the font size system-wide. Also, make sure that your form has allotted enough space for large font sizes.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/04e5c614-79b5-4e6e-9358-4a1d69afc30f/43-best-practices-for-mobile-form-design.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/04e5c614-79b5-4e6e-9358-4a1d69afc30f/43-best-practices-for-mobile-form-design.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/04e5c614-79b5-4e6e-9358-4a1d69afc30f/43-best-practices-for-mobile-form-design.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/04e5c614-79b5-4e6e-9358-4a1d69afc30f/43-best-practices-for-mobile-form-design.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/04e5c614-79b5-4e6e-9358-4a1d69afc30f/43-best-practices-for-mobile-form-design.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/04e5c614-79b5-4e6e-9358-4a1d69afc30f/43-best-practices-for-mobile-form-design.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/04e5c614-79b5-4e6e-9358-4a1d69afc30f/43-best-practices-for-mobile-form-design.png"
			sizes="100vw"
			alt="WhatsApp provides an option to change the font size in the app’s settings"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			WhatsApp provides an option to change the font size in the app’s settings. ()
		</figcaption>
	
</figure>


<h3>Test Your Design Decisions</h3>

<p>All points mentioned above can be considered as industry best practices. But just because something is called a “best practice” doesn’t mean it is always the optimal solution for your form. Apps and websites largely depend on the context in which they are used. Thus, it’s always essential to test your design decisions; make sure that the process of filling out a form is smooth, that the flow is not disrupted and that users can solve any problems they face along the way. Conduct usability testing sessions on a regular basis, collect all valuable data about user interactions, and learn from it.</p>

<h3>Conclusion</h3>

<p>Users can be hesitant to fill out forms. So, our goal as designers is to make the process of filling out a form as easy as possible. When designing a form, strive to create fast and frictionless interactions. Sometimes a minor change &mdash; such as properly writing an error message &mdash; can significantly increase the form’s usability.</p>

<p><em>his article is part of the UX design series sponsored by Adobe. Adobe XD tool is made for a  to stay updated and informed on the latest trends and insights for UX/UI design.</em></p>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(al, yk, il)</span>
</div>


              </article>
            </body>
          </html>
---------------
<h1 id="#title_1" >2、文章： 一年回顾：测试可编程基础设施</h1>
Matt Long
[http://www.infoq.com/cn/articles/testing-programmable-infrastructure?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/testing-programmable-infrastructure?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/testing-programmable-infrastructure/zh/smallimage/testing-programmable-infrastructure-1534535063963-1535211575125.jpg"/><p>可编程基础设施变得越来越普遍，有很多特定的领域问题让可编程基础设施的测试变得很棘手。这篇文章介绍了与之相关的测试工具和方法的演化。</p> <i>By Matt Long</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_2" >3、文章： 电商平台Shopify的技术架构演进思路</h1>
Kir Shatrov
[http://www.infoq.com/cn/articles/e-commerce-at-scale-inside-shopifys-tech-stack?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/e-commerce-at-scale-inside-shopifys-tech-stack?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/e-commerce-at-scale-inside-shopifys-tech-stack/zh/smallimage/logo+%281%29-1535279352277.jpg"/><p>Shopify是一个面向中小型企业的多渠道商务平台，帮助用户创建商店并通过线上的网店或社交媒体以及线下的POS机随时随地销售产品。Shopify为60万商家提供服务，在高峰期每秒处理8万个请求。Shopify还是超级碗、Kylie化妆品、Justin Bieber和Kanye West等名人的商品销售站点。从工程的角度来看，应对这些“闪购”是个巨大挑战，因为它们的流量是不可预测的。</p> <i>By Kir Shatrov</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_3" >4、文章： 看苏宁易购的运营保障体系如何hold住818大促</h1>
朱羿全
[http://www.infoq.com/cn/articles/suning-ops-team-on-818?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/suning-ops-team-on-818?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/suning-ops-team-on-818/zh/smallimage/BOLTS-1524870463316-1535278304832.jpg"/><p>运营质量的好坏关系着用户的体验。苏宁易购是如何保障818 大促线上服务质量的？</p> <i>By 朱羿全</i>
---------------
<h1 id="#title_4" >5、视频演讲： 敏捷开发：API网关与SCF深度结合应用</h1>
刘敏洁
[http://www.infoq.com/cn/presentations/deep-application-of-api-gateway-and-scf?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/deep-application-of-api-gateway-and-scf?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/presentations/deep-application-of-api-gateway-and-scf/zh/mediumimage/liuminjie270-1535294554976.jpg"/><p>API网关是serverless中与无服务器云函数结合最紧密的产品之一，常作为云函数的触发器与调用出口为广大使用SCF的开发者采用。与SCF一起使用时，API网关可以提供请求集成、响应集成等基于HTTP的映射，帮助用户在小程序、app、web页开发中实现快速集成。</p> <i>By 刘敏洁</i>
---------------
<h1 id="#title_5" >6、BitBucket支持Git V2，并改进了搜索功能</h1>
Andrew Morgan
[http://www.infoq.com/cn/news/2018/08/bitbucket-5.13?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/08/bitbucket-5.13?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Atlassian推出了BitBucket Server 5.13，支持Git v2，并且还改进了存储库的搜索方式。包括新的存储库标签功能，以及为某个提交查找相应拉取请求的功能。</p> <i>By Andrew Morgan</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_6" >7、Auth0转向基于AWS的单云架构</h1>
Hrishikesh Barua
[http://www.infoq.com/cn/news/2018/08/auth0-architecture-aws?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/08/auth0-architecture-aws?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Auth0是一家认证、授权和SSO服务提供商。近期，Auth0完成将自身架构从三家云提供商（即AWS、Azure和Google Cloud）转向AWS一家，这是因为它的服务越来越依赖于AWS服务。现在，Auth0的系统分布在4个AWS域中，其中服务是跨区复制的。</p> <i>By Hrishikesh Barua</i> <i> Translated by 盖磊</i>
---------------
<h1 id="#title_7" >8、专访美图林添毅：用 DPos 共识改造以太坊，工程型人才转型区块链开发中的探索</h1>
林添毅
[http://www.infoq.com/cn/news/2018/08/meitu-DirectorLin-DPos-Ethereum?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/08/meitu-DirectorLin-DPos-Ethereum?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>美图公司成立于2008年，公司开发的影像类产品如美图秀秀、美颜相机等覆盖了全球十亿多的独立移动终端，在海内外的总用户过亿。 在拥有海量用户海量数据的情况下，美图希望连接数字世界和真实世界。如何在保护好用户隐私的条件下，能更好的利用这些大数据信息？他们借助了当下大热的区块链技术。并于今年初发布了区块链白皮书，阐述了美图的区块链应用方案：基于沉淀多年的人脸影像技术和AI算法，在区块链平台上为用户创建一个专属的美图智能通行证（MIP），使得用户能够在区块链上用人脸特征作为通证密钥，进行去中心化用户身份验证（KYC）美图结合自身的业务，更多的是面向C端用户，考虑兼顾安全又能融入各DApp的应用场景，更需要底层基础平台的基石力量支持。 对于区块链，作为一位技术人，美图技术经理林添毅，有一些深刻的思考值得和大家分享。</p> <i>By 林添毅</i>
---------------
<h1 id="#title_8" >9、你真了解实时大数据？高手们如何玩转开源流计算？</h1>
曹倩芸
[http://www.infoq.com/cn/news/2018/08/open-source-flow-computing?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/08/open-source-flow-computing?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>9月，一场热闹非凡的技术盛宴——2018实时大数据Meetup要来啦！</p> <i>By 曹倩芸</i>
---------------
<h1 id="#title_9" >10、Kubernetes，原来可以如此简单</h1>
极客时间
[http://www.infoq.com/cn/news/2018/08/Kubernetes-so-easy?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/08/Kubernetes-so-easy?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>不管你是否意识到，在过去的几年时间里，以Docker、Kubernetes为代表的容器技术已经悄然发展成为一项通用技术。放眼国外，Google、Microsoft、IBM等互联网巨头们，仍在容器开源基础设施的技术市场上厮杀。回看国内，包括BAT、滴滴、京东、头条在内的大厂也都争相把容器和Kubernetes项目作为其技术重心，试图“放长线钓大鱼”。</p> <i>By 极客时间</i>
---------------