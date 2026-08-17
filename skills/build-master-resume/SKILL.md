---
name: build-master-resume
description: Build, resume, audit, or translate a comprehensive fact-checked master resume from an empty workspace or existing career documents. Use when Codex needs to interview a person progressively, structure career facts in Career Workbench YAML files, distinguish professional experience from projects or study, maintain evidence and pending questions, generate MASTER_RESUME.pt-BR.md, or produce a fact-equivalent English version on request.
---

# Build Master Resume

Build the career record progressively. Keep canonical facts in YAML, internal uncertainty in `evidence.yaml`, and publishable prose in the master resume.

## Start or resume

1. Locate the user-selected workspace. Never assume an OS-specific path.
2. If the six YAML files are absent, copy the blank files from `assets/workspace/`.
3. Read all existing workspace YAML before asking questions.
4. Read user-provided resumes or profiles as evidence, not unquestioned truth.
5. Read `references/interview.md` before conducting the interview.
6. Read `references/workspace-protocol.md` before editing YAML or generating documents.

## Interview progressively

- Conduct the interview in Portuguese unless the user chooses another language.
- Cover one topic at a time and keep questions small enough to answer conversationally.
- Begin with the earliest incomplete topic: positioning, experience, projects, education, skills, then languages and preferences.
- Do not repeat questions already answered by confirmed workspace data.
- Record supported facts after each topic so the session can resume safely.
- Put ambiguous, missing, or contradictory claims in `evidence.yaml`; do not place them in canonical records.

## Protect factual integrity

- Never invent or infer dates, metrics, scope, technologies, seniority, qualifications, responsibilities, or outcomes.
- Do not strengthen causality. “Worked on” does not mean “led,” and “helped” does not mean “delivered independently.”
- Classify each skill and project as `professional`, `personal-project`, `open-source`, `study`, or `volunteer`.
- Treat a person's explicit confirmation as evidence and record it as a `person` source.
- Ask for confirmation before promoting any pending claim into canonical YAML.

## Generate the master resume

1. Use confirmed canonical facts only.
2. Produce `MASTER_RESUME.pt-BR.md` as a comprehensive source document without a fixed page limit.
3. Include useful detail without turning routine work into exaggerated achievement language.
4. Omit internal evidence IDs, pending questions, source paths, and status markers.
5. Generate `MASTER_RESUME.en.md` only when requested.
6. Translate the Portuguese meaning faithfully; do not add claims or inflate terminology.

## Finish each session

- Summarize files changed, topics completed, unresolved questions, and the next interview topic.
- Validate YAML structure against the protocol reference and, when the repository schemas are available, the corresponding JSON Schemas.
- Never publish, transmit, or commit personal workspace data without explicit permission.
