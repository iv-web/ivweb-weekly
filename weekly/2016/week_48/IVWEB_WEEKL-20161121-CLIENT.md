## 文章索引
1、 <a href="#1android-android-从-0-开始自定义控件之-view-的滑动冲突详解四" >[Android] android 从 0 开始自定义控件之 View 的滑动冲突详解（四）</a><br/>
2、 <a href="#2android-java-数据结构与算法之改良顺序表与双链表类似-arraylist-和-linkedlist带-iterator-迭代器与-fast-fail-机制" >[Android]  java 数据结构与算法之改良顺序表与双链表类似 ArrayList 和 LinkedList（带 Iterator 迭代器与 fast-fail 机制）</a><br/>
3、 <a href="#3android-简述-rtmpdump-与编译移植" >[Android] 简述 RTMPDump 与编译移植</a><br/>
4、 <a href="#4文章-网易-android工程模板化实践" >文章： 网易 Android工程模板化实践</a><br/>
5、 <a href="#5后端-树莓派上的-docker-集群管理" >[后端] 树莓派上的 Docker 集群管理</a><br/>
6、 <a href="#6微服务与安全" >微服务与安全</a><br/>
7、 <a href="#7前端-前端开发之走进-vuejs" >[前端] 前端开发之走进 Vue.js</a><br/>
8、 <a href="#8前端-开源掘金微信小程序初探" >[前端] 开源：掘金微信小程序初探</a><br/>
9、 <a href="#9阅读-synproxy-工作原理" >[阅读] SynProxy 工作原理</a><br/>
10、 <a href="#10阅读-高德-api+python-解决租房问题---知乎专栏-·程序员实验室" >[阅读] 高德 API+Python 解决租房问题 - 知乎专栏 ·「程序员实验室」</a><br/>
11、 <a href="#11阅读-程序员必备技能在-github-pages-上部署自己的简历---知乎专栏-·程序员实验室" >[阅读] 程序员必备技能：在 Github Pages 上部署自己的简历 - 知乎专栏 ·「程序员实验室」</a><br/>
12、 <a href="#12译假新闻与-facebook" >【译】假新闻与 Facebook</a><br/>
13、 <a href="#13前端-在-vue-工作流中使用-css-modules" >[前端] 在 Vue 工作流中使用 CSS Modules</a><br/>
14、 <a href="#14从苏宁十年技术演进看架构意识转变的关键一步" >从苏宁十年技术演进，看架构意识转变的关键一步</a><br/>
15、 <a href="#15uber工程的deckgl框架下的web数据可视化集" >Uber工程的deck.gl框架下的Web数据可视化集</a><br/>
16、 <a href="#16不计前嫌握手言和microsoft宣布新版sql-server将同时支持windows与linux两大平台" >不计前嫌，握手言和：Microsoft宣布新版SQL Server将同时支持Windows与Linux两大平台</a><br/>
17、 <a href="#17连接12万+开发者揭秘网易场景化云服务背后的技术" >连接12万+开发者，揭秘网易场景化云服务背后的技术</a><br/>
18、 <a href="#18微软发布visual-studio-mac预览版" >微软发布Visual Studio Mac预览版</a><br/>
19、 <a href="#19算法时代的媒体" >算法时代的媒体</a><br/>
20、 <a href="#20视频演讲-平安金融云之caas服务建设和应用" >视频演讲： 平安金融云之CaaS服务建设和应用</a><br/>
21、 <a href="#21视频演讲-移动测试体系" >视频演讲： 移动测试体系</a><br/>
22、 <a href="#22文章-借助数据科学解决业务问题" >文章： 借助数据科学解决业务问题</a><br/>
23、 <a href="#23前端-干货-滴滴出行在小程序的实践" >[前端] [干货] 滴滴出行在小程序的实践</a><br/>
24、 <a href="#24文章-大数据杂谈微课堂-|-数据挖掘技术和房地产的有效结合" >文章： 大数据杂谈微课堂 | 数据挖掘技术和房地产的有效结合</a><br/>
25、 <a href="#25视频演讲-以应用为核心重走上云之路" >视频演讲： 以应用为核心，重走上云之路</a><br/><h1 id="#title_0" >1、[Android] android 从 0 开始自定义控件之 View 的滑动冲突详解（四）</h1>
Airsaid
[http://gold.xitu.io/entry/5831b80e2e958a0069dcb9d1](http://gold.xitu.io/entry/5831b80e2e958a0069dcb9d1)
<img src="http://ac-mhke0kuv.clouddn.com/6d631d99b32c3a9106e4.JPG?imageView/2/w/800/h/600/q/80/format/png"/><p>滑动冲突可以说每一个 Android 开发者都遇到过，虽然 Android 已经在如 ViewPager 这些控件内部处理了滑动冲突，但是在我们自己定义控件，或者一些复杂的布局情况下，依然要去解决滑动冲突的情况。 
这一篇文章总结了下滑动冲突出现的场景，以及其中的规则和解决方法。</p><p></p>
---------------
<h1 id="#title_1" >2、[Android]  java 数据结构与算法之改良顺序表与双链表类似 ArrayList 和 LinkedList（带 Iterator 迭代器与 fast-fail 机制）</h1>
shinezejian
[http://gold.xitu.io/entry/5832429f2e958a0069deb7b6](http://gold.xitu.io/entry/5832429f2e958a0069deb7b6)
<img src="http://ac-mhke0kuv.clouddn.com/448a09908e13ad6a5a28.png?imageView/2/w/800/h/600/q/80/format/png"/><p>这篇是数据结构与算法的第 3 篇，通过前两篇的介绍，对应顺序表和链表已有比较深入的了解，而本篇是前两篇的延续，即优化前面所分析过的顺序表和双向链表（带头结点和尾结点，均不带数据）。以下是主要的知识点：
理解 Iterator 接口
为什么需要迭代器 Iterator
迭代器 Iterator 的分析
迭代器 Iterator 的简单实现
迭代器 Iterator 与集合间存在的问题
理解快速失败机制 fast-fail 机制
进化版的 ListIterator 接口
改良的 MyArraryList 的实现
改良的 MyLinkedList 的实现</p><p></p>
---------------
<h1 id="#title_2" >3、[Android] 简述 RTMPDump 与编译移植</h1>
zhengxiaoyong
[http://gold.xitu.io/entry/5831a2e267f356006353ac10](http://gold.xitu.io/entry/5831a2e267f356006353ac10)
<p>RTMPDump 库主要包含三部分：

1、一个基本的客户端程序
2、两个服务器程序（rtmpsrv、rtmpsuck）
3、一个支持 rtmp 协议的库—librtmp</p><p></p>
---------------
<h1 id="#title_3" >4、文章： 网易 Android工程模板化实践</h1>
张云龙
[http://www.infoq.com/cn/articles/practice-of-netease-android-project-template?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/practice-of-netease-android-project-template?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/practice-of-netease-android-project-template/zh/smallimage/logo (8).jpg"/><p>我们网易前端技术部 - 移动技术组作为公司的移动端基础技术部门，主要为其他部门提供解决方案、技术支持和产品孵化。在几年的积累过程中，我们拥有一些自己的框架和 SDK，如轻应用框架、热更新 SDK、网络请求库、本地存储库、页面管理等，服务过网易新闻、云音乐、考拉、易信等亿级产品，先后孵化过青果摄像头、二次元Gacha、严选等重要产品。</p> <i>By 张云龙</i>
---------------
<h1 id="#title_4" >5、[后端] 树莓派上的 Docker 集群管理</h1>
Docker精选
[http://gold.xitu.io/entry/583237b02f301e00596fbd46](http://gold.xitu.io/entry/583237b02f301e00596fbd46)
<p>本文将致力于构建一个利用 Rancher&RancherOS 来管理运行在树莓派上的容器集群。</p><p></p>
---------------
<h1 id="#title_5" >6、微服务与安全</h1>
Jan Stenberg
[http://www.infoq.com/cn/news/2016/11/microservices-security?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2016/11/microservices-security?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>从安全角度看，微服务虽然降低了攻击者可以一次性获取全部信息的风险，但同时也暴露了更多的可攻击点和攻击方式。今年微服务大会的一个主题演讲对微服务中存在的安全问题进行了分析，演讲阐述了如何借助威胁建模、HTTPS、Docker和日志分析等手段来实现微服务中的安全和缺陷检测。</p> <i>By Jan Stenberg</i> <i> Translated by Rays</i>
---------------
<h1 id="#title_6" >7、[前端] 前端开发之走进 Vue.js</h1>
幸运儿
[http://gold.xitu.io/entry/5831af7c128fe10069763797](http://gold.xitu.io/entry/5831af7c128fe10069763797)
<p>前端开发之走进 Vue.js</p><p></p>
---------------
<h1 id="#title_7" >8、[前端] 开源：掘金微信小程序初探</h1>
kalasoo
[http://gold.xitu.io/entry/5831b58f0ce463006c08eee6](http://gold.xitu.io/entry/5831b58f0ce463006c08eee6)
<img src="http://ac-mhke0kuv.clouddn.com/d0304011c01e08a37ae6.png?imageView/2/w/800/h/600/q/80/format/png"/><p>我为了上海的线下活动准备了一个微信小程序的示例，做了掘金最近出的收藏集还有排行榜的样式，大家可以品玩一下</p><p></p>
---------------
<h1 id="#title_8" >9、[阅读] SynProxy 工作原理</h1>
hainuo
[http://gold.xitu.io/entry/58319cd38ac2470061bdd7d2](http://gold.xitu.io/entry/58319cd38ac2470061bdd7d2)
<p>非常不错的文章</p><p></p>
---------------
<h1 id="#title_9" >10、[阅读] 高德 API+Python 解决租房问题 - 知乎专栏 ·「程序员实验室」</h1>
幸运儿
[http://gold.xitu.io/entry/583199990ce463006c07dd19](http://gold.xitu.io/entry/583199990ce463006c07dd19)
<p>高德 API+Python 解决租房问题</p><p></p>
---------------
<h1 id="#title_10" >11、[阅读] 程序员必备技能：在 Github Pages 上部署自己的简历 - 知乎专栏 ·「程序员实验室」</h1>
幸运儿
[http://gold.xitu.io/entry/58319934a0bb9f0067c72df4](http://gold.xitu.io/entry/58319934a0bb9f0067c72df4)
<p>程序员必备技能：在 Github Pages 上部署自己的简历</p><p></p>
---------------
<h1 id="#title_11" >12、【译】假新闻与 Facebook</h1>

[https://www.h5jun.com/post/fake-news.html](https://www.h5jun.com/post/fake-news.html)
<blockquote>
<p>原文：</p>
</blockquote>
<p>在 2001 到 2003 年间，Judith Miller 在纽约时报上发表了一批文章，宣称伊拉克有能力和野心生产大规模杀伤性武器。这是假新闻。</p>
<p>回顾当年，我们无法确定 Miller 写的这些故事在美国 2013 年做出发动伊拉克战争的决定中扮演了怎样的角色；与 Miller 相同来源的消息与小布什政府的对外政策团队有很大关联。但是，纽约时报仍然起到了为这一政策背书的作用，尤其是对民主党人，本来他们应该会更坚定地反对小布什的政策。毕竟，纽约时报可不是一些无人问津的地方小报，它是整个美国影响力最大的报刊，它一般被认为具有左倾倾向。Miller 的故事某种程度上吻合报纸的政治倾向。</p>
<p>我们可以把 Miller 的错误和最近关于 Facebook 的假新闻问题联系起来看；Facebook 用自己的故事告诫我们“假新闻是坏的”。然而，我持有不同的观点：<strong>新闻假不假没那么重要，由谁来决定什么是新闻才是第一重要的</strong>。</p>
<!--more-->
<h4 id="facebook-">Facebook 的媒体商业化</h4>
<p>在，社交网络之所以兴起，是因为之前存在的线下社会网络在往线上网络转变。考虑到人类本质是社会化的，用户开始将时间花在 Facebook 上阅读、发表观点和获取新闻。</p>
<p>随后，Facebook 吸引了媒体、商业公司以及其他希望获得用户注意的公司进驻。这对于 Facebook 来说很棒：Facebook 提供越多的好内容给用户，用户就花越多的时间上 Facebook，Facebook 将广告展现给用户的机会就越多。而反过来，用户花越多时间上 Facebook，他们阅读其他资讯的时间就越少，这进一步加速了媒体（以及商业公司和其他公司）将内容搬到 Facebook 上，产生 Facebook 受欢迎的良性循环：通过获得用户，Facebook 吸引了内容供应商，内容供应商间接帮助 Facebook 进一步深化运营用户，增加的用户也带给内容供应商更多的收益。</p>
<p>这个过程让 Facebook 的内容供应商，即媒体公司，简化了它们的角色，成为纯粹的供货商。Facebook 根据内容的用户参与度计算出重要程度，让每个角色都各取所需：媒体公司获得了广告，Facebook 获得了分享，而用户从庞大的信息数据库中得到他们想看的内容。当然不是所有内容都能吸引所有用户；这就是算法要做的事情：给用户展现他们感兴趣的内容，不论是婴儿图片、征婚启示、喵星人图片、小测验还是政治新闻。根据 Facebook 的观点，或者坦白说，根据 Facebook 用户的观点，这些内容没什么区别。当然其中也包含有假新闻，顺便提一下：在 Facebook 看来，和其它内容一样，并没什么特别的，对于推荐算法来说，它们都是内容，仅根据参与程度影响它的推荐量。</p>
<h4 id="-">媒体和特朗普</h4>
<p>现在在媒体上有许多讨论，关于特朗普的当选。观点是如果媒体没有给特朗普 —— 基本上是媒体报道（而不是付费报道，那种是广告）—— 特朗普永远也当选不了，因此媒体要为特朗普的当选负责。这一看似合理的自我反思，让行业拒绝承认一个更令人不安的现实：如果他们不想要如此的话，媒体不可能做成这件该死的事。</p>
<p><strong>媒体广泛报道特朗普的理由非常简单：这是用户想看到的内容。在媒体商品化的今天，如果像以前那样有编辑特权来决定不报道潜在用户想要看到的内容，就得面对被用户打脸的现实，点击量下降是媒体所不愿承受的。</strong></p>
<p>事实上，假新闻大行其道也是因为同样的原因：因为用户喜闻乐见。这些网站获得流量，因为用户点击并分享它们的文章，因为用户想确认他们心中已经相信是真实的内容（尽管实际上是假的）。确认偏差（即人们更容易相信他们愿意相信的内容 —— 译者注）是一种毒品 —— 正如 Techcrunch 的记者 Kim-Mai Cutler ，这是一种商业模式的原罪。</p>
<h4 id="-facebook-">为什么 Facebook 应该删除假新闻</h4>
<p>所以现在我们回到关于如何处理假新闻的问题。也许 的观点最能代表一般大众的情绪：Facebook 应当消除假新闻以及取消给人们推荐他们心中已经认同的观点的新闻的倾向。Tufekci 写道：</p>
<blockquote>
<p>Mark Zuckerberg, Facebook 的老板，认为Facebook 的假新闻影响选举是个疯狂的想法，因为那些是非常少量的内容，对选举几乎没有影响。他的这种不过脑的坚持，认为他的公司对人们做出决定没有影响的行为，实际上已经对美国和全世界的民主带来了真正的损害……</p>
<p>Facebook 影响政治话语的问题的问题不仅限于传播假新闻。它还有回音室效应。它的推荐算法选择哪些资讯更新出现在用户阅读列表的前面以及哪些被顶到后面去。人类已经倾向于聚集在志同道合的人之中，寻找证实他们偏见的消息。Facebook 的研究显示这家公司的算法通过优先更新用户更愿意看到的内容而鼓励了这一行为。</p>
</blockquote>
<p>Tufekci 给 Facebook 提供了一些建议，包括与外部研究人员分享数据从而更好地理解错误消息如何传播，以及应该如何对付过虑气泡（即智能推荐算法根据你的兴趣推荐内容，像一个泡泡将你包裹起来，把你和其他未推荐内容隔离起来——译者注），以更积极地行动，消除假新闻，就像处理作弊和其他垃圾内容那样，还包括重新启用人类编辑以及重新调整算法来有利于新闻平衡而不是一味通过参与度来推荐。</p>
<h4 id="-facebook-">为什么 Facebook 不应该这么做</h4>
<p>从表面上看，这一切都很合理，但是实际上，Tufekci 的建议有点自以为是。</p>
<p>首先，Facebook 没有动机去做这些事；当时 Facebook ，Facebook 搁置了对新闻推荐算法的改变，这一改变本可能消除假消息，Facebook 的解释是如果那么做，会对右翼站点造成不公平的影响，事实上 Facebook 非常重视在各方观点中保持中立；其他任何行为都会导致用户流失，而这对社交网络来说是不能承受之重。</p>
<p>此外，除了聚焦于参与度之外，任何偏离这一准则的行为都一定会减少用户在 Facebook 上所花费的时间，而在这里 Tufekci 错误地认为这是可接受的，因为他完全没有考虑“竞争对手”。事实上，Facebook 在很长一段时间内处于被挑战的地位上：Snapchat 正在从 Facebook 最有价值的人群中获取关注，尽管新闻资讯的广告变现能力已经接近饱和，Snapchat 依然在最具有价值的科技消费领域威胁着 Facebook：那是以电视为中心的品牌广告领域。</p>
<p>而且，还有更根本的问题：你如何决定哪些新闻是假新闻？准则是什么？而也许最关键的是，谁来决定？认为一些假新闻存在于其他海量内容中，从而得对 Facebook 内容进行编辑并不仅是一个简单的后勤噩梦，而且，至少当涉及到潜在的不良后果时，这个问题远没有它表面上看来那么简单。</p>
<p>实际情况比过滤气泡问题要复杂得多：从指责 Facebook 通过参与度驱动的二阶效应来影响它的用户的信息流，到坚持由于政治原因让平台积极干预用户看到的内容，这两者之间存在巨大的鸿沟。这不是关于建设更好社会的目标和两党争斗的对立，毕竟，支持者认为他们的目标也是建设更好的社会。事实上，如果整个值得关注的点是，Facebook 在其用户的新闻消费中扮演的重要角色，那么更大的恐惧应该是如果坚持人工干预的话，如何防止有人积极地滥用干预者这一角色为自己的利益服务。</p>
<p>我明白为什么自上而下的解决方案是诱人的：假新闻和过滤气泡是摆在我们眼前的问题，如果让 Facebook 修复它们难道不是更好吗？问题是这得假设动用自上而下的权力来做这一切的某人会正好与我的观点相同。那么，如果他们不呢？只要看一下我们现在的政治处境：那些担心特朗普的人，也必须承认的一个事实是，行政部门的权力在过去几十年里已经急剧扩大；我们将巨大的责任和权力交到一个人手中，而忘记了<strong>权力和责任交出容易，收回难</strong>。</p>
<p>因此，如果 Facebook 真的开始主动干预新闻内容，我会更加担忧；正如我，我越来越担心 Zuckerberg 的乌托邦式的观点，要知道，从影响世界到控制世界只有一步之遥。正如政府监管有坏处：当谈到暴政的时候，我们最重要的自由是言论自由，而把一个官员 —— 向总统汇报的人 —— 置于负责监管人们所见内容的位置上，是与这种自由精神背道而驰的。</p>
<p>要牢记的关键一点是假新闻的实际影响是取决于谁传播它：当然，那些马其顿的新闻故事不好，但是它们起作用了，尽管不怎么好，有些人却愿意相信。对比 Miller 在纽约时报的故事：由于纽约时报具有公信力，许多人因此改变了他们的观点，导致了一场到今天影响还没能完全消除的灾难。考虑到这一点，让 Facebook 人工干预新闻结果的潜在风险几乎无法想象。</p>
<h4 id="-">自由和懒惰</h4>
<p>也许有一些折衷方案：对于有些明显是假的新闻来源，Facebook 可以简单地将它们拉黑，更理想的情况，Facebook 可以透明地给出它们做了什么，以及为什么被拉黑的理由。而更进一步，Facebook 在不损害其竞争地位的情况下，可以将部分数据共享给外部研究者，它应该这样做。Facebook 也应该提供更多的配置选项给用户来控制他们的信息流，如果希望避免过滤起泡，可以通过修改配置来做到。</p>
<p>其实，你和我都知道，很少有用户会困扰。而且，表面上看，让许多 Facebook 的批评者最困扰的是，他们觉得如果用户不寻求“正确的”新闻来源，那么，应该有人让他们看到。这听起来很伟大 —— 而且毫无问题，是赢得选举的一个更方便的解决方案，而不必实际做出必要的改变 —— 直到你想起来，你刚刚给了委托人如此大的权力，而他可能不同意你的意见，而人为控制人们所看到的内容是极权主义的标志。</p>
<p>让我总结一下：我很清楚 Facebook 的影响有一定的问题；我特别担心的是，我们为了偷懒，用部落的思路来解决这一问题，影响选举的部分原因是由于如上所述的过滤气泡效应所致（这是为什么 的原因之一）。但是解决办法不是在互联网添加人为把关；要解决这一问题必须要通过互联网的力量，而事实上，我们每一个人，如果我们想要，是可以获得比以前任何时候更多的信息和资源真相的。如果我们想要，我们也可以有更多的方法来接触、理解和说服那些与我们意见相左的人。是的，这比要求 Zuckerberg 改变人们看到的内容有更多的工作要做，但是<strong>因为懒惰而放弃自由从未有过好结果</strong>。</p>
<blockquote>
<p>英文原文：</p>
</blockquote>
---------------
<h1 id="#title_12" >13、[前端] 在 Vue 工作流中使用 CSS Modules</h1>
Zindex
[http://gold.xitu.io/entry/5831b901da2f6000630167fa](http://gold.xitu.io/entry/5831b901da2f6000630167fa)
<img src="http://ac-mhke0kuv.clouddn.com/0b5cc330bc5fc3e05f5e.png?imageView/2/w/800/h/600/q/80/format/png"/><p>本文主要介绍了 CSS Modules，以及如果在最新版的 Vue-loader 中开启 CSS Modules</p><p></p>
---------------
<h1 id="#title_13" >14、从苏宁十年技术演进，看架构意识转变的关键一步</h1>
李东辉
[http://www.infoq.com/cn/news/2016/11/suning-10-Architecture-conscious?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2016/11/suning-10-Architecture-conscious?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>双11狂欢结束后，又是一轮长期的技术复盘时间，这个阶段往往是互联网电商酝酿新一轮架构演进的契机。演进实践中不仅需要解决大促遗留下的问题，还需要判断新的设计是否能够满足未来发展的需要。如何朝着合适的架构演进以减少未来意想不到的坑和教训，这往往是不少架构师需要深思熟虑的问题。</p> <i>By 李东辉</i>
---------------
<h1 id="#title_14" >15、Uber工程的deck.gl框架下的Web数据可视化集</h1>
Nicolas Garcia Belmonte
[http://www.infoq.com/cn/news/2016/11/Uber-deck-gl-Web-data?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2016/11/Uber-deck-gl-Web-data?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>今天，我们开源了deck.gl，这是一个WebGL驱动的框架，专门用于大规模探索和可视化数据集。deck.gl让我们不经妥协就能可视化。</p> <i>By Nicolas Garcia Belmonte</i> <i> Translated by 刘志勇</i>
---------------
<h1 id="#title_15" >16、不计前嫌，握手言和：Microsoft宣布新版SQL Server将同时支持Windows与Linux两大平台</h1>
刘志勇
[http://www.infoq.com/cn/news/2016/11/Microsoft-SQL-Server-Windows-Lin?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2016/11/Microsoft-SQL-Server-Windows-Lin?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>今年三月份，微软首次宣布自旗舰产品SQL Server将支持Linux平台，给世界带来了一个巨大的惊喜。到目前为止，只有被邀请才能预览。但是微软11月17日在纽约举办的Connect开发者大会上宣布，想尝试的用户现在可以试用其内测预览版了。此内测预览版是第一个可同时用于Windows和Linux的版本。</p> <i>By 刘志勇</i>
---------------
<h1 id="#title_16" >17、连接12万+开发者，揭秘网易场景化云服务背后的技术</h1>
陈兴璐
[http://www.infoq.com/cn/news/2016/11/12-cloud-technology-NetEase?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2016/11/12-cloud-technology-NetEase?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>自2015年起，网易悄然上线了多款云服务产品，包括网易云信（即时通讯云）、网易七鱼（全智能云客服）、网易视频云、网易蜂巢（容器云）等，多个角度切入，进军云服务市场。网易云信即网易迈入云服务市场的第一步。
</p> <i>By 陈兴璐</i>
---------------
<h1 id="#title_17" >18、微软发布Visual Studio Mac预览版</h1>
薛命灯
[http://www.infoq.com/cn/news/2016/11/Microsoft-Visual-Studio-Mac?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2016/11/Microsoft-Visual-Studio-Mac?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>日前，微软发布了Visual Studio的Mac预览版。Mac用户终于可以在自己喜欢的平台上使用Visual Studio开发各种应用了。</p> <i>By 薛命灯</i>
---------------
<h1 id="#title_18" >19、算法时代的媒体</h1>
薛命灯
[http://www.infoq.com/cn/news/2016/11/Algorithm-Age-Media?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2016/11/Algorithm-Age-Media?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>算法时代的媒体应该怎样通过算法来为广大用户“去伪存真”？Facebook正走在这样的一条路上。</p> <i>By 薛命灯</i>
---------------
<h1 id="#title_19" >20、视频演讲： 平安金融云之CaaS服务建设和应用</h1>
方国伟
[http://www.infoq.com/cn/presentations/the-construction-and-application-of-caas-services-in-pingan-financial-cloud?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/the-construction-and-application-of-caas-services-in-pingan-financial-cloud?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/the-construction-and-application-of-caas-services-in-pingan-financial-cloud/zh/mediumimage/fangguowei_270.jpg"/><p>平安云的目标是利用平安科技多年金融IT的建设经验和技术积累，构建一个能够满足平安“互联网＋金融”业务发展的平台，实现IT服务共享，推动IT服务模式和运营方式的创新，并且逐步为更多金融机构提供多种服务的金融云平台。这个演讲将围绕着我们构建平安云的容器服务过程中所学到的各种经验教训，从技术选型、架构设计以及DevOps实践等方面的实践和思考。希望这个分享能够为其他云平台或IT服务平台的容器服务建设有所参考，并借此相互学习和借鉴来提高IT服务能力和水平。</p> <i>By 方国伟</i>
---------------
<h1 id="#title_20" >21、视频演讲： 移动测试体系</h1>
佟明来
[http://www.infoq.com/cn/presentations/mobile-test-system?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/mobile-test-system?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/mobile-test-system/zh/mediumimage/tongminglai1_270.jpg"/><p>随着移动通信网络的发展，移动互联网用户数量不断攀升，移动互联网已经成为当今世界发展最快、市场潜力最大的业务，随之而来的移动互联网应用也是缤纷多彩，各种应用已经深入渗透到人们的生活中，为了快速占领细分用户市场，移动应用的开发上线周期越来越短，对移动应用测试的要求越来越高。如何保证移动应用的质量，是测试团队需要解决的一个难题。</p> <i>By 佟明来</i>
---------------
<h1 id="#title_21" >22、文章： 借助数据科学解决业务问题</h1>
Francine Bennett
[http://www.infoq.com/cn/articles/data-science-for-business?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/data-science-for-business?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/data-science-for-business/zh/smallimage/logo-data-science.jpg"/><p>企业越来越意识到，有许多最紧迫的问题，只要稍微运用一点数据科学就可以解决。本文是该系列文章的第一部分，介绍成功实施面向业务的数据科学项目的基础知识。</p> <i>By Francine Bennett</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_22" >23、[前端] [干货] 滴滴出行在小程序的实践</h1>
滴滴出行·DDFE
[http://gold.xitu.io/entry/5831a47f67f356006353c070](http://gold.xitu.io/entry/5831a47f67f356006353c070)
<img src="http://ac-mhke0kuv.clouddn.com/6994856bf2cf26f0f817.jpg?imageView/2/w/800/h/600/q/80/format/png"/><p>滴滴出行的 webapp 有着非常庞大的用户量，对于用户体验的要求很高，因此我们在做小程序的时候也是精益求精的，现在把相关实践给大家看看。</p><p></p>
---------------
<h1 id="#title_23" >24、文章： 大数据杂谈微课堂 | 数据挖掘技术和房地产的有效结合</h1>
蔡白银
[http://www.infoq.com/cn/articles/combination-of-data-mining-technology-and-real-estate?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/combination-of-data-mining-technology-and-real-estate?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/combination-of-data-mining-technology-and-real-estate/zh/smallimage/design_logo.jpg"/><p>数据挖掘依托房地产行业累积的海量数据，从中挖掘出最有价值的数据， 从而改善行业体验，推动行业进步。 本文内容主要包括如下两个部分： 1）数据挖掘在房产领域的可行性和必要性 2）数据挖掘在链家网的实践详情</p> <i>By 蔡白银</i>
---------------
<h1 id="#title_24" >25、视频演讲： 以应用为核心，重走上云之路</h1>
郭宗敬
[http://www.infoq.com/cn/presentations/take-the-application-as-the-core?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/take-the-application-as-the-core?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/take-the-application-as-the-core/zh/mediumimage/guozongjing_200.jpg"/><p>经过这几年的市场教育，云计算的概念已经深入人心，经过数年的发展，人们不再怀疑云就是未来。越来越多的企业开始计划或者实施 IT 业务转型，将业务迁移到云端运行。但是已经实施业务上云的企业开始发现上云之后的路不像原本规划的那么顺畅，对研发及应用运维部门来说，交付和管理效率没有大幅提高；对资源管控部门，缺乏有效的云资源管控治理工具；对于运营部门，PaaS 平台落地困难；对云平台规划部门，缺乏支持遗留 IT 及 IT 演进的开放管理平台。那么其中的问题又在哪里呢？上云的初衷难倒这么难以实现吗？通过这次主题分享，演讲者将为大家分享如何从业务出发，重走上云之路，回归业务上云的本心。</p> <i>By 郭宗敬</i>
---------------