# Getting Started｜建立自己的Career OS事实底座

Career OS不是从一份简历直接推断一个人的全部经历，而是先建立一套可以确认、追溯和持续维护的候选人事实底座（Candidate Source of Truth）。Job Fit Analyzer、Resume Tailor与Interview Coach都会从同一套事实资产中读取信息。

> **事实资产是个性化的，但建立方法是可复用的。**

你不需要会编程、YAML或数据库，也不需要先手工填完所有模板。最简单的方式是把“原始材料 + 对应模板 + 模板顶部Prompt”一起交给AI：AI先提取和追问，你确认后再保存完整Markdown。

## 两种开始方式

### A｜Quick Start：快速开始

适合第一次尝试Career OS、当前主要目标是选岗或定制简历、暂时不想建立完整资产体系的人。

大约20–30分钟准备：

- 一份候选人画像（Candidate Profile）；
- 3–5段重要经历；
- 每段3–5条真实事实；
- 基本工作偏好与约束。

完成后即可进入：`Job Fit Analyzer → Resume Tailor`

→ [开始Quick Start](quick_start.md)

### B｜Full Setup：完整配置

适合在秋招、春招或长期求职中反复投递，希望继续使用Interview Coach与Learning Migration，并降低AI事实漂移和责任膨胀的人。

Full Setup会逐步补充Candidate Profile、Experience Pool、Evidence、个人责任边界（Ownership）、结果范围（Result Scope）、Source / Confidence、Story Bank与Preference & Constraints。

> **这些内容不要求手工一次性完成，可以通过AI协作逐步建立。**

→ [了解Full Setup](full_setup.md)

## 已经有事实资产了？

如果你已经完成Quick Start，下一步不需要安装软件，也不需要把整个仓库交给AI。

→ **[如何真正运行Career OS｜Job Fit、Resume、Interview第一次怎么用](how_to_run.md)**

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
选择当前任务
        ↓
个人资产 + 当前任务材料 + 对应Public Runtime Specification
        ↓
Job Fit / Resume / Interview
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

→ [查看AI协作方法](ai_collaboration_guide.md)

## 什么时候可以进入三个Runtime

| 模块 | 最低Ready标准 |
|---|---|
| Job Fit Analyzer | Candidate Profile、主要经历、核心Evidence、基本偏好与约束、目标JD |
| Resume Tailor | 在上述基础上，关键经历的Ownership、Result Scope和技术能力边界已经明确 |
| Interview Coach | 在上述基础上，已有实际投递Resume、高价值Story、关键Evidence及事实与责任边界 |

## 不要一开始过度建设

> **先Quick Start → 实际选岗与投递 → 再按需要逐步Full Setup。**

事实资产应该随着求职过程增长，而不是一次性完成。

## Markdown-first，结构化可选

本Onboarding采用“Markdown-first Onboarding + Optional Structured Normalization”：

1. 先用Human-readable Markdown整理和确认事实；
2. 有需要时，再让AI转换为Structured YAML；
3. 两种形式必须保持事实一致；
4. 结构化转换不得生成新事实。

YAML只是机器可读表示，不是新的事实来源，也不是普通用户的入门门槛。
