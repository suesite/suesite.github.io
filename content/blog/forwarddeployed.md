---
title: Which direction is forward?
description: Software role changes tell us something about the goal of AI companies.
date: 2026-05-19
---

There’s a role that appears to be exploding in popularity in AI adjacent companies right now: the Forward Deployed Engineer. Since I first heard about LLM assisted coding, aside from the very real enabling potential, I’ve worried that the outcome would be a future where fewer people understood how critical systems worked. I believe some of what we’re seeing with these jobs is a reflection of that.

<!-- excerpt -->

Software companies have long had engineering roles embedded in the sales cycle. Sales engineers might build demos and proofs of concept pre-sales. Solutions engineers and architects set up bespoke configurations or integrations of a product for specific customers. Field engineers might support client implementations in their environments. Now we have these “forward deployed” engineers.

> The role name comes from Palantir and is borrowed from military language (shoutout to [@tante](https://glasgow.social/@tante@tldr.nettime.org/116595174714390869) for informing me of this on mastodon). 

If you’ve worked at a SaaS (Software as a Service) company, you’ll likely be aware that conflict often arises in deciding what to build. In theory product management leads the decision, in collaboration with engineering, with input from sales / customer engagement. In practice it’s usually more complicated.

## Services vs scale

When your product is software, integrating it into a customer’s system can involve building additional software to support the integration. This is something a solutions engineer might do. If your solutions folk are constantly building the same stuff to get your product in place for customers, it might make sense to incorporate what they’re building into the product itself. That way the same solution benefits your other customers, making it easier (and cheaper) to onboard new customers.

The golden rule for SaaS companies was to build for scale. If you depend too heavily on professional services (what those solutions engineers do), growing your customer base means hiring more and more people to service it. The more you can automate by supporting common customer use cases through the product itself, the more easily you can scale to support a steeper growth trajectory.

So far so good, but what one customer needs might not actually be what others need, in fact there can be many reasons not to incorporate a solution into your core product. This is where product management comes in. PMs determine what to include in the roadmap, what the future of the product should be – in doing that they define the bounds of the product, where its edges are. What falls within its bounds is the software you commit to making available at scale, and maintaining over the longer term. 

Product managers liaise with engineering and other teams to determine what is feasible and in the interests of the company’s overall plan. With these constraints in mind, the short and long term goals of the company theoretically determine whether or not those customer integrations become part of the product itself. 

> When we build this way, it becomes important for a significant portion of the people who work at a company to understand something about what the product does, in order to carry out their own duties. Internal communication about the product therefore becomes a priority.

## Who's driving the bus

When those sales-situated engineering roles are clearly defined, it creates a dialogue with customers that makes the product more likely to be successful. In practice it often creates pressure on the relationships between teams. If a customer is a big enough deal for the company, their input can effectively hijack the product process and force prioritisation that benefits them, more than it does your future as the vendor. 

Compensation structures are part of this story too. Where product engineers are typically paid in salary and perhaps bonuses / stock, engineers who work in sales are paid partly in commission. The incentivisation difference creates divergent views of what success looks like.

Sometimes these teams are effectively disconnected from the product process, deploying whatever specific customers need – your software ends up a hundred different things to a hundred different customers, and congrats, you've accidentally become a dev shop instead of a product company. Shifting control away from product management can also **reduce visibility into what is actually being delivered**. 

It used to be that the lack of scalability curbed dependence on building in this service-oriented way, certainly for startups if not large incumbent corporations. But there’s a huge push to get this tech embedded inside organisations by any means necessary, so that the need to demonstrate value – and justify the inevitable price hikes that follow deep subsidisation – become redundant. 

## Who's being escorted out of the room

The rise of these roles is accompanied by an increasing trend in AI-excused layoffs, citing “flattening” management structures as the goal. Companies are laying off middle managers, many of them in product, and telling an unconvincing tale that AI is automating what they did. 

_If this was about building products to better suit real world use cases, I don't believe we'd be using these distinct job titles, or getting rid of managers en masse._

Developers often hate on management, but the role being sidelined has wider consequences. **Part of what product managers do is make intention legible to the company.** They frame a product in terms of vision and value, helping teams around the company to understand what is getting built. By putting customer-embedded engineers in a position to decide what gets built instead, employees lose both visibility into what they are shipping, and opportunities to influence it collectively. 

> Reducing worker understanding of what is being built is a long established labour-crushing tactic. Losing the ability to understand what your company is shipping means losing paths through which we might minimise the harms our software causes.

## Finding leverage

Couple all of this with the deployment of LLMs to generate code in a way that obfuscates understanding of it, and you can see where we’re headed. A world where it's harder to understand systems that affect us. This is why I’m focusing on helping people to understand codebases, and building tooling for that purpose. LLMs can actually aid that understanding – they are being weaponised with clear intention to undermine it.

The primary push for LLM code generation is part of an attempt at deskilling software engineers, but I don't believe it will work. I think it's based on a misunderstanding of what LLMs can do, and what software engineering is. More code in the world is going to mean leverage for people who can understand and change it, we should be ready to take advantage of that.
