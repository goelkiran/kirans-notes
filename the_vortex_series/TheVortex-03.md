# Agile and microservices were invented for people, not for machines

*Kiran's Notes — The Vortex, Article 3 of 12*

**Published in**: *Kiran's Notes* (LinkedIn Newsletter)  
**Original URL**: [LinkedIn Pulse](https://www.linkedin.com/pulse/agile-microservices-were-invented-people-machines-kiran-kumar-x9ekc/)  
**Companion Graphic**: [TheVortex-03.jpeg](../assets/TheVortex-03.jpeg)  
**Author**: Kiran Kumar ([@goelkiran](https://github.com/goelkiran) / [LinkedIn](https://www.linkedin.com/in/kirangoel))  

---

Before I question something, I want to honour it first.

The practices that define how most software teams work today — agile sprints, microservices, DevOps, continuous delivery — were genuinely brilliant solutions to genuinely hard problems. They deserve more than a dismissive "well, that's over now." They deserve understanding. Because only when you understand *why* something was invented can you honestly ask whether the reason still applies.

---

## The army problem

By the mid-2000s, the technology industry had created something that had never existed before: a global army of software engineers. Hundreds of thousands of professionals — in San Francisco, Bangalore, London, Warsaw, Beijing — all trying to contribute to the same growing software systems.

This created a coordination problem of extraordinary complexity. How do you let hundreds of people work on the same codebase without constantly breaking each other's work? How do you deploy changes made by a team in Gurugram without waiting for sign-off from a team in New York? How do you give every engineer a meaningful unit of contribution, rather than a narrow task in a system they can't see the shape of?

These were not technical problems at their core. They were human problems. Organisational problems. Problems of coordination, communication, and autonomy at scale.

Microservices and agile were the answers the industry found.

---

## Microservices: a democratic architecture

The monolithic application — one large system where every component is tightly coupled — was a perfectly reasonable approach when engineering teams were small and sat together. When you can tap the person next to you on the shoulder to explain why you changed that function, tight coupling is manageable.

But at scale, the monolith became a coordination nightmare. A change in one part of the system could break something in a completely different part. Deployments required everyone to agree on the same window. A bug introduced by one team could take down a service owned by another.

Microservices decomposed this problem. Break the system into small, independent services. Each service owns its own data, exposes a clear interface, and can be deployed independently. Give each service to a small team — Amazon famously called these "two-pizza teams," small enough to be fed by two pizzas — and let that team own it end to end.

This was, at its heart, a democratic architecture. Every team gets their plot of land. Their bounded context. Their deployment pipeline. Their on-call rotation. Their autonomy. No single team can break everything. No single engineer becomes a bottleneck.

I spent years building within this model at Fidelity — breaking apart legacy monoliths, defining service boundaries, establishing team ownership. It worked. It genuinely worked, at the scale it was designed for, with the people it was designed around.

---

## Agile: a democratic process

Alongside microservices, agile provided a complementary answer for how work itself should be organised.

The waterfall model — define everything upfront, build for months, release — was designed for a world where requirements were stable and teams were small. Neither was true at internet scale. Requirements changed constantly. Teams were large and distributed. The feedback loop between building and learning was dangerously long.

Agile broke work into small units — sprints, user stories, iterations — each short enough that any individual engineer could deliver something meaningful in two weeks. Stand-ups, retrospectives, planning sessions, demos — these were rituals designed so that no single human became the bottleneck, and no single voice dominated the room.

The two-week sprint was not an arbitrary choice. It was calibrated to human working memory, human attention spans, and the human need to see progress. It gave every engineer — regardless of seniority, regardless of geography — a regular opportunity to contribute and be seen.

That is a democratic process. Inclusive by design.

---

## An honest tribute

I want to be clear about something. These practices were not invented by people who didn't understand software. They were invented by people who understood it deeply — and who understood even more deeply the challenge of coordinating large numbers of human beings building it together.

They solved real problems. Netflix's chaos engineering, born from microservices thinking, made their streaming platform genuinely resilient. Amazon's two-pizza team model gave them the organisational agility to build AWS while running retail. Agile saved countless projects from the death march of waterfall planning.

If you are working in software today, you are probably benefiting from decisions made by engineers who wrestled with these problems honestly and came up with answers that held up at scale, for years.

That matters. It deserves acknowledgement before anything else.

---

## The question I am now asking

And yet.

The constraint these practices were solving — how to coordinate the cognitive bandwidth of a large army of human engineers — is now changing. Not because the army has gone away. But because a new participant has entered the picture, one that doesn't share any of the human limitations that made these solutions necessary.

That participant is the subject of the next article.

*Next: It never went to engineering college — and that might be the point.*

---


---
*#AgileMethodology #Microservices #SoftwareEngineering #TechLeadership #DataEngineering #KiransNotes #TheVortex*
