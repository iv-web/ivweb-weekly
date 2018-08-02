## 文章索引
1、 <a href="#1react-v1642:-server-side-vulnerability-fix" >React v16.4.2: Server-side vulnerability fix</a><br/>
2、 <a href="#2user-experience-psychology-and-performance:-smashingconf-videos" >User Experience Psychology And Performance: SmashingConf Videos</a><br/>
3、 <a href="#3文章-预测性维护的回报与挑战" >文章： 预测性维护的回报与挑战</a><br/>
4、 <a href="#4文章-微服务接口限流的设计与思考附github框架源码" >文章： 微服务接口限流的设计与思考（附GitHub框架源码）</a><br/>
5、 <a href="#5文章-python那么火到底可以用来做什么" >文章： Python那么火，到底可以用来做什么？</a><br/>
6、 <a href="#6文章-用flutter开发一个完整的应用是怎样的体验" >文章： 用Flutter开发一个完整的应用是怎样的体验？</a><br/>
7、 <a href="#7文章-腾讯云如何快速从ipv4向ipv6演进" >文章： 腾讯云如何快速从IPv4向IPv6演进？</a><br/>
8、 <a href="#8amazon-workspaces现支持amazon-linux-2-desktop" >Amazon WorkSpaces现支持Amazon Linux 2 Desktop</a><br/>
9、 <a href="#9v神访谈区块链的工程突破点是提高可扩展性解决拥堵问题" >V神访谈：区块链的工程突破点是提高可扩展性，解决拥堵问题</a><br/>
10、 <a href="#10kafka-20重磅发布新特性独家解读" >Kafka 2.0重磅发布，新特性独家解读</a><br/>
11、 <a href="#11百度跨平台ai推理加速引擎anakin" >百度跨平台AI推理加速引擎：Anakin</a><br/>
12、 <a href="#12视频演讲-谷歌云端及机器学习在市场营销方面的应用" >视频演讲： 谷歌云端及机器学习在市场营销方面的应用</a><br/><h1 id="#title_0" >1、React v16.4.2: Server-side vulnerability fix</h1>

[https://reactjs.org/blog/2018/08/01/react-v-16-4-2.html](https://reactjs.org/blog/2018/08/01/react-v-16-4-2.html)
<p>We discovered a minor vulnerability that might affect some apps using ReactDOMServer. We are releasing a patch version for every affected React minor release so that you can upgrade with no friction. Read on for more details.</p>
<h2 id="short-description">Short Description</h2>
<p>Today, we are releasing a fix for a vulnerability we discovered in the <code class="gatsby-code-text">react-dom/server</code> implementation. It was introduced with the version 16.0.0 and has existed in all subsequent releases until today.</p>
<p>This vulnerability <strong>can only affect some server-rendered React apps.</strong> Purely client-rendered apps are <strong>not</strong> affected. Additionally, we expect that most server-rendered apps don’t contain the vulnerable pattern described below. Nevertheless, we recommend to follow the mitigation instructions at the earliest opportunity.</p>
<p>While we were investigating this vulnerability, we found similar vulnerabilities in a few other popular front-end libraries. We have coordinated this release together with  releases fixing the same issue. The tracking number for this vulnerability is <code class="gatsby-code-text">CVE-2018-6341</code>.</p>
<h2 id="mitigation">Mitigation</h2>
<p><strong>We have prepared a patch release with a fix for every affected minor version.</strong></p>
<h3 id="160x">16.0.x</h3>
<p>If you’re using <code class="gatsby-code-text">react-dom/server</code> with this version:</p>
<ul>
<li><code class="gatsby-code-text">react-dom@16.0.0</code></li>
</ul>
<p>Update to this version instead:</p>
<ul>
<li><code class="gatsby-code-text">react-dom@16.0.1</code> <strong>(contains the mitigation)</strong></li>
</ul>
<h3 id="161x">16.1.x</h3>
<p>If you’re using <code class="gatsby-code-text">react-dom/server</code> with one of these versions:</p>
<ul>
<li><code class="gatsby-code-text">react-dom@16.1.0</code></li>
<li><code class="gatsby-code-text">react-dom@16.1.1</code></li>
</ul>
<p>Update to this version instead:</p>
<ul>
<li><code class="gatsby-code-text">react-dom@16.1.2</code> <strong>(contains the mitigation)</strong></li>
</ul>
<h3 id="162x">16.2.x</h3>
<p>If you’re using <code class="gatsby-code-text">react-dom/server</code> with this version:</p>
<ul>
<li><code class="gatsby-code-text">react-dom@16.2.0</code></li>
</ul>
<p>Update to this version instead:</p>
<ul>
<li><code class="gatsby-code-text">react-dom@16.2.1</code> <strong>(contains the mitigation)</strong></li>
</ul>
<h3 id="163x">16.3.x</h3>
<p>If you’re using <code class="gatsby-code-text">react-dom/server</code> with one of these versions:</p>
<ul>
<li><code class="gatsby-code-text">react-dom@16.3.0</code></li>
<li><code class="gatsby-code-text">react-dom@16.3.1</code></li>
<li><code class="gatsby-code-text">react-dom@16.3.2</code></li>
</ul>
<p>Update to this version instead:</p>
<ul>
<li><code class="gatsby-code-text">react-dom@16.3.3</code> <strong>(contains the mitigation)</strong></li>
</ul>
<h3 id="164x">16.4.x</h3>
<p>If you’re using <code class="gatsby-code-text">react-dom/server</code> with one of these versions:</p>
<ul>
<li><code class="gatsby-code-text">react-dom@16.4.0</code></li>
<li><code class="gatsby-code-text">react-dom@16.4.1</code></li>
</ul>
<p>Update to this version instead:</p>
<ul>
<li><code class="gatsby-code-text">react-dom@16.4.2</code> <strong>(contains the mitigation)</strong></li>
</ul>
<p>If you’re using a newer version of <code class="gatsby-code-text">react-dom</code>, no action is required.</p>
<p>Note that only the <code class="gatsby-code-text">react-dom</code> package needs to be updated.</p>
<h2 id="detailed-description">Detailed Description</h2>
<p>Your app might be affected by this vulnerability only if both of these two conditions are true:</p>
<ul>
<li>Your app is <strong>being rendered to HTML using </strong>, and</li>
<li>Your app <strong>includes a user-supplied attribute name in an HTML tag.</strong></li>
</ul>
<p>Specifically, the vulnerable pattern looks like this:</p>
<div class="gatsby-highlight">
      <pre class="gatsby-code-jsx"><code class="gatsby-code-jsx"><span class="token keyword">let</span> props <span class="token operator">=</span> <span class="token punctuation">{</span><span class="token punctuation">}</span><span class="token punctuation">;</span>
<span class="gatsby-highlight-code-line">props<span class="token punctuation">[</span>userProvidedData<span class="token punctuation">]</span> <span class="token operator">=</span> <span class="token string">"hello"</span><span class="token punctuation">;</span>
</span><span class="token keyword">let</span> element <span class="token operator">=</span> <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span> <span class="token spread"><span class="token punctuation">{</span><span class="token punctuation">...</span><span class="token attr-value">props</span><span class="token punctuation">}</span></span> <span class="token punctuation">/></span></span><span class="token punctuation">;</span>
<span class="token keyword">let</span> html <span class="token operator">=</span> ReactDOMServer<span class="token punctuation">.</span><span class="token function">renderToString</span><span class="token punctuation">(</span>element<span class="token punctuation">)</span><span class="token punctuation">;</span></code></pre>
      </div>
<p>In order to exploit it, the attacker would need to craft a special attribute name that triggers an  vulnerability. For example:</p>
<div class="gatsby-highlight">
      <pre class="gatsby-code-jsx"><code class="gatsby-code-jsx"><span class="token keyword">let</span> userProvidedData <span class="token operator">=</span> <span class="token string">'>&lt;/div>&lt;script>alert("hi")&lt;/script>'</span><span class="token punctuation">;</span></code></pre>
      </div>
<p>In the vulnerable versions of <code class="gatsby-code-text">react-dom/server</code>, the output would let the attacker inject arbitrary markup:</p>
<div class="gatsby-highlight">
      <pre class="gatsby-code-html"><code class="gatsby-code-html"><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span> <span class="token punctuation">></span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">></span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">></span></span><span class="token script language-javascript"><span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"hi"</span><span class="token punctuation">)</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">></span></span></code></pre>
      </div>
<p>In the versions after the vulnerability was  (and before it was introduced), attributes with invalid names are skipped:</p>
<div class="gatsby-highlight">
      <pre class="gatsby-code-html"><code class="gatsby-code-html"><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span><span class="token punctuation">></span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">></span></span></code></pre>
      </div>
<p>You would also see a warning about an invalid attribute name.</p>
<p>Note that <strong>we expect attribute names based on user input to be very rare in practice.</strong> It doesn’t serve any common practical use case, and has other potential security implications that React can’t guard against.</p>
<h2 id="installation">Installation</h2>
<p>React v16.4.2 is available on the npm registry.</p>
<p>To install React 16 with Yarn, run:</p>
<div class="gatsby-highlight">
      <pre class="gatsby-code-bash"><code class="gatsby-code-bash">yarn add react@^16.4.2 react-dom@^16.4.2</code></pre>
      </div>
<p>To install React 16 with npm, run:</p>
<div class="gatsby-highlight">
      <pre class="gatsby-code-bash"><code class="gatsby-code-bash"><span class="token function">npm</span> <span class="token function">install</span> --save react@^16.4.2 react-dom@^16.4.2</code></pre>
      </div>
<p>We also provide UMD builds of React via a CDN:</p>
<div class="gatsby-highlight">
      <pre class="gatsby-code-html"><code class="gatsby-code-html"><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span> <span class="token attr-name">crossorigin</span> <span class="token attr-name">src</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>https://unpkg.com/react@16/umd/react.production.min.js<span class="token punctuation">"</span></span><span class="token punctuation">></span></span><span class="token script language-javascript"></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">></span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span> <span class="token attr-name">crossorigin</span> <span class="token attr-name">src</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>https://unpkg.com/react-dom@16/umd/react-dom.production.min.js<span class="token punctuation">"</span></span><span class="token punctuation">></span></span><span class="token script language-javascript"></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">></span></span></code></pre>
      </div>
<p>Refer to the documentation for .</p>
<h2 id="changelog">Changelog</h2>
<h3 id="react-dom-server">React DOM Server</h3>
<ul>
<li>
<p>Fix a potential XSS vulnerability when the attacker controls an attribute name (<code class="gatsby-code-text">CVE-2018-6341</code>). This fix is available in the latest <code class="gatsby-code-text">react-dom@16.4.2</code>, as well as in previous affected minor versions: <code class="gatsby-code-text">react-dom@16.0.1</code>, <code class="gatsby-code-text">react-dom@16.1.2</code>, <code class="gatsby-code-text">react-dom@16.2.1</code>, and <code class="gatsby-code-text">react-dom@16.3.3</code>. ()</p>
</li>
<li>
<p>Fix a crash in the server renderer when an attribute is called <code class="gatsby-code-text">hasOwnProperty</code>. This fix is only available in <code class="gatsby-code-text">react-dom@16.4.2</code>. ()</p>
</li>
</ul>
---------------
<h1 id="#title_1" >2、User Experience Psychology And Performance: SmashingConf Videos</h1>
The Smashing Editorial
[https://www.smashingmagazine.com/2018/08/smashingconf-ux-videos/](https://www.smashingmagazine.com/2018/08/smashingconf-ux-videos/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/08/smashingconf-ux-videos/" />
              <title>User Experience Psychology And Performance: SmashingConf Videos</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>User Experience Psychology And Performance: SmashingConf Videos</h1>
                  
                    
                    <address>The Smashing Editorial</address>
                  
                  <time datetime="2018-08-01T13:30:35&#43;02:00" class="op-published">2018-08-01T13:30:35+02:00</time>
                  <time datetime="2018-08-01T20:16:00&#43;00:00" class="op-modified">2018-08-01T20:16:00+00:00</time>
                </header>
                

<p>Today, we’d like to shine a light on two videos from our archives as we explore two very different approaches to User Experience (UX). The first explores how we relate our websites to the needs and situations of our visitors, trying to meet them where they are emotionally. The second is a detailed technical exploration into how we measure and track the data around performance as it relates to user experience.</p>

<p>The second video may seem unrelated to the first video; however, while the collecting and analyzing of data might seem very impersonal, the improvements we can make based on the information makes a real difference to the experience of the people we build our sites to serve.</p>

<h3 id="designing-powerful-user-experiences-with-psychology">Designing Powerful User Experiences With Psychology</h3>

<p>Recorded at the  earlier this year, Joe Leech explains <strong>how psychology impacts user experience</strong>. Joe explains the frustrations people using our products face, and the things happening in their everyday lives and environment that can make interacting with our websites and applications difficult. He goes on to help us understand how we can design in a way to <em>help</em> these visitors rather than <em>frustrate</em> them.</p>

<figure class="video-container"><iframe data-src="https://player.vimeo.com/video/266781642" width="600" height="480" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe></figure>

<h3 id="how-s-the-ux-on-the-web-really">How’s The UX On The Web, Really?</h3>

<p>Once you have created a great user experience, how do you know that it is really working well? Especially in terms of site performance, we can track how people are using our sites and examine that data to see what is really happening.</p>

<p>At the , Ilya Grigorik was the Mystery Speaker and spoke about the ways to assess performance in real terms, and benchmark your application against other destinations on the web.</p>

<figure class="video-container"><iframe data-src="https://player.vimeo.com/video/254834890" width="600" height="480" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe></figure>

<p>Enjoyed listening to these talks? There are many more  &mdash; see you there? ;-)</p>



<aside class="product-panel product-panel__tilted product-panel--book" data-audience="non-subscriber">
    <div class="container product-panel--book__container">
      <div class="panel__description panel__description--book">
    <p>With so much happening on the web, what should we really pay attention to? At . Oct <span class="small-caps">23–24</span>.</p>
      <a href="http://smashed.by/confpanelspeakers" class="btn btn--green btn--large">
        Check the speakers&nbsp;→
      </a>
      </div>
      <div class="panel__image panel__image--book">
        <a href="http://smashed.by/confpanelspeakers" class="books__book__image">
        <div class="books__book__img">
          <img src="https://res.cloudinary.com/indysigner/image/upload/v1529498640/sarah-drasner-opt_kaxhos.png" alt="SmashingConf New York 2018, with Dan Mall, Sara Soueidan, Sarah Drasner and many others." width="310" height="400">
        </div>
      </a>
      </div>
    </div>
  </aside>




<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(ra, il)</span>
</div>


              </article>
            </body>
          </html>
---------------
<h1 id="#title_2" >3、文章： 预测性维护的回报与挑战</h1>
Yuval Lavi
[http://www.infoq.com/cn/articles/predictive-maintenance-industrial-iot?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/predictive-maintenance-industrial-iot?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/predictive-maintenance-industrial-iot/zh/smallimage/predictive-maintenance-industrial-iot-logo-1531948040452-1532716055957.jpeg"/><p>预测性维护并不新鲜，但现在比以往任何时候都多，随着工业物联网（IIoT）和人工智能（AI）的发展，预测性维护可以为制造商节约大量的成本。</p> <i>By Yuval Lavi</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_3" >4、文章： 微服务接口限流的设计与思考（附GitHub框架源码）</h1>
王争
[http://www.infoq.com/cn/articles/microservice-interface-rate-limit?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/microservice-interface-rate-limit?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/microservice-interface-rate-limit/zh/smallimage/logo-AD-1532858486045.jpeg"/><p>微服务拆分之后，系统之间的调用关系错综复杂，平台的整体复杂熵升高，出错的概率、debug 问题的难度都高了好几个数量级。所以，服务治理便成了微服务的一个技术重点。服务治理本身的概念比较大，包括鉴权、限流、降级、熔断、监控告警等等，本文聚焦于限流，根据笔者的实战经验，分享一些对微服务接口限流的思考。</p> <i>By 王争</i>
---------------
<h1 id="#title_4" >5、文章： Python那么火，到底可以用来做什么？</h1>
YK Sugi
[http://www.infoq.com/cn/articles/what-can-you-do-with-python-the-3-main-applications?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/what-can-you-do-with-python-the-3-main-applications?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/what-can-you-do-with-python-the-3-main-applications/zh/smallimage/logo32-1532855688119.jpg"/><p>Python那么火，到底可以用来做什么？</p> <i>By YK Sugi</i> <i> Translated by 姚佳灵</i>
---------------
<h1 id="#title_5" >6、文章： 用Flutter开发一个完整的应用是怎样的体验？</h1>
Nick Manning
[http://www.infoq.com/cn/articles/what-it-was-like-to-write-a-full-blown-flutter-app?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/what-it-was-like-to-write-a-full-blown-flutter-app?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/what-it-was-like-to-write-a-full-blown-flutter-app/zh/smallimage/logo-1518043435207-1532855293148.jpeg"/><p>这将是一个很长的博客文章，因为有很多要涵盖：我将iOS应用程序移植到Flutter的经验；关于Flutter的思考；对Google团队的建议</p> <i>By Nick Manning</i> <i> Translated by Daniel_Hu</i>
---------------
<h1 id="#title_6" >7、文章： 腾讯云如何快速从IPv4向IPv6演进？</h1>
秦振华
[http://www.infoq.com/cn/articles/tencent-cloud-from-ipv4-to-ipv6?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/tencent-cloud-from-ipv4-to-ipv6?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/tencent-cloud-from-ipv4-to-ipv6/zh/smallimage/apachebeam-small-1533138880746.jpg"/><p>腾讯已经具备多年的IPv6技术积累，早在2013年就针对教育网的IPv6用户对部分腾讯业务应用访问，进行了底层网络架构的改造；近几年也是投入到IPv6和SDN、Segment Routing等新网络技术综合应用的研究。腾讯云由于受到用户需求的推动，早已开始云上业务IPv6改造的方案研究，现在则已经全面启动IPv6的支持计划。</p> <i>By 秦振华</i>
---------------
<h1 id="#title_7" >8、Amazon WorkSpaces现支持Amazon Linux 2 Desktop</h1>
Steef-Jan Wiggers
[http://www.infoq.com/cn/news/2018/07/aws-linux2-workspaces?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/aws-linux2-workspaces?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>随着新的Amazon WorkSpaces的推出，用户除了Windows 7和Windows 10之外，还可以使用Amazon Linux 2。Amazon Linux 2 WorkSpaces提供了一些不同的使用方式，包括Amazon Machine Image。</p> <i>By Steef-Jan Wiggers</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_8" >9、V神访谈：区块链的工程突破点是提高可扩展性，解决拥堵问题</h1>
COWEN
[http://www.infoq.com/cn/news/2018/08/Vitalik-block-chain-interview?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/08/Vitalik-block-chain-interview?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>从编程、经济学、密码学、分布式系统、信息理论以及数学等学科的交叉点角度来看，Vitalik Buterin 已经高潮将这些领域的见解整合成最成功且具备实践能力的应用程序——以太坊正是其中最典型的例子。而这一切努力，都是为了实现互联网的去中心化。 那么，您是否希望像 Vitalik 一样改变世界？</p> <i>By COWEN</i> <i> Translated by 核子可乐</i>
---------------
<h1 id="#title_9" >10、Kafka 2.0重磅发布，新特性独家解读</h1>
王国璋
[http://www.infoq.com/cn/news/2018/08/kafka2.0-new-features?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/08/kafka2.0-new-features?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>今天 Apache Kafka 项目的 2.0.0 版本正式发布了！距离 1.0 版本的发布，相距还不到一年。这一年不论是社区还是 Confluent 内部对于到底 Kafka 要向哪里发展都有很多讨论：从最初的标准消息系统，到现如今成为一个完整的包括导入导出和处理的流数据平台，从 0.8.2 一直到 1.0 版本，很多新特性和新部件被不断添加。但同时更重要的，关于“一个企业级的流式数据平台，到底有哪些必须的功能”这个问题，也被不断实践和理解。</p> <i>By 王国璋</i>
---------------
<h1 id="#title_10" >11、百度跨平台AI推理加速引擎：Anakin</h1>
蔡芳芳
[http://www.infoq.com/cn/news/2018/08/baidu-ai-anakin?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/08/baidu-ai-anakin?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>我们结合百度实际业务的需求、百度优秀工程师的研发能力以及行业合作伙伴的大力支持共同完成了百度自己的推理引擎Anakin v0.1.0。Anakin目前支持Intel-CPU、NVIDIA-GPU、AMD-GPU和ARM平台，后续将支持更多平台如寒武纪、比特大陆等。</p> <i>By 蔡芳芳</i>
---------------
<h1 id="#title_11" >12、视频演讲： 谷歌云端及机器学习在市场营销方面的应用</h1>
Isaac Tsai
[http://www.infoq.com/cn/presentations/application-of-google-cloud-and-machine-learning-in-marketing?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/application-of-google-cloud-and-machine-learning-in-marketing?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/presentations/application-of-google-cloud-and-machine-learning-in-marketing/zh/mediumimage/IsaacTsai270-1532435795464.jpg"/><p>机器学习即服务是一类自动化和半自动化云平台的统称，用来解决数据预处理、模型训练、模型评估、未来预测等一系列基础设施问题。谷歌云机器学习平台自从上线以来就以预训练的、可以直接调用的高效机器学习模型吸引了许多企业级用户在其上构建简单的机器学习应用。而去年下半年，谷歌就已宣布香港将正式成为谷歌云平台(GCP)的新区域。新区域将于2018年正式启动，它也将成为继新加坡、悉尼、台湾、东京和孟买之后，GCP在亚太地区（APAC）设立的第六个云区域。在香港设立数据中心也将意味着谷歌全球云区域在不断扩大。

本次演讲将通过对GCP平台的介绍，向大家分享深度学习框架的强大后援平台，其中内容包括：
终身价值简介；
如何构建基于TensorFlow的预测模型，分类器/回归器；
如何构建基于GCP的自动化预测系统；
如何把预测系统与内容分发系统相连，创造千人千面的用户体验；
成功案例分享。</p> <i>By Isaac Tsai</i>
---------------