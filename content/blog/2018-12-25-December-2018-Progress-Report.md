---
title: "December 2018 Progress Report"
date: "2018-12-25"
categories:
    - "Development Status"
---

Work has been extremely busy, so I'm afraid I didn't make much progress in September and October, but I ended up with the month of December off. I still didn't have as much time as I had hoped, but I still got lots done.

## Games/AI Server

Because of how AWS is structured and billed, I'm having to give up on supporting third-party games and AIs for now. To communicate with the database (Serverless Aurora), my code needs to be in a VPC (virtual private cloud). But to support third-party games and AI, I need code within that VPC to be able to contact the outside world. That's doable, but it's relatively expensive (my budget is small). Once the service is launched and the monthly pricing is more certain, we can explore adding this option later.

## Gameplay

Filled challenges now lead to actual games. There will be no "undo" feature. Instead, you can preview the results of your move before committing to it. Games can now end normally, and they close and archive successfully. You can resign from games, and in-game chat is also working. The in-game console has been implemented. You can freeze/thaw clocks and agree to end a game in a draw.

## Meta

You can add tags to games, which will be visible to everyone. You can also rank the games relative to each other (including ties). [I wrote and published ranking code](https://github.com/Perlkonig/Condorcet), which I will use to produce overall rankings of the available games. Finally, basic direct messaging has been implemented.

## Next Steps

There is still lots of back end stuff to do (ladders, standing challenges, etc.) but now that the basic game flow is in place, I'm going to turn my attention to the front end. I'm going to start with the rendering engine (the code that takes the JSON output from the game code and converts it into an actual display image). And then I'll start coding the actual interface. We'll see how it goes.

I wish you all a very Merry Christmas and all the best in the new year!