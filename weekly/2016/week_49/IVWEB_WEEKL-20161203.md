## 文章索引
1、 <a href="#1前端-ajax-上传文件nodejs-接收文件" >[前端] ajax 上传文件；nodejs 接收文件；</a><br/>
2、 <a href="#2前端-前端界面-modal-的控制---文蔺的博客-@wemlion" >[前端] 前端界面 Modal 的控制 - 文蔺的博客 @wemlion</a><br/>
3、 <a href="#3译只在需要的时候-polyfill-你的-javascript-代码" >【译】只在需要的时候 Polyfill 你的 JavaScript 代码</a><br/>
4、 <a href="#4前端-视频whats-new-in-typescript-20-&-21" >[前端] 【视频】what's new in typescript 2.0 & 2.1</a><br/>
5、 <a href="#5前端-厉害了网页设计巅峰之作" >[前端] 厉害了，网页设计巅峰之作</a><br/>
6、 <a href="#6前端-scroller-for-vue-20" >[前端] Scroller for Vue 2.0</a><br/>
7、 <a href="#7前端-笔记velocity-2016-第二天" >[前端] 笔记：Velocity 2016 第二天</a><br/>
8、 <a href="#8后端-linux-命令大全提供-500-多个-linux-命令搜索" >[后端] Linux 命令大全提供 500 多个 Linux 命令搜索</a><br/>
9、 <a href="#9后端-spring-定时任务实现方案" >[后端] Spring 定时任务实现方案</a><br/>
10、 <a href="#10nativescript-24版本发布支持web-workers规范" >NativeScript 2.4版本发布，支持Web Workers规范</a><br/>
11、 <a href="#11android-十分钟理解-android-中的嵌套滚动" >[Android] 十分钟理解 Android 中的嵌套滚动</a><br/>
12、 <a href="#12android-android-路由动态配置方案可能是最简单的热更新实现" >[Android] Android 路由动态配置方案——可能是最简单的热更新实现</a><br/>
13、 <a href="#13firefox-focus一个ios的私人浏览器" >Firefox Focus：一个iOS的私人浏览器</a><br/>
14、 <a href="#14作为团队管理者我是如何与团队成员分享信息的" >作为团队管理者，我是如何与团队成员分享信息的</a><br/>
15、 <a href="#15user-space-与-kernel-space" >User space 与 Kernel space</a><br/>
16、 <a href="#16android-我的第一款全栈-side-project" >[Android] 我的第一款全栈 side project</a><br/>
17、 <a href="#17设计-嘿设计师你可不是艺术家成为一个商业设计师的-9-个贴士" >[设计] 嘿，设计师，你可不是艺术家：成为一个商业设计师的 9 个贴士</a><br/>
18、 <a href="#18android-okhttp-更新-token-的解决方案" >[Android] OkHttp 更新 token 的解决方案</a><br/>
19、 <a href="#19net-standard-20整齐划一的目标" >.NET Standard 2.0：整齐划一的目标</a><br/>
20、 <a href="#20工具资源-你的名字非官方命令行工具" >[工具资源] 你的名字。非官方命令行工具</a><br/>
21、 <a href="#21android-listview-源码解析乱弹" >[Android] listview  源码解析乱弹</a><br/>
22、 <a href="#22android-android-跨进程通信-aidl-的使用及注意事项----csdn" >[Android] Android 跨进程通信 Aidl 的使用及注意事项 ---CSDN</a><br/>
23、 <a href="#23android-数字增加动画的-textview" >[Android] 数字增加动画的 TextView</a><br/>
24、 <a href="#24web-development-reading-list-#161:-restyling-form-elements-http/2-hpack-and-the-empathy-vacuum" >Web Development Reading List #161: Restyling Form Elements, HTTP/2 HPACK, And The Empathy Vacuum</a><br/><h1 id="#title_0" >1、[前端] ajax 上传文件；nodejs 接收文件；</h1>
刘建辉1465890419000
[https://gold.xitu.io/entry/58413d870ce46300576aa950](https://gold.xitu.io/entry/58413d870ce46300576aa950)
<img src="https://dn-mhke0kuv.qbox.me/334e67b278181e571c84.jpg?imageView/2/w/800/h/600/q/80/format/png"/><p>有进度条的文件上传，</p><p></p>
---------------
<h1 id="#title_1" >2、[前端] 前端界面 Modal 的控制 - 文蔺的博客 @wemlion</h1>
文蔺
[https://gold.xitu.io/entry/584196062f301e005cff225f](https://gold.xitu.io/entry/584196062f301e005cff225f)
<p>不能直接回车键确认完成的自定义弹窗都是耍流氓。。。</p><p></p>
---------------
<h1 id="#title_2" >3、【译】只在需要的时候 Polyfill 你的 JavaScript 代码</h1>

[https://www.h5jun.com/post/polyfill-javascript-only-when-you-need-to.html](https://www.h5jun.com/post/polyfill-javascript-only-when-you-need-to.html)
<blockquote>
<p>原文：</p>
</blockquote>
<p><em>本文转载自 ，他是一名来自德国南部的实习生，他讨厌不必要的 HTTP 请求，也不爱吃西兰花。Pascal 将说明使用 polyfill 服务的一种方式，在这种方式下你可能可以完全不必使用它。</em></p>
<!--more-->
<h3 id="-">现状</h3>
<p>我们想要用来写 JavaScript。然而由于我们需要兼容老版本的浏览器，那些浏览器不支持 ES6，我们需要解决这个问题。</p>
<p>有一个标准的做法是：<strong>写 ES6 代码 → 将所有代码编译成 ES5 的（比如通过 Babel）→ 再将编译后的代码加载到浏览器执行。</strong></p>
<p>这可能已经不再是最有效率的方式了。因为用这种方式，我们强制最新的浏览器运行旧代码，实际上它们完全可以运行最新的代码。，我们难道不能直接给它们 ES6 代码吗？</p>
<h3 id="-">改进方式</h3>
<p>有一个 polyfill 项目叫做 ，它可以通过 polyfill 方式在客户端执行 ES6 代码。</p>
<p><img src="http://p9.qhimg.com/t0109387db34edbeb01.png" alt=""></p>
<p>它也实现了一些 HTML 特性的 polyfill，比如 <code>&lt;picture&gt;</code> 元素。</p>
<p>下面是他们网站的描述：</p>
<blockquote>
<p>Polyfill.io 读取每个请求的 (UA) 头，并生成适合于该浏览器的 polyfill ，基于你的应用所使用的特性发回必要的代码。[...]</p>
</blockquote>
<p> 在开发和维护这个项目，所以我们能确信这个项目可以持续更新下去，不会死掉。</p>
<p>有一点需要明白：Polyfill.io 没有提供语法糖支持。比如 <strong>类、增强的对象字面量</strong>，以及<strong>箭头函数</strong>之类的特性。对那些代码，你仍然需要进行编译。</p>
<h3 id="-polyfill-io">配置 Polyfill.io</h3>
<p>Adding Polyfill.io to your project can be this simple. Add the CDN-hosted script to your page:</p>
<p>要添加 Polyfill.io 到你的项目里非常简单。将托管在 CDN 的脚本添加到你的页面上：</p>
<pre><code class="hljs lang-xml">`<span class="hljs-tag">&lt;<span class="hljs-name">script</span> <span class="hljs-attr">src</span>=<span class="hljs-string">"https://cdn.polyfill.io/v2/polyfill.min.js"</span>&gt;</span><span class="undefined"></span><span class="hljs-tag">&lt;/<span class="hljs-name">script</span>&gt;</span>`
</code></pre><p>运行脚本将返回 UA 和你想要的特性。</p>
<pre><code class="hljs lang-groovy">UA <span class="hljs-string">detected:</span> chrome/<span class="hljs-number">56.0</span><span class="hljs-number">.0</span>
Features <span class="hljs-string">requested:</span> <span class="hljs-keyword">default</span>
</code></pre><h3 id="-">修改请求参数</h3>
<p>它提供了 来自定义你要返回的特性。</p>
<h4 id="features">Features</h4>
<p>该参数指定需要 polyfill 的浏览器特性。多个特性名之间用逗号分隔。允许使用的特性明在  页中列出。</p>
<pre><code class="hljs lang-xml">`<span class="hljs-tag">&lt;<span class="hljs-name">script</span> <span class="hljs-attr">src</span>=<span class="hljs-string">"https://cdn.polyfill.io/v2/polyfill.min.js?features=fetch"</span>&gt;</span><span class="undefined"></span><span class="hljs-tag">&lt;/<span class="hljs-name">script</span>&gt;</span>`
</code></pre><p>在 Safari 10 下，脚本返回内容如下：</p>
<pre><code class="hljs lang-haml">Features requested: fetch

-<span class="ruby"> setImmediate, <span class="hljs-symbol">License:</span> CC<span class="hljs-number">0</span> (required by <span class="hljs-string">"Promise"</span>, <span class="hljs-string">"fetch"</span>)
</span>-<span class="ruby"> fetch
</span></code></pre><p>如果一个特性，比如 <strong>fetch</strong> 依赖于另一个特性比如 <strong>Promise</strong>，Polyfill.io 会自动加载依赖。</p>
<h4 id="flags">Flags</h4>
<ul>
<li><strong>always</strong> - Polyfill 将始终被包含，不管 UA 中指出的浏览器是否已经支持该特性。</li>
<li><strong>gated</strong> - 通过特性检测来判断 Polyfill，只有在浏览器原生 API 不支持这些特性的情况下才返回并执行 Polyfill。</li>
</ul>
<pre><code class="hljs lang-xml">`<span class="hljs-tag">&lt;<span class="hljs-name">script</span> <span class="hljs-attr">src</span>=<span class="hljs-string">"https://cdn.polyfill.io/v2/polyfill.min.js?features=fetch&amp;flags=gated"</span>&gt;</span><span class="undefined"></span><span class="hljs-tag">&lt;/<span class="hljs-name">script</span>&gt;</span>`
</code></pre><h4 id="callback">Callback</h4>
<p>Polyfill 脚本加载完成之后要执行的函数名。这是最简单的在 polyfill 加载完成后触发你自己的代码的方式，这样 polyfill 服务可以更容易通过 async 和 defer 属性被异步加载。</p>
<h3 id="-">存在的问题</h3>
<p>听起来很好，但是仍然不完美。</p>
<p>最新的浏览器不需要加载 ES5 代码了，但是还需要通过服务器请求来检测是否需要 polyfill。</p>
<p>这非常困扰我，因此我正在做一个小项目来改进它。</p>
<h3 id="-">一个更好的方式</h3>
<h4 id="-dynamic-polyfill">配置 dynamic polyfill</h4>
<p>我创建了一个叫做  的 npm 包。它在发起任何服务端请求前检测特性是否已经被原生支持。</p>
<p>它的配置看起来如下：</p>
<pre><code class="hljs lang-qml"><span class="hljs-keyword">import</span><span class="hljs-string"> polyfill from "dynamic-polyfill"</span>

polyfill({
    <span class="hljs-attribute">fills</span>: <span class="hljs-string">"fetch, Promise"</span>,
    <span class="hljs-attribute">options</span>: <span class="hljs-string">"gated"</span>, <span class="hljs-comment">// default: null</span>
    <span class="hljs-attribute">minify</span>: <span class="hljs-literal">false</span>,  <span class="hljs-comment">// default: true</span>
    afterFill() {
        main()
    }
})

<span class="hljs-function"><span class="hljs-keyword">function</span> <span class="hljs-title">main</span>(<span class="hljs-params"></span>) </span>{
    <span class="hljs-comment">// app code here</span>
}
</code></pre><p>简单来说，它的执行过程如下：</p>
<p><strong>检测 [window.fetch, window.Promise] 是否存在。</strong></p>
<p>如果存在，运行 <code>afterFill()</code> 回调。</p>
<p>如果它们不存在，创建一个 <code>&lt;script&gt;</code> 标签，并且包含 <code>async</code> 属性，将 Polyfill.io 链接插入，用参数中提供的选项去请求，并在它加载完成后执行 <code>afterFill()</code> 回调。</p>
<p><strong>注意：</strong> 现在还没有支持全部选项，只有那些最重要的项被支持。</p>
<h4 id="-">脚本很小</h4>
<p>由于这个模块在压缩后不到 1KB 大小，而且没有任何依赖，对项目使用来说成本超低。</p>
<h3 id="-">结论</h3>
<p>为最新的浏览器写不过时和有效率的 JavaScript，让 Polyfill.io 去处理老版本的的浏览器，如果不必要，别发起额外的 HTTP 请求。</p>
<p>怎么样？是不是觉得棒棒哒？</p>
<blockquote>
<p>英文原文：</p>
</blockquote>
---------------
<h1 id="#title_3" >4、[前端] 【视频】what's new in typescript 2.0 & 2.1</h1>
屌丝准码农一枚
[https://gold.xitu.io/entry/5841e44a128fe100589d454c](https://gold.xitu.io/entry/5841e44a128fe100589d454c)
<img src="https://dn-mhke0kuv.qbox.me/61f8a40b272e8b32dd62.jpg?imageView/2/w/800/h/600/q/80/format/png"/><p>概述 TypeScript 2.0 和 2.1 带来的新功能。</p><p></p>
---------------
<h1 id="#title_4" >5、[前端] 厉害了，网页设计巅峰之作</h1>
王子林
[https://gold.xitu.io/entry/58418232128fe100589bc229](https://gold.xitu.io/entry/58418232128fe100589bc229)
<p>太赞了！！！</p><p></p>
---------------
<h1 id="#title_5" >6、[前端] Scroller for Vue 2.0</h1>
王大虎
[https://gold.xitu.io/entry/58416530ac502e006bed7ebf](https://gold.xitu.io/entry/58416530ac502e006bed7ebf)
<p>下拉刷新 无限加载 （For Vue 1.0, please refer to https://github.com/wangdahoo/vue-scroller）</p><p></p>
---------------
<h1 id="#title_6" >7、[前端] 笔记：Velocity 2016 第二天</h1>
文蔺
[https://gold.xitu.io/entry/584161d2ac502e006cc3e7a3](https://gold.xitu.io/entry/584161d2ac502e006cc3e7a3)
<p>笔记：Velocity 2016 第二天</p><p></p>
---------------
<h1 id="#title_7" >8、[后端] Linux 命令大全提供 500 多个 Linux 命令搜索</h1>
小弟调调™
[https://gold.xitu.io/entry/584166b8c59e0d005693e845](https://gold.xitu.io/entry/584166b8c59e0d005693e845)
<img src="https://dn-mhke0kuv.qbox.me/0078964f96a44762b27c.png?imageView/2/w/800/h/600/q/80/format/png"/><p>516 个 Linux 命令大全，内容包含 Linux 命令手册、详解、学习，值得收藏的 Linux 命令速查手册。</p><p></p>
---------------
<h1 id="#title_8" >9、[后端] Spring 定时任务实现方案</h1>
istarvip
[https://gold.xitu.io/entry/5841447161ff4b006b8b416a](https://gold.xitu.io/entry/5841447161ff4b006b8b416a)
<img src="https://dn-mhke0kuv.qbox.me/bbce87f5eeeaac524d87.png?imageView/2/w/800/h/600/q/80/format/png"/><p>项目开发中需要执行一些定时任务，比如需要在每天凌晨时候，分析一次前一天的日志信息，借此机会整理了一下定时任务的几种实现方式，由于项目采用 spring 框架，所以我都将结合 spring 框架来介绍。</p><p></p>
---------------
<h1 id="#title_9" >10、NativeScript 2.4版本发布，支持Web Workers规范</h1>
James Chesters
[http://www.infoq.com/cn/news/2016/12/nativescript-24?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2016/12/nativescript-24?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>NativeScript 2.4版本发布，该版本将支持Angular 2.2、Node 6、ES6和ES7，同时附带了默认的CSS主题。</p> <i>By James Chesters</i> <i> Translated by 于航</i>
---------------
<h1 id="#title_10" >11、[Android] 十分钟理解 Android 中的嵌套滚动</h1>
Absfree
[https://gold.xitu.io/entry/58418059128fe100576be542](https://gold.xitu.io/entry/58418059128fe100576be542)
<img src="https://dn-mhke0kuv.qbox.me/226a21efb48784055c9a.png?imageView/2/w/800/h/600/q/80/format/png"/><p>本文是对嵌套滚动机制的 “启蒙教育”，十分钟快速理解嵌套滚动是什么及其基本实现原理，为进一步的深入学习做好铺垫。</p><p></p>
---------------
<h1 id="#title_11" >12、[Android] Android 路由动态配置方案——可能是最简单的热更新实现</h1>
Tango
[https://gold.xitu.io/entry/58417323ac502e006b9809d9](https://gold.xitu.io/entry/58417323ac502e006b9809d9)
<img src="https://dn-mhke0kuv.qbox.me/eda9160ef8890c93de24.png?imageView/2/w/800/h/600/q/80/format/png"/><p>本博客主要介绍如何实现路由动态配置，使用 H5 页面替换原生页面，以及原生页面和网页间的任意跳转与传参。</p><p></p>
---------------
<h1 id="#title_12" >13、Firefox Focus：一个iOS的私人浏览器</h1>
David Iffland
[http://www.infoq.com/cn/news/2016/12/firefox-focus-ios-web-browser?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2016/12/firefox-focus-ios-web-browser?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Firefox Focus是一个iOS上的新浏览器，它默认可以屏蔽广告和内容跟踪器。因为它功能精简而且只有单标签的UI，这个浏览器保护了您的隐私和上网速度。</p> <i>By David Iffland</i> <i> Translated by 足下</i>
---------------
<h1 id="#title_13" >14、作为团队管理者，我是如何与团队成员分享信息的</h1>
薛命灯
[http://www.infoq.com/cn/news/2016/12/managers-share-information-membe?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2016/12/managers-share-information-membe?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>作为一名开发经理，Mike大部分时间都花在了会议以及与团队成员的一对一谈话上。周报是对一周会议和各种谈话的总结。通过写周报，可以对每周所做的事情有个整体的印象，还能从中总结出有用的信息。总得来说周报是个不错的工具。</p> <i>By 薛命灯</i>
---------------
<h1 id="#title_14" >15、User space 与 Kernel space</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2016/12/user_space_vs_kernel_space.html](http://www.ruanyifeng.com/blog/2016/12/user_space_vs_kernel_space.html)
<p>学习 Linux 时，经常可以看到两个词：User space（用户空间）和 Kernel space（内核空间）。</p>

        <p>简单说，Kernel space 是 Linux 内核的运行空间，User space 是用户程序的运行空间。为了安全，它们是隔离的，即使用户的程序崩溃了，内核也不受影响。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2016/bg2016120201-2.png" alt="" title="" /></p>

<p>Kernel space 可以执行任意命令，调用系统的一切资源；User space 只能执行简单的运算，不能直接调用系统资源，必须通过系统接口（又称 system call），才能向内核发出指令。</p>

<blockquote><pre><code class="language-clike">
str = "my string" // 用户空间
x = x + 2
file.write(str) // 切换到内核空间

y = x + 4 // 切换回用户空间
</code></pre></blockquote>

<p>上面代码中，第一行和第二行都是简单的赋值运算，在 User space 执行。第三行需要写入文件，就要切换到 Kernel space，因为用户不能直接写文件，必须通过内核安排。第四行又是赋值运算，就切换回 User space。</p>

<p>查看 CPU 时间在 User space 与 Kernel Space 之间的分配情况，可以使用<code>top</code>命令。它的第三行输出就是 CPU 时间分配统计。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2016/bg2016120202.jpg" alt="" title="" /></p>

<p>这一行有 8 项统计指标。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2016/bg2016120203-1.png" alt="" title="" /></p>

<p>其中，第一项<code>24.8 us</code>（user 的缩写）就是 CPU 消耗在 User space 的时间百分比，第二项<code>0.5 sy</code>（system 的缩写）是消耗在 Kernel space 的时间百分比。</p>

<p>随便也说一下其他 6 个指标的含义。</p>

<blockquote>
  <ul>
<li><code>ni</code>：niceness 的缩写，CPU 消耗在 nice 进程（低优先级）的时间百分比</li>
<li><code>id</code>：idle 的缩写，CPU 消耗在闲置进程的时间百分比，这个值越低，表示 CPU 越忙</li>
<li><code>wa</code>：wait 的缩写，CPU 等待外部 I/O 的时间百分比，这段时间 CPU 不能干其他事，但是也没有执行运算，这个值太高就说明外部设备有问题</li>
<li><code>hi</code>：hardware interrupt 的缩写，CPU 响应硬件中断请求的时间百分比</li>
<li><code>si</code>：software interrupt 的缩写，CPU 响应软件中断请求的时间百分比</li>
<li><code>st</code>：stole time 的缩写，该项指标只对虚拟机有效，表示分配给当前虚拟机的 CPU 时间之中，被同一台物理机上的其他虚拟机偷走的时间百分比</li>
</ul>
</blockquote>

<p>如果想查看单个程序的耗时，一般使用<code>time</code>命令。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2016/bg2016120204.jpg" alt="" title="" /></p>

<p>程序名之前加上<code>time</code>命令，会在程序执行完毕以后，默认显示三行统计。</p>

<blockquote>
  <ul>
<li><code>real</code>：程序从开始运行到结束的全部时间，这是用户能感知到的时间，包括 CPU 切换去执行其他任务的时间。</li>
<li><code>user</code>：程序在 User space 执行的时间</li>
<li><code>sys</code>：程序在 Kernel space 执行的时间</li>
</ul>
</blockquote>

<p><code>user</code>和<code>sys</code>之和，一般情况下，应该小于<code>real</code>。但如果是多核 CPU，这两个指标反映的是所有 CPU 的总耗时，所以它们之和可能大于<code>real</code>。</p>

<p>[参考链接]</p>

<blockquote>
  <ul>
<li></li>
<li></li>
<li> </li>
<li></li>
</ul>
</blockquote>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2016-12-02T08:06:28+08:00">2016年12月 2日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>购买文集：</li>
<li>社交媒体：</li>
<li>Feed订阅： </li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------
<h1 id="#title_15" >16、[Android] 我的第一款全栈 side project</h1>
iam_wingjay
[https://gold.xitu.io/entry/58415a75ac502e006bed35bd](https://gold.xitu.io/entry/58415a75ac502e006bed35bd)
<img src="https://dn-mhke0kuv.qbox.me/52885d4ffd342f38b9cf.jpeg?imageView/2/w/800/h/600/q/80/format/png"/><p>介绍了在一款 side project 开发中所积累一些的设计、Android 端、服务端三方面经验。</p><p></p>
---------------
<h1 id="#title_16" >17、[设计] 嘿，设计师，你可不是艺术家：成为一个商业设计师的 9 个贴士</h1>
逗砂
[https://gold.xitu.io/entry/58414df861ff4b00587fd535](https://gold.xitu.io/entry/58414df861ff4b00587fd535)
<img src="https://dn-mhke0kuv.qbox.me/660b628cb4736fbd8616.jpeg?imageView/2/w/800/h/600/q/80/format/png"/><p>不想当商人的艺术家不是一个好设计师╮(╯▽╰)╭</p><p></p>
---------------
<h1 id="#title_17" >18、[Android] OkHttp 更新 token 的解决方案</h1>
Zhiw
[https://gold.xitu.io/entry/584144d0128fe1006c3cfb8f](https://gold.xitu.io/entry/584144d0128fe1006c3cfb8f)
<p>Android 上 OkHttp 更新 Token 的解决方案</p><p></p>
---------------
<h1 id="#title_18" >19、.NET Standard 2.0：整齐划一的目标</h1>
Sergio De Simone
[http://www.infoq.com/cn/news/2016/12/dotnet-standard-20-goals?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2016/12/dotnet-standard-20-goals?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>最近结束的.NET Connect 2016大会上，几位微软MVP针对.NET标准的内容和未来发展谈论了自己的看法。</p> <i>By Sergio De Simone</i> <i> Translated by 大愚若智</i>
---------------
<h1 id="#title_19" >20、[工具资源] 你的名字。非官方命令行工具</h1>
秒速五蕾姆
[https://gold.xitu.io/entry/584182c379bc440065ad5e5c](https://gold.xitu.io/entry/584182c379bc440065ad5e5c)
<p>我会永远记住三叶的。</p><p></p>
---------------
<h1 id="#title_20" >21、[Android] listview  源码解析乱弹</h1>
fmlli
[https://gold.xitu.io/entry/58413cbb61ff4b006b8b0eb8](https://gold.xitu.io/entry/58413cbb61ff4b006b8b0eb8)
<p> 源码解析</p><p></p>
---------------
<h1 id="#title_21" >22、[Android] Android 跨进程通信 Aidl 的使用及注意事项 ---CSDN</h1>
小松
[https://gold.xitu.io/entry/58413c8579bc440065ab5535](https://gold.xitu.io/entry/58413c8579bc440065ab5535)
<img src="https://dn-mhke0kuv.qbox.me/b89be1be7a1fb11ec7c3.png?imageView/2/w/800/h/600/q/80/format/png"/><p>Android 跨进程通信传递数据，使用 Aidl 技术，底层是 Binder 实现，希望可以帮助到你。</p><p></p>
---------------
<h1 id="#title_22" >23、[Android] 数字增加动画的 TextView</h1>
Bakumon
[https://gold.xitu.io/entry/5841389fa22b9d006c147b5d](https://gold.xitu.io/entry/5841389fa22b9d006c147b5d)
<img src="https://dn-mhke0kuv.qbox.me/5360afe49a275d777498.jpg?imageView/2/w/800/h/600/q/80/format/png"/><p>数字增加动画的 TextView </p><p></p>
---------------
<h1 id="#title_23" >24、Web Development Reading List #161: Restyling Form Elements, HTTP/2 HPACK, And The Empathy Vacuum</h1>
Anselm Hannemann
[https://www.smashingmagazine.com/2016/12/web-development-reading-list-161/](https://www.smashingmagazine.com/2016/12/web-development-reading-list-161/)
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
</table><p><strong>Are you afraid of refactoring code?</strong> I <em>love</em> refactoring code. It’s nice to see a code base growing, but this also means that new quirks and suboptimal changes are introduced along the way. At some point, you might realize that there could be a huge opportunity in rewriting the code — to eliminate conflicts or to rename things.</p>
<figure></figure>
<p>For me, refactoring is both: It’s a challenge to master, but, in the end, also a relief to see how the code evolved. We can’t anticipate everything when we first build modules, and we shouldn’t try to do so either. So let’s not be afraid to set our hands to an already existing code base and improve our code over time instead.</p><p>The post .</p>
---------------