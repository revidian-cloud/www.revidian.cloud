---
title: "Part 1: Starting From Scratch... Sort Of"
author: FelicianoTech
date: "2024-03-10T18:30:00-04:00"
categories:
  - "Main Story"
---

A week into my startup-building journey, we've arrived at the first update.
My co-founder and I started the month by putting together a 31-day plan.
Starting from scratch isn't necessarily difficult, but it is tedious.
There are several social media accounts to create, analytics and a mailing list to set up, logos to design, and more.
However, some tasks involve putting in time and using our brains.
These tasks are where I was able to take a shortcut.

## Taking a shortcut

I've made a few attempts to build an events platform over the years.
I never got the code far enough for an MVP, but I maintained many ideas, research, and strategies in Google Docs.
In the past few years, I stumbled across an open-source project that resonated with me.

The project is called [Get Together](https://github.com/GetTogetherComm/GetTogether).
It was created by [Michael Hall](https://www.linkedin.com/in/mhall119/), a community professional I met several years ago at the [Community Leadership Summit](https://www.communityleadershipsummit.com/about/).
Get Together is an event platform that aims to match Meetup.com feature by feature.
As cool as the concept was, the project stalled.
There hasn't been a commit in years, and the GitHub Issues list continues to grow.

I've talked with Michael Hall about taking over the project for several months.
Whenever I think I'm finally going to make progress, it falls through, and communication pauses.
Unfortunately, this means my only route forward is to fork the project.

## Determining the go-to-market strategy (GTM)

Our fork of Get Together will be called [EventHunt](https://github.com/eventhunt-org/monolith).
It will continue the original goals of competing with Meetup and serving as an open-source application anyone can run on their server.

Speaking of which, downloading and running EventHunt on a server may be appetizing for many tech nerds like myself, but it won't appeal to everyone.
Here is where the second half of our strategy comes into play.

We will set up a first-party EventHunt instance called Melitix Events.
This model closely follows what Mastodon, Bitwarden, and Mattermost have, where you can get and run the software for free or avoid the headache of managing a server and use the SaaS instead.
Ultimately, event organizers will have three options:

1. run EventHunt on their infrastructure
1. use the official Melitix Events server of EventHunt
1. find a 3-rd party server in the community and use their server.

## Risks

I'm excited about this plan, but it comes with risks.
The first one involves licensing.
Since we forked Get Together instead of taking the project over, we need to abide by the [BSD-2-Clause license](https://opensource.org/license/bsd-2-clause) that it comes with.
We'll ensure it's compatible with other licenses we might use and continue to share the code contributed to this repository with the public.
It's not a significant concern for me, but ensuring we properly dot our 'i's and cross our 't's will ensure we comply with the license legally and ethically.
We want to be good open-source stewards.

The second risk stems from running an open-source project and a SaaS service simultaneously under different brand names.
One might argue that instead of one product, we're attempting to launch two simultaneously.
That's double the social media, double the websites, and possibly double the problems.

I've been a big fan and advocate of open-source my entire career.
If extra work is required to have better quality open-source code in the world, so be it.
I'm up for the challenge.
Some aspects of product building, such as the feature roadmap, architecture challenges, etc, will overlap between the SaaS and open-source "products".
So instead of saying we're launching two products, let's say we're launching one and a half products.
It'll help me sleep better. :wink:

<br />

Until next week,  
Ricardo (FelicianoTech)
