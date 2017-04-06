## 文章索引
1、 <a href="#1css-in-js-简介" >CSS in JS 简介</a><br/>
2、 <a href="#2creating-one-browser-extension-for-all-browsers:-edge-chrome-firefox-opera-brave-and-vivaldi" >Creating One Browser Extension For All Browsers: Edge, Chrome, Firefox, Opera, Brave And Vivaldi</a><br/>
3、 <a href="#3文章-微服务可靠性设计" >文章： 微服务可靠性设计</a><br/>
4、 <a href="#4文章-如何基于openstack-telemetry项目实现云监控报警服务" >文章： 如何基于Openstack telemetry项目实现云监控报警服务</a><br/>
5、 <a href="#5文章-数据驱动在链家网搜索优化与推荐策略中的实践" >文章： 数据驱动在链家网搜索优化与推荐策略中的实践</a><br/>
6、 <a href="#6视频演讲-如何深度融合搜索和推荐兴趣引擎架构设计" >视频演讲： 如何深度融合搜索和推荐：兴趣引擎架构设计</a><br/>
7、 <a href="#7每月亿行代码全球数万研发落地devops的协同平台devcloud" >每月亿行代码、全球数万研发，落地DevOps的协同平台DevCloud</a><br/>
8、 <a href="#8swift-31改进了语言包管理器和linux实现" >Swift 3.1改进了语言、包管理器和Linux实现</a><br/>
9、 <a href="#9fex-技术周刊---2017/04/05" >FEX 技术周刊 - 2017/04/05</a><br/>
10、 <a href="#10ibm发布了自己的区块链即服务" >IBM发布了自己的区块链即服务</a><br/>
11、 <a href="#11buurtzorg通向teal组织的敏捷之旅" >Buurtzorg通向Teal组织的敏捷之旅</a><br/>
12、 <a href="#12visual-studio-2017迎来f#-41" >Visual Studio 2017迎来F# 4.1</a><br/>
13、 <a href="#13google-cloud-next会议摘要" >Google Cloud Next会议摘要</a><br/>
14、 <a href="#14首届商业敏捷大会圆满落幕" >首届商业敏捷大会圆满落幕</a><br/>
15、 <a href="#15redis之父10x程序员应该具备哪些素质" >Redis之父：10x程序员应该具备哪些素质</a><br/>
16、 <a href="#16周末的时间我们在github用什么语言编程" >周末的时间，我们在GitHub用什么语言编程？</a><br/>
17、 <a href="#17gitlab-9提供了子群组部署面板和集成监控" >GitLab 9提供了子群组、部署面板和集成监控</a><br/><h1 id="#title_0" >1、CSS in JS 简介</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2017/04/css_in_js.html](http://www.ruanyifeng.com/blog/2017/04/css_in_js.html)
<p>1、</p>

<p>以前，网页开发有一个原则，叫做（separation of concerns）。</p>

        <p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017040604.jpg" alt="" title="" /></p>

<p>它的意思是，各种技术只负责自己的领域，不要混合在一起，形成耦合。对于网页开发来说，主要是三种技术分离。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017040605.jpg" alt="" title="" /></p>

<blockquote>
  <ul>
<li>HTML 语言：负责网页的结构，又称语义层</li>
<li>CSS 语言：负责网页的样式，又称视觉层</li>
<li>JavaScript 语言：负责网页的逻辑和交互，又称逻辑层或交互层</li>
</ul>
</blockquote>

<p>简单说，就是一句话，不要写"行内样式"（inline style）和"行内脚本"（inline script）。比如，下面代码就很糟糕（查看）。</p>

<blockquote><pre><code class="language-markup">
&lt;h1 style="color:red;font-size:46px;"  onclick="alert('Hi')">
  Hello World
&lt;/h1>
</code></pre></blockquote>

<p>2、</p>

<p> 出现以后，这个原则不再适用了。因为，React 是组件结构，强制要求把 HTML、CSS、JavaScript 写在一起。</p>

<p>上面的例子使用 React 改写如下（查看）。</p>

<blockquote><pre><code class="language-javascript">
const style = {
  'color': 'red',
  'fontSize': '46px'
};

const clickHandler = () => alert('hi'); 

ReactDOM.render(
  &lt;h1 style={style} onclick={clickHandler}>
     Hello, world!
  &lt;/h1>,
  document.getElementById('example')
);
</code></pre></blockquote>

<p>上面代码在一个文件里面，封装了结构、样式和逻辑，完全违背了"关注点分离"的原则，很多人不适应。</p>

<p>但是，这有利于组件的隔离。每个组件包含了所有需要用到的代码，不依赖外部，组件之间没有耦合，很方便复用。所以，随着 React 的走红和组件模式深入人心，这种"关注点混合"的新写法逐渐成为主流。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017040601.png" alt="" title="" /></p>

<p>3、</p>

<p>表面上，React 的写法是 HTML、CSS、JavaScript 混合在一起。但是，实际上不是。现在其实是用 JavaScript 在写 HTML 和 CSS。</p>

<p>React 在 JavaScript 里面实现了对 HTML 和 CSS 的封装，我们通过封装去操作 HTML 和 CSS。也就是说，网页的结构和样式都通过 JavaScript 操作。</p>

<p>4、</p>

<p>React 对 HTML 的封装是  ，这个在各种 React 教程都有详细介绍，本文不再涉及了，下面来看 React 对 CSS 的封装。</p>

<p>React 对 CSS 封装非常简单，就是沿用了 DOM 的 ，这个在前面已经看到过了。</p>

<blockquote><pre><code class="language-javascript">
const style = {
  'color': 'red',
  'fontSize': '46px'
};
</code></pre></blockquote>

<p>上面代码中，CSS 的<code>font-size</code>属性要写成<code>fontSize</code>，这是 JavaScript 操作 CSS 属性的。</p>

<p>由于 CSS 的封装非常弱，导致了一系列的第三方库，用来加强 React 的 CSS 操作。它们统称为 CSS in JS，意思就是使用 JS 语言写 CSS。根据不完全统计，各种 CSS in JS 的库至少有。老实说，现在也看不出来，哪一个库会变成主流。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017040602.jpg" alt="" title="" /></p>

<p>你可能会问，它们与"CSS 预处理器"（比如 Less 和 ，包括 PostCSS）有什么区别？回答是 CSS in JS 使用 JavaScript 的语法，是 JavaScript 脚本的一部分，不用从头学习一套专用的 API，也不会多一道编译步骤。</p>

<p>5、</p>

<p>上周，我看到一个新的 CSS in JS 库，叫做 。它将一些常用的 CSS 属性封装成函数，用起来非常方便，充分体现使用 JavaScript 语言写 CSS 的优势。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017040606.png" alt="" title="" /></p>

<p>我觉得这个库很值得推荐，这篇文章的主要目的，就是想从这个库来看怎么使用 CSS in JS。</p>

<p>首先，加载 polished.js。</p>

<blockquote><pre><code class="language-javascript">
const polished = require('polished');
</code></pre></blockquote>

<p>如果是浏览器，插入下面的脚本。</p>

<blockquote><pre><code class="language-markup">
&lt;script src="https://unpkg.com/polished@1.0.0/dist/polished.min.js">
&lt;/script>
</code></pre></blockquote>

<p><code>polished.js</code>目前有50多个方法，比如<code>clearfix</code>方法用来清理浮动。</p>

<blockquote><pre><code class="language-javascript">
const styles = {
  ...polished.clearFix(),
};
</code></pre></blockquote>

<p>上面代码中，<code>clearFix</code>就是一个普通的 JavaScript 函数，返回一个对象。</p>

<blockquote><pre><code class="language-javascript">
polished.clearFix()
// {
//  &::after: {
//    clear: "both",
//    content: "",
//    display: "table"
//  }
// }
</code></pre></blockquote>

<p>"展开运算符"（<code>...</code>）将<code>clearFix</code>返回的对象展开，便于与其他 CSS 属性混合。然后，将样式对象赋给 React 组件的<code>style</code>属性，这个组件就能清理浮动了。</p>

<blockquote><pre><code class="language-javascript">
ReactDOM.render(
  &lt;h1 style={style}>Hello, React!&lt;/h1>,
  document.getElementById('example')
);
</code></pre></blockquote>

<p>从这个例子，大家应该能够体会<code>polished.js</code>的用法。</p>

<p>6、</p>

<p>下面再看几个很有用的函数。</p>

<p><code>ellipsis</code>将超过指定长度的文本，使用省略号替代（查看）。</p>

<blockquote><pre><code class="language-javascript">
const styles = {
  ...polished.ellipsis('200px')
}

// 返回值
// {
//   'display': 'inline-block',
//   'max-width': '250px',
//   'overflow': 'hidden',
//   'text-overflow': 'ellipsis',
//   'white-space': 'nowrap',
//   'word-wrap': 'normal'
// }
</code></pre></blockquote>

<p><code>hideText</code>用于隐藏文本，显示图片。</p>

<blockquote><pre><code class="language-javascript">
const styles = {
  'background-image': 'url(logo.png)',
  ...polished.hideText(),
};

// 返回值
// {
  'background-image': 'url(logo.png)',
  'text-indent': '101%',
  'overflow': 'hidden',
  'white-space': 'nowrap',
}
</code></pre></blockquote>

<p><code>hiDPI</code>指定高分屏样式。</p>

<blockquote><pre><code class="language-javascript">
const styles = {
 [polished.hiDPI(1.5)]: {
   width: '200px',
 }
};

// 返回值
//'@media only screen and (-webkit-min-device-pixel-ratio: 1.5),
// only screen and (min--moz-device-pixel-ratio: 1.5),
// only screen and (-o-min-device-pixel-ratio: 1.5/1),
// only screen and (min-resolution: 144dpi),
// only screen and (min-resolution: 1.5dppx)': {
//  'width': '200px',
//}
</code></pre></blockquote>

<p><code>retinaImage</code>为高分屏和低分屏设置不同的背景图。</p>

<blockquote><pre><code class="language-javascript">
const styles = {
 ...polished.retinaImage('my-img')
};

// 返回值
//   backgroundImage: 'url(my-img.png)',
//  '@media only screen and (-webkit-min-device-pixel-ratio: 1.3),
//   only screen and (min--moz-device-pixel-ratio: 1.3),
//   only screen and (-o-min-device-pixel-ratio: 1.3/1),
//   only screen and (min-resolution: 144dpi),
//   only screen and (min-resolution: 1.5dppx)': {
//    backgroundImage: 'url(my-img_2x.png)',
//  }
</code></pre></blockquote>

<p>7、</p>

<p><code>polished.js</code>提供的其他方法如下，详细用法请参考。</p>

<blockquote>
  <ul>
<li><code>normalize()</code>：样式表初始化</li>
<li><code>placeholder()</code>：对 placeholder 伪元素设置样式</li>
<li><code>selection()</code>：对 selection 伪元素设置样式</li>
<li><code>darken()</code>：调节颜色深浅</li>
<li><code>lighten()</code>：调节颜色深浅</li>
<li><code>desaturate()</code>：降低颜色的饱和度</li>
<li><code>saturate()</code>：增加颜色的饱和度 </li>
<li><code>opacify()</code>：调节透明度</li>
<li><code>complement()</code>：返回互补色</li>
<li><code>grayscale()</code>：将一个颜色转为灰度</li>
<li><code>rgb()</code>：指定红、绿、蓝三个值，返回一个颜色</li>
<li><code>rgba()</code>：指定红、绿、蓝和透明度四个值，返回一个颜色</li>
<li><code>hsl()</code>：指定色调、饱和度和亮度三个值，返回一个颜色</li>
<li><code>hsla()</code>：指定色调、饱和度、亮度和透明度三个值，返回一个颜色</li>
<li><code>mix()</code>：混合两种颜色</li>
<li><code>em()</code>：将像素转为 em</li>
<li><code>rem()</code>：将像素转为 rem</li>
</ul>
</blockquote>

<p>目前，<code>polished.js</code>只是1.0版，以后应该会有越来越多的方法。</p>

<p>8、</p>

<p><code>polished.js</code>还有一个特色：所有函数默认都是柯里化的，因此可以进行函数组合运算，定制出自己想要的函数。</p>

<blockquote><pre><code class="language-javascript">
import { compose } from 'ramda';
import { lighten, desaturate } from 'polished';

const tone = compose(lighten(10), desaturate(10))
</code></pre></blockquote>

<p>上面代码使用 Ramda 函数库完成组合运算。Ramda 的用法可以参考我写的。</p>

<p>（正文完）</p>

<p>==========</p>

<p>最后，发布一个活动消息。</p>

<p>大家知道，美国最大之一的在线教育网站优达学城（Udacity），一直赞助我的博客。他们正在国内推广，有一系列的配套活动。</p>

<p></p>

<p>4月6日晚上8点，他们邀请，探讨深度学习和语言智能，感兴趣的朋友不要错过。</p>

<p>【主讲人】</p>

<p>吕正东博士，曾任职于微软亚洲研究院、华为诺亚方舟实验室等著名研究机构，长期从事机器学习及人工智能的研究，在深度学习、自然语言处理和半监督学习等领域卓有建树，是深度学习领域（尤其是自然语言处理方向）具有世界顶尖水平并享有国际声誉的科学家和技术专家。</p>

<p>【活动内容】</p>

<ul>
<li>深度学习在自然语言处理方面的新进展</li>
<li>深度学习是否会主导自然语言处理</li>
<li>自然语言处理和人工智能的下一个大事件</li>
<li>我为什么创立深度好奇</li>
<li>自由提问时间</li>
</ul>

<p>【时间】</p>

<p>4月6日晚上8点</p>

<p>【网址】</p>

<p></p>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2017-04-05T00:15:51+08:00">2017年4月 5日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>博客文集：</li>
<li>社交媒体：</li>
<li>Feed订阅： </li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------
<h1 id="#title_1" >2、Creating One Browser Extension For All Browsers: Edge, Chrome, Firefox, Opera, Brave And Vivaldi</h1>
David Rousset
[https://www.smashingmagazine.com/2017/04/browser-extension-edge-chrome-firefox-opera-brave-vivaldi/](https://www.smashingmagazine.com/2017/04/browser-extension-edge-chrome-firefox-opera-brave-vivaldi/)
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
</table><p>In today's article, we'll create a JavaScript extension that works in all major modern browsers, using the very same code base. Indeed, the Chrome extension model based on HTML, CSS and JavaScript is now available almost everywhere, and there is even a <em>Browser Extension Community Group</em> working on a standard.</p>

<figure></figure>

<p>I'll explain how you can install this extension that supports the web extension model (i.e. Edge, Chrome, Firefox, Opera, Brave and Vivaldi), and provide some simple tips on how to get a unique code base for all of them, but also how to debug in each browser.</p><p>The post .</p>
---------------
<h1 id="#title_2" >3、文章： 微服务可靠性设计</h1>
李林锋
[http://www.infoq.com/cn/articles/micro-service-reliability-design?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/micro-service-reliability-design?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/micro-service-reliability-design/zh/smallimage/article-logo.jpg"/><p>微服务化之后，系统分布式部署，传统单个流程的本地API调用被拆分成多个微服务之间的跨网络调用，由于引入了网络通信、序列化和反序列化等操作，系统发生故障的概率提高了很多。</p> <i>By 李林锋</i>
---------------
<h1 id="#title_3" >4、文章： 如何基于Openstack telemetry项目实现云监控报警服务</h1>
任敏敏
[http://www.infoq.com/cn/articles/how-to-implement-cloud-monitoring-alarm-service?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/how-to-implement-cloud-monitoring-alarm-service?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/how-to-implement-cloud-monitoring-alarm-service/zh/smallimage/automation_logo.jpg"/><p>OpenStack Telemetry项目是OpenStack big tent下负责计量统计的组件，目前Telemetry是包含了四个子项目，Ceilometer、 Aodh、Gnocchi和Panko。其中的Ceilometer项目是最早OpenStack项目中负责计量统计的服务，但是由于云平台数据收集越来越多造成ceilometer越来越复杂，因此在Mitaka版本开始ceilometer项目开始分解为不同项目，并统称为OpenStack Telemetry。</p> <i>By 任敏敏</i>
---------------
<h1 id="#title_4" >5、文章： 数据驱动在链家网搜索优化与推荐策略中的实践</h1>
严言
[http://www.infoq.com/cn/articles/practise-of-data-driven-search-and-optimize-in-lianjia?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/practise-of-data-driven-search-and-optimize-in-lianjia?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/practise-of-data-driven-search-and-optimize-in-lianjia/zh/smallimage/logo (28).jpg"/><p>房产领域天然融合了，房、客、经纪人三方的数据，其相互之间的匹配关系与资源调度也都需要策略进行调优，我们期望通过科学的数据处理与分析，以及合理的实验论证，不断提高线上与线下的策略效果，也给用户带来更好的产品体验。</p> <i>By 严言</i>
---------------
<h1 id="#title_5" >6、视频演讲： 如何深度融合搜索和推荐：兴趣引擎架构设计</h1>
田明军
[http://www.infoq.com/cn/presentations/design-of-interest-engine-architecture?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/design-of-interest-engine-architecture?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/design-of-interest-engine-architecture/zh/mediumimage/tianmingjun270.jpg"/><p>搜索引擎是用户获取信息的超级入口，在过去10多年的发展中逐渐被广大用户接受。个性化推荐通过对用户行为的深入挖掘，在用户被动浏览的场景中为用户提供最符合兴趣的内容，已经被广泛应用于电商、新闻等领域，也越来越得到终端用户的青睐。一点资讯从创办之初，就致力于深度融合搜索和推荐，通过打磨兴趣引擎技术提供满足用户在获取资讯方面的需求。本次分享将介绍一点资讯兴趣引擎服务架构，重点介绍在服务系统方面的一些探索，如果通过索引建设、索引查询和在线排序各个层面支持搜索和推荐技术的打通。</p> <i>By 田明军</i>
---------------
<h1 id="#title_6" >7、每月亿行代码、全球数万研发，落地DevOps的协同平台DevCloud</h1>
木环、麦麦
[http://www.infoq.com/cn/news/2017/04/devcloud-huawei-devops-code?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/04/devcloud-huawei-devops-code?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>在信息化企业的这条路上，我们已经走得很远了，从少数单机到集群的规模壮大；软件生态也不断丰富完善，从底层系统到上层的业务分析、ERP、数据库等自研定制亦或是第三方应用。正式因为有了这些IT基础，云计算也开始生根发芽。</p> <i>By 木环、麦麦</i>
---------------
<h1 id="#title_7" >8、Swift 3.1改进了语言、包管理器和Linux实现</h1>
Sergio De Simone
[http://www.infoq.com/cn/news/2017/04/swift-31-released?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/04/swift-31-released?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>按照计划，近日发布的Swift 3.1在源代码方面可兼容Swift 3.0，但同时在语言和标准库方面包含大量改进，并增强了Linux的实现。</p> <i>By Sergio De Simone</i> <i> Translated by 大愚若智</i>
---------------
<h1 id="#title_8" >9、FEX 技术周刊 - 2017/04/05</h1>

[http://fex.baidu.com/blog/2017/04/fex-weekly-05//](http://fex.baidu.com/blog/2017/04/fex-weekly-05//)
作者：nwind <br> <p>微信搜索『FEX』关注我们的公众号，及时获得最新资讯。</p>

<h2 id="section">深阅读</h2>

<p><strong>Simple React Development in 2017</strong><br />
https://hackernoon.com/simple-react-development-in-2017-113bd563691f<br />
Regardless of your background, you’ve likely had a similar experience: React itself seems pretty straightforward, but the tooling and ecosystem is overwhelming. However, this is a solved problem! Believe it or not, it is actually very simple and painless to start a new React project, thanks to amazing work by the community over the past year. The goal of this guide is to showcase how easy it can be to start modern React development. It shares a step-by-step process, from initial system setup through to deployment, without straying into tangent explanations that aren’t critical at this point in the learning process.</p>

<p><strong>Building For Mobile: RWD, PWA, AMP Or Instant Articles?</strong><br />
https://www.smashingmagazine.com/2017/03/building-for-mobile-rwd-pwa-amp-instant-articles/<br />
Today, as our findings indicate, responsive web design is the norm, with 7 out of 10 mobile-optimized websites being responsive, up from 5 last year, which begs the questions: What’s next? Where is it all heading? We solved the screen-size issue and had a great run for a few years — now what?</p>

<p><strong>70%以上业务由H5开发，手机QQ Hybrid 的架构如何优化演进</strong><br />
http://mp.weixin.qq.com/s?__biz=MjM5MDE0Mjc4MA==&amp;mid=2650995689&amp;idx=1&amp;sn=4f77f121345004ae6e18f4b945e46f8e<br />
介绍QQ会员团队如何在页面打开时间以及用户流量方面所做的优化，分别对应sonic和reshape的两个自主技术框架。</p>

<p><strong>如何向开源项目提交无法解答的问题</strong><br />
https://zhuanlan.zhihu.com/p/25795393<br />
作为一名互联网开发者，本人使用和参与过许多开源项目。开源社区里，提问和回答是最有趣的组成部分，有些你来我往，有些则石沉大海。人们提问的方式有许多迷人和实用的共通之处。我把它们提炼出来，希望能帮助到那些像我一样充满了好奇心、且愿意付诸行动去惹恼开源项目维护者的人们。</p>

<p><strong>Powering UberEATS with React Native and Uber Engineering</strong><br />
https://eng.uber.com/ubereats-react-native/<br />
In this article, we focus on one challenge in particular: how Uber Engineering handled introducing a third party to what had previously been a two-sided marketplace.</p>

<p><strong>Memory-Efficient Image Passing in the Document Scanner</strong><br />
https://blogs.dropbox.com/tech/2017/03/memory-efficient-image-passing-in-document-scanner/<br />
Speed is not the only thing that matters in a mobile environment: what about memory? Bounding both peak memory usage and memory spikes is important, since the operating system may terminate the app outright when under memory pressure. In this blog post, we will discuss some tweaks we made to lower the memory usage of our iOS document scanner.</p>

<p><strong>ARIA Grid: Supporting nonvisual layout and keyboard traversal</strong><br />
https://code.facebook.com/posts/1232839800098854/aria-grid-supporting-nonvisual-layout-and-keyboard-traversal/<br />
At Facebook, we are experimenting with a user interface pattern for traversing a page with a keyboard that we call a logical grid. A logical grid reduces numerous tab stops to a single tab stop within a part of the interface designated as a grid. From the single tab stop, a person can traverse items in the grid using arrow keys.</p>

<p><strong>A11Y Style Guide</strong><br />
http://a11y-style-guide.com/style-guide/<br />
The A11Y style guide comes with pre-populated accessible components that include helpful links to related tools, articles, and WCAG guidelines to make your site more inclusive. These components also serve as a guide for both HTML markup and SCSS/CSS code, to inform designers, front-end and back-end developers at every stage of the website’s creation.</p>

<p><strong>Setting up multi-platform npm packages</strong>  <br />
http://2ality.com/2017/04/setting-up-multi-platform-packages.html<br />
This blog post explains ways of targeting multiple platforms via the same npm package.</p>

<p><strong>Using DevTools to Tweak Designs in the Browser</strong><br />
https://css-tricks.com/using-devtools-tweak-designs-browser/<br />
Let’s look at some ways we can use the browsers DevTools to do design work. There are a few somewhat hidden tricks you mind find handy!</p>

<p><strong>The Basics of DOM Manipulation in Vanilla JavaScript</strong><br />
https://www.sitepoint.com/dom-manipulation-vanilla-javascript-no-jquery/<br />
In this article, I’ll demonstrate how to accomplish some of the most common DOM manipulation tasks with plain JavaScript, namely: querying and modifying the DOM, modifying classes and attributes, listening to events, and animation.</p>

<p><strong>The Definitive Guide for Monitoring Node.js Applications</strong><br />
https://blog.risingstack.com/monitoring-nodejs-applications-nodejs-at-scale/<br />
In this article, we will learn about running and monitoring Node.js applications in Production. Let’s discuss these topics: What is monitoring? What should be monitored? Open-source monitoring solutions; SaaS and On-premise monitoring offerings.</p>

<p><strong>React Fiber是什么</strong><br />
https://zhuanlan.zhihu.com/p/26027085<br />
使用React的同学们都应该要知道React Fiber，因为这玩意快要正式发布了。据说Facebook在自己的网站已经将React Fiber投入实战，所以，React Fiber大势所趋，是时候了解一下React Fiber了。React Fiber是个什么东西呢？官方的一句话解释是“React Fiber是对核心算法的一次重新实现”。这么说似乎太虚无缥缈，所以还是要详细说一下。</p>

<p><strong>React London 2017 Conference Report</strong>  <br />
https://www.magnolia-cms.com/blogs/christopher-zimmermann/detail~&amp;react-london-2017-conference-report~.html<br />
In this blog post I hope to get you up to speed on what was presented at the conference. I’ll do a short blow-by-blow rundown of a few of the presentations and then share one person’s perspective of the themes that emerged during the day. 另附：</p>

<p><strong>React Lifecycle Methods- how and when to use them</strong><br />
https://engineering.musefind.com/react-lifecycle-methods-how-and-when-to-use-them-2111a1b692b1<br />
In an ideal world, we wouldn’t use lifecycle methods. All our rendering issues would be controlled via state and props. But it’s not an ideal world, and sometimes you need to exact a little more control over how and when your component is updating. Use these methods sparingly, and use them with care. I hope this article has been helpful in illuminating when and how to use lifecycle methods.</p>

<p><strong>6 Reasons Why JavaScript’s Async/Await Blows Promises Away</strong><br />
https://hackernoon.com/6-reasons-why-javascripts-async-await-blows-promises-away-tutorial-c7ec10518dd9<br />
In case you missed it, Node now supports async/await out of the box since version 7.6. If you haven’t tried it yet, here are a bunch of reasons with examples why you should adopt it immediately and never look back.</p>

<p><strong>精读 js 模块化发展</strong><br />
https://zhuanlan.zhihu.com/p/26118022<br />
前端精读期刊与大家第一次正式碰面，我们每周会精读并分析若干篇精品好文，试图讨论出结论性观点。这期的主题是：。</p>

<p><strong>从技术、平台、工具、语言&amp;框架等四大方面，详解技术未来的趋势</strong><br />
http://mp.weixin.qq.com/s?__biz=MjM5MDE0Mjc4MA==&amp;mid=2650995709&amp;idx=1&amp;sn=5a750ca48e2fb8ab2e6c13f7ac542b6d<br />
ThoughtWorks 最新的技术雷达的解读。</p>

<p><strong>IMVC（同构 MVC）的前端实践</strong><br />
http://mp.weixin.qq.com/s?__biz=MzIwNjQwMzUwMQ==&amp;mid=2247485119&amp;idx=1&amp;sn=5cd3855a84cd0a7bfd5b7c69ac853258<br />
React/Vue 和 Redux/Vuex 是分别在 MVC 中的 View 层和 Model 层做了进一步发展。如果 MVC 中的 Controller 层也推进一步，将得到一种升级版的 MVC，我们称之为 IMVC（同构 MVC）。IMVC 可以实现一份代码在服务端和浏览器端皆可运行，具备单页应用和多页应用的所有优势，并且可以这两种模式里通过配置项进行自由切换。配合 Node.js、Webpack、Babel 等基础设施，我们可以得到相比之前更加完善的一种前端架构。</p>

<p><strong>[译]一份关于Angular的倡议清单</strong> <br />
http://mp.weixin.qq.com/s?__biz=MzA5Nzc4OTA1Mw==&amp;mid=2659599100&amp;idx=1&amp;sn=568cd164c9bea2e9fba075f0d025491c<br />
Angular虽然是一个优秀的功能全面的JavaScript框架，但是如果停滞不前将逐渐丧失活力。新的特性会为开发者提供更强大的功能和新的机会来构建更完美的App。Eamon O’Tuathail在本文中将会提出一些如何让Angular更新潮更令人振奋的发展建议。</p>

<p><strong>CURL IS C</strong><br />
https://daniel.haxx.se/blog/2017/03/27/curl-is-c/<br />
Every once in a while someone suggests to me that curl and libcurl would do better if rewritten in a “safe language”. Rust is one such alternative language commonly suggested. This happens especially often when we publish new security vulnerabilities. At the end of the day the question that remains is: would we gain more than we would pay, and over which time frame? Who would gain and who would lose? CURL 的维护者对技术选型的考虑挺值得参考的。</p>

<p><strong>Scaling your API with rate limiters</strong><br />
https://stripe.com/blog/rate-limiters<br />
Rate limiting is one of the most powerful ways to prepare your API for scale. The different rate limiting strategies described in this post are not all necessary on day one, you can gradually introduce them once you realize the need for rate limiting. 另附：https://mp.weixin.qq.com/s?__biz=MzA5Nzc4OTA1Mw==&amp;mid=2659599014&amp;idx=1&amp;sn=14ffbf9307b0f11fd218285c837204f2</p>

<p><strong>Thirteen Years of Bad Game Code</strong><br />
http://etodd.io/2017/03/29/thirteen-years-of-bad-game-code/<br />
There are many, many more embarrassing mistakes to discuss. I discovered another “creative” method to avoid globals. For some time I was obsessed with closures. I designed an “entity” “component” “system” that was anything but. I tried to multithread a voxel engine by sprinkling locks everywhere. Here’s the takeaway: Make decisions upfront instead of lazily leaving them to the computer; Separate behavior and state; Write pure functions; Write the client code first; Write boring code.</p>

<p><strong>Modules vs. microservices</strong><br />
https://www.oreilly.com/ideas/modules-vs-microservices<br />
Much has been said about moving from monoliths to microservices. Besides rolling off the tongue nicely, it also seems like a no-brainer to chop up a monolith into microservices. But is this approach really the best choice for your organization? It’s true that there are many drawbacks to maintaining a messy monolithic application. But there is a compelling alternative which is often overlooked: modular application development. In this article, we’ll explore what this alternative entails and show how it relates to building microservices.</p>

<h2 id="section-1">新鲜货</h2>

<p><strong>Google Open Source - A new home for Google Open Source</strong><br />
https://opensource.googleblog.com/2017/03/a-new-home-for-google-open-source.html<br />
赞 Google 的 slogan : Bringing better technology to the world by promoting open source. 另附：.</p>

<p><strong>New Web Features in Safari 10.1</strong><br />
https://webkit.org/blog/7477/new-web-features-in-safari-10-1/<br />
While this release makes the web platform more capable and powerful, it also makes web development easier, simplifying the ongoing maintenance of your code. We’re excited to see how web developers will translate these improvements into better experiences for users.</p>

<p><strong>Swift 3.1 Released!</strong><br />
https://swift.org/blog/swift-3-1-released/<br />
Swift 3.1 is now officially released! Swift 3.1 is a minor release that contains improvements and refinements to the Standard Library. Thanks to efforts by IBM and other members of the community, it also includes many updates to the Linux implementation of Swift. There are also a number of updates to Swift Package Manager.</p>

<p><strong>Echarts v3.5 发布</strong><br />
http://echarts.baidu.com/blog/2017/03/23/new-release.html<br />
在 echarts 新发布的 3.5 版本中，新增了日历坐标系，增强了坐标轴指示器。同时，echarts 统计扩展 1.0 版本发布了。日历坐标系用于在日历中绘制图表，坐标轴指示器方便用户观察数据内容，统计扩展是一个专门用来进行数据分析的工具。</p>

<p><strong>你不知道的前端新特性</strong><br />
https://ppt.baomitu.com/display?slide_id=84a42e3e#/<br />
查漏补缺专用。</p>

<p><strong>The Complete Redux Book</strong><br />
https://leanpub.com/redux-book<br />
In this book you will learn about the inner workings of Redux, and how to use it to solve real-world challenges. We’ll teach you about everything you need to know to use this valuable tool effectively, including store enhancers, normalized state, unit testing, using third-party libraries, and much, much more.</p>

<p><strong>Next.js 2.0</strong><br />
https://zeit.co/blog/next2<br />
We are proud to introduce Next 2.0 to the world. What follows is a quick summary of every new feature and improvement we have made:
Component CSS Support; Programmatic API; Pre-fetching.</p>

<p><strong>Redux Offline: A Persistent Redux Store for Offline-First Apps</strong><br />
https://github.com/jevakallio/redux-offline<br />
Persistent Redux store for Reasonaboutable™️ Offline-First applications, with first-class support for optimistic UI. Use with React, React Native, or as standalone state container for any web app.</p>

<p><strong>Reactide - The first dedicated IDE for React web application development</strong><br />
http://reactide.io/<br />
Reactide is a cross-platform desktop application that offers a custom simulator, making build-tool and server configuration unnecessary. Reactide brings development back to the days where opening a single file instantly renders the project in the browser. With Reactide, developers can achieve the same simplicity with a single React JSX file while still utilizing the power of React.</p>

<p><strong>Fuchsia: a new operating system</strong><br />
https://lwn.net/SubscriberLink/718267/206c8a5fbf0ee2ea/<br />
Fuchsia is a new operating system being built more or less from scratch at Google. From piecing together information from the online documentation and source code, we can surmise that Fuchsia is a complete operating system for PCs, tablets, and high-end phones.</p>

<p><strong>Apollo Client 1.0: A flexible, community-focused JavaScript GraphQL client</strong><br />
https://dev-blog.apollodata.com/apollo-client-1-0-a-flexible-community-focused-javascript-graphql-client-2253b90e6c84<br />
Apollo Client is a client-side library that leverages the power of a GraphQL API to handle data fetching and management for you, so that you can spend less time plumbing data and more on building your application.</p>

<p><strong>Explain Shell</strong><br />
https://explainshell.com/<br />
explainshell is a tool (with a web interface) capable of parsing man pages, extracting options and explain a given command-line by matching each argument to the relevant help text in the man page.</p>

<p><strong>AsciiMath</strong><br />
http://asciimath.org/<br />
AsciiMath is an easy-to-write markup language for mathematics.ASCIIMathML.js is a compact JavaScript program that translates simple calculator-style math expressions on a webpage to MathML.</p>

<p><strong>Polished - A lightweight toolset for writing styles in JavaScript</strong><br />
https://polished.js.org/<br />
Want to write styles in JavaScript, but also want Sass-style helper functions and mixins? Need a consistent color palette throughout your app? ✨ polished is for you!</p>

<p><strong>The 5 features of ES8 and a wishlist for ES</strong><br />
https://www.sitepen.com/blog/2017/03/21/the-5-features-of-es8-and-a-wishlist-for-es9/<br />
We wanted to take a few moments to highlight our 5 favorite things about the upcoming 2017 release: 1. Object.entries and Object.values; 2. String.prototype.padStart / String.prototype.padEnd; 3. Object.getOwnPropertyDescriptors; 4. Async functions; 5. Shared memory and atomics.</p>

<p><strong>Chromium policy on JavaScript dialogs</strong><br />
https://developers.google.com/web/updates/2017/03/dialogs-policy<br />
While they fit into the JavaScript of the time, their synchronous API is problematic for modern browsers. Because the JavaScript engine needs to pause until a user response is obtained, the JavaScript dialogs are app-modal. And because the dialogs are app-modal, they commonly (and unfortunately) are used to harm our users. Because of this, the Chromium team highly recommends that you not use JavaScript dialogs.</p>

<p><strong>Popper.js</strong><br />
https://popper.js.org/<br />
A library used to position poppers in web applications.A popper is an element on the screen which “pops out” from the natural flow of your application. Common examples of poppers are tooltips, popovers and drop-downs.</p>

<p><strong>fsm-as-promised</strong><br />
https://github.com/vstirbu/fsm-as-promised<br />
A minimalistic finite state machine library for browser and node implemented using promises.</p>

<p><strong>Glimmer - A fast and lightweight UI component library from the Ember.js team</strong>  <br />
https://glimmerjs.com/<br />
Glimmer is one of the fastest DOM rendering engines, delivering exceptional performance for initial renders as well as updates. Architected like a virtual machine (VM), Glimmer compiles your templates into low-level code so it can run as fast as possible—without sacrificing ease of use.</p>

<h2 id="section-2">产品及其它</h2>

<p><strong>参与这场线上大战之后，我觉得人类未来还是有希望的</strong><br />
http://mp.weixin.qq.com/s?__biz=MjM5MTE4Nzk1NA==&amp;mid=2650741697&amp;idx=1&amp;sn=9e460ef496d57164c27b617ff17a78f8<br />
愚人节 Reddit上线了一个叫做Place的节点，它是一块空白的巨大画布，每个用户每10分钟会得到一个机会，可以选一种颜色，在上面点一个点（后来间隔时间被修改成5分钟）。规则本身非常简单，但和Reddit的气质非常贴合，Reddit本来就是一个靠投票和用户贡献来产生内容的网站，用户参与度很高。这不仅是一个出色的愚人节项目，也是一个伟大的尝试，在这种完全自由，不受管控，只有简单规则的活动里面，人们之间会产生什么样的互动？</p>

<p><strong>[译]Redis之父：如何成为一个高效的程序员</strong><br />
http://mp.weixin.qq.com/s?__biz=MzA5Nzc4OTA1Mw==&amp;mid=2659599117&amp;idx=1&amp;sn=eac8fb8f90f1dcadcb1d2ac7420410cb<br />
在我的二十年程序员生涯中，我与其他程序员一起工作，作为同事，或者由我指导他们达成目标，为Redis和其他项目贡献代码补丁。在工作过程中，我仔细观察他们。与此同时，有很多人说我是一个高能的程序员。不过我不认为自己是一个工作狂，我只是编码速度比较快而已。
下面列出了我认为可以用于区分程序员生产力高低的重要特质。 另附：</p>

<p><strong>Tower 团队 48 个月远程实践</strong><br />
https://zhuanlan.zhihu.com/p/26031654<br />
有三个驱动我们远程工作的原因，一是产品原因，二是不愿意再花时间在一些麻烦事上，三是最重要的一点，就是因为彼此信任。2013 年我们决定要开始远程工作，当时最大的一个初衷是想要通过这种方式，把产品打造得更好。远程工作适合耐心的团队，适合愿意独自面对自己的团队，适合对目标有清醒认识的团队，适合单兵作战强悍的团队，如果你的团队是这样的，不妨一试。</p>
---------------
<h1 id="#title_9" >10、IBM发布了自己的区块链即服务</h1>
Kent Weare
[http://www.infoq.com/cn/news/2017/04/IBM-Blockchain-BaaS?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/04/IBM-Blockchain-BaaS?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>在近期的IBM InterConnect大会上，IBM宣布发布自己的区块链即服务。该服务基于Linux基金会的Hyperledger
Fabric 1.0版本，运行在经LinuxONE加固的IBM高度安全网络上。Hyperledger Fabric此前一直处于孵化器状态，自此被提升为活跃状态。</p> <i>By Kent Weare</i> <i> Translated by Rays</i>
---------------
<h1 id="#title_10" >11、Buurtzorg通向Teal组织的敏捷之旅</h1>
Ben Linders
[http://www.infoq.com/cn/news/2017/04/agile-journey-buurtzorg-teal?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/04/agile-journey-buurtzorg-teal?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Buurtzorg是荷兰一家全国性的护理组织，完全使用自管理方法来运营。团队完全是自组织的，而且，组织已经建立起了一种文化，后勤部门会为组织中的独立团队提供支持。他们的IT系统是采用敏捷方法开发的，可以帮助团队向病人提供护理服务。</p> <i>By Ben Linders</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_11" >12、Visual Studio 2017迎来F# 4.1</h1>
Pierre-Luc Maheu
[http://www.infoq.com/cn/news/2017/04/visual-studio-2017-fsharp-41?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/04/visual-studio-2017-fsharp-41?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>三月初发布的Visual Studio 2017，包含了F# 4.1和Visual F#工具的更新。F# 4.1带来了语言层面提升以及与C# 7的互操作能力，而那些Visual F#工具是支持Roslyn workspaces的首个版本。
</p> <i>By Pierre-Luc Maheu</i> <i> Translated by 张健欣</i>
---------------
<h1 id="#title_12" >13、Google Cloud Next会议摘要</h1>
Richard Seroter
[http://www.infoq.com/cn/news/2017/04/google-cloud-next?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/04/google-cloud-next?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>来自世界各地的云端爱好者参加了Google Cloud Next会议，听取搜索行业巨头的更新情况。在很多主题演讲和200多个会议中出现了三个较为宽泛的主题要点：服务规模和成熟度、可用的机器学习和企业友好性。</p> <i>By Richard Seroter</i> <i> Translated by 冬雨</i>
---------------
<h1 id="#title_13" >14、首届商业敏捷大会圆满落幕</h1>
Shane Hastie
[http://www.infoq.com/cn/news/2017/04/business-agility2017-success?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/04/business-agility2017-success?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>首届商业敏捷大会最近在纽约召开。会议门票完全售罄，共有超过330人参加。在参与者和演讲者的反馈中，他们强调了在整个组织中采用敏捷思考时文化和思维模式的重要性，以及在当今动荡不安、复杂诡谲的商业环境下商业敏捷对成功的重要性。</p> <i>By Shane Hastie</i> <i> Translated by 袁诗瑶</i>
---------------
<h1 id="#title_14" >15、Redis之父：10x程序员应该具备哪些素质</h1>
antirez
[http://www.infoq.com/cn/news/2017/04/Redis-father-10x?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/04/Redis-father-10x?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Fred Brooks（《人月神话》的作者）最早在他的论文“没有银弹——软件工程的本质和偶然性（No Silver Bullet - Essence and Accidents of Software Engineering）”中提出了“10x程序员”的概念。技术社区对于这个概念呈现出两级分化的观点。Redis之父Salvatore Sanfilippo（antirez）列出了9种特质，他相信，如果一个程序员同时具备了这9种特质，那么就可以说他是一个10x程序员。</p> <i>By antirez</i> <i> Translated by 薛命灯</i>
---------------
<h1 id="#title_15" >16、周末的时间，我们在GitHub用什么语言编程？</h1>
Felipe Hoffa
[http://www.infoq.com/cn/news/2017/04/Top-Weekend-Programming-Language?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/04/Top-Weekend-Programming-Language?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Felipe Hoffa是一位来自智利的工程师，目前为谷歌工作并居住在旧金山，他在2月10日发表了一篇文章，原题是《The top weekend languages according to GitHub's code》，其实在这篇文章之前，Julia Silge已经在Stack Overflow上发表了《Top Weekend Programming Languages》，她只是针对Stack Overflow上的标签进行分析并得出统计数据。因此，读者都在reddit和Hacker News上提出了很多问题，Felipe的这篇文章使用了GitHub上的提交信息，想要进一步回答Julia未能解答的问题。</p> <i>By Felipe Hoffa</i> <i> Translated by 麦克周</i>
---------------
<h1 id="#title_16" >17、GitLab 9提供了子群组、部署面板和集成监控</h1>
Sergio De Simone
[http://www.infoq.com/cn/news/2017/04/gitlab-9-released?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/04/gitlab-9-released?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p> GitLab发布了其软件开发协作平台的第九个版本（GitLab 9.0）。在所有的新特性中，最值得关注的是子群组和集成性能监控。InfoQ就此对GitLab的CEO和联合创始人Sid Sijbrandij进行了采访。</p> <i>By Sergio De Simone</i> <i> Translated by Rays</i>
---------------