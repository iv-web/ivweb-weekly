## 文章索引
1、 <a href="#1iaaspaassaas-的区别" >IaaS，PaaS，SaaS 的区别</a><br/>
2、 <a href="#2文章-timimg-is-almost-everything作者访谈" >文章： 《Timimg is Almost Everything》作者访谈</a><br/>
3、 <a href="#3视频演讲-直面音视频质量评估之痛走进腾讯音视频质量体系" >视频演讲： 直面音视频质量评估之痛——走进腾讯音视频质量体系</a><br/>
4、 <a href="#4文章-2017年你还在用用户画像和协同过滤做推荐系统吗" >文章： 2017年，你还在用用户画像和协同过滤做推荐系统吗？</a><br/>
5、 <a href="#5文章-mxnet-api入门-第6篇" >文章： MXNet API入门 —第6篇</a><br/><h1 id="#title_0" >1、IaaS，PaaS，SaaS 的区别</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2017/07/iaas-paas-saas.html](http://www.ruanyifeng.com/blog/2017/07/iaas-paas-saas.html)
<p>越来越多的软件，开始采用云服务。</p>

        <p>云服务只是一个统称，可以分成三大类。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017072301.jpg" alt="" title="" /></p>

<blockquote>
  <ul>
<li><strong>IaaS</strong>：基础设施服务，Infrastructure-as-a-service</li>
<li><strong>PaaS</strong>：平台服务，Platform-as-a-service</li>
<li><strong>SaaS</strong>：软件服务，Software-as-a-service</li>
</ul>
</blockquote>

<p>它们有什么区别呢？</p>

<p>IBM 的软件架构师 Albert Barron 曾经使用披萨作为比喻，，让它变得更准确易懂。</p>

<p>请设想你是一个餐饮业者，打算做披萨生意。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017072302.jpg" alt="" title="" /></p>

<p>你可以从头到尾，自己生产披萨，但是这样比较麻烦，需要准备的东西多，因此你决定外包一部分工作，采用他人的服务。你有三个方案。</p>

<p><strong>（1）方案一：IaaS</strong></p>

<p>他人提供厨房、炉子、煤气，你使用这些基础设施，来烤你的披萨。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017072303.jpg" alt="" title="" /></p>

<p><strong>（2）方案二：PaaS</strong></p>

<p>除了基础设施，他人还提供披萨饼皮。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017072304.jpg" alt="" title="" /></p>

<p>你只要把自己的配料洒在饼皮上，让他帮你烤出来就行了。也就是说，你要做的就是设计披萨的味道（海鲜披萨或者鸡肉披萨），他人提供平台服务，让你把自己的设计实现。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017072308.jpg" alt="" title="" /></p>

<p><strong>（3）方案三：SaaS</strong></p>

<p>他人直接做好了披萨，不用你的介入，到手的就是一个成品。你要做的就是把它卖出去，最多再包装一下，印上你自己的 Logo。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017072305.jpg" alt="" title="" /></p>

<p>上面的三种方案，可以总结成下面这张图。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017072306.png" alt="" title="" /></p>

<p>从左到右，自己承担的工作量（上图蓝色部分）越来越少，IaaS > PaaS > SaaS。</p>

<p>对应软件开发，则是下面这张图。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017072307.jpg" alt="" title="" /></p>

<p><strong>SaaS 是软件的开发、管理、部署都交给第三方，不需要关心技术问题，可以拿来即用。</strong>普通用户接触到的互联网服务，几乎都是 SaaS，下面是一些例子。</p>

<blockquote>
  <ul>
<li>客户管理服务 Salesforce</li>
<li>团队协同服务 Google Apps</li>
<li>储存服务 Box</li>
<li>储存服务 Dropbox</li>
<li>社交服务 Facebook / Twitter / Instagram</li>
</ul>
</blockquote>

<p><strong>PaaS 提供软件部署平台（runtime），抽象掉了硬件和操作系统细节，可以无缝地扩展（scaling）。开发者只需要关注自己的业务逻辑，不需要关注底层。</strong>下面这些都属于 PaaS。</p>

<blockquote>
  <ul>
<li>Heroku</li>
<li>Google App Engine</li>
<li>OpenShift</li>
</ul>
</blockquote>

<p><strong>IaaS 是云服务的最底层，主要提供一些基础资源。</strong>它与 PaaS 的区别是，用户需要自己控制底层，实现基础设施的使用逻辑。下面这些都属于 IaaS。</p>

<blockquote>
  <ul>
<li>Amazon EC2</li>
<li>Digital Ocean</li>
<li>RackSpace Cloud</li>
</ul>
</blockquote>

<p><strong>参考链接</strong></p>

<ul>
<li>, by David Ng</li>
<li>, by Eamonn Colman</li>
</ul>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2017-07-23T11:20:46+08:00">2017年7月23日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>博客文集：</li>
<li>社交媒体：</li>
<li>Feed订阅： </li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------
<h1 id="#title_1" >2、文章： 《Timimg is Almost Everything》作者访谈</h1>
Ben Linders
[http://www.infoq.com/cn/articles/book-review-timing-everything?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/book-review-timing-everything?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/book-review-timing-everything/zh/smallimage/cover.jpg"/><p>高管们可以也应该参与到软件开发中去。在这本书中，Roland Racko展示了如何通过在软件开发计划的早期阶段使用“问询式管理”的管理风格来提高软件的成功率，进而影响团队的思考和行为方式。</p> <i>By Ben Linders</i> <i> Translated by 孙浩</i>
---------------
<h1 id="#title_2" >3、视频演讲： 直面音视频质量评估之痛——走进腾讯音视频质量体系</h1>
罗必达
[http://www.infoq.com/cn/presentations/enter-tencent-audio-and-video-quality-system?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/enter-tencent-audio-and-video-quality-system?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/enter-tencent-audio-and-video-quality-system/zh/mediumimage/luobida270.jpg"/><p>高质量的音视频通话技术离不开相应的评估与测试体系，音视频质量评估是音视频技术开发和测试都必须具备的基本技能。本次分享围绕音视频质量评估的三大挑战，来给大家介绍音视频质量体系以及腾讯音视频实验室在这方面的思考与实践。内容涵盖如何合理安排主观测试与客观测试，音视频测试实验室的搭建，以及利用无参考评估建立线上音视频质量全维度数据分析与监控能力。</p> <i>By 罗必达</i>
---------------
<h1 id="#title_3" >4、文章： 2017年，你还在用用户画像和协同过滤做推荐系统吗？</h1>
周开拓
[http://www.infoq.com/cn/articles/user-portrait-collaborative-filtering-for-recommend-systems?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/user-portrait-collaborative-filtering-for-recommend-systems?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/user-portrait-collaborative-filtering-for-recommend-systems/zh/smallimage/learning_logo.jpg"/><p>如何使用大规模机器学习解决真实的业务问题？我们今天会以机器学习中的一个典型场景为例来讲解，即基于大规模机器学习模型的推荐系统。</p> <i>By 周开拓</i>
---------------
<h1 id="#title_4" >5、文章： MXNet API入门 —第6篇</h1>
Julien Simon
[http://www.infoq.com/cn/articles/an-introduction-to-the-mxnet-api-part06?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/an-introduction-to-the-mxnet-api-part06?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/an-introduction-to-the-mxnet-api-part06/zh/smallimage/Crashlytics_100_100.jpg"/><p>Apache MXNet是一种功能全面、可以灵活编程并且扩展能力超强的深度学习框架，支持包括卷积神经网络(CNN)与长短期记忆网络(LSTM)在内的顶尖深度模型。这一系列文章介绍了MXNet的基本概念和使用方法。本篇主要介绍不同模型的对比结果。</p> <i>By Julien Simon</i> <i> Translated by 大愚若智</i>
---------------