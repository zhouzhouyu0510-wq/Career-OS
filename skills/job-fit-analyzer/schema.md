# 字段结构（Schema）

以下字段保持英文，以便机器读取与模块间Handoff；中文说明不改变field name、enum或ID contract。

```yaml
input:
  mode: multi_role | single_role
  organization: string
  recruiting_cycle: string | null
  notice_or_job_text: string
  application_constraints:
    max_roles: integer | null
    ordered_preferences: boolean | null
    submission_editable: boolean | null
  user_notes: string | null
  web_research: true

application_unit:
  job_id: string
  title: string
  location: string | null
  eligibility: eligible | conditional | ineligible | unknown
  heterogeneity:
    level: low | medium | high
    direction_selection: true | false | unknown
    allocation_risk: low | medium | high | unknown
  best_direction_fit: string | null
  application_unit_fit: string

ranking:
  tier: S | A | B | C | D | X
  rank_within_tier: integer | null
  recommendation_status: stable | pending_verification
```

未知字段保持`unknown`。只有JD明确写为必须时，Preferred Qualification才进入Hard Gate。
