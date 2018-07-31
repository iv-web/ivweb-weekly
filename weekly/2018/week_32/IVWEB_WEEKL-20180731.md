## 文章索引
1、 <a href="#1what-do-you-need-to-know-when-converting-a-flash-game-into-html5" >What Do You Need To Know When Converting A Flash Game Into HTML5?</a><br/>
2、 <a href="#2css-的空格处理" >CSS 的空格处理</a><br/>
3、 <a href="#3为什么说json不适合做配置文件" >为什么说JSON不适合做配置文件？</a><br/>
4、 <a href="#4文章-如何docker化任意一个应用" >文章： 如何Docker化任意一个应用</a><br/>
5、 <a href="#5文章-软件项目开发中的三个不应做事项" >文章： 软件项目开发中的三个“不应做”事项</a><br/>
6、 <a href="#6文章-docker和微服务的崛起" >文章： Docker和微服务的崛起</a><br/>
7、 <a href="#7文章-kubernetes会不会被自身的复杂性压垮" >文章： Kubernetes会不会被自身的复杂性压垮？</a><br/>
8、 <a href="#8谷歌为什么要对android的开源严防死守" >谷歌为什么要对Android的开源严防死守？</a><br/>
9、 <a href="#9明略成立科学院ieee-fellow吴信东任院长" >明略成立科学院，IEEE Fellow吴信东任院长</a><br/>
10、 <a href="#10android-studio-32-beta-3引入了新的navigation-editorandroid-app-bundle等特性" >Android Studio 3.2 Beta 3引入了新的Navigation Editor、Android App Bundle等特性</a><br/>
11、 <a href="#11hashicorp发布consul-121带来consul-connect服务网格解决方案" >HashiCorp发布Consul 1.2.1，带来Consul Connect服务网格解决方案</a><br/>
12、 <a href="#12谷歌云服务故障原因分析和补救措施" >谷歌云服务故障原因分析和补救措施</a><br/>
13、 <a href="#13文章-如何正确使用async/await" >文章： 如何正确使用async/await？</a><br/>
14、 <a href="#14webide在浏览器中写代码的时代即将来临" >WebIDE：在浏览器中写代码的时代即将来临？</a><br/>
15、 <a href="#15视频演讲-region多可用区架构及同城多活方案实践" >视频演讲： Region多可用区架构及同城多活方案实践</a><br/><h1 id="#title_0" >1、What Do You Need To Know When Converting A Flash Game Into HTML5?</h1>
Tomasz Grajewski
[https://www.smashingmagazine.com/2018/07/converting-flash-game-html5/](https://www.smashingmagazine.com/2018/07/converting-flash-game-html5/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/07/converting-flash-game-html5/" />
              <title>What Do You Need To Know When Converting A Flash Game Into HTML5?</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>What Do You Need To Know When Converting A Flash Game Into HTML5?</h1>
                  
                    
                    <address>Tomasz Grajewski</address>
                  
                  <time datetime="2018-07-30T14:00:26&#43;02:00" class="op-published">2018-07-30T14:00:26+02:00</time>
                  <time datetime="2018-07-30T21:54:11&#43;00:00" class="op-modified">2018-07-30T21:54:11+00:00</time>
                </header>
                <p>With the rise of HTML5 usage, many companies start redoing their most popular titles to get rid of outdated Flash and match their products to the latest industry standards. This change is especially visible in the Gambling/Casino & Entertainment industries and has been happening for several years now, so a decent selection of titles has already been converted.</p>

<p>Unfortunately, when browsing the Internet, you can quite often stumble upon examples of a seemingly hasty job, which results in the lover quality of the final product. That's why it's a good idea for game developers to dedicate some of their time for getting familiar with the subject of Flash to HTML5 conversion and learning which mistakes to avoid before getting down to work.</p>

<p>Among the reasons for choosing JavaScript instead of Flash, apart from the obvious technical issues, is also the fact that changing your game design from SWF to JavaScript can yield a better user experience, which in turn give it a modern look. But how to do it? Do you need a dedicated JavaScript game converter to get rid of this outdated technology? Well, Flash to HTML5 conversion can be a piece of cake &mdash; here's how to take care of it.</p>

<p><strong>Recommended reading</strong>: <em></em></p>

<h3>How To Improve HTML5 Game Experience</h3>

<p>Converting a game to another platform is an excellent opportunity to improve it, fix its issues, and increase the audience. Below are few things that can be easily done and are worth considering:</p>

<ul>
<li><p><strong>Supporting mobile devices</strong><br />Converting from Flash to JavaScript allows reaching a broader audience (users of mobile devices); support for touchscreen controls usually needs to be implemented into the game, too. Luckily, both Android and iOS devices now also support WebGL, so 30 or 60 FPS rendering usually can be easily achieved. In many cases, 60 FPS won't cause any problems, which will only improve with time, as mobile devices become more and more performant.</p></li>
<li><strong>Improving performance</strong><br />When it comes to comparing ActionScript and JavaScript, the latter is faster than the first one. Other than that, converting a game is a good occasion to revisit algorithms used in game code. With JavaScript game development you can optimize them or completely strip unused code that’s left by original developers.</li>
<li><strong>Fixing bugs and making improvements to the gameplay</strong><br />Having new developers looking into game’s source code can help to fix known bugs or discover new and very rare ones. This would make playing the game less irritating for the players, which would make them spend more time on your site and encourage to try your other games.</li>
<li><strong>Adding web analytics</strong><br />In addition to tracking the traffic, web analytics can also be used to gather knowledge on how players behave in a game and where they get stuck during gameplay.</li>
<li><strong>Adding localization</strong><br />This would increase the  audience and is important for kids from other countries playing your game. Or maybe your game is not in English and you want to support that language?</li>
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




<h3>Why Skipping HTML And CSS For In-Game UI Will Improve Game Performance</h3>

<p>When it comes to JavaScript game development, it may be tempting to leverage HTML and CSS for in-game buttons, widgets, and other GUI elements. My advice is to be careful here. It’s counterintuitive, but actually leveraging DOM elements is less performant on complex games and this gains more significance on mobile. If you want to achieve constant 60 FPS on all platforms, then resigning from HTML and CSS may be required.</p>

<p>Non-interactive GUI elements, such as health bars, ammo bars, or score counters can be easily implemented in Phaser by using regular images (the <code>Phaser.Image</code> class), leveraging the <code>.crop</code> property for trimming and the <code>Phaser.Text</code> class for simple text labels.</p>

<p>Such interactive elements as buttons and checkboxes can be implemented by using the built-in <code>Phaser.Button</code> class. Other, more complex elements can be composed of different simple types, like groups, images, buttons and text labels.</p>

<p><strong>Note:</strong> <em>Each time you instantiate a Phaser.Text or PIXI.Text object, a new texture is created to render text onto. This additional texture breaks vertex batching, so be careful not to have too many of them</em>.</p>

<h3>How To Ensure That Custom Fonts Have Loaded</h3>

<p>If you want to render text with a custom vector font (e.g. TTF or OTF), then you need to ensure that the font has already been loaded by the browser before rendering any text. Phaser v2 doesn’t provide a solution for this purpose, but another library can be used: .</p>

<p>Assuming that you have a font file and include the Web Font Loader in your page, then below is a simple example of how to load a font:</p>

<p>Make a simple CSS file that will be loaded by Web Font Loader (you don’t need to include it in your HTML):</p>

<pre><code class="language-css">@font-face {
    // This name you will use in JS
    font-family: 'Gunplay';
    // URL to the font file, can be relative or absolute
    src: url('../fonts/gunplay.ttf') format('truetype');
    font-weight: 400;
}
</code></pre>

<p>Now define a global variable named <code>WebFontConfig</code>. Something as simple as this will usually suffice:</p>

<pre><code class="language-javascript">var WebFontConfig = {
   'classes': false,
   'timeout': 0,
   'active': function() {
       // The font has successfully loaded...
   },
   'custom': {
       'families': ['Gunplay'],
       // URL to the previously mentioned CSS
       'urls': ['styles/fonts.css']
   }
};
</code></pre>

<p>It the end, remember to put your code in the ‘active’ callback shown above. And that’s it!</p>

<h3>How To Make It Easier For Users To Save The Game</h3>

<p>To persistently store local data in ActionScript you would use the SharedObject class. In JavaScript, the simple replacement is , which allows storing strings for later retrieval, surviving page reloads.</p>

<p>Saving data is very simple:</p>

<pre><code class="language-javascript">var progress = 15;
localStorage.setItem('myGame.progress', progress);
</code></pre>

<p>Note that in the above example the <code>progress</code> variable, which is a number, will be converted to a string.</p>

<p>Loading is simple too, but remember that retrieved values will be strings or <code>null</code> if they don’t exists.</p>

<pre class="break-out"><code class="language-javascript">var progress = parseInt(localStorage.getItem('myGame.progress')) || 0;
</code></pre>

<p>Here we’re ensuring that the return value is a number. If it doesn’t exist, then 0 will be assigned to the <code>progress</code> variable.</p>

<p>You can also store and retrieve more complex structures, for example, JSON:</p>

<pre class="break-out"><code class="language-javascript">var stats = {'goals': 13, 'wins': 7, 'losses': 3, 'draws': 1};
localStorage.setItem('myGame.stats', JSON.stringify(stats));
…
var stats = JSON.parse(localStorage.getItem('myGame.stats')) || {};
</code></pre>

<p>There are some cases when the localStorage object won’t be available. For example, when using the <code>file://</code> protocol or when a page is loaded in a private window. You can use the try and catch statement to ensure your code will both continue working and use default values, what is shown in the example below:</p>

<pre class="break-out"><code class="language-javascript">try {
    var progress = localStorage.getItem('myGame.progress');
} catch (exception) {
    // localStorage not available, use default values
}
</code></pre>

<p>Another thing to remember is that the stored data is saved per domain, not per URL. So if there is a risk that many games are hosted on a single domain, then it’s better to use a prefix (namespace) when saving. In the example above <code>'myGame.'</code> is such a prefix and you usually want to replace it with the name of the game.</p>

<p><strong>Note</strong>: <em>If your game is embedded in an iframe, then localStorage won’t persist on iOS. In this case, you would need to store data in the parent iframe instead</em>.</p>

<div class="sponsors__wide-place"></div>




<h3>How To Leverage Replacing Default Fragment Shader</h3>

<p>When Phaser and PixiJS render your sprites, they use a simple internal fragment shader. It doesn’t have many features because it’s tailored for a speed. However, you can replace that shader for your purposes. For example, you can leverage it to inspect overdraw or support more features for rendering.</p>

<p>Below is an example of how to supply your own default fragment shader to Phaser v2:</p>

<pre class="break-out"><code class="language-javascript">function preload() {
    this.load.shader('filename.frag', 'shaders/filename.frag');
}

function create() {
    var renderer = this.renderer;
    var batch = renderer.spriteBatch;
    batch.defaultShader = 
        new PIXI.AbstractFilter(this.cache.getShader('filename.frag'));
    batch.setContext(renderer.gl);
}
</code></pre>

<p><strong>Note:</strong> <em>It’s important to remember that the default shader is used for ALL sprites as well as when rendering to a texture. Also, keep in mind that using complex shaders for all in-game sprites will greatly reduce rendering performance</em>.</p>

<h3>How To Change Tinting Method With A Default Shader</h3>

<p>Custom default shader can be used to replace default tinting method in Phaser and PixiJS.</p>

<p>Tinting in Phaser and PixiJS works by multiplying texture pixels by a given color. Multiplication always darkens colors, which obviously is not a problem; it's simply different from the Flash tinting. For one of our games, we needed to implement tinting similar to Flash and decided that a custom default shader could be used. Below is an example of such fragment shader:</p>

<pre class="break-out"><code class="language-css">// Specific tint variant, similar to the Flash tinting that adds
// to the color and does not multiply. A negative of a color
// must be supplied for this shader to work properly, i.e. set
// sprite.tint to 0 to turn whole sprite to white.
precision lowp float;

varying vec2 vTextureCoord;
varying vec4 vColor;

uniform sampler2D uSampler;

void main(void) {
    vec4 f = texture2D(uSampler, vTextureCoord);
    float a = clamp(vColor.a, 0.00001, 1.0);
    gl_FragColor.rgb = f.rgb * vColor.a + clamp(1.0 - vColor.rgb/a, 0.0, 1.0) * vColor.a * f.a;
    gl_FragColor.a = f.a * vColor.a;
}
</code></pre>

<p>This shader lightens pixels by adding a base color to the tint one. For this to work, you need to supply negative of the color you want. Therefore, in order to get white, you need to set:</p>

<pre class="break-out"><code class="language-css">sprite.tint = 0x000000;  // This colors the sprite to white
Sprite.tint = 0x00ffff;  // This gives red
</code></pre>

<p>The result in our game looks like this (notice how tanks flash white when hit):</p>

<figure><figcaption>Custom default shader (tanks flashing white).</figcaption></figure>

<h3>How To Inspect Overdraw To Detect Fill Rate Issues</h3>

<p>Replacing default shader can also be leveraged to help with debugging. Below I've explained how overdraw can be detected with such a shader.</p>

<p>Overdrawing happens when many or all pixels on the screen are rendered multiple times. For example, many objects taking the same place and being rendered one over another. How many pixels a GPU can render per second is described as fill rate. Modern desktop GPUs have excessive fill rate for usual 2D purposes, but mobile ones are a lot slower.</p>

<p>There is a simple method of finding out how many times each pixel on the screen is written by replacing the default global fragment shader in PixiJS and Phaser with this one:</p>

<pre><code class="language-css">void main(void) {
    gl_FragColor.rgb += 1.0 / 7.0;
}
</code></pre>

<p>This shader lightens pixels that are being processed. The number 7.0 indicates how many writes are needed to turn pixel white; you can tune this number to your liking. In other words, lighter pixels on screen were written several times, and white pixels were written at least 7 times.</p>

<p>This shader also helps to find both “invisible” objects that for some reason are still rendered and sprites that have excessive transparent areas around that need to be stripped (GPU still needs to process transparent pixels in your textures).</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e922ec9a-9236-43b0-bb4f-7c2ef445204d/overdraw.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e922ec9a-9236-43b0-bb4f-7c2ef445204d/overdraw.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e922ec9a-9236-43b0-bb4f-7c2ef445204d/overdraw.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e922ec9a-9236-43b0-bb4f-7c2ef445204d/overdraw.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e922ec9a-9236-43b0-bb4f-7c2ef445204d/overdraw.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e922ec9a-9236-43b0-bb4f-7c2ef445204d/overdraw.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e922ec9a-9236-43b0-bb4f-7c2ef445204d/overdraw.png"
			sizes="100vw"
			alt="Example of the Overdraw shader in action in game development"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Overdraw shader in action. ()
		</figcaption>
	
</figure>


<p>The picture on the left shows how a player sees the game, while the one on the right displays the effect of applying the overdraw shader to the same scene.</p>

<h3>Why Physics Engines Are Your Friends</h3>

<p>A physics engine is a middleware that's responsible for simulating physics bodies (usually rigid body dynamics) and their collisions. Physics engines simulate 2D or 3D spaces, but not both. A typical physics engine will provide:</p>

<ul>
<li>object movement by setting velocities, accelerations, joints, and motors;</li>
<li>detecting collisions between various shape types;</li>
<li>calculating collision responses, i.e. how two objects should react when they collide.</li>
</ul>

<p>At Merixstudio, we’re big fans of the Box2D physics engine and used it on a few occasions. There is a  that works well for this purpose. Box2D is also used in the Unity game engine and GameMaker Studio 2.</p>

<p>While a physics engine will speed-up your development, there is a price you'll have to pay: reduced runtime performance. Detecting collisions and calculating responses is a CPU-intensive task. You may be limited to several dozen dynamic objects in a scene on mobile phones or face degraded performance, as well as reduced frame rate deep below 60 FPS.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/00d39e63-9c0e-4235-bf56-8b3a3e3f5c8a/physics.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/00d39e63-9c0e-4235-bf56-8b3a3e3f5c8a/physics.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/00d39e63-9c0e-4235-bf56-8b3a3e3f5c8a/physics.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/00d39e63-9c0e-4235-bf56-8b3a3e3f5c8a/physics.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/00d39e63-9c0e-4235-bf56-8b3a3e3f5c8a/physics.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/00d39e63-9c0e-4235-bf56-8b3a3e3f5c8a/physics.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/00d39e63-9c0e-4235-bf56-8b3a3e3f5c8a/physics.png"
			sizes="100vw"
			alt="Example of the difference in the scene of a game with and withour Phaser physics debug overlay displayed on top"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Phaser's physics debug overlay. ()
		</figcaption>
	
</figure>


<p>The left part of the image is a scene from a game, while the right side shows the same scene with Phaser physics debug overlay displayed on top.</p>

<div class="sponsors__wide-place"></div>




<h3>How To Export Sounds From A <em>.fla</em> File</h3>

<p>If you have a Flash game sound effects inside of a <em>.fla</em> file, then exporting them from GUI is not possible (at least not in Adobe Animate CC 2017)  due to the lack of menu option serving this purpose. But there is another solution &mdash; a dedicated script that does just that:</p>

<pre class="break-out"><code class="language-javascript">function normalizeFilename(name) {
   // Converts a camelCase name to snake_case name
   return name.replace(/([A-Z])/g, '_$1').replace(/^_/, '').toLowerCase();
}

function displayPath(path) {
   // Makes the file path more readable
   return unescape(path).replace('file:///', '').replace('|', ':');
}


fl.outputPanel.clear();

if (fl.getDocumentDOM().library.getSelectedItems().length > 0)
   // Get only selected items
   var library = fl.getDocumentDOM().library.getSelectedItems();
else
   // Get all items
   var library = fl.getDocumentDOM().library.items;

// Ask user for the export destination directory
var root = fl.browseForFolderURL('Select a folder.');
var errors = 0;

for (var i = 0; i < library.length; i++) {
   var item = library[i];
   if (item.itemType !== 'sound')
       continue;

   var path = root + '/';

   if (item.originalCompressionType === 'RAW')
       path += normalizeFilename(item.name.split('.')[0]) + '.wav';
   else
       path += normalizeFilename(item.name);

   var success = item.exportToFile(path);
   if (!success)
       errors += 1;
   fl.trace(displayPath(path) + ': ' + (success ? 'OK' : 'Error'));
}

fl.trace(errors + ' error(s)');
</code></pre>

<p>How to use the script to export sound files:</p>

<ol>
<li>Save the code above as a <em>.jsfl</em> file on your computer;</li>
<li>Open a <em>.fla</em> file with Adobe Animate;</li>
<li>Select ‘Commands’ &rarr; ‘Run Command’ from the top menu and select the script in the dialogue that opens;</li>
<li>Now another dialogue file pops up for selecting export destination directory.</li>
</ol>

<p>And done! You should now have WAV files in the specified directory. What’s left to do is convert them to, for example, MP3’s, OGG, or AAC.</p>

<h3>How To Use MP3s In Flash To HTML5 Convertions</h3>

<p>The good old MP3 format is back, as some patents have expired and now every browser can decode and play MP3’s. This makes development a bit easier since finally there's no need to prepare two separate audio formats. Previously you needed, for instance, OGG and AAC files, while now MP3 will suffice.</p>

<p>Nonetheless, there are two important things you need to remember about MP3:</p>

<ul>
<li>MP3’s need to decode after loading, what can be time-consuming, especially on mobile devices. If you see a pause after all your assets have loaded, then it probably means that MP3’s being decoded;</li>
<li>gaplessly playing looped MP3’s is a little problematic. The solution is to use mp3loop, about which you can read in .</li>
</ul>

<h3>So, Why Should You Convert Flash To JavaScript?</h3>

<p>As you can see, Flash to JavaScript conversion is not impossible if you know what to do. With knowledge and skill, you can stop struggling with Flash and enjoy the smooth, entertaining games created in JavaScript. Don't try to fix Flash &mdash; get rid of it before everyone is forced to do so!</p>

<h3>Want To Learn More?</h3>

<p>In this article, I was focused mainly on Phaser v2. However, a newer version of  is now available, and I strongly encourage you to check it out, as it introduced a plethora of fresh, cool features, such as multiple cameras, scenes, tilemaps, or Matter.js physics engine.</p>

<p>If you are brave enough and want to create truly remarkable things in browsers, then WebGL is the right thing to learn from the ground up. It’s a lower level of abstraction than various game-building frameworks or tools but allows to achieve greater performance and quality even if you work on 2D games or demos. Among many websites which you may find useful when learning the basics of WebGL would be .</p>

<p>Always remember that there's no such thing as too much knowledge &mdash; especially when it comes to game development!</p>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(rb, ra, yk, il)</span>
</div>


              </article>
            </body>
          </html>
---------------
<h1 id="#title_1" >2、CSS 的空格处理</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2018/07/white-space.html](http://www.ruanyifeng.com/blog/2018/07/white-space.html)
<h2>一、空格规则</h2>

<p>HTML 代码的空格通常会被浏览器忽略。</p>

        <p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018073106.jpg" alt="" title="" /></p>

<blockquote><pre><code class="language-markup">
&lt;p>◡◡hello◡◡world◡◡&lt;/p>
</code></pre></blockquote>

<p>上面是一行 HTML 代码，文字的前部、内部和后部各有两个空格。为了便于识别，这里使用半圆形符号<code>◡</code>表示空格。</p>

<p>浏览器的输出结果如下。</p>

<blockquote><pre><code class="language-markup">
hello world
</code></pre></blockquote>

<p>可以看到，文字的前部和后部的空格都会忽略，内部的连续空格只会算作一个。这就是浏览器处理空格的基本规则。</p>

<p>如果希望空格原样输出，可以使用<code>&lt;pre&gt;</code>标签。</p>

<blockquote><pre><code class="language-markup">
&lt;pre>◡◡hello◡◡world◡◡&lt;/pre>
</code></pre></blockquote>

<p>另一种方法是，改用 HTML 实体<code>&amp;nbsp;</code>表示空格。</p>

<blockquote><pre><code class="language-markup">
&lt;p>&amp;nbsp;&amp;nbsp;hello&amp;nbsp;&amp;nbsp;world&amp;nbsp;&amp;nbsp;&lt;/p>
</code></pre></blockquote>

<h2>二、空格字符</h2>

<p>HTML 处理空格的规则，适用于多种字符。除了普通的空格键，还包括制表符（<code>\t</code>）和换行符（<code>\r</code>和<code>\n</code>）。</p>

<p>浏览器会自动把这些符号转成普通的空格键。</p>

<blockquote><pre><code class="language-markup">
&lt;p>hello
world&lt;/p>
</code></pre></blockquote>

<p>上面代码中，文本内部包含了一个换行符，浏览器视同为空格，输出结果如下。</p>

<blockquote><pre><code class="language-markup">
hello world
</code></pre></blockquote>

<p>所以，文本内部的换行是无效的（除非文本放在<code>&lt;pre&gt;</code>标签内）。</p>

<blockquote><pre><code class="language-markup">
&lt;p>hello&lt;br>world&lt;/p>
</code></pre></blockquote>

<p>上面代码使用<code>&lt;br&gt;</code>标签显式表示换行。</p>

<h2>三、CSS 的 white-space 属性</h2>

<p>HTML 语言的空格处理，基本上就是直接过滤。这样的处理过于粗糙，完全忽视了原始文本内部的空格可能是有意义的。</p>

<p>CSS 提供了一个<code>white-space</code>属性，可以提供更精确一点的空格处理方式。该属性共有六个值，除了一个通用的<code>inherit</code>（继承父元素），下面依次介绍剩下的五个值。</p>

<h3>3.1 white-space: normal</h3>

<p><code>white-space</code>属性的默认值为<code>normal</code>，表示浏览器以正常方式处理空格。</p>

<blockquote><pre><code class="language-markup">
&lt;p>◡◡hellohellohello◡hello
world
&lt;/p>
</code></pre></blockquote>

<p>上面代码中，文本前部有两个空格，内部有一个长单词和一个换行符。</p>

<p>然后，容器<code>&lt;p&gt;</code>指定一个比较小的宽度。为了便于识别，背景色设为红色。</p>

<blockquote><pre><code class="language-css">
p {
  width: 100px;
  background: red;
}
</code></pre></blockquote>

<p>显示效果如下图。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018073101.png" alt="" title="" /></p>

<p>可以看到，文首的空格被忽略。由于容器太窄，第一个单词溢出容器，然后在后面一个空格处换行。文本内部的换行符自动转成了空格。</p>

<h3>3.2 white-space: nowrap</h3>

<p><code>white-space</code>属性为<code>nowrap</code>时，不会因为超出容器宽度而发生换行。</p>

<blockquote><pre><code class="language-css">
p {
  white-space: nowrap;
}
</code></pre></blockquote>

<p>显示效果如下图。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018073102.png" alt="" title="" /></p>

<p>所有文本显示为一行，不会换行。</p>

<h3>3.3 white-space: pre</h3>

<p><code>white-space</code>属性为<code>pre</code>时，就按照<code>&lt;pre&gt;</code>标签的方式处理。</p>

<blockquote><pre><code class="language-css">
p {
  white-space: pre;
}
</code></pre></blockquote>

<p>显示效果如下图。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018073103.png" alt="" title="" /></p>

<p>上面结果与原始文本完全一致，所有空格和换行符都保留了。</p>

<h3>3.4 white-space: pre-wrap</h3>

<p><code>white-space</code>属性为<code>pre-wrap</code>时，基本还是按照<code>&lt;pre&gt;</code>标签的方式处理，唯一区别是超出容器宽度时，会发生换行。</p>

<blockquote><pre><code class="language-css">
p {
  white-space: pre-wrap;
}
</code></pre></blockquote>

<p>显示效果如下图。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018073104.png" alt="" title="" /></p>

<p>文首的空格、内部的空格和换行符都保留了，超出容器的地方发生了折行。</p>

<h3>3.5 white-space: pre-line</h3>

<p><code>white-space</code>属性为<code>pre-line</code>时，意为保留换行符。除了换行符会原样输出，其他都与<code>white-space:normal</code>规则一致。</p>

<blockquote><pre><code class="language-css">
p {
  white-space: pre-line;
}
</code></pre></blockquote>

<p>显示效果如下图。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018073105.png" alt="" title="" /></p>

<p>除了文本内部的换行符没有转成空格，其他都与<code>normal</code>的处理规则一致。这对于诗歌类型的文本很有用。</p>

<h2>四、参考链接</h2>

<ul>
<li>，by Patrick Brosset</li>
<li>，by Sara Cope </li>
</ul>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2018-07-30T20:25:09+08:00">2018年7月30日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>文集：</li>
<li>社交媒体：</li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------
<h1 id="#title_2" >3、为什么说JSON不适合做配置文件？</h1>
Thayne McCombs
[http://www.infoq.com/cn/news/2018/07/json-isnt-good-configlang?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/json-isnt-good-configlang?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>有了这么多更好的配置语言，没有理由还要使用JSON。如果要创建需要用到配置的新应用程序、框架或库，请选择JSON以外的其他选项。</p> <i>By Thayne McCombs</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_3" >4、文章： 如何Docker化任意一个应用</h1>
Henrique Souza
[http://www.infoq.com/cn/articles/how-to-dockerize-any-application?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/how-to-dockerize-any-application?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/how-to-dockerize-any-application/zh/smallimage/logo-ieee-1532807702798.jpg"/><p>这是一篇关于如何Docker化任何应用程序的十步清单。</p> <i>By Henrique Souza</i> <i> Translated by 金灵杰</i>
---------------
<h1 id="#title_4" >5、文章： 软件项目开发中的三个“不应做”事项</h1>
Lawrence Putnam  Jr
[http://www.infoq.com/cn/articles/not-skip-estimation-planning?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/not-skip-estimation-planning?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/not-skip-estimation-planning/zh/smallimage/logo-agile-1530027106665-1532714122266.jpeg"/><p>大量的项目经验表明，仓促进入开发阶段的软件项目注定会失败。在不破坏时间表和超出预算的情况下，要交付质量合格的项目，关键在于做好估算和预先计划。</p> <i>By Lawrence Putnam  Jr</i> <i> Translated by 盖磊</i>
---------------
<h1 id="#title_5" >6、文章： Docker和微服务的崛起</h1>
Karthic Rao, Abraar Syed
[http://www.infoq.com/cn/articles/docker-and-the-rise-of-micorservice?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/docker-and-the-rise-of-micorservice?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/docker-and-the-rise-of-micorservice/zh/smallimage/agil-series-1508534878617-1532805349248.jpeg"/><p>本文介绍了微服务的崛起和Docker之间的关系。</p> <i>By Karthic Rao</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_6" >7、文章： Kubernetes会不会被自身的复杂性压垮？</h1>
Paul Dix
[http://www.infoq.com/cn/articles/will-kubernetes-collapse-under-the-weight-of-its-complexity?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/will-kubernetes-collapse-under-the-weight-of-its-complexity?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/will-kubernetes-collapse-under-the-weight-of-its-complexity/zh/smallimage/logo+%285%29-1532804764752.jpg"/><p>Kubernetes是否太复杂了？它会被自身的复杂性压垮吗？</p> <i>By Paul Dix</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_7" >8、谷歌为什么要对Android的开源严防死守？</h1>
覃云
[http://www.infoq.com/cn/news/2018/07/google-control-androidopensource?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/google-control-androidopensource?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>上周，沸沸扬扬的Android垄断案把Google又一次推向了风口浪尖，在这次的垄断案中，Google被欧盟起诉赔偿50亿美元，被起诉的其中一个原因是Google对外宣称Android是开放的，但其实他们只是开源了一部分代码，很多重要的代码都是闭源的。</p> <i>By 覃云</i>
---------------
<h1 id="#title_8" >9、明略成立科学院，IEEE Fellow吴信东任院长</h1>
陈利鑫
[http://www.infoq.com/cn/news/2018/07/minglue-ieee-fellow?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/minglue-ieee-fellow?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>7月27日，大数据公司明略数据宣布成立明略科学院（MAS，Minglamp Academy of Sciences），由国家“千人计划”特聘专家、长江学者、IEEE & AAAS Fellow吴信东出任院长。</p> <i>By 陈利鑫</i>
---------------
<h1 id="#title_9" >10、Android Studio 3.2 Beta 3引入了新的Navigation Editor、Android App Bundle等特性</h1>
Diogo Carleto
[http://www.infoq.com/cn/news/2018/07/android-studio-3.2-beta-3?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/android-studio-3.2-beta-3?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Google在其Beta频道上发布了Android Studio 3.2 Beta 3。这个版本引入了新的Assistant和Navigation Editor，另外还包含Android Jetpack、AndroidX迁移、Android App Bundle、新的Android Profiler、Lint检查等功能。</p> <i>By Diogo Carleto</i> <i> Translated by 张卫滨 </i>
---------------
<h1 id="#title_10" >11、HashiCorp发布Consul 1.2.1，带来Consul Connect服务网格解决方案</h1>
Daniel Bryant
[http://www.infoq.com/cn/news/2018/07/consul-connect?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/consul-connect?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>HashiCorp发布了Consul 1.2.1，这是其高可用、分布式服务发现和键-值存储的最新版本，该版本还包含Consul Connect的公开测试版。Consul Connect使用Mutual TLS提供服务到服务的连接授权和加密，并且能够“自动把现有的任何Consul集群转换成服务网格解决方案”。</p> <i>By Daniel Bryant</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_11" >12、谷歌云服务故障原因分析和补救措施</h1>
Sergio De Simone
[http://www.infoq.com/cn/news/2018/07/google-cloud-incident-analysis?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/google-cloud-incident-analysis?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>谷歌公布了近期的一个事件的根本原因分析结果，该事件影响了谷歌的部分云服务，并在大约32分钟的时间内将错误率提高了33％至87％，后续他们将采取措施改善平台性能和可用性。</p> <i>By Sergio De Simone</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_12" >13、文章： 如何正确使用async/await？</h1>
Charlee Li
[http://www.infoq.com/cn/articles/javascript-async-await-the-good-part-pitfalls-and-how-to-use?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/javascript-async-await-the-good-part-pitfalls-and-how-to-use?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/javascript-async-await-the-good-part-pitfalls-and-how-to-use/zh/smallimage/GettyImages-499691816-copy-1532806428871.jpeg"/><p>ES7引入的async/await是JavaScript异步编程的一个重大改进，提供了在不阻塞主线程的情况下使用同步代码异步访问资源的能力。在本文中，我们将从不同的角度探索async/await，并演示如何正确有效地使用它们。</p> <i>By Charlee Li</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_13" >14、WebIDE：在浏览器中写代码的时代即将来临？</h1>
徐川
[http://www.infoq.com/cn/news/2018/07/webide-explorecode?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/webide-explorecode?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>云计算拥有现代网络应用最重要的基础——资源，以后应用的开发毫无疑问将围绕着云来进行。WebIDE是这股潮流中的一朵浪花，我相信，它和其它工具一起，将彻底改变我们的开发习惯。</p> <i>By 徐川</i>
---------------
<h1 id="#title_14" >15、视频演讲： Region多可用区架构及同城多活方案实践</h1>
陈剑豪
[http://www.infoq.com/cn/presentations/region-multi-area-structure-and-multi-city-living-plan?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/region-multi-area-structure-and-multi-city-living-plan?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/presentations/region-multi-area-structure-and-multi-city-living-plan/zh/mediumimage/chenjianhao270-1532435563389.jpg"/><p>对于生产级业务而言，高可用架构的重要性不言而喻。面对种种不可抗力导致的故障，生产级业务能否顺利应对？异地多机房部署带来的延迟增大该如何优化？高可用方案因业务而异，但万变不离其宗。作为云服务提供商，我们如何能够在基础设施层面提供更便捷、高效的高可用服务能力？作为云服务的受益者，您如何能够更优雅地利用基础设施构建稳定的生产级服务？

本次演讲将介绍Region的多可用区架构是如何实现的，以及如何构建同城多活系统。</p> <i>By 陈剑豪</i>
---------------