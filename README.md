# Conservative Code Edits

[![skills.sh](https://skills.sh/b/addxing/conservative-code-edits)](https://skills.sh/addxing/conservative-code-edits)

An agent skill for keeping code changes small, scoped, and project-safe. Works with any AI coding tool that supports skills.

## Install

```bash
npx skills add addxing/conservative-code-edits
```

## Usage

Select this skill using your tool’s skill mechanism, or ask for it by name. Invocation syntax and automatic activation depend on the tool.

After installing the skill, ask your AI coding tool to use it when changing code in an existing project:

```text
Use the conservative-code-edits skill to make this UI change.
```

If your tool supports automatic skill activation, it may select this skill when a task involves editing project code, resources, configuration, tests, or documentation.

## What It Does

This skill guides an agent to:

- make the smallest necessary code change
- preserve existing architecture and implementation style
- avoid unrelated refactors and formatting churn
- ask before editing shared foundation code
- use dynamic color resources when a project supports dark mode

## Files

- `SKILL.md` - the skill instructions
- `LICENSE.txt` - Apache 2.0 license
