# 字段结构（Schema）

以下字段保持英文，以便机器读取与模块间Handoff；公开Schema不包含Candidate专属路径、Family结论、Evidence ID或Template资产。

```yaml
input:
  organization: string
  role: string
  job_description: string
  location: string | null
  user_notes: string | null
  web_research: true
  output:
    editable_document: true
    portable_document: false

decision_log:
  routing:
    primary_family: valid_family_id
    secondary_family: valid_family_id | null
  selected_evidence: []
  removed_evidence: []
  tailoring_trace: []
  keyword_coverage: []
  guardrail_results: []
  version: integer
```
