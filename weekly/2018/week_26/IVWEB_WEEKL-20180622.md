## 文章索引
1、 <a href="#1文章-hero-node刘国平dapp如何落地" >文章： Hero Node刘国平：Dapp如何落地？</a><br/>
2、 <a href="#2using-googles-flutter-for-truly-cross-platform-mobile-development" >Using Google’s Flutter For Truly Cross-Platform Mobile Development</a><br/>
3、 <a href="#3wordpress-security-as-a-process" >WordPress Security As A Process</a><br/>
4、 <a href="#4文章-eclipse-collections让java-streams更上一层楼" >文章： Eclipse Collections：让Java Streams更上一层楼</a><br/>
5、 <a href="#5专访肖雨浓netflix是怎样探索落地faas的" >专访肖雨浓：Netflix是怎样探索落地FaaS的？</a><br/>
6、 <a href="#6企业级以太坊联盟发布client规范10" >企业级以太坊联盟发布Client规范1.0</a><br/>
7、 <a href="#7safari浏览器的智能跟踪预防工作原理" >Safari浏览器的智能跟踪预防工作原理</a><br/>
8、 <a href="#8microsoft宣布通过azure-event-grid服务提供对cloudevents的支持" >Microsoft宣布通过Azure Event Grid服务提供对CloudEvents的支持</a><br/>
9、 <a href="#9net-framework-48预览" >.NET Framework 4.8预览</a><br/>
10、 <a href="#10gdpr给网站用户跟踪带来重大影响" >GDPR给网站用户跟踪带来重大影响</a><br/><h1 id="#title_0" >1、文章： Hero Node刘国平：Dapp如何落地？</h1>
金缕春
[http://www.infoq.com/cn/articles/hero-node-how-does-dapp-land?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/hero-node-how-does-dapp-land?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/hero-node-how-does-dapp-land/zh/smallimage/GettyImages-671039130-1512649078720-1529593703479.jpg"/><p>大部分人只关注钱，并不在乎它背后的价值和技术力量。</p> <i>By 金缕春</i>
---------------
<h1 id="#title_1" >2、Using Google’s Flutter For Truly Cross-Platform Mobile Development</h1>
Mike Bluestein
[https://www.smashingmagazine.com/2018/06/google-flutter-mobile-development/](https://www.smashingmagazine.com/2018/06/google-flutter-mobile-development/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/06/google-flutter-mobile-development/" />
              <title>Using Google’s Flutter For Truly Cross-Platform Mobile Development</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>Using Google’s Flutter For Truly Cross-Platform Mobile Development</h1>
                  
                    
                    <address>Mike Bluestein</address>
                  
                  <time datetime="2018-06-21T12:45:08&#43;02:00" class="op-published">2018-06-21T12:45:08+02:00</time>
                  <time datetime="2018-06-21T22:45:45&#43;00:00" class="op-modified">2018-06-21T22:45:45+00:00</time>
                </header>
                

<p>Flutter is an open-source, cross-platform mobile development framework from Google. It allows high-performance, beautiful applications to be built for iOS and Android from a single code base. It is also the development platform for Google&rsquo;s upcoming Fuchsia operating system. Additionally, it is architected in a way that it can be brought to other platforms, via .</p>

<h3 id="why-flutter-was-created-and-why-you-should-use-it">Why Flutter was Created And Why You Should Use It</h3>

<p>Cross-platform toolkits have historically taken one of two approaches:</p>

<ul>
<li>They wrap a web view in a native app and build the application as if it were a website.</li>
<li>They wrap native platform controls and provide some cross-platform abstraction over them.</li>
</ul>

<p>Flutter takes a different approach in an attempt to make mobile development better. It provides a framework application developers work against and an engine with a portable runtime to host applications. The framework builds upon the Skia graphics library, providing widgets that are actually rendered, as opposed to being just wrappers on native controls.</p>

<p>This approach gives the flexibility to build a cross-platform application in a completely custom manner like the web wrapper option provides, but at the same time offering smooth performance. Meanwhile, the rich widget library that comes with Flutter, along with a wealth of open-source widgets, makes it a very feature-rich platform to work with. Put simply, Flutter is the closest thing mobile developers have had for cross-platform development with little to no compromise.</p>



  <aside class="product-panel product-panel__tilted product-panel--book" data-audience="non-subscriber">
    <div class="container product-panel--book__container">
      <div class="panel__description panel__description--book">
    <p>Getting the process <em>just</em> right ain't an easy task. That's why we've set up <strong>'this-is-how-I-work'-sessions</strong> — with smart cookies sharing what works really well for them. A part of the , of course.</p>
      <a href="http://smashed.by/casestudypanelmembership" class="btn btn--green btn--large">
        Explore features&nbsp;→
      </a>
      </div>
      <div class="panel__image panel__image--book">
        <a href="http://smashed.by/casestudypanelmembership" class="books__book__image">
        <div class="books__book__img">
          <img src="https://www.smashingmagazine.com/images/smashing-cat/cat-scubadiving-panel.svg" alt="Smashing TV, with live sessions for professional designers and developers." width="310" height="400">
        </div>
      </a>
      </div>
    </div>
  </aside>




<h3 id="dart">Dart</h3>

<p>Flutter applications are written in Dart, which is a programming language originally developed by Google. Dart is an object-oriented language that supports both ahead-of-time and just-in-time compilation, making it well suited for building native applications, while providing for efficient development workflow with Flutter’s hot reloading. Flutter recently moved to Dart version 2.0 as well.</p>

<p>The Dart language offers many of the features seen in other languages including garbage collection, async-await, strong typing, generics, as well as a .</p>

<p>Dart offers an intersection of features that should be familiar to developers coming from a variety of languages, such as C#, JavaScript, F#, Swift, and Java. Additionally, Dart can compile to Javascript. Combined with Flutter, this allows code to be shared across web and mobile platforms.</p>

<h3 id="historical-timeline-of-events">Historical Timeline Of Events</h3>

<ul>
<li><strong>April 2015</strong><br />
Flutter (originally codenamed Sky) shown at </li>
<li><strong>November 2015</strong><br />
Sky renamed to Flutter</li>
<li><strong>February 2018</strong><br />
Flutter  at Mobile World Congress 2018</li>
<li><strong>April 2018</strong><br />
Flutter </li>
<li><strong>May 2018</strong><br />
Flutter beta 3 announced at Google I/O. Google announces </li>
</ul>

<h3 id="comparison-to-other-development-platforms">Comparison To Other Development Platforms</h3>

<h4 id="apple-android-native">Apple/Android Native</h4>

<p>Native applications offer the least friction in adopting new features. They tend to have user experiences more in tune with the given platform since the applications are built using controls from the platforms vendors themselves (Apple or Google) and often follow design guidelines set out by these vendors. In most cases, native applications will perform better than those built with cross-platform offerings, although the difference can be negligible in many cases depending on the underlying cross-platform technology.</p>

<p>One big advantage native applications have is they can adopt brand new technologies Apple and Google create in beta immediately if desired, without having to wait for any third-party integration. The main disadvantage to building native applications is the lack of code reuse across platforms, which can make development expensive if targeting iOS and Android.</p>

<h4 id="react-native">React Native</h4>

<p>React Native allows native applications to be built using JavaScript. The actual controls the application uses are native platform controls, so the end user gets the feel of a native app. For apps that require customization beyond what React Native&rsquo;s abstraction provides, native development could still be needed. In cases where the amount of customization required is substantial, the benefit of working within React Native&rsquo;s abstraction layer lessens to the point where in some cases developing the app natively would be more beneficial.</p>

<h4 id="xamarin">Xamarin</h4>

<p>When discussing Xamarin, there are two different approaches that need to be evaluated. For their most cross-platform approach, there is Xamarin.Forms. Although the technology is very different to React Native, conceptually it offers a similar approach in that it abstracts native controls. Likewise, it has similar downsides with regard to customization.</p>

<p>Second, there is what many term Xamarin-classic. This approach uses Xamarin&rsquo;s iOS and Android products independently to build platform-specific features, just like when directly using Apple/Android native, only using C# or F# in the Xamarin case. The benefit with Xamarin is that non-platform specific code, things like networking, data access, web services, etc. could be shared.</p>

<p>Unlike these alternatives, Flutter attempts to give developers a more complete cross-platform solution, with code reuse, high-performance, fluid user interfaces, and excellent tooling.</p>

<h3 id="overview-of-a-flutter-app">Overview Of A Flutter App</h3>

<h4 id="creating-an-app">Creating An App</h4>

<p>After , creating an app with Flutter is as simple as either opening a command line and entering <code>flutter create [app_name]</code>, selecting the “Flutter: New Project” command in VS Code, or selecting “Start a new Flutter Project” in Android Studio or IntelliJ.</p>

<p>Regardless of whether you choose to use an IDE or the command line along with your preferred editor, the new Flutter application template gives you a good starting point for an application.</p>

<p>The application brings in the <code>flutter</code>/<code>material.dart</code> package to offer some basic scaffolding for the app, such as a title bar, material icons and theming. It also sets up a stateful widget to demonstrate how to update the user interface when application state changes.</p>











<figure class="article__image break-out">
	
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/180fcd19-9d6e-4083-a3b9-4d2b25577c59/01-introductory-article-on-google-s-flutter.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/180fcd19-9d6e-4083-a3b9-4d2b25577c59/01-introductory-article-on-google-s-flutter.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/180fcd19-9d6e-4083-a3b9-4d2b25577c59/01-introductory-article-on-google-s-flutter.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/180fcd19-9d6e-4083-a3b9-4d2b25577c59/01-introductory-article-on-google-s-flutter.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/180fcd19-9d6e-4083-a3b9-4d2b25577c59/01-introductory-article-on-google-s-flutter.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/180fcd19-9d6e-4083-a3b9-4d2b25577c59/01-introductory-article-on-google-s-flutter.png"
			sizes="100vw"
			alt="New Flutter Application Template"
		/>
	

	
		<figcaption class="op-vertical-bottom">
			The new Flutter application running on iOS and Android. ()
		</figcaption>
	
</figure>


<h4 id="tooling-options">Tooling Options</h4>

<p>Flutter offers incredible flexibility with regard to tooling. Applications can just as easily be developed from the command line along with any editor, as they can be from a supported IDE like VS Code, Android Studio, or IntelliJ. The approach to take depends largely on developer preference.</p>

<p>Android Studio offers the most features, such as a Flutter Inspector to analyze the widgets of a running application and well as monitor application performance. It also offers several refactorings that are convenient when developing a widget hierarchy.</p>

<p>VS Code offers a lighter development experience in that it tends to start faster than Android Studio/IntelliJ. Each IDE offers built-in editing helpers, such as code completion, allowing exploration of various APIs as well as good debugging support.</p>

<p>The command line is also well supported through the <code>flutter</code> command, which makes it easy to create, update and launch an application without any other tooling dependency beyond an editor.</p>











<figure class="article__image break-out">
	
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5fc873ba-ef7c-4185-b2e6-bcaeed7e365f/02-introductory-article-on-google-s-flutter.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5fc873ba-ef7c-4185-b2e6-bcaeed7e365f/02-introductory-article-on-google-s-flutter.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5fc873ba-ef7c-4185-b2e6-bcaeed7e365f/02-introductory-article-on-google-s-flutter.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5fc873ba-ef7c-4185-b2e6-bcaeed7e365f/02-introductory-article-on-google-s-flutter.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5fc873ba-ef7c-4185-b2e6-bcaeed7e365f/02-introductory-article-on-google-s-flutter.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5fc873ba-ef7c-4185-b2e6-bcaeed7e365f/02-introductory-article-on-google-s-flutter.png"
			sizes="100vw"
			alt="Flutter Tooling"
		/>
	

	
		<figcaption class="op-vertical-bottom">
			Flutter tooling supports a variety of enviroments. ()
		</figcaption>
	
</figure>


<h4 id="hot-reloading">Hot Reloading</h4>

<p>Regardless of tooling, Flutter maintains excellent support for hot reloading of an application. This allows a running application to be modified in many cases, maintaining state, without having to stop the app, rebuild and redeploy.</p>

<p>Hot reload dramatically increases development efficiency by allowing quicker iteration. It really makes the platform a pleasure to work with.</p>

<h4 id="testing">Testing</h4>

<p>Flutter includes a <code>WidgetTester</code> utility to interact with widgets from a test. The new application template includes a sample test to demonstrate how to use it when authoring a test, as shown below:</p>

<pre class="break-out"><code class="language-css">// Test included with the new Flutter application template

import 'package:flutter/material.dart';
import 'package:flutter_test/flutter_test.dart';

import 'package:myapp/main.dart';

void main() {
  testWidgets('Counter increments smoke test', (WidgetTester tester) async {
    // Build our app and trigger a frame.
    await tester.pumpWidget(new MyApp());

    // Verify that our counter starts at 0.
    expect(find.text('0'), findsOneWidget);
    expect(find.text('1'), findsNothing);

    // Tap the '+' icon and trigger a frame.
    await tester.tap(find.byIcon(Icons.add));
    await tester.pump();

    // Verify that our counter has incremented.
    expect(find.text('0'), findsNothing);
    expect(find.text('1'), findsOneWidget);
  });
}

</code></pre>

<h4 id="using-packages-and-plugins">Using Packages And Plugins</h4>

<p>Flutter is just beginning, but there is already a rich developer ecosystem:  are already available for developers.</p>

<p>To add a package or plugin, simply include the dependency in the <em>pubspec.yaml</em> file at the application&rsquo;s root directory. Then run <code>flutter packages get</code> either from the command line or through the IDE, and Flutter&rsquo;s tooling will bring in all the required dependencies.</p>

<p>For example, to use the popular image picker plugin for Flutter, the <em>pubspec.yaml</em> need only list it as a dependency like so:</p>

<pre><code class="language-css">dependencies:
  image_picker: "^0.4.1" 
</code></pre>

<p>Then running <code>flutter packages get</code> brings in everything you need to make use of it, after which it can be imported and used in Dart:</p>

<pre><code class="language-css">import 'package:image_picker/image_picker.dart';
</code></pre>

<h3 id="widgets">Widgets</h3>

<p>Everything in Flutter is a widget. This includes user interface elements, such as <code>ListView</code>, <code>TextBox</code>, and <code>Image</code>, as well as other portions of the framework, including layout, animation, gesture recognition, and themes, to name just a few.</p>

<p>By having everything be a widget, the entire application, which incidentally is also a widget, can be represented within the widget hierarchy. Having an architecture where everything is a widget makes it clear where certain attributes and behavior applied to a portion of an app are coming from. This is different from most other application frameworks, which associate properties and behavior inconsistently, sometimes attaching them from other components in a hierarchy and other times on the control itself.</p>

<h4 id="simple-ui-widget-example">Simple UI Widget Example</h4>

<p>The entry point to a Flutter application is the main function. To put a widget for a user interface element on the screen, in <code>main()</code> call <code>runApp()</code> and pass it the widget that will serve as the root of the widget hierarchy.</p>

<pre><code class="language-css">import 'package:flutter/material.dart';

void main() {
  runApp(
    Container(color: Colors.lightBlue)
  );
}
</code></pre>

<p>This results a light blue <code>Container</code> widget that fills the screen:</p>











<figure >
	
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/100954a2-2302-44fd-921b-b372c76884e7/03-introductory-article-on-google-s-flutter.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/100954a2-2302-44fd-921b-b372c76884e7/03-introductory-article-on-google-s-flutter.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/100954a2-2302-44fd-921b-b372c76884e7/03-introductory-article-on-google-s-flutter.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/100954a2-2302-44fd-921b-b372c76884e7/03-introductory-article-on-google-s-flutter.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/100954a2-2302-44fd-921b-b372c76884e7/03-introductory-article-on-google-s-flutter.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/100954a2-2302-44fd-921b-b372c76884e7/03-introductory-article-on-google-s-flutter.png"
			sizes="70vw"
			alt="Minimal Flutter Application"
		/>
	

	
		<figcaption class="op-vertical-bottom">
			Minimal Flutter applcation with a single container ()
		</figcaption>
	
</figure>


<h4 id="stateless-vs-stateful-widgets">Stateless vs. Stateful Widgets</h4>

<p>Widgets come in two flavors: stateless and stateful. Stateless widgets don&rsquo;t change their content after they are created and initialized, whereas stateful widgets maintain some state that can change while running the application, e.g. in response to user interaction.</p>

<p>In this example, a <code>FlatButton</code> widget and <code>Text</code> widget are drawn to the screen. The <code>Text</code> widget starts out with some default <code>String</code> for its state. Pressing the button results in a state change that will cause the <code>Text</code> widget to be updated, displaying a new <code>String</code>.</p>

<p>To encapsulate a widget create a class that derives from either <code>StatelessWidget</code> or <code>StatefulWidget</code>. For example, the light blue <code>Container</code> could be written as follows:</p>

<pre><code class="language-css">class MyWidget extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Container(color: Colors.lightBlue);
  }
}
</code></pre>

<p>Flutter will call the widget&rsquo;s build method when it is inserted into the widget tree so this portion of the UI can be rendered.</p>

<p>For a stateful widget, derive from <code>StatefulWidget</code>:</p>

<pre><code class="language-css">class MyStatefulWidget extends StatefulWidget {

  MyStatefulWidget();

  @override
  State<StatefulWidget> createState() {
    return MyWidgetState();
  }
}
</code></pre>

<p>Stateful widgets return a <code>State</code> class that is responsible for building the widget tree for a given state. When the state changes, the associated portion of the widget tree is rebuilt.</p>

<p>In the following code, the <code>State</code> class updates a <code>String</code> when a button is clicked:</p>

<pre><code class="language-css">class MyWidgetState extends State<MyStatefulWidget> {
  String text = "some text";

  @override
  Widget build(BuildContext context) {
    return Container(
      color: Colors.lightBlue,
      child: Padding(
        padding: const EdgeInsets.all(50.0),
        child: Directionality(
          textDirection: TextDirection.ltr,
          child: Column(
            children: [
              FlatButton(
                child: Text('Set State'),
                onPressed: () {
                  setState(() {
                    text = "some new text";
                  });
                },
              ),
               Text(
                text, 
                style: TextStyle(fontSize: 20.0)),
            ],
          )
        )
      )
    );
  }
}
</code></pre>

<p>The state is updated in a function that is passed to <code>setState()</code>. When <code>setState()</code> is called, this function can set any internal state, such as the string in this example. Then, the <code>build</code> method will be called, updating the stateful widget&rsquo;s tree.</p>











<figure >
	
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/75e25ffb-d03c-4c99-87d8-b2257f7f94d0/04-introductory-article-on-google-s-flutter.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/75e25ffb-d03c-4c99-87d8-b2257f7f94d0/04-introductory-article-on-google-s-flutter.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/75e25ffb-d03c-4c99-87d8-b2257f7f94d0/04-introductory-article-on-google-s-flutter.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/75e25ffb-d03c-4c99-87d8-b2257f7f94d0/04-introductory-article-on-google-s-flutter.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/75e25ffb-d03c-4c99-87d8-b2257f7f94d0/04-introductory-article-on-google-s-flutter.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/75e25ffb-d03c-4c99-87d8-b2257f7f94d0/04-introductory-article-on-google-s-flutter.png"
			sizes="100vw"
			alt="State Change"
		/>
	

	
		<figcaption class="op-vertical-bottom">
			Handling a state change from user interaction ()
		</figcaption>
	
</figure>


<p>Also note the use of the <code>Directionality</code> widget to set the text direction for any widgets in its subtree that require it, such as the <code>Text</code> widgets. The examples here are building code from scratch, so <code>Directionality</code> is needed somewhere up the widget hierarchy. However, using the <code>MaterialApp</code> widget, such as with the default application template, sets up the text direction implicitly.</p>

<h4 id="layout">Layout</h4>

<p>The <code>runApp</code> function inflates the widget to fill the screen by default. To control the widget layout, Flutter offers a variety of layout widgets. There are widgets to perform layouts that align child widgets vertically or horizontally, expand widgets to fill a particular space, limit widgets to a certain area, center them on the screen, and allow widgets to overlap each other.</p>

<p>Two commonly used widgets are <code>Row</code> and <code>Column</code>. These widgets perform layouts to display their child widgets horizontally (Row) or vertically (Column).</p>


  <div id="sponsors-article" data-impression="true" class="c-promo-box c-promo-box--ad sponsors hidden" data-audience="non-subscriber" data-remove="true"></div>



<p>Using these layout widgets simply involves wrapping them around a list of child widgets. The <code>mainAxisAlignment</code> controls how the widgets are positioned along the layout axis, either centered, at the start, end, or with various spacing options.</p>

<p>The following code shows how to align several child widgets in a <code>Row</code> or <code>Column</code>:</p>

<pre><code class="language-css">class MyStatelessWidget extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Row( //change to Column for vertical layout
      mainAxisAlignment: MainAxisAlignment.center,
      children: [
        Icon(Icons.android, size: 30.0),
        Icon(Icons.pets, size: 10.0),
        Icon(Icons.stars, size: 75.0),
        Icon(Icons.rowing, size: 25.0),
      ],
    );
  }
}
</code></pre>











<figure >
	
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/45cc7f1d-16ab-4f64-aebb-0258eda5b9c6/05-introductory-article-on-google-s-flutter.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/45cc7f1d-16ab-4f64-aebb-0258eda5b9c6/05-introductory-article-on-google-s-flutter.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/45cc7f1d-16ab-4f64-aebb-0258eda5b9c6/05-introductory-article-on-google-s-flutter.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/45cc7f1d-16ab-4f64-aebb-0258eda5b9c6/05-introductory-article-on-google-s-flutter.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/45cc7f1d-16ab-4f64-aebb-0258eda5b9c6/05-introductory-article-on-google-s-flutter.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/45cc7f1d-16ab-4f64-aebb-0258eda5b9c6/05-introductory-article-on-google-s-flutter.png"
			sizes="70vw"
			alt="Row Widget"
		/>
	

	
		<figcaption class="op-vertical-bottom">
			Row widget showing horizontal layout ()
		</figcaption>
	
</figure>


<h4 id="responding-to-touch">Responding To Touch</h4>

<p>Touch interaction is handled with gestures, which are encapsulated in the <code>GestureDetector</code> class. Since it is also a widget, adding gesture recognition is as easy as wrapping child widgets in a <code>GestureDetector</code>.</p>

<p>For example, to add touch handling to an <code>Icon</code>, make it a child of a <code>GestureDetector</code> and set the detector&rsquo;s handlers for the desired gestures to capture.</p>

<pre class="break-out"><code class="language-css">class MyStatelessWidget extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return GestureDetector(
      onTap: () => print('you tapped the star'),
      onDoubleTap: () => print('you double tapped the star'),
      onLongPress: () => print('you long pressed the star'),
      child: Icon(Icons.stars, size: 200.0),
    );
  }
}
</code></pre>

<p>In this case, when a tap, double-tap, or long-press is performed on the icon, the  associated text is printed:</p>

<pre class="break-out"><code class="language-css">🔥  To hot reload your app on the fly, press "r". To restart the app entirely, press "R".
An Observatory debugger and profiler on iPhone X is available at: http://127.0.0.1:8100/
For a more detailed help message, press "h". To quit, press "q".
flutter: you tapped the star
flutter: you double tapped the star
flutter: you long pressed the star
</code></pre>

<p>In addition to simple tap gestures, there a wealth of recognizers, for everything from panning and scaling, to dragging. These make it very easy to build interactive applications.</p>

<h4 id="painting">Painting</h4>

<p>Flutter also offers a variety of widgets to paint with including ones that modify opacity, set clipping paths, and apply decorations. It even supports custom painting through the <code>CustomPaint</code> widget, and the associated <code>CustomPainter</code> and <code>Canvas</code> classes.</p>

<p>One example of a painting widget is the <code>DecoratedBox</code>, which can paint a <code>BoxDecoration</code> to the screen. The following example shows how to use this to fill the screen with a gradient fill:</p>

<pre class="break-out"><code class="language-css">class MyStatelessWidget extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return new DecoratedBox(
      child: Icon(Icons.stars, size: 200.0),
      decoration: new BoxDecoration(
        gradient: LinearGradient(
          begin: Alignment.topCenter,
          end: Alignment.bottomCenter,
          colors: [Colors.red, Colors.blue, Colors.green],
          tileMode: TileMode.mirror
        ),
      ),
    );
  }
}
</code></pre>











<figure >
	
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/030bf673-b51a-4d80-991e-f15cad36f18b/06-introductory-article-on-google-s-flutter.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/030bf673-b51a-4d80-991e-f15cad36f18b/06-introductory-article-on-google-s-flutter.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/030bf673-b51a-4d80-991e-f15cad36f18b/06-introductory-article-on-google-s-flutter.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/030bf673-b51a-4d80-991e-f15cad36f18b/06-introductory-article-on-google-s-flutter.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/030bf673-b51a-4d80-991e-f15cad36f18b/06-introductory-article-on-google-s-flutter.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/030bf673-b51a-4d80-991e-f15cad36f18b/06-introductory-article-on-google-s-flutter.png"
			sizes="70vw"
			alt="Gradient Background"
		/>
	

	
		<figcaption class="op-vertical-bottom">
			Painting a gradient background ()
		</figcaption>
	
</figure>


<h4 id="animation">Animation</h4>

<p>Flutter includes an <code>AnimationController</code> class that controls animation playback over time, including starting and stopping an animation, as well as varying the values to an animation. Additionally, there is an <code>AnimatedBuilder</code> widget that allows constructing an animation in conjunction with an <code>AnimationController</code>.</p>

<p>Any widget, such as the decorated star shown earlier, can have its properties animated. For example, refactoring the code to a <code>StatefulWidget</code>, since animating is a state change, and passing an <code>AnimationController</code> to the <code>State</code> class allows the animated value to be used as the widget is built.</p>

<pre class="break-out"><code class="language-css">class StarWidget extends StatefulWidget {
  @override
  State<StatefulWidget> createState() {
    return StarState();
  }
}

class StarState extends State<StarWidget> with SingleTickerProviderStateMixin {
  AnimationController _ac;
  final double _starSize = 300.0;
  
   @override
  void initState() {
    super.initState();

    _ac = new AnimationController(
      duration: Duration(milliseconds: 750),
      vsync: this,
    );
    _ac.forward();
  }

  @override
  Widget build(BuildContext context) {

    return new AnimatedBuilder(
      animation: _ac,
      builder: (BuildContext context, Widget child) {
        return DecoratedBox(
          child: Icon(Icons.stars, size: _ac.value * _starSize),
          decoration: BoxDecoration(
            gradient: LinearGradient(
              begin: Alignment.topCenter,
              end: Alignment.bottomCenter,
              colors: [Colors.red, Colors.blue, Colors.green],
              tileMode: TileMode.mirror
            ),
          ),
        );
      }
   );
  }
}
</code></pre>

<p>In this case, the value is used to vary the size of the widget. The <code>builder</code> function is called whenever the animated value changes, causing the size of the star to vary over 750 ms, creating a scale in effect:</p>

<figure><figcaption>Icon Size Animation</figcaption></figure>

<h3 id="using-native-features">Using Native Features</h3>

<h4 id="platform-channels">Platform Channels</h4>

<p>In order to provide access to native platform APIs on Android and iOS, a Flutter application can use platform channels. These allow Flutter Dart code to send messages to the hosting iOS or Android application. Many of the open-source plugins that are available are built using messaging over platform channels. To learn how to work with platform channels, the  includes a good document that demonstrates accessing native battery APIs.</p>

<h3 id="conclusion">Conclusion</h3>

<p>Even in beta, Flutter offers a great solution for building cross-platform applications. With its excellent tooling and hot reloading, it brings a very pleasant development experience. The wealth of open-source packages and excellent documentation make it easy to get started with. Looking forward, Flutter developers will be able to target Fuchsia in addition to iOS and Android. Considering the extensibility of the engine&rsquo;s architecture, it wouldn&rsquo;t surprise me to see Flutter land on a variety of other platforms as well. With a growing community, it&rsquo;s a great time to jump in.</p>

<h3 id="next-steps">Next Steps</h3>

<ul>
<li></li>
<li></li>
<li></li>
<li></li>
<li></li>
</ul>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(lf, ra, yk, il)</span>
</div>


              </article>
            </body>
          </html>
---------------
<h1 id="#title_2" >3、WordPress Security As A Process</h1>
Luc Princen
[https://www.smashingmagazine.com/2018/06/wordpress-security-as-a-process/](https://www.smashingmagazine.com/2018/06/wordpress-security-as-a-process/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/06/wordpress-security-as-a-process/" />
              <title>WordPress Security As A Process</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>WordPress Security As A Process</h1>
                  
                    
                    <address>Luc Princen</address>
                  
                  <time datetime="2018-06-21T12:30:13&#43;02:00" class="op-published">2018-06-21T12:30:13+02:00</time>
                  <time datetime="2018-06-21T22:45:45&#43;00:00" class="op-modified">2018-06-21T22:45:45+00:00</time>
                </header>
                <p>(<em>This article is kindly sponsored by Sucuri</em>.) WordPress security doesn’t have a good reputation. More than 70% of all WordPress sites carry some kind of vulnerability according to research done on . If you develop WordPress themes or plugins &mdash; or use WordPress for your websites &mdash; that number should scare you.</p>

<p>There’s a lot you can do to make sure you’re not part of the 70%, but it takes more work than just installing a plugin or escaping a string. A lot of advice in this article comes from  and years of personal experience.</p>

<h3>Is WordPress Insecure?</h3>

<p>WordPress has the largest market share among content management systems and a 30% market share among the most popular 10 million sites on the web. That kind of success makes it a big target for hacks. WordPress isn’t less secure than other content management systems &mdash; it’s just more successful.</p>

<p>Vulnerabilities in WordPress core are responsible for less than 10% of all WordPress hacks. Most of those are from out-of-date WordPress installs. The amount of hacks that happen on actual security holes in up-to-date versions (also known as zero-day exploits) in WordPress core account for a tiny percentage of all hacks.</p>

<p>The rest of the infected sites were caused by plugins, themes, hosting, and users. And you, as a WordPress website developer, have control over all of those. If this seems like a big hassle to you, then I can recommend . Otherwise, let’s find out how to deal with WordPress security ourselves!
</p>

<h3>Who’s Attacking You And Why?</h3>

<p>Let’s bust a myth first: A small WordPress website is still an attractive target for hackers. Attacks on a personal basis are very rare. Most hacked WordPress websites are compromised automatically by either a bot or a botnet.</p>

<p>Bots are computer programs that constantly search for websites to hack. They don’t care who you are; they just look for a weakness in your defences. A botnet combines the computing power of many bots to tackle bigger tasks.</p>

<p>Hackers are primarily looking for a way into your server so that they can use your server’s computing power and turn it loose on some other goal or target. Hackers want your server for the following reasons.</p>

<h4>Sending Spam</h4>

<p>Spam accounts for about 60% of all email, and it has to be sent from somewhere. Many hackers want to gain entry to your server through a faulty plugin or an ancient version of WordPress core so that they can turn your server into a spamming machine.</p>

<h4>Attacking Other Websites</h4>

<p>Distributed denial-of-service attacks use many computers to flood a website with so much traffic that they can’t keep up. These attacks are very difficult to mitigate, especially when they are done right. Hackers who break into your server can add it to a pool of servers to attack websites.</p>

<h4>Stealing Resources</h4>

<p>Mining cryptocurrency is very popular now, but it takes a lot of computing power. Hackers who don’t want to spend a lot of money on a server farm will break into unprotected WordPress websites and gain access to servers or to your websites’ visitors and steal computing power.</p>

<h4>Bumping SEO Scores</h4>

<p>A particularly popular hack for WordPress is to gain access to its database and add a bunch of (hidden) text underneath each post, linking to another website. It’s a really quick way to bump one’s SEO score, although Google is getting more vigilant about this behavior, and blacklistings are increasing.<p>

<h4>Stealing Data</h4>

<p>Data is valuable, especially when it’s linked to user profiles and e-commerce information. Getting this data and selling it can make an attacker a handsome profit.</p>

<h3>Why Does Security Matter?</h3>

<p>Apart from not giving criminals the satisfaction, there are plenty of reasons why your website should be secure by default. Having cleaned and dealt with plenty of WordPress hacks myself, I can surely say that they never occur at a convenient time. Cleaning up can take hours and will cost either you or your client money.</p>

<p>To get a hacked WordPress website up and running again, you’ll need to remove and replace every bit of third-party code (including WordPress core); comb through your own code line by line and all other folders on the server to make sure they are still clean; check whether unauthorized users have gained access; and replace all passwords in WordPress, on your server and on your database.</p>

<p>Plenty of services can clean up a WordPress website for you, but prevention is so much better in the long run.</p>

<p>Apart from the cost of cleaning up, hacks can also cost you a lot in missed sales or leads. Hacks move you lower in search rankings, resulting in fewer visitors and fewer conversions.</p>

<p>More than the financial cost, getting hacked hurts your reputation. Visitors come to your website because they trust you. Getting hacked damages your reputation, and that takes a long time to repair.</p>

<p>There’s also a real possibility of legal issues, especially if you have customers in the EU, where  will go into effect in the summer of 2018. That new legislation includes a hefty fine for data breaches that aren’t handled properly.</p>

<p>Money, reputation and legal problems: Bad security can cost you a lot. Investing some time in getting your website, code and team set up with a mindset of security will definitely pay off.</p>

<p>Let’s find out how we can prevent all of this nastiness.</p>

<h3>The CIA Triad</h3>

<p>The CIA triad is a basic framework for every digital security project. It stands for confidentiality, integrity and availability. CIA is a set of rules that limits information access to the right parties, makes sure the information is trustworthy and accurate, and guarantees reliable access to that information.</p>

<p>For WordPress, the CIA framework boils down to the following.</p>

<h4>Confidentiality</h4>

<p>Make sure logged-in users have the right roles assigned and that their capabilities are kept in check. Only give users the minimum access they need, and make sure that administrator information doesn’t leak out to the wrong party. You can do so by hardening WordPress’ admin area and being careful with usernames and credentials.</p>

<h4>Integrity</h4>

<p>Show accurate information on your website, and make sure that user interactions on your website happen correctly.</p>

<p>When accepting requests on both the front and back end, always check that the intent matches the actual action. When data is posted, always filter the data in your code for malicious content by using sanitization and escapes. Make sure spam gets removed by using a spam protection service such as Akismet.</p>

<h4>Availability</h4>

<p>Mak sure your WordPress, plugins and themes are up to date and hosted on a reliable (preferably managed) WordPress host. Daily automated backups also help to ensure that your website stays available to the public.</p>

<p>All three elements lean on each other for support. Code integrity will not work on its own if a user’s confidential password is easily stolen or guessed. All aspects are important to a solid and secure platform.</p>

<p>Security is a lot of hard work. Apart from the work that can be done in code, there’s a huge human element to this framework. Security is a constant process; it can’t be solved by a single plugin.</p>

<h3>Part 1: Integrity &mdash; Trust Nothing</h3>

<p>Verify the intent of user actions and the integrity of the data you’re handling. Throw your inner hippie out the door. Nothing can be trusted online, so double-check everything you do for possible malicious intent.</p>

<h4>Data Validation and Sanitization</h4>

<p>WordPress is excellent at handling data. It makes sure that every interaction is validated and that every bit of data is sanitized, but that’s only in WordPress core. If you’re building your own plugin or theme or even just checking a piece of third-party code, knowing how to do this is essential.</p>

<pre class="break-out"><code class="language-php">//Cast our variable to a string, and sanitize it.
update_post_meta( $post->ID,  ‘some-meta’,  sanitize_text_field( (string)$_POST[‘some-meta’] ) );

//Make sure our variable is an absolute integer.
update_post_meta( $post->ID, ‘some-int’, absint( $_POST[‘int’] ) );
</code></pre>

<p>In this example, we’ve added two pieces of data to a WordPress post using .</p>

<p>We’ve also added an integer to that post and used  to make sure this is an absolute (and non-negative) integer.</p>

<p>Using core WordPress functions such as <code>update_post_meta</code> is a better idea than using the WordPress database directly. This is because WordPress checks everything that needs to be stored in the database for so-called SQL injections. A SQL injection attack runs malicious SQL code through the forms on your website. This code manipulates the database to, for instance, destroy everything, leak user data or create false administrator accounts.</p>

<p>If you ever need to work with a custom table or perform a complicated query in WordPress, use the native  class, and use the <code>prepare</code> function on all your queries to prevent SQL injection attacks:</p>

<pre class="break-out"><code class="language-php">$tableName = $wpdb->prefix . “my_table”;
$sql = $wpdb->prepare( “SELECT * FROM %s”, $tableName );
$results = $wpdb->get_results( $sql );
</code></pre>

<p> goes through every variable to make sure there’s no chance of a SQL injection attack.</p>

<h4>Escaping</h4>

<p>Escaping output is just as important as sanitizing input. Validating data before you save it is important, but you can’t be 100% sure it’s still safe. Trust nothing. WordPress uses a lot of filters to enable plugins and themes to change data on the fly, so there’s a good chance that your data will get parsed through other plugins as well. Escaping data before adding it to your theme or plugin is a smart thing to do.</p>

<p>Escaping is mainly meant to prevent  (XSS) attacks. XSS attacks inject malicious code into the front end of your website. An added bonus of escaping data is that you can be sure that your markup is still valid afterwards.</p>

<p>WordPress has . Here’s a simple example:</p>

<pre class="break-out"><code class="language-php">&lt;a href=“&lt;?php echo esc_url( $url );?>” title=“&lt;?php echo esc_attr( $title );?>”>&lt;?php echo esc_html( $title );?>&lt;/a>
</code></pre>

<p>Escape as late as possible. This ensures that you have the final say over your data.</p>

<h4>Securing Requests</h4>

<p>WordPress admin requests are already pretty secure if you have SSL enabled and if you have a decent host, but some vulnerabilities still exist. You need to check a user’s intent and validate that the incoming request is something that was done by the actual logged-in user.</p>

<p>WordPress . A nonce (or “number used only once”) isn’t really an accurate description of this API in WordPress. It doesn’t only use numbers, and it is much more like a cross-site request forgery (CSRF) token that you’ll find in every modern web framework. These tokens make sure hackers can’t repeat requests. It’s a lot more than just a nonce, but WordPress likes backwards-compatibility, so the name stuck.</p>

<p>Nonces are sent along with every vulnerable request that a user makes. They’re attached to URLs and forms, and they always need to be checked on the receiving end before performing the request. You can add a nonce to a form or a URL. Here’s an example used in a form:</p>

<pre><code class="language-php">&lt;form method= “post”&gt;
&lt;!-- Add a nonce field: --&gt;
&lt;?php wp_nonce_field( ‘post_custom_form’ );?&gt;

&lt;!-- other fields: →
...
&lt;/form&gt;
</code></pre>

<p>In this case, we’re just using the simple helper function <code>wp_nonce_field()</code>, which generates two hidden fields for us that will look like this:</p>

<pre class="break-out"><code class="language-php">&lt;input type="hidden" id="_wpnonce" name="_wpnonce" value="e558d2674e" />

&lt;input type="hidden" name="_wp_http_referer" value="/wp-admin/post.php?post=2&action=edit" />
</code></pre>

<p>The first field checks intent by using a generated code with the <code>'post_custom_form'</code> string that we’ve passed to the function. The second field adds a referrer to validate whether the request was made from within the WordPress installation.</p>

<p>Before processing your task on the other end of the form or URL, you would check the nonce and its validity with <code>wp_verify_nonce</code>:</p>

<pre class="break-out"><code class="language-php">if( wp_verify_nonce( $_REQUEST[‘_wpnonce’], ‘post_custom_form’ ) == false ){
    wp_die( “Nonce isn\’t valid” );
}
</code></pre>

<p>Here, we’re checking the nonce with our action name, and if it doesn’t match, we stop processing the form.</p>

<h4>Third-Party Code</h4>

<p>Third-party plugins and themes are a hotbed for hacks. They’re also the toughest nut to crack when ensuring the security of your website.</p>

<p><strong>Most WordPress hacks are caused by plugins, themes, and out-of-date copies of WordPress</strong>. No piece of software is 100% secure, but a lot of plugins and themes out there either haven’t been updated in a while by their developers or weren’t secure to begin with.</p>

<p>Less code means less to hack. So, before installing yet another plugin, ask yourself whether you really need it. Is there another way to solve this problem?</p>

<p>If you’re sure you need a plugin or theme, then judge it carefully. Look at the rating, the “last updated” date and the required PHP version when browsing through WordPress’ plugin directory. If you’ve found what you’re looking for and everything seems to work, search for any mentions of it on a trusted security blog, such as Sucuri or WordFence.</p>

<p>Another option is to scan the code and make sure it contains proper nonces, sanitation and escaping; these are usually signs of well-written and secure code. You don’t have to know PHP or do a complete code review. A simple and quick way to verify proper use of WordPress security functions is to search the plugin’s code for these strings:</p>

<ul>
<li><code>esc_attr</code></li>
<li><code>esc_html</code></li>
<li><code>wp_nonce_field</code></li>
<li><code>wp_nonce_url</code></li>
<li><code>sanitize_text_field</code></li>
<li><code>$wpdb->prepare</code></li>
</ul>

<p>A plugin could still be secure if it doesn’t include all of these strings, but if none or a low number of these strings are found, that is a red flag. If you do find a vulnerability, please share it with the creator in private, and allow them time to fix it.</p>

<p>Keeping track of vulnerabilities in the WordPress plugin space is getting easier with initiatives such as .</p>

<p><strong>Note:</strong> Some themes out there bundle versions of plugins with their code. This is a symptom of WordPress not having great out-of-the-box dependency management, but it’s also a sign of a very poorly written theme. Always avoid these themes because they include code bases that can’t be updated.</p>

<p>Themes and plugins rarely contain code written by only one developer. <strong>Composer and NPM</strong> have made it so much easier to depend on other libraries that it’s become a popular attack vector. If you’re downloading a cut-and-dry WordPress theme or plugin, this really isn’t a concern, but if you’re working with tools that use Composer or NPM, then it doesn’t hurt to check their dependencies. You can check Composer dependencies with a free command-line interface (CLI) tool by  (which you can use for free but which also has premium options) enables you to check every dependency in your project.</p>

<h3>Part 2: Availability: Keep It Simple</h3>

<p>Your main goal is to keep your website online without interruptions. Even with top-notch security, you can still get in trouble. When that happens, a great backup will save you a big headache.</p>

<h4>Updates</h4>

<p>Open-source can’t exist without updates. Most attacks on WordPress websites happen on outdated versions of either the core software or plugins. Security updates to WordPress’ core are now dealt with automatically (unless you’ve disabled this, you monster!), but security updates in plugins are a different story.</p>

<p>Updating is normally safe with popular, trusted plugins, but all plugins should be tested before they go live on your website. Tools such as WP CLI make updating everything much easier. WordPress lead developer Mark Jaquith had an excellent blog  automatically yet gradually, so that you can filter out possible errors.</p>

<h4>Users, Roles and Capabilities</h4>

<p>“Availability” in the CIA triad has to do with getting information in the right hands. Our main priority with this is limiting the capabilities of your back-end users. Don’t give everyone an admin account.</p>

<p>The admin account in WordPress is unusually powerful. There’s even an option in vanilla WordPress to alter your complete code base from within the WordPress admin account. (If this is new to you and you haven’t disabled this, .)</p>

<p>The roles and capabilities system in WordPress is powerful and is very easy to alter in code. I create a lot of new roles when working with WordPress. The main benefit of this is that you get full control over which parts of the system various users get to access, but another huge benefit is that it prevents third-party code from altering the standard capabilities of WordPress core.</p>

<h4>Email</h4>

<p>WordPress usually handles email via the server it’s on, but this makes all of your email completely dependent on the server it’s running on. Prevent your emails from getting intercepted and seen as spam by using an SMTP service. A lot of plugin options are available to make sure that all of your mail is sent over a secure SMTP connection.</p>

<p>You will, however, need access to the domain name’s DNS settings to add a Sender Policy Framework (SPF) record. All good SMTP services will provide the exact record that needs to be added. An SPF record ensures that your SMTP service is authorized by the domain to send email in its name.</p>

<h4>Monitoring</h4>

<p>Monitoring your website online is a 24/7 task that can be fully automated. In the case of WordPress, we’re interested in uptime and file integrity.</p>

<p>Monitoring <strong>uptime</strong> is usually something a good host will do for you. Tools such as Uptime Robot add even more security. Your first 50 websites are completely free.</p>

<p>Regarding <strong>file integrity</strong>, if a hacker gains access to your server they can change your code.</p>

<p>In this case, plugins are the answer to your problem. Sucuri has a great auditing plugin. It checks all files in your installation against a vast database of known malicious code. It also checks whether WordPress core is still 100% WordPress core, and it gives you a heads up if there’s been a breach, so that you can fix it as soon as possible.</p>

<h4>Backups</h4>

<p>The ultimate fail-safe of every security process is automated backups. Most good hosts will do this for you, but there are other good options if your host doesn’t offer backups. Automattic makes one named  back up to a Dropbox account or an Amazon S3 bucket.</p>

<p>Most of the reliable services in the WordPress backup space are either premium services or premium plugins. Depending on whether you need to fully control your data, you might prefer a plugin that comes with a cloud host, instead of a service. Either one is worth every penny, though.</p>

<h4>Hosting</h4>

<p>WordPress isn’t the only piece of software running on your server. Plenty of attack vectors are open when you’re on crappy hosting. In fact, bad hosting is the main reason why WordPress still supports outdated versions of PHP. At time of writing, WordPress’ own statistics page reports that 32.5% of all WordPress installations are running on PHP versions that do not receive security updates anymore.</p>











<figure class="article__image break-out">
	
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/969f2505-9358-48cf-a617-2f487a4318b9/wordpress-security-as-a-proces.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/969f2505-9358-48cf-a617-2f487a4318b9/wordpress-security-as-a-proces.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/969f2505-9358-48cf-a617-2f487a4318b9/wordpress-security-as-a-proces.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/969f2505-9358-48cf-a617-2f487a4318b9/wordpress-security-as-a-proces.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/969f2505-9358-48cf-a617-2f487a4318b9/wordpress-security-as-a-proces.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/969f2505-9358-48cf-a617-2f487a4318b9/wordpress-security-as-a-proces.png"
			sizes="100vw"
			alt=""
		/>
	

	
		<figcaption class="op-vertical-bottom">
			PHP versions in WordPress as of 10 May 2018. ()
		</figcaption>
	
</figure>


<p>Note the almost 60% of installations running on PHP 5.6 and 7.0, which will receive security patches only until the end of this year.</p>

<p>Hosting is important not only for keeping your server’s software up to date, though. A good host will offer many more services, such as automated daily backups, automated updates, file-integrity monitoring and email security. There’s a big difference between managed WordPress hosts and hosts that give you an online folder with database access.</p>

<p>The best advice is to find a decent managed WordPress host. They cost a little more, but they provide a great backbone for your WordPress website.</p>

<h3>Part 3: Confidentiality</h3>

<p>If you’ve made sure that your code base is as secure as it can be and you’re on a great WordPress host, surrounded by malware scanners and backups, then you’re still going to experience security problems, because people are the worst… at Internet security.</p>

<p>Confidentiality is about educating yourself, your client and the users of the website.</p>

<h4>Confidential Data</h4>

<p>You might not know it, but your plugins and themes are probably showing valuable confidential data. If, for instance, you have <code>WP_DEBUG</code> set to <code>true</code>, then you’re showing every hacker your website’s root path on the server. Debugging data should have no place in your production website.</p>

<p>Another valuable data source are comments and author pages. These are filled with usernames and even email addresses. A hacker could use these in combination with a weak password to get into your website. Be wary of what you show the outside world.</p>

<p>Also, double-check that you’ve put <code>wp-config.php</code> in your <code>.gitignore</code>.</p>

<h4>Don’t Code Alone</h4>

<p>A way to prevent a lot of mistakes from sneaking into your code base is to practice pair programming. If you’re by yourself, this a lot harder, but many online communities are available that are willing to do quick code audits. WordPress for instance, uses Slack to communicate everything about the development of its platform. You will find a lot of people on there who are willing to help. Slower but better alternatives are the WordPress forums, StackOverflow and GitHub Issues, where your questions (and their answers!) are saved so that other people can benefit from them.</p>

<p>Asking for input can be tough, but people love showing their expertise, and WordPress in general has a very open and welcoming community. The point is that if you never ask for input on the quality of your code, then you will have no idea whether your code is secure.</p>

<h4>Logins and Passwords</h4>

<p>Your clients will need to log into WordPress to manage their content. WordPress core does what it can to prevent weak passwords from getting through, but this usually isn’t enough.</p>

<p>I’d recommend adding a plugin for two-factor authentication to your website, along with a limit on login attempts. Even better, do away with passwords entirely and work with magic links.</p>

<h4>Trust But Verify</h4>

<p>So far in this article, we haven’t talked about social engineering at all. It’s a form of hacking that’s gaining momentum, but it generally isn’t used to hack into WordPress websites. It is, however, an excellent way to set up the culture around your website with security in mind. That’s because the best defense against social engineering is “Trust but verify”.</p>

<p>Whenever a client, a user or your boss asks for something related to security, the best way to deal with it is to trust but first to verify whether what they are saying is true.</p>

<p>A client can claim they need administrator access to WordPress, but your job is to verify whether this is true. Do they actually need access, or are they missing just a single capability in their role? Is there a way to solve this problem without adding possibly new attack vectors?</p>

<p>“Trust but verify” is a simple yet effective mantra when it comes to security questions, and it can really help get people up to speed.</p>

<h3>Conclusion</h3>

<p>Is WordPress insecure? No, it’s not. WordPress core is constantly being updated and fixed, and most reported WordPress hacks aren’t from WordPress itself. Is the culture surrounding WordPress insecure? You betcha!</p>

<p>But by having security in mind with every line of code you write, every user you add, every plugin you enable and every hosting bill you pay, you can at least ensure that you’re running a secure website that keeps your reputation intact and your data safe.</p>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(ms, ra, yk, il, al)</span>
</div>


              </article>
            </body>
          </html>
---------------
<h1 id="#title_3" >4、文章： Eclipse Collections：让Java Streams更上一层楼</h1>
Vladimir Zakharov, Kristen O'Leary
[http://www.infoq.com/cn/articles/Refactoring-to-Eclipse-Collections?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/Refactoring-to-Eclipse-Collections?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/Refactoring-to-Eclipse-Collections/zh/smallimage/logo-java-small-new-1528886669220-1529593225438.jpg"/><p>Eclipse Collections是Java的高性能集合框架，为原生JDK集合增加了丰富的功能。在本文中，关键框架贡献者演示了如何将标准Java代码重构为Eclipse Collections数据结构和API，并减小内存开销。</p> <i>By Vladimir Zakharov</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_4" >5、专访肖雨浓：Netflix是怎样探索落地FaaS的？</h1>
肖雨浓
[http://www.infoq.com/cn/news/2018/06/netflix-faas?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/06/netflix-faas?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>2014 年，Serverless 架构进入大众视线，当时业界普遍认为，Serverless 化可大幅降低 IT 成本，将云的费用减少 10%-90%，同时还能提高服务部署效率。</p> <i>By 肖雨浓</i>
---------------
<h1 id="#title_5" >6、企业级以太坊联盟发布Client规范1.0</h1>
Kent Weare
[http://www.infoq.com/cn/news/2018/06/Enterprise-Ethereum-ClientSpec?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/06/Enterprise-Ethereum-ClientSpec?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>5月16日，企业级以太坊联盟（EEA）发布了企业以太坊Client规范1.0，这是一个开放的、跨平台的分布式账本（ledger）框架。该框架的关注点是创建一个基于标准的、企业级可用的方式来构建区块链应用，避免采用多个专用协议的方式。</p> <i>By Kent Weare</i> <i> Translated by 张卫滨 </i>
---------------
<h1 id="#title_6" >7、Safari浏览器的智能跟踪预防工作原理</h1>
Daniel Bryant
[http://www.infoq.com/cn/news/2018/06/safari-tracking-prevention?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/06/safari-tracking-prevention?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>最新版本的Apple浏览器Safari 12将提供“智能跟踪预防”（Intelligent Tracking Prevention，ITP）2.0，旨在降低第三方通过Cookie和其他方法跟踪网络用户的能力。</p> <i>By Daniel Bryant</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_7" >8、Microsoft宣布通过Azure Event Grid服务提供对CloudEvents的支持</h1>
Steef-Jan Wiggers
[http://www.infoq.com/cn/news/2018/06/event-grid-cloudevents?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/06/event-grid-cloudevents?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Microsoft宣布其将提供对CloudEvents的支持。CloudEvents是一项新的开放规范，用于对事件数据提供一致的描述标准。该开放规范由CNCF下设的无服务器工作组提出，而CNCF已与多家云服务和云提供商建立了合作伙伴关系。</p> <i>By Steef-Jan Wiggers</i> <i> Translated by 盖磊</i>
---------------
<h1 id="#title_8" >9、.NET Framework 4.8预览</h1>
Jonathan Allen
[http://www.infoq.com/cn/news/2018/06/.Net-4.8-Preview?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/06/.Net-4.8-Preview?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>虽然人们的大多数关注点都在.NET Core上，但经典的.NET Framework仍然在开发中。.NET 4.8的“早期访问”预览版表明了微软最关心的领域包括高DIP、可访问性和并发性。</p> <i>By Jonathan Allen</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_9" >10、GDPR给网站用户跟踪带来重大影响</h1>
Dylan Schiemann
[http://www.infoq.com/cn/news/2018/06/gdpr-improves-web-performance?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/06/gdpr-improves-web-performance?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>欧盟的“通用数据保护条例”（GDPR）于2018年5月25日生效，其中最明显的影响是用户收到了一系列通知用户隐私政策发生变化的电子邮件。随着网站开始遵守数据隐私条例，开发人员很快就发现网站页面加载性能得到显著改进。</p> <i>By Dylan Schiemann</i> <i> Translated by 无明</i>
---------------