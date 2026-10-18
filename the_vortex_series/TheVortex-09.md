# Speed without sight — why regulatable AI is not a feature, it's a requirement

*Kiran's Notes — The Vortex, Article 9 of 12*

---

There is a version of the agentic AI story that goes like this:

AI systems are becoming capable enough that human oversight is becoming a bottleneck. The future belongs to systems that act faster than any human review process can follow. Governance is friction. Interpretability is a luxury. Speed is the advantage.

I understand the appeal of this story.

I have sat in enough budget conversations to know that “move faster” is always easier to sell than “move carefully.”

But I think this version of the story is wrong.

And not just philosophically. Practically.

---

## A concrete example from a different domain

In 2020, a research team at Texas A&M published a paper at the International Conference on Autonomous Agents and Multiagent Systems that I have been thinking about ever since.

They were working on traffic signal control at real intersections.

The obvious solution was a deep neural network. And it worked — dramatically reducing delays.

But there was a problem.

Transportation agencies require systems that are interpretable and regulatable. A black-box controller that occasionally makes inexplicable decisions is not deployable — no matter how good its average performance is.

So the researchers asked a different question:

Can you build a system that is both interpretable and competitive?

The answer was yes.

---

## What regulatable actually means

The term “interpretable AI” is used loosely enough to lose meaning.

What this work defined more precisely is *regulatable* behaviour.

A system where:
- the relationship between inputs and outputs is predictable  
- a human can understand why a decision was made  
- a human can adjust behaviour without retraining the system  

This is not about explaining a black box after the fact.

It is about designing a system that can be understood and governed from the start.

---

## The governance gap we are walking into

This is where I see the real risk.

Most organisations are adopting AI-assisted development faster than they are evolving their governance models.

The tools are real. The productivity gains are real. The pressure to adopt is real.

But the questions:
- who is accountable  
- how decisions are audited  
- what happens when the system is wrong  

are being deferred.

That gap is accumulating.

And when it is eventually addressed — by regulation, by failure, or by incident — it will be expensive to retrofit.

---

## Interpretability and performance are not enemies

The lesson from the traffic control example is not that interpretability is free.

Sometimes it costs something.

The lesson is that it is a design choice.

And one we have barely explored properly.

If we treat interpretability as a first-class requirement — like performance or scalability — we will design differently.

---

## The real constraint

This is where the vortex matters.

The same system that is accelerating capability is also increasing consequence.

The faster the system moves, the more important it becomes to understand it.

Speed without sight is not an advantage.

It is a liability.

---

## A question worth asking now

Not:
> “Can we use AI for this?”

But:
> “Can we use AI for this in a way we can stand behind?”

That is the difference between capability and responsibility.

And it is one we need to resolve before the system resolves it for us.

*Next: The stack is losing ground — what do we call the engineer who remains?*

---

*Kiran's Notes is a LinkedIn newsletter on data engineering, architecture, and the future of software craft. Subscribe to follow The Vortex series.*

---
*#InterpretableAI #AIGovernance #RegulatableAI #DataEngineering #FinancialServices #KiransNotes #TheVortex*