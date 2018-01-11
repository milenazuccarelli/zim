---
layout: post
title:  "cors solution"
date:   2018-01-11 14:43:23 +0200
thumbnail: "/zim/assets/img/2018-01-11/thumb.png"
circle: a
---

<h3>7. solution</h3>

While working on optimisation I accidentally stumbled on a solution to the CORS issue for images as well as URLS. To initially access the URL (without disabling CORS on safari or without installing an extension in chrome) I’m using <a href="https://github.com/Rob--W/cors-anywhere">cors anywhere</a>, a NodeJS proxy which adds CORS headers to the proxied request. This allows me to access the text and links. In terms of the images I’m using the ImageOptim API web service which resizes the image and injects headers on the fly — I stumbled upon this while trying to pre-scale images to be a power of two (as webgl only accepts these dimensions) and realised it provides headers as well. Both of these services provide a prefix URL to the original url so the final result looks something like:<br/>
<span class="feed">001</span> — http://localhost:8080/http://google.com/ (for links) <br/>
<span class="feed">002</span> — https://img.gs/Personal Code/Options/Image URL (for images)

This means I can go back to adding an input field for the desktop app. I'll update how that turns out in this post. 