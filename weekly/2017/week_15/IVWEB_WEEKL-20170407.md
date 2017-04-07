## 文章索引
1、 <a href="#1文章-protobuf-有没有比-json-快-5-倍" >文章： Protobuf 有没有比 JSON 快 5 倍？</a><br/>
2、 <a href="#2第三届360前端星计划在线作业题" >第三届360前端星计划在线作业题</a><br/>
3、 <a href="#3视频演讲-golang+lua-在京东前端业务系统中最佳实践" >视频演讲： Golang+Lua 在京东前端业务系统中最佳实践</a><br/>
4、 <a href="#4文章-一个云管理平台的架构与功能设计经验谈" >文章： 一个云管理平台的架构与功能设计经验谈</a><br/>
5、 <a href="#5文章-深度学习框架2016年的大盘点" >文章： 深度学习框架：2016年的大盘点</a><br/>
6、 <a href="#6视频演讲-人工智能与软件架构" >视频演讲： 人工智能与软件架构</a><br/>
7、 <a href="#7视频演讲-rds重塑之路" >视频演讲： RDS重塑之路</a><br/>
8、 <a href="#8codeplex关闭建议迁移至github" >CodePlex关闭，建议迁移至GitHub</a><br/>
9、 <a href="#9aws-organizations提供基于策略的集中化帐户管理能力" >AWS Organizations提供基于策略的集中化帐户管理能力</a><br/>
10、 <a href="#10tdd会破坏架构吗" >TDD会破坏架构吗？</a><br/>
11、 <a href="#11文章-盘点大数据开源软件google-trends指数" >文章： 盘点大数据开源软件Google Trends指数</a><br/><h1 id="#title_0" >1、文章： Protobuf 有没有比 JSON 快 5 倍？</h1>
陶文
[http://www.infoq.com/cn/articles/json-is-5-times-faster-than-protobuf?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/json-is-5-times-faster-than-protobuf?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/json-is-5-times-faster-than-protobuf/zh/smallimage/fenbushi2_logo.jpg"/><p>拿 JSON 衬托 Protobuf 的文章真的太多了，经常可以看到文章中写道：“快来用 Protobuf 吧，JSON 太慢啦”。但是 Protobuf 真的有吹的那么牛么？我觉得从 JSON 切换到 Protobuf 怎么也得快一倍吧，要不然对不起付出的切换成本。然而，DSL-JSON 的家伙们居然说在Java语言里 JSON 和那些二进制的编解码格式有得一拼（https://blog.dsl-platform.com/improving-java-json-speed/ ），这太让人惊讶了！虽然你可以认为会说，咱们能不用苹果和梨来做比较了么？两个东西根本用途完全不一样好么。咱们用 Protobuf 是冲着跨语言无歧义的 IDL 的去的，才不仅仅是因为性能呢。好吧，这个我同意。但是仍然有那么多人盲目相信，Protobuf 一定会快很多，我觉得还是有必要彻底终结一下这个关于速度的传说。</p> <i>By 陶文</i>
---------------
<h1 id="#title_1" >2、第三届360前端星计划在线作业题</h1>

[https://www.h5jun.com/post/75team-star-handlock.html](https://www.h5jun.com/post/75team-star-handlock.html)
<div class="toc"><ul>
<li><ul>
<li></li>
<li></li>
<li></li>
<li></li>
<li></li>
<li></li>
<li></li>
</ul>
</li>
</ul>
</div><h1>2017 前端星计划选拔作业</h1>
<p>在移动端设备上，“手势密码”成为一个很常用的 UI 组件。</p>
<p>一个手势密码的界面大致如下：</p>
<p><img src="https://p1.ssl.qhimg.com/t01d73f4b567014b497.png" alt=""></p>
<!--more-->
<p>用户用手指按顺序依次划过 9 个原点中的若干个（必须不少于 4 个点），如果划过的点的数量和顺序与之前用户设置的相同，那么当用户的手指离开屏幕时，判定为密码输入正确，否则密码错误。</p>
<p>要求：实现一个移动网页，允许用户设置手势密码和验证手势密码。已设置的密码记录在本地 localStorage 中。</p>
<p>界面原型和操作流程如下：</p>
<h3>stat 1：设置密码</h3>
<p><img src="https://p5.ssl.qhimg.com/t01ad2dbd1fa3195d55.png" alt=""></p>
<p>用户选择设置密码，提示用户输入手势密码</p>
<h3>stat 2：密码长度太短</h3>
<p><img src="https://p3.ssl.qhimg.com/t01e3ccb14544b73cc3.png" alt=""></p>
<p>如果不足 5 个点，提示用户密码太短</p>
<h3>stat 3：再次输入密码</h3>
<p><img src="https://p4.ssl.qhimg.com/t01e29ee99bbe73b256.png" alt=""></p>
<p>提示用户再次输入密码</p>
<h3>stat 4: 两次密码输入不一致</h3>
<p><img src="https://p4.ssl.qhimg.com/t01698b3be9b0d473e7.png" alt=""></p>
<p>如果用户输入的两次密码不一致，<strong>提示并重置，重新开始设置密码</strong></p>
<h3>stat 5: 密码设置成功</h3>
<p><img src="https://p3.ssl.qhimg.com/t01dc54ccf4133d2b06.png" alt=""></p>
<p>如果两次输入一致，<strong>密码设置成功，更新 localStorage</strong></p>
<h3>stat 6: 验证密码 - 不正确</h3>
<p><img src="https://p1.ssl.qhimg.com/t01410791e9c637add0.png" alt=""></p>
<p>切换单选框进入验证密码模式，将用户输入的密码与保存的密码相比较，如果不一致，则提示<strong>输入密码不正确，重置为等待用户输入</strong>。</p>
<h3>stat 7: 验证密码 - 正确</h3>
<p><img src="https://p0.ssl.qhimg.com/t019bf08a6f82f1d289.png" alt=""></p>
<p>如果用户输入的密码与 localStorage 中保存的密码一致，则提示<strong>密码正确</strong>。</p>
<hr>
<p>请同学们按照上面的需求实现这个网页，在手机上可用。可以不用太考虑古老机器的兼容性，最新的 android 和 iPhone 可用即可。</p>
<p><strong>要求：</strong> </p>
<ol>
<li><p>独立思考，独立完成，严禁抄袭！如果发现抄袭导致代码雷同，抄袭者和被抄袭者将都不会入选，而且会取消以后参加 360 面试的资格。</p>
</li>
<li><p>注意保持良好代码风格和注释，可以在 README 文档里写上自己的思路。</p>
</li>
<li><p>请在截止日期内完成并提交。 </p>
</li>
</ol>
---------------
<h1 id="#title_2" >3、视频演讲： Golang+Lua 在京东前端业务系统中最佳实践</h1>
谢刚
[http://www.infoq.com/cn/presentations/golang-lua-in-Jingdong-front-end-business-system?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/golang-lua-in-Jingdong-front-end-business-system?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/golang-lua-in-Jingdong-front-end-business-system/zh/mediumimage/xiegang270.jpg"/><p>京东分类列表，是用户访问京东的入口之一，每天上亿的访问量。分类列表采用 Golang+Lua 的全新架构，保证分类列表的稳定&快速响应。

本次分享包括以下几点：

分类列表的架构；
Golang 在分类列表中的检索应用；
Lua 在页面模板渲染使用；
在使用 Golang 和 Lua 中遇到的坑。</p> <i>By 谢刚</i>
---------------
<h1 id="#title_3" >4、文章： 一个云管理平台的架构与功能设计经验谈</h1>
牛继宾
[http://www.infoq.com/cn/articles/cloud-manage-platform-arch-and-function?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/cloud-manage-platform-arch-and-function?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/cloud-manage-platform-arch-and-function/zh/smallimage/zhenghe_logo.jpg"/><p>云计算最终的目标是提供服务，将资源进行管理并变现为服务，进而支撑应用。本次内容主要介绍云管理平台的架构与功能设计，通过演讲者在云计算行业的多年实践，从需求、实践、应用支撑等角度对云管理平台的功能规划、架构设计、微服务化改造等进行全面阐述。</p> <i>By 牛继宾</i>
---------------
<h1 id="#title_4" >5、文章： 深度学习框架：2016年的大盘点</h1>
刘志勇
[http://www.infoq.com/cn/articles/2016-deep-learning-framework?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/2016-deep-learning-framework?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/2016-deep-learning-framework/zh/smallimage/logo (11).jpg"/><p>刚刚过去的2016年，回顾这一年，深度学习无疑是2016年最热的词。包括Google、Amazon、Facebook、Microsoft等各大巨头都在不遗余力地推进深度学习的研发和应用。 与BEEVA Labs数据分析师Ricardo Guerrero Gomez-Ol在他的博客上发表了一篇博文，盘点了目前最流行的深度学习框架。他在博文中表示，他写此文的初衷是，他常常听到人们谈论深度学习时，总是问：“我应该从哪里开始呢？”“我听说TensorFlow是最流行的，对吧？”“Caffe很常用，但是我觉得它学起来有点困难。” 因为Ricardo所在的BEEVA实验室，经常和深度学习的许多苦打交道，所以他想分享有趣的发现和感想，帮助那些刚进入深度学习这一迷人世界的人们。 InfoQ整理、结合了Ricardo关于深度学习框架的盘点，写成此文，以飨广大有志于深度学习领域的读者们。</p> <i>By 刘志勇</i>
---------------
<h1 id="#title_5" >6、视频演讲： 人工智能与软件架构</h1>
黄柳青
[http://www.infoq.com/cn/presentations/artificial-intelligence-and-software-architecture?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/artificial-intelligence-and-software-architecture?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/artificial-intelligence-and-software-architecture/zh/mediumimage/huangliuqing270.jpg"/><p>人工智能走向应用，它将怎样改变人机交互模式，从而引发软件架构的崩溃和重造？</p> <i>By 黄柳青</i>
---------------
<h1 id="#title_6" >7、视频演讲： RDS重塑之路</h1>
林足雄
[http://www.infoq.com/cn/presentations/the-road-of-rds-reconstruction?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/the-road-of-rds-reconstruction?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/the-road-of-rds-reconstruction/zh/mediumimage/linzuixiong270.jpg"/><p>在电商大量用户的背景下，产生海量的数据，强依赖于MySQL，如何更好地满足业务上的容量和性能要求。在创业团队的初创阶段到蓬勃发展的团队扩张期，如何更好地组织MySQL的使用来提高研发流程更好地保障业务线质量。</p> <i>By 林足雄</i>
---------------
<h1 id="#title_7" >8、CodePlex关闭，建议迁移至GitHub</h1>
Abel Avram
[http://www.infoq.com/cn/news/2017/04/codeplex-github?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/04/codeplex-github?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Microsoft决定停止提供CodePlex开源项目免费托管服务。他们建议开发人员可以迁移到GitHub或任何其他托管服务提供商。</p> <i>By Abel Avram</i> <i> Translated by 刘嘉洋</i>
---------------
<h1 id="#title_8" >9、AWS Organizations提供基于策略的集中化帐户管理能力</h1>
Steffen Opel
[http://www.infoq.com/cn/news/2017/04/aws-organizations?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/04/aws-organizations?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>自从re:Invent 2016大会发布预览版三个月后，Amazon Web Services最近正式发布了AWS Organizations。这个新服务可在由组织单位组成的层次结构中集中管理多个AWS帐户，并能通过细化的访问权限应用服务控制策略。AWS Organizations还取代了以往单独汇总的计费功能。</p> <i>By Steffen Opel</i> <i> Translated by 大愚若智</i>
---------------
<h1 id="#title_9" >10、TDD会破坏架构吗？</h1>
Andrew Morgan
[http://www.infoq.com/cn/news/2017/04/does-tdd-harm-architecture?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/04/does-tdd-harm-architecture?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>作为敏捷宣言的共同作者，我们熟知的鲍勃大叔Bob Martin，最近发表了一篇文章，对TDD是否会损害架构进行了评估。文中大部分讨论围绕着遵循测试驱动方法对高层设计和实现代码的总体可维护性是否会产生消极影响。</p> <i>By Andrew Morgan</i> <i> Translated by 汪佳南</i>
---------------
<h1 id="#title_10" >11、文章： 盘点大数据开源软件Google Trends指数</h1>
杨雷
[http://www.infoq.com/cn/articles/big-data-open-source-software-google-trends-index?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/big-data-open-source-software-google-trends-index?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/big-data-open-source-software-google-trends-index/zh/smallimage/clou_logo.jpg"/><p>本文列举了大数据相关的部分热门项目，盘点了该生态圈目前流行的一些开源产品和工具，并用google热度趋势图体现了它们的受关注程度。从不同的热度趋势，可以了解到每一个产品在近5年来全球受关注的走势，是越来越受重视还是渐渐淡出。</p> <i>By 杨雷</i>
---------------