## 文章索引
1、 <a href="#1中文技术文档的写作规范" >中文技术文档的写作规范</a><br/>
2、 <a href="#2网络文凭你要不要" >网络文凭，你要不要</a><br/>
3、 <a href="#3npm-scripts-使用指南" >npm scripts 使用指南</a><br/>
4、 <a href="#4react-技术栈系列教程" >React 技术栈系列教程</a><br/>
5、 <a href="#5redux-入门教程三react-redux-的用法" >Redux 入门教程（三）：React-Redux 的用法</a><br/>
6、 <a href="#6redux-入门教程二中间件与异步操作" >Redux 入门教程（二）：中间件与异步操作</a><br/>
7、 <a href="#7redux-入门教程一基本用法" >Redux 入门教程（一）：基本用法</a><br/>
8、 <a href="#8content-security-policy-入门教程" >Content Security Policy 入门教程</a><br/>
9、 <a href="#9亚马逊如何变成-soa面向服务的架构" >亚马逊如何变成 SOA（面向服务的架构）？</a><br/>
10、 <a href="#10程序员小测试保守派-vs-自由派" >程序员小测试：保守派 vs 自由派</a><br/>
11、 <a href="#11软件架构入门" >软件架构入门</a><br/>
12、 <a href="#12https-升级指南" >HTTPS 升级指南</a><br/>
13、 <a href="#13http-协议入门" >HTTP 协议入门</a><br/>
14、 <a href="#14那些无用的人----人类简史读后感" >那些无用的人----《人类简史》读后感</a><br/>
15、 <a href="#15布尔代数入门" >布尔代数入门</a><br/>
16、 <a href="#16this-weeks-javascript-news-issue-307" >This week's JavaScript news, issue 307</a><br/>
17、 <a href="#17this-weeks-javascript-news-issue-306" >This week's JavaScript news, issue 306</a><br/>
18、 <a href="#18yarn---a-new-super-speedy-js-package-manager-from-facebook" >Yarn - a new, super-speedy JS package manager from Facebook</a><br/>
19、 <a href="#19state-of-javascript-2016-results-vue-20-released-angular-2-vs-react-comparison" >State of JavaScript 2016 results, Vue 2.0 released, Angular 2 vs React comparison</a><br/><h1 id="#title_0" >1、中文技术文档的写作规范</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2016/10/document_style_guide.html](http://www.ruanyifeng.com/blog/2016/10/document_style_guide.html)
<p>很多人说，不知道怎么写文档，都是凭着感觉写。</p>

        <p>网上也很少有资料，教你写文档。这已经影响了中文软件的发展。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2016/bg2016101801.jpg" alt="" title="" /></p>

<p>英语世界里，文档非常受重视，许多公司和组织都有自己的文档规范，清楚地规定写作要求，比如也有不少，但都不令人满意，要么太简单，要么不太适用。</p>

<p>我就动手，参考上面的规范，也结合自己的实践，总结了一份简单的。</p>

<blockquote>
  <ol start='1'>
<li></li>
<li></li>
<li></li>
<li></li>
<li></li>
<li></li>
</ol>
</blockquote>

<p>我希望，这样可以抛砖引玉，让更多人重视文档，进而真正出现大家普遍接受的文档规范。</p>

<p>下面是关于写作风格的一个片段。欢迎提交  补充。</p>

<p>=================================</p>

<h2>写作风格</h2>

<p>（摘自）</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2016/bg2016101802.jpg" alt="" title="" /></p>

<p>如果使用了被动语态，应考虑更改为主动语态。</p>

<blockquote><pre><code class="language-markup">
错误：假如此软件尚未被安装，

正确：假如尚未安装这个软件，
</code></pre></blockquote>

<p>不使用非正式的语言风格。</p>

<blockquote><pre><code class="language-markup">
错误：Lady Gaga 的演唱会真是酷毙了，从没看过这么给力的表演！！！

正确：无法参加本次活动，我深感遗憾。
</code></pre></blockquote>

<p>用对"的"、"地"、"得"。</p>

<blockquote><pre><code class="language-markup">
她露出了开心的笑容。
（形容词＋的＋名词）

她开心地笑了。
（副词＋地＋动词）

她笑得很开心。
（动词＋得＋副词）
</code></pre></blockquote>

<p>使用代词时（比如"其"、"该"、"此"、"这"等词），必须明确指代的内容，保证只有一个含义。</p>

<blockquote><pre><code class="language-markup">
错误：从管理系统可以监视中继系统和受其直接控制的分配系统。

正确：从管理系统可以监视两个系统：中继系统和受中继系统直接控制的分配系统。
</code></pre></blockquote>

<p>名词前不要使用过多的形式词。</p>

<blockquote><pre><code class="language-markup">
错误：此设备的使用必须在接受过本公司举办的正式的设备培训的技师的指导下进行。

正确：此设备必须在技师的指导下使用，且指导技师必须接受过由本公司举办的正式设备培训。
</code></pre></blockquote>

<p>句子的长度尽量保持在20个字以内；20～29个字的句子，可以接受；39～39个字的句子，语义必须明确，才能接受；多于40个字的句子，在任何情况下都不能接受。</p>

<blockquote><pre><code class="language-markup">
错误：本产品适用于从由一台服务器进行动作控制的单一节点结构到由多台服务器进行动作控制的并行处理程序结构等多种体系结构。

正确：本产品适用于多种体系结构。无论是由一台服务器（单一节点结构），还是由多台服务器（并行处理结构）进行动作控制，均可以使用本产品。
</code></pre></blockquote>

<p>同样一个意思，尽量使用肯定句表达，不使用否定句表达。</p>

<blockquote><pre><code class="language-markup">
错误：请确认没有接通装置的电源。

正确：请确认装置的电源已关闭。
</code></pre></blockquote>

<p>避免使用双重否定句。</p>

<blockquote><pre><code class="language-markup">
错误：没有删除权限的用户，不能删除此文件。

正确：用户必须拥有删除权限，才能删除此文件。
</code></pre></blockquote>

<p>（正文完）</p>

<p>====================================</p>

<p>下面是推广时间。不过我想先说一些题外话。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2016/bg2016101504.jpg" alt="" title="" /></p>

<p>如果你经常来这里，可能会注意到，有的文章结尾有市场推广信息。就是这样，我的《财新周刊》专栏写到了 Udacity，他们正好在推广纳米学位，就在那篇文章后面做了一个广告。有的朋友因此指责我写"软文"，这不是事实。</p>

<p>事实是，我的博客上没有一篇是"软文"，尽管一直有人来问价格。所有的文章都是真实想法，都是我真心想分享的东西。每一个来访问的读者，我都当作是朋友，不会把一篇广告伪装成正常的文章，去欺骗朋友。这一直是我做人的信条，不会为了一点点钱，就把这么多年的坚持都抛弃了。</p>

<p>推广活动都放在文章的结尾，明确注明是推广，并且我只接受那些我认可的产品。对我来说，这点收入可以补贴服务器支出；对许多读者来说，有些信息可能非常有用，比如下面这条。</p>

<p>====================================</p>

<p>今天推广的主角是，一个前端开发的在线教育平台。</p>

<p></p>

<p>创始人小河就是培训班出身，通过自身努力进入百度，深知自学者的苦恼：企业不愿意要培训班出来的学生，而学生不知道应该选哪一家培训机构。他创业的时候，立志要做一家靠谱的、有信誉、有口碑的在线教育公司。</p>

<p>"海棠学院"的很多讲师都有百度背景，开发过用户上亿的产品。为了做出最容易学会的课程，他们反复尝试，不惜放弃已经录好的500多个课时，推倒重来。功夫不负有心人，"海棠学院"现在已经取得了很好的成绩。</p>

<blockquote>
  <ul>
<li>两门免费课在腾讯课题排名，已经稳定了两个月。</li>
<li>在等平台也是名列前茅。</li>
<li>区别于别家，他们免费课的评价与报名人数真真实实，没有水分。</li>
</ul>
</blockquote>

<p>更难得的是，"海棠学院"是工程师的创业项目，甚至都没有市场销售人员，完全靠用户的口碑来推广。如果课程质量不好，他们马上就完蛋了。</p>

<p></p>

<p>现在，为了发展更多的用户，也是因为对课程很有信心，他们搞了一个，抛弃 "先付费、再学习" 的模式，让用户零成本体验他们提供高质量培训。</p>

<blockquote>
  <ol start='1'>
<li>只需要缴纳 99 元，即可感受海棠学院一周的课程，与正式学员享受一模一样的待遇（录播+直播+教学监管+技术辅导）。</li>
<li>一周后，如果觉得不满意，99 元可以退款。</li>
<li>如果想继续学下去，已经缴纳的 99 元可以抵扣学费，并且学费还可以再优惠 900 元。也就是说，参加这个活动比起直接报名，可以一共节省 999 元的学费。</li>
<li><strong>我的读者还可以使用独家优惠码"ruanyifeng"，学费再抵扣 300 元。</strong></li>
</ol>
</blockquote>

<p>整个课程一共需要 4.5 个月左右，涉及前端开发的各个方面，目标是通过一次系统的培训，你就能从事前端开发这项工作。遇到不懂的地方，可以重学，他们保证让你学会。</p>

<p>想从事前端开发，却不知道从何学起的朋友，不要错过这个机会。只需99元，就可以感受一下专业级、全方位的培训服务，如果不满意，99元还可以退款。</p>

<p>这个活动10月31日截止，因为当天就开课了，后面就恢复原价了。现在 就点击了解详情吧。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2016/bg2016101503.jpg" alt="" title="" /></p>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2016-10-18T08:19:26+08:00">2016年10月18日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>购买文集：</li>
<li>社交媒体：</li>
<li>Feed订阅： </li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------
<h1 id="#title_1" >2、网络文凭，你要不要</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2016/10/online_education.html](http://www.ruanyifeng.com/blog/2016/10/online_education.html)
<p>（说明：本文原载2016年第35期。）</p>

        <p>1.</p>

<p>我一直相信，互联网教育是未来的方向。美国三个主要的在线教育网站--------我都经常访问。</p>

<p>今年四月，Udacity 进入中国，推出了中文版。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2016/bg2016082906.jpg" alt="" title="" /></p>

<blockquote>
  <p>"纳米学位（Nanodegree）是优达学城此前与 Google、Facebook、亚马逊等互联网公司联合推出的学历认证项目。学员在线学习，所有项目考核合格之后即可获得纳米学位。"</p>
</blockquote>

<p>现在总共有12种纳米学位，包括机器学习、无人驾驶车开发、VR 开发这样非常前沿的领域。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2016/bg2016082903.jpg" alt="" title="" /></p>

<p>官网：</p>

<blockquote>
  <p>"我们没有严格意义上的录取流程，对报名者唯一的要求是学习该纳米学位项目所必须的先修知识和技能。纳米学位项目采取自主学习模式，你可以按照你喜欢的速度完成项目。12个月内完成纳米学习，可以得到50%学费返回。"</p>
</blockquote>

<p>该公司宣称，国内的许多互联网公司（比如滴滴出行、优酷土豆、京东、新浪）已经认可了纳米学位。我忍不住想，会不会以后找工作，大家手里拿的不是大学文凭，而是网站颁发的文凭？<strong>如果雇主认可网络文凭，我们是否还需要大学文凭？</strong></p>

<p>下面是我的一些思考。另外，我与优达学城的工程师有过一些个人交流，他们最近正好在搞活动，我想做一下推广，文章的结尾处有详细信息。</p>

<p>2.</p>

<p>当代的大学起源于欧洲修道院的。学生要经过多年的苦修，经过考核，才能毕业。如果想成为高级僧侣，就必须再多熬几年。另外，还有导师作为监督人，防止你学到歪门邪说。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2016/bg2016082907.jpg" alt="" title="" /></p>

<p>这种模式的两大弊端，演变到今天，已经越来越严重了：一个是传授的知识老化，另一个是极其浪费学生的时间。</p>

<p>3.</p>

<p>什么知识才是有用的知识？</p>

<p>农业社会，上一代人的知识可以一成不变地用在下一代。而在信息社会，前几年的知识，再过几年就不能用了。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2016/bg2016082908.jpg" alt="" title="" /></p>

<p>举例来说，眼下就业前景最好的行业，我觉得有两个：区块链和VR。它们在五年前都是不存在的，那时就业最好的是苹果iOS系统的应用开发，可是再往前推五年，它也是不存在的。伴随着它们的是，很多旧工作岗位的消失，比如塞班、黑莓、Windows Phone的开发。</p>

<p>这种情况下，大学应该教什么，我们根本不知道。<strong>学生毕业后的行业，现在根本还没有出现。因此，大学只能重点教基础类课程，但这样就会学到大量没用的东西。</strong>学生感叹，考试一结束，许多课程这辈子再没有用到的机会了。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2016/bg2016082909.jpg" alt="" title="" /></p>

<p>更糟糕的是，学生的培养计划，都是一些二三十年前毕业、然后一直待在大学里、与社会生产实践脱节的人制定的。他们的知识和思维早已过时了。这样的人指定你应该学习的知识，很可能在你学的时候就已经没用了。</p>

<p>4.</p>

<p>退一步说，就算你在大学里能学到真正的知识，也不应该在那里待四年。如果只学最需要学习的东西，一年就够了。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2016/bg2016082911.jpg" alt="" title="" /></p>

<p>四年时间足以让一个人在任何领域成为资深业者，甚至专家。可是我们的大学生呢，经过本科四年，不要说领域专家，甚至能力强的学生都寥寥无几。我们的大学制度用了四年时间，培养出了大量一无所长的、迷茫困惑的、市场滞销的年轻人。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2016/bg2016082910.jpg" alt="" title="" /></p>

<p>18岁是人生最有热情和精力投入一项事业的时候，但是，<strong>大学将你一连四年关在教室和图书馆里，把考试和绩点伪装成你奋斗的目标，人为将你与真实世界隔离，引导你去关注那些对未来人生毫不重要的事情。</strong>经过这样四年的歧途，等你真正走上社会、要跟全世界竞争的时候，你的竞争力不是变强了，而是变弱了。换句话说，四年制大学很可能是削弱你，而不是让你变得更强。</p>

<p>强烈推荐阅读，2014年诺贝尔物理学奖得主中村修二的观点。</p>

<p>世界著名程序员Jamie Zawinski曾经解释，为什么他只读了一个学期的大学就退学。</p>

<blockquote>
  <p>"进了大学以后，每天8点就要起床，开始训练记忆力。有一门课我早就会了，想申请免修。教务长说不行，你必须上，这是政策。见鬼，我为什么要自己付钱，来这种地方。我就退学了，从来没后悔过。"</p>
</blockquote>

<p>我们时代的很多成功者----乔布斯、比尔盖茨、扎克伯格等等----都是退学生，这绝不是偶然的。不是他们在大学待不下去，而是他们发现，没必要在那个地方待四年。如果他们咬着牙忍受下去，熬到拿到文凭的那一天，苹果公司和微软公司可能都不会有了。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2016/bg2016082912.jpg" alt="" title="" /></p>

<p>读大学，只是18岁时很多种选择中的一种，不是唯一的选择，更谈不上是最好的选择。校园是一个美丽的地方，但是如果一定要在里面待上四年，那还是算了吧。</p>

<p>5.</p>

<p>以前，人生的选择很少，你不得不去读大学，因为没有其他地方可以接受高等教育。社会还把很多机会与文凭挂钩，先有文凭，然后才能有就业、职称、住房等等。</p>

<p>但是，时代已经变了，文凭正变得越来越不重要。那些与文凭挂钩的东西，正在一项项脱钩。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2016/bg2016082913.jpg" alt="" title="" /></p>

<p>互联网将教育的自主权，交到了每个人自己手里。上什么课程、什么时间上，都完全由你决定。你可以一边工作，一边利用夜晚和周末，学习网络课程。这样的话，不仅早早就会有收入，而且只学那些对自己最有用、最感兴趣的内容，学习的效率很高。如果发现对学术有兴趣，将来再回大学，攻读更高的学位，也是完全可以的。</p>

<p>等到22岁，别人刚刚开始找工作，还在为归还学贷发愁，你已经有了四年工作经验和一些积蓄，认清了自己的人生道路，开始向事业的高峰冲刺了。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2016/bg2016082914.jpg" alt="" title="" /></p>

<p>（正文完）</p>

<hr />

<p>下面是推广时间。</p>

<p>首先，感谢优达学城为我的读者准备了优惠码。你可以先去看一下他们的，那么多的来自硅谷的优质学习资源，等待你去探索。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2016/bg2016082915.jpg" alt="" title="" /></p>

<p>大部分是免费课程，不花一分钱，就能学到最新的技术。<strong>收费课程则会对学习者提供纳米学位和非常细致的辅导，可以大大加速学习。</strong>这些课程都由一段段小视频组成，随时随地花上五分钟，就可以开始学习。</p>

<p>我个人推荐课程，因为这是他们的强项，最受好评。所有收费课程可以免费体验7天，如果觉得喜欢，<strong>缴费的时候用"ruanyf "这个优惠码，就可以优惠300元。</strong></p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2016/bg2016082904.png" alt="" title="" /></p>

<p>另外，优达学城正在举办"程序员感谢月"，整个十月份都有活动，目的是让更多的人去关注程序员、工程师对社会的贡献。只要你通过一个小 Quiz，证明自己真的是程序员，就有机会拿到各种福利，比如上门按摩券、亚马逊AWS代金券、GrowingIO代金券、与大公司CTO共进午餐的机会等等，详情看。</p>

<p>还犹豫什么，现在就开始吧！</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2016/bg2016082916.jpg" alt="" title="" /></p>

<p>微信号：youdaxue</p>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2016-10-12T07:56:39+08:00">2016年10月12日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>购买文集：</li>
<li>社交媒体：</li>
<li>Feed订阅： </li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------
<h1 id="#title_2" >3、npm scripts 使用指南</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2016/10/npm_scripts.html](http://www.ruanyifeng.com/blog/2016/10/npm_scripts.html)
<p>Node 开发离不开 npm，而脚本功能是 npm 最强大、最常用的功能之一。</p>

        <p>本文介绍如何使用 npm 脚本（npm scripts）。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2016/bg2016101101.jpg" alt="" title="" /></p>

<h2>一、什么是 npm 脚本？</h2>

<p>npm 允许在<code>package.json</code>文件里面，使用<code>scripts</code>字段定义脚本命令。</p>

<blockquote><pre><code class="language-javascript">
{
  // ...
  "scripts": {
    "build": "node build.js"
  }
}
</code></pre></blockquote>

<p>上面代码是<code>package.json</code>文件的一个片段，里面的<code>scripts</code>字段是一个对象。它的每一个属性，对应一段脚本。比如，<code>build</code>命令对应的脚本是<code>node build.js</code>。</p>

<p>命令行下使用<code>npm run</code>命令，就可以执行这段脚本。</p>

<blockquote><pre><code class="language-bash">
$ npm run build
# 等同于执行
$ node build.js
</code></pre></blockquote>

<p>这些定义在<code>package.json</code>里面的脚本，就称为 npm 脚本。它的优点很多。</p>

<blockquote>
  <ul>
<li>项目的相关脚本，可以集中在一个地方。</li>
<li>不同项目的脚本命令，只要功能相同，就可以有同样的对外接口。用户不需要知道怎么测试你的项目，只要运行<code>npm run test</code>即可。</li>
<li>可以利用 npm 提供的很多辅助功能。</li>
</ul>
</blockquote>

<p>查看当前项目的所有 npm 脚本命令，可以使用不带任何参数的<code>npm run</code>命令。</p>

<blockquote><pre><code class="language-bash">
$ npm run
</code></pre></blockquote>

<h2>二、原理</h2>

<p>npm 脚本的原理非常简单。每当执行<code>npm run</code>，就会自动新建一个 Shell，在这个 Shell 里面执行指定的脚本命令。因此，只要是 Shell（一般是 Bash）可以运行的命令，就可以写在 npm 脚本里面。</p>

<p>比较特别的是，<code>npm run</code>新建的这个 Shell，会将当前目录的<code>node_modules/.bin</code>子目录加入<code>PATH</code>变量，执行结束后，再将<code>PATH</code>变量恢复原样。</p>

<p>这意味着，当前目录的<code>node_modules/.bin</code>子目录里面的所有脚本，都可以直接用脚本名调用，而不必加上路径。比如，当前项目的依赖里面有 Mocha，只要直接写<code>mocha test</code>就可以了。</p>

<blockquote><pre><code class="language-javascript">
"test": "mocha test"
</code></pre></blockquote>

<p>而不用写成下面这样。</p>

<blockquote><pre><code class="language-javascript">
"test": "./node_modules/.bin/mocha test"
</code></pre></blockquote>

<p>由于 npm 脚本的唯一要求就是可以在 Shell 执行，因此它不一定是 Node 脚本，任何可执行文件都可以写在里面。</p>

<p>npm 脚本的退出码，也遵守 Shell 脚本规则。如果退出码不是<code>0</code>，npm 就认为这个脚本执行失败。</p>

<h2>三、通配符</h2>

<p>由于 npm 脚本就是 Shell 脚本，因为可以使用 Shell 通配符。</p>

<blockquote><pre><code class="language-javascript">
"lint": "jshint *.js"
"lint": "jshint **/*.js"
</code></pre></blockquote>

<p>上面代码中，<code>*</code>表示任意文件名，<code>**</code>表示任意一层子目录。</p>

<p>如果要将通配符传入原始命令，防止被 Shell 转义，要将星号转义。</p>

<blockquote><pre><code class="language-javascript">
"test": "tap test/\*.js"
</code></pre></blockquote>

<h2>四、传参</h2>

<p>向 npm 脚本传入参数，要使用<code>--</code>标明。</p>

<blockquote><pre><code class="language-javascript">
"lint": "jshint **.js"
</code></pre></blockquote>

<p>向上面的<code>npm run lint</code>命令传入参数，必须写成下面这样。</p>

<blockquote><pre><code class="language-bash">
$ npm run lint --  --reporter checkstyle > checkstyle.xml
</code></pre></blockquote>

<p>也可以在<code>package.json</code>里面再封装一个命令。</p>

<blockquote><pre><code class="language-javascript">
"lint": "jshint **.js",
"lint:checkstyle": "npm run lint -- --reporter checkstyle > checkstyle.xml"
</code></pre></blockquote>

<h2>五、执行顺序</h2>

<p>如果 npm 脚本里面需要执行多个任务，那么需要明确它们的执行顺序。</p>

<p>如果是并行执行（即同时的平行执行），可以使用<code>&amp;</code>符号。</p>

<blockquote><pre><code class="language-bash">
$ npm run script1.js & npm run script2.js
</code></pre></blockquote>

<p>如果是继发执行（即只有前一个任务成功，才执行下一个任务），可以使用<code>&amp;&amp;</code>符号。</p>

<blockquote><pre><code class="language-bash">
$ npm run script1.js && npm run script2.js
</code></pre></blockquote>

<p>这两个符号是 Bash 的功能。此外，还可以使用 node 的任务管理模块：。</p>

<h2>六、默认值</h2>

<p>一般来说，npm 脚本由用户提供。但是，npm 对两个脚本提供了默认值。也就是说，这两个脚本不用定义，就可以直接使用。</p>

<blockquote><pre><code class="language-javascript">
"start": "node server.js"，
"install": "node-gyp rebuild"
</code></pre></blockquote>

<p>上面代码中，<code>npm run start</code>的默认值是<code>node server.js</code>，前提是项目根目录下有<code>server.js</code>这个脚本；<code>npm run install</code>的默认值是<code>node-gyp rebuild</code>，前提是项目根目录下有<code>binding.gyp</code>文件。</p>

<h2>七、钩子</h2>

<p>npm 脚本有<code>pre</code>和<code>post</code>两个钩子。举例来说，<code>build</code>脚本命令的钩子就是<code>prebuild</code>和<code>postbuild</code>。</p>

<blockquote><pre><code class="language-javascript">
"prebuild": "echo I run before the build script",
"build": "cross-env NODE_ENV=production webpack",
"postbuild": "echo I run after the build script"
</code></pre></blockquote>

<p>用户执行<code>npm run build</code>的时候，会自动按照下面的顺序执行。</p>

<blockquote><pre><code class="language-bash">
npm run prebuild && npm run build && npm run postbuild
</code></pre></blockquote>

<p>因此，可以在这两个钩子里面，完成一些准备工作和清理工作。下面是一个例子。</p>

<blockquote><pre><code class="language-javascript">
"clean": "rimraf ./dist && mkdir dist",
"prebuild": "npm run clean",
"build": "cross-env NODE_ENV=production webpack"
</code></pre></blockquote>

<p>npm 默认提供下面这些钩子。</p>

<blockquote>
  <ul>
<li>prepublish，postpublish</li>
<li>preinstall，postinstall</li>
<li>preuninstall，postuninstall</li>
<li>preversion，postversion</li>
<li>pretest，posttest</li>
<li>prestop，poststop</li>
<li>prestart，poststart</li>
<li>prerestart，postrestart</li>
</ul>
</blockquote>

<p>自定义的脚本命令也可以加上<code>pre</code>和<code>post</code>钩子。比如，<code>myscript</code>这个脚本命令，也有<code>premyscript</code>和<code>postmyscript</code>钩子。不过，双重的<code>pre</code>和<code>post</code>无效，比如<code>prepretest</code>和<code>postposttest</code>是无效的。</p>

<p>npm 提供一个<code>npm_lifecycle_event</code>变量，返回当前正在运行的脚本名称，比如<code>pretest</code>、<code>test</code>、<code>posttest</code>等等。所以，可以利用这个变量，在同一个脚本文件里面，为不同的<code>npm scripts</code>命令编写代码。请看下面的例子。</p>

<blockquote><pre><code class="language-javascript">
const TARGET = process.env.npm_lifecycle_event;

if (TARGET === 'test') {
  console.log(`Running the test task!`);
}

if (TARGET === 'pretest') {
  console.log(`Running the pretest task!`);
}

if (TARGET === 'posttest') {
  console.log(`Running the posttest task!`);
}
</code></pre></blockquote>

<p>注意，<code>prepublish</code>这个钩子不仅会在<code>npm publish</code>命令之前运行，还会在<code>npm install</code>（不带任何参数）命令之前运行。这种行为很容易让用户感到困惑，所以 npm 4 引入了一个新的钩子<code>prepare</code>，行为等同于<code>prepublish</code>，而从 npm 5 开始，<code>prepublish</code>将只在<code>npm publish</code>命令之前运行。</p>

<h2>八、简写形式</h2>

<p>四个常用的 npm 脚本有简写形式。</p>

<blockquote>
  <ul>
<li><code>npm start</code>是<code>npm run start</code></li>
<li><code>npm stop</code>是<code>npm run stop</code>的简写</li>
<li><code>npm test</code>是<code>npm run test</code>的简写</li>
<li><code>npm restart</code>是<code>npm run stop &amp;&amp; npm run restart &amp;&amp; npm run start</code>的简写</li>
</ul>
</blockquote>

<p><code>npm start</code>、<code>npm stop</code>和<code>npm restart</code>都比较好理解，而<code>npm restart</code>是一个复合命令，实际上会执行三个脚本命令：<code>stop</code>、<code>restart</code>、<code>start</code>。具体的执行顺序如下。</p>

<blockquote>
  <ol start='1'>
<li>prerestart</li>
<li>prestop</li>
<li>stop</li>
<li>poststop</li>
<li>restart</li>
<li>prestart</li>
<li>start</li>
<li>poststart</li>
<li>postrestart </li>
</ol>
</blockquote>

<h2>九、变量</h2>

<p>npm 脚本有一个非常强大的功能，就是可以使用 npm 的内部变量。</p>

<p>首先，通过<code>npm_package_</code>前缀，npm 脚本可以拿到<code>package.json</code>里面的字段。比如，下面是一个<code>package.json</code>。</p>

<blockquote><pre><code class="language-javascript">
{
  "name": "foo", 
  "version": "1.2.5",
  "scripts": {
    "view": "node view.js"
  }
}
</code></pre></blockquote>

<p>那么，变量<code>npm_package_name</code>返回<code>foo</code>，变量<code>npm_package_version</code>返回<code>1.2.5</code>。</p>

<blockquote><pre><code class="language-javascript">
// view.js
console.log(process.env.npm_package_name); // foo
console.log(process.env.npm_package_version); // 1.2.5
</code></pre></blockquote>

<p>上面代码中，我们通过环境变量<code>process.env</code>对象，拿到<code>package.json</code>的字段值。如果是 Bash 脚本，可以用<code>$npm_package_name</code>和<code>$npm_package_version</code>取到这两个值。</p>

<p><code>npm_package_</code>前缀也支持嵌套的<code>package.json</code>字段。</p>

<blockquote><pre><code class="language-javascript">
  "repository": {
    "type": "git",
    "url": "xxx"
  },
  scripts: {
    "view": "echo $npm_package_repository_type"
  }
</code></pre></blockquote>

<p>上面代码中，<code>repository</code>字段的<code>type</code>属性，可以通过<code>npm_package_repository_type</code>取到。</p>

<p>下面是另外一个例子。</p>

<blockquote><pre><code class="language-javascript">
"scripts": {
  "install": "foo.js"
}
</code></pre></blockquote>

<p>上面代码中，<code>npm_package_scripts_install</code>变量的值等于<code>foo.js</code>。</p>

<p>然后，npm 脚本还可以通过<code>npm_config_</code>前缀，拿到 npm 的配置变量，即<code>npm config get xxx</code>命令返回的值。比如，当前模块的发行标签，可以通过<code>npm_config_tag</code>取到。</p>

<blockquote><pre><code class="language-javascript">
"view": "echo $npm_config_tag",
</code></pre></blockquote>

<p>注意，<code>package.json</code>里面的<code>config</code>对象，可以被环境变量覆盖。</p>

<blockquote><pre><code class="language-javascript">
{ 
  "name" : "foo",
  "config" : { "port" : "8080" },
  "scripts" : { "start" : "node server.js" }
}
</code></pre></blockquote>

<p>上面代码中，<code>npm_package_config_port</code>变量返回的是<code>8080</code>。这个值可以用下面的方法覆盖。</p>

<blockquote><pre><code class="language-bash">
$ npm config set foo:port 80
</code></pre></blockquote>

<p>最后，<code>env</code>命令可以列出所有环境变量。</p>

<blockquote><pre><code class="language-javascript">
"env": "env"
</code></pre></blockquote>

<h2>十、常用脚本示例</h2>

<blockquote><pre><code class="language-javascript">
// 删除目录
"clean": "rimraf dist/*",

// 本地搭建一个 HTTP 服务
"serve": "http-server -p 9090 dist/",

// 打开浏览器
"open:dev": "opener http://localhost:9090",

// 实时刷新
 "livereload": "live-reload --port 9091 dist/",

// 构建 HTML 文件
"build:html": "jade index.jade > dist/index.html",

// 只要 CSS 文件有变动，就重新执行构建
"watch:css": "watch 'npm run build:css' assets/styles/",

// 只要 HTML 文件有变动，就重新执行构建
"watch:html": "watch 'npm run build:html' assets/html",

// 部署到 Amazon S3
"deploy:prod": "s3-cli sync ./dist/ s3://example-com/prod-site/",

// 构建 favicon
"build:favicon": "node scripts/favicon.js",
</code></pre></blockquote>

<h2>十一、参考链接</h2>

<ul>
<li>, by Keith Cirkel</li>
<li>, by Ryan Zimmerman</li>
</ul>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2016-10-11T19:03:27+08:00">2016年10月11日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>购买文集：</li>
<li>社交媒体：</li>
<li>Feed订阅： </li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------
<h1 id="#title_3" >4、React 技术栈系列教程</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2016/09/react-technology-stack.html](http://www.ruanyifeng.com/blog/2016/09/react-technology-stack.html)
<p>上周中秋节，我待在家里，写完了  教程。</p>

        <p>至此，《React 技术栈系列教程》算是比较完整了。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2016/bg2016092301.png" alt="" title="" /></p>

<blockquote>
  <ul>
<li>ES6 语法：</li>
<li>Babel：</li>
<li>React：</li>
<li>Webpack：</li>
<li>React 项目脚手架：</li>
<li>Flex 布局：</li>
<li>CSS Modules：</li>
<li>React-Router：</li>
<li>Flux 架构：</li>
<li>Redux 架构：</li>
<li>Mocha 测试框架：</li>
<li>Istanbul 覆盖率框架：</li>
<li>React 单元测试：</li>
</ul>
</blockquote>

<p>它们都针对初学者，尽量通俗易懂，帮大家节省一些看文档的时间，让你快速上手。其中，也有 2000 颗星了。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2016/bg2016092303.jpg" alt="" title="" /></p>

<p>这两年没停过，一直在学习新东西，学习心得就写成了上面的教程。虽然看上去数量不少，但是下一代的互联网开发技术，我还是只学了很小一部分，像 PostCSS、GraphQL、Electron 这些感兴趣的东西，都没时间搞。</p>

<p>面对技术的高速发展和百花齐放，我有时也感到疲倦烦躁。但是，每当看到它们带来的生产力的飞跃，让你一个人快速搞定前后端的全部开发时，就觉得这终究还是一条正确的道路。</p>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2016-09-23T07:05:12+08:00">2016年9月23日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>购买文集：</li>
<li>社交媒体：</li>
<li>Feed订阅： </li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------
<h1 id="#title_4" >5、Redux 入门教程（三）：React-Redux 的用法</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2016/09/redux_tutorial_part_three_react-redux.html](http://www.ruanyifeng.com/blog/2016/09/redux_tutorial_part_three_react-redux.html)
<p>前两篇教程介绍了 Redux 的，今天是最后一部分，介绍如何在 React 项目中使用 Redux。</p>

        <p>为了方便使用，Redux 的作者封装了一个 React 专用的库 ，本文主要介绍它。</p>

<p>这个库是可以选用的。实际项目中，你应该权衡一下，是直接使用 Redux，还是使用 React-Redux。后者虽然提供了便利，但是需要掌握额外的 API，并且要遵守它的组件拆分规范。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2016/bg2016092101.jpg" alt="" title="" /></p>

<h2>一、UI 组件</h2>

<p>React-Redux 将所有组件分成两大类：UI 组件（presentational component）和容器组件（container component）。</p>

<p>UI 组件有以下几个特征。</p>

<blockquote>
  <ul>
<li>只负责 UI 的呈现，不带有任何业务逻辑</li>
<li>没有状态（即不使用<code>this.state</code>这个变量）</li>
<li>所有数据都由参数（<code>this.props</code>）提供</li>
<li>不使用任何 Redux 的 API</li>
</ul>
</blockquote>

<p>下面就是一个 UI 组件的例子。</p>

<blockquote><pre><code class="language-javascript">
const Title =
  value => &lt;h1>{value}&lt;/h1>;
</code></pre></blockquote>

<p>因为不含有状态，UI 组件又称为"纯组件"，即它纯函数一样，纯粹由参数决定它的值。</p>

<h2>二、容器组件</h2>

<p>容器组件的特征恰恰相反。</p>

<blockquote>
  <ul>
<li>负责管理数据和业务逻辑，不负责 UI 的呈现</li>
<li>带有内部状态</li>
<li>使用 Redux 的 API</li>
</ul>
</blockquote>

<p>总之，只要记住一句话就可以了：UI 组件负责 UI 的呈现，容器组件负责管理数据和逻辑。</p>

<p>你可能会问，如果一个组件既有 UI 又有业务逻辑，那怎么办？回答是，将它拆分成下面的结构：外面是一个容器组件，里面包了一个UI 组件。前者负责与外部的通信，将数据传给后者，由后者渲染出视图。</p>

<p>React-Redux 规定，所有的 UI 组件都由用户提供，容器组件则是由 React-Redux 自动生成。也就是说，用户负责视觉层，状态管理则是全部交给它。</p>

<h2>三、connect()</h2>

<p>React-Redux 提供<code>connect</code>方法，用于从 UI 组件生成容器组件。<code>connect</code>的意思，就是将这两种组件连起来。</p>

<blockquote><pre><code class="language-javascript">
import { connect } from 'react-redux'
const VisibleTodoList = connect()(TodoList);
</code></pre></blockquote>

<p>上面代码中，<code>TodoList</code>是 UI 组件，<code>VisibleTodoList</code>就是由 React-Redux 通过<code>connect</code>方法自动生成的容器组件。</p>

<p>但是，因为没有定义业务逻辑，上面这个容器组件毫无意义，只是 UI 组件的一个单纯的包装层。为了定义业务逻辑，需要给出下面两方面的信息。</p>

<blockquote>
  <p>（1）输入逻辑：外部的数据（即<code>state</code>对象）如何转换为 UI 组件的参数</p>

<p>（2）输出逻辑：用户发出的动作如何变为 Action 对象，从 UI 组件传出去。</p>
</blockquote>

<p>因此，<code>connect</code>方法的完整 API 如下。</p>

<blockquote><pre><code class="language-javascript">
import { connect } from 'react-redux'

const VisibleTodoList = connect(
  mapStateToProps,
  mapDispatchToProps
)(TodoList)
</code></pre></blockquote>

<p>上面代码中，<code>connect</code>方法接受两个参数：<code>mapStateToProps</code>和<code>mapDispatchToProps</code>。它们定义了 UI 组件的业务逻辑。前者负责输入逻辑，即将<code>state</code>映射到 UI 组件的参数（<code>props</code>），后者负责输出逻辑，即将用户对 UI 组件的操作映射成 Action。</p>

<h3>四、mapStateToProps()</h3>

<p><code>mapStateToProps</code>是一个函数。它的作用就是像它的名字那样，建立一个从（外部的）<code>state</code>对象到（UI 组件的）<code>props</code>对象的映射关系。</p>

<p>作为函数，<code>mapStateToProps</code>执行后应该返回一个对象，里面的每一个键值对就是一个映射。请看下面的例子。</p>

<blockquote><pre><code class="language-javascript">
const mapStateToProps = (state) => {
  return {
    todos: getVisibleTodos(state.todos, state.visibilityFilter)
  }
}
</code></pre></blockquote>

<p>上面代码中，<code>mapStateToProps</code>是一个函数，它接受<code>state</code>作为参数，返回一个对象。这个对象有一个<code>todos</code>属性，代表 UI 组件的同名参数，后面的<code>getVisibleTodos</code>也是一个函数，可以从<code>state</code>算出 <code>todos</code> 的值。</p>

<p>下面就是<code>getVisibleTodos</code>的一个例子，用来算出<code>todos</code>。</p>

<blockquote><pre><code class="language-javascript">
const getVisibleTodos = (todos, filter) => {
  switch (filter) {
    case 'SHOW_ALL':
      return todos
    case 'SHOW_COMPLETED':
      return todos.filter(t => t.completed)
    case 'SHOW_ACTIVE':
      return todos.filter(t => !t.completed)
    default:
      throw new Error('Unknown filter: ' + filter)
  }
}
</code></pre></blockquote>

<p><code>mapStateToProps</code>会订阅 Store，每当<code>state</code>更新的时候，就会自动执行，重新计算 UI 组件的参数，从而触发 UI 组件的重新渲染。</p>

<p><code>mapStateToProps</code>的第一个参数总是<code>state</code>对象，还可以使用第二个参数，代表容器组件的<code>props</code>对象。</p>

<blockquote><pre><code class="language-javascript">
// 容器组件的代码
//    &lt;FilterLink filter="SHOW_ALL">
//      All
//    &lt;/FilterLink>

const mapStateToProps = (state, ownProps) => {
  return {
    active: ownProps.filter === state.visibilityFilter
  }
}
</code></pre></blockquote>

<p>使用<code>ownProps</code>作为参数后，如果容器组件的参数发生变化，也会引发 UI 组件重新渲染。</p>

<p><code>connect</code>方法可以省略<code>mapStateToProps</code>参数，那样的话，UI 组件就不会订阅Store，就是说 Store 的更新不会引起 UI 组件的更新。</p>

<h2>五、mapDispatchToProps()</h2>

<p><code>mapDispatchToProps</code>是<code>connect</code>函数的第二个参数，用来建立 UI 组件的参数到<code>store.dispatch</code>方法的映射。也就是说，它定义了哪些用户的操作应该当作 Action，传给 Store。它可以是一个函数，也可以是一个对象。</p>

<p>如果<code>mapDispatchToProps</code>是一个函数，会得到<code>dispatch</code>和<code>ownProps</code>（容器组件的<code>props</code>对象）两个参数。</p>

<blockquote><pre><code class="language-javascript">
const mapDispatchToProps = (
  dispatch,
  ownProps
) => {
  return {
    onClick: () => {
      dispatch({
        type: 'SET_VISIBILITY_FILTER',
        filter: ownProps.filter
      });
    }
  };
}
</code></pre></blockquote>

<p>从上面代码可以看到，<code>mapDispatchToProps</code>作为函数，应该返回一个对象，该对象的每个键值对都是一个映射，定义了 UI 组件的参数怎样发出 Action。</p>

<p>如果<code>mapDispatchToProps</code>是一个对象，它的每个键名也是对应 UI 组件的同名参数，键值应该是一个函数，会被当作 Action creator ，返回的 Action 会由 Redux 自动发出。举例来说，上面的<code>mapDispatchToProps</code>写成对象就是下面这样。</p>

<blockquote><pre><code class="language-javascript">
const mapDispatchToProps = {
  onClick: (filter) => {
    type: 'SET_VISIBILITY_FILTER',
    filter: filter
  };
}
</code></pre></blockquote>

<h2>六、&lt;Provider> 组件</h2>

<p><code>connect</code>方法生成容器组件以后，需要让容器组件拿到<code>state</code>对象，才能生成 UI 组件的参数。</p>

<p>一种解决方法是将<code>state</code>对象作为参数，传入容器组件。但是，这样做比较麻烦，尤其是容器组件可能在很深的层级，一级级将<code>state</code>传下去就很麻烦。</p>

<p>React-Redux 提供<code>Provider</code>组件，可以让容器组件拿到<code>state</code>。</p>

<blockquote><pre><code class="language-javascript">
import { Provider } from 'react-redux'
import { createStore } from 'redux'
import todoApp from './reducers'
import App from './components/App'

let store = createStore(todoApp);

render(
  &lt;Provider store={store}>
    &lt;App />
  &lt;/Provider>,
  document.getElementById('root')
)
</code></pre></blockquote>

<p>上面代码中，<code>Provider</code>在根组件外面包了一层，这样一来，<code>App</code>的所有子组件就默认都可以拿到<code>state</code>了。</p>

<p>它的原理是<code>React</code>组件的属性，请看源码。</p>

<blockquote><pre><code class="language-javascript">
class Provider extends Component {
  getChildContext() {
    return {
      store: this.props.store
    };
  }
  render() {
    return this.props.children;
  }
}

Provider.childContextTypes = {
  store: React.PropTypes.object
}
</code></pre></blockquote>

<p>上面代码中，<code>store</code>放在了上下文对象<code>context</code>上面。然后，子组件就可以从<code>context</code>拿到<code>store</code>，代码大致如下。</p>

<blockquote><pre><code class="language-javascript">
class VisibleTodoList extends Component {
  componentDidMount() {
    const { store } = this.context;
    this.unsubscribe = store.subscribe(() =>
      this.forceUpdate()
    );
  }

  render() {
    const props = this.props;
    const { store } = this.context;
    const state = store.getState();
    // ...
  }
}

VisibleTodoList.contextTypes = {
  store: React.PropTypes.object
}
</code></pre></blockquote>

<p><code>React-Redux</code>自动生成的容器组件的代码，就类似上面这样，从而拿到<code>store</code>。</p>

<h2>七、实例：计数器</h2>

<p>我们来看一个实例。下面是一个计数器组件，它是一个纯的 UI 组件。</p>

<blockquote><pre><code class="language-javascript">
class Counter extends Component {
  render() {
    const { value, onIncreaseClick } = this.props
    return (
      &lt;div>
        &lt;span>{value}&lt;/span>
        &lt;button onClick={onIncreaseClick}>Increase&lt;/button>
      &lt;/div>
    )
  }
}
</code></pre></blockquote>

<p>上面代码中，这个 UI 组件有两个参数：<code>value</code>和<code>onIncreaseClick</code>。前者需要从<code>state</code>计算得到，后者需要向外发出 Action。</p>

<p>接着，定义<code>value</code>到<code>state</code>的映射，以及<code>onIncreaseClick</code>到<code>dispatch</code>的映射。</p>

<blockquote><pre><code class="language-javascript">
function mapStateToProps(state) {
  return {
    value: state.count
  }
}

function mapDispatchToProps(dispatch) {
  return {
    onIncreaseClick: () => dispatch(increaseAction)
  }
}

// Action Creator
const increaseAction = { type: 'increase' }
</code></pre></blockquote>

<p>然后，使用<code>connect</code>方法生成容器组件。</p>

<blockquote><pre><code class="language-javascript">
const App = connect(
  mapStateToProps,
  mapDispatchToProps
)(Counter)
</code></pre></blockquote>

<p>然后，定义这个组件的 Reducer。</p>

<blockquote><pre><code class="language-javascript">
// Reducer
function counter(state = { count: 0 }, action) {
  const count = state.count
  switch (action.type) {
    case 'increase':
      return { count: count + 1 }
    default:
      return state
  }
}
</code></pre></blockquote>

<p>最后，生成<code>store</code>对象，并使用<code>Provider</code>在根组件外面包一层。</p>

<blockquote><pre><code class="language-javascript">
import { loadState, saveState } from './localStorage';

const persistedState = loadState();
const store = createStore(
  todoApp,
  persistedState
);

store.subscribe(throttle(() => {
  saveState({
    todos: store.getState().todos,
  })
}, 1000))

ReactDOM.render(
  &lt;Provider store={store}>
    &lt;App />
  &lt;/Provider>,
  document.getElementById('root')
);
</code></pre></blockquote>

<p>完整的代码看。</p>

<h2>八、React-Router 路由库</h2>

<p>使用<code>React-Router</code>的项目，与其他项目没有不同之处，也是使用<code>Provider</code>在<code>Router</code>外面包一层，毕竟<code>Provider</code>的唯一功能就是传入<code>store</code>对象。</p>

<blockquote><pre><code class="language-javascript">
const Root = ({ store }) => (
  &lt;Provider store={store}>
    &lt;Router>
      &lt;Route path="/" component={App} />
    &lt;/Router>
  &lt;/Provider>
);
</code></pre></blockquote>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2016-09-21T21:11:25+08:00">2016年9月21日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>购买文集：</li>
<li>社交媒体：</li>
<li>Feed订阅： </li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------
<h1 id="#title_5" >6、Redux 入门教程（二）：中间件与异步操作</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2016/09/redux_tutorial_part_two_async_operations.html](http://www.ruanyifeng.com/blog/2016/09/redux_tutorial_part_two_async_operations.html)
<p>，我介绍了 Redux 的基本做法：用户发出 Action，Reducer 函数算出新的 State，View 重新渲染。</p>

        <p><img src="http://www.ruanyifeng.com/blogimg/asset/2016/bg2016092001.jpg" alt="" title="" /></p>

<p>但是，一个关键问题没有解决：异步操作怎么办？Action 发出以后，Reducer 立即算出 State，这叫做同步；Action 发出以后，过一段时间再执行 Reducer，这就是异步。</p>

<p>怎么才能 Reducer 在异步操作结束后自动执行呢？这就要用到新的工具：中间件（middleware）。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2016/bg2016092002.jpg" alt="" title="" /></p>

<h2>一、中间件的概念</h2>

<p>为了理解中间件，让我们站在框架作者的角度思考问题：如果要添加功能，你会在哪个环节添加？</p>

<blockquote>
  <p>（1）Reducer：纯函数，只承担计算 State 的功能，不合适承担其他功能，也承担不了，因为理论上，纯函数不能进行读写操作。</p>

<p>（2）View：与 State 一一对应，可以看作 State 的视觉层，也不合适承担其他功能。</p>

<p>（3）Action：存放数据的对象，即消息的载体，只能被别人操作，自己不能进行任何操作。</p>
</blockquote>

<p>想来想去，只有发送 Action 的这个步骤，即<code>store.dispatch()</code>方法，可以添加功能。举例来说，要添加日志功能，把 Action 和 State 打印出来，可以对<code>store.dispatch</code>进行如下改造。</p>

<blockquote><pre><code class="language-javascript">
let next = store.dispatch;
store.dispatch = function dispatchAndLog(action) {
  console.log('dispatching', action);
  next(action);
  console.log('next state', store.getState());
}
</code></pre></blockquote>

<p>上面代码中，对<code>store.dispatch</code>进行了重定义，在发送 Action 前后添加了打印功能。这就是中间件的雏形。</p>

<p>中间件就是一个函数，对<code>store.dispatch</code>方法进行了改造，在发出 Action 和执行 Reducer 这两步之间，添加了其他功能。</p>

<h2>二、中间件的用法</h2>

<p>本教程不涉及如何编写中间件，因为常用的中间件都有现成的，只要引用别人写好的模块即可。比如，上一节的日志中间件，就有现成的模块。这里只介绍怎么使用中间件。</p>

<blockquote><pre><code class="language-javascript">
import { applyMiddleware, createStore } from 'redux';
import createLogger from 'redux-logger';
const logger = createLogger();

const store = createStore(
  reducer,
  applyMiddleware(logger)
);
</code></pre></blockquote>

<p>上面代码中，<code>redux-logger</code>提供一个生成器<code>createLogger</code>，可以生成日志中间件<code>logger</code>。然后，将它放在<code>applyMiddleware</code>方法之中，传入<code>createStore</code>方法，就完成了<code>store.dispatch()</code>的功能增强。</p>

<p>这里有两点需要注意：</p>

<p>（1）<code>createStore</code>方法可以接受整个应用的初始状态作为参数，那样的话，<code>applyMiddleware</code>就是第三个参数了。</p>

<blockquote><pre><code class="language-javascript">
const store = createStore(
  reducer,
  initial_state,
  applyMiddleware(logger)
);
</code></pre></blockquote>

<p>（2）中间件的次序有讲究。</p>

<blockquote><pre><code class="language-javascript">
const store = createStore(
  reducer,
  applyMiddleware(thunk, promise, logger)
);
</code></pre></blockquote>

<p>上面代码中，<code>applyMiddleware</code>方法的三个参数，就是三个中间件。有的中间件有次序要求，使用前要查一下文档。比如，<code>logger</code>就一定要放在最后，否则输出结果会不正确。</p>

<h2>三、applyMiddlewares()</h2>

<p>看到这里，你可能会问，<code>applyMiddlewares</code>这个方法到底是干什么的？</p>

<p>它是 Redux 的原生方法，作用是将所有中间件组成一个数组，依次执行。下面是它的源码。</p>

<blockquote><pre><code class="language-javascript">
export default function applyMiddleware(...middlewares) {
  return (createStore) => (reducer, preloadedState, enhancer) => {
    var store = createStore(reducer, preloadedState, enhancer);
    var dispatch = store.dispatch;
    var chain = [];

    var middlewareAPI = {
      getState: store.getState,
      dispatch: (action) => dispatch(action)
    };
    chain = middlewares.map(middleware => middleware(middlewareAPI));
    dispatch = compose(...chain)(store.dispatch);

    return {...store, dispatch}
  }
}
</code></pre></blockquote>

<p>上面代码中，所有中间件被放进了一个数组<code>chain</code>，然后嵌套执行，最后执行<code>store.dispatch</code>。可以看到，中间件内部（<code>middlewareAPI</code>）可以拿到<code>getState</code>和<code>dispatch</code>这两个方法。</p>

<h2>四、异步操作的基本思路</h2>

<p>理解了中间件以后，就可以处理异步操作了。</p>

<p>同步操作只要发出一种 Action 即可，异步操作的差别是它要发出三种 Action。</p>

<blockquote>
  <ul>
<li>操作发起时的 Action</li>
<li>操作成功时的 Action</li>
<li>操作失败时的 Action</li>
</ul>
</blockquote>

<p>以向服务器取出数据为例，三种 Action 可以有两种不同的写法。</p>

<blockquote><pre><code class="language-javascript">
// 写法一：名称相同，参数不同
{ type: 'FETCH_POSTS' }
{ type: 'FETCH_POSTS', status: 'error', error: 'Oops' }
{ type: 'FETCH_POSTS', status: 'success', response: { ... } }

// 写法二：名称不同
{ type: 'FETCH_POSTS_REQUEST' }
{ type: 'FETCH_POSTS_FAILURE', error: 'Oops' }
{ type: 'FETCH_POSTS_SUCCESS', response: { ... } }
</code></pre></blockquote>

<p>除了 Action 种类不同，异步操作的 State 也要进行改造，反映不同的操作状态。下面是 State 的一个例子。</p>

<blockquote><pre><code class="language-javascript">
let state = {
  // ... 
  isFetching: true,
  didInvalidate: true,
  lastUpdated: 'xxxxxxx'
};
</code></pre></blockquote>

<p>上面代码中，State 的属性<code>isFetching</code>表示是否在抓取数据。<code>didInvalidate</code>表示数据是否过时，<code>lastUpdated</code>表示上一次更新时间。</p>

<p>现在，整个异步操作的思路就很清楚了。</p>

<blockquote>
  <ul>
<li>操作开始时，送出一个 Action，触发 State 更新为"正在操作"状态，View 重新渲染</li>
<li>操作结束后，再送出一个 Action，触发 State 更新为"操作结束"状态，View 再一次重新渲染</li>
</ul>
</blockquote>

<h2>五、redux-thunk 中间件</h2>

<p>异步操作至少要送出两个 Action：用户触发第一个 Action，这个跟同步操作一样，没有问题；如何才能在操作结束时，系统自动送出第二个 Action 呢？</p>

<p>奥妙就在 Action Creator 之中。</p>

<blockquote><pre><code class="language-javascript">
class AsyncApp extends Component {
  componentDidMount() {
    const { dispatch, selectedPost } = this.props
    dispatch(fetchPosts(selectedPost))
  }

// ...
</code></pre></blockquote>

<p>上面代码是一个异步组件的例子。加载成功后（<code>componentDidMount</code>方法），它送出了（<code>dispatch</code>方法）一个 Action，向服务器要求数据 <code>fetchPosts(selectedSubreddit)</code>。这里的<code>fetchPosts</code>就是 Action Creator。</p>

<p>下面就是<code>fetchPosts</code>的代码，关键之处就在里面。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2016/bg2016092003.jpg" alt="" title="" /></p>

<blockquote><pre><code class="language-javascript">
const fetchPosts = postTitle => (dispatch, getState) => {
  dispatch(requestPosts(postTitle));
  return fetch(`/some/API/${postTitle}.json`)
    .then(response => response.json())
    .then(json => dispatch(receivePosts(postTitle, json)));
  };
};

// 使用方法一
store.dispatch(fetchPosts('reactjs'));
// 使用方法二
store.dispatch(fetchPosts('reactjs')).then(() =>
  console.log(store.getState())
);
</code></pre></blockquote>

<p>上面代码中，<code>fetchPosts</code>是一个Action Creator（动作生成器），返回一个函数。这个函数执行后，先发出一个Action（<code>requestPosts(postTitle)</code>），然后进行异步操作。拿到结果后，先将结果转成 JSON 格式，然后再发出一个 Action（ <code>receivePosts(postTitle, json)</code>）。</p>

<p>上面代码中，有几个地方需要注意。</p>

<blockquote>
  <p>（1）<code>fetchPosts</code>返回了一个函数，而普通的 Action Creator 默认返回一个对象。</p>

<p>（2）返回的函数的参数是<code>dispatch</code>和<code>getState</code>这两个 Redux 方法，普通的 Action Creator 的参数是 Action 的内容。</p>

<p>（3）在返回的函数之中，先发出一个 Action（<code>requestPosts(postTitle)</code>），表示操作开始。</p>

<p>（4）异步操作结束之后，再发出一个 Action（<code>receivePosts(postTitle, json)</code>），表示操作结束。</p>
</blockquote>

<p>这样的处理，就解决了自动发送第二个 Action 的问题。但是，又带来了一个新的问题，Action 是由<code>store.dispatch</code>方法发送的。而<code>store.dispatch</code>方法正常情况下，参数只能是对象，不能是函数。</p>

<p>这时，就要使用中间件。</p>

<blockquote><pre><code class="language-javascript">
import { createStore, applyMiddleware } from 'redux';
import thunk from 'redux-thunk';
import reducer from './reducers';

// Note: this API requires redux@>=3.1.0
const store = createStore(
  reducer,
  applyMiddleware(thunk)
);
</code></pre></blockquote>

<p>上面代码使用<code>redux-thunk</code>中间件，改造<code>store.dispatch</code>，使得后者可以接受函数作为参数。</p>

<p>因此，异步操作的第一种解决方案就是，写出一个返回函数的 Action Creator，然后使用<code>redux-thunk</code>中间件改造<code>store.dispatch</code>。</p>

<h2>六、redux-promise 中间件</h2>

<p>既然 Action Creator 可以返回函数，当然也可以返回其他值。另一种异步操作的解决方案，就是让 Action Creator 返回一个 Promise 对象。</p>

<p>这就需要使用<code>redux-promise</code>中间件。</p>

<blockquote><pre><code class="language-javascript">
import { createStore, applyMiddleware } from 'redux';
import promiseMiddleware from 'redux-promise';
import reducer from './reducers';

const store = createStore(
  reducer,
  applyMiddleware(promiseMiddleware)
); 
</code></pre></blockquote>

<p>这个中间件使得<code>store.dispatch</code>方法可以接受 Promise 对象作为参数。这时，Action Creator 有两种写法。写法一，返回值是一个 Promise 对象。</p>

<blockquote><pre><code class="language-javascript">
const fetchPosts = 
  (dispatch, postTitle) => new Promise(function (resolve, reject) {
     dispatch(requestPosts(postTitle));
     return fetch(`/some/API/${postTitle}.json`)
       .then(response => {
         type: 'FETCH_POSTS',
         payload: response.json()
       });
});
</code></pre></blockquote>

<p>写法二，Action 对象的<code>payload</code>属性是一个 Promise 对象。这需要从模块引入<code>createAction</code>方法，并且写法也要变成下面这样。</p>

<blockquote><pre><code class="language-javascript">
import { createAction } from 'redux-actions';

class AsyncApp extends Component {
  componentDidMount() {
    const { dispatch, selectedPost } = this.props
    // 发出同步 Action
    dispatch(requestPosts(selectedPost));
    // 发出异步 Action
    dispatch(createAction(
      'FETCH_POSTS', 
      fetch(`/some/API/${postTitle}.json`)
        .then(response => response.json())
    ));
  }
</code></pre></blockquote>

<p>上面代码中，第二个<code>dispatch</code>方法发出的是异步 Action，只有等到操作结束，这个 Action 才会实际发出。注意，<code>createAction</code>的第二个参数必须是一个 Promise 对象。</p>

<p>看一下<code>redux-promise</code>的，就会明白它内部是怎么操作的。</p>

<blockquote><pre><code class="language-javascript">
export default function promiseMiddleware({ dispatch }) {
  return next => action => {
    if (!isFSA(action)) {
      return isPromise(action)
        ? action.then(dispatch)
        : next(action);
    }

    return isPromise(action.payload)
      ? action.payload.then(
          result => dispatch({ ...action, payload: result }),
          error => {
            dispatch({ ...action, payload: error, error: true });
            return Promise.reject(error);
          }
        )
      : next(action);
  };
}
</code></pre></blockquote>

<p>从上面代码可以看出，如果 Action 本身是一个 Promise，它 resolve 以后的值应该是一个 Action 对象，会被<code>dispatch</code>方法送出（<code>action.then(dispatch)</code>），但 reject 以后不会有任何动作；如果 Action 对象的<code>payload</code>属性是一个 Promise 对象，那么无论 resolve 和 reject，<code>dispatch</code>方法都会发出 Action。</p>

<p>中间件和异步操作，就介绍到这里。将是最后一部分，介绍如何使用<code>react-redux</code>这个库。</p>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2016-09-20T08:23:28+08:00">2016年9月20日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>购买文集：</li>
<li>社交媒体：</li>
<li>Feed订阅： </li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------
<h1 id="#title_6" >7、Redux 入门教程（一）：基本用法</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2016/09/redux_tutorial_part_one_basic_usages.html](http://www.ruanyifeng.com/blog/2016/09/redux_tutorial_part_one_basic_usages.html)
<p>一年半前，我写了，介绍了 React 的基本用法。</p>

        <p>但是，React 只是 DOM 的一个抽象层，并不是 Web 应用的完整解决方案。也就是说，只用 React 没法写大型应用。</p>

<p>为了解决这个问题，2014年 Facebook 提出了  出现，将 Flux 与函数式编程结合一起，很短时间内就成为了最热门的前端架构。</p>

<p>本文详细介绍 Redux 架构，由于内容较多，全文分成三个部分。今天是第一部分，介绍基本概念和用法。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2016/bg2016091801.png" alt="" title="" /></p>

<h2>零、你可能不需要 Redux</h2>

<p>首先明确一点，Redux 是一个有用的架构，但不是非用不可。事实上，大多数情况，你可以不用它，只用 React 就够了。</p>

<p>曾经有人说过这样一句话。</p>

<blockquote>
  <p>"如果你不知道是否需要 Redux，那就是不需要它。"</p>
</blockquote>

<p>Redux 的创造者 Dan Abramov 又补充了一句。</p>

<blockquote>
  <p>"只有遇到 React 实在解决不了的问题，你才需要 Redux 。"</p>
</blockquote>

<p>简单说，如果你的UI层非常简单，没有很多互动，Redux 就是不必要的，用了反而增加复杂性。</p>

<blockquote>
  <ul>
<li>用户的使用方式非常简单</li>
<li>用户之间没有协作</li>
<li>不需要与服务器大量交互，也没有使用 WebSocket</li>
<li>视图层（View）只从单一来源获取数据</li>
</ul>
</blockquote>

<p>上面这些情况，都不需要使用 Redux。</p>

<blockquote>
  <ul>
<li>用户的使用方式复杂</li>
<li>不同身份的用户有不同的使用方式（比如普通用户和管理员）</li>
<li>多个用户之间可以协作</li>
<li>与服务器大量交互，或者使用了WebSocket</li>
<li>View要从多个来源获取数据</li>
</ul>
</blockquote>

<p>上面这些情况才是 Redux 的适用场景：多交互、多数据源。</p>

<p>从组件角度看，如果你的应用有以下场景，可以考虑使用 Redux。</p>

<blockquote>
  <ul>
<li>某个组件的状态，需要共享</li>
<li>某个状态需要在任何地方都可以拿到</li>
<li>一个组件需要改变全局状态</li>
<li>一个组件需要改变另一个组件的状态</li>
</ul>
</blockquote>

<p>发生上面情况时，如果不使用 Redux 或者其他状态管理工具，不按照一定规律处理状态的读写，代码很快就会变成一团乱麻。你需要一种机制，可以在同一个地方查询状态、改变状态、传播状态的变化。</p>

<p>总之，不要把 Redux 当作万灵丹，如果你的应用没那么复杂，就没必要用它。另一方面，Redux 只是 Web  架构的一种解决方案，也可以选择其他方案。</p>

<h2>一、预备知识</h2>

<p>阅读本文，你只需要懂 React。如果还懂 Flux，就更好了，会比较容易理解一些概念，但不是必需的。</p>

<p>Redux 有很好的）。你可以先阅读本文，再去官方材料详细研究。</p>

<p>我的目标是，提供一个简洁易懂的、全面的入门级参考文档。</p>

<h2>二、设计思想</h2>

<p>Redux 的设计思想很简单，就两句话。</p>

<blockquote>
  <p>（1）Web 应用是一个状态机，视图与状态是一一对应的。</p>

<p>（2）所有的状态，保存在一个对象里面。</p>
</blockquote>

<p>请务必记住这两句话，下面就是详细解释。</p>

<h2>三、基本概念和 API</h2>

<h3>3.1 Store</h3>

<p>Store 就是保存数据的地方，你可以把它看成一个容器。整个应用只能有一个 Store。</p>

<p>Redux 提供<code>createStore</code>这个函数，用来生成 Store。</p>

<blockquote><pre><code class="language-javascript">
import { createStore } from 'redux';
const store = createStore(fn);
</code></pre></blockquote>

<p>上面代码中，<code>createStore</code>函数接受另一个函数作为参数，返回新生成的 Store 对象。</p>

<h3>3.2 State</h3>

<p><code>Store</code>对象包含所有数据。如果想得到某个时点的数据，就要对 Store 生成快照。这种时点的数据集合，就叫做 State。</p>

<p>当前时刻的 State，可以通过<code>store.getState()</code>拿到。</p>

<blockquote><pre><code class="language-javascript">
import { createStore } from 'redux';
const store = createStore(fn);

const state = store.getState();
</code></pre></blockquote>

<p>Redux 规定， 一个 State 对应一个 View。只要 State 相同，View 就相同。你知道 State，就知道 View 是什么样，反之亦然。</p>

<h3>3.3 Action</h3>

<p>State 的变化，会导致 View 的变化。但是，用户接触不到 State，只能接触到 View。所以，State 的变化必须是 View 导致的。Action 就是 View 发出的通知，表示 State 应该要发生变化了。</p>

<p>Action 是一个对象。其中的<code>type</code>属性是必须的，表示 Action 的名称。其他属性可以自由设置，社区有一个可以参考。</p>

<blockquote><pre><code class="language-javascript">
const action = {
  type: 'ADD_TODO',
  payload: 'Learn Redux'
};
</code></pre></blockquote>

<p>上面代码中，Action 的名称是<code>ADD_TODO</code>，它携带的信息是字符串<code>Learn Redux</code>。</p>

<p>可以这样理解，Action 描述当前发生的事情。改变 State 的唯一办法，就是使用 Action。它会运送数据到 Store。</p>

<h3>3.4 Action Creator</h3>

<p>View 要发送多少种消息，就会有多少种 Action。如果都手写，会很麻烦。可以定义一个函数来生成 Action，这个函数就叫 Action Creator。</p>

<blockquote><pre><code class="language-javascript">
const ADD_TODO = '添加 TODO';

function addTodo(text) {
  return {
    type: ADD_TODO,
    text
  }
}

const action = addTodo('Learn Redux');
</code></pre></blockquote>

<p>上面代码中，<code>addTodo</code>函数就是一个 Action Creator。</p>

<h3>3.5 store.dispatch()</h3>

<p><code>store.dispatch()</code>是 View 发出 Action 的唯一方法。</p>

<blockquote><pre><code class="language-javascript">
import { createStore } from 'redux';
const store = createStore(fn);

store.dispatch({
  type: 'ADD_TODO',
  payload: 'Learn Redux'
});
</code></pre></blockquote>

<p>上面代码中，<code>store.dispatch</code>接受一个 Action 对象作为参数，将它发送出去。</p>

<p>结合 Action Creator，这段代码可以改写如下。</p>

<blockquote><pre><code class="language-javascript">
store.dispatch(addTodo('Learn Redux'));
</code></pre></blockquote>

<h2>3.6 Reducer</h2>

<p>Store 收到 Action 以后，必须给出一个新的 State，这样 View 才会发生变化。这种 State 的计算过程就叫做 Reducer。</p>

<p>Reducer 是一个函数，它接受 Action 和当前 State 作为参数，返回一个新的 State。</p>

<blockquote><pre><code class="language-javascript">
const reducer = function (state, action) {
  // ...
  return new_state;
};
</code></pre></blockquote>

<p>整个应用的初始状态，可以作为 State 的默认值。下面是一个实际的例子。</p>

<blockquote><pre><code class="language-javascript">
const defaultState = 0;
const reducer = (state = defaultState, action) => {
  switch (action.type) {
    case 'ADD':
      return state + action.payload;
    default: 
      return state;
  }
};

const state = reducer(1, {
  type: 'ADD',
  payload: 2
});
</code></pre></blockquote>

<p>上面代码中，<code>reducer</code>函数收到名为<code>ADD</code>的 Action 以后，就返回一个新的 State，作为加法的计算结果。其他运算的逻辑（比如减法），也可以根据 Action 的不同来实现。</p>

<p>实际应用中，Reducer 函数不用像上面这样手动调用，<code>store.dispatch</code>方法会触发 Reducer 的自动执行。为此，Store 需要知道 Reducer 函数，做法就是在生成 Store 的时候，将 Reducer 传入<code>createStore</code>方法。</p>

<blockquote><pre><code class="language-javascript">
import { createStore } from 'redux';
const store = createStore(reducer);
</code></pre></blockquote>

<p>上面代码中，<code>createStore</code>接受 Reducer 作为参数，生成一个新的 Store。以后每当<code>store.dispatch</code>发送过来一个新的 Action，就会自动调用 Reducer，得到新的 State。</p>

<p>为什么这个函数叫做 Reducer 呢？因为它可以作为数组的<code>reduce</code>方法的参数。请看下面的例子，一系列 Action 对象按照顺序作为一个数组。</p>

<blockquote><pre><code class="language-javascript">
const actions = [
  { type: 'ADD', payload: 0 },
  { type: 'ADD', payload: 1 },
  { type: 'ADD', payload: 2 }
];

const total = actions.reduce(reducer, 0); // 3
</code></pre></blockquote>

<p>上面代码中，数组<code>actions</code>表示依次有三个 Action，分别是加<code>0</code>、加<code>1</code>和加<code>2</code>。数组的<code>reduce</code>方法接受 Reducer 函数作为参数，就可以直接得到最终的状态<code>3</code>。</p>

<h3>3.7 纯函数</h3>

<p>Reducer 函数最重要的特征是，它是一个纯函数。也就是说，只要是同样的输入，必定得到同样的输出。</p>

<p>纯函数是函数式编程的概念，必须遵守以下一些约束。</p>

<blockquote>
  <ul>
<li>不得改写参数</li>
<li>不能调用系统 I/O 的API</li>
<li>不能调用<code>Date.now()</code>或者<code>Math.random()</code>等不纯的方法，因为每次会得到不一样的结果</li>
</ul>
</blockquote>

<p>由于 Reducer 是纯函数，就可以保证同样的State，必定得到同样的 View。但也正因为这一点，Reducer 函数里面不能改变 State，必须返回一个全新的对象，请参考下面的写法。</p>

<blockquote><pre><code class="language-javascript">
// State 是一个对象
function reducer(state, action) {
  return Object.assign({}, state, { thingToChange });
  // 或者
  return { ...state, ...newState };
}

// State 是一个数组
function reducer(state, action) {
  return [...state, newItem];
}
</code></pre></blockquote>

<p>最好把 State 对象设成只读。你没法改变它，要得到新的 State，唯一办法就是生成一个新对象。这样的好处是，任何时候，与某个 View 对应的 State 总是一个不变的对象。</p>

<h3>3.8 store.subscribe()</h3>

<p>Store 允许使用<code>store.subscribe</code>方法设置监听函数，一旦 State 发生变化，就自动执行这个函数。</p>

<blockquote><pre><code class="language-javascript">
import { createStore } from 'redux';
const store = createStore(reducer);

store.subscribe(listener);
</code></pre></blockquote>

<p>显然，只要把 View 的更新函数（对于 React 项目，就是组件的<code>render</code>方法或<code>setState</code>方法）放入<code>listen</code>，就会实现 View 的自动渲染。</p>

<p><code>store.subscribe</code>方法返回一个函数，调用这个函数就可以解除监听。</p>

<blockquote><pre><code class="language-javascript">
let unsubscribe = store.subscribe(() =>
  console.log(store.getState())
);

unsubscribe();
</code></pre></blockquote>

<h2>四、Store 的实现</h2>

<p>上一节介绍了 Redux 涉及的基本概念，可以发现 Store 提供了三个方法。</p>

<blockquote>
  <ul>
<li>store.getState()</li>
<li>store.dispatch()</li>
<li>store.subscribe()</li>
</ul>
</blockquote>

<blockquote><pre><code class="language-javascript">
import { createStore } from 'redux';
let { subscribe, dispatch, getState } = createStore(reducer);
</code></pre></blockquote>

<p><code>createStore</code>方法还可以接受第二个参数，表示 State 的最初状态。这通常是服务器给出的。</p>

<blockquote><pre><code class="language-javascript">
let store = createStore(todoApp, window.STATE_FROM_SERVER)
</code></pre></blockquote>

<p>上面代码中，<code>window.STATE_FROM_SERVER</code>就是整个应用的状态初始值。注意，如果提供了这个参数，它会覆盖 Reducer 函数的默认初始值。</p>

<p>下面是<code>createStore</code>方法的一个简单实现，可以了解一下 Store 是怎么生成的。</p>

<blockquote><pre><code class="language-javascript">
const createStore = (reducer) => {
  let state;
  let listeners = [];

  const getState = () => state;

  const dispatch = (action) => {
    state = reducer(state, action);
    listeners.forEach(listener => listener());
  };

  const subscribe = (listener) => {
    listeners.push(listener);
    return () => {
      listeners = listeners.filter(l => l !== listener);
    }
  };

  dispatch({});

  return { getState, dispatch, subscribe };
};
</code></pre></blockquote>

<h2>五、Reducer 的拆分</h2>

<p>Reducer 函数负责生成 State。由于整个应用只有一个 State 对象，包含所有数据，对于大型应用来说，这个 State 必然十分庞大，导致 Reducer 函数也十分庞大。</p>

<p>请看下面的例子。</p>

<blockquote><pre><code class="language-javascript">
const chatReducer = (state = defaultState, action = {}) => {
  const { type, payload } = action;
  switch (type) {
    case ADD_CHAT:
      return Object.assign({}, state, {
        chatLog: state.chatLog.concat(payload)
      });
    case CHANGE_STATUS:
      return Object.assign({}, state, {
        statusMessage: payload
      });
    case CHANGE_USERNAME:
      return Object.assign({}, state, {
        userName: payload
      });
    default: return state;
  }
};
</code></pre></blockquote>

<p>上面代码中，三种 Action 分别改变 State 的三个属性。</p>

<blockquote>
  <ul>
<li>ADD_CHAT：<code>chatLog</code>属性</li>
<li>CHANGE_STATUS：<code>statusMessage</code>属性</li>
<li>CHANGE_USERNAME：<code>userName</code>属性</li>
</ul>
</blockquote>

<p>这三个属性之间没有联系，这提示我们可以把 Reducer 函数拆分。不同的函数负责处理不同属性，最终把它们合并成一个大的 Reducer 即可。</p>

<blockquote><pre><code class="language-javascript">
const chatReducer = (state = defaultState, action = {}) => {
  return {
    chatLog: chatLog(state.chatLog, action),
    statusMessage: statusMessage(state.statusMessage, action),
    userName: userName(state.userName, action)
  }
};
</code></pre></blockquote>

<p>上面代码中，Reducer 函数被拆成了三个小函数，每一个负责生成对应的属性。</p>

<p>这样一拆，Reducer 就易读易写多了。而且，这种拆分与 React 应用的结构相吻合：一个 React 根组件由很多子组件构成。这就是说，子组件与子 Reducer 完全可以对应。</p>

<p>Redux 提供了一个<code>combineReducers</code>方法，用于 Reducer 的拆分。你只要定义各个子 Reducer 函数，然后用这个方法，将它们合成一个大的 Reducer。</p>

<blockquote><pre><code class="language-javascript">
import { combineReducers } from 'redux';

const chatReducer = combineReducers({
  chatLog,
  statusMessage,
  userName
})

export default todoApp;
</code></pre></blockquote>

<p>上面的代码通过<code>combineReducers</code>方法将三个子 Reducer 合并成一个大的函数。</p>

<p>这种写法有一个前提，就是 State 的属性名必须与子 Reducer 同名。如果不同名，就要采用下面的写法。</p>

<blockquote><pre><code class="language-javascript">
const reducer = combineReducers({
  a: doSomethingWithA,
  b: processB,
  c: c
})

// 等同于
function reducer(state = {}, action) {
  return {
    a: doSomethingWithA(state.a, action),
    b: processB(state.b, action),
    c: c(state.c, action)
  }
}
</code></pre></blockquote>

<p>总之，<code>combineReducers()</code>做的就是产生一个整体的 Reducer 函数。该函数根据 State 的 key 去执行相应的子 Reducer，并将返回结果合并成一个大的 State 对象。</p>

<p>下面是<code>combineReducer</code>的简单实现。</p>

<blockquote><pre><code class="language-javascript">
const combineReducers = reducers => {
  return (state = {}, action) => {
    return Object.keys(reducers).reduce(
      (nextState, key) => {
        nextState[key] = reducers[key](state[key], action);
        return nextState;
      },
      {} 
    );
  };
};
</code></pre></blockquote>

<p>你可以把所有子 Reducer 放在一个文件里面，然后统一引入。</p>

<blockquote><pre><code class="language-javascript">
import { combineReducers } from 'redux'
import * as reducers from './reducers'

const reducer = combineReducers(reducers)
</code></pre></blockquote>

<h2>六、工作流程</h2>

<p>本节对 Redux 的工作流程，做一个梳理。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2016/bg2016091802.jpg" alt="" title="" /></p>

<p>首先，用户发出 Action。</p>

<blockquote><pre><code class="language-javascript">
store.dispatch(action);
</code></pre></blockquote>

<p>然后，Store 自动调用 Reducer，并且传入两个参数：当前 State 和收到的 Action。 Reducer 会返回新的 State 。</p>

<blockquote><pre><code class="language-javascript">
let nextState = todoApp(previousState, action);
</code></pre></blockquote>

<p>State 一旦有变化，Store 就会调用监听函数。</p>

<blockquote><pre><code class="language-javascript">
// 设置监听函数
store.subscribe(listener);
</code></pre></blockquote>

<p><code>listener</code>可以通过<code>store.getState()</code>得到当前状态。如果使用的是 React，这时可以触发重新渲染 View。</p>

<blockquote><pre><code class="language-javascript">
function listerner() {
  let newState = store.getState();
  component.setState(newState);   
}
</code></pre></blockquote>

<h2>七、实例：计数器</h2>

<p>下面我们来看一个最简单的实例。</p>

<blockquote><pre><code class="language-javascript">
const Counter = ({ value }) => (
  &lt;h1>{value}&lt;/h1>
);

const render = () => {
  ReactDOM.render(
    &lt;Counter value={store.getState()}/>,
    document.getElementById('root')
  );
};

store.subscribe(render);
render();
</code></pre></blockquote>

<p>上面是一个简单的计数器，唯一的作用就是把参数<code>value</code>的值，显示在网页上。Store 的监听函数设置为<code>render</code>，每次 State 的变化都会导致网页重新渲染。</p>

<p>下面加入一点变化，为<code>Counter</code>添加递增和递减的 Action。</p>

<blockquote><pre><code class="language-javascript">
const Counter = ({ value }) => (
  &lt;h1>{value}&lt;/h1>
  &lt;button onClick={onIncrement}>+&lt;/button>
  &lt;button onClick={onDecrement}>-&lt;/button>
);

const reducer = (state = 0, action) => {
  switch (action.type) {
    case 'INCREMENT': return state + 1;
    case 'DECREMENT': return state - 1;
    default: return state;
  }
};

const store = createStore(reducer);

const render = () => {
  ReactDOM.render(
    &lt;Counter
      value={store.getState()}
      onIncrement={() => store.dispatch({type: 'INCREMENT'})}
      onDecrement={() => store.dispatch({type: 'DECREMENT'})}
    />,
    document.getElementById('root')
  );
};

render();
store.subscribe(render);
</code></pre></blockquote>

<p>完整的代码请看。</p>

<p>Redux 的基本用法就介绍到这里，介绍它的高级用法：中间件和异步操作。</p>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2016-09-18T13:15:13+08:00">2016年9月18日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>购买文集：</li>
<li>社交媒体：</li>
<li>Feed订阅： </li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------
<h1 id="#title_7" >8、Content Security Policy 入门教程</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2016/09/csp.html](http://www.ruanyifeng.com/blog/2016/09/csp.html)
<p>跨域脚本攻击  是最常见、危害最大的网页安全漏洞。</p>

        <p><img src="http://www.ruanyifeng.com/blogimg/asset/2016/bg2016091301.png" alt="" title="" /></p>

<p>为了防止它们，要采取很多编程措施，非常麻烦。很多人提出，能不能根本上解决问题，浏览器自动禁止外部注入恶意脚本？</p>

<p>这就是"网页安全政策"（Content Security Policy，缩写 CSP）的来历。本文详细介绍如何使用 CSP 防止 XSS 攻击。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2016/bg2016091302.jpg" alt="" title="" /></p>

<h2>一、简介</h2>

<p>CSP 的实质就是白名单制度，开发者明确告诉客户端，哪些外部资源可以加载和执行，等同于提供白名单。它的实现和执行全部由浏览器完成，开发者只需提供配置。</p>

<p>CSP 大大增强了网页的安全性。攻击者即使发现了漏洞，也没法注入脚本，除非还控制了一台列入了白名单的可信主机。</p>

<p>两种方法可以启用 CSP。一种是通过 HTTP 头信息的<code>Content-Security-Policy</code>的字段。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2016/bg2016091305.jpg" alt="" title="" /></p>

<blockquote><pre><code class="language-http">
Content-Security-Policy: script-src 'self'; object-src 'none';
style-src cdn.example.org third-party.org; child-src https:
</code></pre></blockquote>

<p>另一种是通过网页的<code>&lt;meta&gt;</code>标签。</p>

<blockquote><pre><code class="language-markup">
&lt;meta http-equiv="Content-Security-Policy" content="script-src 'self'; object-src 'none'; style-src cdn.example.org third-party.org; child-src https:">
</code></pre></blockquote>

<p>上面代码中，CSP 做了如下配置。</p>

<blockquote>
  <ul>
<li>脚本：只信任当前域名</li>
<li><code>&lt;object&gt;</code>标签：不信任任何URL，即不加载任何资源</li>
<li>样式表：只信任<code>cdn.example.org</code>和<code>third-party.org</code></li>
<li>框架（frame）：必须使用HTTPS协议加载</li>
<li>其他资源：没有限制</li>
</ul>
</blockquote>

<p>启用后，不符合 CSP 的外部资源就会被阻止加载。</p>

<p>Chrome 的报错信息。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2016/bg2016091303.png" alt="" title="" /></p>

<p>Firefox 的报错信息。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2016/bg2016091306.png" alt="" title="" /></p>

<h2>二、限制选项</h2>

<p>CSP 提供了很多限制选项，涉及安全的各个方面。</p>

<h3>2.1 资源加载限制</h3>

<p>以下选项限制各类资源的加载。</p>

<blockquote>
  <ul>
<li><strong><code>script-src</code></strong>：外部脚本</li>
<li><strong><code>style-src</code></strong>：样式表</li>
<li><strong><code>img-src</code></strong>：图像</li>
<li><strong><code>media-src</code></strong>：媒体文件（音频和视频）</li>
<li><strong><code>font-src</code></strong>：字体文件</li>
<li><strong><code>object-src</code></strong>：插件（比如 Flash）</li>
<li><strong><code>child-src</code></strong>：框架</li>
<li><strong><code>frame-ancestors</code></strong>：嵌入的外部资源（比如&lt;frame>、&lt;iframe>、&lt;embed>和&lt;applet>） </li>
<li><strong><code>connect-src</code></strong>：HTTP 连接（通过 XHR、WebSockets、EventSource等）</li>
<li><strong><code>worker-src</code></strong>：<code>worker</code>脚本</li>
<li><strong><code>manifest-src</code></strong>：manifest 文件</li>
</ul>
</blockquote>

<h3>2.2 default-src</h3>

<p><code>default-src</code>用来设置上面各个选项的默认值。</p>

<blockquote><pre><code class="language-http">
Content-Security-Policy: default-src 'self'
</code></pre></blockquote>

<p>上面代码限制<strong>所有的</strong>外部资源，都只能从当前域名加载。</p>

<p>如果同时设置某个单项限制（比如<code>font-src</code>）和<code>default-src</code>，前者会覆盖后者，即字体文件会采用<code>font-src</code>的值，其他资源依然采用<code>default-src</code>的值。</p>

<h3>2.3 URL 限制</h3>

<p>有时，网页会跟其他 URL 发生联系，这时也可以加以限制。</p>

<blockquote>
  <ul>
<li><strong><code>frame-ancestors</code></strong>：限制嵌入框架的网页</li>
<li><strong><code>base-uri</code></strong>：限制<code>&lt;base#href&gt;</code></li>
<li><strong><code>form-action</code></strong>：限制<code>&lt;form#action&gt;</code></li>
</ul>
</blockquote>

<h3>2.4 其他限制</h3>

<p>其他一些安全相关的功能，也放在了 CSP 里面。</p>

<blockquote>
  <ul>
<li><strong><code>block-all-mixed-content</code></strong>：HTTPS 网页不得加载 HTTP 资源（浏览器已经默认开启）</li>
<li><strong><code>upgrade-insecure-requests</code></strong>：自动将网页上所有加载外部资源的 HTTP 链接换成 HTTPS 协议</li>
<li><strong><code>plugin-types</code></strong>：限制可以使用的插件格式</li>
<li><strong><code>sandbox</code></strong>：浏览器行为的限制，比如不能有弹出窗口等。</li>
</ul>
</blockquote>

<h3>2.5 report-uri</h3>

<p>有时，我们不仅希望防止 XSS，还希望记录此类行为。<code>report-uri</code>就用来告诉浏览器，应该把注入行为报告给哪个网址。</p>

<blockquote><pre><code class="language-http">
Content-Security-Policy: default-src 'self'; ...; report-uri /my_amazing_csp_report_parser;
</code></pre></blockquote>

<p>上面代码指定，将注入行为报告给<code>/my_amazing_csp_report_parser</code>这个 URL。</p>

<p>浏览器会使用<code>POST</code>方法，发送一个JSON对象，下面是一个例子。</p>

<blockquote><pre><code class="language-javascript">
{
  "csp-report": {
    "document-uri": "http://example.org/page.html",
    "referrer": "http://evil.example.com/",
    "blocked-uri": "http://evil.example.com/evil.js",
    "violated-directive": "script-src 'self' https://apis.google.com",
    "original-policy": "script-src 'self' https://apis.google.com; report-uri http://example.org/my_amazing_csp_report_parser"
  }
}
</code></pre></blockquote>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2016/bg2016091304.png" alt="" title="" /></p>

<h2>三、Content-Security-Policy-Report-Only</h2>

<p>除了<code>Content-Security-Policy</code>，还有一个<code>Content-Security-Policy-Report-Only</code>字段，表示不执行限制选项，只是记录违反限制的行为。</p>

<p>它必须与<code>report-uri</code>选项配合使用。</p>

<blockquote><pre><code class="language-http">
Content-Security-Policy-Report-Only: default-src 'self'; ...; report-uri /my_amazing_csp_report_parser;
</code></pre></blockquote>

<h2>四、选项值</h2>

<p>每个限制选项可以设置以下几种值，这些值就构成了白名单。 </p>

<blockquote>
  <ul>
<li>主机名：<code>example.org</code>，<code>https://example.com:443</code></li>
<li>路径名：<code>example.org/resources/js/</code></li>
<li>通配符：<code>*.example.org</code>，<code>*://*.example.com:*</code>（表示任意协议、任意子域名、任意端口）</li>
<li>协议名：<code>https:</code>、<code>data:</code></li>
<li>关键字<code>'self'</code>：当前域名，需要加引号</li>
<li>关键字<code>'none'</code>：禁止加载任何外部资源，需要加引号</li>
</ul>
</blockquote>

<p>多个值也可以并列，用空格分隔。</p>

<blockquote><pre><code class="language-http">
Content-Security-Policy: script-src 'self' https://apis.google.com
</code></pre></blockquote>

<p>如果同一个限制选项使用多次，只有第一次会生效。</p>

<blockquote><pre><code class="language-http">
# 错误的写法
script-src https://host1.com; script-src https://host2.com

# 正确的写法
script-src https://host1.com https://host2.com
</code></pre></blockquote>

<p>如果不设置某个限制选项，就是默认允许任何值。</p>

<h2>五、script-src 的特殊值</h2>

<p>除了常规值，<code>script-src</code>还可以设置一些特殊值。注意，下面这些值都必须放在单引号里面。</p>

<blockquote>
  <ul>
<li><strong><code>'unsafe-inline'</code></strong>：允许执行页面内嵌的<code>&amp;lt;script&gt;</code>标签和事件监听函数</li>
<li><strong><code>unsafe-eval</code></strong>：允许将字符串当作代码执行，比如使用<code>eval</code>、<code>setTimeout</code>、<code>setInterval</code>和<code>Function</code>等函数。</li>
<li><strong>nonce值</strong>：每次HTTP回应给出一个授权token，页面内嵌脚本必须有这个token，才会执行</li>
<li><strong>hash值</strong>：列出允许执行的脚本代码的Hash值，页面内嵌脚本的哈希值只有吻合的情况下，才能执行。</li>
</ul>
</blockquote>

<p>nonce值的例子如下，服务器发送网页的时候，告诉浏览器一个随机生成的token。</p>

<blockquote><pre><code class="language-http">
Content-Security-Policy: script-src 'nonce-EDNnf03nceIOfn39fn3e9h3sdfa'
</code></pre></blockquote>

<p>页面内嵌脚本，必须有这个token才能执行。</p>

<blockquote><pre><code class="language-javascript">
&lt;script nonce=EDNnf03nceIOfn39fn3e9h3sdfa>
  // some code
&lt;/script>
</code></pre></blockquote>

<p>hash值的例子如下，服务器给出一个允许执行的代码的hash值。</p>

<blockquote><pre><code class="language-http">
Content-Security-Policy: script-src 'sha256-qznLcsROx4GACP2dm0UCKCzCG-HiZ1guq6ZZDob_Tng='
</code></pre></blockquote>

<p>下面的代码就会允许执行，因为hash值相符。</p>

<blockquote><pre><code class="language-markup">
&lt;script>alert('Hello, world.');&lt;/script>
</code></pre></blockquote>

<p>注意，计算hash值的时候，&lt;script>标签不算在内。</p>

<p>除了<code>script-src</code>选项，nonce值和hash值还可以用在<code>style-src</code>选项，控制页面内嵌的样式表。</p>

<h2>六、注意点</h2>

<p>（1）<code>script-src</code>和<code>object-src</code>是必设的，除非设置了<code>default-src</code>。</p>

<p>因为攻击者只要能注入脚本，其他限制都可以规避。而<code>object-src</code>必设是因为 Flash 里面可以执行外部脚本。</p>

<p>（2）<code>script-src</code>不能使用<code>unsafe-inline</code>关键字（除非伴随一个nonce值），也不能允许设置<code>data:</code>URL。</p>

<p>下面是两个恶意攻击的例子。</p>

<blockquote><pre><code class="language-markup">
&lt;img src="x" onerror="evil()">
&lt;script src="data:text/javascript,evil()">&lt;/script>
</code></pre></blockquote>

<p>（3）必须特别注意 JSONP 的回调函数。</p>

<blockquote><pre><code class="language-markup">
&lt;script
src="/path/jsonp?callback=alert(document.domain)//">
&lt;/script>
</code></pre></blockquote>

<p>上面的代码中，虽然加载的脚本来自当前域名，但是通过改写回调函数，攻击者依然可以执行恶意代码。</p>

<h2>七、参考链接</h2>

<ul>
<li>, by Lukas Weichselbaum</li>
<li>, by Mike West</li>
</ul>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2016-09-13T09:03:54+08:00">2016年9月13日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>购买文集：</li>
<li>社交媒体：</li>
<li>Feed订阅： </li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------
<h1 id="#title_8" >9、亚马逊如何变成 SOA（面向服务的架构）？</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2016/09/how_amazon_take_soa.html](http://www.ruanyifeng.com/blog/2016/09/how_amazon_take_soa.html)
<p>，我摘录了《程序员的呐喊》。这本书有趣的内容太多，今天再摘录一段。</p>

        <p>1、 </p>

<p>亚马逊公司不仅是世界最大的网络书店，还是世界最大的云服务商。它是怎么实现从电商到云商的转变呢？</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2016/bg2016091101.jpg" alt="" title="" /></p>

<p>一切都是CEO杰夫·贝索斯促成的，他对市场有着超乎常人的理解和预见。</p>

<p>2、</p>

<p>2000年前后，贝索斯有一次在员工大会上提到，各种办公工具、书籍、影音制品都可以数字化，所以也意味着很容易盗版。数字产品可能会利润越来越低，很快就不再产生任何收入了。</p>

<p>所有的民用工业品也都很不妙，服装和电子消费品的消费周期越来越短。连烤炉这种东西，也没人想要去年的型号。总之，卖这些东西，看上去也不太会赚大钱。</p>

<p>亚马逊未来靠什么赚钱，贝索斯不仅忧心忡忡。</p>

<p>3、</p>

<p>2002年，贝索斯突然向全公司发布了一道指令。</p>

<blockquote>
  <p>（1）从今天起，所有的团队都要以服务接口的方式，提供数据和各种功能。</p>

<p>（2）团队之间必须通过接口来通信。</p>

<p>（3）不允许任何其他形式的互操作：不允许直接链接，不允许直接读其他团队的数据，不允许共享内存，不允许任何形式的后门。唯一许可的通信方式，就是通过网络调用服务。</p>

<p>（4）具体的实现技术不做规定，HTTP、Corba、PubSub、自定义协议皆可。</p>

<p>（5）所有的服务接口，必须从一开始就以可以公开作为设计导向，没有例外。这就是说，在设计接口的时候，就默认这个接口可以对外部人员开放，没有讨价还价的余地。</p>

<p>（6）不遵守上面规定，就开除。</p>
</blockquote>

<p>他意识到，亚马逊现有的卖书送书的基础设施，其实可以变成一个非常出色、可定制的计算平台，让用户付费使用。但是前提是，整个基础设施必须改造成面向服务的架构。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2016/bg2016091102.jpg" alt="" title="" /></p>

<p>4.</p>

<p>接下来的几年里，亚马逊全公司都转向了面向服务的架构（SOA）。这个过程中，工程师们得到了大量的经验教训。</p>

<p><strong>教训一：SOA架构的错误定位，非常麻烦。</strong></p>

<p>一个请求可能要经过20次服务器调用，才能找到问题的真正所在。通常，单单是问题的定位就要花费15分钟到几个小时，除非搭建大量的外围监控和报警措施。</p>

<p><strong>教训二：同事也是潜在的 DOS 攻击者。</strong></p>

<p>公司内部某个小组，会突然对你的服务发起大量请求。除非每个服务都设有严格的用量和限量措施，否则根本无法保证可用性。</p>

<p><strong>教训三：监控和质量保障（QA）是两回事。</strong></p>

<p>监控一个服务的时候，可能会得到"一切正常"的回复。但是很有可能，整个服务唯一还正常工作的部分，就是这个回应"一切正常"的模块。只有完整地调用服务，才能确定服务是正常的。</p>

<p>这意味着，真正监控一个服务，必须做到对所有的服务和数据进行完整的语意检查，否则是看不出问题的。如果做到了这一点，本质上就是在做自动化 QA 了。</p>

<p><strong>教训四：必须有服务发现机制。</strong></p>

<p>面对成百上千的服务时，没有服务发现机制是不可想象的。这又离不开服务注册机制，而它本身也是一个服务。亚马逊有一套统一的服务注册机制，可以通过编程的方式找到所有服务，包括一个服务有哪些API，目前是不是运行正常，在什么位置等。</p>

<p><strong>教训五：必须有沙箱用来调试</strong></p>

<p>如果代码中调用了他人服务，查找问题的难度要高很多，除非有统一的方式在沙箱里运行所有服务，否则几乎不可能进行任何调试。</p>

<p><strong>教训六：不能信任任何人</strong></p>

<p>团队采用服务的方式进行合作以后，基本上就不能信任其他团队了，正如不能信任第三方工程师一样。</p>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2016-09-10T19:09:43+08:00">2016年9月10日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>购买文集：</li>
<li>社交媒体：</li>
<li>Feed订阅： </li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------
<h1 id="#title_9" >10、程序员小测试：保守派 vs 自由派</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2016/09/conservative_vs_liberal_programmer.html](http://www.ruanyifeng.com/blog/2016/09/conservative_vs_liberal_programmer.html)
<p>最近，我在阅读 Steve Yegg 的文集。</p>

        <p><img src="http://www.ruanyifeng.com/blogimg/asset/2016/bg2016090801.jpg" alt="" title="" /></p>

<p>这是一本非常有趣的书，里面甚至包含了一个小测试（），区分一个程序员到底是保守派还是自由派。</p>

<p>下面一共有十个问题，每个问题都有 A 和 B 两个选项，请选择你的答案。</p>

<h2>问题一：Bug 还没修复，软件能不能上线？</h2>

<p>（A）软件发布前，应该编写完整测试，充分调试，尽量修复所有bug。</p>

<p>（B）不管多努力，bug 总是无法避免的，如果性质不是很严重，可以先上线，根据反馈再调试和修补。</p>

<h2>问题二：容易出错的特性，是否应该用在程序中？</h2>

<p>（A）很多语言的高级特性都是很容易出错和危险的，应该禁止用在代码里。没有这些特性我们一样可以进行开发，代码也会因此变得更安全。</p>

<p>（B）聪明的程序员有学习动力，知道怎么可以解决问题。为了避免出错，就立下一堆规矩，完全不可取。</p>

<h2>问题三：新的语言或语法是否应该有所限制？</h2>

<p>（A）公司里可以使用的语言数量应该受到限制，这样万一系统在半夜或是圣诞夜挂掉的时候，值班的人就不需要去临时抱佛脚学习新语法了。另外，也应该禁止改变语言原始定义的语法，比如严格限制操作符重载和元编程。</p>

<p>（B）程序员的学习能力是惊人的，没必要"保护"程序员远离新语法，只要有需要，他们自然能学会。</p>

<h2>问题四：静态检查是否必要？</h2>

<p>（A）编译器的安全检查很重要，不能进行静态检查的代码通常是不可接受的。</p>

<p>（B）代码应该短小精悍，静态检查工具可能会让代码变得又臭又长。</p>

<h2>问题五：数据是否一定要有格式定义？</h2>

<p>（A）数据必须遵循事先定义好的格式。比如，关系型数据库必须满足第三范式或UML，XML都必须有DTD，NoSQL数据库必须有单独的格式定义（标明所有允许的键，以及相应的值类型）。</p>

<p>（B）严格的数据定义只会妨碍灵活性，延缓开发进程。更好的策略是写一些注释，或者只定义一部分，甚至先略过它。因为在大量用户案例出现之前，没人知道数据可能会是什么样，代码先行才是正确的做法。</p>

<h2>问题六：公共接口是否应该静态化？</h2>

<p>（A）公共接口必须严格建模。数据绝不可以是无类型的，所有的输入输出实体都必须完整显式地定义为可以静态检查的模型。</p>

<p>（B）公共接口应该尽量简单，向前向后都兼容。建模时太过缜密的话，其实只是在猜测接口会怎么演化。</p>

<h2>问题七：是否可以留有方便修改的后门？</h2>

<p>（A）生产系统里绝不允许存在危险或有风险的后门。想要通过调试器、SSH、或任何接口，连接到工作中的生产系统，去修改运行时的代码或数据，应该是不可能的。</p>

<p>（B）系统的灵活性，有时能决定客户或合同是归你还是归对手。至于生产系统的安全隐患，可以通过日志、监控、审核等手段来缓解。事实证明，很多有最高权限后门和Shell 接口的大型系统，都做到了在控制风险的同时具备运行灵活性。</p>

<h2>问题八：急需的但有安全隐患的系统，是否可以上线？</h2>

<p>（A）假如一个组件的安全性存在任何疑虑，那它就不能发布上线，团队怎么哀求都没用。</p>

<p>（B）企业要保持竞争力，唯有不断有意识地去承担风险。就算不去冒险，其他系统急需这个系统，线上可能还是会出问题，既然如此那还不如冒险一试。</p>

<h2>问题九：代码运行较慢，是否要去解决？</h2>

<p>（A）快比慢好。没人喜欢慢的代码，所以代码的性能一定要好。从一开始，就要有性能意识，那些比较慢的语言和库都应该避免使用。</p>

<p>（B）不要过早优化，代码先跑起来再说。正确性比性能重要，而原型的快速迭代又比正确性更重要。只有当客户将性能列为首要问题时，再进行优化。</p>

<h2>问题十：你最认可的语言是哪一个？</h2>

<p>（A）C++、Java、C#、D、Go、Clojure、Ada、Ocaml、Eiffel、Clojure、Erlang、Pascal、Haskell、SML。</p>

<p>（B）C、Objective-C、JavaScript、Visual Basic、Lua、Scheme、Python、Common Lisp、Smalltalk/Squeak、Perl、Ruby、PHP，Bash。</p>

<h2>结论</h2>

<p>如果你的答案有超过一半的 A，你就属于保守派程序员。你非常重视软件安全和可靠性，厌恶风险，提倡严格管理，认为有效的规章制度是软件质量的保证。</p>

<p>如果你的答案有超过一半的 B，你就属于自由派程序员。你重视软件开发的灵活性，提倡给予程序员足够的自由，只要新功能顺利上线，可以接受一定的风险和瑕疵。</p>

<p>保守派或自由派，都没问题，都是可取的。问题是一支和谐的团队最好是由单一人群组成，要么全是自由派，要么全是保守派，免得双方不停地发生理念上的冲突。</p>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2016-09-08T09:40:13+08:00">2016年9月 8日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>购买文集：</li>
<li>社交媒体：</li>
<li>Feed订阅： </li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------
<h1 id="#title_10" >11、软件架构入门</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2016/09/software-architecture.html](http://www.ruanyifeng.com/blog/2016/09/software-architecture.html)
<p>软件架构（software architecture）就是软件的基本结构。</p>

        <p>合适的架构是软件成功的最重要因素之一。大型软件公司通常有专门的架构师职位（architect），只有资深程序员才可以担任。</p>

<p>O'Reilly 出版过一本免费的小册子）， 介绍了五种最常见的软件架构，是非常好的入门读物。我读后受益匪浅，下面就是我的笔记。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2016/bg2016090301.png" alt="" title="" /></p>

<h2>一、分层架构</h2>

<p>分层架构（layered architecture）是最常见的软件架构，也是事实上的标准架构。如果你不知道要用什么架构，那就用它。</p>

<p>这种架构将软件分成若干个水平层，每一层都有清晰的角色和分工，不需要知道其他层的细节。层与层之间通过接口通信。</p>

<p>虽然没有明确约定，软件一定要分成多少层，但是四层的结构最常见。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2016/bg2016090302.png" alt="" title="" /></p>

<blockquote>
  <ul>
<li>表现层（presentation）：用户界面，负责视觉和用户互动</li>
<li>业务层（business）：实现业务逻辑</li>
<li>持久层（persistence）：提供数据，SQL 语句就放在这一层</li>
<li>数据库（database） ：保存数据 </li>
</ul>
</blockquote>

<p>有的软件在逻辑层和持久层之间，加了一个服务层（service），提供不同业务逻辑需要的一些通用接口。</p>

<p>用户的请求将依次通过这四层的处理，不能跳过其中任何一层。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2016/bg2016090303.png" alt="" title="" /></p>

<p>优点</p>

<blockquote>
  <ul>
<li>结构简单，容易理解和开发</li>
<li>不同技能的程序员可以分工，负责不同的层，天然适合大多数软件公司的组织架构</li>
<li>每一层都可以独立测试，其他层的接口通过模拟解决</li>
</ul>
</blockquote>

<p>缺点</p>

<blockquote>
  <ul>
<li>一旦环境变化，需要代码调整或增加功能时，通常比较麻烦和费时</li>
<li>部署比较麻烦，即使只修改一个小地方，往往需要整个软件重新部署，不容易做持续发布</li>
<li>软件升级时，可能需要整个服务暂停</li>
<li>扩展性差。用户请求大量增加时，必须依次扩展每一层，由于每一层内部是耦合的，扩展会很困难</li>
</ul>
</blockquote>

<h2>二、事件驱动架构</h2>

<p>事件（event）是状态发生变化时，软件发出的通知。</p>

<p>事件驱动架构（event-driven architecture）就是通过事件进行通信的软件架构。它分成四个部分。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2016/bg2016090304.png" alt="" title="" /></p>

<blockquote>
  <ul>
<li>事件队列（event queue）：接收事件的入口</li>
<li>分发器（event mediator）：将不同的事件分发到不同的业务逻辑单元</li>
<li>事件通道（event channel）：分发器与处理器之间的联系渠道</li>
<li>事件处理器（event processor）：实现业务逻辑，处理完成后会发出事件，触发下一步操作</li>
</ul>
</blockquote>

<p>对于简单的项目，事件队列、分发器和事件通道，可以合为一体，整个软件就分成事件代理和事件处理器两部分。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2016/bg2016090305.png" alt="" title="" /></p>

<p>优点</p>

<blockquote>
  <ul>
<li>分布式的异步架构，事件处理器之间高度解耦，软件的扩展性好</li>
<li>适用性广，各种类型的项目都可以用</li>
<li>性能较好，因为事件的异步本质，软件不易产生堵塞</li>
<li>事件处理器可以独立地加载和卸载，容易部署</li>
</ul>
</blockquote>

<p>缺点</p>

<blockquote>
  <ul>
<li>涉及异步编程（要考虑远程通信、失去响应等情况），开发相对复杂</li>
<li>难以支持原子性操作，因为事件通过会涉及多个处理器，很难回滚</li>
<li>分布式和异步特性导致这个架构较难测试</li>
</ul>
</blockquote>

<h2>三、微核架构</h2>

<p>微核架构（microkernel architecture）又称为"插件架构"（plug-in architecture），指的是软件的内核相对较小，主要功能和业务逻辑都通过插件实现。</p>

<p>内核（core）通常只包含系统运行的最小功能。插件则是互相独立的，插件之间的通信，应该减少到最低，避免出现互相依赖的问题。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2016/bg2016090306.png" alt="" title="" /></p>

<p>优点</p>

<blockquote>
  <ul>
<li>良好的功能延伸性（extensibility），需要什么功能，开发一个插件即可</li>
<li>功能之间是隔离的，插件可以独立的加载和卸载，使得它比较容易部署，</li>
<li>可定制性高，适应不同的开发需要</li>
<li>可以渐进式地开发，逐步增加功能</li>
</ul>
</blockquote>

<p>缺点</p>

<blockquote>
  <ul>
<li>扩展性（scalability）差，内核通常是一个独立单元，不容易做成分布式</li>
<li>开发难度相对较高，因为涉及到插件与内核的通信，以及内部的插件登记机制</li>
</ul>
</blockquote>

<h2>四、微服务架构</h2>

<p>微服务架构（microservices architecture）是服务导向架构（service-oriented architecture，缩写 SOA）的升级。</p>

<p>每一个服务就是一个独立的部署单元（separately
deployed unit）。这些单元都是分布式的，互相解耦，通过远程通信协议（比如REST、SOAP）联系。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2016/bg2016090307.png" alt="" title="" /></p>

<p>微服务架构分成三种实现模式。</p>

<blockquote>
  <ul>
<li>RESTful API 模式：服务通过 API 提供，云服务就属于这一类</li>
<li>RESTful 应用模式：服务通过传统的网络协议或者应用协议提供，背后通常是一个多功能的应用程序，常见于企业内部</li>
<li>集中消息模式：采用消息代理（message broker），可以实现消息队列、负载均衡、统一日志和异常处理，缺点是会出现单点失败，消息代理可能要做成集群</li>
</ul>
</blockquote>

<p>优点</p>

<blockquote>
  <ul>
<li>扩展性好，各个服务之间低耦合</li>
<li>容易部署，软件从单一可部署单元，被拆成了多个服务，每个服务都是可部署单元</li>
<li>容易开发，每个组件都可以进行持续集成式的开发，可以做到实时部署，不间断地升级</li>
<li>易于测试，可以单独测试每一个服务</li>
</ul>
</blockquote>

<p>缺点</p>

<blockquote>
  <ul>
<li>由于强调互相独立和低耦合，服务可能会拆分得很细。这导致系统依赖大量的微服务，变得很凌乱和笨重，性能也会不佳。</li>
<li>一旦服务之间需要通信（即一个服务要用到另一个服务），整个架构就会变得复杂。典型的例子就是一些通用的 Utility 类，一种解决方案是把它们拷贝到每一个服务中去，用冗余换取架构的简单性。</li>
<li>分布式的本质使得这种架构很难实现原子性操作，交易回滚会比较困难。</li>
</ul>
</blockquote>

<h2>五、云架构</h2>

<p>云结构（cloud architecture）主要解决扩展性和并发的问题，是最容易扩展的架构。</p>

<p>它的高扩展性，主要原因是没使用中央数据库，而是把数据都复制到内存中，变成可复制的内存数据单元。然后，业务处理能力封装成一个个处理单元（prcessing unit）。访问量增加，就新建处理单元；访问量减少，就关闭处理单元。由于没有中央数据库，所以扩展性的最大瓶颈消失了。由于每个处理单元的数据都在内存里，最好要进行数据持久化。</p>

<p>这个模式主要分成两部分：处理单元（processing unit）和虚拟中间件（virtualized middleware）。</p>

<blockquote>
  <ul>
<li>处理单元：实现业务逻辑</li>
<li>虚拟中间件：负责通信、保持sessions、数据复制、分布式处理、处理单元的部署。</li>
</ul>
</blockquote>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2016/bg2016090311.png" alt="" title="" /></p>

<p>虚拟中间件又包含四个组件。</p>

<blockquote>
  <ul>
<li><strong>消息中间件</strong>（Messaging Grid）：管理用户请求和session，当一个请求进来以后，决定分配给哪一个处理单元。</li>
<li><strong>数据中间件</strong>（Data Grid）：将数据复制到每一个处理单元，即数据同步。保证某个处理单元都得到同样的数据。</li>
<li><strong>处理中间件</strong>（Processing Grid）：可选，如果一个请求涉及不同类型的处理单元，该中间件负责协调处理单元</li>
<li><strong>部署中间件</strong>（Deployment Manager）：负责处理单元的启动和关闭，监控负载和响应时间，当负载增加，就新启动处理单元，负载减少，就关闭处理单元。</li>
</ul>
</blockquote>

<p>优点</p>

<blockquote>
  <ul>
<li>高负载，高扩展性</li>
<li>动态部署</li>
</ul>
</blockquote>

<p>缺点</p>

<blockquote>
  <ul>
<li>实现复杂，成本较高</li>
<li>主要适合网站类应用，不合适大量数据吞吐的大型数据库应用</li>
<li>较难测试</li>
</ul>
</blockquote>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2016-09-03T09:36:50+08:00">2016年9月 3日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>购买文集：</li>
<li>社交媒体：</li>
<li>Feed订阅： </li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------
<h1 id="#title_11" >12、HTTPS 升级指南</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2016/08/migrate-from-http-to-https.html](http://www.ruanyifeng.com/blog/2016/08/migrate-from-http-to-https.html)
<p>上一篇文章我介绍了  ，它只有在 HTTPS 环境才会生效。</p>

        <p>为了升级到 HTTP/2 协议，必须先启用 HTTPS。如果你不了解 HTTPS 协议（学名 TLS 协议），可以参考我以前的文章。</p>

<blockquote>
  <ul>
<li></li>
<li></li>
<li></li>
<li></li>
</ul>
</blockquote>

<p>本文介绍如何将一个 HTTP 网站升级到 HTTPS 。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2016/bg2016082601.png" alt="" title="" /></p>

<h2>一、获取证书</h2>

<p>升级到 HTTPS 协议的第一步，就是要获得一张证书。</p>

<p>证书是一个二进制文件，里面包含经过认证的网站公钥和一些元数据，要从经销商购买。</p>

<blockquote>
  <ul>
<li></li>
<li></li>
<li></li>
</ul>
</blockquote>

<p>证书有很多类型，首先分为三种认证级别。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2016/bg2016082602.png" alt="" title="" /></p>

<blockquote>
  <ul>
<li><strong>域名认证</strong>（Domain Validation）：最低级别认证，可以确认申请人拥有这个域名。对于这种证书，浏览器会在地址栏显示一把锁。</li>
<li><strong>公司认证</strong>（Company Validation）：确认域名所有人是哪一家公司，证书里面会包含公司信息。</li>
<li><strong>扩展认证</strong>（Extended Validation）：最高级别的认证，浏览器地址栏会显示公司名。</li>
</ul>
</blockquote>

<p>还分为三种覆盖范围。</p>

<blockquote>
  <ul>
<li><strong>单域名证书</strong>：只能用于单一域名，<code>foo.com</code>的证书不能用于<code>www.foo.com</code></li>
<li><strong>通配符证书</strong>：可以用于某个域名及其所有一级子域名，比如<code>*.foo.com</code>的证书可以用于<code>foo.com</code>，也可以用于<code>www.foo.com</code></li>
<li><strong>多域名证书</strong>：可以用于多个域名，比如<code>foo.com</code>和<code>bar.com</code></li>
</ul>
</blockquote>

<p>认证级别越高、覆盖范围越广的证书，价格越贵。</p>

<p>还有一个免费证书的选择。为了推广HTTPS协议，电子前哨基金会EFF成立了 ）。</p>

<p>拿到证书以后，可以用  检查一下，信息是否正确。</p>

<h2>二、安装证书</h2>

<p>证书可以放在<code>/etc/ssl</code>目录（Linux 系统），然后根据你使用的Web服务器进行配置。</p>

<blockquote>
  <ul>
<li>，by Mozilla</li>
<li>，by SSLMate</li>
</ul>
</blockquote>

<p>如果使用 Let's Encrypt 证书，请使用自动安装工具 。</p>

<p>安装成功后，使用  检查一下证书是否生效。</p>

<h2>三、修改链接</h2>

<p>下一步，网页加载的 HTTP 资源，要全部改成 HTTPS 链接。因为加密网页内如果有非加密的资源，浏览器是不会加载那些资源的。</p>

<blockquote><pre><code class="language-markup">
&lt;script src="http://foo.com/jquery.js">&lt;/script>
</code></pre></blockquote>

<p>上面这行加载命令，有两种改法。</p>

<blockquote><pre><code class="language-markup">
&lt;!-- 改法一 -->
&lt;script src="https://foo.com/jquery.js">&lt;/script>

&lt;!-- 改法二 -->
&lt;script src="//foo.com/jquery.js">&lt;/script>
</code></pre></blockquote>

<p>其中，改法二会根据当前网页的协议，加载相同协议的外部资源，更灵活一些。</p>

<p>另外，如果页面头部用到了<code>rel="canonical"</code>，也要改成HTTPS网址。</p>

<blockquote><pre><code class="language-markup">
&lt;link rel="canonical" href="https://foo.com/bar.html" />
</code></pre></blockquote>

<h2>四、301重定向</h2>

<p>下一步，修改 Web 服务器的配置文件，使用 301 重定向，将 HTTP 协议的访问导向 HTTPS 协议。</p>

<p>。</p>

<blockquote><pre><code class="language-http">
server {
  listen 80;
  server_name domain.com www.domain.com;
  return 301 https://domain.com$request_uri;
}
</code></pre></blockquote>

<p>（<code>.htaccess</code>文件）。</p>

<blockquote><pre><code class="language-bash">
RewriteEngine On
RewriteCond %{HTTPS} off
RewriteRule (.*) https://%{HTTP_HOST}%{REQUEST_URI} [R=301,L]
</code></pre></blockquote>

<h2>五、安全措施</h2>

<p>以下措施可以进一步保证通信安全。</p>

<h3>5.1 HTTP Strict Transport Security (HSTS)</h3>

<p>访问网站时，用户很少直接在地址栏输入<code>https://</code>，总是通过点击链接，或者3xx重定向，从<code>HTTP</code>页面进入<code>HTTPS</code>页面。攻击者完全可以在用户发出<code>HTTP</code>请求时，劫持并篡改该请求。</p>

<p>另一种情况是恶意网站使用自签名证书，冒充另一个网站，这时浏览器会给出警告，但是许多用户会忽略警告继续访问。</p>

<p>"HTTP严格传输安全"（简称 HSTS）的作用，就是强制浏览器只能发出<code>HTTPS</code>请求，并阻止用户接受不安全的证书。</p>

<p>它在网站的响应头里面，加入一个强制性声明。以下例子摘自。</p>

<blockquote><pre><code class="language-http">
Strict-Transport-Security: max-age=31536000; includeSubDomains
</code></pre></blockquote>

<p>上面这段头信息有两个作用。</p>

<blockquote>
  <p>（1）在接下来的一年（即31536000秒）中，浏览器只要向<code>example.com</code>或其子域名发送HTTP请求时，必须采用HTTPS来发起连接。用户点击超链接或在地址栏输入<code>http://www.example.com/</code>，浏览器应当自动将<code>http</code>转写成<code>https</code>，然后直接向<code>https://www.example.com/</code>发送请求。</p>

<p>（2）在接下来的一年中，如果<code>example.com</code>服务器发送的证书无效，用户不能忽略浏览器警告，将无法继续访问该网站。</p>
</blockquote>

<p>HSTS 很大程度上解决了 SSL 剥离攻击。只要浏览器曾经与服务器建立过一次安全连接，之后浏览器会强制使用<code>HTTPS</code>，即使链接被换成了<code>HTTP</code>。</p>

<p>该方法的主要不足是，用户首次访问网站发出HTTP请求时，是不受HSTS保护的。</p>

<p>如果想要全面分析网站的安全程度，可以使用 Mozilla 的 。</p>

<h3>5.2 Cookie</h3>

<p>另一个需要注意的地方是，确保浏览器只在使用 HTTPS 时，才发送Cookie。</p>

<p>网站响应头里面，<code>Set-Cookie</code>字段加上<code>Secure</code>标志即可。</p>

<blockquote><pre><code class="language-http">
Set-Cookie: LSID=DQAAAK...Eaem_vYg; Secure
</code></pre></blockquote>

<h2>六、参考链接</h2>

<ul>
<li>, by Chris Palmer</li>
<li>, by KeyCDN</li>
<li>, by Matt Mansfield</li>
</ul>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2016-08-26T08:21:40+08:00">2016年8月26日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>购买文集：</li>
<li>社交媒体：</li>
<li>Feed订阅： </li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------
<h1 id="#title_12" >13、HTTP 协议入门</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2016/08/http.html](http://www.ruanyifeng.com/blog/2016/08/http.html)
<p>HTTP 协议是互联网的基础协议，也是网页开发的必备知识，最新版本 HTTP/2 更是让它成为技术热点。</p>

        <p>本文介绍 HTTP 协议的历史演变和设计思路。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2016/bg2016081901.jpg" alt="" title="" /></p>

<h2>一、HTTP/0.9</h2>

<p>HTTP 是基于 TCP/IP 协议的。它不涉及数据包（packet）传输，主要规定了客户端和服务器之间的通信格式，默认使用80端口。</p>

<p>最早版本是1991年发布的0.9版。该版本极其简单，只有一个命令<code>GET</code>。</p>

<blockquote><pre><code class="language-http">
GET /index.html
</code></pre></blockquote>

<p>上面命令表示，TCP 连接（connection）建立后，客户端向服务器请求（request）网页<code>index.html</code>。</p>

<p>协议规定，服务器只能回应HTML格式的字符串，不能回应别的格式。</p>

<blockquote><pre><code class="language-html">
&lt;html>
  &lt;body>Hello World&lt;/body>
&lt;/html>
</code></pre></blockquote>

<p>服务器发送完毕，就关闭TCP连接。</p>

<h2>二、HTTP/1.0</h2>

<h3>2.1 简介</h3>

<p>1996年5月，HTTP/1.0 版本发布，内容大大增加。</p>

<p>首先，任何格式的内容都可以发送。这使得互联网不仅可以传输文字，还能传输图像、视频、二进制文件。这为互联网的大发展奠定了基础。</p>

<p>其次，除了<code>GET</code>命令，还引入了<code>POST</code>命令和<code>HEAD</code>命令，丰富了浏览器与服务器的互动手段。</p>

<p>再次，HTTP请求和回应的格式也变了。除了数据部分，每次通信都必须包括头信息（HTTP header），用来描述一些元数据。</p>

<p>其他的新增功能还包括状态码（status code）、多字符集支持、多部分发送（multi-part type）、权限（authorization）、缓存（cache）、内容编码（content encoding）等。</p>

<h3>2.2 请求格式</h3>

<p>下面是一个1.0版的HTTP请求的例子。</p>

<blockquote><pre><code class="language-http">
GET / HTTP/1.0
User-Agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10_10_5)
Accept: */*
</code></pre></blockquote>

<p>可以看到，这个格式与0.9版有很大变化。</p>

<p>第一行是请求命令，必须在尾部添加协议版本（<code>HTTP/1.0</code>）。后面就是多行头信息，描述客户端的情况。</p>

<h3>2.3 回应格式</h3>

<p>服务器的回应如下。</p>

<blockquote><pre><code class="language-http">
HTTP/1.0 200 OK 
Content-Type: text/plain
Content-Length: 137582
Expires: Thu, 05 Dec 1997 16:00:00 GMT
Last-Modified: Wed, 5 August 1996 15:55:28 GMT
Server: Apache 0.84

&lt;html>
  &lt;body>Hello World&lt;/body>
&lt;/html>
</code></pre></blockquote>

<p>回应的格式是"头信息 + 一个空行（<code>\r\n</code>） + 数据"。其中，第一行是"协议版本 + 状态码（status code） + 状态描述"。</p>

<h3>2.4 Content-Type 字段</h3>

<p>关于字符的编码，1.0版规定，头信息必须是 ASCII 码，后面的数据可以是任何格式。因此，服务器回应的时候，必须告诉客户端，数据是什么格式，这就是<code>Content-Type</code>字段的作用。</p>

<p>下面是一些常见的<code>Content-Type</code>字段的值。</p>

<blockquote>
  <ul>
<li>text/plain</li>
<li>text/html</li>
<li>text/css</li>
<li>image/jpeg</li>
<li>image/png</li>
<li>image/svg+xml</li>
<li>audio/mp4</li>
<li>video/mp4</li>
<li>application/javascript</li>
<li>application/pdf</li>
<li>application/zip</li>
<li>application/atom+xml</li>
</ul>
</blockquote>

<p>这些数据类型总称为<code>MIME type</code>，每个值包括一级类型和二级类型，之间用斜杠分隔。</p>

<p>除了预定义的类型，厂商也可以自定义类型。</p>

<blockquote><pre><code class="language-http">
application/vnd.debian.binary-package
</code></pre></blockquote>

<p>上面的类型表明，发送的是Debian系统的二进制数据包。</p>

<p><code>MIME type</code>还可以在尾部使用分号，添加参数。</p>

<blockquote><pre><code class="language-http">
Content-Type: text/html; charset=utf-8
</code></pre></blockquote>

<p>上面的类型表明，发送的是网页，而且编码是UTF-8。</p>

<p>客户端请求的时候，可以使用<code>Accept</code>字段声明自己可以接受哪些数据格式。</p>

<blockquote><pre><code class="language-http">
Accept: */*
</code></pre></blockquote>

<p>上面代码中，客户端声明自己可以接受任何格式的数据。</p>

<p><code>MIME type</code>不仅用在HTTP协议，还可以用在其他地方，比如HTML网页。</p>

<blockquote><pre><code class="language-html">
&lt;meta http-equiv="Content-Type" content="text/html; charset=UTF-8" />
&lt;!-- 等同于 -->
&lt;meta charset="utf-8" /> 
</code></pre></blockquote>

<h3>2.5 Content-Encoding 字段</h3>

<p>由于发送的数据可以是任何格式，因此可以把数据压缩后再发送。<code>Content-Encoding</code>字段说明数据的压缩方法。</p>

<blockquote><pre><code class="language-http">
Content-Encoding: gzip
Content-Encoding: compress
Content-Encoding: deflate
</code></pre></blockquote>

<p>客户端在请求时，用<code>Accept-Encoding</code>字段说明自己可以接受哪些压缩方法。</p>

<blockquote><pre><code class="language-http">
Accept-Encoding: gzip, deflate
</code></pre></blockquote>

<h3>2.6 缺点</h3>

<p>HTTP/1.0 版的主要缺点是，每个TCP连接只能发送一个请求。发送数据完毕，连接就关闭，如果还要请求其他资源，就必须再新建一个连接。</p>

<p>TCP连接的新建成本很高，因为需要客户端和服务器三次握手，并且开始时发送速率较慢（slow start）。所以，HTTP 1.0版本的性能比较差。随着网页加载的外部资源越来越多，这个问题就愈发突出了。</p>

<p>为了解决这个问题，有些浏览器在请求时，用了一个非标准的<code>Connection</code>字段。</p>

<blockquote><pre><code class="language-http">
Connection: keep-alive
</code></pre></blockquote>

<p>这个字段要求服务器不要关闭TCP连接，以便其他请求复用。服务器同样回应这个字段。</p>

<blockquote><pre><code class="language-http">
Connection: keep-alive
</code></pre></blockquote>

<p>一个可以复用的TCP连接就建立了，直到客户端或服务器主动关闭连接。但是，这不是标准字段，不同实现的行为可能不一致，因此不是根本的解决办法。</p>

<h2>三、HTTP/1.1</h2>

<p>1997年1月，HTTP/1.1 版本发布，只比 1.0 版本晚了半年。它进一步完善了 HTTP 协议，一直用到了20年后的今天，直到现在还是最流行的版本。</p>

<h3>3.1 持久连接</h3>

<p>1.1 版的最大变化，就是引入了持久连接（persistent connection），即TCP连接默认不关闭，可以被多个请求复用，不用声明<code>Connection: keep-alive</code>。</p>

<p>客户端和服务器发现对方一段时间没有活动，就可以主动关闭连接。不过，规范的做法是，客户端在最后一个请求时，发送<code>Connection: close</code>，明确要求服务器关闭TCP连接。</p>

<blockquote><pre><code class="language-http">
Connection: close
</code></pre></blockquote>

<p>目前，对于同一个域名，大多数浏览器允许同时建立6个持久连接。</p>

<h3>3.2 管道机制</h3>

<p>1.1 版还引入了管道机制（pipelining），即在同一个TCP连接里面，客户端可以同时发送多个请求。这样就进一步改进了HTTP协议的效率。</p>

<p>举例来说，客户端需要请求两个资源。以前的做法是，在同一个TCP连接里面，先发送A请求，然后等待服务器做出回应，收到后再发出B请求。管道机制则是允许浏览器同时发出A请求和B请求，但是服务器还是按照顺序，先回应A请求，完成后再回应B请求。</p>

<h3>3.3 Content-Length 字段</h3>

<p>一个TCP连接现在可以传送多个回应，势必就要有一种机制，区分数据包是属于哪一个回应的。这就是<code>Content-length</code>字段的作用，声明本次回应的数据长度。</p>

<blockquote><pre><code class="language-http">
Content-Length: 3495
</code></pre></blockquote>

<p>上面代码告诉浏览器，本次回应的长度是3495个字节，后面的字节就属于下一个回应了。</p>

<p>在1.0版中，<code>Content-Length</code>字段不是必需的，因为浏览器发现服务器关闭了TCP连接，就表明收到的数据包已经全了。</p>

<h3>3.4 分块传输编码</h3>

<p>使用<code>Content-Length</code>字段的前提条件是，服务器发送回应之前，必须知道回应的数据长度。</p>

<p>对于一些很耗时的动态操作来说，这意味着，服务器要等到所有操作完成，才能发送数据，显然这样的效率不高。更好的处理方法是，产生一块数据，就发送一块，采用"流模式"（stream）取代"缓存模式"（buffer）。</p>

<p>因此，1.1版规定可以不使用<code>Content-Length</code>字段，而使用（chunked transfer encoding）。只要请求或回应的头信息有<code>Transfer-Encoding</code>字段，就表明回应将由数量未定的数据块组成。</p>

<blockquote><pre><code class="language-http">
Transfer-Encoding: chunked
</code></pre></blockquote>

<p>每个非空的数据块之前，会有一个16进制的数值，表示这个块的长度。最后是一个大小为0的块，就表示本次回应的数据发送完了。下面是一个例子。</p>

<blockquote><pre><code class="language-http">
HTTP/1.1 200 OK
Content-Type: text/plain
Transfer-Encoding: chunked

25
This is the data in the first chunk

1C
and this is the second one

3
con

8
sequence

0

</code></pre></blockquote>

<h3>3.5 其他功能</h3>

<p>1.1版还新增了许多动词方法：<code>PUT</code>、<code>PATCH</code>、<code>HEAD</code>、 <code>OPTIONS</code>、<code>DELETE</code>。</p>

<p>另外，客户端请求的头信息新增了<code>Host</code>字段，用来指定服务器的域名。</p>

<blockquote><pre><code class="language-http">
Host: www.example.com
</code></pre></blockquote>

<p>有了<code>Host</code>字段，就可以将请求发往同一台服务器上的不同网站，为虚拟主机的兴起打下了基础。</p>

<h3>3.6 缺点</h3>

<p>虽然1.1版允许复用TCP连接，但是同一个TCP连接里面，所有的数据通信是按次序进行的。服务器只有处理完一个回应，才会进行下一个回应。要是前面的回应特别慢，后面就会有许多请求排队等着。这称为（Head-of-line blocking）。</p>

<p>为了避免这个问题，只有两种方法：一是减少请求数，二是同时多开持久连接。这导致了很多的网页优化技巧，比如合并脚本和样式表、将图片嵌入CSS代码、域名分片（domain sharding）等等。如果HTTP协议设计得更好一些，这些额外的工作是可以避免的。</p>

<h2>四、SPDY 协议</h2>

<p>2009年，谷歌公开了自行研发的 SPDY 协议，主要解决 HTTP/1.1 效率不高的问题。 </p>

<p>这个协议在Chrome浏览器上证明可行以后，就被当作 HTTP/2 的基础，主要特性都在 HTTP/2 之中得到继承。</p>

<h2>五、HTTP/2</h2>

<p>2015年，HTTP/2 发布。它不叫 HTTP/2.0，是因为标准委员会不打算再发布子版本了，下一个新版本将是 HTTP/3。</p>

<h3>5.1 二进制协议</h3>

<p>HTTP/1.1 版的头信息肯定是文本（ASCII编码），数据体可以是文本，也可以是二进制。HTTP/2 则是一个彻底的二进制协议，头信息和数据体都是二进制，并且统称为"帧"（frame）：头信息帧和数据帧。</p>

<p>二进制协议的一个好处是，可以定义额外的帧。HTTP/2 定义了近十种帧，为将来的高级应用打好了基础。如果使用文本实现这种功能，解析数据将会变得非常麻烦，二进制解析则方便得多。</p>

<h3>5.2 多工</h3>

<p>HTTP/2 复用TCP连接，在一个连接里，客户端和浏览器都可以同时发送多个请求或回应，而且不用按照顺序一一对应，这样就避免了"队头堵塞"。</p>

<p>举例来说，在一个TCP连接里面，服务器同时收到了A请求和B请求，于是先回应A请求，结果发现处理过程非常耗时，于是就发送A请求已经处理好的部分， 接着回应B请求，完成后，再发送A请求剩下的部分。</p>

<p>这样双向的、实时的通信，就叫做多工（Multiplexing）。</p>

<h3>5.3 数据流</h3>

<p>因为 HTTP/2 的数据包是不按顺序发送的，同一个连接里面连续的数据包，可能属于不同的回应。因此，必须要对数据包做标记，指出它属于哪个回应。</p>

<p>HTTP/2 将每个请求或回应的所有数据包，称为一个数据流（stream）。每个数据流都有一个独一无二的编号。数据包发送的时候，都必须标记数据流ID，用来区分它属于哪个数据流。另外还规定，客户端发出的数据流，ID一律为奇数，服务器发出的，ID为偶数。</p>

<p>数据流发送到一半的时候，客户端和服务器都可以发送信号（<code>RST_STREAM</code>帧），取消这个数据流。1.1版取消数据流的唯一方法，就是关闭TCP连接。这就是说，HTTP/2 可以取消某一次请求，同时保证TCP连接还打开着，可以被其他请求使用。</p>

<p>客户端还可以指定数据流的优先级。优先级越高，服务器就会越早回应。</p>

<h3>5.4 头信息压缩</h3>

<p>HTTP 协议不带有状态，每次请求都必须附上所有信息。所以，请求的很多字段都是重复的，比如<code>Cookie</code>和<code>User Agent</code>，一模一样的内容，每次请求都必须附带，这会浪费很多带宽，也影响速度。</p>

<p>HTTP/2 对这一点做了优化，引入了头信息压缩机制（header compression）。一方面，头信息使用<code>gzip</code>或<code>compress</code>压缩后再发送；另一方面，客户端和服务器同时维护一张头信息表，所有字段都会存入这个表，生成一个索引号，以后就不发送同样字段了，只发送索引号，这样就提高速度了。</p>

<h3>5.5 服务器推送</h3>

<p>HTTP/2 允许服务器未经请求，主动向客户端发送资源，这叫做服务器推送（server push）。</p>

<p>常见场景是客户端请求一个网页，这个网页里面包含很多静态资源。正常情况下，客户端必须收到网页后，解析HTML源码，发现有静态资源，再发出静态资源请求。其实，服务器可以预期到客户端请求网页后，很可能会再请求静态资源，所以就主动把这些静态资源随着网页一起发给客户端了。</p>

<h3>六、参考链接</h3>

<ul>
<li>, by Kamran Ahmed</li>
<li>, by Wikipedia</li>
<li></li>
<li></li>
</ul>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2016-08-19T09:46:33+08:00">2016年8月19日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>购买文集：</li>
<li>社交媒体：</li>
<li>Feed订阅： </li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------
<h1 id="#title_13" >14、那些无用的人----《人类简史》读后感</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2016/08/useless-people.html](http://www.ruanyifeng.com/blog/2016/08/useless-people.html)
<p>（说明：本文原载2016年第32期。）</p>

        <p>1.</p>

<p>最近，我读完了《人类简史》（中信出版社，2014）。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2016/bg2016081601.jpg" alt="" title="" /></p>

<p>它是以色列学者尤瓦尔·赫拉利写的畅销书，主要讲人类这个物种（即）的历史。全书最大特点就是，作者完全用自己的想法解释历史，有大量的独特观点。它不是学术著作，而是表达个人的历史观。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2016/bg2016081602.jpg" alt="" title="" /></p>

<p>最惊人的一个观点，大概是他对人类的前途相当悲观，认为人类可能即将灭绝。</p>

<p>2.</p>

<p>全书最后一章的标题，叫做《智人末日》。</p>

<p>作者感叹道，人类社会存在了七万年，真正的大发展只是最近两三百年。但是，再过一千年，人类是否还会存在，已经很可疑了。 </p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2016/bg2016081603.jpg" alt="" title="" /></p>

<blockquote>
  <p>"今天，人类正在让许多物种灭绝，甚至可能包括自己。如果今天发生核灾而让世界末日降临，人类将毁灭，而老鼠和蟑螂很可能继续生存下去。或许6500万年后，会有一群高智商的老鼠心怀感激地回顾人类造成的这场灾难。"</p>

<p>我们还有多久时间？没有人真正知道。如果智人的历史确实即将谢幕，我们这些最后一代的智人，或许该花点时间回答最后一个问题：我们究竟想要变成什么？"</p>
</blockquote>

<p>3.</p>

<p>尤瓦尔·赫拉利认为，人类可能灭绝的根本原因，在于技术的高速发展。</p>

<p>技术带来了现代化生活，也导致了前所未有的危机。别的不说，眼下的危机就是，<strong>短期内就会有大量失业出现，许多人将变得毫无用处</strong>。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2016/bg2016081604.jpg" alt="" title="" /></p>

<blockquote>
  <p>"技术造成的人力精简，将在今后5年内，导致全球发达国家失去710万个工作岗位，但在科技、专业服务及媒体领域，将创造210万个工作岗位。两相抵销之下，未来五年内，将会净损失500万个工作岗位，其中以行政工作与白领阶级为主。"</p>

<p>---- 摘自世界经济论坛，2016 </p>
</blockquote>

<p>上一次的工业革命，体力劳动被替代了，比如，水车替代了拉磨，汽车替代了马车。这一次的信息技术革命，智力劳动将被替代，计算机替代我们做计算和判断。</p>

<p>体力岗位没了，人类可以从事智力岗位。可是，智力岗位也没了，人类去干什么呢？</p>

<p>4.</p>

<p>今年5月，美国达拉斯发生，一名狙击手放冷枪，打死了5个警察。最后，他被包围在一片建筑群里面，但不知道他的确切位置。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2016/bg2016081605.jpg" alt="" title="" /></p>

<p>警方就派出一个，在建筑群里巡查，一发现目标，就扔出一颗炸弹，一下子就把罪犯炸死了。整个行动高效、快速，警方没有任何流血。更重要的是，这是历史上第一次，机器人警察杀死人类。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2016/bg2016081606.jpg" alt="" title="" /></p>

<p>可以想象，随着犯罪行为的增加，以及罪犯装备的升级，机器人警察将会得到推广，取代人类警察打击犯罪。人类士兵也会被取代，以后的战争就是机器人战争。</p>

<p>《人类简史》作者的说：</p>

<blockquote>
  <p>"未来可能不再需要司机。我们已经有了无人驾驶的汽车。他们不喝酒，不疲惫，比人类驾驶还要安全。当所有的汽车都变成了无人驾驶，我们就可以把所有的车辆联网，形成一个车联网。这样的话，交警可能也不需要了，因为所有的车都可以通过这张网络获取道路信息。"</p>
</blockquote>

<p>无人驾驶不仅会让司机和交警失业，而且长远来看，会消灭整个运输物流行业的工作岗位。比如，既然车辆可以自动到达目的地，那么送货的快递小哥也不需要了。</p>

<p>5.</p>

<p>人的价值体现在他/她的工作成果。如果有些人根本找不到工作，他们的价值体现在哪里呢？</p>

<p>过去，工业革命吸收了农业释放的数十亿人力，将人类的劳动形态从田野和作坊，变成了工厂和办公室；现在，工厂和办公室开始释放人力，又有什么行业可以吸收他们呢？</p>

<p><strong>将来越来越多的人会发现，他们根本不可能找到工作</strong>。智力和体力两方面，机器都比人类能干。你要么比机器更能干，要么比机器更便宜，否则你怎么跟机器竞争工作岗位呢？</p>

<p>6.</p>

<p>有人说，技术会创造新工作，只要不断学习新的技能，就不用担心自己会被淘汰。这对一部人也许可以，但对大部分人这样要求是不现实的。</p>

<blockquote>
  <p>"（世界经济论坛统计，目前的小学生长大后，65%会从事现在还不存在的工作。）孩子们在中学或者大学学到的大多数东西，等到40、50岁的时候可能都会变得无足轻重。如果他们还希望继续保住工作，那就得不断地改造自己，而且频率得越来越快才行。"</p>
</blockquote>

<p>不是每个人都善于学习，更不是每个人都具有学习的意愿。大多数人只希望生活舒适，不愿意动脑筋，去搞懂那些抽象的公式。而且，要求40、50岁的人跟刚走上社会的年轻人一样拼搏，也不现实。<strong>如果终生学习是唯一的就业出路，那对于多数人来说，就是没有出路。</strong></p>

<p>7.</p>

<p>尤瓦尔·赫拉利说，人工智能取代了那些简单技能的工作岗位以后，人类当中会出现一个庞大的、无用的无产阶级。</p>

<blockquote>
  <p>"未来，人类可能会分化为两个主要的等级：一个全新的更先进的精英阶级，很聪明，很富有，有更好的基因和更长的寿命；还有一个全新的一无用处的无产阶级，他们将越来越穷地等待死亡，可能变成没有工作、没有目标、整日靠吸毒度日、戴着VR头盔消磨时光的乌合之众。"</p>
</blockquote>

<p>人类社会的政治和经济结构，都会因此被颠覆。</p>

<p>当代国家建立在人对国家有用的基础上的，大部分人的角色是工人和士兵。如果这些角色被机器取代，那么底层的人们对国家来说，也就不再重要了。国家很可能会忽视他们的需求，只是出于社会稳定的目的，提供基本的生活资料。而人们也比以往更依赖政府，因为如果政府停止救济，他们就无法养活自己。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2016/useless01.jpg" alt="" title="" /></p>

<p>尤瓦尔·赫拉利将这种情景，列为21世纪最悲惨的威胁之一。</p>

<blockquote>
  <p>"随着人工智能变得越来越聪明，会有更多的人被挤出就业市场。没人知道大学该学什么，因为没人知道20岁的时候学的东西到了40岁还有没有用。等你知道的时候，已经有数十亿人变得一点用都没有了。这不是偶然，而是必然。"</p>
</blockquote>

<p>（全文完）</p>

<hr />

<p></p>

<p>下面是推广时间。</p>

<p>最近，上线了。它是一个在线学习平台，如果你希望进入互联网行业、系统学习前端技术，那么我推荐你去看一下。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2016/su_apeclass05.jpg" alt="" title="" /></p>

<p>海棠学院目前提供600课时的前端视频课程，由浅入深、系统讲解各种知识点，每堂课都有课后练习题，保证不同水平的学员都能学会。来自百度，有七年开发经验，主导过多个流量过亿的项目。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2016/su_apeclass06.jpg" alt="" title="" /></p>

<p>如果你每天投入两个小时，一周五天，那么大概四个月时间，就可以从零开始，学完所有课程，掌握前端开发技术。</p>

<p>为了保证学习效果，海棠学院采取多种措施。</p>

<ul>
<li><strong>重视实战。</strong>讲课内容和课后作业，紧贴实际业务，并且还有直播课，引导大家现场完成练习。</li>
<li><strong>重视答疑。</strong>如果你遇到疑问，可以随时向线上助教求助，也可以把问题提交到QQ群和微信群。</li>
<li><strong>强调纪律。</strong>为了保证学员不会半途而废，按时完成进度，每堂课都会线上考勤，并且强制交作业，还会有期中考试。</li>
</ul>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2016/su_apeclass07.jpg" alt="" title="" /></p>

<p>任何疑问或咨询，可以加创始人微信，直接提问。</p>

<p>当然，最重要的还是课程质量，欢迎，现在就开始试听。​​</p>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2016-08-16T08:46:13+08:00">2016年8月16日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>购买文集：</li>
<li>社交媒体：</li>
<li>Feed订阅： </li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------
<h1 id="#title_14" >15、布尔代数入门</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2016/08/boolean-algebra.html](http://www.ruanyifeng.com/blog/2016/08/boolean-algebra.html)
<p>是计算机的基础。没有它，就不会有计算机。</p>

        <p>布尔代数发展到今天，已经非常抽象，但是它的核心思想很简单。本文帮助你理解布尔代数，以及为什么它促成了计算机的诞生。  </p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2016/bg2016080505.jpg" alt="" title="" /></p>

<p>我依据的是《编码的奥妙》的第十章。这是一本好书，强烈推荐。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2016/bg2016080501.jpg" alt="" title="" /></p>

<h2>一、数理逻辑的起源</h2>

<p>19世纪早期，英国数学家乔治·布尔（George Boole，1815－1864）突发奇想：人的思想能不能用数学表达？</p>

<p>此前，数学只用于计算，没有人意识到，数学还能表达人的逻辑思维。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2016/bg2016080502.jpg" alt="" title="" /></p>

<p>两千年来，哲学书都是用文字写的。比如，最著名的三段论：</p>

<blockquote>
  <p>所有人都是要死的， <br />
苏格拉底是人， <br />
 所以，苏格拉底是要死的。</p>
</blockquote>

<p>乔治·布尔认为，这种推理可以用数学表达，也就是说，哲学书完全可以用数学写。这就是数理逻辑的起源。</p>

<h2>二、集合论</h2>

<p>乔治·布尔发明的工具，叫做"集合论"（Set theory）。他认为，逻辑思维的基础是一个个集合（Set），每一个命题表达的都是集合之间的关系。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2016/bg2016080503.jpg" alt="" title="" /></p>

<p>比如，所有人类组成一个集合<code>R</code>，所有会死的东西组成一个集合<code>D</code>。</p>

<blockquote>
  <p>所有人都是要死的</p>
</blockquote>

<p>集合论的写法就是：</p>

<blockquote>
  <p>R X D = R</p>
</blockquote>

<p>集合之间最基本的关系是并集和交集。乘号（<code>X</code>）表示交集，加号（<code>+</code>）表示并集。上面这个式子的意思是，<code>R</code>与<code>D</code>的交集就是<code>R</code>。</p>

<p>同样的，苏格拉底也是一个集合<code>S</code>，这个集合里面只有苏格拉底一个成员。</p>

<blockquote>
  <p>苏格拉底是人 <br />
// 等同于 <br />
S X R = S</p>
</blockquote>

<p>上面式子的意思是，苏格拉底与人类的交集，就是苏格拉底。</p>

<p>将第一个式子代入第二个式子，就得到了结论。</p>

<blockquote>
  <p>S X (R X D) <br />
= (S X R) X D <br />
= S X D <br />
= S</p>
</blockquote>

<p>这个式子的意思是，苏格拉底与会死的东西的交集，就是苏格拉底，即苏格拉底也属于会死的东西。</p>

<h2>三、集合的运算法则</h2>

<p>前面的三段论比较容易，一眼就能看出结论。但是，有些三段轮比较复杂，不容易立即反应过来。</p>

<p>请看下面这两句话。</p>

<blockquote>
  <p>"鸭嘴兽是卵生的哺乳动物。鸭嘴兽是澳洲的动物。"</p>
</blockquote>

<p>你能一眼得到结论吗？</p>

<blockquote>
  <p>鸭嘴兽 X 卵生 = 鸭嘴兽 <br />
鸭嘴兽 x 澳洲 = 鸭嘴兽</p>
</blockquote>

<p>将第一个式子代入第二个，就会得到：</p>

<blockquote>
  <p>鸭嘴兽 X 卵生 x 澳洲 = 鸭嘴兽 <br />
// 相当于 <br />
卵生 x 澳洲 = 鸭嘴兽 + 其他</p>
</blockquote>

<p>因此，结论就是"有的卵生动物是澳洲的动物"，或者"有的澳洲的动物是卵生动物"。</p>

<p>还有更不直观的三段论。</p>

<blockquote>
  <p>"哲学家都是有逻辑头脑的，一个没有逻辑头脑的人总是很顽固。"</p>
</blockquote>

<p>请问结论是什么？</p>

<p>这道题会用到新的概念：全集和空集。集合<code>A</code>和所有不属于它的元素（记作<code>-A</code>）构成全集（<code>I</code>），这时<code>A</code>和<code>-A</code>的交集就是一个空集（<code>0</code>）。</p>

<blockquote>
  <p>A + (-A) = I <br />
A X (-A) = 0</p>
</blockquote>

<p>因此，有下面的公式。</p>

<blockquote>
  <p>B <br />
= B X I <br />
= B X (A + -A) <br />
= B X A + B X (-A) </p>
</blockquote>

<p>回到上面那道题。</p>

<blockquote>
  <p>哲学家 X 逻辑 = 哲学家 <br />
无逻辑 X 顽固 = 无逻辑</p>
</blockquote>

<p>根据第一个命题，可以得到下面的结论。</p>

<blockquote>
  <p>哲学家 X 无逻辑 <br />
= (哲学家 X 逻辑) X 无逻辑 <br />
= 哲学家 X (逻辑 X 无逻辑) <br />
= 哲学家  X 0 <br />
= 0</p>
</blockquote>

<p>即哲学家与没有逻辑的人的交集，是一个空集。</p>

<p>根据第二个命题，可以得到下面的结论。</p>

<blockquote>
  <p>无逻辑 X 顽固 <br />
= 无逻辑 X 顽固 X (哲学家 + 非哲学家) <br />
= 无逻辑 X 顽固 X 哲学家 + 无逻辑 X 顽固 X 非哲学家 <br />
=  0 X 顽固 + 无逻辑 X 顽固 X 非哲学家 <br />
= 无逻辑 X 顽固 X 非哲学家 <br />
= 无逻辑</p>
</blockquote>

<p>也就是说，最终的结论如下。</p>

<blockquote>
  <p>无逻辑 X 顽固 X 非哲学家 = 无逻辑 <br />
// 相当于 <br />
顽固 X 非哲学家 = 无逻辑 + 其他</p>
</blockquote>

<p>结论就是顽固的人与非哲学家之间有交集。通俗的表达就是：一些顽固的人，不是哲学家，或者一些不是哲学家的人，很顽固。</p>

<p>由此可见，集合论可以帮助我们得到直觉无法得到的结论，保证推理过程正确，比文字推导更可靠。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2016/bg2016080506.jpg" alt="" title="" /></p>

<h2>四、 集合论到布尔代数</h2>

<p>既然命题可以用集合论表达，那么逻辑推导无非就是一系列集合运算。</p>

<p>由于集合运算的结果还是集合，那么通过判断个体是否属于指定集合，就可以计算命题的真伪。</p>

<blockquote>
  <p>一名顾客走进宠物店，对店员说："我想要一只公猫，白色或黄色均可；或者一只母猫，除了白色，其他颜色均可；或者只要是黑猫，我也要。"</p>
</blockquote>

<p>这名顾客的要求用集合论表达，就是下面的式子。</p>

<blockquote>
  <p>公猫 X (白色 + 黄色) <br />
+ 母猫 X 非白色 <br />
+ 黑猫</p>
</blockquote>

<p>店员拿出一只灰色的公猫，请问是否满足要求？</p>

<p>布尔代数规定，个体属于某个集合用<code>1</code>表示，不属于就用<code>0</code>表示。 灰色的公猫属于公猫集合，就是<code>1</code>，不属于白色集合，就是<code>0</code>。</p>

<p>上面的表达式变成下面这样。</p>

<blockquote>
  <p>1 X (0 + 0) <br />
+ 0 X 1 <br />
+ 0 <br />
= 0</p>
</blockquote>

<p>因此，就得到结论，灰色的公猫不满足要求。</p>

<p>这就是布尔代数：计算命题真伪的数学方法。</p>

<h2>五、布尔代数的运算法则</h2>

<p>布尔代数的运算法则与集合论很像。</p>

<p>交集的运算法则如下。</p>

<blockquote>
  <p>1 X 1 = 1 <br />
1 X 0 = 0 <br />
0 X 0 = 0</p>
</blockquote>

<p>并集的运算法则如下。</p>

<blockquote>
  <p>1 + 1 = 1 <br />
1 + 0 = 1 <br />
0 + 0 = 0</p>
</blockquote>

<p>集合论可以描述逻辑推理过程，布尔代数可以判断某个命题是否符合这个过程。人类的推理和判断，因此就变成了数学运算。</p>

<p>20世纪初，英国科学家香农指出，布尔代数可以用来描述电路，或者说，电路可以模拟布尔代数。于是，人类的推理和判断，就可以用电路实现了。这就是计算机的实现基础。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2016/bg2016080504.gif" alt="" title="" /></p>

<h2>六、布尔代数的局限</h2>

<p>虽然布尔代数可以判断命题真伪，但是无法取代人类的理性思维。原因是它有一个局限。</p>

<p>它必须依据一个或几个已经明确知道真伪的命题，才能做出判断。比如，只有知道"所有人都会死"这个命题是真的，才能得出结论"苏格拉底会死"。</p>

<p>布尔代数只能保证推理过程正确，无法保证推理所依据的前提是否正确。如果前提是错的，正确的推理也会得到错误的结果。而前提的真伪要由科学实验和观察来决定，布尔代数无能为力。</p>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2016-08-05T08:17:04+08:00">2016年8月 5日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>购买文集：</li>
<li>社交媒体：</li>
<li>Feed订阅： </li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------
<h1 id="#title_15" >16、This week's JavaScript news, issue 307</h1>

[http://javascriptweekly.com/issues/307](http://javascriptweekly.com/issues/307)
<table border="0" width="100%" cellpadding="0" cellspacing="0" bgcolor="#ffffff" style="font-family: 'helvetica neue', helvetica, arial, sans-serif; font-size: 14px; line-height: 20px; color: #333"><tr><td align="center" valign="top">
<table border="0" width="670" cellpadding="0" cellspacing="0" class="container noarchive" style="border-collapse: collapse;"><tr><td style="padding-top: 6px; padding-bottom: 6px; font-size: 11px; text-align: center; color: #555; font-family: verdana, arial, sans-serif">
<span class="nomo">This week's JavaScript news</span> — 
</td></tr></table>
<table border="0" width="670" cellpadding="0" cellspacing="0" class="container" style="border-collapse: collapse">
<tr><td style="background-color: #f7df1e"><table width="100%" cellspacing="0" cellpadding="0" align="left"><tr><td align="left" class="block" style="padding: 6px 12px;">
<table align="left" width="50%" class="gowide"><tr><td><span style="line-height: 36px; font-size: 23px; color: #f7df1e; font-weight: bold; color: #323330">JavaScript Weekly</span></td></tr></table>
<table align="left" style="text-align: right" width="50%" class="gowide lonmo"><tr><td><span style="font-size: 14px; line-height: 36px; font-weight: normal; color: #323330">
Issue 307 — October 27, 2016
</span></td></tr></table>
</td></tr></table></td></tr>
<tr><td style="padding: 16px 12px 12px 12px" align="left">
<div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">Async functions allow you to write promise-based code as if it were synchronous but without blocking the main thread.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Jake Archibald
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">A to-the-point guide to setting up ES6, Babel, Gulp, ESLint, React, Redux, Webpack, Immutable, Mocha, Chai, Sinon, and Flow.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Jonathan Verrecchia
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">Based around V8 5.4 which has 98% coverage of ES6 features. 7.x will get the latest features first, with 6.9 being the new LTS version. Note that there are breaking features, such as  for more.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Node.js Foundation
</div>
<br clear="all" style="clear: both"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">Kendo UI delivers everything you need to build modern web applications under tight deadlines - from the must-haves Data Grids &amp; DropDowns to Spreadsheet &amp; Scheduler. Choose from 70+ UI components and combine them to create beautiful, responsive apps.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Progress
  <span style="background-color: #f7df1e; color: #ffffff; font-weight: normal; padding: 1px 5px 0px 5px;">Sponsor</span>
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">Moritz Kröger discusses his experiences of using Redux without React — the problems faced, the solutions attempted and lessons learned along the way.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Sitepoint
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">A new series of five , is available to check out now.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Nicolás Bevacqua
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">A fun, easily accessible tutorial walking through the bare basics of building a DBN (a design markup language) to SVG compiler.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Mariko Kosaka
</div>
<br clear="all" style="clear: both"><p style="color: #666666; font-size: 16px; font-weight: bold; margin-top: 8px; margin-bottom: 10px; text-transform: uppercase">Jobs <!-- a href="https://hired.com/?utm_source=newsletters&amp;utm_medium=petercooperpress&amp;utm_term=cat-tech-javascript&amp;utm_campaign=q2-16-jsweekly"><img src="http://s3.cooperpress.com.s3.amazonaws.com/hired1.png" valign="middle" align="right" alt="Supported by Hired.com" height="26"></a --></p>
<ul style="padding-left: 18px; margin-top: 10px; list-style-type: square">
<li style="color: #f7df1e; margin-bottom: 10px; font-size: 15px; line-height: 17px">
</span> <span style="color: #999999; font-weight: normal; font-size: 12px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Zalando SE</span>
</li>
<li style="color: #f7df1e; margin-bottom: 10px; font-size: 15px; line-height: 17px">
<span style="font-size: 12px; color: #666666">Slate is hiring an editor to lead its interactives team. Ideal candidates will be smart, funny, and energetic, and will bring a passion for both journalism and computer science.</span> <span style="color: #999999; font-weight: normal; font-size: 12px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Slate Magazine</span>
</li>
<li style="color: #f7df1e; margin-bottom: 10px; font-size: 15px; line-height: 17px">
<span style="font-size: 12px; color: #666666">Finding the right role can be daunting, but not on Hired. Get empowered to find the right role with multiple job offers and free personalized support.</span> <span style="color: #999999; font-weight: normal; font-size: 12px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Hired</span>
</li>
</ul>
<!-- p style="color: #333; font-size: 11px; font-weight: normal; margin-top: 0px; margin-bottom: 10px">Can't find the right job? Want companies to apply to <em>you?</em> </p --><p style="color: #666666; font-size: 16px; font-weight: bold; margin-top: 24px; margin-bottom: 10px; text-transform: uppercase">In brief</p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #00aadd; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">news</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">TechCrunch</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #00aadd; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">news</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif"></span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #990099; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">course</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">Use the same skills you use on the web to build cross-platform, native applications in JavaScript.</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Frontend Masters  <span style="background-color: #f7df1e; color: #ffffff; font-weight: normal; padding: 1px 5px 0px 5px;">Sponsor</span></span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Valerii Iatsko</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Alan B Smith</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Gosha Arinich</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">An in-depth look at what stateful and stateless components are.</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Todd Motto</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Lance Ball</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Todd Motto</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Wes Bos</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #cc00cc; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">video</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">Building a simple AI tool to find solutions to hard problems. <em>24 minutes</em></span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Nikolay Nemshilov</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #cc00cc; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">video</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">Testing and monitoring techniques to deliver and maintain a React + Redux app while being able to sleep without fear of everything breaking in the night. <em>29 minutes.</em></span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Emanuele Rampichini</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #AF7817; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">opinion</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">GitLab</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #bbbbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tools</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">Combining automated deployment, instant hosting and collaborative editing to get you coding with no setup.</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Fog Creek Software  <span style="background-color: #f7df1e; color: #ffffff; font-weight: normal; padding: 1px 5px 0px 5px;">Sponsor</span></span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #bbbbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tools</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">A JS app framework that runs on the JVM (Java Virtual Machine).</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Enonic</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #bbbbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tools</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Lunar Logic</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #00bbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">code</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Dollar Shave Club</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #00bbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">code</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Jeremy Wadhams</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #00bbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">code</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">Expand canvases or active Web page space across multiple devices placed next to each other.</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Paul Sonnentag</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #00bbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">code</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Bilibili</span></p>
</td></tr>
<tr><td bgcolor="#f4f4f4" style="font-family: verdana, helvetica, arial, sans-serif; text-align: left; padding-top: 12px; padding-left: 12px; padding-right: 12px; padding-bottom: 12px" class="noarchive">
<p style="line-height: 15px; font-size: 11px; margin-top: 0">Curated by .</p>
<p style="font-size: 13px"></p>
<p style="font-size: 11px; line-height: 15px">© Cooper Press Ltd. Office 30, Lincoln Way, Louth, LN11 0LS, UK</p>
</td></tr>
</table>
</td></tr></table>
---------------
<h1 id="#title_16" >17、This week's JavaScript news, issue 306</h1>

[http://javascriptweekly.com/issues/306](http://javascriptweekly.com/issues/306)
<table border="0" width="100%" cellpadding="0" cellspacing="0" bgcolor="#ffffff" style="font-family: 'helvetica neue', helvetica, arial, sans-serif; font-size: 14px; line-height: 20px; color: #333"><tr><td align="center" valign="top">
<table border="0" width="670" cellpadding="0" cellspacing="0" class="container noarchive" style="border-collapse: collapse;"><tr><td style="padding-top: 6px; padding-bottom: 6px; font-size: 11px; text-align: center; color: #555; font-family: verdana, arial, sans-serif">
<span class="nomo">This week's JavaScript news</span> — 
</td></tr></table>
<table border="0" width="670" cellpadding="0" cellspacing="0" class="container" style="border-collapse: collapse">
<tr><td style="background-color: #f7df1e"><table width="100%" cellspacing="0" cellpadding="0" align="left"><tr><td align="left" class="block" style="padding: 6px 12px;">
<table align="left" width="50%" class="gowide"><tr><td><span style="line-height: 36px; font-size: 23px; color: #f7df1e; font-weight: bold; color: #323330">JavaScript Weekly</span></td></tr></table>
<table align="left" style="text-align: right" width="50%" class="gowide lonmo"><tr><td><span style="font-size: 14px; line-height: 36px; font-weight: normal; color: #323330">
Issue 306 — October 20, 2016
</span></td></tr></table>
</td></tr></table></td></tr>
<tr><td style="padding: 16px 12px 12px 12px" align="left">
<div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">At OSCON last week, the jQuery Foundation announced its renaming to the  include ESLint, jQuery and Webpack.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
The New Stack
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">Dr. Axel explains another potential addition to JavaScript: . He also shows how you can use it now via Babel.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Dr. Axel Rauschmayer
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">Three major updates for Node this month, with v7 set to become the new ‘current’ release line, v6 transitioning to LTS, and v0.10 reaching its ‘end of life’ with no patches at all beyond October.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Node.js Foundation
</div>
<br clear="all" style="clear: both"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">Get the most from your favorite RDBMS with 3 Node HA, Daily Backup and Auto-scaling. See how easy it is to connect your Database, hassle-free.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Compose
  <span style="background-color: #f7df1e; color: #ffffff; font-weight: normal; padding: 1px 5px 0px 5px;">Sponsor</span>
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">No, it’s not the exponentiation operator, or <code>Array.prototype.includes()</code>, it’s that <code>"use strict"</code> can’t be used in functions with non-simple parameter lists.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Nicholas C. Zakas
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">Angular 2 presents two different methods for creating forms, template-driven (as used in Angular 1.x) or reactive. Todd digs into the latter.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Todd Motto
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">Is package manager fatigue soon to become a thing? Tim Severien summarizes everything you need to know and compares Yarn to io.js.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Sitepoint
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">Julian Motz takes a look at jQuery’s document.ready() method and shows a more vanilla JS approach.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Sitepoint
</div>
<br clear="all" style="clear: both"><p style="color: #666666; font-size: 16px; font-weight: bold; margin-top: 8px; margin-bottom: 10px; text-transform: uppercase">Jobs <!-- a href="https://hired.com/?utm_source=newsletters&amp;utm_medium=petercooperpress&amp;utm_term=cat-tech-javascript&amp;utm_campaign=q2-16-jsweekly"><img src="http://s3.cooperpress.com.s3.amazonaws.com/hired1.png" valign="middle" align="right" alt="Supported by Hired.com" height="26"></a --></p>
<ul style="padding-left: 18px; margin-top: 10px; list-style-type: square">
<li style="color: #f7df1e; margin-bottom: 10px; font-size: 15px; line-height: 17px">
<span style="font-size: 12px; color: #666666">Learn how to get your job listing in front of as many JavaScript developers as possible.</span> <span style="color: #999999; font-weight: normal; font-size: 12px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Cooper Press</span>
</li>
<li style="color: #f7df1e; margin-bottom: 10px; font-size: 15px; line-height: 17px">
<span style="font-size: 12px; color: #666666">Sick of pushy recruiters, and dead end interviews? Try Hired to hear from top tier companies, and only talk to relevant companies.</span> <span style="color: #999999; font-weight: normal; font-size: 12px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Hired</span>
</li>
</ul>
<!-- p style="color: #333; font-size: 11px; font-weight: normal; margin-top: 0px; margin-bottom: 10px">Can't find the right job? Want companies to apply to <em>you?</em> </p --><p style="color: #666666; font-size: 16px; font-weight: bold; margin-top: 24px; margin-bottom: 10px; text-transform: uppercase">In brief</p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #00aadd; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">news</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">JS Foundation</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #00aadd; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">news</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Gerard Sans</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #00aadd; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">news</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif"></span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #00aadd; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">news</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Facebook</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #00aadd; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">news</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">Martin Probst of Google notes that <em>“We believe this is likely a misunderstanding”</em>. Updates to follow.</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Mozilla</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #00aadd; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">news</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">Chrome Dev Summit 2016 will take place at the SFJAZZ Center in San Francisco, CA on November 10-11. Join Chrome VP Darin Fisher for two full days of announcements and talks from the Chrome team. Register now with code <code>JAVASCRIPTWEEKLY</code></span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Google Inc.  <span style="background-color: #f7df1e; color: #ffffff; font-weight: normal; padding: 1px 5px 0px 5px;">Sponsor</span></span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">David Tang</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Emil Ong</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">A very thorough tutorial.</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Wolk Software Engineering</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Dave Ceddia</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #6ca629; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">node</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Gergely Nemeth</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Mat Marquis</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Martino Fornasa</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Dudley Storey</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Christopher Pitt</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Ember Igniter</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Louis Zawadzki</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #cc00cc; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">video</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">Catch up now on all talks from Polymer Summit 2016.</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Google</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #AF7817; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">opinion</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Alex Moldovan</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #AF7817; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">opinion</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">And how ‘let’ solves a common JavaScript “gotcha”…</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Mark Brouch</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> tool for catching errors, even if they're minified. Plugins for React, Vue, &amp; Angular 1 or 2.</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Sentry  <span style="background-color: #f7df1e; color: #ffffff; font-weight: normal; padding: 1px 5px 0px 5px;">Sponsor</span></span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #00bbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">code</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Moin Uddin</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #00bbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">code</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">maxwellito</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"></span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">David Su</span></p>
</td></tr>
<tr><td bgcolor="#f4f4f4" style="font-family: verdana, helvetica, arial, sans-serif; text-align: left; padding-top: 12px; padding-left: 12px; padding-right: 12px; padding-bottom: 12px" class="noarchive">
<p style="line-height: 15px; font-size: 11px; margin-top: 0">Curated by .</p>
<p style="font-size: 13px"></p>
<p style="font-size: 11px; line-height: 15px">© Cooper Press Ltd. Office 30, Lincoln Way, Louth, LN11 0LS, UK</p>
</td></tr>
</table>
</td></tr></table>
---------------
<h1 id="#title_17" >18、Yarn - a new, super-speedy JS package manager from Facebook</h1>

[http://javascriptweekly.com/issues/305](http://javascriptweekly.com/issues/305)
<table border="0" width="100%" cellpadding="0" cellspacing="0" bgcolor="#ffffff" style="font-family: 'helvetica neue', helvetica, arial, sans-serif; font-size: 14px; line-height: 20px; color: #333"><tr><td align="center" valign="top">
<table border="0" width="670" cellpadding="0" cellspacing="0" class="container noarchive" style="border-collapse: collapse;"><tr><td style="padding-top: 6px; padding-bottom: 6px; font-size: 11px; text-align: center; color: #555; font-family: verdana, arial, sans-serif">
<span class="nomo">Pure JS OCR; Is jQuery still relevant?; Doubt over React's license</span> — 
</td></tr></table>
<table border="0" width="670" cellpadding="0" cellspacing="0" class="container" style="border-collapse: collapse">
<tr><td style="background-color: #f7df1e"><table width="100%" cellspacing="0" cellpadding="0" align="left"><tr><td align="left" class="block" style="padding: 6px 12px;">
<table align="left" width="50%" class="gowide"><tr><td><span style="line-height: 36px; font-size: 23px; color: #f7df1e; font-weight: bold; color: #323330">JavaScript Weekly</span></td></tr></table>
<table align="left" style="text-align: right" width="50%" class="gowide lonmo"><tr><td><span style="font-size: 14px; line-height: 36px; font-weight: normal; color: #323330">
Issue 305 — October 13, 2016
</span></td></tr></table>
</td></tr></table></td></tr>
<tr><td style="padding: 16px 12px 12px 12px" align="left">
<div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">A new way to install and manage your npm packages. The initial community response has been very positive, it’s 
</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Facebook Code
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">A pure JS port of the Tesseract OCR engine supporting over 60 languanges, automatic orientation, script detection, character bounding boxes and more. There’s a live demo right on the page.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Guillermo Webster and Kevin Kwok
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">A JavaScript implementation of the full HTML5 form validation and constraints API that replaces or polyfills the browser’s native methods.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Kinetiqa
</div>
<br clear="all" style="clear: both"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">Google’s Polymer Summit will feature two days of talks on Polymer, Web Components, Progressive Web Apps, and the future of the mobile web. All sessions will be livestreamed from  to learn more.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Google Inc.
  <span style="background-color: #f7df1e; color: #ffffff; font-weight: normal; padding: 1px 5px 0px 5px;">Sponsor</span>
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">The transcript of a chat between several experts discussing whether the jQuery project is still useful in modern web development.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Telerik Developer Network
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">Robert Pierce concludes React is not ‘open source.’ This spawned 
</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
El Camino Legal LLP
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">Todd Motto explains the strategies that you can use on existing Angular 1.x codebases to get them into shape for future Angular 2 refactoring.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Todd Motto
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">A look at the work behind reducing the memory consumed by V8’s parser and its compilers.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Michael Hablich
</div>
<br clear="all" style="clear: both"><p style="color: #666666; font-size: 16px; font-weight: bold; margin-top: 8px; margin-bottom: 10px; text-transform: uppercase">Jobs </p>
<ul style="padding-left: 18px; margin-top: 10px; list-style-type: square">
<li style="color: #f7df1e; margin-bottom: 10px; font-size: 15px; line-height: 17px">
<span style="font-size: 12px; color: #666666">Geckoboard is a successful and growing 30-person startup based in East London looking for curious and creative problem solvers to help create beautiful UIs with React and ES6.</span> <span style="color: #999999; font-weight: normal; font-size: 12px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Geckoboard</span>
</li>
<li style="color: #f7df1e; margin-bottom: 10px; font-size: 15px; line-height: 17px">
<span style="font-size: 12px; color: #666666">Econify is a software development shop that primarily works with established companies, leading them through complicated technology challenges. We’re currently seeking a senior Node.js developer. Elixir knowledge a plus.</span> <span style="color: #999999; font-weight: normal; font-size: 12px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Econify</span>
</li>
<li style="color: #f7df1e; margin-bottom: 10px; font-size: 15px; line-height: 17px">
<span style="font-size: 12px; color: #666666">You're on the cutting edge of technology, why job hunt like it's the 90s? Try Hired today and have 4,000+ top companies apply for the chance to interview you.</span> <span style="color: #999999; font-weight: normal; font-size: 12px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Hired</span>
</li>
</ul>
<!-- p style="color: #333; font-size: 11px; font-weight: normal; margin-top: 0px; margin-bottom: 10px">Can't find the right job? Want companies to apply to <em>you?</em> </p --><p style="color: #666666; font-size: 16px; font-weight: bold; margin-top: 24px; margin-bottom: 10px; text-transform: uppercase">In brief</p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #00aadd; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">news</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">The best city to be a techie is Seattle, WA with an average individual salary $36,121 above household median.</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Swizec Teller  <span style="background-color: #f7df1e; color: #ffffff; font-weight: normal; padding: 1px 5px 0px 5px;">Sponsor</span></span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #00aadd; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">news</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px"><em>The Router now supports preloading of lazy loaded modules</em></span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Angular</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #00aadd; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">news</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">Chrome Dev Summit 2016 will take place in San Francisco, CA on Nov 10-11. Join Chrome VP Darin Fisher for two days of announcements and talks from the Chrome team. Register now with code <code>JAVASCRIPTWEEKLY</code></span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Google</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #990099; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">course</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">simplabs are offering Ember.JS workshops, ranging from 3 day Jumpstart events to advanced workshops which cover techniques like complex component architectures, FastBoot and Testing.</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">simplabs  <span style="background-color: #f7df1e; color: #ffffff; font-weight: normal; padding: 1px 5px 0px 5px;">Sponsor</span></span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Stephen Whitmore</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Hugo Di Francesco</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Gant Laborde</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">Updated this year for the latest React.</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Shusaku Uesugi</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Daniel Zen</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">JScrambler</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Jack Oliver and Sophia Shoemaker</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">How (and why) you can write JS with just six characters.</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Jasper Cashmore</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">David Walsh</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #cc00cc; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">video</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">An engineer at Slack demonstrates the tools Slack used to reduce friction in Electron development.</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Machisté Quintana</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"></span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Meth Meth Method</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #AF7817; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">opinion</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Tyler Church</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #AF7817; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">opinion</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Giles Bowkett</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #AF7817; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">opinion</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Yehuda Katz</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #AF7817; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">opinion</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Quincy Larson</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #00bbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">code</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Jade Allen Cook</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #00bbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">code</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Christian Alfoni</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #00bbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">code</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Simon Codrington</span></p>
</td></tr>
<tr><td bgcolor="#f4f4f4" style="font-family: verdana, helvetica, arial, sans-serif; text-align: left; padding-top: 12px; padding-left: 12px; padding-right: 12px; padding-bottom: 12px" class="noarchive">
<p style="line-height: 15px; font-size: 11px; margin-top: 0">Curated by .</p>
<p style="font-size: 13px"></p>
<p style="font-size: 11px; line-height: 15px">© Cooper Press Ltd. Office 30, Lincoln Way, Louth, LN11 0LS, UK</p>
</td></tr>
</table>
</td></tr></table>
---------------
<h1 id="#title_18" >19、State of JavaScript 2016 results, Vue 2.0 released, Angular 2 vs React comparison</h1>

[http://javascriptweekly.com/issues/304](http://javascriptweekly.com/issues/304)
<table border="0" width="100%" cellpadding="0" cellspacing="0" bgcolor="#ffffff" style="font-family: 'helvetica neue', helvetica, arial, sans-serif; font-size: 14px; line-height: 20px; color: #333"><tr><td align="center" valign="top">
<table border="0" width="670" cellpadding="0" cellspacing="0" class="container noarchive" style="border-collapse: collapse;"><tr><td style="padding-top: 6px; padding-bottom: 6px; font-size: 11px; text-align: center; color: #555; font-family: verdana, arial, sans-serif">
<span class="nomo">This week's JavaScript news</span> — 
</td></tr></table>
<table border="0" width="670" cellpadding="0" cellspacing="0" class="container" style="border-collapse: collapse">
<tr><td style="background-color: #f7df1e"><table width="100%" cellspacing="0" cellpadding="0" align="left"><tr><td align="left" class="block" style="padding: 6px 12px;">
<table align="left" width="50%" class="gowide"><tr><td><span style="line-height: 36px; font-size: 23px; color: #f7df1e; font-weight: bold; color: #323330">JavaScript Weekly</span></td></tr></table>
<table align="left" style="text-align: right" width="50%" class="gowide lonmo"><tr><td><span style="font-size: 14px; line-height: 36px; font-weight: normal; color: #323330">
Issue 304 — October  6, 2016
</span></td></tr></table>
</td></tr></table></td></tr>
<tr><td style="padding: 16px 12px 12px 12px" align="left">
<div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">The (very thorough) results from Sacha Greif’s (creator of ) ‘State of JavaScript’ survey. Over 9,000 of you took part and there’s lots to learn here.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Sacha Greif
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">After 8 alphas, 8 betas and 8 RCs, Vue 2.0 is ready for production. It’s a lot faster than before, and includes 
</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Evan You
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">The complexity of the JS ecosystem can sometimes prove overwhelming — here, Jose takes a <em>satirical</em> look at how varied the JS landscape is in 2016. This provoked .</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Jose Aguinaga
</div>
<br clear="all" style="clear: both"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">Most people are aware that Dev Tools exist.. to tweaking CSS or the interactive console. But there is so much more! Let’s look at every dev tools and learn to edit, debug and profile web applications!</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Frontend Masters
  <span style="background-color: #f7df1e; color: #ffffff; font-weight: normal; padding: 1px 5px 0px 5px;">Sponsor</span>
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">Dr. Axel looks at ‘global’, a proposal for a standard way to access the global object in JavaScript across all types of runtime.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Dr. Axel Rauschmayer
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">An in-depth comparison between Angular 2 and React.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Eric Elliott
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">A write-up of what’s going on with TC39 (the group working on specifying the latest versions of JavaScript) around ECMAScript Module support in Node. A great look at the issues involved.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
James M Snell
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">The tale of how a developer with an idea for a JavaScript data grid control turned it into an entire company. I hope this inspires some of you.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Niall Crosby
</div>
<br clear="all" style="clear: both"><p style="color: #666666; font-size: 16px; font-weight: bold; margin-top: 8px; margin-bottom: 10px; text-transform: uppercase">Jobs </p>
<ul style="padding-left: 18px; margin-top: 10px; list-style-type: square">
<li style="color: #f7df1e; margin-bottom: 10px; font-size: 15px; line-height: 17px">
<span style="font-size: 12px; color: #666666">Always wanted to work in a multicultural organisation with clients from all over the world? We travel, present and breathe JavaScript daily. Join us and help create the world's leading lean customer experience platform.</span> <span style="color: #999999; font-weight: normal; font-size: 12px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Backbase</span>
</li>
<li style="color: #f7df1e; margin-bottom: 10px; font-size: 15px; line-height: 17px">
<span style="font-size: 12px; color: #666666">Everyone should have the power to create professional-quality videos. As a member of the Animoto team, you'll be developing a responsive, elegant web experience and pioneering the next generation of video creation software.</span> <span style="color: #999999; font-weight: normal; font-size: 12px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Animoto</span>
</li>
<li style="color: #f7df1e; margin-bottom: 10px; font-size: 15px; line-height: 17px">
<span style="font-size: 12px; color: #666666">On Hired companies apply to interview you. Get 1:1 support for your job search plus upfront compensation details.</span> <span style="color: #999999; font-weight: normal; font-size: 12px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Hired</span>
</li>
</ul>
<!-- p style="color: #333; font-size: 11px; font-weight: normal; margin-top: 0px; margin-bottom: 10px">Can't find the right job? Want companies to apply to <em>you?</em> </p --><p style="color: #666666; font-size: 16px; font-weight: bold; margin-top: 24px; margin-bottom: 10px; text-transform: uppercase">In brief</p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #00aadd; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">news</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Mat Marquis</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #00aadd; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">news</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">WebKit</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #00aadd; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">news</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Dr. Axel Rauschmayer</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #bbbbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">event</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">Featuring 2 days of talks on Polymer, Web Components, Progressive Web Apps, &amp; the future of the mobile web</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Google Inc.  <span style="background-color: #f7df1e; color: #ffffff; font-weight: normal; padding: 1px 5px 0px 5px;">Sponsor</span></span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #bbbbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">event</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">Registration for the Chrome Dev Summit is now open (San Francisco, Nov 10-11). Join Chrome VP Darin Fisher for two days of announcements and talks from the Chrome team.</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Google</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">How to load ES2015 modules synchronously (during the page load) and asynchronously (performing lazy-loading) using System.js.</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Tiago Garcia</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Dominik Kundel</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">This in-depth tutorial details how to write a Trello-like ticketing system from scratch.</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Codementor</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Eric Rozell</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Jordan Schaenzle</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">How to conditionally load polyfills while considering the balance of simplicity and performance.</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Philip Walton</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">Camilo Reyes believes that by applying some SOLID principles, callbacks can still be a useful technique.</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">SitePoint</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">How the new fetch API is a better replacement for XHR when fetching resources.</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Jared Faris</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Ire Aderinokun</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Frank Treacy</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #990099; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">course</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">Rangle offers this free Angular 2 online training program for JavaScript developers. Register now to join the session on October 18-19.</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">RANGLE.IO  <span style="background-color: #f7df1e; color: #ffffff; font-weight: normal; padding: 1px 5px 0px 5px;">Sponsor</span></span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #AF7817; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">opinion</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Martijn Walraven</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #bbbbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tools</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Node.js Foundation</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #bbbbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tools</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">eBay</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #00bbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">code</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif"></span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 12px; padding: 1px 3px; text-transform: uppercase; background-color: #00bbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">code</span><br><span style="color: #999999; font-weight: normal; font-size: 12px; line-height: 18px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Federica Sibella</span></p>
</td></tr>
<tr><td bgcolor="#f4f4f4" style="font-family: verdana, helvetica, arial, sans-serif; text-align: left; padding-top: 12px; padding-left: 12px; padding-right: 12px; padding-bottom: 12px" class="noarchive">
<p style="line-height: 15px; font-size: 11px; margin-top: 0">Curated by .</p>
<p style="font-size: 13px"></p>
<p style="font-size: 11px; line-height: 15px">© Cooper Press Ltd. Office 30, Lincoln Way, Louth, LN11 0LS, UK</p>
</td></tr>
</table>
</td></tr></table>
---------------
