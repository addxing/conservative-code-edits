---
name: conservative-code-edits
description: Enforce a conservative strategy when modifying existing project code: minimize changes, preserve existing architecture and style, avoid unrelated refactors and shared-code risks.
---

## Coding Principles

- Use the smallest necessary change to complete the task; modify only code directly related to the task.
- By default, preserve the existing architecture, interaction logic, state flow, module responsibilities, naming style, and implementation patterns.
- Do not perform unrelated refactors, formatting, optimizations, or cleanups; do not delete pre-existing unrelated code.
- Assess the impact area before modifying, and verify the result after modifying whenever practical.
- Prioritize simplicity; avoid unnecessary complexity and bloated abstractions.

## Project Hard Rules

- Before modifying architecture, interaction logic, state flow, module responsibilities, or core implementation style, you must first explain the reason, impact area, and risk, then wait for confirmation.
- Before modifying shared foundation code, you must first list the impact area and wait for confirmation. Shared foundation code includes: base classes, common UI components, common utilities, network layer, storage layer, routing, logging, analytics, permissions, theme infrastructure, etc.
- If the project supports dark mode, hardcoding fixed UI colors is prohibited; colors must adapt dynamically and prioritize existing color resources.

## Priority

Explicit user request > Project hard rules > Coding principles.
