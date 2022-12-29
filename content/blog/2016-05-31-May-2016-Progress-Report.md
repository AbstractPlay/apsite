---
title: "May 2016 Progress Report"
date: "2016-05-31"
excerpt: "As I expected, having guaranteed development time every month has made it easier for me to make time on the weekends to do additional work. I actually got quite a bit done this month."
categories:
    - "Development Status"
---

Here's the first monthly progress report.

First, let me say how exciting it has been to return to this project. It was always a labour of love, and it has saddened me to be away for so long. It feels great to dive back in. It has also been very challenging (which is part of the fun!) because I am committed to making the highest-performing, most scalable platform that I can.

As I expected, having guaranteed development time every month has made it easier for me to make time on the weekends to do additional work. I actually got quite a bit done this month.

  * The wiki is up with some light documentation. I anticipate doing some more formal documentation shortly, but I spent most of my time this month doing some proof-of-concept coding and setup work.
  * I've setup the two public-facing URLs with full SSL support (via [Let's Encrypt](http://letsencrypt.org)).
    * www.abstractplay.com is the main front end that will support the blog, wiki, and first-party interface.
    * api.abstractplay.com is the API itself, which will allow programmatic access for third-party interfaces and manual browsing for curious parties. It will comply with [RESTful](https://en.wikipedia.org/wiki/Representational_state_transfer) [design](https://restful-api-design.readthedocs.io/en/latest/) [principles](http://restcookbook.com/).
    * The games server is also configured, but it won't be available to external users. The way the system will work, third-party games don't have to be hosted with me. They can be hosted anywhere, as long as they conform to the API outlined (preliminarily) on the wiki. I've coded the simplest of the level 1 games, Ithaka, and am now working on integrating the game server with the API server.
  * I've confirmed that I will move forward with implementing the server-side component in [Python's](http://python.org) [CherryPy framework](http://cherrypy.org).
  * Users can authenticate via Facebook and Google. You can also create a separate username and password if you prefer.
  * The OAuth 2.0 framework is also in place. Third parties can obtain tokens, and users and permissions are properly (as far as I can tell at this point) handled.
  * The system will also support Basic Auth for third-party clients (via the "Authorization" header), but the server won't emit the "WWW-Authenticate" headers, so Basic Auth won't work from a plain browser.
  * I'm focusing on the API for now. Once the infrastructure is in place, I will start worrying about the front end. I want the HTML interface to be responsive and intuitive. There are a number of HTML5 game frameworks out there, and I've tinkered with a few, but I haven't done a formal proof of concept test yet. Notes will appear on the wiki eventually.
  * That said, I *have* had to do some preliminary design of how game states will be represented, which is going to include separating the actual graphics from the representation itself. I finished some code today that allows for custom sprite sheets. Most games will work fine with the generic sprites, but game-specific assets will be supported. The system will also support variants, so even the "generic" sprite set will have variants for colour blindness, different-looking materials, etc. These, too, can be designed by third parties (though they'll need to be hosted by me to work).
  * I also did a lot of schema work. Most are linked from the wiki. This will give you an idea of what custom-written games and AIs will need to produce.

  So I'm pretty happy with how things are going so far. One of the things I need to prepare myself for is getting things to GitHub. This is going to be a learning opportunity for me because it requires a very particular structure, and there's still lots I don't know about best practices in this regard. There's also the issue of separating the development servers from the production servers. Once things are a little more established, I'm going to take a coding break and just focus on this.

  Join us in the Google Group (linked in the sidebar) if you have questions or suggestions. I appreciate the feedback I've received so far. Next update will be at the end of June.

