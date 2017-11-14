## 文章索引
1、 <a href="#1wine-221-发布windows-应用兼容层" >Wine 2.21 发布，Windows 应用兼容层</a><br/>
2、 <a href="#2libuv-1161-发布node-的跨平台异步-io-库" >Libuv 1.16.1 发布，Node 的跨平台异步 IO 库</a><br/>
3、 <a href="#3ant-design-21310-发布阿里企业级-ui-设计语言" >Ant Design 2.13.10 发布，阿里企业级 UI 设计语言</a><br/>
4、 <a href="#4dbeaver-425-发布数据库管理工具" >DBeaver 4.2.5 发布，数据库管理工具</a><br/>
5、 <a href="#5calibre-312-发布开源电子书管理软件" >Calibre 3.12 发布，开源电子书管理软件</a><br/>
6、 <a href="#6apache-phoenix-413-发布hbase-的-sql-驱动" >Apache Phoenix 4.13 发布，HBase 的 SQL 驱动</a><br/>
7、 <a href="#7p6spy-360-正式版发布sql-语句拦截" >P6Spy 3.6.0 正式版发布，SQL 语句拦截</a><br/>
8、 <a href="#8lighttpd-1448-发布高性能-web-服务器" >Lighttpd 1.4.48 发布，高性能 Web 服务器</a><br/>
9、 <a href="#9gitlab-社区版和企业版发布-1013-补丁版本" >GitLab 社区版和企业版发布 10.1.3 补丁版本</a><br/>
10、 <a href="#10puppeteer-013-发布headless-chrome-node-api" >Puppeteer 0.13 发布，Headless Chrome Node API</a><br/>
11、 <a href="#11deruv-v095-发布内容管理系统" >Deruv v0.9.5 发布，内容管理系统</a><br/>
12、 <a href="#12每日一博-|-使用-spring-cloud-sleuth-实现链路监控" >每日一博 | 使用 Spring Cloud Sleuth 实现链路监控</a><br/>
13、 <a href="#13协作翻译-|-了解-ai-与机器学习之深度学习基础指南" >协作翻译 | 了解 AI 与机器学习之深度学习基础指南</a><br/>
14、 <a href="#14码云推荐-|-安全支付输入框-lypaymentfield" >码云推荐 | 安全支付输入框 LYPaymentField</a><br/>
15、 <a href="#15deepin-clone-深度备份还原工具" >Deepin Clone —— 深度备份还原工具</a><br/>
16、 <a href="#16oschina-周日乱弹-拆散她们帮她们过节" >OSChina 周日乱弹 —— 拆散她们，帮她们过节！</a><br/>
17、 <a href="#17go-语言开源发布-8-周年成-2017-年增长最快语言" >Go 语言开源发布 8 周年，成 2017 年增长最快语言</a><br/>
18、 <a href="#18hutool-320-发布java-工具集" >Hutool 3.2.0 发布，Java 工具集</a><br/><h1 id="#title_0" >1、Wine 2.21 发布，Windows 应用兼容层</h1>

[https://www.oschina.net/news/90519/wine-2-21](https://www.oschina.net/news/90519/wine-2-21)
<p>Wine 2.21&nbsp;已发布。Wine （“Wine Is Not an Emulator” 的首字母缩写）是一个能够在多种 POSIX-compliant 操作系统（诸如 Linux，macOS 及 BSD 等）上运行 Windows 应用的兼容层。Wine 不是像虚拟机或者模拟器一样模仿内部的 Windows 逻辑，而是将&nbsp;Windows API 调用翻译成为动态的 POSIX 调用，免除了性能和其他一些行为的内存占用，让你能够干净地集合 Windows 应用到你的桌面。<br/></p><p>更新内容：</p><ul class=" list-paddingleft-2"><li><p>Still more metafile support in GdiPlus.</p></li><li><p>Indirect draws support in Direct 3D.</p></li><li><p>Calling convention fixes on ARM.</p></li><li><p>Improved serial port detection on Linux.</p></li><li><p>Services fixes on WoW64.</p></li><li><p>Better DPI scaling in the Shell Explorer.</p></li><li><p>Various bug fixes.</p></li></ul><p>下载地址：</p><ul class=" list-paddingleft-2"><li><p></p></li></ul>
---------------
<h1 id="#title_1" >2、Libuv 1.16.1 发布，Node 的跨平台异步 IO 库</h1>

[https://www.oschina.net/news/90494/libuv-1-16-1](https://www.oschina.net/news/90494/libuv-1-16-1)
<p>Libuv 1.16.1&nbsp;已发布，&nbsp;更新如下：</p><ul class=" list-paddingleft-2"><li><p>unix: move net/if.h include</p></li><li><p>win: fix undeclared NDIS_IF_MAX_STRING_SIZE</p></li></ul><p>Libuv&nbsp;是一个专注于异步 &nbsp;I/O 的多平台支持库，主要用于 Node.js。</p><p>特性包括：</p><ul class=" list-paddingleft-2"><li><p>非阻塞 TCP 套接字</p></li><li><p>非阻塞命名管道</p></li><li><p>UDP</p></li><li><p>定时器</p></li><li><p>子进程生成</p></li><li><p>通过 uv_getaddrinfo 实现异步 DNS</p></li><li><p>异步文件系统 API：uv_fs_*</p></li><li><p>高分辨率时间：uv_hrtime</p></li><li><p>正在运行程序路径查找：uv_exepath</p></li><li><p>线程池调度：uv_queue_work</p></li><li><p>TTY控制的ANSI转义代码: uv_tty_t</p></li><li><p>文件系统事件现在支持 inotify, ReadDirectoryChangesW 和 kqueue。很快会支持事件端口：uv_fs_event_t</p></li><li><p>进程间的 IPC 与套接字共享：uv_write2</p></li></ul><p>下载地址：</p><ul class=" list-paddingleft-2"><li><p></p></li></ul>
---------------
<h1 id="#title_2" >3、Ant Design 2.13.10 发布，阿里企业级 UI 设计语言</h1>

[https://www.oschina.net/news/90518/ant-design-2-13-10](https://www.oschina.net/news/90518/ant-design-2-13-10)
<p>Ant Design 2.13.10 已发布，Ant Design 是蚂蚁金服开发和正在使用的一套企业级的 UI 设计语言和 React 实现。</p><p>更新内容：</p><ul class=" list-paddingleft-2"><li><p>添加&nbsp;</p></li></ul>
---------------
<h1 id="#title_3" >4、DBeaver 4.2.5 发布，数据库管理工具</h1>

[https://www.oschina.net/news/90517/dbeaver-4-2-5](https://www.oschina.net/news/90517/dbeaver-4-2-5)
<p>DBeaver 4.2.5&nbsp;已发布。DBeaver 是一个通用的数据库管理工具和 SQL 客户端，支持 MySQL, PostgreSQL, Oracle, DB2, MSSQL, Sybase, Mimer, HSQLDB, Derby, 以及其他兼容 JDBC 的数据库。</p><p>更新内容：</p><ul class=" list-paddingleft-2"><li><p>改进 Connection/schema selectors UI</p></li><li><p>新增&nbsp;connection schema select&nbsp;快捷键(CTRL+9, CTRL+0)</p></li><li><p>修复 SQL&nbsp;错误句柄&nbsp;(错误类型检测、重新连接激活)</p></li><li><p>修复 SELECT COUNT(*) transformer</p></li><li><p>SQL completion:&nbsp;多个&nbsp;bug&nbsp;修复</p></li><li><p>SQL editor: 单行注释切换修复</p></li><li><p>SQL editor: 脚本执行 UI 配置&nbsp;(编辑器窗格最大化现在可配置)</p></li><li><p>SQL editor: 支持关联另一个项目的连接</p></li><li><p>Database editor: 不影响数据编辑器的情况下自动保存</p></li><li><p>Results viewer: varchar 以二进制列查看&nbsp;transformer</p></li><li><p>Results viewer:&nbsp;修复状态标签</p></li><li><p>Results viewer:&nbsp;修复 timestamp value&nbsp;编辑器</p></li><li><p>PostgreSQL:&nbsp;view&nbsp;DDL&nbsp;修复</p></li><li><p>MySQL/MariaDB:&nbsp;修复 quoted schema name handle&nbsp;</p></li><li><p>Oracle: 修复 DATE 数据类型支持</p></li><li><p>Oracle: execution plan for queries with parameters</p></li><li><p>Oracle:&nbsp;改进会话 SQL 读取</p></li><li><p>SQL Server: native timestamp format&nbsp;修复</p></li><li><p>Data search: UI&nbsp;修复&nbsp;(性能)</p></li><li><p>MetaData search: UI&nbsp;修复&nbsp;(树结构)</p></li><li><p>ER diagrams:项目浏览器中的数据源信息</p></li><li><p>SSH tunnel&nbsp;配置改进 (本地端口号)</p></li><li><p>i18n model&nbsp;改进</p></li><li><p>汉化</p></li><li><p>Hex editor UI&nbsp;修复&nbsp;(hex panel stretching, preferences)</p></li><li><p>键盘快捷键修复</p></li><li><p>新增 Cloudera Impala driver config</p></li><li><p>新增 CUBRID driver config</p></li><li><p>Office&nbsp;和&nbsp;SVG 扩展移至独立的更新站点</p></li><li><p>其他 UI 修复</p></li></ul><p>具体内容可查阅</p>
---------------
<h1 id="#title_4" >5、Calibre 3.12 发布，开源电子书管理软件</h1>

[https://www.oschina.net/news/90516/calibre-3-12](https://www.oschina.net/news/90516/calibre-3-12)
<p>Calibre 3.12 已发布，Calibre 是一款功能强大的电子书管理软件，支持 Amazon、Apple、Bookeen、Ectaco、Endless Ideas、Google/HTC、Hanlin Song 设备及格式。</p><p><strong>主要更新内容：</strong></p><p>新特性</p><ul class=" list-paddingleft-2"><li><p>Driver for the new Nook Glowlight 3</p><p>Closes tickets:&nbsp;</p></li></ul>
---------------
<h1 id="#title_5" >6、Apache Phoenix 4.13 发布，HBase 的 SQL 驱动</h1>

[https://www.oschina.net/news/90515/apache-phoenix-4-13](https://www.oschina.net/news/90515/apache-phoenix-4-13)
<p>Apache Phoenix 4.13&nbsp;已发布，Apache Phoenix 是&nbsp;</p>
---------------
<h1 id="#title_6" >7、P6Spy 3.6.0 正式版发布，SQL 语句拦截</h1>

[https://www.oschina.net/news/90520/p6spy-3-6-0](https://www.oschina.net/news/90520/p6spy-3-6-0)
<p>P6Spy 3.6.0&nbsp;已发布。<br/></p><p>P6Spy 是一个可以用来在应用程序中拦截和修改数据操作语句的开源框架。 通过 P6Spy 我们可以对 SQL 语句进行拦截，相当于一个 SQL 语句的记录器，这样我们可以用它来作相关的分析，比如性能分析。<br/></p><p>该版本对 boolean parameters （布尔参数）进行了改进，已可配置格式。</p></li></ul>
---------------
<h1 id="#title_7" >8、Lighttpd 1.4.48 发布，高性能 Web 服务器</h1>

[https://www.oschina.net/news/90513/lighttpd-1-4-48](https://www.oschina.net/news/90513/lighttpd-1-4-48)
<p>Lighttpd 1.4.48 已发布，Lighttpd 是一个开源 Web 服务器软件，旨在提供一个专门针对高性能网站，安全、快速、兼容性好并且灵活的 Web Server 环境。具有非常低的内存开销，CPU 占用率低，效能好，以及丰富的模块等特点。</p><p>重要更改</p><ul class=" list-paddingleft-2"><li><p>mod_authn_sasl (新), meson build system (新), revamp build systems</p></li><li><p>bug&nbsp;修复</p></li></ul><p>下载地址：</p><ul class=" list-paddingleft-2"><li><p>)</p></li><li><p>[core] fix dup typedef compiler warning</p></li><li><p>[scons] fix various python2/3 incompatibilities</p></li><li><p>[doc] fix doc/config/conf.d/fastcgi.conf example</p></li></ul>
---------------
<h1 id="#title_8" >9、GitLab 社区版和企业版发布 10.1.3 补丁版本</h1>

[https://www.oschina.net/news/90512/gitlab-10-1-3](https://www.oschina.net/news/90512/gitlab-10-1-3)
<p>GitLab 发布 10.1.3 补丁版本，包括社区版和企业版。</p><p>该版本主要是 Bug 的修复，包括：</p><ul class=" list-paddingleft-2"><li><p><strong>CE/EE:</strong>&nbsp;Fix diff parser so it tolerates to diff special markers in the content (</p>
---------------
<h1 id="#title_9" >10、Puppeteer 0.13 发布，Headless Chrome Node API</h1>

[https://www.oschina.net/news/90514/puppeteer-0-13](https://www.oschina.net/news/90514/puppeteer-0-13)
<p>Puppeteer 是一个控制 headless Chrome 的 Node.js API 。它是一个 Node.js 库，通过&nbsp;</p></li></ul>
---------------
<h1 id="#title_10" >11、Deruv v0.9.5 发布，内容管理系统</h1>

[https://www.oschina.net/news/90509/deruv-0-9-5](https://www.oschina.net/news/90509/deruv-0-9-5)
<p>Deruv 是一个专业、快速的内容管理系统。<br/></p><p>版本0.9.5 主要增加功能：</p><p>1. 标签功能，可以为文章添加5个标签。</p><p>2. console增加简单算法自动获取标签功能。</p><p>3. blog模板增加二级回复功能。</p><p><img data-cke-saved-src="https://static.oschina.net/uploads/space/2017/1112/121632_LLql_3457566.png" src="https://static.oschina.net/uploads/space/2017/1112/121632_LLql_3457566.png" alt=""/></p><p>4. 完善部分小细节。</p>
---------------
<h1 id="#title_11" >12、每日一博 | 使用 Spring Cloud Sleuth 实现链路监控</h1>

[https://my.oschina.net/u/3677020/blog/1570902](https://my.oschina.net/u/3677020/blog/1570902)
<p>介绍Spring Cloud Sleuth和Zipkin的文章在网上其实并不少，所以我打算就我目前的系统来探讨一下，如何实现链路监控。</p>
---------------
<h1 id="#title_12" >13、协作翻译 | 了解 AI 与机器学习之深度学习基础指南</h1>

[https://www.oschina.net/translate/how-deep-learning-works](https://www.oschina.net/translate/how-deep-learning-works)
<p>读完这篇文章，你将会了解到人工智能和机器学习的基础知识。更重要的是你将会了解到最流行的一种机器学习技术——深度学习是如何工作的。阿</p>
---------------
<h1 id="#title_13" >14、码云推荐 | 安全支付输入框 LYPaymentField</h1>

[https://gitee.com/cityleaf/LYPaymentField](https://gitee.com/cityleaf/LYPaymentField)
<p>LYPaymentSecurityField 为安全支付输入框，继承于系统的 UIControl。它的实现原理比较简单，主要就是利用系统的UIKeyInput。</p>
---------------
<h1 id="#title_14" >15、Deepin Clone —— 深度备份还原工具</h1>

[https://www.oschina.net/p/deepin-clone](https://www.oschina.net/p/deepin-clone)
<p>深度备份还原工具是深度科技开发的一款备份还原工具，包括磁盘克隆、磁盘备份、磁盘还原、分区克隆等功能。</p>
---------------
<h1 id="#title_15" >16、OSChina 周日乱弹 —— 拆散她们，帮她们过节！</h1>

[https://my.oschina.net/xxiaobian/blog/1572325](https://my.oschina.net/xxiaobian/blog/1572325)
<p>有个警察最近被拉进一个原来的同学群里，他从来不说话，就是看别人说！……</p>
---------------
<h1 id="#title_16" >17、Go 语言开源发布 8 周年，成 2017 年增长最快语言</h1>

[https://www.oschina.net/news/90502/go-8-years-old](https://www.oschina.net/news/90502/go-8-years-old)
<p>Go 语言作为开源项目</p>
---------------
<h1 id="#title_17" >18、Hutool 3.2.0 发布，Java 工具集</h1>

[https://www.oschina.net/news/90511/hutool-3-2-0](https://www.oschina.net/news/90511/hutool-3-2-0)
<p>Hutool 是一个Java工具包，提供了丰富的文件、日期、日志、正则、字符串、配置文件等工具方法，并封装了一套简单易用的ORM框架。</p><p>主页：&nbsp;（感谢开源中国提供非常好用的Team文档平台）</p><p>此次更新为一次大版本跨越，主要的新特性为增加ExcelWriter用于Excel写出。其它更新如下：</p><p><strong>3.2.0&nbsp;更新内容：</strong><br/>新特性</p><ul class=" list-paddingleft-2"><li><p>MailUtil邮件工具类支持附件</p></li><li><p>Convert增加int、long、short与bytes之间的转换</p></li><li><p>BeetlUtil增加更多简化方法</p></li><li><p>extra模块中模板相关工具类移入template包中</p></li><li><p>ScriptUtil增加eval方法，执行脚本快捷方法</p></li><li><p>增加Excel03SaxReader用于03格式的Excel通过Sax方式读取</p></li><li><p>HttpUtil增加超时重载，post方法支持Rest模式</p></li><li><p>core包中去除servlet-api可选依赖，extra模块中增加ServletUtil（core包中的部分方法移入此工具类）</p></li><li><p>MailUtil支持SSL方式连接</p></li><li><p>增加MapProxy，用于代理Map对象，提供各种getXXX方法（感谢@【珠海】hzhhui）</p></li><li><p>Convert增加toXXXArray方法</p></li><li><p>增加剪贴板工具类ClipboardUtil（感谢@【北京】宁静）</p></li><li><p>ObjectUtil增加toString方法（感谢@【南京】toling）</p></li><li><p>XmlUtil增加readObjectFromXml重载（感谢@【北京】酱油君）</p></li><li><p>FileUtil和IoUtil去除final修饰（issue#49@Github）</p></li><li><p>为了更好的兼容性，Getter和Setter方法获取忽略大小写</p></li><li><p>StrUtil增加split和splitTrim重载方法（感谢@【南京】toling @【北京】宁静）</p></li><li><p>增加FileUtil.writeLines重载方法和writeUtf8Lines方法（感谢@【北京】宁静）</p></li></ul><p>Bug修复</p><ul class=" list-paddingleft-2"><li><p>修复FileUtil.normalize导致的路径修复问题</p></li><li><p>db模块中字段使用别名时去掉包装符</p></li><li><p>CollUtil.filter方法对于不可变集合参数报错问题改进（issue#IFW3Y@Gitee）</p></li><li><p>修复Convert.convert方法目标为数组对象时导致的问题</p></li><li><p>修复poi模块中ExcelReader读取带小数的标准单元格时小数部分丢失问题修复</p></li><li><p>修复SecureUtil.rsa和SecureUtil.dsa方法中publicKey传入问题（感谢@【上海】毛毛虎）</p></li><li><p>修复Cache模块传入Integer.MAX_VALUE错误问题（感谢@【南京】雲栖鬆）</p></li><li><p>修复BeanDesc无法识别isXXX方法的问题</p></li></ul>
---------------