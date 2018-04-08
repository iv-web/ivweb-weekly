## 文章索引
1、 <a href="#1文章-狼叔node全栈为前端带来更多可能" >文章： 狼叔：Node全栈为前端带来更多可能</a><br/>
2、 <a href="#2彩票的数学知识" >彩票的数学知识</a><br/>
3、 <a href="#3文章-chaos-engineering的历史原则以及实践" >文章： Chaos Engineering的历史、原则以及实践</a><br/>
4、 <a href="#4文章-十年了区块链还能不能好了" >文章： 十年了，区块链还能不能好了？</a><br/>
5、 <a href="#5视频演讲-海量消息的直播互动系统演进历程" >视频演讲： 海量消息的直播互动系统演进历程</a><br/>
6、 <a href="#6视频演讲-知识图谱技术实践上" >视频演讲： 知识图谱技术实践（上）</a><br/><h1 id="#title_0" >1、文章： 狼叔：Node全栈为前端带来更多可能</h1>
覃云
[http://www.infoq.com/cn/articles/node-full-stack-bring-more-possibility?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/node-full-stack-bring-more-possibility?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/node-full-stack-bring-more-possibility/zh/smallimage/logo (10)-1522949029081.jpg"/><p>2009年，Node.js横空出世，在几年时间里，Node.js凭借其高性能、易部署等特点迅速在前端领域脱颖而出，成为大火的明星。但一个技术再好，也是有生命周期的，许多开发者开始质疑，Node.js是不是在走下坡路了？Node.js是不是越来越不吃香了？</p> <i>By 覃云</i>
---------------
<h1 id="#title_1" >2、彩票的数学知识</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2018/04/lottery-mathematics.html](http://www.ruanyifeng.com/blog/2018/04/lottery-mathematics.html)
<p>彩票怎样才能中奖？</p>

        <p>理论上，只能靠运气。但是，如果规则设计得不好，就可以钻漏洞。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2018/bg2018040801.jpg" alt="" title="" /></p>

<p>2005年2月，美国的一个彩票品种，就出现了漏洞，被麻省理工学院的学生发现了。随后的七年，这个学生反复购买这个品种，一共赚到了300万美元。</p>

<p>本文介绍他怎么做的，以及其中的数学原理。我依据的材料，主要来自数学教授 Jordan Ellenberg 在斯坦福大学的一次演讲（）。</p>

<h2>一、期望值</h2>

<p>彩票最重要的数学概念，叫做"期望值"（expected value），即同一种行为多次重复以后，所能得到的平均收益。</p>

<p>举例来说，如果每次抽奖需要2元，假设200次抽奖可以中奖一次，奖金为300元。那么，你花了2000元，一共抽奖1000次，中奖了5次，奖金为1500元。</p>

<p>也就是说，1000次抽奖的总收益是1500元，每次的平均收益是1.5元，这就是期望值。它的计算公式如下。</p>

<blockquote>
  <p>期望值 = 300 * (1 / 200) + 0 * (199 / 200) = 1.5</p>
</blockquote>

<p>期望值是1.5元，但是每次抽奖成本2元，于是净亏损0.5元。</p>

<p>一看就知道，这个事情是不划算的，做得越多，越不划算。偶尔买一次彩票，倒也算了；如果你一天到晚不断买彩票，就肯定会亏很多钱（上例是每200次亏100元）。</p>

<p>总之，期望值是衡量彩票收益的一个关键指标。</p>

<h2>二、马萨诸塞州的 WinFall 彩票</h2>

<p>美国马萨诸塞州有一个彩票品种，叫做 WinFall。它的规则很简单：1到48里面，你猜6个数字，猜中就有奖。</p>

<blockquote>
  <ul>
<li>四等奖（6个猜中2个）：奖金2元</li>
<li>三等奖（6个猜中3个）：奖金5元</li>
<li>二等奖（6个猜中4个）：奖金150元</li>
<li>一等奖（6个猜中5个）：奖金4000元</li>
<li>特等奖（6个猜中6个）：奖金池剩余的全部奖金</li>
</ul>
</blockquote>

<p>有一期，一共卖出了930万张彩票，其中特等奖一个，奖金100万美元，一等奖238个，二等奖11625个，三等奖19.8万个，四等奖136.8万个。</p>

<p>计算可知，这种彩票的期望值是0.798元。</p>

<blockquote>
  <p>期望值 = <br />
　　100万 * ( 1 / 930万) + <br />
　　4000 * ( 238 / 930万) + <br />
　　150 * (11625 / 930万) + <br />
　　5 * (19.8万 / 930万) + <br />
　　2 * (136.8万 / 930万 ) <br />
　　= 0.798</p>
</blockquote>

<p>每张彩票的价格是2元，可是平均收益只有0.798元，连一半都不到，可见这种彩票是非常不划算的。因此没有吸引力，购买这种彩票的民众不断减少。</p>

<p>州政府很着急，因为政府从彩票抽成20%（每张0.4元）。如果销售量减少，政府的收益也会减少。于是，政府为了增加这种彩票的吸引力，决定修改彩票规则。</p>

<h2>三、新规则</h2>

<p>新的规则是，如果当期没有特等奖（没人猜中６个数字），那么奖金会分配给一等奖、二等奖、三等奖的得主，各奖项新的中奖金额如下。</p>

<blockquote>
  <ul>
<li>一等奖（6中5）：50000元</li>
<li>二等奖（6中4）：2385元</li>
<li>三等奖（6中3）：60元</li>
</ul>
</blockquote>

<p>还是使用前面的中奖率，计算期望值。</p>

<blockquote>
  <p>期望值 = <br />
　　50000 * ( 238 / 930万) + <br />
　　2385 * (11625 / 930万) + <br />
　　60 * (19.8万 / 930万) + <br />
　　= 5.53</p>
</blockquote>

<p>每张彩票的价格还是2元，但是期望值变成了5.53元。购买这种彩票就变得非常划算，大量购买的话， 可以得到2.5倍的收益。</p>

<p>麻省理工学院的一个学生，发现了这一点。他凑了5000元购买彩票，结果中了将近15000元！</p>

<h2>四、如何选择号码？</h2>

<p>现在我们知道，新规则的彩票是有利可图的，可以大量购买。但是，还有一个问题，应该怎么选择号码，才能保证收益？也就是说，48个号码里面，你应该选择哪6个号码，才能收益最大化？</p>

<p>毕竟你不能购买所有彩票，因为彩票的收益来自没中奖的那些人。你只能购买一部分彩票，设法使得自己购买的号码有最大的中奖可能。</p>

<p>为了简化思考，让我们考虑一种简单的情况。1到7里面猜三个数字，奖金如下。</p>

<blockquote>
  <ul>
<li>猜中3个：奖金6元</li>
<li>猜中2个：奖金2元</li>
<li>猜中1个：无奖金</li>
</ul>
</blockquote>

<p>你可以同时选择七种组合（即购买七张彩票），请问应该如何选择号码？</p>

<h2>五、组合数公式</h2>

<p>首先，让我们考虑一下，1到7这七个数字里面，三个数字的组合一共有多少种？这在数学里面，叫做。</p>

<blockquote>
  <p>组合数公式是指从 m 个不同元素中，取出 n（n ≤ m）个元素的所有组合的个数，用符号 c(m, n) 表示。</p>
</blockquote>

<p>它的计算公式如下。</p>

<blockquote>
  <p>c(m, n) = m! / n! * (m - n)!</p>
</blockquote>

<p>上面公式中，感叹号表示阶乘，比如<code>4!</code> 等于<code>4 * 3 * 2 * 1</code> 。</p>

<p>按照上面的定义，七个数字里面的三个号码的组合，共有<code>c(7, 3)</code>个。</p>

<blockquote>
  <p>c(7, 3) = 7! / 3! * (7 - 3)! = 35</p>
</blockquote>

<p>这就是说，三个数字的组合共有 35 种。我们可以把它们全部列出来。</p>

<blockquote>
  <p>123 124 125 126 127 <br />
134 135 136 137 <br />
145 146 147 <br />
156 157 <br />
167 <br />
234 235 236 237 <br />
245 246 247 <br />
256 257 <br />
267 <br />
345 346 347 <br />
356 357 <br />
367 <br />
456 457 <br />
467 <br />
567</p>
</blockquote>

<p>上面是所有35种可能的组合，你必须从中选出7种。请问应该选择哪七种？</p>

<h2>六、最佳组合</h2>

<p>答案是下面这七种组合。</p>

<blockquote>
  <p>123 145 167 247 256 346 357</p>
</blockquote>

<p>这七张彩票能让你的收益最大化。因为，不管最后的中奖号码是什么，它们可以保证你总是获得6元奖金。如果中奖号码是123，那么你拿到头奖6元；如果中奖号码是367，那么167、346、357这三张彩票各自猜中两个号码，你中了三个小奖，奖金总额也是6元。</p>

<p>仔细观察这七张彩票，你会发现它们是精心选择的：每个数字都正好出现三次。这导致你要么中一个大奖，要么中三个小奖。</p>

<h2>七、几何选择法</h2>

<p>这七张彩票是怎么选出的呢？</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2018/bg2018040802.gif" alt="" title="" /></p>

<p>有一种几何方法，可以非常简单地做到这一点。七个号码就是七个点，把它们用直线连起来，每根线上只能有三个点，而每个点出现在三根线上。画成上面的形状，就得到了七根线（内部的圆也算一根线）。然后，记录一下每根线上的号码，很简单就选出了七张彩票。</p>

<p>更严谨的证明是这样的：1到7这七个数字，共有21种两个数字的组合（<code>C(7, 2)</code>），这意味着只要把这21种组合都买全了，就可以保证中三个小奖。因为三个中奖号码里面，共有三种两个数字的组合（比如中奖号码是367，那么36、37、67都可以中小奖）。另一方面，由于每张彩票包含三个号码，即包含三种两个数字的组合，那么最少只要买7张彩票就能覆盖全部21种组合。</p>

<h2>八、实际的策略</h2>

<p>回到前面的问题，马萨诸塞州的彩票应该怎么买？</p>

<p>6个号码只要猜中4个，就可以中二等奖，只要把所有四个号码的组合都买了，就可以确保中15个二等奖（6个中奖号码共有15个四个号码的组合<code>C(6, 4)</code>）。</p>

<p>48个号码里面共有194580种四个号码的组合（<code>C(48, 4)</code>），既然一张彩票包含15种组合，那么最少购买12972张彩票就够了（<code>194580 / 15 = 12972</code>），就可以包含所有四个号码的组合。如果有兴趣的话，你可以写一个程序，算出包含这194580种组合的所有彩票。</p>

<p>购买12972张彩票，需要25944元（<code>12972 * 2</code>）。根据前面的奖金额，二等奖的奖金奖金是2385元，那么15个二等奖就是35775元（<code>2385 * 15</code>）。因此，投入25944元，可以无风险地获得35775元。</p>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2018-04-07T23:22:08+08:00">2018年4月 7日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>文集：</li>
<li>社交媒体：</li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------
<h1 id="#title_2" >3、文章： Chaos Engineering的历史、原则以及实践</h1>
Gremlin
[http://www.infoq.com/cn/articles/chaos-engineering-the-history-principles-and-practice?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/chaos-engineering-the-history-principles-and-practice?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/chaos-engineering-the-history-principles-and-practice/zh/smallimage/logo (11)-1522950451895.jpg"/><p>来自Gremlin的工程师介绍了混沌工程的历史、原则和实践。</p> <i>By Gremlin</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_3" >4、文章： 十年了，区块链还能不能好了？</h1>
Kai Stinchcombe
[http://www.infoq.com/cn/articles/ten-years-nobody-has-come-up-with-a-use-case-for-blockchain?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/ten-years-nobody-has-come-up-with-a-use-case-for-blockchain?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/ten-years-nobody-has-come-up-with-a-use-case-for-blockchain/zh/smallimage/api-facades-logo-1522951801403.jpg"/><p>区块链到底解决了什么问题？能解决什么问题？能解决什么问题吗？区块链还有希望吗？Kai Stinchcombe的长文令人深思。 </p> <i>By Kai Stinchcombe</i> <i> Translated by Beining</i>
---------------
<h1 id="#title_4" >5、视频演讲： 海量消息的直播互动系统演进历程</h1>
李淼
[http://www.infoq.com/cn/presentations/evolution-process-of-live-interactive-system-of-mass-message?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/evolution-process-of-live-interactive-system-of-mass-message?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/presentations/evolution-process-of-live-interactive-system-of-mass-message/zh/mediumimage/limiao270-1521960214433.jpg"/><p>随着直播产业的持续升温，国内产生了大量的直播平台。由于直播平台的特点，对礼物、红包等消息可靠性要求更高，同时在热门活动或者网红直播的场景下，几十万人同时在一个直播间内，每秒上千万的互动消息吞吐，逐渐成为了一种常态。这就对直播互动平台在稳定性、伸缩性和吞吐能上的提出更高的要求。
本次讲演主要分享融云直播互动平台如何保证消息可靠性的设计方案，如何应对支撑无上限消息并发的架构演进，以及在不断提高单机吞吐性能的优化历程。
</p> <i>By 李淼</i>
---------------
<h1 id="#title_5" >6、视频演讲： 知识图谱技术实践（上）</h1>
邵蓥侠
[http://www.infoq.com/cn/presentations/the-technology-practice-of-knowledge-map01?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/the-technology-practice-of-knowledge-map01?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/presentations/the-technology-practice-of-knowledge-map01/zh/mediumimage/shaolaoshi01270-1521463452318.jpg"/><p>什么是知识图谱，它与AI是什么关系？知识图谱可以解决哪些行业难题，如何在不同业务中成功落地？本课程将从0到1地详细解答，并通过剖析知识图谱技术在多个领域解决实际问题的不同案例，帮助企业理清落地思路。</p> <i>By 邵蓥侠</i>
---------------