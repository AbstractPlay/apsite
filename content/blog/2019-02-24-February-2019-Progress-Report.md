---
title: "February 2019 Progress Report"
date: "2019-02-24"
categories:
    - "Development Status"
---

## Rendering Library

The [rendering library](https://github.com/AbstractPlay/renderer) reached a minimally viable state this month, resulting in a v0.1.0 release!

To minimize network traffic and storage space, and to afford maximum flexibility, the back end produces representations of game state in JSON, [which must follow a specific schema](https://github.com/AbstractPlay/renderer/blob/master/docs/schema.adoc). Here's an initial Ithaka board, for example:

```json
{
   "board": {
      "style": "squares-checkered",
      "width": 4,
      "height": 4
   },
   "legend": {
      "B": {
         "name": "piece",
         "colour": 2
      },
      "G": {
         "name": "piece",
         "colour": 3
      },
      "R": {
         "name": "piece",
         "colour": 1
      },
      "Y": {
         "name": "piece",
         "colour": 4
      }
   },
   "pieces": "BBGG\nB--G\nY--R\nYYRR"
}
```

The front end can then render that based on individual user preferences. The system has 10 built-in colours, 4 colour-blind-friendly colours, and 10 black-and-white patterns, all of which can be customized.

### Standard Colours

![Ithaka board using standard colours](/images/ithaka-standard.svg "Ithaka board using standard colours")

### Colour-Blind-Friendly Colours

![Ithaka board using colour-blind-friendly colours](/images/ithaka-cb.svg "Ithaka board using colour-blind-friendly colours")

### Patterns

![Ithaka board using patterns](/images/ithaka-patterns.svg "Ithaka board using patterns")

The renderer is *not* yet complete. As more games get added to the system, I'll expand the renderer to support them.

## Front End

This is the part that will turn my hair even whiter. Front-end development is a crowded, fast-moving field. It is taking hours to get very basic things working. But progress *is* happening. The internationalization framework is working, as is authentication. I'm still wrapping my head around the ins and outs of [Relay Modern](https://facebook.github.io/relay/en), but the front end is indeed able to communicate with the back end. So this is very good news.

## Next Steps

There's still a lot of front-end work to do. Once it can interact with all the currently implemented features of the back end (profile management, challenge management, game interaction), then I'll start the cycle again: working on the back end to add more functionality and games, then work my way back to the front end to support them.

Talk again soon!
