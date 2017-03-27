## 文章索引
1、 <a href="#1文章-prefix和retrace简介采访stackify的创始人matt-watson" >文章： Prefix和Retrace简介：采访Stackify的创始人Matt Watson</a><br/>
2、 <a href="#2文章-sql-引擎年度总结" >文章： SQL 引擎年度总结</a><br/>
3、 <a href="#3视频演讲-容器技术与微服务架构在跨境电商领域的集成实践" >视频演讲： 容器技术与微服务架构在跨境电商领域的集成实践</a><br/>
4、 <a href="#4从一道坑人的面试题说函数式编程" >从一道坑人的面试题说函数式编程</a><br/><h1 id="#title_0" >1、文章： Prefix和Retrace简介：采访Stackify的创始人Matt Watson</h1>
Pierre-Luc Maheu
[http://www.infoq.com/cn/articles/stackify-prefix-retrace?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/stackify-prefix-retrace?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/stackify-prefix-retrace/zh/headerimage/GettyImages-155430569.jpg"/><p>创立于2011年的Stackify公司是APM领域的新生力量，它推出的APM产品Prefix和Retrace产品分别针对桌面端和服务器端。产品基于.NET性能分析API构建，具有很好的易用性和普适性。本文是InfoQ对该公司CEO和创始人Matt Watson的访谈。</p> <i>By Pierre-Luc Maheu</i> <i> Translated by Rays</i>
---------------
<h1 id="#title_1" >2、文章： SQL 引擎年度总结</h1>
Thomas W. Dinsmore
[http://www.infoq.com/cn/articles/the-year-in-sql-engines?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/the-year-in-sql-engines?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/the-year-in-sql-engines/zh/smallimage/logo-mobile.jpg"/><p>随着NoSQL的不断发展，不断有人在研究如何在NoSQL的基础上去运行SQL，各种开源框架层出不穷，本文总结了部门热门框架，对其进行了介绍。</p> <i>By Thomas W. Dinsmore</i> <i> Translated by 覃璐</i>
---------------
<h1 id="#title_2" >3、视频演讲： 容器技术与微服务架构在跨境电商领域的集成实践</h1>
陈天影
[http://www.infoq.com/cn/presentations/integrated-practice-of-container-technology-and-micro-service?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/integrated-practice-of-container-technology-and-micro-service?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/integrated-practice-of-container-technology-and-micro-service/zh/mediumimage/chentianying270.jpg"/><p>随着敦煌网业务的快速发展，敦煌网较早就研发了自有的微服务框架，并已成熟应用。但仍然面临着很多问题，比如：微服务架构导致的模块数量快速增长与资源粒度的矛盾；所处行业特点，如爆发式流量进入，快速扩容和迁移对资源交付速度的要求；物理机利用率不平均，资源利用不充分；运行环境标准化的问题等。随着Docker的兴起，我们意识到可以使用这一技术解决以上问题。遂将已有服务从传统的部署运行方式转变到了 Docker化的私有云平台。在Docker实践中遇到一些坑，积累了一些经验，就此专题和大家进行分享和探讨。</p> <i>By 陈天影</i>
---------------
<h1 id="#title_3" >4、从一道坑人的面试题说函数式编程</h1>

[https://www.h5jun.com/post/parseInt-to-functional.html](https://www.h5jun.com/post/parseInt-to-functional.html)
<div class="toc"></div><p>一道著名的坑人题，可能一些同学见过：</p>
<pre><code class="hljs lang-js">[<span class="hljs-string">'2'</span>, <span class="hljs-string">'3'</span>, <span class="hljs-string">'4'</span>].map(<span class="hljs-built_in">parseInt</span>);
</code></pre>
<p>说出上面代码的执行结果。</p>
<!--more-->
<p>如果不过脑子的说是 <code>[2, 3, 4]</code>，那么肯定是错了。实际上，真正的执行结果是 <code>[2, NaN, NaN]</code>。为什么会这样呢？是因为 map 的算子是有两个参数的，第一个参数是被迭代数组的元素，第二个参数是该元素的下标。所以 <code>[&#39;2&#39;, &#39;3&#39;, &#39;4&#39;].map(parseInt)</code> 实际上相当于执行了 <code>[parseInt(&#39;2&#39;, 0), parseInt(&#39;3&#39;, 1), parseInt(&#39;4&#39;, 2)]</code>，结果就变成了 <code>[2, NaN, NaN]</code> 了。</p>
<p>今天我们在这里主要不是讨论为什么 <code>parseInt(&#39;2&#39;, 0)</code> 是 2，而 <code>parseInt(&#39;3&#39;, 1)</code> 是 NaN，实际上我们期望的结果应该是 <code>parseInt(&#39;2&#39;, 10)</code> 和 <code>parseInt(&#39;3&#39;, 10)</code>，把字符串 &#39;2&#39;、&#39;3&#39; 转成十进制 number。</p>
<p>所以，正确的写法应该是：</p>
<pre><code class="hljs lang-js">[<span class="hljs-string">'2'</span>, <span class="hljs-string">'3'</span>, <span class="hljs-string">'4'</span>].map(num =&gt; <span class="hljs-built_in">parseInt</span>(num, <span class="hljs-number">10</span>));
</code></pre>
<p>上面这个写法对于这个问题来说是简单的，和函数式编程关系不大。但是，这个问题如果用过程抽象的思路通用化思考，应该是这样的：</p>
<pre><code class="hljs lang-js">[<span class="hljs-string">'2'</span>, <span class="hljs-string">'3'</span>, <span class="hljs-string">'4'</span>].map(num.bindRight(<span class="hljs-literal">null</span>, <span class="hljs-number">10</span>));
</code></pre>
<p>其中 bindRight 和 bind 方法是相反的，bindRight 相当于从右往左 bind：</p>
<pre><code class="hljs lang-js"><span class="hljs-function"><span class="hljs-keyword">function</span> <span class="hljs-title">add</span>(<span class="hljs-params">x, y, z</span>)</span>{
    <span class="hljs-keyword">return</span> <span class="hljs-number">100</span>*x + <span class="hljs-number">10</span> * y + z;
}

<span class="hljs-keyword">let</span> add1 = add.bind(<span class="hljs-literal">null</span>, <span class="hljs-number">1</span>, <span class="hljs-number">2</span>);
<span class="hljs-keyword">let</span> add2 = add.bindRight(<span class="hljs-literal">null</span>, <span class="hljs-number">1</span>, <span class="hljs-number">2</span>);

add1(<span class="hljs-number">3</span>); <span class="hljs-comment">//123</span>
add2(<span class="hljs-number">3</span>); <span class="hljs-comment">//321</span>
</code></pre>
<p>要实现 bindRight，考虑各种情况，稍稍有些复杂，但也并不太麻烦：</p>
<pre><code class="hljs lang-js"><span class="hljs-built_in">Function</span>.prototype.bindRight = <span class="hljs-function"><span class="hljs-keyword">function</span>(<span class="hljs-params">thisObj, ...values</span>)</span>{
  <span class="hljs-keyword">let</span> fn = <span class="hljs-keyword">this</span>, len = fn.length - values.length;
  <span class="hljs-keyword">return</span> <span class="hljs-function"><span class="hljs-keyword">function</span>(<span class="hljs-params">...args</span>)</span>{
    <span class="hljs-keyword">let</span> rest = [], rargs = values.reverse();

    <span class="hljs-keyword">if</span>(len &gt; <span class="hljs-number">0</span>){
      rest = args.slice(<span class="hljs-number">0</span>, len);
    }

    <span class="hljs-keyword">return</span> fn.apply(thisObj, rest.concat(rargs));
  }
}
</code></pre>
<p>这样就实现了我们需要的 bindRight，完整的结果如下：</p>
<p><script src="https:////code.h5jun.com/js/embed.min.js?3.40.2"></script></p>
<p>bindRight 代码并不复杂，如果 bindRight 的参数个数比函数形参多，那么简单将参数次序 reverse 之后传给原来的函数，否则将函数前面的参数补齐。</p>
<p>除了这样实现 bindRight 之外，还可以有利用更基础的高阶函数操作组合的方式：</p>
<pre><code class="hljs lang-js"><span class="hljs-built_in">Function</span>.prototype.reverseArgs = <span class="hljs-function"><span class="hljs-keyword">function</span>(<span class="hljs-params"></span>)</span>{
  <span class="hljs-keyword">let</span> fn = <span class="hljs-keyword">this</span>;
  <span class="hljs-keyword">return</span> <span class="hljs-function"><span class="hljs-keyword">function</span>(<span class="hljs-params">...args</span>)</span>{
    <span class="hljs-keyword">return</span> fn.apply(<span class="hljs-keyword">this</span>, args.reverse());
  }
}

<span class="hljs-built_in">Function</span>.prototype.fixArgsLength = <span class="hljs-function"><span class="hljs-keyword">function</span>(<span class="hljs-params">len</span>)</span>{
  <span class="hljs-keyword">let</span> fn = <span class="hljs-keyword">this</span>;
  <span class="hljs-keyword">return</span> <span class="hljs-function"><span class="hljs-keyword">function</span>(<span class="hljs-params">...args</span>)</span>{
    args.length = len || fn.length;
    <span class="hljs-keyword">return</span> fn.apply(<span class="hljs-keyword">this</span>, args);
  }
}

<span class="hljs-built_in">Function</span>.prototype.bindRight = <span class="hljs-function"><span class="hljs-keyword">function</span>(<span class="hljs-params">thisObj, ...values</span>)</span>{
  <span class="hljs-keyword">return</span> <span class="hljs-keyword">this</span>.reverseArgs().bind(thisObj, ...values).reverseArgs().fixArgsLength(<span class="hljs-number">1</span>);
}
</code></pre>
<p>上面的这段代码里我们通过 reverseArgs 和 fixArgsLength 以及 bind 来组合出 bindRight。reverseArgs 是将函数参数顺序倒序的高阶函数，fixArgsLength 是将函数参数个数固定的高阶函数，我们可以看到 bindRight 就是先 reverseArgs 再 bind，最后 fixArgsLength（大家可以思考下为什么要 fixArgsLength）。这样就可以了。</p>
<p>不过话说，就上面这个问题直接用 fixArgsLength 也可以——</p>
<pre><code class="hljs lang-js">[<span class="hljs-string">"2"</span>,<span class="hljs-string">"3"</span>,<span class="hljs-string">"4"</span>].map(<span class="hljs-built_in">parseInt</span>.fixArgsLength(<span class="hljs-number">1</span>)); <span class="hljs-comment">// [2, 3, 4]</span>
</code></pre>
<p>最后是完整代码：</p>
<p><script src="https:////code.h5jun.com/js/embed.min.js?3.40.2"></script></p>
<p>如有任何问题，欢迎讨论。</p>
---------------