# 如何用AI建立自己的Career OS事实资产

本页解释“为什么这样与AI协作”以及跨模板都适用的方法。**第一次使用时，优先直接使用五个模板顶部的专属Prompt**；本页末尾的通用Prompt只适合已经熟悉流程后的批量复核或格式转换。

普通用户不需要设计Schema或手写YAML。更稳妥的方法是：先让通用AI提取、追问和整理Human-readable Markdown，由用户逐项确认后，再按需要转换为结构化数据。

## Phase 1｜提供原始材料和对应模板

原始材料可以是当前简历、经历回忆、项目报告、PPT、工作笔记、会议纪要、数据表说明、竞赛材料或个人复盘。材料告诉AI“发生过什么”，模板告诉AI“最终按什么结构保存”。

> **隐私提醒：** 上传工作材料前，请确认自己有权使用，并优先删除姓名、联系方式、客户信息、内部经营数据、未公开项目资料、证明人信息等敏感内容。AI不能替你判断内部材料是否有权公开。

## Phase 2｜为什么第一次只提取，不直接写简历

AI第一轮应该提取任务、交付物、材料中明确出现的数字、个人责任，并区分项目结果与个人结果。不要一开始就要求“优化成漂亮简历”：事实资产阶段先追求真实性，再考虑表达强度。

## Phase 3｜为什么第二步必须追问

材料通常缺少最影响准确性的边界，例如：报告由几人完成、本人负责哪些章节、数字属于团队还是个人、最终方案由谁决定。AI应该把这些空白变成问题，而不是用“合理推测”补齐。无法确认时保留“待确认”或`unknown`。

## Phase 4｜用户如何确认

对每条重要Claim，用户需要判断：正确、需要修改、不确定，或不适合对外表达。尤其要核对数字、Ownership、Result Scope、技术能力和材料权限。

## Phase 5｜AI按模板输出完整Markdown

用户回答后，AI再严格按照对应模板输出完整Markdown，不省略栏目。建议每次只处理一种资产或一段Experience，保存后再进入下一步。

模板入口：

- [Candidate Profile模板](templates/candidate_profile_template.md)
- [Experience模板](templates/experience_template.md)
- [Evidence模板](templates/evidence_template.md)
- [Story模板](templates/story_template.md)
- [Preference & Constraints模板](templates/preference_constraints_template.md)

## Phase 6｜可选：转换为结构化数据

Human-readable资产确认后，可以让AI在不新增事实的前提下转换为Structured YAML。

> YAML是机器可读表示，不是新的事实来源。普通用户无需手工编写。

转换完成后，至少抽查Fact、Ownership、Result Scope、Evidence ID、Confidence和Preference是否与Markdown一致。可查看[完全虚构的YAML示例](examples/structured_asset_example.yaml)。

## AI可以做什么

- 从材料中提取事实、整理结构并发现缺口；
- 发起针对性追问；
- 区分项目结果与个人贡献；
- 按模板生成Markdown草稿；
- 在用户确认后转换Schema / YAML；
- 检查不同资产之间的矛盾。

## AI不能代替用户做什么

- 确认某件事情是否真实发生；
- 猜测未提供的数字、Ownership或技术能力；
- 将团队结果升级为个人结果；
- 判断内部材料是否有权公开；
- 在没有用户确认时把推测写入Source of Truth。

## 熟悉流程后可用的通用Prompt

以下Prompt不替代模板顶部的专属Prompt。它们仅用于跨资产复核或格式转换。

### 通用Prompt 1｜事实边界复核

```text
请复核以下已整理资产中的Fact、Ownership、Result Scope、数字和技术能力边界。不要润色，不要补充事实；请列出相互矛盾、缺少Source或仍需用户确认的项目。
```

### 通用Prompt 2｜跨文件一致性检查

```text
请比较以下Candidate Profile、Experience、Evidence和Story，检查同一事实是否出现口径漂移。只能报告差异，不得自动选择或改写事实版本。
```

### 通用Prompt 3｜转换为YAML

```text
请把以下已经由我确认的Markdown资产转换为结构化YAML。只能转换格式，不得补充、推断或升级任何事实；无法映射的字段保留unknown或“待确认”。转换后列出Fact、Ownership、Result Scope、Evidence ID、Confidence与Preference的对应关系，供我抽查。
```

继续阅读：[Quick Start](quick_start.md)｜[Full Setup](full_setup.md)｜[如何真正运行Career OS](how_to_run.md)｜[返回首页](README.md)
