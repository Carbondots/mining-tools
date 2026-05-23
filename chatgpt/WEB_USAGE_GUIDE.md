# Web 端使用说明：把本地 Codex skill 迁移到 ChatGPT

## 结论

本地 Codex skill 不能被 ChatGPT 网页端自动读取。要在 web 端使用，需要把它变成 Custom GPT 或 Project 的 instructions + knowledge files。

推荐方案：创建一个 Custom GPT。

## 方案 A：Custom GPT，最推荐

1. 打开 ChatGPT 网页端。
2. 进入 `Explore GPTs` / `Create a GPT`。
3. 名称建议：`Materials Text-Mining Intro Writer`。
4. 把本目录中的 `ChatGPT_CustomGPT_Instructions.md` 全文复制到 GPT 的 Instructions。
5. 把以下本地 skill 文件上传到 Knowledge：
   - `C:\Users\47031\.codex\skills\text-mining-intro-writing\references\common_text_mining_problems.md`
   - `C:\Users\47031\.codex\skills\text-mining-intro-writing\references\intro_structure_benchmarks.md`
   - `C:\Users\47031\.codex\skills\text-mining-intro-writing\references\material_domain_problem_patterns.md`
   - `C:\Users\47031\.codex\skills\text-mining-intro-writing\references\nature_intro_blueprint.md`
   - `C:\Users\47031\.codex\skills\text-mining-intro-writing\references\practice_iteration_lessons.md`
   - `C:\Users\47031\.codex\skills\text-mining-intro-writing\references\research_writing_skill_synthesis.md`
6. 可选上传：
   - `C:\Users\47031\.codex\skills\text-mining-intro-writing\references\benchmark_iteration_protocol.md`
   只有当你希望 GPT 也帮助你继续迭代这个写作 skill 时再上传。

## 方案 B：ChatGPT Project

如果你不想创建 GPT，可以建一个 Project：

1. 新建 Project，例如 `材料文本挖掘论文写作`。
2. 把 `ChatGPT_CustomGPT_Instructions.md` 粘贴到 Project instructions。
3. 把上述 reference 文件上传到 Project files。
4. 每次在这个 Project 里对话，并明确说：`请按项目 instructions 写 Nature-style 中文 Introduction`。

Project 的优点是方便围绕一个论文长期工作；缺点是它不像 Custom GPT 那样容易复用给不同项目。

## 方案 C：普通对话临时使用

如果只是临时用一次：

1. 在普通 ChatGPT 对话中上传 `ChatGPT_CustomGPT_Instructions.md` 和 reference 文件。
2. 开头写：

```text
请严格按照我上传的 Materials Text-Mining Introduction Writer instructions 工作。默认输出 domain evidence card、reverse outline、中文 Introduction、claim-evidence map 和修改重点。不要输出评分。
```

这个方法最轻量，但每个新对话都要重新上传或重新说明。

## 推荐用户输入模板

```text
请使用 Materials Text-Mining Intro Writer 写一篇 Nature-style 中文 Introduction，默认省略最后的本文成果/贡献段。

材料领域：
[例如：碳点/发光磷光材料/MOF 固态电解质/催化剂/高熵合金]

领域大综述要点：
[粘贴综述内容、关键应用、科学问题、材料变量、已有数据库或数据驱动工作]

文本数据挖掘困难：
[实体类型、关系链、证据位置、为什么 NER/规则/数据库不够、错误绑定后果]

拟采用方法：
[例如：LLM-prompt + RAG + schema + evidence grounding + missing-value labels]

引用材料：
[列出文献或用 [需补文献] 标注]

输出要求：
1. Domain evidence card
2. Reverse outline
3. 中文 Introduction
4. Claim-evidence map
5. 修改重点
不要输出评分。
```

## 重要提醒

- Web 端不会自动访问你本机 Zotero、MinerU 文件或 Codex workspace，除非你上传文件或粘贴内容。
- 不要让 GPT 编造引用。没有引用就标注 `需补文献`。
- 如果要写正式投稿稿件，最好同时上传目标领域综述、已有 intro 基准、你的方法说明和可引用文献表。
