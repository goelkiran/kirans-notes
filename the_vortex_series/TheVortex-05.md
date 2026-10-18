# It only looks like a pendulum swinging back — it isn't

*Kiran's Notes — The Vortex, Article 5 of 12*

**Published in**: *Kiran's Notes* (LinkedIn Newsletter)  
**Original URL**: [LinkedIn Pulse](https://www.linkedin.com/pulse/only-looks-like-pendulum-swinging-back-isnt-kiran-kumar-njuuc/)  
**Companion Graphic**: [TheVortex-05.jpeg](../assets/TheVortex-05.jpeg)  
**Author**: Kiran Kumar ([@goelkiran](https://github.com/goelkiran) / [LinkedIn](https://www.linkedin.com/in/kirangoel))  

---

Something interesting has been happening in the technology industry over the last few years, and it is being misread.

Amazon Prime Video's team published a blog post in 2023 describing how they moved a distributed microservices architecture back into a monolith — and cut their infrastructure costs by 90%. DHH and the Basecamp team have been arguing for years that the Rails monolith never needed to be broken apart. Teams across the industry are quietly consolidating services that were split more out of organisational habit than genuine technical necessity.

Simultaneously, there is a creeping return of structured upfront thinking in software delivery. More design before build. More explicit specifications. In plan mode with agentic AI tools, I often feel — and I will come back to this — like I am doing waterfall all over again.

The easy interpretation of all this is that the pendulum is swinging back. Monoliths returning. Waterfall returning. The microservices and agile era winding down, with the industry retreating to familiar ground.

I think this interpretation is wrong. And the distinction matters.

---

## What a pendulum actually does

A pendulum returns to where it started. The same position, the same height, the same potential energy. If the pendulum is swinging back to monoliths, it means the monolith of 2025 is the same thing as the monolith of 2000, and the only thing that changed was fashion.

That is not what is happening.

The Amazon Prime Video monolith is not the same as a 2000-era monolith. It runs on cloud infrastructure that didn't exist then. It is deployed via CI/CD pipelines that automate what used to require weeks of manual coordination. It is monitored with observability tools that give engineers real-time insight into its behaviour that was simply impossible before. The team that owns it is structured and skilled in ways that reflect twenty years of hard-won understanding about software engineering.

It looks like a monolith. It shares the name. But the ground it sits on is entirely different.

When DHH argues for the Rails monolith, he is not arguing for the monolith of 1999. He is arguing for a specific, considered architectural choice made in 2024 — with full awareness of the alternatives, full access to modern tooling, and a deliberate judgement that the coordination overhead of microservices costs more than it returns for his team size and use case.

That is not a pendulum swinging back. That is a mature industry making more nuanced choices.

---

## The ground has shifted

Here is what I think is actually happening.

Microservices solved a specific problem: how to let large numbers of human engineers work on the same system without constantly breaking each other's work. The decomposition into small services was the answer to a human coordination challenge. Every team gets their bounded context, their independent deployments, their clear interface contracts.

But the assumption underneath all of that — that the bottleneck in software development is human cognitive coordination — is now being challenged by a new participant. Agentic AI can hold the context of an entire large codebase in ways no human can. It does not need the system to be decomposed into microservices to understand what each part does. It does not need service boundaries to be explicit contracts, because it can reason about implicit dependencies.

If the constraint that created microservices is being dissolved, then moving back toward larger systems is not nostalgia. It is a rational response to a changing set of constraints.

Similarly, the plan mode behaviour I observe in agentic AI tools — where the system lays out a comprehensive plan before executing — looks like waterfall. But it is waterfall without the human failures that made waterfall brittle. The plan is generated fast, revised constantly, and executed with a consistency that no human team could maintain over a six-month project.

---

## Why the distinction matters

I am not arguing that microservices are dead, or that agile is finished, or that everyone should immediately move back to monoliths. The right architecture depends on the team, the problem, and the moment.

What I am arguing is that the reason to choose any particular architecture should be based on the actual constraints you face — not on conventions inherited from a different era with different constraints.

If your team is fifty engineers across three time zones, microservices may still be exactly right for you. The human coordination problem is real and present.

But if agentic AI is meaningfully reducing the cognitive cost of working with large codebases — and early evidence suggests it is — then the architectural trade-offs shift. Not completely, not immediately, but directionally.

The pendulum metaphor is seductive because it is simple. Things go one way, then come back. Cycles repeat. But the vortex is not a pendulum. It is a system that evolves. And when a new character enters the system, the calculations change.

The industry is not retreating. It is recalibrating.

*Next: Why an AI doesn't need your architecture to be human-readable.*

---


---
*#SoftwareArchitecture #Microservices #AgileVsWaterfall #TechLeadership #DataEngineering #KiransNotes #TheVortex*
