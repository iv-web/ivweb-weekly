## 文章索引
1、 <a href="#1简单构建-thinkjs-+-vue20-前后端分离的多页应用" >简单构建 ThinkJS + Vue2.0 前后端分离的多页应用</a><br/>
2、 <a href="#2文章-集成学习算法ensemble-method浅析" >文章： 集成学习算法（Ensemble Method）浅析</a><br/>
3、 <a href="#3视频访谈-李小龙链家一站式数据管理平台的发展与展望" >视频访谈： 李小龙：链家一站式数据管理平台的发展与展望</a><br/><h1 id="#title_0" >1、简单构建 ThinkJS + Vue2.0 前后端分离的多页应用</h1>

[https://www.h5jun.com/post/thinkjs-vue2.0-build.html](https://www.h5jun.com/post/thinkjs-vue2.0-build.html)
<div class="toc"><ul>
<li></li>
<li></li>
<li></li>
<li></li>
<li></li>
</ul>
</div><p>最近在使用 ThinkJS + Vue2.0 写一个简单的项目，该项目分为用户端和管理界面，分别对应vue的两个页面<code>index</code>和<code>admin</code>，用户端、管理界面自身是基于vue构建的单页应用，服务端采用thinkjs的提供api。</p>
<p>项目目录结构如下：</p>
<pre><code class="hljs lang-stylus">.
├── README<span class="hljs-selector-class">.md</span>
├── client
│   ├── README<span class="hljs-selector-class">.md</span>
│   ├── build
│   ├── config
│   ├── package<span class="hljs-selector-class">.json</span>
│   ├── src
│   │   ├── components
│   │   ├── modules
│   │   └── pages
│   │       ├── admin
│   │       └── index
│   └── static
└── server
    ├── src
    │   ├── bootstrap
    │   ├── config
    │   ├── controller
    │   │   ├── admin
    │   │   ├── base<span class="hljs-selector-class">.js</span>
    │   │   ├── home
    │   │   └── index<span class="hljs-selector-class">.js</span>
    │   ├── logic
    │   └── model
    ├── view
    │   ├── admin<span class="hljs-selector-class">.html</span>
    │   └── index<span class="hljs-selector-class">.html</span>
    └── www
        └── static
</code></pre><h3>client 的配置</h3>
<p>直接使用vue官方的创建项目，选择使用webpack构建。</p>
<p>修改<code>config/index.js</code>，给webpack-dev-server添加proxyTable:</p>
<pre><code class="hljs lang-js">    proxyTable: {
      <span class="hljs-string">'/api'</span> :  {
        target: <span class="hljs-string">'http://localhost:8360/api/'</span>,
        changeOrigin: <span class="hljs-literal">true</span>,
        pathRewrite: {
          <span class="hljs-string">'^/api'</span>: <span class="hljs-string">'/'</span>
        }
      }
    },
</code></pre>
<p>然后参照《》的方法将其改为多页应用，具体方法为：</p>
<p>调整项目目录，创建<code>src/pages/index</code>，将<code>src/assets</code>、<code>src/router</code>、<code>src/App.vue</code>、<code>src/main.js</code>和<code>./index.html</code>移动到该目录中，并将<code>main.js</code>改名为<code>index.js</code>。</p>
<p>修改构建脚本<code>build/utils.js</code>，添加：</p>
<pre><code class="hljs lang-js"><span class="hljs-comment">// glob是webpack安装时依赖的一个第三方模块，还模块允许你使用 *等符号, 例如lib/*.js就是获取lib文件夹下的所有js后缀名的文件</span>
<span class="hljs-keyword">var</span> glob = <span class="hljs-built_in">require</span>(<span class="hljs-string">'glob'</span>)
    <span class="hljs-comment">// 页面模板</span>
<span class="hljs-keyword">var</span> HtmlWebpackPlugin = <span class="hljs-built_in">require</span>(<span class="hljs-string">'html-webpack-plugin'</span>)
<span class="hljs-comment">// 取得相应的页面路径，因为之前的配置，所以是src文件夹下的pages文件夹</span>
<span class="hljs-keyword">var</span> PAGE_PATH = path.resolve(__dirname, <span class="hljs-string">'../src/pages'</span>)
    <span class="hljs-comment">// 用于做相应的merge处理</span>
<span class="hljs-keyword">var</span> merge = <span class="hljs-built_in">require</span>(<span class="hljs-string">'webpack-merge'</span>)


<span class="hljs-comment">//多入口配置</span>
<span class="hljs-comment">// 通过glob模块读取pages文件夹下的所有对应文件夹下的js后缀文件，如果该文件存在</span>
<span class="hljs-comment">// 那么就作为入口处理</span>
exports.entries = <span class="hljs-function"><span class="hljs-keyword">function</span>(<span class="hljs-params"></span>) </span>{
    <span class="hljs-keyword">var</span> entryFiles = glob.sync(PAGE_PATH + <span class="hljs-string">'/*/*.js'</span>)
    <span class="hljs-keyword">var</span> map = {}
    entryFiles.forEach((filePath) =&gt; {
        <span class="hljs-keyword">var</span> filename = filePath.substring(filePath.lastIndexOf(<span class="hljs-string">'\/'</span>) + <span class="hljs-number">1</span>, filePath.lastIndexOf(<span class="hljs-string">'.'</span>))
        map[filename] = filePath
    })
    <span class="hljs-keyword">return</span> map
}

<span class="hljs-comment">//多页面输出配置</span>
<span class="hljs-comment">// 与上面的多页面入口配置相同，读取pages文件夹下的对应的html后缀文件，然后放入数组中</span>
exports.htmlPlugin = <span class="hljs-function"><span class="hljs-keyword">function</span>(<span class="hljs-params"></span>) </span>{
    <span class="hljs-keyword">let</span> entryHtml = glob.sync(PAGE_PATH + <span class="hljs-string">'/*/*.html'</span>)
    <span class="hljs-keyword">return</span> entryHtml.map((filePath) =&gt; {
        <span class="hljs-keyword">let</span> filename = filePath.substring(filePath.lastIndexOf(<span class="hljs-string">'\/'</span>) + <span class="hljs-number">1</span>, filePath.lastIndexOf(<span class="hljs-string">'.'</span>))
        <span class="hljs-keyword">let</span> conf = {
            <span class="hljs-comment">// 模板来源</span>
            template: filePath,
            <span class="hljs-comment">// 文件名称</span>
            filename: filename + <span class="hljs-string">'.html'</span>,
            <span class="hljs-comment">// 页面模板需要加对应的js脚本，如果不加这行则每个页面都会引入所有的js脚本</span>
            chunks: [<span class="hljs-string">'manifest'</span>, <span class="hljs-string">'vendor'</span>, filename],
            inject: <span class="hljs-literal">true</span>
        }
        <span class="hljs-keyword">if</span> (process.env.NODE_ENV === <span class="hljs-string">'production'</span>) {
            conf = merge(conf, {
                minify: {
                    removeComments: <span class="hljs-literal">true</span>,
                    collapseWhitespace: <span class="hljs-literal">true</span>,
                    removeAttributeQuotes: <span class="hljs-literal">true</span>
                },
                chunksSortMode: <span class="hljs-string">'dependency'</span>
            })
        }
        <span class="hljs-keyword">return</span> <span class="hljs-keyword">new</span> HtmlWebpackPlugin(conf)
    })
}
</code></pre>
<p>修改<code>build/webpack.base.conf.js</code>的入口配置：</p>
<pre><code class="hljs lang-js"><span class="hljs-built_in">module</span>.exports = {
  context: path.resolve(__dirname, <span class="hljs-string">'../'</span>),
  entry: utils.entries(),

  ...
  ...
}
</code></pre>
<p>修改<code>build/webpack.dev.conf.js</code>和<code>build/webpack.prod.conf.js</code>的插件配置：</p>
<pre><code class="hljs lang-js">  plugins: [
    ...

    <span class="hljs-comment">// https://github.com/ampedandwired/html-webpack-plugin</span>
    ...utils.htmlPlugin(),

    ...
  ]
</code></pre>
<p>创建 <code>src/pages/admin</code> 目录，添加<code>admin.html</code>文件：</p>
<pre><code class="hljs lang-html"><span class="hljs-meta">&lt;!DOCTYPE html&gt;</span>
<span class="hljs-tag">&lt;<span class="hljs-name">html</span> <span class="hljs-attr">lang</span>=<span class="hljs-string">"en"</span>&gt;</span>
<span class="hljs-tag">&lt;<span class="hljs-name">head</span>&gt;</span>
  <span class="hljs-tag">&lt;<span class="hljs-name">meta</span> <span class="hljs-attr">charset</span>=<span class="hljs-string">"UTF-8"</span>&gt;</span>
  <span class="hljs-tag">&lt;<span class="hljs-name">meta</span> <span class="hljs-attr">name</span>=<span class="hljs-string">"viewport"</span> <span class="hljs-attr">content</span>=<span class="hljs-string">"width=device-width, initial-scale=1.0"</span>&gt;</span>
  <span class="hljs-tag">&lt;<span class="hljs-name">meta</span> <span class="hljs-attr">http-equiv</span>=<span class="hljs-string">"X-UA-Compatible"</span> <span class="hljs-attr">content</span>=<span class="hljs-string">"ie=edge"</span>&gt;</span>
  <span class="hljs-tag">&lt;<span class="hljs-name">title</span>&gt;</span>Document<span class="hljs-tag">&lt;/<span class="hljs-name">title</span>&gt;</span>
<span class="hljs-tag">&lt;/<span class="hljs-name">head</span>&gt;</span>
<span class="hljs-tag">&lt;<span class="hljs-name">body</span>&gt;</span>
  <span class="hljs-tag">&lt;<span class="hljs-name">h1</span>&gt;</span>Admin<span class="hljs-tag">&lt;/<span class="hljs-name">h1</span>&gt;</span>
<span class="hljs-tag">&lt;/<span class="hljs-name">body</span>&gt;</span>
<span class="hljs-tag">&lt;/<span class="hljs-name">html</span>&gt;</span>
</code></pre>
<p>创建 <code>src/pages/404</code> 目录，添加<code>404.html</code>文件：</p>
<pre><code class="hljs lang-html"><span class="hljs-meta">&lt;!DOCTYPE html&gt;</span>
<span class="hljs-tag">&lt;<span class="hljs-name">html</span> <span class="hljs-attr">lang</span>=<span class="hljs-string">"en"</span>&gt;</span>
<span class="hljs-tag">&lt;<span class="hljs-name">head</span>&gt;</span>
  <span class="hljs-tag">&lt;<span class="hljs-name">meta</span> <span class="hljs-attr">charset</span>=<span class="hljs-string">"UTF-8"</span>&gt;</span>
  <span class="hljs-tag">&lt;<span class="hljs-name">meta</span> <span class="hljs-attr">name</span>=<span class="hljs-string">"viewport"</span> <span class="hljs-attr">content</span>=<span class="hljs-string">"width=device-width, initial-scale=1.0"</span>&gt;</span>
  <span class="hljs-tag">&lt;<span class="hljs-name">meta</span> <span class="hljs-attr">http-equiv</span>=<span class="hljs-string">"X-UA-Compatible"</span> <span class="hljs-attr">content</span>=<span class="hljs-string">"ie=edge"</span>&gt;</span>
  <span class="hljs-tag">&lt;<span class="hljs-name">title</span>&gt;</span>404<span class="hljs-tag">&lt;/<span class="hljs-name">title</span>&gt;</span>
<span class="hljs-tag">&lt;/<span class="hljs-name">head</span>&gt;</span>
<span class="hljs-tag">&lt;<span class="hljs-name">body</span>&gt;</span>
  <span class="hljs-tag">&lt;<span class="hljs-name">h1</span>&gt;</span>404 Not Found<span class="hljs-tag">&lt;/<span class="hljs-name">h1</span>&gt;</span>
<span class="hljs-tag">&lt;/<span class="hljs-name">body</span>&gt;</span>
<span class="hljs-tag">&lt;/<span class="hljs-name">html</span>&gt;</span>
</code></pre>
<p>修改webpack-dev-server的路由表：</p>
<pre><code class="hljs lang-js">    historyApiFallback: {
      rewrites: [
        { <span class="hljs-keyword">from</span>: <span class="hljs-regexp">/^\/$/</span>, to: <span class="hljs-string">'/index.html'</span> },
        { <span class="hljs-keyword">from</span>: <span class="hljs-regexp">/^\/admin\/?$/</span>, to: <span class="hljs-string">'/admin.html'</span> },
        { <span class="hljs-keyword">from</span>: <span class="hljs-regexp">/./</span>, to: <span class="hljs-string">'/404.html'</span> }
      ],
    },
</code></pre>
<p>至此client端的配置就完成了，可以通过 <code>npm start</code> 启动client端，通过 <code>http://localhost:8080</code> 访问页面。</p>
<h3>server 的配置</h3>
<p>直接使用ThinkJS官方的创建项目，修改<code>src/config/router.js</code>，添加路由：</p>
<pre><code class="hljs lang-js"><span class="hljs-built_in">module</span>.exports = [
  [<span class="hljs-regexp">/^\/api\/(.*)/i</span>, <span class="hljs-string">'/:1'</span>],
  [<span class="hljs-regexp">/^\/$/i</span>, <span class="hljs-string">'/'</span>],
  [<span class="hljs-regexp">/^\/admin\/?$/i</span>, <span class="hljs-string">'/index/admin'</span>],
  [<span class="hljs-regexp">/\//</span>, <span class="hljs-string">'index/_404'</span>, <span class="hljs-string">'get'</span>]
];
</code></pre>
<p>修改<code>src/controller/index.js</code>渲染模板：</p>
<pre><code class="hljs lang-js"><span class="hljs-keyword">const</span> Base = <span class="hljs-built_in">require</span>(<span class="hljs-string">'./base.js'</span>);

<span class="hljs-built_in">module</span>.exports = <span class="hljs-class"><span class="hljs-keyword">class</span> <span class="hljs-keyword">extends</span> <span class="hljs-title">Base</span> </span>{
  indexAction() {
    <span class="hljs-keyword">return</span> <span class="hljs-keyword">this</span>.display(<span class="hljs-string">'index.html'</span>);
  }
  adminAction() {
    <span class="hljs-keyword">return</span> <span class="hljs-keyword">this</span>.display(<span class="hljs-string">'admin.html'</span>);
  }
  _404Action() {
    <span class="hljs-keyword">return</span> <span class="hljs-keyword">this</span>.display(<span class="hljs-string">'404.html'</span>);
  }
};
</code></pre>
<p>至此服务器的配置完成，启动server端，client 可通过 <code>http://localhost:8080/api</code> 访问API。</p>
<h3>开发服务端 API</h3>
<p>在 server 中任意 controller 暴露的 API 可以通过 <code>/api/controller/action</code> 来访问，比如：</p>
<pre><code class="hljs lang-js"><span class="hljs-comment">// src/controller/test.js</span>
<span class="hljs-keyword">const</span> Base = <span class="hljs-built_in">require</span>(<span class="hljs-string">'./base.js'</span>);

<span class="hljs-built_in">module</span>.exports = <span class="hljs-class"><span class="hljs-keyword">class</span> <span class="hljs-keyword">extends</span> <span class="hljs-title">Base</span> </span>{
  indexAction() {
    <span class="hljs-keyword">return</span> <span class="hljs-keyword">this</span>.success(<span class="hljs-string">'test'</span>);
  }
};
</code></pre>
<p>可以通过 <code>http://localhost:8080/api/test</code> 访问：</p>
<pre><code class="hljs lang-js">{
  errno: <span class="hljs-number">0</span>,
  errmsg: <span class="hljs-string">""</span>,
  data: <span class="hljs-string">"test"</span>
}
</code></pre>
<h3>添加新页面 abc</h3>
<p>在 client 的 <code>src/pages</code> 目录下创建新的页面 <code>src/pages/abc/abc.html</code>，同时修改 <code>webpack.dev.config.js</code>，historyApiFallback 中添加新的页面路由。</p>
<pre><code class="hljs lang-js">    historyApiFallback: {
      rewrites: [
        { <span class="hljs-keyword">from</span>: <span class="hljs-regexp">/^\/$/</span>, to: <span class="hljs-string">'/index.html'</span> },
        { <span class="hljs-keyword">from</span>: <span class="hljs-regexp">/^\/admin\/?$/</span>, to: <span class="hljs-string">'/admin.html'</span> },
        { <span class="hljs-keyword">from</span>: <span class="hljs-regexp">/^\/abc\/?$/</span>, to: <span class="hljs-string">'/abc.html'</span> },
        { <span class="hljs-keyword">from</span>: <span class="hljs-regexp">/./</span>, to: <span class="hljs-string">'/404.html'</span> }
      ],
    },
</code></pre>
<p>在 server 的 <code>src/controller/index.js</code> 中创建新的 action</p>
<pre><code class="hljs lang-js"><span class="hljs-keyword">const</span> Base = <span class="hljs-built_in">require</span>(<span class="hljs-string">'./base.js'</span>);

<span class="hljs-built_in">module</span>.exports = <span class="hljs-class"><span class="hljs-keyword">class</span> <span class="hljs-keyword">extends</span> <span class="hljs-title">Base</span> </span>{
  ...
  abcAction() {
    <span class="hljs-keyword">return</span> <span class="hljs-keyword">this</span>.display(<span class="hljs-string">'abc.html'</span>);
  }
  _404Action() {
    <span class="hljs-keyword">return</span> <span class="hljs-keyword">this</span>.display(<span class="hljs-string">'404.html'</span>);
  }
};
</code></pre>
<p>修改 router.js 添加新路由：</p>
<pre><code class="hljs lang-js"><span class="hljs-built_in">module</span>.exports = [
  [<span class="hljs-regexp">/^\/api\/(.*)/i</span>, <span class="hljs-string">'/:1'</span>],
  [<span class="hljs-regexp">/^\/$/i</span>, <span class="hljs-string">'/'</span>],
  [<span class="hljs-regexp">/^\/admin\/?$/i</span>, <span class="hljs-string">'/index/admin'</span>],
  [<span class="hljs-regexp">/^\/abc\/?$/i</span>, <span class="hljs-string">'/index/abc'</span>],
  [<span class="hljs-regexp">/\//</span>, <span class="hljs-string">'index/_404'</span>, <span class="hljs-string">'get'</span>]
];
</code></pre>
<p>分别重启sever、client即可。</p>
<h3>生产环境构建</h3>
<p>生产环境构建非常简单，直接在client下运行<code>npm run build</code>，将<code>dist</code>下生成的文件<code>*.html</code>拷贝到server的<code>view</code>目录下，将<code>dist/static</code>目录拷贝到server的<code>www</code>目录下，然后将server部署到生产环境运行即可。</p>
---------------
<h1 id="#title_1" >2、文章： 集成学习算法（Ensemble Method）浅析</h1>
陈祥龙
[http://www.infoq.com/cn/articles/ensemble-method?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/ensemble-method?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/ensemble-method/zh/smallimage/DNUN-logo-small-1526314993792.jpg"/><p>集成学习算法本身不算一种单独的机器学习算法，而是通过构建并结合多个机器学习器来完成学习任务。可以说是集百家 之所长，能在机器学习算法中拥有较高的准确率，不足之处就是模型的训练过程可能比较复杂，效率不是很高。</p> <i>By 陈祥龙</i>
---------------
<h1 id="#title_2" >3、视频访谈： 李小龙：链家一站式数据管理平台的发展与展望</h1>
李小龙
[http://www.infoq.com/cn/interviews/interview-with-lixiaolong-talk-lianjia-date-plantform?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/interviews/interview-with-lixiaolong-talk-lianjia-date-plantform?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/interviews/interview-with-lixiaolong-talk-lianjia-date-plantform/zh/mediumimage/lixiaolong270-1526805075271.jpg"/><p>我们在QCon 全球软件开发大会，2018北京站的现场，很荣幸地采访到了来自链家大数据平台的李小龙先生，请他来谈谈链家一站式数据平台的发展与技术特点。</p> <i>By 李小龙</i>
---------------