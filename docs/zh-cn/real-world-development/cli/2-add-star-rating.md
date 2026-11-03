---
title: "课程 2：添加星级评分"
description: "使用 Copilot CLI 小幅修改游戏卡片，在转发的浏览器中检查更改，并合并你的第一个拉取请求。"
authors:
  - geektrainer
lastUpdated: 2026-09-18
---

安装 Copilot CLI 并尝试过对话后，现在可以首次修改项目了。这次只做一项小改动：游戏数据中已有星级评分，但首页的游戏卡片尚未显示评分。你将让代理显示评分、审查更改，并将其作为你的第一个拉取请求合并。

在本课程中，你将：

- 在功能分支中开始一次专注的 Copilot 对话。
- 请求代理对项目进行小幅修改。
- 使用 `/diff` 审查更改。
- 运行应用，并在转发的浏览器中确认更改。
- 创建并合并你的第一个拉取请求。

## 场景

Tailspin Toys 中的每款游戏都可以有星级评分，而且游戏详情页已显示该评分。不过，首页游戏卡片仅显示标题、类别、发行商和描述。作为热身，你将让代理在每张卡片上显示现有评分。这项小而独立的修改很适合作为首次会话的任务。

## 对话的组成

**对话**是你使用 Copilot CLI 完成任务的工作区。与 Copilot 应用不同，常规 CLI 对话使用终端当前检出的仓库和 Git 分支，而不会创建专用工作树。保存的对话可以稍后继续，而文件和分支仍作为普通 Git 状态保存在磁盘上。

对话中包含三项内容：你的提示和代理的回复、代理探索和编辑文件时的工具活动，以及可通过 `/diff` 检查的更改。

## 开始对话并请求更改

开始新的对话，以实现此功能。

1. 返回 Codespace。
2. 如果终端尚未打开，请按 <kbd>Control</kbd>+<kbd>\`</kbd>（Mac）或 <kbd>Ctrl</kbd>+<kbd>\`</kbd>（Windows/Linux）。
3. 如果 Copilot CLI 尚未启动，请运行以下命令：

   ```bash
   copilot --yolo
   ```

4. 输入斜杠命令 `/new`，然后按 <kbd>Enter</kbd> 开始新会话。
5. 使用以下提示请求更改：

   ```plaintext
   Show each game's starRating out of 5 in the game cards on the list page. If the rating is null, show "No rating yet". Keep the card layout as it is, add tests, and run the relevant checks.
   ```

Copilot 会探索项目，找到用于显示游戏详情的文件，并创建所需代码。你已使用 Copilot CLI 添加了新功能！

## 审查差异

所有 AI 生成的更改都应在合并前审查，即使是小改动也不例外。现在在 Copilot CLI 中检查更改。

1. 输入 `/diff` 并检查每个更改的文件。
2. 确认有评分时游戏卡片会显示数值，而 `starRating` 为 `null` 时会显示 `No rating yet`。
3. 确认测试覆盖这两种状态。
4. 查看 Copilot 运行的检查结果，并要求它修复任何失败项。
5. 审查完成后，按 <kbd>Esc</kbd> 退出差异视图。

> [!NOTE]
> 与所有生成式 AI 工具一样，Copilot 的结果具有概率性，并非完全确定，因此生成的代码可能不同。请检查实际行为，而不要期待某一种固定实现。

## 检查更改

不要只阅读代码就假定它能正常工作。请 Copilot 启动网站，然后在 Codespaces 转发的浏览器中检查更新后的用户界面 (UI)。

1. 请 Copilot 启动应用：

   ```plaintext
   Start the app so I can inspect the star-rating change in my browser. Tell me the URL and leave the server running.
   ```

2. 当 Codespaces 报告端口 `4321` 可用时，选择 **Open in Browser**。
3. 确认游戏卡片显示五分制评分。
4. 返回 Copilot，请它停止刚才启动的服务器：

   ```plaintext
   Stop the development server you started.
   ```

## 创建并合并你的第一个拉取请求

功能已创建。现在创建拉取请求 (PR)，将新代码合并到项目中。

1. 请默认代理提交更改：

   ```plaintext
   Commit the reviewed star-rating changes with an appropriate commit message.
   ```

2. 输入 `/pr create`。Copilot CLI 创建 PR 时会推送现有提交，并显示 PR URL。
3. 按住 <kbd>Command</kbd>（Mac）或 <kbd>Ctrl</kbd>（Windows/Linux），然后选择 Copilot CLI 显示的 URL 以打开 PR。
4. 审查更改的文件和检查结果。
5. 确认无误后，选择 **Merge pull request**，然后确认合并。
6. 返回 Codespace，并使用 `/exit` 退出 Copilot CLI。
7. 更新本地 `main`：

   ```bash
   git checkout main
   git pull
   ```

## 总结和后续步骤

恭喜！你已使用 GitHub Copilot CLI 发布了第一个更改。具体来说，你：

- 在功能分支中开始了一次专注的 Copilot 对话。
- 让代理小幅修改了游戏卡片。
- 使用 `/diff` 审查了更改。
- 运行应用，并在转发的浏览器中确认星级评分。
- 创建并合并了第一个拉取请求。

接下来，你将[从筛选议题开始，使用 Plan 和 Autopilot 模式][next-lesson]构建更大的功能。

## 资源

- [关于 GitHub Copilot CLI][about-copilot-cli]
- [Copilot CLI 命令参考][cli-reference]

[previous-lesson]: ../1-install-copilot-cli/
[next-lesson]: ../3-agent-modes/
[about-copilot-cli]: https://docs.github.com/copilot/concepts/agents/about-copilot-cli
[cli-reference]: https://docs.github.com/copilot/reference/copilot-cli-reference/cli-command-reference
