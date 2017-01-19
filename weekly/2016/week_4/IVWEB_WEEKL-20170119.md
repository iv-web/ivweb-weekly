## 文章索引
1、 <a href="#1视频演讲-浏览器端-javascript-异常监控-for-dummies" >视频演讲： 浏览器端 JavaScript 异常监控 For Dummies</a><br/>
2、 <a href="#2kuzzle一种内部部署的文档后端" >Kuzzle，一种内部部署的文档后端</a><br/>
3、 <a href="#3google发布新的图像压缩技术最高可节省75％带宽" >Google发布新的图像压缩技术，最高可节省75％带宽</a><br/>
4、 <a href="#4视频演讲-jvm-虚拟化-重新定义-java-容器热部署资源管理机制" >视频演讲： JVM 虚拟化—— 重新定义 Java 容器热部署资源管理机制</a><br/>
5、 <a href="#5文章-谈阿里核心业务监控平台sunfire的技术架构" >文章： 谈阿里核心业务监控平台SunFire的技术架构</a><br/>
6、 <a href="#6视频演讲-企业大数据在信用风险管理的应用" >视频演讲： 企业大数据在信用风险管理的应用</a><br/>
7、 <a href="#7文章-用apache-spark做大数据处理第五部分spark机器学习数据流水线" >文章： 用Apache Spark做大数据处理——第五部分：Spark机器学习数据流水线</a><br/>
8、 <a href="#8oracle发布裸金属云数据库服务新的云主机实例以及三个新区域" >Oracle发布裸金属云数据库服务、新的云主机实例以及三个新区域</a><br/>
9、 <a href="#9文章-可预见的敏捷交付" >文章： 可预见的敏捷交付</a><br/>
10、 <a href="#10哈佛海归眼中的中国fintech技术与美国相差的是风雨百年的距离" >哈佛海归眼中的中国Fintech技术：与美国相差的是风雨百年的距离</a><br/>
11、 <a href="#11培养注意力和团队意识" >培养注意力和团队意识</a><br/>
12、 <a href="#12视频演讲-基于文本数据的用户画像实践" >视频演讲： 基于文本数据的用户画像实践</a><br/>
13、 <a href="#13谷歌使用grumpy解决cpython的并发问题" >谷歌使用Grumpy解决CPython的并发问题</a><br/>
14、 <a href="#14微软azure首席架构师john-gossman就微软加入linux基金会一事答疑" >微软Azure首席架构师John Gossman就微软加入Linux基金会一事答疑</a><br/>
15、 <a href="#15物联网技术周报第-77-期:-构建基于-amazon-alex-的声控电子医疗应用" >物联网技术周报第 77 期: 构建基于 Amazon Alex 的声控电子医疗应用</a><br/>
16、 <a href="#16一种在-ibm-openwhisk-中配置和调用操作的简单方法" >一种在 IBM OpenWhisk 中配置和调用操作的简单方法</a><br/>
17、 <a href="#17more-than-just-pretty:-how-imagery-drives-user-experience" >More Than Just Pretty: How Imagery Drives User Experience</a><br/><h1 id="#title_0" >1、视频演讲： 浏览器端 JavaScript 异常监控 For Dummies</h1>
刘小杰
[http://www.infoq.com/cn/presentations/javascript-exception-monitoring-for-dummies-in-browser-side?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/javascript-exception-monitoring-for-dummies-in-browser-side?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/javascript-exception-monitoring-for-dummies-in-browser-side/zh/mediumimage/liuxiaojie270.jpg"/><p>本次分享介绍百姓网在 JS 异常监控方面的探索过程。了解和借鉴其他团队的经验，对比之后制定适合自己项目的方案，力争对现有代码的影响最小化。在了解 window.onerror 的限制与不足后，利用 Babel 进行 AST 转换，将 JS 代码用 try catch 包装起来，并依据浏览器特性分别加载源 JS 和包装后的 JS。上报的异常数据发送到服务端（sentry）用于检索和统计，既可以结合 sourcemap 查看异常对应源码位置的上下文代码，也可以配合灰度测试与异常预警机制提前发现问题。除此之外还有很多细节上的小问题，例如噪音消除、浏览器 Error 对象实现差异等。</p> <i>By 刘小杰</i>
---------------
<h1 id="#title_1" >2、Kuzzle，一种内部部署的文档后端</h1>
Abel Avram
[http://www.infoq.com/cn/news/2017/01/kuzzle?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/01/kuzzle?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/news/2017/01/kuzzle/zh/headerimage/kuzzle.jpg"/><p>新发布的Kuzzle文档后端平台可以内部部署或是在云中运行，它提供了CRUD API和多种SDK，支持多种通信协议，并可通过使用插件做特性扩展。</p> <i>By Abel Avram</i> <i> Translated by Rays</i>
---------------
<h1 id="#title_2" >3、Google发布新的图像压缩技术，最高可节省75％带宽</h1>
刘志勇
[http://www.infoq.com/cn/news/2017/01/Google-RAISR?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/01/Google-RAISR?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>高清显示一直缺乏内容，成了该行业发展的痛点。因为超分辨率技术受成本、硬件限制，未能广为普及。将低分辨率图片转化为高清版本，并可在多种设备上查看和分享，成了市场巨大的需求。 如今，Google为了解决这一痛点，发布了黑科技，让人们看到了希望。</p> <i>By  刘志勇</i>
---------------
<h1 id="#title_3" >4、视频演讲： JVM 虚拟化—— 重新定义 Java 容器热部署资源管理机制</h1>
陆传胜
[http://www.infoq.com/cn/presentations/redefine-the-java-container-resource-management-mechanism?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/redefine-the-java-container-resource-management-mechanism?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/redefine-the-java-container-resource-management-mechanism/zh/mediumimage/luchuansheng270.jpg"/><p>本次分享将介绍阿里巴巴公司开发上线的一种动态更新大规模 Java 应用的方案，通过在 Java 虚拟机层面加入虚拟化的支持，能有效解决传统热更新方案的痛点，高效精确的回收系统资源。对于大规模 Java 应用，可以做到不重启 Java 进程而达到更新应用的目的，整体更新操作时间也被大大缩短。</p> <i>By 陆传胜</i>
---------------
<h1 id="#title_4" >5、文章： 谈阿里核心业务监控平台SunFire的技术架构</h1>
郁松、章邯等
[http://www.infoq.com/cn/articles/alibaba-core-business-monitoring-platform-sunfire?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/alibaba-core-business-monitoring-platform-sunfire?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/alibaba-core-business-monitoring-platform-sunfire/zh/smallimage/Alibaba_100.jpg"/><p>在2016年双11全球购物狂欢节中，天猫全天交易额1207亿元，前30分钟每秒交易峰值17.5万笔，每秒支付峰值12万笔。承载这些秒级数据背后的监控产品是如何实现的呢？接下来本文将从阿里监控体系、监控产品、监控技术架构及实现分别进行详细讲述。 </p> <i>By 郁松、章邯等</i>
---------------
<h1 id="#title_5" >6、视频演讲： 企业大数据在信用风险管理的应用</h1>
李想
[http://www.infoq.com/cn/presentations/application-of-big-data-in-credit-risk-management?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/application-of-big-data-in-credit-risk-management?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/application-of-big-data-in-credit-risk-management/zh/mediumimage/lixiang270.jpg"/><p>传统征信存在的诸多问题，利用金融大数据却能迎刃而解。来自平安科技智能引擎部的企业大数据专家李想，介绍了企业大数据在信用风险管理的应用。</p> <i>By 李想</i>
---------------
<h1 id="#title_6" >7、文章： 用Apache Spark做大数据处理——第五部分：Spark机器学习数据流水线</h1>
Srini Penchikala
[http://www.infoq.com/cn/articles/apache-sparkml-data-pipelines?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/apache-sparkml-data-pipelines?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/apache-sparkml-data-pipelines/zh/smallimage/Spark-ML.jpg"/><p>在支持了机器学习数据流水线之后，Apache Spark框架已经全面支持各种功能，包括ETL、批处理分析、流数据分析和机器学习等。在这个关于Apache Spark的系列文章中，作者Srini Penchikala讨论了Spark ML包的内容，和如何用它来创建并管理机器学习数据流水线。</p> <i>By Srini Penchikala</i> <i> Translated by 足下</i>
---------------
<h1 id="#title_7" >8、Oracle发布裸金属云数据库服务、新的云主机实例以及三个新区域</h1>
杨赛
[http://www.infoq.com/cn/news/2017/01/oracle-expands-cloud-platform?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/01/oracle-expands-cloud-platform?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>2017年1月17日，Oracle公布了其云计算平台Oracle Cloud Platform的重要更新，其中包括裸金属上的Oracle数据库云服务，以及云主机、负载均衡和存储服务的若干升级。同日，Oracle还宣布将在2017年年中之前增加三个新区域：美国弗吉尼亚州、英国伦敦、以及土耳其。</p> <i>By 杨赛</i>
---------------
<h1 id="#title_8" >9、文章： 可预见的敏捷交付</h1>
Russ Lewis
[http://www.infoq.com/cn/articles/predictable-agile-delivery?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/predictable-agile-delivery?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/predictable-agile-delivery/zh/smallimage/GettyImages-609085276.jpg"/><p>人类的团队是独一无二的、非线性的、不可预见的，但在一定条件下，他们的输出可以变成线性的、可扩展的、可预见的。管理者们需要在某些方面做出转变：鼓励提升可预见性，理解他们团队的需求，自己动手清除障碍或快速升级问题以便得到解决。</p> <i>By Russ Lewis</i> <i> Translated by 薛命灯</i>
---------------
<h1 id="#title_9" >10、哈佛海归眼中的中国Fintech技术：与美国相差的是风雨百年的距离</h1>
杜小芳
[http://www.infoq.com/cn/news/2017/01/Harvard-returnees-China-Fintech?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/01/Harvard-returnees-China-Fintech?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>中国的FinTech发展迅猛，已经重塑了本身也很年轻的互联网金融行业，更改变了每个人的生活。而大数据对金融的革新和推进具体起到了什么作用？大数据解决了传统金融什么痛点？中美金融行业的技术是否有差距？这篇文章中我们采访了中国技术开放日.上海站的讲师，平安科技智能引擎部企业大数据专家李想，以此希望能让你了解平安科技金融大数据的创新实践。</p> <i>By 杜小芳</i>
---------------
<h1 id="#title_10" >11、培养注意力和团队意识</h1>
Ben Linders
[http://www.infoq.com/cn/news/2017/01/attention-awareness-teams?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/01/attention-awareness-teams?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>技术使得团队协作更加容易，但同时它也分散了我们的注意力，并且对人与人之间相互交流的质量和内容产生了不良影响。Jeffery Hackert说，仅仅是一个手机就可以吸引你的注意力，降低你的专注度。他建议在团队工作时，要培养成员的注意力、意识和共鸣。</p> <i>By Ben Linders</i> <i> Translated by 尚剑</i>
---------------
<h1 id="#title_11" >12、视频演讲： 基于文本数据的用户画像实践</h1>
丁若谷
[http://www.infoq.com/cn/presentations/practice-of-user-portrait-based-on-text-data?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/practice-of-user-portrait-based-on-text-data?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/practice-of-user-portrait-based-on-text-data/zh/mediumimage/dingruogu270.jpg"/><p>金融、地产等行业客户拥有大量数据，同时又有用户画像的强烈需求。相较于用户人口属性、购物记录等结构化数据，非结构化数据相对难于分析。我们希望从明略数据在为多位企业客户服务的实践经验出发，分享用户画像全流程中涉及到的技术架构，特别是文本数据在技术上所带来的机遇和挑战。同时，我们也会探讨发挥用户画像业务价值的方式，以及为了匹配快速变化的业务需求，在技术上所需的应对和准备。</p> <i>By 丁若谷</i>
---------------
<h1 id="#title_12" >13、谷歌使用Grumpy解决CPython的并发问题</h1>
Abel Avram
[http://www.infoq.com/cn/news/2017/01/grumpy?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/01/grumpy?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>谷歌通过使用Go语言创建了一个新的Python运行时，解决了CPython中全局解释器锁（Global Interpreter Lock）导致的并发局限。</p> <i>By Abel Avram</i> <i> Translated by 王纯超</i>
---------------
<h1 id="#title_13" >14、微软Azure首席架构师John Gossman就微软加入Linux基金会一事答疑</h1>
Rags Srinivas
[http://www.infoq.com/cn/news/2017/01/microsoft-joins-linux-foundation?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/01/microsoft-joins-linux-foundation?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/news/2017/01/microsoft-joins-linux-foundation/zh/headerimage/GettyImages-513551088.jpg"/><p>Rags Srinivas采访了微软Azure的首席架构师和Linux基金会董事会成员，讨论了微软作为一个白金会员加入了Linux基金会的事，以及在微软里面其它的开源活动。</p> <i>By Rags Srinivas</i> <i> Translated by 足下</i>
---------------
<h1 id="#title_14" >15、物联网技术周报第 77 期: 构建基于 Amazon Alex 的声控电子医疗应用</h1>
黄峰达
[http://www.infoq.com/cn/news/2017/01/iot-weekly-77?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/01/iot-weekly-77?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>构建基于 Amazon Alex 的声控电子医疗应用；使用 OpenBTS 基站测试物联网模块；Arduino 101 与 Visuino、蓝牙低功耗与手机进行通讯；新版Win10 IoT物联网发布：小娜驾到；美国OTA更新《物联网信任框架》；Qorvo推出多协议系统级芯片；使用多个DNS供应商以缓解DDoS攻击</p> <i>By 黄峰达</i>
---------------
<h1 id="#title_15" >16、一种在 IBM OpenWhisk 中配置和调用操作的简单方法</h1>

[http://www.ibm.com/developerworks/cn/cloud/library/cl-python-openwhisk-bluemix-trs/index.html?ca=drs-](http://www.ibm.com/developerworks/cn/cloud/library/cl-python-openwhisk-bluemix-trs/index.html?ca=drs-)
IBM OpenWhisk 是一种简单的开源服务，它可以根据需要快速启动和运行代码片段，以响应传入的 REST
            请求。在本教程中，我们将学习如何手动发出 OpenWhisk 命令。然后学习如何使用 Python 库让命令执行变得更简单。
---------------
<h1 id="#title_16" >17、More Than Just Pretty: How Imagery Drives User Experience</h1>
Nick Babich
[https://www.smashingmagazine.com/2017/01/more-than-just-pretty-how-imagery-drives-user-experience/](https://www.smashingmagazine.com/2017/01/more-than-just-pretty-how-imagery-drives-user-experience/)
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
</table><p>As the saying goes, "A picture is worth a thousand words." Human beings are highly visual creatures who are able to process visual information almost instantly; 90 percent of all information that we perceive and that gets transmitted to our brains is visual.</p>

<figure></figure>

<p><strong>Images can be a powerful way to capture users' attention</strong> and differentiate your product. A single image can convey more to the observer than an elaborate block of text. Furthermore, images can cross language barriers in a way text simply can't.</p><p>The post .</p>
---------------