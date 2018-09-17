## 文章索引
1、 <a href="#1vim-配置入门" >Vim 配置入门</a><br/>
2、 <a href="#2文章-点评可调整大小哈希表riak-core和随机切片技术" >文章： 点评可调整大小哈希表：Riak Core和随机切片技术</a><br/>
3、 <a href="#3文章-为什么说kubernetes是新的应用服务器" >文章： 为什么说Kubernetes是新的应用服务器</a><br/>
4、 <a href="#4文章-人工智能的下一个重大挑战理解语言的细微差别" >文章： 人工智能的下一个重大挑战：理解语言的细微差别</a><br/>
5、 <a href="#5视频演讲-对话系统的基本概念与原理" >视频演讲： 对话系统的基本概念与原理</a><br/><h1 id="#title_0" >1、Vim 配置入门</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2018/09/vimrc.html](http://www.ruanyifeng.com/blog/2018/09/vimrc.html)
<p>Vim 是最重要的编辑器之一，主要有下面几个优点。</p>

        <p><img src="https://www.wangbase.com/blogimg/asset/201809/bg2018091601.jpg" alt="" title="" /></p>

<blockquote>
  <ul>
<li>可以不使用鼠标，完全用键盘操作。</li>
<li>系统资源占用小，打开大文件毫无压力。</li>
<li>键盘命令变成肌肉记忆以后，操作速度极快。</li>
<li>服务器默认都安装 Vi 或 Vim。</li>
</ul>
</blockquote>

<p>Vim 的配置不太容易，它有自己的语法，许许多多的命令。我总是记不清楚，所以就整理了下面这篇文章，列出主要配置项的含义。</p>

<h2>一、基础知识</h2>

<p>Vim 的全局配置一般在<code>/etc/vim/vimrc</code>或者<code>/etc/vimrc</code>，对所有用户生效。用户个人的配置在<code>~/.vimrc</code>。</p>

<p>如果只对单次编辑启用某个配置项，可以在命令模式下，先输入一个冒号，再输入配置。举例来说，<code>set number</code>这个配置可以写在<code>.vimrc</code>里面，也可以在命令模式输入。</p>

<blockquote><pre><code class="language-bash">
:set number
</code></pre></blockquote>

<p>配置项一般都有"打开"和"关闭"两个设置。"关闭"就是在"打开"前面加上前缀"no"。</p>

<blockquote><pre><code class="language-bash">
" 打开
set number

" 关闭
set nonumber
</code></pre></blockquote>

<p>上面代码中，双引号开始的行表示注释。</p>

<p>查询某个配置项是打开还是关闭，可以在命令模式下，输入该配置，并在后面加上问号。</p>

<blockquote><pre><code class="language-bash">
:set number?
</code></pre></blockquote>

<p>上面的命令会返回<code>number</code>或者<code>nonumber</code>。</p>

<p>如果想查看帮助，可以使用<code>help</code>命令。</p>

<blockquote><pre><code class="language-bash">
:help number
</code></pre></blockquote>

<h2>二、基本配置</h2>

<p>（1）</p>

<blockquote><pre><code class="language-bash">
set nocompatible
</code></pre></blockquote>

<p>不与 Vi 兼容（采用 Vim 自己的操作命令）。</p>

<p>（2）</p>

<blockquote><pre><code class="language-bash">
syntax on
</code></pre></blockquote>

<p>打开语法高亮。自动识别代码，使用多种颜色显示。</p>

<p>（3）</p>

<blockquote><pre><code class="language-bash">
set showmode
</code></pre></blockquote>

<p>在底部显示，当前处于命令模式还是插入模式。</p>

<p>（4）</p>

<blockquote><pre><code class="language-bash">
set showcmd
</code></pre></blockquote>

<p>命令模式下，在底部显示，当前键入的指令。比如，键入的指令是<code>2y3d</code>，那么底部就会显示<code>2y3</code>，当键入<code>d</code>的时候，操作完成，显示消失。</p>

<p>（5）</p>

<blockquote><pre><code class="language-bash">
set mouse=a
</code></pre></blockquote>

<p>支持使用鼠标。</p>

<p>（6）</p>

<blockquote><pre><code class="language-bash">
set encoding=utf-8  
</code></pre></blockquote>

<p>使用 utf-8 编码。</p>

<p>（7）</p>

<blockquote><pre><code class="language-bash"> 
set t_Co=256
</code></pre></blockquote>

<p>启用256色。</p>

<p>（8）</p>

<blockquote><pre><code class="language-bash">
filetype indent on
</code></pre></blockquote>

<p>开启文件类型检查，并且载入与该类型对应的缩进规则。比如，如果编辑的是<code>.py</code>文件，Vim 就是会找 Python 的缩进规则<code>~/.vim/indent/python.vim</code>。</p>

<h2>三、缩进</h2>

<p>（9）</p>

<blockquote><pre><code class="language-bash">
set autoindent
</code></pre></blockquote>

<p>按下回车键后，下一行的缩进会自动跟上一行的缩进保持一致。</p>

<p>（10）</p>

<blockquote><pre><code class="language-bash">
set tabstop=2
</code></pre></blockquote>

<p>按下 Tab 键时，Vim 显示的空格数。</p>

<p>（11）</p>

<blockquote><pre><code class="language-bash">
set shiftwidth=4
</code></pre></blockquote>

<p>在文本上按下<code>&gt;&gt;</code>（增加一级缩进）、<code>&lt;&lt;</code>（取消一级缩进）或者<code>==</code>（取消全部缩进）时，每一级的字符数。</p>

<p>（12）</p>

<blockquote><pre><code class="language-bash">
set expandtab
</code></pre></blockquote>

<p>由于 Tab 键在不同的编辑器缩进不一致，该设置自动将 Tab 转为空格。</p>

<p>（13）</p>

<blockquote><pre><code class="language-bash">
set softtabstop=2
</code></pre></blockquote>

<p>Tab 转为多少个空格。</p>

<h2>四、外观</h2>

<p>（14）</p>

<blockquote><pre><code class="language-bash">
set number
</code></pre></blockquote>

<p>显示行号</p>

<p>（15）</p>

<blockquote><pre><code class="language-bash">
set relativenumber
</code></pre></blockquote>

<p>显示光标所在的当前行的行号，其他行都为相对于该行的相对行号。</p>

<p>（16）</p>

<blockquote><pre><code class="language-bash">
set cursorline
</code></pre></blockquote>

<p>光标所在的当前行高亮。</p>

<p>（17）</p>

<blockquote><pre><code class="language-bash">
set textwidth=80
</code></pre></blockquote>

<p>设置行宽，即一行显示多少个字符。</p>

<p>（18）</p>

<blockquote><pre><code class="language-bash">
set wrap
</code></pre></blockquote>

<p>自动折行，即太长的行分成几行显示。</p>

<blockquote><pre><code class="language-bash">
set nowrap
</code></pre></blockquote>

<p>关闭自动折行</p>

<p>（19）</p>

<blockquote><pre><code class="language-bash">
set linebreak
</code></pre></blockquote>

<p>只有遇到指定的符号（比如空格、连词号和其他标点符号），才发生折行。也就是说，不会在单词内部折行。</p>

<p>（20）</p>

<blockquote><pre><code class="language-bash">
set wrapmargin=2
</code></pre></blockquote>

<p>指定折行处与编辑窗口的右边缘之间空出的字符数。</p>

<p>（21）</p>

<blockquote><pre><code class="language-bash">
set scrolloff=5
</code></pre></blockquote>

<p>垂直滚动时，光标距离顶部/底部的位置（单位：行）。</p>

<p>（22）</p>

<blockquote><pre><code class="language-bash">
set sidescrolloff=15
</code></pre></blockquote>

<p>水平滚动时，光标距离行首或行尾的位置（单位：字符）。该配置在不折行时比较有用。</p>

<p>（23）</p>

<blockquote><pre><code class="language-bash">
set laststatus=2
</code></pre></blockquote>

<p>是否显示状态栏。0 表示不显示，1 表示只在多窗口时显示，2 表示显示。</p>

<p>（24）</p>

<blockquote><pre><code class="language-bash">
set  ruler
</code></pre></blockquote>

<p>在状态栏显示光标的当前位置（位于哪一行哪一列）。</p>

<h2>五、搜索</h2>

<p>（25）</p>

<blockquote><pre><code class="language-bash">
set showmatch
</code></pre></blockquote>

<p>光标遇到圆括号、方括号、大括号时，自动高亮对应的另一个圆括号、方括号和大括号。</p>

<p>（26）</p>

<blockquote><pre><code class="language-bash">
set hlsearch
</code></pre></blockquote>

<p>搜索时，高亮显示匹配结果。</p>

<p>（27）</p>

<blockquote><pre><code class="language-bash">
set incsearch
</code></pre></blockquote>

<p>输入搜索模式时，每输入一个字符，就自动跳到第一个匹配的结果。</p>

<p>（28）</p>

<blockquote><pre><code class="language-bash">
set ignorecase
</code></pre></blockquote>

<p>搜索时忽略大小写。</p>

<p>（29）</p>

<blockquote><pre><code class="language-bash">
set smartcase
</code></pre></blockquote>

<p>如果同时打开了<code>ignorecase</code>，那么对于只有一个大写字母的搜索词，将大小写敏感；其他情况都是大小写不敏感。比如，搜索<code>Test</code>时，将不匹配<code>test</code>；搜索<code>test</code>时，将匹配<code>Test</code>。</p>

<h2>六、编辑</h2>

<p>（30）</p>

<blockquote><pre><code class="language-bash">
set spell spelllang=en_us
</code></pre></blockquote>

<p>打开英语单词的拼写检查。</p>

<p>（31）</p>

<blockquote><pre><code class="language-bash">
set nobackup
</code></pre></blockquote>

<p>不创建备份文件。默认情况下，文件保存时，会额外创建一个备份文件，它的文件名是在原文件名的末尾，再添加一个波浪号（〜）。</p>

<p>（32）</p>

<blockquote><pre><code class="language-bash">
set noswapfile
</code></pre></blockquote>

<p>不创建交换文件。交换文件主要用于系统崩溃时恢复文件，文件名的开头是<code>.</code>、结尾是<code>.swp</code>。</p>

<p>（33）</p>

<blockquote><pre><code class="language-bash">
set undofile
</code></pre></blockquote>

<p>保留撤销历史。</p>

<p>Vim 会在编辑时保存操作历史，用来供用户撤消更改。默认情况下，操作记录只在本次编辑时有效，一旦编辑结束、文件关闭，操作历史就消失了。</p>

<p>打开这个设置，可以在文件关闭后，操作记录保留在一个文件里面，继续存在。这意味着，重新打开一个文件，可以撤销上一次编辑时的操作。撤消文件是跟原文件保存在一起的隐藏文件，文件名以<code>.un~</code>开头。</p>

<p>（34）</p>

<blockquote><pre><code class="language-bash">
set backupdir=~/.vim/.backup//  
set directory=~/.vim/.swp//
set undodir=~/.vim/.undo// 
</code></pre></blockquote>

<p>设置备份文件、交换文件、操作历史文件的保存位置。</p>

<p>结尾的<code>//</code>表示生成的文件名带有绝对路径，路径中用<code>%</code>替换目录分隔符，这样可以防止文件重名。</p>

<p>（35）</p>

<blockquote><pre><code class="language-bash">
set autochdir
</code></pre></blockquote>

<p>自动切换工作目录。这主要用在一个 Vim 会话之中打开多个文件的情况，默认的工作目录是打开的第一个文件的目录。该配置可以将工作目录自动切换到，正在编辑的文件的目录。</p>

<p>（36）</p>

<blockquote><pre><code class="language-bash">
set noerrorbells
</code></pre></blockquote>

<p>出错时，不要发出响声。</p>

<p>（37）</p>

<blockquote><pre><code class="language-bash">
set visualbell
</code></pre></blockquote>

<p>出错时，发出视觉提示，通常是屏幕闪烁。</p>

<p>（38）</p>

<blockquote><pre><code class="language-bash">
set history=1000
</code></pre></blockquote>

<p>Vim 需要记住多少次历史操作。</p>

<p>（39）</p>

<blockquote><pre><code class="language-bash">
set autoread
</code></pre></blockquote>

<p>打开文件监视。如果在编辑过程中文件发生外部改变（比如被别的编辑器编辑了），就会发出提示。</p>

<p>（40）</p>

<blockquote><pre><code class="language-bash">
set listchars=tab:»■,trail:■
set list
</code></pre></blockquote>

<p>如果行尾有多余的空格（包括 Tab 键），该配置将让这些空格显示成可见的小方块。</p>

<p>（41）</p>

<blockquote><pre><code class="language-bash">
set wildmenu
set wildmode=longest:list,full
</code></pre></blockquote>

<p>命令模式下，底部操作指令按下 Tab 键自动补全。第一次按下 Tab，会显示所有匹配的操作指令的清单；第二次按下 Tab，会依次选择各个指令。</p>

<h2>七、参考链接</h2>

<ul>
<li></li>
<li></li>
<li></li>
</ul>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2018-09-16T09:32:56+08:00">2018年9月16日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>文集：</li>
<li>社交媒体：</li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------
<h1 id="#title_1" >2、文章： 点评可调整大小哈希表：Riak Core和随机切片技术</h1>
Scott Lystig Fritchie
[http://www.infoq.com/cn/articles/dynamo-riak-random-slicing?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/dynamo-riak-random-slicing?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/dynamo-riak-random-slicing/zh/smallimage/dynamo-riak-random-slicing-018-1535144122758-1536935413661.jpg"/><p>分布式流数据处理框架Wallaroo需要支持计算群集规模的调整，实现此需要一种大小可调整的分布式数据结构。一个好的做法是使用分布式哈希表，但问题在于应该如何选择分布式哈希算法？本文探讨了一致性哈希是否的确适用于Wallaroo，分析了现有技术的利弊，并介绍了一种称为随机切片的新技术。</p> <i>By Scott Lystig Fritchie</i> <i> Translated by 盖磊</i>
---------------
<h1 id="#title_2" >3、文章： 为什么说Kubernetes是新的应用服务器</h1>
Rafael Benevides
[http://www.infoq.com/cn/articles/why-kubernetes-is-the-new-application-server?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/why-kubernetes-is-the-new-application-server?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/why-kubernetes-is-the-new-application-server/zh/smallimage/Rowing+Team-1537001515248.jpg"/><p>Kubernetes为应用提供了很多基础设施，而这些基础设施以前都是由应用服务器来提供的。本文分析了容器技术发展对应用服务器所带来的影响，以及云原生应用的典型组成。</p> <i>By Rafael Benevides</i> <i> Translated by 张卫滨 </i>
---------------
<h1 id="#title_3" >4、文章： 人工智能的下一个重大挑战：理解语言的细微差别</h1>
James Yang
[http://www.infoq.com/cn/articles/next-challenge-understanding-nuances-of-language?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/next-challenge-understanding-nuances-of-language?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/next-challenge-understanding-nuances-of-language/zh/smallimage/java-serialization-logo-small-1535467013919-1537002462413.jpg"/><p>我们能让机器听得懂一句话背后的含义吗？</p> <i>By James Yang</i> <i> Translated by 刘志勇</i>
---------------
<h1 id="#title_4" >5、视频演讲： 对话系统的基本概念与原理</h1>
姜文斌
[http://www.infoq.com/cn/presentations/basic-concepts-and-principles-of-dialogue-system?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/basic-concepts-and-principles-of-dialogue-system?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/presentations/basic-concepts-and-principles-of-dialogue-system/zh/mediumimage/jaingwenbin270-1537019816705.jpg"/><p>UNIT为广大开发者提供了可定制的对话系统解决方案，经过近一年的技术升级，UNIT 2.0已于今年七月份正式面世。本次课程，将从UNIT对话系统的基本结构和功能出发，介绍对话系统的核心模块和常用技术，并详细讲解搭建一个对话系统的流程。</p> <i>By 姜文斌</i>
---------------