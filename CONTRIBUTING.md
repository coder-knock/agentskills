# 贡献指南

感谢您对 Agent Skills 的兴趣！本文档将说明如何贡献以及不同类型的反馈应提交到哪里。

## 贡献类型

### 文档改进
我们欢迎对[文档站点](https://agentskills.io)的改进——包括错别字修复、清晰度提升、更好的示例和新指南。文档位于 `docs/` 目录中。

### Bug 报告
在规范、文档或参考库中发现 Bug？请[提交 Issue](https://github.com/agentskills/agentskills/issues)。

### 提案、问题和反馈
有功能请求、规范设计问题或一般性反馈？请[发起讨论](https://github.com/agentskills/agentskills/discussions)。我们使用 Discussions 来处理提案和开放式对话，并将 Issues 保留给具体的 Bug 和问题。

提案应解决您遇到的实际实现挑战，而非理论上的担忧。请向我们展示您面临的问题以及您的提案如何解决它。

我们对规范的添加保持高标准——向规范添加内容比删除内容容易得多。每个新功能都会增加所有实现者必须理解和支持的复杂性。如有疑虑，就不要添加。

> [!NOTE]
> **不确定应该发布在哪里？** 默认选择 [Discussions](https://github.com/agentskills/agentskills/discussions)。如果结果发现是 Bug，我们会将其转换为 Issue。

### 生态系统列表和 Logo 申请
如果您的产品或平台已实现 Agent Skills 兼容性，您可以申请被列入 [agentskills.io](https://agentskills.io)。您的产品必须公开可用，并且能够当前即可发现和执行技能——我们不列出仅宣布有意支持 Skills 或仍处于私有测试阶段的产品。

提交 Pull Request 时需包含：

1. **Logo 文件** — 优先使用 SVG；PNG 也可接受（最小 200×200 像素）。提供浅色和深色两种变体，并遵循 `docs/images/logos/` 中的现有格式。
2. **客户端条目** — 将您的产品添加到 [`docs/snippets/clients.jsx`](docs/snippets/clients.jsx) 数组中。
3. **产品信息** — 在您的 PR 描述中包含产品名称、产品链接以及展示 Skills 实现的文档链接。

我们可能会要求提供演示或截图来验证实现。Logo 申请由 Anthropic 团队审核。

### 参考库（`skills-ref/`）
我们仍在确定参考库的方向，目前不接受代码贡献。Bug 反馈仍可通过 [Issues](https://github.com/agentskills/agentskills/issues) 提交，一般反馈可通过 [Discussions](https://github.com/agentskills/agentskills/discussions) 提交。

### 暂不接受的贡献类型
为了在早期阶段保持项目聚焦，我们目前不接受：

- **技能提交** — 我们不维护社区技能目录。未来可能会改变。
- **重大架构变更** — 我们仍在迭代核心规范。大规模重新设计为时过早。

如果您不确定您的贡献是否合适，请在投入大量精力之前先发起[讨论](https://github.com/agentskills/agentskills/discussions)。

## 开发环境配置

### 文档站点
文档站点使用 [Mintlify](https://mintlify.com/) 构建。

```bash
# 安装 Mintlify CLI
npm i -g mint

# 从 docs/ 目录运行本地开发服务器
cd docs && mint dev
```

本地预览将在 `http://localhost:3000` 可用。

## 提交更改

1. [Fork 本仓库](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo)
2. 为您的更改创建一个分支
3. 进行更改并在本地验证其正常工作
4. 提交 Pull Request

保持 PR 聚焦于一个逻辑更改，并关联任何相关的 Issue。

## AI 辅助贡献

> [!IMPORTANT]
> 如果您使用**任何形式的 AI 辅助**来贡献 Agent Skills，必须在 Pull Request 或 Issue 中披露。

我们欢迎并鼓励使用 AI 工具来帮助改进 Agent Skills。许多有价值的贡献都借助 AI 辅助完成了代码生成、Issue 检测和文档编写。

也就是说，如果您在使用任何形式的 AI 辅助（例如 Claude Code、ChatGPT 等智能体）为 Agent Skills 做出贡献，**必须在 Pull Request 或 Issue 中披露这一点**，同时说明 AI 辅助的程度（例如：文档注释还是代码生成）。

如果您的 PR 回复或评论是由 AI 生成的，也请披露这一点。

例外情况：微不足道的间距或错别字修复无需披露。

披露示例：
> 本 PR 主要由 Claude Code 编写。

或更详细的披露：
> 我咨询了 ChatGPT 来理解代码库，但解决方案完全由我手动编写。

未披露 AI 辅助行为首先是对 PR 另一端的人工审核人员的不尊重，同时也使得难以确定应对贡献应用多少审查力度。

### 我们期望的内容
提交 AI 辅助贡献时，请确保包含：

- **明确披露 AI 使用** — 透明地说明 AI 使用情况和使用程度
- **人工理解** — 您个人理解这些更改的作用
- **明确的理由** — 能够解释为什么需要此更改以及它如何符合 Agent Skills 的目标
- **具体证据** — 包含展示改进的测试用例、场景或示例

### 我们会关闭的内容
我们保留关闭似乎未遵循披露政策的提交的权利。

## 许可证
通过贡献，您同意您的贡献将根据 [Apache License 2.0](LICENSE)（适用于代码和规范文件）和 [CC-BY 4.0](docs/LICENSE)（适用于文档）进行许可。
