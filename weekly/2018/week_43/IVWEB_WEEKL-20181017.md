## 文章索引
1、 <a href="#1文章-nextjs-70正式发布重新编译速度提高42％支持webassembly" >文章： Next.js 7.0正式发布：重新编译速度提高42％，支持WebAssembly</a><br/>
2、 <a href="#2文章-2018年top-26-javascript面试问题和答案" >文章： 2018年，Top 26 JavaScript面试问题和答案</a><br/>
3、 <a href="#3人人恐惧ai寒冬他却希望泡沫再破裂一次" >人人恐惧AI寒冬，他却希望泡沫再破裂一次</a><br/>
4、 <a href="#4exfat-文件系统指南" >exFAT 文件系统指南</a><br/>
5、 <a href="#5文章-zalando的自治扩展" >文章： Zalando的自治扩展</a><br/>
6、 <a href="#6文章-devops-&-sre-必备技能清单" >文章： DevOps & SRE 必备技能清单</a><br/>
7、 <a href="#7photoshop-workflows-and-shortcuts-for-digital-artists" >Photoshop Workflows And Shortcuts For Digital Artists</a><br/>
8、 <a href="#8nvidia宣布rapids医学影像应用和面向自动驾驶汽车的驾驶模拟器" >NVIDIA宣布RAPIDS、医学影像应用和面向自动驾驶汽车的驾驶模拟器</a><br/>
9、 <a href="#9微软发布azure-storage不可变存储功能的正式版本" >微软发布Azure Storage不可变存储功能的正式版本</a><br/>
10、 <a href="#10git-submodule新漏洞已修复" >Git Submodule新漏洞已修复</a><br/>
11、 <a href="#11cloudflare推出域名注册服务不赚利润只收取成本费" >Cloudflare推出域名注册服务：不赚利润只收取成本费</a><br/>
12、 <a href="#12facebook曝至今最严重安全漏洞超过5000万用户受影响" >Facebook曝至今最严重安全漏洞，超过5000万用户受影响</a><br/><h1 id="#title_0" >1、文章： Next.js 7.0正式发布：重新编译速度提高42％，支持WebAssembly</h1>
Next.js博客
[http://www.infoq.com/cn/articles/production-ready-Next.js-7?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/production-ready-Next.js-7?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/production-ready-Next.js-7/zh/smallimage/scaled-autonomy-zalando-S-1538122654146-1539415354048.jpeg"/><p>在经过26次金丝雀发布和340万次下载之后，现在，我们正式推出生产就绪的Next.js 7。</p> <i>By Next.js博客</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_1" >2、文章： 2018年，Top 26 JavaScript面试问题和答案</h1>
FullStack.Cafe
[http://www.infoq.com/cn/articles/top-26-javascript-interview-questions-and-answers-in-2019?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/top-26-javascript-interview-questions-and-answers-in-2019?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/top-26-javascript-interview-questions-and-answers-in-2019/zh/smallimage/logo-1522948961955-1539416511836.jpeg"/><p>根据Stack Overflow的2018年度调查，JavaScript连续六年成为最常用的编程语言。所以我们必须面对这样的现实，JavaScript已经成为全栈开发技能的基石，在全栈开发面试中都会不可避免地涉及到与JavaScript有关的问题。FullStack.Cafe汇编了最常见的JavaScript面试问题和答案，希望能够帮助读者找到下一份梦想中的工作。</p> <i>By FullStack.Cafe</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_2" >3、人人恐惧AI寒冬，他却希望泡沫再破裂一次</h1>
Natalie
[http://www.infoq.com/cn/news/2018/10/ai-fear-winter?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/10/ai-fear-winter?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>AI应用落地，核心是工程问题，不是算法问题，更不是“哲学”问题。一定要特别特别“土”，踏踏实实从朴素的运维、数据库、数据清洗做起，从实际的工程中逐步演化。只有扎扎实实从工程出发，才能实事求是地发展出低成本的、有生命力的AI系统。</p> <i>By Natalie</i>
---------------
<h1 id="#title_3" >4、exFAT 文件系统指南</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2018/10/exfat.html](http://www.ruanyifeng.com/blog/2018/10/exfat.html)
<p>国庆假期，我拍了一些手机视频，打算存到新买的移动硬盘。</p>

        <p>然后，就傻眼了。我的 Mac 电脑无法写入移动硬盘，因为移动硬盘的默认文件系统是 NTFS，Mac 不支持写入 NTFS。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201810/bg2018101601.jpg" alt="" title="" /></p>

<p>虽然可以买一个软件解决这个问题，但是我不想为这种功能付钱。经过一番研究，我发现把移动硬盘的文件系统改成 exFAT，就可以解决问题，Mac 原生支持读写 exFAT。</p>

<p>由于这个问题很普遍，下面我就来写一写跟 exFAT 相关的知识。</p>

<h2>一、文件系统</h2>

<p>所谓文件系统，就是文件的储存方式。简单说，它就是一个门牌系统，为储存设备划分门牌号，每个文件分配一个门牌，然后就能按照门牌找到文件。</p>

<p>没有文件系统的硬盘，就是一块荒地。如果有人住在那里，你只能说那里有人住，精确位置你说不出来。只有划分了路牌，你才能说出，这个人住在"人民路15号"，这样才能精确定位。文件系统就是路牌的划分方法。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201810/bg2018101602.jpg" alt="" title="" /></p>

<p>储存设备都需要指定文件系统，计算机才能读写。所谓"格式化"，就是为硬盘安装文件系统。不同的操作系统有不同的文件系统，Linux 使用 ext4，OSX使用 HFS +，Windows 使用 NTFS，Solaris 和 Unix 使用ZFS。如果计算机不认识某个文件系统，就会显示这块盘无法读写。</p>

<p>现在的问题就是，NTFS 文件系统是 Windows 的专有系统，Mac 可以读，但是默认不能写入。</p>

<h2>二、Windows 的文件系统</h2>

<p>Windows 系统主要有三种文件系统。</p>

<blockquote>
  <ul>
<li>FAT32</li>
<li>NTFS</li>
<li>exFAT</li>
</ul>
</blockquote>

<p>格式化硬盘的时候，Windows 系统会提供这三种文件系统让你选。这时应该选哪一种呢？</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201810/bg2018101603.jpg" alt="" title="" /></p>

<p>FAT32 是最老的文件系统，所有操作系统都支持，兼容性最好。但是，它是为32位计算机设计的，文件不能超过 2<sup>32</sup> - 1 个字节，也就是不能超过 4GB，分区不能超过 8TB。目前来看，这个文件系统有点过时了，只适合小文件，如果有大的视频文件，就不能使用它。</p>

<p>NTFS 是 Windows 的默认文件系统，用来替换 FAT32。Windows 的系统盘只能使用这个系统，移动硬盘买来装的也是它。</p>

<p>exFAT 可以看作是 FAT32 的64位升级版，<code>ex</code>就是 extended 的缩写（表示"扩展的 FAT32"），功能不如 NTFS，但是解决了文件和分区的大小问题，两者最大都可以到 128PB。由于 Mac 和 Linux 电脑可以读写这种系统，所以移动硬盘的文件系统可以改成它。</p>

<h2>三、解决方案</h2>

<p>移动硬盘买来后，你把它格式化成 exFAT 文件系统，问题就解决了。</p>

<p>Windows 在资源管理器或我的电脑里面，都可以进行格式化。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201810/bg2018101604.jpg" alt="" title="" /></p>

<p>Mac 在进行格式化。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201810/bg2018101605.jpg" alt="" title="" /></p>

<p>格式化完成后，就 OK 了。如果你使用 Linux 系统，可能需要装一下 exFAT 支持，Ubuntu 和 Debian 执行下面的命令。</p>

<blockquote><pre><code class="language-bash">
$ sudo apt-get install exfat-utils exfat-fuse
</code></pre></blockquote>

<p>一般读者读到这里，就可以了。如果你像我一样，想用 Linux 进行 exFAT 格式化，请接着往下读。</p>

<h2>四、Linux 的 exFAT 格式化</h2>

<p>Linux 进行硬盘格式化，需要先找到设备路径。</p>

<blockquote><pre><code class="language-bash">
$ sudo fdisk -l
</code></pre></blockquote>

<p>上面命令会列出本机的所有储存设备，移动硬盘一般是<code>/dev/sdX1</code>的形式，比如<code>/dev/sdc1</code>。这里需要了解<code>sdX1</code>的含义，<code>sd</code>表示可移动设备和SATA 设备，<code>X</code>表示设备的序号，依次为 a、b、c 等，最后的<code>1</code>表示这是该设备的第一个分区。</p>

<p>然后，使用下面的命令进行格式化。</p>

<blockquote><pre><code class="language-bash">
$ sudo mkfs.exfat /dev/sdX1
</code></pre></blockquote>

<p>注意，如果你的储存设备只显示为<code>/dev/sdX</code>，没有最后的数字，表明这个设备没有分区。exFAT 只能用来格式化硬盘的一个分区，所以必须先分区，再格式化，下面介绍如何分区。</p>

<h2>五、分区表</h2>

<p>所谓硬盘分区，就是指一块硬盘上面，同时存在多个文件系统。每个文件系统管理的区域，就称为一个分区（partition）。比如，一块 100 GB 的硬盘，可以一半是 NTFS 分区，另一半是 exFAT 分区。</p>

<p>硬盘必须先分区，才能指定每个区的文件系统。分区大小、起始位置、结束位置、文件系统等信息，都储存在分区表里面。</p>

<p>分区表也分成两种格式：MBR 和 GPT。前者是传统格式，兼容性好；后者更现代，功能更强大。一般来说，都推荐使用 GPT。<code>gdisk</code>命令用于分区操作。</p>

<blockquote><pre><code class="language-bash">
$ sudo gdisk /dev/sdX
GPT fdisk (gdisk) version 0.8.8

Partition table scan:
  MBR: not present
  BSD: not present
  APM: not present
  GPT: not present

Creating new GPT entries.

Command (? for help):
</code></pre></blockquote>

<p>上面命令表示对<code>/dev/sdX</code>进行分区。输出结果表明，这个设备还没有分区表。</p>

<p>第一步，<code>o</code>命令表示创建 GPT 分区表。</p>

<blockquote><pre><code class="language-bash">
Command (? for help): o
This option deletes all partitions and creates a new protective MBR.
Proceed? (Y/N): Y
</code></pre></blockquote>

<p>第二步，<code>n</code>命令表示新建一个分区。</p>

<blockquote><pre><code class="language-bash">
Command (? for help): n
Partition number (1-128, default 1):
First sector (34-16326462, default = 2048) or {+-}size{KMGTP}:
Last sector (2048-16326462, default = 16326462) or {+-}size{KMGTP}:
Current type is 'Linux filesystem'
Hex code or GUID (L to show codes, Enter = 8300): 0700
Changed type of partition to 'Microsoft basic data'
</code></pre></blockquote>

<p>上面代码中，分区号（<code>Partition number</code>，默认为<code>1</code>）、起始扇区、结束扇区，都可以接受默认值，直接按回车。这时整个硬盘只建一个分区，占据所有空间。文件系统的类型要设成<code>0700</code>，代表 exFAT。</p>

<p>第三步，<code>w</code>命令表示写入所有变更。</p>

<blockquote><pre><code class="language-bash">
Command (? for help): w

Final checks complete. About to write GPT data. THIS WILL OVERWRITE EXISTING
PARTITIONS!!

Do you want to proceed? (Y/N): Y
OK; writing new GUID partition table (GPT) to /dev/sdX.
Warning: The kernel is still using the old partition table.
The new table will be used at the next reboot.
The operation has completed successfully.
</code></pre></blockquote>

<p>到了这一步，分区表应该已经建立了。然后，使用上一节的命令，建立 exFAT 文件系统。</p>

<blockquote><pre><code class="language-bash">
$ sudo mkfs.exfat /dev/sdX1
mkexfatfs 1.0.1
Creating... done.
Flushing... done.
File system created successfully.
</code></pre></blockquote>

<h2>六、参考链接</h2>

<ul>
<li></li>
<li></li>
<li></li>
</ul>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2018-10-16T17:35:50+08:00">2018年10月16日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>文集：</li>
<li>社交媒体：</li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------
<h1 id="#title_4" >5、文章： Zalando的自治扩展</h1>
Ben Linders, Eric Bowman
[http://www.infoq.com/cn/articles/scaled-autonomy-zalando?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/scaled-autonomy-zalando?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/scaled-autonomy-zalando/zh/smallimage/scaled-autonomy-zalando-S-1538122654146-1539276708783.jpeg"/><p>自治不是你能给予一个团队的东西，它是团队随着时间的推移而习得的东西。它伴随着加倍努力实现目标的责任。在Zalando，创建正确的架构和组织结构可以减少所需的对齐量，并释放出更多的能量，以便在需要对齐的地方进行更彻底的对齐。</p> <i>By Ben Linders, Eric Bowman</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_5" >6、文章： DevOps & SRE 必备技能清单</h1>
Aymen El Amri
[http://www.infoq.com/cn/articles/the-must-know-checklist-for-devops-and-sre?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/the-must-know-checklist-for-devops-and-sre?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/the-must-know-checklist-for-devops-and-sre/zh/smallimage/logo-cote-1539417039947.jpg"/><p>列举了DevOps和SRE的技术基础、必须知道的技能和一些作者的想法。可以用它们作为一个清单来评估自己或其他人，或者为面试DevOps/SRE（Site Reliability Engineers，网站可靠性工程师）工作做准备。</p> <i>By Aymen El Amri</i> <i> Translated by 杨雷</i>
---------------
<h1 id="#title_6" >7、Photoshop Workflows And Shortcuts For Digital Artists</h1>
Yoanna Victorova
[https://www.smashingmagazine.com/2018/10/photoshop-workflows-shortcuts-digital-artists/](https://www.smashingmagazine.com/2018/10/photoshop-workflows-shortcuts-digital-artists/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/10/photoshop-workflows-shortcuts-digital-artists/" />
              <title>Photoshop Workflows And Shortcuts For Digital Artists</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>Photoshop Workflows And Shortcuts For Digital Artists</h1>
                  
                    
                    <address>Yoanna Victorova</address>
                  
                  <time datetime="2018-10-16T15:30:51&#43;02:00" class="op-published">2018-10-16T15:30:51+02:00</time>
                  <time datetime="2018-10-16T13:39:09&#43;00:00" class="op-modified">2018-10-16T13:39:09+00:00</time>
                </header>
                <p>Adobe Photoshop plays a role in almost every digital creator’s life. Photoshop is what many digital artists, photographers, graphic designers, and even some web developers have in common. The tool is so flexible that often you can achieve the same results in several different ways. What sets us all apart is our personal workflows and our preferences on how we use it to achieve the desired outcome.</p>

<p>I use Photoshop every day and shortcuts are a vital part of my workflow. They allow me to save time and to focus better on what I am doing: digital illustration. In this article, I am going to share the Photoshop shortcuts I use frequently &mdash; some of its features that help me be more productive, and a few key parts of my creative process.</p>

<p>To profit the most from this tutorial, some familiarity with Photoshop would be required but no matter if you are a complete beginner or an advanced user, you should be able to follow along because every technique will be explained in detail.</p>

<p>For this article, I've decided to use one of my most famous Photoshop artworks named “Regret”:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b0dab231-ed3c-4af3-a9c3-e3ec42ff167e/1-photoshop-workflows-and-shortcuts-for-digital-artists.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b0dab231-ed3c-4af3-a9c3-e3ec42ff167e/1-photoshop-workflows-and-shortcuts-for-digital-artists.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b0dab231-ed3c-4af3-a9c3-e3ec42ff167e/1-photoshop-workflows-and-shortcuts-for-digital-artists.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b0dab231-ed3c-4af3-a9c3-e3ec42ff167e/1-photoshop-workflows-and-shortcuts-for-digital-artists.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b0dab231-ed3c-4af3-a9c3-e3ec42ff167e/1-photoshop-workflows-and-shortcuts-for-digital-artists.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b0dab231-ed3c-4af3-a9c3-e3ec42ff167e/1-photoshop-workflows-and-shortcuts-for-digital-artists.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b0dab231-ed3c-4af3-a9c3-e3ec42ff167e/1-photoshop-workflows-and-shortcuts-for-digital-artists.png"
			sizes="100vw"
			alt="Picture of the artist writing the article"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Author’s illustration ()
		</figcaption>
	
</figure>


<h4>Table of Contents</h4>

<ol>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
</ol>



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




<h3 id="introduction-to-shortcuts">1. Introduction To Shortcuts: The Path To Boosting Your Productivity</h3>

<p>Every single designer, artist, photographer or web developer has probably once opened Photoshop and has pointed and clicked on an icon to select the Brush tool, the Move tool, and so on. We’ve all been there, but those days are long gone for most of us who use Photoshop every day. Some might still do it today, however, what I would like to talk about before getting into the details, is the importance of shortcuts.</p>

<p>When you think about it, you’re saving perhaps half a second by using a keyboard shortcut instead of moving your mouse (or stylus) over to the <em>Tools</em> bar and selecting the tool you need by clicking on the tool’s little icon. To some that may seem petty, however, do consider that every digital creator does thousands of selections per project and these half-seconds add up to become hours in the end!</p>

<p>Now, before we continue, please note the following:</p>

<ol>
<li><strong>Shortcuts Notation</strong><br />
I use Photoshop on Windows but all of the shortcuts should work the same on Mac OS; the only thing worth mentioning is that the <kbd>Ctrl</kbd> (Control) key on Windows corresponds to the <kbd>Cmd</kbd> (Command) key on the Mac, so I’ll be using <kbd>Ctrl/Cmd</kbd> throughout this tutorial.</li>
<li><strong>Photoshop CS6+</strong><br />
All the features and shortcuts mentioned here should work in Photoshop CS6 and later &mdash; including the latest Photoshop CC 2018.</li>
</ol>

<h3 id ="keyboard-shortcuts-window">2. The Keyboard Shortcuts Window</h3>

<p>To start off, I would like to show you where you can find the  window where you could modify the already existing shortcuts, and learn which key is bound to which feature or tool:</p>

<p>Open Photoshop, go to <em>Edit</em> and select <em>Keyboard Shortcuts</em>. Alternatively, you can access the same from here: <em>Window</em>&nbsp;&rarr; <em>Workspace</em>&nbsp;&rarr; <em>Keyboard Shortcuts & Menus</em>.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2be0fe4c-fee5-4a59-830c-1dacbbc88f17/2-photoshop-workflows-and-shortcuts-for-digital-artists.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2be0fe4c-fee5-4a59-830c-1dacbbc88f17/2-photoshop-workflows-and-shortcuts-for-digital-artists.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2be0fe4c-fee5-4a59-830c-1dacbbc88f17/2-photoshop-workflows-and-shortcuts-for-digital-artists.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2be0fe4c-fee5-4a59-830c-1dacbbc88f17/2-photoshop-workflows-and-shortcuts-for-digital-artists.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2be0fe4c-fee5-4a59-830c-1dacbbc88f17/2-photoshop-workflows-and-shortcuts-for-digital-artists.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2be0fe4c-fee5-4a59-830c-1dacbbc88f17/2-photoshop-workflows-and-shortcuts-for-digital-artists.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2be0fe4c-fee5-4a59-830c-1dacbbc88f17/2-photoshop-workflows-and-shortcuts-for-digital-artists.png"
			sizes="100vw"
			alt="the Edit tab with Keyboard Shortcuts option highlighted"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Photoshop’s edit ()
		</figcaption>
	
</figure>


<p>Now you will be greeted by the <em>Keyboard Shortcuts and Menus</em> window (dialog box), where you can pick a category you would like to check out. There are a ton of options in there, so it could get a bit intimidating at first, but that feeling will pass soon. The main three options (accessible through the <em>Shortcuts for:...</em> dropdown list) are:</p>

<ul>
<li>Application Menus</li>
<li>Panel Menus</li>
<li>Tools</li>
</ul>

<p>Typically the <em>Application Menus</em> will be the first thing you’ll see. These are the shortcuts for the menu options you see on the top of Photoshop’s window (<em>File</em>, <em>Edit</em>, <em>Image</em>, <em>Layer</em>, <em>Type</em>, and so on).</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1f92688a-d6dd-42ff-ac77-58910d165637/3-photoshop-workflows-and-shortcuts-for-digital-artists.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1f92688a-d6dd-42ff-ac77-58910d165637/3-photoshop-workflows-and-shortcuts-for-digital-artists.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1f92688a-d6dd-42ff-ac77-58910d165637/3-photoshop-workflows-and-shortcuts-for-digital-artists.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1f92688a-d6dd-42ff-ac77-58910d165637/3-photoshop-workflows-and-shortcuts-for-digital-artists.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1f92688a-d6dd-42ff-ac77-58910d165637/3-photoshop-workflows-and-shortcuts-for-digital-artists.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1f92688a-d6dd-42ff-ac77-58910d165637/3-photoshop-workflows-and-shortcuts-for-digital-artists.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1f92688a-d6dd-42ff-ac77-58910d165637/3-photoshop-workflows-and-shortcuts-for-digital-artists.png"
			sizes="100vw"
			alt=" Keyboard Shortcuts and Menus option open, displaying the shortcuts for the Applications menu"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Applications menu ()
		</figcaption>
	
</figure>


<p>So for example if you’re using the <em>Brightness/Contrast</em> option often, instead of having to click on <em>Image</em> (in the menu), then <em>Adjustments</em> and finally find and click on <em>Brightness/Contrast</em> item, you can simply assign a key combination and <em>Brightness/Contrast</em> will show right up after you press the keys assigned.</p>

<p>The second section, <em>Panel Menus</em>, is an interesting one as well, especially in its Layers portion. You get to see several options that could be of use to you depending on the type of work you need to do. That’s where the standard New Layer shortcut lies (<kbd>Ctrl/Cmd</kbd> + <kbd>Shift</kbd> + <kbd>N</kbd>) but also you can set up a shortcut for <em>Delete Hidden Layers</em>. Deleting unnecessary layers helps in lowering the size of the Photoshop file and helps improving performance because your computer will not have to cache in on those extra layers that you’re actually not using.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4036bcf8-4342-41be-a581-2a831149688d/4-photoshop-workflows-and-shortcuts-for-digital-artists.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4036bcf8-4342-41be-a581-2a831149688d/4-photoshop-workflows-and-shortcuts-for-digital-artists.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4036bcf8-4342-41be-a581-2a831149688d/4-photoshop-workflows-and-shortcuts-for-digital-artists.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4036bcf8-4342-41be-a581-2a831149688d/4-photoshop-workflows-and-shortcuts-for-digital-artists.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4036bcf8-4342-41be-a581-2a831149688d/4-photoshop-workflows-and-shortcuts-for-digital-artists.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4036bcf8-4342-41be-a581-2a831149688d/4-photoshop-workflows-and-shortcuts-for-digital-artists.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4036bcf8-4342-41be-a581-2a831149688d/4-photoshop-workflows-and-shortcuts-for-digital-artists.png"
			sizes="100vw"
			alt="Keyboard Shortcuts and Menus option open, displaying the shortcuts for the Panel Menus"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Panel menu ()
		</figcaption>
	
</figure>


<p>The third section is <strong>Tools</strong> where you can see the shortcuts assigned to all the tools found in the left panel of Photoshop.</p>

<p><strong>Pro Tip:</strong> <em>To cycle between any of the tools that have sub-tools (example: the <em>Eraser</em> tool has a <em>Background Eraser</em> and a <em>Magic Eraser</em>) you just need to hold your</em> <kbd>Shift</kbd> <em>key and the appropriate shortcut button. In case of the <em>Eraser</em> example, press</em> <kbd>Shift</kbd> + <kbd>E</kbd> <em>a few times until you reach the desired sub-tool.</em></p>

<p>One last thing I would like to mention before wrapping up this section is that the <em>Keyboard Shortcuts and Menus</em> allows you to set up different <em>Profiles</em> (Photoshop calls them “sets” but I think that “profiles” better suits the purpose), so that if you don’t really want to mess with the Photoshop Defaults one, you can simply create a new personalized profile. It’s worth mentioning that when you create a new Profile, you get the Default set of Photoshop Shortcuts in it until you start modifying them.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b8848f87-9be8-434c-8e45-e636548ee01c/5-photoshop-workflows-and-shortcuts-for-digital-artists.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b8848f87-9be8-434c-8e45-e636548ee01c/5-photoshop-workflows-and-shortcuts-for-digital-artists.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b8848f87-9be8-434c-8e45-e636548ee01c/5-photoshop-workflows-and-shortcuts-for-digital-artists.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b8848f87-9be8-434c-8e45-e636548ee01c/5-photoshop-workflows-and-shortcuts-for-digital-artists.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b8848f87-9be8-434c-8e45-e636548ee01c/5-photoshop-workflows-and-shortcuts-for-digital-artists.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b8848f87-9be8-434c-8e45-e636548ee01c/5-photoshop-workflows-and-shortcuts-for-digital-artists.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b8848f87-9be8-434c-8e45-e636548ee01c/5-photoshop-workflows-and-shortcuts-for-digital-artists.png"
			sizes="100vw"
			alt="Keyboard Shortcuts and Menus option showing the Profiles section"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Keyboard shortcuts and menus profile section ()
		</figcaption>
	
</figure>


<p>The <em>Keyboard Shortcuts</em> menu can take a bit of time to get around to, however, if you invest the time in the beginning (best if you do it in your own time rather than during a project), you will benefit later.</p>

<h4>Focusing On The Shortcuts On The Left Side Of Your Keyboard</h4>

<p>After people acknowledged the usefulness of using shortcuts, eventually they agreed that time is being wasted moving your hand from one side of the keyboard to the opposite one. Sounds a bit petty again, however, remember those half-seconds? They still add up, but this time it can even fatigue your arm if you’re constantly switching tools and have to move your arm around. So this probably led to Adobe adding a few more shortcut features focused on the left side of the keyboard.</p>

<p>Now let me show you the shortcuts that I most often use (and why).</p>

<div class="sponsors__wide-place"></div>




<h3 id="brush-size">3. How To Increase And Decrease The Brush Size</h3>

<p>In order to increase or decrease the size of your brush, you need to:</p>

<ol>
    <li>Click and hold the <kbd>Alt</kbd> key. (On the Mac this would be the <kbd>Ctrl</kbd> and <kbd>Alt</kbd> keys),</li>
    <li>Click and hold the right mouse button,</li>
    <li>Then drag horizontally from left to right to increase, and from right to left to decrease the size.</li>
</ol>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4fdc499a-1609-447b-8a50-ff7dd9d6037b/6-photoshop-workflows-and-shortcuts-for-digital-artists.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4fdc499a-1609-447b-8a50-ff7dd9d6037b/6-photoshop-workflows-and-shortcuts-for-digital-artists.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4fdc499a-1609-447b-8a50-ff7dd9d6037b/6-photoshop-workflows-and-shortcuts-for-digital-artists.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4fdc499a-1609-447b-8a50-ff7dd9d6037b/6-photoshop-workflows-and-shortcuts-for-digital-artists.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4fdc499a-1609-447b-8a50-ff7dd9d6037b/6-photoshop-workflows-and-shortcuts-for-digital-artists.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4fdc499a-1609-447b-8a50-ff7dd9d6037b/6-photoshop-workflows-and-shortcuts-for-digital-artists.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4fdc499a-1609-447b-8a50-ff7dd9d6037b/6-photoshop-workflows-and-shortcuts-for-digital-artists.png"
			sizes="100vw"
			alt="Red circle displaying the brush size increase via mouse drag"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Brush size increase preview ()
		</figcaption>
	
</figure>


<p>The moment I learned about this shortcut, I literally couldn’t stop using it!</p>

<p>If you’re a digital artist, I believe you will particularly love it as well. Sketching, painting, erasing, just about everything you need to do with a brush becomes a whole lot easier and fluent because you wouldn’t need to reach for the all too familiar <kbd>[</kbd> and <kbd>]</kbd> keys which are the default ones for increasing and decreasing the brush size. Going for those keys can disrupt your workflow, especially if you need to take your eyes off your project or put the stylus aside.</p>

<h3 id="brush-softness">4. How To Increase And Decrease The Brush Softness</h3>

<p>It’s actually the same key combination but with a slight twist: increasing and decreasing the softness of your Brush will work only for Photoshop’s default Round brushes. Unfortunately, if you have any custom made brushes that have a custom form, this wouldn’t work for those.</p>

<ol>
    <li>Click and hold the <kbd>Alt</kbd> key. (On the Mac this would be <kbd>Ctrl</kbd> and <kbd>Alt</kbd> keys),</li>
    <li>Click and hold the right mouse button,</li>
    <li>Then drag upwards to harden the edge of your brush and drag downwards to make it softer.</li>
</ol>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c3ce503a-7dbb-44c7-8f8a-c0692eb306ca/7-photoshop-workflows-and-shortcuts-for-digital-artists.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c3ce503a-7dbb-44c7-8f8a-c0692eb306ca/7-photoshop-workflows-and-shortcuts-for-digital-artists.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c3ce503a-7dbb-44c7-8f8a-c0692eb306ca/7-photoshop-workflows-and-shortcuts-for-digital-artists.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c3ce503a-7dbb-44c7-8f8a-c0692eb306ca/7-photoshop-workflows-and-shortcuts-for-digital-artists.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c3ce503a-7dbb-44c7-8f8a-c0692eb306ca/7-photoshop-workflows-and-shortcuts-for-digital-artists.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c3ce503a-7dbb-44c7-8f8a-c0692eb306ca/7-photoshop-workflows-and-shortcuts-for-digital-artists.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c3ce503a-7dbb-44c7-8f8a-c0692eb306ca/7-photoshop-workflows-and-shortcuts-for-digital-artists.png"
			sizes="100vw"
			alt="Red circle displaying the brush softness increase via mouse drag"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Brush softness increase preview ()
		</figcaption>
	
</figure>


<p>Again, this shortcut doesn’t work for custom shaped brushes, although it would have been a really nice feature to have. Hopefully, we’ll be able to see that in a future update to Photoshop.</p>

<h3 id="hud-color-picker">5. Quick Color Picker (HUD Color Picker)</h3>

<p>You may or may not be aware that Photoshop offers a quick color picker (HUD Color Picker). And no, this is not the color picker that is located in the <strong>Tools</strong> section.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ee31abe5-a528-4fba-84b4-75511011203e/8-photoshop-workflows-and-shortcuts-for-digital-artists.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ee31abe5-a528-4fba-84b4-75511011203e/8-photoshop-workflows-and-shortcuts-for-digital-artists.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ee31abe5-a528-4fba-84b4-75511011203e/8-photoshop-workflows-and-shortcuts-for-digital-artists.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ee31abe5-a528-4fba-84b4-75511011203e/8-photoshop-workflows-and-shortcuts-for-digital-artists.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ee31abe5-a528-4fba-84b4-75511011203e/8-photoshop-workflows-and-shortcuts-for-digital-artists.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ee31abe5-a528-4fba-84b4-75511011203e/8-photoshop-workflows-and-shortcuts-for-digital-artists.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ee31abe5-a528-4fba-84b4-75511011203e/8-photoshop-workflows-and-shortcuts-for-digital-artists.png"
			sizes="100vw"
			alt="Photoshop’s Quick color picker"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Quick color picker ()
		</figcaption>
	
</figure>


<p>I am referring to what Adobe calls “HUD Color Picker” that pops up right where your cursor is located on the canvas.</p>

<p>This so-called HUD Color Picker is a built-in version and I believe it’s been around since at least Photoshop CS6 (which was released back in 2012). If you’re learning about this now, probably you’re as surprised as I was when I first came across it a few months ago. Yes, it took me a while to get used to, too! Well, to be fair, I do also have some reservations about this color picker, but I’ll get to them in a second.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/91fa551a-7120-4533-942f-e2f81addc6e3/9-photoshop-workflows-and-shortcuts-for-digital-artists.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/91fa551a-7120-4533-942f-e2f81addc6e3/9-photoshop-workflows-and-shortcuts-for-digital-artists.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/91fa551a-7120-4533-942f-e2f81addc6e3/9-photoshop-workflows-and-shortcuts-for-digital-artists.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/91fa551a-7120-4533-942f-e2f81addc6e3/9-photoshop-workflows-and-shortcuts-for-digital-artists.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/91fa551a-7120-4533-942f-e2f81addc6e3/9-photoshop-workflows-and-shortcuts-for-digital-artists.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/91fa551a-7120-4533-942f-e2f81addc6e3/9-photoshop-workflows-and-shortcuts-for-digital-artists.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/91fa551a-7120-4533-942f-e2f81addc6e3/9-photoshop-workflows-and-shortcuts-for-digital-artists.png"
			sizes="100vw"
			alt="Photoshop’s HUD color picker"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Photoshop’s HUD color picker ()
		</figcaption>
	
</figure>


<p>Here’s how to pull up the HUD Color Picker:</p>

<h5>On Windows</h5>

<ol>
<li>Click and hold <kbd>Alt</kbd> + <kbd>Shift</kbd>,</li>
<li>Click and hold the right mouse button.</li>
</ol>

<h5>On Mac</h5>

<ol>
<li>Click and hold <kbd>Ctrl ⌃</kbd> + <kbd>Alt ⌥</kbd> + <kbd>Cmd ⌘</kbd>,</li>
<li>Click and hold the right mouse button.</li>
</ol>

<p>If you’ve followed the key combinations above, you should see this colorful square. However, you’ve probably noticed that it’s a bit awkward to work with it. For example, you need to continue holding all of the keys, and while you do that, you need to hover over to the right rectangle to pick a color gamut and then hover back to the square to pick the shade. With all of the hovering that’s going on, it’s somewhat easy to miss the color that you’ve actually set your heart to pick, which could get a little annoying.</p>

<p>Nevertheless, I do believe that with a little practice you will be able to master the <em>Quick Color Picker</em> and get your desired results. If you’re not too keen on using that built-in version, there are always third-party extensions that you can strap to your Photoshop, for example,  (works with PS CS4, CS5, CS6).</p>

<div class="sponsors__wide-place"></div>




<h3 id="working-with-layers">6. Working With Layers</h3>

<p>One of the advantages of working digitally is undisputedly the ability to work with layers. They are quite versatile, and there’s a lot of things that you could do with them.  You could say that one could write a book just on <em>Layers</em> alone. However, I’m going to do the next best thing, and that would be to share with you <strong>the options I most commonly use when working on my projects</strong>.</p>

<p>As you may have guessed, the Layer section is a pretty important one for any type of digital creative. In this section, I’m going to share the simpler but very useful shortcuts that could be some real lifesavers.</p>

<h4>Clipping Mask Layer</h4>

<p>A <em>Clipping Mask Layer</em> is what I most often use when I’m drawing. For those of you who do not know what that is, it’s basically a layer which you clip on to the layer below. The layer below defines what’s visible on the clipped on layer.</p>

<p>For example, let’s say that you have a circle on the base layer and then you add a <em>Clipping Mask Layer</em> to that circle. When you start drawing on your <em>Clipping Mask Layer</em>, you will be restricted only to the shapes in the <em>Base Layer</em>.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f0013b85-427a-443e-b1c9-9e1f54931662/10-photoshop-workflows-and-shortcuts-for-digital-artists.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f0013b85-427a-443e-b1c9-9e1f54931662/10-photoshop-workflows-and-shortcuts-for-digital-artists.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f0013b85-427a-443e-b1c9-9e1f54931662/10-photoshop-workflows-and-shortcuts-for-digital-artists.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f0013b85-427a-443e-b1c9-9e1f54931662/10-photoshop-workflows-and-shortcuts-for-digital-artists.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f0013b85-427a-443e-b1c9-9e1f54931662/10-photoshop-workflows-and-shortcuts-for-digital-artists.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f0013b85-427a-443e-b1c9-9e1f54931662/10-photoshop-workflows-and-shortcuts-for-digital-artists.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f0013b85-427a-443e-b1c9-9e1f54931662/10-photoshop-workflows-and-shortcuts-for-digital-artists.png"
			sizes="100vw"
			alt="Red circle shape that’s going to be used for a clipping mask"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Red circle shape on transparent background ()
		</figcaption>
	
</figure>












<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9807d385-6cb5-4420-9bd3-21b32b1879ab/11-photoshop-workflows-and-shortcuts-for-digital-artists.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9807d385-6cb5-4420-9bd3-21b32b1879ab/11-photoshop-workflows-and-shortcuts-for-digital-artists.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9807d385-6cb5-4420-9bd3-21b32b1879ab/11-photoshop-workflows-and-shortcuts-for-digital-artists.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9807d385-6cb5-4420-9bd3-21b32b1879ab/11-photoshop-workflows-and-shortcuts-for-digital-artists.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9807d385-6cb5-4420-9bd3-21b32b1879ab/11-photoshop-workflows-and-shortcuts-for-digital-artists.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9807d385-6cb5-4420-9bd3-21b32b1879ab/11-photoshop-workflows-and-shortcuts-for-digital-artists.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9807d385-6cb5-4420-9bd3-21b32b1879ab/11-photoshop-workflows-and-shortcuts-for-digital-artists.png"
			sizes="100vw"
			alt="Drawly’s artwork inserted into circle shape"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Drawing inserted into circle shape ()
		</figcaption>
	
</figure>


<p>Take notice of the layers on the right side of the screen. Layer 0 is the <em>Clipping Mask Layer</em> of the <em>Base Layer &mdash; Layer 1</em>.</p>

<p>This option allows you to really easily create frames and the best part is that they’re non-destructive. The more shapes you add (in this case it’s <em>Layer 1</em>), the more visible parts of the image can be seen.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a4042055-f50f-4ed6-b93a-dfaffa788a17/12-photoshop-workflows-and-shortcuts-for-digital-artists.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a4042055-f50f-4ed6-b93a-dfaffa788a17/12-photoshop-workflows-and-shortcuts-for-digital-artists.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a4042055-f50f-4ed6-b93a-dfaffa788a17/12-photoshop-workflows-and-shortcuts-for-digital-artists.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a4042055-f50f-4ed6-b93a-dfaffa788a17/12-photoshop-workflows-and-shortcuts-for-digital-artists.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a4042055-f50f-4ed6-b93a-dfaffa788a17/12-photoshop-workflows-and-shortcuts-for-digital-artists.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a4042055-f50f-4ed6-b93a-dfaffa788a17/12-photoshop-workflows-and-shortcuts-for-digital-artists.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a4042055-f50f-4ed6-b93a-dfaffa788a17/12-photoshop-workflows-and-shortcuts-for-digital-artists.png"
			sizes="100vw"
			alt="Drawly’s artwork added into various shapes as a clipping mask"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Drawly’s artwork added into various shapes as a clipping mask ()
		</figcaption>
	
</figure>


<p>The most common use for <em>Clipping Mask Layers</em> in digital art/painting is to add shadows and highlights to a base color. For example, let’s say that you’ve completed your character’s line-art and you’ve added their base skin tone. You can use <em>Clipping Mask Layers</em> to add non-destructive shadows and highlights.</p>

<p><strong>Note</strong>: <em>I’m using the term “non-destructive” because you cannot erase away something from the base layers &mdash; they will be safe and sound.)</em></p>

<p>So, how do you create those <em>Clipping Mask Layers</em>? Well, each one starts off as a regular “Layer”.</p>

<p>To create a regular Layer, you can use this shortcut:</p>

<table class="tablesaw break-out" data-tablesaw-mode="swipe" data-tablesaw-minimap>
    <thead>
        <tr>
            <th data-tablesaw-priority="persist">Action</th>
            <th>Keyboard Shortcut</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Creates a new regular Layer</td>
            <td><kbd>Ctrl/Cmd</kbd> + <kbd>Shift</kbd> + <kbd>N</kbd></td>
        </tr>
        <tr>
            <td>Makes the newly created Layer into a Clipping Mask to the Layer below it</td>
            <td><kbd>Ctrl/Cmd</kbd> + <kbd>Alt</kbd> + <kbd>G</kbd></td>
        </tr>
    </tbody>
</table>

<p>An alternative way to make a regular layer into a <em>Clipping Mask</em> is to press and hold the <kbd>Alt</kbd> key, and click between the two Layers. The upper layer will then become the <em>Clipping Mask</em> of the layer below.</p>

<h4>Selecting All Layers</h4>

<p>Every once in a while, you may want to select all of the layers, and group them together so that you can continue building on top of them or a number of other reasons. Typically, what I used to do is simply hold the <kbd>Ctrl/Cmd</kbd> key and then start clicking away at all of the layers. Needless to say, that was a bit time-consuming, especially if I’m working on a big project. So here’s a better way:</p>

<p>What you would need to do is simply press: <kbd>Ctrl/Cmd</kbd> + <kbd>Alt</kbd> + <kbd>A</kbd>.</p>

<p>Now that should’ve selected all of your layers and you will be able to do anything you want with them.</p>

<h4>Flattening Visible Layers</h4>

<p><strong>Clipping Mask Layers</strong> may be totally awesome, however, they don’t always work well if you want to modify something in the general image you’re doing. Sometimes you just need everything (e.g. base color, highlights and shadows) to stop being on different layers and just be combined into one. Sometimes you just need to merge all currently visible layers into one, in a non-destructive way.</p>

<p>Here’s how:</p>

<p>Press and hold <kbd>Ctrl/Cmd</kbd> + <kbd>Alt</kbd> + <kbd>Shift</kbd> + <kbd>E</kbd>.</p>

<p><em>Et voilà</em>! Now you should be seeing an extra layer on the top that has all other visible layers in it. The beauty of this shortcut is that you still have your other layers below &mdash; untouched and safe. If you mess up something with the newly created layer, you can still bring things back to the way they were before and start afresh.</p>

<h4>Copying Multiple Layers</h4>

<p>Every now and then we’re faced with the need to copy stuff from multiple layers. Typically what most people do is duplicate the two given layers they need, merge them and then start erasing away the unnecessary parts of the image.</p>

<p>What you need to do instead is to make a selection and then press:</p>

<p><kbd>Ctrl/Cmd</kbd> + <kbd>Shift</kbd> + <kbd>C</kbd></p>

<p>Here’s an example:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0b4c0e81-8dba-415b-87ab-beffe3a2ab37/13-photoshop-workflows-and-shortcuts-for-digital-artists.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0b4c0e81-8dba-415b-87ab-beffe3a2ab37/13-photoshop-workflows-and-shortcuts-for-digital-artists.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0b4c0e81-8dba-415b-87ab-beffe3a2ab37/13-photoshop-workflows-and-shortcuts-for-digital-artists.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0b4c0e81-8dba-415b-87ab-beffe3a2ab37/13-photoshop-workflows-and-shortcuts-for-digital-artists.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0b4c0e81-8dba-415b-87ab-beffe3a2ab37/13-photoshop-workflows-and-shortcuts-for-digital-artists.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0b4c0e81-8dba-415b-87ab-beffe3a2ab37/13-photoshop-workflows-and-shortcuts-for-digital-artists.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0b4c0e81-8dba-415b-87ab-beffe3a2ab37/13-photoshop-workflows-and-shortcuts-for-digital-artists.png"
			sizes="100vw"
			alt="Three different colored circles on a transparent background"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Three different colored circles ()
		</figcaption>
	
</figure>


<p>As you can see, each color dot is on a separate layer. Let’s say that we need to copy a straight rectangle through the center of the dots and copy it on a layer at the top.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b175010d-5ce5-4643-82fc-6b2f5679f796/14-photoshop-workflows-and-shortcuts-for-digital-artists.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b175010d-5ce5-4643-82fc-6b2f5679f796/14-photoshop-workflows-and-shortcuts-for-digital-artists.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b175010d-5ce5-4643-82fc-6b2f5679f796/14-photoshop-workflows-and-shortcuts-for-digital-artists.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b175010d-5ce5-4643-82fc-6b2f5679f796/14-photoshop-workflows-and-shortcuts-for-digital-artists.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b175010d-5ce5-4643-82fc-6b2f5679f796/14-photoshop-workflows-and-shortcuts-for-digital-artists.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b175010d-5ce5-4643-82fc-6b2f5679f796/14-photoshop-workflows-and-shortcuts-for-digital-artists.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b175010d-5ce5-4643-82fc-6b2f5679f796/14-photoshop-workflows-and-shortcuts-for-digital-artists.png"
			sizes="100vw"
			alt="Three different colored circles with a selection box inside them"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Three different colored circles with a selection box inside them ()
		</figcaption>
	
</figure>


<p>We’ve made a selection and once you press <kbd>Ctrl/Cmd</kbd> + <kbd>Shift</kbd> + <kbd>C</kbd>, Photoshop will copy everything you have in your selection to the clipboard. Then all you have to do is simply paste (<kbd>Ctrl/Cmd</kbd> + <kbd>V</kbd>) anywhere, and a new layer will appear on the top of the page.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/793350a0-4d72-4d68-ae15-47bfa923f382/15-photoshop-workflows-and-shortcuts-for-digital-artists.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/793350a0-4d72-4d68-ae15-47bfa923f382/15-photoshop-workflows-and-shortcuts-for-digital-artists.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/793350a0-4d72-4d68-ae15-47bfa923f382/15-photoshop-workflows-and-shortcuts-for-digital-artists.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/793350a0-4d72-4d68-ae15-47bfa923f382/15-photoshop-workflows-and-shortcuts-for-digital-artists.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/793350a0-4d72-4d68-ae15-47bfa923f382/15-photoshop-workflows-and-shortcuts-for-digital-artists.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/793350a0-4d72-4d68-ae15-47bfa923f382/15-photoshop-workflows-and-shortcuts-for-digital-artists.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/793350a0-4d72-4d68-ae15-47bfa923f382/15-photoshop-workflows-and-shortcuts-for-digital-artists.png"
			sizes="100vw"
			alt="Selection box with the three different colors from the circles"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Selection box with three different colors ()
		</figcaption>
	
</figure>


<p>This shortcut can come really handy especially when you’re working with multiple layers, and you need just a portion of the image to be together in a single layer.</p>

<h3 id ="curves">7. Working With Curves</h3>

<p>In this section of the article, I would like to cover the importance of values as well as <em>Curves</em> which are generally a big topic to cover.</p>

<p>Starting off with the shortcut: <kbd>Ctrl/Cmd</kbd> + <kbd>M</kbd>.</p>

<p>Pretty simple, right? The best things in life are (almost) always simple! However, don’t let this talk about simplicity fool you, the <em>Curves</em> setting is one of the most powerful tools you have in Photoshop. Especially when it comes to tweaking brightness, contrast, colors, tones, and so on.</p>

<p>Now some of you may be feeling a bit of intimidated by the previous sentence: colors, tones, contrast,... say what now? Don’t worry, because the <em>Curves</em> tool is pretty simple to understand and it will do marvelous things for you. Let’s dig into the details.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e3d7f947-b27d-468a-a921-9e4a24c3fd33/16-photoshop-workflows-and-shortcuts-for-digital-artists.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e3d7f947-b27d-468a-a921-9e4a24c3fd33/16-photoshop-workflows-and-shortcuts-for-digital-artists.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e3d7f947-b27d-468a-a921-9e4a24c3fd33/16-photoshop-workflows-and-shortcuts-for-digital-artists.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e3d7f947-b27d-468a-a921-9e4a24c3fd33/16-photoshop-workflows-and-shortcuts-for-digital-artists.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e3d7f947-b27d-468a-a921-9e4a24c3fd33/16-photoshop-workflows-and-shortcuts-for-digital-artists.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e3d7f947-b27d-468a-a921-9e4a24c3fd33/16-photoshop-workflows-and-shortcuts-for-digital-artists.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e3d7f947-b27d-468a-a921-9e4a24c3fd33/16-photoshop-workflows-and-shortcuts-for-digital-artists.png"
			sizes="100vw"
			alt=" Curves histogram"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Curves histogram highlighted in red square ()
		</figcaption>
	
</figure>


<p>This is what the <em>Curves</em> tool basically looks like. As you can see, there’s a moderate amount of options available. What we’re interested in, however, is the area I’ve captured inside the red square. It is actually a simple <em>Histogram</em> with a diagonal line across. The <em>Histogram</em>’s purpose is to show the values of the given image (or painting), left being the darkest points and right being the lightest ones.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/eda3ca8b-54a8-4dc0-8494-7b8e6c8c3543/17-photoshop-workflows-and-shortcuts-for-digital-artists.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/eda3ca8b-54a8-4dc0-8494-7b8e6c8c3543/17-photoshop-workflows-and-shortcuts-for-digital-artists.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/eda3ca8b-54a8-4dc0-8494-7b8e6c8c3543/17-photoshop-workflows-and-shortcuts-for-digital-artists.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/eda3ca8b-54a8-4dc0-8494-7b8e6c8c3543/17-photoshop-workflows-and-shortcuts-for-digital-artists.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/eda3ca8b-54a8-4dc0-8494-7b8e6c8c3543/17-photoshop-workflows-and-shortcuts-for-digital-artists.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/eda3ca8b-54a8-4dc0-8494-7b8e6c8c3543/17-photoshop-workflows-and-shortcuts-for-digital-artists.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/eda3ca8b-54a8-4dc0-8494-7b8e6c8c3543/17-photoshop-workflows-and-shortcuts-for-digital-artists.png"
			sizes="100vw"
			alt="Curves histogram with one anchor point added"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Curves histogram with one anchor point added ()
		</figcaption>
	
</figure>












<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/213ad61e-b010-49af-b75f-6e16636ab5ad/18-photoshop-workflows-and-shortcuts-for-digital-artists.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/213ad61e-b010-49af-b75f-6e16636ab5ad/18-photoshop-workflows-and-shortcuts-for-digital-artists.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/213ad61e-b010-49af-b75f-6e16636ab5ad/18-photoshop-workflows-and-shortcuts-for-digital-artists.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/213ad61e-b010-49af-b75f-6e16636ab5ad/18-photoshop-workflows-and-shortcuts-for-digital-artists.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/213ad61e-b010-49af-b75f-6e16636ab5ad/18-photoshop-workflows-and-shortcuts-for-digital-artists.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/213ad61e-b010-49af-b75f-6e16636ab5ad/18-photoshop-workflows-and-shortcuts-for-digital-artists.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/213ad61e-b010-49af-b75f-6e16636ab5ad/18-photoshop-workflows-and-shortcuts-for-digital-artists.png"
			sizes="100vw"
			alt="Curves histogram with two anchor points added"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Curves histogram with two anchor points added ()
		</figcaption>
	
</figure>


<p>Using the mouse, we can put points on the diagonal line and drag it up and down. We typically decide what we want to darken or lighten. If, for example, we want to have the light parts of our image be just a bit darker, we need to click somewhere on the right side and drag down (just like in the first image).</p>

<p>Here’s an example. First, take a look at the normal image:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e2b7eb98-206c-475e-b1a7-7061e9faa79f/19-1-photoshop-workflows-and-shortcuts-for-digital-artists.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e2b7eb98-206c-475e-b1a7-7061e9faa79f/19-1-photoshop-workflows-and-shortcuts-for-digital-artists.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e2b7eb98-206c-475e-b1a7-7061e9faa79f/19-1-photoshop-workflows-and-shortcuts-for-digital-artists.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e2b7eb98-206c-475e-b1a7-7061e9faa79f/19-1-photoshop-workflows-and-shortcuts-for-digital-artists.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e2b7eb98-206c-475e-b1a7-7061e9faa79f/19-1-photoshop-workflows-and-shortcuts-for-digital-artists.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e2b7eb98-206c-475e-b1a7-7061e9faa79f/19-1-photoshop-workflows-and-shortcuts-for-digital-artists.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e2b7eb98-206c-475e-b1a7-7061e9faa79f/19-1-photoshop-workflows-and-shortcuts-for-digital-artists.png"
			sizes="100vw"
			alt="Drawly’s artwork, original colors and values"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Drawly’s artwork, original colors and values. ()
		</figcaption>
	
</figure>


<p>Now, using <strong>Curves</strong> with the light parts toned down:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a1cd6cb2-63f8-4e67-ad05-fddb468fc1ce/19-2-photoshop-workflows-and-shortcuts-for-digital-artists.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a1cd6cb2-63f8-4e67-ad05-fddb468fc1ce/19-2-photoshop-workflows-and-shortcuts-for-digital-artists.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a1cd6cb2-63f8-4e67-ad05-fddb468fc1ce/19-2-photoshop-workflows-and-shortcuts-for-digital-artists.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a1cd6cb2-63f8-4e67-ad05-fddb468fc1ce/19-2-photoshop-workflows-and-shortcuts-for-digital-artists.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a1cd6cb2-63f8-4e67-ad05-fddb468fc1ce/19-2-photoshop-workflows-and-shortcuts-for-digital-artists.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a1cd6cb2-63f8-4e67-ad05-fddb468fc1ce/19-2-photoshop-workflows-and-shortcuts-for-digital-artists.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a1cd6cb2-63f8-4e67-ad05-fddb468fc1ce/19-2-photoshop-workflows-and-shortcuts-for-digital-artists.png"
			sizes="100vw"
			alt="Curves histogram with one anchor point"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Curves histogram with one anchor point ()
		</figcaption>
	
</figure>


<p>AIn addition, just for demonstration purposes, here’s what would happen if we have the lighter parts darkened and the darker parts lightened:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cb952895-e952-43e4-b45e-4e8004ffc7fb/19-photoshop-workflows-and-shortcuts-for-digital-artists.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cb952895-e952-43e4-b45e-4e8004ffc7fb/19-photoshop-workflows-and-shortcuts-for-digital-artists.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cb952895-e952-43e4-b45e-4e8004ffc7fb/19-photoshop-workflows-and-shortcuts-for-digital-artists.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cb952895-e952-43e4-b45e-4e8004ffc7fb/19-photoshop-workflows-and-shortcuts-for-digital-artists.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cb952895-e952-43e4-b45e-4e8004ffc7fb/19-photoshop-workflows-and-shortcuts-for-digital-artists.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cb952895-e952-43e4-b45e-4e8004ffc7fb/19-photoshop-workflows-and-shortcuts-for-digital-artists.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/cb952895-e952-43e4-b45e-4e8004ffc7fb/19-photoshop-workflows-and-shortcuts-for-digital-artists.png"
			sizes="100vw"
			alt="Curves histogram with two anchor points making the ‘S’ shape"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Curves histogram with two anchor points making the ‘S’ shape ()
		</figcaption>
	
</figure>


<p>You see, basically the linework is the darkest part, which stayed and the other darks have been lightened to a grayish type of value.</p>

<p>Now let me quickly elaborate on values and why they matter: by “values,” especially in the art world, we’re referring to the amount of lightness or darkness in a drawing (painting). With values, we create depth in our painting which on its part helps with creating the illusion which element is closer to the viewer and which one is in the distance (further back).</p>

<h3 id="actions-recording-everything-you-need">8. Actions: Recording Everything You Need For Your Project</h3>

<p>Every so often we all need to deal with repetitive processes which could range from adding a filter over our image to creating certain types of layers with blending modes. Does this sound familiar? If so, keep reading.</p>

<p>Did you know that Photoshop supports programming languages such as JavaScript, AppleScript, and VBScript to automate certain processes? I didn’t, as programming has never been my cup of tea. The good thing is that instead, I came across the <em>Actions</em> panel, which offers a lot of functionality and options for automating some repetitive tasks and workflows. In my opinion, this is the best automation tool that Photoshop has to offer if you don’t know how to code.</p>

<p>The <em>Actions</em> panel basically can record every process you’re doing (e.g. adding a layer, cropping the image, changing its hue, and so on); then you can assign a function key to this process and easily re-use it later at any time.</p>

<p>By using the <em>Actions</em> panel, you can capture just about anything that you do in Photoshop and then save it as a process.</p>

<p>Let me give you an example. Let’s say that you want to automate the process of <em>Create a new Layer</em>, set it as a <em>Clipping Mask</em>, and then set its blending mode to <em>Multiply</em> (or anything else). You can record this whole process which would then be available to you for re-use by the press of a button.</p>

<p>Here’s how it works:</p>

<p>Pressing <kbd>Alt</kbd> + <kbd>F9</kbd> will open this panel:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d64d5e9e-39ed-4f5b-96db-29d5ef7a69ba/20-photoshop-workflows-and-shortcuts-for-digital-artists.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dc31ef25-5fbc-49ed-8dec-2909800b1ea9/20-photoshop-workflows-shortcuts-digital-artists.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dc31ef25-5fbc-49ed-8dec-2909800b1ea9/20-photoshop-workflows-shortcuts-digital-artists.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dc31ef25-5fbc-49ed-8dec-2909800b1ea9/20-photoshop-workflows-shortcuts-digital-artists.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dc31ef25-5fbc-49ed-8dec-2909800b1ea9/20-photoshop-workflows-shortcuts-digital-artists.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dc31ef25-5fbc-49ed-8dec-2909800b1ea9/20-photoshop-workflows-shortcuts-digital-artists.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dc31ef25-5fbc-49ed-8dec-2909800b1ea9/20-photoshop-workflows-shortcuts-digital-artists.png"
			sizes="70vw"
			alt="The actions panel displaying all the default options"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The actions panel displaying all the default options ()
		</figcaption>
	
</figure>


<p>As you can probably see, there are some default (pre-recorded) processes on there. What we’re interested in, however, is creating our own action, which is done by clicking on the “Create new action” icon.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2b35bc8b-da52-424a-9506-e709d79a26c0/21-photoshop-workflows-and-shortcuts-for-digital-artists.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/44cc056f-fbca-40b8-8e21-cfd8228b6d93/21-photoshop-workflows-shortcuts-digital-artists.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/44cc056f-fbca-40b8-8e21-cfd8228b6d93/21-photoshop-workflows-shortcuts-digital-artists.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/44cc056f-fbca-40b8-8e21-cfd8228b6d93/21-photoshop-workflows-shortcuts-digital-artists.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/44cc056f-fbca-40b8-8e21-cfd8228b6d93/21-photoshop-workflows-shortcuts-digital-artists.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/44cc056f-fbca-40b8-8e21-cfd8228b6d93/21-photoshop-workflows-shortcuts-digital-artists.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/44cc056f-fbca-40b8-8e21-cfd8228b6d93/21-photoshop-workflows-shortcuts-digital-artists.png"
			sizes="70vw"
			alt="The actions panel with the “New Action” button highlighted in a red square"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The actions panel with the “New Action” button highlighted ()
		</figcaption>
	
</figure>


<p>Now just like when you create a new layer in the Layers panel, once you click on the “Create new action” icon, a pop-up window opens with a few options in it.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e0913874-cd6f-47c5-9711-17d3d805b79a/22-photoshop-workflows-and-shortcuts-for-digital-artists.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e0913874-cd6f-47c5-9711-17d3d805b79a/22-photoshop-workflows-and-shortcuts-for-digital-artists.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e0913874-cd6f-47c5-9711-17d3d805b79a/22-photoshop-workflows-and-shortcuts-for-digital-artists.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e0913874-cd6f-47c5-9711-17d3d805b79a/22-photoshop-workflows-and-shortcuts-for-digital-artists.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e0913874-cd6f-47c5-9711-17d3d805b79a/22-photoshop-workflows-and-shortcuts-for-digital-artists.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e0913874-cd6f-47c5-9711-17d3d805b79a/22-photoshop-workflows-and-shortcuts-for-digital-artists.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e0913874-cd6f-47c5-9711-17d3d805b79a/22-photoshop-workflows-and-shortcuts-for-digital-artists.png"
			sizes="100vw"
			alt="New Action window displayed with text highlighted"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			New Action window ()
		</figcaption>
	
</figure>


<p>You can choose any given name for the <em>Action</em> you want to create and assign a <em>Function</em> key for it. So, for this demonstration purpose, I’ll create an action that will do the following:</p>

<ul>
    <li>Create a new transparent Layer;</li>
    <li>Add it as a <em>Clipping Mask</em> to the Layer below;</li>
    <li>Set its blending mode to <em>Multiply</em>.</li>
</ul>

<p>I’ll set its <em>Function</em> key to <kbd>Shift</kbd> + <kbd>F2</kbd>.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/92d06783-189a-4e6e-a955-8c51379db2c0/23-photoshop-workflows-and-shortcuts-for-digital-artists.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/92d06783-189a-4e6e-a955-8c51379db2c0/23-photoshop-workflows-and-shortcuts-for-digital-artists.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/92d06783-189a-4e6e-a955-8c51379db2c0/23-photoshop-workflows-and-shortcuts-for-digital-artists.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/92d06783-189a-4e6e-a955-8c51379db2c0/23-photoshop-workflows-and-shortcuts-for-digital-artists.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/92d06783-189a-4e6e-a955-8c51379db2c0/23-photoshop-workflows-and-shortcuts-for-digital-artists.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/92d06783-189a-4e6e-a955-8c51379db2c0/23-photoshop-workflows-and-shortcuts-for-digital-artists.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/92d06783-189a-4e6e-a955-8c51379db2c0/23-photoshop-workflows-and-shortcuts-for-digital-artists.png"
			sizes="100vw"
			alt="Custom name added and function key assigned in New Action box"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Custom name added and function key assigned in New Action box ()
		</figcaption>
	
</figure>


<p>Once you’re ready with these settings, what you need to do is press the <em>Record</em> button. Once you’ve done that, you’ll notice that the <em>Actions</em> panel now has a red button to show you it’s recording.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dabd92a1-4be4-45f1-81ba-5f4b8ce304fe/24-photoshop-workflows-and-shortcuts-for-digital-artists.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/74589404-1af0-4c71-bb08-170624f89479/24-photoshop-workflows-shortcuts-digital-artists.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/74589404-1af0-4c71-bb08-170624f89479/24-photoshop-workflows-shortcuts-digital-artists.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/74589404-1af0-4c71-bb08-170624f89479/24-photoshop-workflows-shortcuts-digital-artists.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/74589404-1af0-4c71-bb08-170624f89479/24-photoshop-workflows-shortcuts-digital-artists.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/74589404-1af0-4c71-bb08-170624f89479/24-photoshop-workflows-shortcuts-digital-artists.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/74589404-1af0-4c71-bb08-170624f89479/24-photoshop-workflows-shortcuts-digital-artists.png"
			sizes="70vw"
			alt="Recording the new Action, record button toggled"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Recording the new Action ()
		</figcaption>
	
</figure>


<p>Now you just have to go about the regular process of creating a new layer, set it as a clipping mask and change its blending mode to <em>Multiply</em>.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4fcd9bf4-edc2-41ff-863d-a7062cdce3d0/25-photoshop-workflows-and-shortcuts-for-digital-artists.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/74fc0201-e99a-4eed-b42c-51a735f92c53/25-photoshop-workflows-shortcuts-digital-artists.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/74fc0201-e99a-4eed-b42c-51a735f92c53/25-photoshop-workflows-shortcuts-digital-artists.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/74fc0201-e99a-4eed-b42c-51a735f92c53/25-photoshop-workflows-shortcuts-digital-artists.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/74fc0201-e99a-4eed-b42c-51a735f92c53/25-photoshop-workflows-shortcuts-digital-artists.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/74fc0201-e99a-4eed-b42c-51a735f92c53/25-photoshop-workflows-shortcuts-digital-artists.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/74fc0201-e99a-4eed-b42c-51a735f92c53/25-photoshop-workflows-shortcuts-digital-artists.png"
			sizes="70vw"
			alt="Heart shape layer added in Layers panel"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Heart shape layer added ()
		</figcaption>
	
</figure>












<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/57974820-fa14-4d61-8cb7-14f8e02c8a42/26-1-photoshop-workflows-and-shortcuts-for-digital-artists.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/77ad6d5d-f823-4f32-a171-4c9fe979fe41/26-1-photoshop-workflows-shortcuts-digital-artists.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/77ad6d5d-f823-4f32-a171-4c9fe979fe41/26-1-photoshop-workflows-shortcuts-digital-artists.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/77ad6d5d-f823-4f32-a171-4c9fe979fe41/26-1-photoshop-workflows-shortcuts-digital-artists.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/77ad6d5d-f823-4f32-a171-4c9fe979fe41/26-1-photoshop-workflows-shortcuts-digital-artists.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/77ad6d5d-f823-4f32-a171-4c9fe979fe41/26-1-photoshop-workflows-shortcuts-digital-artists.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/77ad6d5d-f823-4f32-a171-4c9fe979fe41/26-1-photoshop-workflows-shortcuts-digital-artists.png"
			sizes="70vw"
			alt="Heart shape layer added in Layers panel"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			New layer added on top of the heart shape ()
		</figcaption>
	
</figure>












<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ff530eaa-6386-4c57-ada3-abb32941e52d/26-2-photoshop-workflows-and-shortcuts-for-digital-artists.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6bb30fc2-756b-417a-a2b3-88948a07db44/26-2-photoshop-workflows-shortcuts-digital-artists.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6bb30fc2-756b-417a-a2b3-88948a07db44/26-2-photoshop-workflows-shortcuts-digital-artists.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6bb30fc2-756b-417a-a2b3-88948a07db44/26-2-photoshop-workflows-shortcuts-digital-artists.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6bb30fc2-756b-417a-a2b3-88948a07db44/26-2-photoshop-workflows-shortcuts-digital-artists.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6bb30fc2-756b-417a-a2b3-88948a07db44/26-2-photoshop-workflows-shortcuts-digital-artists.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/6bb30fc2-756b-417a-a2b3-88948a07db44/26-2-photoshop-workflows-shortcuts-digital-artists.png"
			sizes="70vw"
			alt="New layer made in to a clipping mask"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			New layer made in to a clipping mask to the heart shape ()
		</figcaption>
	
</figure>












<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/aedeeae0-576a-469e-870b-6dcd5c1edb00/26-3-photoshop-workflows-and-shortcuts-for-digital-artists.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/34d21989-3bc8-44e0-8d5e-d1e962289e5c/26-3-photoshop-workflows-shortcuts-digital-artists.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/34d21989-3bc8-44e0-8d5e-d1e962289e5c/26-3-photoshop-workflows-shortcuts-digital-artists.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/34d21989-3bc8-44e0-8d5e-d1e962289e5c/26-3-photoshop-workflows-shortcuts-digital-artists.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/34d21989-3bc8-44e0-8d5e-d1e962289e5c/26-3-photoshop-workflows-shortcuts-digital-artists.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/34d21989-3bc8-44e0-8d5e-d1e962289e5c/26-3-photoshop-workflows-shortcuts-digital-artists.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/34d21989-3bc8-44e0-8d5e-d1e962289e5c/26-3-photoshop-workflows-shortcuts-digital-artists.png"
			sizes="70vw"
			alt="Blending mode drop-down menu open, Multiply highlighted"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Blending mode drop-down menu open, Multiply highlighted. ()
		</figcaption>
	
</figure>


<p>Once you’re done, you have to hit the Stop icon on the <em>Actions</em> panel.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8ac59d53-713a-4f32-ac56-19db10944a84/26-4-photoshop-workflows-and-shortcuts-for-digital-artists.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f7af942c-94ba-4f26-9e41-948fa3b96337/26-4-photoshop-workflows-shortcuts-digital-artists.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f7af942c-94ba-4f26-9e41-948fa3b96337/26-4-photoshop-workflows-shortcuts-digital-artists.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f7af942c-94ba-4f26-9e41-948fa3b96337/26-4-photoshop-workflows-shortcuts-digital-artists.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f7af942c-94ba-4f26-9e41-948fa3b96337/26-4-photoshop-workflows-shortcuts-digital-artists.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f7af942c-94ba-4f26-9e41-948fa3b96337/26-4-photoshop-workflows-shortcuts-digital-artists.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f7af942c-94ba-4f26-9e41-948fa3b96337/26-4-photoshop-workflows-shortcuts-digital-artists.png"
			sizes="70vw"
			alt="Actions panel open with the red recording button"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Actions panel open with the red recording button ()
		</figcaption>
	
</figure>


<p>Your automation process is now ready to go! When you press <kbd>Shift</kbd> + <kbd>F2</kbd>, you’ll get a new Layer set as a <em>Clipping Mask</em> to the layer below and its blending mode set to <em>Multiply</em>.</p>

<p>I would also like to mention that the <em>Actions</em> automation process is not limited to just creating layers and setting blending modes. Here are some examples of some pretty handy other uses and options for actions:</p>

<ul>
<li>You can set up to save images as certain types of files to certain folders on your computer;</li>
<li>Using File&nbsp;&rarr; Automate&nbsp;&rarr; Batch for processing lots of images;</li>
<li>The <em>Allow Tool Recording</em> option in the flyout <em>Actions</em> panel menu allows actions to include painting, and so on;</li>
<li>The <em>Insert Conditional</em> option in the flyout <em>Actions</em> panel menu allows actions to change their behavior, based on the state of the document;</li>
<li>File&nbsp;&rarr; Scripts&nbsp;&rarr; Script Events Manager lets actions run based on events, like when a document is opened or a new document is created.</li>
</ul>

<p>Let me give you another example, I’ll create another <em>Action</em> that will change the size of my image and save it as a PNG file in a certain folder on my desktop.</p>

<p>So after we hit the <em>New Action</em> button on the <em>Actions panel</em>, we’ll proceed with picking the shortcut that we want, set a name for it, and I’ll take it a step further and assign a color to the <em>Action</em> (I’ll explain why this is a helpful feature in a bit).</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dbec0de9-ebcd-4374-8520-bfeff03f7721/26-photoshop-workflows-and-shortcuts-for-digital-artists.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dbec0de9-ebcd-4374-8520-bfeff03f7721/26-photoshop-workflows-and-shortcuts-for-digital-artists.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dbec0de9-ebcd-4374-8520-bfeff03f7721/26-photoshop-workflows-and-shortcuts-for-digital-artists.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dbec0de9-ebcd-4374-8520-bfeff03f7721/26-photoshop-workflows-and-shortcuts-for-digital-artists.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dbec0de9-ebcd-4374-8520-bfeff03f7721/26-photoshop-workflows-and-shortcuts-for-digital-artists.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dbec0de9-ebcd-4374-8520-bfeff03f7721/26-photoshop-workflows-and-shortcuts-for-digital-artists.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/dbec0de9-ebcd-4374-8520-bfeff03f7721/26-photoshop-workflows-and-shortcuts-for-digital-artists.png"
			sizes="100vw"
			alt="New Action box open"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			New Action box open ()
		</figcaption>
	
</figure>












<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/46c28822-fbc5-44bb-9fac-9206534ed440/27-photoshop-workflows-and-shortcuts-for-digital-artists.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/46c28822-fbc5-44bb-9fac-9206534ed440/27-photoshop-workflows-and-shortcuts-for-digital-artists.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/46c28822-fbc5-44bb-9fac-9206534ed440/27-photoshop-workflows-and-shortcuts-for-digital-artists.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/46c28822-fbc5-44bb-9fac-9206534ed440/27-photoshop-workflows-and-shortcuts-for-digital-artists.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/46c28822-fbc5-44bb-9fac-9206534ed440/27-photoshop-workflows-and-shortcuts-for-digital-artists.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/46c28822-fbc5-44bb-9fac-9206534ed440/27-photoshop-workflows-and-shortcuts-for-digital-artists.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/46c28822-fbc5-44bb-9fac-9206534ed440/27-photoshop-workflows-and-shortcuts-for-digital-artists.png"
			sizes="100vw"
			alt="Selecting the Function key"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Selecting the Function key ()
		</figcaption>
	
</figure>












<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c1033b63-758c-4713-a008-14663419d886/28-photoshop-workflows-and-shortcuts-for-digital-artists.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c1033b63-758c-4713-a008-14663419d886/28-photoshop-workflows-and-shortcuts-for-digital-artists.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c1033b63-758c-4713-a008-14663419d886/28-photoshop-workflows-and-shortcuts-for-digital-artists.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c1033b63-758c-4713-a008-14663419d886/28-photoshop-workflows-and-shortcuts-for-digital-artists.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c1033b63-758c-4713-a008-14663419d886/28-photoshop-workflows-and-shortcuts-for-digital-artists.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c1033b63-758c-4713-a008-14663419d886/28-photoshop-workflows-and-shortcuts-for-digital-artists.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c1033b63-758c-4713-a008-14663419d886/28-photoshop-workflows-and-shortcuts-for-digital-artists.png"
			sizes="100vw"
			alt="Checking the Shift checkbox"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Checking the Shift checkbox ()
		</figcaption>
	
</figure>












<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/661109c9-2a67-4869-8ea9-846416ff2697/29-photoshop-workflows-and-shortcuts-for-digital-artists.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/661109c9-2a67-4869-8ea9-846416ff2697/29-photoshop-workflows-and-shortcuts-for-digital-artists.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/661109c9-2a67-4869-8ea9-846416ff2697/29-photoshop-workflows-and-shortcuts-for-digital-artists.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/661109c9-2a67-4869-8ea9-846416ff2697/29-photoshop-workflows-and-shortcuts-for-digital-artists.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/661109c9-2a67-4869-8ea9-846416ff2697/29-photoshop-workflows-and-shortcuts-for-digital-artists.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/661109c9-2a67-4869-8ea9-846416ff2697/29-photoshop-workflows-and-shortcuts-for-digital-artists.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/661109c9-2a67-4869-8ea9-846416ff2697/29-photoshop-workflows-and-shortcuts-for-digital-artists.png"
			sizes="100vw"
			alt="Picking a color for the Action"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Picking a color for the Action ()
		</figcaption>
	
</figure>












<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0559a70d-0c93-4448-83e3-9883a2ede9af/30-photoshop-workflows-and-shortcuts-for-digital-artists.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0559a70d-0c93-4448-83e3-9883a2ede9af/30-photoshop-workflows-and-shortcuts-for-digital-artists.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0559a70d-0c93-4448-83e3-9883a2ede9af/30-photoshop-workflows-and-shortcuts-for-digital-artists.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0559a70d-0c93-4448-83e3-9883a2ede9af/30-photoshop-workflows-and-shortcuts-for-digital-artists.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0559a70d-0c93-4448-83e3-9883a2ede9af/30-photoshop-workflows-and-shortcuts-for-digital-artists.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0559a70d-0c93-4448-83e3-9883a2ede9af/30-photoshop-workflows-and-shortcuts-for-digital-artists.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0559a70d-0c93-4448-83e3-9883a2ede9af/30-photoshop-workflows-and-shortcuts-for-digital-artists.png"
			sizes="100vw"
			alt="Displaying that a blue color was picked for the new action"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Blue color picked for the new Action ()
		</figcaption>
	
</figure>


<p>Now about that color, you may notice that when you assign a color, it doesn’t really reflect in the <em>Actions Panel</em>. Instead, everything stays monochrome. The reason is because when you typically open that panel, you’re in the <em>Edit</em> view, where you’re able to modify the <em>Actions</em>, record new ones, and so on. In order to see all of the available actions in a simpler interface, do this:</p>

<ul>
    <li>On the upper-right hand corner of the panel you will see four horizontal lines. Click on those.</li>
    <li>You’ll get a drop-down menu, where you have different <em>Actions</em> options. On the top, you’ll notice a <em>Button Mode</em>.</li>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1488e241-b911-44e7-b96a-215cd1e1670e/31-photoshop-workflows-and-shortcuts-for-digital-artists.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1488e241-b911-44e7-b96a-215cd1e1670e/31-photoshop-workflows-and-shortcuts-for-digital-artists.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1488e241-b911-44e7-b96a-215cd1e1670e/31-photoshop-workflows-and-shortcuts-for-digital-artists.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1488e241-b911-44e7-b96a-215cd1e1670e/31-photoshop-workflows-and-shortcuts-for-digital-artists.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1488e241-b911-44e7-b96a-215cd1e1670e/31-photoshop-workflows-and-shortcuts-for-digital-artists.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1488e241-b911-44e7-b96a-215cd1e1670e/31-photoshop-workflows-and-shortcuts-for-digital-artists.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1488e241-b911-44e7-b96a-215cd1e1670e/31-photoshop-workflows-and-shortcuts-for-digital-artists.png"
			sizes="100vw"
			alt="Actions’ drop-down menu open, highlighted Button Mode"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Actions’ drop-down menu open, highlighted 'Button Mode'. ()
		</figcaption>
	
</figure>


<li>Clicking on that will change the <em>Actions Panel</em> interface, where you will see your available <em>Actions</em> as colorful buttons.</li>
</ul>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ff4aa1dc-325e-4142-ab5a-18b0bfa2789f/32-photoshop-workflows-and-shortcuts-for-digital-artists.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ff4aa1dc-325e-4142-ab5a-18b0bfa2789f/32-photoshop-workflows-and-shortcuts-for-digital-artists.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ff4aa1dc-325e-4142-ab5a-18b0bfa2789f/32-photoshop-workflows-and-shortcuts-for-digital-artists.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ff4aa1dc-325e-4142-ab5a-18b0bfa2789f/32-photoshop-workflows-and-shortcuts-for-digital-artists.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ff4aa1dc-325e-4142-ab5a-18b0bfa2789f/32-photoshop-workflows-and-shortcuts-for-digital-artists.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ff4aa1dc-325e-4142-ab5a-18b0bfa2789f/32-photoshop-workflows-and-shortcuts-for-digital-artists.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ff4aa1dc-325e-4142-ab5a-18b0bfa2789f/32-photoshop-workflows-and-shortcuts-for-digital-artists.png"
			sizes="100vw"
			alt="The Actions’ button mode"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			The Actions’ button mode ()
		</figcaption>
	
</figure>


<p>If you haven’t guessed it already, coloring your <em>Actions</em> will help you distinguish them more easily at a glance. In Button mode, when you take a glance at the panel, you will be able to navigate quickly to the <em>Action</em> that you want to apply to your image/drawing (if you don’t really remember the shortcut you’ve assigned for it).</p>

<p>Okay, so what we have so far is the following:</p>

<ol>
<li>We’ve created a new action;</li>
<li>Set the shortcut for it;</li>
<li>Changed its color;</li>
<li>Named it.</li>
</ol>

<p>Let’s proceed with recording the process that we need.</p>

<p>To open the <em>Image Size</em> menu, you can either go to Image&nbsp;&rarr; Image Size or simply hit <kbd>Ctrl</kbd> + <kbd>Alt</kbd> + <kbd>I</kbd> and you’ll get this window:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/55dcc91a-759a-4640-b5b6-51f9f8ca6cd5/33-photoshop-workflows-and-shortcuts-for-digital-artists.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/55dcc91a-759a-4640-b5b6-51f9f8ca6cd5/33-photoshop-workflows-and-shortcuts-for-digital-artists.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/55dcc91a-759a-4640-b5b6-51f9f8ca6cd5/33-photoshop-workflows-and-shortcuts-for-digital-artists.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/55dcc91a-759a-4640-b5b6-51f9f8ca6cd5/33-photoshop-workflows-and-shortcuts-for-digital-artists.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/55dcc91a-759a-4640-b5b6-51f9f8ca6cd5/33-photoshop-workflows-and-shortcuts-for-digital-artists.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/55dcc91a-759a-4640-b5b6-51f9f8ca6cd5/33-photoshop-workflows-and-shortcuts-for-digital-artists.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/55dcc91a-759a-4640-b5b6-51f9f8ca6cd5/33-photoshop-workflows-and-shortcuts-for-digital-artists.png"
			sizes="100vw"
			alt=" Image size menu open"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			 Image size menu open ()
		</figcaption>
	
</figure>


<p>What you would want to do is set the desired size for your image and once you’re happy with that hit “OK” to apply the changes.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ef857ccd-ac1f-4bf3-ae41-ef0b780efc07/34-photoshop-workflows-and-shortcuts-for-digital-artists.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ef857ccd-ac1f-4bf3-ae41-ef0b780efc07/34-photoshop-workflows-and-shortcuts-for-digital-artists.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ef857ccd-ac1f-4bf3-ae41-ef0b780efc07/34-photoshop-workflows-and-shortcuts-for-digital-artists.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ef857ccd-ac1f-4bf3-ae41-ef0b780efc07/34-photoshop-workflows-and-shortcuts-for-digital-artists.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ef857ccd-ac1f-4bf3-ae41-ef0b780efc07/34-photoshop-workflows-and-shortcuts-for-digital-artists.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ef857ccd-ac1f-4bf3-ae41-ef0b780efc07/34-photoshop-workflows-and-shortcuts-for-digital-artists.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/ef857ccd-ac1f-4bf3-ae41-ef0b780efc07/34-photoshop-workflows-and-shortcuts-for-digital-artists.png"
			sizes="100vw"
			alt="Image size values changed"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Image size values changed ()
		</figcaption>
	
</figure>


<p>Next, what we want to do is use the <em>Save As</em> option in order to get the option to choose the type of file, destination folder, and so on. You can either go to <em>File</em>&nbsp;&rarr; <em>Save As...</em> or you could simply press <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>S</kbd> and you will get the following window:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/04128c8b-f8a2-4376-a834-e33ca88c6de5/35-photoshop-workflows-and-shortcuts-for-digital-artists.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/04128c8b-f8a2-4376-a834-e33ca88c6de5/35-photoshop-workflows-and-shortcuts-for-digital-artists.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/04128c8b-f8a2-4376-a834-e33ca88c6de5/35-photoshop-workflows-and-shortcuts-for-digital-artists.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/04128c8b-f8a2-4376-a834-e33ca88c6de5/35-photoshop-workflows-and-shortcuts-for-digital-artists.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/04128c8b-f8a2-4376-a834-e33ca88c6de5/35-photoshop-workflows-and-shortcuts-for-digital-artists.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/04128c8b-f8a2-4376-a834-e33ca88c6de5/35-photoshop-workflows-and-shortcuts-for-digital-artists.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/04128c8b-f8a2-4376-a834-e33ca88c6de5/35-photoshop-workflows-and-shortcuts-for-digital-artists.png"
			sizes="100vw"
			alt="Saving dialogue box open"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Saving dialogue box open ()
		</figcaption>
	
</figure>


<p>Navigate to the dedicated folder in which you want to save the current project in and actually save it there. An additional <em>Action</em> you can do is to close the image/project you’re working on (don’t worry, the <em>Actions</em> won’t stop recording unless you close down Photoshop).</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9f19b4ad-67c2-4c0a-a945-059920842be6/36-photoshop-workflows-and-shortcuts-for-digital-artists.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9f19b4ad-67c2-4c0a-a945-059920842be6/36-photoshop-workflows-and-shortcuts-for-digital-artists.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9f19b4ad-67c2-4c0a-a945-059920842be6/36-photoshop-workflows-and-shortcuts-for-digital-artists.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9f19b4ad-67c2-4c0a-a945-059920842be6/36-photoshop-workflows-and-shortcuts-for-digital-artists.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9f19b4ad-67c2-4c0a-a945-059920842be6/36-photoshop-workflows-and-shortcuts-for-digital-artists.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9f19b4ad-67c2-4c0a-a945-059920842be6/36-photoshop-workflows-and-shortcuts-for-digital-artists.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9f19b4ad-67c2-4c0a-a945-059920842be6/36-photoshop-workflows-and-shortcuts-for-digital-artists.png"
			sizes="100vw"
			alt="Saving file as PNG, PNG options displayed"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			PNG options displayed ()
		</figcaption>
	
</figure>


<p>Once all of that is done, you can hit the <em>Stop</em> icon on the <em>Actions Panel</em> to stop recording your movement in Photoshop.</p>

<p>If you need to resize a bunch of files and save them in a dedicated folder, you just have to load them up in Photoshop and continue hitting the <em>Action</em> shortcut that you’ve created for <em>Resizing and Saving</em>.</p>

<p>If you take the time to get accustomed to the <em>Actions tool</em> in Photoshop and utilize it, you can say “Goodbye” to the bothersome repetitive work that usually eats up most of your time. You will be able to fly through these tasks with such speed that even  could get jealous of.</p>

<h3 id="conclusion">9. Conclusion</h3>

<p>In this article, I’ve shared some of the shortcuts I mostly use. I sincerely hope that they will help you boost up your productivity and make your workflow better as well.</p>

<h5>Special Thanks</h5>

<p><em>I would like to mention that this tutorial was made possible with the help of Angel (a.k.a. ArcanumEX). You can check out his artwork on his .</em></p>

<h4 id="further-reading">Further Reading</h4>

<p>In addition to everything I’ve talked about so far, I’ll include more resources that I believe you might find helpful. Be sure to check out:</p>

<ul>
<li><a href="https://noahbradley.com/blogs/blog">Noah Bradley’s Resource page<a/></li>
<li><a href="https://www.youtube.com/user/FZDSCHOOL">Feng Zhu’s YouTube Channel<a/></li>
<li></li>
<li></li>
</ul>

<p>What are your favorite shortcuts? Feel free to share them in the comments below!</p>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(mb, ra, yk, il)</span>
</div>


              </article>
            </body>
          </html>
---------------
<h1 id="#title_7" >8、NVIDIA宣布RAPIDS、医学影像应用和面向自动驾驶汽车的驾驶模拟器</h1>
Roland Meertens
[http://www.infoq.com/cn/news/2018/10/Nvidia-keynote-gtc?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/10/Nvidia-keynote-gtc?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>2018年10月10日，在慕尼黑2018年GPU技术大会上，NVIDIA首席执行官Jensen Huang发表了主题演讲。他宣布了RAPIDS，这是一个开源的CUDA加速工具包，可以帮助数据科学家更快地处理数据。他们宣布了在医学影像方面开展的合作。他们还宣布了一个自动驾驶汽车模拟器，汽车制造商可以使用它来验证自动驾驶汽车。</p> <i>By Roland Meertens</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_8" >9、微软发布Azure Storage不可变存储功能的正式版本</h1>
Steef-Jan Wiggers
[http://www.infoq.com/cn/news/2018/10/immutable-storage-azure-ga?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/10/immutable-storage-azure-ga?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>随着新的不可变存储功能的发布，blob特性在特定的保留期间内将是不可以擦除和修改的。该特性从今年6月份开始进行预览使用，现在，微软宣布它在所有公开Azure region中正式发布。</p> <i>By Steef-Jan Wiggers</i> <i> Translated by 张卫滨 </i>
---------------
<h1 id="#title_9" >10、Git Submodule新漏洞已修复</h1>
Sergio De Simone
[http://www.infoq.com/cn/news/2018/10/git-submodule-vulnerability?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/10/git-submodule-vulnerability?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Git社区披露了一个影响clone和submodule命令的安全漏洞，当存在漏洞的机器访问恶意库时，这些命令可以远程执行代码。这个由Mitre分配了编号CVE-2018-17456的漏洞已在Git 2.19.1中修复。</p> <i>By Sergio De Simone</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_10" >11、Cloudflare推出域名注册服务：不赚利润只收取成本费</h1>
张婵
[http://www.infoq.com/cn/news/2018/10/cloudflare-Domain-Nam-Reg?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/10/cloudflare-Domain-Nam-Reg?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>9月27日，Cloudflare官方博客宣布推出域名注册服务，承诺只收取成本费，不赚取利润。

Cloudflare在2010年9月成立，在那之前就有Cloudflare的早期测试版客户问：“你们会推出注册服务吗？！”现在Cloudflare就在做这样的事情，启动第一个能让大家都喜爱的域名注册服务。它围绕三个原则构建：信任，安全和始终公平的定价，可供所有Cloudflare客户使用。

在博客中，Cloudflare也阐述了自己为什么要做这样的域名注册服务。</p> <i>By 张婵</i>
---------------
<h1 id="#title_11" >12、Facebook曝至今最严重安全漏洞，超过5000万用户受影响</h1>
张婵
[http://www.infoq.com/cn/news/2018/10/Facebook-reveals-security-flaw?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/10/Facebook-reveals-security-flaw?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>9月28日，Facebook披露了一个安全漏洞，5000万Facebook用户受到影响，恶意第三方可能会利用这个漏洞访问受影响的用户帐户。Facebook已确认创始人马克扎克伯格及首席运营官谢丽尔桑德伯格是受影响的5000万账户之一。</p> <i>By 张婵</i>
---------------