## 文章索引
1、 <a href="#1building-production-ready-css-grid-layouts-today" >Building Production-Ready CSS Grid Layouts Today</a><br/>
2、 <a href="#2javascript-最新特性实现的三大黑科技" >JavaScript 最新特性实现的三大黑科技</a><br/>
3、 <a href="#3文章-微服务够了" >文章： 微服务，够了</a><br/>
4、 <a href="#4点融cto孔令欣技术不是最重要的领导力" >点融CTO孔令欣：技术不是最重要的领导力</a><br/>
5、 <a href="#5腾讯云答治茜云计算为独角兽和传统企业提供了哪些沃土" >腾讯云答治茜：云计算为独角兽和传统企业提供了哪些沃土？</a><br/>
6、 <a href="#62017年人工智能研究报告" >2017年人工智能研究报告</a><br/>
7、 <a href="#7android开发周报工信部欲统一推送标准android专家看kotlin" >Android开发周报：工信部欲统一推送标准、Android专家看Kotlin</a><br/>
8、 <a href="#8文章-facebook的开源大规模预测系统prophet怎么用" >文章： Facebook的开源大规模预测系统Prophet怎么用？</a><br/>
9、 <a href="#9renee-troughton访谈领导力的敏捷模式" >Renee Troughton访谈：领导力的敏捷模式</a><br/>
10、 <a href="#10stackoverflow转向默认使用https" >StackOverflow转向默认使用HTTPS</a><br/>
11、 <a href="#11arkit奠定了apple平台上实现ar的基石" >ARKit奠定了Apple平台上实现AR的基石</a><br/>
12、 <a href="#12aws-greengrass在iot设备上运行lambda函数" >AWS Greengrass：在IoT设备上运行Lambda函数</a><br/>
13、 <a href="#13树莓派新手入门教程" >树莓派新手入门教程</a><br/>
14、 <a href="#14ios-开发周报wwdc-2017了解-ios-11-sdk-新特性" >iOS 开发周报：WWDC 2017、了解 iOS 11 SDK 新特性</a><br/><h1 id="#title_0" >1、Building Production-Ready CSS Grid Layouts Today</h1>
Morten Rand-Hendriksen
[https://www.smashingmagazine.com/2017/06/building-production-ready-css-grid-layout/](https://www.smashingmagazine.com/2017/06/building-production-ready-css-grid-layout/)
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
</table><p>Industries often experience evolution less as slow and steady progress than as revolutionary shifts in modality that change best practices and methodologies seemingly overnight. This is most definitely true for front-end web development.</p>

<figure></figure>

<p>Our industry thrives on constant, aggressive development, and new technologies emerge on a regular basis that change the way we do things in fundamental ways.</p><p>The post .</p>
---------------
<h1 id="#title_1" >2、JavaScript 最新特性实现的三大黑科技</h1>

[https://www.h5jun.com/post/three-black-tech-in-modern-js.html](https://www.h5jun.com/post/three-black-tech-in-modern-js.html)
<div class="toc"><ul>
<li></li>
<li></li>
<li></li>
</ul>
</div><h2>依次执行多项异步任务</h2>
<p>有时候，我们希望批量执行一组异步任务，但是不是<strong>并行</strong>，而是依次执行，这组任务是动态的，在一个数组里，当然我们可以用 for 循环然后一个一个 await 执行，但是还有另外一种方式：</p>
<!--more-->
<p><script src="https:////code.h5jun.com/js/embed.min.js?3.40.2"></script></p>
<pre><code class="hljs lang-js"><span class="hljs-keyword">async</span> <span class="hljs-function"><span class="hljs-keyword">function</span> <span class="hljs-title">taskReducer</span>(<span class="hljs-params">promise, action</span>)</span>{
  <span class="hljs-keyword">let</span> res = <span class="hljs-keyword">await</span> promise;
  <span class="hljs-keyword">return</span> action(res);
}

<span class="hljs-function"><span class="hljs-keyword">function</span> <span class="hljs-title">sleep</span>(<span class="hljs-params">ms</span>)</span>{
  <span class="hljs-keyword">return</span> <span class="hljs-keyword">new</span> <span class="hljs-built_in">Promise</span>(resolve =&gt; setTimeout(resolve, ms));
}

<span class="hljs-keyword">async</span> <span class="hljs-function"><span class="hljs-keyword">function</span> <span class="hljs-title">asyncTask</span>(<span class="hljs-params">i</span>)</span>{
  <span class="hljs-keyword">await</span> sleep(<span class="hljs-number">500</span>);
  <span class="hljs-built_in">console</span>.log(<span class="hljs-string">`task <span class="hljs-subst">${i}</span> done`</span>);
  <span class="hljs-keyword">return</span> ++i;
}


[asyncTask, asyncTask, asyncTask].reduce(taskReducer, <span class="hljs-number">0</span>);
</code></pre>
<p>在上面的例子里，我们定义了一个 taskReducer：</p>
<pre><code class="hljs lang-js"><span class="hljs-keyword">async</span> <span class="hljs-function"><span class="hljs-keyword">function</span> <span class="hljs-title">taskReducer</span>(<span class="hljs-params">promise, action</span>)</span>{
  <span class="hljs-keyword">let</span> res = <span class="hljs-keyword">await</span> promise;
  <span class="hljs-keyword">return</span> action(res);
}
</code></pre>
<p>这个 reducer 的两个参数是 promise 和 action，promise 是代表当前任务的 promise，而 action 是下一个要执行的任务。我们可以 await 当前 promise 执行当前任务，然后将执行结果传给下一个 action 就可以了。</p>
<p>这样我们可以调用：</p>
<pre><code class="hljs lang-undefined">[task1, task2, task3, ...].reduce(taskReducer, init);
</code></pre>
<p>不管这些任务是同步还是异步都可以被<strong>依次执行</strong>。需要注意的是，每一个任务的返回值将是下一个任务的输入 promise 或者 value。 </p>
<h2>generator 与 async/await 一同使用</h2>
<p>将上面的代码进一步扩展，我们发现，它可以支持 generator 与 async/await 一同使用：</p>
<p><script src="https://code.h5jun.com/js/embed.min.js?3.40.2"></script></p>
<pre><code class="hljs lang-js"><span class="hljs-keyword">async</span> <span class="hljs-function"><span class="hljs-keyword">function</span> <span class="hljs-title">reducer</span>(<span class="hljs-params">promise, action</span>)</span>{
  <span class="hljs-keyword">let</span> res = <span class="hljs-keyword">await</span> promise;
  <span class="hljs-keyword">return</span> action(res);
}

<span class="hljs-function"><span class="hljs-keyword">function</span> <span class="hljs-title">tick</span>(<span class="hljs-params">i</span>)</span>{
  <span class="hljs-built_in">console</span>.log(i);
  <span class="hljs-keyword">return</span> <span class="hljs-keyword">new</span> <span class="hljs-built_in">Promise</span>(resolve =&gt; setTimeout(()=&gt;resolve(++i), <span class="hljs-number">1000</span>));
}

<span class="hljs-function"><span class="hljs-keyword">function</span> <span class="hljs-title">continuous</span>(<span class="hljs-params">...functors</span>)</span>{
  <span class="hljs-keyword">return</span> <span class="hljs-keyword">async</span> <span class="hljs-function"><span class="hljs-keyword">function</span>(<span class="hljs-params">input</span>)</span>{
    <span class="hljs-keyword">return</span> <span class="hljs-keyword">await</span> functors.reduce(reducer, input)
  }
}

<span class="hljs-function"><span class="hljs-keyword">function</span> * <span class="hljs-title">timing</span>(<span class="hljs-params">count = 5</span>)</span>{
  <span class="hljs-keyword">for</span>(<span class="hljs-keyword">let</span> i = <span class="hljs-number">0</span>; i &lt; count; i++){
    <span class="hljs-keyword">yield</span> tick;
  }
}

continuous(...timing(<span class="hljs-number">10</span>))(<span class="hljs-number">0</span>);
</code></pre>
<p>在上面的例子里，我们定义了一个计时 tick 函数，我们通过 timing 来连续调用它，而 timing 是一个 generator，计时器显然是异步函数，然而我们可以：</p>
<pre><code class="hljs lang-undefined">continuous(...timing(10))(0);
</code></pre>
<p>而这里的 continuous 其实就是前面的 reduce 的封装。</p>
<h2>使用 Proxy 实现 PHP 中的常用“魔术方法”</h2>
<p>PHP 中有 <code>__get</code> 、 <code>__set</code> 和 <code>__call</code> 三个强大的魔术方法，可以实现对不存在的属性的读写和方法调用。在新的 ES 标准中添加了 Proxy 类，它可以构造 Proxy 对象，用来“重载”对象的属性和方法读写，从而实现类似于 PHP 的魔术方法：</p>
<p><script src="https:////code.h5jun.com/js/embed.min.js?3.40.2"></script></p>
<pre><code class="hljs lang-js"><span class="hljs-function"><span class="hljs-keyword">function</span> <span class="hljs-title">Magical</span>(<span class="hljs-params">Class</span>)</span>{
  <span class="hljs-keyword">return</span> <span class="hljs-function"><span class="hljs-keyword">function</span>(<span class="hljs-params">...args</span>)</span>{
    <span class="hljs-keyword">return</span> <span class="hljs-keyword">new</span> <span class="hljs-built_in">Proxy</span>(<span class="hljs-keyword">new</span> Class(...args), {
      get: <span class="hljs-function"><span class="hljs-keyword">function</span>(<span class="hljs-params">target, key, receiver</span>) </span>{
        <span class="hljs-keyword">if</span>(<span class="hljs-keyword">typeof</span> target[key] !== <span class="hljs-string">'undefined'</span>){
          <span class="hljs-keyword">return</span> target[key];
        }

        <span class="hljs-keyword">if</span> (<span class="hljs-keyword">typeof</span> target.__get === <span class="hljs-string">'function'</span>){
          <span class="hljs-keyword">return</span> target.__get(key);
        } <span class="hljs-keyword">else</span> <span class="hljs-keyword">if</span> (<span class="hljs-keyword">typeof</span> target.__call === <span class="hljs-string">'function'</span>) {
          <span class="hljs-keyword">return</span> <span class="hljs-function"><span class="hljs-keyword">function</span>(<span class="hljs-params">...args</span>)</span>{
            target.__call.apply(<span class="hljs-keyword">this</span>, [key, ...args]);
          };
        } 
      },
      set: <span class="hljs-function"><span class="hljs-keyword">function</span>(<span class="hljs-params">target, key, value, receiver</span>)</span>{
        <span class="hljs-keyword">if</span>(<span class="hljs-keyword">typeof</span> target[key] !== <span class="hljs-string">'undefined'</span>){
          target[key] = value;
          <span class="hljs-keyword">return</span>;
        }

        <span class="hljs-keyword">if</span> (<span class="hljs-keyword">typeof</span> target.__set === <span class="hljs-string">'function'</span>){
          target.__set(key, value);
          <span class="hljs-keyword">return</span>;
        }
      }
    });
  }
}

<span class="hljs-class"><span class="hljs-keyword">class</span> <span class="hljs-title">Foo</span></span>{
  __set(key, value){
    <span class="hljs-keyword">this</span>[key] = value * <span class="hljs-number">2</span>;
  }
  __get(key){
    <span class="hljs-keyword">return</span> <span class="hljs-keyword">this</span>.b;
  }
  __call(key, ...args){
    <span class="hljs-built_in">console</span>.log(<span class="hljs-string">`call method <span class="hljs-subst">${key}</span> with <span class="hljs-subst">${args}</span>`</span>);
  }
  b(...args){
    <span class="hljs-built_in">console</span>.log(<span class="hljs-string">`b exists: <span class="hljs-subst">${args}</span>`</span>);
  }
}

Foo = Magical(Foo);

<span class="hljs-keyword">var</span> f = <span class="hljs-keyword">new</span> Foo();
f.b(<span class="hljs-number">1</span>,<span class="hljs-number">2</span>,<span class="hljs-number">3</span>);
f.a(<span class="hljs-number">4</span>,<span class="hljs-number">5</span>,<span class="hljs-number">6</span>);
f.c = <span class="hljs-number">3</span>;
<span class="hljs-built_in">console</span>.log(f.c);
</code></pre>
<p>上面的例子里，我们在对象构造的时候，分别“代理”对象实例的属性 get 和 set 方法，如果对象上已存在某个属性或方法，代理直接返回或操作该属性。否则，判断对象上是否有 <code>__get</code>、<code>__set</code> 或者 <code>__call</code> 方法，有的话，做相应的处理。</p>
<p>这里我们使用装饰器模式，定义了一个 Magical 装饰器函数，让它来处理希望使用 Magical 的类。</p>
<p>等到  标准化了之后，我们就可以使用更加优雅的写法了：</p>
<pre><code class="hljs lang-js">@magical
<span class="hljs-class"><span class="hljs-keyword">class</span> <span class="hljs-title">Foo</span> </span>{
    __call(key, ...args){
        ...
    }
}
</code></pre>
<hr>
<p>以上就是今天的所有内容。ES 的新特性为我们提供了非常强大的功能，让我们能够更加优雅地写代码。有任何问题，欢迎留言讨论。</p>
---------------
<h1 id="#title_2" >3、文章： 微服务，够了</h1>
Adam Drake
[http://www.infoq.com/cn/articles/micro-service-is-enough?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/micro-service-is-enough?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/micro-service-is-enough/zh/smallimage/logo-1 (2).jpg"/><p>资深架构师Adam Drake在他的博客上分享了他对微服务的看法，他从自己的经验出发，结合Martin Fowler对微服务的见解，帮助想要采用微服务的公司重新审视微服务。以下内容已获得作者翻译授权，查看英文原文 Enough with the microservices。</p> <i>By Adam Drake</i> <i> Translated by 薛命灯</i>
---------------
<h1 id="#title_3" >4、点融CTO孔令欣：技术不是最重要的领导力</h1>
陈园园
[http://www.infoq.com/cn/news/2017/06/EGO-GTLC?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/06/EGO-GTLC?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>点融CTO孔令欣：技术不是最重要的领导力。</p> <i>By 陈园园</i>
---------------
<h1 id="#title_4" >5、腾讯云答治茜：云计算为独角兽和传统企业提供了哪些沃土？</h1>
腾讯云
[http://www.infoq.com/cn/news/2017/06/qcloud-provides-tech-service?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/06/qcloud-provides-tech-service?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>云计算可以轻松实现弹性扩展，也可以随时扩容以应对互联网流量的变化。云计算技术正在改变企业业务模式、支撑业务增长的主导力量，同时带来更有前景的商业机会。</p> <i>By 腾讯云</i>
---------------
<h1 id="#title_5" >6、2017年人工智能研究报告</h1>
薛命灯
[http://www.infoq.com/cn/news/2017/06/Artificial-Intelligence-Report-2?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/06/Artificial-Intelligence-Report-2?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>来自Cowen公司的一份关于人工智能的研究报告——“人工智能：数据科学的黄金时期”。</p> <i>By 薛命灯</i>
---------------
<h1 id="#title_6" >7、Android开发周报：工信部欲统一推送标准、Android专家看Kotlin</h1>
郭亮
[http://www.infoq.com/cn/news/2017/06/Android-weekly-gongxinbu?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/06/Android-weekly-gongxinbu?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>6月最新安卓各版本份额：牛轧糖达9.5%，暴增34.8%。工信部放大招，未来国内安卓生态或将统一消息推送标准。本期周报为大家带来了Kotlin、微信移动端数据库WCDB、热修复等技术干货，欢迎阅读。</p> <i>By 郭亮</i>
---------------
<h1 id="#title_7" >8、文章： Facebook的开源大规模预测系统Prophet怎么用？</h1>
杨旸
[http://www.infoq.com/cn/articles/facebook-open-source-mass-forecasting-system-prophet?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/facebook-open-source-mass-forecasting-system-prophet?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/facebook-open-source-mass-forecasting-system-prophet/zh/smallimage/logo1 (1).jpg"/><p>本文将结合Facebook的开源预测系统Prophet，介绍时序分析的基本概念和方法。为从事时序分析，或使用开源预测工具的朋友，提供参考。</p> <i>By  杨旸</i>
---------------
<h1 id="#title_8" >9、Renee Troughton访谈：领导力的敏捷模式</h1>
Shane Hastie, Hugo Messer
[http://www.infoq.com/cn/news/2017/06/troughton-leadership-agility?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/06/troughton-leadership-agility?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/news/2017/06/troughton-leadership-agility/zh/headerimage/GettyImages-481096541.jpg"/><p>Renee Troughton将在即将召开的印尼敏捷大会上发表演讲，主题是使用系统思维进行组织变革。成功实现敏捷所面临的挑战并不是让团队开始敏捷或Scrum，而是在系统重建旧有政策与约束之前改革它们。她同InfoQ谈及了这些内容与领导力模式的话题。</p> <i>By Shane Hastie</i> <i> Translated by 王强</i>
---------------
<h1 id="#title_9" >10、StackOverflow转向默认使用HTTPS</h1>
Andrew Morgan
[http://www.infoq.com/cn/news/2017/06/stackoverflow-https?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/06/stackoverflow-https?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/news/2017/06/stackoverflow-https/zh/headerimage/GettyImages-638966228.jpg"/><p>StackOverflow的首席架构师Nick Craver发表了一篇博文，宣布StackOverflow迁移到HTTPS。在该过程中，他们经历了一些技术挑战，包括对数百个域的支持、URL迁移、用户生成内容处理，以及如何达到网站所需的严格性能需求。</p> <i>By Andrew Morgan</i> <i> Translated by Rays</i>
---------------
<h1 id="#title_10" >11、ARKit奠定了Apple平台上实现AR的基石</h1>
Sergio De Simone
[http://www.infoq.com/cn/news/2017/06/ios-augmented-reality-arkit?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/06/ios-augmented-reality-arkit?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/news/2017/06/ios-augmented-reality-arkit/zh/headerimage/GettyImages-625873008.jpg"/><p>在WWDC 2017大会上，Apple公布了ARKit。ARKit是一种为iOS构建增强现实App的框架，意在实现将虚拟内容精确且真实地浸入真实世界场景上。</p> <i>By Sergio De Simone</i> <i> Translated by Rays</i>
---------------
<h1 id="#title_11" >12、AWS Greengrass：在IoT设备上运行Lambda函数</h1>
Abel Avram
[http://www.infoq.com/cn/news/2017/06/aws-greengrass?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/06/aws-greengrass?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Amazon提供了一个可以让开发者在IoT设备上运行Lambda函数的解决方案——AWS Greengrass，它让设备可以与云以及其他设备进行通信。</p> <i>By Abel Avram</i> <i> Translated by 李梦</i>
---------------
<h1 id="#title_12" >13、树莓派新手入门教程</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2017/06/raspberry-pi-tutorial.html](http://www.ruanyifeng.com/blog/2017/06/raspberry-pi-tutorial.html)
<p>（Raspberry Pi）是学习计算机知识、架设服务器的好工具，价格低廉，可玩性高。</p>

        <p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017061501.png" alt="" title="" /></p>

<p>本文根据我的亲身经验，介绍如何从零开始，搭建一个树莓派服务器，控制 LED 灯。你会看到，树莓派玩起来实在很容易。</p>

<p>我要感谢 。</p>

<h2>一、型号</h2>

<p>树莓派是一个迷你电脑，集成在一块电路板。目前，最新的型号有两个。</p>

<p>（1）Raspberry Pi 3代 B 型 </p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017061502.jpg" alt="" title="" /></p>

<p>（2）Raspberry Pi zero （含 zero w）</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017061503.jpg" alt="" title="" /></p>

<p>虽然后者便宜，但是少了许多接口（比如只有一个 USB 口），CPU 和内存都比较低，配件也少，因此推荐购买第3代的 B 型。以下都针对这个型号，但大部分内容对 zero 也适用。</p>

<h2>二、配件</h2>

<p>树莓派本身只是一个主机。要运行起来，必须有配件。</p>

<p>（1）电源</p>

<p>Micro USB 接口的手机充电器，就可以充当电源，但输出必须是 5V 电压、至少 2A 电流。充电宝当电源也没问题。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017061504.jpg" alt="" title="" /></p>

<p>（2）Micro SD 卡</p>

<p>树莓派不带硬盘，Micro SD 卡就是硬盘。最小容量8G，推荐使用16G和32G的卡。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017061506.jpg" alt="" title="" /></p>

<p>（3）显示器</p>

<p>树莓派有 HDMI 输出，显示器必须有该接口。如果有 HDMI 转 VGA 的转接线，那么 VGA 显示器也可以。我用的是一个 7 寸的液晶监视器。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017061507.jpg" alt="" title="" /></p>

<p>不过，显示器只在安装系统时需要，后面可以  登录，就不需要了。</p>

<p>（4）无线键鼠</p>

<p>树莓派内置蓝牙，USB 或蓝牙的无线键鼠都可以用。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017061508.jpg" alt="" title="" /></p>

<p>就像显示器一样，如果树莓派已经装好系统，而且只当作服务器，无线键鼠也可以不配。</p>

<h2>三、电子元件</h2>

<p>除了配件，下面的实验还需要一些电子元件。</p>

<p>（1）面包板（一块）</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017061509.jpg" alt="" title="" /></p>

<p>（2）连接线（若干）</p>

<p>注意，连接线必须一端是公头，一端是母头。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017061510.jpg" alt="" title="" /></p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017061511.jpg" alt="" title="" /></p>

<p>另外，最好也备一些两端都是公头的连接线。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017061512.jpg" alt="" title="" /></p>

<p>（3）LED 二极管（若干）</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017061512.gif" alt="" title="" /></p>

<p>（4）270欧姆的电阻（若干）</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017061513.jpg" alt="" title="" /></p>

<h2>四、安装系统</h2>

<p>如果商家已经装好系统，可以跳过这一步，否则需要自己安装操作系统。</p>

<p>官方提供的操作系统是 ，这是 Debian 系统的定制版。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017061514.png" alt="" title="" /></p>

<p>官方还提供一个安装器 ，建议通过它来安装 Raspbian，相对简单一点。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017061515.png" alt="" title="" /></p>

<blockquote>
  <ol start='1'>
<li>。</li>
<li>格式化 Micro SD 卡为 FAT 格式（）。</li>
<li>解压<code>NOOBS.zip</code>到 Micro SD 卡根目录。</li>
<li>插入 Micro SD 卡到树莓派底部的卡槽，接通电源，启动系统。</li>
</ol>
</blockquote>

<p>正常情况下，按照屏幕上的提示，一路回车，就能装好系统。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017061516.png" alt="" title="" /></p>

<h2>五、SSH 登录</h2>

<p>安装系统后，树莓派就可以上网了（Wifi 或者网线）。这时，你要看一下它的局域网 IP 地址，可以使用下面的命令。</p>

<blockquote><pre><code class="language-bash">
$ sudo ifconfig
</code></pre></blockquote>

<p>然后，从另一台电脑 SSH 登录树莓派。下面的命令是在局域网的另一台电脑上执行的。</p>

<blockquote><pre><code class="language-bash">
$ ssh pi@192.168.1.5
</code></pre></blockquote>

<p>上面代码中，<code>192.168.1.5</code>是我的树莓派的地址，你要换成你的地址。树莓派的默认用户是<code>pi</code>。</p>

<p>树莓派会提示你输入密码。<code>pi</code>的默认密码是<code>raspberry</code>。正常情况下，这样就可以登录树莓派了。接着，就可以进行各种服务器了，比如修改密码。</p>

<blockquote><pre><code class="language-bash">
$ passwd
</code></pre></blockquote>

<p>后面的实验需要将用户加入<code>gpio</code>用户组。</p>

<blockquote><pre><code class="language-bash">
$ sudo adduser pi gpio
</code></pre></blockquote>

<p>上面的代码表示将用户<code>pi</code>加入<code>gpio</code>用户组。</p>

<h2>六、安装 Node</h2>

<p>为了运行 Node 脚本，树莓派必须安装 Node，可以参考。</p>

<blockquote><pre><code class="language-bash">
$ curl -sL https://deb.nodesource.com/setup_8.x | sudo -E bash -
$ sudo apt install nodejs
</code></pre></blockquote>

<p>正常情况下，Node 8.x 版就已经安装成功了。</p>

<blockquote><pre><code class="language-bash">
$ node -v
v8.1.0
</code></pre></blockquote>

<h2>七、点亮 LED</h2>

<p>树莓派提供了一组对外的 IO 接口，称为 GPIO（ 通用 IO 接口，General-purpose input/output）。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017061518.png" alt="" title="" /></p>

<p>它的 40 个脚的定义如下图。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017061519.png" alt="" title="" /></p>

<p>注意，左上角的第1针（3.3V）是一个方块，其他针脚都是圆的。将树莓派翻过来，背后可以看到 GPIO 有一个角是方的，通过这种方法就可以确认哪一个针眼是3.3V。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017061516.jpg" alt="" title="" /></p>

<p>通过 GPIO ，树莓派可以与其他电子元件连接。下面根据 Jonathan Perkin 的，使用树莓派连接 LED 二极管。</p>

<p>这里需要用到面包板。本质上，面包板就是几根导线，上面开了许多可以连到导线的孔。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017061519.jpg" alt="" title="" /></p>

<p><code>+</code>极和<code>-</code>极是两根垂直的导线，标着<code>1</code>、<code>5</code>、<code>10</code>这些数字的行，每一行都是一根水平的导线。导线与导线之间互不连接，另外，面包板的左右两半也是互不连接的。</p>

<p>然后，按照下面的图，将树莓派、面包板、LED 灯、电阻连起来。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017061520.jpg" alt="" title="" /></p>

<p>上图中，红色导线表示电流的正极，从 GPIO 的第1针（3.3V）连到面包板。黑色导线表示电流的负极，从 GPIO 第三排的第6针（ground）连到面包板。它们连到面包板的哪个眼并不重要，但必须保证能组成一个完整的电路（上图的箭头流向）。注意，LED 二极管也有正负极，长脚表示正极，短脚表示负极。电阻没有正负极。</p>

<p>连接完成后，打开树莓派的电源，LED 应该就会亮起来了。</p>

<h2>八、LED 控制脚本</h2>

<p>下面，我们使用 Node 脚本控制 LED。</p>

<p>首先，将正极的导线从1号针脚（3.3V）拔出，插到第6排的11号针脚（上图的 GPIO 17）。这个针脚的电流是脚本可以控制的。</p>

<p>然后，在树莓派上新建一个实验目录，并安装控制 GPIO 的 Node 模块。。</p>

<blockquote><pre><code class="language-bash">
$ mkdir led-demo && cd led-demo
$ npm init -y
$ npm install -S rpio
</code></pre></blockquote>

<p>接着，新建一个脚本。</p>

<blockquote><pre><code class="language-javascript">
// led-on.js
var rpio = require('rpio');

// 打开 11 号针脚（GPIO17) 作为输出
rpio.open(11, rpio.OUTPUT);

// 指定 11 号针脚输出电流（HIGH）
rpio.write(11, rpio.HIGH);
</code></pre></blockquote>

<p>运行这个脚本，应该就会看到 LED 灯泡变亮了。</p>

<blockquote><pre><code class="language-bash">
$ node led-on.js
</code></pre></blockquote>

<p>再新建一个<code>led-off.js</code>脚本，只要改一行（完整代码看）。</p>

<blockquote><pre><code class="language-javascript">
// led-off.js
//...

// 指定 11 号针脚停止输出电流（LOW）
rpio.write(11, rpio.LOW);
</code></pre></blockquote>

<p>运行这个脚本，LED 灯泡应该就会熄灭了。</p>

<blockquote><pre><code class="language-bash">
$ node led-off.js
</code></pre></blockquote>

<p>有了这两个脚本，让 LED 闪烁就轻而易举了。新建一个脚本。</p>

<blockquote><pre><code class="language-javascript">
// led-blink.js
var rpio = require('rpio');
rpio.open(11, rpio.OUTPUT);

function blink() {
  rpio.write(11, rpio.HIGH);
  setTimeout(function ledoff() {
    rpio.write(11, rpio.LOW);
  }, 50);
}

setInterval(blink, 100);
</code></pre></blockquote>

<p>上面的脚本让 LED 每秒闪烁10次。</p>

<blockquote><pre><code class="language-bash">
$ node led-blink.js
</code></pre></blockquote>

<h2>九、HTTP 服务器</h2>

<p>通过控制 LED 可以做很多事，比如架设一个 HTTP 服务器，每当有人访问，LED 就闪烁一下。</p>

<p>首先，在刚才的目录里面装一个服务器模块。</p>

<blockquote><pre><code class="language-bash">
$ npm install -S server
</code></pre></blockquote>

<p>然后，新建一个脚本<code>server.js</code>（完整代码看）。</p>

<blockquote><pre><code class="language-javascript">
// server.js
var server = require('server');
var { get } = server.router;

// ...

server({ port: 8080 }, [
  get('/' ,  ctx => {
    console.log('a request is coming...');
    blink();
  }),
]);

console.log('server starts on 8080 port');
</code></pre></blockquote>

<p>运行这个脚本。</p>

<blockquote><pre><code class="language-bash">
$ node server.js
</code></pre></blockquote>

<p>然后，再打开一个命令行终端，访问8080端口，LED 就会闪一下。</p>

<blockquote><pre><code class="language-bash">
$ curl http://localhost:8080
</code></pre></blockquote>

<p>好了，今天的教程就到这里。接下来，你可以自己探索，做更多的尝试，比如写一个。</p>

<p>（正文完）</p>

<p>================================</p>

<p></p>

<p>下面是推广时间，向大家推荐求职就业的好帮手----。</p>

<p>如果你对现在工作不甚满意，希望寻找更好的职位，或者你已经有了很多工作邀请，感到无所适从，不知道哪个最合适自己，请尝试一下 。它能让你节省精力，从海量机会中找到最适合自己的那个。</p>

<p></p>

<p>注册，提交资料并通过网站对您的评估和配对后，就可以收获 5～10 个满足你要求的好机会。</p>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2017-06-15T17:41:51+08:00">2017年6月15日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>博客文集：</li>
<li>社交媒体：</li>
<li>Feed订阅： </li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------
<h1 id="#title_13" >14、iOS 开发周报：WWDC 2017、了解 iOS 11 SDK 新特性</h1>
靛青K
[http://www.infoq.com/cn/news/2017/06/iOS-weekly-wwdc-2017-ios-11-sdk?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/06/iOS-weekly-wwdc-2017-ios-11-sdk?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>WWDC 2017、了解 iOS 11 SDK 新特性</p> <i>By 靛青K</i>
---------------