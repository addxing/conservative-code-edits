---
name: conservative-code-edits
description: Apply conservative project coding rules before editing source code. Use when Codex needs to modify code, resources, configuration, tests, or documentation in an existing software project and should keep changes minimal, preserve architecture and style, avoid unrelated refactors, identify risky shared-code edits, and respect dark-mode color adaptation.
---

# Conservative Code Edits

## 中文说明

这是一个面向 Codex/AI 编程代理的保守代码修改守则 Skill。它适合在已有项目中进行代码、资源、配置、测试或文档修改时使用，目标是让代理尽量保持改动范围小、风格一致、风险可控。

核心原则：

- 使用最小必要改动完成任务。
- 只修改与任务直接相关的文件。
- 默认保持项目现有架构、交互逻辑、状态流转、模块职责、命名风格和实现模式。
- 不做无关重构、格式化、优化或清理。
- 修改公共基础代码前，先说明影响范围并等待确认。
- 项目支持深色模式时，不新增硬编码固定 UI 色值，优先使用已有动态颜色资源或主题属性。

优先级：

1. 用户明确要求
2. 项目硬性规则
3. 编码原则

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
