# 三个运行模块（Three Runtime Modules）

Career OS将三个问题交给三个边界清晰的Runtime：

| Module | 解决的问题 | 主要输出 |
|---|---|---|
| [Job Fit Analyzer](job-fit-analyzer/README.md) | 有限投递名额应该投什么 | Eligibility、Fit、Ranking、Portfolio、Handoff |
| [Resume Tailor](resume-tailor/README.md) | 确定岗位后应该怎么投 | Evidence Selection、Tailored Resume、Decision Log |
| [Interview Coach](interview-coach/README.md) | 如何准备、训练、复盘和迁移学习 | Question Map、Answer Pack、Debrief、Learning Signals |

运行关系：

`Job Fit Analyzer → Resume Tailor → Submitted Resume → Interview Coach → Learning Signals`

本目录是用于公开展示的Runtime Specification，不是Production Skill源码，也不包含安装信息或Candidate专属路径。
