---
layout: post
title:  "Technical Process"
date:   2018-01-06 14:43:23 +0200
categories: ideas
thumbnail: "/zim/assets/img/2018-01-06/technical-0.png"
circle: b
---

<h3>6. process</h3>

<figure>
    <img src="{{ site.baseurl }}/assets/img/2018-01-06/technical-0.png" width="100%" alt="" />
</figure>

<h3>6a. — uncategorised</h3>
I also need to figure out how to get it working with a joystick for locomotion within VR. This is something I’ve never done with webVR but I know it should be possible somehow. I also need to figure out the input - how will the user write a URL?  So additional tasks which I think will take up the most time:  <br />
<span class="feed">001</span> — adding functionality for the joystick <br />
<span class="feed">002</span> — adding functionality for typing the URL 

For now I think I will need to leave aside the interface for allowing the user to input text. I really don’t have a solution for it in my mind and I don’t know anybody who works with WebVR or a-frame to ask for advice. For now I think the solution will be for the user to input the text with a keyboard when using it in browser, and some how have it automatically appear with a URL of my choice in mobile/headset. I could potentially leave the input field and make the user choose a URL beforehand, and then consequently put the headset on. 
The joystick will also in this case only need to be used on mobile, while for browser the user will use the arrow keys on the keyboard.

Negating what I wrote previously, I found two potential which allow keyboards in aframe (thanks, stackoverflow ha)
<figure style="margin-left: 10em">
    <img src="{{ site.baseurl }}/assets/img/2018-01-06/technical-5.png" width="49%" align="left" alt="" />
    <img src="{{ site.baseurl }}/assets/img/2018-01-06/technical-6.png" width="49%" align="left" alt="" />
<figcaption class="feed" align="right">Fig. b, c: <a href="https://rdub80.github.io/aframe-gui/examples/casestudy_keyboard.html">here</a> and <a href="https://github.com/etiennepinchon/aframe-material#-a-keyboard-%EF%B8%8F">here</a></figcaption>
</figure>

<!-- <p> 
<span class="feed">001</span> — the <span class="feed">&#x0003C;a-keyboard&#x0003E;</span> primitive that's part of the <a href="https://github.com/etiennepinchon/aframe-material#-a-keyboard-%EF%B8%8F">aframe-material collection.</a> <br />
<span class="feed">002</span> — AFrame GUI Component There is a keyboard mapped for gaze/fuze input <a href="https://rdub80.github.io/aframe-gui/examples/casestudy_keyboard.html">two</a>.
</p> -->

<h3>6b. — images</h3>

Getting the images to work has been a tedious process, I keep running into CORS issues which block me from accessing any images. In some cases, due to the way the image was called in the HTML on the website, the URL is a stub and the image comes out black. In the case of Cross Origin Resource Sharing issues the images show up white. At the moment I would tend towards cutting out the image and limit the concept to text alone, however the CORS issue also affects which URLS allow me to access their content, so it’s something I need to resolve. 

<figure style="margin-left: 10em">
    <img src="{{ site.baseurl }}/assets/img/2018-01-06/technical-1.png" width="100%" align="left" alt="" />
    <img src="{{ site.baseurl }}/assets/img/2018-01-06/technical-2.png" width="100%" align="left" alt="" />
<figcaption class="feed" align="right">Fig. d, e: first prototypes with images</figcaption>
</figure>

What CORS is is cross-origin resource sharing. What this means is I can include certain headers in my code, which  make a request to the domain that hosts the image and receives a response. Generally images on a webpage are hosted on the same domain that they're being called on. What I'm attempting is cross-origin as the domain that is calling the image is different from the domain where the image is being hosted. Certain websites, such as CNN, Wikipedia, GitHub Pages and the likes already have headers present which makes it possible for you to access their images. 

I managed to get images working for such websites 
<figure style="margin-left: 10em">
    <img src="{{ site.baseurl }}/assets/img/2018-01-06/technical-3.png" width="100%" align="left" alt="" />
    <img src="{{ site.baseurl }}/assets/img/2018-01-06/technical-4.png" width="100%" align="left" alt="" />
<figcaption class="feed" align="right">Fig. f, g: no CORS issue - cnn and wikipedia</figcaption>
</figure>

<h3>solution</h3>
I have to admit defeat regarding the CORS, I spent so many hours and days on the issue and it just isn't possible to fix. This means the only solution is either to cut out images entirely, or disallow the user from choosing and inputting their own website. Regarding the latter I could limit it to just a wiki encyclopedia vr experience, for example. But my solution will be to cut out the custom input entirely, and present an array of urls that will be randomly selected for the user automatically. 

What also convinced me to take this approach is that aforementioned examples of built-in keyboards concern me in that they're extremely time costly. An issue with Vr installations is the impossibility of a wide reach (relative to other pieces that are being viewed) -- not everyone at the exhibtion can or will view it. Now if the average time per user is multipilied due to inefficiency in interface, it's worth reconsidering this interface.

<figure>
    <img src="{{ site.baseurl }}/assets/img/2018-01-06/technical-7.png" width="100%" alt="" />
</figure>

I'm not entirely devasted with this compromise, as it makes me think of the politics of the open work discussed by Umberto Eco in his 1962 essay titled "The Poetics of the Open Work" (emphasis added):
<p class="indent">
The possibilities which the work's openness makes available always work within a given field of relations. As in the Einsteinian universe, in the "work in movement" we may well deny that there is a single prescribed point of view. But this does not mean complete chaos in its internal relations. What it does imply is <span class="feed">an organizing rule which governs these relations.</span> [...] The author is the one who proposed a number of possibilities which had already been rationally organized, oriented, and endowed with specifications for proper development. All these examples of "open" works and "works in movement" have this latent characteristic, which guarantees that they will always be seen as "works - and not just as a conglomeration of random components ready to emerge from the chaos in which they previously stood and permitted to assume any form whatsoever.
</p>
So I think I'll roll with it with the justification that the pregiven array is just "an organizing rule which governs these relations." hah

<h3>6.c — links</h3>

I should preempt this by saying I am truly skeptical that links will work. At the moment a-frame has support for traversal links, which open portals to other scenes. This is not what I need at all. I did find a GitHub repo about connecting Virtual Worlds through hyperlinks in aframe which seems like a super helpful starting point but the authors have labelled this as highly experimental, and I don’t think this method would offer the support I need.
So far I have implemented a basic sphere triggered upon gaze leading to another standard .html page. The problem I need to face here is: 
<p class="indent">
<span class="feed">001</span> — I need to dynamically grab the base url from the <span class="feed">a</span> tag <br />
<span class="feed">002</span> — I then need to check if it pertains to the same domain as the parent (due to aforementioned CORS issues) <br />
<span class="feed">003</span> — I need to generate an html page for each url — not literally but figuratively, as it’s clear I can’t create a new .html page every time.
</p>

The  biggest challenge I face is the last point, figuring out a way to inject the data of the new Url to a new html page. This is my pseudo code:

//store the url in another form - id or class or some metadata <br />
set the href as a page.html and add some sort of query like ?url=http://blahblah.com <br />
take the query and instead of my url array in the script.js use the query as the Url <br />

test for now: <br />
link through to a new page <br />
keep the input method <br />
see if that works 

Starting with the small test from my pseudo code, I somehow managed to get the link through to work. I'm most proud of this as I was entirely convinced it wouldn't be possible. 

<figure>
    <img src="{{ site.baseurl }}/assets/img/2018-01-06/technical-8.png" width="100%" alt="" />
    <img src="{{ site.baseurl }}/assets/img/2018-01-06/technical-9.png" width="100%" alt="" />
</figure>

It's in no way perfect as it's still the first implementation. In terms of functionality I'm quite happy with it but I aesthetically it needs some work. I think I'll make a separate post for that. 