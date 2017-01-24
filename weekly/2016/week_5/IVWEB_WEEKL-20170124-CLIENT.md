## 文章索引
1、 <a href="#1文章-android蓝牙ble集成多设备最佳实践" >文章： Android蓝牙BLE集成多设备最佳实践</a><br/>
2、 <a href="#2译征服-javascript-面试:-什么是函数式编程|-eric-elliott" >【译】征服 JavaScript 面试: 什么是函数式编程？| Eric Elliott</a><br/>
3、 <a href="#3译征服-javascript-面试什么是闭包" >【译】征服 JavaScript 面试：什么是闭包？</a><br/>
4、 <a href="#4webpack-2最终版本发布聚焦文档内容提升" >Webpack 2最终版本发布，聚焦文档内容提升</a><br/>
5、 <a href="#5视频演讲-链家网高可用架构演进" >视频演讲： 链家网高可用架构演进</a><br/>
6、 <a href="#6文章-组合使用laravel和vfsstream测试文件上传" >文章： 组合使用Laravel和vfsStream测试文件上传</a><br/>
7、 <a href="#7营销部门投资ai前应思考的3个问题" >营销部门投资AI前应思考的3个问题</a><br/>
8、 <a href="#8看法2017会带给我们的文化和方法" >看法：2017会带给我们的文化和方法</a><br/>
9、 <a href="#9如何写出好的-javascript-浅谈-api-设计" >如何写出好的 JavaScript —— 浅谈 API 设计</a><br/>
10、 <a href="#10microsoft-edge更新支持webvr使flash可以即点即运行" >Microsoft Edge更新：支持WebVR，使Flash可以即点即运行</a><br/>
11、 <a href="#11java-10将带来升级版的lambda" >Java 10将带来升级版的Lambda</a><br/>
12、 <a href="#125分钟现场撸代码谈总结会抽奖程序" >5分钟现场撸代码——谈总结会抽奖程序</a><br/>
13、 <a href="#13fex-技术周刊---2017/01/23" >FEX 技术周刊 - 2017/01/23</a><br/>
14、 <a href="#14为什么-是-false-而-!!-是-true" >为什么 [ ] 是 false 而 !![ ] 是 true</a><br/>
15、 <a href="#15文章-包容协作与静默实验" >文章： 包容协作与静默实验</a><br/>
16、 <a href="#16视频演讲-携程多机房微服务灰度发布" >视频演讲： 携程多机房微服务灰度发布</a><br/>
17、 <a href="#17a-case-study:-is-app-indexing-for-google-worth-the-effort" >A Case Study: Is App Indexing For Google Worth The Effort?</a><br/><h1 id="#title_0" >1、文章： Android蓝牙BLE集成多设备最佳实践</h1>
章星星
[http://www.infoq.com/cn/articles/android-bluetooth-ble?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/android-bluetooth-ble?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/android-bluetooth-ble/zh/smallimage/java-logo2.jpg"/><p>公司开发了一款健康类APP，用户可以通过APP连接外部蓝牙BLE设备采集血糖，血压，体重等多个常见健康类指标。因此APP需要同时集成多款设备（多个品牌的血糖仪，血压计，体脂秤等）。每个厂家的设备对接协议是不同的，甚至连同一个设备的不同版本，协议都会有差距。在一个APP中跟多个设备对接，甚至在同一个界面中需要处理多个设备，界面跟协议混在一起，成为一个比较头疼的问题。本文对如何在APP中支持多设备集成，并且在需要对接新设备的时候，容易扩展现有代码提供了一个比较好的实践思路。</p> <i>By 章星星</i>
---------------
<h1 id="#title_1" >2、【译】征服 JavaScript 面试: 什么是函数式编程？| Eric Elliott</h1>

[https://www.h5jun.com/post/master-the-javascript-interview-what-is-functional-programming.html](https://www.h5jun.com/post/master-the-javascript-interview-what-is-functional-programming.html)
<div class="toc"><ul>
<li></li>
<li></li>
<li></li>
<li><ul>
<li></li>
</ul>
</li>
<li></li>
<li></li>
<li></li>
<li></li>
</ul>
</div><blockquote>
<p>原文：</p>
</blockquote>
<p><img src="https://p.ssl.qhimg.com/t01c79775dce5c2651e.jpg" alt=""></p>
<p>函数式编程在 JavaScript 界已经成为了一个非常热门的话题。而仅在几年之前，还几乎没有 JavaScript 程序员了解函数式编程是什么，但在最近三年里，我看到非常多的应用程序代码库里大量使用着函数式编程思想。</p>
<!--more-->
<p><strong>函数式编程</strong> （通常简称为 FP）是指通过复合<strong>纯函数</strong>来构建软件的过程，它避免了<strong>共享的状态（share state）</strong>、<strong>易变的数据(mutable data)</strong>、以及<strong>副作用(side-effects)</strong>。函数式编程是<strong>声明式</strong>而不是<strong>命令式</strong>，并且应用程序状态通过纯函数流转。对比面向对象编程，后者的应用程序状态通常是共享并共用于对象方法。</p>
<p>函数式编程是一种<strong>编程范式</strong>意味着它是一种软件构建的思维方式，有着自己的理论基础和界定法则。其他编程范式的例子包括面向对象编程和过程式编程。</p>
<p>与命令式或面向对象代码相比，函数式代码倾向于更简洁、更可预测以及更易于测试 —— 但是如果你对它以及与它相关的常见模式不熟悉，读函数式代码会让你觉得信息量太大，而且相关文献对于初学者来说往往难以理解。</p>
<p>如果你开始 google 函数式编程的术语，你很可能一下子碰壁，那些学术术语对新人来说着实有点吓人。它有一个非常陡峭的学习曲线。但是如果你已经用 JavaScript 写了一段时间的代码，你很可能不知不觉中在你的软件里已经使用了很多函数式编程原理和功能。</p>
<blockquote>
<p>不要让那些新名词把你吓跑。实际上它比你所听说的要简单很多。</p>
</blockquote>
<p>最难的部分是记住那些以前不熟悉的词汇。在这些名词定义中蕴含了许多思想，你只有理解了它们，才能够开始掌握函数式编程真正的意义：</p>
<ul>
<li>纯函数（Pure functions）</li>
<li>函数复合（Function composition）</li>
<li>避免共享状态（Avoid shared state）</li>
<li>避免改变状态（Avoid mutating state）</li>
<li>避免副作用（Avoid side effects）</li>
</ul>
<p>换句话说，如果你想要了解函数式编程在实际中的意义，你需要从理解那些核心概念开始。</p>
<p>一个<strong>纯函数</strong>是这样的一个函数：</p>
<ul>
<li>给它同样的输入，总是返回同样的结果，并且</li>
<li>没有副作用</li>
</ul>
<p>纯函数有着许多对函数式编程而言非常重要的属性，包括<strong>引用透明</strong>（你可以将一个函数调用替换成它的结果值，而不会对程序的运行造成影响）。获取更多细节，可以阅读。</p>
<p>函数复合是结合两个或多个函数，从而产生一个新函数或进行某些计算的过程。例如，复合操作 <code>f·g</code>（点号意思是对两者执行复合运算）在 JavaScript 中相当于执行 <code>f(g(x))</code>。理解函数复合是理解软件如何用函数式编程模型来构建的很重要的一步。获取更多细节，可以阅读。</p>
<h3 id="toc-283">共享状态</h3>
<p><strong>共享状态</strong> 的意思是任意变量、对象或者内存空间存在于共享作用域下，或者作为对象的属性在各个作用域之间被传递。共享作用域包括全局作用域和闭包作用域。通常，在面向对象编程中，对象以添加属性到其他对象上的方式在作用域之间共享。</p>
<p>举个例子，一个电脑游戏可能会控制一个游戏对象（game object），它上面有角色(characters)和游戏道具（items），这些数据作为属性存储在游戏对象之上。而函数式编程避免共享状态 —— 与前者不同地，它依赖于不可变数据结构和纯粹的计算过程来从已存在的数据中派生出新的数据。要获取更多关于软件开发如何使用函数式编程处理应用程序状态的详细内容，可以阅读。</p>
<p>共享状态的问题是为了理解函数的作用，你需要了解那个函数所用到的全部共享变量的变化历史。</p>
<p>想象你有一个 user 对象需要保存。你的 <code>saveUser()</code> 函数向服务器 API 发起一个请求。此时，用户改变了他们的头像，通过 <code>updateAvatar()</code> 并触发了另一次 <code>saveUser()</code> 请求。在保存动作执行后，服务器返回一个更新的 user 对象，客户端要将这个对象替换内存中的对象，以保持与服务器同步。</p>
<p>不幸地是，第二次请求有可能比第一次请求更早返回，所以当第一次请求（现在已经过时了）返回时，新的头像又从内存中丢失了，被替换回旧的头像。这是一个同步竞争的例子，是一个非常常见的共享状态 bug。</p>
<p>共享状态的另一个常见问题是改变函数调用次序可能导致一连串的错误，因为函数操作共享数据是依时序的：</p>
<pre><code class="hljs lang-dart"><span class="hljs-comment">//使用共享数据，函数调用的次序会改变函数调用的结果</span>
<span class="hljs-keyword">const</span> x = {
  val: <span class="hljs-number">2</span>
};

<span class="hljs-keyword">const</span> x1 = () =&gt; x.val += <span class="hljs-number">1</span>;

<span class="hljs-keyword">const</span> x2 = () =&gt; x.val *= <span class="hljs-number">2</span>;

x1();
x2();

console.log(x.val); <span class="hljs-comment">// 6</span>

<span class="hljs-comment">//下面的例子与上面的相同，除了……</span>
<span class="hljs-keyword">const</span> y = {
  val: <span class="hljs-number">2</span>
};

<span class="hljs-keyword">const</span> y1 = () =&gt; y.val += <span class="hljs-number">1</span>;

<span class="hljs-keyword">const</span> y2 = () =&gt; y.val *= <span class="hljs-number">2</span>;

<span class="hljs-comment">// ...函数的调用次序颠倒了一下...</span>
y2();
y1();

<span class="hljs-comment">// ... 这改变了结果值:</span>
console.log(y.val); <span class="hljs-comment">// 5</span>
</code></pre><p>如果你避免共享状态，函数的调用时序不同就不会改变函数的调用结果。使用纯函数，给定同样的输入，你将总是能得到同样的输出。这使得函数调用完全独立于其他函数调用，可以从根本上简化变更和重构。改变函数内容，或者改变函数调用的时序不会波及和破坏程序的其他部分。</p>
<pre><code class="hljs lang-kotlin">const x = {
  <span class="hljs-variable"><span class="hljs-keyword">val</span></span>: <span class="hljs-number">2</span>
};

const x1 = x =&gt; Object.assign({}, x, { <span class="hljs-variable"><span class="hljs-keyword">val</span></span>: x.<span class="hljs-keyword">val</span> + <span class="hljs-number">1</span>});

const x2 = x =&gt; Object.assign({}, x, { <span class="hljs-variable"><span class="hljs-keyword">val</span></span>: x.<span class="hljs-keyword">val</span> * <span class="hljs-number">2</span>});

console.log(x1(x2(x)).<span class="hljs-keyword">val</span>); <span class="hljs-comment">// 5</span>


const y = {
  <span class="hljs-variable"><span class="hljs-keyword">val</span></span>: <span class="hljs-number">2</span>
};

<span class="hljs-comment">//由于它对于外部变量没有依赖,</span>
<span class="hljs-comment">//我们不需要不同的函数来操作不同的变量</span>

<span class="hljs-comment">//这里故意留白</span>


<span class="hljs-comment">//由于函数没有操作可变数据，你可以调用这些函数任意次，用各种次序</span>
<span class="hljs-comment">//都不会改变之后调用函数的结果值。</span>
x2(y);
x1(y);

console.log(x1(x2(y)).<span class="hljs-keyword">val</span>); <span class="hljs-comment">// 5</span>
</code></pre><p>在上面的例子里，我们使用了 <code>Object.assign()</code> 并传入一个空的 object 作为第一个参数来拷贝 x 的属性，以防止 x 在函数内部被改变。在这个例子里，它等价由于重新创建一个对象，而这是一种 JavaScript 里的通用模式， 用来拷贝已存在状态而不是使用引用，从而避免像我们第一个例子里产生的问题。</p>
<p>如果你仔细看例子里的 <code>console.log()</code> 语句，你会发现我前面已经提到过的概念：函数复合。回顾一下，函数复合看起来像是这样：<code>f(g(x))</code>。在这个例子里，我们的 <code>f()</code> 和 <code>g()</code> 是 <code>x1()</code> 和 <code>x2()</code>，所以复合是 <code>x1·x2</code>。</p>
<p>当然，如果你改变复合的顺序，输出将改变。操作的顺序仍然很重要。<code>f(g(x))</code> 并不总是等价于 <code>g(f(x))</code>，但是，有一件事情发生了改变，那就是函数外部的变量不会被修改 —— 原本函数修改外部变量是一个大问题。要是函数不纯，我们如果不了解函数使用或操作的每个变量的完整历史，就不可能完全理解它做了什么。</p>
<p>移除函数时序依赖，你就完全消除了一大类潜在的 bug。</p>
<h3 id="toc-4ac">不可变性</h3>
<p>一个<strong>不可变的（immutable）</strong>对象是指一个对象不会在它创建之后被改变。对应地，一个<strong>可变的(mutable)</strong>对象是指任何在创建之后可以被改变的对象。</p>
<p>不可变性是函数式编程的一个核心概念，因为没有它，你的程序中的数据流是有损的。状态历史被抛弃而奇怪的 bug 可能会在你的软件中产生。关于更多不变性的意义，阅读 。</p>
<p>在 JavaScript 中，很重要的一点是不要混淆了 <code>const</code> 和不变性。<code>const</code> 创建一个变量绑定，让该变量不能再次被赋值。<code>const</code> 并不创建不可变对象。你虽然不能改变绑定到这个变量名上的对象，但你仍然可以改变它的属性，这意味着 <code>const</code> 的变量仍然是可变的，而不是不可变的。</p>
<p>不可变对象完全不能被改变。你可以通过深度冻结对象来创造一个真正的不可变的值。JavaScript 提供了一个方法，能够浅冻结一个对象：</p>
<pre><code class="hljs lang-qml"><span class="hljs-keyword">const</span> a = <span class="hljs-built_in">Object</span>.freeze({
  <span class="hljs-attribute">foo</span>: <span class="hljs-string">"Hello"</span>,
  <span class="hljs-attribute">bar</span>: <span class="hljs-string">"world"</span>,
  <span class="hljs-attribute">baz</span>: <span class="hljs-string">"!"</span>
});

a.foo = <span class="hljs-string">"Goodbye"</span>;
<span class="hljs-comment">// Error: Cannot assign to read only property "foo" of object Object</span>
</code></pre><p>然而冻结的对象只是表面一层不可变，例如，深层的属性还是可以被改变：</p>
<pre><code class="hljs lang-qml"><span class="hljs-keyword">const</span> a = <span class="hljs-built_in">Object</span>.freeze({
  <span class="hljs-attribute">foo</span>: { <span class="hljs-attribute">greeting</span>: <span class="hljs-string">"Hello"</span> },
  <span class="hljs-attribute">bar</span>: <span class="hljs-string">"world"</span>,
  <span class="hljs-attribute">baz</span>: <span class="hljs-string">"!"</span>
});

a.foo.greeting = <span class="hljs-string">"Goodbye"</span>;

<span class="hljs-built_in">console</span>.log(<span class="hljs-string">`<span class="hljs-subst">${ a.foo.greeting }</span>, <span class="hljs-subst">${ a.bar }</span><span class="hljs-subst">${a.baz}</span>`</span>);
</code></pre><p>如你所见，被冻结的 object 的顶层基本属性不能被改变，但是如果有一个属性本身也是 object（包括数组等），它依然可以被改变 —— 因此甚至被冻结的对象也不是不可变的，除非你遍历整个对象树并冻结每一个对象属性。</p>
<p>在许多函数式编程语言中，有特殊的不可变数据结构，被称为 <strong>trie 数据结构</strong>(trie 的发音为 tree)，这一结构有效地深冻结 —— 意味任何属性无论它的对象层级如何都不能被改变。</p>
<p>当一个对象被拷贝给一个操作符时，tries 使用<strong>结构共享</strong>来共用不可变对象的引用内存地址，这减少内存占用，而且能够显著地改善一些类型的操作的性能。</p>
<p>例如，你可以使用 ID 来比较对象，如果两个对象的根 ID 相同，你不需要继续遍历比较整个对象树来寻找差异。</p>
<p>有一些 JavaScript 的库使用了 tries，包括 。</p>
<p>我体验了这两个库，最终决定在需要大量不可变状态大的型项目中使用 Immutable.js。想要了解这一部分的更多内容，请移步 。</p>
<h3 id="toc-197">副作用（Side Effects）</h3>
<p>副作用是指除了函数返回值以外，任何在函数调用之外观察到的应用程序状态改变。副作用包括：</p>
<ul>
<li>改变了任何外部变量或对象属性（例如，全局变量，或者一个在父级函数作用域链上的变量）</li>
<li>写日志</li>
<li>在屏幕输出</li>
<li>写文件</li>
<li>发网络请求</li>
<li>触发任何外部进程</li>
<li>调用另一个有副作用的函数</li>
</ul>
<p>在函数式编程中，副作用被尽可能避免，这使得程序的作用更容易理解，也使得程序更容易被测试。</p>
<p>Haskell 以及其他函数式编程语言经常从纯函数中隔离和封装副作用，使用  技巧。Mondas 这个话题要深入下去可以写一本书，所以我们先放一放。</p>
<p>你现在需要做的是要从你的软件中隔离副作用行为。如果你让副作用与你的程序逻辑分离，你的软件将会变得更易于扩展、重构、调试、测试和维护。</p>
<p>这也是为什么大部分前端框架鼓励我们分开管理状态和组件渲染，采用松耦合的模型。</p>
<h3 id="toc-aff">通过高阶函数提升可重用性</h3>
<p>函数式编程倾向于复用一组通用的函数功能来处理数据。面向对象编程倾向于把方法和数据集中到对象上。那些被集中的方法只能用来操作设计好的数据类型，通常是那些包含在特定对象实例上的数据。</p>
<p>在函数式编程里，对任何类型的数据一视同仁。同样的 <code>map()</code> 操作可以 map 对象、字符串、数字或任何别的类型，因为它接受一个函数参数，来适当地操作给定类型。函数式编程通过使用<strong>高阶函数</strong>来实现这一技巧。</p>
<p>在 JavaScript 里，<strong>函数是一等公民</strong>，JavaScript 允许使用者将函数作为数据 —— 可以将它们赋值给变量、作为参数传递给其他函数、将它们作为返回值返回，等等……</p>
<p><strong>高阶函数</strong>指的是一个函数以函数为参数，或以函数为返回值，或者既以函数为参数又以函数为返回值。高阶函数经常用于：</p>
<ul>
<li>抽象或隔离行为、作用，异步控制流程作为回调函数，promises，monads，等等……</li>
<li>创建可以泛用于各种数据类型的功能</li>
<li>部分应用于函数参数（偏函数应用）或创建一个柯里化的函数，用于复用或函数复合。</li>
<li>接受一个函数列表并返回一些由这个列表中的函数组成的复合函数。</li>
</ul>
<h4 id="toc-ee2">容器、函子（Functor）、列表和流</h4>
<p>Functor 是可以被用来执行具体 map 操作的数据。换句话说，它是一个有接口的容器，能够遍历其中的值。当你看到“functor”这个词，你在脑海里应该想到“mappable”。</p>
<p>之前我们说同样的 <code>map()</code> 函数能够操作各种数据类型。它是通过将 map 操作抽象出来，提供给 functor API 使用。<code>map()</code> 利用该接口执行重要的流程控制操作。在 <code>Array.prototype.map()</code> 的场景里，容器是一个数组，但是其他数据接口也可以作为 functor，同样它也提供了 mapping 操作的 API。</p>
<p>让我们看一下 <code>Array.prototype.map()</code> 是如何让你从 mapping 功能里抽象数据类型，让 <code>map()</code> 可以适用于任何数据类型的。我们创建一个简单的 <code>double()</code> mapping，它简单地将传给它的值乘以 2：</p>
<pre><code class="hljs lang-cpp"><span class="hljs-keyword">const</span> <span class="hljs-keyword">double</span> = n =&gt; n * <span class="hljs-number">2</span>;
<span class="hljs-keyword">const</span> doubleMap = numbers =&gt; numbers.<span class="hljs-built_in">map</span>(<span class="hljs-keyword">double</span>);
console.<span class="hljs-built_in">log</span>(doubleMap([<span class="hljs-number">2</span>, <span class="hljs-number">3</span>, <span class="hljs-number">4</span>])); <span class="hljs-comment">// [ 4, 6, 8 ]</span>
</code></pre><p>假设我们相对游戏中的目标执行奖励翻倍操作，我们所需要做的只是小小改变一下我们传给 <code>map()</code> 的 <code>double()</code> 函数，这样便一切正常：</p>
<pre><code class="hljs lang-qml"><span class="hljs-keyword">const</span> <span class="hljs-built_in">double</span> = n =&gt; n.points * <span class="hljs-number">2</span>;

<span class="hljs-keyword">const</span> doubleMap = numbers =&gt; numbers.map(<span class="hljs-built_in">double</span>);

<span class="hljs-built_in">console</span>.log(doubleMap([
  { <span class="hljs-attribute">name</span>: <span class="hljs-string">"ball"</span>, <span class="hljs-attribute">points</span>: <span class="hljs-number">2</span> },
  { <span class="hljs-attribute">name</span>: <span class="hljs-string">"coin"</span>, <span class="hljs-attribute">points</span>: <span class="hljs-number">3</span> },
  { <span class="hljs-attribute">name</span>: <span class="hljs-string">"candy"</span>, <span class="hljs-attribute">points</span>: <span class="hljs-number">4</span>}
])); <span class="hljs-comment">// [ 4, 6, 8 ]</span>
</code></pre><p>使用 functors 以及使用高阶函数抽象来创建通用功能函数，以处理任意数值或不同类型的数据，这是函数式编程中很重要的概念。你还能看到类似的概念以被应用。</p>
<blockquote>
<p>“流即是随着时间推移而变化的列表。”</p>
</blockquote>
<p>现在你所需要知道的是容器和容器的值所能应用的形式不仅仅只有数组和 functor。一个数组只是一些内容的列表。如果这个列表随着时间推移而变化则成为一个流 —— 所以你可以应用同样的功能来处理时间流 —— 如果你用函数式编程实际开始构建一个真正的软件时，你就会看到很多这种用法。</p>
<h3 id="toc-d48">对比声明式与命令式</h3>
<p>函数式编程是一个声明式范式，意思是说程序逻辑不需要通过明确描述控制流程来表达。</p>
<p><strong>命令式</strong> 程序花费大量代码来描述用来达成期望结果的特定步骤 —— <strong>控制流</strong>：即如何做。</p>
<p><strong>声明式</strong> 程序抽象了控制流过程，花费大量代码描述的是<strong>数据流</strong>：即做什么。</p>
<p>举个例子，下面是一个用 <strong>命令式</strong> 方式实现的 mapping 过程，接收一个数值数组，并返回一个新的数组，新数组将原数组的每个值乘以 2：</p>
<pre><code class="hljs lang-hsp">const doubleMap = numbers =&gt; {
  const doubled = []<span class="hljs-comment">;</span>
  <span class="hljs-keyword">for</span> (let i = <span class="hljs-number">0</span><span class="hljs-comment">; i &lt; numbers.length; i++) {</span>
    doubled.push(numbers[i] * <span class="hljs-number">2</span>)<span class="hljs-comment">;</span>
  }
  <span class="hljs-keyword">return</span> doubled<span class="hljs-comment">;</span>
}<span class="hljs-comment">;</span>

console.log(doubleMap([<span class="hljs-number">2</span>, <span class="hljs-number">3</span>, <span class="hljs-number">4</span>]))<span class="hljs-comment">; // [4, 6, 8]</span>
</code></pre><p>而实现同样功能的 <strong>声明式</strong> mapping 用函数 <code>Array.prototype.map()</code> 将控制流抽象了，从而我们可以表达更清晰的数据流：</p>
<pre><code class="hljs lang-stata"><span class="hljs-keyword">const</span> doubleMap = numbers =&gt; numbers.map(<span class="hljs-keyword">n</span> =&gt; <span class="hljs-keyword">n</span> * 2);

console.<span class="hljs-built_in">log</span>(doubleMap([2, 3, 4])); <span class="hljs-comment">// [4, 6, 8]</span>
</code></pre><p><strong>命令式</strong> 代码中频繁使用语句。<strong>语句</strong>是指一小段代码，它用来完成某个行为。通用的语句例子包括 <code>for</code>、<code>if</code>、<code>switch</code>、<code>throw</code>，等等……</p>
<p><strong>声明式</strong> 代码更多依赖表达式。<strong>表达式</strong>是指一小段代码，它用来计算某个值。表达式通常是某些函数调用的复合、一些值和操作符，用来计算出结果值。</p>
<p>以下都是表达式：</p>
<pre><code class="hljs lang-css">2 * 2
<span class="hljs-selector-tag">doubleMap</span>(<span class="hljs-selector-attr">[2, 3, 4]</span>)
<span class="hljs-selector-tag">Math</span><span class="hljs-selector-class">.max</span>(4, 3, 2)
</code></pre><p>通常在代码里，你会看到一个表达式被赋给某个变量，或者作为函数返回值，或者作为参数传给一个函数。在被赋值、返回或传递之前，表达式首先被计算，之后它的结果值被使用。</p>
<h3 id="toc-54b">结论</h3>
<p>函数式编程偏好：</p>
<ul>
<li>使用纯函数而不是使用共享状态和副作用</li>
<li>让可变数据成为不可变的</li>
<li>用函数复合替代命令控制流</li>
<li>使用高阶函数来操作许多数据类型，创建通用、可复用功能取代只是操作集中的数据的方法。</li>
<li>使用声明式而不是命令式代码（关注做什么，而不是如何做）</li>
<li>使用表达式替代语句</li>
<li>使用容器与高阶函数替代多态</li>
</ul>
<h3 id="toc-116">作业</h3>
<p>学习和练习这一组核心的数据扩展</p>
<ul>
<li><code>.map()</code></li>
<li><code>.filter()</code></li>
<li><code>.reduce()</code></li>
</ul>
<p>使用 map 来转换如下数组的值为 item 名字：</p>
<pre><code class="hljs lang-hsp"><span class="hljs-comment">// vvv Don"t change vvv</span>
const items = [
  { name: <span class="hljs-string">"ball"</span>, points: <span class="hljs-number">2</span> },
  { name: <span class="hljs-string">"coin"</span>, points: <span class="hljs-number">3</span> },
  { name: <span class="hljs-string">"candy"</span>, points: <span class="hljs-number">4</span>}
]<span class="hljs-comment">;</span>
<span class="hljs-comment">// ^^^ Don"t change ^^^</span>

const result = items.map(
  <span class="hljs-comment">/* ==vvv Replace this code vvv== */</span>
  () =&gt; {}
  <span class="hljs-comment">/* ==^^^ Replace this code ^^^== */</span>
)<span class="hljs-comment">;</span>


<span class="hljs-comment">// vvv Don"t change vvv</span>
test(<span class="hljs-string">"Map"</span>, <span class="hljs-keyword">assert</span> =&gt; {
  const msg = <span class="hljs-string">"Should extract names from objects"</span><span class="hljs-comment">;</span>
  const expected = [
    <span class="hljs-string">"ball"</span>, <span class="hljs-string">"coin"</span>, <span class="hljs-string">"candy"</span>
  ]<span class="hljs-comment">;</span>

  <span class="hljs-keyword">assert</span>.same(result, expected, msg)<span class="hljs-comment">;</span>
  <span class="hljs-keyword">assert</span>.<span class="hljs-keyword">end</span>()<span class="hljs-comment">;</span>
})<span class="hljs-comment">;</span>
<span class="hljs-comment">// ^^^ Don"t change ^^^</span>
</code></pre><p>使用 filter 来选择出 points 大于等于 3 的元素：</p>
<pre><code class="hljs lang-qml"><span class="hljs-comment">// vvv Don"t change vvv</span>
<span class="hljs-keyword">const</span> items = [
  { <span class="hljs-attribute">name</span>: <span class="hljs-string">"ball"</span>, <span class="hljs-attribute">points</span>: <span class="hljs-number">2</span> },
  { <span class="hljs-attribute">name</span>: <span class="hljs-string">"coin"</span>, <span class="hljs-attribute">points</span>: <span class="hljs-number">3</span> },
  { <span class="hljs-attribute">name</span>: <span class="hljs-string">"candy"</span>, <span class="hljs-attribute">points</span>: <span class="hljs-number">4</span> }
];
<span class="hljs-comment">// ^^^ Don"t change ^^^</span>

<span class="hljs-keyword">const</span> result = items.filter(
  <span class="hljs-comment">/* ==vvv Replace this code vvv== */</span>
  () =&gt; {}
  <span class="hljs-comment">/* ==^^^ Replace this code ^^^== */</span>
);


<span class="hljs-comment">// vvv Don"t change vvv</span>
test(<span class="hljs-string">"Filter"</span>, assert =&gt; {
  <span class="hljs-keyword">const</span> msg = <span class="hljs-string">"Should select items where points &gt;= 3"</span>;
  <span class="hljs-keyword">const</span> expected = [
    { <span class="hljs-attribute">name</span>: <span class="hljs-string">"coin"</span>, <span class="hljs-attribute">points</span>: <span class="hljs-number">3</span> },
    { <span class="hljs-attribute">name</span>: <span class="hljs-string">"candy"</span>, <span class="hljs-attribute">points</span>: <span class="hljs-number">4</span> }
  ];

  assert.same(result, expected, msg);
  assert.end();
});
<span class="hljs-comment">// ^^^ Don"t change ^^^</span>
</code></pre><p>使用 reduce 来求出 points 的和:</p>
<pre><code class="hljs lang-hsp"><span class="hljs-comment">// vvv Don"t change vvv</span>
const items = [
  { name: <span class="hljs-string">"ball"</span>, points: <span class="hljs-number">2</span> },
  { name: <span class="hljs-string">"coin"</span>, points: <span class="hljs-number">3</span> },
  { name: <span class="hljs-string">"candy"</span>, points: <span class="hljs-number">4</span> }
]<span class="hljs-comment">;</span>
<span class="hljs-comment">// ^^^ Don"t change ^^^</span>

const result = items.reduce(
  <span class="hljs-comment">/* ==vvv Replace this code vvv== */</span>
  () =&gt; {}
  <span class="hljs-comment">/* ==^^^ Replace this code ^^^== */</span>
)<span class="hljs-comment">;</span>


<span class="hljs-comment">// vvv Don"t change vvv</span>
test(<span class="hljs-string">"Learn reduce"</span>, <span class="hljs-keyword">assert</span> =&gt; {
  const msg = <span class="hljs-string">"should sum all the points"</span><span class="hljs-comment">;</span>
  const expected = <span class="hljs-number">9</span><span class="hljs-comment">;</span>

  <span class="hljs-keyword">assert</span>.same(result, expected, msg)<span class="hljs-comment">;</span>
  <span class="hljs-keyword">assert</span>.<span class="hljs-keyword">end</span>()<span class="hljs-comment">;</span>
})<span class="hljs-comment">;</span>
<span class="hljs-comment">// ^^^ Don"t change ^^^</span>
</code></pre><h3 id="toc-adb">更进一步</h3>
<p>准备好更深入学习了吗？阅读 Jafar Husain 的  来学习一些最重要的函数式编程工具。</p>
<p>想要了解更详细的关于函数式编程的细节以及如何使用函数式编程结合实际每天使用的 JavaScript 来构建真正的应用程序？</p>
<p>。这么好的机会，别错过。</p>
<p><img src="https://p.ssl.qhimg.com/t0136c9315909f9cee2.jpg" alt=""></p>
<hr>
<p><strong><em>Eric Elliott</em></strong><em> is the author of </em><em>. He has contributed to software experiences for </em><strong><em>Adobe Systems</em></strong><em>, </em><strong><em>Zumba Fitness</em></strong><em>, </em><strong><em>The Wall Street Journal</em></strong><em>, </em><strong><em>ESPN</em></strong><em>, </em><strong><em>BBC</em></strong><em>, and top recording artists including </em><strong><em>Usher</em></strong><em>, </em><strong><em>Frank Ocean</em></strong><em>, </em><strong><em>Metallica</em></strong><em>, and many more.</em></p>
<p><em>He spends most of his time in the San Francisco Bay Area with the most beautiful woman in the world.</em></p>
<p>感谢 .</p>
<blockquote>
<p>英文原文：</p>
</blockquote>
---------------
<h1 id="#title_2" >3、【译】征服 JavaScript 面试：什么是闭包？</h1>

[https://www.h5jun.com/post/master-the-javascript-interview-what-is-a-closure.html](https://www.h5jun.com/post/master-the-javascript-interview-what-is-a-closure.html)
<div class="toc"><ul>
<li></li>
<li></li>
<li></li>
</ul>
</div><blockquote>
<p>原文：</p>
</blockquote>
<p><img src="https://p.ssl.qhimg.com/t0163946f0d2b9e13a6.jpg" alt=""></p>
<p>“征服 JavaScript 面试”是我写的一系列文章，来帮助面试者准备他们在面试 JavaScript 中、高级职位中将可能会遇到的一些问题。这些问题我自己在面试中也经常会问。</p>
<!--more-->
<p><img src="https://p1.ssl.qhimg.com/t015b8748cb620aaad5.png" alt=""></p>
<p>在我面试时问出的一系列问题里，闭包通常是我问的第一个或最后一个问题。坦白地说，如果你连闭包也弄不明白，你是不会在 JavaScript 的道路上走多远的。</p>
<p>你别东张西望，说的就是你。你真的理解如何构建一个严谨的 JavaScript 应用？你真的理解代码背后发生的事情或者说一个应用程序是如何工作的？我表示怀疑。如果连个闭包问题都搞不清的话，真是有点够呛。</p>
<p>你不仅仅应该了解闭包的机制，更应该了解闭包为什么很重要，以及能够很容易地回答出闭包的几种可能的应用场景。</p>
<p>闭包在 JavaScript 中常用来实现对象数据的私有，在事件处理和回调函数中也常常会用到它，此外还有，以及其他函数式编程模式。</p>
<p>我不在乎面试者是否知道“closure”这个单词或者它的专业定义。我只想弄清他们是否理解基本原理。如果他们没有，那么通常意味着这些面试者在构建实际 JavaScript 应用方面并没有很多经验。</p>
<blockquote>
<p>如果你不能回答这个问题，你只是个初级开发者。不管你实际上已经干这个多久了。</p>
</blockquote>
<p>为了快速理解下面的内容：你想一下能否举出两个闭包的通用场景？</p>
<h3 id="toc-08b">什么是闭包？</h3>
<p>简言之，<strong>闭包</strong>是由函数引用其周边状态（<strong>词法环境</strong>）绑在一起形成的（封装）组合结构。在 JavaScript 中，闭包在<strong>每个函数被创建时</strong>形成。</p>
<p>这是基本原理，但为什么我们关心这些？实际上，由于闭包与它的词法环境绑在一起，因此<strong>闭包让我们能够从一个函数内部访问其外部函数的作用域</strong>。</p>
<p>要使用闭包，只需要简单地将一个函数定义在另一个函数内部，并将它暴露出来。要暴露一个函数，可以将它返回或者传给其他函数。</p>
<p><strong>内部函数将能够访问到外部函数作用域中的变量</strong>，即使外部函数已经执行完毕。</p>
<h3 id="toc-9c7">闭包使用的例子</h3>
<p>闭包的用途之一是实现对象的私有数据。数据私有是让我们能够面向接口编程而不是面向实现编程的基础。而面向接口编程是一个重要的概念，有助于我们创建更加健壮的软件，因为实现细节比接口约定相对来说更加容易被改变。</p>
<blockquote>
<p>“面向接口编程，别面向实现编程。”
</p>
</blockquote>
<p>在 JavaScript 中，闭包是用来实现数据私有的原生机制。当你使用闭包来实现数据私有时，被封装的变量只能在闭包容器函数作用域中使用。你无法绕过对象<strong>被授权的方法</strong>在外部访问这些数据。在 JavaScript 中，任何定义在闭包作用域下的公开方法才可以访问这些数据。例如：</p>
<pre><code class="hljs lang-js"><span class="hljs-keyword">const</span> getSecret = (secret) =&gt; {
  <span class="hljs-keyword">return</span> {
    get: () =&gt; secret
  };
};

test(<span class="hljs-string">"Closure for object privacy."</span>, assert =&gt; {
  <span class="hljs-keyword">const</span> msg = <span class="hljs-string">".get() should have access to the closure."</span>;
  <span class="hljs-keyword">const</span> expected = <span class="hljs-number">1</span>;
  <span class="hljs-keyword">const</span> obj = getSecret(<span class="hljs-number">1</span>);

  <span class="hljs-keyword">const</span> actual = obj.get();

  <span class="hljs-keyword">try</span> {
    assert.ok(secret, <span class="hljs-string">"This throws an error."</span>);
  } <span class="hljs-keyword">catch</span> (e) {
    assert.ok(<span class="hljs-literal">true</span>, <span class="hljs-string">`The secret var is only available
      to privileged methods.`</span>);
  }

  assert.equal(actual, expected, msg);
  assert.end();
});
</code></pre>
<p>在上面的例子里，<code>get()</code> 方法定义在 <code>getSecret()</code> 作用域下，这让它可以访问任何 <code>getSecret()</code> 中的变量，于是它就是一个被授权的方法。在这个例子里，它可以访问参数 <code>secret</code>。</p>
<p>对象不是唯一的产生私有数据的方式。闭包还可以被用来创建<strong>有状态的函数</strong>，这些函数的执行过程可能由它们自身的内部状态所决定。例如：</p>
<pre><code class="hljs lang-coffeescript">const secret = <span class="hljs-function"><span class="hljs-params">(msg)</span> =&gt;</span> () =&gt; msg;
</code></pre><pre><code class="hljs lang-hsp"><span class="hljs-comment">// Secret - creates closures with secret messages.</span>
<span class="hljs-comment">// https://gist.github.com/ericelliott/f6a87bc41de31562d0f9</span>
<span class="hljs-comment">// https://jsbin.com/hitusu/edit?html,js,output</span>

<span class="hljs-comment">// secret(msg: String) =&gt; getSecret() =&gt; msg: String</span>
const secret = (msg) =&gt; () =&gt; msg<span class="hljs-comment">;</span>

test(<span class="hljs-string">"secret"</span>, <span class="hljs-keyword">assert</span> =&gt; {
  const msg = <span class="hljs-string">"secret() should return a function that returns the passed secret."</span><span class="hljs-comment">;</span>

  const theSecret = <span class="hljs-string">"Closures are easy."</span><span class="hljs-comment">;</span>
  const mySecret = secret(theSecret)<span class="hljs-comment">;</span>

  const actual = mySecret()<span class="hljs-comment">;</span>
  const expected = theSecret<span class="hljs-comment">;</span>

  <span class="hljs-keyword">assert</span>.equal(actual, expected, msg)<span class="hljs-comment">;</span>
  <span class="hljs-keyword">assert</span>.<span class="hljs-keyword">end</span>()<span class="hljs-comment">;</span>
})<span class="hljs-comment">;</span>
</code></pre><p>在函数式编程中，闭包经常用于偏函数应用和柯里化。为了说明这个，我们先定义一些概念：</p>
<p><strong>函数应用：</strong>一个过程，指将参数传给一个函数，并获得它的返回值。</p>
<p><strong>偏函数应用：</strong>一个过程，它传给某个函数其中一部分参数，然后返回一个新的函数，该函数等待接受后续参数。换句话说，偏函数应用是一个函数，它接受另一个函数为参数，这个作为参数的函数本身接受多个参数，它返回一个函数，这个函数与它的参数函数相比，接受更少的参数。偏函数应用<em>提前赋予</em>一部分参数，而返回的函数则等待调用时传入剩余的参数。</p>
<p>偏函数应用通过闭包作用域来提前赋予参数。你可以实现一个通用的函数来赋予指定的函数部分参数，它看起来如下：</p>
<pre><code class="hljs lang-stylus"><span class="hljs-function"><span class="hljs-title">partialApply</span><span class="hljs-params">(targetFunction: Function, ...fixedArgs: Any[])</span></span> =&gt;
  functionWithFewerParams(..<span class="hljs-selector-class">.remainingArgs</span>: Any[])
</code></pre><p>如果你要更进一步理解上面的形式，你可以看。</p>
<p><code>partialApply</code> 接受一个多参数的函数，以及一串我们想要提前赋给这个函数的参数，它返回一个新的函数，这个函数将接受剩余的参数。</p>
<p>下面给一个例子来说明，假设你有一个函数，求两个数的和：</p>
<pre><code class="hljs lang-armasm"><span class="hljs-symbol">const</span> <span class="hljs-keyword">add </span>= (a, <span class="hljs-keyword">b) </span>=&gt; a + <span class="hljs-keyword">b;
</span></code></pre><p>现在你想要得到一个函数，它能够对任何传给它的参数都加 10，我们可以将它命名为 <code>add10()</code>。<code>add10(5)</code> 的结果应该是 <code>15</code>。我们的 <code>partialApply()</code> 函数可以做到这个：</p>
<pre><code class="hljs lang-mipsasm">const <span class="hljs-keyword">add10 </span>= partialApply(<span class="hljs-keyword">add, </span><span class="hljs-number">10</span>)<span class="hljs-comment">;</span>
<span class="hljs-keyword">add10(5);
</span></code></pre><p>在这个例子里，参数 <code>10</code> 通过闭包作用域被提前赋予 <code>add()</code>，从而让我们获得 <code>add10()</code>。</p>
<p>现在让我们看一下如何实现 <code>partialApply()</code>：</p>
<pre><code class="hljs lang-js"><span class="hljs-comment">// Generic Partial Application Function</span>
<span class="hljs-comment">// https://jsbin.com/biyupu/edit?html,js,output</span>
<span class="hljs-comment">// https://gist.github.com/ericelliott/f0a8fd662111ea2f569e</span>

<span class="hljs-comment">// partialApply(targetFunction: Function, ...fixedArgs: Any[]) =&gt;</span>
<span class="hljs-comment">//   functionWithFewerParams(...remainingArgs: Any[])</span>
<span class="hljs-keyword">const</span> partialApply = (fn, ...fixedArgs) =&gt; {
  <span class="hljs-keyword">return</span> <span class="hljs-function"><span class="hljs-keyword">function</span> (<span class="hljs-params">...remainingArgs</span>) </span>{
    <span class="hljs-keyword">return</span> fn.apply(<span class="hljs-keyword">this</span>, fixedArgs.concat(remainingArgs));
  };
};


test(<span class="hljs-string">"add10"</span>, assert =&gt; {
  <span class="hljs-keyword">const</span> msg = <span class="hljs-string">"partialApply() should partially apply functions"</span>

  <span class="hljs-keyword">const</span> add = (a, b) =&gt; a + b;

  <span class="hljs-keyword">const</span> add10 = partialApply(add, <span class="hljs-number">10</span>);


  <span class="hljs-keyword">const</span> actual = add10(<span class="hljs-number">5</span>);
  <span class="hljs-keyword">const</span> expected = <span class="hljs-number">15</span>;

  assert.equal(actual, expected, msg);
});
</code></pre>
<p>如你所见，它只是简单地返回一个函数，这个函数通过闭包访问了传给 <code>partialApply()</code> 函数的 <code>fixedArgs</code> 参数。</p>
<h3 id="toc-a3a">轮到你来试试了</h3>
<p>你用闭包来做什么？如果你有最喜欢的应用场景，举一些例子，在评论中告诉我。</p>
<blockquote>
<p>英文原文：</p>
</blockquote>
---------------
<h1 id="#title_3" >4、Webpack 2最终版本发布，聚焦文档内容提升</h1>
David Iffland
[http://www.infoq.com/cn/news/2017/01/webpack-2-final-documentation?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/01/webpack-2-final-documentation?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/news/2017/01/webpack-2-final-documentation/zh/headerimage/GettyImages-494562157.jpg"/><p>流行的JavaScript模块和资源打包工具webpack 2最终版本已经发布，该版本可以实现对ES2015的本地支持，并大大改善了文档内容。但是，新版本是否能显著改进构建时间和文件大小还有待观察。</p> <i>By David Iffland</i> <i> Translated by 刘嘉洋</i>
---------------
<h1 id="#title_4" >5、视频演讲： 链家网高可用架构演进</h1>
董金勇
[http://www.infoq.com/cn/presentations/evolution-of-lianjia-high-available-architect?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/evolution-of-lianjia-high-available-architect?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/evolution-of-lianjia-high-available-architect/zh/mediumimage/dongjingyong270.jpg"/><p>链家业务突飞猛进，日PV增至数亿，系统可用性逐渐成为业务发展的瓶颈。在强大的业务压力下，解决原系统高可用性问题，打造万亿级房产O2O平台，具有很大挑战。短短两年多时间，甩掉历史包袱，快速脱胎换骨，替代昂贵且低效的方案，形成自己完善的技术体系，链家走出了一条独特的架构演进之路。分享会重点介绍链家网原架构的痛点和解决方案，从会话层架构设计与防护、服务层治理、数据层可用性、基础设施建设等角度分析高可用性，分享从规划到实践，从防范到发现，从发现到处理等一系列高可用措施，分享高可用架构演进过程的心得，以期为高速成长企业的技术架构设计提供借鉴。</p> <i>By 董金勇</i>
---------------
<h1 id="#title_5" >6、文章： 组合使用Laravel和vfsStream测试文件上传</h1>
Terry Rowland
[http://www.infoq.com/cn/articles/vfsstream-file-uploads-laravel?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/vfsstream-file-uploads-laravel?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/vfsstream-file-uploads-laravel/zh/smallimage/logo.jpg"/><p>文件上传的测试可能会非常棘手，但是通过使用恰当的工具，再掌握一些技巧，这个过程可以会更加高效，也能更容易。本文将会创建一个端点来上传包含用户信息的CSV文件，并测试CSV文件中的用户能够展现到一个JSON格式的响应中，同时还会添加校验功能，确保所处理的文件是CSV类型。
</p> <i>By Terry Rowland</i> <i> Translated by 张卫滨</i>
---------------
<h1 id="#title_6" >7、营销部门投资AI前应思考的3个问题</h1>
AMAN NAIMAT
[http://www.infoq.com/cn/news/2017/01/3-marketers-investing-AI?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/01/3-marketers-investing-AI?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>当下热门的人工智能（AI）技术如何在营销领域应用和部署，本文作者提出了3个问题，帮助营销主管们思考并决策：营销预算主要浪费在哪些部分，哪些部分真正带来经济顺差，以及营销部门拥有什么样的独特数据。</p> <i>By AMAN NAIMAT</i> <i> Translated by 杨振涛</i>
---------------
<h1 id="#title_7" >8、看法：2017会带给我们的文化和方法</h1>
Shane Hastie
[http://www.infoq.com/cn/news/2017/01/2017--culture-methods?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/01/2017--culture-methods?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/news/2017/01/2017--culture-methods/zh/headerimage/GettyImages-516755802.jpg"/><p>我们对InfoQ文化与方法编辑团队进行了调查，以获得他们对于2017年技术行业可能发生的事情、将会发生的趋势以及对全球企业的启示的看法。</p> <i>By Shane Hastie</i> <i> Translated by 王纯超</i>
---------------
<h1 id="#title_8" >9、如何写出好的 JavaScript —— 浅谈 API 设计</h1>

[https://www.h5jun.com/post/how-to-write-better-js-code.html](https://www.h5jun.com/post/how-to-write-better-js-code.html)
<div class="toc"><ul>
<li></li>
<li></li>
<li></li>
<li></li>
<li></li>
<li></li>
<li></li>
</ul>
</div><p>这是  的节选。很多同学觉得写 JavaScript 很简单，只要能写出功能来，效果能实现就好。还有一些培训机构，专门教人写各种“炫酷特效”，以此让许多人觉得这些培训很“牛逼”。然而事实上，能写 JavaScript 和写好 JavaScript 这中间还有很遥远的距离。成为专业前端，注定在 JavaScript 路途上需要一步步扎实的修炼，没有捷径。</p>
<p><img src="https://p3.ssl.qhimg.com/t0111abe7db051d82e7.jpg" alt=""></p>
<!--more-->
<p>看一个简单的例子：</p>
<iframe src="https://code.h5jun.com/say/4" height="200px" frameborder="no"></iframe>

<p>实现一个类似于“交通灯”的效果，让三个不同颜色的圆点每隔 2 秒循环切换。</p>
<p>对应的 HTML 和 CSS 如下：</p>
<pre><code class="hljs lang-html"><span class="hljs-tag">&lt;<span class="hljs-name">ul</span> <span class="hljs-attr">id</span>=<span class="hljs-string">"traffic"</span> <span class="hljs-attr">class</span>=<span class="hljs-string">"wait"</span>&gt;</span>
  <span class="hljs-tag">&lt;<span class="hljs-name">li</span>&gt;</span><span class="hljs-tag">&lt;<span class="hljs-name">span</span>&gt;</span><span class="hljs-tag">&lt;/<span class="hljs-name">span</span>&gt;</span><span class="hljs-tag">&lt;/<span class="hljs-name">li</span>&gt;</span>
  <span class="hljs-tag">&lt;<span class="hljs-name">li</span>&gt;</span><span class="hljs-tag">&lt;<span class="hljs-name">span</span>&gt;</span><span class="hljs-tag">&lt;/<span class="hljs-name">span</span>&gt;</span><span class="hljs-tag">&lt;/<span class="hljs-name">li</span>&gt;</span>
  <span class="hljs-tag">&lt;<span class="hljs-name">li</span>&gt;</span><span class="hljs-tag">&lt;<span class="hljs-name">span</span>&gt;</span><span class="hljs-tag">&lt;/<span class="hljs-name">span</span>&gt;</span><span class="hljs-tag">&lt;/<span class="hljs-name">li</span>&gt;</span>
<span class="hljs-tag">&lt;/<span class="hljs-name">ul</span>&gt;</span>
</code></pre>
<pre><code class="hljs lang-css"><span class="hljs-selector-id">#traffic</span> &gt; <span class="hljs-selector-tag">li</span>{
  <span class="hljs-attribute">display</span>: block;
}

<span class="hljs-selector-id">#traffic</span> <span class="hljs-selector-tag">span</span>{
  <span class="hljs-attribute">display</span>: inline-block;
  <span class="hljs-attribute">width</span>: <span class="hljs-number">50px</span>;
  <span class="hljs-attribute">height</span>: <span class="hljs-number">50px</span>;
  <span class="hljs-attribute">background-color</span>: gray;
  <span class="hljs-attribute">margin</span>: <span class="hljs-number">5px</span>;
  <span class="hljs-attribute">border-radius</span>: <span class="hljs-number">50%</span>;
}

<span class="hljs-selector-id">#traffic</span><span class="hljs-selector-class">.stop</span> <span class="hljs-selector-tag">li</span><span class="hljs-selector-pseudo">:nth-child(1)</span> <span class="hljs-selector-tag">span</span>{
  <span class="hljs-attribute">background-color</span>: <span class="hljs-number">#a00</span>;
}

<span class="hljs-selector-id">#traffic</span><span class="hljs-selector-class">.wait</span> <span class="hljs-selector-tag">li</span><span class="hljs-selector-pseudo">:nth-child(2)</span> <span class="hljs-selector-tag">span</span>{
  <span class="hljs-attribute">background-color</span>: <span class="hljs-number">#aa0</span>;
}

<span class="hljs-selector-id">#traffic</span><span class="hljs-selector-class">.pass</span> <span class="hljs-selector-tag">li</span><span class="hljs-selector-pseudo">:nth-child(3)</span> <span class="hljs-selector-tag">span</span>{
  <span class="hljs-attribute">background-color</span>: <span class="hljs-number">#0a0</span>;
}
</code></pre>
<p>那么这一功能的 JavaScript 该如何实现呢？</p>
<h2 id="toc-aaa"></h2>
<p>有的同学说，这个实现还不简单嘛？直接用几个定时器一下切换不就好了：</p>
<pre><code class="hljs lang-js"><span class="hljs-keyword">const</span> traffic = <span class="hljs-built_in">document</span>.getElementById(<span class="hljs-string">"traffic"</span>);

(<span class="hljs-function"><span class="hljs-keyword">function</span> <span class="hljs-title">reset</span>(<span class="hljs-params"></span>)</span>{
  traffic.className = <span class="hljs-string">"wait"</span>;

  setTimeout(<span class="hljs-function"><span class="hljs-keyword">function</span>(<span class="hljs-params"></span>)</span>{
      traffic.className = <span class="hljs-string">"stop"</span>;
      setTimeout(<span class="hljs-function"><span class="hljs-keyword">function</span>(<span class="hljs-params"></span>)</span>{
        traffic.className = <span class="hljs-string">"pass"</span>;
        setTimeout(reset, <span class="hljs-number">2000</span>)
      }, <span class="hljs-number">2000</span>)
  }, <span class="hljs-number">2000</span>);
})();
</code></pre>
<p>没错，就这个功能本身，这样实现就 OK 了。但是这样实现有什么问题呢？</p>
<p>首先是<strong>过程耦合</strong>，状态切换是wait-&gt;stop-&gt;pass 循环，在上面的设计里，实际上操作顺序是耦合在一起的，要先 &#39;wait&#39;，然后等待 2000 毫秒再 &#39;stop&#39;，然后再等待 2000 毫秒在 &#39;pass&#39;，这中间的顺序一旦有调整，需求有变化，代码都需要修改。</p>
<p>其次，这样的异步嵌套是会产生 <strong>callback hell</strong> 的，如果需求不是三盏灯，而是五盏灯、十盏灯，代码的嵌套结构就很深，看起来就很难看了。</p>
<p>所以我们说，版本一方法虽然直接，但因为抽象程度很低（几乎没有提供任何抽象 API），它的扩展性很不好，因为异步问题没处理，代码结构也很不好。如果只能写这样的代码，是不能说就写好了 JavaScript 的。</p>
<h2 id="toc-82b"></h2>
<p>要解决版本一的<strong>过程耦合</strong>问题，最简单的思路是将状态<code>[&#39;wait&#39;,&#39;stop&#39;,&#39;pass&#39;]</code>抽象出来：</p>
<pre><code class="hljs lang-js"><span class="hljs-keyword">const</span> traffic = <span class="hljs-built_in">document</span>.getElementById(<span class="hljs-string">"traffic"</span>);

<span class="hljs-keyword">var</span> stateList = [<span class="hljs-string">"wait"</span>, <span class="hljs-string">"stop"</span>, <span class="hljs-string">"pass"</span>];

<span class="hljs-keyword">var</span> currentStateIndex = <span class="hljs-number">0</span>;

setInterval(<span class="hljs-function"><span class="hljs-keyword">function</span>(<span class="hljs-params"></span>)</span>{
  <span class="hljs-keyword">var</span> state = stateList[currentStateIndex];
  traffic.className = state;
  currentStateIndex = (currentStateIndex + <span class="hljs-number">1</span>) % stateList.length;
}, <span class="hljs-number">2000</span>);
</code></pre>
<p>这是一种数据抽象的思路，应用它我们得到了上面的这个版本。</p>
<p>这一版本比前一版本要好很多，但是它也有问题，最大的问题就是<strong>封装性很差</strong>，它把 stateList 和 currentStateIndex 都暴露出来了，而且以全局变量的形式，这么做很不好，需要优化。</p>
<h2 id="toc-d7c"></h2>
<pre><code class="hljs lang-js"><span class="hljs-keyword">const</span> traffic = <span class="hljs-built_in">document</span>.getElementById(<span class="hljs-string">"traffic"</span>);

<span class="hljs-function"><span class="hljs-keyword">function</span> <span class="hljs-title">start</span>(<span class="hljs-params">traffic, stateList</span>)</span>{
  <span class="hljs-keyword">var</span> currentStateIndex = <span class="hljs-number">0</span>;

  setInterval(<span class="hljs-function"><span class="hljs-keyword">function</span>(<span class="hljs-params"></span>)</span>{
    <span class="hljs-keyword">var</span> state = stateList[currentStateIndex];
    traffic.className = state;
    currentStateIndex = (currentStateIndex + <span class="hljs-number">1</span>) % stateList.length;
  }, <span class="hljs-number">2000</span>);
}

start(traffic, [<span class="hljs-string">"wait"</span>, <span class="hljs-string">"stop"</span>, <span class="hljs-string">"pass"</span>]);
</code></pre>
<p>版本三是中规中矩的一版，也是一般我们在工作中比较常用的思路。应该将暴露出来的 API 暴露出来（本例中的 stateList）。将不应该暴露出来的数据或状态隐藏（本例中的 currentStateIndex）。</p>
<p>有许多同学觉得说写出这一版本来已经很不错的。的确，应该也还不错，但这一版的抽象程度其实也不是很高，或者说，如果考虑适用性，这版已经很好了，但是如果考虑可复用性的话，这版依然有改进空间。</p>
<p>我们再看一个思路上较有意思的版本。</p>
<h2 id="toc-50e"></h2>
<pre><code class="hljs lang-js"><span class="hljs-keyword">const</span> traffic = <span class="hljs-built_in">document</span>.getElementById(<span class="hljs-string">"traffic"</span>);

<span class="hljs-function"><span class="hljs-keyword">function</span> <span class="hljs-title">poll</span>(<span class="hljs-params">...fnList</span>)</span>{
  <span class="hljs-keyword">let</span> stateIndex = <span class="hljs-number">0</span>;

  <span class="hljs-keyword">return</span> <span class="hljs-function"><span class="hljs-keyword">function</span>(<span class="hljs-params">...args</span>)</span>{
    <span class="hljs-keyword">let</span> fn = fnList[stateIndex++ % fnList.length];
    <span class="hljs-keyword">return</span> fn.apply(<span class="hljs-keyword">this</span>, args);
  }
}

<span class="hljs-function"><span class="hljs-keyword">function</span> <span class="hljs-title">setState</span>(<span class="hljs-params">state</span>)</span>{
  traffic.className = state;
}

<span class="hljs-keyword">let</span> trafficStatePoll = poll(setState.bind(<span class="hljs-literal">null</span>, <span class="hljs-string">"wait"</span>),
                            setState.bind(<span class="hljs-literal">null</span>, <span class="hljs-string">"stop"</span>),
                            setState.bind(<span class="hljs-literal">null</span>, <span class="hljs-string">"pass"</span>));

setInterval(trafficStatePoll, <span class="hljs-number">2000</span>);
</code></pre>
<p>这一版用的是<strong>过程抽象</strong>的思路，而过程抽象，是<strong>函数式编程</strong>的基础。在这里，我们抽象出了一个 <code>poll(...fnList)</code> 的高阶组合函数，它将一个函数列表组合起来，每次调用时依次轮流执行列表里的函数。</p>
<p>我们说，程序设计的本质是抽象，而<strong>过程抽象</strong>是一种与<strong>数据抽象</strong>对应的思路，它们是两种不同的抽象模型。数据抽象比较基础，而过程抽象相对高级一些，也更灵活一些。数据抽象是研究函数如何操作数据，而过程抽象则在此基础上研究函数如何操作函数。所以说如果把抽象比作数学，那么数据抽象是初等数学，过程抽象则是高等数学。同一个问题，既可以用初等数学来解决，又可以用高等数学来解决。用什么方法解决，取决于问题的模型和难度等等。</p>
<hr>
<p>好了，上面我们有了四个版本，那么是否考虑了这些版本就足够了呢？</p>
<p>并不是。因为需求是会变更的。假设现在需求变化了：</p>
<p><em>需求变更：让 wait、stop、pass 状态的持续时长不相等，分别改成 1秒、2秒、3秒。</em></p>
<p><img src="https://p1.ssl.qhimg.com/t018c41be76ca3460a2.jpg" alt=""></p>
<p>那么，我们发现 ——</p>
<p>除了版本一之外，版本二、三、四全都跪了……</p>
<p><img src="https://p1.ssl.qhimg.com/t01b151b19a590ffa89.jpg" alt=""></p>
<p>那是否意味着我们要<strong>回归到版本一</strong>呢？</p>
<p>当然并不是。</p>
<hr>
<h2 id="toc-410"></h2>
<pre><code class="hljs lang-js"><span class="hljs-keyword">const</span> traffic = <span class="hljs-built_in">document</span>.getElementById(<span class="hljs-string">"traffic"</span>);

<span class="hljs-function"><span class="hljs-keyword">function</span> <span class="hljs-title">wait</span>(<span class="hljs-params">time</span>)</span>{
  <span class="hljs-keyword">return</span> <span class="hljs-keyword">new</span> <span class="hljs-built_in">Promise</span>(resolve =&gt; setTimeout(resolve, time));
}

<span class="hljs-function"><span class="hljs-keyword">function</span> <span class="hljs-title">setState</span>(<span class="hljs-params">state</span>)</span>{
  traffic.className = state;
}

<span class="hljs-function"><span class="hljs-keyword">function</span> <span class="hljs-title">reset</span>(<span class="hljs-params"></span>)</span>{
  <span class="hljs-built_in">Promise</span>.resolve()
    .then(setState.bind(<span class="hljs-literal">null</span>, <span class="hljs-string">"wait"</span>))
    .then(wait.bind(<span class="hljs-literal">null</span>, <span class="hljs-number">1000</span>))
    .then(setState.bind(<span class="hljs-literal">null</span>, <span class="hljs-string">"stop"</span>))
    .then(wait.bind(<span class="hljs-literal">null</span>, <span class="hljs-number">2000</span>))
    .then(setState.bind(<span class="hljs-literal">null</span>, <span class="hljs-string">"pass"</span>))
    .then(wait.bind(<span class="hljs-literal">null</span>, <span class="hljs-number">3000</span>))
    .then(reset);
}

reset();
</code></pre>
<p>版本五的思路是，<strong>既然我们需要考虑不同的持续时间，那么我们需要将等待时间抽象出来</strong>：</p>
<pre><code class="hljs lang-js"><span class="hljs-function"><span class="hljs-keyword">function</span> <span class="hljs-title">wait</span>(<span class="hljs-params">time</span>)</span>{
  <span class="hljs-keyword">return</span> <span class="hljs-keyword">new</span> <span class="hljs-built_in">Promise</span>(resolve =&gt; setTimeout(resolve, time));
}
</code></pre>
<p>这一版本里我们用了  来处理回调问题，当然对 ES6 之前的版本，可以用 shim 或 polyfill、第三方库，也可以选择不用 Promise。</p>
<p>版本五抽象出的 wait 方法也还比较通用，可以用在其他地方。这是版本五好的一点。</p>
<h2 id="toc-8ff"></h2>
<p>我们还可以进一步抽象，设计出版本六，或者类似的<strong>对象模型</strong>：</p>
<pre><code class="hljs lang-js"><span class="hljs-keyword">const</span> trafficEl = <span class="hljs-built_in">document</span>.getElementById(<span class="hljs-string">"traffic"</span>);

<span class="hljs-function"><span class="hljs-keyword">function</span> <span class="hljs-title">TrafficProtocol</span>(<span class="hljs-params">el, reset</span>)</span>{
  <span class="hljs-keyword">this</span>.subject = el;
  <span class="hljs-keyword">this</span>.autoReset = reset;
  <span class="hljs-keyword">this</span>.stateList = [];
}

TrafficProtocol.prototype.putState = <span class="hljs-function"><span class="hljs-keyword">function</span>(<span class="hljs-params">fn</span>)</span>{
  <span class="hljs-keyword">this</span>.stateList.push(fn);
}

TrafficProtocol.prototype.reset = <span class="hljs-function"><span class="hljs-keyword">function</span>(<span class="hljs-params"></span>)</span>{
  <span class="hljs-keyword">let</span> subject = <span class="hljs-keyword">this</span>.subject;

  <span class="hljs-keyword">this</span>.statePromise = <span class="hljs-built_in">Promise</span>.resolve();
  <span class="hljs-keyword">this</span>.stateList.forEach((stateFn) =&gt; {
    <span class="hljs-keyword">this</span>.statePromise = <span class="hljs-keyword">this</span>.statePromise.then(()=&gt;{
      <span class="hljs-keyword">return</span> <span class="hljs-keyword">new</span> <span class="hljs-built_in">Promise</span>(resolve =&gt; {
        stateFn(subject, resolve);
      });
    });
  });
  <span class="hljs-keyword">if</span>(<span class="hljs-keyword">this</span>.autoReset){
    <span class="hljs-keyword">this</span>.statePromise.then(<span class="hljs-keyword">this</span>.reset.bind(<span class="hljs-keyword">this</span>));
  }
}

TrafficProtocol.prototype.start = <span class="hljs-function"><span class="hljs-keyword">function</span>(<span class="hljs-params"></span>)</span>{
  <span class="hljs-keyword">this</span>.reset();
}

<span class="hljs-keyword">var</span> traffic = <span class="hljs-keyword">new</span> TrafficProtocol(trafficEl, <span class="hljs-literal">true</span>);

traffic.putState(<span class="hljs-function"><span class="hljs-keyword">function</span>(<span class="hljs-params">subject, next</span>)</span>{
  subject.className = <span class="hljs-string">"wait"</span>;
  setTimeout(next, <span class="hljs-number">1000</span>);
});

traffic.putState(<span class="hljs-function"><span class="hljs-keyword">function</span>(<span class="hljs-params">subject, next</span>)</span>{
  subject.className = <span class="hljs-string">"stop"</span>;
  setTimeout(next, <span class="hljs-number">2000</span>);
});

traffic.putState(<span class="hljs-function"><span class="hljs-keyword">function</span>(<span class="hljs-params">subject, next</span>)</span>{
  subject.className = <span class="hljs-string">"pass"</span>;
  setTimeout(next, <span class="hljs-number">3000</span>);
});

traffic.start();
</code></pre>
<p>这一版本里，我们设计了一个 TrafficProtocol 类，它有 putState、reset、start 三个方法：</p>
<ul>
<li><p>putState 接受一个函数作为参数，这个函数自身有两个参数，一个是 subject，是由 TrafficProtocol 对象初始化时设定的 DOM 元素，一个是 next，是一个函数，表示结束当前 state，进入下一个 state。</p>
</li>
<li><p>reset 结束当前状态循环，开始新的循环。</p>
</li>
<li><p>start 开始执行循环，这里的实现是直接调用 reset。</p>
</li>
</ul>
<p>看一下 reset 的实现思路：</p>
<pre><code class="hljs lang-js">TrafficProtocol.prototype.reset = <span class="hljs-function"><span class="hljs-keyword">function</span>(<span class="hljs-params"></span>)</span>{
  <span class="hljs-keyword">let</span> subject = <span class="hljs-keyword">this</span>.subject;

  <span class="hljs-keyword">this</span>.statePromise = <span class="hljs-built_in">Promise</span>.resolve();
  <span class="hljs-keyword">this</span>.stateList.forEach((stateFn) =&gt; {
    <span class="hljs-keyword">this</span>.statePromise = <span class="hljs-keyword">this</span>.statePromise.then(()=&gt;{
      <span class="hljs-keyword">return</span> <span class="hljs-keyword">new</span> <span class="hljs-built_in">Promise</span>(resolve =&gt; {
        stateFn(subject, resolve);
      });
    });
  });
  <span class="hljs-keyword">if</span>(<span class="hljs-keyword">this</span>.autoReset){
    <span class="hljs-keyword">this</span>.statePromise.then(<span class="hljs-keyword">this</span>.reset.bind(<span class="hljs-keyword">this</span>));
  }
}
</code></pre>
<p>在这里我们创建一个 statePromise，然后将 stateList 中的方法（通过 putState 添加的）依次绑定到 promise 上。如果设置了 autoReset，那么我们在 promise 的最后绑定 reset 自身，这样就实现了循环切换。</p>
<p>有了这个模型，我们要添加新的状态，只需要通过 putState 添加一个新的状态就好了。这一模型不仅仅可以用在这个需求里，还可以用在任何需要顺序执行异步请求的地方。</p>
<p>最后，我们看到，版本六用到了面向对象、过程抽象、Promise等模式，它的优点是 API 设计灵活，通用性和扩展性好。但是版本六也有缺点，它的实现复杂度比前面的几个版本都高，我们在做这样的设计时，也需要考虑是否有<strong>过度设计</strong>的嫌疑。</p>
<h2 id="toc-25f">总结</h2>
<ul>
<li>设计是把双刃剑，繁简需要权衡，尺度需要把握。</li>
<li>写代码简单，程序设计不易，需要走心。</li>
</ul>
<p>上面六个版本大家喜欢哪一个，或者有什么其他的思路，欢迎在评论区讨论。</p>
---------------
<h1 id="#title_9" >10、Microsoft Edge更新：支持WebVR，使Flash可以即点即运行</h1>
James Chesters
[http://www.infoq.com/cn/news/2017/01/edge-webvr-flash?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/01/edge-webvr-flash?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/news/2017/01/edge-webvr-flash/zh/headerimage/thumbnail.jpg"/><p>微软已经在2017年开始推出 Windows 10 builds 15002和15007给最终用户，针对Edge多进程模型、即点即用的Flash内容和对WebVR更新的支持为开发人员提供了一个全新的UWP架构。</p> <i>By James Chesters</i> <i> Translated by 冬雨</i>
---------------
<h1 id="#title_10" >11、Java 10将带来升级版的Lambda</h1>
Abraham Marín Pérez
[http://www.infoq.com/cn/news/2017/01/java10-lambda-leftovers?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/01/java10-lambda-leftovers?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/news/2017/01/java10-lambda-leftovers/zh/headerimage/GettyImages-480733685.jpg"/><p>一个新的JEP将用于增强lambda功能，提出的更改包括更好的消岐、对未使用的参数用下划线标注和外部变量的跟踪。虽然这些更改会使Java中的lambda表达式更类似于其它语言，但是初始讨论表明大家都不同程度地支持这个方案。这个JEP补充了一系列其他建议来改进Java语言，包括局部变量类型推断和增强的枚举，所有这些改进都可能出现在Java 10中。</p> <i>By Abraham Marín Pérez</i> <i> Translated by 尚剑</i>
---------------
<h1 id="#title_11" >12、5分钟现场撸代码——谈总结会抽奖程序</h1>

[https://www.h5jun.com/post/luckey-draw-in-5-minutes.html](https://www.h5jun.com/post/luckey-draw-in-5-minutes.html)
<div class="toc"><ul>
<li></li>
<li></li>
<li></li>
<li></li>
<li></li>
<li></li>
</ul>
</div><p>昨天给摄像机，<strong>在开会前5分钟</strong>，裕波临时说要写一个抽奖程序，现场抽10名中奖的小伙伴，于是这个抽奖任务就理（莫）所（名）当（其）然（妙）地落到了我这个团长的头上。</p>
<p>闲话少说，那么如何在开会前现场写一个抽奖程序，满足这一要求呢？</p>
<!--more-->
<p>首先，裕波、成银用白纸给同学做了简单的“奖券”，奖券上只有号码，从 1 ~ 62，一共有 62 人，从其中要公平地抽取出 10 人，而且不重复。所以，初步判断，这是一个简单的随机抽取过程，有 N 个数，从中抽出 M 个（M &lt; N）。直接随机抽取是最容易想到的：</p>
<h3 id="toc-5bf">直接抽取</h3>
<pre><code class="lang-js">const cards = Array(62).fill().map((_,i)=&gt;i+1); //初始化一个 1~62 的数组

function draw(n = 1){ // 一次抽取 n 个，默认一次 1 个
    var ret = [];
    for(var i = 0; i &lt; n; i++){
        let idx = Math.floor(cards.length * Math.random());
        ret.push(...cards.splice(idx, 1));
    }
    return ret;
}
console.log(draw(10)); //抽取一次，10个中奖者
</code></pre>
<p>上面这个方法非常直观，首先生成一个顺序的 1 ~ 62 号的数组，然后从其中随机抽取 10 次，为了不重复，将抽取的数字通过 <code>cards.splice(idx, 1)</code> 从原数组中取出来。</p>
<p>上面这种方式可行，但它不是最好的，因为每次 splice 一个数字，取 10 个数字需要 splice 10 次，这看起来不是特别好。可以想到另一种方法，先对数组进行，然后一次把 10 个数字取出来：</p>
<h3 id="toc-42e">先洗牌</h3>
<pre><code class="lang-js">function draw(amount, n = 1){
    const cards = Array(amount).fill().map((_,i)=&gt;i+1); 

    for(let i = amount - 1; i &gt;= 0; i--){
        let rand = Math.floor((i + 1) * Math.random());
        [cards[rand], cards[i]] =  [cards[i], cards[rand]];
    }
    return cards.slice(0, n);
}
console.log(draw(62, 10));
</code></pre>
<p>上面这个版本是月影实际现场写出的（略有修改），它是不错的，但是它也有明显缺点。首先它先把所有的牌都排序了，但实际上只需要排序 10 张牌就好，多余的排序没有必要。其次，它不方便连续抽奖，比如第一次抽取 10 个号，然后再想多抽取 5 个号，它就做不到了。</p>
<p>我们先解决第一个问题：</p>
<h3 id="toc-ef6">不需要洗所有的牌</h3>
<pre><code class="lang-js">function draw(amount, n = 1){
    const cards = Array(amount).fill().map((_,i)=&gt;i+1); 

    for(let i = amount - 1, stop = amount - n - 1; i &gt; stop; i--){
        let rand = Math.floor((i + 1) * Math.random());
        [cards[rand], cards[i]] =  [cards[i], cards[rand]];
    }
    return cards.slice(-n);
}
console.log(draw(62, 10));
</code></pre>
<p>上面这个版本是优化过的版本，显然如果取 10 个数，只需要循环 10 次即可，不需要把 64 张牌都洗了。</p>
<p>要解决可以连续抽奖的问题，就需要把 cards 提取出来（就像方案 1 的随机抽取一样），但是那样的话就使得函数<strong>有副作用</strong>，虽说是临时写一个抽奖，也不喜欢设计得太糙。或者，那就加一个构造器执行初始化？</p>
<h3 id="toc-6f1">构造器负责初始化</h3>
<pre><code class="lang-js">function Box(amount){
    this.cards = Array(amount).fill().map((_,i)=&gt;i+1); 
}
Box.prototype.draw = function(n = 1){
    let amount = this.cards.length, cards = this.cards;

    for(let i = amount - 1, stop = amount - n - 1; i &gt; stop; i--){
        let rand = Math.floor((i + 1) * Math.random());
        [cards[rand], cards[i]] =  [cards[i], cards[rand]];
    }

    let ret = cards.slice(-n);    
    cards.length = amount - n;

    return ret;
}

var box = new Box(62);
console.log(box.draw(5), box.draw(5)); //一次取 5 个，取 2 次
</code></pre>
<h3 id="toc-db5">更优雅的解决方式？</h3>
<p>实际上，对于一次可能抽取任意多个获奖人的场景，用 ES6 的  非常合适，我们可以直接拿洗牌的版本略做修改：</p>
<pre><code class="lang-js">function * draw(amount){
    const cards = Array(amount).fill().map((_,i)=&gt;i+1); 

    for(let i = amount - 1; i &gt;= 0; i--){
        let rand = Math.floor((i + 1) * Math.random());
        [cards[rand], cards[i]] =  [cards[i], cards[rand]];
        yield cards[i];
    }
}
var drawer = draw(62);

console.log(Array(10).fill().map(()=&gt;drawer.next().value)); //一次取出10个结果
</code></pre>
<p>最后补充一个小技巧，利用 <code>Array(n).fill().map(...)</code> 可以方便快速地构造数组：</p>
<pre><code class="lang-js">Array(10).fill().map((_,i) =&gt; i+1); // 得到 [1,2,3,4,5,6,7,8,9,10]
</code></pre>
<h3 id="toc-25f">总结</h3>
<p>现场抽奖需求虽简单，但也有那么多可以思考的点，不知道你 get 到哪些点，不知道你喜欢哪个版本的代码。或者你有自己的思路？欢迎在底部评论区写下来~</p>
---------------
<h1 id="#title_12" >13、FEX 技术周刊 - 2017/01/23</h1>

[http://fex.baidu.com/blog/2017/01/fex-weekly-23//](http://fex.baidu.com/blog/2017/01/fex-weekly-23//)
作者：zhangtao <br> <h2 id="section">深阅读</h2>

<p><strong>webpack 2.2: The Final Release</strong><br />
https://medium.com/webpack/webpack-2-2-the-final-release-76c3d43bf144#.5g9b4ros0<br />
升级指南 https://webpack.js.org/guides/migrating/</p>

<p><strong>阿里9年，我总结的前端架构演进3大阶段及团队管理心法</strong><br />
http://mp.weixin.qq.com/s?__biz=MjM5MDE0Mjc4MA==&amp;mid=2650995238&amp;idx=1&amp;sn=0c639d9186a5fa02175291694f96d03b<br />
技术人生就是在不断地修行，每个人都有每个人的功课，每个人也有每个人的精彩。你也许刚上路，又或许踽踽独行了很久，听听别人的故事没准也能帮助自己的成长。在阿里修行的9年，他学会了这些。</p>

<p><strong>egg.js 文档第一版发布</strong><br />
https://eggjs.org/zh-cn/intro/<br />
egg 为企业级框架和应用而生，在阿里内部广泛使用，我们希望由 egg 孕育出更多上层框架，帮助开发团队和开发人员降低开发和维护成本。文档质量非常高，从中可以学到很多框架设计及 Node 企业级应用开发的知识，比如这两篇：，文档和框架绝对都是良心之作，不看必悔。</p>

<p><strong>2016 JavaScript Rising Stars</strong><br />
https://risingstars2016.js.org/<br />
The JavaScript community is going full speed on innovation, what was once trendy becomes old-fashioned a few months later. 2016 is over, you may think you missed something important? Don’t worry, we are going to review what were the main trends.</p>

<p><strong>Styled-Components: Enforcing Best Practices In Component-Based Systems</strong><br />
https://www.smashingmagazine.com/2017/01/styled-components-enforcing-best-practices-component-based-systems/<br />
As we’ve built more and more apps with components, we’ve discovered some best practices when working with them. I want to talk about three main ones today: building small, focused and independent components; splitting container and presentational components; and having single-use CSS class names.</p>

<p><strong>The Infrastructure Behind Twitter: Scale</strong><br />
https://blog.twitter.com/2017/the-infrastructure-behind-twitter-scale<br />
Twitter came of age when hardware from physical enterprise vendors ruled the data center. Since then we’ve continually engineered and refreshed our fleet to take advantage of the latest open standards in technology and hardware efficiency in order to deliver the best possible experience.</p>

<p><strong>Caching at Reddit</strong><br />
https://redditblog.com/2017/1/17/caching-at-reddit/<br />
In this post we’ll talk about some of the nuts-and-bolts numbers of Reddit’s caching infrastructure—the number of instances, size of instances, and overall throughput. We hope that sharing this information may help others gauge what type of performance and sizing they can expect when building similar clusters. At the very least, we hope you’ll find it interesting to see a bit more about how Reddit works under the hood.</p>

<p><strong>The Problem With AMP</strong><br />
https://80x24.net/post/the-problem-with-amp/<br />
感兴趣的同学可以研究下 Google 的 AMP https://www.ampproject.org/ ，相关文章：</p>

<p><strong>Speeding up V8 Regular Expressions</strong><br />
http://v8project.blogspot.com/2017/01/speeding-up-v8-regular-expressions.html<br />
This blog post covers V8’s recent migration of RegExp’s built-in functions from a self-hosted JavaScript implementation to one that hooks straight into our new code generation architecture based on TurboFan. V8’s RegExp implementation is built on top of Irregexp, which is widely considered to be one of the fastest RegExp engines.</p>

<p><strong>Introducing Riptide:<br />
WebKit’s Retreating Wavefront Concurrent Garbage Collector</strong><br />
https://webkit.org/blog/7122/introducing-riptide-webkits-retreating-wavefront-concurrent-garbage-collector/
JSC终于也有并发 GC 了，另附，</p>

<p><strong>Google发布新的图像压缩技术，最高可节省75％带宽</strong><br />
https://blog.google/products/google-plus/saving-you-bandwidth-through-machine-learning/<br />
http://mp.weixin.qq.com/s?__biz=MzA5Nzc4OTA1Mw==&amp;mid=2659598877&amp;idx=1&amp;sn=704e7d5a05adaff567c9adf015753124
Google刚刚发布了一种名为RAISR（Rapid and Accurate Super Image Resolution，意为“快速、精确的超级图像分辨率技术”）的图像压缩技术，旨在保存宝贵的数据，而不牺牲照片质量；并在带宽受限的移动设备上提供清晰锐利的图像。Google声称，该技术可以降低高达75％的带宽，RAISR分析同一图像的低分辨率和高分辨率版本，了解到高分辨率版本出众的原因，然后在低分辨率版本模拟出来。</p>

<p><strong>React at 60fps</strong><br />
https://hackernoon.com/react-at-60fps-4e36b8189a4c#.dga0jalth<br />
React is an abstraction over the DOM and as any abstraction, it has its costs and limitations that you may hit sooner or later. Understanding and being able to overcome such limitations are important parts of working with an abstraction. 另附：</p>

<p><strong>[译]前端性能优化の备忘录(2017版)</strong><br />
https://www.w3ctech.com/topic/1945<br />
虽说Micro-optimization可以让你的性能优化手段起作用，但是(我觉得大家)还是应该在思想层面上树立一个明确的目标，这是因为目标量化会影响整个项目期间所作出的任何决定，所以说树立明确的目标才是至关重要的。(至于如何解决前端性能问题)，这里有很多不同的优化模型(model)，不过我们下面将要讨论的(优化模型)内容是十分武断的，所以你只需要确保(在使用上述优化模型时)使用自己的优先次序就行啦。</p>

<p><strong>Improve Your Node.js App Throughput One Micro-optimization at a Time</strong><br />
https://www.infoq.com/articles/node-micro-optimizations-javascript<br />
In order to improve the performance of an application that involves IO, you should understand how your CPU cycles are spent and, more importantly, what is preventing higher degrees of parallelism in your application. While focusing on improving the overall performance of the DataStax Node.js driver for Apache Cassandra, I’ve gained some insights that I share in this article, trying to summarize the most significant areas that could cause throughput degradation in your application.</p>

<p><strong>Modernizing our Progressive Enhancement Delivery</strong><br />
https://www.filamentgroup.com/lab/modernizing-delivery.html<br />
For more than a decade here at Filament Group, we’ve been scrutinizing and updating our workflow for delivering broadly accessible, fault-tolerant websites. Much of that time was spent making small, subtle refinements, but there were several moments where we made larger and philosophical changes to the way we deliver sites as well.</p>

<p><strong>10 Node.js Best Practices: Enlightenment from the Node Gurus</strong><br />
https://www.sitepoint.com/node-js-best-practices-from-the-node-gurus/<br />
In my previous article , I introduced 10 Node.js tips, tricks and techniques you could apply to your code today. This post continues in that vein with a further 10 best practices to help you take your Node skills to the next level.</p>

<p><strong>Virtual DOM is the new IR</strong><br />
https://medium.com/@jiyinyiyong/virtual-dom-is-the-new-ir-67839bcb5c71#.8y15dub50<br />
An intermediate representation is a representation of a program part way between the source and target languages. A good IR is one that is fairly independent of the source and target languages, so that it maximizes its ability to be used in a retargetable compiler.</p>

<p><strong>Node.js Async Best Practices &amp; Avoiding Callback Hell - Node.js at Scale</strong><br />
https://blog.risingstack.com/node-js-async-best-practices-avoiding-callback-hell-node-js-at-scale/<br />
In this post, we cover what tools and techniques you have at your disposal when handling Node.js asynchronous operations: async.js, promises, generators and async functions. After reading this article, you’ll know how to avoid the despised callback hell!</p>

<p><strong>THE LINE OF DEATH</strong><br />
https://textslashplain.com/2017/01/14/the-line-of-death/<br />
When building applications that display untrusted content, security designers have a major problem— if an attacker has full control of a block of pixels, he can make those pixels look like anything he wants, including the UI of the application itself. He can then induce the user to undertake an unsafe action, and a user will be none the wiser.</p>

<p><strong>Asyncing Feeling about JavaScript Generators</strong><br />
https://www.bignerdranch.com/blog/asyncing-feeling-about-javascript-generators/ <br />
Async generators and async iteration have arrived! Err, they’ve reached Stage 3, which means they are likely to ship in a future version of JavaScript. Until then, you can enable Stage 3 proposals in Babel to try them out in your own projects.</p>

<p><strong>百度第三代 Spider 背后的万亿量级实时数据处理系统</strong><br />
http://mp.weixin.qq.com/s?__biz=MjM5MDE0Mjc4MA==&amp;mid=2650995223&amp;idx=1&amp;sn=9c2722a2dcddbc26eefc437a1e82531b<br />
信息技术发展突飞猛进，网络数据呈现爆炸之势，线性扩展面临高昂成本。Spider系统是百度搜索引擎的主要数据来源，每天处理着数万亿次的链接分析和数百亿次的互联网资源采集。那么，第三代Spider是怎样“化繁就简”实现增量式流式处理的呢？</p>

<p><strong>[译]Bluebird 是如何做到比原生实现更快的</strong><br />
http://mp.weixin.qq.com/s?__biz=MzA4NjE3MDg4OQ==&amp;mid=2650964223&amp;idx=1&amp;sn=f2c37c05fb6ad370a67c59ca745bd7bf<br />
Bluebird 是一个广泛使用的 Promise 库，最早在 2013 年得到人们的关注。相比其他同等水平的 Promise 库，Bluebird 快了一百来倍。Bluebird 自始至终遵循着 JavaScript 优化的一些基本原则，所以才有这么好的性能。本文将会介绍其中最有价值的三个方面。</p>

<p><strong>Native ECMAScript modules - the first overview</strong><br />
https://blog.hospodarets.com/native-ecmascript-modules-the-first-overview<br />
ES6 模块化方案的尝试，以后就不需要打包工具了</p>

<p><strong>当我们在抢红包时，微信运维在做什么？</strong><br />
http://mp.weixin.qq.com/s/DhHz99KzXaA6c1VXEt0flA<br />
微信红包的数据库运维经验</p>

<p><strong>Docker Introduction</strong><br />
https://tobiastom.name/explains/docker<br />
非常不错的一篇介绍 Docker 的文章。</p>

<p><strong>A Brief History of JavaScript</strong><br />
https://auth0.com/blog/a-brief-history-of-javascript/<br />
JavaScript is arguably one of the most important languages today. The rise of the web has taken JavaScript places it was never conceived to be. We take a look at how JavaScript has evolved in its short history, and where it is headed. Read on!</p>

<h2 id="section-1">新鲜货</h2>

<p><strong>Chrome开发者工具的小技巧</strong><br />
http://coolshell.cn/articles/17634.html<br />
Chrome的开发者工具是个很强大的东西，相信程序员们都不会陌生，不过有些小功能可能并不为大众所知，所以，写下这篇文章罗列一下可能你所不知道的功能，有的功能可能会比较实用，有的则不一定。</p>

<p><strong>3 New CSS Features to Learn in 2017</strong><br />
https://bitsofco.de/3-new-css-features-to-learn-in-2017/<br />
With the new year, we have a whole new set of things to learn. Although there are many new features, these are 3 new CSS features I’m most excited about adopting this year.</p>

<p><strong>5 web trends for 2017</strong><br />
https://www.oreilly.com/ideas/5-web-trends-for-2017<br />
What’s coming with PWAs, Angular, React, and Vue; the rising tide of functional reactive; looking beyond REST to GraphQL and Falcor; and the future of artificial intelligence on the web.</p>

<p><strong>ChakraCore’s first anniversary</strong><br />
https://blogs.windows.com/msedgedev/2017/01/13/chakracores-first-anniversary/#r5Kc6qJRc0uvz88l.97<br />
开源一周年，虽然用得不多，但还是有不少进步</p>

<p><strong>search update: improved search in the npm CLI (and how we got here)</strong><br />
http://blog.npmjs.org/post/156076312840/search-update<br />
Over last month’s holidays, with the help of npms.io, npm introduced an improved search platform and brought it to the npmjs.com web experience. We’re really proud of how this project went: it was an opportunity to work with folks in the community and pull in an open-source solution that people love. As we promised at the time, here are some more details about the how and the why, and an exciting announcement about bringing new search to the npm command-line tool.</p>

<p><strong>Welcoming Fabric to Google</strong><br />
https://firebase.googleblog.com/2017/01/FabricJoinsGoogle17.html<br />
Twitter 移动应用开发者工具 Fabric 被 Google 收购</p>

<p><strong>Super charge your Sublime Text 3 to increase your productivity</strong> <br />
https://hackernoon.com/super-charge-your-sublime-text-3-to-increase-your-productivity-5d02c2c1b356#.cs0j57lht<br />
一些快捷键和配置技巧</p>

<p><strong>Awesome dataviz</strong><br />
https://github.com/fasouto/awesome-dataviz<br />
译文： https://yq.aliyun.com/articles/45517</p>

<p><strong>Awesome_API</strong><br />
https://github.com/marktony/Awesome_API<br />
A collection of APIs</p>

<p><strong>mo.js - Motion Graphics For The Web</strong><br />
http://mojs.io/<br />
Designed for building Retina-ready ‘silky smooth’ animations and effects.</p>

<p><strong>React Table</strong><br />
https://github.com/tannerlinsley/react-table<br />
react-table is a lightweight, fast and extendable datagrid built for React.</p>

<p><strong>Introducing Draco: compression for 3D graphics</strong><br />
https://opensource.googleblog.com/2017/01/introducing-draco-compression-for-3d.html<br />
谷歌出的 3D 模型压缩格式，很适合 Web 及移动端</p>

<p><strong>WebSlides</strong><br />
https://github.com/jlantunez/webslides<br />
一个新的 Web 演示工具</p>

<p><strong>iView</strong><br />
https://www.iviewui.com/<br />
一个 VUE 的 UI 库</p>

<p><strong>Big List of Naughty Strings</strong><br />
https://github.com/minimaxir/big-list-of-naughty-strings<br />
各种奇怪的字符，用来测试程序健壮性</p>

<p><strong>mathsteps</strong><br />
https://github.com/socraticorg/mathsteps<br />
Step by steps math solutions for everyone. 详细介绍：</p>

<p><strong>Most used words in programming languages</strong><br />
https://anvaka.github.io/common-words/#?lang=js</p>

<p><strong>2016 Top 10 Android Library</strong> <br />
http://stormzhang.com/2017/01/16/top-10-android-library-of-2016/<br />
过去的 2016 年，开源社区异常活跃，很多个人与公司争相开源自己的项目，让人眼花缭乱，然而有些项目只是昙花一现，有些项目却持久创造价值，为开发者提供了极大的便利，这些终究由时间来判断。</p>

<h2 id="section-2">产品及其它</h2>

<p><strong>2016 年那些 10w+ 文章是怎么刷爆朋友圈的</strong><br />
http://mp.weixin.qq.com/s?__biz=MTEwNTM0ODI0MQ==&amp;mid=2653433859&amp;idx=1&amp;sn=c2adc899029523992058f2dcd966c5b4<br />
文中的传播路径图蛮有意思的。</p>

<p><strong>你看到的大多数小程序，可能都在做错误的事情</strong><br />
http://mp.weixin.qq.com/s?__biz=MjM5NDUyOTAwOA==&amp;mid=2652914751&amp;idx=1&amp;sn=d14ba034872872439702daa39a7bc558<br />
一周内，我们看到了一群小程序开发者抢在“风口”来临时发布了他们的产品。一周内，我们看到“得到”的小程序下线了，看到“今日头条”的小程序“暂停服务”了。一周内，我们看到大家尝鲜、转发之后，再没声响了。在小程序正式面世后的一周，我梳理了一些信息，也做了一些小调查，接下来我会在这篇文章中把我的一些观察分享给大家。</p>
---------------
<h1 id="#title_13" >14、为什么 [ ] 是 false 而 !![ ] 是 true</h1>

[https://www.h5jun.com/post/why-false-why-true.html](https://www.h5jun.com/post/why-false-why-true.html)
<div class="toc"></div><p>今天是 JavaScript 课程的第一天。下午的时候给学生介绍 JavaScript 的基本类型，例子中有个有趣的问题，因为时间仓促，没能详细解释。所以写一篇文章来解释，正好也考考大家：</p>
<p><strong>问题：为什么 [ ] == false，而 !![ ] == true？</strong></p>
<!--more-->
<p>这是一个很有迷惑性的问题。咋一看，不可能啊？如果 [ ] == false，那么 !![ ] 相当于 !!false，难道不是为 false 吗，为什么会是 true 呢？会不会是引擎 bug，搞错了？</p>
<pre><code class="hljs lang-js"><span class="hljs-built_in">console</span>.log([] == <span class="hljs-literal">false</span>, !![] == <span class="hljs-literal">true</span>); <span class="hljs-comment">// true, true</span>
</code></pre>
<p>事实上不是 bug，这与 ECMA 规范和类型转换有关。我们知道，非严格比较操作符 == 是会做强制类型转换的，那么根据  它的规则是：</p>
<p><img src="https://p5.ssl.qhimg.com/t0148b4e8aacee1b427.png" alt="">
<em>来源：</em></p>
<p>注意一下：</p>
<ul>
<li>第 7 条：<strong>If Type(y) is Boolean, return the result of the comparison x == ToNumber(y).</strong></li>
<li>第 9 条：<strong>If Type(x) is Object and Type(y) is either String, Number, or Symbol, return the result of the comparison ToPrimitive(x) == y.</strong></li>
</ul>
<p>所以 <code>[] == false</code> 的比较是对 x 执行 ToPrimitive(x)，然后和 ToNumber(false) （为 0）进行比较。</p>
<p>看一下 ToPrimitive：</p>
<p><img src="https://p1.ssl.qhimg.com/t01ee334a9e744a7ad0.png" alt="">
<em>来源：</em></p>
<p><img src="https://p0.ssl.qhimg.com/t01f9a98210a6d6f72f.png" alt="">
<em>来源：</em></p>
<p><img src="https://p2.ssl.qhimg.com/t01dcfaaa4051797781.png" alt="">
<em>来源：</em></p>
<p>根据上面的规则对于 ToPrimitive([ ])，先执行 <code>[].valueOf()</code>，返回 result 的是 [ ]，因为 Type(result) 是 Object，所以继续执行 <code>[].toString()</code>，返回 <code>&quot;&quot;</code>。</p>
<p>因此实际上最终是比较 <code>&quot;&quot; == 0</code>，结果为 true。</p>
<p>再来看 <code>!![] == false</code>：</p>
<p>按照优先级，先执行 <code>!![]</code>，根据规范，实际上是 <code>!!(ToBoolean([]))</code>：</p>
<p><img src="https://p1.ssl.qhimg.com/t0103c93877b67a31ff.png" alt=""></p>
<p>而 ToBoolean 的规则是：</p>
<p><img src="https://p2.ssl.qhimg.com/t0112867db718bf0665.png" alt=""></p>
<p>所以 <code>ToBoolean([])</code> 被转成 true，<code>!!true</code> 自然是 true 了。</p>
<p>所以这就是 <code>[] == false</code> 而 <code>!![] == true</code> 的真正原因了。这也是为什么我们不能用 <code>if(!array)</code> 来判断空数组而要用 <code>if(array.length === 0)</code> 来判断空数组的原因。</p>
<p>同样，还有 <code>[0] == false</code> 而 <code>!![0] == true</code>，现在你自己能分析出原因了。</p>
<p>以上就是今天的内容，如果有任何疑问，欢迎留言讨论~</p>
---------------
<h1 id="#title_14" >15、文章： 包容协作与静默实验</h1>
Sallyann Freudenberg
[http://www.infoq.com/cn/articles/inclusive-collaboration-silence-experiment?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/inclusive-collaboration-silence-experiment?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/inclusive-collaboration-silence-experiment/zh/smallimage/logo.jpg"/><p>随着协作式方法成为软件行业的常态，是时候重新考虑协作，并提供包容各种思想者的工作场所和实践了。本文介绍了“包容协作（Inclusive Collaboration）”，并描述了“静默实验（Silence Experiment）”，以帮助团队思考协作的方方面面，从而更高效地与各种思想者协作。</p> <i>By Sallyann Freudenberg</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_15" >16、视频演讲： 携程多机房微服务灰度发布</h1>
王潇俊
[http://www.infoq.com/cn/presentations/ctrip-multi-room-micro-service-gray-release?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/ctrip-multi-room-micro-service-gray-release?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/ctrip-multi-room-micro-service-gray-release/zh/mediumimage/wangxiaojun270.jpg"/><p>随着微服务的流行，企业内部服务数大量增加，服务的部署架构也变得日益复杂起来。如何有效地设计和组织发布过程，如何合理地控制流程和质量，如何提高沟通效率，如何应对多 IDC 的复杂度，都成为了挑战。

本次分享中，我们将以携程的实际情况为例，从架构、流程、工具等方面介绍如何做到多 IDC 的有效灰度发布。</p> <i>By 王潇俊</i>
---------------
<h1 id="#title_16" >17、A Case Study: Is App Indexing For Google Worth The Effort?</h1>
Bryson Meunier
[https://www.smashingmagazine.com/2017/01/case-study-app-indexing-google-worth-the-effort/](https://www.smashingmagazine.com/2017/01/case-study-app-indexing-google-worth-the-effort/)
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
</table><p>Will the resources spent implementing app indexing for Google search be a boon or a bust for your app’s traffic? In this article, I’ll take you through a <strong>case study for app indexing</strong> at our company, the results of which may surprise you.</p>

<figure></figure>

<p>App indexing is one of the hottest topics in SEO right now, and in some sense for good reason. Google has only been indexing apps for everyone for a little more than two years, and with only 30% of apps being indexed there is huge potential for websites to draw additional search traffic to their apps.</p><p>The post .</p>
---------------