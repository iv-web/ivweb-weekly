## 文章索引
1、 <a href="#1building-mobile-apps-with-capacitor-and-vuejs" >Building Mobile Apps With Capacitor And Vue.js</a><br/>
2、 <a href="#2文章-太平洋保险cims系统微前端实践" >文章： 太平洋保险CIMS系统微前端实践</a><br/>
3、 <a href="#3视频演讲-serverless小程序后端技术分享" >视频演讲： serverless小程序后端技术分享</a><br/>
4、 <a href="#4谷歌fuchsia操作系统将支持运行linux应用程序" >谷歌Fuchsia操作系统将支持运行Linux应用程序</a><br/>
5、 <a href="#5文章-buzzfeed如何从perl单体应用迁移到go和python微服务" >文章： BuzzFeed如何从Perl单体应用迁移到Go和Python微服务</a><br/>
6、 <a href="#6fex-技术周刊---2018/07/02" >FEX 技术周刊 - 2018/07/02</a><br/>
7、 <a href="#7linus-说工程师要爱上-无聊-zemlin-说开源不是零和游戏华为说真正的价值在于有多少人用这个东西|-lc3-2018" >Linus 说工程师要爱上“ 无聊” ，Zemlin 说开源不是零和游戏，华为说真正的价值在于有多少人用这个东西| LC3 2018</a><br/>
8、 <a href="#8文章-改进github工作流的15个建议" >文章： 改进GitHub工作流的15个建议</a><br/>
9、 <a href="#9mlnet-02版增加了集群和新示例" >ML.NET 0.2版增加了集群和新示例</a><br/>
10、 <a href="#10与专门团队一起持续交付" >与专门团队一起持续交付</a><br/>
11、 <a href="#11microsoft-edge现已支持w3c-webdriver建议" >Microsoft Edge现已支持W3C WebDriver建议</a><br/>
12、 <a href="#12tlbleed漏洞通过探测tlb获取cpu秘钥" >TLBleed漏洞：通过探测TLB获取CPU秘钥</a><br/>
13、 <a href="#13文章-使用apache-kafka和ksql实现普及化流处理" >文章： 使用Apache Kafka和KSQL实现普及化流处理</a><br/>
14、 <a href="#14文章-kylin在滴滴olap引擎中的应用" >文章： Kylin在滴滴OLAP引擎中的应用</a><br/><h1 id="#title_0" >1、Building Mobile Apps With Capacitor And Vue.js</h1>
Ahmed Bouchefra
[https://www.smashingmagazine.com/2018/07/mobile-apps-capacitor-vue-js/](https://www.smashingmagazine.com/2018/07/mobile-apps-capacitor-vue-js/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/07/mobile-apps-capacitor-vue-js/" />
              <title>Building Mobile Apps With Capacitor And Vue.js</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>Building Mobile Apps With Capacitor And Vue.js</h1>
                  
                    
                    <address>Ahmed Bouchefra</address>
                  
                  <time datetime="2018-07-02T14:00:41&#43;02:00" class="op-published">2018-07-02T14:00:41+02:00</time>
                  <time datetime="2018-07-02T23:04:44&#43;00:00" class="op-modified">2018-07-02T23:04:44+00:00</time>
                </header>
                

<p>Recently, the Ionic team announced an open-source spiritual successor to Apache Cordova and Adobe PhoneGap, called . Capacitor allows you to build an application with modern web technologies and run it everywhere, from web browsers to native mobile devices (Android and iOS) and even desktop platforms via Electron &mdash; the popular GitHub platform for building cross-platform desktop apps with Node.js and front-end web technologies.</p>

<p>Ionic &mdash; the most popular hybrid mobile framework &mdash; currently runs on top of Cordova, but in future versions, Capacitor will be the default option for Ionic apps. Capacitor also provides a compatibility layer that permits the use of existing Cordova plugins in Capacitor projects.</p>

<p>Aside from using Capacitor in Ionic applications, you can also use it without Ionic with your preferred front-end framework or UI library, such as Vue, React, Angular with Material, Bootstrap, etc.</p>

<p>In this tutorial, we’ll see how to use Capacitor and Vue to build a simple mobile application for Android. In fact, as mentioned, your application can also run as a progressive web application (PWA) or as a desktop application in major operating systems with just a few commands.</p>

<p>We’ll also be using some Ionic 4 UI components to style our demo mobile application.</p>



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




<h3 id="capacitor-features">Capacitor Features</h3>

<p>Capacitor has many features that make it a good alternative to other solutions such as Cordova. Let’s see some of the features of Capacitor:</p>

<ul>
<li><strong>Open-source and free</strong><br />
Capacitor is an open-source project, licensed under the permissive MIT license and maintained by  and the community.</li>
<li><strong>Cross-platform</strong><br />
You can use Capacitor to build apps with one code base and to target multiple platforms. You can run a few more command line interface (CLI) commands to support another platform.</li>
<li><strong>Native access to platform SDKs</strong><br />
Capacitor doesn’t get in the way when you need access to native SDKs.</li>
<li><strong>Standard web and browser technologies</strong><br />
An app built with Capacitor uses standard web APIs, so your application will also be cross-browser and will run well in all modern browsers that follow the standards.</li>
<li><strong>Extensible</strong><br />
You can access native features of the underlying platforms by adding plugins or, if you can’t find a plugin that fits your needs, by creating a custom plugin via a simple API.</li>
</ul>

<h3 id="requirements">Requirements</h3>

<p>To complete this tutorial, you’ll need a development machine with the following requirements:</p>

<ul>
<li>You’ll need Node <em>v8.6+</em> and npm <em>v5.6+</em> installed on your machine. Just head to the  and download the version for your operating system.</li>
<li>To build an iOS app, you’ll need a Mac with Xcode.</li>
<li>To build an Android app, you’ll need to install the Java 8 JDK and Android Studio with the Android SDK.</li>
</ul>

<h3 id="creating-a-vue-project">Creating A Vue Project</h3>

<p>In this section, we’ll install the Vue CLI and generate a new Vue project. Then, we’ll add navigation to our application using the Vue router. Finally, we’ll build a simple UI using Ionic 4 components.</p>

<h4 id="installing-the-vue-cli-v3">Installing The Vue CLI v3</h4>

<p>Let’s start by installing the Vue CLI v3 from npm by running the following from the command line:</p>

<pre><code class="language-bash">$ npm install -g @vue/cli
</code></pre>

<p>You might need to add <code>sudo</code> to install the package globally, depending on your npm configuration.</p>

<h4 id="generating-a-new-vue-project">Generating a New Vue Project</h4>

<p>After installing the Vue CLI, let’s use it to generate a new Vue project by running the following from the CLI:</p>

<pre><code class="language-bash">$ vue create vuecapacitordemo
</code></pre>

<p>You can start a development server by navigating within the project’s root folder and running the following command:</p>

<pre><code class="language-bash"> $ cd vuecapacitordemo
 $ npm run serve
</code></pre>

<p>Your front-end application will be running from <code>http://localhost:8080/</code>.</p>

<p>If you visit <code>http://localhost:8080/</code> in your web browser, you should see the following page:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/57960337-f55a-4b60-818d-a96a9b0b6605/welcome-vue-js-app.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/57960337-f55a-4b60-818d-a96a9b0b6605/welcome-vue-js-app.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/57960337-f55a-4b60-818d-a96a9b0b6605/welcome-vue-js-app.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/57960337-f55a-4b60-818d-a96a9b0b6605/welcome-vue-js-app.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/57960337-f55a-4b60-818d-a96a9b0b6605/welcome-vue-js-app.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/57960337-f55a-4b60-818d-a96a9b0b6605/welcome-vue-js-app.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/57960337-f55a-4b60-818d-a96a9b0b6605/welcome-vue-js-app.png"
			sizes="100vw"
			alt="A Vue application"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			A Vue application ()
		</figcaption>
	
</figure>


<h3 id="adding-ionic-4">Adding Ionic 4</h3>

<p>To be able to use Ionic 4 components in your application, you’ll need to use the core Ionic 4 package from npm.</p>

<p>So, go ahead and open the <code>index.html</code> file, which sits in the <code>public</code> folder of your Vue project, and add the following <code>&amp;lt;script src='https://unpkg.com/@ionic/core@4.0.0-alpha.7/dist/ionic.js'&amp;gt;&amp;lt;/script&amp;gt;</code> tag in the head of the file.</p>

<p>This is the contents of <code>public/index.html</code>:</p>

<pre class="break-out"><code class="language-html">&lt;!DOCTYPE html>
&lt;html>
&lt;head>
&lt;meta  charset="utf-8">
&lt;meta  http-equiv="X-UA-Compatible"  content="IE=edge">
&lt;meta  name="viewport"  content="width=device-width,initial-scale=1.0">
&lt;link  rel="icon"  href="&lt;%= BASE_URL %>favicon.ico">
&lt;title>vuecapacitordemo&lt;/title>
&lt;/head>
&lt;body>
&lt;noscript>
&lt;strong>We’re sorry but vuecapacitordemo doesn’t work properly without JavaScript enabled. Please enable it to continue.&lt;/strong>
&lt;/noscript>
&lt;div  id="app">&lt;/div>
&lt;!-- built files will be auto injected -->
&lt;script  src='https://unpkg.com/@ionic/core@4.0.0-alpha.7/dist/ionic.js'>&lt;/script>
&lt;/body>
&lt;/html>
</code></pre>

<p>You can get the current version of the Ionic core package from .</p>

<p>Now, open <code>src/App.vue</code>, and add the following content within the <code>template</code> tag after deleting what’s in there:</p>

<pre><code class="language-html">&lt;template>
&lt;ion-app>
   &lt;router-view>&lt;/router-view>
&lt;/ion-app>
&lt;/template>
</code></pre>

<p><code>ion-app</code> is an Ionic component. It should be the top-level component that wraps other components.</p>

<p><code>router-view</code> is the Vue router outlet. A component matching a path will be rendered here by the Vue router.</p>

<p>After adding Ionic components to your Vue application, you are going to start getting warnings in the browser console similar to the following:</p>

<pre class="break-out"><code class="language-html">
[Vue warn]: Unknown custom element: &lt;ion-content> - did you register the component correctly? For recursive components, make sure to provide the "name" option.

found in

---> &lt;HelloWorld> at src/components/HelloWorld.vue
       &lt;App> at src/App.vue
         &lt;Root>
</code></pre>

<p>This is because Ionic 4 components are actually web components, so you’ll need to tell Vue that components starting with the <code>ion</code> prefix are not Vue components. You can do that in the <code>src/main.js</code> file by adding the following line:</p>

<pre><code class="language-javascript">Vue.config.ignoredElements = [/^ion-/]
</code></pre>

<p>Those warnings should now be eliminated.</p>

<h4 id="adding-vue-components">Adding Vue Components</h4>

<p>Let’s add two components. First, remove any file in the <code>src/components</code> folder (also, remove any import for the <code>HelloWorld.vue</code> component in <code>App.vue</code>), and add the <code>Home.vue</code> and <code>About.vue</code> files.</p>

<p>Open <code>src/components/Home.vue</code> and add the following template:</p>

<pre class="break-out"><code class="language-html">&lt;template>
&lt;ion-app>
&lt;ion-header>
  &lt;ion-toolbar color="primary">
    &lt;ion-title>
      Vue Capacitor
    &lt;/ion-title>
  &lt;/ion-toolbar>
&lt;/ion-header>

&lt;ion-content padding>
  The world is your oyster.
  &lt;p>If you get lost, the &lt;a href="https://ionicframework.com/docs">docs&lt;/a> will be your guide.&lt;/p>
&lt;/ion-content>
&lt;/ion-app>
&lt;/template>
</code></pre>

<p>Next, in the same file, add the following code:</p>

<pre><code class="language-javascript">&lt;script>
export default {
  name: 'Home'
}
&lt;/script>
</code></pre>

<p>Now, open <code>src/components/About.vue</code> and add the following template:</p>

<pre><code class="language-html">&lt;template>
&lt;ion-app>
&lt;ion-header>
  &lt;ion-toolbar color="primary">
    &lt;ion-title>
      Vue Capacitor | About
    &lt;/ion-title>
  &lt;/ion-toolbar>
&lt;/ion-header>
&lt;ion-content padding>
This is the About page.
&lt;/ion-content>
&lt;/ion-app>
&lt;/template>
</code></pre>

<p>Also, in the same file, add the following code:</p>

<pre><code class="language-javascript">&lt;script>
export default {
  name: 'About'
}
&lt;/script>
</code></pre>

<h4 id="adding-navigation-with-vue-router">Adding Navigation With Vue Router</h4>

<p>Start by installing the Vue router, if it’s not already installed, by running the following command from the root folder of your project:</p>

<pre><code class="language-bash">npm install --save vue-router
</code></pre>

<p>Next, in <code>src/main.js</code>, add the following imports:</p>

<pre><code class="language-javascript">import  Router  from  'vue-router'
import  Home  from  './components/Home.vue'
import  About  from  './components/About.vue'
</code></pre>

<p>This imports the Vue router and the “Home” and “About” components.</p>

<p>Add this:</p>

<pre><code class="language-javascript">Vue.use(Router)
</code></pre>

<p>Create a <code>Router</code> instance with an array of routes:</p>

<pre><code class="language-javascript">const  router  =  new  Router({
routes: [
{
path:  '/',
name:  'Home',
component:  Home
},
{
path:  '/about',
name:  'About',
component:  About
}
]
})
</code></pre>

<p>Finally, tell Vue about the <code>Router</code> instance:</p>

<pre><code class="language-javascript">new  Vue({router,
render:  h  =>  h(App)
}).$mount('#app')
</code></pre>

<p>Now that we’ve set up routing, let’s add some buttons and methods to navigate between our two “Home” and “About” components.</p>

<p>Open <code>src/components/Home.vue</code> and add the following <code>goToAbout()</code> method:</p>

<pre><code class="language-javascript">...
export default {
  name: 'Home',
  methods: {
    goToAbout () {
      this.$router.push('about')
    },
</code></pre>

<p>In the <code>template</code> block, add a button to trigger the <code>goToAbout()</code> method:</p>

<pre><code class="language-html">&lt;ion-button @click="goToAbout" full>Go to About&lt;/ion-button>
</code></pre>

<p>Now we need to add a button to go back to home when we are in the “About” component.</p>

<p>Open <code>src/components/About.vue</code> and add the <code>goBackHome()</code> method:</p>

<pre><code class="language-javascript">&lt;script>
export default {
  name: 'About',
  methods: {
    goBackHome () {
      this.$router.push('/')
    }
  }  
}
&lt;/script>
</code></pre>

<p>And, in the <code>template</code> block, add a button to trigger the <code>goBackHome()</code> method:</p>

<pre><code class="language-html">&lt;ion-button @click="goBackHome()" full>Go Back!&lt;/ion-button>
</code></pre>

<p>When running the application on a real mobile device or emulator, you will notice a scaling issue. To solve this, we need to simply add some <code>meta</code> tags that correctly set the viewport.</p>

<p>In <code>public/index.html</code>, add the following code to the <code>head</code> of the page:</p>

<pre><code class="language-html">&lt;meta name="viewport" content="width=device-width, initial-scale=1.0, minimum-scale=1.0, maximum-scale=1.0, user-scalable=no">
&lt;meta name="format-detection" content="telephone=no">
&lt;meta name="msapplication-tap-highlight" content="no">
</code></pre>

<div id="sponsors-leaderboard-place"></div>


<h3 id="adding-capacitor">Adding Capacitor</h3>

<p>You can use Capacitor in two ways:</p>

<ul>
<li>Create a new Capacitor project from scratch.</li>
<li>Add Capacitor to an existing front-end project.</li>
</ul>


  <div id="sponsors-article" data-impression="true" class="c-promo-box c-promo-box--ad sponsors hidden" data-audience="non-subscriber" data-remove="true"></div>



<p>In this tutorial, we’ll take the second approach, because we created a Vue project first, and now we’ll add Capacitor to our Vue project.</p>

<h4 id="integrating-capacitor-with-vue">Integrating Capacitor With Vue</h4>

<p>Capacitor is designed to be dropped into any modern JavaScript application. To add Capacitor to your Vue web application, you’ll need to follow a few steps.</p>

<p>First, install the Capacitor CLI and core packages from npm. Make sure you are in your Vue project, and run the following command:</p>

<pre><code class="language-bash">$ cd vuecapacitordemo
$ npm install --save @capacitor/core @capacitor/cli
</code></pre>

<p>Next, initialize Capacitor with your app’s information by running the following command:</p>

<pre><code class="language-bash">$ npx cap init
</code></pre>

<p>We are using <code>npx</code> to run Capacitor commands. <code>npx</code> is an utility that comes with  and that is designed to make it easy to run CLI utilities and executables hosted in the npm registry. For example, it allows developers to use locally installed executables without having to use the npm run scripts.</p>

<p>The <code>init</code> command of Capacitor CLI will also add the default native platforms for Capacitor, such as Android and iOS.</p>

<p>You will also get prompted to enter information about your application, such as the name, the application’s ID (which will be mainly used as a package name for the Android application) and the directory of your application.</p>

<p>After you’ve inputted the required details, Capacitor will be added to your Vue project.</p>

<p>You can also provide the application’s details in the command line:</p>

<pre><code class="language-bash">$ npx cap init vuecapacitordemo com.example.vuecapacitordemo
</code></pre>

<p>The application’s name is <code>vuecapacitordemo</code>, and its ID is <code>com.example.vuecapacitordemo</code>. The package name must be a valid Java package name.</p>

<p>You should see a message saying, “Your Capacitor project is ready to go!”</p>

<p>You might also notice that a file named <code>capacitor.config.json</code> has been added to the root folder of your Vue project.</p>

<p>Just like the CLI suggests when we’ve initialized Capacitor in our Vue project, we can now add native platforms that we want to target. This will turn our web application into a native application for each platform that we add.</p>

<p>But just before adding a platform, we need to tell Capacitor where to look for the built files &mdash; that is, the <code>dist</code> folder of our Vue project. This folder will be created when you run the <code>build</code> command of the Vue application for the first time (<code>npm run build</code>), and it is located in the root folder of our Vue project.</p>

<p>We can do that by changing <code>webDir</code> in <code>capacitor.config.json</code>, which is the configuration file for Capacitor. So, simply replace <code>www</code> with <code>dist</code>. Here is the content of <code>capacitor.config.json</code>:</p>

<pre><code class="language-javascript">{
  "appId": "com.example.vuecapacitordemo",
  "appName": "vuecapacitordemo",
  "bundledWebRuntime": false,
  "webDir": "dist"
}
</code></pre>

<p>Now, let’s create the <code>dist</code> folder and build our Vue project by running the following command:</p>

<pre><code class="language-bash">$ npm run build
</code></pre>

<p>After that, we can add the Android platform using the following:</p>

<pre><code class="language-bash">npx cap add android
</code></pre>

<p>If you look in your project, you’ll find that an <code>android</code> native project has been added.</p>

<p>That’s all we need to integrate Capacitor and target Android. If you would like to target iOS or Electron, simply run <code>npx cap add ios</code> or <code>npx cap add electron</code>, respectively.</p>

<h3 id="using-capacitor-plugins">Using Capacitor Plugins</h3>

<p>Capacitor provides a runtime that enables developers to use the three pillars of the web &mdash; HTML, CSS and JavaScript &mdash; to build applications that run natively on the web and on major desktop and mobile platforms. But it also provides a set of plugins to access native features of devices, such as the camera, without having to use the specific low-level code for each platform; the plugin does it for you and provides a normalized high-level API, for that matter.</p>

<p>Capacitor also provides an API that you can use to build custom plugins for the native features not covered by the set of official plugins provided by the Ionic team. You can learn  in the docs.</p>

<p>You can also find more details about available  in the docs.</p>

<h4 id="example-adding-a-capacitor-plugin">Example: Adding a Capacitor Plugin</h4>

<p>Let’s see an example of using a Capacitor plugin in our application.</p>

<p>We’ll use the “Modals” plugin, which is used to show native modal windows for alerts, confirmations and input prompts, as well as action sheets.</p>

<p>Open <code>src/components/Home.vue</code>, and add the following import at the beginning of the <code>script</code> block:</p>

<pre><code class="language-javascript">import { Plugins } from '@capacitor/core';
</code></pre>

<p>This code imports the <code>Plugins</code> class from <code>@capacitor/core</code>.</p>

<p>Next, add the following method to show a dialog box:</p>

<pre><code class="language-javascript">…
  methods: {
    …
    async showDialogAlert(){
      await Plugins.Modals.alert({
          title: 'Alert',
          message: 'This is an example alert box'
      });
    }
</code></pre>

<p>Finally, add a button in the <code>template</code> block to trigger this method:</p>

<pre><code class="language-html">&lt;ion-button @click="showDialogAlert" full>Show Alert Box&lt;/ion-button>
</code></pre>

<p>Here is a screenshot of the dialog box:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1c9a76fc-9f6c-405a-b3b5-f39af7c07eda/capacitor-modal-box.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1c9a76fc-9f6c-405a-b3b5-f39af7c07eda/capacitor-modal-box.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1c9a76fc-9f6c-405a-b3b5-f39af7c07eda/capacitor-modal-box.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1c9a76fc-9f6c-405a-b3b5-f39af7c07eda/capacitor-modal-box.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1c9a76fc-9f6c-405a-b3b5-f39af7c07eda/capacitor-modal-box.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1c9a76fc-9f6c-405a-b3b5-f39af7c07eda/capacitor-modal-box.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1c9a76fc-9f6c-405a-b3b5-f39af7c07eda/capacitor-modal-box.png"
			sizes="70vw"
			alt="Capacitor native modal box"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			A native modal box ()
		</figcaption>
	
</figure>


<p>You can find more details .</p>

<h4 id="building-the-app-for-target-platforms">Building the App for Target Platforms</h4>

<p>In order to build your project and generate a native binary for your target platform, you’ll need to follow a few steps. Let’s first see them in a nutshell:</p>

<ol>
<li>Generate a production build of your Vue application.</li>
<li>Copy all web assets into the native project (Android, in our example) generated by Capacitor.</li>
<li>Open your Android project in Android Studio (or Xcode for iOS), and use the native integrated development environment (IDE) to build and run your application on a real device (if attached) or an emulator.</li>
</ol>

<p>So, run the following command to create a production build:</p>

<pre><code class="language-bash">$ npm run build
</code></pre>

<p>Next, use the <code>copy</code> command of the Capacitor CLI to copy the web assets to the native project:</p>

<pre><code class="language-bash">$ npx cap copy
</code></pre>

<p>Finally, you can open your native project (Android, in our case) in the native IDE (Android Studio, in our case) using the <code>open</code> command of the Capacitor CLI:</p>

<pre><code class="language-bash">$ npx cap open android
</code></pre>

<p>Either Android Studio will be opened with your project, or the folder that contains the native project files will be opened.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d74af403-7ae3-4c55-a216-10eac8f29ee6/android-studio-project.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d74af403-7ae3-4c55-a216-10eac8f29ee6/android-studio-project.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d74af403-7ae3-4c55-a216-10eac8f29ee6/android-studio-project.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d74af403-7ae3-4c55-a216-10eac8f29ee6/android-studio-project.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d74af403-7ae3-4c55-a216-10eac8f29ee6/android-studio-project.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d74af403-7ae3-4c55-a216-10eac8f29ee6/android-studio-project.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d74af403-7ae3-4c55-a216-10eac8f29ee6/android-studio-project.png"
			sizes="100vw"
			alt="Android Studio project"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Capacitor project opened in Android Studio ()
		</figcaption>
	
</figure>


<p>If that doesn’t open Android Studio, then simply open your IDE manually, go to “File” &rarr; “Open…”, then navigate to your project and open the <code>android</code> folder from within the IDE.</p>

<p>You can now use Android Studio to launch your app using an emulator or a real device.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/578d5e2e-a2e2-4b47-a758-a9a9946d489f/capacitor-demo.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/578d5e2e-a2e2-4b47-a758-a9a9946d489f/capacitor-demo.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/578d5e2e-a2e2-4b47-a758-a9a9946d489f/capacitor-demo.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/578d5e2e-a2e2-4b47-a758-a9a9946d489f/capacitor-demo.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/578d5e2e-a2e2-4b47-a758-a9a9946d489f/capacitor-demo.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/578d5e2e-a2e2-4b47-a758-a9a9946d489f/capacitor-demo.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/578d5e2e-a2e2-4b47-a758-a9a9946d489f/capacitor-demo.png"
			sizes="70vw"
			alt="Capacitor demo project"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Capacitor demo project ()
		</figcaption>
	
</figure>


<h3 id="conclusion">Conclusion</h3>

<p>In this tutorial, we’ve used Ionic Capacitor with Vue and Ionic 4 web components to create a mobile Android application with web technologies. You can find the source code of the demo application we’ve created throughout this tutorial in the .</p>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(lf, ra, yk, al)</span>
</div>


              </article>
            </body>
          </html>
---------------
<h1 id="#title_1" >2、文章： 太平洋保险CIMS系统微前端实践</h1>
黄超
[http://www.infoq.com/cn/articles/cpic-cims-micro-frontend-practice?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/cpic-cims-micro-frontend-practice?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/cpic-cims-micro-frontend-practice/zh/smallimage/GettyImages-499691816-copy-1530377097284.jpeg"/><p>微前端的概念最早由 ThoughtWorks 在 2016 年底提出，是一种将微服务推广到前端的设计理念。（https://micro-frontends.org/），目前的趋势是构建一个功能丰富且功能强大的浏览器应用程序，也就是位于微服务架构之上的单页应用程序（SPA）。</p> <i>By 黄超</i>
---------------
<h1 id="#title_2" >3、视频演讲： serverless小程序后端技术分享</h1>
黄文俊
[http://www.infoq.com/cn/presentations/serverless-applet-backend-technology-sharing?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/serverless-applet-backend-technology-sharing?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/presentations/serverless-applet-backend-technology-sharing/zh/mediumimage/huangwenjun270-1530460757982.jpg"/><p>小程序、小游戏的开发已经越来越火爆，而小程序或者小游戏的后台，通常还是按照传统的服务器模式，提供-API-作为后端服务入口进行开发。本次沙龙将会详细讲解如何通过serverless-架构，结合使用-api-网关、云函数、云数据库，实现无需关心服务器、自动实现高并发、并且能够快速上线和无缝更新服务的小程序后端解决方案。</p> <i>By 黄文俊</i>
---------------
<h1 id="#title_3" >4、谷歌Fuchsia操作系统将支持运行Linux应用程序</h1>
Eric Brown
[http://www.infoq.com/cn/news/2018/07/Fuchsia-Linux-available?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/Fuchsia-Linux-available?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>谷歌的非Linux家族操作系统Fuchsia OS增加了一个用于运行Debian Linux应用程序的模拟器。与即将推出的适用于Chrome OS的Linux模拟器一样，相比传统的模拟器，Fuchsia的“Guest” App与宿主操作系统集成得更加紧密。</p> <i>By Eric Brown</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_4" >5、文章： BuzzFeed如何从Perl单体应用迁移到Go和Python微服务</h1>
Charles Humble
[http://www.infoq.com/cn/articles/buzzfeed-microservices-migration?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/buzzfeed-microservices-migration?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/buzzfeed-microservices-migration/zh/smallimage/BuzzFeed_Arrow-final-1528989561770-1530370500394.jpg"/><p>2016年，BuzzFeed启动了一个重构项目，把使用Perl编写的一个单体应用程序转换成一组微服务。他们之所以这样做，主要是因为Perl应用程序被证明很难扩展，使buzzfeed.com独自服务于每月大约70亿次页面访问。</p> <i>By Charles Humble</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_5" >6、FEX 技术周刊 - 2018/07/02</h1>

[http://fex.baidu.com/blog/2018/07/fex-weekly-02//](http://fex.baidu.com/blog/2018/07/fex-weekly-02//)
作者：nwind <br> <h2 id="section">深阅读</h2>

<p><strong>JavaScript Usage by Industry</strong><br />
https://blog.npmjs.org/post/175311966445/javascript-usage-by-industry<br />
We’re continuing our analysis of the results of last winter’s JavaScript Ecosystem Survey, a survey of over 16,000 developers conducted by npm in collaboration with the Node.JS Foundation and the JS Foundation. Our second topic is How JavaScript is used across industries — and, more specifically, how different industries use certain JavaScript tools, frameworks, and practices. To read more about the methodology behind this survey, click .</p>

<p><strong>Standard ECMA-262 ECMAScript® 2018 Language Specification</strong><br />
https://www.ecma-international.org/publications/standards/Ecma-262.htm<br />
The official spec for ES2018 (essentially the 9th edition of the JS spec) has been published. 附：</p>

<p><strong>On Consuming (and Publishing) ES2015+ Packages</strong><br />
https://babeljs.io/blog/2018/06/26/on-consuming-and-publishing-es2015+-packages<br />
For those of us that need to support older browsers, we run a compiler like Babel over application code. But that’s not all of the code that we ship to browsers; there’s also the code in our node_modules. Can we make compiling our dependencies not just possible, but normal? The ability to compile dependencies is an enabling feature request for the whole ecosystem. Starting with some of the changes we made in Babel v7 to make selective dependency compilation possible, we hope to see it standardized moving forward.</p>

<p><strong>Write Perfect Code with Standard and ESLint</strong><br />
https://www.youtube.com/watch?v=arNtoWxBuXc<br />
In this talk, Feross Aboukhadijeh explains about code linting – how to use Standard and ESLint to catch programmer errors before they cause problems for your users. We’ll discuss how to get started with linting, as well as how to improve your setup if you’re already linting your code.</p>

<p><strong>GUI Testing Powered by Deep Learning</strong><br />
https://www.ebayinc.com/stories/blogs/tech/gui-testing-powered-by-deep-learning/<br />
Contemporary developments in DL unleashes efficiencies in GUI testing and in the software lifecycle, potentially. A recent pilot, described below, proved this approach to be realistic and practical. 另附：</p>

<p><strong>美团外卖iOS多端复用的推动、支撑与思考</strong><br />
https://tech.meituan.com/iOS_multiterminal_reuse.html<br />
提到多端复用，不免与组件化产生联系，可以说组件化是多端复用的必要条件之一。大多数公司口中的“组件化”仅仅做到代码分库，使用Cocoapods的Podfile来管理，再在主工程把各个子库的版本号聚合起来。但是能设计一套合理的分层架构，理清依赖关系，并有一整套工具链支撑组件发版与集成的相对较少。否则组件化只会导致包体积增大，开发效率变慢，依赖关系复杂等副作用。</p>

<p><strong>从天河2号到阿里云超算，P9技术大牛的职业发展智慧</strong><br />
https://mp.weixin.qq.com/s?__biz=MjM5MDE0Mjc4MA==&amp;mid=2651007990&amp;idx=1&amp;sn=b8bf7d5a912d8ba6a65c7ffa6cd78835<br />
技术更迭速度之快，经常让处在高新技术行业的程序员们感到焦虑和恐慌，生怕一松懈就被这个时代无情地抛弃。在极客 Live，阿里云超算的负责人何万青老师分享了他的职业发展智慧。他更愿意称自己是“软件工程师”，不喜欢“码农”、“程序员”的称谓；他说技术人要找到自己的无穷大∞，而不应该把时间浪费在已经饱和的事情上；他说技术人的年龄是会增长的，如果只是年龄变化，其他不变，就会被替换掉。</p>

<p><strong>[译]Web前端框架：是解药还是毒药</strong><br />
https://mp.weixin.qq.com/s?__biz=MzUxMzcxMzE5Ng==&amp;mid=2247489138&amp;idx=1&amp;sn=8b130c0ed1c972acdb3f9af5286aee08<br />
要使用现代的前端框架，你需要下载开发环境和依赖，编译代码，然后在浏览器上运行。这个是好是坏？究竟是什么导致了这种不必要的复杂性？是因为我们构建的网站太复杂，还是因为框架本身就很复杂？</p>

<p><strong>Should we use React Native?</strong><br />
https://blog.expo.io/should-we-use-react-native-1465d8b607ac<br />
Watching tens of thousands of developers consider using React Native and talking to many of them, I’ve found that teams considering React Native fall roughly into three broad categories, where two of them are very likely to be successful and happy using React Native, and the other one is usually a bad time. Should I use React Native in my project? Here’s a quick guide that might help you and your team make a decision about whether React Native is a good choice for you.</p>

<p><strong>Building browser extensions with React</strong><br />
https://www.rubberduck.io/blog/browser-extensions-react/<br />
We build Rubberduck, a browser extension that adds IDE features (find usages, definitions, files tree) to GitHub web pages. Our users use it to read and review code faster on the web. We built Rubberduck on React, and we wanted to share our create-react-app setup for extension projects.</p>

<p><strong>The best react inline style libraries — comparing Radium, Aphrodite, &amp; Emotion</strong><br />
https://blog.logrocket.com/the-best-react-inline-style-libraries-comparing-radium-aphrodite-emotion-849ef148c473<br />
This article is about inline styles. However, I’m not going to talk about what they are or whether you should use them or not. I’m going to talk about libraries that will help you use inline styles in your React application — libraries that allow you to use features that are not directly supported otherwise (like media queries). I’ll compare: Radium, Aphrodite, Emotion.</p>

<p><strong>Drawing Images with CSS Gradients</strong><br />
https://css-tricks.com/drawing-images-with-css-gradients/<br />
What I mean by “CSS images” is images that are created using only HTML elements and CSS. They look as if they were SVGs drawn in Adobe Illustrator but they were made right in the browser. Some techniques I’ve seen used are tinkering with border radii, box shadows, and sometimes clip-path.  Let’s take a look at how you can create CSS images that way yourself.</p>

<p><strong>Threads in Node 10.5.0: a practical intro</strong><br />
https://medium.com/dailyjs/threads-in-node-10-5-0-a-practical-intro-3b85a0a3c953<br />
A few days ago, version 10.5.0 of Node.js was released and one of the main features it contained was the addition of initial (and experimental) thread support. This is interesting, specially coming from a language that’s always pride itself of not needed threads thanks to it’s fantastic async I/O. So why would we need threads in Node?</p>

<p><strong>How to build powerful REST APIs blazingly fast with Node.js</strong><br />
https://resthapi.com/blog/2018/06/26/How-To-Build-Powerful-APIs-Blazingly-Fast-With-Nodejs.html<br />
EST APIs in particular are very common place. Unfortunately when it comes to the wild west world of Javascript and Node.js, standards and good practice in writing RESTful APIs can sometimes get thrown out the window. 另附：</p>

<p><strong>Build a Video Chat Service with JavaScript, WebRTC, and Okta</strong><br />
https://scotch.io/tutorials/build-a-video-chat-service-with-javascript-webrtc-and-okta<br />
Today, I thought it’d be fun to walk you through the process of using WebRTC and Okta to build a simple video chat service that allows users to create a chatroom and share the link around to anyone they want who can then join the room and chat with them in real-time.</p>

<p><strong>Web Assembly and Go: A look to the future</strong><br />
https://brianketelsen.com/web-assembly-and-go-a-look-to-the-future/<br />
When Web Assembly(wasm) support landed in Go recently, I knew that the time was ripe for some experimentation. And I couldn’t wait to dive in and try it. I read a few good articles before diving in. This post will chronicle my experience. 另附：.</p>

<p><strong>The C4 Model for Software Architecture</strong><br />
https://www.infoq.com/articles/C4-architecture-model<br />
C4 stands for context, containers, components, and code — a set of hierarchical diagrams that you can use to describe your software architecture at different zoom levels, each useful for different audiences. Think of it as Google Maps for your code.</p>

<p><strong>Migrating Messenger storage to optimize performance</strong><br />
https://code.fb.com/core-data/migrating-messenger-storage-to-optimize-performance/<br />
More than a billion people now use Facebook Messenger to instantly share text, photos, video, and more. As we have evolved the product and added new functionality, the underlying technologies that power Messenger have changed substantially. When Messenger was originally designed, it was primarily intended to be a direct messaging product similar to email, with messages waiting in your inbox the next time you visited the site. Today, Messenger is a mobile-first, real-time communications system used by businesses as well as individuals. To enable that shift, we have made many changes through the years to update the backend system.</p>

<p><strong>Refactoring Thrift schemas at Pinterest</strong><br />
https://medium.com/@Pinterest_Engineering/refactoring-thrift-schemas-at-pinterest-e899008ce22b<br />
The tight coupling of the files has not only created a web of tangled dependencies among the Thrift files, but also among the applications that use them. This leads to a slow and error-prone development cycle, slowing down developer velocity across the company. To address this problem, we recently refactored our Thrift schemas, leading to a huge reduction in code build times while improving code quality and developer velocity. In this blog post, we’ll share our motivation for the project, our approach to solving the problem and the wins we’ve observed.</p>

<p><strong>How not to structure your database-backed web applications: a study of performance bugs in the wild</strong><br />
https://blog.acolyer.org/2018/06/28/how-_not_-to-structure-your-database-backed-web-applications-a-study-of-performance-bugs-in-the-wild/<br />
This is a fascinating study of the problems people get into when using ORMs to handle persistence concerns in their web applications. The authors study real-world applications and distil a catalogue of common performance anti-patterns. There are a bunch of familiar things in the list, and a few that surprised me with the amount of difference they can make. By fixing many of the issues that they find, Yang et al., are able to quantify how many lines of code it takes to address the issue, and what performance improvement the fix delivers.</p>

<p><strong>Python 3 at Facebook</strong><br />
https://lwn.net/SubscriberLink/758159/f1f631e1535ab9d6/<br />
Python 3 adoption has clearly picked up over the last few years, though there is still a long way to go. Big Python-using companies tend to have a whole lot of Python 2.7 code running on their infrastructure and Facebook is no exception. But Jason Fried came to PyCon 2018 to describe what has happened at the company over the last four years or so—it has gone from using almost no Python 3 to it becoming the dominant version of Python in the company. He was instrumental in helping to make that happen and his  may provide other organizations with some ideas on how to tackle their migration.</p>

<h2 id="section-1">新鲜货</h2>

<p><strong>Augmented reality for the web</strong><br />
https://developers.google.com/web/updates/2018/06/ar-for-the-web<br />
In Chrome 67, we </p>

<p><strong>MongoDB 4.0 Now Generally Available</strong><br />
https://www.mongodb.com/mongodb-4.0<br />
MongoDB 4.0 is out with multi-document ACID transaction support being the headline feature. This landing page gives you access to the , downloads, a white paper, the press release, and more. 附：<a href="https://www.mongodb.com/blog/post/mongodb-multi-document-acid-transactions-general-availability">
MongoDB Multi-Document ACID Transactions are GA</a>、.</p>

<p><strong>We’re moving from Azure to Google Cloud Platform</strong><br />
https://about.gitlab.com/2018/06/25/moving-to-gcp/<br />
GitLab.com is migrating to Google Cloud Platform – here’s what this means for you now and in the future. 另附：</p>

<p><strong>Firefox 61 – Quantum of Solstice</strong><br />
https://hacks.mozilla.org/2018/06/firefox-61-quantum-of-solstice/<br />
Parallel CSS Parsing, Retained Display Lists, Accessibility Inspector… 另附：</p>

<p><strong>Trending Repositories of June on GitHub</strong><br />
https://codeburst.io/trending-repositories-of-june-on-github-bdbf90837bc6<br />
Deno, Javascript algorithms, Build your own X, Awesome design patterns… 另附：</p>

<p><strong>Font Awesome 5.1: 409 New Icons + More</strong><br />
https://blog.fontawesome.com/font-awesome-5-1-409-new-icons-more-4c1e407fae49<br />
We’ve packed new icon categories, new icons, and lots of fixes under the hood to add power and ease when using our icons. You’ve got 409 new icons waiting for you. That makes more than 1,000 icons added to Font Awesome already this year!</p>

<p><strong>React Developer Roadmap</strong><br />
https://github.com/adam-golab/react-developer-roadmap<br />
Below you can find a chart demonstrating the paths that you can take and the libraries that you would want to learn in order to become a React developer. I made this chart for all people who encounter me with question “What should I learn next as a React developer?” to give them some tips.</p>

<p><strong>react-day-picker</strong><br />
https://github.com/gpbl/react-day-picker<br />
Flexible date picker component for React. Highly customizable, localizable, with ARIA support, no external dependencies, 9KB gzipped.</p>

<p><strong>vuetify</strong><br />
https://github.com/vuetifyjs/vuetify<br />
Material Component Framework for Vue.js. Vuetify is a semantic component framework for Vue. It aims to provide clean, semantic and reusable components that make building your application a breeze. Build amazing applications with the power of Vue and Material Design and a massive library of beautifully crafted components.</p>

<p><strong>Gio.js</strong><br />
https://github.com/syt123450/giojs<br />
Gio.js is an open source library for web 3D globe data visualization built with Three.js. What makes Gio.js different is that it is simple to use Gio.js to customize a 3D data visualization model in a declarative way, add your own data, and integrate it into your own modern web application. 另附：</p>

<p><strong>Docz</strong><br />
https://www.docz.site/<br />
It has never been so easy to document your things! To break barriers and facilitate the creation of tools was the purpose that Docz arose. Document our things is one of the most important and painful process that exist when you’re creating something new. We lose a lot of our precious time with unnecessary setups to be able to build something that can represent and express what we want with our own style.</p>

<p><strong>MeQ</strong><br />
https://github.com/meqio/meq<br />
A modern messaging platform for Message Push、IM、Group Chatting、IoT etc, based on MQTT protocol. MeQ is written in pure go and standard library,nearly no messy dependencies. so you can easily deploy a standalone binary in linux、unix、macos、windows.</p>

<p><strong>DevTube</strong><br />
https://dev.tube/<br />
The best developer videos in one place</p>

<p><strong>Mastodon</strong><br />
https://www.joinmastodon.org/<br />
Social networking, back in your hands. The world’s largest free, open-source, decentralized microblogging network. 附：</p>

<h2 id="section-2">设计</h2>

<p><strong>Sketch插件Kitchen深度体验</strong><br />
https://uiiiuiii.com/software/80342.html<br />
听说它能帮你节省50%的低效时间。「Kitchen」是蚂蚁金服体验科技发布最新的 Sketch 工具集，支持设计稿快速同步协作；快速配置表格、按钮、分页等 Ant Design 组件；提供精选色板，并可以管理属于你的色板库；接入海量 Iconfont 图标资源，可拖拽修改图标。本着认真负责的态度，这次测评将会从这款插件的各个功能入手，通过实际体验告诉你到底好不好用。</p>

<p><strong>How To Get To Know Your Users</strong><br />
https://www.smashingmagazine.com/2018/06/how-to-get-to-know-your-users/<br />
This article will look at how going below the surface during user research helps us really understand what triggers our users, and how those deeper insights will help us design for persuasion.</p>

<p><strong>The Philosophy in Games</strong><br />
https://blog.prototypr.io/the-philosophy-in-games-e7faef8f9213<br />
What can philosophy and games teach us about Life?</p>

<p><strong>Designing for accessibility is not that hard</strong><br />
https://uxdesign.cc/designing-for-accessibility-is-not-that-hard-c04cc4779d94<br />
Seven easy-to-implement guidelines to design a more accessible web</p>

<p><strong>The most important steps to becoming a great design leader</strong><br />
https://www.invisionapp.com/blog/most-important-steps-becoming-great-design-leader/<br />
Most designers, when presented with a leadership opportunity, leap into the role enthusiastically, unaware of the challenges ahead. That’s what an opportunity is, right? A new, uncharted frontier full of mystery and the just right set of circumstances?</p>

<p><strong>10 Small Design Mistakes We Still Make</strong><br />
https://uxplanet.org/10-small-design-mistakes-we-still-make-1cd5f60bc708<br />
Don’t Make Me Think by Steve Krug. 另附：.</p>

<h2 id="section-3">产品及其它</h2>

<p><strong>What 7 Creepy Patents Reveal About Facebook</strong><br />
https://www.nytimes.com/interactive/2018/06/21/opinion/sunday/facebook-patents-privacy.html<br />
Here are seven Facebook patent applications that show how the company has contemplated gathering and exploiting your personal information.</p>

<p><strong>Interactive maps, now in your language</strong><br />
https://blog.wikimedia.org/2018/06/28/interactive-maps-now-in-your-language/<br />
Imagine you needed to learn about a foreign land, but the only map you had was written in a mysterious script you couldn’t read. That might sound like a plot twist from some adventure story, but it’s actually the situation visitors to Wikimedia projects—including Wikipedia—often found themselves in until recently. An extension called Kartographer enables Wikimedians to create interactive maps simply by supplying the longitude and latitude of a location.</p>

<p><strong>微信的操作系统之路</strong><br />
https://mp.weixin.qq.com/s?__biz=MjM5NzYxMzk4MQ==&amp;mid=2649331233&amp;idx=1&amp;sn=bfa719f584315a047b4a4d68a5efa4c1<br />
这些年来，中国互联网很少有像微信这样影响巨大的产品。因此，今天我想基于微信发展过程中的关键决策，提供一些思考。我会从四个部分分析它： 1）用户在微信发展早期对它的定位：聊天工具; 2）本周引发最多讨论的问题：朋友圈和公众号的内容生态; 3）微信的商业化探索。2013 年腾讯年会，总裁刘炽平喊出了这个口号：微信商业化的元年到了; 4）最后，微信有好几年没有动作，满世界都在说微信老了，于是才有今天的第四部分：小程序.</p>

<p><strong>Google 和央美合作，把徐悲鸿的 200 件画作搬到了线上</strong><br />
http://www.geekpark.net/news/230408<br />
科技和艺术文化的交融已经成了一个绕不开的话题，Google 也有这样一个非营利性的项目，叫 Google Arts &amp; Culture，简单来说就是把艺术文化作品数字化，搬到线上，还用 VR 等技术加深用户的观赏体验。去年 12 月，Google Arts &amp; Culture 和故宫合作，把故宫博物院的几百件珍宝做了线上高清处理，同时开展了一系列策展活动，这对中国艺术的传承和传播有着很重要的意义。2018 年 6 月 19 日，在中央美术学院 100 周年校庆之际，Google Arts &amp; Culture 又和中央美院的美术馆进行合作，上线了一系列馆内珍藏的艺术作品。</p>

<p>– THE END –</p>
---------------
<h1 id="#title_6" >7、Linus 说工程师要爱上“ 无聊” ，Zemlin 说开源不是零和游戏，华为说真正的价值在于有多少人用这个东西| LC3 2018</h1>
杨赛
[http://www.infoq.com/cn/news/2018/07/Zemlin-LC3-2018?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/Zemlin-LC3-2018?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>2018 年6 月25 日-27 日，LC3 大会（LinuxCon + ContainerCon + CloudOpen ）第二次来到中国。相关的中文站记者对三天的大会进行了观察，与读者们分享一些摘要与感想。</p> <i>By 杨赛</i>
---------------
<h1 id="#title_7" >8、文章： 改进GitHub工作流的15个建议</h1>
Gaboesquivel
[http://www.infoq.com/cn/articles/15-recommendations-to-enhance-your-github-flow?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/15-recommendations-to-enhance-your-github-flow?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/15-recommendations-to-enhance-your-github-flow/zh/smallimage/devops-logo-1530549046597.jpg"/><p>这篇文章介绍了最为高效和实用的GitHub开发流程，它可以被用在各种软件开发项目上，开发出高质量的软件。</p> <i>By Gaboesquivel</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_8" >9、ML.NET 0.2版增加了集群和新示例</h1>
Jeff Martin
[http://www.infoq.com/cn/news/2018/07/mlnet02-released?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/mlnet02-released?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>微软发布的ML.NET是一个运行在.NET核心上的多平台机器学习框架。它的第一版是在5月的Build大会上发布的，第二版增加了几个新功能，并发布了一个单独的GitHub repo，演示了如何使用这个框架。</p> <i>By Jeff Martin</i> <i> Translated by 陈亮芬</i>
---------------
<h1 id="#title_9" >10、与专门团队一起持续交付</h1>
Manuel Pais
[http://www.infoq.com/cn/news/2018/07/enabling-continuous-delivery?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/enabling-continuous-delivery?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>BCG Digital Ventures的首席工程师Robin Weston 最近在伦敦持续生命周期大会（Continuous Lifecycle London）上发布了一份经验报告，在该报告中称，外部支持团队能够在难以实施变化的组织和封闭的团队中引入持续交付(CD)实践。该团队不只是引入新的技术和工具，而更专注于分享良好的实践和团队教育。实践范围从持续集成到遵循测试金字塔，或者通过活动度量和识别浪费来减少周期时间。</p> <i>By Manuel Pais</i> <i> Translated by 冬雨</i>
---------------
<h1 id="#title_10" >11、Microsoft Edge现已支持W3C WebDriver建议</h1>
Dylan Schiemann
[http://www.infoq.com/cn/news/2018/06/microsoft-edge-w3c-webdriver?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/06/microsoft-edge-w3c-webdriver?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Microsoft Edge现已支持最近批准的W3C WebDriver建议，这将使Edge更易于实现单元测试和功能测试自动化。Edge WebDriver现在以成为Edge的一个FoD（按需添加特性，Feature on Demand），今后每次Edge发布将提供自动WebDriver更新。</p> <i>By Dylan Schiemann</i> <i> Translated by 盖磊</i>
---------------
<h1 id="#title_11" >12、TLBleed漏洞：通过探测TLB获取CPU秘钥</h1>
Sergio De Simone
[http://www.infoq.com/cn/news/2018/06/tlbleed-vulnerability-tlb-intel?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/06/tlbleed-vulnerability-tlb-intel?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>VUsec安全研究员Ben Gras在一篇文章中写道，一个影响英特尔处理器的边信道漏洞（称为TLBleed）可能通过窥探翻译后援缓冲器（TLB）泄漏信息。
</p> <i>By Sergio De Simone</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_12" >13、文章： 使用Apache Kafka和KSQL实现普及化流处理</h1>
Michael Noll
[http://www.infoq.com/cn/articles/democratizing-stream-processing-apache-kafka-ksql?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/democratizing-stream-processing-apache-kafka-ksql?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/democratizing-stream-processing-apache-kafka-ksql/zh/smallimage/kafka-streaming-logo-2-1528901042755-1530369903080.jpg"/><p>本文作者Michael Noll介绍了如何使用KSQL实现流处理。KSQL是Apache Kafka的数据流SQL引擎。本文内容涵盖了有状态流处理中的挑战、KSQL是如何解决这些挑战的，以及KSQL是如何通过流和表构建了流数据和数据库之间的桥梁。
</p> <i>By Michael Noll</i> <i> Translated by 盖磊</i>
---------------
<h1 id="#title_13" >14、文章： Kylin在滴滴OLAP引擎中的应用</h1>
滴滴数据平台团队
[http://www.infoq.com/cn/articles/kylin-in-didi-olap-engine?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/kylin-in-didi-olap-engine?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/kylin-in-didi-olap-engine/zh/smallimage/GettyImages-683951840-1530378629014.jpg"/><p>滴滴 OLAP 引擎细分多种场景，如灵活分析、固化分析、热点数据等，针对不同场景的特性，使用不同的场景引擎。Apache Kylin 作为滴滴 OLAP 引擎内部的固化分析场景引擎，间接服务了滴滴下游多个重要的数据产品，覆盖了十多条业务线，为用户提供了稳定、可靠、高效的数据分析性能。</p> <i>By 滴滴数据平台团队</i>
---------------