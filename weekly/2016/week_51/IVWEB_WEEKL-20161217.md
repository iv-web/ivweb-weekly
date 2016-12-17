## 文章索引
1、 <a href="#1前端-react-native-的组件通信方式" >[前端] React Native 的组件通信方式</a><br/>
2、 <a href="#2前端-vuejs-20-迁移指南" >[前端] Vue.js 2.0 迁移指南</a><br/>
3、 <a href="#3译配置一个简单而实用的-javascript-开发环境" >【译】配置一个简单而实用的 JavaScript 开发环境</a><br/>
4、 <a href="#4前端-奇舞周刊第-189-期" >[前端] 奇舞周刊第 189 期</a><br/>
5、 <a href="#5后端-spring-cloud-netflix-概览和架构设计-|-掘金技术征文" >[后端] Spring Cloud netflix 概览和架构设计 | 掘金技术征文</a><br/>
6、 <a href="#6银联实验室发布金融sdn技术能力评测标准草案" >银联实验室发布《金融SDN技术能力评测标准》草案</a><br/>
7、 <a href="#7文章-解读2016之golang篇极速提升逐步超越" >文章： 解读2016之Golang篇：极速提升，逐步超越</a><br/>
8、 <a href="#8web-development-reading-list-#163:-the-end-of-year-wrap-up" >Web Development Reading List #163: The End-Of-Year Wrap-Up</a><br/>
9、 <a href="#9解放双手发掘更大的价值智能化运维" >解放双手，发掘更大的价值：智能化运维</a><br/>
10、 <a href="#10ios-ios-图像处理---一种高效裁剪图片圆角的算法" >[iOS] [iOS] 图像处理 - 一种高效裁剪图片圆角的算法</a><br/>
11、 <a href="#11最新java-9时间表看上去自开始就存在风险" >最新Java 9时间表看上去自开始就存在风险</a><br/>
12、 <a href="#12android-有几个基类-用dagger注入几个工具类就敢叫mvp+dagger框架" >[Android] 有几个基类, 用Dagger注入几个工具类就敢叫MVP+Dagger框架？</a><br/>
13、 <a href="#13ios-开发周报-苹果公布-2016-年度-app-&-游戏榜单到年底了为什么不在-ios-上尝试-rex-呢" >iOS 开发周报： 苹果公布 2016 年度 App & 游戏榜单、到年底了，为什么不在 iOS 上尝试 ReX 呢？</a><br/>
14、 <a href="#14android开发周报谷歌开发者大会在京召开android秒级编译详解" >Android开发周报：谷歌开发者大会在京召开、Android秒级编译详解</a><br/>
15、 <a href="#15android-启航---设计模式与-android-源码-篇二" >[Android] 启航 - 设计模式与 Android 源码 (篇二)</a><br/>
16、 <a href="#16mistakes-developers-make-when-learning-design" >Mistakes Developers Make When Learning Design</a><br/><h1 id="#title_0" >1、[前端] React Native 的组件通信方式</h1>
涂鸦码龙
[https://gold.xitu.io/entry/5853ef171b69e6006c888d75](https://gold.xitu.io/entry/5853ef171b69e6006c888d75)
<p>React Native 的组件通信方式</p><p></p>
---------------
<h1 id="#title_1" >2、[前端] Vue.js 2.0 迁移指南</h1>
小芋头君
[https://gold.xitu.io/entry/5853bf7761ff4b0063ad13cd](https://gold.xitu.io/entry/5853bf7761ff4b0063ad13cd)
<img src="https://dn-mhke0kuv.qbox.me/eb357a1f54e09966a68d.png?imageView/2/w/800/h/600/q/80/format/png"/><p>大搜车前端团队的一点点实践总结</p><p></p>
---------------
<h1 id="#title_2" >3、【译】配置一个简单而实用的 JavaScript 开发环境</h1>

[https://www.h5jun.com/post/setting-up-a-minimal-yet-useful-javascript-dev-environment.html](https://www.h5jun.com/post/setting-up-a-minimal-yet-useful-javascript-dev-environment.html)
<blockquote>
<p>原文：</p>
</blockquote>
<p>在一个框架、库和工具无处不在的时代，可能很多人都会面临选择困难症。</p>
<p><img src="https://p4.ssl.qhimg.com/t0144189b90ad8c0926.jpg" alt=""></p>
<!--more-->
<p>根据我的经验，写一个模块或 CLI 工具前你所要做的第一件事就是设置一个开发环境。对这个步骤有人喜欢有人愁。但不管怎样，它可能总是花掉你很多时间，你得不停地调整你配置的方方面面。</p>
<p>当然，你可能使用 webpack、eslint、jasmine 甚至是 TypeScript（而最终可能只换来“很棒”的编译错误信息）。事实上，大部分情况下，作为开发者，我们可以使用一些几乎不用配置的工具。通常来说，这些“开箱即用”的工具是完全可以接受的，并将帮助我们直接解决问题，同时还能提供几乎实时的反馈闭环。</p>
<p>当我们谈论最小化配置，我们最关注的是测试、代码规范检查、监控文件内容改变以及确保你在提交代码前没搞砸前面这些点。</p>
<p>下面是一个帮助你用五分钟或者更少的时间（取决于 NPM 的心情^^）一步步从无到有建立开发环境的步骤：</p>
<h2 id="-node-js-git-">初始化 Node.js 项目和 Git 仓库</h2>
<pre><code class="hljs lang-crystal"><span class="hljs-comment"># Create a directory and cd into it (#protip – $_ holds argument of your last command)</span>
$ mkdir awesome-<span class="hljs-class"><span class="hljs-keyword">module</span> &amp;&amp; <span class="hljs-title">cd</span> $<span class="hljs-title">_</span></span>

<span class="hljs-comment"># Initialize Node.js project with default settings</span>
$ npm init --yes

<span class="hljs-comment"># Create initial folders and files</span>
$ mkdir <span class="hljs-class"><span class="hljs-keyword">lib</span> <span class="hljs-title">test</span></span>
$ touch index.js <span class="hljs-class"><span class="hljs-keyword">lib</span>/<span class="hljs-title">meaningOfLife</span>.<span class="hljs-title">js</span> <span class="hljs-title">test</span>/<span class="hljs-title">index</span>.<span class="hljs-title">test</span>.<span class="hljs-title">js</span> <span class="hljs-title">test</span>/<span class="hljs-title">meaningOfLife</span>.<span class="hljs-title">test</span>.<span class="hljs-title">js</span></span>

<span class="hljs-comment"># Initialize GIT repository and create initial commit</span>
$ git init
$ git add -A; git commit -am <span class="hljs-string">"Awesome Module, day one"</span>
</code></pre><h2 id="-">安装工具</h2>
<p>在这里，我们将使用四个简单的模块，每个模块完成一件事。 负责自动运行 npm 脚本。</p>
<p>为什么选择这几个工具？因为它们不需要任何配置即符合我们使用者的思维习惯。这样少一件事情（指修改配置）需要思考和担心。</p>
<pre><code class="hljs lang-q">$ npm i --<span class="hljs-built_in">save</span>-<span class="hljs-built_in">dev</span> ava standard chokidar-cli precommit-hook
</code></pre><p>记得创建 <code>.gitignore</code> 文件并添加 <code>node_modules</code> 目录到文件中！我们不需要将依赖的库提交到我们的代码仓库里。</p>
<h2 id="-">配置工具</h2>
<p>打开 <code>package.json</code> 并添加这些脚本到你的文件：</p>
<pre><code class="hljs lang-gherkin"><span class="hljs-string">"scripts"</span>:  {
  <span class="hljs-string">"test"</span>:  <span class="hljs-string">"ava"</span>,
  <span class="hljs-string">"lint"</span>:  <span class="hljs-string">"standard"</span>,
  <span class="hljs-string">"dev"</span>:  <span class="hljs-string">"chokidar "</span><span class="hljs-keyword">*</span><span class="hljs-keyword">*</span>/<span class="hljs-keyword">*</span>.js<span class="hljs-string">" -c "</span>standard &amp;&amp; ava<span class="hljs-string">""</span>
},
<span class="hljs-string">"pre-commit"</span>:  [<span class="hljs-string">"test"</span>,  <span class="hljs-string">"lint"</span>],
</code></pre><p>就这样，一切都搞定了！一旦你运行 <code>npm run dev</code> ，所有的 JS 都会通过 Standard.js 进行规范检查，并通过 Ava 进行单元测试。不用额外做别的什么了，你现在就可以开始你的工作。</p>
<p>同样，提交 Git 提交时，这些脚本也会被自动运行。除非你的测试和代码检查都通过，否则你无法提交代码。</p>
<p>两件值得注意的事：</p>
<ol>
<li>你无须安装 <code>standard</code> 或 <code>ava</code> 到你的系统全局域下，因为它们可以从 <code>node</code> 上下文里执行。</li>
<li>因为我们使用 <code>&amp;&amp;</code> 代替 <code>j</code>，在 <code>dev</code> 脚本里，单元测试在代码检查未通过前不会被触发。这让反馈闭环更快（即避免无谓的测试消耗时间）。</li>
</ol>
<h2 id="-">用这个配置工作</h2>
<p>因为环境假定你使用 TDD（测试驱动开发）方式工作（你可能应该这么做！），一但你运行你的 <code>dev</code> 脚本，你可以创建测试并且将它们添加到测试用例集中，不需要重启监控程序或者重新构建。</p>
<p>让我们创建第一个测试文件：</p>
<pre><code class="hljs lang-coffeescript"><span class="hljs-regexp">//</span> test/meaningOfLife.test.js
const test = <span class="hljs-built_in">require</span>(<span class="hljs-string">"ava"</span>)
const meaningOfLife = <span class="hljs-built_in">require</span>(<span class="hljs-string">"../lib/meaningOfLife"</span>)

test(<span class="hljs-string">"Real meaning of life"</span>, <span class="hljs-function"><span class="hljs-params">(t)</span> =&gt;</span> {
  t.<span class="hljs-keyword">is</span>(meaningOfLife(), <span class="hljs-number">42</span>)
})
</code></pre><p>一但你保存文件，你会立即发现你的一个测试用例未通过，让我们来修复它：</p>
<pre><code class="hljs lang-coffeescript"><span class="hljs-regexp">//</span> lib/meaningOfLife.js
<span class="hljs-built_in">module</span>.exports = <span class="hljs-function"><span class="hljs-params">()</span> =&gt;</span> <span class="hljs-number">42</span>
</code></pre><p>好，现在测试通过了！就是这么简单。让我们创建另一个模块，它接受一个数值参数，让它的值加倍，然后对这个模块进行单元测试，看看是否它与我们的“生命的意义”模块能够很好地集成到一起（注意，到这里已经是集成测试，而不是单元测试！）。</p>
<pre><code class="hljs lang-typescript"><span class="hljs-comment">// lib/multiply.js</span>
<span class="hljs-keyword">module</span>.exports = (number) =&gt; {
  <span class="hljs-keyword">if</span> (<span class="hljs-keyword">typeof</span> <span class="hljs-built_in">number</span> !== <span class="hljs-string">"number"</span>) <span class="hljs-keyword">throw</span> <span class="hljs-keyword">new</span> <span class="hljs-built_in">TypeError</span>(<span class="hljs-string">"Only numbers can be multiplied!"</span>)
  <span class="hljs-keyword">return</span> <span class="hljs-built_in">number</span> * <span class="hljs-number">2</span>
}
</code></pre><pre><code class="hljs lang-coffeescript"><span class="hljs-regexp">//</span> test/multiply.test.js
const test = <span class="hljs-built_in">require</span>(<span class="hljs-string">"ava"</span>)
const multiply = <span class="hljs-built_in">require</span>(<span class="hljs-string">"../lib/multiply"</span>)

test(<span class="hljs-string">"Can multiply numbers"</span>, <span class="hljs-function"><span class="hljs-params">(t)</span> =&gt;</span> {
  t.<span class="hljs-keyword">is</span>(multiply(<span class="hljs-number">10</span>), <span class="hljs-number">20</span>)
})

test(<span class="hljs-string">"Throws when you try to multiply non-number value"</span>, <span class="hljs-function"><span class="hljs-params">(t)</span> =&gt;</span> {
  t.throws(<span class="hljs-function"><span class="hljs-params">()</span> =&gt;</span> multiply(<span class="hljs-string">"ohai!"</span>), <span class="hljs-string">"Only numbers can be multiplied!"</span>)
})
</code></pre><p>现在，让我们把两者放在一次测试:</p>
<pre><code class="hljs lang-coffeescript"><span class="hljs-regexp">//</span> test/index.test.js
const test = <span class="hljs-built_in">require</span>(<span class="hljs-string">"ava"</span>)
const awesomeModule = <span class="hljs-built_in">require</span>(<span class="hljs-string">"../index"</span>)

test(<span class="hljs-string">"Works nicely together"</span>, <span class="hljs-function"><span class="hljs-params">(t)</span> =&gt;</span> {
  t.<span class="hljs-keyword">is</span>(awesomeModule(), <span class="hljs-number">84</span>)
})
</code></pre><pre><code class="hljs lang-coffeescript"><span class="hljs-regexp">//</span> index.js
const meaningOfLife = <span class="hljs-built_in">require</span>(<span class="hljs-string">"./lib/meaningOfLife"</span>)
const multiply = <span class="hljs-built_in">require</span>(<span class="hljs-string">"./lib/multiply"</span>)

<span class="hljs-built_in">module</span>.exports = <span class="hljs-function"><span class="hljs-params">()</span> =&gt;</span> multiply(meaningOfLife())
</code></pre><p>它没问题！只需要几分钟时间，我们就可以让一切就绪。</p>
<p>我们作为开发者，经常被闪闪发光的新工具迷住。我们似乎忘记了那些工具本来应该让我们工作得更轻松、更快速和不容易出错。通常情况，最简单的解决方案就足够了。与其花费大量的时间在配置环境上，不如将时间花在编写软件本身上。而遵循上面的步骤将让你可以达到这一目的。</p>
<p>一但你的项目开始增长，你可能会发现自己需要引入一些更复杂的东西。然而，在大部分情况下，这一问题不会出现。上面那些工具会在很长很长一段时间内符合你的需求。</p>
<blockquote>
<p>英文原文：</p>
</blockquote>
---------------
<h1 id="#title_3" >4、[前端] 奇舞周刊第 189 期</h1>
文蔺
[https://gold.xitu.io/entry/5853c04d128fe10069886338](https://gold.xitu.io/entry/5853c04d128fe10069886338)
<p>【前端周刊】奇舞周刊第 189 期 。</p><p></p>
---------------
<h1 id="#title_4" >5、[后端] Spring Cloud netflix 概览和架构设计 | 掘金技术征文</h1>
mavlarn
[https://gold.xitu.io/entry/5853de3661ff4b00684c9a7f](https://gold.xitu.io/entry/5853de3661ff4b00684c9a7f)
<img src="https://dn-mhke0kuv.qbox.me/90b8690df7e2f4c5cd11.png?imageView/2/w/800/h/600/q/80/format/png"/><p>Spring Cloud Netflix 是专门用于开发微服务的框架，提供了服务发现、断路器和监控、智能路由、客户端负载均衡等组件。本文从整体上介绍了该框架、各个组件、关系、部署等方面的问题。文末还针对本人实践中遇到的问题做了一些说明。</p><p></p>
---------------
<h1 id="#title_5" >6、银联实验室发布《金融SDN技术能力评测标准》草案</h1>
杨赛
[http://www.infoq.com/cn/news/2016/12/UnionPay-financial-SDN-draft?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2016/12/UnionPay-financial-SDN-draft?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>2016年10月21日，由中国银联电子商务与电子支付国家工程实验室牵头发起的《金融SDN技术能力评测标准》通过了中国通信标准化协会（CCSA）立项。</p> <i>By 杨赛</i>
---------------
<h1 id="#title_6" >7、文章： 解读2016之Golang篇：极速提升，逐步超越</h1>
郝林
[http://www.infoq.com/cn/articles/2016-review-go?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/2016-review-go?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/2016-review-go/zh/smallimage/logo (22).jpg"/><p>Go语言已经7岁了！今年8月，Go 1.7如期发布。撰写本稿时，Go 1.8的测试版也出来了。我们正在热切盼望着明年2月的Go 1.8正式版。</p> <i>By 郝林</i>
---------------
<h1 id="#title_7" >8、Web Development Reading List #163: The End-Of-Year Wrap-Up</h1>
Anselm Hannemann
[https://www.smashingmagazine.com/2016/12/web-development-reading-list-163/](https://www.smashingmagazine.com/2016/12/web-development-reading-list-163/)
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
</table><p>Only one week left until Christmas, and people already start freaking out again. No gifts purchased yet, work isn’t finished either, and suddenly some budget has to be spent until the end of the year. All of this <strong>puts us under pressure</strong>. To avoid the stress, I’ve seen a lot of people take a vacation from now until the end of the year — probably a good idea.</p>
<figure></figure>
<p>And while it’s nice to see so many web advent calendars, I feel like <strong>I’ve never written a longer reading list</strong> than this one. So save this edition if you don’t have much time currently and read it during some calm moments later this year or early next year. Most articles are still worth reading in a few weeks.</p><p>The post .</p>
---------------
<h1 id="#title_8" >9、解放双手，发掘更大的价值：智能化运维</h1>
孟夕
[http://www.infoq.com/cn/news/2016/12/Intelligent-operation?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2016/12/Intelligent-operation?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>目前业界真正的智能化运维的落地实践其实并不多，大多还是停留在自动化甚至人工化阶段，然而智能化运维是大势所趋，对于大公司来说，更是尤为重要。阿里大数据SRE团队历时2年时间完成了Tesla这一智能化运维体系的设计、开发和落地。基于此，我们采访了阿里Tesla体系负责人熊胜（池枫），希望能带给大家对智能化运维的一些新的思考。</p> <i>By  孟夕</i>
---------------
<h1 id="#title_9" >10、[iOS] [iOS] 图像处理 - 一种高效裁剪图片圆角的算法</h1>
androidwing
[https://gold.xitu.io/entry/5853bb16b123db0065635bea](https://gold.xitu.io/entry/5853bb16b123db0065635bea)
<p>经常看到各种高效裁剪圆角的文章，正好之前做过一点数字图像处理，就打算用空域处理的办法，写个裁剪圆角的算法，一定要尽可能的快的，不然界面容易卡顿。</p><p></p>
---------------
<h1 id="#title_10" >11、最新Java 9时间表看上去自开始就存在风险</h1>
Abraham Marín Pérez
[http://www.infoq.com/cn/news/2016/12/java9-latest-schedule-at-risk?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2016/12/java9-latest-schedule-at-risk?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>在进入特性扩展流程的审批阶段后，Oracle确认将于2017年9月发布Java 9。正如InfoQ在之前所给出的预测，新时间表为特性扩展给出了更长的等待时间，这影响了测试过程，进而可能会引发风险。</p> <i>By Abraham Marín Pérez</i> <i> Translated by Rays</i>
---------------
<h1 id="#title_11" >12、[Android] 有几个基类, 用Dagger注入几个工具类就敢叫MVP+Dagger框架？</h1>
jessyan
[https://gold.xitu.io/entry/5853d4bf8e450a006c563530](https://gold.xitu.io/entry/5853d4bf8e450a006c563530)
<img src="https://dn-mhke0kuv.qbox.me/811d7d01263e805b066e.jpg?imageView/2/w/800/h/600/q/80/format/png"/><p>仅仅有几个基类, 仅仅用Dagger注入几个工具类就敢叫MVP+Dagger+Retrofit+Rxjava框架？</p><p></p>
---------------
<h1 id="#title_12" >13、iOS 开发周报： 苹果公布 2016 年度 App & 游戏榜单、到年底了，为什么不在 iOS 上尝试 ReX 呢？</h1>
靛青K
[http://www.infoq.com/cn/news/2016/12/Mobile-Weekly-apple-2016-app-gam?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2016/12/Mobile-Weekly-apple-2016-app-gam?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>苹果公布 2016 年度 App & 游戏榜单、到年底了，为什么不在 iOS 上尝试 ReX 呢？</p> <i>By 靛青K</i>
---------------
<h1 id="#title_13" >14、Android开发周报：谷歌开发者大会在京召开、Android秒级编译详解</h1>
郭亮
[http://www.infoq.com/cn/news/2016/12/Android-weekly-Google-IO-beijing?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2016/12/Android-weekly-Google-IO-beijing?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>2016年谷歌开发者大会在北京国家会议中心举办。本次大会内容主要面向中国开发者，帮助他们的App走出中国，谷歌也希望通过应用开发和分发平台为中国Android开发者创收。本期周报为大家带来了增量编译详解、MultiDex工作原理、OpenSL ES等方面的技术干货，欢迎阅读。</p> <i>By 郭亮</i>
---------------
<h1 id="#title_14" >15、[Android] 启航 - 设计模式与 Android 源码 (篇二)</h1>
szysky
[https://gold.xitu.io/entry/5853bce0570c350069ed91e2](https://gold.xitu.io/entry/5853bce0570c350069ed91e2)
<img src="https://dn-mhke0kuv.qbox.me/e9af25f9f0990d1e62e5.jpg?imageView/2/w/800/h/600/q/80/format/png"/><p>做一个会设计的 Coder</p><p></p>
---------------
<h1 id="#title_15" >16、Mistakes Developers Make When Learning Design</h1>
Mason Gentry
[https://www.smashingmagazine.com/2016/12/mistakes-developers-make-when-learning-design/](https://www.smashingmagazine.com/2016/12/mistakes-developers-make-when-learning-design/)
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
</table><p>The blank Photoshop document glows in front of you. You've been trying to design a website for an hour but it's going nowhere. <strong>You feel defeated</strong>. You were in this same predicament last month when you couldn't design a website for a project at work. As a developer, you just feel out of your element pushing pixels around.</p>

<figure></figure>

<p>How do designers do it? Do they just mess around in Photoshop or Sketch for a while until a pretty design appears? Can developers who are used to working within the logical constructs of Boolean logic and number theory master the seemingly arbitrary rules of design?</p><p>The post .</p>
---------------