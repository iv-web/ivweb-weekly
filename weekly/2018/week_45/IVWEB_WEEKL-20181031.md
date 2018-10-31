## 文章索引
1、 <a href="#1measuring-performance-with-server-timing" >Measuring Performance With Server Timing</a><br/>
2、 <a href="#2文章-敏捷教练市场发展状况" >文章： 敏捷教练市场发展状况</a><br/>
3、 <a href="#3迷你书-ai前线2018年10月" >迷你书： AI前线（2018年10月）</a><br/>
4、 <a href="#4cybermiles为google私用网络提供区块链支持" >CyberMiles为Google私用网络提供区块链支持</a><br/>
5、 <a href="#5angular-7支持虚拟滚动拖放cli-prompts等特性" >Angular 7支持虚拟滚动、拖放、CLI Prompts等特性</a><br/>
6、 <a href="#6亚马逊发布用于amazon-lightsail的托管数据库" >亚马逊发布用于Amazon Lightsail的托管数据库</a><br/><h1 id="#title_0" >1、Measuring Performance With Server Timing</h1>
Drew McLellan
[https://www.smashingmagazine.com/2018/10/performance-server-timing/](https://www.smashingmagazine.com/2018/10/performance-server-timing/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/10/performance-server-timing/" />
              <title>Measuring Performance With Server Timing</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>Measuring Performance With Server Timing</h1>
                  
                    
                    <address>Drew McLellan</address>
                  
                  <time datetime="2018-10-30T03:40:14&#43;02:00" class="op-published">2018-10-30T03:40:14+02:00</time>
                  <time datetime="2018-10-30T20:53:41&#43;00:00" class="op-modified">2018-10-30T20:53:41+00:00</time>
                </header>
                

<p>When undertaking any sort of performance optimisation work, one of the very first things we learn is that before you can improve performance you must first measure it. Without being able to measure the speed at which something is working, we can’t tell if the changes being made are improving the performance, having no effect, or even making things worse.</p>

<p>Many of us will be familiar with working on a performance problem at some level. That might be something as simple as trying to figure out why JavaScript on your page isn’t kicking in soon enough, or why images are taking too long to appear on bad hotel wifi. The answer to these sorts of questions is often found in a very familiar place: your browser’s developer tools.</p>

<p>Over the years developer tools have been improved to help us troubleshoot these sorts of performance issues in the front end of our applications. Browsers now even have performance audits built right in. This can help track down front end issues, but these audits can show up another source of slowness that we can’t fix in the browser. That issue is slow server response times.</p>

<h3 id="time-to-first-byte">Time to First Byte</h3>

<p>There’s very little browser optimisations can do to improve a page that is simply slow to build on the server. That cost is incurred between the browser making the request for the file and receiving the response. Studying your network waterfall chart in developer tools will show this delay up under the category of “Waiting (TTFB)”. This is how long the browser waits between making the request and receiving the response.</p>



<aside class="product-panel product-panel__tilted product-panel--book" data-audience="non-subscriber">
    <div class="container product-panel--book__container">
      <div class="panel__description panel__description--book">
    <p>Getting workflow <em>just</em> right ain’t an easy task. So are proper estimates. Or alignment among different departments. That’s why we’ve set up <strong>“this-is-how-I-work”-sessions</strong> — with smart cookies sharing what works well for them. A part of the , of course.</p>
      <a href="https://smashed.by/workflowpanelmembership" class="btn btn--green btn--large">
        Explore Smashing Membership&nbsp;↬
      </a>
      </div>
      <div class="panel__image panel__image--book">
        <a href="https://smashed.by/workflowpanelmembership" class="books__book__image">
        <div class="books__book__img">
          <img src="https://www.smashingmagazine.com/images/smashing-cat/smashing-tv-box-cat.svg" alt="Smashing TV, with live sessions for professional designers and developers." width="310" height="400">
        </div>
      </a>
      </div>
    </div>
  </aside>




<p>In performance terms this is know as <em>Time to First Byte</em> - the amount of time it takes before the server starts sending something the browser can begin to work with. Encompassed in that wait time is everything the server needs to do to build the page. For a typical site, that might involve routing the request to the correct part of the application, authenticating the request, making multiple calls to backend systems such as databases and so on. It could involve running content through templating systems, making API calls out to third party services, and maybe even things like sending emails or resizing images. Any work that the server does to complete a request is squashed into that TTFB wait that the user experiences in their browser.</p>

<figure>
<figcaption>Inspecting a document request shows the time the browser spends waiting for the response from the server.</figcaption>
</figure>

<p>So how do we reduce that time and start delivering the page more quickly to the user? Well, that’s a big question, and the answer depends on your application. That is the work of performance optimisation itself. What we need to do first is <em>measure</em> the performance so that the benefit of any changes can be judged.</p>

<h3 id="the-server-timing-header">The Server Timing Header</h3>

<p>The job of  is not to help you actually time activity on your server. You’ll need to do the timing yourself using whatever toolset your backend platform makes available to you. Rather, the purpose of Server Timing is to specify how those measurements can be communicated to the browser.</p>

<p>The way this is done is very simple, transparent to the user, and has minimal impact on your page weight. The information is sent as a simple set of HTTP response headers.</p>

<pre><code class="language-javascript">Server-Timing: db;dur=123, tmpl;dur=56</code></pre>

<p>This example communicates two different timing points named <code>db</code> and <code>tmpl</code>. These aren’t part of the spec - these are names that we’ve picked, in this case to represent some database and template timings respectively.</p>

<div class="sponsors__wide-place"></div>




<p>The <code>dur</code> property is stating the number of milliseconds the operation took to complete. If we look at the request in the Network section of Developer Tools, we can see that the timings have been added to the chart.</p>

<figure>
<figcaption>A new Server Timing section appears, showing the timings set with the Server-Timing HTTP header.</figcaption>
</figure>

<p>The <code>Server-Timing</code> header can take multiple metrics separated by commas:</p>

<pre><code class="language-javascript">Server-Timing: metric, metric, metric</code></pre>

<p>Each metric can specify three possible properties</p>

<ol>
<li>A short <strong>name</strong> for the metric (such as <code>db</code> in our example)</li>
<li>A <strong>duration</strong> in milliseconds (expressed as <code>dur=123</code>)</li>
<li>A <strong>description</strong> (expressed as <code>desc=&quot;My Description&quot;</code>)</li>
</ol>

<p>Each property is separated with a semicolon as the delimiter. We could add descriptions to our example like so:</p>

<pre><code class="language-javascript">Server-Timing: db;dur=123;desc="Database", tmpl;dur=56;desc="Template processing"</code></pre>

<figure>
<figcaption>The names are replaced with descriptions when provided.</figcaption>
</figure>

<p>The only property that is required is <code>name</code>. Both <code>dur</code> and <code>desc</code> are optional, and can be used optionally where required. For example, if you needed to debug a timing problem that was happening on one server or data center and not another, it might be useful to add that information into the response without an associated timing.</p>

<pre><code class="language-javascript">Server-Timing: datacenter;desc="East coast data center", db;dur=123;desc="Database", tmpl;dur=56;desc="Template processing”</code></pre>

<p>This would then show up along with the timings.</p>

<figure>
<figcaption>The "East coast data center" value is shown, even though it has no timings.</figcaption>
</figure>

<p>One thing you might notice is that the timing bars don’t show up in a waterfall pattern. This is simply because Server Timing doesn’t attempt to communicate the <em>sequence</em> of timings, just the raw metrics themselves.</p>

<h3 id="implementing-server-timing">Implementing Server Timing</h3>

<p>The exact implementation within your own application is going to depend on your specific circumstance, but the principles are the same. The steps are always going to be:</p>

<ol>
<li>Time some operations</li>
<li>Collect together the timing results</li>
<li>Output the HTTP header</li>
</ol>

<p>In pseudocode, the generation of response might look like this:</p>

<pre><code class="language-javascript">startTimer('db')
getInfoFromDatabase()  
stopTimer('db')

startTimer('geo')
geolocatePostalAddressWithAPI('10 Downing Street, London, UK')
endTimer('geo')

outputHeader('Server-Timing', getTimerOutput())</code></pre>

<p>The basics of implementing something along those lines should be straightforward in any language. A very simple PHP implementation could use the <code>microtime()</code> function for timing operations, and might look something along the lines of the following.</p>

<pre><code class="language-php">class Timers
{
    private $timers = [];

    public function startTimer($name, $description = null)
    {
        $this->timers[$name] = [
            'start' => microtime(true),
            'desc' => $description,
        ];
    }

    public function endTimer($name)
    {
        $this->timers[$name]['end'] = microtime(true);
    }

    public function getTimers()
    {
        $metrics = [];

        if (count($this->timers)) {
            foreach($this->timers as $name => $timer) {
                $timeTaken = ($timer['end'] - $timer['start']) * 1000;
                $output = sprintf('%s;dur=%f', $name, $timeTaken);

                if ($timer['desc'] != null) {
                    $output .= sprintf(';desc="%s"', addslashes($timer['desc']));
                } 
                $metrics[] = $output;
            }
        }

        return implode($metrics, ', ');
    }
}</code></pre>

<p>A test script would use it as below, here using the <code>usleep()</code> function to artificially create a delay in the running of the script to simulate a process that takes time to complete.</p>

<pre><code class="language-php">$Timers = new Timers();

$Timers->startTimer('db');
usleep('200000');
$Timers->endTimer('db');

$Timers->startTimer('tpl', 'Templating');
usleep('300000');
$Timers->endTimer('tpl');

$Timers->startTimer('geo', 'Geocoding');
usleep('400000');
$Timers->endTimer('geo');

header('Server-Timing: '.$Timers->getTimers());</code></pre>

<p>Running this code generated a header that looked like this:</p>

<pre><code class="language-javascript">Server-Timing: db;dur=201.098919, tpl;dur=301.271915;desc="Templating", geo;dur=404.520988;desc="Geocoding"</code></pre>

<figure>
<figcaption>The Server Timings set in the example show up in the Timings panel with the delays configured in our test script.</figcaption>
</figure>

<h3 id="existing-implementations">Existing Implementations</h3>

<p>Considering how handy Server Timing is, there are relatively few implementations that I could find. The  NPM package offers a convenient way to use Server Timing from Node projects.</p>

<p>If you use a middleware based PHP framework  for a few months, and I always leave a few basic timings enabled if you&rsquo;d like to see an example in the wild.</p>

<p>For browser support, the best I&rsquo;ve seen is in Chrome DevTools, and that&rsquo;s what I&rsquo;ve used for the screenshots in this article.</p>

<h3 id="considerations">Considerations</h3>

<p>Server Timing itself adds very minimal overhead to the HTTP response sent back over the wire. The header is very minimal and is generally safe to be sending without worrying about targeting to only internal users. Even so, it’s worth keeping names and descriptions short so that you’re not adding unnecessary overhead.</p>

<p>More of a concern is the extra work you might be doing on the server to time your page or application. Adding extra timing and logging can itself have an impact on performance, so it’s worth implementing a way to turn this on and off when required.</p>

<p>Using a Server Timing header is a great way to make sure all timing information from both the front-end and the back-end of your application are accessible in one location. Provided your application isn&rsquo;t too complex, it can be easy to implement and you can be up and running within a very short amount of time.</p>

<p>If you&rsquo;d like to read more about Server Timing, you might try the following:</p>

<ul>
<li>The </li>
<li>The  has examples and up to date detail of browser support</li>
<li>An  from the BBC iPlayer team about their use of Server Timing.</li>
</ul>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(ra)</span>
</div>


              </article>
            </body>
          </html>
---------------
<h1 id="#title_1" >2、文章： 敏捷教练市场发展状况</h1>
Alexander Frumkin, Michael de la Maza, Elaine Bulloch
[http://www.infoq.com/cn/articles/mapping-market-agile-coaches?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/mapping-market-agile-coaches?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/mapping-market-agile-coaches/zh/smallimage/mapping-market-agile-coaches-s-1538900483667-1539966150754.jpeg"/><p>2018年7月，包括本文两位作者在内的五位敏捷专家在旧金山会面，分析了敏捷教练市场的发展情况。 市场在短期内看起来非常强劲，但从长期看可能表现疲软。本文总结了会面的结果，讨论了敏捷教练的薪酬、工作地点以及敏捷教练市场的未来发展方向。</p> <i>By Alexander Frumkin, Michael de la Maza, Elaine Bulloch</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_2" >3、迷你书： AI前线（2018年10月）</h1>
InfoQ中文站
[http://www.infoq.com/cn/minibooks/AI-front-201810?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/minibooks/AI-front-201810?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/minibooks/AI-front-201810/zh/smallimage/100-1540881104146.jpg"/><p>本期主要内容：2019将成机器学习关键年：中美AI或有一战；人人恐惧AI寒冬，他却希望泡沫再破裂一次；数十亿用户的Facebook如何进行贝叶斯系统调优？NLP新纪元！如何看待轰炸阅读理解顶级测试的谷歌BERT模型？</p> <i>By InfoQ中文站</i>
---------------
<h1 id="#title_3" >4、CyberMiles为Google私用网络提供区块链支持</h1>
刘志勇
[http://www.infoq.com/cn/news/2018/10/CyberMiles-chainblock-for-Google?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/10/CyberMiles-chainblock-for-Google?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>互联网是巨大的，但它是成千上万个小型私用网络的大杂烩，通过数千个互联网服务提供商（ISP）和数十个大型运营商和服务提供商运营的骨干网连接起来。</p> <i>By 刘志勇</i>
---------------
<h1 id="#title_4" >5、Angular 7支持虚拟滚动、拖放、CLI Prompts等特性</h1>
Diogo Carleto
[http://www.infoq.com/cn/news/2018/10/angular-7?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/10/angular-7?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Google已经正式发布了Angular 7。Angular 7是Google推出的Web框架的一个新的主要版本。新版本带来了虚拟滚动、拖放、CLI Prompts等。</p> <i>By Diogo Carleto</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_5" >6、亚马逊发布用于Amazon Lightsail的托管数据库</h1>
Eldert Grootenboer
[http://www.infoq.com/cn/news/2018/10/amazon-lightsail-managed-db?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/10/amazon-lightsail-managed-db?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>亚马逊宣布了用于其简化的轻量级虚拟私有服务器Lightsail的托管数据库。增加该托管数据库的目的是，允许在Lightsail平台上以最少的工作量创建这些数据库，减轻用户的日常维护任务。</p> <i>By Eldert Grootenboer</i> <i> Translated by 谢丽</i>
---------------