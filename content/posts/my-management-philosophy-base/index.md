---
title: "How I Lead: The Foundation"
date: 2025-11-25
description: "My 4 Pillars of Leadership - Goal, Ownership, Trust, Safety"
tags: ["leadership", "engineering-management", "culture", "team-building", "mental-model"]
categories: ["Leadership"]
series: ["Engineering Leadership"]
showTableOfContents: true
showReadingTime: true
---

After years of leading engineering teams across various organizations and observing entirely different styles of management, I have come to a firm conclusion: ***Effective Leadership is remarkably Quiet***. It is rarely about being the loudest voice in the room or drawing the most impressive architecture on a whiteboard. 

Over my career, transitioning from writing code to managing the teams that ship it - I've learned through trial, error, and countless production deployments to distill my management philosophy into <u>*Four Foundational Pillars*</u>: ***Goal, Integrity, Safety, and  Trust.***

<u>***GIST***</u> is how I lead.

---

## 1. Goal: The "Why" Behind the Code

Engineers do not want to be feature factories. If you hand a team a list of requirements without context, you will get exactly what you asked for, but nothing more. 

Setting a goal is about establishing a shared clarity of purpose. It is the difference between saying, "Implement this new caching layer" and "We need to reduce latency for our mobile users by 20% to improve retention." When the team understands the actual problem we are solving, they are empowered to push back on bad requirements, suggest better architectural trade-offs, and build solutions that actually move the needle.

## 2. Ownership: Autonomy with Accountability

Ownership is often misunderstood as simply being on the hook when things break. Real ownership is end-to-end. 

I expect teams to own the outcome, not just the output. This means an engineer’s job does not end when a pull request is merged. It extends to monitoring the deployment, watching the telemetry, and ensuring the user experience degrades gracefully if a third-party API fails. In return for this level of accountability, leadership must grant the autonomy to make technical decisions. You cannot mandate exactly *how* a system is built and then hold the team accountable if that mandated architecture fails.

## 3. Trust: The Default State

Trust cannot be a carrot dangled at the end of a multi-year roadmap; it has to be the default starting position. 

My job as an Engineering Manager is to hire smart people and trust their expertise. If my lead engineer tells me a system needs to be refactored because the technical debt is slowing down feature velocity, I trust their assessment and advocate for the bandwidth to fix it. Trust also means trusting the team enough to get out of the weeds. I don't need to review every line of code, but I do need to ensure the team has the resources they need to write it well.

## 4. Safety: The Space to Fail

You cannot ask a team to innovate and take massive technical swings if they are terrified of the consequences. 

Safety means that when things go wrong (and they will go wrong), the focus is entirely on the system, not the individual. If a bad configuration takes down a production service, my first question is never "Who did this?" It is "How did our deployment pipeline allow this to reach production?" 

By running blameless post-mortems and treating outages as systemic failures rather than human errors, you build a culture where engineers aren't afraid to take calculated risks.

***

These four pillars are not independent traits; they are load-bearing structures that rely on one another. You cannot have true ownership without trust, and you cannot build trust without safety. 

Once the foundation is set, the way you view challenges and scale your leadership has to adapt over time. I’ll be exploring that next in *How I Lead: The Evolving Lens*.


Leadership is rarely about having the loudest voice in the room or the most impressive technical architecture on a whiteboard. Over my career, moving from writing code to managing the teams that ship it, I have found that effective leadership is remarkably quiet. It is about creating an environment where talented engineers can do their best work without friction.

Through trial, error, and a lot of production deployments, I have distilled my management philosophy into four foundational pillars: Goal, Ownership, Trust, and Safety.

## 1. Goal: The "Why" Behind the Code

Engineers do not want to be feature factories. If you hand a team a list of requirements without context, you will get exactly what you asked for, but nothing more. 

Setting a goal is about establishing a shared clarity of purpose. It is the difference between saying, "Implement this new caching layer" and "We need to reduce latency for our mobile users by 20% to improve retention." When the team understands the actual problem we are solving, they are empowered to push back on bad requirements, suggest better architectural trade-offs, and build solutions that actually move the needle.

## 2. Ownership: Autonomy with Accountability

Ownership is often misunderstood as simply being on the hook when things break. Real ownership is end-to-end. 

I expect teams to own the outcome, not just the output. This means an engineer’s job does not end when a pull request is merged. It extends to monitoring the deployment, watching the telemetry, and ensuring the user experience degrades gracefully if a third-party API fails. In return for this level of accountability, leadership must grant the autonomy to make technical decisions. You cannot mandate exactly *how* a system is built and then hold the team accountable if that mandated architecture fails.

## 3. Trust: The Default State

Trust cannot be a carrot dangled at the end of a multi-year roadmap; it has to be the default starting position. 

My job as an Engineering Manager is to hire smart people and trust their expertise. If my lead engineer tells me a system needs to be refactored because the technical debt is slowing down feature velocity, I trust their assessment and advocate for the bandwidth to fix it. Trust also means trusting the team enough to get out of the weeds. I don't need to review every line of code, but I do need to ensure the team has the resources they need to write it well.

## 4. Safety: The Space to Fail

You cannot ask a team to innovate and take massive technical swings if they are terrified of the consequences. 

Safety means that when things go wrong (and they will go wrong), the focus is entirely on the system, not the individual. If a bad configuration takes down a production service, my first question is never "Who did this?" It is "How did our deployment pipeline allow this to reach production?" 

By running blameless post-mortems and treating outages as systemic failures rather than human errors, you build a culture where engineers aren't afraid to take calculated risks.

***

These four pillars are not independent traits; they are load-bearing structures that rely on one another. You cannot have true ownership without trust, and you cannot build trust without safety. 

Once the foundation is set, the way you view challenges and scale your leadership has to adapt over time. I’ll be exploring that next in *How I Lead: The Evolving Lens*.

## Start with trust, not process

Most management frameworks lead with process: standups, retros, planning ceremonies, ticket hygiene. I lead with trust.

Process without trust is just overhead. Engineers will comply with your ceremonies and route around your intent. But when engineers trust their manager — when they believe you have their back, that you will not weaponize their vulnerabilities, that you will fight for them when it matters — the process becomes almost secondary. They show up differently. They take risks. They tell you the truth early, before problems metastasize.

Building trust is not complicated either. Show up consistently. Do what you say you will do. Protect your team when the pressure is external. Hold them accountable when it is internal. Never surprise them with feedback they have not already heard in private. Be the same person in a 1:1 as you are in an executive review.

That is the whole thing. Trust is not a program. It is a pattern.

---

## Set clear expectations, then get out of the way

Micromanagement is almost always a symptom of unclear expectations. If you have not told an engineer what "great" looks like, you end up watching their work too closely because you have no other signal.

The fix is to front-load clarity. Before someone starts a project, before a quarter kicks off, before a new hire finishes onboarding — invest the time to make the expectations explicit. What does success look like? What does failure look like? Where is the bar? What decisions can they make on their own, and which ones should they loop you in on?

Once that is clear, step back. Talented engineers do not need a manager watching over their shoulder. They need the goal, the context, and the runway.

---

## Recognize strengths and lean into them

Every engineer on a team has something they are exceptional at. The manager's job is to find it — sometimes before they have found it themselves — and then build the conditions where that strength gets used.

I am not talking about painting everyone's weakness as a hidden strength. I am talking about genuinely identifying what each person brings to the team and building around it. The engineer who is brilliant at systems thinking gets pulled into architecture conversations. The engineer who communicates exceptionally well becomes the face of the team in cross-functional discussions. The engineer who codes fast and clean gets to set the technical bar on a critical path.

Strength-based management is not just good for morale. It produces better outcomes. People do their best work when they are doing work that plays to who they are.

---

## Be the safety net

The most important thing I do as a manager is make sure my team knows I have their back.

This means that when they make a mistake — and they will, because that is what people do when they are taking real risks and doing real work — the first question they ask is not "will I get in trouble?" but "how do we fix this?"

It means that when organizational pressure comes from above or from peers, I absorb what I can so my team can stay focused.

It means that when someone on my team is struggling — with the work, with a colleague, with something in their life — they feel safe enough to tell me.

None of this means I shield people from accountability. Clear expectations mean there is accountability built in. But accountability and safety are not opposites. The best teams I have built had both: people knew the bar, and they knew someone was in their corner while they tried to clear it.

---

## Zero tolerance for politics

I genuinely do not care whose team did what. "My team vs your team" thinking is one of the most corrosive forces in any engineering organization, and I work hard to excise it wherever it shows up.

The engineers and managers I respect most are the ones who make the whole org better, not just their corner of it. Who share credit, flag issues that are not technically their problem, and treat cross-functional partners like collaborators rather than obstacles.

I try to model this. I try to hire for it. And I try to call it out — directly, in the moment — when I see it happening around me.

---

## Trust the engineers closest to the code

I came up as a software engineer. I can hold a design conversation, read a post-mortem, and tell when an architecture decision smells wrong. But I have never confused that fluency with expertise.

The engineers closest to the codebase know things I do not. They know which parts of the system are fragile. They know which technical debt is actually fine and which is a ticking clock. They know what the junior engineer on their left is struggling with and what the principal engineer on their right is excited about.

My job is to stay informed enough to ask good questions and make good resourcing decisions — not to pretend I have the technical answers. I lean on my Principal Engineers for direction, and I trust my senior engineers to own the decisions within that direction.

That trust is not blind. It is earned incrementally, the same way all trust is. But the default is trust, not skepticism. And that default changes everything.

---

## The short version

If I had to put my whole management philosophy on a sticky note:

> *Set clear expectations. Build trust before you build anything else. Find each person's strength and use it. Have their back. Stay out of the politics. Trust the engineers closest to the work.*

Everything else is tactics.

---

*This is the first post in a series on engineering leadership. Next up: how I think about merging two engineering teams without losing either culture.*
