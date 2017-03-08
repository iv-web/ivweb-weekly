## 文章索引
1、 <a href="#1文章-google-play的应用发现第3部分使用机器学习打击规模化的垃圾信息和恶意评论" >文章： Google Play的应用发现，第3部分：使用机器学习打击规模化的垃圾信息和恶意评论</a><br/>
2、 <a href="#2用65行代码实现javascript动画序列播放" >用65行代码实现JavaScript动画序列播放</a><br/>
3、 <a href="#3迷你书-阿里巴巴java开发手册" >迷你书： 阿里巴巴Java开发手册</a><br/>
4、 <a href="#4视频访谈-周梁伟通信协议选型与三种类型的消息处理" >视频访谈： 周梁伟：通信协议选型与三种类型的消息处理</a><br/>
5、 <a href="#5文章-拥抱可变性" >文章： 拥抱可变性</a><br/>
6、 <a href="#6文章-李大学cto应该像ceo一样思考" >文章： 李大学：CTO，应该像CEO一样思考</a><br/>
7、 <a href="#7文章-当我们在谈大前端的时候我们谈的是什么" >文章： 当我们在谈大前端的时候，我们谈的是什么</a><br/>
8、 <a href="#8digitalocean发布了高可用的托管负载均衡器" >DigitalOcean发布了高可用的托管负载均衡器</a><br/>
9、 <a href="#9bitbucket引入了强制双因素认证和ip白名单特性" >Bitbucket引入了强制双因素认证和IP白名单特性</a><br/>
10、 <a href="#10kubernetes部署失败的常见原因" >Kubernetes部署失败的常见原因</a><br/>
11、 <a href="#11视频演讲-监控系统产品选型以及经验" >视频演讲： 监控系统产品选型以及经验</a><br/>
12、 <a href="#12how-to-deliver-large-scale-projects-using-a-content-hub-strategy" >How To Deliver Large-Scale Projects Using A Content Hub Strategy</a><br/><h1 id="#title_0" >1、文章： Google Play的应用发现，第3部分：使用机器学习打击规模化的垃圾信息和恶意评论</h1>
Hsu-Chieh Lee, Xing Chen
[http://www.infoq.com/cn/articles/app-discovery-with-google-play-part03?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/app-discovery-with-google-play-part03?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/app-discovery-with-google-play-part03/zh/smallimage/qq.jpg"/><p>InfoQ此前翻译分享了“Google Play的应用发现”系列文章中的“了解主题”和“使用相关App的个性化建议”，本文是该系列的第三部分，主要介绍了Google Play如何借助机器学习技术来打击规模化的垃圾信息和恶意评论。</p> <i>By Hsu-Chieh Lee</i> <i> Translated by 杨振涛</i>
---------------
<h1 id="#title_1" >2、用65行代码实现JavaScript动画序列播放</h1>

[https://www.h5jun.com/post/sixty-lines-of-code-animation.html](https://www.h5jun.com/post/sixty-lines-of-code-animation.html)
<div class="toc"><ul>
<li><ul>
<li></li>
</ul>
</li>
<li></li>
<li></li>
</ul>
</div><p>最近在给学生上课，上周六的第一堂课是关于 JavaScript 动画的内容，其中包括一些简单的动画，比如匀速或者匀加/减速的运动，也包括复杂一些的组合动画。而动画的基本原理，在我已经有了详细的介绍。在这里，我想谈一谈的是，我们可以如何针对现代浏览器设计更加简单的 API，来实现动画的序列播放。</p>
<!--more-->
<h2>基于 Promise 的动画库</h2>
<p>所谓的动画序列，也就是说可以在上一段动画播放结束之后进行下一段动画的播放，这样可以方便用多段动画实现各种不同的复杂效果。而我们不难想到，要实现这个目的，将动画接口实现成 Promise 是一个非常好的方案：</p>
<p><script src="https:////code.h5jun.com/js/embed.min.js?3.40.2"></script></p>
<p>上面这个例子，在支持 async/await 的现代浏览器中代码非常简洁和优雅。如果要兼容旧的浏览器，也并不复杂，只需要即可。再来看一个例子：</p>
<p><script src="https:////code.h5jun.com/js/embed.min.js?3.40.2"></script></p>
<p>有了 Promise，像这样的序列运动非常简单。那么要实现这个动画库，具体该怎么做呢？</p>
<h3>具体实现</h3>
<p>其实整个库实现起来并不复杂，只需要将基础动画封装为 Promise 就可以了。</p>
<p>不过在这里，为了兼容老版本的浏览器，我们先对一些基础函数进行封装：</p>
<pre><code class="hljs lang-js"><span class="hljs-function"><span class="hljs-keyword">function</span> <span class="hljs-title">nowtime</span>(<span class="hljs-params"></span>)</span>{
  <span class="hljs-keyword">if</span>(<span class="hljs-keyword">typeof</span> performance !== <span class="hljs-string">'undefined'</span> &amp;&amp; performance.now){
    <span class="hljs-keyword">return</span> performance.now();
  }
  <span class="hljs-keyword">return</span> <span class="hljs-built_in">Date</span>.now ? <span class="hljs-built_in">Date</span>.now() : (<span class="hljs-keyword">new</span> <span class="hljs-built_in">Date</span>()).getTime();
}
</code></pre>
<p>我们说<strong>动画是关于时间的函数</strong>，因此我们需要一个简单的获取时间功能。在新的  对象，它比 Date 的计时要更精确（可以精确到纳秒）。因此获取时间我们优先使用 performance.now()，如果浏览器不支持 performance.now()，我们再降级使用 Date.now()。</p>
<p>接下来，我们对 requestAnimationFrame 进行 polyfill：</p>
<pre><code class="hljs lang-js"><span class="hljs-keyword">if</span>(<span class="hljs-keyword">typeof</span> global.requestAnimationFrame === <span class="hljs-string">'undefined'</span>){
  global.requestAnimationFrame = <span class="hljs-function"><span class="hljs-keyword">function</span>(<span class="hljs-params">callback</span>)</span>{
    <span class="hljs-keyword">return</span> setTimeout(<span class="hljs-function"><span class="hljs-keyword">function</span>(<span class="hljs-params"></span>)</span>{ <span class="hljs-comment">//polyfill</span>
      callback.call(<span class="hljs-keyword">this</span>, nowtime());
    }, <span class="hljs-number">1000</span>/<span class="hljs-number">60</span>);
  }
  global.cancelAnimationFrame = <span class="hljs-function"><span class="hljs-keyword">function</span>(<span class="hljs-params">qId</span>)</span>{
    <span class="hljs-keyword">return</span> clearTimeout(qId);
  }
}
</code></pre>
<p>然后，是具体的 Animator 实现：</p>
<pre><code class="hljs lang-js"><span class="hljs-function"><span class="hljs-keyword">function</span> <span class="hljs-title">Animator</span>(<span class="hljs-params">duration, update, easing</span>)</span>{
  <span class="hljs-keyword">this</span>.duration = duration;
  <span class="hljs-keyword">this</span>.update = update;
  <span class="hljs-keyword">this</span>.easing = easing;
}

Animator.prototype = {

  animate: <span class="hljs-function"><span class="hljs-keyword">function</span>(<span class="hljs-params"></span>)</span>{

    <span class="hljs-keyword">var</span> startTime = <span class="hljs-number">0</span>,
        duration = <span class="hljs-keyword">this</span>.duration,
        update = <span class="hljs-keyword">this</span>.update,
        easing = <span class="hljs-keyword">this</span>.easing,
        self = <span class="hljs-keyword">this</span>;

    <span class="hljs-keyword">return</span> <span class="hljs-keyword">new</span> <span class="hljs-built_in">Promise</span>(<span class="hljs-function"><span class="hljs-keyword">function</span>(<span class="hljs-params">resolve, reject</span>)</span>{
      <span class="hljs-keyword">var</span> qId = <span class="hljs-number">0</span>;

      <span class="hljs-function"><span class="hljs-keyword">function</span> <span class="hljs-title">step</span>(<span class="hljs-params">timestamp</span>)</span>{
        startTime = startTime || timestamp;
        <span class="hljs-keyword">var</span> p = <span class="hljs-built_in">Math</span>.min(<span class="hljs-number">1.0</span>, (timestamp - startTime) / duration);

        update.call(self, easing ? easing(p) : p, p);

        <span class="hljs-keyword">if</span>(p &lt; <span class="hljs-number">1.0</span>){
          qId = requestAnimationFrame(step);
        }<span class="hljs-keyword">else</span>{
          resolve(self);
        }
      }

      self.cancel = <span class="hljs-function"><span class="hljs-keyword">function</span>(<span class="hljs-params"></span>)</span>{
        cancelAnimationFrame(qId);
        update.call(self, <span class="hljs-number">0</span>, <span class="hljs-number">0</span>);
        reject(<span class="hljs-string">'User canceled!'</span>);
      }

      qId = requestAnimationFrame(step);
    });
  },
  ease: <span class="hljs-function"><span class="hljs-keyword">function</span>(<span class="hljs-params">easing</span>)</span>{
    <span class="hljs-keyword">return</span> <span class="hljs-keyword">new</span> Animator(<span class="hljs-keyword">this</span>.duration, <span class="hljs-keyword">this</span>.update, easing);
  }
};

<span class="hljs-built_in">module</span>.exports = Animator;
</code></pre>
<p>Animator 构造的时候可以传三个参数，第一个是动画的总时长，第二个是动画每一帧的 update 事件，在这里可以改变元素的属性，从而实现动画。update 事件回调提供两个参数，第一个是 ep，是经过 easing 之后的动画进程，第二个是 p，是不经过 easing 的动画进程，ep 和 p 的值都是从 0 开始，到 1 结束。（为什么要使用 ep 和 p，在里已经说明了。）</p>
<p>Animator 有一个 animate 的对象方法，它返回一个 promise，当动画播放完成时，它的 promise 被 resolve，使用者还可以在 promise resolve 前调用 cancel 方法，这样它的 promise 会被 reject。</p>
<p>于是这样，很简单地我们就<strong>通过将 animator 封装为带有返回 Promise 接口的方法</strong>，实现了动画序列。它的实现虽然简单，但功能却是很强大的，用它实现的动画代码也很优雅：</p>
<p><script src="https:////code.h5jun.com/js/embed.min.js?3.40.2"></script></p>
<p>我们还提供了一个 ease 方法（0.2.0+版），能够传入新的 easing，并返回新的 Animator 对象，这样我们就可以在原动画的基础上扩展我们的动画效果：</p>
<p><script src="https:////code.h5jun.com/js/embed.min.js?3.40.2"></script></p>
<h2>用 CSS3 如何？</h2>
<p>的确，许多动画可以用 CSS3 来实现。不过 JavaScript 动画与 CSS3 动画有其不同的特点和使用场景。总体来说， CSS3 动画适用于任何纯展现效果的简单动画。虽然它也能提供基本的动画组合方法（有 animationEnd 时间，但标准化较晚），但操作起来依然不方便，而且还需要 JavaScript 来控制。有些动画库用降级的方式，能采用 CSS3 动画的采用 CSS3 动画，不能的自动降级为 JavaScript 动画，这不失为一种好方式，但也有利有弊。因为 CSS3 动画是绑定为操作元素属性的，而 JavaScript 更灵活一些。就像我们这个封装的动画库，其实提供的是更底层的 API，操作的只是<em>时间</em>和<em>进度</em>，并没有耦合任何元素、属性或者其他展示类的东西，因此它完全可以用来操作 DOM、Canvas、SVG、音频/视频流甚至是其他异步动作。另外，如果在动画过程中需要有其他一些精细的动作处理，也还是应该使用 JavaScript 动画而不是 CSS3 动画。</p>
<h2>总结</h2>
<p>使用 Promise 实现的简单动画库，能够很好地执行组合的时序动画，配合 async/await 代码实现简洁且优雅，同时还具有非常好的扩展性，能够组合出非常强大的动画效果。我相信这将成为未来浏览器上 JavaScript 动画的主要实现方式。</p>
<p>最后，可以访问  获取最新代码。</p>
---------------
<h1 id="#title_2" >3、迷你书： 阿里巴巴Java开发手册</h1>
阿里巴巴集团
[http://www.infoq.com/cn/minibooks/Alibaba-Java-minibook?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/minibooks/Alibaba-Java-minibook?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/minibooks/Alibaba-Java-minibook/zh/smallimage/100.jpg"/><p>《阿里巴巴Java开发手册》凝聚了阿里集团很多同学的知识智慧和经验，这些经验甚至是用血淋淋的故障换来的，希望前车之鉴，后车之师，能够帮助更多的开发者少踩坑，杜绝踩重复的坑。</p> <i>By 阿里巴巴集团</i>
---------------
<h1 id="#title_3" >4、视频访谈： 周梁伟：通信协议选型与三种类型的消息处理</h1>
周梁伟
[http://www.infoq.com/cn/interviews/interview-with-zhouliangwei-talk-protocol-and-message-process?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/interviews/interview-with-zhouliangwei-talk-protocol-and-message-process?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/interviews/interview-with-zhouliangwei-talk-protocol-and-message-process/zh/mediumimage/zhouliangwei270.jpg"/><p>消息通信是网易云信很重要的技术环节，网易云信的周梁伟老师分享了网易云信在消息中间件、协议方面的使用情况，介绍了Online、Nearline和Offline三种类型消息对应的技术处理，数据传输过程的加密处理和他们在负载均衡上的经验。</p> <i>By 周梁伟</i>
---------------
<h1 id="#title_4" >5、文章： 拥抱可变性</h1>
Enrique López Mañas
[http://www.infoq.com/cn/articles/learning-to-use-and-abuse-mutability?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/learning-to-use-and-abuse-mutability?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/learning-to-use-and-abuse-mutability/zh/smallimage/logo4.jpg"/><p>可变性是万恶之源？或许我们不能一刀切，看看作者怎么说。</p> <i>By Enrique López Mañas</i> <i> Translated by 薛命灯</i>
---------------
<h1 id="#title_5" >6、文章： 李大学：CTO，应该像CEO一样思考</h1>
李大学
[http://www.infoq.com/cn/articles/a-cto-should-think-like-ceo?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/a-cto-should-think-like-ceo?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/a-cto-should-think-like-ceo/zh/smallimage/machine_learning_logo.jpg"/><p>本文由李大学通过自身经历分享了为什么了CTO，应该像CEO一样思考。</p> <i>By 李大学</i>
---------------
<h1 id="#title_6" >7、文章： 当我们在谈大前端的时候，我们谈的是什么</h1>
徐川
[http://www.infoq.com/cn/articles/talking-about-daqianduan?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/talking-about-daqianduan?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/talking-about-daqianduan/zh/smallimage/nycc-icon-frontendCamp.jpg"/><p>上个月我在筹备GMTC2017大会的时候，走访了美团点评的刘平川老师、滴滴的左志鹏老师、手淘的天施老师，对大前端的问题进行了深入的讨论，在这里，我想用这样一篇文章来抛砖引玉，探讨大前端的定义。</p> <i>By 徐川</i>
---------------
<h1 id="#title_7" >8、DigitalOcean发布了高可用的托管负载均衡器</h1>
Elton Stoneman
[http://www.infoq.com/cn/news/2017/03/do-load-balancer-release?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/03/do-load-balancer-release?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>DigitalOcean发布了托管负载均衡器，扩展了他们的云服务产品。InfoQ就该负载均衡器的新特性和远景路线图采访了DigitalOcean的共同创始人Mitch Wainer。</p> <i>By Elton Stoneman</i> <i> Translated by Rays</i>
---------------
<h1 id="#title_8" >9、Bitbucket引入了强制双因素认证和IP白名单特性</h1>
Sergio De Simone
[http://www.infoq.com/cn/news/2017/03/bitbucket-improves-security?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/03/bitbucket-improves-security?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Atlassian宣布添加了两项新特性，致力于让Bitbucket更加安全：IP白名单和强制双因素认证。</p> <i>By Sergio De Simone</i> <i> Translated by 张卫滨</i>
---------------
<h1 id="#title_9" >10、Kubernetes部署失败的常见原因</h1>
Hrishikesh Barua
[http://www.infoq.com/cn/news/2017/03/common-kubernetes-fail-reasons?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/03/common-kubernetes-fail-reasons?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>最近一系列的文章重点介绍了Kubernetes部署失败的10种常见原因。这些原因涵盖了从缺少输入和错误输入，到超出资源限制。在大多数情况下，kubectl describe命令可以帮助确定背后的原因。</p> <i>By Hrishikesh Barua</i> <i> Translated by 谢旭</i>
---------------
<h1 id="#title_10" >11、视频演讲： 监控系统产品选型以及经验</h1>
尤勇
[http://www.infoq.com/cn/presentations/monitoring-system-product-selection-and-experience?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/monitoring-system-product-selection-and-experience?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/monitoring-system-product-selection-and-experience/zh/mediumimage/youyong1270.jpg"/><p>监控是个很宽泛的问题，里面涉及到快速的故障通知，精准的故障定位甚至包括可能性性能分析诊断。

监控这领域解决问题非常多，包括从移动，网络，业务，应用等各个方面，任何一个产品都需要有完备的监控，监控就像汽车行驶的方向盘，没有监控，很容易迷失方向。

这次演讲会从监控的各个层次，移动、应用等各个层次讲诉点评在监控领域做的工作以及一些实战经验，希望能让大家对今后的监控选型有所帮助。</p> <i>By 尤勇</i>
---------------
<h1 id="#title_11" >12、How To Deliver Large-Scale Projects Using A Content Hub Strategy</h1>
Sam Wright &#38; Chad Harwood-Jones
[https://www.smashingmagazine.com/2017/03/delivering-large-scale-projects-content-hub-strategy/](https://www.smashingmagazine.com/2017/03/delivering-large-scale-projects-content-hub-strategy/)
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
</table><p>What exactly are the <strong>benefits of a content hub strategy</strong>? Well, first of all, when done correctly, a content hub will capture a significant volume of traffic. And that's what most online businesses want, right?</p>

<figure></figure>

<p>We have recently introduced several clients to the concept of a content hub and would like to share our experience in this article. The clients are high-quality portals filled with targeted, valuable and often evergreen articles that users can return to time and again.</p><p>The post .</p>
---------------