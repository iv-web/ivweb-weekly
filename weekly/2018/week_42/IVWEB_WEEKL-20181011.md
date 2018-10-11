## 文章索引
1、 <a href="#1挑战谷歌英伟达华为披露芯片+ai解决方案" >挑战谷歌英伟达？华为披露芯片+AI解决方案！</a><br/>
2、 <a href="#2git-原理入门" >Git 原理入门</a><br/>
3、 <a href="#3form-design-patterns-book-excerpt:-a-registration-form" >Form Design Patterns Book Excerpt: A Registration Form</a><br/>
4、 <a href="#4文章-scrum丰田之道" >文章： Scrum丰田之道</a><br/>
5、 <a href="#5文章-2018年夏加密数字化货币现状下" >文章： 2018年夏加密数字化货币现状（下）</a><br/>
6、 <a href="#6文章-kubernetes上的十大应用程序" >文章： Kubernetes上的十大应用程序</a><br/>
7、 <a href="#7meet-form-design-patterns-our-new-book-on-accessible-web-forms-now-shipping!" >Meet “Form Design Patterns,” Our New Book On Accessible Web Forms — Now Shipping!</a><br/>
8、 <a href="#8rsocket一个面向反应式应用程序的新型应用网络协议" >RSocket：一个面向反应式应用程序的新型应用网络协议</a><br/>
9、 <a href="#9springone大会上发布了一个实验性的反应式关系型数据库连接驱动r2dbc" >SpringOne大会上发布了一个实验性的反应式关系型数据库连接驱动R2DBC</a><br/>
10、 <a href="#10访谈kotlin在pinterest的逆势生长" >访谈：Kotlin在Pinterest的逆势生长</a><br/>
11、 <a href="#11russ-miles被忽略的架构师和混沌工程" >Russ Miles：被忽略的架构师和混沌工程</a><br/>
12、 <a href="#12netflix实时流处理平台keystone介绍" >Netflix实时流处理平台Keystone介绍</a><br/>
13、 <a href="#13glassfish新纪元" >GlassFish新纪元</a><br/><h1 id="#title_0" >1、挑战谷歌英伟达？华为披露芯片+AI解决方案！</h1>
陈思
[http://www.infoq.com/cn/news/2018/10/hc-ai-chip?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/10/hc-ai-chip?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>10 月 10 日，上海世博展览馆，华为 HC 大会上，华为副董事长徐直军发布了华为 AI 战略和全栈解决方案，其中包括了两款芯片。以下是 AI 前线记者在活动现场的报道。</p> <i>By 陈思</i>
---------------
<h1 id="#title_1" >2、Git 原理入门</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2018/10/git-internals.html](http://www.ruanyifeng.com/blog/2018/10/git-internals.html)
<p>Git 是最流行的版本管理工具，也是程序员的必备技能之一。</p>

        <p>即使天天使用它，很多人也未必了解它的原理。Git 为什么可以管理版本？<code>git add</code>、<code>git commit</code>这些，到底在做什么，你说得清楚吗？</p>

<p>这篇文章用一个实例，解释 Git 的运行过程，帮助你理解 Git 的原理。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201810/bg2018101001.png" alt="" title="" /></p>

<h2>一、初始化</h2>

<p>首先，让我们创建一个项目目录，并进入该目录。</p>

<blockquote><pre><code class="language-bash">
$ mkdir git-demo-project
$ cd git-demo-project
</code></pre></blockquote>

<p>我们打算对该项目进行版本管理，第一件事就是使用<code>git init</code>命令，进行初始化。</p>

<blockquote><pre><code class="language-bash">
$ git init
</code></pre></blockquote>

<p><code>git init</code>命令只做一件事，就是在项目根目录下创建一个<code>.git</code>子目录，用来保存版本信息。</p>

<blockquote><pre><code class="language-bash">
$ ls .git

branches/
config
description
HEAD
hooks/
info/
objects/
refs/
</code></pre></blockquote>

<p>上面命令显示，<code>.git</code>内部还有一些子目录，这里先不解释它们的含义。</p>

<h2>二、保存对象</h2>

<p>接下来，新建一个空文件<code>test.txt</code>。</p>

<blockquote><pre><code class="language-bash">
$ touch test.txt
</code></pre></blockquote>

<p>然后，把这个文件加入 Git 仓库，也就是为<code>test.txt</code>的当前内容创建一个副本。</p>

<blockquote><pre><code class="language-bash">
$ git hash-object -w test.txt

e69de29bb2d1d6434b8b29ae775ad8c2e48c5391
</code></pre></blockquote>

<p>上面代码中，<code>git hash-object</code>命令把<code>test.txt</code>的当前内容压缩成二进制文件，存入 Git。压缩后的二进制文件，称为一个 Git 对象，保存在<code>.git/objects</code>目录。</p>

<p>这个命令还会计算当前内容的 SHA1 哈希值（长度40的字符串），作为该对象的文件名。下面看一下这个新生成的 Git 对象文件。</p>

<blockquote><pre><code class="language-bash">
$ ls -R .git/objects

.git/objects/e6:
9de29bb2d1d6434b8b29ae775ad8c2e48c5391
</code></pre></blockquote>

<p>上面代码可以看到，<code>.git/objects</code>下面多了一个子目录，目录名是哈希值的前2个字符，该子目录下面有一个文件，文件名是哈希值的后38个字符。</p>

<p>再看一下这个文件的内容。</p>

<blockquote><pre><code class="language-bash">
$ cat .git/objects/e6/9de29bb2d1d6434b8b29ae775ad8c2e48c5391
</code></pre></blockquote>

<p>上面代码输出的文件内容，都是一些二进制字符。你可能会问，<code>test.txt</code>是一个空文件，为什么会有内容？这是因为二进制对象里面还保存一些元数据。</p>

<p>如果想看该文件原始的文本内容，要用<code>git cat-file</code>命令。</p>

<blockquote><pre><code class="language-bash">
$ git cat-file -p e69de29bb2d1d6434b8b29ae775ad8c2e48c5391
</code></pre></blockquote>

<p>因为原始文件是空文件，所以上面的命令什么也看不到。现在向<code>test.txt</code>写入一些内容。</p>

<blockquote><pre><code class="language-bash">
$ echo 'hello world' > test.txt
</code></pre></blockquote>

<p>因为文件内容已经改变，需要将它再次保存成 Git 对象。</p>

<blockquote><pre><code class="language-bash">
$ git hash-object -w test.txt

3b18e512dba79e4c8300dd08aeb37f8e728b8dad
</code></pre></blockquote>

<p>上面代码可以看到，随着内容改变，<code>test.txt</code>的哈希值已经变了。同时，新文件<code>.git/objects/3b/18e512dba79e4c8300dd08aeb37f8e728b8dad</code>也已经生成了。现在可以看到文件内容了。</p>

<blockquote><pre><code class="language-bash">
$ git cat-file -p 3b18e512dba79e4c8300dd08aeb37f8e728b8dad

hello world
</code></pre></blockquote>

<h2>三、暂存区</h2>

<p>文件保存成二进制对象以后，还需要通知 Git 哪些文件发生了变动。所有变动的文件，Git 都记录在一个区域，叫做"暂存区"（英文叫做 index 或者 stage）。等到变动告一段落，再统一把暂存区里面的文件写入正式的版本历史。</p>

<p><code>git update-index</code>命令用于在暂存区记录一个发生变动的文件。</p>

<blockquote><pre><code class="language-bash">
$ git update-index --add --cacheinfo 100644 \
3b18e512dba79e4c8300dd08aeb37f8e728b8dad test.txt
</code></pre></blockquote>

<p>上面命令向暂存区写入文件名<code>test.txt</code>、二进制对象名（哈希值）和文件权限。</p>

<p><code>git ls-files</code>命令可以显示暂存区当前的内容。</p>

<blockquote><pre><code class="language-bash">
$ git ls-files --stage

100644 3b18e512dba79e4c8300dd08aeb37f8e728b8dad 0   test.txt
</code></pre></blockquote>

<p>上面代码表示，暂存区现在只有一个文件<code>test.txt</code>，以及它的二进制对象名和权限。知道了二进制对象名，就可以在<code>.git/objects</code>子目录里面读出这个文件的内容。</p>

<p><code>git status</code>命令会产生更可读的结果。</p>

<blockquote><pre><code class="language-bash">
$ git status

要提交的变更：
    新文件：   test.txt
</code></pre></blockquote>

<p>上面代码表示，暂存区里面只有一个新文件<code>test.txt</code>，等待写入历史。</p>

<h2>四、git add 命令</h2>

<p>上面两步（保存对象和更新暂存区），如果每个文件都做一遍，那是很麻烦的。Git 提供了<code>git add</code>命令简化操作。</p>

<blockquote><pre><code class="language-bash">
$ git add --all
</code></pre></blockquote>

<p>上面命令相当于，对当前项目所有变动的文件，执行前面的两步操作。</p>

<h2>五、commit 的概念</h2>

<p>暂存区保留本次变动的文件信息，等到修改了差不多了，就要把这些信息写入历史，这就相当于生成了当前项目的一个快照（snapshot）。</p>

<p>项目的历史就是由不同时点的快照构成。Git 可以将项目恢复到任意一个快照。快照在 Git 里面有一个专门名词，叫做 commit，生成快照又称为完成一次提交。</p>

<p>下文所有提到"快照"的地方，指的就是 commit。</p>

<h2>六、完成提交</h2>

<p>首先，设置一下用户名和 Email，保存快照的时候，会记录是谁提交的。</p>

<blockquote><pre><code class="language-bash">
$ git config user.name "用户名" 
$ git config user.email "Email 地址"
</code></pre></blockquote>

<p>接下来，要保存当前的目录结构。前面保存对象的时候，只是保存单个文件，并没有记录文件之间的目录关系（哪个文件在哪里）。</p>

<p><code>git write-tree</code>命令用来将当前的目录结构，生成一个 Git 对象。</p>

<blockquote><pre><code class="language-bash">
$ git write-tree

c3b8bb102afeca86037d5b5dd89ceeb0090eae9d
</code></pre></blockquote>

<p>上面代码中，目录结构也是作为二进制对象保存的，也保存在<code>.git/objects</code>目录里面，对象名就是哈希值。</p>

<p>让我们看一下这个文件的内容。</p>

<blockquote><pre><code class="language-bash">
$ git cat-file -p c3b8bb102afeca86037d5b5dd89ceeb0090eae9d

100644 blob 3b18e512dba79e4c8300dd08aeb37f8e728b8dad    test.txt
</code></pre></blockquote>

<p>可以看到，当前的目录里面只有一个<code>test.txt</code>文件。</p>

<p>所谓快照，就是保存当前的目录结构，以及每个文件对应的二进制对象。上一个操作，目录结构已经保存好了，现在需要将这个目录结构与一些元数据一起写入版本历史。</p>

<p><code>git commit-tree</code>命令用于将目录树对象写入版本历史。</p>

<blockquote><pre><code class="language-bash">
$ echo "first commit" | git commit-tree c3b8bb102afeca86037d5b5dd89ceeb0090eae9d

c9053865e9dff393fd2f7a92a18f9bd7f2caa7fa
</code></pre></blockquote>

<p>上面代码中，提交的时候需要有提交说明，<code>echo "first commit"</code>就是给出提交说明。然后，<code>git commit-tree</code>命令将元数据和目录树，一起生成一个 Git 对象。现在，看一下这个对象的内容。</p>

<blockquote><pre><code class="language-bash">
$ git cat-file -p c9053865e9dff393fd2f7a92a18f9bd7f2caa7fa

tree c3b8bb102afeca86037d5b5dd89ceeb0090eae9d
author ruanyf <yifeng.ruan@gmail.com> 1538889134 +0800
committer ruanyf <yifeng.ruan@gmail.com> 1538889134 +0800

first commit
</code></pre></blockquote>

<p>上面代码中，输出结果的第一行是本次快照对应的目录树对象（tree），第二行和第三行是作者和提交人信息，最后是提交说明。</p>

<p><code>git log</code>命令也可以用来查看某个快照信息。</p>

<blockquote><pre><code class="language-bash">
$ git log --stat c9053865e9dff393fd2f7a92a18f9bd7f2caa7fa

commit c9053865e9dff393fd2f7a92a18f9bd7f2caa7fa
Author: ruanyf <yifeng.ruan@gmail.com>
Date:   Sun Oct 7 13:12:14 2018 +0800

    first commit

 test.txt | 1 +
 1 file changed, 1 insertion(+)
</code></pre></blockquote>

<h2>七、git commit 命令</h2>

<p>Git 提供了<code>git commit</code>命令，简化提交操作。保存进暂存区以后，只要<code>git commit</code>一个命令，就同时提交目录结构和说明，生成快照。</p>

<blockquote><pre><code class="language-bash">
$ git commit -m "first commit"
</code></pre></blockquote>

<p>此外，还有两个命令也很有用。</p>

<p><code>git checkout</code>命令用于切换到某个快照。</p>

<blockquote><pre><code class="language-bash">
$ git checkout c9053865e9dff393fd2f7a92a18f9bd7f2caa7fa
</code></pre></blockquote>

<p><code>git show</code>命令用于展示某个快照的所有代码变动。</p>

<blockquote><pre><code class="language-bash">
$ git show c9053865e9dff393fd2f7a92a18f9bd7f2caa7fa
</code></pre></blockquote>

<h2>八、branch 的概念</h2>

<p>到了这一步，还没完。如果这时用<code>git log</code>命令查看整个版本历史，你看不到新生成的快照。</p>

<blockquote><pre><code class="language-bash">
$ git log
</code></pre></blockquote>

<p>上面命令没有任何输出，这是为什么呢？快照明明已经写入历史了。</p>

<p>原来<code>git log</code>命令只显示当前分支的变动，虽然我们前面已经提交了快照，但是还没有记录这个快照属于哪个分支。</p>

<p>所谓分支（branch）就是指向某个快照的指针，分支名就是指针名。哈希值是无法记忆的，分支使得用户可以为快照起别名。而且，分支会自动更新，如果当前分支有新的快照，指针就会自动指向它。比如，master 分支就是有一个叫做 master 指针，它指向的快照就是 master 分支的当前快照。</p>

<p>用户可以对任意快照新建指针。比如，新建一个 fix-typo 分支，就是创建一个叫做 fix-typo 的指针，指向某个快照。所以，Git 新建分支特别容易，成本极低。</p>

<p>Git 有一个特殊指针<code>HEAD</code>， 总是指向当前分支的最近一次快照。另外，Git 还提供简写方式，<code>HEAD^</code>指向 <code>HEAD</code>的前一个快照（父节点），<code>HEAD~6</code>则是<code>HEAD</code>之前的第6个快照。</p>

<p>每一个分支指针都是一个文本文件，保存在<code>.git/refs/heads/</code>目录，该文件的内容就是它所指向的快照的二进制对象名（哈希值）。</p>

<h2>九、更新分支</h2>

<p>下面演示更新分支是怎么回事。首先，修改一下<code>test.txt</code>。</p>

<blockquote><pre><code class="language-bash">
$ echo "hello world again" > test.txt
</code></pre></blockquote>

<p>然后，保存二进制对象。</p>

<blockquote><pre><code class="language-bash">
$ git hash-object -w test.txt

c90c5155ccd6661aed956510f5bd57828eec9ddb
</code></pre></blockquote>

<p>接着，将这个对象写入暂存区，并保存目录结构。</p>

<blockquote><pre><code class="language-bash">
$ git update-index test.txt
$ git write-tree

1552fd52bc14497c11313aa91547255c95728f37
</code></pre></blockquote>

<p>最后，提交目录结构，生成一个快照。</p>

<blockquote><pre><code class="language-bash">
$ echo "second commit" | git commit-tree 1552fd52bc14497c11313aa91547255c95728f37 -p c9053865e9dff393fd2f7a92a18f9bd7f2caa7fa

785f188674ef3c6ddc5b516307884e1d551f53ca
</code></pre></blockquote>

<p>上面代码中，<code>git commit-tree</code>的<code>-p</code>参数用来指定父节点，也就是本次快照所基于的快照。</p>

<p>现在，我们把本次快照的哈希值，写入<code>.git/refs/heads/master</code>文件，这样就使得<code>master</code>指针指向这个快照。</p>

<blockquote><pre><code class="language-bash">
$ echo 785f188674ef3c6ddc5b516307884e1d551f53ca > .git/refs/heads/master
</code></pre></blockquote>

<p>现在，<code>git log</code>就可以看到两个快照了。</p>

<blockquote><pre><code class="language-bash">
$ git log

commit 785f188674ef3c6ddc5b516307884e1d551f53ca (HEAD -> master)
Author: ruanyf <yifeng.ruan@gmail.com>
Date:   Sun Oct 7 13:38:00 2018 +0800

    second commit

commit c9053865e9dff393fd2f7a92a18f9bd7f2caa7fa
Author: ruanyf <yifeng.ruan@gmail.com>
Date:   Sun Oct 7 13:12:14 2018 +0800

    first commit
</code></pre></blockquote>

<p><code>git log</code>的运行过程是这样的：</p>

<blockquote>
  <ol start='1'>
<li>查找<code>HEAD</code>指针对应的分支，本例是<code>master</code></li>
<li>找到<code>master</code>指针指向的快照，本例是<code>785f188674ef3c6ddc5b516307884e1d551f53ca</code></li>
<li>找到父节点（前一个快照）<code>c9053865e9dff393fd2f7a92a18f9bd7f2caa7fa</code></li>
<li>以此类推，显示当前分支的所有快照</li>
</ol>
</blockquote>

<p>最后，补充一点。前面说过，分支指针是动态的。原因在于，下面三个命令会自动改写分支指针。</p>

<blockquote>
  <ul>
<li><code>git commit</code>：当前分支指针移向新创建的快照。</li>
<li><code>git pull</code>：当前分支与远程分支合并后，指针指向新创建的快照。</li>
<li><code>git reset [commit_sha]</code>：当前分支指针重置为指定快照。</li>
</ul>
</blockquote>

<h2>十、参考链接</h2>

<ul>
<li>, Shalitha Suranga</li>
</ul>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2018-10-10T18:07:14+08:00">2018年10月10日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>文集：</li>
<li>社交媒体：</li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------
<h1 id="#title_2" >3、Form Design Patterns Book Excerpt: A Registration Form</h1>
Adam Silver
[https://www.smashingmagazine.com/2018/10/form-design-patterns-excerpt-a-registration-form/](https://www.smashingmagazine.com/2018/10/form-design-patterns-excerpt-a-registration-form/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/10/form-design-patterns-excerpt-a-registration-form/" />
              <title>Form Design Patterns Book Excerpt: A Registration Form</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>Form Design Patterns Book Excerpt: A Registration Form</h1>
                  
                    
                    <address>Adam Silver</address>
                  
                  <time datetime="2018-10-10T12:25:00&#43;02:00" class="op-published">2018-10-10T12:25:00+02:00</time>
                  <time datetime="2018-10-10T12:57:45&#43;00:00" class="op-modified">2018-10-10T12:57:45+00:00</time>
                </header>
                <p>Let’s start with a registration form. Most companies want long-term relationships with their users. To do that they need users to sign up. And to do <em>that</em>, they need to give users value in return. Nobody wants to sign up to your service — they just want to access whatever it is you offer, or the promise of a faster experience next time they visit.</p>
<p>Despite the registration form’s basic appearance, there are many things to consider: the primitive elements that make up a form (labels, buttons, and inputs), ways to reduce effort (even on small forms like this), all the way through to form validation.</p>
<p>In choosing such a simple form, we can zoom in on the foundational qualities found in well-designed forms.</p>
<h3>How It Might Look</h3>
<p>The form is made up of four fields and a submit button. Each field is made up of a control (the input) and its associated label.</p>
<figure><img src="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d7c5cc2c-1eb3-4041-bf55-9f8206f98bfa/registration-form-01.png" alt="Registration form with four fields: first name, last name, email address, and password." /><figcaption>Registration form with four fields: first name, last name, email address, and password.</figcaption></figure>
<p>Here’s the HTML:</p>
<pre><code class="language-markup">&lt;form&gt;
  &lt;label for="firstName"&gt;First name&lt;/label&gt;
  &lt;input type="text" id="firstName" name="firstName"&gt;
  &lt;label for="lastName"&gt;Last name&lt;/label&gt;
  &lt;input type="text" id="lastName" name="lastName"&gt;
  &lt;label for="email"&gt;Email address&lt;/label&gt;
  &lt;input type="email" id="email" name="email"&gt;
  &lt;label for="password"&gt;Create password&lt;/label&gt;
  &lt;input type="password" id="password" name="password" placeholder="Must be at least 8 characters"&gt;
  &lt;input type="submit" value="Register"&gt;
&lt;/form&gt;</code></pre>
<p>Labels are where our discussion begins.</p>
<h3>Labels</h3>
<p>In <em></em>, Laura Kalbag sets out four broad parameters that improve the user experience for everyone:</p>
<ul>
<li><strong>Visual</strong>: make it easy to see.</li>
<li><strong>Auditory</strong>: make it easy to hear.</li>
<li><strong>Motor</strong>: make it easy to interact with.</li>
<li><strong>Cognitive</strong>: make it easy to understand.</li>
</ul>
<p>By looking at labels from each of these standpoints, we can see just how important labels are. Sighted users can read them, visually-impaired users can hear them by using a screen reader, and motor-impaired users can more easily set focus to the field thanks to the larger hit area. That’s because clicking a label sets focus to the associated form element.</p>
<figure><img src="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8532d39b-6cda-46c9-a09f-ed1d2ac960d1/registration-form-02.png" alt="The label increases the hit area of the field." /><figcaption>The label increases the hit area of the field.</figcaption></figure>
<p>For these reasons, every control that accepts input should have an auxiliary <code>&lt;label&gt;</code>. Submit buttons don’t accept input, so they don’t need an auxiliary label — the <code>value</code> attribute, which renders the text inside the button, acts as the accessible label.</p>
<p>To connect an input to a label, the input’s <code>id</code> and label’s <code>for</code> attribute should match and be unique to the page. In the case of the email field, the value is &#8220;email&#8221;:</p><pre><code class=" language-markup">html
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span>"email"</span><span class="token punctuation">&gt;</span></span>Email address<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span>"email"</span><span class="token punctuation">&gt;</span></span></code></pre><p>Failing to include a label means ignoring the needs of many users, including those with physical and cognitive impairments. By focusing on the recognized barriers to people with disabilities, we can make our forms easier and more robust for everyone.</p>
<p>For example, a larger hit area is crucial for motor-impaired users, but is easier to hit for those without impairments too.</p>
<h3>Placeholders</h3>
<p>The <code>placeholder</code> attribute is intended to store a hint. It gives users extra guidance when filling out a field — particularly useful for fields that have complex rules such as a password field.</p>
<p>As placeholder text is not a real value, it’s grayed out so that it can be differentiated from user-entered values.</p>
<figure><img src="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bca59558-8b73-4465-b069-d0e192aea1be/registration-form-03.png" alt="The placeholder’s low-contrast, gray text is hard to read." /><figcaption>The placeholder’s low-contrast, gray text is hard to read.</figcaption></figure>
<p>Unlike labels, hints are optional and shouldn’t be used as a matter of course. Just because the <code>placeholder</code> attribute exists doesn’t mean we have to use it. You don’t need a placeholder of &#8220;Enter your first name&#8221; when the label is &#8220;First name&#8221; — that’s needless duplication.</p>
<figure><img src="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d688f531-2957-4c71-ab93-226bb1bb9524/registration-form-04.png" alt="The label and placeholder text have similar content, making the placeholder unnecessary." /><figcaption>The label and placeholder text have similar content, making the placeholder unnecessary.</figcaption></figure>
<p>Placeholders are appealing because of their minimal, space-saving aesthetic. This is because placeholder text is placed <em>inside</em> the field. But this is a problematic way to give users a hint.</p>
<p>First, they disappear when the user types. Disappearing text is hard to remember, which can cause errors if, for example, the user forgets to satisfy one of the password rules. Users often mistake placeholder text for a value, causing the field to be skipped, which again . And to top it off, some browsers don’t support placeholders, some screen readers don’t announce them, and long hint text may get cut off.</p>
<figure><img src="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bf77b953-5d06-4660-adaa-b3649b751192/registration-form-05.png" alt="The placeholder text is cut off as it’s wider than the text box." /><figcaption>The placeholder text is cut off as it’s wider than the text box.</figcaption></figure>
<p>That’s a lot of problems for what is essentially just text. All content, especially a form hint, shouldn’t be considered as nice to have. So instead of using placeholders, it’s better to position hint text above the control like this:</p>
<figure><img src="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f6e627df-3c68-4d75-94c4-2a2b6cf54dae/registration-form-06.png" alt="Hint text placed above the text box instead of placeholder text inside it." /><figcaption>Hint text placed above the text box instead of placeholder text inside it.</figcaption></figure><pre><code class="language-markup">&lt;div class="field"&gt;
  &lt;label for="password"&gt;
  &lt;span class="field-label"&gt;Password&lt;/span&gt;
  &lt;span class="field-hint"&gt;Must contain 8+ characters with at least 1 number and 1 uppercase letter.&lt;/span&gt;
  &lt;/label&gt;
  &lt;input type="password" id="password" name="password"&gt;
&lt;/div&gt;</code></pre>
<p>The hint is placed within the label and inside a <code>&lt;span&gt;</code> so it can be styled differently. By placing it inside the label it will be read out by screen readers, and further enlarges the hit area.</p>
<p>As with most things in design, this isn’t the only way to achieve this functionality. We could use ARIA attributes to associate the hint with the input:</p><pre><code class="language-markup">&lt;div class="field"&gt;
  &lt;label for="password"&gt;Password&lt;/label&gt;
  &lt;p class="field-hint" id="passwordhint"&gt;Must contain 8+ characters with at least 1 number and 1 uppercase letter.&lt;/p&gt;
  &lt;input type="password" id="password" name="password" aria-describedby="passwordhint"&gt;
&lt;/div&gt;</code></pre>
<p>The <code>aria-describedby</code> attribute is used to connect the hint by its <code>id</code> — just like the for attribute for labels, but in reverse. It’s appended to the control’s label and read out after a short pause. In this example, &#8220;password [pause] must contain eight plus characters with at least one number and one uppercase letter.&#8221;</p>
<p>There are other differences too. First, clicking the hint (a <code>&lt;p&gt;</code> in this case) won’t focus the control, which reduces the hit area. Second, despite ARIA’s growing support, it’s never going to be as well supported as native elements. In this particular case, :</p><blockquote><p>&#8220;If you can use a native HTML element or attribute with the semantics and behaviour you require <em>already built in</em>, instead of re-purposing an element and adding an ARIA role, state or property to make it accessible, <em>then do so</em>.&#8221;</p></blockquote><h3>Float Labels</h3>
<p>The  by Matt Smith is a technique that uses the label as a placeholder. The label starts <em>inside</em> the control, but floats above the control as the user types, hence the name. This technique is often lauded for its quirky, minimalist, and space-saving qualities.</p>
<figure><img src="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/eacf3168-04da-4053-a0cd-67b67d7988e3/registration-form-07.png" alt="The float label pattern. On the left, an unfocused text field shows the label inside; on the right, when the text field receives focus, the label moves above the field." /><figcaption>The float label pattern. On the left, an unfocused text field shows the label inside; on the right, when the text field receives focus, the label moves above the field.</figcaption></figure>
<p>Unfortunately, there are several problems with this approach. First, there is no space for a hint because the label and hint are one and the same. Second, they’re hard to read, due to their poor contrast and small text, as they’re typically designed. (Lower contrast is necessary so that users have a chance to differentiate between a real value and a placeholder.) Third, like placeholders, they may be mistaken for a value and could get cropped.</p>
<p>And float labels don’t actually save space. The label needs space to move into in the first place. Even if they did save space, that’s hardly a good reason to diminish the usability of forms.</p><blockquote><p>&#8220;Seems like a lot of effort when you could simply put labels above inputs &amp; get all the benefits/none of the issues.&#8221;<br />&mdash; </p></blockquote><p>Quirky and minimalist interfaces don’t make users feel awesome — obvious, inclusive, and robust interfaces do. Artificially reducing the height of forms like this is both uncompelling and problematic.</p>
<p>Instead, you should prioritize making room for an ever-present, readily available label (and hint if necessary) at the start of the design process. This way you won’t have to squeeze content into a small space.</p>
<p>We’ll be discussing several, less artificial techniques to reduce the size of forms shortly.</p>
<h3>The Question Protocol</h3>
<p>One powerful and <em>natural</em> way to reduce the size of a form is to use a . It helps ensure you know why you are asking every question or including a form field.</p>
<p>Does the registration form need to collect first name, last name, email address and password? Are there better or alternative ways to ask for this information that simplify the experience?</p>
<p>In all likelihood, you don’t need to ask for the user’s first and last name for them to register. If you need that information later, for whatever reason, ask for it then. By removing these fields, we can halve the size of the form. All without resorting to novel and problematic patterns.</p>
<h4>No Password Sign-In</h4>
<p>One way to avoid asking users for a password is to use the <em>no password sign-in</em> pattern. It works by making use of the security of email (which already needs a password). Users enter only their email address, and the service sends a special link to their inbox. Following it logs the user into the service immediately.</p>
<figure><img src="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/131073d9-b645-432a-b288-a70e4a551722/registration-form-08.png" alt="Medium’s passwordless sign-in screen." /><figcaption>Medium’s passwordless sign-in screen.</figcaption></figure>
<p>Not only does this reduce the size of the form to just one field, but it also saves users having to remember another password. While this simplifies the form in isolation, in other ways it adds some extra complexity for the user.</p>
<p>First, users might be less familiar with this approach, and many people are worried about online security. Second, having to move away from the app to your email account is long-winded, especially for users who know their password, or use a password manager.</p>
<p>It’s not that one technique is always better than the other. It’s that a question protocol urges us to think about this as part of the design process. Otherwise, you’d mindlessly add a password field on the form and be done with it.</p>
<h4>Passphrases</h4>
<p>Passwords are generally short, hard to remember, and easy to crack. Users often have to create a password of more than eight characters, made up of at least one uppercase and one lowercase letter, and a number. This micro-interaction is hardly ideal.</p><blockquote><p>&#8220;Sorry but your password must contain an uppercase letter, a number, a haiku, a gang sign, a hieroglyph, and the blood of a virgin.&#8221;<br />&mdash; Anonymous internet meme</p></blockquote><p>Instead of a password, we could ask users for a . A passphrase is a series of words such as &#8220;monkeysinmygarden&#8221; (sorry, that’s the first thing that comes to mind). They are generally easier to remember than passwords, and they are more secure owing to their length — passphrases must be at least 16 characters long.</p>
<p>The downside is that passphrases are less commonly used and, therefore, unfamiliar. This may cause anxiety for users who are already worried about online security.</p>
<p>Whether it’s the no password sign-in pattern or passphrases, we should only move away from convention once we’ve conducted thorough and diverse user research. You don’t want to exchange one set of problems for another unknowingly.</p>
<h3>Field Styling</h3>
<p>The way you style your form components will, at least in part, be determined by your product or company’s brand. Still, label position and focus styles are important considerations.</p>
<h4>Label Position</h4>
<p>Matteo Penzo’s .</p>
<p>Also, some labels contain a lot of text, which causes it to wrap onto multiple lines, which would disrupt the visual rhythm if placed next to the control.</p>
<p>While you should aim to keep labels terse, it’s not always possible. Using a pattern that accommodates varying content — by positioning labels above the control — is a good strategy.</p>
<h4>Look, Size, and Space</h4>
<p>Form fields should look like form fields. But what does that mean exactly?</p>
<p>It means that a text box should look like a text box. Empty boxes signify &#8220;fill me in&#8221; by virtue of being empty, like a coloring-in book. This happens to be part of the reason placeholders are unhelpful. They remove the perceived affordance an empty text box would otherwise provide.</p>
<p>This also means that the empty space should be boxed in (bordered). Removing the border, or having only a bottom border, for example, removes the perceived affordances. A bottom border might at first appear to be a separator. Even if you know you have to fill something in, does the value go above the line or below it?</p>
<p>Spatially, the label should be closest to its form control, not the previous field’s control. Things that appear close together . Having equal spacing might improve aesthetics, but it would be at the cost of usability.</p>
<p>Finally, the label and the text box itself should be large enough to read and tap. This probably means a font size of at least 16 pixels, and ideally an overall .</p>
<h4>Focus Styles</h4>
<p>Focus styles are a simpler prospect. By default, browsers put an outline around the element in focus so users, especially those who use a keyboard, know where they are. The problem with the default styling is that it is often faint and hard to see, and somewhat ugly.</p>
<p>While this is the case, don’t be tempted to remove it, because doing so will diminish the user experience greatly for those traversing the screen by keyboard. We can override the default styling to make it clearer and more aesthetically pleasing.</p>
<pre><code class="language-css">input:focus {
  outline: 4px solid #ffbf47;
}</code></pre>
<h3>The Email Field</h3>
<p>Despite its simple appearance there are some important details that have gone into the field’s construction which affect the experience.</p>
<figure><img src="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b271fada-92f1-4695-b85f-f39b21c09258/registration-form-09.png" alt="The email field." /><figcaption>The email field.</figcaption></figure>
<p>As noted earlier, some fields have a hint in addition to the label, which is why the label is inside a child span. The <code>field-label</code> class lets us style it through CSS.</p>
<pre><code class="language-markup">&lt;div class="field"&gt;
  &lt;label for="email"&gt;
  &lt;span class="field-label"&gt;Email address&lt;/span&gt;
  &lt;/label&gt;
  &lt;input type="email" id="email" name="email"&gt;
&lt;/div&gt;</code></pre>
<p>The label itself is &#8220;Email address&#8221; and uses sentence case. In &#8220;,&#8221; John Saito explains that sentence case (as opposed to title case) is generally easier to read, friendlier, and makes it easier to spot nouns. Whether you heed this advice is up to you, but whatever style you choose, be sure to use it consistently.</p>
<p>The input’s <code>type</code> attribute is set to <code>email</code>, which triggers an email-specific onscreen keyboard on mobile devices. This gives users easy access to the <code>@</code> and <code>.</code> (dot) symbols which every email address must contain.</p>
<figure><img src="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/39a4b8b4-a1b7-4130-b525-508b2d96a83b/registration-form-10.png" alt="Android’s onscreen keyboard for the email field." /><figcaption>Android’s onscreen keyboard for the email field.</figcaption></figure>
<p>People using a non-supporting browser will see a standard text input (<code>&lt;input type="text"&gt;</code>). This is a form of progressive enhancement, which is a cornerstone of designing inclusive experiences.</p>
<h4>Progressive Enhancement</h4>
<p>Progressive enhancement is about users. It just happens to make our lives as designers and developers easier too. Instead of keeping up with a set of browsers and devices (which is impossible!) we can just focus on features.</p>
<p>First and foremost, progressive enhancement is about always giving users a reasonable experience, no matter their browser, device, or quality of connection. When things go wrong — and they will — users won’t suffer in that they can still get things done.</p>
<p>There are a lot of ways an experience can go wrong. Perhaps the style sheet or script fails to load. Maybe everything loads, but the user’s browser doesn’t recognize some HTML, CSS, or JavaScript. Whatever happens, using progressive enhancement when designing experiences stops users having an especially bad time.</p>
<p>It starts with HTML for structure and content. If CSS or JavaScript don’t load, it’s fine because the content is there.</p>
<p>If everything loads OK, perhaps various HTML elements aren’t recognized. For example, some browsers don’t understand <code>&lt;input type="email"&gt;</code>. That’s fine, though, because users will get a text box (<code>&lt;input type="text"&gt;</code>) instead. Users can still enter an email address; they just don’t get an email-specific keyboard on mobile.</p>
<p>Maybe the browser doesn’t understand some fancy CSS, and it will just ignore it. In most cases, this isn’t a problem. Let’s say you have a button with <code>border-radius: 10px</code>. Browsers that don’t recognize this rule will show a button with angled corners. Arguably, the button’s perceived affordance is reduced, but users are left unharmed. In other cases it might be helpful to use .</p>
<p>Then there is JavaScript, which is more complicated. When the browser tries to parse methods it doesn’t recognize, it will throw a hissy fit. This can cause your other (valid and supported) scripts to fail. If your script doesn’t first check that the methods exist (feature detection) and work (feature testing) before using them, then users may get a broken interface. For example, if a button’s click handler calls a method that’s not recognized, the button won’t work. That’s bad.</p>
<p>That’s how you enhance. But what’s better is not needing an enhancement at all. HTML with a little CSS can give users an excellent experience. It’s the content that counts and you don’t need JavaScript for that. The more you can rely on content (HTML) and style (CSS), the better. I can’t emphasize this enough: so often, the basic experience is the best and . There’s no point in enhancing something if it doesn’t <em>add value</em> (see inclusive design principle 7).</p>
<p>Of course, there are times when the basic experience isn’t as good as it could be — that’s when it’s time to enhance. But if we follow the approach above, when a piece of CSS or JavaScript isn’t recognized or executed, things will still work.</p>
<p>Progressive enhancement makes us think about what happens when things fail. It allows us to build experiences with resilience baked in. But equally, it makes us think about whether an enhancement is needed at all; and if it is, how best to go about it.</p>
<h3>The Password Field</h3>
<p>We’re using the same markup as the email field discussed earlier. If you’re using a template language, you’ll be able to create a component that accommodates both types of field. This helps to enforce inclusive design principle 3, <em>be consistent</em>.</p>
<figure><img src="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c5f821e5-5b50-491f-bfa6-c571195a23c7/registration-form-11.png" alt="The password field using the hint text pattern." /><figcaption>The password field using the hint text pattern.</figcaption></figure>
<pre><code class="language-markup">&lt;div class="field"&gt;
  &lt;label for="password"&gt;
    &lt;span class="field-label"&gt;Choose password&lt;/span&gt;
    &lt;span class="field-hint"&gt;Must contain 8+ characters with at least 1 number and 1 uppercase letter.&lt;/span&gt;
  &lt;/label&gt;
  &lt;input type="password" id="password" name="password"&gt;
&lt;/div&gt;</code></pre>
<p>The password field contains a hint. Without one, users won’t understand the requirements, which is likely to cause an error once they try to proceed.</p>
<p>The <code>type="password"</code> attribute masks the input’s value by replacing what the user types with small black dots. This is a security measure that stops people seeing what you typed if they happen to be close by.</p>
<h4>A Password Reveal</h4>
<p>Obscuring the value as the user types makes it hard to fix typos. So when one is made, it’s often easier to delete the whole entry and start again. This is frustrating as most users aren’t using a computer with a person looking over their shoulder.</p>
<p>Owing to the increased risk of typos, some registration forms include an additional &#8220;Confirm password&#8221; field. This is a precautionary measure that requires the user to type the same password twice, doubling the effort and degrading the user experience. Instead, it’s better to let users reveal their password, which speaks to principles 4 and 5, <em>give control</em> and <em>offer choice</em> respectively. This way users can choose to reveal their password when they know nobody is looking, reducing the risk of typos.</p>
<p>Recent versions of Internet Explorer and Microsoft Edge provide this behavior natively. As we’ll be creating our own solution, we should suppress this feature using CSS like this:</p>
<pre><code class="language-css">input[type=password]::-ms-reveal {
  display: none;
}</code></pre>
<figure><img src="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e66769f9-2b29-4437-91ea-0df221c9d1fe/registration-form-12.png" alt="The password field with a &#8220;Show password&#8221; button beside it." /><figcaption>The password field with a &#8220;Show password&#8221; button beside it.</figcaption></figure>
<p>First, we need to inject a button next to the input. The <code>&lt;button&gt;</code> element should be your go-to element for changing anything with JavaScript — except, that is, for changing location, which is what links are for. When clicked, it should toggle the type attribute between <code>password</code> and <code>text</code>; and the button’s label between &#8220;Show&#8221; and &#8220;Hide.&#8221;</p>
<pre><code class="language-javascript">function PasswordReveal(input) {
  // store input as a property of the instance
  // so that it can be referenced in methods
  // on the prototype
  this.input = input;
  this.createButton();
};

PasswordReveal.prototype.createButton = function() {
  // create a button
  this.button = $('&lt;button type="button"&gt;Show password&lt;/button&gt;');
  // inject button
  $(this.input).parent().append(this.button);
  // listen to the button’s click event
  this.button.on('click', $.proxy(this, 'onButtonClick'));
};

PasswordReveal.prototype.onButtonClick = function(e) {
  // Toggle input type and button text
  if(this.input.type === 'password') {
    this.input.type = 'text';
    this.button.text('Hide password');
  } else {
    this.input.type = 'password';
    this.button.text('Show password');
  }
};</code></pre>
<h5>JavaScript Syntax and Architectural Notes</h5>
<p>As there are many flavors of JavaScript, and different ways in which to architect components, we’re going to walk through the choices used to construct the password reveal component, and all the upcoming components in the book.</p>
<p>First, we’re using a constructor. A constructor is a function conventionally written in upper camel case — <code>PasswordReveal</code>, not <code>passwordReveal</code>. It’s initialized using the <code>new</code> keyword, which lets us use the same code to create several instances of the component:</p>
<pre><code class="language-javascript">var passwordReveal1 = new PasswordReveal(document.getElementById('input1'));

var passwordReveal2 = new PasswordReveal(document.getElementById('input2'));</code></pre>
<p>Second, the component’s methods are defined on the prototype — for example, <code>PasswordReveal.prototype.onButtonClick</code>. The prototype is the most performant way to share methods across multiple instances of the same component.</p>
<p>Third, jQuery is being used to create and retrieve elements, and listen to events. While jQuery may not be necessary or preferred, using it means that this book can focus on forms and not on the complexities of cross-browser components.</p>
<p>If you’re a designer who codes a little bit, then jQuery’s ubiquity and low-barrier to entry should be helpful. By the same token, if you prefer not to use jQuery, you’ll have no trouble refactoring the components to suit your preference.</p>
<p>You may have also noticed the use of the <code>$.proxy</code> function. This is jQuery’s implementation of <code>Function.prototype.bind</code>. If we didn’t use this function to listen to events, then the event handler would be called in the element’s context (<code>this</code>). In the example above, <code>this.button</code> would be undefined. But we want <code>this</code> to be the password reveal object instead, so that we can access its properties and methods.</p>
<h5>Alternative Interface Options</h5>
<p>The password reveal interface we constructed above toggles the button’s label between &#8220;Show password&#8221; and &#8220;Hide password.&#8221; Some screen reader users can get confused when the button’s label is changed; once a user encounters a button, they expect that button to persist. Even though the button <em>is</em> persistent, changing the label makes it appear not to be.</p>
<p>If your research shows this to be a problem, you could try two alternative approaches.</p>
<p>First, use a checkbox with a persistent label of &#8220;Show password.&#8221; The state will be signaled by the <code>checked</code> attribute. Screen reader users will hear &#8220;Show password, checkbox, checked&#8221; (or similar). Sighted users will see the checkbox tick mark. The problem with this approach is that checkboxes are for inputting data, not controlling the interface. Some users might think their password will be revealed to the system.</p>
<p>Or, second, change the button’s <code>state</code> — not the label. To convey the state to screen reader users, you can switch the <code>aria-pressed</code> attribute between <code>true</code> (pressed) and <code>false</code> (unpressed).</p>
<pre><code class="language-markup">&lt;button type="button" aria-pressed="true"&gt;  
  Show password
&lt;/button&gt;</code></pre>
<p>When focusing the button, screen readers will announce, &#8220;Show password, toggle button, pressed&#8221; (or similar). For sighted users, you can style the button to look pressed or unpressed accordingly using the attribute selector like this:</p>
<pre><code class="language-css">[aria-pressed="true"] {
  box-shadow: inset 0 0 0 0.15rem #000, inset 0.25em 0.25em 0 #fff;
}</code></pre>
<p>Just be sure that the unpressed and pressed styles are obvious and differentiated, otherwise sighted users may struggle to tell the difference between them.</p>
<h4>Microcopy</h4>
<p>The label is set to &#8220;Choose password&#8221; rather than &#8220;Password.&#8221; The latter is somewhat confusing and could prompt the user to type a password they already possess, which could be a security issue. More subtly, it might suggest the user is already registered, causing users with cognitive impairments to think they are logging in instead.</p>
<p>Where &#8220;Password&#8221; is ambiguous, &#8220;Choose password&#8221; provides clarity.</p>
<h3>Button Styles</h3>
<p>What’s a button? We refer to many different types of components on a web page as a button. In fact, I’ve already covered two different types of button without calling them out. Let’s do that now.</p>
<p>Buttons that submit forms are &#8220;submit buttons&#8221; and they are coded typically as either <code>&lt;input type="submit"&gt;</code> or <code>&lt;button type="submit"&gt;</code>. The <code>&lt;button&gt;</code> element is more malleable in that you can nest other elements inside it. But there’s rarely a need for that. Most submit buttons contain just text.</p><p><em>Note:</em> In older versions of Internet Explorer, if you have multiple <code>&lt;button type="submit"&gt;</code>s, the form will  to the server, regardless of which was clicked. You’ll need to know which button was clicked so you can determine the right course of action to take, which is why this element should be avoided.</p><p>Other buttons are injected into the interface to enhance the experience with JavaScript — much like we did with the password reveal component discussed earlier. That was also a <code>&lt;button&gt;</code> but its <code>type</code> was set to <code>button</code> (not <code>submit</code>).</p>
<p>In both cases, the first thing to know about buttons is that they aren’t links. Links are typically underlined (by user agent styles) or specially positioned (in a navigation bar) so they are distinguishable among regular text. When hovering over a link, the cursor will change to a pointer. This is because, unlike buttons, links have weak .</p>
<p>In <em></em>, Jeremy Keith discusses the idea of material honesty. He says: &#8220;One material should not be used as a substitute for another. Otherwise the end result is deceptive.&#8221; Making a link look like a button is materially dishonest. It tells users that links and buttons are the same when they’re not.</p>
<p>Links can do things buttons can’t do. Links can be opened in a new tab or bookmarked for later, for example. Therefore, buttons shouldn’t look like links, nor should they have a pointer cursor. Instead, we should make buttons look like buttons, which have naturally strong perceived affordance. Whether they have rounded corners, drop shadows, and borders is up to you, but they should look like buttons regardless.</p>
<p>Buttons can still give feedback on hover (and on focus) by changing the background colour, for example.</p>
<h4>Placement</h4>
<p>Submit buttons are typically placed at the bottom of the form: with most forms, users fill out the fields from top to bottom, and then submit. But should the button be aligned left, right or center? To answer this question, we need to think about where users will naturally look for it.</p>
<p>Field labels and form controls are aligned left (in left-to-right reading languages) and run from top to bottom. Users are going to look for the next field below the last one. Naturally, then, the submit button should also be positioned in that location: to the left and directly below the last field. This also helps users who zoom in, as a right-aligned button could more easily disappear off-screen.</p>
<h4>Text</h4>
<p>The button’s text is just as important as its styling. The text should explicitly describe the action being taken. And because it’s an action, it should be a verb. We should aim to use as few words as possible because it’s quicker to read. But we shouldn’t remove words at the cost of clarity.</p>
<p>The exact words can match your brand’s tone of voice, but don’t exchange clarity for quirkiness.</p>
<p>Simple and plain language is easy for everyone to understand. The exact words will depend on the type of service. For our registration form &#8220;Register&#8221; is fine, but depending on your service &#8220;Join&#8221; or &#8220;Sign up&#8221; might be more appropriate.</p>
<h3>Validation</h3>
<p>Despite our efforts to create an inclusive, simple, and friction-free registration experience, we can’t eliminate human error. People make mistakes and when they do, we should make fixing them as easy as possible.</p>
<p>When it comes to form validation, there are a number of important details to consider. From choosing when to give feedback, through to how to display that feedback, down to the formulation of a good error message — all of these things need to be taken into account.</p>
<h4>HTML5 Validation</h4>
<p>HTML5 validation has been around for a while now. By adding just a few HTML attributes, supporting browsers will mark erroneous fields when the form is submitted. Non-supporting browsers fall back to server-side validation.</p>
<p>Normally I would recommend using functionality that the browser provides for free because it’s often more performant, robust, and accessible. Not to mention, it becomes more familiar to users as more sites start to use the standard functionality.</p>
<p>While  is quite good, it’s not implemented uniformly. For example, the required attribute can mark fields as invalid from the outset, which isn’t desirable. Some browsers, such as Firefox 45.7, will show an error of &#8220;Please enter an email address&#8221; even if the user entered something in the box, whereas Chrome, for example, says &#8220;Please include an &#8216;@’ in the email address,&#8221; which is more helpful.</p>
<p>We also want to give users the same interface whether errors are caught on the server or the client. For these reasons we’ll design our own solution. The first thing to do is turn off HTML5 validation: <code>&lt;form novalidate&gt;</code></p>
<h4>Handling Submission</h4>
<p>When the user submits the form, we need to check if there are errors. If there are, we need to prevent the form from submitting the details to the server.</p>
<pre><code class="language-javascript">function FormValidator(form) {
  form.on('submit', $.proxy(this, 'onSubmit'));
}

FormValidator.prototype.onSubmit = function(e) {
  if(!this.validate()) {
    e.preventDefault();
    // show errors
  }
};</code></pre>
<p>Note that we are listening to the form’s submit event, not the button’s click event. The latter will stop users being able to submit the form by pressing <strong>Enter</strong> when focus is within one of the fields. This is also known as <em></em>.</p>
<h4>Displaying Feedback</h4>
<p>It’s all very well detecting the presence of errors, but at this point users are none the wiser. There are three disparate parts of the interface that need to be updated. We’ll talk about each of those now.</p>
<h5>Document Title</h5>
<p>The document’s <code>&lt;title&gt;</code> is the first part of a web page to be read out by screen readers. As such, we can use it to quickly inform users that something has gone wrong with their submission. This is especially useful when the page reloads after a server request.</p>
<p>Even though we’re enhancing the user experience by catching errors on the client with JavaScript, not all errors can be caught this way. For example, checking that an email address hasn’t already been taken can only be checked on the server. And in any case, JavaScript is prone to failure so we .</p>
<p>Where the original page title might read &#8220;Register for [service],&#8221; on error it should read &#8220;(2 errors) Register for [service]&#8221; (or similar). The exact wording is somewhat down to opinion.</p>
<p>The following JavaScript updates the title:</p>
<pre><code class="language-javascript">document.title = "(" + this.errors.length + ")" + document.title;</code></pre>
<p>As noted above, this is primarily for screen reader users, but as is often the case with inclusive design, what helps one set of users helps everyone else too. This time, the updated title acts as a notification in the tab.</p>
<figure><img src="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/38b27454-2ebc-473e-ac73-303755289e53/registration-form-13.png" alt="The browser tab title prefixed with &#8220;(2 errors)&#8221; acting as a quasi notification." /><figcaption>The browser tab title prefixed with &#8220;(2 errors)&#8221; acting as a quasi notification.</figcaption></figure><h5>Error Summary</h5>
<p>In comparison with the title element, the error summary is more prominent, which tells sighted users that something has gone wrong. But it’s also responsible for letting users understand what’s gone wrong and how to fix it.</p>
<p>It’s positioned at the top of the page so users don’t have to scroll down to see it after a page refresh (should an error get caught on the server). Conventionally, errors are colored red. However, relying on color alone could exclude colorblind users. To draw attention to the summary, consider also using position, size, text, and iconography.</p>
<figure><img src="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d472b0d9-f291-4db0-908a-6206fb15b74e/registration-form-14.png" alt="Error summary panel positioned toward the top of the screen." /><figcaption>Error summary panel positioned toward the top of the screen.</figcaption></figure>
<p>The panel includes a heading, &#8220;There’s a problem,&#8221; to indicate the issue. Notice it doesn’t say the word &#8220;Error,&#8221; which isn’t very friendly. Imagine you were filling out your details to purchase a car in a showroom and made a mistake. The salesperson wouldn’t say &#8220;Error&#8221; — in fact it would be odd if they did say that.</p>
<pre><code class="language-markup">&lt;div class="errorSummary" role="group" tabindex="-1" aria-labelledby="errorSummary-heading"&gt;
  &lt;h2 id="errorSummary-heading"&gt;There’s a problem&lt;/h2&gt;
  &lt;ul&gt;
    &lt;li&gt;&lt;a href="#emailaddress"&gt;Enter an email address&lt;/a&gt;&lt;/li&gt;
    &lt;li&gt;&lt;a href="#password"&gt;The password must contain an uppercase letter&lt;/a&gt;&lt;/li&gt;
  &lt;/ul&gt;
&lt;/div&gt;</code></pre>
<p>The container has a <code>role</code> of <code>group</code>, which is used to group a set of interface elements: in this case, the heading and the error links. The <code>tabindex</code> attribute is set to <code>-1</code>, so it can be focused programmatically with JavaScript (when the form is submitted with mistakes). This ensures the error summary panel is scrolled into view. Otherwise, the interface would appear unresponsive and broken when submitted.</p><p><em>Note:</em> Using <code>tabindex="0"</code> means it will be permanently focusable by way of the <strong>Tab</strong> key, which is a 2.4.3 Focus Order WCAG fail. If users can tab to something, they expect it will actually do something.</p>
<pre><code class="language-javascript">FormValidator.prototype.showSummary = function () {
  // ...
  this.summary.focus();
};</code></pre>
<p>Underneath, there’s a list of error links. Clicking a link will set focus to the erroneous field, which lets users jump into the form quickly. The link’s <code>href</code> attribute is set to the control’s id, which in some browsers is enough to set focus to it. However, in other browsers, clicking the link will just scroll the input into view, without focusing it. To fix this we can focus the input explicitly.</p>
<pre><code class="language-javascript">FormValidator.prototype.onErrorClick = function(e) {
  e.preventDefault();
  var href = e.target.href;
  var id = href.substring(href.indexOf("#"), href.length);
  $(id).focus();
};</code></pre>
<p>When there aren’t any errors, the summary panel should be hidden. This ensures that there is only ever one summary panel on the page, and that it appears consistently in the same location whether errors are rendered by the client or the server. To hide the panel we need to add a class of <code>hidden</code>.</p>
<pre><code class="language-markup">&lt;div class="errorSummary hidden" ...&gt;&lt;/div&gt;</code></pre>
<pre><code class="language-css">.hidden {
  display: none;
}</code></pre>
<p><em>Note:</em> You could use the <code>hidden</code> attribute/property to toggle an element’s visibility, but there’s less support for it. Inclusive design is about making decisions that you know are unlikely to exclude people. Using a class aligns with this philosophy.</p>
<h5>Inline Errors</h5>
<p>We need to put the relevant error message just above the field. This saves users scrolling up and down the page to check the error message, and keeps them moving down the form. If the message was placed below the field, we’d  by the browser autocomplete panel or by the onscreen keyboard.</p>
<figure><img src="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c13c3438-4e52-45c7-8971-a7228dcc6347/registration-form-15.png" alt="Inline error pattern with red error text and warning icon just above the field." /><figcaption>Inline error pattern with red error text and warning icon just above the field.</figcaption></figure>
<pre><code class="language-markup">&lt;div class="field"&gt;
  &lt;label for="blah"&gt;
    &lt;span class="field-error"&gt;
    &lt;svg width="1.5em" height="1.5em"&gt;&lt;use xmlns:xlink="http://www.w3.org/1999/xlink" xlink:href="#warning-icon"&gt;&lt;/use&gt;&lt;/svg&gt;
    Enter your email address.
    &lt;/span&gt;
    &lt;span class="field-error"&gt;Enter an email address&lt;/span&gt;
  &lt;/label&gt;
&lt;/div&gt;</code></pre>
<p>Like the hint pattern mentioned earlier, the error message is injected inside the label. When the field is focused, screen reader users will hear the message in context, so they can freely move through the form without having to refer to the summary.</p>
<p>The error message is red and uses an SVG warning icon to draw users’ attention. If we’d used only a color change to denote an error, this would exclude color-blind users. So this works really well for sighted users — but what about screen reader users?</p>
<p>To give both sighted and non-sighted users an equivalent experience, we can use the well-supported <code>aria-invalid</code> attribute. When the user focuses the input, it will now announce &#8220;Invalid&#8221; (or similar) in screen readers.</p>
<pre><code class="language-markup">&lt;input aria-invalid="false"&gt;</code></pre>
<p><em>Note:</em> The registration form only consists of text inputs. In chapter 3, &#8220;A Flight Booking Form,&#8221; we’ll look at how to inject errors accessibly for groups of fields such as radio buttons.</p>
<h4>Submitting the Form Again</h4>
<p>When submitting the form for a second time, we need to clear the existing errors from view. Otherwise, users may see duplicate errors.</p>
<pre><code class="language-javascript">FormValidator.prototype.onSubmit = function(e) {
  this.resetPageTitle();
  this.resetSummaryPanel();
  this.removeInlineErrors();
  if(!this.validate()) {
    e.preventDefault();
    this.updatePageTitle();
    this.showSummaryPanel();
    this.showInlineErrors();
  }
};</code></pre>
<h4>Initialization</h4>
<p>Having finished defining the <code>FormValidator</code> component, we’re now ready to initialize it. To create an instance of <code>FormValidator</code>, you need to pass the form element as the first parameter.</p>
<pre><code class="language-javascript">var validator = new FormValidator(document.getElementById('registration'));</code></pre>
<p>To validate the email field, for example, call the <code>addValidator()</code> method:</p>
<pre><code class="language-javascript">validator.addValidator('email', [{
  method: function(field) {
    return field.value.trim().length > 0;
  },
  message: 'Enter your email address.'
},{
  method: function(field) {
    return (field.value.indexOf('@') > -1);
  },
  message: 'Enter the &#8216;at’ symbol in the email address.'
}]);</code></pre>
<p>The first parameter is the control’s <code>name</code>, and the second is an array of rule objects. Each rule contains two properties: <code>method</code> and <code>message</code>. The <code>method</code> is a function that tests various conditions to return either <code>true</code> or <code>false</code>. False puts the field into an error state, which is used to populate the interface with errors as discussed earlier.</p>
<h5>Forgiving Trivial Mistakes</h5>
<p>In <em>The Design of Everyday Things</em>, Don Norman talks about designing for error. He talks about the way people converse:</p><blockquote><p>&#8220;If a person says something that we believe to be false, we question and debate. We don’t issue a warning signal. We don’t beep. We don’t give error messages. [&hellip;] In normal conversations between two friends, misstatements are taken as normal, as approximations to what was really meant.&#8221;</p></blockquote><p>Unlike humans, machines are not intelligent enough to determine the meaning of most actions, but they are often far less forgiving of mistakes than they need to be. Jared Spool makes a joke about this in &#8220;&#8221; (about 42 minutes in):</p><blockquote><p>&#8220;It takes one line of code to take a phone number and strip out all the dashes and parentheses and spaces, and it takes ten lines of code to write an error message that you left them in.&#8221;</p></blockquote><p>The <code>addValidator</code> method (shown above) demonstrates how to design validation rules so they forgive trivial mistakes. The first rule, for example, trims the value before checking its length, reducing the burden on the user.</p>
<h4>Live Inline Validation</h4>
<p>Live inline validation gives users feedback as they type or when they leave the field (<code>onblur</code>). There’s some evidence to show that  and decreases completion times in long forms. This is partially to do with giving users feedback when the field’s requirements are fresh in users’ minds. But live inline validation (or live validation for short) poses several problems.</p>
<p>For entries that require a certain number of characters, the first keystroke will always constitute an invalid entry. This means users will be interrupted early, which can cause them to switch mental contexts, from entering information to fixing it.</p>
<p>Alternatively, we could wait until the user enters enough characters before showing an error. But this means users only get feedback after they have entered a correct value, which is somewhat pointless.</p>
<p>We could wait until the user leaves the field (<code>onblur</code>), but this is too late as the user has mentally prepared for (and often started to type in) the next field. Moreover, some users switch windows or use a password manager when using a form. Doing so will trigger the blur event, causing an error to show before the user is finished. All very frustrating.</p>
<p>Remember, there’s no problem with giving users feedback without a page refresh. Nor is there a problem with putting the error messages inline (next to fields) — we’ve done this already. The problem with live feedback is that it interrupts users either too early or too late, which often results in a jarring experience.</p>
<p>If users are seeing errors often, there’s probably something wrong elsewhere. Focus on shortening your form and providing better guidance (good labeling and hint text). This way users shouldn’t see more than the odd error. We’ll look at longer forms in the next chapter.</p>
<h4>Checklist Affirmation Pattern</h4>
<p>A variation of live validation involves ticking off rules (marking them as complete) as the user types. This is less invasive than live validation but isn’t suited to every type of field. Here’s an example of MailChimp’s sign-up form, which employs this technique for the password field.</p>
<figure><img src="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4354b784-5c1d-4531-96eb-f049cc394504/registration-form-16.png" alt="MailChimp’s password field with instructions that get marked as the user meets the requirements." /><figcaption>MailChimp’s password field with instructions that get marked as the user meets the requirements.</figcaption></figure>
<p>You should put the rules above the field. Otherwise the onscreen keyboard could obscure the feedback. As a result, users may stop typing and hide the keyboard to then check the feedback.</p>
<h4>A Note on Disabling Submit Buttons</h4>
<p>Some forms are designed to disable the submit button until all the fields become valid. There are several problems with this.</p>
<p>First, users are left wondering what’s actually wrong with their entries. Second, disabled buttons are not focusable, which makes it hard for the button to be discovered by blind users navigating using the <strong>Tab</strong> key. Third, disabled buttons are hard to read as they are grayed out.</p>
<p>As we’re providing users with clear feedback, when the user expects it, there’s no good reason to take control away from the user by disabling the button anyway.</p>
<h4>Crafting a Good Error Message</h4>
<p>There’s nothing more important than content. Users don’t come to your website to enjoy the design. They come to enjoy the content or the outcome of using a service.</p>
<p>Even the most thought out, inclusive and beautifully designed experience counts for nothing if we ignore the words used to craft error messages. One study showed that  &#8220;content and design are inseparable work partners.&#8221;</p>
<p>We’re showing messages in the summary at the top of the screen and next to the fields. Maintaining two versions of the same message is a hard sell for an unconvincing gain. Instead, design an error message that works in both places. &#8220;Enter an &#8216;at’ symbol&#8221; needs context from the field label to make sense. &#8220;Your email address needs an &#8216;at’ symbol&#8221; works well in both places.</p>
<p>Avoid pleasantries, like starting each error message with &#8220;Please.&#8221; On the one hand, this seems polite; on the other, it gets in the way and implies a choice.</p>
<p>Whatever approach you take, there’s going to be some repetition due to the nature of the content. And testing usually involves submitting the form without entering any information at all. This makes the repetition glaringly obvious, which may cause us to flip out. But how often is this the case? Most users aren’t trying to break the interface.</p>
<figure><img src="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/29a29045-3634-435c-949d-15a96da99b9d/registration-form-17.png" alt="An error summary containing a wall of error messages makes the beginning of the words seem too repetitive." /><figcaption>An error summary containing a wall of error messages makes the beginning of the words seem too repetitive.</figcaption></figure>
<p>Different errors require different formatting. Instructions like &#8220;Enter your first name&#8221; are natural. But &#8220;Enter a first name that is 35 characters or less&#8221; is longer, wordier, and less natural than a description like &#8220;First name must be 35 characters or less.&#8221;</p>
<p>Here’s a checklist:</p>
<ul>
<li><strong>Be concise.</strong> Don’t use more words than are necessary, but don’t omit words at the cost of clarity.</li>
<li><strong>Be consistent.</strong> Use the same tone, the same words, and the same punctuation throughout.</li>
<li><strong>Be specific.</strong> If you know why something has gone wrong, say so. &#8220;The email is invalid.&#8221; is ambiguous and puts the burden on the user. &#8220;The email needs an &#8216;at’ symbol&#8221; is clear.</li>
<li><strong>Be human, avoid jargon.</strong> Don’t use words like invalid, forbidden, and mandatory.</li>
<li><strong>Use plain language.</strong> Error messages are not an opportunity to promote your brand’s humorous tone of voice.</li>
<li><strong>Use the active voice.</strong> When an error is an instruction and you tell the user what to do. For example, &#8220;Enter your name,&#8221; not &#8220;First name must be entered.&#8221;</li>
<li><strong>Don’t blame the user.</strong> Let them know what’s gone wrong and how to fix it.</li>
</ul>
<h3>Summary</h3>
<p>In this chapter we solved several fundamental form design challenges that are applicable well beyond a simple registration form. In many respects, this chapter has been as much about what not to do, as it has about what we should. By avoiding novel and artificial space-saving patterns to focus on reducing the number of fields we include, we avoid several usability failures while simultaneously making forms more pleasant.</p>
<h4>Things to Avoid</h4>
<ul>
<li>Using the <code>placeholder</code> attribute as a mechanism for storing label and hint text.</li>
<li>Using incorrect input types.</li>
<li>Styling buttons and links the same.</li>
<li>Validating fields as users type.</li>
<li>Disabling submit buttons.</li>
<li>Using complex jargon and brand-influenced microcopy.</li>
</ul>
</ul>

<p style="border-top: 6px solid #ddd;padding-top: 2em;">And that’s it. If you liked this first chapter of the <em>Form Design Patterns</em>, you can  right away. <em>Happy reading!</em></p>

<figure id="get-the-book" class="article__image smb6__release">
  <a href="https://res.cloudinary.com/indysigner/image/upload/v1538656288/form-design-patterns-wooden-large_bqhcoq.jpg">
    <img style="border-radius: 11px" src="https://res.cloudinary.com/indysigner/image/upload/v1538399913/form-design-patterns-wooden-800_oxm2w5.jpg" sizes="100%" alt="The Form Design Patterns book is a hardcover book with a yellow cover and black text on it">
  </a>
</figure>

<p><div style="border-bottom: 6px solid #ddd;padding-bottom: 1em;" class="book-cta" data-handler="ContentTabs" data-mq="(max-width: 480px)">
  <nav class="content-tabs content-tabs--books">
  <ul>
     <li class="content-tab">
     <button class="btn btn--small btn--white btn--white--bordered">eBook</button>
     </li>
     <li class="content-tab">
     <button class="btn btn--small btn--white btn--white--bordered">Hardcover</button>
     </li>
   </ul>
 </nav>
   <div class="book-cta__col book-cta__hardcover content-tab--content">
  <h3 class="book-cta__title"><span>eBook</span></h3><span class="book-cta__price">$10 <del style="font-size: 0.6em;color:#999;"><span title="Original Price" style="text-decoration: through; color: #757575; font-weight: normal; font-family: 'Mija',Arial,sans-serif;">$19</del></span><a class="btn btn--full btn--large" 
    href="/ebooks/form-design-patterns-ebook/"
    data-product-path="/ebooks/form-design-patterns-ebook/" 
    data-product-sku="form-design-patterns-ebook" 
    data-component="AddToCart" 
  style="text-shadow: 1px 1px 1px rgba(0,0,0,.3);">Get the eBook</a>
  <p class="book-cta__desc">PDF, ePUB, Kindle. Free for .</p>
    </div>
<div class="book-cta__col book-cta__ebook content-tab--content">
  <h3 class="book-cta__title"><span>Hardcover</span></h3><span class="book-cta__price"><span class="green">$29</span> <del style="font-size: 0.6em;color:#999;"><span title="Original Price" style="text-decoration: through; color: #757575; font-weight: normal; font-family: 'Mija',Arial,sans-serif;">$39</del></span><a class="btn btn--full btn--large btn--green" 
    href="/printed-books/form-design-patterns/"
    data-product-sku="form-design-patterns"
    data-product-path="/printed-books/form-design-patterns/"
    data-component="AddToCart" 
    style="text-shadow: 1px 1px 1px rgba(0,0,0,.3);">Get the Print (incl.&nbsp;eBook)</a>
  <p class="book-cta__desc">Printed, quality hardcover. Free airmail shipping worldwide.</p>
  </div>
</div>
<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(cm)</span>
</div>
</p>

              </article>
            </body>
          </html>
---------------
<h1 id="#title_3" >4、文章： Scrum丰田之道</h1>
Nigel Thurlow, Ben Linders
[http://www.infoq.com/cn/articles/scrum-the-toyota-way?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/scrum-the-toyota-way?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/scrum-the-toyota-way/zh/smallimage/toyota-connected-s-1537890707655-1538882959183.jpg"/><p>Toyota Connected使用Scrum和丰田生产系统来实现精益生产，使团队能够快速交付PDCA周期。Scrum of Scrums、Meta Scrum和首席产品所有者是其中一些针对多个团队和产品扩展Scrum的方法。敏捷不是目标。它是一个结果，一种成果。</p> <i>By Nigel Thurlow, Ben Linders</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_4" >5、文章： 2018年夏加密数字化货币现状（下）</h1>
Adam Taché
[http://www.infoq.com/cn/articles/state-of-cryptocurrencies-summer-2018-part3?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/state-of-cryptocurrencies-summer-2018-part3?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/state-of-cryptocurrencies-summer-2018-part3/zh/smallimage/logo-8-1524683952703-1538906899379.jpeg"/><p>本文将全面概述2018年夏季加密货币生态系统的当前状态，主要包括对当前和即将推出的顶级项目的大致介绍和讨论：比特币、比特币现金、Chia、Decred、智能合约平台、隐私类数字化货币和稳定币。本篇为下篇，将介绍隐私类数字化货币(Zcash、Monero、Grin/MimbleWimble、Mobilecoin)和稳定币(MakerDAO、Basis)。</p> <i>By Adam Taché</i> <i> Translated by 冬雨</i>
---------------
<h1 id="#title_5" >6、文章： Kubernetes上的十大应用程序</h1>
kubedex
[http://www.infoq.com/cn/articles/top-10-Kubernetes-applications?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/top-10-Kubernetes-applications?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/top-10-Kubernetes-applications/zh/smallimage/logo-java-1538908212361.jpeg"/><p>Kubernetes是最为流行的容器管理和编排平台，本文总结了Kubernetes集群中经常用到的应用程序及其用途。</p> <i>By kubedex</i> <i> Translated by 张卫滨 </i>
---------------
<h1 id="#title_6" >7、Meet “Form Design Patterns,” Our New Book On Accessible Web Forms — Now Shipping!</h1>
Markus Seyfferth
[https://www.smashingmagazine.com/2018/10/form-design-patterns-release/](https://www.smashingmagazine.com/2018/10/form-design-patterns-release/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/10/form-design-patterns-release/" />
              <title>Meet “Form Design Patterns,” Our New Book On Accessible Web Forms — Now Shipping!</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>Meet “Form Design Patterns,” Our New Book On Accessible Web Forms — Now Shipping!</h1>
                  
                    
                    <address>Markus Seyfferth</address>
                  
                  <time datetime="2018-10-10T13:45:00&#43;02:00" class="op-published">2018-10-10T13:45:00+02:00</time>
                  <time datetime="2018-10-10T12:57:45&#43;00:00" class="op-modified">2018-10-10T12:57:45+00:00</time>
                </header>
                

<p>Forms. It&rsquo;s no coincidence that the word rhymes with “yawns” — web forms are dull to code and even duller for your visitors to fill in. But without forms, the web would just be a library. They let us comment, collect, book, buy, share, and a host of other verbs. And mostly they enable us to do these things in an awkward, opaque, confusing, odd, frustrating, alarming, or alienating way. Forms are such an important part of the web, but we design them poorly all the time. When they&rsquo;re not over-engineered they&rsquo;re usually not engineered at all.</p>

<p>With the new <em>Form Design Patterns</em> book we want to tackle this problem. By going through common real-world problems step by step, you’ll learn how to design simple, <strong>robust</strong>, <strong>lightweight</strong>, responsive, <strong>accessible</strong>, <strong>progressively enhanced</strong>, interoperable and intuitive forms that let users get stuff done no matter what. And by the end of the book you’ll have a close-to exhaustive list of components delivered as a design system that you can use immediately in your own projects. ()</p>

<figure id="get-the-book" class="article__image smb6__release">
    <a href="https://res.cloudinary.com/indysigner/image/upload/v1538656288/form-design-patterns-wooden-large_bqhcoq.jpg">
        <img style="border-radius: 11px" src="https://res.cloudinary.com/indysigner/image/upload/v1538399913/form-design-patterns-wooden-800_oxm2w5.jpg" sizes="100%" alt="Form Design Patterns, our new book on accessible and well-designed web forms.">
    </a>
</figure>

<div class="book-cta" data-handler="ContentTabs" data-mq="(max-width: 480px)">
  <nav class="content-tabs content-tabs--books">
  <ul>
     <li class="content-tab">
     <button class="btn btn--small btn--white btn--white--bordered">eBook</button>
     </li>
     <li class="content-tab">
     <button class="btn btn--small btn--white btn--white--bordered">Hardcover</button>
     </li>
   </ul>
 </nav>
   <div class="book-cta__col book-cta__hardcover content-tab--content">
  <h3 class="book-cta__title"><span>eBook</span></h3><span class="book-cta__price">$10 <del style="font-size: 0.6em;color:#999;"><span title="Original Price" style="text-decoration: through; color: #757575; font-weight: normal; font-family: 'Mija',Arial,sans-serif;">$19</del></span><a class="btn btn--full btn--large" 
    href="/ebooks/form-design-patterns-ebook/"
    data-product-path="/ebooks/form-design-patterns-ebook/" 
    data-product-sku="form-design-patterns-ebook" 
    data-component="AddToCart" 
  style="text-shadow: 1px 1px 1px rgba(0,0,0,.3);">Get the eBook</a>
  <p class="book-cta__desc">PDF, ePUB, Kindle. Free for .</p>
    </div>
<div class="book-cta__col book-cta__ebook content-tab--content">
  <h3 class="book-cta__title"><span>Hardcover</span></h3><span class="book-cta__price"><span class="green">$29</span> <del style="font-size: 0.6em;color:#999;"><span title="Original Price" style="text-decoration: through; color: #757575; font-weight: normal; font-family: 'Mija',Arial,sans-serif;">$39</del></span><a class="btn btn--full btn--large btn--green" 
    href="/printed-books/form-design-patterns/"
    data-product-sku="form-design-patterns"
    data-product-path="/printed-books/form-design-patterns/"
    data-component="AddToCart" 
    style="text-shadow: 1px 1px 1px rgba(0,0,0,.3);">Get the Print (incl.&nbsp;eBook)</a>
  <p class="book-cta__desc">Printed, quality hardcover. Free airmail shipping worldwide.</p>
  </div>
</div>

<!--

<h3 id="about-the-book">About The Book</h3>

*Form Design Patterns* contains ten chapters ([&#8595; Table of Contents](#toc)). Each one represents a common real-world problem that we’ll solve together step by step. Design is just as much about asking (and understanding) questions, as it is about creating solutions. So we’ll spend time doing just that: discussing the problem, weighing up the options, and **creating technical solutions that are simple and inclusive**. 

Ultimately, the book is about <strong>understanding what users need</strong>. Users are people and people are different. So we’ll be considering multiple interaction modalities and how to help users work under situational (temporary or permanent) and environmental circumstances. We’ll be looking at every problem through an inclusive design lens. Because good design is inclusive.

-->

<h3 id="toc">Table Of Contents</h3>

<p>Each chapter revolves around a specific problem — after all, that’s how we solve problems in real life. But don’t be concerned, many of the styles, <strong>components</strong> and <strong>patterns</strong> born out of each chapter are <strong>reusable</strong> and applicable well beyond the specifics and you’ll see examples of this as we move through the book.</p>

<p> (0.7 MB) to get a feeling what the book is like inside.</p>

<ol>
<li><strong>A Registration Form</strong><br />
We’ll start looking at the foundational qualities of a well-designed form and how to think about them. By applying something called a question protocol, we’ll look at how to <em>reduce friction</em> without even touching the interface. Then we’ll look at some crucial patterns, including validation, that we’ll want to use for every form.</li>
<li><strong>A Checkout Form</strong><br />
We’ll consider checkout flows and look at several <em>input types</em> and how they affect the user experience on mobile and desktop browsers, all the while looking at ways to help both first-time and returning customers order quickly and simply.</li>
<li><strong>A Flight Booking Form</strong><br />
We’ll dive into the world of <em>progressively enhanced</em>, custom form components using ARIA. We’ll do this by exploring the best way to let users select destinations, pick dates, add passengers, and choose seats. We’ll analyze <em>native form controls</em>, and look at breaking away from convention when it becomes necessary.</li>
<li><strong>A Login Form</strong><br />
We’ll look at the ubiquitous login form. Despite its simple appearance, there’s a bunch of usability failures that so many sites suffer from.</li>
<li><strong>An Inbox</strong><br />
We’ll design ways to manage email in bulk, our first look at administrative interfaces. As such, this comes with its own set of challenges and patterns, including a responsive ARIA-described action menu, <em>multiple selection</em>, and <em>same-page messaging</em>.</li>
<li><strong>A Search Form</strong><br />
We’ll create a responsive search form that is readily available to users on all pages, and we’ll also consider the importance of the search mechanism that powers it.</li>
<li><strong>A Filter Form</strong><br />
Users often need to filter a large set of unwieldy search results. Without a well-designed filter, users are bound to give up. Filters pose a number of interesting and unique design problems that may force us to challenge best practice to give users a better experience.</li>
<li><strong>An Upload Form</strong><br />
Many services, like photo sharing, messaging, and many back-office applications, let users upload images and documents. We’ll study the file input and how we can use it to upload multiple files at once. Then we’ll look at the intricacies of a drag-and-drop, Ajax-enhanced interface that is inclusive of keyboard and screen reader users.</li>
<li><strong>An Expense Form</strong><br />
We’ll investigate the special problem of needing to create and add lots of expenses (or anything else) into a system. This is really an excuse to cover the <em>add another pattern</em>, which is often useful in administrative interfaces.</li>
<li><strong>A Really Long and Complicated Form</strong><br />
Some forms are very long and take hours to complete. We’ll look at some of the patterns we can use to make long forms easier to manage.</li>
</ol>

<h3 id="about-the-author">About The Author</h3>

<p><a href="https://twitter.com/adambsilver"><img style="float: right; padding: 0 1em 1em 1em; max-width: 250px;" srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4e361b13-4407-4dac-83ed-a4c6138672db/adam-silver-round-large.png 150w,
                    https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_850/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4e361b13-4407-4dac-83ed-a4c6138672db/adam-silver-round-large.png 200w,
                    https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4e361b13-4407-4dac-83ed-a4c6138672db/adam-silver-round-large.png 320w" src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4e361b13-4407-4dac-83ed-a4c6138672db/adam-silver-round-large.png" sizes="100vw" alt="Adam Silver" /></a>Adam Silver working on the web for a range of companies including Tesco, BBC, Just Eat, Financial Times, the Department for Work and Pensions and others.</p>

<p>He’s particularly interested in <em>inclusive design</em> and design systems and writes about this on his blog and popular design publications such as <em>A List Apart</em>. This isn’t his first book either: he previously wrote <em>Maintainable CSS</em>, a book about crafting maintainable UIs with CSS.</p>

<h4 id="technical-details">Technical Details</h4>

<ul>
<li><span class="small-caps">384</span> pages, <span class="small-caps">14</span> × <span class="small-caps">21</span> cm (<span class="small-caps">5.5</span> × <span class="small-caps">8.25</span> inches),</li>
<li>ISBN: <span class="small-caps">978-3-945749-73-9</span> (print),</li>
<li>Quality hardcover with stitched binding and a ribbon page marker,</li>
<li>The <strong>eBook</strong> is available in PDF, EPUB, and Amazon Kindle.</li>
<li>Free worldwide airmail shipping from Germany. </li>
<li>Available as  and <a href="/ebooks/form-design-patterns-ebook/"
data-product-path="/ebooks/form-design-patterns-ebook/" 
data-product-sku="form-design-patterns-ebook" 
data-component="AddToCart" data-silent="true">eBook</a>.</li>
</ul>

<h3 id="testimonials">Testimonials</h3>

<p>It has been our goal to make the book <strong>as practical and useful as possible</strong>. We’ve been honored to receive very positive reviews from people making websites on small and large scale.</p>

<ul>
<li>“I have been writing forms in HTML for over 20 years. This book captures the essence of what it is to embrace standards, progressively enhance and deliver <strong>simple, accessible forms</strong>. By formalising design patterns we can all use and implement, developers and designers can focus on their website and product. I wish this was available 20 years ago!”<br />
<em>&mdash; Paul Duncan, Design Technologists and Accessibility Teacher</em></li>
<li>“Forms. It&rsquo;s no coincidence that the word rhymes with &ldquo;yawns&rdquo; - forms are dull to code and even duller for your visitors to fill in. So make them work better for everyone, using the concrete tips, code and microcopy in this book. And take away your own yawns, as Adam Silver has done all the research and coding for you.”<br />
<em>&mdash; Bruce Lawson, Web standards Advocate</em></li>
<li>“Form Design Patterns is setting out common sense and <strong>inclusive solutions for forms</strong> both simple and potentially complex. It&rsquo;s your companion as you strive to create a simpler and easier interactive web.”<br />
<em>&mdash; Heydon Pickering, UX and accessibility consultant</em></li>
</ul>

<h3 id="why-this-book-is-for-you">Why This Book Is For You</h3>

<p>This book is a practical guide for anyone who needs to design, prototype and build all sorts of forms for digital services, products and websites. <strong>You&rsquo;ll learn</strong>:</p>

<ol>
<li>Available <strong>native form elements</strong> and their powers, limitations and constraints.</li>
<li>When and how to create <strong>accessible custom form components</strong> that can give users a better experience in comparison to their native equivalents.</li>
<li>How to significantly <strong>reduce friction in forms</strong> with careful use of language, flow and order.</li>
<li>Ways (and ways not) to help users <strong>fix form errors</strong> easily.</li>
<li>How to deal with <strong>complex interfaces</strong> that let users upload files and add multiple items of any sort.</li>
<li>Ways to let users <strong>search and filter</strong> a large set of results according to their own mental model.</li>
<li>How to help customers fill out especially <strong>long and complex forms</strong> that may take weeks to fill out.</li>
</ol>

<figure class="break-out">)</figcaption></figure>

<div class="book-cta" data-handler="ContentTabs" data-mq="(max-width: 480px)">
  <nav class="content-tabs content-tabs--books">
  <ul>
     <li class="content-tab">
     <button class="btn btn--small btn--white btn--white--bordered">eBook</button>
     </li>
     <li class="content-tab">
     <button class="btn btn--small btn--white btn--white--bordered">Hardcover</button>
     </li>
   </ul>
 </nav>
   <div class="book-cta__col book-cta__hardcover content-tab--content">
  <h3 class="book-cta__title"><span>eBook</span></h3><span class="book-cta__price">$10 <del style="font-size: 0.6em;color:#999;"><span title="Original Price" style="text-decoration: through; color: #757575; font-weight: normal; font-family: 'Mija',Arial,sans-serif;">$19</del></span><a class="btn btn--full btn--large" 
    href="/ebooks/form-design-patterns-ebook/"
    data-product-path="/ebooks/form-design-patterns-ebook/" 
    data-product-sku="form-design-patterns-ebook" 
    data-component="AddToCart" 
  style="text-shadow: 1px 1px 1px rgba(0,0,0,.3);">Get the eBook</a>
  <p class="book-cta__desc">PDF, ePUB, Kindle. Free for .</p>
    </div>
<div class="book-cta__col book-cta__ebook content-tab--content">
  <h3 class="book-cta__title"><span>Hardcover</span></h3><span class="book-cta__price"><span class="green">$29</span> <del style="font-size: 0.6em;color:#999;"><span title="Original Price" style="text-decoration: through; color: #757575; font-weight: normal; font-family: 'Mija',Arial,sans-serif;">$39</del></span><a class="btn btn--full btn--large btn--green" 
    href="/printed-books/form-design-patterns/"
    data-product-sku="form-design-patterns"
    data-product-path="/printed-books/form-design-patterns/"
    data-component="AddToCart" 
    style="text-shadow: 1px 1px 1px rgba(0,0,0,.3);">Get the Print (incl.&nbsp;eBook)</a>
  <p class="book-cta__desc">Printed, quality hardcover. Free airmail shipping worldwide.</p>
  </div>
</div>

<p style="border-bottom: 6px solid #ddd;padding-bottom: 1em;">We can’t wait to hear your thoughts about the book! <strong>Happy reading</strong>, and we hope that you’ll find the book as useful as we do. Just have a cup of coffee (or tea) ready before you start reading, of course. Stay <em>smashing</em> and... <em>meow</em>!</p>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(bl, hp)</span>
</div>


              </article>
            </body>
          </html>
---------------
<h1 id="#title_7" >8、RSocket：一个面向反应式应用程序的新型应用网络协议</h1>
Charles Humble
[http://www.infoq.com/cn/news/2018/10/rsocket-facebook?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/10/rsocket-facebook?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>SpringOne平台华盛顿大会上宣布的RSocket是一个新的、语言无关的第七层应用网络协议。它是一个双向、多路复用、基于消息、基于反应流回压的二进制协议。</p> <i>By Charles Humble</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_8" >9、SpringOne大会上发布了一个实验性的反应式关系型数据库连接驱动R2DBC</h1>
Charles Humble
[http://www.infoq.com/cn/news/2018/10/springone-r2dbc?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/10/springone-r2dbc?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>在SpringOne平台华盛顿大会上宣布的R2DBC是一个从头开始设计的实验性API，用于针对关系型数据库进行反应式编程。最终目标是试图影响ADBA规范。</p> <i>By Charles Humble</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_9" >10、访谈：Kotlin在Pinterest的逆势生长</h1>
Kesha Williams
[http://www.infoq.com/cn/news/2018/10/kotlin-pinterest?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/10/kotlin-pinterest?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>InfoQ最近采访了Pinterest核心UI团队的Android工程师Christina Lee，讨论了Pinterest对Kotlin的采用情况、Pinterest在采用过程中面临的挑战、从中总结的主要经验教训、从Java过渡到Kotlin的技巧，以及她即将在KotlinConf 2018上进行的演讲主题Representing State: the Kotlin Edition。</p> <i>By Kesha Williams</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_10" >11、Russ Miles：被忽略的架构师和混沌工程</h1>
Jan Stenberg
[http://www.infoq.com/cn/news/2018/10/architects-chaos-engineering?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/10/architects-chaos-engineering?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>在最近于阿姆斯特丹举行的事件驱动微服务大会上，Russ Miles声称，架构师面临的最大挑战是自身被忽视。你有很多很好的想法，比如事件驱动的微服务，但通常的反应是，这些主意听起来不错，但是对于手头要解决的问题来说过于复杂。</p> <i>By Jan Stenberg</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_11" >12、Netflix实时流处理平台Keystone介绍</h1>
Alex Giamas
[http://www.infoq.com/cn/news/2018/10/Netflix-Keystone-Real-Time-Proc?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/10/Netflix-Keystone-Real-Time-Proc?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Netflix近日在他们的技术博客上发表了一篇博文，探讨其实时流处理平台Keystone的设计考虑和见解。Keystone自2015年12月开始运营，随着Netflix订阅用户在过去3年从6500万增长到1.3亿多，其规模大幅增长。本文将介绍Keystone平台的最新情况。</p> <i>By Alex Giamas</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_12" >13、GlassFish新纪元</h1>
Michael Redlich
[http://www.infoq.com/cn/news/2018/10/a-new-era-for-glassfish?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/10/a-new-era-for-glassfish?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Eclipse基金会近日宣布了2018年9月的两个里程碑：GlassFish源代码已经从Oracle迁移完成；Java EE TCK现在已经开源。这被视为Jakarta EE发展的重要里程碑和GlassFish的新纪元，“这是使Jakarta EE成为云原生应用程序开发创新工具的又一个步骤。”</p> <i>By Michael Redlich</i> <i> Translated by 谢丽</i>
---------------