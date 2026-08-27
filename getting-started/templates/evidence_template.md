# Evidence｜证据记录模板

## AI协作填写｜最简单用法

### 1. 你给AI什么

- 本模板；
- 已经由你确认的Experience Markdown。

不要在这一步重新让AI从未经确认的原始材料直接生成Evidence，也不需要为每个日常任务建立Evidence。

### 2. 复制这段Prompt

```text
请只从我已经确认的Experience Markdown中，提取值得用于Job Fit、简历或面试的重要Claim，并严格按照Evidence模板整理。

每条必须记录Fact、Ownership、Result Scope、Source、Confidence和External-safe。无法从已确认Experience确定的字段请标记“待确认”，不得推断；项目结果不得自动写成个人结果，没有依据的数字和技术能力不得补充。

请先列出候选Evidence及待确认问题；等我确认后，再输出完整Evidence Markdown。不需要为每个日常任务建立Evidence。
```

### 3. AI应该先做什么

先筛选真正值得进入Job Fit、简历或面试的重要Claim，并把缺少Source、Ownership或Result Scope的地方列为待确认。

### 4. 你确认后最终得到什么

一条或一组可追溯的Evidence记录。每个重要字段都应由你确认后再保存。

---

> 以下是最终Markdown的填写结构。每个字段下面的一句话说明其用途。

## Evidence ID

用于稳定识别这条Evidence，例如`EV-EXP-001`。  
[请填写]

## Claim

希望在简历、面试或选岗判断中表达或证明的主张。  
[请填写]

## Fact

已经确认真实发生的事情，保留原始口径，不写夸大的结果。  
[请填写]

## Ownership

说明本人实际负责什么，以及哪些部分由团队、负责人或其他成员承担。  
[请填写]

## Result Scope

说明结果可以归因到什么范围，以及不能扩大到哪里。  
[请填写]

## Source

说明事实来自什么材料、记录或本人确认；敏感Source不要直接公开。  
[简历 / 报告 / 工作记录 / 本人确认 / 其他]

## Confidence

说明当前可信程度。建议使用：`confirmed`、`partially_confirmed`或`pending_confirmation`。  
[请填写]

## External-safe

说明该内容是否适合在简历、面试或公开场景表达。  
[yes / needs_redaction / no / 待判断]

## Related Experience

关联到哪一段Experience，便于追溯事实来源。  
[请填写经历名称或ID]

## 用户确认

- 当前状态：[已确认 / 需要修改 / 不确定 / 不适合对外表达]
- 确认说明：[请填写]

[返回Getting Started首页](../README.md)
