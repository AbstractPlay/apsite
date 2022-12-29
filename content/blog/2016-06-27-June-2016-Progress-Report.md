---
title: "June 2016 Progress Report"
date: "2016-06-27"
categories:
    - "Development Status"
---

Another exciting month! Not as much *visible* progress, but my brain is definitely smoking. Here's what happened.

[The GitHub repositories are up!](https://github.com/AbstractPlay) And there's actual code there! If you're a developer and want to see how things are going, take a look. I'm no pro, so I'm open to pull requests.

In order to start testing the back ends, I needed to start working on the front end, so that's where I spent most of my time this month. Let me tell you, I'm getting my butt kicked! This has been the most challenging part so far. So much has happened in the world of front-end development that I just haven't kept track of. I've always been more of a server guy, so that part has been relatively painless, but actual users are much more demanding.

For better and for worse, JavaScript isn't going anywhere, so I'm embracing it. There are just too many upsides. So far everything is working in modern browsers, including mobile ones. So that's a good sign. Here are the tools I'm currently using:

  * [React](https://facebook.github.io/react/) is all the rage, at the moment. It's a pure view library created by Facebook that has all sorts of benefits, but it has a *steep* learning curve. It's taking a lot of mental energy to wrap my head around it. I'm considering just taking a full-blown online course instead of piece-mealing it like I am now.

  * React is just the "view" component. You need a way of managing the application's state. I'm doing that with [Redux](http://redux.js.org/). While the learning curve is not quite as steep as React's, there are still some conceptual hurdles to jump over.

So currently I have the front end at least rendering and routing properly. I'm trying to figure out how to handle authentication at the moment before finally connecting the front end to the back end and testing games. I'll be sure to let people know when I have something available for public testing. I *do* want the feedback.

For those who avoid JavaScript (and I'm one of you; I use ScriptSafe routinely), I apologize but it will be unavoidable. All I can do is promise that I will be doing no ads or surreptitious tracking. The source code will all be available for review.

To start, the front end will still render the games as pure PNGs with manual move entry. I will eventually explore the various HTML5 game engines to find one that will allow for click-and-drag move entry. Regardless, both options will be available, so you can always stick to pure PNGs if you wish. And who knows, if there's a demand for it, I could even find a way to view games and make moves via email or text messages :)

So that's it. Please visit the [Super Duper Games Google Group](https://groups.google.com/forum/#!forum/superdupergames) if you have questions or suggestions. See you in another month!
