## 文章索引
1、 <a href="#1use-cases-for-flexbox" >Use Cases For Flexbox</a><br/>
2、 <a href="#2文章-可扩展性dapp极速前进" >文章： 可扩展性DApp：极速前进！</a><br/>
3、 <a href="#3java-11已经发布" >Java 11已经发布</a><br/><h1 id="#title_0" >1、Use Cases For Flexbox</h1>
Rachel Andrew
[https://www.smashingmagazine.com/2018/10/flexbox-use-cases/](https://www.smashingmagazine.com/2018/10/flexbox-use-cases/)
<html>
            <head>
              <meta charset="utf-8">
              <link rel="canonical" href="https://www.smashingmagazine.com/2018/10/flexbox-use-cases/" />
              <title>Use Cases For Flexbox</title>
            </head>
            <body>
              <article>
                <header>
                  <h1>Use Cases For Flexbox</h1>
                  
                    
                    <address>Rachel Andrew</address>
                  
                  <time datetime="2018-10-04T13:50:30&#43;02:00" class="op-published">2018-10-04T13:50:30+02:00</time>
                  <time datetime="2018-10-04T16:56:41&#43;00:00" class="op-modified">2018-10-04T16:56:41+00:00</time>
                </header>
                

<p>We come to the final part in my Flexbox series here at Smashing Magazine. In this post, I am going to spend some time thinking about what the use cases for Flexbox really are, given that we now have CSS Grid Layout, giving some suggestions for what you might use when and a way to decide.</p>

<h3 id="earlier-in-this-series">Earlier In This Series</h3>

<p>If you haven’t picked up the other articles yet, this is essentially a concluding post so check those out first. I began by describing , and how the browser figures out how big a flex item should be. Now that we know exactly how Flexbox works, we can wrap up by thinking about the use cases it is best for.</p>

<h3 id="should-i-use-grid-or-flexbox">Should I Use Grid Or Flexbox?</h3>

<p>This is still the top question that I’m asked when teaching layout, and in general, I find that as people become more used to working with newer layout methods, it becomes a question you need to ask yourself less. As you build more components you will get a feel for which layout method to use.</p>

<p>If you are just getting to grips with the idea, however, the thing to remember is that <strong>both CSS Grid Layout and Flexbox are both CSS</strong>. Whether you have specified <code>display: grid</code> or <code>display: flex</code>, you often use more that is common than is different. Both Grid and Flexbox use the properties which are part of the Box Alignment specification; they both draw on concepts detailed in CSS Intrinsic and Extrinsic Sizing.</p>

<p>Asking whether your design should use Grid <em>or</em> Flexbox is a bit like asking if your design should use font-size <em>or</em> color. You should probably use both, as required. And, no-one is going to come to chase you if you use the <em>wrong</em> one.</p>



  <aside class="product-panel product-panel__tilted product-panel--book" data-audience="non-subscriber">
    <div class="container product-panel--book__container">
      <div class="panel__description panel__description--book">

    <p>Meet .</p>
    <a href="https://smashed.by/confpanelspeakers" class="btn btn--green btn--large">
      Check all topics&nbsp;and&nbsp;speakers&nbsp;↬
    </a>
      </div>
      <div class="panel__image panel__image--book">

  <a href="https://www.smashingconf.com/ny-2018/" class="books__book__image">
  <div class="books__book__img">
          <img src="https://www.smashingmagazine.com/images/smashing-cat/cat-scubadiving-panel.svg" alt="Smashing TV, with live sessions for professional designers and developers." width="310" height="400">
        </div>
      </a>
      </div>
    </div>
  </aside>




<p>So, we are not picking between Vue.js and React, Bootstrap or Foundation. We are using CSS to do layout, and we need to use the bits of CSS which make most sense for the particular bit of our design that we are working on. Consider each component, and decide what is best for it, or what combination of things are best for it.</p>

<p>That might be Grid, or it might be Flexbox. It might be a grid outer container with some of your grid items becoming flex items or the reverse. There is no issue in nesting a grid inside a flex item if that is what your design calls for.</p>

<h3 id="what-is-flexbox-really-for">What Is Flexbox Really For?</h3>

<p>The Flexbox specification describes the layout method like this,</p>

<blockquote>“Flex layout is superficially similar to block layout. It lacks many of the more complex text- or document-centric properties that can be used in block layout, such as floats and columns. In return, it gains simple and powerful tools for distributing space and aligning content in ways that web apps and complex web pages often need.”</blockquote>

<p>I think the key phrase here is “distributing space and aligning content”. Flexbox is all about taking a bunch of things (which have varying sizes) and fitting them into a container (which itself has a varying size). Flexbox is squishy. Flexbox tries to create the best possible layout for our items, giving bigger items more space and smaller items less space, thus preserving readability of content.</p>

<p>When people find Flexbox hard and weird, it is often because they are trying to use Flexbox as a grid system &mdash; trying to take back control over sizing and space distribution. When you do this, Flexbox can seem weird and hard as you are fighting against the very thing that makes it Flexbox, i.e. that inherent flexibility.</p>

<p>Therefore, patterns which suit flex layout very well are those where we are not so interested in having a pixel-perfect size for each item. We just want those items to display well alongside each other.</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="EdPjgE"
   data-user="rachelandrew"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<p>There are also patterns where you want to have wrapped lines, however, you do not want a strict grid. If we take the seminal grid versus the Flexbox example where we use the repeat auto-fill syntax in grid, and then a flex container with wrapped flex lines. Here we immediately see the difference between the two methods.</p>

<div class="sponsors__wide-place"></div>




<p>In the grid example, the grid items line up in rows and columns. While the number of column tracks changes (depending on space), the items always go into the next grid cell that is available. In fact, there is no way to ask a grid item to span tracks if there are some empty cells to fill in that auto-flow scenario.</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="LgGVyX"
   data-user="rachelandrew"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<p>In the flex example, the final items share any space left over between them; this way, we do not have alignment horizontally and vertically.</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="vVLOZq"
   data-user="rachelandrew"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<p>If we have a flex-basis of auto and any of the flex items are larger, they will also be given more space so that the alignment could be quite different line by line.</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="JmGdEa"
   data-user="rachelandrew"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<p>This then is a very clear example of where we would want to use Flexbox over Grid Layout. If we want the items to wrap but to take up the space they need on a line-by-line basis. That is a very different kind of layout to a grid. Patterns like this might be a set of tags (one or two-word elements that you wish to display nicely as a set of items), taking up the space they need and not rigidly being forced into a strict grid.</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="EdPVNz"
   data-user="rachelandrew"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<p>At the present time, Flexbox is also the best way to perform vertical and horizontal centering of an item inside a container.</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="BqjoxY"
   data-user="rachelandrew"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<p>In the future (when there is browser support for the Box Alignment properties outside of flex layout), we may be able to do this without needing to add <code>display: flex</code> to the container. For now, however, that is what you need to do &mdash; that extra line of CSS is really not an issue.</p>

<p>Flexbox is very good at dealing with small, one-dimensional components. Sets of form fields, icons, or other information can be easily laid out and allowed to be flexible without needing to carefully set the sizing on each item.</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="vVLNbZ"
   data-user="rachelandrew"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<p>You might also choose Flexbox in a scenario where all you need to do is cause content at the bottom of a layout to stick to the bottom of a container rather than popping up. In this example, I make the container a flex container by displaying the contents as a column, then allowing the middle to grow by pushing the footer to the bottom of the component.</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="xyZYwY"
   data-user="rachelandrew"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<p>In production, I am finding that Flexbox is useful for lots of little jobs, making sure that things align properly, that space is shared out nicely between items. You could absolutely use a one-dimensional grid container for some of those things, and don’t worry about it if that is what you decide to do.</p>

<p>What I think Flexbox does very well, however, is to cope with the situation where extra items might need to be added that I didn’t expect in my design. For example, if I have a navigation component using Grid I would be creating enough tracks for all items, as I wouldn’t want a new row to be created if I had &ldquo;too many&rdquo; items. With flexbox, as long as I was allowing the items to be flexible from a flex-basis of 0 (or auto) then the items would allow their new companion into the row and make space for it.</p>

<div class="sponsors__wide-place"></div>




<h3 id="when-should-i-not-use-flexbox">When Should I <em>Not</em> Use Flexbox?</h3>

<p>We have looked at some of the reasons that I think you should choose Flexbox over Grid Layout, so we can now look at some of the places where Flexbox might not be the best choice. We have already looked at our Flexbox versus grid example with items aligned horizontally and vertically versus items which take up space line by line. And, that distinction is the first thing to consider.</p>

<p>The grid example is of two-dimensional layout. Layout in rows and columns at the same time. The Flexbox example is one-dimensional layout. We have wrapped flex lines but space distribution is happening on a line by line basis. Each line is essentially acting as a new flex container in the flex-direction.</p>

<p>Therefore, if your component needs two-dimensional layout, you would be better placed to use Grid over Flexbox. It doesn’t matter whether your component is large or small. If you take one thing from this article, it is to remove the idea from your brain that Grid is somehow only meant for main page layout, and Flexbox for components. You can have a tiny component that requires two-dimensional layout, and main page structures which better suit one-dimensional layout.</p>

<p>Another good point at which Grid may be considered the better solution is if you are applying a width, or a flex-basis set as a length unit to your flex items in order to line them up with another row of flex items, or just to restrict the flexibility in some way. Quite often that indicates either than you really need a two-dimensional layout method or that the control from the container of grid would suit your layout better.</p>

<p>For example, we could make our flex layout display more like a grid, by restricting the flexibility of our items. Setting flex-grow to 0 and sizing the items with percentages, in a similar way to the way we would size items in a floated “grid”. If you find that you are doing that, I would suggest that Grid Layout is a much better approach as it is designed for this type of layout.</p>

<p data-height="500"
   data-theme-id="light"
   data-slug-hash="jeWZyM"
   data-user="rachelandrew"
   data-default-tab="result"
   class='codepen'>See the Pen .</p>


<p>With all that said, remember that there is very often not a clear right <em>or</em> wrong answer. Sometimes the only thing you can do is to try different ways and see what suits the component best. Remember that you can also switch layout methods, using Flexbox at one breakpoint and Grid at another.</p>

<h3 id="and-that-s-a-flex-wrap">And That’s A (Flex) Wrap!</h3>

<p>I hope this series on Flexbox has been helpful and demonstrated how understanding some of the logic behind alignment and sizing of flex items, makes life easier when working with it. If you are left with any outstanding questions or have a pattern which seems not to have an obvious answer in terms of the layout method to use, post a comment.</p>

<div class="signature">
  <img src="https://www.smashingmagazine.com/images/logo/logo--red.png" alt="Smashing Editorial">
  <span>(il)</span>
</div>


              </article>
            </body>
          </html>
---------------
<h1 id="#title_1" >2、文章： 可扩展性DApp：极速前进！</h1>
Yoav Vilner
[http://www.infoq.com/cn/articles/the-amazing-race-for-scalable-dapps?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/articles/the-amazing-race-for-scalable-dapps?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="https://res.infoq.com/articles/the-amazing-race-for-scalable-dapps/zh/smallimage/GettyImages-628837052-1518704902676-1537695774413.jpeg"/><p>进击吧，可扩展性DApp！</p> <i>By Yoav Vilner</i> <i> Translated by 刘志勇</i>
---------------
<h1 id="#title_2" >3、Java 11已经发布</h1>
Ben Evans
[http://www.infoq.com/cn/news/2018/10/java11-released?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global](http://www.infoq.com/cn/news/2018/10/java11-released?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
<img src="http://www.infoq.com/styles/i/logo_bigger.jpg"/><p>ava 11终于推出了，它是Oracle在推行LTS（长期支持，Long-Term Support）后首个按计划推出的版本。虽然Oracle出于缩小旧版本模型和新方法间差距的考虑，也将早期的Java 8纳入到LTS发布中。</p> <i>By Ben Evans</i> <i> Translated by 盖磊</i>
---------------