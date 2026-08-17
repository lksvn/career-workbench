# Career Workbench

Career Workbench is a portable, file-based protocol for building and maintaining fact-checked career data and generating career documents with AI skills.

The public project contains schemas, templates, fictional examples, and reusable skills. Personal career data belongs in a separate private workspace.

## Principles

- YAML is the canonical format for professional facts.
- Markdown is used for narrative outputs such as master resumes.
- Evidence and unresolved questions stay separate from publishable documents.
- Professional experience, personal projects, and study are never conflated.
- The protocol uses relative paths and has no required runtime or operating system.

## Workspace

Create a private directory outside this repository and copy the files from `templates/workspace/` into it. Validate its shape against the schemas in `schemas/`.

```text
<workspace>/
├── profile.yaml
├── experience.yaml
├── projects.yaml
├── education.yaml
├── skills.yaml
├── evidence.yaml
├── MASTER_RESUME.pt-BR.md
└── MASTER_RESUME.en.md
```

`MASTER_RESUME.en.md` is optional and should only be generated on request.

## Skills

- `build-master-resume`: interview, resume, and translation workflow.
- `import-career-kit`: read-only import from a manifest-driven Markdown Career Kit.
- `audit-career-facts`: structural, evidentiary, and narrative consistency audit.
- `tailor-resume`: vacancy analysis and factual targeted-resume generation.

Install a skill by copying its complete directory from `skills/` into your Codex skills directory. Common defaults are `%USERPROFILE%\.codex\skills` on Windows and `~/.codex/skills` on Linux. If `CODEX_HOME` is configured, use its `skills` subdirectory instead.

## Privacy

Do not place a real workspace inside this repository. Before publishing changes, inspect tracked files and Git history for names, contact details, employers, paths, and other identifying data.

See `docs/protocol.md` for the data model and `docs/installation.md` for portable installation guidance.
