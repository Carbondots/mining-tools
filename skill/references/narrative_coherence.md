# Narrative Coherence And Lead-In Logic

Use this file whenever a generated Introduction has enough content but reads like stacked material. The goal is to make the Introduction feel inevitable: each sentence should narrow, explain, challenge, or advance the previous one.

## Core Principle

Do not treat an Introduction as a container for all relevant facts. Treat it as a chain of pressure:

`scientific need -> data bottleneck -> literature evidence form -> extraction failure -> material-specific consequence -> constrained method necessity`

If a sentence does not change the reader's understanding of this chain, merge it, move it, or delete it.

## Before Drafting: Build A Narrative Spine

Write these four items before prose:

1. Controlling question: what unanswered problem makes the whole Introduction necessary?
2. Paragraph promise: what must each paragraph prove before the next paragraph can begin?
3. Bridge logic: why does paragraph N force paragraph N+1?
4. Final pressure: what exact method direction becomes necessary by the end, without claiming current-paper results?

Example spine:

- P1 proves that the material field needs relation-level, sample-level data rather than isolated property values.
- P2 shows that these data exist mainly in literature but are fragmented across text, tables, figures, and supplements.
- P3 explains why manual databases, rules, and NER can recover fragments but not evidence-bound records.
- P4 narrows the general bottleneck to the target material, where mis-binding changes the scientific conclusion.
- P5 argues for schema/RAG/LLM-prompt extraction as a constrained response to that bottleneck.

## Paragraph Lead-In Rules

Each paragraph's first sentence must do one of these jobs:

- **Continuation:** carry forward a term from the previous paragraph and deepen it.
- **Contrast:** show why the previous solution or assumption is insufficient.
- **Narrowing:** move from general materials literature to the target material system.
- **Consequence:** state what becomes wrong or impossible if the previous bottleneck is unresolved.
- **Necessity:** make the method direction a response to the problem, not a separate topic.

Avoid first sentences that simply announce a new topic: "近年来...", "此外...", "随着...", "另一方面...". These are acceptable only when the sentence also states the causal relation to the previous paragraph.

## Sentence Function Chain

For each paragraph, assign every sentence one function before polishing:

| Function | Role |
|---|---|
| Claim | States the paragraph's main message. |
| Reason | Explains why the claim is true. |
| Evidence manifestation | Shows where the issue appears in papers: text, tables, figures, captions, supplements, procedures. |
| Example | Gives a domain-specific example, not a generic slogan. |
| Consequence | Explains what scientific or extraction error follows. |
| Bridge | Makes the next sentence or paragraph necessary. |

A strong load-bearing paragraph usually follows:

`claim -> reason -> evidence manifestation -> domain example -> consequence -> bridge`

If two adjacent sentences have the same function and neither adds specificity, combine them.

## Anti-Stacking Revision

A draft is stacked when:

- sentences can be reordered without damaging the argument;
- each paragraph restarts from a generic background sentence;
- many sentences begin with "此外", "同时", "已有研究", or "LLM" but do not refer back to the previous sentence;
- methods are listed before the reader understands what failure they solve;
- the material-specific paragraph could be reused after replacing the material name.

Fix stacked prose by:

1. Repeating the controlling object deliberately: output object, relation, sample, evidence, or method object.
2. Turning topic jumps into cause-effect bridges.
3. Replacing survey lists with pressure chains: `useful part -> failure mechanism -> unresolved consequence`.
4. Moving generic NLP/LLM claims after the material-literature bottleneck has been established.
5. Ending each paragraph with a sentence that opens the exact need handled by the next paragraph.

## Transition Templates

Use these as logic patterns, not as fixed wording:

- `正因为 [material/data need], the relevant knowledge cannot be treated as isolated facts; it must be recovered as [output object].`
- `This shifts the bottleneck from whether the information exists to whether it can be bound to the correct [sample/relation/evidence].`
- `Manual curation partly solves [coverage/accuracy], but it leaves [scale/update/context] unresolved.`
- `Entity recognition is therefore only an intermediate step; the decisive problem is [relation/evidence binding].`
- `In [target material], this binding problem becomes more severe because [field-specific mechanism].`
- `Once [field-specific evidence] is mis-bound, the extracted record no longer represents [scientific conclusion].`
- `A useful LLM workflow must therefore be constrained by [schema/evidence/refusal], rather than merely asked to summarize papers.`

## Coherence Audit

Before accepting the draft, answer:

1. Can every paragraph's first sentence be traced to the previous paragraph's last sentence?
2. Does each paragraph contain at least one explicit causal, contrastive, or narrowing bridge?
3. Does the material-specific paragraph explain why this field is not just an example of generic "unstructured literature"?
4. Does the method paragraph inherit all prior pressure: output object, evidence binding, uncertainty/refusal, and domain relation?
5. If the draft's sentences are shuffled, does the argument break? If not, revise for stronger sentence dependence.

If any answer is no, revise before running the quality-control score.
