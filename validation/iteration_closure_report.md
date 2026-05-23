# 三领域实战验证闭环报告

## 目标

按用户要求，不再停留在说明层面，而是选择几个领域实战验证 `text-mining-intro-writing` skill。验证方式是：

1. 选取已有高质量文章对应的不同领域。
2. 用当前 skill 生成 V1。
3. 对照基准文章的行文思路、框架、详略安排和语言压力，找出差距。
4. 将共性差距反写进 skill。
5. 再生成 V2/V3/V4，直到内容承载力和结构表现明显收敛。

## 领域选择

| 领域 | 基准文章 | 主要验证点 |
|---|---|---|
| 发光/磷光材料文本挖掘 | `58Z3MKQN`，npj Computational Materials | host-dopant-emission relationship 是否足够早、足够具体 |
| 有机合成文献挖掘 | `UAL253B7`，Nature Communications | reaction record、多模态图文对齐、角色-条件绑定 |
| 冶金 P-M-S-M-P 系统图抽取 | `F9NLVIKW`，Scripta Materialia | processing-mechanism-microstructure-mechanism-property 机制链 |

## 迭代结果

### V1

文件：`v1_generated_intros_and_gap_analysis.md`

结论：结构正确，但仍偏五段式模板。

共性问题：

- output object 出现太晚。
- P3 像方法清单，而不是压力链。
- P5 同质化，三篇都落到泛泛的 schema/evidence/uncertainty。
- 材料/任务 signature 进入主线太晚。
- 段落承载力接近，缺少高质量文章的重点段落压力。

### Skill 规则更新 1

更新文件：

- `SKILL.md`
- `references/nature_intro_blueprint.md`
- `references/intro_structure_benchmarks.md`
- `references/common_text_mining_problems.md`
- `references/material_domain_problem_patterns.md`

新增规则：

- 写作前先生成 domain evidence card。
- P1 必须早早给出 output object。
- P3 必须采用 `route -> useful part -> technical reason it fails -> unresolved challenge`。
- P5 必须使用领域专属 method object。
- 新增三个 mini field cards：phosphors、organic synthesis、metallurgy system charts。

### V2

文件：`v2_generated_intros_after_skill_update.md`

结论：结构明显改善，但长度不足。三个草稿主体约 900-1,080 中文字符，仍像“强提纲”。

### Skill 规则更新 2

更新文件：

- `SKILL.md`
- `references/intro_structure_benchmarks.md`
- `references/practice_iteration_lessons.md`

新增 minimum load gate：

- omit-results Introduction 总中文主体至少 1,500 字。
- P1-P4 通常各不少于 250 字。
- P5 通常不少于 220 字。
- 至少两个段落必须包含 4-6 个句子，展开证据位置、技术原因或误绑定后果。

### V3

文件：`v3_generated_intros_after_length_gate.md`

结论：进一步扩展，但仍未稳定过 1,500 字门槛。

### V4

文件：`v4_generated_intros_pass_length_gate.md`

验证结果：

| 领域 | 中文主体字数 | 段落数 | 结果 |
|---|---:|---:|---|
| 发光/磷光材料 | 1514 | 5 | 通过 |
| 有机合成 | 1506 | 5 | 通过 |
| 冶金 P-M-S-M-P | 1507 | 5 | 通过 |

V4 达到本轮实战验证要求：三篇都保留五段结构，并同时具备 early output object、prior-route pressure chain、material/task-specific mis-binding consequence、domain-specific method object。

## 当前 skill 状态

已验证：

- `quick_validate.py` 通过：`Skill is valid!`
- 普通 skill 目录中无 `score_intro.py`、`evaluation_rubric.md`、`high_impact_benchmark_scoring.md`、`benchmark-score` 残留。
- 评分/对照仍只作为 skill 开发迭代方法，不进入普通用户输出。

## 后续注意

这次验证证明 skill 已比上一版更主动、更具体、更能生成完整引言。但它还不是所有材料领域的一劳永逸模板。下一次遇到碳点、MOF SSE、催化、玻璃、电池等领域时，应继续先做 field card，再用已有相近高质量文章做开发对照。如果生成稿出现同类弱点，再继续更新相应 reference，而不是只改单篇草稿。
