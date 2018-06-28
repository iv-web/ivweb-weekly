## 文章索引
1、 <a href="#1everything-you-need-to-know-about-transactional-email-but-didnt-know-to-ask" >Everything You Need To Know About Transactional Email But Didn’t Know To Ask</a><br/>
2、 <a href="#2文章-2018年的区块链就像2009年的nosql" >文章： 2018年的区块链就像2009年的NoSQL</a><br/>
3、 <a href="#3文章-央视在世界杯高清直播中占了c位-它是怎么做到的" >文章： 央视在世界杯高清直播中占了C位 它是怎么做到的？</a><br/>
4、 <a href="#4文章-istio以及service-mesh的未来" >文章： Istio以及Service Mesh的未来</a><br/>
5、 <a href="#5以太坊推出casper的第一个版本客户端测试开始" >以太坊推出Casper的第一个版本，客户端测试开始</a><br/>
6、 <a href="#6甲骨文解散java-mission-control团队事件新进展" >甲骨文解散Java Mission Control团队事件新进展</a><br/>
7、 <a href="#7基于clang的缓存型c++编译器zapcc开源" >基于Clang的缓存型C++编译器Zapcc开源</a><br/>
8、 <a href="#8java值类型的当前状态" >Java值类型的当前状态</a><br/>
9、 <a href="#9文章-李飞飞团队最新提出opentag模型减少人工标注自动提取产品属性值" >文章： 李飞飞团队最新提出OpenTag模型：减少人工标注，自动提取产品属性值</a><br/>
10、 <a href="#10文章-c#-8中的默认接口方法" >文章： C# 8中的默认接口方法</a><br/><h1 id="#title_0" >1、Everything You Need To Know About Transactional Email But Didn’t Know To Ask</h1>
Garrett Dimon
[https://www.smashingmagazine.com/2018/06/guide-transactional-email/](https://www.smashingmagazine.com/2018/06/guide-transactional-email/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/06/guide-transactional-email/" />
              <title>Everything You Need To Know About Transactional Email But Didn’t Know To Ask</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>Everything You Need To Know About Transactional Email But Didn’t Know To Ask</h1>
                  
                    
                    <address>Garrett Dimon</address>
                  
                  <time datetime="2018-06-27T12:30:49&#43;02:00" class="op-published">2018-06-27T12:30:49+02:00</time>
                  <time datetime="2018-06-27T17:44:43&#43;00:00" class="op-modified">2018-06-27T17:44:43+00:00</time>
                </header>
                

<p>Any application with user-authentication can’t exist without email, yet, email doesn’t always get the attention it deserves. With modern email service providers, it’s easier than ever to create a first-class transactional email experience for your users, but, for most of us, the challenge lies in the fact that you don’t know what you don’t know. We’re going to dive into an end-to-end analysis of everything you need to bring your transactional email up-to-snuff with the rest of your web application.</p>

<p>We’ll address the difference between transactional and bulk emails and how and why to use email authentication. We’ll also talk about handling delivery edge cases gracefully, crafting great email content, and the key pieces of infrastructure you’ll want in place for sending email and monitoring delivery. Then you’ll be well on your way to being a transactional email pro in no time.</p>

<h3 id="the-challenges-of-transactional-email">The Challenges Of Transactional Email</h3>

<p>To some degree, email has traditionally been a second-class citizen because it’s more difficult to monitor and understand how well you’re doing. With your application, there are countless performance monitoring tools to provide insights into front-end, back-end, database, errors, and much more. With email, the tools are less well-known and a little more difficult to use effectively. So let’s explore some of the challenges facing email monitoring and reporting, and then we can look at the available tools and tactics that can work within the challenges and constraints to give you a more informed view of your transactional email.</p>



  <aside class="product-panel product-panel__tilted product-panel--book" data-audience="non-subscriber">
    <div class="container product-panel--book__container">
      <div class="panel__description panel__description--book">
    <p>Getting the process <em>just</em> right ain't an easy task. That's why we've set up <strong>'this-is-how-I-work'-sessions</strong> — with smart cookies sharing what works really well for them. A part of the , of course.</p>
      <a href="http://smashed.by/casestudypanelmembership" class="btn btn--green btn--large">
        Explore features&nbsp;→
      </a>
      </div>
      <div class="panel__image panel__image--book">
        <a href="http://smashed.by/casestudypanelmembership" class="books__book__image">
        <div class="books__book__img">
          <img src="https://www.smashingmagazine.com/images/smashing-cat/cat-scubadiving-panel.svg" alt="Smashing TV, with live sessions for professional designers and developers." width="310" height="400">
        </div>
      </a>
      </div>
    </div>
  </aside>




<p>The biggest underlying challenge with monitoring email is that it’s literally impossible to log in to every recipient’s inbox and check to see if they received the email. So right out off the gate, the best insights we can hope for are simply proxies or estimations of performance. The second biggest challenge is that every ISP plays by their own rules. What might get classified as spam by Outlook could go straight to the inbox in Gmail. And inbox providers can’t share their “secret sauce” because it would immediately be exploited by spammers. So what’s a developer to do?</p>

<p>Open rates can give you a rough approximation, but since they rely on tracking pixels, which can easily be blocked, it’s an incomplete picture. Inbox rates and delivery speeds can’t be directly measured either. So you’d have to settle for sending regular tests to seed accounts that you have the ability to test. These aren’t perfect, but it’s the best available proxy for understanding delivery to the various inbox providers. We’ll address tools help automate this later in the guide.</p>

<p>Adding domain authentication in the form of DKIM, SPF, and DMARC can be difficult and confusing, or, depending on the size of your company, getting access or approval for DNS changes can be cumbersome or impossible. Even then, it’s incredibly easy to get the DNS entries incorrect. If you’re not familiar with domain authentication, don’t worry, we’ll address it in-depth later.</p>

<p>Of course, even if you’re generally able to achieve great delivery, bounce handling introduces more variability to delivery. Recipient’s inboxes may be full. People change jobs, and email addresses become inactive. People make typos with email addresses. People may sign up with a group alias, and then one of the addresses in that group bounces. Temporary server or DNS outages can affect delivery for everybody on a given domain. And then there are spam complaints.</p>

<p>So right out of the gate, the deck is stacked against you. There are plentiful edge cases, and it’s incredibly difficult to get an accurate picture of delivery. Ongoing monitoring is complex, and there’s a lot of room to make mistakes. It paints a gloomy picture, I know. Fortunately, email has come a long way, and while it’s not trivial, there are good solutions to all of these problems.</p>

<h3 id="transactional-vs-bulk-promotional">Transactional vs. Bulk Promotional</h3>

<p>Before we go further, we need to address the significant differences between bulk promotional email and your application’s transactional email. With the former, if an email is lost or delayed, nobody is going to miss it. With the latter, however, a missing or significantly delayed password reset can lead to additional support requests. Your transactional emails are as critical as a page in your application. You can think of a missing or delayed email as being roughly equivalent to a broken page in your web application. Email is a different medium, but it is still a central piece of the experience of using your application.</p>

<p>Because people expect and want to receive transactional emails, they see higher engagement in terms of open and click rates than your bulk promotional email. Similarly, transactional emails will be reported as spam much less frequently than bulk emails. And all of that leads to a better reputation for your transactional email than the bulk promotional emails. In some cases, that could be the difference between the inbox and spam folder. Or, it may just be a matter of which tab Gmail puts the email in. Regardless, the differences between transactional and bulk are stark enough that even . That way, your bulk reputation won’t drag down your transactional reputation.</p>

<p>This brings us to our first tip:</p>

<h5 id="1-separate-your-transactional-and-bulk-sending-streams-using-different-domains-or-subdomains">1. Separate your transactional and bulk sending streams using different domains or subdomains</h5>

<p>In a perfect world, you’d send transactional through your primary domain, and relegate bulk to a subdomain like <code>something@marketing.example.com</code> and each category would have its own IP addresses as well.</p>

<p>Separating your streams is the first step and critical to lay the ground work for the best possible email experience for your recipients. While you can’t guarantee delivery to the inbox, you can do a few things to stack the deck in your favor. Authentication is the next step to doing precisely that. Just like you wouldn’t launch a modern web application without a secure certificate, you don’t want to send email without fully authenticating it.</p>

<h3 id="email-authentication">Email Authentication</h3>

<p>You may have heard acronyms like , and you may have even copied and pasted some DNS entries to set these up. Or you may have skipped it because it felt a little too complex. Either way, these are all standards worth implementing, and they all complement each other and work together to build and protect your reputation. The exact approach to these will vary from provider to provider, but it’s always worth implementing.</p>

<p>Let’s start with DKIM. Without getting too much into the technical details, DKIM does two things. First, it acts as a sort of virtual wax seal on your emails to show that they haven’t been modified in transit. Second, it enables you to build domain reputation.  While DKIM focuses on the domain, SPF focuses on providing a list of approved IP addresses for sending so that receiving mail servers have a better idea of whether an email is being sent from a legitimate source.</p>

<p>One significant benefit of DKIM is that it’s the key to avoiding “via” labels in Gmail or “on behalf of” labels in Outlook. These elements make your emails look a little more likely to be spam and can undermine the trust of your recipients. So DKIM is much more than a behind-the-scenes standard. It’s something that can directly affect the experience of your recipients.</p>

<p>That all brings us to the next foundational tip:</p>

<h5 id="2-authenticate-emails-with-dkim-and-spf">2. Authenticate emails with DKIM and SPF</h5>

<p>While authentication can’t guarantee delivery, it’s a key facet of building a reputation and doing everything you can to ensure great delivery.</p>

<p>DMARC is designed to help protect against phishing attacks. It incorporates both DKIM and SPF to help you monitor sending for your domain and protect your domain reputation by enabling you to publish a DMARC policy. That policy tells inbox providers what to do when an email fails DMARC alignment.</p>

<p>Before DMARC, it was entirely up to inbox providers to choose how to handle emails that weren’t authenticated with DKIM and/or SPF, but with DMARC, you’re able to create a public policy that tells providers to quarantine (send to the spam folder) or reject (outright discard) emails that fail DMARC alignment.</p>

<p>The other benefit of DMARC is that it enables ISPs to deliver reports to you about the sources of email sent using your domain and the quantities that passed for failed alignment via DKIM or return-path. This can enable you to track down legitimate sources that are failing alignment and take action to ensure those sources are authenticated. It can also help you quantify the amount of illegitimate email that’s attempting to be sent using your domain.</p>

<p>PayPal is the quintessential example of the importance of a good DMARC policy. Over the years, countless scammers tried to spoof PayPal emails, but now, with DMARC, PayPal has a published DMARC policy telling ISP’s to reject emails that don’t pass DMARC. So if any scammers try to spoof a PayPal email, they’ll fail DMARC alignment, and the ISPs can be confident in fully rejecting those emails because PayPal has a public policy saying that if an email fails alignment, it should be rejected.</p>

<p>That’s a very brief overview of DMARC, but hopefully it helps provide the context for our third tip:</p>

<h5 id="3-establish-and-publish-a-dmarc-policy">3. Establish and publish a DMARC policy</h5>

<p>Also, if possible, set up a custom return-path to maximize your chance of alignment. Then, monitor your DMARC reports and make adjustments to ensure alignment for any legitimate sources of email. Finally, if your product or brand is the target of a high quantity of phishing attacks, begin phasing in a progressively more aggressive quarantine or reject policy over time.</p>

<p>Postmark’s  is a free and easy way to establish a DMARC policy and begin receiving weekly reports about your domain. With your bulk and transactional email streams separated, and all of the afore-mentioned authentication set up, you’ve handled all of the foundational aspects of delivery. From here on out, we’ll focus on the email handling and treatment within your application.</p>

<div id="sponsors-leaderboard-place"></div>


<h3 id="understand-the-email-lifecycle">Understand The Email Lifecycle</h3>

<p>On the surface, email can sound pretty simple, but when you break down the email lifecycle, there’s a lot of subtlety and opportunity below the surface. The better you understand that, the more you’re able to provide a more nuanced and rich experience for recipients. Most of your opportunities to improve the email experience depending on understanding the nuances of email delivery and automating your application’s ability to process and handle them accordingly. So let’s look at the key events in the life of any email.</p>

<h4 id="queued">Queued</h4>

<p>Once your application has assembled an email from the various bits of content, you’ll queue it up for delivery.  Within your application, you’ll want to ensure that you’re sending email via background processing. We’ll discuss this in depth later, but the simple version is that any time your application communicates with a 3rd party service, you’ll want to handle that communication in the background. Assuming you’re using an email service provider, once you’ve made the request to their API, it will be queued for sending on their end as well.</p>

<h4 id="sent">Sent</h4>

<p>Like any service, your email service provider will have their own queue for processing and sending your email. In most cases, these queues are extremely fast. Whereas sending a bulk email to thousands of recipients can take seconds or minutes, most transactional email will be sent much faster.</p>

<h4 id="accepted">Accepted</h4>

<p>After the email is sent by your email provider, it will ideally be accepted by the inbox provider. However, “Accepted” does not mean “Delivered.” Think of it like the postal service. Just because it has your letter, it still has to process it before it is considered delivered. Also, some inbox providers will accept an email but not ultimately deliver it for a variety of reasons. So even when an email has been accepted, there’s no guarantee that it will eventually be delivered.</p>

<h4 id="rejected">Rejected</h4>

<p>While some inbox providers will quietly reject emails, in most cases, when emails are rejected, it’s done explicitly, and you’ll receive an explanation of the problem with the email. In some cases, it may be IP or domain reputation, or it may be the content of the email. Unfortunately, you won’t always get a clear explanation of the reason for rejection.</p>

<h4 id="bounced">Bounced</h4>

<p>Bounces are a more specific type of rejection. In cases where an email address doesn’t exist, the inbox is full, or some other reasons, mail services will report back that delivery failed and the email bounced. In these cases, you can use your ESP’s bounce handling notifications to proactively take steps to correct the problem. We’ll discuss that in more detail later.</p>

<h4 id="delivered">Delivered</h4>

<p>Delivered is the state where the message has been given to the recipient. It may have been delivered to the inbox, spam folder, or one of Gmail’s tabs, but it has been delivered to some degree. You won’t ever receive an explicit notification that an email has been delivered, but it’s a key state in the lifecycle.</p>

<h4 id="opened-clicked">Opened/Clicked</h4>

<p>Open tracking isn’t entirely reliable because the method used to determine when an email has been opened can be blocked by the email client. Since open tracking relies on the email client to load an invisible image, clients that block image loading mean that those opens won’t be reported. Open rates can serve as a good proxy for delivery. For instance, if you switch email service providers without changing anything about your emails, and your open rates jump significantly, it’s safe to assume that your first email service provider was failing to deliver some portion of messages.</p>

<p>Click tracking is more reliable than open tracking, but it can bring complexities of its own. For instance, using Bit.ly or other URL shortening services is a common tactic used by spammers, so in most cases, the presence of a Bit.ly URL will put your email on the fast track to the spam folder. However, when done well through your email service provider’s click tracking, it can provide useful insights for your emails. Also, even if open tracking is blocked by a client, if someone clicks on an email, it’s safe to assume that the email was opened. So click tracking can help provide more accurate insights on open rates as well.</p>

<p>With open and click tracking, it’s important to give some consideration to privacy. While they can be powerful tools for enriching your recipient’s experience and providing you insights that can be used to improve your emails, they also touch on privacy issues. If you’re not going do anything with the data they provide, you’re better off not using them. Or, if you’re in an industry where privacy is highly sensitive, you’d probably want to think twice before enabling them.</p>

<h4 id="unsubscribed">Unsubscribed</h4>

<p>While unsubscribes are less relevant for transactional emails, it’s still a request that should be respected. While you may not be legally obligated to support unsubscribing from transactional emails, it’s a status you may encounter, and when you do, you should respect it.</p>

<h4 id="spam-complaint">Spam Complaint</h4>

<p>Like unsubscribes, spam complaints are less frequent with transactional email, but they still happen. If your spam complaint rate is high, it’s a good sign that you need to adjust the quantity and/or quality of the transactional emails you’re sending. Like bounce handling, you’ll want to be proactive about spam complaints as well. You’ll want to respect them, but it’s important to remember that some spam complaints are accidental. If someone reports an email as spam, it could affect them receiving future bills or invoices.</p>

<p>This brings us to our fourth tip:</p>

<h5 id="4-closely-integrate-message-events-into-your-application">4. Closely integrate message events into your application</h5>

<p>Most email service providers offer extensive web hooks to automatically notify your application about key events with each message. While bounce handling is the most critical event to track and handle, the other events can provide useful information to enrich your application and make transactional email a more seamlessly integrated element of your user experience.</p>

<h3 id="take-care-with-email-content">Take Care With Email Content</h3>

<p>The content of your emails can play a role in both delivery and engagement. While some rules (such as avoiding the word “Viagra”) may be obvious, others are more subtle. Taking care to craft good content can drastically improve open rates or engagement.</p>

<p>We’ll group several considerations into our fifth tip for great transactional emails:</p>

<h5 id="5-take-time-to-craft-the-content-and-structure-of-your-emails">5. Take time to craft the content and structure of your emails</h5>

<p>Things like the sender name and email address, the subject, preheaders, and mime types can have a meaningful impact on engagement, delivery, and open rates. Don’t let these elements be afterthoughts. Make time to get them right and continuously test and improve them as if they were any other page in your application.</p>

<h4 id="senders-subjects-and-preheaders">Senders, Subjects, And Preheaders</h4>

<p>While every email client is different, they all provide some level of insight about an email before it’s opened through some sort of preview. That can be as simple as displaying the sender and the subject, but it also sometimes contains a preview of the content. This topic could justify an article unto itself, but suffice it to say that it’s worthy of spending some time viewing your emails the way your recipients will. This includes clearly naming the sender, writing a useful and concise subject line, and crafting the perfect . Don’t let these elements be an afterthought because they can have a significant impact on your open rate.</p>

<h4 id="html-and-plain-text">HTML And Plain Text</h4>

<p>The actual content of your emails is important, and including both HTML and plain text versions of your emails can have a huge impact on your recipients. Some people prefer plain text. Whether for performance, privacy, or accessibility, providing a well-formatted and considered plain text option is a win for that recipient. And some spam filters prefer to see a plain text version paired with an HTML version. Litmus has a great writeup on  for more details.</p>

<h4 id="accept-replies-and-avoid-no-reply-addresses">Accept Replies And Avoid “No-Reply” Addresses</h4>

<p>Do what you can to avoid using “no-reply” email addresses. They send the wrong signal in every way possible. As a result, you’ll receive more spam complaints since people can’t reply to unsubscribe. It’s one-way communication and reduces engagement that could otherwise improve deliverability.</p>

<p>Ideally, the from address or reply-to address would send replies to a monitored support inbox. This provides the best experience for recipients and ensures that replies don’t get lost in the mix. However, there’s one main consideration to keep in mind. If a user receives a password reset URL and replies, anybody with access to the reply will also have access to that password reset URL. The same goes for any particularly sensitive information, but, all things considered, you don’t want to send highly sensitive information in email anyways.</p>

<p>Another option is to use inbound receiving email addresses. In the case of things like comment notifications where it might be useful for the recipient to respond directly to the email, setting up inbound email processing can give you the ability to avoid no-reply email addresses.</p>

<p>Regardless of the method, you should always do your best to avoid no-reply addresses. Your customers will appreciate it, and you’ll be much more likely to receive important feedback if you’re listening on all channels.</p>

<h3 id="handle-email-with-care">Handle Email With Care</h3>

<p>The content of your email is important, but how you deliver it and respond to edge cases with delivery can be just as important. There’s a lot that happens (or can happen) with each and every email you send. While most conversations with email focus simply on sending it, <em>how</em> you send it can be just as important.</p>

<p>We’ll group this batch into the sixth high-level tip for great transactional email delivery:</p>

<h5 id="6-invest-in-the-infrastructure-to-send-and-deliver-emails-reliably">6. Invest in the infrastructure to send and deliver emails reliably</h5>

<p>Sending emails sounds simple, but there’s a lot more to it than writing a few lines of code. It’s important to build and maintain the proper infrastructure like background processing and bounce handling to ensure the highest possible reliability for your email.</p>

<h4 id="background-processing">Background Processing</h4>

<p>Assuming you’re using an email service provider, you’ll want to ensure that all of your email sending happens via background processes. This is the case with any communication with any external services, and there are a few reasons. First and foremost, with an external service, there’s always the possibility that it’s down. So if the request fails, it’s important to be able to retry the request automatically after a set period of time. Alternatively, there could be a problem with the request, or something may have changed on the part of the external service. Regardless of the reason, designing resiliency into your email sending will save you some grief at some point.</p>

<p>Similarly, a good background processing setup can make it easier to be alerted to and troubleshoot issues when something does go wrong. If you set up alerts when a queue runs high, you’ll know more quickly when there’s a problem. Also, assuming your background processing is capturing and logging errors, you’ll have a much easier time identifying the source of the issue.</p>

<h4 id="understand-dedicated-ips">Understand Dedicated IPs</h4>

<p>If you’ve looked into transactional email to any degree, you’ve likely encountered the concept of using a dedicated IP address. While there are benefits to using a dedicated IP address, it’s not a black and white issue. In some cases, a dedicated IP address can hurt more than it helps.</p>

<p>With almost every email service provider, you have two options for sending. The first option is to send from the shared IP pool. In these cases, your delivery can be affected by the behavior of other senders using that same IP address. If those senders are nefarious, it can drag down the IP address’s reputation. However, if those senders are good, it can lift the IP address’s reputation.</p>

<p>The second option is a dedicated IP address. With a dedicated IP address, if there are reputation issues with the IP address, you only have yourself to blame. The catch is that, in order for a dedicated IP address to work well, you have to have a consistent daily volume that’s high enough to build and maintain a reputation. That’s somewhere around 10,000-20,000 emails per day. You also have to be careful to slowly warm up the IP address by sending progressively more mail consistently over a set period of time. And, while there are no bad senders to drag your reputation down, it also doesn’t receive any benefit from good senders who could help buoy your IP reputation. With most email service providers, dedicated IP addresses cost more as well.</p>

<p>Finally, while IP reputation still plays a role, inbox providers are increasingly weighting domain reputation in conjunction with IP reputation. Since IP addresses are increasingly disposable, putting more reputation on domains helps mitigate spammers cycling through domains because new domains would have to build reputation. This also means that if you’re having widespread delivery issues, those problems could be attributable to either the IP address or your domain. So swapping IP addresses may help, but if your domain reputation is suffering, changing the IP address won’t help. You’d instead have to focus on cleaning up your domain reputation.</p>

<p>While dedicated IP addresses can be great under the right circumstances, it’s not a slam dunk. And, if you’re using a shared IP address, you’ll want to make sure that you’re monitoring it closely to ensure that other senders aren’t ruining its reputation or landing it on blacklists.</p>

<h4 id="bounce-handling">Bounce Handling</h4>

<p>Emails bounce. There’s no way around it. The reasons for bounces vary, but the need to  is universal. Think of bounce handling as exception handling for email. When an exception happens, you don’t want it silently discarded. You want to know that it happened and what caused it so that you can fix it. The same goes for bounce handling with one caveat. With bounce handling, you can empower your users to fix most problems themselves. This simultaneously increases customer satisfaction and reduces support requests.</p>

<p>When an email bounces with a hard bounce, the most important step is to stop attempting delivery to that address. While some hard bounces may eventually start working again on their own, repeated bounces to the same address is a highly negative signal to inbox providers. From their perspective, it means you’re not keeping your lists clean and that there’s a good chance you’re a spammer.</p>

<p>Unfortunately, if you stop attempting delivery to an address, and that address begins working again, your recipients won’t be able to get their emails. That’s where bounce handling comes in. Using webhooks, your email service provider can automatically notify you of new bounces. Then, you can use that information to present alerts within your application that there were issues delivering the email. That way, your users can correct the issue, and then reactivate delivery.</p>

<p>Postmark makes this even easier with , a simple JavaScript snippet that can be customized and included in your application to proactively alert users to delivery issues so they can correct the issue before it leads to bigger problems or support requests.</p>

<h4 id="notification-management">Notification Management</h4>

<p>With transactional emails, unsubscribing is less of an issue than it is with bulk promotional emails, but providing recipients a way to unsubscribe or manage the volume or types of transactional emails they receive is still great to do.</p>

<p>One-click unsubscribes for each type of email you send can make things convenient if recipients don’t want to receive email for certain types of notifications. Alternatively, providing a preference center for transactional emails is a great way to put more control in recipients’ hands. However, if you go the preference center route, keep the options to a minimum. Keep in mind that a page with an abundance of checkboxes can be overwhelming or confusing. So while granular control is nice, too many options can be counter-productive.</p>

<p>One of the best ways to cut down on frequent notifications is to offer options such as instant, daily, or weekly summaries. That way, you give recipients significant control over notifications to enable them to drastically reduce the quantity without overwhelming them with fine-grained control for dozens of different types of notifications.</p>

<p>Regardless of the method, recognize that giving control over the frequency of notifications can go a long way to helping your customers while also helping to reduce your overall volume of emails. It’s a win-win for your customers and your email costs.</p>

<h3 id="tools-and-monitoring">Tools And Monitoring</h3>

<p>While other facets of application development have made impressive strides in tooling, best practices, and reliability, email is still somewhat of a black box. With applications, you can monitor uptime, page load times, application performance, and countless other aspects. Since email inboxes are private, however, there’s no way to accurately measure real delivery information. Open and click rates can serve as decent proxies, but they’re still only proxies. Fortunately, there are some great tools that can complement each other and, together, provide a relatively clear picture of your email delivery.</p>

<p>This is key to appreciating our seventh and final tip:</p>

<h5 id="7-use-available-tools-to-monitor-and-improve-your-delivery">7. Use available tools to monitor and improve your delivery</h5>

<p>Just like you’d monitor your application’s uptime or performance, it’s equally important to monitor email delivery. While no one tool can tell you everything, a combination fo great tools can make a huge difference in ensuring that your email delivery is reliable and help troubleshoot those times when it isn’t.</p>

<p>In order to have good coverage, you’ll want to use the following tools and pay close attention to patterns over time.</p>

<ol>
<li>Monitor trends in open and click rates for your emails. It’s only a proxy, but it’s good for relative historical numbers. For example, if you notice your open or click rates falling dramatically over time, that’s often an early warning sign that you may be encountering delivery issues. Since an email can’t be opened if it’s not delivered successfully, decreases in open rates can be caused by delivery issues.</li>
<li>Gmail offers  which can help you gauge IP and domain reputation to understand which email sources may be having delivery issues. This is a great forensic tool to turn to when you suspect that you may be having delivery issues. It only provides insight from Gmail, but that’s often a good-enough proxy for understanding how your reputation might look to the other providers as well.</li>
<li>Use the  to see if your domain or IP address has landed on a blacklist. If you’re on a shared IP address, you probably want to set up a permanent and automatic monitor for that shared IP address so you’ll know sooner if you end up on a blacklist.</li>
<li>Use a tool like  to monitor inbox placement for your emails. It’s important to keep in mind that these tools rely on seed lists to test delivery. That is, since they can’t test delivery to real recipients’ inboxes, they have to use test addresses as a proxy. Like with most email delivery tools, this isn’t a perfect science, but in practice, it’s close enough to still be very useful at gauging delivery quality.</li>
</ol>

<p>The more monitoring and alerting you have in place, the sooner you’ll know about problems and be able to correct them. Often, poor email delivery can be an invisible problem that only surfaces when support requests begin to show up, but by then, you could have already had 100’s or 1,000’s of emails end up in spam folders or not arrive at all. Just like you wouldn’t want your customers to be the ones alerting you to application downtime, you don’t want them to be the first to alert you to potential delivery issues either.</p>

<h3 id="bring-it-all-together">Bring It All Together</h3>

<p>You have plenty of options when it comes to sending email. You can even set up a server and Mail Transfer Agent (MTA) and send for yourself if you’d like, but you’ll be taking on a lot of responsibility and overhead. Managing reputation is difficult. Establishing relationships with ISP’s is even harder.</p>

<p>Unless sending email is your core service, you’re often better off turning to an email service provider. Even then, it’s important to recognize that great delivery can’t be a foregone conclusion. Even though all ESP’s claim that they provide great delivery, that’s not always the case. In most cases, when you’re evaluating ESP’s, you’ll be much better off if you use the tools mentioned above to get quantifiable delivery information for yourself rather than taking their word for it. This is true whether you use a shared IP address or a dedicated IP address. Great delivery isn’t automatic, and you should always be gathering hard data on your delivery.</p>

<p>Regardless of how you handle email, make sure to treat it as an extension of your application’s user experience rather than an afterthought. Take time to write concise and helpful emails, and do everything possible to seamlessly integrate it into the user experience. Be judicious about firing off too many emails, and give your users the ability to tune email notifications for their needs.</p>

<p>Finally, monitor your transactional email delivery like you would any other service in your stack. If your users aren’t receiving critical emails like password resets and invoices, you’ll be losing goodwill, and your support costs will increase. Don’t let your email delivery fail quietly. Make sure that you’re notified quickly and loudly of any potential delivery issues long before it gets bad enough for your customers to email you.</p>

<p>Your application can’t work without email. While it’s not as easy to measure or monitor as most aspects of your application, it’s still a critical piece of functionality that deserves your full attention. Invest the time in making your email experience great, and you’ll unquestionably reap the rewards.</p>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(ra, il)</span>
</div>


              </article>
            </body>
          </html>
---------------
<h1 id="#title_1" >2、文章： 2018年的区块链就像2009年的NoSQL</h1>
Bryan
[http://www.infoq.com/cn/articles/blockchain-2018-nosql-2009?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/blockchain-2018-nosql-2009?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/blockchain-2018-nosql-2009/zh/smallimage/logo32-1530027654378.jpg"/><p>如果有人问你“什么是NoSQL”，相信你很难回答这个问题。你可能会说，NoSQL是“一个不使用SQL的数据库”，但对于不同的人来说，这句话的含义也不一样。如果有人问你“什么是区块链”，也是一样的道理。</p> <i>By Bryan</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_2" >3、文章： 央视在世界杯高清直播中占了C位 它是怎么做到的？</h1>
李海琦
[http://www.infoq.com/cn/articles/cctv-in-world-cup?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/cctv-in-world-cup?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/cctv-in-world-cup/zh/smallimage/logo1-1530117487212.jpg"/><p>本文从极速高清的工作原理出发，详细介绍腾讯云的深度学习技术如何对世界杯直播场景进行优化，其中还有腾讯云如何在PK中胜出、如何在一周内完成央视网极速高清服务私有化部署等不为人知的故事。</p> <i>By 李海琦</i>
---------------
<h1 id="#title_3" >4、文章： Istio以及Service Mesh的未来</h1>
Jasmine Jaksic
[http://www.infoq.com/cn/articles/istio-future-service-mesh?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/istio-future-service-mesh?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/istio-future-service-mesh/zh/smallimage/Istio-Future-of-Service-Meshes-1529065924373-1529844640974.jpeg"/><p>Service Mesh 提供了一种透明的、与编程语言无关的方式，使网络配置、安全配置以及服务观察等操作能够灵活而简便地实现自动化。本文将对 Istio Service Mesh 的过去、现状以及未来进行透彻的分析。Istio 项目的近期目标是在关键的特性进入 beta 阶段后推出 1.0 版本，其中包括对于混合环境的支持。
</p> <i>By Jasmine Jaksic</i> <i> Translated by 邵思华</i>
---------------
<h1 id="#title_4" >5、以太坊推出Casper的第一个版本，客户端测试开始</h1>
Kent Weare
[http://www.infoq.com/cn/news/2018/06/Ethereum-Casper-First-Release?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/06/Ethereum-Casper-First-Release?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>在reddit最近的一篇博文中，以太坊开发者Danny Ryan宣布了Casper Friendly Finality Gadget（FFG）的第一个版本，这是以太坊的权益证明一致性算法。这个软件的发布以及验证者的引入有助于向权益证明（PoS）一致性区块链转换。</p> <i>By Kent Weare</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_5" >6、甲骨文解散Java Mission Control团队事件新进展</h1>
Kesha Williams
[http://www.infoq.com/cn/news/2018/06/new-details-jmc?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/06/new-details-jmc?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>根据前不久的报道，甲骨文在开源Java Mission Control后裁掉了整个开发团队，一位前甲骨文员工透露了一些有关事件转折的额外信息。</p> <i>By Kesha Williams</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_6" >7、基于Clang的缓存型C++编译器Zapcc开源</h1>
Sergio De Simone
[http://www.infoq.com/cn/news/2018/06/zapcc-caching-cpp-compiler-open?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/06/zapcc-caching-cpp-compiler-open?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Zapcc是一个缓存型C++编译器，基于Clang/LLVM的一个分支创建，据称重编译的速度快50倍，完整构建的速度快2到5倍。由Creemple开发，最初在2015年底发布，Zapcc现在开源了。
</p> <i>By Sergio De Simone</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_7" >8、Java值类型的当前状态</h1>
Ben Evans
[http://www.infoq.com/cn/news/2018/06/JavaValuesJun18?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/06/JavaValuesJun18?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>甲骨文正在将值类型引入到Java中，我们对目前的状态进行了更新。</p> <i>By Ben Evans</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_8" >9、文章： 李飞飞团队最新提出OpenTag模型：减少人工标注，自动提取产品属性值</h1>
马卓奇
[http://www.infoq.com/cn/articles/OpenTag-open-attribute-value-extraction?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/OpenTag-open-attribute-value-extraction?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/OpenTag-open-attribute-value-extraction/zh/smallimage/GettyImages-508140566-1529942960363.jpg"/><p>今天给大家带来的是李飞飞团队最新提出的OpenTag模型论文的解读。OpenTag是目前第一个端到端的开放式属性值提取框架，从建模、推断和学习三个方面解决了现实生活中属性值提取面临的挑战。</p> <i>By 马卓奇</i>
---------------
<h1 id="#title_9" >10、文章： C# 8中的默认接口方法</h1>
Bassam Alugili
[http://www.infoq.com/cn/articles/default-interface-methods-cs8?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/default-interface-methods-cs8?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/default-interface-methods-cs8/zh/smallimage/default-interface-methods-small-1-1528982559551-1529844086690.jpg"/><p>默认接口方法已经被包含在C# 8的新功能建议中，开发人员可以像使用trait那样使用默认方法。trait是面向对象的编程技术，用于提升不相关类之间方法的重用性。C#语言开发人员基于Java的默认方法概念开发此功能。</p> <i>By Bassam Alugili</i> <i> Translated by 无明</i>
---------------