## 文章索引
1、 <a href="#1api-之下" >API 之下</a><br/>
2、 <a href="#2文章-管理微服务中的数据" >文章： 管理微服务中的数据</a><br/>
3、 <a href="#3文章-ipfs如何冲击我们熟知的网络世界" >文章： IPFS如何冲击我们熟知的网络世界</a><br/>
4、 <a href="#4文章-区块链架构设计建议我们应该用区块链做什么" >文章： 区块链架构设计建议：我们应该用区块链做什么？</a><br/>
5、 <a href="#5文章-如何理解unix里一切都是文件这句话" >文章： 如何理解“Unix里一切都是文件”这句话？</a><br/><h1 id="#title_0" >1、API 之下</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2018/08/api-below.html](http://www.ruanyifeng.com/blog/2018/08/api-below.html)
<p>虽然标题里面有 API，但是本文谈的不是编程，而是更重要的事情。</p>

        <p>很多公司的组织架构，都有一个中层。高层领导和基层员工之间，存在大量的中层干部。公司越大，中层干部越多。</p>

<p>2015年，硅谷创业家（Peter Reinhardt）观察到一个现象：硅谷科技公司正在变得越来越大，但是公司的中层几乎没有变大。原因就在于，大公司正在用 API 替代掉中层干部。</p>

<p>所谓 API，就是软件的接口。通过 API，软件接受外部指令，并且输出结果。莱因哈特发现，高层通过软件，直接给基层下达任务，因此不需要中层了。</p>

<p>举例来说，外卖送餐员就没有领导，他们直接从 API 接受任务，然后把送餐结果回报给 API。不仅是外包员工，现在的趋势是公司内部也采用这种管理方式，将日常管理制度化和标准化，基层员工通过 API 获知并完成公司下达的任务。</p>

<p>阿里和腾讯这样的大型互联网公司，只有几万人，但是他们的营业额和业务范围之大，如果换成传统公司，至少需要几十万人。为什么几万人可以做成几十万人的事情？原因之一就是，阿里和腾讯都有很强大的内部网络，员工的各种需求，不需要找领导，直接到内网查询或填写表单就可以了。传统上，中层干部承担的管理职责，都被内部网络取代了。</p>

<p>这种趋势发展下去，<strong>长期来看，未来只有两种工作：API 之上的工作和 API 之下的工作。</strong> API 之上就是制定 API 规则、给 API 下达指令的人。API 之下就是接受 API 指令进行工作的人。</p>

<p>根据莱因哈特的观点，绘制了一张趋势图。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201808/bg2018081301.jpg" alt="" title="" /></p>

<p>2005年，亚马逊推出 ，允许世界各地的人们到该网站接单，完成任务后领取报酬。这就是第一种 API 之下的工作，此后这类工作不断增加，直到今天。</p>

<p>预计到2020年，人工智能广泛应用以后，API 之下的工作将急剧增加，API 之上的工作将急剧减少，未来的大部分工作岗位都是 API 之下的工作，大部分人都要接受软件的指令工作。同时，由于机器人越来越强大，会抢走一部分工作，以后想找一份 API 之下的工作恐怕也不容易。</p>

<p>很显然，API 之下的工作是比较差的，因为报酬较低、竞争激烈，能不能拿到活、工作业绩的评价都取决于别人，所以远不如 API 之上的工作。而且，API 不会对你进行职业培训，也不会关心你的职业生涯。莱因哈特说："一旦管理层和基层员工之间引入软件层，就没有了明显的向上路径"，基层员工将毫无晋升到管理层的途径。</p>

<p>软件正在变得越来越强大，用途越来越广，那么 API 层将越来越厚。未来的年轻人生活在 API 之下，抬头向上看，只会看到一个无边无际的软件层，根本不知道如何爬到云端，去做那些 API 之上的工作。</p>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2018-08-13T07:33:02+08:00">2018年8月13日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>文集：</li>
<li>社交媒体：</li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------
<h1 id="#title_1" >2、文章： 管理微服务中的数据</h1>
Randy Shoup, Thomas Betts
[http://www.infoq.com/cn/articles/managing-data-microservices?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/managing-data-microservices?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/managing-data-microservices/zh/smallimage/logo-man-1523863324370-1534004693982.jpg"/><p>本文提供了一些如何管理微服务中数据的实际样例，突出强调了如何从单体数据库进行迁移。推荐的做法是首先构建单体的架构，在实际需要微服务的扩展性和其他收益的时候，再迁移至微服务的架构。</p> <i>By Randy Shoup</i> <i> Translated by 张卫滨 </i>
---------------
<h1 id="#title_2" >3、文章： IPFS如何冲击我们熟知的网络世界</h1>
Kaspar Triebstok
[http://www.infoq.com/cn/articles/how-ipfs-is-disrupting-the-web?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/how-ipfs-is-disrupting-the-web?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/how-ipfs-is-disrupting-the-web/zh/smallimage/GettyImages-509049212+copy-1534010586099.jpg"/><p>试想这样一个世界：4k视频流无需缓冲、用户离线不会影响线上工作、商家可以零成本开展电子商务活动、政府无法控制互联网接入。
有哪些因素驱动企业投资相关技术来实现这一愿景？今天我们又能从这一趋势中获得哪些好处？在回答这些问题之前，我们先来看看现在的Web 2.0面临哪些问题。</p> <i>By Kaspar Triebstok</i> <i> Translated by 王强</i>
---------------
<h1 id="#title_3" >4、文章： 区块链架构设计建议：我们应该用区块链做什么？</h1>
付晓岩
[http://www.infoq.com/cn/articles/what-should-we-do-using-blockchain?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/what-should-we-do-using-blockchain?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/what-should-we-do-using-blockchain/zh/smallimage/GettyImages-671039130-1512649078720-1534011417263.jpg"/><p>区块链是一个备受瞩目的话题，随着 ICO、割韭菜等乱象逐渐被识破、被禁止，真正关注其实用价值的“链圈人”越来越多，而从技术角度开始的争议、变革正在让区块链朝着更真实、更有益的方向发展。本文以 Hyperledger Fabric 架构设计为例，先抛开有币的情况，针对联盟链，就“链圈人”一直关注的几个问题进行探讨，提出笔者对区块链应该用来做什么的建议。</p> <i>By 付晓岩</i>
---------------
<h1 id="#title_4" >5、文章： 如何理解“Unix里一切都是文件”这句话？</h1>
PH7
[http://www.infoq.com/cn/articles/in-unix-everything-is-a-file?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/in-unix-everything-is-a-file?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/in-unix-everything-is-a-file/zh/smallimage/logo-ag-1525417039268-1534011141855.jpeg"/><p>UNIX操作系统的设计、用户界面、文化和演变都是建立在它的一套统一的想法和概念上。其中最重要的一点可能是“一切皆文件”，而这个概念被认为是UNIX的灵魂之一。</p> <i>By PH7</i> <i> Translated by 无明</i>
---------------