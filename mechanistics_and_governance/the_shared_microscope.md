# The shared microscope — why AI's rivals are cooperating to see inside their own models

**Published in**: *Kiran's Notes* (LinkedIn Newsletter)  
**Original URL**: [LinkedIn Pulse](https://www.linkedin.com/pulse/shared-microscope-why-ais-rivals-cooperating-see-inside-kiran-kumar-vw9lc/)  
**Author**: Kiran Kumar ([@goelkiran](https://github.com/goelkiran) / [LinkedIn](https://www.linkedin.com/in/kirangoel))  
**Date**: July 6, 2026  

---

Most of the machine reading that runs quietly inside investment, risk and insurance work is a black box, and the industry has learned to live with that. Models score filings, earnings calls, broker research, claims notes and news. The scores are useful. The signal is real. Nobody in the room can say, in plain language, what the model actually noticed — and for years that has been an acceptable trade. The output earns its keep, so the opacity is tolerated.

I want to honour that trade before I question it. The dense vectors these models produce carry more about a document than any analyst could annotate by hand. A thousand numbers, each meaningless on its own, together holding a reading of the text richer than the summary a person would write. That is not a flaw. It is the reason the technique works at all. The compression is the point.

And yet the opacity has a cost, because in regulated industries "why did the model flag this" is not an idle question. It is a question a regulator can ask.

Here is what has changed. A corner of AI research called mechanistic interpretability is starting to make the black box legible — and the way it doing so is worth watching even if you never train a model yourself.

---

## The technique, and a term worth remembering

A **sparse autoencoder**, or SAE, takes one of those tangled thousand-number vectors and decomposes it into a small set of named features — a learned dictionary in which each entry is, at best, a single concept.

It is an elegant idea, and I want to give it its due. Inside these models, concepts sit on top of one another; many meanings share the same handful of numbers. The field calls this superposition. The sparse autoencoder pulls the meanings apart, so that instead of a wall of numbers you get a handful of concepts that are actually firing on a given sentence — legible, one at a time. If you take one term away from this note, make it this one: *sparse autoencoder*. It is worth an hour of your own reading.

The idea is not confined to a whiteboard. Anthropic's "Golden Gate Claude" was the case that made it legible for everyone: turn one feature up, and the assistant became so fixated on the bridge that it worked the landmark into almost any reply. The same tooling shows how finely the dictionary can be carved — a mention of a dog can trip a feature for "dogs," or the wider "animals," or the narrower "chihuahuas," depending on how the concepts were cut.

---

## It is escaping language models

The signal that convinced me this is more than a curiosity is that the method is leaving language models behind.

Trained on protein models, SAEs recover features that line up with real biology, without being told what to look for. A [2025 study in PNAS](https://www.pnas.org/), from a team at MIT working on Meta's ESM2 protein model, surfaced sparse features tied to genuine protein families and functions — the NAD kinase family, the machinery of iron–sulfur cluster assembly — pulled out in an unsupervised pass and only named afterwards. On DNA models, the same approach has been used to find exon–intron boundaries and transcription-factor binding sites; the interpretability work on the Arc Institute's Evo 2 genome model runs through exactly this route.

The move here is to study the model in order to study the biology. The predictor stops being an oracle you either trust or distrust, and becomes something a scientist can reason with. In drug discovery, knowing *why* a model flagged a target is starting to matter as much as the flag itself.

---

## The part I keep coming back to

Consider [Neuronpedia](https://neuronpedia.org/). It is an open platform that now hosts tens of millions of these features across models from several labs, where anyone can browse the concepts a model has learned, watch which ones light up on a sentence, and steer them. It was built by Johnny Lin — an ex-Apple engineer who left consumer software to work on interpretability full time — with Joseph Bloom and others, in the orbit of Neel Nanda's research, then open-sourced and supported by Decode Research and Open Philanthropy. A small effort, holding open a window that the largest labs in the world are also looking through. It deserves the credit before anything else in this note.

And around that window, the labs converge. Google DeepMind open-sources its SAE suites — Gemma Scope — and hands the interactive demo to Neuronpedia. Anthropic open-sources its circuit-tracing tools, and made its first-ever investment in another startup: [Goodfire](https://www.goodfire.ai/), an interpretability company that Salesforce and Eric Schmidt later backed. OpenAI [publishes its own work](https://openai.com/) on scaling SAEs. Academic groups at MIT, Stanford and elsewhere put their results into the same shared tooling.

These are competitors on the capability leaderboard. They do not agree on much. They are cooperating on the instrument.

That is the thing I find worth sitting with. Not that we can see inside the models — that the field is building the microscope together, in the open, while racing each other on everything else. When rivals converge on a shared set of tools, it is usually because each of them has decided, on their own, that they cannot afford not to see inside. The cooperation is the tell.

---

## What it could map onto

The same engine that maps protein function can map the narrative structure of financial text. I find that worth thinking about for the investment, risk and insurance world, even from outside any one model.

*From an opaque score to named, auditable concepts:*  
An opaque document score could become a set of named, auditable concepts — guidance hedging, supply-chain stress, litigation language — rather than a number nobody can defend. Latent themes nobody predefined could surface as candidates for a thematic basket. A book's narrative exposure could be decomposed into concept features and watched as it drifts. And where a model decision has to be explained to a regulator, a feature carrying a validated label is a more defensible answer than "the model decided." In regulated work, that last point is not a nice-to-have. It is the difference between a control you can stand behind and one you cannot.

---

## The honest part

SAEs are early. They are strong at discovery and interpretability and far weaker as a turnkey source of alpha, and they demand careful validation before anything else near capital is touched. I want to be clear about that, because the failure mode here is treating an interpretability tool as a signal generator and skipping the validation that regulated work requires.

But in a field where "why did the model say that" is a compliance question, and in a moment where the rest of science is racing to open the same black box in the open, features that are interpretable by construction are worth watching closely.

---

*#InvestmentManagement #RiskManagement #MachineLearning #Interpretability #SAE #KiransNotes*
