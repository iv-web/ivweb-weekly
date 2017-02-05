## 文章索引
1、 <a href="#1walmartlabs使用react-native的体验" >WalmartLabs使用React Native的体验</a><br/>
2、 <a href="#2编写良好的单元测试" >编写良好的单元测试</a><br/>
3、 <a href="#3apache-eagle毕业成为顶级项目" >Apache Eagle毕业成为顶级项目</a><br/>
4、 <a href="#4docker-113-版增强了cli-针对swarm-mode的compose-file支持及secrets-api" >Docker 1.13 版增强了CLI、 针对Swarm Mode的Compose-File支持及Secrets API</a><br/>
5、 <a href="#5第三方工具对性能和文化的危害以及规避" >第三方工具对性能和文化的危害以及规避</a><br/>
6、 <a href="#6openapi规范30版接近最终发布" >OpenAPI规范3.0版接近最终发布</a><br/>
7、 <a href="#7intel开源深度学习库bigdlnon-gpu-on-spark" >Intel开源深度学习库BigDL：Non GPU on Spark</a><br/>
8、 <a href="#8oracle进击云计算搅局者or生力军" >Oracle进击云计算，搅局者or生力军?</a><br/>
9、 <a href="#9深度学习框架-mxnet-成为-apache-孵化器项目" >深度学习框架 MXNet 成为 Apache 孵化器项目</a><br/>
10、 <a href="#10文章-raft-一致性算法论文译文" >文章： Raft 一致性算法论文译文</a><br/>
11、 <a href="#11gitlab事故之技术详叙抢救后恢复在线已确定下一步计划" >GitLab事故之技术详叙：抢救后恢复在线，已确定下一步计划</a><br/><h1 id="#title_0" >1、WalmartLabs使用React Native的体验</h1>
刘志勇
[http://www.infoq.com/cn/news/2017/02/WalmartLabs-React-Native?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/02/WalmartLabs-React-Native?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>React Native是Facebook于2015年开源的跨平台移动应用开发框架，是Facebook早先开源的UI框架React在原生移动应用平台的衍生产物，目前支持iOS和Android两大平台。React Native使用Javascript语言，类似于HTML的JSX，以及CSS来开发移动应用，因此熟悉Web前端开发的技术人员只需很少的学习就可以进入移动应用开发领域。 React Native运行时包含一个原生主线程和一个JS线程，JS线程执行JS代码，负责界面布局和业务逻辑处理，原生线程负责界面渲染和原生功能执行。不久前，WalmartLabs的React Native团队成员Matt Bresnan、M.K.Safi、Sanket Patel和Keerti合著了一篇文章，为我们分享了WalmartLabs使用React Native的体验。</p> <i>By 刘志勇</i>
---------------
<h1 id="#title_1" >2、编写良好的单元测试</h1>
Ben Linders
[http://www.infoq.com/cn/news/2017/02/writing-good-unit-tests?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/02/writing-good-unit-tests?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>尽量保持较小的单元测试规模，使用恰当的工具，将程序员和测试人员配对；这是编写良好的单元测试的一些建议。单元测试混合了编程和测试；程序员和测试人员要一起工作，互相学习，拓展自己的知识面。</p> <i>By Ben Linders</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_2" >3、Apache Eagle毕业成为顶级项目</h1>
Alexandre Rodrigues
[http://www.infoq.com/cn/news/2017/02/apache-eagle-graduates-top-level?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/02/apache-eagle-graduates-top-level?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Apache Eagle是一个识别大数据平台上的安全和性能问题的开源解决方案，2017年1月10日，Apache Eagle毕业成为Apache顶级项目。Eagle首先由eBay在2015年10月开源，它主要用来即时监测敏感数据访问和恶意活动，并及时采取行动。</p> <i>By Alexandre Rodrigues</i> <i> Translated by 尚剑</i>
---------------
<h1 id="#title_3" >4、Docker 1.13 版增强了CLI、 针对Swarm Mode的Compose-File支持及Secrets API</h1>
Daniel Bryant
[http://www.infoq.com/cn/news/2017/02/docker-1.13?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/02/docker-1.13?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Docker股份有限公司已经发布了开源Docker容器引擎项目的1.13版。这个版本包括对Docker CLI的重大重新调整，引入了回收再利用磁盘空间的‘clean-up’命令，以及几个实验性特性，比如镜像层压缩和改进了日志的Prometheus-style端点。伴随Docker 1.13版的发行，还有支持工具链的新版本，包括：Docker Compose 1.10、Docker Machine 0.9.0和Notary 0.4.3。</p> <i>By Daniel Bryant</i> <i> Translated by 冬雨</i>
---------------
<h1 id="#title_4" >5、第三方工具对性能和文化的危害以及规避</h1>
Manuel Pais
[http://www.infoq.com/cn/news/2017/02/3rd-party-governance-Adidas?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/02/3rd-party-governance-Adidas?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>大型鞋服类制造商的IT如何驯服他们国际网站上第三方工具失控的扩散，避免影响性能。此外，这还导致业务和IT之间互相指责的文化环境。专注于性能数据和用户体验验证的新的第三方管理过程是止血的关键。</p> <i>By Manuel Pais</i> <i> Translated by 冬雨</i>
---------------
<h1 id="#title_5" >6、OpenAPI规范3.0版接近最终发布</h1>
Abel Avram
[http://www.infoq.com/cn/news/2017/02/openapi-3?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/02/openapi-3?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>“开放API战略”(Open API Initiativev) 发布了OpenAPI规范3.0版的预览，其中给出了一些重大改进。</p> <i>By Abel Avram</i> <i> Translated by Rays</i>
---------------
<h1 id="#title_6" >7、Intel开源深度学习库BigDL：Non GPU on Spark</h1>
杜小芳
[http://www.infoq.com/cn/news/2017/02/Intel-BigDL-Non-GPU-on-Spark?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/02/Intel-BigDL-Non-GPU-on-Spark?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Intel开源了基于Apache Spark的分布式深度学习框架BigDL。BigDL借助现有的Spark集群来运行深度学习计算，并简化存储在Hadoop中的大数据集的数据加载。 对于直接支持已有Spark集群的深度学习开源库，BigDL是唯一的一个框架。</p> <i>By 杜小芳</i>
---------------
<h1 id="#title_7" >8、Oracle进击云计算，搅局者or生力军?</h1>
朱昊冰
[http://www.infoq.com/cn/news/2017/02/Oracle-cloud-number?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/02/Oracle-cloud-number?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>据来自Synergy研究集团2016全球云计算运营商市场份额第三季度数据显示，亚马逊网络服务（AWS）拥有全球公共IaaS的45％份额，是微软、谷歌和IBM市场总和的两倍之多。AWS还在平台即服务（PaaS）市场中处于领先地位，但Synergy发现其市场幅度较窄，不过仍然领先于Salesforce。在托管私有云上，IBM位居市场第一名，其次是Amazon，Rackspace和澳大利亚公司NTT。总的来说，全球四大云提供商——亚马逊、微软、IBM和谷歌继续控制着超过一半的全球云市场，市场份额也继续保持增长。</p> <i>By 朱昊冰</i>
---------------
<h1 id="#title_8" >9、深度学习框架 MXNet 成为 Apache 孵化器项目</h1>
尚剑
[http://www.infoq.com/cn/news/2017/02/deep-study-MXNet-Apache?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/02/deep-study-MXNet-Apache?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>MXNet是一个轻量级、可移植、灵活的分布式深度学习框架，2017年1月23日，该项目进入Apache基金会，成为Apache的孵化器项目。</p> <i>By  尚剑</i>
---------------
<h1 id="#title_9" >10、文章： Raft 一致性算法论文译文</h1>
罗远航
[http://www.infoq.com/cn/articles/raft-paper?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/raft-paper?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/raft-paper/zh/headerimage/logo.jpg"/><p>Raft 是一种用来管理日志复制的一致性算法。它和 Paxos 的性能和功能是一样的，但是它和 Paxos 的结构不一样；这使得 Raft 更容易理解并且更易于建立实际的系统。为了提高理解性，Raft 将一致性算法分为了几个部分，例如领导选取（leader selection），日志复制（log replication）和安全性（safety），同时它使用了更强的一致性来减少了必须需要考虑的状态。从用户学习的结果来看，Raft 比 Paxos 更容易学会。Raft 还包括了一种新的机制来使得动态改变集群成员，它使用重叠大多数（overlapping majorities）来保证安全。

</p> <i>By 罗远航</i>
---------------
<h1 id="#title_10" >11、GitLab事故之技术详叙：抢救后恢复在线，已确定下一步计划</h1>
周明耀
[http://www.infoq.com/cn/news/2017/02/Technical-details-accident-GitLa?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/02/Technical-details-accident-GitLa?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>2017年1月31日太平洋时间晚上，GitLab通过推特发文承认300GB生产环境数据因为UNIX SA的误操作，已经被彻底删除（后发文补充说明已经挽回部分数据），引起业界一片哗然。本文对GitLab做了初步介绍，并继续追踪GitLab在2月1日发布的申明，弄清楚事故发生时的各种问题根本原因。最后摘录了一些网友的跟帖，大多数人都对GitLab表达了自己的支持和宽容。</p> <i>By 周明耀</i>
---------------