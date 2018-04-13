## 文章索引
1、 <a href="#1automating-your-feature-testing-with-selenium-webdriver" >Automating Your Feature Testing With Selenium WebDriver</a><br/>
2、 <a href="#2文章-pwa登陆ios了但它还有这些缺陷" >文章： PWA登陆iOS了，但它还有这些缺陷</a><br/>
3、 <a href="#3文章-深入理解服务型领导力" >文章： 深入理解服务型领导力</a><br/>
4、 <a href="#4文章-re如何让你的敏捷开发真正起效" >文章： Re：如何让你的敏捷开发真正起效</a><br/>
5、 <a href="#5视频演讲-ios-app-内存专项实践封闭系统下的大自由" >视频演讲： iOS App 内存专项实践：封闭系统下的大自由</a><br/>
6、 <a href="#6采访nicole-forsgren博士dora与google就devops促进状态报告开展合作" >采访Nicole Forsgren博士：DORA与Google就《DevOps促进状态报告》开展合作</a><br/>
7、 <a href="#7敏捷团队心理安全的培养" >敏捷团队心理安全的培养</a><br/>
8、 <a href="#8typescript-28引入条件类型" >TypeScript 2.8引入条件类型</a><br/>
9、 <a href="#9visual-studio-2017-157预览版发布" >Visual Studio 2017 15.7预览版发布</a><br/>
10、 <a href="#10hyperledger添加caliper度量区块链性能" >Hyperledger添加Caliper度量区块链性能</a><br/><h1 id="#title_0" >1、Automating Your Feature Testing With Selenium WebDriver</h1>
Nils Schütte
[https://www.smashingmagazine.com/2018/04/feature-testing-selenium-webdriver/](https://www.smashingmagazine.com/2018/04/feature-testing-selenium-webdriver/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/04/feature-testing-selenium-webdriver/" />
              <title>Automating Your Feature Testing With Selenium WebDriver</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>Automating Your Feature Testing With Selenium WebDriver</h1>
                  
                    
                    <address>Nils Schütte</address>
                  
                  <time datetime="2018-04-12T12:45:54&#43;02:00" class="op-published">2018-04-12T12:45:54+02:00</time>
                  <time datetime="2018-04-12T12:25:05&#43;00:00" class="op-modified">2018-04-12T12:25:05+00:00</time>
                </header>
                

<p>This article is for web developers who wish to spend less time testing the front end of their web applications but still want to be confident that every feature works fine. It will save you time by automating repetitive online tasks with Selenium WebDriver. You will find a step-by-step example for automating and testing the login function of WordPress, but you can also adapt the example for any other login form.</p>

<h3 id="what-is-selenium-and-how-can-it-help-you">What Is Selenium And How Can It Help You?</h3>

<p>Selenium is a framework for the automated testing of web applications. Using Selenium, you can basically automate every task in your browser as if a real person were to execute the task. The interface used to send commands to the different browsers is called Selenium WebDriver. Implementations of this interface are available for every major browser, including Mozilla Firefox, Google Chrome and Internet Explorer.</p>

<h3 id="automating-your-feature-testing-with-selenium-webdriver">Automating Your Feature Testing With Selenium WebDriver</h3>

<p>Which type of web developer are you? Are you the disciplined type who tests all key features of your web application after each deployment. If so, you are probably annoyed by how much time this repetitive testing consumes. Or are you the type who just doesn’t bother with testing key features and always thinks, &ldquo;I should test more, but I’d rather develop new stuff.&rdquo; If so, you probably only find bugs by chance or when your client or boss complains about them.</p>

<p>I have been working for a well-known online retailer in Germany for quite a while, and I always belonged to the second category: It was so exciting to think of new features for the online shop, and I didn’t like at all going over all of the previous features again after each new software deployment. So, the strategy was more or less to hope that all key features would work.</p>



<aside class="product-panel product-panel__tilted product-panel--book" data-audience="non-subscriber">
    <div class="container product-panel--book__container">
      <div class="panel__description panel__description--book">
    <p>Nope, we can't do any magic tricks, but we have articles,  get a seasoned selection of magic front-end tricks — e.g. <strong>live designing sessions</strong> and perf audits, too. <em>Just sayin'</em>! ;-)</p>

      <a href="https://www.smashingmagazine.com/membership/?utm_medium=panel" class="btn btn--green btn--large">
        Explore Smashing Wizardry&nbsp;→
      </a>
      </div>
      <div class="panel__image panel__image--book">
        <a href="https://www.smashingmagazine.com/membership/?utm_medium=panel" class="books__book__image">
        <div class="books__book__img">
          <img src="https://www.smashingmagazine.com/images/smashing-cat/cat-wizard.svg" alt="Smashing Cat, just preparing to do some magic stuff." width="310" height="400">
        </div>
      </a>
      </div>
    </div>
  </aside>





<div class="c-garfield-the-cat">


<p>One day, we had a serious drop in our conversion rate and started digging in our web analytics tools to find the source of this drop. It took quite a while before we found out that our checkout did not work properly since the previous software deployment.</p>

<p>This was the day when I started to do some research about automating our testing process of web applications, and I stumbled upon Selenium and its WebDriver. Selenium is basically a framework that allows you to automate web browsers. WebDriver is the name of the key interface that allows you to send commands to all major browsers (mobile and desktop) and work with them as a real user would.</p>

<h3 id="preparing-the-first-test-with-selenium-webdriver">Preparing The First Test With Selenium WebDriver</h3>

<p>First, I was a little skeptical of whether Selenium would suit my needs because the framework is most commonly used in Java, and I am certainly not a Java expert. Later, I learned that being a Java expert is not necessary to take advantage of the power of the Selenium framework.</p>

<p>As a simple first test, I tested the login of one of my WordPress projects. Why WordPress? Just because using the WordPress login form is an example that everybody can follow more easily than if I were to refer to some custom web application.</p>

<p>What do you need to start using Selenium WebDriver? Because I decided to use the most common implementation of Selenium in Java, I needed to set up my little Java environment.</p>

<p>If you want to follow my example, you can use the Java environment of your choice. If you haven’t set one up yet, I suggest .</p>

<p>Because I wanted to test the login in Chrome, I made sure that the Chrome browser was already installed on my machine. That’s all I did in preparation.</p>

<h3 id="downloading-the-chromedriver">Downloading The ChromeDriver</h3>

<p>All major browsers provide their own implementation of the WebDriver interface. Because I wanted to test the WordPress login in Chrome, I needed to get the WebDriver implementation of Chrome: </p>

<p>I extracted the ZIP archive and stored the executable file <code>chromedriver.exe</code> in a location that I could remember for later.</p>

<h3 id="setting-up-our-selenium-project-in-eclipse">Setting Up Our Selenium Project In Eclipse</h3>

<p>The steps I took in Eclipse are probably pretty basic to someone who works a lot with Java and Eclipse. But for those like me, who are not so familiar with this, I will go over the individual steps:</p>

<ol>
    <li>Open Eclipse.</li>
    <li>Click the "New" icon.<br />
        <figure><figcaption>Creating a new project in Eclipse</figcaption></figure>
    </li>
    <li>Choose the wizard to create a new "Java Project," and click “Next.”<br />
        <figure><figcaption>Choose the java-project wizard.</figcaption></figure>
    </li>
    <li>Give your project a name, and click "Finish."<br />
        <figure><figcaption>The eclipse project wizard</figcaption></figure>
    </li>
    <li>Now you should see your new Java project on the left side of the screen.<br />
        <figure><figcaption>We successfully created a project to run the Selenium WebDriver.</figcaption></figure>
    </li>
</ol>

<h3 id="adding-the-selenium-library-to-our-project">Adding The Selenium Library To Our Project</h3>

<p>Now we have our Java project, but Selenium is still missing. So, next, we need to bring the Selenium framework into our Java project. Here are the steps I took:</p>

<ol>
    <li>Download the  of the Java Selenium library.<br/>
        <figure><figcaption>Download the Selenium library.</figcaption></figure>
    </li>
    <li>Extract the archive, and store the folder in a place you can remember easily.</li>
    <li>Go back to Eclipse, and go to "Project" &rarr; “Properties.”<br />
        <figure><figcaption>Go to properties to integrate the Selenium WebDriver in you project.</figcaption></figure>
    </li>
    <li>In the dialog, go to "Java Build Path" and then to register “Libraries.”</li>
    <li>Click on "Add External JARs."<br />
        <figure><figcaption> Add the Selenium lib to your Java build path.</figcaption></figure>
    </li>
    <li>Navigate to the just downloaded folder with the Selenium library. Highlight all <code>.jar</code> files and click "Open."<br />
        <figure><figcaption>Select all files of the lib to add to your project.</figcaption></figure>
    </li>
    <li>Repeat this for all <code>.jar</code> files in the subfolder <code>libs</code> as well.</li>
    <li>Eventually, you should see all <code>.jar</code> files in the libraries of your project:<br />
        <figure><figcaption>The Selenium WebDriver framework has now been successfully integrated into your project!</figcaption></figure>
    </li>
</ol>

<p>That’s it! Everything we’ve done until now is a one-time task. You could use this project now for all of your different tests, and you wouldn’t need to do the whole setup process for every test case again. Kind of neat, isn’t it?</p>

<h3 id="creating-our-testing-class-and-letting-it-open-the-chrome-browser">Creating Our Testing Class And Letting It Open the Chrome Browser</h3>


  <div id="sponsors-article" data-impression="true" class="c-promo-box c-promo-box--ad sponsors hidden" data-audience="non-subscriber" data-remove="true"></div>



<p>Now we have our Selenium project, but what next? To see whether it works at all, I wanted to try something really simple, like just opening my Chrome browser.</p>

<p>To do this, I needed to create a new Java class from which I could execute my first test case. Into this executable class, I copied a few Java code lines, and believe it or not, it worked! Magically, the Chrome browser opened and, after a few seconds, closed all by itself.</p>

<p>Try it yourself:</p>

<ol>
    <li>Click on the "New" button again (while you are in your new project’s folder).<br />
        <figure><figcaption>Create a new class to run the Selenium WebDriver.</figcaption></figure>
    </li>
    <li>Choose the "Class" wizard, and click “Next.”<br />
        <figure><figcaption>Choose the Java class wizard to create a new class.</figcaption></figure>
    </li>
    <li>Name your class (for example, "RunTest"), and click “Finish.”<br />
        <figure><figcaption>The eclipse Java Class wizard.</figcaption></figure>
    </li>
    <li>Replace all code in your new class with the following code. The only thing you need to change is the path to <code>chromedriver.exe</code> on your computer:<br />
<pre class="break-out"><code class="language-bash">import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;

/**
 * @author Nils Schuette via frontendtest.org
 */
public class RunTest {
    static WebDriver webDriver;
    /**
     * @param args
     * @throws InterruptedException
     */
    public static void main(final String[] args) throws InterruptedException {
        // Telling the system where to find the chrome driver
        System.setProperty(
                "webdriver.chrome.driver",
                "C:/PATH/TO/chromedriver.exe");

        // Open the Chrome browser
        webDriver = new ChromeDriver();

        // Waiting a bit before closing
        Thread.sleep(7000);

        // Closing the browser and WebDriver
        webDriver.close();
        webDriver.quit();
    }
}
</code></pre></li>
<li>Save your file, and click on the play button to run your code.<br />
    <figure><figcaption>Running your first Selenium WebDriver project.</figcaption></figure>
</li>
<li>If you have done everything correctly, the code should open a new instance of the Chrome browser and close it shortly thereafter.<br />
    <figure>)</figcaption></figure>
</li>
</ol>

<h3 id="testing-the-wordpress-admin-login">Testing The WordPress Admin Login</h3>

<p>Now I was optimistic that I could automate my first little feature test. I wanted the browser to navigate to one of my WordPress projects, login to the admin area and verify that the login was successful. So, what commands did I need to look up?</p>

<ol>
<li>Navigate to the login form,</li>
<li>Locate the input fields,</li>
<li>Type the username and password into the input fields,</li>
<li>Hit the login button,</li>
<li>Compare the current page’s headline to see if the login was successful.</li>
</ol>

<p>Again, after I had done all the necessary updates to my code and clicked on the run button in Eclipse, my browser started to magically work itself through the WordPress login. I successfully ran my first automated website test!</p>

<p>If you want to try this yourself, replace all of the code of your Java class with the following. I will go through the code in detail afterwards. Before executing the code, you must replace four values with your own:</p>

<ol>
<li><p>The location of your <code>chromedriver.exe</code> file (as above),</p></li>

<li><p>The URL of the WordPress admin account that you want to test,</p></li>

<li><p>The WordPress username,</p></li>

<li><p>The WordPress password.</p></li>
</ol>

<p>Then, save and let it run again. It will open Chrome, navigate to the login of your WordPress website, login and check whether the <code>h1</code> headline of the current page is &ldquo;Dashboard.&rdquo;</p>

<pre class="break-out"><code class="language-bash">import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;

/**
 * @author Nils Schuette via frontendtest.org
 */
public class RunTest {
    static WebDriver webDriver;
    /**
     * @param args
     * @throws InterruptedException
     */
    public static void main(final String[] args) throws InterruptedException {
        // Telling the system where to find the chrome driver
        System.setProperty(
                "webdriver.chrome.driver",
                "C:/PATH/TO/chromedriver.exe");

        // Open the Chrome browser
        webDriver = new ChromeDriver();

        // Maximize the browser window
        webDriver.manage().window().maximize();

        if (testWordpresslogin()) {
            System.out.println("Test Wordpress Login: Passed");
        } else {
            System.out.println("Test Wordpress Login: Failed");

        }

        // Close the browser and WebDriver
        webDriver.close();
        webDriver.quit();
    }

    private static boolean testWordpresslogin() {
        try {
            // Open google.com
            webDriver.navigate().to("https://www.YOUR-SITE.org/wp-admin/");

            // Type in the username
            webDriver.findElement(By.id("user_login")).sendKeys("YOUR_USERNAME");

            // Type in the password
            webDriver.findElement(By.id("user_pass")).sendKeys("YOUR_PASSWORD");

            // Click the Submit button
            webDriver.findElement(By.id("wp-submit")).click();

            // Wait a little bit (7000 milliseconds)
            Thread.sleep(7000);

            // Check whether the h1 equals “Dashboard”
            if (webDriver.findElement(By.tagName("h1")).getText()
                    .equals("Dashboard")) {
                return true;
            } else {
                return false;
            }

        // If anything goes wrong, return false.
        } catch (final Exception e) {
            System.out.println(e.getClass().toString());
            return false;
        }
    }
}
</code></pre>

<p>If you have done everything correctly, your output in the Eclipse console should look something like this:</p>

<figure>)</figcaption></figure>

<h3 id="understanding-the-code">Understanding The Code</h3>

<p>Because you are probably a web developer and have at least a basic understanding of other programming languages, I am sure you already grasp the basic idea of the code: We have created a separate method, <code>testWordpressLogin</code>, for the specific test case that is called from our main method.</p>

<p>Depending on whether the method returns true or false, you will get an output in your console telling you whether this specific test passed or failed.</p>

<p>This is not necessary, but this way you can easily add many more test cases to this class and still have readable code.</p>

<p>Now, step by step, here is what happens in our little program:</p>

<ol>
    <li>First, we tell our program where it can find the specific WebDriver for Chrome.<br />
        <pre class="break-out"><code class="language-bash">System.setProperty("webdriver.chrome.driver","C:/PATH/TO/chromedriver.exe");</code></pre>
    </li>
    <li>We open the Chrome browser and maximize the browser window.<br />
        <pre class="break-out"><code class="language-bash">webDriver = new ChromeDriver();
webDriver.manage().window().maximize();</code></pre>
</li>
<li>This is where we jump into our submethod and check whether it returns true or false.<br />
    <pre class="break-out"><code class="language-bash">if (testWordpresslogin()) …</code></pre>
</li>
<li>The following part in our submethod might not be intuitive to understand:<br />The <code>try{…}catch{…}</code> blocks. If everything goes as expected, only the code in <code>try{…}</code> will be executed, but if anything goes wrong while executing <code>try{…}</code>, then the execution continuous in <code>catch{}</code>. Whenever you try to locate an element with <code>findElement</code> and the browser is not able to locate this element, it will throw an exception and execute the code in <code>catch{…}</code>. In my example, the test will be marked as "failed" whenever something goes wrong and the <code>catch{}</code> is executed.</li>
<li>In the submethod, we start by navigating to our WordPress admin area and locating the fields for the username and the password by looking for their IDs. Also, we type the given values in these fields.<br />
    <pre class="break-out"><code class="language-bash">webDriver.navigate().to("https://www.YOUR-SITE.org/wp-admin/");
webDriver.findElement(By.id("user_login")).sendKeys("YOUR_USERNAME");
webDriver.findElement(By.id("user_pass")).sendKeys("YOUR_PASSWORD");</code></pre>
<br />
<figure><figcaption>Selenium fills out our login form</figcaption></figure>
</li>
<li>After filling in the login form, we locate the submit button by its ID and click it.<br />
    <pre class="break-out"><code class="language-bash">webDriver.findElement(By.id("wp-submit")).click();</code></pre>
</li>
<li>In order to follow the test visually, I include a 7-second pause here (7000 milliseconds = 7 seconds).<br />
    <pre class="break-out"><code class="language-bash">Thread.sleep(7000);</code></pre>
</li>
<li>If the login is successful, the <code>h1</code> headline of the current page should now be "Dashboard," referring to the WordPress admin area. Because the <code>h1</code> headline should exist only once on every page, I have used the tag name here to locate the element. In most other cases, the tag name is not a good locator because an HTML tag name is rarely unique on a web page. After locating the <code>h1</code>, we extract the text of the element with <code>getText()</code> and check whether it is equal to the string “Dashboard.” If the login is not successful, we would not find “Dashboard” as the current <code>h1</code>. Therefore, I’ve decided to use the <code>h1</code> to check whether the login is successful.<br />
    <pre class="break-out"><code class="language-javascript">if (webDriver.findElement(By.tagName("h1")).getText().equals("Dashboard")) 
    {
        return true;
    } else {
        return false;
    }
</code></pre>
<br />
<figure>)</figcaption></figure>
</li>
<li>If anything has gone wrong in the previous part of the submethod, the program would have jumped directly to the following part. The <code>catch</code> block will print the type of exception that happened to the console and afterwards return <code>false</code> to the main method.<br />
    <pre class="break-out"><code class="language-javascript">catch (final Exception e) {
            System.out.println(e.getClass().toString());
            return false;
        }</code></pre>
</li>
</ol>

<h3 id="adapting-the-test-case">Adapting The Test Case</h3>

<p>This is where it gets interesting if you want to adapt and add test cases of your own. You can see that we always call methods of the <code>webDriver</code> object to do something with the Chrome browser.</p>

<p>First, we maximize the window:</p>

<pre class="break-out"><code class="language-bash">webDriver.manage().window().maximize();</code></pre>

<p>Then, in a separate method, we navigate to our WordPress admin area:</p>

<pre class="break-out"><code class="language-bash">webDriver.navigate().to("https://www.YOUR-SITE.org/wp-admin/");</code></pre>

<p>There are other methods of the <code>webDriver</code> object we can use. Besides the two above, you will probably use this one a lot:</p>

<pre class="break-out"><code class="language-bash">webDriver.findElement(By. …)</code></pre>

<p>The <code>findElement</code> method helps us find different elements in the DOM. There are different options to find elements:</p>

<ul>
<li><code>By.id</code></li>
<li><code>By.cssSelector</code></li>
<li><code>By.className</code></li>
<li><code>By.linkText</code></li>
<li><code>By.name</code></li>
<li><code>By.xpath</code></li>
</ul>

<p>If possible, I recommend using <code>By.id</code> because the ID of an element should always be unique (unlike, for example, the <code>className</code>), and it is usually not affected if the structure of your DOM changes (unlike, say, the <code>xPath</code>).</p>

<p><strong>Note</strong>: <em>You can read more about the different options for locating elements with WebDriver over .</em></p>

<p>As soon as you get ahold of an element using the <code>findElement</code> method, you can call the different available methods of the element. The most common ones are <code>sendKeys</code>, <code>click</code> and <code>getText</code>.</p>

<p>We’re using <code>sendKeys</code> to fill in the login form:</p>

<pre class="break-out"><code class="language-bash">webDriver.findElement(By.id("user_login")).sendKeys("YOUR_USERNAME");</code></pre>

<p>We have used <code>click</code> to submit the login form by clicking on the submit button:</p>

<pre class="break-out"><code class="language-bash">webDriver.findElement(By.id("wp-submit")).click();</code></pre>

<p>And <code>getText</code> has been used to check what text is in the <code>h1</code> after the submit button is clicked:</p>

<pre class="break-out"><code class="language-bash">webDriver.findElement(By.tagName("h1")).getText()</code></pre>

<p><strong>Note</strong>: <em>Be sure to check out  with an element.</em></p>

<h3 id="conclusion">Conclusion</h3>

<p>Ever since I discovered the power of Selenium WebDriver, my life as a web developer has changed. I simply love it. The deeper I dive into the framework, the more possibilities I discover &mdash; running one test simultaneously in Chrome, Internet Explorer and Firefox or even on my smartphone, or taking screenshots automatically of different pages and comparing them. Today, I use Selenium WebDriver not only for testing purposes, but also to . Whenever I see an opportunity to automate my work on the web, I simply copy my initial WebDriver project and adapt it to the next task.</p>

<p>If you think that Selenium WebDriver is for you, I recommend looking at  on several (mobile) devices with Selenium Grid).</p>

<p>I look forward to hearing whether you find WebDriver as useful as I do!</p>




<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(rb, ra, al, il)</span>
</div>


</div>



              </article>
            </body>
          </html>
---------------
<h1 id="#title_1" >2、文章： PWA登陆iOS了，但它还有这些缺陷</h1>
Maximiliano Firtman
[http://www.infoq.com/cn/articles/progressive-web-apps-on-ios-are-here?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/progressive-web-apps-on-ios-are-here?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/progressive-web-apps-on-ios-are-here/zh/smallimage/dow-1523549869649.jpg"/><p>本文概括介绍了最新发布的iOS 11.3对PWA的支持情况，以及PWA应用开发者需要注意的问题。</p> <i>By Maximiliano Firtman</i> <i> Translated by 大愚若智</i>
---------------
<h1 id="#title_2" >3、文章： 深入理解服务型领导力</h1>
Vikram Raghuram
[http://www.infoq.com/cn/articles/nuances-servant-leadership?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/nuances-servant-leadership?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/nuances-servant-leadership/zh/headerimage/GettyImages-850340232-1522948961641.jpg"/><p>服务型领导力是一种哲学观，也是一系列实践，它丰富了个人生活，让组织变得更好，并且创造了一个更加公平和友爱的世界。在一个组织中，每一个团队和个人都需要回答这些问题：我为什么在做这件事？我的角色可以为这里带来什么价值？顺着目标前进可以获得更好的结果。</p> <i>By Vikram Raghuram</i> <i> Translated by 刘嘉洋</i>
---------------
<h1 id="#title_3" >4、文章： Re：如何让你的敏捷开发真正起效</h1>
Beining
[http://www.infoq.com/cn/articles/why-isnt-agile-working?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/why-isnt-agile-working?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/why-isnt-agile-working/zh/smallimage/tb-1523552494711.jpg"/><p>敏捷开发大家都在讲：起不起效冷暖自知。如何让你的敏捷开发真正起效？作者对敏捷失败的常见问题进行了剖析并给出了具体建议。 notes：前几天敏捷开发的新闻的精神续作。所以建议同一人审校。 --- 列表问题已经修复。</p> <i>By Beining</i>
---------------
<h1 id="#title_4" >5、视频演讲： iOS App 内存专项实践：封闭系统下的大自由</h1>
黄闻欣
[http://www.infoq.com/cn/presentations/ios-app-memory-special-practice-the-big-freedom-under-the-closed-system?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/ios-app-memory-special-practice-the-big-freedom-under-the-closed-system?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/presentations/ios-app-memory-special-practice-the-big-freedom-under-the-closed-system/zh/mediumimage/huangwenxin270-1521963754591.jpg"/><p>iOS 作为一个封闭的系统，有自成一格的工具和平台。但是这些工具更像是给开发自测的时候使用的，完全无法打通到研发流程中，也难以配合自动化测试。这里通过 App 内存专项的各个方面如何脱离 Instuments，打通流程并全自动化为例，提供了另外一种思路，利用 hook，私有函数等技术，在封闭的系统中用更自由和轻松的方法测试 iOS App。</p> <i>By 黄闻欣</i>
---------------
<h1 id="#title_5" >6、采访Nicole Forsgren博士：DORA与Google就《DevOps促进状态报告》开展合作</h1>
Helen Beal
[http://www.infoq.com/cn/news/2018/04/DORA-Google-Cloud-New-Research?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/04/DORA-Google-Cloud-New-Research?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>DORA公司和Google Cloud将针对软件开发人员问题合作开展原创性研究，进而发布《DevOps促进状态报告》（The Accelerate State of DevOps Report）。该项研究的目的，是为了给出一些可对改进技术交付团队的资源管理、生产力和质量提供指导的新发现。</p> <i>By Helen Beal</i> <i> Translated by 盖磊</i>
---------------
<h1 id="#title_6" >7、敏捷团队心理安全的培养</h1>
Ben Linders
[http://www.infoq.com/cn/news/2018/04/cultivating-psychological-safety?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/04/cultivating-psychological-safety?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>当我们感觉到压力、威胁或者是不安时，就不太可能充满创造性地思考、协作或解决问题。你可以通过认真倾听，事事留心让人们了解，即使犯错误也没什么关系，这样就可以培养一种安全的文化环境。</p> <i>By Ben Linders</i> <i> Translated by 刘嘉洋</i>
---------------
<h1 id="#title_7" >8、TypeScript 2.8引入条件类型</h1>
Dylan Schiemann
[http://www.infoq.com/cn/news/2018/04/typescript-2-8-conditional-types?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/04/typescript-2-8-conditional-types?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>最新发布的TypeScript 2.8包含了若干主要特性和一些问题修复，其中最为重要的是新增了条件类型，开发人员可以根据其他类型的特征为变量选择适当的类型。</p> <i>By Dylan Schiemann</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_8" >9、Visual Studio 2017 15.7预览版发布</h1>
Jeff Martin
[http://www.infoq.com/cn/news/2018/04/vs2017-15.7-preview2?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/04/vs2017-15.7-preview2?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Visual Studio 2017已经发布一年多了，微软一直持续定期推出更新。第7个预览版也已发布，这一版本继续带来大量的改进。</p> <i>By Jeff Martin</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_9" >10、Hyperledger添加Caliper度量区块链性能</h1>
Kent Weare
[http://www.infoq.com/cn/news/2018/04/Hyperledger-Caliper-Performance?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/04/Hyperledger-Caliper-Performance?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>3月19日，Hyperledger宣布，Caliper已经被技术指导委员会接收为一个Hyperledger项目。Hyperledger Caliper是一个区块链基准测试工具，让项目可以不间断地跟踪不同区块链实现的性能特性。</p> <i>By Kent Weare</i> <i> Translated by 谢丽</i>
---------------