---
title: "Part 7: First Public Commit of EventHunt Lands on GitHub"
author: FelicianoTech
date: "2024-07-08T20:00:00-04:00"
description: "Struggle SaaS is back. EventHunt landed on GitHub, but much work remains before anyone can run it on a server."
categories:
  - "Main Story"
tags:
  - open-source
---

Hey folks, the last time I wrote was at the end of April, as I've been looking for a job (and am still looking; [hire me](https://www.linkedin.com/in/ricardofeliciano/)).
I can no longer ignore my deep-down propensity to build things.
Thus, in parallel with my job search, I shall continue building Melitix and EventHunt.

In [my last post](/blog/changes-to-struggle-saas/), I mentioned that maintaining a weekly publishing cadence was too difficult.
Instead of "weekly" posts, I will publish "parts" when and if I have more to say about this journey.
Welcome to part 7.

I have yet to work on content marketing as I mentioned I would.
Instead, I focused on my re-write (or re-imaging, if you will) of [GetTogether](https://github.com/GetTogetherComm/GetTogether).
I put in a few weeks of matching the design and features of GetTogether but in an entirely new codebase.
Two days ago (July 6, 2024) I prepped the code to be public and pushed it up to GitHub.
You can find it at [eventhunt-org/webapp](https://github.com/eventhunt-org/webapp).

## Publishing Open-Source Is Scary

Making the code public was remarkably scary, and probably not for the reason you think.
Many devs worry about publishing their code publicly due to scrutiny of the code itself.
Is it good enough? Will I be made fun of? Did I comment enough? So on and so on.
While I can't say that wasn't slightly on my mind, this wasn't what made running `git push` so scary for me.
The process around publishing an open-source project as a "company" was.

I have tons of open-source projects on GitHub.
I rarely think about the implications.
I slapped an MIT license on them and moved on.
For EventHunt, while I wanted it to be an open-source project, I was worried about losing control.
A big company can try to outmaneuver me and hurt my chances of ever making a buck, a contributor can submit code that causes legal problems for the codebase, and who knows what else.
This led me to questions that took days for me to answer:

- Which license do I choose? GPL, MIT, Apache? BSD?
- Do I use a Contributor License Agreement (CLA)?
- What the hell are Developer Certificates of Origin (DCO)?

Stressing with these questions made me ask myself, "Should I make this project open-source at all?"

I want to avoid getting down the rabbit hole here (maybe I'll write something on my personal blog one day), but I'll explain what I decided and why.

In short, I strongly felt that EventHunt should be an open-source project.
Of the open-source licenses, the GPL made sense but limited me in what I could do as a business once the public started contributing to the repository.
The solution for this problem is to use a CLA.
Implementing a CLA is fine, but my former colleague Drew DeVault likes to tell people, [Seriously, don't sign a CLA](https://drewdevault.com/2023/07/04/Dont-sign-a-CLA-2.html).
I don't agree with some of his points, but many people do, and I wanted to consider their opinions.

Without a CLA, a copyleft license such as the GPL won't work.
EventHunt was published on GitHub two days ago with the [BSD 3-clause license](https://choosealicense.com/licenses/bsd-3-clause/).
This license allows the project to be open-source, helps protect the names/sponsors/trademarks, and allows me to have a future enterprise version of EventHunt to make some money and fund this whole thing.
I drew inspiration from both GitLab and Tailscale in how they manage their open-source projects.
They don't use CLAs, use MIT or BSD-3, and use DCOs.

## The Current State of EventHunt

The code is now public, but the project isn't ready for… anything yet.
As of its first commit, EventHunt is not ready to be run in production.
Fundamental features are either incomplete or outright missing.
The first milestone I'm looking to hit is 99% design parity and 90% feature parity with GetTogether.

On its own, GetTogether has few features.
Compared to a brand-new codebase, though, it has a good amount.
The first release of EventHunt will have basics such as allowing the creation of events, groups, and RSVPs.
It won't have extras, such as social logins, for example.
We'll work our way there.

Visit the early [EventHunt codebase on GitHub](https://github.com/eventhunt-org/webapp) and give it a star!
Development is just getting started, and it should be fun.

<br />

Until the next one,  
Ricardo (FelicianoTech)
