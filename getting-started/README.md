# Getting Started｜建立自己的Career OS事实底座

Career OS不是从一份简历直接推断一个人的全部经历，而是先建立一套可以确认、追溯和持续维护的候选人事实底座（Candidate Source of Truth）。Job Fit Analyzer、Resume Tailor与Interview Coach都会从同一套事实资产中读取信息。

> **事实资产是个性化的，但建立方法是可复用的。**

你不需要会编程、YAML或数据库，也不需要一次建立几十个文件。建议先完成Quick Start，在真实选岗和投递中使用，再按需要逐步补充Full Setup。

## 两种开始方式

### A｜Quick Start：快速开始

适合第一次尝试Career OS、当前主要目标是选岗或定制简历、暂时不想建立完整资产体系的人。

大约20–30分钟准备：

- 一份候选人画像（Candidate Profile）；
- 3–5段重要经历；
- 每段3–5条真实事实；
- 基本工作偏好与约束。

完成后即可进入：

`Job Fit Analyzer → Resume Tailor`

→ [开始Quick Start](quick_start.md)

### B｜Full Setup：完整配置

适合在秋招、春招或长期求职中反复投递，希望继续使用Interview Coach与Learning Migration，并降低AI事实漂移和责任膨胀的人。

Full Setup会逐步补充：

- Candidate Profile；
- Experience Pool；
- Evidence；
- 个人责任边界（Ownership）；
- 结果适用范围（Result Scope）；
- Source / Confidence；
- Story Bank；
- Preference & Constraints。

> **这些内容不要求手工一次性完成，可以通过AI协作逐步建立。**

→ [了解Full Setup](full_setup.md)

## 完整Onboarding路径

```text
原始材料 / 个人回忆
        ↓
AI辅助提取与追问
        ↓
Candidate Profile
        ↓
Experience Pool
        ↓
Evidence + Ownership + Result Scope
        ↓
Story Bank
        ↓
Preference & Constraints
        ↓
用户确认事实
        ↓
Candidate Source of Truth Ready
        ↓
Job Fit Analyzer → Resume Tailor → Interview Coach
```

## AI与用户怎样分工

| AI可以做 | 必须由用户完成 |
|---|---|
| 从材料中提取事实、整理结构 | 确认事情是否真实发生 |
| 发现信息缺口并发起追问 | 澄清数字、个人责任与结果边界 |
| 区分项目结果与个人贡献 | 判断材料是否有权使用或公开 |
| 生成Human-readable Markdown草稿 | 对重要Claim作最终确认 |
| 在确认后转换Schema / YAML | 决定哪些内容不适合对外表达 |
| 检查资产前后矛盾 | 拒绝AI没有依据的推断 |

AI负责整理、提问、结构化和格式转换；用户负责提供事实、澄清边界和最终确认。AI不能用“合理推测”填补事实空白。

→ [查看AI协作方法与可复制Prompt](ai_collaboration_guide.md)

## 什么时候可以进入三个Runtime

| Runtime | 最低Ready标准 |
|---|---|
| Job Fit Analyzer | Candidate Profile、主要经历、核心Evidence、基本偏好与约束、目标JD |
| Resume Tailor | 在上述基础上，关键经历的Ownership、Result Scope和技术能力边界已经明确 |
| Interview Coach | 在上述基础上，已有实际投递Resume、高价值Story、关键Evidence及事实与责任边界 |

## 资产准备好后，怎么开始使用？

Career OS Public Edition提供的是可阅读、可复用的工作流规范与示例，不是托管式SaaS或一键安装工具。

完成自己的事实资产后，可以将相关资产作为上下文提供给通用AI工具，并按照对应Runtime的公开规范执行：

- [Job Fit Analyzer](../skills/job-fit-analyzer/README.md)：输入Candidate Profile、主要Experience / Evidence、Preference & Constraints以及目标JD，用于选岗与志愿排序。
- [Resume Tailor](../skills/resume-tailor/README.md)：在确定目标岗位后，读取同一事实底座进行Evidence选择、岗位化表达和简历收敛。
- [Interview Coach](../skills/interview-coach/README.md)：在实际投递后，结合Submission Resume、Story与Evidence进行问题准备、模拟、复盘和学习迁移。

无论使用哪一种AI工具，下游Runtime都只能选择、组织和翻译已经确认的事实，不能因为岗位需要而创造新的Candidate Fact。

## 不要一开始过度建设

不需要为了使用Career OS先建立几十个文件。更有效的顺序是：

> **先Quick Start → 实际选岗与投递 → 再按需要逐步Full Setup。**

事实资产应该随着求职过程增长，而不是一次性完成。

## Markdown-first，结构化可选

本Onboarding采用“Markdown-first Onboarding + Optional Structured Normalization”：

1. 先用Human-readable Markdown整理和确认事实；
2. 有需要时，再让AI转换为Structured YAML；
3. 两种形式必须保持事实一致；
4. 结构化转换不得生成新事实。

YAML只是机器可读表示，不是新的事实来源，也不是普通用户的入门门槛。
