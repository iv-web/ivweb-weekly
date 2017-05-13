## 文章索引
1、 <a href="#1使用-nodejs-对文本内容分词和关键词抽取" >使用 Node.js 对文本内容分词和关键词抽取</a><br/>
2、 <a href="#2web-development-reading-list-#182:-ipfs-wikipedia-new-webpack-cli-and-css-grid-breakout" >Web Development Reading List #182: IPFS Wikipedia, New Webpack CLI, And CSS Grid Breakout</a><br/>
3、 <a href="#3javascript编译器prepack旨在减少启动时间" >JavaScript编译器Prepack：旨在减少启动时间</a><br/>
4、 <a href="#4azul-systems推出falcon一个基于llvm的新的java即时编译器" >Azul Systems推出Falcon，一个基于LLVM的新的Java即时编译器</a><br/>
5、 <a href="#5大规模精益创业流程中的原则" >大规模精益创业：流程中的原则</a><br/>
6、 <a href="#62017科技行业离职人员研究报告发布" >2017科技行业离职人员研究报告发布</a><br/>
7、 <a href="#7#334:-a-look-at-chrome-canarys-new-es6-module-support" >#334: A Look at Chrome Canary's New ES6 Module Support</a><br/>
8、 <a href="#8gcc-71发布完全支持c++17" >GCC 7.1发布，完全支持C++17</a><br/>
9、 <a href="#9google发力智能识别cloud-speech-api正式发布" >Google发力智能识别：Cloud Speech API正式发布</a><br/>
10、 <a href="#10mongodb-atlas扩展了aws服务" >MongoDB Atlas扩展了AWS服务</a><br/>
11、 <a href="#11reinhold就jigsaw投票一事向jcp提交公开信" >Reinhold就Jigsaw投票一事向JCP提交公开信</a><br/>
12、 <a href="#12net-framework-47正式发布" >.NET Framework 4.7正式发布</a><br/><h1 id="#title_0" >1、使用 Node.js 对文本内容分词和关键词抽取</h1>

[https://www.h5jun.com/post/segment-with-nodejs.html](https://www.h5jun.com/post/segment-with-nodejs.html)
<div class="toc"></div><p>在讨论技术前先卖个萌，吃货的世界你不懂~~</p>
<p><img src="https://p1.ssl.qhimg.com/t01ee4cb9bf6b602f75.png" alt=""></p>
<!--more-->
<p>的文章有 tag，用户可以基于 tag 来快速筛选感兴趣的文章，文章也可以依照 tag 关联来进行相关推荐。但是现在众成翻译的 tag 是在推荐文章的时候设置的，都是英文的，而且人工设置难免不规范和不完全。虽然发布文章后也可以人工编辑，但是我们也不能指望用户或管理员能够时时刻刻编辑出恰当的 tag，所以我们需要用工具来自动生成 tag。</p>
<p>在现在开源的分词工具里面，。</p>
<p>nodejieba 的安装和使用十分简单：</p>
<pre><code class="hljs lang-undefined">npm install nodejieba
</code></pre>
<pre><code class="hljs lang-js"><span class="hljs-keyword">var</span> nodejieba = <span class="hljs-built_in">require</span>(<span class="hljs-string">"nodejieba"</span>);
<span class="hljs-keyword">var</span> result = nodejieba.cut(<span class="hljs-string">"帝国主义要把我们的地瓜分掉"</span>);
<span class="hljs-built_in">console</span>.log(result);
<span class="hljs-comment">//[ '帝国主义', '要', '把', '我们', '的', '地', '瓜分', '掉' ]</span>

result = nodejieba.cut(<span class="hljs-string">'土地，俺老孙的金箍棒在哪里？'</span>);
<span class="hljs-built_in">console</span>.log(result);
<span class="hljs-comment">//[ '土地', '，', '俺', '老', '孙', '的', '金箍棒', '在', '哪里', '？' ]</span>

result = nodejieba.cut(<span class="hljs-string">'大圣，您的金箍棒就棒在特别配您的头型！'</span>);
<span class="hljs-built_in">console</span>.log(result); 
<span class="hljs-comment">//[ '大圣','，','您','的','金箍棒','就','棒','在','特别','配','您','的','头型','！' ]</span>
</code></pre>
<p>我们可以载入自己的字典，在字典里给每个词分别设置权重和词性：</p>
<p>编辑 <code>user.uft8</code></p>
<pre><code class="hljs lang-stata">地瓜 9999 <span class="hljs-keyword">n</span>
金箍 9999 <span class="hljs-keyword">n</span>
棒就棒在 9999
</code></pre><p>然后通过 <code>nodejieba.load</code> 加载字典。</p>
<pre><code class="hljs lang-js"><span class="hljs-keyword">var</span> nodejieba = <span class="hljs-built_in">require</span>(<span class="hljs-string">"nodejieba"</span>);

nodejieba.load({
  userDict: <span class="hljs-string">'./user.utf8'</span>,
});

<span class="hljs-keyword">var</span> result = nodejieba.cut(<span class="hljs-string">"帝国主义要把我们的地瓜分掉"</span>);
<span class="hljs-built_in">console</span>.log(result);
<span class="hljs-comment">//[ '帝国主义', '要', '把', '我们', '的', '地瓜', '分', '掉' ]</span>

result = nodejieba.cut(<span class="hljs-string">'土地，俺老孙的金箍棒在哪里？'</span>);
<span class="hljs-built_in">console</span>.log(result);
<span class="hljs-comment">//[ '土地', '，', '俺', '老', '孙', '的', '金箍棒', '在', '哪里', '？' ]</span>

result = nodejieba.cut(<span class="hljs-string">'大圣，您的金箍棒就棒在特别配您的头型！'</span>);
<span class="hljs-built_in">console</span>.log(result); 
<span class="hljs-comment">//[ '大圣', '，', '您', '的', '金箍', '棒就棒在', '特别', '配', '您', '的', '头型', '！' ]</span>
</code></pre>
<p>除了分词以外，我们可以利用 nodejieba 提取关键词：</p>
<pre><code class="hljs lang-js"><span class="hljs-keyword">const</span> content = <span class="hljs-string">`
HTTP、HTTP/2与性能优化

本文的目的是通过比较告诉大家，为什么应该从HTTP迁移到HTTPS，以及为什么应该添加到HTTP/2的支持。在比较HTTP和HTTP/2之前，先看看什么是HTTP。

什么是HTTP
HTTP是在万维网上通信的一组规则。HTTP属于应用层协议，跑在TCP/IP层之上。用户通过浏览器请求网页时，HTTP负责处理请求并在Web服务器与客户端之间建立连接。

有了HTTP/2，不使用雪碧图、压缩、拼接，也可以提升性能。然而，这不代表不应该使用这些技术。不过这已经清楚表明了我们从HTTP/1.1移动到HTTP/2的必要性。
`</span>;

<span class="hljs-keyword">const</span> nodejieba = <span class="hljs-built_in">require</span>(<span class="hljs-string">"nodejieba"</span>);

<span class="hljs-keyword">const</span> result = nodejieba.extract(content, <span class="hljs-number">20</span>);

<span class="hljs-built_in">console</span>.log(result);
</code></pre>
<p>输出的结果类似下面这样：</p>
<pre><code class="hljs lang-groovy">[ { <span class="hljs-string">word:</span> <span class="hljs-string">'HTTP'</span>, <span class="hljs-string">weight:</span> <span class="hljs-number">140.8704516850025</span> },
  { <span class="hljs-string">word:</span> <span class="hljs-string">'请求'</span>, <span class="hljs-string">weight:</span> <span class="hljs-number">14.23018001394</span> },
  { <span class="hljs-string">word:</span> <span class="hljs-string">'应该'</span>, <span class="hljs-string">weight:</span> <span class="hljs-number">14.052171126120001</span> },
  { <span class="hljs-string">word:</span> <span class="hljs-string">'万维网'</span>, <span class="hljs-string">weight:</span> <span class="hljs-number">12.2912397395</span> },
  { <span class="hljs-string">word:</span> <span class="hljs-string">'TCP'</span>, <span class="hljs-string">weight:</span> <span class="hljs-number">11.739204307083542</span> },
  { <span class="hljs-string">word:</span> <span class="hljs-string">'1.1'</span>, <span class="hljs-string">weight:</span> <span class="hljs-number">11.739204307083542</span> },
  { <span class="hljs-string">word:</span> <span class="hljs-string">'Web'</span>, <span class="hljs-string">weight:</span> <span class="hljs-number">11.739204307083542</span> },
  { <span class="hljs-string">word:</span> <span class="hljs-string">'雪碧图'</span>, <span class="hljs-string">weight:</span> <span class="hljs-number">11.739204307083542</span> },
  { <span class="hljs-string">word:</span> <span class="hljs-string">'HTTPS'</span>, <span class="hljs-string">weight:</span> <span class="hljs-number">11.739204307083542</span> },
  { <span class="hljs-string">word:</span> <span class="hljs-string">'IP'</span>, <span class="hljs-string">weight:</span> <span class="hljs-number">11.739204307083542</span> },
  { <span class="hljs-string">word:</span> <span class="hljs-string">'应用层'</span>, <span class="hljs-string">weight:</span> <span class="hljs-number">11.2616203224</span> },
  { <span class="hljs-string">word:</span> <span class="hljs-string">'客户端'</span>, <span class="hljs-string">weight:</span> <span class="hljs-number">11.1926274509</span> },
  { <span class="hljs-string">word:</span> <span class="hljs-string">'浏览器'</span>, <span class="hljs-string">weight:</span> <span class="hljs-number">10.8561552143</span> },
  { <span class="hljs-string">word:</span> <span class="hljs-string">'拼接'</span>, <span class="hljs-string">weight:</span> <span class="hljs-number">9.85762638414</span> },
  { <span class="hljs-string">word:</span> <span class="hljs-string">'比较'</span>, <span class="hljs-string">weight:</span> <span class="hljs-number">9.5435285574</span> },
  { <span class="hljs-string">word:</span> <span class="hljs-string">'网页'</span>, <span class="hljs-string">weight:</span> <span class="hljs-number">9.53122979951</span> },
  { <span class="hljs-string">word:</span> <span class="hljs-string">'服务器'</span>, <span class="hljs-string">weight:</span> <span class="hljs-number">9.41204128224</span> },
  { <span class="hljs-string">word:</span> <span class="hljs-string">'使用'</span>, <span class="hljs-string">weight:</span> <span class="hljs-number">9.03259988558</span> },
  { <span class="hljs-string">word:</span> <span class="hljs-string">'必要性'</span>, <span class="hljs-string">weight:</span> <span class="hljs-number">8.81927328699</span> },
  { <span class="hljs-string">word:</span> <span class="hljs-string">'添加'</span>, <span class="hljs-string">weight:</span> <span class="hljs-number">8.0484751722</span> } ]
</code></pre><p>我们添加一些新的关键词到字典里：</p>
<pre><code class="hljs lang-undefined">性能
HTTP/2
</code></pre><p>输出结果如下：</p>
<pre><code class="hljs lang-groovy">[ { <span class="hljs-string">word:</span> <span class="hljs-string">'HTTP'</span>, <span class="hljs-string">weight:</span> <span class="hljs-number">105.65283876375187</span> },
  { <span class="hljs-string">word:</span> <span class="hljs-string">'HTTP/2'</span>, <span class="hljs-string">weight:</span> <span class="hljs-number">58.69602153541771</span> },
  { <span class="hljs-string">word:</span> <span class="hljs-string">'请求'</span>, <span class="hljs-string">weight:</span> <span class="hljs-number">14.23018001394</span> },
  { <span class="hljs-string">word:</span> <span class="hljs-string">'应该'</span>, <span class="hljs-string">weight:</span> <span class="hljs-number">14.052171126120001</span> },
  { <span class="hljs-string">word:</span> <span class="hljs-string">'性能'</span>, <span class="hljs-string">weight:</span> <span class="hljs-number">12.61259281884</span> },
  { <span class="hljs-string">word:</span> <span class="hljs-string">'万维网'</span>, <span class="hljs-string">weight:</span> <span class="hljs-number">12.2912397395</span> },
  { <span class="hljs-string">word:</span> <span class="hljs-string">'IP'</span>, <span class="hljs-string">weight:</span> <span class="hljs-number">11.739204307083542</span> },
  { <span class="hljs-string">word:</span> <span class="hljs-string">'HTTPS'</span>, <span class="hljs-string">weight:</span> <span class="hljs-number">11.739204307083542</span> },
  { <span class="hljs-string">word:</span> <span class="hljs-string">'1.1'</span>, <span class="hljs-string">weight:</span> <span class="hljs-number">11.739204307083542</span> },
  { <span class="hljs-string">word:</span> <span class="hljs-string">'TCP'</span>, <span class="hljs-string">weight:</span> <span class="hljs-number">11.739204307083542</span> },
  { <span class="hljs-string">word:</span> <span class="hljs-string">'Web'</span>, <span class="hljs-string">weight:</span> <span class="hljs-number">11.739204307083542</span> },
  { <span class="hljs-string">word:</span> <span class="hljs-string">'雪碧图'</span>, <span class="hljs-string">weight:</span> <span class="hljs-number">11.739204307083542</span> },
  { <span class="hljs-string">word:</span> <span class="hljs-string">'应用层'</span>, <span class="hljs-string">weight:</span> <span class="hljs-number">11.2616203224</span> },
  { <span class="hljs-string">word:</span> <span class="hljs-string">'客户端'</span>, <span class="hljs-string">weight:</span> <span class="hljs-number">11.1926274509</span> },
  { <span class="hljs-string">word:</span> <span class="hljs-string">'浏览器'</span>, <span class="hljs-string">weight:</span> <span class="hljs-number">10.8561552143</span> },
  { <span class="hljs-string">word:</span> <span class="hljs-string">'拼接'</span>, <span class="hljs-string">weight:</span> <span class="hljs-number">9.85762638414</span> },
  { <span class="hljs-string">word:</span> <span class="hljs-string">'比较'</span>, <span class="hljs-string">weight:</span> <span class="hljs-number">9.5435285574</span> },
  { <span class="hljs-string">word:</span> <span class="hljs-string">'网页'</span>, <span class="hljs-string">weight:</span> <span class="hljs-number">9.53122979951</span> },
  { <span class="hljs-string">word:</span> <span class="hljs-string">'服务器'</span>, <span class="hljs-string">weight:</span> <span class="hljs-number">9.41204128224</span> },
  { <span class="hljs-string">word:</span> <span class="hljs-string">'使用'</span>, <span class="hljs-string">weight:</span> <span class="hljs-number">9.03259988558</span> } ]
</code></pre><p>在这个基础上，我们采用白名单的方式过滤出一些可以作为 tag 的词：</p>
<pre><code class="hljs lang-js"><span class="hljs-keyword">const</span> content = <span class="hljs-string">`
HTTP、HTTP/2与性能优化

本文的目的是通过比较告诉大家，为什么应该从HTTP迁移到HTTPS，以及为什么应该添加到HTTP/2的支持。在比较HTTP和HTTP/2之前，先看看什么是HTTP。

什么是HTTP
HTTP是在万维网上通信的一组规则。HTTP属于应用层协议，跑在TCP/IP层之上。用户通过浏览器请求网页时，HTTP负责处理请求并在Web服务器与客户端之间建立连接。

有了HTTP/2，不使用雪碧图、压缩、拼接，也可以提升性能。然而，这不代表不应该使用这些技术。不过这已经清楚表明了我们从HTTP/1.1移动到HTTP/2的必要性。
`</span>;

<span class="hljs-keyword">const</span> nodejieba = <span class="hljs-built_in">require</span>(<span class="hljs-string">"nodejieba"</span>);

nodejieba.load({
  userDict: <span class="hljs-string">'./user.utf8'</span>,
});

<span class="hljs-keyword">const</span> result = nodejieba.extract(content, <span class="hljs-number">20</span>);

<span class="hljs-keyword">const</span> tagList = [<span class="hljs-string">'HTTPS'</span>, <span class="hljs-string">'HTTP'</span>, <span class="hljs-string">'HTTP/2'</span>, <span class="hljs-string">'Web'</span>, <span class="hljs-string">'浏览器'</span>, <span class="hljs-string">'性能'</span>];

<span class="hljs-built_in">console</span>.log(result.filter(item =&gt; tagList.indexOf(item.word) &gt;= <span class="hljs-number">0</span>));
</code></pre>
<p>最后得到：</p>
<pre><code class="hljs lang-groovy">[ { <span class="hljs-string">word:</span> <span class="hljs-string">'HTTP'</span>, <span class="hljs-string">weight:</span> <span class="hljs-number">105.65283876375187</span> },
  { <span class="hljs-string">word:</span> <span class="hljs-string">'HTTP/2'</span>, <span class="hljs-string">weight:</span> <span class="hljs-number">58.69602153541771</span> },
  { <span class="hljs-string">word:</span> <span class="hljs-string">'性能'</span>, <span class="hljs-string">weight:</span> <span class="hljs-number">12.61259281884</span> },
  { <span class="hljs-string">word:</span> <span class="hljs-string">'HTTPS'</span>, <span class="hljs-string">weight:</span> <span class="hljs-number">11.739204307083542</span> },
  { <span class="hljs-string">word:</span> <span class="hljs-string">'Web'</span>, <span class="hljs-string">weight:</span> <span class="hljs-number">11.739204307083542</span> },
  { <span class="hljs-string">word:</span> <span class="hljs-string">'浏览器'</span>, <span class="hljs-string">weight:</span> <span class="hljs-number">10.8561552143</span> } ]
</code></pre><p>这就是我们想要的结果。</p>
<p>以上就是分词库 nodejieba 基本的使用方法，在将来我们可以利用它对众成翻译发布的译文自动分析添加相应的 tag，以为各位译者和读者提供更好的用户体验。</p>
<p>有任何问题，欢迎在讨论区讨论~</p>
---------------
<h1 id="#title_1" >2、Web Development Reading List #182: IPFS Wikipedia, New Webpack CLI, And CSS Grid Breakout</h1>
Anselm Hannemann
[https://www.smashingmagazine.com/2017/05/web-development-reading-list-182/](https://www.smashingmagazine.com/2017/05/web-development-reading-list-182/)
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
</table><p>When did you take your last <strong>vacation</strong>? For many of us, it was probably a long time ago. However, since quite a while, I stumble across more and more stories about companies that take unusual steps vacation-wise. Companies giving their employees a day off each week in summer or going on vacation together as a team building event instead of traveling somewhere just to work.</p>
<figure></figure>
<p>But while there’s a <strong>new generation building their dream work environments</strong>, a lot of people still suffer from very bad working conditions. They work long hours and are discriminated or harassed by colleagues or their managers. And just this week, I heard that many company owners are desperate because “Generation Y” doesn’t want to work long hours anymore.</p><p>The post .</p>
---------------
<h1 id="#title_2" >3、JavaScript编译器Prepack：旨在减少启动时间</h1>
David Iffland
[http://www.infoq.com/cn/news/2017/05/prepack-javascript-compiler?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/05/prepack-javascript-compiler?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Facebook透露了Prepack项目，一个编译时的JavaScript解析器，旨在通过预计算全局代码块来减少代码初始化时间。React Native应用和其他具有启动时间瓶颈的平台可以从该工具中获得最大的好处。</p> <i>By David Iffland</i> <i> Translated by 薛命灯</i>
---------------
<h1 id="#title_3" >4、Azul Systems推出Falcon，一个基于LLVM的新的Java即时编译器</h1>
Charles Humble, Victor Grazi
[http://www.infoq.com/cn/news/2017/05/azul-falcon?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/05/azul-falcon?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>近日，Azul Systems发布了Zing 17.03。该版本完全支持Azul基于LLVM的新的Java即时（JIT）编译器Falcon。该编译器设计用来取代Zing先前版本以及Oracle HotSpot和OpenJDK使用的C2编译器。Falcon是1997年JavaOne大会推出C2以来Java SE的第一个新的生产用JIT编译器。</p> <i>By Charles Humble</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_4" >5、大规模精益创业：流程中的原则</h1>
Ben Linders
[http://www.infoq.com/cn/news/2017/05/scaling-lean-startup?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/05/scaling-lean-startup?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>大型组织想要像精益创业公司一样行事，但要成为敏捷组织，他们需要重新思考自身招聘、激励和管理员工的方式。当团队基于能够快速学习到的知识作出低风险的决策，并且用学习的成果提升交付项目的价值，组织就应该奖励他们。</p> <i>By Ben Linders</i> <i> Translated by 王强</i>
---------------
<h1 id="#title_5" >6、2017科技行业离职人员研究报告发布</h1>
Shane Hastie
[http://www.infoq.com/cn/news/2017/05/tech-leavers-report?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/05/tech-leavers-report?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>卡普尔社会影响力中心对科技行业人员离职的原因进行了考察，并公布了研究结果。该研究得出的4个主要结论是：不公平导致离职；不同群体在职场体验上差别很大；不公平每年导致数10亿美元的损失；如果做得好，多元化和包容精神可以改善文化，减少离职。</p> <i>By Shane Hastie</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_6" >7、#334: A Look at Chrome Canary's New ES6 Module Support</h1>

[http://javascriptweekly.com/issues/334](http://javascriptweekly.com/issues/334)
<table border="0" width="100%" cellpadding="0" cellspacing="0" bgcolor="#ffffff" style="font-family: 'helvetica neue', helvetica, arial, sans-serif; font-size: 14px; line-height: 20px; color: #333"><tr><td align="center" valign="top">
<table border="0" width="600" cellpadding="0" cellspacing="0" class="container noarchive" style="border-collapse: collapse;"><tr><td style="padding-top: 6px; padding-bottom: 6px; font-size: 11px; text-align: center; color: #555; font-family: verdana, arial, sans-serif">
<span class="nomo">This week's JavaScript news</span> — 
</td></tr></table>
<table border="0" width="600" cellpadding="0" cellspacing="0" class="container" style="border-collapse: collapse">
<tr><td style="background-color: #f7df1e"><table width="100%" cellspacing="0" cellpadding="0" align="left"><tr><td align="left" class="block" style="padding: 6px 12px;">
<table align="left" width="50%" class="gowide"><tr><td><span style="line-height: 36px; font-size: 23px; color: #f7df1e; font-weight: bold; color: #323330">JavaScript Weekly</span></td></tr></table>
<table align="left" style="text-align: right" width="50%" class="gowide lonmo"><tr><td><span style="font-size: 14px; line-height: 36px; font-weight: normal; color: #323330">
Issue 334 — May 12, 2017
</span></td></tr></table>
</td></tr></table></td></tr>
<tr><td style="padding: 16px 12px 12px 12px" align="left">
<p style="margin-top: 0; font-size: 1.0em; line-height: 1.5em; padding-top: 0; margin-bottom: 20px; background-color: #f6f6f6; padding: 12px"><b>A note from your editor, </strong> is also looking strong if you want to stay up to date with the latest database news :-)</p>
<div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">Based on D3.js v4 and built around reusable components, Britecharts makes it easy to declaratively build charts and visualizations, such as  too.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Eventbrite
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">The Fetch API is now supported in all mainstream browsers (except IE). It’s promise based and far more elegant than XMLHttpRequest. This is a very thorough intro.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Zell Liew
</div>
<br clear="all" style="clear: both"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">Become a Full Stack Engineer and gain the confidence to master the command line and server.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Frontend Masters
  <span style="border: 1px solid #999; border-radius: 2px; color: #999; font-size: 11px; font-weight: normal; padding: 1px 5px 1px 5px; ">Sponsor</span>
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">ES6/ES2015 modules are now natively supported in Chrome Canary behind the <em>Experimental Web Platform</em> flag. Here’s the basics of how they work. You may also like  showing off a use case.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Sam Thorogood
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">Like a test runner but for performance. It runs in Chrome (headlessly too, if you have the right version) and produces reports on your code’s execution.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Nicolas Gryman
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">Still an alpha/work-in-progress but is significantly faster than other minifiers due to taking a unique approach. Also supports ES6 upwards.</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Rich Harris
</div>
<br clear="all" style="clear: both"><div style="font-size: 18px; margin: 2px 0px"></div>
<div style="font-size: 14px; line-height: 19px; margin-top: 0px; margin-bottom: 3px">First linked a month ago as a pure decoder, now it does lossy encoding too. 
</div>
<div style="color: #999999; font-weight: normal; font-size: 12px; line-height: 14px; text-transform: uppercase; margin-top: 5px; font-family: verdana, arial, sans-serif">
Photopea
</div>
<br clear="all" style="clear: both"><p style="color: #666666; font-size: 16px; font-weight: bold; margin-top: 8px; margin-bottom: 10px; text-transform: uppercase">Jobs </p>
<ul style="padding-left: 18px; margin-top: 10px; list-style-type: square">
<li style="color: #f7df1e; margin-bottom: 10px; font-size: 15px; line-height: 17px">
<span style="font-size: 12px; color: #666666">Web devs with JavaScript, CSS, and HTML experience wanted to design and ship new features, and see them loved (or hated) by millions.</span> <span style="color: #999999; font-weight: normal; font-size: 12px; text-transform: uppercase; font-family: verdana, arial, sans-serif">craigslist</span>
</li>
<li style="color: #f7df1e; margin-bottom: 10px; font-size: 15px; line-height: 17px">
<span style="font-size: 12px; color: #666666">We're looking for an enthusiastic front end engineer to join our team. 3 blocks from the beach. Go to our website to learn more.</span> <span style="color: #999999; font-weight: normal; font-size: 12px; text-transform: uppercase; font-family: verdana, arial, sans-serif">MJD Interactive</span>
</li>
<li style="color: #f7df1e; margin-bottom: 10px; font-size: 15px; line-height: 17px">
<span style="font-size: 12px; color: #666666">Booking.com is looking for Front End Developers all around the globe to join us at our beautiful headquarters in Amsterdam.</span> <span style="color: #999999; font-weight: normal; font-size: 12px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Booking<span>.</span>com</span>
</li>
</ul>
<p style="color: #333; font-size: 12px; font-weight: normal; margin-top: 0px; margin-bottom: 10px">Can't find the right job? Want companies to apply to <em>you?</em> </p>
<p style="color: #666666; font-size: 16px; font-weight: bold; margin-top: 24px; margin-bottom: 10px; text-transform: uppercase">In Brief</p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #00aadd; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">news</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Facebook</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #00aadd; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">news</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">In Porto Alegre (Aug 25-26) and Fortaleza (Sep 1-2).</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif"></span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <br><span style="font-size: 13px; color: #444444; line-height: 19px">PubNub gets your data anywhere in under 0.25 seconds. It’s easy with PubNub’s Angular library.</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">PubNub  <span style="border: 1px solid #999; border-radius: 2px; color: #999; font-size: 11px; font-weight: normal; padding: 1px 5px 1px 5px;">Sponsor</span></span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Lucas Fernandes da Costa</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #6ca629; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">node</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Danny Grander</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Todd Motto</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Louis Hoebregts</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Dr. Axel Rauschmayer</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Reg Braithwaite</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> user.</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Elad Ossadon</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #99dd00; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tutorial</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Zell Liew</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #bbbbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tools</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Bugsnag  <span style="border: 1px solid #999; border-radius: 2px; color: #999; font-size: 11px; font-weight: normal; padding: 1px 5px 1px 5px;">Sponsor</span></span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #bbbbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">tools</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Michael Wanyoike</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #00bbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">code</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Reaction Commerce</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #00bbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">code</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Wei Song</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #00bbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">code</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Levin Van</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px"> <span style="font-size: 11px; padding: 1px 3px; text-transform: uppercase; background-color: #00bbbb; color: #fff; font-weight: normal; font-family: verdana, arial, sans-serif">code</span> <br><span style="font-size: 13px; color: #444444; line-height: 19px">Well documented and with live examples.</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Ahmed Bouhuolia</span></p>
<p style="color: #f7df1e; margin-bottom: 14px; font-size: 16px; line-height: 18px">.</span><br><span style="color: #999999; font-weight: normal; font-size: 11px; line-height: 16px; text-transform: uppercase; font-family: verdana, arial, sans-serif">Red Gate  <span style="border: 1px solid #999; border-radius: 2px; color: #999; font-size: 11px; font-weight: normal; padding: 1px 5px 1px 5px;">Sponsor</span></span></p>
<p style="margin-top: 0; font-size: 1.0em; line-height: 1.5em; padding-top: 0; margin-bottom: 20px; background-color: #f6f6f6; padding: 12px"><b>P.S.</b> Wondering where all the React stuff is? It's in its own newsletter, </p>
</td></tr>
<tr><td bgcolor="#f4f4f4" style="font-family: verdana, helvetica, arial, sans-serif; text-align: left; padding-top: 12px; padding-left: 12px; padding-right: 12px; padding-bottom: 12px" class="noarchive">
<p style="line-height: 15px; font-size: 11px; margin-top: 0">Curated by .</p>
<p style="line-height: 15px; font-size: 11px; margin-top: 0">Like this? You may also enjoy: </p>
<p style="font-size: 13px"></p>
<p style="font-size: 11px; line-height: 15px">© Cooperpress Ltd. Office 30, Lincoln Way, Louth, LN11 0LS, UK</p>
</td></tr>
</table>
</td></tr></table>
---------------
<h1 id="#title_7" >8、GCC 7.1发布，完全支持C++17</h1>
Sergio De Simone
[http://www.infoq.com/cn/news/2017/05/gcc-71-released?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/05/gcc-71-released?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>据GCC的维护者Jakub Jelinek所写，在GNU编译器套件集GCC的最新主版本GCC 7.1中，提供了丰富的新特性，包括：对当前C++17草案的实验性支持、更好的诊断能力以及新的优化技术。</p> <i>By Sergio De Simone</i> <i> Translated by Rays</i>
---------------
<h1 id="#title_8" >9、Google发力智能识别：Cloud Speech API正式发布</h1>
Kent Weare
[http://www.infoq.com/cn/news/2017/05/Google-Cloud-Speech-API?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/05/Google-Cloud-Speech-API?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/news/2017/05/Google-Cloud-Speech-API/zh/headerimage/GettyImages-540218890.jpg"/><p>Google在近期的博客帖子中，宣布它们的Cloud Speech API正式发布。Cloud Speech API允许开发人员添加预先训练好的机器学习模型，用于视频、图像和文本分析中的识别任务，并可实现动态翻译。Cloud Speech API曾于去年夏天以测试版发布。</p> <i>By Kent Weare</i> <i> Translated by Rays</i>
---------------
<h1 id="#title_9" >10、MongoDB Atlas扩展了AWS服务</h1>
Alex Giamas
[http://www.infoq.com/cn/news/2017/05/MongoDB-Atlas-AWS-Expansion?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/05/MongoDB-Atlas-AWS-Expansion?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>作为广受欢迎的NoSQL数据库之一，MongoDB已成为很多Web系统中实际使用的非关系型数据库，它随着PaaS和IaaS服务提供商的增长而一并增长。MongoDB Atlas是MongoDB有限公司发布的DBaaS服务，目前已在14个AWS区域中可用，本地存储在三个AWS区域上可用。</p> <i>By Alex Giamas</i> <i> Translated by Rays</i>
---------------
<h1 id="#title_10" >11、Reinhold就Jigsaw投票一事向JCP提交公开信</h1>
Charles Humble
[http://www.infoq.com/cn/news/2017/05/jigsaw-open-letter?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/05/jigsaw-open-letter?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Mark Reinhold 向 JCP 执行委员会提交了一封公开信，在公开信中，他表示对 IBM 投了 JSR 376 反对票一事感到震惊，并争辩说，Red Hat 之所以也投反对票，是出于“保护他们自家的非标准模块化系统，而这个系统在 JBoss/Wildfly 之外的生态系统并没有多少用武之地”。</p> <i>By Charles Humble</i> <i> Translated by 薛命灯</i>
---------------
<h1 id="#title_11" >12、.NET Framework 4.7正式发布</h1>
Jeff Martin
[http://www.infoq.com/cn/news/2017/05/net47-released?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/05/net47-released?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>以前.NET Framework 4.7是随Windows 10 Creators Edition一并提供的，现在它已经正式发布，这意味着使用旧版本Windows的用户现在也能安装它了。.NET Framework 4.7通过Windows 10 Anniversary Update发布，支持Windows 7 SP1及以上版本，其中提供了一些新的特性，包括对C#和VB15的支持、一些软件缺陷的修正，以及更大程度上的加密支持。</p> <i>By Jeff Martin</i> <i> Translated by Rays</i>
---------------