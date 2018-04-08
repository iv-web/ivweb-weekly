## 文章索引
1、 <a href="#1hit-the-ground-running-with-vuejs-and-firestore" >Hit The Ground Running With Vue.js And Firestore</a><br/>
2、 <a href="#2视频演讲-分布式海量二进制文件存储系统" >视频演讲： 分布式海量二进制文件存储系统</a><br/>
3、 <a href="#3视频演讲-深度学习在图像理解中的应用" >视频演讲： 深度学习在图像理解中的应用</a><br/>
4、 <a href="#4everything-new-in-es2016-2017-and-2018" >Everything New in ES2016, 2017, and 2018</a><br/><h1 id="#title_0" >1、Hit The Ground Running With Vue.js And Firestore</h1>
Lukas van Driel
[https://www.smashingmagazine.com/2018/04/vuejs-firebase-firestore/](https://www.smashingmagazine.com/2018/04/vuejs-firebase-firestore/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/04/vuejs-firebase-firestore/" />
              <title>Hit The Ground Running With Vue.js And Firestore</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>Hit The Ground Running With Vue.js And Firestore</h1>
                  
                    
                    <address>Lukas van Driel</address>
                  
                  <time datetime="2018-04-06T13:30:33&#43;02:00" class="op-published">2018-04-06T13:30:33+02:00</time>
                  <time datetime="2018-04-06T19:56:59&#43;00:00" class="op-modified">2018-04-06T19:56:59+00:00</time>
                </header>
                

<p>Google Firebase has a new data storage possibility called ‘Firestore’ (currently in beta stage) which builds on the success of the <em>Firebase Realtime Database</em> but adds some nifty features. In this article, we’ll set up the basics of a web app using Vue.js and Firestore.</p>

<p>Let&rsquo;s say you have this great idea for a new product (e.g. the next Twitter, Facebook, or Instagram, because we can never have too much social, right?). To start off, you want to make a prototype or <strong>M</strong>inimum <strong>V</strong>iable <strong>P</strong>roduct (MVP) of this product. The goal is to build the core of the app as fast as possible so you can show it to users and get feedback and analyze usage. The emphasis is heavily on development speed and quick iterating.</p>

<p>But before we start building, our amazing product needs a name. Let&rsquo;s call it “Amazeballs.” It’s going to be <em>legen</em> &mdash; wait for it &mdash; <em>dary</em>!</p>

<p>Here’s a shot of how I envision it:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/24ca95ce-f01e-44ad-a95d-556c4377616c/vuejs-and-firebase-image1.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/24ca95ce-f01e-44ad-a95d-556c4377616c/vuejs-and-firebase-image1.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/24ca95ce-f01e-44ad-a95d-556c4377616c/vuejs-and-firebase-image1.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/24ca95ce-f01e-44ad-a95d-556c4377616c/vuejs-and-firebase-image1.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/24ca95ce-f01e-44ad-a95d-556c4377616c/vuejs-and-firebase-image1.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/24ca95ce-f01e-44ad-a95d-556c4377616c/vuejs-and-firebase-image1.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/24ca95ce-f01e-44ad-a95d-556c4377616c/vuejs-and-firebase-image1.png"
			sizes="100vw"
			alt="Screenshot of Amazeballs app"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The legendary Amazeballs app
		</figcaption>
	
</figure>


<p>Our Amazeballs app is &mdash; of course &mdash; all about sharing cheesy tidbits of your personal life with friends, in so-called Balls. At the top is a form for posting Balls, below that are your friends’ Balls.</p>

<p>When building an MVP, you&rsquo;ll need tooling that gives you the power to quickly implement the key features as well as the flexibility to quickly add and change features later on. My choice falls on Vue.js as it&rsquo;s a Javascript-rendering framework, backed by the Firebase suite (by Google) and its new real-time database called Firestore.</p>



  <aside class="product-panel product-panel__tilted product-panel--book">
    <div class="container product-panel--book__container">
      <div class="panel__description panel__description--book">
    <p><em>“You must unlearn what you have learned!”</em> Meet the <strong>brand new episode</strong> of  with smart front-end tricks and UX techniques. Featuring Yiying Lu, Aarron Draplin, Smashing Yoda, and many others. Tickets now on sale. April <span class="small-caps">17-18</span>.</p>
      <a href="https://www.smashingmagazine.com/events/san-francisco-2018/#speakers" class="btn btn--green btn--large">
        Check the speakers&nbsp;→
      </a>
      </div>
      <div class="panel__image panel__image--book">
        <a href="https://www.smashingmagazine.com/membership/" class="books__book__image">
        <div class="books__book__img">
          <img src="https://www.smashingmagazine.com/images/smashing-cat/cat-smashingconf-sf.png" alt="SmashingConf San Francisco, with Yiying Lu, Josh Clark and many others." width="310" height="400">
        </div>
      </a>
      </div>
    </div>
  </aside>





<div class="c-garfield-the-cat">


<p>Firestore can directly be accessed using normal HTTP methods which makes it a full backend-as-a-service solution in which you don’t have to manage any of your own servers but still store data online.</p>

<p>Sounds powerful and daunting, but no sweat, I&rsquo;ll guide you through the steps of creating and hosting this new web app. Notice how big the scrollbar is on this page; there’s not a huge amount of steps to it. Also, if you want to know where to put each of the code snippets in a code repository, you can see a .</p>

<h3 id="let-s-start">Let’s Start</h3>

<p>We’re starting out with . It’s great for Javascript beginners, as you start out with HTML and gradually add logic to it. But don’t underestimate; it packs a lot of powerful features. This combination makes it my first choice for a front-end framework.</p>

<p>Vue.js has a . We’ll use that to get the bare-bones set-up quickly. First, install the CLI, then use it to create a new project based on the &ldquo;webpack-simple&rdquo; template.</p>

<pre><code class="language-bash">npm install -g vue-cli

vue init webpack-simple amazeballs
</code></pre>

<p>If you follow the steps on the screen (<code>npm install</code> and <code>npm run dev</code>) a browser will open with a big Vue.js logo.</p>

<p>Congrats! That was easy.</p>

<p>Next up, we need to create a Firebase project. Head on over to  and create a project. A project starts out in the free Spark plan, which gives you a limited database (1 GB data, 50K reads per day) and 1 GB of hosting. This is more than enough for our MVP, and easily upgradable when the app gains traction.</p>

<p>Click on the ‘Add Firebase to your web app’ to display the config that you need. We’ll use this config in our application, but in a nice Vue.js manner using .</p>

<p>First <code>npm install firebase</code>, then create a file called <em>src/store.js</em>. This is the spot that we’re going to put the shared state in so that each Vue.js component can access it independently of the component tree. Below is the content of the file. The state only contains some placeholders for now.</p>

<pre class="break-out"><code class="language-javascript">import Vue from 'vue';
import firebase from 'firebase/app';
import 'firebase/firestore';

// Initialize Firebase, copy this from the cloud console
// Or use mine :)
var config = {
  apiKey: "AIzaSyDlRxHKYbuCOW25uCEN2mnAAgnholag8tU",
  authDomain: "amazeballs-by-q42.firebaseapp.com",
  databaseURL: "https://amazeballs-by-q42.firebaseio.com",
  projectId: "amazeballs-by-q42",
  storageBucket: "amazeballs-by-q42.appspot.com",
  messagingSenderId: "972553621573"
};
firebase.initializeApp(config);

// The shared state object that any vue component can get access to. 
// Has some placeholders that we’ll use further on!
export const store = {
  ballsInFeed: null,
  currentUser: null,
  writeBall: (message) => console.log(message)
};
</code></pre>

<p>Now we’ll add the Firebase parts. One piece of code to get the data from the Firestore:</p>

<pre><code class="language-javascript">// a reference to the Balls collection
const ballsCollection = firebase.firestore()
  .collection('balls');

// onSnapshot is executed every time the data
// in the underlying firestore collection changes
// It will get passed an array of references to 
// the documents that match your query
ballsCollection
  .onSnapshot((ballsRef) => {
    const balls = [];
    ballsRef.forEach((doc) => {
      const ball = doc.data();
      ball.id = doc.id;
      balls.push(ball);
    });
    store.ballsInFeed = balls;
  });</code></pre>

<p>And then replace the <code>writeBall</code> function with one that actually executes a write:</p>

<pre><code class="language-javascript">writeBall: (message) => ballsCollection.add({
  createdOn: new Date(),
  author: store.currentUser,
  message
})</code></pre>

<p>Notice how the two are completely decoupled. When you insert into a collection, the <code>onSnapshot</code> is triggered because you’ve inserted an item. This makes state management a lot easier.</p>

<p>Now you have a shared state object that any Vue.js component can easily get access to. Let’s put it to good use.</p>




  <aside class="product-panel product-panel__tilted product-panel--book" data-audience="non-subscriber" data-remove="true">
    <div class="container product-panel--book__container">
      <div class="panel__description panel__description--book">
        <p>
          Is your pattern library up to date today? <em>Alla Kholmatova</em> has just finished a fully fledged book on <strong>Design Systems</strong> and how to get them right. With common traps, gotchas and the lessons she learned. Hardcover, eBook. <em>Just sayin'.</em>
        </p>
        <a href="https://www.smashingmagazine.com/printed-books/design-systems/">
          <button class="btn btn--green btn--large">
            Table of Contents&nbsp;&rarr;
          </button>
        </a>
      </div>
      <div class="panel__image panel__image--book">
        <a href="https://www.smashingmagazine.com/printed-books/design-systems/" class="books__book__image">
        <div class="books__book__img">
          <img src="https://www.smashingmagazine.com/images/books/design-systems--large-opt.png">
        </div>
      </a>
      </div>
    </div>
  </aside>




<h3 id="post-stuff">Post Stuff!</h3>

<p>First, let’s find out who the current user is.</p>

<p>Firebase has authentication APIs that help you with the grunt of the work of getting to know your user. Enable the appropriate ones on the  in <em>Authentication</em> &rarr; <em>Sign In Method</em>. For now, I’m going to use Google Login &mdash; with a very non-fancy button.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5d072d18-c52d-4c27-8ca8-1b869a2f30a2/vuejs-and-firebase-image2.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5d072d18-c52d-4c27-8ca8-1b869a2f30a2/vuejs-and-firebase-image2.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5d072d18-c52d-4c27-8ca8-1b869a2f30a2/vuejs-and-firebase-image2.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5d072d18-c52d-4c27-8ca8-1b869a2f30a2/vuejs-and-firebase-image2.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5d072d18-c52d-4c27-8ca8-1b869a2f30a2/vuejs-and-firebase-image2.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5d072d18-c52d-4c27-8ca8-1b869a2f30a2/vuejs-and-firebase-image2.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5d072d18-c52d-4c27-8ca8-1b869a2f30a2/vuejs-and-firebase-image2.png"
			sizes="100vw"
			alt="Screenshot of login page with Google authentication"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Authentication with Google Login
		</figcaption>
	
</figure>


<p>Firebase doesn’t give you any interface help, so you’ll have to create your own &ldquo;Login with Google/Facebook/Twitter&rdquo; buttons, and/or username/password input fields. Your login component will probably look a bit like this:</p>

<pre class="break-out"><code class="language-javascript">&lt;template&gt;
  &lt;div&gt;
    &lt;button @click.prevent="signInWithGoogle"&gt;Log in with Google&lt;/button&gt;
  &lt;/div&gt;
&lt;/template&gt;

&lt;script&gt;
import firebase from 'firebase/app';
import 'firebase/auth';

export default {
  methods: {
    signInWithGoogle() {
      var provider = new firebase.auth.GoogleAuthProvider();
      firebase.auth().signInWithPopup(provider);
    }
  }
}
&lt;/script&gt;</code></pre>

<p>Now there’s one more piece of the login puzzle, and that’s getting the <code>currentUser</code> variable in the store. Add these lines to your <em>store.js</em>:</p>

<pre><code class="language-javascript">// When a user logs in or out, save that in the store
firebase.auth().onAuthStateChanged((user) => {
  store.currentUser = user;
});</code></pre>

<p>Due to these three lines, every time the currently-logged-in user changes (logs in or out), <code>store.currentUser</code> also changes. Let&rsquo;s post some Balls!</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/41d9c2b0-3f0d-45bf-aa36-c8239079d39b/vuejs-and-firebase-image3.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/41d9c2b0-3f0d-45bf-aa36-c8239079d39b/vuejs-and-firebase-image3.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/41d9c2b0-3f0d-45bf-aa36-c8239079d39b/vuejs-and-firebase-image3.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/41d9c2b0-3f0d-45bf-aa36-c8239079d39b/vuejs-and-firebase-image3.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/41d9c2b0-3f0d-45bf-aa36-c8239079d39b/vuejs-and-firebase-image3.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/41d9c2b0-3f0d-45bf-aa36-c8239079d39b/vuejs-and-firebase-image3.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/41d9c2b0-3f0d-45bf-aa36-c8239079d39b/vuejs-and-firebase-image3.png"
			sizes="100vw"
			alt="Screenshot of logout option"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Login state is stored in the store.js file
		</figcaption>
	
</figure>


<p>The input form is a separate Vue.js component that is hooked up to the <code>writeBall</code> function in our store, like this:</p>

<pre><code class="language-javascript">&lt;template&gt;
  &lt;form @submit.prevent="formPost"&gt;
    &lt;textarea v-model="message" /&gt;
    &lt;input type="submit" value="DUNK!" /&gt;
  &lt;/form&gt;
&lt;/template&gt;

&lt;script&gt;
import { store } from './store';

export default {
  data() {
    return {
      message: null,
    };
  },
  methods: {
    formPost() {
      store.writeBall(this.message);
    }
  },
}
&lt;/script&gt;</code></pre>

<p>Awesome! Now people can log in and start posting Balls. But wait, we’re missing authorization. We want you to only be able to post Balls yourself, and that’s where <em>Firestore Rules</em> come in. They’re made up of Javascript-ish code that defines access privileges to the database. You can enter them via the Firestore console, but you can also use the Firebase CLI to install them from a file on disk. Install and run it like this:</p>

<pre><code class="language-bash">npm install -g firebase-tools
firebase login
firebase init firestore</code></pre>

<p>You’ll get a file named <em>firestore.rules</em> where you can add authorization for your app. We want every user to be able to insert their own balls, but not to insert or edit someone else’s. The below example do nicely. It allows everyone to read all documents in the database, but you can only insert if you’re logged in, and the inserted resource has a field “author” that is the same as the currently logged in user.</p>

<pre><code class="language-javascript">service cloud.firestore {
  match /databases/{database}/documents {
    match /{document=**} {
      allow read: if true;
      allow create: if request.auth.uid != null &amp;&amp; request.auth.uid == request.resource.data.author;
    }
  }
}</code></pre>

<p>It looks like just a few lines of code, but it’s very powerful and can get complex very quickly. Firebase is working on better tooling around this part, but for now, it’s trial-and-error until it behaves the way you want.</p>

<p>If you run <code>firebase deploy</code>, the Firestore rules will be deployed and securing your production data in seconds.</p>




<h3 id="adding-server-logic">Adding Server Logic</h3>

<p>On your homepage, you want to see a timeline with your friends’ Balls. Depending on how you want to determine which Balls a user sees, performing this query directly on the database could be a performance bottleneck. An alternative is to create a <em>Firebase Cloud Function</em> that activates on every posted Ball and appends it to the walls of all the author&rsquo;s friends. This way it&rsquo;s asynchronous, non-blocking and eventually consistent. Or in other words, it&rsquo;ll get there.</p>

<p>To keep the examples simple, I’ll do a small demo of listening to created Balls and modifying their message. Not because this is particularly useful, but to show you how easy it is to get cloud functions up-and-running.</p>

<pre><code class="language-javascript">const functions = require('firebase-functions');

exports.createBall = functions.firestore
  .document('balls/{ballId}')
  .onCreate(event => {
    var createdMessage = event.data.get('message');
    return event.data.ref.set({
      message: createdMessage + ', yo!'
    }, {merge: true});
});</code></pre>

<p>Oh, wait, I forgot to tell you where to write this code.</p>

<pre><code class="language-bash">firebase init functions</code></pre>

<p>This creates the functions directory with an <em>index.js</em>. That’s the file you can write your own <em>Cloud Functions</em> in. Or copy-paste mine if you’re very impressed by it.</p>

<p><em>Cloud Functions</em> give you a nice spot to decouple different parts of your application and have them asynchronously communicate. Or, in architectural drawing style:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/60a32785-e375-49c4-b9bc-887951a2a343/vuejs-and-firebase-image4.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/60a32785-e375-49c4-b9bc-887951a2a343/vuejs-and-firebase-image4.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/60a32785-e375-49c4-b9bc-887951a2a343/vuejs-and-firebase-image4.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/60a32785-e375-49c4-b9bc-887951a2a343/vuejs-and-firebase-image4.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/60a32785-e375-49c4-b9bc-887951a2a343/vuejs-and-firebase-image4.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/60a32785-e375-49c4-b9bc-887951a2a343/vuejs-and-firebase-image4.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/60a32785-e375-49c4-b9bc-887951a2a343/vuejs-and-firebase-image4.png"
			sizes="100vw"
			alt="Server logic architectural diagram of Cloud Functions"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Asynchronous communication between the different components of your application
		</figcaption>
	
</figure>


<h3 id="last-step-deployment">Last Step: Deployment</h3>

<p>Firebase has its Hosting option available for this, and you can use it via the Firebase CLI.</p>

<pre><code class="language-bash">firebase init hosting</code></pre>

<p>Choose <code>dist</code>as a public directory, and then ‘Yes’ to rewrite all URLs to <code>index.html</code>. This last option allows you to use  to manage pretty URLs within your app.</p>

<p>Now there’s a small hurdle: the <code>dist</code> folder doesn’t contain an <code>index.html</code> file that points to the right build of your code. To fix this, add an npm script to your <code>package.json</code>:</p>

<pre><code class="language-javascript">{
  "scripts": {
    "deploy": "npm run build &amp;&amp; mkdir dist/dist &amp;&amp; mv dist/*.* dist/dist/ &amp;&amp; cp index.html dist/ &amp;&amp; firebase deploy"
  }
}</code></pre>

<p>Now just run <code>npm deploy</code>, and the Firebase CLI will show you the URL of your hosted code!</p>

<h3 id="when-to-use-this-architecture">When To Use This Architecture</h3>

<p>This setup is perfect for an MVP. By the third time you’ve done this, you’ll have a working web app in minutes &mdash; backed by a scalable database that is hosted for free. You can immediately start building features.</p>

<p>Also, there’s a lot of space to grow. If <em>Cloud Functions</em> aren’t powerful enough, you can fall back to a traditional API running on docker in Google Cloud for instance. Also, you can upgrade your Vue.js architecture with <code>vue-router</code> and <code>vuex</code>, and use the power of webpack that’s included in the vue-cli template.</p>

<p>It’s not all rainbows and unicorns, though. The most notorious caveat is the fact that your clients are immediately talking to your database. There’s no middleware layer that you can use to transform the raw data into a format that’s easier for the client. So, you have to store it in a client-friendly way. Whenever your clients request change, you’re going to find it pretty difficult to run data migrations on Firebase. For that, you’ll need to write a custom Firestore client that reads every record, transforms it, and writes it back.</p>

<blockquote class="pull-quote"><p></p></blockquote>

<p>So what are examples of projects using these tools? Amongst the big names that use Vue.js are  that was downloaded over a million times in the first five days. It can take quite some load, and it’s very versatile with clients for web, native mobile, Unity, and so on.</p>

<h3 id="where-do-i-sign-up">Where Do I Sign Up?!</h3>

<p>If you want to learn more, consider the following resources:</p>

<ul>
<li> containing all of the above code</li>
<li>Documentation on </li>
<li>Documentation on </li>
<li>An entertaining way to get to know Firebase better &mdash; </li>
</ul>

<p>Happy coding!</p>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(da, ra, hj, il)</span>
</div>


</div>




  <div id="sponsors-article-end" data-impression="true" class="c-promo-box c-promo-box--ad c-promo-box--wide sponsors hidden" data-audience="non-subscriber" data-remove="true"></div>



              </article>
            </body>
          </html>
---------------
<h1 id="#title_1" >2、视频演讲： 分布式海量二进制文件存储系统</h1>
夏鸣
[http://www.infoq.com/cn/presentations/distributed-mass-binary-file-storage-system?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/distributed-mass-binary-file-storage-system?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/presentations/distributed-mass-binary-file-storage-system/zh/mediumimage/xiaming270-1521959582852.jpg"/><p>随着互联网爆炸式增长，如何高效可靠地存储海量图片、视频、备份等数据成为决定系统综合性能的关键因素。本次分享，夏鸣博士将为大家介绍 Ambry，一个由领英开发的分布式二进制文件存储系统。Ambry 是 Apache 许可的 开源软件，已在领英生产环境中稳定运行两年。本次分享将包括 Ambry 的设计原理与架构，以及针对大文件流（streaming）的处理与优化。
</p> <i>By 夏鸣</i>
---------------
<h1 id="#title_2" >3、视频演讲： 深度学习在图像理解中的应用</h1>
熊鹏飞
[http://www.infoq.com/cn/presentations/the-application-of-deep-learning-in-image-understanding?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/the-application-of-deep-learning-in-image-understanding?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/presentations/the-application-of-deep-learning-in-image-understanding/zh/mediumimage/xiongpengfei270-1521984427953.jpg"/><p>此次视频主要分享的内容为：图像理解的定义；传统图像理解技术；深度学习基础知识；深度学习图像理解技术；图像理解进阶。</p> <i>By 熊鹏飞</i>
---------------
<h1 id="#title_3" >4、Everything New in ES2016, 2017, and 2018</h1>

[https://javascriptweekly.com/issues/380](https://javascriptweekly.com/issues/380)
<table border=0 align="center" border="0">
  <tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   ">

  <div>    
    <table border=0 border=0><tr>
<td align="left" style="padding-left: 4px; font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   "><p>#380 — April  6, 2018</p></td>
<td align="right" style="padding-right: 4px; font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   "><p></p></td>
</tr></table>
    
    <table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0 12px;  "><p>JavaScript Weekly</p></td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — This is a worthwhile roundup of all the new bits and pieces in recent ECMAScript specs, but note that <code>SharedBufferArray</code> support has been disabled in most runtimes due to Spectre, so give that a miss.</p>
  <p>Raja Rao DV </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — This is a big deal given the weight this book has in the field.</p>
  <p>Martin Fowler </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"> enables interoperability between WebAssembly modules and JavaScript.</p>
  <p>Alex Crichton </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;">.</p>
  <p>Scrivito <span style="text-transform: uppercase; padding: 1px 4px;  margin-left: 4px; font-size: 0.9em;   color: #997 !important;">sponsor</span></p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;">▶  </span> — RxJS is used for reactive programming using observable streams and this is a great ‘from scratch’ crash course.</p>
  <p>Gary Simon </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;">, a feature introduced in ES6, work.</p>
  <p>Arfat Salman </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — A 4 part series from PubNub brought together in one place walking through bringing the Google Maps JavaScript API together with PubNub’s real-time services.</p>
  <p>Joe Hanson </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>webpack on Twitter </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></p>
  <p>Rob Eisenberg </p>
</td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  "><p>💻 Jobs</p></td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Sticker Mule is looking for passionate developers to join our remote team. Come help us become the Internet’s best place to shop and work.</p>
  <p>Sticker Mule </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — MotorK is looking for passionate Junior and Senior mobile devs to join the team. Great place to work and career opportunities.</p>
  <p>MotorK </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"> today.</p>
  <p>woo.io </p>
</td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  "><p>📘 Tutorials</p></td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Firestore is a new data storage approach from Google Firebase.</p>
  <p>Lukas Van Driel </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — $99 Introductory, online rate. In-person rate available to join us at the Ranch.</p>
  <p>Big Nerd Ranch <span style="text-transform: uppercase; padding: 1px 4px;  margin-left: 4px; font-size: 0.9em;   color: #997 !important;">sponsor</span></p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Google </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Dr. Axel Rauschmayer </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Marcin Wanago </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Experimental but neat.</p>
  <p>Anders Pitman </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Adeyinka Adegbenro </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Snipcart <span style="text-transform: uppercase; padding: 1px 4px;  margin-left: 4px; font-size: 0.9em;   color: #997 !important;">sponsor</span></p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>DJ Walker </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Kyle Pennell </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Claudio Ribeiro </p>
</td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  "><p>🔧 Code and Tools</p></td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Imagine a CDN but more dynamic and with more control.</p>
  <p>Fly.io </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;">) but may prove handy to JS developers too.</p>
  <p>Tom Hudson </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Try Segment and integrate 200+ tools with the flip of a switch.</p>
  <p>Segment <span style="text-transform: uppercase; padding: 1px 4px;  margin-left: 4px; font-size: 0.9em;   color: #997 !important;">sponsor</span></p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>GoDaddy Open Source </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>The Sails Company </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — <em>“Designed to slide. No less, no more”</em> says the creator.</p>
  <p>Jędrzej Chałubek </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></p>
  <p>Daniel Cook </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Based on a pattern like ‘ca_se’ or ‘CaSe’.</p>
  <p>Pedro Moreira </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Vladimir Simonov </p>
</td></tr></table>
<table border=0 border=0><tr><td style=" font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   "></td></tr></table>
</div>

  </td></tr>
</table>





<img src="https://javascriptweekly.com/open/380/rss" width="1" height="1" />
---------------