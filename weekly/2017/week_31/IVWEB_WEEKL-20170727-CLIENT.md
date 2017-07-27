## 文章索引
1、 <a href="#1前端每周清单第-23-期react-内部原理与实现自定义基于-javascript-的-16-位虚拟机使用-apollo-server-快速搭建-graphql-服务端" >前端每周清单第 23 期：React 内部原理与实现，自定义基于 JavaScript 的 16 位虚拟机，使用 Apollo Server 快速搭建 GraphQL 服务端</a><br/>
2、 <a href="#2视频演讲-探究-nodejs-的服务端之路" >视频演讲： 探究 Node.js 的服务端之路</a><br/>
3、 <a href="#3error-handling-in-react-16" >Error Handling in React 16</a><br/>
4、 <a href="#4穷忙的人生" >穷忙的人生</a><br/>
5、 <a href="#5文章-终极反馈环从客户上报的缺陷中学习" >文章： 终极反馈环：从客户上报的缺陷中学习</a><br/>
6、 <a href="#6文章-同程旅游实时计算的演进" >文章： 同程旅游实时计算的演进</a><br/>
7、 <a href="#7王者荣耀的推送是如何做的腾讯信鸽精准推送系统解析" >王者荣耀的推送是如何做的？腾讯信鸽精准推送系统解析</a><br/>
8、 <a href="#8事件溯源系统中事件的版本化" >事件溯源系统中事件的版本化</a><br/><h1 id="#title_0" >1、前端每周清单第 23 期：React 内部原理与实现，自定义基于 JavaScript 的 16 位虚拟机，使用 Apollo Server 快速搭建 GraphQL 服务端</h1>
王下邀月熊
[http://www.infoq.com/cn/news/2017/07/arch-weekly-23?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/07/arch-weekly-23?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>前端每周清单第 23 期：React 内部原理与实现，自定义基于 JavaScript 的 16 位虚拟机，使用 Apollo Server 快速搭建 GraphQL 服务端</p> <i>By 王下邀月熊</i>
---------------
<h1 id="#title_1" >2、视频演讲： 探究 Node.js 的服务端之路</h1>
黄鼎恒
[http://www.infoq.com/cn/presentations/explore-the-node.js-server-side-of-the-road?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/explore-the-node.js-server-side-of-the-road?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/explore-the-node.js-server-side-of-the-road/zh/mediumimage/huangdingheng270.jpg"/><p>在 Node.js 日趋流行的情况下，有不少不同的声音，诚然在将 JavaScript 通过 v8 引入服务端是一个创造性的想法，但是随着人们的使用也渐渐暴露了越来越多的问题。
本次分享我将结合饿了么在 Node.js 方面的项目实践，与大家谈论从前端转向服务端程序的各项要素，并讲述 v8 引擎的内存结构，内存释放以及内存泄漏的各项情况。并讨论将 Node.js 引入服务端带来的优势与常见的问题及其解决方案，以及目前 Node.js 的意义。</p> <i>By 黄鼎恒</i>
---------------
<h1 id="#title_2" >3、Error Handling in React 16</h1>

[https://facebook.github.io/react/blog/2017/07/26/error-handling-in-react-16.html](https://facebook.github.io/react/blog/2017/07/26/error-handling-in-react-16.html)
<p>As React 16 release is getting closer, we would like to announce a few changes to how React handles JavaScript errors inside components. These changes are included in React 16 beta versions, and will be a part of React 16.</p>

<p><strong>By the way, </strong></p>

<h2>Behavior in React 15 and Earlier</h2>

<p>In the past, JavaScript errors inside components used to corrupt React’s internal state and cause it to  on next renders. These errors were always caused by an earlier error in the application code, but React did not provide a way to handle them gracefully in components, and could not recover from them.</p>

<h2>Introducing Error Boundaries</h2>

<p>A JavaScript error in a part of the UI shouldn’t break the whole app. To solve this problem for React users, React 16 introduces a new concept of an “error boundary”.</p>

<p>Error boundaries are React components that <strong>catch JavaScript errors in their children (and grandchildren), log those errors, and display a fallback UI</strong> instead of the component tree that crashed. Error boundaries catch errors during rendering, in lifecycle methods, and in constructors of the whole tree below them.</p>

<p>A class component becomes an error boundary if it defines a new lifecycle method called <code>componentDidCatch(error, info)</code>:</p>
<div class="highlight"><pre><code class="language-js" data-lang="js"><span class="kr">class</span> <span class="nx">ErrorBoundary</span> <span class="kr">extends</span> <span class="nx">React</span><span class="p">.</span><span class="nx">Component</span> <span class="p">{</span>
  <span class="nx">constructor</span><span class="p">(</span><span class="nx">props</span><span class="p">)</span> <span class="p">{</span>
    <span class="kr">super</span><span class="p">(</span><span class="nx">props</span><span class="p">);</span>
    <span class="k">this</span><span class="p">.</span><span class="nx">state</span> <span class="o">=</span> <span class="p">{</span> <span class="nx">hasError</span><span class="o">:</span> <span class="kc">false</span> <span class="p">};</span>
  <span class="p">}</span>

<span class="hll">  <span class="nx">componentDidCatch</span><span class="p">(</span><span class="nx">error</span><span class="p">,</span> <span class="nx">info</span><span class="p">)</span> <span class="p">{</span>
</span><span class="hll">    <span class="c1">// Display fallback UI</span>
</span><span class="hll">    <span class="k">this</span><span class="p">.</span><span class="nx">setState</span><span class="p">({</span> <span class="nx">hasError</span><span class="o">:</span> <span class="kc">true</span> <span class="p">});</span>
</span><span class="hll">    <span class="c1">// You can also log the error to an error reporting service</span>
</span><span class="hll">    <span class="nx">logErrorToMyService</span><span class="p">(</span><span class="nx">error</span><span class="p">,</span> <span class="nx">info</span><span class="p">);</span>
</span><span class="hll">  <span class="p">}</span>
</span>
  <span class="nx">render</span><span class="p">()</span> <span class="p">{</span>
<span class="hll">    <span class="k">if</span> <span class="p">(</span><span class="k">this</span><span class="p">.</span><span class="nx">state</span><span class="p">.</span><span class="nx">hasError</span><span class="p">)</span> <span class="p">{</span>
</span><span class="hll">      <span class="c1">// You can render any custom fallback UI</span>
</span><span class="hll">      <span class="k">return</span> <span class="o">&lt;</span><span class="nx">h1</span><span class="o">&gt;</span><span class="nx">Something</span> <span class="nx">went</span> <span class="nx">wrong</span><span class="p">.</span><span class="o">&lt;</span><span class="err">/h1&gt;;</span>
</span><span class="hll">    <span class="p">}</span>
</span>    <span class="k">return</span> <span class="k">this</span><span class="p">.</span><span class="nx">props</span><span class="p">.</span><span class="nx">children</span><span class="p">;</span>
  <span class="p">}</span>
<span class="p">}</span>
</code></pre></div>
<p>Then you can use it as a regular component:</p>
<div class="highlight"><pre><code class="language-js" data-lang="js"><span class="o">&lt;</span><span class="nx">ErrorBoundary</span><span class="o">&gt;</span>
  <span class="o">&lt;</span><span class="nx">MyWidget</span> <span class="o">/&gt;</span>
<span class="o">&lt;</span><span class="err">/ErrorBoundary&gt;</span>
</code></pre></div>
<p>The <code>componentDidCatch()</code> method works like a JavaScript <code>catch {}</code> block, but for components. Only class components can be error boundaries. In practice, most of the time you’ll want to declare an error boundary component once and use it throughout your application.</p>

<p>Note that <strong>error boundaries only catch errors in the components below them in the tree</strong>. An error boundary can’t catch an error within itself. If an error boundary fails trying to render the error message, the error will propagate to the closest error boundary above it. This, too, is similar to how <code>catch {}</code> block works in JavaScript.</p>

<h2>Live Demo</h2>

<p>Check out .</p>

<h2>Where to Place Error Boundaries</h2>

<p>The granularity of error boundaries is up to you. You may wrap top-level route components to display a “Something went wrong” message to the user, just like server-side frameworks often handle crashes. You may also wrap individual widgets in an error boundary to protect them from crashing the rest of the application.</p>

<h2>New Behavior for Uncaught Errors</h2>

<p>This change has an important implication. <strong>As of React 16, errors that were not caught by any error boundary will result in unmounting of the whole React component tree.</strong></p>

<p>We debated this decision, but in our experience it is worse to leave corrupted UI in place than to completely remove it. For example, in a product like Messenger leaving the broken UI visible could lead to somebody sending a message to the wrong person. Similarly, it is worse for a payments app to display a wrong amount than to render nothing.</p>

<p>This change means that as you migrate to React 16, you will likely uncover existing crashes in your application that have been unnoticed before. Adding error boundaries lets you provide better user experience when something goes wrong.</p>

<p>For example, Facebook Messenger wraps content of the sidebar, the info panel, the conversation log, and the message input into separate error boundaries. If some component in one of these UI areas crashes, the rest of them remain interactive.</p>

<p>We also encourage you to use JS error reporting services (or build your own) so that you can learn about unhandled exceptions as they happen in production, and fix them.</p>

<h2>Why Not Use <code>try</code> / <code>catch</code>?</h2>

<p><code>try</code> / <code>catch</code> is great but it only works for imperative code:</p>
<div class="highlight"><pre><code class="language-js" data-lang="js"><span class="k">try</span> <span class="p">{</span>
  <span class="nx">showButton</span><span class="p">();</span>
<span class="p">}</span> <span class="k">catch</span> <span class="p">(</span><span class="nx">error</span><span class="p">)</span> <span class="p">{</span>
  <span class="c1">// ...</span>
<span class="p">}</span>
</code></pre></div>
<p>However, React components are declarative and specify <em>what</em> should be rendered:</p>
<div class="highlight"><pre><code class="language-js" data-lang="js"><span class="o">&lt;</span><span class="nx">Button</span> <span class="o">/&gt;</span>
</code></pre></div>
<p>Error boundaries preserve the declarative nature of React, and behave as you would expect. For example, even if an error occurs in a <code>componentDidUpdate</code> hook caused by a <code>setState</code> somewhere deep in the tree, it will still correctly propagate to the closest error boundary.</p>

<h2>Naming Changes from React 15</h2>

<p>React 15 included a very limited support for error boundaries under a different method name: <code>unstable_handleError</code>. This method no longer works, and you will need to change it to <code>componentDidCatch</code> in your code starting from the first 16 beta release.</p>
---------------
<h1 id="#title_3" >4、穷忙的人生</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2017/07/working-poor.html](http://www.ruanyifeng.com/blog/2017/07/working-poor.html)
<p>1、</p>

<p>香港曾经有一档电视真人秀，叫做，专门邀请富人体验穷人的生活。</p>

        <p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017071601.jpg" alt="" title="" /></p>

<p>有一期节目的主人公是。他的父亲田元灏是香港纺织界的头面人物，人称"一代裤王"。他本科毕业于康奈尔大学电子工程专业，又去读了哈佛大学 MBA，回到香港后创办了服装品牌 G2000 和 U2，是那种很努力的"富二代"。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017071602.jpg" alt="" title="" /></p>

<p>他崇尚自由竞争和人生奋斗，座右铭是"如果你今天对自己满意，明天就会被淘汰"，一直宣扬 "如果你有斗志，弱者也可以变成强者。"</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017071603.jpg" alt="" title="" /></p>

<p>但是，参加了这次电视节目以后，他的观点发生了180度转变，对着电视镜头公开说：</p>

<blockquote>
  <p>"这个社会在极严厉地惩罚，那些没条件读书的人。穷人一輩子都不可能变有钱人。在強弱悬殊的情况下，只有弱者越弱，越來越慘！"</p>
</blockquote>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017071604.jpg" alt="" title="" /></p>

<p>2、</p>

<p>田北辰为什么改变观点，认为穷人不可能翻身呢？原来，节目组请他了两天清洁工的生活，薪资是每小时25港币，每天的生活费只有50港币，住在只有1.6平方米的"笼屋"，月租1350港币。</p>

<p>所谓"笼屋"，外面看着像衣橱，门一拉开，里面只能放下一张床，关上门四面全挨着木板墙，东西都挂在墙上。就是这种条件，房产中介还称它为"豪华笼屋"，因为还有600港币的更低档，就是在马桶上放一块木板睡人。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017071605.jpg" alt="" title="" /></p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017071606.jpg" alt="" title="" /></p>

<p>上班时间是早上五点，地铁头班车还没开，只能坐夜宵巴士，车费是13港币，田北辰惊呼："每天生活费只有50港币，这怎么坐得起！"</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017071607.jpg" alt="" title="" /></p>

<p>开始工作后，好不容易熬到中午吃饭，但只有15元的预算，大部分的饭要20元，他最后只能坐在街边的楼梯上，就着白开水嚼干粮。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017071608.jpg" alt="" title="" /></p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017071609.jpg" alt="" title="" /></p>

<p>吃完了，还要抓紧时间躺在花坛上休息一会。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017071610.jpg" alt="" title="" /></p>

<p>做满9个小时，就可以下班了。但是，真正的清洁工为了养家户口，还要去做夜班，一天在外近17个小时，只能睡5、6个小时。田北辰说，因为只有两天，自己才有斗志坚持下去，如果要做一个月，甚至半年，那就太绝望了！</p>

<blockquote>
  <p>"没有学历、技术的人，为了活下去，不是住笼屋就是要工作到半夜，对于他们，最重要事情是下一顿吃什么，怎么会有时间和精力去思考未来怎么发展？来来去去都在死胡同！"</p>
</blockquote>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017071611.jpg" alt="" title="" /></p>

<p>3、</p>

<p>每天忙于工作，干到累死，但还是很穷，只能租屋住，没有自己的积蓄，一旦停止工作或者生病在床，生活来源顿时就成问题。田北辰体验的这种人生，社会学家早就注意到了，起名为"穷忙族"，百度百科的如下。</p>

<blockquote>
  <p>"穷忙族是指那些薪水不多，整日奔波劳动，却始终无法摆脱贫穷的人。最早出现于上世纪90年代的美国，指拼命工作仍然无法摆脱最低水准生活的人们。日本经济学家门仓贵史在《穷忙族》一书中，他对"穷忙族"下的定义是：每天繁忙地工作却依然不能过上富裕生活的人。"</p>
</blockquote>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017071614.jpg" alt="" title="" /></p>

<p>不仅香港有"穷忙族"，内地也越来越多。举例来说，根据，2016年上海送外卖最多的送餐员，是一位叫做何文妹的中年女性，至少送出了12214单。即使全年无休，每天平均也要33单，从午饭时间一直送到深夜，一刻不停。电瓶车的电瓶，一天要准备6组。车上插着两个手机，一个导航，一个接单。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017071612.jpg" alt="" title="" /></p>

<p>这种强度的劳动，每年能有多少收入呢？每单的送餐费是8元，这就是说，何文妹一年的送餐总收入在10万元左右。扣除电瓶费、车辆维护费、通信费等等以后，净收入大概还能剩下8万多元。这是"送餐王"的收入水平，大部分送餐员的收入，应该远不如她，可能只有一半左右。</p>

<p>上海的底层劳动者，收入基本就是这种水平。他们还要用这些钱支付房租。每天下班回到家，累得就想睡觉，睁开眼就要去上班，日复一日，人生的出路在哪里？</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017071613.jpg" alt="" title="" /></p>

<p>4、</p>

<p>将来的"穷忙族"，不仅是低技能的底层劳动者，还将包括很多受过高等教育、写字楼工作的白领。年轻人如果没有家庭支持，想要靠自己的努力出人头地，会变得越来越难。因为单靠工资收入，已经不足以积累财富了。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017071615.jpg" alt="" title="" /></p>

<p>有一项说：</p>

<blockquote>
  <p>"1993年属于低等收入者的城里人，到了1995年有43%都能向上爬。而相比之下，2011年属于低等收入者的城里人，到了2013年只有20%摘掉最底层的帽子。一个不恰当的比喻，如果上世纪90年代算是城市穷人的黄金时代的话，那今天这种好日子已经结束了。"</p>

<p>"一方面，城里穷人越来越难走出贫困；另一方面，城里富人的位置也坐得越来越稳。1993-1995年，城里的高等收入者有64%的概率能一直当富人。而到了2011-2013年，高等收入者竟然有84%的概率能保证自己不被从富人列表中除名。"</p>
</blockquote>

<p>上面的数字就是说，如果你是穷人，80%的概率以后你还是穷人；如果你是富人，84%的概率是以后你还是富人。一个台湾人说：</p>

<blockquote>
  <p>"那种奴隶化的生活（长时间工作，却仅能勉强满足温饱）才是历史的常态。过去三十年社会阶层的大幅流动，是历史的不正常，现在开始回归常态。99%的我们，都面临着这种大趋势的吞噬：你的工资不变，但房价和物价却是越来越高，于是你必需花更多时间来挣钱，甚至一天做二份工，最后成为没有自己时间的奴隶。"</p>
</blockquote>

<p>总的来看，下一代青年不太可能有上一代那么多机会。经济增长率已经开始放缓，还将继续放缓，人口增长高峰已经过去，老龄化越来越严重，老人的消费远不及年轻人。矿业、制造业、零售业、证券业......除了高科技，几乎所有行业都不会有以前那么高的增长率。上一代人赶上了中国经济起飞，还拥有依靠房地产翻身的机会，但是下一代人不会再有这样的机会。你现在买入一套房子，十年后价值翻上十倍，完全是零可能。</p>

<p>越来越多的人将会发现，即使从小就努力学习，从很好的学校毕业，后来努力工作，但迎接他们的将是"长久的低薪、难升迁的职场、高昂的物价、买不起的房子......"。尽管你很努力，待人友善，有公德心，但就是挣不到钱，只能在社会的底层挣扎。</p>

<p>5、</p>

<p>2015年，社会工作者藤田孝典调查日本的老人问题。</p>

<p>他，很多老人年轻时都拿过中产阶级的薪水（400万日元），但是现在已经沦落到社会的底层，过着非常困苦的生活。"七老八十还要在大热天当廉价劳工，因经济拮据而妻离子散，唯有独居烂屋，孤零零度过晚年。"</p>

<p>藤田孝典将这些老人称为"下流老人"（底层老人）。他称，日本的下流老人以后可能会达到1亿人。要知道，日本现在的总人口也只有1.27亿。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017071616.jpg" alt="" title="" /></p>

<p>下流老人有三大特征。（1）收入极低，即使政府提供补助费，也难以维持健康饮食，以及一般家庭应有的生活；（2）存款不足，老人必须提心吊胆地过活，一旦碰到突发事故或慢性病，日常已经捉襟见肘的生活，就会面临崩溃危险；（3）老无所依，子女连自己都养不起，更遑论赡养老人。日本不少老人因家庭破碎而长期独居，平日缺乏与亲朋邻里的交流，关系疏离，一旦发生意外无人照应。在晚年失去可以依靠的人，是下流老人最悲苦的特征。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017071617.jpg" alt="" title="" /></p>

<p>下流老人的根源就是，钱花光了，人还没死。日本媒体还发明了一个词"老后破产"，这就是长寿的恶梦。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017071618.jpg" alt="" title="" /></p>

<p>现代科技如此发达，人的寿命越来越长，可是工作又积累不了财富，于是，"清贫青年，流沙中年，下流老人"就成了大多数人必然的命运归宿。</p>

<p>（说明：本文选自我正在写的新书《未来世界的幸存者》，点击免费阅读全书。）</p>

<p>（正文完）</p>

<p>=========================================================</p>

<p>下面是推广时间。今天要向大家介绍。</p>

<p>普遍认为，程序员是一份高薪的职业。</p>

<blockquote>
  <ul>
<li>工作 3 年，平均年收入：10-20 万；</li>
<li>工作3-5 年，平均年收入：15-30万；</li>
<li>工作5-10 年，平均年收入30-50万左右；</li>
</ul>
</blockquote>

<p>（数据来源：程序员客栈/稀土掘金）</p>

<p>但是，岗位总有天花板，如果还想提高收入，除了提高技能、升职加薪之外，其实还可以通过股票投资，给自己增加一份被动收入，甚至实现财富自由，都有可能。</p>

<p></p>

<p>小熊之家，曾经是巴克莱银行的IT人员，程序员本身严密、理性的思维能力，让他在股票投资上如鱼得水。2007年～2015年，他个人美股投资累计收益263%，平均年化收益率12%；2013年～2015年，A股投资累计收益203%，平均年化收益率32.7%。</p>

<p>通过投资，他不再被工作束缚，并实现了财富自由。</p>

<p>2011年，他创立了理财在线教育网站----的院生已超过100万人，大量院生从0开始学习理财，懂得如何获得工资以外的被动收入，让资产保值增值。</p>

<p>如果你不想被死工资绑定，如果你想让自己的理性思维和逻辑能力，在股票投资分析上大放异彩，不妨来长投学习这门股票投资初级课，打开。</p>

<p></p>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2017-07-26T20:29:46+08:00">2017年7月26日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>博客文集：</li>
<li>社交媒体：</li>
<li>Feed订阅： </li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------
<h1 id="#title_4" >5、文章： 终极反馈环：从客户上报的缺陷中学习</h1>
Emanuil Slavov
[http://www.infoq.com/cn/articles/ultimate-feedback-loop?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/ultimate-feedback-loop?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/ultimate-feedback-loop/zh/headerimage/GettyImages-508140566-copy.jpg"/><p>对于客户上报的缺陷，探究其根源能对你的组织产生巨大的影响力。确保客户满意，降低成本，提高员工参与积极性的最佳做法便是“内视”，毕竟你已经有相应的数据了。最终，这一切都是为了持续改进。</p> <i>By Emanuil Slavov</i> <i> Translated by 大愚若智</i>
---------------
<h1 id="#title_5" >6、文章： 同程旅游实时计算的演进</h1>
李苏兴
[http://www.infoq.com/cn/articles/evolution-of-tongcheng-real-time-computing?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/evolution-of-tongcheng-real-time-computing?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/evolution-of-tongcheng-real-time-computing/zh/smallimage/logo-1 (1).jpg"/><p>同程旅游 (LY.COM) 是一家专业的一站式旅游预订平台，提供近万家景点门票、特价机票、出国旅游、周边游、自驾游及酒店预订服务 ; 专业旅游线路服务。全年公司服务人次超过 3 亿。目前同程旅游各个业务线，如：国内国际酒店，机票，火车票，会员，商业智能，分析等等都使用实时计算平台来构建实时类系统。 本文以时间为线索来介绍我们在实时计算平台建设过程中做过的工作，遇到的问题，希望能给需要实时计算的公司和同学提供参考。</p> <i>By 李苏兴</i>
---------------
<h1 id="#title_6" >7、王者荣耀的推送是如何做的？腾讯信鸽精准推送系统解析</h1>
Amos
[http://www.infoq.com/cn/news/2017/07/xinge-push?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/07/xinge-push?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p></p> <i>By Amos</i>
---------------
<h1 id="#title_7" >8、事件溯源系统中事件的版本化</h1>
Jan Stenberg
[http://www.infoq.com/cn/news/2017/07/versioning-event-sourcing?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/07/versioning-event-sourcing?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/news/2017/07/versioning-event-sourcing/zh/headerimage/storingevents.jpg"/><p>Greg Young在今年DDD eXchange会议上指出，在事件溯源系统中，其中的一项挑战就在于软件可能已经经历了许多的变更，但是数年前放到事件存储中的事件现在必须依然能够读取。如果系统可以废弃，那么事件的版本化相对会简单很多。但实际的挑战在于，有些系统是无法废弃的。</p> <i>By Jan Stenberg</i> <i> Translated by 张卫滨</i>
---------------