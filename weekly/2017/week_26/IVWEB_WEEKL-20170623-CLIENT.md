## 文章索引
1、 <a href="#1文章-关于norx物联网安全和区块链听听philipp-jovanovic怎么说" >文章： 关于NORX，物联网安全和区块链，听听Philipp Jovanovic怎么说</a><br/>
2、 <a href="#2html-自定义元素教程" >HTML 自定义元素教程</a><br/>
3、 <a href="#3视频演讲-搜狗深度学习技术在广告推荐领域的应用" >视频演讲： 搜狗深度学习技术在广告推荐领域的应用</a><br/>
4、 <a href="#4文章-如何进行技术招聘" >文章： 如何进行技术招聘？</a><br/>
5、 <a href="#5乐变黄杲当前如何选择app热更新服务" >乐变黄杲：当前如何选择App热更新服务</a><br/>
6、 <a href="#6free-icon-set:-happy-4th-of-july-🇺🇸-20-icons-png-eps-ai-svg" >Free Icon Set: Happy 4th Of July 🇺🇸 (20 Icons, PNG, EPS, AI, SVG)</a><br/>
7、 <a href="#7google发布新的tensorflow物体检测api" >Google发布新的TensorFlow物体检测API</a><br/>
8、 <a href="#8物联网技术周报第-95-期:-工信部发文推进移动物联网nb-iot建设" >物联网技术周报第 95 期: 工信部发文推进移动物联网（NB-IoT）建设</a><br/>
9、 <a href="#9概览visual-studio-153的第二个预览版" >概览Visual Studio 15.3的第二个预览版</a><br/>
10、 <a href="#10c#-72和80路线图" >C# 7.2和8.0路线图</a><br/>
11、 <a href="#11联结技术领导者|-ego-全国会员招募季正式开启" >联结技术领导者| EGO 全国会员招募季正式开启</a><br/><h1 id="#title_0" >1、文章： 关于NORX，物联网安全和区块链，听听Philipp Jovanovic怎么说</h1>
Mathieu Bolla, Philipp Jovanovic
[http://www.infoq.com/cn/articles/jovanovic-norix-iot-blockchain?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/jovanovic-norix-iot-blockchain?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/jovanovic-norix-iot-blockchain/zh/smallimage/crypto.jpg"/><p>在本次采访（最初发布在InfoQ的法国站上）中，Mathieu Bolla和EPFL的密码专家Philipp Jovanovic进行了对话，讨论了关于NORX，物联网安全和保持自己在线安全及区块链等话题。</p> <i>By Mathieu Bolla</i> <i> Translated by 姚佳灵</i>
---------------
<h1 id="#title_1" >2、HTML 自定义元素教程</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2017/06/custom-elements.html](http://www.ruanyifeng.com/blog/2017/06/custom-elements.html)
<p>组件是 Web 开发的方向，现在的热点是 JavaScript 组件，但是 HTML 组件未来可能更有希望。</p>

        <p>本文就介绍 HTML 组件的基础知识：自定义元素（custom elements）。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017062201.png" alt="" title="" /></p>

<p>文章结尾还有一则 （含 React Native），欢迎关注。</p>

<h2>一、浏览器处理</h2>

<p>我们一般都使用标准的 HTML 元素。</p>

<blockquote><pre><code class="language-markup">
&lt;p>Hello World&lt;/p>
</code></pre></blockquote>

<p>上面代码中，<code>&lt;p&gt;</code>就是标准的 HTML 元素。</p>

<p>如果使用非标准的自定义元素，会有什么结果？</p>

<blockquote><pre><code class="language-markup">
&lt;greeting>Hello World&lt;/greeting>
</code></pre></blockquote>

<p>上面代码中，<code>&lt;greeting&gt;</code>就是非标准元素，浏览器不认识它。这段代码的是，浏览器照常显示<code>Hello World</code>，这说明浏览器并没有过滤这个元素。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017062202.png" alt="" title="" /></p>

<p>现在，为自定义元素加上样式。</p>

<blockquote><pre><code class="language-css">
greeting {
  display: block;
  font-size: 36px;
  color: red;
}
</code></pre></blockquote>

<p>如下。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017062203.png" alt="" title="" /></p>

<p>接着，使用脚本操作这个元素。</p>

<blockquote><pre><code class="language-javascript">
function customTag(tagName, fn){
  Array
    .from(document.getElementsByTagName(tagName))
    .forEach(fn);
}

function greetingHandler(element) {
  element.innerHTML = '你好，世界';
}   

customTag('greeting', greetingHandler);
</code></pre></blockquote>

<p>如下。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017062204.png" alt="" title="" /></p>

<p>这说明，浏览器对待自定义元素，就像对待标准元素一样，只是没有默认的样式和行为。这种处理方式是写入 的。</p>

<blockquote>
  <p>"User agents must treat elements and attributes that they do not understand as semantically neutral; leaving them in the DOM (for DOM processors), and styling them according to CSS (for CSS processors), but not inferring any meaning from them."</p>
</blockquote>

<p>上面这段话的意思是，浏览器必须将自定义元素保留在 DOM 之中，但不会任何语义。除此之外，自定义元素与标准元素都一致。</p>

<p>事实上，浏览器提供了一个<code>HTMLUnknownElement</code>对象，所有自定义元素都是该对象的实例。</p>

<blockquote><pre><code class="language-javascript">
var tabs = document.createElement('tabs');

tabs instanceof HTMLUnknownElement // true
tabs instanceof HTMLElement // true
</code></pre></blockquote>

<p>上面代码中，<code>tabs</code>是一个自定义元素，同时继承了<code>HTMLUnknownElement</code>和<code>HTMLElement</code>接口。</p>

<h2>二、HTML import</h2>

<p>有了自定义元素，就可以写出语义性非常好的 HTML 代码。</p>

<blockquote><pre><code class="language-markup">
&lt;share-buttons>
  &lt;social-button type="weibo">
    &lt;a href="...">微博&lt;/a>
  &lt;/social-button>
  &lt;social-button type="weixin">
    &lt;a href="...">微信&lt;/a>
  &lt;/social-button>
&lt;/share-buttons>
</code></pre></blockquote>

<p>上面的代码，一眼就能看出语义。</p>

<p>如果将<code>&lt;share-buttons&gt;</code>元素的样式与脚本，封装在一个 HTML 文件<code>share-buttons.html</code>之中，这个元素就可以复用了。</p>

<p>使用的时候，先引入<code>share-buttons.html</code>。</p>

<blockquote><pre><code class="language-markup">
&lt;link rel="import" href="share-buttons.html">
</code></pre></blockquote>

<p>然后，就可以在网页中使用<code>&lt;share-buttons&gt;</code>了。</p>

<blockquote><pre><code class="language-markup">
&lt;article>
  &lt;h1>Title&lt;/h1>
  &lt;share-buttons/>
  ... ...
&lt;/article>
</code></pre></blockquote>

<p>HTML imports 的更多用法可以参考教程（）。目前只有 Chrome 浏览器支持这个语法。</p>

<h2>三、Custom Elements 标准</h2>

<p>HTML5 标准规定了自定义元素是合法的。然后，W3C 就为自定义元素制定了一个单独的 。</p>

<p>它与其他三个标准放在一起---- HTML Imports，HTML Template、Shadow DOM----统称为 。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017062205.jpg" alt="" title="" /></p>

<p>Custom Elements 标准对自定义元素的名字做了。</p>

<blockquote>
  <p>"自定义元素的名字必须包含一个破折号（<code>-</code>）所以<code>&lt;x-tags&gt;</code>、<code>&lt;my-element&gt;</code>和<code>&lt;my-awesome-app&gt;</code>都是正确的名字，而<code>&lt;tabs&gt;</code>和<code>&lt;foo_bar&gt;</code>是不正确的。这样的限制使得 HTML 解析器可以分辨那些是标准元素，哪些是自定义元素。"</p>
</blockquote>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017062206.jpg" alt="" title="" /></p>

<p>注意，一旦名字之中使用了破折号，自定义元素就不是<code>HTMLUnknownElement</code>的实例了。</p>

<blockquote><pre><code class="language-javascript">
var xTabs = document.createElement('x-tabs');

xTabs instanceof HTMLUnknownElement // false
xTabs instanceof HTMLElement // true
</code></pre></blockquote>

<p>Custom Elements 标准规定了，自定义元素的定义可以使用 ES6 的。</p>

<blockquote><pre><code class="language-javascript">
// 定义一个 &lt;my-element>&lt;/my-element>
class MyElement extends HTMLElement {...}
window.customElements.define('my-element', MyElement);
</code></pre></blockquote>

<p>上面代码中，原生的<code>window.customElements</code>对象的<code>define</code>方法用来定义 Custom Element。该方法接受两个参数，第一个参数是自定义元素的名字，第二个参数是一个 ES6 的<code>class</code>。</p>

<p>这个<code>class</code>使用<code>get</code>和<code>set</code>方法定义 Custom Element 的某个属性。</p>

<blockquote><pre><code class="language-javascript">
class MyElement extends HTMLElement {
  get content() {
    return this.getAttribute('content');
  }

  set content(val) {
    this.setAttribute('content', val);
  }
}
</code></pre></blockquote>

<p>有了这个定义，网页之中就可以插入<code>&lt;my-element&gt;</code>了。</p>

<blockquote><pre><code class="language-markup">
&lt;my-element content="Custom Element">
  Hello
&lt;/my-element>
</code></pre></blockquote>

<p>处理脚本如下。</p>

<blockquote><pre><code class="language-javascript">
function customTag(tagName, fn){
  Array
    .from(document.getElementsByTagName(tagName))
    .forEach(fn);
}

function myElementHandler(element) {
  element.textConent = element.content;
}

customTag('my-element', myElementHandler);
</code></pre></blockquote>

<p>如下。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017062207.png" alt="" title="" /></p>

<p>ES6 Class 的一个好处是，可以很容易地写出继承类。</p>

<blockquote><pre><code class="language-javascript">
class MyNewElement extends MyElement {
  // ...
}

customElements.define('my-new-element', MyNewElement);
</code></pre></blockquote>

<p>今天的教程就到这里，更多用法请参考谷歌的。</p>

<h2>四、参考链接</h2>

<ul>
<li>John Negoita, </li>
<li>StackOverflow, </li>
<li>Eric Bidelman, </li>
</ul>

<p>（正文完）</p>

<p>==============================</p>

<p></p>

<p>下面是一则培训消息。</p>

<p>自从我写了以后，有两种反馈：一种是觉得内容不够完整深入，希望有更详细的介绍，另一种是要求补上 React Native。对此我也没办法，精力有限，无法持续投入，只能推荐大家自己去看官方文档。</p>

<p>昨天，，希望我帮忙推广。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017062101.png" alt="" title="" /></p>

<p>我听了很兴奋，因为  和 mustache.js 就是他们的作品。我相信，国内很难找到这样水平的老师和课程。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017062102.png" alt="" title="" /></p>

<p>实际上，这件事在美国也很受关注， 进行了报道。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017062105.png" alt="" title="" /></p>

<p>与美国完全同步，一共持续4个月，分成三个环节。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017062103.png" alt="" title="" /></p>

<p>课程内容涉及整个 React 技术栈，PC 端和手机端并重。学完之后，可以获得纳米学位的证书。</p>

<p>课程价格是 3399 元人民币。如果是第一次购买优达学城的课程，可以使用优惠码<code>ruanyf</code>，便宜300元。注意，该课程不是零基础的，要求学习者已经掌握 JavaScript 基本语法，所以有报名审核环节。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017062104.png" alt="" title="" /></p>

<p>想学 React/React Native 的同学可以考虑一下，真的是很好的课程，点击了解详情，报名到6月27日截止。</p>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2017-06-22T11:50:17+08:00">2017年6月22日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>博客文集：</li>
<li>社交媒体：</li>
<li>Feed订阅： </li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------
<h1 id="#title_2" >3、视频演讲： 搜狗深度学习技术在广告推荐领域的应用</h1>
舒鹏
[http://www.infoq.com/cn/presentations/application-of-sogou-deep-learning-technology-in-ad-recommendation-field?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/application-of-sogou-deep-learning-technology-in-ad-recommendation-field?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/application-of-sogou-deep-learning-technology-in-ad-recommendation-field/zh/mediumimage/shupeng270.jpg"/><p>搜索广告是一种涉及多项复杂技术的商业形态，为众多互联网业务提供着经济支撑，新技术的应用可以使广告出的更准、更漂亮，带来更好的用户体验和经济效益。作为目前业界最流行的新技术，深度学习已经在语音、图像、NLP 等领域获得广泛应用并取得突破。我们从 2015 年开始尝试将该项新技术应用于搜狗广告的线上业务，在 CTR 预估、广告物料生成和广告相关性上均取得了较好成效。
本次演讲将以搜狗无线搜索广告为例，分享搜索广告系统的整体架构和目前深度学习的相关应用，并重点关注其中的 CTR 预估模块。介绍 CTR 预估的作用、重要性和常用方法，以及将 DNN 应用于线上 CTR 预估的方法，包括模型融合框架、并行化训练等。介绍模型评价的一些基本方式和新模型的效果及存在的问题，并给出进一步的可能解决方案和我们目前的进展。</p> <i>By 舒鹏</i>
---------------
<h1 id="#title_3" >4、文章： 如何进行技术招聘？</h1>
Jan Jorgensen
[http://www.infoq.com/cn/articles/how-to-carry-out-technical-recruitment?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/how-to-carry-out-technical-recruitment?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/how-to-carry-out-technical-recruitment/zh/smallimage/logo4 (1).jpg"/><p>技术招聘的重要性远超你的想象，一个公司的招聘流程恰恰可以反映其工程团队的水平。Jan Jorgensen在博客上分享了他经验之谈，好的招聘流程可以促成好的工程团队，而且必须做到快速回应、测试驱动和积极沟通。</p> <i>By  Jan Jorgensen</i> <i> Translated by 薛命灯</i>
---------------
<h1 id="#title_4" >5、乐变黄杲：当前如何选择App热更新服务</h1>
徐川
[http://www.infoq.com/cn/news/2017/06/how-to-choose-app-hotpatch?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/06/how-to-choose-app-hotpatch?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>上半年苹果的两次警告，通知iOS开发者在6月12日前移除热更新相关代码，否则将会下架相关App，一时间风声鹤唳，那么App热更新技术到底还能用吗？Android热更新技术还有必要做吗？</p> <i>By 徐川</i>
---------------
<h1 id="#title_5" >6、Free Icon Set: Happy 4th Of July 🇺🇸 (20 Icons, PNG, EPS, AI, SVG)</h1>
Iris Lješnjanin (Senior Editor)
[https://www.smashingmagazine.com/2017/06/4th-of-july-free-icons/](https://www.smashingmagazine.com/2017/06/4th-of-july-free-icons/)
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
</table><p>Every once in a while, we publish  related to different occasions and themes. Today, we'd like to share an icon set dedicated to a well-known upcoming American holiday.</p>

<figure></figure>

<p>Some of you may already be working on the usual flyers or brochures, so we thought we'd help you out with a set of colorful icons to spice up your designs a bit differently this year. Thank us later!</p><p>The post .</p>
---------------
<h1 id="#title_6" >7、Google发布新的TensorFlow物体检测API</h1>
Mister Who
[http://www.infoq.com/cn/news/2017/06/Google-TensorFlow-API?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/06/Google-TensorFlow-API?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Google发布TensorFlow物体检测API，帮助开发人员和研究人员识别图片中的物体。Google专注于提高API的易用性和性能，新的模型于6月16号发布，在基准测试中表现出良好的性能，并已经开始应用于研究工作当中。</p> <i>By Mister Who</i>
---------------
<h1 id="#title_7" >8、物联网技术周报第 95 期: 工信部发文推进移动物联网（NB-IoT）建设</h1>
黄峰达
[http://www.infoq.com/cn/news/2017/06/iot-weekly-95?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/06/iot-weekly-95?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>AWS Greengrass：在IoT设备上运行Lambda函数；一文理清散乱的物联网里开发者必须关注的技术！；使用 Android Things 和 Twilio 构建智能门铃；IDC：2021年全球物联网开支预计突破1.4万亿美元；工信部发文推进移动物联网（NB-IoT）建设；电信联想携手打造NB-IoT生态物联网进入大爆发时代；阿里巴巴成立首个 IoT 生态联盟，将打通技术标准。</p> <i>By 黄峰达</i>
---------------
<h1 id="#title_8" >9、概览Visual Studio 15.3的第二个预览版</h1>
Jeff Martin
[http://www.infoq.com/cn/news/2017/06/vs2017-153-preview2?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/06/vs2017-153-preview2?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Visual Studio 15.3的第二个预览版现已发布，亮点在于对.NET Framework 4.7的支持。该版本主要针对修正软件缺陷，以及提高可用性，意在提升VS软件的品质。</p> <i>By Jeff Martin</i> <i> Translated by Rays</i>
---------------
<h1 id="#title_9" >10、C# 7.2和8.0路线图</h1>
Jonathan Allen
[http://www.infoq.com/cn/news/2017/06/CSharp-7.2?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/06/CSharp-7.2?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>C# 7.2和8.0的许多新功能已经列入了计划，其中包括空引用类型和有限多重继承。</p> <i>By Jonathan Allen</i> <i> Translated by 罗远航</i>
---------------
<h1 id="#title_10" >11、联结技术领导者| EGO 全国会员招募季正式开启</h1>
赵新龙
[http://www.infoq.com/cn/news/2017/06/EGO-national-membership-opened?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/06/EGO-national-membership-opened?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>中国规模最大、最具活力的技术领导者社群EGO 全面开启会员招募季，为期十天，速来勾搭！ </p> <i>By 赵新龙</i>
---------------