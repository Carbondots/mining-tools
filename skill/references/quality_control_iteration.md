# Quality Control And Iterative Revision

Use this file in normal drafting and revision tasks. It provides an approximate quality-control loop for deciding whether a generated Introduction is strong enough or needs another rewrite.

## Purpose

The score is a writing-control tool, not a rigid automated metric. Use it to identify weak dimensions, revise the draft, and then re-evaluate. Do not let a draft pass simply because it has the right section labels.

## Approximate Quality Rubric

Score out of 100:

| Dimension | Points | What To Check |
|---|---:|---|
| Problem trajectory | 12 | The argument moves from material/scientific need to literature bottleneck to method necessity; each paragraph makes the next one necessary. |
| Narrative coherence | 15 | Paragraph lead-ins, final sentences, and sentence-to-sentence transitions form a causal/contrastive chain rather than a stack of related facts. |
| User-structure fidelity | 8 | If the user supplied a writing framework, the draft preserves its order, intent, and emphasis while repairing weak logic links. If no user structure was supplied, award these points for a coherent default structure. |
| Domain evidence card completeness | 8 | Output object, core relation, evidence locations, mis-binding consequence, prior-route bottleneck, and method object are all explicit. |
| Material/task specificity | 12 | The draft names the target material's variables, relations, evidence types, and wrong scientific conclusion caused by mis-binding. |
| Prior-route pressure chain | 8 | Manual/database/rule/NER/domain-model routes are written as `useful part -> technical reason it fails -> unresolved challenge`, not as a survey list. |
| Evidence discipline | 12 | Major factual claims are cited, source-noted, or marked `需补文献`; no invented references, numbers, first claims, or performance values. |
| Method inevitability | 8 | The final paragraph names the exact method/output object and explains refusal behavior when evidence is absent. |
| Length and paragraph load | 7 | Default omit-results draft has 1,800-2,400 Chinese characters, or at least 1,500; P1-P4 carry real mechanism/evidence/consequence detail. |
| Nature-style Chinese prose | 7 | Dense, clear, stable terminology, varied sentence rhythm, no slogans, no unjustified method-first opening. |
| Omission compliance | 3 | If requested, the draft stops before current-paper result/contribution claims. |

## Quality Bands

- 90-100: Excellent draft. Only local polishing and citation completion remain.
- 85-89: Strong draft. Acceptable for user review after fixing the two weakest dimensions.
- 75-84: Not yet excellent. Revise and regenerate once.
- Below 75: Rewrite from the domain evidence card, narrative spine, and reverse outline.

For Nature-style writing, aim for at least 85. If below 85, do not present the draft as final; revise using the lowest-scoring dimensions.

## User-Provided Structure Rule

If the user provides a rough writing structure, outline, paragraph plan, or rhetorical order:

1. Use it as the primary structure.
2. Convert it into a reverse outline with paragraph roles and target lengths.
3. Convert it into a narrative spine with paragraph-to-paragraph bridge logic.
4. Evaluate whether each user-specified part has enough evidence and transition.
5. Repair missing logic links without replacing the structure.
6. Penalize only when the draft ignores the user structure, not when it differs from the default five-part fallback.

If the user structure conflicts with omit-results mode or asks for unsupported claims, keep the structure but remove/mark the unsupported parts.

## Hard Gates

Apply these gates before accepting a draft:

- If the Chinese body is below 1,200 characters, it is not a full Introduction.
- If the Chinese body is 1,200-1,500 characters, it is a short draft and must be expanded unless the user explicitly asks for brevity.
- If the draft ignores the user's supplied structure without justification, revise the reverse outline.
- If the draft lacks a narrative spine or paragraph-to-paragraph bridge logic, build it and revise before scoring.
- If adjacent paragraphs can be swapped without damaging the argument, revise the lead-ins and final bridge sentences.
- If sentence order inside a load-bearing paragraph can be shuffled freely, revise the paragraph using a sentence-function chain.
- If the draft lacks a real output object early in the argument, revise the opening or the first user-specified problem paragraph.
- If the prior-route section is a method list rather than a pressure chain, revise that section.
- If the material-specific difficulty section does not state a concrete wrong scientific conclusion caused by mis-binding, revise that section.
- If the method-necessity section says only "schema + evidence + uncertainty" without a domain-specific output object, revise that section.
- If user requested omit-results mode and result/contribution claims appear, remove them.

## Iterative Revision Loop

1. Generate V1 from the domain evidence card, narrative spine, and reverse outline.
2. Evaluate V1 with the rubric and hard gates.
3. If score is below 85 or any hard gate fails, identify the two weakest dimensions.
4. If narrative coherence is weak, revise in this order:
   - paragraph first sentences;
   - paragraph final bridge sentences;
   - sentence-function chain inside the weakest paragraph;
   - repeated transitions and topic jumps.
5. Rewrite only the paragraphs responsible for those weaknesses, unless the entire trajectory is flawed.
6. Re-evaluate the revised draft.
7. If still below 85, perform one more targeted rewrite.
8. After two revision passes, if the draft still cannot reach 85, explain the missing evidence or domain information that blocks improvement.

## Output For Quality Control

For full drafting tasks, include:

1. Domain evidence card.
2. Reverse outline.
3. Narrative spine.
4. Final Chinese Introduction after revision.
5. Claim-evidence map.
6. Quality-control table:
   - approximate score;
   - weakest dimensions;
   - coherence fixes already applied;
   - revision actions already applied;
   - remaining evidence gaps.

Keep the score approximate and explain it in prose. Do not pretend it is an objective journal decision.
