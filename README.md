# Text Mining Intro Writing

Nature-style Chinese Introduction writing resources for materials text-data-mining papers.

This repository contains two layers:

1. `skill/`: the original Codex skill files.
2. `chatgpt/`: web-side Custom GPT / Project configuration.

## Recommended Web Setup

Create a Custom GPT in ChatGPT:

- Name: `Materials Text-Mining Intro Writer`
- Description: `Draft and revise Nature-style Chinese Introductions for materials text-mining papers.`
- Instructions: copy the full text from `chatgpt/CHATGPT_INSTRUCTIONS.md`
- Knowledge files: upload the files in `skill/references/`

Recommended knowledge files:

- `common_text_mining_problems.md`
- `intro_structure_benchmarks.md`
- `material_domain_problem_patterns.md`
- `nature_intro_blueprint.md`
- `practice_iteration_lessons.md`
- `research_writing_skill_synthesis.md`

Optional for skill development only:

- `benchmark_iteration_protocol.md`

Do not use numerical scoring in normal writing conversations. Benchmark comparison is for improving the writing process, not for user-facing scores.

## User Prompt Template

```text
请使用 Materials Text-Mining Intro Writer 写一篇 Nature-style 中文 Introduction，默认省略最后的本文成果/贡献段。

材料领域：

领域大综述要点：

文本数据挖掘困难：

拟采用方法：

引用材料：

输出：
1. Domain evidence card
2. Reverse outline
3. 中文 Introduction
4. Claim-evidence map
5. 修改重点
不要输出评分。
```

## Validation

The current version was stress-tested on three domains:

- luminescent phosphors;
- organic synthesis literature mining;
- metallurgy P-M-S-M-P system chart extraction.

See `validation/iteration_closure_report.md` and `validation/v4_generated_intros_pass_length_gate.md`.
