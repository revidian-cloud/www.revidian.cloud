---
title: "Part 4: Launching Melitix Next Month Yet Starting a Rewrite"
author: FelicianoTech
date: "2024-03-31T18:00:00-04:00"
categories:
  - "Main Story"
tags:
  - ""
---

In my [first weekly blog post](/blog/week-1--starting-from-scratch--sort-of/), I mentioned that I was "sort of" starting from scratch.
While I was creating a new company, I was starting off with the code from the [Get Together project](https://github.com/GetTogetherComm/GetTogether).
This decision allowed me to start with a working app and lay improvements on top rather than building an entire app from scratch.

Using an existing codebase was supposed to be a competitive advantage, so near the end of [last week's post](/blog/week-3--two-steps-forward-one-step-back/), I stated that I would be launching in April.
So why, on that very night, did I decide to completely rewrite the entire codebase weeks before launching?
Well, I have my reasons.
The better question in the future will be, was it worth it?


## My concerns with the existing codebase

I had some concerns with the Get Together codebase going in.
The project's creator even warned me about the age of the framework on which the app is built, so I wasn't surprised by the issues I was facing.
Here are the problems I had.

### Get Together was written in Python
Python is the programming language used to write Get Together.
I know enough Python to get by, but it isn't a language I'm very comfortable with.
Since the codebase is old, it runs well with older Python releases, but I had trouble getting it running with the latest releases.

### Get Together uses Django v3
Django is a web framework written in Python.
Web frameworks can be used to create web apps faster than writing the same app entirely from scratch.
I have little experience with Django, but it's popular.
The problem here is that Get Together is using v3, while v5 is the latest release.
Upgrading the codebase through two major releases will be challenging for a Python amateur.

### Old Dependencies
The issue with very old dependencies is touched on in the Python and Django paragraphs above, but it doesn't end there.
In the `requirements.txt` file, where all of the code dependencies for Python are declared, many of the project versions in use are very old.
There are tons of bug fixes and, more importantly, security fixes that need to be brought into the project.
Again, this would be a good bit of work for me.

### Testing
Earlier this month, I started the work to get the project built and tested on CircleCI.
What I discovered is there are only a few tests.
That's okay.
Many open-source and proprietary projects are not as well-tested as they should be.
I get it.
The problem was, of the few tests, a couple of them weren't passing.

These failing tests made me rethink the decision to use the codebase.
In trying to weigh the pros and cons of using the codebase vs starting over, the failing tests made me lose confidence in the Get Together codebase.


## Rewriting the code

I wanted to launch in April, but the existing code was making me feel nervous.
Rewriting the code would alleviate those concerns but could delay the launch a month or more.

I decided to give myself a challenge.
I would start a rewrite of the codebase for precisely one week.
If I made significant progress in that week, I would continue.
Otherwise, I would tough it out with the Get Together Python code.
Here we are a week later, and I would guesstimate that I'm 50% of the way through the rewrite.
For only seven days of work, I'm happy with that progress.

### What I'm hoping to achieve
I'm rewriting the Get Together project in the Go programming language.
It's a language that I LOVE, very fast, and with which I have some prior work.
This allows me to borrow code from my other Go web apps to use for this week.

The switch to Go means I get a fast codebase with up-to-date packages.
Theoretically, this means a more secure web app for the users.
There's also a business aspect to this.

### Entrepreneurial decisions
When I still had a co-founder for this project, I could afford to spend more time learning Python, Django, and the existing Get Together codebase.
I had someone else to worry about marketing and sales and to share the execution load with me.
As a solopreneur, my mindset has changed.

I will not only be coding the software but also wearing all hats in the business.
I need to be more flexible and efficient in where I spend my time.
My hope is that this rewrite is an investment—an investment that will pay off with a faster turnaround for bug fixing and feature development after launch.

<br />

Until next week,  
Ricardo (FelicianoTech)
