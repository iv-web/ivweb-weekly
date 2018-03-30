## 文章索引
1、 <a href="#1react-v1630:-new-lifecycles-and-context-api" >React v16.3.0: New lifecycles and context API</a><br/>
2、 <a href="#2文章-任何人都可以借助workers在cloudflare上运行javascript了" >文章： 任何人都可以借助Workers在Cloudflare上运行JavaScript了</a><br/>
3、 <a href="#3文章-用深度学习解决冯-诺依曼结构内存性能瓶颈" >文章： 用深度学习解决冯-诺依曼结构内存性能瓶颈</a><br/>
4、 <a href="#4understanding-logical-properties-and-values" >Understanding Logical Properties And Values</a><br/>
5、 <a href="#5视频演讲-如何构建低成本高效能的视觉感知系统" >视频演讲： 如何构建低成本高效能的视觉感知系统</a><br/>
6、 <a href="#6视频演讲-解锁深度视频理解的潜力" >视频演讲： 解锁深度视频理解的潜力</a><br/>
7、 <a href="#7谈笔1000亿的生意揭秘菜鸟全球智能仓配技术实践" >谈笔1000亿的生意：揭秘菜鸟全球智能仓配技术实践</a><br/>
8、 <a href="#8文章-虚拟现实将颠覆敏捷教练和指导方式" >文章： 虚拟现实将颠覆敏捷教练和指导方式</a><br/>
9、 <a href="#9无人驾驶汽车致人死亡" >无人驾驶汽车致人死亡</a><br/>
10、 <a href="#10gitlab揭示devops价值和挑战的新调查研究" >GitLab揭示DevOps价值和挑战的新调查研究</a><br/>
11、 <a href="#11github安全告警检测出了400多万个漏洞" >GitHub安全告警检测出了400多万个漏洞</a><br/>
12、 <a href="#12打造敏捷公司" >打造敏捷公司</a><br/>
13、 <a href="#13#smoosh门引发web兼容性上的挑战" >“#smoosh门”引发Web兼容性上的挑战</a><br/>
14、 <a href="#14左耳朵耗子从亚马逊的实践谈分布式系统的难点" >左耳朵耗子：从亚马逊的实践，谈分布式系统的难点</a><br/>
15、 <a href="#15文章-saas的窘境与未来缺少服务难成气候" >文章： SaaS的窘境与未来：缺少服务，难成气候？</a><br/><h1 id="#title_0" >1、React v16.3.0: New lifecycles and context API</h1>

[https://reactjs.org/blog/2018/03/29/react-v-16-3.html](https://reactjs.org/blog/2018/03/29/react-v-16-3.html)
<p>A few days ago, we , including gradual migration strategies. In React 16.3.0, we are adding a few new lifecycle methods to assist with that migration. We are also introducing new APIs for long requested features: an official context API, a ref forwarding API, and an ergonomic ref API.</p>
<p>Read on to learn more about the release.</p>
<h2 id="official-context-api">Official Context API</h2>
<p>For many years, React has offered an experimental API for context. Although it was a powerful tool, its use was discouraged because of inherent problems in the API, and because we always intended to replace the experimental API with a better one.</p>
<p>Version 16.3 introduces a new context API that is more efficient and supports both static type checking and deep updates.</p>
<blockquote>
<p><strong>Note</strong></p>
<p>The old context API will keep working for all React 16.x releases, so you will have time to migrate.</p>
</blockquote>
<p>Here is an example illustrating how you might inject a “theme” using the new context API:
<div class="gatsby-highlight">
        <pre class="gatsby-code-jsx"><code><span class="gatsby-highlight-code-line"><span class="token keyword">const</span> ThemeContext <span class="token operator">=</span> React<span class="token punctuation">.</span><span class="token function">createContext</span><span class="token punctuation">(</span><span class="token string">'light'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</span>
<span class="token keyword">class</span> <span class="token class-name">ThemeProvider</span> <span class="token keyword">extends</span> <span class="token class-name">React<span class="token punctuation">.</span>Component</span> <span class="token punctuation">{</span>
  state <span class="token operator">=</span> <span class="token punctuation">{</span>theme<span class="token punctuation">:</span> <span class="token string">'light'</span><span class="token punctuation">}</span><span class="token punctuation">;</span>

  <span class="token function">render</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token keyword">return</span> <span class="token punctuation">(</span>
<span class="gatsby-highlight-code-line">      <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>ThemeContext.Provider</span> <span class="token attr-name">value</span><span class="token script language-javascript"><span class="token punctuation">=</span><span class="token punctuation">{</span><span class="token keyword">this</span><span class="token punctuation">.</span>state<span class="token punctuation">.</span>theme<span class="token punctuation">}</span></span><span class="token punctuation">></span></span>
</span><span class="gatsby-highlight-code-line">        <span class="token punctuation">{</span><span class="token keyword">this</span><span class="token punctuation">.</span>props<span class="token punctuation">.</span>children<span class="token punctuation">}</span>
</span><span class="gatsby-highlight-code-line">      <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>ThemeContext.Provider</span><span class="token punctuation">></span></span>
</span>    <span class="token punctuation">)</span><span class="token punctuation">;</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>

<span class="token keyword">class</span> <span class="token class-name">ThemedButton</span> <span class="token keyword">extends</span> <span class="token class-name">React<span class="token punctuation">.</span>Component</span> <span class="token punctuation">{</span>
  <span class="token function">render</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token keyword">return</span> <span class="token punctuation">(</span>
<span class="gatsby-highlight-code-line">      <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>ThemeContext.Consumer</span><span class="token punctuation">></span></span>
</span><span class="gatsby-highlight-code-line">        <span class="token punctuation">{</span>theme <span class="token operator">=></span> <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>Button</span> <span class="token attr-name">theme</span><span class="token script language-javascript"><span class="token punctuation">=</span><span class="token punctuation">{</span>theme<span class="token punctuation">}</span></span> <span class="token punctuation">/></span></span><span class="token punctuation">}</span>
</span><span class="gatsby-highlight-code-line">      <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>ThemeContext.Consumer</span><span class="token punctuation">></span></span>
</span>    <span class="token punctuation">)</span><span class="token punctuation">;</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>
        </div></p>
<p></p>
<h2 id="createref-api"><code>createRef</code> API</h2>
<p>Previously, React provided two ways of managing refs: the legacy string ref API and the callback API. Although the string ref API was the more convenient of the two, it had  and so our official recommendation was to use the callback form instead.</p>
<p>Version 16.3 adds a new option for managing refs that offers the convenience of a string ref without any of the downsides:
<div class="gatsby-highlight">
        <pre class="gatsby-code-jsx"><code><span class="token keyword">class</span> <span class="token class-name">MyComponent</span> <span class="token keyword">extends</span> <span class="token class-name">React<span class="token punctuation">.</span>Component</span> <span class="token punctuation">{</span>
  <span class="token function">constructor</span><span class="token punctuation">(</span>props<span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token keyword">super</span><span class="token punctuation">(</span>props<span class="token punctuation">)</span><span class="token punctuation">;</span>

<span class="gatsby-highlight-code-line">    <span class="token keyword">this</span><span class="token punctuation">.</span>inputRef <span class="token operator">=</span> React<span class="token punctuation">.</span><span class="token function">createRef</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</span>  <span class="token punctuation">}</span>

  <span class="token function">render</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
<span class="gatsby-highlight-code-line">    <span class="token keyword">return</span> <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>text<span class="token punctuation">"</span></span> <span class="token attr-name">ref</span><span class="token script language-javascript"><span class="token punctuation">=</span><span class="token punctuation">{</span><span class="token keyword">this</span><span class="token punctuation">.</span>inputRef<span class="token punctuation">}</span></span> <span class="token punctuation">/></span></span><span class="token punctuation">;</span>
</span>  <span class="token punctuation">}</span>

  <span class="token function">componentDidMount</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
<span class="gatsby-highlight-code-line">    <span class="token keyword">this</span><span class="token punctuation">.</span>inputRef<span class="token punctuation">.</span>current<span class="token punctuation">.</span><span class="token function">focus</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</span>  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>
        </div></p>
<blockquote>
<p><strong>Note:</strong></p>
<p>Callback refs will continue to be supported in addition to the new <code>createRef</code> API.</p>
<p>You don’t need to replace callback refs in your components. They are slightly more flexible, so they will remain as an advanced feature.</p>
</blockquote>
<p></p>
<h2 id="forwardref-api"><code>forwardRef</code> API</h2>
<p> (or HOCs) are a common way to reuse code between components. Building on the theme context example from above, we might create an HOC that injects the current “theme” as a prop:</p>
<p><div class="gatsby-highlight">
        <pre class="gatsby-code-jsx"><code><span class="token keyword">function</span> <span class="token function">withTheme</span><span class="token punctuation">(</span>Component<span class="token punctuation">)</span> <span class="token punctuation">{</span>
  <span class="token keyword">return</span> <span class="token keyword">function</span> <span class="token function">ThemedComponent</span><span class="token punctuation">(</span>props<span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token keyword">return</span> <span class="token punctuation">(</span>
<span class="gatsby-highlight-code-line">      <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>ThemeContext.Consumer</span><span class="token punctuation">></span></span>
</span><span class="gatsby-highlight-code-line">        <span class="token punctuation">{</span>theme <span class="token operator">=></span> <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>Component</span> <span class="token spread"><span class="token punctuation">{</span><span class="token punctuation">...</span><span class="token attr-value">props</span><span class="token punctuation">}</span></span> <span class="token attr-name">theme</span><span class="token script language-javascript"><span class="token punctuation">=</span><span class="token punctuation">{</span>theme<span class="token punctuation">}</span></span> <span class="token punctuation">/></span></span><span class="token punctuation">}</span>
</span><span class="gatsby-highlight-code-line">      <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>ThemeContext.Consumer</span><span class="token punctuation">></span></span>
</span>    <span class="token punctuation">)</span><span class="token punctuation">;</span>
  <span class="token punctuation">}</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span>
</code></pre>
        </div></p>
<p>We can use the above HOC to wire components up to the theme context without having to use <code>ThemeContext</code> directly. For example:</p>
<p><div class="gatsby-highlight">
        <pre class="gatsby-code-jsx"><code><span class="token keyword">class</span> <span class="token class-name">FancyButton</span> <span class="token keyword">extends</span> <span class="token class-name">React<span class="token punctuation">.</span>Component</span> <span class="token punctuation">{</span>
  buttonRef <span class="token operator">=</span> React<span class="token punctuation">.</span><span class="token function">createRef</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

  <span class="token function">focus</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token keyword">this</span><span class="token punctuation">.</span>buttonRef<span class="token punctuation">.</span>current<span class="token punctuation">.</span><span class="token function">focus</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
  <span class="token punctuation">}</span>

  <span class="token function">render</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
<span class="gatsby-highlight-code-line">    <span class="token keyword">const</span> <span class="token punctuation">{</span>label<span class="token punctuation">,</span> theme<span class="token punctuation">,</span> <span class="token operator">...</span>rest<span class="token punctuation">}</span> <span class="token operator">=</span> <span class="token keyword">this</span><span class="token punctuation">.</span>props<span class="token punctuation">;</span>
</span>    <span class="token keyword">return</span> <span class="token punctuation">(</span>
      <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>button</span>
        <span class="token spread"><span class="token punctuation">{</span><span class="token punctuation">...</span><span class="token attr-value">rest</span><span class="token punctuation">}</span></span>
        <span class="token attr-name">className</span><span class="token script language-javascript"><span class="token punctuation">=</span><span class="token punctuation">{</span><span class="token template-string"><span class="token string">`</span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>theme<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string">-button`</span></span><span class="token punctuation">}</span></span>
<span class="gatsby-highlight-code-line">        <span class="token attr-name">ref</span><span class="token script language-javascript"><span class="token punctuation">=</span><span class="token punctuation">{</span><span class="token keyword">this</span><span class="token punctuation">.</span>buttonRef<span class="token punctuation">}</span></span><span class="token punctuation">></span></span>
</span>        <span class="token punctuation">{</span>label<span class="token punctuation">}</span>
      <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>button</span><span class="token punctuation">></span></span>
    <span class="token punctuation">)</span><span class="token punctuation">;</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>

<span class="gatsby-highlight-code-line"><span class="token keyword">const</span> FancyThemedButton <span class="token operator">=</span> <span class="token function">withTheme</span><span class="token punctuation">(</span>FancyButton<span class="token punctuation">)</span><span class="token punctuation">;</span>
</span>
<span class="token comment">// We can render FancyThemedButton as if it were a FancyButton</span>
<span class="token comment">// It will automatically receive the current "theme",</span>
<span class="token comment">// And the HOC will pass through our other props.</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>FancyThemedButton</span>
  <span class="token attr-name">label</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>Click me!<span class="token punctuation">"</span></span>
  <span class="token attr-name">onClick</span><span class="token script language-javascript"><span class="token punctuation">=</span><span class="token punctuation">{</span>handleClick<span class="token punctuation">}</span></span>
<span class="token punctuation">/></span></span><span class="token punctuation">;</span>
</code></pre>
        </div></p>
<p>HOCs typically . This means that we can’t attach a ref to <code>FancyButton</code> if we use <code>FancyThemedButton</code>— so there’s no way for us to call <code>focus()</code>.</p>
<p>The new <code>forwardRef</code> API solves this problem by providing a way for us to intercept a <code>ref</code> and forward it as a normal prop:
<div class="gatsby-highlight">
        <pre class="gatsby-code-jsx"><code><span class="token keyword">function</span> <span class="token function">withTheme</span><span class="token punctuation">(</span>Component<span class="token punctuation">)</span> <span class="token punctuation">{</span>
  <span class="token comment">// Note the second param "ref" provided by React.forwardRef.</span>
  <span class="token comment">// We can attach this to Component directly.</span>
<span class="gatsby-highlight-code-line">  <span class="token keyword">function</span> <span class="token function">ThemedComponent</span><span class="token punctuation">(</span>props<span class="token punctuation">,</span> ref<span class="token punctuation">)</span> <span class="token punctuation">{</span>
</span>    <span class="token keyword">return</span> <span class="token punctuation">(</span>
      <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>ThemeContext.Consumer</span><span class="token punctuation">></span></span>
        <span class="token punctuation">{</span>theme <span class="token operator">=></span> <span class="token punctuation">(</span>
<span class="gatsby-highlight-code-line">          <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>Component</span> <span class="token spread"><span class="token punctuation">{</span><span class="token punctuation">...</span><span class="token attr-value">props</span><span class="token punctuation">}</span></span> <span class="token attr-name">ref</span><span class="token script language-javascript"><span class="token punctuation">=</span><span class="token punctuation">{</span>ref<span class="token punctuation">}</span></span> <span class="token attr-name">theme</span><span class="token script language-javascript"><span class="token punctuation">=</span><span class="token punctuation">{</span>theme<span class="token punctuation">}</span></span> <span class="token punctuation">/></span></span>
</span>        <span class="token punctuation">)</span><span class="token punctuation">}</span>
      <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>ThemeContext.Consumer</span><span class="token punctuation">></span></span>
    <span class="token punctuation">)</span><span class="token punctuation">;</span>
  <span class="token punctuation">}</span>

  <span class="token comment">// These next lines are not necessary,</span>
  <span class="token comment">// But they do give the component a better display name in DevTools,</span>
  <span class="token comment">// e.g. "ForwardRef(withTheme(MyComponent))"</span>
<span class="gatsby-highlight-code-line">  <span class="token keyword">const</span> name <span class="token operator">=</span> Component<span class="token punctuation">.</span>displayName <span class="token operator">||</span> Component<span class="token punctuation">.</span>name<span class="token punctuation">;</span>
</span><span class="gatsby-highlight-code-line">  ThemedComponent<span class="token punctuation">.</span>displayName <span class="token operator">=</span> <span class="token template-string"><span class="token string">`withTheme(</span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>name<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string">)`</span></span><span class="token punctuation">;</span>
</span>
  <span class="token comment">// Tell React to pass the "ref" to ThemedComponent.</span>
<span class="gatsby-highlight-code-line">  <span class="token keyword">return</span> React<span class="token punctuation">.</span><span class="token function">forwardRef</span><span class="token punctuation">(</span>ThemedComponent<span class="token punctuation">)</span><span class="token punctuation">;</span>
</span><span class="token punctuation">}</span>

<span class="gatsby-highlight-code-line"><span class="token keyword">const</span> fancyButtonRef <span class="token operator">=</span> React<span class="token punctuation">.</span><span class="token function">createRef</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</span>
<span class="token comment">// fancyButtonRef will now point to FancyButton</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>FancyThemedButton</span>
  <span class="token attr-name">label</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>Click me!<span class="token punctuation">"</span></span>
  <span class="token attr-name">onClick</span><span class="token script language-javascript"><span class="token punctuation">=</span><span class="token punctuation">{</span>handleClick<span class="token punctuation">}</span></span>
<span class="gatsby-highlight-code-line">  <span class="token attr-name">ref</span><span class="token script language-javascript"><span class="token punctuation">=</span><span class="token punctuation">{</span>fancyButtonRef<span class="token punctuation">}</span></span>
</span><span class="token punctuation">/></span></span><span class="token punctuation">;</span>
</code></pre>
        </div></p>
<h2 id="component-lifecycle-changes">Component Lifecycle Changes</h2>
<p>React’s class component API has been around for years with little change. However, as we add support for more advanced features (such as ) we stretch this model in ways that it was not originally intended.</p>
<p>For example, with the current API, it is too easy to block the initial render with non-essential logic. In part this is because there are too many ways to accomplish a given task, and it can be unclear which is best. We’ve observed that the interrupting behavior of error handling is often not taken into consideration and can result in memory leaks (something that will also impact the upcoming async rendering mode). The current class component API also complicates other efforts, like our work on .</p>
<p>Many of these issues are exacerbated by a subset of the component lifecycles (<code>componentWillMount</code>, <code>componentWillReceiveProps</code>, and <code>componentWillUpdate</code>). These also happen to be the lifecycles that cause the most confusion within the React community. For these reasons, we are going to deprecate those methods in favor of better alternatives.</p>
<p>We recognize that this change will impact many existing components. Because of this, the migration path will be as gradual as possible, and will provide escape hatches. (At Facebook, we maintain more than 50,000 React components. We depend on a gradual release cycle too!)</p>
<blockquote>
<p><strong>Note:</strong></p>
<p>Deprecation warnings will be enabled with a future 16.x release, <strong>but the legacy lifecycles will continue to work until version 17</strong>.</p>
<p>Even in version 17, it will still be possible to use them, but they will be aliased with an “UNSAFE_” prefix to indicate that they might cause issues. We have also prepared an  in existing code.</p>
</blockquote>
<p>In addition to deprecating unsafe lifecycles, we are also adding a couple of new lifecyles:</p>
<ul>
<li> is being added as a safer alternative to the legacy <code>componentWillReceiveProps</code>.</li>
<li> is being added to support safely reading properties from e.g. the DOM before updates are made.</li>
</ul>
<p></p>
<h2 id="strictmode-component"><code>StrictMode</code> Component</h2>
<p><code>StrictMode</code> is a tool for highlighting potential problems in an application. Like <code>Fragment</code>, <code>StrictMode</code> does not render any visible UI. It activates additional checks and warnings for its descendants.</p>
<blockquote>
<p><strong>Note:</strong></p>
<p><code>StrictMode</code> checks are run in development mode only; <em>they do not impact the production build</em>.</p>
</blockquote>
<p>Although it is not possible for strict mode to catch all problems (e.g. certain types of mutation), it can help with many. If you see warnings in strict mode, those things will likely cause bugs for async rendering.</p>
<p>In version 16.3, <code>StrictMode</code> helps with:</p>
<ul>
<li>Identifying components with unsafe lifecycles</li>
<li>Warning about legacy string ref API usage</li>
<li>Detecting unexpected side effects</li>
</ul>
<p>Additional functionality will be added with future releases of React.</p>
<p></p>
---------------
<h1 id="#title_1" >2、文章： 任何人都可以借助Workers在Cloudflare上运行JavaScript了</h1>
谢丽
[http://www.infoq.com/cn/articles/run-javaScript-on-cloudflare-with-workers?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/run-javaScript-on-cloudflare-with-workers?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/run-javaScript-on-cloudflare-with-workers/zh/smallimage/api-facades-logo-1522221283266.jpg"/><p>任何人都可以借助Workers在Cloudflare上运行JavaScript了。Workers使用标准的Service Workers API编写，运行在一个基于V8构建的新环境中。5个月前，该服务开始了Beta测试，如今，Cloudflare Workers已经准备好向所有人提供服务了。</p> <i>By 谢丽</i>
---------------
<h1 id="#title_2" >3、文章： 用深度学习解决冯-诺依曼结构内存性能瓶颈</h1>
Milad Hashem等
[http://www.infoq.com/cn/articles/learning-memory-access-patterns?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/learning-memory-access-patterns?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/learning-memory-access-patterns/zh/smallimage/redis-logo-1522225599019.jpg"/><p>这篇论文展示了深度学习在解决冯·诺依曼架构计算机内存性能瓶颈问题中的应用。论文关注的是学习内存访问模式这一关键问题，意在构建一种准确高效的内存预期器。研究提出将预期策略视为NLP中的n-gram模型，并使用RNN模型完全替代基于表的传统预取。在基准测试集上的实验表明，基于神经网络的模型在预测内存访问模式上可稳定地给出更优的准确率和召回率。该论文是将神经网络应用于计算机结构设计中的一篇开创性工作。</p> <i>By Milad Hashem等</i> <i> Translated by 盖磊</i>
---------------
<h1 id="#title_3" >4、Understanding Logical Properties And Values</h1>
Rachel Andrew
[https://www.smashingmagazine.com/2018/03/understanding-logical-properties-values/](https://www.smashingmagazine.com/2018/03/understanding-logical-properties-values/)
<![CDATA[
          
        ]]>
---------------
<h1 id="#title_4" >5、视频演讲： 如何构建低成本高效能的视觉感知系统</h1>
潘争
[http://www.infoq.com/cn/presentations/how-to-build-a-low-cost-and-efficient-visual-perception-system?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/how-to-build-a-low-cost-and-efficient-visual-perception-system?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/presentations/how-to-build-a-low-cost-and-efficient-visual-perception-system/zh/mediumimage/panzheng270-1521462726370.jpg"/><p>低成本、高精度、实时性、低功耗是下一阶段自动驾驶环境感知方案的迫切需求，是自动驾驶产品落地的瓶颈。视觉是环境感知的各种方案中接近这一要求的方式。为了能够达到低成本高效能的目标，我们探索了多种方法，包括高效的物体检测、语义分割的深度学习算法、网络压缩和剪枝方法、Inferen阶段的GPU、FPGA加速等。结合多种方法，我们在嵌入式平台上实现了视觉感知的实时预测。</p> <i>By 潘争</i>
---------------
<h1 id="#title_5" >6、视频演讲： 解锁深度视频理解的潜力</h1>
曾文军
[http://www.infoq.com/cn/presentations/the-potential-of-unlocking-the-depth-of-video-understanding?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/the-potential-of-unlocking-the-depth-of-video-understanding?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/presentations/the-potential-of-unlocking-the-depth-of-video-understanding/zh/mediumimage/zengwenjun270-1521471844797.jpg"/><p>人工智能离不开感知，而视觉是我们最主要的感知手段。深度学习近年来颠覆了图像/视频理解的进程。这要归因于大数据，大计算，和深度学习体系结构和方法的巨大进步和创新。这次演讲将讨论在视觉智能发展中深度学习技术的关键理念和主要进展，并基于一些实际用例简单阐明如何在这个令人兴奋的领域中开拓市场，实现技术落地。本次演讲也将讨论一些未来技术趋势。</p> <i>By 曾文军</i>
---------------
<h1 id="#title_6" >7、谈笔1000亿的生意：揭秘菜鸟全球智能仓配技术实践</h1>
麦克周
[http://www.infoq.com/cn/news/2018/03/intelligence-logistics-practice?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/03/intelligence-logistics-practice?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>3月24日，菜鸟网络2018技术论坛深圳站圆满结束，围绕智慧物流背后的成长和关键技术，来自菜鸟网络的四名技术资深专家与两百余位开发者们深度分享了菜鸟网络物流智能化、自动化、全球化的技术实践与架构演进。</p> <i>By 麦克周</i>
---------------
<h1 id="#title_7" >8、文章： 虚拟现实将颠覆敏捷教练和指导方式</h1>
Michael de la Maza, Elena Vassilieva
[http://www.infoq.com/cn/articles/virtual-reality-disrupt-coaching?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/virtual-reality-disrupt-coaching?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/virtual-reality-disrupt-coaching/zh/headerimage/GettyImages-655137196-1521633127451.jpg"/><p>我们认为，在未来3 - 5年内，在线技术（虚拟现实，增强现实，自适应个性化学习和视频会议）将对敏捷教练和培训领域带来极大冲击。到2020年底，至少有一个大型，可靠的敏捷/ Scrum认证机构将在虚拟现实中运营敏捷/ Scrum认证课程。今天的胜利者，或许将成为明天的失败者。</p> <i>By Michael de la Maza</i> <i> Translated by 冬雨</i>
---------------
<h1 id="#title_8" >9、无人驾驶汽车致人死亡</h1>
Roland Meertens
[http://www.infoq.com/cn/news/2018/03/uber-driverless-fatality?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/03/uber-driverless-fatality?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>据BBC报道，一名行人于周日晚间在美国亚利桑那州坦佩被Uber的无人驾驶汽车撞击身亡。Uber确认称，当时车辆处于自动驾驶模式，但车内坐有安全驾驶员，该名驾驶员是车祸发生时车内唯一的乘客。</p> <i>By Roland Meertens</i> <i> Translated by 大愚若智</i>
---------------
<h1 id="#title_9" >10、GitLab揭示DevOps价值和挑战的新调查研究</h1>
Helen Beal
[http://www.infoq.com/cn/news/2018/03/GitLab-2018-developer-survey?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/03/GitLab-2018-developer-survey?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>GitLab发布的2018年全球开发人员报告显示，软件专业人士共同认识到在高度协作的DevOps风格环境中工作的价值，并体会到了这样做的好处。65％的受访者表示，DevOps节省了大量时间，如果只关注于管理人员则更是高达81％。</p> <i>By Helen Beal</i> <i> Translated by 冬雨</i>
---------------
<h1 id="#title_10" >11、GitHub安全告警检测出了400多万个漏洞</h1>
Sergio De Simone
[http://www.infoq.com/cn/news/2018/03/github-vulnerability-alerts-resp?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/03/github-vulnerability-alerts-resp?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>据GitHub介绍，去年十月推出的安全告警极大地减少了开发人员消除Ruby和JavaScript项目漏洞的时间。</p> <i>By Sergio De Simone</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_11" >12、打造敏捷公司</h1>
Ben Linders
[http://www.infoq.com/cn/news/2018/03/becoming-agile-company?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/03/becoming-agile-company?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>要成为一家敏捷公司，组织必须放弃大部分层级和微管理：完全改变管理模型，而不是进行小规模的增量调整，那样会沉溺在传统的官僚体系中。他们要停止做那些妨碍敏捷性的事情，专注于客户导向、内在动机、基于信任的领导和不那么正式的计划。</p> <i>By Ben Linders</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_12" >13、“#smoosh门”引发Web兼容性上的挑战</h1>
Dylan Schiemann
[http://www.infoq.com/cn/news/2018/03/smooshgate-web-compatibility?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/03/smooshgate-web-compatibility?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>TC39提案Array.prototype.flatten会导致旧网站在Firefox Nightly版中无法正常显示。在回应这一软件缺陷报告时，该新特性的建议者开玩笑称会考虑将“flatten”改名为“smoosh”。这在JavaScript社区引发了大范围的口诛笔伐。</p> <i>By Dylan Schiemann</i> <i> Translated by 盖磊</i>
---------------
<h1 id="#title_13" >14、左耳朵耗子：从亚马逊的实践，谈分布式系统的难点</h1>
陈皓
[http://www.infoq.com/cn/news/2018/03/amazon-distributed-practice?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/03/amazon-distributed-practice?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>本文摘自陈皓（左耳朵耗子）在极客时间App/小程序上开始的全年付费专栏《左耳听风》，已获授权。</p> <i>By 陈皓</i>
---------------
<h1 id="#title_14" >15、文章： SaaS的窘境与未来：缺少服务，难成气候？</h1>
周明耀
[http://www.infoq.com/cn/articles/SaaS-SkyNAS-Synology?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/SaaS-SkyNAS-Synology?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/SaaS-SkyNAS-Synology/zh/smallimage/123-1522287767913.jpg"/><p></p> <i>By 周明耀</i>
---------------