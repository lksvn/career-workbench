# AGENTS.md

## Purpose

This repository defines a generic, public Career Workbench protocol. It must not contain real personal career data.

## Sources of truth

- `schemas/` defines the canonical data contracts.
- `templates/workspace/` provides blank workspace files.
- `skills/*/SKILL.md` defines agent workflows.
- `examples/fictional/` contains fictional fixtures only.

## Safety

- Never invent dates, metrics, responsibilities, technologies, qualifications, or outcomes.
- Keep professional work, personal projects, study, and unconfirmed claims distinct.
- Keep evidence and pending questions out of publishable resume documents.
- Never modify an import source. Write only to the explicitly selected destination workspace.
- Do not introduce absolute machine paths or OS-specific path logic.

## Editing

- Keep skills concise and use progressive disclosure through `references/`.
- Update schemas, templates, examples, and documentation together when interfaces change.
- Use only fictional data in examples and tests.
- Do not add a mandatory runtime, CLI, build step, symlink, or shell-specific installer in v1.

## Verification

- Validate each skill with the skill-creator validator.
- Check every example against the corresponding schema when a validator is available.
- Search tracked content for personal identifiers and absolute Windows or Unix home paths.
- Exercise new workflows against a temporary or disposable workspace.
