## 文章索引
1、 <a href="#1introducing-the-react-profiler" >Introducing the React Profiler</a><br/>
2、 <a href="#2the-importance-of-manual-accessibility-testing" >The Importance Of Manual Accessibility Testing</a><br/>
3、 <a href="#3文章-siemens-healthineers在teamplay使用持续交付" >文章： Siemens Healthineers在teamplay使用持续交付</a><br/>
4、 <a href="#4文章-谷歌宣布其bigquery服务已支持以太坊区块链数据分析" >文章： 谷歌宣布其BigQuery服务已支持以太坊区块链数据分析</a><br/>
5、 <a href="#5文章-apache-beam实战指南-|-玩转kafkaio与flink" >文章： Apache Beam实战指南 | 玩转KafkaIO与Flink</a><br/>
6、 <a href="#6程序员编程利器后起之秀-vs-code" >程序员编程利器：后起之秀 VS Code</a><br/><h1 id="#title_0" >1、Introducing the React Profiler</h1>

[https://reactjs.org/blog/2018/09/10/introducing-the-react-profiler.html](https://reactjs.org/blog/2018/09/10/introducing-the-react-profiler.html)
<p>React 16.5 adds support for a new DevTools profiler plugin.
This plugin uses React’s  to collect timing information about each component that’s rendered in order to identify performance bottlenecks in React applications.
It will be fully compatible with our upcoming  features.</p>
<p>This blog post covers the following topics:</p>
<ul>
<li></li>
<li>
<p></p>
<ul>
<li></li>
<li></li>
<li></li>
<li></li>
<li></li>
<li></li>
</ul>
</li>
<li>
<p></p>
<ul>
<li></li>
<li></li>
</ul>
</li>
</ul>
<h2 id="profiling-an-application">Profiling an application</h2>
<p>DevTools will show a “Profiler” tab for applications that support the new profiling API:</p>
<p>
  <a
    class="gatsby-resp-image-link"
    href="/static/devtools-profiler-tab-4da6b55fc3c98de04c261cd902c14dc3-53c76.png"
    style="display: block"
    target="_blank"
    rel="noopener"
  >
  
  <span
    class="gatsby-resp-image-wrapper"
    style="position: relative; display: block; ; max-width: 840px; margin-left: auto; margin-right: auto;"
  >
    <span
      class="gatsby-resp-image-background-image"
      style="padding-bottom: 47.82608695652174%; position: relative; bottom: 0; left: 0; background-image: url('data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABQAAAAKCAYAAAC0VX7mAAAACXBIWXMAAAsSAAALEgHS3X78AAAB60lEQVQoz62RzW7TQBSFI8Srsekz1BJs2LDkLVjUKGSRxJay6AsgRJtCwwKJqiGNY4fSFhAqUdImkf/GcezxZHw9l5lpQXSBxIIjfTrjY+mTf2qDPXvr7XH34bA/2nbcsTEcjY0TxzMc95Px4ahvvN5/Y3QPDo2Xr/aMo+OB3r2xxPM0rutuSx45jvOgpvLty/l3uiaYXX7FTZYgcIqiLDSVPJcsQ9hkuquSyi1Hmq+RMaYpigJV5vO5q4W94dX5e2+F3YFfHowi6I1jeHeawKFHNL1xcof9YQRnPwgwmgOlFKSLK2GSJB+l7n5ttogvAp/hbBbA9TIRkzkT0yUVYVqKKKtEtIY7hJKsAIHid5QUCSEDLczW6YUa4utFFUwnOJkQvJqGSIIM+YYj54AbXsm+oSxBdonSqF/1D+GJFsZkpYWrZVKlYSyCgIo4osL3C7GKE5FEiTwzEYaFhIo0zgVnXIi/PWGepWdqSBeEp0EEflBAFDIIJSuyBimFwKdACINYkqUMoAQl+QW/Ffa18PNlOFFDSSvcyG+c5yj/ooQiMtmixH9KFEWnWrj12Hz67HnrhW1bO82WZbbbbbPVusFqt0zLkm3ZZlteq3uKZrNp1ut1s9FoKHZs2250Op0nWnibe/+B2u7ubu0n/Rxb5mrVIIgAAAAASUVORK5CYII='); background-size: cover; display: block;"
    >
      <img
        class="gatsby-resp-image-image"
        style="width: 100%; height: 100%; margin: 0; vertical-align: middle; position: absolute; top: 0; left: 0; box-shadow: inset 0px 0px 0px 400px white;"
        alt="New DevTools "profiler" tab"
        title=""
        src="/static/devtools-profiler-tab-4da6b55fc3c98de04c261cd902c14dc3-acf85.png"
        srcset="/static/devtools-profiler-tab-4da6b55fc3c98de04c261cd902c14dc3-c1418.png 210w,
/static/devtools-profiler-tab-4da6b55fc3c98de04c261cd902c14dc3-5d5d8.png 420w,
/static/devtools-profiler-tab-4da6b55fc3c98de04c261cd902c14dc3-acf85.png 840w,
/static/devtools-profiler-tab-4da6b55fc3c98de04c261cd902c14dc3-53c76.png 1012w"
        sizes="(max-width: 840px) 100vw, 840px"
      />
    </span>
  </span>
  
  </a>
    </p>
<blockquote>
<p>Note:</p>
<p><code class="gatsby-code-text">react-dom</code> 16.5+ supports profiling in DEV mode.
A production profiling bundle is also available as <code class="gatsby-code-text">react-dom/profiling</code>.
Read more about how to use this bundle at  </p>
</blockquote>
<p>The “Profiler” panel will be empty initially. Click the record button to start profiling:</p>
<p>
  <a
    class="gatsby-resp-image-link"
    href="/static/start-profiling-bae8d10e17f06eeb8c512c91c0153cff-53c76.png"
    style="display: block"
    target="_blank"
    rel="noopener"
  >
  
  <span
    class="gatsby-resp-image-wrapper"
    style="position: relative; display: block; ; max-width: 840px; margin-left: auto; margin-right: auto;"
  >
    <span
      class="gatsby-resp-image-background-image"
      style="padding-bottom: 47.82608695652174%; position: relative; bottom: 0; left: 0; background-image: url('data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABQAAAAKCAYAAAC0VX7mAAAACXBIWXMAAAsSAAALEgHS3X78AAABdUlEQVQoz62QvU7DMBCAI8SrsfAMjQQzI+9RBthpq0ody9ABMTC0C0lKwo8KDEjt0GZomthJmx8S1+bukkbAiHrSp7OTu89na4+318f347sTe2w3DNPQDaPENE19OBzq/f6NPhgMIPf10WhE3+k/YBkPumPbDcdxTi3LOtIwPiYvnyxkaj53VRAEv/B9Xy2XS7VarZTnIR59Z4xBZsr1AsXDSGFMp1OHhLOn57cszZTP10Ucx+IvSZIQaZqK9XotNpuNkFKK7XYrCkSIHIVwuAG6Q40HwTsdoSQWSlwQ1fpngISoa0oEdnPOTRJGUURCrMdcFAUBI5RZCFX9rzMCYpWXtVQAz2CRMAzDWgjNEvaSeZ5ki4WEUyVcs55qNyWu8zyXcH2Jz1EJzZ1wUgnzLMtEAm+VcC5i1xVfsI+hAZqxqX47zNVVkbwSPpAQJpipPQQM9krCdrt93u12LzudThO4+AdN6L9qtVpnJKziYA9ovV5P+wavR2c66XZI3gAAAABJRU5ErkJggg=='); background-size: cover; display: block;"
    >
      <img
        class="gatsby-resp-image-image"
        style="width: 100%; height: 100%; margin: 0; vertical-align: middle; position: absolute; top: 0; left: 0; box-shadow: inset 0px 0px 0px 400px white;"
        alt="Click "record" to start profiling"
        title=""
        src="/static/start-profiling-bae8d10e17f06eeb8c512c91c0153cff-acf85.png"
        srcset="/static/start-profiling-bae8d10e17f06eeb8c512c91c0153cff-c1418.png 210w,
/static/start-profiling-bae8d10e17f06eeb8c512c91c0153cff-5d5d8.png 420w,
/static/start-profiling-bae8d10e17f06eeb8c512c91c0153cff-acf85.png 840w,
/static/start-profiling-bae8d10e17f06eeb8c512c91c0153cff-53c76.png 1012w"
        sizes="(max-width: 840px) 100vw, 840px"
      />
    </span>
  </span>
  
  </a>
    </p>
<p>Once you’ve started recording, DevTools will automatically collect performance information each time your application renders.
Use your app as you normally would.
When you are finished profiling, click the “Stop” button.</p>
<p>
  <a
    class="gatsby-resp-image-link"
    href="/static/stop-profiling-45619de03bed468869f7a0878f220586-53c76.png"
    style="display: block"
    target="_blank"
    rel="noopener"
  >
  
  <span
    class="gatsby-resp-image-wrapper"
    style="position: relative; display: block; ; max-width: 840px; margin-left: auto; margin-right: auto;"
  >
    <span
      class="gatsby-resp-image-background-image"
      style="padding-bottom: 47.82608695652174%; position: relative; bottom: 0; left: 0; background-image: url('data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABQAAAAKCAYAAAC0VX7mAAAACXBIWXMAAAsSAAALEgHS3X78AAABcklEQVQoz62QS2vCQBCAQ+lf66W/wUB77rH/Qw/tuSQieLSHQMFDD3oxiSQHUfsCC1UP5rGJeTRuNrvd2SRiH/TkwMdkM7PfDiNZD3fnj+P+hTW2Grqhy7peYhiGPBgM5F7vXtY0jeeePBwOxX9R55j6SLYtq2Hb9qVpmmcSxNN08oZCxJbLNfN9/xue57HNZsNc12WOAzjiP0KIZ8TWjs+CcMsgFouFLYQfL6+zLNsxD0V5kiQkTRMCuSZN0z1wzrKM0KIgBScHCMEg5I/rXHcqhQjNxROMEnoQRUH/DC6i0HwAgdtBEBilcLsVQuitMiuo6GF8DPYzoC56eA3nOcvzXDTzNZilMAz3QpgAPlcrl2r9Z/qZJLQs/Z4QY0zjOKawikpo1MJpJcQcKJI03pHZ3CF8DELLVeyB3dV9FbgSjoQwiqJ3doTgg02EUFXV606nc9Nut5ucVo2iqK3D8z80+f1bRVGuhLCKkyMgdbtd6Qtm52eikNUIKgAAAABJRU5ErkJggg=='); background-size: cover; display: block;"
    >
      <img
        class="gatsby-resp-image-image"
        style="width: 100%; height: 100%; margin: 0; vertical-align: middle; position: absolute; top: 0; left: 0; box-shadow: inset 0px 0px 0px 400px white;"
        alt="Click "stop" when you are finished profiling"
        title=""
        src="/static/stop-profiling-45619de03bed468869f7a0878f220586-acf85.png"
        srcset="/static/stop-profiling-45619de03bed468869f7a0878f220586-c1418.png 210w,
/static/stop-profiling-45619de03bed468869f7a0878f220586-5d5d8.png 420w,
/static/stop-profiling-45619de03bed468869f7a0878f220586-acf85.png 840w,
/static/stop-profiling-45619de03bed468869f7a0878f220586-53c76.png 1012w"
        sizes="(max-width: 840px) 100vw, 840px"
      />
    </span>
  </span>
  
  </a>
    </p>
<p>Assuming your application rendered at least once while profiling, DevTools will show several ways to view the performance data.
We’ll .</p>
<h2 id="reading-performace-data">Reading performace data</h2>
<h3 id="browsing-commits">Browsing commits</h3>
<p>Conceptually, React does work in two phases:</p>
<ul>
<li>The <strong>render</strong> phase determines what changes need to be made to e.g. the DOM. During this phase, React calls <code class="gatsby-code-text">render</code> and then compares the result to the previous render.</li>
<li>The <strong>commit</strong> phase is when React applies any changes. (In the case of React DOM, this is when React inserts, updates, and removes DOM nodes.) React also calls lifecycles like <code class="gatsby-code-text">componentDidMount</code> and <code class="gatsby-code-text">componentDidUpdate</code> during this phase.</li>
</ul>
<p>The DevTools profiler groups performance info by commit.
Commits are displayed in a bar chart near the top of the profiler:</p>
<p>
  <a
    class="gatsby-resp-image-link"
    href="/static/commit-selector-bd72dec045515d59be51c944e902d263-8ef72.png"
    style="display: block"
    target="_blank"
    rel="noopener"
  >
  
  <span
    class="gatsby-resp-image-wrapper"
    style="position: relative; display: block; ; max-width: 601px; margin-left: auto; margin-right: auto;"
  >
    <span
      class="gatsby-resp-image-background-image"
      style="padding-bottom: 9.983361064891847%; position: relative; bottom: 0; left: 0; background-image: url('data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABQAAAACCAIAAADXZGvcAAAACXBIWXMAAAsSAAALEgHS3X78AAAAbUlEQVQI103KuwqEMBBAUf//X7axtLERbLaKuMWC2RDcmcyMeSNYaiWe7sJtAED/DJJ8vuaPUkpJKeWHKxNzRNxly+gq0eH9zpTJNQ5httEC+xBZthD8NZdbrau1pBRPk+ilb1/z2BltQPXxPZwvF2xA6VCC0AAAAABJRU5ErkJggg=='); background-size: cover; display: block;"
    >
      <img
        class="gatsby-resp-image-image"
        style="width: 100%; height: 100%; margin: 0; vertical-align: middle; position: absolute; top: 0; left: 0; box-shadow: inset 0px 0px 0px 400px white;"
        alt="Bar chart of profiled commits"
        title=""
        src="/static/commit-selector-bd72dec045515d59be51c944e902d263-8ef72.png"
        srcset="/static/commit-selector-bd72dec045515d59be51c944e902d263-69e48.png 210w,
/static/commit-selector-bd72dec045515d59be51c944e902d263-3b0aa.png 420w,
/static/commit-selector-bd72dec045515d59be51c944e902d263-8ef72.png 601w"
        sizes="(max-width: 601px) 100vw, 601px"
      />
    </span>
  </span>
  
  </a>
    </p>
<p>Each bar in the chart represents a single commit with the currently selected commit colored black.
You can click on a bar (or the left/right arrow buttons) to select a different commit.</p>
<p>The color and height of each bar corresponds to how long that commit took to render.
(Taller, yellow bars took longer than shorter, blue bars.)</p>
<h3 id="filtering-commits">Filtering commits</h3>
<p>The longer you profile, the more times your application will render.
In some cases you may end up with <em>too many commits</em> to easily process.
The profiler offers a filtering mechanism to help with this.
Use it to specify a threshold and the profiler will hide all commits that were <em>faster</em> than that value.</p>
<p><img src="/filtering-commits-683b9d860ef722e1505e5e629df7ef7e.gif" alt="Filtering commits by time"></p>
<h3 id="flame-chart">Flame chart</h3>
<p>The flame chart view represents the state of your application for a particular commit.
Each bar in the chart represents a React component (e.g. <code class="gatsby-code-text">App</code>, <code class="gatsby-code-text">Nav</code>).
The size and color of the bar represents how long it took to render the component and its children.
(The width of a bar represents how much time was spent <em>when the component last rendered</em> and the color represents how much time was spent <em>as part of the current commit</em>.)</p>
<p>
  <a
    class="gatsby-resp-image-link"
    href="/static/flame-chart-3046f500b9bfc052bde8b7b3b3cfc243-53c76.png"
    style="display: block"
    target="_blank"
    rel="noopener"
  >
  
  <span
    class="gatsby-resp-image-wrapper"
    style="position: relative; display: block; ; max-width: 840px; margin-left: auto; margin-right: auto;"
  >
    <span
      class="gatsby-resp-image-background-image"
      style="padding-bottom: 47.82608695652174%; position: relative; bottom: 0; left: 0; background-image: url('data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABQAAAAKCAYAAAC0VX7mAAAACXBIWXMAAAsSAAALEgHS3X78AAAB30lEQVQoz62Rz08TURDHG+O/xsW/gZeIN6M3L548kTSQiFHUgx5oS9PIqQkhgaIpEovYbep2d1vaQgndSpV2f++2XWRnZ3y7LejZ8E2+eW/mzXzevN1EZevdvaKwfV/6Xpuv1UQWWRRFJksSE4Qy2y0U2F6xyHZ3CqwiVJmi1Jksy6yuKHGNJEnzPF7gPXOJSMftZsccTejXQCdvNCLf92NPJhNyXIdc1yXDMkk3dZ5zyfMcnvfIdhzyxmMeexRJVVUxBrbaJ0dD3SVdMwJDN8EyLG4TTO7hQAOeB7V3Bu2zDvwY9MHqdeGnUIGLahV8bQgBwFUE1DStzHF3E5/yyaaw+ZSOS0k4+rKIjVISGwfPsbG3iKeHy9j6uoQdeR3HZh/9y4CvJqp1Bd3zcwwsCzkLIqBt20IMXN1aaz7cWKZn2+/DtdIH2hA/0mE1T0tvH9Cb9ceU//yKbN+ha0EY0u8guIkRMQZallWJgQenJ82dwQWVhkbYG1+iz2vkfhdf7m/ifquMmqNHU2CIfzXl3OgaOJ1w5HqN2WX8W/BDXgBIANOnwHSoEKLGyP/uZ76aAb/FQP6XunQLchxHiYHpdPpJNptdzWQyK9wv/sMrvP91KpV6FANnunMLTuRyucQfU2RSA7PakTgAAAAASUVORK5CYII='); background-size: cover; display: block;"
    >
      <img
        class="gatsby-resp-image-image"
        style="width: 100%; height: 100%; margin: 0; vertical-align: middle; position: absolute; top: 0; left: 0; box-shadow: inset 0px 0px 0px 400px white;"
        alt="Example flame chart"
        title=""
        src="/static/flame-chart-3046f500b9bfc052bde8b7b3b3cfc243-acf85.png"
        srcset="/static/flame-chart-3046f500b9bfc052bde8b7b3b3cfc243-c1418.png 210w,
/static/flame-chart-3046f500b9bfc052bde8b7b3b3cfc243-5d5d8.png 420w,
/static/flame-chart-3046f500b9bfc052bde8b7b3b3cfc243-acf85.png 840w,
/static/flame-chart-3046f500b9bfc052bde8b7b3b3cfc243-53c76.png 1012w"
        sizes="(max-width: 840px) 100vw, 840px"
      />
    </span>
  </span>
  
  </a>
    </p>
<blockquote>
<p>Note:</p>
<p>The width of a bar indicates how long it took to render the component (and its children) when they last rendered.
If the component did not re-render as part of this commit, the time represents a previous render.
The wider a component is, the longer it took to render.</p>
<p>The color of a bar indicates how long the component (and its children) took to render in the selected commit.
Yellow components took more time, blue components took less time, and gray components did not render at all during this commit.</p>
</blockquote>
<p>For example, the commit shown above took a total of 18.4ms to render.
The <code class="gatsby-code-text">Router</code> component was the “most expensive” to render (taking 18.4ms).
Most of this time was due to two of its children, <code class="gatsby-code-text">Nav</code> (8.4ms) and <code class="gatsby-code-text">Route</code> (7.9ms).
The rest of the time was divided between its remaining children or spent in the component’s own render method.</p>
<p>You can zoom in or out on a flame chart by clicking on components:
<img src="/zoom-in-and-out-39ba82394205242af7c37ccb3a631f4d.gif" alt="Click on a component to zoom in or out"></p>
<p>Clicking on a component will also select it and show information in the right side panel which includes its <code class="gatsby-code-text">props</code> and <code class="gatsby-code-text">state</code> at the time of this commit.
You can drill into these to learn more about what the component actually rendered during the commit:</p>
<p><img src="/props-and-state-1f4d023f1a0f281386625f28df87c78f.gif" alt="Viewing a component&#x27;s props and state for a commit"></p>
<p>In some cases, selecting a component and stepping between commits may also provide a hint as to <em>why</em> the component rendered:</p>
<p><img src="/see-which-props-changed-cc2a8b37bbce52c49a11c2f8e55dccbc.gif" alt="Seeing which values changed between commits"></p>
<p>The above image shows that <code class="gatsby-code-text">state.scrollOffset</code> changed between commits.
This is likely what caused the <code class="gatsby-code-text">List</code> component to re-render.</p>
<h3 id="ranked-chart">Ranked chart</h3>
<p>The ranked chart view represents a single commit.
Each bar in the chart represents a React component (e.g. <code class="gatsby-code-text">App</code>, <code class="gatsby-code-text">Nav</code>).
The chart is ordered so that the components which took the longest to render are at the top.</p>
<p>
  <a
    class="gatsby-resp-image-link"
    href="/static/ranked-chart-0c81347535e28c9cdef0e94fab887b89-53c76.png"
    style="display: block"
    target="_blank"
    rel="noopener"
  >
  
  <span
    class="gatsby-resp-image-wrapper"
    style="position: relative; display: block; ; max-width: 840px; margin-left: auto; margin-right: auto;"
  >
    <span
      class="gatsby-resp-image-background-image"
      style="padding-bottom: 47.82608695652174%; position: relative; bottom: 0; left: 0; background-image: url('data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABQAAAAKCAYAAAC0VX7mAAAACXBIWXMAAAsSAAALEgHS3X78AAABlUlEQVQoz62OT2/TMBiHI7SvxoXPMEtwhhvckPYBECqHIY6s6r/BdpjaXmARNzSta6WQpGuF1o5kW7e1YYmj1HHiuH6xvYpNOwBC+0mPbL2v9fxsdFrvHpn7zceHVnfV/tZFtnWNa/dQr/MVmbufkWl+QeanNuod7CHXsZHjuqjf7yPHcZBt26vyfGJZ1kND5Xg0HpEcwLskkKQcSAa/wXMOEY4hTa4giCgkdAFzQiGOMUQRhiRJNCq+71taOOhtD04HHwCPWwU7aXF22ubFEuo1eXb8kQuvxmf9TU7HW3wefOeTixmfTac8yzJeFAVTwiAIOlK3Yrwovx4+a7yClJxzYKEQWSAg/3kDuxIiDwUUob6nSSg8zxdRFAkpE9LFlRBjfKCFL3fqw72Jr2YLtf0TKly+IoQApRQYYyCE0EJZ0NXCtWZ9eEawFsqIf8ntnlvC6x/aP44Oc7FQM6aWf0OW3p2xpXBfC/OUenAPiePY1cL3GxvPq9XqeqVSKUne/AelWq32tlwuP9XCZR7cA0aj0TB+AdiMX66/MIlxAAAAAElFTkSuQmCC'); background-size: cover; display: block;"
    >
      <img
        class="gatsby-resp-image-image"
        style="width: 100%; height: 100%; margin: 0; vertical-align: middle; position: absolute; top: 0; left: 0; box-shadow: inset 0px 0px 0px 400px white;"
        alt="Example ranked chart"
        title=""
        src="/static/ranked-chart-0c81347535e28c9cdef0e94fab887b89-acf85.png"
        srcset="/static/ranked-chart-0c81347535e28c9cdef0e94fab887b89-c1418.png 210w,
/static/ranked-chart-0c81347535e28c9cdef0e94fab887b89-5d5d8.png 420w,
/static/ranked-chart-0c81347535e28c9cdef0e94fab887b89-acf85.png 840w,
/static/ranked-chart-0c81347535e28c9cdef0e94fab887b89-53c76.png 1012w"
        sizes="(max-width: 840px) 100vw, 840px"
      />
    </span>
  </span>
  
  </a>
    </p>
<blockquote>
<p>Note:</p>
<p>A component’s render time includes the time spent rendering its children,
so the components which took the longest to render are generally near the top of the tree.</p>
</blockquote>
<p>As with the flame chart, you can zoom in or out on a ranked chart by clicking on components.</p>
<h3 id="component-chart">Component chart</h3>
<p>Sometimes it’s useful to see how many times a particular component rendered while you were profiling.
The component chart provides this information in the form of a bar chart.
Each bar in the chart represents a time when the component rendered.
The color and height of each bar corresponds to how long the component took to render <em>relative to other components</em> in a particular commit.</p>
<p>
  <a
    class="gatsby-resp-image-link"
    href="/static/component-chart-d71275b42c6109e222fbb0932a0c8c09-53c76.png"
    style="display: block"
    target="_blank"
    rel="noopener"
  >
  
  <span
    class="gatsby-resp-image-wrapper"
    style="position: relative; display: block; ; max-width: 840px; margin-left: auto; margin-right: auto;"
  >
    <span
      class="gatsby-resp-image-background-image"
      style="padding-bottom: 47.82608695652174%; position: relative; bottom: 0; left: 0; background-image: url('data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABQAAAAKCAYAAAC0VX7mAAAACXBIWXMAAAsSAAALEgHS3X78AAACSElEQVQoz62P20tUURTGh+gf6a33CHwTukCIQQ9JNw8kEZHRU2+9BzaCJ1LLB43xOPiaMjIgBl1Gzcuc0RnL0RQdTUWdOefsc3Wcs85ardlq9Af0wcf69tqL3147tjCeaPqiTzzM5xZbs9mscuJ5RWdPTU4qqVRKSafTyujIqJLJZBRd15WzuRzP5PP51kKh0JbL5a7H6lpZXloXrk27e/tkWhaZpkkWV0vYMpfLZVkNwyTTsEgIIV2f3auYZDsO1bW5WVqQwFJpa9lzHTosV0LX88D3ffC52lYFhLCAYbC/UwTXWOW8DfwY9wV4POP6Ac97NeGF9KO4Psu48zHnmIq00Ue1lV5AIqw7NJcwmH4sM0CEYRgihEfsABmEDMVqlc9RiCyob1gxjDkJrGwXipR/QrTWHdGZTJ0w00xQtfmAFNW8v1cRvxIeHpBrGVS2KuR6rgTaQsxLoFgdKdJCG1Vnn0bHYh0lwVlBmGjAo68tyE0Mph5hsPweg60xDJ0SVrd30d7ZQd8PMAKQQN76ZEN7bewnLbYTpC/Wqp+uwdGvBMBBBnDiMkSfGiCYeQ74uRFg/BKEqQsAvz9CzToGr7wPYSRhtVPgjAS6G+Ml2npJ9P0q0XwT0TTXmZtE2WaiuRucr5z09VucG4mcb0Q+f4S//K9s216SwMG+jhfJN+3dgx0tXVq8VR3qfKAOxe+o2ut77Luq1qmoWpxz/L6qddxWtb5Xav/bd2p/b4/6YWBAHdS0rmQy2ZNIJJ5J4KnO/QfHhoeHY38AsLpA6BTZFEwAAAAASUVORK5CYII='); background-size: cover; display: block;"
    >
      <img
        class="gatsby-resp-image-image"
        style="width: 100%; height: 100%; margin: 0; vertical-align: middle; position: absolute; top: 0; left: 0; box-shadow: inset 0px 0px 0px 400px white;"
        alt="Example component chart"
        title=""
        src="/static/component-chart-d71275b42c6109e222fbb0932a0c8c09-acf85.png"
        srcset="/static/component-chart-d71275b42c6109e222fbb0932a0c8c09-c1418.png 210w,
/static/component-chart-d71275b42c6109e222fbb0932a0c8c09-5d5d8.png 420w,
/static/component-chart-d71275b42c6109e222fbb0932a0c8c09-acf85.png 840w,
/static/component-chart-d71275b42c6109e222fbb0932a0c8c09-53c76.png 1012w"
        sizes="(max-width: 840px) 100vw, 840px"
      />
    </span>
  </span>
  
  </a>
    </p>
<p>The chart above shows that the <code class="gatsby-code-text">List</code> component rendered 11 times.
It also shows that each time it rendered, it was the most “expensive” component in the commit (meaning that it took the longest).</p>
<p>To view this chart, either double-click on a component <em>or</em> select a component and click on the blue bar chart icon in the right detail pane.
You can return to the previous chart by clicking the “x” button in the right detail pane.
You can aso double click on a particular bar to view more information about that commit.</p>
<p><img src="/see-all-commits-for-a-fiber-99cb4321ded8eb0c21ae5fc673878563.gif" alt="How to view all renders for a specific component"></p>
<p>If the selected component did not render at all during the profiling session, the following message will be shown:</p>
<p>
  <a
    class="gatsby-resp-image-link"
    href="/static/no-render-times-for-selected-component-8eb0c37a13353ef5d9e61ae8fc040705-53c76.png"
    style="display: block"
    target="_blank"
    rel="noopener"
  >
  
  <span
    class="gatsby-resp-image-wrapper"
    style="position: relative; display: block; ; max-width: 840px; margin-left: auto; margin-right: auto;"
  >
    <span
      class="gatsby-resp-image-background-image"
      style="padding-bottom: 47.82608695652174%; position: relative; bottom: 0; left: 0; background-image: url('data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABQAAAAKCAYAAAC0VX7mAAAACXBIWXMAAAsSAAALEgHS3X78AAABZ0lEQVQoz62PzU7CQBDHG+OrefEZaKJnj74HHvQBCiHckQMx8eABE5VSUlDwQEI9oId+7PaD2rTLjrND26BHwz/5dbc7M/+Z0SZ3xumDdX9mT+yGaZp6xXg81ofDod7v9/XBYKD3erf4/0jvVY5ljnTbthvT6fTcsqwTTel9PlvyiMN6/QUBYxAEDBjbEQQBuK4Lvu+D53kE55xQuZ8egzCKQGm1ciZk6Dgf8zT9BtcPizhOxGazqUFTEUWRyPO8Bs2IJElETHlJzpMCXhfLZ7Q71jC4oBYghfrsU6m6qxMbSZxYZllWRreqTm3xQoZhGJLhFlUUBSiEEDXV286P8gAnpRjsOtEFBxv9MsSkLa4hFbiqZJxJjMk4jultX382IEOsqSd8KzvleAicQKRpSuBaKplQhQoVr+4leWn4RIY4gQMHEA42I8NWq3XZ6XSu2+12E7n6B02svzEM44IMSx0dAK3b7Wo/FtRnZY5UiRMAAAAASUVORK5CYII='); background-size: cover; display: block;"
    >
      <img
        class="gatsby-resp-image-image"
        style="width: 100%; height: 100%; margin: 0; vertical-align: middle; position: absolute; top: 0; left: 0; box-shadow: inset 0px 0px 0px 400px white;"
        alt="No render times for the selected component"
        title=""
        src="/static/no-render-times-for-selected-component-8eb0c37a13353ef5d9e61ae8fc040705-acf85.png"
        srcset="/static/no-render-times-for-selected-component-8eb0c37a13353ef5d9e61ae8fc040705-c1418.png 210w,
/static/no-render-times-for-selected-component-8eb0c37a13353ef5d9e61ae8fc040705-5d5d8.png 420w,
/static/no-render-times-for-selected-component-8eb0c37a13353ef5d9e61ae8fc040705-acf85.png 840w,
/static/no-render-times-for-selected-component-8eb0c37a13353ef5d9e61ae8fc040705-53c76.png 1012w"
        sizes="(max-width: 840px) 100vw, 840px"
      />
    </span>
  </span>
  
  </a>
    </p>
<h3 id="interactions">Interactions</h3>
<p>React recently added another  for tracking the <em>cause</em> of an update.
“Interactions” tracked with this API will also be shown in the profiler:</p>
<p>
  <a
    class="gatsby-resp-image-link"
    href="/static/interactions-a91a39ac076b71aa7a202aaf46f8bd5a-53c76.png"
    style="display: block"
    target="_blank"
    rel="noopener"
  >
  
  <span
    class="gatsby-resp-image-wrapper"
    style="position: relative; display: block; ; max-width: 840px; margin-left: auto; margin-right: auto;"
  >
    <span
      class="gatsby-resp-image-background-image"
      style="padding-bottom: 47.82608695652174%; position: relative; bottom: 0; left: 0; background-image: url('data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABQAAAAKCAYAAAC0VX7mAAAACXBIWXMAAAsSAAALEgHS3X78AAABl0lEQVQoz62RzW7aQBDHraqvlkufIZaSc499j/TQPgAgxD1wQJFy6IFKSQyOgBAUKVFJJKAW9trOrm28O97J7ILpoT1VGemn9Xz9Z0Z2bi8an36MLk/G/vh4OBy6NaPRyB0MBm6v13P7/b7bPe+S/9PGPc+zNf7Qcyfj8fFkMjn1ff/IMfYwv3tMeIrL1RrjOEZG1C9jDDebDYZheCBJEkzT1ObXYYzJ6ysaWywWt1bw19PTPY8TXP2OVMA45FkGWY0QIASHoiggJwT5JAo0BMIogpAxE5Naa1wul9ck99F5mU7nIgiwoMIKkXKVNkZDNchSy0zossh1JaWNZ9tCr4JAx4zpPM9MCMyGdNWNFXyezeZpFCEPgkpVgGVZopTygFIKt0LYb07nizRGUW6RtseSYmS1oGcF4/V6jqaxKCoFoEEpDeYljK+sX+182pLut9vX/LVhyvkMd1m5n/Zvdo1AdSSvQf9B7gWvrCDnfIHvYPTnp1aw2Wx+abfb31qt1hnx9T84o/7vjUbjsxXc24d3wOl0Os4blShlbz/d1/8AAAAASUVORK5CYII='); background-size: cover; display: block;"
    >
      <img
        class="gatsby-resp-image-image"
        style="width: 100%; height: 100%; margin: 0; vertical-align: middle; position: absolute; top: 0; left: 0; box-shadow: inset 0px 0px 0px 400px white;"
        alt="The interactions panel"
        title=""
        src="/static/interactions-a91a39ac076b71aa7a202aaf46f8bd5a-acf85.png"
        srcset="/static/interactions-a91a39ac076b71aa7a202aaf46f8bd5a-c1418.png 210w,
/static/interactions-a91a39ac076b71aa7a202aaf46f8bd5a-5d5d8.png 420w,
/static/interactions-a91a39ac076b71aa7a202aaf46f8bd5a-acf85.png 840w,
/static/interactions-a91a39ac076b71aa7a202aaf46f8bd5a-53c76.png 1012w"
        sizes="(max-width: 840px) 100vw, 840px"
      />
    </span>
  </span>
  
  </a>
    </p>
<p>The image above shows a profiling session that tracked four interactions.
Each row represents an interaction that was tracked.
The colored dots along the row represent commits that were related to that interaction.</p>
<p>You can also see which interactions were tracked for a particular commit from the flame chart and ranked chart views as well:</p>
<p>
  <a
    class="gatsby-resp-image-link"
    href="/static/interactions-for-commit-9847e78f930cb7cf2b0f9682853a5dbc-53c76.png"
    style="display: block"
    target="_blank"
    rel="noopener"
  >
  
  <span
    class="gatsby-resp-image-wrapper"
    style="position: relative; display: block; ; max-width: 840px; margin-left: auto; margin-right: auto;"
  >
    <span
      class="gatsby-resp-image-background-image"
      style="padding-bottom: 47.82608695652174%; position: relative; bottom: 0; left: 0; background-image: url('data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABQAAAAKCAYAAAC0VX7mAAAACXBIWXMAAAsSAAALEgHS3X78AAABuUlEQVQoz62Ry27aQBSGraqv1k2fISO16y77Humi3XUDCPECva3SICULLkkxYGKCsAmCFMYm2OBbYo7P6ZmBpllX+aVftmfO+fzPGaP97fPr0/aPN91f5pFpmkK50+mIbrcrms2GODn5Kc7PzsTXL99Fq9UW/X5f27Is0ev1VN0RP99yzytDaTS0x3dRSkt5R3GcUJZlj47jmDzPo9lsxt8xpWmq1zabDQVBQFEUaStNp9OOBlr29dV8uSYp5U56Hvi+r71arYBhwIUwHF6DlDNe8yAIQ/i9WIDHNdnDA+x2u1wBuafJuJdGvV637asBua4L4/EYlR3HRWswRNdx0HUnOJ/Pcb0OEAAwiSO8GY1wLSXmSYLMAgUMw7ClgXx2m+dBk8mk4DS8saEsjeiycUoXF5fkOA7luQ6hVdzfU3J7S9liQbnvExaFBvII2hrI87GTJFGzKbIs5X1CKlJMfROXS4k8N5UCH8Xv9MSsv8B9wu12Ozj8XMUAVcBdgPujwL+1vQtOhE+NmB+ADQ3kW7qhZxDffF8Dy+Xy+2q1+rFSqRyzP/yHj7n/U6lUeqeBB714Bhu1Ws34A880Xu+Ar3OjAAAAAElFTkSuQmCC'); background-size: cover; display: block;"
    >
      <img
        class="gatsby-resp-image-image"
        style="width: 100%; height: 100%; margin: 0; vertical-align: middle; position: absolute; top: 0; left: 0; box-shadow: inset 0px 0px 0px 400px white;"
        alt="List of interactions for a commit"
        title=""
        src="/static/interactions-for-commit-9847e78f930cb7cf2b0f9682853a5dbc-acf85.png"
        srcset="/static/interactions-for-commit-9847e78f930cb7cf2b0f9682853a5dbc-c1418.png 210w,
/static/interactions-for-commit-9847e78f930cb7cf2b0f9682853a5dbc-5d5d8.png 420w,
/static/interactions-for-commit-9847e78f930cb7cf2b0f9682853a5dbc-acf85.png 840w,
/static/interactions-for-commit-9847e78f930cb7cf2b0f9682853a5dbc-53c76.png 1012w"
        sizes="(max-width: 840px) 100vw, 840px"
      />
    </span>
  </span>
  
  </a>
    </p>
<p>You can navigate between interactions and commits by clicking on them:</p>
<p><img src="/navigate-between-interactions-and-commits-7c66e7686b5242473c87b3d0b4576cf3.gif" alt="Navigate between interactions and commits"></p>
<p>The tracking API is still new and we will cover it in more detail in a future blog post.</p>
<h2 id="troubleshooting">Troubleshooting</h2>
<h3 id="no-profiling-data-has-been-recorded-for-the-selected-root">No profiling data has been recorded for the selected root</h3>
<p>If your your application has multiple “roots”, you may see the following message after profiling:

  <a
    class="gatsby-resp-image-link"
    href="/static/no-profiler-data-multi-root-0755492a211f5bbb775285c0ff2fdfda-53c76.png"
    style="display: block"
    target="_blank"
    rel="noopener"
  >
  
  <span
    class="gatsby-resp-image-wrapper"
    style="position: relative; display: block; ; max-width: 840px; margin-left: auto; margin-right: auto;"
  >
    <span
      class="gatsby-resp-image-background-image"
      style="padding-bottom: 47.82608695652174%; position: relative; bottom: 0; left: 0; background-image: url('data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABQAAAAKCAYAAAC0VX7mAAAACXBIWXMAAAsSAAALEgHS3X78AAABjUlEQVQoz62Qy07CQBRAG+OvufEbmETXLv0PWOgH8GhY2wVCAjEuxbZUNEpMTCCB0kDoY0pfdKYz3hkeC40LE25yeqfzOHPnKtaDev74+ngxtIYlwzCQQNd11Ol0ULvdRpqmoftWC/V6PaTdaajb7SLTNOW+gaGjoWWVXoz+pTkwzxQRnwP9Cy8cbttz7vk+9zyP+5BXq5VkuVwexovFgruuywOxD3BcnwdBwHme8PFkbEnhZDT6yPyAu35Ioiimcbwl2ZMkh7xer2kURZQxRouioIQKaM4h4KI+6E6VIAxHfBsUYH8BHwYSyY81cU5U+iyFIcZSWGRZQaB8gvEvKMAJkbdCdRIQwxQRSCG0SZdCGEhhinERzGbMt20WAHg+Z6HjMG86ZWKeJAmD5x0qBBGD1rA0TffCbYXw9ndxU5KmebrZ0Ah6leW5RPzHcCDJMgrrsrciRA93TxXkO+GTFEKTJ/wIgTF+k8JarXbdaDRuIJfr9XoFckXkf1BWVfW2Wq1eSeEuTo6A0mw2lW+bPmTlyk2LHgAAAABJRU5ErkJggg=='); background-size: cover; display: block;"
    >
      <img
        class="gatsby-resp-image-image"
        style="width: 100%; height: 100%; margin: 0; vertical-align: middle; position: absolute; top: 0; left: 0; box-shadow: inset 0px 0px 0px 400px white;"
        alt="No profiling data has been recorded for the selected root"
        title=""
        src="/static/no-profiler-data-multi-root-0755492a211f5bbb775285c0ff2fdfda-acf85.png"
        srcset="/static/no-profiler-data-multi-root-0755492a211f5bbb775285c0ff2fdfda-c1418.png 210w,
/static/no-profiler-data-multi-root-0755492a211f5bbb775285c0ff2fdfda-5d5d8.png 420w,
/static/no-profiler-data-multi-root-0755492a211f5bbb775285c0ff2fdfda-acf85.png 840w,
/static/no-profiler-data-multi-root-0755492a211f5bbb775285c0ff2fdfda-53c76.png 1012w"
        sizes="(max-width: 840px) 100vw, 840px"
      />
    </span>
  </span>
  
  </a>
    </p>
<p>This message indicates that no performance data was recorded for the root that’s selected in the “Elements” panel.
In this case, try selecting a different root in that panel to view profiling information for that root:</p>
<p><img src="/select-a-root-to-view-profiling-data-bdc30593d414b5c8d2ae92027ed11940.gif" alt="Select a root in the &#x22;Elements&#x22; panel to view its performance data"></p>
<h3 id="no-timing-data-to-display-for-the-selected-commit">No timing data to display for the selected commit</h3>
<p>Sometimes a commit may be so fast that <code class="gatsby-code-text">performance.now()</code> doesn’t give DevTools any meaningful timing information.
In this case, the following message will be shown:</p>
<p>
  <a
    class="gatsby-resp-image-link"
    href="/static/no-timing-data-for-commit-63b2fb6298feecb179272c467020ed95-53c76.png"
    style="display: block"
    target="_blank"
    rel="noopener"
  >
  
  <span
    class="gatsby-resp-image-wrapper"
    style="position: relative; display: block; ; max-width: 840px; margin-left: auto; margin-right: auto;"
  >
    <span
      class="gatsby-resp-image-background-image"
      style="padding-bottom: 47.82608695652174%; position: relative; bottom: 0; left: 0; background-image: url('data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABQAAAAKCAYAAAC0VX7mAAAACXBIWXMAAAsSAAALEgHS3X78AAABe0lEQVQoz61QTUvDQBAN4l/z4m9oQM8e/R/1oFehLaU/QSwWexK0CYQkrQURNGAxkKRJNh/tJpNdZzdJqSdB+uAxs7Ozb96Oot/dnj7q47OFaXZMy1RNs6Zt26quzdSHyVSdTJ/U8f1Y1TRd1i3LUufzuYzY28F4bhjGiSLwtrTfw4Twjy+PJ4TwLMt2jCLCw+Cbp4HD1+EaaylPkoTHcYx3kcwFBRzHMaSg7/uvDAtxRsuCUiiKAsqyhBLjZrMFmsdAExfCyAcoKaRpCqvVClzXxfuN6C2EoOd5Lyh3rBBClrwGINlfzPOcoRuGLllVVax5JxzPfgniFytsrr+bZ1zkguiIp/it7XZbTwXglFLegjEmBcMw1KRgEARLLHIUrkhCGJ4ZrmFHbGS4J0kc1rpie2gFa4doddFMLpCA0+Vu0J2MYqcoAi1ELkT2WDSCz1IQJ3/yAwB3akvBfr9/ORwOrweDQRd59Q928f1Nr9e7kIINjg5AZTQaKT+0smf7vT5VvwAAAABJRU5ErkJggg=='); background-size: cover; display: block;"
    >
      <img
        class="gatsby-resp-image-image"
        style="width: 100%; height: 100%; margin: 0; vertical-align: middle; position: absolute; top: 0; left: 0; box-shadow: inset 0px 0px 0px 400px white;"
        alt="No timing data to display for the selected commit"
        title=""
        src="/static/no-timing-data-for-commit-63b2fb6298feecb179272c467020ed95-acf85.png"
        srcset="/static/no-timing-data-for-commit-63b2fb6298feecb179272c467020ed95-c1418.png 210w,
/static/no-timing-data-for-commit-63b2fb6298feecb179272c467020ed95-5d5d8.png 420w,
/static/no-timing-data-for-commit-63b2fb6298feecb179272c467020ed95-acf85.png 840w,
/static/no-timing-data-for-commit-63b2fb6298feecb179272c467020ed95-53c76.png 1012w"
        sizes="(max-width: 840px) 100vw, 840px"
      />
    </span>
  </span>
  
  </a>
    </p>
---------------
<h1 id="#title_1" >2、The Importance Of Manual Accessibility Testing</h1>
Eric Bailey
[https://www.smashingmagazine.com/2018/09/importance-manual-accessibility-testing/](https://www.smashingmagazine.com/2018/09/importance-manual-accessibility-testing/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/09/importance-manual-accessibility-testing/" />
              <title>The Importance Of Manual Accessibility Testing</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>The Importance Of Manual Accessibility Testing</h1>
                  
                    
                    <address>Eric Bailey</address>
                  
                  <time datetime="2018-09-12T13:30:55&#43;02:00" class="op-published">2018-09-12T13:30:55+02:00</time>
                  <time datetime="2018-09-12T15:02:12&#43;00:00" class="op-modified">2018-09-12T15:02:12+00:00</time>
                </header>
                

<p>Earlier this year, a man  after following directions from a smartphone app that helps drivers navigate by issuing turn-by-turn directions. Unfortunately, the app’s programming did not include instructions to avoid roads that turn into boat launches.</p>

<p>From the perspective of the app, it did exactly what it was programmed to do, i.e. to find the most optimal route from point A to point B given the information made available to it. From the perspective of the man, it failed him by not taking the real world into account.</p>

<p>The same principle applies for accessibility testing.</p>

<div class="c-felix-the-cat">
<h4>Designing For Accessibility And Inclusion</h4>
<p>The more inclusive you are to the needs of your users, the more accessible your design is. Let’s take a closer look at the different lenses of accessibility through which you can refine your designs. </p>
</div>

<h3 id="automated-accessibility-testing">Automated Accessibility Testing</h3>

<p>I am going to assume that you’re reading this article because you’re interested in learning how to test your websites and web apps to ensure they’re accessible. If you want to learn more about why accessibility is necessary,  elsewhere.</p>

<p>Automated accessibility testing is a process where you use a series of scripts to test for the presence, or lack of certain conditions in code. These conditions are dictated by the , a standard by the W3C that outlines how to make digital experiences accessible.</p>



  <aside class="product-panel product-panel__tilted product-panel--book" data-audience="non-subscriber">
    <div class="container product-panel--book__container">
      <div class="panel__description panel__description--book">
    <p>Getting the process <em>just</em> right ain't an easy task. That's why we've set up <strong>'this-is-how-I-work'-sessions</strong> — with smart cookies sharing what works really well for them. A part of the , of course.</p>
      <a href="https://smashed.by/casestudypanelmembership" class="btn btn--green btn--large">
        Explore features&nbsp;→
      </a>
      </div>
      <div class="panel__image panel__image--book">
        <a href="https://smashed.by/casestudypanelmembership" class="books__book__image">
        <div class="books__book__img">
          <img src="https://www.smashingmagazine.com/images/smashing-cat/cat-scubadiving-panel.svg" alt="Smashing TV, with live sessions for professional designers and developers." width="310" height="400">
        </div>
      </a>
      </div>
    </div>
  </aside>




<p>For example, an automated accessibility test might check to see if the <code>tabindex</code> attribute is present and if . The pseudocode would be something like:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8dc9a519-567b-49a5-823c-1d452f200e77/tabindex-flowchart.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8dc9a519-567b-49a5-823c-1d452f200e77/tabindex-flowchart.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8dc9a519-567b-49a5-823c-1d452f200e77/tabindex-flowchart.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8dc9a519-567b-49a5-823c-1d452f200e77/tabindex-flowchart.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8dc9a519-567b-49a5-823c-1d452f200e77/tabindex-flowchart.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8dc9a519-567b-49a5-823c-1d452f200e77/tabindex-flowchart.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8dc9a519-567b-49a5-823c-1d452f200e77/tabindex-flowchart.png"
			sizes="100vw"
			alt="A flowchart that asks if the tabindex value is present. If yes, it asks if the tabindex value is greater than 0. If it is greater than zero, it fails. If not, it passes. If no tabindex value is present, it also passes."
		/>
	</a>

	
</figure>


<p>Failures can then be collected and used to generate reports that disclose the number, and severity of accessibility issues. Certain automated accessibility products can also integrate as a  (CI/CD) tool, presenting just-in-time warnings to developers when they attempt to add code to a central repository.</p>

<p>These automated programs are incredible resources. Modern websites and web apps are complicated things that involve hundreds of states, thousands of lines of code, and complicated multi-screen interactions. It’d be absurd to expect a human (or a team of humans) to mind all the code controlling every possible permutation of the site, to say nothing of things like .</p>

<p>Automation really shines here. It can repeatedly and tirelessly pour over these details with perfect memory, at a rate far faster than any human is capable of.</p>

<h3 id="however">However&hellip;</h3>

<p>Automated accessibility tests aren’t a turnkey solution, nor are they a silver bullet. There are some limitations to keep in mind when using them.</p>

<h4 id="thinking-to-think-of-things">Thinking To Think Of Things</h4>

<p>One of both the best and worst aspects of the web is that there are many different ways to implement a solution to a problem. While this flexibility has kept the web robust and adaptable and ensured it outlived other competing technologies, it also means that you’ll sometimes see code that is, um, creatively implemented.</p>

<p>The test suite is only as good as what its author thought to check for. A naïve developer might only write tests for , and sketchy 3rd party scripts exist.</p>

<p>For example,  than what someone would hear if they were navigating using a screen reader.</p>

<p>If you’re not using a testing service that includes this rule, it won’t be reported. The code will still “pass”, but it’s passing by omission, not because it’s actually accessible.</p>

<h4 id="state">State</h4>

<p>Some automated accessibility tests cannot parse the various states of interactive content. Critical parts of the user interface are effectively invisible to automation unless the test is run when the content is in an active, selected, or disabled state.</p>

<p>By interactive content, I mean things that the user has yet to take action on, or aren’t present when the page loads. Unopened modals, collapsed accordions, hidden tab content and carousel slides are all examples.</p>

<p>It takes sophisticated software to automatically test the various states of every component within a single screen, let alone across an entire web app or website. While it is possible to augment testing software with automated accessibility checks, it is very resource-intensive, usually requiring a dedicated team of engineers to set up and maintain.</p>

<h4 id="valid-markup">“Valid” Markup</h4>

<p>.</p>

<p>Just having the presence of ARIA does not guarantee that it will automatically make something accessible. Unfortunately, and in spite of . A lot of off-the-shelf code has this problem, perpetuating the issue.</p>

<p>For example, certain ARIA attributes and values  and should <strong>never</strong> be placed in markup.</p>

<pre><code class="language-html">&lt;button role="command"&gt;Save&lt;/button&gt;

&lt;!-- Never do this --&gt;
</code></pre>

<p>To further complicate the issue, . While an attribute may be used appropriately, the browser may not communicate the declared role, property, or state to assistive technology.</p>

<p>There is also the scenario where ARIA can be applied to an element and be valid from a technical standpoint, yet be unusable from an assistive technology perspective. For example:</p>

<p><pre><code class="language-html">&lt;h1 aria-hidden=&ldquo;true&rdquo;&gt;
  Tired of unevenly cooked asparagus? Try this tip from the world&rsquo;s oldest cookbook.
&lt;/h1&gt;
</code></pre>
<p><em>This one .</em></p></p>

<p>The  <code>aria-hidden</code> declaration will , yet allow it to be still rendered visibly on the page. It’s a problematic pattern.</p>

<p>Headings &mdash; especially first-level headings &mdash; are vital in . If a person is using assistive technology to navigate, the <code>aria-hidden</code> declaration applied to the <code>h1</code> element will make it difficult for them to quickly determine the page’s purpose. It will force them to navigate around the rest of the page to gain context, an annoying and labor-intensive process.</p>

<p>Some automated accessibility tests may scan the code and not report an error since the syntax itself is valid. The automation has no way of knowing the greater context of the declaration’s use.</p>

<p>This isn’t to say you should completely avoid using ARIA! When , ARIA can fix the gaps in accessibility that sometimes plague complicated interactions; it provides some much-needed context to the people who rely on assistive technology.</p>

<div class="sponsors__wide-place"></div>




<h3 id="much-needed-context">Much-Needed Context</h3>

<p>As the soggy car demonstrates, computers are awful at understanding the overall situation of the outside world. It’s up to us humans to be the ultimate arbiters in determining if what the computer spits out is useful or not.</p>

<h4 id="debunking">Debunking</h4>

<p>Before we discuss how to provide appropriate context, there are a few common misunderstandings about accessibility work that need to be addressed:</p>

<p>First, not all screen reader users are blind. In addition to all the points Adrian Roselli . When’s the last time you spoke to Siri or Alexa?</p>

<p>Second, accessibility is more than just screen readers. The rules outlined in the  ensure that the largest number of people can read and operate technology, regardless of ability or circumstance.</p>

<p>For example, the rule that stipulates  will also be helpful to have here).</p>

<p>Third, disabilities  and can be brought about by your environment. It can be a short-term thing, like rain on your glasses, sleep deprivation, or an allergies-induced migraine. It can also be longer-term, such as a debilitating illness, broken limb, or a depressive episode. Multiple, compounding conditions can (and do) affect individuals.</p>

<p>That all being said, many accessibility fixes that help screen readers work properly also benefit other assistive technologies.</p>

<h4 id="get-your-feet-wet">Get Your Feet Wet</h4>

<p>Knowing where to begin can be overwhelming. Consider ’s great advice:</p>

<blockquote>“Before you release a website, tab through it. If you cannot see where you are on the page after each tab; you&#39;re not finished yet. </blockquote>

<p>, and if they can be activated via keyboard input. If there’s something you can click or tap on that isn’t getting highlighted when receiving keyboard focus, take note of it. Also pay attention to the order interactive components are highlighted when focused &mdash; it should match the reading order of the site.</p>

<p>An obvious focus state and logical tab order go a great way to helping make your site accessible. These two features benefit , screen readers.</p>

<p>If you need a baseline to compare your testing to, Dave Rupert has an excellent project called . This project provides examples of components such as switches, checkboxes, and radio buttons that have well-tested and documented support for assistive technology. A clever reader might use one of these resources to help them try out the other!</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/43da18aa-bbd8-46f3-a83d-cc0ffbd37914/nutrition-cards-and-styled-form-controls.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/43da18aa-bbd8-46f3-a83d-cc0ffbd37914/nutrition-cards-and-styled-form-controls.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/43da18aa-bbd8-46f3-a83d-cc0ffbd37914/nutrition-cards-and-styled-form-controls.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/43da18aa-bbd8-46f3-a83d-cc0ffbd37914/nutrition-cards-and-styled-form-controls.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/43da18aa-bbd8-46f3-a83d-cc0ffbd37914/nutrition-cards-and-styled-form-controls.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/43da18aa-bbd8-46f3-a83d-cc0ffbd37914/nutrition-cards-and-styled-form-controls.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/43da18aa-bbd8-46f3-a83d-cc0ffbd37914/nutrition-cards-and-styled-form-controls.png"
			sizes="100vw"
			alt="A screenshot of homepage for the a11y Styled Form Controls website placed over a screenshot of the Nutrition Cards for Accessible Components website."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<h4 id="the-fourth-myth">The Fourth Myth</h4>

<p>With that out of the way, I’m going to share a fourth myth with you: not every assistive technology user is a power user. Like with any other piece of software, there’s a learning curve involved.</p>

<p>In her post about , Lisa Zhu discovers that their initial accessibility fix wasn’t intuitive. While their first implementation was “technically” correct, it didn’t line up with how people who rely on VoiceOver actually use their devices. A second solution simplified the interaction to better align with their expectations.</p>

<p>Don’t assume that just because something hypothetically functions that it’s actually usable. Trust your gut: if it feels especially awkward, cumbersome, or tedious to operate for you, chances are it’ll be for others.</p>

<h4 id="dive-right-in">Dive Right In</h4>

<p>While not every accessibility issue is a screen reader issue, you should still get in the habit of testing your site with one. Not an emulator, simulator, or some other proxy solution.</p>

<p>If you find yourself struggling to operate a complicated interactive component using , it’s probably a sign that the component needs to be simplified. Chances are that the simplification will help non-assistive technology users as well. Good design benefits everyone!</p>

<p>The same goes for navigation. If it’s difficult to move around the website or web app, it’s probably a sign that you need to update your . Both of these features are used by assistive technology to quickly and efficiently navigate.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e86e65a5-74d6-4f89-98a5-11cb21ec3f12/sidebar-markup.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e86e65a5-74d6-4f89-98a5-11cb21ec3f12/sidebar-markup.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e86e65a5-74d6-4f89-98a5-11cb21ec3f12/sidebar-markup.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e86e65a5-74d6-4f89-98a5-11cb21ec3f12/sidebar-markup.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e86e65a5-74d6-4f89-98a5-11cb21ec3f12/sidebar-markup.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e86e65a5-74d6-4f89-98a5-11cb21ec3f12/sidebar-markup.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e86e65a5-74d6-4f89-98a5-11cb21ec3f12/sidebar-markup.png"
			sizes="100vw"
			alt="Two code examples for a sidebar. One uses a div element, while the others uses an aside element. Both have the class of sidebar applied to them, with a subheading of Recent Posts."
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Both of these are sidebars, but only one of them is semantically described as such. A computer doesn't know what a sidebar is, so it's up to you to tell it.
		</figcaption>
	
</figure>


<p>Another good thing to review is the text content used to describe your links. Hopping from link to link is another common assistive technology navigation technique; some screen readers can even generate a list of all link content on the page:</p>

<blockquote>“Think before you link! Your &quot;helpful&quot; click here links look like this to a screen reader user. ALT = JAWS links list”<br /><figure></blockquote>

<p>When navigating using an ordered list devoid of the surrounding non-link content, avoiding ambiguous terms like “click here” or “more info” can go a long way to ensuring a person can understand the overall meaning of the page. As a bonus, it’ll help alleviate cognitive concerns for everyone, as you are more accurately explaining .</p>

<div class="sponsors__wide-place"></div>




<h3 id="how-to-test">How To Test</h3>

<p>Each screen reader has a different approach to how it announces content. This is intentional. It’s a balancing act between the product’s features, the operating system it is installed on, the form factor it is available in, and the types of input it can receive.</p>

<p> information.</p>

<p><strong>All of these screen readers can be used for free</strong>, provided you have the hardware. You can also virtualize that hardware, either .</p>

<h4 id="automate">Automate</h4>

<p>Automated accessibility tests should be your first line of defense. They will help you catch a great deal of nitpicky, easily-preventable errors before they get committed. Repeated errors may also signal problems in template logic, where one upstream tweak can fix multiple pages. Identifying and resolving these issues allows you to spend your valuable manual testing time much more wisely.</p>

<p>It may also be helpful to log accessibility issues in a place where people can collaborate, such as Google Sheets. Quantifying the frequency and severity of errors can lead to good things like updated documentation, opportunities for lunch and learn education, and other healthy changes to organizational workflow.</p>

<p>Much like manual testing with a variety of screen readers, it is recommended that you  to prevent gaps.</p>

<h4 id="windows">Windows</h4>

<p>The two most popular screen readers on Windows are JAWS and NVDA.</p>

<h5 id="jaws">JAWS</h5>

<p> screen reader on the market. It works best with Firefox and Chrome, with concessions for supporting Internet Explorer. Although it is pay software, it can be operated in full in demo mode for 40 minutes at a time (this should be more than sufficient to perform basic testing).</p>

<h5 id="nvda">NVDA</h5>

<p> is strongly encouraged. It is a feature-rich alternative to JAWS. It works best with Firefox.</p>

<h5 id="narrator">Narrator</h5>

<p>Windows comes bundled with a built-in screen reader called . It works well with Edge, but has difficulty interfacing with other browsers.</p>

<h4 id="apple">Apple</h4>

<h5 id="macos">macOS</h5>

<p> is enabled.</p>

<h5 id="ios">iOS</h5>

<p>VoiceOver is also .</p>

<h4 id="android">Android</h4>

<p>Google recently folded  demographics, should give pause for consideration.</p>

<table class="tablesaw break-out" data-tablesaw-mode="swipe" data-tablesaw-minimap>
  <caption>Popular screen readers</caption>
  <thead>
    <tr>
      <th scope="col">Screen Reader</th>
      <th scope="col">Platform</th>
      <th scope="col">Preferred Browser(s)</th>
      <th scope="col">Manual</th>
      <th scope="col">Launch</th>
      <th scope="col">Quit</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td scope="row"></td>
      <td>Windows</td>
      <td>Chrome, Firefox</td>
      <td></td>
      <td>Launch JAWS as you would any other Windows application</td>
      <td><kbd>Insert</kbd> + <kbd>F4</kbd></td>
    </tr>
    <tr>
      <td scope="row"></td>
      <td>Windows</td>
      <td>Firefox</td>
      <td></td>
      <td><kbd>Ctrl</kbd> + <kbd>Alt</kbd> + <kbd>N</kbd></td>
      <td><kbd>Insert</kbd> + <kbd>Q</kbd></td>
    </tr>
    <tr>
      <td scope="row"></td>
      <td>Windows</td>
      <td>Edge</td>
      <td></td>
      <td><kbd>Windows key</kbd> + <kbd>Control</kbd> + <kbd>Enter</kbd></td>
      <td><kbd>Windows key</kbd> + <kbd>Control</kbd> + <kbd>Enter</kbd></td>
    </tr>
    <tr>
      <td scope="row"></td>
      <td>macOS</td>
      <td>Safari</td>
      <td></td>
      <td><kbd>Command</kbd> + <kbd>F5</kbd> or tap  3 times</td>
      <td><kbd>Command</kbd> + <kbd>F5</kbd> or tap  3 times</td>
    </tr>
    <tr>
      <td scope="row"></td>
      <td>iOS</td>
      <td>Mobile Safari</td>
      <td></td>
      <td>Tell Siri to, “Turn on VoiceOver.” or </td>
      <td>Tell Siri to, “Turn off VoiceOver.” or </td>
    </tr>
    <tr>
      <td scope="row"></td>
      <td>Android</td>
      <td>Mobile Chrome</td>
      <td></td>
      <td>Press both volume keys for 3 seconds</td>
      <td>Press both volume keys for 3 seconds</td>
    </tr>
  </tbody>
</table>

<h4 id="call-the-professionals">Call The Professionals</h4>

<p>If you do not require the use of assistive technology on a frequent basis then  how the people who do interact with the web.</p>

<p>Much like traditional user testing, being too close to the thing you created may cloud your judgment.  are a good way to become aware of the problem space, but you should not use yourself as a litmus test for whether the entire experience is truly accessible. <strong>You are not the expert</strong>.</p>

<p>If your product serves a huge population of users, if its core base of users trends towards having a higher probability of disability conditions (specialized product, elderly populations, foreign language speakers, etc.), and/or if it is , I would strongly encourage allocating a portion of your budget for testing by people with disabilities.</p>

<blockquote>“At what point does your organisation stop supporting a browser in terms of % usage? 18% of the global pop. have an </blockquote>

<p>This isn’t to say you should completely delegate the responsibility to these testers. Much as how automated accessibility testing can detect smaller issues to remove, a first round of basic manual testing helps professional testers focus their efforts on the complicated interactions you need an expert’s opinion on. In addition to optimizing the value of their time, it helps to get you more comfortable triaging. It is also a professional courtesy, plain and simple.</p>

<p>There are a few companies that perform manual testing by people with disabilities:</p>

<ul>
<li></li>
<li></li>
<li> (by Knowbility)</li>
</ul>

<h3 id="designed-experiences">Designed Experiences</h3>

<p>We also need to acknowledge the other large barrier to accessible sites that can’t be automated away: poor user experience.</p>

<p>User experience can make or break a product. Your code can compile perfectly, your time to first paint can be lightning quick, and your Webpack setup can be beyond reproach. All this is irrelevant if . User experience encompasses all users, including those who navigate with the aid of assistive technology.</p>

<p>If a person cannot operate your website or web app, they’ll abandon it and not think twice. If they are forced to use your site to get a service unavailable by other means, there’s  (and rightly so).</p>

<p>As a discipline, user experience can be roughly divided into two parts: how something <strong>looks</strong> and how it <strong>behaves</strong> They’re intrinsically interlinked concepts &mdash; work on either may affect both. While accessible design is a topic unto itself, there are some big-picture things we can keep in mind when approaching accessible user experiences from a testing perspective:</p>

<h4 id="how-it-looks">How It Looks</h4>

<p>The WCAG does a great job covering a lot of , the way you handle your breakpoints, etc.</p>

<blockquote>“A good font should tell you:<br />the difference between m and rn<br />the difference between I and l<br />the difference between O and 0.”<br /><br />&mdash; </blockquote>

<p>It’s one of those “” situations. Smart, accessible defaults can save countless time and money down the line. Lean and mean startups all the way up to multinational conglomerates value efficient use of resources, and this is one of those places where you can really capitalize on that. Put your basic design patterns &mdash; say collected in something like a mood board or living style guide &mdash; in front of people early and often to see if your designed intent is clear.</p>

<h4 id="how-it-behaves">How It Behaves</h4>

<p>An enticing color palette and collection of thoughtfully-curated stock photography only go so far. Eventually, you’re going to have to synthesize all your design decisions to create something that addresses a need.</p>

<p>Behavior can be as small as a , or as large as finding a product and purchasing it. What’s important here is to make sure that all the barriers to a person trying to accomplish the task at hand are removed.</p>

<p>If you’re using personas, don’t create a separate persona for a user with a disability. Instead,  are all worth integrating.</p>

<blockquote>“When looking at your site&#39;s analytics, remember that if you don&#39;t see many users on lower end phones or from more remote areas, it&#39;s not because they aren&#39;t a target for your product or service. It is because your mobile experience sucks.<br />As a developer, it&#39;s your job to fix it.”<br /><br />&mdash; </blockquote>

<p>User testing, ideally simulating conditions as close to what a person would be doing in the real world (including their individual device preferences and presence of assistive technology), is also key. Verifying that people are actually able to make the logical leaps necessary to operate your interface addresses a lot of , a difficult-to-quantify yet vital thing to accommodate.</p>

<h3 id="we-shape-our-tools-our-tools-shape-us">We Shape Our Tools, Our Tools Shape Us</h3>

<p>Our tool use corresponds to the kind of work we do: Carpenters drive nails with hammers, chefs cook using skillets, surgeons cut with scalpels. It’s a self-reinforcing phenomenon, and it tends to lead to over-categorization.</p>

<p>Sometimes this over-categorization gets in the way of us remembering to consider the real world. A surgeon might have a carpentry hobby; a chef might be a retired veterinarian. It’s important to understand that , accessibility is a holistic practice, essential to some but useful to all.</p>

<p>Used with discretion, ARIA is a very good tool to have at our disposal. We shouldn’t shy away from using it, provided we understand the <strong>how</strong> and <strong>why</strong> behind why they work.</p>

<p>The same goes for automated accessibility tests, as well as GPS apps. They’re great tools to have, just get to know the terrain a little bit first.</p>

<h3 id="resources">Resources</h3>

<h4 id="automated-accessibility-tools">Automated Accessibility Tools</h4>

<ul>
<li>)</li>
<li> (Chrome)</li>
<li> (Browser)</li>
<li> (Chrome and Firefox)</li>
</ul>

<h4 id="professional-services">Professional Services</h4>

<ul>
<li></li>
<li></li>
<li></li>
<li></li>
<li></li>
<li></li>
</ul>

<h4 id="references">References</h4>

<ul>
<li></li>
<li></li>
<li></li>
<li>“,” Digital.gov</li>
<li>“,” Web Accessibility Initiative (WAI)</li>
<li>“,” Web Accessibility Initiative (WAI)</li>
<li>“,” W3C Working Draft</li>
</ul>

<h4 id="quick-tests">Quick Tests</h4>

<ul>
<li>“,” Open Inclusion</li>
<li>“,” Karl Groves</li>
<li>“,” The Paciello Group</li>
<li>“,” Web Accessibility Initiative (WAI)</li>
<li>“,” MDN Web Docs</li>
</ul>

<h4 id="further-reading">Further Reading</h4>

<ul>
<li>“,” Jesse Hausler, Medium</li>
<li>“,” Shawn Lawton Henry, uiAccess</li>
<li>“,” Claudio Luís Vera, Medium</li>
<li>“,” Steven Lambert, Smashing Magazine</li>
<li>“,” Karl Groves</li>
<li>“,” MDN Web Docs</li>
<li>“,” Susan Jean Robertson</li>
<li>“,” Sparkbox</li>
<li>“,” Chris Ashton, Smashing Magazine</li>
<li>“,” Axess Lab</li>
<li>“,” Service Manual, GOV.UK</li>
<li>“,” Tom Graham &amp; André Gonçalves, Smashing Magazine</li>
<li>“,” Heydon Pickering, Smashing Magazine</li>
<li>“,” Heydon Pickering, Smashing Magazine</li>
<li>“,” Taylor Hunt, CodePen</li>
<li>“,” Mehmet Duran, GOV.UK</li>
</ul>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(rb, ra, yk, il)</span>
</div>


              </article>
            </body>
          </html>
---------------
<h1 id="#title_2" >3、文章： Siemens Healthineers在teamplay使用持续交付</h1>
Dave Farley, Vladyslav Ukis
[http://www.infoq.com/cn/articles/continuous-delivery-teamplay?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/continuous-delivery-teamplay?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/continuous-delivery-teamplay/zh/smallimage/Adopting-Continuous-Delivery-Siemens-Healthineers-logo-small-1535643109541-1536345255666.jpg"/><p>持续交付是一种保证系统在整个开发过程中都处于可发布状态的工作方式。本文介绍了Siemens Healthineers的一个大型软件开发组织如何开始向持续交付转型，描述了他们在规范化的医疗领域逐步、安全地改变开发过程所采用的策略与技巧。</p> <i>By Dave Farley</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_3" >4、文章： 谷歌宣布其BigQuery服务已支持以太坊区块链数据分析</h1>
Allen Day, Evgeny Medvedev
[http://www.infoq.com/cn/articles/ethereum-bigquery-public-dataset-smart-contract-analytics?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/ethereum-bigquery-public-dataset-smart-contract-analytics?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/ethereum-bigquery-public-dataset-smart-contract-analytics/zh/smallimage/GettyImages-544982936+copy-1536428137134.jpg"/><p>Google日前发布了以太坊区块链的分析工具，本文详细介绍了这一工具的方方面面。</p> <i>By Allen Day</i> <i> Translated by 刘志勇</i>
---------------
<h1 id="#title_4" >5、文章： Apache Beam实战指南 | 玩转KafkaIO与Flink</h1>
张海涛
[http://www.infoq.com/cn/articles/apache-beam-kafkaio-and-flink?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/apache-beam-kafkaio-and-flink?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/apache-beam-kafkaio-and-flink/zh/smallimage/logo+%286%29-1536428650658.jpg"/><p>本文是Apache Beam实战指南系列文章的第二篇内容，将重点介绍 Apache Beam与Flink的关系，对Beam框架中的KafkaIO和Flink源码进行剖析，并结合应用示例和代码解读带你进一步了解如何结合Beam玩转Kafka和Flink。</p> <i>By 张海涛</i>
---------------
<h1 id="#title_5" >6、程序员编程利器：后起之秀 VS Code</h1>
吕鹏
[http://www.infoq.com/cn/news/2018/09/How-increase-efficiency-3?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/09/How-increase-efficiency-3?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>提高你3倍的编程效率。</p> <i>By 吕鹏</i>
---------------