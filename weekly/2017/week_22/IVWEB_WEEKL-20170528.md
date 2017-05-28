## 文章索引
1、 <a href="#1智能时代的大前端gmtc2017全球移动技术大会" >智能时代的大前端：GMTC2017全球移动技术大会</a><br/>
2、 <a href="#2server-sent-events-教程" >Server-Sent Events 教程</a><br/>
3、 <a href="#3文章-中国技术开放日欧洲行籍籍无名欧洲it产业" >文章： 中国技术开放日欧洲行：籍籍无名欧洲IT产业</a><br/>
4、 <a href="#4全球236家顶级自动驾驶公司中国仅有滴滴和摩拜上榜" >全球236家顶级自动驾驶公司，中国仅有滴滴和摩拜上榜</a><br/>
5、 <a href="#5微软将所有的windows代码库迁移到git" >微软将所有的Windows代码库迁移到Git</a><br/><h1 id="#title_0" >1、智能时代的大前端：GMTC2017全球移动技术大会</h1>
徐川
[http://www.infoq.com/cn/news/2017/05/gmtc-2017-bj?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/05/gmtc-2017-bj?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>移动端等各种终端设备的兴起，给开发者带来更多的开发挑战，大前端一次开发适配多终端的便捷性让大前端时代的来临变成大势所趋。</p> <i>By 徐川</i>
---------------
<h1 id="#title_1" >2、Server-Sent Events 教程</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2017/05/server-sent_events.html](http://www.ruanyifeng.com/blog/2017/05/server-sent_events.html)
<p>服务器向浏览器推送信息，除了 ，还有一种方法：Server-Sent Events（以下简称 SSE）。本文介绍它的用法。</p>

        <p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017052701.png" alt="" title="" /></p>

<h2>一、SSE 的本质</h2>

<p>严格地说，无法做到服务器主动推送信息。但是，有一种变通方法，就是服务器向客户端声明，接下来要发送的是流信息（streaming）。</p>

<p>也就是说，发送的不是一次性的数据包，而是一个数据流，会连续不断地发送过来。这时，客户端不会关闭连接，会一直等着服务器发过来的新的数据流，视频播放就是这样的例子。本质上，这种通信就是以流信息的方式，完成一次用时很长的下载。</p>

<p>SSE 就是利用这种机制，使用流信息向浏览器推送信息。它基于 HTTP 协议，目前除了 IE/Edge，其他浏览器都支持。</p>

<h2>二、SSE 的特点</h2>

<p>SSE 与 WebSocket 作用相似，都是建立浏览器与服务器之间的通信渠道，然后服务器向浏览器推送信息。</p>

<p>总体来说，WebSocket 更强大和灵活。因为它是全双工通道，可以双向通信；SSE 是单向通道，只能服务器向浏览器发送，因为流信息本质上就是下载。如果浏览器向服务器发送信息，就变成了另一次 HTTP 请求。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017052702.jpg" alt="" title="" /></p>

<p>但是，SSE 也有自己的优点。</p>

<blockquote>
  <ul>
<li>SSE 使用 HTTP 协议，现有的服务器软件都支持。WebSocket 是一个独立协议。</li>
<li>SSE 属于轻量级，使用简单；WebSocket 协议相对复杂。</li>
<li>SSE 默认支持断线重连，WebSocket 需要自己实现。</li>
<li>SSE 一般只用来传送文本，二进制数据需要编码后传送，WebSocket 默认支持传送二进制数据。</li>
<li>SSE 支持自定义发送的消息类型。</li>
</ul>
</blockquote>

<p>因此，两者各有特点，适合不同的场合。</p>

<h2>三、客户端 API</h2>

<h3>3.1 EventSource 对象</h3>

<p>SSE 的客户端 API 部署在<code>EventSource</code>对象上。下面的代码可以检测浏览器是否支持 SSE。</p>

<blockquote><pre><code class="language-javascript">
if ('EventSource' in window) {
  // ...
}
</code></pre></blockquote>

<p>使用 SSE 时，浏览器首先生成一个<code>EventSource</code>实例，向服务器发起连接。</p>

<blockquote><pre><code class="language-javascript">
var source = new EventSource(url);
</code></pre></blockquote>

<p>上面的<code>url</code>可以与当前网址同域，也可以跨域。跨域时，可以指定第二个参数，打开<code>withCredentials</code>属性，表示是否一起发送 Cookie。</p>

<blockquote><pre><code class="language-javascript">
var source = new EventSource(url, { withCredentials: true });
</code></pre></blockquote>

<p><code>EventSource</code>实例的<code>readyState</code>属性，表明连接的当前状态。该属性只读，可以取以下值。</p>

<blockquote>
  <ul>
<li>0：相当于常量<code>EventSource.CONNECTING</code>，表示连接还未建立，或者断线正在重连。</li>
<li>1：相当于常量<code>EventSource.OPEN</code>，表示连接已经建立，可以接受数据。</li>
<li>2：相当于常量<code>EventSource.CLOSED</code>，表示连接已断，且不会重连。</li>
</ul>
</blockquote>

<h3>3.2 基本用法</h3>

<p>连接一旦建立，就会触发<code>open</code>事件，可以在<code>onopen</code>属性定义回调函数。</p>

<blockquote><pre><code class="language-javascript">
source.onopen = function (event) {
  // ...
};

// 另一种写法
source.addEventListener('open', function (event) {
  // ...
}, false);
</code></pre></blockquote>

<p>客户端收到服务器发来的数据，就会触发<code>message</code>事件，可以在<code>onmessage</code>属性的回调函数。</p>

<blockquote><pre><code class="language-javascript">
source.onmessage = function (event) {
  var data = event.data;
  // handle message
};

// 另一种写法
source.addEventListener('message', function (event) {
  var data = event.data;
  // handle message
}, false);
</code></pre></blockquote>

<p>上面代码中，事件对象的<code>data</code>属性就是服务器端传回的数据（文本格式）。</p>

<p>如果发生通信错误（比如连接中断），就会触发<code>error</code>事件，可以在<code>onerror</code>属性定义回调函数。</p>

<blockquote><pre><code class="language-javascript">
source.onerror = function (event) {
  // handle error event
};

// 另一种写法
source.addEventListener('error', function (event) {
  // handle error event
}, false);
</code></pre></blockquote>

<p><code>close</code>方法用于关闭 SSE 连接。</p>

<blockquote><pre><code class="language-javascript">
source.close();
</code></pre></blockquote>

<h3>3.3 自定义事件</h3>

<p>默认情况下，服务器发来的数据，总是触发浏览器<code>EventSource</code>实例的<code>message</code>事件。开发者还可以自定义 SSE 事件，这种情况下，发送回来的数据不会触发<code>message</code>事件。</p>

<blockquote><pre><code class="language-javascript">
source.addEventListener('foo', function (event) {
  var data = event.data;
  // handle message
}, false);
</code></pre></blockquote>

<p>上面代码中，浏览器对 SSE 的<code>foo</code>事件进行监听。如何实现服务器发送<code>foo</code>事件，请看下文。</p>

<h2>四、服务器实现</h2>

<h3>4.1 数据格式</h3>

<p>服务器向浏览器发送的 SSE 数据，必须是 UTF-8 编码的文本，具有如下的 HTTP 头信息。</p>

<blockquote><pre><code class="language-markup">
Content-Type: text/event-stream
Cache-Control: no-cache
Connection: keep-alive
</code></pre></blockquote>

<p>上面三行之中，第一行的<code>Content-Type</code>必须指定 MIME 类型为<code>event-steam</code>。</p>

<p>每一次发送的信息，由若干个<code>message</code>组成，每个<code>message</code>之间用<code>\n\n</code>分隔。每个<code>message</code>内部由若干行组成，每一行都是如下格式。</p>

<blockquote><pre><code class="language-markup">
[field]: value\n
</code></pre></blockquote>

<p>上面的<code>field</code>可以取四个值。</p>

<blockquote>
  <ul>
<li>data</li>
<li>event</li>
<li>id</li>
<li>retry</li>
</ul>
</blockquote>

<p>此外，还可以有冒号开头的行，表示注释。通常，服务器每隔一段时间就会向浏览器发送一个注释，保持连接不中断。</p>

<blockquote><pre><code class="language-markup">
: This is a comment
</code></pre></blockquote>

<p>下面是一个例子。</p>

<blockquote><pre><code class="language-markup">
: this is a test stream\n\n

data: some text\n\n

data: another message\n
data: with two lines \n\n
</code></pre></blockquote>

<h3>4.2 data 字段</h3>

<p>数据内容用<code>data</code>字段表示。</p>

<blockquote><pre><code class="language-markup">
data:  message\n\n
</code></pre></blockquote>

<p>如果数据很长，可以分成多行，最后一行用<code>\n\n</code>结尾，前面行都用<code>\n</code>结尾。</p>

<blockquote><pre><code class="language-markup">
data: begin message\n
data: continue message\n\n
</code></pre></blockquote>

<p>下面是一个发送 JSON 数据的例子。</p>

<blockquote><pre><code class="language-markup">
data: {\n
data: "foo": "bar",\n
data: "baz", 555\n
data: }\n\n
</code></pre></blockquote>

<h3>4.3 id 字段</h3>

<p>数据标识符用<code>id</code>字段表示，相当于每一条数据的编号。</p>

<blockquote><pre><code class="language-markup">
id: msg1\n
data: message\n\n
</code></pre></blockquote>

<p>浏览器用<code>lastEventId</code>属性读取这个值。一旦连接断线，浏览器会发送一个 HTTP 头，里面包含一个特殊的<code>Last-Event-ID</code>头信息，将这个值发送回来，用来帮助服务器端重建连接。因此，这个头信息可以被视为一种同步机制。</p>

<h3>4.4 event 字段</h3>

<p><code>event</code>字段表示自定义的事件类型，默认是<code>message</code>事件。浏览器可以用<code>addEventListener()</code>监听该事件。</p>

<blockquote><pre><code class="language-markup">
event: foo\n
data: a foo event\n\n

data: an unnamed event\n\n

event: bar\n
data: a bar event\n\n
</code></pre></blockquote>

<p>上面的代码创造了三条信息。第一条的名字是<code>foo</code>，触发浏览器的<code>foo</code>事件；第二条未取名，表示默认类型，触发浏览器的<code>message</code>事件；第三条是<code>bar</code>，触发浏览器的<code>bar</code>事件。</p>

<p>下面是另一个例子。</p>

<blockquote><pre><code class="language-markup">
event: userconnect
data: {"username": "bobby", "time": "02:33:48"}

event: usermessage
data: {"username": "bobby", "time": "02:34:11", "text": "Hi everyone."}

event: userdisconnect
data: {"username": "bobby", "time": "02:34:23"}

event: usermessage
data: {"username": "sean", "time": "02:34:36", "text": "Bye, bobby."}
</code></pre></blockquote>

<h3>4.5 retry 字段</h3>

<p>服务器可以用<code>retry</code>字段，指定浏览器重新发起连接的时间间隔。</p>

<blockquote><pre><code class="language-markup">
retry: 10000\n
</code></pre></blockquote>

<p>两种情况会导致浏览器重新发起连接：一种是时间间隔到期，二是由于网络错误等原因，导致连接出错。</p>

<h2>五、Node 服务器实例</h2>

<p>SSE 要求服务器与浏览器保持连接。对于不同的服务器软件来说，所消耗的资源是不一样的。Apache 服务器，每个连接就是一个线程，如果要维持大量连接，势必要消耗大量资源。Node 则是所有连接都使用同一个线程，因此消耗的资源会小得多，但是这要求每个连接不能包含很耗时的操作，比如磁盘的 IO 读写。</p>

<p>下面是 Node 的 SSE 服务器。</p>

<blockquote><pre><code class="language-javascript">
var http = require("http");

http.createServer(function (req, res) {
  var fileName = "." + req.url;

  if (fileName === "./stream") {
    res.writeHead(200, {
      "Content-Type":"text/event-stream",
      "Cache-Control":"no-cache",
      "Connection":"keep-alive",
      "Access-Control-Allow-Origin": '*',
    });
    res.write("retry: 10000\n");
    res.write("event: connecttime\n");
    res.write("data: " + (new Date()) + "\n\n");
    res.write("data: " + (new Date()) + "\n\n");

    interval = setInterval(function () {
      res.write("data: " + (new Date()) + "\n\n");
    }, 1000);

    req.connection.addListener("close", function () {
      clearInterval(interval);
    }, false);
  }
}).listen(8844, "127.0.0.1");
</code></pre></blockquote>

<p>请将上面的代码保存为<code>server.js</code>，然后执行下面的命令。</p>

<blockquote><pre><code class="language-bash">
$ node server.js
</code></pre></blockquote>

<p>上面的命令会在本机的<code>8844</code>端口，打开一个 HTTP 服务。</p>

<p>然后，打开这个，查看客户端代码并运行。</p>

<h2>六、参考链接</h2>

<ul>
<li>Colin Ihrig, </li>
<li>Colin Ihrig，</li>
<li>Eric Bidelman, </li>
<li>MDN，</li>
<li>Segment.io, </li>
</ul>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2017-05-27T15:49:29+08:00">2017年5月27日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>博客文集：</li>
<li>社交媒体：</li>
<li>Feed订阅： </li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------
<h1 id="#title_2" >3、文章： 中国技术开放日欧洲行：籍籍无名欧洲IT产业</h1>
徐吟乐, 陈连平
[http://www.infoq.com/cn/articles/unknown-UN-IT?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/unknown-UN-IT?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/unknown-UN-IT/zh/smallimage/GettyImages-465290867-copy.jpg"/><p>如果说在硅谷，IT 业代表着商业化；在日本，IT 业跟制造业紧密相连；那么在欧洲，IT 业又是一个怎样的状态？这是一篇也许不那么严谨的科普文，却可以带你管中窥豹地看看，欧洲 IT 业是什么样的画风。</p> <i>By 徐吟乐</i>
---------------
<h1 id="#title_3" >4、全球236家顶级自动驾驶公司，中国仅有滴滴和摩拜上榜</h1>
Jack Stewart
[http://www.infoq.com/cn/news/2017/05/world-top-236-autodrive-didi-mob?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/05/world-top-236-autodrive-didi-mob?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>全球236家顶级自动驾驶公司，中国仅有滴滴和摩拜上榜</p> <i>By Jack Stewart</i>
---------------
<h1 id="#title_4" >5、微软将所有的Windows代码库迁移到Git</h1>
Abel Avram
[http://www.infoq.com/cn/news/2017/05/microsoft-windows-git?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/05/microsoft-windows-git?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>微软将所有的Windows代码从Source Depot迁移到基于GVFS的Git上。</p> <i>By Abel Avram</i> <i> Translated by 薛命灯</i>
---------------