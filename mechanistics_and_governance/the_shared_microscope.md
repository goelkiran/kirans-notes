# The shared microscope — why AI's rivals are cooperating to see inside their own models

**Published in**: *Kiran's Notes* (LinkedIn Newsletter)  
**Original URL**: [https://www.linkedin.com/pulse/shared-microscope-why-ais-rivals-cooperating-see-inside-kiran-kumar-vw9lc/](https://www.linkedin.com/pulse/shared-microscope-why-ais-rivals-cooperating-see-inside-kiran-kumar-vw9lc/)  
**Author**: Kiran Kumar ([@goelkiran](https://github.com/goelkiran) / [LinkedIn](https://www.linkedin.com/in/kirangoel))  

---

Date: July 6, 2026
Most of the machine reading that runs quietly inside investment, risk and insurance work is a black box, and the industry has learned to live with that. Models score filings, earnings calls, broker research, claims notes and news. The scores are useful. The signal is real. Nobody in the room can say, in plain language, what the model actually noticed — and for years that has been an acceptable trade. The output earns its keep, so the opacity is tolerated.

It is an elegant idea, and I want to give it its due. Inside these models, concepts sit on top of one another; many meanings share the same handful of numbers. The field calls this superposition. The sparse autoencoder pulls the meanings apart, so that instead of a wall of numbers you get a handful of concepts that are actually firing on a given sentence — legible, one at a time. If you take one term away from this note, make it this one:
sparse autoencoder
. It is worth an hour of your own reading.

The idea is not confined to a whiteboard. Anthropic's "Golden Gate Claude" was the case that made it legible for everyone: turn one feature up, and the assistant became so fixated on the bridge that it worked the landmark into almost any reply. The same tooling shows how finely the dictionary can be carved — a mention of a dog can trip a feature for "dogs," or the wider "animals," or the narrower "chihuahuas," depending on how the concepts were cut.

It is escaping language models
The signal that convinced me this is more than a curiosity is that the method is leaving language models behind.

Trained on protein models, SAEs recover features that line up with real biology, without being told what to look for. A
2025 study in PNAS
, from a team at MIT working on Meta's ESM2 protein model, surfaced sparse features tied to genuine protein families and functions — the NAD kinase family, the machinery of iron–sulfur cluster assembly — pulled out in an unsupervised pass and only named afterwards. On DNA models, the same approach has been used to find exon–intron boundaries and transcription-factor binding sites; the interpretability work on the Arc Institute's Evo 2 genome model runs through exactly this route.

The move here is to study the model in order to study the biology. The predictor stops being an oracle you either trust or distrust, and becomes something a scientist can reason with. In drug discovery, knowing
why
a model flagged a target is starting to matter as much as the flag itself.

The part I keep coming back to
Consider
Neuronpedia
. It is an open platform that now hosts tens of millions of these features across models from several labs, where anyone can browse the concepts a model has learned, watch which ones light up on a sentence, and steer them. It was built by Johnny Lin — an ex-Apple engineer who left consumer software to work on interpretability full time — with Joseph Bloom and others, in the orbit of Neel Nanda's research, then open-sourced and supported by Decode Research and Open Philanthropy. A small effort, holding open a window that the largest labs in the world are also looking through. It deserves the credit before anything else in this note.
