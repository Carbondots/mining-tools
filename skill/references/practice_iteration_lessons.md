# Practice Iteration Lessons

Load this file when a generated Introduction has the right structure but still does not feel like a top-journal research Introduction.

## Correction To The Earlier Stress Test

An earlier stress test used generated domains and a quantitative script. That test is useful only as a warning about thin drafts. It is not evidence that a carbon-dot or other target-domain Introduction is genuinely strong, because no real target-domain source or high-quality in-domain benchmark had been provided.

New rule:

- Use published high-impact Introductions as development benchmarks when improving the skill.
- Do not expose numerical rubrics or script outputs in normal user-facing skill results.
- During skill development, compare a generated draft with existing high-quality articles; if the draft is weaker, update the writing requirements and regenerate.

## Repeated Failure Pattern

The common failure is "thin completeness": five paragraphs each fulfill a formal role, but the body still reads like an outline or proposal abstract.

Symptoms:

- one sentence for domain importance,
- one sentence for literature difficulty,
- one sentence for existing methods,
- one sentence for material specificity,
- one sentence for LLM-prompt necessity,
- little pressure escalation between paragraphs.

## Top-Journal Density Rule

For every load-bearing paragraph, include the triad:

1. Scientific mechanism: why the material problem is inherently coupled.
2. Text/evidence manifestation: where the coupled information appears in papers.
3. Extraction consequence: what goes wrong if the fields are separated or mis-bound.

Example transformations:

- Thin: `NER cannot bind precursor, condition, and property.`
- Stronger: `A temperature value may denote hydrothermal synthesis, carbonization, annealing, or testing; without the step role and sample identity, the same number can be assigned to the wrong precursor-property record.`

- Thin: `MOF SSE data are scattered across papers.`
- Stronger: `A conductivity value can describe a pristine framework, a polymer composite, a humidity-conditioned pellet, or a full-cell interface; each interpretation changes whether the material should be prioritized as a solid electrolyte.`

- Thin: `Phosphor extraction requires host-dopant relations.`
- Stronger: `An emission peak is comparable only when bound to host lattice, activator valence, dopant concentration, excitation wavelength, and measurement condition; otherwise the database may teach a model false structure-property relations.`

## Benchmark Lessons From The High-Impact Pass

- Nature-style leads are compressed but not vague: the opening names the scientific need and the data bottleneck quickly.
- npj Computational Materials-style materials papers spend real space on the material relation chain before claiming a pipeline.
- Acta/Scripta Materialia examples treat mechanisms and design logic as first-class objects; the extraction task should preserve those objects, not flatten them into values.
- RAG/LLM benchmarks justify method through citation correctness, coverage, transparency, and expert evaluation rather than through generic LLM capability.

## Cross-Domain Gap Detection

After generating drafts for multiple domains, check:

- If all drafts are structurally correct but under 1,500 Chinese characters, tighten length gates and expand evidence-consequence sentences.
- If all drafts use the same LLM paragraph, add domain-specific method-object wording.
- If all drafts mention "unstructured literature" without examples of text/table/figure evidence, expand P2.
- If all drafts mention NER but not relation binding, expand P3/P4.
- If all drafts could swap material names with little change, rewrite P4 from the material problem bank.
- If all drafts have equal paragraph lengths and repeated transitions, vary pacing according to the benchmark.

## Domain-Specific Expansion Moves

Use these when a draft is short:

- Carbon dots: add sample aliasing, precursor diversity, surface-state ambiguity, excitation/QY binding, and unknown-value refusal.
- MOF SSE: add candidate-space vs tested-space gap, pristine/composite distinction, temperature/humidity/testing-state labels, and screening consequence.
- Phosphors: add host lattice, activator valence, excitation-emission pair, dopant concentration series, and quantum-efficiency test mode.
- Alloys/catalysts: add process sequence, action-role labels, heat treatment or solvent-addition order, and processing-structure-property consequences.
- Nanomaterials: add paragraph classification, synthesis vs characterization separation, image/table evidence, and morphology/size mis-assignment risk.

## Acceptance Standard For Drafting

Accept the draft only when:

- The Chinese body is at least 1,500 characters for a short Nature-style omit-results Introduction, preferably 1,800-2,400.
- P1-P4 each carry enough mechanism/evidence/consequence detail to function as paragraphs, not outline bullets.
- There is no current-paper result language if omission was requested.
- The material-specific paragraph explains a concrete wrong scientific conclusion caused by extraction failure.
- The method paragraph states what the LLM must not infer when evidence is absent.
- The argument has the same kind of problem pressure and detail allocation seen in high-quality benchmark articles.
