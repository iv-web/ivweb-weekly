## 文章索引
1、 <a href="#1sharing-code-between-projects:-lessons-learned-in-the-trenches" >Sharing Code Between Projects: Lessons Learned In The Trenches</a><br/>
2、 <a href="#2文章-区块链快速通道从技术原理到应用落地" >文章： 区块链快速通道：从技术原理到应用落地</a><br/>
3、 <a href="#3文章-基于云原生技术和服务网格的java-ee" >文章： 基于云原生技术和服务网格的Java EE</a><br/>
4、 <a href="#4文章-天天写业务代码如何成为技术大牛" >文章： 天天写「业务代码」，如何成为「技术大牛」？</a><br/>
5、 <a href="#5架构测试安全大数据宜人贷金融科技面面观" >架构、测试、安全、大数据：宜人贷金融科技面面观</a><br/>
6、 <a href="#6物联网技术周报第-134-期:-智能音箱-alexa-与-arduino-制作家门口的安全快递柜" >物联网技术周报第 134 期: 智能音箱 Alexa 与 Arduino 制作家门口的安全快递柜</a><br/>
7、 <a href="#7jdk-11版本时间表" >JDK 11版本时间表</a><br/>
8、 <a href="#8qcon北京2018圆满结束探索前沿技术最佳实践" >QCon北京2018圆满结束，探索前沿技术最佳实践</a><br/>
9、 <a href="#9从catchpoint的调查结果看网站可靠性工程师的工作" >从Catchpoint的调查结果看网站可靠性工程师的工作</a><br/><h1 id="#title_0" >1、Sharing Code Between Projects: Lessons Learned In The Trenches</h1>
Jonathan Saring
[https://www.smashingmagazine.com/2018/04/sharing-code-between-projects/](https://www.smashingmagazine.com/2018/04/sharing-code-between-projects/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/04/sharing-code-between-projects/" />
              <title>Sharing Code Between Projects: Lessons Learned In The Trenches</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>Sharing Code Between Projects: Lessons Learned In The Trenches</h1>
                  
                    
                    <address>Jonathan Saring</address>
                  
                  <time datetime="2018-04-25T14:40:51&#43;02:00" class="op-published">2018-04-25T14:40:51+02:00</time>
                  <time datetime="2018-04-25T19:51:24&#43;00:00" class="op-modified">2018-04-25T19:51:24+00:00</time>
                </header>
                <p>About a year ago, we came to a crossroad that changed the way we build software today. Like many other teams, we were working on a few things at a time, developing different projects for our web and mobile applications, with shared ingredients in the form of common Node.js code between our back-end repositoriess and microservices, and common React UI components with some slight visual and functional differences between our apps.</p>

<p>As our team grew and code lines multiplied, we began to realize that with every passing day <strong>we were writing the same code over and over again</strong>. Over time, it became harder to maintain our code base and develop new features with the same speed and efficiency.</p>

<p>Finally, we decided to find a solution that would enable us to share and sync common components of code between our projects. Here is what we learned along our journey, which eventually gave birth to .</p>











<figure >
	
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1a867ddc-af30-472b-8ef1-fd9a74164e59/01-sharing-code-between-projects.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1a867ddc-af30-472b-8ef1-fd9a74164e59/01-sharing-code-between-projects.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1a867ddc-af30-472b-8ef1-fd9a74164e59/01-sharing-code-between-projects.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1a867ddc-af30-472b-8ef1-fd9a74164e59/01-sharing-code-between-projects.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1a867ddc-af30-472b-8ef1-fd9a74164e59/01-sharing-code-between-projects.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/1a867ddc-af30-472b-8ef1-fd9a74164e59/01-sharing-code-between-projects.png"
			sizes="100vw"
			alt="Sharing code components between projects"
		/>
	

	
		<figcaption class="op-vertical-bottom">
			Code components as building blocks. ()
		</figcaption>
	
</figure>




<aside class="product-panel product-panel__tilted product-panel--book" data-audience="non-subscriber">
    <div class="container product-panel--book__container">
      <div class="panel__description panel__description--book">
    <p>What if there was a web conference without... slides? Meet <strong>. June <span class="small-caps">26–27</span>. With everything from live designing to live performance audits.</p>
      <a href="https://www.smashingmagazine.com/events/toronto-2018/#speakers" class="btn btn--green btn--large">
        Check the speakers&nbsp;→
      </a>
      </div>
      <div class="panel__image panel__image--book">
        <a href="https://www.smashingmagazine.com/events/toronto-2018/#speakers" class="books__book__image">
        <div class="books__book__img">
          <img src="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5a0383cf-197a-49b9-975a-9d1f02c1ace9/dan-hov.png" alt="SmashingConf Toronto 2018, with Dan Mall, Sara Soueidan, Lea Verou and many others." width="310" height="400">
        </div>
      </a>
      </div>
    </div>
  </aside>





<div class="c-garfield-the-cat">


<h3>Common Code In The Wild</h3>

<p>While Git is great for collaborating on a single repository, sharing code between multiple projects can be more challenging than we think.</p>

<p>To get started, we looked into our own code base to learn how many times we duplicated our own integration to our user service. The unbelievable result was no less than 86 instances. After the initial shock, we started thinking that this must also be happening elsewhere.</p>











<figure >
	
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b66750c6-d86a-48a5-b72d-186c70303b70/05-sharing-code-between-projects.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b66750c6-d86a-48a5-b72d-186c70303b70/05-sharing-code-between-projects.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b66750c6-d86a-48a5-b72d-186c70303b70/05-sharing-code-between-projects.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b66750c6-d86a-48a5-b72d-186c70303b70/05-sharing-code-between-projects.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b66750c6-d86a-48a5-b72d-186c70303b70/05-sharing-code-between-projects.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/b66750c6-d86a-48a5-b72d-186c70303b70/05-sharing-code-between-projects.png"
			sizes="100vw"
			alt="Code shared in multiple projects"
		/>
	

	
		<figcaption class="op-vertical-bottom">
			Using the same code in different places. ()
		</figcaption>
	
</figure>


<p>We asked some friends working in a few different organizations of various sizes to run a simple copy-and-paste detection on their code base, looking for duplicates of code longer than 100 lines. The result blew us away: On average, more than 30% of their code base was duplicated.</p>

<p>Finally, we decided to look deep into the open-source projects on GitHub, checking for both duplications and re-implementations of a simple <code>isString</code> function in the 10,000 most popular JavaScript GitHub projects.</p>

<p>Amazingly, we found <strong>this function was implemented in more than 100 different ways</strong> and duplicated over 1,000 times in only 10,000 repositories. Later studies claim that over 50% of the code on GitHub is actually . We realized we were not the only ones facing this issue.</p>

<h3>Looking For A Solution</h3>

<p>Before building , we looked for a tool that would help us turn the smaller components that our apps are built from into building blocks that could be shared between our projects and synced across our code base. We also wanted to organize them and make them discoverable for our team. Here’s a short summary of what we learned.</p>

<h4>A Micro-Package Arsenal With NPM</h4>

<p>At first, we considered publishing all of our UI components, utility functions and smaller modules as packages to NPM. This seemed like the obvious solution for modularity for our software’s building blocks. However, we quickly learned that this solution came with huge overhead.</p>

<p>Trying to publish a few files from our project to NPM forced us to split our repository and create new ones just to share this code. When dealing with hundreds of components, <strong>this meant having to maintain and make changes across hundreds of repositories</strong>.</p>

<p>We would also have to refactor our code base, removing the newly created packages from their original repositories, boilerplating the packages in the new repositories and so on.</p>

<p>Even then, we had now a simple way to organize these packages and make them easily  to our entire team. Another major problem was the coupling between the packages and the owners of their origin repositories, which made it nearly impossible for other people to quickly make updates to the packages while working on their own projects.</p>

<p>This kind of overhead was too much for us to handle. So, we quickly decided to look for a better way to share our code.</p>

<h4>Lerna Monorepos</h4>

<p>The next option we came up with was to use  in order to refactor our code base into a few multi-package repositories, often referred to as “monorepos”.</p>











<figure >
	
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0c2d8af6-10ab-44c5-98c6-bff611315f09/06-sharing-code-between-projects.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0c2d8af6-10ab-44c5-98c6-bff611315f09/06-sharing-code-between-projects.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0c2d8af6-10ab-44c5-98c6-bff611315f09/06-sharing-code-between-projects.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0c2d8af6-10ab-44c5-98c6-bff611315f09/06-sharing-code-between-projects.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0c2d8af6-10ab-44c5-98c6-bff611315f09/06-sharing-code-between-projects.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/0c2d8af6-10ab-44c5-98c6-bff611315f09/06-sharing-code-between-projects.png"
			sizes="100vw"
			alt="The Hydra of Lerna"
		/>
	

	
		<figcaption class="op-vertical-bottom">
			Lerna multi-package repository. ()
		</figcaption>
	
</figure>


<p>The upside of this solution was that it would allow us to maintain and publish all our packages from a single repository. However, this option, too, came with a set of drawbacks, particularly when working with smaller components.</p>

<p>Choosing this option meant we would still have to effectively keep multiple packages with multiple <code>package.json</code> files, multiple build and test environments and a complicated dependency tree to handle between them. Updating these packages must also go through the main repository, still making it hard to modify these package from other projects when working with a few separate monorepos.</p>

<p>For example, take the popular  React UI library. Even though it uses Lerna to publish five different packages from the same repository, you would still have to install the entire library to use each of its components. Making changes would still have to go through that project as well, and discoverability for these component didn’t improve.</p>

<p>Monorepos can be great for some cases (such as testing or building a project as a whole) and can definitely work for some teams. However, refactoring your entire code base just to share common code between projects while still having to struggle with the issues mentioned above made us drop this option as well.</p>

<h3>Shared Libraries</h3>

<p>This option was quickly dropped, too. In a lot of way, it resembles using a CD-ROMs instead of an iTunes playlist. First, it made no sense to force an entire library of React components and an entire utility library and so on on each of our projects.</p>

<p>Secondly, every project using it would be tightly coupled to the development of this library, making it impossible to adjust its components for each project. This becomes most painful when sharing common Node.js code between our microservices, which would now be coupled to the library.</p>

<p>Thirdly, discoverability within the library is bound to be poor and would involve a lot of work with its documentation and usage in different edge cases.</p>

<p>Because it makes very little sense to couple and slow down our development, we try to <strong>minimize the use of these libraries as much as possible</strong>. Even popular JavaScript utility libraries such as Lodash are working hard to make their smaller components  via NPM.</p>

<h4>Git Submodules</h4>

<p>Finally, we turned back time and looked into working with .</p>

<p><blockquote class="twitter-tweet" data-lang="en"><p lang="en" dir="ltr">You there.  You&#39;re thinking about using a Git submodule.  DON&#39;T.  Just don&#39;t.  It&#39;s not worth it, ever.</p>&mdash; Jeremy Kahn (@jeremyckahn) </blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script></p>

<p>Git enables you to make one repository a subdirectory of another repository, creating a single working tree for the entire project, so that a repository can utilize code from another repository.</p>

<p>As for many other teams, this solution did not last for us. First, submodules only work on the master branch, which causes problems for rapid development. Secondly, submodules increase coupling between projects, which makes it hard to work on cross-repository assignments. Finally, a submodule repository is oblivious to its own nesting and the existence of dependent repositories.</p>

<p>After trying these different solutions, we realized that it shouldn’t be this complicated. There really should be <strong>a simpler way to organize, share and develop components of code</strong> from different projects.  So, we decided to build it, and called it .</p>

<h3>Building Bit</h3>

<p>Our vision for a solution was simple: turn our components and modules into building blocks that can be easily isolated from any project, organized in the cloud and used in any project.</p>

<p>









<figure >
	
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bd15a981-1f30-4b9b-836d-0ae9cb226b6a/04-sharing-code-between-projects.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bd15a981-1f30-4b9b-836d-0ae9cb226b6a/04-sharing-code-between-projects.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bd15a981-1f30-4b9b-836d-0ae9cb226b6a/04-sharing-code-between-projects.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bd15a981-1f30-4b9b-836d-0ae9cb226b6a/04-sharing-code-between-projects.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bd15a981-1f30-4b9b-836d-0ae9cb226b6a/04-sharing-code-between-projects.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/bd15a981-1f30-4b9b-836d-0ae9cb226b6a/04-sharing-code-between-projects.png"
			sizes="100vw"
			alt="Bit sharing workflow"
		/>
	

	
		<figcaption class="op-vertical-bottom">
			Isolate, share and organize your reusable code. ()
		</figcaption>
	
</figure>

<p>When building it, we set a few guidelines for what we needed from the project.</p></p>

<ul>
<li>Make it seamless to isolate and share code components from any project, without having to create new repositories or manually configure build and test environments and dependencies for each component.</li>
<li>Enable two-way development, so that each component could be changed and updated from any project, while changes would be synced across our code base.</li>
<li>Make it simple to organize and share our components, while making them discoverable for our entire team with useful visual information.</li>
</ul>

<p>After hard work and extensive research, in 2017 we released the first version of  to GitHub.</p>

<h4>How It Works</h4>

<p> is made of three simple steps:</p>

<ol>
    <li>The first is to simply tell Bit which components of code you would like to share from your project, and it will immediately start tracking them in all of the projects you share them in.</li>
    <li>You can then tag a version for these components so that Bit automatically defines and locks their dependency tree for both file and package dependencies, and creates an isolated environment for each component to build and test in isolation.</li>
    <li>Finally, you can share the components to the cloud (or your own remote server), where they will be organized, will be made discoverable and can be installed with NPM or Yarn like any other package.</li>
</ol>

<p>You don’t have to create new repositories, split your code base or refactor a single line of code.</p>


  <div id="sponsors-article" data-impression="true" class="c-promo-box c-promo-box--ad sponsors hidden" data-audience="non-subscriber" data-remove="true"></div>



<p>Now comes the really cool part. You can also <strong>use Bit to import the components into other projects</strong> for further development. Because Bit tracks your components between projects, you can simultaneously develop them from different repositories and sync changes across your code base.</p>

<p>This fast and distributed workflow means you won’t be tied by ownership issues, and you can actually develop the shared code and update changes from any of your team’s projects.</p>

<p>Let’s see an example.</p>

<h4>Example: Bit With React UI Components</h4>











<figure >
	
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/625fcc75-6aed-46c0-b5cd-9ff1f1895397/07-sharing-code-between-projects.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/625fcc75-6aed-46c0-b5cd-9ff1f1895397/07-sharing-code-between-projects.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/625fcc75-6aed-46c0-b5cd-9ff1f1895397/07-sharing-code-between-projects.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/625fcc75-6aed-46c0-b5cd-9ff1f1895397/07-sharing-code-between-projects.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/625fcc75-6aed-46c0-b5cd-9ff1f1895397/07-sharing-code-between-projects.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/625fcc75-6aed-46c0-b5cd-9ff1f1895397/07-sharing-code-between-projects.png"
			sizes="100vw"
			alt="A React Hero component with Bit"
		/>
	

	
		<figcaption class="op-vertical-bottom">
			A )
		</figcaption>
	
</figure>


<p>For this example, let’s pick a common use case: syncing React UI components between apps. Although designed to be reusable, achieving such reusability can be .</p>

<p>Let’s take an example  on Bit’s free web hub.</p>

<p>As you can see, <strong>each of the components is now available to any developer</strong> to install with NPM or Yarn or to import into their own projects for further development.</p>

<p>All of the components are organized and can be shared with your team and searched for via a search engine. They are presented with visual rendering, build and test results (you can use premade external build and test  or create your own), and come with auto-parsed docs so that you can make an informed decision on which components to use.</p>

<p>Once it’s changed from a different project, you can update the component’s version in the scope (which works as a remote source of truth) and sync changes between different repositories.</p>

<p>A short  is available for the example project.</p>

<h3>Conclusion</h3>

<p>Sharing code between projects is vital to building software faster, while making your code base simpler to maintain and develop over time. As more of our applications are built using reusable components such as React and Vue UI components, Node.js modules, simple functions, GraphQL APIs and more, turning them into building blocks for different projects becomes more rewarding.</p>

<p>However, the overhead of splitting repositories, refactoring projects, and modifying components from different projects can make it hard to effectively collaborate and share your code. These are the lessons learned from our own journey towards <strong>simple and effective code sharing</strong>, making it simpler to share, discover and collaborate as a team while building with our common LEGO bricks.</p>

<p>Bit is an open-source project, so feel free to . Just remember that, at the end of the day, sharing code is always about people and about growing a collaborative culture where people play together to build great things.</p>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(rb, ra, al, yk, il)</span>
</div>



  <div id="sponsors-article-end" data-impression="true" class="c-promo-box c-promo-box--ad c-promo-box--wide sponsors hidden" data-audience="non-subscriber" data-remove="true"></div>



</div>



              </article>
            </body>
          </html>
---------------
<h1 id="#title_1" >2、文章： 区块链快速通道：从技术原理到应用落地</h1>
李晨
[http://www.infoq.com/cn/articles/blockchain-from-theory-to-lannding?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/blockchain-from-theory-to-lannding?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/blockchain-from-theory-to-lannding/zh/smallimage/logo-devops-1517322113546-1524676331239.jpeg"/><p>区块链是机遇也是挑战，如何在这风起云涌的区块链世界里获得加速卡实现弯道超车？没有区块链技术基础的你又怎样迅速部署属于自己的第一个应用？ 为了解决一部分粉丝的困惑，我们邀请到万向区块链旗下万云平台首席架构师兼产品总监李晨，从以下两个方面为大家分享他和万云团队对区块链技术及应用的思考：一是对区块链技术进行基本介绍，尤其是区块链的发展历史和核心技术；二是分享万云平台在区块链行业当中的探索。</p> <i>By 李晨</i>
---------------
<h1 id="#title_2" >3、文章： 基于云原生技术和服务网格的Java EE</h1>
Sebastian Daschner
[http://www.infoq.com/cn/articles/cloud-native-service-mesh-java-ee?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/cloud-native-service-mesh-java-ee?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/cloud-native-service-mesh-java-ee/zh/smallimage/GettyImages-845809800-1524208773636.jpg"/><p>Java EE可以很容易地与云原生技术（如Kubernetes或Istio）结合在一起，用以构建现代化的以服务为驱动的应用程序。</p> <i>By Sebastian Daschner</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_3" >4、文章： 天天写「业务代码」，如何成为「技术大牛」？</h1>
李运华
[http://www.infoq.com/cn/articles/how-to-become-tech-master?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/how-to-become-tech-master?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/how-to-become-tech-master/zh/smallimage/GettyImages-628619884-1514929417641-1524401958791.jpg"/><p>不管是开发、测试、运维，每个技术人员心理多多少少都有一个成为技术大牛的梦，毕竟“梦想总是要有的，万一实现了呢”！正是对技术梦的追求，促使我们不断地努力和提升自己。然而……</p> <i>By 李运华</i>
---------------
<h1 id="#title_4" >5、架构、测试、安全、大数据：宜人贷金融科技面面观</h1>
张晓楠
[http://www.infoq.com/cn/news/2018/04/Caesar-Drools-ATDD?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/04/Caesar-Drools-ATDD?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>
4月20日-22日，QCon全球软件开发大会在北京召开，宜人贷与大会主办方极客邦科技共同打造“金融科技的创新实践”宜人贷技术专场，为金融、互联网行业对金融科技感兴趣的从业者呈现“业务高速发展下的互联网金融系统架构演进”、“前后端自动化测试前置的实践与落地”、“互联网场景下的办公网安全”、“数据驱动金融科技：从营销到反欺诈”四场主题分享，并通过“我的技术管理之道”圆桌对话，为技术人进阶管理提供建议。</p> <i>By 张晓楠</i>
---------------
<h1 id="#title_5" >6、物联网技术周报第 134 期: 智能音箱 Alexa 与 Arduino 制作家门口的安全快递柜</h1>
黄峰达
[http://www.infoq.com/cn/news/2018/04/iot-weekly-134?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/04/iot-weekly-134?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>智能音箱 Alexa 与 Arduino 制作家门口的安全快递柜；使用 IoT 技术创建简单而有趣的加速计游戏；车纷享：基于阿里云 HBase 构建车联网平台实践；联发科与微软合作推出物联网专用芯片组；Facebook 新研究成果：通过手臂皮肤震动阅读文字；靠近物联网 微软发布定制 Linux 内核；Qualcomm 发布专门面向物联网终端的视觉智能平台 集成摄像头、人工智能和计算机视觉领域的最新技术；阿里全资收购中天微 力主研发AI“中国芯”</p> <i>By 黄峰达</i>
---------------
<h1 id="#title_6" >7、JDK 11版本时间表</h1>
Michael Redlich
[http://www.infoq.com/cn/news/2018/04/proposed-schedule-for-jdk-11?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/04/proposed-schedule-for-jdk-11?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Oracle首席架构师Mark Reinhold最近提出了将于2018年9月发布的JDK 11 GA版本的时间表。JEP-320的新功能之一是移除可能会破坏现有应用程序的Java EE和CORBA模块。</p> <i>By Michael Redlich</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_7" >8、QCon北京2018圆满结束，探索前沿技术最佳实践</h1>
师海君
[http://www.infoq.com/cn/news/2018/04/QCon-beijing-2018?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/04/QCon-beijing-2018?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>由极客邦科技与 InfoQ 中国主办的 QCon全球软件开发大会，于 2018年4月20 日 - 22日在北京国际会议中心举办。本次大会特邀 200 多位国内外技术专家，与 2000 余名技术管理者、架构师共同分享和交流新技术在行业应用中的最新实践，助力企业技术选型、业务升级与顺利转型。</p> <i>By 师海君</i>
---------------
<h1 id="#title_8" >9、从Catchpoint的调查结果看网站可靠性工程师的工作</h1>
Helen Beal
[http://www.infoq.com/cn/news/2018/04/Site-Reliability-Engineer-Survey?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/04/Site-Reliability-Engineer-Survey?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>和软件工程师一样，网站可靠性管理工程师需要负责IT运营，2003年Google就推出了这一设想，2016年Google推出了《网站可靠性管理，Google如何运营生产系统》一书，详细介绍了这一方面内容。网站监测服务公司Catchpoint最近调查了416名网站可靠性管理工程师（SRE），希望借此了解SRE的具体工作。</p> <i>By Helen Beal</i> <i> Translated by 刘嘉洋</i>
---------------