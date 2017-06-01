## 文章索引
1、 <a href="#1视频演讲-tera在百亿级实时搜索架构中的应用" >视频演讲： Tera在百亿级实时搜索架构中的应用</a><br/>
2、 <a href="#2xor-加密简介" >XOR 加密简介</a><br/>
3、 <a href="#3视频演讲-程序猿如何进化云上的开发运维一体化" >视频演讲： 程序猿如何进化——云上的开发运维一体化</a><br/>
4、 <a href="#4文章-时序数据库深入浅出之存储篇" >文章： 时序数据库深入浅出之存储篇</a><br/>
5、 <a href="#5文章-如何进行人力再造指导即服务" >文章： 如何进行人力再造：指导即服务</a><br/>
6、 <a href="#6视频演讲-人工智能+微服务的最佳实践分享" >视频演讲： 人工智能+微服务的最佳实践分享</a><br/>
7、 <a href="#7文章-集预测处理关联和资源优化于一体的智能运维系统" >文章： 集预测、处理、关联和资源优化于一体的智能运维系统</a><br/>
8、 <a href="#8fex-技术周刊---2017/05/31" >FEX 技术周刊 - 2017/05/31</a><br/>
9、 <a href="#9android开发周报android免安装应用开放android-studio-30版本前瞻" >Android开发周报：Android免安装应用开放、Android Studio 3.0版本前瞻</a><br/>
10、 <a href="#10ios-开发周报苹果诺基亚专利大战最终和解用-swift-中的单向数据流来替代臃肿的视图控制器" >iOS 开发周报：苹果诺基亚专利大战最终和解、用 Swift 中的单向数据流来替代臃肿的视图控制器</a><br/>
11、 <a href="#11john-davis访谈为未开发的软件计算运营成本" >John Davis访谈：为未开发的软件计算运营成本</a><br/>
12、 <a href="#12新的加密货币推进了m2m经济的构建" >新的加密货币推进了M2M经济的构建</a><br/>
13、 <a href="#13istio用于微服务的服务啮合层" >Istio：用于微服务的服务啮合层</a><br/>
14、 <a href="#14google发布了tensorflow-lite用于移动电话的神经网络库" >Google发布了Tensorflow Lite，用于移动电话的神经网络库</a><br/>
15、 <a href="#15good-vibes-and-summer-dreams:-joyful-wallpapers-for-your-desktop-june-2017-edition" >Good Vibes And Summer Dreams: Joyful Wallpapers For Your Desktop (June 2017 Edition)</a><br/><h1 id="#title_0" >1、视频演讲： Tera在百亿级实时搜索架构中的应用</h1>
齐志宏
[http://www.infoq.com/cn/presentations/tera-in-the-ten-thousand-level-real-time-search-framework?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/tera-in-the-ten-thousand-level-real-time-search-framework?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/tera-in-the-ten-thousand-level-real-time-search-framework/zh/mediumimage/quzhihong270.jpg"/><p>演讲重点介绍 Tera 作为核心技术，是如何支撑百度链接存储，实时索引筛选以及实时用户行为分析等多个重要系统的。</p> <i>By 齐志宏</i>
---------------
<h1 id="#title_1" >2、XOR 加密简介</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2017/05/xor.html](http://www.ruanyifeng.com/blog/2017/05/xor.html)
<p>本文介绍一种简单高效、非常安全的加密方法：XOR 加密。</p>

        <p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017053107.jpg" alt="" title="" /></p>

<h2>一、 XOR 运算</h2>

<p>逻辑运算之中，除了  运算，中文称为"异或运算"。</p>

<p>它的定义是：两个值相同时，返回<code>false</code>，否则返回<code>true</code>。也就是说，<code>XOR</code>可以用来判断两个值是否不同。</p>

<blockquote><pre><code class="language-javascript">
true XOR true // false
false XOR false // false
true XOR false // true
true XOR false // true
</code></pre></blockquote>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017053102.jpg" alt="" title="" /></p>

<p>JavaScript 语言的二进制运算，有一个专门的 XOR 运算符，写作<code>^</code>。</p>

<blockquote><pre><code class="language-javascript">
1 ^ 1 // 0
0 ^ 0 // 0
1 ^ 0 // 1
0 ^ 1 // 1
</code></pre></blockquote>

<p>上面代码中，如果两个二进制位相同，就返回<code>0</code>，表示<code>false</code>；否则返回<code>1</code>，表示<code>true</code>。</p>

<h2>二、 XOR 的应用</h2>

<p>XOR 运算有一个很奇妙的特点：如果对一个值连续做两次 XOR，会返回这个值本身。</p>

<blockquote><pre><code class="language-javascript">
// 第一次 XOR
1010 ^ 1111 // 0101

// 第二次 XOR
0101 ^ 1111 // 1010
</code></pre></blockquote>

<p>上面代码中，原始值是<code>1010</code>，再任意选择一个值（上例是<code>1111</code>），做两次 XOR，最后总是会得到原始值<code>1010</code>。这在数学上是很容易证明的。</p>

<h2>三、加密应用</h2>

<p>XOR 的这个特点，使得它可以用于信息的加密。</p>

<blockquote><pre><code class="language-javascript">
message XOR key // cipherText
cipherText XOR key // message
</code></pre></blockquote>

<p>上面代码中，原始信息是<code>message</code>，密钥是<code>key</code>，第一次 XOR 会得到加密文本<code>cipherText</code>。对方拿到以后，再用<code>key</code>做一次 XOR 运算，就会还原得到<code>message</code>。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017053106.gif" alt="" title="" /></p>

<h2>四、完美保密性</h2>

<p>二战期间，各国为了电报加密，对密码学进行了大量的研究和实践，其中就包括 XOR 加密。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017053103.jpg" alt="" title="" /></p>

<p>战后，英国计算机学家香农（Claude Shannon）将他的公开发表，证明了只要满足两个条件，XOR 加密是无法破解的。</p>

<blockquote>
  <ul>
<li><code>key</code>的长度大于等于<code>message</code></li>
<li><code>key</code>必须是一次性的，且每次都要随机产生</li>
</ul>
</blockquote>

<p>理由很简单，如果每次的<code>key</code>都是随机的，那么产生的<code>CipherText</code>具有所有可能的值，而且是均匀分布，无法从<code>CipherText</code>看出<code>message</code>的任何特征。也就是说，它具有最大的"信息熵"，因此完全不可能破解。这被称为 XOR 的（perfect secrecy）。</p>

<p>满足上面两个条件的<code>key</code>，叫做 （缩写为OTP），意思是"一次性密码本"，因为以前这样的<code>key</code>都是印刷成密码本，每次使用的时候，必须从其中挑选<code>key</code>。</p>

<h2>五、实例：哈希加密</h2>

<p>下面的例子使用 XOR，对用户的登陆密码进行加密。实际运行效果看。</p>

<p></p>

<p>第一步，用户设置登陆密码的时候，算出这个密码的哈希，这里使用的是 MD5 算法，也可以采用其他哈希算法。</p>

<blockquote><pre><code class="language-javascript">
const message = md5(password);
</code></pre></blockquote>

<p>第二步，生成一个随机的 key。</p>

<blockquote><pre><code class="language-javascript">
// 生成一个随机整数，范围是 [min, max]
function getRandomInt(min, max) {
  return Math.floor(Math.random() * (max - min + 1)) + min;
}

// 生成一个随机的十六进制的值，在 0 ～ f 之间 
function getHex() {
  let n = 0;
  for (let i = 4; i > 0; i--) {
    n = (getRandomInt(0, 1) << (i - 1)) + n;
  }
  return n.toString(16);
}

// 生成一个32位的十六进制值，用作一次性 Key
function getOTP() {
  const arr = [];
  for (let i = 0; i < 32; i++) {
    arr.push(getHex());
  }
  return arr.join('');
}
</code></pre></blockquote>

<p>上面代码中，生成的<code>key</code>是32位的十六进制值，对应 MD5 产生的128位的二进制哈希。</p>

<p>第三步，进行 XOR 运算，求出加密后的<code>message</code>。</p>

<blockquote><pre><code class="language-javascript">
function getXOR(message, key) {
  const arr = [];
  for (let i = 0; i < 32; i++) {
    const  m = parseInt(message.substr(i, 1), 16);
    const k = parseInt(key.substr(i, 1), 16);
    arr.push((m ^ k).toString(16));
  }
  return arr.join('');
}
</code></pre></blockquote>

<p>使用这种方法保存用户的登陆密码，即使加密文本泄露，只要一次性的密钥（<code>key</code>）没有泄露，对方也无法破解。</p>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2017-05-31T14:29:17+08:00">2017年5月31日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>博客文集：</li>
<li>社交媒体：</li>
<li>Feed订阅： </li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------
<h1 id="#title_2" >3、视频演讲： 程序猿如何进化——云上的开发运维一体化</h1>
胡平
[http://www.infoq.com/cn/presentations/how-evolution-of-program-apes?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/how-evolution-of-program-apes?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/how-evolution-of-program-apes/zh/mediumimage/huping270.jpg"/><p>介绍开发运维一体化（DevOps）在传统 DIY 方式和基于云 PaaS 方式下的区别和对比，现场演示如何利用甲骨文的开发者云迅速搭建企业开发运维一体化平台。</p> <i>By 胡平</i>
---------------
<h1 id="#title_3" >4、文章： 时序数据库深入浅出之存储篇</h1>
百度云时序数据库资深工程师
[http://www.infoq.com/cn/articles/storage-in-sequential-databases?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/storage-in-sequential-databases?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/storage-in-sequential-databases/zh/smallimage/thinking_logo.jpg"/><p>2017 年时序数据库忽然火了起来。开年 2 月 Facebook 开源了 beringei 时序数据库；到了 4 月基于 PostgreSQL 打造的时序数据库 TimeScaleDB 也开源了，而早在 2016 年 7 月，百度云在其天工物联网平台上发布了国内首个多租户的分布式时序数据库产品 TSDB，成为支持其发展制造，交通，能源，智慧城市等产业领域的核心产品，同时也成为百度战略发展产业物联网的标志性事件。时序数据库作为物联网方向一个非常重要的服务，业界的频频发声，正说明各家企业已经迫不及待的拥抱物联网时代的到来。 本文会从时序数据库的基本概念、使用场景、解决的问题一一展开，最后会从如何解决时序数据存储这一技术问题入手进行深入分析。</p> <i>By 百度云时序数据库资深工程师</i>
---------------
<h1 id="#title_4" >5、文章： 如何进行人力再造：指导即服务</h1>
Medhat Sabry
[http://www.infoq.com/cn/articles/people-reengineering-mentoring?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/people-reengineering-mentoring?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/people-reengineering-mentoring/zh/smallimage/logo1.jpg"/><p>软件行业每五年就有半数职位被新毕业生取代，这使得缺乏经验成为了业内普遍现象。人力再造引入了多种方法来应对这一现状，其中包括指导即服务。这些方法可以平顺地提高年轻一代的职业成熟度，进而改善绩效、增加员工留存率。—— Medhat Sabry</p> <i>By Medhat Sabry </i> <i> Translated by 王强</i>
---------------
<h1 id="#title_5" >6、视频演讲： 人工智能+微服务的最佳实践分享</h1>
陈辉
[http://www.infoq.com/cn/presentations/best-practice-of-artificial-intelligence-and-micro-service?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/best-practice-of-artificial-intelligence-and-micro-service?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/best-practice-of-artificial-intelligence-and-micro-service/zh/mediumimage/chenhui270.jpg"/><p>人工智能和微服务是当下最火的两个技术趋势，作为一家 AI 创业公司，我们在实践中积累了一定的机器学习微服务化经验，希望通过一些具体的案例向大家展示如何使用微服务搭建机器学习平台，以及微服务在图像识别和文本分析上的具体应用。</p> <i>By 陈辉</i>
---------------
<h1 id="#title_6" >7、文章： 集预测、处理、关联和资源优化于一体的智能运维系统</h1>
籍鑫璞
[http://www.infoq.com/cn/articles/intelligent-operation-and-maintenance-system?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/intelligent-operation-and-maintenance-system?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/intelligent-operation-and-maintenance-system/zh/smallimage/logo (34).jpg"/><p>随着业务量的增加，通过设置单纯的阈值来监控报警是远远不够的。而且这种被动式的触发报警很多时候需要人工去处理。 我们提出来DoctorStarange，它是一个智能的预测和处理系统，能够提前预测出一些监控项的报警，并提前处理预测的报警，最大程度减少报警次数；它是一个关联不同报警项的系统，能够帮助运维人员去更快地排查报警；它还是一个对机器各个维度进行检测的系统，能够优化机器资源。</p> <i>By 籍鑫璞</i>
---------------
<h1 id="#title_7" >8、FEX 技术周刊 - 2017/05/31</h1>

[http://fex.baidu.com/blog/2017/05/fex-weekly-31//](http://fex.baidu.com/blog/2017/05/fex-weekly-31//)
作者：duhongbin01 <br> <p>微信搜索『FEX』关注我们的公众号，及时获得最新资讯。</p>

<h2 id="section">深阅读</h2>

<p><strong>npm v5.0.0</strong><br />
http://blog.npmjs.org/post/161081169345/v500<br />
npm@5 takes npm a pretty big step forward, significantly improving its performance in almost all common situations, fixing a bunch of old errors due to the architecture, and just generally making it more robust and fault-tolerant. It comes with changes to make life easier for people doing monorepos, for users who want consistency/security guarantees, and brings semver support to git dependencies.</p>

<p><strong>The Architect Elevator — Visiting the upper floors</strong><br />
https://martinfowler.com/articles/architect-elevator.html<br />
Traditionally, architects were considered to be those folks who make major design decisions on a project, draw architecture diagrams, and direct developers. Those tasks are in fact better handled by the development team and modern tooling than by a single person. Many modern companies therefore eschew software architect as a separate job title, even though they highly value software architecture. The good news is that many new tasks await architects in large organizations. And they are far more interesting and impactful than drawing class diagrams. However, they require architects to engage at the upper floors of their organization.</p>

<p><strong>A Roadmap to the Programmable World</strong><br />
https://www.infoq.com/articles/iot-programmable-world-roadmap<br />
The emergence of millions of remotely programmable devices in our surroundings will pose significant challenges for software developers. A roadmap from today’s cloud-centric, data-centric Internet of Things systems to the Programmable World highlights those challenges that haven’t received enough attention.</p>

<p><strong>The state of JavaScript modules</strong><br />
https://medium.com/webpack/the-state-of-javascript-modules-4636d1774358<br />
In the following post, I will explain and summarize the current state of implementations and why I think that the transition to ES modules (ESM) will not harm the Node.js ecosystem. In the end, I will outline what these changes will mean for webpack users and module authors.</p>

<p><strong>V8, Advanced JavaScript, &amp; the Next Performance Frontier</strong><br />
https://www.youtube.com/watch?v=EdFDJANJJLs<br />
This talk will help developers write performant JavaScript, use new language constructs (ES2015+, async/await, etc.), and learn about the latest developments in modern benchmarking. We’ll also demo DevTools asynchronous debugging features and new JavaScript code coverage tools.</p>

<p><strong>Pix2code - Generating Code from a Graphical User Interface Screenshot</strong><br />
https://github.com/tonybeltramelli/pix2code<br />
Transforming a graphical user interface screenshot created by a designer into computer code is a typical task conducted by a developer in order to build customized software, websites and mobile applications. In this paper, we show that Deep Learning techniques can be leveraged to automatically generate code given a graphical user interface screenshot as input. Our model is able to generate code targeting three different platforms (i.e. iOS, Android and web-based technologies) from a single input image with over 77% of accuracy.</p>

<p><strong>What is the Future of Front End Web Development?</strong><br />
https://nolanlawson.com/2017/05/22/a-brief-and-incomplete-history-of-javascript-bundlers/<br />
这是一个值得每个 Web 开发者思考的问题，这篇文章的观点挺值得参考的：State is the big concept; We’re not building pages, we’re building systems; The line between native and web is blurring; CSS preprocessing will slowly fade away…</p>

<p><strong>A Unified Styling Language</strong><br />
https://medium.com/seek-blog/a-unified-styling-language-d0c208de2660<br />
In the past few years we’ve seen the rise of CSS-in-JS, emerging primarily from within the React community. This, of course, hasn’t been without its controversies. Many people, particularly those already intimately familiar with CSS, have looked on in disbelief. “Why would anyone want to write CSS in JS? Surely this is a terrible idea! If only they’d learn CSS!” If this was your reaction, then read on. We’re going to take a look at why writing your styles in JavaScript isn’t such a terrible idea after all, and why I think you should be keeping an eye on this rapidly evolving space.</p>

<p><strong>Chrome won</strong><br />
https://andreasgal.com/2017/05/25/chrome-won/<br />
前 Mozilla CTO 对浏览器发展的分析：Chrome is eating the browser market, and everyone else except Safari is getting obliterated. Does this mean Google owns the Web if they own Chrome? No. Absolutely not. Browsers are what the Web looked like in the first decades of the Internet. Mobile disrupted the Web, but the Web embraced mobile and at the heart of most apps beats a lot of JavaScript and HTTPS and REST these days. The future Web will look yet again completely different. Much will survive, and some parts of it will get disrupted.</p>

<p><strong>IBM, Google and Lyft give microservices a ride on the Istio Service Mesh</strong><br />
https://developer.ibm.com/dwblog/2017/istio/<br />
IBM and Google announced the launch of </p>

<p><strong>Node.js Streams: Everything you need to know</strong><br />
https://medium.freecodecamp.com/node-js-streams-everything-you-need-to-know-c9141306be93<br />
Node.js streams have a reputation for being hard to work with, and even harder to understand. Well I’ve got good news for you — that’s no longer the case. Over the years, developers created lots of packages out there with the sole purpose of making working with streams easier. But in this article, I’m going to focus on the native Node.js stream API.</p>

<p><strong>The Roadmap for React: Fiber and Beyond</strong><br />
https://www.youtube.com/watch?v=QW5TE4vrklU<br />
Andrew Clark, an engineer on the React team at Facebook, shares what’s in the pipeline for React 16 and beyond.</p>

<p><strong>React vs Angular: Two Sides of JavaScript</strong><br />
https://blog.prototypr.io/react-vs-angular-two-sides-of-javascript-b850de22b413<br />
Bringing our knowledge together, we decided to shed some light on React vs Angular question and share some thoughts with you. Thus, in this article, we are going to transform our front-end development experience into something that will help you to determine the technology that fits you better.</p>

<p><strong>Rebuilding Slack’s Emoji Picker in React</strong><br />
https://slack.engineering/rebuilding-slacks-emoji-picker-in-react-bfbd8ce6fbfe<br />
We determined that the best way to introduce React would be to rebuild an existing product feature — that way, we could compare the development process and end result to a known quantity. We wanted a component that was interactive, self-contained, and demanding enough to prove our assumption that React could improve performance. It didn’t take long to find a perfect candidate — the highly used and surprisingly complex Emoji Picker.</p>

<p><strong>Why is Marko Fast?</strong><br />
https://medium.com/@psteeleidem/why-is-marko-fast-a20796cb8ae3<br />
Instead of focusing on benchmarks in this article, I want to focus on the details of optimizations that we have applied to Marko.</p>

<p><strong>Server-Sent Events 教程</strong><br />
http://www.ruanyifeng.com/blog/2017/05/server-sent_events.html<br />
服务器向浏览器推送信息，除了 WebSocket，还有一种方法：Server-Sent Events（以下简称 SSE）。本文介绍它的用法。</p>

<p><strong>Node.js cluster 踩坑小结</strong><br />
https://zhuanlan.zhihu.com/p/27069865<br />
如果你要一个 common 的中规中矩的 LB 推荐用 nginx，如果你要比较好的均衡推荐用 HAproxy（不过不能像 nginx 那样处理静态文件），如果你要 LB 不差缓存比 nginx 好一点的可以用 Varnish（当然资源缓存最好用 CDN）。</p>

<p><strong>[译]浏览器前端优化</strong><br />
http://zcfy.cc/article/optimising-the-front-end-for-the-browser-hacker-noon-2847.html<br />
对之前《Optimising the front end for the browser》一文的翻译，通过浏览器加载过程来介绍</p>

<p><strong>Hyperloop，让发布简洁高效</strong><br />
http://tech.meituan.com/iOS_Hyperloop.html<br />
Hyperloop 是服务于美团点评客户端的组件发版、持续集成、App 打包构建、资源调度等各个环节的发布调度系统。名称起源于美国 Elon Musk 构想的 Hyperloop 超级高铁，象征着现代、简洁、高效。Hyperloop 提供了一站式的平台，管理着美团点评 iOS 业务的超过 300 个组件和包括美团 iOS 客户端在内的4个App。</p>

<p><strong>美图图像选型评测及优化历程</strong><br />
https://mp.weixin.qq.com/s?__biz=MzAwMDU1MTE1OQ==&amp;mid=2653548744&amp;idx=1&amp;sn=d08a1988f686e1096c0fee14dc2e53c8<br />
图像的格式及编码是互联网应用非常关键的基础架构问题，同时如何选择合适的图片格式，如何选择合适的压缩算法以及相关参数都是很有挑战性的技术难点。本文作者是美图资深图像处理专家，介绍其评测对比常用格式及常用算法和工具的优缺点，可以作为相关技术选型及优化的重要参考。</p>

<p><strong>Solving the Last Item Problem for a Circular Distribution with Partially Overlapping Items</strong><br />
https://css-tricks.com/solving-last-item-problem-circular-distribution-partially-overlapping-items<br />
介绍通过CSS3 3D变换的方法来实现卡片环绕分布的效果，最后又给出几个结合animation的动画效果的demo</p>

<p><strong>You might not need to transpile your JavaScript</strong><br />
https://medium.freecodecamp.com/you-might-not-need-to-transpile-your-javascript-4d5e0a438ca<br />
This post is not as wild as, say, YouMightNotNeedJS.com, but it does elaborate on transpilation, and explains why it may not be as necessary in the near future.</p>

<p><strong>Kill Google AMP before it KILLS the web</strong><br />
https://www.theregister.co.uk/2017/05/19/open_source_insider_google_amp_bad_bad_bad/<br />
In my view, don’t go far enough in stating the problem and I feel this needs to be said very clearly: Google’s AMP is bad – bad in a potentially web-destroying way. Google AMP is bad news for how the web is built, it’s bad news for publishers of credible online content, and it’s bad news for consumers of that content. 另附：.</p>

<p><strong>HTTPS on Stack Overflow: The End of a Long Road</strong><br />
https://nickcraver.com/blog/2017/05/22/https-on-stack-overflow/<br />
We deployed HTTPS by default on Stack Overflow. All traffic is now redirected to https:// and Google links will change over the next few weeks. The activation of this is quite literally flipping a switch (feature flag), but getting to that point has taken years of work. As of now, HTTPS is the default on all Q&amp;A websites. We’ve been rolling it out across the Stack Exchange network for the past 2 months. Stack Overflow is the last site, and by far the largest. This is a huge milestone for us, but by no means the end. There’s still more work to do, which we’ll get to.</p>

<p><strong>View Counting at Reddit</strong><br />
https://redditblog.com/2017/05/24/view-counting-at-reddit/<br />
Vote score and number of comments were the main indicators of activity on a given post. We wanted to build a system that could capture this activity by counting the number of views a post received. This number is then shown to content creators and moderators to provide them better insight into the activity on specific posts. In this post, we’re going to talk about how we implemented counting at scale.</p>

<p><strong>Automation as a Service — Introducing Scriptflask</strong><br />
https://medium.com/netflix-techblog/automation-as-a-service-introducing-scriptflask-17a8e4ad954b<br />
In our previous post, we spoke about building a common set of utilities — shell/python scripts that would communicate with each microservice in the netflix service ecosystem — which gave us an easy way to fetch data and make data assertions on any part of the data service pipeline. However, we began to hit the limits of our model much faster than we expected. In the following section, we talk about some of the obstacles we faced and how we developed a solution to overcome this.</p>

<p><strong>Writing a Really, Really Fast JSON Parser</strong><br />
https://chadaustin.me/2017/05/writing-a-really-really-fast-json-parser/<br />
I used to think JSON parsing was not something you ever wanted in your application’s critical path. It’s certainly not the kind of algorithm that modern computers love (read byte, branch, read byte, branch). That said, this problem has been beaten to death. We now have multiple parsers that can parse data at hundreds of megabytes per second — around the same rate as SHA-256! If we relaxed some of the constraints on sajson, it could even go faster.</p>

<p><strong>Best Practices for Long Scrolling</strong><br />
https://blogs.adobe.com/creativecloud/best-practices-for-long-scrolling/<br />
Long scrolling can create a completely immersive browsing experience. If users like a UI and find it intuitive, then they won’t really mind the length of the scrolling. Thus, focus on their goals and make things more convenient for your users.</p>

<h2 id="section-1">新鲜货</h2>

<p><strong>Introducing GitHub Marketplace and more tools to customize your workflow</strong><br />
https://github.com/blog/2359-introducing-github-marketplace-and-more-tools-to-customize-your-workflow<br />
 is a new way to discover and purchase tools that extend your workflow. Find apps to use across your development process, from continuous integration to project management and code review. Then start using them without setting up multiple accounts or payment methods. More than a dozen integrators have apps in GitHub Marketplace today, including Travis CI, Appveyor, Waffle, ZenHub, Sentry, and Codacy—with more coming soon.</p>

<p><strong>Node.js 8.0 RC1</strong><br />
https://nodejs.org/download/rc/v8.0.0-rc.1/<br />
另附：</p>

<p><strong>全球最大的 Git Repo 诞生了</strong><br />
http://top.jobbole.com/36865/<br />
微软 24 日宣布，当前该公司几乎所有工程师都已经 。</p>

<p><strong>Stack Overflow: Helping One Million Developers Exit Vim</strong><br />
https://stackoverflow.blog/2017/05/23/stack-overflow-helping-one-million-developers-exit-vim/<br />
In the five years since this question was asked, there have been over a million other developers who got stuck in Vim and couldn’t escape without a bit of help. In honor of this milestone, we decided to take a look at the data surrounding this question. In particular, we’ll try measuring who is most likely to get stuck in Vim as opposed to using it intentionally, and examining how that balance varies by country and by programming language.</p>

<p><strong>Kotlin is like TypeScript</strong><br />
https://gi-no.github.io/kotlin-is-like-typescript/<br />
方便熟悉 TypeScript 的人学习 Kotlin。另附：。</p>

<p><strong>Preact-cli</strong><br />
https://github.com/developit/preact-cli<br />
Your next Preact PWA starts in 30 seconds.</p>

<p><strong>Blockstack</strong><br />
https://github.com/blockstack/blockstack<br />
 is a new decentralized internet where you own your data and your apps run locally without remote servers. Blockstack provides decentralized services for naming/DNS, identity, authentication and storage. Developers can use JavaScript libraries to build serverless apps and they don’t need to worry about managing infrastructure. Blockstack replaces the current client/server model; users control their data, apps run client-side, and the open Blockstack network replaces server-side functionality.</p>

<p><strong>ORY Editor</strong><br />
https://github.com/ory/editor<br />
The ORY Editor is a smart, extensible and modern editor (“WYSIWYG”) for the web written in React. If you are fed up with the limitations of contenteditable, you are in the right place. The ORY Editor is used at Germany’s largest (~800k uniques per month) E-Learning Website www.serlo.org to improve the wiki experience.</p>

<p><strong>Moon - A minimal, blazing fast UI library</strong><br />
https://github.com/KingPixil/moon<br />
仿照 VUE 的 api，但体积只有 6k，而且号称性能更好</p>

<p><strong>Razzle</strong><br />
https://github.com/jaredpalmer/razzle<br />
Create server-rendered universal JavaScript applications with no configuration</p>

<p><strong>ngVue</strong><br />
https://github.com/ngVue/ngVue<br />
Use Vue2 components in Angular 1.x</p>

<p><strong>Birdview.js</strong><br />
http://achrafkassioui.com/birdview/<br />
用户获取整个web页面鸟瞰图的一个JS库，但在处理position:fixed元素、overflow:hidden的内容会有些小问题。</p>

<p><strong>GetImageColors: Get Colors From Your Images</strong><br />
https://www.getimagecolors.com/<br />
获取图片中各种颜色的占比情况，对颜色对比鲜明的图片识别情况比较好</p>

<p><strong>Waterdroplet WebGL Shader</strong><br />
https://codepen.io/stefanweck/pen/Vbgeax<br />
模拟雨滴在窗户上滑落的场景，通过JS实现雨滴的模拟并用WebGL shader来完成雨滴粘黏和下滴的效果。</p>

<p><strong>4 CSS Filters For Adjusting Color</strong><br />
http://vanseodesign.com/css/4-css-filters-for-adjusting-color/<br />
介绍了4种通过CSS改变图片颜色的方式，grayscale，hue-rotate，saturate，sepia</p>

<p><strong>The Top 9 Animation Libraries for UI Designers in 2017</strong><br />
https://www.sitepoint.com/our-top-9-animation-libraries/</p>

<p><strong>Linux Inside</strong><br />
https://0xax.gitbooks.io/linux-insides/content/<br />
A book-in-progress about the linux kernel and its insides. The goal is simple - to share my modest knowledge about the insides of the linux kernel and help people who are interested in linux kernel insides, and other low-level subject matter.</p>

<h2 id="section-2">产品及其它</h2>

<p><strong>扎克伯格哈佛毕业演讲：使命感能创造真正的快乐</strong><br />
https://mp.weixin.qq.com/s?__biz=MzA5NzIwMjQzMA==&amp;mid=2649819081&amp;idx=6&amp;sn=e99391c0f2360197dc6fb4645319a1bc<br />
作为千禧一代，我们会出于直觉和本能发现目标。仅仅发现目标还不够，我们这代人面临的挑战，是创造一个人人都能有使命感的世界。使命感使我们意识到我们身上有比自己更重要的东西，我们是被需要的，我们要为之加倍努力。使命感能创造真正的快乐。创造一个每个人都有使命感的世界的三种方法：一起做有意义的项目；通过重新定义平等，使每个人都有追求目标的自由；在全世界建立社群。</p>

<p><strong>从员工出走仅剩 5 人，到一支打胜仗的铁军</strong><br />
https://mp.weixin.qq.com/s?__biz=MjM5OTM5OTAyMQ==&amp;mid=2654431377&amp;idx=1&amp;sn=f04113b5481edde211f69755fb465cd9<br />
讲京东的企业文化与组织效能，这几个观点挺有意思的：对创业公司而言，一定要以结果为导向，以效率为导向，要有公平意识，但是不能以公平为导向；卓越领导力的三个原型——内在力量：温柔、勇敢、顽皮；从来没有什么救世主，更没有所谓的专家，不能 All in 的外部顾问和专家都是耍流氓；没有任何人能够被管理，人只能管理自己，每个人都是自己的上帝，不能成为别人的上帝，人们可以被领导，但不能被强制，人们只服从自己的意愿。</p>

<p><strong>终于明白1135家制造企业怎么把自己玩死了</strong><br />
http://www.iheima.com/zixun/2017/0529/163340.shtml<br />
统制造企业的困境与其说是因为外部环境的挑战，还不如说是自己内部作死。他们是通过一次次美好而成功的战术，让自己最终陷入了战略困境之网，现在是越挣扎，网子勒的越紧。中国制造之振兴，首先在于工业文化之振兴，破除巨婴情结，让企业学会面对现实，学会像成年人一样思考问题，让员工。中国现在需要的不是一场以“智能制造”为名的政治运动，而是一场全面的制造业文艺复兴。</p>
---------------
<h1 id="#title_8" >9、Android开发周报：Android免安装应用开放、Android Studio 3.0版本前瞻</h1>
郭亮
[http://www.infoq.com/cn/news/2017/05/Android-weekly-Free-install?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/05/Android-weekly-Free-install?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>近日Google发布了Android Studio 3.0金丝雀版，改版本增加了对Kotlin的支持、提升速度等20多项功能。Android免安装应用对所有开发者开放，Android的又一大进步正式发力。本期周报为大家带来了多篇关于Kotlin的文章，还有截屏、GC等技术干货，欢迎阅读。</p> <i>By 郭亮</i>
---------------
<h1 id="#title_9" >10、iOS 开发周报：苹果诺基亚专利大战最终和解、用 Swift 中的单向数据流来替代臃肿的视图控制器</h1>
靛青K
[http://www.infoq.com/cn/news/2017/05/ios-weekly-Apple-NOKIA-patent-se?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/05/ios-weekly-Apple-NOKIA-patent-se?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>苹果诺基亚专利大战最终和解、用 Swift 中的单向数据流来替代臃肿的视图控制器</p> <i>By 靛青K</i>
---------------
<h1 id="#title_10" >11、John Davis访谈：为未开发的软件计算运营成本</h1>
Daniel Bryant
[http://www.infoq.com/cn/news/2017/05/calculating-cost-software?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/05/calculating-cost-software?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>DevOps企业峰会将于6月5号和6号在伦敦举行，来自easyJet的首席架构师John Davis将会带来“为未开发的软件计算运营成本”的演讲。InfoQ与Davis进行了交谈，讨论了一些事项，包括传统企业的IT项目开发如何迁移到协作性更强的“DevOps”上来、项目管理和成本管理将会发生怎样的变化，以及如何通过微服务和自动化性能测试为现有服务预测未来的成本。</p> <i>By Daniel Bryant</i> <i> Translated by 薛命灯</i>
---------------
<h1 id="#title_11" >12、新的加密货币推进了M2M经济的构建</h1>
Ignacio Aguerrevere
[http://www.infoq.com/cn/news/2017/05/iota-cryptocurrency-m2m-economy?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/05/iota-cryptocurrency-m2m-economy?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p> IOTA正在推进自己的加密货币协议，意在创建一种物联网设备适用的经济形态。IOTA的目标是实现在数十亿互联网驱动设备间的货币及数据交换。</p> <i>By Ignacio Aguerrevere</i> <i> Translated by Rays</i>
---------------
<h1 id="#title_12" >13、Istio：用于微服务的服务啮合层</h1>
Abel Avram
[http://www.infoq.com/cn/news/2017/05/istio?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/05/istio?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Google、IBM和Lyft开源了微服务管理、保护和监控框架Istio。Istio为希腊语，意思是“启航”。</p> <i>By Abel Avram</i> <i> Translated by Rays</i>
---------------
<h1 id="#title_13" >14、Google发布了Tensorflow Lite，用于移动电话的神经网络库</h1>
Roland Meertens
[http://www.infoq.com/cn/news/2017/05/google-tensorflow-lite?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/05/google-tensorflow-lite?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Google宣布了一个专门针对移动电话而优化的Tensorflow新版本，称为Tensorflow Lite。它允许开发人员在用户的移动电话上实时地运行人工智能应用。该库在设计上力求更快和更小的同时，依然支持最先进的技术。</p> <i>By Roland Meertens</i> <i> Translated by Rays</i>
---------------
<h1 id="#title_14" >15、Good Vibes And Summer Dreams: Joyful Wallpapers For Your Desktop (June 2017 Edition)</h1>
Cosima Mielke
[https://www.smashingmagazine.com/2017/05/desktop-wallpaper-calendars-june-2017/](https://www.smashingmagazine.com/2017/05/desktop-wallpaper-calendars-june-2017/)
<table width="650">
	<tr>
		<td width="650">
			<div style="width:650px;">
				<img src="http://statisches.auslieferung.commindo-media-ressourcen.de/advertisement.gif" alt="" border="0"/>
				<br/>
				<a href="http://auslieferung.commindo-media-ressourcen.de/random.php?mode=target&collection=smashing-rss&position=1" target="_blank">
					<img src="http://auslieferung.commindo-media-ressourcen.de/random.php?mode=image&collection=smashing-rss&position=1" border="0" alt=""/>
				</a>
				&nbsp;
				<a href="http://auslieferung.commindo-media-ressourcen.de/random.php?mode=target&collection=smashing-rss&position=2" target="_blank">
					<img src="http://auslieferung.commindo-media-ressourcen.de/random.php?mode=image&collection=smashing-rss&position=2" border="0" alt=""/>
				</a>
				&nbsp;
				<a href="http://auslieferung.commindo-media-ressourcen.de/random.php?mode=target&collection=smashing-rss&position=3" target="_blank">
					<img src="http://auslieferung.commindo-media-ressourcen.de/random.php?mode=image&collection=smashing-rss&position=3" border="0" alt=""/>
				</a>
			</div>
		</td>
	</tr>
</table><p>Where do you seek inspiration? In the bright colors that nature is showing at this time of year? A conversation with a friend maybe? Or a journey you recently went on? Well, we also might have something for you: Our <strong>monthly desktop wallpapers</strong> post is an opportunity to refuel your creative battery and get a little in-between inspiration shot — since nine years already.</p>
<figure></figure>
<p>Each month, artists and designers from across the globe challenge their creative skills to create inspiring, unique, and simply beautiful wallpapers for you to indulge in. Wallpapers that are a bit more distinctive as the usual crowd and that’ll, hopefully, cater for some fresh ideas.</p><p>The post .</p>
---------------