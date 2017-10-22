## 文章索引
1、 <a href="#1uglifyjs-315-发布javascript-压缩和美化工具包" >UglifyJS 3.1.5 发布，JavaScript 压缩和美化工具包</a><br/>
2、 <a href="#2napajs-微软开源的多线程-javascript-运行环境" >Napa.js —— 微软开源的多线程 JavaScript 运行环境</a><br/>
3、 <a href="#3vertx-350-发布基于-jvm-的-node-替代者" >Vert.x 3.5.0 发布，基于 JVM 的 Node 替代者</a><br/>
4、 <a href="#4协作翻译-|-为安卓开发者介绍的移动开发框架-flutter" >协作翻译 | 为安卓开发者介绍的移动开发框架 Flutter</a><br/>
5、 <a href="#5gitea-121-发布golang-编写的自助-git-服务" >Gitea 1.2.1 发布，Golang 编写的自助 Git 服务</a><br/>
6、 <a href="#6apache-commons-codec-111-版本正式发布" >Apache Commons Codec 1.11 版本正式发布</a><br/>
7、 <a href="#7谷歌或更新-chrome阻止浏览器运行挖矿程序" >谷歌或更新 Chrome：阻止浏览器运行挖矿程序</a><br/>
8、 <a href="#8wine-203-稳定版发布windows-应用兼容层" >Wine 2.0.3 稳定版发布，Windows 应用兼容层</a><br/>
9、 <a href="#9rocketchat-0591-发布slack-开源替代品" >Rocket.Chat 0.59.1 发布，Slack 开源替代品</a><br/>
10、 <a href="#10cphalcon-324-发布php-的-c-扩展-web-框架" >Cphalcon 3.2.4 发布，PHP 的 C 扩展 Web 框架</a><br/>
11、 <a href="#11微软和亚马逊联合推出深度学习库-gluon" >微软和亚马逊联合推出深度学习库 —— Gluon</a><br/>
12、 <a href="#12hibernate-orm-52-的第-12-个-bug-修复版本发布" >Hibernate ORM 5.2 的第 12 个 Bug 修复版本发布</a><br/>
13、 <a href="#13nideshop-微信小程序商城-添加微信支付功能" >NideShop 微信小程序商城 添加微信支付功能</a><br/>
14、 <a href="#14grafana-460-beta2-发布度量和分析仪表板" >Grafana 4.6.0 beta2 发布，度量和分析仪表板</a><br/>
15、 <a href="#15ublock-origin-因为屏蔽-csp-而遭受批评" >uBlock Origin 因为屏蔽 CSP 而遭受批评</a><br/>
16、 <a href="#16优麒麟-1710-正式版发布全新风格&全新体验" >优麒麟 17.10 正式版发布，全新风格&全新体验！</a><br/>
17、 <a href="#17每日一博-|-区块链之以太坊区块链技术初探" >每日一博 | 区块链之以太坊区块链技术初探</a><br/>
18、 <a href="#18scala-2124-发布编译时间再减少-5-10％" >Scala 2.12.4 发布，编译时间再减少 5-10％</a><br/>
19、 <a href="#19码云推荐-|-原生安卓编写的小游戏-honeycombsmazep" >码云推荐 | 原生安卓编写的小游戏 HoneycombsMazep</a><br/>
20、 <a href="#20hugo-0302-发布go-编写的静态网站生成器" >Hugo 0.30.2 发布，Go 编写的静态网站生成器</a><br/>
21、 <a href="#21element-200-beta1-发布基于-vue-20-的组件库" >Element 2.0.0-beta.1 发布，基于 Vue 2.0 的组件库</a><br/>
22、 <a href="#22周六乱弹-程序员的女朋友注意了当你男友说" >周六乱弹 —— 程序员的女朋友注意了，当你男友说：</a><br/>
23、 <a href="#23不只是阿里巴巴的操作系统alios-宣布开源" >不只是阿里巴巴的操作系统，AliOS 宣布开源</a><br/>
24、 <a href="#24facebook-开源帮助开发者消灭最顽固的软件-bug-的工具" >Facebook 开源帮助开发者消灭最顽固的软件 bug 的工具</a><br/>
25、 <a href="#25jekyll-361-发布静态站点生成器" >Jekyll 3.6.1 发布，静态站点生成器</a><br/>
26、 <a href="#26symfony-400-beta1-发布全堆栈-php-web-框架" >Symfony 4.0.0 beta1 发布，全堆栈 PHP Web 框架</a><br/>
27、 <a href="#27最新的-opensuse-tumbleweed-快照已移除-gcc-6" >最新的 openSUSE Tumbleweed 快照已移除 GCC 6</a><br/><h1 id="#title_0" >1、UglifyJS 3.1.5 发布，JavaScript 压缩和美化工具包</h1>

[https://www.oschina.net/news/89815/uglifyjs-3-1-5](https://www.oschina.net/news/89815/uglifyjs-3-1-5)
<p>UglifyJS v3.1.5 已发布，UglifyJS 是一个 JavaScript 的解析、分解、压缩和美化工具包：</p><ul class=" list-paddingleft-2"><li><p>一个从 JavaScript 代码中生成抽象语法树（AST）的解析器。</p></li><li><p>一个从 AST 输出 JavaScript 代码的代码生成器，并提供获取源路线的选项。</p></li><li><p>compressor (optimizer) - 它使用 transformer API 将 AST 优化至最小</p></li><li><p>mangler - 将局部变量的名称减少为（通常）单个字母</p></li><li><p>scope analyzer - 它是用于扩充 AST 的工具，其中包含了定义/引用变量的位置信息</p></li><li><p>tree walker- 一个简单的 API，可以让您在 AST 中的每个节点上执行某些操作</p></li><li><p>tree transformer -&nbsp;另一种用于转换 tree 的 API</p></li></ul><p>UglifyJS 3.0.0 版本需要特别注意的是：</p><ul class=" list-paddingleft-2"><li><p>uglify-js@3.x 有一个新的 API 和 CLI ，且不向后兼容 uglify-js@2.x</p></li></ul><p>该版本未找到具体的更新日志，详情查阅</p></li></ul>
---------------
<h1 id="#title_1" >2、Napa.js —— 微软开源的多线程 JavaScript 运行环境</h1>

[https://www.oschina.net/p/napajs](https://www.oschina.net/p/napajs)
<p><span style="color: rgb(17, 17, 17); font-family: &quot;PingFang SC&quot;, &quot;Helvetica Neue&quot;, &quot;Microsoft YaHei UI&quot;, &quot;Microsoft YaHei&quot;, &quot;Noto Sans CJK SC&quot;, Sathu, EucrosiaUPC, sans-serif; font-size: 16px; line-height: 25.888px; widows: 1; background-color: rgb(255, 255, 255);">Napa.js 是微软开源的一个基于 V8 的多线程 JavaScript 运行环境。</span></p>
---------------
<h1 id="#title_2" >3、Vert.x 3.5.0 发布，基于 JVM 的 Node 替代者</h1>

[https://www.oschina.net/news/89796/vertx-3-5-0](https://www.oschina.net/news/89796/vertx-3-5-0)
<p>Vert.x 3.5.0 正式版已发布。Vert.x 是一个用于下一代异步、可伸缩、并发应用的框架，旨在为JVM提供一个</p>
---------------
<h1 id="#title_3" >4、协作翻译 | 为安卓开发者介绍的移动开发框架 Flutter</h1>

[https://www.oschina.net/translate/intro-to-flutter-for-android-developers](https://www.oschina.net/translate/intro-to-flutter-for-android-developers)
<p>给各位安卓开发者介绍 Flutter 开发框架，欢迎加入 Dart 阵营</p>
---------------
<h1 id="#title_4" >5、Gitea 1.2.1 发布，Golang 编写的自助 Git 服务</h1>

[https://www.oschina.net/news/89817/gitea-1-2-1](https://www.oschina.net/news/89817/gitea-1-2-1)
<p>Gitea 1.2.1&nbsp;版本已发布。Gitea 的首要目标是创建一个极易安装，运行非常快速，安装和使用体验良好的自建 Git 服务。项目采用 Go 作为后端语言，只要生成一个可执行程序即可。并且他还支持跨平台，支持 Linux、 macOS 和 Windows 以及各种架构，除了x86、amd64，还包括 ARM 和 PowerPC。</p><p><img alt="" height="421" data-cke-saved-src="https://static.oschina.net/uploads/space/2017/1022/020828_9ian_2896879.jpg" src="https://static.oschina.net/uploads/space/2017/1022/020828_9ian_2896879.jpg" width="300"/></p><p>该版本包含5个用户提交的修复，分别如下：</p><ul class=" list-paddingleft-2"><li><p>Fix PR, milestone and label functionality if issue unit is disabled (</p>
---------------
<h1 id="#title_5" >6、Apache Commons Codec 1.11 版本正式发布</h1>

[https://www.oschina.net/news/89816/apache-commons-codec-1-11](https://www.oschina.net/news/89816/apache-commons-codec-1-11)
<p>Apache Commons Codec 1.11 已发布，Apache Commons Codec（TM）提供通用编码器和解码器的实现，如 Base64、Hex、Phonetic 和 URL 。<br/></p><p>该版本带来了许多新特性，以及大量修复和改变。部分新特性如下：</p><ul class=" list-paddingleft-2"><li><p>新增对 XXHash32 的支持</p></li><li><p>流畅的 DigestUtils 界面</p></li><li><p>流畅的 HmacUtils 接口</p></li><li><p>新增对 CRC32-C 的支持</p></li><li><p>新增 HmacAlgorithms.HMAC_SHA_224（仅&nbsp;Java 8）</p></li><li><p>支持 JEP 287：SHA-3 哈希算法</p></li><li><p>创建了一个最小的 Digest 命令行实用程序：org.apache.commons.codec.digest.Digest</p></li><li><p>新增 DigestUtils.getDigest（String，MessageDigest）</p></li><li><p>公开部分 DigestUtils API</p></li><li><p>将 java.io.File API 添加到 MessageDigestAlgorithm<br/></p></li></ul><p>完整内容请查阅</p>
---------------
<h1 id="#title_6" >7、谷歌或更新 Chrome：阻止浏览器运行挖矿程序</h1>

[https://www.oschina.net/news/89821/chrome-permission-to-block-malvertising-attempts](https://www.oschina.net/news/89821/chrome-permission-to-block-malvertising-attempts)
<p><img src="https://static.oschina.net/uploads/space/2017/1022/073416_Fc3S_2720166.jpg"/></p><p>加密货币的兴起，也引发了诸多的行业乱象。因为有些人没想着自行搭建挖矿平台，而是暗地里利用其他人的资源为自己谋利。<br/></p><p>早段时间，媒体曾报道过在受害者 PC 上挖矿的恶意软件。而现在，又有网站被爆出利用访客的设备来挖矿，比如海盗湾。为了杜绝这种以浏览器为入口、未经用户许可而让他们的设备消耗资源的行径，搜索巨头 Google 决定出手整治一番。</p><p>Chrome 工程师考虑反制方法，他们讨论了创建黑名单，在浏览器这一层次屏蔽挖矿代码，但这一提议被认为不切实际，被认为留给扩展做更好。<br/></p><p>据&nbsp;</p>
---------------
<h1 id="#title_7" >8、Wine 2.0.3 稳定版发布，Windows 应用兼容层</h1>

[https://www.oschina.net/news/89814/wine-2-0-3](https://www.oschina.net/news/89814/wine-2-0-3)
<p>Wine 已发布新的 2.0.3 稳定版。Wine （“Wine Is Not an Emulator” 的首字母缩写）是一个能够在多种 POSIX-compliant 操作系统（诸如 Linux，macOS 及 BSD 等）上运行 Windows 应用的兼容层。Wine 不是像虚拟机或者模拟器一样模仿内部的 Windows 逻辑，而是将&nbsp;Windows API 调用翻译成为动态的 POSIX 调用，免除了性能和其他一些行为的内存占用，让你能够干净地集合 Windows 应用到你的桌面。<br/></p><p>更新内容：</p><ul class=" list-paddingleft-2"><li><p>各种 bug 修复</p></li><li><p>修复了对 FreeType 2.8.1 的兼容性问题</p></li></ul><p>下载地址：</p><p></p>
---------------
<h1 id="#title_8" >9、Rocket.Chat 0.59.1 发布，Slack 开源替代品</h1>

[https://www.oschina.net/news/89813/rocketchat-0-59-1](https://www.oschina.net/news/89813/rocketchat-0-59-1)
<p>Rocket.Chat 0.59.1 已发布，Rocket.Chat 是特性最丰富的 Slack 开源替代品之一。</p><p>主要功能：群组聊天，直接通信，私聊群，桌面通知，媒体嵌入，链接预览，文件上传，语音/视频 聊天，截图等等。</p><p>Rocket.Chat 原生支持 Windows，Mac OS X ，Linux，iOS 和 Android 平台。Rocket.Chat 通过</p></li></ul>
---------------
<h1 id="#title_9" >10、Cphalcon 3.2.4 发布，PHP 的 C 扩展 Web 框架</h1>

[https://www.oschina.net/news/89812/cphalcon-3-2-4](https://www.oschina.net/news/89812/cphalcon-3-2-4)
<p>Cphalcon 3.2.4 已发布，Cphalcon 是一个开源的 Web 框架，作为 PHP 语言 C 扩展，它提供了更高的性能与更低的资源消耗。<br/></p><p>更新内容：</p><ul class=" list-paddingleft-2"><li><p>Fixed regression of&nbsp;</p></li></ul>
---------------
<h1 id="#title_10" >11、微软和亚马逊联合推出深度学习库 —— Gluon</h1>

[https://www.oschina.net/p/gluon](https://www.oschina.net/p/gluon)
<p>Gluon 是微软联合亚马逊推出的一个开源深度学习库，这是一个清晰、简洁、简单但功能强大的深度学习 API，该规范可以为开发人员快速学习深度学习速度，而不需要关心所选择的深度学习框架。Gluon API 提供了灵活的接口来简化深度学习原型设计、创建、训练以及部署，而且不会牺牲数据训练的速度。</p>
---------------
<h1 id="#title_11" >12、Hibernate ORM 5.2 的第 12 个 Bug 修复版本发布</h1>

[https://www.oschina.net/news/89810/hibernate-orm-5212-final-release](https://www.oschina.net/news/89810/hibernate-orm-5212-final-release)
<div id="preamble">
<div class="sectionbody">
<div class="paragraph">
<p>Hibernate ORM 5.2 的第 12 个 Bug 修复版本发布了，该版本主要是 Bug 修复，下面是修复的 Bug 列表：</p>
</div>
</div>
</div>
<div class="sect1">
<div class="sectionbody">
<div class="ulist">
<ul>
<li>
<p>tag is ;</p>
</li>
<li>
<p>changes are listed );</p>
</li>
<li>
<p>release bundles are at .</p>
</li>
</ul>
</div>
<div class="paragraph">
<p>详细信息请看&nbsp;</p>
</div>
</div>
</div>
---------------
<h1 id="#title_12" >13、NideShop 微信小程序商城 添加微信支付功能</h1>

[https://www.oschina.net/news/89809/nideshop-wechat-pay](https://www.oschina.net/news/89809/nideshop-wechat-pay)
<p>NideShop 是一款基于Node.js开发的微信小程序商城，开源免费，无论是个人还是公司使用都无需授权。</p><p>本次更新：</p><ol class=" list-paddingleft-2"><li><p>添加微信支付功能</p></li><li><p>修复微信登录失败</p></li><li><p>添加微信配置到 src/common/config/config.js</p></li></ol>
---------------
<h1 id="#title_13" >14、Grafana 4.6.0 beta2 发布，度量和分析仪表板</h1>

[https://www.oschina.net/news/89820/grafana-4-6-0-beta2](https://www.oschina.net/news/89820/grafana-4-6-0-beta2)
<p>Grafana 4.6.0 beta2 已发布，这是一个 Bug 修复版本，更新内容如下：</p><ul class=" list-paddingleft-2"><li><p>ColorPicker: 修复颜色选择器不显示的问题&nbsp;</p></li></ul>
---------------
<h1 id="#title_14" >15、uBlock Origin 因为屏蔽 CSP 而遭受批评</h1>

[https://www.oschina.net/news/89807/ublock-origin-criticized-for-blocking-csp](https://www.oschina.net/news/89807/ublock-origin-criticized-for-blocking-csp)
<p>uBlock Origin 被发现如果使用了特定的脚本，将会阻止 CSP 使用它网站上的报告。</p><p>CSP 指的是内容安全策略，为了缓解很大一部分潜在的跨站脚本问题，浏览器的扩展程序系统引入了内容安全策略(CSP)的一般概念。这将引入一些相当严格的策略，会使扩展程序在默认情况下更加安全，开发者可以创建并强制应用一些规则，管理网站允许加载的内容。</p><p>uBlock Origin 的开发者 Raymond Hill 回应说，这不是一个错误，而是有意设计成这样的。如果 CSP 报告注入了特定的 Google Analytics 脚本，该扩展将阻止发送 CSP 报告。</p><p><img src="https://static.oschina.net/uploads/space/2017/1021/083058_rame_3703517.png"/></p><p>浏览器扩展 uBlock Origin 屏蔽 Google Analytics 以防止用户跟踪。这是由于某些网站如果未正确加载 Google Analytics 将不能正常运行，因此将注入一个特定的脚本，以减少网站破坏的可能性。</p><p>uBlock Origin 表示它代表了用户方面的利益，如果对远程服务器的网络请求可能对用户造成不利影响，则会被阻止。此外，还有些第三方网站可能存在滥用用户跟踪系统的情况，这也是为什么这些报告会在 uBlock Origin 中被阻止的原因。</p><p>Raymond Hill 表示将在不久的将来发布更新的 WebExtensions 版本的 uBlock Origin，区分了注入中断脚本和常规 CSP 报告引起的屏蔽情况。</p><p>编译自：</p>
---------------
<h1 id="#title_15" >16、优麒麟 17.10 正式版发布，全新风格&全新体验！</h1>

[https://www.oschina.net/news/89806/ubuntu-kylin-17-10](https://www.oschina.net/news/89806/ubuntu-kylin-17-10)
<p>优麒麟团队已正式发布优麒麟(Ubuntu&nbsp;Kylin)&nbsp;17.10开源操作系统（版本代号Artful&nbsp;Aardvark）。此次发布在系统内核、桌面环境、特色应用、合作软件上都有一系列细腻而实用的更新。同时发布的还有&nbsp;Ubuntu&nbsp;17.10、Lubuntu&nbsp;17.10、Ubuntu&nbsp;Mate&nbsp;17.10&nbsp;等开源发行版。</p>
---------------
<h1 id="#title_16" >17、每日一博 | 区块链之以太坊区块链技术初探</h1>

[https://my.oschina.net/linapex/blog/1553703](https://my.oschina.net/linapex/blog/1553703)
<p>区块链的概念最近很火，它来自于比特币等加密货币的实现，但是目前，这项技术已经逐步运用在各个领域。</p>
---------------
<h1 id="#title_17" >18、Scala 2.12.4 发布，编译时间再减少 5-10％</h1>

[https://www.oschina.net/news/89804/scala-2-12-4](https://www.oschina.net/news/89804/scala-2-12-4)
<p>Scala 2.12.4 已发布，与上个版本比较，</p>
---------------
<h1 id="#title_18" >19、码云推荐 | 原生安卓编写的小游戏 HoneycombsMazep</h1>

[https://gitee.com/raybest4u/HoneycombsMazep](https://gitee.com/raybest4u/HoneycombsMazep)
<p>用原生安卓编写一个小游戏 游戏是按照《最强大脑》中“蜂巢迷宫”为原型，锻炼用户记忆和空间思维能力 适合初学者学习。</p>
---------------
<h1 id="#title_19" >20、Hugo 0.30.2 发布，Go 编写的静态网站生成器</h1>

[https://www.oschina.net/news/89819/hugo-0-30-2](https://www.oschina.net/news/89819/hugo-0-30-2)
<p>Hugo 0.30.2 已发布，Hugo 是 Go 编写的静态网站生成器，速度快，易用，可配置。Hugo 有一个内容和模板目录，把他们渲染到完全的 HTML 网站。</p><p>该版本通过 baseURL 中的子路径修复了快速渲染模式&nbsp;。</p>
---------------
<h1 id="#title_20" >21、Element 2.0.0-beta.1 发布，基于 Vue 2.0 的组件库</h1>

[https://www.oschina.net/news/89801/element-2-0-0-beta1](https://www.oschina.net/news/89801/element-2-0-0-beta1)
<p>Element 2.0.0 beta1 已发布，意味着离 2.0 正式版又近了一步。<br/></p><p>Element 是饿了么开源的一套为开发者、设计师和产品经理准备的基于 Vue 2.0 的组件库，提供了配套设计资源，帮助你的网站快速成型。<br/></p><h4>新特性</h4><ul class=" list-paddingleft-2"><li><p>综合</p></li><ul class=" list-paddingleft-2" style="list-style-type: square;"><li><p>新增 TypeScript 类型声明</p></li><li><p>重绘了全部图标，并新增了部分图标</p></li><li><p>为部分非兼容性更新增加控制台警告，方便迁移项目。当你在项目中使用了被移除或更名了的属性或事件时，控制台会出现一条警告，例如：</p><pre data-cke-widget-data="%7B%22code%22%3A%22%5BElement%20Migrating%5D%5BElSwitch%5D%5BAttribute%5D%3A%20on-color%20is%20renamed%20to%20active-color.%5Cn%22%2C%22classes%22%3Anull%7D" data-cke-widget-upcasted="1" data-cke-widget-keep-attr="0" data-widget="codeSnippet" class="cke_widget_element">[Element&nbsp;Migrating][ElSwitch][Attribute]:&nbsp;on-color&nbsp;is&nbsp;renamed&nbsp;to&nbsp;active-color.</pre><p><span class="cke_reset cke_widget_drag_handler_container" style="background: url(&quot;https://my.oschina.net/dist/www/vendor/ckeditor/4.5.8/plugins/widget/images/handle.png&quot;) rgba(220, 220, 220, 0.5); top: -15px; left: 0px; display: block;"></span></p></li><li><p>新增了一系列基于断点的工具类，用于当视口尺寸满足一定条件时隐藏元素</p></li></ul><li><p>Layout</p></li><ul class=" list-paddingleft-2" style="list-style-type: square;"><li><p>新增断点&nbsp;<code>xl</code>，适用于宽度大于 1920px 的视口</p></li></ul><li><p>Table</p></li><ul class=" list-paddingleft-2" style="list-style-type: square;"><li><p>新增&nbsp;<code>span-method</code>&nbsp;属性，用于合并行或列</p></li><li><p>新增&nbsp;<code>clearSort</code>&nbsp;方法，用于清空排序状态</p></li><li><p>新增&nbsp;<code>clearFilter</code>&nbsp;方法，用于清空过滤状态</p></li><li><p>对于可展开行，当该行展开时会获得一个&nbsp;<code>.expanded</code>&nbsp;类名，方便自定义样式</p></li></ul><li><p>DatePicker</p></li><ul class=" list-paddingleft-2" style="list-style-type: square;"><li><p>新增&nbsp;<code>unlink-panels</code>&nbsp;属性，用于在选择日期范围时取消两个日期面板之间的联动</p></li></ul><li><p>Select</p></li><ul class=" list-paddingleft-2" style="list-style-type: square;"><li><p>新增&nbsp;<code>reserve-keyword</code>&nbsp;属性，用于在选择某个选项后保留当前的搜索关键词</p></li></ul></ul><h4>修复</h4><ul class=" list-paddingleft-2"><li><p>Table</p></li><ul class=" list-paddingleft-2" style="list-style-type: square;"><li><p>修复 TableColumn 的&nbsp;<code>header-align</code>&nbsp;属性失效的问题</p></li><li><p>修复 Table 在父元素从&nbsp;<code>display: none</code>&nbsp;变成其他状态时会隐藏的问题</p></li><li><p>修复 Table 在父元素为&nbsp;<code>display: flex</code>&nbsp;时可能出现的宽度逐渐变大的问题</p></li><li><p>修复&nbsp;<code>append</code>&nbsp;具名 slot 和固定列并存时，动态获取表格数据会导致固定列消失的问题</p></li><li><p>修复&nbsp;<code>expand-row-keys</code>&nbsp;属性初始化无效的问题</p></li><li><p>修复&nbsp;<code>data</code>&nbsp;改变时过滤条件失效的问题</p></li><li><p>修复多级表头时固定列隐藏情况计算错误的问题</p></li></ul></ul><h4>非兼容性更新</h4><ul class=" list-paddingleft-2"><li><p>Switch</p></li><ul class=" list-paddingleft-2" style="list-style-type: square;"><li><p>由于&nbsp;<code>on-*</code>&nbsp;属性在 JSX 中会被识别为事件，导致 Switch 所有&nbsp;<code>on-*</code>&nbsp;属性在 JSX 中无法正常工作，所以&nbsp;<code>on-*</code>&nbsp;属性更名为&nbsp;<code>active-*</code>，对应地，<code>off-*</code>&nbsp;属性更名为&nbsp;<code>inactive-*</code>。受到影响的属性有：<code>on-icon-class</code>、<code>off-icon-class</code>、<code>on-text</code>、<code>off-text</code>、<code>on-color</code>、<code>off-color</code>、<code>on-value</code>、<code>off-value</code></p></li></ul><li><p>Table</p></li><ul class=" list-paddingleft-2" style="list-style-type: square;"><li><p><code>sort-method</code>&nbsp;现在和&nbsp;<code>Array.sort</code>&nbsp;保持一致的逻辑，要求返回一个数字。</p></li></ul></ul><h4>下载地址：</h4><ul class=" list-paddingleft-2"><li><p></p></li></ul>
---------------
<h1 id="#title_21" >22、周六乱弹 —— 程序员的女朋友注意了，当你男友说：</h1>

[https://my.oschina.net/xxiaobian/blog/1554205](https://my.oschina.net/xxiaobian/blog/1554205)
<p>一大早被对面的洗衣机吵醒。叫醒我的不是梦想，是对面的洗衣机...</p>
---------------
<h1 id="#title_22" >23、不只是阿里巴巴的操作系统，AliOS 宣布开源</h1>

[https://www.oschina.net/news/89799/alios-announces-open-source](https://www.oschina.net/news/89799/alios-announces-open-source)
<p>今天，<strong>AliOS家族旗下面向IoT领域的轻量级物联网嵌入式操作系统AliOS Things正式开源。</strong></p><p>对于AliOS开源，阿里巴巴集团资深副总裁、AliOS总裁胡晓明谈及他的观点，他认为操作系统不应该仅仅是阿里的操作系统，希望通过把AliOS开源，让OS变成各行各业大家的OS。</p><p>他表示，未来阿里将关注最底层的研发，并且把生态环境建设好，和各行各业发生化学反应，让智能发生。</p><p>目前，智能多端的发展还处于起步阶段，距离真正实现万物智能还有很长的路要走。</p><p><img src="https://static.oschina.net/uploads/space/2017/1021/080231_5KCC_3703517.jpg"/></p><p>而目前的行业变化对操作系统的发展提出了三方面的挑战：首先，行业需求呈现多样性、碎片化的趋势，以手机为基础的操作系统并不能满足多端的定制化需求；云服务已经成为终端智能的基础设施，而手机操作系统仍然以端为中心，不是云端一体化的的操作系统；第三，智能硬件的软硬件创新成本相对手机提升，市场呼唤更合适的操作系统及其生态。</p><p>AliOS在多端应用场景下已经做了一些尝试，包括在汽车、消费电子领域，以及新零售、金融和教育领域等，和芯片厂商、集成商一起紧密合作，也获得了一些成果。<strong>AliOS将把操作系统和能力开放出来，让广大的设备厂商以及更多的设备集成商和OEM获益。</strong></p><p>AliOS面向多端可配置，四个软件层分别面向设备厂商、芯片厂商、设备方案商、中间技术商，系统设计严格遵循CPL可配置原则，模块内部实现高内聚、模块间依赖松耦合，插件化设计，可按需加载，禁止反向依赖，在保证更高可定制化的同时，不破坏系统兼容性。</p><p>AliOS将把系统开放给更多的合作伙伴，同时将提供硬件抽象层的开发指南、完善的测试集合以及最佳的工程实践经验，也将和更多的硬件厂商一起合作提供参考方案，从而降低行业定制的门槛。操作系统开源会加速生态的发展，但高度的碎片化不利于生态玩家，因此AliOS将提供两级认证，包括硬件兼容认证和软件兼容认证，持续为多端智能进行赋能。</p><p>AliOS还将推出硬件设计中心并开放，为软件制造商与硬件制造商搭建沟通需求的桥梁，并携手ISV和厂商，面向四大领域提供参考方案，支持客户定制。</p><p>了让开发者更关注应用和开发、部署和迭代，AliOS Things会为开发者提供一个功能强大、好用的工具，其核心组件包括一个轻量级的实时内核、低功耗引擎、连接协议，还包括安全组件、uMesh自组网、语音交互、多变升级云连接SDK，除了OS本身还将提供一个集成开发环境，让开发者能基于这个IDE更方便地做开发。</p><p><img src="https://static.oschina.net/uploads/space/2017/1021/080258_Sy9J_3703517.jpg"/></p><p>转自：。</p>
---------------
<h1 id="#title_23" >24、Facebook 开源帮助开发者消灭最顽固的软件 bug 的工具</h1>

[https://www.oschina.net/news/89798/facebook-open-source-development-tools-racerd](https://www.oschina.net/news/89798/facebook-open-source-development-tools-racerd)
<p>有一种软件bug是开发复杂软件项目开发者的噩梦，那就是代码中的竞态（Race Condition，也被译作竞争条件）引发的软件bug，近日Facebook开源了开发工具RacerD，来帮助开发者检查并预防Race Condition bug。<br/></p><p><img alt="" data-cke-saved-src="https://static.oschina.net/uploads/space/2017/1021/073431_JwPk_3703517.jpg" src="https://static.oschina.net/uploads/space/2017/1021/073431_JwPk_3703517.jpg" style="width: 800px; height: 400px;"/><br/></p><p>Race Condition是程序在多线程多任务处理时，对有些共享资源进行操作（例如两个进程同时修改同一个数据时），导致整个处理过程变得混乱甚至锁死，引发BUG。</p><p>Race Condition查找起来非常困难，开发者很难彻查一个app中所有的潜在问题，因为Race Condition引发的bug并不持续，因此难以诊断。</p><p>Facebook科学家Peter O‘Hearn在接受采访时指出，RacerD能查出大多数race condition导致的bug，虽然不能保证全部。</p><p>据悉，Facebook的Android应用开发团队在迭代新闻源并发功能（可将app性能提升5%）时使用RacerD找到来超过1000个race condition bug。</p><p>目前RacerD兼容Java，下一步Facebook将进一步开发使RacerD能够兼容C++。</p><p>转自：。</p>
---------------
<h1 id="#title_24" >25、Jekyll 3.6.1 发布，静态站点生成器</h1>

[https://www.oschina.net/news/89797/jekyll-3-6-1](https://www.oschina.net/news/89797/jekyll-3-6-1)
<p>Jekyll 3.6.1 已发布。Jekyll 是一个简单的博客形态的静态站点生成器，适用于个人、项目或组织站点。可以想像它是一个基于文件的 CMS ，没有任何复杂性。 Jekyll 收集你的内容，呈现 Markdown 和 Liquid 模板，并生成一个完整的静态网站，可以由 Apache、Nginx 或其他 Web 服务器提供服务。<br/></p><p>文档改进</p><ul class=" list-paddingleft-2"><li><p>Doc y_day in docs/permalinks</p></li><li><p>Update frontmatter.md</p></li><li><p>Elaborate on excluding items from processing</p></li><li><p>Style lists in tables</p></li><li><p>Remove duplicate `available`&nbsp;</p></li></ul><p>开发修复</p><ul class=" list-paddingleft-2"><li><p>Bump rubocop to use `v0.50.x`&nbsp;</p></li></ul><p>下载地址：</p><ul class=" list-paddingleft-2"><li><p></p></li></ul>
---------------
<h1 id="#title_25" >26、Symfony 4.0.0 beta1 发布，全堆栈 PHP Web 框架</h1>

[https://www.oschina.net/news/89818/symfony-4-0-0-beta1](https://www.oschina.net/news/89818/symfony-4-0-0-beta1)
<p>Symfony 已发布全新的 4.0.0 首个测试版本，Symfony 是一个基于 MVC 模式的面向对象的 PHP Web 框架。基于最佳 Web 开发实践，已经有多个网站完全采用此框架开发，symfony 的目的是加速 Web 应用的创建与维护。</p><p>4.0 版本带来了大量的新特性，完整内容请查阅</p></li></ul>
---------------
<h1 id="#title_26" >27、最新的 openSUSE Tumbleweed 快照已移除 GCC 6</h1>

[https://www.oschina.net/news/89795/gnu-compiler-collection-6-removed-from-tumbleweed](https://www.oschina.net/news/89795/gnu-compiler-collection-6-removed-from-tumbleweed)
<p><img src="https://static.oschina.net/uploads/space/2017/1021/082246_BbGX_3703517.png"/></p><p>本周&nbsp;</p>
---------------