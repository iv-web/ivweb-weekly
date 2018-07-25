## 文章索引
1、 <a href="#1视频演讲-基于html5开发高性能跨平台app" >视频演讲： 基于HTML5开发高性能跨平台APP</a><br/>
2、 <a href="#2json-web-token-入门教程" >JSON Web Token 入门教程</a><br/>
3、 <a href="#3bootstrap-413" >Bootstrap 4.1.3</a><br/>
4、 <a href="#4文章-无服务器计算能够颠覆关系型数据库市场吗" >文章： 无服务器计算能够颠覆关系型数据库市场吗？</a><br/>
5、 <a href="#5文章-同行评审阻碍或促进敏捷开发" >文章： 同行评审阻碍或促进敏捷开发</a><br/>
6、 <a href="#6文章-历数graalvm的十大用途" >文章： 历数GraalVM的十大用途</a><br/>
7、 <a href="#7文章-微信读书android阅读引擎卡顿监控测试" >文章： 微信读书（Android）阅读引擎卡顿监控测试</a><br/>
8、 <a href="#8文章-tidb中的混沌测试实践" >文章： TiDB中的混沌测试实践</a><br/>
9、 <a href="#9视频演讲-基于云场景架构设计的mysql分布式数据库" >视频演讲： 基于云场景架构设计的MySQL分布式数据库</a><br/>
10、 <a href="#10视频演讲-原生云架构的呼叫中心实践" >视频演讲： 原生云架构的呼叫中心实践</a><br/>
11、 <a href="#11fex-技术周刊---2018/07/23" >FEX 技术周刊 - 2018/07/23</a><br/>
12、 <a href="#12视频演讲-从安全和便捷谈一谈cis底层的技术实现" >视频演讲： 从安全和便捷谈一谈CIS底层的技术实现</a><br/>
13、 <a href="#13解密深度学习的营销场景应用阿里妈妈登场ijcai" >解密深度学习的营销场景应用，阿里妈妈登场IJCAI</a><br/>
14、 <a href="#14专访saumitra-buragohain-:-hortonworks数据平台30" >专访Saumitra Buragohain : Hortonworks数据平台3.0</a><br/>
15、 <a href="#15microsoft提供windows-10-iot-core-services预览版本" >Microsoft提供Windows 10 IoT Core Services预览版本</a><br/>
16、 <a href="#16azure虚拟wan和azure防火墙公开预览" >Azure虚拟WAN和Azure防火墙公开预览</a><br/>
17、 <a href="#17本地部署比saas更容易满足gdpr要求吗" >本地部署比SaaS更容易满足GDPR要求吗？</a><br/>
18、 <a href="#18谷歌开源量子计算框架cirq可在bristlecone处理器上运行" >谷歌开源量子计算框架Cirq，可在Bristlecone处理器上运行</a><br/>
19、 <a href="#19introducing-the-webp-manual" >Introducing “The WebP Manual”</a><br/>
20、 <a href="#20converting-images-to-webp" >Converting Images To WebP</a><br/>
21、 <a href="#21text-editing-tips-and-tricks-roundup" >Text Editing Tips And Tricks Roundup</a><br/><h1 id="#title_0" >1、视频演讲： 基于HTML5开发高性能跨平台APP</h1>
李德兴
[http://www.infoq.com/cn/presentations/developing-high-performance-cross-platform-app-based-on-html5?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/developing-high-performance-cross-platform-app-based-on-html5?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/presentations/developing-high-performance-cross-platform-app-based-on-html5/zh/mediumimage/lidexin270-1531482902968.jpg"/><p>Html5具有天然的跨平台特性，基于Html5混合技术架构的跨平台APP如今已然成为主流。本演讲将向大家分享我们在大规模使用Html5进行跨平台APP开发过程中，遇到过哪些坑，并讨论如何优化，将HTML5技术高效地应用于APP开发中，希望能给企业在业务快速落地过程中提供参考。</p> <i>By 李德兴</i>
---------------
<h1 id="#title_1" >2、JSON Web Token 入门教程</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2018/07/json_web_token-tutorial.html](http://www.ruanyifeng.com/blog/2018/07/json_web_token-tutorial.html)
<p>JSON Web Token（缩写 JWT）是目前最流行的跨域认证解决方案，本文介绍它的原理和用法。</p>

        <p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018072301.jpg" alt="" title="" /></p>

<h2>一、跨域认证的问题</h2>

<p>互联网服务离不开用户认证。一般流程是下面这样。</p>

<blockquote>
  <p>1、用户向服务器发送用户名和密码。</p>

<p>2、服务器验证通过后，在当前对话（session）里面保存相关数据，比如用户角色、登录时间等等。</p>

<p>3、服务器向用户返回一个 session_id，写入用户的 Cookie。</p>

<p>4、用户随后的每一次请求，都会通过 Cookie，将 session_id 传回服务器。</p>

<p>5、服务器收到 session_id，找到前期保存的数据，由此得知用户的身份。</p>
</blockquote>

<p>这种模式的问题在于，扩展性（scaling）不好。单机当然没有问题，如果是服务器集群，或者是跨域的服务导向架构，就要求 session 数据共享，每台服务器都能够读取 session。</p>

<p>举例来说，A 网站和 B 网站是同一家公司的关联服务。现在要求，用户只要在其中一个网站登录，再访问另一个网站就会自动登录，请问怎么实现？</p>

<p>一种解决方案是 session 数据持久化，写入数据库或别的持久层。各种服务收到请求后，都向持久层请求数据。这种方案的优点是架构清晰，缺点是工程量比较大。另外，持久层万一挂了，就会单点失败。</p>

<p>另一种方案是服务器索性不保存 session 数据了，所有数据都保存在客户端，每次请求都发回服务器。JWT 就是这种方案的一个代表。</p>

<h2>二、JWT 的原理</h2>

<p>JWT 的原理是，服务器认证以后，生成一个 JSON 对象，发回给用户，就像下面这样。</p>

<blockquote><pre><code class="language-javascript">
{
  "姓名": "张三",
  "角色": "管理员",
  "到期时间": "2018年7月1日0点0分"
}
</code></pre></blockquote>

<p>以后，用户与服务端通信的时候，都要发回这个 JSON 对象。服务器完全只靠这个对象认定用户身份。为了防止用户篡改数据，服务器在生成这个对象的时候，会加上签名（详见后文）。</p>

<p>服务器就不保存任何 session 数据了，也就是说，服务器变成无状态了，从而比较容易实现扩展。</p>

<h2>三、JWT 的数据结构</h2>

<p>实际的 JWT 大概就像下面这样。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018072304.jpg" alt="" title="" /></p>

<p>它是一个很长的字符串，中间用点（<code>.</code>）分隔成三个部分。注意，JWT 内部是没有换行的，这里只是为了便于展示，将它写成了几行。</p>

<p>JWT 的三个部分依次如下。</p>

<blockquote>
  <ul>
<li>Header（头部）</li>
<li>Payload（负载）</li>
<li>Signature（签名）</li>
</ul>
</blockquote>

<p>写成一行，就是下面的样子。</p>

<blockquote><pre><code class="language-javascript">
Header.Payload.Signature
</code></pre></blockquote>

<p><img src="https://www.wangbase.com/blogimg/asset/201807/bg2018072303.jpg" alt="" title="" /></p>

<p>下面依次介绍这三个部分。</p>

<h3>3.1 Header</h3>

<p>Header 部分是一个 JSON 对象，描述 JWT 的元数据，通常是下面的样子。</p>

<blockquote><pre><code class="language-javascript">
{
  "alg": "HS256",
  "typ": "JWT"
}
</code></pre></blockquote>

<p>上面代码中，<code>alg</code>属性表示签名的算法（algorithm），默认是 HMAC SHA256（写成 HS256）；<code>typ</code>属性表示这个令牌（token）的类型（type），JWT 令牌统一写为<code>JWT</code>。</p>

<p>最后，将上面的 JSON 对象使用 Base64URL 算法（详见后文）转成字符串。</p>

<h3>3.2 Payload</h3>

<p>Payload 部分也是一个 JSON 对象，用来存放实际需要传递的数据。JWT 规定了7个官方字段，供选用。</p>

<blockquote>
  <ul>
<li>iss (issuer)：签发人</li>
<li>exp (expiration time)：过期时间</li>
<li>sub (subject)：主题</li>
<li>aud (audience)：受众</li>
<li>nbf (Not Before)：生效时间</li>
<li>iat (Issued At)：签发时间</li>
<li>jti (JWT ID)：编号</li>
</ul>
</blockquote>

<p>除了官方字段，你还可以在这个部分定义私有字段，下面就是一个例子。</p>

<blockquote><pre><code class="language-javascript">
{
  "sub": "1234567890",
  "name": "John Doe",
  "admin": true
}
</code></pre></blockquote>

<p>注意，JWT 默认是不加密的，任何人都可以读到，所以不要把秘密信息放在这个部分。</p>

<p>这个 JSON 对象也要使用 Base64URL 算法转成字符串。</p>

<h3>3.3 Signature</h3>

<p>Signature 部分是对前两部分的签名，防止数据篡改。</p>

<p>首先，需要指定一个密钥（secret）。这个密钥只有服务器才知道，不能泄露给用户。然后，使用 Header 里面指定的签名算法（默认是 HMAC SHA256），按照下面的公式产生签名。</p>

<blockquote><pre><code class="language-javascript">
HMACSHA256(
  base64UrlEncode(header) + "." +
  base64UrlEncode(payload),
  secret)
</code></pre></blockquote>

<p>算出签名以后，把 Header、Payload、Signature 三个部分拼成一个字符串，每个部分之间用"点"（<code>.</code>）分隔，就可以返回给用户。</p>

<h3>3.4 Base64URL</h3>

<p>前面提到，Header 和 Payload 串型化的算法是 Base64URL。这个算法跟 Base64 算法基本类似，但有一些小的不同。</p>

<p>JWT 作为一个令牌（token），有些场合可能会放到 URL（比如 api.example.com/?token=xxx）。Base64 有三个字符<code>+</code>、<code>/</code>和<code>=</code>，在 URL 里面有特殊含义，所以要被替换掉：<code>=</code>被省略、<code>+</code>替换成<code>-</code>，<code>/</code>替换成<code>_</code> 。这就是 Base64URL 算法。 </p>

<h2>四、JWT 的使用方式</h2>

<p>客户端收到服务器返回的 JWT，可以储存在 Cookie 里面，也可以储存在 localStorage。</p>

<p>此后，客户端每次与服务器通信，都要带上这个 JWT。你可以把它放在 Cookie 里面自动发送，但是这样不能跨域，所以更好的做法是放在 HTTP 请求的头信息<code>Authorization</code>字段里面。</p>

<blockquote><pre><code class="language-javascript">
Authorization: Bearer &lt;token>
</code></pre></blockquote>

<p>另一种做法是，跨域的时候，JWT 就放在 POST 请求的数据体里面。</p>

<h2>五、JWT 的几个特点</h2>

<p>（1）JWT 默认是不加密，但也是可以加密的。生成原始 Token 以后，可以用密钥再加密一次。</p>

<p>（2）JWT 不加密的情况下，不能将秘密数据写入 JWT。</p>

<p>（3）JWT 不仅可以用于认证，也可以用于交换信息。有效使用 JWT，可以降低服务器查询数据库的次数。</p>

<p>（4）JWT 的最大缺点是，由于服务器不保存 session 状态，因此无法在使用过程中废止某个 token，或者更改 token 的权限。也就是说，一旦 JWT 签发了，在到期之前就会始终有效，除非服务器部署额外的逻辑。</p>

<p>（5）JWT 本身包含了认证信息，一旦泄露，任何人都可以获得该令牌的所有权限。为了减少盗用，JWT 的有效期应该设置得比较短。对于一些比较重要的权限，使用时应该再次对用户进行认证。</p>

<p>（6）为了减少盗用，JWT 不应该使用 HTTP 协议明码传输，要使用 HTTPS 协议传输。</p>

<h2>六、参考链接</h2>

<ul>
<li>， by Auth0</li>
<li>, by Bryan Manuele</li>
<li>, by dwyl</li>
</ul>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2018-07-23T17:10:58+08:00">2018年7月23日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>文集：</li>
<li>社交媒体：</li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------
<h1 id="#title_2" >3、Bootstrap 4.1.3</h1>

[http://blog.getbootstrap.com/2018/07/24/bootstrap-4-1-3/](http://blog.getbootstrap.com/2018/07/24/bootstrap-4-1-3/)
<p>Hot on the heels of v4.1.2, we’re shipping another patch release to address an issue with our browserslist config, fix some CSS bugs, make JavaScript plugins UMD ready, and improve form control rendering. Up next will be v4.2, our second minor release where we add some new features.</p>

<p>But first, here are the highlights for v4.1.3. Pay attention to the change to <code class="highlighter-rouge">.form-control</code>s which adds a new fixed <code class="highlighter-rouge">height</code>.</p>

<ul>
  <li><strong>Fixed:</strong> Moved the browserslist config from our <code class="highlighter-rouge">package.json</code> to a separate file to avoid unintended inherited browser settings across npm projects.</li>
  <li><strong>Fixed:</strong> Removed the <code class="highlighter-rouge">:not(:root)</code> selector from our <code class="highlighter-rouge">svg</code> Reboot styles, resolving an issue that caused all inline SVGs ignore <code class="highlighter-rouge">vertical-align</code> styles via single class due to higher specificity.</li>
  <li><strong>Fixed:</strong> Buttons in custom file inputs are once again clickable when focused.</li>
  <li><strong>Improved:</strong> Bootstrap’s plugins can now be imported separately in any contexts because they are now UMD ready.</li>
  <li><strong>Improved:</strong> <code class="highlighter-rouge">.form-control</code>s now have a fixed <code class="highlighter-rouge">height</code> to compensate for differences in computed height across different <code class="highlighter-rouge">type</code>s. This also fixes some IE alignment issues.</li>
  <li><strong>Improved:</strong> Added <code class="highlighter-rouge">Noto Color Emoji</code> to our system font stack for better rendering in Linux OSes.</li>
</ul>

<p>Checkout the full , so stay tuned for some awesome new features like toasts, dismissible badges, negative margins (responsive grid gutters!), spinners, and more!</p>

<p> to see the latest in action. The full release has been published to npm and will soon appear on the Bootstrap CDN and Rubygems.</p>

<p>&lt;3,<br />
</p>
---------------
<h1 id="#title_3" >4、文章： 无服务器计算能够颠覆关系型数据库市场吗？</h1>
David Yahalom
[http://www.infoq.com/cn/articles/is-serverless-computing-changer-for-the-relational-db-market?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/is-serverless-computing-changer-for-the-relational-db-market?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/is-serverless-computing-changer-for-the-relational-db-market/zh/smallimage/DNUN-logo-small-1532205476337.jpg"/><p>无服务器计算能够颠覆关系型数据库市场吗？</p> <i>By David Yahalom</i>
---------------
<h1 id="#title_4" >5、文章： 同行评审阻碍或促进敏捷开发</h1>
Patrick Londa
[http://www.infoq.com/cn/articles/peer-reviews-sandbag-propel?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/peer-reviews-sandbag-propel?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/peer-reviews-sandbag-propel/zh/smallimage/Peer-Reviews-logo-1531354656439-1532193999542.jpg"/><p>敏捷团队非常渴望反馈，但是他们得到反馈的速度已经够快了吗？如果你的同行评审过程没有恰当的结构化，那么它可能会拖累开发。本文介绍了团队如何通过采用结构化但灵活的流程加速开发、培养协作文化来解锁代码和文档评审的潜能。</p> <i>By Patrick Londa</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_5" >6、文章： 历数GraalVM的十大用途</h1>
Chris Seaton
[http://www.infoq.com/cn/articles/graalvm-ten-things?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/graalvm-ten-things?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/graalvm-ten-things/zh/smallimage/logo+%287%29-1532207937419.jpg"/><p>本文介绍了GraalVM的十大用途。</p> <i>By Chris Seaton</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_6" >7、文章： 微信读书（Android）阅读引擎卡顿监控测试</h1>
赵公卓
[http://www.infoq.com/cn/articles/weixin-reading-stuck-monitor-and-test?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/weixin-reading-stuck-monitor-and-test?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/weixin-reading-stuck-monitor-and-test/zh/smallimage/logo-1525205057798-1532427964528.jpeg"/><p>微信读书发布之初，从支持最基本的TXT纯文本书籍，再经过快速迭代同时支持EPUB格式书籍，整个过程当中阅读引擎的功能一直在快速膨胀，加上项目前期快速试错，进度紧张等原因，逐渐积累的卡顿问题开始凸显，通过对用户反馈的问题进行统计分析，读书时翻页卡顿的投诉占比高达51%，远超其它问题。为提升读书的用户体验和口碑，我们必须优化解决掉卡顿的问题。</p> <i>By 赵公卓</i>
---------------
<h1 id="#title_7" >8、文章： TiDB中的混沌测试实践</h1>
Siddon Tang
[http://www.infoq.com/cn/articles/chaos-practice-in-tidb?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/chaos-practice-in-tidb?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/chaos-practice-in-tidb/zh/smallimage/GettyImages-509049212+copy-1532206236983.jpg"/><p>本文介绍了TiDB中的混沌实践，并推荐了一些非常有用的混沌工具和平台。</p> <i>By Siddon Tang</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_8" >9、视频演讲： 基于云场景架构设计的MySQL分布式数据库</h1>
黄伟
[http://www.infoq.com/cn/presentations/mysql-distributed-database-based-on-cloud-scene-architecture?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/mysql-distributed-database-based-on-cloud-scene-architecture?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/presentations/mysql-distributed-database-based-on-cloud-scene-architecture/zh/mediumimage/huangwei270-1532434790580.jpg"/><p>在云时代，企业IT业务走向跨地区、全球化部署，IT应用软件逐渐云化、分布式化，要求数据库也要基于云场景架构设计，具备跨地区分布式部署的能力。这次演讲将总结传统数据库上云或云服务化遇到的问题，并深入介绍华为云原生分布式数据库的技术原理和最佳实践。</p> <i>By 黄伟</i>
---------------
<h1 id="#title_9" >10、视频演讲： 原生云架构的呼叫中心实践</h1>
安静波
[http://www.infoq.com/cn/presentations/call-center-practice-of-primary-cloud-architecture?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/call-center-practice-of-primary-cloud-architecture?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/presentations/call-center-practice-of-primary-cloud-architecture/zh/mediumimage/anjingbo270-1531535470843.jpg"/><p>在这个演讲中，将为各位介绍北京天润融通科技股份有限公司（Ti-net）基于AWS和阿里云的大型呼叫中心产品CTI-Cloud的架构。讲解呼叫中心全云的概念；阐述软件架构如何通过模块解耦、无状态化、负载均衡和云基础设施大容量组件的应用；如何实现跨区高可用，高性能和弹性伸缩；如何通过Direct Connect如何让网络服务实现高可用。结合云服务商过去一年中的功能演进，讲述天润融通对云服务的理解和，CTI-Cloud平台的架构演进是怎样受益于云架构的。 </p> <i>By 安静波</i>
---------------
<h1 id="#title_10" >11、FEX 技术周刊 - 2018/07/23</h1>

[http://fex.baidu.com/blog/2018/07/fex-weekly-23//](http://fex.baidu.com/blog/2018/07/fex-weekly-23//)
作者：zhangjunah <br> <h2 id="section">业界会议</h2>

<p><strong>极客公园 - Rebuild 2018</strong><br />
http://rebuild.geekpark.net/<br />
附：<br />
<br />
<br />
</p>

<h2 id="section-1">深阅读</h2>

<p><strong>Building the Google Photos Web UI</strong><br />
https://medium.com/google-design/google-photos-45b714dfbed1<br />
We wanted to try something ambitious and simultaneously support a full-width (justified) layout, preserve the aspect–ratio of each photo, be scrubbable (ie let you jump to any section of your archive), handle hundreds-of-thousands of photos, scroll at 60fps, and load near instantly. At the time no other photo gallery supported all of this, and to the best of my knowledge they still don’t. While many other galleries now support some of these features they usually square crop each photo to make the layout work. Here is a technical write up about how we solved those challenges, and a peek under the hood of how the web version of Google Photos works.</p>

<p><strong>The future of WebAssembly - A look at upcoming features and proposals</strong><br />
https://blog.scottlogic.com/2018/07/20/wasm-future.html<br />
WebAssembly is a performance optimised virtual machine that was shipped in all four major browsers earlier this year. It is a nascent technology and the current version is very much an MVP (minimum viable product). This blog post takes a look at the WebAssembly roadmap and the features it might be gain in the near future. I’ll try to keep this blog post relatively high-level, so I’ll skip over some of the more technical proposals, instead focusing on what they might mean for languages that target WebAssembly.</p>

<p><strong>Webmentions: Enabling Better Communication on the Internet</strong><br />
https://alistapart.com/article/webmentions-enabling-better-communication-on-the-internet<br />
Over 1 million Webmentions will have been sent across the internet since the specification was made a full Recommendation by the W3C—the standards body that guides the direction of the web—in early January 2017. That number is rising rapidly, and in the last few weeks I’ve seen a growing volume of chatter on social media and the blogosphere about these new “mentions” and the people implementing them.</p>

<p><strong>A one year PWA retrospective</strong><br />
https://medium.com/@Pinterest_Engineering/a-one-year-pwa-retrospective-f4a2f4129e05<br />
The idea of building a “Progressive Web App” (PWA) is not new, but its definition has changed with the emergence of key technologies like service workers. Now it’s finally possible to build great experiences in a mobile browser. Being an early adopter can be scary, so we’d like to share a brief overview of our experience building one of the world’s largest progressive web apps.</p>

<p><strong>CSS-in-JS: FTW || WTF?</strong><br />
https://vimeo.com/278439003<br />
Everyone’s talking about CSS-in-JS. It’s the Kim Kardashian of web development. And, as with Kimmie, opinions are polarised. To some, CSS in JS just makes sense: it’s local to your component, it can’t leak and, hey, I know how to write JavaScript and CSS is weird. To others, CSS-in-JS is an abomination that makes them want to emulate Kimmie and “release a fragrance” in disdain. Why are scripters so afraid of the cascade? Why the hesitance about inheritance? Let’s look at what CSS seems to lack, what the CSS-in-JS libraries can teach us, so we don’t do as Kim’s buttocks did and “Break the Internet”.</p>

<p><strong>可视化图形语法 G2 3.2 迭变</strong><br />
https://yuque.com/antv/blog/g2-3.2-release<br />
G2 是蚂蚁金服体验技术部  团队的重要产品之一，3.2 三大特性：让图表会讲故事，信息获取效率更高，图表一键换肤。</p>

<p><strong>美团客户端响应式框架 EasyReact 开源啦</strong><br />
https://tech.meituan.com/react_programming_framework_easyreact_opensource.html<br />
 是一款基于响应式编程范式的客户端开发框架，开发者可以使用此框架轻松地解决客户端的异步问题。目前 EasyReact 已在美团和大众点评客户端的部分业务中实践，并且持续迭代了一年多的时间。近日，我们决定开源这个项目的 iOS Objective-C 语言部分，希望能够帮助更多的开发者不断探索更广泛的业务场景，也欢迎更多的社区的开发者跟我们一起加强 EasyReact 的功能。</p>

<p><strong>WebIDE：在浏览器中写代码的时代即将来临</strong><br />
https://mp.weixin.qq.com/s?__biz=MjM5MDE0Mjc4MA==&amp;mid=2651008292&amp;idx=1&amp;sn=9ea83174885b14d39ba75e9cdc60f075<br />
在开发工具中，IDE 一向只是开发工具提供商的自留地，但它现在俨然已成为云计算厂商的目光焦点。WebIDE 到底是什么？它和以前的 IDE 有什么区别？它背后的技术是什么样的？为什么云计算厂商这么重视它？本文将对这些问题一一梳理。</p>

<p><strong>Operationalizing Node.js for Server Side Rendering</strong><br />
https://medium.com/airbnb-engineering/operationalizing-node-js-for-server-side-rendering-c5ba718acfc9<br />
As Airbnb builds more of its Frontend around Server Side Rendering, we took a look at how to optimize our server configurations to support it.</p>

<p><strong>N-API: Next generation APIs for Node.js native addons available across all LTS release lines</strong><br />
https://medium.com/the-node-js-collection/n-api-next-generation-apis-for-node-js-native-addons-available-across-all-lts-release-lines-4f35b781f00e<br />
N-API was put in as an experimental feature in Node.js 8.0, and after meeting a rigorous exit criteria defined by the community, it has been promoted to a supported feature in Node.js 10. It has also been backported to all LTS release lines. Having N-API with the same API across all LTS releases is a great milestone and we believe this is a significant step towards enabling its adoption. Many thanks to Gabriel Schulhof who put in a tremendous amount of effort to backport this feature across these versions.</p>

<p><strong>Location-Aware Distribution: Configuring servers at scale</strong><br />
https://code.fb.com/data-infrastructure/location-aware-distribution-configuring-servers-at-scale/<br />
In this post, we describe Location-Aware Distribution (LAD), a new peer-to-peer system that handles the distribution of configuration changes to millions of servers. We find that LAD is dramatically better at distributing large updates, 100 MB for LAD versus 5 MB previously, and also scales to support around 40,000 subscribers per distributor versus 2,500 subscribers before.</p>

<p><strong>Productivity at Scale: How We Improved Build Time by 400% at LinkedIn</strong><br />
https://engineering.linkedin.com/blog/2018/07/how-we-improved-build-time-by-400-percent<br />
One source of the productivity loss was the build system. Play Framework uses SBT as its default build system. SBT had served us well for a couple of years, however the growing size of our applications and LinkedIn’s scale started to push the build system to its limits. So, we started to look for alternatives and eventually decided to move to Gradle. A year later, as of this post, our largest Play app takes less than 5 minutes for IDE refresh, and build times are down from 60 minutes to 15 minutes. Here’s the story of how we got to this point.</p>

<p><strong>The Holy Grail Of Reusable Components: Custom Elements, Shadow DOM, And NPM</strong><br />
https://www.smashingmagazine.com/2018/07/reusable-components-custom-elements-shadow-dom-npm/<br />
This article looks at augmenting HTML with components that have built-in functionality and styles. We’ll also learn how to make these custom elements reusable across projects using NPM.</p>

<p><strong>The Best Explanation of JavaScript Reactivity</strong><br />
https://medium.com/vue-mastery/the-best-explanation-of-javascript-reactivity-fea6112dd80d<br />
Many front-end JavaScript frameworks (Ex. Angular, React, and Vue) have their own Reactivity engines. By understanding what reactivity is and how it works, you can improve your development skills and more effectively use JavaScript frameworks. In the video and the article below, we build the same sort of Reactivity you see in the Vue source code.</p>

<p><strong>JavaScript fundamentals before learning React</strong><br />
https://www.robinwieruch.de/javascript-fundamentals-react-requirements/<br />
After all my teachings about React, be it online for a larger audience or on-site for companies transitioning to web development and React, I always come to the conclusion that React is all about JavaScript. Newcomers to React but also myself see it as an advantage, because you carry your JavaScript knowledge for a longer time around compared to your React skills. 另附：</p>

<p><strong>Reflectly — From React Native to Flutter</strong><br />
https://medium.com/reflectly-engineering/reflectly-from-react-native-to-flutter-2e3dffced2ea<br />
Why we moved 500.000+ users to Flutter</p>

<p><strong>Reddit’s Voting UI in Vanilla vs React vs Vue vs Hyperapp</strong><br />
https://itnext.io/reddits-voting-ui-in-vanilla-vs-react-vs-vue-vs-hyperapp-shedding-light-on-the-purpose-of-spa-ee6b6ac9a8cc<br />
Many beginners may wonder what the purpose of SPA (Single Page Application) libraries/frameworks is. Why can’t they just use plain old JavaScript since it can achieve the same thing without the bloat? What is the purpose of them, and why are they so hyped up?</p>

<p><strong>REST was NEVER about CRUD</strong><br />
https://tyk.io/blog/rest-never-crud/<br />
A popular myth is that REST-based APIs must be CRUD-based – that couldn’t be further from the truth. It is simply one pattern in our API design toolbox. This article outlines a variety of additional patterns available for REST-based APIs. The intent isn’t to be fully exhaustive, but to open the options for API designers uncertain about how to apply designs beyond CRUD to REST-based APIs. 另附：.</p>

<p><strong>SRE fundamentals: SLIs, SLAs and SLOs</strong><br />
https://cloudplatform.googleblog.com/2018/07/sre-fundamentals-slis-slas-and-slos.html<br />
The concept of SRE starts with the idea that metrics should be closely tied to business objectives. We use several essential measurements—SLO, SLA and SLI—in SRE planning and practice.</p>

<p><strong>Into the Borg – SSRF inside Google production network</strong><br />
https://opnsec.com/2018/07/into-the-borg-ssrf-inside-google-production-network/<br />
In March 2018, I reported an XSS in Google Caja, a tool to securely embed arbitrary html/javascript in a webpage. In May 2018, after the XSS was fixed, I realised that Google Sites was using an unpatched version of Google Caja, so I looked if it was vulnerable to the XSS. However, the XSS wasn’t exploitable there.</p>

<p><strong>Windows Command-Line: Inside the Windows Console</strong><br />
https://blogs.msdn.microsoft.com/commandline/2018/07/10/windows-command-line-inside-the-windows-console/<br />
Welcome to the third post in the Windows Command-Line series. In this post, we’ll start to dig into the internals of the Windows Console and Command-Line, what it is, what it does … and what it doesn’t do. Posts in this series: , The Evolution of the Windows Command-Line(https://blogs.msdn.microsoft.com/commandline/2018/06/27/windows-command-line-the-evolution-of-the-windows-command-line/), Inside the Windows Console (this post).</p>

<p><strong>Getting to Go: The Journey of Go’s Garbage Collector</strong><br />
https://blog.golang.org/ismmkeynote<br />
This is the transcript from the keynote I gave at the International Symposium on Memory Management (ISMM) on June 18, 2018. For the past 25 years ISMM has been the premier venue for publishing memory management and garbage collection papers and it was an honor to have been invited to give the keynote.</p>

<p><strong>How to take 7 years to ship a beta</strong><br />
https://medium.com/@eigenbom/how-to-take-7-years-to-ship-a-beta-4fcfc2428d88<br />
It’s been almost 7 years since I quit my last job. Back in 2011 I was a freshly baked postgraduate in Melbourne. I was entering my 30’s and the indie game renaissance was in full swing. When my contract ended I decided to leave academia and pursue my own path in game development. I then began working on a game called Moonman. Fast forward some long years and that game, now called MoonQuest, has just been released on Steam Early Access and itch.io. So how can you take 7 years to make your game? Here are some important tips and tricks for taking your sweet time.</p>

<h2 id="section-2">新鲜货</h2>

<p><strong>ndb</strong><br />
https://github.com/GoogleChromeLabs/ndb<br />
ndb is an improved debugging experience for Node.js, enabled by Chrome DevTools. ndb requires Node &gt;=8.0.0. It works best with Node &gt;=10.</p>

<p><strong>npm v6.2.0</strong><br />
https://blog.npmjs.org/post/175871462900/v620<br />
In case you missed it, we moved!. We look forward to seeing future PRs landing in npm/cli in the future, and we’ll be chatting with you all in npm.community. Go check it out! This final release of npm@6.2.0 includes a couple of features that weren’t quite ready on time but that we’d still like to include. Enjoy!</p>

<p><strong>Introducing Data Transfer Project: an open source platform promoting universal data portability</strong><br />
https://opensource.googleblog.com/2018/07/introducing-data-transfer-project.html<br />
We’re taking our commitment to portability a step further. In tandem with Microsoft, Twitter, and Facebook we’re announcing the </p>

<p><strong>2018 Serverless Community Survey</strong><br />
https://serverless.com/blog/2018-serverless-community-survey-huge-growth-usage/<br />
huge growth in serverless usage.</p>

<p><strong>CanJS 5.0</strong><br />
https://www.bitovi.com/blog/canjs-5<br />
CanJS 5.0 is out with what you’ve been asking for — faster setup, webpack support, configure-less models, more powerful query logic, and dynamic components. Read on to find out how you can take advantage of these features in your app. 另附：</p>

<p><strong>Animating SVG Files With SVGator</strong><br />
https://www.smashingmagazine.com/2018/07/animating-svg-files-svgator/<br />
We’re pretty excited by tools such as SVGator, which really speed up the process when you’re making simple SVG animations. Here’s how easy it is to use and how you can get a great-looking animation in no time.</p>

<p><strong>TOAST UI Grid</strong><br />
http://ui.toast.com/tui-grid/<br />
A powerful widget which allows you to visualize and edit data via its table representation. The TOAST UI Grid is a component that can display, edit, add, and delete multiple data. You can append units to the data shown and use html to represent images and links instead of textual data.</p>

<p><strong>Phenomenon</strong><br />
https://github.com/vaneenige/phenomenon<br />
Phenomenon is a very small, low-level WebGL library that provides the essentials to deliver a high performance experience. Its core functionality is built around the idea of moving millions of particles around using the power of the GPU.</p>

<p><strong>localForage</strong><br />
https://github.com/localForage/localForage<br />
localForage is a fast and simple storage library for JavaScript. localForage improves the offline experience of your web app by using asynchronous storage (IndexedDB or WebSQL) with a simple, localStorage-like API. localForage uses localStorage in browsers with no IndexedDB or WebSQL support.</p>

<p><strong>asciichart</strong><br />
https://github.com/kroitor/asciichart<br />
Console ASCII line charts in pure Javascript (for NodeJS and browsers) with no dependencies. This code is absolutely free for any usage, you just do whatever the fuck you want.</p>

<p><strong>signale</strong><br />
https://github.com/klauscfhq/signale<br />
Hackable and configurable to the core, signale can be used for logging purposes, status reporting, as well as for handling the output rendering process of other node modules and applications.</p>

<p><strong>react-flame-graph</strong><br />
https://github.com/bvaughn/react-flame-graph<br />
React components for efficiently rendering large lists and tabular data.</p>

<p><strong>Polly.JS</strong><br />
https://github.com/Netflix/pollyjs<br />
Polly.JS is a standalone, framework-agnostic JavaScript library that enables recording, replaying, and stubbing HTTP interactions. Polly taps into native browser APIs to mock requests and responses with little to no configuration while giving you the ability to take full control of each request with a simple, powerful, and intuitive API.</p>

<p><strong>Nock - HTTP server mocking and expectations library for Node.js</strong><br />
https://github.com/nock/nock<br />
Nock can be used to test modules that perform HTTP requests in isolation. For instance, if a module performs HTTP requests to a CouchDB server or makes HTTP requests to the Amazon API, you can test that module in isolation. 另附：</p>

<p><strong>v8n</strong><br />
https://github.com/imbrn/v8n<br />
The ultimate JavaScript validation library you’ve ever needed. Dead simple fluent API. Customizable. Reusable.</p>

<p><strong>Z - Pattern Matching for Javascript</strong><br />
https://z-pattern-matching.github.io/<br />
The pattern matching is basically a switch on steroids, you can create powerful conditions such based on Object properties or Array content without manipulating the Object or Array itself. That amount of power leads you write functional, immutable, and expressive code instead imperative, which reduces a lot of complexity and bugs.</p>

<p><strong>Fastpack</strong><br />
http://fastpack.io/<br />
Why? JavaScript bundling can be faster. We can critically re-think the building infrastructure. We have proper tools. Writing OCaml is fun! 又一个轮子，不过这个的确是非常必要：JavaScript bundling can be faster.</p>

<p><strong>Scrolling Gradient</strong><br />
https://codepen.io/MadeByMike/pen/eKPZZz<br />
I decided to adapt the CSS Only Scroll Indicator technique to make a background gradient that canges with scroll position. The top right corner of the gradient changes while the bottom right remains the same. This works by overlaying 2 gradients, The first is a top-to-bottom gradient with a height of the content. This contains the colors you want to cycle through. The other is a top-left, to bottom-right gradient from transparent to a solid color. This gradient is fixed to the viewport dimensions and pulled behind text, similar to the scroll indicator.</p>

<p><strong>Teach Yourself Computer Science</strong><br />
https://teachyourselfcs.com/<br />
There are plenty of resources out there, but some are better than others. You don’t need yet another “200+ Free Online Courses” listicle. You need answers to these questions: Which subjects should you learn, and why? What is the best book or video lecture series for each subject? This guide is our attempt to definitively answer these questions.</p>

<h2 id="section-3">设计</h2>

<p><strong>Mobbin - Latest Mobile Design Patterns</strong><br />
https://mobbin.design/<br />
Mobbin is a hand-picked collection of the latest mobile design patterns from apps that reflect the best in design. Get inspiration from over 130 iOS apps and 6,000 patterns (screenshots from iPhone X) available on the platform. Sign up to save your favorite patterns.</p>

<p><strong>Your Body Text Is Too Small</strong><br />
https://blog.marvelapp.com/body-text-small/<br />
Why website body text should be bigger, and ways to optimize it.</p>

<p><strong>Mobile product designers will shape the future of 3D application design</strong><br />
https://www.invisionapp.com/blog/ux-designers-mobile-ar/<br />
When Google and Apple launched their mobile augmented reality (AR) platforms last summer, they effectively shifted the center of gravity for 3D application design and development. Before these launches, the main hardware platform focus had been virtual reality headsets and use cases that tended heavily toward gaming, filmmaking, architecture, and engineering.</p>

<p><strong>What I learned from chatting with 7,000 strangers on the internet</strong><br />
https://redditblog.com/2018/07/18/what-i-learned-from-chatting-with-7000-strangers-on-the-internet/<br />
our feedback helped us reshape the direction of chat on Reddit from one-to-one chat to private group chats and eventually to community-based chat rooms (and your jokes helped me get through many a long day). Chat rooms are now in beta and being released to more subreddits daily. Check out r/subchats or this post if you’d like to see how it works!</p>

<p><strong>What’s Appening? Gamification and Playfulness in Headspace</strong><br />
https://uxplanet.org/whats-appening-gamification-and-playfulness-in-headspace-f9cabfab6690<br />
Gamification is about using elements from game design in non-game situations to increase engagement and encourage desirable behaviors from users. What so many gamification designers seem to miss is that games aren’t just about points and achievements. They’re about being fun and playful. Headspace is a guided meditation app that uses game elements that increase and enable intrinsic motivation to create long-term change. In this article, I’m going to look at how they do that, as well as how they might be able to do that better.</p>

<p><strong>起点读书APP，背后的改版设计实录</strong><br />
https://www.uisdc.com/qidian-app-revised-design<br />
于一个较大型且历史包袱比较重的项目我们是如何去做改版的。</p>

<h2 id="section-4">产品及其它</h2>

<p><strong>Kiwix</strong><br />
http://www.kiwix.org/<br />
In many places internet can be slow, unreliable or even censored. Kiwix is an offline solution that allows you to access educational content like Wikipedia, the Wiktionary, TED talks and many others on any computer or smartphone - without the need for a live internet connection. We bring internet content to people without internet access. In schools, universities, prisons, and of course at home. Locally-stored content saves bandwidth and download time. Kiwix is small and efficient, works on low power or old computers. It also runs on a wide range of operating systems, from Android and iOS to Microsoft Windows, macOS and GNU/Linux distributions. 另附：.</p>

<p><strong>PeerTube, the “Decentralized YouTube”, succeeds in crowdfunding</strong><br />
https://quariety.com/2018/07/20/peertube-the-decentralized-youtube-succeeds-in-crowdfunding/<br />
It is done. With 53,100 euros collected in forty-two days, the PeerTube project originating in France blows through its initial goal. The principle is intriguing: a fully decentralized version of YouTube , whose computer code is freely accessible and editable, and where videos are shared between users without relying on a central system. Online since March 2018 in a beta version, the project should definitely take off by October, based on the money raised.</p>

<p><strong>How the Nintendo Entertainment System lives on in open source</strong><br />
https://blog.github.com/2018-07-16-how-the-nintendo-entertainment-system-lives-on-in-open-source-game-bytes/<br />
The NES was released 35 years ago today. While official NES games haven’t been released in over 20 years, a “homebrew” scene exists where developers are still creating NES games (playable on the original hardware or on emulators) in the original 6502 Assembly Language. Whether you grew up playing NES games, or your parents did, you’re bound to find something of interest—either in the gameplay or in the code—for some of these games below.</p>

<p><strong>网易云音乐王诗沐：方法论其实没那么重要</strong><br />
https://mp.weixin.qq.com/s?__biz=MzUyMDQ5NzI5Mg==&amp;mid=2247497915&amp;idx=1&amp;sn=46c2e72460e26100f35627457be81e7c<br />
对于一个产品经理来讲，最重要的不是抽象地去学习别人的方法论，而是通过自己的深度思考和用户洞察，不断总结和迭代自己的方法论，不断的形成闭环。网易云音乐上线这几年来，收到了很多赞誉。很多用户感觉云音乐特别懂用户的心，比他的妈妈还要懂，不仅能找到他喜欢的歌，还能通过音乐的互动与其他人产生共鸣。</p>
---------------
<h1 id="#title_11" >12、视频演讲： 从安全和便捷谈一谈CIS底层的技术实现</h1>
童航君
[http://www.infoq.com/cn/presentations/technical-realization-of-cis-bottom-layer?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/technical-realization-of-cis-bottom-layer?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/presentations/technical-realization-of-cis-bottom-layer/zh/mediumimage/tonghangjun270-1531487027556.jpg"/><p>CIS是一种serverless container的服务，能够帮助用户便捷、安全、低成本和灵活地使用容器，适用于批量计算场景，也能和现有Kubernetes 集群进行快速对接。议题将围绕安全和便捷两个角度探讨CIS底层的技术实现。</p> <i>By 童航君</i>
---------------
<h1 id="#title_12" >13、解密深度学习的营销场景应用，阿里妈妈登场IJCAI</h1>
Jackson
[http://www.infoq.com/cn/news/2018/07/IJCAI2018?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/IJCAI2018?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>当地时间 7 月 13 日——19 日，IJCAI 2018 在瑞典首都斯德哥尔摩顺利召开。在此次大会上，阿里巴巴旗下大数据营销平台阿里妈妈亮相并披露了在人工智能领域的发展方向，在开放与前沿两大关键词的引导下，凸显了其在行业引领 Ad Tech 的位置及实力。此外，阿里巴巴集团还以会展、Industry Talk、论文报告等方式展示了其在人工智能领域的技术能力与成果。</p> <i>By Jackson</i>
---------------
<h1 id="#title_13" >14、专访Saumitra Buragohain : Hortonworks数据平台3.0</h1>
Rags Srinivas
[http://www.infoq.com/cn/news/2018/07/hdp-30-ga?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/hdp-30-ga?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>InfoQ就Hadoop的总体情况，特别是HDP 3.0采访了Hortonworks的产品管理高级总监Saumitra Buragohain。</p> <i>By Rags Srinivas</i> <i> Translated by 姚佳灵</i>
---------------
<h1 id="#title_14" >15、Microsoft提供Windows 10 IoT Core Services预览版本</h1>
Sergio De Simone
[http://www.infoq.com/cn/news/2018/07/windows-iot-core-services-prev?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/windows-iot-core-services-prev?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Microsoft正在提供Windows 10 IoT Core OS全新收费服务的预览版本，该服务可以实现设备更新的管理以及设备健康评估。此外，这款新的服务对于之后发布的每个版本的OS都提供十年的技术支持。</p> <i>By Sergio De Simone</i> <i> Translated by 刘嘉洋</i>
---------------
<h1 id="#title_15" >16、Azure虚拟WAN和Azure防火墙公开预览</h1>
Steef-Jan Wiggers
[http://www.infoq.com/cn/news/2018/07/azure-virtual-wan-firewall?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/azure-virtual-wan-firewall?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>通过Azure虚拟WAN和Azure防火墙，微软将提供两项新服务，帮助客户实现网络现代化。Azure虚拟WAN服务将简化大范围的分路连接，而借助Azure防火墙，企业可以加强他们的云安全策略。两项服务现在都处于公开预览阶段。</p> <i>By Steef-Jan Wiggers</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_16" >17、本地部署比SaaS更容易满足GDPR要求吗？</h1>
Matt Campbell
[http://www.infoq.com/cn/news/2018/07/saas-compliance-gdpr-on-premise?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/saas-compliance-gdpr-on-premise?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>欧盟的GDPR引发了争论，有人认为迁移到本地解决方案更有利于满足GDPR的要求，而另一部分人则认为实现合规性与托管模型无关。</p> <i>By Matt Campbell</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_17" >18、谷歌开源量子计算框架Cirq，可在Bristlecone处理器上运行</h1>
Alan Ho
[http://www.infoq.com/cn/news/2018/07/quantcomputing-cirq?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/quantcomputing-cirq?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>谷歌开源量子计算框架Cirq，可在Bristlecone处理器上运行。</p> <i>By Alan Ho</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_18" >19、Introducing “The WebP Manual”</h1>
Markus Seyfferth
[https://www.smashingmagazine.com/2018/07/webp-manual/](https://www.smashingmagazine.com/2018/07/webp-manual/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/07/webp-manual/" />
              <title>Introducing “The WebP Manual”</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>Introducing “The WebP Manual”</h1>
                  
                    
                    <address>Markus Seyfferth</address>
                  
                  <time datetime="2018-07-24T12:00:00&#43;02:00" class="op-published">2018-07-24T12:00:00+02:00</time>
                  <time datetime="2018-07-24T10:53:31&#43;00:00" class="op-modified">2018-07-24T10:53:31+00:00</time>
                </header>
                

<p>What’s WebP in the first place? Can we actually use it today? And if yes, how exactly? The role of media in performance, specifically images, is of huge concern. Images are powerful. Engaging visuals evoke visceral feelings. They can provide key information and context to articles, or merely add humorous asides. They do anything for us that plain text just can’t by itself.</p>

<p>But when there’s too much imagery, it can be frustrating for users on slow connections, or run afoul of data plan allowances. In the latter scenario, that can cost users real money. This sort of inadvertent trespass can carry real consequences.</p>

<p>In this eBook, <strong>you’ll learn all about WebP</strong>: what it’s capable of, how it performs, how to convert images to the format in a variety of ways, and most importantly, how to use it. Of course — the eBook is — and always will be, .</p>

<ul>
  <li>Looking for a sneak peek? .</li>
</ul>

<p><em>84 pages. Written by . Cover Design by Ricardo Gimenes. Available in PDF, Kindle, and ePub formats.</em></p>

<figure><img src="https://res.cloudinary.com/indysigner/image/upload/v1531926616/webp-manual-ipad-opt_akcnzz.png" width="800" height="800" alt="Smashing Book 6" /></a></figure>

<div class="book-cta" data-handler="ContentTabs" data-mq="(max-width: 480px)">
  <nav class="content-tabs content-tabs--books">
  <ul>
     <li class="content-tab">
     <button class="btn btn--small btn--white btn--white--bordered">eBook</button>
     </li>
     <li class="content-tab">
     <button class="btn btn--small btn--white btn--white--bordered">Free for Members</button>
     </li>
   </ul>
 </nav>
  <div id="getthebook" class="book-cta__col book-cta__hardcover content-tab--content">
  <span class="book-cta__price"><span class="green">$14.90</span></span>
  <p class="book-cta__desc">PDF, ePUB, Kindle.</p>
  </div>
  <div class="book-cta__col book-cta__ebook content-tab--content">
  <span class="book-cta__price"><span class="green">$0.00 </span><span class="book-cta__price--del"><del>$14.90</del></span></span> 
   <p class="book-cta__desc">...along with .</em></small></p>
    </div>
</div>

<h3 id="a-id-toc-a-what-s-in-the-ebook">What’s In The eBook</h3>

<p>This guide will encourage you to experiment and see what’s possible with WebP:</p>

<ul>
<li><p><strong>WebP Basics</strong><br />
WebP images usually use less disk space when compared to other formats at reasonably comparable visual similarity. Depending on your site’s audience and the browsers they use, this is an opportunity to deliver less data-intensive user experiences for a significant segment of your audience.</p></li>

<li><p><strong>Performance</strong><br />
We’ll cover how both lossy and lossless WebP compare to JPEGs and PNGs exported by a number of image encoders.</p></li>

<li><p><strong>Converting Images To WebP</strong> ()<br />
This can be done in a myriad of ways, from something as simple as exporting from your preferred design program, by using Cloudinary and similar services, and even in Node.js-based build systems. Here, we’ll cover all avenues.</p></li>

<li><p><strong>Using WebP Images</strong><br />
Because WebP isn’t supported in all browsers just yet, you’ll need to learn how to use it that sites and applications gracefully fall back to established formats when WebP support is lacking. Here, we’ll discuss the many ways you can use WebP responsibly, starting by detecting browser support in the <em>Accept</em> request header.</p></li>
</ul>

<h3 id="a-id-author-a-about-the-author">About The Author</h3>

<p><img style="float: right; padding: 1em;border-radius: 110px;" src="https://res.cloudinary.com/indysigner/image/upload/v1531928782/jeremy-wagner-round_qqpwwr.jpg" width="150" height="150" alt="Dan Mall" />
Jeremy Wagner is a performance-obsessed front-end developer, author and speaker living and working in the frozen wastes of Saint Paul, Minnesota. He is also the author of <em>Web Performance in Action</em>, a web developer’s companion guide for creating fast websites. You can find him on Twitter @malchata, or read .</p>

<p><h3 style="padding-top: 1.5em;border-top: 3px solid #e5e5e5;">Here’s Why This eBook Is For You</h3>
<p><em>The WebP Manual</em> will get you ready for the new image format that is capable to significantly less data-intensive user experiences for a majority of your audience:</p>
<ul>
<li>Learn how lossy and lossless WebP compare to JPEGs and PNGs exported by a number of image encoders.</li>
<li>Learn which services and plugins you can use to export or convert images to WebP with your preferred design tool or command line tool.</li>
<li>Learn how to can use WebP in production, and how to implement proper fallbacks for browsers that don’t support WebP just yet.</li>
<li>Learn how to use the full potential of the WebP format. It will substantially improve loading performance for many of your users, customers, and clients, and it will become one of your favorite tools for making websites as lean as possible. </li>
</ul></p>

<p><em>The eBook is  (you can cancel anytime, of course)</em>.</p>

<figure><img src="https://res.cloudinary.com/indysigner/image/upload/v1531932476/ebook-inside-hires-white_alqspp.jpg" width="800" height="800" alt="Smashing Book 6" /></a></figure>

<div class="book-cta" data-handler="ContentTabs" data-mq="(max-width: 480px)">
  <nav class="content-tabs content-tabs--books">
  <ul>
     <li class="content-tab">
     <button class="btn btn--small btn--white btn--white--bordered">eBook</button>
     </li>
     <li class="content-tab">
     <button class="btn btn--small btn--white btn--white--bordered">Free for Members</button>
     </li>
   </ul>
 </nav>
  <div id="getthebook" class="book-cta__col book-cta__hardcover content-tab--content">
  <span class="book-cta__price"><span class="green">$14.90</span></span>
  <p class="book-cta__desc">PDF, ePUB, Kindle.</p>
  </div>
  <div class="book-cta__col book-cta__ebook content-tab--content">
  <span class="book-cta__price"><span class="green">$0.00 </span><span class="book-cta__price--del"><del>$14.90</del></span></span> 
   <p class="book-cta__desc">...along with .</em></small></p>
    </div>
</div>

              </article>
            </body>
          </html>
---------------
<h1 id="#title_19" >20、Converting Images To WebP</h1>
Jeremy Wagner
[https://www.smashingmagazine.com/2018/07/converting-images-to-webp/](https://www.smashingmagazine.com/2018/07/converting-images-to-webp/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/07/converting-images-to-webp/" />
              <title>Converting Images To WebP</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>Converting Images To WebP</h1>
                  
                    
                    <address>Jeremy Wagner</address>
                  
                  <time datetime="2018-07-24T11:00:30&#43;02:00" class="op-published">2018-07-24T11:00:30+02:00</time>
                  <time datetime="2018-07-24T10:53:31&#43;00:00" class="op-modified">2018-07-24T10:53:31+00:00</time>
                </header>
                

<p>To use WebP, you’ll first need to convert your existing images to the format. This can be done in a myriad of ways, from something as simple as exporting from your preferred design program, to cloud services, to the official cwebp encoder, and even in Node.js-based build systems. Here, we’ll cover all avenues.</p>

<h3 id="sketch">Sketch</h3>

<p>Sketch is able to export any resource in a design document to WebP natively. To export an image to WebP, select a resource on the canvas, open the <strong>Export</strong> panel on the right hand side, and choose “WEBP” in the format dropdown.</p>











<figure >
	
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7acdc6b5-f289-4b7d-a3ad-9c70b1e18a8d/01-converting-images-to-webp-chapter.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7acdc6b5-f289-4b7d-a3ad-9c70b1e18a8d/01-converting-images-to-webp-chapter.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7acdc6b5-f289-4b7d-a3ad-9c70b1e18a8d/01-converting-images-to-webp-chapter.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7acdc6b5-f289-4b7d-a3ad-9c70b1e18a8d/01-converting-images-to-webp-chapter.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7acdc6b5-f289-4b7d-a3ad-9c70b1e18a8d/01-converting-images-to-webp-chapter.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7acdc6b5-f289-4b7d-a3ad-9c70b1e18a8d/01-converting-images-to-webp-chapter.png"
			sizes="100vw"
			alt="The resource export panel in Sketch, with the WebP format chosen in the format dropdown."
		/>
	

	
		<figcaption class="op-vertical-bottom">
			The resource export panel in Sketch, with the WebP format chosen in the format dropdown. ()
		</figcaption>
	
</figure>


<p>After you make your selection, click the <strong>Export Bitmap&hellip;</strong> button. The resulting dialog will predictably ask where you want the image to be exported to. Within that dialog, a slider will appear at the bottom that prompts you to specify the quality of the WebP image from 0 to 100, implying the output is lossy WebP.</p>











<figure >
	
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/97df1aea-4a37-41ef-87c7-10910ebd9725/02-converting-images-to-webp-chapter.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/97df1aea-4a37-41ef-87c7-10910ebd9725/02-converting-images-to-webp-chapter.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/97df1aea-4a37-41ef-87c7-10910ebd9725/02-converting-images-to-webp-chapter.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/97df1aea-4a37-41ef-87c7-10910ebd9725/02-converting-images-to-webp-chapter.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/97df1aea-4a37-41ef-87c7-10910ebd9725/02-converting-images-to-webp-chapter.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/97df1aea-4a37-41ef-87c7-10910ebd9725/02-converting-images-to-webp-chapter.png"
			sizes="100vw"
			alt="A slider shown in sketch for exporting lossy WebP images. The slider goes from 0 to 100, where 0 is the lowest quality, and 100 is the highest."
		/>
	

	
		<figcaption class="op-vertical-bottom">
			The quality slider in the export dialog when exporting a resource to WebP. ()
		</figcaption>
	
</figure>


<p>If you’re using design software to export to WebP, Sketch is probably one of the easier programs to use. Although, there <em>are</em> other programs capable of doing this, such as Photoshop.</p>

<h3 id="photoshop">Photoshop</h3>

<p>Exporting images to WebP in Photoshop is possible, but is not as convenient as in Sketch. You’ll need to rely on a plug-in to get the job done. The good news, however, is that the Photoshop plug-in <em>does</em> give you a bit more flexibility than Sketch does. To obtain the Photoshop plug-in for exporting WebP images, visit the  and grab the version for your system. Once installed, start Photoshop and open an image. Once opened, you can export an image to WebP through the <strong>Save As&hellip;</strong> dialog. At the bottom of the dialog where you choose a format, you’ll notice two options: WebP, and WebP Lossless.</p>

<p>What happens from here depends on what you choose in the dropdown. If you choose WebP Lossless, the file will be exported, and that will be that. If you choose WebP, however, you’ll be presented with a dialog with several configuration options:</p>











<figure >
	
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/009581bc-a12d-4c6a-85e7-c648020d0ea1/03-converting-images-to-webp-chapter.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/009581bc-a12d-4c6a-85e7-c648020d0ea1/03-converting-images-to-webp-chapter.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/009581bc-a12d-4c6a-85e7-c648020d0ea1/03-converting-images-to-webp-chapter.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/009581bc-a12d-4c6a-85e7-c648020d0ea1/03-converting-images-to-webp-chapter.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/009581bc-a12d-4c6a-85e7-c648020d0ea1/03-converting-images-to-webp-chapter.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/009581bc-a12d-4c6a-85e7-c648020d0ea1/03-converting-images-to-webp-chapter.png"
			sizes="100vw"
			alt="A dialogue in Photoshop for the WebP plugin showing various options for export quality, denoising, and filtering."
		/>
	

	
		<figcaption class="op-vertical-bottom">
			The Photoshop plug-in’s lossy WebP export dialog. ()
		</figcaption>
	
</figure>


<p>In most cases, you’ll merely adjust the encoding quality, but feel free to experiment with the filtering, denoising, and sharpness options to obtain the desired result. Unfortunately, this plug-in lacks the ability to show a preview of the image before you save it. If you’re accustomed to using the <strong>Save for Web</strong> tool, this is kind of a bummer, as you’ll have to go at it blind.</p>

<p>Of course, if you’re not a fan of tinkering around in imaging software, the easiest possible option for using WebP might just be to rely on an image optimization CDN. Cloudinary is one such service.</p>

<h3 id="cloudinary">Cloudinary</h3>

<p>Using WebP is not a frictionless experience, and the easiest way to use it is to never have to convert to the format on your own in the first place. Some online services can do this work for you, and Cloudinary is one of them.</p>

<p>You only need to upload images to the service. From there, Cloudinary will optimize your images for you. These optimizations are highly customizable, and one such optimization is to automatically serve whatever image format is optimal for your users. If you use Cloudinary to serve your site’s images <em>and</em> your visitors are using WebP-capable browsers, Cloudinary takes on the hassle of serving WebP images for you, provided you choose the proper URL parameters. When you upload an image, Cloudinary’s control panel will provide a URL to your image that looks something like this:</p>

<pre><code class="language-bash">https://res.cloudinary.com/drp9iwjqz/image/upload/v1508291830/jeremywagner.me/using-webp-images/tacos-2x.jpg</code></pre>

<p>Using any number of URL parameters, you can change how Cloudinary serves images to you, including serving WebP images automatically to clients that can best handle them. The parameter that controls this behavior is _f<em>auto</em>, which tells Cloudinary to automatically pick the best format for the client issuing the request. Parameters are added after the <em>/upload/</em> portion in the URL like so:</p>

<pre><code class="language-bash">https://res.cloudinary.com/drp9iwjqz/image/upload/f_auto/v1508291830/jeremywagner.me/using-webp-images/tacos-2x.jpg</code></pre>

<p>Though Cloudinary preserves the extension, you can tell what the content type of the image is by looking at the image’s <em>Content-Type</em> response header. If you’re using a browser that supports WebP, that header will have a value of <em>image/webp</em>. Of course, Cloudinary is capable of more than simply serving the best format for a given browser. You can combine multiple parameters by separating them with commas. For example, here’s how you could tell Cloudinary to automatically pick the best format <em>and</em> the best quality setting (represented by <code>q_auto</code>):</p>

<pre><code class="language-bash">https://res.cloudinary.com/drp9iwjqz/image/upload/f_auto,q_auto/v1508291830/jeremywagner.me/using-webp-images/tacos-2x.jpg</code></pre>

<p>To learn more about what Cloudinary is capable of, .</p>

<p>While Cloudinary is a convenient tool that does the work of image optimization for you, you may yet feel compelled to encode your own images. And there are plenty of good reasons to do so! Beyond using imaging software, you can accomplish this with perhaps the most flexibility by using the Google’s official WebP command line encoder.</p>

<h3 id="the-official-cwebp-command-line-encoder">The Official cwebp Command Line Encoder</h3>

<p>The official tool for encoding images to the WebP format is Google’s own command line utility. While a command line program may not be as easy to use as a graphical interface, it offers much more flexibility in controlling the output. Most graphical front-ends that export to WebP abstract away features that don’t neatly fit into a dialog, and thus aren’t the best tools for achieving the best result for your site. Before you can use the command line encoder, however, you’ll need to install it.</p>

<h4 id="installing">Installing</h4>

<p>Your installation method will depend on your operating system. The easiest way to install the WebP encoder will be through your operating system’s package manager. macOS users can install the encoder and related tools using the :</p>

<pre><code class="language-bash">brew install webp
</code></pre>

<p>Windows users can install the encoder using :</p>

<pre><code class="language-bash">choco install webp
</code></pre>

<p>Users of Red Hat and Red Hat-derived Linux distros such as CentOS or Fedora can use yum to install the encoder:</p>

<pre><code class="language-bash">yum install libwebp-tools
</code></pre>

<p>Other platforms may use different package managers (such as <code>apt-get</code> for Debian Linux), but the mere presence of a package manager doesn’t mean it will provide a way to install the encoder. If your operating system package manager somehow fails you, the WebP encoder is available via  (npm):</p>

<p>If none of these options work for you,  and compile your own binaries. It’s a bit onerous, but the option <em>is</em> there.</p>

<p>With the encoder installed, let’s take a look at some quick examples of how you can use it.</p>

<h4 id="simple-command-line-examples">Simple Command Line Examples</h4>

<p>The WebP encoder can be invoked with the <code>cwebp</code> command. For starters, let’s examine what is arguably the most common use case of converting an image to lossy WebP:</p>

<pre><code class="language-bash">cwebp -q 75 source.png -o output.webp
</code></pre>

<p>This command takes a PNG and outputs it to lossy WebP by way of the <code>-o</code> parameter. By default, the encoder outputs lossy WebP images, and the quality of the output can be set from 0 to 100 via the <code>-q</code> parameter. The default lossy quality setting is 75.</p>

<p>You may remember reading earlier that WebP is capable of full alpha transparency, even for lossy images. You can control the quality of this transparency in the same fashion via the <code>-alpha_q</code> parameter:</p>

<pre><code class="language-bash">cwebp -q 75 -alpha_q 10 source.png -o output.web
</code></pre>

<p><code>-alpha_q</code> applies lossy compression to the transparency in an image. The default for <code>-alpha_q</code> is 100, which is lossless. You can further reduce output size by lowering this value, which will apply lossy compression to the transparency, but lowering it <em>too</em> much can significantly degrade the quality of transparent regions in the image.</p>











<figure >
	
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/642ec547-e4b8-43ae-b257-67f42d2c4938/04-converting-images-to-webp-chapter.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/642ec547-e4b8-43ae-b257-67f42d2c4938/04-converting-images-to-webp-chapter.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/642ec547-e4b8-43ae-b257-67f42d2c4938/04-converting-images-to-webp-chapter.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/642ec547-e4b8-43ae-b257-67f42d2c4938/04-converting-images-to-webp-chapter.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/642ec547-e4b8-43ae-b257-67f42d2c4938/04-converting-images-to-webp-chapter.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/642ec547-e4b8-43ae-b257-67f42d2c4938/04-converting-images-to-webp-chapter.png"
			sizes="100vw"
			alt="A side-by-side comparison of two transparent WebP images of a cloud on a checkered background. The image on the left is a lossy WebP exported at a quality of 75 at 26.88 kB. The image on the right is a lossy WebP exported at the same quality, but with a much poorer transparency quality of 10/100 (albeit at a much smaller file size of 8.45 kB)."
		/>
	

	
		<figcaption class="op-vertical-bottom">
			A lossy transparent WebP with best transparency quality (left), and a lossy transparent WebP with low transparency quality (right). Note the loss of fine details at the cloud’s edges. ()
		</figcaption>
	
</figure>


<p>If you’re conservative in adjusting <code>-alpha_q</code>, you can reduce the size of transparent images even further, but be sure to examine the output to ensure it’s acceptable to you. If you’re automating conversion of images (through a shell script, for example), you might want to shy away from setting this parameter at all. It’s also worth noting that <code>-alpha_q</code> has no effect when encoding lossless WebP images.</p>

<p>We’ve discussed encoding lossy WebP images with cwebp, but what if you want to export to lossless WebP? Just use the <code>-lossless</code> option:</p>

<pre><code class="language-bash">cwebp -lossless source.png -o output.webp
</code></pre>

<p>Depending on image content, you may not realize as much of a reduction in output file size when compared to lossy WebP. You <em>can</em> control the aggressiveness of the compression via the <code>-z</code> parameter, though:</p>

<pre><code class="language-bash">cwebp -lossless -z 9 source.png -o output.webp
</code></pre>

<p>The <code>-z</code> parameter accepts a value between 0 (no compression) and 9 (most compression). Higher compression yields lower file sizes, but requires more time to encode images. You can also set the <code>-m</code> parameter to influence output size, which specifies a compression method from 0 to 6:</p>

<pre><code class="language-bash">cwebp -lossless -m 6 -z 9 source.png -o output.webp
</code></pre>

<p>You can also use the <code>-q</code> parameter to tell cwebp how aggressively to compress the image, which can be slightly confusing because <code>-q</code> means something entirely different for lossless WebP than it does for lossy images For lossless WebP, <code>-q 100</code> applies the most compression, whereas <code>-q 0</code> applies the least. You can use <code>-q</code> in tandem with the <code>-m</code> and <code>-z</code> parameters to achieve very high compression, like so:</p>

<pre><code class="language-bash">cwebp -lossless -m 6 -z 9 -q 100 source.png -o output.webp
</code></pre>

<p>This level of compression takes by far the longest, but it can go quite a ways further in reducing your lossless image payloads. Experiment to find what works best for you. You might shave off more kilobytes than you thought possible!</p>

<p>Of course, these are just some quick examples of what’s possible. cwebp is an amazingly flexible encoder. To get the full list of available options, type <code>cwebp -longhelp</code> and poke around.</p>

<p>There’s a good chance you’ll need to convert a whole bunch of images at once. Next, I’ll show you a couple ways you can convert multiple files with short commands for Unix-like systems on bash.</p>

<h4 id="bulk-conversion-in-bash">Bulk Conversion in Bash</h4>

<p>If you’re using Bash on a Unix-like operating system such as macOS or Ubuntu, and you have a directory of images you need to convert to WebP, the <code>find</code> command does an excellent job. As the name would imply, <code>find</code> finds objects in the file system. The syntax for finding files by a specific extension is very straightforward:</p>

<pre><code class="language-bash">find ./ -type f -name '*.png'
</code></pre>

<p>In case you’re not familiar with how <code>find</code> works, let’s step through this example command.</p>

<ol>
<li>The first argument is the file system path to search, which in this case, is the current directory.</li>
<li>The second argument specifies the type of file system object. You can find directories with <code>-type d</code>. We’re finding files in this case, however, which means we’re going with <code>-type f</code>.</li>
<li>Lastly, the <code>-name</code> argument is the pattern by which to find files. In this instance, we’re finding all files ending in <em>.png</em>. When we run this command in a directory tree containing PNG files, the output might look something like this:</li>
</ol>

<pre><code class="language-bash">./sources/5-1024w.png
./sources/14-768w.png
./sources/old/15-768w.png
</code></pre>

<p>This might not seem very useful by itself, but here’s where the magic happens: you can take the files found by <code>find</code> and redirect them as input to any other program you want via the <code>-exec</code> parameter. Here’s how you could use <code>-exec</code> with cwebp to encode all PNGs in a subtree to lossy WebP images at a quality setting of 75:</p>

<pre><code class="language-bash">find ./ -type f -name '*.png' -exec sh -c 'cwebp -q 75 $1 -o "${1%.png}.webp"' _ {} \;
</code></pre>

<p>This may look a bit convoluted, but let’s step through what’s going on so we can better understand it together:</p>

<ol>
<li>The initial part of the command finds all files ending with a <em>.png</em> extension in the current directory (and subdirectories), just as we described earlier.</li>
<li>Files found are sent to the <code>-exec</code> parameter, which invokes an instance of the <code>sh</code> shell. The <code>-c</code> parameter accepts a command to run.</li>
<li>The command invoked is the <code>cwebp</code> encoder. The <code>-q</code> argument is the quality setting.</li>
<li>The <code>$1</code> placeholder represents the file found by <code>find</code> as an argument passed into <code>sh</code>. The <code>-o &quot;${1%.png}.webp&quot;</code> portion is the output file name. The pattern expressed replaces the <em>.png</em> extension with a <em>.webp</em> extension.</li>
<li>The final part passes the reference to the file found by <code>find</code> (represented by <code>{}</code>) to <code>sh</code>, and the entire command is terminated by <code>\;</code>.</li>
</ol>

<p>While this is admittedly a bit unwieldy, it’s quite useful when you need to convert a number of images to WebP quickly. When invoking cwebp in this fashion, feel free to adjust parameters as necessary to achieve the desired results. Just be aware this example command dumps the converted images into the same folder as the source images, so adjust as needed to control the location of the output.</p>

<p>The only drawback of this approach is it may take a long time to finish if you’re processing a large number of files, since images are processed one after the other rather than concurrently. If you need to speed up processing a bit, you might consider parallelizing image processing, which we’ll talk about next.</p>

<h4 id="concurrent-bulk-conversion-in-bash">Concurrent Bulk Conversion in Bash</h4>

<p>Here’s a potential scenario. You have hundreds, perhaps thousands of images you need to convert to WebP. While cwebp is reasonably fast, it can still take a very long time if you’re not processing images concurrently. Serialized processing doesn’t make the best use of your CPU’s potential like concurrent processing does. To get around this, you can augment the earlier command used for serialized batch conversion with <code>xargs</code> like so:</p>

<pre><code class="language-bash">find ./ -type f -name '*.png' | xargs -P 8 -I {} sh -c 'cwebp -q 75 $1 -o "${1%.png}.webp"' _ {} \;
</code></pre>

<p>This isn’t much different than the command from earlier, except with some key differences:</p>

<ol>
<li>The <code>-exec</code> parameter is notably absent. Instead, the output from <code>find</code> is piped directly to <code>xargs</code>, which handles processing in lieu of <code>-exec</code>.</li>
<li>The <code>xargs</code> command immediately follows the <code>|</code> character with three specific parts. The first is the <code>-P</code> parameter, which specifies the maximum amount of concurrent processes (8 in this example). The second is the <code>-I</code> parameter, which is the input <code>xargs</code> acts on (the value of which is the file found by <code>find</code>, represented by the <code>{}</code> placeholder). The final argument is the command <code>xargs</code> will execute, which is exactly the same as in the serialized bulk conversion command from before.</li>
</ol>

<p>If you want to increase the amount of concurrent processes, simply change the value you pass to the <code>-P</code> parameter. Unlike other asynchronous approaches, <code>xargs</code> allows you to throttle concurrency to a specified maximum so you don’t render your system unresponsive. While this approach may only shave off a few seconds for small batches of images, it shines when operating on very large ones. For example, when converting a batch of roughly 10,000 JPEGs to WebP, a serialized approach using only <code>find</code> took 21 minutes and 26 seconds, whereas a concurrent approach using <em>both</em> <code>find</code> and <code>xargs</code> took <strong>9 minutes and 8 seconds</strong>. This is approximately a <strong>57% decrease</strong> in processing time, and with a relatively conservative concurrency of 8 processes at a time. If you can afford to bump up concurrency, you may realize further reductions in processing time.</p>




<p>Of course, these commands aren’t limited to merely converting images to WebP. Whatever shell commands you can think of that will work with <code>find</code> and/or <code>xargs</code> will be just as serviceable. Experiment and see what you can pull off.</p>

<p>If converting images to WebP this way isn’t to your liking, maybe you’d prefer to accomplish the task in JavaScript. Next, we’ll talk about how to convert your images to WebP using Node.js, as well as within the various build systems available in the Node.js ecosystem.</p>

<h3 id="convert-images-to-webp-with-node-js">Convert Images to WebP with Node.js</h3>

<p>Node.js’s only use isn’t just a JavaScript application stack. Even in environments where JavaScript isn’t used in an application back-end, Node.js still proves useful as a build tool. The tool used for exporting images to WebP in Node.js or any Node.js-based build system is imagemin. . Whether you’re writing scripts to run with Node.js, or using one of many Node.js-based build systems (gulp, et al.), imagemin is the ticket. Let’s get started by demonstrating how you can convert images to WebP in a simple Node.js script.</p>

<h4 id="using-a-node-js-script">Using a Node.js Script</h4>

<p>Perhaps you’re not the type to reach for an opinionated build system first, and prefer to use Node.js scripts instead. That’s reasonable enough, and if you know how to write JavaScript, the learning curve isn’t very steep, since you don’t need to learn the syntax of a build system. To get started on converting images to WebP in Node.js, install the imagemin and imagemin-webp modules in your project root directory:</p>

<pre><code class="language-bash">npm install imagemin imagemin-webp
</code></pre>

<p>This command installs two modules: the first is imagemin itself, and the second is the imagemin-webp plug-in that extends imagemin so it can convert images to WebP. With these two modules installed locally in our project, we can then write a small script that will process JPEG images in a directory and convert them to WebP:</p>

<pre><code class="language-javascript">const imagemin = require("imagemin");
const webp = require("imagemin-webp");

imagemin(["sources/*.png"], "images", {
  use: [
    webp({
      quality: 75
    })
  ]
}).then(function() {
  console.log("Images converted!");
});
</code></pre>

<p>This short script imports the imagemin and imagemin-webp modules into the current script as two constants (<code>imagemin</code> and <code>webp</code>, respectively). We then run imagemin’s main method, which takes three arguments:</p>

<ol>
<li>The location of the source images. In this case, we’re converting all files ending in <em>.png</em> in the sources directory, which is assumed to be located in the same directory as the script itself.</li>
<li>The destination directory, which in this case is <em>images</em>. This directory is created if it doesn’t already exist.</li>
<li>An options object for the imagemin program. In this case, we’re specifying the use option, which allows us to pass plug-ins into imagemin. The only plug-in we’re using here is an instance of imagemin-webp (represented by the <code>webp</code> constant). The plug-in itself also accepts a configuration object, which we have used to specify that we want all PNGs converted to lossy WebP (implied, as lossy encoding is the default) with a <code>quality</code> setting of 75.</li>
</ol>

<p>Imagemin will convert images for us, and when it’s finished, it will return a . In that Promise, we output to the console that all of the images have been converted. If we save this script as <em>webp.js</em>, we can run it with the <code>node</code> command like so:</p>

<pre><code class="language-bash">node webp.js
</code></pre>

<p>Assuming everything is successful, a message will appear in the console:</p>

<pre><code class="language-bash">Images converted!
</code></pre>

<p>When all is done, WebP images should now exist in the <em>images</em> directory, relative to the location of where you saved <em>webp.js</em>. If you want to tweak the output, . For example, if you wanted to to generate lossless WebP images, you would instead use the <code>lossless</code> option like so:</p>

<pre><code class="language-javascript">webp({
  lossless: true
})
</code></pre>

<p>Just be aware that , the quality setting for lossless mode adjusts the compression. The compression is still lossless, but higher settings will generate smaller files.</p>

<p>Pro tip: the options you can pass to this plug-in are the same, no matter where you invoke the imagemin-webp plug-in, be it in a Node.js script, or the build system of your choice. Speaking of build systems, let’s next cover how you might convert images using gulp.</p>

<h4 id="using-gulp">Using gulp</h4>

<p>As far as build systems go,  is pretty common. Thanks to a huge ecosystem of plug-ins, gulp can do almost anything you’d need it to, including converting images to WebP! If you have gulp installed and configured for your project, you only need to install a few extra node modules at the command line:</p>

<pre><code class="language-bash">npm install gulp-imagemin imagemin-webp gulp-ext-replace
</code></pre>

<p> helps us to overcome this so we can write WebP images to the disk with the proper <em>.webp</em> extension.</p>

<p>Once you have these plug-ins installed, you’d just need to write a quick gulp task that reads source images from the disk and outputs them to WebP format. That task might look something like this:</p>

<pre class="break-out"><code class="language-javascript">const gulp = require("gulp");
const imagemin = require("gulp-imagemin");
const webp = require("imagemin-webp");
const extReplace = require("gulp-ext-replace");

gulp.task("exportWebP", function() {
  let src = "src/images/**/*.png"; // Where your PNGs are coming from.
  let dest = "dist/images"; // Where your WebPs are going.

  return gulp.src(src)
    .pipe(imagemin([
      webp({
        quality: 75
      })
    ]))
    .pipe(extReplace(".webp"))
    .pipe(gulp.dest(dest));
});
</code></pre>

<p>There’s a lot going on here, so let’s break it down:</p>

<ol>
<li>Like any Node.js-driven program, the first part of the script imports the modules necessary for the script to work.</li>
<li>Using the <code>gulp.task</code> method, we create a task named <code>exportWebP</code>, which starts with two variables: <code>src</code> points to the image files we want to process (PNG files in this example). <code>dest</code> points to the directory where the resulting WebP images will be written to.</li>
<li>The <code>gulp.src</code> method reads the PNG images from the location specified by the <code>src</code> variable.</li>
<li>Images are ferried to imagemin by the <code>gulp.pipe</code> method. The sole argument passed to imagemin is an array of imagemin plug-ins, which in this case is the sole imagemin-webp plug-in. As is the case with using imagemin in any environment, the arguments passed to the imagemin-webp plug-in (or any imagemin plug-in) will follow the same format.</li>
<li>Before we write the converted WebP images to the disk, we want to ensure the resulting files are written with a <em>.webp</em> extension by using the gulp-ext-replace plug-in.</li>
<li>Using gulp’s <code>dest</code> method, we write all the converted images to the location specified earlier by the <code>dist</code> variable.</li>
</ol>

<p>When everything’s in place, we can invoke gulp on the command line to convert images in the <em>src/images</em> directory like so:</p>

<pre><code class="language-bash">gulp exportWebP
</code></pre>

<p>Once the command finishes, your destination directory will contain WebP images you converted from whatever gulp finds in the source directory. That simple!</p>

<p>If you prefer Grunt over gulp, you’re in luck. Next, we’ll show an example of how you can use Grunt to convert images to WebP.</p>

<h4 id="using-grunt">Using Grunt</h4>

<p>Much like gulp,  is a task runner, albeit with a different syntax. It can be used for many of the same things gulp is used for, including optimization and conversion of images to different formats via imagemin. Unsurprisingly, it too can convert images to WebP by way of imagemin’s imagemin-webp plug-in. If you have a project currently using Grunt that you would like to modify to generate WebP images, it’s a relatively trivial task. In the directory containing <em>Gruntfile.js</em>, simply install these two modules like so:</p>

<pre><code class="language-bash">npm install grunt-contrib-imagemin imagemin-webp
</code></pre>

<p>This command installs the imagemin plug-in for Grunt (provided by ), as well as the familiar imagemin-webp plug-in used to convert images to WebP. Once the installation finishes, you’ll need to set up a Grunt task in <em>Gruntfile.js</em> like so:</p>

<pre><code class="language-javascript">const grunt = require("grunt");
const webp = require("imagemin-webp");

grunt.initConfig({
  imagemin: {
    dist: {
      options: {
        use: [webp({
          quality: 75
        })]
      },
      files: [{
        expand: true,
        cwd: "src/images/",
        src: ["**/*.png"],
        dest: "dist/images",
        ext: ".webp"
      }]
    }
  }
});

grunt.loadNpmTasks("grunt-contrib-imagemin");
</code></pre>

<p>Once again, let’s step through this code and find out what’s going on:</p>

<ol>
<li>Initially, we <code>require</code> the necessary grunt and imagemin-webp modules that we’ll need for the imagemin Grunt task.</li>
<li>In the imagemin task, we create a <code>dist</code> target, which is what we’ll run from the command line. This target contains an <code>options</code> object for Grunt’s imagemin plug-in that allows us to specify configuration options. In this case, we supply an instance of the imagemin-webp plug-in and pass the usual options to it.</li>
<li>The <code>files</code> object is the guts of the operation. cwd specifies which directory we want to work within. <code>src</code> specifies the files within <code>cwd</code> that we want to convert to WebP. <code>dest</code> specifies the directory we want to output the converted images to. Finally, <code>ext</code> specifies that we want the converted images to be saved with a <em>.webp</em> extension.</li>
<li>The last line of code loads the grunt-contrib-imagemin plug-in so we can use it in the Gruntfile.</li>
</ol>

<p>Once you have this in place, you can convert images to WebP like so:</p>

<pre><code class="language-bash">grunt imagemin:dist
</code></pre>

<p>Once this command finishes, images ending in <em>.png</em> in the directory specified in <code>files.cwd</code> will be converted to WebP, and output to the directory specified in <code>files.dest</code>.</p>

<p>Grunt is not quite as intuitive as gulp is, and is falling out of use somewhat. However, it’s still a serviceable choice for a build system, and you may yet encounter it in some situations.</p>

<p>To round out our documentation of how to convert images to WebP within the the Node.js ecosystem, let’s discuss how you might accomplish that same task in webpack.</p>

<div class="sponsors__wide-place"></div>




<h3 id="using-webpack">Using Webpack</h3>

<p>If you’re developing modern JavaScript applications, chances are high that  is in your midst. In contrast to gulp and Grunt, which style themselves as task runners, webpack is a module bundler that analyzes your code starting from one or more entry points and generates optimized output. While much of what webpack does is accomplished through loaders, it does have a large ecosystem of plug-ins, too. imagemin is represented in that space by imagemin-webpack-plugin.</p>

<p>How webpack works and how to write a config for it are complex subjects, especially if you’re used to using task runners like gulp. I’m going to assume you have at least <em>some</em> familiarity with webpack basics, and just show you how to add imagemin to an existing webpack config to convert images to WebP. Like gulp and Grunt before, you’ll need to use npm to install a few necessary Node.js modules:</p>

<pre><code class="language-bash">npm install imagemin-webpack-plugin imagemin-webp copy-webpack-plugin
</code></pre>

<p>Similar to how gulp has its own imagemin plug-in, webpack has one as well, in the form of ) to pipe the files it encounters in its dependency graph to imagemin intelligently, but it may be more expedient to specify a source directory on the disk and let imagemin churn through everything it finds and spit out images to the destination directory. Such code might look something like this:</p>

<pre class="break-out"><code class="language-javascript">ImageminWebpackPlugin = require("imagemin-webpack-plugin").default;
ImageminWebP = require("imagemin-webp");
CopyWebpackPlugin = require("copy-webpack-plugin");

module.exports = {
  // Omitted required entry, output, and loader configs for brevity...
  plugins: [
    new CopyWebpackPlugin([{
      from: "./src/images/*.png",
      to: "./images/[name].webp"
    }]),
    new ImageminWebpackPlugin({
      plugins: [
        ImageminWebP({
          quality: 75
        })
      ]
    })
  ]
};
</code></pre>

<p>As we have with other code examples, let’s step through everything and get a handle on what’s happening:</p>

<ol>
<li>As noted, the required entry, output, and loader configurations have been omitted for brevity and relevance, as we’re assuming you have <em>some</em> familiarity with webpack.</li>
<li>The <code>plugins</code> config is merely an array of plug-ins we want to use. The first plug-in in the array is an instance of copy-webpack-plugin. To start, we specify in <code>from</code> the files we want to copy from the source directory. In this example, we include all files ending in <em>.png</em> from a specific source directory.</li>
<li>Next, we tell copy-webpack-plugin where we want the optimized images to go in the <code>to</code> option. It’s important to note in this option that we’re using a placeholder of <code>[name]</code> to tell copy-webpack-plugin that we want the name of the output file to be the same as its corresponding source. However, because we’re outputting WebP files, we don’t want to preserve the source file’s extension, so we’re hardcoding the output file’s extension to <em>.webp</em>. It’s also important to remember that files will be written to a location relative to whatever is set in <code>output.path</code> earlier in your webpack config.</li>
<li>The next plug-in in the sequence is an instance of imagemin-webpack-plugin, which should look familiar to other imagemin use cases. Here, we’re simply passing an instance of the imagemin-webp plug-in to the imagemin instance.</li>
</ol>

<p>Using this configuration, all images ending in <em>.png</em> found in <em>./src/images</em> will be converted to WebP and output to the images directory relative to your configuration’s <code>output.path</code> directory.</p>

<p>While there are multiple approaches to converting images to WebP within webpack, this aims to be the most straightforward. Compared to other build systems, webpack is an incredibly rich (and at times complex) tool. This example is not meant to be <em>the</em> authoritative approach to generating WebP images within webpack, but rather to show that it’s possible.</p>

<p><h3 style="padding-top: 1.5em;border-top: 3px solid #e5e5e5;">Did You Like This Excerpt? Here’s Why This eBook May Be, Just May Be, For You 😉</h3>
<p><em>The WebP Manual</em> will get you ready for the new image format that is capable to significantly less data-intensive user experiences for a majority of your audience:</p>
<ul>
<li>Learn how lossy and lossless WebP compare to JPEGs and PNGs exported by a number of image encoders.</li>
<li>Learn which services and plugins you can use to export or convert images to WebP with your preferred design tool or command line tool.</li>
<li>Learn how to can use WebP in production, and how to implement proper fallbacks for browsers that don’t support WebP just yet.</li>
<li>Learn how to use the full potential of the WebP format. It will substantially improve loading performance for many of your users, customers, and clients, and it will become one of your favorite tools for making websites as lean as possible. </li>
</ul></p>

<p><em>The eBook is  (you can cancel anytime, of course)</em>.</p>

<figure><img src="https://res.cloudinary.com/indysigner/image/upload/v1531926616/webp-manual-ipad-opt_akcnzz.png" width="800" height="800" alt="A mockup of The WebP Manual’s cover on a white iPad" /></a></figure>

<div class="book-cta" data-handler="ContentTabs" data-mq="(max-width: 480px)">
  <nav class="content-tabs content-tabs--books">
  <ul>
     <li class="content-tab">
     <button class="btn btn--small btn--white btn--white--bordered">eBook</button>
     </li>
     <li class="content-tab">
     <button class="btn btn--small btn--white btn--white--bordered">Free for Members</button>
     </li>
   </ul>
 </nav>
  <div id="getthebook" class="book-cta__col book-cta__hardcover content-tab--content">
  <span class="book-cta__price"><span class="green">$14.90</span></span>
  <p class="book-cta__desc">PDF, ePUB, Kindle.</p>
  </div>
  <div class="book-cta__col book-cta__ebook content-tab--content">
  <span class="book-cta__price"><span class="green">$0.00 </span><span class="book-cta__price--del"><del>$14.90</del></span></span> 
   <p class="book-cta__desc">...along with .</em></small></p>
    </div>
</div>

              </article>
            </body>
          </html>
---------------
<h1 id="#title_20" >21、Text Editing Tips And Tricks Roundup</h1>
Rachel Andrew
[https://www.smashingmagazine.com/2018/07/text-editing-tips-tricks/](https://www.smashingmagazine.com/2018/07/text-editing-tips-tricks/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/07/text-editing-tips-tricks/" />
              <title>Text Editing Tips And Tricks Roundup</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>Text Editing Tips And Tricks Roundup</h1>
                  
                    
                    <address>Rachel Andrew</address>
                  
                  <time datetime="2018-07-23T13:30:35&#43;02:00" class="op-published">2018-07-23T13:30:35+02:00</time>
                  <time datetime="2018-07-24T10:53:31&#43;00:00" class="op-modified">2018-07-24T10:53:31+00:00</time>
                </header>
                

<p> for their favorite text editing tricks, shortcuts, and features that save them time. Here’s a roundup of what we’ve found quite useful along with a couple of other suggestions you may find handy.</p>

<h3 id="favourite-keyboard-shortcuts">Favourite Keyboard Shortcuts</h3>

<p>Many of you have favorite keyboard shortcuts. Some of these will be editor or operating system specific, although in many cases you’ll be able to find a similar shortcut with the tools you are using. I’ve rounded up a few from the community below.</p>

<p>Ste Grainer shared :</p>

<blockquote>The basic movement/selection shortcuts that many don’t know about:<br /><br />Hold <kbd>Cmd</kbd> + <kbd>Arrow Key</kbd> to move to the beginning/end of a line or top/bottom of a document.<br /><br />Hold <kbd>Opt</kbd> + <kbd>Arrow Key</kbd> to move word to word horizontally and block to block vertically.<br /><br />Shift to select while doing those.</blockquote>

<p>From :</p>

<blockquote>Select all occurences of current selection (<kbd>Ctrl</kbd> + <kbd>SHIFT</kbd> + <kbd>L</kbd> in VSCode) and duplicate line/selection which I set up as <kbd>Ctrl</kbd> + <kbd>D</kbd>.</blockquote>

<p> shared a few favorite shortcuts for hopping around or deleting text:</p>

<blockquote><kbd>⌥</kbd> + <kbd>forward/back arrows</kbd> allows to jump to the next word instead of the next letter<br /><kbd>⌥</kbd> + <kbd>up/down arrows</kbd> allows to jump to the beginning/end of the paragraph<br /><kbd>⌥</kbd> + <kbd>Backspace</kbd> deletes the whole word instead of letters by letters.</p></blockquote>

<p>Many of the suggested tips came from web developers &mdash; tips for the editors they used most frequently. We also received suggestions for Android Studio from :</p>

<blockquote>In Android Studio:<br />
<ul>
<li><kbd>Ctrl</kbd> + <kbd>D</kbd> &mdash; Duplicate line</li>
<li><kbd>Ctrl</kbd> + <kbd>Y</kbd> &mdash; Delete line</li>
<li><kbd>Ctrl</kbd> + <kbd>W</kbd> &mdash; Select block</li>
<li><kbd>Ctrl</kbd> + <kbd>O</kbd> &mdash; Override methods</li>
<li><kbd>Ctrl</kbd> + <kbd>ALT</kbd> + <kbd>L</kbd> &mdash; Reformat code</li>
</ul></blockquote>



<aside class="product-panel product-panel__tilted product-panel--book" data-audience="non-subscriber">
    <div class="container product-panel--book__container">
      <div class="panel__description panel__description--book">
    <p>Getting workflow <em>just</em> right ain’t an easy task. So are proper estimates. Or alignment among different departments. That’s why we’ve set up <strong>“this-is-how-I-work”-sessions</strong> — with smart cookies sharing what works well for them. A part of the , of course.</p>
      <a href="http://smashed.by/workflowpanelmembership" class="btn btn--green btn--large">
        Explore features&nbsp;→
      </a>
      </div>
      <div class="panel__image panel__image--book">
        <a href="http://smashed.by/workflowpanelmembership" class="books__book__image">
        <div class="books__book__img">
          <img src="https://www.smashingmagazine.com/images/smashing-cat/smashing-tv-box-cat.svg" alt="Smashing TV, with live sessions for professional designers and developers." width="310" height="400">
        </div>
      </a>
      </div>
    </div>
  </aside>




<h3 id="editor-shortcut-cheatsheets">Editor Shortcut Cheatsheets</h3>

<p>As we can see from the tips already posted, learning the keyboard shortcuts for your editor saves a lot of time. It is always worth taking a look at what is available for your editor, as learning a few of these shortcuts can save a lot of typing over the course of a day writing code.</p>

<p>On Twitter,  which is a detailed list of shortcuts for Atom. I also took a look at what was available for other frequently used editors.</p>

<h4 id="visual-studio-code">Visual Studio Code</h4>

<p>The VS Code website has a number of downloadable cheatsheets in PDF format, if you find it useful to keep a cheatsheet printed out on your desk.</p>

<ul>
<li></li>
<li></li>
<li></li>
</ul>

<p>”</p>

<h4 id="sublime-text">Sublime Text</h4>

<p>A good selection of Sublime Text 3 shortcuts for Windows, Mac, and Linux can be found .</p>

<p>We also have an article here on Smashing Magazine in which Jai Panda shares some of his favorite .</p>

<h3 id="customizing-your-environment">Customizing Your Environment</h3>

<p>Our keyboards and default computer settings are designed more for typing text than typing code. Some commenters have made changes to their defaults in order to make it faster to type the things they most often need to type.</p>

<p> made this suggestion:</p>

<blockquote>I minimize the number of times I have to hold <kbd>Shift</kbd> and press a button. If I make brackets (<code>(</code> <code>)</code>) far more often than I use <code>9</code> and <code>0</code>, I customize the keyboard to reflect that, my <kbd>9</kbd> is <code>(</code> and <kbd>Shift</kbd> + <kbd>9</kbd> is <code>9</code>, etc.</blockquote>

<p> sets his ‘Key Repeat’ and ‘Delay Until Repeat’ to their highest setting in order that his cursor just “flies across the screen when using the arrows.”</p>

<p> told us how he, “created <kbd>Alt</kbd> + <kbd>;</kbd> as a shortcut to insert a semicolon at the end of a current line.”</p>

<h3 id="using-emmet">Using Emmet</h3>

<p>A number of people mentioned the text expansion system of . If you hand-code a lot of HTML and CSS then Emmet can save you a great deal of typing time. When writing HTML, Emmet abbreviations will be familiar to anyone who understands CSS. For example, if you want to create an unordered list inside a <code>div</code> element, you could use the following:</p>

<pre><code class="language-html">div&#x3E;ul&#x3E;li
</code></pre>

<p>Which would then turn into:</p>

<pre><code class="language-html">&#x3C;div&#x3E;
  &#x3C;ul&#x3E;
    &#x3C;li&#x3E;&#x3C;/li&#x3E;
  &#x3C;/ul&#x3E;
&#x3C;/div&#x3E;
</code></pre>

<p>The abbreviation is exactly the selector that would select the <code>li</code> in CSS. A <code>div</code> with a <code>ul</code> as a direct child, and a <code>li</code> as a direct child of the <code>ul</code>. Take a look at the  for more examples.</p>

<p>Emmet is built into VS Code and  for many other editors.</p>

<div class="sponsors__wide-place"></div>




<h3 id="use-a-clipboard-manager">Use A Clipboard Manager</h3>

<p> for OS X, which sadly seems to be discontinued.</p>

<p>Similar tools include:</p>

<ul>
<li> for MacOS</li>
<li> for MacOS</li>
<li> for Windows</li>
<li> Windows and MacOS (currently in Beta)</li>
</ul>

<p>Many editors also include a clipboard history for copy and paste actions within the editor. On Twitter, .</p>

<h3 id="a-collection-of-recommended-tools">A Collection Of Recommended Tools</h3>

<p>There were a few specific tools recommended in the comments, so here is a roundup of useful tools you may not have heard of.</p>

<h4 id="vim">Vim</h4>

<p>People who like Vim, really really like Vim. It certainly comes with a learning curve, however, if you are very keen on optimizing your keyboard editing then the time invested is likely to be worth it. As , you can do things like type <code>13k</code> to move the cursor 13 lines up.</p>

<p>Take a look at the  as well.</p>

<h4 id="prettier">Prettier</h4>

<p> is an open-source <em>opinionated</em> code formatting tool. Using Prettier ensures that all code is formatted to a consistent style. This is incredibly helpful when working in a team as it means that a consistent style is enforced, without anyone really needing to think about it.</p>

<p>, in order that you can use Prettier within whichever environment you chose.</p>

<h4 id="autohotkey">AutoHotkey</h4>

<p>I had not heard of the tool . AutoHotkey is an automation scripting language for Windows. Using the scripting language you can create shortcuts for common tasks, for example, to insert a template.</p>

<h4 id="converting-text-formats-with-pandoc">Converting Text Formats With Pandoc</h4>

<p>One of my favorite tools is . I use Pandoc when I need to convert one text format to another. One of the really useful things Pandoc can do is turn HTML or Markdown into EPUB format. I frequently do this in order to turn a set of notes into a file I can read using iBooks on my iPad. I do this in order to have an easily accessible set of notes for my workshops or to turn lengthy documentation into an easy to read offline format to read on an airplane.</p>

<p>Pandoc can convert from and to many different file formats. In addition to creating quick EPUB files, I also use it to convert copy from Word documents to Markdown or other useful formats. This can be very useful if you get some messy copy from a client that needs to be converted to enter into a CMS.</p>

<div class="sponsors__wide-place"></div>




<h4 id="textexpander-and-typinator">TextExpander And Typinator</h4>

<p> a try.</p>

<p>These text expansion tools can be useful outside of writing code. If you often find yourself typing the same information in answer to emails or support requests, creating a shortcut to insert that text can quickly pay dividends in terms of time saved.</p>

<h4 id="textwasher">Textwasher</h4>

<p>Recommended on Facebook by Dennis Germundal,  is a very simple tool for cleaning any formatting from text.</p>

<h3 id="add-your-suggestions-in-the-comments">Add Your Suggestions In The Comments</h3>

<p>There are a vast number of ways to enhance productivity in the tools we use every day, and it is also incredibly easy to completely overlook them. I hope that among these suggestions there will be something for you to try out. Or perhaps this will be a prompt for you to dig a little deeper into the documentation for your editors and other tools. I have certainly been inspired to do so.</p>

<p>If you missed the tweet and have some great tips to share, then add them to the comments. We’d love to hear them!</p>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(il)</span>
</div>


              </article>
            </body>
          </html>
---------------