---
title: How should we teach software development now?
description: Exploring software development learning topics in the context of AI-assisted coding.
date: 2026-04-30
---

Yesterday I [posted on LinkedIn](https://www.linkedin.com/posts/sue-smith-benormal_ive-been-thinking-and-posting-about-ai-assisted-activity-7455333012457738240-1n7y) about realising I've been thinking and writing about AI-assisted coding for three years now, and that overwhelmingly I still stand by the positions I've taken. My first public post on the subject was in May 2023, so I'm going to revisit it on the same day this year. But for now, since the discussion touched on what we should be teaching on software engineering courses, it prompted me to jot down my current thinking, still very much WIP but here you go.

<!-- excerpt -->

⚠️ _Note that this is squarely focused on courses where the goal is to learn the skills in being a working software developer. Many other courses involve writing code as a technique in service of some other goal – strategies will vary enormously there, as the potential to lean more heavily on LLMs to generate code increases on small scale, low complexity apps. The skills I'm focused on here are for preparing to work on the kind of complex systems teams of software engineers collaborate on._

1. I thoroughly recommend restricting reliance on LLMs when teaching programming fundamentals. It's unrealistic to expect to eliminate it, but as far as possible I'd get students up to speed with the basics the "old fashioned" way, by writing their code manually.

2. I would also look to the humanities, where educators are using LLMs to generate content, then having the students engage in critical thinking about the output. Raspberry Pi Foundation have shared resources for similar, covering topics like [anthropomorphism](https://www.raspberrypi.org/blog/ai-education-anthropomorphism/).

> _These first two are essentially focused on harm reduction regarding the negative consequences of LLMs being available. That's unfortunate but necessary at this stage._

3. Explore using LLMs to aid activities such as debugging and code comprehension. We're going to need a heavier focus on code reading skills when lots more code is being generated, and I'm cautiously optimistic we'll see the rise of better tooling to support these practices. Similarly, with the explosion in outages and incidents, I have to assume performance and security topics are going to be more central to the working life of a developer.

4. I think there's tremendous potential to use LLMs to generate practice exercises dynamically. Mostly I see anecdotal accounts of people doing this, but again I'm hopeful we'll have dedicated tooling to enable it. Having an LLM generate a broken project the learner has to fix is an idea I'd like to experiment with.

5. In terms of developing *with* LLMs, this is where I'm more hesitant. I'm thinking writing specifications, LLM scaffolding etc (the many and varied markdown files involved in effective deployment of this stuff). I would tend to treat this as an advanced topic, second to e.g. learning a foundation in programming with one or two existing languages. It might seem frustrating to not be leveraging recent technology straight away, but I storngly believe an upfront investment in these foundational skills will pay off in the long run.

In industry settings, the overarching advice I'd give is to [build a culture of learning](/blog/oneanswer/) in your organisation. That is of course not a trivial task, but a good start would be encouraging tactics like peer learning, pair programming, and mentorship – these are going to be more valuable and essential than ever.

I am a broken record on this but Raspberry Pi Foundation publish phenomenal resources on teaching programming in the context of AI:

* [AI pedagogy quick reads](https://www.raspberrypi.org/blog/pedagogy-quick-reads-turning-abstract-ideas-into-classroom-practice/)
* [Experience AI](https://experience-ai.org/en/units)
* [The Hello World magazine](https://www.raspberrypi.org/hello-world/) which has tons of example lessons

I am extremely interested in hearing other perspectives on teaching with this stuff!