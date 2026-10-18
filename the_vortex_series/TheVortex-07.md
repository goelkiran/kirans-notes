# If the coder and the tester share the same brain, who finds the blind spots?

*Kiran's Notes — The Vortex, Article 7 of 12*

---

I want to return to the question that started this whole series.

A quality engineer on my team — experienced, sharp, the kind of person who thinks in failure modes as naturally as most people think in features — leaned back in a retrospective and asked it almost casually:

*"If the developer used an AI assistant to write the code, and I'm using the same AI to generate test cases — are we actually testing anything, or are we just validating each other's assumptions?"*

Six months later, I still do not have a clean answer. But I have been thinking about it carefully enough that I can at least frame the question properly.

It is the same signal I mentioned in the first article. Something has shifted — and our practices have not caught up yet.

---

## What testing was actually for

Before we ask whether our current testing practices still make sense, we need to ask what they were designed to do. Because testing, like microservices and agile, was not invented in a vacuum. It was invented in response to specific failure patterns.

Human developers make specific kinds of mistakes. We misremember requirements. We make off-by-one errors. We forget edge cases that were not in the story. We introduce regressions when we touch code we do not fully understand. We get tired at 5pm on a Friday and make a decision we should not.

Test-Driven Development was designed around these failure patterns. Write the test first, so you cannot forget what the requirement was. Red-green-refactor, so you always have a safety net. Behaviour-Driven Development added a layer of shared language between developers and testers, because ambiguity in requirements was itself a major failure source.

These are all, at their core, compensations for human cognitive limitations. The test suite is not just a technical artefact. It is a record of every way a human mind has been found to fail at this particular problem.

---

## What changes when the coder is an agent

Agentic AI does not make the same kinds of mistakes humans make. It makes different ones.

It does not get tired. It does not misremember requirements it was given in the same context window. It does not make off-by-one errors in the way a human does. It is remarkably consistent at generating code that does what it was asked to do.

But it has its own failure modes.

It can be confidently wrong about something it was never trained to be uncertain about. It can optimise for the stated requirement while missing an unstated one that any experienced engineer would have noticed. It can generate code that passes all the tests and still has a subtle logical flaw that emerges only under a specific combination of conditions that nobody thought to test for.

These are not the same failure patterns that TDD was designed to catch.

And if you are using the same AI to generate both the code and the test cases, you are creating a system that validates its own assumptions — which is not testing. It is confirmation.

---

## The plan mode observation

There is something else I have noticed that connects to this.

When I work with agentic AI tools in plan mode — laying out a complex problem, breaking it into steps, defining dependencies before any code is written — it feels structured in a way that is deeply familiar.

Specification first. Sequence defined upfront. Execution follows the plan.

It feels like waterfall.

I do not think this is a bad thing. The instinct behind waterfall — that you should understand what you are building before you build it — was always correct. The problem was rigidity, and the human coordination cost of long sequential cycles.

Agentic AI changes those constraints. The plan can be revised quickly. Execution is more consistent. The cost of iteration drops.

Which raises a quiet question: are we rediscovering the value of upfront design — without the limitations that made it brittle the first time?

---

## What testing needs to become

I do not think testing gets smaller in this world. I think it gets sharper.

A few principles I am working through:

Test with a different model than the one that coded. Different training, different blind spots, different failure modes. Not perfect — but meaningfully better than testing with the same model.

Shift emphasis from functional testing to property testing. Not just “does this work for these inputs?” but “does this behave correctly across the space of possible inputs?”

Keep humans in the loop for intent, not mechanics. The most important question is not “did the code do what I asked?” but “did I ask for the right thing?”

That is still a human judgement.

---

## An open question worth sitting with

BDD forced us to define behaviour clearly before writing code.

But when both the developer and the tester are AI systems, who defines the behaviour?

Who writes the “given, when, then”?

That responsibility has not gone away.

It may be the most important one we have left.

*Next: We never needed to track which species wrote the code — until now.*

---

*Kiran's Notes is a LinkedIn newsletter on data engineering, architecture, and the future of software craft. Subscribe to follow The Vortex series.*

---
*#SoftwareTesting #AgenticAI #TDD #BDD #QualityEngineering #KiransNotes #TheVortex*