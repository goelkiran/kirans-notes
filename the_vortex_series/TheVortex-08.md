# We never needed to track which species wrote the code — until now

*Kiran's Notes — The Vortex, Article 8 of 12*

---

Software versioning is one of the quieter achievements of the engineering profession.

The idea that every change to a codebase should be recorded — who made it, when, what it changed, why — seems obvious in retrospect. But it took decades of painful experience with unmaintainable systems before the industry converged on it as a standard practice.

We version libraries. We version APIs. We version database schemas. We tag releases. We maintain changelogs. We record the commit message that explains why a function was changed at 11pm on a Tuesday in 2019.

What we have never thought to record is which kind of mind wrote the code.

We did not need to.

---

## The assumption we never stated

All developers were, as far as the versioning system was concerned, functionally equivalent instances of the same species.

Homo sapiens. Roughly consistent cognitive architecture. Trained through roughly similar educational and professional processes.

The variance mattered at the individual level — a senior engineer’s commit carries different implicit assumptions than a junior engineer’s — but the species was constant. It did not need a version number.

That assumption is now breaking down.

This is another version of the signal I described at the start of the series — something fundamental has shifted, but our systems still assume it hasn’t.

---

## Models evolve faster than developers do

A human engineer’s capabilities change slowly. Training, experience, mentorship, deliberate practice over years — these produce meaningful growth, but on a timescale of years.

Foundation models evolve on a completely different curve.

The gap in reasoning quality, security awareness, edge-case handling, and architectural judgement between a model from eighteen months ago and one from today is not incremental. It is substantial. And often discontinuous.

This means a codebase partially authored by an agent running on a model from two years ago is a genuinely different artefact than one authored by an agent running on a current model.

The older sections may have blind spots the current model would not have. They may reflect assumptions about security, performance, or correctness that no longer hold.

And we have no way to represent this in our version control systems today.

---

## Why this matters for audit and accountability

In regulated industries — and I have spent my career in one — auditability is never abstract.

Regulators want to know:
- what the system does  
- how it was built  
- who is responsible  

Today, that answer is human.

A development team signed off. Named individuals were accountable. The audit trail connects decisions to people.

As agentic AI takes on more of the work, that answer becomes incomplete.

The named individual may have reviewed and approved — but did not write.

The model that generated the first draft of a critical function is not recorded anywhere.

That is not a theoretical gap. It is a practical one.

And it will not stay invisible for long.

---

## What model provenance could look like

I am not proposing a finished standard. But the shape of one is not hard to imagine.

At minimum, development tooling should record:
- which model assisted  
- which version  
- when it was used  

Not as a replacement for human accountability — the human still owns the decision — but as additional context.

This has practical value beyond compliance.

If a vulnerability traces back to a specific model behaviour, you can identify where that model influenced your codebase.

If a model is later found to have systematic blind spots, you know where to look first.

We already track library dependencies because they shape system behaviour.

The model that wrote the code is not so different.

---

## The species assumption, made visible

There is something quietly profound about this moment.

When we built version control systems, we embedded an assumption so deep we never stated it: the entity making changes is always human.

That assumption was invisible because it was always true.

Now it is visible precisely because it is no longer fully true.

The minds participating in software development are no longer uniform. They vary in architecture, training, capability, and limitation — and they evolve faster than any human team.

Recording that variation is not bureaucracy.

It is the minimum required to maintain accountability in a system that is no longer built by a single kind of mind.

*Next: Speed without sight — why regulatable AI is not a feature, it's a requirement.*

---

*Kiran's Notes is a LinkedIn newsletter on data engineering, architecture, and the future of software craft. Subscribe to follow The Vortex series.*

---
*#SoftwareVersioning #AIGovernance #Compliance #DataEngineering #AuditTrail #KiransNotes #TheVortex*