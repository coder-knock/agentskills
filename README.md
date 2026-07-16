# Agent Skills（智能体技能）

[![Discord](https://img.shields.io/badge/Discord-Join-5865F2?logo=discord&logoColor=white)](https://discord.gg/MKPE9g8aUy)

一种标准化的方式，为 AI 智能体赋予新的能力和专业知识。

## 什么是 Agent Skills？

Agent Skills 是一种轻量级、开放的格式，用于扩展 AI 智能体的能力，提供专业知识和工作流。

其核心是，一个技能是一个包含 `SKILL.md` 文件的文件夹。该文件包含元数据（至少包括 `name` 和 `description`）和指令，告诉智能体如何执行特定任务。技能还可以捆绑脚本、参考资料、模板和其他资源。

```
my-skill/
├── SKILL.md          # 必需：元数据 + 指令
├── scripts/          # 可选：可执行代码
├── references/       # 可选：文档
├── assets/           # 可选：模板、资源
└── ...               # 任何额外的文件或目录
```

## 为什么需要 Agent Skills？

智能体的能力越来越强，但通常缺乏可靠完成实际工作所需的上下文。Skills 通过将程序性知识以及公司、团队和用户特定的上下文打包成便携式、版本控制的文件夹来解决这个问题，智能体可以按需加载这些文件夹。这为智能体提供了：

- **领域专业知识**：捕获专业知识——从法律审查流程到数据分析管道再到演示文稿格式化——作为可重用的指令和资源。
- **可重复的工作流**：将多步骤任务转化为一致、可审计的程序。
- **跨产品复用**：构建一次技能，可在任何兼容技能的智能体中使用。

## Agent Skills 如何工作？

智能体通过**渐进式披露**分三个阶段加载技能：

1. **发现**：启动时，智能体仅加载每个可用技能的名称和描述，仅足以知道何时可能相关。

2. **激活**：当任务与技能的描述匹配时，智能体将完整的 `SKILL.md` 指令读入上下文。

3. **执行**：智能体遵循指令，根据需要选择执行捆绑的代码或加载引用的文件。

完整的指令仅在任务需要时加载，因此智能体可以手边保留许多技能，而只需占用少量的上下文空间。

## 在哪里可以使用 Agent Skills？

大量 AI 工具和智能体客户端支持 Agent Skills——查看 [客户端展示](https://agentskills.io/clients) 了解其中一些！

## 入门

- **[文档](https://agentskills.io)** — 指南和教程
- **[规范](https://agentskills.io/specification)** — 格式详情
- **[示例技能](https://github.com/anthropics/skills)** — 看看可能的效果
- **[Discord](https://discord.gg/MKPE9g8aUy)** — 分享你正在构建的内容！

## 开放开发

Agent Skills 格式最初由 [Anthropic](https://www.anthropic.com/) 开发，作为开放标准发布，并已被越来越多的智能体产品采用。该标准欢迎来自更广泛生态系统的贡献——请参阅 [`CONTRIBUTING.md`](CONTRIBUTING.md) 了解如何参与。

## 许可证

本仓库中的代码根据 [Apache 2.0](LICENSE) 许可。文档根据 [CC-BY-4.0](https://creativecommons.org/licenses/by/4.0/) 许可。详见各个目录。
