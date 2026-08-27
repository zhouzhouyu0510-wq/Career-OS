# 如何用AI建立自己的Career OS事实资产

普通用户不需要自己设计Schema或手写YAML。更稳妥的方法是：先让ChatGPT、Gemini、Claude等通用AI协助提取、追问和整理Human-readable Markdown，由用户逐项确认后，再按需要转换为结构化数据。

## Phase 1｜提供原始材料

可以提供：

- 当前简历；
- 实习或项目回忆；
- 项目报告、PPT与工作笔记；
- 会议纪要与数据表说明；
- 竞赛材料；
- 个人复盘。

> **隐私提醒：**上传工作材料前，请确认自己有权使用，并优先删除姓名、联系方式、客户信息、内部经营数据、未公开项目资料、证明人信息等敏感内容。AI不能替你判断内部材料是否有权公开。

## Phase 2｜先提取事实，不急着包装

AI首先只做：

- 提取任务；
- 提取交付物（Deliverable）；
- 提取材料中明确出现的数字；
- 提取个人责任；
- 区分个人结果与项目结果；
- 标记不确定信息。

不要一开始就要求“帮我优化成漂亮简历”。事实资产阶段首先追求真实性，而不是表达强度。

## Phase 3｜让AI针对缺口追问

AI应围绕最影响准确性的信息提问，例如：

- 这个报告由几个人共同完成？
- 你具体负责哪些章节？
- 这个数字是团队整体还是你的个人工作量？
- 最终方案由谁决定？
- 这个规则是你提出、参与修改，还是最终审批？
- 结果是否有材料或本人回忆可以确认？

> AI不能用“合理推测”填补这些空白。无法确认时应记录为“待确认”或`unknown`。

## Phase 4｜生成Human-readable资产

优先生成：

- Candidate Profile Markdown；
- Experience Markdown；
- Evidence Markdown；
- Story Markdown；
- Preference & Constraints Markdown。

对应模板：

- [Candidate Profile模板](templates/candidate_profile_template.md)
- [Experience模板](templates/experience_template.md)
- [Evidence模板](templates/evidence_template.md)
- [Story模板](templates/story_template.md)
- [Preference & Constraints模板](templates/preference_constraints_template.md)

## Phase 5｜用户确认与冻结

每条重要Claim必须由用户判断：

- 正确；
- 需要修改；
- 不确定；
- 不适合对外表达。

未确认内容不得自动升级为事实。确认后仍可保留版本记录，但不应悄悄覆盖原始边界。

## Phase 6｜可选：转换为结构化数据

Human-readable资产确认后，可以让AI在不新增事实的前提下转换为Structured YAML。

> YAML是机器可读表示，不是新的事实来源。普通用户无需手工编写。

转换完成后，至少抽查：

- Fact；
- Ownership；
- Result Scope；
- Evidence ID；
- Confidence；
- Preference。

确认这些字段与Markdown一致。可查看[完全虚构的YAML示例](examples/structured_asset_example.yaml)。

## AI可以做什么

- 从材料中提取事实并整理结构；
- 发现信息缺口并发起针对性追问；
- 区分项目结果与个人贡献；
- 生成Markdown草稿；
- 在用户确认后进行Schema / YAML格式转换；
- 检查不同资产之间的矛盾。

## AI不能代替用户做什么

- 确认某件事情是否真实发生；
- 猜测未提供的数字；
- 将团队结果升级为个人结果；
- 猜测Ownership；
- 自动确认技术能力；
- 判断内部材料是否有权公开；
- 在没有用户确认时把推测写入Source of Truth。

## 可复制Prompt

### Prompt 1｜整理一段经历

```text
我正在建立Career OS事实资产。请先不要帮我写简历。请根据我提供的材料提取：背景、任务、个人行动、交付物、项目结果、个人贡献和责任边界。对不能确定的信息标记“待确认”，不要自行推断。完成初步整理后，再针对最影响事实准确性的缺口向我提问。
```

### Prompt 2｜建立Evidence

```text
请从已经由我确认的经历中，提取可能进入简历或面试的重要Claim。对每条记录Fact、Ownership、Result Scope、Source、Confidence和External-safe。项目整体结果不能自动写成个人结果，没有证据的数字或技术能力不得补充。
```

### Prompt 3｜建立Story

```text
请从已确认Evidence中选择适合面试的高价值经历，按照Situation、Task、Insight、Action、Result、Contribution、Reflection整理Story。不得增加原Evidence中不存在的事实；无法确认的细节请标记“待确认”。
```

### Prompt 4｜转换为YAML

```text
请把以下已经由我确认的Markdown资产转换为结构化YAML。只能转换格式，不得补充、推断或升级任何事实；无法映射的字段请保留unknown或“待确认”。转换后请列出Fact、Ownership、Result Scope、Evidence ID、Confidence与Preference的对应关系，供我抽查。
```

[返回Getting Started首页](README.md)
