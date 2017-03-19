## 文章索引
1、 <a href="#1reduce-和-transduce-的含义" >Reduce 和 Transduce 的含义</a><br/>
2、 <a href="#2视频演讲-如何出品一个技术专题" >视频演讲： 如何出品一个技术专题</a><br/><h1 id="#title_0" >1、Reduce 和 Transduce 的含义</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2017/03/reduce_transduce.html](http://www.ruanyifeng.com/blog/2017/03/reduce_transduce.html)
<p>学习，必须掌握很多术语，否则根本看不懂文档。</p>

        <p>本文介绍两个基本术语：<code>reduce</code>和<code>transduce</code>。它们非常重要，也非常有用。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017031801.png" alt="" title="" /></p>

<h2>一、reduce 的用法</h2>

<p><code>reduce</code>是一种数组运算，通常用于将数组的所有成员"累积"为一个值。</p>

<blockquote><pre><code class="language-javascript">
var arr = [1, 2, 3, 4];

var sum = (a, b) => a + b;

arr.reduce(sum, 0) // 10
</code></pre></blockquote>

<p>上面代码中，<code>reduce</code>对数组<code>arr</code>的每个成员执行<code>sum</code>函数。<code>sum</code>的参数<code>a</code>是累积变量，参数<code>b</code>是当前的数组成员。每次执行时，<code>b</code>会加到<code>a</code>，最后输出<code>a</code>。</p>

<p>累积变量必须有一个初始值，上例是<code>reduce</code>函数的第二个参数<code>0</code>。如果省略该参数，那么初始值默认是数组的第一个成员。</p>

<blockquote><pre><code class="language-javascript">
var arr = [1, 2, 3, 4];

var sum = function (a, b) {
  console.log(a, b);
  return a + b;
};

arr.reduce(sum) // => 10
// 1 2
// 3 3
// 6 4
</code></pre></blockquote>

<p>上面代码中，<code>reduce</code>方法省略了初始值。通过<code>sum</code>函数里面的打印语句，可以看到累积变量每一次的变化。</p>

<p>总之，<code>reduce</code>方法提供了一种遍历手段，对数组所有成员进行"累积"处理。</p>

<h2>二、map 是 reduce 的特例</h2>

<p>累积变量的初始值也可以是一个数组。</p>

<blockquote><pre><code class="language-javascript">
var arr = [1, 2, 3, 4];

var handler = function (newArr, x) {
  newArr.push(x + 1);
  return newArr;
};

arr.reduce(handler, [])
// [2, 3, 4, 5]
</code></pre></blockquote>

<p>上面代码中，累积变量的初始值是一个空数组，结果<code>reduce</code>就返回了一个新数组，等同于执行<code>map</code>方法，对原数组进行一次"变形"。下面是使用<code>map</code>改写上面的例子。</p>

<blockquote><pre><code class="language-javascript">
var arr = [1, 2, 3, 4];
var plusOne = x => x + 1;
arr.map(plusOne) // [2, 3, 4, 5]
</code></pre></blockquote>

<p>事实上，所有的<code>map</code>方法都可以基于<code>reduce</code>实现。</p>

<blockquote><pre><code class="language-javascript">
function map(f, arr) {
  return arr.reduce(function(result, x) {
    result.push(f(x));
    return result;
  }, []);
}
</code></pre></blockquote>

<p>因此，<code>map</code>只是<code>reduce</code>的一种特例。</p>

<h2>三、<code>reduce</code>的本质</h2>

<p>本质上，<code>reduce</code>是三种运算的合成。</p>

<blockquote>
  <ul>
<li>遍历</li>
<li>变形</li>
<li>累积</li>
</ul>
</blockquote>

<p>还是来看上面的例子。</p>

<blockquote><pre><code class="language-javascript">
var arr = [1, 2, 3, 4];
var handler = function (newArr, x) {
  newArr.push(x + 1);
  return newArr;
};

arr.reduce(handler, [])
// [2, 3, 4, 5]
</code></pre></blockquote>

<p>上面代码中，首先，<code>reduce</code>遍历了原数组，这是它能够取代<code>map</code>方法的根本原因；其次，<code>reduce</code>对原数组的每个成员进行了"变形"（上例是加<code>1</code>）；最后，才是把它们累积起来（上例是<code>push</code>方法）。</p>

<h2>四、 transduce 的含义</h2>

<p><code>reduce</code>包含了三种运算，因此非常有用。但也带来了一个问题：代码的复用性不高。在<code>reduce</code>里面，变形和累积是耦合的，不太容易拆分。</p>

<p>每次使用<code>reduce</code>，开发者往往都要从头写代码，重复实现很多基本功能，很难复用别人的代码。</p>

<blockquote><pre><code class="language-javascript">
var handler = function (newArr, x) {
  newArr.push(x + 1);
  return newArr;
};
</code></pre></blockquote>

<p>上面的这个处理函数，就很难用在其他场合。</p>

<p>有没有解决方法呢？回答是有的，就是把"变形"和"累积"这两种运算分开。如果<code>reduce</code>允许变形运算和累积运算分开，那么代码的复用性就会大大增加。这就是<code>transduce</code>方法的由来。</p>

<p><code>transduce</code>这个名字来自 transform（变形）和 reduce 这两个单词的合成。它其实就是<code>reduce</code>方法的一种不那么耦合的写法。</p>

<blockquote><pre><code class="language-javascript">
// 变形运算
var plusOne = x => x + 1;

// 累积运算
var append = function (newArr, x) {
  newArr.push(x);
  return newArr;
}; 

R.transduce(R.map(plusOne), append, [], arr);
// [2, 3, 4, 5]
</code></pre></blockquote>

<p>上面代码中，<code>plusOne</code>是变形操作，<code>append</code>是累积操作。我使用了 的<code>transduce</code>实现。可以看到，<code>transduce</code>就是将变形和累积从<code>reduce</code>拆分出来，其他并无不同。</p>

<h2>五、transduce 的用法</h2>

<p><code>transduce</code>最大的好处，就是代码复用更容易。</p>

<blockquote><pre><code class="language-javascript">
var arr = [1, 2, 3, 4];
var append = function (newArr, x) {
  newArr.push(x);
  return newArr;
}; 

// 示例一
var plusOne = x => x + 1;
var square = x => x * x;

R.transduce(
  R.pipe(R.map(plusOne), R.map(square)), 
  append, 
  [], 
  arr
); // [2, 5, 10, 17]

// 示例二
var isOdd = x => x % 2 === 1;

R.transduce(
  R.pipe(R.filter(isOdd), R.map(square)), 
  append, 
  [], 
  arr
); // [1, 9]
</code></pre></blockquote>

<p>上面代码中，示例一是两个变形操作的合成，示例二是过滤操作与变形操作的合成。这两个例子都使用了 。</p>

<p>可以看到，<code>transduce</code>非常有利于代码的复用，可以将一系列简单的、可复用的函数合成为复杂操作。作为练习，有兴趣的读者可以试试，使用<code>reduce</code>方法完成上面两个示例。你会发现，代码的复杂度和行数大大增加。</p>

<h2>六、Transformer 对象</h2>

<p><code>transduce</code>函数的第一个参数是一个对象，称为 Transformer 对象（变形器）。前面例子中，<code>R.map(plusOne)</code>返回的就是一个 Transformer 对象。</p>

<p>事实上，任何一个对象只要遵守 ，就是 Transformer 对象。</p>

<blockquote><pre><code class="language-javascript">
var Map = function(f, xf) {
    return {
       "@@transducer/init": function() { 
           return xf["@@transducer/init"](); 
       },
       "@@transducer/result": function(result) { 
           return xf["@@transducer/result"](result); 
       },
       "@@transducer/step": function(result, input) {
           return xf["@@transducer/step"](result, f(input)); 
       }
    };
};
</code></pre></blockquote>

<p>上面代码中，<code>Map</code>函数返回的就是一个 Transformer 对象。它必须具有以下三个属性。</p>

<blockquote>
  <ul>
<li>@@transducer/step：执行变形操作</li>
<li>@@transducer/init：返回初始值</li>
<li>@@transducer/result：返回变形后的最终值</li>
</ul>
</blockquote>

<p>所有符合这个协议的对象，都可以与其他 Transformer 对象合成，充当<code>transduce</code>函数的第一个参数。</p>

<p>因此，<code>transduce</code>函数的参数类型如下。</p>

<blockquote><pre><code class="language-javascript">
transduce(
  变形器 : Object,
  累积器 : Function,
  初始值 : Any,
  原始数组 : Array
)
</code></pre></blockquote>

<h2>七、into 方法</h2>

<p>最后，你也许发现了，前面所有示例使用的都是同一个累积器。</p>

<blockquote><pre><code class="language-javascript">
var append = function (newArr, x) {
  newArr.push(x);
  return newArr;
}; 
</code></pre></blockquote>

<p>上面代码的<code>append</code>函数是一个常见累积器。因此， Ramda 函数库提供了<code>into</code>方法，将它内置了。也就是说，<code>into</code>方法相当于默认提供<code>append</code>的<code>transduce</code>函数。</p>

<blockquote><pre><code class="language-javascript">
R.transduce(R.map(R.add(1)), append, [], [1,2,3,4]);
// 等同于
R.into([], R.map(R.add(1)), [1,2,3,4]);
</code></pre></blockquote>

<p>上面代码中，<code>into</code>方法的第一个参数是初始值，第二个参数是变形器，第三个参数是原始数组，不需要提供累积器。</p>

<p>下面是另外一个例子。</p>

<blockquote><pre><code class="language-javascript">
R.into(
  [5, 6],
  R.pipe(R.take(2), R.map(R.add(1))),
  [1, 2, 3, 4]
) // [5, 6, 2, 3]
</code></pre></blockquote>

<h2>八、参考链接</h2>

<ul>
<li></li>
<li></li>
<li></li>
</ul>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2017-03-18T16:50:20+08:00">2017年3月18日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>博客文集：</li>
<li>社交媒体：</li>
<li>Feed订阅： </li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------
<h1 id="#title_1" >2、视频演讲： 如何出品一个技术专题</h1>
付海军
[http://www.infoq.com/cn/presentations/how-to-produce-a-technical-topic?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/how-to-produce-a-technical-topic?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/how-to-produce-a-technical-topic/zh/mediumimage/fuhaijun270.jpg"/><p>为了提升大会的演讲效果和听众对演讲内容的接受度，QCon组委会和往届一样，在会前举办了QCon北京2017讲师演讲经验交流会。在此次交流会上，本届互联网广告系统实践专题出品人付海军和各位讲师分享了他出品这一专题的心路历程。</p> <i>By 付海军</i>
---------------