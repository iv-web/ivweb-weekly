## 文章索引
1、 <a href="#1谷歌推出最新angularjs升级工具可快速迁移至angular" >谷歌推出最新AngularJS升级工具，可快速迁移至Angular</a><br/>
2、 <a href="#2building-a-room-detector-for-iot-devices-on-mac-os" >Building A Room Detector For IoT Devices On Mac OS</a><br/>
3、 <a href="#3文章-使用服务网格提高安全性christian-posta带你探索istio的新功能" >文章： 使用服务网格提高安全性：Christian Posta带你探索Istio的新功能</a><br/>
4、 <a href="#4文章-推荐30个用于微服务的顶级工具" >文章： 推荐30个用于微服务的顶级工具</a><br/>
5、 <a href="#5文章-上交大提出支持并行计算的srnn比rnn快136倍代码已开源" >文章： 上交大提出支持并行计算的SRNN：比RNN快136倍！（代码已开源）</a><br/>
6、 <a href="#6视频演讲-玩转cos对象存储与scf深度结合应用" >视频演讲： 玩转COS：对象存储与SCF深度结合应用</a><br/>
7、 <a href="#7从摩尔定律到人工智能指数定律释放人类潜能" >从摩尔定律到人工智能，指数定律释放人类潜能</a><br/>
8、 <a href="#8微软将开源其对抗云网络中断的秘密武器" >微软将开源其对抗云网络中断的秘密武器</a><br/>
9、 <a href="#9全球物流无人机发展报告前景广阔未来三年为关键期" >全球物流无人机发展报告：前景广阔，未来三年为关键期</a><br/><h1 id="#title_0" >1、谷歌推出最新AngularJS升级工具，可快速迁移至Angular</h1>
覃云
[http://www.infoq.com/cn/news/2018/08/new-AngularJS-updatetools?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/08/new-AngularJS-updatetools?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>众所周知，AngularJS和Angular虽说是一脉相承，但其实是两个不同的产品：AngularJS指的是Angular 2.0之前（即AngularJS 1.x）的版本，Angular指Angular 2.0之后的版本，由于Angular 不兼容AngularJS，这让很多用AngularJS的开发者感觉被谷歌抛弃了，纷纷转向其他的框架，而坚持使用Angular的开发者也开始了迁移之路。</p> <i>By 覃云</i>
---------------
<h1 id="#title_1" >2、Building A Room Detector For IoT Devices On Mac OS</h1>
Alvin Wan
[https://www.smashingmagazine.com/2018/08/building-room-detector-iot-devices-mac-os/](https://www.smashingmagazine.com/2018/08/building-room-detector-iot-devices-mac-os/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/08/building-room-detector-iot-devices-mac-os/" />
              <title>Building A Room Detector For IoT Devices On Mac OS</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>Building A Room Detector For IoT Devices On Mac OS</h1>
                  
                    
                    <address>Alvin Wan</address>
                  
                  <time datetime="2018-08-29T14:20:53&#43;02:00" class="op-published">2018-08-29T14:20:53+02:00</time>
                  <time datetime="2018-08-29T18:41:58&#43;00:00" class="op-modified">2018-08-29T18:41:58+00:00</time>
                </header>
                

<p>Knowing which room you’re in enables various IoT applications &mdash; from turning on the light to changing TV channels. So, how can we detect the moment you and your phone are in the kitchen, or bedroom, or living room? With today’s commodity hardware, there are a myriad of possibilities:</p>

<p>One solution is to <strong>equip each room with a bluetooth device</strong>. Once your phone is within range of a bluetooth device, your phone will know which room it is, based on the bluetooth device. However, maintaining an array of Bluetooth devices is significant overhead &mdash; from replacing batteries to replacing dysfunctional devices. Additionally, proximity to the Bluetooth device is not always the answer: if you’re in the living room, by the wall shared with the kitchen, your kitchen appliances should not start churning out food.</p>

<p>Another, albeit impractical, solution is to <strong>use GPS</strong>. However, keep in mind hat GPS works poorly indoors in which the multitude of walls, other signals, and other obstacles wreak havoc on GPS’s precision.</p>

<p>Our approach instead is to <strong>leverage all in-range WiFi networks</strong> &mdash; even the ones your phone is not connected to. Here is how: consider the strength of WiFi A in the kitchen; say it is 5. Since there is a wall between the kitchen and the bedroom, we can reasonably expect the strength of WiFi A in the bedroom to differ; say it is 2. We can exploit this difference to predict which room we’re in. What’s more: WiFi network B from our neighbor can only be detected from the living room but is effectively invisible from the kitchen. That makes prediction even easier. In sum, the list of all in-range WiFi gives us plentiful information.</p>

<p>This method has the distinct advantages of:</p>

<ol>
<li>not requiring more hardware;</li>
<li>relying on more stable signals like WiFi;</li>
<li>working well where other techniques such as GPS are weak.</li>
</ol>

<p>The more walls the better, as the more disparate the WiFi network strengths, the easier the rooms are to classify. You will build a simple desktop app that collects data, learns from the data, and predicts which room you’re in at any given time.</p>

<h4><span class="rh">Further Reading</span> on SmashingMag:</h4>

<ul>
<li></li>
<li></li>
<li></li>
<li></li>
</ul>

<h3 id="prerequisites">Prerequisites</h3>

<p>For this tutorial, you will need a Mac OSX. Whereas the code can apply to any platform, we will only provide dependency installation instructions for Mac.</p>

<ul>
<li>Mac OSX</li>
<li>Homebrew, a package manager for Mac OSX. To install, copy-and-paste the command at </li>
<li>Installation of NodeJS 10.8.0+ and npm</li>
<li>Installation of Python 3.6+ and pip. See the first 3 sections of </li>
</ul>



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




<h3 id="step-0-setup-work-environment">Step 0: Setup Work Environment</h3>

<p>Your desktop app will be written in NodeJS. However, to leverage more efficient computational libraries like <code>numpy</code>, the training and prediction code will be written in Python. To start, we will setup your environments and install dependencies. Create a new directory to house your project.</p>

<pre><code class="language-bash">mkdir ~/riot
</code></pre>

<p>Navigate into the directory.</p>

<pre><code class="language-bash">cd ~/riot
</code></pre>

<p>Use pip to install Python’s default virtual environment manager.</p>

<pre><code class="language-bash">sudo pip install virtualenv
</code></pre>

<p>Create a Python3.6 virtual environment named <code>riot</code>.</p>

<pre><code class="language-bash">virtualenv riot --python=python3.6
</code></pre>

<p>Activate the virtual environment.</p>

<pre><code class="language-bash">source riot/bin/activate
</code></pre>

<p>Your prompt is now preceded by <code>(riot)</code>. This indicates we have successfully entered the virtual environment. Install the following packages using <code>pip</code>:</p>

<ul>
<li><code>numpy</code>: An efficient, linear algebra library</li>
<li><code>scipy</code>: A scientific computing library that implements popular machine learning models</li>
</ul>

<pre><code class="language-bash">pip install numpy==1.14.3 scipy
==1.1.0
</code></pre>

<p>With the working directory setup, we will start with a desktop app that records all WiFi networks in-range. These recordings will constitute training data for your machine learning model. Once we have data on hand, you will write a least squares classifier, trained on the WiFi signals collected earlier. Finally, we will use the least squares model to predict the room you’re in, based on the WiFi networks in range.</p>

<h3 id="step-1-initial-desktop-application">Step 1: Initial Desktop Application</h3>

<p>In this step, we will create a new desktop application using Electron JS. To begin, we will instead the Node package manager <code>npm</code> and a download utility <code>wget</code>.</p>

<pre><code class="language-bash">brew install npm wget
</code></pre>

<p>To begin, we will create a new Node project.</p>

<pre><code class="language-bash">npm init
</code></pre>

<p>This prompts you for the package name and then the version number. Hit <code>ENTER</code> to accept the default name of <code>riot</code> and default version of <code>1.0.0</code>.</p>

<pre><code class="language-bash">package name: (riot)
version: (1.0.0)
</code></pre>

<p>This prompts you for a project description. Add any non-empty description you would like. Below, the description is <code>room detector</code></p>

<pre><code class="language-bash">description: room detector
</code></pre>

<p>This prompts you for the entry point, or the main file to run the project from. Enter <code>app.js</code>.</p>

<pre><code class="language-bash">entry point: (index.js) app.js
</code></pre>

<p>This prompts you for the <code>test command</code> and <code>git repository</code>. Hit <code>ENTER</code> to skip these fields for now.</p>

<pre><code class="language-bash">test command:
git repository:
</code></pre>

<p>This prompts you for <code>keywords</code> and <code>author</code>. Fill in any values you would like. Below, we use <code>iot</code>, <code>wifi</code> for keywords and use <code>John Doe</code> for the author.</p>

<pre><code class="language-bash">keywords: iot,wifi
author: John Doe
</code></pre>

<p>This prompts you for the license. Hit <code>ENTER</code> to accept the default value of <code>ISC</code>.</p>

<pre><code class="language-bash">license: (ISC)
</code></pre>

<p>At this point, <code>npm</code> will prompt you with a summary of information so far. Your output should be similar to the following.</p>

<pre><code class="language-json">{
  "name": "riot",
  "version": "1.0.0",
  "description": "room detector",
  "main": "app.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "keywords": [
    "iot",
    "wifi"
  ],
  "author": "John Doe",
  "license": "ISC"
}
</code></pre>

<p>Hit <code>ENTER</code> to accept. <code>npm</code> then produces a <code>package.json</code>. List all files to double-check.</p>

<pre><code class="language-bash">ls
</code></pre>

<p>This will output the only file in this directory, along with the virtual environment folder.</p>

<pre><code class="language-bash">package.json
riot
</code></pre>

<p>Install NodeJS dependencies for our project.</p>

<pre class="break-out"><code class="language-bash">npm install electron --global  # makes electron binary accessible globally
npm install node-wifi --save
</code></pre>

<p>Start with , by downloading the file, using the below. The following <code>-O</code> argument renames <code>main.js</code> to <code>app.js</code>.</p>

<pre class="break-out"><code class="language-bash">wget https://raw.githubusercontent.com/electron/electron-quick-start/master/main.js -O app.js
</code></pre>

<p>Open <code>app.js</code> in <code>nano</code> or your favorite text editor.</p>

<pre><code class="language-bash">nano app.js
</code></pre>

<p>On line 12, change <em>index.html</em> to <em>static/index.html</em>, as we will create a directory <code>static</code> to contain all HTML templates.</p>

<pre><code class="language-bash">function createWindow () {
  // Create the browser window.
  win = new BrowserWindow({width: 1200, height: 800})

  // and load the index.html of the app.
  win.loadFile('static/index.html')

  // Open the DevTools.
</code></pre>

<p>Save your changes and exit the editor. Your file should match the  of the <code>app.js</code> file. Now create a new directory to house our HTML templates.</p>

<pre><code class="language-bash">mkdir static
</code></pre>

<p>Download a stylesheet created for this project.</p>

<pre class="break-out"><code class="language-bash">wget https://raw.githubusercontent.com/alvinwan/riot/master/static/style.css?token=AB-ObfDtD46ANlqrObDanckTQJ2Q1Pyuks5bf79PwA%3D%3D -O static/style.css
</code></pre>

<p>Open <code>static/index.html</code> in <code>nano</code> or your favorite text editor. Start with the standard HTML structure.</p>

<pre><code class="language-html">&lt;!DOCTYPE html&gt;
  &lt;html&gt;
    &lt;head&gt;
      &lt;meta charset="UTF-8"&gt;
      &lt;title&gt;Riot | Room Detector&lt;/title&gt;
    &lt;/head&gt;
    &lt;body&gt;
      &lt;main&gt;
      &lt;/main&gt;
    &lt;/body&gt;
  &lt;/html&gt;
</code></pre>

<p>Right after the title, link the Montserrat font linked by Google Fonts and stylesheet.</p>

<pre class="break-out"><code class="language-html">&lt;title&gt;Riot &#124; Room Detector&lt;/title&gt;
  &lt;!-- start new code --&gt;
  &lt;link href="https://fonts.googleapis.com/css?family=Montserrat:400,700" rel="stylesheet"&gt;
  &lt;link href="style.css" rel="stylesheet"&gt;
  &lt;!-- end new code --&gt;
&lt;/head&gt;
</code></pre>

<p>Between the <code>main</code> tags, add a slot for the predicted room name.</p>

<pre><code class="language-html">&lt;main&gt;
  &lt;!-- start new code --&gt;
  &lt;p class="text"&gt;I believe you’re in the&lt;/p&gt;
  &lt;h1 class="title" id="predicted-room-name"&gt;(I dunno)&lt;/h1&gt;
  &lt;!-- end new code --&gt;
&lt;/main&gt;
</code></pre>

<p>Your script should now match the following exactly. Exit the editor.</p>

<pre class="break-out"><code class="language-html">&lt;!DOCTYPE html&gt;
  &lt;html&gt;
    &lt;head&gt;
      &lt;meta charset="UTF-8"&gt;
      &lt;title&gt;Riot | Room Detector&lt;/title&gt;
      &lt;link href="https://fonts.googleapis.com/css?family=Montserrat:400,700" rel="stylesheet"&gt;
      &lt;link href="style.css" rel="stylesheet"&gt;
    &lt;/head&gt;
    &lt;body&gt;
      &lt;main&gt;
        &lt;p class="text"&gt;I believe you’re in the&lt;/p&gt;
        &lt;h1 class="title" id="predicted-room-name"&gt;(I dunno)&lt;/h1&gt;
      &lt;/main&gt;
    &lt;/body&gt;
  &lt;/html&gt;
</code></pre>

<p>Now, amend the package file to contain a start command.</p>

<pre><code class="language-bash">nano package.json
</code></pre>

<p>Right after line 7, add a <code>start</code> command that’s aliased to <code>electron .</code>. Make sure to add a comma to the end of the previous line.</p>

<pre><code class="language-bash">"scripts": {
  "test": "echo \"Error: no test specified\" && exit 1",
  "start": "electron ."
},
</code></pre>

<p>Save and exit. You are now ready to launch your desktop app in Electron JS. Use <code>npm</code> to launch your application.</p>

<pre><code class="language-bash">npm start
</code></pre>

<p>Your desktop application should match the following.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a91cdb8b-81d9-4e49-9abb-f05c8a9112bf/1-building-room-detector-iot-devices.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a91cdb8b-81d9-4e49-9abb-f05c8a9112bf/1-building-room-detector-iot-devices.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a91cdb8b-81d9-4e49-9abb-f05c8a9112bf/1-building-room-detector-iot-devices.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a91cdb8b-81d9-4e49-9abb-f05c8a9112bf/1-building-room-detector-iot-devices.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a91cdb8b-81d9-4e49-9abb-f05c8a9112bf/1-building-room-detector-iot-devices.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a91cdb8b-81d9-4e49-9abb-f05c8a9112bf/1-building-room-detector-iot-devices.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a91cdb8b-81d9-4e49-9abb-f05c8a9112bf/1-building-room-detector-iot-devices.png"
			sizes="100vw"
			alt="home page with button"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Home page with “Add New Room” button available ()
		</figcaption>
	
</figure>


<p>This completes your starting desktop app. To exit, navigate back to your terminal and CTRL+C. In the next step, we will record wifi networks, and make the recording utility accessible through the desktop application UI.</p>

<h3 id="step-2-record-wifi-networks">Step 2: Record WiFi Networks</h3>

<p>In this step, you will write a NodeJS script that records the strength and frequency of all in-range wifi networks. Create a directory for your scripts.</p>

<pre><code class="language-javascript">mkdir scripts
</code></pre>

<p>Open <code>scripts/observe.js</code> in <code>nano</code> or your favorite text editor.</p>

<pre><code class="language-javascript">nano scripts/observe.js
</code></pre>

<p>Import a NodeJS wifi utility and the filesystem object.</p>

<pre><code class="language-javascript">var wifi = require('node-wifi');
var fs = require('fs');
</code></pre>

<p>Define a <code>record</code> function that accepts a completion handler.</p>

<pre><code class="language-javascript">/**
 * Uses a recursive function for repeated scans, since scans are asynchronous.
 */
function record(n, completion, hook) {
}
</code></pre>

<p>Inside the new function, initialize the wifi utility. Set <code>iface</code> to null to initialize to a random wifi interface, as this value is currently irrelevant.</p>

<pre><code class="language-javascript">function record(n, completion, hook) {
    wifi.init({
        iface : null
    });
}
</code></pre>

<p>Define an array to contain your samples. <em>Samples</em> are training data we will use for our model. The samples in this particular tutorial are lists of in-range wifi networks and their associated strengths, frequencies, names etc.</p>

<pre><code class="language-javascript">function record(n, completion, hook) {
    ...
    samples = []
}
</code></pre>

<p>Define a recursive function <code>startScan</code>, which will asynchronously initiate wifi scans. Upon completion, the asynchronous wifi scan will then recursively invoke <code>startScan</code>.</p>

<pre><code class="language-javascript">function record(n, completion, hook) {
  ...
  function startScan(i) {
    wifi.scan(function(err, networks) {
    });
  }
  startScan(n);
}
</code></pre>

<p>In the <code>wifi.scan</code> callback, check for errors or empty lists of networks and restart the scan if so.</p>

<pre><code class="language-javascript">wifi.scan(function(err, networks) {
  if (err || networks.length == 0) {
    startScan(i);
    return
  }
});
</code></pre>

<p>Add the recursive function’s base case, which invokes the completion handler.</p>

<pre class="break-out"><code class="language-javascript">wifi.scan(function(err, networks) {
  ...
  if (i <= 0) {
    return completion({samples: samples});
  }
});
</code></pre>

<p>Output a progress update, append to the list of samples, and make the recursive call.</p>

<pre><code class="language-javascript">wifi.scan(function(err, networks) {
  ...
  hook(n-i+1, networks);
  samples.push(networks);
  startScan(i-1);
});
</code></pre>

<p>At the end of your file, invoke the <code>record</code> function with a callback that saves samples to a file on disk.</p>

<pre class="break-out"><code class="language-javascript">function record(completion) {
  ...
}

function cli() {
  record(1, function(data) {
    fs.writeFile('samples.json', JSON.stringify(data), 'utf8', function() {});
  }, function(i, networks) {
    console.log(" * [INFO] Collected sample " + (21-i) + " with " + networks.length + " networks");
  })
}

cli();
</code></pre>

<p>Double check that your file matches the following:</p>

<pre class="break-out"><code class="language-javascript">var wifi = require('node-wifi');
var fs = require('fs');

/**
 * Uses a recursive function for repeated scans, since scans are asynchronous.
 */
function record(n, completion, hook) {
  wifi.init({
      iface : null // network interface, choose a random wifi interface if set to null
  });

  samples = []
  function startScan(i) {
    wifi.scan(function(err, networks) {
        if (err || networks.length == 0) {
          startScan(i);
          return
        }
        if (i <= 0) {
          return completion({samples: samples});
        }
        hook(n-i+1, networks);
        samples.push(networks);
        startScan(i-1);
    });
  }

  startScan(n);
}

function cli() {
    record(1, function(data) {
        fs.writeFile('samples.json', JSON.stringify(data), 'utf8', function() {});
    }, function(i, networks) {
        console.log(" * [INFO] Collected sample " + i + " with " + networks.length + " networks");
    })
}

cli();
</code></pre>

<p>Save and exit. Run the script.</p>

<pre><code class="language-javascript">node scripts/observe.js
</code></pre>

<p>Your output will match the following, with variable numbers of networks.</p>

<pre><code class="language-javascript"> * [INFO] Collected sample 1 with 39 networks
</code></pre>

<p>Examine the samples that were just collected. Pipe to <code>json_pp</code> to pretty print the JSON and pipe to head to view the first 16 lines.</p>

<pre><code class="language-javascript">cat samples.json &#124; json_pp &#124; head -16
</code></pre>

<p>The below is example output for a 2.4 GHz network.</p>

<pre><code class="language-javascript">{
  "samples": [
    [
      {
        "mac": "64:0f:28:79:9a:29",
        "bssid": "64:0f:28:79:9a:29",
        "ssid": "SMASHINGMAGAZINEROCKS",
         "channel": 4,
         "frequency": 2427,
          "signal_level": "-91",
          "security": "WPA WPA2",
          "security_flags": [
           "(PSK/AES,TKIP/TKIP)",
          "(PSK/AES,TKIP/TKIP)"
        ]
      },
</code></pre>

<p>This concludes your NodeJS wifi-scanning script. This allows us to view all in-range WiFi networks. In the next step, you will make this script accessible from the desktop app.</p>

<div class="sponsors__wide-place"></div>




<h3 id="step-3-connect-scan-script-to-desktop-app">Step 3: Connect Scan Script To Desktop App</h3>

<p>In this step, you will first add a button to the desktop app to trigger the script with. Then, you will update the desktop app UI with the script’s progress.</p>

<p>Open <code>static/index.html</code>.</p>

<pre><code class="language-html">nano static/index.html
</code></pre>

<p>Insert the &ldquo;Add&rdquo; button, as shown below.</p>

<pre class="break-out"><code class="language-html">&lt;h1 class="title" id="predicted-room-name"&gt;(I dunno)&lt;/h1&gt;
        &lt;!-- start new code --&gt;
        &lt;div class="buttons"&gt;
            &lt;a href="add.html" class="button"&gt;Add new room&lt;/a&gt;
        &lt;/div&gt;
        &lt;!-- end new code --&gt;
    &lt;/main&gt;
</code></pre>

<p>Save and exit. Open <code>static/add.html</code>.</p>

<pre><code class="language-html">nano static/add.html
</code></pre>

<p>Paste the following content.</p>

<pre class="break-out"><code class="language-html">&lt;!DOCTYPE html&gt;
  &lt;html&gt;
    &lt;head&gt;
      &lt;meta charset="UTF-8"&gt;
      &lt;title&gt;Riot | Add New Room&lt;/title&gt;
      &lt;link href="https://fonts.googleapis.com/css?family=Montserrat:400,700" rel="stylesheet"&gt;
      &lt;link href="style.css" rel="stylesheet"&gt;
    &lt;/head&gt;
    &lt;body&gt;
      &lt;main&gt;
        &lt;h1 class="title" id="add-title"&gt;0&lt;/h1&gt;
        &lt;p class="subtitle"&gt;of &lt;span&gt;20&lt;/span&gt; samples needed. Feel free to move around the room.&lt;/p&gt;
        &lt;input type="text" id="add-room-name" class="text-field" placeholder="(room name)"&gt;
        &lt;div class="buttons"&gt;
          &lt;a href="#" id="start-recording" class="button"&gt;Start recording&lt;/a&gt;
          &lt;a href="index.html" class="button light"&gt;Cancel&lt;/a&gt;
        &lt;/div&gt;
        &lt;p class="text" id="add-status" style="display:none"&gt;&lt;/p&gt;
      &lt;/main&gt;
      &lt;script&gt;
        require('../scripts/observe.js')
      &lt;/script&gt;
    &lt;/body&gt;
  &lt;/html&gt;
</code></pre>

<p>Save and exit. Reopen <code>scripts/observe.js</code>.</p>

<pre><code class="language-javascript">nano scripts/observe.js
</code></pre>

<p>Beneath the <code>cli</code> function, define a new <code>ui</code> function.</p>

<pre><code class="language-javascript">function cli() {
    ...
}

// start new code
function ui() {
}
// end new code

cli();
</code></pre>

<p>Update the desktop app status to indicate the function has started running.</p>

<pre class="break-out"><code class="language-javascript">function ui() {
  var room_name = document.querySelector('#add-room-name').value;
  var status = document.querySelector('#add-status');
  var number = document.querySelector('#add-title');
  status.style.display = "block"
  status.innerHTML = "Listening for wifi..."
}
</code></pre>

<p>Partition the data into training and validation data sets.</p>

<pre><code class="language-javascript">function ui() {
  ...
  function completion(data) {
    train_data = {samples: data['samples'].slice(0, 15)}
    test_data = {samples: data['samples'].slice(15)}
    var train_json = JSON.stringify(train_data);
    var test_json = JSON.stringify(test_data);
  }
}
</code></pre>

<p>Still within the <code>completion</code> callback, write both datasets to disk.</p>

<pre class="break-out"><code class="language-javascript">function ui() {
  ...
  function completion(data) {
    ...
    fs.writeFile('data/' + room_name + '_train.json', train_json, 'utf8', function() {});
    fs.writeFile('data/' + room_name + '_test.json', test_json, 'utf8', function() {});
    console.log(" * [INFO] Done")
    status.innerHTML = "Done."
  }
}
</code></pre>

<p>Invoke <code>record</code> with the appropriate callbacks to record 20 samples and save the samples to disk.</p>

<pre class="break-out"><code class="language-javascript">function ui() {
  ...
  function completion(data) {
    ...
  }
  record(20, completion, function(i, networks) {
    number.innerHTML = i
    console.log(" * [INFO] Collected sample " + i + " with " + networks.length + " networks")
  })
}
</code></pre>

<p>Finally, invoke the <code>cli</code> and <code>ui</code> functions where appropriate. Start by deleting the <code>cli();</code> call at the bottom of the file.</p>

<pre><code class="language-javascript">function ui() {
    ...
}

cli();  // remove me
</code></pre>

<p>Check if the document object is globally accessible. If not, the script is being run from the command line. In this case, invoke the <code>cli</code> function. If it is, the script is loaded from within the desktop app. In this case, bind the click listener to the <code>ui</code> function.</p>

<pre><code class="language-javascript">if (typeof document == 'undefined') {
    cli();
} else {
    document.querySelector('#start-recording').addEventListener('click', ui)
}
</code></pre>

<p>Save and exit. Create a directory to hold our data.</p>

<pre><code class="language-bash">mkdir data
</code></pre>

<p>Launch the desktop app.</p>

<pre><code class="language-bash">npm start
</code></pre>

<p>You will see the following homepage. Click on &ldquo;Add room&rdquo;.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/33b7d71e-21c0-452e-9122-8ef76427c053/2-building-room-detector-iot-devices.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/33b7d71e-21c0-452e-9122-8ef76427c053/2-building-room-detector-iot-devices.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/33b7d71e-21c0-452e-9122-8ef76427c053/2-building-room-detector-iot-devices.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/33b7d71e-21c0-452e-9122-8ef76427c053/2-building-room-detector-iot-devices.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/33b7d71e-21c0-452e-9122-8ef76427c053/2-building-room-detector-iot-devices.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/33b7d71e-21c0-452e-9122-8ef76427c053/2-building-room-detector-iot-devices.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/33b7d71e-21c0-452e-9122-8ef76427c053/2-building-room-detector-iot-devices.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<p>You will see the following form. Type in a name for the room. Remember this name, as we will use this later on. Our example will be <code>bedroom</code>.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f7dfbf49-0b2b-4203-9524-c9b84d64cc5d/3-building-room-detector-iot-devices.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f7dfbf49-0b2b-4203-9524-c9b84d64cc5d/3-building-room-detector-iot-devices.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f7dfbf49-0b2b-4203-9524-c9b84d64cc5d/3-building-room-detector-iot-devices.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f7dfbf49-0b2b-4203-9524-c9b84d64cc5d/3-building-room-detector-iot-devices.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f7dfbf49-0b2b-4203-9524-c9b84d64cc5d/3-building-room-detector-iot-devices.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f7dfbf49-0b2b-4203-9524-c9b84d64cc5d/3-building-room-detector-iot-devices.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f7dfbf49-0b2b-4203-9524-c9b84d64cc5d/3-building-room-detector-iot-devices.png"
			sizes="100vw"
			alt="Add New Room page"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			“Add New Room” page on load ()
		</figcaption>
	
</figure>


<p>Click &ldquo;Start recording,&rdquo; and you will see the following status &ldquo;Listening for wifi&hellip;&rdquo;.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/eaf322d0-60e8-4b2a-9751-62be0c5cc7b6/4-building-room-detector-iot-devices.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/eaf322d0-60e8-4b2a-9751-62be0c5cc7b6/4-building-room-detector-iot-devices.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/eaf322d0-60e8-4b2a-9751-62be0c5cc7b6/4-building-room-detector-iot-devices.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/eaf322d0-60e8-4b2a-9751-62be0c5cc7b6/4-building-room-detector-iot-devices.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/eaf322d0-60e8-4b2a-9751-62be0c5cc7b6/4-building-room-detector-iot-devices.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/eaf322d0-60e8-4b2a-9751-62be0c5cc7b6/4-building-room-detector-iot-devices.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/eaf322d0-60e8-4b2a-9751-62be0c5cc7b6/4-building-room-detector-iot-devices.png"
			sizes="100vw"
			alt="starting recording"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			“Add New Room” starting recording ()
		</figcaption>
	
</figure>


<p>Once all 20 samples are recorded, your app will match the following. The status will read “Done.”</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c7b15151-2a24-4464-8540-64143f60d355/5-building-room-detector-iot-devices.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c7b15151-2a24-4464-8540-64143f60d355/5-building-room-detector-iot-devices.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c7b15151-2a24-4464-8540-64143f60d355/5-building-room-detector-iot-devices.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c7b15151-2a24-4464-8540-64143f60d355/5-building-room-detector-iot-devices.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c7b15151-2a24-4464-8540-64143f60d355/5-building-room-detector-iot-devices.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c7b15151-2a24-4464-8540-64143f60d355/5-building-room-detector-iot-devices.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c7b15151-2a24-4464-8540-64143f60d355/5-building-room-detector-iot-devices.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			“Add New Room” page after recording is complete ()
		</figcaption>
	
</figure>


<p>Click on the misnamed “Cancel” to return to the homepage, which matches the following.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/33b7d71e-21c0-452e-9122-8ef76427c053/2-building-room-detector-iot-devices.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/33b7d71e-21c0-452e-9122-8ef76427c053/2-building-room-detector-iot-devices.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/33b7d71e-21c0-452e-9122-8ef76427c053/2-building-room-detector-iot-devices.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/33b7d71e-21c0-452e-9122-8ef76427c053/2-building-room-detector-iot-devices.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/33b7d71e-21c0-452e-9122-8ef76427c053/2-building-room-detector-iot-devices.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/33b7d71e-21c0-452e-9122-8ef76427c053/2-building-room-detector-iot-devices.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/33b7d71e-21c0-452e-9122-8ef76427c053/2-building-room-detector-iot-devices.png"
			sizes="100vw"
			alt="finished recording"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			“Add New Room” page after recording is complete ()
		</figcaption>
	
</figure>


<p>We can now scan wifi networks from the desktop UI, which will save all recorded samples to files on disk. Next, we will train an out-of-box machine learning algorithm-least squares on the data you have collected.</p>

<h3 id="step-4-write-python-training-script">Step 4: Write Python Training Script</h3>

<p>In this step, we will write a training script in Python. Create a directory for your training utilities.</p>

<pre><code class="language-bash">mkdir model
</code></pre>

<p>Open <code>model/train.py</code></p>

<pre><code class="language-bash">nano model/train.py
</code></pre>

<p>At the top of your file, import the <code>numpy</code> computational library and <code>scipy</code> for its least squares model.</p>

<pre><code class="language-bash">import numpy as np
from scipy.linalg import lstsq
import json
import sys
</code></pre>

<p>The next three utilities will handle loading and setting up data from the files on disk. Start by adding a utility function that flattens nested lists. You will use this to flatten a list of list of samples.</p>

<pre><code class="language-bash">import sys

def flatten(list_of_lists):
    """Flatten a list of lists to make a list.
    >>> flatten([[1], [2], [3, 4]])
    [1, 2, 3, 4]
    """
    return sum(list_of_lists, [])
</code></pre>

<p>Add a second utility that loads samples from the specified files. This method abstracts away the fact that samples are spread out across multiple files, returning just a single generator for all samples. For each of the samples, the label is the index of the file. e.g., If you call <code>get_all_samples('a.json', 'b.json')</code>, all samples in <code>a.json</code> will have label 0 and all samples in <code>b.json</code> will have label 1.</p>

<pre class="break-out"><code class="language-bash">def get_all_samples(paths):
  """Load all samples from JSON files."""
  for label, path in enumerate(paths):
  with open(path) as f:
    for sample in json.load(f)['samples']:
      signal_levels = [
        network['signal_level'].replace('RSSI', '') or 0
        for network in sample]
      yield [network['mac'] for network in sample], signal_levels, label
</code></pre>

<p>Next, add a utility that encodes the samples using a bag-of-words-esque model. Here is an example: Assume we collect two samples.</p>

<ol>
<li>wifi network A at strength 10 and wifi network B at strength 15</li>
<li>wifi network B at strength 20 and wifi network C at strength 25.</li>
</ol>

<p>This function will produce a list of three numbers for each of the samples: the first value is the strength of wifi network A, the second for network B, and the third for C. In effect, the format is [A, B, C].</p>

<ol>
<li>[10, 15, 0]</li>
<li>[0, 20, 25]</li>
</ol>

<pre class="break-out"><code class="language-bash">def bag_of_words(all_networks, all_strengths, ordering):
  """Apply bag-of-words encoding to categorical variables.

  >>> samples = bag_of_words(
  ...     [['a', 'b'], ['b', 'c'], ['a', 'c']],
  ...     [[1, 2], [2, 3], [1, 3]],
  ...     ['a', 'b', 'c'])
  >>> next(samples)
  [1, 2, 0]
  >>> next(samples)
  [0, 2, 3]
  """
  for networks, strengths in zip(all_networks, all_strengths):
    yield [strengths[networks.index(network)]
      if network in networks else 0
      for network in ordering]
</code></pre>

<p>Using all three utilities above, we synthesize a collection of samples and their labels. Gather all samples and labels using <code>get_all_samples</code>. Define a consistent format <code>ordering</code> to one-hot encode all samples, then apply <code>one_hot</code> encoding to samples. Finally, construct the data and label matrices <code>X</code> and <code>Y</code> respectively.</p>

<pre class="break-out"><code class="language-bash">def create_dataset(classpaths, ordering=None):
  """Create dataset from a list of paths to JSON files."""
  networks, strengths, labels = zip(*get_all_samples(classpaths))
  if ordering is None:
    ordering = list(sorted(set(flatten(networks))))
  X = np.array(list(bag_of_words(networks, strengths, ordering))).astype(np.float64)
  Y = np.array(list(labels)).astype(np.int)
  return X, Y, ordering
</code></pre>

<p>These functions complete the data pipeline. Next, we abstract away model prediction and evaluation. Start by defining the prediction method. The first function normalizes our model outputs, so that the sum of all values totals to 1 and that all values are non-negative; this ensures that the output is a valid probability distribution. The second evaluates the model.</p>

<pre class="break-out"><code class="language-bash">def softmax(x):
  """Convert one-hotted outputs into probability distribution"""
  x = np.exp(x)
  return x / np.sum(x)


def predict(X, w):
  """Predict using model parameters"""
  return np.argmax(softmax(X.dot(w)), axis=1)
</code></pre>

<p>Next, evaluate the model’s accuracy. The first line runs prediction using the model. The second counts the numbers of times both predicted and true values agree, then normalizes by the total number of samples.</p>

<pre><code class="language-bash">def evaluate(X, Y, w):
  """Evaluate model w on samples X and labels Y."""
  Y_pred = predict(X, w)
  accuracy = (Y == Y_pred).sum() / X.shape[0]
  return accuracy
</code></pre>

<p>This concludes our prediction and evaluation utilities. After these utilities, define a <code>main</code> function that will collect the dataset, train, and evaluate. Start by reading the list of arguments from the command line <code>sys.argv</code>; these are the rooms to include in training. Then create a large dataset from all of the specified rooms.</p>

<pre class="break-out"><code class="language-bash">def main():
  classes = sys.argv[1:]

  train_paths = sorted(['data/{}_train.json'.format(name) for name in classes])
  test_paths = sorted(['data/{}_test.json'.format(name) for name in classes])
  X_train, Y_train, ordering = create_dataset(train_paths)
  X_test, Y_test, _ = create_dataset(test_paths, ordering=ordering)
</code></pre>

<p>Apply one-hot encoding to the labels. A <em>one-hot encoding</em> is similar to the bag-of-words model above; we use this encoding to handle categorical variables. Say we have 3 possible labels. Instead of labelling 1, 2, or 3, we label the data with [1, 0, 0], [0, 1, 0], or [0, 0, 1]. For this tutorial, we will spare the explanation for why one-hot encoding is important. Train the model, and evaluate on both the train and validation sets.</p>

<pre class="break-out"><code class="language-bash">def main():
  ...
  X_test, Y_test, _ = create_dataset(test_paths, ordering=ordering)
  
  Y_train_oh = np.eye(len(classes))[Y_train]
  w, _, _, _ = lstsq(X_train, Y_train_oh)
  train_accuracy = evaluate(X_train, Y_train, w)
  test_accuracy = evaluate(X_test, Y_test, w)
</code></pre>

<p>Print both accuracies, and save the model to disk.</p>

<pre><code class="language-bash">def main():
  ...
  print('Train accuracy ({}%), Validation accuracy ({}%)'.format(train_accuracy*100, test_accuracy*100))
  np.save('w.npy', w)
  np.save('ordering.npy', np.array(ordering))
  sys.stdout.flush()
</code></pre>

<p>At the end of the file, run the <code>main</code> function.</p>

<pre><code class="language-javascript">if __name__ == '__main__':
  main()
</code></pre>

<p>Save and exit. Double check that your file matches the following:</p>

<pre class="break-out"><code class="language-bash">import numpy as np
from scipy.linalg import lstsq
import json
import sys


def flatten(list_of_lists):
    """Flatten a list of lists to make a list.
    >>> flatten([[1], [2], [3, 4]])
    [1, 2, 3, 4]
    """
    return sum(list_of_lists, [])


def get_all_samples(paths):
    """Load all samples from JSON files."""
    for label, path in enumerate(paths):
        with open(path) as f:
            for sample in json.load(f)['samples']:
                signal_levels = [
                    network['signal_level'].replace('RSSI', '') or 0
                    for network in sample]
                yield [network['mac'] for network in sample], signal_levels, label


def bag_of_words(all_networks, all_strengths, ordering):
    """Apply bag-of-words encoding to categorical variables.
    >>> samples = bag_of_words(
    ...     [['a', 'b'], ['b', 'c'], ['a', 'c']],
    ...     [[1, 2], [2, 3], [1, 3]],
    ...     ['a', 'b', 'c'])
    >>> next(samples)
    [1, 2, 0]
    >>> next(samples)
    [0, 2, 3]
    """
    for networks, strengths in zip(all_networks, all_strengths):
        yield [int(strengths[networks.index(network)])
            if network in networks else 0
            for network in ordering]


def create_dataset(classpaths, ordering=None):
    """Create dataset from a list of paths to JSON files."""
    networks, strengths, labels = zip(*get_all_samples(classpaths))
    if ordering is None:
        ordering = list(sorted(set(flatten(networks))))
    X = np.array(list(bag_of_words(networks, strengths, ordering))).astype(np.float64)
    Y = np.array(list(labels)).astype(np.int)
    return X, Y, ordering


def softmax(x):
    """Convert one-hotted outputs into probability distribution"""
    x = np.exp(x)
    return x / np.sum(x)


def predict(X, w):
    """Predict using model parameters"""
    return np.argmax(softmax(X.dot(w)), axis=1)


def evaluate(X, Y, w):
    """Evaluate model w on samples X and labels Y."""
    Y_pred = predict(X, w)
    accuracy = (Y == Y_pred).sum() / X.shape[0]
    return accuracy


def main():
    classes = sys.argv[1:]

    train_paths = sorted(['data/{}_train.json'.format(name) for name in classes])
    test_paths = sorted(['data/{}_test.json'.format(name) for name in classes])
    X_train, Y_train, ordering = create_dataset(train_paths)
    X_test, Y_test, _ = create_dataset(test_paths, ordering=ordering)

    Y_train_oh = np.eye(len(classes))[Y_train]
    w, _, _, _ = lstsq(X_train, Y_train_oh)
    train_accuracy = evaluate(X_train, Y_train, w)
    validation_accuracy = evaluate(X_test, Y_test, w)

    print('Train accuracy ({}%), Validation accuracy ({}%)'.format(train_accuracy*100, validation_accuracy*100))
    np.save('w.npy', w)
    np.save('ordering.npy', np.array(ordering))
    sys.stdout.flush()


if __name__ == '__main__':
    main()
</code></pre>

<p>Save and exit. Recall the room name used above when recording the 20 samples. Use that name instead of <code>bedroom</code> below. Our example is <code>bedroom</code>. We use <code>-W ignore</code> to ignore warnings from a LAPACK bug.</p>

<pre><code class="language-bash">python -W ignore model/train.py bedroom
</code></pre>

<p>Since we&rsquo;ve only collected training samples for one room, you should see 100% training and validation accuracies.</p>

<pre><code class="language-bash">Train accuracy (100.0%), Validation accuracy (100.0%)
</code></pre>

<p>Next, we will link this training script to the desktop app.</p>

<div class="sponsors__wide-place"></div>




<h3 id="step-5-link-train-script">Step 5: Link Train Script</h3>

<p>In this step, we will automatically retrain the model whenever the user collects a new batch of samples. Open <code>scripts/observe.js</code>.</p>

<pre><code class="language-bash">nano scripts/observe.js
</code></pre>

<p>Right after the <code>fs</code> import, import the child process spawner and utilities.</p>

<pre><code class="language-javascript">var fs = require('fs');
// start new code
const spawn = require("child_process").spawn;
var utils = require('./utils.js');
</code></pre>

<p>In the <code>ui</code> function, add the following call to <code>retrain</code> at the end of the completion handler.</p>

<pre class="break-out"><code class="language-javascript">function ui() {
  ...
  function completion() {
    ...
    retrain((data) => {
      var status = document.querySelector('#add-status');
      accuracies = data.toString().split('\n')[0];
      status.innerHTML = "Retraining succeeded: " + accuracies
    });
  }
    ...
}
</code></pre>

<p>After the <code>ui</code> function, add the following <code>retrain</code> function. This spawns a child process that will run the python script. Upon completion, the process calls a completion handler. Upon failure, it will log the error message.</p>

<pre class="break-out"><code class="language-javascript">function ui() {
  ..
}

function retrain(completion) {
  var filenames = utils.get_filenames()
  const pythonProcess = spawn('python', ["./model/train.py"].concat(filenames));
  pythonProcess.stdout.on('data', completion);
  pythonProcess.stderr.on('data', (data) => {
    console.log(" * [ERROR] " + data.toString())
  })
}
</code></pre>

<p>Save and exit. Open <code>scripts/utils.js</code>.</p>

<pre><code class="language-javascript">nano scripts/utils.js
</code></pre>

<p>Add the following utility for fetching all datasets in <code>data/</code>.</p>

<pre class="break-out"><code class="language-javascript">var fs = require('fs');

module.exports = {
  get_filenames: get_filenames
}

function get_filenames() {
  filenames = new Set([]);
  fs.readdirSync("data/").forEach(function(filename) {
      filenames.add(filename.replace('_train', '').replace('_test', '').replace('.json', '' ))
  });
  filenames = Array.from(filenames.values())
  filenames.sort();
  filenames.splice(filenames.indexOf('.DS_Store'), 1)
  return filenames
}
</code></pre>

<p>Save and exit. For the conclusion of this step, physically move to a new location. There ideally should be a wall between your original location and your new location. The more barriers, the better your desktop app will work.</p>

<p>Once again, run your desktop app.</p>

<pre><code class="language-bash">npm start
</code></pre>

<p>Just as before, run the training script. Click on &ldquo;Add room&rdquo;.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/33b7d71e-21c0-452e-9122-8ef76427c053/2-building-room-detector-iot-devices.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/33b7d71e-21c0-452e-9122-8ef76427c053/2-building-room-detector-iot-devices.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/33b7d71e-21c0-452e-9122-8ef76427c053/2-building-room-detector-iot-devices.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/33b7d71e-21c0-452e-9122-8ef76427c053/2-building-room-detector-iot-devices.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/33b7d71e-21c0-452e-9122-8ef76427c053/2-building-room-detector-iot-devices.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/33b7d71e-21c0-452e-9122-8ef76427c053/2-building-room-detector-iot-devices.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/33b7d71e-21c0-452e-9122-8ef76427c053/2-building-room-detector-iot-devices.png"
			sizes="100vw"
			alt="home page with button"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Home page with “Add New Room” button available ()
		</figcaption>
	
</figure>


<p>Type in a room name that is different from your first room&rsquo;s. We will use <code>living room</code>.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f7dfbf49-0b2b-4203-9524-c9b84d64cc5d/3-building-room-detector-iot-devices.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f7dfbf49-0b2b-4203-9524-c9b84d64cc5d/3-building-room-detector-iot-devices.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f7dfbf49-0b2b-4203-9524-c9b84d64cc5d/3-building-room-detector-iot-devices.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f7dfbf49-0b2b-4203-9524-c9b84d64cc5d/3-building-room-detector-iot-devices.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f7dfbf49-0b2b-4203-9524-c9b84d64cc5d/3-building-room-detector-iot-devices.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f7dfbf49-0b2b-4203-9524-c9b84d64cc5d/3-building-room-detector-iot-devices.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f7dfbf49-0b2b-4203-9524-c9b84d64cc5d/3-building-room-detector-iot-devices.png"
			sizes="100vw"
			alt="Add New Room page"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			“Add New Room” page on load ()
		</figcaption>
	
</figure>


<p>Click &ldquo;Start recording,&rdquo; and you will see the following status &ldquo;Listening for wifi&hellip;&rdquo;.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2fcc6909-e63b-461c-a01d-7a5b1f42b3de/6-building-room-detector-iot-devices.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2fcc6909-e63b-461c-a01d-7a5b1f42b3de/6-building-room-detector-iot-devices.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2fcc6909-e63b-461c-a01d-7a5b1f42b3de/6-building-room-detector-iot-devices.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2fcc6909-e63b-461c-a01d-7a5b1f42b3de/6-building-room-detector-iot-devices.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2fcc6909-e63b-461c-a01d-7a5b1f42b3de/6-building-room-detector-iot-devices.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2fcc6909-e63b-461c-a01d-7a5b1f42b3de/6-building-room-detector-iot-devices.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2fcc6909-e63b-461c-a01d-7a5b1f42b3de/6-building-room-detector-iot-devices.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			“Add New Room” starting recording for second room ()
		</figcaption>
	
</figure>


<p>Once all 20 samples are recorded, your app will match the following. The status will read &ldquo;Done. Retraining model&hellip;&rdquo;</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c4f30314-0743-4ed4-a7d9-e008e6cea4db/7-building-room-detector-iot-devices.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c4f30314-0743-4ed4-a7d9-e008e6cea4db/7-building-room-detector-iot-devices.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c4f30314-0743-4ed4-a7d9-e008e6cea4db/7-building-room-detector-iot-devices.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c4f30314-0743-4ed4-a7d9-e008e6cea4db/7-building-room-detector-iot-devices.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c4f30314-0743-4ed4-a7d9-e008e6cea4db/7-building-room-detector-iot-devices.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c4f30314-0743-4ed4-a7d9-e008e6cea4db/7-building-room-detector-iot-devices.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c4f30314-0743-4ed4-a7d9-e008e6cea4db/7-building-room-detector-iot-devices.png"
			sizes="100vw"
			alt="finished recording 2"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			“Add New Room” page after recording for second room complete ()
		</figcaption>
	
</figure>


<p>In the next step, we will use this retrained model to predict the room you’re in, on the fly.</p>

<h3 id="step-6-write-python-evaluation-script">Step 6: Write Python Evaluation Script</h3>

<p>In this step, we will load the pretrained model parameters, scan for wifi networks, and predict the room based on the scan.</p>

<p>Open <code>model/eval.py</code>.</p>

<pre><code class="language-bash">nano model/eval.py
</code></pre>

<p>Import libraries used and defined in our last script.</p>

<pre><code class="language-bash">import numpy as np
import sys
import json
import os
import json

from train import predict
from train import softmax
from train import create_dataset
from train import evaluate
</code></pre>

<p>Define a utility to extract the names of all datasets. This function assumes that all datasets are stored in <code>data/</code> as <code>&lt;dataset&gt;_train.json</code> and <code>&lt;dataset&gt;_test.json</code>.</p>

<pre class="break-out"><code class="language-javascript">from train import evaluate

def get_datasets():
  """Extract dataset names."""
  return sorted(list({path.split('_')[0] for path in os.listdir('./data')
    if '.DS' not in path}))
</code></pre>

<p>Define the <code>main</code> function, and start by loading parameters saved from the training script.</p>

<pre><code class="language-javascript">def get_datasets():
  ...

def main():
  w = np.load('w.npy')
  ordering = np.load('ordering.npy')
</code></pre>

<p>Create the dataset and predict.</p>

<pre><code class="language-javascript">def main():
  ...
  classpaths = [sys.argv[1]]
  X, _, _ = create_dataset(classpaths, ordering)
  y = np.asscalar(predict(X, w))
</code></pre>

<p>Compute a confidence score based on the difference between the top two probabilities.</p>

<pre><code class="language-javascript">def main():
  ...
  sorted_y = sorted(softmax(X.dot(w)).flatten())
  confidence = 1
  if len(sorted_y) > 1:
    confidence = round(sorted_y[-1] - sorted_y[-2], 2)
</code></pre>

<p>Finally, extract the category and print the result. To conclude the script, invoke the <code>main</code> function.</p>

<pre class="break-out"><code class="language-javascript">def main()
  ...
  category = get_datasets()[y]
  print(json.dumps({"category": category, "confidence": confidence}))

if __name__ == '__main__':
  main()
</code></pre>

<p>Save and exit. Double check your code matches the following ():</p>

<pre class="break-out"><code class="language-python">import numpy as np
import sys
import json
import os
import json

from train import predict
from train import softmax
from train import create_dataset
from train import evaluate


def get_datasets():
    """Extract dataset names."""
    return sorted(list({path.split('_')[0] for path in os.listdir('./data')
        if '.DS' not in path}))


def main():
    w = np.load('w.npy')
    ordering = np.load('ordering.npy')

    classpaths = [sys.argv[1]]
    X, _, _ = create_dataset(classpaths, ordering)
    y = np.asscalar(predict(X, w))

    sorted_y = sorted(softmax(X.dot(w)).flatten())
    confidence = 1
    if len(sorted_y) > 1:
        confidence = round(sorted_y[-1] - sorted_y[-2], 2)

    category = get_datasets()[y]
    print(json.dumps({"category": category, "confidence": confidence}))


if __name__ == '__main__':
    main()
</code></pre>

<p>Next, we will connect this evaluation script to the desktop app. The desktop app will continuously run wifi scans and update the UI with the predicted room.</p>

<h3 id="step-7-connect-evaluation-to-desktop-app">Step 7: Connect Evaluation To Desktop App</h3>

<p>In this step, we will update the UI with a &ldquo;confidence&rdquo; display. Then, the associated NodeJS script will continuously run scans and predictions, updating the UI accordingly.</p>

<p>Open <code>static/index.html</code>.</p>

<pre><code class="language-bash">nano static/index.html
</code></pre>

<p>Add a line for confidence right after the title and before the buttons.</p>

<pre class="break-out"><code class="language-html">&lt;h1 class="title" id="predicted-room-name"&gt;(I dunno)&lt;/h1&gt;
&lt;!-- start new code --&gt;
&lt;p class="subtitle"&gt;with &lt;span id="predicted-confidence"&gt;0%&lt;/span&gt; confidence&lt;/p&gt;
&lt;!-- end new code --&gt;
&lt;div class="buttons"&gt;
</code></pre>

<p>Right after <code>main</code> but before the end of the <code>body</code>, add a new script <code>predict.js</code>.</p>

<pre><code class="language-javascript">&lt;/main&gt;
  &lt;!-- start new code --&gt;
  &lt;script&gt;
  require('../scripts/predict.js')
  &lt;/script&gt;
  &lt;!-- end new code --&gt;
&lt;/body&gt;
</code></pre>

<p>Save and exit. Open <code>scripts/predict.js</code>.</p>

<pre><code class="language-javascript">nano scripts/predict.js
</code></pre>

<p>Import the needed NodeJS utilities for the filesystem, utilities, and child process spawner.</p>

<pre><code class="language-javascript">var fs = require('fs');
var utils = require('./utils');
const spawn = require("child_process").spawn;
</code></pre>

<p>Define a <code>predict</code> function which invokes a separate node process to detect wifi networks and a separate Python process to predict the room.</p>

<pre class="break-out"><code class="language-javascript">function predict(completion) {
  const nodeProcess = spawn('node', ["scripts/observe.js"]);
  const pythonProcess = spawn('python', ["-W", "ignore", "./model/eval.py", "samples.json"]);
}
</code></pre>

<p>After both processes have spawned, add callbacks to the Python process for both successes and errors. The success callback logs information, invokes the completion callback, and updates the UI with the prediction and confidence. The error callback logs the error.</p>

<pre class="break-out"><code class="language-javascript">function predict(completion) {
  ...
  pythonProcess.stdout.on('data', (data) => {
    information = JSON.parse(data.toString());
    console.log(" * [INFO] Room '" + information.category + "' with confidence '" + information.confidence + "'")
    completion()

    if (typeof document != "undefined") {
      document.querySelector('#predicted-room-name').innerHTML = information.category
      document.querySelector('#predicted-confidence').innerHTML = information.confidence
    }
  });
  pythonProcess.stderr.on('data', (data) => {
    console.log(data.toString());
  })
}
</code></pre>

<p>Define a main function to invoke the <code>predict</code> function recursively, forever.</p>

<pre><code class="language-javascript">function main() {
  f = function() { predict(f) }
  predict(f)
}

main();
</code></pre>

<p>One last time, open the desktop app to see the live prediction.</p>

<pre><code class="language-bash">npm start
</code></pre>

<p>Approximately every second, a scan will be completed and the interface will be updated with the latest confidence and predicted room. Congratulations; you have completed a simple room detector based on all in-range WiFi networks.</p>

<figure>)</figcaption></figure>

<h3 id="conclusion">Conclusion</h3>

<p>In this tutorial, we created a solution using only your desktop to detect your location within a building. We built a simple desktop app using Electron JS and applied a simple machine learning method on all in-range WiFi networks. This paves the way for Internet-of-things applications without the need for arrays of devices that are costly to maintain (cost not in terms of money but in terms of time and development).</p>

<p><strong>Note</strong>: <em>You can see the source code in its entirety on .</em></p>

<p>With time, you may find that this least squares does not perform spectacularly in fact. Try finding two locations within a single room, or stand in doorways. Least squares will be large unable to distinguish between edge cases. Can we do better? It turns out that we can, and in future lessons, we will leverage other techniques and the fundamentals of machine learning to better performance. This tutorial serves as a quick test bed for experiments to come.</p>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(ra, il)</span>
</div>


              </article>
            </body>
          </html>
---------------
<h1 id="#title_2" >3、文章： 使用服务网格提高安全性：Christian Posta带你探索Istio的新功能</h1>
Christian Posta
[http://www.infoq.com/cn/articles/istio-security-mtls-jwt?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/istio-security-mtls-jwt?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/istio-security-mtls-jwt/zh/smallimage/istio-security-mtls-jwt-s-1534205189556-1535212301624.jpeg"/><p>Istio正试图解决通过云平台运行应用程序时可能面临的一些非常困难的挑战：应用程序网络、可靠性、可观测性以及（本文重点介绍的）安全性。借助Istio，网格中不同服务之间的通信将变得更安全，并且默认便会被加密。Istio还有助于解决“源头”和“最终用户”的JWT标识令牌验证问题。</p> <i>By Christian Posta</i> <i> Translated by 大愚若智</i>
---------------
<h1 id="#title_3" >4、文章： 推荐30个用于微服务的顶级工具</h1>
Stefan Thorpe
[http://www.infoq.com/cn/articles/30-tools-for-building-microservices?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/30-tools-for-building-microservices?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/30-tools-for-building-microservices/zh/smallimage/logo-tips-1535280027775.jpg"/><p>本文列出了很多可用于构建微服务的工具，其中大多数是免费的，可用于执行特定任务，也有一些提供了收费功能。</p> <i>By Stefan Thorpe</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_4" >5、文章： 上交大提出支持并行计算的SRNN：比RNN快136倍！（代码已开源）</h1>
马卓奇
[http://www.infoq.com/cn/articles/sliced-recurrent-neural-networks?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/sliced-recurrent-neural-networks?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/sliced-recurrent-neural-networks/zh/smallimage/logo-small-1514379998506-1535280556747.jpg"/><p>本文介绍了切片循环神经网络，可以通过将序列分割成多个子序列来实现并行化计算。SRNN具有通过多层网络和极少的额外参数来获得高层次信息的能力。不需要改变循环单元，SRNN的速度便可以达到标准RNN的136倍，而且训练更长的序列时，SRNN的速度能够更快。作者在六个大规模情感分析数据集上进行了实验，实验结果表明SRNN比标准的RNN具有更好的性能。</p> <i>By 马卓奇</i>
---------------
<h1 id="#title_5" >6、视频演讲： 玩转COS：对象存储与SCF深度结合应用</h1>
卢萌凯
[http://www.infoq.com/cn/presentations/deep-application-of-object-storage-and-scf?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/deep-application-of-object-storage-and-scf?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/presentations/deep-application-of-object-storage-and-scf/zh/mediumimage/lumengkai270-1535294744133.jpg"/><p>很多时候用户会希望对云上存储的文件做一些简单处理，比如图片缩略、音视频转码、日志分析等。作为目前大量用户选用的云上存储产品，COS可以和无服务器云函数SCF相结合，便捷实现触发回调、读取COS上传或删除事件、自动运行、完成业务逻辑；同时后端也可以对接云上其他产品，实现多产品联动。</p> <i>By 卢萌凯</i>
---------------
<h1 id="#title_6" >7、从摩尔定律到人工智能，指数定律释放人类潜能</h1>
Sharon
[http://www.infoq.com/cn/news/2018/08/law-of-indices-release-potential?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/08/law-of-indices-release-potential?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>你学过指数吗？恐怕没几个人会对这个问题说 “No”。 指数式发展实实在在地就在我们身边、在我们手上发生。不相信吗？看看你的手机。</p> <i>By Sharon</i>
---------------
<h1 id="#title_7" >8、微软将开源其对抗云网络中断的秘密武器</h1>
Yevgeniy Sverdlik
[http://www.infoq.com/cn/news/2018/08/Microsoft-Open-Network-Emulator?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/08/Microsoft-Open-Network-Emulator?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>微软的研究人员说，他们正在打算开源开放网络模拟器，该系统模拟了为微软的超大规模云平台提供动力的整个网络。近一年来，微软利用它对网络的更改在被部署到生产中前进行测试。研究人员说，微软的网络工程师在建议的更改中找到了数百个错误，从而防止了可能出现的重大中断错误。</p> <i>By Yevgeniy Sverdlik</i> <i> Translated by 姚佳灵</i>
---------------
<h1 id="#title_8" >9、全球物流无人机发展报告：前景广阔，未来三年为关键期</h1>
陈利鑫
[http://www.infoq.com/cn/news/2018/08/logistics-drones-furtudevreport?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/08/logistics-drones-furtudevreport?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>当前，物流无人机的热度再起，电商、物流，甚至似乎航空制造业、互联网平台企业也纷纷加码，规模化商用也不再是影视作品中酷炫的设想。</p> <i>By 陈利鑫</i>
---------------