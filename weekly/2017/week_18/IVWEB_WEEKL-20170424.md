## 文章索引
1、 <a href="#1熵宇宙的终极规则" >熵：宇宙的终极规则</a><br/>
2、 <a href="#2视频演讲-产品思维和设计思维详解" >视频演讲： 产品思维和设计思维详解</a><br/>
3、 <a href="#3文章-深度学习利器-tensorflow系统架构及高性能程序设计" >文章： 深度学习利器： TensorFlow系统架构及高性能程序设计</a><br/>
4、 <a href="#4文章-devops详解" >文章： DevOps详解</a><br/>
5、 <a href="#5视频演讲-基于视频大数据和人工智能的新天网" >视频演讲： 基于视频大数据和人工智能的新天网</a><br/>
6、 <a href="#6android开发周报国内安卓份额飙升至864sdk无埋点技术解析" >Android开发周报：国内安卓份额飙升至86.4%、SDK无埋点技术解析</a><br/><h1 id="#title_0" >1、熵：宇宙的终极规则</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2017/04/entropy.html](http://www.ruanyifeng.com/blog/2017/04/entropy.html)
<p>1、</p>

<p>有人曾经问我："成年后，有没有书籍改变过你的世界观？"</p>

        <p>我想了想，还真有这样的书。那时，我已经工作好几年了，偶然在图书馆翻到一本旧书（上海译文出版社，1987）。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017042401.jpg" alt="" title="" /></p>

<p>那本书是科普著作，介绍物理学概念"熵"。中学毕业后，我再没有碰过物理学，但是没想到读完以后，我看待世界的眼光都变了。</p>

<p>"熵"这个概念非常简单，很容易理解，但又异常强大，可以解释很多事情。这篇文章，我就来谈谈，为什么你应该懂得熵是什么，它可能也会改变你的世界观。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017042402.png" alt="" title="" /></p>

<p>2、</p>

<p>为了理解熵，必须讲一点物理学。</p>

<p>19世纪，物理学家开始认识到，世界的动力是能量，并且提出，即能量的总和是不变的。但是，有一个现象让他们很困惑。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017042403.jpg" alt="" title="" /></p>

<p>（上图中，单摆在两侧的最高点，势能最大，动能为零；在中间的低点，动能最大，势能为零，能量始终守恒。）</p>

<p>物理学家发现，能量无法百分百地转换。比如，蒸汽机使用的是热能，将其转换为推动机器的机械能。这个过程中，总是有一些热能损耗掉，无法完全转变为机械能。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017042404.png" alt="" title="" /></p>

<p>（上图中，能量 E 的转换，总是会导致能量损耗 ∆E。）</p>

<p>一开始，物理学家以为是技术水平不高导致的，但后来发现，技术再进步，也无法将能量损耗降到零。<strong>他们就将那些在能量转换过程中浪费掉的、无法再利用的能量称为熵。</strong></p>

<p>后来，这个概念被总结成了：能量转换总是会产生熵，如果是封闭系统，所有能量最终都会变成熵。</p>

<p>3、</p>

<p>熵既然是能量，为什么无法利用？它又是怎么产生的？为什么所有能量最后都会变成熵？这些问题我想了很久。</p>

<p>物理学家有很多种解释，有一种我觉得最容易懂：能量转换的时候，大部分能量会转换成预先设定的状态，比如热能变成机械能、电能变成光能。但是，就像细胞突变那样，还有一部分能量会生成新的状态。这部分能量就是熵，由于状态不同，所以很难利用，除非外部注入新的能量，专门处理熵。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017042405.jpg" alt="" title="" /></p>

<p>（上图，能量转换过程中，创造出许多新状态。）</p>

<p><strong>总之，能量转换会创造出新的状态，熵就是进入这些状态的能量。</strong></p>

<p>4、</p>

<p>现在请大家思考：状态多意味着什么？</p>

<p>状态多，就是可能性多，表示比较混乱；状态少，就是可能性少，相对来说就比较有秩序。因此，上面结论的另一种表达是：<strong>能量转换会让系统的混乱度增加，熵就是系统的混乱度。</strong></p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017042406.png" alt="" title="" /></p>

<p>（上图中，熵低则混乱度低，熵高则混乱度高。）</p>

<p>转换的能量越大，创造出来的新状态就会越多，因此高能量系统不如低能量系统稳定，因为前者的熵较大。而且，凡是运动的系统都会有能量转换，热力学第二定律就是在说，所有封闭系统最终都会趋向混乱度最大的状态，除非外部注入能量。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017042407.png" alt="" title="" /></p>

<p>（上图中，冰块是分子的有序排列，能量释放后，变成液体水，分子排列变得无序。）</p>

<p>5、</p>

<p>熵让我理解了一件事，<strong>如果不施加外力影响，事物永远向着更混乱的状态发展。</strong>比如，房间如果没人打扫，只会越来越乱，不可能越来越干净。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017042408.jpg" alt="" title="" /></p>

<p>（上图中，如果不花费能量打扫，房间总是越来越乱。）</p>

<p>为什么"世间好物不坚牢，彩云易散琉璃脆"？就是因为事物维持美好的状态是需要能量的，如果没有能量输入，美好的状态就会结束。</p>

<p>这就是我世界观的变化。我从此认识到，人类社会并非一定会变得更进步、更文明。相反地，人类如同宇宙的其他事物一样，常态和最终命运一定是变得更混乱和无序。过去五千年，人类文明的进步只是因为人类学会利用外部能量（牲畜、火种、水力等等）。越来越多的能量注入，使得人类社会向着文明有序的方向发展。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017042409.jpg" alt="" title="" /></p>

<p>（上图中，经过130多亿年的膨胀，宇宙变得越来越无序了。）</p>

<p>6、</p>

<p>工业革命以后，人类社会的进步速度加快了，变得更加先进有序，消耗的能量也指数级地增长：水力不够了用煤炭，煤炭不够了用石油，石油不够了用核能。</p>

<p>能量消耗越大，就会产生越多的熵。因此，人类社会始终处于一种矛盾状态：整个社会变得更加有序和严密的同时，无序和混乱也在暗处不断滋长。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017042410.jpg" alt="" title="" /></p>

<p>我们只是依靠更大的能量输入，在压制熵的累积。不断增加的熵，正在各种方面爆发出来：垃圾污染、地球变暖、土地沙化、PM2.5、物种灭绝......甚至心理疾病、孤独感和疏离感的暴增，我认为都是熵的增加对人类精神造成的结果。</p>

<p>我们需要能量，让世界变得有秩序，但这样是有代价的。<strong>物理学告诉我们，没有办法消除熵和混乱，我们只是让某些局部变得更有秩序，把混乱转移到另一些领域。</strong></p>

<p>7、</p>

<p>人类社会正在加速发展。表面上，我们正在经历一个减熵过程，一切变得越来越有秩序，自动化带来了便捷。但是，能量消耗也在同步放大，为了解决越来越多的熵，我们不得不寻找更多的能量，这又导致熵的进一步增加，从而陷入恶性循环。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017042411.jpg" alt="" title="" /></p>

<p>迄今为止，人类一直能够找到足够的能量，解决熵带来的混乱。但是，这种解决方式正变得捉襟见肘。如果我们继续像现在这样加速发展，那么终有一天会出现能量缺口，地球上的能量不足以解决熵，那时一切就会发生逆转，仿佛细小的裂缝演变成巨大的雪崩，秩序开始崩塌，世界走向混乱。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017042412.jpg" alt="" title="" /></p>

<p>（[说明] 本文出自我正在写的新书《未来世界的幸存者》，点击免费阅读全书。）</p>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2017-04-23T21:23:20+08:00">2017年4月23日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>博客文集：</li>
<li>社交媒体：</li>
<li>Feed订阅： </li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------
<h1 id="#title_1" >2、视频演讲： 产品思维和设计思维详解</h1>
张玉婷
[http://www.infoq.com/cn/presentations/product-thinking-and-design-thinking?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/product-thinking-and-design-thinking?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/product-thinking-and-design-thinking/zh/mediumimage/zhangyuting270.jpg"/><p>在产品团队中，不同角色（产品汪，设计湿，程序猿）对于产品需求的必要性和目的理解经常会不同。通过实际案例，来讲述设计思维和产品思维，例如如何处理大众需求和小众需求，买点和卖点，产品调性的高和低等方面。

本次演讲的主要内容包括：

从设计角度看产品；
从产品角度看设计；
体验设计与产品设计的平衡。</p> <i>By 张玉婷</i>
---------------
<h1 id="#title_2" >3、文章： 深度学习利器： TensorFlow系统架构及高性能程序设计</h1>
武维
[http://www.infoq.com/cn/articles/tensorflow-architecture-and-programming?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/tensorflow-architecture-and-programming?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/tensorflow-architecture-and-programming/zh/smallimage/research_puzzle-nodes-small.jpg"/><p>本文首先回顾了TensorFlow 1.0主要新特性及TensorFlow 2017 Dev Summit的主要议程。并随着TensorFlow新版本的不断发布以及新特性的不断增加，TensorFlow使用更加灵活，运行速度更快，使用方式更产品化，已成为目前主流的深度学习平台之一。 接着介绍了TensorFlow的系统架构，包括Client，Master，Worker，Kernel的相关概念及运行方式，是一种适合大规模分布式训练的机器学习平台。从上述系统架构中可以看到，TensorFlow内核采用C/C++开发，当采用Python API去训练模型的时候，需要不断地用Python调用C/C++底层接口，重复的接口调用一定程度上影响了程序的执行性能。如果有最求高性能运算的朋友，可以尝试用下本文高性能运算章节推荐的方法。</p> <i>By  武维</i>
---------------
<h1 id="#title_3" >4、文章： DevOps详解</h1>
Jerome Kehrli
[http://www.infoq.com/cn/articles/detail-analysis-of-devops?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/detail-analysis-of-devops?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/detail-analysis-of-devops/zh/smallimage/xx_logo.jpg"/><p>DevOps是一种方法论，归纳总结了面临独一无二的机遇和强有力需求的网络巨头们，结合自身业务本质构思出全新工作方式的过程中所采用的实践，而他们的业务需求也很直接：以史无前例的节奏对自己的系统进行演进，有时候可能还需要以天为单位对系统或业务进行扩展。 虽然DevOps对初创公司来说很明显是不可或缺的，但那些有着庞大的老式IT部门的大企业才是能从这些基本原则和实践中获得最大收益的。本文将试图解释得出这个结论的原因和实现方法。</p> <i>By Jerome Kehrli</i> <i> Translated by 大愚若智</i>
---------------
<h1 id="#title_4" >5、视频演讲： 基于视频大数据和人工智能的新天网</h1>
赵勇
[http://www.infoq.com/cn/presentations/network-base-on-video-big-data-and-artificial-intelligence?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/network-base-on-video-big-data-and-artificial-intelligence?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/network-base-on-video-big-data-and-artificial-intelligence/zh/mediumimage/zhaoyong270.jpg"/><p>随着平安城市和智慧城市的建设进入智能阶段，公安、交通等部门对于视图大数据的分析应用产生了强烈需求，他们希望借助大数据分析的能力，进行更快速地案件侦破和更高效的交通管理。格灵深瞳瞄准视图大数据的应用需求，利用海量的数据、先进的深度学习、高性能计算及大数据技术，在产品化的视觉计算处理和数据架构方面进行了相关探索。这次分享将会逐一介绍我们在视图大数据方面所做的一些工作。</p> <i>By 赵勇</i>
---------------
<h1 id="#title_5" >6、Android开发周报：国内安卓份额飙升至86.4%、SDK无埋点技术解析</h1>
郭亮
[http://www.infoq.com/cn/news/2017/04/android-weekly-86-4?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/04/android-weekly-86-4?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>2017年2月全球移动操作系统份额出炉，国内安卓暴涨至86.4%。本期周报为大家带来了Android SDK无埋点技术、OOM分析、Android GC、辅助功能等技术干货，欢迎阅读。</p> <i>By 郭亮</i>
---------------