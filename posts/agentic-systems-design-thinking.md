---
title: "Design Thinking and Agentic Systems: Why User Engagement Matters"
slug: design-thinking-agentic-systems
author: 
status: draft
created_date: 2026-01-30
published_date: 
last_updated: 2026-01-30
tags:
  - agentic-ai
  - llm
  - design-thinking
  - user-research
categories:
  - ai-ml
  - internal
summary: "Why design thinking and early user engagement are critical for building successful agentic AI systems."
audience: internal
---

# Design Thinking and Agentic Systems: Why User Engagement Matters

## The Core Insight

After working on LLM-based solutions for enterprise customers, one lesson stands out: **the technical challenges we face are often symptoms of not engaging users in a tight enough loop**.

Problems that seem purely technical—data issues, reliability concerns, evaluation difficulties—can often be anticipated or avoided through rigorous design thinking.

> **Note:** This describes an ideal state. Real projects have compressed timelines and busy stakeholders. But understanding the ideal helps us make better trade-offs.

## Why Design Thinking Matters for Agentic Systems

Design thinking is human-centered problem-solving: understand users, define the problem, ideate, prototype, and test. What makes it different from waterfall is the *scale and frequency* of iteration. The tighter the loop with users, the faster you learn.

**The projects that struggle most are those where the technical team builds in isolation**, only to discover late that the system doesn't fit workflows or that users don't trust the outputs.

### It Also Forces You to Get Organized

There's a secondary benefit that's easy to overlook: design thinking imposes structure on your own thinking.

When you have to articulate a problem clearly enough to discuss it with users, you can't hide behind vague intentions. When you have to explain what your prototype does, you discover the gaps in your own understanding. When you have to define success criteria collaboratively, you're forced to prioritize.

On the T-Mobile project, we found ourselves questioning the solution throughout the engagement as more context emerged. We kept learning things mid-project that could have been established earlier with better upfront problem definition. For example, we eventually discovered that the true problem was getting both *dimensions* and *count* right—not just count alone. Accurate counts were still valuable, but they only told part of the story without correct dimensions. That's a fundamental insight about the problem structure, and we learned it late. A more rigorous design thinking process would have surfaced this priority earlier, saving us from optimizing the wrong thing.

This organization pays dividends beyond user engagement. It makes your team more aligned, your stakeholder updates more coherent, and your technical decisions more defensible. The discipline of explaining your work to users makes you better at explaining it to everyone else too.

## Key Challenges (And How User Engagement Helps)

### The Data Problem

Many data problems are actually *user understanding* problems in disguise.

- **Insufficient data:** Users know where documentation gaps exist and where tribal knowledge lives
- **Data drift:** Users can tell you about seasonal patterns and upcoming business changes. Understanding and communicating about data distributions is critical. On the T-Mobile project, we knew we were focusing on tower antennas as the first iteration—both the customer and our team were aligned and felt confident in this scope. But clear, ongoing communication is essential to ensure you're not solving only part of the problem when the customer might have grander expectations. Alignment on the *current* scope doesn't mean alignment on the *full* vision.
- **Distribution mismatch:** Watching real users reveals gaps your test set missed. On the T-Mobile project, we were told throughout that we were on track to solve the right problem. But when we delivered, the customer mentioned that the large text output might need to be rethought for how they'd actually use it. The expectations we'd been building toward weren't fully grounded in the reality of day-to-day usage. Observing real users earlier would have surfaced this disconnect sooner.

### System Complexity

Agentic systems involve multi-step reasoning, tool usage, and state management.

- **State management:** Users can tell you how long tasks take, where breakpoints exist, what context they expect the system to remember
- **Tool selection:** Users know which integrations are essential vs. nice-to-have
- **Error propagation:** Users can identify which steps need precision vs. which tolerate approximation

### The Demo Problem

This deserves special attention: **LLM systems demo incredibly well**.

A curated demo with practiced questions in a controlled environment creates unrealistic expectations. The gap between demo and production destroys trust.

We saw this firsthand on the T-Mobile project. We jumped straight into solutioning and showed them a beautiful demo—polished interface, impressive responses, the whole package. The problem? That demo validated their existing assumptions rather than challenging them. Instead of taking a step back to critically examine whether their proposed approach was even the right one, we gave them a shiny artifact that confirmed what they already wanted to believe.

This is the hidden danger with agentic and LLM solutions: **the demo can look beautiful while masking fundamental problems with the underlying approach**. A well-crafted demo creates a false sense of progress. It short-circuits the critical thinking needed to ask: "Is what we're building actually the right thing?"

When you involve real users early—watching them interact with prototypes, hearing actual questions, seeing confusion—you discover the gap *before* stakeholders set expectations.

### Evaluation

If your evaluation data doesn't match what users actually throw at the system, your metrics are meaningless.

- Build evaluation datasets from real user queries, not technical team assumptions
- Define "reliable enough" *with* users—requirements vary dramatically by use case
- Measure task completion and user trust, not just technical metrics

## Practical Takeaways

1. **Engage end users and domain experts early.** The people who will actually use the system day-to-day—not just the stakeholders who commissioned it—should be part of the conversation from the start. They understand the workflows, edge cases, and trust barriers that won't appear in any requirements document.

2. **Define success criteria collaboratively before building.** Work with the people who'll rely on the system to understand what "accurate enough" means for their context. What failure modes can they tolerate? What would make them stop trusting it?

3. **Test with realistic usage, not curated demos.** Real users may phrase questions differently than you'd expect, approach tasks from unexpected angles, and encounter scenarios your test set didn't anticipate. Observing actual usage reveals these gaps.

4. **Build in feedback mechanisms.** Give people a way to flag when the system fails them—this creates a continuous stream of evaluation data and shows you're invested in getting it right.

5. **Be honest about constraints.** If you can only do one conversation with end users instead of ten, that's still better than zero. Partial engagement beats no engagement.

## Conclusion

Design thinking isn't a silver bullet. But it helps you discover data constraints before they become architectural problems, build for real user behavior, define success metrics that matter, and identify trust barriers early.

The best agentic systems aren't just technically excellent—they're built by teams who deeply understand the humans they're building for.
