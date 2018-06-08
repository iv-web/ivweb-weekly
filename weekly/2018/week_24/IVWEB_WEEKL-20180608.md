## 文章索引
1、 <a href="#1keeping-nodejs-fast:-tools-techniques-and-tips-for-making-high-performance-nodejs-servers" >Keeping Node.js Fast: Tools, Techniques, And Tips For Making High-Performance Node.js Servers</a><br/>
2、 <a href="#2我对react-native的那些执念" >我对React Native的那些执念</a><br/>
3、 <a href="#3文章-netflix:当你按下播放的时候发生了什么" >文章： Netflix:当你按下“播放”的时候发生了什么？</a><br/>
4、 <a href="#4文章-携程apollo配置中心架构深度剖析" >文章： 携程Apollo配置中心架构深度剖析</a><br/>
5、 <a href="#5视频演讲-oppo-redis-cluster技术实践" >视频演讲： OPPO Redis Cluster技术实践</a><br/>
6、 <a href="#6文章-devsecops的三种解读" >文章： DevSecOps的三种解读</a><br/>
7、 <a href="#7极限编程创始人ron-jeffries建议开发者放弃敏捷" >极限编程创始人Ron Jeffries建议开发者放弃敏捷</a><br/>
8、 <a href="#8oracle在开源mission-control后将其开发团队解散" >Oracle在开源Mission Control后将其开发团队解散</a><br/>
9、 <a href="#9typescript-29发布更新了对esnext的支持" >TypeScript 2.9发布，更新了对ES.Next的支持</a><br/>
10、 <a href="#10zip-slip目录遍历漏洞已影响多个java项目" >Zip Slip目录遍历漏洞已影响多个Java项目</a><br/>
11、 <a href="#11you-probably-dont-need-derived-state" >You Probably Don't Need Derived State</a><br/><h1 id="#title_0" >1、Keeping Node.js Fast: Tools, Techniques, And Tips For Making High-Performance Node.js Servers</h1>
David Mark Clements
[https://www.smashingmagazine.com/2018/06/nodejs-tools-techniques-performance-servers/](https://www.smashingmagazine.com/2018/06/nodejs-tools-techniques-performance-servers/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/06/nodejs-tools-techniques-performance-servers/" />
              <title>Keeping Node.js Fast: Tools, Techniques, And Tips For Making High-Performance Node.js Servers</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>Keeping Node.js Fast: Tools, Techniques, And Tips For Making High-Performance Node.js Servers</h1>
                  
                    
                    <address>David Mark Clements</address>
                  
                  <time datetime="2018-06-07T13:45:51&#43;02:00" class="op-published">2018-06-07T13:45:51+02:00</time>
                  <time datetime="2018-06-07T20:00:03&#43;00:00" class="op-modified">2018-06-07T20:00:03+00:00</time>
                </header>
                

<p>If you’ve been building anything with Node.js for long enough, then you’ve no doubt experienced the pain of unexpected speed issues. JavaScript is an evented, asynchronous language. That can make reasoning about performance <em>tricky</em>, as will become apparent. The surging popularity of Node.js has exposed the need for tooling, techniques and thinking suited to the constraints of server-side JavaScript.</p>

<p>When it comes to performance, what works in the browser doesn’t necessarily suit Node.js.  So, how do we make sure a Node.js implementation is fast and fit for purpose? Let’s walk through a hands-on example.</p>

<h3 id="tools">Tools</h3>

<p>Node is a very versatile platform, but one of the predominant applications is creating networked processes. We’re going to focus on profiling the most common of these: HTTP web servers.</p>

<p>We’ll need a tool that can blast a server with lots of requests while measuring the performance. For example, we can use :</p>

<pre><code class="language-bash">npm install -g autocannon
</code></pre>

<p>Other good HTTP benchmarking tools include , but AutoCannon is written in Node, provides similar (or sometimes greater) load pressure, and is very easy to install on Windows, Linux, and Mac OS X.</p>



<aside class="product-panel product-panel__tilted product-panel--book" data-audience="non-subscriber">
    <div class="container product-panel--book__container">
      <div class="panel__description panel__description--book">
    <p>Nope, we can't do any magic tricks, but we have articles,  get a seasoned selection of magic front-end tricks — e.g. <strong>live designing sessions</strong> and perf audits, too. <em>Just sayin'</em>! ;-)</p>

      <a href="http://smashed.by/perfpanelmembership" class="btn btn--green btn--large">
        Explore Smashing Wizardry&nbsp;→
      </a>
      </div>
      <div class="panel__image panel__image--book">
        <a href="http://smashed.by/perfpanelmembership" class="books__book__image">
        <div class="books__book__img">
          <img src="https://www.smashingmagazine.com/images/smashing-cat/cat-wizard.svg" alt="Smashing Cat, just preparing to do some magic stuff." width="310" height="400">
        </div>
      </a>
      </div>
    </div>
  </aside>





<div class="c-garfield-the-cat">


<p>After we’ve established a baseline performance measurement, if we decide our process could be faster we’ll need some way to diagnose problems with the process. A great tool for diagnosing various performance issues is , which can also be installed with npm:</p>

<pre><code class="language-bash">npm --install -g clinic
</code></pre>

<p>This actually installs a suite of tools. We’ll be using ) as we go.</p>

<p><strong>Note</strong>: <em>For this hands-on example we’ll need Node 8.11.2 or higher.</em></p>

<h3 id="the-code">The Code</h3>

<p>Our example case is a simple REST server with a single resource: a large JSON payload exposed as a GET route at <code>/seed/v1</code>. The server is an <code>app</code> folder which consists of a <em>package.json</em> file (depending on <code>restify 7.1.0</code>), an <em>index.js</em> file and a <em>util.js</em> file.</p>

<p>The <em>index.js</em> file for our server looks like so:</p>

<pre><code class="language-javascript">'use strict'

const restify = require('restify')
const { etagger, timestamp, fetchContent } = require('./util')()
const server = restify.createServer()

server.use(etagger().bind(server))

server.get('/seed/v1', function (req, res, next) {
  fetchContent(req.url, (err, content) => {
    if (err) return next(err)
    res.send({data: content, url: req.url, ts: timestamp()})
    next()
  })
})

server.listen(3000)
</code></pre>

<p>This server is representative of the common case of serving client-cached dynamic content. This is achieved with the <code>etagger</code> middleware, which calculates an <code>ETag</code> header for the latest state of the content.</p>

<p>The <em>util.js</em> file provides implementation pieces that would commonly be used in such a scenario, a function to fetch the relevant content from a backend, the etag middleware and a timestamp function that supplies timestamps on a minute-by-minute basis:</p>

<pre class="break-out"><code class="language-javascript">'use strict'

require('events').defaultMaxListeners = Infinity
const crypto = require('crypto')

module.exports = () => {
  const content = crypto.rng(5000).toString('hex')
  const ONE_MINUTE = 60000
  var last = Date.now()

  function timestamp () {
    var now = Date.now()
    if (now &mdash; last >= ONE_MINUTE) last = now
    return last
  }
  
  function etagger () {
    var cache = {}
    var afterEventAttached = false
    function attachAfterEvent (server) {
      if (attachAfterEvent === true) return
      afterEventAttached = true
      server.on('after', (req, res) => {
        if (res.statusCode !== 200) return
        if (!res._body) return
        const key = crypto.createHash('sha512')
          .update(req.url)
          .digest()
          .toString('hex')
        const etag = crypto.createHash('sha512')
          .update(JSON.stringify(res._body))
          .digest()
          .toString('hex')
        if (cache[key] !== etag) cache[key] = etag
      })
    }
    return function (req, res, next) {
      attachAfterEvent(this)
      const key = crypto.createHash('sha512')
        .update(req.url)
        .digest()
        .toString('hex')
      if (key in cache) res.set('Etag', cache[key])
      res.set('Cache-Control', 'public, max-age=120')
      next()
    }
  }

  function fetchContent (url, cb) {
    setImmediate(() => {
      if (url !== '/seed/v1') cb(Object.assign(Error('Not Found'), {statusCode: 404}))
      else cb(null, content)
    })
  }

  return { timestamp, etagger, fetchContent }
  
}
</code></pre>

<p>By no means take this code as an example of best practices! There are multiple code smells in this file, but we’ll locate them as we measure and profile the application.</p>

<p><em>To get the full source for our starting point, the slow server can be found over .</em></p>

<h3 id="profiling">Profiling</h3>

<p>In order to profile, we need two terminals, one for starting the application, and the other for load testing it.</p>

<p>In one terminal, within the <code>app</code>, folder we can run:</p>

<pre><code class="language-bash">node index.js
</code></pre>

<p>In another terminal we can profile it like so:</p>

<pre><code class="language-bash">autocannon -c100 localhost:3000/seed/v1
</code></pre>

<p>This will open 100 concurrent connections and bombard the server with requests for ten seconds.</p>

<p>The results should be something similar to the following (Running 10s test @ <code>http://localhost:3000/seed/v1</code> &mdash; 100 connections):</p>

<p><table class="tablesaw break-out" data-tablesaw-mode="swipe" data-tablesaw-minimap>
    <thead>
        <tr>
            <th data-tablesaw-priority="persist">Stat</th>
            <th>Avg</th>
            <th>Stdev</th>
            <th>Max</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Latency (ms)</td>
            <td>3086.81</td>
            <td>1725.2</td>
            <td>5554</td>
        </tr>
        <tr>
            <td>Req/Sec</td>
            <td>23.1</td>
            <td>19.18</td>
            <td>65</td>
        </tr>
        <tr>
            <td>Bytes/Sec</td>
            <td>237.98 kB</td>
            <td>197.7 kB</td>
            <td>688.13 kB</td>
        </tr>
    </tbody>
</table><figcaption><em>231 requests in 10s, 2.4 MB read</em></figcaption></p>

<p>Results will vary depending on the machine. However, considering that a &ldquo;Hello World&rdquo; Node.js server is easily capable of thirty thousand requests per second on that machine that produced these results, 23 requests per second with an average latency exceeding 3 seconds is dismal.</p>

<h3 id="diagnosing">Diagnosing</h3>

<h4 id="discovering-the-problem-area">Discovering The Problem Area</h4>

<p>We can diagnose the application with a single command, thanks to Clinic Doctor’s &ndash;on-port command. Within the <code>app</code> folder we run:</p>

<pre><code class="language-bash">clinic doctor --on-port=’autocannon -c100 localhost:$PORT/seed/v1’ -- node index.js
</code></pre>

<p>This will create an HTML file that will automatically open in our browser when profiling is complete.</p>

<p>The results should look something like the following:</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/db105d3d-b2d3-4830-9cc8-7486deec7157/keeping-nodejs-fast-fig1.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/db105d3d-b2d3-4830-9cc8-7486deec7157/keeping-nodejs-fast-fig1.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/db105d3d-b2d3-4830-9cc8-7486deec7157/keeping-nodejs-fast-fig1.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/db105d3d-b2d3-4830-9cc8-7486deec7157/keeping-nodejs-fast-fig1.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/db105d3d-b2d3-4830-9cc8-7486deec7157/keeping-nodejs-fast-fig1.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/db105d3d-b2d3-4830-9cc8-7486deec7157/keeping-nodejs-fast-fig1.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/db105d3d-b2d3-4830-9cc8-7486deec7157/keeping-nodejs-fast-fig1.png"
			sizes="100vw"
			alt="Clinic Doctor has detected an Event Loop issue"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Clinic Doctor results
		</figcaption>
	
</figure>


<p>The Doctor is telling us that we have probably had an Event Loop issue.</p>

<p>Along with the message near the top of the UI, we can also see that the Event Loop chart is red, and shows a constantly increasing delay. Before we dig deeper into what this means, let’s first understand the effect the diagnosed issue is having on the other metrics.</p>

<p>We can see the CPU is consistently at or above 100% as the process works hard to process queued requests. Node’s JavaScript engine (V8) actually uses two CPU cores. One for the Event Loop and the other for Garbage Collection. When we see the CPU spiking up to 120% in some cases, the process is collecting objects related to handled requests.</p>


  <div id="sponsors-article" data-impression="true" class="c-promo-box c-promo-box--ad sponsors hidden" data-audience="non-subscriber" data-remove="true"></div>



<p>We see this correlated in the Memory graph. The solid line in the Memory chart is the Heap Used metric. Any time there’s a spike in CPU we see a fall in the Heap Used line, showing that memory is being deallocated.</p>

<p>Active Handles are unaffected by the Event Loop delay. An active handle is an object that represents either I/O (such as a socket or file handle) or a timer (such as a <code>setInterval</code>). We instructed AutoCannon to open 100 connections (<code>-c100</code>). Active handles stay a consistent count of 103. The other three are handles for STDOUT, STDERR, and the handle for the server itself.</p>

<p>If we click the Recommendations panel at the bottom of the screen, we should see something like the following:</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6199a9b8-9a33-40b3-b2d9-8fab98936d0d/keeping-nodejs-fast-fig2.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6199a9b8-9a33-40b3-b2d9-8fab98936d0d/keeping-nodejs-fast-fig2.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6199a9b8-9a33-40b3-b2d9-8fab98936d0d/keeping-nodejs-fast-fig2.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6199a9b8-9a33-40b3-b2d9-8fab98936d0d/keeping-nodejs-fast-fig2.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6199a9b8-9a33-40b3-b2d9-8fab98936d0d/keeping-nodejs-fast-fig2.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6199a9b8-9a33-40b3-b2d9-8fab98936d0d/keeping-nodejs-fast-fig2.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6199a9b8-9a33-40b3-b2d9-8fab98936d0d/keeping-nodejs-fast-fig2.png"
			sizes="100vw"
			alt="Clinic Doctor recommendations panel opened"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Viewing issue specific recommendations
		</figcaption>
	
</figure>


<h4 id="short-term-mitigation">Short-Term Mitigation</h4>

<p>Root cause analysis of serious performance issues can take time. In the case of a live deployed project, it’s worth adding overload protection to servers or services. The idea of overload protection is to monitor event loop delay (among other things), and respond with “503 Service Unavailable” if a threshold is passed. This allows a load balancer to fail over to other instances, or in the worst case means users will have to refresh. The  which provides the same protection.</p>

<h4 id="understanding-the-problem-area">Understanding The Problem Area</h4>

<p>As the short explanation in Clinic Doctor explains, if the Event Loop is delayed to the level that we’re observing it’s very likely that one or more functions are &ldquo;blocking&rdquo; the Event Loop.</p>

<p>It’s especially important with Node.js to recognize this primary JavaScript characteristic: asynchronous events cannot occur until currently executing code has completed.</p>

<p>This is why a <code>setTimeout</code> cannot be precise.</p>

<p>For instance, try running the following in a browser’s DevTools or the Node REPL:</p>

<pre><code class="language-javascript">console.time('timeout')
setTimeout(console.timeEnd, 100, 'timeout')
let n = 1e7
while (n--) Math.random()
</code></pre>

<p>The resulting time measurement will never be 100ms. It will likely be in the range of 150ms to 250ms. The <code>setTimeout</code> scheduled an asynchronous operation (<code>console.timeEnd</code>), but the currently executing code has not yet complete; there are two more lines. The currently executing code is known as the current “tick.” For the tick to complete, <code>Math.random</code> has to be called ten million times. If this takes 100ms, then the total time before the timeout resolves will be 200ms (plus however long it takes the <code>setTimeout</code> function to actually queue the timeout beforehand, usually a couple of milliseconds).</p>

<p>In a server-side context, if an operation in the current tick is taking a long time to complete requests cannot be handled, and data fetching cannot occur because asynchronous code will not be executed until the current tick has completed. This means that computationally expensive code will slow down all interactions with the server. So it’s recommended to split out resource intense work into separate processes and call them from the main server, this will avoid cases where on rarely used but expensive route slows down the performance of other frequently used but inexpensive routes.</p>

<p>The example server has some code that is blocking the Event Loop, so the next step is to locate that code.</p>

<h3 id="analyzing">Analyzing</h3>

<p>One way to quickly identify poorly performing code is to create and analyze a flame graph. A flame graph represents function calls as blocks sitting on top of each other &mdash; not over time but in aggregate. The reason it’s called a ‘flame graph’ is because it typically uses an orange to red color scheme, where the redder a block is the &ldquo;hotter&rdquo; a function is, meaning, the more it’s likely to be blocking the event loop. Capturing data for a flame graph is conducted through sampling the CPU &mdash; meaning that a snapshot of the function that is currently being executed and it’s stack is taken. The heat is determined by the percentage of time during profiling that a given function is at the top of the stack (e.g. the function currently being executed) for each sample. If it’s not the last function to ever be called within that stack, then it’s likely to be blocking the event loop.</p>

<p>Let’s use <code>clinic flame</code> to generate a flame graph of the example application:</p>

<pre><code class="language-bash">clinic flame --on-port=’autocannon -c100 localhost:$PORT/seed/v1’ -- node index.js
</code></pre>

<p>The result should open in our browser with something like the following:</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e66e46db-278c-45f8-b376-2eb0e61b1c07/keeping-nodejs-fast-fig3.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e66e46db-278c-45f8-b376-2eb0e61b1c07/keeping-nodejs-fast-fig3.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e66e46db-278c-45f8-b376-2eb0e61b1c07/keeping-nodejs-fast-fig3.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e66e46db-278c-45f8-b376-2eb0e61b1c07/keeping-nodejs-fast-fig3.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e66e46db-278c-45f8-b376-2eb0e61b1c07/keeping-nodejs-fast-fig3.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e66e46db-278c-45f8-b376-2eb0e61b1c07/keeping-nodejs-fast-fig3.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e66e46db-278c-45f8-b376-2eb0e61b1c07/keeping-nodejs-fast-fig3.png"
			sizes="100vw"
			alt="Clinic’s flame graph shows that server.on is the bottleneck"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Clinic’s flame graph visualization
		</figcaption>
	
</figure>


<p>The width of a block represents how much time it spent on CPU overall. Three main stacks can be observed taking up the most time, all of them highlighting <code>server.on</code> as the hottest function. In truth, all three stacks are the same. They diverge because during profiling optimized and unoptimized functions are treated as separate call frames. Functions prefixed with a <code>*</code> are optimized by the JavaScript engine, and those prefixed with a <code>~</code> are unoptimized. If the optimized state isn’t important to us, we can simplify the graph further by pressing the Merge button. This should lead to view similar to the following:</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cb7a8625-10cb-439e-b5a3-c8a5471dad42/keeping-nodejs-fast-fig4.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cb7a8625-10cb-439e-b5a3-c8a5471dad42/keeping-nodejs-fast-fig4.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cb7a8625-10cb-439e-b5a3-c8a5471dad42/keeping-nodejs-fast-fig4.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cb7a8625-10cb-439e-b5a3-c8a5471dad42/keeping-nodejs-fast-fig4.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cb7a8625-10cb-439e-b5a3-c8a5471dad42/keeping-nodejs-fast-fig4.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cb7a8625-10cb-439e-b5a3-c8a5471dad42/keeping-nodejs-fast-fig4.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cb7a8625-10cb-439e-b5a3-c8a5471dad42/keeping-nodejs-fast-fig4.png"
			sizes="100vw"
			alt="Merged flame graph"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Merging the flame graph
		</figcaption>
	
</figure>


<p>From the outset, we can infer that the offending code is in the <code>util.js</code> file of the application code.</p>

<p>The slow function is also an event handler: the functions leading up to the function are part of the core <code>events</code> module, and <code>server.on</code> is a fallback name for an anonymous function provided as an event handling function. We can also see that this code isn’t in the same tick as code that actually handles the request. If there were functions in the core, <code>http</code>, <code>net</code>, and <code>stream</code> would be in the stack.</p>

<p>Such core functions can be found by expanding other, much smaller, parts of the flame graph. For instance, try using the search input on the top right of the UI to search for <code>send</code> (the name of both <code>restify</code> and <code>http</code> internal methods). It should be on the right of the graph (functions are alphabetically sorted):</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/08c9f71a-a7b7-41c3-b4ca-bf8f231be74a/keeping-nodejs-fast-fig5.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/08c9f71a-a7b7-41c3-b4ca-bf8f231be74a/keeping-nodejs-fast-fig5.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/08c9f71a-a7b7-41c3-b4ca-bf8f231be74a/keeping-nodejs-fast-fig5.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/08c9f71a-a7b7-41c3-b4ca-bf8f231be74a/keeping-nodejs-fast-fig5.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/08c9f71a-a7b7-41c3-b4ca-bf8f231be74a/keeping-nodejs-fast-fig5.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/08c9f71a-a7b7-41c3-b4ca-bf8f231be74a/keeping-nodejs-fast-fig5.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/08c9f71a-a7b7-41c3-b4ca-bf8f231be74a/keeping-nodejs-fast-fig5.png"
			sizes="100vw"
			alt="Flame graph has two small blocks highlighted which represent HTTP processing function"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Searching the flame graph for HTTP processing functions
		</figcaption>
	
</figure>


<p>Notice how comparatively small all the actual HTTP handling blocks are.</p>

<p>We can click one of the blocks highlighted in cyan which will expand to show functions like <code>writeHead</code> and <code>write</code> in the <em>http_outgoing.js</em> file (part of Node core <code>http</code> library):</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/aa2473b4-f097-4068-ac8a-3d6d26bd6e8c/keeping-nodejs-fast-fig6.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/aa2473b4-f097-4068-ac8a-3d6d26bd6e8c/keeping-nodejs-fast-fig6.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/aa2473b4-f097-4068-ac8a-3d6d26bd6e8c/keeping-nodejs-fast-fig6.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/aa2473b4-f097-4068-ac8a-3d6d26bd6e8c/keeping-nodejs-fast-fig6.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/aa2473b4-f097-4068-ac8a-3d6d26bd6e8c/keeping-nodejs-fast-fig6.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/aa2473b4-f097-4068-ac8a-3d6d26bd6e8c/keeping-nodejs-fast-fig6.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/aa2473b4-f097-4068-ac8a-3d6d26bd6e8c/keeping-nodejs-fast-fig6.png"
			sizes="100vw"
			alt="Flame graph has zoomed into a different view showing HTTP related stacks"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Expanding the flame graph into HTTP relevant stacks
		</figcaption>
	
</figure>


<p>We can click <strong>all stacks</strong> to return to the main view.</p>

<p>The key point here is that even though the <code>server.on</code> function isn’t in the same tick as the actual request handling code, it’s still affecting the overall server performance by delaying the execution of otherwise performant code.</p>

<h3 id="debugging">Debugging</h3>

<p>We know from the flame graph that the problematic function is the event handler passed to <code>server.on</code> in the <em>util.js</em> file.</p>

<p>Let’s take a look:</p>

<pre><code class="language-javascript">server.on('after', (req, res) => {
  if (res.statusCode !== 200) return
  if (!res._body) return
  const key = crypto.createHash('sha512')
    .update(req.url)
    .digest()
    .toString('hex')
  const etag = crypto.createHash('sha512')
    .update(JSON.stringify(res._body))
    .digest()
    .toString('hex')
  if (cache[key] !== etag) cache[key] = etag
})
</code></pre>

<p>It’s well known that cryptography tends to be expensive, as does serialization (<code>JSON.stringify</code>) but why don’t they appear in the flame graph? These operations are in the captured samples, but they’re hidden behind the <code>cpp</code> filter. If we press the <code>cpp</code> button we should see something like the following:</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/04ac9144-fbb4-47f3-a55a-dff4e053b9ec/keeping-nodejs-fast-fig7.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/04ac9144-fbb4-47f3-a55a-dff4e053b9ec/keeping-nodejs-fast-fig7.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/04ac9144-fbb4-47f3-a55a-dff4e053b9ec/keeping-nodejs-fast-fig7.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/04ac9144-fbb4-47f3-a55a-dff4e053b9ec/keeping-nodejs-fast-fig7.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/04ac9144-fbb4-47f3-a55a-dff4e053b9ec/keeping-nodejs-fast-fig7.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/04ac9144-fbb4-47f3-a55a-dff4e053b9ec/keeping-nodejs-fast-fig7.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/04ac9144-fbb4-47f3-a55a-dff4e053b9ec/keeping-nodejs-fast-fig7.png"
			sizes="100vw"
			alt="Additional blocks related to C&#43;&#43; have been revealed in the flame graph (main view)"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Revealing serialization and cryptography C++ frames
		</figcaption>
	
</figure>


<p>The internal V8 instructions relating to both serialization and cryptography are now shown as the hottest stacks and as taking up most of the time. The <code>JSON.stringify</code> method directly calls C++ code; this is why we don’t see a JavaScript function. In the cryptography case, functions like <code>createHash</code> and <code>update</code> are in the data, but they are either inlined (which means they disappear in the merged view) or too small to render.</p>

<p>Once we start to reason about the code in the <code>etagger</code> function it can quickly become apparent that it’s poorly designed. Why are we taking the <code>server</code> instance from the function context? There’s a lot of hashing going on, is all of that necessary? There’s also no <code>If-None-Match</code> header support in the implementation which would mitigate some of the load in some real-world scenarios because clients would only make a head request to determine freshness.</p>

<p>Let’s ignore all of these points for the moment and validate the finding that the actual work being performed in <code>server.on</code> is indeed the bottleneck. This can be achieved by setting the <code>server.on</code> code to an empty function and generating a new flamegraph.</p>

<p>Alter the <code>etagger</code> function to the following:</p>

<pre><code class="language-javascript">function etagger () {
  var cache = {}
  var afterEventAttached = false
  function attachAfterEvent (server) {
    if (attachAfterEvent === true) return
    afterEventAttached = true
    server.on('after', (req, res) => {})
  }
  return function (req, res, next) {
    attachAfterEvent(this)
    const key = crypto.createHash('sha512')
      .update(req.url)
      .digest()
      .toString('hex')
    if (key in cache) res.set('Etag', cache[key])
    res.set('Cache-Control', 'public, max-age=120')
    next()
  }
}
</code></pre>

<p>The event listener function passed to <code>server.on</code> is now a no-op.</p>

<p>Let’s run <code>clinic flame</code> again:</p>

<pre><code class="language-bash">clinic flame --on-port='autocannon -c100 localhost:$PORT/seed/v1' -- node index.js
</code></pre>

<p>This should produce a flame graph similar to the following:</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4cdce88f-d682-4897-9f86-ae4f0b0faebc/keeping-nodejs-fast-fig8.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4cdce88f-d682-4897-9f86-ae4f0b0faebc/keeping-nodejs-fast-fig8.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4cdce88f-d682-4897-9f86-ae4f0b0faebc/keeping-nodejs-fast-fig8.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4cdce88f-d682-4897-9f86-ae4f0b0faebc/keeping-nodejs-fast-fig8.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4cdce88f-d682-4897-9f86-ae4f0b0faebc/keeping-nodejs-fast-fig8.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4cdce88f-d682-4897-9f86-ae4f0b0faebc/keeping-nodejs-fast-fig8.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4cdce88f-d682-4897-9f86-ae4f0b0faebc/keeping-nodejs-fast-fig8.png"
			sizes="100vw"
			alt="Flame graph shows that Node.js event system stacks are still the bottleneck"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Flame graph of the server when server.on is an empty function
		</figcaption>
	
</figure>


<p>This looks better, and we should have noticed an increase in request per second. But why is the event emitting code so hot? We would expect at this point for the HTTP processing code to take up the majority of CPU time, there’s nothing executing at all in the <code>server.on</code> event.</p>

<p>This type of bottleneck is caused by a function being executed more than it should be.</p>

<p>The following suspicious code at the top of <code>util.js</code> may be a clue:</p>

<pre><code class="language-javascript">require('events').defaultMaxListeners = Infinity
</code></pre>

<p>Let’s remove this line and start our process with the <code>--trace-warnings</code> flag:</p>

<pre><code class="language-bash">node --trace-warnings index.js
</code></pre>

<p>If we profile with AutoCannon in another terminal, like so:</p>

<pre><code class="language-bash">autocannon -c100 localhost:3000/seed/v1
</code></pre>

<p>Our process will output something similar to:</p>

<pre class="break-out"><code class="language-javascript">(node:96371) MaxListenersExceededWarning: Possible EventEmitter memory leak detected. 11 after listeners added. Use emitter.setMaxListeners() to increase limit
  at _addListener (events.js:280:19)
  at Server.addListener (events.js:297:10)
  at attachAfterEvent 
    (/Users/davidclements/z/nearForm/keeping-node-fast/slow/util.js:22:14)
  at Server.<anonymous>
    (/Users/davidclements/z/nearForm/keeping-node-fast/slow/util.js:25:7)
  at call
    (/Users/davidclements/z/nearForm/keeping-node-fast/slow/node_modules/restify/lib/chain.js:164:9)
  at next
    (/Users/davidclements/z/nearForm/keeping-node-fast/slow/node_modules/restify/lib/chain.js:120:9)
  at Chain.run
    (/Users/davidclements/z/nearForm/keeping-node-fast/slow/node_modules/restify/lib/chain.js:123:5)
  at Server._runUse
    (/Users/davidclements/z/nearForm/keeping-node-fast/slow/node_modules/restify/lib/server.js:976:19)
  at Server._runRoute
    (/Users/davidclements/z/nearForm/keeping-node-fast/slow/node_modules/restify/lib/server.js:918:10)
  at Server._afterPre
    (/Users/davidclements/z/nearForm/keeping-node-fast/slow/node_modules/restify/lib/server.js:888:10)
</code></pre>

<p>Node is telling us that lots of events are being attached to the <em>server</em> object. This is strange because there’s a boolean that checks if the event has been attached and then returns early essentially making <em>attachAfterEvent</em> a no-op after the first event is attached.</p>

<p>Let’s take a look at the <code>attachAfterEvent</code> function:</p>

<pre><code class="language-javascript">var afterEventAttached = false
function attachAfterEvent (server) {
  if (attachAfterEvent === true) return
  afterEventAttached = true
  server.on('after', (req, res) => {})
}
</code></pre>

<p>The conditional check is wrong! It checks whether <code>attachAfterEvent</code> is true instead of <code>afterEventAttached</code>. This means a new event is being attached to the <code>server</code> instance on every request, and then all prior attached events are being fired after each request. <em>Whoops!</em></p>

<h3 id="optimizing">Optimizing</h3>

<p>Now that we’ve discovered the problem areas, let’s see if we can make the server faster.</p>

<h4 id="low-hanging-fruit">Low-Hanging Fruit</h4>

<p>Let’s put the <code>server.on</code> listener code back (instead of an empty function) and use the correct boolean name in the conditional check. Our <code>etagger</code> function looks as follows:</p>

<pre><code class="language-javascript">function etagger () {
  var cache = {}
  var afterEventAttached = false
  function attachAfterEvent (server) {
    if (afterEventAttached === true) return
    afterEventAttached = true
    server.on('after', (req, res) => {
      if (res.statusCode !== 200) return
      if (!res._body) return
      const key = crypto.createHash('sha512')
        .update(req.url)
        .digest()
        .toString('hex')
      const etag = crypto.createHash('sha512')
        .update(JSON.stringify(res._body))
        .digest()
        .toString('hex')
      if (cache[key] !== etag) cache[key] = etag
    })
  }
  return function (req, res, next) {
    attachAfterEvent(this)
    const key = crypto.createHash('sha512')
      .update(req.url)
      .digest()
      .toString('hex')
    if (key in cache) res.set('Etag', cache[key])
    res.set('Cache-Control', 'public, max-age=120')
    next()
  }
}
</code></pre>

<p>Now we check our fix by profiling again. Start the server in one terminal:</p>

<pre><code class="language-bash">node index.js
</code></pre>

<p>Then profile with AutoCannon:</p>

<pre><code class="language-bash">autocannon -c100 localhost:3000/seed/v1
</code></pre>

<p>We should see results somewhere in the range of a 200 times improvement (Running 10s test @ <code>http://localhost:3000/seed/v1</code> &mdash; 100 connections):</p>

<p><table class="tablesaw break-out" data-tablesaw-mode="swipe" data-tablesaw-minimap>
    <thead>
        <tr>
            <th data-tablesaw-priority="persist">Stat</th>
            <th>Avg</th>
            <th>Stdev</th>
            <th>Max</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Latency (ms)</td>
            <td>19.47</td>
            <td>4.29</td>
            <td>103</td>
        </tr>
        <tr>
            <td>Req/Sec</td>
            <td>5011.11</td>
            <td>506.2</td>
            <td>5487</td>
        </tr>
        <tr>
            <td>Bytes/Sec</td>
            <td>51.8 MB</td>
            <td>5.45 MB</td>
            <td>58.72 MB</td>
        </tr>
    </tbody>
</table><figcaption><em>50k requests in 10s, 519.64 MB read</em></figcaption></p>

<p>It’s important to balance potential server cost reductions with development costs. We need to define, in our own situational contexts, how far we need to go in optimizing a project. Otherwise, it can be all too easy to put 80% of the effort into 20% of the speed enhancements. Do the constraints of the project justify this?</p>

<p>In some scenarios, it could be appropriate to achieve a 200 times improvement with a low hanging fruit and call it a day. In others, we may want to make our implementation as fast as it can possibly be. It really depends on project priorities.</p>

<p>One way to control resource spend is to set a goal. For instance, 10 times improvement, or 4000 requests per second. Basing this on business needs makes the most sense. For instance, if server costs are 100% over budget, we can set a goal of 2x improvement.</p>




  <aside class="product-panel product-panel__tilted product-panel--book" data-audience="non-subscriber" data-remove="true">
    <div class="container product-panel--book__container">
      <div class="panel__description panel__description--book">
        <p>
          Is your pattern library up to date today? <em>Alla Kholmatova</em> has just finished a fully fledged book on <strong>Design Systems</strong> and how to get them right. With common traps, gotchas and the lessons she learned. Hardcover, eBook. <em>Just sayin'.</em>
        </p>
        <a href="https://www.smashingmagazine.com/printed-books/design-systems/">
          <button class="btn btn--green btn--large">
            Table of Contents&nbsp;&rarr;
          </button>
        </a>
      </div>
      <div class="panel__image panel__image--book">
        <a href="https://www.smashingmagazine.com/printed-books/design-systems/" class="books__book__image">
        <div class="books__book__img">
          <img src="https://www.smashingmagazine.com/images/books/design-systems--large-opt.png">
        </div>
      </a>
      </div>
    </div>
  </aside>




<h4 id="taking-it-further">Taking It Further</h4>

<p>If we produce a new flame graph of our server, we should see something similar to the following:</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/754786c8-2600-4b9f-861d-fe73157175f2/keeping-nodejs-fast-fig9.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/754786c8-2600-4b9f-861d-fe73157175f2/keeping-nodejs-fast-fig9.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/754786c8-2600-4b9f-861d-fe73157175f2/keeping-nodejs-fast-fig9.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/754786c8-2600-4b9f-861d-fe73157175f2/keeping-nodejs-fast-fig9.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/754786c8-2600-4b9f-861d-fe73157175f2/keeping-nodejs-fast-fig9.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/754786c8-2600-4b9f-861d-fe73157175f2/keeping-nodejs-fast-fig9.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/754786c8-2600-4b9f-861d-fe73157175f2/keeping-nodejs-fast-fig9.png"
			sizes="100vw"
			alt="Flame graph still shows server.on as the bottleneck, but a smaller bottleneck"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Flame graph after the performance bug fix has been made
		</figcaption>
	
</figure>


<p>The event listener is still the bottleneck, it’s still taking up one-third of CPU time during profiling (the width is about one third the whole graph).</p>

<p>What additional gains can be made, and are the changes (along with their associated disruption) worth making?</p>

<p>With an optimized implementation, which is nonetheless slightly more constrained, the following performance characteristics can be achieved (Running 10s test @ <code>http://localhost:3000/seed/v1</code> &mdash; 10 connections):</p>

<p><table class="tablesaw break-out" data-tablesaw-mode="swipe" data-tablesaw-minimap>
    <thead>
        <tr>
            <th data-tablesaw-priority="persist">Stat</th>
            <th>Avg</th>
            <th>Stdev</th>
            <th>Max</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Latency (ms)</td>
            <td>0.64</td>
            <td>0.86</td>
            <td>17</td>
        </tr>
        <tr>
            <td>Req/Sec</td>
            <td>8330.91</td>
            <td>757.63</td>
            <td>8991</td>
        </tr>
        <tr>
            <td>Bytes/Sec</td>
            <td>84.17 MB</td>
            <td>7.64 MB</td>
            <td>92.27 MB</td>
        </tr>
    </tbody>
</table><figcaption><em>92k requests in 11s, 937.22 MB read</em></figcaption></p>

<p>While a 1.6x improvement is significant, it arguable depends on the situation whether the effort, changes, and code disruption necessary to create this improvement are justified. Especially when compared to the 200x improvement on the original implementation with a single bug fix.</p>

<p>To achieve this improvement, the same iterative technique of profile, generate flamegraph, analyze, debug, and optimize was used to arrive at the final optimized server, the code for which can be found .</p>

<p>The final changes to reach 8000 req/s were:</p>

<ul>
<li>Don’t build objects and then serialize, ;</li>
<li>;</li>
<li>Don’t hash the URL, .</li>
</ul>

<p>These changes are slightly more involved, a little more disruptive to the code base, and leave the <code>etagger</code> middleware a little less flexible because it puts the burden on the route to provide the <code>Etag</code> value. But it achieves an extra 3000 requests per second on the profiling machine.</p>

<p>Let’s take a look at a flame graph for these final improvements:</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ec765a73-3727-4fa2-aa78-c7a3ef8f5de5/keeping-nodejs-fast-fig10.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ec765a73-3727-4fa2-aa78-c7a3ef8f5de5/keeping-nodejs-fast-fig10.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ec765a73-3727-4fa2-aa78-c7a3ef8f5de5/keeping-nodejs-fast-fig10.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ec765a73-3727-4fa2-aa78-c7a3ef8f5de5/keeping-nodejs-fast-fig10.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ec765a73-3727-4fa2-aa78-c7a3ef8f5de5/keeping-nodejs-fast-fig10.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ec765a73-3727-4fa2-aa78-c7a3ef8f5de5/keeping-nodejs-fast-fig10.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ec765a73-3727-4fa2-aa78-c7a3ef8f5de5/keeping-nodejs-fast-fig10.png"
			sizes="100vw"
			alt="Flame graph shows that internal code related to the net module is now the bottleneck"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Healthy flame graph after all performance improvements
		</figcaption>
	
</figure>


<p>The hottest part of the flame graph is part of Node core, in the <code>net</code> module. This is ideal.</p>

<h3 id="preventing-performance-problems">Preventing Performance Problems</h3>

<p>To round off, here are some suggestions on ways to prevent performance issues in before they are deployed.</p>

<p>Using performance tools as informal checkpoints during development can filter out performance bugs before they make it into production. Making AutoCannon and Clinic (or equivalents) part of everyday development tooling is recommended.</p>

<p>When buying into a framework, find out what it’s policy on performance is. If the framework does not prioritize performance, then it’s important to check whether that aligns with infrastructural practices and business goals. For instance, Restify has clearly (since the release of version 7) invested in enhancing the library’s performance. However, if low cost and high speed is an absolute priority, consider Fastify which  by a Restify contributor.</p>

<p>Watch out for other widely impacting library choices &mdash; especially consider logging. As developers fix issues, they may decide to add additional log output to help debug related problems in the future. If an unperformant logger is used, this can strangle performance over time after the fashion of the  logger is the fastest newline delimited JSON logger available for Node.js.</p>

<p>Finally, always remember that the Event Loop is a shared resource. A Node.js server is ultimately constrained by the slowest logic in the hottest path.</p>




<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(rb, ra, il)</span>
</div>


</div>




  <div id="sponsors-article-end" data-impression="true" class="c-promo-box c-promo-box--ad c-promo-box--wide sponsors hidden" data-audience="non-subscriber" data-remove="true"></div>



              </article>
            </body>
          </html>
---------------
<h1 id="#title_1" >2、我对React Native的那些执念</h1>
罗晴明
[http://www.infoq.com/cn/news/2018/06/react-native-insistence?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/06/react-native-insistence?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>对于 React Native的使用者来说，你应该了解 React Native开发路线，避免掉坑出不来。</p> <i>By 罗晴明</i>
---------------
<h1 id="#title_2" >3、文章： Netflix:当你按下“播放”的时候发生了什么？</h1>
陈亮芬
[http://www.infoq.com/cn/articles/netflix-what-happens-when-you-press-play?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/netflix-what-happens-when-you-press-play?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/netflix-what-happens-when-you-press-play/zh/smallimage/logo-ieee-1528386565808.jpg"/><p>文章介绍了Netflix为用户提供视频服务所涉及的云技术，主要包括：Netflix选择AWS的优势，使用AWS如何进行存储、计算、分析、个性化推荐，对视频源文件的转码、使用CDN的必要性以及Open Connect简介等。</p> <i>By 陈亮芬</i>
---------------
<h1 id="#title_3" >4、文章： 携程Apollo配置中心架构深度剖析</h1>
杨波
[http://www.infoq.com/cn/articles/ctrip-apollo-configuration-center-architecture?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/ctrip-apollo-configuration-center-architecture?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/ctrip-apollo-configuration-center-architecture/zh/smallimage/BOLTS-1524870463316-1528302395624.jpg"/><p>Apollo（阿波罗）是携程框架部研发并开源的一款生产级的配置中心产品，它能够集中管理应用在不同环境、不同集群的配置，配置修改后能够实时推送到应用端，并且具备规范的权限、流程治理等特性，适用于微服务配置管理场景。</p> <i>By 杨波</i>
---------------
<h1 id="#title_4" >5、视频演讲： OPPO Redis Cluster技术实践</h1>
郭祥
[http://www.infoq.com/cn/presentations/oppo-redis-cluster-technology-practice?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/oppo-redis-cluster-technology-practice?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/presentations/oppo-redis-cluster-technology-practice/zh/mediumimage/guoxiang270-1528168294189.jpg"/><p>本次分享主要介绍OPPO在Redis Cluster大规模使用过程中的经验总结，将从Redis调优、监控体系、深度运维等多个角度进行分享。
</p> <i>By 郭祥</i>
---------------
<h1 id="#title_5" >6、文章： DevSecOps的三种解读</h1>
Guy Podjarny
[http://www.infoq.com/cn/articles/three-faces-DevSecOps?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/three-faces-DevSecOps?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/three-faces-DevSecOps/zh/headerimage/GettyImages-900874864-1527029199848.jpg"/><p>当前有很多供应商都在提DevSecOps这个术语，但对于却有着不同的解读，那么它是什么呢？支持 DevOps 技术的安全解决方案？还是调整适应DevOps 方法论？或者是拥抱DevOps 哲学？
</p> <i>By Guy Podjarny</i> <i> Translated by 冬雨</i>
---------------
<h1 id="#title_6" >7、极限编程创始人Ron Jeffries建议开发者放弃敏捷</h1>
Rui Miguel Ferreira
[http://www.infoq.com/cn/news/2018/06/developers-should-abandon-agile?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/06/developers-should-abandon-agile?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Ron Jeffries是极限编程（XP）的创始人之一，也是敏捷宣言的签名人之一，他在博客中发表了一篇文章，主张开发人员应该放弃“敏捷”，也就是说他们应远离“虚假敏捷”或“黑暗敏捷”，更接近敏捷宣言的价值观和原则。</p> <i>By Rui Miguel Ferreira</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_7" >8、Oracle在开源Mission Control后将其开发团队解散</h1>
Kesha Williams
[http://www.infoq.com/cn/news/2018/06/open-source-jmc?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/06/open-source-jmc?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>甲骨文于5月3日宣布开源Java Mission Control工具套件（也称为JMC），收到了Java开发社区的热烈掌声，也让开发社区兴奋无比。但这种兴奋很快被一种不安的情绪所替代，据报道，整个JMC开发团队因此被解散。</p> <i>By Kesha Williams</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_8" >9、TypeScript 2.9发布，更新了对ES.Next的支持</h1>
Dylan Schiemann
[http://www.infoq.com/cn/news/2018/06/typescript-2-9-es-next?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/06/typescript-2-9-es-next?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>TypeScript 2.9包含多项针对该语言的改善。现在，能够支持ES.Next的import.meta，同时支持keyof和映射对象类型中的符号与数字字面量。</p> <i>By Dylan Schiemann</i> <i> Translated by 张卫滨 </i>
---------------
<h1 id="#title_9" >10、Zip Slip目录遍历漏洞已影响多个Java项目</h1>
Charles Humble
[http://www.infoq.com/cn/news/2018/06/zip-slip?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/06/zip-slip?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>近日，专注于安全监控防范工作的 Snyk 公司披露了一种可能会造成任意文件被覆写的安全漏洞，称为 Zip Slip。其相应的攻击手段是创建一种特制的ZIP压缩文件，在其中包含会对目录进行遍历的文件名。受该风险影响的项目多达数千个，包括 AWS CodePipeline、Spring Integration、LinkedIn的Pinot、 Apache/Twitter Heron、Alibaba JStorm、Jenkins、Gradle 和 Google Cloud Platform等。
</p> <i>By Charles Humble</i> <i> Translated by 邵思华</i>
---------------
<h1 id="#title_10" >11、You Probably Don't Need Derived State</h1>

[https://reactjs.org/blog/2018/06/07/you-probably-dont-need-derived-state.html](https://reactjs.org/blog/2018/06/07/you-probably-dont-need-derived-state.html)
<p>React 16.4 included a  which caused some existing bugs in React components to reproduce more consistently. If this release exposed a case where your application was using an anti-pattern and didn’t work properly after the fix, we’re sorry for the churn. In this post, we will explain some common anti-patterns with derived state and our preferred alternatives.</p>
<p>For a long time, the lifecycle <code>componentWillReceiveProps</code> was the only way to update state in response to a change in props without an additional render. In version 16.3, , so the results of misusing it are easier to notice.</p>
<blockquote>
<p>Note</p>
<p>All of the anti-patterns described in this post apply to both the older <code>componentWillReceiveProps</code> and the newer <code>getDerivedStateFromProps</code>.</p>
</blockquote>
<p> This blog post will cover the following topics:</p>
<ul>
<li></li>
<li>
<p></p>
<ul>
<li></li>
<li></li>
</ul>
</li>
<li></li>
<li></li>
</ul>
<h2 id="when-to-use-derived-state">When to Use Derived State</h2>
<p><code>getDerivedStateFromProps</code> exists for only one purpose. It enables a component to update its internal state as the result of <strong>changes in props</strong>. Our previous blog post provided some examples, like .</p>
<p>We did not provide many examples, because as a general rule, <strong>derived state should be used sparingly</strong>. All problems with derived state that we have seen can be ultimately reduced to either (1) unconditionally updating state from props or (2) updating state whenever props and state don’t match. (We’ll go over both in more detail below.)</p>
<ul>
<li>If you’re using derived state to memoize some computation based only on the current props, you don’t need derived state. See  below.</li>
<li>If you’re updating derived state unconditionally or updating it whenever props and state don’t match, your component likely resets its state too frequently. Read on for more details.</li>
</ul>
<h2 id="common-bugs-when-using-derived-state">Common Bugs When Using Derived State</h2>
<p>The terms  usually refer to form inputs, but they can also describe where any component’s data lives. Data passed in as props can be thought of as <strong>controlled</strong> (because the parent component <em>controls</em> that data). Data that exists only in internal state can be thought of as <strong>uncontrolled</strong> (because the parent can’t directly change it).</p>
<p>The most common mistake with derived state is mixing these two; when a derived state value is also updated by <code>setState</code> calls, there isn’t a single source of truth for the data. The  mentioned above may sound similar, but it’s different in a few important ways. In the loading example, there is a clear source of truth for both the “source” prop and the “loading” state. When the source prop changes, the loading state should <strong>always</strong> be overridden. Conversely, the state is overridden only when the prop <strong>changes</strong> and is otherwise managed by the component.</p>
<p>Problems arise when any of these constraints are changed. This typically comes in two forms. Let’s take a look at both.</p>
<h3 id="anti-pattern-unconditionally-copying-props-to-state">Anti-pattern: Unconditionally copying props to state</h3>
<p>A common misconception is that <code>getDerivedStateFromProps</code> and <code>componentWillReceiveProps</code> are only called when props “change”. These lifecycles are called any time a parent component rerenders, regardless of whether the props are “different” from before. Because of this, it has always been unsafe to <em>unconditionally</em> override state using either of these lifecycles. <strong>Doing so will cause state updates to be lost.</strong></p>
<p>Let’s consider an example to demonstrate the problem. Here is a <code>EmailInput</code> component that “mirrors” an email prop in state:</p>
<div class="gatsby-highlight">
      <pre class="gatsby-code-jsx"><code><span class="token keyword">class</span> <span class="token class-name">EmailInput</span> <span class="token keyword">extends</span> <span class="token class-name">Component</span> <span class="token punctuation">{</span>
  state <span class="token operator">=</span> <span class="token punctuation">{</span> email<span class="token punctuation">:</span> <span class="token keyword">this</span><span class="token punctuation">.</span>props<span class="token punctuation">.</span>email <span class="token punctuation">}</span><span class="token punctuation">;</span>

  <span class="token function">render</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token keyword">return</span> <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">onChange</span><span class="token script language-javascript"><span class="token punctuation">=</span><span class="token punctuation">{</span><span class="token keyword">this</span><span class="token punctuation">.</span>handleChange<span class="token punctuation">}</span></span> <span class="token attr-name">value</span><span class="token script language-javascript"><span class="token punctuation">=</span><span class="token punctuation">{</span><span class="token keyword">this</span><span class="token punctuation">.</span>state<span class="token punctuation">.</span>email<span class="token punctuation">}</span></span> <span class="token punctuation">/></span></span><span class="token punctuation">;</span>
  <span class="token punctuation">}</span>

  <span class="token function-variable function">handleChange</span> <span class="token operator">=</span> event <span class="token operator">=></span> <span class="token punctuation">{</span>
    <span class="token keyword">this</span><span class="token punctuation">.</span><span class="token function">setState</span><span class="token punctuation">(</span><span class="token punctuation">{</span> email<span class="token punctuation">:</span> event<span class="token punctuation">.</span>target<span class="token punctuation">.</span>value <span class="token punctuation">}</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
  <span class="token punctuation">}</span><span class="token punctuation">;</span>

  <span class="token function">componentWillReceiveProps</span><span class="token punctuation">(</span>nextProps<span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token comment">// This will erase any local state updates!</span>
    <span class="token comment">// Do not do this.</span>
    <span class="token keyword">this</span><span class="token punctuation">.</span><span class="token function">setState</span><span class="token punctuation">(</span><span class="token punctuation">{</span> email<span class="token punctuation">:</span> nextProps<span class="token punctuation">.</span>email <span class="token punctuation">}</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>
      </div>
<p>At first, this component might look okay. State is initialized to the value specified by props and updated when we type into the <code>&#x3C;input></code>. But if our component’s parent rerenders, anything we’ve typed into the <code>&#x3C;input></code> will be lost! () This holds true even if we were to compare <code>nextProps.email !== this.state.email</code> before resetting.</p>
<p>In this simple example, adding <code>shouldComponentUpdate</code> to rerender only when the email prop has changed could fix this. However in practice, components usually accept multiple props; another prop changing would still cause a rerender and improper reset. Function and object props are also often created inline, making it hard to implement a <code>shouldComponentUpdate</code> that reliably returns true only when a material change has happened.  As a result, <code>shouldComponentUpdate</code> is best used as a performance optimization, not to ensure correctness of derived state.</p>
<p>Hopefully it’s clear by now why <strong>it is a bad idea to unconditionally copy props to state</strong>. Before reviewing possible solutions, let’s look at a related problematic pattern: what if we were to only update the state when the email prop changes?</p>
<h3 id="anti-pattern-erasing-state-when-props-change">Anti-pattern: Erasing state when props change</h3>
<p>Continuing the example above, we could avoid accidentally erasing state by only updating it when <code>props.email</code> changes:</p>
<div class="gatsby-highlight">
      <pre class="gatsby-code-jsx"><code><span class="token keyword">class</span> <span class="token class-name">EmailInput</span> <span class="token keyword">extends</span> <span class="token class-name">Component</span> <span class="token punctuation">{</span>
  state <span class="token operator">=</span> <span class="token punctuation">{</span>
    email<span class="token punctuation">:</span> <span class="token keyword">this</span><span class="token punctuation">.</span>props<span class="token punctuation">.</span>email
  <span class="token punctuation">}</span><span class="token punctuation">;</span>

  <span class="token function">componentWillReceiveProps</span><span class="token punctuation">(</span>nextProps<span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token comment">// Any time props.email changes, update state.</span>
    <span class="token keyword">if</span> <span class="token punctuation">(</span>nextProps<span class="token punctuation">.</span>email <span class="token operator">!==</span> <span class="token keyword">this</span><span class="token punctuation">.</span>props<span class="token punctuation">.</span>email<span class="token punctuation">)</span> <span class="token punctuation">{</span>
      <span class="token keyword">this</span><span class="token punctuation">.</span><span class="token function">setState</span><span class="token punctuation">(</span><span class="token punctuation">{</span>
        email<span class="token punctuation">:</span> nextProps<span class="token punctuation">.</span>email
      <span class="token punctuation">}</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
    <span class="token punctuation">}</span>
  <span class="token punctuation">}</span>
  
  <span class="token comment">// ...</span>
<span class="token punctuation">}</span>
</code></pre>
      </div>
<blockquote>
<p>Note</p>
<p>Even though the example above shows <code>componentWillReceiveProps</code>, the same anti-pattern applies to <code>getDerivedStateFromProps</code>.</p>
</blockquote>
<p>We’ve just made a big improvement. Now our component will erase what we’ve typed only when the props actually change.</p>
<p>There is still a subtle problem. Imagine a password manager app using the above input component. When navigating between details for two accounts with the same email, the input would fail to reset. This is because the prop value passed to the component would be the same for both accounts! This would be a surprise to the user, as an unsaved change to one account would appear to affect other accounts that happened to share the same email. ()</p>
<p>This design is fundamentally flawed, but it’s also an easy mistake to make. () Fortunately there are two alternatives that work better. The key to both is that <strong>for any piece of data, you need to pick a single component that owns it as the source of truth, and avoid duplicating it in other components.</strong> Let’s take a look at each of the alternatives.</p>
<h2 id="preferred-solutions">Preferred Solutions</h2>
<h3 id="recommendation-fully-controlled-component">Recommendation: Fully controlled component</h3>
<p>One way to avoid the problems mentioned above is to remove state from our component entirely. If the email address only exists as a prop, then we don’t have to worry about conflicts with state. We could even convert <code>EmailInput</code> to a lighter-weight functional component:</p>
<div class="gatsby-highlight">
      <pre class="gatsby-code-jsx"><code><span class="token keyword">function</span> <span class="token function">EmailInput</span><span class="token punctuation">(</span>props<span class="token punctuation">)</span> <span class="token punctuation">{</span>
  <span class="token keyword">return</span> <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">onChange</span><span class="token script language-javascript"><span class="token punctuation">=</span><span class="token punctuation">{</span>props<span class="token punctuation">.</span>onChange<span class="token punctuation">}</span></span> <span class="token attr-name">value</span><span class="token script language-javascript"><span class="token punctuation">=</span><span class="token punctuation">{</span>props<span class="token punctuation">.</span>email<span class="token punctuation">}</span></span> <span class="token punctuation">/></span></span><span class="token punctuation">;</span>
<span class="token punctuation">}</span>
</code></pre>
      </div>
<p>This approach simplifies the implementation of our component, but if we still want to store a draft value, the parent form component will now need to do that manually. ()</p>
<h3 id="recommendation-fully-uncontrolled-component-with-a-key">Recommendation: Fully uncontrolled component with a <code>key</code></h3>
<p>Another alternative would be for our component to fully own the “draft” email state. In that case, our component could still accept a prop for the <em>initial</em> value, but it would ignore subsequent changes to that prop:</p>
<div class="gatsby-highlight">
      <pre class="gatsby-code-jsx"><code><span class="token keyword">class</span> <span class="token class-name">EmailInput</span> <span class="token keyword">extends</span> <span class="token class-name">Component</span> <span class="token punctuation">{</span>
  state <span class="token operator">=</span> <span class="token punctuation">{</span> email<span class="token punctuation">:</span> <span class="token keyword">this</span><span class="token punctuation">.</span>props<span class="token punctuation">.</span>defaultEmail <span class="token punctuation">}</span><span class="token punctuation">;</span>

  <span class="token function-variable function">handleChange</span> <span class="token operator">=</span> event <span class="token operator">=></span> <span class="token punctuation">{</span>
    <span class="token keyword">this</span><span class="token punctuation">.</span><span class="token function">setState</span><span class="token punctuation">(</span><span class="token punctuation">{</span> email<span class="token punctuation">:</span> event<span class="token punctuation">.</span>target<span class="token punctuation">.</span>value <span class="token punctuation">}</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
  <span class="token punctuation">}</span><span class="token punctuation">;</span>

  <span class="token function">render</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token keyword">return</span> <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">onChange</span><span class="token script language-javascript"><span class="token punctuation">=</span><span class="token punctuation">{</span><span class="token keyword">this</span><span class="token punctuation">.</span>handleChange<span class="token punctuation">}</span></span> <span class="token attr-name">value</span><span class="token script language-javascript"><span class="token punctuation">=</span><span class="token punctuation">{</span><span class="token keyword">this</span><span class="token punctuation">.</span>state<span class="token punctuation">.</span>email<span class="token punctuation">}</span></span> <span class="token punctuation">/></span></span><span class="token punctuation">;</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>
      </div>
<p>In order to reset the value when moving to a different item (as in our password manager scenario), we can use the special React attribute called <code>key</code>. When a <code>key</code> changes, React will . Keys are usually used for dynamic lists but are also useful here. In our case, we could use the user ID to recreate the email input any time a new user is selected:</p>
<div class="gatsby-highlight">
      <pre class="gatsby-code-jsx"><code><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>EmailInput</span>
  <span class="token attr-name">defaultEmail</span><span class="token script language-javascript"><span class="token punctuation">=</span><span class="token punctuation">{</span><span class="token keyword">this</span><span class="token punctuation">.</span>props<span class="token punctuation">.</span>user<span class="token punctuation">.</span>email<span class="token punctuation">}</span></span>
  <span class="token attr-name">key</span><span class="token script language-javascript"><span class="token punctuation">=</span><span class="token punctuation">{</span><span class="token keyword">this</span><span class="token punctuation">.</span>props<span class="token punctuation">.</span>user<span class="token punctuation">.</span>id<span class="token punctuation">}</span></span>
<span class="token punctuation">/></span></span>
</code></pre>
      </div>
<p>Each time the ID changes, the <code>EmailInput</code> will be recreated and its state will be reset to the latest <code>defaultEmail</code> value. () With this approach, you don’t have to add <code>key</code> to every input. It might make more sense to put a <code>key</code> on the whole form instead. Every time the key changes, all components within the form will be recreated with a freshly initialized state.</p>
<p>In most cases, this is the best way to handle state that needs to be reset.</p>
<blockquote>
<p>Note</p>
<p>While this may sound slow, the performance difference is usually insignificant. Using a key can even be faster if the components have heavy logic that runs on updates since diffing gets bypassed for that subtree.</p>
</blockquote>
<h4 id="alternative-1-reset-uncontrolled-component-with-an-id-prop">Alternative 1: Reset uncontrolled component with an ID prop</h4>
<p>If <code>key</code> doesn’t work for some reason (perhaps the component is very expensive to initialize), a workable but cumbersome solution would be to watch for changes to “userID” in <code>getDerivedStateFromProps</code>:</p>
<div class="gatsby-highlight">
      <pre class="gatsby-code-jsx"><code><span class="token keyword">class</span> <span class="token class-name">EmailInput</span> <span class="token keyword">extends</span> <span class="token class-name">Component</span> <span class="token punctuation">{</span>
  state <span class="token operator">=</span> <span class="token punctuation">{</span>
    email<span class="token punctuation">:</span> <span class="token keyword">this</span><span class="token punctuation">.</span>props<span class="token punctuation">.</span>defaultEmail<span class="token punctuation">,</span>
    prevPropsUserID<span class="token punctuation">:</span> <span class="token keyword">this</span><span class="token punctuation">.</span>props<span class="token punctuation">.</span>userID
  <span class="token punctuation">}</span><span class="token punctuation">;</span>

  <span class="token keyword">static</span> <span class="token function">getDerivedStateFromProps</span><span class="token punctuation">(</span>props<span class="token punctuation">,</span> state<span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token comment">// Any time the current user changes,</span>
    <span class="token comment">// Reset any parts of state that are tied to that user.</span>
    <span class="token comment">// In this simple example, that's just the email.</span>
    <span class="token keyword">if</span> <span class="token punctuation">(</span>props<span class="token punctuation">.</span>userID <span class="token operator">!==</span> state<span class="token punctuation">.</span>prevPropsUserID<span class="token punctuation">)</span> <span class="token punctuation">{</span>
      <span class="token keyword">return</span> <span class="token punctuation">{</span>
        prevPropsUserID<span class="token punctuation">:</span> props<span class="token punctuation">.</span>userID<span class="token punctuation">,</span>
        email<span class="token punctuation">:</span> props<span class="token punctuation">.</span>email
      <span class="token punctuation">}</span><span class="token punctuation">;</span>
    <span class="token punctuation">}</span>
    <span class="token keyword">return</span> <span class="token keyword">null</span><span class="token punctuation">;</span>
  <span class="token punctuation">}</span>

  <span class="token comment">// ...</span>
<span class="token punctuation">}</span>
</code></pre>
      </div>
<p>This also provides the flexibility to only reset parts of our component’s internal state if we so choose. ()</p>
<blockquote>
<p>Note</p>
<p>Even though the example above shows <code>getDerivedStateFromProps</code>, the same technique can be used with <code>componentWillReceiveProps</code>.</p>
</blockquote>
<h4 id="alternative-2-reset-uncontrolled-component-with-an-instance-method">Alternative 2: Reset uncontrolled component with an instance method</h4>
<p>More rarely, you may need to reset state even if there’s no appropriate ID to use as <code>key</code>. One solution is to reset the key to a random value or autoincrementing number each time you want to reset. One other viable alternative is to exposing an instance method to imperatively reset the internal state:</p>
<div class="gatsby-highlight">
      <pre class="gatsby-code-jsx"><code><span class="token keyword">class</span> <span class="token class-name">EmailInput</span> <span class="token keyword">extends</span> <span class="token class-name">Component</span> <span class="token punctuation">{</span>
  state <span class="token operator">=</span> <span class="token punctuation">{</span>
    email<span class="token punctuation">:</span> <span class="token keyword">this</span><span class="token punctuation">.</span>props<span class="token punctuation">.</span>defaultEmail
  <span class="token punctuation">}</span><span class="token punctuation">;</span>

  <span class="token function">resetEmailForNewUser</span><span class="token punctuation">(</span>newEmail<span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token keyword">this</span><span class="token punctuation">.</span><span class="token function">setState</span><span class="token punctuation">(</span><span class="token punctuation">{</span> email<span class="token punctuation">:</span> newEmail <span class="token punctuation">}</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
  <span class="token punctuation">}</span>

  <span class="token comment">// ...</span>
<span class="token punctuation">}</span>
</code></pre>
      </div>
<p>The parent form component could then )</p>
<p>Refs can be useful in certain cases like this one, but generally we recommend you use them sparingly. Even in the demo, this imperative method is nonideal because two renders will occur instead of one.</p>
<hr>
<h3 id="recap">Recap</h3>
<p>To recap, when designing a component, it is important to decide whether its data will be controlled or uncontrolled.</p>
<p>Instead of trying to <strong>“mirror” a prop value in state</strong>, make the component <strong>controlled</strong>, and consolidate the two diverging values in the state of some parent component. For example, rather than a child accepting a “committed” <code>props.value</code> and tracking a “draft” <code>state.value</code>, have the parent manage both <code>state.draftValue</code> and <code>state.committedValue</code> and control the child’s value directly. This makes the data flow more explicit and predictable.</p>
<p>For <strong>uncontrolled</strong> components, if you’re trying to reset state when a particular prop (usually an ID) changes, you have a few options:</p>
<ul>
<li><strong>Recomendation: To reset <em>all internal state</em>, use the <code>key</code> attribute.</strong></li>
<li>Alternative 1: To reset <em>only certain state fields</em>, watch for changes in a special property (e.g. <code>props.userID</code>).</li>
<li>Alternative 2: You can also consider fall back to an imperative instance method using refs.</li>
</ul>
<h2 id="what-about-memoization">What about memoization?</h2>
<p>We’ve also seen derived state used to ensure an expensive value used in <code>render</code> is recomputed only when the inputs change. This technique is known as .</p>
<p>Using derived state for memoization isn’t necessarily bad, but it’s usually not the best solution. There is inherent complexity in managing derived state, and this complexity increases with each additional property. For example, if we add a second derived field to our component state then our implementation would need to separately track changes to both.</p>
<p>Let’s look at an example of one component that takes one prop—a list of items—and renders the items that match a search query entered by the user. We could use derived state to store the filtered list:</p>
<div class="gatsby-highlight">
      <pre class="gatsby-code-jsx"><code><span class="token keyword">class</span> <span class="token class-name">Example</span> <span class="token keyword">extends</span> <span class="token class-name">Component</span> <span class="token punctuation">{</span>
  state <span class="token operator">=</span> <span class="token punctuation">{</span>
    filterText<span class="token punctuation">:</span> <span class="token string">""</span><span class="token punctuation">,</span>
  <span class="token punctuation">}</span><span class="token punctuation">;</span>

  <span class="token keyword">static</span> <span class="token function">getDerivedStateFromProps</span><span class="token punctuation">(</span>props<span class="token punctuation">,</span> state<span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token comment">// Re-run the filter whenever the list array or filter text change.</span>
    <span class="token comment">// Note we need to store prevPropsList and prevFilterText to detect changes.</span>
    <span class="token keyword">if</span> <span class="token punctuation">(</span>
      props<span class="token punctuation">.</span>list <span class="token operator">!==</span> state<span class="token punctuation">.</span>prevPropsList <span class="token operator">||</span>
      state<span class="token punctuation">.</span>prevFilterText <span class="token operator">!==</span> state<span class="token punctuation">.</span>filterText
    <span class="token punctuation">)</span> <span class="token punctuation">{</span>
      <span class="token keyword">return</span> <span class="token punctuation">{</span>
        prevPropsList<span class="token punctuation">:</span> props<span class="token punctuation">.</span>list<span class="token punctuation">,</span>
        prevFilterText<span class="token punctuation">:</span> state<span class="token punctuation">.</span>filterText<span class="token punctuation">,</span>
        filteredList<span class="token punctuation">:</span> props<span class="token punctuation">.</span>list<span class="token punctuation">.</span><span class="token function">filter</span><span class="token punctuation">(</span>item <span class="token operator">=></span> item<span class="token punctuation">.</span>text<span class="token punctuation">.</span><span class="token function">includes</span><span class="token punctuation">(</span>state<span class="token punctuation">.</span>filterText<span class="token punctuation">)</span><span class="token punctuation">)</span>
      <span class="token punctuation">}</span><span class="token punctuation">;</span>
    <span class="token punctuation">}</span>
    <span class="token keyword">return</span> <span class="token keyword">null</span><span class="token punctuation">;</span>
  <span class="token punctuation">}</span>

  <span class="token function-variable function">handleChange</span> <span class="token operator">=</span> event <span class="token operator">=></span> <span class="token punctuation">{</span>
    <span class="token keyword">this</span><span class="token punctuation">.</span><span class="token function">setState</span><span class="token punctuation">(</span><span class="token punctuation">{</span> filterText<span class="token punctuation">:</span> event<span class="token punctuation">.</span>target<span class="token punctuation">.</span>value <span class="token punctuation">}</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
  <span class="token punctuation">}</span><span class="token punctuation">;</span>

  <span class="token function">render</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token keyword">return</span> <span class="token punctuation">(</span>
      <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>Fragment</span><span class="token punctuation">></span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">onChange</span><span class="token script language-javascript"><span class="token punctuation">=</span><span class="token punctuation">{</span><span class="token keyword">this</span><span class="token punctuation">.</span>handleChange<span class="token punctuation">}</span></span> <span class="token attr-name">value</span><span class="token script language-javascript"><span class="token punctuation">=</span><span class="token punctuation">{</span><span class="token keyword">this</span><span class="token punctuation">.</span>state<span class="token punctuation">.</span>filterText<span class="token punctuation">}</span></span> <span class="token punctuation">/></span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>ul</span><span class="token punctuation">></span></span><span class="token punctuation">{</span><span class="token keyword">this</span><span class="token punctuation">.</span>state<span class="token punctuation">.</span>filteredList<span class="token punctuation">.</span><span class="token function">map</span><span class="token punctuation">(</span>item <span class="token operator">=></span> <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>li</span> <span class="token attr-name">key</span><span class="token script language-javascript"><span class="token punctuation">=</span><span class="token punctuation">{</span>item<span class="token punctuation">.</span>id<span class="token punctuation">}</span></span><span class="token punctuation">></span></span><span class="token punctuation">{</span>item<span class="token punctuation">.</span>text<span class="token punctuation">}</span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>li</span><span class="token punctuation">></span></span><span class="token punctuation">)</span><span class="token punctuation">}</span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>ul</span><span class="token punctuation">></span></span>
      <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>Fragment</span><span class="token punctuation">></span></span>
    <span class="token punctuation">)</span><span class="token punctuation">;</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>
      </div>
<p>This implementation avoids recalculating <code>filteredList</code> more often than necessary. But it is more complicated than it needs to be, because it has to separately track and detect changes in both props and state in order to properly update the filtered list. In this example, we could simplify things by using <code>PureComponent</code> and moving the filter operation into the render method: </p>
<div class="gatsby-highlight">
      <pre class="gatsby-code-jsx"><code><span class="token comment">// PureComponents only rerender if at least one state or prop value changes.</span>
<span class="token comment">// Change is determined by doing a shallow comparison of state and prop keys.</span>
<span class="token keyword">class</span> <span class="token class-name">Example</span> <span class="token keyword">extends</span> <span class="token class-name">PureComponent</span> <span class="token punctuation">{</span>
  <span class="token comment">// State only needs to hold the current filter text value:</span>
  state <span class="token operator">=</span> <span class="token punctuation">{</span>
    filterText<span class="token punctuation">:</span> <span class="token string">""</span>
  <span class="token punctuation">}</span><span class="token punctuation">;</span>

  <span class="token function-variable function">handleChange</span> <span class="token operator">=</span> event <span class="token operator">=></span> <span class="token punctuation">{</span>
    <span class="token keyword">this</span><span class="token punctuation">.</span><span class="token function">setState</span><span class="token punctuation">(</span><span class="token punctuation">{</span> filterText<span class="token punctuation">:</span> event<span class="token punctuation">.</span>target<span class="token punctuation">.</span>value <span class="token punctuation">}</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
  <span class="token punctuation">}</span><span class="token punctuation">;</span>

  <span class="token function">render</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token comment">// The render method on this PureComponent is called only if</span>
    <span class="token comment">// props.list or state.filterText has changed.</span>
    <span class="token keyword">const</span> filteredList <span class="token operator">=</span> <span class="token keyword">this</span><span class="token punctuation">.</span>props<span class="token punctuation">.</span>list<span class="token punctuation">.</span><span class="token function">filter</span><span class="token punctuation">(</span>
      item <span class="token operator">=></span> item<span class="token punctuation">.</span>text<span class="token punctuation">.</span><span class="token function">includes</span><span class="token punctuation">(</span><span class="token keyword">this</span><span class="token punctuation">.</span>state<span class="token punctuation">.</span>filterText<span class="token punctuation">)</span>
    <span class="token punctuation">)</span>

    <span class="token keyword">return</span> <span class="token punctuation">(</span>
      <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>Fragment</span><span class="token punctuation">></span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">onChange</span><span class="token script language-javascript"><span class="token punctuation">=</span><span class="token punctuation">{</span><span class="token keyword">this</span><span class="token punctuation">.</span>handleChange<span class="token punctuation">}</span></span> <span class="token attr-name">value</span><span class="token script language-javascript"><span class="token punctuation">=</span><span class="token punctuation">{</span><span class="token keyword">this</span><span class="token punctuation">.</span>state<span class="token punctuation">.</span>filterText<span class="token punctuation">}</span></span> <span class="token punctuation">/></span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>ul</span><span class="token punctuation">></span></span><span class="token punctuation">{</span>filteredList<span class="token punctuation">.</span><span class="token function">map</span><span class="token punctuation">(</span>item <span class="token operator">=></span> <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>li</span> <span class="token attr-name">key</span><span class="token script language-javascript"><span class="token punctuation">=</span><span class="token punctuation">{</span>item<span class="token punctuation">.</span>id<span class="token punctuation">}</span></span><span class="token punctuation">></span></span><span class="token punctuation">{</span>item<span class="token punctuation">.</span>text<span class="token punctuation">}</span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>li</span><span class="token punctuation">></span></span><span class="token punctuation">)</span><span class="token punctuation">}</span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>ul</span><span class="token punctuation">></span></span>
      <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>Fragment</span><span class="token punctuation">></span></span>
    <span class="token punctuation">)</span><span class="token punctuation">;</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>
      </div>
<p>The above approach is much cleaner and simpler than the derived state version. Occasionally, this won’t be good enough—filtering may be slow for large lists, and <code>PureComponent</code> won’t prevent rerenders if another prop were to change. To address both of these concerns, we could add a memoization helper to avoid unnecessarily re-filtering our list:</p>
<div class="gatsby-highlight">
      <pre class="gatsby-code-jsx"><code><span class="token keyword">import</span> memoize <span class="token keyword">from</span> <span class="token string">"memoize-one"</span><span class="token punctuation">;</span>

<span class="token keyword">class</span> <span class="token class-name">Example</span> <span class="token keyword">extends</span> <span class="token class-name">Component</span> <span class="token punctuation">{</span>
  <span class="token comment">// State only needs to hold the current filter text value:</span>
  state <span class="token operator">=</span> <span class="token punctuation">{</span> filterText<span class="token punctuation">:</span> <span class="token string">""</span> <span class="token punctuation">}</span><span class="token punctuation">;</span>

  <span class="token comment">// Re-run the filter whenever the list array or filter text changes:</span>
  filter <span class="token operator">=</span> <span class="token function">memoize</span><span class="token punctuation">(</span>
    <span class="token punctuation">(</span>list<span class="token punctuation">,</span> filterText<span class="token punctuation">)</span> <span class="token operator">=></span> list<span class="token punctuation">.</span><span class="token function">filter</span><span class="token punctuation">(</span>item <span class="token operator">=></span> item<span class="token punctuation">.</span>text<span class="token punctuation">.</span><span class="token function">includes</span><span class="token punctuation">(</span>filterText<span class="token punctuation">)</span><span class="token punctuation">)</span>
  <span class="token punctuation">)</span><span class="token punctuation">;</span>

  <span class="token function-variable function">handleChange</span> <span class="token operator">=</span> event <span class="token operator">=></span> <span class="token punctuation">{</span>
    <span class="token keyword">this</span><span class="token punctuation">.</span><span class="token function">setState</span><span class="token punctuation">(</span><span class="token punctuation">{</span> filterText<span class="token punctuation">:</span> event<span class="token punctuation">.</span>target<span class="token punctuation">.</span>value <span class="token punctuation">}</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
  <span class="token punctuation">}</span><span class="token punctuation">;</span>

  <span class="token function">render</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token comment">// Calculate the latest filtered list. If these arguments haven't changed</span>
    <span class="token comment">// since the last render, `memoize-one` will reuse the last return value.</span>
    <span class="token keyword">const</span> filteredList <span class="token operator">=</span> <span class="token keyword">this</span><span class="token punctuation">.</span><span class="token function">filter</span><span class="token punctuation">(</span><span class="token keyword">this</span><span class="token punctuation">.</span>props<span class="token punctuation">.</span>list<span class="token punctuation">,</span> <span class="token keyword">this</span><span class="token punctuation">.</span>state<span class="token punctuation">.</span>filterText<span class="token punctuation">)</span><span class="token punctuation">;</span>

    <span class="token keyword">return</span> <span class="token punctuation">(</span>
      <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>Fragment</span><span class="token punctuation">></span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">onChange</span><span class="token script language-javascript"><span class="token punctuation">=</span><span class="token punctuation">{</span><span class="token keyword">this</span><span class="token punctuation">.</span>handleChange<span class="token punctuation">}</span></span> <span class="token attr-name">value</span><span class="token script language-javascript"><span class="token punctuation">=</span><span class="token punctuation">{</span><span class="token keyword">this</span><span class="token punctuation">.</span>state<span class="token punctuation">.</span>filterText<span class="token punctuation">}</span></span> <span class="token punctuation">/></span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>ul</span><span class="token punctuation">></span></span><span class="token punctuation">{</span>filteredList<span class="token punctuation">.</span><span class="token function">map</span><span class="token punctuation">(</span>item <span class="token operator">=></span> <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>li</span> <span class="token attr-name">key</span><span class="token script language-javascript"><span class="token punctuation">=</span><span class="token punctuation">{</span>item<span class="token punctuation">.</span>id<span class="token punctuation">}</span></span><span class="token punctuation">></span></span><span class="token punctuation">{</span>item<span class="token punctuation">.</span>text<span class="token punctuation">}</span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>li</span><span class="token punctuation">></span></span><span class="token punctuation">)</span><span class="token punctuation">}</span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>ul</span><span class="token punctuation">></span></span>
      <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>Fragment</span><span class="token punctuation">></span></span>
    <span class="token punctuation">)</span><span class="token punctuation">;</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>
      </div>
<p>This is much simpler and performs just as well as the derived state version!</p>
<p>When using memoization, remember a couple of constraints:</p>
<ol>
<li>In most cases, you’ll want to <strong>attach the memoized function to a component instance</strong>. This prevents multiple instances of a component from resetting each other’s memoized keys.</li>
<li>Typically you’ll want to use a memoization helper with a <strong>limited cache size</strong> in order to prevent memory leaks over time. (In the example above, we used <code>memoize-one</code> because it only caches the most recent argument and result.)</li>
<li>None of the implementations shown in this section will work if <code>props.items</code> is recreated each time the parent component renders. But in most cases, this setup is appropriate.</li>
</ol>
<h2 id="in-closing">In closing</h2>
<p>In real world applications, components often contain a mix of controlled and uncontrolled behaviors. This is okay! If each value has a clear source of truth, you can avoid the anti-patterns mentioned above.</p>
<p>It is also worth re-iterating that <code>getDerivedStateFromProps</code> (and derived state in general) is an advanced feature and should be used sparingly because of this complexity. If your use case falls outside of these patterns, please share it with us on  or Twitter!</p>
---------------