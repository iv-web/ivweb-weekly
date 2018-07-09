## 文章索引
1、 <a href="#1web-worker-使用教程" >Web Worker 使用教程</a><br/>
2、 <a href="#2文章-红帽技术开放日参与开源社区不只有贡献代码这一种方式" >文章： 红帽技术开放日：参与开源社区不只有贡献代码这一种方式</a><br/>
3、 <a href="#3文章-ballerina微服务编程语言最新发布版本与ballerina-central简介" >文章： Ballerina微服务编程语言：最新发布版本与“Ballerina Central”简介</a><br/>
4、 <a href="#4迷你书-架构师2018年7月" >迷你书： 架构师（2018年7月）</a><br/><h1 id="#title_0" >1、Web Worker 使用教程</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2018/07/web-worker.html](http://www.ruanyifeng.com/blog/2018/07/web-worker.html)
<h2>一、概述</h2>

        <p>JavaScript 语言采用的是单线程模型，也就是说，所有任务只能在一个线程上完成，一次只能做一件事。前面的任务没做完，后面的任务只能等着。随着电脑计算能力的增强，尤其是多核 CPU 的出现，单线程带来很大的不便，无法充分发挥计算机的计算能力。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018070801.png" alt="" title="" /></p>

<p>Web Worker 的作用，就是为 JavaScript 创造多线程环境，允许主线程创建 Worker 线程，将一些任务分配给后者运行。在主线程运行的同时，Worker 线程在后台运行，两者互不干扰。等到 Worker 线程完成计算任务，再把结果返回给主线程。这样的好处是，一些计算密集型或高延迟的任务，被 Worker 线程负担了，主线程（通常负责 UI 交互）就会很流畅，不会被阻塞或拖慢。</p>

<p>Worker 线程一旦新建成功，就会始终运行，不会被主线程上的活动（比如用户点击按钮、提交表单）打断。这样有利于随时响应主线程的通信。但是，这也造成了 Worker 比较耗费资源，不应该过度使用，而且一旦使用完毕，就应该关闭。</p>

<p>Web Worker 有以下几个使用注意点。</p>

<p>（1）<strong>同源限制</strong></p>

<p>分配给 Worker 线程运行的脚本文件，必须与主线程的脚本文件同源。</p>

<p>（2）<strong>DOM 限制</strong></p>

<p>Worker 线程所在的全局对象，与主线程不一样，无法读取主线程所在网页的 DOM 对象，也无法使用<code>document</code>、<code>window</code>、<code>parent</code>这些对象。但是，Worker 线程可以<code>navigator</code>对象和<code>location</code>对象。</p>

<p>（3）<strong>通信联系</strong></p>

<p>Worker 线程和主线程不在同一个上下文环境，它们不能直接通信，必须通过消息完成。</p>

<p>（4）<strong>脚本限制</strong></p>

<p>Worker 线程不能执行<code>alert()</code>方法和<code>confirm()</code>方法，但可以使用 XMLHttpRequest 对象发出 AJAX 请求。</p>

<p>（5）<strong>文件限制</strong></p>

<p>Worker 线程无法读取本地文件，即不能打开本机的文件系统（<code>file://</code>），它所加载的脚本，必须来自网络。</p>

<h2>二、基本用法</h2>

<h3>2.1 主线程</h3>

<p>主线程采用<code>new</code>命令，调用<code>Worker()</code>构造函数，新建一个 Worker 线程。</p>

<blockquote><pre><code class="language-javascript">
var worker = new Worker('work.js');
</code></pre></blockquote>

<p><code>Worker()</code>构造函数的参数是一个脚本文件，该文件就是 Worker 线程所要执行的任务。由于 Worker 不能读取本地文件，所以这个脚本必须来自网络。如果下载没有成功（比如404错误），Worker 就会默默地失败。</p>

<p>然后，主线程调用<code>worker.postMessage()</code>方法，向 Worker 发消息。</p>

<blockquote><pre><code class="language-javascript">
worker.postMessage('Hello World');
worker.postMessage({method: 'echo', args: ['Work']});
</code></pre></blockquote>

<p><code>worker.postMessage()</code>方法的参数，就是主线程传给 Worker 的数据。它可以是各种数据类型，包括二进制数据。</p>

<p>接着，主线程通过<code>worker.onmessage</code>指定监听函数，接收子线程发回来的消息。</p>

<blockquote><pre><code class="language-javascript">
worker.onmessage = function (event) {
  console.log('Received message ' + event.data);
  doSomething();
}

function doSomething() {
  // 执行任务
  worker.postMessage('Work done!');
}
</code></pre></blockquote>

<p>上面代码中，事件对象的<code>data</code>属性可以获取 Worker 发来的数据。</p>

<p>Worker 完成任务以后，主线程就可以把它关掉。</p>

<blockquote><pre><code class="language-javascript">
worker.terminate();
</code></pre></blockquote>

<h3>2.2 Worker 线程</h3>

<p>Worker 线程内部需要有一个监听函数，监听<code>message</code>事件。</p>

<blockquote><pre><code class="language-javascript">
self.addEventListener('message', function (e) {
  self.postMessage('You said: ' + e.data);
}, false);
</code></pre></blockquote>

<p>上面代码中，<code>self</code>代表子线程自身，即子线程的全局对象。因此，等同于下面两种写法。</p>

<blockquote><pre><code class="language-javascript">
// 写法一
this.addEventListener('message', function (e) {
  this.postMessage('You said: ' + e.data);
}, false);

// 写法二
addEventListener('message', function (e) {
  postMessage('You said: ' + e.data);
}, false);
</code></pre></blockquote>

<p>除了使用<code>self.addEventListener()</code>指定监听函数，也可以使用<code>self.onmessage</code>指定。监听函数的参数是一个事件对象，它的<code>data</code>属性包含主线程发来的数据。<code>self.postMessage()</code>方法用来向主线程发送消息。</p>

<p>根据主线程发来的数据，Worker 线程可以调用不同的方法，下面是一个例子。</p>

<blockquote><pre><code class="language-javascript">
self.addEventListener('message', function (e) {
  var data = e.data;
  switch (data.cmd) {
    case 'start':
      self.postMessage('WORKER STARTED: ' + data.msg);
      break;
    case 'stop':
      self.postMessage('WORKER STOPPED: ' + data.msg);
      self.close(); // Terminates the worker.
      break;
    default:
      self.postMessage('Unknown command: ' + data.msg);
  };
}, false);
</code></pre></blockquote>

<p>上面代码中，<code>self.close()</code>用于在 Worker 内部关闭自身。</p>

<h3>2.3 Worker 加载脚本</h3>

<p>Worker 内部如果要加载其他脚本，有一个专门的方法<code>importScripts()</code>。</p>

<blockquote><pre><code class="language-javascript">
importScripts('script1.js');
</code></pre></blockquote>

<p>该方法可以同时加载多个脚本。</p>

<blockquote><pre><code class="language-javascript">
importScripts('script1.js', 'script2.js');
</code></pre></blockquote>

<h3>2.4 错误处理</h3>

<p>主线程可以监听 Worker 是否发生错误。如果发生错误，Worker 会触发主线程的<code>error</code>事件。</p>

<blockquote><pre><code class="language-javascript">
worker.onerror(function (event) {
  console.log([
    'ERROR: Line ', e.lineno, ' in ', e.filename, ': ', e.message
  ].join(''));
});

// 或者
worker.addEventListener('error', function (event) {
  // ...
});
</code></pre></blockquote>

<p>Worker 内部也可以监听<code>error</code>事件。</p>

<h3>2.5 关闭 Worker</h3>

<p>使用完毕，为了节省系统资源，必须关闭 Worker。</p>

<blockquote><pre><code class="language-javascript">
// 主线程
worker.terminate();

// Worker 线程
self.close();
</code></pre></blockquote>

<h2>三、数据通信</h2>

<p>前面说过，主线程与 Worker 之间的通信内容，可以是文本，也可以是对象。需要注意的是，这种通信是拷贝关系，即是传值而不是传址，Worker 对通信内容的修改，不会影响到主线程。事实上，浏览器内部的运行机制是，先将通信内容串行化，然后把串行化后的字符串发给 Worker，后者再将它还原。</p>

<p>主线程与 Worker 之间也可以交换二进制数据，比如 File、Blob、ArrayBuffer 等类型，也可以在线程之间发送。下面是一个例子。</p>

<blockquote><pre><code class="language-javascript">
// 主线程
var uInt8Array = new Uint8Array(new ArrayBuffer(10));
for (var i = 0; i &lt; uInt8Array.length; ++i) {
  uInt8Array[i] = i * 2; // [0, 2, 4, 6, 8,...]
}
worker.postMessage(uInt8Array);

// Worker 线程
self.onmessage = function (e) {
  var uInt8Array = e.data;
  postMessage('Inside worker.js: uInt8Array.toString() = ' + uInt8Array.toString());
  postMessage('Inside worker.js: uInt8Array.byteLength = ' + uInt8Array.byteLength);
};
</code></pre></blockquote>

<p>但是，拷贝方式发送二进制数据，会造成性能问题。比如，主线程向 Worker 发送一个 500MB 文件，默认情况下浏览器会生成一个原文件的拷贝。为了解决这个问题，JavaScript 允许主线程把二进制数据直接转移给子线程，但是一旦转移，主线程就无法再使用这些二进制数据了，这是为了防止出现多个线程同时修改数据的麻烦局面。这种转移数据的方法，叫做。这使得主线程可以快速把数据交给 Worker，对于影像处理、声音处理、3D 运算等就非常方便了，不会产生性能负担。</p>

<p>如果要直接转移数据的控制权，就要使用下面的写法。</p>

<blockquote><pre><code class="language-javascript">
// Transferable Objects 格式
worker.postMessage(arrayBuffer, [arrayBuffer]);

// 例子
var ab = new ArrayBuffer(1);
worker.postMessage(ab, [ab]);
</code></pre></blockquote>

<h2>四、同页面的 Web Worker</h2>

<p>通常情况下，Worker 载入的是一个单独的 JavaScript 脚本文件，但是也可以载入与主线程在同一个网页的代码。</p>

<blockquote><pre><code class="language-markup">
&lt;!DOCTYPE html>
  &lt;body>
    &lt;script id="worker" type="app/worker">
      addEventListener('message', function () {
        postMessage('some message');
      }, false);
    &lt;/script>
  &lt;/body>
&lt;/html>
</code></pre></blockquote>

<p>上面是一段嵌入网页的脚本，注意必须指定<code>&lt;script&gt;</code>标签的<code>type</code>属性是一个浏览器不认识的值，上例是<code>app/worker</code>。</p>

<p>然后，读取这一段嵌入页面的脚本，用 Worker 来处理。</p>

<blockquote><pre><code class="language-javascript">
var blob = new Blob([document.querySelector('#worker').textContent]);
var url = window.URL.createObjectURL(blob);
var worker = new Worker(url);

worker.onmessage = function (e) {
  // e.data === 'some message'
};
</code></pre></blockquote>

<p>上面代码中，先将嵌入网页的脚本代码，转成一个二进制对象，然后为这个二进制对象生成 URL，再让 Worker 加载这个 URL。这样就做到了，主线程和 Worker 的代码都在同一个网页上面。</p>

<h2>五、实例：Worker 线程完成轮询</h2>

<p>有时，浏览器需要轮询服务器状态，以便第一时间得知状态改变。这个工作可以放在 Worker 里面。</p>

<blockquote><pre><code class="language-javascript">
function createWorker(f) {
  var blob = new Blob([f.toString()]);
  var url = window.URL.createObjectURL(blob);
  var worker = new Worker(url);
  return worker;
}

var pollingWorker = createWorker(function (e) {
  var cache;

  function compare(new, old) { ... };

  setInterval(function () {
    fetch('/my-api-endpoint').then(function (res) {
      var data = res.json();

      if (!compare(data, cache)) {
        cache = data;
        self.postMessage(data);
      }
    })
  }, 1000)
});

pollingWorker.onmessage = function () {
  // render data
}

pollingWorker.postMessage('init');
</code></pre></blockquote>

<p>上面代码中，Worker 每秒钟轮询一次数据，然后跟缓存做比较。如果不一致，就说明服务端有了新的变化，因此就要通知主线程。</p>

<h2>六、实例： Worker 新建 Worker</h2>

<p>Worker 线程内部还能再新建 Worker 线程。下面的例子是将一个计算密集的任务，分配到10个 Worker。</p>

<p>主线程代码如下。</p>

<blockquote><pre><code class="language-javascript">
var worker = new Worker('worker.js');
worker.onmessage = function (event) {
  document.getElementById('result').textContent = event.data;
};
</code></pre></blockquote>

<p>Worker 线程代码如下。</p>

<blockquote><pre><code class="language-javascript">
// worker.js

// settings
var num_workers = 10;
var items_per_worker = 1000000;

// start the workers
var result = 0;
var pending_workers = num_workers;
for (var i = 0; i &lt; num_workers; i += 1) {
  var worker = new Worker('core.js');
  worker.postMessage(i * items_per_worker);
  worker.postMessage((i + 1) * items_per_worker);
  worker.onmessage = storeResult;
}

// handle the results
function storeResult(event) {
  result += event.data;
  pending_workers -= 1;
  if (pending_workers &lt;= 0)
    postMessage(result); // finished!
}
</code></pre></blockquote>

<p>上面代码中，Worker 线程内部新建了10个 Worker 线程，并且依次向这10个 Worker 发送消息，告知了计算的起点和终点。计算任务脚本的代码如下。</p>

<blockquote><pre><code class="language-javascript">
// core.js
var start;
onmessage = getStart;
function getStart(event) {
  start = event.data;
  onmessage = getEnd;
}

var end;
function getEnd(event) {
  end = event.data;
  onmessage = null;
  work();
}

function work() {
  var result = 0;
  for (var i = start; i &lt; end; i += 1) {
    // perform some complex calculation here
    result += 1;
  }
  postMessage(result);
  close();
}
</code></pre></blockquote>

<h2>七、API</h2>

<h3>7.1 主线程</h3>

<p>浏览器原生提供<code>Worker()</code>构造函数，用来供主线程生成 Worker 线程。</p>

<blockquote><pre><code class="language-javascript">
var myWorker = new Worker(jsUrl, options);
</code></pre></blockquote>

<p><code>Worker()</code>构造函数，可以接受两个参数。第一个参数是脚本的网址（必须遵守同源政策），该参数是必需的，且只能加载 JS 脚本，否则会报错。第二个参数是配置对象，该对象可选。它的一个作用就是指定 Worker 的名称，用来区分多个 Worker 线程。</p>

<blockquote><pre><code class="language-javascript">
// 主线程
var myWorker = new Worker('worker.js', { name : 'myWorker' });

// Worker 线程
self.name // myWorker
</code></pre></blockquote>

<p><code>Worker()</code>构造函数返回一个 Worker 线程对象，用来供主线程操作 Worker。Worker 线程对象的属性和方法如下。</p>

<blockquote>
  <ul>
<li>Worker.onerror：指定 error 事件的监听函数。</li>
<li>Worker.onmessage：指定 message 事件的监听函数，发送过来的数据在<code>Event.data</code>属性中。</li>
<li>Worker.onmessageerror：指定 messageerror 事件的监听函数。发送的数据无法序列化成字符串时，会触发这个事件。</li>
<li>Worker.postMessage()：向 Worker 线程发送消息。</li>
<li>Worker.terminate()：立即终止 Worker 线程。</li>
</ul>
</blockquote>

<h3>7.2 Worker 线程</h3>

<p>Web Worker 有自己的全局对象，不是主线程的<code>window</code>，而是一个专门为 Worker 定制的全局对象。因此定义在<code>window</code>上面的对象和方法不是全部都可以使用。</p>

<p>Worker 线程有一些自己的全局属性和方法。</p>

<blockquote>
  <ul>
<li>self.name： Worker 的名字。该属性只读，由构造函数指定。</li>
<li>self.onmessage：指定<code>message</code>事件的监听函数。</li>
<li>self.onmessageerror：指定 messageerror 事件的监听函数。发送的数据无法序列化成字符串时，会触发这个事件。</li>
<li>self.close()：关闭 Worker 线程。</li>
<li>self.postMessage()：向产生这个 Worker 线程发送消息。</li>
<li>self.importScripts()：加载 JS 脚本。</li>
</ul>
</blockquote>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2018-07-08T20:59:46+08:00">2018年7月 8日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>文集：</li>
<li>社交媒体：</li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------
<h1 id="#title_1" >2、文章： 红帽技术开放日：参与开源社区不只有贡献代码这一种方式</h1>
张婵
[http://www.infoq.com/cn/articles/redhat-tech-open-day?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/redhat-tech-open-day?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/redhat-tech-open-day/zh/smallimage/logo-1522948961955-1530984248302.jpeg"/><p>红帽（Red Hat) 是全球最大的开源软件公司，今年是红帽建立 25 周年，适逢 LC3 大会在北京举办，6 月 28 日和 29 日红帽举办了开源社区开放日和媒体交流会，和大家分享红帽的最新消息，并探讨了如何建设开源社区让更多人参与开源。</p> <i>By 张婵</i>
---------------
<h1 id="#title_2" >3、文章： Ballerina微服务编程语言：最新发布版本与“Ballerina Central”简介</h1>
Tyler Jewell
[http://www.infoq.com/cn/articles/ballerina-microservices-language-part-1?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/ballerina-microservices-language-part-1?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/ballerina-microservices-language-part-1/zh/smallimage/ballerina-1527427668312-1530980292978.jpeg"/><p>该教程阐述了Ballerina，这是一个新的编程语言和平台，它的目标在于让创建具有弹性的服务变得更加容易，这些服务会跨分布式端点进行集成和编排。针对分布式系统的基本原语，Ballerina使用编译期抽象让编译器生成制件，如部署到Docker和Kubernetes API上所需的网关。</p> <i>By Tyler Jewell</i> <i> Translated by 张卫滨 </i>
---------------
<h1 id="#title_3" >4、迷你书： 架构师（2018年7月）</h1>
InfoQ中文站
[http://www.infoq.com/cn/minibooks/architect-201807?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/minibooks/architect-201807?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/minibooks/architect-201807/zh/smallimage/100-1530785320414.jpg"/><p>本期主要内容：Spark团队开源新作：全流程机器学习平台MLflow；Google发布Flutter Release Preview 1；独家揭秘：腾讯千亿级参数分布式机器学习系统无量背后的技术门道；阿里巴巴为什么不用 ZooKeeper 做服务发现？</p> <i>By InfoQ中文站</i>
---------------