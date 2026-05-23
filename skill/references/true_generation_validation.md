# True Generation Validation

Use this file only when developing, benchmarking, or improving this skill against existing papers. Ordinary user drafting does not need this file unless the user explicitly asks whether the skill really works.

## Purpose

A benchmark comparison is not a true generation test unless the skill actually writes an Introduction from realistic input. Gap analysis, rubric tables, and rhetorical diagnosis are useful, but they cannot prove that the writing workflow works.

The required loop is:

`source article evidence -> 领域/困难 input card -> generated Introduction -> usability judgment from the generated text -> skill update -> regenerate if needed`

## Required Input Card

Before generating a benchmark Introduction, compress the source article into this user-facing card. Keep it short enough that it resembles what a real user might provide.

| Field | Required content |
|---|---|
| `领域` | The scientific or material domain, not just "text mining". |
| `困难` | The concrete information-structure difficulty in the field. |
| Paper type | Extraction/database, RAG/literature synthesis, relation prediction, system chart/knowledge graph, or hypothesis generation. |
| Output object | The object the paper must recover: record, relation, answer, graph, chart, or hypothesis. |
| Evidence locations | Where the needed evidence appears: text, tables, figures, captions, supplements, procedures, retrieved passages, expert annotations. |
| Mis-binding or misuse consequence | What scientific conclusion, prediction, answer, graph edge, or hypothesis becomes wrong. |
| Method direction | The constrained method direction that follows from the difficulty. |
| Omit-results boundary | Which dataset sizes, performance values, case-study results, or contribution claims should not be written. |

## Generation Requirement

Generate a real Chinese omit-results Introduction from the card. Do not write only:

- a gap table;
- a reverse outline;
- a list of lessons;
- a benchmark score;
- a paragraph-by-paragraph comparison.

The generated draft should be long enough to expose writing failures. A very short draft cannot test narrative continuity, paragraph load, or method inevitability.

## Usability Judgment

Judge the generated text itself:

- `usable`: the draft has the right paper type, output object, narrative chain, field-specific consequence, and method necessity. It may still need citations and local polishing.
- `partially usable`: the draft has the right direction but lacks domain texture, case-level examples, or top-journal pressure.
- `not usable`: the draft misclassifies the paper type, becomes generic, stacks facts without logic, or cannot support the claimed method need.

Tie every judgment to visible text behavior, such as:

- the opening object is wrong or late;
- paragraphs can be swapped without loss;
- the material-specific paragraph could be reused after replacing the domain name;
- the final method paragraph is generic;
- RAG papers omit citation correctness or coverage;
- hypothesis papers omit synergy and scientific grounding;
- system-chart papers flatten graphs into databases.

## Skill Update Rule

When a generated draft is weaker than the benchmark, update the smallest reusable rule that would prevent the same failure:

- wrong paper type -> update `paper_type_routing.md` or the routing step in `SKILL.md`;
- weak `领域/困难` extraction -> update this file and the domain evidence card rule;
- abstract but correct draft -> update `material_domain_problem_patterns.md` or `practice_iteration_lessons.md`;
- stacked prose -> update `narrative_coherence.md`;
- method paragraph generic -> update `nature_intro_blueprint.md` or `paper_type_routing.md`;
- repeated underlength drafts -> update `quality_control_iteration.md`.

After the update, regenerate at least the weakest failed case or state the missing source evidence that blocks a stronger generation.

## Five-Article Validation Lessons

The 2026-05-23 real generation round showed:

- RAG/literature-synthesis drafts become usable only when the input card foregrounds citation correctness, coverage, transparency, and expert verification.
- Reaction extraction drafts are strong when the card names role-condition-yield-structure binding and text-image evidence.
- Relation-prediction drafts are strong when the card names the relation as the prediction object, such as `host-dopant-emission relationship`.
- System-chart drafts are strong when the card names graph/chart semantics, edge direction, mechanism-vs-observation distinction, and source labels.
- Hypothesis-generation drafts remain too abstract unless the card includes concrete mechanism synergy, scientific grounding, and domain case details.

Therefore, in future validation, do not accept "领域: X; 困难: 文献非结构化" as enough input. The card must expose the scientific object, evidence locations, and consequence of wrong binding.
