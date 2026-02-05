# Reflecting on the T-Mobile Anomaly Detection Project: Learnings from a Successful Engagement

Hey team, wanted to share some observations from our recent customer work and get your thoughts.

The T-Mobile Anomaly Detection project was a success. We delivered what the customer wanted to see and helped them measure the feasibility of their vision. The forcing functions we put in place ensured they could see real value. That said, every successful engagement has learnings, and I've been reflecting on what we could refine for even greater impact next time. Curious if others have run into similar patterns.

## The Demo Dynamic

Early on, we showed T-Mobile a polished demo. Impressive interface, strong responses, the whole package. It worked: it built excitement and helped the customer see what was possible.

But here's a tension worth naming: **that demo also validated their existing assumptions rather than challenging them.** It confirmed what they wanted to believe, which is great for momentum but can shortcut the critical thinking about whether the approach is right.

This is a common dynamic with LLM/agentic work. The demo looks great, which builds confidence. The question is how to balance that momentum with space to question the underlying approach. Has anyone found a good way to navigate this?

## Learnings Along the Way

Throughout the engagement, we kept learning things that refined our understanding:

- **Dimensions mattered as much as count.** The customer needed both to demonstrate value, not just count alone. We initially focused on count, then adapted once we understood dimensions were equally critical.

- **Output format for real usage.** At delivery, the customer mentioned the large text output might need rethinking for day-to-day use. Valid feedback that we could potentially surface earlier with more structured problem definition upfront.

These aren't failures. They're the natural evolution of understanding a complex problem. The question is whether a more rigorous design thinking process (user interviews, journey mapping, structured problem definition) could surface some of these insights earlier.

## Why Agentic Systems Make This Harder

This matters for all projects, but agentic systems raise the stakes. These systems make autonomous decisions and chain multiple reasoning steps together. Small misunderstandings about user needs don't just create friction. They cascade through multi-step workflows in unexpected ways.

When the system is making decisions on behalf of users, we need to deeply understand what those users actually need. Building in isolation until the demo is a recipe for late-stage surprises.

## Some Practices That Might Help

Based on this experience, a few things I'm thinking about for future projects:

1. **Engage end users early**, not just the stakeholders who commissioned it. On T-Mobile, the customer positioned themselves as the SMEs, which made broader user engagement difficult to plan for.
2. **Define success criteria collaboratively** before building. What does "good enough" actually mean?
3. **Test with realistic usage**, not curated demos. We started with demos but eventually integrated real images.
4. **Build in feedback loops** so we're learning continuously, not just at delivery. Make sure to surface both the good and the bad, not just demo highlights.
5. **Tune evaluators with SMEs**. On T-Mobile LESA, iterating on LLM-as-a-judge with domain experts dramatically improved how well metrics reflected real quality

## Want to Hear From You

I'm sharing this to start a discussion, not prescribe answers. A few questions I'd love your input on:

- **What pitfalls have you observed** on LLM/agentic projects related to user engagement?
- **What mitigations have been useful?** Any specific design thinking tools or practices that worked well?
- **How do you balance** the pressure to show progress (demos) with the need to validate the right problem first?

If you've used specific frameworks like journey mapping, assumption testing, or structured user interviews, I'd love to hear what worked and what didn't.
