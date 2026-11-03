---
title: "课程 9：GitHub Copilot CLI 斜杠命令"
description: "探索用于管理上下文、选择模型、共享会话和选择性委派云代理的斜杠命令。"
authors:
  - geektrainer
lastUpdated: 2026-09-18
---

与其他优秀的 CLI 工具一样，GitHub Copilot CLI 提供了许多斜杠命令供你使用。这些命令提供高级功能、后台信息和其他配置选项。你已经使用过 `/diff`、`/mcp`、`/skills`、`/agent` 和 `/pr` 等命令。接下来了解一些其他实用命令。

在本课程中，你将：

- 使用 `/context` 和 `/compact` 了解 Copilot 如何管理对话上下文。
- 使用 `/model` 查看可用模型。
- 了解 `/share` 如何导出或共享会话。
- 探索用于并行工作、工作树和委派到云代理的可选命令。

## 场景

你已完成 CLI 核心工作流。现在了解其他功能，包括管理上下文、切换模型、共享会话，以及选择是否将工作委派给 [Copilot 云代理][about-cloud-agent]。

## 探索 Copilot CLI 上下文

处理大型或复杂任务时，可能会达到模型的最大上下文窗口。Copilot CLI 会在需要时自动压缩对话，你也可以使用斜杠命令检查或压缩上下文。

1. 返回 Codespace；如果 Copilot CLI 尚未打开，请从仓库根目录启动。
2. 输入：

   ```plaintext
   /context
   ```

3. 查看模型、当前令牌用量，以及上下文在系统指令、工具、消息和空闲空间之间的分配情况。
4. 压缩对话：

   ```plaintext
   /compact
   ```

5. 再次输入 `/context` 并比较结果。如果对话本来就很短，变化可能不明显。

> [!NOTE]
> 随着上下文窗口逐渐填满，Copilot CLI 会自动压缩上下文。若要自行选择压缩时机，请使用 `/compact`。如果要切换到无关任务并开始全新对话，请使用 `/clear` 或 `/new`。

## 选择模型

不同模型各有优势，不同开发者也有各自偏好。Copilot CLI 可以列出模型并让你选择要使用的模型。

1. 输入：

   ```plaintext
   /model
   ```

2. 查看可用模型和用量信息。
3. 保留当前模型、选择其他模型，或按 <kbd>Esc</kbd> 关闭列表。

## 共享会话

团队合作和分享经验有助于每个人更好地使用 AI 工具。`/share` 命令可以将会话导出为 Markdown 或 HTML 文件、创建可共享链接，或发布 GitHub gist。

1. 输入 `/help`，查看当前版本中的 `/share` 选项。
2. 如果要共享此会话，请选择合适的目标，例如使用 `/share file` 导出本地 Markdown 文件。
3. 发送或发布导出内容前，请先进行审查。会话导出可能包含提示、回复和项目详情。

发布链接或 gist 是可选操作。不要发布团队无意共享的仓库或对话内容。

## 可选：扩展或委派工作

核心研讨会已完成。Copilot CLI 还提供了适用于大型任务的命令：

- `/fleet` 可以将独立子任务分配给多个子代理并行执行。
- `/worktree` 可以为单独的任务创建隔离的 Git 工作树。
- `/delegate` 可以将任务发送给 Copilot 云代理。它会异步工作，并可能创建拉取请求。

这些命令是可选的，因为它们可能创建额外工作树或远程工作。尝试前，请开始一项新的、范围明确的任务，并使用常规工作流审查结果。若要深入了解异步代理工作，请继续学习[云代理研讨会][cloud-workshop]。

## 总结和后续步骤

使用 Copilot CLI 斜杠命令可以对其进行配置、共享会话并查看后台运行情况。在本课程中，你：

- 使用 `/context` 和 `/compact` 了解 Copilot 如何管理对话上下文。
- 使用 `/model` 查看可用模型。
- 了解了 `/share` 如何导出或共享会话。
- 探索了用于并行工作、工作树和委派到云代理的可选命令。

Copilot CLI 还有许多其他斜杠命令。现在请[回顾所学内容][next-lesson]并了解后续步骤。

## 资源

- [Copilot CLI 命令参考][cli-reference]
- [Copilot CLI 中的上下文管理][context-management]
- [关于 Copilot 云代理][about-cloud-agent]

[previous-lesson]: ../8-create-pull-request/
[next-lesson]: ../10-review/
[cli-reference]: https://docs.github.com/copilot/reference/copilot-cli-reference/cli-command-reference
[context-management]: https://docs.github.com/copilot/concepts/agents/copilot-cli/context-management
[about-cloud-agent]: https://docs.github.com/copilot/concepts/agents/cloud-agent/about-cloud-agent
[cloud-workshop]: ../../cloud/
