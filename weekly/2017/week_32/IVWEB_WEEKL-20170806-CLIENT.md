## 文章索引
1、 <a href="#1用信号来控制异步流程" >用信号来控制异步流程</a><br/><h1 id="#title_0" >1、用信号来控制异步流程</h1>

[https://www.h5jun.com/post/signals-and-async.html](https://www.h5jun.com/post/signals-and-async.html)
<div class="toc"><ul>
<li></li>
</ul>
</div><p>我们知道，JavaScript 不管是操作 DOM，还是执行服务端任务，不可避免需要处理许多异步调用。在早期，许多开发者仅仅通过 JavaScript 的回调方式来处理异步，但是那样很容易造成异步回调的嵌套，产生 “Callback Hell”。</p>
<p><img src="https://p1.ssl.qhimg.com/t012ba4a8fb02337f2f.jpg" alt=""> </p>
<!--more-->
<p>后来，一些开发者使用了 Promise 思想来避免异步回调的嵌套，社区将根据思想提出 Promise/A+ 规范，最终，在 ES6 中内置实现了 Promise 类，随后又基于 Promise 类在 ES2017 里实现了 async/await，形成了现在非常简洁的异步处理方式。</p>
<p>比如  下面这段代码就是典型的 async/await 用法，它看起来和同步的写法完全一样，只是增加了 async/await 关键字。</p>
<pre><code class="hljs lang-js"><span class="hljs-built_in">module</span>.exports = <span class="hljs-class"><span class="hljs-keyword">class</span> <span class="hljs-keyword">extends</span> <span class="hljs-title">think</span>.<span class="hljs-title">Controller</span> </span>{
  <span class="hljs-keyword">async</span> indexAction(){
    <span class="hljs-keyword">let</span> model = <span class="hljs-keyword">this</span>.model(<span class="hljs-string">'user'</span>);
    <span class="hljs-keyword">try</span>{
      <span class="hljs-keyword">await</span> model.startTrans();
      <span class="hljs-keyword">let</span> userId = <span class="hljs-keyword">await</span> model.add({name: <span class="hljs-string">'xxx'</span>});
      <span class="hljs-keyword">let</span> insertId = <span class="hljs-keyword">await</span> <span class="hljs-keyword">this</span>.model(<span class="hljs-string">'user_group'</span>).add({user_id: userId, group_id: <span class="hljs-number">1000</span>});
      <span class="hljs-keyword">await</span> model.commit();
    }<span class="hljs-keyword">catch</span>(e){
      <span class="hljs-keyword">await</span> model.rollback();
    }
  }
}
</code></pre>
<p>async/await 可以算是一种语法糖，它将</p>
<pre><code class="hljs lang-js">promise.then(res =&gt; {
    <span class="hljs-keyword">do</span> sth.
}).catch(err =&gt; {
    some error
})
</code></pre>
<p>转换成了</p>
<pre><code class="hljs lang-js"><span class="hljs-keyword">try</span>{
    res = <span class="hljs-keyword">await</span> promise
    <span class="hljs-keyword">do</span> sth
}<span class="hljs-keyword">catch</span>(err){
    some error
}
</code></pre>
<p>有了 async，await，可以写出原来很难写出的非常简单直观的代码：</p>
<p><script src="https:////code.h5jun.com/js/embed.min.js?3.40.2"></script></p>
<pre><code class="hljs lang-js"><span class="hljs-function"><span class="hljs-keyword">function</span> <span class="hljs-title">idle</span>(<span class="hljs-params">time</span>)</span>{
  <span class="hljs-keyword">return</span> <span class="hljs-keyword">new</span> <span class="hljs-built_in">Promise</span>(resolve=&gt;setTimeout(resolve, time))
}

(<span class="hljs-keyword">async</span> <span class="hljs-function"><span class="hljs-keyword">function</span>(<span class="hljs-params"></span>)</span>{
  <span class="hljs-comment">//noprotect</span>
  <span class="hljs-keyword">do</span> {
    traffic.className = <span class="hljs-string">'stop'</span>
    <span class="hljs-keyword">await</span> idle(<span class="hljs-number">1000</span>)
    traffic.className = <span class="hljs-string">'pass'</span>
    <span class="hljs-keyword">await</span> idle(<span class="hljs-number">1500</span>)
    traffic.className = <span class="hljs-string">'wait'</span>
    <span class="hljs-keyword">await</span> idle(<span class="hljs-number">500</span>)
  }<span class="hljs-keyword">while</span>(<span class="hljs-number">1</span>)
})()
</code></pre>
<p>上面的代码中，我们利用异步的 setTimeout 实现了一个 idle 的异步方法，返回 promise。许多异步处理过程都能让它们返回 promise，从而产生更简单直观的代码。</p>
<p>网页中的 JavaScript 还有一个问题，就是我们要响应很多异步事件，表示用户操作的异步事件其实不太好改写成 promise，事件代表控制，它和数据与流程往往是两个层面的事情，所以许多现代框架和库通过绑定机制把这一块封装起来，让开发者能够聚焦于操作数据和状态，从而避免增加系统的复杂度。</p>
<p>比如上面那个“交通灯”，这样写已经是很简单，但是如果我们要增加几个“开关”，表示“暂停/继续“和”开启/关闭”，要怎么做呢？如果我们还想要增加开关，人工控制和切换灯的转换，又该怎么实现呢？</p>
<p>有同学想到这里，可能觉得，哎呀这太麻烦了，用 async/await 搞不定，还是用之前传统的方式去实现吧。</p>
<p>其实即使用“传统”的思路，要实现这样的异步状态控制也还是挺麻烦的，但是我们的 PM 其实也经常会有这样麻烦的需求。</p>
<p>我们试着来实现一下：</p>
<p><script src="https:////code.h5jun.com/js/embed.min.js?3.40.2"></script></p>
<pre><code class="hljs lang-js"><span class="hljs-function"><span class="hljs-keyword">function</span> <span class="hljs-title">defer</span>(<span class="hljs-params"></span>)</span>{
  <span class="hljs-keyword">let</span> deferred = {}; 
  deferred.promise = <span class="hljs-keyword">new</span> <span class="hljs-built_in">Promise</span>((resolve, reject) =&gt; {
    deferred.resolve = resolve
    deferred.reject = reject
  })
  <span class="hljs-keyword">return</span> deferred
}

<span class="hljs-class"><span class="hljs-keyword">class</span> <span class="hljs-title">Idle</span> </span>{
  wait(time){
    <span class="hljs-keyword">this</span>.deferred = <span class="hljs-keyword">new</span> defer()
    <span class="hljs-keyword">this</span>.timer = setTimeout(()=&gt;{
      <span class="hljs-keyword">this</span>.deferred.resolve({canceled: <span class="hljs-literal">false</span>})
    }, time)

    <span class="hljs-keyword">return</span> <span class="hljs-keyword">this</span>.deferred.promise
  }
  cancel(){
    clearTimeout(<span class="hljs-keyword">this</span>.timer)
    <span class="hljs-keyword">this</span>.deferred.resolve({canceled: <span class="hljs-literal">true</span>})
  }
}

<span class="hljs-keyword">const</span> idleCtrl = <span class="hljs-keyword">new</span> Idle()

<span class="hljs-keyword">async</span> <span class="hljs-function"><span class="hljs-keyword">function</span> <span class="hljs-title">turnOnTraffic</span>(<span class="hljs-params"></span>)</span>{
  <span class="hljs-keyword">let</span> state;
  <span class="hljs-comment">//noprotect</span>
  <span class="hljs-keyword">do</span> {
    traffic.className = <span class="hljs-string">'stop'</span>
    state = <span class="hljs-keyword">await</span> idleCtrl.wait(<span class="hljs-number">1000</span>)
    <span class="hljs-keyword">if</span>(state.canceled) <span class="hljs-keyword">break</span>
    traffic.className = <span class="hljs-string">'pass'</span>
    state = <span class="hljs-keyword">await</span> idleCtrl.wait(<span class="hljs-number">1500</span>)
    <span class="hljs-keyword">if</span>(state.canceled) <span class="hljs-keyword">break</span>
    traffic.className = <span class="hljs-string">'wait'</span>
    state = <span class="hljs-keyword">await</span> idleCtrl.wait(<span class="hljs-number">500</span>)
    <span class="hljs-keyword">if</span>(state.canceled) <span class="hljs-keyword">break</span>
  }<span class="hljs-keyword">while</span>(<span class="hljs-number">1</span>)
  traffic.className = <span class="hljs-string">''</span>
}

turnOnTraffic()

onoffButton.onclick = <span class="hljs-function"><span class="hljs-keyword">function</span>(<span class="hljs-params"></span>)</span>{
  <span class="hljs-keyword">if</span>(traffic.className === <span class="hljs-string">''</span>){
    turnOnTraffic()
    onoffButton.innerHTML = <span class="hljs-string">'关闭'</span>
  } <span class="hljs-keyword">else</span> {
    onoffButton.innerHTML = <span class="hljs-string">'开启'</span>
    idleCtrl.cancel()
  }
}
</code></pre>
<p>上面这么做实现了控制交通灯的开启关闭。但是实际上这样的代码让 onoffButton、 idelCtrl 和 traffic 各种耦合，有点惨不忍睹……</p>
<p>这还只是最简单的“开启/关闭”，“暂停/继续”要比这个更复杂，还有用户自己控制灯的切换呢，想想都头大！</p>
<p>在这种情况下，因为我们把控制和状态混合在一起，所以程序逻辑不可避免地复杂了。这种复杂度与 callback 和 async/await 无关。<strong>async/await 只能改变程序的结构，并不能改变内在逻辑的复杂性。</strong></p>
<p>那么我们该怎么做呢？这里我们就要换一种思路，让信号（Signal）登场了！看下面的例子：</p>
<p><script src="https:////code.h5jun.com/js/embed.min.js?3.40.2"></script></p>
<pre><code class="hljs lang-js"><span class="hljs-class"><span class="hljs-keyword">class</span> <span class="hljs-title">Idle</span> <span class="hljs-keyword">extends</span> <span class="hljs-title">Signal</span> </span>{
  <span class="hljs-keyword">async</span> wait(time){
    <span class="hljs-keyword">this</span>.state = <span class="hljs-string">'wait'</span>
    <span class="hljs-keyword">const</span> timer = setTimeout(() =&gt; {
      <span class="hljs-keyword">this</span>.state = <span class="hljs-string">'timeout'</span>
    }, time)
    <span class="hljs-keyword">await</span> <span class="hljs-keyword">this</span>.while(<span class="hljs-string">'wait'</span>)
    clearTimeout(timer)
  }
  cancel(){
    <span class="hljs-keyword">this</span>.state = <span class="hljs-string">'cancel'</span>
  }
}

<span class="hljs-class"><span class="hljs-keyword">class</span> <span class="hljs-title">TrafficSignal</span> <span class="hljs-keyword">extends</span> <span class="hljs-title">Signal</span> </span>{
  <span class="hljs-keyword">constructor</span>(id){
    <span class="hljs-keyword">super</span>(<span class="hljs-string">'off'</span>)
    <span class="hljs-keyword">this</span>.container = <span class="hljs-built_in">document</span>.getElementById(id)
    <span class="hljs-keyword">this</span>.idle = <span class="hljs-keyword">new</span> Idle()
  }
  get lightStat(){
    <span class="hljs-keyword">return</span> <span class="hljs-keyword">this</span>.state
  }
  <span class="hljs-keyword">async</span> pushStat(val, dur = <span class="hljs-number">0</span>){
    <span class="hljs-keyword">this</span>.container.className = val
    <span class="hljs-keyword">this</span>.state = val
    <span class="hljs-keyword">await</span> <span class="hljs-keyword">this</span>.idle.wait(dur)
  }
  get canceled(){
    <span class="hljs-keyword">return</span> <span class="hljs-keyword">this</span>.idle.state === <span class="hljs-string">'cancel'</span>
  }
  cancel(){
    <span class="hljs-keyword">this</span>.pushStat(<span class="hljs-string">'off'</span>)
    <span class="hljs-keyword">this</span>.idle.cancel()
  }
}

<span class="hljs-keyword">const</span> trafficSignal = <span class="hljs-keyword">new</span> TrafficSignal(<span class="hljs-string">'traffic'</span>)

<span class="hljs-keyword">async</span> <span class="hljs-function"><span class="hljs-keyword">function</span> <span class="hljs-title">turnOnTraffic</span>(<span class="hljs-params"></span>)</span>{
  <span class="hljs-comment">//noprotect</span>
  <span class="hljs-keyword">do</span> {
    <span class="hljs-keyword">await</span> trafficSignal.pushStat(<span class="hljs-string">'stop'</span>, <span class="hljs-number">1000</span>)
    <span class="hljs-keyword">if</span>(trafficSignal.canceled) <span class="hljs-keyword">break</span>
    <span class="hljs-keyword">await</span> trafficSignal.pushStat(<span class="hljs-string">'pass'</span>, <span class="hljs-number">1500</span>)
    <span class="hljs-keyword">if</span>(trafficSignal.canceled) <span class="hljs-keyword">break</span>
    <span class="hljs-keyword">await</span> trafficSignal.pushStat(<span class="hljs-string">'wait'</span>, <span class="hljs-number">500</span>)
    <span class="hljs-keyword">if</span>(trafficSignal.canceled) <span class="hljs-keyword">break</span>
  }<span class="hljs-keyword">while</span>(<span class="hljs-number">1</span>)

  trafficSignal.lightStat = <span class="hljs-string">'off'</span>
}


turnOnTraffic()

onoffButton.onclick = <span class="hljs-function"><span class="hljs-keyword">function</span>(<span class="hljs-params"></span>)</span>{
  <span class="hljs-keyword">if</span>(trafficSignal.lightStat === <span class="hljs-string">'off'</span>){
    turnOnTraffic()
    onoffButton.innerHTML = <span class="hljs-string">'关闭'</span>
  } <span class="hljs-keyword">else</span> {
    onoffButton.innerHTML = <span class="hljs-string">'开启'</span>
    trafficSignal.cancel()
  }
}
</code></pre>
<p>我们对代码进行一些修改，封装一个 TrafficSignal，让 onoffButton 只控制 traficSignal 的状态。这里我们用一个简单的 ，它可以实现状态和控制流的分离，例如：</p>
<p><script src="https:////code.h5jun.com/js/embed.min.js?3.40.2"></script></p>
<pre><code class="hljs lang-js"><span class="hljs-keyword">const</span> signal = <span class="hljs-keyword">new</span> Signal(<span class="hljs-string">'default'</span>)

;(<span class="hljs-keyword">async</span> () =&gt; {
    <span class="hljs-keyword">await</span> signal.while(<span class="hljs-string">'default'</span>)
    <span class="hljs-built_in">console</span>.log(<span class="hljs-string">'leave default state'</span>)
})()

;(<span class="hljs-keyword">async</span> () =&gt; {
    <span class="hljs-keyword">await</span> signal.until(<span class="hljs-string">'state1'</span>)
    <span class="hljs-built_in">console</span>.log(<span class="hljs-string">'to state1'</span>)
})()

;(<span class="hljs-keyword">async</span> () =&gt; {
    <span class="hljs-keyword">await</span> signal.until(<span class="hljs-string">'state2'</span>)
    <span class="hljs-built_in">console</span>.log(<span class="hljs-string">'to state2'</span>)
})()

;(<span class="hljs-keyword">async</span> () =&gt; {
    <span class="hljs-keyword">await</span> signal.until(<span class="hljs-string">'state3'</span>)
    <span class="hljs-built_in">console</span>.log(<span class="hljs-string">'to state3'</span>)
})()

setTimeout(() =&gt; {
    signal.state = <span class="hljs-string">'state0'</span>
}, <span class="hljs-number">1000</span>)

setTimeout(() =&gt; {
    signal.state = <span class="hljs-string">'state1'</span>
}, <span class="hljs-number">2000</span>)

setTimeout(() =&gt; {
    signal.state = <span class="hljs-string">'state2'</span>
}, <span class="hljs-number">3000</span>)

setTimeout(() =&gt; {
    signal.state = <span class="hljs-string">'state3'</span>
}, <span class="hljs-number">4000</span>)
</code></pre>
<p>有同学说，这样写代码也不简单啊，代码量比上面写法还要多。的确这样写代码量是比较多的，但是它结构清晰，耦合度低，可以很容易扩展，比如：</p>
<p><script src="https:////code.h5jun.com/js/embed.min.js?3.40.2"></script></p>
<pre><code class="hljs lang-js"><span class="hljs-class"><span class="hljs-keyword">class</span> <span class="hljs-title">Idle</span> <span class="hljs-keyword">extends</span> <span class="hljs-title">Signal</span> </span>{
  <span class="hljs-keyword">async</span> wait(time){
    <span class="hljs-keyword">this</span>.state = <span class="hljs-string">'wait'</span>
    <span class="hljs-keyword">const</span> timer = setTimeout(() =&gt; {
      <span class="hljs-keyword">this</span>.state = <span class="hljs-string">'timeout'</span>
    }, time)
    <span class="hljs-keyword">await</span> <span class="hljs-keyword">this</span>.while(<span class="hljs-string">'wait'</span>)
    clearTimeout(timer)
  }
  cancel(){
    <span class="hljs-keyword">this</span>.state = <span class="hljs-string">'cancel'</span>
  }
}

<span class="hljs-class"><span class="hljs-keyword">class</span> <span class="hljs-title">TrafficSignal</span> <span class="hljs-keyword">extends</span> <span class="hljs-title">Signal</span> </span>{
  <span class="hljs-keyword">constructor</span>(id){
    <span class="hljs-keyword">super</span>(<span class="hljs-string">'off'</span>)
    <span class="hljs-keyword">this</span>.container = <span class="hljs-built_in">document</span>.getElementById(id)
    <span class="hljs-keyword">this</span>.idle = <span class="hljs-keyword">new</span> Idle()
  }
  get lightStat(){
    <span class="hljs-keyword">return</span> <span class="hljs-keyword">this</span>.state
  }
  <span class="hljs-keyword">async</span> pushStat(val, dur = <span class="hljs-number">0</span>){
    <span class="hljs-keyword">this</span>.container.className = val
    <span class="hljs-keyword">this</span>.state = val
    <span class="hljs-keyword">if</span>(dur) <span class="hljs-keyword">await</span> <span class="hljs-keyword">this</span>.idle.wait(dur)
  }
  get canceled(){
    <span class="hljs-keyword">return</span> <span class="hljs-keyword">this</span>.idle.state === <span class="hljs-string">'cancel'</span>
  }
  cancel(){
    <span class="hljs-keyword">this</span>.idle.cancel()
    <span class="hljs-keyword">this</span>.pushStat(<span class="hljs-string">'off'</span>)
  }
}

<span class="hljs-keyword">const</span> trafficSignal = <span class="hljs-keyword">new</span> TrafficSignal(<span class="hljs-string">'traffic'</span>)

<span class="hljs-keyword">async</span> <span class="hljs-function"><span class="hljs-keyword">function</span> <span class="hljs-title">turnOnTraffic</span>(<span class="hljs-params"></span>)</span>{
  <span class="hljs-comment">//noprotect</span>
  <span class="hljs-keyword">do</span> {
    <span class="hljs-keyword">await</span> trafficSignal.pushStat(<span class="hljs-string">'stop'</span>, <span class="hljs-number">1000</span>)
    <span class="hljs-keyword">if</span>(trafficSignal.canceled) <span class="hljs-keyword">break</span>
    <span class="hljs-keyword">await</span> trafficSignal.pushStat(<span class="hljs-string">'pass'</span>, <span class="hljs-number">1500</span>)
    <span class="hljs-keyword">if</span>(trafficSignal.canceled) <span class="hljs-keyword">break</span>
    <span class="hljs-keyword">await</span> trafficSignal.pushStat(<span class="hljs-string">'wait'</span>, <span class="hljs-number">500</span>)
    <span class="hljs-keyword">if</span>(trafficSignal.canceled) <span class="hljs-keyword">break</span>
  }<span class="hljs-keyword">while</span>(<span class="hljs-number">1</span>)

  trafficSignal.lightStat = <span class="hljs-string">'off'</span>
}


turnOnTraffic()

onoffButton.onclick = <span class="hljs-function"><span class="hljs-keyword">function</span>(<span class="hljs-params"></span>)</span>{
  <span class="hljs-keyword">if</span>(trafficSignal.lightStat === <span class="hljs-string">'off'</span>){
    turnOnTraffic()
    onoffButton.innerHTML = <span class="hljs-string">'关闭'</span>
  } <span class="hljs-keyword">else</span> {
    onoffButton.innerHTML = <span class="hljs-string">'开启'</span>
    trafficSignal.cancel()
  }
}

turnRed.onclick = <span class="hljs-function"><span class="hljs-keyword">function</span>(<span class="hljs-params"></span>)</span>{
  trafficSignal.cancel()
  trafficSignal.pushStat(<span class="hljs-string">'stop'</span>)
}

turnGreen.onclick = <span class="hljs-function"><span class="hljs-keyword">function</span>(<span class="hljs-params"></span>)</span>{
  trafficSignal.cancel()
  trafficSignal.pushStat(<span class="hljs-string">'pass'</span>)
}

turnYellow.onclick = <span class="hljs-function"><span class="hljs-keyword">function</span>(<span class="hljs-params"></span>)</span>{
  trafficSignal.cancel()
  trafficSignal.pushStat(<span class="hljs-string">'wait'</span>)
}
</code></pre>
<p>Signal 非常适合于事件控制的场合，再举一个更简单的例子，如果我们用一个按钮控制简单的动画的暂停和执行，可以这样写：</p>
<p><script src="https:////code.h5jun.com/js/embed.min.js?3.40.2"></script></p>
<pre><code class="hljs lang-js"><span class="hljs-keyword">let</span> traffic = <span class="hljs-keyword">new</span> Signal(<span class="hljs-string">'stop'</span>)

requestAnimationFrame(<span class="hljs-keyword">async</span> <span class="hljs-function"><span class="hljs-keyword">function</span> <span class="hljs-title">update</span>(<span class="hljs-params">t</span>)</span>{
  <span class="hljs-keyword">await</span> traffic.until(<span class="hljs-string">'pass'</span>)
  block.style.left = <span class="hljs-built_in">parseInt</span>(block.style.left || <span class="hljs-number">50</span>) + <span class="hljs-number">1</span> + <span class="hljs-string">'px'</span>
  requestAnimationFrame(update)
})

button.onclick = e =&gt; {
  traffic.state = button.className = button.className === <span class="hljs-string">'stop'</span> ? <span class="hljs-string">'pass'</span> : <span class="hljs-string">'stop'</span>
}
</code></pre>
<h3>总结</h3>
<p>我们可以用 Signal 来控制异步流程，它最大的作用是将状态和控制分离，我们只需要改变 Signal 的状态，就可以控制异步流程，Signal 支持 until 和 while 谓词，来控制状态的改变。</p>
<p>可以在  上进一步了解关于 Signal 的详细信息。</p>
---------------