---
title: Getting Involved
description: Participate in Abstract Play development
lead: This article discusses how to participate in Abstract Play development.
date: 2023-04-30T21:00:00.000Z
#weight: 10
---

Abstract Play is an open-source project, and participation is warmly welcomed! Whether coding new games, translating strings, or just fixing bugs, this article has instructions on how to get involved.

<!--more-->

## Translations

The most common way people contribute is to translate game messages into their native language. We're finalizing instructions, but in the meantime, if you want to get started, please email [support@abstractplay.com](mailto:support@abstractplay.com).

## Process

If you want to contribute code, the normal way is through a pull request. Each repository (see below) has a README that explains how to set up a local environment. Don't hesitate to [reach out to the developers](mailto:support@abstractplay.com) with any questions.

## Repositories

All of Abstract Play's source code lives on [GitHub @AbstractPlay](https://github.com/AbstractPlay). The project is split up over a few different repositories:

- [apsite](https://github.com/AbstractPlay/apsite): This is where this website and documentation lives. You go here if you wish to update or expand the documentation.

- [front](https://github.com/AbstractPlay/front): This is where you actually interact with the service. It's what appears when you go to <https://play.abstractplay.com>. You go here if you want to help with refining the UX or translating strings.

- [gameslib](https://github.com/AbstractPlay/gameslib): All the games are implemented in TypeScript. This library contains all of the games and is reused by various other repositories. If you're feeling ambitious, this is where you'd come to implement a new game or fix a bug in an existing one. You also come here if you want to help translating game messages.

- [node-backend](https://github.com/AbstractPlay/node-backend): This is the heart of the record-keeping system and is what allows users to interact with each other. You'd only come here if you wanted to expand the core functionality of Abstract Play.

- [renderer](https://github.com/AbstractPlay/renderer): The renderer is a special library that creates interactable game boards. It's pretty specialized, but if you want to change how boards are generated, this is where you'd start.

- [recranks](https://github.com/AbstractPlay/recranks): The records and rankings code is what generates ratings and other statistics from the ever-growing pool of completed games. This is still very much a work in progress.


