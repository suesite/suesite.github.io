---
title: On convenience and understanding
description: Can we leverage automation while still preserving understanding?
date: 2026-05-07
---

> _"There is some compulsion in software where automation breeds more automation and we accidentally leap over the phase where it was actually optimal for both usefulness and understanding."_ [Me, on mastodon the other day](https://glasgow.social/@sue/116499571969099762)

**Being able to generate code is forcing us to figure out when it’s a good idea to actually write it.**

<!-- excerpt -->

Recently I’ve found myself making a few small static websites, and I’ve come face to face with this choice, although not regarding LLMs. The last decade or so saw the growth of generated static site frameworks. These let you create websites without hand coding every bit of HTML. They’re handy for reusing layouts in your pages, and giving you a single point of change if you decide to redesign your site. However, it’s a lot harder to understand what’s going on under the hood, and harder to set up than what we did before – write HTML in a text editor and upload the files to a server.

A few years back I decided to brush up on my frontend skills, having been focused on server side development for several years. During that time, generated static site frameworks had exploded. I discovered I had to set up a dev environment, and go through a build and deploy process, just to get a simple website online. I was like wtf are we doing here. It had become a lot harder to teach people how to get started making websites. 

## To automate, or not

Naturally I am biased, but Glitch did a great job of keeping the door open to new developers by abstracting some of this away. Setting up dev environments is understanding I frankly wish I'd never had to develop. It's not relevant to the goals I care about – usually those relate to the content and functionality of a site I'm working on. I want to comprehend the logic in the code that gets deployed to the web, not so interested in deployment pipelines and the like. Having used Glitch to teach people who'd never written code before, I can say the balance of automation and understanding was a pretty good match for what they cared about.

As I approached making those simple websites recently, I realised it would be handy to be able to reuse layouts, but certainly didn’t need the power of a full static site framework. So I decided to write some small scripts to use templating libraries, so that I could generate my pages locally and just dump them online. It felt like I was seeking some lost stage of automation we skipped over but that was optimal for my purposes, before our automations obfuscated the bejesus out of everything.

When you learn how to automate making things with code, it can become a habit you jump to instinctively. We automate one thing and immediately leap to automating more and more of the same process. But each automation comes at the cost of understanding. Too often we’ve taken things far enough to sacrifice understanding in ways that created new problems – for learners, for teams, even for ourselves when we looked back at projects we’d previously worked on.

## We're here again

Choosing when and how to leverage LLMs to generate code is subject to the same balancing act. This automation gives us the opportunity to opt out of understanding that is not relevant to our goals. But how do we know when it is worth prioritising understanding? Well it’s difficult to make that call in the moment, because typically we find out we’ve got it wrong later. For that reason I’d recommend a regular practice of revisiting your comprehension of the projects you work on. If you feel you’re losing your sense of wtf is going on *in a way that is relevant to your goals*, take a step back and course correct.
