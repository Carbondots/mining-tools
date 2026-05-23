# Intro Structure Benchmarks

Use this file when deciding how long each part of a materials text-mining Introduction should be and how much emphasis each part deserves.

## Evidence Base

The benchmark comes from the local 36-paper Introduction extraction and structure reports in:

`G:\paper\文献数据挖掘\文献调研\codex\codex_整理归档\最终成果`

Quantitative extraction table:

- Papers: 36.
- Explicit Introduction or Background/Summary headings: 27.
- Inferred lead sections: 9.
- Mean extracted Introduction length: 6,477 characters.
- Median: 6,443 characters.
- Interquartile range: 5,840 to 7,229 characters.
- Minimum/maximum: 1,752 to 10,092 characters.

Reusable evidence distribution in the theme table:

| Theme | Evidence Items | Share |
|---|---:|---:|
| Materials/domain status and why text mining is needed | 267 | 33.6% |
| What text mining does and how it is introduced | 218 | 27.4% |
| LLM-prompt advantages | 156 | 19.6% |
| NER limits and need for LLM-prompt | 154 | 19.4% |

Interpretation: the strongest introductions spend roughly 60% of reusable argumentative space on domain/data/literature context before turning to method contrast. They do not rush into LLMs.

## High-Impact Benchmark Allocation

Use genuine benchmark articles to adjust the default structure:

| Benchmark Pattern | Typical Allocation | Lesson |
|---|---|---|
| Nature/Nature Communications lead article | Short, forceful opening; early bottleneck; contribution appears after pressure is established. | Use clear problem pressure before method detail. |
| npj Computational Materials article | Domain importance and material-specific complexity receive more space. | Do not compress material science into a one-sentence preface. |
| Acta/Scripta Materialia article | Materials design logic and mechanism chains receive long paragraphs. | Explain why the scientific relation, not only the text format, makes extraction difficult. |
| LLM/RAG method article | Benchmarking, transparency, and citation/evidence reliability shape the final turn. | Justify method through verification and traceability, not novelty slogans. |

## Dominant Tension Rule

Before drafting, choose the paragraph that should carry the dominant tension:

- If the field is a material-specific extraction task, P4 should be the heaviest paragraph.
- If the field is a data-acquisition bottleneck, P3 should be the heaviest paragraph.
- If the field is a new knowledge object, P2 and P3 should jointly define that object before method justification.
- If the field is a hypothesis-generation task, P1 and P4 should define what counts as a valuable hypothesis.

Do not make five equal paragraphs. High-quality Introductions usually create one visibly load-bearing paragraph where the unresolved challenge becomes concrete.

## Default Chinese Target Length

For a Chinese Nature-style Introduction that excludes the final results/contribution paragraph, target 1,800 to 2,400 Chinese characters across five paragraphs.

If the user later asks for a full conventional Introduction including current-paper achievements, add a sixth paragraph of about 250 to 400 Chinese characters.

## Minimum Load Gate

Do not accept a five-paragraph draft as a full Introduction if it is only a strong outline.

Minimum practical floor for omit-results mode:

- Total Chinese body: at least 1,500 Chinese characters.
- P1-P4: usually at least 250 Chinese characters each.
- P5: usually at least 220 Chinese characters.
- At least two paragraphs should contain 4-6 sentences with concrete evidence locations, technical reasons, or mis-binding consequences.

If a draft fails this gate, expand before polishing style. Add mechanisms, examples, evidence locations, and consequences rather than repeating generic importance claims.

## Five-Part Allocation

| Part | Role | Target Share | Chinese Length |
|---|---|---:|---:|
| P1 | Material domain importance and data-driven need | 18-22% | 330-500 chars |
| P2 | Literature as unstructured but valuable data source | 18-24% | 350-550 chars |
| P3 | Existing routes and common bottlenecks | 22-28% | 420-650 chars |
| P4 | Material-specific extraction difficulty | 20-26% | 420-650 chars |
| P5 | Why LLM-prompt/RAG/schema extraction is necessary | 12-18% | 280-430 chars |
| P6 optional | Current paper results/contributions | 8-12% | 250-400 chars |

## Detail Pattern Learned From The Extracted Intros

Use detailed explanation for:

- The material system's scientific complexity.
- The data object that must be recovered from literature.
- The exact output object and why it must appear early.
- Why simple entity extraction is insufficient.
- The evidence-preserving requirement: source text, citation, field binding, uncertainty.
- The technical reason prior routes fail, not only a list of failed routes.

Use concise explanation for:

- Generic AI/ML background.
- Generic "literature grows fast" statements.
- Generic LLM capability claims.
- Lists of prior tools.

## Paragraph-Level Checks

Each paragraph must answer one question:

1. Why does this material field need data-driven organization?
2. Why are papers the critical but difficult data source?
3. Why do existing databases/manual/rule/NER/BERT routes not solve this problem?
4. What is special about this material's text and evidence chain?
5. What method family is therefore justified, before claiming current-paper results?

If two adjacent paragraphs answer the same question, merge or sharpen them.
