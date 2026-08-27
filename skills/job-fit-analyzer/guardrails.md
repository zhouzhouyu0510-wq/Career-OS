# 风险检查（Guardrails）

- 遗漏硬门槛（Eligibility Overlook Risk）
- 将优先项误判为必须项（Preferred-as-Must Risk）
- 经历过度泛化（Experience Overgeneralization Risk）
- 竞争力幻觉（Competitiveness Hallucination Risk）
- 名气偏差（Prestige Bias Risk）
- 忽略Candidate偏好（Preference Override Risk）
- 偏好权重过高（Preference Overweight Risk）
- 单篇面经过拟合（External Anecdote Overfit Risk）
- 浪费有限志愿（Application Limit Waste Risk）
- 组合风险高度相关（Portfolio Correlation Risk）
- 内部分配风险（Direction Allocation Risk）
- Tier枚举漂移（Tier Enum Contract）

Questions to Verify分为`decision-critical`、`important`与`informational`。如果一个Unknown足以改变P1或Tier，推荐状态必须是`pending_verification`。
