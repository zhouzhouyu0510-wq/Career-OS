# 输出协议（Output Contract）

每一条Tailored Claim都必须回溯到已确认Evidence，并保留Ownership与Result Scope。

Keyword状态只允许：

- **K1 Supported Keyword**：Candidate有直接Evidence支持。
- **K2 Safe Translation**：原事实支持其含义，可安全翻译为岗位语言。
- **K3 Unsupported Keyword**：只能保留为Gap，禁止写入Resume。

新Version不得覆盖历史Version。Job Fit Handoff只是推荐输入，Resume Tailor仍需重新执行Evidence Audit与Claim Guardrail。
