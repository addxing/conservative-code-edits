# Conservative Code Edits

[![skills.sh](https://skills.sh/b/addxing/conservative-code-edits)](https://skills.sh/addxing/conservative-code-edits)

面向 Codex/AI 编程代理的保守代码修改守则 Skill，用于约束代理在已有项目中进行最小必要改动，避免无关重构，保护公共基础代码，并在支持深色模式的项目中优先使用动态颜色资源。

## 安装

```bash
npx skills add addxing/conservative-code-edits
```

## 使用方式

安装后，在需要修改已有项目代码时，让 Codex 使用这个 Skill：

```text
Use $conservative-code-edits to make this UI change.
```

当任务涉及修改项目代码、资源、配置、测试或文档时，也可以依赖 Skill 的自动触发。

## 功能说明

这个 Skill 会指导代理：

- 使用最小必要改动完成任务
- 只修改与任务直接相关的代码
- 默认沿用项目现有架构、交互逻辑、状态流转和命名风格
- 避免无关重构、格式化、优化或清理
- 修改基类、公共 UI 组件、公共工具类、网络层、存储层、主题等公共基础代码前，先说明影响范围并等待确认
- 项目支持深色模式时，禁止新增硬编码固定 UI 色值，优先使用现有动态颜色资源或主题属性

## 文件说明

- `SKILL.md` - Skill 指令
- `agents/openai.yaml` - Codex UI 元数据
- `LICENSE.txt` - Apache 2.0 许可证
