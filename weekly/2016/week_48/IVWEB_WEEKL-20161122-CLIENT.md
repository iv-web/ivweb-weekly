## 文章索引
1、 <a href="#1android-译-react-native-android-的-native-模块" >[Android] [译] React Native Android 的 native 模块</a><br/>
2、 <a href="#2android-重识-okhttp探究源码设计" >[Android] 重识 OkHttp——探究源码设计</a><br/>
3、 <a href="#3android-adapter-使用-butterknife-的简单封装" >[Android] adapter 使用 butterknife 的简单封装</a><br/>
4、 <a href="#4工具资源-git-的原理简析" >[工具资源] Git 的原理简析</a><br/>
5、 <a href="#5css-inheritance-the-cascade-and-global-scope:-your-new-old-worst-best-friends" >CSS Inheritance, The Cascade And Global Scope: Your New Old Worst Best Friends</a><br/>
6、 <a href="#6前端-理解-js-事件循环二-macrotask-和-microtask" >[前端] 理解 js 事件循环二 (macrotask 和 microtask)</a><br/>
7、 <a href="#7前端-003-期ddfe-技术周刊" >[前端] [003 期]DDFE 技术周刊</a><br/>
8、 <a href="#8后端-docker-入门概览" >[后端] docker 入门概览</a><br/>
9、 <a href="#9后端-张大胖的-socket" >[后端] 张大胖的 socket</a><br/>
10、 <a href="#10后端-张大胖学递归" >[后端] 张大胖学递归</a><br/>
11、 <a href="#11后端-编译还是解释" >[后端] 编译还是解释？</a><br/>
12、 <a href="#12后端-常见数据结构-二--树-二叉树红黑树b-树" >[后端] 常见数据结构 (二)- 树 (二叉树，红黑树，B 树)</a><br/>
13、 <a href="#13后端-常见数据结构-一--栈-队列-堆-哈希表" >[后端] 常见数据结构 (一)- 栈, 队列, 堆, 哈希表</a><br/>
14、 <a href="#14后端-部署流水线搭建小记dockerjenkinsjava-和-couchbase" >[后端] 部署流水线搭建小记：Docker、Jenkins、Java 和 Couchbase</a><br/>
15、 <a href="#15设计-15-款优质实用简洁的个人简历模板打包下载-一" >[设计] 15 款优质实用简洁的个人简历模板打包下载 （一）</a><br/>
16、 <a href="#16阅读-真实世界的全栈工程师的十八项必备技能" >[阅读] 真实世界的全栈工程师的十八项必备技能</a><br/>
17、 <a href="#17前端-如何写出漂亮的-react-组件" >[前端] 如何写出漂亮的 React 组件</a><br/>
18、 <a href="#18前端-探索-rxjs---做一个-github-小应用" >[前端] 探索 RxJS - 做一个 github 小应用</a><br/>
19、 <a href="#19fex-技术周刊---2016/11/21" >FEX 技术周刊 - 2016/11/21</a><br/>
20、 <a href="#20javaslang-30之路" >Javaslang 3.0之路</a><br/>
21、 <a href="#21logzio提供了基于机器学习的日志分析" >Logz.io提供了基于机器学习的日志分析</a><br/>
22、 <a href="#22微软发布aspnet-core-11的第一个预览版本" >微软发布Asp.Net Core 1.1的第一个预览版本</a><br/>
23、 <a href="#23webassembly浏览器预览版收集社区反馈" >WebAssembly浏览器预览版收集社区反馈</a><br/>
24、 <a href="#242016企业开发趋势lightbend关于jvm开发者的调查" >2016企业开发趋势：Lightbend关于JVM开发者的调查</a><br/>
25、 <a href="#25视频演讲-宜信大数据金融应用在lain容器paas上的落地" >视频演讲： 宜信大数据金融应用在LAIN容器PaaS上的落地</a><br/>
26、 <a href="#26视频演讲-百鬼夜行の看不见的无线安全" >视频演讲： 百鬼夜行の看不见的无线安全</a><br/>
27、 <a href="#27视频访谈-黄桦如何正确使用知识图谱" >视频访谈： 黄桦：如何正确使用知识图谱</a><br/>
28、 <a href="#28文章-从两个风格迥异的api平台说开去" >文章： 从两个风格迥异的API平台说开去</a><br/>
29、 <a href="#29文章-技术演讲三板斧思路布局全盘演练临场把控" >文章： 技术演讲三板斧：思路布局、全盘演练、临场把控</a><br/>
30、 <a href="#30文章-对话亚马逊一号员工shel-kaphan" >文章： 对话亚马逊一号员工Shel Kaphan</a><br/>
31、 <a href="#31视频演讲-如何通过-app+wi-fi-数据给企业做大数据精准用户画像" >视频演讲： 如何通过 APP+Wi-Fi 数据给企业做大数据精准用户画像</a><br/>
32、 <a href="#32编辑精选有关-bluemix-的强大功能的最受欢迎教程" >编辑精选：有关 Bluemix 的强大功能的最受欢迎教程</a><br/>
33、 <a href="#33前端-最全的资源教程前端涉及的所有知识体系" >[前端] 最全的资源教程：前端涉及的所有知识体系</a><br/>
34、 <a href="#34spotify-playlists-to-fuel-your-coding-and-design-sessions" >Spotify Playlists To Fuel Your Coding And Design Sessions</a><br/><h1 id="#title_0" >1、[Android] [译] React Native Android 的 native 模块</h1>
ShirleyYang
[http://gold.xitu.io/entry/5832e55fc4c971005f565b4c](http://gold.xitu.io/entry/5832e55fc4c971005f565b4c)
<p>跟着作者，来试试做一个跟 ImagePickerIOS 差不多的安卓组件吧。用 Java 编写自己的 native 模块技能点 get ！</p><p></p>
---------------
<h1 id="#title_1" >2、[Android] 重识 OkHttp——探究源码设计</h1>
sososeen09
[http://gold.xitu.io/entry/5833058f67f356005bfae0cb](http://gold.xitu.io/entry/5833058f67f356005bfae0cb)
<p>探究 OkHttp 的源码设计，更深刻的理解，以便更灵活地运用</p><p></p>
---------------
<h1 id="#title_2" >3、[Android] adapter 使用 butterknife 的简单封装</h1>
deadline
[http://gold.xitu.io/entry/58331bcaa0bb9f005a1074ba](http://gold.xitu.io/entry/58331bcaa0bb9f005a1074ba)
<p>adapter 使用 butterknife 的简单封装</p><p></p>
---------------
<h1 id="#title_3" >4、[工具资源] Git 的原理简析</h1>
maimingliang
[http://gold.xitu.io/entry/5832f35c5c497d006b27d76b](http://gold.xitu.io/entry/5832f35c5c497d006b27d76b)
<img src="http://ac-mhke0kuv.clouddn.com/561e12ab8e55b8e95fb9.png?imageView/2/w/800/h/600/q/80/format/png"/><p>Git 的原理简析</p><p></p>
---------------
<h1 id="#title_4" >5、CSS Inheritance, The Cascade And Global Scope: Your New Old Worst Best Friends</h1>
Heydon Pickering
[https://www.smashingmagazine.com/2016/11/css-inheritance-cascade-global-scope-new-old-worst-best-friends/](https://www.smashingmagazine.com/2016/11/css-inheritance-cascade-global-scope-new-old-worst-best-friends/)
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
</table><p>I'm big on . I've long been sold on dividing websites into components, not pages, and amalgamating those components dynamically into interfaces. Flexibility, efficiency and maintainability abound.</p>

<figure></figure>

<p>But I don't want my design to <em>look</em> like it's made out of unrelated things. I'm making an interface, not a surrealist photomontage. As luck would have it, there is already a technology, called CSS, which is designed specifically to solve this problem. Using CSS, I can propagate styles that cross the borders of my HTML components, <strong>ensuring a consistent design with minimal effort</strong>.</p>



<p>The post .</p>
---------------
<h1 id="#title_5" >6、[前端] 理解 js 事件循环二 (macrotask 和 microtask)</h1>
晨辰
[http://gold.xitu.io/entry/58332d560ce46300610e4bad](http://gold.xitu.io/entry/58332d560ce46300610e4bad)
<p>通过 macrotask 和 microtask 更好的去理解 js 的事件循环</p><p></p>
---------------
<h1 id="#title_6" >7、[前端] [003 期]DDFE 技术周刊</h1>
滴滴出行·DDFE
[http://gold.xitu.io/entry/58330af8a22b9d006c6d0705](http://gold.xitu.io/entry/58330af8a22b9d006c6d0705)
<p>《藏经阁，中国软件开发者大会嘉宾的演讲稿》、《JavaScript 运行机制详解：再谈 Event Loop》、《JavaScript ES6 核心功能一览》……</p><p></p>
---------------
<h1 id="#title_7" >8、[后端] docker 入门概览</h1>
brianway
[http://gold.xitu.io/entry/58330a328ac247005a16d614](http://gold.xitu.io/entry/58330a328ac247005a16d614)
<img src="http://ac-mhke0kuv.clouddn.com/d66660ba6fa2601947ff.png?imageView/2/w/800/h/600/q/80/format/png"/><p>本文对 docker 进行大致介绍，包括概述, 安装, 简单使用, 架构, 基本原理等方面</p><p></p>
---------------
<h1 id="#title_8" >9、[后端] 张大胖的 socket</h1>
刘欣
[http://gold.xitu.io/entry/5832ed602f301e0061d7c79b](http://gold.xitu.io/entry/5832ed602f301e0061d7c79b)
<img src="http://ac-mhke0kuv.clouddn.com/620f45657734604a7bb2.jpg?imageView/2/w/800/h/600/q/80/format/png"/><p>socket 是对 TCP 的良好抽象</p><p></p>
---------------
<h1 id="#title_9" >10、[后端] 张大胖学递归</h1>
刘欣
[http://gold.xitu.io/entry/5832ecfa2e958a005de73129](http://gold.xitu.io/entry/5832ecfa2e958a005de73129)
<img src="http://ac-mhke0kuv.clouddn.com/e4cf798fff45a4a01a7f.jpg?imageView/2/w/800/h/600/q/80/format/png"/><p>尾递归在机器层面很容易理解</p><p></p>
---------------
<h1 id="#title_10" >11、[后端] 编译还是解释？</h1>
刘欣
[http://gold.xitu.io/entry/5832ec86da2f600061c7f547](http://gold.xitu.io/entry/5832ec86da2f600061c7f547)
<img src="http://ac-mhke0kuv.clouddn.com/f23026d8c7a67336e529.jpg?imageView/2/w/800/h/600/q/80/format/png"/><p>了解了底层原理， 不用太纠结什么是编译，什么是解释</p><p></p>
---------------
<h1 id="#title_11" >12、[后端] 常见数据结构 (二)- 树 (二叉树，红黑树，B 树)</h1>
brianway
[http://gold.xitu.io/entry/58330d1067f356005bfb211b](http://gold.xitu.io/entry/58330d1067f356005bfb211b)
<img src="http://ac-mhke0kuv.clouddn.com/3220ea5e715d1ca503c7.jpeg?imageView/2/w/800/h/600/q/80/format/png"/><p>本文介绍数据结构中几种常见的树: 二分查找树，2-3 树，红黑树，B 树。</p><p></p>
---------------
<h1 id="#title_12" >13、[后端] 常见数据结构 (一)- 栈, 队列, 堆, 哈希表</h1>
brianway
[http://gold.xitu.io/entry/58330cbfa0bb9f005a0fed62](http://gold.xitu.io/entry/58330cbfa0bb9f005a0fed62)
<img src="http://ac-mhke0kuv.clouddn.com/1e8bfd8990d9d14c21bf.jpeg?imageView/2/w/800/h/600/q/80/format/png"/><p>本文介绍几种常见的数据结构: 栈、队列、堆、哈希表，等等。</p><p></p>
---------------
<h1 id="#title_13" >14、[后端] 部署流水线搭建小记：Docker、Jenkins、Java 和 Couchbase</h1>
Docker精选
[http://gold.xitu.io/entry/5833896fd203090058cff054](http://gold.xitu.io/entry/5833896fd203090058cff054)
<img src="http://ac-mhke0kuv.clouddn.com/4f09d92c8dc3a736c209.jpg?imageView/2/w/800/h/600/q/80/format/png"/><p>这篇文章讲述了如何用 Jenkins 和 Docker 来为一个需要和数据库交互的 Java 应用创建部署流水线（deployment pipeline）。</p><p></p>
---------------
<h1 id="#title_14" >15、[设计] 15 款优质实用简洁的个人简历模板打包下载 （一）</h1>
稀土区
[http://gold.xitu.io/entry/5832dbb6c4c971005f561347](http://gold.xitu.io/entry/5832dbb6c4c971005f561347)
<img src="http://ac-mhke0kuv.clouddn.com/e1c8deb79e3b841ed05f.jpg?imageView/2/w/800/h/600/q/80/format/png"/><p>简历在求职中必不可少，本次分享的简历简介精致，而且样式多种多样。包含 INDD、IDML、PDF、PSD、DOCX 等格式，方便自由修改和学习。</p><p></p>
---------------
<h1 id="#title_15" >16、[阅读] 真实世界的全栈工程师的十八项必备技能</h1>
Phodal
[http://gold.xitu.io/entry/58338678c59e0d005f40a5a5](http://gold.xitu.io/entry/58338678c59e0d005f40a5a5)
<img src="http://ac-mhke0kuv.clouddn.com/7976c8d617ba82f36fe3.jpg?imageView/2/w/800/h/600/q/80/format/png"/><p>原来编码只是十八分之一的技能~~</p><p></p>
---------------
<h1 id="#title_16" >17、[前端] 如何写出漂亮的 React 组件</h1>
王下邀月熊
[http://gold.xitu.io/entry/5832dae0c4c971005f5608ff](http://gold.xitu.io/entry/5832dae0c4c971005f5608ff)
<p>在 Walmart Labs 的产品开发中，我们进行了大量的 Code Review 工作，这也保证了我有机会从很多优秀的工程师的代码中学习他们的代码风格与样式。在这篇博文里我会分享出我最欣赏的五种组件模式与代码片。不过我首先还是要谈谈为什么我们需要执着于提高代码的阅读体验。就好像你有很多种方式去装扮一只猫，如果你把你的爱猫装扮成了如下这样子:</p><p></p>
---------------
<h1 id="#title_17" >18、[前端] 探索 RxJS - 做一个 github 小应用</h1>
ecmadao
[http://gold.xitu.io/entry/58338f53570c350059e2efa4](http://gold.xitu.io/entry/58338f53570c350059e2efa4)
<img src="http://ac-mhke0kuv.clouddn.com/2875eab89fad8f563685.png?imageView/2/w/800/h/600/q/80/format/png"/><p>了解了 RxJS 的核心概念之后，本文就一步一步的来做一个基于 RxJS 和 github API 的 github 搜索工具。完成文中的案例，就相当于学习了一遍 RxJS 的 “Quick Start”，相信之后的场景和 Rx 应用大家也可以熟练应对。文中源码可见：https://github.com/ecmadao/rxjs-example</p><p></p>
---------------
<h1 id="#title_18" >19、FEX 技术周刊 - 2016/11/21</h1>

[http://fex.baidu.com/blog/2016/11/fex-weekly-21//](http://fex.baidu.com/blog/2016/11/fex-weekly-21//)
作者：zhangbobell <br> <p>微信搜索『FEX』关注我们的公众号，及时获得最新资讯。</p>

<h2 id="section">业界会议</h2>

<p><strong>Chrome Dev Summit 2016</strong><br />
https://blog.chromium.org/2016/11/chrome-dev-summit-2016-mobile-web-moves.html
https://developer.chrome.com/devsummit/
附   </p>

<p><strong>SDCC 2016中国软件开发者大会</strong><br />
http://sdcc.csdn.net/
可关注前端专场和微信开发专场。会议 PPT 下载： http://download.csdn.net/meeting/meeting_detail/23  </p>

<h2 id="section-1">深阅读</h2>

<p><strong>React v15.4.0</strong><br />
https://facebook.github.io/react/blog/2016/11/16/react-v15.4.0.html<br />
15.4.0 is a special release, and we would like to highlight a few notable changes in it:<br />
- Separating React and React DOM<br />
- Profiling Components with Chrome Timeline<br />
- Mocking Refs for Snapshot Testing  </p>

<p><strong>What Test Engineers do at Google: Building Test Infrastructure</strong><br />
https://testing.googleblog.com/2016/11/what-test-engineers-do-at-google.html<br />
In a recent post, we broadly talked about What Test Engineers do at Google. In this post, I talk about one aspect of the work TEs may do: building and improving test infrastructure to make engineers more productive.</p>

<p><strong>Node.js Garbage Collection Explained</strong><br />
https://blog.risingstack.com/node-js-at-scale-node-js-garbage-collection/<br />
In this article, you are going to learn how Node.js garbage collection works, what happens in the background when you write code and how memory is freed up for you.</p>

<p><strong>Not An Imposter: Fighting Front-End Fatigue</strong><br />
https://www.smashingmagazine.com/2016/11/not-an-imposter-fighting-front-end-fatigue/<br />
这几个观点挺不错的：<br />
- Get Your Fundamentals Locked In<br />
- You Don’t Need To Learn Everything<br />
- Most Companies Aren’t Using Bleeding Edge Tech <br />
- The More You Learn, The More You Discover You Don’t Know, And That’s Okay<br />
- Don’t Spend All Your Free Time Learning  </p>

<p><strong>You, Me And The Emoji: Character Sets, Encoding And Emoji</strong><br />
https://www.smashingmagazine.com/2016/11/character-sets-encoding-emoji/<br />
We all recognize emoji. They’ve become the global pop stars of digital communication. But what are they, technically speaking? And what might we learn by taking a closer look at these images, characters, pictographs… whatever they are. We will dig deep to learn about how these thingamajigs work.  </p>

<p><strong>Infoq- 双 11 技术专栏</strong>  </p>

<p><br />
学习下这场狂欢背后各家的关键技术。  </p>

<p><strong>Nodejs 线上服务稳定性保障体系</strong><br />
https://zhuanlan.zhihu.com/p/23778500<br />
来自大搜车的实践经验，本文会有条理的将我们团队在稳定性保障方面做的一些事情与大家分享，文中着重强调“线上”服务的保障，尽量不会涉及开发过程中的话题，改天会就开发过程的质量保障另外介绍。另外，我们在此方面也并非完全成熟，大家可以作为参考，但也许并非最佳实践，本文我会尽量讲我们的解决问题的思路，而不是最终如何执行。</p>

<p><strong>如何打造亚秒级页面加载速度的网店</strong>  </p>

<p><br />
良好的用户体验需要从三方面来实现：前端、网络，以及后端性能。前端性能在我们看来是最容易实现的，因为市面上已经有很多现成的工具以及各种最佳实践，照做很容易就能搞定。但依然有很多网站没有参照这些最佳实践，甚至完全没有对前端进行任何优化。网络性能是页面加载速度的最大影响因素，同时也是最难优化的。缓存和CDN是最有效的优化方法，但需要注意到，这些机制只能对静态内容进行优化。后端性能主要取决于单台服务器的性能以及分布式环境的规模。横向扩展非常难以实现，因此从一开始就要妥善考虑。很多项目将缩放能力和性能放在最后考虑，随着业务的增长最终将遇到非常棘手的问题。<br />
另附一篇性能强相关的文章：  </p>

<p><strong>Vue 的理念问题</strong><br />
https://zhuanlan.zhihu.com/p/23752826<br />
赞 Vue 作者的观点：Vue 有一个其他框架真的都没有的理念，同时也是我觉得真正关系到 Vue 的成功的一点，那就是『把高大上的思想变得平易近人』。每个喜欢 Vue 的用户，都会提到容易上手和文档友好。易用性不是偶然的，做到易用而强大也不是简单的事情。  </p>

<p><strong>Atom 背后的故事</strong>  </p>

<p><br />
Atom 是 GitHub 在 2014 年发布的一款基于 Web 技术构建的文本编辑器，我从 2014 年末开始使用 Atom 完成我的全部工作，对 Atom 很是喜爱，也创建了 Atom 的中文社区、翻译了一部分 Atom 的文档和博客。今天我将着重介绍 Atom 背后的故事，包括底层的 Electron、如何对 Atom 进行定制、Atom 的插件化机制、Atom 在启动速度和渲染性能方面的优化等。<br />
另附一篇 Electron 科普文：  </p>

<p><strong>Why AlloyFinger is so much smaller than hammerjs</strong><br />
http://www.cnblogs.com/iamzhanglei/p/6064325.html<br />
AlloyFinger 向国外社区介绍自己的文章。期待越来越多的国内类库走向世界。  </p>

<p><strong>React Native初探</strong><br />
http://www.cnblogs.com/yexiaochai/p/6042112.html<br />
挺全面的一个 RN 学习教程，还收录了很多资料。  </p>

<p><strong>Why I took October off from OSS volunteering</strong><br />
http://www.snarky.ca/why-i-took-october-off-from-oss-volunteering<br />
维护过不少开源项目的 FEX 成员表示深有感触  </p>

<p><strong>The Coming Revolution in Email Design</strong><br />
http://alistapart.com/article/the-coming-revolution-in-email-design<br />
Email, the web’s much maligned little cousin, is in the midst of a revolution—one that will change not only how designers and developers build HTML email campaigns, but also the way in which subscribers interact with those campaigns.  </p>

<p><strong>Choosing Ember over React in 2016</strong><br />
https://blog.instant2fa.com/choosing-ember-over-react-in-2016-41a2e7fd341#.7nirza98m<br />
One month ago, we started working on a new product: Instant 2FA, the easiest way to add two-factor authentication to any site in less than an hour. This blog post outlines our thinking behind choosing Ember (a technology none of us had ever used before) over React (which we’ve been running for 2.5 years in production at Clef) and our reflections on the decision after one month of work.  </p>

<p><strong>Write Reusable JavaScript Business Logic with peasy-js</strong><br />
https://www.sitepoint.com/reusable-javascript-business-logic-peasy-js/<br />
peasy-js makes it trivial to whimsically swap out UI, backend, and data frameworks in your applications by creating your business logic in a composable, reusable, scalable, and testable manner.  </p>

<p><strong>Abusing npm libraries for data exfiltration</strong><br />
https://blog.sourceclear.com/all-your-secrets-belong-to-us/<br />
In this blog post, we demonstrate how an attacker can use npm to exfiltrate information from the developer’s machine. Although we show the attack scenarios for npm, similar attacks can also be done on other package managers like gradle.  </p>

<p><strong>NodeJS Advanced - How to create a native add-on using C++</strong><br />
https://github.com/DAB0mB/node-distance-addon/blob/master/README.md<br />
In this tutorial we gonna go through the basics on how to write a native add-on to NodeJS using C++, one of the platform’s most powerful capabilities of which most web/JS developers now a days are not even familiar with.  </p>

<p><strong>Migrating to Jest</strong><br />
https://medium.com/@kentcdodds/migrating-to-jest-881f75366e7e#.t98xx6gqu<br />
Jest https://github.com/facebook/jest 在 PayPal 的实践。  </p>

<p><strong>How We Make Money at Stack Overflow: 2016 Edition</strong><br />
http://stackoverflow.blog/2016/11/How-We-Make-Money-at-Stack-Overflow-2016-Edition/<br />
可以了解下 stack overflow 的商业模式。  </p>

<p><strong>手机APP安装包缩减方案</strong><br />
http://tmq.qq.com/author/153906054/<br />
如何发现和优化体积  </p>

<p><strong>WebP原理和Android支持现状介绍</strong><br />
http://mp.weixin.qq.com/s?__biz=MzA3NTYzODYzMg==&amp;mid=2653578220&amp;idx=1&amp;sn=bdc57c640427984e240b19d8b9e10a15<br />
目前各大公司都已经使用了  </p>

<h2 id="section-2">新鲜货</h2>

<p><strong>Visual Studio Development – Introducing Visual Studio for Mac</strong><br />
https://msdn.microsoft.com/en-us/magazine/mt790182.aspx<br />
https://www.visualstudio.com/vs/visual-studio-for-mac/<br />
At Connect(); in November, Microsoft is launching a preview of Visual Studio for Mac. This is an exciting development, evolving the mobile-centric Xamarin Studio IDE into a true mobile-first, cloud-first development tool for .NET and C#, and bringing the Visual Studio development experience to the Mac. 同时，  </p>

<p><strong>Google Earth VR</strong>  </p>

<p><br />
https://blog.google/products/google-vr/google-earth-vr-bringing-whole-wide-world-virtual-reality/<br />
Google 发布了 Google Earth VR，效果很震撼。 </p>

<p><strong>**Next.js</strong><br />
https://github.com/zeit/next.js<br />
https://medium.com/javascript-mantra/next-js-53e9cf4da5af#.7vfoq7evi<br />
Next.js is a minimalistic framework for server-rendered React applications. 挺火的一个库，推出没多久 star 已经 6000 多了。其设计理念如下：<br />
- Zero setup. Use the filesystem as an API<br />
- Only JavaScript. Everything is a function<br />
- Automatic server rendering and code splitting<br />
- Data fetching is up to the developer<br />
- Anticipation is the key to performance<br />
- Simple deployment  </p>

<p><strong>mo.js</strong>  </p>

<p><br />
http://mojs.io/<br />
mo.js is a JavaScript library devoted to motion for the web. It offers a declarative syntax motion and the creation of elements for animation. Even though mo.js is still in beta, there is already a host of amazing features to play with.   </p>

<p><strong>Angular 2.2.0 Now Available</strong>  </p>

<p><br />
Angular version 2.2.0 - is now available. This is a minor release following our announced adoption of Semantic Versioning, meaning that it contains no breaking changes and that it is be a drop-in replacement for 2.1.x.  </p>

<p><strong>Clarity Design System</strong><br />
https://github.com/vmware/clarity<br />
UX guidelines, HTML/CSS framework, and Angular 2 components working together to craft exceptional experiences. 来自 vmware 的 UI 组件库。  </p>

<p><strong>Preact</strong><br />
https://github.com/developit/preact/<br />
Preact is a fast, 3kB alternative to React, with the same ES2015 API. Preact retains a large amount of compatibility with React, but only the modern (ES6 Classes and stateless functional components) interfaces. As one would expect coming from React, Components are simple building blocks for composing a User Interface.  </p>

<p><strong>Choo</strong><br />
https://github.com/yoshuawuyts/choo<br />
https://www.sitepoint.com/functional-programming-choo/<br />
choo cleanly structures internal data flow, so that all pieces of logic can be combined into a nice, cohesive machine. Internally all logic lives within models that contain several properties. subscriptions are functions that are called at startup and have send() passed in, so they act as read-only sources of data. effects react to changes, perform an action and can then post the results. reducers take data, modify it, and update the internal state.   </p>

<p><strong>Pino</strong>  </p>

<p><br />
http://www.nearform.com/nodecrunch/sematext-guest-post-pino-fastest-node-js-logger-production/<br />
Extremely fast node.js logger, inspired by Bunyan. It also includes a shell utility to pretty-print its log files.  </p>

<p><strong>Celery 4.0</strong>  </p>

<p><br />
Celery is a simple, flexible, and reliable distributed system to process vast amounts of messages, while providing operations with the tools required to maintain such a system. It’s a task queue with focus on real-time processing, while also supporting task scheduling.  </p>

<p><strong>The First Object Database for Node: Introducing Realm Node.js</strong><br />
https://realm.io/news/first-object-database-realm-node-js-server/<br />
At Realm, we’re very focused on mobile developers, and have built and open-sourced Realm Mobile Database versions for Swift, Objective-C, Java, Xamarin, and React Native. But today, we’re announcing something completely different: Realm Node.js. We’re pretty sure this is the first real object database for Node, and is available today on NPM as a free and fully open source repo – just run npm install –save realm.<br />
视频教程 https://egghead.io/lessons/node-js-use-realm-object-database-with-node-js  </p>

<p><strong>12 JavaScript libraries to watch in 2017</strong>  </p>

<p><br />
Most developers already know the big names like jQuery and React. But in this post I’d like to introduce twelve alternative JS libraries that are less well-known but rising rapidly. <br />
另附：  </p>

<p><strong>Clarity Design System</strong><br />
https://github.com/vmware/clarity<br />
UX guidelines, HTML/CSS framework, and Angular 2 components working together to craft exceptional experiences. 来自 vmware 的 UI 组件库。</p>

<p><strong>ChaosSocket</strong><br />
https://zzarcon.github.io/chaosocket/<br />
Chaosocket aims to provide you a set of tools to test this sort of behaviours, also it respects the WebSocket interface, making this transparent to you, this means that you don’t have to modify your code at all when you introduce the library in your app.   </p>

<p><strong>Running NodeJS on Linux on Windows</strong><br />
https://hackernoon.com/running-nodejs-on-linux-on-windows-88bd12993bae#.esg8xldwo<br />
介绍了 WSL  https://msdn.microsoft.com/en-us/commandline/wsl/about 给 windows 下 node 开发中的代来的便利  </p>

<p><strong>Best of Visual Studio Code: Features, Plugins, Acting Like Atom and Sublime</strong><br />
https://scotch.io/tutorials/best-of-visual-studio-code-features-plugins-acting-like-atom-and-sublime<br />
vscode 挺好用的，没用过的赶紧去体验下。  </p>

<h2 id="section-3">产品及其它</h2>

<p><strong>ICQ: 20 Years Is No Limit!</strong><br />
https://medium.com/@Dimitryophoto/icq-20-years-is-no-limit-8734e1eea8ea#.grm5dt7ql<br />
译文 http://mp.weixin.qq.com/s?__biz=MjM5NDUyOTAwOA==&amp;mid=2652913882&amp;idx=1&amp;sn=174c8d7803f99027aa805c4ab2aa2834<br />
ICQ is turning 20 (and that is no small potatoes). A whole generation has already grown up with the forerunner of all messengers. For this occasion, we have decided to take a retrospective look at how our technology developed over the past two decades.  </p>

<p><strong>技术债：the good, the bad, and the tao</strong><br />
http://mp.weixin.qq.com/s?__biz=MzA3NDM0ODQwMw==&amp;mid=2649827509&amp;idx=1&amp;sn=61a7adbeb49a105b9a22bae41614d07f<br />
技术债是每个技术团队都面临的问题，技术债并非洪水猛兽，我们要要合理控制，让其发挥债务的优势。作者这几个处理建议值得参考：<br />
- 拥抱 MVP。先解决温饱问题，再考虑还债。<br />
- 把技术债外包出去<br />
- 雇佣你所能获得的最优秀的人，给予她们你所能给予的，最能发挥她们能力的权限。<br />
- 拥抱匡威定律。你的组织架构决定了你的代码结构。想要快速独立的功能交付能力，你要有包含所有角色，拥有直接决策权的端到端的功能团队，而不是开发，测试，运维等彼此独立。<br />
- 在实现上可以多些负债，在接口上尽量减少负债。  </p>

<p><strong>虚幻与喧嚣，互联网时代真的要落幕了</strong><br />
http://mp.weixin.qq.com/s?__biz=MjM5OTM5OTAyMQ==&amp;mid=2654430480&amp;idx=1&amp;sn=c903fe8efd4301939b124a439e553871<br />
这个文章从对当前互联网的一些现象尤其是创业相关的分析还是挺值得看看的。  </p>

<p><strong>被忽略的交互设计本质</strong><br />
http://mp.weixin.qq.com/s?__biz=MTEwNTM0ODI0MQ==&amp;mid=2653433671&amp;idx=1&amp;sn=74acc467e43f3f73de73ae76f203ca7d<br />
谈论交互设计本质是起源于日常的很多谈论，不管是向朋友介绍自己从事“交互”相关岗位，还是需要向亲戚通过三言两语解释自己的工作内容；甚至在工作的上下游沟通中，也经常会被问道“你怎么就判断用户是这么想的”“产品如何从0（概念）到1（页面界面）的”；这些问题促使我想要追本溯源，捋顺一下交互的由来、工作内容，以及依照什么方法执行等问题。  </p>

<p><strong>稻盛和夫：除了拼命工作之外，不存在第二条通往成功的路</strong><br />
http://mp.weixin.qq.com/s?__biz=MzA5Mzk0NjQwOA==&amp;mid=2653198516&amp;idx=5&amp;sn=e9c76dc9c11f4a6fe8d00708ba63f51a<br />
当你每天都全身心投入工作时，低效的、漫不经心的现象就会消失。拼命工作可以磨练灵魂。人一旦有了闲暇，就会动起不正经的念头，干不正经的事。企业经营的根本意义和真正目的既不是圆技术者之梦，也不是肥经营者一己之私。经营者必须为员工的幸福殚精竭虑，必须超脱私心，让企业拥有大义名分。 “无论如何也要达成目标”这一愿望的强烈程度，正是事情成败的关键所在。  </p>

<p><strong>前 Facebook 副总裁：伟大的公司每六年出现一个，关键在于找到受限制资源</strong><br />
http://mp.weixin.qq.com/s?__biz=MzA5NzAzMjIxMw==&amp;mid=2650925567&amp;idx=3&amp;sn=4770ebfac8a8ea3f1ca48dc51bcd9ada<br />
当大家都在做记忆芯片，英特尔就做CPU；当大家都在拼命做PC的时候，微软就做操作系统；当大家都在做操作系统的时候，思科决定把所有电脑连接起来；当大家都在想着怎么样让电脑相互连接，谷歌想到的是如何组织机器之间的信息……结果他们都赢了。尽管公司主体不同，你会看到同一套规则在发生作用：找到受限制的资源并使之变得富足，是成就伟大企业的底层密码。  </p>
---------------
<h1 id="#title_19" >20、Javaslang 3.0之路</h1>
Michael Redlich
[http://www.infoq.com/cn/news/2016/11/the-road-to-javaslang-3?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2016/11/the-road-to-javaslang-3?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Javaslang是一个开源的函数式库，为Java 8及以上提供了持久化的数据类型和函数式的控制结构，最近，它发布了主版本3.0的路线图，承诺要对这个库进行比较明显的变更，移除不必要和废弃的特性。</p> <i>By Michael Redlich</i> <i> Translated by 张卫滨</i>
---------------
<h1 id="#title_20" >21、Logz.io提供了基于机器学习的日志分析</h1>
Hrishikesh Barua
[http://www.infoq.com/cn/news/2016/11/logzio-ml-log-analysis?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2016/11/logzio-ml-log-analysis?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p> Logz.io提供了一种智能日志分析的托管服务，该服务能够从人类与日志数据的交互中获得新的观点，这些日志数据包括技术论坛上的讨论内容和公共代码库。</p> <i>By Hrishikesh Barua</i> <i> Translated by Rays</i>
---------------
<h1 id="#title_21" >22、微软发布Asp.Net Core 1.1的第一个预览版本</h1>
Pierre-Luc Maheu
[http://www.infoq.com/cn/news/2016/11/aspnet-core-1-1-preview?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2016/11/aspnet-core-1-1-preview?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>微软最近发布了ASP.NET Core 1.1的预览版，这个版本包含了多个新的中间件组件、针对Windows的WebListener服务器、Razor视图编译以及Azure相关的特性。</p> <i>By Pierre-Luc Maheu</i> <i> Translated by 张卫滨</i>
---------------
<h1 id="#title_22" >23、WebAssembly浏览器预览版收集社区反馈</h1>
David Iffland
[http://www.infoq.com/cn/news/2016/11/webassembly-browser-preview?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2016/11/webassembly-browser-preview?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>即将面世的WebAssembly技术已经进入浏览器预览阶段，主要的浏览器厂商发布了与该语言兼容的稳定版本。它们希望社区使用它并提供相应的反馈。</p> <i>By David Iffland</i> <i> Translated by 王纯超</i>
---------------
<h1 id="#title_23" >24、2016企业开发趋势：Lightbend关于JVM开发者的调查</h1>
Michael Redlich
[http://www.infoq.com/cn/news/2016/11/lightbend-enterprise-survey-2016?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2016/11/lightbend-enterprise-survey-2016?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Lightbend最近调查了2100个JVM开发者来研究开发趋势和IT基础设施趋势之间的相互关系。成果发表在一篇白皮书中，显示微服务和轻量级容器在挑战重量级的J2EE应用服务器。</p> <i>By Michael Redlich</i> <i> Translated by 足下</i>
---------------
<h1 id="#title_24" >25、视频演讲： 宜信大数据金融应用在LAIN容器PaaS上的落地</h1>
孙毅
[http://www.infoq.com/cn/presentations/creditease-big-data-financial-app-in-lain-container-paas?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/creditease-big-data-financial-app-in-lain-container-paas?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/creditease-big-data-financial-app-in-lain-container-paas/zh/mediumimage/wangyi_270.jpg"/><p>在云计算不断发展的今天，原本传统的金融业也在追求高科技。为了改进原来的开发运维模式，不管是持续地发布自己的产品，还是稳定地维护应用，抑或是快速响应线上突发流量，都面临挑战。为了达到高效一体化运维，高质量快速持续交付，宜信大数据创新中心自研的基于容器技术的私有PaaS：LAIN。那LAIN到底基于什么样的背景，实现了什么样的特性，又有哪些技术难点？LAIN的落地对于宜信大数据的应用开发和运维带来了什么样的变革？LAIN项目负责人孙毅将分享宜信大数据金融应用在LAIN容器PaaS上的落地实践。</p> <i>By 孙毅</i>
---------------
<h1 id="#title_25" >26、视频演讲： 百鬼夜行の看不见的无线安全</h1>
杨哲
[http://www.infoq.com/cn/presentations/the-invisible-wireless-security?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/the-invisible-wireless-security?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/the-invisible-wireless-security/zh/mediumimage/yangzhe1_270.jpg"/><p>讲述目前暗流涌动的无线通信安全领域的真实现状，揭露无线 Hacking 技术，曝光多个重点行业的严重无线安全隐患。</p> <i>By 杨哲</i>
---------------
<h1 id="#title_26" >27、视频访谈： 黄桦：如何正确使用知识图谱</h1>
黄桦
[http://www.infoq.com/cn/interviews/interview-with-haunghua-talk-knowledge-mapping?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/interviews/interview-with-haunghua-talk-knowledge-mapping?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/interviews/interview-with-haunghua-talk-knowledge-mapping/zh/mediumimage/huanghua_270.jpg"/><p>我们在ArchSummit深圳大会的现场采访了明略数据的黄桦，他介绍了知识图谱在公安和金融领域落地的情况，遇到的困难和解决方案，分享了在技术选型，降低成本和保证系统准确性，实时性和安全性方面的经验，最后分享了明略未来的发展方向。</p> <i>By 黄桦</i>
---------------
<h1 id="#title_27" >28、文章： 从两个风格迥异的API平台说开去</h1>
刘志勇
[http://www.infoq.com/cn/articles/speaking-from-two-different-styles-api-platform?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/speaking-from-two-different-styles-api-platform?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/speaking-from-two-different-styles-api-platform/zh/smallimage/logo1.jpg"/><p>有人的地方就有江湖。有江湖的地方就有纷争。有纷争的地方就有是非。有是非的地方就有无奈。 自然，有API的地方就有app。</p> <i>By 刘志勇</i>
---------------
<h1 id="#title_28" >29、文章： 技术演讲三板斧：思路布局、全盘演练、临场把控</h1>
赵成
[http://www.infoq.com/cn/articles/three-axes-of-technical-presentation?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/three-axes-of-technical-presentation?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/three-axes-of-technical-presentation/zh/smallimage/xx_logo (2).jpg"/><p>本文来自一位InfoQ大会的明星讲师赵成，他在参加了一场演讲培训会之后，结合培训会所学和已有经验写下的一篇感想文。文中既有演讲内容准备的思路和方法论，还有台上临场时的细节把控，更有一些个人经历体会。</p> <i>By 赵成</i>
---------------
<h1 id="#title_29" >30、文章： 对话亚马逊一号员工Shel Kaphan</h1>
Craig Cannon
[http://www.infoq.com/cn/articles/talk-with-amazon-shel-kaphan?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/talk-with-amazon-shel-kaphan?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/talk-with-amazon-shel-kaphan/zh/smallimage/logo (20).jpg"/><p>Employee #1 是一个专注于分享科技公司早期员工背后故事的系列访谈。Shel Kaphan是亚马逊的一号员工。他目前正专注于个人兴趣，并且依然住在西雅图。</p> <i>By Craig Cannon</i> <i> Translated by NER</i>
---------------
<h1 id="#title_30" >31、视频演讲： 如何通过 APP+Wi-Fi 数据给企业做大数据精准用户画像</h1>
郭炜
[http://www.infoq.com/cn/presentations/how-to-use-app-wi-fi-data-to-accurate-user-portrait?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/how-to-use-app-wi-fi-data-to-accurate-user-portrait?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/how-to-use-app-wi-fi-data-to-accurate-user-portrait/zh/mediumimage/guowei_270.jpg"/><p>帮助传统企业或互联网企业通过线上线下数据融合，做到精准用户画像。简介用户画像基本方法，深入讨论基于移动用户线上线下相结合的方式建立用户画像的相关算法与实践。</p> <i>By 郭炜</i>
---------------
<h1 id="#title_31" >32、编辑精选：有关 Bluemix 的强大功能的最受欢迎教程</h1>

[http://www.ibm.com/developerworks/cn/cloud/library/cl-best-of-bluemix-tutorials-2016-trs/index.html?ca=drs-](http://www.ibm.com/developerworks/cn/cloud/library/cl-best-of-bluemix-tutorials-2016-trs/index.html?ca=drs-)
自从我上次汇编有关 IBM Bluemix 的最受欢迎 developerWorks
            教程列表以来，已过去几个月了，在这个行业（众所周知），几个月可能发生很多事情。所以是时候再总结一下了。但是，我想提供我自己的一些建议，而不是只收集我们网站上最受欢迎的内容。developerWorks
            非常幸运地拥有了丰富的主题专家，他们拥有深入的洞察力和写作技能，能够引导您掌握复杂的开发主题。以下是 5 篇出色地演示了 Bluemix
            的功能的最新教程。了解您如何才能以创新（且有趣）的新方法利用 IBM 的云平台。尽情畅享吧！
---------------
<h1 id="#title_32" >33、[前端] 最全的资源教程：前端涉及的所有知识体系</h1>
IT程序狮
[http://gold.xitu.io/entry/58338e5f5c497d006b2a77b1](http://gold.xitu.io/entry/58338e5f5c497d006b2a77b1)
<img src="http://ac-mhke0kuv.clouddn.com/1d3a488ab0793da57866.jpg?imageView/2/w/800/h/600/q/80/format/png"/><p>本文作者总结了一个前端开发最全的资源、教程列表。涵盖前端知识体系、知识结构、图书推荐以及入门视频教程，全的简直不要不要的了。推荐收藏！</p><p></p>
---------------
<h1 id="#title_33" >34、Spotify Playlists To Fuel Your Coding And Design Sessions</h1>
Cosima Mielke
[https://www.smashingmagazine.com/2016/11/playlists-fuel-coding-design-sessions/](https://www.smashingmagazine.com/2016/11/playlists-fuel-coding-design-sessions/)
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
</table><p>Some like it loud, others need some steady beats to stay focused, others calm tunes. A while ago we  what music the web community is listening to when coding and designing.</p>

<figure></figure>

<p>The answers were as diverse as the community itself and certainly too good to live an existence only in a Twitter discussion. That’s why we’ve compiled those hand-crafted playlists, favorite artists, and loved soundtracks in this article to see <strong>which tunes fuel the web</strong>, and, well, first and foremost, to provide you with some new ear candy to get you through lengthy coding and design sessions, of course. Get your headphones ready!</p><p>The post .</p>
---------------