# 字段结构（Schema）

以下field name、enum与ID保持英文，以支持版本治理、Question Provenance和模块间连接。

```yaml
question:
  question_id: string
  priority: must | should | if_time_allows
  provenance: observed_real | external_repeated | external_possible | generated_predictive | mock_generated
  target_story_ids: []

prepared_answer:
  answer_id: string
  version: string
  priority: must | should
  source_story_ids: []
  source_resume_version: string
  fact_boundary: string
  candidate_review_status: draft | reviewed | candidate_edited | superseded

real_interview_record:
  raw_record_status: draft | candidate_confirmed | frozen
  reconstruction_confidence: high | medium | low
  observable_reaction: string | null
  candidate_interpretation: string | null
  analysis_ref: string | null
```
