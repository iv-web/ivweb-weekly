## 文章索引
1、 <a href="#1javascript-内存泄漏教程" >JavaScript 内存泄漏教程</a><br/>
2、 <a href="#2fex-技术周刊---2017/04/17" >FEX 技术周刊 - 2017/04/17</a><br/>
3、 <a href="#3ios-开发周报迪拜独特艺术长廊-apple-store-建成使用-visual-studio-code-编写-swift-代码" >iOS 开发周报：迪拜独特艺术长廊 Apple Store 建成、使用 Visual Studio Code 编写 Swift 代码</a><br/>
4、 <a href="#4android开发周报android份额超越windowsapk瘦身探索" >Android开发周报：Android份额超越Windows、Apk瘦身探索</a><br/>
5、 <a href="#5microsoft对azure-functions添加了application-insights的支持" >Microsoft对Azure Functions添加了Application Insights的支持</a><br/>
6、 <a href="#6google发布了cloud-machine-learning-api更新" >Google发布了Cloud Machine Learning API更新</a><br/>
7、 <a href="#7安全失败实验" >安全失败实验</a><br/>
8、 <a href="#8重新定义数据库历史的时刻" >重新定义数据库历史的时刻</a><br/>
9、 <a href="#9视频演讲-架构本质及大型电商微服务实践" >视频演讲： 架构本质及大型电商微服务实践</a><br/>
10、 <a href="#10文章-单体保卫战第一部分" >文章： 单体保卫战（第一部分）</a><br/>
11、 <a href="#11文章-mysql分布式数据库高可用实践架构复制机制多机房" >文章： MySQL分布式数据库高可用实践：架构、复制机制、多机房</a><br/>
12、 <a href="#12文章-机器学习工程师必知的十大算法" >文章： 机器学习工程师必知的十大算法</a><br/>
13、 <a href="#13视频演讲-if-then-no-else:-谈构建技术体系过程中的抉择" >视频演讲： if..., then no else: 谈构建技术体系过程中的抉择</a><br/>
14、 <a href="#14visual-basic-15语言新特性" >Visual Basic 15语言新特性</a><br/><h1 id="#title_0" >1、JavaScript 内存泄漏教程</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2017/04/memory-leak.html](http://www.ruanyifeng.com/blog/2017/04/memory-leak.html)
<h2>一、什么是内存泄漏？</h2>

<p>程序的运行需要内存。只要程序提出要求，操作系统或者运行时（runtime）就必须供给内存。</p>

        <p>对于持续运行的服务进程（daemon），必须及时释放不再用到的内存。否则，内存占用越来越高，轻则影响系统性能，重则导致进程崩溃。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017041701-1.png" alt="" title="" /></p>

<p>不再用到的内存，没有及时释放，就叫做内存泄漏（memory leak）。</p>

<p>有些语言（比如 C 语言）必须手动释放内存，程序员负责内存管理。</p>

<blockquote><pre><code class="language-clang">
char * buffer;
buffer = (char*) malloc(42);

// Do something with buffer

free(buffer);
</code></pre></blockquote>

<p>上面是 C 语言代码，<code>malloc</code>方法用来申请内存，使用完毕之后，必须自己用<code>free</code>方法释放内存。</p>

<p>这很麻烦，所以大多数语言提供自动内存管理，减轻程序员的负担，这被称为"垃圾回收机制"（garbage collector）。</p>

<h2>二、垃圾回收机制</h2>

<p>垃圾回收机制怎么知道，哪些内存不再需要呢？</p>

<p>最常使用的方法叫做（reference counting）：语言引擎有一张"引用表"，保存了内存里面所有的资源（通常是各种值）的引用次数。如果一个值的引用次数是<code>0</code>，就表示这个值不再用到了，因此可以将这块内存释放。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017041703.png" alt="" title="" /></p>

<p>上图中，左下角的两个值，没有任何引用，所以可以释放。</p>

<p>如果一个值不再需要了，引用数却不为<code>0</code>，垃圾回收机制无法释放这块内存，从而导致内存泄漏。</p>

<blockquote><pre><code class="language-javascript">
const arr = [1, 2, 3, 4];
console.log('hello world');
</code></pre></blockquote>

<p>上面代码中，数组<code>[1, 2, 3, 4]</code>是一个值，会占用内存。变量<code>arr</code>是仅有的对这个值的引用，因此引用次数为<code>1</code>。尽管后面的代码没有用到<code>arr</code>，它还是会持续占用内存。</p>

<p>如果增加一行代码，解除<code>arr</code>对<code>[1, 2, 3, 4]</code>引用，这块内存就可以被垃圾回收机制释放了。</p>

<blockquote><pre><code class="language-javascript">
const arr = [1, 2, 3, 4];
console.log('hello world');
arr = null;
</code></pre></blockquote>

<p>上面代码中，<code>arr</code>重置为<code>null</code>，就解除了对<code>[1, 2, 3, 4]</code>的引用，引用次数变成了<code>0</code>，内存就可以释放出来了。</p>

<p>因此，并不是说有了垃圾回收机制，程序员就轻松了。你还是需要关注内存占用：那些很占空间的值，一旦不再用到，你必须检查是否还存在对它们的引用。如果是的话，就必须手动解除引用。</p>

<h2>三、内存泄漏的识别方法</h2>

<p>怎样可以观察到内存泄漏呢？</p>

<p>是，如果连续五次垃圾回收之后，内存占用一次比一次大，就有内存泄漏。这就要求实时查看内存占用。</p>

<h3>3.1 浏览器</h3>

<p>Chrome 浏览器查看内存占用，按照以下步骤操作。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017041704.png" alt="" title="" /></p>

<blockquote>
  <ol start='1'>
<li>打开开发者工具，选择 Timeline 面板</li>
<li>在顶部的<code>Capture</code>字段里面勾选 Memory</li>
<li>点击左上角的录制按钮。</li>
<li>在页面上进行各种操作，模拟用户的使用情况。</li>
<li>一段时间后，点击对话框的 stop 按钮，面板上就会显示这段时间的内存占用情况。</li>
</ol>
</blockquote>

<p>如果内存占用基本平稳，接近水平，就说明不存在内存泄漏。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017041705.png" alt="" title="" /></p>

<p>反之，就是内存泄漏了。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017041706.png" alt="" title="" /></p>

<h3>3.2 命令行</h3>

<p>命令行可以使用 Node 提供的方法。</p>

<blockquote><pre><code class="language-javascript">
console.log(process.memoryUsage());
// { rss: 27709440,
//  heapTotal: 5685248,
//  heapUsed: 3449392,
//  external: 8772 }
</code></pre></blockquote>

<p><code>process.memoryUsage</code>返回一个对象，包含了 Node 进程的内存占用信息。该对象包含四个字段，单位是字节，如下。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017041702-1.png" alt="" title="" /></p>

<blockquote>
  <ul>
<li>rss（resident set size）：所有内存占用，包括指令区和堆栈。</li>
<li>heapTotal："堆"占用的内存，包括用到的和没用到的。</li>
<li>heapUsed：用到的堆的部分。</li>
<li>external： V8 引擎内部的 C++ 对象占用的内存。</li>
</ul>
</blockquote>

<p>判断内存泄漏，以<code>heapUsed</code>字段为准。</p>

<h2>四、WeakMap</h2>

<p>前面说过，及时清除引用非常重要。但是，你不可能记得那么多，有时候一疏忽就忘了，所以才有那么多内存泄漏。</p>

<p>最好能有一种方法，在新建引用的时候就声明，哪些引用必须手动清除，哪些引用可以忽略不计，当其他引用消失以后，垃圾回收机制就可以释放内存。这样就能大大减轻程序员的负担，你只要清除主要引用就可以了。</p>

<p>ES6 考虑到了这一点，推出了两种新的数据结构：。它们对于值的引用都是不计入垃圾回收机制的，所以名字里面才会有一个"Weak"，表示这是弱引用。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017041707.jpg" alt="" title="" /></p>

<p>下面以 WeakMap 为例，看看它是怎么解决内存泄漏的。</p>

<blockquote><pre><code class="language-javascript">
const wm = new WeakMap();

const element = document.getElementById('example');

wm.set(element, 'some information');
wm.get(element) // "some information"
</code></pre></blockquote>

<p>上面代码中，先新建一个 Weakmap 实例。然后，将一个 DOM 节点作为键名存入该实例，并将一些附加信息作为键值，一起存放在 WeakMap 里面。这时，WeakMap 里面对<code>element</code>的引用就是弱引用，不会被计入垃圾回收机制。</p>

<p>也就是说，DOM 节点对象的引用计数是<code>1</code>，而不是<code>2</code>。这时，一旦消除对该节点的引用，它占用的内存就会被垃圾回收机制释放。Weakmap 保存的这个键值对，也会自动消失。</p>

<p>基本上，如果你要往对象上添加数据，又不想干扰垃圾回收机制，就可以使用 WeakMap。</p>

<h2>五、WeakMap 示例</h2>

<p>WeakMap 的例子很难演示，因为无法观察它里面的引用会自动消失。此时，其他引用都解除了，已经没有引用指向 WeakMap 的键名了，导致无法证实那个键名是不是存在。</p>

<p>我一直想不出办法，直到有一天贺师俊老师，如果引用所指向的值占用特别多的内存，就可以通过<code>process.memoryUsage</code>方法看出来。</p>

<p>根据这个思路，网友 vtxf 补充了下面的。</p>

<p>首先，打开 Node 命令行。</p>

<blockquote><pre><code class="language-bash">
$ node --expose-gc
</code></pre></blockquote>

<p>上面代码中，<code>--expose-gc</code>参数表示允许手动执行垃圾回收机制。</p>

<p>然后，执行下面的代码。</p>

<blockquote><pre><code class="language-javascript">
// 手动执行一次垃圾回收，保证获取的内存使用状态准确
> global.gc(); 
undefined

// 查看内存占用的初始状态，heapUsed 为 4M 左右
> process.memoryUsage(); 
{ rss: 21106688,
  heapTotal: 7376896,
  heapUsed: 4153936,
  external: 9059 }

> let wm = new WeakMap();
undefined

> const b = new Object();
undefined

> global.gc();
undefined

// 此时，heapUsed 仍然为 4M 左右
> process.memoryUsage(); 
{ rss: 20537344,
  heapTotal: 9474048,
  heapUsed: 3967272,
  external: 8993 }

// 在 WeakMap 中添加一个键值对，
// 键名为对象 b，键值为一个 5*1024*1024 的数组  
> wm.set(b, new Array(5*1024*1024));
WeakMap {}

// 手动执行一次垃圾回收
> global.gc();
undefined

// 此时，heapUsed 为 45M 左右
> process.memoryUsage(); 
{ rss: 62652416,
  heapTotal: 51437568,
  heapUsed: 45911664,
  external: 8951 }

// 解除对象 b 的引用  
> b = null;
null

// 再次执行垃圾回收
> global.gc();
undefined

// 解除 b 的引用以后，heapUsed 变回 4M 左右
// 说明 WeakMap 中的那个长度为 5*1024*1024 的数组被销毁了
> process.memoryUsage(); 
{ rss: 20639744,
  heapTotal: 8425472,
  heapUsed: 3979792,
  external: 8956 }
</code></pre></blockquote>

<p>上面代码中，只要外部的引用消失，WeakMap 内部的引用，就会自动被垃圾回收清除。由此可见，有了它的帮助，解决内存泄漏就会简单很多。</p>

<h2>六、参考链接</h2>

<ul>
<li></li>
<li></li>
<li></li>
</ul>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2017-04-16T20:35:49+08:00">2017年4月16日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>博客文集：</li>
<li>社交媒体：</li>
<li>Feed订阅： </li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------
<h1 id="#title_1" >2、FEX 技术周刊 - 2017/04/17</h1>

[http://fex.baidu.com/blog/2017/04/fex-weekly-17//](http://fex.baidu.com/blog/2017/04/fex-weekly-17//)
作者：2betop <br> <p>微信搜索『FEX』关注我们的公众号，及时获得最新资讯。</p>

<h2 id="section">业界会议</h2>

<p><strong>QCon 北京 2017</strong><br />
http://2017.qconbeijing.com/schedule<br />
业界盛会，可找感兴趣的去看。附 </p>

<p><strong>报名 - 百度技术沙龙：Web生态技术 - 4.22</strong><br />
http://mp.weixin.qq.com/s?__biz=MjM5MDE0Mjc4MA==&amp;mid=2650995797&amp;idx=2&amp;sn=13b671e0c5a144a26c9a16d9ad8b0904<br />
4月22日，我们邀请了数位百度资深研发工程师，从Web生态角度出发，通过四个主题，分享百度在Web速度优化、Web体验增强、Web数据可视化、Web安全方面的技术沉淀和积累。同时，我们邀请了W3C的标准技术专家为大家分享W3C关于Web性能标准规范的工作进展和考虑。</p>

<h2 id="section-1">深阅读</h2>

<p><strong>Real-world JavaScript performance</strong><br />
https://blog.chromium.org/2017/04/real-world-javascript-performance.html<br />
Over the course of the past year, the V8 team has developed a new method for measuring performance against snapshots of real web pages. Using insights from real-world measurements, the V8 team improved the speed of the average page load in Chrome by 10-20% over the course of the past year. 另附：.</p>

<p><strong>PhantomJS - Stepping down as maintainer</strong><br />
https://groups.google.com/forum/#!topic/phantomjs/9aI5d-LDuNE<br />
. I think people will switch to it, eventually. Chrome is faster and more stable than PhantomJS. And it doesn’t eat memory like crazy. I don’t see any future in developing PhantomJS. Developing PhantomJS 2 and 2.5 as a single developer is a bloody hell.</p>

<p><strong>TypeScript at Slack</strong><br />
https://slack.engineering/typescript-at-slack-a81307fa288d#1<br />
At Slack, we strive to be good open-source citizens. To that end, we strive to make the move to TypeScript easier for other developers: Whenever we find gaps, we try to close them. 另：.</p>

<p><strong>How we built Twitter Lite</strong><br />
https://blog.twitter.com/2017/how-we-built-twitter-lite<br />
Twitter web 版本技术栈的介绍，主要使用 node+react+redux. 另附：[Twitter Lite and High Performance React Progressive Web Apps at Scale])(https://medium.com/@paularmstrong/twitter-lite-and-high-performance-react-progressive-web-apps-at-scale-d28a00e780a3)</p>

<p><strong>Creating a Modern OCR Pipeline Using Computer Vision and Deep Learning</strong><br />
https://blogs.dropbox.com/tech/2017/04/creating-a-modern-ocr-pipeline-using-computer-vision-and-deep-learning/<br />
In this post we will take you behind the scenes on how we built a state-of-the-art Optical Character Recognition (OCR) pipeline for our mobile document scanner. We used computer vision and deep learning advances such as bi-directional Long Short Term Memory (LSTMs), Connectionist Temporal Classification (CTC), convolutional neural nets (CNNs), and more. In addition, we will also dive deep into what it took to actually make our OCR pipeline production-ready at Dropbox scale.</p>

<p><strong>The Ultimate Guide to Becoming a CTO</strong><br />
https://brainhub.eu/guide-to-becoming-a-cto<br />
Becoming a CTO is really hard. There is nothing more valuable than a real experience, but in addition to the experience, you can find a ton of useful resources over the internet to help you get started. Therefore we’ve put together an amazing list of (recommended by other CTOs) resources (blog posts, books, presentations, videos etc.). The reason why we’re doing this is to help you to become a better CTO/Technical Leader in your startup or company.</p>

<p><strong>The Post JavaScript Apocalypse - Douglas Crockford</strong><br />
https://www.youtube.com/watch?v=NPB34lDZj3E<br />
This is about JavaScript, clutter, purity, and thoughts on what should be in the language that comes after, assuming that we all live that long.</p>

<p><strong>So what’s this GraphQL thing I keep hearing about?</strong><br />
https://medium.freecodecamp.com/so-whats-this-graphql-thing-i-keep-hearing-about-baf4d36c20cf<br />
GraphQL is a syntax that describes how to ask for data, and is generally used to load data from a server to a client. GraphQL has three main characteristics: It lets the client specify exactly what data it needs; It makes it easier to aggregate data from multiple sources; It uses a type system to describe data. So how did GraphQL get started? What does it look like in practice? And how do you start using it? Read on to find out!</p>

<p><strong>ECharts GL 1.0 alpha 发布</strong><br />
http://echarts.baidu.com/blog/2017/04/12/echarts-gl-alpha.html<br />
距离 ECharts-X 最近一个版本已经过去了两年多时间，期间我们不断被开发者在各种渠道询问 ECharts-X 为什么还不升级新版本，是不是不再维护了等等，对于这些问题我们只能回答我们还没准备好。尽管这两年时间 ECharts X 没什么动静，但是其它的工作，像 ECharts 3 的架构大改动和后续版本的迭代升级，以及其它 WebGL 产品的开发，都是对新版本架构和技术上的积累。现在我们终于可以说我们准备得差不多了，ECharts-X 的下一代，ECharts-GL 发布 1.0 alpha。</p>

<p><strong>使用 FIS3 构建 Vue 前端工程. webpack 用户也请看过来</strong><br />
http://isay.me/2017/04/vue-projects-development-with-fis3.html<br />
使用 FIS 进行更细致的打包，不过其实 FIS 支持自动分析依赖的</p>

<p><strong>上帝说：要有一门面向未来的语言，于是有了 erlang</strong><br />
http://mp.weixin.qq.com/s?__biz=MzA3NDM0ODQwMw==&amp;mid=2649827691&amp;idx=1&amp;sn=8d6854f91bb9d16470ef6eed9d3ad8ec<br />
这篇文章对 erlang 的介绍挺有意思的，尤其是 erlang 的设计哲学，很多都可以当做系统设计原则来用。</p>

<p><strong>如何处理好前后端分离的 API 问题</strong><br />
http://mp.weixin.qq.com/s?__biz=MjM5Mjg4NDMwMA==&amp;mid=2652974908&amp;idx=1&amp;sn=cc0fd32fba8602c6cf26d42e0ee3ff3f<br />
API 的维护是一件烦人的事，所以最好能一次设计好 API。可是这是不可能的，API 在其的生命周期里，应该是要不断地演进的。它与精益创业的思想是相似的，当一个 API 不合适现有场景时，应该对这个 API 进行更新，以满足需求。也因此，API 本身是面向变化的，问题是这种变化是双向的、单向的、联动的？还是静默的？API 设计是一个非常大的话题，这里我们只讨论：演进、设计及维护</p>

<p><strong>文本数据可视化 - 从 Wordle 谈起</strong><br />
http://geekplux.com/2017/04/12/text-data-visualization-wordle.html<br />
大到宣传海报，小到个人名片，Wordle 如今随处可见。它可以轻松的展示出一段文字的关键词，让我们对这段话的内容一目了然。\本文就从最简单的 Wordle 说起，说说文本内容可视化，以窥数据可视化一隅。</p>

<p><strong>浏览器缓存机制剖析</strong><br />
http://louiszhai.github.io/2017/04/07/http-cache/<br />
缓存一直是前端优化的主战场, 利用好缓存就成功了一半. 本篇从http请求和响应的头域入手, 让你对浏览器缓存有个整体的概念. 最终你会发现强缓存, 协商缓存 和 启发式缓存是如此的简单</p>

<p><strong>The Psychology of Speed</strong><br />
https://www.sitepoint.com/the-psychology-of-speed/<br />
Why do people leave a website? There could be many reasons, such difficulty finding what they are looking for. But there’s a good chance users leave a site because it feels too slow to load. In this section, I want to draw some attention to psychology, and how it plays a big role in our perception of speed and performance.</p>

<p><strong>How We Track Pageviews Is All Wrong</strong><br />
https://philipwalton.com/articles/how-we-track-pageviews-is-all-wrong/<br />
The reality is the web has changed a lot in the last 10-15 years, and more and more websites don’t fit this traditional model. Our analytics tools haven’t kept up. Analytics tools should measure user engagement, and they shouldn’t be coupled to site implementation. When the user experience improves, we should be able to prove it via our analytics reports. This is the most straightforward way to make the business case for progress.</p>

<p><strong>A Comprehensive Guide To HTTP/2 Server Push</strong><br />
https://www.smashingmagazine.com/2017/04/guide-http2-server-push/<br />
In this article, you’ll learn all about server push, from how it works to the problems it solves. You’ll also learn how to use it, how to tell if it’s working, and its impact on performance. Let’s begin!</p>

<p><strong>How we made our DNS stack 3x faster</strong><br />
https://blog.cloudflare.com/how-we-made-our-dns-stack-3x-faster/<br />
Cloudflare is now well into its 6th year and providing authoritative DNS has been a core part of infrastructure from the start. Last year we decided to replace two core elements of our DNS infrastructure: the part of our DNS server that answers authoritative queries and the data pipeline which takes changes made by our customers to DNS records and distributes them to our edge machines across the globe. The rough architecture of the system can be seen above.</p>

<p><strong>Debugging Tips and Tricks</strong><br />
https://css-tricks.com/debugging-tips-tricks/<br />
I have a few tips and tricks I rely on pretty heavily and found that I give the same advice again and again during workshops, so here’s a compilation of some of them, as well as some from the community. We’ll start with some core tenets and then drill down to more specific examples.</p>

<p><strong>Mastering the Node.js CLI &amp; Command Line Options</strong><br />
https://blog.risingstack.com/mastering-the-node-js-cli-command-line-options/<br />
Node.js comes with a lot of CLI options to expose built-in debugging &amp; to modify how V8, the JavaScript engine works. In this post, we have collected the most important CLI commands to help you become more productive.</p>

<p><strong>V8 plan for Node.js LTS Carbon (A potential path to TurboFan + Ignition)</strong><br />
https://github.com/nodejs/CTC/issues/99<br />
V8 5.9 will be the first version with TurboFan + Ignition (TF+I) turned on by default. As parts of the Node.js codebase have been tuned to CrankShaft, there will be a non trivial amount of churn to adapt to the new pipeline. This also creates a security risk as CrankShaft and FullCodeGen are no longer maintained by the V8 team or tested by the Chrome security team.</p>

<h2 id="section-2">新鲜货</h2>

<p><strong>Anbox - Android in a Box</strong><br />
https://mm.gravedo.de/blog/posts/2017-04-10-introducing-anbox/<br />
Anbox puts the Android operating system into a container, abstracts hardware access and integrates core system services into a GNU/Linux system. Every Android application will behave integrated into your operating system like any other native application.</p>

<p><strong>What’s new in Microsoft Edge in the Windows 10 Creators Update</strong><br />
https://blogs.windows.com/msedgedev/2017/04/11/introducing-edgehtml-15/<br />
This release updates the Windows web platform to EdgeHTML 15, the fourth release of EdgeHTML and a major step forward both in terms of the browser user experience, web platform capabilities, and fundamentals like performance, efficiency, and accessibility. In this post, we’ll share a quick overview of what’s new in each area, for both users and web developers.</p>

<p><strong>deck.gl</strong><br />
http://uber.github.io/deck.gl/#/documentation/overview/introduction<br />
三维数据可视化库，偏向地图类的应用</p>

<p><strong>Ionic 3.0 has Arrived!</strong><br />
http://blog.ionic.io/ionic-3-0-has-arrived/<br />
We are so excited to announce the release of Ionic 3.0! This version jump may worry some of you, but don’t let it! The required changes to go from 2.x.x to 3.0.x are minimal.</p>

<p><strong>Prettier 1.0</strong><br />
http://jlongster.com/prettier-1.0<br />
Prettier is a JavaScript formatter that works by compiling your code to an AST, and then pretty-printing the AST. Like browsers wrap text, prettier will also wrap code according to a given line length. The result is good-looking code that is completely consistent no matter who wrote it.</p>

<p><strong>react-ionize</strong><br />
https://github.com/mhink/react-ionize<br />
react-ionize is a library which lets you build the “non-browser” parts of an Electron app using React components to manage your application’s state.</p>

<p><strong>React Boilrplate</strong><br />
http://www.boilrplate.com/language/react<br />
了解下流行的 React 脚手架，create-react-app 无疑是排第一的，这个网站还收录了其它的一些 Boilrplate</p>

<p><strong>web-dsp</strong><br />
https://github.com/shamadee/web-dsp<br />
WebDSP is a collection of highly performant algorithms, which are designed to be building blocks for web applications that aim to operate on media data. The methods are written in C++ and compiled to WASM, and exposed as simple vanilla Javascript functions developers can run on the client side.</p>

<p><strong>Barba.js</strong><br />
https://github.com/luruke/barba.js<br />
Barba.js is a small (4kb minified and gzipped), flexible and dependency free library that helps you creating fluid and smooth transitions between your website’s pages. It helps reducing the delay between your pages, minimizing browser HTTP requests and enhancing your user’s web experience.</p>

<p><strong>AcrossTabs</strong><br />
https://github.com/wingify/across-tabs<br />
Easy communication between cross-origin browser tabs</p>

<p><strong>chrome-remote-interface</strong><br />
https://github.com/cyrus-and/chrome-remote-interface<br />
Chrome Debugging Protocol interface that helps to instrument Chrome (or any other suitable implementation) by providing a simple abstraction of commands and notifications using a straightforward JavaScript API.</p>

<p><strong>Color Tool - Material Design</strong><br />
https://material.io/color/<br />
Create, share, and apply color palettes to your UI, as well as measure the accessibility level of any color combination.</p>

<p><strong>Musical User Interfaces</strong><br />
http://arthurcarabott.com/mui/<br />
This is an ongoing set of projects focused on better interfaces for music software. The goal is to re-think many of the ways in which audio software is designed. These are a set of prototypes for how we might interact with music software more fluently, to better realise our ideas, and encourage creativity. The primary concern is not about the quality of DSP, or the way things sound, but how we use and interact with our tools.</p>

<p><strong>腾讯开源基于微服务的平台Tars</strong><br />
http://mp.weixin.qq.com/s?__biz=MjM5MDE0Mjc4MA==&amp;mid=2650995811&amp;idx=1&amp;sn=f3feeaf543547e8f6ae565801a9fcfdc<br />
Tars主要是支持多语言的高性能RPC开发框架和配套一体化的服务治理平台，可以帮助企业或者用户以微服务的方式快速构建稳定可靠的分布式应用。Github https://github.com/Tencent/Tars</p>

<p><strong>方程式又一波大规模 0day 攻击泄漏</strong><br />
https://zhuanlan.zhihu.com/p/26375989<br />
Shadow Brokers再次泄露出一份震惊世界的机密文档，其中包含了多个精美的 。</p>

<p><strong>Nginx reaches 33.3% web server market share while Apache falls below 50%</strong><br />
https://w3techs.com/blog/entry/nginx_reaches_33_3_percent_web_server_market_share_while_apache_falls_below_50_percent<br />
Half of the web still runs on Apache’s web server, but one third already uses Nginx, and the gap is closing fast. We have a closer look at the detailed statistics and trends.</p>

<p><strong>Textbook manifesto</strong><br />
http://greenteapress.com/wp/textbook-manifesto/<br />
My textbook manifesto is so simple it sounds stupid. Here it is: Students should read and understand textbooks. That’s it.  It’s hard to imagine that anyone would disagree, but here’s the part I find infuriating: the vast majority of textbook authors, publishers, professors, and students behave as if they do not expect students to read or understand textbooks.</p>

<p><strong>Qt binding for Go (Golang)</strong><br />
https://github.com/therecipe/qt<br />
Qt is a cross-platform application framework that is used for developing application software that can be run on various software and hardware platforms with little or no change in the underlying codebase, while still being a native application with native capabilities and speed. Qt binding for Go (Golang) with support for Windows / macOS / Linux / Android / iOS / Sailfish OS / Raspberry Pi / AsteroidOS. 在跨平台 GUI 程序开发领域 qt 是除了 web 外的另一大分支。</p>

<p><strong>BetterTLS</strong><br />
http://techblog.netflix.com/2017/04/bettertls-name-constraints-test-suite.html<br />
BetterTLS is a test suite for HTTPS clients implementing verification of the Name Constraints certificate extension.</p>

<p><strong>planck.js</strong><br />
https://github.com/shakiba/planck.js<br />
重写的 Box2D</p>

<p><strong>Robert Taylor, Innovator Who Shaped Modern Computing, Dies at 85</strong><br />
https://www.nytimes.com/2017/04/14/technology/robert-taylor-innovator-who-shaped-modern-computing-dies-at-85.html<br />
向大师致敬，译文：。跟其他许多创造发明一样，互联网的诞生是许多人共同努力的结果。不过，发明这项改变世界的技术的最大功劳也许应当归属罗伯特·W·泰勒（Robert W. Taylor）。</p>

<h2 id="section-3">产品及其它</h2>

<p><strong>AutoDraw - Fast Drawing for Everyone</strong><br />
https://www.blog.google/topics/machine-learning/fast-drawing-everyone/<br />
Drawing on your phone or computer can be slow and difficult—so we created AutoDraw, a new web-based tool that pairs machine learning with drawings created by talented artists to help you draw. 这是背后的论文：.</p>

<p><strong>How to Study: A Brief Guide</strong><br />
http://www.cse.buffalo.edu/~rapaport/howtostudy.html<br />
I am going to give you some suggestions on how to study efficiently. They worked for me when I was in high school, college, and graduate school. Not only that, but they worked equally well for me in humanities courses (like philosophy and literature) and in science courses (like math and computer science).</p>

<p><strong>[译]硅谷看微信：来自微信的7堂课</strong><br />
http://mp.weixin.qq.com/s/Aqarg2HtZOYu2VKgQWUmnQ<br />
今年4月12日，Y Combinator的合伙人之一Anu Hariharan就微信发表了一篇博文。从她的角度，谈自己对微信的理解和认识。并且，从中总结了七堂课给美国的创业者。</p>

<p><strong>在阿里讲了5小时运营后，我想试着重新解读“运营”</strong><br />
http://mp.weixin.qq.com/s?__biz=MjM5NDUyOTAwOA==&amp;mid=2652915417&amp;idx=2&amp;sn=b7358b4c98f7cb3f20ce8970a315c82b<br />
在整个互联网业内，当谈及到“运营”时，我们的理解仍然是模糊、混乱和高度不清晰的。且，这个状况，不仅对于运营从业者们无益，甚至某种程度上，对于行业的发展都已经带来了一些阻碍。我们或许需要一个对于“运营”的全新解释。它应该打破此前“内容运营、用户运营、活动运营”这一类的僵硬框架，应该足够简洁清晰，也应该能够让诸多运营从业者对于自己在做的事情不再充满疑惑。</p>

<p><strong>傅盛：认知升级三部曲</strong><br />
</p>
---------------
<h1 id="#title_2" >3、iOS 开发周报：迪拜独特艺术长廊 Apple Store 建成、使用 Visual Studio Code 编写 Swift 代码</h1>
靛青K
[http://www.infoq.com/cn/news/2017/04/ios-weekly-Visual-Studio-Code-Sw?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/04/ios-weekly-Visual-Studio-Code-Sw?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>迪拜独特艺术长廊 Apple Store 建成、使用 Visual Studio Code 编写 Swift 代码</p> <i>By 靛青K</i>
---------------
<h1 id="#title_3" >4、Android开发周报：Android份额超越Windows、Apk瘦身探索</h1>
郭亮
[http://www.infoq.com/cn/news/2017/04/Android-weekly-over-windows?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/04/Android-weekly-over-windows?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>今年的Google I/O大会首场会议将在美国时间5月17日上午十点在加州举办。Android Nougat在发布近六个月后仍然无法成为该操作系统的主流版本，甚至距离很远。而目前，安卓5.X（棒棒糖）仍然占据主流地位。本期周报为大家带来了Apk瘦身、线程安全、渲染优化、React Native等技术干货，欢迎阅读。</p> <i>By 郭亮</i>
---------------
<h1 id="#title_4" >5、Microsoft对Azure Functions添加了Application Insights的支持</h1>
Kent Weare
[http://www.infoq.com/cn/news/2017/04/Azure-Functions-Insight?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/04/Azure-Functions-Insight?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/news/2017/04/Azure-Functions-Insight/zh/headerimage/GettyImages-471179856.jpg"/><p>Microsoft近期在一个博客帖子中宣布了支持Application Insights的Azure Functions初步预览版。这两个服务的集成，使得开发人员不仅可以使用内建的代码性能测量（Instrumentation），并通过一个门户网页查看代码的性能趋势，而且可以设置用于生成通知或调出外部Webhook的监控阈值。</p> <i>By Kent Weare</i> <i> Translated by Rays</i>
---------------
<h1 id="#title_5" >6、Google发布了Cloud Machine Learning API更新</h1>
Srini Penchikala
[http://www.infoq.com/cn/news/2017/04/google-cloud-machine-learning?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/04/google-cloud-machine-learning?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/news/2017/04/google-cloud-machine-learning/zh/headerimage/GettyImages-625303084.jpg"/><p> 近期在Google Cloud Next大会上，Google发布了Cloud Machine Learning API更新。其中包括用于计算机视觉、智能视频分析、语音识别、自然语言处理、机器翻译和职位搜索等领域的一系列API，使用户能构建看得见、听得到并能理解非结构化数据的机器学习应用，有助于实现下一代产品推荐、医学影像分析和欺诈检测等用例。</p> <i>By Srini Penchikala</i> <i> Translated by Rays</i>
---------------
<h1 id="#title_6" >7、安全失败实验</h1>
Ben Linders
[http://www.infoq.com/cn/news/2017/04/safe-to-fail-experiments?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/04/safe-to-fail-experiments?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>在复杂的环境中，可以使用安全失败实验探测、感知和响应。你必须知道成功和失败分别是什么样子，为了应对潜在的失败，你需要能够抑制或增强探测的效果。安全失败实验可以帮助你处理风险和不确定性，了解并保留选择的余地。</p> <i>By Ben Linders</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_7" >8、重新定义数据库历史的时刻</h1>
足下
[http://www.infoq.com/cn/news/2017/04/redefine-database-history?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/04/redefine-database-history?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>《高性能MySQL》的作者Baron Schwartz认为NoSQL并不是昙花一现。在将来，在传统关系型数据库所未能满足的三个方面将会有蓬勃发展：向后兼容的新关系型和SQL、时间序列型和流式数据库。</p> <i>By  足下</i>
---------------
<h1 id="#title_8" >9、视频演讲： 架构本质及大型电商微服务实践</h1>
王庆友
[http://www.infoq.com/cn/presentations/essence-of-architecture-practice-of-large-scale-electric-merchant-microservice?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/essence-of-architecture-practice-of-large-scale-electric-merchant-microservice?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/essence-of-architecture-practice-of-large-scale-electric-merchant-microservice/zh/mediumimage/wangqingyou270.jpg"/><p>一个架构大师必须高屋建瓴，道术结合，准确把握总体业务目标和具体技术选型。

架构的本质是系统有序化重构，适配业务发展。业务架构/应用架构/技术架构类似生产力/生产关系/生产工具的关系，它们之间有主次，有先后。

业务架构解决系统如何理解业务的问题，过程分两步。首先是业务定位和边界划分，对于复杂业务，还需要进一步抽象，形成共享业务域，构造基础业务平台。

应用架构解决系统如何合理拆分，微服务属于应用架构范畴，相比传统的 SOA 或分布式架构，它更适用复杂的业务场景（业务广度和深度复杂，业务之间存在大量共享业务逻辑）。

1 号店的微服务实践和它的业务特点高度适配，最终打造了一个形散神不散的系统，同时通过额外的技术特性（监控/流控/访问授权/水平扩展/容器化部署等）更好地支持业务。

</p> <i>By 王庆友</i>
---------------
<h1 id="#title_9" >10、文章： 单体保卫战（第一部分）</h1>
Dan Haywood
[http://www.infoq.com/cn/articles/monolith-defense-part-1?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/monolith-defense-part-1?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/monolith-defense-part-1/zh/headerimage/GettyImages-465184785.jpg"/><p>在微服务时代，“单体”变成了一个肮脏的词汇。不过，按照模块化进行设计的单体更适合用在复杂的领域，比如企业应用。这一系列的文章包含了两个部分，第1部分对微服务和单体架构的关键不同点进行了比较，列出了每种架构的优点和缺点。</p> <i>By Dan Haywood</i> <i> Translated by 薛命灯</i>
---------------
<h1 id="#title_10" >11、文章： MySQL分布式数据库高可用实践：架构、复制机制、多机房</h1>
杜明友
[http://www.infoq.com/cn/articles/practise-of-high-availability-mysql-distributed-database?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/practise-of-high-availability-mysql-distributed-database?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/practise-of-high-availability-mysql-distributed-database/zh/smallimage/risk-logo-small.jpg"/><p>网易IM云服务为百万商家亿级终端用户提供即时通信服务。商家产品爆款、用户活跃交流都在考验着我们的业务系统。如何保障系统的稳定运行，支撑更大的并发，提供真正的可扩展的IM云服务一直是我们非常关注的一个问题。 </p> <i>By 杜明友</i>
---------------
<h1 id="#title_11" >12、文章： 机器学习工程师必知的十大算法</h1>
James Le
[http://www.infoq.com/cn/articles/10-algorithms-machine-learning-engineers-need-to-know?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/10-algorithms-machine-learning-engineers-need-to-know?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/10-algorithms-machine-learning-engineers-need-to-know/zh/smallimage/legacy_systems.jpg"/><p>本文主要介绍了一些最常用的机器学习算法，包括决策树、朴素贝叶斯分类、最小二乘法、逻辑回归、支持向量机、集成方法、聚类算法、主成分分析、奇异值分解和独立成分分析。此文由原作者授权，InfoQ中文站翻译并分享。</p> <i>By James Le</i> <i> Translated by 尚剑</i>
---------------
<h1 id="#title_12" >13、视频演讲： if..., then no else: 谈构建技术体系过程中的抉择</h1>
王福强
[http://www.infoq.com/cn/presentations/the-choice-of-in-the-process-of-building-a-technical-system?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/the-choice-of-in-the-process-of-building-a-technical-system?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/the-choice-of-in-the-process-of-building-a-technical-system/zh/mediumimage/wangfuqiang270.jpg"/><p>技术体系建设和管理虽则每家企业各有特色，但也是不是无规章可寻，只不过， 就跟一个人的生命线一样，一旦选择，就没有回头路可走， 所以， 我们在选择自己企业的技术体系和管理策略的时候，就要尽量多想在前头，然后在落地过程中再根据具体情况灵活应对，以最大限度的使得整个技术体系可以平稳有效的支撑整个公司的业务发展。
本议题将围绕着“人， 事，文化”三个方面为大家分享一家之言， 希望大家可以从共性和个性两方面都能有所获益。</p> <i>By 王福强</i>
---------------
<h1 id="#title_13" >14、Visual Basic 15语言新特性</h1>
Jonathan Allen
[http://www.infoq.com/cn/news/2017/04/VB-15?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/04/VB-15?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>对于C#的两个重要特性元组和Ref返回值，Visual Basic 15提供了对等的实现。这两个特性都是“不完全的”，但已经可以提供足够的变通方案，让VB应用程序可以消费使用了这些特性的C#库。</p> <i>By Jonathan Allen</i> <i> Translated by 谢丽</i>
---------------