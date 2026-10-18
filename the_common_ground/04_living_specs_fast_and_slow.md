# Living specs, fast and slow

**Published in**: *Kiran's Notes* (LinkedIn Newsletter)  
**Original URL**: [https://www.linkedin.com/pulse/living-specs-fast-slow-kiran-kumar-rqq5e/](https://www.linkedin.com/pulse/living-specs-fast-slow-kiran-kumar-rqq5e/)  
**Author**: Kiran Kumar ([@goelkiran](https://github.com/goelkiran) / [LinkedIn](https://www.linkedin.com/in/kirangoel))  

---

Date: (Published via Kiran's Notes)
A growing share of software is now built like this: you describe what it should do, in plain words, and an agent builds it from your description. The description — the spec — is the part you author. The code is what comes out the other side.

When the code is built from the spec, a stale spec stops being a tired document and becomes a wrong instruction. The agent does not pause and wonder whether the spec still matches reality. It reads what is in front of it and builds that, fast. A person reading an out-of-date runbook at least frowns. The agent does not frown. So the gap that opens between what we wrote down and what the system actually does — the thing we have always called drift — stops being a quiet mess in a wiki and becomes something that ships.

There is an odd upside hiding in this, though, and it is worth seeing. In the old way of working, the code was the truth and the document drifted away from it. Now the spec leads and the code follows. So the question we are left with changes. It stops being "is the documentation up to date with the code?" and becomes "is the spec still what we actually want?" That second question is a better one to be holding. One is bookkeeping. The other is about what you meant.

The one spec we already keep alive
Before going further, it is worth noticing that we already keep one kind of specification alive, and have for years. The test suite.

A test is a small, exact statement of what the code should do: given this input, expect that result. What makes a test different from a design document is that it runs. When someone changes the code and the behaviour no longer matches, the test fails — loudly, in front of the whole team. A test cannot quietly go out of date. The moment it stops being true, it says so.

This is the one corner of our work where the description and the thing it describes are kept in step on their own. Not by discipline. By the fact that the description is something a machine can run. The idea has a history worth knowing, and it has a name. Behaviour-driven development, with its plain "given, when, then" phrasing, and tools like Cucumber that turn those sentences into checks a machine can run, were all reaching for the same thing: a description of behaviour that a non-programmer could read and a computer could test. Gojko Adzic called the goal "living documentation" — writing that stays true because it is wired to the code it describes.
