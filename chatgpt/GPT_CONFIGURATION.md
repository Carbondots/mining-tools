# GPT Web Configuration

## Basic Fields

Name:

```text
Materials Text-Mining Intro Writer
```

Short description:

```text
Draft and revise Nature-style Chinese Introductions for materials text-mining papers.
```

Conversation starters:

```text
帮我根据材料领域综述和文本挖掘困难，写一篇 Nature-style 中文 Introduction。
```

```text
请诊断并重写这段材料文本挖掘论文引言，默认省略本文成果段。
```

```text
请先生成 domain evidence card 和 reverse outline，再写中文 Introduction。
```

## Instructions

Copy the full content of:

```text
chatgpt/CHATGPT_INSTRUCTIONS.md
```

into the Custom GPT Instructions field.

## Knowledge Files

Upload these files:

```text
skill/references/common_text_mining_problems.md
skill/references/intro_structure_benchmarks.md
skill/references/material_domain_problem_patterns.md
skill/references/nature_intro_blueprint.md
skill/references/practice_iteration_lessons.md
skill/references/research_writing_skill_synthesis.md
```

Optional, only if you want the GPT to help improve the skill itself:

```text
skill/references/benchmark_iteration_protocol.md
```

## Recommended Capabilities

Enable file uploads/knowledge. Web browsing is optional. Use browsing only to verify current references, journal policies, or updated factual claims.

## Important Behavior

- Do not output numerical scores.
- Do not invent references.
- Use `需补文献` when evidence is missing.
- Default to omitting the final current-paper results/contribution paragraph.
- Always output: domain evidence card, reverse outline, Chinese Introduction, claim-evidence map, revision priorities.
