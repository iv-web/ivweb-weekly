## 文章索引
1、 <a href="#1每周分享第-9-期" >每周分享第 9 期</a><br/>
2、 <a href="#2smashing-book-6-excerpt:-bringing-personality-back-to-the-web" >Smashing Book 6 Excerpt: Bringing Personality Back To The Web</a><br/>
3、 <a href="#3wwdc-2018-diary-of-an-ios-developer" >WWDC 2018 Diary Of An iOS Developer</a><br/>
4、 <a href="#4文章-一文看懂net的各种变体" >文章： 一文看懂.NET的各种变体</a><br/>
5、 <a href="#5文章-中小企业如何做好推荐系统" >文章： 中小企业如何做好推荐系统？</a><br/>
6、 <a href="#6人脸识别技术的真相" >人脸识别技术的真相</a><br/>
7、 <a href="#7instana支持基于ai驱动的aws-lambda应用程序监控" >Instana支持基于AI驱动的AWS Lambda应用程序监控</a><br/>
8、 <a href="#8麻省理工研究人员在比特币闪电网络上测试oracle和智能合约" >麻省理工研究人员在比特币闪电网络上测试Oracle和智能合约</a><br/>
9、 <a href="#9文章-weex技术在苏宁移动办公开发中的实践" >文章： Weex技术在苏宁移动办公开发中的实践</a><br/>
10、 <a href="#10文章-通俗解读aws-vpc子网" >文章： 通俗解读“AWS VPC子网”</a><br/><h1 id="#title_0" >1、每周分享第 9 期</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2018/06/weekly-issue-9.html](http://www.ruanyifeng.com/blog/2018/06/weekly-issue-9.html)
<p>这里记录过去一周，我看到的值得分享的东西，每周五发布。</p>

        <p>这个周末是端午节，我要陪家人旅行，所以提前一天发布，祝大家端午节快乐。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201806/bg2018061401.jpg" alt="" title="" /></p>

<p>（题图：星愿公园，上海，2017）</p>

<p>一个网友看了我的新书，留言说："现在已经是未来了，大多数人不知道而已"。这也是我的感受，普通人不知道现在的技术先进到什么地步，很多神话般的功能都已经做到了。</p>

<p>举例来说，我看到一个，麻省理工学院发明了一种远程充电技术，可以隔空用无线电波给微型电子设备充电。他们做了一个实验，把传感器埋入一头猪的体内，大约皮下10公分的地方，然后相隔一米发送无线电波，居然就把传感器驱动起来了！</p>

<p>这意味着微型电子设备从此不需要电池了，可以做得很小（比米粒还小），从而能够植入人体，使用的时候，发送电波就行了。以前做不到，是因为无线电波携带的能量非常微弱，又不知道设备的具体位置，没法用来充电。新技术克服了这些难点。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201806/bg2018061402.jpg" alt="" title="" /></p>

<p>一旦人体可以植入电子设备，不再有充电的难题，那会带来怎样的变革？我的想象力都不够了......以后可能不再需要身份证了，每个人的体内植入私钥，检查身份的时候，一发信号，返回一个私钥签名的证书，只要跟公钥匹配，立刻就验明正身。</p>

<h2>新闻</h2>

<p>1、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201806/bg2018061403.jpg" alt="" title="" /></p>

<p>美国一家名叫 Volans-i 的创业公司，开发了一种时速300公里、续航800公里的无人驾驶飞机，主要用来送货，可以负重9公斤。官网介绍是向工厂，医院，建筑工地和海上船舶提供重型零件和设备。</p>

<p>可以想象，收发室以后可以设在楼顶。也没有快递员，无人飞机直接就把货送过来了。</p>

<p>2、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201806/bg2018061404.jpg" alt="" title="" /></p>

<p>刚刚发布的 Chrome 67 提供了桌面 PWA 功能，也就是说，可以把网页变成桌面应用，能够离线使用，并且 Windows 和 Mac 都支持。上面图片里的媒体播放器，实际上是一个网页。有了它，Electron 的使用场景大大缩减，可能只剩下读写本地文件。 </p>

<p>3、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201806/bg2018061405.jpg" alt="" title="" /></p>

<p>新加坡到纽约的航班是世界上最长的航班，连续飞行18小时45分钟。今年10月，新加坡航空公司将重启这条航线。</p>

<p>它会世界上首次使用超远程飞机空客 A350-900 ULR。这种飞机的特点就是很节省燃料，整架飞机使用碳纤维制成，比传统的铝质材料轻，并且只有两台发动机，而不是传统的四台发动机。同时，它最多只能搭载161位乘客，这一方面为了减轻负重，另一方面也是为了提供稍大的座位，毕竟要坐上18个小时。</p>

<p>据说，主要就是因为新飞机省油，才使得这种超远程航线有利可图。</p>

<p>4、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201806/bg2018061406.jpg" alt="" title="" /></p>

<p>最近爆出的CSS漏洞窃取用户信息，令人叹为观止。黑客诱导用户访问一个恶意网页，里面嵌入 iframe 加载用户 facebook 主页。然后用一个单像素图片，逐一放在 iframe 的每个像素上面，再使用 mix-blend-mode 的 CSS 设置，根据渲染时间差异，算出原始像素的颜色，20秒可以拿到用户名。</p>

<p>5、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201806/bg2018061407.jpg" alt="" title="" /></p>

<p>目前，以太坊的交易量已经占到所有加密货币交易的一半。很多人认为，比特币的地位将越来越衰弱，被其他加密货币取代。</p>

<p>6、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201806/bg2018061408.jpg" alt="" title="" /></p>

<p>Nodejs 的创始人 Ryan Dahl 一共做过两次关于 JS 的公开演讲。 一次是2009年宣布 Node 项目诞生，另一次是九年后的昨天，演讲题目是《Node 的设计失误》。</p>

<p>这个演讲的内容非常火爆，基本上把 Node 全部否定了，认为 libuv 和 npm（包括 package.json）都是设计错误，怪不得 JS 圈里面没人作声。他觉得，Node 已经无药可救了，所以动手写了一个新项目 deno（这个名字是 node 的拆分，表示 node 重组）。</p>

<p>7、</p>

<p>据英国《金融时报》网站6月2日报道，通过所谓的首次代币发行（ICO），总部位于开曼群岛的Block.one公司提供EOS代币，换取另一种加密货币以太币。据区块链咨询公司"新魔力"公司提供的数据，以6月1日的兑换率计算，这次发行筹集到了41.5亿美元。Block.one拒绝提供正式交易数据。报道称，为了规避监管障碍，在该公司于1日结束的ICO中，美国公民被禁止参与。</p>

<p>不管加密货币能不能成为真正的货币，只要能够推动金融改革，让投融资变得更加互联网化，它就成功了。</p>

<p>8、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201806/bg2018061409.jpg" alt="" title="" /></p>

<p>微软在宣布收购 GitHub 几天后表示，未来几个月里面，就会发布 Visual Studio 2019。</p>

<p>5月份的 Build 2018 开发者大会上，微软展示了两个新的 Visual Studio 功能：IntelliCode 和 Live Share。前者使用 AI 提供改进代码质量和工作效率的智能建议，后者可让开发人员与团队成员进行实时协作，这些团队成员可以直接从 Visual Studio 和 Visual Studio Code 进行协同编辑和调试。</p>

<h2>免费 Python 课程</h2>

<p>本期《每周分享》很高兴得到）的赞助。他们成立于2017年，是老男孩教育的在线教育品牌。</p>

<p>Python 是现在最热门的语言，。这门课帮助大家掌握 Python 的基本用法，具备简单的开发能力。</p>

<p></p>

<p>如果你有 Python 基础，想要用爬虫来做一些有趣的事情，比如：</p>

<blockquote>
  <ul>
<li>爬取知乎热门文章并对指定回答批量刷赞</li>
<li>爬取微博热门话题评论并分类分析</li>
<li>爬取58同城批量获取客户的租房需求、联系方式</li>
<li>破解业内通用的图片&amp;滑动验证码</li>
<li>如何应对网站反爬虫策略</li>
</ul>
</blockquote>

<p>课程就能满足你的需求。该课程从爬虫开发入手，旨在提高学员的 Python 实战能力，在源码级别深度剖析流行的爬虫框架，研究如何提高爬虫性能，并包含防爬策略的解决方法。</p>

<p><a href="https://www.luffycity.com/home/camp?source=ruanyifeng"><img src="https://www.wangbase.com/blogimg/asset/201806/bg2018061411.jpg" alt="4779557561561238374.jpg" title="" />
</a></p>

<p><strong>最重要的事情放在最后说，上面这两门课程都是免费的！</strong>缴纳99元保证金即可参与，只要完成3次作业和参与直播，提交学习笔记，就可以退还保证金，还可获得《Python全栈开发实战》及内部教材书籍，视频课程、定制文化衫等作为奖励。另外，还会有1对1的导师逐行批改你的代码、讲师3次直播答疑，还有班主任组队小伙伴共同学习。</p>

<p>这两门课都只有 200 个名额，点击这里加入。跟客服说看了阮一峰博客，还可以获得50元课程代金券。</p>

<h2>教程</h2>

<p>1、[文章]  （英文）</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201806/bg2018061412.jpg" alt="" title="" /></p>

<p>本文介绍数码相机 CMOS 芯片的感光原理，彩色的光线是如何变成数字信号的。</p>

<p>2、[游戏] </p>

<p><img src="https://www.wangbase.com/blogimg/asset/201806/bg2018061413.jpg" alt="" title="" /></p>

<p>一个帮助玩家学习人工智能的游戏。你扮演一个人工智能专家，在游戏的引导下解决各种问题。</p>

<p>3、[文章] （英文）</p>

<p>这篇文章教你如何在没有任何 Linux 经验的情况下，全新安装Kubuntu 18.04系统，并在这个系统安装比特币完整节点，加入比特币网络。</p>

<p>4、[视频] （英文中字）</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201806/bg2018061414.jpg" alt="" title="" /></p>

<p>志愿者从 Youtube 搬到 B 站的40集视频教程。</p>

<p>5、[仓库] （中文）</p>

<p>Ruby China 论坛的精华贴整理。</p>

<p>6、[PDF] （英文）</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201806/bg2018061415.jpg" alt="" title="" /></p>

<p>上面是相关系数的计算公式，这是统计学的基础公式。我一直不知道它是怎么推导出来的，为什么这个公式就能断定两个矢量的相关性，我读过的教科书都不解释这一点。</p>

<p>这里有一篇论文，给出相关系数的，所以完全相关是+1或-1，完全不相关是0，一下子就看懂了。</p>

<p>7、[PPT] （英文）</p>

<p>2013年的时候，Docker 团队介绍他们为什么使用 Go 语言写 Docker。</p>

<p>8、[文章]  （英文）</p>

<p>一组三个部分的系列文章，介绍如何从零开始写一个 Markdown 解析器。作者是用 Ruby 语言实现，但是一些基本知识的介绍跟语言无关，写得挺好的。</p>

<h2>资源</h2>

<p>1、</p>

<p><img src="https://cdn.yuque.com/yuque/0/2018/png/84141/1527321073136-49ebdc56-6011-43e5-a335-47d2b381a8d4.png" alt="Robots   The Old Robots Web Site.png | center | 340x363" title="" /></p>

<p>这个数据库收集人类历史上生产的各种型号的机器人。</p>

<p>2、[电子书] （英文）</p>

<p>这是开源教材，介绍密钥加密的知识。因为是研究生教材，内容不容易。</p>

<h2>工具</h2>

<p>1、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201806/bg2018061417.jpg" alt="" title="" /></p>

<p>多人实时协同作画的桌面应用。</p>

<p>2、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201806/bg2018061427.jpg" alt="" title="" /></p>

<p>一个有手绘效果的网页组件库。但是，真正特别之处在于它的底层是 Web components，让我们看到了除了React/Vue之外，还有其他的路。</p>

<p>3、</p>

<p>Python 语言的格式要求特别高，因为它通过缩进判断语法区块。现在有了这个工具，就可以自动化格式化 Python 代码，所以你不用担心写出风格一团糟的代码。</p>

<p>4、</p>

<p>一个新的 JavaScript 转码器，号称比 Babel 快20倍。</p>

<p>5、 </p>

<p><img src="https://www.wangbase.com/blogimg/asset/201806/bg2018061418.jpg" alt="" title="" /></p>

<p>Uber 开源的基于地图的数据可视化框架。</p>

<p>6、</p>

<p>作者用 Python + ADB 做的 Bot。它会自动打开 APP 对视频截图，然后请求腾讯的 ，当颜值大于门限值 <code>BEAUTY_THRESHOLD</code>时，点赞并关注，接着翻到下一页，重复进行该过程。</p>

<h2>文摘</h2>

<p>1、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201806/bg2018061419.jpg" alt="" title="" /></p>

<p>2012年8月，微信公众号平台诞生。产品经理回忆，当时根本没有布局战略。但是，公众号的发展超乎想象，上线短短数年，就成为国内最大的内容生产和内容分发平台，一个个暴富传奇在公众号平台上诞生。</p>

<p>可是，五年后的今天，公众号的风口似乎已经过去。根据新榜发布的《2017年中国微信500强年报》，公众号整体平均阅读数下降了24%。内容同质化、用户审美疲劳、短视频来势凶猛，自媒体野蛮掘金的时代结束了。</p>

<blockquote>
  <p>龙泉2014年做"什么值得吃"时，只是一个人凭兴趣一周写两篇，2017年他成立了公司，投入了3个人做新号"马达厨房"，图文质量比最初做"什么值得吃"时好得多，但却怎么也做不起来。</p>

<p>胡辛束也面临同样的困境。她们的粉丝数始终无法突破60万，到了2017年，阅读量也开始下滑，拿融资时日均阅读可以达到七八万，年底时头条阅读量仅两三万。</p>

<p>"基本上没有免费的流量可言，再起来的要么就是花钱，要么就是内容实在优质，能够靠文章自然涨粉的非常少，互推也基本上没有效果，因为号实在太多了。"情感大号"入江之鲸"的创始人鲸鱼表示。</p>
</blockquote>

<p>2、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201806/bg2018061420.jpg" alt="" title="" /></p>

<p>2017年7月20日，软银集团董事长孙正义在东京的 SoftBank World 大会的演讲。</p>

<p>他称，这一次的信息革命，会带来一个没人能想象的世界。对于这种巨大的变革，他实在太兴奋，忙到觉得睡觉都是浪费时间。软银把所有的钱都投在新技术上面，他说金额比其他VC的投资总额还要多。</p>

<p>接下来，他就介绍几个他认为最重要的技术领域。</p>

<p>3、（英文）</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201806/bg2018061421.jpg" alt="" title="" /></p>

<p>能量的储存一直是难题。电池技术无法储存大量的能量，而且成本高昂。这篇文章提出，我们可以考虑使用压缩空气来储存能量。</p>

<blockquote>
  <p>目前，全球99％以上的电力储存都是由抽水蓄能电站完成，在电力富余的时候，将水从较低水库抽到较高水库。但它需要两个垂直分开的大型水体和一个或两个水坝的合适地理位置。它也会淹没大片土地。大多数能够建造的水电站都已经投入使用，这意味着进一步发展的可能性很小。</p>

<p>压缩空气储能被认为是可再生能源电网的重要组成部分，因为它可以大规模储存风力涡轮机和太阳能电池板的剩余电量。相比电池，更可持续，具有更长的预期寿命，更低的生命周期成本，技术简单性和低维护成本。</p>

<p>目前，全世界只有两座大型空气压缩储存工厂：一座在德国，一座建于1979年，另一座在美国，建于1991年。这主要因为压缩空气储能和释放能量时，会有一半的能量损失。抽水蓄能电池的充/放电效率为70-85％，化学电池达到65-90％，但现有压缩空气的工厂，储能效率仅为50%左右。这是因为压缩到高压时，空气温度升高，导致能量变为热量，散发到大气中。</p>
</blockquote>

<h2>新奇</h2>

<p>1、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201806/bg2018061422.jpg" alt="" title="" /></p>

<p>华硕最新笔记本的触摸板，是一块触摸屏。为什么没有人早点想到这个点子？</p>

<h2>每周图片</h2>

<p><strong>1、七年前的微信评价</strong></p>

<p><img src="https://www.wangbase.com/blogimg/asset/201806/bg2018061423.jpg" alt="" title="" /></p>

<p>还记得短信流行的年代吗？上面是七年前微信刚刚问世时，用户对它的评价。很多人没有意识到，技术改变的不是产品，而是我们。</p>

<p>2、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201806/bg2018061424.jpg" alt="" title="" /></p>

<p>第一张图是 G Suite 办公套件，第二张图是谷歌云。</p>

<p>3、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201806/bg2018061425.jpg" alt="" title="" /></p>

<p>Node 创始人 ry 发了一个新项目 deno，它是基于 V8 引擎的 TypeScript 运行时（Node 是 JavaScript 运行时）。 结果，一个中国网友跑去，写了上面的留言。 ​​​</p>

<h2>本周金句</h2>

<p>Mixmax 公司写了一篇。他们原先使用 npm 管理 JavaScript 模块，觉得不好就改成了 yarn，后来觉得还是不好，又改回了 npm。</p>

<p>网友的："这就是我喜欢JavaScript的地方：你总是有活要忙。"</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201806/bg2018061426.jpg" alt="" title="" /></p>

<h2>欢迎订阅</h2>

<p>这个专栏每周五发布，同步更新在我的。</p>

<p>微信搜索"<strong>阮一峰的网络日志</strong>"或者扫描二维码，即可订阅。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2018/bg2018042311.jpg" alt="image | left" title="" /></p>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2018-06-14T14:01:28+08:00">2018年6月14日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>文集：</li>
<li>社交媒体：</li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------
<h1 id="#title_1" >2、Smashing Book 6 Excerpt: Bringing Personality Back To The Web</h1>
Vitaly Friedman
[https://www.smashingmagazine.com/2018/06/bringing-personality-back-to-the-web/](https://www.smashingmagazine.com/2018/06/bringing-personality-back-to-the-web/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/06/bringing-personality-back-to-the-web/" />
              <title>Smashing Book 6 Excerpt: Bringing Personality Back To The Web</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>Smashing Book 6 Excerpt: Bringing Personality Back To The Web</h1>
                  
                    
                    <address>Vitaly Friedman</address>
                  
                  <time datetime="2018-06-14T14:40:27&#43;02:00" class="op-published">2018-06-14T14:40:27+02:00</time>
                  <time datetime="2018-06-14T18:32:54&#43;00:00" class="op-modified">2018-06-14T18:32:54+00:00</time>
                </header>
                

<p>Generic web layouts have become somewhat of a misnomer in conversations circling around web design these days. We’re bored and slightly annoyed by how predictable and uninspired most web experiences have become. Not without reason, though. Every single landing page seems to be a twin of pretty much every other web page.</p>

<p>In the header, a compelling hero image with a short main heading is followed by a lengthier subheading. Beneath them, uniform blocks of media objects are alternated &mdash; an image and a few paragraphs of text. First, text on the left, image on the right; then image on the left, text on the right. Rinse and repeat. Rounded profile photos and a square grid of thumbnails complete the picture, with perfect shapes perfectly aligned along the 12-column grid. The only variations come from sporadic parallax transitions and  notorious carousels, positioned at the top or bottom of the page &mdash; or perhaps both.</p>

<p>It’s not that somebody imposed these rules or limitations on our creative output; usually they originate from good motives and the best intentions. After all, one of the main tenets of web design has always been creating a subtle, almost invisible and functional interface &mdash; an interface that doesn’t make users think, where less is more, and form follows function, where simplicity prevails &mdash; an interface where everything feels just right.</p>

<p>Yet when everything is structured in a predictable way, nothing really stands out. Given how remarkably similar names, logos, icons, typography, layouts, and even shades of gradients on call-to-action buttons often are, it’s not surprising our <strong>users find it difficult to distinguish between brands</strong>, products, and services these days.</p>




<p>Very few people miss the golden times of the infamous Flash, with its strikingly experimental layouts and obscure mystery-meat navigation. Admittedly, in many cases the focus has shifted from creating an experience to merely providing content in a structured form. Yet unlike in those good ol’ days when we talked about how wonderful or horrible websites were, <strong>today most experiences are almost invisible</strong>, making it exceptionally difficult to connect emotionally with them.</p>

<p>If I asked you to think of a recently visited website that left a lasting, memorable impression on you, or what websites you truly love and admire for their unique design, or what website had a truly remarkable personality, would you be able to answer these questions immediately? Would you be able to provide more than one or two examples? Chances are that you won’t.</p>

<p>Not every website has to be unforgettable. It’s not that memorable websites automatically perform better, or hit better key performance indicators. However, if you want your product or service to stand out in a highly competitive and challenging environment, you need to be different in some way. Many of us would consider this to be the task of the marketing team. After all, they are supposed to place the product in the right light, at the right spot, for the right audience, at the right price. Yet in a world where many digital products are fairly usable and feature-rich, this would be a daunting undertaking that would often require months of extensive research and testing without the guarantee of a successful outcome. And even then, unless you are extremely good at predicting and shaping the next shiny big thing, it might not be good enough.</p>

<p>Customers are used to and expect decent experiences. They aren’t always fast or straightforward, but simply because of the sheer number of offerings, there are always decent tools and services out there that would be good enough.</p>

<p>We tend to believe we rationalize our decisions to extremes, choosing the best candidates, but it’s not necessarily true. According to well-known Herbert A. Simon’s <em>satisficing theory</em>, we tend to prefer the first option that meets an acceptability threshold, just because we don’t know if we can find a better option or how much effort it would take. We rarely study the entire spectrum of options in detail (and sometimes it’s nearly impossible), and as a result, we <em>satisfice</em> with a candidate that meets our needs or seems to address <em>most</em> needs.</p>

<p>To draw an audience’s attention, we need to be better than “good enough.” Nothing can beat word of mouth, but to get there we need to come up with something that’s worth looking at. What if I told you that there was a shortcut to getting there?</p>

<p>It’s not just about price. It’s not just about features. It’s not just about choosing the right placement of buttons, or the right shades of colors in endless A/B tests. And it’s not about choosing a cute mascot illustration that shows up in email campaigns. In the end, it’s about creating an <strong>experience that people can fall in love with, or connect deeply with</strong> &mdash; an experience that, of course, drives the purpose of the site, but also shows the human side of it, like the personality of the people building it, their values and principles, their choices and priorities.</p>

<p>That means designing voice and tone, interface copy, and embracing storytelling, authenticity, inclusivity, and respect; and all of that while establishing a unique visual language supported by original layout compositions and interaction patterns. Together with clear and honest messaging, these create a unique signature, which, used consistently, makes the product stand out from the rest. This task might sound as daunting as months of marketing research, but it doesn’t necessarily require an enormous amount of effort or resources.</p>

<p>In this chapter, we’ll look into a few <strong>practical techniques and strategies</strong> that might help you find, form, and surface your personality efficiently. By doing so, we’ll  explore how doing so consistently could fit into existing design workflows, along with plenty of examples to give you a good start. But before we get there, we need to figure out how omnipresent design patterns and best practices fit into the equation.</p>

<h3>Breaking Out By Breaking In</h3>

<p>The creative process isn’t linear. Every single design decision &mdash; from colors and type to layout and interactivity &mdash; requires us to consider options and evaluate combinations. While the creative process is often seen as a straightforward, iterative process, in reality it’s very rare that we smoothly move from one mock-up to another through a series of enhancements and adjustments. More often than not, we tend to float and diverge, heading from one dead end to another, resolving conflicts and rerouting our creative direction along the way.</p>

<p>Those dead ends happen when we realize we aren’t really getting anywhere with the result exposed on our digital canvas. We’ve been there so many times, we know how to explore uncharted territories and how to maneuver the flanks, and so as we keep sculpting our ideas, we keep making progress, slowly but steadily moving towards a tangible result. Two steps forward, one step back, revisiting what we’ve done so far and refining those precious pixels &mdash; based on… frankly, based on intuition and random experiments. Eventually the back-and-forth brings us to a calm, peaceful, and beautiful place &mdash; just where we think we’ve found a solution &mdash; <em>the</em> solution.</p>

<p>We know, of course, that it’s unlikely it’s going to be the <em>one</em>, though, don’t we?</p>

<p>This journey from <em>nothing</em> to <em>something</em> isn’t just full of conflicting micro-decisions; it’s crammed with unknowns, traps, friction, and difficult constraints, be they of a technical nature or time-sensitive. And at every moment of the process, the beautiful, harmless creatures of our imagination can be mercilessly smashed against the harsh reality of user interviews and client revisions. So we swizzle around from one direction to another in a fertile yet remarkably hostile place. As a result, usually we can’t afford the luxury of losing time, as we know that the path to <em>that</em> deadline, harmlessly floating in the remote future, will be full of surprises and unexpected turnarounds.</p>

<p>To avoid losing time, we rely on things that worked well in our previous projects &mdash; the off-canvas navigation, the accordion pattern, rounded profile images, and the holy 12-column grid layout. It’s not for lack of knowledge, skill, or enthusiasm that we fall back to all those established practices &mdash; it’s just infinitely more difficult and time-consuming to come up with something different every single time. And because we lack time, we use all those wonderful, tried-and-tested design patterns &mdash; all of them tangible, viable solutions for a particular kind of problem. Obviously, this process might be slightly different for different people, but broken down into its essence, that’s what’s happening behind the scenes as we make progress in our designs.</p>

<p>When we started working on the redesign of Smashing Magazine a few years ago, one of the first steps we took was listing and exploring components and micro-interactions. We built the article layout and a style guide, responsive tables and forms, and used many of the established best practices to keep them accessible, fast, and responsive. Yet when putting all these perfect components together, we realized that while they were working well as standalone solutions, they just didn’t work together as a whole. The building blocks of the system weren’t sufficient to maintain and support the system. We had to redesign what we’d built so far, and we had to introduce overarching connections <em>between</em> those components that would be defined through the personality and voice and tone of the new identity.</p>

<p>When we apply design patterns to our interfaces, we essentially bring together a group of loose modules or interactions that lack any connection to everything else. Rather than asking how a particular pattern helps drive the purpose of the experience, we often explore a micro-problem in isolation, putting micro-solutions together. With design patterns, we run the risk of adding a component just because it’s trendy these days &mdash; like a parallax-effect, slow and impactful transitions, and fade-ins. By doing so, sometimes we might lose the big picture of what role that component would play at a bigger scale, and how it could be connected to everything else. As a result, we produce soulless, dull, bloated designs with generic compositions and generic visual treatments. That’s how we create something that looks like everything else.</p>

<p>It’s not that design patterns and best practices are necessarily evil, though. They are merely a double-edged sword helping and troubling the visual output.,When applying them, we need to do so carefully and thoughtfully. Whenever you consider resolving a problem with a design pattern, it’s a good idea to ask yourself a few questions:</p>

<ol>
<li>What problem exactly are we solving?</li>
<li>Is the pattern really the best solution for the problem?</li>
<li>How do people experience this interaction, and what pain points do they encounter while doing so?</li>
<li>How does this component help us reach the overarching goal of the system?</li>
<li>How do we connect that component to the rest of the system &mdash; in terms of both aesthetics and interaction design?</li>
<li>Is the solution really universally understood, or do we need to provide more clarity to the design (labels, better copy, affordance, replacing icons with words)?</li>
<li>Is it a good idea to keep the pattern as is at all times? Or is it better to load or adjust it conditionally, perhaps based on the viewport, or how many times a customer has visited the page?</li>
</ol>

<p>Essentially, we try to <strong>break down a design pattern</strong> by exploring when and how it’s useful or damaging, and how it helps in achieving our goals. We break out of predictable patterns by breaking in to their nature and understanding why we actually use them. First, we examine the component in its bare, abstract form, without the context of where it’s typically used and how it’s usually designed; for example, rather than thinking of an off-canvas navigation sliding from the left to right, or right to left, we look into the interaction pattern on its own &mdash; essentially, progressive disclosure in which content is hidden by default and displayed on click/tap. Then, for every pattern, we explore its usability issues and problems, resolve them, and then style and design the module in a way that feels connected to everything else. That last step could be something as simple as a consistently used transition, or a geometric pattern, or a non-conventional position in the layout. Finally, once everything is in place, we repackage the design pattern and add it to the library, ready to be served for the rest of the system.</p>

<p>Of course, best practices and design patterns are fantastic shortcuts for getting on the right track faster. They let us tap into predictable interactions and sequential knowledge that most of our users will have. In fact, they are as relevant today as they’ve always been. The key is in finding a way to apply them <em>meaningfully</em> within the context of the visual language used throughout the site, and knowing when to break them <em>deliberately</em> to trigger an emotional connection.</p>

<h3>Humans Connect To Humans</h3>

<p>Do you remember the good ol’ days when we used an omnipresent “we” to make our little web shops appear bigger than they actually were? You might have been the only person freelancing from home in slippers and a bathrobe, or one of the very few people in a small design agency, but that profound “we” made the company sound more serious, and hence more trustworthy, didn’t it? We’ve pretended to be somebody else to get projects we wouldn’t be entrusted with otherwise &mdash; and I’ll be the first to admit that I am as guilty of it as everybody else.</p>











<figure >
	<a href="https://mailchimp.com/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a647df8b-d479-473d-acd6-f0909ccd6d5e/00-mailchimp-high-five1.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a647df8b-d479-473d-acd6-f0909ccd6d5e/00-mailchimp-high-five1.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a647df8b-d479-473d-acd6-f0909ccd6d5e/00-mailchimp-high-five1.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a647df8b-d479-473d-acd6-f0909ccd6d5e/00-mailchimp-high-five1.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a647df8b-d479-473d-acd6-f0909ccd6d5e/00-mailchimp-high-five1.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a647df8b-d479-473d-acd6-f0909ccd6d5e/00-mailchimp-high-five1.png"
			sizes="100vw"
			alt="Micro-interactions matter. The animation captures the essence of a feeling a user has before sending out a campaign to customers. It establishes an emotional connection."
		/>
	</a>

	
</figure>












<figure >
	<a href="https://mailchimp.com/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/32f84741-e7a8-4d17-9c87-5658ae129a0c/00-mailchimp-high-five2.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/32f84741-e7a8-4d17-9c87-5658ae129a0c/00-mailchimp-high-five2.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/32f84741-e7a8-4d17-9c87-5658ae129a0c/00-mailchimp-high-five2.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/32f84741-e7a8-4d17-9c87-5658ae129a0c/00-mailchimp-high-five2.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/32f84741-e7a8-4d17-9c87-5658ae129a0c/00-mailchimp-high-five2.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/32f84741-e7a8-4d17-9c87-5658ae129a0c/00-mailchimp-high-five2.png"
			sizes="100vw"
			alt="MailChimp’s interaction design just before and just after an email campaign is sent out."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			MailChimp’s interaction design just before and just after an email campaign is sent out. (
		</figcaption>
	
</figure>


<p>These days, when so many things around us are exaggerated and deceptive, authenticity remains one of the few qualities people genuinely connect to. Too often, however, it’s not exhibited through a website at all, regrettably creating a vague image of yet another obscure entity covered with corporate stock photos and meaningless jargon. When every brand promises to disrupt or be different, nothing truly feels disruptive or any different, and this causes alienation and skepticism.</p>

<p>Humans can genuinely connect to brands they trust, but brands need to earn that trust first. Obviously, it comes from reliable recommendations and positive experiences. But as designers communicating on behalf of companies, how do we efficiently elicit trust in people who aren’t yet aware of the brand? As it turns out, trust can also come from the appearance of the brand, which can be influenced by its values, beliefs, principles, and activities. It isn’t easy to fall in love with a company or organization without knowing somebody who admires it almost contagiously. It’s much easier to connect with <em>people</em> whose values you support, and with <em>people</em> who stand behind their beliefs and principles.</p>

<p>If humans connect best to humans, perhaps if our interfaces reflected the values of the people creating them, we might be one step closer to triggering that desired emotional connection. We’ve been there before, of course, and so that’s why we show the people working in the company on a “Team” page or in the footer of the front page, right? Well, let’s look into it from a slightly different perspective.</p>

<p>What if you were asked to describe the <strong>personality of your brand</strong>? What adjectives would you use? Think about it for a minute, and write them down.</p>

<p>Ready? Chances are high that you’ve come up with common and predictable answers. Perhaps words such as “simple,” “clean,” “strong,” “dynamic,” “flexible,” or “well-structured” have come to mind. Or maybe “attentive to details,” “focused,” “user-centric,” and “quality-driven.”</p>

<p>Can you see a problem with these answers? These words describe our <em>intention</em> rather than our <em>personality</em>. While the former is usually very specific and stable, the latter is usually very fuzzy and ever-changing. The qualities outlined above don’t provide a good answer to the question, as they describe <em>how we want to be perceived</em>, but not necessarily how we actually <em>are</em>. In fact, usually we don’t really know who we are or how we are perceived outside of the comfortable company bubble we find ourselves in.</p>

<p>Instead, what if you asked your colleagues and customers a slightly different question: what they care about most in their work, and what they value the most about the company or the product. Maybe they care about the diversity of talented, motivated co-workers who are knowledgeable and experienced, yet also approachable and humble? Maybe it’s the fact that the company is actively contributing to pro bono projects for non-profit organizations that make a real difference in the world. Maybe because it supports schools and newcomers to the industry by providing an annual scholarship. Or because it ties in the profits with a fair salary bonus for all employees. Or just because it allows you to play with the latest fancy technologies and crazy experiments, and contribute to open-source in five percent of your working time. The company doesn’t need huge ambitions, idealist goals, or a fancy working environment to stand out.</p>

<p><strong>Sidenote</strong>: <em>Designing humane experiences means being kind and humble, and emphasizing qualities that matter to the company and to users. That means highlighting privacy, respect, ethics, and transparency, but also reflecting the personality of people working on the product</em>.</p>

<p>Here’s an example. Your company could care deeply about diversity, data privacy, accessibility, and transparent pricing. That would mean your interface is accessible and honest, you publicly take a stand against giving away customer data to third parties, and you include features that support pricing comparison without pushing your agenda over the edge. You could highlight those values prominently along with the competitive pricing tiers, and measure the outcome.</p>

<p>Now, can you spot a similar thread among all of the statements above? Because they come from personal experiences, they seem much more human and relatable than more general and abstract terms you might come up with initially.</p>

<p>That’s why companies like Slack or MailChimp feel so much more tangible than brands like Uber or General Electric. They employ quirky and informal microcopy and illustrations that reflect their human side. They don’t shine through a mission statement or press releases, but through the quirks in the interface and how they communicate publicly, via email, or in social channels. That’s the underlying foundation of a character deeply integrated into the user experience.</p>











<figure >
	<a href="https://slack.com/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1b068903-f5a1-4d7c-8f05-db5682c517db/00-slack-messaging1.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1b068903-f5a1-4d7c-8f05-db5682c517db/00-slack-messaging1.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1b068903-f5a1-4d7c-8f05-db5682c517db/00-slack-messaging1.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1b068903-f5a1-4d7c-8f05-db5682c517db/00-slack-messaging1.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1b068903-f5a1-4d7c-8f05-db5682c517db/00-slack-messaging1.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1b068903-f5a1-4d7c-8f05-db5682c517db/00-slack-messaging1.png"
			sizes="100vw"
			alt="Slack"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>












<figure >
	<a href="https://slack.com">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1b068903-f5a1-4d7c-8f05-db5682c517db/00-slack-messaging1.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1b068903-f5a1-4d7c-8f05-db5682c517db/00-slack-messaging1.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1b068903-f5a1-4d7c-8f05-db5682c517db/00-slack-messaging1.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1b068903-f5a1-4d7c-8f05-db5682c517db/00-slack-messaging1.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1b068903-f5a1-4d7c-8f05-db5682c517db/00-slack-messaging1.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1b068903-f5a1-4d7c-8f05-db5682c517db/00-slack-messaging1.png"
			sizes="100vw"
			alt="Slack"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>












<figure >
	<a href="https://slack.com">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2b12239c-2309-4d8d-b89a-2b7e2d8fa1df/00-slack-messaging2.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2b12239c-2309-4d8d-b89a-2b7e2d8fa1df/00-slack-messaging2.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2b12239c-2309-4d8d-b89a-2b7e2d8fa1df/00-slack-messaging2.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2b12239c-2309-4d8d-b89a-2b7e2d8fa1df/00-slack-messaging2.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2b12239c-2309-4d8d-b89a-2b7e2d8fa1df/00-slack-messaging2.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2b12239c-2309-4d8d-b89a-2b7e2d8fa1df/00-slack-messaging2.jpg"
			sizes="100vw"
			alt="Slack’s loading messages reflect the personality of the brand and the people working there. That’s the power of copywriting at play."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Slack’s loading messages reflect the personality of the brand and the people working there. That’s the power of copywriting at play. (
		</figcaption>
	
</figure>


<p>To avoid a generic appearance, you need to <strong>define your personality first</strong>. That means asking the right questions and finding accurate answers. When conducting user interviews with our readers, we quickly realized they had a quite different perspective on the Smashing brand than we did. Frankly, we confidently described the brand by listing all the usual suspects, the qualities you probably came up with initially. The truth was baffling, though: we couldn’t have been further away from how the brand was actually perceived.</p>

<p>We always wanted the magazine to be a professional, respectable publication with a strong voice in the industry, highlighting important work done by members of the community. User interviews brought up qualities that didn’t really describe that goal in the way we always strived for. Instead, we heard words such as “informal,” “quirky,” “friendly,” “approachable,” “supportive,” “community,” and &mdash; most importantly &mdash; “cats.”</p>

<p>Now, we never wanted our legacy to be cats, but it wasn’t really up to us at this point. Back in 2012, our dear illustrator Ricardo Gimenes chose to bring a Smashing cat to life as a mascot for our very first Smashing Conference. There was no conscious decision for or against it. We didn’t even properly discuss it, as we didn’t know if we’d host more conferences in the future anyway. This small decision put something in motion that we couldn’t dismiss years later. Because conferences turned out to become one of our central products, we’ve been promoting them heavily in our mailings, announcements, release posts, and social media messages.</p>

<p>Over time, every conference had to put up with a cat illustration of its own, and all these cats were facing our customers over and over again for years. Cat illustrations heavily influenced the perception of the brand without us actively fostering or guiding it. So we had to make a decision: either let the cats slowly fade away into oblivion, or integrate them heavily into the new design. You probably have discovered by now what we’ve settled with. As of this point, we have over 70 quirky and friendly cats freely wandering all over the new Smashing Magazine website.</p>











<figure >
	<a href="https://www.smashingmagazine.com/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f381b16c-3f08-4d09-a660-79730f4086ba/smashing-tv-cat.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f381b16c-3f08-4d09-a660-79730f4086ba/smashing-tv-cat.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f381b16c-3f08-4d09-a660-79730f4086ba/smashing-tv-cat.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f381b16c-3f08-4d09-a660-79730f4086ba/smashing-tv-cat.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f381b16c-3f08-4d09-a660-79730f4086ba/smashing-tv-cat.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f381b16c-3f08-4d09-a660-79730f4086ba/smashing-tv-cat.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>












<figure >
	<a href="https://www.smashingmagazine.com/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cbc46f01-10f5-4df5-88e9-cdb1ceb60b0f/2-smashing-cat.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cbc46f01-10f5-4df5-88e9-cdb1ceb60b0f/2-smashing-cat.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cbc46f01-10f5-4df5-88e9-cdb1ceb60b0f/2-smashing-cat.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cbc46f01-10f5-4df5-88e9-cdb1ceb60b0f/2-smashing-cat.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cbc46f01-10f5-4df5-88e9-cdb1ceb60b0f/2-smashing-cat.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cbc46f01-10f5-4df5-88e9-cdb1ceb60b0f/2-smashing-cat.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>However, as much as a mascot can help make the brand more approachable, it’s rarely enough to convey the full story. Interviews also helped us realize how important the <strong>community aspect</strong> of Smashing Magazine actually was. The words “community” and “people” appeared in user interviews a lot, and not without reason &mdash; the magazine wouldn’t exist without humble and generous open-source contributions from people behind the scenes. Our design didn’t really reflect it, though. So we chose to shift the focus slightly towards highlighting the people behind the scenes &mdash; authors, editors, and members of the community. Showing people prominently has become another attribute defining our design signature &mdash; and that explains why author thumbnails take up such a prominent position in the design, and why we highlight authors publishing on their own blogs or other platforms on our front page.</p>

<p>What does it all mean for you? <strong>Ask questions to surface humane qualities</strong> that lie in the very heart of the company first. This will give you a foundation to build a visual language on &mdash; a language that would translate your qualities to the interface design. Every company has a unique signature in <em>some</em> way, and often it’s reflected through the people working there. Ultimately, it’s just about finding the time and courage to explore it &mdash; and to embrace the fact that our flaws and quirks are a part of it as much as our big ambitions and good intentions are.</p>

<h3>Personality Is Never Perfect</h3>

<p>As designers, we often take pride in being perfectionists. Every pixel has to be polished, every angle has to be just right, and all components should be aligned to the grid. Remember that never-ending discussion about the perfect <code>border-radius</code> on call-to-action buttons? After an eloquent and long-winded debate, the design team eventually settles on 11px, just to switch over to 13px a few months later, just to move back to 12px by the end of the year. In many companies, these changes are prompted through numerous ongoing A/B tests, in which nothing is left to chance, and everything &mdash; from assumptions to design decisions &mdash; has to be tested and proved first.</p>




<p>We restlessly strive to reach the most effective, the best performing solution &mdash; a solution that’s just right. However, aren’t we riding our horses to death trying to improve the same tiny component over and over again, just to find a slightly better variant of it, with all those minimal, microscopic changes?</p>

<p class="c-pre-sidenote--left">Espen Brunborg, a creative lead for a graphic design agency in Norway, suggests to <strong>never conduct A/B tests alone.</strong><sup>1</sup> According to Espen, A/B tests help us reach a <em>local</em> maximum of the user experience, but often they aren’t far-reaching enough to encompass the big picture in its entirety, effectively stopping us from reaching a <em>global</em> maximum.<sup>2</sup> That’s why in addition to A/B tests (in which microcopy and colors and positions in the layout are tested), they run so-called <em>A/Z tests</em>, testing an existing “baseline” design against completely different designs. Their differences lie not only in the shade of a button or copy, but in absolutely different layouts and visual treatments. The branding and the core principles remain the same, but pretty much everything else keeps evolving. This allows Espen and his team to reach new absolute maxima in terms of conversion and KPIs every few months.</p><p class="c-sidenote c-sidenote--right"><sup>1</sup> Jakob Nielsen wrote an article called “” back in 2005. The article highlights some of the limitations and downsides of A/B testing; most notably, that it should never be the only method used on a project &mdash; observation of user behavior often generates deeper insights.<br /><br /><sup>2</sup> Bill Buxton was probably the first to discuss this problem in his book Sketching User Experiences back in 2007. According to Bill Buxton, designers often end up with a local hill-climbing problem when the design gets plateaued on a local maximum.</p>

<p>In one of our conversations years back, Elliot Jay Stocks, who was involved in the 2012 redesign of Smashing Magazine, briefly mentioned one fine detail of his design process that stayed with me for quite some time. He said that a good design possesses one of two qualities: it’s either <em>absolutely perfect</em> in every way, with perfect alignment, sizing, and hierarchy (which is usually quite hard to achieve), or it’s <em>deliberately imperfect</em> in a few consistent ways (which is much easier to achieve). According to Elliot, in a good design there shouldn’t be anything in between. In other words, buttons should either be perfectly aligned to the grid, or not aligned at all &mdash; offset by 20–30 pixels and more. Being off just by a few pixels would feel wrong, while being off by 20–30px looks deliberate, and hence less broken.</p>

<p>So what if, instead of chasing the perfect solution for every single component, we ran and tested various expressions of our personalities? In interface design, it would mean entirely different creative directions. Perhaps a multicolumn layout with bold typography, against a geometric layout with a single accent color? What if, rather than seeking the perfect roundness of a button, you deliberately introduced slight inconsistencies? A custom animation on one of the call-to-action buttons, or a dynamic placement of an image outside of the box in which it’s usually supposed to be placed? Or perhaps rotating a subheading by 90 degrees? The personality can be expressed in many entirely different ways, so the task is to discover variations that are promising enough for testing.</p>

<p>A personality is never perfect, and so perhaps our websites shouldn’t be perfect either. What if you set up a publicly visible art board in your company, with magnets representing the qualities on one side, and magnets representing components or visual treatments on the other side, and then randomly clashed one against the other to produce a visual direction for the next A/Z test? Apply perfectionism to the level of detail required to produce deliberately imperfect designs.</p>

<p>This approach won’t always win, but complemented with A/B tests, it might bring you to new heights you wouldn’t be able to achieve otherwise. Ultimately, we want customers to fall in love with their experience and consequently the brand, to form a lasting bond. A deliberately imperfect yet humane interface can help us get there. It requires you to find just one distinguishable quality that nobody else has, and boost it up.</p>

<h3>Choose One Thing And Boost It Up</h3>

<p>In our interfaces, personality can be expressed through a <em>design signature</em> &mdash; a recurring visual treatment, the voice and tone of the copy, or an interaction pattern used consistently from one page to another. It might be tempting to explore a diverse mix of sophisticated, non-conventional treatments that would be seen in the interface miles away from the mouse cursor.  However, that’s a recipe for a disastrous experience that prioritizes a designer’s expression over users’ intentions. However bold the personality is, its design signature should remain subtle.</p>

<p>When working with Dan Mall on the Smashing redesign, one interesting detail Dan brought up at the very start of the project was the role of the signature in the final outcome. According to Dan, choosing a few distinct, competing expressions of the personality is often too much: it’s enough to choose just one little detail and boost it up all the way. In more practical terms, that means picking one pattern and using it consistently, <em>everywhere</em>: on every page, and in every user interaction. How do you find that sacred detail? You go back to the roots of the company.</p>

<p>In the very early days of Smashing Magazine, we didn’t have any branding at all. We chose a pretty random WordPress theme, placed the name in Arial, and that was it. Eventually, in early 2007 Ryan Denzel from South Africa designed Smashing Magazine’s logo, which included a letter S tilted by 11.6 degrees. Despite minor alterations in the shade and colors of the logo, we stayed true to the design for over a decade, and with the recent redesign, we weren’t considering changing it. However, when seeking a design signature that would be deeply connected with the brand, we actually took the tilting of the logo very close to our heart &mdash; from the very start.</p>

<p>Early design explorations with Andy Clarke used the tilting consistently for every single visual element on the site. This signature carried over to the final design as well. Today, all icons, author images, conference flags, job board logos, illustrations on product panels, and book covers on product pages are all consistently tilted. That tiny detail doesn’t break the experience, yet it lends a unique visual treatment to the design that’s clearly distinguishable from everything else as a result.</p>











<figure class="article__image break-out">
	<a href="https://www.smashingmagazine.com/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/53d6b1ca-7b79-41fd-81e2-2481f9821e1f/bringing-personality-back-living-style-guide.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/53d6b1ca-7b79-41fd-81e2-2481f9821e1f/bringing-personality-back-living-style-guide.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/53d6b1ca-7b79-41fd-81e2-2481f9821e1f/bringing-personality-back-living-style-guide.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/53d6b1ca-7b79-41fd-81e2-2481f9821e1f/bringing-personality-back-living-style-guide.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/53d6b1ca-7b79-41fd-81e2-2481f9821e1f/bringing-personality-back-living-style-guide.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/53d6b1ca-7b79-41fd-81e2-2481f9821e1f/bringing-personality-back-living-style-guide.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>












<figure class="article__image break-out">
	<a href="https://www.smashingmagazine.com/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f4813efa-9729-40c5-ab85-c5ea953de144/bringing-personality-back-smashing-website.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f4813efa-9729-40c5-ab85-c5ea953de144/bringing-personality-back-smashing-website.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f4813efa-9729-40c5-ab85-c5ea953de144/bringing-personality-back-smashing-website.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f4813efa-9729-40c5-ab85-c5ea953de144/bringing-personality-back-smashing-website.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f4813efa-9729-40c5-ab85-c5ea953de144/bringing-personality-back-smashing-website.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f4813efa-9729-40c5-ab85-c5ea953de144/bringing-personality-back-smashing-website.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>Admittedly, we did redesign the tilting through the process, moving away from 11.6 degrees to 11 degrees, and adding 11px roundness to all components. It was months later that the bold colors and typography and layout came into play, supporting the quirkiness and informal style of the tilted elements &mdash; all slowly crawling up into the design mock-ups eventually.</p>

<p>At this point you might be slightly worried that you don’t really have any distinctive element that could be promoted to become your signature. You might not have the tilting or a particular color palette that stands out. As it turns out, anything can become a design signature. In the next sections, we’ll explore some examples and ideas you could use for you own particular situation.</p>

<h3>Why Custom Illustrations Work Better Than Stock Photos</h3>

<p>Once the qualities of the personality have been identified, the next step is to translate these qualities into a distinct visual language. Initially it happens via color and typography, so when defining the visual style, look out for these qualities in color combinations and type families.</p>

<p>Probably the easiest way to come up with your own design signature is by using custom illustrations designed specifically for the brand. Every artist has their own unique style, and unlike stock images or stock photos that often almost enforce generic appearance into layouts, custom illustrations give a brand a unique voice and tone. You don’t need to go overboard and create dozens of illustrations; just a few would probably do. Think about replacing all the stock photos you’ve purchased with custom illustrations &mdash; this should give you a good enough baseline to start with.</p>











<figure class="article__image break-out">
	<a href="https://www.atlassian.com/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/25485b4d-94f1-4c1a-9d36-877c2ea50bce/bringing-personality-back-01-atlassian.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/25485b4d-94f1-4c1a-9d36-877c2ea50bce/bringing-personality-back-01-atlassian.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/25485b4d-94f1-4c1a-9d36-877c2ea50bce/bringing-personality-back-01-atlassian.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/25485b4d-94f1-4c1a-9d36-877c2ea50bce/bringing-personality-back-01-atlassian.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/25485b4d-94f1-4c1a-9d36-877c2ea50bce/bringing-personality-back-01-atlassian.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/25485b4d-94f1-4c1a-9d36-877c2ea50bce/bringing-personality-back-01-atlassian.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p> is a wonderful example of an illustrative style applied thoroughly and beautifully at every touchpoint of the experience. The illustrations are more approachable than stock photos. Notice, however, that they rarely appear on a plain background &mdash; they are supported by the color palette and typographic choices that complement the illustration style.</p>

<p>Why are custom illustrations not enough to stand out? Because just like many other attributes on the web, illustrative style also follows trends. Compare Atlassian’s style to ’s visual language. Yes, the fine details are different, but the pastel color combinations are similar. The illustrations from these different projects could happily coexist within one single website, and many customers wouldn’t notice a difference.</p>











<figure class="article__image break-out">
	<a href="https://slack.com/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/78cd3385-2c12-4c78-b1f3-12073d88be72/bringing-personality-back-03-slack.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/78cd3385-2c12-4c78-b1f3-12073d88be72/bringing-personality-back-03-slack.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/78cd3385-2c12-4c78-b1f3-12073d88be72/bringing-personality-back-03-slack.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/78cd3385-2c12-4c78-b1f3-12073d88be72/bringing-personality-back-03-slack.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/78cd3385-2c12-4c78-b1f3-12073d88be72/bringing-personality-back-03-slack.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/78cd3385-2c12-4c78-b1f3-12073d88be72/bringing-personality-back-03-slack.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>A distinct visual style requires further attention to other elements on the page, primarily backgrounds, typography, shapes, and layout. Notice how all of these <strong>elements play together</strong> on . Illustrations aren’t just added to a blank white canvas &mdash; they interplay with the background, text colors, and the layout.</p>











<figure class="article__image break-out">
	<a href="https://bond.backerkit.com/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/716d6cfd-7af7-44ca-8c46-373ff7a25f1e/bringing-personality-back-09-bond1.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/716d6cfd-7af7-44ca-8c46-373ff7a25f1e/bringing-personality-back-09-bond1.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/716d6cfd-7af7-44ca-8c46-373ff7a25f1e/bringing-personality-back-09-bond1.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/716d6cfd-7af7-44ca-8c46-373ff7a25f1e/bringing-personality-back-09-bond1.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/716d6cfd-7af7-44ca-8c46-373ff7a25f1e/bringing-personality-back-09-bond1.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/716d6cfd-7af7-44ca-8c46-373ff7a25f1e/bringing-personality-back-09-bond1.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>












<figure >
	<a href="https://bond.backerkit.com/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4b8c8c68-9178-4f79-b309-c595704d839d/bringing-personality-back-09-bond2.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4b8c8c68-9178-4f79-b309-c595704d839d/bringing-personality-back-09-bond2.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4b8c8c68-9178-4f79-b309-c595704d839d/bringing-personality-back-09-bond2.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4b8c8c68-9178-4f79-b309-c595704d839d/bringing-personality-back-09-bond2.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4b8c8c68-9178-4f79-b309-c595704d839d/bringing-personality-back-09-bond2.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4b8c8c68-9178-4f79-b309-c595704d839d/bringing-personality-back-09-bond2.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>












<figure >
	<a href="https://bond.backerkit.com/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/954f0eff-c2d3-4471-8542-8022650d1e06/bringing-personality-back-09-bond3.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/954f0eff-c2d3-4471-8542-8022650d1e06/bringing-personality-back-09-bond3.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/954f0eff-c2d3-4471-8542-8022650d1e06/bringing-personality-back-09-bond3.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/954f0eff-c2d3-4471-8542-8022650d1e06/bringing-personality-back-09-bond3.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/954f0eff-c2d3-4471-8542-8022650d1e06/bringing-personality-back-09-bond3.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/954f0eff-c2d3-4471-8542-8022650d1e06/bringing-personality-back-09-bond3.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>












<figure >
	<a href="https://bond.backerkit.com/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3bf3b93e-e600-4f8a-88ee-3d729e14a417/bringing-personality-back-09-bond4.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3bf3b93e-e600-4f8a-88ee-3d729e14a417/bringing-personality-back-09-bond4.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3bf3b93e-e600-4f8a-88ee-3d729e14a417/bringing-personality-back-09-bond4.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3bf3b93e-e600-4f8a-88ee-3d729e14a417/bringing-personality-back-09-bond4.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3bf3b93e-e600-4f8a-88ee-3d729e14a417/bringing-personality-back-09-bond4.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3bf3b93e-e600-4f8a-88ee-3d729e14a417/bringing-personality-back-09-bond4.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p> uses a collage-like style for all its illustrations on landing pages and help pages. The key is that illustrations are used consistently across pages. They might not make sense to every visitor, but they contribute to the unique visual appearance of the brand.</p>











<figure class="article__image break-out">
	<a href="https://medium.com/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/79807bc1-4e89-4283-a413-2e5ef67c4b49/bringing-personality-back-25-medium-1.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/79807bc1-4e89-4283-a413-2e5ef67c4b49/bringing-personality-back-25-medium-1.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/79807bc1-4e89-4283-a413-2e5ef67c4b49/bringing-personality-back-25-medium-1.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/79807bc1-4e89-4283-a413-2e5ef67c4b49/bringing-personality-back-25-medium-1.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/79807bc1-4e89-4283-a413-2e5ef67c4b49/bringing-personality-back-25-medium-1.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/79807bc1-4e89-4283-a413-2e5ef67c4b49/bringing-personality-back-25-medium-1.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>












<figure >
	<a href="https://medium.com/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1eeee836-5acc-48b3-bec5-2d82f9adc7ba/bringing-personality-back-25-medium-2.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1eeee836-5acc-48b3-bec5-2d82f9adc7ba/bringing-personality-back-25-medium-2.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1eeee836-5acc-48b3-bec5-2d82f9adc7ba/bringing-personality-back-25-medium-2.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1eeee836-5acc-48b3-bec5-2d82f9adc7ba/bringing-personality-back-25-medium-2.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1eeee836-5acc-48b3-bec5-2d82f9adc7ba/bringing-personality-back-25-medium-2.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1eeee836-5acc-48b3-bec5-2d82f9adc7ba/bringing-personality-back-25-medium-2.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>












<figure >
	<a href="https://medium.com/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/66fcdfb6-4566-4530-8476-4e3399e12976/bringing-personality-back-25-medium-3.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/66fcdfb6-4566-4530-8476-4e3399e12976/bringing-personality-back-25-medium-3.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/66fcdfb6-4566-4530-8476-4e3399e12976/bringing-personality-back-25-medium-3.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/66fcdfb6-4566-4530-8476-4e3399e12976/bringing-personality-back-25-medium-3.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/66fcdfb6-4566-4530-8476-4e3399e12976/bringing-personality-back-25-medium-3.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/66fcdfb6-4566-4530-8476-4e3399e12976/bringing-personality-back-25-medium-3.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>












<figure >
	<a href="https://medium.com/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8ef59cef-1818-48a2-9b93-5fab019a300d/bringing-personality-back-25-medium-4.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8ef59cef-1818-48a2-9b93-5fab019a300d/bringing-personality-back-25-medium-4.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8ef59cef-1818-48a2-9b93-5fab019a300d/bringing-personality-back-25-medium-4.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8ef59cef-1818-48a2-9b93-5fab019a300d/bringing-personality-back-25-medium-4.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8ef59cef-1818-48a2-9b93-5fab019a300d/bringing-personality-back-25-medium-4.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8ef59cef-1818-48a2-9b93-5fab019a300d/bringing-personality-back-25-medium-4.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>Health insurance is a very competitive and not  particularly friendly nor transparent environment for citizens and business. With custom illustrations, subtle animated GIFs, and straightforward copywriting, , a newcomer to the industry, appears more approachable and relatable.</p>











<figure class="article__image break-out">
	<a href="https://medium.com/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/07ca52ae-a5a1-4192-a8ff-8c8a78982809/bringing-personality-back-26-oscar-3.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/07ca52ae-a5a1-4192-a8ff-8c8a78982809/bringing-personality-back-26-oscar-3.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/07ca52ae-a5a1-4192-a8ff-8c8a78982809/bringing-personality-back-26-oscar-3.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/07ca52ae-a5a1-4192-a8ff-8c8a78982809/bringing-personality-back-26-oscar-3.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/07ca52ae-a5a1-4192-a8ff-8c8a78982809/bringing-personality-back-26-oscar-3.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/07ca52ae-a5a1-4192-a8ff-8c8a78982809/bringing-personality-back-26-oscar-3.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>












<figure >
	<a href="https://medium.com/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1211bc11-b2ef-4e55-ae75-063d300c92a7/bringing-personality-back-26-oscar-1.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1211bc11-b2ef-4e55-ae75-063d300c92a7/bringing-personality-back-26-oscar-1.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1211bc11-b2ef-4e55-ae75-063d300c92a7/bringing-personality-back-26-oscar-1.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1211bc11-b2ef-4e55-ae75-063d300c92a7/bringing-personality-back-26-oscar-1.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1211bc11-b2ef-4e55-ae75-063d300c92a7/bringing-personality-back-26-oscar-1.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1211bc11-b2ef-4e55-ae75-063d300c92a7/bringing-personality-back-26-oscar-1.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>












<figure >
	<a href="https://medium.com/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/838df77b-3351-4964-85ae-9a66a223c496/bringing-personality-back-26-oscar-2.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/838df77b-3351-4964-85ae-9a66a223c496/bringing-personality-back-26-oscar-2.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/838df77b-3351-4964-85ae-9a66a223c496/bringing-personality-back-26-oscar-2.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/838df77b-3351-4964-85ae-9a66a223c496/bringing-personality-back-26-oscar-2.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/838df77b-3351-4964-85ae-9a66a223c496/bringing-personality-back-26-oscar-2.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/838df77b-3351-4964-85ae-9a66a223c496/bringing-personality-back-26-oscar-2.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>












<figure >
	<a href="https://medium.com/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/73da17ff-a007-428d-a4c9-05d43bff13dc/bringing-personality-back-26-oscar-4.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/73da17ff-a007-428d-a4c9-05d43bff13dc/bringing-personality-back-26-oscar-4.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/73da17ff-a007-428d-a4c9-05d43bff13dc/bringing-personality-back-26-oscar-4.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/73da17ff-a007-428d-a4c9-05d43bff13dc/bringing-personality-back-26-oscar-4.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/73da17ff-a007-428d-a4c9-05d43bff13dc/bringing-personality-back-26-oscar-4.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/73da17ff-a007-428d-a4c9-05d43bff13dc/bringing-personality-back-26-oscar-4.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p> is a conference website with vivid color combinations and background, and boxy components designed as if they were <strong>three-dimensional</strong>. This is enough to set the design apart. The visual treatment produces depth, which is used for speakers, talks, and main navigation.</p>











<figure class="article__image break-out">
	<a href="https://webconf.asia/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7ea48e90-9a3e-4ea6-b606-45266f0184ee/bringing-personality-back-05-webconf1.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7ea48e90-9a3e-4ea6-b606-45266f0184ee/bringing-personality-back-05-webconf1.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7ea48e90-9a3e-4ea6-b606-45266f0184ee/bringing-personality-back-05-webconf1.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7ea48e90-9a3e-4ea6-b606-45266f0184ee/bringing-personality-back-05-webconf1.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7ea48e90-9a3e-4ea6-b606-45266f0184ee/bringing-personality-back-05-webconf1.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7ea48e90-9a3e-4ea6-b606-45266f0184ee/bringing-personality-back-05-webconf1.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>












<figure class="article__image break-out">
	<a href="https://webconf.asia/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6d3c2bc0-46a8-4029-aecb-3fd857574f73/bringing-personality-back-05-webconf2.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6d3c2bc0-46a8-4029-aecb-3fd857574f73/bringing-personality-back-05-webconf2.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6d3c2bc0-46a8-4029-aecb-3fd857574f73/bringing-personality-back-05-webconf2.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6d3c2bc0-46a8-4029-aecb-3fd857574f73/bringing-personality-back-05-webconf2.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6d3c2bc0-46a8-4029-aecb-3fd857574f73/bringing-personality-back-05-webconf2.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6d3c2bc0-46a8-4029-aecb-3fd857574f73/bringing-personality-back-05-webconf2.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p> uses <strong>slanted shapes</strong> and compositions consistently on call-to-action buttons, in the navigation, and even in the quantity selector on the product page. That’s their design signature. Notice how even micro-components such as product labels use the same pattern.</p>











<figure class="article__image break-out">
	<a href="http://www.bandenjager.nl/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/639cad11-e570-49e8-a14b-ba9306ad214e/bringing-personality-back-06-banden1.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/639cad11-e570-49e8-a14b-ba9306ad214e/bringing-personality-back-06-banden1.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/639cad11-e570-49e8-a14b-ba9306ad214e/bringing-personality-back-06-banden1.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/639cad11-e570-49e8-a14b-ba9306ad214e/bringing-personality-back-06-banden1.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/639cad11-e570-49e8-a14b-ba9306ad214e/bringing-personality-back-06-banden1.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/639cad11-e570-49e8-a14b-ba9306ad214e/bringing-personality-back-06-banden1.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>












<figure class="article__image break-out">
	<a href="http://www.bandenjager.nl/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6bd05d3f-ca15-49ac-8873-8a93f21e1db2/bringing-personality-back-07-banden1.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6bd05d3f-ca15-49ac-8873-8a93f21e1db2/bringing-personality-back-07-banden1.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6bd05d3f-ca15-49ac-8873-8a93f21e1db2/bringing-personality-back-07-banden1.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6bd05d3f-ca15-49ac-8873-8a93f21e1db2/bringing-personality-back-07-banden1.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6bd05d3f-ca15-49ac-8873-8a93f21e1db2/bringing-personality-back-07-banden1.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6bd05d3f-ca15-49ac-8873-8a93f21e1db2/bringing-personality-back-07-banden1.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p> uses a tree shape… everywhere, accompanying custom illustrations that highlight the ongoing activities of the foundation.</p>











<figure class="article__image break-out">
	<a href="https://marumarumarumori.jp/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/39694cce-4d61-4add-9b2c-32758ea29b86/bringing-personality-back-08-marumari.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/39694cce-4d61-4add-9b2c-32758ea29b86/bringing-personality-back-08-marumari.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/39694cce-4d61-4add-9b2c-32758ea29b86/bringing-personality-back-08-marumari.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/39694cce-4d61-4add-9b2c-32758ea29b86/bringing-personality-back-08-marumari.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/39694cce-4d61-4add-9b2c-32758ea29b86/bringing-personality-back-08-marumari.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/39694cce-4d61-4add-9b2c-32758ea29b86/bringing-personality-back-08-marumari.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p> lets its visitors explore cities with an interactive guide, complemented with videos and photos. Every single city has its own signature which is a wavy horizontal line, outlining that city’s most important landmark. The cities differ in the curves of the lines, and the design uses lines as a signature for animations, transitions, and arrangement of items in the layout.</p>











<figure class="article__image break-out">
	<a href="http://www.storytrail.co/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1e12b700-e210-45db-84da-df4d04567181/bringing-personality-back-08-storytrail1.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1e12b700-e210-45db-84da-df4d04567181/bringing-personality-back-08-storytrail1.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1e12b700-e210-45db-84da-df4d04567181/bringing-personality-back-08-storytrail1.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1e12b700-e210-45db-84da-df4d04567181/bringing-personality-back-08-storytrail1.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1e12b700-e210-45db-84da-df4d04567181/bringing-personality-back-08-storytrail1.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1e12b700-e210-45db-84da-df4d04567181/bringing-personality-back-08-storytrail1.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>












<figure class="article__image break-out">
	<a href="http://www.storytrail.co/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/940c2270-3373-4891-a425-30e40c4b050f/bringing-personality-back-08-storytrail2.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/940c2270-3373-4891-a425-30e40c4b050f/bringing-personality-back-08-storytrail2.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/940c2270-3373-4891-a425-30e40c4b050f/bringing-personality-back-08-storytrail2.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/940c2270-3373-4891-a425-30e40c4b050f/bringing-personality-back-08-storytrail2.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/940c2270-3373-4891-a425-30e40c4b050f/bringing-personality-back-08-storytrail2.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/940c2270-3373-4891-a425-30e40c4b050f/bringing-personality-back-08-storytrail2.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p> beautifully describes the underlying principle of Haufe’s dynamic grid.</p>











<figure class="article__image break-out">
	<a href="https://www.haufe.com/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/722bc7d2-9aea-464d-95d9-6008c7c651c4/bringing-personality-back-32-haufe-3.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/722bc7d2-9aea-464d-95d9-6008c7c651c4/bringing-personality-back-32-haufe-3.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/722bc7d2-9aea-464d-95d9-6008c7c651c4/bringing-personality-back-32-haufe-3.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/722bc7d2-9aea-464d-95d9-6008c7c651c4/bringing-personality-back-32-haufe-3.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/722bc7d2-9aea-464d-95d9-6008c7c651c4/bringing-personality-back-32-haufe-3.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/722bc7d2-9aea-464d-95d9-6008c7c651c4/bringing-personality-back-32-haufe-3.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>












<figure >
	<a href="https://www.haufe.com/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/60472218-d3b6-49a1-92cb-831e9a252a4f/bringing-personality-back-32-haufe-4.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/60472218-d3b6-49a1-92cb-831e9a252a4f/bringing-personality-back-32-haufe-4.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/60472218-d3b6-49a1-92cb-831e9a252a4f/bringing-personality-back-32-haufe-4.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/60472218-d3b6-49a1-92cb-831e9a252a4f/bringing-personality-back-32-haufe-4.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/60472218-d3b6-49a1-92cb-831e9a252a4f/bringing-personality-back-32-haufe-4.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/60472218-d3b6-49a1-92cb-831e9a252a4f/bringing-personality-back-32-haufe-4.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>












<figure >
	<a href="https://www.haufe.com/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/138e1313-8257-48ef-8f25-84788bf76e0a/bringing-personality-back-32-haufe-5.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/138e1313-8257-48ef-8f25-84788bf76e0a/bringing-personality-back-32-haufe-5.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/138e1313-8257-48ef-8f25-84788bf76e0a/bringing-personality-back-32-haufe-5.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/138e1313-8257-48ef-8f25-84788bf76e0a/bringing-personality-back-32-haufe-5.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/138e1313-8257-48ef-8f25-84788bf76e0a/bringing-personality-back-32-haufe-5.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/138e1313-8257-48ef-8f25-84788bf76e0a/bringing-personality-back-32-haufe-5.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>












<figure >
	<a href="https://www.haufe.com/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a35e8438-7819-4d17-96ac-4b3d339c6507/bringing-personality-back-14-haufe3.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a35e8438-7819-4d17-96ac-4b3d339c6507/bringing-personality-back-14-haufe3.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a35e8438-7819-4d17-96ac-4b3d339c6507/bringing-personality-back-14-haufe3.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a35e8438-7819-4d17-96ac-4b3d339c6507/bringing-personality-back-14-haufe3.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a35e8438-7819-4d17-96ac-4b3d339c6507/bringing-personality-back-14-haufe3.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a35e8438-7819-4d17-96ac-4b3d339c6507/bringing-personality-back-14-haufe3.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>












<figure >
	<a href="https://www.haufe.com/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4df8d7d4-3da6-42d9-bd97-08719cb4dd90/bringing-personality-back-32-haufe-1.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4df8d7d4-3da6-42d9-bd97-08719cb4dd90/bringing-personality-back-32-haufe-1.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4df8d7d4-3da6-42d9-bd97-08719cb4dd90/bringing-personality-back-32-haufe-1.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4df8d7d4-3da6-42d9-bd97-08719cb4dd90/bringing-personality-back-32-haufe-1.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4df8d7d4-3da6-42d9-bd97-08719cb4dd90/bringing-personality-back-32-haufe-1.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4df8d7d4-3da6-42d9-bd97-08719cb4dd90/bringing-personality-back-32-haufe-1.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>












<figure >
	<a href="https://www.haufe.com/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b938dc21-217b-4986-b398-fb1243e7efae/bringing-personality-back-32-haufe-2.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b938dc21-217b-4986-b398-fb1243e7efae/bringing-personality-back-32-haufe-2.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b938dc21-217b-4986-b398-fb1243e7efae/bringing-personality-back-32-haufe-2.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b938dc21-217b-4986-b398-fb1243e7efae/bringing-personality-back-32-haufe-2.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b938dc21-217b-4986-b398-fb1243e7efae/bringing-personality-back-32-haufe-2.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b938dc21-217b-4986-b398-fb1243e7efae/bringing-personality-back-32-haufe-2.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>Another way of drawing attention is by adding randomness to your compositions.  contains illustrations split into three vertical parts, randomly offset horizontally and colored with a set of predefined colors. It’s really not that difficult to add a little bit of personality to stand out. It’s a nice example of introducing some chaos in the design language by combining predictable parts of the system in seemingly random, unpredictable ways.</p>











<figure class="article__image break-out">
	<a href="http://rc3.me">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d78e4545-54b0-4c89-90c5-6ae860f40854/bringing-personality-back-18-rc31.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d78e4545-54b0-4c89-90c5-6ae860f40854/bringing-personality-back-18-rc31.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d78e4545-54b0-4c89-90c5-6ae860f40854/bringing-personality-back-18-rc31.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d78e4545-54b0-4c89-90c5-6ae860f40854/bringing-personality-back-18-rc31.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d78e4545-54b0-4c89-90c5-6ae860f40854/bringing-personality-back-18-rc31.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d78e4545-54b0-4c89-90c5-6ae860f40854/bringing-personality-back-18-rc31.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p> also adds some randomness to her portfolio. The layout changes completely between different breakpoints, creating a totally different experience on mobile and desktop devices. Even the favicon changes dynamically as well.</p>











<figure class="article__image break-out">
	<a href="https://lynnandtonic.com/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ca13f770-45bf-4062-8494-7e77c3172428/bringing-personality-back-19-lynn1.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ca13f770-45bf-4062-8494-7e77c3172428/bringing-personality-back-19-lynn1.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ca13f770-45bf-4062-8494-7e77c3172428/bringing-personality-back-19-lynn1.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ca13f770-45bf-4062-8494-7e77c3172428/bringing-personality-back-19-lynn1.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ca13f770-45bf-4062-8494-7e77c3172428/bringing-personality-back-19-lynn1.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ca13f770-45bf-4062-8494-7e77c3172428/bringing-personality-back-19-lynn1.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>When considering the visual direction of a site, it’s a good idea to consider custom illustration style, backgrounds, typography, and shapes. Establish strong connections between all of these attributes by reusing design decisions, such as the choice of colors and spacing. While doing so, of course, it wouldn’t hurt avoiding predictable options used widely everywhere else. One of the effective ways to achieve this is by keeping tabs on ongoing design trends, then pick the most prevalent one and… <em>smash it to pieces</em>.</p>

<h3>Pick A Trend And Smash It To Pieces</h3>

<p>When talking about great design, Yves Saint-Laurent, a well-known French fashion designer, once noted that “Fashions fade; style is eternal.” According to Saint-Laurent, to create timeless designs it’s important to take note of trends, yet serve an <em>interpretation</em> of trends through the lens of your own personal style. That’s not what we usually see on the web.</p>

<p class="c-pre-sidenote--left">It’s almost ironic that it has become trendy to dislike trends these days, and for good reason: usually their primary purpose is visual embellishment, rather than driving a designer’s intent, and often they don’t add much to the experience beyond friction, confusion, and fancy whistles and bells. No wonder then that designers have started to fight back with “” &mdash; websites that aim to exhibit the essence of a website in its unstructured form, exposing the website’s functions to extremes.<sup>3</sup></p><p class="c-sidenote c-sidenote--right"><sup>3</sup> It’s worth noting that brutalism in architecture is characterized by unconcerned aesthetics, not intentionally broken aesthetics. When applied to web design, this style often goes along with deliberately broken design conventions and guiding principles.</p>

<p>While doing so, designers often deliberately break design patterns, usability practices, and design trends. At first glance they might appear as designs created with the sole purpose of being different, but because they have a striking personality, they draw attention to themselves. Admittedly, sometimes they seem to be too far-fetched in how they deliberately turn their back on well-established design principles. Not everybody can afford it, and not everybody would feel comfortable connecting such non-conventional aesthetics to their brand.</p>￼











<figure class="article__image break-out">
	<a href="https://www.bloomberg.com/features/elon-musk-goals/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/72c11057-88f4-45f5-8ebe-be8a4dcc3408/bringing-personality-back-10-tesla1.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/72c11057-88f4-45f5-8ebe-be8a4dcc3408/bringing-personality-back-10-tesla1.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/72c11057-88f4-45f5-8ebe-be8a4dcc3408/bringing-personality-back-10-tesla1.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/72c11057-88f4-45f5-8ebe-be8a4dcc3408/bringing-personality-back-10-tesla1.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/72c11057-88f4-45f5-8ebe-be8a4dcc3408/bringing-personality-back-10-tesla1.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/72c11057-88f4-45f5-8ebe-be8a4dcc3408/bringing-personality-back-10-tesla1.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>












<figure class="article__image break-out">
	<a href="https://www.bloomberg.com/features/elon-musk-goals/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/24dec85d-fc97-46c1-a422-6c00993ad88f/bringing-personality-back-10-tesla2.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/24dec85d-fc97-46c1-a422-6c00993ad88f/bringing-personality-back-10-tesla2.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/24dec85d-fc97-46c1-a422-6c00993ad88f/bringing-personality-back-10-tesla2.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/24dec85d-fc97-46c1-a422-6c00993ad88f/bringing-personality-back-10-tesla2.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/24dec85d-fc97-46c1-a422-6c00993ad88f/bringing-personality-back-10-tesla2.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/24dec85d-fc97-46c1-a422-6c00993ad88f/bringing-personality-back-10-tesla2.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Brutalist designs. 
		</figcaption>
	
</figure>


<p>A slightly more pragmatic strategy, of course, lives somewhere between generic designs and brutalist designs. To get there, you could pick a trend, find a unique perspective and apply your personality to it. For example, if you see many websites using smooth and silky animations, think about how they would fit into your story, and find the twist that would enrich it, and make it more personal. Break down the trend into pieces to understand its mechanics and what’s happening behind the scenes, then twist some parts of it, repackage, and integrate into your design.</p>











<figure class="article__image break-out">
	<a href="https://dropbox.design/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/621a4367-4c5d-42ef-b1dc-3c1f20dbf820/bringing-personality-back-11-dropbox3.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/621a4367-4c5d-42ef-b1dc-3c1f20dbf820/bringing-personality-back-11-dropbox3.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/621a4367-4c5d-42ef-b1dc-3c1f20dbf820/bringing-personality-back-11-dropbox3.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/621a4367-4c5d-42ef-b1dc-3c1f20dbf820/bringing-personality-back-11-dropbox3.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/621a4367-4c5d-42ef-b1dc-3c1f20dbf820/bringing-personality-back-11-dropbox3.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/621a4367-4c5d-42ef-b1dc-3c1f20dbf820/bringing-personality-back-11-dropbox3.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>












<figure class="article__image break-out">
	<a href="https://dropbox.design/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4919c6c5-8869-4e9c-817e-9ed68eb94dce/bringing-personality-back-11-dropbox2.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4919c6c5-8869-4e9c-817e-9ed68eb94dce/bringing-personality-back-11-dropbox2.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4919c6c5-8869-4e9c-817e-9ed68eb94dce/bringing-personality-back-11-dropbox2.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4919c6c5-8869-4e9c-817e-9ed68eb94dce/bringing-personality-back-11-dropbox2.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4919c6c5-8869-4e9c-817e-9ed68eb94dce/bringing-personality-back-11-dropbox2.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4919c6c5-8869-4e9c-817e-9ed68eb94dce/bringing-personality-back-11-dropbox2.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>












<figure class="article__image break-out">
	<a href="https://dropbox.design/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5b89d3b9-2230-4307-b6cb-9d3f9166bb19/bringing-personality-back-11-dropbox1.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5b89d3b9-2230-4307-b6cb-9d3f9166bb19/bringing-personality-back-11-dropbox1.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5b89d3b9-2230-4307-b6cb-9d3f9166bb19/bringing-personality-back-11-dropbox1.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5b89d3b9-2230-4307-b6cb-9d3f9166bb19/bringing-personality-back-11-dropbox1.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5b89d3b9-2230-4307-b6cb-9d3f9166bb19/bringing-personality-back-11-dropbox1.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5b89d3b9-2230-4307-b6cb-9d3f9166bb19/bringing-personality-back-11-dropbox1.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>Instead of using bouncy animations, you could introduce an <strong>artificial delay</strong>, effectively slowing down the appearance of items on the page. If most profile images you see have a perfect circular shape, try to come up with another shape that would work well for you to display avatars. If most photos are rectangular, think of another shape that might do the job well.</p>











<figure class="article__image break-out">
	<a href="http://loflorecords.com/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1e10a7b9-6219-4ddd-932a-5ab6afdaab9b/bringing-personality-back-12-loflo1.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1e10a7b9-6219-4ddd-932a-5ab6afdaab9b/bringing-personality-back-12-loflo1.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1e10a7b9-6219-4ddd-932a-5ab6afdaab9b/bringing-personality-back-12-loflo1.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1e10a7b9-6219-4ddd-932a-5ab6afdaab9b/bringing-personality-back-12-loflo1.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1e10a7b9-6219-4ddd-932a-5ab6afdaab9b/bringing-personality-back-12-loflo1.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1e10a7b9-6219-4ddd-932a-5ab6afdaab9b/bringing-personality-back-12-loflo1.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>












<figure class="article__image break-out">
	<a href="http://loflorecords.com/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1cb2e8f9-140a-42ee-9d4e-50059754f673/bringing-personality-back-12-loflo2.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1cb2e8f9-140a-42ee-9d4e-50059754f673/bringing-personality-back-12-loflo2.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1cb2e8f9-140a-42ee-9d4e-50059754f673/bringing-personality-back-12-loflo2.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1cb2e8f9-140a-42ee-9d4e-50059754f673/bringing-personality-back-12-loflo2.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1cb2e8f9-140a-42ee-9d4e-50059754f673/bringing-personality-back-12-loflo2.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1cb2e8f9-140a-42ee-9d4e-50059754f673/bringing-personality-back-12-loflo2.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>Instead of using off-canvas transitions, think about a particular kind of transition or animation that would best reflect your brand. For more corporate entities, a fast-paced transition might work best; for creative projects, a slightly more playful and slow transition might be a better fit.  is a wonderful example of the latter. If all transitions were removed, the portfolio website would look pretty much like every other portfolio out there.</p>











<figure class="article__image break-out">
	<a href="https://waaark.com/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/41667107-3639-4b5a-bc19-4bd75b11e185/bringing-personality-back-16-waaark1.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/41667107-3639-4b5a-bc19-4bd75b11e185/bringing-personality-back-16-waaark1.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/41667107-3639-4b5a-bc19-4bd75b11e185/bringing-personality-back-16-waaark1.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/41667107-3639-4b5a-bc19-4bd75b11e185/bringing-personality-back-16-waaark1.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/41667107-3639-4b5a-bc19-4bd75b11e185/bringing-personality-back-16-waaark1.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/41667107-3639-4b5a-bc19-4bd75b11e185/bringing-personality-back-16-waaark1.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>












<figure class="article__image break-out">
	<a href="https://waaark.com/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/607e532c-fbc6-41de-b2d6-f6cb99234673/bringing-personality-back-16-waaark2.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/607e532c-fbc6-41de-b2d6-f6cb99234673/bringing-personality-back-16-waaark2.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/607e532c-fbc6-41de-b2d6-f6cb99234673/bringing-personality-back-16-waaark2.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/607e532c-fbc6-41de-b2d6-f6cb99234673/bringing-personality-back-16-waaark2.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/607e532c-fbc6-41de-b2d6-f6cb99234673/bringing-personality-back-16-waaark2.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/607e532c-fbc6-41de-b2d6-f6cb99234673/bringing-personality-back-16-waaark2.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>












<figure class="article__image break-out">
	<a href="https://waaark.com/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e5e3f334-4888-48db-b136-6b851b716e2e/bringing-personality-back-16-waaark3.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e5e3f334-4888-48db-b136-6b851b716e2e/bringing-personality-back-16-waaark3.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e5e3f334-4888-48db-b136-6b851b716e2e/bringing-personality-back-16-waaark3.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e5e3f334-4888-48db-b136-6b851b716e2e/bringing-personality-back-16-waaark3.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e5e3f334-4888-48db-b136-6b851b716e2e/bringing-personality-back-16-waaark3.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e5e3f334-4888-48db-b136-6b851b716e2e/bringing-personality-back-16-waaark3.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p> uses a short and subtle geometric animation to highlight the featured article on the site. Foreground and background images are a bit offset and animated, with a geometric shape in the background and a story preview in the foreground. That’s enough to give the experience some personality.</p>











<figure class="article__image break-out">
	<a href="http://implementconsultinggroup.com/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/165e904a-6723-4f8f-af79-f49187e9a0d3/bringing-personality-back-33-investment-1.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/165e904a-6723-4f8f-af79-f49187e9a0d3/bringing-personality-back-33-investment-1.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/165e904a-6723-4f8f-af79-f49187e9a0d3/bringing-personality-back-33-investment-1.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/165e904a-6723-4f8f-af79-f49187e9a0d3/bringing-personality-back-33-investment-1.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/165e904a-6723-4f8f-af79-f49187e9a0d3/bringing-personality-back-33-investment-1.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/165e904a-6723-4f8f-af79-f49187e9a0d3/bringing-personality-back-33-investment-1.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>












<figure class="article__image break-out">
	<a href="http://implementconsultinggroup.com/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/110e2b45-566d-4123-87ce-383ee7ca92c2/bringing-personality-back-33-investment-4.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/110e2b45-566d-4123-87ce-383ee7ca92c2/bringing-personality-back-33-investment-4.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/110e2b45-566d-4123-87ce-383ee7ca92c2/bringing-personality-back-33-investment-4.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/110e2b45-566d-4123-87ce-383ee7ca92c2/bringing-personality-back-33-investment-4.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/110e2b45-566d-4123-87ce-383ee7ca92c2/bringing-personality-back-33-investment-4.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/110e2b45-566d-4123-87ce-383ee7ca92c2/bringing-personality-back-33-investment-4.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>












<figure class="article__image break-out">
	<a href="http://implementconsultinggroup.com/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fb0ea17b-1694-4871-9d08-7bfdb3c35583/bringing-personality-back-33-investment-2.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fb0ea17b-1694-4871-9d08-7bfdb3c35583/bringing-personality-back-33-investment-2.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fb0ea17b-1694-4871-9d08-7bfdb3c35583/bringing-personality-back-33-investment-2.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fb0ea17b-1694-4871-9d08-7bfdb3c35583/bringing-personality-back-33-investment-2.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fb0ea17b-1694-4871-9d08-7bfdb3c35583/bringing-personality-back-33-investment-2.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fb0ea17b-1694-4871-9d08-7bfdb3c35583/bringing-personality-back-33-investment-2.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>Imagine for a second that you have to redesign your ongoing project, but can’t use any basic shapes such as circles, rectangles, or triangles. What would you choose? We all know there is an infinite amount of options, but why is it then that so often we are constrained by highly predictable and heavily used choices? What is neither a circle nor a rectangle nor a triangle? Well, slanted or tilted elements aren’t. Neither are letters and large typography. Nor are custom responsive illustrations or iconography. Nor whitespace, audio, and video. Nor transitions and animations. Nor pretty much any other shape created via a polygon, with content embedded via SVG masks.</p>











<figure class="article__image break-out">
	<a href="http://www.tpsre.ru/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2e8002d4-f656-4a9c-bd53-274681103d38/bringing-personality-back-13-tpsre1.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2e8002d4-f656-4a9c-bd53-274681103d38/bringing-personality-back-13-tpsre1.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2e8002d4-f656-4a9c-bd53-274681103d38/bringing-personality-back-13-tpsre1.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2e8002d4-f656-4a9c-bd53-274681103d38/bringing-personality-back-13-tpsre1.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2e8002d4-f656-4a9c-bd53-274681103d38/bringing-personality-back-13-tpsre1.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2e8002d4-f656-4a9c-bd53-274681103d38/bringing-personality-back-13-tpsre1.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>












<figure class="article__image break-out">
	<a href="http://www.tpsre.ru/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f2e8ae57-b56d-4b19-9e9d-7528b7b3b62a/bringing-personality-back-13-tpsre2.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f2e8ae57-b56d-4b19-9e9d-7528b7b3b62a/bringing-personality-back-13-tpsre2.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f2e8ae57-b56d-4b19-9e9d-7528b7b3b62a/bringing-personality-back-13-tpsre2.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f2e8ae57-b56d-4b19-9e9d-7528b7b3b62a/bringing-personality-back-13-tpsre2.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f2e8ae57-b56d-4b19-9e9d-7528b7b3b62a/bringing-personality-back-13-tpsre2.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f2e8ae57-b56d-4b19-9e9d-7528b7b3b62a/bringing-personality-back-13-tpsre2.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>












<figure class="article__image break-out">
	<a href="http://www.tpsre.ru/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3fe28a1a-f2c9-401d-b674-a5b389d3eea3/bringing-personality-back-13-tpsre3.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3fe28a1a-f2c9-401d-b674-a5b389d3eea3/bringing-personality-back-13-tpsre3.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3fe28a1a-f2c9-401d-b674-a5b389d3eea3/bringing-personality-back-13-tpsre3.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3fe28a1a-f2c9-401d-b674-a5b389d3eea3/bringing-personality-back-13-tpsre3.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3fe28a1a-f2c9-401d-b674-a5b389d3eea3/bringing-personality-back-13-tpsre3.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/3fe28a1a-f2c9-401d-b674-a5b389d3eea3/bringing-personality-back-13-tpsre3.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p> is a network of decentralized markets and communities. The site uses custom shapes, smooth transitions, and animations to provide a distinct experience. No rectangles or circles. And notice how well the colors, background images, and typography work together on the site.</p>











<figure class="article__image break-out">
	<a href="https://district0x.io/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4f82f3eb-dd00-4808-9353-e901dec2e669/bringing-personality-back-15-district0x1.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4f82f3eb-dd00-4808-9353-e901dec2e669/bringing-personality-back-15-district0x1.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4f82f3eb-dd00-4808-9353-e901dec2e669/bringing-personality-back-15-district0x1.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4f82f3eb-dd00-4808-9353-e901dec2e669/bringing-personality-back-15-district0x1.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4f82f3eb-dd00-4808-9353-e901dec2e669/bringing-personality-back-15-district0x1.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4f82f3eb-dd00-4808-9353-e901dec2e669/bringing-personality-back-15-district0x1.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>












<figure class="article__image break-out">
	<a href="https://district0x.io/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6aa962d3-e2cb-450f-95aa-465b70324e6e/bringing-personality-back-15-district0x2.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6aa962d3-e2cb-450f-95aa-465b70324e6e/bringing-personality-back-15-district0x2.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6aa962d3-e2cb-450f-95aa-465b70324e6e/bringing-personality-back-15-district0x2.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6aa962d3-e2cb-450f-95aa-465b70324e6e/bringing-personality-back-15-district0x2.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6aa962d3-e2cb-450f-95aa-465b70324e6e/bringing-personality-back-15-district0x2.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6aa962d3-e2cb-450f-95aa-465b70324e6e/bringing-personality-back-15-district0x2.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>It’s not that all basic shapes should be ignored and dismissed from now on, of course. Avoiding basic shapes deliberately is one of the very first exercises we do when we try to come up with a slightly more original art direction. Once you’ve come up with a decent idea without basic shapes, you can start bringing them back sparingly when necessary. Chances are high, however, that you might be able to get away without them altogether.</p>

<h3 id="do-make-people-think">Do Make People Think</h3>

<p>Why is it that when we are puzzling our way around a foreign city and a souvenir shop owner is desperately trying to catch our attention on the street and push a sale, we pass by in haste; yet we slowly walk into a beautifully designed souvenir store that is silent and humble just around the corner? Perhaps it’s because we seek authentic, honest, and respectful experiences, and tend to ignore everything that doesn’t fit the bill. In his fantastic book Blink, Malcolm Gladwell outlined an interesting phenomenon related to how humans value their experiences.</p>

<p>According to Gladwell, we tend to be more satisfied with our experiences when we feel valued, listened to, and understood. Doctors who take a disproportionate amount of time listening, asking questions, and taking notes with their patients tend to get significantly better reviews and higher ratings despite the fact that other doctors might be as proficient and knowledgeable. They might jump to correct conclusions faster, yet their efficiency doesn’t elicit trust and connection in their patients. Of course, primarily we want the problem to be solved, but we also love falling in love with a charming personality, wisdom, expertise, and human kindness.</p>

<p>We know by now that we can enable human connections by embedding compassion into our interfaces. However, these connections don’t just happen overnight &mdash; they take time. But where does it leave us in the age of instant gratification and invisible interfaces, when it has become the essence of our job to avoid interruptions and distractions, and create a clear path for customers to follow seamlessly? If we aren’t supposed to make people think, how do we even get a chance to establish an emotional connection in the first place?</p>

<p>We do so by slowing down. Deliberately. By making people think. Not much. Just a little bit. Just enough to make them feel valued, or smile, or get curious. We do so by adding friction. A few bumps here and there, enough to offer a chance of being directly confronted with the personality infused in our interfaces. It might even mean confusing the customer every now and again just to enable a speedy recovery from that confusion with a dash of positive emotion in their eyes. That’s how memorable experiences emerge.</p>

<p>Everything is a little bit off on  &mdash; the spacing, the color combinations, the form layout, the hierarchy, the buttons, the cursor, the lightboxes, the illustrations. This consistent breaking of predictable patterns makes the website appear interesting and appealing. Breaking things slowly and deliberately, one component at a time. That’s not a regular restaurant website.</p>











<figure class="article__image break-out">
	<a href="https://baolondon.com/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/04389a08-67b0-44ed-ae1b-832da8d14907/bringing-personality-back-17-bao1.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/04389a08-67b0-44ed-ae1b-832da8d14907/bringing-personality-back-17-bao1.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/04389a08-67b0-44ed-ae1b-832da8d14907/bringing-personality-back-17-bao1.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/04389a08-67b0-44ed-ae1b-832da8d14907/bringing-personality-back-17-bao1.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/04389a08-67b0-44ed-ae1b-832da8d14907/bringing-personality-back-17-bao1.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/04389a08-67b0-44ed-ae1b-832da8d14907/bringing-personality-back-17-bao1.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>












<figure class="article__image break-out">
	<a href="https://baolondon.com/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2f2c1769-324b-416f-b5f7-26b816cf121e/bringing-personality-back-17-bao2.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2f2c1769-324b-416f-b5f7-26b816cf121e/bringing-personality-back-17-bao2.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2f2c1769-324b-416f-b5f7-26b816cf121e/bringing-personality-back-17-bao2.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2f2c1769-324b-416f-b5f7-26b816cf121e/bringing-personality-back-17-bao2.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2f2c1769-324b-416f-b5f7-26b816cf121e/bringing-personality-back-17-bao2.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2f2c1769-324b-416f-b5f7-26b816cf121e/bringing-personality-back-17-bao2.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>












<figure class="article__image break-out">
	<a href="https://baolondon.com/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dfd1002f-37f0-4bf7-bcd2-804fbe486192/bringing-personality-back-17-bao3.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dfd1002f-37f0-4bf7-bcd2-804fbe486192/bringing-personality-back-17-bao3.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dfd1002f-37f0-4bf7-bcd2-804fbe486192/bringing-personality-back-17-bao3.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dfd1002f-37f0-4bf7-bcd2-804fbe486192/bringing-personality-back-17-bao3.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dfd1002f-37f0-4bf7-bcd2-804fbe486192/bringing-personality-back-17-bao3.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dfd1002f-37f0-4bf7-bcd2-804fbe486192/bringing-personality-back-17-bao3.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>Everything is way off on the , and it’s done deliberately as well. The hostel was struggling to sell rooms as the competition was quite tough in Amsterdam. Rather than improving the design, they made it worse to fit well within their story. If you can’t make it better, make it worse. Even if you don’t have a wonderful product to sell, it’s always possible to wrap a story around it and make it more interesting. Pretty much every element on the page actively makes people confused &mdash; from color combination to typography to interactions. It worked though &mdash; they are expanding to Lisbon now.</p>











<figure class="article__image break-out">
	<a href="http://hansbrinker.eu/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c3990857-05cd-404e-a074-2c711fd23270/bringing-personality-back-24-hansbrinker1.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c3990857-05cd-404e-a074-2c711fd23270/bringing-personality-back-24-hansbrinker1.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c3990857-05cd-404e-a074-2c711fd23270/bringing-personality-back-24-hansbrinker1.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c3990857-05cd-404e-a074-2c711fd23270/bringing-personality-back-24-hansbrinker1.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c3990857-05cd-404e-a074-2c711fd23270/bringing-personality-back-24-hansbrinker1.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c3990857-05cd-404e-a074-2c711fd23270/bringing-personality-back-24-hansbrinker1.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>












<figure class="article__image break-out">
	<a href="http://hansbrinker.eu/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/518845a0-9c5a-4a22-9f06-a3d44233dc05/bringing-personality-back-24-hansbrinker2.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/518845a0-9c5a-4a22-9f06-a3d44233dc05/bringing-personality-back-24-hansbrinker2.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/518845a0-9c5a-4a22-9f06-a3d44233dc05/bringing-personality-back-24-hansbrinker2.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/518845a0-9c5a-4a22-9f06-a3d44233dc05/bringing-personality-back-24-hansbrinker2.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/518845a0-9c5a-4a22-9f06-a3d44233dc05/bringing-personality-back-24-hansbrinker2.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/518845a0-9c5a-4a22-9f06-a3d44233dc05/bringing-personality-back-24-hansbrinker2.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>












<figure class="article__image break-out">
	<a href="http://hansbrinker.eu/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0a81f8c0-bd2d-4e3b-8ce8-cbf8547f7778/bringing-personality-back-24-hansbrinker3.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0a81f8c0-bd2d-4e3b-8ce8-cbf8547f7778/bringing-personality-back-24-hansbrinker3.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0a81f8c0-bd2d-4e3b-8ce8-cbf8547f7778/bringing-personality-back-24-hansbrinker3.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0a81f8c0-bd2d-4e3b-8ce8-cbf8547f7778/bringing-personality-back-24-hansbrinker3.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0a81f8c0-bd2d-4e3b-8ce8-cbf8547f7778/bringing-personality-back-24-hansbrinker3.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0a81f8c0-bd2d-4e3b-8ce8-cbf8547f7778/bringing-personality-back-24-hansbrinker3.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>Now, of course, not everybody will like it, and some people will find it annoying, confusing, misleading, childish, or just over the top. Very much like we find it difficult to connect to some people, we might experience the same issue with an interface that attempts to show its human side. But isn’t it worth it? Perhaps in times when everything is remarkably similar and doesn’t really stand for anything, it’s worth striving for our product to be genuinely loved by many people for the price of being genuinely disliked by some people, rather than eliciting no feelings at all.</p>

<p>In his “How I Built This” , Mike Krieger, the co-founder and creative mind behind Instagram, mentioned that rather than spending a significant amount of time trying to understand why people abandoned the service, one of the fundamental principles that drives growth is focusing on customers who deeply love your product and stay around for years. By prioritizing existing customers and what they truly love about your product, you might not only attach them to your product, but also boost the word-of-mouth marketing that’s infinitely more effective than traditional landing pages.</p>

<p>It doesn’t mean, though, that we shouldn’t take good care of experiences customers have when abandoning the product, or &mdash; even worse &mdash; that we should make it harder for them to leave. The humane qualities of the interface should shine consistently through all the touchpoints of the experience &mdash; and it holds true for onboarding as much as offboarding. In fact, the latter is often neglected as it isn’t deemed as being that important &mdash; after all, at the point when the customer will face it, they have almost abandoned the product.</p>

<h3 id="offboarding-matters">Offboarding Matters</h3>

<p>Just like human relationships sometimes end abruptly and badly, leaving a lasting negative aftermath, so can our relationships with digital products. It’s highly unlikely that a person abandoning a product with a mysteriously long-winded journey through cancellation redirects would praise the product to friends and colleagues. People leave for very different reasons, and sometimes it has literally nothing to do with the service or the experience. They might have moved on, or just want to save money for something more important, or perhaps they just found an alternative that better fits their needs.</p>











<figure >
	<a href="https://www.smashingmagazine.com/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7e540073-0906-4004-9e30-4adef47b13a9/bringing-personality-back-wemisssyou.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7e540073-0906-4004-9e30-4adef47b13a9/bringing-personality-back-wemisssyou.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7e540073-0906-4004-9e30-4adef47b13a9/bringing-personality-back-wemisssyou.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7e540073-0906-4004-9e30-4adef47b13a9/bringing-personality-back-wemisssyou.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7e540073-0906-4004-9e30-4adef47b13a9/bringing-personality-back-wemisssyou.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7e540073-0906-4004-9e30-4adef47b13a9/bringing-personality-back-wemisssyou.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>












<figure >
	<a href="https://www.smashingmagazine.com/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/90690a28-42f4-4b78-a7d2-078888c4e4fe/bringing-personality-back-sm2.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/90690a28-42f4-4b78-a7d2-078888c4e4fe/bringing-personality-back-sm2.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/90690a28-42f4-4b78-a7d2-078888c4e4fe/bringing-personality-back-sm2.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/90690a28-42f4-4b78-a7d2-078888c4e4fe/bringing-personality-back-sm2.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/90690a28-42f4-4b78-a7d2-078888c4e4fe/bringing-personality-back-sm2.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/90690a28-42f4-4b78-a7d2-078888c4e4fe/bringing-personality-back-sm2.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>What if at the moment of departure we make them feel deeply valued and understood? Admittedly, with Smashing Magazine’s redesign, we didn’t spend too much time designing the offboarding UX, but it was important for us that the experience fitted well within the overall personality of the interface. When our customers cancel their membership subscription, we greet them with a respectful and even encouraging notice, providing a little gift for sticking around with us for so long, and explaining what happens to their personal data.</p>

<p>The result was surprising: we discovered that customers who cancel the subscription and go through the offboarding UX, sometimes tend to be even more eager to recommend us to their friends and total strangers than some loyal members who stick around for a long time. They just admire how respectfully and thoughtfully we deal with their decision, and that we don’t pull all the shady tricks from the trenches to make it difficult for them to leave.</p>

<h3 id="make-boring-interesting">Make Boring Interesting</h3>

<p>It’s difficult to introduce playful elements into an experience which is otherwise very much corporate and formal. However, whenever you are designing a particular interaction, be it as simple as hovering a button, or moving from one section to another, or filling in a form, there is always some room to make the experience slightly more interesting.</p>











<figure class="article__image break-out">
	<a href="http://www.bodenusa.com/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ce6d3ac5-29b5-4120-bd9f-7fc509292441/bringing-personality-back-boden.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ce6d3ac5-29b5-4120-bd9f-7fc509292441/bringing-personality-back-boden.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ce6d3ac5-29b5-4120-bd9f-7fc509292441/bringing-personality-back-boden.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ce6d3ac5-29b5-4120-bd9f-7fc509292441/bringing-personality-back-boden.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ce6d3ac5-29b5-4120-bd9f-7fc509292441/bringing-personality-back-boden.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ce6d3ac5-29b5-4120-bd9f-7fc509292441/bringing-personality-back-boden.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>For example, out of all the wonderful form elements on a given page, what could be less exciting than a “Title” input? Sometimes appearing alongside radio button counterparts or a dropdown, rigorously asking customers for very personal information about their marital status, without any obvious reason whatsoever. And that’s exactly the moment when we can make it shine beautifully. A great way of creating memorable experiences is adding a bit of surprise at the point where <strong>it’s most unexpected</strong>. Pick the most boring, unnoticeable part of the experience and try to make it interesting. Now, is there a way to make this interaction more interesting?</p>

<p>When creating a new account on , customers are dazzled with a quite unusual selection of options, ranging from Admiral to Squadron Leader and Baroness. Who hasn’t wanted to be a Squadron Leader at some point in their life? This little design decision elicits smiles, and prompts customers to share this gem with their friends and colleagues. By the way, the list of options is quite lengthy.</p>











<figure class="article__image break-out">
	<a href="http://www.bodenusa.com/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a1a67a94-f4c1-4ff0-834e-24f728b09f3f/bringing-personality-back-boden2.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a1a67a94-f4c1-4ff0-834e-24f728b09f3f/bringing-personality-back-boden2.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a1a67a94-f4c1-4ff0-834e-24f728b09f3f/bringing-personality-back-boden2.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a1a67a94-f4c1-4ff0-834e-24f728b09f3f/bringing-personality-back-boden2.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a1a67a94-f4c1-4ff0-834e-24f728b09f3f/bringing-personality-back-boden2.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a1a67a94-f4c1-4ff0-834e-24f728b09f3f/bringing-personality-back-boden2.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p> is just one of many local breweries in the US. When customers enter the site, as always they are prompted with an age check that’s supposed to ensure they are over a certain age limit. Most people &mdash; honestly or dishonestly &mdash; would click on “Yes” and move on, but if the customer chooses to click on “No,” they embark on a “choose-your-own-adventure” trip to be guided to a video that best describes their personality.</p>











<figure class="article__image break-out">
	<a href="https://austinbeerworks.com/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/feae39dc-67cf-419f-a89c-5d6fd9730146/bringing-personality-back-22-austin1.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/feae39dc-67cf-419f-a89c-5d6fd9730146/bringing-personality-back-22-austin1.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/feae39dc-67cf-419f-a89c-5d6fd9730146/bringing-personality-back-22-austin1.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/feae39dc-67cf-419f-a89c-5d6fd9730146/bringing-personality-back-22-austin1.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/feae39dc-67cf-419f-a89c-5d6fd9730146/bringing-personality-back-22-austin1.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/feae39dc-67cf-419f-a89c-5d6fd9730146/bringing-personality-back-22-austin1.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>












<figure >
	<a href="https://austinbeerworks.com/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9014d329-9853-498d-9794-d201659d652f/bringing-personality-back-22-austin2.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9014d329-9853-498d-9794-d201659d652f/bringing-personality-back-22-austin2.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9014d329-9853-498d-9794-d201659d652f/bringing-personality-back-22-austin2.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9014d329-9853-498d-9794-d201659d652f/bringing-personality-back-22-austin2.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9014d329-9853-498d-9794-d201659d652f/bringing-personality-back-22-austin2.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9014d329-9853-498d-9794-d201659d652f/bringing-personality-back-22-austin2.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>












<figure >
	<a href="https://austinbeerworks.com/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f7694030-2ff8-401b-aa0d-955180c5ae60/bringing-personality-back-22-austin3.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f7694030-2ff8-401b-aa0d-955180c5ae60/bringing-personality-back-22-austin3.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f7694030-2ff8-401b-aa0d-955180c5ae60/bringing-personality-back-22-austin3.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f7694030-2ff8-401b-aa0d-955180c5ae60/bringing-personality-back-22-austin3.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f7694030-2ff8-401b-aa0d-955180c5ae60/bringing-personality-back-22-austin3.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f7694030-2ff8-401b-aa0d-955180c5ae60/bringing-personality-back-22-austin3.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>












<figure >
	<a href="https://austinbeerworks.com/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f83ce391-4512-488f-9e58-b1deb14f81fb/bringing-personality-back-22-austin4.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f83ce391-4512-488f-9e58-b1deb14f81fb/bringing-personality-back-22-austin4.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f83ce391-4512-488f-9e58-b1deb14f81fb/bringing-personality-back-22-austin4.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f83ce391-4512-488f-9e58-b1deb14f81fb/bringing-personality-back-22-austin4.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f83ce391-4512-488f-9e58-b1deb14f81fb/bringing-personality-back-22-austin4.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f83ce391-4512-488f-9e58-b1deb14f81fb/bringing-personality-back-22-austin4.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>












<figure >
	<a href="https://austinbeerworks.com/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/eed01e1e-3f99-4d67-80ca-1d2858fadf9e/bringing-personality-back-22-austin5.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/eed01e1e-3f99-4d67-80ca-1d2858fadf9e/bringing-personality-back-22-austin5.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/eed01e1e-3f99-4d67-80ca-1d2858fadf9e/bringing-personality-back-22-austin5.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/eed01e1e-3f99-4d67-80ca-1d2858fadf9e/bringing-personality-back-22-austin5.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/eed01e1e-3f99-4d67-80ca-1d2858fadf9e/bringing-personality-back-22-austin5.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/eed01e1e-3f99-4d67-80ca-1d2858fadf9e/bringing-personality-back-22-austin5.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>












<figure >
	<a href="https://austinbeerworks.com/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cead55a5-46a1-439d-8246-04b30ec67c89/bringing-personality-back-22-austin6.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cead55a5-46a1-439d-8246-04b30ec67c89/bringing-personality-back-22-austin6.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cead55a5-46a1-439d-8246-04b30ec67c89/bringing-personality-back-22-austin6.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cead55a5-46a1-439d-8246-04b30ec67c89/bringing-personality-back-22-austin6.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cead55a5-46a1-439d-8246-04b30ec67c89/bringing-personality-back-22-austin6.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cead55a5-46a1-439d-8246-04b30ec67c89/bringing-personality-back-22-austin6.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>Who doesn’t love disliking a pop-up? However, pop-ups can be made interesting too.  uses the most annoyingly delightful pop-up out there, beautifully illustrated as a person holding a sign in front of the website. As the visitors hover over it to close it, the pop-up sneakily moves away a little bit, making it just a tad more difficult to close it. Personally, I wish every single website had a pop-up like that.</p>











<figure class="article__image break-out">
	<a href="https://www.volkshotel.nl/en/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a6a51bc2-3deb-4268-bb9a-98c40d3f5b77/bringing-personality-back-21-volkshotel.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a6a51bc2-3deb-4268-bb9a-98c40d3f5b77/bringing-personality-back-21-volkshotel.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a6a51bc2-3deb-4268-bb9a-98c40d3f5b77/bringing-personality-back-21-volkshotel.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a6a51bc2-3deb-4268-bb9a-98c40d3f5b77/bringing-personality-back-21-volkshotel.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a6a51bc2-3deb-4268-bb9a-98c40d3f5b77/bringing-personality-back-21-volkshotel.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a6a51bc2-3deb-4268-bb9a-98c40d3f5b77/bringing-personality-back-21-volkshotel.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p> doesn’t look particularly exceptional until the visitor chooses to interact with it. When moving from one exhibition detail page to another, rather than just loading another page, the user is moved from one room to another within a 3D space. Unexpected and memorable.</p>











<figure class="article__image break-out">
	<a href="https://tympanus.net/Development/Exhibition/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bbadab1a-77be-434b-b552-ebb88cda0892/bringing-personality-back-20-exhibition1.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bbadab1a-77be-434b-b552-ebb88cda0892/bringing-personality-back-20-exhibition1.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bbadab1a-77be-434b-b552-ebb88cda0892/bringing-personality-back-20-exhibition1.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bbadab1a-77be-434b-b552-ebb88cda0892/bringing-personality-back-20-exhibition1.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bbadab1a-77be-434b-b552-ebb88cda0892/bringing-personality-back-20-exhibition1.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bbadab1a-77be-434b-b552-ebb88cda0892/bringing-personality-back-20-exhibition1.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>












<figure class="article__image break-out">
	<a href="https://tympanus.net/Development/Exhibition/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/98277004-ebdb-404d-9845-338443807f71/bringing-personality-back-20-exhibition2.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/98277004-ebdb-404d-9845-338443807f71/bringing-personality-back-20-exhibition2.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/98277004-ebdb-404d-9845-338443807f71/bringing-personality-back-20-exhibition2.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/98277004-ebdb-404d-9845-338443807f71/bringing-personality-back-20-exhibition2.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/98277004-ebdb-404d-9845-338443807f71/bringing-personality-back-20-exhibition2.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/98277004-ebdb-404d-9845-338443807f71/bringing-personality-back-20-exhibition2.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>What’s a slightly more common interaction on the web? Forms, in all their different flavors and appearances. In fact, chances are high that you have some sort of a login and password input on your site, and, of course, that’s a pretty boring interaction. Adding a character responding to a user’s input might spice things up a little. As a result, people might spend more time interacting with the form before signing in. That’s better engagement at hand.  does just that.</p>

<figure class="break-out"></figcaption></figure>

<p>The strategy is simple: choose one predictable, boring pattern, study user expectations and… break them mercilessly by adding something unexpected and uplifting to it. Please note that it doesn’t mean breaking usability just for the sake of breaking it; rather, it’s about making a handful of boring elements more interesting by adding some unconventional treatments to their design.</p>

<h3 id="find-a-pain-point-and-solve-it-well">Find A Pain Point And Solve It Well</h3>

<p>Can you hear restless voices of skepticism whispering from the corner of the room? Not every corporate setting will sustain a funky custom illustration, a quirky animation, or an unconventional interaction. A striking visual identity might not really fit into your digital presence, custom illustrations might not be within the budget, and you might not want to break customer’s expectations anyway.</p>

<p>In these cases, you might want to explore a slightly different route. If you can’t convey your personality through unconventional aesthetics or interaction, an alternative is to <strong>convey it through superior problem solving</strong>. It means you need to uncover painful moments of interaction &mdash; when customers are annoyed or disappointed or confused &mdash; on similar sites, and sweep through experimental and seemingly far-fetched solutions to try to trump the experience that your competitors provide. Take on a problem, and tackle it meticulously, head on.</p>

<p>Surprisingly, most of the time these pain points aren’t particular features; it’s the perceived complexity of the interaction and the lack of transparency. Too many form fields; too much time investment; too slow an interaction; too many repeated questions; too many unnecessary requirements. The angle is to find a way to make seemingly complex interactions deceptively easy, hence surpassing expectations.</p>

<p>It goes without saying that solving a particular pain point won’t help much if basics aren’t covered properly. Accessibility, performance, proper visual hierarchy, and responsive behavior are the founding pillars of every experience, and have to be considered first.</p>

<p> is a Swiss trip planner app that allows customers to check the schedule of trains and purchase train tickets. On its own, it’s a trip planner like every single similar app out there, except for one thing. The app provides a “touch timetable”; customers can define their common destinations and arrange them on a grid. To purchase a ticket from Zurich to Lausanne, for example, it’s enough to draw a line on the grid connecting Zurich and Lausanne and then confirm the selection. Booking tickets has never been that fast and easy. That’s a great example of making a conventionally complex interaction straightforward, especially for people who commute frequently. Also, it’s a unique design signature that nobody else has (yet).</p>











<figure >
	<a href="http://www.sbb.ch/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/08242d92-4c0f-47f9-8bc8-0dce751b04cc/bringing-personality-back-27-ubique-3.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/08242d92-4c0f-47f9-8bc8-0dce751b04cc/bringing-personality-back-27-ubique-3.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/08242d92-4c0f-47f9-8bc8-0dce751b04cc/bringing-personality-back-27-ubique-3.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/08242d92-4c0f-47f9-8bc8-0dce751b04cc/bringing-personality-back-27-ubique-3.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/08242d92-4c0f-47f9-8bc8-0dce751b04cc/bringing-personality-back-27-ubique-3.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/08242d92-4c0f-47f9-8bc8-0dce751b04cc/bringing-personality-back-27-ubique-3.jpg"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>












<figure >
	<a href="http://www.sbb.ch/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5c75a494-67cd-477c-8cbb-474b0c719f40/bringing-personality-back-27-ubique-1.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5c75a494-67cd-477c-8cbb-474b0c719f40/bringing-personality-back-27-ubique-1.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5c75a494-67cd-477c-8cbb-474b0c719f40/bringing-personality-back-27-ubique-1.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5c75a494-67cd-477c-8cbb-474b0c719f40/bringing-personality-back-27-ubique-1.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5c75a494-67cd-477c-8cbb-474b0c719f40/bringing-personality-back-27-ubique-1.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5c75a494-67cd-477c-8cbb-474b0c719f40/bringing-personality-back-27-ubique-1.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>What would it take to provide a remarkable video-playing experience? It might sound as simple as designing a track and a thumb with a few ticks on the track for quick jumps. However, if you study common problems users experience frequently, you’ll find one particular issue that stands out. People tend to pause videos and then continue watching later, yet restoring the state of where things were left off is unnecessarily complex in many video player UIs.</p>

<p>In fact, you might encounter people writing down the exact time stamp when they paused the video, just to return to it later on another device &mdash; but then again, in most UIs it’s impossible to jump precisely to a particular second, and most of the time you have to guess and tap the position of a thumb on the track correctly. In the same way, jumping back and forward by 30 seconds or even by a few minutes can be remarkably challenging, especially on mobile, as most interfaces aren’t designed around that particular case.</p>

<p>Not only does  provide fully accessible controls for navigation, it also contains a keyframes preview with thumbnails appearing on hover, and navigation via keyboard &mdash; and it stores the current state of the video, allowing customers to save a particular time stamp with a unique URL to continue watching later. YouTube also contains many lengthy videos, like documentaries or tutorials, so users can slide up the thumb vertically to adjust the scale of the track and hence jump to the point of interest more precisely. Unfortunately, only a few users know of the feature, and the interaction isn’t particularly self-explanatory, but those who do know of it, use it frequently. One pain point, solved well.</p>











<figure class="article__image break-out">
	<a href="https://www.youtube.com/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d30074c7-283e-4138-98ab-eb4589ff5158/bringing-personality-back-28-youtube-1.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d30074c7-283e-4138-98ab-eb4589ff5158/bringing-personality-back-28-youtube-1.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d30074c7-283e-4138-98ab-eb4589ff5158/bringing-personality-back-28-youtube-1.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d30074c7-283e-4138-98ab-eb4589ff5158/bringing-personality-back-28-youtube-1.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d30074c7-283e-4138-98ab-eb4589ff5158/bringing-personality-back-28-youtube-1.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d30074c7-283e-4138-98ab-eb4589ff5158/bringing-personality-back-28-youtube-1.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>












<figure class="article__image break-out">
	<a href="https://www.youtube.com/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a95b1901-f8c2-4271-bff4-2a9ded7957ac/bringing-personality-back-28-youtube-2.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a95b1901-f8c2-4271-bff4-2a9ded7957ac/bringing-personality-back-28-youtube-2.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a95b1901-f8c2-4271-bff4-2a9ded7957ac/bringing-personality-back-28-youtube-2.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a95b1901-f8c2-4271-bff4-2a9ded7957ac/bringing-personality-back-28-youtube-2.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a95b1901-f8c2-4271-bff4-2a9ded7957ac/bringing-personality-back-28-youtube-2.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a95b1901-f8c2-4271-bff4-2a9ded7957ac/bringing-personality-back-28-youtube-2.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>Most academic publications contain dozens of endnotes, footnotes, and references, listed in the order of appearance. If a reader is interested in a particular footnote, they have to jump to the end of the article to read it, and then jump back to continue reading the article. This experience might be a bit too tedious for frequent use, yet it’s the default experience we all are accustomed to.</p>

<p>The  solves this problem in a different way. References are always located right next to the point where they are mentioned. Every side note and footnote either appears on the sides on larger screens, or displayed inline via an accordion. Once a user has tapped on the footnote, it expands in its entirety, while the footnote turns into a “close” button. A simple problem solved well.</p>











<figure class="article__image break-out">
	<a href="https://www.harvardlawreview.org/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2fd4c11a-055d-4023-b1c9-f9c754f87623/bringing-personality-back-29-hlr-1.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2fd4c11a-055d-4023-b1c9-f9c754f87623/bringing-personality-back-29-hlr-1.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2fd4c11a-055d-4023-b1c9-f9c754f87623/bringing-personality-back-29-hlr-1.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2fd4c11a-055d-4023-b1c9-f9c754f87623/bringing-personality-back-29-hlr-1.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2fd4c11a-055d-4023-b1c9-f9c754f87623/bringing-personality-back-29-hlr-1.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2fd4c11a-055d-4023-b1c9-f9c754f87623/bringing-personality-back-29-hlr-1.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>












<figure >
	<a href="https://www.harvardlawreview.org/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/617c6eda-09f5-486c-a717-ed0ddbe15373/bringing-personality-back-29-hlr-2.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/617c6eda-09f5-486c-a717-ed0ddbe15373/bringing-personality-back-29-hlr-2.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/617c6eda-09f5-486c-a717-ed0ddbe15373/bringing-personality-back-29-hlr-2.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/617c6eda-09f5-486c-a717-ed0ddbe15373/bringing-personality-back-29-hlr-2.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/617c6eda-09f5-486c-a717-ed0ddbe15373/bringing-personality-back-29-hlr-2.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/617c6eda-09f5-486c-a717-ed0ddbe15373/bringing-personality-back-29-hlr-2.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>Imagine you want to book a wonderful vacation with your family, but you haven’t picked your dates yet. You have an idea of when you’d like to go, and you have some flexibility regarding the dates for your next vacation.  suggests a route based on your preferences. That’s a real problem case solved well. Most traveling websites ask for specific dates for inbound and outbound flights.</p>











<figure class="article__image break-out">
	<a href="https://www.dohop.com/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5e662b47-d970-441a-a704-07866dc61ab7/bringing-personality-back-30-dohop.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5e662b47-d970-441a-a704-07866dc61ab7/bringing-personality-back-30-dohop.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5e662b47-d970-441a-a704-07866dc61ab7/bringing-personality-back-30-dohop.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5e662b47-d970-441a-a704-07866dc61ab7/bringing-personality-back-30-dohop.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5e662b47-d970-441a-a704-07866dc61ab7/bringing-personality-back-30-dohop.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5e662b47-d970-441a-a704-07866dc61ab7/bringing-personality-back-30-dohop.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>












<figure class="article__image break-out">
	<a href="https://www.dohop.com/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b4718996-4b39-478f-b037-c0dedc805234/bringing-personality-back-31-routeperfect.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b4718996-4b39-478f-b037-c0dedc805234/bringing-personality-back-31-routeperfect.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b4718996-4b39-478f-b037-c0dedc805234/bringing-personality-back-31-routeperfect.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b4718996-4b39-478f-b037-c0dedc805234/bringing-personality-back-31-routeperfect.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b4718996-4b39-478f-b037-c0dedc805234/bringing-personality-back-31-routeperfect.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b4718996-4b39-478f-b037-c0dedc805234/bringing-personality-back-31-routeperfect.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>Good solutions require time and focus. They require us to <em>really</em> understand what pain points users experience first. Users might not be very good at articulating those paint points, so we developed a simple technique that helps us get to the root of the problem.</p>

<p>We ask testers to complete a particular task on a competitor’s website, and record their session on video, along with a webcam, using the device that they are used to. It could be as easy as finding an item in a catalog, or checking out on a retail store, or finding a particular section in the navigation. Of course, we observe their behavior and ask questions if something appears to be unusual, but too often many things that happen during the sessions go unnoticed &mdash; they are just too difficult to spot right away. That’s why we <strong>rewatch recorded user sessions in slow motion</strong>, often slowing down the playback five or six times.</p>

<p>We look for repeated movements and imprecise hits, as well as negative facial expressions and gestures. More specifically, we search for <em>little moments of despair</em> &mdash; fleeting moments of confusion when movements or gestures don’t make any sense: circling around a button or a link over and over again; focusing on a particular interactive element for far too long; selecting the same text a few times in a row and then continuing to navigate without acting on it. The playback sessions usually happen right after the test, so we still have an opportunity to ask questions and validate our assumptions with the tester. Even a few recordings usually provide actionable insights &mdash; and it doesn’t require many resources or much investment. It’s also a good idea to examine customer support logs, and ask the support team about common complaints.</p>

<p>Once we’ve identified some issues, we explore solutions that would provide more clarity and ease the interaction, sometimes by designing without any particular visual language in mind. The point is to find an interaction pattern that would be way more superior to the experience customers had on the competitor’s sites. We then produce a digital mock-up and invite the same customers to try to solve the same tasks, along with a new group of testers who haven’t seen both interfaces yet. We measure the time needed to complete an interaction and ask them to choose which interaction they find more straightforward and useful, and why. Surprisingly, faster interactions aren’t necessarily perceived as being faster, and slower interactions aren’t necessarily perceived as being slower. Based on that, we iterate and evolve those prototypes. In many ways, those pain points become the heart of our experience that we tackle first and radiate the entire experience out from. That’s why sometimes, instead of running a test on a competitor’s website, we test our own solutions in the same way.</p>

<p>Good solutions trigger an emotional attachment with or without non-conventional aesthetics or interaction. The more pain points you can address well within your interface, the more likely the difference in experience is to be noticed. Only a few websites make it to customers’ browser toolbars, so think about that one pain point and the one solution that would make them do just that.</p>

<h3 id="exceeding-expectations-by-default">Exceeding Expectations By Default</h3>

<p>Here’s another question for you: of all the hotel experiences you ever had, which ones are the most memorable? Think about it for a moment. Think about what made them so special and why they are so memorable. It might have been an extraordinary natural backdrop, or remarkably attentive personnel, or a lavish breakfast buffet. Or something entirely different. In fact, for many of us it could have been a pretty average dormitory as much as an exquisite 5-star chalet in the Swiss alps. The environment matters, but it’s not the environment alone that matters.</p>

<p class="c-pre-sidenote--left">The reason why these experiences are memorable is because they aren’t average.<sup>4</sup> In fact, they are the very opposite of average in *some* way, as *something* was exceptional about them. It’s not necessarily the hotel itself &mdash; it’s the timing and the people we happen to spend these experiences with. A good hotel provides a setting that enables wonderful experiences, and so does a good website interface. A *memorable* hotel adds a fine detail to the experience that exceeds our expectations, and it does so without telling us up front. And so do memorable websites.</p><p class="c-sidenote c-sidenote--right"><sup>4</sup> According to Daniel Kahneman’s peak-end rule, we tend to judge experiences largely based on how we felt at its peak (that is, its most intense point) and at its end, rather than on the total sum or average of every moment of the experience. The effect occurs whether the experience is pleasant or unpleasant. Other information aside from the peak and end of the experience is not lost, but it is not used. That means we can tap into very negative and very positive parts of the experience, and tweak them to create an emotional connection.</p>

<p>As Brené Brown, a research professor at the University of Houston, so beautifully expressed in , “good design is a function of empathy, while non-empathic design is self-indulgent and self-centered.” The key, then, is to empathize with customers both in their negative and positive experiences, rather than pushing your own agenda. To our customers, that extra fine attention to a few little details can make all the difference in the world. So we could sprinkle a little bit of human kindness here and there, adding extra value silently, without even mentioning it. That fine detail could be as simple as a custom-designed profile illustration, based on the photo the customer has uploaded. It could be a handwritten thank-you note, signed by the entire team and sent via good ol’ snail mail. It could also be an unexpectedly straightforward resolution of a problem after a mistake has been made.</p>

<p>In an eCommerce setting, it could mean the ability to modify or cancel a finished order within five mins after the successful checkout. On the one side, it could help a customer avoid a time-consuming interaction with the support team; and on the other side, just imagine the look on the customer’s face when they realize that the date of the booking was wrong, yet it’s possible to cancel the booking with a click of a button &mdash; without any charges applied.</p>











<figure >
	<a href="https://www.smashingmagazine.com/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7d5bdba8-1e49-411c-b3f4-b4491a92099e/35-finish-checkout.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7d5bdba8-1e49-411c-b3f4-b4491a92099e/35-finish-checkout.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7d5bdba8-1e49-411c-b3f4-b4491a92099e/35-finish-checkout.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7d5bdba8-1e49-411c-b3f4-b4491a92099e/35-finish-checkout.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7d5bdba8-1e49-411c-b3f4-b4491a92099e/35-finish-checkout.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7d5bdba8-1e49-411c-b3f4-b4491a92099e/35-finish-checkout.png"
			sizes="100vw"
			alt="Smashing Magazine’s checkout"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			A mock-up we’re currently exploring in Smashing Magazine’s checkout to allow inline editing of data on the review step and editing of the order within 5 minutes after the purchase.
		</figcaption>
	
</figure>


<p>In the same way, an interface could suggest to a signed-in customer to use a saved coupon code, or inform them about a similar &mdash; and hence potentially duplicate &mdash; booking made a while back. The personality of the brand shines best in those little moments when it helps customers prevent mistakes. By acting on behalf of the experience rather than business every now and again, the interface makes the customer feel genuinely valued, respected, and helped, and that works much better than any ingenious interface copy ever would.</p>











<figure >
	<a href="https://www.smashingmagazine.com/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4b6018be-2b10-49fd-8eb2-a93ca54d2314/35-finish-checkout-2.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4b6018be-2b10-49fd-8eb2-a93ca54d2314/35-finish-checkout-2.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4b6018be-2b10-49fd-8eb2-a93ca54d2314/35-finish-checkout-2.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4b6018be-2b10-49fd-8eb2-a93ca54d2314/35-finish-checkout-2.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4b6018be-2b10-49fd-8eb2-a93ca54d2314/35-finish-checkout-2.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4b6018be-2b10-49fd-8eb2-a93ca54d2314/35-finish-checkout-2.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>One way of preventing mistakes is by writing adaptive and helpful error messages. That’s one of the most obvious points of frustration for customers, and it’s remarkable how little effort is put into recovery experience, often falling back to generic and abstract messages. Perhaps they don’t cost a sale but they can damage the long-term perception of the brand. People who experience unrecoverable issues during one of the key interactions on a site tend to not use it in the future at all as they expect the issue to creep out in other interactions too.</p>

<p>Overall, error messages deserve slightly more credit than they are usually given. By nature, they appear at the point where the customer’s progress is blocked. That’s also the point where the customers have to slow down and pay full attention to resolve the problem. That’s quite unusual for the entire spectrum of experiences on a site, and we can use the situation to our advantage to infuse a bit of personality into the experience. Every single time our interfaces fail to meet expectations, we should see it as an opportunity to create a memorable impact in the process of speedy recovery. If we manage to turn an annoyance into the feeling of being valued or understood along the way, we might be heading off on the right track.</p>

<p>One of the very first things I started working on when we embarked on the redesign was <strong>filling elaborate spreadsheets</strong> with alternate wordings for our checkout error messages. It wasn’t done with the intention to A/B test the &ldquo;best performing&rdquo; error message, though; it was done primarily to discover better expressions of the personality through the interface. On their own, error messages don’t really make sense, but they fit well within the story being told throughout the site. Obviously, we try to make it as difficult as possible to make mistakes in the first place, but once an error has occurred, we try to use both adaptive and playful copywriting to address the issue while also raise the occasional smile.</p>











<figure class="article__image break-out">
	<a href="https://styleguide.mailchimp.com/voice-and-tone/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/aa593cc1-a763-4914-ba1a-ad3b79db043f/bringing-personality-back-34-mailchimp-voice-tone.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/aa593cc1-a763-4914-ba1a-ad3b79db043f/bringing-personality-back-34-mailchimp-voice-tone.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/aa593cc1-a763-4914-ba1a-ad3b79db043f/bringing-personality-back-34-mailchimp-voice-tone.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/aa593cc1-a763-4914-ba1a-ad3b79db043f/bringing-personality-back-34-mailchimp-voice-tone.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/aa593cc1-a763-4914-ba1a-ad3b79db043f/bringing-personality-back-34-mailchimp-voice-tone.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/aa593cc1-a763-4914-ba1a-ad3b79db043f/bringing-personality-back-34-mailchimp-voice-tone.png"
			sizes="100vw"
			alt="Voice &amp;amp; Tone by MailChimp"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Voice and tone are the main pillars of a personality. MailChimp has built a dedicated voice and tone style guide to align designers, customer support, and everybody else in the way they communicate to customers.
		</figcaption>
	
</figure>


<p><strong>Seek critical pain points</strong> that customers often experience on the site by looking into customer support logs and user interviews, and design these experiences with extra care and attention. It goes without saying that a quirky personality won’t help much if the customer isn’t able to solve a problem, so take care of the basics first. Ultimately, it doesn’t take that much effort to turn negative experiences into positive ones &mdash; it’s just a matter of having it on your to-do list when designing an interface.</p>

<h3 id="the-two-sides-of-personality">The Two Sides Of Personality</h3>

<p>As much as we love sharing our experiences and showing our better side to people around us, we can’t stand that one person spending the entire evening talking about themselves. In our interfaces, every time we add yet another parallax transition or a slow bouncy animation to people who have seen it a dozen times already, we are essentially letting the interface highlight its fanciness without helping the user along the way. Eventually, after a few visits, all those whistles and bells that achieve a strong first impact become annoying as they add too much friction.</p>

<p>Nobody loves self-centered characters, and so a website shouldn’t be self-centered either. The design signature should never take the leading role in the user experience as it’s never the main reason why people access the website. It should be humble and remain in the shadows, noticeable but not obstructing the smooth flow frequent visitors have got used to.</p>

<p>In her brilliant talk on , Val Head, a designer from Pittsburgh, US, suggested using prominent animations very sparingly, as they should be reserved for very special occasions, while subtle micro-animations could accompany the user all along the way. Val suggests using animation only for key compositions of your story, like sending a marketing campaign, or favoriting an item, or seeing a successful purchasing page, while everything else should remain calm and as normal. With this idea in mind we could think of designing our interfaces with two kinds of interactions: the prominent “showroom” ones, used rarely; and subtle “workhorse” ones, used frequently.</p>

<p>Reserve special visual treatments and interactions for special occasions, but also embed subtle treatments used consistently across the entire site. Twitter, for example, uses an elaborate animation when a user “hearts”  a tweet. Facebook displays a confetti animation when you congratulate a friend on their birthday or a wedding. In Smashing’s case, we use vibrant colors and cat illustrations as our showroom signature, while tilting, hover-animations, and shadows beneath them make up our workhorse signature.</p>

<p>We are used to the idea of our designs adjusting to the viewport or network conditions, but it might be worth looking into adjusting the design based on the frequency of usage too. The technique is often called <em></em>, essentially a dynamic simplification of an interface as users become familiar with it. The idea is simple: identify the major features in your interface, and assign levels to these features. Then, track your user’s usage by monitoring the frequency of use within a certain time period and create proficiency profiles for the user. Based on the current level, you could then adjust components of the interface to reduce hand-holding.</p>

<p>As .</p>











<figure >
	<a href="http://layervault.tumblr.com/post/42361566927/progressive-reduction">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/56c14e61-383c-49d8-b42f-b9f4375c4a27/bringing-personality-back-33-progressive-reduction.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/56c14e61-383c-49d8-b42f-b9f4375c4a27/bringing-personality-back-33-progressive-reduction.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/56c14e61-383c-49d8-b42f-b9f4375c4a27/bringing-personality-back-33-progressive-reduction.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/56c14e61-383c-49d8-b42f-b9f4375c4a27/bringing-personality-back-33-progressive-reduction.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/56c14e61-383c-49d8-b42f-b9f4375c4a27/bringing-personality-back-33-progressive-reduction.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/56c14e61-383c-49d8-b42f-b9f4375c4a27/bringing-personality-back-33-progressive-reduction.png"
			sizes="100vw"
			alt="Adjusting a button based on the frequency of use"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Adjusting a button based on the frequency of use. The technique was first published by  from LayerVault.
		</figcaption>
	
</figure>


<p>The more often customers visit the site, the less likely they want to be confronted with anything that would slow them down. Therefore, it might be a good idea to slowly fade out showroom signatures with growing frequency of use, perhaps removing parallax-effects or speeding up transitions for returning users. In the end, it’s all about the choreography: don’t be that person at a dinner party filling the room with an extensive story of their life.</p>

<p>The Signature at the Heart of the Design
The design process is a mythical creature. Everybody somehow manages to come up with their own workflow, tooling, and processes, yet it’s very rare that anybody is really satisfied with it. When it comes to infusing personality into the design, when and where would be the right point to include it in the design process?</p>

<p>, Patty Toland, a senior UX designer from Filament Group in Boston mentioned the hierarchy of priorities the team uses when designing and building responsive experiences. The main goal of the process is to create the “leanest, fastest-loading, most optimized page.” The main foundation is and has always been a fully accessible experience, in which text, images, data, charts, audio, video, forms and so on are all broadly accessible and function fully in their default form. Applied to the context of the design process, it means meaningful markup and properly defined relationships between components.</p>











<figure class="article__image break-out">
	<a href="https://t.co/Tb0q1gMwQS">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/617ead05-6176-4bf1-adf1-d3a59ca127af/bringing-personality-back-filament.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/617ead05-6176-4bf1-adf1-d3a59ca127af/bringing-personality-back-filament.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/617ead05-6176-4bf1-adf1-d3a59ca127af/bringing-personality-back-filament.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/617ead05-6176-4bf1-adf1-d3a59ca127af/bringing-personality-back-filament.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/617ead05-6176-4bf1-adf1-d3a59ca127af/bringing-personality-back-filament.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/617ead05-6176-4bf1-adf1-d3a59ca127af/bringing-personality-back-filament.png"
			sizes="100vw"
			alt="the hierarchy of priorities the team uses when designing and building responsive experiences"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Patty Toland, Filament Group, “”.
		</figcaption>
	
</figure>


<p>With accessible components ready to be served, the next step is taking care of the scale of the design. That’s where the decisions about grid, content size, order, and arrangement, as well as breakpoints, come into play. Often the proportions will be defined using <em>content wireframes</em>: low-fidelity mock-ups with gray boxes; the height of each box in proportion to others defines its weight in the layout. Sometimes we add notes about the personality across the content blocks, and then reflect them when it comes to visual design.</p>











<figure class="article__image break-out">
	<a href="https://weareadjacent.com/projects/syracuse-university-original-orange/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f5f0a4da-ac15-46c4-819b-b8e0940488aa/bringing-personality-back-grid6.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f5f0a4da-ac15-46c4-819b-b8e0940488aa/bringing-personality-back-grid6.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f5f0a4da-ac15-46c4-819b-b8e0940488aa/bringing-personality-back-grid6.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f5f0a4da-ac15-46c4-819b-b8e0940488aa/bringing-personality-back-grid6.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f5f0a4da-ac15-46c4-819b-b8e0940488aa/bringing-personality-back-grid6.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f5f0a4da-ac15-46c4-819b-b8e0940488aa/bringing-personality-back-grid6.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>












<figure class="article__image break-out">
	<a href="https://weareadjacent.com/projects/syracuse-university-original-orange/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/77672739-289a-410a-bb0a-b294c8593739/bringing-personality-back-grid9.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/77672739-289a-410a-bb0a-b294c8593739/bringing-personality-back-grid9.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/77672739-289a-410a-bb0a-b294c8593739/bringing-personality-back-grid9.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/77672739-289a-410a-bb0a-b294c8593739/bringing-personality-back-grid9.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/77672739-289a-410a-bb0a-b294c8593739/bringing-personality-back-grid9.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/77672739-289a-410a-bb0a-b294c8593739/bringing-personality-back-grid9.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>












<figure class="article__image break-out">
	<a href="https://weareadjacent.com/projects/syracuse-university-original-orange/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e004fc6d-4f91-4d61-9afd-b7d61b0bf0c2/bringing-personality-back-grid11.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e004fc6d-4f91-4d61-9afd-b7d61b0bf0c2/bringing-personality-back-grid11.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e004fc6d-4f91-4d61-9afd-b7d61b0bf0c2/bringing-personality-back-grid11.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e004fc6d-4f91-4d61-9afd-b7d61b0bf0c2/bringing-personality-back-grid11.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e004fc6d-4f91-4d61-9afd-b7d61b0bf0c2/bringing-personality-back-grid11.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e004fc6d-4f91-4d61-9afd-b7d61b0bf0c2/bringing-personality-back-grid11.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>












<figure class="article__image break-out">
	<a href="https://weareadjacent.com/projects/syracuse-university-original-orange/">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/95276c42-c122-4aa9-b8ab-d3bd5cc1d1ea/bringing-personality-back-otto.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/95276c42-c122-4aa9-b8ab-d3bd5cc1d1ea/bringing-personality-back-otto.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/95276c42-c122-4aa9-b8ab-d3bd5cc1d1ea/bringing-personality-back-otto.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/95276c42-c122-4aa9-b8ab-d3bd5cc1d1ea/bringing-personality-back-otto.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/95276c42-c122-4aa9-b8ab-d3bd5cc1d1ea/bringing-personality-back-otto.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/95276c42-c122-4aa9-b8ab-d3bd5cc1d1ea/bringing-personality-back-otto.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Content wireframes in action. At the top the wireframe of 
		</figcaption>
	
</figure>


<p>With low-fidelity prototypes in place, the next step for the design is to gain style, with logo, brand colors, custom fonts, transitions, and animations added to the mix. Sometimes this hierarchy will be perfectly mapped in the order we write React components and CSS properties with Sass. Even seemingly unrelated tasks, like BEM naming for classes, will happen in that order as well. The prototypes will gain abstract utility classes first, and more elaborate relationships will be reflected through more specific class names throughout the process. The process establishes a clear separation of responsibilities for modules.</p>

<p>This process seems plausible at first, but it raises a very critical question: what pages to design and prototype first? When we start designing, we design the heart of the experience first: the most critical and impactful part of the experience. More specifically, we try to capture the very essence of the experience by exploring key interactions, then break it down into reusable components, and then radiate outwards from that essence. For an online magazine, it would be reading experience and typography first. For a landing page, it would be the pricing plans and a feature comparison first.</p>

<p>For an ecommerce site it means looking into the components that would make up an extraordinary relevant and useful product page first. That means large image thumbnails, concise copywriting, transparent pricing, exposed ratings and testimonials, psychological anchors, and call-to-action buttons. The visual design decisions made there are then translated to other parts of the interface, specifically forms and labels and error messages in the checkout. Only then, eventually, we reach the category pages and the FAQ pages living on the far outer edges of the experience spectrum. Somewhere in between we explore the front page, but usually we design it late rather than early in the process &mdash; at the point when we’ve established a strong identity already, so we use the front page to amplify and explore it prominently, potentially with a bold design that would exhibit the main qualities of the personality.</p>

<p>Remember overarching connections mentioned earlier in the chapter? A critical part of the design process is to connect modules, so they don’t appear as standalone solutions when put together in the interface. When we have enough modules to build the first prototype, we jump into the browser and build mobile-first. It’s in this process that we finally decide on the grid and the layout and the structure, and implement the connections between modules. In fact, for us, the signature is that magical bond that ties things together.</p>

<p>That’s why we start thinking about the signature of the design when we start designing the heart of the experience, and sometimes even before that. Spreadsheets exploring error messages, visual experiments around shapes and colors and type, as well as user interviews help us get there. Eventually, decisions made for the first prototype can be reused for other pages, yet sometimes we need to run the process from the start again &mdash; as some pages clearly will be one-offs, such as the landing page or a front page. They will still exhibit relationships to everything else because they are designed and built using the personality traits that have been solidified by this point.</p>

<p>It’s these relationships that would then lay the main foundation of a design system, along with components and examples of the interface in use. Too often style guides show a component in isolation, along with Sass class names and a code snippet, without including how that component should appear and behave in relation to other modules on the page. Examples matter both for designers and developers, and they give a good reason to both visit and keep the design system up to date in the long-term.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/86804105-06c0-4763-82be-bac79b0a63bf/bringing-personality-back-grid7.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/86804105-06c0-4763-82be-bac79b0a63bf/bringing-personality-back-grid7.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/86804105-06c0-4763-82be-bac79b0a63bf/bringing-personality-back-grid7.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/86804105-06c0-4763-82be-bac79b0a63bf/bringing-personality-back-grid7.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/86804105-06c0-4763-82be-bac79b0a63bf/bringing-personality-back-grid7.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/86804105-06c0-4763-82be-bac79b0a63bf/bringing-personality-back-grid7.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/86804105-06c0-4763-82be-bac79b0a63bf/bringing-personality-back-grid7.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			(Image courtesy: Andrew Clarke) ()
		</figcaption>
	
</figure>












<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8ad0e3c6-2952-4920-92d3-2d9a46649db1/bringing-personality-back-grid3.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8ad0e3c6-2952-4920-92d3-2d9a46649db1/bringing-personality-back-grid3.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8ad0e3c6-2952-4920-92d3-2d9a46649db1/bringing-personality-back-grid3.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8ad0e3c6-2952-4920-92d3-2d9a46649db1/bringing-personality-back-grid3.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8ad0e3c6-2952-4920-92d3-2d9a46649db1/bringing-personality-back-grid3.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8ad0e3c6-2952-4920-92d3-2d9a46649db1/bringing-personality-back-grid3.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8ad0e3c6-2952-4920-92d3-2d9a46649db1/bringing-personality-back-grid3.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			(Image courtesy: Andrew Clarke) ()
		</figcaption>
	
</figure>












<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d503a144-b34c-4352-98e5-84e2ccc5c170/bringing-personality-back-grid8.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d503a144-b34c-4352-98e5-84e2ccc5c170/bringing-personality-back-grid8.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d503a144-b34c-4352-98e5-84e2ccc5c170/bringing-personality-back-grid8.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d503a144-b34c-4352-98e5-84e2ccc5c170/bringing-personality-back-grid8.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d503a144-b34c-4352-98e5-84e2ccc5c170/bringing-personality-back-grid8.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d503a144-b34c-4352-98e5-84e2ccc5c170/bringing-personality-back-grid8.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d503a144-b34c-4352-98e5-84e2ccc5c170/bringing-personality-back-grid8.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			(Image courtesy: Andrew Clarke) ()
		</figcaption>
	
</figure>












<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/91ab0152-2864-4839-8710-240fd1800159/bringing-personality-back-grid1.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/91ab0152-2864-4839-8710-240fd1800159/bringing-personality-back-grid1.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/91ab0152-2864-4839-8710-240fd1800159/bringing-personality-back-grid1.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/91ab0152-2864-4839-8710-240fd1800159/bringing-personality-back-grid1.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/91ab0152-2864-4839-8710-240fd1800159/bringing-personality-back-grid1.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/91ab0152-2864-4839-8710-240fd1800159/bringing-personality-back-grid1.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/91ab0152-2864-4839-8710-240fd1800159/bringing-personality-back-grid1.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			(Image courtesy: Andrew Clarke) ()
		</figcaption>
	
</figure>












<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/568ca569-5e37-4125-8d35-c4b1767b5c89/bringing-personality-back-planning.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/568ca569-5e37-4125-8d35-c4b1767b5c89/bringing-personality-back-planning.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/568ca569-5e37-4125-8d35-c4b1767b5c89/bringing-personality-back-planning.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/568ca569-5e37-4125-8d35-c4b1767b5c89/bringing-personality-back-planning.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/568ca569-5e37-4125-8d35-c4b1767b5c89/bringing-personality-back-planning.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/568ca569-5e37-4125-8d35-c4b1767b5c89/bringing-personality-back-planning.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/568ca569-5e37-4125-8d35-c4b1767b5c89/bringing-personality-back-planning.png"
			sizes="100vw"
			alt="A storyboard with components"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			A storyboard with components. Each component also has a speed and level of dynamics attached to them. (Image courtesy: Andrew Clarke) ()
		</figcaption>
	
</figure>


<p>We often create user journey maps to understand the flow users go through to accomplish their tasks, and with personality traits in mind, we could even complement them with storyboards, adding some personality highlights at different points of user experience. Besides, in the context of design systems, we could explore not only components in isolation, but also how the design language can use components to slow down or speed up the experience, or provide greater or lesser impact, as well as dynamic and static layout compositions &mdash; very much like we do with showroom and workhorse interactions.</p>

<p>You could even print them out and put them as magnets on a storyboard, so designers can freely move them around and thus explore ways of combining predictable components in unpredictable ways. That’s what Andrew Clarke does when embedding art direction and storytelling in his designs &mdash; very much like comic strip designers arrange the frames according to narrative dynamics and impact when laying out a comic story.</p>

<p>The design signature lies at the very heart of the design. It’s an strand that connects the components in the interface, and it’s what helps designers stay on track when maintaining or evolving a design language. Deciding on the personality traits first helps drive the direction of the design, and can be just a good enough constraint to dissolve initial intentions and goals into tangible, distinguishable attributes that could eventually become the heart of the experience.</p>

<h3 id="wrapping-up">Wrapping Up</h3>

<p>As much as we could get seduced by the charm of a website, in the end, the main purpose of it shouldn’t be self-indulgence. Expressions of the personality of the site enable emotional connections with customers and visitors, and because they are human by their nature, they outline a path to authentic, honest, and respectful interfaces. It’s up to us to figure out how to shape that path and the outcome ahead of us.</p>

<p>Now, it might not be for everybody, and perhaps not every site needs a personality in the first place, or perhaps it should be subtle and express itself in little nuances here and there. I hope that in either of these cases, once flipping over the last page of this book, you’ll have a good enough tool belt of ideas and techniques to create unique and humane experiences &mdash; experiences people could fall in love with.</p>

<hr />

<p><em>I’d like to express sincere gratitude to Jen Simmons, Rachel Andrew, Andrew Clarke, Dan Mall, Espen Brunborg, and Elliot Jay Stocks for inspiring work, contributions, and help in discussing the idea of art direction on the web, and making the web more diverse and experimental. I’d also like to thank Marko Dugonjić, Alberta Soranzo, Sashka Maximova, Lilia Zinchenko, Stefan Bucher, Benoit Henry, Nils Mielke, Thord D. Hedengren, and Bertrand Lirette for reviewing the chapter, as well as our fantastic community, which has shared techniques and lessons learned from its work for everybody to use. You are truly smashing!</em></p>

<hr />

<p><em>The brand new . It contains everything you need to know on how to tackle the new adventures web design and development are bringing along. No theory &mdash; just things that worked in practice.</em></p>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(ra, og, yk, il)</span>
</div>


              </article>
            </body>
          </html>
---------------
<h1 id="#title_2" >3、WWDC 2018 Diary Of An iOS Developer</h1>
Lou Franco
[https://www.smashingmagazine.com/2018/06/wwdc-2018-diary-ios-developer/](https://www.smashingmagazine.com/2018/06/wwdc-2018-diary-ios-developer/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/06/wwdc-2018-diary-ios-developer/" />
              <title>WWDC 2018 Diary Of An iOS Developer</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>WWDC 2018 Diary Of An iOS Developer</h1>
                  
                    
                    <address>Lou Franco</address>
                  
                  <time datetime="2018-06-14T13:45:32&#43;02:00" class="op-published">2018-06-14T13:45:32+02:00</time>
                  <time datetime="2018-06-14T18:32:54&#43;00:00" class="op-modified">2018-06-14T18:32:54+00:00</time>
                </header>
                

<p>The traditional boundaries of summer in the US are Memorial and Labor Day, but iOS developers mark the summer by WWDC and the iPhone release. Even though the weather is cool and rainy this week in NYC, I’m in a summer mood and looking forward to the renewal that summer and WWDC promise.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5f668c12-dd91-4f44-a118-2f9f59c94b5e/wwdc-2018-diary-intro-wwdc.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5f668c12-dd91-4f44-a118-2f9f59c94b5e/wwdc-2018-diary-intro-wwdc.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5f668c12-dd91-4f44-a118-2f9f59c94b5e/wwdc-2018-diary-intro-wwdc.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5f668c12-dd91-4f44-a118-2f9f59c94b5e/wwdc-2018-diary-intro-wwdc.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5f668c12-dd91-4f44-a118-2f9f59c94b5e/wwdc-2018-diary-intro-wwdc.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5f668c12-dd91-4f44-a118-2f9f59c94b5e/wwdc-2018-diary-intro-wwdc.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5f668c12-dd91-4f44-a118-2f9f59c94b5e/wwdc-2018-diary-intro-wwdc.jpg"
			sizes="100vw"
			alt="Photo in front of the San Jose McEnery Convention Center"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			WWDC ()
		</figcaption>
	
</figure>


<p>It’s the morning of June 4th, and I’m reviewing my notes from  after the Core ML announcement.</p>

<p>Apple did release . But from the outside, Core ML seems mostly to have one obvious use: image classification. There doesn’t seem to be a lot of energy around exploring wildly different applications (even though we all know the ML is at the core of self-driving cars and whiz-bang demos like Google Duplex).</p>



<aside class="product-panel product-panel__tilted product-panel--book" data-audience="non-subscriber">
    <div class="container product-panel--book__container">
      <div class="panel__description panel__description--book">
    <p>What if there was a web conference without... slides? Meet <strong>. June <span class="small-caps">26–27</span>. With everything from live designing to live performance audits.</p>
      <a href="http://smashed.by/confpanelspeakers" class="btn btn--green btn--large">
        Check the speakers&nbsp;→
      </a>
      </div>
      <div class="panel__image panel__image--book">
        <a href="http://smashed.by/confpanelspeakers" class="books__book__image">
        <div class="books__book__img">
          <img src="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5a0383cf-197a-49b9-975a-9d1f02c1ace9/dan-hov.png" alt="SmashingConf Toronto 2018, with Dan Mall, Sara Soueidan, Lea Verou and many others." width="310" height="400">
        </div>
      </a>
      </div>
    </div>
  </aside>




<p>Another way Apple uses ML is in Siri, and earlier this year, I wrote about  and mentioned its perceived and real deficiencies when compared to Alexa and Google. One issue I explored was how Siri’s emphasis on pre-defined intents limits its range but hasn’t produced the promised accuracy that you might get from a bounded focus.</p>

<p>The introduction of HomePod last year only highlighted Siri’s woes, and a  showed 98% satisfaction with iPhone X but only a 20% satisfaction with Siri.</p>

<p>With all of this in the back of my mind, I personally was hoping to hear that Apple was going to make some major improvements in AR, ML, and Siri. Specifically, as an iOS developer, I wanted to see many more Core ML models, spanning more than just image classification and more help in making models. For Siri, I wanted to see many more intents and possibly some indication that intents would be a thing that would be added year round. It was a long-shot, but for AR, the next step is a device. But in the meantime, I hoped for increased spatial accuracy.</p>

<p>Finally, I love Xcode Playgrounds and iPad Playground books, but they need to to be a lot faster and stable, so I was hoping for something there too.</p>

<p>On the morning of WWDC, :</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/75e60355-3514-49ca-b90a-5cd66ba1958c/wwdc-2018-diary-day-1-tweet.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/75e60355-3514-49ca-b90a-5cd66ba1958c/wwdc-2018-diary-day-1-tweet.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/75e60355-3514-49ca-b90a-5cd66ba1958c/wwdc-2018-diary-day-1-tweet.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/75e60355-3514-49ca-b90a-5cd66ba1958c/wwdc-2018-diary-day-1-tweet.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/75e60355-3514-49ca-b90a-5cd66ba1958c/wwdc-2018-diary-day-1-tweet.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/75e60355-3514-49ca-b90a-5cd66ba1958c/wwdc-2018-diary-day-1-tweet.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/75e60355-3514-49ca-b90a-5cd66ba1958c/wwdc-2018-diary-day-1-tweet.png"
			sizes="100vw"
			alt="An image of a tweet with my WWDC wishes"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			My tweet describing what I was hoping for from WWDC 2018 ()
		</figcaption>
	
</figure>


<p>This wasn’t a prediction. It’s just a list of things I wanted to use in 2017 but found them underpowered or too hard for me to get started with, and was hoping Apple would make some improvements.</p>

<p>My plan for the day is to watch the keynote live, and then to watch the Platforms State of the Union. Those give a good overview of what to concentrate on for the rest of the week.</p>

<h3 id="end-of-day-1-the-keynote-and-platforms-state-of-the-union">End Of Day 1: The Keynote And Platforms State Of The Union</h3>

<p>The first day of WWDC is the , which is an overview of the entire event, with some details for developers so that they can choose which sessions to attend.</p>

<h4 id="summary-of-notable-non-ios-developer-announcements">Summary Of Notable, Non-iOS Developer Announcements</h4>

<p>WWDC is not entirely about iOS development, so here’s a quick list of other things that happened to the other platforms or that are not very developer focused.</p>

<ul>
<li>To get it out of the way, there were <strong>no hardware announcements at all</strong>. No previews and no updates on the Mac Pro. We’ll have to wait for the iPhone and follow-on events in the fall.</li>
<li>iOS 12 has a new Shortcuts app that seems to be the result of their acquisition of Workflow. It’s a way to <strong>“script” a series of steps via drag and drop</strong>. You can also assign the shortcut to a Siri keyword, which I’ll be covering below.</li>
<li>iOS will <strong>automatically group notifications</strong> that are from the same app and let you act on them as a group.</li>
<li>Animojis can now mimic you sticking out your tongue, and the new <strong>Memojis are highly configurable human faces</strong> that you can customize to look like yourself.</li>
<li><strong>FaceTime supports group video chat</strong> of up to 32 people.</li>
<li>There is a new <strong>Screen Time app that gives you reports on your phone and app usage</strong> (to help you control yourself and be less distracted). It is also the basis of new parental controls.</li>
<li>Apple TV got a small update: Support for Dolby Atmos and new <strong>screen savers taken from the International Space Station</strong>.</li>
</ul>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/75a1ff08-72f1-41d3-a519-39cd1f3ec655/wwdc-2018-diary-intro-tv-space.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/75a1ff08-72f1-41d3-a519-39cd1f3ec655/wwdc-2018-diary-intro-tv-space.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/75a1ff08-72f1-41d3-a519-39cd1f3ec655/wwdc-2018-diary-intro-tv-space.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/75a1ff08-72f1-41d3-a519-39cd1f3ec655/wwdc-2018-diary-intro-tv-space.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/75a1ff08-72f1-41d3-a519-39cd1f3ec655/wwdc-2018-diary-intro-tv-space.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/75a1ff08-72f1-41d3-a519-39cd1f3ec655/wwdc-2018-diary-intro-tv-space.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/75a1ff08-72f1-41d3-a519-39cd1f3ec655/wwdc-2018-diary-intro-tv-space.jpg"
			sizes="100vw"
			alt="Photo of the new Apple TV Space Screen Saver"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Apple TV Space Screen Saver ()
		</figcaption>
	
</figure>


<ul>
<li><strong>The Watch got a competition mode</strong> for challenging others to workout-related challenges. It will also try to <strong>auto-detect the beginning and end of workouts</strong> in case you forget to start or stop them, and it now has Hiking and Yoga workouts.</li>
<li>The Watch also has a new Walkie-Talkie mode that you can enable for trusted contacts.</li>
<li>There are <strong>more audio SDKs that are native on the Watch</strong>, and Apple’s Podcasts app is now available. I expect third-party podcast apps will take advantage of these new SDKs as well.</li>
<li>The Mac got the anchor spot of the event (which is hopefully an indication of renewed attention). It will be called <strong>macOS Mojave and features a  dark mode</strong>.</li>
<li>There are big updates to the Mac App Store, but notably, it now gets the <strong>same visual and content treatment the iOS App Store</strong> got last year. There are enough changes to the sandbox that <strong>Panic has decided to move Transit back there</strong>.</li>
<li><strong>Quick Look in the Finder now has some simple actions</strong> you can do to the file (e.g. rotating an image) and is customizable via Automator.</li>
<li><strong>Mojave will be the last version of macOS to support 32-bit</strong> apps and frameworks, which means the Quick Time Framework going away. It has seemingly been replaced with some video capture features in the OS itself.</li>
<li>Apple announced that they are internally using <strong>a port of UIKit to make Mac apps</strong> and showed ports of Stocks, News, Home, and Voice Memos. The new framework will be released in 2019.</li>
</ul>

<h4 id="the-ios-developer-announcements-i-m-most-excited-about">The iOS Developer Announcements I’m Most Excited About</h4>

<p>iOS Developers got some good news as well. They hit on the four major areas I wanted to see improvement on:</p>

<ul>
<li>SiriKit now has <strong>custom intents</strong>, which opens up the possibilities quite a bit.</li>
<li>Create ML is a new way to use Xcode Playgrounds to train models via <em>transfer learning</em>, which lets you <strong>augment existing models with your own training data</strong>.</li>
<li>Xcode playgrounds now allow you to <strong>add code to the bottom of a page and run it without restarting</strong>. It’s hard to know if Playgrounds will be more stable until we get a real release in September, but this will make trying code much faster.</li>
<li>ARKit 2 was announced along with a <strong>new Augmented Reality file format called USDZ</strong>, which is open and was developed with Adobe and Pixar. Adobe announced some tooling support already. It will allow users and developers to store and share AR assets and experiences. In addition, ARKit 2 allows multiple devices to be in the same AR environment and supports 3D object detection.</li>
</ul>

<p>We didn’t get an AR device, but it sure feels like we’ll get one soon. And it needs to come from Apple (not third parties) because running ARKit requires an iOS device.</p>

<h4 id="setting-up-your-machine">Setting Up Your Machine</h4>

<p>Everything you need is available now in the . To use the code in the article, you need the Xcode 10 Beta. I would not recommend using iOS 12 Betas yet, but if you really want to, go to the portal on your device and download the iOS 12 Beta Configuration Profile.</p>

<p>The only major thing you need a device with the beta for is ARKit 2. Everything else should run well enough in Xcode 10’s simulator. As of the first beta, Siri Shortcut support in the simulator is limited, but there is enough there to think that that will be fixed in future releases.</p>

<h3 id="end-of-day-2-playing-with-siri-custom-intents">End Of Day 2: Playing With Siri Custom Intents</h3>

<p>Last year, I wrote how you needed to fit within one of Apple’s pre-defined intents in order to . This mechanism was introduced in 2016 and added to in 2017 and even between WWDC events. But it was clear that Amazon’s approach of custom intents was superior for getting voice control into more diverse apps, and Apple added that to SiriKit last week.</p>

<p>To be clear, this is a first implementation, so it’s not as extensive as Alexa Skills just yet, but it opens up Siri’s possibilities quite a bit. As I discussed in the previous article, the main limitation of custom intents is that the developer needs to do all of the language translation. SiriKit gets around this a little by asking the user to provide the phrase that they’d like to use, but there is still more translation needed for custom intents than for predefined intents.</p>

<p>And they built in on the same foundation as the predefined intents, so everything I covered still applies. In fact, I will show you how to add a new custom intent to , the app I wrote for the original SiriKit article.</p>

<h4 id="free-siri-shortcut-support-if-you-already-support-spotlight">(Free) Siri Shortcut Support If You Already Support Spotlight</h4>

<p>If you use <code>NSUserActivity</code> to indicate things in your app that your user can initiate via handoff or search, then it’s trivial to make them available to Siri as well.</p>

<p>All you need to do is add the following line to your activity object:</p>

<pre><code class="language-javascript">activity.isEligibleForPrediction = true
</code></pre>

<p>This will only work for Spotlight-enabled activities (where <code>isEligibleForSearch</code> is <code>true</code>).</p>

<p>Now, when users do this activity, it is considered <em>donated</em> for use in Siri. Siri will recommend very commonly done activities or users can find them in the Shortcuts app. In either case, the user will be able to assign their own spoken phrase in order to start it. Your support for starting the activity via Spotlight is sufficient to support it being started via a shortcut.</p>

<p>In List-o-Mat, we could make the individual lists available to Spotlight and Siri by constructing activity objects and assigning them to the <code>ListViewController</code>. Users could open them via Siri with their own phrase.</p>

<p>It’s redundant in our case because we had a pre-defined intent for opening a list, but most apps are not so lucky and now have this simple mechanism. So, if your app has activities that aren’t supported by Siri’s pre-defined intents (e.g. playing a podcast), you can just make them eligible for prediction and not worry about custom intents.</p>

<h4 id="configuring-sirikit-to-use-custom-intents">Configuring SiriKit To Use Custom Intents</h4>

<p>If you do need to use a custom intent, then SiriKit needs to be added to your app, which requires a bit of configuration.</p>

<p>All of the steps for configuring SiriKit for custom intents are the same as for predefined intents, which is covered in detail in my . To summarize:</p>

<ol>
<li>You are adding an extension, so you need a new App ID, and provisioning profile and your app’s entitlements needs have Siri added.</li>
<li>You probably need an App Group (it’s how the extension and app communicate).</li>
<li>You’ll need an Intents Extension in your project</li>
<li>There are Siri specific <em>.plist</em> keys and project entitlements you need to update.</li>
</ol>

<p>All of the details can be found in my SiriKit article, so I’ll just cover what you need to support a custom intent in List-o-Mat.</p>


  <div id="sponsors-article" data-impression="true" class="c-promo-box c-promo-box--ad sponsors hidden" data-audience="non-subscriber" data-remove="true"></div>



<h4 id="adding-a-copy-list-command-to-list-o-mat">Adding A Copy List Command To List-o-Mat</h4>

<p>Custom intents are meant to be used only where there is no pre-defined intent, and Siri does actually offer a lot of list and task support in its Lists and Notes Siri Domain.</p>

<p>But, one way to use a list is as a template for a repeated routine or process. To do that we’ll want to copy an existing list and uncheck all of its items. The built-in List intents don’t support this action.</p>

<p>First, we need to add a way to do this manually. Here is a demo of this new behavior in List-o-Mat:</p>

<figure><figcaption>Copying a list in List-o-Mat</figcaption></figure>

<p>To get this behavior to be invokable by Siri, we’ll “donate an intent,” which means we’ll tell iOS every time you do this. Then, it will eventually learn that in the morning, you like to copy this list and offer it as a shortcut. Users can also look for donated intents and assign phrases manually.</p>

<h4 id="creating-the-custom-intent">Creating The Custom Intent</h4>

<p>The next step is to create the custom intent in Xcode. There is a new file template, so:</p>

<ol>
    <li>Choose File&nbsp;&rarr;&nbsp;New File and pick “SiriKit Intent Definition File”.<br />
        <figure>)</figcaption></figure>
    </li>
    <li>Name the file <em>ListOMatCustomIntents.intentdefinition</em>, and choose to put the file in both the App and Intent Extension targets. This will automatically generate classes into both targets that implement the intent protocols but have your custom behavior implemented.</li>
    <li>Open the <em>Definition</em> file.</li>
    <li>Use the + button on the bottom left to add an intent and name it “CopyList”.</li>
    <li>Set the Category to “Create” and fill in the title and subtitle to describe the intent:<br />
        <figure>)</figcaption></figure>
    </li>
    <li>Add a String parameter named “list”.<br />
        <figure>)</figcaption></figure>
    </li>
    <li>Add a shortcut type with the list parameter and give it a title named “Copy list”.<br />
        <figure>)</figcaption></figure>
    </li>
</ol>

<p>If you look in the Intent plist, you will see that this intent has already been configured for you:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8c55b7f6-8058-4d4b-ba9d-f6a87499a383/wwdc-2018-diary-day-2-plist.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8c55b7f6-8058-4d4b-ba9d-f6a87499a383/wwdc-2018-diary-day-2-plist.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8c55b7f6-8058-4d4b-ba9d-f6a87499a383/wwdc-2018-diary-day-2-plist.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8c55b7f6-8058-4d4b-ba9d-f6a87499a383/wwdc-2018-diary-day-2-plist.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8c55b7f6-8058-4d4b-ba9d-f6a87499a383/wwdc-2018-diary-day-2-plist.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8c55b7f6-8058-4d4b-ba9d-f6a87499a383/wwdc-2018-diary-day-2-plist.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8c55b7f6-8058-4d4b-ba9d-f6a87499a383/wwdc-2018-diary-day-2-plist.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
</figure>


<h4 id="donating-the-intent">Donating The Intent</h4>

<p>When we do a user interaction in our app that we want Siri to know about, we donate it to Siri. Siri keeps track of contextual information, like the time, day of the week, and even location, and if it notices a pattern, it will offer the shortcut to the user.</p>

<p>When we tap the Copy menu, add this code:</p>

<pre class="break-out"><code class="language-javascript">@available(iOS 12, *)
func donateCopyListInteraction(listName: String) {
    let copyListInteraction = CopyListIntent()
    copyListInteraction.list = listName
    copyListInteraction.suggestedInvocationPhrase = "Copy \(listName)"
    let interaction = INInteraction(intent: copyListInteraction, response: nil)
    interaction.donate { [weak self] (error) in
        self?.show(error: error)
    }
}
</code></pre>

<p>This simply creates an object of the auto-generated <code>CopyListIntent</code> class and donates it to Siri. Normally, iOS would collect this info and wait for the appropriate time to show it, but for development, you can open the Settings app, go to the Developer section, and turn on Siri Shortcut debugging settings.</p>

<p><strong>Note</strong>: <em>As of this writing, with the first betas, this debug setting only works on devices, and not the simulator. Since the setting is there, I expect it to start working in further betas.</em></p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6bc372de-1f4a-49a5-9e07-63443b53625c/wwdc-2018-diary-day-2-dev-settings.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6bc372de-1f4a-49a5-9e07-63443b53625c/wwdc-2018-diary-day-2-dev-settings.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6bc372de-1f4a-49a5-9e07-63443b53625c/wwdc-2018-diary-day-2-dev-settings.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6bc372de-1f4a-49a5-9e07-63443b53625c/wwdc-2018-diary-day-2-dev-settings.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6bc372de-1f4a-49a5-9e07-63443b53625c/wwdc-2018-diary-day-2-dev-settings.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6bc372de-1f4a-49a5-9e07-63443b53625c/wwdc-2018-diary-day-2-dev-settings.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6bc372de-1f4a-49a5-9e07-63443b53625c/wwdc-2018-diary-day-2-dev-settings.png"
			sizes="100vw"
			alt="Screenshot of Siri debug settings"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Turn on Siri Shortcut debugging
		</figcaption>
	
</figure>


<p>When you do this, your donated shortcut shows up on in Siri Suggestions in Spotlight.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b5f761b7-ce7f-4e6e-8edc-30d320cbb3fa/wwdc-2018-diary-day-2-copylist-debug.jpeg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b5f761b7-ce7f-4e6e-8edc-30d320cbb3fa/wwdc-2018-diary-day-2-copylist-debug.jpeg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b5f761b7-ce7f-4e6e-8edc-30d320cbb3fa/wwdc-2018-diary-day-2-copylist-debug.jpeg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b5f761b7-ce7f-4e6e-8edc-30d320cbb3fa/wwdc-2018-diary-day-2-copylist-debug.jpeg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b5f761b7-ce7f-4e6e-8edc-30d320cbb3fa/wwdc-2018-diary-day-2-copylist-debug.jpeg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b5f761b7-ce7f-4e6e-8edc-30d320cbb3fa/wwdc-2018-diary-day-2-copylist-debug.jpeg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b5f761b7-ce7f-4e6e-8edc-30d320cbb3fa/wwdc-2018-diary-day-2-copylist-debug.jpeg"
			sizes="100vw"
			alt="Screenshot of the donated shortcut in Siri"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			You can debug your donated shortcut in search
		</figcaption>
	
</figure>


<p>Tapping that will call into your Intent extension because we are allowing background execution. We’ll add support for that next.</p>

<h4 id="handling-the-custom-intent">Handling The Custom Intent</h4>

<p>We already have an Intents extension, and since the custom intent definitions file is already added to the file, it also has the generated intent classes. All we need to do is add a handler.</p>

<p>The first step is to add a new class, named <code>CopyListIntentHandler</code> to the extension. Here is its code:</p>

<pre class="break-out"><code class="language-javascript">import Intents

@available(iOS 12, *)
class CopyListIntentHandler: ListOMatIntentsHandler, CopyListIntentHandling {

    func handle(intent: CopyListIntent, completion: @escaping (CopyListIntentResponse) -> Void) {

        // Find the list
        var lists = loadLists()
        guard
            let listName = intent.list?.lowercased(),
            let listIndex = lists.index(where: { $0.name.lowercased() == listName})
        else {
            completion(CopyListIntentResponse(code: .failure, userActivity: nil))
            return
        }

        // Copy the list to the top, and respond with success
        copyList(from: &lists, atIndex: listIndex, toIndex: 0)
        save(lists: lists)
        let response = CopyListIntentResponse(code: .success, userActivity: nil)
        completion(response)
    }

}
</code></pre>

<p>Custom intents only have a confirm and handle phase (custom resolution of parameters is not supported). Since the default <code>confirm()</code> returns success, we’ll just implement <code>handle()</code>, which has to look up the list, copy it, and let Siri know if it was successful or not.</p>

<p>You also need to dispatch to this class from the registered intent handler by adding this code:</p>

<pre class="break-out"><code class="language-javascript">if #available(iOS 12, *) {
    if intent is CopyListIntent {
        return CopyListIntentHandler()
    }
}
</code></pre>

<p>Now you can actually tap that Siri suggestion and it will bring this up:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1c76ea5f-b38e-4ca0-af5f-28db47658733/wwdc-2018-diary-day-2-copylist-create.jpeg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1c76ea5f-b38e-4ca0-af5f-28db47658733/wwdc-2018-diary-day-2-copylist-create.jpeg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1c76ea5f-b38e-4ca0-af5f-28db47658733/wwdc-2018-diary-day-2-copylist-create.jpeg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1c76ea5f-b38e-4ca0-af5f-28db47658733/wwdc-2018-diary-day-2-copylist-create.jpeg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1c76ea5f-b38e-4ca0-af5f-28db47658733/wwdc-2018-diary-day-2-copylist-create.jpeg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1c76ea5f-b38e-4ca0-af5f-28db47658733/wwdc-2018-diary-day-2-copylist-create.jpeg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1c76ea5f-b38e-4ca0-af5f-28db47658733/wwdc-2018-diary-day-2-copylist-create.jpeg"
			sizes="100vw"
			alt="Screenshot of the activated shortcut"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Activate the shortcut ()
		</figcaption>
	
</figure>


<p>And tapping the Create button will copy the list. The button says “Create” because of the category we chose in the intent definition file.</p>

<p>Phew, that was a lot. These new Siri shortcuts are the main feature in iOS 12 that has a new large developer surface area to explore. Also, since I happened to have a good (and documented) Siri example to work with, it was reasonable to try to add the new features to it this week.</p>

<p>You can see the update . Until Xcode 10 and iOS 12 are released it’s in its own branch.</p>

<p>The next few days, I’ll mostly be looking at Apple sample code or making much smaller projects.</p>

<h3 id="end-of-day-3-xcode-playgrounds">End Of Day 3: Xcode Playgrounds</h3>

<p>The entire previous day was spent in Xcode 10 beta, which didn’t crash once and seemed ready for development. So now I wanted to explore the new Playgrounds features.</p>

<p>The main thing I wanted from playgrounds is to make them more stable and much faster. To make them faster, Apple added a big feature — a REPL mode.</p>

<p>Before Xcode 10, when you were in a Playground that had auto-run on (which is the default), every line of code actually rebuilt the entire file and ran it from the beginning. If you had built up any state, it was lost. But, the real issue was that this was way too slow for iterative development. When I use Playgrounds, I set them to manually run, but even that is slow.</p>

<p>In Xcode 10, manual running is more the norm, but after you run it, you can add more lines at the bottom of the page and continue execution. This means you can explore data and draw views iteratively without constantly rebuilding and starting from scratch.</p>

<p>To get started, I created an iOS playground (File&nbsp;&rarr;&nbsp;New&nbsp;&rarr;&nbsp;Playground) with the Single View template.</p>

<p>Turn on manual running by bringing down the menu below the Play button (the triangle in the bottom left corner). This puts a vertical strip to the left that shows the current position of the Play head (kind of like breakpoints).</p>

<p>You can tap any line and then tap the play button to its left. This will run the Playground to this point. Then you can go further by tapping lines lower in the Playground. Critically, you can add more lines to the bottom and type <kbd>Shift</kbd> + <kbd>Enter</kbd> after each one to move the Play head to that point.</p>

<p>Here’s a GIF of me changing the label of a view without needing to restart the Playground. After each line I type, I am pressing <kbd>Shift</kbd> + <kbd>Enter</kbd>.</p>

<figure><figcaption>Add more code and run it without restarting</figcaption></figure>

<p>Playgrounds also support custom rendering of your types now, and Apple is making a big push for every Swift framework to include a Playground to document it.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e3a7770e-c5c7-4a97-ac70-adf61b548e90/wwdc-2018-diary-day-3-playground-all-the-things.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e3a7770e-c5c7-4a97-ac70-adf61b548e90/wwdc-2018-diary-day-3-playground-all-the-things.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e3a7770e-c5c7-4a97-ac70-adf61b548e90/wwdc-2018-diary-day-3-playground-all-the-things.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e3a7770e-c5c7-4a97-ac70-adf61b548e90/wwdc-2018-diary-day-3-playground-all-the-things.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e3a7770e-c5c7-4a97-ac70-adf61b548e90/wwdc-2018-diary-day-3-playground-all-the-things.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e3a7770e-c5c7-4a97-ac70-adf61b548e90/wwdc-2018-diary-day-3-playground-all-the-things.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e3a7770e-c5c7-4a97-ac70-adf61b548e90/wwdc-2018-diary-day-3-playground-all-the-things.png"
			sizes="100vw"
			alt="WWDC photo showing slide to encourage more Playgrounds"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			TJ Usiyan asks WWDC attendees to add Playgrounds to their projects. ()
		</figcaption>
	
</figure>


<h3 id="end-of-day-4-create-ml">End Of Day 4: Create ML</h3>

<p>Last year, Apple made a big leap for programming Machine Learning for their devices. There was a new ML model file format and direct support for it in Xcode.</p>

<p>The potential was that there would be a large library of these model files, that there would be tools that would create them, and that many more app developers would be able to incorporate ML into their projects without having to know how to create models.</p>

<p>This hasn’t fully materialized. Apple didn’t add to the repository of models after WWDC, and although there are third-party repositories, they mostly have models that are variations on the image classification demos. ML is used for a lot more than image classification, but a broad selection of examples did not appear.</p>

<p>So, it became clear that any real app would need its developers to train new models. Apple released  for this purpose, but its far from simple.</p>

<p>At WWDC 2018, Apple did a few things to Core ML:</p>

<ol>
<li>They <strong>expanded the Natural Language Processing (NLP) part of Core ML</strong> which gives us a new major domain of examples.</li>
<li>They added the concept of <em>Transfer Learning</em> to Core ML, which allows you to <strong>add training data to an existing model</strong>. This means you can take models from the library, and customize them to your own data (for example, have them recognize new objects in images you provide).</li>
<li><strong>They released Create ML which is implemented inside of Xcode Playgrounds</strong> and lets you drag and drop data for training and generate model extensions (using Transfer Learning).</li>
</ol>

<p>This is another nice step in democratizing ML. There’s not much code to write here. To extend an image classifier, you just need to gather and label images. Once you have them, you just drag them into Create ML. You can see the demo in this .</p>

<h3 id="end-of-the-week-play-with-the-new-ar-demos">End Of The Week: Play With The New AR Demos</h3>

<p>ARKit was another big addition last year and it seems even more clear that an AR device is coming.</p>

<p>My  is still a good way to get started. Most of the new features are about making AR more accurate and faster.</p>

<p>After that, if you have installed a beta, you will definitely want to download the new . This app takes advantage of the new features of ARKit, especially the multi-player experience. Two or more devices on the same network and in the same place, can communicate with each other and see the same AR experience.</p>

<p>Of course, to play this, you need two or more devices you are willing to put on the iOS 12 beta. I’m waiting for the public beta to do this because I only have one beta-safe device.</p>

<p>The easier AR app to play with is the new Measure app, which allows you to measure the length of real objects you see in AR camera view. There have been third-party apps that do this, but Apple’s is polished and pre-installed with iOS 12.</p>

<h3 id="links-to-wwdc-videos-and-sample-code">Links To WWDC Videos And Sample Code</h3>

<p>So, I’m looking forward to doing more with Xcode 10 and iOS 12 this summer while we wait for the new phones and whatever devices Apple might release at the end of the summer. In the meantime, iOS developers can enjoy the sun, track our hikes with our new beta Watch OS, and watch these WWDC videos when we get a chance.</p>

<p>.</p>

<p>Here are the videos referenced in this article:</p>

<ul>
<li></li>
<li></li>
<li></li>
<li></li>
<li></li>
</ul>

<p>To start playing with Xcode 10 and iOS 12:</p>

<ul>
<li> (visit on a device to get the beta profile)</li>
<li></li>
<li> (the multi-player ARKit 2 game)</li>
</ul>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(ra, il)</span>
</div>


              </article>
            </body>
          </html>
---------------
<h1 id="#title_3" >4、文章： 一文看懂.NET的各种变体</h1>
Wayne Citrin
[http://www.infoq.com/cn/articles/varieties-dotnet?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/varieties-dotnet?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/varieties-dotnet/zh/smallimage/Understanding-the-Varieties-of-dotNET-1528373714065-1528991915779.jpeg"/><p>本文的目标不是要深入到各种.NET的技术细节中，关于技术细节已经有大量的技术资源可参考。相反，本文的目的是澄清一个简单的问题：在特定情况下应该使用哪种.NET？</p> <i>By Wayne Citrin</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_4" >5、文章： 中小企业如何做好推荐系统？</h1>
庄正中
[http://www.infoq.com/cn/articles/how-can-micro-enterprise-build-a-good-recommendation-system?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/how-can-micro-enterprise-build-a-good-recommendation-system?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/how-can-micro-enterprise-build-a-good-recommendation-system/zh/smallimage/DNUN-logo-small-1528992292838.jpg"/><p>对于中小企业来说，拥有一个优质的推荐系统可以让诸多业务问题迎刃而解，然而大部分企业只想着应用 AI，却不知道怎样的推荐系统是适合自身业务的，本文作者是来自荔枝 FM 的数据挖掘工程师兼 AI 工程师，本文他将为读者解答中小企业如果做一套好推荐系统。</p> <i>By 庄正中</i>
---------------
<h1 id="#title_5" >6、人脸识别技术的真相</h1>
Alexis Perrier
[http://www.infoq.com/cn/news/2018/06/face-recognition-technology?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/06/face-recognition-technology?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>人脸识别是机器学习的直接应用，这项技术已经被消费者、行业和执法机关广泛采用，它可能为我们的日常生活带来了便利，但也有严重的隐私问题。人脸识别已经超过了人类的工作效率，但是，在某些应用中实际实现时还存在问题。</p> <i>By Alexis Perrier</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_6" >7、Instana支持基于AI驱动的AWS Lambda应用程序监控</h1>
Helen Beal
[http://www.infoq.com/cn/news/2018/06/instana-ai-monitoring-lambda?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/06/instana-ai-monitoring-lambda?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Instana是一家提供动态容器化微服务监控服务的云原生供应商，他们的监控服务基于人工智能。最近他们宣布支持无服务器计算平台AWS Lambda，已上架AWS Marketplace。</p> <i>By Helen Beal</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_7" >8、麻省理工研究人员在比特币闪电网络上测试Oracle和智能合约</h1>
Kent Weare
[http://www.infoq.com/cn/news/2018/06/Bitcoin-Lightning-Oracles?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/06/Bitcoin-Lightning-Oracles?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>麻省理工学院（MIT）透露了他们在比特币闪电网络上运行智能合约的测试结果。研究人员Tadge Dryja和Alin S. Dragos最近在Coindesk分享了这些结果。在比特币网络上运行智能合约并不是新鲜事，不过，信任实体Oracle与智能合约相结合的方法在比特币区块链中显得独一无二。</p> <i>By Kent Weare</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_8" >9、文章： Weex技术在苏宁移动办公开发中的实践</h1>
陈思佳
[http://www.infoq.com/cn/articles/weex-in-suning-mobile-officing-practice?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/weex-in-suning-mobile-officing-practice?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/weex-in-suning-mobile-officing-practice/zh/smallimage/logo-how-technology-smal-llogo-1528807242487-1528939691758.jpg"/><p>Weex是一套简单易用的跨平台开发方案，能以web的开发体验构建高性能、可扩展的native应用，为了做到这些，Weex与 Vue合作，使用 Vue 作为上层框架，并遵循 W3C 标准实现了统一的 JSEngine 和 DOM API，打造三端一致的 native 应用。</p> <i>By 陈思佳</i>
---------------
<h1 id="#title_9" >10、文章： 通俗解读“AWS VPC子网”</h1>
Prasad Vara
[http://www.infoq.com/cn/articles/aws-vpc-explained?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/aws-vpc-explained?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/aws-vpc-explained/zh/smallimage/Merge-Replication-CRDT-logo-1528485981783-1528939339268.jpeg"/><p>在本文中，我们将讨论AWS中可用的、不同类型的VPC设置。然后，我们还将介绍VPC中的核心术语，并对主要组件进行解释。</p> <i>By Prasad Vara</i> <i> Translated by 陈亮芬</i>
---------------