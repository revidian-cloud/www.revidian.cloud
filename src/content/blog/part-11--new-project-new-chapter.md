---
title: "Part 11: A New Project, a New Chapter"
author: FelicianoTech
date: "2025-03-01T17:30:00-05:00"
description: "Let's discuss my early ideas for building Revidian Cloud."
feature: building-revidian-cloud-1910x1000.jpg
featureHide: true
categories:
  - "Main Story"
---

I started the Struggle SaaS blog in March 2024 to document my journey building Melitix, an open-source Meetup competitor.
The first 10 parts (posts) of the "Main Story," published over a year, were about building Melitix.
Starting with part 11, let's discuss my early ideas for building Revidian Cloud.

<!--more-->

## What is Revidian Cloud?

My imperfect elevator pitch: "A management hub for all of your Internet assets—domain names, services, TLS certificates, etc."
Considering that what I'm trying to build is still in flux, let's break this elevator pitch down a bit.

I am the classic developer stereotype that buys a lot of domain names for projects that likely never get built.
Due to bargain hunting and top-level domain (TLD) availability, I have a ton of domains with Namecheap but some of them are with Cloudflare, Porkbun, etc.
Revidian Cloud will allow you to view all these domains, regardless of registrar, in one location.
See which domains are in use, have external DNS, compare expiration dates, etc., all in one app.
This is the simple, high-level vision.

Now take what I want to do with domain names and apply it to services (websites and web apps), TLS certificates, and maybe Kubernetes clusters, and that's what Revidian Cloud will be.
Pulling assets into one big hub or dashboard is only one level of what can be done.
An abstraction layer over registrars and DNS providers can enable interesting features.

### Example 1
For example, a company domain name, `PurpleBrothers.com` (made up), was imported into Revidian Cloud.
We have three services set up with it: `www.PurpleBrothers.com`, the marketing site, `email.PurpleBrothers.com`, the email gateway, and `store.PurpleBrothers.com`, the e-commerce store.
In an effort to sound more professional, the company wants to rebrand.
They bought `PurpleIndustries.com` as part of their new name.
They imported that domain name into Revidian Cloud as well.
What could a future Revidian Cloud offer?

I envision a scenario where they would set up `PurpleIndustries.com` as an alias domain to `PurpleBrothers.com`.
This instructs Revidian Cloud to mirror the DNS entries for both domain names so that they point to the same place.
Has the IP address for the marketing site changed?
We change it for one of the domains and the other will change as well, keeping them in sync.
Revidian Cloud could warn you when you try to delete the old domain, reminding you that it's still in an alias pair with the new domain and possibly serving traffic.
Instead, they could schedule when the DNS entries go dark.

### Example 2
Another possible scenario of Revidian Cloud value involves typical DNS entries.
When you want to enable Google Workspaces (or G-Suite, or whatever they call it these days) on a domain name, you must add a set of 5 MX records to your domain's DNS.
Mistype something and it will likely not work.
I see Revidian Cloud offering a simple button you can click to have these entries added automatically.
In fact, I can see Revidian Cloud scanning the DNS entries to quickly tell you which services you have enabled in the domain based on DNS.


## Who is Revidian Cloud for?

Again, I'm still figuring this out but I have an early hypothesis.
Right now I can see Revidian Cloud serving three customer segments:

### Power users
I would fall into this category.
Power users are indie devs and solopreneurs who don't have a large team (or a team at all) and could use a little help managing their Internet assets.

### Enterprises
Large multi-division companies such as Sony or Disney could use Revidian Cloud.
Take Disney for example with brands such as core Disney, Marvel, Star Wars, ESPN, etc.
There's possibly hundreds of domains and websites that they manage.
A tool to consolidate and manage these assets would come in handy at these companies.
They may have some sort of solution already in place that I will need to research but we'll see.

### Agencies
The third group I see Revidian Cloud useful for is local agencies.
Individuals and companies that build and manage websites on behalf of clients.
Juggling multiple accounts at various registrars and providers for each client, a tool like Revidian Cloud would make a lot of sense for management, time savings, and potentially security.
In the near term, I imagine being able to make the most revenue from this customer segment.

It's still extremely early so let's see how that plays out.


## Early Feedback / Try it out

I'm looking for two types of people to try out Revidian Cloud:

1. **Tech-savvy tinkerers.** If you like to try new things, have some domains, and have a product mindset. I would love to discuss the UI and UX and make sure I'm thinking things through and making a decent product. Help kick the tires, even if it's just for fun.  
2. **Potential Users.** Does Revidian Cloud sound like something you will need now or in the near future? If so, I need to hear from you.

Please sign up at [Cloud.Revidian.com](https://cloud.revidian.com/) and I will reach out to you swiftly. Alternatively, you can contact me directly via my contact form or social media. You can find both on my personal website, [Feliciano.Tech](https://www.feliciano.tech/).

<br />

Until the next one,  
Ricardo (FelicianoTech)
