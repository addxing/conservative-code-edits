# Conservative Code Edits

[![skills.sh](https://skills.sh/b/addxing/conservative-code-edits)](https://skills.sh/addxing/conservative-code-edits)

A Codex-compatible agent skill for keeping code changes small, scoped, and project-safe.

## Install

```bash
npx skills add addxing/conservative-code-edits
```

## Usage

After installing the skill, ask Codex to use it when changing code in an existing project:

```text
Use $conservative-code-edits to make this UI change.
```

You can also rely on automatic triggering when the task involves editing project code, resources, configuration, tests, or documentation.

## What It Does

This skill guides an agent to:

- make the smallest necessary code change
- preserve existing architecture and implementation style
- avoid unrelated refactors and formatting churn
- ask before editing shared foundation code
- use dynamic color resources when a project supports dark mode

## Files

- `SKILL.md` - the skill instructions
- `agents/openai.yaml` - Codex UI metadata
- `LICENSE.txt` - Apache 2.0 license
