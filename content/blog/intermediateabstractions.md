---
title: In search of intermediate abstractions
description: Working with LLM generated code effectively requires some intermediate abstractions.
date: 2026-10-21
img: https://www.sue.codes/fusebox.jpg
---

![a fusebox on its side](fusebox.jpg)

Teams using LLMs to build software are still figuring out how to handle the mountain of code that now needs read if you aren't delegating all of that to agents. I'm increasingly convinced we need interventions that support human comprehension of code, for many individual and organisational reasons. Reading all of our generated code line by line is not feasible, but referring purely to specifications, prompts etc that were used to generate it is inadequate when it comes to knowing what is actually going on in a system. 

__We need intermediate levels of abstraction that help us to be more strategic about what we attempt to understand in codebases.__

<!-- excerpt -->

> Enjoyed this Ray Myers post which touches on abstractions: ["Coding" is largely "Solved"](https://raymyers.org/post/coding-is-largely-something/)

## Pick your lens

I'm working on a codebase comprehension tool called [Randan](https://www.randan.dev) right now. Its goal is helping people get to know an application they either generated or inherited and now need to understand.

There are many different levels of detail at which we can analyse and build understanding of a codebase. Here are some examples:

* All of the source code
* The directory structure
* Application entry points
* Dependency maps
* Script file structures
* Content of particularly high signal files
* The user interface
* Behaviour during execution

In my extension, I'm using a combination of static and dynamic analysis at some of these levels, plus input from a language model.

<div class="container">
<iframe src="https://www.youtube.com/embed/IhsG38VHPtE" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</div>

The script file structure can itself be represented in a range of ways – from the deep language-specific analysis you might get with an abstract syntax tree utility like typescript's compiler tooling, or a language parsing tool like tree-sitter – _to the higher level language-agnostic extension APIs exposed by IDEs_. 

## Choose your seats

I decided I wanted to remain at whichever level let me work across languages, so that I could focus on the "comprehension" algorithm, so I'm leaning a lot on the VS Code [Document Symbol](https://code.visualstudio.com/api/references/vscode-api#DocumentSymbol) API. The Document Symbol provider gives you a hierarchical list of "symbols" in a script file. Symbols can be code components like functions, variables, events, and so on. Reliability varies enormously by language and of course reflects how well supported the language is by the tooling for it in the IDE.

The symbol APIs (there are a couple of others) sit above the language server, creating an abstraction that represents programming structures in a language-agnostic way. Once you have a list of symbols to explore, you can dig further into information like the call hierarchy and references. I'm using these representations to inform some dynamic analysis that the extension then conducts at runtime.

The downside to the level of analysis I'm using most is that it's tailored to the IDE. So if I decide e.g. to port this to Jetbrains I'll likely need to do some thinking about how to represent similar behavior via its APIs. 

## Check the UIs

A good way to learn which of these types of abstraction are available in any IDE is taking a look at the views you can access during code editing and execution (particularly in debug mode). Views like document outlines, call stacks etc represent the IDE makers' default selection of information that might be helpful to a developer working on a project. These are typically super configurable to accommodate the myriad ways in which we make sense of software programs in order to work on them.

> Harnesses for working with LLMs in IDEs leverage some of these APIs behind the scenes.

Often these abstractions are exposed in the UI with the option of revealing more detail on demand, so that as a developer you can drill down in specific places. This principle of progressive disclosure seems particularly valuable right now – ___being able to choose the level of fidelity that suits a task is key___.

## From analysis to understanding

I'm using language model queries in conjunction with a few different rounds of analysis, to identify places likely to be instructive for first investigations of a codebase (based on recognising patterns from projects in the training data) and generating natural language descriptions of what's happening when the code at those locations executes. The aim is to help someone construct a mental model of a project they're working on and build the confidence they need to take ownership of it.

I've long wanted to create learning supports that illuminate the space between code in a file and what happens when a program runs. Exploring these intermediate levels of abstraction feels key to that purpose.