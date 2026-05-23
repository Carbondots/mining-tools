# Five-Article Benchmark Gap Analysis

## Purpose

This round stress-tests the `text-mining-intro-writing` skill against five existing high-impact or high-relevance text-mining papers. The goal is not to reproduce their result/contribution paragraphs. The user usually wants an omit-results Introduction, so the comparison separates:

- **avoidable writing gaps**: wrong paper type, weak pressure chain, generic method paragraph, missing output object, weak narrative bridges;
- **scope gaps**: published papers include dataset size, performance, validation, or contributions that the target omit-results draft should not include unless the user asks.

Scores are approximate development scores used to iterate the skill.

## Five Articles

| ID | Paper | Type | Benchmark target |
|---|---|---|---|
| S3LTWBGE | Synthesizing scientific literature with retrieval-augmented language models | RAG / literature synthesis | citation-grounded synthesis; coverage; transparency; expert evaluation |
| UAL253B7 | ReactionSeek: LLM-powered literature data mining and knowledge discovery in organic synthesis | extraction/database | reaction record; roles; conditions; text-image alignment |
| 58Z3MKQN | Text mining-assisted machine learning prediction and experimental validation of emission wavelengths | relation prediction | host-dopant-emission binding; prediction meaning; experimental validation context |
| F9NLVIKW | Automated extraction of materials system charts using a large language model framework | system chart / mechanism graph | P-M-S-M-P chart; mechanism direction; source labels |
| PSZJCRRQ | Beyond designer's knowledge: generating materials design hypotheses via a large language model | hypothesis generation | scientific hypothesis value; synergy; grounding; mechanism interaction |

## Gap Scores

| Paper | Benchmark level | Current skill V1 estimate | Gap | Main avoidable gaps | Scope gap from omit-results |
|---|---:|---:|---:|---|---|
| S3LTWBGE | 90 | 81 | 9 | The skill tends to force a materials-extraction story and underweights citation correctness, coverage, transparency, expert evaluation, and long-form synthesis quality. | 3-4 points: full paper reports benchmark/dataset/evaluation details that omit-results mode should not claim. |
| UAL253B7 | 89 | 85 | 4 | Reaction object is mostly captured, but text-image alignment and molecular role switching need to appear earlier and more causally. | 2-3 points: full paper includes Organic Syntheses-scale validation and high precision/recall. |
| 58Z3MKQN | 88 | 86 | 2 | Strong fit after prior iterations; remaining gap is richer phosphor-specific evidence and experimental validation context. | 2 points: omit-results mode intentionally avoids prediction R2/F1 and experimental success claims. |
| F9NLVIKW | 88 | 84 | 4 | Skill captures P-M-S-M-P but can still flatten charts into databases; source labels, edge direction, and mechanism-vs-observation distinction need stronger rules. | 2-3 points: published article reports extraction accuracy and readability indices. |
| PSZJCRRQ | 87 | 78 | 9 | Biggest mismatch: current skill may treat the paper as extraction/database instead of hypothesis generation; it underdefines valuable hypothesis, synergy, and scientific grounding. | 3 points: full paper includes model evaluation and case study results. |

## Cross-Article Diagnosis

### 1. Paper Type Is A First-Order Choice

The old default pressure chain works well for extraction/database papers and relation-prediction papers, but it is too narrow for RAG synthesis and hypothesis generation. OpenScholar needs a synthesis/citation-verification chain; design-hypothesis papers need a hypothesis-quality chain.

### 2. Output Object Must Match The Paper Type

Different papers require different opening objects:

- S3LTWBGE: citation-grounded long-form answer / evidence-linked synthesis.
- UAL253B7: reaction record.
- 58Z3MKQN: host-dopant-emission relationship.
- F9NLVIKW: P-M-S-M-P system chart.
- PSZJCRRQ: scientifically grounded design hypothesis.

If the output object is wrong, later paragraph polishing cannot fully repair the Introduction.

### 3. Method Necessity Must Be Type-Specific

Generic "schema + evidence + uncertainty" is not enough:

- RAG synthesis needs retrieval, self-feedback, citation verification, coverage, transparency, and expert evaluation.
- Reaction extraction needs text-image alignment and role/condition binding.
- Relation prediction needs relation context and downstream prediction meaning.
- System charts need node/edge types, edge direction, source labels, and mechanism uncertainty.
- Hypothesis generation needs synergy, grounding, and expert/auditable evaluation.

### 4. Narrative Coherence Is Necessary But Not Sufficient

The previous iteration improved paragraph lead-ins and sentence-function chains. This round shows that coherence can still connect the wrong story if the paper type is misclassified. Therefore routing must happen before narrative spine generation.

## Skill Iterations Made From This Round

1. Added `references/paper_type_routing.md`.
2. Updated `SKILL.md` to identify paper type before user-structure mapping, domain evidence card, reverse outline, and narrative spine.
3. Added type-specific load-bearing triads:
   - extraction/database: `field object -> evidence manifestation -> binding consequence`;
   - RAG/literature synthesis: `scientific synthesis need -> citation/coverage risk -> verification necessity`;
   - relation prediction: `scientific relation -> extraction binding -> downstream prediction consequence`;
   - system chart/knowledge graph: `mechanism relation -> graph/chart representation -> source/direction consequence`;
   - hypothesis generation: `design need -> mechanism synergy -> grounding/evaluation consequence`.
4. Added `Paper-type fit` to the quality rubric.
5. Added hard gates for RAG, hypothesis-generation, and system-chart papers.

## New Acceptance Standard

A generated Introduction should not pass only because it is coherent, specific, and long enough. It should pass only if it tells the correct type of story for the paper:

- synthesis story for RAG;
- record story for extraction;
- relation story for prediction;
- mechanism graph story for system charts;
- hypothesis quality story for design generation.
