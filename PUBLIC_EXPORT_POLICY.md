# 公开导出规则（Public Export Policy）

## 导出方式（Export Model）

Public Edition从空目录开始，仅通过Whitelist加入明确允许公开的内容。它不是“复制私人工作区后再删除敏感文件”的结果。

## 允许公开（Allowed）

- 通用Architecture与Design Principles
- Generic Schema与Runtime Contract
- Evidence、Ownership、Provenance、Confidentiality Guardrail
- 去私人化的Version History
- 完全Synthetic的Demo

## 禁止公开（Excluded）

- 真实Candidate身份、教育、联系方式、偏好与Choice Threshold
- 真实Employer、Project、Achievement、Evidence或Application Material
- Submitted Resume与真实Interview / Learning Record
- Skill Installation ID、Private Source ID、Private Link与Local Machine Path
- 私人备份、文件清单、校验材料及私人Binary File

## 发布门槛（Release Gate）

只有递归审计对PII、真实候选人事实、Confidential Material、Private Runtime Reference与真实Application Data均返回0项，并且Synthetic Demo标识与Binary Exclusion通过，Public Edition才可以进入下一发布阶段。
