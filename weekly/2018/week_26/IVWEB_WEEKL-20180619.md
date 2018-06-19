## 文章索引
1、 <a href="#1javascript-的-this-原理" >JavaScript 的 this 原理</a><br/>
2、 <a href="#2spritejs-canvas动画从未如此简单" >SpriteJS —— Canvas动画从未如此简单</a><br/>
3、 <a href="#3bem-for-beginners:-why-you-need-bem" >BEM For Beginners: Why You Need BEM</a><br/>
4、 <a href="#4文章-对话vitalik-buterin" >文章： 对话Vitalik Buterin</a><br/>
5、 <a href="#5文章-阿里提出电商搜索全局排序方法淘宝无线主搜gmv提升5" >文章： 阿里提出电商搜索全局排序方法，淘宝无线主搜GMV提升5%</a><br/>
6、 <a href="#6文章-科技发展是如何通过碎片化来影响未来工作的" >文章： 科技发展是如何通过碎片化来影响未来工作的</a><br/>
7、 <a href="#7京东构建了全球最大的kubernetes集群没有之一" >京东构建了全球最大的Kubernetes集群，没有之一</a><br/>
8、 <a href="#8隐私和安全是macos-mojave和safari-12的第一要务" >隐私和安全是macOS Mojave和Safari 12的第一要务</a><br/><h1 id="#title_0" >1、JavaScript 的 this 原理</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2018/06/javascript-this.html](http://www.ruanyifeng.com/blog/2018/06/javascript-this.html)
<h2>一、问题的由来</h2>

<p>学懂 JavaScript 语言，一个标志就是理解下面两种写法，可能有不一样的结果。</p>

        <blockquote><pre><code class="language-javascript">
var obj = {
  foo: function () {}
};

var foo = obj.foo;

// 写法一
obj.foo()

// 写法二
foo()
</code></pre></blockquote>

<p>上面代码中，虽然<code>obj.foo</code>和<code>foo</code>指向同一个函数，但是执行结果可能不一样。请看下面的例子。</p>

<blockquote><pre><code class="language-javascript">
var obj = {
  foo: function () { console.log(this.bar) },
  bar: 1
};

var foo = obj.foo;
var bar = 2;

obj.foo() // 1
foo() // 2
</code></pre></blockquote>

<p>这种差异的原因，就在于函数体内部使用了<code>this</code>关键字。很多教科书会告诉你，<code>this</code>指的是函数运行时所在的环境。对于<code>obj.foo()</code>来说，<code>foo</code>运行在<code>obj</code>环境，所以<code>this</code>指向<code>obj</code>；对于<code>foo()</code>来说，<code>foo</code>运行在全局环境，所以<code>this</code>指向全局环境。所以，两者的运行结果不一样。</p>

<p>这种解释没错，但是教科书往往不告诉你，为什么会这样？也就是说，函数的运行环境到底是怎么决定的？举例来说，为什么<code>obj.foo()</code>就是在<code>obj</code>环境执行，而一旦<code>var foo = obj.foo</code>，<code>foo()</code>就变成在全局环境执行？</p>

<p>本文就来解释 JavaScript 这样处理的原理。理解了这一点，你就会彻底理解<code>this</code>的作用。</p>

<h2>二、内存的数据结构</h2>

<p>JavaScript 语言之所以有<code>this</code>的设计，跟内存里面的数据结构有关系。</p>

<blockquote><pre><code class="language-javascript">
var obj = { foo:  5 };
</code></pre></blockquote>

<p>上面的代码将一个对象赋值给变量<code>obj</code>。JavaScript 引擎会先在内存里面，生成一个对象<code>{ foo: 5 }</code>，然后把这个对象的内存地址赋值给变量<code>obj</code>。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201806/bg2018061801.png" alt="" title="" /></p>

<p>也就是说，变量<code>obj</code>是一个地址（reference）。后面如果要读取<code>obj.foo</code>，引擎先从<code>obj</code>拿到内存地址，然后再从该地址读出原始的对象，返回它的<code>foo</code>属性。</p>

<p>原始的对象以字典结构保存，每一个属性名都对应一个属性描述对象。举例来说，上面例子的<code>foo</code>属性，实际上是以下面的形式保存的。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201806/bg2018061802.png" alt="" title="" /></p>

<blockquote><pre><code class="language-javascript">
{
  foo: {
    [[value]]: 5
    [[writable]]: true
    [[enumerable]]: true
    [[configurable]]: true
  }
}
</code></pre></blockquote>

<p>注意，<code>foo</code>属性的值保存在属性描述对象的<code>value</code>属性里面。</p>

<h2>三、函数</h2>

<p>这样的结构是很清晰的，问题在于属性的值可能是一个函数。</p>

<blockquote><pre><code class="language-javascript">
var obj = { foo: function () {} };
</code></pre></blockquote>

<p>这时，引擎会将函数单独保存在内存中，然后再将函数的地址赋值给<code>foo</code>属性的<code>value</code>属性。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201806/bg2018061803.png" alt="" title="" /></p>

<blockquote><pre><code class="language-javascript">
{
  foo: {
    [[value]]: 函数的地址
    ...
  }
}
</code></pre></blockquote>

<p>由于函数是一个单独的值，所以它可以在不同的环境（上下文）执行。</p>

<blockquote><pre><code class="language-javascript">
var f = function () {};
var obj = { f: f };

// 单独执行
f()

// obj 环境执行
obj.f()
</code></pre></blockquote>

<h2>四、环境变量</h2>

<p>JavaScript 允许在函数体内部，引用当前环境的其他变量。</p>

<blockquote><pre><code class="language-javascript">
var f = function () {
  console.log(x);
};
</code></pre></blockquote>

<p>上面代码中，函数体里面使用了变量<code>x</code>。该变量由运行环境提供。</p>

<p>现在问题就来了，由于函数可以在不同的运行环境执行，所以需要有一种机制，能够在函数体内部获得当前的运行环境（context）。所以，<code>this</code>就出现了，它的设计目的就是在函数体内部，指代函数当前的运行环境。</p>

<blockquote><pre><code class="language-javascript">
var f = function () {
  console.log(this.x);
}
</code></pre></blockquote>

<p>上面代码中，函数体里面的<code>this.x</code>就是指当前运行环境的<code>x</code>。</p>

<blockquote><pre><code class="language-javascript">
var f = function () {
  console.log(this.x);
}

var x = 1;
var obj = {
  f: f,
  x: 2,
};

// 单独执行
f() // 1

// obj 环境执行
obj.f() // 2
</code></pre></blockquote>

<p>上面代码中，函数<code>f</code>在全局环境执行，<code>this.x</code>指向全局环境的<code>this</code>。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201806/bg2018061804.png" alt="" title="" /></p>

<p>在<code>obj</code>环境执行，<code>this.x</code>指向<code>obj.x</code>。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201806/bg2018061805.png" alt="" title="" /></p>

<p>回到本文开头提出的问题，<code>obj.foo()</code>是通过<code>obj</code>找到<code>foo</code>，所以就是在<code>obj</code>环境执行。一旦<code>var foo = obj.foo</code>，变量<code>foo</code>就直接指向函数本身，所以<code>foo()</code>就变成在全局环境执行。</p>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2018-06-18T15:43:41+08:00">2018年6月18日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>文集：</li>
<li>社交媒体：</li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------
<h1 id="#title_1" >2、SpriteJS —— Canvas动画从未如此简单</h1>

[https://www.h5jun.com/post/spritejs.html](https://www.h5jun.com/post/spritejs.html)
<div class="toc"><ul>
<li></li>
<li></li>
<li></li>
<li></li>
<li></li>
<li></li>
<li></li>
<li></li>
<li></li>
</ul>
</div><p>SpriteJS是一款由360奇舞团开源的跨终端canvas绘图库，可以基于canvas快速绘制结构化UI、动画和交互效果，并发布到任何拥有canvas环境的平台上（比如浏览器、小程序和node）。</p>
<p><script src="https://code.h5jun.com/js/embed.min.js?3.40.2"></script></p>
<p>我们知道，Canvas Api可以很灵活地绘制各种矢量图形到画布上，但是Canvas Api本身比较低级，比如我们要在画布中央绘制一个带有圆角的红色矩形，使用Canvas原生的Api，需要这样：</p>
<p></p>
<pre><code class="hljs lang-js"><span class="hljs-keyword">const</span> canvas = <span class="hljs-built_in">document</span>.getElementById(<span class="hljs-string">'paper'</span>),
      context = canvas.getContext(<span class="hljs-string">'2d'</span>)

<span class="hljs-keyword">const</span> [x, y, w, h, r] = [<span class="hljs-number">200</span>, <span class="hljs-number">200</span>, <span class="hljs-number">200</span>, <span class="hljs-number">200</span>, <span class="hljs-number">50</span>]

context.fillStyle = <span class="hljs-string">'red'</span>
context.beginPath()
context.moveTo(x + r, y)
context.arcTo(x + w, y, x + w, y + h, r)
context.arcTo(x + w, y + h, x, y + h, r)
context.arcTo(x, y + h, x, y, r)
context.arcTo(x, y, x + w, y, r)
context.closePath()
context.fill()
</code></pre>
<p>如果实现相同的效果，使用SpriteJS是这样写：</p>
<p></p>
<pre><code class="hljs lang-js"><span class="hljs-keyword">const</span> scene = <span class="hljs-keyword">new</span> spritejs.Scene(<span class="hljs-string">'#container'</span>),
      layer = scene.layer()

<span class="hljs-keyword">const</span> s = <span class="hljs-keyword">new</span> spritejs.Sprite({
  anchor: <span class="hljs-number">0.5</span>,
  bgcolor: <span class="hljs-string">'red'</span>,
  pos: [<span class="hljs-number">300</span>, <span class="hljs-number">300</span>],
  size: [<span class="hljs-number">200</span>, <span class="hljs-number">200</span>],
  borderRadius: <span class="hljs-number">50</span>,
})

layer.append(s)
</code></pre>
<p>Sprite为图形创建类似于DOM的对象模型，因此我们可以像创建DOM元素一样，创建Sprite元素，并将它们append到layer上，从而将元素呈现到画布上。</p>
<h3>SpriteJS 的特点</h3>
<ul>
<li>基于canvas绘制的文档对象模型</li>
<li>四种基本精灵类型：Sprite、Path、Label、Group</li>
<li>支持基础和高级的精灵属性，精灵盒模型、属性与CSS3具有高度一致性。</li>
<li>简便而强大的Transition、Animation API</li>
<li>支持雪碧图和资源预加载</li>
<li>可扩展的事件机制</li>
<li>高性能的缓存策略</li>
<li>对D3、Matter-js、Proton和其他第三方库友好</li>
<li>跨平台，支持node-canvas、微信小程序</li>
</ul>
<p><em>Sprite 文档结构</em></p>
<p><img src="https://s2.ssl.qhres.com/static/fe9c288115878476.svg" alt="Sprite文档结构"></p>
<p>SpriteJS支持设置精灵元素常用的基本属性，包括：</p>
<ul>
<li>archor: 锚点，定义元素坐标的参考点，[0,0]是左上角，[1,1]是右下角</li>
<li>size([x,y]): 精灵元素的大小</li>
<li>pos([width,height]): 精灵元素的位置</li>
<li>id: 元素的ID</li>
<li>name: 元素的name</li>
<li>bgcolor: 背景颜色</li>
<li>border: 边框</li>
<li>borderRadius: 圆角</li>
<li>padding: 同css的padding</li>
<li>zIndex: 同css的zIndex</li>
<li>textures: 精灵图片</li>
<li>filter: 滤镜</li>
<li>offsetPath: 同css3的offsetPath</li>
<li>offsetDistance: 同css3的offsetDistance</li>
<li>rotate: 旋转角度</li>
<li>scale: 缩放</li>
<li>translate: 平移</li>
<li>skew: 倾斜</li>
<li>transform: 同css3的transform</li>
</ul>
<p>如果只是绘制静态图形，SpriteJS还体现不出优势，但如果要给图形增加动画效果，那么SpriteJS内置了<strong>Transition API</strong>和标准的</p>
<p>比如我们要让上面的圆角矩形的颜色从红色过度到绿色，只需要：</p>
<p></p>
<pre><code class="hljs lang-js"><span class="hljs-keyword">const</span> scene = <span class="hljs-keyword">new</span> spritejs.Scene(<span class="hljs-string">'#container'</span>),
      layer = scene.layer()

<span class="hljs-keyword">const</span> s = <span class="hljs-keyword">new</span> spritejs.Sprite({
  anchor: <span class="hljs-number">0.5</span>,
  bgcolor: <span class="hljs-string">'red'</span>,
  pos: [<span class="hljs-number">300</span>, <span class="hljs-number">300</span>],
  size: [<span class="hljs-number">200</span>, <span class="hljs-number">200</span>],
  borderRadius: <span class="hljs-number">50</span>,
})

layer.append(s)

s.transition(<span class="hljs-number">2.0</span>).attr({bgcolor: <span class="hljs-string">'green'</span>})
</code></pre>
<p>我们可以同时对多个属性应用Transition：</p>
<p></p>
<pre><code class="hljs lang-js"><span class="hljs-keyword">const</span> scene = <span class="hljs-keyword">new</span> spritejs.Scene(<span class="hljs-string">'#container'</span>),
      layer = scene.layer()

<span class="hljs-keyword">const</span> s = <span class="hljs-keyword">new</span> spritejs.Sprite({
  anchor: <span class="hljs-number">0.5</span>,
  bgcolor: <span class="hljs-string">'red'</span>,
  pos: [<span class="hljs-number">300</span>, <span class="hljs-number">300</span>],
  size: [<span class="hljs-number">200</span>, <span class="hljs-number">200</span>],
  borderRadius: <span class="hljs-number">50</span>,
})

layer.append(s)

s.transition(<span class="hljs-number">2.0</span>)
 .attr({
  bgcolor: <span class="hljs-string">'green'</span>,
  width: width =&gt; width + <span class="hljs-number">100</span>,
 })
</code></pre>
<p>而且Transition本身返回Promise，所以我们可以方便地实现连续的Transition动画：</p>
<p></p>
<pre><code class="hljs lang-js"><span class="hljs-keyword">const</span> scene = <span class="hljs-keyword">new</span> spritejs.Scene(<span class="hljs-string">'#container'</span>),
      layer = scene.layer()

<span class="hljs-keyword">const</span> s = <span class="hljs-keyword">new</span> spritejs.Sprite({
  anchor: <span class="hljs-number">0.5</span>,
  bgcolor: <span class="hljs-string">'red'</span>,
  pos: [<span class="hljs-number">300</span>, <span class="hljs-number">300</span>],
  size: [<span class="hljs-number">200</span>, <span class="hljs-number">200</span>],
  borderRadius: <span class="hljs-number">50</span>,
})

layer.append(s)

(<span class="hljs-keyword">async</span> <span class="hljs-function"><span class="hljs-keyword">function</span>(<span class="hljs-params"></span>)</span>{
  <span class="hljs-keyword">await</span> s.transition(<span class="hljs-number">2.0</span>)
    .attr({
      bgcolor: <span class="hljs-string">'green'</span>,
      width: width =&gt; width + <span class="hljs-number">100</span>,
     })
  <span class="hljs-keyword">await</span> s.transition(<span class="hljs-number">1.0</span>)
    .attr({
      bgcolor: <span class="hljs-string">'yellow'</span>,
      height: height =&gt; height + <span class="hljs-number">100</span>,    
    })
}())
</code></pre>
<p>除了简单的Transition动画之外，我们可以使用浏览器标准的来实现更加复杂的动画，对于Web Animation API或CSS3 Animation比较熟悉的同学应该对它比较熟悉：</p>
<p></p>
<pre><code class="hljs lang-js"><span class="hljs-keyword">const</span> scene = <span class="hljs-keyword">new</span> spritejs.Scene(<span class="hljs-string">'#container'</span>),
      layer = scene.layer()

<span class="hljs-keyword">const</span> s = <span class="hljs-keyword">new</span> spritejs.Sprite({
  anchor: <span class="hljs-number">0.5</span>,
  bgcolor: <span class="hljs-string">'red'</span>,
  pos: [<span class="hljs-number">300</span>, <span class="hljs-number">300</span>],
  size: [<span class="hljs-number">200</span>, <span class="hljs-number">200</span>],
  borderRadius: <span class="hljs-number">50</span>,
})

layer.append(s)

s.animate([
  {rotate: <span class="hljs-number">0</span>, borderRadius: <span class="hljs-number">50</span>, bgcolor: <span class="hljs-string">'red'</span>},
  {rotate: <span class="hljs-number">360</span>, borderRadius: <span class="hljs-number">0</span>, bgcolor: <span class="hljs-string">'green'</span>, offset: <span class="hljs-number">0.7</span>},
  {rotate: <span class="hljs-number">720</span>, borderRadius: <span class="hljs-number">50</span>, bgcolor: <span class="hljs-string">'blue'</span>}
], {
  duration: <span class="hljs-number">3000</span>,
  iterations: <span class="hljs-literal">Infinity</span>,
  direction: <span class="hljs-string">'alternate'</span>,
  easing: <span class="hljs-string">'ease-in-out'</span>,
})
</code></pre>
<p>SpriteJS支持所有的标准Web Animation API的timing选项，另外我们也可以使用规范中定义的<code>animaton.finished</code>的Promise方便地实现顺序的动画：</p>
<p></p>
<pre><code class="hljs lang-js"><span class="hljs-keyword">const</span> scene = <span class="hljs-keyword">new</span> spritejs.Scene(<span class="hljs-string">'#container'</span>),
      layer = scene.layer()

<span class="hljs-keyword">const</span> s = <span class="hljs-keyword">new</span> spritejs.Sprite({
  anchor: <span class="hljs-number">0.5</span>,
  bgcolor: <span class="hljs-string">'red'</span>,
  pos: [<span class="hljs-number">100</span>, <span class="hljs-number">100</span>],
  size: [<span class="hljs-number">50</span>, <span class="hljs-number">50</span>],
})

<span class="hljs-keyword">const</span> s2 = s.cloneNode(<span class="hljs-literal">true</span>)
s2.attr({
  y: <span class="hljs-number">500</span>,
})

layer.append(s, s2)

;(<span class="hljs-keyword">async</span> <span class="hljs-function"><span class="hljs-keyword">function</span>(<span class="hljs-params"></span>)</span>{
  <span class="hljs-keyword">await</span> s.animate([
    {x: <span class="hljs-number">500</span>, offset: <span class="hljs-number">0.5</span>},
    {rotate: <span class="hljs-number">45</span>, bgcolor: <span class="hljs-string">'blue'</span>},
  ], {
    duration: <span class="hljs-number">2000</span>,
    fill: <span class="hljs-string">'forwards'</span>,
  }).finished

  <span class="hljs-keyword">await</span> s2.animate([
    {x: <span class="hljs-number">500</span>, offset: <span class="hljs-number">0.5</span>},
    {rotate: <span class="hljs-number">45</span>, bgcolor: <span class="hljs-string">'green'</span>},
  ], {
    duration: <span class="hljs-number">2000</span>,
    fill: <span class="hljs-string">'forwards'</span>,
  }).finished

  <span class="hljs-keyword">await</span> <span class="hljs-built_in">Promise</span>.all([s.animate([
    {y: <span class="hljs-number">500</span>}
  ], {
    duration: <span class="hljs-number">2000</span>,
    fill: <span class="hljs-string">'forwards'</span>,
  }).finished, s2.animate([
    {y: <span class="hljs-number">100</span>}
  ], {
    duration: <span class="hljs-number">2000</span>,
    fill: <span class="hljs-string">'forwards'</span>,
  }).finished])

  <span class="hljs-keyword">await</span> <span class="hljs-built_in">Promise</span>.all([s, s2].map(s =&gt; s.animate([
    {x: <span class="hljs-number">100</span>}
  ], {
    duration: <span class="hljs-number">2000</span>,
    fill: <span class="hljs-string">'forwards'</span>,    
  }).finished))

  <span class="hljs-keyword">await</span> s.animate([
    {rotate: <span class="hljs-number">-360</span>, bgcolor: <span class="hljs-string">'red'</span>}
  ], {
    duration: <span class="hljs-number">1000</span>,
    fill: <span class="hljs-string">'forwards'</span>,    
  }).finished

  <span class="hljs-keyword">await</span> s2.animate([
    {rotate: <span class="hljs-number">-360</span>, bgcolor: <span class="hljs-string">'red'</span>}
  ], {
    duration: <span class="hljs-number">1000</span>,
    fill: <span class="hljs-string">'forwards'</span>,    
  }).finished
}())
</code></pre>
<h3>Sprite texture</h3>
<p>我们可以给Sprite元素绑定图片，只需要将图片的URL作为元素的textures属性。</p>
<p></p>
<pre><code class="hljs lang-js"><span class="hljs-keyword">const</span> scene = <span class="hljs-keyword">new</span> spritejs.Scene(<span class="hljs-string">'#container'</span>),
      layer = scene.layer()

<span class="hljs-keyword">const</span> s = <span class="hljs-keyword">new</span> spritejs.Sprite({
  textures: <span class="hljs-string">'https://p0.ssl.qhimg.com/t01a72262146b87165f.png'</span>,
  anchor: <span class="hljs-number">0.5</span>,
  pos: [<span class="hljs-number">300</span>, <span class="hljs-number">300</span>],
  scale: <span class="hljs-number">0.5</span>,
})

layer.append(s)
</code></pre>
<p>注意这里使用<code>textures</code>而不是<code>texture</code>作为属性名，因为sprite对象允许我们传多张图片进去，绘制的时候会将这些图片依次叠加。</p>
<p>我们还可以给多张图片指定rect和srcRect：</p>
<p></p>
<pre><code class="hljs lang-js"><span class="hljs-keyword">const</span> scene = <span class="hljs-keyword">new</span> spritejs.Scene(<span class="hljs-string">'#container'</span>),
      layer = scene.layer()

<span class="hljs-keyword">const</span> texture = <span class="hljs-string">'https://p5.ssl.qhimg.com/t01a2bd87890397464a.png'</span>

<span class="hljs-keyword">const</span> s = <span class="hljs-keyword">new</span> spritejs.Sprite()
s.attr({
  anchor: <span class="hljs-number">0.5</span>,
  textures: [
    {src: texture, rect: [<span class="hljs-number">0</span>, <span class="hljs-number">0</span>, <span class="hljs-number">190</span>, <span class="hljs-number">268</span>], srcRect: [<span class="hljs-number">0</span>, <span class="hljs-number">0</span>, <span class="hljs-number">190</span>, <span class="hljs-number">268</span>]},
    {src: texture, rect: [<span class="hljs-number">200</span>, <span class="hljs-number">278</span>, <span class="hljs-number">190</span>, <span class="hljs-number">268</span>], srcRect: [<span class="hljs-number">191</span>, <span class="hljs-number">269</span>, <span class="hljs-number">190</span>, <span class="hljs-number">268</span>]},
    {src: texture, rect: [<span class="hljs-number">0</span>, <span class="hljs-number">278</span>, <span class="hljs-number">190</span>, <span class="hljs-number">268</span>], srcRect: [<span class="hljs-number">0</span>, <span class="hljs-number">269</span>, <span class="hljs-number">190</span>, <span class="hljs-number">268</span>]},
    {src: texture, rect: [<span class="hljs-number">200</span>, <span class="hljs-number">0</span>, <span class="hljs-number">190</span>, <span class="hljs-number">268</span>], srcRect: [<span class="hljs-number">191</span>, <span class="hljs-number">0</span>, <span class="hljs-number">190</span>, <span class="hljs-number">268</span>]},
  ],
  border: [<span class="hljs-number">2</span>, <span class="hljs-string">'grey'</span>],
  pos: [<span class="hljs-number">300</span>, <span class="hljs-number">300</span>],
})

layer.append(s)
</code></pre>
<p>使用textures的时候，我们支持资源的预加载和雪碧图，我们可以将资源使用进行打包（可使用TP的免费版，导出配置文件格式为JSON Hash）</p>
<p></p>
<pre><code class="hljs lang-js">(<span class="hljs-keyword">async</span> <span class="hljs-function"><span class="hljs-keyword">function</span> (<span class="hljs-params"></span>) </span>{
  <span class="hljs-keyword">const</span> {Scene, Sprite} = spritejs
  <span class="hljs-keyword">const</span> scene = <span class="hljs-keyword">new</span> Scene(<span class="hljs-string">'#paper'</span>, {viewport: [<span class="hljs-string">'auto'</span>, <span class="hljs-string">'auto'</span>], resolution: [<span class="hljs-number">1200</span>, <span class="hljs-number">1200</span>]})

  <span class="hljs-keyword">await</span> scene.preload([
    <span class="hljs-string">'https://p3.ssl.qhimg.com/t010ded517024020e10.png'</span>,
    <span class="hljs-string">'https://s1.ssl.qhres.com/static/6ead70a354da7aa4.json'</span>,
  ])

  ...

  const layer = scene.layer(<span class="hljs-string">'fglayer'</span>)

  ...

  const head = <span class="hljs-keyword">new</span> Sprite(<span class="hljs-string">'head.png'</span>)
  head.attr({
    pos: [<span class="hljs-number">606</span>, <span class="hljs-number">0</span>],
  })

  <span class="hljs-keyword">const</span> neck = <span class="hljs-keyword">new</span> Sprite(<span class="hljs-string">'neck.png'</span>)
  neck.attr({
    pos: [<span class="hljs-number">626</span>, <span class="hljs-number">68</span>],
    zIndex: <span class="hljs-number">-1</span>,
  })

  <span class="hljs-keyword">const</span> body = <span class="hljs-keyword">new</span> Sprite(<span class="hljs-string">'body.png'</span>)
  body.attr({
    pos: [<span class="hljs-number">606</span>, <span class="hljs-number">73</span>],
  })

  <span class="hljs-keyword">const</span> leftArm = <span class="hljs-keyword">new</span> Sprite(<span class="hljs-string">'arm-1.png'</span>)
  leftArm.attr({
    pos: [<span class="hljs-number">600</span>, <span class="hljs-number">73</span>],
  })

  <span class="hljs-keyword">const</span> rightArm = <span class="hljs-keyword">new</span> Sprite(<span class="hljs-string">'arm-2.png'</span>)
  rightArm.attr({
    pos: [<span class="hljs-number">675</span>, <span class="hljs-number">73</span>],
  })

  ...
}())
</code></pre>
<h3>绘制矢量图</h3>
<p>除了普通的Sprite类型之外，SpriteJS提供绘制矢量图的Path类型</p>
<p></p>
<pre><code class="hljs lang-js"><span class="hljs-keyword">const</span> scene = <span class="hljs-keyword">new</span> Scene(<span class="hljs-string">'#svgpath'</span>, {viewport: [<span class="hljs-string">'auto'</span>, <span class="hljs-string">'auto'</span>], resolution: [<span class="hljs-number">1540</span>, <span class="hljs-number">600</span>]})
<span class="hljs-keyword">const</span> layer = scene.layer(<span class="hljs-string">'fglayer'</span>)

<span class="hljs-keyword">const</span> p1 = <span class="hljs-keyword">new</span> Path()
p1.attr({
  path: {
    d: <span class="hljs-string">'M280,250A200,200,0,1,1,680,250A200,200,0,1,1,280,250Z'</span>,
    transform: {
      scale: <span class="hljs-number">0.5</span>,
    },
    trim: <span class="hljs-literal">true</span>,
  },
  strokeColor: <span class="hljs-string">'#033'</span>,
  fillColor: <span class="hljs-string">'#839'</span>,
  lineWidth: <span class="hljs-number">12</span>,
  pos: [<span class="hljs-number">100</span>, <span class="hljs-number">50</span>],
})

layer.appendChild(p1)

<span class="hljs-keyword">const</span> p2 = <span class="hljs-keyword">new</span> Path()
p2.attr({
  path: {
    d: <span class="hljs-string">'M480,50L423.8,182.6L280,194.8L389.2,289.4L356.4,430L480,355.4L480,355.4L603.6,430L570.8,289.4L680,194.8L536.2,182.6Z'</span>,
    transform: {
      rotate: <span class="hljs-number">45</span>,
    },
    trim: <span class="hljs-literal">true</span>,
  },
  fillColor: <span class="hljs-string">'#ed8'</span>,
  pos: [<span class="hljs-number">450</span>, <span class="hljs-number">100</span>],
})
layer.appendChild(p2)

<span class="hljs-keyword">const</span> p3 = <span class="hljs-keyword">new</span> Path()
p3.attr({
  path: {
    d: <span class="hljs-string">'M480,437l-29-26.4c-103-93.4-171-155-171-230.6c0-61.6,48.4-110,110-110c34.8,0,68.2,16.2,90,41.8C501.8,86.2,535.2,70,570,70c61.6,0,110,48.4,110,110c0,75.6-68,137.2-171,230.8L480,437z'</span>,
    trim: <span class="hljs-literal">true</span>,
  },
  strokeColor: <span class="hljs-string">'#f37'</span>,
  lineWidth: <span class="hljs-number">20</span>,
  lineJoin: <span class="hljs-string">'round'</span>,
  lineCap: <span class="hljs-string">'round'</span>,
  pos: [<span class="hljs-number">1000</span>, <span class="hljs-number">100</span>],
})
layer.appendChild(p3)
</code></pre>
<p>Path能够支持使用来在Canvas上绘制矢量图形：</p>
<p>SVG和Sprite Path：</p>
<pre><code class="hljs lang-html"><span class="hljs-tag">&lt;<span class="hljs-name">svg</span> <span class="hljs-attr">viewBox</span>=<span class="hljs-string">"0 0 100 100"</span> <span class="hljs-attr">xmlns</span>=<span class="hljs-string">"http://www.w3.org/2000/svg"</span>&gt;</span>
  <span class="hljs-tag">&lt;<span class="hljs-name">path</span> <span class="hljs-attr">d</span>=<span class="hljs-string">"M 10,30
           A 20,20 0,0,1 50,30
           A 20,20 0,0,1 90,30
           Q 90,60 50,90
           Q 10,60 10,30 z"</span>/&gt;</span>
<span class="hljs-tag">&lt;/<span class="hljs-name">svg</span>&gt;</span>
</code></pre>
<p></p>
<pre><code class="hljs lang-js"><span class="hljs-keyword">const</span> p = <span class="hljs-keyword">new</span> spritejs.Path(<span class="hljs-string">`M 10,30
           A 20,20 0,0,1 50,30
           A 20,20 0,0,1 90,30
           Q 90,60 50,90
           Q 10,60 10,30 z`</span>)

p.attr({
    fillColor: <span class="hljs-string">'red'</span>,
    pos: [<span class="hljs-number">200</span>, <span class="hljs-number">200</span>],
})

layer.append(p)
</code></pre>
<p>SpriteJS还能够支持Path的transition（或animate）</p>
<p></p>
<pre><code class="hljs lang-js"><span class="hljs-keyword">const</span> scene = <span class="hljs-keyword">new</span> spritejs.Scene(<span class="hljs-string">'#container'</span>),
      layer = scene.layer()

<span class="hljs-keyword">const</span> paths = [
  <span class="hljs-string">"M280,250A200,200,0,1,1,680,250A200,200,0,1,1,280,250Z"</span>,
  <span class="hljs-string">"M480,50L423.8,182.6L280,194.8L389.2,289.4L356.4,430L480,355.4L480,355.4L603.6,430L570.8,289.4L680,194.8L536.2,182.6Z"</span>,
  <span class="hljs-string">"M480,437l-29-26.4c-103-93.4-171-155-171-230.6c0-61.6,48.4-110,110-110c34.8,0,68.2,16.2,90,41.8C501.8,86.2,535.2,70,570,70c61.6,0,110,48.4,110,110c0,75.6-68,137.2-171,230.8L480,437z"</span>,
  <span class="hljs-string">"M595,82.1c1,1-1,2-1,2s-6.9,2-8.9,4.9c-2,2-4.9,8.8-4.9,8.8c3.9-1,8.9-2,13.8-4c1,0,2,1,3,2c1,0-11.8,4.9-14.8,6.9c-2,2-11.8,9.9-14.8,9.9c-2.9,0-9.9,1-9.9,1c1,2,2,3.9,3.9,6.9c0,0-6.9,4-6.9,4.9c-1,1-5.9,6.9-5.9,6.9s17.7,1.9,23.6-7.9c-5.9,9.8-19.7,19.7-48.2,19.7c-29.5,0-53.1-11.8-68.9-17.7c-16.7-6.9-38.4-14.8-56.1-14.8c-16.7,0-36.4,4.9-49.2,16.8c-22.6-8.8-54.1-4-68.9,9.8c-13.8,13.8-27.5,30.5-29.5,42.3c-2.9,12.9-9.8,43.3-19.7,57.2c-13.8,22.5-29.5,28.5-34.5,38.3c-4.9,9.9-4.9,30.5-4,30.5c2,1,8.9,0,12.8-2c7.9-2.9,29.5-25.6,37.4-36.4c7.9-10.9,34.5-58.1,38.4-74.8s7.9-33.5,19.7-42.3c12.8-8.8,28.5-4.9,28.5-3.9c0,0-14.7,11.8-15.7,44.3s18.7,28.6,8.8,49.2c-9.9,17.7-39.3,5.9-49.2,16.7c-7.9,8.9,0,40.3,0,46.2c0,6-3,33.5-4.9,40.4c-1,5.9,0,9.8-1,13.8c-1,3,6,3.9,6,3.9s-6,7.8-8.9,5.9c-2.9-1-4.9-1-6.9,0c-2,0-5.9,1.9-9.9,0L232.9,401c2,1,4.9,1.9,7.9,1c4-1,23.6-9.9,25.6-11.9c2.9-1,19.7-10.8,22.6-16.7c2-5.9,5.9-24.6,5.9-30.5c1-6,2-24.6,2-29.5s-1-13.8,0-17.7c2-2.9,4.9-6.9,8.9-8.9c4.9-1,10.8-1,11.8-1c2,0,18.7,2,21.6,2c3.9,0,19.7-2.9,23.6-5c4.9-0.9,7.8,0,8.9,2c2,1.9-2,4.9-2,5.9c-1,1-8.8,10.8-10.8,14.7c-2,4.9-8.8,13.8-6.9,17.7c2,3.9,2,4.9,7.8,7.9c5.9,1.9,28.5,13.8,41.3,25.6c13.8,12.7,26.6,28.4,28.6,36.4c2.9,8.9,7.8,9.8,10.8,9.8c3,1,8.9,2,8.9,5.9s-1,8.8-1,8.8l36.4,13.8c0,0,0-12.8-1-17.7c-1-5.9-6.9-11.8-11.8-17.7c-4.9-6.9-56-57.1-61-61c-4.9-3-8.9-6.9-9.8-14.7c-1-7.9,8.8-13.8,14.8-20.6c3.9-4.9,14.7-27.6,16.7-30.6c2-2.9,8.9-10.8,12.8-10.8c4.9,0,15.8,6.9,29.5,11.8c5.9,2,48.2,12.8,54.1,14.8c5.9,1,18.6,0,22.6,3.9c3.9,2.9,0,10.9-1,15.8c-1,5.9-11.8,27.5-11.8,27.5s2,7.8,2,13.8c0,6.9-2.9,31.5-5.9,39.3c-2,8.9-15.8,31.6-18.7,35.5c-2,2.9-4.9,4.9-4.9,9.9c0,4.9,8.8,6,11.8,9.8c4,3,1,8.8,0,14.8l39.4,16.7c0-2.9,2-7.9,0-9.9c-1-2.9-5.9-8.8-8.8-12.8c-2-2.9-8.9-13.8-10.8-15.8c-2-2.9-2-8.8,0-13.8c1-4.9,13.8-38.3,14.7-42.3c2-4.9,20.7-44.3,22.6-49.2c2-5.9,17.7-34.4,19.7-39.4c2-5.9,14.8-10.8,18.7-10.8c4.9,0,29.5,8.8,33.4,10.8c2.9,1,25.6,10.9,29.5,12.8c4.9,1.9,2,5.9-1,6.9c-2.9,1.9-39.4,26.5-42.3,27.5c-2.9,1-5.9,3.9-7.9,3.9c-2.9,0-6.9,3.1-6.9,4c0,2-1,5.9-5.9,5.9c-3.9,0-11.8-5.9-16.7-11.8c-6.9,3.9-11.8,6.9-14.8,12.8c-4.9,4.9-6.9,8.9-9.8,15.8c2,2,5.9,2.9,8.8,2.9h31.5c3,0,6.9-0.9,9.9-1.9c2.9-2,80.7-53.1,80.7-53.1s12.8-9.9,12.8-18.7c0-6.9-5.9-8.9-7.9-11.8c-3-1.9-20.7-13.8-23.6-15.7c-4-2.9-17.7-10.9-21.6-12.9c-3-1.9-13.8-5.8-13.8-5.8c3-8.9,5-15.8,5.9-17.7c1-2,1-19.7,2-22.7c0-2.9,5-15.7,6.9-17.7c2-2,6.9-17.7,7.9-20.7c1-1.9,8.8-24.6,12.8-24.6c3.9-1,7.9,2.9,11.8,2.9c4,1,18.7-1,26.6,0c6.9,1,15.8,9.9,17.7,10.8c2.9,1,9.8,3.9,11.8,3.9c1,0,10.8-6.9,10.8-8.8c0-2-6.9-5.9-7.9-5.9c-1-1-7.8-4.9-7.8-4.9c0,1,2.9-1.9,7.8-1.9c3.9,0,7.9,3.9,8.8,4.9c2,1,6.9,3.9,7.9,1.9c1-1,4.9-5.9,4.9-8.9c0-4-3.9-8.8-5.9-10.8s-24.6-23.6-26.6-24.6c-2.9-1-14.7-11.8-14.7-14.7c-1-2-6.9-6.9-7.9-7.9s-30.5-21.6-34.5-24.6c-3.9-2.9-7.9-7.8-7.9-12.7s-2-17.7-2-17.7s-6.9-1-9.8,1.9c-2.9,2-9.8,17.8-13.8,17.8c-10.9-2-24.6,1-24.6,2.9c1,2.9,10.8,1,10.8,1c0,1-3.9,5.9-6.9,5.9c-2,0-7.8,2-8.8,2.9c-2,0-5.9,3.1-5.9,3.1c2.9,0,5.9,0,9.8,0.9c0,0-5.9,4-8.9,4c-2.9,0-12.8,2.9-15.7,3.9c-2,1.9-9.9,7.9-9.9,7.9H589l1,2h4.9L595,82.1L595,82.1z"</span>,
  <span class="hljs-string">"M638.9,259.3v-23.8H380.4c-0.7-103.8-37.3-200.6-37.3-200.6s-8.5,0-22.1,0C369.7,223,341.4,465,341.4,465h22.1c0,0,11.4-89.5,15.8-191h210.2l11.9,191h22.1c0,0-5.3-96.6-0.6-205.7H638.9z"</span>,
  <span class="hljs-string">"M345.47,250L460.94,450L230,450Z M460.94,50L576.41,250L345.47,250Z M576.41,250L691.88,450L460.94,450Z"</span>,
]
<span class="hljs-keyword">const</span> p = <span class="hljs-keyword">new</span> spritejs.Path({d: paths[<span class="hljs-number">0</span>], scale: <span class="hljs-number">0.5</span>})

p.attr({
  fillColor: <span class="hljs-string">'blue'</span>,
  pos: [<span class="hljs-number">0</span>, <span class="hljs-number">0</span>],
})

layer.append(p)

<span class="hljs-keyword">let</span> i = <span class="hljs-number">0</span>

<span class="hljs-function"><span class="hljs-keyword">function</span> <span class="hljs-title">wait</span>(<span class="hljs-params">ms</span>) </span>{
  <span class="hljs-keyword">return</span> <span class="hljs-keyword">new</span> <span class="hljs-built_in">Promise</span>(resolve =&gt; {
    setTimeout(resolve, ms)
  })
}

(<span class="hljs-keyword">async</span> <span class="hljs-function"><span class="hljs-keyword">function</span>(<span class="hljs-params"></span>)</span>{
  <span class="hljs-comment">// noprotected</span>
  <span class="hljs-keyword">for</span>(<span class="hljs-keyword">let</span> i = <span class="hljs-number">0</span>; i &lt; <span class="hljs-number">100</span>; i++) {
    <span class="hljs-keyword">await</span> p.transition(<span class="hljs-number">2.0</span>)
     .attr({d: paths[++i % paths.length]})
    <span class="hljs-keyword">await</span> wait(<span class="hljs-number">1000</span>)
  }  
}())
</code></pre>
<h3>分组</h3>
<p>除了Sprite、Path外，SpriteJS支持Group元素，可以将多个Sprite设置成一组，进行统一的动画。</p>
<p></p>
<pre><code class="hljs lang-js">(<span class="hljs-function"><span class="hljs-keyword">function</span> (<span class="hljs-params"></span>) </span>{
  <span class="hljs-keyword">const</span> {Scene, Path, Group} = spritejs
  <span class="hljs-keyword">const</span> scene = <span class="hljs-keyword">new</span> Scene(<span class="hljs-string">'#paper'</span>, {viewport: [<span class="hljs-string">'auto'</span>, <span class="hljs-string">'auto'</span>], resolution: [<span class="hljs-number">1200</span>, <span class="hljs-number">1200</span>]})

  <span class="hljs-keyword">const</span> layer = scene.layer(<span class="hljs-string">'fglayer'</span>)
  layer.canvas.style.backgroundColor = <span class="hljs-string">'#9cd470'</span>

  <span class="hljs-keyword">const</span> d = <span class="hljs-string">'M235.946483,75.0041277 C229.109329,53.4046689 214.063766,34.845093 195.469876,22.3846101 C175.428247,8.9577702 151.414895,2 127.314132,2 C75.430432,2 31.6212932,32.8626807 18.323944,74.9130141 C8.97646468,77.1439182 2,85.5871171 2,95.7172992 C2,104.709941 7.49867791,112.371771 15.2700334,115.546944 C15.8218133,115.773348 16.6030463,122.336292 16.8270361,123.236385 C22.1235768,144.534892 35.4236577,163.530709 52.5998558,176.952027 C52.6299032,176.976876 52.6626822,177.001726 52.6954612,177.026575 C72.5513428,192.535224 98.5478246,202 127.043705,202 C152.034964,202 176.867791,194.597706 197.428422,180.146527 C215.659011,167.335395 230.201962,148.621202 236.52831,126.969284 C237.566312,123.421373 238.549682,119.685713 239.038636,116.019079 C239.044099,115.983185 239.074146,115.444787 239.082341,115.442025 C246.673412,112.184022 252,104.580173 252,95.7172992 C252,85.6892748 245.15192,77.3371896 235.946483,75.0041277'</span>
  <span class="hljs-keyword">const</span> shadowD = <span class="hljs-string">'M82.1534529,43 C127.525552,43 164.306906,33.6283134 164.306906,21.663753 C164.306906,9.6991926 127.525552,0 82.1534529,0 C36.7813537,0 0,9.6991926 0,21.663753 C0,33.6283134 36.7813537,43 82.1534529,43 Z'</span>
  <span class="hljs-keyword">const</span> shadow = <span class="hljs-keyword">new</span> Path()
  shadow.attr({
    path: shadowD,
    fillColor: <span class="hljs-string">'#000000'</span>,
    opacity: <span class="hljs-number">0.05</span>,
    pos: [<span class="hljs-number">500</span>, <span class="hljs-number">734</span>],
    anchor: <span class="hljs-number">0.5</span>,
    scale: [<span class="hljs-number">1.3</span>, <span class="hljs-number">1.2</span>]
  })
  layer.append(shadow)

  <span class="hljs-keyword">const</span> lemon = <span class="hljs-keyword">new</span> Path()
  lemon.attr({
    path: {d},
    anchor: <span class="hljs-number">0.5</span>,
    pos: [<span class="hljs-number">500</span>, <span class="hljs-number">600</span>],
    fillColor: <span class="hljs-string">'#fed330'</span>,
    scale: <span class="hljs-number">1.4</span>
  })
  layer.append(lemon)

  <span class="hljs-keyword">const</span> lemonGroup = <span class="hljs-keyword">new</span> Group()
  lemonGroup.attr({
    anchor: <span class="hljs-number">0.5</span>,
    pos: [<span class="hljs-number">610</span>, <span class="hljs-number">600</span>],
    size: [<span class="hljs-number">180</span>, <span class="hljs-number">180</span>],
    bgcolor: <span class="hljs-string">'#faee35'</span>,
    border: [<span class="hljs-number">6</span>, <span class="hljs-string">'#fdbd2c'</span>],
    borderRadius: <span class="hljs-number">90</span>,
    scale: <span class="hljs-number">1.5</span>
  })
  layer.append(lemonGroup)

  <span class="hljs-keyword">const</span> d2 = <span class="hljs-string">'M0,0L0,100A15,15,0,0,0,50,86.6z'</span>
  <span class="hljs-keyword">for</span>(<span class="hljs-keyword">let</span> i = <span class="hljs-number">0</span>; i &lt; <span class="hljs-number">12</span>; i++) {
    <span class="hljs-keyword">const</span> t = <span class="hljs-keyword">new</span> Path()
    t.attr({
      path: {d: d2, transform: {scale: <span class="hljs-number">0.65</span>}},
      pos: [<span class="hljs-number">90</span>, <span class="hljs-number">90</span>],
      lineWidth: <span class="hljs-number">2</span>,
      lineCap: <span class="hljs-string">'round'</span>,
      lineJoin: <span class="hljs-string">'round'</span>,
      strokeColor: <span class="hljs-string">'#fff'</span>,
      fillColor: <span class="hljs-string">'#f8c32d'</span>,
      rotate: <span class="hljs-number">30</span> * i,
    })
    lemonGroup.append(t)
  }

  lemonGroup.animate([
    {rotate: <span class="hljs-number">360</span>},
  ], {
    duration: <span class="hljs-number">10000</span>,
    iterations: <span class="hljs-literal">Infinity</span>,
  })

  lemonGroup.on(<span class="hljs-string">'mouseenter'</span>, (evt) =&gt; {
    layer.timeline.playbackRate = <span class="hljs-number">3.0</span>
  })
  lemonGroup.on(<span class="hljs-string">'mouseleave'</span>, (evt) =&gt; {
    layer.timeline.playbackRate = <span class="hljs-number">1.0</span>
  })
}())
</code></pre>
<p>分组可以嵌套，这样我们就可以用分组元素组合成复杂的UI组件。</p>
<h3>响应事件</h3>
<p>SpriteJS不只是能够给精灵元素添加动画，还能像操作DOM元素那样够给精灵元素注册事件。精灵元素支持基本的mouse事件和touch事件，这些事件被SpriteJS的scene代理给对应的精灵：</p>
<p></p>
<pre><code class="hljs lang-js"><span class="hljs-keyword">const</span> scene = <span class="hljs-keyword">new</span> Scene(<span class="hljs-string">'#dom-events'</span>, {viewport: [<span class="hljs-string">'auto'</span>, <span class="hljs-string">'auto'</span>], resolution: [<span class="hljs-number">1540</span>, <span class="hljs-number">600</span>]})
<span class="hljs-keyword">const</span> layer = scene.layer(<span class="hljs-string">'fglayer'</span>)

<span class="hljs-keyword">const</span> s1 = <span class="hljs-keyword">new</span> Sprite()
s1.attr({
  anchor: [<span class="hljs-number">0.5</span>, <span class="hljs-number">0.5</span>],
  pos: [<span class="hljs-number">770</span>, <span class="hljs-number">300</span>],
  size: [<span class="hljs-number">300</span>, <span class="hljs-number">300</span>],
  rotate: <span class="hljs-number">45</span>,
  bgcolor: <span class="hljs-string">'#3c7'</span>,
})

layer.append(s1)

s1.on(<span class="hljs-string">'mouseenter'</span>, (evt) =&gt; {
  s1.attr(<span class="hljs-string">'border'</span>, [<span class="hljs-number">4</span>, <span class="hljs-string">'blue'</span>])
})
s1.on(<span class="hljs-string">'mouseleave'</span>, (evt) =&gt; {
  s1.attr(<span class="hljs-string">'border'</span>, [<span class="hljs-number">0</span>, <span class="hljs-string">''</span>])
})

<span class="hljs-keyword">const</span> anchorCross = <span class="hljs-keyword">new</span> Path(<span class="hljs-string">'M0,10H10,20M10,0V10,20'</span>)
anchorCross.attr({
  anchor: [<span class="hljs-number">0.5</span>, <span class="hljs-number">0.5</span>],
  pos: [<span class="hljs-number">770</span>, <span class="hljs-number">300</span>],
  strokeColor: <span class="hljs-string">'red'</span>,
  rotate: <span class="hljs-number">45</span>,
  lineWidth: <span class="hljs-number">4</span>,
})

layer.append(anchorCross)

<span class="hljs-keyword">const</span> label = <span class="hljs-keyword">new</span> Label(<span class="hljs-string">'鼠标位置：'</span>)

label.attr({
  pos: [<span class="hljs-number">20</span>, <span class="hljs-number">50</span>],
  font: <span class="hljs-string">'32px Arial'</span>,
  lineHeight: <span class="hljs-number">56</span>,
})

layer.append(label)

layer.on(<span class="hljs-string">'mousemove'</span>, (evt) =&gt; {
  <span class="hljs-keyword">const</span> {x, y, targetSprites} = evt

  label.text = <span class="hljs-string">`鼠标位置：\n相对于 layer: <span class="hljs-subst">${Math.round(x)}</span>, <span class="hljs-subst">${Math.round(y)}</span>`</span>

  <span class="hljs-keyword">if</span>(targetSprites.length &amp;&amp; targetSprites.includes(s1)) {
    <span class="hljs-keyword">const</span> [offsetX, offsetY] = s1.pointToOffset(x, y).map(<span class="hljs-built_in">Math</span>.round)
    label.text += <span class="hljs-string">`\n相对于元素：<span class="hljs-subst">${offsetX}</span>, <span class="hljs-subst">${offsetY}</span>`</span>
  }
})
</code></pre>
<p>默认代理的事件：</p>
<ul>
<li>mousedown</li>
<li>mouseup</li>
<li>mousemove</li>
<li>mouseenter</li>
<li>mouseleave</li>
<li>touchstart</li>
<li>touchend</li>
<li>touchmove</li>
</ul>
<p>SpriteJS还可以代理其他事件，比如keyboard事件，我们可以为keyboard事件改写精灵的事件检测函数<code>pointCollision</code>：</p>
<p></p>
<pre><code class="hljs lang-js"><span class="hljs-keyword">const</span> scene = <span class="hljs-keyword">new</span> Scene(<span class="hljs-string">'#event-delegate'</span>, {viewport: [<span class="hljs-string">'auto'</span>, <span class="hljs-string">'auto'</span>], resolution: [<span class="hljs-number">1540</span>, <span class="hljs-number">600</span>]})
<span class="hljs-keyword">const</span> layer = scene.layer()

<span class="hljs-class"><span class="hljs-keyword">class</span> <span class="hljs-title">KeyButton</span> <span class="hljs-keyword">extends</span> <span class="hljs-title">Label</span> </span>{
  pointCollision(evt) {
    <span class="hljs-keyword">return</span> evt.originalEvent.key === <span class="hljs-keyword">this</span>.text
  }
}
KeyButton.defineAttributes({
  init(attr) {
    attr.setDefault({
      font: <span class="hljs-string">'42px Arial'</span>,
      border: {width: <span class="hljs-number">4</span>, color: <span class="hljs-string">'black'</span>, style: <span class="hljs-string">'solid'</span>},
      width: <span class="hljs-number">50</span>,
      height: <span class="hljs-number">50</span>,
      anchor: [<span class="hljs-number">0.5</span>, <span class="hljs-number">0.5</span>],
      textAlign: <span class="hljs-string">'center'</span>,
      lineHeight: <span class="hljs-number">50</span>,
    })
  },
})

<span class="hljs-keyword">const</span> keys = [
  <span class="hljs-string">'qwertyuiop'</span>,
  <span class="hljs-string">'asdfghjkl'</span>,
  <span class="hljs-string">'zxcvbnm'</span>,
]
<span class="hljs-keyword">for</span>(<span class="hljs-keyword">let</span> i = <span class="hljs-number">0</span>; i &lt; <span class="hljs-number">3</span>; i++) {
  <span class="hljs-keyword">const</span> keyButtons = [...keys[i]]
  <span class="hljs-keyword">for</span>(<span class="hljs-keyword">let</span> j = <span class="hljs-number">0</span>; j &lt; keyButtons.length; j++) {
    <span class="hljs-keyword">const</span> key = <span class="hljs-keyword">new</span> KeyButton(keyButtons[j])
    key.attr({
      pos: [<span class="hljs-number">250</span> + j * <span class="hljs-number">80</span>, <span class="hljs-number">200</span> + i * <span class="hljs-number">100</span>],
    })
    key.on(<span class="hljs-string">'keydown'</span>, (evt) =&gt; {
      key.attr({
        bgcolor: <span class="hljs-string">'grey'</span>,
        fillColor: <span class="hljs-string">'white'</span>,
      })
    })
    key.on(<span class="hljs-string">'keyup'</span>, (evt) =&gt; {
      key.attr({
        bgcolor: <span class="hljs-string">'transparent'</span>,
        fillColor: <span class="hljs-string">'black'</span>,
      })
    })
    layer.append(key)
  }
}

<span class="hljs-keyword">const</span> label = <span class="hljs-keyword">new</span> Label(<span class="hljs-string">'轻敲键盘'</span>)
label.attr({
  anchor: [<span class="hljs-number">0.5</span>, <span class="hljs-number">0</span>],
  pos: [<span class="hljs-number">770</span>, <span class="hljs-number">50</span>],
  font: <span class="hljs-string">'42px Arial'</span>,
})
layer.append(label)

scene.delegateEvent(<span class="hljs-string">'keydown'</span>, <span class="hljs-built_in">document</span>)
scene.delegateEvent(<span class="hljs-string">'keyup'</span>, <span class="hljs-built_in">document</span>)
</code></pre>
<p>关于事件处理更多的内容，可以查看</p>
<h3>SpriteJS和D3</h3>
<p>由于SpriteJS的Api和DOM拥有高度一致性，因此它对D3友好，可以方便地使用D3+SpriteJS实现数据可视化展现。</p>
<p></p>
<pre><code class="hljs lang-js">(<span class="hljs-function"><span class="hljs-keyword">function</span> (<span class="hljs-params"></span>) </span>{
  <span class="hljs-keyword">const</span> paper = <span class="hljs-keyword">new</span> spritejs.Scene(<span class="hljs-string">'#paper'</span>, {
    viewport: [<span class="hljs-string">'auto'</span>, <span class="hljs-string">'auto'</span>],
    resolution: [<span class="hljs-number">1600</span>, <span class="hljs-number">1200</span>],
    stickMode: <span class="hljs-string">'width'</span>,
  })

  <span class="hljs-keyword">const</span> dataset = [<span class="hljs-number">125</span>, <span class="hljs-number">121</span>, <span class="hljs-number">127</span>, <span class="hljs-number">193</span>, <span class="hljs-number">309</span>]

  <span class="hljs-keyword">const</span> linear = d3.scaleLinear()
    .domain([<span class="hljs-number">100</span>, d3.max(dataset)])
    .range([<span class="hljs-number">0</span>, <span class="hljs-number">500</span>])

  <span class="hljs-keyword">const</span> colors = [<span class="hljs-string">'#fe645b'</span>, <span class="hljs-string">'#feb050'</span>, <span class="hljs-string">'#c2af87'</span>, <span class="hljs-string">'#81b848'</span>, <span class="hljs-string">'#55abf8'</span>]

  <span class="hljs-keyword">const</span> s = d3.select(paper).append(<span class="hljs-string">'fglayer'</span>)

  <span class="hljs-keyword">const</span> chart = s.selectAll(<span class="hljs-string">'sprite'</span>)
    .data(dataset)
    .enter()
    .append(<span class="hljs-string">'sprite'</span>)
    .attr(<span class="hljs-string">'x'</span>, <span class="hljs-number">450</span>)
    .attr(<span class="hljs-string">'y'</span>, (d, i) =&gt; {
      <span class="hljs-keyword">return</span> <span class="hljs-number">200</span> + i * <span class="hljs-number">95</span>
    })
    .attr(<span class="hljs-string">'width'</span>, <span class="hljs-number">0</span>)
    .attr(<span class="hljs-string">'height'</span>, <span class="hljs-number">80</span>)
    .attr(<span class="hljs-string">'bgcolor'</span>, <span class="hljs-string">'#ccc'</span>)

  chart.transition()
    .duration(<span class="hljs-number">2000</span>)
    .attr(<span class="hljs-string">'width'</span>, (d, i) =&gt; {
      <span class="hljs-keyword">return</span> linear(d)
    })
    .attr(<span class="hljs-string">'bgcolor'</span>, (d, i) =&gt; {
      <span class="hljs-keyword">return</span> colors[i]
    })

  s.append(<span class="hljs-string">'axis'</span>)
    .attr(<span class="hljs-string">'ticks'</span>, [<span class="hljs-number">100</span>, <span class="hljs-number">200</span>, <span class="hljs-number">300</span>, <span class="hljs-number">400</span>])
    .attr(<span class="hljs-string">'axisScales'</span>, [linear])
    .attr(<span class="hljs-string">'direction'</span>, <span class="hljs-string">'bottom'</span>)
    .attr(<span class="hljs-string">'pos'</span>, [<span class="hljs-number">450</span>, <span class="hljs-number">700</span>])
    .attr(<span class="hljs-string">'color'</span>, <span class="hljs-string">'#666'</span>)

  chart.on(<span class="hljs-string">'click'</span>, (data) =&gt; {
    <span class="hljs-comment">/* eslint-disable no-console */</span>
    <span class="hljs-built_in">console</span>.log(data, d3.event)
    <span class="hljs-comment">/* eslint-enable no-console */</span>
  })
}())
</code></pre>
<p>更多的例子见：</p>
<h3>物理引擎</h3>
<p>SpriteJS的</p>
<p></p>
<pre><code class="hljs lang-js"><span class="hljs-comment">// module aliases</span>
<span class="hljs-keyword">const</span> {Engine, World, Composites, Composite, Bodies} = Matter

<span class="hljs-comment">// create an engine</span>
<span class="hljs-keyword">const</span> engine = Engine.create()
<span class="hljs-comment">// engine.world.gravity.scale = 0; //turn off gravity (it's added back in later)</span>

<span class="hljs-keyword">const</span> stackA = Composites.stack(<span class="hljs-number">100</span>, <span class="hljs-number">100</span>, <span class="hljs-number">6</span>, <span class="hljs-number">6</span>, <span class="hljs-number">0</span>, <span class="hljs-number">0</span>, (x, y) =&gt; {
  <span class="hljs-keyword">return</span> Bodies.rectangle(x, y, <span class="hljs-number">15</span>, <span class="hljs-number">15</span>, {
    <span class="hljs-comment">// friction: 0,</span>
    <span class="hljs-comment">// frictionAir: 0,</span>
    <span class="hljs-comment">// frictionStatic: 0,</span>
    <span class="hljs-comment">// restitution: 1</span>
  })
})

<span class="hljs-keyword">const</span> wall = Bodies.rectangle(<span class="hljs-number">400</span>, <span class="hljs-number">300</span>, <span class="hljs-number">500</span>, <span class="hljs-number">20</span>, {
  isStatic: <span class="hljs-literal">true</span>,
})

World.add(engine.world, [stackA, wall])

<span class="hljs-keyword">const</span> offset = <span class="hljs-number">5</span>
World.add(engine.world, [
  Bodies.rectangle(<span class="hljs-number">400</span>, -offset, <span class="hljs-number">800</span> + <span class="hljs-number">2</span> * offset, <span class="hljs-number">50</span>, {
    isStatic: <span class="hljs-literal">true</span>,
  }),
  Bodies.rectangle(<span class="hljs-number">400</span>, <span class="hljs-number">600</span> + offset, <span class="hljs-number">800</span> + <span class="hljs-number">2</span> * offset, <span class="hljs-number">50</span>, {
    isStatic: <span class="hljs-literal">true</span>,
  }),
  Bodies.rectangle(<span class="hljs-number">800</span> + offset, <span class="hljs-number">300</span>, <span class="hljs-number">50</span>, <span class="hljs-number">600</span> + <span class="hljs-number">2</span> * offset, {
    isStatic: <span class="hljs-literal">true</span>,
  }),
  Bodies.rectangle(-offset, <span class="hljs-number">300</span>, <span class="hljs-number">50</span>, <span class="hljs-number">600</span> + <span class="hljs-number">2</span> * offset, {
    isStatic: <span class="hljs-literal">true</span>,
  }),
])

<span class="hljs-keyword">const</span> scene = <span class="hljs-keyword">new</span> Scene(<span class="hljs-string">'#simple-demo'</span>, {viewport: [<span class="hljs-string">'auto'</span>, <span class="hljs-string">'auto'</span>], resolution: [<span class="hljs-number">800</span>, <span class="hljs-number">600</span>]})
<span class="hljs-keyword">const</span> fglayer = scene.layer(<span class="hljs-string">'fglayer'</span>)

<span class="hljs-keyword">const</span> blocks = []

<span class="hljs-function"><span class="hljs-keyword">function</span> <span class="hljs-title">render</span>(<span class="hljs-params"></span>) </span>{
  Engine.update(engine, <span class="hljs-number">16</span>)
  <span class="hljs-keyword">const</span> bodies = Composite.allBodies(engine.world)
  <span class="hljs-comment">// console.log(bodies)</span>
  <span class="hljs-keyword">for</span>(<span class="hljs-keyword">let</span> i = <span class="hljs-number">0</span>; i &lt; bodies.length; i++) {
    <span class="hljs-keyword">const</span> body = bodies[i],
      {position, angle} = body
    <span class="hljs-keyword">const</span> pos = [
        <span class="hljs-built_in">Math</span>.round(position.x * <span class="hljs-number">10</span>) / <span class="hljs-number">10</span>,
        <span class="hljs-built_in">Math</span>.round(position.y * <span class="hljs-number">10</span>) / <span class="hljs-number">10</span>,
      ],
      rotate = <span class="hljs-built_in">Math</span>.round(<span class="hljs-number">180</span> * angle * <span class="hljs-number">10</span> / <span class="hljs-built_in">Math</span>.PI) / <span class="hljs-number">10</span>

    <span class="hljs-keyword">let</span> block = blocks[i]
    <span class="hljs-keyword">if</span>(!block) {
      <span class="hljs-keyword">const</span> {min, max} = body.bounds
      block = <span class="hljs-keyword">new</span> Sprite()
      block.attr({
        anchor: <span class="hljs-number">0.5</span>,
        size: [max.x - min.x, max.y - min.y],
        pos,
        rotate,
        bgcolor: body.render.fillStyle,
      })
      blocks[i] = block
      fglayer.append(block)
    } <span class="hljs-keyword">else</span> {
      block.attr({
        pos,
        rotate,
      })
    }
  }
  <span class="hljs-built_in">window</span>.requestAnimationFrame(render)
}

render()
</code></pre>
<h3>粒子系统</h3>
<p>同样，通过</p>
<p></p>
<pre><code class="hljs lang-js"><span class="hljs-keyword">const</span> {Scene, ProtonRenderer} = spritejs
<span class="hljs-keyword">const</span> scene = <span class="hljs-keyword">new</span> Scene(<span class="hljs-string">'#container'</span>, {
  viewport: [<span class="hljs-number">600</span>, <span class="hljs-number">600</span>],
  resolution: [<span class="hljs-number">600</span>, <span class="hljs-number">600</span>],
})
<span class="hljs-keyword">const</span> layer = scene.layer(<span class="hljs-string">'fglayer'</span>)

<span class="hljs-keyword">const</span> proton = <span class="hljs-keyword">new</span> Proton()
<span class="hljs-keyword">const</span> emitter = <span class="hljs-keyword">new</span> Proton.Emitter()

<span class="hljs-comment">// set Rate</span>
emitter.rate = <span class="hljs-keyword">new</span> Proton.Rate(Proton.getSpan(<span class="hljs-number">10</span>, <span class="hljs-number">20</span>), <span class="hljs-number">0.1</span>)

<span class="hljs-comment">// add Initialize</span>
emitter.addInitialize(<span class="hljs-keyword">new</span> Proton.Radius(<span class="hljs-number">1</span>, <span class="hljs-number">12</span>))
emitter.addInitialize(<span class="hljs-keyword">new</span> Proton.Life(<span class="hljs-number">2</span>, <span class="hljs-number">4</span>))
emitter.addInitialize(<span class="hljs-keyword">new</span> Proton.Velocity(<span class="hljs-number">3</span>, Proton.getSpan(<span class="hljs-number">0</span>, <span class="hljs-number">360</span>), <span class="hljs-string">'polar'</span>))

<span class="hljs-comment">// add Behaviour</span>
emitter.addBehaviour(<span class="hljs-keyword">new</span> Proton.Color(<span class="hljs-string">'#ff0000'</span>, <span class="hljs-string">'random'</span>))
emitter.addBehaviour(<span class="hljs-keyword">new</span> Proton.Alpha(<span class="hljs-number">1</span>, <span class="hljs-number">0</span>))

<span class="hljs-comment">// set emitter position</span>
emitter.p.x = layer.canvas.width / <span class="hljs-number">2</span>
emitter.p.y = layer.canvas.height / <span class="hljs-number">2</span>
emitter.emit(<span class="hljs-number">5</span>)

<span class="hljs-comment">// add emitter to the proton</span>
proton.addEmitter(emitter)

<span class="hljs-comment">// add canvas renderer</span>
<span class="hljs-keyword">const</span> renderer = <span class="hljs-keyword">new</span> ProtonRenderer(layer)
proton.addRenderer(renderer)

<span class="hljs-comment">// use Euler integration calculation is more accurate (default false)</span>
Proton.USE_CLOCK = <span class="hljs-literal">false</span>
<span class="hljs-comment">// proton.update()</span>
<span class="hljs-function"><span class="hljs-keyword">function</span> <span class="hljs-title">tick</span>(<span class="hljs-params"></span>) </span>{
  requestAnimationFrame(tick)
  proton.update()
}
tick()
</code></pre>
<p>更多粒子见</p>
<h3>外部时钟</h3>
<p>SpriteJS支持外部时钟，这使得它可以很容易与其他效果库一起使用，比如下面的例子演示了将SpriteJS与AlloyTeam的一同使用：</p>
<p></p>
<pre><code class="hljs lang-js">;(<span class="hljs-keyword">async</span> <span class="hljs-function"><span class="hljs-keyword">function</span> (<span class="hljs-params"></span>) </span>{
  <span class="hljs-keyword">const</span> birdsJsonUrl = <span class="hljs-string">'https://s5.ssl.qhres.com/static/5f6911b7b91c88da.json'</span>
  <span class="hljs-keyword">const</span> birdsRes = <span class="hljs-string">'https://p.ssl.qhimg.com/d/inn/c886d09f/birds.png'</span>

  <span class="hljs-keyword">const</span> scene = <span class="hljs-keyword">new</span> Scene(<span class="hljs-string">'#curvejs'</span>, {
    resolution: [<span class="hljs-number">1540</span>, <span class="hljs-number">600</span>],
    viewport: <span class="hljs-string">'auto'</span>,
  })
  <span class="hljs-keyword">const</span> layer = scene.layer(<span class="hljs-string">'fglayer'</span>, {
    autoRender: <span class="hljs-literal">false</span>,
  })
  <span class="hljs-keyword">await</span> scene.preload([birdsRes, birdsJsonUrl])
  <span class="hljs-keyword">const</span> s = <span class="hljs-keyword">new</span> Sprite(<span class="hljs-string">'bird1.png'</span>)

  s.attr({
    anchor: [<span class="hljs-number">0.5</span>, <span class="hljs-number">0.5</span>],
    pos: [<span class="hljs-number">300</span>, <span class="hljs-number">100</span>],
    transform: {
      scale: [<span class="hljs-number">0.5</span>, <span class="hljs-number">0.5</span>],
    },
    offsetPath: <span class="hljs-string">'M10,80 q100,120 120,20 q140,-50 160,0'</span>,
    zIndex: <span class="hljs-number">200</span>,
  })
  s.animate([
    {offsetDistance: <span class="hljs-number">0</span>},
    {offsetDistance: <span class="hljs-number">1</span>},
  ], {
    duration: <span class="hljs-number">3000</span>,
    direction: <span class="hljs-string">'alternate'</span>,
    iterations: <span class="hljs-literal">Infinity</span>,
  })

  s.animate([
    {scale: [<span class="hljs-number">0.5</span>, <span class="hljs-number">0.5</span>], offsetRotate: <span class="hljs-string">'auto'</span>},
    {scale: [<span class="hljs-number">0.5</span>, <span class="hljs-number">-0.5</span>], offsetRotate: <span class="hljs-string">'reverse'</span>},
    {scale: [<span class="hljs-number">0.5</span>, <span class="hljs-number">0.5</span>], offsetRotate: <span class="hljs-string">'auto'</span>},
  ], {
    duration: <span class="hljs-number">6000</span>,
    iterations: <span class="hljs-literal">Infinity</span>,
    easing: <span class="hljs-string">'step-end'</span>,
  })
  s.animate([
    {textures: <span class="hljs-string">'bird1.png'</span>},
    {textures: <span class="hljs-string">'bird2.png'</span>},
    {textures: <span class="hljs-string">'bird3.png'</span>},
  ], {
    duration: <span class="hljs-number">300</span>,
    direction: <span class="hljs-string">'alternate'</span>,
    iterations: <span class="hljs-literal">Infinity</span>,
  })
  layer.appendChild(s)

  <span class="hljs-keyword">const</span> util = {
    random(min, max) {
      <span class="hljs-keyword">return</span> min + <span class="hljs-built_in">Math</span>.floor(<span class="hljs-built_in">Math</span>.random() * (max - min + <span class="hljs-number">1</span>))
    },
    randomColor() {
      <span class="hljs-keyword">return</span> [<span class="hljs-string">'#22CAB3'</span>, <span class="hljs-string">'#90CABE'</span>, <span class="hljs-string">'#A6EFE8'</span>, <span class="hljs-string">'#C0E9ED'</span>, <span class="hljs-string">'#C0E9ED'</span>, <span class="hljs-string">'#DBD4B7'</span>, <span class="hljs-string">'#D4B879'</span>, <span class="hljs-string">'#ECCEB2'</span>, <span class="hljs-string">'#F2ADA6'</span>, <span class="hljs-string">'#FF7784'</span>][util.random(<span class="hljs-number">0</span>, <span class="hljs-number">9</span>)]
    },
  }

  <span class="hljs-keyword">const</span> {Stage, Curve, motion} = curvejs

  <span class="hljs-keyword">const</span> randomColor = util.randomColor,
    stage = <span class="hljs-keyword">new</span> Stage(layer.canvas)

  stage.add(<span class="hljs-keyword">new</span> Curve({
    points: [<span class="hljs-number">378</span>, <span class="hljs-number">123</span>, <span class="hljs-number">297</span>, <span class="hljs-number">97</span>, <span class="hljs-number">209</span>, <span class="hljs-number">174</span>, <span class="hljs-number">217</span>, <span class="hljs-number">258</span>],
    color: randomColor(),
    motion: motion.rotate,
    data: <span class="hljs-built_in">Math</span>.PI / <span class="hljs-number">20</span>,
  }))

  stage.add(<span class="hljs-keyword">new</span> Curve({
    points: [<span class="hljs-number">378</span>, <span class="hljs-number">123</span>, <span class="hljs-number">385</span>, <span class="hljs-number">195</span>, <span class="hljs-number">293</span>, <span class="hljs-number">279</span>, <span class="hljs-number">217</span>, <span class="hljs-number">258</span>],
    color: randomColor(),
    motion: motion.rotate,
    data: <span class="hljs-built_in">Math</span>.PI / <span class="hljs-number">20</span>,
  }))

  <span class="hljs-function"><span class="hljs-keyword">function</span> <span class="hljs-title">tick</span>(<span class="hljs-params"></span>) </span>{
    stage.update()
    layer.draw(<span class="hljs-literal">false</span>)
    requestAnimationFrame(tick)
  }

  tick()
}())
</code></pre>
<p>以上是SpriteJS的一些简单介绍。它还有许多神奇的功能，有兴趣的同学可以浏览SpriteJS的官方文档</p>
<p>要深入了解SpriteJS或者希望给SpriteJS贡献代码，可以关注我们的。对SpriteJS有疑问，或者需要了解进一步细节，可以加入SpriteJS官方微信群：</p>
<p><img src="https://p0.ssl.qhimg.com/t01d85724b779ce260f.jpg" alt="官方微信群"></p>
---------------
<h1 id="#title_2" >3、BEM For Beginners: Why You Need BEM</h1>
Inna Belaya
[https://www.smashingmagazine.com/2018/06/bem-for-beginners/](https://www.smashingmagazine.com/2018/06/bem-for-beginners/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/06/bem-for-beginners/" />
              <title>BEM For Beginners: Why You Need BEM</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>BEM For Beginners: Why You Need BEM</h1>
                  
                    
                    <address>Inna Belaya</address>
                  
                  <time datetime="2018-06-18T14:00:51&#43;02:00" class="op-published">2018-06-18T14:00:51+02:00</time>
                  <time datetime="2018-06-18T21:17:37&#43;00:00" class="op-modified">2018-06-18T21:17:37+00:00</time>
                </header>
                

<p>BEM makes your code scalable and reusable, thus increasing productivity and facilitating teamwork. Even if you are the only member of the team, BEM can be useful for you. Nevertheless, many developers believe that such a system approach like BEM puts additional boundaries on their project and makes your project overloaded, cumbersome, and slow.</p>

<p>We’ll be collecting all of the main aspects of BEM in a condensed form. This article helps you understand the basic ideas of BEM in just 20 minutes, and to reject prejudices that the system approach is detrimental to your project.</p>

<p>The Big BEM consists of <strong>Methodology</strong>, <strong>Technologies</strong>, <strong>Libraries</strong>, and <strong>Tools</strong>. In this article, we’ll talk more about the methodology itself because it is the concentrated experience of a huge number of developers and it brings a systematic approach to any project.</p>

<p>In order to show you some practical cases of BEM, we’ll touch on the BEM technologies and completely skip the libraries and tools.</p>

<p>From theory to practice:</p>

<ul>
<li></li>
<li>

<ul>
<li></li>
<li></li>
<li></li>
</ul></li>
<li></li>
<li></li>
<li></li>
</ul>

<p>So, is BEM a hero or a villain? It’s up to you! But first, read the article.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3a93b95e-3e4e-4367-86cb-0606ace15af3/sign-theme-batman.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3a93b95e-3e4e-4367-86cb-0606ace15af3/sign-theme-batman.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3a93b95e-3e4e-4367-86cb-0606ace15af3/sign-theme-batman.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3a93b95e-3e4e-4367-86cb-0606ace15af3/sign-theme-batman.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3a93b95e-3e4e-4367-86cb-0606ace15af3/sign-theme-batman.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3a93b95e-3e4e-4367-86cb-0606ace15af3/sign-theme-batman.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3a93b95e-3e4e-4367-86cb-0606ace15af3/sign-theme-batman.png"
			sizes="100vw"
			alt="BEM as a Batman logo"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			BEMBatman
		</figcaption>
	
</figure>




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




<h3 id="the-main-reasons-why-we-do-not-use-any-selectors-except-classes">The Main Reasons Why We Do Not Use Any Selectors Except Classes</h3>

<p>One of the basic rules of the BEM methodology is to use only class selectors. In this section, we’ll explain why.</p>

<ul>
<li>Why don’t we use IDs?</li>
<li>Why don’t we use tag selectors?</li>
<li>Why don’t we use a universal selector?</li>
<li>Why don’t we use CSS reset?</li>
<li>Why don’t we use nested selectors?</li>
<li>Why don’t we combine a tag and a class in a selector?</li>
<li>Why don’t we use combined selectors-</li>
<li>Why don’t we use attribute selectors?</li>
</ul>

<h4 id="we-don-t-use-ids-id-selectors">We Don’t Use IDs (ID Selectors)</h4>

<p>The ID provides a unique name for an HTML element. If the name is unique, you can’t reuse it in the interface. This prevents you from reusing the code.</p>

<h5 id="common-misconceptions">Common Misconceptions</h5>

<ol>
<li><strong>IDs are required for using JavaScript.</strong><br />
Modern browsers can work with either IDs or classes. Any type of selector is processed at the same rate in the browser.</li>
<li><strong>IDs are used with the  <code>&lt;label&gt;</code> tag.</strong><br />
If you place <code>&lt;label&gt;</code> inside a control, it doesn’t need an ID. Instead of <code>&lt;input id=&quot;ID&quot;&gt;&lt;label for=&quot;ID&quot;&gt;Text&lt;/label&gt;</code>, simply use <code>&lt;label&gt;&lt;input type=&quot;...&quot;&gt;Text&lt;/label&gt;</code>.</li>
</ol>

<h4 id="we-don-t-use-tag-selectors">We Don’t Use Tag Selectors</h4>

<p>HTML page markup is unstable: A new design can change the nesting of the sections, heading levels (for example, from <code>&lt;h1&gt;</code> to <code>&lt;h3&gt;</code>) or turn the <code>&lt;p&gt;</code> paragraph into the <code>&lt;div&gt;</code> tag. Any of these changes will break styles that are written for tags. Even if the design doesn’t change, the set of tags is limited. To use an existing layout in another project, you have to solve conflicts between styles written for the same tags.</p>

<p>An extended set of semantic tags can’t meet all layout needs, either.</p>

<p>An example is when the page header contains a logo. A click on the logo opens the main page of the site (<code>index</code>). You can mark it up with tags by using the <code>&lt;img&gt;</code> tag for the image and the <code>&lt;a&gt;</code> tag for the link.</p>

<pre><code class="language-html">&lt;header&gt;
  &lt;a href="/"&gt;
    &lt;img src="img.logo.png" alt="Logo"&gt;
  &lt;/a&gt;
&lt;/header&gt;
</code></pre>

<p>To distinguish between the logo link and an ordinary link in the text, you need extra styles. Now remove underlining and the blue color from the logo link:</p>

<pre><code class="language-css">header a {
  ...
}
</code></pre>

<p>The logo link doesn’t need to be shown on the main page, so change the index page markup:</p>

<pre><code class="language-html">&lt;header&gt;
  &lt;!-- the &lt;a&gt; tag is replaced with &lt;span&gt; --&gt;
  &lt;span&gt;
    &lt;img src="img.logo.png" alt="Logo"&gt;
  &lt;/span&gt;
&lt;/header&gt;
</code></pre>

<p>You don’t need to remove the underlining and the blue color for the <code>&lt;span&gt;</code> tag. So let’s make general rules for the logo link from different pages:</p>

<pre><code class="language-css">header a,
header span
{
  ...
}
</code></pre>

<p>At first glance, this code seems all right, but imagine if the designer removes the logo from the layout. The selector names don’t help you understand which styles should be removed from the project with the logo. The &ldquo;header a&rdquo; selector doesn’t show the connection between the link and the logo. This selector could belong to the link in the header menu or, for example, to the link to the author’s profile. The &ldquo;header span&rdquo; selector could belong to any part of the header.</p>

<p>To avoid confusion, just use  the <code>logo</code> class selector to write the logo styles:</p>

<pre><code class="language-css">.logo {
  ...
}
</code></pre>

<h4 id="we-don-t-use-css-reset">We Don’t Use CSS Reset</h4>

<p>CSS reset is a set of global CSS rules created for the whole page. These styles affect all layout nodes, violate the independence of components, and make it harder to reuse them.</p>

<p>In BEM, &ldquo;reset&rdquo; and &ldquo;normalize&rdquo; aren’t even used for a single block. Resetting and normalization cancel existing styles and replace them with other styles, which you will have to change and update later in any case. As a result, the developer has to write styles that override the ones that were just reset.</p>

<h4 id="we-don-t-use-the-universal-selector">We Don’t Use The Universal Selector (<code>*</code>)</h4>

<p>The universal selector indicates that the project features a style that affects all nodes in the layout. This limits reuse of the layout in other projects:</p>

<ul>
<li>You have to additionally transfer the styles with an asterisk to the project. But in this case, the universal selector might affect the styles in the new project.</li>
<li>The styles with an asterisk must be added to the layout you are transferring.</li>
</ul>

<p>In addition, a universal selector can make the project code unpredictable. For example, it can affect the styles of the universal library components.</p>

<p>Common styles don’t save you time. Often developers start by resetting all margins for components (<code>* { margin: 0; padding: 0; }</code>), but then they still set them the same as in the layout (for example, <code>margin: 12px; padding: 30px;</code>).</p>

<h4 id="we-don-t-use-nested-selectors">We Don’t Use Nested Selectors</h4>

<p>Nested selectors increase code coupling and make it difficult to reuse the code.</p>

<p>The BEM methodology doesn’t prohibit nested selectors, but it recommends not to use them too much. For example, nesting is appropriate if you need to change styles of the elements depending on the block’s state or its assigned theme.</p>

<pre><code class="language-css">.button_hovered .button__text
{
  text-decoration: underline;
}
.button_theme_islands .button__text
{
  line-height: 1.5;
}
</code></pre>

<h4 id="we-don-t-use-combined-selectors">We Don’t Use Combined Selectors</h4>

<p>Combined selectors are more specific than single selectors, which makes it more difficult to redefine blocks.</p>

<p>Consider the following code:</p>

<pre><code class="language-html">&lt;button class="button button_theme_islands"&gt;...&lt;/button&gt;
</code></pre>

<p>Let’s say you set CSS rules in the <code>.button.button_theme_islands</code> selector to do less writing. Then you add the &ldquo;active&rdquo; modifier to the block:</p>

<pre><code class="language-html">&lt;button class="button button_theme_islands button_active"&gt;...&lt;/button&gt;
</code></pre>

<p>The <code>.button_active</code> selector doesn’t redefine the block properties written as <code>.button.button_theme_islands</code> because  <code>.button.button_theme_islands</code> is more specific than <code>.button_active</code>. To redefine it, combine the block modifier selector with the <code>.button</code> selector and declare it below the <code>.button.button_theme_islands</code> because both selectors are equally specific:</p>

<pre><code class="language-css">.button.button_theme_islands {}
.button.button_active {}
</code></pre>

<p>If you use simple class selectors, you won’t have problems redefining the styles:</p>

<pre><code class="language-css">.button_theme_islands {}
.button_active {}
.button {}
</code></pre>

<h4 id="we-don-t-combine-a-tag-and-a-class-in-a-selector">We Don’t Combine A Tag And A Class In A Selector</h4>

<p>Combining a tag and a class in the same selector (for example, <code>button.button</code>) makes CSS rules more specific, so it is more difficult to redefine them.</p>

<p>Consider the following code:</p>

<pre><code class="language-html">&lt;button class="button"&gt;...&lt;/button&gt;
</code></pre>

<p>Let’s say you set CSS rules in the <code>button.button</code> selector.
Then you add the <code>active</code> modifier to the block:</p>

<pre><code class="language-css">&lt;button class="button button_active"&gt;...&lt;/button&gt;
</code></pre>

<p>The <code>.button_active</code> selector doesn’t redefine the block properties written as <code>button.button</code> because  <code>button.button</code> is more specific than <code>.button_active</code>. To make it more specific, you should combine the block modifier selector with the <code>button.button_active</code> tag.</p>

<p>As the project develops, you might end up with blocks with <code>input.button</code>, <code>span.button</code> or <code>a.button</code> selectors. In this case, all modifiers of the <code>button</code> block and all its nested elements will require four different declarations for each instance.</p>

<h5 id="possible-exceptions">Possible Exceptions</h5>

<p>In rare cases, the methodology allows combining tag and class selectors. For example, this can be used for setting the comments style in CMS systems that can’t generate the correct layout.</p>

<p>You can use the comment to write a text, insert images, or add markup. To make them match the site design, the developer can pre-define styles for all tags available to the user and cascade them down to the nested blocks:</p>

<pre><code class="language-html">&lt;div class="content"&gt;
  ... &lt;!-- the user’s text --&gt;
&lt;/div&gt;
CSS rules:
.content a {
  ...
}
.content p {
  font-family: Arial, sans-serif;
  text-align: center;
}
</code></pre>

<h4 id="we-don-t-use-attribute-selectors">We Don’t Use Attribute Selectors</h4>

<p>Attribute selectors are less informative than class selectors. As proof, consider an example with a search form in the header:</p>

<pre><code class="language-html">&lt;header&gt;
  &lt;form action="/"&gt;
    &lt;input name="s"&gt;
    &lt;input type="submit"&gt;
  &lt;/form&gt;
&lt;/header&gt;
</code></pre>

<p>Try using selector attributes to write the form styles:</p>

<pre><code class="language-css">header input[type=submit],
header input[type=checkbox] {
  width: auto;
  margin-right: 20px;
}
header input[type=checkbox] {
  margin: 0;
}
</code></pre>

<p>In this example, you can’t tell for sure from the selector name that the styles belong to the search form. Using classes makes it clearer. Classes don’t have restrictions that prevent you from writing clearly. For example, you can write it like this:</p>

<pre><code class="language-css">.form .search {
  ...
}
</code></pre>

<p>Now the code is less ambiguous, and it’s clear that the styles belong to the search form.</p>

<p>But the nested selectors still make the CSS rules more specific and prevent you from transferring the layout between projects. To get rid of nesting, use BEM principles.</p>

<p><strong>Summary</strong>: <em><code>class</code> is the only selector that allows you to isolate the styles of each component in the project; increase the readability of the code and do not limit the re-use of the layout.</em></p>

<p>CSS styles isolation is the most frequent start point of the BEM journey. But this is the least that BEM can give you. To understand how isolated independent components are arranged in BEM, you need to learn the basic concepts, i.e. Block, Element, Modifier, and Mix. Let’s do this in the next section.</p>

<h3 id="the-basics-of-bem">The Basics Of BEM</h3>

<ul>
<li></li>
<li></li>
<li></li>
</ul>

<h4 id="block-and-elements">Block And Elements</h4>

<p>The BEM methodology is a set of universal rules that can be applied regardless of the technologies used, such as CSS, Sass, HTML, JavaScript or React.</p>

<p>BEM helps to solve the following tasks:</p>

<ul>
<li>Reuse the layout;</li>
<li>Move layout fragments around within a project safely;</li>
<li>Move the finished layout between projects;</li>
<li>Create stable, predictable and clear code;</li>
<li>Reduce the project debugging time.</li>
</ul>

<p>In a BEM project, the interface consists of . Blocks are independent components of the page. An element can’t exist outside the block, so keep in mind that each element can belong to one block only.</p>


  <div id="sponsors-article" data-impression="true" class="c-promo-box c-promo-box--ad sponsors hidden" data-audience="non-subscriber" data-remove="true"></div>



<p>The first two letters in BEM stand for <strong>B</strong>locks and <strong>E</strong>lements. The block name is always unique. It sets the namespace for elements and provides a visible connection between the block parts. Block names are long but clear in order to show the connection between components and to avoid losing any parts of these components when transferring the layout.</p>

<p>To see the full power of BEM naming, consider this example with a form. According to the BEM methodology, the form is implemented using the <code>form</code> block. In HTML, the block name is included in the <code>class</code> attribute:</p>

<pre><code class="language-html">&lt;form class="form" action="/"&gt;
</code></pre>

<p>All parts of the form (the <code>form</code> block) that don’t make sense on their own are considered its elements. So the search box (<code>search</code>) and the button (<code>submit</code>) are elements of the <code>form</code> block. Classes also indicate that an element belongs to the block:</p>

<pre><code class="language-html">&lt;form class="form" action="/"&gt;
  &lt;input class="form__search" name="s"&gt;
  &lt;input class="form__submit" type="submit"&gt;
&lt;/form&gt;
</code></pre>

<p>Note that the block’s name is separated from the element’s name with a special separator. In the BEM , and each developer chooses the one that suits them. The important thing is that separators allow you to distinguish blocks from elements and modifiers programmatically.</p>

<p>Selector names make it clear that in order to move the form to another project, you need to copy all of its components:</p>

<pre><code class="language-css">.form__search {}
.form__submit {}
</code></pre>

<p>Using blocks and elements for class names solves an important problem: It helps us get rid of nested selectors. All selectors in a BEM project have the same weight. That means it is much easier to redefine styles written according to BEM. Now, to use the same form in another project, you can just copy its layout and styles.</p>

<p>The idea of the   of BEM components is that you can explicitly define the connection between the block and its elements.</p>

<h4 id="modifiers-and-mixes">Modifiers And Mixes</h4>

<p>Officially, &ldquo;M&rdquo; stands for <strong>M</strong>odifier, but it also implies one more important notion in BEM: &ldquo;mix&rdquo;. Both modifiers and mixes make changes to a block and its elements. Let’s take a closer look at this.</p>

<h5 id="modifiers">Modifiers</h5>

<p>A  defines the look, state and behavior of a block or an element. Adding modifiers is optional. Modifiers let you combine different block features, as you can use any number of modifiers. But a block or an element can’t be assigned different values of the same modifier.</p>

<p>Let’s explore how modifiers work.</p>

<p>Imagine the project needs the same search form as in the example above. It should have the same functions but look different (for example, the search forms in the header and in the footer of the page should differ). The first thing you can do to change the appearance of the form is to write additional styles:</p>

<pre><code class="language-css">header .form {}
footer .form {}
</code></pre>

<p>The <code>header .form</code> selector has more weight than the <code>form</code> selector, which means that one rule will override the other one. But as we have discussed, nested selectors increase code coupling and make reuse difficult, so this approach doesn’t work for us.</p>

<p>In BEM, you can use a modifier to add new styles to the block:</p>

<pre><code class="language-css">&lt;!-- Added the form_type_original modifier--&gt;
&lt;form class="form form_type_original" action="/"&gt;
  &lt;input class="form__search" name="s"&gt;
  &lt;input class="form__submit" type="submit"&gt;
&lt;/form&gt;
</code></pre>

<p>The line <code>&lt;form class=&quot;form form_type_original&quot;&gt;&lt;/form&gt;</code> indicates that the block was assigned a <code>type</code> modifier with the <code>original</code> value. In a classic scheme, the modifier name is separated from the block or element name with an underscore.</p>

<p>The form can have a unique color, size, type, or design theme. All these parameters can be set with a modifier:</p>

<pre><code class="language-html">&lt;form class="form form_type_original form_size_m form_theme_forest"&gt;</form>
</code></pre>

<p>The same form can look different but stay the same size:</p>

<pre><code class="language-html">&lt;form class="form form_type_original form_size_m form_theme_forest"&gt;&lt;/form&gt;
&lt;form class="form form_type_original form_size_m form_theme_sun"&gt;&lt;/form&gt;
</code></pre>

<p>But the selectors for each modifier will still have the same weight:</p>

<pre><code class="language-css">.form_type_original {}
.form_size_m {}
.form_theme_forest {}
</code></pre>

<p><strong>Important</strong>: <em>A modifier contains only additional styles that change the original block implementation in some way. This allows you to set the appearance of a universal block only once, and add only those features that differ from the original block code into the modifier styles.</em></p>

<pre><code class="language-css">.form {
  /* universal block styles */
}
.form_type_original {
  /* added styles */
}
</code></pre>

<p>This is why a modifier should always be on the same DOM node with the block and the element it is associated with.</p>

<pre><code class="language-css">&lt;form class="form form_type_original"&gt;&lt;/form&gt;
</code></pre>

<p>You can use modifiers to apply universal components in very specific cases. The block and element code doesn’t change. The necessary combination of modifiers is created on the DOM node.</p>

<h5 id="mixes">Mixes</h5>

<p>A  allows you to apply the same formatting to different HTML elements and combine the behavior and styles of several entities while avoiding code duplication. They can replace abstract wrapper blocks.</p>

<p>A mix means that you host several BEM entities (blocks, elements, modifiers) on a single DOM node. Similar to modifiers, mixes are used for changing blocks. Let’s look at some examples of when you should use a mix.</p>

<p>Blocks can differ not only visually but also semantically. For example, a search form, a registration form and a form for ordering cakes are all forms. In the layout, they are implemented with the &ldquo;form&rdquo; block but they don’t have any styles in common. It is impossible to handle such differences with a modifier.
You can define common styles for such blocks but you won’t be able to reuse the code.</p>

<pre><code class="language-css">.form,
.search,
.register {
  ...
}
</code></pre>

<p>You can use a mix to create semantically different blocks for the same form:</p>

<pre><code class="language-html">&lt;form class="form" action="/"&gt;
  &lt;input class="form__search" name="s"&gt;
  &lt;input class="form__submit" type="submit"&gt;
&lt;/form&gt;
</code></pre>

<p>The <code>.form</code> class selector describes all styles that can be applied to any form (order, search or registration):</p>

<pre><code class="language-css">.form {}
</code></pre>

<p>Now you can make a search form from the universal form. To do this, create an additional <code>search</code> class in the project. This class will be responsible only for the search. To combine the styles and behavior of the<code>.form</code>and<code>.search</code> classes, place these classes on a single DOM node:</p>

<pre><code class="language-html"><!-- A mix of "form" and "search" blocks -->
&lt;form class="form search" action="/"&gt;
  &lt;input class="form__search" name="s"&gt;
  &lt;input class="form__submit" type="submit"&gt;
&lt;/form&gt;
</code></pre>

<p>In this case, the <code>.search</code> class is a separate block that defines behavior. This block can’t have modifiers responsible for the form, themes, and sizes. These modifiers already belong to the universal form. A mix helps to combine the styles and behavior of these blocks.</p>

<p>Let’s take one more example where the component’s semantics is changed. Here is a navigation menu in the page header in which all entries are links:</p>

<pre><code class="language-html">&lt;nav class="menu"&gt;
  &lt;a class="link" href=""&gt;&lt;/a&gt;
  &lt;a class="link" href=""&gt;&lt;/a&gt;
  &lt;a class="link" href=""&gt;&lt;/a&gt;
&lt;/nav&gt;
</code></pre>

<p>The link functionality is already implemented in the <code>link</code> block, but the menu links have to differ visually from the links in the text. There are several ways to change the menu links:</p>

<ol>
<li>Create a menu entry modifier that turns the entry into a link:<br />

<pre><code class="language-html">&lt;nav class="menu"&gt;
  &lt;a class="menu__item menu__item_link" href=""&gt;&lt;/a&gt;
  &lt;a class="menu__item menu__item_link" href=""&gt;&lt;/a&gt;
  &lt;a class="menu__item menu__item_link" href=""&gt;&lt;/a&gt;
&lt;/nav&gt;
</code></pre>
<br />In this case, to implement the modifier, you should copy the `link` block behavior and styles. This will lead to code duplication.</li>
<li>Use a mix of the `link` universal block and the `item` element of the `menu` block:<br />

<pre><code class="language-html">&lt;nav class="menu"&gt;
  &lt;a class="link menu__item" href=""&gt;&lt;/a&gt;
  &lt;a class="link menu__item" href=""&gt;&lt;/a&gt;
  &lt;a class="link menu__item" href=""&gt;&lt;/a&gt;
&lt;/nav&gt;
</code></pre>
<br />With the mix of the two BEM entities, you can now implement the basic link functionality from the `link` block and additional CSS rules from the `menu` block, and avoid code duplication.</li>
</ol>

<h5 id="external-geometry-and-positioning-giving-up-abstract-html-wrappers">External Geometry And Positioning: Giving Up Abstract HTML Wrappers</h5>

<p>Mixes are used to position a block relative to other blocks or to position elements inside a block. In BEM, styles responsible for geometry and positioning are set in the parent block. Let’s take a universal menu block that has to be placed in the header. In the layout, the block has to have a 20px indent from the parent block.</p>

<p>This task has several solutions:</p>

<ol>
<li>Write styles with indents for the menu block:<br />

<pre><code class="language-css">.menu {
  margin-left: 20px;
}
</code></pre>
<br />In this case, the "menu" block isn’t universal anymore. If you have to place the menu in the page footer, you will have to edit styles because the indents will probably be different.</li>
<li>Create the menu block modifier:<br />

<pre><code class="language-html">&lt;div&gt;
  &lt;ul class="menu menu_type_header"&gt;
    &lt;li class="menu__item"&gt;&lt;a href=""&gt;&lt;/a&gt;&lt;/li&gt;
    &lt;li class="menu__item"&gt;&lt;a href=""&gt;&lt;/a&gt;&lt;/li&gt;
    &lt;li class="menu__item"&gt;&lt;a href=""&gt;&lt;/a&gt;&lt;/li&gt;
  &lt;/ul&gt;
&lt;/div&gt;
</code></pre>

<pre><code class="language-css">.menu_type_header {
  margin-left: 20px;
}
.menu_type_footer {
  margin-left: 30px;
}
</code></pre>
<br />In this case, the project will include two kinds of menus, although this is not the case. The menu stays the same.</li>
<li>Define the external positioning of the block:  nest the `menu` block in the abstract wrapper (for example, the `wrap` block) setting all indents:<br />

<pre><code class="language-html">&lt;div class="wrap"&gt;
  &lt;ul class="menu"&gt;
    &lt;li class="menu__item"&gt;&lt;a href=""&gt;&lt;/a&gt;&lt;/li&gt;
    &lt;li class="menu__item"&gt;&lt;a href=""&gt;&lt;/a&gt;&lt;/li&gt;
    &lt;li class="menu__item"&gt;&lt;a href=""&gt;&lt;/a&gt;&lt;/li&gt;
  &lt;/ul&gt;
&lt;/div&gt;
</code></pre>
<br />To avoid the temptation to create modifiers and change the block styles to position the block on the page, you need to understand one thing:<br /><br />
<blockquote>The indent from a parent block isn’t a feature of the nested block. It is a feature of the parent block. It has to know that the nested block has to be indented from the border by a certain number of pixels.</blockquote></li>
<li>Use a mix. The information about nested block positioning is included in the parent block elements. Then the parent block element is mixed into the nested block. In this case, the nested block doesn’t specify any indents and can be easily reused in any place.</li>
</ol>

<p>Let’s go on with our example:</p>

<pre><code class="language-html">&lt;div&gt;
  &lt;ul class="menu header__menu"&gt;
    &lt;li class="menu__item"&gt;&lt;a href=""&gt;&lt;/a&gt;&lt;/li&gt;
    &lt;li class="menu__item"&gt;&lt;a href=""&gt;&lt;/a&gt;&lt;/li&gt;
    &lt;li class="menu__item"&gt;&lt;a href=""&gt;&lt;/a&gt;&lt;/li&gt;
  &lt;/ul&gt;
&lt;/div&gt;
</code></pre>

<p>In this case, external geometry and positioning of the <code>menu</code> block are set through the <code>header__menu</code> element. The <code>menu</code> block doesn’t specify any indents and can be easily reused.</p>

<p>The parent block element (in our case it is <code>header__menu</code>) performs the task of the wrapper blocks responsible for external positioning of the block.</p>

<h4 id="blocks-in-the-file-structure">Blocks In The File Structure</h4>

<p>All BEM projects have a similar . The familiar file structure makes it easier for developers to navigate the project, switch between projects, and move blocks from one project to another.</p>

<p>The implementation of each block is stored in a separate project folder. Each technology (CSS, JavaScript, tests, templates, documentation, images) is in a separate file.</p>

<p>For example, if the <code>input</code> block appearance is set with CSS, the code is saved in the <code>input.css</code> file.</p>

<pre><code class="language-css">project
  common.blocks/
    input/
      input.css # The "input" block implementation with CSS
      input.js  # The "input" block implementation with JavaScript
</code></pre>

<p>The code for modifiers and elements is also stored in separate files of the block. This approach allows you to include in the build only those modifiers and elements that are necessary for the implementation of the block.</p>

<pre><code class="language-css">project
  common.blocks/
    input/
      input.css           # The "input" block implementation with CSS
      input.js            # The "input" block implementation with JavaScript
      input_theme_sun.css # The "input_theme_sun" modifier implementation
      input__clear.css    # The "input__clear" element implementation with CSS
      input__clear.js     # The "input__clear" element implementation with JavaScript
</code></pre>

<p>To improve the project navigation, combine block modifiers with multiple values in directories.</p>

<p>The file structure of any BEM project consists of ). Redefinition levels allow you to:</p>

<ul>
<li>Divide the project into platforms;</li>
<li>Easily update the block libraries included in the project;</li>
<li>Use common blocks to develop multiple projects;</li>
<li>Change the design themes without affecting the project logic;</li>
<li>Conduct experiments in a live project.</li>
</ul>

<p>Using blocks and storing all block technologies in the same folder makes it easy to move blocks between projects. To move all styles and behavior of the block together with the layout, just copy the block folder to the new project.</p>

<h3 id="non-evident-advantages-of-the-methodology">Non-Evident Advantages Of The Methodology</h3>

<h4 id="the-convenience-of-parallel-development">The Convenience Of Parallel Development</h4>

<p>In BEM, any layout is divided into blocks. Because the blocks are independent, they can be developed in parallel by several developers.</p>

<p>A developer creates a block as a universal component that can be reused in any other project.</p>

<p>An example is the .</p>

<p>Using blocks in project layout helps you save the time on integrating code written by several developers, guarantees the uniqueness of component names, and lets you test blocks at the development stage.</p>

<h4 id="testing-the-layout">Testing The Layout</h4>

<p>It is problematic to test the functionality of the whole page, especially in a dynamic project connected to a database.</p>

<p>In BEM, each block is covered by tests. Tests are a block implementation technology, like Javascript or CSS. Blocks are tested at the development stage. It is easier to check the correctness of one block and then assemble the project from tested blocks. After that, all you have to do is to make sure that the block wrapper is working correctly.</p>

<h4 id="customizable-build-of-a-project">Customizable Build Of A Project</h4>

<p>For convenient development, all blocks and technologies in a BEM project are placed in separate folders and files. To combine the source files into a single file (for example, to put all CSS files in <code>project.css</code>, all JS files in <code>project.js</code>, and so on), we use the build process.</p>

<p>The build performs the following tasks:</p>

<ul>
<li>Combines source files that are spread out across the project’s file system;</li>
<li>Includes only necessary blocks, elements, and modifiers (BEM entities) in the project;</li>
<li>Follows the order for including entities;</li>
<li>Processes the source file code during the build (e.g. compiles LESS code to CSS code).</li>
</ul>

<p>To include only the necessary BEM entities in the build, you need to create a list of blocks, elements, and modifiers used on the pages. This list is called a <strong>declaration</strong>.</p>

<p>Since BEM blocks are developed independently and placed in separate files in the file system, they don’t &lsquo;know&rsquo; anything about each other. To build blocks based on other blocks, specify dependencies. There is a BEM technology responsible for this: the <code>deps.js</code> files. Dependency files let the build engine know which additional blocks have to be included in the project.</p>

<h3 id="practical-case-bem-is-not-only-for-css">Practical Case: BEM Is Not Only For CSS</h3>

<p>In the previous sections, all code examples are for CSS. But BEM allows you to modify the behavior of the block and its representation in HTML in the same declarative way like in CSS.</p>

<h4 id="how-to-use-templating-in-bem">How To Use Templating In BEM</h4>

<p>In HTML, the block markup is repeated every time the block appears on the page. If you create the HTML markup manually and then need to fix an error or make changes, you will need to modify the markup for every instance of the block. To generate HTML code and apply fixes automatically, BEM uses templates; blocks are responsible for the way they are presented in HTML.</p>

<p>Templates allow you to:</p>

<ul>
<li>Reduce the time used for project debugging, because the template changes are automatically applied to all project blocks;</li>
<li>Modify the block layout;</li>
<li>Move blocks with the current layout to another project.</li>
</ul>

<p>BEM uses the  template engine which features two engines:</p>

<ul>
<li><strong>BEMHTML</strong><br />
Transforms the  description of the page to HTML. The templates are described in .bemhtml.js files.</li>
<li><strong>BEMTREE</strong><br />
Transforms data to BEMJSON. The templates are described in BEMJSON format in <em>.bemtree.js</em> files.</li>
</ul>

<p>If templates aren’t written for the blocks, the template engine sets the <code>&lt;div&gt;</code> tag for the blocks by default.</p>

<p>Compare the declaration of the blocks and the HTML output:</p>

<p>Declaration:</p>

<pre><code class="language-css">{
  block: 'menu',
  content: [
    {
      elem: 'item',
      content: {
        block: 'link'}
    },
    { 
      elem: 'item',
      elemMods: { current: true }, // Set the modifier for the menu item
      content: {
        block: 'link'
      }
    }
  ]
}
</code></pre>

<p>HTML:</p>

<pre><code class="language-html">&lt;div class="menu"&gt;
  &lt;div class="menu__item"&gt;
    &lt;div class="link"&gt;&lt;/div&gt;
  &lt;/div&gt;
  &lt;div class="menu__item menu__item_current"&gt;
    &lt;div class="link"&gt;&lt;/div&gt;
  &lt;/div&gt;
&lt;/div&gt;
</code></pre>

<p>To modify the <code>menu</code> block layout, you need to write templates for the block:</p>

<ol>
<li>Let’s change the <code>menu</code> block tag:<br />

<pre><code class="language-css">block('menu')(
  tag()('menu') // Set the "menu" tag for the menu block 
)
</code></pre>
<br />Modified HTML:<br />

<pre><code class="language-html">&lt;menu class="menu"&gt; &lt;!-- Replace the "div" tag with the "menu" tag for the "menu" block --&gt;
  &lt;div class="menu__item"&gt;
    &lt;div class="link"&gt;&lt;/div&gt;
  &lt;/div&gt;
  &lt;div class="menu__item menu__item_current"&gt;
    &lt;div class="link"&gt;&lt;/div&gt;
  &lt;/div&gt;
&lt;/menu&gt;
</code></pre>
<br />Similar to CSS, the template is applied to all "menu" blocks on the page.</li>
<li>Add an extra element (<code>menu__inner</code>) that works as an inner wrapper and is responsible for the layout of the elements in the <code>menu</code> block. Originally the <code>menu__inner</code> element wasn’t included in the declaration, so we have to add it when the templates are built.<br /><br />BEM templates are written in JavaScript, so you can also use JavaScript to add a new element to the template:<br />

<pre><code class="language-css">block('menu')(
  tag()('menu'),
  content()(function() {
    return {
      elem: 'inner',
      content: this.ctx.content
    };
  })
)
</code></pre>

<pre><code class="language-html">&lt;menu class="menu"&gt; &lt;!-- Replace the "div" tag with the "menu" tag for the "menu" block --&gt;
  &lt;div class="menu__inner"&gt;
    &lt;div class="menu__item"&gt;
      &lt;div class="link"&gt;&lt;/div&gt;
    &lt;/div&gt;
    &lt;div class="menu__item menu__item_current"&gt;
      &lt;div class="link"&gt;&lt;/div&gt;
    &lt;/div&gt;
  &lt;/div&gt;
&lt;/menu&gt;
</code></pre>
</li>
<li>Replace tags for all <code>inner</code> and <code>item</code> elements:<br />

<pre><code class="language-css">block('menu')(
  tag()('menu'),
  content()(function() {
    return {
      elem: 'inner',
      content: this.ctx.content
    }
  }),
  elem('inner')(
    tag()('ul')
  ),
  elem('item')(
    tag()('li')
  )
)
</code></pre>

<pre><code class="language-html">&lt;menu class="menu"&gt;
  &lt;ul class="menu__inner"&gt;
    &lt;li class="menu__item"&gt;
      &lt;div class="link"&gt;&lt;/div&gt;
    &lt;/li&gt;
    &lt;li class="menu__item menu__item_current"&gt;
      &lt;div class="link"&gt;&lt;/div&gt;
    &lt;/li&gt;
  &lt;/ul&gt;
&lt;/menu&gt;
</code></pre>
</li>
<li>Set the <code>&lt;a&gt;</code> tag for all links on the page:<br />

<pre><code class="language-css">block('menu')(
  tag()('menu'),
  content()(function() {
    return {
      elem: 'inner',
      content: this.ctx.content
    }
  }),
  elem('inner')(
    tag()('ul')
  ),
  elem('item')(
    tag()('li')
  )
);
block('link')(
  tag()('a')
);
</code></pre>

<pre><code class="language-html">&lt;menu class="menu"&gt;
  &lt;ul class="menu__inner"&gt;
    &lt;li class="menu__item"&gt;
      &lt;a class="link"&gt;&lt;/a&gt;
    &lt;/li&gt;
    &lt;li class="menu__item menu__item_current"&gt;
      &lt;a class="link"&gt;&lt;/a&gt;
    &lt;/li&gt;
  &lt;/ul&gt;
&lt;/menu&gt;
</code></pre>
</li>
<li>Modify the existing template. Rules in templates are applied in the same way as in CSS: a lower rule overrides a higher rule. Add new rules to the template, and change the link tag from  <code>&lt;a&gt;</code> to <code>&lt;span&gt;</code>:<br />

<pre><code class="language-css">block('link')(
  tag()('a')
);
block('link')(
  tag()('span')
);
</code></pre>

<pre><code class="language-html">&lt;menu class="menu"&gt;
  &lt;ul class="menu__inner"&gt;
    &lt;li class="menu__item"&gt;
      &lt;span class="link"&gt;&lt;/span&gt;
    &lt;/li&gt;
    &lt;li class="menu__item menu__item_current"&gt;
      &lt;span class="link"&gt;&lt;/span&gt;
    &lt;/li&gt;
  &lt;/ul&gt;
&lt;/menu&gt;
</code></pre>
</li>
</ol>

<h3 id="bem-is-a-customizable-system">BEM Is A Customizable System</h3>

<p>BEM methodology provides you strict rules to create a system in your project. But at the same time, a lot of BEM rules can be customized. BEM methodology allows you to change the naming convention, choose the most convenient file structure or add any technologies you want to the block.</p>

<p>Now you can tune in the system and make your own superhero of BEM!</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b1c6b06e-9ccb-409d-84cb-589e07607e32/sign-theme-captain-america.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b1c6b06e-9ccb-409d-84cb-589e07607e32/sign-theme-captain-america.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b1c6b06e-9ccb-409d-84cb-589e07607e32/sign-theme-captain-america.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b1c6b06e-9ccb-409d-84cb-589e07607e32/sign-theme-captain-america.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b1c6b06e-9ccb-409d-84cb-589e07607e32/sign-theme-captain-america.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b1c6b06e-9ccb-409d-84cb-589e07607e32/sign-theme-captain-america.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b1c6b06e-9ccb-409d-84cb-589e07607e32/sign-theme-captain-america.png"
			sizes="100vw"
			alt="BEM as a Captain America logo"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			BEM Captain America
		</figcaption>
	
</figure>


<h3 id="how-to-get-more-out-of-bem">How To Get More Out Of BEM</h3>

<p>To start learning BEM principles, visit our .</p>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(rb, ra, il)</span>
</div>


              </article>
            </body>
          </html>
---------------
<h1 id="#title_3" >4、文章： 对话Vitalik Buterin</h1>
Hans Ulrich Obrist, Vitalik Buterin
[http://www.infoq.com/cn/articles/vitalik-buterin?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/vitalik-buterin?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/vitalik-buterin/zh/smallimage/logo-ieee-1528995981090.jpg"/><p>经Jehan Chu介绍，由著名艺术策展人Hans Ulrich Obrist对以太坊创始人Vitalik Buterin进行的采访实录。</p> <i>By Hans Ulrich Obrist</i> <i> Translated by 姚佳灵</i>
---------------
<h1 id="#title_4" >5、文章： 阿里提出电商搜索全局排序方法，淘宝无线主搜GMV提升5%</h1>
瑞溪
[http://www.infoq.com/cn/articles/ecommerce-search-ranking?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/ecommerce-search-ranking?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/ecommerce-search-ranking/zh/smallimage/image_fences-1529078977514.jpg"/><p>AI 前线本周带来第 35 篇论文解读，本期要解读的论文来自阿里巴巴，主题是：电商搜索全局排序方法。一个好的排序算法可以为电商带来销量的巨大提升，如果你也是这一领域的开发者，希望阿里巴巴的这篇论文解读对你能有所启发。</p> <i>By 瑞溪</i>
---------------
<h1 id="#title_5" >6、文章： 科技发展是如何通过碎片化来影响未来工作的</h1>
Ben Linders, Kary Bheemaiah
[http://www.infoq.com/cn/articles/tech-fragmentation-future-of-work?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/tech-fragmentation-future-of-work?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/tech-fragmentation-future-of-work/zh/smallimage/logo232-1528992873867.jpeg"/><p>科技让世界变得碎片化。随着科技的发展，市场开始变得碎片化，而在这一过程中，新的市场出现了。关键在于了解环境是如何发生变化的，这样个人和公司就可以适应变化并从中受益。当我们的团队由多元化认知的人组成时，就可以更好地解决复杂问题或做出预测。随着我们越来越碎片化，我们将成为一个以任务为基础的社会，而不是以工作为基础的社会。</p> <i>By Ben Linders</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_6" >7、京东构建了全球最大的Kubernetes集群，没有之一</h1>
鲍永成
[http://www.infoq.com/cn/news/2018/06/jd-biggest-kubernetes-cluster?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/06/jd-biggest-kubernetes-cluster?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>2018 年的 618，鲍永成和他的同事们写下了这篇文章，他们希望能够系统梳理过去几年京东在基础架构方面的点击探索，也希望这系列文章能够帮助到更多的中小公司少走弯路。</p> <i>By 鲍永成</i>
---------------
<h1 id="#title_7" >8、隐私和安全是macOS Mojave和Safari 12的第一要务</h1>
Daniel Bryant
[http://www.infoq.com/cn/news/2018/06/mojave-safari-security-privacy?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/06/mojave-safari-security-privacy?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>在年度开发者大会WWDC上，苹果预览了其桌面操作系统的最新版本macOS Mojave和经过升级的Web浏览器Safari 12。苹果表示，增强隐私和安全是这些版本的第一要务。</p> <i>By Daniel Bryant</i> <i> Translated by 谢丽</i>
---------------