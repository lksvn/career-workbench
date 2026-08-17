# Installing the skills

No installer or symlink is required. Copy each desired skill directory, including its `SKILL.md`, `agents/`, and resource folders, into the active Codex skills directory.

## Windows example

```powershell
Copy-Item -Recurse -LiteralPath '<repository>\skills\build-master-resume' -Destination '<skills-directory>\build-master-resume'
```

## Linux example

```sh
cp -R '<repository>/skills/build-master-resume' '<skills-directory>/build-master-resume'
```

Repeat for `import-career-kit`, `audit-career-facts`, and `tailor-resume`. Replace placeholders with local paths. Copying is preferred over linking so the installed skill is an explicit snapshot.

After copying, start a new Codex task or reload skill discovery if the host requires it.
