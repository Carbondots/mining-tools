# Nature-Style Chinese Introduction Blueprint

Use this file to draft the Introduction after loading the structure benchmarks and problem patterns.

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
3. Build a five-row reverse outline with paragraph role, target length, evidence, and transition.
4. Draft paragraph by paragraph. Each paragraph must have one message and a first sentence that states that message.
5. Check claim-evidence alignment after each paragraph.
6. Check the Chinese body length before polishing. If it is below 1,500 Chinese characters, expand the load-bearing paragraphs before doing sentence-level edits.
7. Remove the current-paper results paragraph unless requested.
8. When revising the skill itself, compare the draft against high-impact benchmarks to find reusable writing-rule gaps. Do not include this comparison in ordinary user-facing drafting output.

## Paragraph Blueprint

### P1: Domain Importance And Data Need

Goal: start from the material problem, not from NLP.

Must include:

- Why this material system matters.
- Why data-driven or AI-assisted discovery is relevant.
- The real output object by the second sentence.
- Which design/search/performance space is too large for intuition alone.
- One concrete mechanism showing why multiple variables interact.

Avoid:

- Generic "AI is developing rapidly".
- Long application lists with no relation to data.

Possible sentence pattern:

`[材料体系] 因 [关键性质/应用] 成为 [领域] 的重要对象；真正限制数据驱动设计的并不是单个数值缺失，而是缺少能够连接 [核心关系] 的 [输出对象]。然而，其性能优化同时受 [变量组1]、[变量组2] 和 [变量组3] 控制，使经验试错和单篇论文阅读难以支撑系统设计。`

### P2: Literature As Latent Data

Goal: explain why papers are the key data source and why they are difficult.

Must include:

- Literature contains the relevant knowledge.
- The knowledge is dispersed across text, tables, figures, captions, and supplementary files.
- The desired output is sample-level, field-level, or relation-level structured data.
- At least one example of where each evidence type usually appears.

Possible sentence pattern:

`这些知识已经大量存在于已发表文献中，但通常以实验叙述、表格、图注和补充信息的形式分散出现；只有将 [字段链] 还原为同一样品的结构化记录，才能支持跨论文比较和后续建模。`

### P3: Existing Routes And Common Bottlenecks

Goal: introduce manual curation, databases, rules, NER, domain models, or RAG only as needed.

Must include:

- One or two prior routes.
- Their useful part, technical limitation, and root reason.
- The exact unresolved challenge.
- A transition from entity recognition to relation/evidence binding.

Possible sentence pattern:

`人工整理和领域数据库能够提供高置信数据，但其覆盖范围、更新速度和字段完整性难以适应 [材料体系] 的文献增长；基于规则或 NER 的方法可以识别 [实体类型]，却往往难以判断 [关系/绑定问题]，因为相关证据常跨句、跨表格或跨段落出现。换言之，已有路线留下的核心缺口不是缺少实体，而是缺少可复核的 [输出对象]。`

### P4: Material-Specific Difficulty

Goal: make the Introduction belong to the target material, not to any text-mining paper.

Must include:

- The material-specific relation chain.
- Concrete field examples.
- Why wrong binding changes scientific meaning.
- A mis-binding consequence sentence that explains what scientific conclusion would become wrong.

Possible sentence pattern:

`在 [材料体系] 中，这一问题更加突出：[变量A] 与 [变量B] 并非独立字段，而是共同决定 [性质/应用] 的条件组合。如果抽取时丢失 [样品编号/步骤顺序/测试条件/表面状态]，同一数值就可能被错误地解释为另一种材料或另一种性能。`

### P5: Method Necessity Without Results

Goal: justify LLM-prompt/RAG/schema extraction as the necessary methodological direction, while stopping before current-paper achievements.

Must include:

- Why schema-guided prompt extraction fits the specific challenge.
- Why evidence preservation is necessary.
- What exact output object should be produced.
- What the model must refuse to infer when evidence is absent.

Possible sentence pattern:

`因此，更合适的路径是将 LLM 的上下文理解能力限制在明确的领域 schema、检索证据和可审计输出中，使模型不是概括论文，而是生成带有原文定位、缺失值标记和不确定性说明的 [输出对象]；当 [关键字段/关系] 缺少证据时，模型应保留空缺或标注不确定，而不是用常识补全。`

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
- Use 5-8 sentences in the two load-bearing paragraphs: existing-route bottleneck and material-specific difficulty.
- Let each sentence connect by cause, contrast, consequence, refinement, or example.
- Use stable terms for material objects and method objects.
- Use cautious verbs for unresolved claims: "有望", "可用于", "需要", "提示", "限制".
- Prefer short transitions: "然而", "因此", "更关键的是", "在这一背景下".
- Avoid decorative phrases such as "在当今快速发展的时代", "具有划时代意义", "开启新范式" unless the evidence supports them.
- Avoid synonym cycling. Technical repetition is clarity.
- Vary sentence length. Short sentences should mark a conceptual turn; longer sentences should carry mechanism and evidence.

## Citation Discipline

For every main claim, attach one of:

- a normal citation marker supplied by the user,
- a source note from the local evidence table,
- `需补文献 [claim type]`.

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
