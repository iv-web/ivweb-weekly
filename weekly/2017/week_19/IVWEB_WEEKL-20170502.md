## 文章索引
1、 <a href="#1fish-shell-入门教程" >Fish shell 入门教程</a><br/>
2、 <a href="#2文章-信息架构ia之不存人工智能ai将焉附" >文章： 信息架构（IA）之不存，人工智能（AI）将焉附</a><br/>
3、 <a href="#3文章-深度学习指南在ios平台上使用tensorflow" >文章： 深度学习指南：在iOS平台上使用TensorFlow</a><br/>
4、 <a href="#4视频演讲-mip移动页面加速器的架构与原理" >视频演讲： MIP移动页面加速器的架构与原理</a><br/>
5、 <a href="#5视频演讲-spotify-广告系统架构演进" >视频演讲： Spotify-广告系统架构演进</a><br/>
6、 <a href="#6文章-nasa的10条代码编写原则" >文章： NASA的10条代码编写原则</a><br/><h1 id="#title_0" >1、Fish shell 入门教程</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2017/05/fish_shell.html](http://www.ruanyifeng.com/blog/2017/05/fish_shell.html)
<p>是程序员的必备技能。图形界面虽然好看，解决问题还是要靠命令行。</p>

        <p>命令行由 Shell 提供。各种命令通过 Shell，传递给操作系统的内核。学习命令行就是在学习 Shell。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017050201.jpg" alt="" title="" /></p>

<p>Shell 有好几种，目前最常用是  好用。</p>

<p>五年前，我第一次尝试 Fish，感到很惊艳，一直用到现在。本文介绍 Fish 的主要特点，希望你也来尝试它。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017050202.jpg" alt="" title="" /></p>

<p>感谢对本文提供赞助，结尾处有他们的课程推荐。</p>

<h2>一、简介</h2>

<p>Fish 是"the <span style="font-weight: 700;">f</span>riendly <span style="font-weight: 700;">i</span>nteractive <span style="font-weight: 700;">sh</span>ell"的简称，最大特点就是方便易用。很多其他 Shell 需要配置才有的功能，Fish 默认提供，不需要任何配置。</p>

<p>如果你想拥有一个方便好用的 Shell，又不想学习一大堆语法，或者花费很多时间配置，那么你一定要尝试一下 Fish。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017050204.png" alt="" title="" /></p>

<h2>二、安装</h2>

<p>Ubuntu 和 Debian 的安装方法。</p>

<blockquote><pre><code class="language-bash">
$ sudo apt-get install fish
</code></pre></blockquote>

<p>Mac 的安装方法。</p>

<blockquote><pre><code class="language-bash">
$ brew install fish
</code></pre></blockquote>

<p>其他系统的安装请参考。</p>

<h2>三、启动与帮助</h2>

<p>安装完成后，就可以启动 Fish。</p>

<blockquote><pre><code class="language-bash">
$ fish
</code></pre></blockquote>

<p>由于 Fish 的语法与 Bash 有很大差异，Bash 脚本一般不兼容。因此，我建议不要将 Fish 设为默认 Shell，而是每次手动启动它。</p>

<p>使用过程中，如果需要帮助，可以输入<code>help</code>命令。浏览器就会自动打开，显示在线文档。</p>

<blockquote><pre><code class="language-bash">
$ help
</code></pre></blockquote>

<h2>四、彩色显示</h2>

<p>进入 Fish 以后，你注意到的第一件事，可能就是它默认彩色显示。</p>

<blockquote style="font-size: initial;"><pre><code>
# 无效命令为红色
$ <span style="color:red;">mkd</span>

# 有效命令为蓝色
$ <span style="color: blue;">mkdir</span>
</code></pre></blockquote>

<p>有效路径会有下划线。</p>

<blockquote style="font-size: initial;"><pre><code>
$ cat <span style="text-decoration: underline;">~/somefi</span> 
</code></pre></blockquote>

<p>上面代码表示，存在以<code>~/somefi</code>开头的路径。如果没有下划线，你就知道这个路径不存在。</p>

<h2>五、自动建议</h2>

<p>Fish 会自动在光标后面给出建议，表示可能的选项，颜色为灰色。</p>

<blockquote style="font-size: initial;"><pre><code>
# 命令建议
$ /bin/h<span style="color: gray;text-decoration: underline;">o</span><span style="color: gray;">stname</span>

# 参数建议
$ grep --i<span style="color: gray;">gnore-case</span>

# 路径建议
$ ls <span style="color: blue;text-decoration: underline;">no</span><span style="color: gray;">de_modules</span>
</code></pre></blockquote>

<p>如果采纳建议，可以按下<code>→</code>或<code>Control + F</code>。如果只采纳一部分，可以按下<code>Alt + →</code>。</p>

<h2>六、自动补全</h2>

<p>输入命令时，Fish 会自动显示匹配的上一条历史记录。</p>

<blockquote style="font-size: initial;"><pre><code>
$ g<span style="color: gray;">it commit -m "feat: first commit"</span>
</code></pre></blockquote>

<p>如果没有匹配的历史记录，Fish 会猜测可能的结果，自动补全各种输入。比如，输入<code>pyt</code>再按下<code>Tab</code>，就会自动补全为<code>python</code>命令。</p>

<p>如果有多个可能的结果，Fish 会把它们都列出，还带有简要介绍。</p>

<blockquote><pre><code class="language-bash">
$ vi[按下 Tab 键]

vi (Executable link, 2.7MB)
view (Vi IMproved, 一个程序员的文本编辑器)
viewer.py (Executable, 967B)
viewres  (Graphical class browser for Xt)
...and 12 more rows
</code></pre></blockquote>

<p>这时，再按一次<code>tab</code>，就可以在这些命令之中选择。</p>

<p>除了补全命令，Fish 还可以补全参数。比如，<code>ls</code>命令的<code>-l</code>参数后面按下<code>Tab</code>键，就会显示可以连用的其他参数。</p>

<blockquote><pre><code class="language-bash">
$ ls -l[按下 Tab 键]

-l1  (List one file per line)
-lA  (Show hidden except . and ..)  
-la  (Show hidden)
-lB  (Ignore files ending with ~)
...and 16 more rows```
</code></pre></blockquote>

<p>Fish 还可以自动补全 Git 分支。</p>

<blockquote style="font-size: initial;"><pre><code>
$ git checkout m<span style="color: gray">aster</span>
</code></pre></blockquote>

<h2>七、易懂的语法</h2>

<p>Fish 的语法非常自然，一眼就能看懂。</p>

<p><code>if</code>语句。</p>

<blockquote><pre><code class="language-bash">
if grep fish /etc/shells
    echo Found fish
else if grep bash /etc/shells
    echo Found bash
else
    echo Got nothing
end
</code></pre></blockquote>

<p><code>switch</code>语句。</p>

<blockquote><pre><code class="language-bash">
switch (uname)
case Linux
    echo Hi Tux!
case Darwin
    echo Hi Hexley!
case FreeBSD NetBSD DragonFly
    echo Hi Beastie!
case '*'
    echo Hi, stranger!
end
</code></pre></blockquote>

<p><code>while</code>循环。</p>

<blockquote><pre><code class="language-bash">
while true
    echo "Loop forever"
end
</code></pre></blockquote>

<p><code>for</code>循环。</p>

<blockquote><pre><code class="language-bash">
for file in *.txt
    cp $file $file.bak
end
</code></pre></blockquote>

<h2>八、函数</h2>

<p>Fish 的函数用来封装命令，或者为现有的命令起别名。</p>

<blockquote><pre><code class="language-bash">
function ll
    ls -lhG $argv
end
</code></pre></blockquote>

<p>上面代码定义了一个<code>ll</code>函数。命令行执行这个函数以后，就可以用<code>ll</code>命令替代<code>ls -lhG</code>。其中，变量<code>$argv</code>表示函数的参数。</p>

<p>下面是另一个例子。</p>

<blockquote><pre><code class="language-bash">
function ls
    command ls -hG $argv
end
</code></pre></blockquote>

<p>上面的代码重新定义<code>ls</code>命令。注意，函数体内的<code>ls</code>之前，要加上<code>command</code>，否则会因为无限循环而报错。</p>

<h2>九、提示符</h2>

<p><code>fish_prompt</code>函数用于定义命令行提示符（prompt）。</p>

<blockquote><pre><code class="language-bash">
function fish_prompt
    set_color purple
    date "+%m/%d/%y"
    set_color FF0
    echo (pwd) '>'
    set_color normal
end
</code></pre></blockquote>

<p>执行上面的函数以后，你的命令行提示符就会变成下面这样。</p>

<blockquote><pre><code class="language-bash">
02/06/13
/home/tutorial > 
</code></pre></blockquote>

<h2>十、配置</h2>

<p>Fish 的配置文件是<code>~/.config/fish/config.fish</code>，每次 Fish 启动，就会自动加载这个文件。</p>

<p>我们可以在这个文件里面写入各种自定义函数，它们会被自动加载。比如，上面的<code>fish_prompt</code>函数就可以写在这个文件里面，这样每次启动 Fish，就会出现自定义的提示符。</p>

<p>Fish 还提供 Web 界面配置该文件。</p>

<blockquote><pre><code class="language-bash">
$ fish_config
</code></pre></blockquote>

<p>输入上面的命令以后，浏览器就会自动打开本机的 8000 端口，用户可以在网页上对 Fish 进行配置，比如选择提示符和配色主题。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017050203.png" alt="" title="" /></p>

<p>（正文完）</p>

<hr />

<p>下面是推广时间。</p>

<p>最近，Angela Zhu 在她的公众号发文。</p>

<blockquote>
  <p>"前些日子，突发奇想，在我的小密圈里提了这样一个问题：'未来，什么样的程序员才是不可替代的?'"</p>
</blockquote>

<p>曹政回复了一篇。</p>

<blockquote>
  <p>"从我的历史来说，我一直追寻的是让自己可替代，不论是去尽可能培养年轻的接班人，还是外部延聘比我更出色的技术高手。如果没有人可以接手我的系统，我设计的平台，我才会觉得紧张和不安。"</p>
</blockquote>

<p>这个讨论涉及了很多问题。</p>

<blockquote>
  <ul>
<li>个人如何保持竞争力</li>
<li>公司如何选人</li>
<li>如何留住人才</li>
</ul>
</blockquote>

<p>这些问题没有标准答案。但是，有一点是肯定的：程序员必须勇于尝试、开拓和创新，在挑战和失败面前不放弃。</p>

<p>帮助你形成自己的竞争力。</p>

<p></p>

<p>，他是谷歌无人驾驶汽车项目的奠基人。感兴趣的朋友不要错过，如果试听不满意，一周内全额退款。</p>

<p></p>

<p>优达学城还有一门，重点讲授编程基础和数学基础（线性代数、微积分和统计学），适合不知道如何入门的年轻朋友。</p>

<p>另外，还有等课程，大家也可以关注。</p>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2017-05-02T07:45:33+08:00">2017年5月 2日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>博客文集：</li>
<li>社交媒体：</li>
<li>Feed订阅： </li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------
<h1 id="#title_1" >2、文章： 信息架构（IA）之不存，人工智能（AI）将焉附</h1>
Seth Earley
[http://www.infoq.com/cn/articles/artificial-intelligence?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/artificial-intelligence?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/artificial-intelligence/zh/headerimage/GettyImages-148059275.jpg"/><p>人工智能正日益受到各行各业中不同规模的企业的重视，从资金充裕的初创公司到一些久负盛名的软件企业。在本文中，作者介绍了可用于企业及其客户之前，人工智能技术在需要高质量的结构化数据。</p> <i>By Seth Earley</i> <i> Translated by Rays</i>
---------------
<h1 id="#title_2" >3、文章： 深度学习指南：在iOS平台上使用TensorFlow</h1>
Matthijs Hollemans
[http://www.infoq.com/cn/articles/getting-started-with-tensorflow-on-ios?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/getting-started-with-tensorflow-on-ios?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/getting-started-with-tensorflow-on-ios/zh/smallimage/risk-logo-small.jpg"/><p>本文主要介绍TensorFlow背后的设计思路、如何利用其训练一套简单的分类器，以及如何将上述成果引入您的iOS应用。</p> <i>By Matthijs Hollemans</i> <i> Translated by 运和凭</i>
---------------
<h1 id="#title_3" >4、视频演讲： MIP移动页面加速器的架构与原理</h1>
李浪波
[http://www.infoq.com/cn/presentations/arch-and-principle-of-mip-mobile-page-accelerator?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/arch-and-principle-of-mip-mobile-page-accelerator?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/arch-and-principle-of-mip-mobile-page-accelerator/zh/mediumimage/liangbo270.jpg"/><p>MIP是百度推出的通用移动页面加速解决方案，可大幅的提升移动页面的访问速度和到达率，MIP目前已覆盖的上亿流量。本次分享介绍移动页面加速器（MIP）的架构设计和加速原理。本次将重点介绍MIP的简介、架构设计和加速原理等方面。 </p> <i>By 李浪波</i>
---------------
<h1 id="#title_4" >5、视频演讲： Spotify-广告系统架构演进</h1>
Kinshuk Mishra
[http://www.infoq.com/cn/presentations/spotify-advertising-system-arch-evolution?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/spotify-advertising-system-arch-evolution?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/spotify-advertising-system-arch-evolution/zh/mediumimage/kkkk270.jpg"/><p>在产品高速成长的公司中，随着技术的改进，系统的持续演进是不可避免的。产品和业务需求也不断演进，规模的变化又会影响运营成本。近年来，Spotify 的广告系统经历了几次大的变化。对 Spotify 的广告技术栈而言，性能是刚需——要做到大规模、高可用、低延迟。任何宕机或业务中断都会直接影响收入。随着新兴消费平台的兴起，后端和数据基础设施技术也已经成熟，Spotify 的产品也有很多改进。广告技术系统的需求也在变化。Kinshuk 将在演讲中分享保证日常服务不中断的前提下改进 Spotify 广告系统的经验。</p> <i>By Kinshuk Mishra</i>
---------------
<h1 id="#title_5" >6、文章： NASA的10条代码编写原则</h1>
Gerard J. Holzmann
[http://www.infoq.com/cn/articles/nasa-10-coding-rules-for-safety-critical-program?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/nasa-10-coding-rules-for-safety-critical-program?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/nasa-10-coding-rules-for-safety-critical-program/zh/smallimage/huiyi.jpg"/><p>有时候，编写代码必须遵守一定的原则，尤其是在代码的正确性会对人的生命产生决定性影响的领域，例如飞机、将宇航员送上同步轨道的航天器，以及距离居住地仅几英里远的核电站等设施运行的控制代码。本文将介绍由NASA喷气推进实验室首席科学家Gerard J. Holzmann所提出的，侧重于安全参数的10条代码编写原则。</p> <i>By Gerard J. Holzmann</i> <i> Translated by 大愚若智</i>
---------------