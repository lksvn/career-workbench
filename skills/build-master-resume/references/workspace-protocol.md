# Workspace protocol

The workspace root contains `profile.yaml`, `experience.yaml`, `projects.yaml`, `education.yaml`, `skills.yaml`, `evidence.yaml`, `MASTER_RESUME.pt-BR.md`, and an optional `MASTER_RESUME.en.md`.

Use `schema_version: 1`. Use stable lowercase kebab-case IDs. Use ISO-like dates with the available precision: `YYYY`, `YYYY-MM`, or `YYYY-MM-DD`; use `null` when unknown. Do not guess missing precision.

Canonical YAML contains confirmed facts only. Evidence statuses are `confirmed`, `needs-confirmation`, `conflicting`, and `rejected`. Allowed contexts are `professional`, `personal-project`, `open-source`, `study`, and `volunteer`. Skill confidence may remain `null` until the person confirms it.

Before changing a record ID, update every `subject_ref`, `related_refs`, `source_refs`, and `evidence_refs` that depends on it.
