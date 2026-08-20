# Selection plan

When the workflow needs a renderer-neutral handoff, create a YAML selection
plan conforming to `references/resume-selection.schema.json`.

- Use zero-based indexes to select exact canonical responsibility, achievement,
  contribution, and outcome strings. Do not copy those claims into the plan.
- `professional_skill_ids` may reference only skills whose canonical contexts
  contain `professional`.
- Every supporting record ID must exist in one of the six canonical files.
- An `unsupported` requirement must have no supporting record IDs and must not
  appear in the resume headline, summary, skills, or selected claims.
- Project and study evidence may be selected, but its context must remain visible.
- `omissions` explains material exclusions; it is part of the handoff report,
  never part of the resume itself.
- For `pt-BR`, include `translations` for every selected narrative field. Each
  translated claim stays bound to its canonical record ID and zero-based index.
  Preserve dates, quantities, scope, authorship, technology versions, and
  project context exactly; do not use translation to strengthen a claim.
- Technology and organization names normally remain unchanged. Translate role,
  summary, responsibility, achievement, project description, contribution,
  outcome, location, education status, and language labels whenever they would
  otherwise leak source-language prose into the rendered document.

Write the plan beside the targeted resume by default:

```text
<workspace>/tailored-resumes/<company>-<role>.<language>.selection.yaml
```
