## 文章索引
1、 <a href="#1视频演讲-基于容器的金融云服务生命周期管理体系设计与实践" >视频演讲： 基于容器的金融云服务生命周期管理体系设计与实践</a><br/>
2、 <a href="#2wordpress-notifications-made-easy" >WordPress Notifications Made Easy</a><br/>
3、 <a href="#3文章-深度学习的关键无监督深度学习简介附python代码" >文章： 深度学习的关键：无监督深度学习简介（附Python代码）</a><br/>
4、 <a href="#4文章-解密新一代java-jit编译器graal" >文章： 解密新一代Java JIT编译器Graal</a><br/>
5、 <a href="#5文章-ci/cddevops背后的推动力" >文章： CI/CD：DevOps背后的推动力</a><br/>
6、 <a href="#6文章-一文掌握aws成为云计算工程师" >文章： 一文掌握AWS，成为云计算工程师</a><br/>
7、 <a href="#7文章-服务网格的概述和工具选择" >文章： 服务网格的概述和工具选择</a><br/>
8、 <a href="#8作为程序员像ceo一样思考产品的现在与未来" >作为程序员，像CEO一样思考产品的现在与未来？</a><br/>
9、 <a href="#9netbsd-80带来spectre-v2/v4meltdownlazy-fpu缓解措施" >NetBSD 8.0带来Spectre V2/V4、Meltdown、Lazy FPU缓解措施</a><br/>
10、 <a href="#102018年20大python数据科学库都做了哪些更新" >2018年，20大Python数据科学库都做了哪些更新？</a><br/>
11、 <a href="#11改名之后的java-ee现在有什么新进展" >改名之后的Java EE，现在有什么新进展？</a><br/>
12、 <a href="#12物联网技术周报第-144-期:-基于-kafka-+-ots-+-maxcompute-完成了一次物联网系统技术重构" >物联网技术周报第 144 期: 基于 KafKa + OTS + MaxCompute 完成了一次物联网系统技术重构</a><br/><h1 id="#title_0" >1、视频演讲： 基于容器的金融云服务生命周期管理体系设计与实践</h1>
郭江林
[http://www.infoq.com/cn/presentations/financial-cloud-service-lifecycle-management-system?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/financial-cloud-service-lifecycle-management-system?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/presentations/financial-cloud-service-lifecycle-management-system/zh/mediumimage/guojianglin270-1532434969487.jpg"/><p>在实体经济中，最具活力和潜力的是为数众多的中小微企业。而中小银行已成为金融体系活力源泉和服务中小微企业的主力军。但在面对复杂的银行环境和金融机构环境限制，千奇百怪的问题层出不穷：CI/CD 无法保障；跨部门的沟通和分片管理使产品的生命周期管理极其困难；整个产品设计从版本库到用户手中的过程极其臃肿缓慢。就在全国中小型银行与中小型支付机构需要快速迭代，服务架构老化生锈，调用复杂且规模在快速增长的背景下，如何保障业务的快速迭代？如何保障服务稳定？如何透明式的管理软件的整个生命周期？本次演讲将从基于容器的金融云服务生命周期体系出发带大家一一破冰。</p> <i>By 郭江林</i>
---------------
<h1 id="#title_1" >2、WordPress Notifications Made Easy</h1>
Jakub Mikita
[https://www.smashingmagazine.com/2018/07/wordpress-notifications-made-easy/](https://www.smashingmagazine.com/2018/07/wordpress-notifications-made-easy/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/07/wordpress-notifications-made-easy/" />
              <title>WordPress Notifications Made Easy</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>WordPress Notifications Made Easy</h1>
                  
                    
                    <address>Jakub Mikita</address>
                  
                  <time datetime="2018-07-26T14:20:27&#43;02:00" class="op-published">2018-07-26T14:20:27+02:00</time>
                  <time datetime="2018-07-26T22:06:02&#43;00:00" class="op-modified">2018-07-26T22:06:02+00:00</time>
                </header>
                <p>WordPress doesn’t offer any kind of notification system. All you can use is the <code>wp_mail()</code> function, but all of the settings have to be hardcoded, or else you have to create a separate settings screen to allow the user tweak the options. It takes many hours to write a system that is reliable, configurable and easy to use. But not anymore. I’ll show you how to create your own notification system within minutes with the free Notification plugin. <strong>By notification, I mean any kind of notification</strong>. Most of the time, it will be email, but with the plugin we’ll be using, you can also send webhooks and other kinds of notifications.</p>

<p>While creating a project for one of my clients, I encountered this problem I’ve described. The requirement was to have multiple custom email alerts with configurable content. Instead of hardcoding each and every alert, I decided to build a system. I wanted it to be very flexible, and the aim was to be able to code new scenarios as quickly as possible.</p>

<p>The code I wrote was the start of a great development journey. It turned out that the system I created was flexible enough that it could work as a separate package. This is how the  plugin was born.</p>

<p>Suppose you want to send an email about a user profile being updated by one of your website’s members. WordPress doesn’t provide that functionality, but with the Notification plugin, you can create such an email in minutes. Or suppose you want to synchronize your WooCommerce products with third-party software by sending a webhook to a separate URL every time a new product is published. That’s easy to do with the plugin, too.</p>

<div class="c-felix-the-cat">
<h4>Lessons Learned While Developing WordPress Plugins</h4>
<p>Good plugin development and support lead to more downloads. More downloads mean more money and a better reputation. Learn how you can develop good-quality products with seven golden rules. </p>
</div>

<p>In this article, you’ll learn how to integrate the plugin in your own application and how to create an advanced WordPress notification system more quickly and easily than ever.</p>

<p>In this article, we’ll cover:</p>

<ol>
<li>how to install the plugin,</li>
<li>the idea behind the plugin and its architecture,</li>
<li>creating a custom scenario for notifications,</li>
<li>creating the action (step 1 of the process),</li>
<li>creating the trigger (step 2 of the process),</li>
<li>creating the custom notification type,</li>
<li>how to enable white-label mode and bundle the plugin in your package.</li>
</ol>



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




<h3>Installing The Plugin</h3>

<p>To create your own scenarios, you are going to need the Notification plugin. Just install it from the WordPress.org repository in your WordPress dashboard, or download it from the .</p>

<figure></figcaption></figure>

<p>Later in the article, you’ll learn how to hide this plugin from your clients and make it work as an integrated part of your plugin or theme.</p>

<h3>The Idea Of The Plugin</h3>

<p>Before going into your code editor, you’ll need to know what the plugin’s architecture looks like. The plugin contains many various components, but its core is really .</p>

<p>The main components are:</p>

<ul>
<li><strong>The notification</strong><br />This could be an email, webhook, push notification or SMS.</li>
<li><strong>The trigger</strong><br />This is what sends the notification. It’s effectively the WordPress action.</li>
<li><strong>The merge tag</strong><br />This is a small portion of the dynamic content, like <code>{post_title}</code>.</li>
</ul>

<p>To give you a better idea of how it all plays together, you can watch this short video:</p>

<figure class="video-container"><iframe data-src="https://www.youtube.com/embed/UPqVBhLGTek" width="600" height="480" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe></figure>

<p>The core of the Notification plugin is really just an API. All of the default triggers, like <em>Post published</em> and <em>User registered</em> are things built on top of that API.</p>

<p>Because the plugin was created for developers, adding your own triggers is very easy. All that’s required is a , which is just a single line of code and a class declaration.</p>

<h3>Custom Scenario</h3>

<p>Let’s devise a simple scenario. We’ll add a text area and button to the bottom of each post, allowing bugs in the article to be reported. Then, we’ll trigger the notification upon submission of the form.</p>

<figure></figure>

<p>This scenario was covered in another article, “”.</p>

<p>For simplicity, let’s make it a static form, but there’s no problem putting the action in an AJAX handler, instead of in the <code>wp_mail()</code> function.</p>

<p>Let’s create the form.</p>

<h4>The Form</h4>

<pre class="break-out"><code class="language-php">add_filter( 'the_content', 'report_a_bug_form' );
function report_a_bug_form( $content ) {

    // Display the form only on posts.
    if ( ! is_single() ) {
        return $content;
    }

    // Add the form to the bottom of the content.
    $content .= '&lt;form action="' . admin_url( 'admin-post.php' ) . '" method="POST">
        &lt;input type="hidden" name="post_id" value="' . get_ID() . '">
        &lt;input type="hidden" name="action" value="report_a_bug">
        &lt;textarea name="message" placeholder="' . __( 'Describe what\'s wrong...', 'reportabug' ) . '">&lt;/textarea>
        &lt;button>' . __( 'Report a bug', 'reportabug' ) . '&lt;/button>
    &lt;/div>';

    return $content;

}
</code></pre>

<p>Please note that many components are missing, like WordPress nonces, error-handling and display of the action’s result, but these are not the subject of this article. To better understand how to handle these actions, please read the .</p>

<h3>Preparing The Action</h3>

<p>To trigger the notification, we are going to need just a single action. This doesn’t have to be a custom action like the one below. You can use any of the actions already registered in WordPress core or another plugin.</p>

<h4>The Form Handler And Action</h4>

<pre class="break-out"><code class="language-php">add_action( 'admin_post_report_a_bug', 'report_a_bug_handler' );
add_action( 'admin_post_nopriv_report_a_bug', 'report_a_bug_handler' );
function report_a_bug_handler() {

    do_action( 'report_a_bug', $_POST['post_id'], $_POST['message'] );

    // Redirect back to the article.
    wp_safe_redirect( get_permalink( $_POST['post_id'] ) );
    exit;

}
</code></pre>

<p>You can read more on how to use the <code>admin-post.php</code> file in the .</p>

<p>This is all we need to create a custom, configurable notification. Let’s create the trigger.</p>

<h3>Registering The Custom Trigger</h3>

<p>The trigger is just a simple class that extends the abstract trigger. The abstract class does all of the work for you. It puts the trigger in the list, and it handles the notifications and merge tags.</p>

<p>Let’s start with the trigger declaration.</p>

<h4>Minimal Trigger Definition</h4>

<pre class="break-out"><code class="language-php">class ReportBug extends \BracketSpace\Notification\Abstracts\Trigger {

    public function __construct() {

        // Add slug and the title.
        parent::__construct(
            'reportabug',
            __( 'Bug report sent', 'reportabug' )
        );

        // Hook to the action.
        $this->add_action( 'report_a_bug', 10, 2 );

    }

    public function merge_tags() {}

}
</code></pre>

<p>All you need to do is call the parent constructor and pass the trigger slug and nice name.</p>

<p>Then, we can hook into our custom action. The <code>add_action</code> method is very similar to the <code>add_action()</code> function; so, the second parameter is the priority, and the last one is the number of arguments. Only the callback parameter is missing because the abstract class does that for us.</p>

<p>Having the class, we can register it as our new trigger.</p>

<pre><code class="language-php">register_trigger( new ReportBug() );
</code></pre>

<p>This is now a fully working trigger. You can select it from the list when composing a new notification.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a6eb58f6-39a8-443a-95fb-4d0d1fbec1d1/trigger.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a6eb58f6-39a8-443a-95fb-4d0d1fbec1d1/trigger.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a6eb58f6-39a8-443a-95fb-4d0d1fbec1d1/trigger.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a6eb58f6-39a8-443a-95fb-4d0d1fbec1d1/trigger.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a6eb58f6-39a8-443a-95fb-4d0d1fbec1d1/trigger.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a6eb58f6-39a8-443a-95fb-4d0d1fbec1d1/trigger.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a6eb58f6-39a8-443a-95fb-4d0d1fbec1d1/trigger.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<p>Although the trigger is working and we can already send the notification we want, it’s not very useful. We don’t have any way to show the recipient which post has a bug and what the message is.</p>

<p>This would be the time, then, to register some merge tags and set up the trigger context with the action parameters we have: the post ID and the message.</p>

<p>To do this, we can add another method to the trigger class. This is the action callback, where we can catch the action arguments.</p>

<div class="sponsors__wide-place"></div>




<h4>Handling Action Arguments</h4>

<pre><code class="language-php">public function action( $post_ID, $message ) {

    // If the message is empty, don't send any notifications.
    if ( empty( $message ) ) {
        return false;
    }

    // Set the trigger properties.
    $this->post    = get_post( $post_ID );
    $this->message = $message;

}
</code></pre>

<p>Note the <code>return false;</code> statement. If you return <code>false</code> from this method, the trigger will be stopped, and no notification will be sent. In our case, we don’t want a notification to be submitted with an empty message. In the real world, you’d want to validate that before the form is sent.</p>

<p>Then, we just set the trigger class’ properties, the complete post object and the message. Now, we can use them to add some merge tags to our trigger. We can just fill the content of the <code>merge_tags</code> method we declared earlier.</p>

<h4>Defining Merge Tags</h4>

<pre class="break-out"><code class="language-php">public function merge_tags() {

    $this->add_merge_tag( new \BracketSpace\Notification\Defaults\MergeTag\UrlTag( array(
        'slug'        => 'post_url',
        'name'        => __( 'Post URL', 'reportabug' ),
        'resolver'    => function( $trigger ) {
            return get_permalink( $trigger->post->ID );
        },
    ) ) );

    $this->add_merge_tag( new \BracketSpace\Notification\Defaults\MergeTag\StringTag( array(
        'slug'        => 'post_title',
        'name'        => __( 'Post title', 'reportabug' ),
        'resolver'    => function( $trigger ) {
            return $trigger->post->post_title;
        },
    ) ) );

    $this->add_merge_tag( new \BracketSpace\Notification\Defaults\MergeTag\HtmlTag( array(
        'slug'        => 'message',
        'name'        => __( 'Message', 'reportabug' ),
        'resolver'    => function( $trigger ) {
            return nl2br( $trigger->message );
        },
    ) ) );

    $this->add_merge_tag( new \BracketSpace\Notification\Defaults\MergeTag\EmailTag( array(
        'slug'        => 'post_author_email',
        'name'        => __( 'Post author email', 'reportabug' ),
        'resolver'    => function( $trigger ) {
            $author = get_userdata( $trigger->post->post_author );
            return $author->user_email;
        },
    ) ) );

}
</code></pre>

<p>This will add four merge tags, all ready to use while a notification is being composed.</p>

<p>The merge tag is an instance of a special class. You can see that there are many types of these tags, and we are using them depending on the value that is returned from the resolver. You can see all merge tags in the .</p>

<p>All merge tags are added via the <code>add_merge_tag</code> method, and they require the config array with three keys:</p>

<ul>
    
<li><strong>slug</strong><br />The static value that will be used in the notification (i.e. <code>{post_url}</code>).</li>
<li><strong>name</strong><br />The translated label for the merge tag.</li>
<li><strong>resolver</strong><br />The function that replaces the merge tag with the actual value.</li>
</ul>

<p>The resolver doesn’t have to be the closure, as in our case, but using it is convenient. You can pass a function name as a string or an array if this is a method in another class.</p>

<p>In the resolver function, only one argument is available: the trigger class instance. Thus, we can access the properties we just set in the <code>action</code> method and return the value we need.</p>

<p>And that’s all! The merge tags are not available to use with our trigger, and we can set up as many notifications of the bug report as we want.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/42d32928-bb71-4f69-a42f-45f74250ee89/notification.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/42d32928-bb71-4f69-a42f-45f74250ee89/notification.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/42d32928-bb71-4f69-a42f-45f74250ee89/notification.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/42d32928-bb71-4f69-a42f-45f74250ee89/notification.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/42d32928-bb71-4f69-a42f-45f74250ee89/notification.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/42d32928-bb71-4f69-a42f-45f74250ee89/notification.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/42d32928-bb71-4f69-a42f-45f74250ee89/notification.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<h3>Creating The Custom Notification Type</h3>

<p>The Notification plugin offers not only custom triggers, but also custom notification types. The plugin ships with two types, email and webhook, but it has a simple API to register your own notifications.</p>

<p>It works very similarly to the custom trigger: You also need a class and a call to one simple function to register it.</p>

<p>I’m showing only an example; the implementation will vary according to the system you wish to integrate. You might need to include a third-party library and call its API or operate in WordPress’ file system, but the guide below will set you up with the basic process.</p>

<p>Let’s start with a class declaration:</p>

<pre class="break-out"><code class="language-php">class CustomNotification extends \BracketSpace\Notification\Abstracts\Notification {

    public function __construct() {

        // Add slug and the title.
        parent::__construct( 
            'custom_notification',
            __( 'Custom Notification', 'textdomain' )
        );

    }

    public function form_fields() {}

    public function send( \BracketSpace\Notification\Interfaces\Triggerable $trigger ) {}

}
</code></pre>

<p>In the constructor, you must call the parent’s class constructor and pass the slug and nice name of the notification.</p>

<p>The <code>form_fields</code> method is used to create a configuration form for notifications. (For example, the email notification would have a subject, body, etc.)</p>

<p>The <code>send</code> method is called by the trigger, and it’s where you can call the third-party API that you wish to integrate with.</p>

<p>Next, you have to register it with the <code>register_notification</code> function.</p>

<pre><code class="language-php">register_trigger( new CustomNotification() );
</code></pre>

<h4>The Notification Form</h4>

<p>There might be a case in which you have a notification with no configuration fields. That’s fine, but most likely you’ll want to give the WordPress administrator a way to configure the notification content with the merge tags.</p>

<p>That’s why we’ll register two fields, the title and the message, in the <code>form_fields</code> method. It looks like this:</p>

<pre class="break-out"><code class="language-php">public function form_fields() {

    $this->add_form_field( new \BracketSpace\Notification\Defaults\Field\InputField( array(
        'label'       => __( 'Title', 'textdomain' ),
        'name'        => 'title',
        'resolvable'  => true,
        'description' => __( 'You can use merge tags', 'textdomain' ),
    ) ) );

    $this->add_form_field( new \BracketSpace\Notification\Defaults\Field\TextareaField( array(
        'label'       => __( 'Message', 'textdomain' ),
        'name'        => 'message',
        'resolvable'  => true,
        'description' => __( 'You can use merge tags', 'textdomain' ),
    ) ) );

}
</code></pre>

<p>As you can see, each field is an object and is registered with the <code>add_form_field</code> method. For the list of all available field types, please visit .</p>

<p>Each field has the translatable label, the unique name and a set of other properties. You can define whether the field should be resolved with the merge tags with the <code>resolvable</code> key. This means that when someone uses the <code>{post_title}</code> merge tag in this field, it will be changed with the post’s actual title. You can also provide the <code>description</code> field for a better user experience.</p>

<p>At this point, your custom notification type can be used in the plugin’s interface with any available trigger type.</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/121010fd-aba6-47e2-b889-de2312903d0e/custom-notification.png">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/121010fd-aba6-47e2-b889-de2312903d0e/custom-notification.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/121010fd-aba6-47e2-b889-de2312903d0e/custom-notification.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/121010fd-aba6-47e2-b889-de2312903d0e/custom-notification.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/121010fd-aba6-47e2-b889-de2312903d0e/custom-notification.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/121010fd-aba6-47e2-b889-de2312903d0e/custom-notification.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/121010fd-aba6-47e2-b889-de2312903d0e/custom-notification.png"
			sizes="100vw"
			alt=""
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			()
		</figcaption>
	
</figure>


<h4>Sending The Custom Notification</h4>

<p>In order to make it really work, we have to use the <code>send</code> method in our notification class declaration. This is the place where you can write an API call or use WordPress’ file system or any WordPress API, and do whatever you like with the notification data.</p>

<p>This is how you can access it:</p>

<pre class="break-out"><code class="language-php">public function send( \BracketSpace\Notification\Interfaces\Triggerable $trigger ) {

    $title   = $this->data['title'];
    $message = $this->data['message'];

    // @todo Write the integration here.

}
</code></pre>

<p>At this point, all of the fields are resolved with the merge tags, which means the variables are ready to be shipped.</p>

<p>That gives you endless possibilities to integrate WordPress with any service, whether it’s your local SMS provider, another WordPress installation or any external API you wish to communicate with.</p>

<div class="sponsors__wide-place"></div>




<h3>White Labeling And Bundling The Plugin</h3>

<p>It’s not ideal to create a dependency of a plugin that can be easily deactivated and uninstalled. If you are building a system that really requires the Notification plugin to be always available, you can bundle the plugin in your own code.</p>

<p>If you’ve used the Advanced Custom Fields plugin before, then you are probably familiar with the bundling procedure. Just copy the plugin’s files to your plugin or theme, and invoke the plugin manually.</p>

<p>The Notification plugin works very similarly, but invoking the plugin is much simpler than with Advanced Custom Fields.</p>

<p>Just copy the plugin’s files, and require one file to make it work.</p>

<pre><code class="language-php">require_once( 'path/to/plugin/notification/load.php' );
</code></pre>

<p>The plugin will figure out its location and the URLs.</p>

<p>But bundling the plugin might not be enough. Perhaps you need to completely hide that you are using this third-party solution. This is why the Notification plugin comes with a white-label mode, which you can activate at any time.</p>

<p>It also is enabled as a single call to a function:</p>

<pre><code class="language-php">notification_whitelabel( array(
    // Admin page hook under which the Notifications will be displayed.
    'page_hook'       => 'edit.php?post_type=page',
    // If display extensions page.
    'extensions'      => false,
    // If display settings page.
    'settings'        => false,
    // Limit settings access to user IDs.
    // This works only if settings are enabled.
    'settings_access' => array( 123, 456 ),
) );
</code></pre>

<p>By default, calling this function will hide all of the default triggers.</p>

<p>Using both techniques, white labeling and bundling, will completely hide any references to the plugin’s origin, and the solution will behave as a fully integrated part of your system.</p>

<h3>Conclusion</h3>

<p>The Notification plugin is an all-in-one solution for any custom WordPress notification system. It’s extremely easy to configure, and it works out of the box. All of the triggers that are registered will work with any notification type, and if you have any advanced requirements, you can save some time by using an existing .</p>

<p>If you’d like to learn more details and advanced techniques, go to the .</p>

<p>I’m always open to new ideas, so if you have any, you can reach out to me here in the comments, via the .</p>

<p> from the repository, and give it a try!</p>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(ra, yk, il)</span>
</div>


              </article>
            </body>
          </html>
---------------
<h1 id="#title_2" >3、文章： 深度学习的关键：无监督深度学习简介（附Python代码）</h1>
Faizan Shaikh
[http://www.infoq.com/cn/articles/trudging-into-unsupervised-deep-learning?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/trudging-into-unsupervised-deep-learning?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/trudging-into-unsupervised-deep-learning/zh/smallimage/GettyImages-628619884-1514929417641-1532265722659.jpg"/><p>在这篇文章中，我们用一个直观的案例研究概述了无监督深度学习的概念。并且详解了在MNIST数据集上进行无监督学习的代码，包括K-Means、自编码器以及DEC算法。</p> <i>By Faizan Shaikh</i> <i> Translated by 马卓奇</i>
---------------
<h1 id="#title_3" >4、文章： 解密新一代Java JIT编译器Graal</h1>
Ben Evans
[http://www.infoq.com/cn/articles/Graal-Java-JIT-Compiler?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/Graal-Java-JIT-Compiler?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/Graal-Java-JIT-Compiler/zh/smallimage/Getting-to-Know-Graal-the-New-Java-JIT-Compiler-logo-1531559646800-1532196036548.jpg"/><p>Oracle发布了Graal，它既是Java的新JIT编译器，也是下一代多语言虚拟机GraalVM的主要组件。这项工作旨在改善启动时间，并减少Java应用程序的资源占用，并在单个VM中解锁完全多语言技术。初始版本包括JVM和对JS、Ruby和R语言的支持。</p> <i>By Ben Evans</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_4" >5、文章： CI/CD：DevOps背后的推动力</h1>
Christina Cardoza
[http://www.infoq.com/cn/articles/cicd-driving-force-behind-devops?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/cicd-driving-force-behind-devops?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/cicd-driving-force-behind-devops/zh/smallimage/GettyImages-628837052-1518704902676-1532264245837.jpeg"/><p>Christina Cardoza在文中告诉我们，为什么说CI/CD才是DevOps背后的推动力。</p> <i>By Christina Cardoza</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_5" >6、文章： 一文掌握AWS，成为云计算工程师</h1>
SpectralCoding
[http://www.infoq.com/cn/articles/so_you_want_to_learn_aws_aka_how_do_i_learn_to_be?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/so_you_want_to_learn_aws_aka_how_do_i_learn_to_be?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/so_you_want_to_learn_aws_aka_how_do_i_learn_to_be/zh/smallimage/logo-cloud-1527438712853-1532265243086.jpeg"/><p>本文带一步一步了解AWS，入门云计算。</p> <i>By SpectralCoding</i> <i> Translated by 安翔</i>
---------------
<h1 id="#title_6" >7、文章： 服务网格的概述和工具选择</h1>
Twain Taylor
[http://www.infoq.com/cn/articles/an-overview-of-the-service-mesh-and-its-tooling-options?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/an-overview-of-the-service-mesh-and-its-tooling-options?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/an-overview-of-the-service-mesh-and-its-tooling-options/zh/smallimage/GettyImages-683951840-1532264701966.jpg"/><p>该文章简要介绍了服务网络的定义及其在网络中的作用，包括负载均衡和服务发现，并介绍了在服务网格管理中的两个重要工具Linkerd和Istio，最后介绍和网络安全相关的工具Project Calico</p> <i>By Twain Taylor</i> <i> Translated by 方彦</i>
---------------
<h1 id="#title_7" >8、作为程序员，像CEO一样思考产品的现在与未来？</h1>
极客时间
[http://www.infoq.com/cn/news/2018/07/think-production-future?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/think-production-future?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>给大家介绍一位兼通技术和产品的作者，他在极客时间的专栏「邱岳的产品手记」得到了读者们极高的评价。专栏完结后，很多读者们希望他能继续第二季。</p> <i>By 极客时间</i>
---------------
<h1 id="#title_8" >9、NetBSD 8.0带来Spectre V2/V4、Meltdown、Lazy FPU缓解措施</h1>
Sergio De Simone
[http://www.infoq.com/cn/news/2018/07/netbsd-8-released?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/netbsd-8-released?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>NetBSD是一款基于BSD的操作系统，跨许多体系结构提供了可移植性。NetBSD 8.0是该系统的一个主要版本，该版本带来了Spectre V2/V4、Meltdown、Lazy FPU漏洞缓解措施以及许多新特性和Bug修复。</p> <i>By Sergio De Simone</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_9" >10、2018年，20大Python数据科学库都做了哪些更新？</h1>
ActiveWizards
[http://www.infoq.com/cn/news/2018/07/20-python-libraries-data?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/20-python-libraries-data?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>去年，我们发了一篇博文，列举了一些被证明是最有用的Python库。今年，我们扩充了原来的清单，并重新审视之前讨论过的库，重点关注在过去一年内出现的更新。我们对它们进行了分组，排序不分先后，因为真的说不清它们哪个更好。</p> <i>By ActiveWizards</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_10" >11、改名之后的Java EE，现在有什么新进展？</h1>
Cesar Saavedra
[http://www.infoq.com/cn/news/2018/07/javaee-changename-advantage?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/javaee-changename-advantage?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Jakarta EE正在为企业版Java开辟新的道路。在这篇文章中，Cesar Saavedra将解释为什么说Jakarta EE为企业版Java带来了新鲜的空气。</p> <i>By Cesar Saavedra</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_11" >12、物联网技术周报第 144 期: 基于 KafKa + OTS + MaxCompute 完成了一次物联网系统技术重构</h1>
黄峰达
[http://www.infoq.com/cn/news/2018/07/iot-weekly-144?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/07/iot-weekly-144?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>基于 KafKa + OTS + MaxCompute 完成了一次物联网系统技术重构；使用 Raspberry Pi 和 Arduino 构建一个示波器；使用 OpenCV 和 ESP32 构建一个跟随脸部移动的伺服器；小米联合金山云发布 “1KM边缘计算” 携手布局“云+边缘”新赛道；微软宣布启动 Windows 10 IoT Core Services 公开预览；微软与通用电气达成最大规模合作 推工业物联网普及。</p> <i>By 黄峰达</i>
---------------