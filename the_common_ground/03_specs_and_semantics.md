# Specs and semantics — the two surfaces humans must answer for

**Published in**: *Kiran's Notes* (LinkedIn Newsletter)  
**Original URL**: [https://www.linkedin.com/pulse/specs-semantics-two-surfaces-humans-must-answer-kiran-kumar-ivltc/](https://www.linkedin.com/pulse/specs-semantics-two-surfaces-humans-must-answer-kiran-kumar-ivltc/)  
**Author**: Kiran Kumar ([@goelkiran](https://github.com/goelkiran) / [LinkedIn](https://www.linkedin.com/in/kirangoel))  

---

Three articles cleared the ground: a format both readers can parse, a location the agent can reach, a meaning everyone shares. None of them says what to build. Two human-authored surfaces do. The specification declares what should happen. The semantic model declares what things mean. Both are declarative, both are generative controls — they state what should be true, as opposed to the defensive controls (tests, evals, audit logs) that catch what went wrong — and both stay human. When an agent generates the implementation, these two are the only artefacts a person actually authored, which makes them the only things a person can answer for. Spec-driven development is the name the industry has landed on for the first surface. This piece is about why accountability concentrates on the two, and why the specification is the one that turns intent into software.

Half a pair
I ended the last article holding half a pair.

The semantic model gives an agent what the words mean — that a customer is a retail investor and a client is an institution, that positions is ambiguous and has to be resolved or asked. That is meaning. It is necessary. It is not sufficient. Knowing what the words mean does not tell you what to do with them. A dictionary is not an instruction.

The other half is the specification. The semantic model declares what things mean; the specification declares what should happen. Build this report. Apply this rule. When a trade settles, update these positions, in this order, with this treatment of the edge cases. One surface is the vocabulary. The other is the sentence written in it.

Put them together and you have what I called last time the twin anchor of the agentic software lifecycle. Both are declarative — they state what should be true, not how to make it so. Both are authored by people. Both are binding on the agent. And both, I want to argue, are the surfaces a human has to stay accountable for, long after the agent has taken over the typing.

Generative and defensive
There is a distinction worth drawing before going further, because it explains why these two surfaces matter more than the rest.

Some of the controls in a software system are generative. They declare what should be true, before the work is done. The specification is generative — it says what the system should do. The semantic model is generative — it says what the terms mean. They are the source. Everything correct in the system is meant to flow from them.

The rest of the controls are defensive. They catch what went wrong, after the work is done. Tests. Evaluations. Guardrails. Audit logs. Lineage. These are the net beneath the work — and they matter, more than ever, as I will come to. But a net does not decide what should be caught. It reports that something fell. The defensive controls can tell you the system is wrong. They cannot tell you what right was.

The generative half is where intent lives. And intent cannot be generated. An agent can write the code, propose the tests, draft the specification itself — but it drafts from what it was given, and the giving is human. Strip a system down to the artefacts that originated with a person, and you are left with two: what should happen, and what things mean. Specs and semantics. Everything else is downstream of them.

The specification is not new
Before I argue that the specification is becoming the centre of the work, I want to honour what it has always been. The instinct is old, and the people who held it were right.

We have been writing down what software should do for as long as we have built it. The requirements document. The functional spec. Design by contract — Bertrand Meyer's idea that a function should state its preconditions and postconditions as a binding promise. Behaviour-driven development, with its given-when-then, written to force ambiguity into the open before a line of code was cut. Acceptance criteria on a story card. Every one of these was an attempt to capture intent in a form that would survive the journey to implementation.

And every one of them met the same wall. The specification was documentation about the work, kept beside the work, and it went stale the moment the code moved on without it. The agile generation saw this and drew a hard lesson: working software over comprehensive documentation. The heavyweight spec, written once and frozen, had failed the pace of the internet. So the industry learned to travel light — to treat the conversation as the carrier of intent and the document as a cost.

That lesson was correct for its moment. I lived it; I taught it. The spec deserved its demotion, because nobody read it twice.

What changed is the reader.

Spec-driven development
When the entity reading the specification is an agent, the specification stops being documentation about the work and becomes the work.

This is the shift now travelling under the name spec-driven development. The idea is plain and, once you sit with it, hard to unsee. Instead of prompting an agent for code and hoping the result matches what you meant, you write the specification first. The agent generates a plan from the spec, a set of tasks from the plan, and the implementation from the tasks. The spec is the source of truth. The code is a build artefact of it — the way a compiled binary is a build artefact of source. If the behaviour is wrong, you do not patch the code. You fix the spec and regenerate.

GitHub open-sourced a toolkit for exactly this in September 2025, called Spec Kit. Its workflow is four moves — specify, plan, tasks, implement — and each move produces a Markdown artefact that feeds the next. GitHub's own framing is that we have been treating coding agents like search engines when we should treat them like literal-minded pair programmers: capable, fast, and in need of unambiguous instruction. The spec is how you give it.
