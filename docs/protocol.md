# Career Workbench protocol

## Canonical files

Each workspace contains six YAML documents. Their schemas use JSON Schema Draft 2020-12 and reject unknown top-level fields.

| File | Purpose |
| --- | --- |
| `profile.yaml` | Identity, contact channels, location, links, and positioning |
| `experience.yaml` | Employment and contract history |
| `projects.yaml` | Professional, personal, open-source, volunteer, and study projects |
| `education.yaml` | Formal education, courses, and certifications |
| `skills.yaml` | Skills classified by context and confidence |
| `evidence.yaml` | Sources, supported claims, conflicts, and pending questions |

Every document has `schema_version: 1`. Stable record IDs use lowercase kebab-case and are referenced from `evidence.yaml`.

## Factual status

Canonical career records contain only confirmed facts. Missing or contradictory information belongs in `evidence.yaml` as a pending item or conflict. An agent may draft language from confirmed facts, but it must not strengthen scope or causality.

Evidence status values:

- `confirmed`: explicitly stated by the person or supported by an authoritative source.
- `needs-confirmation`: plausible but not sufficiently supported.
- `conflicting`: sources disagree.
- `rejected`: the person has said the claim is false or unusable.

## Context classification

Technology and project claims must identify their context. Allowed contexts are `professional`, `personal-project`, `open-source`, `study`, and `volunteer`. A skill used in study must not be presented as professional experience.

## Narrative outputs

`MASTER_RESUME.pt-BR.md` is the comprehensive primary narrative. It may be longer than an application resume. `MASTER_RESUME.en.md` is an optional factual translation, not an independently enhanced version.

Narrative documents must not expose evidence IDs, confirmation markers, source paths, or internal questions.

## Vacancy-specific derivatives

A targeted resume may have an adjacent `.selection.yaml` file conforming to
`schemas/resume-selection.schema.json`. This derivative is not a seventh
canonical career file. It records the vacancy requirement map and exact
canonical records selected for rendering, plus gaps and omissions that must
remain outside the publishable resume.
