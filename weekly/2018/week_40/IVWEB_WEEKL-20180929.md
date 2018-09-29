## 文章索引
1、 <a href="#1parcel-110-typescript-31-and-lots-of-handy-js-snippets" >Parcel 1.10, TypeScript 3.1, and lots of handy JS snippets</a><br/>
2、 <a href="#2十年前端老兵学习dapp开发投身下一个浪潮" >十年前端老兵：学习DApp开发，投身下一个浪潮</a><br/>
3、 <a href="#3每周分享第-24-期" >每周分享第 24 期</a><br/>
4、 <a href="#4privacy-by-design:-how-to-sell-privacy-and-make-change" >Privacy By Design: How To Sell Privacy And Make Change</a><br/>
5、 <a href="#5文章-全球范围区块链应用情况概述" >文章： 全球范围区块链应用情况概述</a><br/>
6、 <a href="#6文章-你是创新的阻碍吗" >文章： 你是创新的阻碍吗？</a><br/>
7、 <a href="#7起底联盟链fisco-bcos-与-fabric之较" >起“底”联盟链：FISCO BCOS 与 Fabric之较</a><br/>
8、 <a href="#8实现远程团队的敏捷" >实现远程团队的敏捷</a><br/>
9、 <a href="#9hyperledger发布burrow新版本改进集成和开发体验" >Hyperledger发布Burrow新版本，改进集成和开发体验</a><br/>
10、 <a href="#10亚马逊发布aws-cloudformation宏功能" >亚马逊发布AWS CloudFormation宏功能</a><br/><h1 id="#title_0" >1、Parcel 1.10, TypeScript 3.1, and lots of handy JS snippets</h1>

[https://javascriptweekly.com/issues/405](https://javascriptweekly.com/issues/405)
<table border=0 align="center" border="0">
  <tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   ">

  <div>    
    <table border=0 border=0><tr>
<td align="left" style="padding-left: 4px; font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   "><p>#405 — September 28, 2018</p></td>
<td align="right" style="padding-right: 4px; font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   "><p></p></td>
</tr></table>
    
    <table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0 12px;"><p>JavaScript Weekly</p></td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   ">
  
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — We first linked this project last year, but it’s just had a ‘1.1’ release where lots of the snippets have been updated and improved, so if you want to do lots of interesting things with arrays, math, strings, and more, check it out.</p>
  <p>30 Seconds </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"> You can read it online for free too, or even direct from the book’s git repo.</p>
  <p>Nicolas Bevacqua </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Use Sentry's open source error tracking to get to the root cause of issues. Setup only takes 5 minutes.</p>
  <p>Sentry <span style="text-transform: uppercase; padding: 1px 4px;  margin-left: 4px; font-size: 0.9em;   color: #997 !important;">sponsor</span></p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;">.</p>
  <p>Devon Govett </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></p>
  <p>Microsoft </p>
</td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0;"><p>💻 Jobs</p></td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Our small dynamic team is looking for an experienced frontend developer to help build and iterate features for an open online community for creative collaboration.
</p>
  <p>Hitrecord </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Create a profile to connect with inspiring companies seeking JavaScript devs.</p>
  <p>Vettery </p>
</td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0;"><p>📘 Tutorials and Opinions</p></td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — A gentle and effective walkthrough of creating and animating flocks of virtual birds.</p>
  <p>Drew Cutchins </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — The latest version of V8 offers a native code coverage reporting feature and here’s how it works with Node.</p>
  <p>Benjamin Coe (npm, Inc.) </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — The node-influx client library features a simple API for most InfluxDB operations and is fully supported in Node and the browser, all without needing any extra dependencies.</p>
  <p>InfluxData <span style="text-transform: uppercase; padding: 1px 4px;  margin-left: 4px; font-size: 0.9em;   color: #997 !important;">sponsor</span></p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Dropbox </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Jake Lumetta, et al. </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Glad Chinda </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Airbnb’s extremely popular guide continues to get frequent updates.</p>
  <p>Airbnb </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>mongodb <span style="text-transform: uppercase; padding: 1px 4px;  margin-left: 4px; font-size: 0.9em;   color: #997 !important;">sponsor</span></p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Podcasts, like blogs, have a way of coming and going, but these are all ready to listen to now.</p>
  <p>François Lanthier Nadeau <span style="text-transform: uppercase; margin-left: 4px; font-size: 0.9em;  padding: 1px 4px; ">podcast</span></p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Jecelyn Yeen </p>
</td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0;"><p>🔧 Code and Tools</p></td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   ">
  
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Create interactive data tables quickly from any HTML table or JavaScript or JSON data source.</p>
  <p>Oli Folkerd </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Visual Studio Marketplace </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Build and scale interactive, immersive apps with PubNub - chat, collaboration, geolocation, device control and gaming.</p>
  <p>PubNub <span style="text-transform: uppercase; padding: 1px 4px;  margin-left: 4px; font-size: 0.9em;   color: #997 !important;">sponsor</span></p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Manage and scale a pool of headless Chrome instances for crawling sites.</p>
  <p>Apify </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Stephen Pinkerton and Zack Bloom (Cloudflare) </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — It uses the in-browser IndexedDB database client-side but can then use MongoDB as a back-end store for bi-directional sync.</p>
  <p>turtle DB </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — This is a really neat effect.</p>
  <p>Joe B. Lewis </p>
</td></tr></table>
<table border=0 border=0><tr><td style=" font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   "></td></tr></table>
</div>

  </td></tr>
</table>





<img src="https://javascriptweekly.com/open/405/rss" width="1" height="1" />
---------------
<h1 id="#title_1" >2、十年前端老兵：学习DApp开发，投身下一个浪潮</h1>
CSS 魔法
[http://www.infoq.com/cn/news/2018/09/DApp-next-Internet-wave?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/09/DApp-next-Internet-wave?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>过去的十年，可以说是 App 的十年。但未来的十年，DApp 被寄予了厚望。App 的形态是前端开发者的专长，而 DApp 将同样离不开前端开发者的参与。 “CSS 魔法”，08 年加入互联网，是一位有十年经验的前端老兵。他认为区块链将是下一个重要的节点，对区块链技术也有着自己的理解和有启示意义的看法。</p> <i>By CSS 魔法</i>
---------------
<h1 id="#title_2" >3、每周分享第 24 期</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2018/09/weekly-issue-24.html](http://www.ruanyifeng.com/blog/2018/09/weekly-issue-24.html)
<p>这里记录过去一周，我看到的值得分享的东西，每周五发布。</p>

        <p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018092801.jpg" alt="" title="" /></p>

<p>（题图：浦东滨江，上海，2018。）</p>

<p>上面，有人问："新人进入软件行业，应该学什么？"</p>

<p>很多热心人提供建议。有人说：</p>

<blockquote>
  <p>"你应该好好学习一门语言。精通一门计算机语言，可以让年轻工程师脱颖而出。这不仅对日常工作很有帮助，也有利于以后学习其他语言。学习的东西包括：设计模式、调试、性能、生态系统、标准库等等。"</p>
</blockquote>

<p>立刻有人提出相反的建议。</p>

<blockquote>
  <p>"我建议学习几种彼此非常不同的语言。例如 Java，Go 和 JavaScript。你要学到精通其中每一种语言，能够独立地从头搭建一个新项目，在该语言的生态系统中完成所有开发工作。"</p>
</blockquote>

<p>有人举出几种必须掌握的工具。</p>

<blockquote>
  <p>学习 SQL，你将能够使用任何与数据库相关的软件。 <br />
学习 HTML，你将能够创建一个通用的用户界面。 <br />
学习 GIT，你将能够与他人分享您的工作。 <br />
学习 Unix shell，你将能够部署所有的东西。 </p>
</blockquote>

<p>不少人这种说法。</p>

<blockquote>
  <p>"大多数职业（从医生到电工），多年的经验等同于多年的专业知识。但是在软件开发中，技术变化如此之快，你花费了大量时间学习技术和工具，一旦这些技术被取代，你的知识将变得毫无价值，因为它们大部分都是实施的细节。最终，所有这些年，你确实积累了一些一般性的经验，但与具体实施相关的知识，你都不再掌握了。</p>

<p>唯一留下的是那些基本的东西，你应该专注于软件开发的核心知识和数学知识，您的这些技能会不断增长，而不是随着技术潮流的变化而消失。"</p>
</blockquote>

<p>我最喜欢的是下面。</p>

<blockquote>
  <p>"不要让自己太忙碌。不过，说起来容易做起来难。</p>

<p>我们雇用新毕业的工程师时，会派给他们很多琐碎的工作，使他们饱和。他们会逐渐忘记大学里学到的课程，全部注意力都集中在手头的工作。很多人倾向于通过忙碌程度来评价自己，我相信这是一个死亡陷阱。"</p>
</blockquote>

<h2>新闻</h2>

<p>1、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018092802.jpg" alt="" title="" /></p>

<p>以前的 3D 打印，一般都使用塑料。今年，3D 金属打印机问世了，可以用金属打印零件，生成更轻、更坚固、更复杂的形状，而且成本更低、速度更快。这为复杂的金属模具和金属部件的生产带来了前所未有的便利。以后再不担心老机器的零件停产了，只要把老零件扫描一下，原样打印可以了。</p>

<p>目前，3D 金属打印机的价格不到10万美元。</p>

<p>2、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018092803.jpg" alt="" title="" /></p>

<p>英国剑桥大学的胚胎学家，只使用干细胞就培育出了一个小鼠胚胎。这里的神奇之处在于，这个胚胎没有使用卵子，也没有使用精子，只是一个普通细胞培育出来的。这意味着，只要一个普通的细胞就能创造出生命。</p>

<p>3、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018092804.jpg" alt="" title="" /></p>

<p>多伦多正在开展一个智能城市项目，在城市中安装各种类型的传感器，收集空气质量、噪声、人们活动的所有数据。所有数据将开放出来，允许第三方公司在上面开发服务。</p>

<p>以后的城市不仅将布满摄像探头，而且布满传感器。</p>

<p>4、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018092805.jpg" alt="" title="" /></p>

<p>植物人能不能醒来？中国科学院和中国人民解放军总医院开发了一个人工智能系统，评估病人醒来的机会，据说准确率达到90%。</p>

<p>一名19岁的植物人，昏迷六个月，七个神经科医生评估以后，给出了23分中的7分，这意味着他的家人可以合法拔管。但是这个系统评估脑部扫描结果后，给出了23分中的20分。结果，该青年在12个月内醒来。</p>

<p>5、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018092806.jpg" alt="" title="" /></p>

<p>越来越多的人使用电动滑板或电动滑板车，受伤的案例不断增加。鼻子、手腕和肩膀骨折、面部裂伤是常见情况，最糟糕时，摔到头部，会导致大脑永久性受损。加州的一家医院在7月的最后两周，治疗了18名在电动滑板车事故中受重伤的病人。旧金山的一家大医院的急诊室医生说，他每周看到多达10起重伤。</p>

<p>加州正准备立法，要求使用电动滑板车之前，用户必须接受安全培训，而且在使用时，必须戴头盔。</p>

<p>6、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018092807.jpg" alt="" title="" /></p>

<p>动物几乎都是对称的，左边的四肢与右边一样，这是怎么产生的？</p>

<p>澳大利亚莫纳什大学的生物学家，开展了一项试验。他们在小鼠胚胎的左后腿，注射了一种限制腿部生长的细胞，使得一条腿生长得比另一条腿慢。结果发现，那条长得慢的腿会发出信号，通知其余组织（ 包括另一条后腿），以减缓它们的生长。直到受阻的肢体赶上正常生长的腿，才会重新恢复均匀的生长。</p>

<p>7、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018092808.jpg" alt="" title="" /></p>

<p>美国的气象频道采用 3D 模拟视频，播放天气预报。</p>

<p>主持人在绿幕前录制天气预报，后面的背景用游戏引擎 Unreal Engine 4 生成。电视台将风速、方向、降雨量和无数气象数据输入系统，生成 3D渲染图，以提供准确的可视化效果。看完，我觉得以后电视剧也可以这样拍。</p>

<p>8、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018092809.jpg" alt="" title="" /></p>

<p>美国一个45岁的女自行车手 Denise Mueller-Korenek，骑出了每小时295公里（183.932英里/小时）的世界记录，成为世界上骑得最快的人。</p>

<p>她必须躲在拖车牵引的整流罩里面，防止这种速度产生的巨大风阻。而且，前1.5公里是拖车拉动前进的，以便产生150公里/小时左右的初速度。</p>

<p>9、<strong>一句话新闻</strong></p>

<ul>
<li>宣布，2045年淘汰所有化石能源，电力来源都不含碳。<br><br></li>
<li>宣布，今年年底，电池的成本有望降到100美元/千瓦时。目前，顶配的特斯拉汽车是100千万时的电池，这意味着，电动汽车的成本有望显著降低。<br><br></li>
<li>在物理、工程、数学方面发表的论文数量，已经成为了世界第一。有研究称，中国学者参与的论文占到全球论文的三分之一。不过在质量上（引用次数）还是不行，落后美国较多。<br><br></li>
<li>消息，7月份全国彩票销售额546亿元，同比增长61.9%，1-7月合计增长25.6%。去年同期的增长率只有4.2%，今年的彩票销售这么好，不知道跟经济下行有多大关系。</li>
</ul>

<h2>数据分析师课程</h2>

<p>本期《每周分享》很高兴得到了优达学城（Udacity）的支持。优达学城是国际著名的在线教育平台，中国区对课程进行汉化，并提供中文服务。</p>

<p>今天给大家推荐的，就是他们的两个级别。</p>

<blockquote>
  <ul>
<li>帮助初学者进入这个领域，通过3个月的时间，让你学会 Python 和 SQL 两大主流数据分析工具，掌握数据清洗、探索性分析、可视化等基础分析技能，并且辅导你做完"空气质量分析"、"气候是否变暖"、"网站用户行为分析"等5个实战项目。<br><br></li>
<li>适合有一定数学、Python、SQL 基础的学员，帮助大家成为一个真正的数据工程师。它也是3个月时间，教授高级的数据分析和统计方法，完成4个可以用于生产环境的真实项目。</li>
</ul>
</blockquote>

<p>你可能不确定它们是否适合自己，优达学城为此提供了299元的"七天试学班"。你可以在七天里面，体验所有服务，并且在助教指导下，自己动手完成第一个项目。到期后，如果想继续学，再缴纳其余的学费。下面是前几期课程的学员评价摘录。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018092810.jpg" alt="" title="" /></p>

<p>扫码下面海报里面的二维码，就可获取详细的课程大纲，或者咨询课程，进行选课自测。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018092811.jpg" alt="" title="" /></p>

<h2>教程</h2>

<p>1、（英文） </p>

<p>HTML 网页的 <code>&lt;input&gt;</code> 元素有几十个属性，本文介绍其中三个开发者比较不熟悉的属性。</p>

<p>2、（英文）</p>

<p>这篇文章很容易懂，解释怎么使用 serverless 服务，修改 HTTP 回应。这个服务看起来很好用，缺点好像是只有使用 Cloudflare CDN 的网站才能用。</p>

<p>3、（英文）</p>

<p>《人类简史》的作者尤瓦尔·赫拉利的最新文章。他提出，人工智能有利于政府，可以将权力集中在少数精英手里。唯一可能的解决方法，是寻找分布式的技术方案，防止资源的集中。</p>

<p>4、（英文）</p>

<p>脚本的第一行为什么以 <code>#!</code> 开头？Shell 内部又是如何处理脚本的？</p>

<p>5、（英文）</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018092812.jpg" alt="" title="" /></p>

<p>Chrome 66 支持 Presentation API，这个 API 允许浏览器定制投射到第二块屏幕的内容，使用脚本进行控制。</p>

<p>5、（英文）</p>

<p>网页可以向第三方站点发出请求，这是 CSRF 攻击的主要原因。这篇文章总结了可能发出第三方请求的七种情况。</p>

<p>6、（英文）</p>

<p>本文从协议设计的顶层角度，总体上解释互联网协议的设计思想。</p>

<p>7、（英文）</p>

<p>本文解释了 Redux 想要解决的问题，而 GraphQL 可以解决同样的问题。但是，该文没有给出细节。</p>

<p>8、（英文）</p>

<p>为了提高安全性，防止监听，DNS 查询已经可以在 HTTPS 协议上完成。这篇文章教你怎么写一个 Node 客户端，获取 DNS 信息。</p>

<p>9、（英文）</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018092813.jpg" alt="" title="" /></p>

<p>本文介绍著名的压缩算法霍夫曼编码的发明人戴维·霍夫曼的故事。</p>

<p>10、（英文）</p>

<p>本文是 V8 官方团队写的历史回顾，介绍 V8 每一年在技术上的突破。</p>

<h2>资源</h2>

<p>1、（英文）</p>

<p>这是一本互动书籍，免费，帮助读者了解如何使用 SQL 对数据集运行查询。</p>

<p>2、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018092814.jpg" alt="" title="" /></p>

<p>大数据研究需要数据集，谷歌推出数据集搜索，根据关键词找出相关的数据集。</p>

<p>3、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018092815.jpg" alt="" title="" /></p>

<p>谷歌推出了很多产品，许多后来都放弃了。这个网页列出所有被谷歌放弃的产品，目前有70个。</p>

<p>4、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018092816.jpg" alt="" title="" /></p>

<p>遇到灾难（地震、洪水、大雪等等）怎么办？东京市政府编写的免费电子书，这里是简体中文版的下载。</p>

<p>5、</p>

<p>本文给出一个可视化展示，比较不同软件的代码行数。</p>

<h2>工具</h2>

<p>1、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018092817.jpg" alt="" title="" /></p>

<p>一般情况下，Node REPL 环境只能在命令行使用。这个工具起了一个服务，让你在浏览器里就能使用 REPL 环境。</p>

<p>2、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018092818.jpg" alt="" title="" /></p>

<p>一个使用 GPU 进行渲染的终端模拟器。理论上，视觉效果将非常顺滑，尤其是长文本滚动和窗口切换。</p>

<p>3、</p>

<p>一个前端脚本，将 Markdown 文件自动转成静态网站。</p>

<p>4、</p>

<p>谁说密码一定是字符？这个网站的密码是图片。图片密码有两种用法，一种用法是上传某张图片作为密码，另一种是给定一张图片，你在上面点击几个只有自己知道的位置。</p>

<p>5、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018092819.jpg" alt="" title="" /></p>

<p>React 应用的原型设计工具。</p>

<p>6、</p>

<p>一个架设在本地的网络书签管理系统，会自动抓取书签内容，并生成标签和摘要，使用 django 框架开发。</p>

<p>7、</p>

<p>一个快速、强大的 CSV 文件的命令行处理工具，使用 Rust 语言开发。</p>

<p>8、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018092820.jpg" alt="" title="" /></p>

<p>一个在线编写五线谱的工具，可以实时听到编写的旋律。</p>

<p>9、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018092821.jpg" alt="" title="" /></p>

<p>Mac 的屏保程序，会显示一段文学作品的段落，里面包含了当前时间。</p>

<h2>文摘</h2>

<p>1、</p>

<p>有些城市位于山地，平面地图无法显示道路的坡度。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018092822.jpg" alt="" title="" /></p>

<p>设计师希望，地图能够显示道路的倾斜方向和倾斜程度，最初的想法是加上方向箭头。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018092823.jpg" alt="" title="" /></p>

<p>箭头太不直观，于是改成三角形。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018092824.jpg" alt="" title="" /></p>

<p>三角形的含义还是不清晰，考虑改成3D。不同的颜色表示不同的坡度。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018092825.jpg" alt="" title="" /></p>

<p>下面是最后的成品。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018092826.jpg" alt="" title="" /></p>

<p>2、</p>

<p>山东省济南市章丘区，一家食品垃圾回收厂接收了当地餐馆和食堂送来的大量剩饭剩菜，然后使用蟑螂进行无害化处理。剩饭剩菜通过管道注入玻璃容器中，被数百万只蟑螂吞噬。</p>

<p>对于大多数人来说，蟑螂是传播病毒和污染食物的害虫。但是，济南的技术人员李延荣花了数年时间研究蟑螂后，成功地将它们变成了食品回收工具。</p>

<p>在回收工厂，蟑螂每天食用15吨食物垃圾，占章丘餐厅和食堂产生的食物垃圾的三分之一以上。以前，大部分食物垃圾都会填埋，导致出现环境问题。现在，蟑螂可以分解废物，留下很少的残留物。蟑螂死后，它们的身体具有高蛋白质和氮化合物，将被制成蟑螂粉，用作动物饲料的蛋白质来源。</p>

<p>回收工厂同时也是蟑螂养殖基地。养殖人员表示，由于蟑螂的恢复能力和快速繁殖能力，蟑螂的数量呈指数级增长。2014年，工厂只有400公斤的蟑螂。 2015年，这一数字飙升至4吨，而今年预计将在这里生产超过3,000吨的蟑螂。</p>

<p>2008年，李延荣开始研究蟑螂。他读到，昆虫（包括蟑螂）是高蛋白质的营养食品的来源。曾经在济南一家回收公司工作的李延荣很快就有了养蟑螂的想法。他发现山东已有几家蟑螂养殖场为医药公司提供原料，但是成本高昂，因为他们使用谷物喂食蟑螂，每吨蟑螂的繁殖成本可达1万元人民币（1,527美元）。然而，零售价有时只有几十元一公斤。</p>

<p>章丘环境卫生中心主任安峰告诉李延荣，处理食物垃圾非常困难。垃圾填埋后，食物垃圾会污染地下水，给居民带来健康问题。李延荣很自然想到，那么为什么不用食物垃圾喂蟑螂呢？</p>

<p>为了测试蟑螂的饮食习惯，李延荣开始给蟑螂喂食各种食物 -- 辛辣的，酸的，甚至腐烂的。事实证明，蟑螂根本没有味觉或气味。它们还具有强大的免疫系统，可以消化几乎任何东西。他还对蟑螂粉进行了测试，发现用蟑螂粉喂养的鸡不仅更健康，而且比正常鸡更强壮，更快。鸡蛋也有较厚的壳。</p>

<p>在他研究蟑螂的三年中，李申请了30多项专利，其中两项获得批准。 2014年，他找到了安峰，并询问环境卫生中心是否可以免费为他提供食品垃圾。政府很高兴这样做，因为它是垃圾填埋场的更好替代品。2015年底，李延荣辞去了工作，开办了自己的公司，全身心地投入到蟑螂和回收工厂。</p>

<h2>本周图片</h2>

<p>1、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018092827.jpg" alt="" title="" /></p>

<p>1985年个人 PC 刚刚诞生，那时报纸上的饼图都是手绘的。</p>

<p>2、</p>

<p>如果变量是一个布尔值，变量名最好加上 is、has 或 can 作为前缀（见下图）。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018092828.jpg" alt="" title="" /></p>

<p>3、</p>

<p>丹麦第二大城市奥胡斯，在海港里建设了一个浮动的海水浴场。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018092829.jpg" alt="" title="" /></p>

<p>游泳池长50米，还设有儿童游泳池和跳水池，以及日光浴甲板，供人们享受阳光。整个设施一共可以容纳650人。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018092830.jpg" alt="" title="" /></p>

<h2>本周金句</h2>

<p>1、</p>

<p>作为一个决策者，你的职责不是做出很多决定，而是只需做出几个高质量的决定。</p>

<p>如果我每天做出三个不错的决定，就很满意了。巴菲特说，他的一年就是做对三个投资决定。</p>

<p>-- ，亚马逊公司创始人</p>

<p>2、</p>

<p>各大网站对用户的监控无所不在，为了提供服务，它们必须这么做。事实上，如果不提供那些基于用户数据分析的功能，你还会觉得它们的功能不够好。</p>

<p>这注定了隐私已经不复存在。唯一的应对方法就是双向透明，网站可以监控用户行为，那么用户也必须能够监督网站，知道网站怎么使用用户数据。</p>

<p>-- Tim O'Reilly 《未来地图》</p>

<h2>欢迎订阅</h2>

<p>这个专栏每周五发布，同步更新在我的。</p>

<p>微信搜索"<strong>阮一峰的网络日志</strong>"或者扫描二维码，即可订阅。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2018/bg2018042311.jpg" alt="" title="" /></p>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2018-09-28T08:41:06+08:00">2018年9月28日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>文集：</li>
<li>社交媒体：</li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------
<h1 id="#title_3" >4、Privacy By Design: How To Sell Privacy And Make Change</h1>
Joe Toscano
[https://www.smashingmagazine.com/2018/09/privacy-by-design/](https://www.smashingmagazine.com/2018/09/privacy-by-design/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/09/privacy-by-design/" />
              <title>Privacy By Design: How To Sell Privacy And Make Change</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>Privacy By Design: How To Sell Privacy And Make Change</h1>
                  
                    
                    <address>Joe Toscano</address>
                  
                  <time datetime="2018-09-28T13:50:13&#43;02:00" class="op-published">2018-09-28T13:50:13+02:00</time>
                  <time datetime="2018-09-28T21:41:47&#43;00:00" class="op-modified">2018-09-28T21:41:47+00:00</time>
                </header>
                <p>Privacy is a fundamental human right that allows us to be our true selves. It’s what allows us to be weirdos without shame. It allows us to have dissenting opinions without consequence. And, ultimately, it’s what allows us to be free. This is why many nations have strict laws concerning privacy. However, in spite of this common understanding, privacy on the Internet is <strong>one of the least understood and poorly defined topics to date</strong> because it spans a vast array of issues, taking shape in many different forms, which makes it incredibly difficult to identify and discuss. However, I’d like to try to resolve this ambiguity.</p>

<p>In the United States, it is a federal offense to open someone’s mail. This is considered a criminal breach of privacy that . Metaphorically speaking, each piece of data we create on the Internet &mdash; whether photo, video, text, or something else &mdash; can be thought of as parcel of mail. However, unlike opening our mail in real life, Internet companies can legally open every piece of mail that gets delivered through their system without legal consequence. Moreover, they can make copies of it as well. What these companies are doing would be comparable to someone opening our mail, copying it at Kinkos, then storing it in a file cabinet with our name on it and sharing it with anyone willing to pay for it. Want to open that file cabinet or delete some of the copies? Too bad. Our mail is currently considered their property, and <strong>we have almost no control over how it gets used</strong>.</p>

<p>Could you imagine the outrage the public would experience if they found out that the postal service was holding their mail hostage and selling it to whoever was willing to pay? What’s happening with data on the Internet is no different, and it’s time this changes.</p>

<p>It’s more than just a matter of ethics that this happens, it’s a matter of basic human rights.</p>

<p>The problem with making the changes that need to be made (without changes being forced into place by regulation) is putting dollar signs to the issues. What is the financial return on a 20,000-hour engineering investment to improve consumer privacy standards? Are consumers demanding these changes? Because if it doesn’t make a fiscal return and consumers aren’t demanding it, then why should change be made? And even if they are and there is a return, what does 20,000 hours of investment even look like? What is going to be put on the product roadmap and when? These are <strong>all valid concerns that need to be addressed</strong> in order to help us move forward effectively. So, let’s discuss.</p>

<p><strong>Recommended reading</strong>: <em></em></p>



  <aside class="product-panel product-panel__tilted product-panel--book" data-audience="non-subscriber">
    <div class="container product-panel--book__container">
      <div class="panel__description panel__description--book">

    <p>Meet .</p>
    <a href="https://smashed.by/confpanelspeakers" class="btn btn--green btn--large">
      Check all topics&nbsp;and&nbsp;speakers&nbsp;↬
    </a>
      </div>
      <div class="panel__image panel__image--book">

  <a href="https://www.smashingconf.com/ny-2018/" class="books__book__image">
  <div class="books__book__img">
          <img src="https://www.smashingmagazine.com/images/smashing-cat/cat-scubadiving-panel.svg" alt="Smashing TV, with live sessions for professional designers and developers." width="310" height="400">
        </div>
      </a>
      </div>
    </div>
  </aside>




<h3>Do Consumers Want It?</h3>

<p>The answer to this question is a hard yes. Findings by Pew Research Center show that  are “very confident” that government agencies can keep them secure.</p>

<p>Now, I know what you’re thinking. This is consumer demand, and until those consumers start leaving old products behind, there’s no fiscal reason to make any change. And (although I don’t agree with your logic) you’re right. Right now there is little fiscal reason to make any change. However, when consumer demand reaches a critical mass, things always change. And the businesses that lead the way before the change is demanded always win in the long run. <strong>Those who refuse to make a change until they’re forced to always feel the most pain</strong>. History shows this to be the truth. But what’s going to happen in legislation that will change business so much? Great question.</p>

<p>What’s about to happen to data protection and privacy standards across the world, through regulation, will not be so different than what occurred less than a decade ago when consumers demanded protection from spam emails, which resulted in the CAN-SPAM Act in the United States &mdash; but on a much greater scale, and with exponentially greater impact. This , which was created because consumers were sick of getting spam emails, set the rules for commercial email, established requirements for commercial messages, gave recipients the right to have individuals and companies stop emailing them, and spelt out tough penalties for violations. As we enter a period where <strong>consumers are beginning to understand just how badly they’ve been deceived</strong> (for years, giving people intimate control of their data will undoubtedly be the future of data collection) &mdash; whether that be through free will or legislation. And those who choose to move first will win. Don’t believe me?</p>

<p>Consider the fact that , the beginning of what will be a long fight. These examples are just a peek into what’s coming. The people are demanding more, and we’re reaching the tipping point.</p>

<p>The first to take steps to respond to this demand is the EU, which established the GDPR, and now policymakers in other countries are beginning to follow suit, working on laws in their country to define our cyber future. For example, United States Senate Intelligence Committee Vice Chairman, Mark Warner recently laid out some of ideas in .</p>

<p>What we’re seeing is a human reaction to incredible manipulation. No matter how domesticated we may be compared to previous generations, people will always push back when they feel they’re being threatened. It’s a natural reaction that has allowed us to survive for millennia. Today, tech has become more than just a consumer-facing industry. It is now <strong>also becoming a matter of national security</strong>. And for this reason, there will be a reaction whether we like it or not. And it will be better if we come out with a strategy to prepare instead of getting swept under the rug. So, what’s the financial return you ask? Well, how much is your business worth? That’s how much.</p>

<p><strong>Recommended reading</strong>: <em></em></p>

<div class="sponsors__wide-place"></div>




<p>For a simple framework of what exactly needs to be addressed and why, we can hold several truths to be foundational in the creation of digital systems:</p>

<ol>
<li><strong>Privacy must be proactive, not reactive, and must anticipate privacy issues before they reach the user.</strong><br />These issues are not issues that we want to deal with after a problem has come to life but are instead issues we want to prevent entirely, if possible. </li>
<li><strong>Privacy must be the default setting.</strong><br />There is no “best for business” option in regards to privacy; this is an issue that is about what’s best for the consumer, which, in the long run, will be better for the business. We can see what happens when coercive flaws are exposed to the public through what happened to Paypal and Venmo in August 2018 when  to the brand. More of this is sure to come to the businesses that wait for something bad to happen before making a change. </li>
<li><strong>Privacy must be positive sum and should avoid dichotomies.</strong><br />There is no binary relationship to be had with privacy; it is a forever malleable issue that needs constant oversight and perpetual iteration. Our work doesn’t end at the terms and service agreement, it lasts forever, and should be considered a foundational element of your product that evolves with the product and enables consumers to protect themselves &mdash; not one that takes advantage of their lack of understanding. </li>
<li><strong>Privacy standards must be visible, transparent, open, documented and independently verifiable.</strong><br />There’s no great way to define a litmus test for your privacy standards, but a couple of questions we should all ask ourselves as business people are: First, if the press published your privacy agreement, would it be understandable? Second, if it were understandable, would consumers enjoy what they read? And last but not least, if not, what do you need to change? </li>
</ol>

<p>These principles will be highly valuable foundations to keep in mind as products are built and evolve. They represent quick and easy questions to ask yourself and your team that will allow you to have a good baseline of ethics, but for a lengthier piece on legal foundations you can read more from . And for a full list of things to inspect during a Privacy Impact Assessment (PIA), you can also check out how assessments are done according to:</p>

<ul>
<li></li>
<li></li>
<li></li>
</ul>

<p>But before rushing off to make changes in your product, first let’s point out some of the current flaws out in the wild and talk about what change might look like once they are implemented properly.</p>

<h3>How To Make Change</h3>

<p>One of the biggest problems with US privacy practices is how hard it is to understand terms and service agreements (T&S), which play a major role in defining privacy but tend to do so very poorly. Currently, users are forced to read long documents full of legal language and technical jargon if they hope to understand what they’re agreeing to. One study actually demonstrated that it would take approximately 201 hours (nearly ten days) per year for the average person <strong>to read every privacy policy they encounter on an annual basis</strong>. The researchers estimated that the value of this lost time would amount to nearly $781 billion per year, which is beyond unacceptable considering these are the rules that are supposed to protect consumers &mdash; rules that are touted to be easy and digestible. This puts consumers in a position where they’re forced to opt-in without truly understanding what they’re getting into. And in many cases it’s not even the legal language that’s coercive, it’s the way options are given, in general, as clearly proven across various experiences:</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8f222c1a-cb7a-479e-b6b8-21fa43e30e7a/img01-consentassumed.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8f222c1a-cb7a-479e-b6b8-21fa43e30e7a/img01-consentassumed.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8f222c1a-cb7a-479e-b6b8-21fa43e30e7a/img01-consentassumed.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8f222c1a-cb7a-479e-b6b8-21fa43e30e7a/img01-consentassumed.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8f222c1a-cb7a-479e-b6b8-21fa43e30e7a/img01-consentassumed.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8f222c1a-cb7a-479e-b6b8-21fa43e30e7a/img01-consentassumed.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8f222c1a-cb7a-479e-b6b8-21fa43e30e7a/img01-consentassumed.png"
			sizes="100vw"
			alt="This image shows what many sites currently do to collect consent in a way that assumes consent and gets the consumer to agree in a way that is dangerous."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			When consent is collected this way, it is assumed. ()
		</figcaption>
	
</figure>


<p>The example given above is generic wireframe, but I chose to do this because we’ve all seen patterns like this and others like it that are related to collecting more specific types of data. I could list specific examples, but the list would go on forever and there’s no reason to list off specific companies demonstrating manipulative patterns because these patterns (and other, very similar patterns) can be found on nearly every single website or app on the Internet. There’s one major problem with asking for consent this way: Consumers aren’t allowed to <em>not accept</em> terms and services without several extra steps, lots of reading, and often much more. This is <strong>a fundamental flaw that needs to be addressed</strong> because asking for consent means there needs to be an option to say no, and in order to know whether “no” is the best option, consumers need to understand what they’re consenting to. However, products aren’t built that way. Why? Well, it’s best for business.</p>

<p>If we really sit and think about this, what’s easy to see but let go unrecognized is that companies spend more time creating splash pages to explain how to use the app than we do to explain what data is being collected and why. Why? Simple changes to the way T&S agreements are made would not only make consumers more aware of what they’re signing up for, but also <strong>allow them to be more responsible consumers</strong>. We can see some of these changes already being made due to the impact the GDPR has been having across the world. In many European nations, it is not uncommon for consent to be asked through modals like these:</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8f473376-5889-48df-9927-e635cb068085/img02-benefitsrecognized.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8f473376-5889-48df-9927-e635cb068085/img02-benefitsrecognized.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8f473376-5889-48df-9927-e635cb068085/img02-benefitsrecognized.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8f473376-5889-48df-9927-e635cb068085/img02-benefitsrecognized.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8f473376-5889-48df-9927-e635cb068085/img02-benefitsrecognized.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8f473376-5889-48df-9927-e635cb068085/img02-benefitsrecognized.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8f473376-5889-48df-9927-e635cb068085/img02-benefitsrecognized.png"
			sizes="100vw"
			alt="In this image, the benefits of giving consent have been recognized, but there is still room for improvement."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			In this image, the benefits of giving consent have been recognized. ()
		</figcaption>
	
</figure>


<p>This first example is a good step forward. It tells the consumer what their data will be used for, but it’s still lacking transparency about where the data will be going and giving priority to the agreement without an option to decline. It also jams everything into a single body of text, which makes the information much less digestible.</p>

<p>A better example of how this might be designed is something like the modal below, which is now common among many European sites:</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a27b4d70-1964-42c7-98e7-25ed69e95359/img03-europeangdpr.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a27b4d70-1964-42c7-98e7-25ed69e95359/img03-europeangdpr.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a27b4d70-1964-42c7-98e7-25ed69e95359/img03-europeangdpr.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a27b4d70-1964-42c7-98e7-25ed69e95359/img03-europeangdpr.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a27b4d70-1964-42c7-98e7-25ed69e95359/img03-europeangdpr.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a27b4d70-1964-42c7-98e7-25ed69e95359/img03-europeangdpr.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a27b4d70-1964-42c7-98e7-25ed69e95359/img03-europeangdpr.png"
			sizes="100vw"
			alt="This image shows how consent is asked across many sites in Europe, in order to comply with the General Data Protection Regulation (GDPR) and give consumers better options. It’s still not what they need though."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			After GDPR compliance became an issue, many more options were given but improvements could still be made. ()
		</figcaption>
	
</figure>


<p>This gives consumers a comprehensive understanding of what their data will be used for and does it in a digestible manner. However, it still lacks any significant information about where the data will be going after they consent. There’s not a single clue as to where their data will be shared, who it will be shared with, and what limitations exist within those agreements. While this is much better than the majority of options on the web, there are still improvements to be made.</p>

<h4>Third-Party Login Prompt</h4>

<p>For example, when using a third-party service to log into your platform, consumers should be made well aware of the following:

<ol>
<li>What data is going to be taken from the third-party;</li>
<li>What it’s being used for and how it might affect their experience if you don’t have access to it;</li>
<li>Who else has or might have access to it.</li>
</ol>

<p>To implement this in a way that gives the consumer control, this experience should also allow consumers to opt-in to individual parts of the collection, not be forced to agree to everything or nothing at all.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/19edb5f9-fdd9-45e9-8889-c70ed20b16de/img04-3rdpartylogin.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/19edb5f9-fdd9-45e9-8889-c70ed20b16de/img04-3rdpartylogin.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/19edb5f9-fdd9-45e9-8889-c70ed20b16de/img04-3rdpartylogin.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/19edb5f9-fdd9-45e9-8889-c70ed20b16de/img04-3rdpartylogin.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/19edb5f9-fdd9-45e9-8889-c70ed20b16de/img04-3rdpartylogin.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/19edb5f9-fdd9-45e9-8889-c70ed20b16de/img04-3rdpartylogin.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/19edb5f9-fdd9-45e9-8889-c70ed20b16de/img04-3rdpartylogin.png"
			sizes="100vw"
			alt="This mock-up shows a generic version of how a site might ask for consent when using a 3rd party login on their site. It demonstrates how listing a bunch of variables is no good and why we need to ask for consent on each point individually."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			By forcing consumers to check off at each point, it adds friction to the process, yes, but also makes sure the content is digestible. ()
		</figcaption>
	
</figure>


<p>This would make the T&S digestible and allow consumers to opt into what they truly agree to, not what the company wants them to agree to. And to make sure it’s truly opt-in, the default should be set to opt-out. This would be a small change that would make a dramatic difference in the way consent is asked for. Today, <strong>most companies blanket this content in legal jargon</strong> to hide what they’re really interested in, but the days of asking for consent in this way are quickly coming to an end.</p> 

<p>If you’re providing consumers with a meaningful service, and doing so ethically, these changes shouldn’t be an issue. If there is a true value to the service, consumers are not going to resist your ask. They just want to know who they can and cannot trust, and this is one simple step that can help your business prove its trustworthiness.</p>

<h4>Single- And Multi-Point Data Collection Requests</h4>

<p>Next, when it comes to creating understandable T&S agreements for your platform, we have to consider how this might play out more contextually &mdash; within the application experience. Keep in mind that if it’s all given up front, that’s not digestible. For this reason, <strong>data collection request should happen contextually</strong>, when the consumer is about to use part of your service that requires an extra layer of data to be collected.</p>

<p>To demonstrate how this ask may occur, here are a couple of examples of what a single- and multi-point data collection request might look like:</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/96280340-0865-48de-b38f-1f07e65506bb/datarequests-new.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/96280340-0865-48de-b38f-1f07e65506bb/datarequests-new.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/96280340-0865-48de-b38f-1f07e65506bb/datarequests-new.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/96280340-0865-48de-b38f-1f07e65506bb/datarequests-new.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/96280340-0865-48de-b38f-1f07e65506bb/datarequests-new.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/96280340-0865-48de-b38f-1f07e65506bb/datarequests-new.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/96280340-0865-48de-b38f-1f07e65506bb/datarequests-new.png"
			sizes="100vw"
			alt="These mockups show what it might look like when asking for permission to use specific points of data. This includes showing people what their data is being used for, why it’s important to that process, and allowing them to opt-in or -out of each individual point, without having to read through a long list of legal jargon in the terms and service agreement."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Single- and multi-point data requests can be designed to reduce the complexity of current terms of service agreements. ()
		</figcaption>
	
</figure>


<p>Breaking the T&S down into digestible interaction points within the experience instead of asking the user for everything up front allows them to get a better understanding of what’s going on and why. If you don’t need the data to improve the experience, why is it being collected? And if it’s being collected for frivolous reasons that only benefit the company, then be honest. That’s just basic honesty, which unfortunately is considered revolutionary, progressive customer service in the modern world.</p>

<p>The biggest key to these initial asks is that <strong>none of this should be opt-in by default</strong>. All initial triggers should give the people using the tool to opt-in if they choose and use it without opting in if they choose. The days of forced opt-in (or, worse yet, coercive opt-in) are coming to an abrupt halt, and those who lead the way will stay ahead of the pack for a long time to come.</p>

<h4>Data Control Center</h4>

<p>Beyond asking for consent in a meaningful way, it will also be important that we give consumers the ability to control their data post-hoc. Consumers’ access to control <em>their data</em> should not end at the terms and service agreement. Somewhere in their account controls, there should also be a place (or places) where consumers can control their data on the platform after they’ve invested time with the service. This area should show them what data is being collected, who it’s being shared with, how they can remove it, and much more.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/21685916-6c22-411d-86b4-74836d8b8c3f/img06-datacontrols.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/21685916-6c22-411d-86b4-74836d8b8c3f/img06-datacontrols.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/21685916-6c22-411d-86b4-74836d8b8c3f/img06-datacontrols.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/21685916-6c22-411d-86b4-74836d8b8c3f/img06-datacontrols.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/21685916-6c22-411d-86b4-74836d8b8c3f/img06-datacontrols.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/21685916-6c22-411d-86b4-74836d8b8c3f/img06-datacontrols.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/21685916-6c22-411d-86b4-74836d8b8c3f/img06-datacontrols.png"
			sizes="100vw"
			alt="This mockup displays the way to create data controls that inform the consumer not only of what data is being used, but where it’s going, and it allows consumers to intimately control those flows of data in a way they feel safe with."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			While we can often download our data now, we generally have no, or very little, control over it. This needs to change. ()
		</figcaption>
	
</figure>


<p>The idea of full data control may seem incredibly liberal, but it is no doubt the future. And as the property of the consumer creating the data, it should be considered a basic human right. There’s no reason why this should be a debate at this point in history. Data represents the story of our lives &mdash; collectively &mdash; and combined it creates vast amounts of power against those who create it, especially if we allow the systems to remain black boxes. So, beyond giving consumers access to their data, as we’ve discussed in the previous sections, we’ll also need to make the experience more understandable so that consumers can defend themselves.</p>

<div class="sponsors__wide-place"></div>




<h4>Create Explainable AI</h4>

<p>While it is incredible to get a suggested result that shows us things we want before we even knew we wanted them, this also puts machines in a powerful position they are not yet ready to uphold alone. When <strong>machines are positioned as experts</strong> and perform at a level that is intelligent enough to pass as such, the public will generally trust them until they fail. However, if machines fail in ways the public is incapable of understanding, they will remain expert despite their failure, which is one of the greatest threats to humanity.</p>

<p>For example, if someone were to use a visual search tool to identify the difference between an edible mushroom and a poisonous mushroom, and they didn’t know that the machine told them a poisonous mushroom was safe, that person could die. Or what happens when .</p>

<p>To ensure the public is capable of understanding what’s happening behind the scenes we need to create what DARPA calls explainable artificial intelligence (XAI) &mdash; tools that explain how machines make their decisions and the accuracy with which these tasks have been achieved. This isn’t about giving trade secrets away but allowing consumers to feel like they can trust these machines and defend themselves if an error were to occur.</p>

<p>Although it is not based in artificial intelligence, a good example of what this might look like is CreditKarma, which allows people to have a better understanding of their credit score &mdash; a system that used to be hidden just like algorithms are today. This tool allows consumers to have a better understanding of what’s happening behind the scenes and debate the legitimacy of their results if they believe the system has failed. Similar tools are being created with systems like  but these systems are just beginning to scratch the surface of explainable AI.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/019b427b-76e2-4db7-a715-db7af9b4a78d/img07-explainableai-wild.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/019b427b-76e2-4db7-a715-db7af9b4a78d/img07-explainableai-wild.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/019b427b-76e2-4db7-a715-db7af9b4a78d/img07-explainableai-wild.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/019b427b-76e2-4db7-a715-db7af9b4a78d/img07-explainableai-wild.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/019b427b-76e2-4db7-a715-db7af9b4a78d/img07-explainableai-wild.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/019b427b-76e2-4db7-a715-db7af9b4a78d/img07-explainableai-wild.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/019b427b-76e2-4db7-a715-db7af9b4a78d/img07-explainableai-wild.png"
			sizes="100vw"
			alt="The image includes screenshots from Google Maps and Netflix to demonstrate how it might look to make a system that explains its decisions. Both are good first steps, but there is much improvement to be made."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Here we see systems that attempt to explain the machine’s decision on a very superficial level. This is a good start, but we need better. ()
		</figcaption>
	
</figure>


<p>Despite these efforts, most algorithms today dictate our experience based on what a company thinks we want. But consumers should no longer be invisibly controlled by large, publicly traded corporations. <strong>Consumers should have the right to control their own algorithm</strong>. This could be something as simple as letting them know what variables are used for what parts of the experience and how changing the weights of each variable will impact their experience, then giving them the ability to tweak that until it fits their needs &mdash; including turning the algorithm off completely, if that’s what they prefer. Whether this would be a paid feature or a free feature is still up for debate, but what is not debatable is whether this freedom should be offered.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/33698c84-be0a-4b98-8b7e-ff84215ec423/img08-explainableai.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/33698c84-be0a-4b98-8b7e-ff84215ec423/img08-explainableai.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/33698c84-be0a-4b98-8b7e-ff84215ec423/img08-explainableai.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/33698c84-be0a-4b98-8b7e-ff84215ec423/img08-explainableai.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/33698c84-be0a-4b98-8b7e-ff84215ec423/img08-explainableai.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/33698c84-be0a-4b98-8b7e-ff84215ec423/img08-explainableai.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/33698c84-be0a-4b98-8b7e-ff84215ec423/img08-explainableai.png"
			sizes="100vw"
			alt="The mockup shows how we might make artificial intelligence that explains itself in a way that consumers are capable of using and controlling themselves, instead of the control being left to the hands of privately held or publicly traded corporations."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Algorithm controls will be the future of business. Could this be a way to generate service revenue instead of relying solely on ads? Should it be free? ()
		</figcaption>
	
</figure>


<p>While the example above is a generic proposal, it begins to imagine how we might make the experience in more specific situations. By giving consumers the ability to understand their data, the way it’s being used, and how that affects their lives, we will have designed a system that puts consumers in control of their own freedom.</p>

<p>However, no matter how well these changes are made, we must also realize that giving people better control of their privacy does not automatically imply a safer environment for consumers. In fact, it may make things worse. Studies have shown that <strong>giving people better control of their data actually makes it more likely that they’ll provide more sensitive information</strong>. And if the consumer is unaware of how that data may be used (even if they know where it's being shared), this puts them in harm’s way. In this sense, giving consumers better control of their data and expecting it to make the Internet safer is like putting a nutrition label on a Snickers and expecting it to make the candy bar less fattening. It won’t, and people are still going to eat it.</p>

<p>While I do believe that consumers have a fundamental right to better privacy controls and greater transparency, I also believe it is our job, as data-literate technologists to not only build better systems but also to help the public understand Internet safety. So, the last step in bringing this together is to bring awareness to the fact that control isn’t all consumers need. They also need to understand what is happening on the backend &mdash; and why. This doesn’t necessarily mean providing them with source code or giving away their IPs, but at least <strong>providing them with enough information to understand what’s going on</strong> at a base level, as a matter of safety. And in order to achieve this, we’ll need to push beyond our screens. We’ll need to extend our work into our communities and help create that future.</p>

<p><strong>Recommended reading</strong>: <em></em></p>

<h3>Incentivize Change</h3>

<p>Giving up privacy is something the population has been corralled into due to the monopolies that exist in the tech world, consumers’ misunderstanding of why this is so dangerous within, and a lack of tactical solutions associated with fiscal returns. However, this is a problem that needs to be solved. As Barack Obama noted in his administration’s summary of concerns about internet privacy:</p>

<blockquote>“One thing should be clear: Even though we live in a world in which we share personal information more freely than in the past, we must reject the conclusion that privacy is an outmoded value. It has been at the heart of our democracy from its inception, and we need it now more than ever.”</blockquote>

<p>Creating trustworthy and secure data-sharing experiences will be one of the biggest challenges our world will face in the coming decades.</p>

<p>We can look at how Facebook’s stock dropped 19 percent in one day after announcing they’re going to re-focus on privacy efforts as proof of how difficult making these changes may be. This is because investors who have recently been focused on the short-term revenue growth know how badly companies need to implement better strategies, but also realize <strong>the cost involved if the public starts to question a business</strong> &mdash; and Facebook’s public statement admitting this startled the sheep.</p>

<p>While the process will not be easy (and at many times may be painful), we all know that privacy is the soft underbelly of tech and it’s time to change that. The decisions being made today will pay off big in the long run; a stark difference to the short-term, quarterly mindset that has come to dominate business in the past decade or so of growth. Thus, discovering creative ways to make these issues a priority for all stakeholders should be considered essential for businesses and policymakers alike, which means our job as technologists needs to extend beyond the boardroom.</p>

<p>For example, a great way to incentivize these changes beyond discussing the numbers and issues brought up in this article would be through tax breaks for companies that allocate large amounts of their budget to improving their systems. Breaks could be given to companies that decide to <strong>supply regular training or workshops for their staff</strong> to help make privacy and security a priority in the company culture. They could be given to companies that hire professional hackers to find loopholes in their systems before attacks occur. They could be given to those who allocate large amounts of hours to restructuring their business practices in a way that benefits consumers. In this sense, such incentives would not be so different than tax breaks given to businesses that implement eco-friendly practices.</p>

<p>The idea of tax breaks may sound outrageous to some, but incentives such as these would represent a more proactive solution than the way things are handled now. While it may feel good to read a headline stating “Google fined a record $5 billion by the EU for Android antitrust violations,“ we must keep in mind that fines like this only represent a small fraction of such companies’ revenue. Combine this with the fact that most cases take several years or decades to conclude, and that percentage only gets smaller. With this for consideration, the idea of tax breaks can be approached from a different perspective, which is that they are not about rewarding previously negligent behavior but about <strong>increasing public safety in a way that is in the best interest of everyone involved</strong>. Maintaining our current system, which allows companies to string out court cases while they continue their malpractices is just as, if not more, dangerous than having no laws at all.</p>

<p>If you enjoyed reading this article and think others should read it as well, please help spread the word.</p>

<p><em>This article is the beginning of a series of articles I will be writing about dedicated to Internet safety, in which I will work to put fiscal numbers to ethical design patterns so that we, as technologists can change the businesses we’re building and create a better culture surrounding the development of internet-connected experiences.</em></p>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(il, ra, yk)</span>
</div>


              </article>
            </body>
          </html>
---------------
<h1 id="#title_4" >5、文章： 全球范围区块链应用情况概述</h1>
Mann Matharu
[http://www.infoq.com/cn/articles/an-overview-on-how-blockchain-is-being-used-around-world?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/an-overview-on-how-blockchain-is-being-used-around-world?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/an-overview-on-how-blockchain-is-being-used-around-world/zh/smallimage/GettyImages-544982936+copy-1537642075965.jpg"/><p>区块链已受到了广泛的关注，其实施已经超越了加密货币本身，并已在越来越多的公司和组织中落地。尽管不少人对比特币的未来发展充满疑虑，但大多数技术专家都绝对认可区块链的未来。区块链正在全球范围内得到开发，并以多种方式使用。</p> <i>By Mann Matharu</i> <i> Translated by 盖磊</i>
---------------
<h1 id="#title_5" >6、文章： 你是创新的阻碍吗？</h1>
Robert Zazueta
[http://www.infoq.com/cn/articles/barrier-innovation?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/barrier-innovation?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/barrier-innovation/zh/smallimage/barrier-to-innovation-logo-small-1536317162697-1537636688556.jpg"/><p>你已采用SOA和微服务等技术来保持基础设施的与时俱进。 那你为什么还要努力创新呢？ 这不是技术问题，而是文化问题。Rob Zazueta解释了如何专注于敏捷文化可能对组织更有利，而不是采用最新的架构趋势。</p> <i>By Robert Zazueta</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_6" >7、起“底”联盟链：FISCO BCOS 与 Fabric之较</h1>
付晓岩
[http://www.infoq.com/cn/news/2018/09/uncover-consortium-blockchain?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/09/uncover-consortium-blockchain?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>在国家政策的鼓励下，区块链技术的研发与推广正在不断升温，技术、标准、平台、框架都在持续发展，这其中，既有来自国外的布道者，也有源自国内的探索者。做为区块链三大部署形态之一的联盟链，因其与现实场景的高度契合性，正在出现越来越多的落地实例。</p> <i>By 付晓岩</i>
---------------
<h1 id="#title_7" >8、实现远程团队的敏捷</h1>
Angela Wick
[http://www.infoq.com/cn/news/2018/09/being-agile-remote?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/09/being-agile-remote?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>最近举办的Agile2018大会上，Shane Hastie和Shannon Ewan讨论了分布式敏捷团队和如何运作它们的相关内容。他们探讨了高性能团队的实施，远程团队的谣言以及让远程团队正常运作的策略，他们还分享了自己在ICAgile（完全远程的团队和组织）的工作经历。</p> <i>By Angela Wick</i> <i> Translated by 刘嘉洋</i>
---------------
<h1 id="#title_8" >9、Hyperledger发布Burrow新版本，改进集成和开发体验</h1>
Kent Weare
[http://www.infoq.com/cn/news/2018/09/Hyperledger-Burrow-DevExperience?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/09/Hyperledger-Burrow-DevExperience?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>在最近的一篇博文中，Hyperledger开源项目宣布了下一个版本的Burrow，v.0.21.0。这个版本改进了集成、密钥签名、Helm Charts for Kubernetes及开发体验。</p> <i>By Kent Weare</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_9" >10、亚马逊发布AWS CloudFormation宏功能</h1>
Steef-Jan Wiggers
[http://www.infoq.com/cn/news/2018/09/aws-cloudformations-macros?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/09/aws-cloudformations-macros?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>借助AWS CloudFormation，开发人员可以建模并定义他们的基础设施即代码（IaC）。亚马逊发布了一项名为Macros的AWS CloudFormation新功能，开发人员可以通过调用基于AWS Lambda Function的转换来扩展CloudFormation模板的原生语法。</p> <i>By Steef-Jan Wiggers</i> <i> Translated by 无明</i>
---------------