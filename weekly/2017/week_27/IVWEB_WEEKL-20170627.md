## 文章索引
1、 <a href="#1漫谈-js-函数式编程一" >漫谈 JS 函数式编程（一）</a><br/>
2、 <a href="#2学会思考而不只是编程" >学会思考，而不只是编程</a><br/>
3、 <a href="#3文章-深入浅出tensorflow六tensorflow高层封装" >文章： 深入浅出TensorFlow（六）TensorFlow高层封装</a><br/>
4、 <a href="#4视频访谈-专访明略数据邵蓥侠传统公安领域的机器学习实践" >视频访谈： 专访明略数据邵蓥侠：传统公安领域的机器学习实践</a><br/>
5、 <a href="#5应用工程师的分布式系统理论" >应用工程师的分布式系统理论</a><br/>
6、 <a href="#6safari-11增加多项缺失功能并增强默认的隐私保护措施" >Safari 11增加多项缺失功能，并增强默认的隐私保护措施</a><br/>
7、 <a href="#7gpu技术大会上采访greg-kurtzer" >GPU技术大会上采访Greg Kurtzer</a><br/>
8、 <a href="#8gartner公布iaas云厂商报告aws和微软依然是领军者" >Gartner公布IaaS云厂商报告，AWS和微软依然是领军者</a><br/>
9、 <a href="#9文章-mxnet-api入门-第1篇" >文章： MXNet API入门 —第1篇</a><br/>
10、 <a href="#10ios-开发周报苹果想用-iphone-管理你的医疗历史the-right-way-to-architect-ios-app-with-swift" >iOS 开发周报：苹果想用 iPhone 管理你的医疗历史、The Right Way to Architect iOS App with Swift</a><br/>
11、 <a href="#11android开发周报android-80开始推送微店插件化实践" >Android开发周报：Android 8.0开始推送、微店插件化实践</a><br/>
12、 <a href="#12在银行内部建立创业公司与peterjan-van-nieuwenhuizen的问答" >在银行内部建立创业公司：与Peterjan van Nieuwenhuizen的问答</a><br/>
13、 <a href="#13google发布mobilenets一种预训练的高效tensorflow计算机视觉模型" >Google发布MobileNets，一种预训练的高效Tensorflow计算机视觉模型</a><br/>
14、 <a href="#14oracle的java模块化系统保卫战" >Oracle的Java模块化系统保卫战</a><br/>
15、 <a href="#15fex-技术周刊---2017/06/26" >FEX 技术周刊 - 2017/06/26</a><br/>
16、 <a href="#16left-handed-brush-lettering:-how-to-get-started" >Left-Handed Brush Lettering: How To Get Started</a><br/><h1 id="#title_0" >1、漫谈 JS 函数式编程（一）</h1>

[https://www.h5jun.com/post/js-functional-1.html](https://www.h5jun.com/post/js-functional-1.html)
<div class="toc"><ul>
<li></li>
<li><ul>
<li></li>
<li></li>
</ul>
</li>
</ul>
</div><blockquote>
<p>这可能是最简单易懂的函数式编程介（扯）绍（淡）了</p>
</blockquote>
<p><img src="https://p5.ssl.qhimg.com/t01be0fea9eac30db67.png" alt=""></p>
<p>目前前端界（以及其他一些领域）对函数式编程大体上两种态度，一些人是觉得函数式编程特牛逼，尤其是现在许多新生的框架和库都在标榜自己的函数式特征。而另一些人，又觉得函数式编程学起来很难，而且似乎也没有什么卵用，理由是在自己经历的项目里面很难看到具体的函数式编程应用场景，甚至其中许多人认同一个观点，觉得函数式编程只适合于学术研究，很难在工程项目中实际使用。</p>
<!--more-->
<p>不管你在阅读本文之前属于哪一种人，又或者你是刚接触函数式编程的新人，都没有关系。本文不是研究函数式编程范式的学术研究，而函数式编程作为一个可以说是程序设计理论中最古老的编程范式，在它几十年上百年的发展历史中，已经积累了大量的资料和素材，对于想要在学术领域里完全弄明白它的同学，完全可以在网上、书店里找到各种资料。本文的重点不在于概念，而在于实战。因此，你不会听到太多各种函数式编程的名词讨论，比如诸如 Curry、Mond 之类的专业术语。相反，我们主要来讨论函数式编程在前端领域内使用的一些实际例子，了解为什么前端需要学习函数式编程，使用函数式编程写代码能给我们带来什么。如果弄明白了这些，那么关于函数式编程不实用的谣言也就不攻自破了。</p>
<hr>
<h2>数据抽象或过程抽象</h2>
<p>为什么我们接受面向过程或面向对象思想很容易，而我们要完全接受函数式编程却感觉难得多？</p>
<p><img src="https://p0.ssl.qhimg.com/t014bd4a2678c54f7aa.png" alt=""></p>
<p>我认为这个问题大体上可以这么解释：</p>
<p>人脑本能地容易理解“看得见“、“摸得着”的物体，对于“运动”和“变化”一类不着形的东西，人脑理解起来要略微地费劲一些。而人类要做好一件复杂的事情，大脑有两种抽象方向，一种是对实体进行抽象，另一种是对过程进行抽象：</p>
<p><img src="https://p4.ssl.qhimg.com/t018779b35f35143e84.jpg" alt=""></p>
<p>简答来说，即在软件设计的过程中，如果要保证软件产品的功能稳定可用，同时要保证它的灵活性和可扩展性，那么系统就要有变化的部分和不变的部分。哪些部分应当设计成“不变”，哪些部分应当设计成“可变”，在这个取舍过程中，FP（函数式编程）和 OOP（面向对象编程）正是走了两条不同的路线。</p>
<p>面向对象对数据进行抽象，将行为以对象方法的方式封装到数据实体内部，从而降低系统的耦合度。而函数式编程，选择对过程进行抽象，将数据以输入输出流的方式封装进过程内部，从而也降低系统的耦合度。两者虽是截然不同，然而在系统设计的目标上可以说是殊途同归的。</p>
<p>面向对象思想和函数式编程思想也是不矛盾的，因为一个庞大的系统，可能既要对数据进行抽象，又要对过程进行抽象，或者一个局部适合进行数据抽象，另一个局部适合进行过程抽象，这都是可能的。数据抽象不一定以对象实体为形式，同样过程抽象也不是说形式上必然是 functional 的，比如流式对象（InputStream、OutputStream）、Express 的 middleware，就带有明显的过程抽象的特征。但是在通常情况下，OOP更适合用来做数据抽象，FP更适合用来做过程抽象。</p>
<h2>纯函数</h2>
<p>再具体深入下去之前，我们先来解答一个问题，那就是为什么用 FP 或过程抽象能够降低系统的耦合度。这里我们要先理解一个概念，这个概念叫“纯函数”。</p>
<p>根据定义，如果一个函数符合两个条件，它被称为<strong>纯函数</strong>:</p>
<ul>
<li>此函数在相同的输入值时，总是产生相同的输出。函数的输出和当前运行环境的<strong>上下文状态</strong>无关。</li>
<li>此函数运行过程不影响运行环境，比如不会触发事件、更改环境中的对象、终端输出值等。</li>
</ul>
<p>简单来说，也就是当<strong>一个函数的输出不受外部环境影响，同时也不影响外部环境时，该函数就是纯函数。</strong></p>
<p><img src="https://p1.ssl.qhimg.com/t0192c9e40e207d972d.png" alt=""></p>
<p>JavaScript 内置函数中有不少纯函数，也有不少非纯函数。</p>
<p>比如以下函数是纯函数：</p>
<ul>
<li>String.prototype.toUpperCase</li>
<li>Array.prototype.map</li>
<li>Function.prototype.bind</li>
</ul>
<p>以下函数不是纯函数：</p>
<ul>
<li>Math.random</li>
<li>Date.now</li>
<li>document.body.appendChild</li>
<li>Array.prototype.sort</li>
</ul>
<p>为什么要区分纯函数和非纯函数呢？因为在系统里，纯函数与非纯函数相比，在可测试性、可维护性、可移植性、并行计算和可扩展性方面都有着巨大的优势。</p>
<p>在这里我用可测试性来举例：</p>
<p>对于纯函数，因为是<strong>无状态</strong>的，测试的时候不需要构建运行时环境，也不需要用特定的顺序进行测试：</p>
<pre><code class="hljs lang-js">test(t =&gt; {
    t.is(add(<span class="hljs-number">10</span>, <span class="hljs-number">20</span>), <span class="hljs-number">30</span>); <span class="hljs-comment">//add(x,y) 是个纯函数，不需要为它构建测试环境</span>
    ...
});
</code></pre>
<p>对于非纯函数，就比较复杂：</p>
<pre><code class="hljs lang-js">test.before(t =&gt; {
    <span class="hljs-keyword">let</span> list = <span class="hljs-built_in">document</span>.createElement(<span class="hljs-string">'ul'</span>);
    list.id = <span class="hljs-string">'xxxxxx'</span>;
    ...
});

test(t =&gt; {
    <span class="hljs-keyword">let</span> list = <span class="hljs-built_in">document</span>.getElementById(<span class="hljs-string">'xxxxxx'</span>);
    t.is(sortList(list).innerHTML, <span class="hljs-string">`&lt;ul&gt;
        ...
    &lt;/ul&gt;`</span>);
});

test.after(t =&gt; {
    ...
    document.removeChild(list);
});
</code></pre>
<h4>函数式编程能够减少系统中的非纯函数</h4>
<p>首先我们看一个例子：</p>
<p><script src="https:////code.h5jun.com/js/embed.min.js?3.40.2"></script></p>
<pre><code class="hljs lang-js"><span class="hljs-comment">//two impure functions</span>

<span class="hljs-function"><span class="hljs-keyword">function</span> <span class="hljs-title">setColor</span>(<span class="hljs-params">el, color</span>)</span>{
  el.style.color = color;
}

<span class="hljs-function"><span class="hljs-keyword">function</span> <span class="hljs-title">setColors</span>(<span class="hljs-params">els, color</span>)</span>{
  els.forEach(el =&gt; setColor(el, color));
}

<span class="hljs-keyword">let</span> items1 = <span class="hljs-built_in">document</span>.querySelectorAll(<span class="hljs-string">'ul &gt; li:nth-child(2n + 1)'</span>);
<span class="hljs-keyword">let</span> items2 = <span class="hljs-built_in">document</span>.querySelectorAll(<span class="hljs-string">'ul &gt; li:nth-child(3n + 1)'</span>);

setColors(items2, <span class="hljs-string">'green'</span>);
setColors(items1, <span class="hljs-string">'red'</span>);
</code></pre>
<p>在这里我们有两个彼此依赖的非纯函数，setColor(el, color) 和 setColors(els, color)。在测试的时候，我们需要构建环境来测试两个函数。</p>
<p>现在，我们用函数式编程思想来改造这个系统：</p>
<p><script src="https:////code.h5jun.com/js/embed.min.js?3.40.2"></script></p>
<pre><code class="hljs lang-js"><span class="hljs-comment">//only one impure function</span>

<span class="hljs-function"><span class="hljs-keyword">function</span> <span class="hljs-title">batch</span>(<span class="hljs-params">fn</span>)</span>{
  <span class="hljs-keyword">return</span> <span class="hljs-function"><span class="hljs-keyword">function</span>(<span class="hljs-params">target, ...args</span>)</span>{
    <span class="hljs-keyword">if</span>(target.length &gt;= <span class="hljs-number">0</span>){
      <span class="hljs-keyword">return</span> <span class="hljs-built_in">Array</span>.from(target).map(item =&gt; fn.apply(<span class="hljs-keyword">this</span>, [item, ...args]));
    }<span class="hljs-keyword">else</span>{
      <span class="hljs-keyword">return</span> fn.apply(<span class="hljs-keyword">this</span>, [target, ...args]);
    }
  }
}

<span class="hljs-function"><span class="hljs-keyword">function</span> <span class="hljs-title">setColor</span>(<span class="hljs-params">el, color</span>)</span>{
  el.style.color = color;
}

<span class="hljs-keyword">let</span> setColors = batch(setColor);

<span class="hljs-keyword">let</span> items1 = <span class="hljs-built_in">document</span>.querySelectorAll(<span class="hljs-string">'ul &gt; li:nth-child(2n + 1)'</span>);
<span class="hljs-keyword">let</span> items2 = <span class="hljs-built_in">document</span>.querySelectorAll(<span class="hljs-string">'ul &gt; li:nth-child(3n + 1)'</span>);

setColors(items2, <span class="hljs-string">'green'</span>);
setColors(items1, <span class="hljs-string">'red'</span>);
</code></pre>
<p>在这里，我们建立一个过程抽象的高阶函数 batch(fn)，这个函数的作用是，对它的输入函数返回一个新的函数，这个函数与输入函数的区别是，如果调用的第一个实参是一个数组，那么将这个数组展开，用每一个值依次调用输入函数，返回一个数组，包活每次调用返回的结果。</p>
<p>batch(fn) 本身虽然看似复杂，但是有意思的事，这个函数无疑是纯函数，所以 batch(fn) 自身的测试是非常简单的：</p>
<pre><code class="hljs lang-js">test(t =&gt; {
  <span class="hljs-keyword">let</span> add = (x, y) =&gt; x + y;
  <span class="hljs-keyword">let</span> listAdd = batch(add);

  t.deepEqual(listAdd([<span class="hljs-number">1</span>,<span class="hljs-number">2</span>,<span class="hljs-number">3</span>], <span class="hljs-number">1</span>), [<span class="hljs-number">2</span>,<span class="hljs-number">3</span>,<span class="hljs-number">4</span>]);
});
</code></pre>
<p>由于我们上面举的例子 setColor 和 setColors 虽然不是纯函数，但是却非常简单，因此似乎设计 batch(fn) 的意义不大，有把系统变得更复杂的嫌疑。然而，对于有许多操作 DOM 的函数的框架或库，有了 batch(fn)，我们就可以实现很简单的接口（对单一元素操作），然后利用 batch(fn) 获得更复杂接口（对元素进行批量操作），从而大大降低系统本身的复杂的，提升可维护性。</p>
<p>注意一点，batch(fn) 输出的函数有副作用，然而 batch(fn) 用闭包将输出的函数的副作用限制在了 batch(fn) 的作用域内。</p>
<h4> 的 lift 方法</h4>
<p>Ramda.js 的 lift 方法和 batch 有一点点类似，不过功能更强大。让我们来用它实现一个有一点点“烧脑”的效果，来作为这篇文章的结尾：</p>
<p><script src="https:////code.h5jun.com/js/embed.min.js?3.40.2"></script></p>
<pre><code class="hljs lang-js"><span class="hljs-keyword">async</span> <span class="hljs-function"><span class="hljs-keyword">function</span> <span class="hljs-title">reducer</span>(<span class="hljs-params">promise, action</span>)</span>{
  <span class="hljs-keyword">let</span> res = <span class="hljs-keyword">await</span> promise;
  <span class="hljs-keyword">return</span> action(res);
}

<span class="hljs-function"><span class="hljs-keyword">function</span> <span class="hljs-title">continuous</span>(<span class="hljs-params">...functors</span>)</span>{
  <span class="hljs-keyword">return</span> <span class="hljs-keyword">async</span> <span class="hljs-function"><span class="hljs-keyword">function</span>(<span class="hljs-params">input</span>)</span>{
    <span class="hljs-keyword">return</span> <span class="hljs-keyword">await</span> functors.reduce(reducer, input)
  }
}

<span class="hljs-function"><span class="hljs-keyword">function</span> <span class="hljs-title">sleep</span>(<span class="hljs-params">ms</span>)</span>{
  <span class="hljs-keyword">return</span> <span class="hljs-keyword">new</span> <span class="hljs-built_in">Promise</span>(resolve =&gt; setTimeout(resolve, ms));
}

<span class="hljs-keyword">async</span> <span class="hljs-function"><span class="hljs-keyword">function</span> <span class="hljs-title">setColor</span>(<span class="hljs-params">item, color</span>)</span>{
  <span class="hljs-keyword">await</span> sleep(<span class="hljs-number">500</span>);
  item.style.color = color;
}

<span class="hljs-keyword">let</span> comb = R.lift((el, color) =&gt; {
  <span class="hljs-keyword">return</span> [el, color];
});

<span class="hljs-keyword">let</span> changeColorTo = (args) =&gt; R.partial(setColor, args);

<span class="hljs-keyword">let</span> items = <span class="hljs-built_in">Array</span>.from(list.children);

<span class="hljs-keyword">let</span> task = R.map(changeColorTo, comb(
  items,
  [<span class="hljs-string">'red'</span>, <span class="hljs-string">'orange'</span>, <span class="hljs-string">'yellow'</span>]
));

continuous(...task)(<span class="hljs-number">0</span>);
</code></pre>
<p>-- 期待下一篇吧 --</p>
---------------
<h1 id="#title_1" >2、学会思考，而不只是编程</h1>
Yevgeniy Brikman
[http://www.infoq.com/cn/news/2017/06/Dont-learn-code-Learn-think?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/06/Dont-learn-code-Learn-think?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>中国人常说“授之以鱼不如授之以渔”。如果说教授编程是授之以鱼，那么教授计算机科学就是授之以渔。为什么说学习计算机科学比学会编程要重要得多？来听听Yevgeniy Brikman的解释。</p> <i>By Yevgeniy Brikman</i> <i> Translated by 薛命灯</i>
---------------
<h1 id="#title_2" >3、文章： 深入浅出TensorFlow（六）TensorFlow高层封装</h1>
郑泽宇
[http://www.infoq.com/cn/articles/introduction-of-tensorflow-part06?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/introduction-of-tensorflow-part06?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/introduction-of-tensorflow-part06/zh/smallimage/logo (1).jpg"/><p>为了让TensorFlow使用起来更加灵活，更加方便，可以使用一些高级封装。本文将介绍TensorFlow的四种主要封装：TensorFlow-Slim、tf.contrib.learn（之前也被称为skflow）、TFLearn、Keras；同时还将通过其中常用的三种方式在MNIST数据集上实现卷积神经网络。</p> <i>By 郑泽宇</i>
---------------
<h1 id="#title_3" >4、视频访谈： 专访明略数据邵蓥侠：传统公安领域的机器学习实践</h1>
邵蓥侠
[http://www.infoq.com/cn/interviews/interview-with-shaoyingxia-talk-machine-learning-practice?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/interviews/interview-with-shaoyingxia-talk-machine-learning-practice?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/interviews/interview-with-shaoyingxia-talk-machine-learning-practice/zh/mediumimage/shaoyingxia270.jpg"/><p>在公安领域应用大数据和机器学习是非常有价值的事情，具体的工作中要解决数据清理问题、寻求到合适的数学模型。负责过相应项目明略数据的邵蓥侠有哪些可以分享的经验？InfoQ在QCon北京站对其进行了视频专访。</p> <i>By 邵蓥侠</i>
---------------
<h1 id="#title_4" >5、应用工程师的分布式系统理论</h1>
Andrew Morgan
[http://www.infoq.com/cn/news/2017/06/distributed-systems-theory?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/06/distributed-systems-theory?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/news/2017/06/distributed-systems-theory/zh/headerimage/GettyImages-521696036.jpg"/><p>分布式系统工程师、《RabbitMQ实战》合著者Alvaro Videla在2017伦敦QCon上回顾了分布式系统理论。主题涵盖将分布式系统从不同维度进行分类，例如时间模型、故障模式。并讨论这些类别的选型考虑因素。</p> <i>By Andrew Morgan</i> <i> Translated by 金灵杰</i>
---------------
<h1 id="#title_5" >6、Safari 11增加多项缺失功能，并增强默认的隐私保护措施</h1>
David Iffland
[http://www.infoq.com/cn/news/2017/06/safari-11-announced-with-webrtc?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/06/safari-11-announced-with-webrtc?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/news/2017/06/safari-11-announced-with-webrtc/zh/headerimage/GettyImages-532389864.jpg"/><p>苹果宣布了旗下浏览器的最新版本Safari 11。Safari 11运行在iOS和macOS上，现在支持WebRTC和WebAssembly。此外它还增加了一个新的追踪屏蔽器，可以削弱第三方追踪用户网络痕迹的能力。</p> <i>By David Iffland</i> <i> Translated by 王强</i>
---------------
<h1 id="#title_6" >7、GPU技术大会上采访Greg Kurtzer</h1>
Rags Srinivas
[http://www.infoq.com/cn/news/2017/06/gpu-tech-conference?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/06/gpu-tech-conference?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Rags Srinivas在GPU技术大会上采访了参与诸多开源软件的贡献者Greg Kurtzer。</p> <i>By Rags Srinivas</i> <i> Translated by 周元昊</i>
---------------
<h1 id="#title_7" >8、Gartner公布IaaS云厂商报告，AWS和微软依然是领军者</h1>
薛命灯
[http://www.infoq.com/cn/news/2017/06/Gartner-announce-IaaS-aws?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/06/Gartner-announce-IaaS-aws?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Gartner发布了最新的IaaS云厂商魔力象限报告，AWS和微软仍然是领军者，处于“领导者（Leaders）”象限，而Google处于“愿景者（Visionaries）”象限，阿里巴巴、IBM和Oracle紧随其后。</p> <i>By 薛命灯</i>
---------------
<h1 id="#title_8" >9、文章： MXNet API入门 —第1篇</h1>
Julien Simon
[http://www.infoq.com/cn/articles/an-introduction-to-the-mxnet-api-part01?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/an-introduction-to-the-mxnet-api-part01?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/an-introduction-to-the-mxnet-api-part01/zh/smallimage/Crashlytics_100_100.jpg"/><p>Apache MXNet是一种功能全面、可以灵活编程并且扩展能力超强的深度学习框架，支持包括卷积神经网络(CNN)与长短期记忆网络(LSTM)在内的顶尖深度模型。这一系列文章介绍了MXNet的基本概念和使用方法。</p> <i>By Julien Simon</i> <i> Translated by 大愚若智</i>
---------------
<h1 id="#title_9" >10、iOS 开发周报：苹果想用 iPhone 管理你的医疗历史、The Right Way to Architect iOS App with Swift</h1>
靛青K
[http://www.infoq.com/cn/news/2017/06/ios-weekly-apple-iphone-Medical?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/06/ios-weekly-apple-iphone-Medical?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>苹果想用 iPhone 管理你的医疗历史、The Right Way to Architect iOS App with Swift</p> <i>By 靛青K</i>
---------------
<h1 id="#title_10" >11、Android开发周报：Android 8.0开始推送、微店插件化实践</h1>
郭亮
[http://www.infoq.com/cn/news/2017/06/Android-weekly-8-0-weidian?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/06/Android-weekly-8-0-weidian?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Android O的正式名称预测为奥利奥，版本号确定为8.0。谷歌为参与Android Beta的用户分发了全新的Android O系统，也就是第三个开发者预览版。本期周报为大家带来了crash处理、WCDB、路由、注解等多方面的技术干货，欢迎阅读。</p> <i>By 郭亮</i>
---------------
<h1 id="#title_11" >12、在银行内部建立创业公司：与Peterjan van Nieuwenhuizen的问答</h1>
Hugo Messer, Shane Hastie
[http://www.infoq.com/cn/news/2017/06/startup-within-bank?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/06/startup-within-bank?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/news/2017/06/startup-within-bank/zh/headerimage/GettyImages-628883362.jpg"/><p>Peterjan van Nieuwenhuizen是印度尼西亚BTPN银行的智能数字化银行业务负责人。在即将到来的印度尼西亚敏捷大会上，他将会介绍在传统银行中建立创业心态所需要的文化变更，它将带来的挑战和机遇以及想实现所需要的条件。他向InfoQ分享了他的经验。</p> <i>By Hugo Messer</i> <i> Translated by 刘嘉洋</i>
---------------
<h1 id="#title_12" >13、Google发布MobileNets，一种预训练的高效Tensorflow计算机视觉模型</h1>
Roland Meertens
[http://www.infoq.com/cn/news/2017/06/google-mobilenets-tensorflow?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/06/google-mobilenets-tensorflow?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Google在Tensorflow的Github代码库中，发布了多个用在移动电话上的高效预训练计算机视觉模型。这些模型间的差别在于模型的参数、单图像处理的计算能力以及预测的准确性，开发人员可从中做出选取。</p> <i>By Roland Meertens</i> <i> Translated by Rays</i>
---------------
<h1 id="#title_13" >14、Oracle的Java模块化系统保卫战</h1>
Michael Redlich
[http://www.infoq.com/cn/news/2017/06/oracle-defends-jpms?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/06/oracle-defends-jpms?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>2017年企业新兴技术（ETE）大会上最为及时的演讲之一要算由Oracle JVM负责人Karen Kinnear呈献的“Java的未来：模块化及其他”。在她演讲之前的这段时间发生了很多事情，其中最为引人瞩目的就是5月8号针对JSR 376的投票事件。</p> <i>By Michael Redlich</i> <i> Translated by 薛命灯</i>
---------------
<h1 id="#title_14" >15、FEX 技术周刊 - 2017/06/26</h1>

[http://fex.baidu.com/blog/2017/06/fex-weekly-26//](http://fex.baidu.com/blog/2017/06/fex-weekly-26//)
作者：zhangtao <br> <p>微信搜索『FEX』关注我们的公众号，及时获得最新资讯。</p>

<h2 id="section">深阅读</h2>

<p><strong>Google’s Flutter = React + Java Swing</strong><br />
https://codeburst.io/googles-flutter-react-java-swing-8174c8d9d402<br />
Google has recently announced its new mobile UI framework called Flutter. It allows you to create native-ish mobile apps that run on Android, iOS and Google’s new Fuchsia operating system.</p>

<p><strong>Techniques for decomposing React components</strong><br />
https://medium.com/dailyjs/techniques-for-decomposing-react-components-e8a1081ef5da<br />
React components have a lot of power and flexibility. With so many tools at your disposal, it is incredibly easy for components to grow over time, become bloated and do too much. As with any other kind of programming, adhering to the single responsibility principle not only makes your components easier to maintain, but also allows for greater reuse. However, identifying how to separate the responsibilities of a large React component is not always easy. Here are three techniques to get you started, from the simplest to most advanced.</p>

<p><strong>webpack 3: Official Release!!</strong><br />
https://medium.com/webpack/webpack-3-official-release-15fd2dd8f07b<br />
虽然号称 98% 的用户不受影响，但实际上…</p>

<p><strong>San - 一个传统的MVVM组件框架</strong><br />
http://efe.baidu.com/blog/san-a-traditional-mvvm-component-framework/<br />
百度推出的 MVVM 框架，甚至兼容 IE6. 如果拿车来比喻，我们想造的是一台陆巡。相比轿车甚至多数SUV，它没有那么好开，看不到很多 2.0T 的车尾灯；相比牧马人和 benz G，他越野能力和通过性也没那么强。但是它很可靠，能稳稳当当、舒适地带你到任何想去的地方。</p>

<p><strong>如何理解Heroku提出的12要素应用</strong><br />
http://mp.weixin.qq.com/s?__biz=MzA5Nzc4OTA1Mw==&amp;mid=2659599357&amp;idx=1&amp;sn=50146645d8c1d1ee7135ee8a0115364d<br />
由公有云 PaaS 的先驱 Heroku 于 2012 年提出（[原文参见 ），目的是告诉开发者如何利用云平台提供的便利来开发更具可靠性和扩展性、更加易于维护的云原生应用。距离 12 原则的提出已有五年之久，12 原则的有些细节可能已经不那么跟得上时代，也有人批评 12 原则的提出从一开始就有过于依赖 Heroku 自身特性的倾向，不过不管怎么说，12 原则依旧是业界最为系统的云原生应用开发指南，我们可以把它作为一个非常有力的参考，但是也千万不要教条。</p>

<p><strong>靠谱程序员必备技能——重构</strong><br />
http://mp.weixin.qq.com/s?__biz=MzIyNjE4NjI2Nw==&amp;mid=2652558943&amp;idx=1&amp;sn=1516afcf876b9fb4a17ce048c5ade58d<br />
敏捷软件开发的十二条原则中有一条是：我们始终拥抱需求变化，哪怕是在软件开发的后期。为了达到这种状态，我们就要在开发过程中持续地优化代码。而重构这项技术，为我们提供了一种更可控的方式来优化代码。附：.</p>

<p><strong>大前端公共知识梳理：这些知识你都掌握了吗</strong><br />
http://mp.weixin.qq.com/s?__biz=MzIwNjQwMzUwMQ==&amp;mid=2247485277&amp;idx=1&amp;sn=82703e13febb1e7947cc18d1f57fc375<br />
随着移动化联网浪潮的汹涌而来与浏览器性能的提升，iOS、Android、Web 等前端开发技术各领风骚，大前端的概念也日渐成为某种共识。虽然具体的代码实现、使用的技术不同，但是 Android、iOS 以及 Web 乃至于 React Native 等开发中，我们需要解决的问题、能够用到的架构设计模式都是可以相互借鉴的。
在我们从某个领域迁移到其他领域时，我们能很方便地知道应该学习些什么，不同的技术、工具他们的职责是什么，应该选择怎样的架构或者设计模式。</p>

<p><strong>如何使用JavaScript构建机器学习模型</strong><br />
https://www.jiqizhixin.com/articles/e2a4be9d-4b00-48d5-bccf-cc5a3582dd9b<br />
JavaScript？我不是应该使用 Python 吗？甚至 Scikit-learn 在 JavaScript 上都不工作。这是可能的，实际上，连我自己都惊讶于开发者对此忽视的态度。就 Scikit-learn 而言，Javascript 的开发者事实上已经推出了适用的库，它会在本文中有所提及。那么，让我们看看 Javascript 在机器学习上能够做什么吧。</p>

<p><strong>2017年Android百大框架排行榜</strong><br />
http://www.cnblogs.com/jincheng-yangchaofan/articles/7018780.html<br />
榜单排序依据：1.项目开源 2.github上该项目的star个数 3.开发团队、作者的实力</p>

<p><strong>美团点评酒店后台故障演练系统</strong><br />
http://tech.meituan.com/thrifycopy_and_faultdrill_system.html<br />
套常态化的“故障演练”机制与工具来反复验证，可以确保服务能在正常情形下表现出正常的行为，在异常状况下，也要有正确、可控的表现。这个服务或是工具能执行：容量与性能评估；故障演练，进而进行依赖梳理、预案验证，保证服务柔性可用。这样才能够做到在节假日与大促时心中有数，在提高系统服务能力的同时增加开发人员应对与处理故障的经验。下面，以酒店后台switch研发组开发的“Faultdrill”系统为例，向大家介绍一下我们在这方面的经验。</p>

<p><strong>An inside look at Quantum DOM Scheduling</strong><br />
https://hacks.mozilla.org/2017/06/an-inside-look-at-quantum-dom-scheduling/<br />
Quantum DOM: Scheduling is a significant piece of Project Quantum, which focuses on making Firefox more responsive, especially when lots of tabs are open. In this article, we’ll describe problems we identified in multi-tab browsing, the solutions we figured out, the current status of Quantum DOM, and opportunities for contribution to the project. 另附：</p>

<p><strong>A new approach to text rendering</strong><br />
http://blog.atom.io/2017/06/22/a-new-approach-to-text-rendering.html<br />
In Atom 1.19, we’re landing a complete rewrite of the text editor’s DOM interaction layer that improves rendering performance and simplifies the code. Prompted by the availability of some valuable new DOM APIs with the upgrade to Electron 1.6, we decided to start over from the beginning and take a critical look at the structure and performance every aspect of our DOM interaction.</p>

<p><strong>Connect: behind the front-end experience</strong><br />
https://stripe.com/blog/connect-front-end-experience<br />
In this blog post, we’ll describe how we used several next-generation web technologies to bring Connect to life, and walk through some of the finer technical details (and excitement!) on our front-end journey.</p>

<p><strong>ES2017’s async/await is the best thing to ever happen to JavaScript</strong><br />
https://certsimple.com/blog/javascript-equals-async-await<br />
Eventually I began understanding the idea of functions as values, that could be written inline, and passed to other functions as options. A callback was essentially a ‘what to do next’ action. I understood callbacks, and learned common async patterns. I liked learning a lot about functions, scope, and closures. I used, but never liked callbacks: a nagging doubt said this is the VMs job, not the programmers.</p>

<p><strong>Intern and JavaScript Testing in 2017</strong><br />
https://www.sitepen.com/blog/2017/06/22/intern-and-javascript-testing-in-2017/<br />
 was created to alleviate this problem and to provide a solid glue architecture for testing applications using JavaScript and various asynchronous patterns such as Promises. Intern has certainly helped us and our users test their applications far more efficiently than was previously possible. As the world of JavaScript evolved, though, we noticed that writing quality tests was getting more difficult.</p>

<p><strong>What Does a Well-Documented CSS Codebase Look Like?</strong><br />
https://css-tricks.com/well-documented-css-codebase-look-like/<br />
A well-documented CSS codebase enforces consistency, boosts maintainability, and helps the team to build a shared vocabulary. So, here we go! Let’s examine the 4 big signs of a well-documented CSS codebase: CSS Tech Stack &amp; Toolchain; CSS Conventions; CSS Architecture; CSS Component Descriptions and Examples.</p>

<p><strong>Functional programming in Javascript is an antipattern</strong><br />
https://medium.com/@alexdixon/functional-programming-in-javascript-is-an-antipattern-58526819f21e<br />
I’m going out on a limb and calling functional programming in Javascript an antipattern. It’s an attractive path that gives way to a maze. It seems to solve some problems but ends up creating more. More importantly, those problems appear to have no higher-level solution that can prevent me from having to deal with them over and over again.</p>

<p><strong>The State of Angular and the Due Date of Version 5</strong><br />
https://hackernoon.com/the-state-of-angular-and-the-due-date-of-version-5-68374002267f<br />
In this article, we will take a high level overview of the 4.x.x versions, see the scheduling of the upcoming versions, discover the due date of the new Angular baby — Version 5, and we will review on two more surprises that are provided by Angular.</p>

<p><strong>JavaScript for Microcontrollers and IoT</strong><br />
https://auth0.com/blog/javascript-for-microcontrollers-and-iot-part-1/<br />
The low-end nature of certain microcontroller platforms makes it somewhat difficult for beginners to use JavaScript. In this post we will take a brief look at the different options for running JavaScript on small devices, and we will also pick one of them and get one JavaScript engine running on it.</p>

<p><strong>Site Speed Monitoring in A/B Testing and Feature Ramp-up</strong><br />
https://engineering.linkedin.com/blog/2017/06/site-speed-monitoring-in-a-b-testing-and-feature-ramp-up<br />
Predicting site speed impact of a feature rollout is a difficult engineering problem, particularly at scale. We are ramping hundreds of changes simultaneously through A/B testing. When ramping a feature into production, how can developers gain visibility into the site speed impact? Likewise, when a performance optimization is enabled in production, how can the developer quantify the benefit? In addition, how can performance degradation be detected at an early stage of feature ramp-up, before the impact spreads out to a larger audience? In this blog, we share our experiences and solutions here at LinkedIn.</p>

<p><strong>Evolution of Dropbox’s Edge Network</strong><br />
https://blogs.dropbox.com/tech/2017/06/evolution-of-dropboxs-edge-network/<br />
Since launching  last year, we’ve been storing and serving more than 90 percent of our users’ data on our own custom-built infrastructure, which has helped us to be more efficient and improved performance for our users globally.</p>

<p><strong>Content Popularity for Open Connect</strong><br />
https://medium.com/netflix-techblog/content-popularity-for-open-connect-b86d56f613b<br />
There are many reasons why Netflix cares about the popularity of our TV shows and movies. On the Open Connect Content Delivery team, we predict content popularity to maximize our infrastructure efficiency. From the Content Delivery perspective, we view popularity as the number of times a piece of content is watched. We compute it by dividing total bytes streamed from this asset by the size in bytes of the asset.</p>

<p><strong>Designing The Perfect Accordion</strong><br />
https://www.smashingmagazine.com/2017/06/designing-perfect-accordion-checklist/<br />
Design patterns can be extremely helpful, mostly because they save time and get us better results, faster. This series of articles is a summary of observations and experiments made throughout the time. Tighten up your seat belts: in this new series of articles on SmashingMag, we’ll look into examples of everything from carousels to filters, calculators, charts, timelines, maps, multi-column tables, almighty pricing plans all the way to seating selection in airline and cinema websites. But before we head off to complex interface problems, let’s start with something seemingly simple and obvious: an accordion.</p>

<p><strong>10 Tips On Typography in Web Design</strong><br />
https://uxplanet.org/10-tips-on-typography-in-web-design-13a378f4aa0d<br />
More than 95% percent of information on the web is in the form of written language. Good typography makes the act of reading effortless, while poor typography turns users off. Optimizing typography is optimizing readability, accessibility, usability(!), overall graphic balance. In this article, I will provide a set of rules that help you improve readability and legibility of your text content.</p>

<p><strong>Tabs, spaces and your salary - how is it really?</strong><br />
http://evelinag.com/blog/2017/06-20-stackoverflow-tabs-spaces-and-salary/index.html#.WU31cmQw2gw<br />
This blog post is my attempt to shed some light into the issue. The original article encouraged people to explore the data for themselves and this is precisely what I did. So I’d like to invite you to follow me through a little data science detective story and a deep dive into the data from the Stack Overflow survey. You’ll see that tabs and spaces are not what they seem. Spoiler: your salary has more to do with the type of company and the environment you work in rather than what type of indentation you use.</p>

<p><strong>Why use SemVer?</strong><br />
http://blog.npmjs.org/post/162134793605/why-use-semver<br />
npm’s documentation recommends that you use semantic versioning, which we also call semver, but it doesn’t explain why you’d use SemVer in the first place. This post is a quick overview of SemVer and why it’s a good idea.</p>

<h2 id="section-1">新鲜货</h2>

<p><strong>Mikeal Rogers: Node.js Will Overtake Java Within a Year</strong><br />
https://thenewstack.io/open-source-profile-mikeal-rogers-node-js/<br />
Mikeal Rogers has been with the Node.js Foundation since day one. Rogers’ main contribution, though, is organization and coordination within the Node.js open source community — particularly in scaling governance and processes as the project has accelerated from a dozen early contributors to many hundreds. Rogers spoke with The New Stack to talk about his experience getting started in the open source world, working at the Node.js Foundation and becoming an open source governance principals guru.</p>

<p><strong>Cell</strong><br />
https://github.com/intercellular/cell<br />
A self-constructing web app framework powered by a self-driving DOM. Cell has one and only one design goal: Easy.</p>

<p><strong>Spected</strong><br />
https://github.com/25th-floor/spected<br />
Spected is a low level validation library for validating objects against defined validation rules. Framework specific validation libraries can be built upon spected, leveraging the spected appraoch of separating the speciific input from any validation. Furthermore it can be used to verify the validity deeply nested objects, f.e. server side validation of data or client side validation of JSON objects. Spected can also be used to validate Form inputs etc.</p>

<p><strong>Flight - The best way to build animation compositions for React</strong><br />
https://github.com/jondot/react-flight<br />
Design and compose a component to start with, a component to end with, and Flight will take it from there. Flight tries to be for React what Principle is for Sketch compositions - the fastest, most friction free way to compose and an effortless way to animate an idea, an interaction, or a short movie-like composition in a self-contained widget (a React component after all).</p>

<p><strong>Flexible date picker for React</strong><br />
https://github.com/gpbl/react-day-picker<br />
no dependencies – fully customizable – ARIA support – localizable – less than 10KB</p>

<p><strong>Grid Styled</strong><br />
https://github.com/jxnblk/grid-styled<br />
Responsive React grid system built with styled-components.</p>

<p><strong>Stardust: GPU-based Visualization Library</strong><br />
https://stardustjs.github.io/<br />
Stardust is a library for rendering information visualizations with GPU (WebGL). Stardust provides an easy-to-use and familiar API for defining marks and binding data to them. With Stardust, you can render tens of thousands of markers and animate them in real time without the hassle of managing WebGL shaders and buffers.</p>

<p><strong>Luna</strong><br />
http://www.luna-lang.org/<br />
Visual and textual functional programming language with a focus on productivity, collaboration and development ergonomics.</p>

<p><strong>Animate.css</strong><br />
https://daneden.github.io/animate.css/<br />
Just-add-water CSS animations. 另附：.</p>

<p><strong>mini.css</strong><br />
http://minicss.org/<br />
mini.css is a lightweight CSS framework (under 7KB gzipped) designed with mobile devices and modern browsers in mind. Responsiveness, ease of use and customization are some of the main features of the framework, while accessibility and extensive documentation are some of the secondary focuses of the project. The framework is written using Sass, while most of its components are based on Flexbox.</p>

<p><strong>AlloyTeam正式发布pasition</strong><br />
https://alloyteam.github.io/pasition/<br />
Pasition - Path Transition with little JS code, render to anywhere. 类似的库 https://github.com/veltman/flubber</p>

<p><strong>Redbird Reverse Proxy</strong><br />
https://github.com/OptimalBits/redbird<br />
Handling dynamic virtual hosts, load balancing, proxying web sockets and SSL encryption should be easy and robust. With redbird you get a complete library to build dynamic reverse proxies with the speed and robustness of http-proxy. This light-weight package includes everything you need for easy reverse routing of your applications. Great for routing many applications from different domains in one single host, handling SSL with ease, etc.</p>

<p><strong>JSON Server</strong><br />
https://github.com/typicode/json-server<br />
Get a full fake REST API with zero coding in less than 30 seconds (seriously). Created with &lt;3 for front-end developers who need a quick back-end for prototyping and mocking.</p>

<p><strong>Syntax Highlighting as a Service</strong><br />
https://photon.sh/<br />
Photon is a powerful, multiplatform, highly customizable and free syntax highlighter for the modern web.</p>

<p><strong>Get Ready for Web Bluetooth!</strong><br />
http://developer.telerik.com/content-types/tutorials/get-ready-web-bluetooth/<br />
With the new Web Bluetooth API now available in Chrome Browsers 56+ and Opera 44+, as well as more recent Android browsers, the world of connected devices just got a little closer to realizing the promise of the Physical Web: “Walk up and use anything”.</p>

<p><strong>Easy Machine Learning</strong><br />
https://github.com/ICT-BDA/EasyML<br />
中科院开源的机器学习系统</p>

<p><strong>Origami anything</strong><br />
http://news.mit.edu/2017/algorithm-origami-patterns-any-3-D-structure-0622<br />
New algorithm generates practical paper-folding patterns to produce any 3-D structure.</p>

<p><strong>Codemod</strong><br />
https://github.com/facebook/codemod<br />
Codemod is a tool/library to assist you with large-scale codebase refactors that can be partially automated but still require human oversight and occasional intervention. Codemod was developed at Facebook and released as open source. 附介绍：.</p>

<p><strong>vue-table-component</strong>  <br />
https://github.com/spatie/vue-table-component<br />
A Vue component that can render a filterable and sortable table. It aims to be very lightweight and easy to use.</p>

<p><strong>Practical Node.js Book, 2nd Edition, Open-Sourced on GitHub</strong><br />
https://www.kickstarter.com/projects/azat/practical-nodejs-book-2nd-edition-open-sourced-on<br />
Making Practical Node.js current is a worthwhile aim but it’s not enough. The plan is to write it on GitHub, where you can follow along, comment, give me feedback, and through this collaboration I can ensure that the 2nd edition of Practical Node.js is even better than the first.</p>

<h2 id="section-2">产品及其它</h2>

<p><strong>Why we’re betting against real-time team messaging</strong><br />
https://blog.doist.com/why-were-betting-against-real-time-team-messaging-521804a3da09<br />
This post is the story of why we stopped using Slack. It’s also the story of how we had the (possibly) crazy idea that we could contribute something fundamentally different to an already cluttered team communication market - . Something for teams like ours with the audacity to think that maybe there’s more to work than keeping up with group chat…</p>

<p><strong>贝佐斯的独特思维是什么</strong><br />
http://mp.weixin.qq.com/s?__biz=MzA5ODMzMDkzOA==&amp;mid=2661082003&amp;idx=1&amp;sn=59b74d10aafcd29a08193fa8c9de233d<br />
贝佐斯管理哲学中的“逆向工作法”直击事物本质。大概也正因为此智慧，让贝佐斯超越巴菲特，成为全球的第二大富豪。学习贝佐斯“逆向工作法”，更重要的是可以将此运用到自己的工作和生活中。</p>

<p><strong>2017年度最具商业价值人工智能公司TOP50</strong><br />
http://www.iheima.com/zixun/2017/0624/163769.shtml<br />
我们评选出的50个项目只是对当前人工智能技术应用现状的一个极小的缩影。由于处于技术研发期以及其他原因，还有部分项目不便对外曝光。而由于时间和获取渠道等各种原因的限制，也有众多的项目并未参与本次评选。而这些入选者，也是在人工智能领域中起步不久的新秀。在未来，我们还将见证它们的成长，以及看到更多的革命性的技术和研究涌现，更多的行业应用爆发和改变。</p>

<p><strong>对话王兴：太多人关注边界，而不关注核心</strong><br />
http://mp.weixin.qq.com/s?__biz=MzA3NDI0ODMzMw==&amp;mid=2651302476&amp;idx=1&amp;sn=c9f183fc410db9b9f45e49010be7eb79<br />
在中国互联网中，美团是一家特殊的公司。大量公司是从垂直领域开始成长，然后不断延展，所以他们难免由行业思维出发，更多去思考终局和边界。而美团点评是用商业流转中的一个环节来作为自己的内核——这个内核从商业上看，是交易；从客户看，是服务。它的业务是横向的，所以王兴的思考和多数CEO不太一样，他更多通用的、跨界的思考。比如他对业务和竞争的看法，他认为不要期望一家独大，也不要期望结束战争，所有人都要接受竞合才是新常态，同时，他认为太多思考边界和终局是错误的，“哪有什么真正的终局？”附：</p>

<p><strong>马云美国一小时英文演讲实录：错过中国，你就错过了未来</strong><br />
http://www.toutiao.com/i6434698496976093697/<br />
作为小企业，你没有什么可失去，你唯一要焦虑的就是失去机会。错过互联网商业，错过中国，你就错过了未来。未来20年让我们打造一个体系，帮助中小企业实现更加自由便利的贸易。这就是为什么我过去一年飞行了870小时，会见了超过40位国家元首和政府高层，今年我会飞行超过1000个小时。如果我们相信，就要让它实现！</p>

<p><strong>华为离职副总裁徐家骏-工作感悟</strong><br />
http://www.yixieshi.com/86188.html<br />
非常值得学习：从小事做起，学会吃亏，与他人合作；勇于实践，勇于犯错，善于反思；独立思考，不人云亦云；对职业负责、对目标负责，对自己负责，成功者往往自觉自律、信守承诺、心无旁骛；要有方法、有套路，对问题系统思考、对解决方案有战略性的设计；少抱怨、少空谈、积极主动，多干实事；关注人，帮助人，真诚待人，厚道做人；</p>

<p>– THE END –</p>
---------------
<h1 id="#title_15" >16、Left-Handed Brush Lettering: How To Get Started</h1>
Alma Hoffmann
[https://www.smashingmagazine.com/2017/06/left-handed-brush-lettering/](https://www.smashingmagazine.com/2017/06/left-handed-brush-lettering/)
<table width="650">
	<tr>
		<td width="650">
			<div style="width:650px;">
				<img src="http://statisches.auslieferung.commindo-media-ressourcen.de/advertisement.gif" alt="" border="0"/>
				<br/>
				<a href="http://auslieferung.commindo-media-ressourcen.de/random.php?mode=target&collection=smashing-rss&position=1" target="_blank">
					<img src="http://auslieferung.commindo-media-ressourcen.de/random.php?mode=image&collection=smashing-rss&position=1" border="0" alt=""/>
				</a>
				&nbsp;
				<a href="http://auslieferung.commindo-media-ressourcen.de/random.php?mode=target&collection=smashing-rss&position=2" target="_blank">
					<img src="http://auslieferung.commindo-media-ressourcen.de/random.php?mode=image&collection=smashing-rss&position=2" border="0" alt=""/>
				</a>
				&nbsp;
				<a href="http://auslieferung.commindo-media-ressourcen.de/random.php?mode=target&collection=smashing-rss&position=3" target="_blank">
					<img src="http://auslieferung.commindo-media-ressourcen.de/random.php?mode=image&collection=smashing-rss&position=3" border="0" alt=""/>
				</a>
			</div>
		</td>
	</tr>
</table><p>Lettering and calligraphy are quickly becoming desired skills in a designer's toolbox. Designers such as Marian Bantjes, Jessica Hische, Sean Wes and Martina Flor, just to name a few, have become not only an inspiration to the rest of us, but also a standard.</p>

<figure></figure>

<p>Their work is not only client-based; they have become their own brand by providing products to their followers as well. Other designers have followed suit, and now it would seem that lettering and calligraphy are everywhere.</p><p>The post .</p>
---------------