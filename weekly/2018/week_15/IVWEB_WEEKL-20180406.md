## 文章索引
1、 <a href="#1analyzing-your-companys-social-media-presence-with-ibm-watson-and-nodejs" >Analyzing Your Company’s Social Media Presence With IBM Watson And Node.js</a><br/>
2、 <a href="#2视频演讲-分布式-kv-存储系统-cellar-演进之路" >视频演讲： 分布式 KV 存储系统 Cellar 演进之路</a><br/>
3、 <a href="#3视频演讲-深度学习在crt中的应用" >视频演讲： 深度学习在CRT中的应用</a><br/>
4、 <a href="#4the-rise-of-intelligent-conversational-ui" >The Rise Of Intelligent Conversational UI</a><br/><h1 id="#title_0" >1、Analyzing Your Company’s Social Media Presence With IBM Watson And Node.js</h1>
Jamie Munro
[https://www.smashingmagazine.com/2018/04/analyzing-social-media-presence-ibm-watson-nodejs/](https://www.smashingmagazine.com/2018/04/analyzing-social-media-presence-ibm-watson-nodejs/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/04/analyzing-social-media-presence-ibm-watson-nodejs/" />
              <title>Analyzing Your Company’s Social Media Presence With IBM Watson And Node.js</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>Analyzing Your Company’s Social Media Presence With IBM Watson And Node.js</h1>
                  
                    
                    <address>Jamie Munro</address>
                  
                  <time datetime="2018-04-04T13:00:50&#43;02:00" class="op-published">2018-04-04T13:00:50+02:00</time>
                  <time datetime="2018-04-05T20:04:51&#43;00:00" class="op-modified">2018-04-05T20:04:51+00:00</time>
                </header>
                <p>If you are unfamiliar with Machine Learning (ML) technology, it has existed in science fiction for many years and is finally reaching its maturity in our society. One of the first ML examples I saw as a kid was in Star Trek’s <em>The Next Generation</em> when Lieutenant Tasha Yar trains with her holographic opponent that learns how to fight and better defeat in future battles.
</p>

<p>In today’s society, China has developed a “” that is a guard rail controlled by a computer system that can direct the flow of traffic into different lanes, increasing safety and improving traveling time. This is done automatically based on time of day and how much traffic is flowing in each direction.
</p>

<p>Another example is  that automatically detect traffic patterns and alter the traffic lights on-the-fly. Each light is controlled independently to help reduce both the commuting time and the idling time of cars. According to the article, pilot tests have demonstrated a reduced travel time of 25% and idling time by over 40%. There are, of course, hundreds of other examples of ML technology that make intelligent decisions based on the content it consumes.
</p>

<p>To accomplish today’s goal, I am going to demonstrate (using Node.js) how to perform a search with Twitter’s API to retrieve content that will be inputted into the ML algorithm to be analyzed. This way, you’ll be provided with characteristics about the users who wrote that specific content so that you can get a better understanding of your audience. The example application will be written using Node.js as the server.</p>

<p>It is beyond the scope of this article to demonstrate how to write an ML algorithm. Instead, to aid in the analysis, I will demonstrate how to use IBM’s  to help you understand the general personality of your social media audience.
</p>

<aside class="product-panel product-panel__tilted product-panel--book">
    <div class="container product-panel--book__container">
      <div class="panel__description panel__description--book">
    <p>Getting the process <em>just</em> right ain't an easy task. That's why we've set up <strong>'this-is-how-I-work'-sessions</strong> — with smart cookies sharing what works really well for them. A part of the , of course.</p>
      <a href="https://www.smashingmagazine.com/membership/" class="btn btn--green btn--large">
        Explore features&nbsp;→
      </a>
      </div>
      <div class="panel__image panel__image--book">
        <a href="https://www.smashingmagazine.com/membership/" class="books__book__image">
        <div class="books__book__img">
          <img src="https://www.smashingmagazine.com/images/smashing-cat/cat-scubadiving-panel.svg" alt="Smashing TV, with live sessions for professional designers and developers." width="310" height="400">
        </div>
      </a>
      </div>
    </div>
  </aside>



<div class="c-garfield-the-cat">


<h3>What Is IBM Watson?</h3>

<p>In 2011, Watson began as a computer system that attempted to index the (entire) Internet. It was originally programmed to answer questions posed in ordinary English. Watson  on the TV show <em>Jeopardy!</em> claiming a $1,000,000 cash prize.</p>

<p>Watson was now a proven success.</p>

<p>With the fame of winning on <em>Jeopardy!</em>, IBM has continued to push Watson’s capabilities. Watson has evolved into an enterprise-level application that is focused on Artificial Intelligence (AI) which you can train to identify what you care about most allowing you to make smarter decisions automatically.</p>

<p>The suite of Watson’s services is divided into six high-level categories:</p>

<ol>
<li><strong>Conversation</strong><br />The services in this category allow you to build intelligent chatbot’s or a virtual customer service agent.</li>
<li><strong>Knowledge</strong><br />This category is focused on teaching Watson how to interpret data to unlock hidden value and monitor trends.</li>
<li><strong>Vision</strong><br />This service provides the ability to tag content inside an image that is used to train Watson to be able to automatically recognize the same pattern inside of other images.</li>
<li><strong>Speech</strong><br />These services provide the ability to convert speech to text and the inverse, text to speech.</li>
<li><strong>Language</strong><br />This category is split between translating one language to another as well as interpreting the text to predict what predefined category the text belongs to.</li>
<li><strong>Empathy</strong><br />This category is devoted to understanding the content’s tone, personality, and emotional state. Inside this category is a service called “Personality Insights” that will be used in this article to predict the personality characteristics with the social media content we will provide it.</li>
</ol>

<p>This article will be focusing on understanding the personality of the content that we will fetch from Twitter. However, as you can see, Watson provides many other AI features that you can explore to automate many other processes simply through training and content aggregation.</p>

<h3>Personality Insights</h3>

<p> will analyze content and help you understand the habits and preferences at an individual level and at scale. This is called the ‘personality profile.’ The profile is split into two high-level groups: <strong>Personality characteristics</strong> and <strong>Consumption preferences</strong>. These groups are further broken down into more finite components.</p>

<p><strong>Note</strong>: <em>To help understand the high-level concepts (before we deep dive into the results), the  provides this helpful summary describing how the profile is inferred from the content you provide it.</em></p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9ae384dc-90de-4dd4-967f-de0c8d605f39/personality-insights.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9ae384dc-90de-4dd4-967f-de0c8d605f39/personality-insights.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9ae384dc-90de-4dd4-967f-de0c8d605f39/personality-insights.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9ae384dc-90de-4dd4-967f-de0c8d605f39/personality-insights.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9ae384dc-90de-4dd4-967f-de0c8d605f39/personality-insights.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9ae384dc-90de-4dd4-967f-de0c8d605f39/personality-insights.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9ae384dc-90de-4dd4-967f-de0c8d605f39/personality-insights.jpg"
			sizes="100vw"
			alt="IBM Watson’s Big Five Personality Traits"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Big Five Personality Traits. Image courtesy: )
		</figcaption>
	
</figure>


<h4>Personality Characteristics</h4>

<p>The <em>Personality Insights</em> service infers personality characteristics based on three primary models:</p>

<ul>
  <li>The ‘Big Five’ personality characteristics represent the most widely used model for generally describing how a person engages with the world. The model includes five primary dimensions:</li>
  <ul>
    <li>Agreeableness</li>
    <li>Conscientiousness</li>
    <li>Extraversion</li>
    <li>Emotional range</li>
    <li>Openness<br /><strong>Note</strong>: <em>Each dimension has six facets that further characterize an individual according to the dimension.</em></li>
  </ul>
  <li>Needs describe which aspects of a product will resonate with a person. The model includes twelve characteristic needs:</li>
  <ul>
    <li>Excitement</li>
    <li>Harmony</li>
    <li>Curiosity</li>
    <li>Ideal</li>
    <li>Closeness</li>
    <li>Self-expression</li>
    <li>Liberty</li>
    <li>Love</li>
    <li>Practicality</li>
    <li>Stability</li>
    <li>Challenge</li>
    <li>Structure</li>
  </ul>
  <li>Values describe motivating factors that influence a person’s decision making. The model includes five values:</li>
  <ul>
    <li>Self-transcendence / Helping others</li>
    <li>Conservation / Tradition</li>
    <li>Hedonism / Taking pleasure in life</li>
    <li>Self-enhancement / Achieving success</li>
    <li>Open to change / Excitement</li>
  </ul>
</ul>

<p><em>For more information, see .</em></p>

<h4>Consumption preferences</h4>

<p>Based on the personality characteristics inferred from the input text, the service can also return an indication of the author’s consumption preferences. ‘Consumption preferences’ indicate the author’s likelihood to pursue different products, services, and activities. The service groups the individual preferences into eight categories:</p>

<ul>
<li>Shopping</li>
<li>Music</li>
<li>Movies</li>
<li>Reading and learning</li>
<li>Health and activity</li>
<li>Volunteering</li>
<li>Environmental concern</li>
<li>Entrepreneurship</li>
</ul>

<p>Each category contains from one to as many as a dozen individual preferences.</p>


  <div id="sponsors-article" data-impression="true" class="c-promo-box c-promo-box--ad sponsors hidden" data-audience="non-subscriber" data-remove="true"></div>



<p><strong>Note</strong>: <em>For more information, see .</em></p>

<p>To be effective, Watson requires a minimum of a hundred words to provide an insight into the consumer’s personality. The more words provided, the better Watson can analyze and determine the consumer’s preference.</p>

<p>This means, if you wish to target individuals, you will need to collect more data than one or two tweets from a specific person. However, if a user writes a product review, blog post, email, or anything else related to your company, this could be analyzed on both an individual level and at scale.</p>

<p>To begin, let’s start by setting up the Personality Insights service to begin analyzing a real-world example.</p>

<h3>Configuring The Personality Insights Service</h3>

<p>Watson is an enterprise application but they offer . IBM offers a Lite plan that is free. The Lite plan is limited to 1,000 API calls per month and is automatically deleted after 30 days &mdash; perfect for our demonstration.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a5024fb7-1c5e-4939-8f95-c6aa963c94a9/insights-service.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a5024fb7-1c5e-4939-8f95-c6aa963c94a9/insights-service.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a5024fb7-1c5e-4939-8f95-c6aa963c94a9/insights-service.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a5024fb7-1c5e-4939-8f95-c6aa963c94a9/insights-service.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a5024fb7-1c5e-4939-8f95-c6aa963c94a9/insights-service.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a5024fb7-1c5e-4939-8f95-c6aa963c94a9/insights-service.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a5024fb7-1c5e-4939-8f95-c6aa963c94a9/insights-service.jpg"
			sizes="100vw"
			alt="Create the Personality Insights Service"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Create the Personality Insights Service. ()
		</figcaption>
	
</figure>


<p>Once the service has been added, we will need to retrieve the service’s credentials to perform API calls against it. From , your service should be displayed. After you've selected the service, you'll find a link to view the Service credentials in the left-hand menu. You will need to create a new ‘Credential.’ A unique name is required and optional configuration parameters can be defaulted for this login. For now, we will leave the configuration options empty.</p>

<p>After you have created a credential, select the ‘View’ credentials link. This will display the API’s URL, your username, and password required to securely execute API calls. Save these somewhere safe as we will need them in the next step.</p>

<h3>Testing The Personality Insights Service</h3>

<p>To perform API calls, I am going to use Node.js. If you already have Node.js installed, you can move on to the next step; otherwise, follow the instructions to setup Node.js from the .</p>

<p>To demonstrate how to use the <em>Personality Insights</em>, I am going to create a new Node.js project on my computer. With a command prompt open, navigate to the directory where your Node.js projects will be stored and create your new project:</p>

<pre><code class="language-javascript">mkdir watson-sentiments
cd watson-sentiments
npm init
</code></pre>

<p>To assist with making the API calls to Watson, I am going to leverage the NPM Package: . This package can be installed via the command prompt:</p>

<pre><code class="language-bash">npm install watson-developer-cloud --save</code></pre>

<p>Before making the first call, the <em>PersonalityInsightsV3</em> object needs to be instantiated with the credentials from the previous section. Begin by creating a new file called <em>index.js</em> that will contain the Node.js code.</p>

<p>Here is an example of configuring the class so it is ready to make API calls:</p>

<pre class="break-out"><code class="language-javascript">var PersonalityInsightsV3 = require(’watson-developer-cloud/personality-insights/v3’);
var personality_insights = new PersonalityInsightsV3({
  "url": "https://gateway.watsonplatform.net/personality-insights/api",
  "username": "**************************",
  "password": "*************",
  "version_date": "2017-12-01"
});
</code></pre>

<p>The <code>personality_insights</code> variable is what we will use to interact with the API for the <em>Personality Insights</em> service. Let’s review how to execute a call and return a personality profile:</p>

<pre class="break-out"><code class="language-javascript">var fs = require(’fs’);

personality_insights.profile({
"contentItems": [
   {
         "content": "Some content that contains more than 100 words...",
         "contenttype": "text/plain",
         "created": 1447639154000,
         "id": "666073008692314113",
         "language": "en"
      }
   ],
   "consumption_preferences": true
}, (err, response) => {
if (err) throw err;

fs.writeFile("results.txt", JSON.stringify(response, null, 2), function(err) {
if (err) throw err;

console.log("Results were saved!");
});
  });
</code></pre>

<p>The <code>profile</code> function accepts an array of <code>contentItems</code>. The ‘content’ item contains the actual content with a few additional properties identifying additional information to help Watson interpret it.</p>

<p>When this is executed, the results are written to a text file (the results are too large to write in the console). The result is an object that contains the following high-level properties:</p>

<ul>
<li><code>word_count</code></li>
<li>The count of words interpreted</li>
<li><code>processed_language</code></li>
</ul>

<p>The language that the content provided, e.g. (en).</p>

<ul>
<li><strong>Personality</strong><br />This is an array of the ‘Big Five’ personality characteristics (Openness, Conscientiousness, Extraversion, Agreeableness, and Emotional range). Each characteristic contains an overall percentile for that characteristic (e.g. 0.8100175318417588). To ascertain more detail, there is an array called <code>children</code> that provides more in-depth insight. For example, a child category under ‘Openness’ is ‘Adventurousness’ that contains its own percentile.</li>
<li><strong>Needs</strong><br />This is an array of the twelve characteristics that define the aspects a person will resonate with a product (Excitement, Harmony, Curiosity, Ideal, Closeness, Self-expression, Liberty, Love, Practicality, Stability, Challenge, and Structure). Each characteristic contains a percentile of how the content was interpreted.</li>
<li><strong>Values</strong><br />This is an array of the five characteristics that describe motivating factors that influence a person’s decision making (Self-transcendence / Helping others, Conservation / Tradition, Hedonism / Taking pleasure in life, Self-enhancement / Achieving success, and Open to change / Excitement). Each characteristic contains a percentile of how the content was interpreted.</li>
<li><strong>Behavior</strong><br />This is an array that contains thirty-one elements. Each element provides a percentile of when the content was created. Seven of the elements define the days of the week (Sunday through Saturday). The remaining twenty-four elements define the hours of the day. This helps you understand when customer’s interact with your product.</li>
<li><code>consumption_preferences</code><br />This is an array that contains eight different categories with as much as a twelve child categories providing a percentile of likelihood to pursue different products, services, and activities (Shopping, Music, Movies, Reading and learning, Health and activity, Volunteering, Environmental concern, and Entrepreneurship).</li>
<li><strong>Warnings</strong><br />This is an array that provides messages if a problem was encountered interpreting the content provided.</li>
</ul>

<p>Here is a CodePen of the formatted results:</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="NXrypp"
   data-user="endyourif"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<h3>Configuring Twitter</h3>

<p>To search Twitter for relevant tweets, I am going to use the Twitter NPM package. From a console window where the application is hosted, run the following command to install:</p>

<pre><code class="language-bash">npm install twitter --save</code></pre>

<p>Before we can implement the Twitter package, you need to .</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cee7e291-da72-436a-9f3d-59653a1de389/twitter.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cee7e291-da72-436a-9f3d-59653a1de389/twitter.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cee7e291-da72-436a-9f3d-59653a1de389/twitter.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cee7e291-da72-436a-9f3d-59653a1de389/twitter.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cee7e291-da72-436a-9f3d-59653a1de389/twitter.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cee7e291-da72-436a-9f3d-59653a1de389/twitter.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cee7e291-da72-436a-9f3d-59653a1de389/twitter.jpg"
			sizes="100vw"
			alt="Retrieving Twitter’s Access Tokens"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Retrieving Twitter’s Access Tokens. ()
		</figcaption>
	
</figure>


<p>Once you’ve created your application, you need to retrieve the authorization keys required to perform API calls. With your application created, navigate to the ‘Keys’ and ‘Access Tokens’ page. Since we are not performing API calls against users of Twitter, OAuth integration is not required. Instead, we need only the four following keys:</p>

<ol>
<li>Consumer Key</li>
<li>Consumer Secret</li>
<li>Access Token</li>
<li>Access Token Secret</li>
</ol>

<p>The last two keys need to be generated near the bottom of the ‘Keys’ and ‘Access Tokens’ page. With the keys, here is an example of searching for Tweets about #SmashingMagazine:</p>

<pre class="break-out"><code class="language-javascript">var Twitter = require(’twitter’);

var client = new Twitter({
  consumer_key: ’*********************’,
  consumer_secret: ’******************’,
  access_token_key: ’******************’,
  access_token_secret: ’****************’
});

client.get(’search/tweets’, { q: ’#SmashingMagazine’ }, function(error, tweets, response) {
if(error) throw error;

console.log(tweets);
});
</code></pre>

<p>The result of this code will log a list tweets about Smashing Magazine. For the purposes of this demonstration, the following fields are of interest to us:</p>

<ol>
<li><code>id</code></li>
<li><code>created_at</code></li>
<li><code>text</code></li>
<li><code>metadata.iso_language_code</code></li>
</ol>

<p>These are the fields we will feed Watson.</p>

<h3>Integrating Personality Insights With Twitter</h3>

<p>With Twitter setup and Watson setup, it’s time to integrate the two together and see the results. To make it interesting, let’s search for <code>#DonaldTrump</code> to see what the world thinks about the President of the United States. Here is the code example to search Twitter, feed the results into Watson, and write the results to a text file:</p>

<pre class="break-out"><code class="language-javascript">var fs = require(’fs’);
var Twitter = require(’twitter’);

var client = new Twitter({
  consumer_key: ’*********************’,
  consumer_secret: ’******************’,
  access_token_key: ’******************’,
  access_token_secret: ’****************’
});

var PersonalityInsightsV3 = require(’watson-developer-cloud/personality-insights/v3’);
var personality_insights = new PersonalityInsightsV3({
  "url": "https://gateway.watsonplatform.net/personality-insights/api",
  "username": "**************************",
  "password": "*************",
  "version_date": "2017-12-01"
});

client.get(’search/tweets’, { q: ’#DonaldTrump’ }, function(error, tweets, response) {
if(error) throw error;

var contentItems = [];

// Loop through the tweets
for (var i = 0; i < tweets.statuses.length; i++) {
var tweet = tweets.statuses[i];

contentItems.push({
"content": tweet.text,
"contenttype": "text/plain",
"created": new Date(tweet.created_at).getTime(),
"id": tweet.id,
"language": tweet.metadata.iso_language_code
});
}

// Call Watson with the tweets
personality_insights.profile({
"contentItems": contentItems,
"consumption_preferences": true
}, (err, response) => {
if (err) throw err;

// Write the results to a file
fs.writeFile("results.txt", JSON.stringify(response, null, 2), function(err) {
if (err) throw err;

console.log("Results were saved!");
});
});
});
</code></pre>

<p>Here is another CodePen of the formatted results that I received:</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="ppPyRM"
   data-user="endyourif"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<h3>What Do The Results Say?</h3>

<p>Once we’ve analyzed the ‘Openness’ trait of the ‘Big Five,’ we can infer the following:</p>

<ul>
<li>Emotion is quite low at 13%</li>
<li>Imagination is average at 54%</li>
<li>Intellect is very high at 96%</li>
<li>Authority challenging is also quite high at 87%</li>
</ul>

<p>The ‘Conscientiousness’ trait at a high-level is average at 46% compared with the ‘Openness’ high-level average of 88%. Whereas ‘Agreeableness’ is very low at only 25%. I guess people on Twitter don’t like to agree with Donald Trump.</p>

<p>Moving on to the ‘Needs.’ The sub-categories of ‘Curiosity’ and ‘Structure’ are in the 60 percentile compared to other categories being below the 10th percentile (Excitement, Harmony, etc.).</p>

<p>And finally, under ‘Values,’ the sub-category that stands out to me as interesting is the ‘Openness’ to ‘Change’ at an abysmal 6%.</p>

<p>Based on when you perform your search, your results may vary as the results are limited to the past seven days from executing the example.</p>

<p>From these results, I would determine that the average person who tweets about Donald Trump is quite intellectual, challenges authority, and is not open to change.</p>

<p>With these results, it would allow you to automatically alter how you would target your content towards your audience to match the results received. You will need to determine what categories are of interest and what percentiles do you wish to target. With this ammunition, you can begin automating.</p>

<h3>What Else Can I Do With Watson?</h3>

<p>As I mentioned at the beginning of this article, Watson offers many other different services. With these services, you could automate many different parts of common business processes. For example:</p>

<ul>
<li>Building a chat bot that can intelligently answer questions based on a knowledge base of information;</li>
<li>Build an application where you dictate what you want written to Watson by using the speech to text functionality;</li>
<li>Automatically translate your content into different languages to create a multi-lingual site or knowledge base;</li>
<li>Teach Watson how to look for specific patterns in images. This could be used to determine if a logo is embedded into a photo.</li>
</ul>

<p>This, of course, is a very small subset that my limited imagination can postulate. I’m sure you can think of many other ways to leverage Watson’s immense capabilities.</p>

<p>If you are looking for more examples, IBM has an entire GitHub repository dedicated to their . The example folder contains over ten sample applications that convert speech to text, text to speech, tone analysis, and visual recognition to name just a few.</p>

<h3>Conclusion</h3>

<p>Before Watson can runaway with technological growth, resulting in the singularity where Artificial Intelligence destroys mankind, this article demonstrated how you can turn social media content into a powerful understanding of how the people creating the content think. Using the results from Watson, your application can use the categories of interest where the percentile exceeds or is less than a predetermined amount to change how you target your audience.</p>

<p>If you have other interesting uses of Watson or how you are using the <em>Personality Insights</em>, be sure to leave a comment below.
</p>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(rb, ra, yk, il)</span>
</div>



  <div id="sponsors-article-end" data-impression="true" class="c-promo-box c-promo-box--ad c-promo-box--wide sponsors hidden" data-audience="non-subscriber" data-remove="true"></div>



</div>



              </article>
            </body>
          </html>
---------------
<h1 id="#title_1" >2、视频演讲： 分布式 KV 存储系统 Cellar 演进之路</h1>
齐泽斌
[http://www.infoq.com/cn/presentations/the-path-of-evolution-of-the-distributed-kv-storage-system-cellar?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/the-path-of-evolution-of-the-distributed-kv-storage-system-cellar?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/presentations/the-path-of-evolution-of-the-distributed-kv-storage-system-cellar/zh/mediumimage/qizebin270-1521958902036.jpg"/><p>互联网服务的典型特征是流量大、全年无休。作为互联网服务的最底层系统分布式存储，其性能和可用性的要求会更高。本次演讲将分享美团点评新一代 KV 存储系统 Cellar 在支撑快速增长的业务的同时，是如何演进其架构，以不断提升其可用性和性能，支撑每日万亿级的访问量。</p> <i>By 齐泽斌</i>
---------------
<h1 id="#title_2" >3、视频演讲： 深度学习在CRT中的应用</h1>
张俊林
[http://www.infoq.com/cn/presentations/the-application-of-deep-learning-in-crt?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/the-application-of-deep-learning-in-crt?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/presentations/the-application-of-deep-learning-in-crt/zh/mediumimage/zhangjunlin270-1521463164779.jpg"/><p>此次视频主要分享的内容为：当深度学习遇到CTR预估；传统主流CTR预估方法深度学习基础模型；深度学习CTR预估模型；互联网公司深度学习CTR案例。</p> <i>By 张俊林</i>
---------------
<h1 id="#title_3" >4、The Rise Of Intelligent Conversational UI</h1>
Burke Holland
[https://www.smashingmagazine.com/2018/04/rise-intelligent-conversational-ui/](https://www.smashingmagazine.com/2018/04/rise-intelligent-conversational-ui/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/04/rise-intelligent-conversational-ui/" />
              <title>The Rise Of Intelligent Conversational UI</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>The Rise Of Intelligent Conversational UI</h1>
                  
                    
                    <address>Burke Holland</address>
                  
                  <time datetime="2018-04-05T13:00:48&#43;02:00" class="op-published">2018-04-05T13:00:48+02:00</time>
                  <time datetime="2018-04-05T20:04:51&#43;00:00" class="op-modified">2018-04-05T20:04:51+00:00</time>
                </header>
                

<p>For a long time, we’ve thought of interfaces strictly in a visual sense: buttons, dropdown lists, sliders, carousels (please no more carousels). But now we are staring into a future composed not just of visual interfaces, but of conversational ones as well. Microsoft alone reports that three thousand new bots are built every week on their . Every. Week.</p>

<p>The importance of Conversational UI cannot be understated, even if some of us wish it wasn’t happening.</p>

<p>The most important advancement in Conversational UI has been <strong>N</strong>atural <strong>L</strong>anguage <strong>P</strong>rocessing (NLP). This is the field of computing that deals not with deciphering the exact words that a user said, but with parsing out of it their actual intent. If the bot is the interface, NLP is the brain. In this article, we’re going to take a look at why NLP is so important, and how you (<em>yes, you!</em>) can build your own.</p>

<h3 id="speech-recognition-vs-nlp">Speech Recognition vs. NLP</h3>

<p>Most people will be familiar with Amazon Echo, Cortana, Siri or Google Home, all of which have an interface that is primarily conversational. They are also all using NLP.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7c5bc3d5-bb83-44de-a481-1b87be2d4c87/intelligent-assistants.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7c5bc3d5-bb83-44de-a481-1b87be2d4c87/intelligent-assistants.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7c5bc3d5-bb83-44de-a481-1b87be2d4c87/intelligent-assistants.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7c5bc3d5-bb83-44de-a481-1b87be2d4c87/intelligent-assistants.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7c5bc3d5-bb83-44de-a481-1b87be2d4c87/intelligent-assistants.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7c5bc3d5-bb83-44de-a481-1b87be2d4c87/intelligent-assistants.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7c5bc3d5-bb83-44de-a481-1b87be2d4c87/intelligent-assistants.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>Aside from these intelligent assistants, most Conversational UIs have nothing to do with voice at all. They are text driven. These are the bots we chat with in Slack, Facebook Messenger or over SMS. They deliver high quality gifs in our chats, watch our build processes and even manage our pull requests.</p>



<aside class="product-panel product-panel__tilted product-panel--book">
    <div class="container product-panel--book__container">
      <div class="panel__description panel__description--book">
    <p>Getting workflow <em>just</em> right ain't an easy task. So are proper estimates. Or alignment among different departments. That's why we've set up <strong>'this-is-how-I-work'-sessions</strong> — with smart cookies sharing what works well for them. A part of the , of course.</p>
      <a href="https://www.smashingmagazine.com/membership/" class="btn btn--green btn--large">
        Explore features&nbsp;→
      </a>
      </div>
      <div class="panel__image panel__image--book">
        <a href="https://www.smashingmagazine.com/membership/" class="books__book__image">
        <div class="books__book__img">
          <img src="https://www.smashingmagazine.com/images/smashing-cat/smashing-tv-box-cat.svg" alt="Smashing TV, with live sessions for professional designers and developers." width="310" height="400">
        </div>
      </a>
      </div>
    </div>
  </aside>





<div class="c-garfield-the-cat">












<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f26d209f-fd5f-417e-92e6-9479dac38632/github-bot.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f26d209f-fd5f-417e-92e6-9479dac38632/github-bot.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f26d209f-fd5f-417e-92e6-9479dac38632/github-bot.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f26d209f-fd5f-417e-92e6-9479dac38632/github-bot.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f26d209f-fd5f-417e-92e6-9479dac38632/github-bot.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f26d209f-fd5f-417e-92e6-9479dac38632/github-bot.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f26d209f-fd5f-417e-92e6-9479dac38632/github-bot.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>Conversational UIs built on text are nice because there is no speech recognition component. The text is already parsed.</p>

<p>When it comes to a verbal interaction, the fundamental problem is not recognizing the speech. We’ve mostly got that one down.</p>

<figure class="video-container"><iframe data-src="https://www.youtube.com/embed/JUM3uuAqBV0" width="600" height="480" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe></figure>

<p>OK, so maybe it’s not perfect. I still get voicemails every day like a game of <em>Mad Libs</em> that I never asked to play. iOS just sticks a blank line in whenever they don’t know what exactly was said.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cbc2b2fa-6dc0-404e-9f76-7fa159941250/bad-voicemail.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cbc2b2fa-6dc0-404e-9f76-7fa159941250/bad-voicemail.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cbc2b2fa-6dc0-404e-9f76-7fa159941250/bad-voicemail.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cbc2b2fa-6dc0-404e-9f76-7fa159941250/bad-voicemail.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cbc2b2fa-6dc0-404e-9f76-7fa159941250/bad-voicemail.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cbc2b2fa-6dc0-404e-9f76-7fa159941250/bad-voicemail.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cbc2b2fa-6dc0-404e-9f76-7fa159941250/bad-voicemail.png"
			sizes="60vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>Google, on the other hand, just tries to guess. Like this one from my father. I have absolutely no idea what this message is actually trying to say other than “Be Safe” which honestly sounds like my mom, and not my dad. I have a hard time believing he ever said that. I don’t trust the computer.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/502ff828-f384-4d5a-9820-969b47e0832b/google-voice.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/502ff828-f384-4d5a-9820-969b47e0832b/google-voice.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/502ff828-f384-4d5a-9820-969b47e0832b/google-voice.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/502ff828-f384-4d5a-9820-969b47e0832b/google-voice.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/502ff828-f384-4d5a-9820-969b47e0832b/google-voice.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/502ff828-f384-4d5a-9820-969b47e0832b/google-voice.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/502ff828-f384-4d5a-9820-969b47e0832b/google-voice.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>I’m picking on voice mail transcriptions here, which might be the hardest speech recognition to do given how degraded the audio quality is.</p>

<p>Nevertheless, speech recognition <em>is</em> largely a solved problem. It’s even built right into Chrome and it works remarkably well.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0ed9098e-781f-4e09-aad8-b1d9ae9f5be1/chrome-speech.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0ed9098e-781f-4e09-aad8-b1d9ae9f5be1/chrome-speech.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0ed9098e-781f-4e09-aad8-b1d9ae9f5be1/chrome-speech.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0ed9098e-781f-4e09-aad8-b1d9ae9f5be1/chrome-speech.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0ed9098e-781f-4e09-aad8-b1d9ae9f5be1/chrome-speech.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0ed9098e-781f-4e09-aad8-b1d9ae9f5be1/chrome-speech.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0ed9098e-781f-4e09-aad8-b1d9ae9f5be1/chrome-speech.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>After we solved the problem of speech recognition, we started to use it everywhere. That was unfortunate because speech recognition on it’s own doesn’t do us a whole lot of good. Interfaces that rely soley on speech recognition require the user to state things a precise way and they can only state the limited number of exact words or phrases that the interface knows about. This is not natural. This is not how a conversation works.</p>

<p>Without NLP, Conversational UI can be true nightmare.</p>

<h3 id="conversational-ui-without-nlp">Conversational UI Without NLP</h3>

<p>We’re probably all familiar with automated phone menus. These are known as <strong>I</strong>nteractive <strong>V</strong>oice <strong>R</strong>esponse systems &mdash; or IVRs for short. They are designed to take the place of the traditional operator and automatically transfer callers to the right place without having to talk to a human. On the surface, this seems like a good idea. In practice, it’s mostly just you waiting while a recorded voice reads out a list of menu items that “may have changed.”</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4b642c61-61bc-490e-9eba-db290977df5c/scream.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4b642c61-61bc-490e-9eba-db290977df5c/scream.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4b642c61-61bc-490e-9eba-db290977df5c/scream.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4b642c61-61bc-490e-9eba-db290977df5c/scream.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4b642c61-61bc-490e-9eba-db290977df5c/scream.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4b642c61-61bc-490e-9eba-db290977df5c/scream.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4b642c61-61bc-490e-9eba-db290977df5c/scream.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>A  found that 83% of people feel IVR systems “provide either no benefit at all, or only a cost savings benefit to the company.” They also noted that IVR systems “score lower than any other service option.” People would literally rather do anything else than use an automated phone menu.</p>

<p>NLP has changed the IVR market rather significantly in the past few years. NLP can pick a user’s intent out of anything they say, so it’s better to just let them say it and then determine if you support the action.</p>

<p>Check out how AT&amp;T does it.</p>

<figure class="video-container"><iframe data-src="https://www.youtube.com/embed/ihYCDzqFZ54" width="600" height="480" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe></figure>

<p>AT&amp;T has a truly intelligent Conversational UI. It uses NLP to let me just state my intent. Also, notice that I don&rsquo;t have to know what to say. I can fumble all around and it still picks out my intent.</p>

<p>AT&amp;T also uses information that it already has (my phone number) and then leverages text messaging to send me a link to a traditional visual UI, which is probably a much better UX for making a payment. NLP drives the whole experience here. Without it, the rest of the interaction would not be nearly as smooth.</p>


  <div id="sponsors-article" data-impression="true" class="c-promo-box c-promo-box--ad sponsors hidden" data-audience="non-subscriber" data-remove="true"></div>



<p>NLP is powerful, but more importantly, it is also accessible to developers everywhere. You don’t have to know a thing about Machine Learning (ML) or Artificial Intelligence (AI) to use it. All you need to how to do is make an AJAX call. Even I can do that!</p>

<h3 id="building-an-nlp-interface">Building An NLP Interface</h3>

<p>So much of Machine Learning still remains inaccessible to developers. Even the best YouTube videos on the subject quickly become hard to follow with subjects like <em>Neural Networks</em> and <em>Gradient Descents</em>. We have, however, made significant progress in the field of Language Processing, to the point that it’s accessible to developers of nearly any skill level.</p>

<p>Natural Language Processing differs based on the service, but the overall idea is that the user has an intent, and that intent contains entities. That means exactly nothing to you at the moment, so let’s work up a hypothetical Home Automation bot and see how this works.</p>

<h3 id="the-home-automation-example">The Home Automation Example</h3>

<p>In the field of Natural Language Processing, the canonical “Hello World” is usually a Home Automation demo. This is because it helps to clearly demonstrate the fundamental concepts of NLP without overloading your brain.</p>

<p>A Home Automation Bot is a service that can control hypothetical lights in a hypothetical house. For instance, we might want to say “Turn on the kitchen lights”. That is our intent. If we said “Hello”, we are clearly expressing a different intent. Inside of that intent, there are two pieces of information that we need to complete the action:</p>

<ol>
<li>The ‘Location’ of the light (kitchen)</li>
<li>The desired state of the lights ‘Power’ (on/off)</li>
</ol>

<p>These (Location, Power) are known as entities.</p>

<p>When we are finished designing our NLP interface, we are going to be able to call an HTTP endpoint and pass it our intent: “Turn on the kitchen lights.” That endpoint will return to us the intent (Control Lights) and two objects representing our entities: Location and Power. We can then pass those into a function which actually controls our lights…</p>

<pre><code class="language-javascript">function controlLights(location, power) {
  console.log(`Turning ${power} the ${location} lights`);
  
  // TODO: Call an imaginary endpoint which controls lights   
}
</code></pre>

<p>There are a lot of NLP services out there that are available today for developers. For this example, I’m going to show the  project from Microsoft because it is free to use.</p>

<p>LUIS is a completely visual tool, so we won’t actually be writing any code at all. We’ve already talked about Intents and Entities, so you already know most of the terminology that you need to know to build this interface.</p>

<p>The first step is to create a “Control Lights” intent in LUIS.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/417710b9-4bae-45ec-8a5b-a941476feb28/control-lights.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/417710b9-4bae-45ec-8a5b-a941476feb28/control-lights.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/417710b9-4bae-45ec-8a5b-a941476feb28/control-lights.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/417710b9-4bae-45ec-8a5b-a941476feb28/control-lights.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/417710b9-4bae-45ec-8a5b-a941476feb28/control-lights.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/417710b9-4bae-45ec-8a5b-a941476feb28/control-lights.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/417710b9-4bae-45ec-8a5b-a941476feb28/control-lights.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>Before I do anything with that intent, I need to define my Location and Power entities. Entities can be different types &mdash; kind of like types in a programming language. You can have dates, lists and even entities that are related to other entities. In this case, Power is a list of values (on, off) and Location is a simple entity, which can be any value.</p>

<p>It will be up to LUIS to be smart enough to figure out exactly <em>what</em> the Location is.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7fa12dd0-4290-47a6-9c84-f8b8e2e24615/create-entities.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7fa12dd0-4290-47a6-9c84-f8b8e2e24615/create-entities.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7fa12dd0-4290-47a6-9c84-f8b8e2e24615/create-entities.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7fa12dd0-4290-47a6-9c84-f8b8e2e24615/create-entities.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7fa12dd0-4290-47a6-9c84-f8b8e2e24615/create-entities.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7fa12dd0-4290-47a6-9c84-f8b8e2e24615/create-entities.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7fa12dd0-4290-47a6-9c84-f8b8e2e24615/create-entities.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>












<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/77fdc4d6-1ba1-4178-8833-76388bb395f5/power-entity.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/77fdc4d6-1ba1-4178-8833-76388bb395f5/power-entity.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/77fdc4d6-1ba1-4178-8833-76388bb395f5/power-entity.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/77fdc4d6-1ba1-4178-8833-76388bb395f5/power-entity.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/77fdc4d6-1ba1-4178-8833-76388bb395f5/power-entity.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/77fdc4d6-1ba1-4178-8833-76388bb395f5/power-entity.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/77fdc4d6-1ba1-4178-8833-76388bb395f5/power-entity.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>Now we can begin to train this model to understand all of the different ways that we might ask it to control the lights in a different location. Let’s think of all the different ways that we could do that:</p>

<ul>
<li>Turn off the kitchen lights;</li>
<li>Turn off the lights in the office;</li>
<li>The lights in the living room, turn them on;</li>
<li>Lights, kitchen, off;</li>
<li>Turn off the lights (no location).</li>
</ul>

<p>As I feed these into the Control Lights intent as utterances, LUIS tries to determine where in the intent the entities are. You can see that because Power is a discreet list of values, it gets that right every time.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/78d7d128-e147-4cc0-8f0e-0f4d3e7ee4b1/control-lights-1.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/78d7d128-e147-4cc0-8f0e-0f4d3e7ee4b1/control-lights-1.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/78d7d128-e147-4cc0-8f0e-0f4d3e7ee4b1/control-lights-1.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/78d7d128-e147-4cc0-8f0e-0f4d3e7ee4b1/control-lights-1.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/78d7d128-e147-4cc0-8f0e-0f4d3e7ee4b1/control-lights-1.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/78d7d128-e147-4cc0-8f0e-0f4d3e7ee4b1/control-lights-1.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/78d7d128-e147-4cc0-8f0e-0f4d3e7ee4b1/control-lights-1.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>But it has no idea what a Location even is. LUIS wants us to go through this list and tell it where the Location is. That’s done by clicking on a word or group of words and assigning to the right entity. As we are doing this, we are really creating a machine learning model that LUIS is going to use to statistically estimate what qualifies as a Location.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/547ee534-5a9a-4dec-92b6-3e1da83d4994/control-lights-2.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/547ee534-5a9a-4dec-92b6-3e1da83d4994/control-lights-2.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/547ee534-5a9a-4dec-92b6-3e1da83d4994/control-lights-2.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/547ee534-5a9a-4dec-92b6-3e1da83d4994/control-lights-2.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/547ee534-5a9a-4dec-92b6-3e1da83d4994/control-lights-2.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/547ee534-5a9a-4dec-92b6-3e1da83d4994/control-lights-2.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/547ee534-5a9a-4dec-92b6-3e1da83d4994/control-lights-2.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>When I’m done telling LUIS where in these utterances all the locations are, my dashboard looks like this…</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a33cba90-397a-4ce1-b46b-e68d068980fa/control-lights-3.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a33cba90-397a-4ce1-b46b-e68d068980fa/control-lights-3.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a33cba90-397a-4ce1-b46b-e68d068980fa/control-lights-3.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a33cba90-397a-4ce1-b46b-e68d068980fa/control-lights-3.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a33cba90-397a-4ce1-b46b-e68d068980fa/control-lights-3.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a33cba90-397a-4ce1-b46b-e68d068980fa/control-lights-3.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a33cba90-397a-4ce1-b46b-e68d068980fa/control-lights-3.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>Now we train the model by clicking on the “Train” button at the top. Do you feel like a data scientist yet?</p>

<figure></figure>

<p>Now I can test it using the test panel. You can see that LUIS is already pretty smart. The Power is easy to pick out, but it can actually pick out Locations it has never seen before. It&rsquo;s doing what your brain does &mdash; using the information that it has to make an educated guess. Machine Learning is equal parts impressive and scary.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/833d086a-fd5c-407a-9964-d248dda99331/scary-impressive.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/833d086a-fd5c-407a-9964-d248dda99331/scary-impressive.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/833d086a-fd5c-407a-9964-d248dda99331/scary-impressive.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/833d086a-fd5c-407a-9964-d248dda99331/scary-impressive.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/833d086a-fd5c-407a-9964-d248dda99331/scary-impressive.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/833d086a-fd5c-407a-9964-d248dda99331/scary-impressive.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/833d086a-fd5c-407a-9964-d248dda99331/scary-impressive.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>If we try hard enough, we can fool the AI. The more utterances we give it and label, the smarter it will get. I added 35 utterances to mine before I was done and it is close to bullet proof.</p>

<p>So now we get to the important part, which is how we actually use this NLP in an app. LUIS has a “Publish” menu option which allows us to publish our model to the internet where it’s exposed via a single HTTP endpoint. It will look something like this…</p>

<pre class="break-out"><code class="language-bash">https://westus.api.cognitive.microsoft.com/luis/v2.0/apps/c4396135-ee3f-40a9-8b83-4704cddabf7a?subscription-key=19d29a12d3fc4d9084146b466638e62a&amp;verbose=true&amp;timezoneOffset=0&amp;q=</code></pre>

<p>The very last part of that query string is a <code>q=</code> variable. This is where we would pass our intent.</p>

<pre class="break-out"><code class="language-bash">https://westus.api.cognitive.microsoft.com/luis/v2.0/apps/c4396135-ee3f-40a9-8b83-4704cddabf7a?subscription-key=19d29a12d3fc4d9084146b466638e62a&amp;verbose=true&amp;timezoneOffset=0&amp;q=turn on the kitchen lights</code></pre>

<p>The response that we get back looks is just a JSON object.</p>

<pre><code class="language-javascript">{
  "query": "turn on the kitchen lights",
  "topScoringIntent": {
    "intent": "Control Lights",
    "score": 0.999999046
  },
  "intents": [
    {
      "intent": "Control Lights",
      "score": 0.999999046
    },
    {
      "intent": "None",
      "score": 0.0532306843
    }
  ],
  "entities": [
    {
      "entity": "kitchen",
      "type": "Location",
      "startIndex": 12,
      "endIndex": 18,
      "score": 0.9516622
    },
    {
      "entity": "on",
      "type": "Power",
      "startIndex": 5,
      "endIndex": 6,
      "resolution": {
        "values": [
          "on"
        ]
      }
    }
  ]
}
</code></pre>

<p>Now this is something that we can work with as developers! This is how you add NLP to any project &mdash; with a single REST endpoint. Now you’re free to create a bot with some real brains!</p>

<p> used the browser speech API and a LUIS model to create a voice powered calculator that is running right inside of CodePen. Chrome is required for the speech API.</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="JMwQYg"
   data-user="btholt"
   data-default-tab="result"
   class='codepen'>See the Pen . </p>


<h3 id="bot-design-is-still-hard">Bot Design Is Still Hard</h3>

<p>Having a smart bot is only half the battle. We still need to account for any of the actions that our system might expose, and that can lead to a lot of different logical paths which makes for messy code.</p>

<p>Conversations also happen in stages, so the bot needs to be able to intelligently direct users down the right path without frustrating them or being unable to recover when something goes wrong. It needs to be able to recover when the conversation dies midstream and then starts again. That’s a whole other article and I’ve included some resources below to help.</p>

<p>When it comes to language understanding, the AI platforms are mature and ready to use today. While that won’t help you perfectly design your bot, it will be a key component to building a bot that people don’t hate.</p>

<h4 id="great-ui-is-just-great-ui">Great UI Is Just Great UI</h4>

<p><strong>A final note:</strong> As we saw from the AT&amp;T example, a <em>truly</em> smart interface combines great speech recognition, Natural Language Processing, different types of conversational UI (speech and text) and even a visual UI. In short, great UI is just that &mdash; great UI &mdash; and it is not a zero sum game. Great UIs will leverage all of the technology available to provide the best possible user experience.</p>

<p><em>Special thanks to  for his input on this article.</em></p>

<h4 id="further-resources">Further Resources:</h4>

<ul>
<li>“,” Microsoft Azure (<em>Doc written by Mat Velloso, Kamran Iqbal, and Robert Standefer</em>)</li>
<li>“,” Anton Skorniakov, Smashing Magazine</li>
<li>“,” LUIS, Microsoft Azure</li>
</ul>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(rb, ra, yk, il)</span>
</div>



  <div id="sponsors-article-end" data-impression="true" class="c-promo-box c-promo-box--ad c-promo-box--wide sponsors hidden" data-audience="non-subscriber" data-remove="true"></div>



</div>



              </article>
            </body>
          </html>
---------------