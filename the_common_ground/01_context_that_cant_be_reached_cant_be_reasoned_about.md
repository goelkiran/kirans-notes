# Context that can't be reached can't be reasoned about

*Kiran's Notes — The Common Ground, Article 1 of 5*

**Published in**: *Kiran's Notes* (LinkedIn Newsletter)  
**Original URL**: [LinkedIn Pulse](https://www.linkedin.com/pulse/context-cant-reached-reasoned-kiran-kumar-gssec/)  
**Author**: Kiran Kumar ([@goelkiran](https://github.com/goelkiran) / [LinkedIn](https://www.linkedin.com/in/kirangoel))  
**Date**: May 23, 2026  

---

## TL;DR

The last article was about format — the substrate humans and agents can both read. This one is about location. A well-formatted Markdown specification is useless to an agent if it lives in a Confluence space behind a login, three clicks from the code. For an agent, distance is absence: what it cannot reach, it cannot reason about. We once kept requirements, tests, and scripts in the repository alongside the code, for human traceability. Agile dissolved that, for good reasons — trust and conversation replaced the sealed specification. A new reader brings the old discipline back, for a new reason. Co-locate everything, text-first, reachable in one pass.

## The discipline we used to have

When I started out, software shipped on physical media. Floppy disks, then CDs — pressed, boxed, couriered to clients who might be on another continent. I was at Infosys in Mohali, building systems for Adidas in Herzogenaurach, near Erlangen, and there was a discipline to that era I have been thinking about lately.

When you ship software on a CD, you cannot patch it on Monday morning. Whatever is on the disc is what the client runs. So someone in the chain had to guarantee that the code, the binary, and the requirement all traced to the same specification. Validation and verification were both explicit — are we building the right thing, and are we building it right. Not because we were paranoid. Because the medium left no room for ambiguity.

So we kept everything together. The requirements lived in the repository, in a ./doc folder. The test cases lived in ./test. The scripts lived alongside the code they exercised. We versioned all of it in Visual SourceSafe, the same place the source lived. If you wanted to know what a module was meant to do, you did not open another tool or log into another system. You looked in the folder next to the code.

This was not elegant. VSS was not a good tool. But the artefacts were co-located, and co-location gave us something worth having: traceability by proximity. You could trace a clean line from what was asked to what was shipped.

That was the obligation of the era. And then the era changed.

## Why the documents moved out

The vortex — the spinning system of cheaper hardware, software, and connectivity I wrote about earlier — did something to the distance between people.

As networks improved and travel grew cheaper, the communication distance between business and developer collapsed. A requirement no longer had to survive a long passage on paper. Stakeholders and engineers could talk — on a call, on a screen share, in a shared room. Business learned something in the process: if developers understood the requirement, they would build the right thing. Trust grew.

And trust changed the shape of the work. The focus shifted from proving that you had built what was asked to discovering together what should be built. Developers became partners in requirement elicitation, not recipients of a sealed specification. Agile prevailed — not as a fashion, but as a response to a real change in the cost of communication.

The strict, structured, co-located requirement document was no longer the mechanism of trust. Conversation was. Shared understanding, built in stand-ups and reviews and three-amigos sessions, replaced the document that once had to carry everything because nobody could ask a question.

Validation and verification did not disappear. They became implicit — folded into sprint reviews, continuous delivery, the constant feedback of working software. And as the document stopped being the carrier of trust, it drifted. Out of the repository. Into Confluence. Into Jira. Into SharePoint, into shared drives, into someone's OneDrive. The cross-references remained — Jira linked to Confluence, Confluence to the repo. But the proximity was gone. Location was no longer deemed necessary.

I want to be clear about something. This was not a mistake.

## What the move got right

The tools that absorbed our documents were built to solve real problems. Atlassian was founded in 2002 by two developers, and Jira began life as an issue tracker — a developer's tool. But the products grew to serve a wider room. Confluence gave non-technical stakeholders a place to write without learning version control. Jira gave managers visibility — boards, burndown charts, roadmaps, the ability to see across a programme without reading code.

These were real advances. A scrum master coordinating six teams needs a board, not a git log. A product owner tracking a release needs a roadmap, not a directory listing. A business stakeholder contributing a requirement should not have to learn branching and merging to do it. The separation of concerns — code in the repository, documents in the wiki, tickets in the tracker — was a rational response to different people, with different skills, working on different things.

The agile manifesto valued working software over comprehensive documentation, and it was right to. The heavyweight specification, written once and frozen, had failed the internet era. Requirements changed too fast. The document was stale before the ink dried.

So the documents moved out for good reasons, and the people who moved them were not careless. They were responding to the constraints of their moment — exactly as we had responded to ours, when we kept everything in ./doc because a CD could not be patched.

And yet.

## What the move left behind

Something was lost when the artefacts dispersed, and we did not name it at the time.

We lost traceability by proximity — the ability to open one location and see the requirement, the design, the code, the test, and the history of what went wrong, all tied to the same version. The cross-reference is not the same as the co-location. A link from Jira to Confluence tells you where to go; it does not put the thing in front of you. Every hop is a context switch, a login, a search, a moment where the thread can break.

Nowhere is this clearer than with the analyst.

Consider how data and requirement analysis works in most enterprises today. An analyst investigates a question. They write SQL — sometimes a great deal of it, careful and clever — in a standalone tool. They save it on their own drive. The script is rarely committed to the project repository. It is seldom linked to the Jira ticket that prompted it. It is almost never tied to the release version of the code it informed. When the analyst moves teams, or leaves, the knowledge leaves with them. The script that explained why a number looked the way it did is gone, or buried in a folder no one will find.

This is not the analyst's failing. The tools they were given saved work outside the project structure by default. The path of least resistance led away from the repository, not toward it. We built workflows where the most valuable diagnostic work a person does ends up the least reachable.

For a human, this is a cost. You can usually find the analyst, ask them, reconstruct the reasoning. Expensive, but possible.

For an agent, it is not a cost. It is a wall.

## A reader who cannot ask

Here is what changes with agentic AI in the workflow.

An agent does not attend the stand-up. It cannot absorb shared understanding through a hallway conversation. It cannot build intuition over months on a team. It cannot find the analyst and ask what the script was for. It reads what it can reach, and it reasons about what it reads. What it cannot reach does not exist.

For an agent, distance is absence.

A Markdown specification — well-formatted, cognitively portable, everything the last article argued for — is invisible to an agent if it lives in a Confluence space behind an authentication boundary, three clicks and an API call from the repository the agent is working in. The format is right. The location is wrong. And location is not a minor detail. It is the difference between context that informs the work and context that might as well not exist.

This is why the old discipline returns. Not because waterfall was right and agile was wrong — that is the pendulum reading, and as I argued earlier, the pendulum is the wrong metaphor. The ground has shifted. We are not going back to ./doc because sealed specifications were better. We are going back to co-location because a new reader has joined the team, and that reader can reason only about what it can reach.

The old motivation was traceability, for humans. The new motivation is accessibility, for agents. Both point to the same place. Bring the artefacts home.

## Bringing the artefacts home

## What does this look like in practice?

Requirements and design in the repository, written in Markdown and Mermaid — diffable, reviewable, versioned with the code they govern. The analyst's SQL committed alongside the module it queries, tied to the release it informed. Test cases and their results in the repository, not emailed around. Architecture decisions where the code can see them. Observability insights and incident write-ups linked to the lines they concern. And a context file — a CLAUDE.md, an AGENTS.md, a README that has grown up — that tells any reader, human or agent, how the project is shaped and where things live.

All of it text-first. All of it a first-class citizen for the agent that will read it.

The monorepo has two axes, and the industry built only one.

The familiar one is horizontal. Google and Meta keep vast amounts of code in a single repository — code consolidated with code, across projects and teams. Call it the horizontal monorepo. It is not what I am describing. Google runs the best-known monorepo in the industry and still keeps its design documents in Google Docs, its incidents in separate tooling, its requirements in a tracker. The horizontal monorepo consolidated the code and left the artefacts where they were.

The other axis is vertical. Not code with code, but every artefact with the code it concerns — requirement, design, script, test, incident, gathered in one place. Call it the vertical monorepo. Docs-as-code came closest to the instinct a decade ago: documentation in Markdown, versioned beside the code, reviewed through pull requests. It had the right idea. But it made its case for a human reader. What changes now is the reader. Co-location stops being a nicety that disciplined teams adopt and becomes a requirement, because the new reader cannot ask.

One repository for a project — code with the requirement that shaped it, the design that governs it, the script that diagnosed it, the test that proves it, the incident that marked it. Co-located not because it is tidy, but because the reader can reason only about what it can reach.

Now consider what becomes possible when the context is all in one place.

A new requirement lands. An agent reads it against the codebase, the design notes, and the existing tests, and identifies the impacted modules in minutes. Today, a senior engineer spends half a day cross-referencing Confluence pages and Jira tickets to answer the same question.

A developer fixes a bug. The agent updates the affected documentation, adjusts the test expectations, and annotates the design note — because all of them live in the same repository, in the same change. Today, documentation drift is the default, and the doc is wrong within a sprint.

Support investigates an incident at two in the morning. They find the analyst's diagnostic scripts in the repository — versioned, tied to the right release, ready to run — instead of paging someone to search a personal drive. The reasoning done once is available to whoever needs it next.

An architect reviews a change for acceptance. They compare the prescribed design, which lives in the repository, against the implementation, which lives beside it, and find the drift in minutes. They assess its impact while the change is still a change, not after it has shipped.

None of these scenarios needs a new tool. They need the artefacts to be in one reachable place, in a format the reader can parse. The capability has been waiting on the co-location.

And the benefits are not only for agents. The team that co-locates gets things humans have wanted all along. Onboarding becomes a matter of reading one repository instead of hunting across four tools. The audit trail records who changed what, when, and why — across every artefact, not only the source. A pull request that changes the code and updates the affected specification is reviewable as a single, coherent unit. And the question "which version of this document is the current one" stops being asked, because there is one, and it lives where the work lives.

## Onwards

There is a symmetry here worth sitting with. We co-located in the era of CDs because the medium would not forgive a mismatch. We dispersed in the era of agile because trust and conversation made proximity feel unnecessary. We co-locate again in the era of agents because a reader has joined who cannot ask, cannot wait, and cannot reach beyond what we place in front of it.

Three eras. Three motivations. The same answer recovering.

The last article argued for the right format — cognitively portable, readable by human and agent alike. This one argues for the right place — physically proximate, reachable in a single pass. Format without proximity is half the substrate. You can write the cleanest Markdown in the world, and if it lives where the agent cannot reach it, you have written it for no one.

Get both right, and something quiet and powerful happens. The context stops being a thing you maintain and starts being a thing the work can rely on.

But format and proximity still leave a harder question untouched. Even when an artefact is reachable and readable, the words inside it have to mean the same thing to everyone who reads them. And meaning, it turns out, is the slipperiest substrate of all.

## Have your teams started thinking and working on vertical monorepo?

Next: What "semantic" actually means now — the word everyone uses and no one defines.

---

*#SoftwareArchitecture #DevOps #DocsAsCode #Monorepo #AgenticAI #DataEngineering #KiransNotes #TheCommonGround*
