## 文章索引
1、 <a href="#1restful-api-最佳实践" >RESTful API 最佳实践</a><br/>
2、 <a href="#2how-to-build-a-news-application-with-angular-6-and-material-design" >How To Build A News Application With Angular 6 And Material Design</a><br/>
3、 <a href="#3文章-为什么在eos上的dapp对开发人员来说不盈利" >文章： 为什么在EOS上的dApp对开发人员来说不盈利？</a><br/>
4、 <a href="#4amazon发布aws存储网关硬件设备" >Amazon发布AWS存储网关硬件设备</a><br/><h1 id="#title_0" >1、RESTful API 最佳实践</h1>
阮一峰
[http://www.ruanyifeng.com/blog/2018/10/restful-api-best-practices.html](http://www.ruanyifeng.com/blog/2018/10/restful-api-best-practices.html)
<p> 是目前最流行的 API 设计规范，用于 Web 数据接口的设计。</p>

        <p>它的大原则容易把握，但是细节不容易做对。本文总结 RESTful 的设计细节，介绍如何设计出易于理解和使用的 API。</p>

<p><img src="https://www.wangbase.com/blogimg/asset/201810/bg2018100301.jpg" alt="" title="" /></p>

<h2>一、URL 设计</h2>

<h3>1.1 动词 + 宾语</h3>

<p>RESTful 的核心思想就是，客户端发出的数据操作指令都是"动词 + 宾语"的结构。比如，<code>GET /articles</code>这个命令，<code>GET</code>是动词，<code>/articles</code>是宾语。</p>

<p>动词通常就是五种 HTTP 方法，对应 CRUD 操作。</p>

<blockquote>
  <ul>
<li>GET：读取（Read）</li>
<li>POST：新建（Create）</li>
<li>PUT：更新（Update）</li>
<li>PATCH：更新（Update），通常是部分更新</li>
<li>DELETE：删除（Delete）</li>
</ul>
</blockquote>

<p>根据 HTTP 规范，动词一律大写。</p>

<h3>1.2 动词的覆盖</h3>

<p>有些客户端只能使用<code>GET</code>和<code>POST</code>这两种方法。服务器必须接受<code>POST</code>模拟其他三个方法（<code>PUT</code>、<code>PATCH</code>、<code>DELETE</code>）。</p>

<p>这时，客户端发出的 HTTP 请求，要加上<code>X-HTTP-Method-Override</code>属性，告诉服务器应该使用哪一个动词，覆盖<code>POST</code>方法。</p>

<blockquote><pre><code class="language-http">
POST /api/Person/4 HTTP/1.1  
X-HTTP-Method-Override: PUT
</code></pre></blockquote>

<p>上面代码中，<code>X-HTTP-Method-Override</code>指定本次请求的方法是<code>PUT</code>，而不是<code>POST</code>。</p>

<h3>1.3 宾语必须是名词</h3>

<p>宾语就是 API 的 URL，是 HTTP 动词作用的对象。它应该是名词，不能是动词。比如，<code>/articles</code>这个 URL 就是正确的，而下面的 URL 不是名词，所以都是错误的。</p>

<blockquote>
  <ul>
<li>/getAllCars</li>
<li>/createNewCar</li>
<li>/deleteAllRedCars</li>
</ul>
</blockquote>

<h3>1.4 复数 URL</h3>

<p>既然 URL 是名词，那么应该使用复数，还是单数？</p>

<p>这没有统一的规定，但是常见的操作是读取一个集合，比如<code>GET /articles</code>（读取所有文章），这里明显应该是复数。</p>

<p>为了统一起见，建议都使用复数 URL，比如<code>GET /articles/2</code>要好于<code>GET /article/2</code>。</p>

<h3>1.5 避免多级 URL</h3>

<p>常见的情况是，资源需要多级分类，因此很容易写出多级的 URL，比如获取某个作者的某一类文章。</p>

<blockquote><pre><code class="language-http">
GET /authors/12/categories/2
</code></pre></blockquote>

<p>这种 URL 不利于扩展，语义也不明确，往往要想一会，才能明白含义。</p>

<p>更好的做法是，除了第一级，其他级别都用查询字符串表达。</p>

<blockquote><pre><code class="language-http">
GET /authors/12?categories=2
</code></pre></blockquote>

<p>下面是另一个例子，查询已发布的文章。你可能会设计成下面的 URL。</p>

<blockquote><pre><code class="language-http">
GET /articles/published
</code></pre></blockquote>

<p>查询字符串的写法明显更好。</p>

<blockquote><pre><code class="language-http">
GET /articles?published=true
</code></pre></blockquote>

<h2>二、状态码</h2>

<h3>2.1 状态码必须精确</h3>

<p>客户端的每一次请求，服务器都必须给出回应。回应包括 HTTP 状态码和数据两部分。</p>

<p>HTTP 状态码就是一个三位数，分成五个类别。</p>

<blockquote>
  <ul>
<li><code>1xx</code>：相关信息</li>
<li><code>2xx</code>：操作成功</li>
<li><code>3xx</code>：重定向</li>
<li><code>4xx</code>：客户端错误</li>
<li><code>5xx</code>：服务器错误</li>
</ul>
</blockquote>

<p>这五大类总共包含状态码，覆盖了绝大部分可能遇到的情况。每一种状态码都有标准的（或者约定的）解释，客户端只需查看状态码，就可以判断出发生了什么情况，所以服务器应该返回尽可能精确的状态码。</p>

<p>API 不需要<code>1xx</code>状态码，下面介绍其他四类状态码的精确含义。</p>

<h3>2.2 2xx 状态码</h3>

<p><code>200</code>状态码表示操作成功，但是不同的方法可以返回更精确的状态码。</p>

<blockquote>
  <ul>
<li>GET: 200 OK</li>
<li>POST: 201 Created</li>
<li>PUT: 200 OK</li>
<li>PATCH: 200 OK</li>
<li>DELETE: 204 No Content</li>
</ul>
</blockquote>

<p>上面代码中，<code>POST</code>返回<code>201</code>状态码，表示生成了新的资源；<code>DELETE</code>返回<code>204</code>状态码，表示资源已经不存在。</p>

<p>此外，<code>202 Accepted</code>状态码表示服务器已经收到请求，但还未进行处理，会在未来再处理，通常用于异步操作。下面是一个例子。</p>

<blockquote><pre><code class="language-http">
HTTP/1.1 202 Accepted

{
  "task": {
    "href": "/api/company/job-management/jobs/2130040",
    "id": "2130040"
  }
}
</code></pre></blockquote>

<h3>2.3 3xx 状态码</h3>

<p>API 用不到<code>301</code>状态码（永久重定向）和<code>302</code>状态码（暂时重定向，<code>307</code>也是这个含义），因为它们可以由应用级别返回，浏览器会直接跳转，API 级别可以不考虑这两种情况。</p>

<p>API 用到的<code>3xx</code>状态码，主要是<code>303 See Other</code>，表示参考另一个 URL。它与<code>302</code>和<code>307</code>的含义一样，也是"暂时重定向"，区别在于<code>302</code>和<code>307</code>用于<code>GET</code>请求，而<code>303</code>用于<code>POST</code>、<code>PUT</code>和<code>DELETE</code>请求。收到<code>303</code>以后，浏览器不会自动跳转，而会让用户自己决定下一步怎么办。下面是一个例子。</p>

<blockquote><pre><code class="language-http">
HTTP/1.1 303 See Other
Location: /api/orders/12345
</code></pre></blockquote>

<h3>2.4 4xx 状态码</h3>

<p><code>4xx</code>状态码表示客户端错误，主要有下面几种。</p>

<p><code>400 Bad Request</code>：服务器不理解客户端的请求，未做任何处理。</p>

<p><code>401 Unauthorized</code>：用户未提供身份验证凭据，或者没有通过身份验证。</p>

<p><code>403 Forbidden</code>：用户通过了身份验证，但是不具有访问资源所需的权限。</p>

<p><code>404 Not Found</code>：所请求的资源不存在，或不可用。</p>

<p><code>405 Method Not Allowed</code>：用户已经通过身份验证，但是所用的 HTTP 方法不在他的权限之内。</p>

<p><code>410 Gone</code>：所请求的资源已从这个地址转移，不再可用。</p>

<p><code>415 Unsupported Media Type</code>：客户端要求的返回格式不支持。比如，API 只能返回 JSON 格式，但是客户端要求返回 XML 格式。</p>

<p><code>422 Unprocessable Entity</code> ：客户端上传的附件无法处理，导致请求失败。</p>

<p><code>429 Too Many Requests</code>：客户端的请求次数超过限额。</p>

<h3>2.5 5xx 状态码</h3>

<p><code>5xx</code>状态码表示服务端错误。一般来说，API 不会向用户透露服务器的详细信息，所以只要两个状态码就够了。</p>

<p><code>500 Internal Server Error</code>：客户端请求有效，服务器处理时发生了意外。</p>

<p><code>503 Service Unavailable</code>：服务器无法处理请求，一般用于网站维护状态。</p>

<h2>三、服务器回应</h2>

<h3>3.1 不要返回纯本文</h3>

<p>API 返回的数据格式，不应该是纯文本，而应该是一个 JSON 对象，因为这样才能返回标准的结构化数据。所以，服务器回应的 HTTP 头的<code>Content-Type</code>属性要设为<code>application/json</code>。</p>

<p>客户端请求时，也要明确告诉服务器，可以接受 JSON 格式，即请求的 HTTP 头的<code>ACCEPT</code>属性也要设成<code>application/json</code>。下面是一个例子。</p>

<blockquote><pre><code class="language-http">
GET /orders/2 HTTP/1.1 
Accept: application/json
</code></pre></blockquote>

<h3>3.2 发生错误时，不要返回 200 状态码</h3>

<p>有一种不恰当的做法是，即使发生错误，也返回<code>200</code>状态码，把错误信息放在数据体里面，就像下面这样。</p>

<blockquote><pre><code class="language-http">
HTTP/1.1 200 OK
Content-Type: application/json

{
  "status": "failure",
  "data": {
    "error": "Expected at least two items in list."
  }
}
</code></pre></blockquote>

<p>上面代码中，解析数据体以后，才能得知操作失败。</p>

<p>这张做法实际上取消了状态码，这是完全不可取的。正确的做法是，状态码反映发生的错误，具体的错误信息放在数据体里面返回。下面是一个例子。</p>

<blockquote><pre><code class="language-http">
HTTP/1.1 400 Bad Request
Content-Type: application/json

{
  "error": "Invalid payoad.",
  "detail": {
     "surname": "This field is required."
  }
}
</code></pre></blockquote>

<h3>3.3 提供链接</h3>

<p>API 的使用者未必知道，URL 是怎么设计的。一个解决方法就是，在回应中，给出相关链接，便于下一步操作。这样的话，用户只要记住一个 URL，就可以发现其他的 URL。这种方法叫做 HATEOAS。</p>

<p>举例来说，GitHub 的 API 都在  这个域名。访问它，就可以得到其他 URL。</p>

<blockquote><pre><code class="language-http">
{
  ...
  "feeds_url": "https://api.github.com/feeds",
  "followers_url": "https://api.github.com/user/followers",
  "following_url": "https://api.github.com/user/following{/target}",
  "gists_url": "https://api.github.com/gists{/gist_id}",
  "hub_url": "https://api.github.com/hub",
  ...
}
</code></pre></blockquote>

<p>上面的回应中，挑一个 URL 访问，又可以得到别的 URL。对于用户来说，不需要记住  URL 设计，只要从 api.github.com 一步步查找就可以了。</p>

<p>HATEOAS 的格式没有统一规定，上面例子中，GitHub 将它们与其他属性放在一起。更好的做法应该是，将相关链接与其他属性分开。</p>

<blockquote><pre><code class="language-http">
HTTP/1.1 200 OK
Content-Type: application/json

{
  "status": "In progress",
   "links": {[
    { "rel":"cancel", "method": "delete", "href":"/api/status/12345" } ,
    { "rel":"edit", "method": "put", "href":"/api/status/12345" }
  ]}
}
</code></pre></blockquote>

<h2>四、参考链接</h2>

<ul>
<li>, by Florimond Manca</li>
<li>, by MicroSoft Azure </li>
</ul>

<p>（完）</p>

        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;border:1px solid #d3d3d3;margin:1em;background-color:#AAD2F0;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"><h3>文档信息</h3>
<ul>
<li>版权声明：自由转载-非商用-非衍生-保持署名（）</li>
<li>发表日期： <abbr class="published" title="2018-10-03T18:53:24+08:00">2018年10月 3日</abbr></li>
<li>更多内容：   » 
 
</li>
<li>文集：</li>
<li>社交媒体：</li>

</ul></div>        
        <div style="color:#556677;line-height:160%;padding:0.3em 0.5em;margin:1em;-moz-border-radius: 10px;-webkit-border-radius:10px;border-radius: 10px;"></div>
---------------
<h1 id="#title_1" >2、How To Build A News Application With Angular 6 And Material Design</h1>
Rachid Sakara
[https://www.smashingmagazine.com/2018/10/news-application-with-angular-and-material-design/](https://www.smashingmagazine.com/2018/10/news-application-with-angular-and-material-design/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/10/news-application-with-angular-and-material-design/" />
              <title>How To Build A News Application With Angular 6 And Material Design</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>How To Build A News Application With Angular 6 And Material Design</h1>
                  
                    
                    <address>Rachid Sakara</address>
                  
                  <time datetime="2018-10-03T12:00:26&#43;02:00" class="op-published">2018-10-03T12:00:26+02:00</time>
                  <time datetime="2018-10-03T19:12:50&#43;00:00" class="op-modified">2018-10-03T19:12:50+00:00</time>
                </header>
                

<p>Are you looking to combine Google’s  applications? Well, look no further!</p>

<p>In this tutorial, we’re going to build a news application using two of the most powerful and popular resources out there, Angular 6 and material design. You’ll learn how to incorporate Google’s material design components into Angular application templates to change and style your application in a professional way. The tutorial also serves as a reminder of how to make HTTP requests to bring live news articles to an application using the .</p>

<p>Before we get started building the app, let’s quickly review the resources we’re going to use, Angular and material design, and see why we’ve paired them to build this application?</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e7486f5f-7cb1-4a4e-b125-9f7fdeb11146/introduction.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e7486f5f-7cb1-4a4e-b125-9f7fdeb11146/introduction.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e7486f5f-7cb1-4a4e-b125-9f7fdeb11146/introduction.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e7486f5f-7cb1-4a4e-b125-9f7fdeb11146/introduction.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e7486f5f-7cb1-4a4e-b125-9f7fdeb11146/introduction.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e7486f5f-7cb1-4a4e-b125-9f7fdeb11146/introduction.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e7486f5f-7cb1-4a4e-b125-9f7fdeb11146/introduction.png"
			sizes="100vw"
			alt="A news application with Angular 6 and Material Design"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			A news application with Angular 6 and Material Design. ()
		</figcaption>
	
</figure>


<h3>What Is Angular?</h3>

<p>Angular &mdash; according to the  &mdash; is described as follows:</p>

<blockquote>“Angular is a platform that makes it easy to build applications with the web. Angular combines declarative templates, dependency injection, end-to-end tooling, and integrated best practices to solve development challenges. Angular empowers developers to build applications that live on the web, mobile, or the desktop.”</blockquote>

<p>In short, it’s the most powerful JavaScript framework for building highly interactive and dynamic web applications.</p>

<blockquote>“As mentioned, Angular is powerful, but also popular, which is why companies such as Upwork, Freelancer, Udemy, YouTube, Paypal, Nike, Google, Telegram, Weather, iStockphoto, AWS, Crunchbase are using it.”</blockquote>



<aside class="product-panel product-panel__tilted product-panel--book" data-audience="non-subscriber">
    <div class="container product-panel--book__container">
      <div class="panel__description panel__description--book">
    <p>Front-end is messy and complicated these days. That's why we publish  with a growing selection of <strong>front-end&nbsp;&amp;&nbsp;UX goodies</strong>. So you get your work done, better and faster.</p>

      <a href="https://smashed.by/perfpanelmembership" class="btn btn--green btn--large">
        Explore Smashing Membership&nbsp;↬
      </a>
      </div>
      <div class="panel__image panel__image--book">
        <a href="https://smashed.by/perfpanelmembership" class="books__book__image">
        <div class="books__book__img">
          <img src="https://www.smashingmagazine.com/images/smashing-cat/cat-rollerderby.svg" alt="Smashing Cat, just preparing to do some magic stuff." width="310" height="400">
        </div>
      </a>
      </div>
    </div>
  </aside>




<h3>What Is Google’s Material Design?</h3>

<p>Material design is a design language introduced by Google in the summer of 2014 for Android’s new OS. Although its initial focus was touch-based mobile apps, now its functionality has been extended to reach the web design world.</p>

<p>It’s an adaptable system of guidelines, components, and tools that support the best practices of user interface design. It’s also backed by open-source code and supported by a large community of designers and developers who are collaborating together to build beautiful products.</p>

<h3>Why Angular And Google’s Material Design Specifically?</h3>

<p>It’s a matter of choice. No JavaScript framework is better than another. It’s all about what your project needs. The same goes for programming languages.</p>

<p>Now, I’m not going to outline the benefits and features of Angular. Instead, I’m going to share with you why I’ve picked Angular specifically to build a news application.</p>

<p>As is always the case with any news application, communicating with back-end services over the HTTP protocol is a crucial part. This is where the newer Angular <strong>HttpClient module</strong>, which is an improved version of the old Http, can help us easily interact with the service API.</p>

<p><strong>The model-view-viewmodel</strong> (MVVM) of Angular will be handy when it comes to binding the remote data that will be stored in objects into our application template, where the component plays the part of the controller/viewmodel and where the template represents the view. This is what we call the Angular template language.</p>

<p><strong>The two-way binding system</strong>, which means that any changes in the application’s state will be automatically reflected into the view, and vice versa. You’ll notice that when selecting the news resources from the side menu, that will change the state of our news article. </p>

<p>What I like most about Angular is the <strong>SPA technology</strong>. Loading only the part of the page that needs to be changed will definitely help our application load and perform more quickly and smoothly.</p>

<p>Of course, there are many other benefits and features of Angular, which you can look up with a quick online search.</p>

<h3>What About The Visual Aspect?</h3>

<p>We’ve chosen material design because its language is a suitable fit for Angular, and it’s easy to implement.</p>

<p>It’s also a very popular visual language; it’s responsive, and most Google apps are built with it. We want our app to look as much like a Google app as possible.</p>

<p>As an introduction, that’s all we need. It’s time to look at the project overview and then jump into the build process.</p>

<ul>
<li></li>
<li></li>
<li></li>
<li></li>
<li></li>
<li></li>
<li></li>
<li></li>
<li></li>
</ul>

<h3 id="project-overview">Project Overview</h3>

<blockquote>“Getting the latest live news articles from a range of , including BBC News, CNN, TechCrunch, Huffington Post and more, along with different categories, like technology, sports, business, science and entertainment.”</blockquote>

<p>This is how your application will look when you finish it:</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fb95aed3-3e20-4908-af4d-2897375b4b46/project-overview.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fb95aed3-3e20-4908-af4d-2897375b4b46/project-overview.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fb95aed3-3e20-4908-af4d-2897375b4b46/project-overview.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fb95aed3-3e20-4908-af4d-2897375b4b46/project-overview.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fb95aed3-3e20-4908-af4d-2897375b4b46/project-overview.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fb95aed3-3e20-4908-af4d-2897375b4b46/project-overview.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/fb95aed3-3e20-4908-af4d-2897375b4b46/project-overview.png"
			sizes="100vw"
			alt="A news application overview"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Project overview. ()
		</figcaption>
	
</figure>


<p>That should get you excited, shouldn’t it? Let’s start by building the app.</p>

<h3 id="prerequisites">Prerequisites</h3>

<p>This is what you’re going to need in order to follow along with this tutorial:</p>

<ul>
<li> and npm installed on your machine;</li>
<li> installed on your machine;</li>
<li>A basic understanding of <strong>Angular</strong>.</li>
</ul>

<p>Once that stuff is out of the way, we can proceed.</p>

<h3 id="setting-up-an-angular-project">Setting Up The Angular Project</h3>

<p>In this section, we’re going to use the Angular command line interface (CLI) to generate a new Angular project. To do so, head over to the CLI and run this:</p>

<pre><code class="language-html">ng new news-app</code></pre>

<p>Next, point your command line to the project’s root folder by running the following:</p>

<pre><code class="language-html">cd news-app</code></pre>

<div class="sponsors__wide-place"></div>




<h3 id="installing-dependencies">Installing Dependencies</h3>

<p>To set up our dependencies, we’re going to install, with just one command, all of the dependencies necessary for this tutorial. Don’t worry, I’ll explain this in a second:</p>

<pre class="break-out"><code class="language-html">npm install --save @angular/material @angular/animations @angular/cdk</code></pre>

<p>We have three packages being installed with this command.</p>

<h4 id="angular-material">@angular/material</h4>

<p>This is the official material design package for the Angular framework.</p>

<h4 id="angular-animations">@angular/animations</h4>

<p>Installing the Angular animation package separately from the Angular core library is necessary. Certain material components need access to the animation libraries, which is why we’re installing it here.</p>

<h4 id="angular-cdk">@angular/cdk</h4>

<p>The <strong>CDK</strong> part stands for “component dev kit”, which provides us with high-quality predefined behaviors for your components, since modern web development is all about components.</p>

<p>It is recommended to include the Angular CDK any time you want to link Google’s material design to an Angular application.</p>

<p>To find out more about Angular CDK, check out this  .</p>

<p>Let’s run our app to see that everything works just fine. You can start a development server by running the following command:</p>

<pre class="break-out"><code class="language-html">ng serve</code></pre>

<p>Now, if you visit  in a browser, you should see the following page:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c232e07e-2f23-4a03-883d-9ecfeca1c638/welcome-to-news-app.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c232e07e-2f23-4a03-883d-9ecfeca1c638/welcome-to-news-app.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c232e07e-2f23-4a03-883d-9ecfeca1c638/welcome-to-news-app.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c232e07e-2f23-4a03-883d-9ecfeca1c638/welcome-to-news-app.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c232e07e-2f23-4a03-883d-9ecfeca1c638/welcome-to-news-app.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c232e07e-2f23-4a03-883d-9ecfeca1c638/welcome-to-news-app.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c232e07e-2f23-4a03-883d-9ecfeca1c638/welcome-to-news-app.png"
			sizes="100vw"
			alt="Welcome to news app"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Running the Angular project on development server. ()
		</figcaption>
	
</figure>


<p>Now, in your code editor, navigate to the file <code>/src/app/app.module.ts</code>, and add the following packages that we’ve just installed:</p>

<pre class="break-out"><code class="language-javascript">… Other imports …
import { BrowserAnimationsModule } from '@angular/platform-browser/animations';
import { MatButtonModule, MatCardModule, MatMenuModule, MatToolbarModule, MatIconModule, MatSidenavModule, MatListModule } from '@angular/material';
</code></pre>

<p>It is important to understand what’s going on here. First, we’re importing the animations package to animate our application a bit.</p>

<blockquote>The next import is what’s unique to Angular material. Before, we just included a single material module. Now, we have to import each material component that we intend to use.</blockquote>

<p>As you can see, we’ve added seven different modules here for material buttons, cards, menus, lists toolbars, side navigation, and icons.</p>

<p>After adding those packages to your <code>app.module.ts</code> file, make sure that your file matches the following:</p>

<pre class="break-out"><code class="language-css">import { BrowserModule } from '@angular/platform-browser';
import { NgModule } from '@angular/core';
import { HttpClientModule } from '@angular/common/http';
import { NewsApiService } from './news-api.service';

import { BrowserAnimationsModule } from '@angular/platform-browser/animations';
import { MatButtonModule, MatCardModule, MatMenuModule, MatToolbarModule, MatIconModule, MatSidenavModule, MatListModule } from '@angular/material';

import { AppComponent } from './app.component';

@NgModule({
  declarations: [
    AppComponent
  ],
  imports: [
    BrowserModule,
    BrowserAnimationsModule,
    HttpClientModule,
    MatButtonModule,
    MatMenuModule,
    MatCardModule,
    MatToolbarModule,
    MatIconModule,
    MatSidenavModule,
    MatListModule,
  ],
  providers: [NewsApiService],
  bootstrap: [AppComponent]
})
export class AppModule { }
</code></pre>

<p><strong>Note</strong>: <em>The statement</em> <strong>import { HttpClientModule } from @angular/common/http</strong><em> in the file above wasn’t generated automatically, but rather added manually. So, make sure you do that, too. And don’t worry about the <strong>NewsApiService</strong> service provider because we’re going to take care of that later on.</em></p>

<p>You might be wondering, though, how did I know the names of the modules to import? The official  gives you the exact code needed to import each module.</p>

<p>If you click on any of the components in the left menu and then click on the “API” tab, it provides you with the exact import line that you need to use.</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9b6bcd4d-406c-4859-a6db-aa510f258c2e/api-reference.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9b6bcd4d-406c-4859-a6db-aa510f258c2e/api-reference.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9b6bcd4d-406c-4859-a6db-aa510f258c2e/api-reference.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9b6bcd4d-406c-4859-a6db-aa510f258c2e/api-reference.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9b6bcd4d-406c-4859-a6db-aa510f258c2e/api-reference.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9b6bcd4d-406c-4859-a6db-aa510f258c2e/api-reference.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/9b6bcd4d-406c-4859-a6db-aa510f258c2e/api-reference.png"
			sizes="100vw"
			alt="API reference for Angular Material Components"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			API reference for Angular Material Component. ()
		</figcaption>
	
</figure>


<p>In terms of setup, that’s all we need to do before we actually begin using and integrating material components in our templates.</p>

<p>You just have to remember to import each unique component that you plan to use. </p>

<h3 id="acquiring-free-api-key">Acquiring Free API Key</h3>

<p>We’re going to use the  to feed us some news headlines as JSON data, which we’ll implement in the application template.</p>

<p>What is the News API service?</p>

<p>The News API is a simple HTTP REST API for searching and retrieving live articles from all over the web.</p>

<p>Now that you know what the News API is, the next step is to get a free , which will help us make some call requests to the server and grab the news articles.</p>

<p>You can sign up for just 30 seconds. You’ll only need to provide your first name, email address, and password. That’s all.</p>

<p>After signing up, you’ll find the API key already generated for you in the dashboard. Just save it in a text file somewhere on your desktop; because we’ll use it in the next chapter.</p>

<h3 id="working-on-components">Working On The Components</h3>

<p>To start working on the components, you need to create a service provider to manage the interaction with the News API service.</p>

<h4>Creating The Service Provider</h4>

<p>Enter this command to generate a new service provider:</p>

<pre><code class="language-html">ng generate service NewsApi
</code></pre>

<p>After that, go to the generated <code>/src/app/news-api.service.ts</code> file, and add the following code to it:</p>

<pre class="break-out"><code class="language-css">import { Injectable } from '@angular/core';
import { HttpClient  } from '@angular/common/http';


@Injectable({
  providedIn: 'root'
})
export class NewsApiService {

  api_key = 'PUT_YOUR_API_KEY_HERE';

  constructor(private http:HttpClient) { }
  initSources(){
     return this.http.get('https://newsapi.org/v2/sources?language=en&apiKey='+this.api_key);
  }
  initArticles(){
   return this.http.get('https://newsapi.org/v2/top-headlines?sources=techcrunch&apiKey='+this.api_key);
  }
  getArticlesByID(source: String){
   return this.http.get('https://newsapi.org/v2/top-headlines?sources='+source+'&apiKey='+this.api_key);
  }
} 
</code></pre>

<p>It’s time to use our <strong>API Key</strong>. Just paste it where it says, “Put_YOUR_API_KEY_HERE”.</p>

<p>We’ve imported <code>HttpClient</code>, which will be responsible for making API calls to our endpoints and fetching news headlines for us.</p>

<p>Now, for the <code>initSources</code> function, we simply prepare our left-side menu with some news resources. After that, we’ve created another function, <code>initArticles</code> which retrieves the first articles from <strong>TechCrunch</strong> once the application gets started.</p>

<p>As for the last function, <code>getArticlesByID</code>, it’s going to simply bring some articles for the passing parameter.</p>

<h4>The Main Component</h4>

<p>The service provider is done. Let’s move to the <code>/src/app/app.component.ts</code> file and add this code:</p>

<pre class="break-out"><code class="language-css">import { Component } from '@angular/core';
import { NewsApiService } from './news-api.service';


@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.css']
})
export class AppComponent {

mArticles:Array<any>;
mSources:Array<any>;
    
constructor(private newsapi:NewsApiService){}

ngOnInit() {
        //load articles
       this.newsapi.initArticles().subscribe(data => this.mArticles = data['articles']);
      //load news resources
     this.newsapi.initSources().subscribe(data=> this.mSources = data['sources']);    
}

searchArticles(source){
     this.newsapi.getArticlesByID(source).subscribe(data => this.mArticles = data['articles']);
}
}
</code></pre>

<p>We’re defining two properties here: <strong>mArticles</strong>, for holding news articles, and <strong>mSources</strong>, for holding news resources. Both are defined as an array.</p>

<p>In the constructor, we’re simply creating a <strong>NewsAPIService</strong> instance.</p>

<p>Next, we’re using that instance on the <strong>ngOnInit()</strong> function to initialize our two properties.</p>

<p>For the <strong>searchArticles</strong> function, it will be triggered whenever the user selects a specific resource from the left-side menu. Then we’re passing this parameter to the <strong>getArticlesByID</strong> service provider function to retrieves articles for it.</p>

<div class="sponsors__wide-place"></div>




<h3 id="defining-material-default-style">Defining Material’s Default Style</h3>

<p>In our <code>/src/styles.css</code> file, which is generated by the Angular CLI, let’s add the following:</p>

<pre class="break-out"><code class="language-css">@import '~@angular/material/prebuilt-themes/indigo-pink.css';
body {
    padding: 2em 23em;
    background:lightgray;
}
</code></pre>

<p>Based on your preference, you can change <code>indigo-pink.css</code> to:</p>

<ul>
<li>deeppurple-amber.css</li>
<li>indigo-pink.css</li>
<li>pink-bluegrey.css</li>
<li>purple-green.css</li>
</ul>

<p>I'm also adding some CSS to the <code>body</code> tag, only to demonstrate this layout. This helps it look more like an app, even on desktop.</p>

<p>Let’s also add two lines to our <code>/src/index.html</code> file just before the closing <code>head</code> tag:</p>

<pre class="break-out"><code class="language-html">&lt;link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet"&gt;
&lt;link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Roboto:300,400,500,700,400italic"&gt;
</code></pre>

<p>The first line imports the material design icon font, and the second one is the Roboto font, which is used by the material design team.</p>

<h3 id="define-a-template">Defining A Template</h3>

<p>Let’s start off by adding the following template in the <code>/src/app/app.component.html</code> file:</p>

<pre class="break-out"><code class="language-html">&lt;mat-toolbar color="primary"&gt;
  &lt;button mat-button (click)="sidenav.open ()" &gt;&lt;mat-icon&gt;menu&lt;/mat-icon&gt;&lt;/button&gt;
  &lt;span&gt;News Headlines&lt;/span&gt;  
  &lt;span class="example-spacer"&gt;&lt;/span&gt;
  &lt;button mat-button [matMenuTriggerFor]="appMenu"&gt;&lt;mat-icon&gt;settings&lt;/mat-icon&gt;&lt;/button&gt;
&lt;/mat-toolbar&gt;
&lt;mat-menu #appMenu="matMenu"&gt;
  &lt;button mat-menu-item&gt; Settings &lt;/button&gt;
  &lt;button mat-menu-item&gt; Help &lt;/button&gt;
&lt;/mat-menu&gt;
&lt;mat-sidenav-container class="example-container"&gt;
  
  &lt;mat-sidenav #sidenav class="example-sidenav"&gt;
    &lt;mat-list class="list-nav"&gt;
        &lt;mat-list-item class="list-item" *ngFor="let source of mSources" (click)="searchArticles(source.id);sidenav.close();"&gt;
          
          &lt;div mat-card-avatar [ngStyle]="{'background-image': 'url(../assets/images/'+ source.id +'.png)'}" class="example-header-image"&gt;&lt;/div&gt;
          
          &lt;span class="source-name"&gt; {{source.name}}&lt;/span&gt;
        
        &lt;/mat-list-item&gt;
    &lt;/mat-list&gt;
  &lt;/mat-sidenav&gt;
  &lt;mat-card class="example-card"  *ngFor="let article of mArticles"&gt;
    &lt;mat-card-header&gt;
      &lt;div mat-card-avatar [ngStyle]="{'background-image': 'url(../assets/images/'+ article.source.id +'.png)'}" class="example-header-image"&gt;&lt;/div&gt;
      &lt;mat-card-title class="title"&gt;{{article.title}}&lt;/mat-card-title&gt;
      &lt;mat-card-subtitle&gt;{{article.source.name}}&lt;/mat-card-subtitle&gt;
    &lt;/mat-card-header&gt;
    &lt;img mat-card-image class="img-article" src={{article.urlToImage}} alt=""&gt;
    &lt;mat-card-content&gt;
      &lt;p&gt;
        {{article.description}}
      &lt;/p&gt;
    &lt;/mat-card-content&gt;
    &lt;mat-card-actions class="action-buttons"&gt;
      &lt;button mat-button color="primary"&gt;&lt;mat-icon&gt;thumb_up_alt&lt;/mat-icon&gt; 12 Likes&lt;/button&gt;
      &lt;button mat-button color="primary"&gt;&lt;mat-icon&gt;comment&lt;/mat-icon&gt; Comments&lt;/button&gt;
      &lt;button mat-button color="primary"&gt;&lt;mat-icon&gt;share&lt;/mat-icon&gt; Share&lt;/button&gt;
      &lt;a mat-button color="primary" href={{article.url}} target="_blank" &gt;&lt;mat-icon&gt;visibility&lt;/mat-icon&gt; More&lt;/a&gt;
    &lt;/mat-card-actions&gt;
  &lt;/mat-card&gt;
&lt;/mat-sidenav-container&gt;
</code></pre>

<p>So, what have we done here?</p>

<p>First, we define a toolbar with a left-side menu, along with the application’s main title and the settings’ right menu.</p>

<p>Next, we’re using <code>*ngFor</code> for both sources and articles, and in doing so, our left-side menu will hold the news resources, and the main contents will hold the news articles.</p>

<p>One thing to notice is that on the <code>click</code> event of our list items, we’ve added two functions because that event executes any JavaScript code. The first function is <code>searchArticles</code>, which we’ve already explain, and the second one is <code>sidenav.close()</code> which will automatically close our left-side menu once the user has selected a resource.</p>

<h4>Styling Our Component</h4>

<p>The last thing to do with the components is to visit the <code>/src/app.component.css</code> file and paste the following code in it:</p>

<pre><code class="language-css">.example-spacer {
  flex: 1 1 auto;
}

.example-card{
    margin-top: 4px;
}

.example-header-image { 
  background-size: cover;
}

.title{
    font-weight: bold;
}

.img-article{
    height: 350px;
}

.action-buttons{
    text-align: center;
}
    
.example-container {
    width: 100%;
    height: auto;
    border: 1px solid rgba(111, 111, 111, 0.50);
}
  
.example-sidenav-content {
    display: flex;
    height: 75%;
    align-items: center;
    justify-content: center;
}
  
.example-sidenav {
    padding: 20px;
}

.source-name {
    margin-left:5px; 
}

.list-item:hover{
    cursor: pointer;
    background-color: #3f51b5;
    color: white;
}
</code></pre>

<h4>Set Up Images For News Resources</h4>

<p>Move to the <code>/src/assets</code> directory, and create a new folder named <code>images</code>. Then, download these images either from a .</p>

<p>They are the logos of our news resources. Once you download them, copy and paste all of the image files into the <code>images</code> folder that you just created.</p>

<p>Once everything is complete, run this:</p>

<pre class="break-out"><code class="language-html">ng serve</code></pre>

<p>Now, your app should look like the screenshot below. Pretty awesome, huh!</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7a7751f7-236b-4723-b00f-316c11cfca05/angular-material-design-final-product.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7a7751f7-236b-4723-b00f-316c11cfca05/angular-material-design-final-product.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7a7751f7-236b-4723-b00f-316c11cfca05/angular-material-design-final-product.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7a7751f7-236b-4723-b00f-316c11cfca05/angular-material-design-final-product.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7a7751f7-236b-4723-b00f-316c11cfca05/angular-material-design-final-product.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7a7751f7-236b-4723-b00f-316c11cfca05/angular-material-design-final-product.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7a7751f7-236b-4723-b00f-316c11cfca05/angular-material-design-final-product.png"
			sizes="100vw"
			alt="the news application final product"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Launching the app after everything is complete. ()
		</figcaption>
	
</figure>


<p>Note that when the news snippets are loaded on the main page, a “More” button (as you can see in the picture above) takes the user to read the whole story.</p>

<h3 id="conclusion">Conclusion</h3>

<p>There you have it! I hope this tutorial was useful and that you’ve enjoyed building this application. If so, feel free to leave your feedback and comments below. In the meantime, the  documentation is pretty cool. It provides you with an overview of each component, an API and an example.</p>

<p>The entire source code of this app is available on , which already implements the service API used in this tutorial.</p>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(ra, al, yk, il)</span>
</div>


              </article>
            </body>
          </html>
---------------
<h1 id="#title_2" >3、文章： 为什么在EOS上的dApp对开发人员来说不盈利？</h1>
Alex Vet
[http://www.infoq.com/cn/articles/why-dapp-on-eos-is-not-profitable-for-developers?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/why-dapp-on-eos-is-not-profitable-for-developers?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/why-dapp-on-eos-is-not-profitable-for-developers/zh/smallimage/devops-logo-1537695270184.jpg"/><p>EOS让开发人员承担交易和存储的成本。而ETH让用户承担成本。</p> <i>By Alex Vet</i> <i> Translated by 姚佳灵</i>
---------------
<h1 id="#title_3" >4、Amazon发布AWS存储网关硬件设备</h1>
Eldert Grootenboer
[http://www.infoq.com/cn/news/2018/10/aws-storage-gateway-appliance?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/10/aws-storage-gateway-appliance?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Amazon发布了他们的AWS存储网关硬件设备，在本地应用程序和AWS存储服务之间提供混合存储。通过提供硬件设备，Amazon提供了一种在本地缓存数据并与云保持同步的预配置解决方案。</p> <i>By Eldert Grootenboer</i> <i> Translated by 谢丽</i>
---------------