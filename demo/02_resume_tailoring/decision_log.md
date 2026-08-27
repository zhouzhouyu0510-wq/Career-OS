Synthetic Demo｜完全虚构示例，不使用任何真实候选人、企业、投递或面试数据。

# P1 / P2简历决策记录（Resume Decision Log）

## Source of Truth

本轮只读取`candidate_a_evidence.yaml`中的10条Synthetic Evidence：甲、乙、丙三段Experience各3条，Leadership 1条。Resume输出不新增事实、数字、Ownership或Result。

## P1｜Strategy Review Draft

Review Draft保留全部10条Evidence，以便Candidate先审阅事实边界和表达方向：

- 甲公司3条：Research、Comparison Matrix、Assumption / Uncertainty Tracker；
- 丙公司3条：Reporting View、Behavior Group、Decision Memo；
- 乙公司3条：Record Validation、Exception Taxonomy、Weekly QA Summary；
- Leadership 1条：多Workstream协调。

## P1｜Review → Submission收敛

| Review内容 | Submission处理 | 原因 |
|---|---|---|
| SYN-EV-GAMMA-01 + 02两条 | 合并为1条 | 同属Pattern Analysis，单列会重复 |
| SYN-EV-BETA-02 + 03两条 | 合并为1条 | P1只需保留Data-quality Differentiator |
| 三段Experience均完整展开 | 排序为Alpha → Gamma → Beta | 对齐Strategy岗位的Research优先级 |
| 10条Review Bullet | 收敛为8条Submission Bullet | 接近一页内容密度，同时保留全部Evidence Trace |

未删除任何Canonical Evidence；被压缩内容仍留在Source of Truth与Decision Trace。

## P2｜Risk Submission重排

- 乙公司置于首段，突出Data Validation、Rule Interpretation、Exception Traceability与QA Monitoring；
- 丙公司置于第二段，只翻译为Monitoring / Reporting Support；
- 甲公司置于第三段，只保留Evidence Traceability与Uncertainty Identification；
- SYN-EV-ALPHA-02不进入P2 Submission，因为市场比较框架与岗位核心职责距离较远；
- Data Validation保持`adjacent_strong`，禁止写成Direct Risk-management Experience。

## Safe Translation｜安全翻译

| Canonical Meaning | 岗位语言 | Status |
|---|---|---|
| Industry Brief | 产业研究与管理层信息提炼 | K1 Supported |
| Business-pattern Memo | 商业分析 | K2 Safe Translation |
| Data Validation | 数据质量与规则解释支持 | K1 Supported / Adjacent Strong |
| Weekly QA Summary | Monitoring / Risk-reporting Support | K2 Safe Translation |
| Enterprise Strategy Ownership | — | K3 Gap |
| Direct Risk-management Ownership | — | K3 Gap |
| Risk Model Development | — | K3 Gap |

Guardrails：全部通过。
