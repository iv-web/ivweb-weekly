## 文章索引
1、 <a href="#1每周分享第-1-期" >每周分享第 1 期</a><br/>
2、 <a href="#2文章-直播终端技术比较native-vs-h5-vs-webrtc-vs-小程序" >文章： 直播终端技术比较：Native vs H5 vs WebRTC vs 小程序</a><br/>
3、 <a href="#3文章-专访rafael-schloming用于微服务开发人员的工作流程和部署模式" >文章： 专访Rafael Schloming：用于微服务开发人员的工作流程和部署模式</a><br/>
4、 <a href="#4文章-功夫贷首席科学家黄利舟90-亿放款1000-万用户背后的fintech-数据服务实践" >文章： 功夫贷首席科学家黄利舟：90 亿放款、1000 万用户背后的Fintech 数据服务实践</a><br/>
5、 <a href="#5视频演讲-开源分布式监控-cat-系统的高可用实践" >视频演讲： 开源分布式监控 CAT 系统的高可用实践</a><br/>
6、 <a href="#6文章-区块链毁誉参半如何客观理性全面的看待区块链的本质现状剖析和未来预测" >文章： 区块链毁誉参半，如何客观、理性、全面的看待区块链的本质，现状剖析和未来预测</a><br/><h1 id="#title_0" >1、每周分享第 1 期</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2018/04/weekly-issue-1.html](http://www.ruanyifeng.com/blog/2018/04/weekly-issue-1.html)
<p>这里记录过去一周，我看到的值得分享的东西。</p>

        <h2>语雀</h2>

<p>语雀（）是阿里巴巴集团内部最大的文档平台，也是阿里系知识管理和团队协作的主要工具之一。</p>

<p>今天（4月23日）是世界读书日，选在今天放开注册，不再需要邀请码，用户可以直接注册，跟阿里的正式员工一样使用所有功能。</p>

<p></p>

<p>为了配合世界读书日，语雀还邀请了一些互联网知名人士，写下他们的推荐书单，比如蚂蚁金服 CTO 的。</p>

<h2>新闻</h2>

<p>1、 限制第三方调用 API</p>

<p>4月4日，Instagram 无预警地宣布，立即废止一大批 ，像用户的 follower、like 等数据都无法再拿到了。同时宣布，每个用户的每小时 API 请求数量限制，从 5000 降低为 200。另外，还计划从2018年12月11日起，不再允许第三方 App 获取它的公开内容。</p>

<p>稍早，Twitter 也宣布，2018年6月19日之后，将不再提供 streaming services，这意味着第三方客户端 Tweetbot、Tweetings、Twitterrific 将无法自动刷新时间轴，必须用户自己手动刷新，才能看到新内容。有人做了一个网站  呼吁 Twitter 改变这个决定。</p>

<p>这些大型社交媒体想要表达的意思已经很清楚了：我们不欢迎第三方客户端。</p>

<p>2、</p>

<p>3月21日，北京市发布《关于优化人才服务促进科技创新推动高精尖产业发展的若干措施》，其中有这样一条内容：</p>

<blockquote>
  <p>在本市行政区域内的高新技术企业、创新型总部企业、新型研发机构等科技创新主体中承担重要工作，近3年每年应税收入超过上一年度全市职工平均工资一定倍数的（企业注册在城六区和北京经济技术开发区的为8倍，注册在本市其他区域的为6倍）。</p>
</blockquote>

<p>根据北京市统计局、市人力社保局发布数据，2016年度北京市职工年平均工资为92477元，月平均工资为7706元。而近日某招聘网站新鲜出炉的《2018旺季人才趋势报告》中显示，北京市平均月薪达到10712元。由此估算出月薪至少要 7 万可申请办理人才引进。</p>

<p>3、</p>

<p>Travis-CI 公布了3月13日生产数据库出错的调查报告。一个开发者执行了生产环境的检查以后，在同一个 Session 里面运行测试。由于数据库地址是环境变量给出的，这时 Session 里面的数据库地址的环境变量指向生产环境，导致测试脚本清空了生产环境的数据库。</p>

<p>4、</p>

<p>根据统计，距离硅谷最近的大城市圣何塞，去年100万美元左右的普通房屋，每个工作日价格上涨798美元，一年上涨了20万美元，是全美房价上涨之冠。亚军是旧金山，每个工作日上涨481美元；季军是西雅图（微软总部所在地），上涨434美元。</p>

<h2>教程</h2>

<p>1、[免费电子书] ，by 吴恩达</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2018/bg2018042302.png" alt="" title="" /></p>

<p>吴恩达（Andrew Ng）是斯坦福大学的教授，人工智能领域的权威，曾经担任过百度的首席科学家。</p>

<p>他的新书《Machine Learning Yearning》现在可以。今后几个月里面，他每完成一个部分，你就会得到邮件通知，可以立即读到。根据说明，这本书大概100页左右，每章的长度很短，非常容易阅读。内容主要关于如何实现你自己的机器学习项目，重点不是算法，而是如何运用算法到真实项目。</p>

<p>2、[免费视频教程] ，by 加州大学伯克利分校</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2018/bg2018042303.png" alt="" title="" /></p>

<p>加州大学伯克利分校的视频课程（数据科学基础），现在上网了。报名学习是免费的，如果需要证书才收费。</p>

<p>课程分成三个部分，每个部分需要5个星期学习，都由加大的老师亲自教授。整个课程针对初学者，不需要任何统计学或编程的基础。</p>

<ul>
<li>第一部分：</li>
<li>第二部分：</li>
<li>第三部分：</li>
</ul>

<p>3、[文章] , by Gerald Bauer</p>

<p>介绍如何使用 Ruby 语言从零开始写一个区块链实现，代码非常好懂，并有各种基础概念的解释。</p>

<p>4、[文章] , by Peter Krumins</p>

<p>位运算（bit operation）的用途，有很多例子。</p>

<p>5、[文章] </p>

<p>React 官方关于 React 原始设计思想的解释。</p>

<p>6、[图片] </p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2018/bg2018042304.png" alt="" title="" /></p>

<p>7、[电子书] </p>

<p>一份爱好者整理的 Google 面试准备指南。</p>

<p>8、[文章] </p>

<p>9、[文章] </p>

<p>人眼如何感受到色彩，读懂这篇文章需要一点物理学知识。</p>

<h2>文摘</h2>

<p>1、，by 康亮</p>

<blockquote>
  <p>2011年在百度浏览器团队时遇到几件让人影响深刻的事情。 有一次开会，产品拿出 Google 某个产品的 DEMO，里面有一段很酷炫 3D 效果，要求开发加上，只给2天时间，大家目瞪口呆。后续的开发为了赶节奏，导致非常多的 bug，又为了修改 bug，leader 将所有的 bug 按照人员平均分配，导致不同模块间的同学相互修改......实在难以想象。好比让做花卷的厨子，去修改西湖醋鱼的味道。</p>

<p>最初的现象是：bug 下降得慢，延伸 bug 反而增加，每个人都累的半死，代码风格极其杂乱，为了赶工导致的临时方案层出不穷。</p>

<p>到了中期：人员离职越来也多，代码难以维护，新加的需求与之前的临时方案冲突。</p>

<p>到了后期：想做一些修复，想调整架构，又要保证正常运行，其难度好比在一架飞行的飞机上拆换零件。</p>

<p>然后我也急忙离职了。。。。实在看不到成功的可能性。</p>
</blockquote>

<p>2、，by SQLite</p>

<blockquote>
  <p>SQLite 不使用 。Fossil 和 Git 都是区块链式的版本控制系统，都是分布式，都将内容存储为由加密哈希标识的一系列不可变的提交。Git 非常流行，许多开发人员不熟悉其他任何版本管理工具。然而，SQLite 更喜欢Fossil，本文解释为什么。</p>
</blockquote>

<p>3、</p>

<blockquote>
  <p>美国人均预期寿命连续两年下降。如果不告诉你国家名字，只是让你猜测的话，你一定会认为，这发生在某个战乱中的国家。不幸的是，这种事情恰恰就发生在美国。</p>

<p>2016年，零资产或者负资产家庭已经达到30.4%。也就是说，只要你有一块钱存款而么有负债，即使你是个流浪汉，你也比30%的美国家庭富有。</p>

<p>美国人到底有多穷？69%的美国人，存款少于1000美元。好多人说美国人很富有，确实，如果你找到了一个好职业，你的收入会很高很高。但是实际上，绝大多数美国人很穷，只能靠救济和福利过活。一半的美国人，他们的年平均收入低于25000美元。美国平均收入40000多，中位数收入只有25000美元。中位数是什么意思？50%收入高于这个数字，50%收入低于这个数字。</p>
</blockquote>

<p>4、</p>

<blockquote>
  <p>从现在起，我们可以靠美国芯片活得很好的幻想应该破灭了。中国有组织科技攻关的能力，也有推动国产芯片逐渐替代外来芯片所需要的动员力，最重要的就是决心。</p>

<p>特朗普政府在帮助我们下这个决心。如果中国真的转换了思路，也许过多少年之后，我们会感谢美国今天做出的限制决定，庆幸它促使中国早一点恢复了清醒。</p>

<p>一旦中国加速研发使用国产芯片的工作全面上路，美国方面的态度也将随之软下来。美国半导体产品还可以进入中国，但到那时主动权将牢牢掌握在我们自己的手里。</p>
</blockquote>

<h2>工具</h2>

<p>1、</p>

<p>开源的社区软件，形式非常新颖美观。</p>

<p>2、</p>

<p>通过 HTTP Header 读写 JSON 数据的免费 datastore。</p>

<p>3、</p>

<p>Node 应用的火焰图生成工具，用于性能分析。</p>

<p>4、</p>

<p>DNS 响应时间的命令行比较脚本。</p>

<p>5、</p>

<p>多张图片合成一张图片的浏览器 JS 库，使用了 Canvas。</p>

<p>6、</p>

<p>一个基于 Bootstrap4 的面板（dashboard）组件库。</p>

<p>7、</p>

<p>老牌的多人实时编辑协同工具。</p>

<h2>新奇</h2>

<p>1、</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2018/bg2018042305.jpg" alt="" title="" /></p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2018/bg2018042306.png" alt="" title="" /></p>

<p>Braille Neue 是布里叶盲文系统与正常字母的结合，无障碍设计的典范，为什么没有人早点想到这个点子呢。</p>

<p>2、</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2018/bg2018042307.jpg" alt="" title="" /></p>

<p>一个非常牛的项目，作者在 Macbook 的摄像头上面，架了一块镜子。然后，自动捕捉并识别手指的坐标。</p>

<p>3、</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2018/bg2018042308.png" alt="" title="" /></p>

<p>水母版的《超级马里奥》网页游戏，所有东西都会像水母一样升缩。</p>

<p><strong>4、小狗 USB</strong></p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2018/bg2018042309.jpg" alt="" title="" /></p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2018/bg2018042310.jpg" alt="" title="" /></p>

<h2>本周金句</h2>

<p>人生就像玻璃窗上的苍蝇，前途一片光明，却找不到出路。</p>

<h2>欢迎订阅</h2>

<p>这个专栏会本步更新在我的。</p>

<p>微信搜索"<strong>阮一峰的网络日志</strong>"或者扫描二维码，即可手机订阅。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2018/bg2018042311.jpg" alt="" title="" /></p>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2018-04-22T23:14:57+08:00">2018年4月22日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>文集：</li>
<li>社交媒体：</li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------
<h1 id="#title_1" >2、文章： 直播终端技术比较：Native vs H5 vs WebRTC vs 小程序</h1>
冼牛
[http://www.infoq.com/cn/articles/live-broardcast-native-vs-h5-vs-webrtc-vs-miniprogram?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/live-broardcast-native-vs-h5-vs-webrtc-vs-miniprogram?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/live-broardcast-native-vs-h5-vs-webrtc-vs-miniprogram/zh/smallimage/logo1-1524330440179.jpg"/><p>连麦直播技术逐步在原生APP, 浏览器H5，浏览器WebRTC，微信小程序上延伸，衍生出更加丰富的生态，提供更加便捷和良好的用户体验，对视频直播平台和用户来说是好消息。然而，欲带皇冠，必承其重。特别是在浏览器WebRTC和微信小程序上，开发者要充分理解这些类型终端的特点和局限，才能更好地在上面利用连麦直播技术进行创新，服务用户。</p> <i>By 冼牛</i>
---------------
<h1 id="#title_2" >3、文章： 专访Rafael Schloming：用于微服务开发人员的工作流程和部署模式</h1>
Daniel Bryant
[http://www.infoq.com/cn/articles/microservice-developer-workflows?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/microservice-developer-workflows?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/microservice-developer-workflows/zh/headerimage/GettyImages-616902766_preview-1522943564274.jpeg"/><p>基于他2013年在Datawire开发微服务应用的经历，Rafael Schloming认为开发负责人应该问的问题中最重要的一个(虽然经常被忽略)是:“如何分拆我庞大的整体过程?”因为开发过程对于建立和保持工作速度是至关重要的。</p> <i>By Daniel Bryant</i> <i> Translated by 冬雨</i>
---------------
<h1 id="#title_3" >4、文章： 功夫贷首席科学家黄利舟：90 亿放款、1000 万用户背后的Fintech 数据服务实践</h1>
黄利舟
[http://www.infoq.com/cn/articles/91gfd-huanglizhou-fintech-practice?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/91gfd-huanglizhou-fintech-practice?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/91gfd-huanglizhou-fintech-practice/zh/smallimage/LOGO-devops-1510006950409-1524334551673.jpeg"/><p>3 月 29 日，TGO 鲲鹏会杭州分会会员、功夫贷合伙人兼首席科学家黄利舟作为 TGO 线上分享第六季的嘉宾，以直播的形式分享了 数据在 Fintech 中的应用 。本文根据当天直播内容整理。</p> <i>By 黄利舟</i>
---------------
<h1 id="#title_4" >5、视频演讲： 开源分布式监控 CAT 系统的高可用实践</h1>
吴其敏
[http://www.infoq.com/cn/presentations/the-practice-of-open-source-distributed-monitoring-cat-system?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/the-practice-of-open-source-distributed-monitoring-cat-system?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/presentations/the-practice-of-open-source-distributed-monitoring-cat-system/zh/mediumimage/wuqimin_270-1524137353553.jpg"/><p>线上发布了服务，怎么知道它一切正常？为什么一个低级错误，需要花一个通宵、十几个人来排错？某个核心服务挂了，导致大量报错，如何确定到底是哪里出了问题？应用程序有性能瓶颈，如何提供一些有效工具发现？该主题主要分享 CAT 系统的高可用架构设计思路、应用实践以及如何提高业务系统的敏捷性和伸缩性。</p> <i>By 吴其敏</i>
---------------
<h1 id="#title_5" >6、文章： 区块链毁誉参半，如何客观、理性、全面的看待区块链的本质，现状剖析和未来预测</h1>
高泽龙
[http://www.infoq.com/cn/articles/blockchain-essence-present-and-future?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/blockchain-essence-present-and-future?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/blockchain-essence-present-and-future/zh/smallimage/agil-series-1508534878617-1524331549986.jpeg"/><p>区块链的本质是什么？我们又该如何看待区块链？</p> <i>By 高泽龙</i>
---------------