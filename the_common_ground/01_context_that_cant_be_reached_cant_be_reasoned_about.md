# Context that can't be reached can't be reasoned about

**Published in**: *Kiran's Notes* (LinkedIn Newsletter)  
**Original URL**: [https://www.linkedin.com/pulse/context-cant-reached-reasoned-kiran-kumar-gssec/](https://www.linkedin.com/pulse/context-cant-reached-reasoned-kiran-kumar-gssec/)  
**Author**: Kiran Kumar ([@goelkiran](https://github.com/goelkiran) / [LinkedIn](https://www.linkedin.com/in/kirangoel))  

---

The last article was about format — the substrate humans and agents can both read. This one is about location. A well-formatted Markdown specification is useless to an agent if it lives in a Confluence space behind a login, three clicks from the code. For an agent, distance is absence: what it cannot reach, it cannot reason about. We once kept requirements, tests, and scripts in the repository alongside the code, for human traceability. Agile dissolved that, for good reasons — trust and conversation replaced the sealed specification. A new reader brings the old discipline back, for a new reason. Co-locate everything, text-first, reachable in one pass.

The discipline we used to have
When I started out, software shipped on physical media. Floppy disks, then CDs — pressed, boxed, couriered to clients who might be on another continent. I was at Infosys in Mohali, building systems for Adidas in Herzogenaurach, near Erlangen, and there was a discipline to that era I have been thinking about lately.

When you ship software on a CD, you cannot patch it on Monday morning. Whatever is on the disc is what the client runs. So someone in the chain had to guarantee that the code, the binary, and the requirement all traced to the same specification. Validation and verification were both explicit — are we building the right thing, and are we building it right. Not because we were paranoid. Because the medium left no room for ambiguity.

So we kept everything together. The requirements lived in the repository, in a ./doc folder. The test cases lived in ./test. The scripts lived alongside the code they exercised. We versioned all of it in Visual SourceSafe, the same place the source lived. If you wanted to know what a module was meant to do, you did not open another tool or log into another system. You looked in the folder next to the code.

This was not elegant. VSS was not a good tool. But the artefacts were co-located, and co-location gave us something worth having: traceability by proximity. You could trace a clean line from what was asked to what was shipped.

That was the obligation of the era. And then the era changed.

Why the documents moved out
The vortex — the spinning system of cheaper hardware, software, and connectivity I wrote about earlier — did something to the distance between people.

As networks improved and travel grew cheaper, the communication distance between business and developer collapsed. A requirement no longer had to survive a long passage on paper. Stakeholders and engineers could talk — on a call, on a screen share, in a shared room. Business learned something in the process: if developers understood the requirement, they would build the right thing. Trust grew.
