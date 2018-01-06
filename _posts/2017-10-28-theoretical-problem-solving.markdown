---
layout: post
title:  "Theoretical Problem Solving"
date:   2017-10-28 15:51:23 +0200
categories: ideas
thumbnail: "/zim/assets/img/2017-10-28/thumb3.png"
circle: a
---

<h3>Theoretical Problem Solving</h3>

In these days I'm working on breaking down the process of what needs to be done. As each operation is going to be somewhat "independant" (I realise it sounds a bit counter-intuitive to use this term when referring to a Rube Golberg machine), I don't need to have the whole machine designed beforehand. It will be more of trial-and-error to see what works together and what doesn't. I'm calling this <span class="feed">theoretical problem solving</span> for now as it consists mostly of brainstorming possible cause and effect scenarios, working within my limited repetoire of physical computing knowledge:

<p class="indent">
— use an LED or emit light from a source &#10230; as a ball passes in front of the light, a photoresistor detects this break and the resistance changes <br />
— use a flex sensor &#10230; induce a collision with the ball <br />
— pour water into a container &#10230; use water sensor to detect the change in level
</p>

And some other procedures I'd like to play around with, but of which the effect is still unknown to me:

<p class="indent">
— use a motor to make something spin <br />
— produce noise to then potentially detect
</p>

I don't necessarily want the machine to be afinalistic, but if we were to consider the machine as a whole as <span class="feed">the cause</span>, then I want <span class="feed">the effect</span> to be simple - maybe make a chime or produce some text. I think incorporating sound could be interesting as it would add another dimension. Every time a user interacts with the machine it could output a different sound, perhaps depending on its mood. And if this machine were to have a mood, it could also be interesting to have this mood driven by some sort of data. For example I could use a twitter API to detect a certain trend or a global mood and call it something like "machines have feelings too" or "touch me to make me feel something" or "maybe if you touch me I'll finally feel something".
