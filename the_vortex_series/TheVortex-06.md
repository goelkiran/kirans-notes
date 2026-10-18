# Why an AI doesn't need your architecture to be human-readable

*Kiran's Notes — The Vortex, Article 6 of 12*

**Published in**: *Kiran's Notes* (LinkedIn Newsletter)  
**Original URL**: [LinkedIn Newsletter](https://www.linkedin.com/newsletters/kiran-s-notes-7449344281594585089/)  
**Companion Graphic**: [TheVortex-06.jpeg](../assets/TheVortex-06.jpeg)  
**Author**: Kiran Kumar ([@goelkiran](https://github.com/goelkiran) / [LinkedIn](https://www.linkedin.com/in/kirangoel))  

---

Every best practice in software engineering has a reason. The reason is almost always a human being.

We write readable code because the next person to touch it will be a human with limited time and context. We document APIs because the engineer on the consuming team is not the engineer who built the service, and we cannot expect them to read a thousand lines of source code to understand an interface. We standardise on shared languages and frameworks because a team of twelve cannot afford twelve different mental models. We enforce naming conventions because inconsistency is cognitively expensive when you are scanning code at speed, with a deadline, under pressure.

Every single one of these practices was invented as an accommodation to human cognition. They are not mathematical truths. They are organisational responses to the reality of how human minds work.

And agentic AI has none of these limitations.

---

## What human-readable actually means

I have led large engineering teams for long enough to know what "readable code" really means in practice. It means code that a mid-level engineer, unfamiliar with this particular module, can open, scan, and understand well enough to make a safe change within an hour. That is the practical standard. Not elegant. Not beautiful. Understandable, quickly, under pressure.

This is a remarkably low bar in absolute terms. But it is the right bar for human teams, because it is calibrated to human cognitive realities: limited working memory, limited context, limited time.

An agentic AI system operating on a codebase has none of these constraints in the same form. It can hold the entire codebase in its reasoning context. It can trace a variable across five hundred files without losing the thread. It can understand implicit dependencies that are never stated anywhere, because it can reason about the behaviour of the system as a whole.

It does not need your module to be small. It does not need your function names to be descriptive. It does not need your architecture to be layered in a way that maps to human organisational boundaries.

This is not a minor point. It is a fundamental shift in what software can be.

---

## The constraints we are about to lose

Consider what falls away when the primary reader of code is no longer human:

The preference for a single standardised language stack disappears. A human team standardises on Python or Java or Go partly because cognitive switching between languages is expensive. An agent can work across ten languages without friction, selecting the best tool for each specific job — a query language for data transformation, a systems language for performance-critical paths, a functional language for complex business logic — all in the same system, all understood without complaint.

The imperative to keep services small and bounded dissolves. We decomposed into microservices partly because no human can hold a large system in their head. An agent can. The system can be as large and complex as the problem demands, without the artificial boundaries we imposed to suit human cognitive limits.

The documentation requirement changes shape. We write documentation for humans who need context they don't have. Agents derive context from the code itself. This does not mean documentation becomes useless — it means its purpose changes, from explanation to intent. Why was this built, not what does it do.

---

## The case for interpretability — and why it is not the same thing

Here I want to be careful, because there is an important distinction that gets lost in conversations about AI and code.

Saying that agentic AI does not need human-readable architecture is not the same as saying humans do not need to understand what AI-assisted systems do.

In safety-critical domains — financial systems, healthcare, aviation — the requirement for interpretability and regulatability is non-negotiable. A signal controller that manages traffic at a live intersection cannot operate as a black box, regardless of how capable the underlying model is. Ault, Hanna and Sharon demonstrated this precisely in their 2020 paper for the International Conference on Autonomous Agents and Multiagent Systems: they showed that a regulatable control function — one with a monotonic, interpretable relationship between inputs and outputs — could perform competitively with a deep neural network, while remaining fully auditable by a human operator.

The lesson is not that AI systems should be unreadable. The lesson is that interpretability is a design choice, not a side effect of human limitations. We can build systems that are optimised for AI to operate and still legible enough for humans to govern.

That is a different and harder design challenge than what we face today. Today, we make systems readable because the operators are human. Tomorrow, we will need to make systems governable even when the operators are agents.

---

## What this means in practice

In my design reviews over the last year, I have started asking a different question. Not "will the next engineer understand this?" but "will a human be able to audit, govern, and take responsibility for what this system does?"

These are different questions. The first is about readability. The second is about accountability.

Readability is a property of code. Accountability is a property of systems and organisations. As agentic AI takes on more of the work of reading and writing code, readability becomes less important. Accountability does not diminish — if anything, it becomes more important, because the systems being built are capable of acting with greater autonomy.

The architecture of the future does not need to be readable. It needs to be governable.

That distinction is going to require us to rethink some fundamental assumptions about what good engineering looks like.

*Next: If the coder and the tester share the same brain, who finds the blind spots?*

---


*Reference: Ault, J., Hanna, J.P., & Sharon, G. (2020). Learning an Interpretable Traffic Signal Control Policy. Proceedings of the 19th International Conference on Autonomous Agents and Multiagent Systems (AAMAS 2020).*

---
*#AIEngineering #SoftwareArchitecture #InterpretableAI #DataGovernance #TechLeadership #KiransNotes #TheVortex*
