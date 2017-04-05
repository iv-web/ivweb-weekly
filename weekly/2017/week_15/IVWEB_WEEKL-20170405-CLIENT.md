## 文章索引
1、 <a href="#1how-to-set-up-an-automated-testing-system-using-android-phones-a-case-study" >How To Set Up An Automated Testing System Using Android Phones (A Case Study)</a><br/>
2、 <a href="#2视频演讲-计算广告的训练和平滑思想" >视频演讲： 计算广告的训练和平滑思想</a><br/>
3、 <a href="#3文章-nanonets数据不足时如何深度学习" >文章： NanoNets：数据不足时如何深度学习</a><br/>
4、 <a href="#4文章-首届tensorflow开发者大会tensorflow发展这一年来的总结" >文章： 首届TensorFlow开发者大会：TensorFlow发展这一年来的总结</a><br/>
5、 <a href="#5文章-用深度学习技术来找到yelp上的美图" >文章： 用深度学习技术来找到Yelp上的美图</a><br/>
6、 <a href="#6文章-evernote从自有数据中心到google云的迁移-第2篇" >文章： Evernote从自有数据中心到Google云的迁移-第2篇</a><br/>
7、 <a href="#7迷你书-中国顶尖技术团队访谈录·第八季" >迷你书： 中国顶尖技术团队访谈录·第八季</a><br/>
8、 <a href="#850-vibrant-illustrations-to-let-your-mind-wander" >50 Vibrant Illustrations To Let Your Mind Wander</a><br/><h1 id="#title_0" >1、How To Set Up An Automated Testing System Using Android Phones (A Case Study)</h1>
Alexey Perfilov
[https://www.smashingmagazine.com/2017/04/automated-testing-system-android-phones/](https://www.smashingmagazine.com/2017/04/automated-testing-system-android-phones/)
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
</table><p>Regression testing is one of the most time-consuming tasks when developing a mobile Android app. Using <em>myMail</em> as a case study, I'd like to share my experience and advice on how to build a flexible and extensible automated testing system for Android smartphones &#8212; from scratch.</p>

<figure></figure>

<p>The team at <em>myMail</em> currently uses about 60 devices for regression testing. On average, we test roughly 20 builds daily. Approximately 600 UI tests and more than 3,500 unit tests are run on each build.</p><p>The post .</p>
---------------
<h1 id="#title_1" >2、视频演讲： 计算广告的训练和平滑思想</h1>
崔骁凯
[http://www.infoq.com/cn/presentations/calculate-the-training-and-smoothing-of-advertising?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/calculate-the-training-and-smoothing-of-advertising?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/calculate-the-training-and-smoothing-of-advertising/zh/mediumimage/cuixiaokai270.jpg"/><p>计算广告是目前移动互联网的主流盈利模式之一，vivo 作为国内领先的手机终端厂商之一，在移动互联网的计算广告之路上也积累了不少的经验和教训。在这一领域，新广告的训练以及成熟广告的平滑方法业界没有统一的标准，而多种主流的方法或多或少都存在一些弊端，比如：需要单独开辟训练位，或者实时产生的训练反馈不能以合适的权重影响质量度打分，又或者在训练过程中不能区别对待不同的广告，使综合收益最大化。关于这一领域网络上公开的资料较少，且大部分资料涉及到专业的数学知识，晦涩难懂，一般工程师很难在短期内转化并应用到实际业务场景。

本次分享将通过 vivo 在计算广告上的实践之路，深入浅出的为大家介绍 vivo 是如何解决以上难题的，以及思路是什么样的。除了现成的方法，也希望借助解决问题的思路分享，使得在不同的业务环境中的听众都能得到一些收获。</p> <i>By 崔骁凯</i>
---------------
<h1 id="#title_2" >3、文章： NanoNets：数据不足时如何深度学习</h1>
Sarthak Jain
[http://www.infoq.com/cn/articles/how-to-learn-when-the-data-is-insufficient?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/how-to-learn-when-the-data-is-insufficient?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/how-to-learn-when-the-data-is-insufficient/zh/smallimage/agile-logo (1).jpg"/><p>使用深度学习技术解决问题的过程中，最常见的障碍在于训练模型过程中所需的海量数据。需要如此多的数据，原因在于机器在学习的过程中会在模型中遇到大量参数。在面对某一领域的具体问题时，通常可能无法得到构建模型所需规模的数据。然而在一个模型训练任务中针对某种类型数据获得的关系也可以轻松地应用于同一领域的不同问题，这就是所谓的迁移学习。</p> <i>By Sarthak Jain</i> <i> Translated by 大愚若智</i>
---------------
<h1 id="#title_3" >4、文章： 首届TensorFlow开发者大会：TensorFlow发展这一年来的总结</h1>
段石石
[http://www.infoq.com/cn/articles/tensorflow-development-this-year?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/tensorflow-development-this-year?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/tensorflow-development-this-year/zh/smallimage/microservicesArticlelogo.jpg"/><p>TensorFlow 在 2015 年年底一出现就受到了极大的关注，经过一年多的发展，已经成为了在机器学习、深度学习项目中最受欢迎的框架之一。自发布以来，TensorFlow不断在完善并增加新功能，直到在这次大会上发布了稳定版本的TensorFlow V1.0。这次是谷歌第一次举办的TensorFlow开发者和爱好者大会，我们从主题演讲、有趣应用、技术生态、移动端和嵌入式应用多方面总结这次大会上的Submit，希望能对TensorFlow开发者有所帮助。</p> <i>By 段石石</i>
---------------
<h1 id="#title_4" >5、文章： 用深度学习技术来找到Yelp上的美图</h1>
Alex M.
[http://www.infoq.com/cn/articles/finding-beautiful-yelp-photos-use-deep-learning?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/finding-beautiful-yelp-photos-use-deep-learning?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/finding-beautiful-yelp-photos-use-deep-learning/zh/smallimage/heinz-kabutz-article-icon.jpg"/><p>Yelp的数据库中已经存储了几千万张相片，用户们现在每天都会上传大概十万张，而且速度还在不断加快。文中介绍了Yelp如何用深度学习技术来挖掘每家商户的最好的相片并优先展示在商户封面上，从而为用户提供最好的体验的。</p> <i>By Alex M.</i> <i> Translated by 足下</i>
---------------
<h1 id="#title_5" >6、文章： Evernote从自有数据中心到Google云的迁移-第2篇</h1>
薛命灯
[http://www.infoq.com/cn/articles/migration-of-evernote-to-google-cloud-part02?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/migration-of-evernote-to-google-cloud-part02?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/migration-of-evernote-to-google-cloud-part02/zh/smallimage/database.jpg"/><p>2016年底，Evernote对他们的服务进行了一次大规模的迁移。他们将Evernote服务从自有数据中心迁移到了Google Cloud Platform上。他们在短短的70天内完成了整个迁移过程，包括Evernote服务、存储数据和其他配套服务。参与这次迁移的工程师们在Evernote官方博客上分享了这次迁移的过程。这是一个系列的文章，总共有5篇。</p> <i>By 薛命灯</i>
---------------
<h1 id="#title_6" >7、迷你书： 中国顶尖技术团队访谈录·第八季</h1>
InfoQ中文站
[http://www.infoq.com/cn/minibooks/toptech08?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/minibooks/toptech08?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/minibooks/toptech08/zh/smallimage/100.jpg"/><p></p> <i>By InfoQ中文站</i>
---------------
<h1 id="#title_7" >8、50 Vibrant Illustrations To Let Your Mind Wander</h1>
Veerle Pieters
[https://www.smashingmagazine.com/2017/04/vibrant-illustrations-inspiration/](https://www.smashingmagazine.com/2017/04/vibrant-illustrations-inspiration/)
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
</table><p>On days when things don't seem to go as you'd like them to and inspiration is at its lowest, it's good to take a short break and go outside to try and <strong>empty your mind</strong>. That always seems to be the best remedy for me, especially whenever I jump on my bike and go for a short ride.</p>

<figure></figure>

<p>Now the time has come to enjoy these moments even more as the spring season finally starts to show up in nature. We're starting to see green leaves on the trees again, and every morning I wake up to the sounds of the birds chirping. I really enjoy these small joys of spring &#8212; who doesn't?</p><p>The post .</p>
---------------