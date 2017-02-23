## 文章索引
1、 <a href="#1视频访谈-吕慧伟推荐系统的请求量飞速增长同时兼顾稳定性" >视频访谈： 吕慧伟：推荐系统的请求量飞速增长，同时兼顾稳定性</a><br/>
2、 <a href="#2函数式编程入门教程" >函数式编程入门教程</a><br/>
3、 <a href="#3文章-docker引领测试革新" >文章： Docker引领测试革新</a><br/>
4、 <a href="#4文章-在kubernetes上用paddlepaddle运行深度学习" >文章： 在Kubernetes上用PaddlePaddle运行深度学习</a><br/>
5、 <a href="#5视频演讲-蚂蚁金服在大数据合作上的创新实践" >视频演讲： 蚂蚁金服在大数据合作上的创新实践</a><br/>
6、 <a href="#6文章-beehive一次ios模块化解耦实践" >文章： BeeHive，一次iOS模块化解耦实践</a><br/>
7、 <a href="#7视频演讲-聚划算无线的插件化生存之道" >视频演讲： 聚划算无线的插件化生存之道</a><br/>
8、 <a href="#8google-cloud-endpoints正式发布" >Google Cloud Endpoints正式发布</a><br/>
9、 <a href="#9微软airsim一个无人机和机器人的模拟器" >微软AirSim，一个无人机和机器人的模拟器</a><br/>
10、 <a href="#10如何提升员工的工作积极性" >如何提升员工的工作积极性</a><br/>
11、 <a href="#11微服务的未来功能性服务设计和可观测性" >微服务的未来：功能性服务设计和可观测性</a><br/>
12、 <a href="#12how-to-use-shadows-and-blur-effects-in-modern-ui-design" >How To Use Shadows And Blur Effects In Modern UI Design</a><br/><h1 id="#title_0" >1、视频访谈： 吕慧伟：推荐系统的请求量飞速增长，同时兼顾稳定性</h1>
吕慧伟
[http://www.infoq.com/cn/interviews/interview-with-lvhuiwei-talk-recommendation-system?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/interviews/interview-with-lvhuiwei-talk-recommendation-system?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/interviews/interview-with-lvhuiwei-talk-recommendation-system/zh/mediumimage/lvhuiwei270.jpg"/><p>腾讯云的吕慧伟老师给我们介绍了腾讯云推荐引擎的一些基本情况，包括它的目的和技术沉淀、演进的过程，还有推荐系统的应用场景，分享了重构实时计算系统时遇到的困难和解决办法，最后分享了未来的发展方向和下一个技术攻坚点
</p> <i>By 吕慧伟</i>
---------------
<h1 id="#title_1" >2、函数式编程入门教程</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2017/02/fp-tutorial.html](http://www.ruanyifeng.com/blog/2017/02/fp-tutorial.html)
<p>你可能听说过函数式编程（Functional programming），甚至已经使用了一段时间。</p>

        <p>但是，你能说清楚，它到底是什么吗？</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017022201.jpg" alt="" title="" /></p>

<p>网上搜索一下，你会轻松找到好多答案。</p>

<blockquote>
  <ul>
<li>与面向对象编程（Object-oriented programming）和过程式编程（Procedural programming）并列的编程范式。</li>
<li>最主要的特征是，函数是。</li>
<li>强调将计算过程分解成可复用的函数，典型例子就是<code>map</code>方法和<code>reduce</code>方法组合而成 。</li>
<li>只有的函数，才是合格的函数。</li>
</ul>
</blockquote>

<p>上面这些说法都对，但还不够，都没有回答下面这个更深层的问题。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017022202.jpg" alt="" title="" /></p>

<blockquote>
  <p><strong>为什么要这样做？</strong></p>
</blockquote>

<p>这就是，本文要解答的问题。我会通过最简单的语言，帮你理解函数式编程，并且学会它那些基本写法。</p>

<p>需要声明的是，我不是专家，而是一个初学者，最近两年才真正开始学习函数式编程。一直苦于看不懂各种资料，立志要写一篇清晰易懂的教程。下面的内容肯定不够严密，甚至可能包含错误，但是我发现，像下面这样解释，初学者最容易懂。</p>

<p>另外，本文比较长，阅读时请保持耐心。结尾还有 的推广，非常感谢他们对本文的赞助。</p>

<h2>一、范畴论</h2>

<p>函数式编程的起源，是一门叫做范畴论（Category Theory）的数学分支。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017022205.jpg" alt="" title="" /></p>

<p>理解函数式编程的关键，就是理解范畴论。它是一门很复杂的数学，认为世界上所有的概念体系，都可以抽象成一个个的"范畴"（category）。</p>

<h3>1.1 范畴的概念</h3>

<p>什么是范畴呢？</p>

<p>的一句话定义如下。</p>

<blockquote>
  <p>"范畴就是使用箭头连接的物体。"（In mathematics, a category is an algebraic structure that comprises "objects" that are linked by "arrows". ）</p>
</blockquote>

<p>也就是说，彼此之间存在某种关系的概念、事物、对象等等，都构成"范畴"。随便什么东西，只要能找出它们之间的关系，就能定义一个"范畴"。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017022210.jpg" alt="" title="" /></p>

<p>上图中，各个点与它们之间的箭头，就构成一个范畴。</p>

<p>箭头表示范畴成员之间的关系，正式的名称叫做"态射"（morphism）。范畴论认为，同一个范畴的所有成员，就是不同状态的"变形"（transformation）。通过"态射"，一个成员可以变形成另一个成员。</p>

<h3>1.2 数学模型</h3>

<p>既然"范畴"是满足某种变形关系的所有对象，就可以总结出它的数学模型。</p>

<blockquote>
  <ul>
<li>所有成员是一个集合</li>
<li>变形关系是函数</li>
</ul>
</blockquote>

<p>也就是说，范畴论是集合论更上层的抽象，简单的理解就是"集合 + 函数"。</p>

<p>理论上通过函数，就可以从范畴的一个成员，算出其他所有成员。</p>

<h3>1.3 范畴与容器</h3>

<p>我们可以把"范畴"想象成是一个容器，里面包含两样东西。</p>

<blockquote>
  <ul>
<li>值（value）</li>
<li>值的变形关系，也就是函数。</li>
</ul>
</blockquote>

<p>下面我们使用代码，定义一个简单的范畴。</p>

<blockquote><pre><code class="language-javascript">
class Category {
  constructor(val) { 
    this.val = val; 
  }

  addOne(x) {
    return x + 1;
  }
}
</code></pre></blockquote>

<p>上面代码中，<code>Category</code>是一个类，也是一个容器，里面包含一个值（<code>this.val</code>）和一种变形关系（<code>addOne</code>）。你可能已经看出来了，这里的范畴，就是所有彼此之间相差<code>1</code>的数字。</p>

<p>注意，本文后面的部分，凡是提到"容器"的地方，全部都是指"范畴"。</p>

<h3>1.4 范畴论与函数式编程的关系</h3>

<p>范畴论使用函数，表达范畴之间的关系。</p>

<p>伴随着范畴论的发展，就发展出一整套函数的运算方法。这套方法起初只用于数学运算，后来有人将它在计算机上实现了，就变成了今天的"函数式编程"。</p>

<p><strong>本质上，函数式编程只是范畴论的运算方法，跟数理逻辑、微积分、行列式是同一类东西，都是数学方法，只是碰巧它能用来写程序。</strong></p>

<p>所以，你明白了吗，为什么函数式编程要求函数必须是纯的，不能有副作用？因为它是一种数学运算，原始目的就是求值，不做其他事情，否则就无法满足函数运算法则了。</p>

<p>总之，在函数式编程中，函数就是一个管道（pipe）。这头进去一个值，那头就会出来一个新的值，没有其他作用。</p>

<h2>二、函数的合成与柯里化</h2>

<p>函数式编程有两个最基本的运算：合成和柯里化。</p>

<h3>2.1 函数的合成</h3>

<p>如果一个值要经过多个函数，才能变成另外一个值，就可以把所有中间步骤合并成一个函数，这叫做"函数的合成"（compose）。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017022204.png" alt="" title="" /></p>

<p>上图中，<code>X</code>和<code>Y</code>之间的变形关系是函数<code>f</code>，<code>Y</code>和<code>Z</code>之间的变形关系是函数<code>g</code>，那么<code>X</code>和<code>Z</code>之间的关系，就是<code>g</code>和<code>f</code>的合成函数<code>g·f</code>。</p>

<p>下面是合成两个函数的简单代码。</p>

<blockquote><pre><code class="language-javascript">
const compose = function (f, g) {
  return function (x) {
    return f(g(x));
  };
}
</code></pre></blockquote>

<p>函数的合成还必须满足结合律。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017022209.png" alt="" title="" /></p>

<blockquote><pre><code class="language-javascript">
compose(f, compose(g, h))
// 等同于
compose(compose(f, g), h)
// 等同于
compose(f, g, h)
</code></pre></blockquote>

<p>合成也是函数必须是纯的一个原因。因为一个不纯的函数，怎么跟其他函数合成？怎么保证各种合成以后，它会达到预期的行为？</p>

<p>前面说过，函数就像数据的管道（pipe）。那么，函数合成就是将这些管道连了起来，让数据一口气从多个管道中穿过。</p>

<h3>2.2 柯里化</h3>

<p><code>f(x)</code>和<code>g(x)</code>合成为<code>f(g(x))</code>，有一个隐藏的前提，就是<code>f</code>和<code>g</code>都只能接受一个参数。如果可以接受多个参数，比如<code>f(x, y)</code>和<code>g(a, b, c)</code>，函数合成就非常麻烦。 </p>

<p>这时就需要函数柯里化了。所谓"柯里化"，就是把一个多参数的函数，转化为单参数函数。</p>

<blockquote><pre><code class="language-javascript">
// 柯里化之前
function add(x, y) {
  return x + y;
}

add(1, 2) // 3

// 柯里化之后
function addX(y) {
  return function (x) {
    return x + y;
  };
}

addX(2)(1) // 3
</code></pre></blockquote>

<p>有了柯里化以后，我们就能做到，所有函数只接受一个参数。后文的内容除非另有说明，都默认函数只有一个参数，就是所要处理的那个值。</p>

<h2>三、函子</h2>

<p>函数不仅可以用于同一个范畴之中值的转换，还可以用于将一个范畴转成另一个范畴。这就涉及到了函子（Functor）。</p>

<h3>3.1 函子的概念</h3>

<p>函子是函数式编程里面最重要的数据类型，也是基本的运算单位和功能单位。</p>

<p>它首先是一种范畴，也就是说，是一个容器，包含了值和变形关系。<strong>比较特殊的是，它的变形关系可以依次作用于每一个值，将当前容器变形成另一个容器。</strong></p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017022203.png" alt="" title="" /></p>

<p>上图中，左侧的圆圈就是一个函子，表示人名的范畴。外部传入函数<code>f</code>，会转成右边表示早餐的范畴。</p>

<p>下面是一张更一般的图。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017022211.jpg" alt="" title="" /></p>

<p>上图中，函数<code>f</code>完成值的转换（<code>a</code>到<code>b</code>），将它传入函子，就可以实现范畴的转换（<code>Fa</code>到<code>Fb</code>）。</p>

<h3>3.2 函子的代码实现</h3>

<p>任何具有<code>map</code>方法的数据结构，都可以当作函子的实现。</p>

<blockquote><pre><code class="language-javascript">
class Functor {
  constructor(val) { 
    this.val = val; 
  }

  map(f) {
    return new Functor(f(this.val));
  }
}
</code></pre></blockquote>

<p>上面代码中，<code>Functor</code>是一个函子，它的<code>map</code>方法接受函数<code>f</code>作为参数，然后返回一个新的函子，里面包含的值是被<code>f</code>处理过的（<code>f(this.val)</code>）。</p>

<p><strong>一般约定，函子的标志就是容器具有<code>map</code>方法。该方法将容器里面的每一个值，映射到另一个容器。</strong></p>

<p>下面是一些用法的示例。</p>

<blockquote><pre><code class="language-javascript">
(new Functor(2)).map(function (two) {
  return two + 2;
});
// Functor(4)

(new Functor('flamethrowers')).map(function(s) {
  return s.toUpperCase();
});
// Functor('FLAMETHROWERS')

(new Functor('bombs')).map(_.concat(' away')).map(_.prop('length'));
// Functor(10)
</code></pre></blockquote>

<p>上面的例子说明，函数式编程里面的运算，都是通过函子完成，即运算不直接针对值，而是针对这个值的容器----函子。函子本身具有对外接口（<code>map</code>方法），各种函数就是运算符，通过接口接入容器，引发容器里面的值的变形。</p>

<p>因此，<strong>学习函数式编程，实际上就是学习函子的各种运算。</strong>由于可以把运算方法封装在函子里面，所以又衍生出各种不同类型的函子，有多少种运算，就有多少种函子。函数式编程就变成了运用不同的函子，解决实际问题。</p>

<h2>四、of 方法</h2>

<p>你可能注意到了，上面生成新的函子的时候，用了<code>new</code>命令。这实在太不像函数式编程了，因为<code>new</code>命令是面向对象编程的标志。</p>

<p><strong>函数式编程一般约定，函子有一个<code>of</code>方法，用来生成新的容器。</strong></p>

<p>下面就用<code>of</code>方法替换掉<code>new</code>。</p>

<blockquote><pre><code class="language-javascript">
Functor.of = function(val) {
  return new Functor(val);
};
</code></pre></blockquote>

<p>然后，前面的例子就可以改成下面这样。</p>

<blockquote><pre><code class="language-javascript">
Functor.of(2).map(function (two) {
  return two + 2;
});
// Functor(4)
</code></pre></blockquote>

<p>这就更像函数式编程了。</p>

<h2>五、Maybe 函子</h2>

<p>函子接受各种函数，处理容器内部的值。这里就有一个问题，容器内部的值可能是一个空值（比如<code>null</code>），而外部函数未必有处理空值的机制，如果传入空值，很可能就会出错。</p>

<blockquote><pre><code class="language-javascript">
Functor.of(null).map(function (s) {
  return s.toUpperCase();
});
// TypeError
</code></pre></blockquote>

<p>上面代码中，函子里面的值是<code>null</code>，结果小写变成大写的时候就出错了。</p>

<p>Maybe 函子就是为了解决这一类问题而设计的。简单说，它的<code>map</code>方法里面设置了空值检查。</p>

<blockquote><pre><code class="language-javascript">
class Maybe extends Functor {
  map(f) {
    return this.val ? Maybe.of(f(this.val)) : Maybe.of(null);
  }
}
</code></pre></blockquote>

<p>有了 Maybe 函子，处理空值就不会出错了。</p>

<blockquote><pre><code class="language-javascript">
Maybe.of(null).map(function (s) {
  return s.toUpperCase();
});
// Maybe(null)
</code></pre></blockquote>

<h2>六、Either 函子</h2>

<p>条件运算<code>if...else</code>是最常见的运算之一，函数式编程里面，使用 Either 函子表达。</p>

<p>Either 函子内部有两个值：左值（<code>Left</code>）和右值（<code>Right</code>）。右值是正常情况下使用的值，左值是右值不存在时使用的默认值。</p>

<blockquote><pre><code class="language-javascript">
class Either extends Functor {
  constructor(left, right) {
    this.left = left;
    this.right = right;
  }

  map(f) {
    return this.right ? 
      Either.of(this.left, f(this.right)) :
      Either.of(f(this.left), this.right);
  }
}

Either.of = function (left, right) {
  return new Either(left, right);
};
</code></pre></blockquote>

<p>下面是用法。</p>

<blockquote><pre><code class="language-javascript">
var addOne = function (x) {
  return x + 1;
};

Either.of(5, 6).map(addOne);
// Either(5, 7);

Either.of(1, null).map(addOne);
// Either(2, null);
</code></pre></blockquote>

<p>上面代码中，如果右值有值，就使用右值，否则使用左值。通过这种方式，Either 函子表达了条件运算。</p>

<p>Either 函子的常见用途是提供默认值。下面是一个例子。</p>

<blockquote><pre><code class="language-javascript">
Either
.of({address: 'xxx'}, currentUser.address)
.map(updateField);
</code></pre></blockquote>

<p>上面代码中，如果用户没有提供地址，Either 函子就会使用左值的默认地址。</p>

<p>Either 函子的另一个用途是代替<code>try...catch</code>，使用左值表示错误。</p>

<blockquote><pre><code class="language-javascript">
function parseJSON(json) {
  try {
    return Either.of(null, JSON.parse(json));
  } catch (e: Error) {
    return Either.of(e, null);
  }
}
</code></pre></blockquote>

<p>上面代码中，左值为空，就表示没有出错，否则左值会包含一个错误对象<code>e</code>。一般来说，所有可能出错的运算，都可以返回一个 Either 函子。</p>

<h2>七、ap 函子</h2>

<p>函子里面包含的值，完全可能是函数。我们可以想象这样一种情况，一个函子的值是数值，另一个函子的值是函数。</p>

<blockquote><pre><code class="language-javascript">
function addTwo(x) {
  return x + 2;
}

const A = Functor.of(2);
const B = Functor.of(addTwo)
</code></pre></blockquote>

<p>上面代码中，函子<code>A</code>内部的值是<code>2</code>，函子<code>B</code>内部的值是函数<code>addTwo</code>。</p>

<p>有时，我们想让函子<code>B</code>内部的函数，可以使用函子<code>A</code>内部的值进行运算。这时就需要用到 ap 函子。</p>

<p>ap 是 applicative（应用）的缩写。凡是部署了<code>ap</code>方法的函子，就是 ap 函子。</p>

<blockquote><pre><code class="language-javascript">
class Ap extends Functor {
  ap(F) {
    return Ap.of(this.val(F.val));
  }
}
</code></pre></blockquote>

<p>注意，<code>ap</code>方法的参数不是函数，而是另一个函子。</p>

<p>因此，前面例子可以写成下面的形式。</p>

<blockquote><pre><code class="language-javascript">
Ap.of(addTwo).ap(Function.of(2))
// Ap(4)
</code></pre></blockquote>

<p>ap 函子的意义在于，对于那些多参数的函数，就可以从多个容器之中取值，实现函子的链式操作。</p>

<blockquote><pre><code class="language-javascript">
function add(x) {
  return function (y) {
    return x + y;
  };
}

Ap.of(add).ap(Maybe.of(2)).ap(Maybe.of(3));
// Ap(5)
</code></pre></blockquote>

<p>上面代码中，函数<code>add</code>是柯里化以后的形式，一共需要两个参数。通过 ap 函子，我们就可以实现从两个容器之中取值。它还有另外一种写法。</p>

<blockquote><pre><code class="language-javascript">
Ap.of(add(2)).ap(Maybe.of(3));
</code></pre></blockquote>

<h2>八、Monad 函子</h2>

<p>函子是一个容器，可以包含任何值。函子之中再包含一个函子，也是完全合法的。但是，这样就会出现多层嵌套的函子。</p>

<blockquote><pre><code class="language-javascript">
Maybe.of(
  Maybe.of(
    Maybe.of({name: 'Mulburry', number: 8402})
  )
)
</code></pre></blockquote>

<p>上面这个函子，一共有三个<code>Maybe</code>嵌套。如果要取出内部的值，就要连续取三次<code>this.val</code>。这当然很不方便，因此就出现了 Monad 函子。</p>

<p><strong>Monad 函子的作用是，总是返回一个单层的函子。</strong>它有一个<code>flatMap</code>方法，与<code>map</code>方法作用相同，唯一的区别是如果生成了一个嵌套函子，它会取出后者内部的值，保证返回的永远是一个单层的容器，不会出现嵌套的情况。</p>

<blockquote><pre><code class="language-javascript">
class Monad extends Functor {
  join() {
    return this.val;
  }
  flatMap(f) {
    return this.map(f).join();
  }
}
</code></pre></blockquote>

<p>上面代码中，如果函数<code>f</code>返回的是一个函子，那么<code>this.map(f)</code>就会生成一个嵌套的函子。所以，<code>join</code>方法保证了<code>flatMap</code>方法总是返回一个单层的函子。这意味着嵌套的函子会被铺平（flatten）。</p>

<h2>九、IO 操作</h2>

<p>Monad 函子的重要应用，就是实现 I/O （输入输出）操作。</p>

<p>I/O 是不纯的操作，普通的函数式编程没法做，这时就需要把 IO 操作写成<code>Monad</code>函子，通过它来完成。</p>

<blockquote><pre><code class="language-javascript">
var fs = require('fs');

var readFile = function(filename) {
  return new IO(function() {
    return fs.readFileSync(filename, 'utf-8');
  });
};

var print = function(x) {
  return new IO(function() {
    console.log(x);
    return x;
  });
}
</code></pre></blockquote>

<p>上面代码中，读取文件和打印本身都是不纯的操作，但是<code>readFile</code>和<code>print</code>却是纯函数，因为它们总是返回 IO 函子。</p>

<p>如果 IO 函子是一个<code>Monad</code>，具有<code>flatMap</code>方法，那么我们就可以像下面这样调用这两个函数。</p>

<blockquote><pre><code class="language-javascript">
readFile('./user.txt')
.flatMap(print)
</code></pre></blockquote>

<p>这就是神奇的地方，上面的代码完成了不纯的操作，但是因为<code>flatMap</code>返回的还是一个 IO 函子，所以这个表达式是纯的。我们通过一个纯的表达式，完成带有副作用的操作，这就是 Monad 的作用。</p>

<p>由于返回还是 IO 函子，所以可以实现链式操作。因此，在大多数库里面，<code>flatMap</code>方法被改名成<code>chain</code>。</p>

<blockquote><pre><code class="language-javascript">
var tail = function(x) {
  return new IO(function() {
    return x[x.length - 1];
  });
}

readFile('./user.txt')
.flatMap(tail)
.flatMap(print)

// 等同于
readFile('./user.txt')
.chain(tail)
.chain(print)
</code></pre></blockquote>

<p>上面代码读取了文件<code>user.txt</code>，然后选取最后一行输出。</p>

<h2>十、参考链接</h2>

<ul>
<li></li>
<li></li>
<li></li>
<li></li>
<li></li>
</ul>

<p>（正文完）</p>

<p>=============================================</p>

<p><strong>感谢你读完了全文。下面还有一个推广，请再花一分钟阅读。</strong></p>

<p>去年十月，我。</p>

<p>现在，他们进入中国市场快满周年了，又有一个本地化课程发布了。那就是由 Google 和 Github 合作制作的认证课程。</p>

<p></p>

<p>这个课程完全是国际水准，讲解深入浅出，示例丰富，贴近大公司开发实践，帮助你牢牢掌握那些最实用的前端技术。</p>

<p>课程由硅谷工程师英语讲授，配有全套中文字幕，以及全中文的学习辅导，还有首次引入中国的同步学习小组和导师监督服务，包含一对一的代码辅导。课程通过后，还能拿到 Google、Github 参与颁发的学习认证。</p>

<p></p>

<p>这门课程今天（2月22日）就开始报名了，现在就点击，了解更多。我的读者报名时，请使用优惠码<code>ruanyfFEND</code>。</p>

<p>最后，欢迎立即扫码，关注优达学城（微信号：youdaxue），跟踪最新的 IT 在线学习和培训资讯。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017022208.jpg" alt="" title="" /></p>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2017-02-22T09:00:46+08:00">2017年2月22日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>博客文集：</li>
<li>社交媒体：</li>
<li>Feed订阅： </li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------
<h1 id="#title_2" >3、文章： Docker引领测试革新</h1>
孙远
[http://www.infoq.com/cn/articles/docker-lead-test-innovation?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/docker-lead-test-innovation?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/docker-lead-test-innovation/zh/smallimage/logfsdfsdo.jpg"/><p>随着Docker技术被越来越多的人所认可，其应用的范围也越来越广泛。本文将从测试类型、Devops、自动化测试、测试场景、测试实践等方面介绍Docker对软件测试技术的影响。我假设读者在看这篇文章时已经对Docker和其所依赖的核心技术有了一定的了解。</p> <i>By 孙远</i>
---------------
<h1 id="#title_3" >4、文章： 在Kubernetes上用PaddlePaddle运行深度学习</h1>
Yi Wang,
[http://www.infoq.com/cn/articles/deep-learning-with-paddlepaddle-on-kubernetes?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/deep-learning-with-paddlepaddle-on-kubernetes?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/deep-learning-with-paddlepaddle-on-kubernetes/zh/smallimage/logo-3 (1).jpg"/><p>百度研究院在 Kubernetes 上跑深度学习框架 PaddlePaddle。本文介绍了什么是PaddlePaddle、为什么要在 Kubernetes上运行PaddlePaddle，以及在Kubernetes进行分布式训练和接下来的工作。</p> <i>By Yi Wang,</i> <i> Translated by 冬雨</i>
---------------
<h1 id="#title_4" >5、视频演讲： 蚂蚁金服在大数据合作上的创新实践</h1>
周卫林
[http://www.infoq.com/cn/presentations/innovation-practice-of-antgroup-clothing-in-the-cooperation-of-big-data?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/innovation-practice-of-antgroup-clothing-in-the-cooperation-of-big-data?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/innovation-practice-of-antgroup-clothing-in-the-cooperation-of-big-data/zh/mediumimage/zhouweilin270.jpg"/><p>蚂蚁金服通过大数据创造了不少全新的业务模式和产品体验，比如蚂蚁微贷、运费险和芝麻信用等，促进了业务的极大发展。在多年数据业务化的过程中，我们也深知一家公司无法完全掌握数据业务化的三要素，因此需要提供平台机制和创新技术，发挥出大数据的乘数效应。本次演讲将重点介绍蚂蚁金服在大数据合作上的创新实践，涵盖业务挑战、应用案例和技术实践。</p> <i>By 周卫林</i>
---------------
<h1 id="#title_5" >6、文章： BeeHive，一次iOS模块化解耦实践</h1>
戴鹏
[http://www.infoq.com/cn/articles/beehive-a-ios-modular-decoupling-practice?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/beehive-a-ios-modular-decoupling-practice?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/beehive-a-ios-modular-decoupling-practice/zh/smallimage/logo 112 (5).jpg"/><p>在本文，天猫的戴鹏继续分享了BeeHive的目的，举例说明最佳实践，并且剖析其结构和原理。</p> <i>By 戴鹏</i>
---------------
<h1 id="#title_6" >7、视频演讲： 聚划算无线的插件化生存之道</h1>
金津
[http://www.infoq.com/cn/presentations/juhuasuan-wireless-plug-in-the-survival-of-the-road?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/juhuasuan-wireless-plug-in-the-survival-of-the-road?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/juhuasuan-wireless-plug-in-the-survival-of-the-road/zh/mediumimage/jinjin270.jpg"/><p>聚划算是基于淘宝和天猫生长而出的营销平台，有自己的独立客户端，同时也有天猫和手机淘宝的访问入口，活动多，动态性和实时性要求极高，对于开发团队来说，就需要在维护自己客户端迭代的同时，确保功能高效同步到多个平台；同时需要满足各个业务方随时随地无法预计的各种实时性需求。这就对传统的开发模式和构架提出了极大的挑战，在这个过程中，聚划算无线团队和手淘天猫团队一起，逐步推进了淘系 App 的插件化体系，同时由于自身的特殊性，聚划算内部也演化出了各种独有的技术方案。
分享大致分为以下几点：
如何将业务进行插件化，进行多客户端同步部署，所使用构架的发展历程；
如何将 App 自身插件化，作为容器迎接第三方的插入；
如何使用各种动态化技术提高业务的实时能力。</p> <i>By 金津</i>
---------------
<h1 id="#title_7" >8、Google Cloud Endpoints正式发布</h1>
Sergio De Simone
[http://www.infoq.com/cn/news/2017/02/google-cloud-endpoints-ga?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/02/google-cloud-endpoints-ga?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/news/2017/02/google-cloud-endpoints-ga/zh/headerimage/GettyImages-517965466.jpg"/><p>经过3个月的Beta测试之后，谷歌正式发布了其基于Open API的API管理系统Cloud Endpoints（GCE）。据谷歌介绍，该系统旨在让开发人员可以构建高效、易于扩展的API平台。</p> <i>By Sergio De Simone</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_8" >9、微软AirSim，一个无人机和机器人的模拟器</h1>
Abel Avram
[http://www.infoq.com/cn/news/2017/02/airsim?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/02/airsim?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/news/2017/02/airsim/zh/headerimage/GettyImages-510486456.jpg"/><p>微软开发并开源了AirSim，一个用于模拟无人机在全世界的飞行的工具。这个模拟器基于虚幻引擎构建，微软很快会增加对机器人和其它类型移动设备的支持。</p> <i>By Abel Avram</i> <i> Translated by 足下</i>
---------------
<h1 id="#title_9" >10、如何提升员工的工作积极性</h1>
Rui Miguel Ferreira
[http://www.infoq.com/cn/news/2017/02/employee-experience?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/02/employee-experience?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/news/2017/02/employee-experience/zh/headerimage/GettyImages-524156476.jpg"/><p>Jacob Morgan，主讲嘉宾、畅销书作者，同时也是The Future Work Community组织的联合创始人、全球领先思考组织的创新委员会委员，专注于探索新的工作领域，在和Cisco的在线研讨会中分享了组织如何创造卓越的员工体验，那些促使人们想要在工作中主动表现的推动方式。</p> <i>By Rui Miguel Ferreira</i> <i> Translated by 麦克周</i>
---------------
<h1 id="#title_10" >11、微服务的未来：功能性服务设计和可观测性</h1>
Daniel Bryant
[http://www.infoq.com/cn/news/2017/02/microservices-design-observe?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/02/microservices-design-observe?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/news/2017/02/microservices-design-observe/zh/headerimage/GettyImages-1.jpg"/><p>为了准备将于柏林举行的第16届和第17届microXchg会议，InfoQ与Uwe Friedrichsen和Adrian Cole一同讨论了功能性服务设计（functional service design）和对于监测分布式系统的新挑战，以及未来微服务架构的类型应该是怎样的。</p> <i>By Daniel Bryant</i> <i> Translated by 罗远航</i>
---------------
<h1 id="#title_11" >12、How To Use Shadows And Blur Effects In Modern UI Design</h1>
Nick Babich
[https://www.smashingmagazine.com/2017/02/shadows-blur-effects-user-interface-design/](https://www.smashingmagazine.com/2017/02/shadows-blur-effects-user-interface-design/)
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
</table><p>When you examine the most successful interaction designs of recent years, the clear winners are those who provide an excellent functionality. While functional aspect of a design is key to product success, aesthetics and visual details are equally important &#8212; particularly how they can improve those functional elements.</p>

<figure></figure>

<p>In today's article, I'll explain how visual elements, such as shadows and blur effects, can improve the functional elements of a design.</p><p>The post .</p>
---------------