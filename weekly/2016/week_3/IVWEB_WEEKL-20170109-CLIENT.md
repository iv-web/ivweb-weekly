## 文章索引
1、 <a href="#1文章-基于clang插件的一种ios包大小瘦身方案" >文章： 基于clang插件的一种iOS包大小瘦身方案</a><br/>
2、 <a href="#2视频演讲-浅谈代码复用攻击与防御" >视频演讲： 浅谈代码复用攻击与防御</a><br/>
3、 <a href="#3视频演讲-微服务的集成远远不止一个api" >视频演讲： 微服务的集成，远远不止一个API</a><br/>
4、 <a href="#4文章-科技把我们每个人都变成一个有围墙的花园" >文章： 科技把我们每个人都变成一个有“围墙的花园”</a><br/>
5、 <a href="#5文章-一个遗留系统自动化测试的七年之痒" >文章： 一个遗留系统自动化测试的七年之痒</a><br/><h1 id="#title_0" >1、文章： 基于clang插件的一种iOS包大小瘦身方案</h1>
王康
[http://www.infoq.com/cn/articles/clang-plugin-ios-app-size-reducing?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/clang-plugin-ios-app-size-reducing?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/clang-plugin-ios-app-size-reducing/zh/smallimage/logo2 (10).jpg"/><p>最近公司一款iOS APP(本文只讨论使用Objective C开发的iOS安装包)一直在瘦身，我们团队的APP也愈发庞大了。而要解决这个问题，思路主要集中在两个方向，资源和代码。资源主要在于图片，方法包括移除未被引用的图片，只使用一套图片(2x或3x)，图片伸缩等；代码层面主要思路包括重构消除冗余，linkmap中selector引用分析等。除此之外，有没有别的路径呢？</p> <i>By 王康</i>
---------------
<h1 id="#title_1" >2、视频演讲： 浅谈代码复用攻击与防御</h1>
陈平
[http://www.infoq.com/cn/presentations/attack-and-defense-of-code-reuse?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/attack-and-defense-of-code-reuse?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/attack-and-defense-of-code-reuse/zh/mediumimage/chenping270.jpg"/><p>代码复用攻击是一种利用程序本身代码的攻击方式。与注入式攻击不同，代码复用攻击不需要引入恶意代码。经典的 Return Oriented Programming 属于代码复用攻击范畴，并且被证明是图灵完备的。该攻击可以绕过传统经典的防御方法的 DEP。随着代码复用攻击手法不停演变，ASLR 及其增强对代码复用攻击也束手无策。魔高一尺道高一丈，如何防御代码复用攻击？本课题给出防御方法。</p> <i>By 陈平</i>
---------------
<h1 id="#title_2" >3、视频演讲： 微服务的集成，远远不止一个API</h1>
王延炯
[http://www.infoq.com/cn/presentations/micro-service-integration-far-more-than-one-api?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/micro-service-integration-far-more-than-one-api?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/micro-service-integration-far-more-than-one-api/zh/mediumimage/wangyanjong270.jpg"/><p>「微服务」是一个听上去很美，可以快速拥抱变化的概念。在物理形态上，它从 WAR 向 fatjar 演进；在运行环境上，它从应用服务器 向 docker/rkt 演进。但最终，服务还要与纵向的App / Web 以及横向的Service，以及外围的Partner Serivce 或者IoT Serivce，进行运行时集成，才能体现其价值。微服务间的集成，最简单的是程序员通过一次同步的API调用显式完成，也可以演进为异步事件驱动、观察者模式的松耦合集成。大团队背景下的微服务的集成，「犹如聚沙成搭」，远远不止一个API …</p> <i>By 王延炯</i>
---------------
<h1 id="#title_3" >4、文章： 科技把我们每个人都变成一个有“围墙的花园”</h1>
Todd Hoff
[http://www.infoq.com/cn/articles/technology-turn-us-all-into-a-walled-garden?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/technology-turn-us-all-into-a-walled-garden?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/technology-turn-us-all-into-a-walled-garden/zh/smallimage/logo-ux.jpg"/><p>现在互联网信息系统的构建架构将使我们永远不会看到某些类型的信息，让每个人都生活在由软件算法创建的有“围墙的花园”，例如脸书、谷歌等网站提供的消息都是通过人工智能判断为能给用户和网站同时带来最大利益的信息。</p> <i>By Todd Hoff</i> <i> Translated by 刘志勇</i>
---------------
<h1 id="#title_4" >5、文章： 一个遗留系统自动化测试的七年之痒</h1>
胡志芳
[http://www.infoq.com/cn/articles/automation-test-of-a-seven-year-legacy-system?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/automation-test-of-a-seven-year-legacy-system?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/automation-test-of-a-seven-year-legacy-system/zh/smallimage/logo (22).jpg"/><p>项目从2009年开始启动，采用的是TDD的开发方式。在这之后的过程中，团队做过各种尝试去调整自动化测试的策略去更好的适应不同阶段项目的特征，比如调整不同类型测试的比例，引入新的测试类型等。</p> <i>By 胡志芳</i>
---------------