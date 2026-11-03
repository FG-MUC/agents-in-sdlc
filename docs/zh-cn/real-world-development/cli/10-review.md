---
title: "课程 10：回顾与后续步骤"
description: "回顾 Copilot CLI 工作流、两个拉取请求、可复用的自定义配置和更多资源。"
authors:
  - geektrainer
lastUpdated: 2026-09-29
---

你在 Tailspin Toys 的连续工作流中使用了 GitHub Copilot CLI。你：

- 准备了 Codespace、安装 Copilot CLI、探索项目并找到预先创建的筛选议题。
- 添加了星级评分，在转发的浏览器中检查结果，并手动合并了第一个拉取请求 (PR)。
- 从筛选议题开始，在 Plan 模式中确定方案，在 Autopilot 模式中实现，并在 Interactive 模式中审查。
- 使用自定义指令引导代理，然后自定义现有的 `quality-checks` 技能，并使用它运行单元测试、lint 和类型检查。
- 添加 Playwright 模型上下文协议 (MCP) 服务器，并使用它在真实浏览器中探索筛选功能。
- 创建并选择质量保障 (QA) 自定义代理，以评估需求、覆盖率、技能结果和浏览器证据。
- 审查了完整的筛选更改，并授权 Agent Merge 合并筛选 PR。
- 探索了用于管理上下文、模型、共享和选择性云端委派的斜杠命令。

## 你交付的内容

本研讨会包含两个 PR 里程碑，各自基于更新后的 `main` 创建独立分支：

1. **星级评分：** 在游戏卡片上显示现有的 `starRating` 和明确的未评分状态。
2. **筛选和质量工作流：** 实现筛选、更新指令并将其应用到功能中、自定义 `quality-checks` 报告、创建 QA 配置并包含相关测试。

从规划筛选功能到创建 PR，你始终使用同一对话和分支。为简化研讨会流程，我们将这些工作合并到一个 PR 中。

## 不同类型的验证

你通过多种方式检查代码：自动化测试、亲自在浏览器中检查，以及使用 MCP 让 Copilot 在浏览器中进行探索。`quality-checks` 技能运行单元测试、lint 和类型检查，并按新格式报告结果。创建 PR 前，QA 将这些结果与需求和测试覆盖率审查结合起来。

新增测试应解决实际缺口；QA 运行后不需要添加测试也可能是正确结果。授权合并前请审查代码和证据，并在更改后更新受影响的验证证据。

## 最佳实践

提供给 Copilot 的上下文和工具会影响它的工作。在本研讨会中，你更新了指令、自定义了技能、创建了 QA 配置并配置了 MCP 服务器。请在不同对话中复用这些自定义配置，并根据团队需求调整。指令设定标准，技能描述可重复的任务，自定义代理定义专业角色，MCP 服务器连接外部工具。请检查实际更改和工具结果，而不只是代理的摘要。

根据任务选择**模式和模型**。使用 **Plan** 在构建前思考方案，使用 **Interactive** 跟进范围明确的更改，使用 **Autopilot** 处理边界清晰的任务。常规编辑可选择速度更快的模型，复杂工作则选择能力更强的模型。

上下文与基础设施同样重要。清晰说明要构建的内容、原因和方式，会显著影响输出结果。

## 继续探索

你已完成核心工作流。还可以了解一些 Copilot CLI 功能：

- 使用 `/review` 请求代码审查代理分析更改。
- 使用 `/rubber-duck` 讨论问题并获得另一种观点。
- 使用 `/fleet` 并行协调独立子任务。
- 使用 `/worktree` 隔离单独任务。
- 使用 `/delegate` 将任务发送给 Copilot 云代理。

## 后续步骤

提高工具使用能力的最佳方法就是持续使用它。将它用于生产代码、个人项目，或那个你多年来一直想构建的小应用。与团队分享经验，也向团队成员学习。最后，别忘了继续查看文档。

如果要从终端扩展 Tailspin Toys，请继续学习可选的 [Foundry Backer Concierge 系列][foundry]。若要比较其他开发环境，请探索 [VS Code 研讨会][vscode]、[GitHub Copilot 应用研讨会][app]或 [Copilot 云代理研讨会][cloud]。

## 资源

- [关于 GitHub Copilot CLI][about-cli]
- [Copilot CLI 命令参考][cli-reference]
- [自定义 Copilot CLI][customize-cli]
- [使用 Copilot CLI 管理拉取请求][manage-prs]

[previous-lesson]: ../9-cli-power-tools/
[foundry]: ../8-foundry-agent/
[vscode]: ../../vscode/
[app]: ../../app/
[cloud]: ../../cloud/
[about-cli]: https://docs.github.com/copilot/concepts/agents/about-copilot-cli
[cli-reference]: https://docs.github.com/copilot/reference/copilot-cli-reference/cli-command-reference
[customize-cli]: https://docs.github.com/copilot/how-tos/copilot-cli/customize-copilot
[manage-prs]: https://docs.github.com/copilot/how-tos/copilot-cli/use-copilot-cli/manage-pull-requests
