## 文章索引
1、 <a href="#1how-we-built-an-ios-app-to-shoot-a-3d-video-case-study" >How We Built An iOS App To Shoot A 3D Video (Case Study)</a><br/>
2、 <a href="#2神经网络入门" >神经网络入门</a><br/>
3、 <a href="#3视频演讲-百度外卖从-idc-到云端服务迁移历程" >视频演讲： 百度外卖从 IDC 到云端服务迁移历程</a><br/>
4、 <a href="#4文章-如何有效地收集移动应用中的用户反馈" >文章： 如何有效地收集移动应用中的用户反馈</a><br/>
5、 <a href="#5视频演讲-百度超大规模低成本对象存储-bos构建之路" >视频演讲： 百度超大规模低成本对象存储-BOS构建之路</a><br/>
6、 <a href="#6文章-虚拟研讨会数据科学机器学习深度学习人工智能及企业开发人员" >文章： 虚拟研讨会：数据科学、机器学习、深度学习、人工智能及企业开发人员</a><br/>
7、 <a href="#7文章-如何使用kubernetes-gpu集群自动化深度学习训练" >文章： 如何使用Kubernetes GPU集群自动化深度学习训练</a><br/>
8、 <a href="#8rust语言2017路线图半年回顾" >Rust语言2017路线图半年回顾</a><br/>
9、 <a href="#9从java到spring为何独得青睐spring-summit-2017不可不知的那些事儿" >从Java到Spring为何独得青睐Spring Summit 2017不可不知的那些事儿</a><br/><h1 id="#title_0" >1、How We Built An iOS App To Shoot A 3D Video (Case Study)</h1>
Evgeny Khrolenok &#38; Igor Mikheiko
[https://www.smashingmagazine.com/2017/07/ios-app-3d-video-case-study/](https://www.smashingmagazine.com/2017/07/ios-app-3d-video-case-study/)
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
</table><p>It wasn’t long after Hollywood released its first 3D films that the movie format quickly gained huge popularity worldwide. Thanks to developments in video-recording technology, any user can now shoot a video on their own. You can make a stereo record of memorable events in your life or create wonderful material for your business.</p>

<figure></figure>

<p>Our team was also attracted to 3D filming. We thoroughly studied the features of the human visual apparatus and the technical details of stereoscopic photography. Then, we decided to develop an iOS app to shoot 3D videos and upload the videos to YouTube. The idea behind the app was to facilitate the shooting of 3D video by mounting two iPhones to a special frame — and we did it! That was how the <em>Stereo Video Recorder</em> app appeared.</p><p>The post .</p>
---------------
<h1 id="#title_1" >2、神经网络入门</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2017/07/neural-network.html](http://www.ruanyifeng.com/blog/2017/07/neural-network.html)
<p>眼下最热门的技术，绝对是人工智能。</p>

        <p>人工智能的底层模型是（neural network）。许多复杂的应用（比如模式识别、自动控制）和高级模型（比如深度学习）都基于它。学习人工智能，一定是从它开始。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017071201.jpg" alt="" title="" /></p>

<p>什么是神经网络呢？网上似乎通俗的解释。</p>

<p>前两天，我读到 Michael Nielsen 的开源教材（Neural Networks and Deep Learning），意外发现里面的解释非常好懂。下面，我就按照这本书，介绍什么是神经网络。</p>

<p>这里我要感谢课程的消息，欢迎关注。</p>

<h2>一、感知器</h2>

<p>历史上，科学家一直希望模拟人的大脑，造出可以思考的机器。人为什么能够思考？科学家发现，原因在于人体的神经网络。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017071212.png" alt="" title="" /></p>

<blockquote>
  <ol start='1'>
<li>外部刺激通过神经末梢，转化为电信号，转导到神经细胞（又叫神经元）。</li>
<li>无数神经元构成神经中枢。</li>
<li>神经中枢综合各种信号，做出判断。</li>
<li>人体根据神经中枢的指令，对外部刺激做出反应。</li>
</ol>
</blockquote>

<p>既然思考的基础是神经元，如果能够"人造神经元"（artificial neuron），就能组成人工神经网络，模拟思考。上个世纪六十年代，提出了最早的"人造神经元"模型，叫做（perceptron），直到今天还在用。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017071202.png" alt="" title="" /></p>

<p>上图的圆圈就代表一个感知器。它接受多个输入（x1，x2，x3...），产生一个输出（output），好比神经末梢感受各种外部环境的变化，最后产生电信号。</p>

<p>为了简化模型，我们约定每种输入只有两种可能：1 或 0。如果所有输入都是1，表示各种条件都成立，输出就是1；如果所有输入都是0，表示条件都不成立，输出就是0。</p>

<h2>二、感知器的例子</h2>

<p>下面来看一个例子。城里正在举办一年一度的游戏动漫展览，小明拿不定主意，周末要不要去参观。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017071213.jpg" alt="" title="" /></p>

<p>他决定考虑三个因素。</p>

<blockquote>
  <ol start='1'>
<li>天气：周末是否晴天？</li>
<li>同伴：能否找到人一起去？</li>
<li>价格：门票是否可承受？</li>
</ol>
</blockquote>

<p>这就构成一个感知器。上面三个因素就是外部输入，最后的决定就是感知器的输出。如果三个因素都是 Yes（使用<code>1</code>表示），输出就是1（去参观）；如果都是 No（使用<code>0</code>表示），输出就是0（不去参观）。</p>

<h2>三、权重和阙值</h2>

<p>看到这里，你肯定会问：如果某些因素成立，另一些因素不成立，输出是什么？比如，周末是好天气，门票也不贵，但是小明找不到同伴，他还要不要去参观呢？</p>

<p>现实中，各种因素很少具有同等重要性：某些因素是决定性因素，另一些因素是次要因素。因此，可以给这些因素指定权重（weight），代表它们不同的重要性。</p>

<blockquote>
  <ul>
<li>天气：权重为8</li>
<li>同伴：权重为4</li>
<li>价格：权重为4</li>
</ul>
</blockquote>

<p>上面的权重表示，天气是决定性因素，同伴和价格都是次要因素。</p>

<p>如果三个因素都为1，它们乘以权重的总和就是 8 + 4 + 4 = 16。如果天气和价格因素为1，同伴因素为0，总和就变为 8 + 0 + 4 = 12。</p>

<p>这时，还需要指定一个阈值（threshold）。如果总和大于阈值，感知器输出1，否则输出0。假定阈值为8，那么 12 > 8，小明决定去参观。阈值的高低代表了意愿的强烈，阈值越低就表示越想去，越高就越不想去。</p>

<p>上面的决策过程，使用数学表达如下。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017071203.png" alt="" title="" /></p>

<p>上面公式中，<code>x</code>表示各种外部因素，<code>w</code>表示对应的权重。</p>

<h2>四、决策模型</h2>

<p>单个的感知器构成了一个简单的决策模型，已经可以拿来用了。真实世界中，实际的决策模型则要复杂得多，是由多个感知器组成的多层网络。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017071205.png" alt="" title="" /></p>

<p>上图中，底层感知器接收外部输入，做出判断以后，再发出信号，作为上层感知器的输入，直至得到最后的结果。（注意：感知器的输出依然只有一个，但是可以发送给多个目标。）</p>

<p>这张图里，信号都是单向的，即下层感知器的输出总是上层感知器的输入。现实中，有可能发生循环传递，即 A 传给 B，B 传给 C，C 又传给 A，这称为（recurrent neural network），本文不涉及。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017071211.png" alt="" title="" /></p>

<h2>五、矢量化</h2>

<p>为了方便后面的讨论，需要对上面的模型进行一些数学处理。</p>

<blockquote>
  <ul>
<li>外部因素 <code>x1</code>、<code>x2</code>、<code>x3</code> 写成矢量 <code>&lt;x1, x2, x3&gt;</code>，简写为 <code>x</code></li>
<li>权重 <code>w1</code>、<code>w2</code>、<code>w3</code> 也写成矢量 <code>(w1, w2, w3)</code>，简写为 <code>w</code></li>
<li>定义运算 <code>w⋅x = ∑ wx</code>，即 <code>w</code> 和 <code>x</code> 的点运算，等于因素与权重的乘积之和</li>
<li>定义 <code>b</code> 等于负的阈值 <code>b = -threshold</code></li>
</ul>
</blockquote>

<p>感知器模型就变成了下面这样。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017071206.png" alt="" title="" /></p>

<h2>六、神经网络的运作过程</h2>

<p>一个神经网络的搭建，需要满足三个条件。</p>

<blockquote>
  <ul>
<li>输入和输出</li>
<li>权重（<code>w</code>）和阈值（<code>b</code>）</li>
<li>多层感知器的结构</li>
</ul>
</blockquote>

<p>也就是说，需要事先画出上面出现的那张图。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017071205.png" alt="" title="" /></p>

<p>其中，最困难的部分就是确定权重（<code>w</code>）和阈值（<code>b</code>）。目前为止，这两个值都是主观给出的，但现实中很难估计它们的值，必需有一种方法，可以找出答案。</p>

<p>这种方法就是试错法。其他参数都不变，<code>w</code>（或<code>b</code>）的微小变动，记作<code>Δw</code>（或<code>Δb</code>），然后观察输出有什么变化。不断重复这个过程，直至得到对应最精确输出的那组<code>w</code>和<code>b</code>，就是我们要的值。这个过程称为模型的训练。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017071207.png" alt="" title="" /></p>

<p>因此，神经网络的运作过程如下。</p>

<blockquote>
  <ol start='1'>
<li>确定输入和输出</li>
<li>找到一种或多种算法，可以从输入得到输出</li>
<li>找到一组已知答案的数据集，用来训练模型，估算<code>w</code>和<code>b</code></li>
<li>一旦新的数据产生，输入模型，就可以得到结果，同时对<code>w</code>和<code>b</code>进行校正</li>
</ol>
</blockquote>

<p>可以看到，整个过程需要海量计算。所以，神经网络直到最近这几年才有实用价值，而且一般的 CPU 还不行，要使用专门为机器学习定制的 GPU 来计算。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017071214.jpg" alt="" title="" /></p>

<h2>七、神经网络的例子</h2>

<p>下面通过车牌自动识别的例子，来解释神经网络。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017071215.jpg" alt="" title="" /></p>

<p>所谓"车牌自动识别"，就是高速公路的探头拍下车牌照片，计算机识别出照片里的数字。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017071216.jpg" alt="" title="" /></p>

<p>这个例子里面，车牌照片就是输入，车牌号码就是输出，照片的清晰度可以设置权重（<code>w</code>）。然后，找到一种或多种，作为感知器。算法的得到结果是一个概率，比如75%的概率可以确定是数字<code>1</code>。这就需要设置一个阈值（<code>b</code>）（比如85%的可信度），低于这个门槛结果就无效。</p>

<p>一组已经识别好的车牌照片，作为训练集数据，输入模型。不断调整各种参数，直至找到正确率最高的参数组合。以后拿到新照片，就可以直接给出结果了。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017071217.png" alt="" title="" /></p>

<h2>八、输出的连续性</h2>

<p>上面的模型有一个问题没有解决，按照假设，输出只有两种结果：0和1。但是，模型要求<code>w</code>或<code>b</code>的微小变化，会引发输出的变化。如果只输出<code>0</code>和<code>1</code>，未免也太不敏感了，无法保证训练的正确性，因此必须将"输出"改造成一个连续性函数。</p>

<p>这就需要进行一点简单的数学改造。</p>

<p>首先，将感知器的计算结果<code>wx + b</code>记为<code>z</code>。</p>

<blockquote><pre><code class="language-javascript">
z = wx + b
</code></pre></blockquote>

<p>然后，计算下面的式子，将结果记为<code>σ(z)</code>。</p>

<blockquote><pre><code class="language-javascript">
σ(z) = 1 / (1 + e^(-z))
</code></pre></blockquote>

<p>这是因为如果<code>z</code>趋向正无穷<code>z → +∞</code>（表示感知器强烈匹配），那么<code>σ(z) → 1</code>；如果<code>z</code>趋向负无穷<code>z → -∞</code>（表示感知器强烈不匹配），那么<code>σ(z) → 0</code>。也就是说，只要使用<code>σ(z)</code>当作输出结果，那么输出就会变成一个连续性函数。</p>

<p>原来的输出曲线是下面这样。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017071208.png" alt="" title="" /></p>

<p>现在变成了这样。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017071209.png" alt="" title="" /></p>

<p>实际上，还可以证明<code>Δσ</code>满足下面的公式。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017071210.png" alt="" title="" /></p>

<p>即<code>Δσ</code>和<code>Δw</code>和<code>Δb</code>之间是线性关系，变化率是偏导数。这就有利于精确推算出<code>w</code>和<code>b</code>的值了。</p>

<p>（正文完）</p>

<p>=============================================</p>

<p></p>

<p>下面是推广时间。</p>

<p>前端开发是，今天（7月13日）开始报名了，感兴趣的朋友不要错过！</p>

<p></p>

<p>本课程的重点是讲解如何应用 CSS 框架和 JavaScript 框架，做出高性能、高可用性的产品，并且使用测试工具保证代码质量。学习过程中，学员必须完成以下课堂练习。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017071219.jpg" width="400" height="483" style="width: 400px;height: 483px;"/> <img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017071220.jpg" width="400"  height="483"  style="width: 400px;height: 483px;"/></p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017071221.jpg" width="400"  height="483" style="width: 400px;height: 483px;"/> <img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017071222.jpg" width="400"  height="483" style="width: 400px;height: 483px;"/></p>

<p>该课程是纳米学位课程，学员提交的每一行代码都有导师 code review，并且每周可以预约导师一对一辅导，对于提高个人能力极有帮助。</p>

<p>由于有真人 code review 环节，所以招生人数有限制，本期只有100个名额，目前已经预定了67个。了解详情，报名从速哦。</p>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2017-07-13T06:33:10+08:00">2017年7月13日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>博客文集：</li>
<li>社交媒体：</li>
<li>Feed订阅： </li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------
<h1 id="#title_2" >3、视频演讲： 百度外卖从 IDC 到云端服务迁移历程</h1>
赵晓燕
[http://www.infoq.com/cn/presentations/baidu-takeaway-from-idc-to-cloud-service-migration-process?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/baidu-takeaway-from-idc-to-cloud-service-migration-process?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/baidu-takeaway-from-idc-to-cloud-service-migration-process/zh/mediumimage/zhaoxiaoyan270.jpg"/><p>历时 1 年时间，百度外卖从百度整体 spinoff 完毕；包括百度外卖基础设施建设、在线业务未停服从 IDC 到云端迁移方案和迁移实战、涉及到的运维平台建设，全部迁移完毕。在 1 年的迁移过程中，遇到众多困难，涉及到所有百度成熟的 20+ 个运维平台全部不可用，IDC<->云端网络不通数据无法平滑切换，用户端 / 商户端 / 物流端业务几百个模块耦合错综复杂无法在同一天完成全部切换，同时业务决定我们必须无缝切换即使凌晨也不能中断服务；面对这些困难，我们自研了 12 个运维平台（包括权限系统、部署系统、网络监控、CMDB、智能化监控等），用 BVROUTER 方式打通 IDC<->云端网络，整体设计了业务 / 数据整体快速切换方案做到单点数据秒级切换、切换过程没有损失任何一个订单、用户零感知。</p> <i>By 赵晓燕</i>
---------------
<h1 id="#title_3" >4、文章： 如何有效地收集移动应用中的用户反馈</h1>
Jianing Zheng
[http://www.infoq.com/cn/articles/effectively-collect-user-feedback-mobile-apps?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/effectively-collect-user-feedback-mobile-apps?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/effectively-collect-user-feedback-mobile-apps/zh/headerimage/GettyImages-526827958.jpg"/><p>本文从多个角度，包括用户体验、开发、运营和成本等分析了各种形式的移动应用中的反馈。它还分析了哪种形式的反馈在哪种情况下更适用，目的是帮助移动应用程序开发人员或产品经理使用合适的反馈机制并改进其产品。</p> <i>By Jianing Zheng</i> <i> Translated by 姚佳灵</i>
---------------
<h1 id="#title_4" >5、视频演讲： 百度超大规模低成本对象存储-BOS构建之路</h1>
牛献会
[http://www.infoq.com/cn/presentations/baidu-bos-construction-of-large-scale-low-cost-object-storage?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/baidu-bos-construction-of-large-scale-low-cost-object-storage?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/baidu-bos-construction-of-large-scale-low-cost-object-storage/zh/mediumimage/xxxx2700.jpg"/><p>对象存储支撑了海量数据的存放，要求高可靠和高扩展的同时，还要求极低的成本。本次分享主要介绍百度云对象存储如何演进并在保证高可用性的前提下，降低存储的成本。</p> <i>By 牛献会</i>
---------------
<h1 id="#title_5" >6、文章： 虚拟研讨会：数据科学、机器学习、深度学习、人工智能及企业开发人员</h1>
Rags Srinivas
[http://www.infoq.com/cn/articles/DS-ML-DL-AI?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/DS-ML-DL-AI?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/DS-ML-DL-AI/zh/headerimage/vp-ai.jpg"/><p>为进一步阐明人工智能相关的多个技术概念，并探讨企业开发人员如何使用这些技术改进自身解决方案的智能性，InfoQ近期邀请了数位人工智能领域的专家，开展了一次虚拟专家研讨会。</p> <i>By Rags Srinivas</i> <i> Translated by Rays</i>
---------------
<h1 id="#title_6" >7、文章： 如何使用Kubernetes GPU集群自动化深度学习训练</h1>
CarolGuo
[http://www.infoq.com/cn/articles/kubernetes-gpu-cluster-to-automate-deep-learning-training?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/kubernetes-gpu-cluster-to-automate-deep-learning-training?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/kubernetes-gpu-cluster-to-automate-deep-learning-training/zh/smallimage/world_logo.jpg"/><p>该指南能帮助同行研究者和爱好者们轻松地使用Kubernetex GPU集群来自动化和加速他们的深度学习训练。</p> <i>By CarolGuo</i>
---------------
<h1 id="#title_7" >8、Rust语言2017路线图半年回顾</h1>
谢丽
[http://www.infoq.com/cn/news/2017/07/Rust-2017-Road-map-review-half-y?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/07/Rust-2017-Road-map-review-half-y?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>近日，Rust核心团队成员Nicholas Matsakis在Rust官方博文上发表了一篇博文，介绍2017年Rust路线图上各项计划的进展情况。</p> <i>By 谢丽</i>
---------------
<h1 id="#title_8" >9、从Java到Spring为何独得青睐Spring Summit 2017不可不知的那些事儿</h1>
张晓楠
[http://www.infoq.com/cn/news/2017/07/Java-Spring-Summit-2017?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/07/Java-Spring-Summit-2017?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>作为最受欢迎的编程语言之一，Java诞生这二十多年以来拥有着数量众多的铁杆粉丝。虽然新的编程语言层出不穷，但是很多人对Java的钟爱却丝毫未变。而在Java为数众多的框架中，Spring框架独得很多人的青睐。</p> <i>By 张晓楠</i>
---------------