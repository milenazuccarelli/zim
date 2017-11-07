---
layout: post
title:  "Functionality and Visual Communication"
date:   2017-11-07 16:43:23 +0200
categories: ideas
thumbnail: "/zim/assets/img/thumb4_2.png"
circle: a
---

<h3>4. Functionality and Visual Communication</h3>
<figure >
    <img src="{{ site.baseurl }}/assets/img/img2.png"  alt="" />
    <img src="{{ site.baseurl }}/assets/img/img3.png"  alt="" />
    <figcaption class="feed">Fig. a.1: test using img tag instead of alt or span</figcaption>
</figure>
<h3>4.a — functionality</h3>
Although as a first basic test it works well, the script that I've worked so far has a few issues. As I'm using an XMLHttpRequest to a different domain than that which my page is on, some pages are failing to load as an 'Access-Control-Allow-Origin' header is present on the requested resource. I'm getting a  <span class="feed">«origin 'null' is therefore not allowed access»</span> error. This is normal for security reasons and means that if I want to make cross-domain requests I need to employ a different strategy. I'm going to try that using CORS. For now it's as simple as downloading a chrome extension for my browser, however, it's a bigger problem in an installation scenario where I can't predict the URL provided, or even if I want the app to be accessible to other users further along the line. This is something I will have to implement this within the script, hopefully, I will manage! 

Other functionality I need to add is what I can only describe as "separating the tasks". The flow at the moment is that the user types in URL in the top left-hand corner and the text prints on the same page. I need to achieve is one page with only an input field in the center prompts the user to enter a URL and hit enter. Once the enter button has been hit it leads to a new page with the final result, as it were.

<h3>4.b — appearance</h3>
<figure >
    <img src="{{ site.baseurl }}/assets/img/img1.png" alt="" />
    <figcaption class="feed">Fig. a: test using div instead of span or p</figcaption>
</figure>

I'm debating between different visual outputs at the moment. <br />
<span class="feed">001</span> — What I initially intended for concrete poetry was more visual poetry. I didn't want the text to form some sort of shape, I just want it to be arbitrary and just visually deconstructed and <span class="show__image"><span class="blog__image"><img src="{{ site.baseurl }}/assets/img/johncage.JPG" alt="visual poem" /></span><span>scattered</span></span> (but a lot more so than what Jack Kerouac implies with that term...!) It's the output I have at the moment but something feels uneasy about it. It breaks up the text so that it's a bit easier to look at and read certain phrases. Of course I'm in need of a change of font but serifs are often associated with poetry so that shouldn't be the problem. 

<span class="feed">002</span> — I tried a second output where I took all that text and ordered in in lines like a traditional poem. This would lead to just <span class="feed">serendipitous <strikethrough>concrete</strikethrough> web poetry</span>. For shorter poems (pictured: Metal Magazine) it could work, although upon first glance the links could throw off the perception of it being a  poem. In the second case (pictured: CNN) it becomes a lot harder to look at or even read as it's so dense with information. Personally, I felt too overwhelmed to bother trying to even skim it.

<figure style="margin-left: 10em">
    <img src="{{ site.baseurl }}/assets/img/poem1.png" width="49%" alt="" /> <br/>
    <img src="{{ site.baseurl }}/assets/img/poem2.png" width="49%" alt="" /> 
<figcaption class="feed">Fig. b: structured poems</figcaption>
</figure>

<span class="feed">003</span> — I was thinking I could place some of the text on paths to curve them, but this is not very typical of any visual poetry. Although it has a lot of potential to look extremely corny, cringey, cheesy, cliché, and all those good things, I could take a stab at giving in to making <span class="show__image"><span class="blog__image"><img src="{{ site.baseurl }}/assets/img/ilpleut.jpg" alt="calligrammes" /></span><span>calligrammes</span></span>. I've been interested in experimenting with SVG paths in HTML and Javascript lately. I did a few experiments with these: <br /> 
— assigning a given/predetermined path to a line of text <br />
— dynamically assinging a path to a line of text as the user draws with his cursor <br />
I was using these experiments to replace my portfolio website with something less serious. To see it in action [click here][miles-website]! I hope the instructions are clear enough but the aim it just to drag your mouse around and draw a new path. 

<figure>
    <img src="{{ site.baseurl }}/assets/img/site.png" alt="" />
<figcaption class="feed">Fig. c: experiments in Javascript svg paths and my website, apageofobjects.me </figcaption>
</figure>

Concrete poems and <span class="show__image"><span class="blog__image"><img src="{{ site.baseurl }}/assets/img/ilpleut.jpg" alt="Apolinaire il pleut" /></span><span>calligrammes</span></span> have a distinct meaning or object they're referencing which determines the shape of the poem. As the poems that are being generated are serendipitous and arbitrary I think it would be funny and also make a lot of sense to put them into abstract forms, which still have a visual shape but not a defined concept. 

Catch me outside how bout dat:<br />
<span class="feed">001</span> — [my GitHub repo][miles-gh]<br />
<span class="feed">002</span> — [my Twitter][miles-twitter]<br />
<span class="feed">003</span> — [my website][miles-website]

[miles-gh]:   https://github.com/piccolazucca
[miles-twitter]: https://twitter.com/studionugae
[miles-website]: http://apageofobjects.me
