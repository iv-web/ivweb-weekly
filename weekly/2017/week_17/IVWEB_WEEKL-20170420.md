## 文章索引
1、 <a href="#1如何用原生-js-实现手势解锁组件" >如何用原生 JS 实现手势解锁组件</a><br/>
2、 <a href="#2its-time-to-start-using-css-custom-properties" >It’s Time To Start Using CSS Custom Properties</a><br/>
3、 <a href="#3java-ee-8终于给出即将完成的迹象" >Java EE 8终于给出即将完成的迹象</a><br/>
4、 <a href="#4文章-大数据管理平台apache-geode-分布式系统内部结构剖析" >文章： 大数据管理平台Apache Geode 分布式系统内部结构剖析</a><br/>
5、 <a href="#5自动化数据科学与机器学习auto-sklearn开发团队访谈" >自动化数据科学与机器学习：Auto-sklearn开发团队访谈</a><br/>
6、 <a href="#6未来的net之多重继承" >未来的.NET之多重继承</a><br/>
7、 <a href="#7视频演讲-当你的团队还支撑不起梦想时" >视频演讲： 当你的团队还支撑不起梦想时</a><br/>
8、 <a href="#8postgresql-10新特性概述" >PostgreSQL 10新特性概述</a><br/>
9、 <a href="#9faunadb一款由前twitter技术负责人创建的新的分布式数据库" >FaunaDB：一款由前Twitter技术负责人创建的新的分布式数据库</a><br/>
10、 <a href="#10文章-开发高质量软件的区别因素" >文章： 开发高质量软件的区别因素</a><br/>
11、 <a href="#11文章-解密大规模的api优先转型来自paypal的课程第二部" >文章： 解密大规模的API优先转型：来自PayPal的课程（第二部）</a><br/>
12、 <a href="#12文章-火力全开大数据领域2017年全景剖析" >文章： 火力全开：大数据领域2017年全景剖析</a><br/>
13、 <a href="#13a-brief-overview-on-responsive-navigation-patterns" >A Brief Overview On Responsive Navigation Patterns</a><br/><h1 id="#title_0" >1、如何用原生 JS 实现手势解锁组件</h1>

[https://www.h5jun.com/post/handlock-comp.html](https://www.h5jun.com/post/handlock-comp.html)
<div class="toc"><ul>
<li><ul>
<li></li>
<li></li>
<li><ul>
<li></li>
<li></li>
</ul>
</li>
<li></li>
<li><ul>
<li></li>
<li></li>
</ul>
</li>
<li></li>
<li></li>
</ul>
</li>
<li></li>
</ul>
</div><p>这是。600多名学生参与了解答，最后通过了60人。这60名同学完成的不错，思路、代码风格、功能完成度颇有可取之处，不过也有一些欠考虑的地方，比如发现很多同学能按照需求实现完整的功能，但是不知道应当如何<strong>设计开放的 API</strong>，或者说，如何分析和预判产品需求和未来的变化，从而决定什么应当开放，什么应当封装。这无关于答案正确与否，还是和经验有关。</p>
<p>在这里，我提供一个，并不是说这一版就最好，而是说，通过这一版，分析当我们遇到这样的比较复杂的 UI 需求的时候，我们应该怎样思考和实现。</p>
<!--more-->
<p><img src="https://p.ssl.qhimg.com/d/inn/603c0bc8/06692681-E1C6-400A-A516-D7F8B26732C7.png" alt=""></p>
<h2>组件设计的一般步骤</h2>
<p>组件设计一般来说包括如下一些过程：</p>
<ol>
<li>理解需求</li>
<li>技术选型</li>
<li>结构（UI）设计</li>
<li>数据和API设计</li>
<li>流程设计</li>
<li>兼容性和细节优化</li>
<li>工具 &amp; 工程化</li>
</ol>
<p>这些过程并不是每个组件设计的时候都会遇到，但是通常来说一个项目总会在其中一些过程里遇到问题需要解决。下面我们来简单分析一下。</p>
<h3>理解需求</h3>
<p>作业本身只是说设计一个常见的手势密码的 UI 交互，可以通过选择验证密码和设置密码来切换两种状态，每种状态有自己的流程。因此大部分同学就照着需求把整个组件的状态切换和流程封装了起来，有的同学提供了一定的 UI 样式配置能力，但是基本上没有同学能将流程和状态切换过程中的节点给开放出来。实际上这个组件如果要给用户使用，显然需要将过程节点开放出来，也就是说，<strong>需要由使用者决定设置密码的过程里执行什么操作、验证密码的过程和密码验证成功后执行什么操作</strong>，这些是组件开发者无法代替使用者来决定的。</p>
<pre><code class="hljs lang-js"><span class="hljs-keyword">var</span> password = <span class="hljs-string">'11121323'</span>;

<span class="hljs-keyword">var</span> locker = <span class="hljs-keyword">new</span> HandLock.Locker({
  container: <span class="hljs-built_in">document</span>.querySelector(<span class="hljs-string">'#handlock'</span>),
  check: {
    checked: <span class="hljs-function"><span class="hljs-keyword">function</span>(<span class="hljs-params">res</span>)</span>{
      <span class="hljs-keyword">if</span>(res.err){
        <span class="hljs-built_in">console</span>.error(res.err); <span class="hljs-comment">//密码错误或长度太短</span>
        [执行操作...]
      }<span class="hljs-keyword">else</span>{
        <span class="hljs-built_in">console</span>.log(<span class="hljs-string">`正确，密码是：<span class="hljs-subst">${res.records}</span>`</span>);
        [执行操作...]
      }
    },
  },
  update:{
    beforeRepeat: <span class="hljs-function"><span class="hljs-keyword">function</span>(<span class="hljs-params">res</span>)</span>{
      <span class="hljs-keyword">if</span>(res.err){
        <span class="hljs-built_in">console</span>.error(res.err); <span class="hljs-comment">//密码长度太短</span>
        [执行操作...]
      }<span class="hljs-keyword">else</span>{
        <span class="hljs-built_in">console</span>.log(<span class="hljs-string">`密码初次输入完成，等待重复输入`</span>);
        [执行操作...]
      }
    },
    afterRepeat: <span class="hljs-function"><span class="hljs-keyword">function</span>(<span class="hljs-params">res</span>)</span>{
      <span class="hljs-keyword">if</span>(res.err){
        <span class="hljs-built_in">console</span>.error(res.err); <span class="hljs-comment">//密码长度太短或者两次密码输入不一致</span>
        [执行操作...]
      }<span class="hljs-keyword">else</span>{
        <span class="hljs-built_in">console</span>.log(<span class="hljs-string">`密码更新完成，新密码是：<span class="hljs-subst">${res.records}</span>`</span>);
        [执行操作...]
      }
    },
  }
});

locker.check(password);
</code></pre>
<h3>技术选型</h3>
<p>这个问题的 UI 展现的核心是九宫格和选中的小圆点，从技术上来讲，我们有三种可选方案： DOM/Canvas/SVG，三者都是可以实现主体 UI 的。</p>
<p>如果使用 DOM，最简单的方式是使用 flex 布局，这样能够做成响应式的。</p>
<p><script src="https:////code.h5jun.com/js/embed.min.js?3.40.2"></script></p>
<p>使用 DOM 的优点是容易实现响应式，事件处理简单，布局也不复杂（但是和 Canvas 比起来略微复杂），但是斜线（demo 里没有画）的长度和斜率需要计算。</p>
<p>除了使用 DOM 外，使用 Canvas 绘制也很方便：</p>
<p><script src="https:////code.h5jun.com/js/embed.min.js?3.40.2"></script> </p>
<p>用 Canvas 实现有两个小细节，第一是要实现响应式，可以用 DOM 构造一个正方形的容器：</p>
<pre><code class="hljs lang-css"><span class="hljs-selector-id">#container</span> {
  <span class="hljs-attribute">position</span>: relative;
  <span class="hljs-attribute">overflow</span>: hidden;
  <span class="hljs-attribute">width</span>: <span class="hljs-number">100%</span>;
  <span class="hljs-attribute">padding-top</span>: <span class="hljs-number">100%</span>;
  <span class="hljs-attribute">height</span>: <span class="hljs-number">0px</span>;
  <span class="hljs-attribute">background-color</span>: white;
}
</code></pre>
<p>在这里我们使用 <code>padding-top:100%</code> 撑开容器高度使它等于容器宽度。</p>
<p>第二个细节是为了在 retina 屏上获得清晰的显示效果，我们将 Canvas 的宽高增加一倍，然后通过 <code>transform: scale(0.5)</code> 来缩小到匹配容器宽高。</p>
<pre><code class="hljs lang-css"><span class="hljs-selector-id">#container</span> <span class="hljs-selector-tag">canvas</span>{
  <span class="hljs-attribute">position</span>: absolute;
  <span class="hljs-attribute">left</span>: <span class="hljs-number">50%</span>;
  <span class="hljs-attribute">top</span>: <span class="hljs-number">50%</span>;
  <span class="hljs-attribute">transform</span>: <span class="hljs-built_in">translate</span>(-50%, -50%) <span class="hljs-built_in">scale</span>(0.5);
}
</code></pre>
<p>由于 Canvas 的定位是 absolute，它本身的默认宽高并不等于容器的宽高，需要通过 JS 设置：</p>
<pre><code class="hljs lang-js"><span class="hljs-keyword">let</span> width = <span class="hljs-number">2</span> * container.getBoundingClientRect().width;
canvas.width = canvas.height = width;
</code></pre>
<p>这样我们就可以通过在 Canvas 上绘制实心圆和连线来实现 UI 了。具体的方法在后续的内容里有更详细的讲解。</p>
<p>最后我们来看一下用 SVG 绘制：</p>
<p><script src="https:////code.h5jun.com/js/embed.min.js?3.40.2"></script></p>
<p>由于 SVG 原生操作的 API 不是很方便，这里使用了 ，实现起来和使用 Canvas 大同小异，这里就不赘述了。</p>
<p>SVG 的问题是移动端兼容性不如 DOM 和 Canvas 好。</p>
<p>综合上面三者的情况，最终我选择使用 Canvas 来实现。</p>
<h3>结构设计</h3>
<p>使用 Canvas 实现的话 DOM 结构就比较简单。为了响应式，我们需要实现一个自适应宽度的正方形容器，方法前面已经介绍过。接着在容器中创建 Canvas。这里需要注意的一点是，我们应当把 Canvas 分层。这是因为 Canvas 的渲染机制里，要更新画布的内容，需要刷新要更新的区域重新绘制。因为我们有必要把频繁变化的内容和基本不变的内容分层管理，这样能显著提升性能。</p>
<h4>分成 3 个图层</h4>
<p><img src="https://p4.ssl.qhimg.com/t01e8fbcac1b8d2f472.png" alt=""></p>
<p>在这里我把 UI 分别绘制在 3 个图层里，对应 3 个 Canvas。最上层只有随着手指头移动的那个线段，中间是九个点，最下层是已经绘制好的线。之所以这样分，是因为随手指头移动的那条线需要不断刷新，底下两层都不用频繁更新，但是把连好的线放在最底层是因为我要做出圆点把线的一部分遮挡住的效果。</p>
<h4>确定圆点的位置</h4>
<p><img src="https://p0.ssl.qhimg.com/t01a663c97f0dd807e3.png" alt=""></p>
<p>圆点的位置有两种定位法，第一种是九个九宫格，圆点在小九宫格的中心位置。如果认真的同学，已经发现在前面 DOM 方案里，我们就是采用这样的方式，圆点的直径为 11.1%。第二种方式是用横竖三条线把宽高四等分，圆点在这些线的交点处。</p>
<p>在 Canvas 里我们采用第二种方法来确定圆点（代码里的 n = 3）。</p>
<pre><code class="hljs lang-js"><span class="hljs-keyword">let</span> range = <span class="hljs-built_in">Math</span>.round(width / (n + <span class="hljs-number">1</span>));

<span class="hljs-keyword">let</span> circles = [];

<span class="hljs-comment">//drawCircleCenters</span>
<span class="hljs-keyword">for</span>(<span class="hljs-keyword">let</span> i = <span class="hljs-number">1</span>; i &lt;= n; i++){
  <span class="hljs-keyword">for</span>(<span class="hljs-keyword">let</span> j = <span class="hljs-number">1</span>; j &lt;= n; j++){
    <span class="hljs-keyword">let</span> y = range * i, x = range * j;
    drawSolidCircle(circleCtx, fgColor, x, y, innerRadius);
    <span class="hljs-keyword">let</span> circlePoint = {x, y};
    circlePoint.pos = [i, j];
    circles.push(circlePoint);
  }
}
</code></pre>
<p>最后一点，严格说不属于结构设计，但是因为我们的 UI 是通过触屏操作，我们需要考虑 Touch 事件处理和坐标的转换。</p>
<pre><code class="hljs lang-js"><span class="hljs-function"><span class="hljs-keyword">function</span> <span class="hljs-title">getCanvasPoint</span>(<span class="hljs-params">canvas, x, y</span>)</span>{
  <span class="hljs-keyword">let</span> rect = canvas.getBoundingClientRect();
  <span class="hljs-keyword">return</span> {
    x: <span class="hljs-number">2</span> * (x - rect.left), 
    y: <span class="hljs-number">2</span> * (y - rect.top),
  };
}
</code></pre>
<p>我们将 Touch 相对于屏幕的坐标转换为 Canvas 相对于画布的坐标。代码里的 2 倍是因为我们前面说了要让 retina 屏下清晰，我们将 Canvas 放大为原来的 2 倍。</p>
<h3>API 设计</h3>
<p>接下来我们需要设计给使用者使用的 API 了。在这里，我们将组件功能分解一下，独立出一个单纯记录手势的 Recorder。将组件功能分解为更加底层的组件，是一种简化组件设计的常用模式。</p>
<p><img src="https://p5.ssl.qhimg.com/t01cf2097cf8acb1cb7.png" alt=""></p>
<p>我们抽取出底层的 Recorder，让 Locker 继承 Recorder，Recorder 负责记录，Locker 管理实际的设置和验证密码的过程。</p>
<p>我们的 Recorder 只负责记录用户行为，由于用户操作是异步操作，我们将它设计为 Promise 规范的 API，它可以以如下方式使用：</p>
<pre><code class="hljs lang-js"><span class="hljs-keyword">var</span> recorder = <span class="hljs-keyword">new</span> HandLock.Recorder({
  container: <span class="hljs-built_in">document</span>.querySelector(<span class="hljs-string">'#main'</span>)
});

<span class="hljs-function"><span class="hljs-keyword">function</span> <span class="hljs-title">recorded</span>(<span class="hljs-params">res</span>)</span>{
  <span class="hljs-keyword">if</span>(res.err){
    <span class="hljs-built_in">console</span>.error(res.err);
    recorder.clearPath();
    <span class="hljs-keyword">if</span>(res.err.message !== HandLock.Recorder.ERR_USER_CANCELED){
      recorder.record().then(recorded);
    }
  }<span class="hljs-keyword">else</span>{
    <span class="hljs-built_in">console</span>.log(res.records);
    recorder.record().then(recorded);
  }      
}

recorder.record().then(recorded);
</code></pre>
<p>对于输出结果，我们简单用选中圆点的行列坐标拼接起来得到一个唯一的序列。例如 &quot;11121323&quot; 就是如下选择图形：</p>
<p><img src="https://p4.ssl.qhimg.com/t012a1dd06ae9814468.png" alt=""></p>
<p>为了让 UI 显示具有灵活性，我们还可以将外观配置抽取出来。</p>
<pre><code class="hljs lang-js"><span class="hljs-keyword">const</span> defaultOptions = {
  container: <span class="hljs-literal">null</span>, <span class="hljs-comment">//创建canvas的容器，如果不填，自动在 body 上创建覆盖全屏的层</span>
  focusColor: <span class="hljs-string">'#e06555'</span>,  <span class="hljs-comment">//当前选中的圆的颜色</span>
  fgColor: <span class="hljs-string">'#d6dae5'</span>,     <span class="hljs-comment">//未选中的圆的颜色</span>
  bgColor: <span class="hljs-string">'#fff'</span>,        <span class="hljs-comment">//canvas背景颜色</span>
  n: <span class="hljs-number">3</span>, <span class="hljs-comment">//圆点的数量： n x n</span>
  innerRadius: <span class="hljs-number">20</span>,  <span class="hljs-comment">//圆点的内半径</span>
  outerRadius: <span class="hljs-number">50</span>,  <span class="hljs-comment">//圆点的外半径，focus 的时候显示</span>
  touchRadius: <span class="hljs-number">70</span>,  <span class="hljs-comment">//判定touch事件的圆半径</span>
  render: <span class="hljs-literal">true</span>,     <span class="hljs-comment">//自动渲染</span>
  customStyle: <span class="hljs-literal">false</span>, <span class="hljs-comment">//自定义样式</span>
  minPoints: <span class="hljs-number">4</span>,     <span class="hljs-comment">//最小允许的点数</span>
};
</code></pre>
<p>这样我们实现完整的 Recorder 对象，核心代码如下：</p>
<pre><code class="hljs lang-js">[...] <span class="hljs-comment">//定义一些私有方法</span>

<span class="hljs-keyword">const</span> defaultOptions = {
  container: <span class="hljs-literal">null</span>, <span class="hljs-comment">//创建canvas的容器，如果不填，自动在 body 上创建覆盖全屏的层</span>
  focusColor: <span class="hljs-string">'#e06555'</span>,  <span class="hljs-comment">//当前选中的圆的颜色</span>
  fgColor: <span class="hljs-string">'#d6dae5'</span>,     <span class="hljs-comment">//未选中的圆的颜色</span>
  bgColor: <span class="hljs-string">'#fff'</span>,        <span class="hljs-comment">//canvas背景颜色</span>
  n: <span class="hljs-number">3</span>, <span class="hljs-comment">//圆点的数量： n x n</span>
  innerRadius: <span class="hljs-number">20</span>,  <span class="hljs-comment">//圆点的内半径</span>
  outerRadius: <span class="hljs-number">50</span>,  <span class="hljs-comment">//圆点的外半径，focus 的时候显示</span>
  touchRadius: <span class="hljs-number">70</span>,  <span class="hljs-comment">//判定touch事件的圆半径</span>
  render: <span class="hljs-literal">true</span>,     <span class="hljs-comment">//自动渲染</span>
  customStyle: <span class="hljs-literal">false</span>, <span class="hljs-comment">//自定义样式</span>
  minPoints: <span class="hljs-number">4</span>,     <span class="hljs-comment">//最小允许的点数</span>
};

<span class="hljs-keyword">export</span> <span class="hljs-keyword">default</span> <span class="hljs-class"><span class="hljs-keyword">class</span> <span class="hljs-title">Recorder</span></span>{
  <span class="hljs-keyword">static</span> get ERR_NOT_ENOUGH_POINTS(){
    <span class="hljs-keyword">return</span> <span class="hljs-string">'not enough points'</span>;
  }
  <span class="hljs-keyword">static</span> get ERR_USER_CANCELED(){
    <span class="hljs-keyword">return</span> <span class="hljs-string">'user canceled'</span>;
  }
  <span class="hljs-keyword">static</span> get ERR_NO_TASK(){
    <span class="hljs-keyword">return</span> <span class="hljs-string">'no task'</span>;
  }
  <span class="hljs-keyword">constructor</span>(options){
    options = <span class="hljs-built_in">Object</span>.assign({}, defaultOptions, options);

    <span class="hljs-keyword">this</span>.options = options;
    <span class="hljs-keyword">this</span>.path = [];

    <span class="hljs-keyword">if</span>(options.render){
      <span class="hljs-keyword">this</span>.render();
    }
  }
  render(){
    <span class="hljs-keyword">if</span>(<span class="hljs-keyword">this</span>.circleCanvas) <span class="hljs-keyword">return</span> <span class="hljs-literal">false</span>;

    <span class="hljs-keyword">let</span> options = <span class="hljs-keyword">this</span>.options;
    <span class="hljs-keyword">let</span> container = options.container || <span class="hljs-built_in">document</span>.createElement(<span class="hljs-string">'div'</span>);

    <span class="hljs-keyword">if</span>(!options.container &amp;&amp; !options.customStyle){
      <span class="hljs-built_in">Object</span>.assign(container.style, {
        position: <span class="hljs-string">'absolute'</span>,
        top: <span class="hljs-number">0</span>,
        left: <span class="hljs-number">0</span>,
        width: <span class="hljs-string">'100%'</span>,
        height: <span class="hljs-string">'100%'</span>,
        lineHeight: <span class="hljs-string">'100%'</span>,
        overflow: <span class="hljs-string">'hidden'</span>,
        backgroundColor: options.bgColor
      });
      <span class="hljs-built_in">document</span>.body.appendChild(container); 
    }
    <span class="hljs-keyword">this</span>.container = container;

    <span class="hljs-keyword">let</span> {width, height} = container.getBoundingClientRect();

    <span class="hljs-comment">//画圆的 canvas，也是最外层监听事件的 canvas</span>
    <span class="hljs-keyword">let</span> circleCanvas = <span class="hljs-built_in">document</span>.createElement(<span class="hljs-string">'canvas'</span>); 

    <span class="hljs-comment">//2 倍大小，为了支持 retina 屏</span>
    circleCanvas.width = circleCanvas.height = <span class="hljs-number">2</span> * <span class="hljs-built_in">Math</span>.min(width, height);
    <span class="hljs-keyword">if</span>(!options.customStyle){
      <span class="hljs-built_in">Object</span>.assign(circleCanvas.style, {
        position: <span class="hljs-string">'absolute'</span>,
        top: <span class="hljs-string">'50%'</span>,
        left: <span class="hljs-string">'50%'</span>,
        transform: <span class="hljs-string">'translate(-50%, -50%) scale(0.5)'</span>, 
      });
    }

    <span class="hljs-comment">//画固定线条的 canvas</span>
    <span class="hljs-keyword">let</span> lineCanvas = circleCanvas.cloneNode(<span class="hljs-literal">true</span>);

    <span class="hljs-comment">//画不固定线条的 canvas</span>
    <span class="hljs-keyword">let</span> moveCanvas = circleCanvas.cloneNode(<span class="hljs-literal">true</span>);

    container.appendChild(lineCanvas);
    container.appendChild(moveCanvas);
    container.appendChild(circleCanvas);

    <span class="hljs-keyword">this</span>.lineCanvas = lineCanvas;
    <span class="hljs-keyword">this</span>.moveCanvas = moveCanvas;
    <span class="hljs-keyword">this</span>.circleCanvas = circleCanvas;

    <span class="hljs-keyword">this</span>.container.addEventListener(<span class="hljs-string">'touchmove'</span>, 
      evt =&gt; evt.preventDefault(), {passive: <span class="hljs-literal">false</span>});

    <span class="hljs-keyword">this</span>.clearPath();
    <span class="hljs-keyword">return</span> <span class="hljs-literal">true</span>;
  }
  clearPath(){
    <span class="hljs-keyword">if</span>(!<span class="hljs-keyword">this</span>.circleCanvas) <span class="hljs-keyword">this</span>.render();

    <span class="hljs-keyword">let</span> {circleCanvas, lineCanvas, moveCanvas} = <span class="hljs-keyword">this</span>,
        circleCtx = circleCanvas.getContext(<span class="hljs-string">'2d'</span>),
        lineCtx = lineCanvas.getContext(<span class="hljs-string">'2d'</span>),
        moveCtx = moveCanvas.getContext(<span class="hljs-string">'2d'</span>),
        width = circleCanvas.width,
        {n, fgColor, innerRadius} = <span class="hljs-keyword">this</span>.options;

    circleCtx.clearRect(<span class="hljs-number">0</span>, <span class="hljs-number">0</span>, width, width);
    lineCtx.clearRect(<span class="hljs-number">0</span>, <span class="hljs-number">0</span>, width, width);
    moveCtx.clearRect(<span class="hljs-number">0</span>, <span class="hljs-number">0</span>, width, width);

    <span class="hljs-keyword">let</span> range = <span class="hljs-built_in">Math</span>.round(width / (n + <span class="hljs-number">1</span>));

    <span class="hljs-keyword">let</span> circles = [];

    <span class="hljs-comment">//drawCircleCenters</span>
    <span class="hljs-keyword">for</span>(<span class="hljs-keyword">let</span> i = <span class="hljs-number">1</span>; i &lt;= n; i++){
      <span class="hljs-keyword">for</span>(<span class="hljs-keyword">let</span> j = <span class="hljs-number">1</span>; j &lt;= n; j++){
        <span class="hljs-keyword">let</span> y = range * i, x = range * j;
        drawSolidCircle(circleCtx, fgColor, x, y, innerRadius);
        <span class="hljs-keyword">let</span> circlePoint = {x, y};
        circlePoint.pos = [i, j];
        circles.push(circlePoint);
      }
    }

    <span class="hljs-keyword">this</span>.circles = circles;
  }
  <span class="hljs-keyword">async</span> cancel(){
    <span class="hljs-keyword">if</span>(<span class="hljs-keyword">this</span>.recordingTask){
      <span class="hljs-keyword">return</span> <span class="hljs-keyword">this</span>.recordingTask.cancel();
    }
    <span class="hljs-keyword">return</span> <span class="hljs-built_in">Promise</span>.resolve({err: <span class="hljs-keyword">new</span> <span class="hljs-built_in">Error</span>(Recorder.ERR_NO_TASK)});
  }
  <span class="hljs-keyword">async</span> record(){
    <span class="hljs-keyword">if</span>(<span class="hljs-keyword">this</span>.recordingTask) <span class="hljs-keyword">return</span> <span class="hljs-keyword">this</span>.recordingTask.promise;

    <span class="hljs-keyword">let</span> {circleCanvas, lineCanvas, moveCanvas, options} = <span class="hljs-keyword">this</span>,
        circleCtx = circleCanvas.getContext(<span class="hljs-string">'2d'</span>),
        lineCtx = lineCanvas.getContext(<span class="hljs-string">'2d'</span>),
        moveCtx = moveCanvas.getContext(<span class="hljs-string">'2d'</span>);

    circleCanvas.addEventListener(<span class="hljs-string">'touchstart'</span>, ()=&gt;{
      <span class="hljs-keyword">this</span>.clearPath();
    });

    <span class="hljs-keyword">let</span> records = [];

    <span class="hljs-keyword">let</span> handler = evt =&gt; {
      <span class="hljs-keyword">let</span> {clientX, clientY} = evt.changedTouches[<span class="hljs-number">0</span>],
          {bgColor, focusColor, innerRadius, outerRadius, touchRadius} = options,
          touchPoint = getCanvasPoint(moveCanvas, clientX, clientY);

      <span class="hljs-keyword">for</span>(<span class="hljs-keyword">let</span> i = <span class="hljs-number">0</span>; i &lt; <span class="hljs-keyword">this</span>.circles.length; i++){
        <span class="hljs-keyword">let</span> point = <span class="hljs-keyword">this</span>.circles[i],
            x0 = point.x,
            y0 = point.y;

        <span class="hljs-keyword">if</span>(distance(point, touchPoint) &lt; touchRadius){
          drawSolidCircle(circleCtx, bgColor, x0, y0, outerRadius);
          drawSolidCircle(circleCtx, focusColor, x0, y0, innerRadius);
          drawHollowCircle(circleCtx, focusColor, x0, y0, outerRadius);

          <span class="hljs-keyword">if</span>(records.length){
            <span class="hljs-keyword">let</span> p2 = records[records.length - <span class="hljs-number">1</span>],
                x1 = p2.x,
                y1 = p2.y;

            drawLine(lineCtx, focusColor, x0, y0, x1, y1);
          }

          <span class="hljs-keyword">let</span> circle = <span class="hljs-keyword">this</span>.circles.splice(i, <span class="hljs-number">1</span>);
          records.push(circle[<span class="hljs-number">0</span>]);
          <span class="hljs-keyword">break</span>;
        }
      }

      <span class="hljs-keyword">if</span>(records.length){
        <span class="hljs-keyword">let</span> point = records[records.length - <span class="hljs-number">1</span>],
            x0 = point.x,
            y0 = point.y,
            x1 = touchPoint.x,
            y1 = touchPoint.y;

        moveCtx.clearRect(<span class="hljs-number">0</span>, <span class="hljs-number">0</span>, moveCanvas.width, moveCanvas.height);
        drawLine(moveCtx, focusColor, x0, y0, x1, y1);        
      }
    };


    circleCanvas.addEventListener(<span class="hljs-string">'touchstart'</span>, handler);
    circleCanvas.addEventListener(<span class="hljs-string">'touchmove'</span>, handler);

    <span class="hljs-keyword">let</span> recordingTask = {};
    <span class="hljs-keyword">let</span> promise = <span class="hljs-keyword">new</span> <span class="hljs-built_in">Promise</span>((resolve, reject) =&gt; {
      recordingTask.cancel = (res = {}) =&gt; {
        <span class="hljs-keyword">let</span> promise = <span class="hljs-keyword">this</span>.recordingTask.promise;

        res.err = res.err || <span class="hljs-keyword">new</span> <span class="hljs-built_in">Error</span>(Recorder.ERR_USER_CANCELED);
        circleCanvas.removeEventListener(<span class="hljs-string">'touchstart'</span>, handler);
        circleCanvas.removeEventListener(<span class="hljs-string">'touchmove'</span>, handler);
        <span class="hljs-built_in">document</span>.removeEventListener(<span class="hljs-string">'touchend'</span>, done);
        resolve(res);
        <span class="hljs-keyword">this</span>.recordingTask = <span class="hljs-literal">null</span>;

        <span class="hljs-keyword">return</span> promise;
      }

      <span class="hljs-keyword">let</span> done = evt =&gt; {
        moveCtx.clearRect(<span class="hljs-number">0</span>, <span class="hljs-number">0</span>, moveCanvas.width, moveCanvas.height);
        <span class="hljs-keyword">if</span>(!records.length) <span class="hljs-keyword">return</span>;

        circleCanvas.removeEventListener(<span class="hljs-string">'touchstart'</span>, handler);
        circleCanvas.removeEventListener(<span class="hljs-string">'touchmove'</span>, handler);
        <span class="hljs-built_in">document</span>.removeEventListener(<span class="hljs-string">'touchend'</span>, done);

        <span class="hljs-keyword">let</span> err = <span class="hljs-literal">null</span>;

        <span class="hljs-keyword">if</span>(records.length &lt; options.minPoints){
          err = <span class="hljs-keyword">new</span> <span class="hljs-built_in">Error</span>(Recorder.ERR_NOT_ENOUGH_POINTS);
        }

        <span class="hljs-comment">//这里可以选择一些复杂的编码方式，本例子用最简单的直接把坐标转成字符串</span>
        <span class="hljs-keyword">let</span> res = {err, records: records.map(o =&gt; o.pos.join(<span class="hljs-string">''</span>)).join(<span class="hljs-string">''</span>)};

        resolve(res);
        <span class="hljs-keyword">this</span>.recordingTask = <span class="hljs-literal">null</span>;
      };
      <span class="hljs-built_in">document</span>.addEventListener(<span class="hljs-string">'touchend'</span>, done);
    });

    recordingTask.promise = promise;

    <span class="hljs-keyword">this</span>.recordingTask = recordingTask;

    <span class="hljs-keyword">return</span> promise;
  }
}
</code></pre>
<p>它的几个公开的方法，recorder 负责记录绘制结果， clearPath 负责在画布上清除上一次记录的结果，cancel 负责终止记录过程，这是为后续流程准备的。</p>
<h3>流程设计</h3>
<p>接下来我们基于 Recorder 来设计设置和验证密码的流程：</p>
<h4>验证密码</h4>
<p><img src="https://p5.ssl.qhimg.com/t01c6fccad2c6c01576.png" alt=""></p>
<h4>设置密码</h4>
<p><img src="https://p4.ssl.qhimg.com/t0122f23e6530a7b6fb.png" alt=""></p>
<p>有了前面异步 Promise API 的 Recorder，我们不难实现上面的两个流程。</p>
<p><strong>验证密码的内部流程</strong></p>
<pre><code class="hljs lang-js"><span class="hljs-keyword">async</span> check(password){
  <span class="hljs-keyword">if</span>(<span class="hljs-keyword">this</span>.mode !== Locker.MODE_CHECK){
    <span class="hljs-keyword">await</span> <span class="hljs-keyword">this</span>.cancel();
    <span class="hljs-keyword">this</span>.mode = Locker.MODE_CHECK;
  }  

  <span class="hljs-keyword">let</span> checked = <span class="hljs-keyword">this</span>.options.check.checked;

  <span class="hljs-keyword">let</span> res = <span class="hljs-keyword">await</span> <span class="hljs-keyword">this</span>.record();

  <span class="hljs-keyword">if</span>(res.err &amp;&amp; res.err.message === Locker.ERR_USER_CANCELED){
    <span class="hljs-keyword">return</span> <span class="hljs-built_in">Promise</span>.resolve(res);
  }

  <span class="hljs-keyword">if</span>(!res.err &amp;&amp; password !== res.records){
    res.err = <span class="hljs-keyword">new</span> <span class="hljs-built_in">Error</span>(Locker.ERR_PASSWORD_MISMATCH)
  }

  checked.call(<span class="hljs-keyword">this</span>, res);
  <span class="hljs-keyword">this</span>.check(password);
  <span class="hljs-keyword">return</span> <span class="hljs-built_in">Promise</span>.resolve(res);
}
</code></pre>
<p><strong>设置密码的内部流程</strong></p>
<pre><code class="hljs lang-js"><span class="hljs-keyword">async</span> update(){
  <span class="hljs-keyword">if</span>(<span class="hljs-keyword">this</span>.mode !== Locker.MODE_UPDATE){
    <span class="hljs-keyword">await</span> <span class="hljs-keyword">this</span>.cancel();
    <span class="hljs-keyword">this</span>.mode = Locker.MODE_UPDATE;
  }

  <span class="hljs-keyword">let</span> beforeRepeat = <span class="hljs-keyword">this</span>.options.update.beforeRepeat, 
      afterRepeat = <span class="hljs-keyword">this</span>.options.update.afterRepeat;

  <span class="hljs-keyword">let</span> first = <span class="hljs-keyword">await</span> <span class="hljs-keyword">this</span>.record();

  <span class="hljs-keyword">if</span>(first.err &amp;&amp; first.err.message === Locker.ERR_USER_CANCELED){
    <span class="hljs-keyword">return</span> <span class="hljs-built_in">Promise</span>.resolve(first);
  }

  <span class="hljs-keyword">if</span>(first.err){
    <span class="hljs-keyword">this</span>.update();
    beforeRepeat.call(<span class="hljs-keyword">this</span>, first);
    <span class="hljs-keyword">return</span> <span class="hljs-built_in">Promise</span>.resolve(first);   
  }

  beforeRepeat.call(<span class="hljs-keyword">this</span>, first);

  <span class="hljs-keyword">let</span> second = <span class="hljs-keyword">await</span> <span class="hljs-keyword">this</span>.record();      

  <span class="hljs-keyword">if</span>(second.err &amp;&amp; second.err.message === Locker.ERR_USER_CANCELED){
    <span class="hljs-keyword">return</span> <span class="hljs-built_in">Promise</span>.resolve(second);
  }

  <span class="hljs-keyword">if</span>(!second.err &amp;&amp; first.records !== second.records){
    second.err = <span class="hljs-keyword">new</span> <span class="hljs-built_in">Error</span>(Locker.ERR_PASSWORD_MISMATCH);
  }

  <span class="hljs-keyword">this</span>.update();
  afterRepeat.call(<span class="hljs-keyword">this</span>, second);
  <span class="hljs-keyword">return</span> <span class="hljs-built_in">Promise</span>.resolve(second);
}
</code></pre>
<p>可以看到，有了 Recorder 之后，Locker 的验证和设置密码基本上就是顺着流程用 async/await 写下来就行了。</p>
<h3>细节问题</h3>
<p>实际手机触屏时，如果上下拖动，浏览器有默认行为，会导致页面上下移动，需要阻止 touchmove 的默认事件。</p>
<pre><code class="hljs lang-js"><span class="hljs-keyword">this</span>.container.addEventListener(<span class="hljs-string">'touchmove'</span>, 
      evt =&gt; evt.preventDefault(), {passive: <span class="hljs-literal">false</span>});
</code></pre>
<p>这里仍然需要注意的一点是， touchmove 事件在 chrome 下默认是一个 ，因此 addEventListener 的时候需要传参 {passive: false}，否则的话不能 preventDefault。</p>
<h3>工具 &amp; 工程化</h3>
<p>因为我们的代码使用了 ES6+，所以需要引入 babel 编译，我们的组件也使用 webpack 进行打包，以便于使用者在浏览器中直接引入。</p>
<p>这方面的内容，在之前的博客里，这里就不再一一说明。</p>
<p>最后，具体的代码可以直接查看 。</p>
<h2>总结</h2>
<p>以上就是今天要讲的全部内容，这里面有几个点我想再强调一下：</p>
<ol>
<li>在设计 API 的时候思考真正的需求，判断什么该开放、什么该封装</li>
<li>做好技术调研和核心方案研究，选择合适的方案</li>
<li>优化和解决细节问题</li>
</ol>
<p>最后，如有任何问题，欢迎大家在下方评论区探讨。</p>
---------------
<h1 id="#title_1" >2、It’s Time To Start Using CSS Custom Properties</h1>
Serg Hospodarets
[https://www.smashingmagazine.com/2017/04/start-using-css-custom-properties/](https://www.smashingmagazine.com/2017/04/start-using-css-custom-properties/)
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
</table><p>Today, CSS preprocessors are a standard for web development. One of the main advantages of preprocessors is that they enable you to use variables. This helps you to avoid copying and pasting code, and it simplifies development and refactoring.</p>

<figure></figure>

<p>We use preprocessors to store colors, font preferences, layout details — mostly everything we use in CSS. But preprocessor variables have some limitations.</p><p>The post .</p>
---------------
<h1 id="#title_2" >3、Java EE 8终于给出即将完成的迹象</h1>
Michael Redlich
[http://www.infoq.com/cn/news/2017/04/long-road-for-java-ee-8?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/04/long-road-for-java-ee-8?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p> Java EE 8终于给出了即将完成的迹象。Oracle在近期的博客帖子中，更新了Java社区中Java EE 8的相关活动情况，其中给出了最新的发布时间表和更新的JSR活动。历经近四年的开发，Java EE 8的实现之路充满坎坷。</p> <i>By Michael Redlich</i> <i> Translated by Rays</i>
---------------
<h1 id="#title_3" >4、文章： 大数据管理平台Apache Geode 分布式系统内部结构剖析</h1>
杨旭钧
[http://www.infoq.com/cn/articles/internal-structure-of-apache-geode-distributed-system?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/internal-structure-of-apache-geode-distributed-system?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/internal-structure-of-apache-geode-distributed-system/zh/smallimage/logo 112 (6).jpg"/><p>Apache Geode于去年11月从Apache孵化器毕业成为顶级项目，是一个相当成熟、强健的的数据管理平台，提供实时的、一致的、贯穿整个云架构地访问数据关键型应用。Geode自身功能比较多，首先它是一个基于JVM的NoSQL分布式数据处理平台，同时集中间件、缓存、消息队列、事件处理引擎、NoSQL数据库于一身的分布式内存数据处理平台。</p> <i>By 杨旭钧</i>
---------------
<h1 id="#title_4" >5、自动化数据科学与机器学习：Auto-sklearn开发团队访谈</h1>
Matthew Mayo
[http://www.infoq.com/cn/news/2017/04/Automated-science-Auto-sklearn?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/04/Automated-science-Auto-sklearn?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>在最近由Kdnuggets举办的自动化数据科学与机器学习博客大赛中，Auto-sklearn开发团队勇夺了冠军。Matthew Mayo采访了Auto-sklearn开发团队，了解了Auto-sklearn项目的基本情况，以及开发人员的背景和自动化数据科学的动态。</p> <i>By Matthew Mayo</i> <i> Translated by 刘志勇</i>
---------------
<h1 id="#title_5" >6、未来的.NET之多重继承</h1>
Jonathan Allen
[http://www.infoq.com/cn/news/2017/04/Clr-Default-Methods?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/04/Clr-Default-Methods?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/news/2017/04/Clr-Default-Methods/zh/headerimage/GettyImages-481062930.jpg"/><p>通过抽象接口引入有限形式的多重继承，这一.NET新提议颇具争议性。该特性是受Java默认方法（Default Methods）的启发。</p> <i>By Jonathan Allen</i> <i> Translated by Rays</i>
---------------
<h1 id="#title_6" >7、视频演讲： 当你的团队还支撑不起梦想时</h1>
杨荣伟
[http://www.infoq.com/cn/presentations/when-your-team-can-not-afford-to-dream?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/when-your-team-can-not-afford-to-dream?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/when-your-team-can-not-afford-to-dream/zh/mediumimage/yangrongwei270.jpg"/><p>随着国内互联网创业大潮的兴起，越来越多有经验的技术人员跳出原有公司成熟体系的舒适圈，加入了初创公司。然而管理初创技术团队与成熟技术团队的方式方法上存在诸多本质上的不同，照搬成熟公司管理经验的后果往往会被现实撞的头破血流。

演讲人亲身经历过一家互联网公司从十人规模团队成长为千人规模团队的全过程，并在公司担任技术学院院长，承担工程师的入职培训与专业晋升培训，对初创团队如何成长为能支撑起梦想的团队有着不一样的深刻体会。演讲会重点分享如何打造成长型团队的实战经验，帮助各位加入初创公司的技术管理者少走弯路。</p> <i>By 杨荣伟</i>
---------------
<h1 id="#title_7" >8、PostgreSQL 10新特性概述</h1>
Sergio De Simone
[http://www.infoq.com/cn/news/2017/04/postgresql-10-features?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/04/postgresql-10-features?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>PostgreSQL继续向着将在2017年9月份发布的第10个主版本迈进，EnterpriseDB首席架构师和PostgreSQL贡献者Robert Hass根据PostgreSQL官方路线图编制了一份PostgreSQL 10重要特性列表。</p> <i>By Sergio De Simone</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_8" >9、FaunaDB：一款由前Twitter技术负责人创建的新的分布式数据库</h1>
Abel Avram
[http://www.infoq.com/cn/news/2017/04/faunadb?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/04/faunadb?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>前Twitter技术负责人和Couchbase一起创建了一款新的通用时态数据库FaunaDB。</p> <i>By Abel Avram</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_9" >10、文章： 开发高质量软件的区别因素</h1>
Cynthia Freeney
[http://www.infoq.com/cn/articles/quality-software-factors?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/quality-software-factors?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/quality-software-factors/zh/smallimage/logo.jpg"/><p>软件质量可达到的水平反映了一个组织的经营决策。有许多因素影响这个决策，包括开发、构建和测试环境的有效性，资源和相关技能、诚信、积极性和经验水平、商业协议，以及采用的流程和产能工具。</p> <i>By Cynthia Freeney</i> <i> Translated by 冬雨</i>
---------------
<h1 id="#title_10" >11、文章： 解密大规模的API优先转型：来自PayPal的课程（第二部）</h1>
Erik Hogan
[http://www.infoq.com/cn/articles/paypal-api-first-part2?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/paypal-api-first-part2?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/paypal-api-first-part2/zh/headerimage/GettyImages-537447438.jpg"/><p>第二堂课（总共三次）探究了PayPal是如何应用更多的API优先方法来构建平台服务的。在这篇文章中，我们将会深入了解PayPal是如何管理它们的API组合（Portfolio）的。</p> <i>By Erik Hogan</i> <i> Translated by 罗远航</i>
---------------
<h1 id="#title_11" >12、文章： 火力全开：大数据领域2017年全景剖析</h1>
Matt Turck
[http://www.infoq.com/cn/articles/the-2017-big-data-landscape?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/the-2017-big-data-landscape?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/the-2017-big-data-landscape/zh/smallimage/logo (30).jpg"/><p>数据生态系统在2017年终于实现了火力全开。本文为大家提供了一个有关大数据领域详细的“国情咨文”，以及投资机构针对这一行业的见解和关键趋势。</p> <i>By Matt Turck</i> <i> Translated by 大愚若智</i>
---------------
<h1 id="#title_12" >13、A Brief Overview On Responsive Navigation Patterns</h1>
Chris Poteet
[https://www.smashingmagazine.com/2017/04/overview-responsive-navigation-patterns/](https://www.smashingmagazine.com/2017/04/overview-responsive-navigation-patterns/)
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
</table><p>To say that <strong>responsive web design has changed our industry</strong> would be an understatement at best. We used to ask our clients which resolutions and devices they wanted us to support, but we now know the answer is “as many as possible.” To answer a challenge like this and to handle our increasingly complex world, our industry has exploded with new thinking, patterns and approaches.</p>

<figure></figure>

<p>In this article, I want to look specifically at the issue of responsive navigation. We will first talk about information architecture, then the purpose of navigation, and finally we will look at three responsive navigation patterns that have served well over time.</p><p>The post .</p>
---------------