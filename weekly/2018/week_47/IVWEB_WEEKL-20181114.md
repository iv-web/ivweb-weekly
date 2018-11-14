## 文章索引
1、 <a href="#1react-conf-recap:-hooks-suspense-and-concurrent-rendering" >React Conf recap: Hooks, Suspense, and Concurrent Rendering</a><br/>
2、 <a href="#2sending-emails-asynchronously-through-aws-ses" >Sending Emails Asynchronously Through AWS SES</a><br/><h1 id="#title_0" >1、React Conf recap: Hooks, Suspense, and Concurrent Rendering</h1>

[https://reactjs.org/blog/2018/11/13/react-conf-recap.html](https://reactjs.org/blog/2018/11/13/react-conf-recap.html)
<p>This year’s  took place on October 25 and 26 in Henderson, Nevada, where more than 600 attendees gathered to discuss the latest in UI engineering.</p>
<br>
<div>
          <div
            class="gatsby-resp-iframe-wrapper"
            style="padding-bottom: 56.25%; position: relative; height: 0; overflow: hidden;"
          >
            <iframe src="https://www.youtube.com/embed/V-QO-KO90iQ" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen style="
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
          "></iframe>
          </div>
          </div>
<p>Sophie Alpert and Dan Abramov kicked off Day 1 with their keynote, React Today and Tomorrow. In the talk, they introduced , which are a new proposal that adds the ability to access features such as state without writing a JavaScript class. Hooks promise to dramatically simplify the code required for React components and are currently available in a React alpha release.</p>
<br>
<div>
          <div
            class="gatsby-resp-iframe-wrapper"
            style="padding-bottom: 56.25%; position: relative; height: 0; overflow: hidden;"
          >
            <iframe src="https://www.youtube.com/embed/ByBPyMBTzM0" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen style="
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
          "></iframe>
          </div>
          </div>
<p>On the morning of Day 2, Andrew Clark and Brian Vaughn presented Concurrent Rendering in React. Andrew covered the recently announced  tooling to make apps built in React run faster.</p>
<br>
<div>
          <div
            class="gatsby-resp-iframe-wrapper"
            style="padding-bottom: 56.25%; position: relative; height: 0; overflow: hidden;"
          >
            <iframe src="https://www.youtube.com/embed/UcqRXTriUVI" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen style="
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
          "></iframe>
          </div>
          </div>
<p>In the afternoon, Parashuram N spoke in detail about React Native’s New Architecture, a long-term project that the React Native team has been working on over the past year and . We’re really excited about the potential of this project to improve performance, simplify interoperability with other libraries, and set a strong foundation for the future of React Native.</p>
<p>Now that the conference is over, all 28 conference talks are . There are tons of great ones from both days. We can’t wait until next year!</p>
---------------
<h1 id="#title_1" >2、Sending Emails Asynchronously Through AWS SES</h1>
Leonardo Losoviz
[https://www.smashingmagazine.com/2018/11/sending-emails-asynchronously-through-aws-ses/](https://www.smashingmagazine.com/2018/11/sending-emails-asynchronously-through-aws-ses/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/11/sending-emails-asynchronously-through-aws-ses/" />
              <title>Sending Emails Asynchronously Through AWS SES</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>Sending Emails Asynchronously Through AWS SES</h1>
                  
                    
                    <address>Leonardo Losoviz</address>
                  
                  <time datetime="2018-11-13T14:30:53&#43;01:00" class="op-published">2018-11-13T14:30:53+01:00</time>
                  <time datetime="2018-11-13T14:40:42&#43;00:00" class="op-modified">2018-11-13T14:40:42+00:00</time>
                </header>
                

<p>Most applications send emails to communicate with their users. Transactional emails are those triggered by the user&rsquo;s interaction with the application, such as when welcoming a new user after registering in the site, giving the user a link to reset the password, or attaching an invoice after the user does a purchase. All these previous cases will typically require sending only one email to the user. In some other cases though, the application needs to send many more emails, such as when a user posts new content on the site, and all her followers (which, in a platform like Twitter, may amount to millions of users) will receive a notification. In this latter situation, not architected properly, sending emails may become a bottleneck in the application.</p>

<p>That is what happened in my case. I have a site that may need to send 20 emails after some user-triggered actions (such as user notifications to all her followers). Initially, it relied on sending the emails through a popular cloud-based SMTP provider (such as ), however the response back to the user would take seconds. Evidently, connecting to the SMTP server to send those 20 emails was slowing the process down significantly.</p>

<p>After inspection, I found out the sources of the problem:</p>

<ol>
<li><strong>Synchronous connection</strong><br/> The application connects to the SMTP server and waits for an acknowledgment, synchronously, before continuing the execution of the process.</li>
<li><strong>High latency</strong><br/> While my server is located in Singapore, the SMTP provider I was using has its servers located in the US, making the roundtrip connection take considerable time.</li>
<li><strong>No reusability of the SMTP connection</strong></br> When calling the function to send an email, the function sends the email immediately, creating a new SMTP connection on that moment (it doesn&rsquo;t offer to collect all emails and send them all together at the end of the request, under a single SMTP connection).</li>
</ol>

<p>Because of #1, the time the user must wait for the response is tied to the time it takes to send the emails. Because of #2, the time to send one email is relatively high. And because of #3, the time to send 20 emails is 20 times the time it takes to send one email. While sending only one email may not make the application terribly slower, sending 20 emails certainly does, affecting the user experience.</p>

<p>Let&rsquo;s see how we can solve this issue.</p>



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




<h3 id="paying-attention-to-the-nature-of-transactional-emails">Paying Attention To The Nature Of Transactional Emails</h3>

<p>Before anything, we must notice that not all emails are equal in importance. We can broadly categorize emails into two groups: priority and non-priority emails. For instance, if the user forgot the password to access the account, she will expect the email with the password reset link immediately on her inbox; that is a priority email. In contrast, sending an email notifying that somebody we follow has posted new content does not need to arrive on the user&rsquo;s inbox immediately; that is a non-priority email.</p>

<p>The solution must optimize how these two categories of emails are sent. Assuming that there will only be a few (maybe 1 or 2) priority emails to be sent during the process, and the bulk of the emails will be non-priority ones, then we design the solution as follows:</p>

<ul>
<li><strong>Priority emails</strong> can simply avoid the high latency issue by using an SMTP provider located in the same region where the application is deployed. In addition to good research, this involves integrating our application with the provider&rsquo;s API.</li>
<li><strong>Non-priority emails</strong> can be sent asynchronously, and in batches where many emails are sent together. Implemented at the application level, it requires an appropriate technology stack.</li>
</ul>

<p>Let&rsquo;s define the technology stack to send emails asynchronously next.</p>

<h3 id="defining-the-technology-stack">Defining The Technology Stack</h3>

<p><strong>Note:</strong> I have decided to base my stack on AWS services because my website is already hosted on AWS EC2. Otherwise, I would have an overhead from moving data among several companies&rsquo; networks. However, we can implement our soluting using other cloud service providers too.</p>

<p>My first approach was to set-up a queue. Through a queue, I could have the application not send the emails anymore, but instead publish a message with the email content and metadata in a queue, and then have another process pick up the messages from the queue and send the emails.</p>

<div class="sponsors__wide-place"></div>




<p>However, when checking the queue service from AWS, called , I decided that it was not an appropriate solution, because:</p>

<ul>
<li>It is rather complex to set-up;</li>
<li>A standard queue message can store only up top 256 kb of information, which may not be enough if the email has attachments (an invoice for instance). And even though it is possible to split a large message into smaller messages, the complexity grows even more.</li>
</ul>

<p>Then I realized that I could perfectly imitate the behavior of a queue through a combination of other AWS services, , which are much easier to set-up. S3, a cloud object storage solution to store and retrieve data, can act as the repository for uploading the messages, and Lambda, a computing service that runs code in response to events, can pick a message and execute an operation with it.</p>

<p>In other words, we can set-up our email sending process like this:</p>

<ol>
<li>The application uploads a file with the email content + metadata to an S3 bucket.</li>
<li>Whenever a new file is uploaded into the S3 bucket, S3 triggers an event containing the path to the new file.</li>
<li>A Lambda function picks the event, reads the file, and sends the email.</li>
</ol>

<p>Finally, we have to decide how to send emails. We can either keep using the SMTP provider that we already have, having the Lambda function interact with their APIs, or use the AWS service for sending emails, called . Using SES has both benefits and drawbacks:</p>

<h5 id="benefits">Benefits:</h5>

<ul>
<li>Very simple to use from within AWS Lambda (it just takes 2 lines of code).</li>
<li>It is cheaper: Lambda fees are computed based on the amount of time it takes to execute the function, so connecting to SES from within the AWS network will take a shorter time than connecting to an external server, making the function finish earlier and costing less. (Unless SES is not available in the same region where the application is hosted; in my case, because SES is not offered in the Asian Pacific (Singapore) region, where my EC2 server is located, then I might be better off connecting to some Asia-based external SMTP provider).</li>
</ul>

<h5 id="drawbacks">Drawbacks:</h5>

<ul>
<li>Not many stats for monitoring our sent emails are provided, and adding more powerful ones requires extra effort (eg: tracking what percentage of emails were opened, or what links were clicked, ).</li>
<li>If we keep using the SMTP provider for sending the priority emails, then we won&rsquo;t have our stats all together in 1 place.</li>
</ul>

<p>For simplicity, in the code below we will be using SES.</p>

<p>We have then defined the logic of the process and stack as follows: The application sends priority emails as usual, but for non-priority ones, it uploads a file with email content and metadata to S3; this file is asynchronously processed by a Lambda function, which connects to SES to send the email.</p>

<p>Let&rsquo;s start implementing the solution.</p>

<div class="sponsors__wide-place"></div>




<h3 id="differentiating-between-priority-and-non-priority-emails">Differentiating Between Priority And Non-Priority Emails</h3>

<p>In short, this all depends on the application, so we need to decide on an email by email basis. I will describe a solution I implemented for WordPress, which requires some hacks around the constraints from function <code>wp_mail</code>. For other platforms, the strategy below will work too, but quite possibly there will be better strategies, which do not require hacks to work.</p>

<p>The way to send an email in WordPress is by calling function <code>wp_mail</code>, and we don&rsquo;t want to change that (eg: by calling either function <code>wp_mail_synchronous</code> or <code>wp_mail_asynchronous</code>), so our implementation of <code>wp_mail</code> will need to handle both synchronous and asynchronous cases, and will need to know to which group the email belongs. Unluckily, <code>wp_mail</code> doesn&rsquo;t offer any extra parameter from which we could asses this information, as it can be seen from its signature:</p>

<pre class="break-out"><code class="language-javascript">function wp_mail( $to, $subject, $message, $headers = '', $attachments = array() )</code></pre>

<p>Then, in order to find out the category of the email we add a hacky solution: by default, we make an email belong to the priority group, and if <code>$to</code> contains a particular email (eg: nonpriority@asynchronous.mail), or if <code>$subject</code> starts with a special string (eg: &ldquo;[Non-priority!]&ldquo;), then it belongs to the non-priority group (and we remove the corresponding email or string from the subject). <code>wp_mail</code> is a pluggable function, so we can override it simply by implementing a new function with the same signature on our functions.php file. Initially, it contains the same code of the original <code>wp_mail</code> function, located in file wp-includes/pluggable.php, to extract all parameters:</p>

<pre class="break-out"><code class="language-javascript">if ( !function_exists( 'wp_mail' ) ) :

function wp_mail( $to, $subject, $message, $headers = '', $attachments = array() ) {

  $atts = apply_filters( 'wp_mail', compact( 'to', 'subject', 'message', 'headers', 'attachments' ) );

  if ( isset( $atts['to'] ) ) {
    $to = $atts['to'];
  }

  if ( !is_array( $to ) ) {
    $to = explode( ',', $to );
  }

  if ( isset( $atts['subject'] ) ) {
    $subject = $atts['subject'];
  }

  if ( isset( $atts['message'] ) ) {
    $message = $atts['message'];
  }

  if ( isset( $atts['headers'] ) ) {
    $headers = $atts['headers'];
  }

  if ( isset( $atts['attachments'] ) ) {
    $attachments = $atts['attachments'];
  }

  if ( ! is_array( $attachments ) ) {
    $attachments = explode( "\n", str_replace( "\r\n", "\n", $attachments ) );
  }
  
  // Continue below...
}
endif;
</code></pre>

<p>And then we check if it is non-priority, in which case we then fork to a separate logic under function <code>send_asynchronous_mail</code> or, if it is not, we keep executing the same code as in the original <code>wp_mail</code> function:</p>

<pre class="break-out"><code class="language-javascript">function wp_mail( $to, $subject, $message, $headers = '', $attachments = array() ) {

  // Continued from above...

  $hacky_email = "nonpriority@asynchronous.mail";
  if (in_array($hacky_email, $to)) {

    // Remove the hacky email from $to
    array_splice($to, array_search($hacky_email, $to), 1);

    // Fork to asynchronous logic
    return send_asynchronous_mail($to, $subject, $message, $headers, $attachments);
  }

  // Continue all code from original function in wp-includes/pluggable.php
  // ...
}
</code></pre>

<p>In our function <code>send_asynchronous_mail</code>, instead of uploading the email straight to S3, we simply add the email to a global variable <code>$emailqueue</code>, from which we can upload all emails together to S3 in a single connection at the end of the request:</p>

<pre class="break-out"><code class="language-javascript">function send_asynchronous_mail($to, $subject, $message, $headers, $attachments) {
  
  global $emailqueue;
  if (!$emailqueue) {
    $emailqueue = array();
  }
  
  // Add email to queue. Code continues below...
}
</code></pre>

<p>We can upload one file per email, or we can bundle them so that in 1 file we contain many emails. Since <code>$headers</code> contains email meta (from, content-type and charset, CC, BCC, and reply-to fields), we can group emails together whenever they have the same <code>$headers</code>. This way, these emails can all be uploaded in the same file to S3, and the <code>$headers</code> meta information will be included only once in the file, instead of once per email:</p>

<pre class="break-out"><code class="language-javascript">function send_asynchronous_mail($to, $subject, $message, $headers, $attachments) {
  
  // Continued from above...

  // Add email to the queue
  $emailqueue[$headers] = $emailqueue[$headers] ?? array();
  $emailqueue[$headers][] = array(
    'to' => $to,
    'subject' => $subject,
    'message' => $message,
    'attachments' => $attachments,
  );

  // Code continues below
}
</code></pre>

<p>Finally, function <code>send_asynchronous_mail</code> returns <code>true</code>. Please notice that this code is hacky: <code>true</code> would normally mean that the email was sent successfully, but in this case, it hasn&rsquo;t even been sent yet, and it could perfectly fail. Because of this, the function calling <code>wp_mail</code> must not treat a <code>true</code> response as &ldquo;the email was sent successfully,&rdquo; but an acknowledgment that it has been enqueued. That&rsquo;s why it is important to restrict this technique to non-priority emails so that if it fails, the process can keep retrying in the background, and the user will not expect the email to already be in her inbox:</p>

<pre class="break-out"><code class="language-javascript">function send_asynchronous_mail($to, $subject, $message, $headers, $attachments) {
  
  // Continued from above...

  // That's it!
  return true;
}
</code></pre>

<h3 id="uploading-emails-to-s3">Uploading Emails To S3</h3>

<p>In my previous article “”, I described how to create a bucket in S3, and how to upload files to the bucket through the SDK. All code below continues the implementation of a solution for WordPress, hence we connect to AWS using the SDK for PHP.</p>

<p>We can extend from the abstract class <code>AWS_S3</code> (introduced in my previous article) to connect to S3 and upload the emails to a bucket &ldquo;async-emails&rdquo; at the end of the request (triggered through <code>wp_footer</code> hook). Please notice that we must keep the ACL as &ldquo;private&rdquo; since we don&rsquo;t want the emails to be exposed to the internet:</p>

<pre class="break-out"><code class="language-javascript">class AsyncEmails_AWS_S3 extends AWS_S3 {

  function __construct() {

    // Send all emails at the end of the execution
    add_action("wp_footer", array($this, "upload_emails_to_s3"), PHP_INT_MAX);
  }

  protected function get_acl() {

    return "private";
  }

  protected function get_bucket() {

    return "async-emails";
  }

  function upload_emails_to_s3() {

    $s3Client = $this->get_s3_client();

    // Code continued below...
  }
}
new AsyncEmails_AWS_S3();
</code></pre>

<p>We start iterating through the pairs of headers =&gt; emaildata saved in global variable <code>$emailqueue</code>, and get a default configuration from function <code>get_default_email_meta</code> for if the headers are empty. In the code below, I only retrieve the &ldquo;from&rdquo; field from the headers (the code to extract all headers can be copied from the original function <code>wp_mail</code>):</p>

<pre class="break-out"><code class="language-javascript">class AsyncEmails_AWS_S3 extends AWS_S3 {

  public function get_default_email_meta() {

    // Code continued from above...

    return array(
      'from' => sprintf(
        '%s <%s>',
        get_bloginfo('name'),
        get_bloginfo('admin_email')
      ),
      'contentType' => 'text/html',
      'charset' => strtolower(get_option('blog_charset'))
    );
  }

  public function upload_emails_to_s3() {

    // Code continued from above...

    global $emailqueue;
    foreach ($emailqueue as $headers => $emails) {

      $meta = $this->get_default_email_meta();

      // Retrieve the "from" from the headers
      $regexp = '/From:\s*(([^\<]*?) <)?<?(.+?)>?\s*\n/i';
      if(preg_match($regexp, $headers, $matches)) {
        
        $meta['from'] = sprintf(
          '%s <%s>',
          $matches[2],
          $matches[3]
        );
      }

      // Code continued below... 
    }
  }
}
</code></pre>

<p>Finally, we upload the emails to S3. We decide how many emails to upload per file with the intention to save money. Lambda functions charge based on the amount of time they need to execute, calculated on spans of 100ms. The more time a function requires, the more expensive it becomes.</p>

<p>Sending all emails by uploading 1 file per email, then, is more expensive than uploading 1 file per many emails, since the overhead from executing the function is computed once per email, instead of only once for many emails, and also because sending many emails together fills the 100ms spans more thoroughly.</p>

<p>So we upload many emails per file. How many emails? Lambda functions have a maximum execution time (3 seconds by default), and if the operation fails, it will keep retrying from the beginning, not from where it failed. So, if the file contains 100 emails, and Lambda manages to send 50 emails before the max time is up, then it fails and it retries executing the operation again, sending the first 50 emails once again. To avoid this, we must choose a number of emails per file that we are confident is enough to process before the max time is up. In our situation, we could choose to send 25 emails per file. The number of emails depends on the application (bigger emails will take longer to be sent, and the time to send an email will depend on the infrastructure), so we should do some testing to come up with the right number.</p>

<p>The content of the file is simply a JSON object, containing the email meta under property &ldquo;meta&rdquo;, and the chunk of emails under property &ldquo;emails&rdquo;:</p>

<pre class="break-out"><code class="language-javascript">class AsyncEmails_AWS_S3 extends AWS_S3 {

  public function upload_emails_to_s3() {

    // Code continued from above...
    foreach ($emailqueue as $headers => $emails) {

      // Code continued from above...

      // Split the emails into chunks of no more than the value of constant EMAILS_PER_FILE:
      $chunks = array_chunk($emails, EMAILS_PER_FILE);
      $filename = time().rand();
      for ($chunk_count = 0; $chunk_count < count($chunks); $chunk_count++) {
        
        $body = array(
          'meta' => $meta,
          'emails' => $chunks[$chunk_count],
        );

        // Upload to S3
        $s3Client->putObject([
          'ACL' => $this->get_acl(),
          'Bucket' => $this->get_bucket(),
          'Key' => $filename.$chunk_count.'.json',
          'Body' => json_encode($body),
        ]);  
      }   
    }
  }
}
</code></pre>

<p>For simplicity, in the code above, I am not uploading the attachments to S3. If our emails need to include attachments, then we must use SES function <code>SendRawEmail</code> instead of <code>SendEmail</code> (which is used in the Lambda script below).</p>

<p>Having added the logic to upload the files with emails to S3, we can move next to coding the Lambda function.</p>

<h3 id="coding-the-lambda-script">Coding The Lambda Script</h3>

<p>Lambda functions are also called serverless functions, not because they do not run on a server, but because the developer does not need to worry about the server: the developer simply provides the script, and the cloud takes care of provisioning the server, deploying and running the script. Hence, as mentioned earlier, Lambda functions are charged based on function execution time.</p>

<p>The following Node.js script does the required job. Invoked by the S3 &ldquo;Put&rdquo; event, which indicates that a new object has been created on the bucket, the function:</p>

<ol>
<li>Obtains the new object&rsquo;s path (under variable <code>srcKey</code>) and bucket (under variable <code>srcBucket</code>).</li>
<li>Downloads the object, through <code>s3.getObject</code>.</li>
<li>Parses the content of the object, through <code>JSON.parse(response.Body.toString())</code>, and extracts the emails and the email meta.</li>
<li>Iterates through all the emails, and sends them through <code>ses.sendEmail</code>.</li>
</ol>

<pre class="break-out"><code class="language-javascript">var async = require('async');
var aws = require('aws-sdk');
var s3 = new aws.S3();
      
exports.handler = function(event, context, callback) {

  var srcBucket = event.Records[0].s3.bucket.name;
  var srcKey = decodeURIComponent(event.Records[0].s3.object.key.replace(/\+/g, " ")); 

  // Download the file from S3, parse it, and send the emails
  async.waterfall([

    function download(next) {

      // Download the file from S3 into a buffer.
      s3.getObject({
        Bucket: srcBucket,
        Key: srcKey
      }, next);
    },
    function process(response, next) {
          
      var file = JSON.parse(response.Body.toString());
      var emails = file.emails;
      var emailsMeta = file.meta;
        
      // Check required parameters
      if (emails === null || emailsMeta === null) {
        callback('Bad Request: Missing required data: ' + response.Body.toString());
        return;
      }
      if (emails.length === 0) {
        callback('Bad Request: No emails provided: ' + response.Body.toString());
        return;
      }
      
      var totalEmails = emails.length;
      var sentEmails = 0;
      for (var i = 0; i < totalEmails; i++) {

        var email = emails[i];
        var params = {
          Destination: {
            ToAddresses: email.to
          },
          Message: {          
            Subject: {
              Data: email.subject,
              Charset: emailsMeta.charset
            }
          },
          Source: emailsMeta.from
        };

        if (emailsMeta.contentType == 'text/html') {

          params.Message.Body = {
            Html: {
              Data: email.message,
              Charset: emailsMeta.charset
            }
          };
        } 
        else {

          params.Message.Body = {
            Text: {
              Data: email.message,
              Charset: emailsMeta.charset
            }
          };
        }

        // Send the email
        var ses = new aws.SES({
          "region": "us-east-1"
        });
        ses.sendEmail(params, function(err, data) {

          if (err) {
            console.error('Unable to send email due to an error: ' + err);
            callback(err);
          }

          sentEmails++;
          if (sentEmails == totalEmails) {
            next();
          }
        });
      }
    }
  ], 
  function (err) {

    if (err) {
        console.error('Unable to send emails due to an error: ' + err);
        callback(err);
    }

    // Success
    callback(null);
  });
};
</code></pre>

<p>Next, we must upload and configure the Lambda function to AWS, which involves:</p>

<ol>
<li>Creating an execution role granting Lambda permissions to access S3.</li>
<li>Creating a .zip package containing all the code, i.e. the Lambda function we are creating + all the required Node.js modules.</li>
<li>Uploading this package to AWS using a CLI tool.</li>
</ol>

<p>How to do these things is properly explained on the AWS site, on the .</p>

<h3 id="hooking-up-s3-with-the-lambda-function">Hooking Up S3 With The Lambda Function</h3>

<p>Finally, having the bucket and the Lambda function created, we need to hook both of them together, so that whenever there is a new object created on the bucket, it will trigger an event to execute the Lambda function. To do this, we go to the  and click on the bucket row, which will show its properties:</p>











<figure class="article__image break-out">
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8423da32-aad8-4175-bcf6-6433d4af2224/s3-dashboard-bucket-properties.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8423da32-aad8-4175-bcf6-6433d4af2224/s3-dashboard-bucket-properties.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8423da32-aad8-4175-bcf6-6433d4af2224/s3-dashboard-bucket-properties.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8423da32-aad8-4175-bcf6-6433d4af2224/s3-dashboard-bucket-properties.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8423da32-aad8-4175-bcf6-6433d4af2224/s3-dashboard-bucket-properties.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8423da32-aad8-4175-bcf6-6433d4af2224/s3-dashboard-bucket-properties.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8423da32-aad8-4175-bcf6-6433d4af2224/s3-dashboard-bucket-properties.jpg"
			sizes="100vw"
			alt="Displaying bucket properties inside the S3 dashboard"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Clicking on the bucket's row displays the bucket's properties. ()
		</figcaption>
	
</figure>


<p>Then clicking on Properties, we scroll down to the item &ldquo;Events&rdquo;, and there we click on Add a notification, and input the following fields:</p>

<ul>
<li><strong>Name:</strong> name of the notification, eg: &ldquo;EmailSender&rdquo;;</li>
<li><strong>Events:</strong> &ldquo;Put&rdquo;, which is the event triggered when a new object is created on the bucket;</li>
<li><strong>Send to:</strong> &ldquo;Lambda Function&rdquo;;</li>
<li><strong>Lambda:</strong> name of our newly created Lambda, eg: &ldquo;LambdaEmailSender&rdquo;.</li>
</ul>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e654a767-4f2d-4f3a-8202-49ac9b3e4ad0/setting-up-s3-lambda.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e654a767-4f2d-4f3a-8202-49ac9b3e4ad0/setting-up-s3-lambda.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e654a767-4f2d-4f3a-8202-49ac9b3e4ad0/setting-up-s3-lambda.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e654a767-4f2d-4f3a-8202-49ac9b3e4ad0/setting-up-s3-lambda.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e654a767-4f2d-4f3a-8202-49ac9b3e4ad0/setting-up-s3-lambda.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e654a767-4f2d-4f3a-8202-49ac9b3e4ad0/setting-up-s3-lambda.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/e654a767-4f2d-4f3a-8202-49ac9b3e4ad0/setting-up-s3-lambda.jpg"
			sizes="100vw"
			alt="Setting up S3 with Lambda"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Adding a notification in S3 to trigger an event for Lambda. ()
		</figcaption>
	
</figure>


<p>Finally, we can also set the S3 bucket to automatically delete the files containing the email data after some time. For this, we go to the Management tab of the bucket, and create a new Lifecycle rule, defining after how many days the emails must expire:</p>











<figure >
	<a href="https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7ddcdd6a-a3f2-4bd3-8b39-cc0107370dc2/lifecycle-rule.jpg">
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7ddcdd6a-a3f2-4bd3-8b39-cc0107370dc2/lifecycle-rule.jpg 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7ddcdd6a-a3f2-4bd3-8b39-cc0107370dc2/lifecycle-rule.jpg 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7ddcdd6a-a3f2-4bd3-8b39-cc0107370dc2/lifecycle-rule.jpg 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7ddcdd6a-a3f2-4bd3-8b39-cc0107370dc2/lifecycle-rule.jpg 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7ddcdd6a-a3f2-4bd3-8b39-cc0107370dc2/lifecycle-rule.jpg 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7ddcdd6a-a3f2-4bd3-8b39-cc0107370dc2/lifecycle-rule.jpg"
			sizes="100vw"
			alt="Lifecycle rule"
		/>
	</a>

	
		<figcaption class="op-vertical-bottom">
			Setting up a Lifecycle rule to automatically delete files from the bucket. ()
		</figcaption>
	
</figure>


<p>That&rsquo;s it. From this moment, when adding a new object on the S3 bucket with the content and meta for the emails, it will trigger the Lambda function, which will read the file and connect to SES to send the emails.</p>

<p>I implemented this solution on my site, and it became fast once again: by offloading sending emails to an external process, whether the applications send 20 or 5000 emails doesn&rsquo;t make a difference, the response to the user who triggered the action will be immediate.</p>

<h3 id="conclusion">Conclusion</h3>

<p>In this article we have analyzed why sending many transactional emails in a single request may become a bottleneck in the application, and created a solution to deal with the issue: instead of connecting to the SMTP server from within the application (synchronously), we can send the emails from an external function, asynchronously, based on a stack of AWS S3 + Lambda + SES.</p>

<p>By sending emails asynchronously, the application can manage to send thousands of emails, yet the response to the user who triggered the action will not be affected. However, to ensure that the user is not waiting for the email to arrive in the inbox, we also decided to split emails into two groups, priority and non-priority, and send only the non-priority emails asynchronously. We provided an implementation for WordPress, which is rather hacky due to the limitations of function <code>wp_mail</code> for sending emails.</p>

<p>A lesson from this article is that serverless functionalities on a server-based application work pretty well: sites running on a CMS like WordPress can improve their performance by implementing only specific features on the cloud, and avoid a great deal of complexity that comes from migrating highly dynamic sites to a fully serverless architecture.</p>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(rb, ra, yk, il)</span>
</div>


              </article>
            </body>
          </html>
---------------