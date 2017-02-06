## 文章索引
1、 <a href="#1视频演讲-比-buck-更快蚂蚁聚宝-android-秒级编译方案-freeline" >视频演讲： 比 Buck 更快——蚂蚁聚宝 Android 秒级编译方案 Freeline</a><br/>
2、 <a href="#2文章-2016机器学习大盘点第3篇" >文章： 2016机器学习大盘点（第3篇）</a><br/>
3、 <a href="#3文章-书评实战apache-jmeter" >文章： 书评：实战Apache JMeter</a><br/>
4、 <a href="#4文章-处理分布式团队间的文化差异" >文章： 处理分布式团队间的文化差异</a><br/><h1 id="#title_0" >1、视频演讲： 比 Buck 更快——蚂蚁聚宝 Android 秒级编译方案 Freeline</h1>
何嘉文（弦影）
[http://www.infoq.com/cn/presentations/android-second-compilation-scheme-freeline?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/android-second-compilation-scheme-freeline?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/android-second-compilation-scheme-freeline/zh/mediumimage/hejiawen270.jpg"/><p>Freeline 是蚂蚁聚宝团队 15 年 10 月在 Android 平台上的量身定做的一个基于动态替换的编译方案，5 月阿里集团内部开源，稳定性方面：完善的基线对齐，进程级别异常隔离机制。性能方面：内部采用了类似 Facebook 的开源工具 buck 的多工程多任务并发思想：端口扫描，代码扫描，并发编译，并发 dx，并发 merge dex 等策略，在多核机器上有明显加速效果，另外在 class 及 dex、resources 层面作了相应缓存策略，做到真正增量开发，另外引入并优化 buck 的部分加速组件 dx，DexMerger，资源编译方面，深入改造了 Aapt 资源编译流程，当资源发生改变时候，秒级完成增量包编译，其中增量包仅含最小的变更集合，后期也被运用到线上进行资源/代码动态替换。相比目前 instant-run、buck、layoutcast 等方案快数倍速度。</p> <i>By 何嘉文（弦影）</i>
---------------
<h1 id="#title_1" >2、文章： 2016机器学习大盘点（第3篇）</h1>
Thomas W. Dinsmore
[http://www.infoq.com/cn/articles/2016-machine-learning-market-part03?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/2016-machine-learning-market-part03?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/2016-machine-learning-market-part03/zh/smallimage/fire_logo.jpg"/><p>作为这一系列文章的第三篇，本文将介绍大型科技公司2016年在机器学习和深度学习领域的举措。</p> <i>By Thomas W. Dinsmore</i> <i> Translated by 大愚若智</i>
---------------
<h1 id="#title_2" >3、文章： 书评：实战Apache JMeter</h1>
Victor Grazi
[http://www.infoq.com/cn/articles/jmeter-by-example-book-review?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/jmeter-by-example-book-review?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/jmeter-by-example-book-review/zh/smallimage/logo.jpg"/><p>JMeter已经成为负载测试方面不可或缺的测试工具，它为那些包含Web前端、JVM服务器和一堆NoSQL或关系型数据库的多层架构应用程序提供了很多功能。这本书作为学习指南可以帮助读者克服JMeter的学习曲线。</p> <i>By Victor Grazi</i> <i> Translated by 薛命灯</i>
---------------
<h1 id="#title_3" >4、文章： 处理分布式团队间的文化差异</h1>
Hugo Messer, Savita Pahuja
[http://www.infoq.com/cn/articles/culture-distributed-team?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/culture-distributed-team?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/culture-distributed-team/zh/headerimage/GettyImages-489084228.jpg"/><p>分布式团队如今已经成为许多组织的标准形态。公司是国际化的，沟通技术使人们不必待在同地“办公室”中，许多新的工作环境可以是“游牧式”的。在分布式团队中，成为高效的团队是有可能的，但必须要多花些精力去克服距离所产生的固有挑战。</p> <i>By Hugo Messer</i> <i> Translated by 冬雨</i>
---------------