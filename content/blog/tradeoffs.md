---
title: Automation is a trade-off
description: We should have more explicit conversations about the trade-offs we make when we use automations.
date: 2026-04-28
canonical: https://dev.to/suesmith/automation-is-a-trade-off-2fh8
---

___This post was originally published on [dev.to](https://dev.to/suesmith/automation-is-a-trade-off-2fh8).___

![artwork of a solar microscope drawing box](machine.jpg)

A couple of years ago I wrote [a post about abstractions](https://dev.to/suesmith/abstractions-no-not-like-that-3pl3). I’m revisiting it here with AI-assisted coding in mind, because I see similar issues arising. LLMs make it easier than ever to generate code, but when we look at what happens next, the picture becomes a little bit less clear.

<!-- excerpt -->

When you build an abstraction or automation intended for use by other people, you make a decision about **what is valuable for them to know about**, and what isn’t. In programming this is extraordinarily hard. Often we accidentally hide information it turns out the user needs or wants to know about. And it can change over time, because in software, context has a huge influence over how and what we build. 

The world of APIs grew from the power of being able to import code written by others – we were able to focus on the unique aspects of our own problems / solutions. But choosing to use a dependency has consequences we didn’t always take seriously. It’s a trade-off I wish we were having more explicit conversations about with AI.

> ⚠️ _I should note that I don’t view LLM prompts as programming abstractions but as code generation automations, for reasons I’ve been exploring in [recent talks](https://www.sue.codes/blog/fingerscode/)._

## Progressive Disclosure?

One approach to managing the trade-off is to provide a kind of [escape hatch](https://www.nngroup.com/articles/progressive-disclosure/) where you can see and configure the underlying implementation if you want, or ignore it if you don’t need to know what’s going on under there.

Here’s where I get skeptical about vibe coding platforms positioning themselves as _empowering_. I won’t name the company, but I recently tried generating a simple static website from a service aimed at people without prior coding skills. I exported the app to VS Code. The implementation was ludicrously over-engineered, with a ton of TypeScript files and **zero** documentation. Not a code comment, not a README, nothing. The output was effectively obfuscated. Even as an experienced developer I would have had an extremely hard time working with this codebase.

Perhaps you’re wondering if this is an edge case, assuming these codebases don’t need to be worked on directly. I pay close attention to accounts from people using these services and that's not what I'm finding. Overwhelmingly they get you to a prototype, but in order to take your app to the next level you do need to engage with the code. Even the platforms themselves have subtly shifted their messaging to reflect this.

## The interface is not the LLM

The platforms I'm referring to here are a little different from e.g. using an assistant or agent in your IDE. The underlying prompts and LLM scaffolding are partly or wholly hidden from the user. They could easily instruct the model to prefer human-readable implementations and provide ample documentation – to produce programs that are optimized for the user to learn from, and that act as a foundation to build on. That would be empowering.

Here’s another awkward piece of the puzzle. In order to ask the model for such an enabling starting point, you already need to know something about how software is built. So that precludes anyone without prior development experience. 

## Let’s talk about the trade-offs

Here are some considerations I think are valuable when it comes to either designing or using an automation for code generation:

* **What details are being hidden from the user?**
* **What decisions are being made about the implementation?**
  * **Are the decisions accidental or deliberate, what is driving them?**
* **How can these decisions be changed?**

Importantly:

* **What might the user need to know later that they don’t know now?**

Taking a moment to answer these questions might help us make better choices about the abstractions we build, and those we choose to adopt.

## What does empowerment look like?

Sometimes I imagine a platform like Glitch, but that generates apps from a prompt, while prioritizing ease of extension and subsequent learning – what the Glitch Hello apps were meticulously designed to do. Such a thing is absolutely feasible, at least technically. But the reality is that software company decisions are determined by economic dynamics. They are incentivized to prioritize engagement over enablement – in many cases what this looks like is platform lock-in.

I do see people being enabled to build software using LLMs, usually with the support of other human beings in their workplaces or communities. There is tremendous potential for opening the gateway to developer skills with this technology, but it won’t happen by accident, and we should scrutinize claims of empowerment that don’t check out when we scratch the surface.

## What does accountability look like?

There’s a parallel problem even professional developers are experiencing, as AI-generated code is harder to work with, increasing the maintenance burden over time. Using LLMs to generate code is reducing our ability to build strong mental models of our codebases. Again, I don’t believe this has to be the case, we could use these automations while still preserving agency and understanding.

For working developers, the question of accountability plays a huge role here. When things go wrong, who is held responsible, and what are the consequences? Understanding what you’re committing to a codebase has implications I don’t believe we’ve fully reckoned with yet.

## We can shape this

As we begin to discover the longer term consequences of using LLMs to generate code, I would love to see more honest conversations about what is truly involved in enabling people over both the short and long term. Because we can build for that if we want to.
