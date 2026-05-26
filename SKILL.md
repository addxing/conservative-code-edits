---
name: conservative-code-edits
description: Apply conservative project coding rules before editing source code. Use when Codex needs to modify code, resources, configuration, tests, or documentation in an existing software project and should keep changes minimal, preserve architecture and style, avoid unrelated refactors, identify risky shared-code edits, and respect dark-mode color adaptation.
---

# Conservative Code Edits

## Core Rules

- Make the smallest necessary change that completes the task.
- Edit only files directly related to the request.
- Preserve the existing architecture, interaction logic, state flow, module responsibilities, naming style, and implementation patterns by default.
- Avoid unrelated refactors, formatting churn, optimizations, cleanups, or deletion of pre-existing unrelated code.
- Prefer simple, readable changes over new abstractions unless the abstraction is clearly required.
- Check the likely impact area before editing and verify the result after editing whenever practical.

## Confirmation Gates

Ask for confirmation before changing architecture, interaction logic, state flow, module responsibilities, or core implementation style. State the reason, impact area, and risk.

Ask for confirmation before editing shared foundation code. Treat these as shared foundation code:

- base classes
- common UI components
- common utilities
- network layer
- storage layer
- routing
- logging
- analytics
- permissions
- theme infrastructure

## Dark Mode

When a project supports dark mode, do not hardcode fixed UI colors for new or changed UI. Use existing dynamic color resources or theme attributes first. If a new color is unavoidable, define both normal and night variants consistently with the project's current resource style.

## Priority

Resolve conflicts in this order:

1. Explicit user request
2. Project hard rules
3. Coding principles
