---
name: import-career-kit
description: Import a personal manifest-driven Markdown Career Kit into a separate Career Workbench workspace without modifying the source. Use when Codex needs to inspect PROFILE.md and derived resume artifacts, convert supported facts into portable YAML, classify professional versus study or project experience, report contradictions, or create a reversible migration comparison.
---

# Import Career Kit

Convert supported career facts into a separate workspace while preserving the source repository byte-for-byte.

## Establish boundaries

1. Obtain or infer an explicit source directory and destination workspace.
2. Resolve both paths and ensure they are different and neither contains the other.
3. Confirm the destination is not the public Career Workbench repository.
4. Treat the source as read-only throughout the task.
5. Read `references/import-mapping.md` before mapping content.

## Inspect the source

1. Read its repository instructions, especially privacy and source-of-truth rules.
2. Read `PROFILE.md` first when present.
3. Inspect its export manifest or index to identify relevant current artifacts.
4. Read only artifacts required to resolve or detect factual differences.
5. Record each source in destination `evidence.yaml` using relative references when possible.

## Import safely

- Create the six canonical YAML files in the destination when absent.
- Give canonical source-of-truth content precedence only when the source repository explicitly defines that rule.
- Import supported facts and preserve their meaning without stylistic inflation.
- Put disagreements in `conflicts`, ambiguous statements in `claims` with `needs-confirmation`, and missing information in `pending_questions`.
- Never promote technologies from study or personal projects to professional context.
- Do not overwrite already confirmed destination facts silently; record a conflict instead.

## Compare and report

Create `IMPORT_REPORT.md` in the destination containing source files read, records imported, conflicts, pending confirmations, content intentionally excluded, and confirmation that the source was not changed. Avoid exposing unnecessary machine-specific paths.

Do not generate a master resume unless the user also requests it or invokes the master-resume workflow.

## Verify

- Compare source Git status or file metadata before and after when available.
- Inspect destination YAML for required top-level keys and stable IDs.
- Report all destination files created or changed and all unresolved conflicts.
- Never commit, publish, or attach a remote to the private destination without explicit permission.
