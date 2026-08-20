# Installing the skills

No installer or symlink is required. Copy each desired skill directory, including its `SKILL.md`, references, assets, and any useful host adapters, into the skills directory recognized by your agent.

The canonical interface is `SKILL.md`. Directories such as `agents/` contain optional platform metadata and may be ignored by hosts that do not use them. If an agent does not support directory-based skills, its user can still load or adapt the Markdown instructions through that agent's supported mechanism.

## Windows example

```powershell
Copy-Item -Recurse -LiteralPath '<repository>\skills\build-master-resume' -Destination '<skills-directory>\build-master-resume'
```

## Linux example

```sh
cp -R '<repository>/skills/build-master-resume' '<skills-directory>/build-master-resume'
```

Repeat for `import-career-kit`, `audit-career-facts`, and `tailor-resume`. Replace placeholders with paths appropriate to the selected host. Copying is preferred over linking so the installed skill is an explicit snapshot.

After copying, reload skill discovery or restart the agent session if the host requires it.
