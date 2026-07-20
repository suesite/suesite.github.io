---
title: The proofs are in the pudding
description: Learning about static analysis is teaching me about robustness and effectiveness.
date: 2026-07-20
---

I’ve been making myself describe the project I’m working on so that I can get input on some design decisions. I stumbled on a timely [LinkedIn post](https://www.linkedin.com/posts/vincentlextrait_an-overdue-analysis-of-claude-code-behind-ugcPost-7476646859185233920-7RFe/) about how Claude Code works. It touches on static analysis, something I’m having to learn a wee bit about for my project. The post is focused on claims of machine understanding – I’m not particularly interested in those kinds of conversation as I don’t see the value. However the detail might speak to the limitations of LLMs in practice, which I do care about because it affects the power of this technology to undermine labour. But I digress.

<!-- excerpt -->

## Seeing the wood _and_ the trees

In my project, I need to make a series of trade-offs in processing the content of a codebase. The project is aimed at helping people understand how a software system works, using a combination of direct analysis and language model queries. It’s something I’ve wanted to build for a long time, but the arrival of LLMs makes it more feasible, and makes a more comprehensive solution possible with minimal investment – not by generating code, but by integrating language models programmatically to support user understanding. 

I'm building this because what concerns me most about LLMs is the reduction in code comprehension we're watching unfold. More software in the world and fewer people who understand it is [a prospect that alarms me](https://www.sue.codes/blog/stillteach/), because understanding how systems work enables us to influence them.

## A very weird database query

Deciding where to insert the LLM call, what information to pass it – and therefore what to carry out before querying it – is turning out to be the bulk of the work. I’m doing a bit of static analysis in the application itself, passing the output of that to the model, then doing more processing on the response. Defining the bounds of the functionality I author in the app means specifying the interface with the model. I'm having to think about which signifiers in a codebase are most informative.

I could keep building more and more processing into the analysis to improve the quality of the info I send the model, but there’s a point at which it’s not worth the additional coding or execution resources. What I’m after is a first pass at some information that I’m going to build into further anlaysis, and update as more information becomes available. **There is no one correct answer to the query**, and no real benchmark or baseline to check it against.

>  I need to strike a balance between the robustness of deterministic processing on the static / dynamic analysis with the unreliable but semantically helpful language model input. The LLM is helping in two ways:
> * Identifying key location candidates based on pattern matching from so many codebases in the training data
> * Providing natural language explanations of the code points 

## That'll do prompt

In software we often face this tension between robustness and effort (both human and machine). Platforms that are successful don’t win because they prioritise an exhaustive solution, they win primarily on account of what they enable people to do – by solving a real problem and presenting an interface people can use. Many of the products that have achieved mass adoption hide unsophisticated, inefficient implementations under the hood, but they’re available and usable.

> Criticism of AI platform implementation is [academic](https://glasgow.social/@sue/116872943163360034) as long as the results are good enough in practice, in context. It doesn't really matter how many research papers prove something isn't what it's claimed to be, what matters is what plays out in practice – these insights can inform that, but they don't change outcomes when more powerful dynamics are at play. 


I'm highly sceptical about LLMs being able to generate anything of signficiant complexity without engineering knowhow, but there are places where a guess based on training data is good enough to complete a task.

**What level of fidelity is good enough depends entirely on context.** None of us are paying attention to all possible implementation details. Even if we’re not using LLMs, we’re mostly writing in high level programming languages, using dependencies and APIs to abstract away the detail we’ve decided not to pay attention to. Making solid judgements about [what level of detail](https://www.sue.codes/blog/tradeoffs/) is suited to a particular task is the trick.

___You can see a teeny tiny preview of some early progress on my project over at [randan.dev](https://www.randan.dev).___

