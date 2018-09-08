## 文章索引
1、 <a href="#1每周分享第-21-期" >每周分享第 21 期</a><br/>
2、 <a href="#2专访尤雨溪先别管40了vue-cli重构了解一下" >专访尤雨溪：先别管4.0了，Vue CLI重构了解一下</a><br/>
3、 <a href="#3谷歌开源的加密库tink正式发布12版本" >谷歌开源的加密库Tink正式发布1.2版本</a><br/>
4、 <a href="#4与ibm的lin-sun关于istio-10和微服务的问答" >与IBM的Lin Sun关于Istio 1.0和微服务的问答</a><br/>
5、 <a href="#5谷歌首创基于云的ai自治系统为数据中心自动降温" >谷歌首创基于云的AI自治系统，为数据中心自动降温</a><br/>
6、 <a href="#6抖音技术开放日报名中日活15亿背后技术全解" >抖音技术开放日报名中：日活1.5亿背后技术全解</a><br/>
7、 <a href="#7腾讯优图升级为计算机视觉研发中心与科学宣布战略合作" >腾讯优图升级为计算机视觉研发中心，与《科学》宣布战略合作</a><br/>
8、 <a href="#8how-github-removed-jquery-from-their-frontend" >How GitHub Removed jQuery From Their Frontend</a><br/>
9、 <a href="#9getting-started-with-machine-learning" >Getting Started With Machine Learning</a><br/><h1 id="#title_0" >1、每周分享第 21 期</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2018/09/weekly-issue-21.html](http://www.ruanyifeng.com/blog/2018/09/weekly-issue-21.html)
<p>这里记录过去一周，我看到的值得分享的东西，每周五发布。</p>

        <p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018090701.jpg" alt="" title="" /></p>

<p>漫画家蔡志忠有一个演讲，题目叫做。读完这份演讲稿，我觉得他说的有道理。</p>

<p>有些人非常勤奋，别人休息和娱乐的时候，都在工作学习。但是努力了一辈子，人生也没有显著的提升，就像报道里经常说的："某某在平凡的岗位上，勤勤恳恳工作了一辈子"。</p>

<p>另一方面，很多成功者似乎也没有特别努力，就取得了许多成就，过上了好日子。蔡志忠以自己为例，他从小就喜欢画画，然后一直画，不知不觉就成了大漫画家，名利双收，从没有觉得过得很辛苦。</p>

<blockquote>
  <p>老师或父母老是说，努力就会走到巅峰----才怪。如果这样，不是所有人都走上巅峰了吗？没有人开始不努力，为什么后来不努力，因为努力没有效果。"</p>

<p>人生不是走斜坡，你持续走就可以走到巅峰；<strong>人生像走阶梯，每一阶有每一阶的难点，</strong>学物理有物理的难点，学漫画有漫画的难点，你没有克服难点，再怎么努力都是原地跳。所以当你克服难点，你跳上去就不会下来了。</p>
</blockquote>

<p>蔡志忠的核心观点就是黑体的那句话，成功的人生是台阶式向上，而不是一条水平线。努力只是说明你拼命在走，跟你能不能向上走，关系不大。那些努力却没有结果的人，根本原因就在于，他一直走在平面上，没有走到更高的台阶。</p>

<p>也就是说，<strong>垂直方向的努力更有意义，水平方向的努力意义不大。</strong>你把同一件事情勤奋地做上十遍，还是只会做这一件事；你做完这件事后，再去挑战更难的事情，就有机会学会做两件事。</p>

<p>初学者经常问我，前端开发应该学习哪一个框架？我的回答就是，你觉得哪一个框架比较容易，就用那个。因为它们都是解决同样的问题，你只要知道怎么解决就可以了，没必要深究哪一个解决得更好。<strong>对你更重要的是，要去解决更多的问题，而不是如何最好地解决一个问题。</strong></p>

<p>只有通过解决更多的问题，人生才能摆脱水平运动，进入上升运动。当然，这里还有一个天赋和兴趣的问题，如果找到属于你的领域，不用特别努力就能上台阶；如果找不对领域，再努力也只能做水平运动。</p>

<h2>新闻</h2>

<p>1、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018090702.jpg" alt="" title="" /></p>

<p>本周一（9月2日）是 Chrome 浏览器的10岁生日。十年来，这个项目带动了无数创新，让互联网产生了天翻地覆的变化。</p>

<p>十年前，主流浏览器还是 IE6，JS 仍然是一种玩具语言，一大堆无法调试的运行时错误。谷歌决定做自己的浏览器，为此特别开发了底层引擎 V8。发布的那天，所有人都震惊了，原来JS可以运行得这么快...... 后来，V8 导致了 Node 的诞生，Chrome 导致了 Electron 和 ChromeOS。</p>

<p>为了纪念了这个日子，Chrome、Gmail、Google Drive 都在这一天发了新版。</p>

<p>2、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018090703.jpg" alt="" title="" /></p>

<p>德国科学家发明了一种机器充电臂，它能自动给电动汽车充电，完全不用司机下车。电动车开到它的旁边，摄像头自动识别出充电口，然后将充电臂伸进去，充满后再缩回去。</p>

<p>3、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018090704.jpg" alt="" title="" /></p>

<p>美国一家创业公司推出车窗广告服务。他们在车内安装微型投影仪，在车窗上向外播放全彩广告，车主可以获取广告分成。</p>

<p>以后堵车的时候就有意思了，你的前后左右都是彩色屏幕，同时向你播放广告。</p>

<p>4、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018090705.jpg" alt="" title="" /></p>

<p>糖尿病患者对血糖含量是非常敏感的，血糖过高，就需要立刻注射胰岛素，否则会有严重后果。但是怎么能实时知道血糖过高呢？科学家发明了人工胰脏，它每隔几分钟自动检测血糖含量，一旦发现血糖过高，就向血液注入胰岛素。</p>

<p>现在，这种设备已经有 DIY 方案，病人随身携带葡萄糖监测仪，测试结果通过蓝牙传回手机，发现含量过高就会报警，提醒要注射胰岛素。整套设备的成本大约250美元。</p>

<p>5、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018090706.jpg" alt="" title="" /></p>

<p>亚马逊的市值本周突破了1万亿美元，成为历史上第二家万亿美元公司（第一家是苹果）。这使得亚马逊的老板贝佐斯的财富暴涨，2018年就增加了670亿美元，总资产到达了1670亿美元，成为世界最富有的人。</p>

<p>今年670亿美元的净增长，相当于他每小时就新增800万美元的财富。</p>

<p>6、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018090707.jpg" alt="" title="" /></p>

<p>微软共同创始人保罗艾伦投资的 Stratolaunch 飞机，最近正式亮相。它是世界上最大的飞机，翼展可以达到117米，主要用来在空中发射火箭。由于它可以多次使用，因此显著降低了火箭的发射成本。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018090708.jpg" alt="" title="" /></p>

<p>7、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018090709.jpg" alt="" title="" /></p>

<p>多仓库管理工具 Lerna 修改了 MIT 许可证，加了一个条款：凡是帮助美国海关移民执行局（ICE）虐待非法移民的公司，一律不得使用该工具，排在第一名的是微软。在这个名单的基础上，又加上了一些虐待劳工的公司，包括苹果、沃尔玛和特斯拉。</p>

<p>更新：这个许可证现在又被改回来了。</p>

<p>8、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018090710.jpg" alt="" title="" /></p>

<p>有人统计了，什么主题的电子书在亚马逊销售额最高。前5名全部是教科书，里面有4种是医学教科书。排名最高的计算机类书籍是 Access 数据库。</p>

<p>9、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018090711.jpg" alt="" title="" /></p>

<p>最近，TempleOS 操作系统的作者特里.戴维斯（Terry a. Davis）去世了。他生于1969年，是一个程序员，曾经为一些大公司工作。工作十年后，他患上了精神分裂症，必须接受治疗。</p>

<p>2003年，他声称接收到了上帝的指令，要为上帝写一个操作系统，起名为 TempleOS（temple的意思是圣殿）。这个系统的编程语言是他自创的 HolyC（神圣的C）。IT 行业没人认真对待 TempleOS，特里.戴维斯后来一无所有，没有房子，不得不睡在车上。没人知道他是怎么死的，TempleOS 官网上只有一句话，宣布他死了，仅此而已。</p>

<p>10、<strong>一句话新闻</strong></p>

<blockquote>
  <ul>
<li>，将禁止第三方 Cookie 追踪用户。举例来说，我访问脸书，脸书在我的浏览器留下 Cookie。然后，我又访问其他引用脸书的网站，这时Firefox将禁止发向脸书的请求读取Cookie。</li>
<li>建议成员国取消夏令时。目前，所有28个欧盟成员国被要求在3月的最后一个星期天将时钟拨快一小时，并在10月的最后一个星期天拨慢一个小时。</li>
<li>称，希望打造"终身不退休社会"，雇佣不设年龄限制，只要有意愿就能参加工作。  </li>
</ul>
</blockquote>

<h2>教程</h2>

<p>1、（英文）</p>

<p>有一句名言："计算机科学有两大难题：缓存不一致和变量命名。"本文就介绍缓存与源数据不一致的基本知识。</p>

<p>2、（英文）</p>

<p>用户发出的请求，很大一部分是缓存服务器响应的。这意味着，不一定需要感染源站，只要能在缓存服务器注入恶意代码，就能达到目的。本文给出了这方面的详细介绍以及实际的案例。</p>

<p>3、（英文）</p>

<p>OCaml 是一种通用语言，在函数式编程里面加入了命令式编程和面向对象编程的特性。</p>

<p>4、（英文）</p>

<p>Python 有大量的魔术方法（方法名前后有两个下划线），本文给出了一个完整的介绍。</p>

<p>5、（英文）</p>

<p>本文详细指导你搭建一个免费推特机器人，每当有人在推特 follow 你，就会收到一条欢迎私信。</p>

<p>6、（中文）</p>

<p>地中海沿岸，很多城市最热闹的大街就在海边。我一直很奇怪，难道他们不怕涨潮吗？现在终于确认了，地中海几乎没有潮汐。</p>

<p>7、（英文）</p>

<p>Swift 语言一般用于开发 iPhone 的 App，现在开始有人尝试将它用于服务端编程。</p>

<p>8、（中文）</p>

<p>想要学习浏览器自动化的同学，可以看看这篇中文教程。</p>

<p>9、（英文）</p>

<p>.snap 是一种新的 Linux 安装包格式，最大特点就是自带依赖，某种程序上很像容器。</p>

<p>10、（英文）</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018090712.jpg" alt="" title="" /></p>

<p>本文比较了谷歌、微软、亚马逊、IBM 四家公司的人脸检测服务的准确性。</p>

<h2>资源</h2>

<p>1、 </p>

<p>该网站收集各个学科开源的大学教材。</p>

<p>2、</p>

<p>25道 C++ 的编程题，经常用于面试。</p>

<p>3、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018090713.jpg" alt="" title="" /></p>

<p>中国护照排在第55位，免签国29个，落地签国49个。</p>

<p>4、</p>

<p>一个网页源码的搜索引擎，可以搜索哪些网页使用 react.min.js，或者服务器是 <code>Server: nginx/1.4.7"</code> 。</p>

<p>5、</p>

<p>一个收集 Java 核心知识的中文库。</p>

<p>6、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018090714.jpg" alt="" title="" /></p>

<p>《计算机网络：系统方法》英文原版开源了（）。 </p>

<h2>工具</h2>

<p>1、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018090715.jpg" alt="" title="" /></p>

<p>一个命令行操作录制成 SVG 动画的工具，不错。</p>

<p>2、</p>

<p>eno 是类似 yaml、 toml 的一种配置语言。</p>

<p>3、</p>

<p>Node 脚本里面加载 wasm 模块的处理器，即让 Node 可以方便地运行 wasm 模块。</p>

<p>4、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018090716.jpg" alt="" title="" /></p>

<p>一个生成对称图形的网站，可以用来生成墙纸。</p>

<p>5、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018090717.jpg" alt="" title="" /></p>

<p>Kakoune 是一个类似 Vim 的编辑器，它的主要特点是更友好合理的命令语法。 Vim 的命令是"动词 + 对象"，Kakoune 的命令是"对象 + 动词"。</p>

<p>7、</p>

<p>Mithril 是一个类似 React 的轻量级前端端架，比 React 简单。主要特点有两个：一个是路由、状态管理、fetch 这些主要功能都内置了，二是体积很小（8kb）。</p>

<p>8、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018090718.jpg" alt="" title="" /></p>

<p>Favioli 是一个很好玩的 Chrome 浏览器插件。它可以将网页的 Favicon 替换成 Emoji。</p>

<p>9、</p>

<p>codesandbox.io 是一个前端代码的在线编辑器，支持各种不同的框架，可以随时预览代码的运行结果。</p>

<p>10、</p>

<p>mobiledoc 是一种数据格式，用于所见即所得编辑器的底层数据。mobiledoc-kit 是这种数据格式的开发工具，开发者可以基于这套工具方便地做出编辑器。</p>

<h2>文摘</h2>

<p>1、<strong>生命的诞生</strong></p>

<p>以下摘自比尔布莱森的《万物简史》。</p>

<p>1953年，芝加哥大学的研究生斯坦利·米勒拿起两个长颈烧瓶----一个盛着一点水，代表远古的海洋，一个装着甲烷、氨和硫化氢的气体混合物，代表地球早期的大气----然后用橡皮管子把两个瓶子一连，放了几次电火花算作闪电。几个星期以后，瓶子里的水呈黄绿色，变成了营养丰富的汁，里面有氨基酸、脂肪酸、糖以及别的有机化合物。米勒的导师、诺贝尔奖获得者哈罗德·尤里欣喜万分，说："我可以打赌，上帝肯定是这么干的。"</p>

<p>所有生命的始发点，都可以追溯到同一种原始的抽动。极其遥远的过去，在某个时刻，有一小块化学物质躁动一下，于是就有了生命。它吸收营养，轻轻地搏动几下，经历了短暂的存在。这么多情况也许以前发生过，也许发生过多次。但是，这位老祖宗干了另一件非同寻常的事：它将自己一分为二，产生了一个后代。一小袋遗传物质从一个生命实体转移给了另一个生命实体，此后就这样延续下去，再也没有停止过。这是个创造我们大家的时刻。生物学家有时候将其称为"大诞生"。</p>

<p>2、</p>

<p>第二次世界大战，希特勒包围列宁格勒长达900天，切断了200万居民的所有食物供应，企图饿死俄国人。冬天的时候，成千上万的人饿死了。列宁格勒居民饿到吃木屑，许多人试图在零下30°C的天气里步行几公里到食品配送亭，结果冻死在路上。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018090719.jpg" alt="" title="" /></p>

<p>当时，列宁格勒瓦维洛夫植物研究所藏有近20万种植物的种子，其中约四分之一可食用，是世界上最大的粮食作物遗传多样性库之一。其中有大量的大米，小麦，玉米，豆类和土豆，足以支撑研究所的植物学家吃饱。但是，科学家们并没有用食物来挽救自己的生命，而是保护这些种子不受纳粹以及街头寻找食物的人们的破坏。</p>

<p>科学家全天候轮流保护着仓库，冷得麻木，饥饿消瘦。随着围困时间越来越长，他们一个接一个地开始饿死，但至死没有吃过一粒研究所的种子。1942年1月，花生专家 Alexander Stchukin 在写字台上去世。植物学家德米特里·伊万诺夫（Dmitri Ivanov）也死于饥饿，他的周围是数千包大米种子。1944年春天，德军撤退时，有9人已经饿死。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018090720.jpg" alt="" title="" /></p>

<p>这个种子库是世界第一个植物多样性种子库。它由俄罗斯最杰出的植物学家和遗传学家尼古拉·瓦维洛夫于1926年建立。他是首批预见植物多样性消失的科学家之一，并认识到这可能对粮食生产造成灾难性影响。瓦维洛夫在一个贫困的乡村长大，饱受经常性的作物歉收和食物配给困扰，从很小的时候就开始痴迷于他的祖国俄罗斯和世界的饥荒。20世纪早期，他在五大洲进行了广泛的访问，共访问了64个国家，收集了各种植物和粮食作物标本。他自学了15种语言，以便与当地农民交谈。经过近十年的旅行和数百次旅行后，成立了列宁格勒植物研究所。</p>

<p>下图是瓦维洛夫制作的种子标本。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018090721.jpg" alt="" title="" /></p>

<h2>新奇</h2>

<p>1、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018090722.jpg" alt="" title="" /></p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018090723.jpg" alt="" title="" /></p>

<p>宏碁公司新推出了一款 Predator Thronos 游戏椅，自带三个27寸显示器，可以让你躺着（140度后仰）打游戏，还会随着游戏一起震动。</p>

<p>这个产品有前途，如果能解决睡眠问题就好了，打累了睡一会，醒了接着打。以后网吧可能都是这种椅子。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018090724.jpg" alt="" title="" /></p>

<p>2、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018090725.jpg" alt="" title="" /></p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018090726.jpg" alt="" title="" /></p>

<p>加拿大科学家做出来了一个原型设备，可以把触摸屏卷起来。</p>

<h2>本周图片</h2>

<p>1、</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018090727.jpg" alt="" title="" /></p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018090728.jpg" alt="" title="" /></p>

<p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018090729.jpg" alt="" title="" /></p>

<h2>本周金句</h2>

<p>1、</p>

<p>一个网页依赖于大约十万个其他发明。没有 HTML 代码的发明，没有计算机编程，没有LED或阴极射线管，没有计算机芯片，没有电话线，没有长距离信号中继器，没有发电机，没有高速涡轮机，就没有任何网页。（凯文·凯利）</p>

<p>2、</p>

<p>我很遗憾花了这么多年时间专注于一个狭窄的领域，忽略了许多重要的技能。我严重低估了产业界可以学到的东西，以及博士的机会成本！</p>

<p>-- ，数学博士。他发表文章认为，即使人工智能这样的领域，博士学位都是不必要的，不值得专门去读。</p>

<p>3、</p>

<p>伟大的文明会崩溃，技术也会倒退。罗马帝国灭亡后，欧洲的技术水平大大倒退，停滞发展了1000年。这样的事情，如今也不是没有可能发生。</p>

<p>-- TIm O'reily《未来地图》</p>

<h2>欢迎订阅</h2>

<p>这个专栏每周五发布，同步更新在我的。</p>

<p>微信搜索"<strong>阮一峰的网络日志</strong>"或者扫描二维码，即可订阅。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2018/bg2018042311.jpg" alt="image | left" title="" /></p>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2018-09-07T11:15:29+08:00">2018年9月 7日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>文集：</li>
<li>社交媒体：</li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------
<h1 id="#title_1" >2、专访尤雨溪：先别管4.0了，Vue CLI重构了解一下</h1>
覃云
[http://www.infoq.com/cn/news/2018/09/vue-v3-refactoring?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/09/vue-v3-refactoring?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>InfoQ 采访了尤雨溪，以下是对采访内容的整理。</p> <i>By 覃云</i>
---------------
<h1 id="#title_2" >3、谷歌开源的加密库Tink正式发布1.2版本</h1>
Thai Duong
[http://www.infoq.com/cn/news/2018/09/Google-open-source-Tink-1.2?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/09/Google-open-source-Tink-1.2?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>为了帮助开发人员交付安全的加密代码，谷歌开发了Tink—一个支持多语言的跨平台加密库。他们希望Tink能够成为一个社区项目，因此Tink从一开始就托管在GitHub上，并且已经吸引到了几个外部贡献者。</p> <i>By Thai Duong</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_3" >4、与IBM的Lin Sun关于Istio 1.0和微服务的问答</h1>
Rags Srinivas
[http://www.infoq.com/cn/news/2018/09/Istio-lin-sun?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/09/Istio-lin-sun?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>InfoQ联系到了IBM的高级技术成员Lin Sun，她同时还是Istio项目版本释放团队的参与者，讨论了Istio的总体情况以及1.0发布版本的具体情况。</p> <i>By Rags Srinivas</i> <i> Translated by 张卫滨 </i>
---------------
<h1 id="#title_4" >5、谷歌首创基于云的AI自治系统，为数据中心自动降温</h1>
DeepMind
[http://www.infoq.com/cn/news/2018/09/google-cloud-AI-sys-lowertemp?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/09/google-cloud-AI-sys-lowertemp?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>2016年，DeepMind联合开发了一个人工智能驱动的推荐系统，用以提高谷歌数据中心的能源效率。现在，他们将这个系统提升到一个新的水平：在数据中心运营专家的监督之下直接让AI系统控制数据中心的冷却系统。这种首创的基于云的控制系统现在可以安全地为多个谷歌数据中心提供节能服务。</p> <i>By DeepMind</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_5" >6、抖音技术开放日报名中：日活1.5亿背后技术全解</h1>
王霖
[http://www.infoq.com/cn/news/2018/09/Douyin-tech-open-day?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/09/Douyin-tech-open-day?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>抖音于 2016 年 9 月上线，一年多时间就成为了行业内现象级的短视频应用，是字节跳动旗下除了今日头条等业务以外的核心产品之一。截止到今年 6 月，抖音的国内日活突破 1.5 亿，刷抖音已经成为当下人们记录美好生活的方式。</p> <i>By 王霖</i>
---------------
<h1 id="#title_6" >7、腾讯优图升级为计算机视觉研发中心，与《科学》宣布战略合作</h1>
陈利鑫
[http://www.infoq.com/cn/news/2018/09/Tencent-cooperation-with-Science?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/09/Tencent-cooperation-with-Science?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>9月6日，在腾讯优图计算机视觉峰会上，腾讯高级执行副总裁汤道生宣布，腾讯优图实验室升级为腾讯计算机视觉研发中心，并首次公开该实验室最全面的应用落地案例；与此同时，腾讯优图实验室也正式宣布和《科学》期刊达成了战略合作，探讨通过学术奖金、产学研交流等多种形式，在人工智能前沿研究领域展开广泛合作。</p> <i>By 陈利鑫</i>
---------------
<h1 id="#title_7" >8、How GitHub Removed jQuery From Their Frontend</h1>

[https://javascriptweekly.com/issues/402](https://javascriptweekly.com/issues/402)
<table border=0 align="center" border="0">
  <tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   ">

  <div>    
    <table border=0 border=0><tr>
<td align="left" style="padding-left: 4px; font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   "><p>#402 — September  7, 2018</p></td>
<td align="right" style="padding-right: 4px; font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   "><p></p></td>
</tr></table>
    
    <table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0 12px;"><p>JavaScript Weekly</p></td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
      <p>Apologies if you notice today's issue is a little lower tempo than usual. We have some great things coming up, including more interviews like Dr. Axel's in , but today I've been struck by a sickness bug 😷 and have struggled to even get this far. To a better next week! 🙂<br>
      <span style="color: #666666;"><em>— Peter Cooper, editor</em></span></p>
    </td></tr></table>
<div style="   margin-top: 14px; margin-bottom: 8px;  "></div>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — GitHub has just been able to drop jQuery as a dependency of the frontend code for GitHub.com. This transition has taken years and here’s what they’ve learnt and what libraries have replaced it.</p>
  <p>GitHub Engineering </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;">.</p>
  <p>Sindre Sorhus </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;">.</p>
  <p>Progress Kendo UI <span style="text-transform: uppercase; padding: 1px 4px;  margin-left: 4px; font-size: 0.9em;   color: #997 !important;">sponsor</span></p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Sacha Greif’s popular survey returns, aiming to see what tools and technologies in the JavaScript space that developers are using, happy with and excited about. Results are expected in November and we’ll share them then.</p>
  <p>Sacha Greif </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Want to get your head around <code>setTimeout</code> vs <code>setInterval</code> vs <code>setImmediate</code> vs  <code>requestAnimationFrame</code> and others? This will help.</p>
  <p>Nolan Lawson </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></p>
  <p>Sufyan Dawoodjee </p>
</td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0;"><p>💻 Jobs</p></td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;">.</p>
  <p>x-team </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Create a profile to connect with inspiring companies seeking JavaScript devs.</p>
  <p>Vettery </p>
</td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0;"><p>📘 Tutorials and Opinions</p></td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — A preview of an as yet unreleased course, but even these three pages might help you out if you’re still learning how promises and async/await can improve your code.</p>
  <p>Frontend Armory </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Get your browser to speak back to you.</p>
  <p>Manuel Wieser </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Combine A-Frame, PubNub, and WebVR to launch a browser-based VR game.</p>
  <p>PubNub <span style="text-transform: uppercase; padding: 1px 4px;  margin-left: 4px; font-size: 0.9em;   color: #997 !important;">sponsor</span></p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Hugo Di Francesco </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — The <code>matchMedia</code> method is the key.</p>
  <p>Craig Buckler </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — <em>“A complete breakdown on why we needed Redux in the past, and why we don’t any more.”</em></p>
  <p>Jack Scott </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Google Developers </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — One for the functional programming fans :-)</p>
  <p>Reg Braithwaite </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>mongodb <span style="text-transform: uppercase; padding: 1px 4px;  margin-left: 4px; font-size: 0.9em;   color: #997 !important;">sponsor</span></p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Hubert Zub </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — TypeScript has never been easier to adopt thanks to the new TypeScript plugin for Babel.</p>
  <p>Matt Turnbull </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Lighthouse is a performance auditing tool embedded in Chrome.</p>
  <p>Tim Nolet </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Phil Leggetter </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Cathy Ha </p>
</td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0;"><p>🔧 Code and Tools</p></td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"> Addy Osmani.</p>
  <p>Sasha Koss </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span> — Take online payments in a custom form using Vue and the Square Payment Form.</p>
  <p>Square Developer <span style="text-transform: uppercase; padding: 1px 4px;  margin-left: 4px; font-size: 0.9em;   color: #997 !important;">sponsor</span></p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></span></p>
  <p>Angular </p>
</td></tr></table>

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
  
  <p><span style="font-weight: 600; font-size: 1.1em; color: #000;"></p>
  <p>React GitHub Repo </p>
</td></tr></table>
<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px;">

<table border=0 border=0><tr><td style="font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;    padding: 0px 15px;">
<p>🗓 <strong>Upcoming JavaScript Events</strong></p>

<ul>
<li>
 — A one day single track event.</li>

<li>
 — A new 2 day conference focused on all front end frameworks with keynotes from the teams of the most popular ones.</li>

<li>
 — One of the largest JavaScript events. Organized by the Linux Foundation.</li>

<li>
 — A two-day, two-track, developer event focused on mobility and the cutting-edge JavaScript ecosystem.</li>

<li></li>

</ul>

</td></tr></table>
</td></tr></table>
<table border=0 border=0><tr><td style=" font-family: -apple-system,BlinkMacSystemFont,Helvetica,sans-serif; font-size: 15px; line-height: 1.55em;   "></td></tr></table>
</div>

  </td></tr>
</table>





<img src="https://javascriptweekly.com/open/402/rss" width="1" height="1" />
---------------
<h1 id="#title_8" >9、Getting Started With Machine Learning</h1>
Alvin Wan
[https://www.smashingmagazine.com/2018/09/getting-started-with-machine-learning/](https://www.smashingmagazine.com/2018/09/getting-started-with-machine-learning/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/09/getting-started-with-machine-learning/" />
              <title>Getting Started With Machine Learning</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>Getting Started With Machine Learning</h1>
                  
                    
                    <address>Alvin Wan</address>
                  
                  <time datetime="2018-09-07T14:00:26&#43;02:00" class="op-published">2018-09-07T14:00:26+02:00</time>
                  <time datetime="2018-09-07T14:07:14&#43;00:00" class="op-modified">2018-09-07T14:07:14+00:00</time>
                </header>
                

<p>The goal of machine learning is to find patterns in data and use those patterns to make predictions. It can also give us a framework to discuss machine learning problems and solutions &mdash; as you’ll see in this article.</p>

<p>First, we will start with definitions and applications for machine learning. Then, we will discuss abstractions in machine learning and use that to frame our discussion: data, models, optimization models, and optimization algorithms. Later on in the article, we will discuss fundamental topics that underlie all machine learning methods and conclude with practical guidance for getting started with using machine learning. By the end, you should have an understanding of how to advance your practice and study of machine learning.</p>

<p>Let’s begin.</p>

<h3 id="so-what-exactly-is-machine-learning">So, What Exactly Is Machine Learning?</h3>

<p>Machine learning is generically a set of techniques to find patterns in data. Applications range from self-driving cars to personal AI assistants, from translating between French and Taiwanese to translating between voice and text. There are a few common applications of machine learning that already or could potentially permeate your day-to-day.</p>

<ol>
<li><strong>Detecting anomalies</strong><br />
Recognize spikes in website traffic or highlight abnormal bank activity.</li>
<li><strong>Recommend similar content</strong><br />
Find products you may be looking for or even Smashing Magazine articles that are relevant.</li>
<li><strong>Predict the future</strong><br />
Plan the path of neighboring vehicles or identify and extrapolate market trends for stocks.</li>
</ol>

<p>The above are few of many applications of machine learning, but most applications tie back to learning the underlying <em>distribution</em> of data. A distribution specifies events and probability of each event. For example:</p>

<ul>
<li>With 50% probability, you buy an item $5 or less.</li>
<li>With 25% probability, you buy an item $5-$10.</li>
<li>With 24% probability, you buy an item $10-100.</li>
<li>With 1% probability, you buy an item &gt; $100.</li>
</ul>



  <aside class="product-panel product-panel__tilted product-panel--book" data-audience="non-subscriber" data-remove="true">
    <div class="container product-panel--book__container">
      <div class="panel__description panel__description--book">
        <p>
          Is your pattern library up to date today? <em>Alla Kholmatova</em> has just finished a fully fledged book on <strong>Design Systems</strong> and how to get them right. With common traps, gotchas and the lessons she learned. Hardcover, eBook. <em>Just sayin'.</em>
        </p>
        <a href="https://smashed.by/uxpaneldsbook">
          <button class="btn btn--green btn--large">
            Table of Contents&nbsp;&rarr;
          </button>
        </a>
      </div>
      <div class="panel__image panel__image--book">
        <a href="https://smashed.by/uxpaneldsbook" class="books__book__image">
        <div class="books__book__img">
          <img src="https://www.smashingmagazine.com/images/books/design-systems--large-opt.png">
        </div>
      </a>
      </div>
    </div>
  </aside>








    









<p>Using this distribution, we can accomplish all of our tasks above:</p>

<ol>
<li><strong>Detecting anomalies</strong><br />
With a $100 purchase, we can confidently call this an anomaly.</li>
<li><strong>Recommend similar content</strong><br />
A purchase of $3 means we should recommend more items $5 or less.</li>
<li><strong>Predict the future</strong><br />
Without any prior information, we can predict that the next purchase will be $5 or less.</li>
</ol>

<p>With a distribution of data, we can accomplish a myriad of tasks. In sum, one goal in machine learning is to learn this distribution.</p>

<p>Even more generically, our goal is to learn a specific function with particular inputs and outputs. We call this function our <em>model</em>. Our input is denoted <code>x</code>. Say our model, which accepts input <code>x</code>, is</p>

<pre><code class="language-javascript">f(x) = ax
</code></pre>

<p>Here, <code>a</code> is a <em>parameter</em> of our model. Each parameter corresponds to a different instance of our model. In other words, the model where <code>a=2</code> is different from the model where <code>a=3</code>. In machine learning, our goal is to learn this parameter, changing it until we do “well.” How do we determine which values of <code>a</code> do “well”?</p>

<p>We need to define a way to evaluate our model, for each parameter <code>a</code>. To start, the output of <code>f(x)</code> is our <em>prediction</em>. We will refer to <code>y</code> as our <em>label</em>, meaning the true and desired output. With our predictions and our labels, we can define a <em>loss</em> function. One such loss function is simply the difference between our prediction and our label, <code>&#124;f(x) - y&#124;</code>. Using this loss function, we can then evaluate different parameters for our model. Picking the best parameter for our model is known as <em>training</em>. If we have a few possible parameters, we can simply try each parameter and pick the one with the smallest loss!</p>

<p>However, most problems are not as simple. <strong>What happens if there are an infinite number of different parameters?</strong> Let’s say all decimal values between 0 and 1? Between 0 and infinity? This brings us to our next topic: abstractions in machine learning. We will discuss different facets of machine learning, to compartmentalize your knowledge into data, models, objectives, and methods of solving objectives. Beyond learning the right parameter, there are plenty of other challenges: how do we break down a problem as complex as controlling a robot? How do we control a self-driving car? What does it mean to train a model that identifies faces? The section below will help you organize answers to these questions.</p>

<h3 id="abstractions">Abstractions</h3>

<p>There are countless topics in machine learning &mdash; at various levels of specificity. To better understand where each piece fits in the larger picture, consider the following abstractions for machine learning. These abstractions compartmentalize our discussion of machine learning topics, and knowing them will make it easier for you to frame topics. The following classifications are taken from Professor Jonathan Shewchuck at UC Berkeley:</p>

<ol>
    <li><strong>Application and Data</strong><br />Consider the possible inputs and the desired output for the problem.<br /><blockquote><strong>Questions</strong>: What is your goal? How is your data structured? Are there labels? Is it reasonable for us to extract output from the provided inputs?<br /><br /><strong>Example</strong>: The goal is to classify pictures of handwritten digits. The input is an image of a handwritten number. The output is a number.</blockquote><br /></li>
    <li><strong>Model</strong><br />Determine the class of functions under consideration.<br /><blockquote><strong>Questions</strong>: Are linear functions sufficient? Quadratic functions? Polynomials? What types of patterns are we interested in? Are neural networks appropriate? Logistic regression?<br /><br /><strong>Example</strong>: Linear regression</blockquote><br /></li>
    <li><strong>Optimization Problem</strong><br />Formulate a concrete objective in mathematics.<br /><blockquote><strong>Questions</strong>: How do we define loss? How do we define success? Should we apply additionally penalties to bias our algorithm? Are there imbalances in the data our objective needs to consider?<br /><br /><strong>Example</strong>: Find `x` that minimizes <code>&#124;Ax-b&#124;^2</code></blockquote><br /></li>
    <li><strong>Optimization Algorithm</strong><br />Determine how you will solve the optimization problem.<br /><blockquote><strong>Questions</strong>: Can we compute a solution by hand? Do we need an iterative algorithm? Can we convert this problem to an equivalent but easier-to-solve objective, and solve that one?<br /><br /><strong>Example</strong>: Take derivative of the function. Set it to zero. Solve for our optimal parameter.</blockquote><br /></li>
</ol>

<h4 id="abstraction-1-data">Abstraction 1: Data</h4>

<p>In practice, collecting, managing, and packaging data is 90% of the battle. The data contains <em>samples</em> in which each sample is a specific realization of our input. For example, our <em>input</em> may generically be images of dogs. The first <em>sample</em> is specifically a picture of Maxie, my Bernese Mountain dog-chow chow mix at home. The second sample is specifically a picture of Charlie, a young corgi.</p>

<p>While training your model, it is important to handle your data properly. This means separating our data accordingly and not peeking prematurely at any set of data. In general, our data is split into three portions:</p>

<ol>
<li><strong>Training set</strong><br />
This is the dataset you train your model on. The model may see this set hundreds of times.</li>
<li><strong>Validation set</strong><br />
This is the dataset you evaluate your model on, to assess accuracy and tune your model or method accordingly.</li>
<li><strong>Test set</strong><br />
This is the dataset you evaluate on to assess accuracy, once at the very end. Running on the test set prematurely could mean your model overfits to the test set as well, so run only once. We will discuss the notion of “overfitting” in more detail below.</li>
</ol>

<div class="sponsors__wide-place"></div>




<h4 id="abstraction-2-models">Abstraction 2: Models</h4>

<p>Machine learning methods are split into the following two:</p>

<h5 id="supervised-learning">Supervised Learning</h5>

<p>In supervised learning, our algorithm has access to labeled data. Still, we explore the following two classes of problems:</p>

<ul>
  <li><strong>Classification</strong><br />Determine which of <code>k</code> classes <code>{C_1, C_2, ... C_k}</code> to which each sample belongs, e.g. “Which breed of dog is this?” The dog could be one of <code>{"corgi", "bernese mountain dog", "chow chow"...}</code></li>
  <li><strong>Regression</strong><br />Determine a real-valued output (which are often probabilities), e.g. “What is the probability this patient has neuroblastoma (eye cancer)?”</li>
</ul>

<h5 id="unsupervised-learning">Unsupervised Learning</h5>

<p>In unsupervised learning, our algorithm does not have access to labels, and we explore the following classes of problems:</p>

<ul>
  <li><strong>Clustering</strong><br />Cluster samples into <code>k</code> clusters. We do not have a label for the resulting clusters. “Which DNA sequences are most similar?”</li>
  <li><strong>Dimensionality reduction</strong><br />Reduce the number of “unique” (linearly independent) features we consider. “What are common features of faces?”</li>
</ul>

<h4 id="abstraction-3-optimization-objective">Abstraction 3: Optimization Objective</h4>

<p>Before discussing optimization objectives and algorithms, we&rsquo;ll need an example to discuss. Least squares are the canonical example. We will restrict our attention to a specific form of least squares: Let us return to our grade-school problem of fitting a line to some points.</p>

<p>Let’s recall the equation of a line:</p>

<pre><code class="language-javascript">y = m * x + b
</code></pre>

<p>Assume we have such a line. This is the true underlying model.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6680e9a9-e6f1-4853-bb47-7bf384f6e366/1-getting-started-with-ml.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6680e9a9-e6f1-4853-bb47-7bf384f6e366/1-getting-started-with-ml.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6680e9a9-e6f1-4853-bb47-7bf384f6e366/1-getting-started-with-ml.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6680e9a9-e6f1-4853-bb47-7bf384f6e366/1-getting-started-with-ml.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6680e9a9-e6f1-4853-bb47-7bf384f6e366/1-getting-started-with-ml.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6680e9a9-e6f1-4853-bb47-7bf384f6e366/1-getting-started-with-ml.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6680e9a9-e6f1-4853-bb47-7bf384f6e366/1-getting-started-with-ml.png"
			sizes="100vw"
			alt=" true model"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			True model. The line that generates our data. ()
		</figcaption>
	
</figure>


<p>Now, sample points from this line.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c15add57-28c5-4e12-9b9a-24c254f0ff0e/2-getting-started-with-ml.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c15add57-28c5-4e12-9b9a-24c254f0ff0e/2-getting-started-with-ml.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c15add57-28c5-4e12-9b9a-24c254f0ff0e/2-getting-started-with-ml.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c15add57-28c5-4e12-9b9a-24c254f0ff0e/2-getting-started-with-ml.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c15add57-28c5-4e12-9b9a-24c254f0ff0e/2-getting-started-with-ml.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c15add57-28c5-4e12-9b9a-24c254f0ff0e/2-getting-started-with-ml.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c15add57-28c5-4e12-9b9a-24c254f0ff0e/2-getting-started-with-ml.png"
			sizes="100vw"
			alt="true data"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			True data. Data that is sampled from the true model. ()
		</figcaption>
	
</figure>


<p>For each point, jiggle it a little bit. In other words, add <em>noise</em>, which is random perturbations. This noise is due to real-world processes.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f48c8c95-f505-4300-bd27-89ae9f087078/3-getting-started-with-ml.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f48c8c95-f505-4300-bd27-89ae9f087078/3-getting-started-with-ml.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f48c8c95-f505-4300-bd27-89ae9f087078/3-getting-started-with-ml.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f48c8c95-f505-4300-bd27-89ae9f087078/3-getting-started-with-ml.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f48c8c95-f505-4300-bd27-89ae9f087078/3-getting-started-with-ml.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f48c8c95-f505-4300-bd27-89ae9f087078/3-getting-started-with-ml.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f48c8c95-f505-4300-bd27-89ae9f087078/3-getting-started-with-ml.png"
			sizes="100vw"
			alt="noise"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Noise. Real-world perturbations that affect our data. This may be due to imprecision in measurements, lossy compression, and so on. ()
		</figcaption>
	
</figure>


<p>This gives us our <em>observed data</em>. We will call these points <code>(x_1, y_1), (x_2, y_2), (x_3, y_3)...</code>. This is the training data we are given to train a model on. We do not have access to the underlying line that generated this data (the original green line).</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5b1e254b-93c3-4158-86ea-a5876de90992/4-getting-started-with-ml.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5b1e254b-93c3-4158-86ea-a5876de90992/4-getting-started-with-ml.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5b1e254b-93c3-4158-86ea-a5876de90992/4-getting-started-with-ml.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5b1e254b-93c3-4158-86ea-a5876de90992/4-getting-started-with-ml.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5b1e254b-93c3-4158-86ea-a5876de90992/4-getting-started-with-ml.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5b1e254b-93c3-4158-86ea-a5876de90992/4-getting-started-with-ml.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5b1e254b-93c3-4158-86ea-a5876de90992/4-getting-started-with-ml.png"
			sizes="100vw"
			alt="observations"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Observations. Our true data with noise and ultimately what we will use to train a model. ()
		</figcaption>
	
</figure>


<p>Say we have an estimate for the <em>parameters</em> of a line. In this case, the parameters are <code>m</code> and <code>b</code>. This gives us a predicted line, drawn in blue below.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dd8499fa-ebeb-4c3b-b30b-c61c2a380aa6/5-getting-started-with-ml.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dd8499fa-ebeb-4c3b-b30b-c61c2a380aa6/5-getting-started-with-ml.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dd8499fa-ebeb-4c3b-b30b-c61c2a380aa6/5-getting-started-with-ml.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dd8499fa-ebeb-4c3b-b30b-c61c2a380aa6/5-getting-started-with-ml.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dd8499fa-ebeb-4c3b-b30b-c61c2a380aa6/5-getting-started-with-ml.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dd8499fa-ebeb-4c3b-b30b-c61c2a380aa6/5-getting-started-with-ml.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dd8499fa-ebeb-4c3b-b30b-c61c2a380aa6/5-getting-started-with-ml.png"
			sizes="100vw"
			alt="proposed model"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Proposed model. The result of training a model on our observations. ()
		</figcaption>
	
</figure>


<p>We wish to evaluate our blue line, to see how accurate it is. To start, we use <code>m</code> and <code>b</code> to estimate <code>y</code>. We compute a set of <code>ŷ</code> values.</p>

<pre><code class="language-javascript">ŷ_i = m * x_i + b
</code></pre>

<p>The error for a single predicted <code>ŷ_i</code> and true <code>y_i</code> is simply</p>

<pre><code class="language-javascript">(ŷ_i−y_i)^2
</code></pre>

<p>Our total error is then the sum of squared differences, across all samples. This yields our loss.</p>

<pre><code class="language-javascript">∑(ŷ_i−y_i)^2
</code></pre>

<p>Presented visually, this is the vertical distance between our observed points and our predicted line.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d2ba7e3c-e380-48d0-96a9-117d8886eab4/6-getting-started-with-ml.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d2ba7e3c-e380-48d0-96a9-117d8886eab4/6-getting-started-with-ml.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d2ba7e3c-e380-48d0-96a9-117d8886eab4/6-getting-started-with-ml.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d2ba7e3c-e380-48d0-96a9-117d8886eab4/6-getting-started-with-ml.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d2ba7e3c-e380-48d0-96a9-117d8886eab4/6-getting-started-with-ml.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d2ba7e3c-e380-48d0-96a9-117d8886eab4/6-getting-started-with-ml.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d2ba7e3c-e380-48d0-96a9-117d8886eab4/6-getting-started-with-ml.png"
			sizes="100vw"
			alt="observed error"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Observed error. The distance between our observed data and our proposed model. ()
		</figcaption>
	
</figure>


<p>Plugging in <code>ŷ_i</code> from above, we then have the total error in terms of <code>m</code> and <code>b</code>.</p>

<pre><code class="language-javascript">∑(m * x_i + b − y_i)^2
</code></pre>

<p>Finally, we want to minimize this quantity. This yields our <strong>objective function</strong>, abstraction 3 from our list of abstractions above.</p>

<pre><code class="language-javascript">min_{m, b} ∑(m * x_i + b−y_i)^2
</code></pre>

<p>The above states in mathematics that the goal is to minimize the loss by changing values of <code>m</code> and <code>b</code>. The purpose of this section was to motivate fitting a line of best of fit, a special case of <em>least squares</em>. Additionally, we showed examined the <em>least squares objective</em>. Next, we need to solve this objective.</p>

<h4 id="abstraction-4-optimization-algorithm">Abstraction 4: Optimization Algorithm</h4>

<p>How do we minimize this? We take the derivative with respect to <code>m</code>`, set to 0 and solve. After solving, we obtain the analytical solution. Solving for an analytical solution was our <strong>optimization algorithm</strong>, the fourth and final abstraction in our list of abstractions.</p>

<p><strong>Note</strong>: <em>The important portion of this section is to inform you that least squares have a closed form solution, meaning that the optimal solution for our problem can be computed, explicitly. To understand why this is significant, we need to examine a problem without a closed-form solution. For example, we could never solve <code>x=logx</code> for a standard base-10 logarithm. Try graphing these two lines, and we see that they never intersect. In which case, we have no closed-form solution. On the other hand, ordinary least squares have a closed-form &mdash; which is good news. For any problem reduced to least squares, we can then compute the optimal solution, given our data and assumptions.</em></p>

<h3 id="fundamental-topics">Fundamental Topics</h3>

<p>Before studying more methods, it is necessary to understand the undercurrents of machine learning. These will govern the initial study of machine learning:</p>

<h4 id="bias-variance-tradeoffs">Bias-Variance Tradeoffs</h4>

<p>One of machine learning’s most dreaded evils is <em>overfitting</em> in which a model is too closely tailored to the training data. In the limit, the most overfit model will memorize the data. This might mean that if one does well on exam A, one repeats every detail for exam B &mdash; down to the duration of an inter-exam restroom trip and whether or not one used the urinal.</p>

<p>A related but less common evil is <em>underfitting</em>, where the model is not sufficiently expressive to capture important information in the data. This could mean that one looks only at homework scores to predict exam scores, ignoring the effects of reading notes, completing practice exams, and more. Our goal is to build a model that generalizes to new examples while making the appropriate distinctions.</p>

<p>Given these two evils, there are a variety of approaches to fighting both. One is modifying your optimization objective to include a term that penalizes model complexity. Another is tuning <em>hyperparameters</em> that govern either your objective or your algorithm, which may correspond to notions such as “training speed” or “momentum.” The bias-variance tradeoff gives us a precise way of defining and handling both overfitting and underfitting.</p>

<div class="sponsors__wide-place"></div>




<h4 id="maximum-likelihood-estimation-mle-maximum-a-posteriori-map">Maximum Likelihood Estimation (MLE) + Maximum A Posteriori (MAP)</h4>

<p>Say we have ice cream flavors A, B, and C. We observe different recipes. Our goal is to predict which flavor each recipe produces.</p>

<p>One way to predict flavors based on recipes is to first estimate the following probability:</p>

<pre><code class="language-javascript">P(flavor&#124;recipe)
</code></pre>

<p>Given this probability and a new recipe, how can we predict the flavor? Given a recipe, simply consider the probability of each of the flavors A, B, C.</p>

<pre><code class="language-javascript">P(flavor=A&#124;recipe) = 0.4
P(flavor=B&#124;recipe) = 0.5
P(flavor=C&#124;recipe) = 0.1
</code></pre>

<p>Then, pick the flavor that has the highest probability. Above, flavor B has the highest probability, given our recipe. Thus, we predict flavor B. Restating the above rule in mathematics, we have:</p>

<pre class="break-out"><code class="language-javascript">argmax_{flavor} P(flavor&#124;recipe)  # argmax means take the flavor that corresponds to the max value
</code></pre>

<p>However, the only information at our disposal is the reverse: the probability of some recipe given the flavor.</p>

<pre><code class="language-javascript">P(recipe&#124;flavor)
</code></pre>

<p>For Maximum Likelihood Estimates, we make assumptions and find that the two values are proportional.</p>

<pre><code class="language-javascript">P(recipe&#124;flavor) ~ P(flavor&#124;recipe)
</code></pre>

<p>Since we’re only interested in the class with maximum probability <code>P(flavor&#124;recipe)</code>, we can simply find the class with maximum probability, for a proportional value <code>P(recipe&#124;flavor)</code>.</p>

<pre><code class="language-javascript">argmax_{flavor} P(recipe&#124;flavor)
</code></pre>

<p>MLE offers the above objective as one way to predict, using the probability of data given the labels.</p>

<p>However, allow me to convince you that it&rsquo;s reasonable to assume we have <code>(x&#124;y)</code>. We can estimate this from observed, real-world data. For example, say we wish to estimate the number of marbles each student in your class carries, based on the number of rubber ducks the student carries.</p>

<p>Each student&rsquo;s number of rubber ducks is the data <code>x</code>, and the number of marbles she or he has is y. We will use this sample data below.</p>

<pre><code class="language-javascript">&#124; x &#124; y &#124;
&#124;---&#124;---&#124;
&#124; 1 &#124; 2 &#124;
&#124; 1 &#124; 1 &#124;
&#124; 1 &#124; 2 &#124;
&#124; 2 &#124; 1 &#124;
&#124; 2 &#124; 2 &#124;
&#124; 1 &#124; 2 &#124;
</code></pre>

<p>For every <code>y</code>, we can compute the number of <code>x</code>, given us <code>P(x&#124;y)</code>. For the first one, <code>P(x=1&#124;y=1)</code>, consider all of the rows where <code>y=1</code>. There are 2, and only one of them has <code>x=1</code>. Therefore, <code>P(x=1&#124;y=1) = <sup>1</sup>&frasl;<sub>2</sub></code>. We can repeat this for all values of <code>x</code> and <code>y</code>.</p>

<pre><code class="language-javascript">P(x=1&#124;y=1) = 1/2
P(x=2&#124;y=1) = 1/2
P(x=1&#124;y=2) = 3/4
P(x=2&#124;y=2) = 1/4
</code></pre>

<h4 id="featurizations-regularization">Featurizations, Regularization</h4>

<p>Least squares draw lines of best fit for us. Note that least squares can fit the model anytime the model is linear in its inputs <code>x</code> and outputs <code>y</code>.</p>

<p>Say <code>m=1</code>. We have the following equation:</p>

<pre><code class="language-javascript">y = x + b
</code></pre>

<p>However, what if we had data that doesn&rsquo;t generally follow a line? Specifically, consider a set of data sampled along a circle. Recall that the equation for a circle is:</p>

<pre><code class="language-javascript">x^2 + y^2 = r^2
</code></pre>

<p>Can least squares fit this well? As it stands, no. The model is <em>not</em> linear in its inputs <code>x</code> and outputs <code>y</code>. Instead, the model above is <em>quadratic</em> in <code>x</code> and <code>y</code>. However, it turns out that we can use <em>still</em> use least squares, just with a modification. To accomplish this, <strong>we featurize our samples</strong>.</p>

<p>Consider the following: what if the input to our model was <code>x_ = x^2</code> and <code>y_ = y^2</code>? Then, our model is trying to learn the following model.</p>

<pre><code class="language-javascript">x_ + y_ = r^2
</code></pre>

<p>Is this linear in the model&rsquo;s input <code>x_</code> and output <code>y_</code>? Yes. Note the subtlety. The current model is still quadratic in <code>x</code>,<code>y</code> but it is linear in <code>x_</code>,<code>y_</code>. This means that least squares can fit the data if we square <code>x^2</code> and <code>y^2</code> before training least squares.</p>

<p>More generally, we can take any non-linear featurization to apply least squares to labels that are non-linear in the features. This is a fairly powerful tool, known as <em>featurization</em>.</p>

<p>However, featurizations lead to more complex models. Regularization allows us to penalize model complexity, ensuring that we do not overfit the training data.</p>

<h3 id="conclusion">Conclusion</h3>

<p>In this article, you&rsquo;ve touched on major topics in the fundamentals of machine learning. Using the abstractions above, you now have a framework to discuss machine learning problems and solutions. Using the fundamental topics above, you now also have quintessential concepts to learn more about, giving you the necessary tools to evaluate risk and other concerns in a machine learning application.</p>

<h4 id="further-reading">Further Reading</h4>

<p>We will continue to explore these topics in depth, both the undercurrents of machine learning and specific methods. In the interim, here are resources to further your study and exploration of machine learning:</p>

<ul>
<li>“,” Machine Learning course CS189, UC Berkeley</li>
<li> (for efficient linear algebra utilities)</li>
<li> (for out-of-the-box machine learning methods)</li>
</ul>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(ra, il)</span>
</div>


              </article>
            </body>
          </html>
---------------