## 文章索引
1、 <a href="#1react-v1560" >React v15.6.0</a><br/>
2、 <a href="#2github是如何改进自身的dns架构的" >GitHub是如何改进自身的DNS架构的</a><br/>
3、 <a href="#3apmcon-2017启动传统行业+互联网的性能大碰撞" >APMCon 2017启动，传统行业+互联网的性能大碰撞</a><br/>
4、 <a href="#4云原生这么火你学好spring了吗让spring大神教教你" >云原生这么火你学好Spring了吗？让Spring大神教教你</a><br/>
5、 <a href="#5对aws-lambda的支持添加到了aws-x-ray分布式跟踪服务中" >对AWS Lambda的支持添加到了AWS X-Ray分布式跟踪服务中</a><br/>
6、 <a href="#6github调查开源项目文档许可证书在工作中的使用情况" >GitHub调查开源项目：文档、许可证书、在工作中的使用情况</a><br/>
7、 <a href="#7文章-linux权限控制的基本原理" >文章： Linux权限控制的基本原理</a><br/>
8、 <a href="#8ocado-technology-发布了kubermesh-一个支持自动配置采用网状网络的-kubernetes-集群原型" >Ocado Technology 发布了“Kubermesh”， 一个支持自动配置、采用网状网络的 Kubernetes 集群原型</a><br/>
9、 <a href="#9c#-71先睹为快第二部分" >C# 7.1先睹为快（第二部分）</a><br/>
10、 <a href="#10puppet-labs发布2017年devops现状调查报告" >Puppet Labs发布2017年DevOps现状调查报告</a><br/>
11、 <a href="#11视频演讲-从传统-idc-到混合云架构经验谈" >视频演讲： 从传统 IDC 到混合云架构经验谈</a><br/>
12、 <a href="#12convincing-clients:-how-to-get-sign-off-when-it-matters" >Convincing Clients: How To Get Sign Off When It Matters</a><br/><h1 id="#title_0" >1、React v15.6.0</h1>

[https://facebook.github.io/react/blog/2017/06/13/react-v15.6.0.html](https://facebook.github.io/react/blog/2017/06/13/react-v15.6.0.html)
<p>Today we are releasing React 15.6.0. As we prepare for React 16.0, we have been fixing and cleaning up many things. This release continues to pave the way.</p>

<h2>Improving Inputs</h2>

<p>In React 15.6.0 the <code>onChange</code> event for inputs is a little bit more reliable and handles more edge cases, including the following:</p>

<ul>
<li>not firing when radio button is clicked but not changed ()</li>
<li>changing an input of type <code>range</code> with the arrow keys ()</li>
<li>pasting text into a text area in IE11 ()</li>
<li>auto-fill in IE11 ()</li>
<li>clearing input with &#39;x&#39; button or right-click &#39;delete&#39; in IE11 ()</li>
<li>not firing when characters are present in the input on render in IE11 ()</li>
</ul>

<p>Thanks to  and everyone who helped out on those issues and PRs.</p>

<h2>Less Noisy Deprecation Warnings</h2>

<p>We are also including a couple of new warnings for upcoming deprecations. These should not affect most users, and for more details see the changelog below.</p>

<p>After the last release, we got valuable community feedback that deprecation warnings were causing noise and failing tests. <strong>In React 15.6, we have downgraded deprecation warnings to use <code>console.warn</code> instead of <code>console.error</code>.</strong> Our other warnings will still use <code>console.error</code> because they surface urgent issues which could lead to bugs. Unlike our other warnings, deprecation warnings can be fixed over time and won&#39;t cause problems in your app if shipped. We believe that downgrading the urgency of deprecation warnings will make your next update easier. Thanks to everyone who was involved in the discussion of this change.</p>

<hr>

<h2>Installation</h2>

<p>We recommend using  is a good place to get started.</p>

<p>To install React with Yarn, run:</p>
<div class="highlight"><pre><code class="language-bash" data-lang="bash">yarn add react@^15.6.0 react-dom@^15.6.0
</code></pre></div>
<p>To install React with npm, run:</p>
<div class="highlight"><pre><code class="language-bash" data-lang="bash">npm install --save react@^15.6.0 react-dom@^15.6.0
</code></pre></div>
<p>We recommend using a bundler like  so you can write modular code and bundle it together into small packages to optimize load time.</p>

<p>Remember that by default, React runs extra checks and provides helpful warnings in development mode. When deploying your app, make sure to .</p>

<p>In case you don&#39;t use a bundler, we also provide pre-built bundles in the npm packages which you can  on your page:</p>

<ul>
<li><strong>React</strong><br/>
Dev build with warnings: <br/>
Minified build for production: <br/></li>
<li><strong>React with Add-Ons</strong><br/>
Dev build with warnings: <br/>
Minified build for production: <br/></li>
<li><strong>React DOM</strong> (include React in the page before React DOM)<br/>
Dev build with warnings: <br/>
Minified build for production: <br/></li>
<li><strong>React DOM Server</strong> (include React in the page before React DOM Server)<br/>
Dev build with warnings: <br/>
Minified build for production: <br/></li>
</ul>

<p>We&#39;ve also published version <code>15.6.0</code> of <code>react</code> and <code>react-dom</code> on npm, and the <code>react</code> package on bower.</p>

<hr>

<h2>Changelog</h2>

<h2>15.6.0 (June 13, 2017)</h2>

<h3>React</h3>

<ul>
<li>Downgrade deprecation warnings to use <code>console.warn</code> instead of <code>console.error</code>. ()</li>
<li>Add a deprecation warning for <code>React.createClass</code>. Points users to <code>create-react-class</code> instead. ()</li>
<li>Add deprecation warnings and separate module for <code>React.DOM</code> factory helpers. ()</li>
<li>Warn for deprecation of <code>React.createMixin</code> helper, which was never used. ()</li>
</ul>

<h3>React DOM</h3>

<ul>
<li>Add support for CSS variables in <code>style</code> attribute. ()</li>
<li>Add support for CSS Grid style properties. ()</li>
<li>Fix bug where inputs mutated value on type conversion. ()</li>
<li>Fix issues with <code>onChange</code> not firing properly for some inputs. ()</li>
<li>Fix bug where controlled number input mistakenly allowed period. ()</li>
<li>Fix bug where performance entries were being cleared. ()</li>
</ul>
---------------
<h1 id="#title_1" >2、GitHub是如何改进自身的DNS架构的</h1>
Sergio De Simone
[http://www.infoq.com/cn/news/2017/06/github-dns-infrastructure?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/06/github-dns-infrastructure?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>据GitHub高级架构工程师Joe Williams撰文介绍，过去数年中，GitHub一直使用的是一个简单的DNS架构。虽然它也能适合工作需求，但现在GitHub已迁移到一个能更好地支持自身规模的新架构。</p> <i>By Sergio De Simone</i> <i> Translated by Rays</i>
---------------
<h1 id="#title_2" >3、APMCon 2017启动，传统行业+互联网的性能大碰撞</h1>
薛梁
[http://www.infoq.com/cn/news/2017/06/apmcon-2017?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/06/apmcon-2017?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>记得《解读2016之APM篇》一文中，听云CTO Wood和前AppDynamics首席数据科学家赵宇辰都提到，应用性能管理的关注点正在逐渐向物联网、直播、微服务、容器等方向倾斜，例如你的共享单车App识别不了二维码，在手机上看不了直播等情况一样，这就需要通过更智能的APM技术对异常进行检测和根因诊断，提前解决应用故障问题。</p> <i>By 薛梁</i>
---------------
<h1 id="#title_3" >4、云原生这么火你学好Spring了吗？让Spring大神教教你</h1>
张晓楠
[http://www.infoq.com/cn/news/2017/06/cloud-spring-summit?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/06/cloud-spring-summit?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Spring Summit 2017，从企业上云、传统行业在数字经济时代机遇与挑战等宏观战略层面，以及微服务、DevOps、Reactive、CloudNative Java等微观技术层面，来诠释如何完成企业数字化转型这道考题。</p> <i>By 张晓楠</i>
---------------
<h1 id="#title_4" >5、对AWS Lambda的支持添加到了AWS X-Ray分布式跟踪服务中</h1>
Daniel Bryant
[http://www.infoq.com/cn/news/2017/06/aws-xray-lambda?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/06/aws-xray-lambda?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>在AWS X-Ray分布式跟踪服务4月份发布的通用版本（General Availability，GA）中，Amazon已经为X-Ray添加了对AWS Lambda的支持，它能够记录函数调用和相关的元数据，通过AWS Console进行图像化展示并进行分析以便于调试或故障的恢复。</p> <i>By Daniel Bryant</i> <i> Translated by 张卫滨</i>
---------------
<h1 id="#title_5" >6、GitHub调查开源项目：文档、许可证书、在工作中的使用情况</h1>
Abel Avram
[http://www.infoq.com/cn/news/2017/06/github-survey-open-source?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/06/github-survey-open-source?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/news/2017/06/github-survey-open-source/zh/headerimage/GettyImages-485587762.jpg"/><p>GitHub对开源项目进行了一个调查，在对所收集的数据进行分析后，发布了结果。他们感兴趣的内容包括：开发人员跟开源项目之间是什么关系、文档扮演了什么样的角色、项目中出现的消极互动的程度和影响。
</p> <i>By Abel Avram</i> <i> Translated by 姚佳灵</i>
---------------
<h1 id="#title_6" >7、文章： Linux权限控制的基本原理</h1>
吕凯
[http://www.infoq.com/cn/articles/basic-principle-of-Linux-privilege-control?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/basic-principle-of-Linux-privilege-control?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/basic-principle-of-Linux-privilege-control/zh/smallimage/clou_logo.jpg"/><p>这里，我们主要介绍 Linux 系统中，权限控制的基本原理。</p> <i>By 吕凯</i>
---------------
<h1 id="#title_7" >8、Ocado Technology 发布了“Kubermesh”， 一个支持自动配置、采用网状网络的 Kubernetes 集群原型</h1>
Daniel Bryant
[http://www.infoq.com/cn/news/2017/06/kubermesh-ocado?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/06/kubermesh-ocado?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Ocado Technology团队创造了Kubermesh，一个“基于裸机、自我托管、自我恢复、自我配置、采用部分网状网络的Kubernetes集群”。Kubermesh本质上可以被视为一个粘合节点，它将多个技术结合在一起，从而构成了一个容器平台。这个平台由一个使用OSPF3路由协议的部分网状网络和一个用iPXE启动、自我安装的Kubernetes部署组成。该Kubernetes部署运行在由Openstack管理着的裸机服务器上。</p> <i>By Daniel Bryant</i> <i> Translated by 燕春翔</i>
---------------
<h1 id="#title_8" >9、C# 7.1先睹为快（第二部分）</h1>
Jonathan Allen
[http://www.infoq.com/cn/news/2017/06/CSharp-7.1-b?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/06/CSharp-7.1-b?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/news/2017/06/CSharp-7.1-b/zh/headerimage/GettyImages-625206764.jpg"/><p>昨天我们介绍了异步Main函数（Async Main）和默认表达式（Default Expressions）。我们的C# 7.1之旅将继续，今天要介绍的特性在建议中称为推导元组名（Infer Tuple Names）和使用泛型的模式匹配（Pattern-matching with Generics）。</p> <i>By Jonathan Allen</i> <i> Translated by Rays</i>
---------------
<h1 id="#title_9" >10、Puppet Labs发布2017年DevOps现状调查报告</h1>
Hrishikesh Barua
[http://www.infoq.com/cn/news/2017/06/puppetlabs-devops-report-2017?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/06/puppetlabs-devops-report-2017?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/news/2017/06/puppetlabs-devops-report-2017/zh/headerimage/GettyImages-517703860.jpg"/><p>Puppet Labs 2017年DevOps现状调查报告显示，高效IT团队的部署频率越来越高而且恢复速度越来越快了。人们更注重自动化，借助松耦合的架构和团队来促进持续交付。转型领导和精益产品管理实践也是高效团队的关键驱动力。</p> <i>By Hrishikesh Barua</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_10" >11、视频演讲： 从传统 IDC 到混合云架构经验谈</h1>
周乾
[http://www.infoq.com/cn/presentations/from-traditional-idc-to-hybrid-cloud-architecture-experience?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/from-traditional-idc-to-hybrid-cloud-architecture-experience?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/from-traditional-idc-to-hybrid-cloud-architecture-experience/zh/mediumimage/zhouqian270.jpg"/><p>量化派是一家数据驱动的科技金融 Fintech 公司，通过人工智能、大数据机器学习等前沿技术提供消费信贷撮合及消费场景下的白条服务，每年处理千万级用户信用及信用消费申请。随着业务的高速发展，原有的 IDC 托管服务已经无法满足量化派在基础设施快速扩容、高可用及监控管理等方面的需求。青云QingCloud 提供的公私一体的混合云解决方案提供秒级资源调度、全面的监控告警服务及完备的高可用机制。借助青云QingCloud 提供的完整云平台，量化派正在打造公有云和私有云并存的混合云架构。在此次演讲中，量化派技术总监周乾将分享从传统 IDC 到混合云架构的演进过程及技术实践。</p> <i>By 周乾</i>
---------------
<h1 id="#title_11" >12、Convincing Clients: How To Get Sign Off When It Matters</h1>
Paul Boag
[https://www.smashingmagazine.com/2017/06/convincing-clients-sign-off/](https://www.smashingmagazine.com/2017/06/convincing-clients-sign-off/)
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
</table><p>We have all been there. That dreaded moment when after weeks of work we have to present our progress to key stakeholders, and they mercilessly tear it apart. It feels inevitable, but usually, we can avoid these situations.</p>

<figure></figure>

<p>Wouldn’t life be so much easier if we didn’t need to get other people to buy-in to our work? Unfortunately, it doesn’t work that way, especially in digital. What we do involves so many different disciplines working together. We have to get the support of colleagues, stakeholders and management. But, achieving that can be painful, to say the least.</p><p>The post .</p>
---------------