## 文章索引
1、 <a href="#1每周分享第-19-期" >每周分享第 19 期</a><br/>
2、 <a href="#2图灵奖得主john-hopcroft李开复博士吴恩达做导师300学生5周培训后成ai工程师" >图灵奖得主John Hopcroft，李开复博士，吴恩达做导师，300学生5周培训后成“AI工程师”</a><br/>
3、 <a href="#3文章-区块链性能测评实战案例" >文章： 区块链性能测评实战案例</a><br/>
4、 <a href="#4是什么成就了中国最具创新力的公司帮他们的超脑计划孵出阿尔法蛋" >是什么成就了中国最具创新力的公司，帮他们的超脑计划孵出阿尔法蛋？</a><br/>
5、 <a href="#5android-smart-linkify-api背后的机器学习" >Android Smart Linkify API背后的机器学习</a><br/>
6、 <a href="#6liftbridge为nats提供了类kafka的日志api" >Liftbridge为NATS提供了类Kafka的日志API</a><br/>
7、 <a href="#7甘特更新企业敏捷规划工具的魔力象限" >甘特更新企业敏捷规划工具的魔力象限</a><br/>
8、 <a href="#8微软必应从net-core-21获得了性能提升" >微软必应从.NET Core 2.1获得了性能提升</a><br/>
9、 <a href="#9微软驱动模块框架旨在简化windows驱动开发" >微软驱动模块框架旨在简化Windows驱动开发</a><br/>
10、 <a href="#10johnny-five-is-alive-ghost-20-and-stimulus" >Johnny Five is alive, Ghost 2.0, and Stimulus</a><br/><h1 id="#title_0" >1、每周分享第 19 期</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2018/08/weekly-issue-19.html](http://www.ruanyifeng.com/blog/2018/08/weekly-issue-19.html)
<p>这里记录过去一周，我看到的值得分享的东西，每周五发布。</p>

        <p><img src="https://www.wangbase.com/blogimg/asset/201808/bg2018082401.jpg" alt="" title="" /></p>

<p>上周，我看了电影《头号玩家》（Ready Player One）。这是今年的新片，如果你还没看过，我推荐去看一下。不是因为它有多精彩，而是因为这部电影就是未来的真实场景。</p>

<p>未来存在两种世界：真实世界和电子游戏创造的虚拟世界。真实世界里面，你是一个其貌不扬、处处受挫、穷困无聊的鲁蛇（loser）。没关系，你可以去虚拟世界。那里，你会有一个俊美潇洒的化身（avatar），在各种壮丽好玩的场所漫游，还可能成为众人景仰的英雄。</p>

<p>《头号玩家》的主人公就是这样的人物，他不上学也没工作，住在贫民区的集装箱，偷吃别人冰箱里面的食品填饱肚子。但是，他在虚拟世界里面解出了三道谜题，拯救了世界。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201808/bg2018082402.jpg" alt="" title="" /></p>

<p>随着技术的进步，虚拟世界越来越逼真，越来越好玩，而真实世界的生存难度也越来越高，那么一定会有越来越多的人沉迷于虚拟世界。对他们来说，虚拟世界远比真实世界更有意思和意义。虚拟世界的角色更像自己。</p>

<p>虚拟世界唯一不能解决的，是人的生理需求。我们必须在真实世界里面睡觉、吃饭、上厕所......如果能够制造一种机器，类似胶囊旅馆，玩家躺在里面，不用出来就能解决一切生理需求，让你在虚拟世界里面连续玩一个月。那样的话，真实世界还有人愿意回来吗？</p>

<h2>新闻</h2>

<p>1、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201808/bg2018082403.jpg" alt="" title="" /></p>

<p>《国家地理》杂志的长篇报道，美国一起换脸手术的全过程。现年22岁的 Katie Stubblefield （左图）2014年遇到感情问题，在哥哥住家的厕所中，朝着自己的脸部开枪自寻短见。</p>

<p>Katie 被送往医院急救，虽然成功保住性命，但脸部严重毁容，从头皮、额头、眼皮、鼻子、下颚等都受到重创。2016年3月，Katie 列入换脸手术等候名单，等了14个月才成功找到捐赠者。她的新脸来自一名因服药过量而身亡的31岁女子Adrea Schneider（右图）。2017年5月4日，Katie 接受了长达31个小时的换脸手术,共有11名外科医生和数名专家参与了这项手术。</p>

<p>原报道有多张图片，可能会引起不适，谨慎点击。</p>

<p>2、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201808/bg2018082404.jpg" alt="" title="" /></p>

<p>使用机器学习算法，为维基百科添加条目。第一步是收集30,000篇关于科学家的维基百科文章，用来训练算法怎么写人物条目。然后，从学术搜索引擎里面找出20万名科学家的名单，发现哪些人还没有条目，再根据新闻报道和他们的论文，生成完整的传记条目添加到维基百科。</p>

<p>3、</p>

<p>德国科学家找了89个志愿者，要求他们与机器人互动。互动结束后，志愿者必须关掉机器人，这时机器人发出哀求，希望不要被关掉，说自己这样会很痛苦，并有哭泣声。</p>

<p>结果，43个志愿者犹豫了，其中13个人因此没有关掉机器人。这说明人也会被机器人打动，或者说被操纵。</p>

<p>4、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201808/bg2018082405.jpg" alt="" title="" /></p>

<p>BBC 报道，英国科学家将一个生物工程肺移植到了猪体内。</p>

<p>科学家首先从供体猪获取肺部，然后去除所有细胞和血管，只留下了一个由蛋白质组成的支撑架。然后，再将受体猪的干细胞放到这个"支撑架"上，用生物因子促进它的生长和分裂，直至长成一个生物工程肺。这样做的目的是，由于肺是由自体干细胞生成的，可以大大地降低排斥反应。</p>

<p>如果这种技术可以运用于人类，那将改变器官移植来源不足和排斥反应的问题。</p>

<p>5、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201808/bg2018082406.jpg" alt="" title="" /></p>

<p>乐高推出纯天然的积木，使用甘蔗制造。该公司计划，到2030年大部分产品都使用环保材料或再生资源制造。</p>

<p>6、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201808/bg2018082407.jpg" alt="" title="" /></p>

<p>由于美国的校园枪击案高发，一家公司研发出了枪支自动识别系统。只要校内的监视器识别出枪支，就立刻报警。</p>

<p>7、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201808/bg2018082408.jpg" alt="" title="" /></p>

<p>科学家早就发现，南极冰川上流淌着血红的液体，被称为"南极血瀑"。这些红色液体是从哪里来的？最近终于找到了答案。原来冰川的下面有一个地下湖，水质含有大量的铁元素，因此呈现红色。冰川的挤压作用，将地下水挤到了冰川表面，形成了血瀑。</p>

<p>8、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201808/bg2018082409.jpg" alt="" title="" /></p>

<p>苹果手机和 iPad 使用的是 lightning 充电口，而不是其他手机的 USB 充电口，这导致苹果必须使用专门的充电设备。</p>

<p>欧盟正在考虑，强迫苹果将充电口改成 USB。这是为了保护环境，统一充电接口，降低每年51000吨废弃的充电设备。苹果公司的回应是，它将提供 lightning 到 USB 的适配器。目前，还不清楚欧盟会不会接受这种措施。</p>

<p>9、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201808/bg2018082410.jpg" alt="" title="" /></p>

<p>微软的海底机房项目，带有两个外部摄像头，现在全天直播海底世界，看上去鱼儿很喜欢这个东西（也许与它会散热有关）。</p>

<p>10、<strong>一句话新闻</strong></p>

<ul>
<li>最新版已不再信任赛门铁克证书，其他浏览器很快也会跟进。</li>
<li>是美国房价最高的城市，有很多无家可归的流浪汉，街头大便已经成了社会公害。截止8月13日，已有14597通投诉电话，平均每天65通。</li>
<li>继支持 Node 8.0 以后，内置 Puppeteer （无头版 Chrome 浏览器）。</li>
</ul>

<h2>教程</h2>

<p>1、（英文）</p>

<p>如果你需要在 Python 语言用到随机数，看这篇文章就够了。</p>

<p>2、（英文）</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201808/bg2018082411.jpg" alt="" title="" /></p>

<p>Cherry 是世界最著名的机械键盘品牌，这篇文章介绍这个品牌的历史。</p>

<p>3、（英文）</p>

<p>Python 初级语法教程。</p>

<p>4、（英文）</p>

<p>提高 SSH 安全等级的一些知识。本文较难，需要密码学知识。</p>

<p>5、（英文）</p>

<p>Google 官方介绍 Kubernetes 这个项目是怎么诞生的。</p>

<p>6、（英文）</p>

<p>这组系列文章介绍脚本语言的运行虚拟机（VM）怎么写。</p>

<p>7、（英文）</p>

<p>本文从 C 程序员的角度比较 C++、Go、Rust 这三种语言。</p>

<p>8、（英文）</p>

<p>WireGuard 仍然是一个实验性的新产品，目前只有 Linux 和安卓客户端。</p>

<p>9、（英文）</p>

<p>从一个失败的正则表达式解释正则引擎的运行原理。</p>

<p>10、（英文）</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201808/bg2018082412.jpg" alt="" title="" /></p>

<p>本文使用鸽子传信作为比喻，解释 HTTPS 协议。</p>

<p>11、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201808/bg2018082413.jpg" alt="" title="" /></p>

<p>Debian 是历史最悠久、使用最广泛的 Linux 发行版之一。今年8月16日是它25周年的生日，本文介绍一些它的小知识。</p>

<h2>资源</h2>

<p>1、（英文）</p>

<p>fast.ai 免费的深度学习课程。</p>

<p>2、（英文）</p>

<p>《哥德尔、埃舍尔、巴赫》一书的解读。</p>

<p>3、（英文）</p>

<p>介绍计算机底层知识的免费电子书。</p>

<p>4、</p>

<p>谷歌的一个数据可视化项目，将14000种鸟叫进行分类，可以在页面上选择收听这些鸟叫。</p>

<p>5、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201808/bg2018082414.jpg" alt="" title="" /></p>

<p>MacOS system6 是 Macintosh计算机的操作系统，1988年由苹果公司发布。这里用虚拟机在浏览器里面启动这个操作系统。</p>

<h2>工具</h2>

<p>1、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201808/bg2018082415.jpg" alt="" title="" /></p>

<p>Git 操作，你喜欢使用命令行还是图形界面？这个项目可以在命令行提供 Git 的图形界面。</p>

<p>2、</p>

<p>一个命令行音乐播放器，支持 Spotify, Google Play Music, YouTube 等服务。</p>

<p>3、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201808/bg2018082416.jpg" alt="" title="" /></p>

<p>团队登录服务器的 SSH 管理工具。</p>

<p>4、</p>

<p>Python 语言写的短网址服务，前后端代码都包括。</p>

<p>5、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201808/bg2018082417.jpg" alt="" title="" /></p>

<p>一个点对点通信的聊天工具，主打信息加密。</p>

<p>6、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201808/bg2018082418.jpg" alt="" title="" /></p>

<p>这是一个开源的低成本单板电脑，可以在家里自己制造。</p>

<p>7、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201808/bg2018082419.jpg" alt="" title="" /></p>

<p>一个适用于远程办公团队的 App，它要求每个成员每天贴一段自己的视频"露露脸"。</p>

<p>8、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201808/bg2018082420.jpg" alt="" title="" /></p>

<p>Ghost 是一个博客软件，类似 Wordpress。最近发布了2.0版，更换了编辑器，并且提供很多新功能。新编辑器的最大特点是增加了 Card，可以嵌入各种资源。</p>

<p>9、</p>

<p>JWL 是一种软件许可证，称为公平世界许可证。采用这个许可证的软件，不道德的行业不得使用，包括烟草，赌博，贩卖人口，奴役，仇恨言论的提供者等等。 它是BSD 3许可证的扩展。</p>

<h2>文摘</h2>

<p>1、</p>

<p>以下摘自比尔布莱森的《万物简史》。</p>

<p>生命的出现，首先需要有一个合适的恒星。这个恒星必须大到足以辐射很大的热量，又不能太大，以至于很快自燃殆尽。恒星越大，燃烧得越快。假如我们的太阳是现在的10倍之大，它会在1000万年之后，而不是在100亿年之后消耗干净，我们现在就不会在这里。</p>

<p>我们还必须与太阳有适当的距离。离太阳太近，地球上的一切都会化为蒸气；离太阳太远，一切都会结成冰块。只要地球离太阳再远5%，或再近15%，地球上就不适于居住。</p>

<p>金星离太阳只比我们近4000万公里。太阳的热量射到那里只比我们早两分钟。金星的大小和结构很像地球，但是，轨道距离上的小小差别，产生了全然不同的结果。热这么几摄氏度就意味着金星无法留住表面的水，结果对气候造成了灾难性的后果。随着水分蒸发，氢原子逸入太空，氧原子与碳在大气里形成了厚厚的一层温室气体一氧化碳。金星变得令人窒息。它的表面温度高达470摄氏度，连铅都会熔化。金星表面的大气压是地球表面的90倍，任何人都受不了。目前我们生产不出隔热服装，也制造不了隔热的宇宙飞船，因此无法前往金星。我们对金星表面的了解，是基于遥远的雷达图像，以及一艘苏联无人探测器。那个探测器于1972年满怀希望地降落在云团里，运转不到1小时，就永远的关闭了。所以，你只要向太阳移动2光分，就会发生上诉情况。</p>

<p>要是离太阳再远一点，问题不是太热而是太冷，这一点，冰冷的火星可以作证。火星一度也是个比较合意的地方，但它没有留住有用的大气层，变成了一个天寒地冻的不毛之地。</p>

<p>2、</p>

<p>我叫刘拓，现在是北京大学考古文博学院的博士生。我很关注一些很少被记录的，而且可能会消失的、容易变化的古迹，想方设法去拍摄它们。国内的很多文物在我拍过之后消失了，所以这个记录让我比较有成就感。我总是选择那些急迫需要拍摄的地方。</p>

<p>我在2013年的时候才第一次出国。我还是像在国内一样，选择更急迫的地方。有一个例子就是阿富汗的贾姆宣礼塔。阿富汗有两个世界遗产，其中一个很有名，是巴米扬石窟。这个遗产还是挺好去的，从喀布尔每周有三四班飞机可以飞过去。而且巴米扬本身是一个安全的区域，所以如果愿意去的话还是很容易的。但是贾姆宣礼塔的位置非常的偏僻，它是在整个阿富汗的最中部。在它西边的赫拉特和东边的喀布尔是两个大城市，距离这个塔都有一天以上的车程，而且路上是比较危险的。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201808/bg2018082421.jpg" alt="" title="" /></p>

<p>我选择去这个塔是因为在2017年的时候，我突然发现喀布尔到塔所在的县城恰赫恰兰之间开行了一个航班，因此我可以设计一个只在那儿停留一天的线路来去这个塔。</p>

<p>这个飞机是我见过的最小的，它一排就3个座，能坐不到40个人。飞到那儿了以后景象还是挺吓人的，因为它是个省城，全城都是土坯的房子，就在这个山坡上，看上去就类似于中国的一个小村庄一样。</p>

<p>出了机场仅仅几分钟的时间，我就被当地军人抓住了，因为一个外国人突然出现在这么小的地方很不同寻常。我被带到局子里，问你是来干什么的？你为什么会出现在这儿？我就赶紧掏出一张图片，因为我问路都是用图片，我就说贾姆贾姆，贾姆宣礼塔。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201808/bg2018082422.jpg" alt="" title="" /></p>

<p>这个时候他们的长官出来了，他是会说英语的，他告诉我说这个塔路程太远了，而且路上挺危险的，我们肯定不会让你去。我当时都快哭出来了，我说我这趟行程都是围绕着这个塔安排的时间，如果不能去的话就白来了。然后他转头就说，我只是说不让你一个人去，但是我们可以带你去呀。所以他一招手招出来了十几个士兵，然后开了两辆皮卡，皮卡后面架了两挺冲锋枪，两辆车就往那个塔开过去。</p>

<p>100公里的路程开了6个小时，我感觉已经颠到失去知觉了，终于在拐过一个弯以后进入到河谷里，这个塔就在山谷之间挺立出来了，特别漂亮。士兵就跟我大叫"贾姆贾姆"，我们非常欢快地开到了塔下面。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201808/bg2018082423.jpg" alt="" title="" /></p>

<h2>本周图片</h2>

<p>1、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201808/bg2018082424.jpg" alt="" title="" /></p>

<p>苹果公司对 IT 行业的一大"贡献"，就是它发明了好多接口。上面都是苹果设备的转接线。</p>

<p>2、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201808/bg2018082425.jpg" alt="" title="" /></p>

<p>1976年，苹果公司成立时的第一个 Logo，是牛顿坐在苹果树下面。很快，乔布斯就用咬了一口的苹果，取代了这个 Logo。</p>

<p>3、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201808/bg2018082426.jpg" alt="" title="" /></p>

<p>美国的一个养鸡场主发明了鸡尿布，在网上销售，取得了很好的销量。鸡穿上这种尿布以后，所有排泄物都包在尿布里面，对环境毫无影响，因此就可以养在家里。</p>

<p>这一方面满足了把鸡当做宠物养的需求，另一方面也使得人们能够在 Instagram 上面发各种好玩的鸡照片/视频。</p>

<h2>新奇</h2>

<p>1、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201808/bg2018082427.jpg" alt="" title="" /></p>

<p>美国国家航空航天局 NASA 为了庆祝成立60周年，将德彪西的名曲《月光》配上月球勘测器拍摄的图像，制作了一段视频，描绘了太阳光在月球表面的流动，"通过光，地表和音乐的相互作用，提供了科学和艺术的迷人融合"。</p>

<h2>本周金句</h2>

<p>像奴隶一样工作，像国王一样命令，像神一样创造。（，1876年－1957年，现代主义雕塑先驱）</p>

<h2>欢迎订阅</h2>

<p>这个专栏每周五发布，同步更新在我的。</p>

<p>微信搜索"<strong>阮一峰的网络日志</strong>"或者扫描二维码，即可订阅。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2018/bg2018042311.jpg" alt="image | left" title="" /></p>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2018-08-24T11:27:05+08:00">2018年8月24日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>文集：</li>
<li>社交媒体：</li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------
<h1 id="#title_1" >2、图灵奖得主John Hopcroft，李开复博士，吴恩达做导师，300学生5周培训后成“AI工程师”</h1>
陈思
[http://www.infoq.com/cn/news/2018/08/five-week-ai?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/08/five-week-ai?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>图灵奖得主John Hopcroft，李开复博士，吴恩达做导师，300学生5周培训后成“AI工程师”。</p> <i>By 陈思</i>
---------------
<h1 id="#title_2" >3、文章： 区块链性能测评实战案例</h1>
杜行舟
[http://www.infoq.com/cn/articles/block-chain-practice?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/block-chain-practice?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/block-chain-practice/zh/smallimage/how-to-choose-stream-processor-logo-1535097141658.jpeg"/><p>近期区块链的技术概念在传统IT圈逐渐升温，成为许多遗产系统升级重构方案的备选技术路线。笔者本人多年从事应用系统研发，目前所维护的系统性能渐露瓶颈，分片扩容难度较大且面临分布式改进的潜在需求，因而亟需区块链架构技术储备。</p> <i>By 杜行舟</i>
---------------
<h1 id="#title_3" >4、是什么成就了中国最具创新力的公司，帮他们的超脑计划孵出阿尔法蛋？</h1>
Sharon
[http://www.infoq.com/cn/news/2018/08/Intel-alfa-egg?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/08/Intel-alfa-egg?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>是什么成就了中国最具创新力的公司，帮他们的超脑计划孵出阿尔法蛋？</p> <i>By Sharon</i>
---------------
<h1 id="#title_4" >5、Android Smart Linkify API背后的机器学习</h1>
Alex Giamas
[http://www.infoq.com/cn/news/2018/08/Machine-Le-Android-Smart-Linkify?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/08/Machine-Le-Android-Smart-Linkify?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>上周，谷歌发布了代号为Pie的Android 9。Android正在推出一系列由人工智能提供支持的新功能。Android Smart Linkify是最重要的新AI功能之一。</p> <i>By Alex Giamas</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_5" >6、Liftbridge为NATS提供了类Kafka的日志API</h1>
Richard Seroter
[http://www.infoq.com/cn/news/2018/08/nats-liftbridge?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/08/nats-liftbridge?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>事件驱动是当前的一个技术热点。开源项目Liftbridge以可扩展的类Kafka日志API扩展了NATS，加入到这一热点领域中。为了解该项目的更多细节，并了解不断变化中的系统连接技术环境，InfoQ采访了资深技术人员Tyler Treat。Treat是Liftbridge项目的创立者，也是NATS的长期贡献者。</p> <i>By Richard Seroter</i> <i> Translated by 盖磊</i>
---------------
<h1 id="#title_6" >7、甘特更新企业敏捷规划工具的魔力象限</h1>
Rui Miguel Ferreira
[http://www.infoq.com/cn/news/2018/08/magicq-enterprise-agile-planning?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/08/magicq-enterprise-agile-planning?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>2017年，甘特从研究“企业敏捷规划工具”转向了“应用程序开发生命周期管理”。分析师表示，通过利用以客户为中心和以业务成果为驱动并带有持续反馈的实践，企业敏捷规划（EAP）工具可以帮助企业大规模地实施敏捷实践，他们认为这代表了以项目为中心的敏捷工具和传统应用程序开发生命周期管理（ADLM）的一种演化。</p> <i>By Rui Miguel Ferreira</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_7" >8、微软必应从.NET Core 2.1获得了性能提升</h1>
Sergio De Simone
[http://www.infoq.com/cn/news/2018/08/bing-speedup-dotnet-core-2.1?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/08/bing-speedup-dotnet-core-2.1?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>据微软工程师Mukul Sabharwal介绍，在将微软搜索引擎必应迁移到.NET Core 2.1之后，内部服务延迟降低了34%，这主要归功于.NET社区贡献的改进。</p> <i>By Sergio De Simone</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_8" >9、微软驱动模块框架旨在简化Windows驱动开发</h1>
Sergio De Simone
[http://www.infoq.com/cn/news/2018/08/windows-driver-module-framework?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/08/windows-driver-module-framework?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>使用微软最近新开源的微软驱动模块框架（DMF），Windows驱动开发者现在有一种更简单的方式创建简单的结构化驱动以及在驱动之间共享代码了。</p> <i>By Sergio De Simone</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_9" >10、Johnny Five is alive, Ghost 2.0, and Stimulus</h1>

[https://javascriptweekly.com/issues/400](https://javascriptweekly.com/issues/400)
<table border=0 align="center" border="0">
  <tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   ">

  <div>    
    <table border=0 border=0><tr>
<td align="left" style="padding-left: 4px; font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   "><p>#400 — August 24, 2018</p></td>
<td align="right" style="padding-right: 4px; font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   "><p></p></td>
</tr></table>
    
    <table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0 12px;  "><p>JavaScript Weekly</p></td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
      <p>Due to unforeseen circumstances, this 400th issue of JavaScript Weekly comes to you from a tent in the middle of a freezing cold field in Yorkshire! Apologies if it's a few hours late, but we were  also waiting for Babel 7.0 to drop <em>(update: it's not, it's now )</em>.</p>

      <p>A huge thanks to you for being a subscriber, and an extra special thanks if you're one of the few hundred subscribers who has stayed with us since issue 1 almost 8 years ago :-)<br>
      <span style="color: #666666;"><em>— Peter Cooper, editor</em></span></p>
    </td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   ">
  
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"> page is packed with source code examples of what it can be used to achieve.</p>
  <p>Johnny Five Team </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — An epic tutorial covering the full GraphQL server experience using Apollo Server and Express including authentication, roles/permissions, subscriptions, error handling, pagination..</p>
  <p>Robin Wieruch </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"> to learn more.</p>
  <p>Sencha, Inc. <span style="text-transform: uppercase; padding: 1px 4px;  margin-left: 4px; font-size: 0.9em;   color: #997 !important;">sponsor</span></p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Very technical but exciting news if you’re planning to lean heavily on WebAssembly. V8 6.9 (and hence Chrome 69) and above will start WebAssembly code <em>much</em> faster.</p>
  <p>Clemens Hammacher </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Want a fully JavaScript powered blog? 2.0 takes big steps forward with a new editor, multi-language support, custom routes, custom site structures, and more.</p>
  <p>John O'Nolan </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"> Here, he shows just what went into the process of creating it.</p>
  <p>Dr. Axel Rauschmayer </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></p>
  <p>Basecamp </p>
</td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0;  "><p>💻 Jobs</p></td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Learn from the best and lead by example. Do your finest work, with purpose, freedom, and a great community.</p>
  <p>Reaktor </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Help build a world class user interface for the platform that collects data to drive business insights for our teams.</p>
  <p>Netflix </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Vettery specializes in dev roles and is completely free for job seekers. Create a profile to get started.</p>
  <p>Vettery </p>
</td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0;  "><p>📘 Tutorials and Stories</p></td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — I hope you like math! This is a neat walkthrough of calculating the dot product of two complex vectors with JS.</p>
  <p>Mateo Gianolio </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — It’s a short, high level piece, but it’s nice to see Vue getting more mainstream attention which is basically what the article is about too :-)</p>
  <p>Klint Finley (WIRED) </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — A handy cheat sheet used by JavaScript developers interested in writing functional style code. Check it out.</p>
  <p>Progress Kendo UI <span style="text-transform: uppercase; padding: 1px 4px;  margin-left: 4px; font-size: 0.9em;   color: #997 !important;">sponsor</span></p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — The <code>filter</code> array method creates a new array of elements that pass a test defined in a given function. This tutorial will help you feel confident with it.</p>
  <p>Adam Giese </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Want to dig into a little machine learning with JavaScript? This introduces some basic concepts.</p>
  <p>Aral Roca </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>The npm Blog </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Try 'The Frontier' free for 14-days. Short tutorials from the instructors and authors you trust.</p>
  <p>Big Nerd Ranch <span style="text-transform: uppercase; padding: 1px 4px;  margin-left: 4px; font-size: 0.9em;   color: #997 !important;">sponsor</span></p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Adrian Oprea </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Ayooluwa Isaiah (Pusher) </p>
</td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0;  "><p>🔧 Code and Tools</p></td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Checkly </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"> of the end result.</p>
  <p>Andrei Volchenko </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>ROLLBAR <span style="text-transform: uppercase; padding: 1px 4px;  margin-left: 4px; font-size: 0.9em;   color: #997 !important;">sponsor</span></p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — If you want to work with immutable state, this is worth looking at.</p>
  <p>Michel Weststrate </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></p>
  <p>iodide </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Don’t want to use <code>fetch</code> but still want to make simple jQuery-style Ajax requests? This is an option.</p>
  <p>Fernando Daciuk </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Don’t click if you aren’t ready to use a fair bit of bandwidth, but this example of emulating Windows 2000 in the browser (at high performance, too) is certainly compelling.</p>
  <p>Fabrice Bellard </p>
</td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px;  ">

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
<p>📅 Upcoming JavaScript Events</p>

    <ul>
    <li>
 — A two day event with talks, workshops and an advice lounge.</li>

    <li>
 — A one day single track event.</li>

    <li>
 — A new 2 day conference focused on all front end frameworks with keynotes from the teams of the most popular ones.</li>

    <li>
 — One of the largest JavaScript events. Organized by the Linux Foundation.</li>

    <li>
 — The European Community Ember Conference</li>

    </ul>

    </td></tr></table>
</td></tr></table>
<table border=0 border=0><tr><td style=" font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   "></td></tr></table>
</div>

  </td></tr>
</table>





<img src="https://javascriptweekly.com/open/400/rss" width="1" height="1" />
---------------