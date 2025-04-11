---
title: "Part 8: Alphas & Betas & Testing, Oh My!"
author: FelicianoTech
date: "2024-10-12T15:30:00-04:00"
description: "As I begin to look for alpha testers to try out EventHunt, I share my thoughts on MVPs, alpha testing, and how it differs from beta testing."
categories:
  - "Main Story"
feature: "alpha-stage.jpg"
featureHide: true
---

Hey folks, after another three-month break, I am back in the driver's seat of Melitix.
Unemployment has not been fun and keeps derailing me.
I finally got some freelance work to help out, but I'm still looking for a full-time role ([hire me](https://www.linkedin.com/in/ricardofeliciano/)).
I'm eager to move the story Melitix along, so let's get to it.

Melitix is currently at the stage that all of my SaaS projects have made it to, but never passed, getting real users.
I have thoughts about why I've struggled with this in the past, but I'll save that for another time.
For now, let's get into the Melitix MVP and alpha testing.


## Building an MVP

I've been building EventHunt, the open-source project that will power Melitix.
I was initially going to fork a project called [Get Together](https://github.com/GetTogetherComm/GetTogether), but due to issues with the codebase and my preference for a different programming language, I decided to start from scratch.

Many software engineers build Minimally Viable Products (MVPs) incorrectly.
They take too much time, ship the wrong thing, etc.
I've made these mistakes and I'm trying a different approach this time.
Cutting scope and delivering small amounts of value throughout the MVP process is the way to go about an MVP.

There's a great illustration by Henrik Kniberg that I've referred to time and time again regarding "the right way" to build an MVP:

{{< figure src="how-mvps-should-work.png" width="800px" class="aligncenter" >}}

The process on the bottom might take longer and involve a bit more work, but you get to provide value sooner and see happy faces earlier on.
If you're curious about Henrik's philosophy of building MVPs, you can read his article on the thought process and this illustration [here](https://blog.crisp.se/2016/01/25/henrikkniberg/making-sense-of-mvp).

Following Henrik's framework, my next step is to try and test my skateboard.


## Alpha Testing

<div style="display:flex; flex-direction:column; align-items:center; margin-left:auto; margin-right:auto; border:1px solid #53d769; padding:10px; width: 350px;">
    <p style="margin-top:0;">💡 I'm looking for people to alpha test EventHunt. Interested?</p>
    <a style="display:inline-block; margin:2px; border-radius:5px; background-color:#53D769; padding:2px 4px; width:100px; color:white; text-decoration:none; font-family:sans-serif; font-size:smaller; text-align:center;" href="https://www.eventhunt.org/alpha" target="_blank">Sign Up</a>
</div>

I've worked at a Continuous Integration & Delivery company for 8 years.
Testing, in its various forms and stages, is now baked into my brain.
I've been building EventHunt, and it now has some functionality.
Is it at feature parity with GetTogether yet? No.
Is it at feature parity with Meetup.com? Hell no.
Does it have enough to serve as an MVP? Maybe, I'm not really sure.

### My Alpha Test Goals
The question of whether or not what I have is MVP-ready is the main goal for the alpha test.
Defining my goals for the alpha test further, here's what I'm aiming for:

1. Confirm EventHunt has **just enough** features \- I have a ton of ideas for this project, but I can't build them all right now. I'm building the smallest set of features possible to get the first few users. Limit scope creep.  
1. Find & fix critical bugs \- bugs that are so severe that they hamper my ability to hit goal \#1 need to be fixed in this stage. Bugs that are aesthetic or performance-related can be de-prioritized.  
1. Find early users \- during the alpha test, I'm also trying to determine if this person will be a good fit for EventHunt. There's a high probability of this considering this person was interested enough to test a product in the alpha stage.

### Alpha vs Beta Testing
I want to end this post with my thoughts on the difference between alpha and beta testing.
A quick Google search shows a lot of confusion on the topic, with some people suggesting there is no difference other than the order.

{{< figure src="alpha-beta-diagram.jpg" width="800px" class="aligncenter" >}}

Order is part of it, but really these concepts are part of a testing and releasing methodology.
You don't need to implement each stage in your project, and what each stage means might differ between developers and companies.
What's essential is that meaning and context are applied to each stage you have.
From a product management standpoint, it is important to make sure everyone is on the same page internally.
If you're building an open-source project like I am, this then applies externally as well.

I differentiate between alpha and beta testing by the resistance to change.
During alpha testing, I plan on rebuilding the server environment multiple times.
Whole features might come or go.
APIs can completely change.
For SaaS, this includes deleting the alpha database and starting it fresh each time.

This is my hard line between alpha and beta regarding EventHunt.
During the alpha, the database is volatile.
Users should expect that any data they enter during this period will be deleted at some point in the near future.
Once EventHunt enters beta, the database becomes non-volatile and will persist between releases with regular backups taken.

Is this how you see MVPs and alphas vs betas? Do you have a different approach?

<br />

Until the next one,  
Ricardo (FelicianoTech)
