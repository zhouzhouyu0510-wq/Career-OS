# Quick Start｜不会YAML，也能快速完成首轮配置

如果现有简历和经历材料比较完整，可以先在约20–30分钟内完成首轮配置；经历较多或责任边界需要进一步确认时，可分批完成。
你不需要先自己填写所有模板。最简单的方法是把“原始材料 + 对应模板 + 本页Prompt”一起交给AI，让AI先提取事实、标记缺口并追问；你确认后，它再按模板输出完整Markdown。

## Step 0｜准备一个AI对话或工作区

可以使用支持文本输入或文件读取的通用AI工具。如果工具支持Project、Workspace等持续保存文件的方式，可以建立一个长期的`My Career OS`工作区；如果不支持，普通单次对话也可以完成Quick Start。

不要假设AI会永久记住资产。**你自己保存的Markdown文件始终是可控的事实资产副本。**

## Step 1｜AI帮你建立Candidate Profile

### 你需要提供

- 当前简历；
- 你对求职方向、偏好与明确不偏好的简单描述；
- [Candidate Profile模板](templates/candidate_profile_template.md)。

### 复制给AI

```text
我正在建立Career OS Candidate Profile。

我已经提供：
1. Candidate Profile模板；
2. 我的简历和/或求职背景说明。

请先不要替我完善人设，也不要根据专业或经历推测能力和偏好。

第一步，请按照模板提取目前能确认的信息；
第二步，把无法确认但会影响求职判断的信息列成问题向我确认；
第三步，等我回答后，再严格按照模板输出一份完整Markdown。

对无法确认的信息保留“待确认”，不得自行补全。最终输出中不要省略模板栏目。
```

### 你最后应该得到

一份完整的`candidate_profile.md`。保存前逐项核对能力、技能边界和偏好。

## Step 2｜AI帮你逐段整理Experience

### 你需要提供

- 当前简历中这段经历的描述；
- 你对这段经历的回忆，或有权使用且已经脱敏的材料；
- [Experience模板](templates/experience_template.md)。

**一次处理一段经历。** 不建议第一轮把十段经历全部交给AI。

### 复制给AI

```text
我正在建立Career OS Experience资产。我已提供一段经历的简历描述、回忆或脱敏材料，以及Experience模板。

请先不要写简历Bullet，也不要包装表达。第一轮只输出：
1. 初步事实：背景、任务、个人行动、Deliverable、项目结果和个人贡献；
2. 个人责任边界（Ownership），并区分项目结果与个人结果；
3. 待确认问题。

最终决策权、数字或责任范围无法确认时必须提问或标记“待确认”，不得推断。等我回答后，再严格按照模板输出完整Experience Markdown，不省略栏目。
```

### 你最后应该得到

建议分别保存为`experience_01.md`、`experience_02.md`、`experience_03.md`。文件名只是建议，不是强制Schema。

## Step 3｜AI帮你提取核心Evidence

### 你需要提供

- 已经由你确认的Experience Markdown；
- [Evidence模板](templates/evidence_template.md)。

### 复制给AI

```text
请只从我已经确认的Experience Markdown中，提取值得用于Job Fit、简历或面试的重要Claim，并严格按照Evidence模板整理。

每条必须记录Fact、Ownership、Result Scope、Source、Confidence和External-safe。无法从已确认Experience确定的字段请标记“待确认”，不得推断；项目结果不得自动写成个人结果，没有依据的数字和能力不得补充。

请先列出候选Evidence及待确认问题；等我确认后，再输出完整Evidence Markdown。不需要为每个日常任务建立Evidence。
```

### 你最后应该得到

一组只覆盖高价值Claim的Evidence记录。所有重要字段必须由你确认。

## Step 4｜AI帮你整理Preference & Constraints

### 你需要提供

- 你对城市、工作内容、行业、稳定性、成长等选择的自然语言描述；
- [Preference & Constraints模板](templates/preference_constraints_template.md)。

### 复制给AI

```text
请根据我的自然语言描述和Preference & Constraints模板，整理我的求职偏好与约束。

请先区分：明确偏好、可以接受、Hard Constraint和Trade-off；发现矛盾或条件不清时先向我追问。你可以帮助我看见取舍，但不能替我决定价值观、最低条件或最终选择。

等我确认后，再按模板输出完整Markdown；无法确认的内容保留“待确认”。
```

### 你最后应该得到

一份`preference_constraints.md`，其中偏好、硬约束和可接受交换清楚分开。

## Step 5｜保存最低可运行资产

推荐但不强制的个人目录：

```text
my-career-os/
├── candidate_profile.md
├── experiences/
│   ├── experience_01.md
│   ├── experience_02.md
│   └── experience_03.md
├── evidence/
└── preference_constraints.md
```

不需要建立几十个文件，也不需要手写YAML。Story可以等到准备面试时再补充：需要时使用[Story模板](templates/story_template.md)。

## Quick Start完成检查

- [ ] 我有一份本人确认的Candidate Profile；
- [ ] 我逐段整理了3–5段重要经历；
- [ ] 高价值事实已区分Fact、Ownership与Result Scope；
- [ ] 我记录了Preference、Hard Constraint与Trade-off；
- [ ] 所有待确认项都没有被AI自动升级为事实。

> **资产已经准备好了？下一步直接看：[如何真正运行Career OS](how_to_run.md)。**

继续阅读：[Full Setup](full_setup.md)｜[AI协作通用方法](ai_collaboration_guide.md)｜[返回首页](README.md)
