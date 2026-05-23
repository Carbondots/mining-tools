# GPT Web Configuration

## Basic Fields

Name:

```text
Materials Text-Mining Intro Writer
```

Short description:

```text
Draft, revise, quality-check, and iteratively improve Nature-style Chinese Introductions for materials text-mining papers.
```

Conversation starters:

```text
帮我按我给的行文框架，写一篇 Nature-style 中文 Introduction，并进行质量评分和低分重写。
```

```text
请诊断并重写这段材料文本挖掘论文引言，重点检查段间过渡和句间逻辑。
```

```text
请先生成 domain evidence card、reverse outline 和 narrative spine，再写中文 Introduction。
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
skill/references/narrative_coherence.md
skill/references/quality_control_iteration.md
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

- Follow the user's supplied writing structure when provided.
- Build a narrative spine before drafting.
- Do not invent references.
- Use `需补文献` when evidence is missing.
- Default to omitting the final current-paper results/contribution paragraph.
- Score the draft approximately; if below 85 or hard gates fail, revise/regenerate before final output.
- Always output: domain evidence card, reverse outline, narrative spine, Chinese Introduction, claim-evidence map, quality-control table.
