---
name: tailor-resume
description: Create a vacancy-specific, ATS-friendly resume from a Career Workbench workspace without changing canonical facts. Use when Codex needs to analyze a job description, select and prioritize supported experience, adapt a professional summary and skills section, preserve study-versus-professional context, create a Portuguese or English targeted resume, or report material fit gaps and excluded keywords.
---

# Tailor Resume

Create a focused derivative resume from confirmed workspace facts. Never edit canonical YAML or master resumes as part of tailoring.

## Gather inputs

1. Resolve the selected Career Workbench workspace.
2. Obtain the complete vacancy text or a source the user has authorized Codex to inspect.
3. Determine output language from the vacancy unless the user specifies it.
4. Read all six workspace YAML files and the matching-language master resume.
5. Read `references/vacancy-analysis.md` before extracting requirements.
6. Read `references/selection-policy.md` before selecting or wording evidence.

If the vacancy text is incomplete or inaccessible, identify the missing source instead of guessing requirements.

## Analyze the vacancy

Build an internal requirement map containing:

- role purpose and seniority;
- mandatory and preferred technologies;
- responsibilities and domain context;
- language, location, contract, and work-arrangement constraints;
- explicit education or certification requirements;
- keywords that are supported, unsupported, or supported only in study/projects.

Do not treat generic recruiter language as evidence about the person.

## Select evidence

- Use confirmed canonical records only.
- Prioritize relevance, recency, depth, and supported outcomes.
- Preserve the person's actual career length and titles. Condense older roles when appropriate, but never reduce or hide years to fit a lower seniority.
- Include professional technologies only when their professional context is supported.
- Include study or personal-project technologies only when relevant and label their context visibly.
- Treat confidence as a self-assessment, not a qualification.
- Preserve AI-assisted authorship distinctions. Do not imply sole manual implementation.
- Omit personal details that the target market does not require.

When a mandatory requirement lacks support, record the gap instead of inserting the keyword into the resume.

## Draft the resume

1. Use the one-column structure in `assets/resume-template.md` as guidance.
2. Write a vacancy-specific headline and summary without changing the preferred professional identity.
3. Order skills by relevance while preserving their factual context.
4. Emphasize the most relevant responsibilities and projects; do not rewrite routine work as unsupported achievement.
5. Use direct, natural language and standard headings. Avoid tables, columns, icons, photos, progress bars, and keyword stuffing.
6. Target content that can normally fit one or two pages after export. Prefer omission of low-relevance detail over tiny typography or compressed prose.
7. Match the vacancy language. When translating, preserve meaning, dates, metrics, technology versions, and status.

## Deliver

Return the draft in the conversation unless the user asks for a file or the task already establishes a destination. For a workspace file, default to:

```text
<workspace>/tailored-resumes/<company>-<role>.<language>.md
```

Use lowercase kebab-case for the filename and `pt-BR` or `en` for language. Do not overwrite an existing targeted resume without inspecting it first.

Alongside the resume, report:

- vacancy requirements emphasized;
- relevant facts intentionally omitted for space;
- unsupported or project-only requirements;
- any claim requiring confirmation;
- expected page-density risk.

Do not create cover letters, submit applications, publish files, or modify job trackers unless separately requested.

## Verify

- Compare every resume claim against YAML and `evidence.yaml`.
- Confirm dates, numbers, URLs, seniority, employment status, and project context.
- Search for unsupported mandatory keywords accidentally introduced into prose.
- Confirm no pending question, evidence ID, source path, or internal status marker appears.
- When both language versions are produced, compare their factual meaning.
