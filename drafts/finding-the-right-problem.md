---
title: "Finding the Right Problem: The Art of Narrowing Scope in Forward-Deployed Engineering"
slug: finding-the-right-problem
author: 
status: draft
created_date: 2026-01-13
published_date: 
last_updated: 2026-01-13
tags:
  - forward-deployed
  - problem-definition
  - scope
  - prioritization
  - strategy
categories:
  - software-engineering
  - team-dynamics
summary: "In forward-deployed engineering, finding the right problem isn't about finding any problem worth solving—it's about narrowing scope to the most important thing to solve right now."
---

# Finding the Right Problem: The Art of Narrowing Scope in Forward-Deployed Engineering

## Introduction

When you start a forward-deployed engagement, you're rarely handed a well-defined problem. You're handed a landscape of problems. Pain points, ambitions, technical debt, organizational friction, unmet customer needs—all tangled together in ways that aren't immediately obvious.

The temptation is to try to solve it all. Or at least, to solve as much as possible. You're here to help, after all. The partner has needs. The clock is ticking.

But I've learned—sometimes the hard way—that trying to solve everything is one of the fastest paths to solving nothing well. The engagements that succeed aren't the ones that tackle the broadest scope. They're the ones that find the right problem and solve it deeply.

That said, sometimes what the partner actually needs is general guidance rather than a deep solution to a specific problem. They want advice, direction, a sounding board—not a team building something alongside them. That's valid. But even then, the scope needs to be clearly defined. "General guidance" isn't a scope—it's the absence of one. What kind of guidance? On what topics? To what end? The requirement might be advisory rather than delivery-focused, but it still needs boundaries. Understanding what the partner actually wants—whether it's a solved problem, a strategic recommendation, or something else entirely—is itself a narrowing exercise. You can't serve them well until you know what "well" looks like.

Finding the right problem, in this context, means one thing: narrowing scope until you've identified the most important thing to solve. Not the most interesting thing. Not the thing you're best equipped to solve. The thing that matters most to the partner, right now, given their constraints and capabilities.

This post is about how to do that narrowing, why it's harder than it sounds, and why getting it right changes everything.

## Why Broad Scope Fails

Let's start with the failure mode. An engagement begins with discovery. The partner shares their challenges. You listen, you ask questions, you take notes. By the end, you have a list. It's a long list.

The natural instinct is to organize that list, prioritize it, and start working through it. Maybe you'll get to everything, maybe you won't, but at least you're making progress across multiple fronts.

Here's what actually happens:

**Effort gets diluted.** When you're working on five problems at once, you're not giving any of them the depth they deserve. You make surface-level progress everywhere but transformative progress nowhere.

**Timelines slip.** Broad scope means more dependencies, more unknowns, more coordination overhead. What looked achievable on paper becomes unachievable in practice.

**The partner can't absorb it.** Even if you somehow deliver on everything, the partner team has to take ownership of all of it. A broad scope means a broad knowledge transfer burden. They end up with partial understanding of many things instead of deep understanding of the thing that matters.

**Impact becomes diffuse.** When the engagement ends, what was the outcome? "We made improvements across several areas" is a hard story to tell. It doesn't land with stakeholders. It doesn't demonstrate clear value.

**You lose the thread.** Midway through the engagement, priorities shift. New information emerges. With broad scope, you don't have a clear anchor. Everything is in flight, so everything is up for renegotiation.

Broad scope feels ambitious. It feels like you're maximizing value. But in practice, it's often a way of avoiding the harder question: what actually matters most?

## What "Finding the Right Problem" Means

Finding the right problem isn't about finding a problem worth solving. In any forward-deployed engagement, there are dozens of problems worth solving. The question is: which one is the most important to solve given the time, resources, and context you're working within?

This is a narrowing exercise. You start with the full landscape and you reduce, reduce, reduce until you've arrived at something specific enough to solve well.

### The Right Problem Is Narrow

If you can't explain the problem in a sentence or two, it's probably too broad. "Improve the data pipeline" isn't a problem—it's a category. "Reduce pipeline latency for the nightly batch job from 8 hours to under 2" is a problem.

Narrow problems have clear boundaries. You know what's in scope and what's out. You can tell when you've solved them.

### The Right Problem Is High-Impact

Narrowing isn't just about picking something small. It's about picking something small that matters disproportionately. The right problem, when solved, creates momentum. It unblocks other things. It demonstrates value. It builds trust.

Ask: if we only solve this one thing, will the engagement still be considered a success? If the answer is no, you might not have found the right problem yet.

### The Right Problem Is Solvable

This sounds obvious, but it's easy to miss. The right problem is one you can actually solve in the time available, with the people available, given the constraints that exist. Ambition is good. Fantasy is not.

Some problems are important but not solvable—at least not by you, not now. They require organizational change, budget allocation, or capabilities that don't exist yet. Those problems might be worth naming, but they're not the right problem to focus an engagement on.

### The Right Problem Is the Partner's Problem

In forward-deployed work, you're not solving problems for yourself. You're solving problems that the partner will live with long after you're gone. The right problem has to be something they care about, something they're motivated to own, something that connects to their goals—not just yours.

This is where it gets tricky. Sometimes you see a problem that's technically critical but the partner doesn't feel its urgency. Other times the partner is focused on something that feels less important to you. Finding the right problem means navigating that gap.

## The Narrowing Process

So how do you actually narrow from "everything that could be done" to "the one thing that should be done"? Here's what's worked for me.

### Start by Listening Broadly

Before you can narrow, you need to understand the full landscape. Don't jump to conclusions in the first week. Ask questions. Shadow the team. Understand not just the technical challenges but the organizational ones. What's keeping people up at night? What have they tried before? What do they wish was different?

The goal isn't to solve anything yet. It's to map the territory.

### Identify the Constraints

Every engagement has constraints that shape what's possible. Time is the obvious one—how long do you have? But there are others:

- **Partner capacity.** How much bandwidth does the partner team have to work alongside you? To learn? To take ownership?
- **Technical constraints.** What can't be changed? What systems are off-limits? What dependencies exist?
- **Organizational constraints.** Who needs to approve changes? What processes must be followed? What's the appetite for risk?
- **Stakeholder alignment.** What do the decision-makers actually care about? What would success look like from their perspective?

Constraints aren't obstacles to work around. They're inputs that shape the problem you choose. A problem that ignores constraints isn't the right problem—it's a fantasy.

### Ask "Why" Repeatedly

When a partner says "we need X," ask why. Then ask why again. The stated problem is often a symptom. The right problem is usually a few layers deeper.

"We need better monitoring" might become "we can't debug production issues fast enough" which might become "we don't understand why the nightly job fails intermittently" which might become "there's a race condition in the data sync process."

The deeper you go, the more specific the problem becomes. Specificity is your friend.

### Force Prioritization

At some point, you have to make a call. You can't narrow indefinitely. Here's a forcing function that helps:

If you could only solve one problem in this engagement—one—what would it be?

This question is uncomfortable. People resist it. "We need to solve A and B and C." But the resistance is informative. Push through it. What's the one thing?

Once you have an answer, pressure-test it. Why this one? What happens if you don't solve it? What does solving it enable? Is the partner aligned?

### Validate with the Partner

You don't get to decide the right problem unilaterally. The partner has to agree. And not just agree in a passive "sure, sounds good" way—they have to believe this is the most important thing.

This means having an explicit conversation: "Based on everything we've learned, we think the most important problem to focus on is X. Here's why. Does that match your understanding? Is there something more important we should consider?"

If there's misalignment, explore it. Maybe you're missing context. Maybe they're seeing something you're not. Or maybe you need to make the case for why your assessment is different from theirs.

The goal is genuine alignment, not just sign-off. If the partner doesn't believe in the problem you've chosen, the engagement is already in trouble.

## Why Narrowing Is Hard

If narrowing scope is so valuable, why doesn't everyone do it? Because it's genuinely uncomfortable.

### It Feels Like You're Leaving Value on the Table

When you see ten problems and choose to focus on one, you're explicitly deciding not to solve nine others. That feels wasteful. The partner came to you with needs, and you're saying "we're not going to address most of them."

This discomfort is real, but it's misleading. Trying to solve ten problems and solving none of them well leaves more value on the table than solving one problem deeply.

### It Requires Saying No

Narrowing means saying no—to the partner, to stakeholders, sometimes to your own team. No is hard. No creates friction. No requires you to justify your reasoning and hold your ground.

But no is what makes focus possible. Every yes to something is an implicit no to something else. Better to make the no explicit and intentional.

### It Demands Confidence in Uncertainty

Early in an engagement, you don't have perfect information. You're making bets. Choosing the right problem means committing to a direction when you're not 100% certain it's correct.

This is uncomfortable. What if you're wrong? What if you miss something? But waiting for certainty means waiting forever. At some point, you have to decide.

### The Partner May Not Want to Narrow

Sometimes the partner resists narrowing. They want everything. They're paying for help, and they want help with all of it.

This is where your role shifts from executor to advisor. You're not just there to build what they ask for. You're there to help them understand what's actually achievable and what will create the most value. Sometimes that means pushing back.

## Signs You've Found the Right Problem

How do you know when you've narrowed enough? When you've landed on the right problem? Here are some indicators:

**You can state the problem crisply.** If you can explain it in one or two sentences, and someone new to the engagement could understand it, you're probably in the right territory.

**The partner is energized about solving it.** Not just agreeing—genuinely excited. This is the problem they want solved. When you talk about progress, they lean in.

**Success is measurable.** You know what "done" looks like. You can point to specific outcomes that would indicate the problem is solved.

**It's achievable in the time available.** Not theoretically achievable—actually achievable given the constraints, the team, the dependencies.

**Solving it creates momentum.** The problem isn't isolated. Solving it unblocks other things, builds confidence, demonstrates value.

**You've said no to other things.** If you haven't explicitly decided not to work on other problems, you probably haven't narrowed enough. Narrowing requires sacrifice.

## Signs You Haven't Narrowed Enough

On the flip side, here are warning signs that your scope is still too broad:

**The problem statement is fuzzy.** "Improve the system" or "make things faster" isn't a problem—it's a direction. If you can't get specific, you haven't narrowed.

**You can't explain what's out of scope.** If everything is in scope, nothing is. The right problem has clear boundaries.

**Timelines feel impossible.** If every estimate is "we'll see" or "it depends," the scope is probably too broad to reason about.

**The partner team seems overwhelmed.** If they can't keep up with what you're doing, you're likely doing too much.

**You're making progress on multiple fronts but finishing nothing.** Lots of activity, little completion. That's a scope problem.

## Narrowing Throughout the Engagement

Finding the right problem isn't a one-time exercise. It happens at the beginning of the engagement, but it also happens throughout.

As you learn more, you'll refine your understanding of the problem. What seemed critical might turn out to be less important. What seemed like a detail might reveal itself as the core issue.

Be willing to re-narrow. If you realize midway through that you've got the wrong problem, or that the scope is still too broad, adjust. It's better to course-correct than to keep building the wrong thing.

The goal isn't to get it perfect on day one. The goal is to be intentional about scope, to keep asking "is this the most important thing?" and to have the courage to change course when the answer is no.

## Conclusion

In forward-deployed engineering, finding the right problem is perhaps the most important thing you do. Everything else—the code, the architecture, the documentation, the knowledge transfer—flows from that choice.

Finding the right problem means narrowing. It means resisting the urge to solve everything and instead asking: what is the most important thing to solve right now, given the time we have, the constraints we face, and the partner we're serving?

Narrowing is uncomfortable. It requires saying no. It requires confidence in uncertainty. It requires conversations with partners who might want more than you can deliver.

But the alternative—broad scope, diluted effort, diffuse impact—is worse. Engagements that try to solve everything often solve nothing well. Engagements that find the right problem and solve it deeply create lasting value.

The right problem is narrow. It's high-impact. It's solvable. It's the partner's problem, not just yours.

Find that problem. Then solve it like it's the only thing that matters.

Because in a time-bounded engagement, it might be.
