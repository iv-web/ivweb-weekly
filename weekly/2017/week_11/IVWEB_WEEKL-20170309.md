## 文章索引
1、 <a href="#1typescript-22为javascript开发者带来更多期待的功能" >TypeScript 2.2为JavaScript开发者带来更多期待的功能</a><br/>
2、 <a href="#2使用-webpack2-和-npm-scripts-进行-javascript-组件开发" >使用 webpack2 和 NPM Scripts 进行 JavaScript 组件开发</a><br/>
3、 <a href="#3文章-基于虚拟化的安全性---第2篇内核通信" >文章： 基于虚拟化的安全性 - 第2篇：内核通信</a><br/>
4、 <a href="#4视频演讲-网格社区闲鱼技术架构体系演进" >视频演讲： 网格社区：闲鱼技术架构体系演进</a><br/>
5、 <a href="#5文章-叶亚明合格cto的六要素" >文章： 叶亚明：合格CTO的六要素</a><br/>
6、 <a href="#6迷你书-架构师2017年3月" >迷你书： 架构师（2017年3月）</a><br/>
7、 <a href="#7从反应式到预测式全域大数据的技术演进解析" >从反应式到预测式，全域大数据的技术演进解析</a><br/>
8、 <a href="#8人为失误导致aws-s3的us-east-1区服务宕机" >人为失误导致AWS S3的US-EAST-1区服务宕机</a><br/>
9、 <a href="#9swift内存所有权宣言" >Swift内存所有权宣言</a><br/>
10、 <a href="#10文章-chrome-56已经支持图像识别-apishape-detection-api" >文章： Chrome 56已经支持图像识别 API（Shape Detection API）</a><br/>
11、 <a href="#11java性能最后一个领域去除垃圾回收器" >Java性能最后一个领域：去除垃圾回收器</a><br/>
12、 <a href="#12jay-simons谈atlassian收购trello" >Jay Simons谈Atlassian收购Trello</a><br/>
13、 <a href="#13微软开源基于云的生理学研究工具" >微软开源基于云的生理学研究工具</a><br/>
14、 <a href="#14deeplearning4j如何建设深度学习开源社区" >Deeplearning4j：如何建设深度学习开源社区</a><br/>
15、 <a href="#15学习机器学习之如何根据需求选择一种算法" >学习机器学习之如何根据需求选择一种算法</a><br/>
16、 <a href="#16视频演讲-什么是架构的极致由-iot-核心参考架构-sluff-带来的思考" >视频演讲： 什么是架构的极致？——由 IoT 核心参考架构 Sluff 带来的思考</a><br/>
17、 <a href="#17how-to-simplify-networking-in-android:-introducing-the-volley-http-library" >How To Simplify Networking In Android: Introducing The Volley HTTP Library</a><br/>
18、 <a href="#18hibernation-time-is-over!-inspiring-desktop-wallpapers-to-fuel-your-creativity-march-2017-edition" >Hibernation Time Is Over! Inspiring Desktop Wallpapers To Fuel Your Creativity (March 2017 Edition)</a><br/><h1 id="#title_0" >1、TypeScript 2.2为JavaScript开发者带来更多期待的功能</h1>
David Iffland
[http://www.infoq.com/cn/news/2017/03/typescript-22-released?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/03/typescript-22-released?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Microsoft的TypeScript版本2.2为JavaScript开发人员提供了更多他们习惯的东西；它提供了人性化功能，以帮助消除简单的错误，并提供了更多的选择，以消除不必要的拼写错误。</p> <i>By David Iffland</i> <i> Translated by 谢旭</i>
---------------
<h1 id="#title_1" >2、使用 webpack2 和 NPM Scripts 进行 JavaScript 组件开发</h1>

[https://www.h5jun.com/post/using-webpack2-and-npm-scripts.html](https://www.h5jun.com/post/using-webpack2-and-npm-scripts.html)
<div class="toc"><ul>
<li></li>
<li><ul>
<li></li>
<li></li>
<li></li>
</ul>
</li>
<li></li>
<li><ul>
<li></li>
</ul>
</li>
<li></li>
</ul>
</div><p>最近  成为非常流行的打包工具，很多项目都在使用它。在我们进行 <strong>JavaScript 独立组件</strong>开发的时候，如果我们想要使用语言新特性，又想发布的时候产出兼容性好的代码，那么使用 webpack 就能够很大程度上帮助我们实现这一目标。</p>
<p>现在让我们来看看究竟该怎么做吧。</p>
<!--more-->
<h2>搭建一个简易环境</h2>
<p>首先，第一步是初始化和安装一些必要的依赖，搭建一个简易的开发和调试环境：</p>
<pre><code class="hljs lang-bash"><span class="hljs-comment"># 初始化 package.json</span>
npm init -i
<span class="hljs-comment"># 安装 http-server</span>
npm install http-server --save-dev
<span class="hljs-comment"># 安装 webpack </span>
npm install webpack webpack-dev-server --save-dev
<span class="hljs-comment"># 安装 babel 和 babel 插件，如果不想使用 babel 编译 ES6+，可以跳过这一步</span>
npm install babel-loader babel-core babel-preset-env babel-plugin-transform-runtime --save-dev
</code></pre>
<p>有了这个基础环境之后，我们来配置一份 webpack.config.js</p>
<h2>配置 webpack</h2>
<p>我们在项目目录里添加 webpack.config.js</p>
<pre><code class="hljs lang-js"><span class="hljs-built_in">module</span>.exports = <span class="hljs-function"><span class="hljs-keyword">function</span>(<span class="hljs-params">env = {}</span>)</span>{

  <span class="hljs-keyword">const</span> webpack     = <span class="hljs-built_in">require</span>(<span class="hljs-string">'webpack'</span>),
        path        = <span class="hljs-built_in">require</span>(<span class="hljs-string">'path'</span>),
        fs          = <span class="hljs-built_in">require</span>(<span class="hljs-string">'fs'</span>),
        packageConf = <span class="hljs-built_in">JSON</span>.parse(fs.readFileSync(<span class="hljs-string">'package.json'</span>, <span class="hljs-string">'utf-8'</span>));

  <span class="hljs-keyword">let</span> name      = packageConf.name,
      version   = packageConf.version,
      library   = name.replace(<span class="hljs-regexp">/^(\w)/</span>, m =&gt; m.toUpperCase()),
      proxyPort = <span class="hljs-number">8081</span>,
      plugins   = [],
      loaders   = [];

  <span class="hljs-keyword">if</span>(env.production){
    name += <span class="hljs-string">`-<span class="hljs-subst">${version}</span>.min`</span>;
    <span class="hljs-comment">//compress js in production environment</span>
    plugins.push(
      <span class="hljs-keyword">new</span> webpack.optimize.UglifyJsPlugin({
        compress: {
          warnings: <span class="hljs-literal">false</span>,
          drop_console: <span class="hljs-literal">false</span>,
         }
      })
    );
  }

  <span class="hljs-keyword">if</span>(fs.existsSync(<span class="hljs-string">'./.babelrc'</span>)){
    <span class="hljs-comment">//use babel</span>
    <span class="hljs-keyword">let</span> babelConf = <span class="hljs-built_in">JSON</span>.parse(fs.readFileSync(<span class="hljs-string">'.babelrc'</span>));
    loaders.push({
      test: <span class="hljs-regexp">/\.js$/</span>,
      exclude: <span class="hljs-regexp">/(node_modules|bower_components)/</span>,
      loader: <span class="hljs-string">'babel-loader'</span>,
      query: babelConf
    });
  }

  <span class="hljs-keyword">return</span> {
    entry: <span class="hljs-string">'./lib/app.js'</span>,
    output: {
      filename: <span class="hljs-string">`<span class="hljs-subst">${name}</span>.js`</span>,
      path: path.resolve(__dirname, <span class="hljs-string">'dist'</span>),
      publicPath: <span class="hljs-string">'/static/js/'</span>,
      library: <span class="hljs-string">`<span class="hljs-subst">${library}</span>`</span>,
      libraryTarget: <span class="hljs-string">'umd'</span>
    },

    plugins: plugins,

    <span class="hljs-built_in">module</span>: {
      loaders: loaders
    },

    devServer: {
      proxy: {
        <span class="hljs-string">"*"</span>: <span class="hljs-string">`http://127.0.0.1:<span class="hljs-subst">${proxyPort}</span>`</span>,
      }
    }
  };
}
</code></pre>
<p>代码比较长，但不复杂，这里我分别解释一下各部分的作用：</p>
<h3>生产环境和开发环境</h3>
<p>首先我们从 package.json 里面取出一些信息，包括模块名和版本号，我们依赖它们来生成对应的 umd 模块的 library、输出的文件名以及版本号。</p>
<p>在这里我们规定在开发环境时输出 <code>模块名.js</code>，在生产环境发布时输出 <code>模块名-版本号.min.js</code>。</p>
<p>在 webpack2 里，我们可以通过 env.production 获取命令行参数 <code>--env.production</code>，从而区别是开发环境还是生产环境。</p>
<pre><code class="hljs lang-js">  <span class="hljs-keyword">if</span>(env.production){
    name += <span class="hljs-string">`-<span class="hljs-subst">${version}</span>.min`</span>;
    <span class="hljs-comment">//compress js in production environment</span>
    plugins.push(
      <span class="hljs-keyword">new</span> webpack.optimize.UglifyJsPlugin({
        compress: {
          warnings: <span class="hljs-literal">false</span>,
          drop_console: <span class="hljs-literal">false</span>,
         }
      })
    );
  }
</code></pre>
<p>在生产环境中，我们不仅改变输出的文件名，还配置 UglifyJsPlugin 来压缩脚本。</p>
<h3>使用 babel 编译 ES6</h3>
<p>如果脚本用到 ES6，我们希望用 babel 编译的话，还需要加载 babel-loader 来进行编译。我们采用 babel 的默认配置 <code>.babelrc</code>，在项目目录里添加 .babelrc：</p>
<pre><code class="hljs lang-json">{
  <span class="hljs-attr">"presets"</span>: [<span class="hljs-string">"env"</span>],
  <span class="hljs-attr">"plugins"</span>: [<span class="hljs-string">"transform-runtime"</span>]
}
</code></pre>
<p>然后我们在 webpack.config.json 里根据配置来添加 loader:</p>
<pre><code class="hljs lang-js">  <span class="hljs-keyword">if</span>(fs.existsSync(<span class="hljs-string">'./.babelrc'</span>)){
    <span class="hljs-comment">//use babel</span>
    <span class="hljs-keyword">let</span> babelConf = <span class="hljs-built_in">JSON</span>.parse(fs.readFileSync(<span class="hljs-string">'.babelrc'</span>));
    loaders.push({
      test: <span class="hljs-regexp">/\.js$/</span>,
      exclude: <span class="hljs-regexp">/(node_modules|bower_components)/</span>,
      loader: <span class="hljs-string">'babel-loader'</span>,
      query: babelConf
    });
  }
</code></pre>
<h3>配置开发调试的 webpack-dev-server</h3>
<p>最后，为了在开发环境里调试，我们还需要配置 webpack-dev-server:</p>
<pre><code class="hljs lang-js">    devServer: {
      proxy: {
        <span class="hljs-string">"*"</span>: <span class="hljs-string">`http://127.0.0.1:<span class="hljs-subst">${proxyPort}</span>`</span>,
      }
    }
</code></pre>
<p>webpack-dev-server 是一个代理，我们之前安装了 http-server，我们用 webpack-dev-server 来代理它，所以开发时我们让 http-server 运行在 8081 端口：</p>
<pre><code class="hljs lang-undefined">webpack-dev-server --quiet &amp; http-server -p 8081 -c-1
</code></pre>
<h2>创建 NPM Scripts</h2>
<p>配置好了 webpack，创建 NPM Scripts 是个非常简单的过程：</p>
<pre><code class="hljs lang-js">  <span class="hljs-string">"scripts"</span>: {
    [...]
    <span class="hljs-string">"start"</span>: <span class="hljs-string">"webpack-dev-server --quiet &amp; http-server -c-1 -p 8081"</span>,
    <span class="hljs-string">"build-release"</span>: <span class="hljs-string">"webpack --env.production"</span>
  },
</code></pre>
<p>我们在 package.json 里添加两个脚本，这样我们就可以使用 <code>npm start</code> 来启动开发环境，使用 <code>npm run build-release</code> 来发布到生产环境了。</p>
<h2>开始项目开发</h2>
<p>接下来我们创建 lib/app.js：</p>
<pre><code class="hljs lang-js"><span class="hljs-built_in">module</span>.exports = <span class="hljs-built_in">require</span>(<span class="hljs-string">'./demo'</span>);
</code></pre>
<p>然后创建 lib/demo.js:</p>
<pre><code class="hljs lang-js"><span class="hljs-built_in">module</span>.exports = <span class="hljs-class"><span class="hljs-keyword">class</span> <span class="hljs-title">Demo</span></span>{
  <span class="hljs-keyword">async</span> test(){
    <span class="hljs-keyword">return</span> <span class="hljs-keyword">new</span> <span class="hljs-built_in">Promise</span>((resolve) =&gt; {
      setTimeout(resolve, <span class="hljs-number">1000</span>)
    });
  }
}
</code></pre>
<p>创建 examples/index.html:</p>
<pre><code class="hljs lang-html"><span class="hljs-meta">&lt;!DOCTYPE html&gt;</span>
<span class="hljs-tag">&lt;<span class="hljs-name">html</span> <span class="hljs-attr">lang</span>=<span class="hljs-string">"en"</span>&gt;</span>
<span class="hljs-tag">&lt;<span class="hljs-name">head</span>&gt;</span>
  <span class="hljs-tag">&lt;<span class="hljs-name">meta</span> <span class="hljs-attr">charset</span>=<span class="hljs-string">"UTF-8"</span>&gt;</span>
  <span class="hljs-tag">&lt;<span class="hljs-name">title</span>&gt;</span>Demo<span class="hljs-tag">&lt;/<span class="hljs-name">title</span>&gt;</span>
<span class="hljs-tag">&lt;/<span class="hljs-name">head</span>&gt;</span>
<span class="hljs-tag">&lt;<span class="hljs-name">body</span>&gt;</span>
  <span class="hljs-tag">&lt;<span class="hljs-name">h1</span>&gt;</span>Hello<span class="hljs-tag">&lt;/<span class="hljs-name">h1</span>&gt;</span>
  <span class="hljs-tag">&lt;<span class="hljs-name">script</span> <span class="hljs-attr">src</span>=<span class="hljs-string">"/static/js/demo.js"</span>&gt;</span><span class="undefined"></span><span class="hljs-tag">&lt;/<span class="hljs-name">script</span>&gt;</span>
  <span class="hljs-tag">&lt;<span class="hljs-name">script</span>&gt;</span><span class="javascript">
    <span class="hljs-keyword">var</span> d = <span class="hljs-keyword">new</span> Demo();
    d.test().then(<span class="hljs-function"><span class="hljs-keyword">function</span>(<span class="hljs-params"></span>)</span>{
      <span class="hljs-built_in">console</span>.log(<span class="hljs-string">'test done!'</span>);
    });
  </span><span class="hljs-tag">&lt;/<span class="hljs-name">script</span>&gt;</span>
<span class="hljs-tag">&lt;/<span class="hljs-name">body</span>&gt;</span>
<span class="hljs-tag">&lt;/<span class="hljs-name">html</span>&gt;</span>
</code></pre>
<p>运行 <code>npm start</code>，访问 </p>
<p>打开控制台，1秒后就能看到输出 <code>test done</code>。</p>
<h3>构建和发布</h3>
<p>接下来，我们可以停止开发服务器，运行 <code>npm run build-release</code>。如果你的 package.json 里的版本号是 1.0.0，那么它将在 dist 目录下生成 demo-1.0.0.min.js。这是一个 umd 的包，所以你可以在浏览器中使用 amd/cmd 库加载或者直接在 script 标签中引入和使用。</p>
<h2>总结</h2>
<p>我们使用 webpack 搭建了一个简单的组件开发环境，这样我们可以简单地开始我们的 JS 组件开发，使用新的语言规范，然后通过 webpack-dev-server 代理 http-server 进行调试，通过 webpack --env.production 进行发布。我们还可以将它们与 NPM Scripts 集成，这样我们的组件开发就非常方便了。</p>
<p>你喜欢的组件开发方式是怎样的？欢迎在评论区讨论。</p>
---------------
<h1 id="#title_2" >3、文章： 基于虚拟化的安全性 - 第2篇：内核通信</h1>
Adrien Chevalier
[http://www.infoq.com/cn/articles/virtualization-based-security-part02?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/virtualization-based-security-part02?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/virtualization-based-security-part02/zh/smallimage/shanshangjiaoxia.jpg"/><p>本文是第二篇文章，涉及基于虚拟化的安全和设备保护功能。在第一篇中，我们介绍了从Windows引导加载程序到VTL0启动的系统引导过程。在这篇文章中，我们将解释VTL0和VTL1之间如何进行内核通信。当它们使用超级调用进行通信时，我们将首先描述Hyper-V的超级调用实现，然后内核如何使用它们进行通信。为了完成这一描述，我们将列出这项工作中我们发现的所有不同的超级调用和安全服务调用。</p> <i>By Adrien Chevalier</i> <i> Translated by 刘志勇</i>
---------------
<h1 id="#title_3" >4、视频演讲： 网格社区：闲鱼技术架构体系演进</h1>
孙兵（酒丐）
[http://www.infoq.com/cn/presentations/the-evolution-of-xianyu-technology-architecture?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/the-evolution-of-xianyu-technology-architecture?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/the-evolution-of-xianyu-technology-architecture/zh/mediumimage/sunbing270.jpg"/><p>贴合消费升级、人们对绿色生活方式的认同，闲置交易已成为人们生活的一种新常态。闲鱼自2014年成立至今，当前已累计超过1亿实名认证用户，成为国内最大闲置交易平台，在这样一个以非专业卖家为主的共享经济平台中，如何有效的组织用户，建立用户之间的信任关系并形成互惠的闲置交易，闲鱼在社区的建立与发展做了大量业务和产品技术的尝试。</p> <i>By 孙兵（酒丐）</i>
---------------
<h1 id="#title_4" >5、文章： 叶亚明：合格CTO的六要素</h1>
InfoQ
[http://www.infoq.com/cn/articles/six-elements-of-a-qualified-cto?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/six-elements-of-a-qualified-cto?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/six-elements-of-a-qualified-cto/zh/smallimage/change_logo.jpg"/><p>本文分享了作者（叶亚明）分享了在携程5年间经历的很多事情，并进行了归纳了一下，希望通过分享引起一些共鸣。 </p> <i>By InfoQ</i>
---------------
<h1 id="#title_5" >6、迷你书： 架构师（2017年3月）</h1>
InfoQ中文站
[http://www.infoq.com/cn/minibooks/architect-201703?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/minibooks/architect-201703?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/minibooks/architect-201703/zh/smallimage/100.jpg"/><p>本期主要内容：谷歌新发布的分布式数据库服务；Yahoo开源TensorFlowOnSpark；百亿级微信红包的高并发资金交易系统设计方案；复盘GC算法的发展历程及现状</p> <i>By InfoQ中文站</i>
---------------
<h1 id="#title_6" >7、从反应式到预测式，全域大数据的技术演进解析</h1>
曹倩芸
[http://www.infoq.com/cn/news/2017/03/youmeng-bigdata-interview?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/03/youmeng-bigdata-interview?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>目前，国内一批大数据企业都开始致力于此项技术的研究和探索——即围绕用户的使用过程来打造一对一的体验。从已掌握的、能体现用户在某个特定过程的数据入手，厘清这些数据将在接下来的哪些互动环节提供支持与帮助，从而据此制定具体的互动体验。因此，这一过程也将改变企业开展业务的方式——从反应式到主动式和预测式。</p> <i>By 曹倩芸</i>
---------------
<h1 id="#title_7" >8、人为失误导致AWS S3的US-EAST-1区服务宕机</h1>
Abel Avram
[http://www.infoq.com/cn/news/2017/03/aws-s3-disruption?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/03/aws-s3-disruption?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>由一次人为失误引发的连锁反应导致了很多S3服务器宕机，其中包括两个影响S3运行的关键子系统。由此导致了S3的故障，影响到了不仅S3本身还有其他一些依赖S3的服务。四个小时后S3才重新恢复正常。</p> <i>By Abel Avram</i> <i> Translated by Rays</i>
---------------
<h1 id="#title_8" >9、Swift内存所有权宣言</h1>
Sergio De Simone
[http://www.infoq.com/cn/news/2017/03/swift-memory-ownership-model?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/03/swift-memory-ownership-model?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>据Swift的创建者和前团队负责人Chris Lattner介绍，Swift 4的主要目标之一就是要定义一个类似于Rust/Cyclone的内存所有权模型。在当前Swift 4已进入第二阶段的情况下，Swift团队发布了一个详细阐明Swift内存所有权工作方式的宣言。</p> <i>By Sergio De Simone</i> <i> Translated by Rays</i>
---------------
<h1 id="#title_9" >10、文章： Chrome 56已经支持图像识别 API（Shape Detection API）</h1>
Miguel Casas-Sanchez (GoogleInc）
[http://www.infoq.com/cn/articles/chrome-shape-detection?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/chrome-shape-detection?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/articles/chrome-shape-detection/zh/smallimage/xx_logo (2).jpg"/><p>本文档描述了一套Chrome中针对静态和/或动态图像的图形识别（如：人脸识别）API。</p> <i>By Miguel Casas-Sanchez (GoogleInc）</i> <i> Translated by 谈浩</i>
---------------
<h1 id="#title_10" >11、Java性能最后一个领域：去除垃圾回收器</h1>
Abraham Marín Pérez
[http://www.infoq.com/cn/news/2017/03/java-epsilon-gc?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/03/java-epsilon-gc?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>一份新提交的JEP草案提到创建一个无操作的垃圾回收器：一种不进行实际内存回收的GC方式。该GC方式旨在帮助JVM实现者和研究者，以及少部分无需垃圾回收的超高性能应用程序。如果这项JEP继续推进，新的GC方式将会和现有GC方式一起存在，并且通过显式激活方式使用。</p> <i>By Abraham Marín Pérez</i> <i> Translated by 金灵杰</i>
---------------
<h1 id="#title_11" >12、Jay Simons谈Atlassian收购Trello</h1>
Rui Miguel Ferreira
[http://www.infoq.com/cn/news/2017/03/atlassian-acquires-trello?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/03/atlassian-acquires-trello?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>2017年1月9日，Atlassian公司（一个团队协作和生产力解决提供商）宣布公司已经就收购Trello达成协议，Trello是一个可视化工具，其利用看板帮助团队和个人管理他们的项目和任务。</p> <i>By Rui Miguel Ferreira</i> <i> Translated by 麦克周</i>
---------------
<h1 id="#title_12" >13、微软开源基于云的生理学研究工具</h1>
Michael Stiefel
[http://www.infoq.com/cn/news/2017/03/Microsoft-cloud-biological-resea?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/03/Microsoft-cloud-biological-resea?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Bio Model Analyzer是一款微软基于云的生理学研究工具，可以用于对细胞交互和通信进行建模，现已经在GitHub上开源，在MIT许可之下。研究人员使用Bio Model Analyzer (BMA) 去创建计算机模型，该模型可以比较健康和不健康细胞内的处理。BMA模型可以使科学家看到成千上万个基因和蛋白质的相互使用，加快疾病的研究和治疗速度。</p> <i>By Michael Stiefel</i> <i> Translated by 冬雨</i>
---------------
<h1 id="#title_13" >14、Deeplearning4j：如何建设深度学习开源社区</h1>
Ola Kohut
[http://www.infoq.com/cn/news/2017/03/Deeplearning4j-how-deep-study?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/03/Deeplearning4j-how-deep-study?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Deeplearning4j是第一个为 Java和 Scala编写的商业级、开源、分布式神经网络库，它是 Gitter上最活跃的社区之一。 Gitter采访了 Deeplearning4j的创始人Adam和 Chris，分享了他们在开源社区建设方面的想法、经验和教训。本访谈内容可以在 Gitter上的 deeplearning4j频道观看。</p> <i>By Ola Kohut</i> <i> Translated by 刘志勇</i>
---------------
<h1 id="#title_14" >15、学习机器学习之如何根据需求选择一种算法</h1>
麦克周
[http://www.infoq.com/cn/news/2017/03/Learning-machine-Demand-selectio?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2017/03/Learning-machine-Demand-selectio?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>随着机器学习的进一步火热，越来越多的算法已经可以用在许多任务的执行上，并且表现出色。 但是动手之前到底哪个算法可以解决我们特定的实际问题并且运行效果良好，这个答案很多新手是不知道的。如果你处理问题时间可以很长，你可以逐个调研并且尝试它们，反之则要在最短的时间内解决技术调研任务。 Michael Beyeler的一篇文章告诉我们整个技术选型过程，一步接着一步，依靠已知的技术，从模型选择到超参数调整。</p> <i>By 麦克周</i>
---------------
<h1 id="#title_15" >16、视频演讲： 什么是架构的极致？——由 IoT 核心参考架构 Sluff 带来的思考</h1>
周爱民
[http://www.infoq.com/cn/presentations/the-ultimate-architecture-thinking-from-iot-core-reference-architecture-sluff?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/the-ultimate-architecture-thinking-from-iot-core-reference-architecture-sluff?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/resource/presentations/the-ultimate-architecture-thinking-from-iot-core-reference-architecture-sluff/zh/mediumimage/zhouaimin270.jpg"/><p>IoT 领域中已经有太多的公司或组织提出他们的『物联网参考架构』，然而多数情况下这些架构的设计目的只是为了『装进更多他们的产品』。在本次分享中，我将从领域模型谈起，从解决真实的领域问题出发来提出一个『核心参考架构』。在这个过程中，我们以追求极致为最终理念，一方面实现了对现有其它参考架构的一个归纳萃取，另一方面也提供了在分析、设计与实现三方面高度一致的真实可用的架构模型：Sluff。我在分享中将会介绍整个架构分析、设计与实现的全程，以及其中的种种权衡。
在 Sluff 这个标准的核心参考架构的基础上，我们基于 NodeJS 提交了它的一个具体实现。本次分享中，我也将介绍这个项目/产品的进展以及特性：一定程度上，它是 IoT 的一个参考运行框架。</p> <i>By 周爱民</i>
---------------
<h1 id="#title_16" >17、How To Simplify Networking In Android: Introducing The Volley HTTP Library</h1>
Chetan Giridhar
[https://www.smashingmagazine.com/2017/03/simplify-android-networking-volley-http-library/](https://www.smashingmagazine.com/2017/03/simplify-android-networking-volley-http-library/)
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
</table><p>In a world driven by the Internet, <strong>mobile apps need to share and receive information</strong> from their products' back end (for example, from databases) as well as from third-party sources such as Facebook and Twitter.</p>

<figure></figure>

<p>These interactions are often made through RESTful APIs. When the number of requests increases, the way these requests are made becomes very critical to development, because the manner in which you fetch data can really affect the user experience of an app.</p><p>The post .</p>
---------------
<h1 id="#title_17" >18、Hibernation Time Is Over! Inspiring Desktop Wallpapers To Fuel Your Creativity (March 2017 Edition)</h1>
Cosima Mielke
[https://www.smashingmagazine.com/2017/02/hibernation-time-is-over-inspiring-desktop-wallpapers-to-fuel-your-creativity/](https://www.smashingmagazine.com/2017/02/hibernation-time-is-over-inspiring-desktop-wallpapers-to-fuel-your-creativity/)
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
</table><p>Sometimes all we need is a little <strong>inspiration kick to get our creative juices flowing</strong>. Maybe your secret is to go for a short walk, have a little chat with a colleague, or scroll through your favorite eye candy resources. Whatever it might be that helps you get new ideas, we, too, have something for you that could work just as good: desktop wallpapers.</p>

<figure></figure>

<p>To bring you a regular dose of unique and inspiring wallpapers, we embarked on our .</p>
---------------