# Job Fit Analyzer｜Public Runtime Specification

Job Fit Analyzer解决：**当一家单位开放多个岗位、投递名额有限时，Candidate应该把机会给谁。**

它不是简单的JD关键词匹配器，而是把以下判断分开：Eligibility、Candidate→Job Fit、Competitiveness、Job→Candidate Fit与Application Strategic Value。

支持两种Mode：

- `multi_role`：比较同一单位内的多个Application Unit，并优化有限志愿组合。
- `single_role`：分析单个岗位，并生成Resume Tailor Handoff。

暂不包含Cross-company Portfolio Optimization。

继续阅读：[Runtime](runtime.md)｜[Schema](schema.md)｜[Guardrails](guardrails.md)｜[Handoff Contract](handoff_schema.yaml)

