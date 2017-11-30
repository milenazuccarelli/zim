---
layout: post
title:  "Navigating Space"
date:   2017-11-07 16:43:23 +0200
categories: ideas
thumbnail: "/zim/assets/img/img1.png"
circle: a
---

<h3>5. navigating through space</h3>

<figure>
    <img src="{{ site.baseurl }}/assets/img/prototype4.png" width="100%" alt="" />
</figure>
How are different ways to interpret a page or what are the different components which it could be broken down into?
<p class="indent">
— visual poems <br />
— dada poems <br />
— take a text for a walk <br />
— soundscape <br />
— transform any website into a news website and call it "objective realities" (this is something I will do anyway) <br />
</p>

Thinking outside of the the 2d context within which we experience a web page. What if you could navigate through the space of a webpage, navigate through the text and images and experience it around you? A way of achiveing this, and making the data somehow "tangible" is through VR. I've never used any software for building virtual realities, and I'm not sure if it's possible to use ajax in Unity to import this data. I know it's possible in WebVR as it's written in Javascript anyway so it makes the most sense to do it in that. 
I like the idea because the website becomes an object of study and exploration for the user. 

In a-frame I've started working on a prototype that takes each part of text from the website and injects it into the page as an <span class="feed">a-entity</span> component. It took me so much longer than anticipated as I kept running into problems when attemping to integrate things dynamically. For now I've succeeded in printing the text within the scene. It's a very rough first prototype but I'm happy with what I was able to achieve after running into so many obstacles along the way. 

<figure style="margin-left: 10em">
    <img src="{{ site.baseurl }}/assets/img/prototype1.png"  align="left" alt="" /> <br/>
    <img src="{{ site.baseurl }}/assets/img/prototype2.png"  align="left" alt="" /><br/>
    <!-- <div style="width:49%;"></div> -->
    <img src="{{ site.baseurl }}/assets/img/prototype3.png"  align="left" alt="" /><br/>
<figcaption class="feed">Fig. a: first working prototype</figcaption>
</figure>

[miles-gh]:   https://github.com/piccolazucca
[miles-twitter]: https://twitter.com/studionugae
[miles-website]: http://apageofobjects.me
