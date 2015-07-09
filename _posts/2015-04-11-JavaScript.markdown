---
layout: post
title:  "Ruby and JS: Like Mac and Windows"
date:   2015-04-11
categories: technical
---

### Loops and Hula Hoops

One of the first things you'll notice about Ruby is how symantically it reads when it comes to looping. Part of this comes down to its wonderful syntax, but also, part of it is the public methods readily available that make things like iteration and looping a breeze (and intuitive). But let's be fair here, Javascript has some built-in loops too, like #.map. The issue is Javascript's readily-available loops are limited (we're talking like 10-20% or what Ruby offers; who knows though, maybe I'm biased). Further, writing a loop from scratch requires a lot more work than Ruby, which means you'll be spending more time building tools that you need, rather than using tools you already have so that you can get more done in less time.

Beware: Here comes a rant for some entertainment; we'll get back on track afterwards. Let's look at the dynamic that exists here. I mean, Javascript has to be popular for some reason right? Just like Windows? I love Windows, everyone does, that's why everyone uses them (some mild sarcasm here, because I really do use Windows often too). The reality is (in my humble opinion...) Javascript is the widely-utilized language thanks to its domination over the web-browsing space, and getting everyone to change to the language that makes more sense and looks better isn't as easy as sending an e-mail to everyone. This is the same issue that exists between Mac and Windows, Mac does things really, really well, and looks great at the same time, but most things are made for Windows (particularly within the business realm) because a majority of everyone has Windows. However, over the years, we've seen their control of the market diminish as more people have embraced Macs, and just the same, Ruby is gaining more tracton every day. It only a matter of time, folks...

### Wait... What about the loops?

Okay... let's get back on track here. We'll start by comparing the implementation of map iterations on Arrays in both Ruby and Javascript for a visual, side-by-side comparison. As you will see by the code examples provided below (output is after examples), the methods of implementation are actually very similar.

![ruby map example](http://tonytino.github.io/imgs/ruby-map-example.png)

![javascript map example](http://tonytino.github.io/imgs/javascript-map-example.png)

![output for loop examples](http://tonytino.github.io/imgs/output-loop-example.png)

#### The key differences you'll notice are:

Javascript requires parentheses around the if/else if conditions.
Javascript requires that you declare things like var for the array and function for the loop.
While not absolutely necessary, for consistency and reliability purposes, the use of a === in Javascript is recommended versus ==. However, either would work in this particular instance.
Javascript does not offer string interpolation (see the else statement for Ruby), and therefore, concatenation is necessary.

Believe me when I say this is just scratching the surface, and we used an iteration method that Javascript just so happens to offer. Otherwise, we'd have to write the function ourselves (example below; same output as before). Once you get past the fact that Javascript isn't the most convenient language to write in, it's really not that bad (or, is it?).

![javascript loop example](http://tonytino.github.io/imgs/javascript-loop-example.png)