## 文章索引
1、 <a href="#1android-pay-终于退役google-pay-将正式上线" >Android Pay 终于退役，Google Pay 将正式上线</a><br/>
2、 <a href="#2杜绝恶意拍摄android-p-将拒绝后台应用访问相机" >杜绝恶意拍摄，Android P 将拒绝后台应用访问相机</a><br/>
3、 <a href="#3乙站再回应-360-快视频侵权已发律师函要求赔偿道歉" >乙站再回应 360 快视频侵权：已发律师函，要求赔偿道歉</a><br/>
4、 <a href="#4bringing-together-react-d3-and-their-ecosystem" >Bringing Together React, D3, And Their Ecosystem</a><br/>
5、 <a href="#5zabbix-347-发布开源分布式监控解决方案" >Zabbix 3.4.7 发布，开源分布式监控解决方案</a><br/>
6、 <a href="#6spring-integration-502-发布spring-消息通信" >Spring Integration 5.0.2 发布，Spring 消息通信</a><br/>
7、 <a href="#7spring-boot-200-rc2-发布下周发布正式版" >Spring Boot 2.0.0 RC2 发布，下周发布正式版！</a><br/>
8、 <a href="#8hibernate-ogm-530final-发布nosql-持久层框架" >Hibernate OGM 5.3.0.Final 发布，NoSQL 持久层框架</a><br/>
9、 <a href="#9wildfly-1200beta1-发布支持-servlet-40" >WildFly 12.0.0.Beta1 发布，支持 Servlet 4.0</a><br/>
10、 <a href="#10angularjs和angular的路线图" >AngularJS和Angular的路线图</a><br/>
11、 <a href="#11chrome-64-将可移除地址中的跟踪代码谷歌的跟踪除外" >Chrome 64 将可移除地址中的跟踪代码，谷歌的跟踪除外</a><br/>
12、 <a href="#12文章-区块链的价值在于建立信任而ico却在摧毁信任" >文章： 区块链的价值在于建立信任，而ICO却在摧毁信任</a><br/>
13、 <a href="#13文章-批处理etl已经消亡apache-kafka才是数据处理的未来吗" >文章： 批处理ETL已经消亡，Apache Kafka才是数据处理的未来吗？</a><br/>
14、 <a href="#14视频演讲-支撑千万亿级交易额的银行云计算架构演进" >视频演讲： 支撑千万亿级交易额的银行云计算架构演进</a><br/>
15、 <a href="#15视频演讲-腾讯包管理系统演进" >视频演讲： 腾讯包管理系统演进</a><br/>
16、 <a href="#16视频演讲-京东金融移动端多业务集成解决方案" >视频演讲： 京东金融移动端多业务集成解决方案</a><br/>
17、 <a href="#17new-bootstrap-themes" >New Bootstrap themes</a><br/>
18、 <a href="#18java-字节码注入工具-byteman-401-发布" >Java 字节码注入工具 Byteman 4.0.1 发布</a><br/><h1 id="#title_0" >1、Android Pay 终于退役，Google Pay 将正式上线</h1>

[https://www.oschina.net/news/93531/google-play-will-launched](https://www.oschina.net/news/93531/google-play-will-launched)
<p>一月初Google&nbsp;两大电子支付方式 Android Pay 与 Google Wallet 将合并为 Google Pay。Google Pay app 于周二正式上线且可供下载，并开通消费功能。</p><p><img alt="" data-cke-saved-src="https://static.oschina.net/uploads/space/2018/0221/170857_LVBj_3703517.jpg" src="https://static.oschina.net/uploads/space/2018/0221/170857_LVBj_3703517.jpg"/></p><p>Google Pay 目的在取代 Android Pay 及 Google Wallet，用于网络、实体店及所有Google服务消费，及个人间转帐。Google 消费支付产品管理总监 Gerardo Capiel&nbsp;表示，长期而言Google Pay将整合 Google所有产品，使用者所有支付卡资讯都将储存于 Google 帐号内，因而不论以 Google Chrome 在网络购物或声控 Assistant 消费，结帐资讯都是一致的。也正致力于拓展 Google Pay 的线上与实体商店合作伙伴。</p><p>随着Google Pay的上线，Android Pay 将正式退役。不过Google强调原有Android Pay时代的功能，以及累积的银行优惠和安全防护都会保留。</p><p>用于个人转帐的Google Wallet将改名为Google Pay Send并改版上线。未来几个月后，美国、英国的Google Pay用户就可以用它来转帐。</p><p>目前可接受Google Pay的商店包括麦当劳、Dunkin Donuts、Walgreens、Whole Foods等，而整合Google Pay的app包括 Airbnb、Hotel Tonight 及外卖行业 Doordash 等。</p><p>现在Google Pay也极力拓展第三方app及商店。开发人员可通过 Google Pay API 整合电子支付业如Adyen、 Braintree (Native, Web)、EBANX、Paysafe、Stripe、 Vantiv及Worldpay等，后续还会增加其他行业，而商店网站则可通过电商网站平台Shopify和Google Pay整合。</p>
---------------
<h1 id="#title_1" >2、杜绝恶意拍摄，Android P 将拒绝后台应用访问相机</h1>

[https://www.oschina.net/news/93515/android-p-hijacking-camera](https://www.oschina.net/news/93515/android-p-hijacking-camera)
<p>&nbsp;发现的源代码提交，Android P&nbsp;会检测并阻止后台应用访问相机。</p><p>限制是基于应用的用户 ID（UID），Android 将其分配给安装在设备上的每个应用。UID 对于每个应用程序都是唯一的，只要这些应用保留在你的设备上，这些 UID 就不会更改。提交状态表明，Android P 会在 UID “空闲”时进行检测，如果发现一个不活动的 UID 请求摄像头访问，将立即生成一个错误，以防止访问相机。<br/></p><p><img data-cke-saved-src="https://static.oschina.net/uploads/space/2018/0221/074107_F4X7_2896879.png" src="https://static.oschina.net/uploads/space/2018/0221/074107_F4X7_2896879.png" width="1340" height="754"/><br/></p><p>之前的&nbsp;Android 8.0&nbsp;就要求应用在主动使用相机时显示通知。因此，Android P 的摄像头限制可以看作是对现有措施的延伸。该功能对那些在不知情的情况下默默录制视频或拍照的恶意应用有很好的威慑作用。</p>
---------------
<h1 id="#title_2" >3、乙站再回应 360 快视频侵权：已发律师函，要求赔偿道歉</h1>

[https://www.oschina.net/news/93533/b-station-respond-to-360-fast-video-infringement](https://www.oschina.net/news/93533/b-station-respond-to-360-fast-video-infringement)
<p>大过年的360公司也不安分啊，在年初四就被曝出旗下的360快视频大规模盗取其他视频平台版权视频，甚至存在盗取账号数据库情况。不过快视频很快就表示“不，不存在，已经报警处理”，但受影响最大的bilibili哔哩哔哩动画在凌晨再次做出回应，表示快视频的侵权行为是“性质极为恶劣，规模巨大，情节极为严重”，目前已经委托律师事务所发出律师函，替广大视频Up主做主，要求马上停止侵权行为，赔偿损失，赔礼道歉，消除影响。</p><p>事情发酵到这个地步，基本上可以确认360快视频平台上存在大量未经授权转载的视频，虽然快视频表示“这是个别用户的侵权行为”，但快视频作为管理方，拥有不可推卸的审核责任。毕竟中国已经逐步走向尊重数字版权的法制时代，出现如此大规模的盗取视频事件，影响是非常恶劣。</p><p>目前已经有超过100名B站Up主已经授权B站进行维权，而根据不完全统计，被盗取视频的Up主多达千人之多，严重损害了B站用户及B站的合法权益。</p><p><img alt="" data-cke-saved-src="https://static.oschina.net/uploads/space/2018/0221/214517_Yno4_3703517.jpg" src="https://static.oschina.net/uploads/space/2018/0221/214517_Yno4_3703517.jpg"/></p><p>鉴于之前360水滴直播平台的事件以关闭平台而告终，本次侵权事件也是对360公司发力短视频业务的一次重大考验，我们期待360可以正视以及依法处理本次侵权行为。</p><p>来自：</p>
---------------
<h1 id="#title_3" >4、Bringing Together React, D3, And Their Ecosystem</h1>

[https://www.smashingmagazine.com/2018/02/react-d3-ecosystem/](https://www.smashingmagazine.com/2018/02/react-d3-ecosystem/)
Since its creation in 2011, D3.js has become the de facto standard for building complex data visualizations on the web. React is also quickly maturing as the library of choice for creating component-based user interfaces.
Both React and D3 are two excellent tools designed with goals that sometimes collide. Both take control of user interface elements, and they do so in different ways. How can we make them work together while optimizing for their distinct advantages according to your current project?
---------------
<h1 id="#title_4" >5、Zabbix 3.4.7 发布，开源分布式监控解决方案</h1>

[https://www.oschina.net/news/93530/zabbix-3-4-7-released](https://www.oschina.net/news/93530/zabbix-3-4-7-released)
<p>Zabbix 3.4.7 已发布，发布主页显示该版本没有新增的特性和改进，主要是对自 Zabbix 3.4.x 以来已知的 bug 进行了修复。具体如下：</p><ul class=" list-paddingleft-2" style="list-style-type: disc;"><li><p>ZBX-13403 allowed proxy to execute remote commands on agents using encrypted connection</p></li><li><p>ZBX-13441 fixed crashes in case of failures (e.g. timeouts) during VMware hypervisor discovery<br/></p></li><li><p>ZBX-12607 fixed performance of map.get API method and map-related views<br/></p></li><li><p>ZBX-13055 fixed compilation failure in Alpine Linux due to missing res_ninit() function<br/></p></li><li><p>ZBX-13194 fixed incorrect processing of zabbix[wcache,value,*] internal check<br/></p></li><li><p>ZBX-13117 fixed vfs.dir.size with symbol links on Windows</p></li></ul><p>详细内容</p><p>Zabbix 是一个基于 Web 界面的提供分布式系统监视以及网络监视功能的企业级开源解决方案。</p>
---------------
<h1 id="#title_5" >6、Spring Integration 5.0.2 发布，Spring 消息通信</h1>

[https://www.oschina.net/news/93529/spring-integration-5-0-2-released](https://www.oschina.net/news/93529/spring-integration-5-0-2-released)
<p>Spring Integration 5.0 维护版 5.0.2 已发布，可从 Maven Central，JCenter 和还提供了一些错误修复，特别是对于带有收集方法参数的 @ServiceActivator，以及 LockRegistryLeaderInitiator，建议升级。</p><p>该版本还带来了一些新功能：</p><ul class=" list-paddingleft-2" style="list-style-type: disc;"><li><p>Micrometer 已支持收集消息组件指标，要启用，只需在应用程序上下文中声明 MicrometerMetricsFactory bean 以覆盖内置的 metrics factory：</p></li></ul><pre class="brush:java;toolbar: true; auto-links: false;">@Bean
public&nbsp;MicrometerMetricsFactory&nbsp;metricsFactory(MeterRegistry&nbsp;meterRegistry)&nbsp;{
&nbsp;&nbsp;&nbsp;&nbsp;return&nbsp;new&nbsp;MicrometerMetricsFactory(meterRegistry);
}</pre><p>新增的这个功能是希望使这个 MicrometerMetricsFactory 成为下一个 5.1 版本的默认设置。</p><p>值得注意的是，这个版本是最新的 </p>
---------------
<h1 id="#title_6" >7、Spring Boot 2.0.0 RC2 发布，下周发布正式版！</h1>

[https://www.oschina.net/news/93528/spring-boot-2-0-0-rc2-released](https://www.oschina.net/news/93528/spring-boot-2-0-0-rc2-released)
<p>Spring Boot 2.0.0.RC2 。<br/></p><p>感谢所有为 Spring Boot 2.0 做出贡献的人！</p>
---------------
<h1 id="#title_7" >8、Hibernate OGM 5.3.0.Final 发布，NoSQL 持久层框架</h1>

[https://www.oschina.net/news/93527/hibernate-ogm-5-3-final-released](https://www.oschina.net/news/93527/hibernate-ogm-5-3-final-released)
<p></p>
---------------
<h1 id="#title_8" >9、WildFly 12.0.0.Beta1 发布，支持 Servlet 4.0</h1>

[https://www.oschina.net/news/93526/wildfly-12-0-0-beta1-released](https://www.oschina.net/news/93526/wildfly-12-0-0-beta1-released)
<p>WildFly 12.0.0.Beta1 </p>
---------------
<h1 id="#title_9" >10、AngularJS和Angular的路线图</h1>
Abel Avram
[http://www.infoq.com/cn/news/2018/02/roadmap-angular?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/02/roadmap-angular?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>在下一次主要版本发布后，AngularJS即将进入为期三年的LTS（长时间支持版本）。与此同时，Angular仍将保持每六个月发布一次主要版本。</p> <i>By Abel Avram</i> <i> Translated by 刘嘉洋</i>
---------------
<h1 id="#title_10" >11、Chrome 64 将可移除地址中的跟踪代码，谷歌的跟踪除外</h1>

[https://www.oschina.net/news/93532/google-chrome-64-link-trim-feature](https://www.oschina.net/news/93532/google-chrome-64-link-trim-feature)
<p>当你尝试分享一个链接，你经常会发现链接地址中含有长长的跟踪字符串，因此你常常需要在分享链接地址时将某个问号后面的字符串手动删除。现在，Chrome 64 将为用户。当你拷贝网址分享时浏览器会自动移除其中的跟踪代码。然而有人测试发现，这一功能对 Google 自己平台的跟踪代码无效。Google 是最大的网络广告服务商之一，而跟踪对网络广告的定向服务至关重要。</p><p><img alt="" data-cke-saved-src="https://static.oschina.net/uploads/space/2018/0221/220639_9hKF_3703517.jpg" src="https://static.oschina.net/uploads/space/2018/0221/220639_9hKF_3703517.jpg"/></p><p>这只是Chrome 64的更新的其中之一。它最近还推出了自动拦截恶意的功能，这些广告违反了Better Ads标准，还能够整个网站静音以自动播放视频，并为Windows用户提供HDR支持。</p>
---------------
<h1 id="#title_11" >12、文章： 区块链的价值在于建立信任，而ICO却在摧毁信任</h1>
田宁宁
[http://www.infoq.com/cn/articles/ICO-is-destroying-trust-blockchain?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/ICO-is-destroying-trust-blockchain?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/ICO-is-destroying-trust-blockchain/zh/smallimage/logo-small-1517852729089-1519140901003.jpg"/><p>本文根据蚂蚁金服副总裁、技术实验室负责人蒋国飞，在 2 月 9 日 FT 中文网 VIEW FROM THE TOP 沙龙上的首次分享及会后采访整理而成。</p> <i>By 田宁宁</i>
---------------
<h1 id="#title_12" >13、文章： 批处理ETL已经消亡，Apache Kafka才是数据处理的未来吗？</h1>
Daniel Bryant
[http://www.infoq.com/cn/articles/batch-etl-streams-kafka?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/batch-etl-streams-kafka?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/batch-etl-streams-kafka/zh/headerimage/GettyImages-116577526-1516658862634.jpeg"/><p>在QCon旧金山2016会议上，Neha Narkhed做了“ETL已死，而实时流长存”的演讲，并讨论了企业级数据处理领域所面临的挑战。该演讲的核心前提是开源的Apache Kafka流处理平台能够提供灵活且统一的框架，支持数据转换和处理的现代需求。</p> <i>By Daniel Bryant</i> <i> Translated by 张卫滨</i>
---------------
<h1 id="#title_13" >14、视频演讲： 支撑千万亿级交易额的银行云计算架构演进</h1>
龙成
[http://www.infoq.com/cn/presentations/the-evolution-of-bank-cloud-computing-architecture?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/the-evolution-of-bank-cloud-computing-architecture?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/presentations/the-evolution-of-bank-cloud-computing-architecture/zh/mediumimage/longcheng270-1514038419658.jpg"/><p>以可用性为第一目标的金融在线服务在过去的20年内完成了省级集中、大集中、容灾中心、两地三中心、双活数据中心到云的多年发展，在移动互联网和云计算为 IT 基础的今天，银行如何在服务千万亿交易额的业务同时，考虑到成本、快捷和提升用户体验，真正实现可用、易用和好用。
本次演讲内容将由银行数据中心架构到云计算演进的设计建设过程，运行维护和问题的快速发现处理为主线，为大家讲述银行数据中心建设的过去，现在和未来3～5年的预期。</p> <i>By 龙成</i>
---------------
<h1 id="#title_14" >15、视频演讲： 腾讯包管理系统演进</h1>
陈芳录
[http://www.infoq.com/cn/presentations/evolution-of-tencent-package-management-system?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/evolution-of-tencent-package-management-system?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/presentations/evolution-of-tencent-package-management-system/zh/mediumimage/chenfanglu270-1517059444206.jpg"/><p>早在2006年，腾讯SNG运营部就开始设计和实现包系统了，经过10多年不断使用和优化，现在包系统不仅承载了SNG的标准化运维理念，并且被多个BG广泛使用。目前，在包系统上，共托管了3.5W个包，平均每天执行超过5K个发布任务。那么，腾讯的包系统是如何实现的？如何同时支撑业务发布和运维管理？经过哪些功能演化？</p> <i>By 陈芳录</i>
---------------
<h1 id="#title_15" >16、视频演讲： 京东金融移动端多业务集成解决方案</h1>
王秀刚
[http://www.infoq.com/cn/presentations/multi-service-integration-solution-for-jingdong-financial-mobile-terminal?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/multi-service-integration-solution-for-jingdong-financial-mobile-terminal?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/presentations/multi-service-integration-solution-for-jingdong-financial-mobile-terminal/zh/mediumimage/wangxiugang270-1517039156009.jpg"/><p>随着集团业务的不断发展，研发团队规模增大（100多人），App活跃持续增长（月活千万级），客户端单一的工程已经不能够满足当前业务需求。因此，多工程集成的客户端项目应用而生。

工程结构上的拆分（工程组件化），使整个项目层次分明，业务解耦，对研发效率明显提升。在此基础上，京东金融【再组件化平台】的建立，测试和研发人员可以任意快速的搭建自己需要的业务模块工程，进行单元开发和测试，提高研发和测试的团队协作的效率，简化团队协作流程，快速迭代，保证App的整体性能。</p> <i>By 王秀刚</i>
---------------
<h1 id="#title_16" >17、New Bootstrap themes</h1>

[http://blog.getbootstrap.com/2018/02/21/new-bootstrap-themes/](http://blog.getbootstrap.com/2018/02/21/new-bootstrap-themes/)
<div class="embed-responsive embed-responsive-16by9">
  <iframe class="embed-responsive-item" src="https://www.youtube.com/embed/atxUuldUcfI?start=37&amp;rel=0" width="760" height="570" allowfullscreen=""></iframe>
</div>

<p>Just over a month ago, we shipped the long awaited Bootstrap 4 stable release. With a brand new codebase designed to better support customization with all new components and documentation, it was the perfect time to debut some brand new themes built. Today, we’d like to introduce you to our brand new .</p>

<h2 id="10-new-themes">10 new themes</h2>

<p></p>

<p>Over the last several months, we’ve been hard at work with theme creators to build the best themes for you. When we created our original three Bootstrap themes, our goal was to provide the best themes, build tools, documentation, and support to everyone building with Bootstrap. With today’s update, we’re adding 10 new themes to the mix from a global community of designers and developers.</p>

<p>Every theme is built on Bootstrap 4 (stable, no beta or alpha here!) and comes with its own build tools and customer support. Prices are set by creators with pricing that incentivizes unique and well supported themes. Collectively, this inaugural batch of theme developers have built themes used by over 500,000 people. We’re excited to grow our Themes user base, push the boundaries of premium themes, and help everyone bring their ideas to life on the web.</p>

<p></p>

<h2 id="sell-your-themes">Sell your themes</h2>

<p>Our  isn’t just for buying themes. If you’re a theme creator, we’d love to work with you to include your themes or to build new exclusive themes. We’re looking for new creators to design and build high quality themes, provide first class documentation and support, and help create unique experiences built on Bootstrap.</p>

<p>Learn more at .</p>

<p>Happy theming,<br />
</p>
---------------
<h1 id="#title_17" >18、Java 字节码注入工具 Byteman 4.0.1 发布</h1>

[https://www.oschina.net/news/93525/byteman-4-0-1-released](https://www.oschina.net/news/93525/byteman-4-0-1-released)
<p>Byteman 4.0.1 已发布，现已可以从 Byteman&nbsp;</p>
---------------