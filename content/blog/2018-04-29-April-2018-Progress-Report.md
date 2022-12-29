---
title: "April 2018 Progress Report"
date: "2018-04-29"
categories:
    - "Development Status"
excerpt: "TLDR: Things are still moving forward. I'm moving to AWS's serverless framework to deliver Abstract Play."
---

So no updates in a while. All I can do is apologize. This is still a project I'm excited about, but life has been challenging on many fronts, so one must prioritize.

In some ways, it's a good thing, because in the meantime a couple things have happened:

* [The GDPR](https://www.eugdpr.org/) entered the picture and changed, well, everything. I would have had to refactor quite a bit of code to comply.

* [AWS Lambda](https://aws.amazon.com/lambda/) has really come into its own and now supports C#.

TLDR: Things are still moving forward. I'm moving to AWS's serverless framework to deliver Abstract Play.

## GDPR

The GDPR has a number of requirements that affect how Abstract Play will have to function:

* Right to access: Users have the right to know what personal data I have. This was already going to be a part of the rewrite.

  * The site itself will only have data on games, including chat logs, that are either ongoing or have been completed in the past so many days.

  * Once a game is over, a single game report is generated (with no chat log) and put into a central, publicly available data bank. Player ratings will be generated based on this corpus of data.

  * A player's profile page will gather in one place all the data associated with them.

  * I'm not sure yet how access logs are going to be handled. I'm still researching this.

* Right to be forgotten: This is the big one.

  * User accounts will be handled through [AWS Cognito](https://aws.amazon.com/cognito/).

  * What I'll be storing is a player account tied to that user account with all the AP-specific settings, including a changeable display name.

  * Permanent game records will be tied to the player account only, not the user account.

  * Users can delete their user account. Doing so irreversibly disavows the player account. It can never be recovered.

  * The player account remains, as do the game records themselves, but there no way for me to tie that player id to the original user id.

  * The player's display name and name history will also be deleted from the player account as those are considered "personal data" under the GDPR.

## AWS

I'm moving to AWS. It's a little pricier, but the benefits are worth the cost.

* I won't have to process personal information. Amazon will, and they are far better equipped to handle security than I am. User accounts will be handled through [AWS Cognito](https://aws.amazon.com/cognito/). You'll be able to create accounts using Google, Facebook, Amazon, or a standard username/password if you really want. All logs will live with AWS, too.

* Almost everything is on demand. The only thing that needs to be running constantly is the database server. And that cost can be controlled and minimized by prepaying.

  * Lambdas are self-contained functions. I only pay for the time it takes for each to run.

  * These functions get called through [API Gateway](https://aws.amazon.com/api-gateway/). This means I don't have to pay to have multiple virtual servers constantly running or deal with rolling my own REST handlers with all the associated authorization and JSON schema checking and handling.

* AWS means essentially unlimited scalability.

## So where are things now?

All the work on the front end is still good. None of that needs to change.

The work on JSON schemas is still all good. The core approach isn't changing.

The work on database design is still mostly good. It's just the user and player differentiation that needs to be addressed.

The API server is a write-off. The CherryPy framework is being taken over by API Gateway and the individual resources will be ported to Lambdas.

The Games server is also a complete write-off. But I've already redone all that work in C#. (Ithaka is fully implemented.) The GitHub repos have been updated accordingly.

Now I have to start reimplementing some of the API resources in C# and then continue work on the front end interface.

I wish I could say all the recent life challenges are dealt with, but they're not. I will continue making forward progress. It will be easier now that I better understand the GDPR ramifications and have thought through how to accommodate them.
