Synthetic Demo｜完全虚构示例，不使用任何真实候选人、企业、投递或面试数据。

# 3分钟端到端演示

本目录通过完全虚构的**候选人A（Candidate A）**与**D公司（Company Delta）**，演示Career OS如何把“认识候选人、选择岗位、定制简历、准备面试和迁移学习”连接成一条可追溯的工作流。

所有人物、公司、岗位、数字、Evidence、简历与面试均为Synthetic，不映射任何真实候选人或招聘数据。默认路径全部为Human-readable Markdown，无需理解YAML或Schema。

## 3分钟阅读路径

### Step 1｜认识候选人

→ [候选人A画像](candidate/candidate_a_profile.md)

先了解候选人的教育背景、经历组合、工作偏好与技能边界。

### Step 2｜查看候选人Evidence

→ [候选人A Evidence Pool](candidate/candidate_a_evidence.md)

查看10条事实Evidence，以及每条经历的个人责任（Ownership）与结果范围（Result Scope）。

### Step 3｜查看D公司四个岗位

→ [D公司岗位说明](jobs/company_delta_jobs.md)

了解四个岗位的职责、核心要求和优先条件；本场景最多可投递2个有顺序志愿。

### Step 4｜Job Fit Analyzer：选什么

1. [岗位清单](01_job_fit/job_inventory.md)
2. [逐岗匹配分析](01_job_fit/fit_analysis.md)
3. [P1 / P2志愿组合](01_job_fit/portfolio_recommendation.md)

结论保持为：P1战略分析岗、P2风险分析岗；产品分析岗不选，数据分析岗存在明确技术缺口。

### Step 5｜Resume Tailor：同一Candidate怎样生成不同简历

1. [Evidence选择与决策轨迹](02_resume_tailoring/tailored_evidence_selection.md)
2. [战略分析岗内容评审稿](02_resume_tailoring/strategy_review_draft.md)
3. [战略分析岗投递稿](02_resume_tailoring/strategy_submission_draft.md)
4. [风险分析岗投递稿](02_resume_tailoring/risk_submission_draft.md)
5. [P1 / P2定制对比](02_resume_tailoring/p1_p2_tailoring_comparison.md)

补充查看：[完整简历Decision Log](02_resume_tailoring/decision_log.md)。

### Step 6｜Interview Coach：准备、模拟与学习迁移

1. [问题地图](03_interview_coach/question_map.md)
2. [参考答案准备](03_interview_coach/answer_preparation.md)
3. [模拟与复盘](03_interview_coach/mock_debrief_example.md)
4. [跨岗位学习迁移](03_interview_coach/learning_migration.md)

## Technical / Structured Trace

以下文件保留稳定ID、Schema字段与模块Handoff，供希望核验机器可读结构的读者深入查看：

- [Candidate Profile YAML](candidate/candidate_a_profile.yaml)
- [Candidate Evidence YAML](candidate/candidate_a_evidence.yaml)
- [Company Delta Jobs YAML](jobs/company_delta_jobs.yaml)
- [P1 Resume Tailor Handoff](01_job_fit/resume_tailor_handoff_p1.yaml)
- [P2 Resume Tailor Handoff](01_job_fit/resume_tailor_handoff_p2.yaml)
