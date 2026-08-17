---
name: audit-career-facts
description: Audit Career Workbench YAML data, evidence, master resumes, translations, and supporting repositories for structural errors and unsupported career claims. Use when Codex needs to validate workspace files, find duplicate or broken references, detect professional-versus-study misclassification, compare PT-BR and English documents, identify unverified claims, or produce a prioritized factual-risk report without silently rewriting canonical data.
---

# Audit Career Facts

Audit the selected workspace without changing canonical data unless the user separately asks for fixes. Treat the audit as evidence review, not a writing exercise.

## Establish scope

1. Resolve the workspace selected by the user. Never assume an operating-system-specific path.
2. Read its repository instructions and all six canonical YAML files.
3. Read `references/audit-checklist.md` before auditing.
4. Read master resumes and other narrative outputs included in the requested scope.
5. Inspect supporting repositories only when the user provides them, the workspace cites them, or a material claim requires verification.
6. Keep private workspace content private; quote only the minimum needed to explain a finding.

## Run the audit

Perform these passes in order:

1. **Structure:** parse YAML, check `schema_version`, required files, top-level keys, stable IDs, allowed values, and date precision. Use repository JSON Schemas when available.
2. **References:** find duplicate IDs and broken `subject_ref`, `source_refs`, `related_refs`, and `evidence_refs`.
3. **Evidence:** verify that canonical claims have support, pending or conflicting claims stay outside canonical facts, and repository evidence matches the files inspected.
4. **Classification:** distinguish professional, personal-project, open-source, study, and volunteer contexts. Flag technologies whose narrative context is stronger than their evidence.
5. **Narratives:** compare each master resume with canonical YAML. Detect invented scope, omitted qualifications, unsupported metrics, stale wording, and internal evidence markers.
6. **Translation:** compare PT-BR and English structure, dates, metrics, technologies, status, and seniority. Treat stylistic differences as acceptable when factual meaning is equivalent.
7. **Privacy and portability:** detect unnecessary personal data in public artifacts, absolute machine paths, OS-dependent assumptions, secrets, and public/private boundary violations.

## Classify findings

Use the severity and category rules in `references/audit-checklist.md`. Report only actionable findings supported by concrete evidence. Do not report harmless wording differences as defects.

For each finding include:

- severity and category;
- affected file and record or section;
- observed evidence;
- factual or operational risk;
- recommended correction without applying it.

## Report results

Use `references/report-format.md`. Return the report in the conversation unless the user asks for a file. When no findings exist, state which passes ran and which sources were not independently verified.

Never mark an audit clean merely because files parse. Separate structural validity, factual consistency, evidence coverage, narrative parity, and privacy.

## Preserve boundaries

- Do not invent missing evidence to resolve a finding.
- Do not promote self-assessment, repository technology, or AI-generated code into professional experience.
- Do not treat a repository's feature set as proof that the person manually implemented every feature.
- Do not modify source repositories during verification.
- Do not edit canonical YAML, resumes, evidence, or Git history unless the user explicitly requests remediation.
- Do not commit, publish, push, or add remotes as part of an audit.
