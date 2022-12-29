---
title: "April 2017 Progress Report"
date: "2017-04-13"
categories:
    - "Development Status"
---

Two words: development hell.

For a sense of what it feels like to write even moderately complex front-end code, [read this Medium post](https://hackernoon.com/how-it-feels-to-learn-javascript-in-2016-d3a717dd577f). I love talking to computers. I love figuring out how to make them do my bidding, but I'm not a fan of the scaffolding required to get to the stuff you actually care about (e.g., actually coding freaking games). This is one reason I love short coding challenges like [Project Euler](https://projecteuler.net/) and [CodinGame](https://www.codingame.com/).

The difficulties are compounded when you aren't working on the project regularly. It takes time just to get your head back in the game, and the libraries and frameworks you're using get updated and can introduce incompatibilities that weren't a problem a month or two ago.

My first two hours this morning were spent figuring out why the API server stopped running. The virtual hosting company had updated their Python libraries, which borked my `virtualenv`, and which also borked some older Python libraries that are now fully defunct. Fortunately these are not core to what I'm working on now, but I'm going to have to cross that bridge soon. But at least I was able to get it back up.

Then I realized that I was at a point where I was going to start adding more and more text, and before I did that, I realized I should finalize the internationalization (i18n) framework. Usually i18n requires marking the strings in your code somehow so that the system can look for translations, and I'd rather do that now when I have a couple dozen strings as opposed to later when I have hundreds. So I did some research and decided to go with `react-intl`, but that introduced some new NPM dependencies. It took me another hour or so to resolve those and get my `package.json` file compiling properly again.

Then I had to integrate the i18n code with the rest of the system, which thankfully didn't take too long. Then I tagged a single string. Then I spent the rest of the day trying to understand the best translation workflow&mdash;how I extract those strings from my code, translate them, and then import them back in. This shouldn't be all that difficult, but go back and reread that Medium post. Nothing is simple in this world.

I am now able to extract the marked strings and create separate locale files that we can translate. But they don't integrate with standard `gettext` tools. At this point, I'll be happy just to be able to translate. At the next session, I need to figure out the best way to import the translated files into the front end and make it possible to switch between them in the UI. *Then* I'll go through and finish flagging all the strings before moving on.

I'm still committed to this project, but I won't lie; sessions like today's are frustrating. I want to find a way to develop more regularly so I can start making some real headway. We're really close, but it feels like a real [Zeno's Paradox](http://platonicrealms.com/encyclopedia/zenos-paradox-of-the-tortoise-and-achilles). I will be ecstatic when I can actually start working on the actual games again.

I'll report again soon. Stay tuned!


