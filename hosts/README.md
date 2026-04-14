# Prompt Master Host Packages

These host packages make Prompt Master easier to install in environments with different customization primitives.

## Canonical source

- `SKILL.md` is the canonical behavior file.
- `references/` contains optional support material.
- Files under `hosts/` are wrappers and install surfaces, not the source of truth.

## Packages

### Claude

- Folder: `hosts/claude/`
- Use when the host has a native skill import flow or a skills directory.
- Recommended artifact: the full repository folder, keeping `SKILL.md` at the root.

### GitHub Copilot / VS Code

- Folder: `hosts/copilot/`
- Use when the host supports reusable prompt files.
- Recommended artifact: `prompt-master.prompt.md`

### Generic agents and model runtimes

- Folder: `hosts/generic/`
- Use when the host accepts a system prompt, developer prompt, or preset.
- Recommended artifact: `PROMPT_MASTER_SYSTEM.md`

## Packaging policy

- Keep the root skill host-agnostic.
- Keep wrappers thin and task-oriented.
- If behavior changes, update `SKILL.md` first and then sync host wrappers only where needed.