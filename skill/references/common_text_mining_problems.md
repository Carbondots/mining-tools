# Common Text-Mining Problems

Use this file to build cross-paper and cross-domain transferable language. These problems can be reused across material systems, but every final draft must connect them to the specific material domain.

## Transferable Problem Chain

1. Materials discovery is shifting toward data-driven and AI-assisted design.
2. Data-driven design needs structured, sample-level, machine-readable records.
3. Much of the necessary knowledge is locked in papers, tables, figures, captions, supplementary files, and narrative experimental procedures.
4. Manual curation is slow, expensive, inconsistent, and hard to update.
5. Existing databases often omit processing history, sample identity, uncertainty, negative cases, and field-specific context.
6. Rule-based extraction and NER can identify entities but often fail at relation binding, cross-sentence context, cross-table evidence, and domain-specific syntax.
7. Domain BERT or supervised models need labeled corpora and may transfer poorly across subfields.
8. LLM-prompt/RAG/schema workflows can use context and flexible instructions, but must be grounded by evidence to avoid hallucination.

## Output Object Grammar

Name the output object early and keep it stable. Use this grammar:

`The paper does not merely extract [entities/values]; it reconstructs [output object] that binds [field A], [field B], [field C], and [evidence source] into one auditable record.`

Examples:

- Phosphors: `host-dopant-emission relationship`.
- Organic synthesis: `reaction record`.
- Metallurgy: `P-M-S-M-P system chart`.
- Carbon dots: `sample-level precursor-process-surface-performance record`.
- MOF solid-state electrolytes: `candidate-level structure-modification-electrochemical-performance record`.

## Reusable Chinese Claim Forms

Use these as patterns, not fixed boilerplate:

- 材料研究并不缺少单篇论文中的知识，真正缺少的是可跨论文比较、可追溯、可计算的样品级记录。
- 文献中的实验事实常以正文叙述、图表、图注和补充信息的形式分散出现，导致同一样品的组成、工艺、结构和性能难以被自动绑定。
- 人工整理能够保证局部准确性，但难以跟上文献增长，也难以稳定覆盖处理历史、测试条件、异常值和未报告字段。
- 现有数据库通常更适合存放已经标准化的结果，而不擅长恢复论文中隐含的实验上下文。
- 传统 NER 的优势在于实体边界识别，但材料文本挖掘更需要把实体放回样品、工艺、表征和性能之间的证据链中。
- 基于规则的 parser 在字段边界明确的任务中有效，但当命名方式、表格结构和上下文关系随材料体系变化时，规则维护成本会迅速上升。
- LLM-prompt 的价值不应写成“模型更强”，而应写成能够在明确 schema、上下文证据和约束输出之间建立可复核的结构化记录。
- RAG 或证据回链的必要性来自科学写作本身：每个抽取字段都需要能回到原文位置，而不是只输出看似合理的答案。

## Method-Contrast Ladder

Use this order when comparing methods:

1. Manual curation: accurate but not scalable.
2. Domain databases: useful but coverage and fields are incomplete.
3. Rules and regular expressions: precise in narrow formats but brittle.
4. NER and relation extraction: good for entity spans but weak for sample-level binding.
5. Domain language models: better terminology representation but require labels or fine-tuning.
6. LLM-prompt/RAG/multi-stage schema: flexible and context-aware, but must be constrained, source-grounded, and audited.

Do not list methods as a survey if the Introduction is for a research article. Mention only enough prior routes to make the target challenge unavoidable.

Convert every method contrast into this chain:

`[route] is useful for [what it can do], but fails at [target relation] because [technical reason]; therefore [unresolved challenge] remains.`

## Hard Fail Genericity

The following statements are too generic unless followed by material-specific detail:

- 文献数量快速增长。
- 文本是非结构化的。
- 人工提取效率低。
- NER 难以处理复杂关系。
- LLM 具有强大的理解能力。

Repair them by adding the exact object, field, and relation:

- Which material entities?
- Which synthesis or processing variables?
- Which structural or surface descriptors?
- Which performance values?
- Which sample identity or evidence-binding problem?
- Which figure, table, caption, or supplement source?
