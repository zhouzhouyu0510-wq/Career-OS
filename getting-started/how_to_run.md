# 如何真正运行Career OS｜从事实资产到第一次结果

## 需要安装Career OS吗？

**不需要。**

当前Career OS Public Edition V1提供的是**Public Runtime Specification**，不是一键安装的软件或Agent Skill。Runtime可以理解为“告诉AI这个模块应该怎样工作的一套操作规则”，其中包含流程、Schema、Guardrails和输出约定。

仓库中的`skills/`目录名称不代表Public Edition V1已经是可一键安装的Skill Package。当前使用方式是：

> **我的事实资产 + 当前任务材料 + 对应Public Runtime Specification = AI执行Career OS**

当前V1使用可复用的AI工作流规范；可安装Skill形式属于后续版本方向，本轮未实现。

## 要下载整个GitHub仓库吗？

不需要每次把整个仓库上传给AI。你可以选择以下方式。

### 方法A｜第一次下载Repo到本地

在GitHub选择`Code → Download ZIP`并解压保存。以后运行某个模块时，只提供：

- 自己与当前任务相关的事实资产；
- 本次JD、实际提交Resume或其他任务材料；
- 对应`skills/<module>/`内的Runtime及配套规则。

Demo、三张图片、screenshots、无关docs以及另外两个模块的Runtime都不需要上传。

### 方法B｜让AI读取GitHub链接

如果你使用的AI工具能够可靠读取网页或GitHub文件，可以提供对应Runtime入口链接。但不要假设所有AI都能完整读取链接；无法确认时，优先直接提供Runtime文件。

## 两种长期使用方式

### 方法1｜推荐：长期AI工作区 / Project

如果你使用的AI工具支持持续保存项目文件，可以建立`My Career OS`工作区，长期放置Candidate Profile、Experience、Evidence、Preference、Story和三个Public Runtime Specification。以后每次新投递主要补充新JD、Job Fit结果、实际提交Resume或面试记录。

不要把AI的“记忆”当成事实数据库。**用户自己保存的Markdown资产仍然是可控的Source of Truth副本。**每次运行前应确认AI能访问最新版资产。

> 将真实求职资产交给任何AI工具前，请根据所使用服务的隐私政策和自己的材料权限判断是否适合上传；公司内部、客户、未公开项目或其他敏感材料应优先脱敏或只保留事实摘要。

### 方法2｜单次对话

普通新对话也可以运行。每次只提供：

```text
相关个人资产
+ 当前任务材料
+ 本次需要的Public Runtime Specification
```

开新对话或更换AI工具时，需要重新提供必要文件或上下文。

## 第一次运行Job Fit Analyzer

Runtime入口：[Job Fit Analyzer Runtime](../skills/job-fit-analyzer/runtime.md)

同一模块建议一并提供：[Schema](../skills/job-fit-analyzer/schema.md)、[Guardrails](../skills/job-fit-analyzer/guardrails.md)和[Handoff Contract](../skills/job-fit-analyzer/handoff_schema.yaml)。

### Step 1｜准备输入

- Candidate Profile；
- 主要Experience / Evidence；
- Preference & Constraints；
- 本次招聘公告或JD；
- Job Fit Analyzer Public Runtime Specification及上述配套规则。

### Step 2｜只给当前模块需要的材料

本次不需要提供Resume Tailor或Interview Coach Runtime。

### Step 3｜复制Launch Prompt

```text
我希望使用Career OS的Job Fit Analyzer分析这次招聘。

我已经提供：
1. 我的Candidate Source of Truth相关资产；
2. 本次招聘公告 / JD；
3. Job Fit Analyzer Public Runtime Specification。

请先完整读取这些材料，再严格按照Runtime、Schema和Guardrails执行。

要求：
- Candidate事实只能来自我已经提供并确认的事实资产；
- 不得根据JD反向创造我没有的能力或经历；
- 明确区分Candidate→Job Fit和Job→Candidate Fit；
- 关键信息不足时请标记Unknown或向我确认；
- 如果存在多个岗位和投递名额限制，请给出有顺序的岗位组合建议；
- 最终用自然中文解释结论，并保留必要的Evidence追溯。

请先检查当前输入是否足够，再开始分析。
```

### Step 4｜你会得到什么

输出会解释能否投（Eligibility）、事实与岗位要求的覆盖程度（Candidate→Job Fit）、现实竞争力、岗位是否符合你的偏好（Job→Candidate Fit）、主要Gap，以及有限名额下的Portfolio Recommendation。

## 第一次运行Resume Tailor

Runtime入口：[Resume Tailor Runtime](../skills/resume-tailor/runtime.md)

同一模块建议一并提供：[Schema](../skills/resume-tailor/schema.md)、[Guardrails](../skills/resume-tailor/guardrails.md)和[Output Contract](../skills/resume-tailor/output_contract.md)。

### Step 1｜准备输入

- Candidate Source of Truth；
- 目标JD；
- Job Fit结果或Handoff（如有）；
- Resume Tailor Public Runtime Specification及上述配套规则。

### Step 2｜复制Launch Prompt

```text
我希望使用Career OS的Resume Tailor为这个目标岗位定制简历。

我已经提供：
1. 我的Candidate Source of Truth；
2. 目标岗位JD；
3. Job Fit结果或岗位选择依据；
4. Resume Tailor Public Runtime Specification。

请先检查输入是否充分，再严格按照Runtime、Schema和Guardrails执行。

请先生成Content-rich Review Draft供我审核，不要直接压缩成最终投递版。

所有Bullet都必须能够追溯到已有Evidence。

可以改变：
- Evidence优先级；
- 经历排序；
- 岗位语言；
- 内容压缩方式。

不得改变：
- Candidate Fact；
- 数字；
- Ownership；
- Result Scope；
- 未确认的技术能力。

等我确认Review Draft后，再进入Submission Draft。
```

### Step 3｜保存实际投递版本

Review Draft是审核中间稿，Submission Draft是准备投递的版本。最终真正提交给岗位的简历应单独保存为**Actual Submitted Resume**，因为Interview Coach需要读取实际提交版本，而不是中间草稿。

## 第一次运行Interview Coach

Runtime入口：[Interview Coach Runtime](../skills/interview-coach/runtime.md)

同一模块建议一并提供：[Schema](../skills/interview-coach/schema.md)、[Guardrails](../skills/interview-coach/guardrails.md)和[Learning Contract](../skills/interview-coach/learning_contract.md)。

### Step 1｜准备输入

- Candidate Source of Truth；
- 目标JD；
- Actual Submitted Resume；
- 关键Evidence；
- 已确认Story（如有）；
- Interview Coach Public Runtime Specification及上述配套规则。

### Step 2｜复制Launch Prompt

```text
我希望使用Career OS的Interview Coach准备这个岗位的面试。

我已经提供：
1. Candidate Source of Truth；
2. 目标岗位JD；
3. 实际提交的Resume；
4. 已确认的Story和Evidence（如已有）；
5. Interview Coach Public Runtime Specification。

请先检查输入是否完整，再进入面试准备。

请区分：
- 必须准备；
- 建议准备；
- 时间允许再准备。

所有参考答案只能基于已有Candidate Fact和Evidence；
预测问题不能冒充真实面经；
不得为了回答完整而创造新的经历、数字或Ownership；
如果后续进行Mock或Debrief，也不得因为一次模拟自动修改Candidate事实。
```

## 一个完整但很短的例子

假设你想比较D公司的4个岗位，只需要给AI：

```text
my-career-os/candidate_profile.md
my-career-os/experiences/
my-career-os/evidence/
my-career-os/preference_constraints.md
D公司岗位JD
Job Fit Analyzer Runtime及配套规则
```

然后复制上面的Job Fit Launch Prompt。你不需要上传Synthetic Demo全文，也不需要提供另外两个Runtime。

## 下一次怎么继续用？

### 同一个AI工作区

如果个人资产和Runtime已经保存在工作区，下一次通常只需新增JD或当前任务材料。但在运行前，应确认AI确实能访问最新版事实资产和Runtime。

### 新对话或新AI工具

重新提供“当前任务需要的事实资产 + 对应Public Runtime Specification + 当前任务材料”。不存在“安装一次以后所有AI都会自动记住”的保证。

### 资产发生变化

出现新经历、新证据、事实修正或新的用户确认时，先更新Candidate Source of Truth，再运行下游模块。不要只修改某份简历而不更新事实资产。

## FAQ

### Q1｜我需要会YAML吗？

不需要。Markdown即可开始；YAML只是可选的结构化形式。

### Q2｜我需要安装Career OS吗？

Public Edition V1不需要安装，也不是一键安装Skill。

### Q3｜我要把整个GitHub仓库上传给AI吗？

不需要。只提供当前任务有关的事实资产、任务材料与对应Runtime。

### Q4｜AI会自动永久记住我的资产吗？

不要假设会。个人保存的事实资产文件才是可控副本。

### Q5｜我每换一个岗位都要重新建资产吗？

不需要。同一Source of Truth可以重复使用，通常只改变当前JD和下游选择。

### Q6｜什么时候需要更新事实资产？

新经历、新证据、事实修正或用户确认发生变化时更新。

继续阅读：[Quick Start](quick_start.md)｜[Full Setup](full_setup.md)｜[返回Getting Started首页](README.md)
