# Benchmark Iteration Protocol

Use this file only when improving this skill against existing high-quality articles. Do not load it for ordinary user drafting unless the user explicitly asks to iterate the skill itself.

## Purpose

High-impact articles are used as a development benchmark for the skill, not as a user-facing evaluation feature. The loop is:

1. Select high-quality existing Introduction sections in related domains.
2. Use the current skill to generate a Chinese Introduction from the same problem logic.
3. Compare the generated draft with the original article's rhetorical logic, framework, paragraph pacing, specificity, and language charm.
4. If the generated draft is weaker, update the reusable writing requirements in the skill references.
5. Regenerate and compare again.
6. Stop when the generated draft can reproduce the high-quality article's level of problem pressure, detail allocation, and prose force without copying its text.

## Benchmark Selection

Prefer articles that meet at least two conditions:

- Published in Nature, Nature Communications, npj Computational Materials, Acta Materialia, Scripta Materialia, or another field-leading venue.
- The article is about materials discovery, scientific literature mining, LLM/RAG extraction, structured materials knowledge, or a close analogue.
- The Introduction or lead section is available with enough clean prose for paragraph analysis.
- The article's domain is close enough to the target material to transfer rhetorical pressure.

If local extraction contains abstract, author information, figures, tables, or results, isolate the functional Introduction logic before comparison.

## Local Benchmark Pool

| Key | Article | Venue | Use |
|---|---|---|---|
| `S3LTWBGE` | Synthesizing scientific literature with retrieval-augmented language models | Nature | RAG, citation reliability, scientific synthesis pressure. |
| `UAL253B7` | ReactionSeek: LLM-powered literature data mining and knowledge discovery in organic synthesis | Nature Communications | Multimodal literature mining and data curation bottleneck. |
| `58Z3MKQN` | Text mining-assisted machine learning prediction and experimental validation of emission wavelengths | npj Computational Materials | Materials-specific text mining and host-dopant-property binding. |
| `PSZJCRRQ` | Beyond designer's knowledge: generating materials design hypotheses via a large language model | Acta Materialia | Materials design hypotheses and beyond-expert-prior framing. |
| `F9NLVIKW` | Automated extraction of materials system charts using a large language model framework | Scripta Materialia | Processing-microstructure-mechanism-property extraction. |

## What To Compare

Compare drafts qualitatively:

- Does the opening create a real material/scientific need before naming the method?
- Does the draft define the real data object, such as sample-level relationships, reaction records, literature synthesis answers, or system charts?
- Does it explain why prior routes fail for a technical reason?
- Does the material-specific paragraph show what scientific conclusion becomes wrong if fields are mis-bound?
- Does the method paragraph justify schema/RAG/LLM through evidence, context, and auditability?
- Does paragraph length follow argumentative need rather than five equal blocks?
- Does the Chinese prose have pressure, rhythm, and exact nouns instead of generic slogans?

## How To Update The Skill

When a benchmark comparison exposes a weakness, update the smallest reusable rule that would prevent the same weakness later:

- If drafts are too generic, update `material_domain_problem_patterns.md`.
- If drafts are structurally correct but thin, update `practice_iteration_lessons.md`.
- If drafts have poor paragraph pacing, update `intro_structure_benchmarks.md`.
- If drafts sound method-first, update `nature_intro_blueprint.md`.
- If drafts lack cross-domain problem language, update `common_text_mining_problems.md`.
- If drafts lack writing flow, update `research_writing_skill_synthesis.md`.

Do not add tables, numerical rubrics, or scripts for evaluation to the ordinary skill workflow.
