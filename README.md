# Text Mining Intro Writing

Nature-style Chinese Introduction writing resources for materials text-data-mining papers.

This repository contains two layers:

1. `skill/`: the original Codex skill files.
2. `chatgpt/`: web-side Custom GPT / Project configuration.

## Recommended Web Setup

Create a Custom GPT in ChatGPT:

- Name: `Materials Text-Mining Intro Writer`
- Description: `Draft, revise, quality-check, and iteratively improve Nature-style Chinese Introductions for materials text-mining papers.`
- Instructions: copy the full text from `chatgpt/CHATGPT_INSTRUCTIONS.md`
- Knowledge files: upload the files in `skill/references/`

Recommended knowledge files:

- `common_text_mining_problems.md`
- `intro_structure_benchmarks.md`
- `material_domain_problem_patterns.md`
- `nature_intro_blueprint.md`
- `narrative_coherence.md`
- `quality_control_iteration.md`
- `practice_iteration_lessons.md`
- `research_writing_skill_synthesis.md`

Optional for skill development only:

- `benchmark_iteration_protocol.md`

## Current Writing Behavior

The assistant should:

- follow the user's supplied writing structure when provided;
- build a domain evidence card, reverse outline, and narrative spine before drafting;
- write a coherent Introduction rather than stack related facts;
- run an approximate quality-control score;
- revise or regenerate if the score is below 85 or any hard gate fails;
- default to omitting the final current-paper results/contribution paragraph unless requested.

## User Prompt Template

```text
请使用 Materials Text-Mining Intro Writer 写一篇 Nature-style 中文 Introduction，默认省略最后的本文成果/贡献段。

我的预设行文结构：
[例如：领域需求 -> 文献数据瓶颈 -> 现有NLP路线不足 -> 碳点文本挖掘特异性困难 -> schema/RAG/LLM-prompt必要性]

材料领域：

领域大综述要点：

文本数据挖掘困难：

拟采用方法：

引用材料：

输出：
1. Domain evidence card
2. Reverse outline
3. Narrative spine
4. 中文 Introduction
5. Claim-evidence map
6. Quality-control table

如果评分低于 85，请先重写再输出最终版本。
```

## Validation

The earlier version was stress-tested on three domains:

- luminescent phosphors;
- organic synthesis literature mining;
- metallurgy P-M-S-M-P system chart extraction.

The current version adds a further quality-control layer for narrative coherence: paragraph lead-ins, paragraph-final bridges, and sentence-function chains.

See `validation/iteration_closure_report.md` and `validation/v4_generated_intros_pass_length_gate.md`.
