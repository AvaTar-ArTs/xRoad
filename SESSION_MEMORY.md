# Session Memory

This note captures the current state so we can resume quickly later.

## Git ignore context
- Global ignore file exists at `~/.gitignore_global`
- Git is configured to use it: `core.excludesfile = /Users/steven/.gitignore_global`
- `~/.config/git/ignore` exists (currently minimal)
- Repo `.gitignore` is present and kept small/project-specific

## Latest setup changes in this repo
- Added `.editorconfig` and `.gitattributes` for consistent formatting and line endings
- Added formatter/linter configs:
  - `.prettierrc.json`, `.prettierignore`
  - `.markdownlint.json`
  - `.ruff.toml`
  - `.shellcheckrc`, `.shfmt.conf`

## Pending choice
- Whether to merge a curated subset of global ignores into the repo `.gitignore`

