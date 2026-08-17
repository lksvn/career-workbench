# Audit checklist

## Severity

- `critical`: exposes secrets or private data publicly, or creates a materially false career claim likely to cause harm.
- `high`: unsupported employment, qualification, technology context, date, metric, authorship, or seniority claim.
- `medium`: broken evidence traceability, material PT-BR/English mismatch, stale project status, or ambiguous classification.
- `low`: portability, maintainability, completeness, or clarity issue with limited factual risk.

## Categories

Use `structure`, `reference`, `evidence`, `classification`, `narrative`, `translation`, `privacy`, or `portability`.

## Structural checks

- Six YAML files exist and use `schema_version: 1`.
- YAML parses and matches available schemas.
- IDs use lowercase kebab-case and are unique within the workspace.
- Dates use only supported precision and do not invent missing months or days.
- Enumerations use allowed contexts, evidence statuses, and confidence levels.
- Required arrays exist even when empty.

Blank templates may intentionally fail non-empty field constraints. Do not treat a blank template as a populated workspace.

## Reference checks

- Every evidence source referenced by a claim exists.
- Every evidence reference attached to a skill exists.
- Subject and related references point to real records or an explicitly documented workspace-level subject such as `profile`.
- Renamed records do not leave stale references.
- Claims do not use one vague source to support unrelated facts without explanation.

## Factual checks

- Employment dates, organizations, roles, responsibilities, technologies, and metrics have support.
- Project features do not imply manual authorship without evidence of the person's role.
- AI-assisted work distinguishes direction, testing, manual contribution, and generated implementation where known.
- Incomplete education is not described as a completed degree.
- Historical tools are not presented as current proficiency without confirmation.
- Confidence labels remain self-assessments, not formal qualifications.
- Uncertain claims remain `needs-confirmation` or `conflicting` and stay out of narrative outputs.

## Classification checks

- Professional technologies have evidence from employment or paid professional projects.
- Study and personal-project technologies remain visibly classified in narratives.
- Repository dependencies alone do not prove skill proficiency.
- SQL databases are not described as NoSQL, and frameworks are not described as languages.
- A professional project within an employment role does not automatically prove ownership of every subsystem.

## Narrative and translation checks

- Names, dates, metrics, URLs, technology versions, and status match canonical YAML.
- PT-BR and English preserve the same factual meaning and project context.
- Narrative documents contain no evidence IDs, source paths, pending questions, or internal status markers.
- Comprehensive master resumes may differ in word count; compare meaning rather than sentence alignment.
- Preferences and contact details remain current and appropriately private for the target artifact.

## Repository verification

When a cited repository is available, inspect its instructions, README, manifest, relevant source files, tests, recent history, remote URL, and worktree status as needed. Do not run destructive setup or expose `.env` contents. Report whether scope, technology, feature, recency, and authorship were verified independently or only stated by the person.
