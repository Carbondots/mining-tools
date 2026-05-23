---
name: text-mining-intro-writing
description: Draft, revise, quality-check, score approximately, and iteratively improve Nature-style Chinese Introduction sections for materials text-data-mining papers. Use when the user provides a material-domain review, field-specific extraction difficulties, a proposed text-mining/LLM-prompt/RAG/NER/database method, a preferred writing structure, or asks to write, optimize, polish, evaluate, or compare an introduction for materials literature mining, NLP information extraction, knowledge graph, or LLM-prompt papers.
---

# Text Mining Intro Writing

## Overview

Use this skill to turn a material-domain review plus a text-mining difficulty summary into a high-density Chinese Introduction for a Nature-family manuscript. The default output excludes the final conventional paragraph that reports the current paper's concrete results unless the user explicitly asks for it.

The skill's job is writing plus quality control: structure, narrative coherence, paragraph lead-ins, sentence-to-sentence logic, rhetorical pressure, material specificity, evidence discipline, Chinese academic prose, approximate evaluation, and targeted regeneration when the draft is not good enough.

## Core Workflow

1. Intake the material domain, target journal family, manuscript type, proposed method, field-specific extraction difficulties, available review notes, citation material, and any user-provided writing structure.
2. Load only the needed references:
   - `references/intro_structure_benchmarks.md` for paragraph length and emphasis allocation.
   - `references/research_writing_skill_synthesis.md` when polishing paragraph logic, reviewer-facing clarity, or prose quality.
   - `references/common_text_mining_problems.md` for cross-domain transferable problem language.
   - `references/material_domain_problem_patterns.md` for field-specific lead-in and problem discovery.
   - `references/paper_type_routing.md` before drafting or benchmarking to identify whether the manuscript is an extraction/database, RAG/literature-synthesis, relation-prediction, system-chart/knowledge-graph, or hypothesis-generation paper.
   - `references/nature_intro_blueprint.md` for drafting the Chinese Introduction.
   - `references/narrative_coherence.md` for paragraph lead-ins, sentence-to-sentence logic, transitions, and anti-stacking revision.
   - `references/quality_control_iteration.md` for approximate scoring, hard gates, and regeneration.
   - `references/practice_iteration_lessons.md` when a generated draft has the right structure but still feels unlike a top-journal Introduction.
   - `references/benchmark_iteration_protocol.md` only when explicitly improving this skill against existing high-quality articles, not for ordinary drafting.
   - `references/true_generation_validation.md` when testing or improving the skill against real papers; use it to force the loop `source evidence -> domain/difficulty input card -> generated Introduction -> usability judgment -> skill update`.
3. Identify the paper type before deciding the pressure chain:
   - extraction/database;
   - RAG/literature synthesis;
   - relation prediction and validation;
   - system chart or knowledge graph;
   - hypothesis generation.
   Use `references/paper_type_routing.md` to adapt the output object, bottleneck, and method-necessity paragraph. Do not turn every paper into a generic structured-database story.
4. Identify whether the user supplied a preferred writing structure:
   - If yes, preserve the user's section order, paragraph roles, and emphasis unless it conflicts with evidence discipline or the omit-results rule.
   - Convert the user's structure into the reverse outline, narrative spine, and quality-control criteria.
   - Do not force the default five-part structure onto a user-provided framework.
   - If the user's structure is incomplete, keep its order but fill missing logic links with the smallest necessary additions.
5. Build a domain evidence card before the reverse outline:
   - paper type and secondary type, if any;
   - output object: what structured record, synthesis, relation, graph, chart, or hypothesis the paper must recover;
   - core relation: the scientific relation that must be preserved;
   - evidence locations: text, tables, figures, captions, supplements, or procedures;
   - mis-binding or misuse consequence: what scientific conclusion becomes wrong;
   - prior-route bottleneck: why manual/database/rule/NER/domain-model routes leave the challenge unresolved;
   - method object: the exact schema/RAG/LLM output object, not a generic "structured database".
6. When developing or benchmarking the skill against existing papers, first compress the source article into a realistic user-facing domain/difficulty input card:
   - `领域`;
   - `困难`;
   - paper type;
   - output object;
   - evidence locations;
   - mis-binding or misuse consequence;
   - method direction;
   - result/contribution claims that must not be written in omit-results mode.
   Then draft only from this card plus allowed source notes. Do not treat a gap table or rhetorical diagnosis as a true generation test.
7. Build a reverse outline before drafting: paragraph role, target length, main claim, required evidence, and transition into the next paragraph.
8. Build a narrative spine before drafting:
   - one controlling question for the whole Introduction;
   - one causal or contrastive bridge between each pair of paragraphs;
   - one sentence-function chain for each paragraph, such as `claim -> reason -> evidence manifestation -> consequence -> next-step bridge`.
9. Draft in Chinese with explicit evidence discipline. Every major factual or trend claim needs a citation marker, source note, or clearly marked `需补文献`.
10. Check whether the draft is merely a skeleton. For the default omit-results Introduction, the Chinese body should normally be 1,800-2,400 Chinese characters; anything below 1,500 characters must be expanded before polishing. As a practical floor, load-bearing paragraphs should usually each carry at least 250 Chinese characters.
11. Revise for top-journal density and continuity: every load-bearing paragraph should contain the type-appropriate triad:
   - extraction/database: `field object -> evidence manifestation -> binding consequence`;
   - RAG/literature synthesis: `scientific synthesis need -> citation/coverage risk -> verification necessity`;
   - relation prediction: `scientific relation -> extraction binding -> downstream prediction consequence`;
   - system chart/knowledge graph: `mechanism relation -> graph/chart representation -> source/direction consequence`;
   - hypothesis generation: `design need -> mechanism synergy -> grounding/evaluation consequence`.
   Every sentence should either answer the previous sentence or make the next sentence necessary.
12. Run the coherence audit in `references/narrative_coherence.md`. If paragraphs read as stacked facts, rebuild the paragraph lead-ins and transitions before scoring.
13. Evaluate the draft with `references/quality_control_iteration.md`. If the approximate score is below 85 or any hard gate fails, revise the weakest paragraphs and evaluate again.
14. Stop before result/contribution claims when the user asks to omit current-paper results.
15. In benchmark/development mode, do not mark the iteration successful until at least one actual Introduction has been generated from a `领域/困难` card and judged usable or not usable from the generated text itself.

## Writing Contract

Use the user's supplied structure when available. Treat the default five-part structure as a fallback, not a fixed requirement.

Default fallback:

1. Material domain importance and data-driven need.
2. Literature as the key but unstructured data source.
3. Limits of manual curation, databases, rules, NER, or small domain models.
4. The material-specific difficulty that makes this field harder than a generic extraction task.
5. Why evidence-preserving LLM-prompt/RAG/schema-based extraction is necessary.

Do not open with "LLM has developed rapidly" unless the user asks for a method-first review. For a Nature-style research Introduction, start from the scientific/material problem, reveal literature data as the bottleneck, and make the method feel like the consequence of that bottleneck.

When the user provides a custom framework, preserve its intended rhetoric, such as:

- application-first;
- controversy/gap-first;
- benchmark-comparison-first;
- mechanism-first;
- database/resource-first;
- method-paper-first.

Only adjust the structure when a paragraph order creates unsupported claims, result leakage, or an unclear problem-to-method chain.

## Hard Rules

1. Do not invent references, numbers, database sizes, performance values, or "first" claims.
2. Do not write only generic problems such as "literature is unstructured" or "manual extraction is slow"; always connect them to the chosen material's entities, properties, process variables, and sample-level relationships.
3. Name the real output object by the opening paragraph's second sentence. Examples: `host-dopant-emission relationship`, `reaction record`, `P-M-S-M-P system chart`, `sample-level carbon-dot record`, `citation-grounded long-form answer`, `scientifically grounded design hypothesis`.
4. If the user supplied a structure, do not overwrite it with the default five-part structure; improve it from inside its own logic.
5. Do not use the wrong paper type. A RAG/literature-synthesis paper must foreground citation correctness and synthesis coverage; a hypothesis-generation paper must foreground hypothesis quality, synergy, and grounding; a system-chart paper must foreground graph/chart semantics and source labels.
6. Do not make the paper look like a minor patch to a naive baseline. Frame the unresolved challenge around the root information-structure problem.
7. Keep terminology stable: choose one name for the material system, one name for the proposed method, and one schema vocabulary.
8. Write prior routes as a pressure chain, not a survey list: `route -> useful part -> technical reason it fails -> unresolved challenge`.
9. Make the final method paragraph type-specific and domain-specific. It must name the exact output object and the appropriate verification/refusal behavior, not only "schema + evidence + uncertainty".
10. If the user asks to omit current-paper results, stop before claims like "本文提出", "我们构建", "实验结果表明", "precision/recall", or "主要贡献如下".
11. Do not accept a draft that only names its paragraph roles. Expand load-bearing paragraphs with the type-appropriate mechanism/evidence/consequence triad.
12. Do not accept a draft whose sentences can be freely reordered without changing meaning. That means the prose is a list, not an argument.
13. Do not accept paragraphs that begin independently with repeated openers such as "此外", "同时", "另一方面" unless they explain a real causal, contrastive, or narrowing relation.
14. If quality is below 85, do not present the first draft as final. Regenerate or revise using the two weakest dimensions from the quality-control table.
15. After two revision passes, if the Introduction still cannot reach a strong level, state the missing evidence or domain information that blocks further improvement.
16. In benchmark/development mode, do not call a comparison complete unless the skill has actually generated an Introduction from a compressed `领域/困难` card and the generated text itself has been checked for usability.

## Output Contract

For full drafting tasks, return:

1. A compact reverse outline table.
2. A brief narrative spine showing how the paragraphs lead into each other.
3. The final Chinese Introduction after any needed revision.
4. A claim-evidence map listing each main claim and its source status.
5. A brief domain evidence card.
6. A quality-control table with approximate score, weakest dimensions, coherence fixes applied, revision actions applied, and remaining evidence gaps.

For revision tasks, return:

1. The main diagnosis.
2. The revised paragraphs only, unless the user asks for a full rewrite.
3. Approximate before/after quality judgment and a brief explanation of what changed and why.
