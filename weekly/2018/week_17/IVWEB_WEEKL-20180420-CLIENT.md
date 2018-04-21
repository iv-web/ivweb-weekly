## 文章索引
1、 <a href="#1文章-ibm技术专家hyperleger-fabric-架构与部署实例解析" >文章： IBM技术专家：Hyperleger Fabric 架构与部署实例解析</a><br/>
2、 <a href="#2how-to-create-an-audio/video-recording-app-with-react-native:-an-in-depth-tutorial" >How To Create An Audio/Video Recording App With React Native: An In-Depth Tutorial</a><br/>
3、 <a href="#3文章-聊一聊事务的历史" >文章： 聊一聊事务的历史</a><br/>
4、 <a href="#4文章-apache-kylin实践链家数据分析引擎的演变史" >文章： Apache Kylin实践：链家数据分析引擎的演变史</a><br/>
5、 <a href="#5文章-新书问答agile-management" >文章： 新书问答：Agile Management</a><br/>
6、 <a href="#6视频演讲-visual-dlecharts与深度学习" >视频演讲： Visual-DL—ECharts与深度学习</a><br/>
7、 <a href="#7视频演讲-高可用容器云在前隆科技的实践" >视频演讲： 高可用容器云在前隆科技的实践</a><br/>
8、 <a href="#8从bat到tmd现在国内外一线架构师都在做什么" >从BAT到TMD，现在国内外一线架构师都在做什么？</a><br/>
9、 <a href="#9jakarta-ee工作组正式成立" >Jakarta EE工作组正式成立</a><br/>
10、 <a href="#10出海独角兽企业揭秘如何三招获得13亿用户" >出海独角兽企业揭秘：如何三招获得13亿用户</a><br/>
11、 <a href="#11微软azure-paas发展之路" >微软Azure PaaS发展之路</a><br/>
12、 <a href="#12kayenta来自netflix和google的开源金丝雀分析工具" >Kayenta：来自Netflix和Google的开源金丝雀分析工具</a><br/>
13、 <a href="#13d3发布50版本" >D3发布5.0版本</a><br/>
14、 <a href="#14实现创造协作和创新能力的软件工程" >实现创造、协作和创新能力的软件工程</a><br/>
15、 <a href="#15vivint大规模iot部署的指标收集" >Vivint大规模IoT部署的指标收集</a><br/>
16、 <a href="#16从instagram到facebook我总结了一份硅谷产品实战指南" >从Instagram到Facebook：我总结了一份硅谷产品实战指南</a><br/><h1 id="#title_0" >1、文章： IBM技术专家：Hyperleger Fabric 架构与部署实例解析</h1>
赵振华
[http://www.infoq.com/cn/articles/ibm-hyperleger-fabric-achitecture-deployment?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/ibm-hyperleger-fabric-achitecture-deployment?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/ibm-hyperleger-fabric-achitecture-deployment/zh/smallimage/GettyImages-544982936 copy-1524073551922.jpg"/><p>区块链前哨第五期社群分享“超级账本 Fabric 的架构与设计”，邀请了来自 IBM 的技术专家赵振华先生现场分享。本文根据分享内容整理而成。本文主要介绍 Hyperledger Fabric 的特性、架构与核心组件，并具体分析交易过程的实现，企业案例等内容。从技术角度介绍下 Hyperledger Fabric 是什么，其实现过程是怎样的。</p> <i>By 赵振华</i>
---------------
<h1 id="#title_1" >2、How To Create An Audio/Video Recording App With React Native: An In-Depth Tutorial</h1>
Oleh Mryhlod
[https://www.smashingmagazine.com/2018/04/audio-video-recording-react-native-expo/](https://www.smashingmagazine.com/2018/04/audio-video-recording-react-native-expo/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/04/audio-video-recording-react-native-expo/" />
              <title>How To Create An Audio/Video Recording App With React Native: An In-Depth Tutorial</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>How To Create An Audio/Video Recording App With React Native: An In-Depth Tutorial</h1>
                  
                    
                    <address>Oleh Mryhlod</address>
                  
                  <time datetime="2018-04-19T12:15:26&#43;02:00" class="op-published">2018-04-19T12:15:26+02:00</time>
                  <time datetime="2018-04-19T14:33:52&#43;00:00" class="op-modified">2018-04-19T14:33:52+00:00</time>
                </header>
                <p>React Native is a young technology, already gaining popularity among developers. It is a great option for smooth, fast, and efficient mobile app development. High-performance rates for mobile environments, code reuse, and a strong community: These are just some of the benefits React Native provides.</p>

<p>In this guide, I will share some insights about the high-level capabilities of React Native and the products you can develop with it in a short period of time.</p>

<p>We will delve into the step-by-step process of creating a video/audio recording app with React Native and .  Expo is an open-source toolchain built around React Native for developing iOS and Android projects with React and JavaScript. It provides a bunch of native APIs maintained by native developers and the open-source community.</p>

<p>After reading this article, you should have all the necessary knowledge to create video/audio recording functionality with React Native.</p>

<p>Let's get right to it.</p>

<h3>Brief Description Of The Application</h3>

<p>The application you will learn to develop is called a multimedia notebook. I have implemented part of this functionality in an online job board application for the film industry. The main goal of this mobile app is to connect people who work in the film industry with employers. They can create a profile, add a video or audio introduction, and apply for jobs.</p>

<p>The application consists of three main screens that you can switch between with the help of a tab navigator:</p>

<ul>
<li>the audio recording screen,</li>
<li>the video recording screen,</li>
<li>a screen with a list of all recorded media and functionality to play back or delete them.</li>
</ul>

<p><em>Check out how this app works by .</em></p>



<aside class="product-panel product-panel__tilted product-panel--book" data-audience="non-subscriber">
    <div class="container product-panel--book__container">
      <div class="panel__description panel__description--book">
    <p>Getting workflow <em>just</em> right ain't an easy task. So are proper estimates. Or alignment among different departments. That's why we've set up <strong>'this-is-how-I-work'-sessions</strong> — with smart cookies sharing what works well for them. A part of the , of course.</p>
      <a href="https://www.smashingmagazine.com/membership/" class="btn btn--green btn--large">
        Explore features&nbsp;→
      </a>
      </div>
      <div class="panel__image panel__image--book">
        <a href="https://www.smashingmagazine.com/membership/" class="books__book__image">
        <div class="books__book__img">
          <img src="https://www.smashingmagazine.com/images/smashing-cat/smashing-tv-box-cat.svg" alt="Smashing TV, with live sessions for professional designers and developers." width="310" height="400">
        </div>
      </a>
      </div>
    </div>
  </aside>





<div class="c-garfield-the-cat">


<p>First, download Expo to your mobile phone. There are two options to open the project :</p>

<ol>
<li>Open the link in the browser, scan the QR code with your mobile phone, and wait for the project to load.</li>
<li>Open the link with your mobile phone and click on “Open project using Expo”.</li>
</ol>

<p>You can also open the app in the browser. Click on “Open project in the browser”. If you have a paid account on , visit it and enter the code in the field to open the project. If you don’t have an account, click on “Open project” and wait in an account-level queue to open the project.</p>

<p>However, I recommend that you download the Expo app and open this project on your mobile phone to check out all of the features of the video and audio recording app.</p>

<p><em>You can find the full code for the media recording app in the  on GitHub.</em></p>

<h4>Dependencies Used For App Development</h4>

<p>As mentioned, the media recording app is developed with React Native and Expo.</p>

<p>You can see the full list of dependencies in the repository’s <code>package.json</code> file.</p>

<p>These are the main libraries used:</p>

<ul>
<li>React-navigation, for navigating the application,</li>
<li>Redux, for saving the application’s state,</li>
<li>React-redux, which are React bindings for Redux,</li>
<li>Recompose, for writing the components’ logic,</li>
<li>Reselect, for extracting the state fragments from Redux.</li>
</ul>

<p>Let's look at the project's structure:</p>











<figure >
	
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8d47762c-3e33-4bdf-a2c2-d0c4d66ff6f6/project-s-structure.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8d47762c-3e33-4bdf-a2c2-d0c4d66ff6f6/project-s-structure.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8d47762c-3e33-4bdf-a2c2-d0c4d66ff6f6/project-s-structure.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8d47762c-3e33-4bdf-a2c2-d0c4d66ff6f6/project-s-structure.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8d47762c-3e33-4bdf-a2c2-d0c4d66ff6f6/project-s-structure.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8d47762c-3e33-4bdf-a2c2-d0c4d66ff6f6/project-s-structure.png"
			sizes="70vw"
			alt=""
		/>
	

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<ul>
<li><code>src/index.js</code>: root app component imported in the <code>app.js</code> file;</li>
<li><code>src/components</code>: reusable components;</li>
<li><code>src/constants</code>: global constants;</li>
<li><code>src/styles</code>: global styles, colors, fonts sizes and dimensions.</li>
<li><code>src/utils</code>: useful utilities and recompose enhancers;</li>
<li><code>src/screens</code>: screens components;</li>
<li><code>src/store</code>: Redux store;</li>
<li><code>src/navigation</code>: application’s navigator;</li>
<li><code>src/modules</code>: Redux modules divided by entities as modules/audio, modules/video, modules/navigation.</li>
</ul>

<p>Let’s proceed to the practical part.</p>

<h3>Create Audio Recording Functionality With React Native</h3>

<p>First, it's important to сheck the . I recommend opening the code as you read this article to better understand the process.</p>

<p>When launching the application for the first time, you’ll need the user's permission for audio recording, which entails access to the microphone. Let's use <code>Expo.AppLoading</code> and ask permission for recording by using <code>Expo.Permissions</code> (see the <code>src/index.js</code>) during <code>startAsync</code>.</p>

<p><strong>Await</strong> <code>Permissions.askAsync(Permissions.AUDIO_RECORDING);</code></p>

<p>Audio recordings are displayed on a seperate screen whose UI changes depending on the state.</p>

<p>First, you can see the button “Start recording”. After it is clicked, the audio recording begins, and you will find the current audio duration on the screen. After stopping the recording, you will have to type the recording’s name and save the audio to the <strong>Redux store</strong>.</p>

<p>My audio recording UI looks like this:</p>











<figure >
	
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2d729edd-0fd1-40f5-bc89-3613b916eac1/audio-recording-ui.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2d729edd-0fd1-40f5-bc89-3613b916eac1/audio-recording-ui.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2d729edd-0fd1-40f5-bc89-3613b916eac1/audio-recording-ui.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2d729edd-0fd1-40f5-bc89-3613b916eac1/audio-recording-ui.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2d729edd-0fd1-40f5-bc89-3613b916eac1/audio-recording-ui.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/2d729edd-0fd1-40f5-bc89-3613b916eac1/audio-recording-ui.png"
			sizes="100vw"
			alt=""
		/>
	

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>I can save the audio in the <strong>Redux store</strong> in the following format:</p>

<pre><code class="language-javascript">audioItemsIds: [‘id1’, ‘id2’],
audioItems: {
 ‘id1’: {
    id: string,
    title: string,
    recordDate: date string,
    duration: number,
    audioUrl: string,
 }
},</code></pre>

<p>Let’s write the audio logic by using Recompose in the screen’s container <code>src/screens/RecordAudioScreenContainer</code>.</p>

<p>Before you start recording, customize the audio mode with the help of <code>Expo.Audio.set.AudioModeAsync</code> (mode), where mode is the dictionary with the following <strong>key-value pairs</strong>:</p>

<ul>
<li><code>playsInSilentModeIOS</code>: A boolean selecting whether your experience’s audio should play in silent mode on iOS. This value defaults to false.</li>
<li><code>allowsRecordingIOS</code>: A boolean selecting whether recording is enabled on iOS. This value defaults to false. Note: When this flag is set to true, playback may be routed to the phone receiver, instead of to the speaker.</li>
<li><code>interruptionModeIOS</code>: An enum selecting how your experience’s audio should interact with the audio from other apps on iOS.</li>
<li><code>shouldDuckAndroid</code>: A boolean selecting whether your experience’s audio should automatically be lowered in volume (“duck”) if audio from another app interrupts your experience. This value defaults to true. If false, audio from other apps will pause your audio.</li>
<li><code>interruptionModeAndroid</code>: An enum selecting how your experience’s audio should interact with the audio from other apps on Android.</li>
</ul>

<p><strong>Note</strong>: <em>You can learn more about the customization of <strong>AudioMode</strong> in .</em></p>

<p>I have used the following values in this app:</p>

<p><code>interruptionModeIOS: Audio.INTERRUPTION_MODE_IOS_DO_NOT_MIX</code>, &mdash; Our record interrupts audio from other apps on IOS.</p>

<p><code>playsInSilentModeIOS</code>: <strong>true</strong>,</p>

<p><code>shouldDuckAndroid</code>: <strong>true</strong>,</p>

<p><code>interruptionModeAndroid: Audio.INTERRUPTION_MODE_ANDROID_DO_NOT_MIX</code> &mdash; Our record interrupts audio from other apps on Android.</p>

<p><code>allowsRecordingIOS</code> Will change to true before the audio recording and to false after its completion.</p>

<p>To implement this, let's write the handler <code>setAudioMode</code> with <strong>Recompose</strong>.</p>

<pre class="break-out"><code class="language-javascript">withHandlers({
 setAudioMode: () => async ({ allowsRecordingIOS }) => {
   try {
     await Audio.setAudioModeAsync({
       allowsRecordingIOS,
       interruptionModeIOS: Audio.INTERRUPTION_MODE_IOS_DO_NOT_MIX,
       playsInSilentModeIOS: true,
       shouldDuckAndroid: true,
       interruptionModeAndroid: Audio.INTERRUPTION_MODE_ANDROID_DO_NOT_MIX,
     });
   } catch (error) {
     console.log(error) // eslint-disable-line
   }
 },
}),</code></pre>

<p>To record the audio, you’ll need to create an instance of the <code>Expo.Audio.Recording class</code>.</p>

<pre><code class="language-javascript">const recording = new Audio.Recording();</code></pre>

<p>After creating the recording instance, you will be able to receive the <strong>status of the Recording</strong> with the help of <code>recordingInstance.getStatusAsync()</code>.</p>

<p>The status of the recording is a dictionary with the following key-value pairs:</p>

<ul>
<li><code>canRecord:</code> a boolean.</li>
<li><code>isRecording:</code> a boolean describing whether the recording is currently recording.</li>
<li><code>isDoneRecording:</code> a boolean.</li>
<li><code>durationMillis:</code> current duration of the recorded audio.</li>
</ul>

<p>You can also set a function to be called at regular intervals with <code>recordingInstance.setOnRecordingStatusUpdate(onRecordingStatusUpdate).</code></p>

<p>To update the UI, you will need to call <code>setOnRecordingStatusUpdate</code> and set your own callback.</p>

<p>Let’s add some props and a recording callback to the container.</p>

<pre class="break-out"><code class="language-javascript">withStateHandlers({
    recording: null,
    isRecording: false,
    durationMillis: 0,
    isDoneRecording: false,
    fileUrl: null,
    audioName: '',
  }, {
    setState: () => obj => obj,
    setAudioName: () => audioName => ({ audioName }),
   recordingCallback: () => ({ durationMillis, isRecording, isDoneRecording }) =>
      ({ durationMillis, isRecording, isDoneRecording }),
  }),</code></pre>

<p>The callback setting for <code>setOnRecordingStatusUpdate</code> is:</p>

<p><code>recording.setOnRecordingStatusUpdate(props.recordingCallback);</code></p>

<p><code>onRecordingStatusUpdate</code> is called every 500 milliseconds by default. To make the UI update valid, set the 200 milliseconds interval with the help of <code>setProgressUpdateInterval</code>:</p>

<p><code>recording.setProgressUpdateInterval(200);</code></p>

<p>After creating an instance of this class, call <code>prepareToRecordAsync</code> to record the audio.</p>

<p><code>recordingInstance.prepareToRecordAsync(options)</code> loads the recorder into memory and prepares it for recording. It must be called before calling <code>startAsync()</code>. This method can be used if the <strong>recording instance</strong> has never been prepared.</p>


  <div id="sponsors-article" data-impression="true" class="c-promo-box c-promo-box--ad sponsors hidden" data-audience="non-subscriber" data-remove="true"></div>



<p>The parameters of this method include such options for the recording as sample rate, bitrate, channels, format, encoder and extension. You can find a list of all recording options in this .</p>

<p>In this case, let’s use <code>Audio.RECORDING_OPTIONS_PRESET_HIGH_QUALITY</code>.</p>

<p>After the recording has been prepared, you can start recording by calling the method <code>recordingInstance.startAsync()</code>.</p>

<p>Before creating a new <strong>recording instance</strong>, check whether it has been created before. <strong>The handler</strong> for beginning the recording looks like this:</p>

<pre class="break-out"><code class="language-javascript">onStartRecording: props => async () => {
      try {
        if (props.recording) {
          props.recording.setOnRecordingStatusUpdate(null);
          props.setState({ recording: null });
        }

        await props.setAudioMode({ allowsRecordingIOS: true });

        const recording = new Audio.Recording();
        recording.setOnRecordingStatusUpdate(props.recordingCallback);
        recording.setProgressUpdateInterval(200);

        props.setState({ fileUrl: null });

await recording.prepareToRecordAsync(Audio.RECORDING_OPTIONS_PRESET_HIGH_QUALITY);
        await recording.startAsync();

        props.setState({ recording });
      } catch (error) {
        console.log(error) // eslint-disable-line
      }
    },</code></pre>

<p>Now you need to write a <strong>handler</strong> for the audio recording completion. After clicking the stop button, you have to stop the recording, disable it on iOS, receive and save the local URL of the recording, and set <code>OnRecordingStatusUpdate</code> and the <strong>recording instance to null</strong>:</p>

<pre class="break-out"><code class="language-javascript">onEndRecording: props => async () => {
      try {
        await props.recording.stopAndUnloadAsync();
        await props.setAudioMode({ allowsRecordingIOS: false });
      } catch (error) {
        console.log(error); // eslint-disable-line
      }

      if (props.recording) {
        const fileUrl = props.recording.getURI();
        props.recording.setOnRecordingStatusUpdate(null);
        props.setState({ recording: null, fileUrl });
      }
    },</code></pre>

<p>After this, type the audio name, click the <strong>“continue”</strong> button, and the audio note will be saved in the <strong>Redux store</strong>.</p>

<pre><code class="language-javascript">onSubmit: props => () => {
      if (props.audioName && props.fileUrl) {
        const audioItem = {
          id: uuid(),
          recordDate: moment().format(),
          title: props.audioName,
          audioUrl: props.fileUrl,
          duration: props.durationMillis,
        };

        props.addAudio(audioItem);
        props.setState({
          audioName: '',
          isDoneRecording: false,
        });

        props.navigation.navigate(screens.LibraryTab);
      }
    },</code></pre>

<figure>)</figcaption></figure>

<h3>Audio Playback With React Native</h3>

<p>You can play the audio on the screen with the saved audio notes. To start the audio playback, click one of the items on the list. Below, you can see the audio player that allows you to track the current position of playback, to set the playback starting point and to toggle the playing audio.</p>

<p>Here’s what my audio playback UI looks like:</p>











<figure >
	
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d5dbf7c5-3b4b-463e-8bc5-37f842df6534/audio-playback-ui.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d5dbf7c5-3b4b-463e-8bc5-37f842df6534/audio-playback-ui.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d5dbf7c5-3b4b-463e-8bc5-37f842df6534/audio-playback-ui.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d5dbf7c5-3b4b-463e-8bc5-37f842df6534/audio-playback-ui.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d5dbf7c5-3b4b-463e-8bc5-37f842df6534/audio-playback-ui.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/d5dbf7c5-3b4b-463e-8bc5-37f842df6534/audio-playback-ui.png"
			sizes="100vw"
			alt=""
		/>
	

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p> share a unified imperative API for media playback.</p>

<p>Let's write the logic of the audio playback by using Recompose in the screen container <code>src/screens/LibraryScreen/LibraryScreenContainer</code>, as the audio player is available only on this screen.</p>

<p>If you want to display the player at any point of the application, I recommend writing the logic of the player and audio playback in <strong>Redux operations</strong> using <strong>redux-thunk</strong>.</p>

<p>Let's customize the audio mode in the same way we did for the audio recording. First, set <code>allowsRecordingIOS</code> to <strong>false</strong>.</p>

<pre class="break-out"><code class="language-javascript">lifecycle({
    async componentDidMount() {
      await Audio.setAudioModeAsync({
        allowsRecordingIOS: false,
        interruptionModeIOS: Audio.INTERRUPTION_MODE_IOS_DO_NOT_MIX,
        playsInSilentModeIOS: true,
        shouldDuckAndroid: true,
        interruptionModeAndroid: Audio.INTERRUPTION_MODE_ANDROID_DO_NOT_MIX,
      });
    },
  }),</code></pre>

<p>We have created the <strong>recording instance</strong> for audio recording. As for audio playback, we need to create the <strong>sound instance</strong>. We can do it in two different ways:</p>

<ol>
<li><code>const playbackObject = new Expo.Audio.Sound();</code></li>
<li><code>Expo.Audio.Sound.create(source, initialStatus = {}, onPlaybackStatusUpdate = null, downloadFirst = true)</code></li>
</ol>

<p>If you use the first method, you will need to call <code>playbackObject.loadAsync()</code>, which loads the media from source into memory and prepares it for playing, after creation of the instance.</p>

<p>The second method is a static convenience method to construct and load a sound. It сreates and loads a sound from source with the optional <code>initialStatus</code>, <code>onPlaybackStatusUpdate</code> and <code>downloadFirst</code> parameters.</p>

<p>The source parameter is the source of the sound. It supports the following forms:</p>

<ul>
<li>a dictionary of the form <code>{ uri: 'http://path/to/file' }</code> with a network URL pointing to an audio file on the web;</li>
<li><code>require('path/to/file')</code> for an audio file asset in the source code directory;</li>
<li>an  object for an audio file asset.</li>
</ul>

<p><code>The initialStatus</code> parameter is the initial playback status. <code>PlaybackStatus</code> is the structure returned from all playback API calls describing the state of the <code>playbackObject</code> at that point of time. It is a dictionary with the key-value pairs. You can check all of the keys of the <code>PlaybackStatus</code> in the .</p>

<p><code>onPlaybackStatusUpdate</code> is a function taking a single parameter, <code>PlaybackStatus</code>. It is called at regular intervals while the media is in the loaded state. The interval is 500 milliseconds by default. In my application, I set it to 50 milliseconds interval for a proper UI update.</p>

<p>Before creating the sound instance, you will need to implement the <code>onPlaybackStatusUpdate callback</code>. First, add some props to the screen container:</p>

<pre><code class="language-javascript">withClassVariableHandlers({
    playbackInstance: null,
    isSeeking: false,
    shouldPlayAtEndOfSeek: false,
    playingAudio: null,
  }, 'setClassVariable'),
  withStateHandlers({
    position: null,
    duration: null,
    shouldPlay: false,
    isLoading: true,
    isPlaying: false,
    isBuffering: false,
    showPlayer: false,
  }, {
    setState: () => obj => obj,
  }),</code></pre>

<p>Now, implement <code>onPlaybackStatusUpdate</code>. You will need to make several validations based on <code>PlaybackStatus</code> for a proper UI display:</p>

<pre class="break-out"><code class="language-javascript">withHandlers({
    soundCallback: props => (status) => {
      if (status.didJustFinish) {
        props.playbackInstance().stopAsync();
      } else if (status.isLoaded) {
        const position = props.isSeeking()
          ? props.position
          : status.positionMillis;
        const isPlaying = (props.isSeeking() || status.isBuffering)
          ? props.isPlaying
          : status.isPlaying;
        props.setState({
          position,
          duration: status.durationMillis,
          shouldPlay: status.shouldPlay,
          isPlaying,
          isBuffering: status.isBuffering,
        });
      }
    },
  }),</code></pre>

<p>After this, you have to implement a handler for the audio playback. If a sound instance is already created, you need to unload the media from memory by calling <code>playbackInstance.unloadAsync()</code> and clear <code>OnPlaybackStatusUpdate</code>:</p>

<pre class="break-out"><code class="language-javascript">loadPlaybackInstance: props => async (shouldPlay) => {
      props.setState({ isLoading: true });

      if (props.playbackInstance() !== null) {
        await props.playbackInstance().unloadAsync();
        props.playbackInstance().setOnPlaybackStatusUpdate(null);
        props.setClassVariable({ playbackInstance: null });
      }
      const { sound } = await Audio.Sound.create(
        { uri: props.playingAudio().audioUrl },
        { shouldPlay, position: 0, duration: 1, progressUpdateIntervalMillis: 50 },
        props.soundCallback,
      );

      props.setClassVariable({ playbackInstance: sound });

      props.setState({ isLoading: false });
    },</code></pre>

<p>Call the handler <code>loadPlaybackInstance(true)</code> by clicking the item in the list. It will automatically load and play the audio.</p>

<p>Let's add the pause and play functionality (toggle playing) to the audio player. If audio is already playing, you can pause it with the help of <code>playbackInstance.pauseAsync()</code>.  If audio is paused, you can resume playback from the paused point with the help of the <code>playbackInstance.playAsync()</code> method:</p>

<pre><code class="language-javascript">onTogglePlaying: props => () => {
      if (props.playbackInstance() !== null) {
        if (props.isPlaying) {
          props.playbackInstance().pauseAsync();
        } else {
          props.playbackInstance().playAsync();
        }
      }
    },</code></pre>

<p>When you click on the playing item, it should stop. If you want to stop audio playback and put it into the 0 playing position, you can use the method <code>playbackInstance.stopAsync()</code>:</p>

<pre><code class="language-javascript">onStop: props => () => {
      if (props.playbackInstance() !== null) {
        props.playbackInstance().stopAsync();

        props.setShowPlayer(false);
        props.setClassVariable({ playingAudio: null });
      }
    },</code></pre>

<p>The audio player also allows you to rewind the audio with the help of the slider. When you start sliding, the audio playback should be paused with <code>playbackInstance.pauseAsync()</code>.</p>

<p>After the sliding is complete, you can set the audio playing position with the help of <code>playbackInstance.setPositionAsync(value)</code>, or play back the audio from the set position with <code>playbackInstance.playFromPositionAsync(value)</code>:</p>

<pre class="break-out"><code class="language-javascript">onCompleteSliding: props => async (value) => {
      if (props.playbackInstance() !== null) {
        if (props.shouldPlayAtEndOfSeek) {
          await props.playbackInstance().playFromPositionAsync(value);
        } else {
          await props.playbackInstance().setPositionAsync(value);
        }
        props.setClassVariable({ isSeeking: false });
      }
    },</code></pre>

<p>After this, you can pass the props to the components <code>MediaList</code> and <code>AudioPlayer</code> (see the file <code>src/screens/LibraryScreen/LibraryScreenView</code>).</p>

<figure></figure>

<h3>Video Recording Functionality With React Native</h3>

<p>Let's proceed to video recording.</p>

<p>We’ll use <code>Expo.Camera</code> for this purpose. <code>Expo.Camera</code> is a React component that renders a preview of the device’s front or back camera. <code>Expo.Camera</code> can also take photos and record videos that are saved to the app’s cache.</p>

<p>To record video, you need permission for access to the camera and microphone. Let's add the request for camera access as we did with the audio recording (in the file <code>src/index.js</code>):</p>

<pre><code class="language-javascript">await Permissions.askAsync(Permissions.CAMERA);</code></pre>

<p>Video recording is available on the “Video Recording” screen. After switching to this screen, the camera will turn on.</p>

<p>You can change the camera type (front or back) and start video recording. During recording, you can see its general duration and can cancel or stop it. When recording is finished, you will have to type the name of the video, after which it will be saved in the <strong>Redux store</strong>.</p>

<p>Here is what my video recording UI looks like:</p>











<figure >
	
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c3bceb69-985d-4765-bf48-e32b347e510e/video-recording-ui.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c3bceb69-985d-4765-bf48-e32b347e510e/video-recording-ui.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c3bceb69-985d-4765-bf48-e32b347e510e/video-recording-ui.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c3bceb69-985d-4765-bf48-e32b347e510e/video-recording-ui.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c3bceb69-985d-4765-bf48-e32b347e510e/video-recording-ui.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/c3bceb69-985d-4765-bf48-e32b347e510e/video-recording-ui.png"
			sizes="100vw"
			alt=""
		/>
	

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>Let’s write the video recording logic by using Recompose on the container screen

<code>src/screens/RecordVideoScreen/RecordVideoScreenContainer</code>.</p>

<p>You can see the full list of all props in the <code>Expo.Camera</code> component in .</p>

<p>In this application, we will use the following props for <code>Expo.Camera</code>.</p>

<ul>
<li><code>type</code>: The camera type is set (front or back).</li>
<li><code>onCameraReady</code>: This callback is invoked when the camera preview is set. You won't be able to start recording if the camera is not ready.</li>
<li><code>style</code>: This sets the styles for the camera container. In this case, the size is 4:3.</li>
<li><code>ref</code>: This is used for direct access to the camera component.</li>
</ul>

<p>Let's add the variable for saving the type and handler for its changing.</p>

<pre><code class="language-javascript">cameraType: Camera.Constants.Type.back,
toggleCameraType: state => () => ({
      cameraType: state.cameraType === Camera.Constants.Type.front
        ? Camera.Constants.Type.back
        : Camera.Constants.Type.front,
    }),</code></pre>

<p>Let's add the variable for saving the camera ready state and callback for <code>onCameraReady</code>.</p>

<pre><code class="language-javascript">isCameraReady: false,

setCameraReady: () => () => ({ isCameraReady: true }),</code></pre>

<p>Let's add the variable for saving the camera component reference and setter.</p>

<pre><code class="language-javascript">cameraRef: null,

setCameraRef: () => cameraRef => ({ cameraRef }),</code></pre>

<p>Let's pass these variables and handlers to the camera component.</p>

<pre><code class="language-javascript">&lt;Camera
          type={cameraType}
          onCameraReady={setCameraReady}
          style={s.camera}
          ref={setCameraRef}
        /></code></pre>

<p>Now, when calling <code>toggleCameraType</code> after clicking the button, the camera will switch from the front to the back.</p>

<p>Currently, we have access to the camera component via the reference, and we can start video recording with the help of <code>cameraRef.recordAsync()</code>.</p>

<p>The method <code>recordAsync</code> starts recording a video to be saved to the cache directory.</p>

<h5>Arguments:</h5>

<p>Options (object) &mdash; a map of options:</p>

<ul>
<li><code>quality</code> (VideoQuality): Specify the quality of recorded video. Usage: Camera.Constants.VideoQuality['<value>'], possible values: for 16:9 resolution 2160p, 1080p, 720p, 480p (Android only) and for 4:3 (the size is 640x480). If the chosen quality is not available for the device, choose the highest one.</li>
<li><code>maxDuration</code> (number): Maximum video duration in seconds.</li>
<li><code>maxFileSize</code> (number): Maximum video file size in bytes.</li>
<li><code>mute</code> (boolean): If present, video will be recorded with no sound.</li>
</ul>

<p><code>recordAsync</code> returns a promise that resolves to an object containing the video file’s URI property. You will need to save the file’s URI in order to play back the video hereafter. The promise is returned if <code>stopRecording</code> was invoked, one of <code>maxDuration</code> and <code>maxFileSize</code> is reached or the camera preview is stopped.</p>

<p>Because the ratio set for the camera component sides is 4:3, let's set the same format for the video quality.</p>

<p>Here is what the handler for starting video recording looks like (see the full code of the container in the repository):</p>

<pre class="break-out"><code class="language-javascript">onStartRecording: props => async () => {
      if (props.isCameraReady) {
        props.setState({ isRecording: true, fileUrl: null });
        props.setVideoDuration();
        props.cameraRef.recordAsync({ quality: '4:3' })
          .then((file) => {
            props.setState({ fileUrl: file.uri });
          });
      }
    },</code></pre>

<p>During the video recording, we can’t receive the recording status as we have done for audio. That's why I have created a function to set video duration.</p>

<p>To stop the video recording, we have to call the following function:</p>

<pre><code class="language-javascript">stopRecording: props => () => {
      if (props.isRecording) {
        props.cameraRef.stopRecording();
        props.setState({ isRecording: false });
        clearInterval(props.interval);
      }
    },</code></pre>

<p>Check out the entire process of video recording.</p>

<figure></figure>

<h3>Video Playback Functionality With React Native</h3>

<p>You can play back the video on the “Library” screen. Video notes are located in the “Video” tab.</p>

<p>To start the video playback, click the selected item in the list. Then, switch to the playback screen, where you can watch or delete the video.</p>

<p>The UI for video playback looks like this:</p>











<figure >
	
		<img
			srcset="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/52f5acaf-2a76-4cae-bea1-17cb3a3b090a/video-playback-ui.png 400w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_800/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/52f5acaf-2a76-4cae-bea1-17cb3a3b090a/video-playback-ui.png 800w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1200/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/52f5acaf-2a76-4cae-bea1-17cb3a3b090a/video-playback-ui.png 1200w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_1600/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/52f5acaf-2a76-4cae-bea1-17cb3a3b090a/video-playback-ui.png 1600w,
			        https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_2000/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/52f5acaf-2a76-4cae-bea1-17cb3a3b090a/video-playback-ui.png 2000w"
			src="https://res.cloudinary.com/indysigner/image/fetch/f_auto,q_auto/w_400/https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/52f5acaf-2a76-4cae-bea1-17cb3a3b090a/video-playback-ui.png"
			sizes="100vw"
			alt=""
		/>
	

	
		<figcaption class="op-vertical-bottom">
			
		</figcaption>
	
</figure>


<p>To play back the video, use <code>Expo.Video</code>, a component that displays a video inline with the other React Native UI elements in your app.</p>

<p>The video will be displayed on the separate screen, PlayVideo.</p>

<p>You can check out all of the .</p>

<p>In our application, the <code>Expo.Video</code> <strong>component</strong> uses native playback controls and looks like this:</p>

<pre><code class="language-javascript">&lt;Video
        source={{ uri: videoUrl }}
        style={s.video}
        shouldPlay={isPlaying}
        resizeMode="contain"
        useNativeControls={isPlaying}
        onLoad={onLoad}
        onError={onError}
      /></code></pre>

<ul>
<li><code>source</code><br />

This is the source of the video data to display. The same forms as for Expo.Audio.Sound are supported.</li>
<li><code>resizeMode</code><br />

This is a string describing how the video should be scaled for display in the component view’s bounds. It can be “stretch”, “contain” or “cover”.</li>
<li><code>shouldPlay</code><br />

This boolean describes whether the media is supposed to play.</li>
<li><code>useNativeControls</code><br />

This boolean, if set to true, displays native playback controls (such as play and pause) within the video component.</li>
<li><code>onLoad</code><br />

This function is called once the video has been loaded.</li>
<li><code>onError</code><br />

This function is called if loading or playback has encountered a fatal error. The function passes a single error message string as a parameter.</li>
</ul>

<p>When the video is uploaded, the play button should be rendered on top of it.</p>

<p>When you click the play button, the video turns on and the native playback controls are displayed.</p>

<p>Let’s write the logic of the video using Recompose in the screen container <code>src/screens/PlayVideoScreen/PlayVideoScreenContainer</code>:</p>

<pre class="break-out"><code class="language-javascript">const defaultState = {
  isError: false,
  isLoading: false,
  isPlaying: false,
};

const enhance = compose(
  paramsToProps('videoUrl'),
  withStateHandlers({
    ...defaultState,
    isLoading: true,
  }, {
    onError: () => () => ({ ...defaultState, isError: true }),
    onLoad: () => () => defaultState,
   onTogglePlaying: ({ isPlaying }) => () => ({ ...defaultState, isPlaying: !isPlaying }),
  }),
);</code></pre>

<p>As previously mentioned, the <code>Expo.Audio.Sound</code> objects and <code>Expo.Video</code> components share a unified imperative API for media playback. That's why you can create custom controls and use more advanced functionality with the Playback API.</p>

<p>Check out the video playback process:</p>

<figure></figure>

<p>See the full code for the application in the .</p>

<p>You can also install the app on your phone by using  and check out how it works in practice.</p>

<h3>Wrapping Up</h3>

<p>I hope you have enjoyed this article and have enriched your knowledge of React Native. You can use this audio and video recording tutorial to create your own custom-designed media player. You can also scale the functionality and add the ability to save media in the phone’s memory or on a server, synchronize media data between different devices, and share media with others.</p>

<p>As you can see, there is a wide scope for imagination. If you have any questions about the process of developing an audio or video recording app with React Native, feel free to drop a comment below.</p>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(da, lf, ra, yk, al, il)</span>
</div>



  <div id="sponsors-article-end" data-impression="true" class="c-promo-box c-promo-box--ad c-promo-box--wide sponsors hidden" data-audience="non-subscriber" data-remove="true"></div>



</div>



              </article>
            </body>
          </html>
---------------
<h1 id="#title_2" >3、文章： 聊一聊事务的历史</h1>
Arjun Narayan
[http://www.infoq.com/cn/articles/history_transaction_histories?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/history_transaction_histories?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/history_transaction_histories/zh/smallimage/image_fences-1524155481069.jpg"/><p>本文简述了事务不同隔离级别的历史，并阐述了不同时期，业界对串行化事务隔离级别的认识。</p> <i>By Arjun Narayan</i> <i> Translated by 周元昊</i>
---------------
<h1 id="#title_3" >4、文章： Apache Kylin实践：链家数据分析引擎的演变史</h1>
王龙帅, 张如松
[http://www.infoq.com/cn/articles/lianjia-data-analysis-apache-kylin?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/lianjia-data-analysis-apache-kylin?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/lianjia-data-analysis-apache-kylin/zh/smallimage/logo (7)-1524154925760.jpg"/><p>伴随链家业务线的拓宽和发展，以及数据生态的建设，数据规模快速增长。2015年大数据部门成立至今，集群数据存储量为 9PB，服务器规模为 200 台 +。与此同时，数据需求也随着业务的发展落地不断增长，如统计分析、指标 API、运营报表等，不同业务需求差异较大，维度越来越多，需要定制化开发。面对数十亿行级别的数据，低延迟响应的特性，保障服务稳定、数据准确，链家的数据分析引擎经历了如下的发展历程。</p> <i>By 王龙帅</i>
---------------
<h1 id="#title_4" >5、文章： 新书问答：Agile Management</h1>
Ben Linders
[http://www.infoq.com/cn/articles/book-review-agile-management-hoogveld?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/book-review-agile-management-hoogveld?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/book-review-agile-management-hoogveld/zh/smallimage/book-agile-cover-1523567530011.jpg"/><p>Mike Hoogveld所著的《敏捷管理》（Agile Management）一书，探讨了为提高组织内的灵活性和创业精神，应如何以敏捷方式实现敏捷的原则和价值观。此外，该书还介绍了如何以“客户的声音”为出发点，设计提供给客户的产品、服务、渠道和流程。</p> <i>By Ben Linders</i> <i> Translated by 盖磊</i>
---------------
<h1 id="#title_5" >6、视频演讲： Visual-DL—ECharts与深度学习</h1>
李德清
[http://www.infoq.com/cn/presentations/visual-dl-echarts-and-deep-learning?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/visual-dl-echarts-and-deep-learning?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/presentations/visual-dl-echarts-and-deep-learning/zh/mediumimage/lideqing270-1523800951299.jpg"/><p>Visual DL为百度深度学习可视化平台，可以通过可视化的方法将模型训练过程中的各个参数以及计算的数据流图实时地展现出来，以帮助模型训练者更好地理解、调试、优化模型。本次分享将结合我们在Visual DL项目的实践经验，介绍我们在深度学习领域是如何使用可视化来解决一些问题。</p> <i>By 李德清</i>
---------------
<h1 id="#title_6" >7、视频演讲： 高可用容器云在前隆科技的实践</h1>
朱轶坤
[http://www.infoq.com/cn/presentations/the-practice-of-high-availability-container-cloud-in-mobanker?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/presentations/the-practice-of-high-availability-container-cloud-in-mobanker?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/presentations/the-practice-of-high-availability-container-cloud-in-mobanker/zh/mediumimage/zhuyikun_270-1524137158607.jpg"/><p>前隆容器云平台是前隆科技技术运营中心 DevOps 团队基于 Docker 容器技术开发的一套应用服务管理平台，支持应用服务按需扩展、秒级伸缩，友好的用户交互过程，规范化的应用部署流程，旨在将开发、测试、运维人员从各环境的服务部署、应用配置、资源管理中解放出来，并同时保证平台的健壮与可用性。此次演讲旨在和大家分享在前隆容器云平台实施过程中的相关容器技术实践。</p> <i>By 朱轶坤</i>
---------------
<h1 id="#title_7" >8、从BAT到TMD，现在国内外一线架构师都在做什么？</h1>
David
[http://www.infoq.com/cn/news/2018/04/BATtoTMD?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/04/BATtoTMD?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>最近几年，耳熟能详的"BAT"都在大谈基础设施转型，例如百度的 Apollo 自动驾驶平台，例如提供计算和数据处理能力的阿里云，例如定位为合作伙伴提供连接一切能力的微信。但当看似“BAT”的体量与技术能力达到了中国互联网的上限时，后起之秀如"TMD"（头条、美团、滴滴）以各自深耕多年的技术底蕴和业务体系也成了一方巨擘。</p> <i>By David</i>
---------------
<h1 id="#title_8" >9、Jakarta EE工作组正式成立</h1>
Matt Raible
[http://www.infoq.com/cn/news/2018/04/jakarta-ee-working-group?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/04/jakarta-ee-working-group?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>未来的Java EE技术将被命名为Jakarta EE，目前Eclipse基金会正在积极开发当中。Java EE还在甲骨文管辖之下时，甲骨文通过JCP（Java Community Process）来做出决策并引入新功能。由于Eclipse基金会没有用于Java EE的JCP，因此必须建立新的进程，也就是Jakarta EE工作组。</p> <i>By Matt Raible</i> <i> Translated by 无明</i>
---------------
<h1 id="#title_9" >10、出海独角兽企业揭秘：如何三招获得13亿用户</h1>
贾凯强
[http://www.infoq.com/cn/news/2018/04/SHAREit-User?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/04/SHAREit-User?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>互联网时代的典型特征是信息流爆炸，用户传播和增长速度呈现指数上升，但由于竞争的逐步加剧，获得用户这件事正在变得越发艰难，那么如何才能让产品快速获得用户呢？笔者有幸找到了一家精于此道的企业 SHAREit（茄子快传），他们在短短的时间里获得了 13亿用户，那么这背后藏着怎样的秘密呢？</p> <i>By 贾凯强</i>
---------------
<h1 id="#title_10" >11、微软Azure PaaS发展之路</h1>
张婵
[http://www.infoq.com/cn/news/2018/04/azure-paas?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/04/azure-paas?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>云计算通常包括IaaS, SaaS和PaaS三个层面，相较于已成气候的IaaS和SaaS，最近几年云计算领域的集中发力点在PaaS层面。微软作为全球老牌IT巨头，也是PaaS供应商的领导者。微软的PaaS之路是怎么一步步发展起来的？对此我们专访了微软Azure资深架构师Steven，来了解微软Azure PaaS的发展之路。</p> <i>By 张婵</i>
---------------
<h1 id="#title_11" >12、Kayenta：来自Netflix和Google的开源金丝雀分析工具</h1>
Abel Avram
[http://www.infoq.com/cn/news/2018/04/kayenta?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/04/kayenta?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Kayenta是一种开源的自动金丝雀分析工具，用于评估新版本软件产品的准备良好程度。</p> <i>By Abel Avram</i> <i> Translated by 盖磊</i>
---------------
<h1 id="#title_12" >13、D3发布5.0版本</h1>
Dylan Schiemann
[http://www.infoq.com/cn/news/2018/04/d3-releases-5-async?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/04/d3-releases-5-async?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>D3团队发布了5.0版本，引入了一些比较新的异步模式，例如promises和fetch，并更新了一些关键的可视化API。</p> <i>By Dylan Schiemann</i> <i> Translated by 张健欣</i>
---------------
<h1 id="#title_13" >14、实现创造、协作和创新能力的软件工程</h1>
Ben Linders
[http://www.infoq.com/cn/news/2018/04/software-engineering?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/04/software-engineering?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>软件工程作为一门学科，必须基于反馈、增量、实验和经验做不断迭代。仅有工匠精神是不够的，工程是一种增强创造、协作和创新能力的放大器。工程原则是持续交付的基石。</p> <i>By Ben Linders</i> <i> Translated by 盖磊</i>
---------------
<h1 id="#title_14" >15、Vivint大规模IoT部署的指标收集</h1>
Hrishikesh Barua
[http://www.infoq.com/cn/news/2018/04/metrics-iot-vivint?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/04/metrics-iot-vivint?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>Vivint工程团队构建了自己的指标收集平台，用于收集和分析他们部署的设备上的指标。他们之所以编写自己的系统是希望能够只存储聚合数据，并集中精力分析这些数据，这是通过Rothko项目实现的。</p> <i>By Hrishikesh Barua</i> <i> Translated by 谢丽</i>
---------------
<h1 id="#title_15" >16、从Instagram到Facebook：我总结了一份硅谷产品实战指南</h1>
曲晓音
[http://www.infoq.com/cn/news/2018/04/instagram-facebook-product?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/04/instagram-facebook-product?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>从Instagram到Facebook，我总结了一份硅谷产品实战指南。</p> <i>By 曲晓音</i>
---------------