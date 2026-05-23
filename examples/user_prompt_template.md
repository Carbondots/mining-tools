# User Prompt Template

```text
请使用 Materials Text-Mining Intro Writer 写一篇 Nature-style 中文 Introduction，默认省略最后的本文成果/贡献段。

我的预设行文结构：
[例如：领域需求 -> 文献数据瓶颈 -> 现有NLP路线不足 -> 目标材料文本挖掘特异性困难 -> schema/RAG/LLM-prompt必要性]

材料领域：
[例如：碳点 / 发光磷光材料 / MOF 固态电解质 / 催化剂 / 高熵合金]

领域大综述要点：
[粘贴综述内容、关键应用、科学问题、材料变量、已有数据库或数据驱动工作]

文本数据挖掘困难：
[实体类型、关系链、证据位置、为什么 NER/规则/数据库不够、错误绑定后果]

拟采用方法：
[例如：LLM-prompt + RAG + schema + evidence grounding + missing-value labels]

引用材料：
[列出文献；没有证据的位置请用 需补文献 标注]

输出要求：
1. Domain evidence card
2. Reverse outline
3. Narrative spine
4. 中文 Introduction
5. Claim-evidence map
6. Quality-control table

请重点检查段间过渡和句间逻辑。如果评分低于 85，先按最弱维度重写，再输出最终版本。
```
