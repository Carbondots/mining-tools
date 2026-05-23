# Nature-Style Chinese Introduction Blueprint

Use this file to draft the Introduction after loading the structure benchmarks, problem patterns, and narrative-coherence rules.

## Drafting Sequence

1. Write a one-sentence thesis for the whole Introduction:
   - `[material domain] needs [text-mining method] because [material-specific evidence chain] is locked in [literature forms] and cannot be recovered reliably by [existing route].`
2. Build a domain evidence card before any prose:
   - output object;
   - core scientific relation;
   - evidence locations;
   - mis-binding consequence;
   - prior-route bottleneck;
   - method object and refusal behavior.
3. Check whether the user supplied a rough structure. If yes, map the user's structure into the reverse outline and preserve the user's order unless it breaks evidence discipline or omit-results mode. If no, use the default five-part fallback.
4. Build a reverse outline with paragraph role, target length, evidence, and transition.
5. Build a narrative spine: controlling question, paragraph promises, paragraph-to-paragraph bridges, and final method pressure.
6. Draft paragraph by paragraph. Each paragraph must have one message, a first sentence that states or advances that message, and a last sentence that prepares the next paragraph.
7. Check claim-evidence alignment after each paragraph.
8. Check the Chinese body length before polishing. If it is below 1,500 Chinese characters, expand the load-bearing paragraphs before doing sentence-level edits.
9. Remove the current-paper results paragraph unless requested.
10. Run the coherence audit before scoring. If the draft reads like stacked material, revise lead-ins and transitions first.
11. When revising the skill itself, compare the draft against high-impact benchmarks to find reusable writing-rule gaps. Do not include this comparison in ordinary user-facing drafting output.

## User Structure Adaptation

User structure takes priority over the default blueprint. Common user structures include:

- `application importance -> field bottleneck -> literature mining gap -> proposed extraction route`;
- `existing review consensus -> unresolved data problem -> why current NLP fails -> our method necessity`;
- `material mechanism -> evidence scattering -> relation extraction challenge -> LLM/RAG schema`;
- `database/resource gap -> text-mining method gap -> material-specific schema`.

For any user structure:

1. Preserve the user's paragraph order and emphasis.
2. Add missing output object and evidence discipline inside the user's first suitable paragraph.
3. Put the prior-route pressure chain in the user-specified gap/method paragraph.
4. Put the mis-binding consequence in the user-specified difficulty paragraph.
5. If the user's structure has no place for one of these, add a short bridging sentence rather than a new major section.
6. Keep the user's structure coherent by writing explicit bridges between the user's parts. Do not solve a weak outline by replacing it with the default five-part template.

## Paragraph Blueprint

### P1: Domain Importance And Data Need

Goal: start from the material problem, not from NLP.

Must include:

- why this material system matters;
- why data-driven or AI-assisted discovery is relevant;
- the real output object by the second sentence;
- which design/search/performance space is too large for intuition alone;
- one concrete mechanism showing why multiple variables interact;
- a final sentence that explains why literature-scale evidence is needed.

Possible logic:

`field need -> coupled design variables -> missing structured output object -> why single-paper reading or intuition is insufficient -> literature-scale data need`

### P2: Literature As Latent Data

Goal: explain why papers are the key data source and why they are difficult.

Must include:

- literature contains the relevant knowledge;
- the knowledge is dispersed across text, tables, figures, captions, and supplementary files;
- the desired output is sample-level, field-level, or relation-level structured data;
- at least one example of where each evidence type usually appears;
- a final sentence that shifts the bottleneck from information existence to evidence binding.

Possible logic:

`knowledge exists -> evidence is fragmented -> output object requires binding -> fragmentation creates extraction rather than reading problem`

### P3: Existing Routes And Common Bottlenecks

Goal: introduce manual curation, databases, rules, NER, domain models, or RAG only as needed.

Must include:

- one or two prior routes;
- their useful part, technical limitation, and root reason;
- the exact unresolved challenge;
- a transition from entity recognition to relation/evidence binding;
- a final sentence that opens the material-specific difficulty.

Possible logic:

`manual/database route helps but cannot scale or update -> rule/NER route finds entities but misses relation/evidence binding -> unresolved challenge is complete records -> target material makes this failure scientifically consequential`

### P4: Material-Specific Difficulty

Goal: make the Introduction belong to the target material, not to any text-mining paper.

Must include:

- the material-specific relation chain;
- concrete field examples;
- why wrong binding changes scientific meaning;
- a mis-binding consequence sentence that explains what scientific conclusion would become wrong;
- a final sentence that makes constrained LLM/RAG/schema extraction necessary.

Possible logic:

`general binding problem becomes sharper here -> field-specific variables interact -> evidence appears in separate paper locations -> wrong binding changes the scientific conclusion -> method must preserve evidence and uncertainty`

### P5: Method Necessity Without Results

Goal: justify LLM-prompt/RAG/schema extraction as the necessary methodological direction, while stopping before current-paper achievements.

Must include:

- why schema-guided prompt extraction fits the specific challenge;
- why evidence preservation is necessary;
- what exact output object should be produced;
- what the model must refuse to infer when evidence is absent.

Possible logic:

`because prior paragraphs establish relation/evidence binding as the root problem -> LLM/RAG/schema is useful only when constrained -> output must include evidence locations and missing-value behavior -> stop before reporting current-paper results`

## Rhetorical Pattern From High-Impact Benchmarks

Use pressure escalation rather than template filling:

1. Field need: the scientific field needs a kind of knowledge that single-paper reading cannot provide.
2. Latent data: the knowledge already exists, but in fragmented literature forms.
3. Bottleneck: existing routes fail because they cannot bind the right evidence to the right sample/relation.
4. Material-specific pressure: in this field, wrong binding changes the scientific conclusion.
5. Method necessity: schema/RAG/LLM-prompt becomes necessary because it can combine context, constraints, and evidence traceability.

Do not make every paragraph the same length. The bottleneck and material-specific paragraphs should often carry more detail than the opening and final method paragraphs.

## Style Rules

- Use high-density academic Chinese. Prefer concrete nouns over slogans.
- Put the paragraph message in the first sentence.
- End each paragraph with a bridge that makes the next paragraph necessary.
- Use 5-8 sentences in the two load-bearing paragraphs: existing-route bottleneck and material-specific difficulty.
- Let each sentence connect by cause, contrast, consequence, refinement, or example.
- Use stable terms for material objects and method objects.
- Use cautious verbs for unresolved claims: "有望", "可用于", "需要", "提示", "限制".
- Prefer short transitions only when they carry logic: "然而", "因此", "更关键的是", "在这一背景下".
- Avoid decorative phrases such as "在当今快速发展的时代", "具有划时代意义", "开启新范式" unless the evidence supports them.
- Avoid synonym cycling. Technical repetition is clarity.
- Vary sentence length. Short sentences should mark a conceptual turn; longer sentences should carry mechanism and evidence.

## Citation Discipline

For every main claim, attach one of:

- a normal citation marker supplied by the user,
- a source note from the local evidence table,
- `需补文献[claim type]`.

Never turn a source note into a formal citation if the reference entry is missing.

## Omission Rule For The User's Current Objective

The user's stated default is to omit the final result/contribution paragraph. Therefore stop after the method-necessity paragraph. Do not add:

- "本文提出..."
- "我们构建..."
- "实验结果表明..."
- "精度达到..."
- "本研究的主要贡献如下..."

If a transition to Methods is needed, end with a non-result sentence:

`这一写法将引言的重点保留在问题必要性上，为后续方法部分展开 schema 设计、证据回链和质量控制留下空间。`
