# What "semantic" actually means now

**Published in**: *Kiran's Notes* (LinkedIn Newsletter)  
**Original URL**: [https://www.linkedin.com/pulse/what-semantic-actually-means-now-kiran-kumar-jverc/](https://www.linkedin.com/pulse/what-semantic-actually-means-now-kiran-kumar-jverc/)  
**Author**: Kiran Kumar ([@goelkiran](https://github.com/goelkiran) / [LinkedIn](https://www.linkedin.com/in/kirangoel))  

---

around 2001, proposed a machine-readable layer of meaning over the web — ontologies, structured relationships, data that carried its own definitions. It was an ambitious and largely correct idea that arrived ahead of its readers; the machines of the day could not do much with it. Closer to my own world, the business-intelligence semantic layer has been quietly doing this work for decades. The Business Objects "universe," the OLAP cube, then LookML, then the modern semantic layers — all of them exist to define a term like revenue or active customer once, so that every dashboard agrees on what it means. Define it in one place; consume it everywhere.

These were not failures. They understood the real problem: meaning has to be explicit and shared. What they had, that we no longer have, was a reader who could fall back on tacit knowledge. The dashboard could afford a slightly fuzzy definition of revenue because a human read the number and applied judgement. The new reader (LLM Agent) brings no judgement of its own to the domain. It brings inferred meaning, which is confident and often wrong in exactly the places that matter.

And declared meaning has two faces, both of which we will need. There are the definitions — what each entity means, the things you would put in a dictionary. And there are the relationships — how the entities connect, the things you would draw as a map. A fund contains share classes. A client holds positions. A security is a kind of instrument. Definitions are the nodes; relationships are the edges. Hold on to that pairing, because the thing I am about to argue we build has exactly that shape.

What to build
So here is the prescription. It has three parts, and they follow the path the first two articles laid down: the right format, in the right place, now carrying the right meaning.

First, build a semantic model and a knowledge graph — and let humans own them.
The semantic model is the dictionary with teeth. For each entity that matters, it declares the definition, an example or two, the synonyms that should map to it, and — this is the part most glossaries miss — the defaults and the known ambiguities. It records that "positions" is context-dependent and marks it, so a reader knows to resolve it or ask rather than guess. The knowledge graph is the map: the relationships between those entities, the hierarchy of fund to portfolio to share class, the edges a query has to traverse to be correct. Definitions and relationships. Nodes and edges. Two faces of one declared layer.

Both are authored by people and reviewed by people. This matters enough to say plainly: the agent does not get to write the canonical definitions. If the agent authored the declared layer, you would have inferred meaning governing inferred meaning — the model marking its own homework, the snake eating its tail. Domain experts and data engineers declare; the agent consumes and checks. Humans think; agents infer. The declared layer is where that line is drawn in ink.
