---
title: "Part 12: First Stop, Domain Names"
author: FelicianoTech
date: "2025-03-30T01:30:00-04:00"
description: "I'm on the product roadmap train planning the MVP of Revidian Cloud. First stop? Domain names."
feature: "starting-with-domain-names--1910x1000.jpg"
featureHide: true
categories:
  - "Main Story"
---

There's several core concepts in Revidian Cloud that make it tick.
It's the availability of all of them in one place that will truly create Revidian Cloud's value in the future.
For the Minimally Viable Product (MVP) release, I've decided to stick with just one “core concept” and flesh it out.
In the near future I can begin to add others to complement domains.

<!--more-->

## Domain Names

The first core concept of Revidian Cloud are domain names.
As they will be the building blocks of everything else to come, it makes sense for domain names to be the first stop in the product roadmap.

One of my first “itches” I'm solving is the fact that having several domain names at multiple registrars is annoying.
There's many reasons why this happens, which I touched on in [part 11](/blog/part-11--new-project-new-chapter/).
Having to log into different websites to see what I have isn't great but add in the constant upsells on those websites, the varying design and quality of UI, it's a mess.
The Revidian Cloud MVP will allow you to view all of your domain names, their expiration dates, which registrars they are from, and where DNS is hosted, in one app.


## Verification & Importing

When it comes to the Revidian Cloud brand, there's certain aspirations that I have.
I want to support the little guy, embrace open-source, innovation, and integrity.
There's a space in the domain market that I feel doesn't mesh well with integrity.
I don't want Revidian Cloud to be used to squat domains, spy on competitor's domains, or become a market to try and snipe domains from others.
This is why I will be requiring verification for domains.

Verification is added friction I hope I can minimize as it will be worthwhile.
Importing domains from another platform such as Cloudflare is the best way to implement verification.
Cloudflare ensures that domains are owned by the user.
Importing from Cloudflare’s API means they do the verification for me and the user can import many domains in one go.
A win-win situation, or so I thought.

### Security Concerns
When I was shopping around the idea of Revidian Cloud to some friends, I received a bit of feedback that gave me pause.
A friend told me, “I would be hesitant to give a SaaS tool that much access to my registrar and similar services”.

He later told me, “I'm sure there are plenty of less paranoid folks \[out there\]” but the damage was done.
Would everyone feel like this? Is this whole concept screwed? :grimacing:
I thought it through and decided that there's really only one way to answer these questions, continue with the project, launch the MVP, and see what happens.

### Applying Feedback
I did take my friend's feedback to heart which led to me changing the workflow for adding a domain name.
While API imports from providers is still the best way to do this, I decided to additionally allow adding domain names manually.
In this workflow a user would add a domain name, get a token, create a TXT record with this token via their DNS provider, allowing Revidian Cloud to verify their ownership.
This is a workflow seen at many Email Service Providers (ESPs), Google Search Console, Let’s Encrypt, and more as a method to verify ownership.

I like this workflow because adding support for various registrars and DNS providers will take time.
I need to build out support for them one by one.
In the meantime, TXT verification will allow users to verify domain names from any provider on day one of the launch.
I'm not sure if I'll ever get my friend to use Revidian Cloud but I am proud that I was able to take legitimate criticism and quickly turn it into a positive change for the web app.


## Challenges

The API security paranoia is only one challenge ahead.
To determine which registrar APIs I should prioritize, I've been researching registrar popularity and how their APIs work.
This led me to a list of potential issues:

1. The very nature of supporting several APIs for multiple providers will be a chore. This will be a fragile point in my codebase as APIs can go down, have bugs, make breaking changes, etc. Porkbun for example considers their public API to be beta. That doesn't fill me with confidence.  
2. The technologies used by these APIs vary. For example, the Namecheap API deals with XML instead of JSON. Yes, that's right. In the year 2025, the Namecheap API is XML-based. :unamused: This is annoying but something I will have to deal with.  
3. Additional security. Some providers make working with their API more complex than simply using an API token. Again I'll bring up Namecheap as an example. When a user creates an API token on Namecheap, they must provide an IP address to whitelist for that API token. This means that I will need to provide a consistent, outgoing IP address from my web app in order for Namecheap customers to be able to export their domain names. That’s very… unfortunate.

It's not all challenges though.
I've already built domain name import support for Cloudflare and it was a piece of cake.
Not only is Cloudflare awesome, their API is reasonable and they provide a Go SDK, which is great considering my app is written in Go. :thumbsup:


## An April Soft Launch

I'm preparing to launch the MVP next month in April.
It will be a stripped down app with just basic support for adding domain names, viewing/filtering domain names, and getting expiration notices via email, Slack, and Mattermost.

Other features I'm working on such as services and monitoring, software detection, etc won't be there yet.
Neither will payment plans.
It will be a free MVP in order to get others to kick the tires and get early feedback on the UX and feature set as I begin to add features.
Reach out to me or sign up at [https://cloud.revidian.com](https://cloud.revidian.com) in order to be notified when the MVP becomes available in April.

<br />

Until the next one,  
Ricardo (FelicianoTech)
