# 运行流程（Runtime）

1. Input Preflight｜输入预检
2. Notice / Job Extraction｜公告与岗位提取
3. Application Unit Heterogeneity Analysis｜申请入口异质性分析
4. Application Constraint Detection｜投递限制识别
5. Eligibility Gate｜硬门槛判断
6. Broad Screening｜全岗位初筛
7. Deep External Research｜Shortlist深度研究
8. Four-layer Fit｜四层Fit分析
9. Ranking｜单岗位排序
10. Portfolio Optimization｜有限志愿组合优化
11. Questions to Verify｜待核实问题
12. Resume Tailor Handoff｜下游交接
13. Decision Log｜决策记录

## 四层判断（Four-layer Fit）

- **Eligibility**：能不能投。
- **Candidate→Job Fit**：已确认Evidence能否覆盖核心工作。
- **Competitiveness**：面对现实Candidate Pool，凭什么赢。
- **Job→Candidate Fit**：拿到以后是否符合Candidate已确认偏好。

Application Strategic Value决定有限名额是否值得投入。系统不使用单一百分比替代这些维度。

## 直接匹配（Direct Match）

Direct Match必须同时通过五维一致性：

1. Core Business Problem
2. Core Action
3. Analysis / Decision Object
4. Output Type
5. Ownership / Responsibility Context

只有方法相似，不足以构成Direct Match。

## 高异质入口（Heterogeneous Application Unit）

当一个投递入口覆盖差异显著的内部方向时，Runtime必须区分`best_direction_fit`与`application_unit_fit`。Portfolio Ranking使用后者，并显式记录Direction Selection与Direction Allocation Risk。
