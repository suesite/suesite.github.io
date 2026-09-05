---
title: Harnesses are just software
description: Learning what is happening in the software around the model.
date: 2026-09-05
img: https://www.sue.codes/harnessdog.jpg
---

When I decided I wanted to make a programming learning tool that incorporates LLMs, I chose to build for IDEs, starting with VS Code. I did that because I believed there would be value in steering people back towards code, and because it would let me build with LLMs in a **model agnostic** way. What's happening with open models and model companies in general is making me glad I didn't target one of their platforms.

![a dog in a parachute harness](harnessdog.jpg)

_A ["war dog"](https://commons.wikimedia.org/wiki/File:War_Dog_Reception_and_Training_Center,_San_Carlos,_California_German_shepherd,_%22Pal%22,_gets_fitted_for_a_dog_parachute_harness_for_rescuing_fliers,_circa_1944_(cropped).jpg) being fitted for a parachute harness._

<!-- excerpt -->

What I'm also coming face to face with is how much of the magic people are experiencing isn't from the models themselves, but in the software around them – the harness if you must call it that. 

I'm mostly making LLM requests directly in my code rather than e.g. leveraging the copilot orchestration you benefit from when you use the chat. I've experimented by providing tool access to run agent style loops and parse the results programmatically, to replicate a little of what copilot itself does. It's all giving me a more tangible sense of the smoke and mirrors that are at work in most of the interfaces to this stuff.

## A peculiar kind of data

If it isn’t obvious, a harness is just software. The LLM calls provide a way to incorporate data into your processing, but it's a very peculiar, unpredictable kind of data. You need to heavily constrain what you send and receive the model – the harness has to behave like a very paranoid API client. 

The range of possible inputs and outputs is endless. It's partly why people are having such chronic disagreements about the value of this technology, because they’re having wildly different experiences using it and talking past one another as a result. Learning how to use the model where it's most beneficial (and least wasteful) is quite a task. 

## This is where we can find leverage

The good news is that harnesses are a wide open space where we can shape the experience of using these technologies. And we can teach folk about harnesses just the same way we taught them about other software. Don't let the mystifying naming fool you.

> There's still so much opportunity to build pathways that illuminate rather than obfuscate, that enable rather than undermine, that center the human operator rather than seeking to automate them out of the process.

What's happened to the web over the last couple of decades made it harder for people to perceive what is going on under the hood when they interact with software. It initially alarmed me how much more opaque LLMs seemed to make the situation, but the reality of the split between model and harness gives me new hope we can teach people how to understand and change the software systems that affect them. As it turns out language models are quite handy for that.
