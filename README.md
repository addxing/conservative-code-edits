# Conservative Code Edits

[![skills.sh](https://skills.sh/b/addxing/conservative-code-edits)](https://skills.sh/addxing/conservative-code-edits)

A Codex-compatible agent skill for keeping code changes small, scoped, and project-safe.

面向 Codex/AI 编程代理的保守代码修改守则 Skill，用于约束代理在已有项目中进行最小必要改动，避免无关重构，保护公共基础代码，并在支持深色模式的项目中优先使用动态颜色资源。

## Install

```bash
npx skills add addxing/conservative-code-edits
```

## What It Does

This skill guides an agent to:

- make the smallest necessary code change
- preserve existing architecture and implementation style
- avoid unrelated refactors and formatting churn
- ask before editing shared foundation code
- use dynamic color resources when a project supports dark mode

## 中文说明

这个 Skill 适合在维护已有项目时使用，尤其适用于对代码变更范围、架构稳定性和 UI 深色模式适配有明确要求的团队。

它会指导代理：

- 只修改与任务直接相关的代码
- 默认沿用项目现有架构、交互逻辑、状态流转和命名风格
- 避免无关重构、格式化、优化或清理
- 修改基类、公共 UI 组件、公共工具类、网络层、存储层、主题等公共基础代码前先说明影响范围并等待确认
- 项目支持深色模式时，禁止新增硬编码固定 UI 色值，优先使用现有动态颜色资源或主题属性

## Files

- `SKILL.md` - the skill instructions
- `agents/openai.yaml` - Codex UI metadata
- `LICENSE.txt` - Apache 2.0 license
