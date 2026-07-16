# CLAUDE.md

本文件为 Claude Code (claude.ai/code) 在本仓库中工作时提供指导。该项目定义了一种开放格式，用于通过 SKILL.md 文件教 AI 智能体专业化的工作流。

## 文档

Agent Skills 文档站点定义在 `docs/` 目录中，使用 [Mintlify](https://mintlify.com/) 构建。

### 快速启动命令

```bash
# 运行本地开发服务器
npm run dev
```

本地预览可在 `http://localhost:3000` 访问

### 开发注意事项

- **导航**：定义在 `docs/docs.json` 的 `navigation.pages` 数组中
- **添加页面**：在 `/docs` 中创建新的 `.mdx` 文件，将文件名（不带扩展名）添加到导航中
- **部署**：推送到 `main` 分支后自动进行
- **故障排除**：如果页面显示 404，请确保你从包含 `docs.json` 的目录运行 `mint dev`
