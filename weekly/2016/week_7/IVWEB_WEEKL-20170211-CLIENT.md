## 文章索引
1、 <a href="#1为什么文件名要小写" >为什么文件名要小写？</a><br/>
2、 <a href="#2疲劳垃圾邮件备份缺失拖垮了gitlabcom" >疲劳、垃圾邮件、备份缺失，拖垮了GitLab.com</a><br/>
3、 <a href="#3swift-4-abi稳定性的征途" >Swift 4 ABI稳定性的征途</a><br/>
4、 <a href="#4google神经机器翻译系统实现zero-shot翻译" >Google神经机器翻译系统实现Zero-Shot翻译</a><br/>
5、 <a href="#5hbase-13-发布性能大幅提升" >HBase 1.3 发布，性能大幅提升</a><br/>
6、 <a href="#6realm-mobile-platform添加水平可扩展性支持遗留数据源和复制" >Realm Mobile Platform添加水平可扩展性，支持遗留数据源和复制</a><br/>
7、 <a href="#7gitlab-816现在包括监控工具并将自动部署扩展到google-container-engine上" >GitLab 8.16现在包括监控工具并将自动部署扩展到Google Container Engine上</a><br/>
8、 <a href="#8死而复生rethinkdb宣布进入linux基金会" >死而复生？RethinkDB宣布进入Linux基金会！</a><br/>
9、 <a href="#9文章-为什么google用apache-beam彻底替换掉mapreduce" >文章： 为什么Google用Apache Beam彻底替换掉MapReduce</a><br/>
10、 <a href="#10web-development-reading-list-#169:-tls-at-scale-brotli-benefits-and-easy-onion-deployments" >Web Development Reading List #169: TLS At Scale, Brotli Benefits, And Easy Onion Deployments</a><br/><h1 id="#title_0" >1、为什么文件名要小写？</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2017/02/filename-should-be-lowercase.html](http://www.ruanyifeng.com/blog/2017/02/filename-should-be-lowercase.html)
<p>上周，加入了文件的命名规则。</p>

        <blockquote>
  <p>"文件名建议只使用小写字母，不使用大写字母。"</p>

<p>"为了醒目，某些说明文件的文件名，可以使用大写字母，比如<code>README</code>、<code>LICENSE</code>。"</p>
</blockquote>

<p>网友看见了，就为什么文件名要小写？ </p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017021006.png" alt="" title="" /></p>

<p>说实话，虽然这是 Linux 传统，我却从没认真想过原因。赶紧查资料，结果发现四个很有说服力的理由，支持这样做。</p>

<p>下面就是这四个理由。另外，文后我还会发布一条前端培训的消息。</p>

<h2>一、可移植性</h2>

<p>Linux 系统是大小写敏感的，而 Windows 系统和 Mac 系统正好相反，大小写不敏感。一般来说，这不是大问题。</p>

<p>但是，如果两个文件名只有大小写不同，其他都相同，跨平台就会出问题。</p>

<blockquote>
  <ul>
<li><code>foobar</code></li>
<li><code>Foobar</code></li>
<li><code>FOOBAR</code></li>
<li><code>fOObAr</code></li>
</ul>
</blockquote>

<p>上面四个文件名，Windows 系统会把它们都当作<code>foobar</code>。如果它们同时存在，你可能没办法打开后面三个文件。</p>

<p>另一方面，在 Mac 系统上开发时，有时会疏忽，写错大小写。</p>

<blockquote><pre><code class="language-javascript">
// 正确文件名是 MyModule.js
const module = require('./myModule');
</code></pre></blockquote>

<p>上面的代码在 Mac 上面可以运行，因为 Mac 认为<code>MyModule.js</code>和<code>myModule.js</code>是同一个文件。但是，一旦代码到服务器运行就会报错，因为 Linux 系统找不到<code>myModule.js</code>。</p>

<p>如果所有的文件名都采用小写，就不会出现上面的问题，可以保证项目有良好的可移植性。</p>

<h2>二、易读性</h2>

<p>小写文件名通常比大写文件名更易读，比如<code>accessibility.txt</code>就比<code>ACCESSIBILITY.TXT</code>易读。</p>

<p>有人习惯使用，单词的第一个字母大写，其他字母小写。这种方法的问题是，如果遇到全部是大写的缩略词，就会不适用。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017021002.jpg" alt="" title="" /></p>

<p>比如，一个姓李的纽约特警，无论写成<code>NYPoliceSWATLee</code>还是<code>NyPoliceSwatlee</code>，都怪怪的，还是写成<code>ny-police-swat-lee</code>比较容易接受。</p>

<h2>三、易用性</h2>

<p>某些系统会生成一些预置的用户目录，采用首字母大写的目录名。比如，Ubuntu 在用户主目录会默认生成<code>Downloads</code>、 <code>Pictures</code>、<code>Documents</code>等目录。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017021003.png" alt="" title="" /></p>

<p>Mac 系统更过分，一部分系统目录也是大写的，比如<code>/Library/Audio/Apple Loops/</code>。</p>

<p>另外，某些常见的配置文件或说明文件，也采用大写的文件名，比如<code>Makefile</code>、<code>INSTALL</code>、<code>CHANGELOG</code>、<code>.Xclients</code>和<code>.Xauthority</code>等等。</p>

<p>所以，用户的文件都采用小写文件名，就很方便与上面这些目录或文件相区分。</p>

<p>如果你打破砂锅问到底，为什么操作系统会采用这样的大写文件名？原因也很简单，因为早期 Unix 系统上，<code>ls</code>命令先列出大写字母，再列出小写字母，大写的路径会排在前面。因此，如果目录名或文件名是大写的，就比较容易被用户首先看到。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017021001.png" alt="" title="" /></p>

<h2>四、便捷性</h2>

<p>文件名全部小写，还有利于命令行操作。比如，某些命令可以不使用<code>-i</code>参数了。</p>

<blockquote><pre><code class="language-bash">
# 大小写敏感的搜索
$ find . -name abc
$ locate "*.htmL"

# 大小写不敏感的搜索
$ find . -iname abc
$ locate -i "*.HtmL"
</code></pre></blockquote>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017021004.png" alt="" title="" /></p>

<p>另外，大写字母需要按下 Shift 键，多多少少有些麻烦。如果文件名小写，就不用碰这个键了，不仅省事，还可以提高打字速度。</p>

<p>程序员长时间使用键盘，每分钟少按几次 Shift，一天下来就可以省掉很多手指动作。长年累月，也是对自己身体的一种保护。</p>

<p>综上所述，文件名全部使用小写字母和连词线（all-lowercase-with-dashes），是一种值得推广的正确做法。</p>

<p>（正文完）</p>

<hr />

<p>下面是推广时间。</p>

<p>如果大家还有印象，以前我。</p>

<p>他们的特色就是保证课程质量，不吹牛，非常低调地将所有精力，都投入课程准备和学员的悉心指导，让学员循序渐进、多敲多练，掌握前端编程，做出好的项目。如果你想投入前端行业，或者了解互联网技术，他们是一个不错的选择。</p>

<p></p>

<p>根据我的提议，创始人张小河了前几期学员的反馈。</p>

<blockquote>
  <p>"身为一个应届生，接触前端完全是因为不喜欢自己的专业，又到了就业的时节，想想自己还是对互联网比较感兴趣，从网上了解了一下互联网各个方面的工作，发现自己对前端比较感兴趣，由此而入了坑......（）"</p>
</blockquote>

<p>现在，2017年开始招生了。和上次冬季班一样，依然是<strong>0成本入学</strong>，只需要缴纳 99 元，即可感受一周的课程，享受完全正式的待遇（录播 + 直播 + 教学监管 + 技术辅导）。一周后，如果觉得不满意，99 元可以退款。</p>

<p>不管你最后是否报名，只要参加培训，都可以免费获得一份。</p>

<p></p>

<p>春季班定在3月初开课，名额已经不多了。想从事前端开发，却不知道从何学起的朋友，不要错过这个机会，点击，了解详情吧。</p>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2017-02-10T08:21:42+08:00">2017年2月10日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>博客文集：</li>
<li>社交媒体：</li>
<li>Feed订阅： </li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------
<h1 id="#title_1" >2、疲劳、垃圾邮件、备份缺失，拖垮了GitLab.com</h1>
David Iffland
[http://www.infoq.com/cn/news/2017/02/gitlab-crash-data-loss?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/02/gitlab-crash-data-loss?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/news/2017/02/gitlab-crash-data-loss/zh/headerimage/GettyImages-469556011.jpg"/><p>生产环境数据丢失、数小时的宕机，这是GitLab给我们带来的不幸而扣人心弦的故事，这个故事告诉我们小事可以变成灾难，比如垃圾邮件、工程师疲劳状态。</p> <i>By David Iffland</i> <i> Translated by 周明耀</i>
---------------
<h1 id="#title_2" >3、Swift 4 ABI稳定性的征途</h1>
Sergio De Simone
[http://www.infoq.com/cn/news/2017/02/swift4-abi-stability-roadmap?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/02/swift4-abi-stability-roadmap?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/news/2017/02/swift4-abi-stability-roadmap/zh/headerimage/cover.jpg"/><p>最近发布在swift-evolution邮件杂志中的《Swift ABI稳定性宣言》旨在汇编所有需要解决的问题，然后宣布Swift ABI具有稳定性。 但是目前尚不完全清楚Swift 4 ABI是否具有稳定性。</p> <i>By Sergio De Simone</i> <i> Translated by Alina</i>
---------------
<h1 id="#title_3" >4、Google神经机器翻译系统实现Zero-Shot翻译</h1>
Dylan Raithel
[http://www.infoq.com/cn/news/2017/02/zero-shot-translation?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/02/zero-shot-translation?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Google的多语言神经机器翻译系统创造了一种中介语言，使其可以对以前未进行直接互译训练的语言对和短语进行翻译，他们称之为Zero-Shot翻译。

</p> <i>By Dylan Raithel</i> <i> Translated by 尚剑</i>
---------------
<h1 id="#title_4" >5、HBase 1.3 发布，性能大幅提升</h1>
Alexandre Rodrigues
[http://www.infoq.com/cn/news/2017/02/apache-hbase-1.3?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/02/apache-hbase-1.3?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>性能测试报告显示，Apache HBase 1.3.0中预写日志（WAL）特性在纯SATA磁盘里运行的平均延时减少了20%；在SATA-SSD磁盘里运行的延时减少了40%。这些改进有助于提高Apache Phoenix、OpenTSDB以及其他依赖HBase引擎做数据持久化和快速查询功能的软件项目的性能。</p> <i>By Alexandre Rodrigues</i> <i> Translated by 魏星</i>
---------------
<h1 id="#title_5" >6、Realm Mobile Platform添加水平可扩展性，支持遗留数据源和复制</h1>
Sergio De Simone
[http://www.infoq.com/cn/news/2017/02/realm-mobile-platform-1?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/02/realm-mobile-platform-1?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Realm团队宣布其Realm Mobile Platform的1.0版本，旨在通过自动实时数据同步、实时协作、实时通讯等功能为iOS和Android平台创建移动应用程序。</p> <i>By Sergio De Simone</i> <i> Translated by 刘嘉洋</i>
---------------
<h1 id="#title_6" >7、GitLab 8.16现在包括监控工具并将自动部署扩展到Google Container Engine上</h1>
Sergio De Simone
[http://www.infoq.com/cn/news/2017/02/gitlab-816-gce?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/02/gitlab-816-gce?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>继上个月在OpenShift上引入自动部署以支持Kubernetes后，GitLab 8.16在Google Cloud上提供了自动部署功能。此外，GitLab 8.16改进了问题搜索和过滤器界面，并包括监控工具Prometheus和Slack的替代者Mattermost。</p> <i>By Sergio De Simone</i> <i> Translated by 汪欣</i>
---------------
<h1 id="#title_7" >8、死而复生？RethinkDB宣布进入Linux基金会！</h1>
刘志勇
[http://www.infoq.com/cn/news/2017/02/RethinkDB-join-Linux?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/02/RethinkDB-join-Linux?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>2016年10月5日，RethinkDB联合创始人Slava Akhmechet在官网上宣布RethinkDB破产倒闭。Slava Akhmechet称其已经尽了最大的努力，最终还是无法建立一个可持续的商业模式。接下来Stripe公司将接纳RethinkDB公司，RethinkDB工程师团队将加入到Stripe。在交接过程中RethinkDB公司下的RethinkDB和Horizon的开源项目不会关闭，这两个项目都将持续可用，rethinkdb.com和horizon.io网站上的一切都可正常访问。Slava Akhmechet也希望在广大社区贡献者的努力下，保持继续开放的开发进程。 日前，RethinkDB项目有了新的动态。</p> <i>By 刘志勇</i>
---------------
<h1 id="#title_8" >9、文章： 为什么Google用Apache Beam彻底替换掉MapReduce</h1>
足下
[http://www.infoq.com/cn/articles/why-google-replace-beam-with-apache-mapreduce?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/why-google-replace-beam-with-apache-mapreduce?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/why-google-replace-beam-with-apache-mapreduce/zh/smallimage/logo2 (7).jpg"/><p>1月10日，Apache软件基金会宣布，Apache Beam成功孵化，成为该基金会的一个新的顶级项目。谷歌坚信Apache Beam就是数据批量处理和流式处理的未来。</p> <i>By  足下</i>
---------------
<h1 id="#title_9" >10、Web Development Reading List #169: TLS At Scale, Brotli Benefits, And Easy Onion Deployments</h1>
Anselm Hannemann
[https://www.smashingmagazine.com/2017/02/web-development-reading-list-169/](https://www.smashingmagazine.com/2017/02/web-development-reading-list-169/)
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
</table><p><strong>Everyone here can have a big impact on a project</strong>, on someone else. I get very excited about this when I read stories like the one about an intern at Google who did an experiment that saves tons of traffic, or when I get an email from one of my readers who now published an awesome complete beginner’s guide to front-end development.</p>
<figure></figure>
<p>We need to recognize that our industry depends on people who share their open-source code and we should support them and their projects that we heavily rely on. Finally, we also need to understand that these people perhaps don’t want a job as an employee at some big company but remain independent instead. So if you make money with a project that uses open-source libraries or other resources, maybe Valentine’s Day might be an occasion to show your appreciation and make the author a nice present.</p><p>The post .</p>
---------------