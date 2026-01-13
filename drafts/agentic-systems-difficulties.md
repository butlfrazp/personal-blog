---
title: "Design Thinking and the Difficulties of Building Agentic Systems"
slug: design-thinking-agentic-systems-difficulties
author: 
status: draft
created_date: 2026-01-13
published_date: 
last_updated: 2026-01-13
tags:
  - agentic-ai
  - llm
  - ai-agents
  - design-thinking
  - user-research
categories:
  - ai-ml
  - systems-design
summary: "Why design thinking and early user engagement are critical for building successful agentic AI systems, and how they help prevent common pitfalls."
---

# Design Thinking and the Difficulties of Building Agentic Systems

## Introduction

Over the past few years, I've had the opportunity to work at Microsoft building LLM-based software solutions for enterprise customers. These projects have spanned a wide range of applications, from conversational chatbots and intelligent assistants to sophisticated agentic systems designed for tasks like anomaly detection, workflow automation, and complex decision support.

Through this work, one lesson has emerged more clearly than any other: **the technical challenges we face are often symptoms of not engaging users early enough**. Time and again, problems that seemed purely technical (data issues, reliability concerns, evaluation difficulties) could have been anticipated or avoided entirely through rigorous design thinking at the project's outset.

This post argues that design thinking isn't just a nice process to follow. It's a critical risk mitigation strategy. I'll walk through common challenges in building agentic systems and show how early user engagement helps address each one.

> **A note on idealism:** What I'm describing here is an ideal state. In reality, timelines are compressed, stakeholders are busy, and perfect user engagement isn't always possible. But I believe it's important to have these conversations and strive toward this ideal, even when we fall short. Understanding what *should* happen helps us make better trade-offs when constraints force compromises.

## The Importance of Design Thinking

Before diving into technical challenges, it's critical to address something that often determines success or failure before a single line of code is written: **involving the right people from the start**.

### What is Design Thinking?

Design thinking is a human-centered approach to problem-solving that prioritizes understanding the needs, behaviors, and pain points of the people who will actually use the system. It typically involves five phases:

1. **Empathize**: Deeply understand your users through observation and engagement
2. **Define**: Clearly articulate the problem you're solving based on user insights
3. **Ideate**: Generate a wide range of potential solutions
4. **Prototype**: Build quick, low-fidelity versions to test ideas
5. **Test**: Gather feedback and iterate

### Why It Matters for Agentic Systems

In my experience, the projects that struggle most are those where the technical team builds in isolation, only to discover late in the process that the system doesn't fit the actual workflow or that users don't trust its outputs.

**The people who will use the system must be involved from day one.** This isn't just a nice-to-have. It's essential. End users understand the nuances of their domain, the edge cases that will break your carefully designed prompts, and the trust barriers that will prevent adoption.

Design thinking workshops at the outset of a project help ensure that:

- You're solving the right problem (not the problem you assumed existed)
- The system fits naturally into existing workflows
- Users feel ownership and trust in the solution
- Edge cases and failure modes are identified early

When design thinking is front and center, you build systems that people actually want to use.

## Key Challenges (And How Design Thinking Helps)

### Challenge 1: The Data Problem

One of the most consistent challenges across projects is **the lack of sufficient, high-quality data**. This manifests in several ways that can derail even well-architected systems. But here's the thing: many data problems are actually *user understanding* problems in disguise.

#### Insufficient Data for Pattern Recognition and Information Extraction

Many organizations come to the table with grand ambitions for what their agentic system will accomplish, but when we dig into the available data, we find gaps. In our work, we're typically not fine-tuning models. Instead, we're building systems that perform information lookup and extraction, which relies heavily on recognizing patterns in the data. Without sufficient examples of those patterns, the system can't learn what to look for.

This scarcity makes it difficult to:
- Establish reliable baselines for system performance
- Build robust evaluation datasets
- Define the patterns the system needs to recognize
- Validate that information extraction is working correctly

**How design thinking helps:** When you engage users early in the Empathize phase, you discover what data actually exists versus what stakeholders *think* exists. Users on the ground know where the documentation gaps are, which processes are tracked and which aren't, and where the tribal knowledge lives. This surfaces data constraints before you've committed to an architecture that depends on data you don't have.

#### Data Drift

Even when initial data is adequate, **data drift** presents an ongoing challenge. The data distribution the system encounters in production often differs from what was available during development. This can happen because:

- The business environment evolves (new products, changing customer behavior)
- Seasonal patterns weren't captured in the training data
- The system's own existence changes user behavior

In our experience, that last point is the most common culprit. Once a system is live, users adapt to it. They change how they phrase questions, what tasks they attempt, and how they interact with the underlying data. The system you built was trained on pre-system behavior, but now it's operating in a post-system world.

Data drift is particularly insidious in agentic systems because the effects compound. If an early step in an agent's reasoning chain is influenced by drifted data, errors propagate through subsequent steps.

**How design thinking helps:** By deeply understanding your users' workflows and environment during the Empathize phase, you can anticipate *how* and *why* data might change. Users can tell you about seasonal patterns, upcoming business changes, and historical shifts that won't appear in any dataset. They know that "Q4 is always different" or "we're launching a new product line next month." This proactive understanding lets you design for drift rather than react to it.

#### Distribution Mismatch

Closely related to drift is the problem of **distribution mismatch**, where the actual system's data distribution differs from what we expected during design. This often happens when:

- Development data came from a subset of users or use cases
- Test environments don't accurately reflect production load and variety
- Stakeholders had assumptions about data that didn't match reality

We've seen projects where the chatbot performed beautifully on test queries, only to struggle in production because real users asked questions in ways nobody anticipated.

**How design thinking helps:** This is perhaps where design thinking provides the most value. When you observe real users and understand the true distribution of their questions, tasks, and edge cases, you build systems that match reality, not assumptions.

Instead of technical teams guessing what questions users will ask, you *watch* them work. You *listen* to the actual language they use. You discover that the carefully curated test set of 50 questions represents maybe 30% of what real users actually ask. The other 70%? Those are the questions that would have broken your system on day one.

**Being proactive rather than reactive:** The alternative is shipping and then discovering the mismatch, which is far more expensive. You've built the wrong thing, users lose trust immediately, and now you're scrambling to fix a live system while managing stakeholder disappointment. Design thinking front-loads this discovery when changes are cheap.

### Challenge 2: System Complexity in Agentic Workflows

Agentic systems are fundamentally more complex than traditional software or even simpler LLM applications like chatbots. They involve multi-step reasoning, tool usage, state management across tasks, and graceful handling of failures at any point in the chain. This complexity creates challenges that compound quickly.

#### State Management Across Multi-Step Tasks

Unlike a simple question-answer interaction, agentic systems often work on tasks that span multiple steps and can take several minutes to complete. This raises difficult questions:

- **Context persistence:** What does the system need to remember between steps? Between sessions?
- **Checkpoint and recovery:** If something fails midway through a complex task, can the system recover without starting over?
- **Memory limitations:** LLMs have context windows. How do you manage information that exceeds those limits?

These aren't just technical problems. They're user experience problems. If a user works with an agent for 20 minutes on a complex task and then loses everything due to a timeout or error, that's a trust-destroying experience.

**How design thinking helps:** By understanding user workflows, you learn how long tasks actually take, where natural breakpoints exist, and what context users expect the system to remember. Users can tell you "I need to pause this for a meeting and come back" or "I expect it to remember what I said yesterday." This shapes your state management architecture around real needs rather than technical assumptions.

#### Tool Selection and Orchestration

Agentic systems often need to choose which tools to use, in what order, and how to handle failures when tools don't behave as expected. Getting this wrong leads to:

- **Wrong tool selection:** The agent picks the wrong tool for the task, producing useless or incorrect results
- **Cascading failures:** One tool fails, but the agent proceeds anyway, compounding the error
- **Security and access issues:** The agent tries to use tools the user doesn't have access to, or performs actions with unintended consequences

**How design thinking helps:** Users know which tools they actually use day-to-day, which integrations are essential versus nice-to-have, and where security concerns will block adoption entirely. They can help you prioritize: "I need this to work with our CRM. Everything else is optional." They can also identify failure modes: "If the database lookup fails, I'd rather get nothing than a guess."

#### Error Propagation in Multi-Step Tasks

In agentic systems, errors compound. If the first step of a five-step process produces slightly wrong output, each subsequent step may amplify that error. By the end, you've confidently produced something completely wrong.

This is where the non-deterministic nature of LLMs becomes particularly dangerous. Traditional software fails loudly with an exception or an error code. LLMs fail quietly, producing plausible-sounding outputs that are subtly incorrect.

**How design thinking helps:** Users can help identify which steps are most critical for accuracy, where human checkpoints might be valuable, and what "close enough" means at each stage. Some tasks can tolerate approximation; others need precision. Only users can tell you which is which.

### Challenge 3: Evaluation and Testing

Evaluation is where everything comes together, or falls apart. You can build the most sophisticated agentic system in the world, but if you can't measure whether it's actually working, you're flying blind.

#### Why Evaluation Matters

Without robust evaluation, you face several risks:

- **No baseline for improvement:** How do you know if changes make things better or worse?
- **False confidence:** The system might appear to work in demos but fail on real tasks
- **Stakeholder misalignment:** Different people have different definitions of "success"
- **Regression blindness:** You can't catch when updates break existing functionality

In agentic systems, evaluation is especially challenging because outputs are often non-deterministic. The same input might produce different but equally valid outputs. Traditional software testing (expected input leads to expected output) doesn't translate directly.

#### Defining "Reliable Enough"

One of the hardest questions in agentic systems is: **what does "reliable" even mean?**

Traditional software has clear reliability expectations. An API either returns the right response or it doesn't. A function either produces the correct output or it throws an error. You can measure uptime, error rates, and latency with precision.

LLM-based systems don't work this way. The same input can produce different outputs. "Correct" is often subjective. The system might be 95% accurate, but the 5% failures could be catastrophic or trivial depending on context.

This is why reliability must be defined *with users*, not by the technical team alone:

- **A creative writing assistant can tolerate high variability.** Different suggestions each time might even be a feature.
- **An anomaly detection system needs consistency.** If it flags different things on the same data, users lose trust.
- **A customer service bot might need to be right 99% of the time** because the 1% failure goes to an angry customer.
- **An internal research tool might be fine at 80%.** Users can verify and it still saves time.

Only users can tell you where on this spectrum your system needs to be. Only users can define what failure modes are acceptable ("wrong answer is okay if it admits uncertainty") versus unacceptable ("confidently wrong is a dealbreaker").

**How design thinking helps:** During the Define phase, work with users to establish reliability requirements *before* you build. Ask: "How often can this be wrong before you stop trusting it?" and "What kind of wrong is worse: missing something or flagging something incorrectly?" These conversations shape your architecture and your evaluation criteria.

#### The Demo Problem: Why False Confidence is So Dangerous

Let me expand on false confidence, because this is one of the most insidious problems in generative AI projects: **these systems demo incredibly well**.

Put an LLM-powered system in front of stakeholders, ask it a few well-crafted questions, and watch the room light up. The responses are fluent, confident, and often genuinely impressive. Executives leave the demo excited. Budgets get approved. Timelines get set. Everyone believes they've seen the future.

But here's what the demo didn't show:

**The demo was curated.** The person running the demo knows which questions produce good outputs. They've practiced. They phrase things in ways that work. They avoid the queries that cause the system to stumble, hallucinate, or return nonsense.

**The demo environment is controlled.** The data is clean. The context is well-defined. The use case is narrow. None of the messy reality of production is present: no ambiguous inputs, no malformed data, no users who interact with the system in unexpected ways.

**The "wow factor" masks fragility.** When an LLM produces a beautifully written response, it *feels* like intelligence. It's easy to assume that this fluency extends to correctness and reliability. But fluency and accuracy are not the same thing. The system can confidently produce wrong answers that sound completely plausible.

**Demos show the best case, not the distribution.** Even if the demo queries are legitimate, they represent a tiny fraction of what users will actually ask. Real usage follows a long-tail distribution. The most common queries might work fine, but users will inevitably venture into the 70% of queries the system has never seen.

**The gap between demo and production destroys trust.** This is the real cost. When stakeholders have seen the impressive demo and then the production system fails on basic tasks, you don't just have a technical problem. You have a credibility problem. Users lose trust quickly. Stakeholders question the investment. The project gets labeled as "overpromised and underdelivered."

I've seen this pattern repeatedly: a dazzling demo creates unrealistic expectations, the team rushes to ship, and then months are spent managing disappointment and rebuilding trust that shouldn't have been lost in the first place.

**How design thinking helps:** When you involve real users early, watching them interact with prototypes, hearing their actual questions, seeing where they get confused, you discover the gap between demo and reality *before* stakeholders set expectations. Design thinking forces you to test with the messy, uncontrolled reality of actual usage. It replaces the curated demo with genuine user feedback.

The goal isn't to never demo. Demos are valuable for building excitement and alignment. The goal is to pair demos with honest evaluation data, to set realistic expectations, and to let user research ground the project in reality rather than letting a polished demo write checks the system can't cash.

#### Evaluation Data Must Match User Expectations

Here's where many projects go wrong: they build evaluation datasets based on what the *technical team* thinks users will do, not what users *actually* do. The result is a system that scores well on benchmarks but disappoints in production.

Your evaluation data should reflect:

- **The real distribution of user queries and tasks**, not just the happy path
- **Edge cases that users encounter**: the weird questions, the typos, the ambiguous requests
- **The language users actually use**, which is often different from how technical teams phrase things
- **The volume and variety of production traffic**, not just a curated set of 50 test cases

If your evaluation data doesn't match what users will actually throw at the system, your metrics are meaningless.

#### Metrics Should Reflect What Matters to Users

Technical metrics are easy to measure but often miss the point. Latency, token count, and API costs matter for operations, but they don't answer the fundamental question: **did this help the user accomplish their goal?**

User-centered evaluation focuses on:

- **Task completion:** Did the system help the user finish what they were trying to do?
- **Accuracy of information:** Was the extracted or retrieved information correct?
- **Trust and confidence:** Does the user believe the system's outputs?
- **Time saved:** Is this actually faster than the manual process?
- **Error impact:** When the system fails, how bad is it? Can users recover?

These metrics require user input to define. What counts as "accurate enough" varies by context. A system that's 90% accurate might be transformative for one use case and unacceptable for another.

#### How Design Thinking Fits In

Design thinking directly informs evaluation at every phase:

**Empathize:** By observing users, you understand what they're actually trying to accomplish and what frustrates them about current processes. This tells you what to measure.

**Define:** When you clearly articulate the problem, you naturally define success criteria. "Help users find relevant documents faster" implies metrics around search relevance and time-to-answer.

**Prototype & Test:** Early prototypes tested with real users generate organic evaluation data. The questions users ask, the ways they misuse the system, the feedback they provide: all of this becomes your evaluation dataset.

The design thinking loop (build, test, learn, iterate) is essentially a continuous evaluation process. Users aren't just validators at the end; they're co-creators of the evaluation framework itself.

#### Being Proactive About Evaluation

The reactive approach is to ship first and figure out metrics later when stakeholders start asking hard questions. The proactive approach, informed by design thinking, is to define success criteria with users *before* building, then design the system to be measurable from day one.

This means:

- Building in logging and observability that captures what users actually do
- Creating feedback mechanisms so users can flag when the system fails them
- Establishing baseline metrics from user research before launch
- Planning for ongoing evaluation, not just launch-day testing

When evaluation is an afterthought, you end up measuring what's easy instead of what matters. When it's baked into the design thinking process from the start, you measure what users actually care about.

## The Ideal vs. Reality

I want to be honest: what I've described is an ideal state. In practice, there are real constraints:

- **Time pressure:** Projects have deadlines, and thorough design thinking takes time
- **User availability:** The people you need to talk to are often the busiest
- **Organizational dynamics:** Sometimes decisions are made above you before user research happens
- **Budget constraints:** Proper user research requires investment

I don't have perfect solutions for these constraints. But I believe strongly that understanding the ideal helps us make better trade-offs. If you can only do one user interview instead of ten, that's still better than zero. If you can only observe users for a day instead of a week, you'll still learn things that surprise you.

The goal isn't perfection. It's shifting from a purely reactive posture ("users are complaining, let's fix it") to a more proactive one ("let's understand users before we build").

## Conclusion

The difficulties of building agentic systems are real and significant. Data problems, reliability concerns, state management, tool orchestration, and evaluation challenges will all demand your attention.

But many of these technical challenges are downstream of a more fundamental issue: **we often don't understand our users well enough before we start building**.

Design thinking isn't a silver bullet. It won't eliminate data drift or make LLMs deterministic. But it will help you:

- Discover data constraints before they become architectural problems
- Anticipate how distributions will shift over time
- Build for real user behavior, not assumed behavior
- Define success metrics that actually matter to users
- Identify trust barriers and failure modes early

Is this idealistic? Yes. Will every project have the luxury of thorough user research? No. But having these conversations, pushing for more user engagement, advocating for design thinking workshops, insisting that end users have a seat at the table, moves us in the right direction.

The best agentic systems I've seen weren't just technically excellent. They were built by teams who deeply understood the humans they were building for.
