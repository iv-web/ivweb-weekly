## 文章索引
1、 <a href="#1pointfree-编程风格指南" >Pointfree 编程风格指南</a><br/>
2、 <a href="#2chrome开始集成图形识别-apishape-detection-api" >Chrome开始集成图形识别 API（Shape Detection API）</a><br/>
3、 <a href="#3文章-百度云互动直播的技术细节和解决方案实践经验谈" >文章： 百度云互动直播的技术细节和解决方案实践经验谈</a><br/>
4、 <a href="#4文章-历经8年双11流量洗礼淘宝开放平台如何攻克技术难关" >文章： 历经8年双11流量洗礼，淘宝开放平台如何攻克技术难关？</a><br/>
5、 <a href="#5文章-就欧盟的通用数据保护法规gdpr影响采访immuta" >文章： 就欧盟的通用数据保护法规(GDPR)影响采访Immuta</a><br/><h1 id="#title_0" >1、Pointfree 编程风格指南</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2017/03/pointfree.html](http://www.ruanyifeng.com/blog/2017/03/pointfree.html)
<p>本文要回答一个很重要的问题：有什么用？</p>

        <p>目前，主流的编程语言都不是函数式的，已经能够满足需求。为何还要学函数式编程呢，只为了多理解一些新奇的概念？</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017031201.jpg" alt="" title="" /></p>

<p>一个网友说：</p>

<blockquote>
  <p>"函数式编程有什么优势呢？"</p>

<p>"我感觉，这种写法可能会令人头痛吧。"</p>
</blockquote>

<p>很长一段时间，我根本不知道从何入手，如何将它用于实际项目？直到有一天，我学到了 Pointfree 这个概念，顿时豁然开朗，原来应该这样用！</p>

<p>我现在觉得，Pointfree 就是如何使用函数式编程的答案。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017031210.jpg" alt="" title="" /></p>

<h2>一、程序的本质</h2>

<p>为了理解 Pointfree，请大家先想一想，什么是程序？</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017031202.png" alt="" title="" /></p>

<p>上图是一个编程任务，左侧是数据输入（input），中间是一系列的运算步骤，对数据进行加工，右侧是最后的数据输出（output）。<strong>一个或多个这样的任务，就组成了程序。</strong></p>

<p>输入和输出（统称为 I/O）与键盘、屏幕、文件、数据库等相关，这些跟本文无关。<strong>这里的关键是，中间的运算部分不能有 I/O 操作，应该是纯运算，即通过纯粹的数学运算来求值。</strong>否则，就应该拆分出另一个任务。</p>

<p>I/O 操作往往有现成命令，大多数时候，编程主要就是写中间的那部分运算逻辑。现在，主流写法是过程式编程和面向对象编程，但是我觉得，最合适纯运算的是函数式编程。</p>

<h2>二、函数的拆分与合成</h2>

<p>上面那张图中，运算过程可以用一个函数<code>fn</code>表示。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017031203.png" alt="" title="" /></p>

<p><code>fn</code>的类型如下。</p>

<blockquote><pre><code class="language-javascript">
fn :: a -> b
</code></pre></blockquote>

<p>上面的式子表示，函数<code>fn</code>的输入是数据<code>a</code>，输出是数据<code>b</code>。</p>

<p>如果运算比较复杂，通常需要将<code>fn</code>拆分成多个函数。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017031204.png" alt="" title="" /></p>

<p><code>f1</code>、<code>f2</code>、<code>f3</code>的类型如下。</p>

<blockquote><pre><code class="language-javascript">
f1 :: a -> m
f2 :: m -> n
f3 :: n -> b
</code></pre></blockquote>

<p>上面的式子中，输入的数据还是<code>a</code>，输出的数据还是<code>b</code>，但是多了两个中间值<code>m</code>和<code>n</code>。</p>

<p>我们可以把整个运算过程，想象成一根水管（pipe），数据从这头进去，那头出来。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017031205.png" alt="" title="" /></p>

<p>函数的拆分，无非就是将一根水管拆成了三根。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017031206.png" alt="" title="" /></p>

<p>进去的数据还是<code>a</code>，出来的数据还是<code>b</code>。<code>fn</code>与<code>f1</code>、<code>f2</code>、<code>f3</code>的关系如下。</p>

<blockquote><pre><code class="language-javascript">
fn = R.pipe(f1, f2, f3);
</code></pre></blockquote>

<p>上面代码中，我用到了 。</p>

<h2>三、Pointfree 的概念</h2>

<blockquote><pre><code class="language-javascript">
fn = R.pipe(f1, f2, f3);
</code></pre></blockquote>

<p>这个公式说明，如果先定义<code>f1</code>、<code>f2</code>、<code>f3</code>，就可以算出<code>fn</code>。整个过程，根本不需要知道<code>a</code>或<code>b</code>。</p>

<p>也就是说，我们完全可以把数据处理的过程，定义成一种与参数无关的合成运算。不需要用到代表数据的那个参数，只要把一些简单的运算步骤合成在一起即可。</p>

<p><strong>这就叫做 Pointfree：不使用所要处理的值，只合成运算过程。</strong>中文可以译作"无值"风格。</p>

<p>请看下面的例子。</p>

<blockquote><pre><code class="language-javascript">
var addOne = x => x + 1;
var square = x => x * x;
</code></pre></blockquote>

<p>上面是两个简单函数<code>addOne</code>和<code>square</code>。</p>

<p>把它们合成一个运算。</p>

<blockquote><pre><code class="language-javascript">
var addOneThenSquare = R.pipe(addOne, square);

addOneThenSquare(2) //  9
</code></pre></blockquote>

<p>上面代码中，<code>addOneThenSquare</code>是一个合成函数。定义它的时候，根本不需要提到要处理的值，这就是 Pointfree。</p>

<h2>四、Pointfree 的本质</h2>

<p>Pointfree 的本质就是使用一些通用的函数，组合出各种复杂运算。上层运算不要直接操作数据，而是通过底层函数去处理。这就要求，将一些常用的操作封装成函数。</p>

<p>比如，读取对象的<code>role</code>属性，不要直接写成<code>obj.role</code>，而是要把这个操作封装成函数。</p>

<blockquote><pre><code class="language-javascript">
var prop = (p, obj) => obj[p];
var propRole = R.curry(prop)('role');
</code></pre></blockquote>

<p>上面代码中，<code>prop</code>函数封装了读取操作。它需要两个参数<code>p</code>（属性名）和<code>obj</code>（对象）。这时，要把数据<code>obj</code>要放在最后一个参数，这是为了方便柯里化。函数<code>propRole</code>则是指定读取<code>role</code>属性，下面是它的用法（查看）。</p>

<blockquote><pre><code class="language-javascript">
var isWorker = s => s === 'worker';
var getWorkers = R.filter(R.pipe(propRole, isWorker));

var data = [
  {name: '张三', role: 'worker'},
  {name: '李四', role: 'worker'},
  {name: '王五', role: 'manager'},
];
getWorkers(data)
// [
//   {"name": "张三", "role": "worker"},
//   {"name": "李四", "role": "worker"}
// ]
</code></pre></blockquote>

<p>上面代码中，<code>data</code>是传入的值，<code>getWorkers</code>是处理这个值的函数。定义<code>getWorkers</code>的时候，完全没有提到<code>data</code>，这就是 Pointfree。</p>

<p>简单说，Pointfree 就是运算过程抽象化，处理一个值，但是不提到这个值。这样做有很多好处，它能够让代码更清晰和简练，更符合语义，更容易复用，测试也变得轻而易举。</p>

<h2>五、Pointfree 的示例一</h2>

<p>下面，我们来看一个示例。</p>

<blockquote><pre><code class="language-javascript">
var str = 'Lorem ipsum dolor sit amet consectetur adipiscing elit';
</code></pre></blockquote>

<p>上面是一个字符串，请问其中最长的单词有多少个字符？</p>

<p>我们先定义一些基本运算。</p>

<blockquote><pre><code class="language-javascript">
// 以空格分割单词
var splitBySpace = s => s.split(' ');

// 每个单词的长度
var getLength = w => w.length;

// 词的数组转换成长度的数组
var getLengthArr = arr => R.map(getLength, arr); 

// 返回较大的数字
var getBiggerNumber = (a, b) => a > b ? a : b;

// 返回最大的一个数字
var findBiggestNumber = 
  arr => R.reduce(getBiggerNumber, 0, arr);
</code></pre></blockquote>

<p>然后，把基本运算合成为一个函数（查看）。</p>

<blockquote><pre><code class="language-javascript">
var getLongestWordLength = R.pipe(
  splitBySpace,
  getLengthArr,
  findBiggestNumber
);

getLongestWordLength(str) // 11
</code></pre></blockquote>

<p>可以看到，整个运算由三个步骤构成，每个步骤都有语义化的名称，非常的清晰。这就是 Pointfree 风格的优势。</p>

<p>Ramda 提供了很多现成的方法，可以直接使用这些方法，省得自己定义一些常用函数（查看）。</p>

<blockquote><pre><code class="language-javascript">
// 上面代码的另一种写法
var getLongestWordLength = R.pipe(
  R.split(' '),
  R.map(R.length),
  R.reduce(R.max, 0)
);
</code></pre></blockquote>

<h2>六、Pointfree 示例二</h2>

<p>最后，看一个实战的例子，拷贝自 Scott Sauyet 的文章。那篇文章能帮助你深入理解柯里化，强烈推荐阅读。</p>

<p>下面是一段服务器返回的 JSON 数据。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017031207.png" alt="" title="" /></p>

<p>现在要求是，找到用户 Scott 的所有未完成任务，并按到期日期升序排列。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017031208.png" alt="" title="" /></p>

<p>过程式编程的代码如下（查看）。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017031209.png" alt="" title="" /></p>

<p>上面代码不易读，出错的可能性很大。</p>

<p>现在使用 Pointfree 风格改写（查看）。</p>

<blockquote><pre><code class="language-javascript">
var getIncompleteTaskSummaries = function(membername) {
  return fetchData()
    .then(R.prop('tasks'))
    .then(R.filter(R.propEq('username', membername)))
    .then(R.reject(R.propEq('complete', true)))
    .then(R.map(R.pick(['id', 'dueDate', 'title', 'priority'])))
    .then(R.sortBy(R.prop('dueDate')));
};
</code></pre></blockquote>

<p>上面代码已经清晰很多了。</p>

<p>另一种写法是，把各个<code>then</code>里面的函数合成起来（查看）。</p>

<blockquote><pre><code class="language-javascript">
// 提取 tasks 属性
var SelectTasks = R.prop('tasks');

// 过滤出指定的用户
var filterMember = member => R.filter(
  R.propEq('username', member)
);

// 排除已经完成的任务
var excludeCompletedTasks = R.reject(R.propEq('complete', true));

// 选取指定属性
var selectFields = R.map(
  R.pick(['id', 'dueDate', 'title', 'priority'])
);

// 按照到期日期排序
var sortByDueDate = R.sortBy(R.prop('dueDate'));

// 合成函数
var getIncompleteTaskSummaries = function(membername) {
  return fetchData().then(
    R.pipe(
      SelectTasks,
      filterMember(membername),
      excludeCompletedTasks,
      selectFields,
      sortByDueDate,
    )
  );
};
</code></pre></blockquote>

<p>上面的代码跟过程式的写法一比较，孰优孰劣一目了然。</p>

<h2>七、参考链接</h2>

<ul>
<li></li>
<li></li>
</ul>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2017-03-13T06:56:10+08:00">2017年3月13日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>博客文集：</li>
<li>社交媒体：</li>
<li>Feed订阅： </li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------
<h1 id="#title_1" >2、Chrome开始集成图形识别 API（Shape Detection API）</h1>
Miguel Casas-Sanchez
[http://www.infoq.com/cn/news/2017/03/Chrome-Shape-Detection-API?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/03/Chrome-Shape-Detection-API?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>本文档描述了一套Chrome中针对静态和/或动态图像的图形识别（如：人脸识别）API。</p> <i>By Miguel Casas-Sanchez</i> <i> Translated by 谈浩</i>
---------------
<h1 id="#title_2" >3、文章： 百度云互动直播的技术细节和解决方案实践经验谈</h1>
邢怀飞
[http://www.infoq.com/cn/articles/practical-experience-of-Baidu-cloud-interactive-live?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/practical-experience-of-Baidu-cloud-interactive-live?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/practical-experience-of-Baidu-cloud-interactive-live/zh/smallimage/baidu_cloud_100.jpg"/><p>互动直播已成为直播发展的趋势，不妨一起了解下其前沿技术。 1、互动直播的功能与核心技术是什么？ 2、目前有哪些主流的技术方案？这些方案都有哪些优缺点？ 3、互动直播技术发展趋势如何？ 本文将从以上方面详细解答，希望能让你有所收获。</p> <i>By 邢怀飞</i>
---------------
<h1 id="#title_3" >4、文章： 历经8年双11流量洗礼，淘宝开放平台如何攻克技术难关？</h1>
风胜
[http://www.infoq.com/cn/articles/taobao-open-platform-overcome-technical-difficulties?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/taobao-open-platform-overcome-technical-difficulties?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/taobao-open-platform-overcome-technical-difficulties/zh/smallimage/choice.jpg"/><p>本文将为您揭开淘宝开放平台的高性能API网关、高可靠消息服务、零漏单数据同步的技术内幕。</p> <i>By 风胜</i>
---------------
<h1 id="#title_4" >5、文章： 就欧盟的通用数据保护法规(GDPR)影响采访Immuta</h1>
Manuel Pais
[http://www.infoq.com/cn/articles/immuta-gdpr-implications?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/immuta-gdpr-implications?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/immuta-gdpr-implications/zh/headerimage/GettyImages-530764034.jpg"/><p>InfoQ采访了Immuta的Andrew Burt和Steve Touw，来更好地了解欧盟的通用数据保护法规带来的影响和挑战，这项法规将于2018年五月生效。</p> <i>By Manuel Pais</i> <i> Translated by 足下</i>
---------------