## 文章索引
1、 <a href="#1开源中国-android-客户端-v290-发布" >开源中国 Android 客户端 v2.9.0 发布</a><br/>
2、 <a href="#2javamelody-1700-发布java-应用监控平台" >JavaMelody 1.70.0 发布，Java 应用监控平台</a><br/>
3、 <a href="#3flying-092-发布mybatis-插件组" >flying 0.9.2 发布，mybatis 插件组</a><br/>
4、 <a href="#4excel4j-v210版本更新java-快速操作-excel-工具" >Excel4J v2.1.0版本更新，Java 快速操作 Excel 工具</a><br/>
5、 <a href="#5每日一博-|-消息中间件集群部署测试与应用" >每日一博 | 消息中间件集群部署、测试与应用</a><br/>
6、 <a href="#6码云推荐-|-基于深度学习的分词系统和语料项目" >码云推荐 | 基于深度学习的分词系统和语料项目</a><br/>
7、 <a href="#7suse-linux-enterprise-15-beta-1-发布" >SUSE Linux Enterprise 15 Beta 1 发布</a><br/>
8、 <a href="#8openrasp-百度开源的自适应安全解决方案" >OpenRASP —— 百度开源的自适应安全解决方案</a><br/>
9、 <a href="#9协作翻译-|-用-go-语言编写一门工具的终极指南" >协作翻译 | 用 Go 语言编写一门工具的终极指南</a><br/>
10、 <a href="#10oschina-周六乱弹-泡在油冷主机的深海少女" >OSChina 周六乱弹 ——泡在油冷主机的深海少女</a><br/>
11、 <a href="#11linux-基金会提出-cdla-协议助推开放数据共享" >Linux 基金会提出 CDLA 协议，助推开放数据共享</a><br/>
12、 <a href="#12mcafee-宣布不再允许政府检查其软件源码" >McAfee 宣布不再允许政府检查其软件源码</a><br/><h1 id="#title_0" >1、开源中国 Android 客户端 v2.9.0 发布</h1>

[https://www.oschina.net/news/90044/oschina-android-app-v290-release](https://www.oschina.net/news/90044/oschina-android-app-v290-release)
<p>
	重阳节里，出游赏秋、登高远眺、观赏菊花、遍插茱萸、吃重阳糕、饮菊花酒。但是，千万表忘记来我大 OSC 逛逛哦。因为在今天这个特殊的日子里，我们非常高兴地宣布：开源中国最新版客户端发布啦！</p><p><strong><em><span style="text-decoration:underline;">「广而告之：开源中国源创会西安站已经开始报名了，详情</span></em></strong><strong><em><span style="text-decoration:underline;">。这次古都西安的源创会，有 Apache Kylin 内容、React &amp; Redux 重构 Web 应用、微服务等众多 Topic，精彩满满等你来哦」</span></em></strong></p><p>
	这个版本是一个 bugfix 的版本，主要修改上个版本中的一些小问题及用户体验方面的提升。主要有：</p><p></p><ol class=" list-paddingleft-2"><li><p>
			新增动弹长图保存、分享		</p></li><li><p>
			优化大图初始化默认大小显示		</p></li><li><p>
			优化动弹输入@、#等文本体验		</p></li><li><p>
			长按发布动弹		</p></li></ol><p><span style="color:#333333;font-family:&quot;font-size:16px;background-color:#FFFFFF;">~~~~~~~~~~~~~~~~~~~~~~~~~~~~~</span></p><p>
		还犹豫什么呢？赶快扫描如下二维码下载吧（记得要开 WIFI ）！或者<br/></p><p></p>
---------------
<h1 id="#title_1" >2、JavaMelody 1.70.0 发布，Java 应用监控平台</h1>

[https://www.oschina.net/news/90049/javamelody-1-70-0](https://www.oschina.net/news/90049/javamelody-1-70-0)
<p>JavaMelody 1.70.0 发布了，JavaMelody 的目标是在 QA 和生产环境中监视 Java 或 Java EE 应用程序。<br/></p><p>更新内容：</p><ul class=" list-paddingleft-2"><li><p>added: integration with <strong>Prometheus</strong>: Metrics are already displayed in the monitoring reports. You can also scrape the same metrics from </p></li></ul>
---------------
<h1 id="#title_2" >3、flying 0.9.2 发布，mybatis 插件组</h1>

[https://www.oschina.net/news/90046/flying-0-9-2](https://www.oschina.net/news/90046/flying-0-9-2)
<p>flying 是一个可以极大增加 mybatis 开发速度的插件组，它提供了一种全新的操作数据的方式，希望能对您有所帮助。</p><p>众所周知，mybatis 虽然易于上手，但放到互联网环境下使用时，不可避免的要面对诸如‘’一级缓存存在脏数据‘’、‘’需要写大量明文 SQL 语句‘’等问题。对于这些问题 mybatis 的开发团队选择了一种谦逊的方式，他们开放 mybatis 接口，允许用户开发插件，按自己的方式来解决这些问题。于是，一切 ORM 领域相关的问题在 mybatis 上通过插件都有了解决方案。</p><p><strong>flying 主要特点：</strong></p><p><strong>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;</strong>以前我们在 mapper.xml 中要写很复杂的 sql 语句，但现在在 mapper.xml 中只需这样：</p><pre>&nbsp;&nbsp;&nbsp;&nbsp;&lt;select&nbsp;id=&quot;select&quot;&nbsp;resultMap=&quot;result&quot;&gt;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;flying#{?}:select
&nbsp;&nbsp;&nbsp;&nbsp;&lt;/select&gt;

&nbsp;&nbsp;&nbsp;&nbsp;&lt;select&nbsp;id=&quot;selectOne&quot;&nbsp;resultMap=&quot;result&quot;&gt;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;flying:selectOne
&nbsp;&nbsp;&nbsp;&nbsp;&lt;/select&gt;

&nbsp;&nbsp;&nbsp;&nbsp;&lt;insert&nbsp;id=&quot;insert&quot;&gt;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;flying:insert
&nbsp;&nbsp;&nbsp;&nbsp;&lt;/insert&gt;

&nbsp;&nbsp;&nbsp;&nbsp;&lt;update&nbsp;id=&quot;update&quot;&gt;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;flying:insert
&nbsp;&nbsp;&nbsp;&nbsp;&lt;/update&gt;

&nbsp;&nbsp;&nbsp;&nbsp;&lt;delete&nbsp;id=&quot;delete&quot;&gt;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;flying:delete
&nbsp;&nbsp;&nbsp;&nbsp;&lt;/delete&gt;</pre><p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;在您的实体类上加上这样一些标注：<br/></p><pre>package&nbsp;myPackage;
import&nbsp;javax.persistence.Column;
import&nbsp;javax.persistence.Id;
import&nbsp;javax.persistence.Table;
&nbsp;&nbsp;&nbsp;&nbsp;
@Table(name&nbsp;=&nbsp;&quot;account&quot;)
public&nbsp;class&nbsp;Account&nbsp;{
&nbsp;&nbsp;&nbsp;&nbsp;@Id
&nbsp;&nbsp;&nbsp;&nbsp;@Column
&nbsp;&nbsp;&nbsp;&nbsp;private&nbsp;Integer&nbsp;id;
	&nbsp;&nbsp;&nbsp;&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;@Column
&nbsp;&nbsp;&nbsp;&nbsp;private&nbsp;java.lang.String&nbsp;name;

&nbsp;&nbsp;&nbsp;&nbsp;@Column
&nbsp;&nbsp;&nbsp;&nbsp;private&nbsp;Integer&nbsp;age;
	&nbsp;&nbsp;&nbsp;&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;/*&nbsp;省略&nbsp;getter&nbsp;和&nbsp;setter&nbsp;*/
}</pre><p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp; flying 就完全明白您的数据结构和您想做的事情了。&nbsp;接下来您增删改查这个实体就会变得非常简单：</p><pre>&nbsp;&nbsp;&nbsp;&nbsp;/*&nbsp;新增&nbsp;*/
&nbsp;&nbsp;&nbsp;&nbsp;Account&nbsp;newAccount&nbsp;=&nbsp;new&nbsp;Account();
&nbsp;&nbsp;&nbsp;&nbsp;newAccount.setName(&quot;ann&quot;);
&nbsp;&nbsp;&nbsp;&nbsp;newAccount.setAge(18);
&nbsp;&nbsp;&nbsp;&nbsp;accountService.insert(newAccount);

&nbsp;&nbsp;&nbsp;&nbsp;/*&nbsp;按主键查询&nbsp;*/
&nbsp;&nbsp;&nbsp;&nbsp;Account&nbsp;account&nbsp;=&nbsp;accountService.select(newAccount.getId());
&nbsp;&nbsp;&nbsp;&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;/*&nbsp;按姓名查询，这里忽略了年龄&nbsp;*/
&nbsp;&nbsp;&nbsp;&nbsp;Account&nbsp;accountC1&nbsp;=&nbsp;new&nbsp;Account();
&nbsp;&nbsp;&nbsp;&nbsp;accountC1.setName(&quot;ann&quot;);
&nbsp;&nbsp;&nbsp;&nbsp;Account&nbsp;account1&nbsp;=&nbsp;accountService.selectOne(accountC1);
&nbsp;&nbsp;&nbsp;&nbsp;/*&nbsp;account1&nbsp;和&nbsp;account&nbsp;代表相同的业务数据&nbsp;*/
&nbsp;&nbsp;&nbsp;&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;/*&nbsp;按年龄查询，这里忽略了姓名&nbsp;*/
&nbsp;&nbsp;&nbsp;&nbsp;Account&nbsp;accountC2&nbsp;=&nbsp;new&nbsp;Account();
&nbsp;&nbsp;&nbsp;&nbsp;accountC2.setAge(18);
&nbsp;&nbsp;&nbsp;&nbsp;Account&nbsp;account2&nbsp;=&nbsp;accountService.selectOne(accountC2);
&nbsp;&nbsp;&nbsp;&nbsp;/*&nbsp;account2&nbsp;和&nbsp;account&nbsp;代表相同的业务数据&nbsp;*/
&nbsp;&nbsp;&nbsp;&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;/*&nbsp;按姓名和年龄查询&nbsp;*/
&nbsp;&nbsp;&nbsp;&nbsp;Account&nbsp;accountC3&nbsp;=&nbsp;new&nbsp;Account();
&nbsp;&nbsp;&nbsp;&nbsp;accountC3.setName(&quot;ann&quot;);
&nbsp;&nbsp;&nbsp;&nbsp;accountC3.setAge(18);
&nbsp;&nbsp;&nbsp;&nbsp;Account&nbsp;account3&nbsp;=&nbsp;accountService.selectOne(accountC3);
&nbsp;&nbsp;&nbsp;&nbsp;/*&nbsp;account3&nbsp;和&nbsp;account&nbsp;代表相同的业务数据&nbsp;*/
&nbsp;&nbsp;&nbsp;&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;/*&nbsp;修改&nbsp;*/
&nbsp;&nbsp;&nbsp;&nbsp;account.setName(&quot;bob&quot;);
&nbsp;&nbsp;&nbsp;&nbsp;accountService.update(newAccount);
&nbsp;&nbsp;&nbsp;&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;/*&nbsp;按主键删除&nbsp;*/
&nbsp;&nbsp;&nbsp;&nbsp;accountService.delete(newAccount);</pre><p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp; 由于 flying 掌握了您全部的数据结构和实体关系，所以操作数据变得非常简单，您再也不需要定义 “getAccountByIDName、getAccountByName” 这样的方法了，由此带来更大的好处是您的 service 层只需要关注事务方面的逻辑即可，它从低级代码中完全解放了出来。以上只是 flying 功能的冰山一角，其它的功能如多表联查、分页、乐观锁、跨数据源查询、二级缓存等 flying 都有简单的解决方案，您可以在&nbsp;&nbsp;中进行查看。</p><p>0.9.2 新增内容：</p><ul class=" list-paddingleft-2"><li><p>兼容 JPA 中的 @Column、@Id、@Table 标签，这些标签可以和 @FieldMapperAnnotation、@TableMapperAnnotation 协同使用，优先级从高到低为：@Id、@FieldMapperAnnotation 和 @TableMapperAnnotation、@Column 和 @Table。</p></li><li><p>现在 ignoreTag 对 insert、update、updatePersistent 也会起作用。如果 @Column 中设置 insertable = false 和 updateable = false，会在新增和修改时起到永久性忽略的作用。</p></li></ul>
---------------
<h1 id="#title_3" >4、Excel4J v2.1.0版本更新，Java 快速操作 Excel 工具</h1>

[https://www.oschina.net/news/90045/excel4j-2-1-0](https://www.oschina.net/news/90045/excel4j-2-1-0)
<p><strong>java基于poi实现快速操作Excel的工具[v2.1.0]版本更新:</strong></p><p><strong>v2.x新特性</strong></p><ol class=" list-paddingleft-2"><li><p>Excel读取支持部分类型转换了(如转为Integer,Long,Date(部分)等) v2.0.0之前只能全部内容转为String</p></li><li><p>Excel支持非注解读取Excel内容了,内容存于`List&lt;List&lt;String&gt;&gt;`对象内</p></li><li><p>现在支持`List&lt;List&lt;String&gt;&gt;`导出Excel了(可以不基于模板)</p></li><li><p>Excel新增了Map数据样式映射功能(模板可为每个key设置一个样式,定义为:&amp;key, 导出Map数据的样式将与key值映射)</p></li><li><p>新增读取Excel数据转换器接口`com.github.converter.ReadConvertible`</p></li><li><p>新增写入Excel数据转换器接口`com.github.converter.WriteConvertible`</p></li><li><p>修复已知bug</p></li></ol>
---------------
<h1 id="#title_4" >5、每日一博 | 消息中间件集群部署、测试与应用</h1>

[https://my.oschina.net/u/3112259/blog/1556837](https://my.oschina.net/u/3112259/blog/1556837)
<p>业务系统中，通常会遇到这些场景：A系统向B系统主动推送一个处理请求；A系统向B系统发送一个业务处理请求，因为某些原因（断电、宕机。。），B业务系统挂机了，A系统发起的请求处理失败；前端应用并发量过大，部分请求丢失或后端业务系统卡死。。。。这个时候，消息中间件就派上用场了--提升系统稳定性、可用性、可扩展性。</p>
---------------
<h1 id="#title_5" >6、码云推荐 | 基于深度学习的分词系统和语料项目</h1>

[https://gitee.com/koth/kcws](https://gitee.com/koth/kcws)
<p>kcws 是一个基于深度学习的分词系统和语料项目。本项目模型 BiLSTM+CRF&nbsp;。</p>
---------------
<h1 id="#title_6" >7、SUSE Linux Enterprise 15 Beta 1 发布</h1>

[https://www.oschina.net/news/90050/suse-linux-enterprise-15-beta1](https://www.oschina.net/news/90050/suse-linux-enterprise-15-beta1)
<p>SUSE Linux Enterprise 15 Beta 1 发布了。SUSE Linux Enterprise Server 是为支持物理、虚拟和基于云的任务关键型工作负载而构建的世界一流的、安全的开放源代码服务器操作系统。操作系统在帮助组织加速创新、增强系统可靠性、满足严格的安全要求和适应新技术方面更上一层楼。最新版本的&nbsp;Service Pack 3&nbsp;通过支持 ARM 单芯片系统、Intel、AMD、SAP HANA、z Systems 和 NVM Express over Fabrics 使用最新的硬件环境，优化基础设施。</p><p>更新内容：</p><p>&nbsp;SLE 15 开发了“传统基础设施”和“软件定义基础设施”，SLE 15 的五个主要目标是：</p><ul class=" list-paddingleft-2"><li><p>处理传统和集装箱化基础设施，为传统和敏捷数据中心提供通用代码库。</p></li><li><p>从单一介质开始安装所有SUSE Linux Enterprise 15产品。</p></li><li><p>轻松使用模块和扩展，并轻松搜索，安装和使用SUSE Universe中的软件包。</p></li><li><p>多种体系结构和部署方案可用于：X86_64，Power LE，System z，ARM64。</p></li><li><p>按照</p><p>规范和安全开发，使用安全开发模式构建。</p></li></ul><p>下载地址：).</p>
---------------
<h1 id="#title_7" >8、OpenRASP —— 百度开源的自适应安全解决方案</h1>

[https://www.oschina.net/p/openrasp](https://www.oschina.net/p/openrasp)
<p>最近几年，Web攻击手段开始变得复杂，攻击面也越来越广。传统的安全防护手段，WAF、IDS 等等，大多是基于规则，已经不能满足企业对安全的基本需求。Gartner 在2014年提出了 &quot;应用自我保护&quot; 技术的概念，即 &quot;对应用服务的保护，不应该依赖于外部系统；应用应该具备自我保护的能力&quot;。为此，百度推出了开源的自适应安全产品 -- OpenRASP，希望通过开源免费的形式，让更多的人参与进来，并让互联网变得更加安全。</p>
---------------
<h1 id="#title_8" >9、协作翻译 | 用 Go 语言编写一门工具的终极指南</h1>

[https://www.oschina.net/translate/the-ultimate-guide-to-writing-a-go-tool](https://www.oschina.net/translate/the-ultimate-guide-to-writing-a-go-tool)
<p>这是一篇非常长的博客文章，解释了如何编写类似这样的工具以及如何构建它的每一个细节。 它包含许多特有的细节、提示和技巧和某些未知的 Go 位。</p>
---------------
<h1 id="#title_9" >10、OSChina 周六乱弹 ——泡在油冷主机的深海少女</h1>

[https://my.oschina.net/xxiaobian/blog/1557514](https://my.oschina.net/xxiaobian/blog/1557514)
<p>周六到了，你们准备好去金拱门吃全家桶了吗？以后麦当劳的贺年广告，应该不会再是那种开瓶可乐点个汉堡当年夜饭的了，现在将会更接地气：“金拱门携全体员工给您拜年了！”麦当劳的主要吉祥物，麦当劳叔叔也可能要改名为“金叔叔”了。</p>
---------------
<h1 id="#title_10" >11、Linux 基金会提出 CDLA 协议，助推开放数据共享</h1>

[https://www.oschina.net/news/90038/linux-foundation-presents-clda](https://www.oschina.net/news/90038/linux-foundation-presents-clda)
<p>神经网络、机器学习、无人驾驶……这些尖端技术都需要大量的数据支撑。但团队和开发者要怎么公开分享数据？ Linux 基金会给的答案是： （社区数据许可协议，简称 CDLA ）。</p><p><img height="740" data-cke-saved-src="https://static.oschina.net/uploads/space/2017/1027/160604_ZpDS_2896879.png" src="https://static.oschina.net/uploads/space/2017/1027/160604_ZpDS_2896879.png" width="2230"/></p><p>过去，开源社区展现了其强大的开放式合作力量，一些重要的软件资产往往是由世界各地的程序员相互协作构建的。随着大数据时代的发展，已经到了将这些训练集更加公开的时候了。但同时存在的问题是：知识产权法在对待数据上有别于开源协议，常用的 OSI 认可的开源许可证在应用于数据时效果不佳。</p><p>因此，Linux 基金会提出了&nbsp;CDLA，以支持围绕策划和共享“开放”数据构建的协作社区。旨在允许所有类型的个人和组织在共享开源软件的同时轻松共享数据。CDLA 分为两类：</p><ul class=" list-paddingleft-2"><li><p>Sharing 许可证：鼓励将数据贡献回社区</p></li><li><p>Permissive 许可证：对开放数据的贡献者和使用者不作要求</p></li></ul><p><img height="462" data-cke-saved-src="https://static.oschina.net/uploads/space/2017/1027/161139_9GQr_2896879.png" src="https://static.oschina.net/uploads/space/2017/1027/161139_9GQr_2896879.png" width="1838"/></p><p>Linux 基金会此举有望将开源社区带入全新的发展阶段，当然随着而来的实施难度也不可忽视，具体能带来什么影响，拭目以待！</p>
---------------
<h1 id="#title_11" >12、McAfee 宣布不再允许政府检查其软件源码</h1>

[https://www.oschina.net/news/90037/mcafee-refuse-source-code-reviews](https://www.oschina.net/news/90037/mcafee-refuse-source-code-reviews)
<p>为获取政府单位的信任，IT 科技公司会配合要求开放产品源码供检查以获得产品在海外出售的许可证。但据</p>
---------------