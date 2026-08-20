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

Each skill is self-contained in a directory with a `SKILL.md`. Install it in the skills directory recognized by your agent or load the instructions using the mechanism supported by that host.

Files under `agents/` are optional host adapters. For example, `agents/openai.yaml` provides OpenAI-specific discovery metadata but is not required by the Career Workbench protocol or by the skill instructions themselves.

## Privacy

Do not place a real workspace inside this repository. Before publishing changes, inspect tracked files and Git history for names, contact details, employers, paths, and other identifying data.

See `docs/protocol.md` for the data model and `docs/installation.md` for portable installation guidance.

Vacancy-specific renderer handoffs use the optional
`schemas/resume-selection.schema.json` contract. They remain derivative files
and do not modify the six canonical workspace documents.
Portuguese plans carry indexed, fact-equivalent narrative translations so a
renderer does not need to infer or silently strengthen canonical claims.

## License

Career Workbench is available under the [MIT License](LICENSE).
