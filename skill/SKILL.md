---
name: text-mining-intro-writing
description: Draft and revise Nature-style Chinese Introduction sections for materials text-data-mining papers. Use when the user provides a material-domain review, field-specific extraction difficulties, a proposed text-mining/LLM-prompt/RAG/NER/database method, or asks to write, optimize, polish, or compare an introduction for materials literature mining, NLP information extraction, knowledge graph, or LLM-prompt papers.
---

# Text Mining Intro Writing

## Overview

Use this skill to turn a material-domain review plus a text-mining difficulty summary into a high-density Chinese Introduction for a Nature-family manuscript. The default output excludes the final conventional paragraph that reports the current paper's concrete results unless the user explicitly asks for it.

The skill's job is writing: structure, rhetorical logic, paragraph pacing, material specificity, evidence discipline, and Chinese academic prose.

## Core Workflow

1. Intake the material domain, target journal family, manuscript type, proposed method, field-specific extraction difficulties, available review notes, and citation material.
2. Load only the needed references:
   - `references/intro_structure_benchmarks.md` for paragraph length and emphasis allocation.
   - `references/research_writing_skill_synthesis.md` when polishing paragraph logic, reviewer-facing clarity, or prose quality.
   - `references/common_text_mining_problems.md` for cross-domain transferable problem language.
   - `references/material_domain_problem_patterns.md` for field-specific lead-in and problem discovery.
   - `references/nature_intro_blueprint.md` for drafting the Chinese Introduction.
   - `references/practice_iteration_lessons.md` when a generated draft has the right structure but still feels unlike a top-journal Introduction.
   - `references/benchmark_iteration_protocol.md` only when explicitly improving this skill against existing high-quality articles, not for ordinary drafting.
3. Build a domain evidence card before the reverse outline:
   - output object: what structured record the paper must recover;
   - core relation: the scientific relation that must be preserved;
   - evidence locations: text, tables, figures, captions, supplements, or procedures;
   - mis-binding consequence: what scientific conclusion becomes wrong;
   - prior-route bottleneck: why manual/database/rule/NER/domain-model routes leave the challenge unresolved;
   - method object: the exact schema/RAG/LLM output object, not a generic "structured database".
4. Build a reverse outline before drafting: paragraph role, target length, main claim, required evidence, and transition into the next paragraph.
5. Draft in Chinese with explicit evidence discipline. Every major factual or trend claim needs a citation marker, source note, or clearly marked `需补文献`.
6. Check whether the draft is merely a skeleton. For the default omit-results Introduction, the Chinese body should normally be 1,800-2,400 Chinese characters; anything below 1,500 characters must be expanded before polishing. As a practical floor, P1-P4 should usually each carry at least 250 Chinese characters and P5 at least 220 Chinese characters.
7. Revise for top-journal density: every load-bearing paragraph should contain `scientific mechanism -> text/evidence manifestation -> extraction consequence`.
8. Stop before result/contribution claims when the user asks to omit current-paper results.

## Writing Contract

Use a five-part structure by default:

1. Material domain importance and data-driven need.
2. Literature as the key but unstructured data source.
3. Limits of manual curation, databases, rules, NER, or small domain models.
4. The material-specific difficulty that makes this field harder than a generic extraction task.
5. Why evidence-preserving LLM-prompt/RAG/schema-based extraction is necessary.

Do not open with "LLM has developed rapidly" unless the user asks for a method-first review. For a Nature-style research Introduction, start from the scientific/material problem, reveal literature data as the bottleneck, and make the method feel like the consequence of that bottleneck.

## Hard Rules

1. Do not invent references, numbers, database sizes, performance values, or "first" claims.
2. Do not write only generic problems such as "literature is unstructured" or "manual extraction is slow"; always connect them to the chosen material's entities, properties, process variables, and sample-level relationships.
3. Name the real output object by the opening paragraph's second sentence. Examples: `host-dopant-emission relationship`, `reaction record`, `P-M-S-M-P system chart`, `sample-level carbon-dot record`.
4. Do not make the paper look like a minor patch to a naive baseline. Frame the unresolved challenge around the root information-structure problem.
5. Keep terminology stable: choose one name for the material system, one name for the proposed method, and one schema vocabulary.
6. Write prior routes as a pressure chain, not a survey list: `route -> useful part -> technical reason it fails -> unresolved challenge`.
7. Make the final method paragraph domain-specific. It must name the exact output object and refusal behavior, not only "schema + evidence + uncertainty".
8. If the user asks to omit current-paper results, stop before claims like "本文提出", "我们构建", "实验结果表明", "precision/recall", or "主要贡献如下".
9. Do not accept a five-paragraph draft that only names the five roles. Expand load-bearing paragraphs with `scientific mechanism -> text/evidence manifestation -> extraction consequence`.
10. If quality still feels weak, revise the writing directly and explain the main revision priorities in prose.

## Output Contract

For full drafting tasks, return:

1. A compact reverse outline table.
2. The Chinese Introduction draft.
3. A claim-evidence map listing each main claim and its source status.
4. A brief domain evidence card and the highest-priority revision suggestions in prose.

For revision tasks, return:

1. The main diagnosis.
2. The revised paragraphs only, unless the user asks for a full rewrite.
3. A brief explanation of what changed and why.
