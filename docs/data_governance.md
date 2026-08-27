# 数据与证据治理（Data / Evidence Governance）

## 信息类型

- **Canonical Fact｜已确认事实**：经过核验的Candidate现实。
- **Candidate Insight｜候选人洞察**：经Candidate确认的解释或偏好。
- **Prepared Narrative｜准备表达**：面向具体岗位组织的事实表达。
- **External Role Knowledge｜外部岗位知识**：有来源的公司、岗位或市场信息。
- **Derived Analysis｜派生分析**：Runtime生成的决策、诊断或建议。
- **Synthetic Fixture｜测试样例**：用于公开演示或Runtime测试的虚构数据。

## Claim Guardrail

所有Runtime共同遵守五条边界：

1. **Ownership｜责任边界**：个人贡献不等于团队Owner。
2. **Result Scope｜结果口径**：项目结果不会自动变成个人结果。
3. **Number｜数字口径**：只有已确认数字可以作为Candidate Evidence。
4. **Confidentiality｜保密边界**：不适合外部表达的信息必须被阻断。
5. **Technical Depth｜技术深度**：Exposure不等于Proficiency或Production Ownership。

## External Source Governance

| Level | 含义 | 可形成的Signal |
|---|---|---|
| A | Official / Primary Source | Confirmed Role Signal |
| B | Corroborated Supporting Source | Supporting Evidence |
| C | 多条独立、近期、岗位可识别的经验重复 | Repeated Anecdotal Signal |
| D | 单条个人经验 | Possible Signal |
| Noise | 无法核验、跨岗位或低可信内容 | Ignore |

## Mutation Policy

Runtime可以排序、选择、翻译与诊断，但不能创造Candidate History。任何可能改变Canonical Layer的发现都必须进入Review流程，并保留Source、Confidence与Rationale。
