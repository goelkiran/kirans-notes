# The whole message

*Kiran's Notes — The Common Ground, Article 5 of 5*

**Published in**: *Kiran's Notes* (LinkedIn Newsletter)  
**Original URL**: [LinkedIn Pulse](https://www.linkedin.com/pulse/whole-message-kiran-kumar-m9osc/)  
**Author**: Kiran Kumar ([@goelkiran](https://github.com/goelkiran) / [LinkedIn](https://www.linkedin.com/in/kirangoel))  
**Date**: June 27, 2026  

---

## TL;DR

Before a long holiday, you write a handover differently than a normal note — you spell out the things you would usually leave unsaid, because for three weeks nobody can ask you what you meant. That is the oldest problem in communication: getting the whole of what you mean into a message a reader cannot question. An agent working from your spec is the lowest-context reader you will ever write for — it shares none of your unspoken world — and as the work moves to autopilot, it loses even the ability to stop and ask. So the message has to carry everything. This is the last article in the series, and it ends not with answers but with the questions that leaves me holding: about working asynchronously, about whether intent can move between agents, about the craft of writing it, and about whether intent can be made to correct itself the way a deep-space message does.

## A message for a reader who can't ask

Before a long holiday once, I spent an afternoon on a handover. Not the usual two lines — a proper document — because I knew I would be unreachable for a few weeks, with a bad signal and a firm intention not to check email. Whoever picked up my work would have only the document. They could not ask me what I meant.

So I wrote differently than I normally do. I spelled out the things I would ordinarily leave unsaid — the bits that "everyone knows" — because I could no longer count on someone tapping me on the shoulder.

That small discomfort, writing for a reader who cannot ask, is a version of the oldest problem in communication. And the purest attempt at it ever made is bolted to a spacecraft.

In 1977 two Voyager probes left Earth carrying a gold-plated record of sounds and images — music, a greeting, a baby's cry, waves on a shore. The people who made it had to assume the reader would share nothing with them. Not a language. Not a biology. Not even the idea of what a record is. So they etched the instructions onto the cover: how to play it, how fast to spin it, and a map of pulsars showing where it came from — all measured against the one thing they hoped any reader could recognise, the hydrogen atom. It is the most careful message we have ever written, precisely because it had the least shared understanding to lean on. Nobody would be there to explain it.

## One word, two meanings

I have leaned on a word there that has quietly come to mean two things, and the two meanings meet in this article.

When the people who built that record worried about shared context, they meant it the way the anthropologist Edward Hall did: the web of things two people take for granted, so that they never have to be said. When an engineer today says context, they usually mean something narrower — the text loaded into a model's window, the files and instructions it can see. This whole series has been about the second kind of context. This last piece is about the first, because the first is what the second is for.

Hall drew a line between high-context and low-context communication. In a high-context exchange, most of the meaning lives in what is shared and unspoken — a glance between old colleagues, a one-word instruction that lands because you both know the whole backstory. In a low-context exchange, the meaning is in the message itself, set down plainly, because little can be assumed. People who know each other well talk in high context. Strangers, and lawyers, and anyone writing for a reader far away, talk in low context.

An agent working from your spec is the lowest-context reader you will ever write for. It does not share your week, your hallway conversations, the thing the team agreed on Tuesday and never wrote down. And when it works on its own while you sleep, it cannot do the one thing even a brand-new colleague would — stop and ask. So everything you would normally leave to shared understanding has to come up out of your head and into the message. The whole message. That is the standard the Golden Record was built to. It is, a little strangely, the standard a spec is now drifting toward.

## The asking is going away

For now there is a safety valve. Today's agents do ask. Meet an ambiguous spec and a good one stops and checks, and the round-trip costs you a minute.

But the shape of the work is changing. We are practicing both choreography and orchestration modes with Agentic AI Engineering. More and more, the orchestration runs on its own — the agent plans, writes, fixes, and reruns its own tests without coming back to you. The natural endpoint looks a little like working with a team across a wide time zone: you hand over the intent in the evening and review the results in the morning. And the further apart the handover and the review drift, the more the message has to carry by itself, because the cost of a clarifying question has gone from a minute to a day.

Which is where I want to end — not with answers, but with the questions this leaves me holding.

## Four things I don't have answers to

Whether we have trained the right muscle. If we are heading for a world where intent goes in at night and work comes back in the morning, then the moment of writing the spec becomes the only moment we are fully in control. Everything after is unsupervised. We have spent decades learning to work in tight loops, correcting as we go, catching our own vagueness halfway through. Writing the whole message up front, before anyone starts, is a different skill — and I am not sure we have trained it. The craft may have to move almost entirely to that first hour.

Whether intent can move between machines. This is the one I find hardest to put down. If intent is the real artifact — if the spec and the meaning are what a human authors and answers for — then it should not be welded to one machine. I ought to be able to start a job in one tool, on one company's model, and hand the half-finished work to another tool on a different model without losing the thread: stop midway in Antigravity and pick the same task up in Claude Code, before the first agent has even finished. The series argued for cognitive portable formats, intent that any reader can reach and understand. But the per-change state — the plan, the working notes, the half-built thing — is that portable too? Or does the handover still drop something on the floor? Whether intent (along with whole harness) is the common ground, or only feels like it, gets decided right there.

Whether writing it becomes a craft we share with the agent. This one is more hopeful. Writing the whole message will become a craft of its own, and I don't think it will be a lonely one. The person who writes the intent — and that is becoming a design job as much as an engineering one — will do it in a loop with the some (sometimes even the same that will carry it out) agents, asking them, before the work begins, where the message is still thin. The agent stops being only the reader and becomes the editor that shows you the ambiguities and gaps while you can still close them. Closing them up front is the price of being allowed to walk away and sleep.

Whether intent can be made to repair itself. This is the one I keep circling. When an agent runs unsupervised for hours and drifts from what you meant, what pulls it back? Part of the answer we already have: a test that fails is a drift detector, and an agent that re-reads the spec against the code is a corrector of sorts. But that is mostly error detection — it tells you something is wrong. I keep thinking about the harder trick, the one deep-space engineers solved decades ago. A Voyager probe cannot ask Earth to resend a corrupted picture; the round-trip is measured in hours or years. So the message is built to repair itself. Reed–Solomon codes — the same family that rebuilds the scratched audio on a compact disc — add enough structured redundancy that the receiver can reconstruct what was lost without ever asking. Detect and rebuild, alone, rather than detect and request. Is there an equivalent for intent? Could we write a spec with enough redundancy — the same meaning stated more than one way, each part checkable against the others — that an agent could notice it had drifted and recompute what we meant, without waking us? And the honest other half of the question: do we even need that machinery, or is it cheaper to re-ground the agent often and lightly than to armour the message? I don't know. I find that I want to.

## Onwards

That is where the series ends. Not because the questions are answered, but because they are the right ones to be holding now — and they all come back to the place we started: the gap between one mind and another, and the old, hard work of getting the whole of what you mean across it.

We are learning to write for readers we will not be there to help. The probe is already past the edge of the solar system, carrying its careful message to no one in particular. We are about to do a smaller version of the same thing most nights — hand over the whole of what we mean, and ask for the work back by morning. The least we can do is write the message well.

This is the final article in The Common Ground, Reforming.

Kiran's Notes is a LinkedIn newsletter on data engineering, architecture, and the future of software craft.

---

*#AgenticAI #SoftwareEngineering #SpecDrivenDevelopment #HumanInTheLoop #DataEngineering #KiransNotes #TheCommonGround*
