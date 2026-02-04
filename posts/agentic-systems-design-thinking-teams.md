# Reflecting on the T-Mobile Anomaly Detection Project: What Would You Have Done Differently?

Hey team, wanted to share some observations from our recent customer work and get your thoughts.

After wrapping up the T-Mobile Anomaly Detection project, I've been reflecting on what we could have done differently for greater customer impact. We delivered something, but I keep thinking about the moments where a more user-centric approach might have changed our trajectory earlier. Curious if others have run into similar patterns.

## The Demo Trap

Here's what happened: we jumped straight into solutioning and showed T-Mobile a beautiful demo. Polished interface, impressive responses, the whole package.

The problem? **That demo validated their existing assumptions rather than challenging them.** Instead of taking a step back to critically examine whether their proposed approach was even the right one, we gave them a shiny artifact that confirmed what they already wanted to believe.

This feels like a common trap with LLM/agentic work. The demo looks great, which creates false confidence. Has anyone else experienced this? What's worked to avoid it?

## Things We Learned Too Late

Throughout the engagement, we kept discovering things mid-project that could have been established earlier:

- **Dimensions mattered as much as count.** The customer needed both to demonstrate value, not just count alone. We optimized count first, only to realize dimensions were equally critical.

- **Output format for real usage.** We were told we were on track, but at delivery they mentioned the large text output might need rethinking for day-to-day use. That feedback could have come way earlier.

A more rigorous design thinking process (user interviews, journey mapping, even just more structured problem definition sessions) might have surfaced these earlier.

## Why Agentic Systems Make This Harder

This matters for all projects, but agentic systems raise the stakes. These systems make autonomous decisions and chain multiple reasoning steps together. Small misunderstandings about user needs don't just create friction. They cascade through multi-step workflows in unexpected ways.

When the system is making decisions on behalf of users, we need to deeply understand what those users actually need. Building in isolation until the demo is a recipe for late-stage surprises.

## Some Practices That Might Help

Based on this experience, a few things I'm thinking about for future projects:

1. **Engage end users early**, not just the stakeholders who commissioned it. On T-Mobile, the customer positioned themselves as the SMEs, which made broader user engagement difficult to plan for.
2. **Define success criteria collaboratively** before building. What does "good enough" actually mean?
3. **Test with realistic usage**, not curated demos. We started with demos but eventually integrated real images.
4. **Build in feedback loops** so we're learning continuously, not just at delivery. Make sure to surface both the good and the bad, not just demo highlights.
5. **Tune evaluators with SMEs**. On LESA, iterating on LLM-as-a-judge with domain experts dramatically improved how well metrics reflected real quality

## Want to Hear From You

I'm sharing this to start a discussion, not prescribe answers. A few questions I'd love your input on:

- **What pitfalls have you observed** on LLM/agentic projects related to user engagement?
- **What mitigations have been useful?** Any specific design thinking tools or practices that worked well?
- **How do you balance** the pressure to show progress (demos) with the need to validate the right problem first?

If you've used specific frameworks like journey mapping, assumption testing, or structured user interviews, I'd love to hear what worked and what didn't.
