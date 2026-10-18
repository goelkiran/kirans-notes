# What "semantic" actually means now

*Kiran's Notes — The Common Ground, Article 2 of 5*

**Published in**: *Kiran's Notes* (LinkedIn Newsletter)  
**Original URL**: [LinkedIn Pulse](https://www.linkedin.com/pulse/what-semantic-actually-means-now-kiran-kumar-jverc/)  
**Author**: Kiran Kumar ([@goelkiran](https://github.com/goelkiran) / [LinkedIn](https://www.linkedin.com/in/kirangoel))  
**Date**: June 7, 2026  

---

## TL;DR

The first two articles were about format and location — the substrate humans and agents can both read, and reaching it in one pass. This one is about meaning. The word "semantic" has split in two. There is the meaning a model infers from training — embeddings, the geometry from Article 1 — and the meaning humans declare and govern. An agent arrives carrying the inferred kind; correctness needs the declared kind. When the declared layer is missing, meaning breaks in two silent ways: the agent merges terms the domain keeps apart, or it picks one meaning and never tells you.

The fix is a human-authored semantic model and knowledge graph, federated by department, versioned, checked out per project, and read on both the build side and the insights side. Define meaning once, and every reader/agent resolves it the same way.

## A sentence that breaks quietly

Here is a sentence that looks harmless.

"Show the client's current positions."

A business analyst writes it into a requirement. It is clear, it is short, and every human who reads it nods. An agent picks it up, reads the codebase, writes the query, and returns a clean answer. No error. No warning. And the answer is wrong.

It is wrong because the words did more work than anyone noticed. In asset management industry it is common to have a customer table and a client table, and they are not the same — customer is retail, the individuals who hold a fund, and client is institutional, the organisations whose money the firm runs under a mandate. The agent saw "client," found something close enough, and joined it. Positions means open, unsettled trades to the desk, and total holdings to the back office; the agent chose one. Current could mean as-of-now, as-of-last-close, or as-of-settlement; the agent assumed one. None of these choices was flagged. The agent did not know there was a choice to flag.

This is the part worth sitting with. A human analyst, handed the same sentence, would pause. They carry the meaning in their head — they know "client" is not "customer" here, they know to ask which "positions," they know "current" is a trap. They would walk to the desk and ask. The agent cannot walk anywhere. It reads what is written, infers the rest, and proceeds.

As of today, agents are not attending our daily standups where human resolve the dependencies and doubts. We are pushing them to auto/vibe code based on specs.

There are two ways this goes wrong, and they are worth naming, because once you can name them you start seeing them everywhere.

The first is silent collapse. The domain keeps two things apart, and the agent folds them into one. Customer and client. Fund, portfolio, and share class — three precise things in asset management, related but not interchangeable, that a model will happily treat as synonyms because in its training they often were. The distinction the business depends on disappears into a join, and nothing marks the loss.

The second is silent pick. A word has more than one settled meaning, and the agent chooses one. Positions. Cash — is that per-currency, converted to a base currency, or base plus near-cash instruments like institutional liquidity funds? Current. The agent does not weigh the options and surface the ambiguity. It selects, commits, and moves on. It does not flag the choice, because to flag it the agent would have to know the choice existed.

Neither failure may throw an error. That is what makes them dangerous. A crash you can catch. A confident wrong answer, produced fast and phrased fluently, propagates. It lands in a report, informs a decision, and is discovered — if it is discovered — a long way downstream. Not an acceptable outcome for a regulated industry.

## Two kinds of meaning

The trouble starts with the word itself. Semantic has been stretched across so much ground that it has lost its edges. Semantic web. Semantic search. Semantic layer. Semantic kernel. Five people can say "semantic" in a meeting and mean five different things, and the conversation proceeds because nobody notices they have each silently picked a meaning. The irony is not lost on me.

So let me draw one line through it, because this single distinction does most of the work.

There is meaning a model infers, and meaning humans declare.

Inferred meaning is what the model derives from its training — the embeddings I wrote about in Article 1, words placed as points in a space of thousands of dimensions, close to the words they tend to appear with. It is statistical, general, and probabilistic. It is why a model knows that "client" and "customer" are usually near-synonyms in ordinary English. The agent arrives already carrying this. It is the meaning it brings to the door.

Declared meaning is what a person writes down and governs. In this given organisation, a customer is a retail investor and a client is an institution, and here is the difference, and here is an example of each. It is specific, authored, and binding. It is not what the words tend to mean across the internet; it is what they mean here, on purpose, with someone accountable for the definition.

The whole problem in the sentence above is the gap between the two. The agent had inferred meaning and used it. The organisation needed declared meaning and had not supplied it. The model's statistical hunch overrode a distinction the business cared about, and there was nothing in its path to stop it.

Which gives the principle the rest of this article turns on: no silent resolution. When an agent meets an ambiguous term, it has three honest moves. It can resolve the term against a declared definition. It can apply a declared default — a meaning the organisation has marked as the one to assume when none is specified. Or it can ask. What it must not do is the fourth thing, the thing it does by default: guess from inferred meaning and proceed without a word.

The agent arrives with the inferred kind; correctness needs the declared kind. The gap between them is where meaning breaks — with no error thrown.

I want to be clear that this is not a new worry, and the people who saw it early deserve credit before I go further.

Meaning has been a known problem for a long time, and there have been serious attempts to fix it. The semantic web, set out by Tim Berners-Lee around 2001, proposed a machine-readable layer of meaning over the web — ontologies, structured relationships, data that carried its own definitions. It was an ambitious and largely correct idea that arrived ahead of its readers; the machines of the day could not do much with it. Closer to my own world, the business-intelligence semantic layer has been quietly doing this work for decades. The Business Objects "universe," the OLAP cube, then LookML, then the modern semantic layers — all of them exist to define a term like revenue or active customer once, so that every dashboard agrees on what it means. Define it in one place; consume it everywhere.

These were not failures. They understood the real problem: meaning has to be explicit and shared. What they had, that we no longer have, was a reader who could fall back on tacit knowledge. The dashboard could afford a slightly fuzzy definition of revenue because a human read the number and applied judgement. The new reader (LLM Agent) brings no judgement of its own to the domain. It brings inferred meaning, which is confident and often wrong in exactly the places that matter.

And declared meaning has two faces, both of which we will need. There are the definitions — what each entity means, the things you would put in a dictionary. And there are the relationships — how the entities connect, the things you would draw as a map. A fund contains share classes. A client holds positions. A security is a kind of instrument. Definitions are the nodes; relationships are the edges. Hold on to that pairing, because the thing I am about to argue we build has exactly that shape.

## What to build

So here is the prescription. It has three parts, and they follow the path the first two articles laid down: the right format, in the right place, now carrying the right meaning.

First, build a semantic model and a knowledge graph — and let humans own them.

The semantic model is the dictionary with teeth. For each entity that matters, it declares the definition, an example or two, the synonyms that should map to it, and — this is the part most glossaries miss — the defaults and the known ambiguities. It records that "positions" is context-dependent and marks it, so a reader knows to resolve it or ask rather than guess. The knowledge graph is the map: the relationships between those entities, the hierarchy of fund to portfolio to share class, the edges a query has to traverse to be correct. Definitions and relationships. Nodes and edges. Two faces of one declared layer.

Both are authored by people and reviewed by people. This matters enough to say plainly: the agent does not get to write the canonical definitions. If the agent authored the declared layer, you would have inferred meaning governing inferred meaning — the model marking its own homework, the snake eating its tail. Domain experts and data engineers declare; the agent consumes and checks. Humans think; agents infer. The declared layer is where that line is drawn in ink.

And there will not be one of these for the whole company. There will be many — one per department, because trading, compliance, and client services each have their own vocabulary, and a single global model would be either too rigid to maintain or too vague to help. Federated, not central. Each project then checks out the department-level slice it needs into the root of its repository, where the agent can reach it in a single pass — the co-location Article 2 argued for, now applied to meaning. The business analyst writes specifications against it; the agents iterate against it.

A word on those specifications, since they are about to do heavy lifting. Spec-driven development is the practice of writing the intent down — what should happen, in a form the agent builds from — rather than leaving it implicit in a conversation. I will give it the full treatment it deserves in the next article. For now, the point is what happens when the spec meets the semantic model. The spec says what should happen. The semantic model says what the words in it mean. Author a spec in the declared vocabulary, and the agent reads both the intent and the meaning from the same reachable place.

That pairing is the load-bearing claim of this whole series, so let me state it once, cleanly.

The spec and the semantic model are the twin anchor of the agentic software lifecycle.

One governs intent; the other governs meaning. Take either away and the agent is back to guessing.

Second, treat the declared layer as something with a lifecycle, not a one-time document.

Declare, govern, consume. Declaring is the authoring above. Consuming is the checkout.

Governing is the part that keeps the whole thing from rotting, and it is where the work actually lives. A federation of departmental models will overlap and conflict — compliance's "client" against sales's "client" — and definitions drift as the business changes. So the corpus of models and graphs is versioned, co-located with the work, and run through periodic automated review: an agent scanning the whole set for overlap, for ambiguity, for gaps where a term is used but never defined.

Note the shape of that review, because it is the same principle again. The agent flags; the humans resolve. It can find the conflict between two definitions of "client" far faster than a person scanning wikis ever could. It does not get to decide which one wins. No silent resolution — not at query time, and not in governance either. The human stays in the seat where the decision is made.

This is the honest part of the prescription, and I will not soften it: authoring and governing a semantic layer is real work. It is not a download. It is people sitting down to agree what their words mean and writing it where machines can read it. But the cost is real either way. Semantic entropy — the meaning that leaks at every boundary, which I named in Article 1 — compounds silently as you add agents, and it compounds fastest in exactly the high-stakes places where a wrong answer is most expensive. So the choice is not between paying and not paying. It is this: invest once, upfront, in a governed model — or pay forever, in wrong answers nobody caught.

Third, use the declared layer on the way out, not only on the way in.

So far this is about building software — specs to code. But the same declared meaning serves the other direction, when people and agents query the data and the APIs. Here the mechanism is the system prompt: the instruction that routes the model through the right semantic model and knowledge graph before it does anything. When it decodes a question, it resolves the terms against the declared definitions. When it generates SQL, it builds against the declared model rather than the raw schema. When it retrieves passages to answer a question, it uses the graph to find the right ones rather than matching on surface similarity. Same declared meaning, two paths out — the structured path of query generation and the unstructured path of retrieval.

Put the three parts together and the payoff is one line. Define once, resolve everywhere. The analyst, the spec author, the code-generating agent, the query agent, the person at a dashboard — all of them reading the same declared meaning, so "client" is the same client and "revenue" is the same revenue, on the way in and on the way out. It is the cure for the oldest complaint in data work, the one where finance and sales show up to the meeting with two different numbers and both swear theirs is right.

The agent arrives with the inferred kind; correctness needs the declared kind. The gap between them is where meaning breaks — with no error thrown.

## This is already happening

If this sounded speculative, it is not. The strongest evidence is that the serious data platforms have converged on exactly this shape, and they have done it because agents forced the issue.

Snowflake's Cortex Analyst is the clearest case. It answers natural-language questions by generating SQL, and the thing that makes it reliable is a semantic model — a YAML file that maps business terms to the database schema, defines what each metric means, and, tellingly, carries an explicit field for synonyms. Snowflake's own work reported that this declared model lifted text-to-SQL accuracy by around twenty per cent over giving the model the raw schema alone. The schema told the model the shape of the data. The semantic model told it the meaning. The meaning was worth twenty points.

dbt did something that answers the where-does-it-live question directly. At Coalesce in 2025 it open-sourced MetricFlow, the engine behind its semantic layer, under the Apache 2.0 licence, with the stated aim of powering trustworthy AI and agents. The mechanism is the part to notice: an agent asks for a metric by name, and the engine generates the SQL from the governed definition, so the result is — their phrase — correct by construction. The definitions are metrics-as-code: YAML in the Git repository, reviewed in pull requests, tested in the pipeline. That is the declared layer living exactly where Article 2 said it should, governed exactly the way this article argues for.

Cube describes the role of the declared layer better than I can. An engineer at Brex, talking about building agentic analytics on Cube's semantic layer, put it this way: the large language model is the engine, but the semantic layer is the map. The model supplies fluency; the declared meaning supplies the route. Cube's layer is open source, it connects to models through the same Model Context Protocol the industry is standardising on, and it was named in the 2026 Gartner Market Guide for agentic analytics — which tells you this has moved from idea to category.

For the relationship side — the knowledge graph rather than the metric definitions — the work is moving too. Microsoft's GraphRAG, open-sourced in 2024, builds a graph of entities and their relationships out of a body of documents, then lets a model traverse that graph to answer a question — which addresses the multi-hop, whole-corpus reasoning that flat similarity retrieval handles badly. It is the ontology branch of the same instinct: declare not just what things mean but how they connect, and let the agent walk the edges.

And the clearest signal of all is that competitors are agreeing on a standard. The Open Semantic Interchange effort has dbt, Snowflake, and Salesforce — with BlackRock among the co-leads, which should interest anyone in asset management — working on a shared specification for semantics, published in early 2026 under an open licence, so that meaning is portable across tools and clouds. Vendors do not standardise on something optional. They were, by the common phrase of the year, calling 2025 the year of the semantic layer. The agents are why.

## Onwards

Three articles, three layers of one common ground. Format, so both readers can parse the characters. Location, so the reader can reach them. Meaning, so they mean the same thing to everyone. The first two are mechanical — you verify them by looking. Meaning you have to declare, because it does not live in the artefact. It lives in the heads of the people who wrote it, and the new reader cannot see inside a head.

So the work of this layer is to get the meaning onto the page: a semantic model for what things mean, a knowledge graph for how they connect, owned by humans and read on the way in and the way out. But that is only half a pair. The semantic model says what the words mean. It does not say what should happen — and that second anchor, intent written down as a specification, is the one I have been circling for two articles now.

Next: Specs and semantics — the two surfaces humans must answer for, and why the specification is the one that turns intent into software.
