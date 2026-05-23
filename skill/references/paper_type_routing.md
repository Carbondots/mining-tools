# Paper-Type Routing For Text-Mining Introductions

Use this file before drafting or benchmarking. The same five-paragraph fallback should not be forced onto every text-mining paper. First identify the paper type, then adapt the Introduction pressure chain.

## Routing Step

Classify the target manuscript into one primary type and, if needed, one secondary type:

1. **Extraction/database paper**: builds structured records from literature.
2. **RAG/literature-synthesis paper**: answers or synthesizes scientific questions with citations.
3. **Relation-prediction paper**: extracts a domain relation and uses it for prediction or validation.
4. **System-chart/knowledge-graph paper**: reconstructs mechanism or causal relation networks.
5. **Hypothesis-generation paper**: generates design hypotheses from extracted knowledge.

The opening object, bottleneck, and method necessity must match the type. Do not turn every paper into a generic "structured database" story.

## Type 1: Extraction Or Database Paper

Use for reaction records, synthesis records, property databases, sample-level records, or field extraction pipelines.

- Opening object: `reaction record`, `sample-level material record`, `synthesis recipe`, `property record`.
- Core pressure: the field needs comparable records, but literature scatters fields across text, tables, figures, captions, and supplements.
- Prior-route bottleneck: manual curation is accurate but narrow; rules/NER recognize entities but fail at sample-level binding.
- Method necessity: schema/prompt/RAG/LLM must output evidence-linked records and mark missing values.
- Avoid: writing only "literature is unstructured" without field roles, sample identity, or missing-value refusal.

Benchmark signal: ReactionSeek uses reaction role, condition, yield, and text-image alignment as the real data object.

## Type 2: RAG Or Literature-Synthesis Paper

Use for OpenScholar-like systems, review-question answering, citation-grounded synthesis, or scientific literature summarization.

- Opening object: `citation-grounded long-form answer`, `evidence-linked synthesis`, `review question response`.
- Core pressure: scientific questions require multi-paper synthesis, not isolated extraction records.
- Prior-route bottleneck: generic LLMs can summarize fluently but fail on coverage, citation correctness, transparency, and expert verifiability.
- Method necessity: retrieval, self-feedback, citation verification, and expert evaluation are central, not optional accessories.
- Avoid: forcing material-specific sample/schema language when the benchmark is about literature synthesis quality.

Benchmark signal: OpenScholar's method necessity is anchored in citation correctness, coverage, transparency, and expert evaluation.

## Type 3: Relation-Prediction And Validation Paper

Use for papers that extract a scientific relation and use it in ML prediction or experimental validation.

- Opening object: `host-dopant-emission relationship`, `composition-property relation`, `processing-property record`.
- Core pressure: prediction requires relation-level data, not isolated values.
- Prior-route bottleneck: entity extraction finds materials and values but misses the binding that makes the relation valid.
- Method necessity: extraction must preserve the relation context and downstream model meaning.
- Avoid: overemphasizing generic database construction while underexplaining why the extracted relation supports prediction.

Benchmark signal: phosphor emission work depends on host lattice, dopant identity/valence, emission wavelength, and validation context.

## Type 4: System-Chart Or Knowledge-Graph Paper

Use for materials system charts, processing-structure-property graphs, mechanism graphs, or knowledge graphs.

- Opening object: `P-M-S-M-P system chart`, `processing-structure-property graph`, `mechanism-aware knowledge graph`.
- Core pressure: the field needs causal/mechanistic relations, not only nodes or values.
- Prior-route bottleneck: NER and relation extraction can recover fragments but often flatten mechanisms, directionality, and information-source labels.
- Method necessity: LLM/schema workflow must preserve node types, edge direction, source labels, and uncertainty.
- Avoid: calling the output a database when the real object is a graph or chart that preserves reasoning.

Benchmark signal: system-chart papers spend substantial space defining the chart because the schema is the scientific argument container.

## Type 5: Hypothesis-Generation Paper

Use for papers that generate design hypotheses, mechanism combinations, or new candidate reasoning from extracted knowledge.

- Opening object: `scientifically grounded design hypothesis`, `synergistic mechanism hypothesis`, `candidate design rationale`.
- Core pressure: materials design needs hypotheses that combine mechanisms beyond a designer's existing knowledge.
- Prior-route bottleneck: generic LLM ideation can be fluent but not necessarily grounded, synergistic, or experimentally actionable.
- Method necessity: the workflow must connect extracted system charts, scientific grounding, synergy evaluation, and expert/auditable checks.
- Avoid: framing the paper as simple extraction or summarization. The central object is the quality of the generated hypothesis.

Benchmark signal: design-hypothesis papers define what makes a hypothesis valuable: synergy, grounding, mechanism interaction, and downstream design relevance.

## Benchmark Gap Interpretation

When comparing a generated omit-results Introduction with a full published article:

1. Separate avoidable gaps from unavoidable gaps.
2. Avoidable gaps include wrong paper type, missing output object, weak narrative bridges, generic method paragraph, and lack of domain-specific consequence.
3. Unavoidable gaps may come from the user's omit-results requirement: published Introductions often include contributions, dataset size, performance, or validation results that the target draft should intentionally omit.
4. Score the draft against its allowed scope, but record how much of the gap is caused by omitted result/contribution material.

## Five-Article Lessons

- OpenScholar/RAG: weak drafts overuse generic LLM/RAG language and underweight citation correctness, coverage, transparency, and expert evaluation.
- ReactionSeek: weak drafts mention organic synthesis broadly but fail to bind reaction roles, image/text evidence, and conditions into a reaction record.
- Phosphor emission prediction: weak drafts name emission wavelengths but do not make host-dopant-emission binding the core scientific relation.
- Materials system charts: weak drafts flatten P-M-S-M-P charts into ordinary databases and lose mechanism direction/source labels.
- Design hypothesis generation: weak drafts treat the task as extraction, while the benchmark requires defining valuable hypotheses, synergy, and scientific grounding.
