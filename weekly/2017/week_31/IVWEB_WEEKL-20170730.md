## 文章索引
1、 <a href="#1窗口管理器-xmonad-教程" >窗口管理器 xmonad 教程</a><br/><h1 id="#title_0" >1、窗口管理器 xmonad 教程</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2017/07/xmonad.html](http://www.ruanyifeng.com/blog/2017/07/xmonad.html)
<p>开发者最需要的，就是一个顺手的开发环境。</p>

        <p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017072701.jpg" alt="" title="" /></p>

<p>每个人的偏好不一样，我的开发环境是 Fish Shell + Xfce + xmonad + Vim，已经用了好多年，非常满意。</p>

<p>三个月前，我介绍了 。根据本文，读者可以从零开始配置并使用 xmonad。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017072702.png" alt="" title="" /></p>

<p>xmonad 的所有操作都通过键盘，只适合命令行的重度用户。如果你喜欢鼠标和图形界面，xmonad 不适合你。另外，它本身也不支持 Windows 系统。</p>

<h2>一、xmonad 是什么？</h2>

<p>xmonad 是一种窗口管理器（window manager），用来管理软件窗口的位置和大小，会自动在桌面上平铺（tiling）窗口。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017072703.jpg" alt="" title="" /></p>

<p>（图片说明：各种软件窗口）</p>

<p>注意，窗口管理器不是桌面环境（desktop environment）。后者是一套功能完善、集成各种工具的图形用户界面，比如 Gnome 和 KDE。桌面环境肯定包含了窗口管理器，但是（某些）窗口管理器可以不需要桌面环境，独立运行，xmonad 就是这种。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017072704.png" alt="" title="" /></p>

<p>（图片说明：典型的桌面环境）</p>

<p>桌面环境通常很重，窗口管理器就很轻，不仅体积小，资源占用也少，用户可以配置各种细节，释放出系统的最大性能。</p>

<p>Linux 系统允许用户更换窗口管理器，有可以选择。xmonad 一直是最受欢迎的前三名，它使用 Haskell 语言编写，是世界上使用人数最多的 Haskell 软件。它的特点就是极简化，性能高。</p>

<h2>二、安装</h2>

<p>xmonad 的官网提供，各个发行版都有。如果想自己编译，也可以下载源码。 </p>

<p>我的发行版是 Debian，安装就是一行命令。</p>

<blockquote><pre><code class="language-bash">
$ sudo apt-get install xmonad
</code></pre></blockquote>

<p>此外，还需要再安装两个小工具。</p>

<blockquote><pre><code class="language-bash">
$ sudo apt-get install xmobar dmenu
</code></pre></blockquote>

<p>安装完成后，退出当前对话（session），选择 xmonad 会话重新登录。登录后，你会看到一个完全空白的桌面，什么也没有，这说明 xmonad 起作用了，因为这时还没有任何软件窗口。</p>

<h2>三、常用命令</h2>

<h3>3.1 打开终端</h3>

<p>第一步，你需要打开一个窗口。一般来说，总是打开命令行终端窗口。</p>

<p>xmonad 提供一个功能键，称为<code>mod</code>键（modifier 的缩写），所有操作都要使用这个键，默认为<code>alt</code>键，但是一般会把它改掉，比如改成<code>Windows</code>键，具体修改方法请看后文。</p>

<p>打开终端窗口，按下<code>mod + shift + return</code>（默认为<code>alt + shift + return</code>）。这会打开一个终端窗口，占据了所有桌面空间。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017072705.png" alt="" title="" /></p>

<p>按下<code>mod + shift + return</code>，再打开一个终端窗口。它与第一个窗口水平地平分屏幕，每个窗口占据50%空间。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017072706.png" alt="" title="" /></p>

<p>注意，第二个窗口占据桌面的左边，自动获得焦点，成为当前窗口。这个左边部分就称为"主栏"（master pane），右边部分称为"副栏"，前面打开的第一个窗口自动进入副栏。</p>

<p>再按一次<code>mod + shift + return</code>，打开第三个窗口。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017072707.png" alt="" title="" /></p>

<p>这时，第三个窗口就会占据主栏，前两个窗口自动进入副栏。规则就是，新窗口总是独占主栏，旧窗口平分副栏。</p>

<h3>3.2 布局模式</h3>

<p>默认的布局模式是，主栏在左边，副栏在右边。</p>

<p>按下<code>mod + space</code>，布局模式改成主栏在上方，副栏在下方。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017072708.png" alt="" title="" /></p>

<p>再按一次<code>mod + space</code>，就变成独占模式，当前窗口独占整个桌面，其他窗口不可见。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017072705.png" alt="" title="" /></p>

<p>再按一次<code>mod + space</code>，就变回默认模式（主栏在左边，副栏在右边）。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017072707.png" alt="" title="" /></p>

<p>按下<code>mod + ,</code>（mod + 逗号），一个副栏窗口会移动到主栏，即主栏变成有两个窗口，副栏变成只有一个窗口。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017072709.png" alt="" title="" /></p>

<p>再按一次<code>mod + ,</code>（mod + 逗号），主栏变成三个窗口，副栏消失。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017072710.png" alt="" title="" /></p>

<p>按下<code>mod + .</code>（mod + 句号），主栏减少一个窗口，副栏增加一个窗口。</p>

<h3>3.3 移动焦点</h3>

<p>新窗口总是自动获得焦点，变成当前窗口。按下<code>mod + j</code>，焦点顺时针移动到下一个窗口。</p>

<p>按下<code>mod + k</code>，焦点逆时针移动到上一个窗口。</p>

<p>如果当前窗口在副栏，按下<code>mod + return</code>，会与主栏窗口对调位置。</p>

<h3>3.4 调整窗口顺序</h3>

<p>按下<code>mod + shift + j</code>，按照顺时针的顺序，当前窗口与下一个窗口交换位置，即当前窗口前进到下一个位置。</p>

<p>按下<code>mod + shift + k</code>，按照逆时针顺序，当前窗口与上一个窗口交换位置。即当前窗口后退到上一个位置。</p>

<h3>3.5 调整栏位大小</h3>

<p>按下<code>mod + l</code>，主栏增加尺寸。</p>

<p>按下<code>mod + h</code>，副栏增加尺寸。</p>

<h3>3.6 浮动窗口</h3>

<p>正常情况下，xmonad 决定了窗口的位置和大小，但有时我们希望自己控制。xmonad 允许某个窗口浮动，脱离原有的布局。</p>

<p>按下<code>mod + 鼠标左键</code>拖动窗口，该窗口就会变成浮动窗口，可以放到屏幕的任何位置。</p>

<p>按下<code>mod + 鼠标右键</code>可以调整窗口大小。</p>

<p>按下<code>mod + t</code>，当前浮动窗口就会结束浮动，重新回到 xmonad 的布局。</p>

<h3>3.7 关闭窗口</h3>

<p>窗口可以自然关闭（比如终端窗口按<code>ctrl + d</code>），也可以让 xmonad 强行关闭它。</p>

<p>按下<code>mod + shift + c</code>，会关闭当前窗口，焦点移到下一个窗口。</p>

<h3>3.8 退出 xmonad</h3>

<p>按下<code>mod + shift + q</code>，将会立刻关闭所有窗口，退出 xmonad，用户需要重新登录。</p>

<h2>四、工作区</h2>

<p>xmonad 提供9个工作区，相当于提供9个桌面。按下<code>mod + 1</code>到<code>mod + 9</code>切换。 xmonad 启动后，默认处于1号工作区 。</p>

<p>如果要将一个窗口移到不同的工作区，先用<code>mod + j</code>或<code>mod + k</code>，将其变成焦点窗口，然后使用<code>mod + shift + 6</code>，就将其移到了6号工作区。</p>

<p>我的习惯是，1号工作区是终端，2号是浏览器，4号是虚拟机。</p>

<h2>五、多显示器</h2>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017072712.jpg" alt="" title="" /></p>

<p>多显示器需要使用配置工具，我用的是 xrandr。其他工具还有 Xinerama 和 winView，另外 arandr 是 xrandr 的图形界面，也可以用。</p>

<p>下面的命令查看显示器的连接情况。</p>

<blockquote><pre><code class="language-bash">
$ xrandr -q
</code></pre></blockquote>

<p>具体的配置教程可以看。</p>

<p>使用多显示器时，每个显示器会分配到一个工作区。默认情况下，1号工作区显示在主显示器，2号工作区显示在第二个显示器。如果要将4号工作区显示在当前显示器，那么按下<code>mod + 4</code>，4号工作就会与当前屏幕中的工作区互换位置。</p>

<p><code>mod + w</code> 转移焦点到左显示器，<code>mod + e</code>转移焦点到右显示器。</p>

<p><code>mod + shift + w</code>将当前窗口移到左显示器，<code>mod + shift + e</code>将当前窗口移到右显示器。</p>

<h2>六、配置文件</h2>

<p>xmonad 的配置文件是<code>～/.xmonad/xmonad.hs</code>。该文件需要用户自己新建，。</p>

<p>这个文件里面，<code>modMask</code>决定了<code>mod</code>到底是哪一个键。</p>

<blockquote><pre><code class="language-bash">
modMask = mod4Mask
</code></pre></blockquote>

<p>上面的这行就将<code>mod</code>键设为了<code>Windows</code>键。</p>

<p>修改配置文件以后，按下<code>mod + q</code>，新的配置就会生效。</p>

<h2>七、xmobar</h2>

<p>xmonad 的默认桌面，什么也没有，不太方便。xmobar 提供了一个状态栏，将常用信息显示在上面，比如 CPU 和内存的占用情况、天气、时间等等。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017072713.jpg" alt="" title="" /></p>

<p>（图片说明：顶部状态栏就是 xmobar。）</p>

<p>它的配置文件是<code>~/.xmobarrc</code>（教程是我的笔记本电脑使用的配置。</p>

<h2>八、dmenu</h2>

<p>最后，dmenu 在桌面顶部提供了一个菜单条，可以快速启动应用程序。</p>

<p><img src="http://www.ruanyifeng.com/blogimg/asset/2017/bg2017072714.png" alt="" title="" /></p>

<p>（图片说明：dmenu 显示在屏幕顶部，输入<code>fire</code>会自动显示包含<code>fire</code>的启动命令。）</p>

<p>它从系统变量<code>$PATH</code>指定的路径中，寻找所有的应用程序，根据用户的键入，动态提示最符合的结果。</p>

<p>按下<code>mod + p</code>就会进入<code>dmenu</code>菜单栏，按下<code>ESC</code>键可以退出。方向键用来选择应用程序，<code>return</code>键用来启动。</p>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2017-07-29T08:25:25+08:00">2017年7月29日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>博客文集：</li>
<li>社交媒体：</li>
<li>Feed订阅： </li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------