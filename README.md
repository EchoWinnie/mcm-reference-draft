# MCM Reference Draft · 美赛建模参考稿

为数学建模队伍生成一份有实质模型、计算依据和结论的精简参考论文，帮助讨论、复现与完善。默认**英文论文＋中文思路说明**；不是官方提交成品，也不保证竞赛成绩。

Create a concise, substantive MCM/ICM reference paper and a practical team guide from a problem statement and attachments. The default paper language is English. The guide follows the user's language, with Chinese as the primary-audience fallback. This is a reference for team development, not a submission-ready report.

## 中文使用说明

提供题目及其附件，然后调用：

```text
使用 $mcm-reference-draft 处理这道 MCM/ICM 题目。
生成英文精简参考论文和中文思路说明，覆盖全部题目要求。
有数据就完成必要计算与验证，并附可复现代码。
明确哪些结论已验证、哪些部分仍需我们队伍补强。
```

通常交付 `reference-paper.md` 和 `team-guide.md`；发生数值计算时附所用代码、结果和必要图表。完整多问任务默认约 2,000–3,500 英文词作为软预算，不为了字数漏问或凑内容。缺附件时会完成可支持的模型和分析，并指出无法计算的结论，不编造比赛数据。

可以指定论文、说明的语言及篇幅，例如“英文论文，西班牙语队伍说明”“论文控制在 1,500 词左右”“本次只做问题二”。题目要求的 memo 或 letter 会作为参考稿的一部分处理。

## English usage

Supply the complete problem statement and relevant attachments, then ask:

```text
Use $mcm-reference-draft to produce a concise English reference paper
and a team guide in my preferred language. Address every requirement,
run feasible computations, and distinguish supported results from
assumptions, illustrations and work still needed.
```

Language preferences are independent: an English paper may be paired with a Chinese, Spanish, French or other supported-language guide. Source documents can use a different language. Explicit requests take precedence. Actual language and file-reading capabilities depend on the host agent.

The skill covers problem interpretation, economical model selection, implementable equations, actual calculations where feasible, targeted validation and a compact written argument. It does not require a particular optimizer, model provider, manuscript engine or other skill package.

## 安装 / Installation

Install the whole `mcm-reference-draft` folder into your agent's supported skills directory. Preserve the relative paths; the reference files are part of the skill. In Codex the user-level `~/.agents/skills/mcm-reference-draft/` location can be used. Refresh skills or open a new chat if the host does not discover it immediately.

将整个文件夹放入所用智能体的技能目录，保留下面的结构。若未立即识别，可刷新技能列表或开启新对话。

```text
mcm-reference-draft/
  SKILL.md
  README.md
  agents/
    openai.yaml
  references/
    deliverables-and-languages.md
    modeling-and-validation.md
    sources-and-adaptation.md
```

## 设计参考 / Design references

Based on a review of workflow ideas from [XiaoMaColtAI/math-modeling-skill](https://github.com/XiaoMaColtAI/math-modeling-skill), [MathModelAgent](https://github.com/jihe520/MathModelAgent), and [EZ Math Model](https://github.com/woodfishhhh/EZ_math_model), with contest-format claims checked against [COMAP](https://www.contest.comap.com/undergraduate/contests/mcm/instructions.html). See [sources and adaptation decisions](references/sources-and-adaptation.md) for exact inspected files and scope.

The package contains original task instructions inspired by those designs, not copies of their implementation or bundled dependencies. Runtime output quality still requires checking against the supplied problem, data and domain knowledge.
