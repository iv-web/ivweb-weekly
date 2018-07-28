## 文章索引
1、 <a href="#1每周分享第-15-期" >每周分享第 15 期</a><br/>
2、 <a href="#2logging-activity-with-the-web-beacon-api" >Logging Activity With The Web Beacon API</a><br/>
3、 <a href="#3视频演讲-万台规模服务架构下kubernetes探索与实践" >视频演讲： 万台规模服务架构下Kubernetes探索与实践</a><br/>
4、 <a href="#4视频演讲-传统企业devops微服务落地从0到1" >视频演讲： 传统企业DevOps微服务落地从0到1</a><br/>
5、 <a href="#5业务流程长周期服务和微服务" >业务流程、长周期服务和微服务</a><br/>
6、 <a href="#6github推出python安全警告" >GitHub推出Python安全警告</a><br/>
7、 <a href="#7devops采用现状情况报告" >DevOps采用现状情况报告</a><br/>
8、 <a href="#8避免流量高峰期cdn问题的10个方法" >避免流量高峰期CDN问题的10个方法</a><br/>
9、 <a href="#9ionic-4-beta-the-web-beacon-api-and-some-golden-oldies" >Ionic 4 beta, the Web Beacon API, and some golden oldies</a><br/><h1 id="#title_0" >1、每周分享第 15 期</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2018/07/weekly-issue-15.html](http://www.ruanyifeng.com/blog/2018/07/weekly-issue-15.html)
<p>这里记录过去一周，我看到的值得分享的东西，每周五发布。</p>

        <p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018072701.jpg" alt="" title="" /></p>

<p>（题图：集盒商城，杭州，2018）</p>

<p>很多网友问，《每周分享》的来源是什么，你从哪里得知这些消息？</p>

<p>我的消息来源主要是下面几个。</p>

<blockquote>
  <ul>
<li></li>
<li></li>
<li>RSS 订阅</li>
<li>Twitter 和 Facebook</li>
</ul>
</blockquote>

<p>多年来，我每天都会浏览这些消息来源，了解资讯，看到有意思的东西，就会写入《每周分享》。我从学生时代就有做笔记的习惯，《每周分享》只是把个人笔记公开了而已。</p>

<p>这些消息来源大部分是英语，中文的内容比较少，因为中文信息来源很难找。国内的媒体往往只报道，谁融到了多少钱、谁上市了、哪位高管又跳槽了......技术本身的报道是非常少的。另一方面，国内的氛围是，独家技术都不太愿意曝光，更别说写得清晰易懂了。</p>

<p>我希望，国内也能有 Hacker News 那样的技术资讯网站。《每周分享》只是第一步，看看有多少人对这类东西感兴趣。如果有那么一批读者，经常来看，那么进一步就可以做社区，共同创造一些更有意义和价值的东西。</p>

<h2>新闻</h2>

<p>1、</p>

<p>我们知道，只有雌蚊子才叮人，雄蚊子是不叮人的。</p>

<p>利用这个特点，2017年11月，澳大利亚昆士兰州人工培养了数百万只雄蚊子。这些蚊子携带一种特殊的细菌，然后被释放到大自然。它们与雌蚊子交配，卵不会孵化，结果当地蚊子的数量减少了80%。</p>

<p>2、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018072702.jpg" alt="" title="" /></p>

<p>2018年6月4日，民政部发布了"2018年一季度结婚大数据"。全国结婚登记301.7万对，同比下降5.7%。过去五年，这个指标一直在下降，五年前的2013年一季度，全国还有428万对结婚。只过了五年，全国结婚人数将近3分之一。</p>

<p>由于同期的人口总数是增长的，就说明，国内年轻人结婚的意愿越来越淡薄，选择单身的人越来越多。另外，这五年的离婚人数一直在上升，虽然上升速度不快。</p>

<p>3、</p>

<p>2018年5月，GDPR（欧洲保护消费者隐私法案 ）生效。现在，第一份裁决已经出炉了。德国一家法院根据 GDPR，判决全球域名最高管理机构 ICANN 违法。</p>

<p>ICANN 现在的做法是，登记域名时，必须提供三个联系方式：域名所有人、技术负责人、域名管理员。法院认为，这些信息太多了，只要域名所有人的联系方式即可，技术负责人和域名管理员的联系方式是不必要的，ICANN 又提不出合理的解释，因此判决违法。该案现在进入上诉流程。</p>

<p>4、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018072703.jpg" alt="" title="" /></p>

<p>10 寸是目前最小的 Surface 型号。 它可以当做平板电脑使用，也可以配上键盘，当做笔记本使用。重量521.6克，续航9个小时，售价399美元。由于能够使用微软 Office，可能会比 iPad 更受欢迎。</p>

<p>这个产品的另一个意义在于，它是 Windows 10 以后，微软发布的屏幕最小的硬件。如果成功的话，估计会进一步缩小屏幕，直至重返手机市场。</p>

<p>5、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018072725.jpg" alt="" title="" /></p>

<p>加州大学的研究人员提出，可以通过键盘上的热残留窃取密码。用户使用键盘后的一分钟以内，就可以通过热像仪，找出用户使用的键，从而暴力破解密码。</p>

<p>6、</p>

<p>太空是不是接近真空？现在，科学家告诉我们，太空存在大量碳氢化合物分子，有很多很多脏兮兮的油脂。</p>

<p>悉尼新南威尔士大学的化学家蒂姆施密特教授表示，未来宇宙飞船穿越星际空间时会遇到星际尘埃，其中部分是油脂，部分是烟灰，部分是沙子般的硅酸盐。它们使得飞船的挡风玻璃上会厚厚地粘上一层。他还说，太阳系没有星际尘埃，因为太阳风把它们都吹散了。</p>

<p>7、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018072704.jpg" alt="" title="" /></p>

<p>微软向 Git 2.18 提交了一个新功能，会自动在Git 仓库生成一个有向图数据文件，这个文件保存每个提交之间的线性关系。这会大大加快大型库的合并操作的速度。另外，以后生成节点关系图，只要根据这个文件即可，不用遍历整个库 。</p>

<p>8、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018072705.jpg" alt="" title="" /></p>

<p>有一项研究，计算了自己做饭和去饭店吃的价格差异。结论是同样的食材，饭店比自己做贵5倍，如果吃连锁店的套餐会贵三倍。为了省钱和健康，还是自己多做做饭吧。</p>

<p>9、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018072706.jpg" alt="" title="" /></p>

<p>2017年，湖南省长沙市一位产妇在医生的建议下，做了华大基因的"无创DNA检查"，结果显示胎儿低风险，就把小孩生了下来。结果，这个新生儿有"13号染色体长臂缺失综合症"、"脑发育不良"、"虹膜缺损"等一系列缺陷和疾病。这意味着，小男孩很可能会智力障碍、生长迟缓、外表异常，几乎无法正常长大。</p>

<p>虽然这个案例是基因检测失败了，但是可以设想，如果这种检测是准确的（未来肯定可以做到），那么每个胚胎一定都会做这种检测。如果结果是高风险，胚胎就没有出生的机会；如果结果是某个基因缺失，可以修补后再出生。是过去20年 DNA 测序的价格变动。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018072707.jpg" alt="" title="" /></p>

<p>10、</p>

<p>媒体报道，为了实现双因素认证，谷歌公司内部已经全员使用物理密钥。也就是说，除了密码，登录还需要物理凭证。下一步，谷歌会这种物理密钥。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018072708.jpg" alt="" title="" /></p>

<p>以后，随着  标准的推广，普通网站也可以使用物理密钥登录。一旦当前设备（比如手机）登录过一次，以后就不需要输入密码，直接用物理密钥就可以登录。</p>

<p>11、<strong>一句话新闻</strong></p>

<p>(1) ，理由是安卓绑定谷歌服务，帮助谷歌垄断在互联网搜索领域的主导地位。真讽刺，中国出售的安卓手机会剥离谷歌服务，现在成了欧盟眼中的正确做法。</p>

<p>(2) 北美148个城市的，第一名是旧金山，3500美元一个月，第二名是曼哈顿的3000美元。大部分城市都超过1000美元。</p>

<p>(3) 的 API 调用，免费额度缩小30倍，价格提高14倍。这迫使大量网站转为使用 OpenStreetMap。</p>

<h2>互联网人才报告</h2>

<p>本期《每周分享》很高兴得到高端互联网人才招聘网站  的赞助。</p>

<p>2018年的日历已翻了一半，又到了年中盘点的时刻。在科技企业频传上市消息的第二季度，互联网人才的流向和薪资水平是否也有了新的变动？</p>

<p>近期，互联网技术招聘平台  发布了《2018年 Q2 互联网人才市场流动报告》，分析了技术开发者的最新薪资动态。</p>

<p>给大家分享报告的几个结论：</p>

<blockquote>
  <p>1、         Q1 全年跳槽高峰过后，Q2 面邀薪资继续上涨，小有惊喜；</p>

<p>2、         管理型、专家型技术人才市场行情坚挺，全栈和数据工程师涨薪最快；</p>

<p>3、         招聘需求集中于上市公司，创业公司吸引人才变难；</p>

<p>......</p>
</blockquote>

<p>如果你还想知道：哪些细分领域薪资最高？哪些公司是Q2互联网人眼中的当红炸子鸡？获得季度跳槽涨薪王称号的程序员是怎样的存在？</p>

<p><strong>扫描以下海报关注 100offer，回复关键词「薪资报告」，即可免费领取完整版报告。</strong></p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018072709.jpg" alt="" title="" /></p>

<h2>教程</h2>

<p>1、（英文）</p>

<p>一篇很好的初级 Python 教程，教你用最基本的语法，算出平均数和标准差。</p>

<p>2、（英文）</p>

<p>有人把 WordPress 编译成了 .Net 代码，运行的时候只需要 .Net 环境，不需要 PHP 了。随着转码器的流行，以后这种事情可能越来越多。你用什么语言可能根本无所谓了，反正都可以转来转去。</p>

<p>3、（英文）</p>

<p>为什么是 192.168.1.1 这个地址，而不是别的地址被指定为内网 IP？</p>

<p>4、（英文）</p>

<p>Kubernetes 是现在最流行的容器集群管理工具，本文给出了一份上手教程，教大家怎么安装和使用它。</p>

<p>5、（英文）</p>

<p>dd 命令通常用来克隆整块磁盘，或者制作 Linux 系统的 USB 启动盘。这篇文章教你怎么用，其实很简单。</p>

<p>6、（英文）</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018072710.jpg" alt="" title="" /></p>

<p>Webpack 是现在最流行的模块打包器，可以将脚本依赖打包成一个文件。这到底是怎么实现的？如果自己写一个打包器，应该怎么写？</p>

<p>7、（英文）</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018072711.jpg" alt="" title="" /></p>

<p>介绍 Chrome 开发者工具各个部分的用法。</p>

<p>8、（英文）</p>

<p>介绍 MacOS 内核的历史演变，跟 Linux 的差异还是很大的。</p>

<p>9、（英文）</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018072712.jpg" alt="" title="" /></p>

<p>WAF 是应用程序级别的防火墙，目前主要用在 Web 服务器软件。这篇文章简单介绍了 WAF 的概念。</p>

<h2>资源</h2>

<p>1、</p>

<p>开源电子书。如何写一个解释器，其实也就是如何自己设计并实现一门语言。</p>

<p>2、</p>

<p>这个书单推荐了10本学习 Java 语言的必读书，前三名是 Effective Java、Clean Code 和 Java Concurrency in Practice。</p>

<p>3、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018072713.jpg" alt="" title="" /></p>

<p>这个网站收集各种软件的 Cheat Sheet（常用操作表）。</p>

<p>4、</p>

<p>谷歌推出的机器学习各个领域的初学者指南，目前只有两个专题。</p>

<h2>工具</h2>

<p>1、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018072714.jpg" alt="" title="" /></p>

<p>Firefox 推出的管理密码的 App，最大特色是浏览器和手机同步。某个网站的密码，浏览器输入了，手机里也能看到，反之亦然，基本上就是有桌面同步功能的 1Password。目前只有 iOS 版本。</p>

<p>2、</p>

<p>该网站提供50个国家或地区的虚拟电话号码，可以用来接收当地短信或来电。</p>

<p>3、</p>

<p>这篇文章介绍了 Google Analytics 等8个网站统计工具。</p>

<p>4、</p>

<p>asmttpd 是一个用汇编语言写的 Web 服务器，非常小，二进制包只有 6KB，功能比较少，但性能很好。</p>

<p>5、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018072715.jpg" alt="" title="" /></p>

<p>开源的在线图像编辑器。</p>

<p>6、</p>

<p>又一个新的 JS 打包器问世了，企图替代 Webpack。</p>

<p>7、</p>

<p>一个浏览器的表单验证库，采用链式写法，特点是易读易写。</p>

<p>8、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018072716.jpg" alt="" title="" /></p>

<p>一个波兰程序员为了学中文，制作了一个工具：输入常用汉字，自动生成学习卡片。</p>

<p>9、</p>

<p>BGP 图像比 JPG 图像有更好的压缩比，但是它的解析需要加载一个前端 JS 库。</p>

<h2>文摘</h2>

<p>1、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018072717.jpg" alt="" title="" /></p>

<p>人类正在产生海量的信息，目前都储存在硬盘上。科学家正在尝试使用 DNA 储存这些信息。</p>

<p>所有蛋白质都是由4种核苷酸构成：腺嘌呤（A）、胸腺嘧啶（T）、鸟嘌呤（G）、胞嘧啶（C）。如果规定 A 表示00，C 表示01，T 表示11，G 表示10，那么只要组合这些核苷酸就能表示所有信息。</p>

<p>每个人类细胞含有30亿个碱基对，大概是几十 MB 的数据。人体包含几十万亿个细胞，也就是说，如果使用 DNA 储存数据，那么大概只要一个汽车的后备箱，就能放下人类的所有数据。</p>

<p>2、</p>

<p>如果人类可以像植物那样进行光合作用，直接从太阳接收能量。这肯定会让人类的生活变得更轻松：我们不用通过食物补充能量了，用在饮食上的时间可以用到其他方面。过度开发的农业用地将恢复自然生态系统。 饥饿，营养不良和食源性疾病的发病率将直线下降。</p>

<p>但是，人类无法进行光合作用，这到底是为什么呢？</p>

<p>原因是动物和植物走了不同的进化方向：植物通过保持静止，来保存它们缓慢但恒定的太阳能摄取，但动物要四处移动，依靠太阳补充能量太缓慢，所以需要能量密集的食物来提供能量。</p>

<p>未来，人类贴上光合作用的皮肤贴片，似乎也不是不可能。这里的关键是，我们需要一种技术，可以利用太阳能将二氧化碳转为人体可以吸收的糖，这样通过晒太阳，人类就能补充能量。另外，如果能将叶绿体变成人体皮肤，那么，也许我们可以让一个人永远在水下，因为除了糖，光合作用还产生氧气。</p>

<p>这里的麻烦在于，人体没有足够的表面积，来捕获大量阳光。植物有树叶，所以能够利用比自身体积大得多的表面积，吸收太阳能。人体的表面积与体积之比实在太小。</p>

<p>3、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018072718.jpg" alt="" title="" /></p>

<p>2018年6月5日，主持完台积电（TSMC）2017 年年度股东大会后，董事长 87 岁的张忠谋正式从他创办的公司退休。</p>

<p>台积电（TSMC）是"台湾积体电路制造股份有限公司" 的缩写。顾名思义，就是在台湾制造积体电路，也就是集成电路。集成电路是现代计算机业的起点，它能在更小的空间里聚集更复杂的电路。在 1958 年集成电路发明之前，由晶体管组装的计算机一台就几乎要堆满一整个房间。</p>

<p>今天台积电市值超过 2000 亿美元，是全球前 30 大上市公司。但它创办 31 年来只做一个生意----把其它公司设计的芯片造出来。台积电是全球第一个专门做这生意的公司，它启动了芯片制造的分工----有人专门设计、有人专门制造。</p>

<p>因为有台积电这样的公司专注于越来越复杂的芯片制造，专门的设计公司，比如英伟达、ATI、高通、博通甚至苹果才能专注于提升芯片设计。这种分工在 PC 时代带来 3D 图形处理革命，在智能手机时代更是直接促成因素之一。现在芯片业谈起自动驾驶，台积电依然是背后的支柱。</p>

<p>但集成电路的出现和台积电或者张忠谋都没什么关系。1958年 27 岁的张忠谋刚加入老牌半导体公司德州仪器。同年，比他早加入公司没多久的工程师杰克·基尔比（Jack Kilby）发明了第一块集成电路。</p>

<h2>新奇</h2>

<p>1、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018072719.jpg" alt="" title="" /></p>

<p>你是不是经常为会议超时烦恼？国外一家创业公司推出了一个小装置，可以通过颜色，提醒大家会议的进度。正常情况下是绿色，表示时间充分。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018072720.jpg" alt="" title="" /></p>

<p>一旦时间快到了，就会变成红色。等到预定结束时，就开始不停闪烁。</p>

<h2>本周图片</h2>

<p>1、（组图）</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018072721.jpg" alt="" title="" /></p>

<p>台湾网友为手机装了一颗废弃的单反镜头，高景深和长焦都有不错的表现。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018072722.jpg" alt="" title="" /></p>

<p>2、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018072723.jpg" alt="" title="" /></p>

<p>日本岛根县出云大社有一根世界最大草绳，全长13.6米、重5.2吨，用了2公顷水稻稻草制作的草绳捻成，制作耗时3个半月。最近，时隔6年，这根绳子又换了一根新的。</p>

<p>3、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018072724.jpg" alt="" title="" /></p>

<p>Reddit 上面有一个帖子询问大家，哪些建筑物看上去很像电影里面坏蛋的巢穴，里面有很多有趣的建筑物照片。</p>

<h2>本周金句</h2>

<p>1、</p>

<p>一个软件要多么自负，才会选择 .key 作为文件后缀名。这个软件就叫 Mac Keynote。（推特）</p>

<p>2、</p>

<p>计算机领域有点像是沉积的岩石，每个人在一座山里贡献了其中薄薄的一层，使山变得更加高耸。用户只是站在山顶，只有带着 X 光，你才能看到山里面是什么样子。（）</p>

<p>3、</p>

<p>這段大陸創業的日子，帶給了我太多美好的回憶，這所謂的『美好回憶』，不是指我有多成功，而是我選擇了自己想要的生活，有句話不是這樣說嗎？唯一真正的成功，是按自己的意思過上生活。（一个）</p>

<h2>欢迎订阅</h2>

<p>这个专栏每周五发布，同步更新在我的。</p>

<p>微信搜索"<strong>阮一峰的网络日志</strong>"或者扫描二维码，即可订阅。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2018/bg2018042311.jpg" alt="image | left" title="" /></p>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2018-07-27T11:42:03+08:00">2018年7月27日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>文集：</li>
<li>社交媒体：</li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------
<h1 id="#title_1" >2、Logging Activity With The Web Beacon API</h1>
Drew McLellan
[https://www.smashingmagazine.com/2018/07/logging-activity-web-beacon-api/](https://www.smashingmagazine.com/2018/07/logging-activity-web-beacon-api/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/07/logging-activity-web-beacon-api/" />
              <title>Logging Activity With The Web Beacon API</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>Logging Activity With The Web Beacon API</h1>
                  
                    
                    <address>Drew McLellan</address>
                  
                  <time datetime="2018-07-27T13:40:14&#43;02:00" class="op-published">2018-07-27T13:40:14+02:00</time>
                  <time datetime="2018-07-27T14:14:35&#43;00:00" class="op-modified">2018-07-27T14:14:35+00:00</time>
                </header>
                

<p>The Beacon API is a JavaScript-based Web API for sending small amounts of data from the browser to the web server without waiting for a response. In this article, we’ll look at what that can be useful for, what makes it different from familiar techniques like <code>XMLHTTPRequest</code> (‘Ajax’), and how you can get started using it.</p>

<p>If you know why you want to use Beacon already, feel free to jump directly to the  section.</p>

<h3 id="what-is-the-beacon-api-for">What Is The Beacon API For?</h3>

<p>The Beacon API is used for sending small amounts of data to a server <em>without waiting for a response</em>. That last part is critical and is the key to why Beacon is so useful &mdash; our code never even gets to see a response, even if the server sends one. Beacons are specifically for sending data and then forgetting about it. We don’t expect a response and we don’t get a response.</p>

<p>Think of it like a postcard sent home when on vacation. You put a small amount of data on it (a bit of “Wish you were here” and “The weather’s been lovely”), put it in the mailbox, and you don’t expect a response. No one sends a return postcard saying “Yes, I do wish I was there actually, thank you very much!”</p>

<p>For modern websites and applications, there’s a number of use cases that fall very neatly into this pattern of send-and-forget.</p>



  <aside class="product-panel product-panel__tilted product-panel--book" data-audience="non-subscriber">
    <div class="container product-panel--book__container">
      <div class="panel__description panel__description--book">
    <p>Getting the process <em>just</em> right ain't an easy task. That's why we've set up <strong>'this-is-how-I-work'-sessions</strong> — with smart cookies sharing what works really well for them. A part of the , of course.</p>
      <a href="http://smashed.by/casestudypanelmembership" class="btn btn--green btn--large">
        Explore features&nbsp;→
      </a>
      </div>
      <div class="panel__image panel__image--book">
        <a href="http://smashed.by/casestudypanelmembership" class="books__book__image">
        <div class="books__book__img">
          <img src="https://www.smashingmagazine.com/images/smashing-cat/cat-scubadiving-panel.svg" alt="Smashing TV, with live sessions for professional designers and developers." width="310" height="400">
        </div>
      </a>
      </div>
    </div>
  </aside>




<h4 id="tracking-stats-and-analytics-data">Tracking Stats And Analytics Data</h4>

<p>The first use case that comes to mind for most people is analytics. Big solutions like Google Analytics might give a good overview of things like page visits, but what if we wanted something more customized? We could write some JavaScript to track what’s happening in a page (maybe how a user interacts with a component, how far they’ve scrolled to, or which articles have been displayed before they follow a CTA) but we then need to send that data to the server when the user leaves the page. Beacon is perfect for this, as we’re just logging the data and don’t need a response.</p>

<p>There’s no reason we couldn’t also cover the sort of mundane tasks often handled by Google Analytics, reporting on the user themselves and the capability of their device and browser. If the user has a logged in session, you could even tie those stats back to a known individual. Whatever data you gather, you can send it back to the server with Beacon.</p>

<h4 id="debugging-and-logging">Debugging And Logging</h4>

<p>Another useful application for this behavior is logging information from your JavaScript code. Imagine you have a complex interactive component on your page that works perfectly for all your tests, but occasionally fails in production. You know it’s failing, but you can’t see the error in order to begin debugging it. If you can detect a failure in the code itself, you could then gather up diagnostics and use Beacon to send it all back for logging.</p>

<p>In fact, any logging task can usefully be performed using Beacon, be that creating save-points in a game, collecting information on feature use, or recording results from a multivariate test. If it’s something that happens in the browser that you want the server to know about, then Beacon is likely a contender.</p>

<h3 id="can-t-we-already-do-this">Can’t We Already Do This?</h3>

<p>I know what you’re thinking. None of this is new, is it? We’ve been able to communicate from the browser to the server using <code>XMLHTTPRequest</code> for more than a decade. More recently we also have the Fetch API which does much the same thing with a more modern promise-based interface. Given that, why do we need the Beacon API at all?</p>

<p>The key here is that because we don’t get a response, the browser can queue up the request and send it <em>without blocking execution</em> of any other code. As far as the browser is concerned, it doesn’t matter if our code is still running or not, or where the script execution has got to, as there’s nothing to return it can just background the sending of the HTTP request until it’s convenient to send it.</p>

<p>That might mean waiting until CPU load is lower, or until the network is free, or even just sending it right away if it can. The important thing is that the browser queues the beacon and returns control immediately. It does not hold things up while the beacon sends.</p>

<p>To understand why this is a big deal, we need to look at how and when these sorts of requests are issued from our code. Take our example of an analytics logging script. Our code may be timing how long the users spend on a page, so it becomes critical that the data is sent back to the server at the last possible moment. When the user goes to leave a page, we want to stop timing and send the data back home.</p>

<p>Typically, you’d use either the <code>unload</code> or <code>beforeunload</code> event to execute the logging. These are fired when the user does something like following a link on the page to navigate away. The trouble here is that code running on one of the <code>unload</code> events can block execution and delay the unloading of the page. If unloading of the page is delayed, then the loading next page is also delayed, and so the experience feels really sluggish.</p>

<p>Keep in mind how slow HTTP requests can be. If you’re thinking about performance, typically one of the main factors you try to cut down on is extra HTTP requests because going out to the network and getting a response can be super slow. The very last thing you want to do is put that slowness between the activation of a link and the start of the request for the next page.</p>

<p>Beacon gets around this by queuing the request without blocking, returning control immediately back to your script. The browser then takes care of sending that request in the background without blocking. This makes everything much faster, which makes users happier and lets us all keep our jobs.</p>

<div class="sponsors__wide-place"></div>




<h3 id="getting-started">Getting Started</h3>

<p>So we understand what Beacon is, and why we might use it, so let’s get started with some code. The basics couldn’t be simpler:</p>

<pre><code class="language-javascript">let result = navigator.sendBeacon(url, data);
</code></pre>

<p>The result is boolean, <code>true</code> if the browser accepted and queued the request, and <code>false</code> if there was a problem in doing so.</p>

<h4 id="using-navigator-sendbeacon">Using <code>navigator.sendBeacon()</code></h4>

<p><code>navigator.sendBeacon</code> takes two parameters. The first is the URL to make the request to. The request is performed as an HTTP POST, sending any data provided in the second parameter.</p>

<p>The data parameter can be in one of several formats, all if which are taken directly from the Fetch API. This can be a <code>Blob</code>, a <code>BufferSource</code>, <code>FormData</code> or <code>URLSearchParams</code> &mdash; basically any of the body types used when making a request with Fetch.</p>

<p>I like using <code>FormData</code> for basic key-value data as it’s uncomplicated and easy to read back.</p>

<pre><code class="language-javascript">// URL to send the data to
let url = '/api/my-endpoint';
    
// Create a new FormData and add a key/value pair
let data = new FormData();
data.append('hello', 'world');
    
let result = navigator.sendBeacon(url, data);
    
if (result) { 
  console.log('Successfully queued!');
} else {
  console.log('Failure.');
}
</code></pre>

<h4 id="browser-support">Browser Support</h4>

<p>Support in browsers for Beacon is very good, with the only notable exceptions being Internet Explorer (works in Edge) and Opera Mini. For most uses, that should be fine, but it’s worth testing for support before trying to use <code>navigator.sendBeacon</code>.</p>

<p>That’s easy to do:</p>

<pre><code class="language-javascript">if (navigator.sendBeacon) {
  // Beacon code
} else {
  // No Beacon. Maybe fall back to XHR?
}
</code></pre>
        

<p>If Beacon isn’t available and your request is important, you could fall back to a blocking method such as XHR. Depending on your audience and purpose, you might equally choose to not bother.</p>

<h3 id="an-example-logging-time-on-a-page">An Example: Logging Time On A Page</h3>

<p>To see this in practice, let’s create a basic system to time how long a user stays on a page. When the page loads we’ll note the time, and when the user leaves the page we’ll send the start time and current time to the server.</p>

<p>As we only care about time spent (not the actual time of day) we can use <code>performance.now()</code> to get a basic timestamp as the page loads:</p>

<pre><code class="language-javascript">let startTime = performance.now();
</code></pre>

<p>If we wrap up our logging into a function, we can call it when the page unloads.</p>

<pre><code class="language-javascript">let logVisit = function() {
  // Test that we have support
  if (!navigator.sendBeacon) return true;
      
  // URL to send the data to, e.g.
  let url = '/api/log-visit';
      
  // Data to send
  let data = new FormData();
  data.append('start', startTime);
  data.append('end', performance.now());
  data.append('url', document.URL);
      
  // Let's go!
  navigator.sendBeacon(url, data);
};
</code></pre>

<p>Finally, we need to call this function when the user leaves the page. My first instinct was to use the <code>unload</code> event, but Safari on a Mac seems to block the request with a security warning, so <code>beforeunload</code> works just fine for us here.</p>

<pre><code class="language-javascript">window.addEventListener('beforeunload', logVisit);
</code></pre>

<p>When the page unloads (or, just before it does) our <code>logVisit()</code> function will be called and provided the browser supports the Beacon API our beacon will be sent.</p>

<p>(Note that if there is no Beacon support, we return <code>true</code> and pretend it all worked great. Returning <code>false</code> would cancel the event and stop the page unloading. That would be unfortunate.)</p>

<div class="sponsors__wide-place"></div>




<h3 id="considerations-when-tracking">Considerations When Tracking</h3>

<p>As so many of the potential uses for Beacon revolve around tracking of activity, I think it would be remiss not to mention the social and legal responsibilities we have as developers when logging and tracking activity that could be tied back to users.</p>

<h4 id="gdpr">GDPR</h4>

<p>We may think of the recent European GDPR laws as they related to email, but of course, the legislation relates to storing any type of personal data. If you know who your users are and can identify their sessions, then you should check what activity you are logging and how it relates to your stated policies.</p>

<p>Often we don’t need to track as much data as our instincts as developers tell us we should. It can be better to deliberately <em>not</em> store information that would identify a user, and then you reduce your likelihood of getting things wrong.</p>

<h4 id="dnt-do-not-track">DNT: Do Not Track</h4>

<p>In addition to legal requirements, most browsers have a setting to enable the user to express a desire not to be tracked. Do Not Track sends an HTTP header with the request that looks like this:</p>

<pre><code class="language-bash">DNT: 1</code></pre>

<p>If you’re logging data that can track a specific user and the user sends a positive <code>DNT</code> header, then it would be best to follow the user’s wishes and anonymize that data or not track it at all.</p>

<p>In PHP, for example, you can very easily test for this header like so:</p>

<pre><code class="language-php">if (!empty($_SERVER['HTTP_DNT'])) { 
  // User does not wish to be tracked ... 
}
</code></pre>

<h3 id="in-conclusion">In Conclusion</h3>

<p>The Beacon API is a really useful way to send data from a page back to the server, particularly in a logging context. Browser support is very broad, and it enables you to seamlessly log data without negatively impacting the user’s browsing experience and the performance of your site. The non-blocking nature of the requests means that the performance is much faster than alternatives such as XHR and Fetch.</p>

<p>If you’d like to read more about the Beacon API, the following sites are worth a look.</p>

<ul>
<li>“,” W3C Candidate Recommendation</li>
<li>“,” MDN web docs, Mozilla</li>
<li>“,” caniuse.com</li>
</ul>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(ra, il)</span>
</div>


              </article>
            </body>
          </html>
---------------
<h1 id="#title_2" >3、视频演讲： 万台规模服务架构下Kubernetes探索与实践</h1>
徐运元
[http://www.infoq.com/cn/presentations/kubernetes-under-thousands-scale-service-structure?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/kubernetes-under-thousands-scale-service-structure?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/presentations/kubernetes-under-thousands-scale-service-structure/zh/mediumimage/xuyunyuan270-1532435269731.jpg"/><p>近年来，容器的使用越来越深入，越来越多的服务采用容器的方式进行部署。容器作为一种轻量级虚拟化技术几乎革新了整个IT领域软件开发部署流程。但随着服务数量的增加，如何高效自动管理容器和相关的计算、存储等资源，将容器技术真正落地上线？如何管理服务之间的依赖关系？如何对多个服务之间的更新与部署进行管理？如何在新的环境中实现多个服务的快速部署？带着这些问题，让我们一起来探索的Kubernetes应用编排管理是如何在在万台规模服务架构下来实践的。</p> <i>By 徐运元</i>
---------------
<h1 id="#title_3" >4、视频演讲： 传统企业DevOps微服务落地从0到1</h1>
赵安全
[http://www.infoq.com/cn/presentations/devops-micro-service-land-of-traditional-enterprise?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/devops-micro-service-land-of-traditional-enterprise?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/presentations/devops-micro-service-land-of-traditional-enterprise/zh/mediumimage/zhaoanquan270-1531535723072.jpg"/><p>DevOps和微服务，是目前开发运维领域最火的方向之一。作为传统企业，习惯了传统三层架构、瀑布开发模型、按照CMMI要求按部就班的做开发，如何迈出走向DevOps开发模式和微服务架构落地的第一步，一直是一个难题。本次分享基于一个传统企业项目案例，描述传统企业中的一个试点团队，如何按照DevOps和微服务的要求，调整组织架构、开发方式、开发运维管理和流程，从最初的迷茫和混乱，最终摸索形成了一套自己的DevOps体系和微服务设计开发方式，并取得初步成效的过程。涉及：DevOps和微服务结合场景下的组织架构设计、DevOps流程体系设计和工具落地、微服务设计思路和领域建模、微服务架构选型、分布式事务处理、服务治理等。
</p> <i>By 赵安全</i>
---------------
<h1 id="#title_4" >5、业务流程、长周期服务和微服务</h1>
Jan Stenberg
[http://www.infoq.com/cn/news/2018/07/events-commands-services?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/events-commands-services?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>在近期举行的DDD eXchange 2018会议上，Martin Schimak认为在最近几年间，领域事件引发了越来越多的讨论，但是我们对命令也应如此，在这次会议上他讨论了微服务领域的事件、命令以及长周期的服务，以及流程管理器和类似的工具如何有助于运行核心的业务逻辑。</p> <i>By Jan Stenberg</i> <i> Translated by 张卫滨 </i>
---------------
<h1 id="#title_5" >6、GitHub推出Python安全警告</h1>
Diogo Carleto
[http://www.infoq.com/cn/news/2018/07/githhub-security-alerts-python?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/githhub-security-alerts-python?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>GitHub宣布了Python安全警告，使Python用户可以访问依赖图，并在他们的库所依赖的包存在安全漏洞时收到警告。</p> <i>By Diogo Carleto</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_6" >7、DevOps采用现状情况报告</h1>
Volodymyr Fedak
[http://www.infoq.com/cn/news/2018/07/devops-adoption-state?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/devops-adoption-state?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>本文报告中的统计数据清楚地表明，引入DevOps的公司能够看到他们的软件交付操作有了明显的改进，并且能够实现他们的既定业务目标。然而，传统的文化很难打破，除非能够实现真正的合作和知识分享，这也是DevOps目前面临的一大挑战。</p> <i>By Volodymyr Fedak</i> <i> Translated by 奚甜甜</i>
---------------
<h1 id="#title_7" >8、避免流量高峰期CDN问题的10个方法</h1>
Hadar Weiss
[http://www.infoq.com/cn/news/2018/07/10way-avoid-CDN-atpeak?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/10way-avoid-CDN-atpeak?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>避免流量高峰期CDN问题的10个方法</p> <i>By Hadar Weiss</i> <i> Translated by 姚佳灵</i>
---------------
<h1 id="#title_8" >9、Ionic 4 beta, the Web Beacon API, and some golden oldies</h1>

[https://javascriptweekly.com/issues/396](https://javascriptweekly.com/issues/396)
<table border=0 align="center" border="0">
  <tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   ">

  <div>    
    <table border=0 border=0><tr>
<td align="left" style="padding-left: 4px; font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   "><p>#396 — July 27, 2018</p></td>
<td align="right" style="padding-right: 4px; font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   "><p></p></td>
</tr></table>
    
    <table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0 12px;  "><p>JavaScript Weekly</p></td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
      <p>If you've not ventured to the end of an issue of JavaScript Weekly recently, you'll be missing some of the bonus links or 'golden oldies' we've been running — this issue has a set of 4 older posts we've been seeing getting some fresh love on social media recently, so check those out.</p>
      <p>Also, if you want to submit articles or libraries for us to consider  or just hit reply :-) Thanks!<br>
      <span style="color: #666666;"><em>— Peter Cooper, editor</em></span></p>
    </td></tr></table>
<div style="   margin-top: 14px; margin-bottom: 8px;  "></div>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"> by all major browsers) that provides an efficient way for data to be asynchronously sent from a page back to a server for logging purposes.</p>
  <p>Drew McLellan </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — The beta release of Ionic 4, a framework for building native apps and PWAs with Web technology, has <em>just</em> landed. 4.0 marks the first version to completely embrace modern Web APIs such as Custom Elements, CSS Variables and Shadow DOM, plus it’s framework-agnostic at its core.</p>
  <p>Ionic </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Your browser developer tools are now available for site sessions other than your own. Easily understand performance issues thanks to page speed metrics, network analysis, downloadable HAR files, and comprehensive stack traces on all your visitors’ sessions.</p>
  <p>Fullstory <span style="text-transform: uppercase; padding: 1px 4px;  margin-left: 4px; font-size: 0.9em;   color: #997 !important;">sponsor</span></p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — JavaScript examples of many common algorithms (e.g. bit manipulation, Pascal’s triangle, Hamming distance) and data structures (e.g. linked lists, tries, graphs) with explanations. <em>(We linked this a couple of months ago but it has been substantially improved since then.)</em></p>
  <p>Oleksii Trekhleb </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Run your Node code with <code>ndb</code> and get extra, powerful Node debugging features right in Chrome’s DevTools including editing files and setting breakpoints before modules are loaded.</p>
  <p>Google Chrome Labs </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Redux, MobX and Vuex can make managing cross-component state trivial, but what would it take to write one for yourself?</p>
  <p>Andy Bell </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — And they’ve replaced it with.. no specific framework, but judicious use of <code>querySelectorAll</code>, custom elements, polyfills, etc.</p>
  <p>Mislav Marohnić on Twitter </p>
</td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   ">
  
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"> Significantly lighter than the TUI Grid we linked last week.</p>
  <p>Piotr Kowalski </p>
</td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0;  "><p>💻 Jobs</p></td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Work with smart devs and designers to solve meaningful problems for great clients. React, Vue, Gatsby, WordPress, Craft, and more.</p>
  <p>Upstatement </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Vettery specializes in developer roles and is completely free for job seekers.</p>
  <p>Vettery </p>
</td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0;  "><p>📘 Tutorials and Opinions</p></td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></p>
  <p>Dave Ceddia </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — A neat tutorial showing how to create a striking HTML-to-particle effect.</p>
  <p>Zach Saucier </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — A really detailed look at running Express (the Node.js webapp library) in a serverless context.</p>
  <p>Adnan Rahić </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — DigitalOcean offers tutorials, projects and answers to your questions about Ubuntu 18:04.</p>
  <p>DigitalOcean <span style="text-transform: uppercase; padding: 1px 4px;  margin-left: 4px; font-size: 0.9em;   color: #997 !important;">sponsor</span></p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — A quick tutorial on getting started with Vue that includes the use of a component from the Kendo UI library of Vue UI components.</p>
  <p>John Willoughby </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Samuel Oloruntoba </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Ryan Baker </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Thorsten Lorenz </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>NativeScript <span style="text-transform: uppercase; padding: 1px 4px;  margin-left: 4px; font-size: 0.9em;   color: #997 !important;">sponsor</span></p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Flavio Copes </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — One for beginners/learners.</p>
  <p>Craig Buckler </p>
</td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0;  "><p>🔧 Code and Tools</p></td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   ">
  
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></p>
  <p>Epicmax </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Matthew Phillips </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — A tool for finding those duplicated code smells in your codebase. Supports ES6, JSX and Flow.</p>
  <p>Daniel St. Jules </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Make data-driven decisions on whether you should be building features, or fixing bugs to stabilize your app.</p>
  <p>Bugsnag <span style="text-transform: uppercase; padding: 1px 4px;  margin-left: 4px; font-size: 0.9em;   color: #997 !important;">sponsor</span></p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"> It’s incredibly fast.</p>
  <p>Cosmo Wolfe </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — A minor release that’s a drop-in replacement for Angular 6.0. TypeScript 2.8 and 2.9 support has been added.</p>
  <p>Stephen Fluin (Google) </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Conforms to the ECMA-376 OOXML specification 2nd edition and the examples in the documentation are quite thorough.</p>
  <p>Nathan (Nater) Jorde </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Based on the Gamepad API.</p>
  <p>Colin van Eenige </p>
</td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px;  ">
<table border=0 border=0><tr><td style=" font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   "></td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  "><div style="line-height: 1.3em; font-size: 1.4em; color: #555555;">☀️ Some Summery JavaScript Golden Oldies</div></td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — A true golden oldie if you want to nail down your knowledge of scope and closures.</p>
  <p>Zell Liew </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — A fantastic round-up of concepts, tools, and things to consider.</p>
  <p>Sarah Drasner </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — <em>“Doing is learning. Doing it badly? It’s still learning. Learning modern JavaScript these days can feel like a futile exercise in WTF.”</em></p>
  <p>Gina Trapani </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;  padding: 0px 15px;  ">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Click “Compile” on the right then skim along the bottom.</p>
  <p>Boopathi Rajaa </p>
</td></tr></table>
</td></tr></table>
<table border=0 border=0><tr><td style=" font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   "></td></tr></table>
</div>

  </td></tr>
</table>





<img src="https://javascriptweekly.com/open/396/rss" width="1" height="1" />
---------------